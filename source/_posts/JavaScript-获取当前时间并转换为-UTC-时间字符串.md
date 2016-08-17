---
title: '[JavaScript] 获取当前时间并转换为 UTC 时间字符串'
tags:
  - javascript
date: 2016-07-01 17:31:46
---

    var utc = new Date().toISOString().slice(0, -5);
    console.log(utc);
    //OUTPUT: 2016-07-01T09:26:52

    var utc = new Date().toISOString();
    console.log(utc);
    //OUTPUT: 2016-07-01T09:31:17.008Z