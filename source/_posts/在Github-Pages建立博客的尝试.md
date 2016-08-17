---
title: 在Github Pages建立博客的尝试
tags:
  - Github Pages建立博客
  - 折腾
date: 2014-02-14 20:47:46
---

前面的基本部分就不说了。使用Ruby的话建议安装[RailsInstaller](http://railsinstaller.org)，能够省掉很多麻烦。
将淘宝Ruby源加入到列表里：

<pre>gem sources —remove [https://rubygems.org/](https://rubygems.org/)
gem sources -a [http://ruby.taobao.org/](http://ruby.taobao.org/)</pre>
查看源列表：

`gem sources -l`

这样一来，速度就会快很多。

使用JekyII搭建博客推荐教程：[Github Pages极简教程](http://yanping.me/cn/blog/2012/03/18/github-pages-step-by-step/)

使用Octopress搭建博客推荐教程：windows下的[教程1](http://sinosmond.github.com/blog/2012/03/12/install-and-deploy-octopress-to-github-on-windows7-from-scratch/)、[教程2](http://tonytonyjan.heroku.com/2012/03/01/install-octopress-on-windows/)，[ubuntu下的教程](http://www.yangzhiping.com/tech/octopress.html)

按照 [教程1](http://sinosmond.github.com/blog/2012/03/12/install-and-deploy-octopress-to-github-on-windows7-from-scratch/) 基本已经解决问题了。但是遇到了这个错误：

`gh-pages -&amp;gt; gh-pages (non-fast forward)`

<span style="color: #99cc00;">解决方法：</span>

`git push origin :gh-pages
git push origin gh-pages`