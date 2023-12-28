# pretask：通过qemu启动riscv架构的openeuler系统，并成功执行neofetch，并实现在本地和docker加速osc构建coretils



## 1.通过qemu启动riscv架构的openeuler系统，并成功执行neofetch

主要参考（openEuler-23.09-RISC-V-qemu-riscv64）：

[通过 QEMU 仿真 RISC-V 环境并启动 openEuler RISC-V 系统](https://www.openeuler.org/zh/blog/phoebe/2023-09-26-Run-openEuler-RISC-V-On-Qemu.html)
手动编译安装：``

```
wget https://download.qemu.org/qemu-8.1.2.tar.xz
tar -xvf qemu-8.1.2.tar.xz
cd qemu-8.1.2
mkdir res
cd res
sudo apt install libspice-protocol-dev libepoxy-dev libgtk-3-dev libspice-server-dev build-essential autoconf automake autotools-dev pkg-config bc curl gawk git bison flex texinfo gperf libtool patchutils mingw-w64 libmpc-dev libmpfr-dev libgmp-dev libexpat-dev libfdt-dev zlib1g-dev libglib2.0-dev libpixman-1-dev libncurses5-dev libncursesw5-dev meson libvirglrenderer-dev libsdl2-dev -y
../configure --target-list=riscv64-softmmu,riscv64-linux-user --prefix=/usr/local/bin/qemu-riscv64 --enable-slirp
make -j$(nproc)
sudo make install
```

然后将`/usr/local/bin/qemu-riscv64/bin`添加到`$PATH`环境变量中

- 文本编辑器打开`~/.bashrc`：

  ```bash
  vim ~/.bashrc
  ```

- 末尾添加以下行：

  ```bash
  export PATH=$PATH:/usr/local/bin/qemu-riscv64/bin
  ```

- 最后，重新加载`.bashrc`文件：

  ```bash
  source ~/.bashrc
  ```

下载磁盘镜像：需要下载启动固件 (fw_payload_oe_uboot_2304.bin)，磁盘映像(openEuler-23.09-RISC-V-qemu-riscv64.qcow2.xz)和启动脚本(start_vm.sh)。[repo.openeuler.org/openEuler-23.09/virtual_machine_img/riscv64/](https://repo.openeuler.org/openEuler-23.09/virtual_machine_img/riscv64/)

##### 启动虚拟机

- 确认当前目录内包含 `fw_payload_oe_uboot_2304.bin`，磁盘映像压缩包，以及启动脚本。
- 解压映像压缩包 `xz -dk openEuler-23.09-RISC-V-qemu-riscv64.qcow2.xz`
- 调整启动参数
- 执行启动脚本 `$ bash start_vm.sh`

##### neofetch：

 ``git clone https://github.com/dylanaraps/neofetch.git`

- 进入目录构建安装：`sudo make install`

![联想截图_20231218230427](C:\Users\17632\Pictures\联想截图\联想截图_20231218230427.png)

## 2.在openeuler本地进行构建

23.09 源没有 obs 需要从源码安装

obs 安装

1. osc 
   - `git clone https://github.com/openSUSE/osc.git`
   - `sudo make install`
2. 修改.oscrc文件：apiurl、user、passwd
   - `vim /home/admin/.oscrc `
3. obs平台的配置信息下载到本地
   - `osc co home:rainw:branches:openEuler:23.09:RISC-V/coreutils`
   - 同步到本地：`osc up -S`
   - commit时因为平台限制无法直接使用，一般通过修改_service文件来实现
4. obs-build
   - `git clone https://github.com/openSUSE/obs-build.git`
   - `sudo make install`

#### 直接进行osc build 会默认使用nspawn，但在`dnf install systemd-container`之后依旧显示该错误。

![image-20231220234625666](C:\Users\17632\AppData\Roaming\Typora\typora-user-images\image-20231220234625666.png)

`[  205s] /usr/lib/build/build-vm-nspawn: line 35: systemd-nspawn: command not found
[  206s] /usr/lib/build/build-vm-nspawn: line 41: systemd-nspawn: command not found`

#### 所以使用chroot来构建：

`osc build --no-verify --clean --vm-type=chroot`

![image-20231220234527792](C:\Users\17632\AppData\Roaming\Typora\typora-user-images\image-20231220234527792.png)

#### 构建成功：![image-20231220234914724](C:\Users\17632\AppData\Roaming\Typora\typora-user-images\image-20231220234914724.png)

## 3.加速构建

### docker

###### 1.官网下载docker for windows

###### [Docker: Accelerated Container Application Development](https://www.docker.com/)

###### 2.启动Hyper-v功能

将以下内容保存为.bat文件运行

```shell
pushd "%~dp0"

dir /b %SystemRoot%\servicing\Packages\*Hyper-V*.mum >hyper-v.txt

for /f %%i in ('findstr /i . hyper-v.txt 2^>nul') do dism /online /norestart /add-package:"%SystemRoot%\servicing\Packages\%%i"

del hyper-v.txt

Dism /online /enable-feature /featurename:Microsoft-Hyper-V -All /LimitAccess /ALL

pause
```

###### 3.打开windows 终端

手动更新

`wsl --update`

更新完成应显示：

![image-20231224001259157](C:\Users\17632\AppData\Roaming\Typora\typora-user-images\image-20231224001259157.png)

###### 4.docker构建

`osc build standard_riscv64 riscv64 --no-verify --clean --vm-type=docker`

![image-20231224005621371](C:\Users\17632\AppData\Roaming\Typora\typora-user-images\image-20231224005621371.png)

![image-20231224005634387](C:\Users\17632\AppData\Roaming\Typora\typora-user-images\image-20231224005634387.png)

### nspawn

`osc build standard_riscv64 riscv64 --no-verify --clean --vm-type=nspawn`

`osc build standard_riscv64 riscv64 --vm-type=nspawn`

`dnf install systemd-container`

问题：缺少build-initvm

但由于wsl-ubuntu是init启动，找不到systemd相关的包，nspawn构建暂未成功

## 参考

1. BuildService API **error**: can*'t verify packages due to lack of GPG keys*[如何通过OpenSUSE Open Build Service（OBS）构建软件包 - 迁移 - openEuler 论坛](https://forum.openeuler.org/t/topic/875/4)
2. OBS常用命令：[OBS 笔记 [misaka00251's Knowledge base\]](https://wiki.251.sh/openeuler_risc-v_obs)
3. nspawn加速[基于 systemd-nspawn 和 QEMU User Mode 搭建 openEuler RISC-V 软件包的快速开发环境 - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/528373554)