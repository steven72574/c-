##STL(Standard Template Library)标准模板库  
STL广义上分为：容器（container）,算法（algorithm），迭代器（iterator）  
容器和算法之间通过迭代器无缝连接  
STL几乎所有代码采用了模板类或模板函数  
STL六大组件：
1.容器：各种数据结构，vector，list，deque，set，map等，用于存放数据  
2.算法，如sort，find，copy，for_each等  
3.迭代器：使容器和算法间无缝衔接，能够依序寻访某个容器所含的各个元素，又无需暴露该容器的内部表示方式，且每个容器都有自己的迭代器    
4.仿函数：行为类似函数，可作为算法的某种策略  
5.适配器：一种用来修饰容器或者仿函数或迭代器接口的东西  
6.空间配置器：负责空间的配置和管理  

迭代器种类  
常用容器中的迭代器为双向迭代器和随机迭代器  
![image](https://user-images.githubusercontent.com/83968454/206591298-150f9b1b-2cba-42d6-ae19-c0232515f3e6.png)  
# Vector 容器
```c++
#include <iostream>
using namespace std;
#include"template.h"
#include<vector>

class Person
{
public:
    Person(string name, int age)
    {
        myName = name;
        myAge = age;
    }
    string myName;
    int myAge;
};
int main()
{   //**************************************************int类型
    vector<int> v;
    v.push_back(10);//就是java Arraylist的add
    v.push_back(20);
    v.push_back(30);
    v.push_back(40);
    //遍历方式
    for (vector<int>::iterator it = v.begin(); it < v.end(); it++) {
        cout << *it << endl;
    }
    //****************************************************自定数据类型
    Person p1("aa", 18);
    Person p2("bc", 20);
    vector<Person> vp;
    vp.push_back(p1);
    vp.push_back(p2);

    for (vector<Person>::iterator it = vp.begin();it < vp.end(); it++) {
        cout << it->myName << " "<<(*it).myAge << endl;
        
    }
    
}
```
# string 容器
string是c++风格的字符串，而string本质上是一个类  
string内部封装了char*，所以是类在管理c语言的字符  
### string的构造函数
string();创建空字符串  
string(const char\*s);使用c风格字符串c初始化  
string(const string& str);使用另一个string初始化  
string(int n,char c);  
### string赋值
![image](https://user-images.githubusercontent.com/83968454/206595145-fff3a46c-5033-4d7d-b9a1-603764e39df3.png)  
### string字符串拼接  
![image](https://user-images.githubusercontent.com/83968454/206595306-295f5af5-abe7-4b88-a120-9736bf8a0146.png)  
### string字符串查找与替换
![image](https://user-images.githubusercontent.com/83968454/206595560-f98f9194-ef38-4dcf-8c05-d95b9a749b08.png)  
### string字符串的比较
![image](https://user-images.githubusercontent.com/83968454/206595688-a2ab623d-d532-4cb0-b42a-641dfcc341ef.png)  
### string字符串存取
![image](https://user-images.githubusercontent.com/83968454/206595774-98c1954c-7114-47dd-9afb-dcde98cad6cd.png)  
### 字符串的插入和删除
![image](https://user-images.githubusercontent.com/83968454/206595890-264754fa-dd12-4615-bf5b-f6d234acf88d.png)  
### 子串
![image](https://user-images.githubusercontent.com/83968454/206595956-63924037-09d1-4a9d-8292-d4cb484525ec.png)  


 



