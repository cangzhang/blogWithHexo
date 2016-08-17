---
title: '[AngularJS] ngMesages'
tags:
  - angularjs
  - ngmessages
date: 2016-04-12 22:56:49
---

关于 `ngMessages` 官方文档地址 [在这里](https://docs.angularjs.org/api/ngMessages/directive/ngMessages)，可是却非常不详细，只列出了三种情况`required`、`minlength`、`maxlength`.
如果在 `element` 里写了自己定义的规则 `ng-pattern`，需要给出当正则生效时给出的 `ngMessage`，就需要这样写：

    &lt;form name="myForm"&gt;
      &lt;label&gt;
        &lt;input name="myField"
                type="text"
                ng-model="myName"
                ng-pattern="/{expression}/"
                /&gt;
        &lt;/label&gt;
      &lt;div ng-messages="myForm.myField.$error"&gt;
        &lt;div ng-message="minlength"&gt;...&lt;/div&gt;
        &lt;div ng-message="pattern"&gt;...&lt;/div&gt;
      &lt;/div&gt;
    &lt;/form&gt;`</pre>

    一种调试的方法：

    <pre>`&lt;pre&gt;{{myForm.myField.$error}}&lt;/pre&gt;
    //错误内容形式：{ "pattern": true }

这样的话直观地看到错误内容，相应的指定错误消息了

参考内容：
[Easy Form Validation in AngularJS with ngMessages](http://www.sitepoint.com/easy-form-validation-angularjs-ngmessages/)
[ngMessages revisited](http://blog.thoughtram.io/2015/06/06/ng-messages-revisited.html)