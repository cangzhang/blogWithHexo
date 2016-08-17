---
title: '[Symfony]生成 setters/getters 遇到 Too many arguments 错误解决方法'
tags:
  - symfony3
date: 2016-05-01 22:42:49
---

输入 `php bin/console doctrine:generate:entity myBundle:MyEntity` 后一直提示如下错误：

> [SymfonyComponentConsoleExceptionRuntimeException]   Too many
> arguments.

搜了一圈stackoverflow，后来试了一个命令：

     php bin/console cache:clear

问题就这样解决了0.0

//如果使用的 `Symfony2` 那么上面的 `bin/console` 应该换成  `app/console`