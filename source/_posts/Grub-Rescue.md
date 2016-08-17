---
title: Grub Rescue
tags:
  - ubuntu
  - grub2
date: 2016-04-28 12:49:52
---

grub rescue&gt;

    ls

    ls (hd0,x)/boot/grub

    set root=(hd0,x)

    set prefix=(hd0,x)/boot/grub

    insmod normal

    normal

    sudo update-grub

    sudo apt-get install grub-efi