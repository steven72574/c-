### 记录c++上课笔记，便于复习
创建文件，右键源文件，添加->新建项-> c++  
```c++
#include <iostream>
using namespace std;

int main() {
	int a = 10;
	cout << "hello world" ;//不换行
	cout << "换行" << endl; //endl 换行符
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
![image](https://user-images.githubusercontent.com/83968454/204139154-0b901a75-3dbf-4021-b445-935965255044.png)
```c++

float b = 3.14159f;//f可以将该该数字限定为float数据类型。而不加f，编译器默认该数字为double型
double c = 3.14159;
```
![image](https://user-images.githubusercontent.com/83968454/204139457-b58182e7-3dc6-4d87-b6e2-21823039b520.png)
