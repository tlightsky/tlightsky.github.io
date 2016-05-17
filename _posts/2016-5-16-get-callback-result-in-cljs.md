---
layout: post
title:  "cljs获取函数回调参数的方法"
date:   2016-5-12 09:51:02
categories: laravel controller
---

## callback argument as chan
`<<<` 这种方法是可以的
`<<obj` 是之前我自创的，试用宏的方式获得chan


## 排序，(sort-by keyfn list)

{% highlight clojurescript %}
(defonce keyfy-re #".*_(\d+)\.jpg")

(defn keyfy [s]
  (let [s (second (re-find keyfy-re s))]
    (js/parseInt s)))

{% highlight %}

PS: 昨天干了一个很蠢的事，在调研清楚功能之前先选用库进行调试。
做了一些无用功，这点需要自省，在做之前掌握所有信息。
对所有观点进行压力测试，找最聪明的人反驳自己，以接近真实。
