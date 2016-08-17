---
title: 'E: Sub-process /usr/bin/dpkg returned an error code (1)的解决方法'
tags:
  - Ubuntu Sub-process 错误
  - 折腾
date: 2014-02-14 20:47:46
---

具体见[此处](http://askubuntu.com/questions/195950/package-system-broken-e-sub-process-usr-bin-dpkg-returned-an-error-code-1)，此问题见于Ubuntu

<pre lang="shell">sudo dpkg --configure -a
sudo apt-get install -f
sudo gedit /var/lib/dpkg/status</pre>
找到当前正在安装的软件包名称，将其移除后保存，然后执行：
<pre lang="shell">sudo apt-get clean
sudo apt-get autoremove
sudo apt-get update
sudo apt-get upgrade
sudo apt-get -f install</pre>