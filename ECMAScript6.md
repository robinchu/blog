# ES6

## 块级作用域

1. 变量提升
2. 内部变量覆盖外部变量
3. 用来计数的循环变量泄露为全局变量
4. 块中的变量不影响它内部的子块的变量

`变量冻结Object.freeze({})`

```js

//深度冻结对象

// es5
var constantize = (obj) => {
	Object.freeze(obj);
	Object.keys(obj).forEach((key, value) => {
		if (typeof obj[key] === 'object') {
			constantize( obj[key]);	
		}
	})
}

// es6
'use strict';

var _typeof = typeof Symbol === "function" && typeof Symbol.iterator === "symbol" ? function (obj) { return typeof obj; } : function (obj) { return obj && typeof Symbol === "function" && obj.constructor === Symbol && obj !== Symbol.prototype ? "symbol" : typeof obj; };

var constantize = function constantize(obj) {
   Object.freeze(obj);
   Object.keys(obj).forEach(function (key, value) {
       if (_typeof(obj[key]) === 'object') {
           constantize(obj[key]);
       }
   });
};

```

## 变量的解构赋值

1. 解析赋值的惰性求值
2. 对象的解构

```js
var {foo:fo, bar:bar} = {foo:"aaa", bar:"bbb"}
```

## 解构赋值的使用

1. 交换变量的值
2. 函数返回多个值
3. 函数参数的定义
4. 提取JSON数据
5. 函数参数的默认值
6. 遍历Map结构
7. 输入模块的指定方向

j
