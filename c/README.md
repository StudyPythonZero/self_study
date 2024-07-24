## 简介  
c语言简单了解

## 目录
1. [格式](#1格式)
2. [基本数据类型](#2基本数据类型)
3. [变量](#3变量)(2024年7月25日学习到的地方)
4. [运算符]()
5. [分支循环]()
6. [数组]()
7. [字符串]()
8. [函数]()
9. [指针]()
10. [结构体]()
11. [预处理]()

## 内容
### 1.格式  
内容
```c
#include<stdio.h> // 引入库：标准输入输出
int main(void) // 定义主函数，输入为空
{
    printf("Hello world\n"); // 格式化打印内容,\n表示换行
    return 0; // 返回0，表示运转正常
}
```
输出结果：
```
Hello world

```  
[返回目录](#目录)  

### 2.基本数据类型
内容
```c
#include<stdio.h> 
int main(void) 
{
    // 注1：C语言只规定了short类型占用不能多于int，long类型占用不得少于int
    // 注2：关键字 unsigned 作为前缀只能用于非负数的场合
    // 注3：判断正负的方式为二进制最大的一位是否为0
    //      比如 0000 0000 0000 0001 是  1
    //      而   1000 0000 0000 0001 是 -1
    printf("%llu\n", sizeof(int)); 
    printf("%llu\n", sizeof(short));
    printf("%llu\n", sizeof(long));
    printf("%llu\n", sizeof(long long));
    // 注4：浮点数我只是简单了解，还没认真看，以后会更新笔记 2024.7.25留
    printf("%llu\n", sizeof(float));
    printf("%llu\n", sizeof(double));
    printf("%llu\n", sizeof(long float));
    // 注5：字符类型同注4 PS：粗略感觉没有char数组常用 2024.7.25留
    printf("%llu", sizeof(char)); 
    return 0; 
}
```

运行结果  
```
4
2
4
8
4
8
16
1
```
[返回目录](#目录)  

### 3.变量  
内容
```c
#include<stdio.h> 
void test(void);
// 变量可以在各种范围内定义
int number = 5; // 定义一个int类型的变量，变量名称为number，它的值为5，其他类型的变量定义同理
int main(void) 
{
    printf("%d\n", number);
    int number = 10; // 定义main函数范围内的局部变量number
    // 注1：当局部变量和全局变量同名时，局部范围内会优先使用局部变量
    printf("%d\n", number);
    number = 20; // 变量的值可以被改变
    printf("%d\n", number); 
    test(); // 注2：局部变量值的修改对全局同名变量没有影响
    return 0; 
}

void test(void) {
    printf("%d", number);
}
```

输出结果
```
5
10
20
5
```  
[返回目录](#目录)  
