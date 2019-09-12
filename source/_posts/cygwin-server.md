---
title: Cygwin server
date: 2016-12-10 16:52:54
tags: cygwin
categories: 运维
---
## 安装cygwin server

cygserver是为Cygwin作为后台service运行而设计的。Linux的后台是daemon，Windows的后台是service。cygwin的程序要作为daemon运行，就必须成为win的service，这时候就需要cygserver。

在Cygwin中安装：

```c
cygserver-config
```
按照界面提示进行差一个server的安装，并同意将其安装为服务。

运行该服务

```c
cygrunsrv --start cygserver
```
cygrunsrv其实是启动的win的cygserver的service，可以在cmd中启动

```c
net start cygserver
```
