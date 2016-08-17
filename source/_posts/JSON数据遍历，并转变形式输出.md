---
title: JSON数据遍历，并转变形式输出
tags:
  - javascript
date: 2016-04-06 18:09:13
---

代码如下：

    var originParameters = {
          "5": {
              "4": 5,
              "5": "1",
              "6": "1",
              "10": "1"
          }
    };

    var arr = originParameters[5];
    console.log(arr);
    console.log("------");
    var FieldParameters = [];
    for (var i in arr){
      var  temp  =  {};
      temp.FieldParameterId = i;
      temp.value = arr[i];
      FieldParameters.push(temp);
    }
    console.log(FieldParameters);
    console.log("------");
    //console.log(JSON.stringify(FieldParameters));
    console.log("------");

    var $scope = {};
    $scope.formData = {};
    $scope.formData.AttributeParameters = FieldParameters;
    console.log($scope.formData);

输出结果如下：
![Output](/img/bVuDVy "Output")