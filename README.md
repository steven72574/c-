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
