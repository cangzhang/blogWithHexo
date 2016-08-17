---
title: 修改Chrome默认搜索引擎为Google.com
tags:
  - Google Chrome
  - 折腾
date: 2014-07-11 14:33:00
---

1.  关闭所有的Chrome窗口
2.  进入Chrome的用户设置文件夹，对于Windows Vista和Windows 7用户进入已经变为了 `%LOCALAPPDATA%\Google\Chrome\User Data\Default\Preferences`3.  用记事本打开`Preferences`文件
4.  找到`last_known_google_url`和 `last_prompted_google_url`这两行，修改为Google.com，或者其它你想用的Google本地化搜索域名.
5.  保存文件，重新打开Chrome，即可看到变化.
![TEST](http://segmentfault.com/img/bVcGL6)