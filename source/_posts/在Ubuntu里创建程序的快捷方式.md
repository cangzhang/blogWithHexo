---
title: 在Ubuntu里创建程序的快捷方式
tags:
  - Ubuntu建立程序快捷方式
  - 折腾
date: 2014-02-14 20:47:46
---

下面我以Pycharm（Python的一个相当不错的IDE）来作为演示：
首先：

<pre lang="shell">sudo gedit /usr/share/applications/pycharm.desktop</pre>
下面的是我的desktop文件的内容：

`[Desktop Entry]
Comment=Python IDE //程序说明
Name=Pycharm //程序名称
Exec=/opt/pycharm/bin/pycharm.sh //指定执行文件位置
Encoding=UTF-8
Terminal=false
Type=Application
Categories=Application;
Icon=/usr/share/applications/pycharm.png //这里定义图标路径`

如果你想像我一样省事，直接  `sudo cp pycharm.desktop /home/__username__/Desktop/pycharm.desktop`