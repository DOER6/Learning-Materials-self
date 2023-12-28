## **PLCT Lab**

PLCT Lab 全称是程序语言与编译技术实验室，隶属于中国科学院软件研究所（ISCAS）智能软件研究中心（ISRC），致力于成为编译技术领域的开源领导者，推进工具链及运行时系统等软件基础设施的技术革新，具备主导开发和维护重要基础设施的技术及管理能力。与此同时，致力于培养一万名编译领域尖端人才，推动先进编译技术在国内的普及和发展。

我们相信 RISC-V 是指令集架构的未来。

+ #### BJ106 openEuler RISC-V 操作系统开发实习生

  岗位介绍:参与 openEuler 官方 risc-v sig 的维护工作，包含 compiler sig 的 LLVM 平行宇宙计划 RISC-V 方向实习生。

  实习内容：

  1. 跟踪 openEuler 在 RISC-V 架构的软件包构建情况并进行修复
  2. 参与以 llvm 构建发行版的「LLVM 平行宇宙计划」的软件包构建情况、进行尝试性修复与提交
  3. 协助 maintainer 调研并解决 oerv 系统 issue
  4. 构建并丰富openEuler软件生态，参加社区 SIG 组开源运作
  5. 调研分析操作系统领域最新动向和前沿技术，结合产品场景应用落地

+ #### 岗位要求:

  - 基础能力 Lv2 及以上。

  - 对 linux 发行版有一定使用经验。
  - 掌握中文普通话、英文[通常要求 CET4/6 通过]。
  - 微信响应速度快，每周7天中至少能够有3天、工作时间有至少连续3个小时在线一起工作。

- 如何正确的投递简历?
- 在投递简历之前最好对我们有更多一点了解。以下是阅读材料：

- 极简项目管理 是目前PLCT实验室的管理方式，实习生也在管理范围内。请先阅读。
- 我们如何进行实习生招聘
- 我们如何对实习生进行能力评定和培养
- 实习生生存手册 目前还在断断续续的撰写中，欢迎围观和贡献PR (Pull Requests)

阅读之后，接下来就可以发邮件了。以下内容请认真阅读。不符合条件邮件不会收到回复。

有意者请投递简历至：**吴老师 wuwei2016@iscas.ac.cn**

邮件标题请注明：**岗位编号 - 姓名 - 手机号码 - 学校**

（兼职实习的伙伴可以用【兼职】取代【学校】）

邮件正文请:**进行跟应聘职位相关的自我介绍**，不超过300字。

邮件必须附带简历。**没有PDF格式简历的邮件不保证会收到回复**。

- 通知上机考试的时间和登陆说明

  考试前15分钟可以登陆进入。请不要提前尝试登陆，密码输入错误IP会被ban两小时。

  == 登陆方式 ==

  ssh 你的GitHub账号名全小写@ep.plctlab.org

  登陆进去之后，用

  tmux attach || tmux

  进入考试环境。考题通过微信发送给你。

  没有使用过 ssh、tmux、命令行环境的同学请提前自学。

  == 考试规则 ==

  开放式。可以上网查询，可以看书，可以从Google上寻找已经有或者类似的答案。

  禁忌是不可以问其他人。直接求助其他人类视为作弊，失去资格。

#### 所有实习生共性要求（技术类）

开放岗位的入职要求（教学助理等非技术类的同学只需要满足前两条）：

1. 良好的沟通理解能力、能够观察和感知他人的态度和观点。能够主动沟通、遇到计划外或坏消息能够大声的说出来。
2. 知道如何陈述bugs/issues以及向其他人求助，如何不浪费同事的时间，将复现bug需要的信息提供完整。
3. 能力值评定一般要求达到LV2级别及以上。参见：我们如何面试实习生，我们如何给实习生评级。
4. 热爱编程，经常写代码。C/C++/Java/JavaScript 任何一种常见语言都可以。
5. 熟练使用 Linux 命令行；会一点 Python/Bash 脚本进行自动化。
6. 熟练使用 Google 搜索引擎、流畅高清看油管。
7. 熟练使用 Git，能够自己 rebase 解决 conflicts。
8. （加分）自学了 RISC-V 指令集，包括 RV32GC 和 RV64GC。在自己的电脑上部署运行起来QEMU-RISCV64以及Spike模拟器。
9. （加分）对于网络知识有基本了解并熟练使用，例如SSH任意端口登陆、Port Forwarding、反向链接、ProxyCommand 等配置自行掌握。

其他说明：所有岗位默认都是远程实习，支持全球实习工资支付（中国学生必须是国内银行卡，与软件所北京本部签约需要建设银行卡）。实习随时可以开始随时可以暂停随时可以结束（如果超过一周旷工、或八周没有外部可见产出会被劝退）。





面试官您好，接下来我大概花三分钟的时间介绍一下我自己，我叫王睿，是一名山东科技大学通信工程专业的大三学生，由于还是一名在校大学生，所以项目经验比较少，只有一些比赛和简单的实验项目





1."小狗状态"接口的设计要求编写一个接口DogState，其中包括一个void showState()方法。Dog类中包括一个DogState接口声明的变量State，并且有一个show()方法用于回调接口state的showState()方法。另外，需要编写实现DogState接口的类来描述小狗的各种状态，并在主类中测试小狗的各种状态。

1. **接口 `DogState`:**
   
   - 定义了一个带有 `showState()` 方法的接口。
   
2. **`Dog` 类:**
   - 拥有一个名为 `state` 的 `DogState` 字段。
   - 包含方法：
     - `show()`: 调用当前状态的 `showState()` 方法。
     - `setState(DogState s)`: 设置狗的状态。

3. **状态实现类:**
   
   - 三个状态类 (`MeetEnemyState`、`MeetFriendState` 和 `MeetAnotherDog`) 实现了 `DogState` 接口。
   - 每个状态类提供了自己的 `showState` 方法实现。
   
4. **`CheckDogState` 类（主类）:**
   - 包含 `main` 方法。
   
   - 创建一个 `Dog` 对象 (`yellowDog`) 并演示了状态的变化：
     
     ​	分别设置为 `MeetEnemyState`， `MeetFriendState`，`MeetAnotherDog`，展示状态。

实现了状态设计模式，允许 `Dog` 对象根据内部状态的变化动态改变其行为，展示了小狗在面对敌人、朋友或其他狗时的不同反应。



2.在Java GUI编程中，输入输出流通常用于处理与文件、网络、或其他数据源的交互。对于GUI应用程序，常见的输入输出流使用主要涉及到文件读写和网络通信。





### 技能与经验

- **编程语言：** 精通至少一门编程语言，包括C/C++/Java。具备基本的函数调用概念，能够编译和运行源代码，具备编写数组读入、排序、按照格式输出程序的能力。
- **脚本编程：** 熟练掌握Python/Bash脚本编程技能，能够通过自主学习理解给定脚本的含义，并灵活运用脚本解决问题。
- **软件开发：** 能够完成函数级别的功能开发，具备阅读代码、理解局部代码逻辑的能力。
- **沟通与记录：** 具备及时与mentor及同事沟通的能力，能够用文字记录工作，总结问题与经验。
- **Linux操作：** 具有Linux的使用经验，熟悉命令行操作，掌握常用命令如grep、find、date、sed、tr、head等。
- **版本控制：** 能够使用基本的git和GitHub/gitlab功能，包括但不限于clone、commit、push、branch、merge等。



以下是三个简单的C语言实现代码，分别对应一个命令行计算器、一个学生成绩管理系统以及一个猜数字的小游戏。

### 1. 命令行计算器

```c
#include <stdio.h>

int main() {
    char operator;
    double num1, num2, result;

    // 用户输入运算符和两个操作数
    printf("Enter an operator (+, -, *, /): ");
    scanf(" %c", &operator);

    printf("Enter two numbers: ");
    scanf("%lf %lf", &num1, &num2);

    // 根据运算符执行相应的计算o
    switch (operator) {
        case '+':
            result = num1 + num2;
            break;
        case '-':
            result = num1 - num2;
            break;
        case '*':
            result = num1 * num2;
            break;
        case '/':
            // 防止除数为零的情况
            if (num2 != 0) {
                result = num1 / num2;
            } else {
                printf("Error: Division by zero\n");
                return 1; // 返回非零值表示程序异常结束
            }
            break;
        default:
            printf("Error: Invalid operator\n");
            return 1;
    }

    // 输出计算结果
    printf("Result: %lf\n", result);

    return 0; // 返回零表示程序正常结束
}
```



### 2. 学生成绩管理系统

```c
#include <stdio.h>

#define MAX_STUDENTS 50

struct Student {
    char name[50];
    int id;
    float grades;
};

int main() {
    struct Student students[MAX_STUDENTS];
    int numStudents, i;
    float totalGrades = 0, average;

    // 输入学生数量
    printf("Enter the number of students: ");
    scanf("%d", &numStudents);

    // 输入学生信息和成绩
    for (i = 0; i < numStudents; ++i) {
        printf("Enter name of student %d: ", i + 1);
        scanf("%s", students[i].name);

        printf("Enter ID of student %d: ", i + 1);
        scanf("%d", &students[i].id);

        printf("Enter grades of student %d: ", i + 1);
        scanf("%f", &students[i].grades);

        totalGrades += students[i].grades;
    }

    // 计算平均分
    average = totalGrades / numStudents;

    // 输出学生信息和平均分
    printf("\nStudent Information:\n");
    for (i = 0; i < numStudents; ++i) {
        printf("Name: %s, ID: %d, Grades: %.2f\n", students[i].name, students[i].id, students[i].grades);
    }

    printf("\nAverage Grades: %.2f\n", average);

    return 0;
}
```

### 3. 猜数字游戏

```c++
#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main() {
    int secretNumber, guess, attempts = 0;

    // 生成随机数
    srand(time(NULL));
    secretNumber = rand() % 100 + 1;

    printf("Welcome to the Guess the Number Game!\n");

    do {
        // 用户输入猜测的数字
        printf("Enter your guess (1-100): ");
        scanf("%d", &guess);

        // 判断猜测是否正确
        if (guess > secretNumber) {
            printf("Too high! Try again.\n");
        } else if (guess < secretNumber) {
            printf("Too low! Try again.\n");
        }

        attempts++;

    } while (guess != secretNumber);

    // 输出猜测次数
    printf("Congratulations! You guessed the number in %d attempts.\n", attempts);

    return 0;
}
```



#### 1. C++ 程序设计：

在C++中，我牢固掌握了面向对象编程，能够有效地设计和实现数据结构和算法。通过实际项目，我获得了在系统开发、图形界面设计和游戏编程方面的经验。

#### 2. Java 程序设计：

我具备扎实的Java编程基础，能够开发后端服务和前端应用。我的项目经验包括使用Spring框架构建Web服务和Android应用程序的开发，展现了全栈开发的能力。

#### 3. 数据结构（C）：

在C语言环境下，我熟悉各类数据结构的设计和实现，包括链表、树等。我在项目中成功应用了数据结构来解决实际问题，提高了程序的效率。

#### 4. 计算机网络：

我了解计算机网络的基本原理，熟悉TCP/IP协议栈。通过参与网络通信模块的设计，我具备处理分布式系统和网络编程的实际经验。

#### 5. 操作系统与编程：

在操作系统方面，我学到了进程管理、内存管理和文件系统等核心概念。我能够在Linux环境下进行系统管理和Shell脚本编写，处理并发编程和线程同步问题。

#### 6. 总结：

通过这些学习和实践，我构建了跨足多领域的实际技能。我对技术问题有着实际的见解和解决方案，并在项目中展现了灵活性和适应能力。我期待通过RISC-V实习生岗位，将我的技能应用到实际项目中，为团队的成功做出贡献。



### 基础概念能力边界评估



[TOC]



##### int、float、double、char等基本数据类型的大小、范围以及在内存中的存储方式

1. **int：**
   - 大小：通常为4个字节，即32位。
   - 范围：约为 -2,147,483,648 到 2,147,483,647。
   - 存储方式：以二进制补码形式存储。
2. **float：**
   - 大小：通常为4个字节，即32位。
   - 范围：约为 3.4E-38 到 3.4E+38，但精度有限。
   - 存储方式：采用IEEE 754标准，将浮点数分为符号位、指数位和尾数位。
3. **double：**
   - 大小：通常为8个字节，即64位。
   - 范围：约为 1.7E-308 到 1.7E+308，具有更高的精度。
   - 存储方式：同样采用IEEE 754标准，但有更多的位数用于存储。
4. **char：**
   - 大小：通常为1个字节，即8位。
   - 范围：0 到 255 或 -128 到 127（取决于是否使用有符号类型）。
   - 存储方式：以ASCII码或其他字符编码方式存储字符。

这些数值和范围可能会因编译器和计算机体系结构的不同而有所变化。在实际编程中，可以使用`sizeof`操作符来获取各种数据类型在当前编译环境中的实际大小。


##### 描述一下OSI模型和TCP/IP模型，它们之间有什么区别？

**OSI模型（Open Systems Interconnection 模型）：**

OSI模型是一个由国际标准化组织（ISO）定义的框架，用于描述计算机或通信系统中不同层次之间的交互。它将网络通信划分为七个层次，每个层次都有特定的功能。这七个层次从下到上分别是：

1. **物理层（Physical Layer）：** 主要关注数据的物理传输，如电缆、光纤等。
2. **数据链路层（Data Link Layer）：** 负责将物理层提供的比特流组织成帧，并进行错误检测和纠正。
3. **网络层（Network Layer）：** 处理路由和逻辑寻址，负责将数据包从源主机传输到目标主机。
4. **传输层（Transport Layer）：** 提供端到端的通信控制，负责数据的分段和重组，以及错误检测和纠正。
5. **会话层（Session Layer）：** 负责建立、管理和终止会话（或连接）。
6. **表示层（Presentation Layer）：** 处理数据的格式化、加密和压缩，以确保两个系统能够互相理解。
7. **应用层（Application Layer）：** 提供网络服务给用户，包括文件传输、电子邮件等。

**TCP/IP模型：**

TCP/IP模型是实际使用最广泛的网络协议栈，它是基于实践而非理论的模型。它将网络通信分为四个层次，从下到上分别是：

1. **网络接口层（Link Layer）：** 相当于OSI模型中的物理层和数据链路层的结合，处理硬件设备和网络介质之间的通信。
2. **网络层（Internet Layer）：** 类似于OSI模型的网络层，负责数据的路由和寻址。
3. **传输层（Transport Layer）：** 类似于OSI模型的传输层，提供端到端的通信控制。
4. **应用层（Application Layer）：** 类似于OSI模型的最上层，提供网络服务给用户。

**区别：**

1. **层次差异：** OSI模型有七个层次，而TCP/IP模型只有四个。在TCP/IP模型中，数据链路层和物理层合并为网络接口层，而表示层和会话层的功能被包括在应用层中。
2. **发展历史：** OSI模型是在20世纪80年代初制定的，而TCP/IP模型是在20世纪70年代末和80年代初发展起来的。
3. **广泛应用：** TCP/IP模型是实际应用最广泛的模型，特别是在互联网领域。大多数互联网协议都是基于TCP/IP的。

尽管两者有区别，但可以通过对应层次之间的关系来映射它们，以便更好地理解和比较两个模型。



##### 什么是操作系统？操作系统的主要功能是什么？



**操作系统：**

操作系统是一种系统软件，它是计算机系统中的核心部分，负责管理和控制硬件资源，并提供给应用程序一个简单、一致的接口。操作系统的存在使得计算机硬件能够有效地运行各种应用程序，提供了用户与计算机之间的交互界面。

**操作系统的主要功能：**

1. **进程管理：**
   - 创建和终止进程。
   - 暂停和恢复进程的执行。
   - 进程间通信和同步。
2. **内存管理：**
   - 分配和释放内存空间。
   - 虚拟内存管理，允许程序使用比物理内存更大的地址空间。
3. **文件系统管理：**
   - 文件的创建、删除、读取和写入。
   - 目录管理和文件权限控制。
4. **设备驱动程序管理：**
   - 提供硬件设备的抽象接口。
   - 管理设备的输入和输出。
5. **用户界面：**
   - 提供命令行或图形用户界面，使用户能够与计算机交互。
   - 处理用户输入和输出。
6. **作业调度：**
   - 决定哪个进程在什么时候执行。
   - 优化系统性能，确保资源有效利用。
7. **网络管理：**
   - 提供网络服务和协议支持。
   - 管理网络连接和通信。
8. **安全和权限控制：**
   - 确保系统和数据的安全性。
   - 控制用户对系统资源的访问权限。
9. **错误处理：**
   - 监测和处理硬件和软件错误。
   - 提供错误日志和报告。
10. **系统资源管理：**
    - 管理CPU、内存、磁盘空间等硬件资源。
    - 优化资源分配，提高系统性能。

这些功能协同工作，使得操作系统能够有效地管理计算机系统，为应用程序提供良好的执行环境。在不同的操作系统中，这些功能可能有所差异，但总体上，操作系统的目标是提供一个方便、高效、安全的计算环境。



##### 什么是冯·诺依曼体系结构？



冯·诺依曼体系结构是一种计算机系统的基本设计原理，由约翰·冯·诺依曼（John von Neumann）于1945年提出。这种体系结构的关键思想是将计算机的存储器（Memory）、控制器（Control Unit）、运算器（Arithmetic Logic Unit，ALU）和输入/输出设备统一看作存储器，并将指令和数据以二进制形式存储在同一存储器中。

主要特征包括：

1. **存储程序概念：** 冯·诺依曼体系结构首次引入了存储程序的概念，即程序和数据存储在同一存储器中。这使得计算机可以按照存储在存储器中的程序顺序执行指令。
2. **指令和数据的二进制表示：** 冯·诺依曼体系结构中，计算机内部的指令和数据都以二进制形式表示，使得它们可以在同一存储器中存储和处理。
3. **按顺序执行指令：** 冯·诺依曼体系结构的计算机按照存储器中指令的顺序一步步执行，依次处理每一条指令，包括从存储器读取指令、解码指令、执行操作、存储结果等步骤。
4. **统一存储器结构：** 冯·诺依曼体系结构中，所有信息，包括指令和数据，都存储在同一存储器中。这与之前的计算机体系结构相比，具有更大的灵活性和通用性。
5. **由控制单元和算术逻辑单元组成：** 计算机的控制单元负责指令的控制和执行，而算术逻辑单元负责算术和逻辑运算。这两个单元协同工作，实现计算机的功能。

冯·诺依曼体系结构成为了现代计算机设计的基石，几乎所有的通用计算机都采用了这一体系结构。这种设计思想的普及推动了计算机科学和技术的发展，对计算机领域的进步产生了深远的影响。



##### 什么是编译器？编译器的主要任务是什么？

**编译器：**

编译器是一种计算机程序，用于将高级编程语言的源代码翻译成目标机器的可执行代码。编译器是一种独立于计算机体系结构的工具，它负责将程序员编写的高级语言代码转换为计算机硬件能够执行的机器代码。

**编译器的主要任务：**

1. **词法分析（Lexical Analysis）：**
   - 将源代码分割成一个个词法单元（Token），例如关键字、标识符、运算符等。
2. **语法分析（Syntax Analysis）：**
   - 将词法单元组织成语法结构，形成抽象语法树。
3. **语义分析（Semantic Analysis）：**
   - 确保程序语法正确，进行语义检查，例如类型检查、变量声明检查等。
4. **中间代码生成（Intermediate Code Generation）：**
   - 将抽象语法树转换为中间代码，这是一种介于高级语言和机器语言之间的表示形式。
5. **代码优化（Code Optimization）：**
   - 对中间代码进行优化，以提高程序性能，包括减小代码大小、提高执行速度等。
6. **代码生成（Code Generation）：**
   - 将优化后的中间代码翻译成目标机器的汇编语言或机器码。
7. **目标代码优化（Target Code Optimization）：**
   - 针对特定目标机器的代码进行优化，以最大程度地利用目标机器的特性和性能。
8. **目标代码生成（Target Code Generation）：**
   - 将最终优化后的代码生成目标机器能够执行的二进制代码。
9. **符号表管理（Symbol Table Management）：**
   - 维护程序中各种标识符（变量、函数名等）的信息，以便在编译过程中进行引用和查找。
10. **错误处理（Error Handling）：**
    - 检测并报告源代码中的错误，以帮助程序员进行调试。

编译器的主要目标是将高级语言代码翻译成可执行代码，同时尽可能地进行优化，以提高程序的性能和效率。不同编程语言可能有不同的编译器，而每个编译器都需要根据相应语言的语法和语义规则进行定制。



##### 什么是设计模式？举例说明一个常用的设计模式及其应用场景。

**设计模式：**

设计模式是在软件设计中常见问题的可重用解决方案。它们是一种为了提高代码可维护性、可读性和可重用性而被提炼出来的经验性的解决方案。设计模式不是可直接转化为代码的完整设计，而是一种描述一般设计问题和相应解决方案的方法。

**举例说明一个常用的设计模式及其应用场景：**

**设计模式：单例模式（Singleton Pattern）**

**定义：** 单例模式确保一个类只有一个实例，并提供一个全局访问点。

**应用场景：** 当一个系统中有且仅有一个对象负责某项任务，并且该对象在整个系统生命周期内需要保持一致时，使用单例模式是非常合适的。

**例子：**

```
javaCopy codepublic class Singleton {
    // 声明一个静态的实例变量
    private static Singleton instance;

    // 将构造方法私有化，防止外部直接实例化
    private Singleton() {
        // 私有构造方法
    }

    // 提供一个全局访问点获取实例
    public static Singleton getInstance() {
        if (instance == null) {
            // 如果实例不存在，创建一个新实例
            instance = new Singleton();
        }
        return instance;
    }
}
```

**解释：**

- 在这个例子中，`Singleton` 类有一个私有的静态实例变量 `instance`，并且私有的构造方法，防止外部直接实例化。
- 提供了一个全局的静态方法 `getInstance()` 来获取实例，确保只有一个实例存在。
- 如果实例不存在，则在第一次调用 `getInstance()` 时创建一个新的实例，以后每次调用都返回同一个实例。

**优点：**

- 确保了全局只有一个实例，节省了系统资源。
- 提供了一个全局访问点，方便对实例的控制。

**注意事项：**

- 在多线程环境下，需要考虑线程安全性，可以在 `getInstance()` 方法上加锁或使用双重检查锁定来确保线程安全。

这是设计模式中的一个简单示例，单例模式在实际应用中非常常见，例如数据库连接池、日志系统等。



##### 简要描述一下Git的基本工作流程是什么？



Git的基本工作流程涉及到本地仓库和远程仓库之间的协作。以下是Git的基本工作流程：

1. **克隆（Clone）：**

   - 使用 `git clone` 命令从远程仓库克隆项目到本地。这会在本地创建一个与远程仓库相同的副本。

   ```
   bashCopy code
   git clone <远程仓库URL>
   ```

2. **修改（Modify）：**

   - 在本地工作目录中修改文件。可以使用各种编辑器或IDE进行修改。

3. **添加（Stage）：**

   - 使用 `git add` 命令将修改的文件添加到暂存区。暂存区是一个中间区域，用于准备提交的文件。

   ```
   bashCopy code
   git add <文件名>
   ```

4. **提交（Commit）：**

   - 使用 `git commit` 命令将暂存区的文件提交到本地仓库，并附上相应的提交信息。

   ```
   bashCopy code
   git commit -m "提交信息"
   ```

5. **推送（Push）：**

   - 使用 `git push` 命令将本地仓库的提交推送到远程仓库。

   ```
   bashCopy code
   git push origin <分支名>
   ```

6. **拉取（Pull）：**

   - 如果其他人对远程仓库进行了修改，你需要将这些修改拉取到本地。使用 `git pull` 命令来获取并合并远程仓库的修改。

   ```
   bashCopy code
   git pull origin <分支名>
   ```

7. **分支（Branch）：**

   - 创建新的分支，用于独立开发某个功能或修复问题。使用 `git branch` 创建分支，然后使用 `git checkout` 或 `git switch` 切换到该分支。

   ```
   bashCopy codegit branch <分支名>
   git checkout <分支名>  # 或 git switch <分支名>
   ```

8. **合并（Merge）：**

   - 将一个分支的修改合并到另一个分支。通常在开发新功能后，将其合并回主分支。

   ```
   bashCopy codegit checkout <目标分支>
   git merge <源分支>
   ```

这是一个简单的Git基本工作流程示例。实际使用中可能会涉及更多操作，如解决冲突、创建标签等，但以上步骤涵盖了日常开发中的核心操作。



#### 带信号量操作和互斥

这是一个使用 pthread 和信号量（semaphore）的简单多线程程序，其中有两个线程：`computeThread` 和 `printThread`。

1. **头文件和全局变量：**
   
   ```c
   #include <pthread.h>
   #include <stdio.h>
   #include <semaphore.h>
   
   int buf = 0;                             // 全局变量 buf
   pthread_mutex_t mutex_x = PTHREAD_MUTEX_INITIALIZER;  // 互斥锁
   sem_t sem;                               // 信号量
   ```
   
2. **`computeThread` 函数：**
   ```c
   void *computeThread()
   {
       int i = 0;
       while (1)
       {
           pthread_mutex_lock(&mutex_x);   // 加锁
           while (buf != 0)
           {
               pthread_mutex_unlock(&mutex_x);  // 解锁，允许其他线程执行
               sched_yield();  // 让出 CPU，避免过多占用资源
               pthread_mutex_lock(&mutex_x);   // 再次加锁
           }
   
           buf = i;  // 将计算结果存入 buf
           printf("Computing buf=%d...", buf);
           i++;
           pthread_mutex_unlock(&mutex_x);  // 解锁
           sem_post(&sem);  // 发送信号通知 printThread 线程数据可用
       }
       return NULL;
   }
   ```

   - `computeThread` 负责计算并更新全局变量 `buf`，然后通过信号量通知 `printThread` 数据已准备好。

3. `printThread` 函数：**
   ```c
   void *printThread()
   {
       while (1)
       {
           sem_wait(&sem);  // 等待信号
           pthread_mutex_lock(&mutex_x);  // 加锁
           printf("buf=%d\n", buf);  // 打印 buf
           buf = 0;  // 清空 buf
           pthread_mutex_unlock(&mutex_x);  // 解锁
       }
       return NULL;
   }
   ```

   - `printThread` 等待信号，一旦收到信号，它就会打印 `buf` 的值，并将 `buf` 重置为 0。

4. **`main` 函数：**
   ```c
   int main()
   {
       sem_init(&sem, 0, 0);  // 初始化信号量
       pthread_t thread1_id, thread2_id;
   
       pthread_create(&thread2_id, NULL, &printThread, NULL);  // 创建 printThread 线程
       pthread_create(&thread1_id, NULL, &computeThread, NULL);  // 创建 computeThread 线程
   
       pthread_join(thread1_id, NULL);  // 等待 computeThread 线程结束
       pthread_join(thread2_id, NULL);  // 等待 printThread 线程结束
   
       return 0;
   }
   ```

   - `main` 函数初始化信号量，创建两个线程，并等待这两个线程的结束。其中，`printThread` 负责打印 `buf` 的值，而 `computeThread` 负责计算并更新 `buf`。这两个线程通过互斥锁 `mutex_x` 和信号量 `sem` 进行同步。
   
     
   

### cnt.c

这段 C++ 代码是一个简单的程序，用于统计给定字符串中的二元组和三元组的出现频率。让我逐行解释它：
       
     #include <iostream>
     #include <unordered_map>
     #include <algorithm>

上面这几行是包含所需的头文件，其中 `<iostream>` 用于输入输出操作，`<unordered_map>` 用于创建无序映射，`<algorithm>` 包含了一些算法。
   ``void countPairsAndTriplets(const std::string& input) {``

``		std::unordered_map<std::string, int> frequency;``
这里定义了一个函数 `countPairsAndTriplets`，它接受一个字符串 `input` 作为参数，并创建了一个无序映射 `frequency`，用于存储二元组和三元组的频率。
         for (size_t i = 0; i < input.length() - 1; ++i) {
             std::string pair = input.substr(i, 2);
             frequency[pair]++;
         }
       
这个循环遍历输入字符串，每次取两个字符作为一个二元组，然后将这个二元组作为键存储在 `frequency` 中，并增加对应的频率。
         for (size_t i = 0; i < input.length() - 2; ++i) {
             std::string triplet = input.substr(i, 3);
             frequency[triplet]++;
         }
类似地，这个循环遍历输入字符串，每次取三个字符作为一个三元组，然后将这个三元组作为键存储在 `frequency` 中，并增加对应的频率。
         for (const auto& entry : frequency) {
             std::cout << entry.first << " " << entry.second << std::endl;
         }
最后，这个循环遍历 `frequency` 映射中的所有键值对，输出二元组和三元组以及它们的频率。
     int main(int argc, char* argv[]) {
         if (argc != 2) {
             std::cerr << "ERROR: Need a string." << std::endl;
             return 1;
         }
         std::string input(argv[1]);
         std::transform(input.begin(), input.end(), input.begin(), ::tolower);
         countPairsAndTriplets(input);
         return 0;
     }
`main` 函数首先检查命令行参数的数量，确保只有一个字符串作为输入。然后，将输入字符串转换为小写形式（忽略大小写），最后调用 `countPairsAndTriplets` 函数来统计并输出二元组和三元组的频率。
       

### check.c

当然，我将更详细地解释每一句代码：
       
     ```cpp
     #include <iostream>
     #include <cmath>
     
     struct Point {
         double x, y;
     };
     ```

这部分代码引入了两个头文件，`<iostream>` 用于标准输入输出，`<cmath>` 提供了一些数学函数。接着定义了一个简单的结构体 `Point`，用来表示平面上的点，其中包含两个成员变量 `x` 和 `y` 表示横坐标和纵坐标。
       
     ```cpp
     bool onSegment(Point p, Point q, Point r) {
         if (q.x <= std::max(p.x, r.x) && q.x >= std::min(p.x, r.x) &&
             q.y <= std::max(p.y, r.y) && q.y >= std::min(p.y, r.y))
             return true;
         return false;
     }
     ```

这是一个辅助函数，用于检查点 `q` 是否在由 `p` 和 `r` 构成的线段上。它使用 `std::max` 和 `std::min` 函数来确保点 `q` 在以 `p` 和 `r` 为端点的线段上。
       
     ```cpp
     bool doIntersect(Point p1, Point q1, Point p2, Point q2) {
         double o1 = (q1.y - p1.y) * (p2.x - p1.x) - (q1.x - p1.x) * (p2.y - p1.y);
         double o2 = (q1.y - p1.y) * (q2.x - p1.x) - (q1.x - p1.x) * (q2.y - p1.y);
         double o3 = (q2.y - p2.y) * (p1.x - p2.x) - (q2.x - p2.x) * (p1.y - p2.y);
         double o4 = (q2.y - p2.y) * (q1.x - p2.x) - (q2.x - p2.x) * (q1.y - p2.y);
         if (o1 * o2 < 0 && o3 * o4 < 0) {
             return true;
         }
         if (o1 == 0 && onSegment(p1, p2, q1)) return true;
         if (o2 == 0 && onSegment(p1, q2, q1)) return true;
         if (o3 == 0 && onSegment(p2, p1, q2)) return true;
         if (o4 == 0 && onSegment(p2, q1, q2)) return true;
         return false;
     }
     ```

这是判断两条线段是否相交的函数。使用叉乘法计算四个交点的方向，并根据这些方向的符号关系判断两条线段是否相交。同时，还检查了端点是否在另一条线段上，以确保相交判定的正确性。
       
     ```cpp
     int main(int argc, char* argv[]) {
         if (argc != 9) {
             std::cerr << "ERROR: Invalid number of arguments." << std::endl;
             return 1;
         };
         Point L1P1 = {std::stod(argv[1]), std::stod(argv[2])};
         Point L1P2 = {std::stod(argv[3]), std::stod(argv[4])};
         Point L2P1 = {std::stod(argv[5]), std::stod(argv[6])};
         Point L2P2 = {std::stod(argv[7]), std::stod(argv[8])};
         if (doIntersect(L1P1, L1P2, L2P1, L2P2)) {
             std::cout << "TRUE" << std::endl;
         } else {
             std::cout << "FALSE" << std::endl;
         }
         return 0;
     }

这是主函数，用于处理程序的输入和输出。首先，检查命令行参数的数量是否为9，如果不是，输出错误信息并返回1。接着，使用 `std::stod` 将命令行参数转换为 `double` 类型，构造了表示两条线段的四个点 `L1P1`、`L1P2`、`L2P1` 和 `L2P2`。最后，调用 `doIntersect` 函数判断两条线段是否相交，如果相交则输出 "TRUE"，否则输出 "FALSE"。
       
    makefile

这是一个简单的 Makefile 文件，用于构建三个 C++ 程序：`mixplus`、`check` 和 `cnt`。以下是对每个部分的解释：
       
     1. `CC = g++`: 定义了一个变量 `CC`，用于指定 C++ 编译器，这里指定为 `g++`。
       
     2. `CFLAGS = -Wall -std=c++11`: 定义了一个变量 `CFLAGS`，用于指定编译选项，其中 `-Wall` 表示开启所有警告，`-std=c++11` 表示使用 C++11 标准。
       
     3. `all: mixplus check cnt`: 定义了一个伪目标 `all`，表示当执行 `make` 命令时，默认构建 `mixplus`、`check` 和 `cnt`。
       
     4. `mixplus: mixplus.c`: 定义了一个目标 `mixplus`，表示构建 `mixplus` 可执行文件，依赖于 `mixplus.c` 源文件。下面是构建规则：
       makefile
        $(CC) $(CFLAGS) -o mixplus mixplus.c
        ```

这里使用了 `g++` 编译器，传递了指定的编译选项 `-Wall -std=c++11`，并指定输出文件为 `mixplus`。
       
5. `check: check.c`: 类似于 `mixplus`，定义了目标 `check`，表示构建 `check` 可执行文件，依赖于 `check.c` 源文件。
       
   
        $(CC) $(CFLAGS) -o check check.c
    
6. `cnt: cnt.c`: 类似于上述目标，定义了目标 `cnt`，表示构建 `cnt` 可执行文件，依赖于 `cnt.c` 源文件。
       
   
        $(CC) $(CFLAGS) -o cnt cnt.c
    
7. `clean`: 定义了一个目标 `clean`，用于删除生成的可执行文件。规则为：
   
        rm -f mixplus check cnt
    

这里使用 `rm -f` 命令删除文件，`-f` 表示忽略不存在的文件，以避免出现错误。
在使用 `make` 命令时，它会根据依赖关系和规则构建相应的目标。例如，执行 `make all` 将构建所有可执行文件，执行 `make clean` 将删除生成的可执行文件。

### testcases.txt

这是一个测试用例文件，其中包含了一系列命令行测试案例，用于测试 `mixplus`、`check` 和 `cnt` 程序的不同情况。
1. **Mixplus Test Cases:**
 - `./mixplus 0x10 1`: 将两个参数相加，一个是十六进制数 `0x10`，另一个是十进制数 `1`。
- `./mixplus 10 0x1`: 同上，但参数顺序不同。
- `./mixplus 10`: 仅提供一个参数，测试程序对缺少参数的反应。
- `./mixplus 0x0dragonegg`: 包含非法字符的十六进制数，测试程序对输入的容错性。
- `./mixplus 10 0x`: 一个参数为十进制，另一个参数为空的十六进制字符串，测试程序对输入的容错性。
- `./mixplus 10 0xdragon`: 一个参数为十进制，另一个参数包含非法字符的十六进制数，测试程序对输入的容错性。
- `./mixplus 0xdeadbeef hello world`: 两个参数都包含非法字符，测试程序对输入的容错性。
- `./mixplus 10 0xdragon`: 一个参数为十进制，另一个参数为包含非法字符的十六进制数，测试程序对输入的容错性。
2. **Check Test Case:**
    - `./check 0 0 1 1 0 1 1 0`: 测试 `check` 程序，传递四个点的坐标，检查两线段是否相交。

3. **Cnt Test Case:**
   - `./cnt abcd`: 测试 `cnt` 程序，传递一个字符串，统计字符串中的两字符和三字符子串的频率。

这些测试用例旨在涵盖不同输入情况，以验证程序的正确性和容错性。在执行测试时，可以通过查看程序的输出来确认程序是否按照预期工作。

### mixplus.c

下面是对每一部分代码的详细解释：

```cpp
#include <iostream>
#include <iomanip>
#include <sstream>
#include <cctype>
```

这部分代码包含了程序所需的头文件，其中 `<iostream>` 提供了标准输入输出流，`<iomanip>` 提供了控制输出格式的工具，`<sstream>` 提供了字符串流的支持，`<cctype>` 提供了字符处理函数。

```cpp
int main(int argc, char* argv[]) {
    // Check input
    if (argc != 3) {
        std::cerr << "ERROR" << std::endl;
        return 1;
    }
    std::string input1(argv[1]);
    std::string input2(argv[2]);

    if (input1.empty() || input2.empty()) {
        std::cerr << "ERROR" << std::endl;
        return 1;
    }
```

在 `main` 函数开始，首先检查命令行参数的数量是否为3。如果不是，输出错误信息到标准错误流 (`std::cerr`)，并返回1表示程序异常终止。接着，将命令行参数中的两个字符串存储在 `input1` 和 `input2` 中。

```cpp
    int num1, num2;

    {
        std::istringstream ss1(input1);
        if (input1.substr(0, 2) == "0x") {
            ss1.ignore(2);

            for (size_t i = 0; i < ss1.str().size(); ++i) {
                input1[i + 2] = std::tolower(input1[i + 2]);
            }
            for (char c : input1.substr(2)) {
                if (!std::isxdigit(c)) {
                    std::cerr << "ERROR" << std::endl;
                    return 1;
                }
            }
            ss1 >> std::hex >> num1;
        } else {
            ss1 >> std::dec >> num1;
        }

        if (ss1.fail()) {
            std::cerr << "ERROR" << std::endl;
            return 1;
        }
    }
```

这一部分处理第一个输入字符串 `input1`。首先，使用 `std::istringstream` 创建一个字符串流 `ss1`，然后判断 `input1` 的前两个字符是否为 "0x"，如果是，则表示 `input1` 是一个十六进制数。接着，通过 `ss1.ignore(2)` 跳过 "0x" 的两个字符。

然后，使用一个循环将 `input1` 中除了前两个字符外的字符转换为小写，这是为了防止十六进制数中的字母为大写时，导致解析失败。

接着，通过一个循环检查除前两个字符外的部分是否都是有效的十六进制字符，如果包含非法字符，输出错误信息并返回1。最后，使用 `ss1 >> std::hex >> num1` 将转换后的字符串解析为整数 `num1`。

如果前面的操作失败，即解析出错，或者 `ss1.fail()` 返回 `true`，则输出错误信息并返回1。

```cpp
{
        std::istringstream ss2(input2);
        if (input2.substr(0, 2) == "0x") {
            ss2.ignore(2);
            for (size_t i = 0; i < ss2.str().size(); ++i) {
                input2[i + 2] = std::tolower(input2[i + 2]);
            }
            for (char c : input2.substr(2)) {
                if (!std::isxdigit(c)) {
                    std::cerr << "ERROR" << std::endl;
                    return 1;
                }
            }

            ss2 >> std::hex >> num2;
        } else {
            ss2 >> std::dec >> num2;
        }

        if (ss2.fail()) {
            std::cerr << "ERROR" << std::endl;
            return 1;
        }
    }
```

这一部分与前面的代码类似，处理第二个输入字符串 `input2`。同样，通过字符串流 `ss2` 处理 `input2`，判断是否为十六进制数，进行相应的处理，最终解析为整数 `num2`。

```cpp
    // Result
    int sum = num1 + num2;
    std::cout << std::uppercase << std::hex << "0x" << sum << " " << std::dec << sum << std::endl;
    return 0;
}
```

最后，计算 `num1` 和 `num2` 的和，存储在 `sum` 中。然后，使用 `std::cout` 输出结果的十六进制表示（带有 "0x" 前缀）和十进制表示，其中 `std::uppercase` 用于将字母转换为大写。最后，返回0表示程序正常结束。
