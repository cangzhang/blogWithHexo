---
title: Windows 下挂载EFI分区
tags:
  - windows10
date: 2016-04-28 12:10:12
---

以管理员身份运行`cmd`， 输入：

    diskpart
    list disk
    sel disk x
    list part
    sel part x //ESP分区
    ass //挂载并分配盘符

接下来管理员权限运行编辑器就可以打开分区目录进行修改了。