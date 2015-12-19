---
layout: post
title:  "Immutable Redux Bootstrap"
date:   2015-12-16 11:23:57
categories: redux immutable react router
---
最近打算基于[WeUI][WeUI]做公众号的改版，这个是微信官方UI Team出的库。应该还是比较靠谱的。

仔细研究了下，发现居然已经有了[React的版本][ReactWeUI]，只是可能适配尚未完全。
不过官方[接受PR][PR]，还有会有持续改善。并且自己也可以在其中贡献些力量。

这次使用React，希望继续基于之前的redux+immutable来做，所以打算整理一个基础的Bootstrap方便以后类似项目启动

这次的Project打算使用的技术大概有以下几个：

- ### 主要依赖库
  - react
  - redux
  - react-router
  - [redux-router][redux-router]

- ### 打包等开发工具
  - webpack
  - [babel][babel]
  - eslint
  - less
  - mocha
  - uglify-loader

[项目链接][项目链接](整理中)


[WeUI]:         https://github.com/weui/weui
[ReactWeUI]:    https://github.com/weui/react-weui
[PR]:           https://github.com/weui/react-weui/issues/3
[babel]:        https://github.com/babel/babel/blob/master/doc/design/monorepo.md
[redux-router]: https://www.npmjs.com/package/redux-router
[项目链接]:       https://github.com/tlightsky/immutable-redux-bootstrap
