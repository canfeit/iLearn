## 6 种原始数据类型(只读):

- Boolean
- Number
- String
- Symbol(ES6)
- null(ES 关键字,空对象,无对象特征)
- undefined(全局变量,未定义对象,无对象特征)

```js
typeof undefined; // 'undefined'
typeof null; // 'object'
(2.0).toString(); // '2'
(2).toString(); // '2',包装类型临时对象
```

## 引用类型

- 原生对象:Boolean(包装对象),Number(包装对象),String(包装对象)
  Math(内置对象),global(内置对象)
  Array,Date,Error,RegExp,Arguments,JSON,Function,Map,Set,Object
- 宿主对象:BOM,DOM
- 自定义对象
