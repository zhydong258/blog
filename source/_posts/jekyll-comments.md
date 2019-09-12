---
title: Jekyll Comments
date: 2016-12-11 16:52:54
tags: 
  - jekyll comments
  - comments
categories: 运维
---
## Jekyll添加评论系统

搭建在github上的blog，需要一个comments的系统。话说，用的可能性不大，不过看别人有，所以自己也就添加了一个。

## duoshuo

评论是用的多说，国产的还是比较适合国内的环境，在[多说](https://duoshuo.com)上注册一个账号。填上你的网站名称和地址，
填上一个short-name，最后会给出参考的代码，通用代码就行。

## 配置jekyll

jekyll默认的comments是 disqus系统，打开_config.yml文件，修改comments的provider为duoshuo，修改short-name。

## 需改JB的提供的duoshuo代码

打开_include/JB/comments-providers/duoshuo，把多说网站提供的通用代码粘贴进来，覆盖掉原来的代码。

~~~js
<!-- 多说评论框 start -->
	<div class="ds-thread" data-thread-key="{{ page.id }}" data-title="{{ page.title }}" data-url="{{ site.url}}{{ page.url }}"></div>
<!-- 多说评论框 end -->
<!-- 多说公共JS代码 start (一个网页只需插入一次) -->
<script type="text/javascript">
var duoshuoQuery = {short_name:'{{ site.JB.comments.duoshuo.short_name }}'};
	(function() {
		var ds = document.createElement('script');
		ds.type = 'text/javascript';ds.async = true;
		ds.src = (document.location.protocol == 'https:' ? 'https:' : 'http:') + '//static.duoshuo.com/embed.js';
		ds.charset = 'UTF-8';
		(document.getElementsByTagName('head')[0] 
		 || document.getElementsByTagName('body')[0]).appendChild(ds);
	})();
	</script>
<!-- 多说公共JS代码 end -->
~~~
