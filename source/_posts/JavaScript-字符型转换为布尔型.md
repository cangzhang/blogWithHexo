---
title: '[JavaScript]字符型转换为布尔型'
tags:
  - javascript
date: 2016-04-06 18:15:17
---

原格式为：

    {
        "a": "1",
        "b": "0"
    }`</pre>

    目标格式：

    <pre>`{
        "a": true,
        "b": false
    }`</pre>

    关键语句：

    <pre>`var arr = [];
    for (var i in obj){
                var  temp  =  {};
                temp.a = i;
                temp.value = !!parseInt(obj[i]);

               arr.push(temp);
            }
    return arr;