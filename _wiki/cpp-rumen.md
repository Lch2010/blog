---
layout: wiki
title: c++入门（略详）
cate1: C++
cate2:
description: c++入门（略详）
keywords: 入门, C++
---

C++ 新手入门指北

**请关注[lianchanghua](https://www.luogu.com.cn/user/564475)谢谢喵。**

## P1：基础设备。

知周所众，拥有一个好的设备，是一个 OIer 必不可少的基础，所以，作者来推荐一下新手应该用的好设备：

- 硬件：能跑代码就行，不要多高级。（最好 win8 及以上，原因请看下方）
- 软件：大家比较常用的有这几种：
1. [Dev-C++(新手必备)](https://sourceforge.net/projects/orwelldevcpp/)
1. [VS code(老 OIer的最爱)](https://code.visualstudio.com/)
1. [Red Panda(老少皆宜，作者主推)](https://royqh1979.gitee.io/redpandacpp/)

这个看自己喜好，不过作者真的十分推荐 Red Panda，为什么呢？当然不是我收钱了，这个 Red Panda 介于 Dev_C++ 和 VS code 之间，可谓是十分友好，缺点嘛，就是实时编译和自动补全，不过是可以关掉的，喜欢的朋友可以去试试。

然后这个 VS code 需要 win8 及以上的电脑，不过也有 [win7的](https://code.visualstudio.com/updstes/v1_70)
，还有[网页版的](https://vscode.dev)。

最后，就是我们的 Dev C++了，新手基本都用这个，也是比较好用的。


## P2：入门语法

我们学汉语，从拼音开始，我们学英文，从字母开始。而我们学 C++，从框架开始。

下面是一个基本的框架：
```cpp
#include<iostream>
using namespace std;
int main(){
  return 0;
}
```
我们来看第一行`#include<iostream>`，这里，`include<...>`是头文件，里面可以填充其他头文件名，这里，建议使用万能头，包含几乎所有常用头文件，当然，副作用就是编译速度慢，可是带来的优点也是很明显的：不用背其他头文件。

[使用万能头与不使用万能头的对比](https://www.luogu.com.cn/paste/5xar8y1h)

怎么样？是不是万能头更方便？

剩下的其实没有那么重要了，可忽略（我才不会告诉你是我也不太清楚了呢！╭(╯^╰)╮）。

好了接着奔向我们的语法部分，真正开启我们 C++ 路上的新征程！

### 输入与输出（cin,cout VS scanf,printf）

初学这的第一个程序是什么？

那肯定是输出 `Hello,World!`。

那么我们应该怎么输出呢？

这就邀请出这两位大神：`cout` and `printf`！

下面是 `cout` 的操作。
```cpp
#include<bits/stdc++.h>
using namespace std;
signed main(){
  cout<<"Hello,World!";
  return 0;
}
```

下面是 `printf` 的操作。
```cpp
#include<bits/stdc++.h>
using namespace std;
signed main(){
  printf("Hello,World!");
  return 0;
}
```
然后，你就可以去切[这道题](https://www.luogu.com.cn/problem/B2002)了。然后，恭喜你！获得了人生中，首个 AC！

然后，光说不行呀！还得听别人讲，所以，又搬出了我们的好朋友 `cin` and `scanf`。

下面以 A+B 为示例：

`cin` 版

```cpp
#include<bits/stdc++.h>
using namespace std;
int main(){
  int a,b;
  cin>>a>>b;
  cout<<a<<b;
  return 0;
}
```

`scanf` 版

```cpp
#include<bits/stdc++.h>
using namespace std;
int main(){
  int a,b;
  scanf("%d%d",&a,&b);
  printf("%d",a+b);
  return 0;
}
```

参考资料：[lanruixiang的blog](https://lanruixiang.github.io/wiki/cpp-rumen/)
