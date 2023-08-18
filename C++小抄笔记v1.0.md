##### ![C++1920x1080](D:\MyGit\cpp-series\C++1920x1080.jpg)

------

笔者注:

​	本文系个人整理，已进行原创声明，如需转载或发表请联系作者。

联系方式 : 

- 公众号  -- python入门到进阶

- 微    信  -- W656824258

勘误:

由于我自己也不是资深编程高手，在创作此内容时尽管已经力求精准，查阅了诸多资料，还是难保有所疏漏，如果各位发现有误可以微信联系，欢迎指正。   



















<div style="page-break-after:always"></div>

[TOC]























<div style="page-break-after:always"></div>

# C++ 基本概念

## 一、第一个C++程序

```c++
#include <iostream>
using namespace std;

int main(){
	cout << "Hello World";
    return 0;
}
```

<div style="page-break-after:always"></div>

## 二、基本输入输出语句

```c++
// 声明一个变量
int number = 1;

// 声明一个常量
const double pi = 3.14;

// 数学表达式
int x = 10 + 3;

// 在控制台输出内容
cout << "x=" << x  << endl;  // endl 表示换行

// 从控制台读入数据
cin >> number;
```

<div style="page-break-after:always"></div>

## 三、数据类型

### 1、一些常用数据类型

```c++
// 数据类型
int age = 18;                  // 整型
double price = 9.99;           // 双精度浮点数
float interestRate = 3.67F;    // 单精度浮点数
long fileSize = 90000L;        // 长整型
char letter = 'a';             // 字符型
string name = "Wzs";           // 字符串
bool isValid = true;           // 布尔类型
auto years = 5;                // 自动识别数据类型 (C++11及以后支持)
```

### 2、数字系统

```c++
int x = 255;                   // 十进制数
int y = 0b111111;              // 二进制数
int z = 0xFF;                  // 十六进制数
```

### 3、数据类型占据空间和范围

```c++
int bytes = sizeof(int);
int min = numeric_limits<int>::min();  // int 类型所能存储最小值
int max = numeric_limits<int>::max();  // int 类型所能存储最大值
```

### 4、数组

``` c++
int numbers[] = {1, 2, 3};
cout << numbers[0];          // 理解数组下标从零开始即可
```

### 5、数据类型转换

```c++
// C语言风格的数据类型转换
double a = 2.0;
int b = (int) a;

// C++风格的数据类型转换
int c = static_cast<int>(a);
```

<div style="page-break-after:always"></div>

## 四、判断语句

### 1、比较运算符

```c++
bool a = 10 > 5;
bool b = 10 == 10;
bool c = 10 != 5;
```

### 2、逻辑运算符

```c++
bool d = a && b;               // 逻辑与  --->  左右同时为真，结果为真
bool e = a || b;               // 逻辑或  --->  左右一边为真，结果为真
bool f = !a;                   // 逻辑非  --->  真变假，假变真
```

### 3、if....else if...else语句

```c++
if (temperature < 60){
  // ...
}
else if (temperature < 90){
  // ...
}
else{
  // ...
}
```

### 4、条件运算符

```c++
double commission = (sales < 10'000) > .05 : .1;
```

### 5、switch语句

```c++
switch (menu){
  case 1:
    // ...
    break;
  case 2:
    // ...
    break;
  // ...
  default:
    // ...
}
```

<div style="page-break-after:always"></div>

## 五、循环语句

### 1、for循环

```c++
for (int i = 0; i < 5; i++)
  	cout << i;
```

### 2、while循环

```c++
int i = 0;
while (i < 5){
  cout << i << endl;
  i++;
}
```

### 3、do...while循环

```c++
int i = 0;
do{
  cout << i << endl;
  i++;
}while (i < 5);
```

### 4、基于范围的for循环

```c++
int numbers[] = {1, 2, 3};
for (int number: numbers)
  	cout << number << endl;
```

<div style="page-break-after:always"></div>

## 六、函数

### 1、定义函数

```c++
// 无返回值的函数
void greet(string name){
	cout << "Hello " << name;
}

// 有返回值的函数
string fullName(string firstName, string lastName){
    return firstName + " " + lastName;
}
```

### 2、使用默认值参数

```c++
double calculateTax(double income, double taxRate = .2){
    return income * taxRate;
}
```

### 3、函数重载

```c++
void greet(string name){
    cout << "Hello " << name;
}

void greet(string title, string name){
    cout << "Hello " << title << " " << name; 
}
```

 ### 4、引用传参

```c++
void incresePrice(double &price){
    price *= 1.2;
}
```

### 5、函数声明

```c++
void greet(string name);
```

### 6、定义命名空间

```c++
namespace messaging{
  	void greet(string name){}
}
```

### 7、使用命名空间

```c++
using namespace messaging
// or
using messaging::greet;
```

