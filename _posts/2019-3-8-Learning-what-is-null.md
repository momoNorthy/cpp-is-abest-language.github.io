# 一·什么是"NULL"
######  节选至<cstdio>(iostream里也有)
```
namespace std
{
  #if !defined(DEFINED_NULL)
  #if !defined(__cplusplus)
  #define NULL ((void*)0)
  #else
  #define NULL 0
  #endif
  #define DEFINED_NULL
  #endif
```
######  所以，在main.cpp中，写如下代码：
```
#include<iostream>
void fool(int*a){std::cout<<"int ptr"<<std::endl;}
void fool(int a){std::cout<<"int value"<<std::endl;}
int main()
{
  fool(NULL);
}
```
得到：`int value`
### 证明了NULL就是0（在c++中）
`更新时间：2019.3.8日`
