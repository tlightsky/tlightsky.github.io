---
layout: post
title:  "github sock5 proxy设置"
date:   2016-7-20 09:51:02
categories: video template
---

# 设置git相关
修改 /etc/ssh_config 中的这一项，去掉#
{% highlight shell %}
GSSAPIAuthentication no
{% endhighlight %}

在/etc/ssh_config 中，添加下面代码：
{% highlight shell %}
Host github github.com
     Hostname github.com
     User git
     ProxyCommand /usr/bin/proxy-wrapper '%h %p'
{% endhighlight %}

然后我们创建proxy-wrapper 程序，就一行：

{% highlight shell %}
nc -x127.0.0.1:1082 -X5 $*
{% endhighlight %}


[知乎参考](https://www.zhihu.com/question/23315073)
