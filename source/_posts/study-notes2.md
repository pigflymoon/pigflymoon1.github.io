---
layout: post
title: "javascript-callback 回调函数"
date:  19/07/17 7:51 PM
tags: 
	-  javascript
	-  编程
---

    

# 回调函数

```javascript
let x =function(){
  console.log('I am called from inside of x')
};

let y =function(callback){
	console.log('y function');
	callback();
};

y(x);

```
![](images/callback1.png) 
![](images/callback2.png) 
我们把x作为一个函数体（函数本身）传到y里，而不是执行x（不是把x执行的结果），然后到时候再执行它。
## 例子2
```javascript
let calc = function (num1,num2,calcType) {
    
  if(calcType == "add"){
      return num1 + num2;
  } else if(calcType === "multiply"){
      return num1 * num2;
  }
};

console.log(calc(2,3,'add'));
```

```javascript
let add = function(a,b) {
    return a + b;
  
};

let multiply = function(a,b) {
  return a * b; 
}
 
let calc = function(num1,num2,callback) {
    
    if(typeof callback === "function"){
        return callback(num1,num2);
    }
  
}

console.log(calc(2,3,add));

console.log(calc(2,3,function(a,b){
    return a - b;
}))

```
![](images/callback3.png) 


```javascript
var myArr = [{
    num: 5,
    str: 'apple',
    },{
     num: 7,
     str: 'cabbage',
    },{
     num: 1,
     str: 'ban',
    }];

myArr.sort(function(val1,val2) {
    if(val1.str > val2.str){
        return -1;
    }else{
        return 1;
    }
  
});

console.log(myArr);
```