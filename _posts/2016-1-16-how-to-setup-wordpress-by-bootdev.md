---
layout: post
title:  "如何使用bootdev的php docker脚本，快速搭建一个wordpress"
date:   2016-1-16 4:23:57
categories: wordpress bootdev
---

预置条件：
* [数据库搭建]()
* [安装docker]()
* [安装docker-compose]()

正文：
1. 将[phpfpm](phpfpm)项目clone到本地
2. 在根目录下编写`docker-compose.yml`如下

```
web:
  build: .
  ports:
    - "80:80"
  volumes:
    - ./app:/usr/local/nginx
```

3. 下载并解压wordpress文件，并命名为app目录

{% highlight shell %}
wget http://wordpress.org/latest.zip
unzip latest.zip
mv wordpress app
{% endhighlight %}

4. 修改数据库配置wp-config.php


另外想要用好wordpress，一个ftp配置会是很方便的选择。
可以参考我的另外一篇，[如何使用docker搭建简易ftp服务器]（撰写中）


[phpfpm]: https://github.com/chankongching/bootdev-nginx-phpfpm56-docker
