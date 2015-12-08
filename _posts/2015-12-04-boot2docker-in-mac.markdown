---
layout: post
title:  "boot2docker在Mac中跑web可能遇到的问题"
date:   2015-12-04
categories: docker boot2docker mac
---
在Mac中使用docker，需要boot2docker这个工具。
它其实是借助virtualbox跑了一个linux虚拟机。
所以在使用上会与linux上的docker有些不同。
最近遇到的一个大坑就是：
{% highlight javascript %}
  如果你在boot2docker中，使用port选项指定了一个端口。
  其实不是指映射到你本地Mac的端口，而是映射到virtualbox的端口。  
{% endhighlight %}

比如docker-compose里，`port: "80:80"`
那么此时，需通过boot2docker ip这个命令，得到虚拟机的ip地址。
再打开就可以了。
