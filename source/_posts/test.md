---
layout: post
title: "test"
date:  26/05/17 11:10 PM
tags: 
	-  test
	-  test
---
    这里写正文（上面的---是必要的）
# Table of Contents
  * [子标题 1](#chapter-1)
  * [子标题 2](#chapter-2)
  * [子标题 3](#chapter-3)
    
# 标题
# Chapter 1 <a id="chapter-1"></a>
Content for chapter one.       


`Array.from`方法用于将两类对象转为真正的数组：类似数组的对象（array-like object）和可遍历（iterable）的对象（包括ES6新增的数据结构Set和Map）。

下面是一个类似数组的对象，`Array.from`将它转为真正的数组。

```javascript
let arrayLike = {
    '0': 'a',
    '1': 'b',
    '2': 'c',
    length: 3
};

// ES5的写法
var arr1 = [].slice.call(arrayLike); // ['a', 'b', 'c']

// ES6的写法
let arr2 = Array.from(arrayLike); // ['a', 'b', 'c']
```
