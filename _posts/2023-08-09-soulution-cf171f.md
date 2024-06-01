---
layout: post
title: CF171F 题解
categories: 题解
description: CF171F 题解
keywords: solution
mathjax: true
---

[题目传送门](https://www.luogu.com.cn/problem/CF171F)

#### 题目大意

求第 $$n$$ 个反转之后是另一个素数（注意反转之后与原数不同）的素数。

#### 思路

我们可以先将所有的素数都筛选出来，枚举 $$11$$ 到 $$106106$$ 中的数就可以了。再找反素数，就只要将一个数字反转，再判断是不是素数就可以了。是不是很简单？

#### AC code
```cpp
#include<bits/stdc++.h>
using namespace std;
const int N=10000005;
bool vis[N];
int p[N],cnt;
int c(int x){  
	int t=0;
	while(x){
		t=t*10+x%10;
		x/=10;
	}
	return t;
}
signed main(){
	ios::sync_with_stdio(false);
	cin.tie(0);cout.tie(0);
	int n;
	cin>>n;
	for(int i=2;i<=N;i++){
		if(vis[i]==0) p[++cnt]=i;
		for(int j=1;p[j]*i<=N&&j<=cnt;j++){
			vis[p[j]*i]=1;
			if(i%p[j]==0)		break;
		}
	}
	int g=0;
	for(int i=2;i<=N;i++){
		int x=c(i); 
		if(x==i) 				continue;
		if(!vis[i]&&!vis[x])	g++;
		if(g==n){
			cout<<i;
			return 0;
		}
	}
	return 0;
} 
```