---
title: '[Symfony3]删除默认bundle(AppBundle)'
tags:
  - symfony3
date: 2016-05-01 19:22:10
---

1.  删除 `app\AppKernel.php`的 `registerBundles()` 相应 `appBundle` 部分.

2.  删除`app\config\routing.yml` 中 `appBundle` 相应部分.

3.  删除`src`目录下整个`appBundle`文件夹.