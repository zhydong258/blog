---
title: Quick Start for Hexo
date: 2016-12-27 16:52:54
tags: Hexo
categories: 运维
---
Welcome to [Hexo](https://hexo.io/)! This is your very first post. Check [documentation](https://hexo.io/docs/) for more info. If you get any problems when using Hexo, you can find the answer in [troubleshooting](https://hexo.io/docs/troubleshooting.html) or you can ask me on [GitHub](https://github.com/hexojs/hexo/issues).

## Quick Start

### Install 

``` bash
$ npm install hexo-cli -g
$ hexo init blog
$ cd blog
$ npm install
```

### Create a new post

``` bash
$ hexo new "My New Post"
$ hexo new page about
$ hexo new page tags
```

More info: [Writing](https://hexo.io/docs/writing.html)

### Run server

``` bash
$ hexo server
$ hexo server -p 5000
```

More info: [Server](https://hexo.io/docs/server.html)

### Generate static files

``` bash
$ hexo generate
$ hexo generate --deploy
```

More info: [Generating](https://hexo.io/docs/generating.html)

### Deploy to remote sites

``` bash
$ hexo deploy
```

More info: [Deployment](https://hexo.io/docs/deployment.html)

### Add tags and categories

```yaml
tags:
  - Testing
  - Another Tag
categories: Label
```

More info: [Tags](http://theme-next.iissnan.com/theme-settings.html)
