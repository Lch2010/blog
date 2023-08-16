---
layout: wiki
title: 快速入门 C++
cate1: C++
cate2:
description: 快速入门 C++
keywords: 入门, C++
---

此教程是为了让一些有编程基础的人快速入门 C++ 的，所以比较简洁，不会有详细解释

## C/C++ 编辑器

以下三个是比较常用的 C++ 编辑器

1. VSCode
2. Dev-C++
3. Vim

下载链接分别是：

- [VSCode](https://code.visualstudio.com/)
- [Dev-C++](https://sourceforge.net/projects/orwelldevcpp/)
- [Vim](https://www.vim.org/download.php)

作者首推 VSCode，然后是 Dev-C++

## 代码模板

```cpp
#include<bits/stdc++.h> //头文件
using namespace std; //名字空间
int main(){ //主函数
    cout<<"Hello! World!\n";
    return 0; 
}
```

## 头文件

调用头文件：`#include<文件名>`

万能头：`#include<bits/stdc++.h>`

万能头几乎包含所有常用头文件，除了 `windows.h`

## 定义变量

像 `int` `long` `double` `bool` `string` `char` 等都是 C++ 定义变量的关键字

`int a;` 定义一个整型 `a`

`string a;` 定义一个字符串 `a`

下表列出了许多类型的范围、占空间大小

|类型|字节数|范围|
|:-:|:-:|:-:|
|char|1|-128 到 127|
|unsigned char|1|0 到 255|
|int|4|-2,147,483,648 到 2,147,483,647|
|unsigned int|4|0 到 4,294,967,295|
|short int|2|-32,768 到 32,767|
|unsigned short int|2|0 到 65,535|
|long long|8|-9,223,372,036,854,775,808 到 9,223,372,036,854,775,807|
|unsigned long long|8|0 to 18,446,744,073,709,551,615|
|float|4|-3.4e38 到 3.4e38|
|double|8|-1.7e308 到 1.7e308|
|long double|16|-1.7e308 到 1.7e308|