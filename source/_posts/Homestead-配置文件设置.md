---
title: Homestead 配置文件设置
tags:
  - homestead
date: 2016-04-02 10:26:16
---

内容如下，主要是共享目录的挂载：

    ---
    ip: "192.168.10.10"
    memory: 2048
    cpus: 1
    provider: virtualbox

    authorize: ~/.ssh/id_rsa.pub

    keys:
        - ~/.ssh/id_rsa

    folders:
        - map: D:/projects/stuTrac
          to: /home/vagrant/Code

        - map: D:/projects
          to: /home/projects

    sites:
        - map: homestead.app
          to: /home/vagrant/Code/public

    databases:
        - homestead