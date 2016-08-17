---
title: 安装配置Hexo
tags: []
date: 2014-06-13 11:41:19
---

我又回归了！放弃了独立空间，放弃了独立域名（主要原因是没钱我会说吗，╭(╯^╰)╮

Hexo的官网：[http://zespia.tw/hexo/，](http://zespia.tw/hexo/，) 具体步骤：[http://zespia.tw/hexo/docs/](http://zespia.tw/hexo/docs/)

事实上，作者已经写的非常详细。我只想补充一些自己的经验，以及一些可能会遇到的问题。

我的 **配置文件** 内容主要如下（关键部分）：

### Site 部分：

`title: 未必博客
subtitle: Where cangzhang makes it.
description:
author: cangzhang
email: cangzan@gmail.com
language: zh-CN`

### Extensions 部分：

`theme: landscape
exclude_generator:`

*   hexo-generator-feed

### Deploy 部分：

`deploy:
  type: github
  repository: git@github.com:cangzhang/cangzhang.github.io.git
  branch: master`

### 可能遇到的问题：

`求助 fatal: &#39;furtee.github.com&#39; does not appear to be a git repository`
[https://github.com/tommy351/hexo/issues/29](https://github.com/tommy351/hexo/issues/29)

`git - Error when push commits with Github: fatal: could not read Username - Stack Overflow`
[http://stackoverflow.com/questions/20871549/error-when-push-commits-with-github-fatal-could-not-read-username](http://stackoverflow.com/questions/20871549/error-when-push-commits-with-github-fatal-could-not-read-username)

—-EOF—-