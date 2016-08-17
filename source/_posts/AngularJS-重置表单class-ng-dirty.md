---
title: '[AngularJS] 重置表单class ng-dirty'
tags:
  - angularjs
date: 2016-06-02 13:39:09
---

在表单提交之后，如果仅仅是清空表单数据内容，相应 `input` 的 `class` 并不会改变（依然是 `ng-dirty` 状态），我们需要移除这些红色的 `required` 提示。

        &lt;div ng-app="myApp" ng-controller="myCtrl as ctrl"&gt;
          &lt;form name="ctrl.myForm"&gt;
            &lt;div&gt;&lt;label for="email"&gt;Email&lt;/label&gt;
            &lt;input name="myInput" type="email" ng-model="ctrl.email" id="email" required&gt;&lt;/div&gt;
            &lt;div&gt;&lt;label for="password"&gt;Password&lt;/label&gt;
            &lt;input name="myPassword" type="password" minlength="8" ng-model="ctrl.password" id="password" required&gt;&lt;/div&gt;
            &lt;div&gt;
            &lt;button ng-click="ctrl.reset()" type="button"&gt;Reset&lt;/button&gt;
            &lt;/div&gt;
          &lt;/form&gt;
    `</pre>

    `JavaScript` 代码：

    <pre>`
    angular.module('myApp', [])
        .controller('myCtrl', myCtrl);

    function myCtrl(){
        var vm = this;
        vm.reset = function(){
            vm.myForm.$setPristine();
            vm.myForm.$setUntouched();
            vm.email = vm.password = '';
      }
    }

_表单input区域必须放在 `form` 中_

参考连接：[Angular clear subform data and reset validation](http://stackoverflow.com/questions/18648427/angular-clear-subform-data-and-reset-validation%20%5BAngular%20clear%20subform%20data%20and%20reset%20validation%5D)