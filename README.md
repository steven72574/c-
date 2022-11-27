### 记录c++上课笔记，便于复习
创建文件，右键源文件，添加->新建项-> c++  
cout默认输出六位有效数字，超过的部分会用科学计数法表示。
```c++
#include <iostream>
using namespace std;

int main() {
	int a = 10;
	cout << "hello world" ;//不换行
	cout << "换行" << endl; //endl 换行符与 \n作用一样
	cout << “换行\n” ; 
	cout << "a =" << a << endl; // “ << ”相当于拼接符，java中字符串拼接的 “+”
	
	system("pause");
	return 0;
}
```
### 注释（c++与java注释语法相同）
单行注释 //  
多行注释/* 描述信息*/  

### 变量
定义：给一段内存空间起名，以方便操作这段内存  
变量可以用科学计数法；  
``` c++
float a = 2e3; // 输出2000
float b = 2e-3; // 输出 0.002  
```
### 常量
记录程序中不可更改的数据  
有两种方法  
定义变量名时不要用关键字  
```c++
#define day 10 ;//宏常量
const int a = 10;//在变量定义前加关键字const
```
### 标识符（变量名）命名规则
1.标识符不能是关键字  
2.只能由字母数字、下划线  
3.第一个字母必须为字母或下划线，不能为数字  
4.字母区分大小写  
## 数据类型

__sizeof( 数据类型/变量) ： 可以统计数据类型占内存的大小__  

### 整型
![image](https://user-images.githubusercontent.com/83968454/204138895-3e925fcd-da8b-4f70-9858-65d3e257ed56.png)  

### 实型（浮点型）
小数点后的数字位数为有效数字  
cout默认输出六位有效数字，超过的部分会用科学计数法表示。
![image](https://user-images.githubusercontent.com/83968454/204139154-0b901a75-3dbf-4021-b445-935965255044.png)
```c++

float b = 3.14159f;//f可以将该该数字限定为float数据类型。而不加f，编译器默认该数字为double型
double c = 3.14159;
```
![image](https://user-images.githubusercontent.com/83968454/204139457-b58182e7-3dc6-4d87-b6e2-21823039b520.png)

### 字符型（基本和java一样）
字符变量占用一个字节  
字符型变量存储Ascii编码  
常见ASCII码值：  
'a' -> 97  
'A' -> 65  
'0' -> 48  
```c++
char ch = 'a';
char ch1 = 97;//可以直接赋值
cout << ch - '0' << endl; //和java一样，字符型之间可以直接加减
cout << (int)'A' << endl; //计算ACSII码值
```
### 转义字符
\t  制表符  能够让后面的内容对齐  
```c++
cout << "aaaa\tHelloWorld'n";
cout << "aa\tHelloWorld'n";
cout << "aaaaaa\tHelloWorld'n";
```
![image](https://user-images.githubusercontent.com/83968454/204140505-2425fc6e-60d4-408e-8e50-804d3c164daf.png)  
\n  换行符，与cout << endl 中的endl一样作用  
\\ 代表 一个反斜杠 '\'   
\'  
\"  
\?  


### 字符串型
有两种风格  
1.c风格型  
```c++
char str1[] = "This is a string";
```
2.c++风格
```c++
string str2 = "This is another string";
```
vs2019之前，用string 声明字符串前，要加string头文件。
```c++
#include<string>
```

### 布尔型
bool 占用一个字节空间  
输入的值只要非零都为真  
```c++
bool b = true;
b = 1; //这种赋值也可以
bool c = false;
c = 1;
cout << b << endl; //输出1
cout << c <, endl; //输出0
```

### 数据的输入
cin >> 变量名  

### 运算符
加减乘除和Java一样  
两小数相除才是小数  
有一方是浮点型，则结果是浮点型(和java一样)  
自增自减符和java一样  

```c++
	int a = 7;
	int b = 3;
	cout << a / b << endl; //两整数相除会取整数部分，和Java一样
	cout << a % b << endl; //求余数，注意，两个小数不能取模运算，但是java可以
```
__赋值运算与java一样__  
```c++
 int a = 10;
 a += 2;
```
__比较运算符与java一样__
![image](https://user-images.githubusercontent.com/83968454/204142298-f9327b26-9299-4363-ade0-e22da1db828b.png)
```c++
	int a = 110;
	int b = 10;
	cout << (a == b) << endl; //要加括号，这里是要注意的地方
```
__逻辑运算符与java一样__
```c++
! 	//非
&&	//与
||	//或
```

### 程序流程结构
顺序结构  
选择结构，如if  
循环结构  
### if语句（和java一样）
```c++
#include <iostream>
using namespace std;

int main() {
	
	int a = 0 ;
	cout << "输入你的分数\n";
	cin >> a;
	if (a >= 60) {
		cout << "恭喜你及格啦\n";
	}
	else if(a >= 50){
		cout << "很遗憾你没有及格，但是很接近及格，继续加油哦\n";
	}
	else {
		cout << "很遗憾你没有及格，请再接再厉吧\n";
	}
	system("pause");
	return 0; 
}
```
### 三目运算符（三元运算符，和java一样）
表达式1? 表达式2：表达式3
表达式1为 __true__ 则 执行表达式2，否则执行表达式3

### switch 语句(和java一样)
switch判断时只能是整型或者字符型，不能是一个区间。但优点是结构清晰，执行效率高。  
若无break，则实行完一个case语句，会接着执行下一个case语句  
若case中的条件都不满足，则执行break  
```c++
#include <iostream>
using namespace std;

int main() {
	
	cout << "输入这部电影的分数(1-5)\n";
	int score = 0;
	cin >> score;
	switch (score) {
	case 1:
		cout << "电影很烂\n";
		break;
	case 2:
		cout << "电影一般般，没有亮点\n";
		break;
	case 3:
		cout << "电影还行，凑合着看\n";
		break;
	case 4:
		cout << "电影挺不错的，好看\n";
		break;
	case 5:
		cout << "这部电影非常棒啊，强推\n";
		break;
	default:
		cout << "输入的分数不在范围内哦\n";
		break;
	}

	system("pause");

	return 0; 
}
```

### while语句（和java一样）
while(判断条件){
}

### do while语句（和java一样）
do {}while()

### for循环（和java一样）
continue break关键字也和java一样  

### goto语句（跳到标记直接执行，最好不好使用,不方便阅读，因为会跳来跳去）
goto 标记;
标记一般是大写;
```c++
#include <iostream>
using namespace std;

int main() {
	
	cout << "1" << endl;
	goto Jump;
	cout << "2" << endl;
	cout << "3" << endl;
	cout << "4" << endl;
	
	Jump: //标记处用的是冒号，不是分号

	cout << "5" << endl;

	system("pause");
	return 0; 
}
```
### 数组
数组声明方式，和java很不同
```c++
//C++ 数组声明
int a[10];
int b[2] = { 1,2 };
int c[] = { 1,2,3 };
sizeof(a);//获取数组在内存中的长度，和java不同
cout << &a[0] << endl; // 取址符 &，取元素在内存中的地址  
int length = sizeof(a)/sizeof(a[0])//获取数组元素个数，也就是java的数组长度a. length
```
```java
//Java 数组声明
int[] a;
int[] b = new int[2];
int[] c = new int[]{1,2,3};
```
__二维数组__
```c++
int arr1[2][2];
int arr3[2][3] = //最推荐的
{
	{1,2,3},
	{4,5,6}
};
int arr2[2][3] = { 1, 2 ,3, 4 ,5 ,6};//会自动根据每行有3个元素，分为两行
int arr4[][3] = { 1, 2 ,3, 4 ,5 ,6};//根据列的元素个数，自动分行，但是a[2][]则是不行的
```

### 6.函数（和java非常类似）
函数要在主函数之前，要不然找不到。或者在主函数前声明函数（没有函数体语句，只有头,如下），告诉编译器有这个函数。
```c++
int getSum(int a, int b);
```
函数的值称为形式参数  
实际传入的值为实际参数  

### 函数分文件编写
1.创建.h后缀名的头文件  
![image](https://user-images.githubusercontent.com/83968454/204148747-057b9820-9520-466e-b6b6-62c62770ed9b.png)  
2.创建.cpp后缀名的源文件  
![image](https://user-images.githubusercontent.com/83968454/204148795-fab1b268-d304-46db-baad-56470a2961ad.png)  
3.在头文件中添加函数声明  
4.在源文件中添加函数定义（编写函数）  
然后在源文件中添加
```c++
#include "getSum.h"  
```
最后在主函数把头文件include进来

## 7.指针
指针实际上也是一种数据类型，可以通过指针保持一个变量的地址。  
在32位操作系统下占 __4__ 字节  
在64位操作系统下占 __8__ 字节  
__空指针__：指向内存中编号为0的指针，这块内存是不能访问的。空指针用于初始化指针变量  
__野指针__: 指针变量指向非法的内存空间  
空指针和野指针都不是我们申请的空间，因此不要访问，访问会出错  
![image](https://user-images.githubusercontent.com/83968454/204150428-a92a559e-8b6b-46f0-a0bd-d22d78f56183.png)  

```c++
#include <iostream>
using namespace std;

int main() {

	int* p;//定义指针
	int a = 10;
	p = &a;//p存储a的内存地址
	cout << *p << endl;  //获取该内存地址存放的值
	
	system("pause");
	return 0; 
}
``

__常量指针__:指针的__指向__可以改，但是该指针__指向的值__不能改，如下图  
__指针常量__:指针__指向的值__可以改，但是__指向__不能改。
```c++
int main() {
	
	int a = 10;
	int b = 20;
	const int* p = &a;
	*p = 20; //会报错
	p = &b; //这个操作可以

	system("pause");
	return 0; 
}
```
