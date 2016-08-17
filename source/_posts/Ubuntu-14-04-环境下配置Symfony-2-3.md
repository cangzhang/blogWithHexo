---
title: Ubuntu 14.04 环境下配置Symfony 2.3
tags:
  - symfony
  - ubuntu
date: 2015-05-08 19:22:17
---

首先，我们需要安装PHP5

    $ sudo apt-get install php5
    `</pre>

    接下来

    <pre>`$ curl -LsS http://symfony.com/installer &gt; symfony.phar
    $ sudo mv symfony.phar /usr/local/bin/symfony
    $ chmod a+x /usr/local/bin/symfony
    `</pre>

    接下来，我们需要安装2.3版本的Symfony

    <pre>`$ symfony new my_project 2.3
    `</pre>

    过程可能会比较漫长。

    安装提示成功以后，根据提示，输入

    <pre>`$ php my_project/app/check.php
    `</pre>

    检查错误。

    * * *

    遇到的问题：

    1.data.timezone()

    运行

    <pre>`$ locate php.ini
    `</pre>

    查找php.ini地址，找到timezone具体行数，将前面的注释取消，输入

    <pre>`date.timezone = Asia/Chongqing
    `</pre>

    具体timezone参考[这里](http://php.net/manual/zh/timezones.asia.php)

    2.WARNING  intl extension should be available

              Install and enable the intl extension (used for validators).

    输入命令：

    <pre>`$ sudo apt-get install php5-intl
    `</pre>

    3.WARNING  PDO should have some drivers installed (currently available: none)

              Install PDO drivers (mandatory for Doctrine).

    输入命令：

    <pre>`$ sudo apt-get install php5-mysql
    