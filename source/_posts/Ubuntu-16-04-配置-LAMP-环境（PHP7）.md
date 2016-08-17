---
title: Ubuntu 16.04 配置 LAMP 环境（PHP7）
tags:
  - ubuntu
  - lamp
date: 2016-08-04 09:05:06
---

    sudo apt-get update
    `</pre>

    ## Step 1\. Install Apache2

    <pre>`sudo apt-get install apache2
    sudo ufw app list
    //Sample output:
    Available applications:
      Apache
      Apache Full
      Apache Secure
      OpenSSH

    sudo ufw allow in "Apache Full" 
    //Allow incoming traffic for this profile
    `</pre>

    ## Step 2\. Install MySQL

    <pre>`sudo apt-get install mysql-server
    sudo mysql_secure_installation

    `</pre>

    ## Step 3\. Install PHP

    <pre>`sudo apt-get install php7

    `</pre>

    ## Step 4\. Install PHP Modules

    <pre>`apt-cache search php- | less
    apt-cache show package_name
    sudo apt-get install php7-*

* * *

遇到的问题：

*   重新设置 Mysql user/pwd.(解决方法见链接2)

* * *

参考文章：
[How To Install Linux, Apache, MySQL, PHP (LAMP) stack on Ubuntu 16.04](https://www.digitalocean.com/community/tutorials/how-to-install-linux-apache-mysql-php-lamp-stack-on-ubuntu-16-04)
[MySQL ERROR 1698 (28000) 错误](http://www.cnblogs.com/leolztang/p/5094930.html)