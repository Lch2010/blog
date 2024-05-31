---
layout: post
title: CF468A 题解
categories: 题解
description: CF468A 题解
keywords: solution
mathjax: true
---

感谢 @[I_like_magic_200911](https://www.luogu.com.cn/user/778235) 帮忙修改 Markdown 和 $$\LaTeX$$


我们先在纸上模拟一遍，可以发现：

- 如果 $$n<4$$，那么便是无解。

- 在 $$n>4$$ 的情况下，可以发现一套通法：
    
在 $$n$$ 为奇数时，方法如下：

$$5 \times 4 = 20$$

$$20 + 3 = 23$$

$$23 + 2 = 25$$

$$25 - 1 = 24$$

最后，不停地乘 $$1$$ 即可；
        
在 $$n$$ 为偶数时，方法如下： 

$$1 \times 2 = 2$$  

$$2 \times 3 = 6$$	

$$4 \times 6 = 24$$

最后，不停地乘 $$1$$ 即可。
      
```cpp
#include<bits/stdc++.h>
#define int long long 
using namespace std;
signed main(){
    int n;
    cin>>n;  
	if(n<4){//4以下无解 
		cout<<"NO";
		exit(0);
	}
    cout<<"YES"<<"\n";
    if(n%2){//判断奇偶
    	//奇数情况 
    	cout<<"5 * 4 = 20"<<"\n";
		cout<<"20 + 3 = 23"<<"\n";
		cout<<"23 + 2 = 25"<<"\n";
		cout<<"25 - 1 = 24"<<"\n";
		for(int i=n;i>=6;i-=2){
			cout<<i<<" - "<<i-1<<" = "<<"1"<<"\n";
			cout<<"24 * 1 = 24"<<"\n";
		}
	}
    else{
    	//偶数情况 
		cout<<"1 * 2 = 2"<<"\n";
		cout<<"2 * 3 = 6"<<"\n";
		cout<<"4 * 6 = 24"<<"\n";
		for(int i=n;i>=5;i-=2){
			cout<<i<<" - "<<i-1<<" = "<<"1"<<"\n";
			cout<<"24 * 1 = 24"<<"\n";
		}
    }
    return 0;
}
```
$$2023.7.19$$ 修改注释，感谢@[Tjaweiof](https://www.luogu.com.cn/user/550933)

$$2023.7.24$$ 修改解释，感谢@[Soul_Seeker](https://www.luogu.com.cn/user/947270)
