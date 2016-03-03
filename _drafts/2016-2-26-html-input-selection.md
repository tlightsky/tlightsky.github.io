---
layout: post
title:  "html输入框问题"
date:   2016-2-24 09:51:02
categories: html input selection
---

最近有一个需求，
是点击后选中所点击的input框

那么这里需要的是对于input框的选中处理

根据stackoverflow提供的方法，现在的做法是：
input.click的回调里调用e.target.select()

这样的做法，在pc，android是有效的。
但是在iPhone上只能让光标移到最后。
不过暂时可以满足公众号的需求。

ps：遇到一个很蛋疼的问题，微信官方的调试助手会在android报错，导致无法运行app。
