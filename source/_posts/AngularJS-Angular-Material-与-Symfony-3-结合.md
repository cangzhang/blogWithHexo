---
title: 'AngularJS, Angular Material 与 Symfony 3 结合'
tags:
  - angularjs
  - angular-material
  - symfony
date: 2016-05-18 16:00:10
---

首先需要在父级模版中引入 `AngularJS` 和 `Angular Material`.

    &lt;link rel="stylesheet" href="{{ asset('angular-material.css') }}"&gt;
    &lt;link rel="stylesheet" href="https://fonts.googleapis.com/css?family=RobotoDraft:300,400,500,700,400italic"&gt;

    &lt;script src="{{ asset('angular.js') }}"&gt;&lt;/script&gt;
    &lt;script src="{{ asset('angular-aria.js') }}"&gt;&lt;/script&gt;
    &lt;script src="{{ asset('angular-animate.js') }}"&gt;&lt;/script&gt;
    &lt;script src="{{ asset('angular-material.js') }}"&gt;&lt;/script&gt;
    `</pre>

    在js文件中,写入:

    <pre>`angular.module('myApp',['ngMaterial'])
        .config(function($interpolateProvider){
            $interpolateProvider.startSymbol('{[{').endSymbol('}]}');
    })
        .controller('myController', myController);

    myController.$inject = ['$scope'];

    function myController( $scope ) {

    }`</pre>

    最后,在twig模版中写scope变量时,需要写成:

    <pre>`{[{ scopeVariable }]}

* * *

参考内容:

*   [http://stackoverflow.com/questions/13671701/angularjs-twig-conflict-with-double-curly-braces](http://stackoverflow.com/questions/13671701/angularjs-twig-conflict-with-double-curly-braces)