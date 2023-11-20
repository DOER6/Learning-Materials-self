#### 1."小狗状态"接口的设计要求编写一个接口DogState，其中包括一个void showState()方法。Dog类中包括一个DogState接口声明的变量State，并且有一个show()方法用于回调接口state的showState()方法。另外，需要编写实现DogState接口的类来描述小狗的各种状态，并在主类中测试小狗的各种状态。

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



#### 2.在Java GUI编程中，输入输出流通常用于处理与文件、网络、或其他数据源的交互。对于GUI应用程序，常见的输入输出流使用主要涉及到文件读写和网络通信。





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

    // 根据运算符执行相应的计算
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

这些代码提供了基本的功能，可以根据实际需求进行修改和扩展。

