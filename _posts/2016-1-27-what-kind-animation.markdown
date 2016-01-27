---
layout: post
title:  "我们需要什么样的动画"
date:   2016-1-27 09:51:02
categories: animation react
---

### 前情概要：

* 公司需要为全彩屏幕提供模板制作


### 总结下来需要的质量属性：

* 自适应
* 只改文字
* 有时序

在这里顺便分析下之前拥有的方案的属性

#### animatron

* 自适应 NO
* 改文字 OK
* 有时序 OK

#### 纯html

* 自适应 OK
* 改文字 OK
* 有时序 NO

最终的方案，初步定为animatron的动画格式的基础上，进行自适应改造。如下：

* 添加flex-box布局，使得animatron拥有自适应能力
* 添加raf控制，使得animatron的时序在服务器端可控
