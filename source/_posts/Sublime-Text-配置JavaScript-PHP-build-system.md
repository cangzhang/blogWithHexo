---
title: '[Sublime Text] 配置JavaScript, PHP build system'
tags:
  - sublime-text
date: 2016-08-17 12:18:08
---

首先配置 node 和 PHP 环境；
选择 Tools -&gt; Build System -&gt; New Build System 之后，

*   创建 JavaScript.sublime-build 文件：

    {
        "cmd": ["node", "$file"],
        "file_regex": "^[ ]*File \"(...*?)\", line ([0-9]*)",
        "working_dir": "${file_path}",
        "selector": "source.js",
        "shell": true,
        "encoding": "utf-8",
        "windows": {
            "cmd": ["node", "$file"]
        },
        "linux": {
            "cmd": ["killall node; node", "$file"]
        }
    }
    `</pre>

*   创建 PHP.sublime-build 文件：
    <pre>`{
        "cmd": ["php", "$file"],
        "file_regex": "php$",
        "selector": "source.php"
    }