### 记录c++上课笔记，便于复习
创建文件，右键源文件，添加->新建项-> c++
```c++
#include <iostream>
using namespace std;

int main() {
	int a = 10;
	cout << "hello world" ;//不换行
	cout << "换行" << endl; //endl 换行符
	cout << "a =" << a << endl;
	
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
```c++
#define day 10 ;//宏常量
const int a = 10;//在变量定义前加关键字const
```
