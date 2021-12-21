---
title: How to upgrade Hexo to latest?
date: 2020-12-04 13:47:42
tags: Hexo
categories: 运维 
---

今天又想起来自己在Github的博客了，从上面clone下来，重新安装了nvm和lts的node。发现hexo版本比较低，决定升级。

## 安装hexo-cli

``` bash
$ npm install -g hexo-cli
```

## 安装升级需要的package

``` bash
$ npm install -g npm-check
$ npm-check
```
检查系统安装的插件是否需要升级。

``` bash
$ npm install -g npm-upgrade
$ npm-upgrade
```
升级系统的所有插件。

进入Hexo初始化的文件夹，重新install。

``` bash
$ rm -rf node_modules
$ npm install --save
```

## Breaking changes
大版本升级，问题多出现在_config.xml上，搜索下解决就好。

## NexT主题的升级
直接从Github下载最新的主题，注意themes\next\_config.xml要自己修改了。
