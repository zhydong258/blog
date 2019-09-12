---
title: Hello World
date: 2016-06-18 16:52:54
tags:
---
我已经记不得这算是我的第几个blog了。前前后后大概也要有四、五个了吧。希望这个可以一直写下去。
既然是以github来搭建的blog，那就先来说说，怎么用github来建立个人blog吧。

## 准备

你必须要有一个github的帐号，这个必须有。
登录github，建立USERNAME.github.com的仓库。当然，USERNAME是你自己的用户名。

## 开始

```
git clone https://github.com/plusjade/jekyll-bootstrap.git USERNAME.github.com
cd USERNAME.github.com
git remote set-url origin git@github.com:USERNAME/USERNAME.github.com.git
git push origin master
```
使用jekyll-bootstrap作为快速开始的基础。
[Jekyll QuickStart](http://jekyllbootstrap.com/usage/jekyll-quick-start.html) jekyll bootstrap的3分钟建站教程。

## 编写日志

``rake post title="Hello World"``

会在_posts文件夹下面生成一个已YYYY-MM-DD-title.md的文件，使用Markdown的语法编辑这个文件。

## 本地发布

如果要在本地查看的话，你需要jekyll。当然，jekyll是基于ruby的，你同样需要ruby。
```
$ cd USERNAM.github.com
$ jekyll server --port 4400
```

在浏览器中打开localhost:4400，就可以看到了。

## 发布

```
$ git add .
$ git commit -m "Add new content"
$ git push origin master
```
在浏览器中打开https://USERNAME.github.com，看看自己的第一篇blog吧。
