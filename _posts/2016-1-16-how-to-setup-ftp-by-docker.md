---
layout: post
title:  "如何使用docker搭建简易ftp服务器"
date:   2016-1-16 5:23:57
categories: ftp docker pure-ftp
---

本篇讲述如何使用docker快速搭建ftp服务器。

前置条件：
* [安装docker]()
* [安装docker-compose]()

使用[stilliard/pure-ftpd](stilliard/pure-ftpd)，这个ftp docker image。
步骤如下：

1. 新建ftp/docker-compose.yml文件，内容如下：
```
web:
  build: .
  ports:
    - "80:80"
  volumes:
    - ./app:/usr/local/nginx
ftp:
  image: stilliard/pure-ftpd
  volumes:
    - "./app:/home/ftpusers/code"
    - "./pure-ftpd:/etc/pure-ftpd"
  ports:
    - "21:21"
    - "30000:30000"
    - "30001:30001"
    - "30002:30002"
    - "30003:30003"
    - "30004:30004"
    - "30005:30005"
    - "30006:30006"
    - "30007:30007"
    - "30008:30008"
    - "30009:30009"
  environment:
    PUBLICHOST: localhost
```

2. 在ftp目录中，运行`docker-compose up -d`
3. 运行命令`docker exec -it ftp_ftp_1 bash`
4. 建立用户：
{% highlight bash %}
pure-pw useradd code -u ftpuser -d /home/ftpusers/code
pure-pw mkdb
{% endhighlight %}

[stilliard/pure-ftpd]: https://hub.docker.com/r/stilliard/pure-ftpd/
