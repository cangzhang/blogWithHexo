---
title: Apache配置本地访问地址
tags:
  - apache
date: 2016-03-27 10:31:15
---

本地要访问特定文件地址时，如果放在`xampp`的根目录里，找起来会特别麻烦。
如果将该文件夹映射到localhost里，相信就会方便很多，而且便于集中管理。

比如我的本地文件夹地址是`D:\projects\test`，在`httpd.conf`里，添加下面内容：

        #映射地址为localhost/z
        Alias /z "D:/projects"
        &lt;Directory "D:/projects"&gt;
            Options Indexes FollowSymLinks Includes ExecCGI
            #如果不想列出目录则将上面一行换成下面一行
            #Options None 
            AllowOverride All
            Require all granted
        &lt;/Directory&gt;

那么，就可以直接访问了。
![访问效果](/img/bVtRPa "访问效果")