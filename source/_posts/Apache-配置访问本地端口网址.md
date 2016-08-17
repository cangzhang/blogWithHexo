---
title: '[Apache] 配置访问本地端口网址'
tags:
  - apache
date: 2016-05-30 18:46:02
---

在`httpd-vhosts.conf`中，新建如下内容：

    &lt;VirtualHost 127.0.0.1&gt;
           ServerName  x.y:8000
           DocumentRoot "D:\projects\xxx\web"
          &lt;Directory "D:\projects\xxx\web"&gt;
             RewriteEngine on
             AllowOverride All
          &lt;/Directory&gt;
    &lt;/VirtualHost&gt;

重启Apache即可生效。