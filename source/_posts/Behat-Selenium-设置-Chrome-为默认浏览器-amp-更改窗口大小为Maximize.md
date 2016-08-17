---
title: '[Behat] Selenium 设置 Chrome 为默认浏览器 &amp; 更改窗口大小为Maximize'
tags:
  - selenium
date: 2016-06-07 15:59:42
---

默认浏览器设置为Chrome:

*   打开`behat.yml`文件，找到`browser_name`，修改为
`browser_name: chrome`

*   下载chromedriver，并将它与selenium放在同一个文件夹下。

*   启动时首先运行selenium文件

修改默认窗口为Maximize：

    $this-&gt;getSession()-&gt;getDriver()-&gt;maximizeWindow('current');
    