---
title: win下查看端口
date: 2016-12-11 16:52:54
tags: windows
categories: 运维
---
## 起因

jekyll的整个环境是运行在cygwin下面的，每次要在本次运行jekyll server的话，总是提示说是4000的端口被占用了。一只没有去找原因，偷懒加了个 --port 4400 来解决问题。

## netstat ##
今天打算去解决这个问题，那就看看是哪个程序在占用4000的端口吧。打开cmd窗口：

``$ netstat -aon | more``

看看是哪个PID在占用4000.通过PID去找到这个process。在task manager中去找PID。
是foxitprotect.exe，福昕的保护进程。把福昕卸载了。

问题解决了。话说，用什么看PDF呢？
