---
title: Google Chrome自由安装第三方插件
tags:
  - Google Chrome
  - 折腾
date: 2014-07-03 12:00:26
---

涵盖 Windows XP/7 、Mac OS X 、Linux 的 Chrome 第三方应用安装策略说明。

听说众多 Chrome 粉丝为 Google 禁止安装第三方应用的问题感到相当烦恼。那么我就来

简单地解救一下。

实现的方法,其实只是利用了 Chrome 为企业批量配置 Chrome 浏览器提供的策略配置功能罢了,这是 N 年前就有的功能了,只是方法麻烦了一点,大家没了解过。

Windows XP 在进行配置前得先安装群组策略管理工具(GPMC),以及该工具所须的组件:

1.  Windows 图像处理组件(WIC)  [http://www.microsoft.com/zh-cn/download/details.aspx?id=32](http://www.microsoft.com/zh-cn/download/details.aspx?id=32)

2.  Microsoft .NET Framework 1.1  [http://www.microsoft.com/zh-cn/download/details.aspx?id=26](http://www.microsoft.com/zh-cn/download/details.aspx?id=26)

3.  Group Policy Management Console (GPMC) with Service Pack 1  [http://www.microsoft.com/zh-CN/download/details.aspx?id=21895](http://www.microsoft.com/zh-CN/download/details.aspx?id=21895)

然后,我没有 Windows 7 可供测试(求支援),我只是在用 XP ,所以我有点标题党了……

先下载一个官方提供的压缩包并解压缩:[http://dl.google.com/dl/edgedl/chrome/policy/policy_templates.zip](http://dl.google.com/dl/edgedl/chrome/policy/policy_templates.zip)

按 Ctrl­R 调出运行窗口,输入 gpedit.msc并运行之:

1.  选择左侧窗口的「计算机配置」——「管理模板」,鼠标右键单击,选择「添加/删除模板」。

2.  按左下角「添加」按钮添加刚才解压出来的文件夹的 windows\adm\zh-­CN\chrome.adm文件

3.  左侧出现了「计算机配置——管理模板(——「经典管理模板(ADM)」)——Google——Google Chrome」的目录。

4.  进入子目录「扩展程序」,双击「配置扩展程序、应用和用户脚本安装源」开始修改配置。

5.  在出现的窗口中选择「已启用」,然后点击「显示」。

6.  在新出现的窗口中点击「添加」,输入 _://_/*,确定。

7.  继续按「确定」确认修改并关闭窗口,再按剩下窗口右下的「应用」。

最后打开 Chrome 的 chrome://policy 页面,击左上方的按钮重新加载策略信息便可令设置即时生效。

没有图片总是有点不太好,可以参考这篇官方文章:[https://support.google.com/installer/answer/146164?hl=en](https://support.google.com/installer/answer/146164?hl=en)

中文版(没配图):[https://support.google.com/installer/answer/146164?hl=zh-Hans](https://support.google.com/installer/answer/146164?hl=zh-Hans)

不通过 chrome://plugins 页面停用 update 插件来取消自动更新的方法也在里面。

[参考资料]Exhausitive List of All Manageable Policies [http://www.chromium.org/administrators/policy-list-3](http://www.chromium.org/administrators/policy-list-3)

Policy Template for Windows [http://www.chromium.org/administrators/policy-templates](http://www.chromium.org/administrators/policy-templates)

[http://www.chromium.org/administrators/mac-quick-start](http://www.chromium.org/administrators/mac-quick-start)

[http://www.chromium.org/administrators/linux-quick-start](http://www.chromium.org/administrators/linux-quick-start)

原文转载自 铅笔的博客
[https://drive.google.com/folderview?id=0By-rJN-esrnrWVc2ZWJhZlJ2cDA&amp;usp=sharing](https://drive.google.com/folderview?id=0By-rJN-esrnrWVc2ZWJhZlJ2cDA&amp;usp=sharing)