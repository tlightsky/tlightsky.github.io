---
layout: post
title:  "ustc debian source"
date:   2016-7-22 09:51:02
categories: ustc debian source
---

#github 代理

修改 /etc/ssh_config

{% highlight yml %}
Host github github.com
     Hostname github.com
     User git
     ProxyCommand /usr/local/bin/proxy-wrapper '%h %p'
{% endhighlight %}

修改文件/usr/local/bin/proxy-wrapper：

{% highlight yml %}
nc -x127.0.0.1:1082 -X5 $*
{% endhighlight %}
