# **rules**

*代码规范*

## <a name="table-of-contents">目录</a>

  1. [要求或禁止使用分号代替 ASI (semi)](#semi)
  1. [未使用过的变量 (no-unused-vars)](#no-unused-vars)
  1. [禁用 console (no-console)](#no-console)
  1. [强制数组方法的回调函数中有 return 语句 (array-callback-return)](#array-callback-return)
  1. [要求 Switch 语句中有 Default 分支 (default-case)](#default-case)
  1. [强制在点号之前或之后换行 (dot-location)](#dot-location)
  1. [要求使用 === 和 !== (eqeqeq)](#eqeqeq)
  1. [要求调用无参构造函数时带括号 (new-parens)](#new-parens)
  1. [禁止使用 Array 构造函数 (no-array-constructor)](#no-array-constructor)
  1. [禁用 caller 或 callee (no-caller)](#no-caller)
  1. [禁止在条件语句中出现赋值操作符（no-cond-assign）](#no-cond-assign)
  1. [不允许改变用const声明的变量 (no-const-assign)](#no-const-assign)
  1. [禁止在正则表达式中使用控制字符（no-control-regex）](#no-control-regex)
  1. [禁止删除变量 (no-delete-var)](#no-delete-var)
  1. [禁止在 function 定义中出现重复的参数 (no-dupe-args)](#no-dupe-args)
  1. [不允许类成员中有重复的名称 (no-dupe-class-members)](#no-dupe-class-members)
  1. [no-dupe-keys](#no-dupe-keys)
  1. [no-duplicate-case](#no-duplicate-case)
  1. [no-empty-character-class](#no-empty-character-class)
  1. [no-empty-pattern](#no-empty-pattern)
  1. [no-eval](#no-eval)
  1. [no-ex-assign](#no-ex-assign)
  1. [no-extend-native](#no-extend-native)
  1. [no-extra-bind](#no-extra-bind)
  1. [no-extra-label](#no-extra-label)
  1. [no-fallthrough](#no-fallthrough)
  1. [no-func-assign](#no-func-assign)
  1. [no-implied-eval](#no-implied-eval)
  1. [no-invalid-regexp](#no-invalid-regexp)
  1. [no-iterator](#no-iterator)
  1. [no-label-var](#no-label-var)
  1. [no-labels](#no-labels)
  1. [no-lone-blocks](#no-lone-blocks)
  1. [no-loop-func](#no-loop-func)
  1. [no-mixed-operators](#no-mixed-operators)
  1. [no-multi-str](#no-multi-str)
  1. [no-native-reassign](#no-native-reassign)
  1. [no-negated-in-lhs](#no-negated-in-lhs)
  
# 代码规范常见问题

## <a name="semi">要求或禁止使用分号代替 ASI (semi)</a>

命令行中的 --fix 选项可以自动修复一些该规则报告的问题。
```python
semi: ['error', 'always']
```


  - **等级 : "error"**
  - **选项 "always"**: (默认) 要求在语句末尾使用分号

##### 默认选项 "always" 的 <font color=#f00>错误</font> 代码示例：

```python
/*eslint semi: ["error", "always"]*/

var name = "ESLint"

object.method = function() {
    // ...
}
```
##### 默认选项 "always" 的 正确 代码示例：

```python
/*eslint semi: "error"*/

var name = "ESLint";

object.method = function() {
    // ...
};
```
**[⬆ 回到顶部](#table-of-contents)**
   
## <a name="no-unused-vars">禁止未使用过的变量 (no-unused-vars)</a>
```python
'no-unused-vars': [
  'warn',
  {
    args: 'none',
    ignoreRestSiblings: true,
  },
]
```
  - **等级 : "warn"**
  - **选项 "args"**: none - 不检查参数
  - **选项 "ignoreRestSiblings"**: 选项是个布尔类型 (默认: false)。使用 Rest 属性 可能会“省略”对象中的属性，但是默认情况下，其兄弟属性被标记为 “unused”。使用该选项可以使 rest 属性的兄弟属性被忽略。
  
##### 选项 { "args": "none" } 的 正确 代码示例：

```python
/*eslint no-unused-vars: ["error", { "args": "none" }]*/
    
(function(foo, bar, baz) {
    return bar;
})();
```
##### 选项 { "ignoreRestSiblings": true } 的 正确 代码示例：

```python
/*eslint no-unused-vars: ["error", { "ignoreRestSiblings": true }]*/
// 'type' is ignored because it has a rest property sibling.
var { type, ...coords } = data;
```
**[⬆ 回到顶部](#table-of-contents)**

## <a name="no-console">禁用 console (no-console)</a>
```python
'no-console': 'off'
```
- **选项 "off"**: 关闭禁用

**[⬆ 回到顶部](#table-of-contents)**

## <a name="array-callback-return">强制数组方法的回调函数中有 return 语句 (array-callback-return)</a>
```python
'array-callback-return': 'off'
```
- **选项 "off"**: 关闭禁用

**[⬆ 回到顶部](#table-of-contents)**

 ## <a name="default-case">要求 Switch 语句中有 Default 分支 (default-case)</a>
 ```python
 'default-case': ['warn', { commentPattern: '^no default$' }]
 ```
 - **等级 : "warn"**
 - **选项 "commentPattern "**: 设置 commentPattern 为一个正则表达式字符串，来改变默认的 /^no default$/i 注释匹配模式
 
 此规则的目的是在 switch 语句中强制声明 default 分支。或者也可以在最后一个 case 分支下，使用 // no default 来表明此处不需要 default 分支。注释可以任何形式出现，比如 // No Default。
 
##### 错误 代码示例：

```python
/*eslint default-case: "error"*/
 
switch (a) {
case 1:
     /* code */
     break;
}
```
##### 正确 代码示例：

```python
/*eslint default-case: "error"*/
         
switch (a) {
 case 1:
     /* code */
     break;

 default:
     /* code */
     break;
}


switch (a) {
 case 1:
     /* code */
     break;

 // no default
}

switch (a) {
 case 1:
     /* code */
     break;

 // No Default
}
```
**[⬆ 回到顶部](#table-of-contents)**
   
## <a name="dot-location">强制在点号之前或之后换行 (dot-location)</a>
   
命令行中的 --fix 选项可以自动修复一些该规则报告的问题。
 ```python
'dot-location': ['warn', 'property']
 ```

- **等级 : "warn"**
- **选项 "property"**: 表达式中的点号操作符应该和属性在同一行。
   
##### 选项 "property" 的 错误 代码示例：

```python
/*eslint dot-location: ["error", "property"]*/

var foo = object.
property;
```
##### 选项 "property" 的 正确 代码示例：

```python
/*eslint dot-location: ["error", "property"]*/
       
var foo = object
.property;
var bar = object.property;
```   
   
**[⬆ 回到顶部](#table-of-contents)**

## <a name="eqeqeq">要求使用 === 和 !== (eqeqeq)</a>
   
命令行中的 --fix 选项可以自动修复一些该规则报告的问题。
 ```python
eqeqeq: ['warn', 'allow-null']
 ```

- **等级 : "warn"**
- **选项 "allow-null"**: 使用 “always”，然后传一个 “null” 选项，属性值为 “ignore” 代替。这将告诉 eslint 除了与 null 字面量进行比较时，总是强制使用绝对相等。
   
**[⬆ 回到顶部](#table-of-contents)**

## <a name="new-parens">要求调用无参构造函数时带括号 (new-parens)</a>

命令行中的 --fix 选项可以自动修复一些该规则报告的问题。
```python
'new-parens': 'warn'
```


- **等级 : "warn"**

##### 错误 代码示例：

```python
/*eslint new-parens: "error"*/

var person = new Person;
var person = new (Person);
```
##### 正确 代码示例：

```python
/*eslint new-parens: "error"*/

var person = new Person();
var person = new (Person)();
```
**[⬆ 回到顶部](#table-of-contents)**

## <a name="no-array-constructor">禁止使用 Array 构造函数 (no-array-constructor)</a>

```python
'no-array-constructor': 'warn'
```

- **等级 : "warn"**

##### 错误 代码示例：

```python
/*eslint no-array-constructor: "error"*/

Array(0, 1, 2)
/*eslint no-array-constructor: "error"*/

new Array(0, 1, 2)
```
##### 正确 代码示例：

```python
/*eslint no-array-constructor: "error"*/

Array(500)
/*eslint no-array-constructor: "error"*/

new Array(someOtherArray.length)
```
**[⬆ 回到顶部](#table-of-contents)**

## <a name="no-caller">禁用 caller 或 callee (no-caller)</a>

```python
'no-caller': 'warn'
```

- **等级 : "warn"**

##### 错误 代码示例：

```python
/*eslint no-caller: "error"*/

function foo(n) {
    if (n <= 0) {
        return;
    }

    arguments.callee(n - 1);
}

[1,2,3,4,5].map(function(n) {
    return !(n > 1) ? 1 : arguments.callee(n - 1) * n;
});
```
##### 正确 代码示例：

```python
/*eslint no-caller: "error"*/

function foo(n) {
    if (n <= 0) {
        return;
    }

    foo(n - 1);
}

[1,2,3,4,5].map(function factorial(n) {
    return !(n > 1) ? 1 : factorial(n - 1) * n;
});
```
**[⬆ 回到顶部](#table-of-contents)**

## <a name="no-cond-assign">禁止在条件语句中出现赋值操作符（no-cond-assign）</a>

```python
'no-cond-assign': ['warn', 'always']
```

- **等级 : "warn"**
- **选项 "always"**: 禁止条件语句中出现赋值语句。
##### 选项 "always" 的 错误 代码示例：

```python
/*eslint no-cond-assign: ["error", "always"]*/

// Unintentional assignment
var x;
if (x = 0) {
    var b = 1;
}

// Practical example that is similar to an error
function setHeight(someNode) {
    "use strict";
    do {
        someNode.height = "100px";
    } while (someNode = someNode.parentNode);
}

// Practical example that wraps the assignment in parentheses
function setHeight(someNode) {
    "use strict";
    do {
        someNode.height = "100px";
    } while ((someNode = someNode.parentNode));
}

// Practical example that wraps the assignment and tests for 'null'
function setHeight(someNode) {
    "use strict";
    do {
        someNode.height = "100px";
    } while ((someNode = someNode.parentNode) !== null);
}
```
##### 选项 "always" 的 正确 代码示例：

```python
/*eslint no-cond-assign: ["error", "always"]*/

// Assignment replaced by comparison
var x;
if (x === 0) {
    var b = 1;
}
```
**[⬆ 回到顶部](#table-of-contents)**

## <a name="no-const-assign">不允许改变用const声明的变量 (no-const-assign)</a>

```python
'no-const-assign': 'warn'
```

- **等级 : "warn"**

##### 错误 代码示例：

```python
/*eslint no-const-assign: "error"*/
/*eslint-env es6*/

const a = 0;
a = 1;
/*eslint no-const-assign: "error"*/
/*eslint-env es6*/

const a = 0;
a += 1;
/*eslint no-const-assign: "error"*/
/*eslint-env es6*/

const a = 0;
++a;
```
##### 正确 代码示例：

```python
/*eslint no-const-assign: "error"*/
/*eslint-env es6*/

const a = 0;
console.log(a);
/*eslint no-const-assign: "error"*/
/*eslint-env es6*/

for (const a in [1, 2, 3]) { // `a` is re-defined (not modified) on each loop step.
    console.log(a);
}
/*eslint no-const-assign: "error"*/
/*eslint-env es6*/

for (const a of [1, 2, 3]) { // `a` is re-defined (not modified) on each loop step.
    console.log(a);
}
```
**[⬆ 回到顶部](#table-of-contents)**

## <a name="no-control-regex">禁止在正则表达式中使用控制字符（no-control-regex）</a>

```python
'no-control-regex': 'warn'
```

- **等级 : "warn"**

##### 错误 代码示例：

```python
/*eslint no-control-regex: "error"*/

var pattern1 = /\x1f/;
var pattern2 = new RegExp("\x1f");
```
##### 正确 代码示例：

```python
/*eslint no-control-regex: "error"*/

var pattern1 = /\x20/;
var pattern2 = new RegExp("\x20");
```
**[⬆ 回到顶部](#table-of-contents)**

## <a name="no-delete-var">禁止删除变量 (no-delete-var)</a>

```python
'no-delete-var': 'warn'
```

- **等级 : "warn"**

##### 错误 代码示例：

```python
/*eslint no-delete-var: "error"*/

var x;
delete x;
```

**[⬆ 回到顶部](#table-of-contents)**

## <a name="no-dupe-args">禁止在 function 定义中出现重复的参数 (no-dupe-args)</a>

```python
'no-dupe-args': 'warn'
```

- **等级 : "warn"**

##### 错误 代码示例：

```python
/*eslint no-dupe-args: "error"*/

function foo(a, b, a) {
    console.log("value of the second a:", a);
}

var bar = function (a, b, a) {
    console.log("value of the second a:", a);
};
```
##### 正确 代码示例：

```python
/*eslint no-dupe-args: "error"*/

function foo(a, b, c) {
    console.log(a, b, c);
}

var bar = function (a, b, c) {
    console.log(a, b, c);
};
```
**[⬆ 回到顶部](#table-of-contents)**

## <a name="no-dupe-class-members">不允许类成员中有重复的名称 (no-dupe-class-members)</a>

```python
'no-dupe-class-members': 'warn'
```

- **等级 : "warn"**

##### 错误 代码示例：

```python
/*eslint no-dupe-class-members: "error"*/
/*eslint-env es6*/

class Foo {
  bar() { }
  bar() { }
}

class Foo {
  bar() { }
  get bar() { }
}

class Foo {
  static bar() { }
  static bar() { }
}
```
##### 正确 代码示例：

```python
/*eslint no-dupe-class-members: "error"*/
/*eslint-env es6*/

class Foo {
  bar() { }
  qux() { }
}

class Foo {
  get bar() { }
  set bar(value) { }
}

class Foo {
  static bar() { }
  bar() { }
}
```
**[⬆ 回到顶部](#table-of-contents)**
