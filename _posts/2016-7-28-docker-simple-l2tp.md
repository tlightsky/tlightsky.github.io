---
layout: post
title:  "docker simple l2tp"
date:   2016-7-28 09:51:02
categories: docker l2tp
---

## l2tp in docker


{% highlight yml %}
l2tp:
  image: siomiz/softethervpn
  ports:
   - "500:500/udp"
   - "4500:4500/udp"
   - "1701:1701/tcp"
  environment:
   - PSK=gg
   - USERS=wc:wc
  cap_add:
  - NET_ADMIN
  restart: always
{% endhighlight %}
