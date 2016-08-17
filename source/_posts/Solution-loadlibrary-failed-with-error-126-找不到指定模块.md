---
title: '[Solution]loadlibrary failed with error 126:找不到指定模块'
tags:
  - AutoCAD错误
  - 折腾
date: 2014-02-14 20:47:46
---

今天安装AutoCAD 2014的时候遇到了这个问题。Google了一下，发现原来这个问题只出现在Win 7/Vista + ATI显卡上面。下面公布解决方法：<a id="more"></a>

## 方法一（操作简单）

把显卡改为根据电源模式调节，具体步骤:鼠标右键-&gt;显示卡属性-&gt;电源-&gt;可切换显示卡属性-&gt;手动或根据电源选择图形处理器-&gt;应用。
这样，你就可以打开了。

## 方法二（稍微复杂些，而且未必有效）

这个稍微复杂些，还未必有效，但是说不定可以解决其他软件比如PS的类似问题。

`=============分割线=============
Hi,
<span style="line-height: 1.714285714; font-size: 1rem;">in order to use openGL, copy :</span>
%WINDIR%\system32\opengl32.dll

*   to :
%WINDIR%\system32.dll
yes… “.dll” without name. Will work with the following command:
start -&gt; execute (or shortcut WindowsKey + R) : cmd [ok]
cd %WINDIR%\system32
copy opengl32.dll .dll
If UAC’s still active you may have to run command prompt as administrator.
source : [http://www.tomshardware.com/forum/284973-33-catalyst-breaks-opengl-games](http://www.tomshardware.com/forum/284973-33-catalyst-breaks-opengl-games)
I tried it successfully for Quake III &amp; Adobe Photoshop CS5.
This is relevant _only_ if you’re using an ATI videocard _and_ you’re under Vista or 7.
=======================================`