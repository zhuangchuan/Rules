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
  1. [禁止在对象字面量中出现重复的键 (no-dupe-keys)](#no-dupe-keys)
  1. [禁止重复 case 标签（no-duplicate-case）](#no-duplicate-case)
  1. [禁止在正则表达式中出现空字符集 (no-empty-character-class)](#no-empty-character-class)
  1. [禁止使用空解构模式 (no-empty-pattern)](#no-empty-pattern)
  1. [禁用 eval()（no-eval）](#no-eval)
  1. [禁止对 catch 子句中的异常重新赋值 (no-ex-assign)](#no-ex-assign)
  1. [禁止扩展原生对象 (no-extend-native)](#no-extend-native)
  1. [禁止不必要的函数绑定 (no-extra-bind)](#no-extra-bind)
  1. [禁用不必要的标签 (no-extra-label)](#no-extra-label)
  1. [禁止 case 语句落空 (no-fallthrough)](#no-fallthrough)
  1. [禁止对 function 声明重新赋值 (no-func-assign)](#no-func-assign)
  1. [禁用隐式的eval() (no-implied-eval)](#no-implied-eval)
  1. [禁止在 RegExp 构造函数中出现无效的正则表达式 (no-invalid-regexp)](#no-invalid-regexp)
  1. [禁用迭代器 (no-iterator)](#no-iterator)
  1. [禁用与变量同名的标签 (no-label-var)](#no-label-var)
  1. [禁用标签语句 (no-labels)](#no-labels)
  1. [禁用不必要的嵌套块 (no-lone-blocks)](#no-lone-blocks)
  1. [禁止循环中存在函数 (no-loop-func)](#no-loop-func)
  1. [禁止混合使用不同的操作符 (no-mixed-operators)](#no-mixed-operators)
  1. [禁止多行字符串 (no-multi-str)](#no-multi-str)
  1. [禁止重新分配本地对象（no-native-resssign）](#no-native-reassign)
  1. [不允许在in表达式中否定左操作数（no-negated-in-lhs）](#no-negated-in-lhs)
  
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

## <a name="no-dupe-keys">禁止在对象字面量中出现重复的键 (no-dupe-keys)</a>

```python
'no-dupe-keys': 'warn'
```

- **等级 : "warn"**

##### 错误 代码示例：

```python
/*eslint no-dupe-keys: "error"*/

var foo = {
    bar: "baz",
    bar: "qux"
};

var foo = {
    "bar": "baz",
    bar: "qux"
};

var foo = {
    0x1: "baz",
    1: "qux"
};
```
##### 正确 代码示例：

```python
/*eslint no-dupe-keys: "error"*/

var foo = {
    bar: "baz",
    quxx: "qux"
};
```
**[⬆ 回到顶部](#table-of-contents)**

## <a name="no-duplicate-case">禁止重复 case 标签（no-duplicate-case）</a>

```python
'no-duplicate-case': 'warn'
```

- **等级 : "warn"**

##### 错误 代码示例：

```python
/*eslint no-duplicate-case: "error"*/

var a = 1,
    one = 1;

switch (a) {
    case 1:
        break;
    case 2:
        break;
    case 1:         // duplicate test expression
        break;
    default:
        break;
}

switch (a) {
    case one:
        break;
    case 2:
        break;
    case one:         // duplicate test expression
        break;
    default:
        break;
}

switch (a) {
    case "1":
        break;
    case "2":
        break;
    case "1":         // duplicate test expression
        break;
    default:
        break;
}
```
##### 正确 代码示例：

```python
/*eslint no-duplicate-case: "error"*/

var a = 1,
    one = 1;

switch (a) {
    case 1:
        break;
    case 2:
        break;
    case 3:
        break;
    default:
        break;
}

switch (a) {
    case one:
        break;
    case 2:
        break;
    case 3:
        break;
    default:
        break;
}

switch (a) {
    case "1":
        break;
    case "2":
        break;
    case "3":
        break;
    default:
        break;
}
```
**[⬆ 回到顶部](#table-of-contents)**

## <a name="no-empty-character-class">禁止在正则表达式中出现空字符集 (no-empty-character-class)</a>

```python
'no-empty-character-class': 'warn'
```

- **等级 : "warn"**

##### 错误 代码示例：

```python
/*eslint no-empty-character-class: "error"*/

/^abc[]/.test("abcdefg"); // false
"abcdefg".match(/^abc[]/); // null
```
##### 正确 代码示例：

```python
/*eslint no-empty-character-class: "error"*/

/^abc/.test("abcdefg"); // true
"abcdefg".match(/^abc/); // ["abc"]

/^abc[a-z]/.test("abcdefg"); // true
"abcdefg".match(/^abc[a-z]/); // ["abcd"]
```
**[⬆ 回到顶部](#table-of-contents)**

## <a name="no-empty-pattern">禁止使用空解构模式 (no-empty-pattern)</a>

```python
'no-empty-pattern': 'warn'
```

- **等级 : "warn"**

##### 错误 代码示例：

```python
/*eslint no-empty-pattern: "error"*/

var {} = foo;
var [] = foo;
var {a: {}} = foo;
var {a: []} = foo;
function foo({}) {}
function foo([]) {}
function foo({a: {}}) {}
function foo({a: []}) {}
```
##### 正确 代码示例：

```python
/*eslint no-empty-pattern: "error"*/

var {a = {}} = foo;
var {a = []} = foo;
function foo({a = {}}) {}
function foo({a = []}) {}
```
**[⬆ 回到顶部](#table-of-contents)**

## <a name="no-eval">禁用 eval()（no-eval）</a>

```python
'no-eval': 'warn'
```

- **等级 : "warn"**

##### 错误 代码示例：

```python
/*eslint no-eval: "error"*/

var obj = { x: "foo" },
    key = "x",
    value = eval("obj." + key);

(0, eval)("var a = 0");

var foo = eval;
foo("var a = 0");

// This `this` is the global object.
this.eval("var a = 0");
```
##### 正确 代码示例：

```python
/*eslint no-eval: "error"*/
/*eslint-env es6*/

var obj = { x: "foo" },
    key = "x",
    value = obj[key];

class A {
    foo() {
        // This is a user-defined method.
        this.eval("var a = 0");
    }

    eval() {
    }
}
```
**[⬆ 回到顶部](#table-of-contents)**

## <a name="no-ex-assign">禁止对 catch 子句中的异常重新赋值 (no-ex-assign)</a>

```python
'no-ex-assign': 'warn'
```

- **等级 : "warn"**

##### 错误 代码示例：

```python
/*eslint no-ex-assign: "error"*/

try {
    // code
} catch (e) {
    e = 10;
}
```
##### 正确 代码示例：

```python
/*eslint no-ex-assign: "error"*/

try {
    // code
} catch (e) {
    var foo = 10;
}
```
**[⬆ 回到顶部](#table-of-contents)**

## <a name="no-extend-native">禁止扩展原生对象 (no-extend-native)</a>

```python
'no-extend-native': 'warn'
```

- **等级 : "warn"**

##### 错误 代码示例：

```python
/*eslint no-extend-native: "error"*/

Object.prototype.a = "a";
Object.defineProperty(Array.prototype, "times", { value: 999 });
```

**[⬆ 回到顶部](#table-of-contents)**

## <a name="no-extra-bind">禁止不必要的函数绑定 (no-extra-bind)</a>
命令行中的 --fix 选项可以自动修复一些该规则报告的问题。
```python
'no-extra-bind': 'warn'
```

- **等级 : "warn"**

##### 错误 代码示例：

```python
/*eslint no-extra-bind: "error"*/
/*eslint-env es6*/

var x = function () {
    foo();
}.bind(bar);

var x = (() => {
    foo();
}).bind(bar);

var x = (() => {
    this.foo();
}).bind(bar);

var x = function () {
    (function () {
      this.foo();
    }());
}.bind(bar);

var x = function () {
    function foo() {
      this.bar();
    }
}.bind(baz);
```
##### 正确 代码示例：

```python
/*eslint no-extra-bind: "error"*/

var x = function () {
    this.foo();
}.bind(bar);

var x = function (a) {
    return a + 1;
}.bind(foo, bar);
```
**[⬆ 回到顶部](#table-of-contents)**

## <a name="no-extra-label">禁用不必要的标签 (no-extra-label)</a>
命令行中的 --fix 选项可以自动修复一些该规则报告的问题。
```python
'no-extra-label': 'warn'
```

- **等级 : "warn"**

##### 错误 代码示例：

```python
/*eslint no-extra-label: "error"*/

A: while (a) {
    break A;
}

B: for (let i = 0; i < 10; ++i) {
    break B;
}

C: switch (a) {
    case 0:
        break C;
}
```
##### 正确 代码示例：

```python
/*eslint no-extra-label: "error"*/

while (a) {
    break;
}

for (let i = 0; i < 10; ++i) {
    break;
}

switch (a) {
    case 0:
        break;
}

A: {
    break A;
}

B: while (a) {
    while (b) {
        break B;
    }
}

C: switch (a) {
    case 0:
        while (b) {
            break C;
        }
        break;
}
```
**[⬆ 回到顶部](#table-of-contents)**

## <a name="no-fallthrough">禁止 case 语句落空 (no-fallthrough)</a>
```python
'no-fallthrough': 'warn'
```

- **等级 : "warn"**

##### 错误 代码示例：

```python
/*eslint no-fallthrough: "error"*/

switch(foo) {
    case 1:
        doSomething();

    case 2:
        doSomething();
}
```
##### 正确 代码示例：

```python
/*eslint no-fallthrough: "error"*/

switch(foo) {
    case 1:
        doSomething();
        break;

    case 2:
        doSomething();
}

function bar(foo) {
    switch(foo) {
        case 1:
            doSomething();
            return;

        case 2:
            doSomething();
    }
}

switch(foo) {
    case 1:
        doSomething();
        throw new Error("Boo!");

    case 2:
        doSomething();
}

switch(foo) {
    case 1:
    case 2:
        doSomething();
}

switch(foo) {
    case 1:
        doSomething();
        // falls through

    case 2:
        doSomething();
}
```
**[⬆ 回到顶部](#table-of-contents)**

## <a name="no-func-assign">禁止对 function 声明重新赋值 (no-func-assign)</a>
```python
'no-func-assign': 'warn'
```

- **等级 : "warn"**

##### 错误 代码示例：

```python
/*eslint no-func-assign: "error"*/

function foo() {}
foo = bar;

function foo() {
    foo = bar;
}
```
##### 正确 代码示例：

```python
/*eslint no-func-assign: "error"*/

var foo = function () {}
foo = bar;

function foo(foo) { // `foo` is shadowed.
    foo = bar;
}

function foo() {
    var foo = bar;  // `foo` is shadowed.
}
```
**[⬆ 回到顶部](#table-of-contents)**

## <a name="no-implied-eval">禁用隐式的eval() (no-implied-eval)</a>
```python
'no-implied-eval': 'warn'
```

- **等级 : "warn"**

##### 错误 代码示例：

```python
/*eslint no-implied-eval: "error"*/

setTimeout("alert('Hi!');", 100);

setInterval("alert('Hi!');", 100);

execScript("alert('Hi!')");

window.setTimeout("count = 5", 10);

window.setInterval("foo = bar", 10);
```
##### 正确 代码示例：

```python
/*eslint no-implied-eval: "error"*/

setTimeout(function() {
    alert("Hi!");
}, 100);

setInterval(function() {
    alert("Hi!");
}, 100);
```
**[⬆ 回到顶部](#table-of-contents)**

## <a name="no-invalid-regexp">禁止在 RegExp 构造函数中出现无效的正则表达式 (no-invalid-regexp)</a>
```python
'no-invalid-regexp': 'warn'
```

- **等级 : "warn"**

##### 错误 代码示例：

```python
/*eslint no-invalid-regexp: "error"*/

RegExp('[')

RegExp('.', 'z')

new RegExp('\\')
```
##### 正确 代码示例：

```python
/*eslint no-invalid-regexp: "error"*/

RegExp('.')

new RegExp

this.RegExp('[')
```
**[⬆ 回到顶部](#table-of-contents)**

## <a name="no-iterator">禁用迭代器 (no-iterator)</a>
```python
'no-iterator': 'warn'
```

- **等级 : "warn"**

##### 错误 代码示例：

```python
/*eslint no-iterator: "error"*/

Foo.prototype.__iterator__ = function() {
    return new FooIterator(this);
};

foo.__iterator__ = function () {};

foo["__iterator__"] = function () {};
```
##### 正确 代码示例：

```python
/*eslint no-iterator: "error"*/

var __iterator__ = foo; // Not using the `__iterator__` property.
```
**[⬆ 回到顶部](#table-of-contents)**

## <a name="no-label-var">禁用与变量同名的标签 (no-label-var)</a>
```python
'no-label-var': 'warn'
```

- **等级 : "warn"**

##### 错误 代码示例：

```python
/*eslint no-label-var: "error"*/

var x = foo;
function bar() {
x:
  for (;;) {
    break x;
  }
}
```
##### 正确 代码示例：

```python
/*eslint no-label-var: "error"*/

// The variable that has the same name as the label is not in scope.

function foo() {
  var q = t;
}

function bar() {
q:
  for(;;) {
    break q;
  }
}
```
**[⬆ 回到顶部](#table-of-contents)**

## <a name="no-labels">禁用标签语句 (no-labels)</a>
```python
'no-labels': ['warn', { allowLoop: true, allowSwitch: false }]
```

- **等级 : "warn"**
- **选项 "allowLoop"**: (boolean，默认是 false) - 如果这个选项被设置为 true，该规则忽略循环语句中的标签。

##### 选项 { "allowLoop": true } 的 正确 代码示例：

```python
/*eslint no-labels: ["error", { "allowLoop": true }]*/

label:
    while (true) {
        break label;
    }
```

**[⬆ 回到顶部](#table-of-contents)**

## <a name="no-lone-blocks">禁用不必要的嵌套块 (no-lone-blocks)</a>
```python
'no-lone-blocks': 'warn'
```

- **等级 : "warn"**

##### 错误 代码示例：

```python
/*eslint no-lone-blocks: "error"*/

{}

if (foo) {
    bar();
    {
        baz();
    }
}

function bar() {
    {
        baz();
    }
}

{
    function foo() {}
}

{
    aLabel: {
    }
}
```
##### 正确 代码示例：

```python
/*eslint no-lone-blocks: "error"*/
/*eslint-env es6*/

while (foo) {
    bar();
}

if (foo) {
    if (bar) {
        baz();
    }
}

function bar() {
    baz();
}

{
    let x = 1;
}

{
    const y = 1;
}

{
    class Foo {}
}

aLabel: {
}
```
**[⬆ 回到顶部](#table-of-contents)**

## <a name="no-loop-func">禁止循环中存在函数 (no-loop-func)</a>
```python
'no-loop-func': 'warn'
```

- **等级 : "warn"**

##### 错误 代码示例：

```python
/*eslint no-loop-func: "error"*/
/*eslint-env es6*/

for (var i=10; i; i--) {
    (function() { return i; })();
}

while(i) {
    var a = function() { return i; };
    a();
}

do {
    function a() { return i; };
    a();
} while (i);

let foo = 0;
for (let i=10; i; i--) {
    // Bad, function is referencing block scoped variable in the outer scope.
    var a = function() { return foo; };
    a();
}
```
##### 正确 代码示例：

```python
/*eslint no-loop-func: "error"*/
/*eslint-env es6*/

var a = function() {};

for (var i=10; i; i--) {
    a();
}

for (var i=10; i; i--) {
    var a = function() {}; // OK, no references to variables in the outer scopes.
    a();
}

for (let i=10; i; i--) {
    var a = function() { return i; }; // OK, all references are referring to block scoped variables in the loop.
    a();
}

var foo = 100;
for (let i=10; i; i--) {
    var a = function() { return foo; }; // OK, all references are referring to never modified variables.
    a();
}
//... no modifications of foo after this loop ...
```
**[⬆ 回到顶部](#table-of-contents)**

## <a name="no-mixed-operators">禁止混合使用不同的操作符 (no-mixed-operators)</a>
```python
'no-mixed-operators': [
      'warn',
      {
        groups: [
          ['&', '|', '^', '~', '<<', '>>', '>>>'],
          ['==', '!=', '===', '!==', '>', '>=', '<', '<='],
          ['&&', '||'],
          ['in', 'instanceof'],
        ],
        allowSamePrecedence: false,
      },
    ]
```

- **等级 : "warn"**
- **选项 "groups "**:  (string[][]) - 指定要比较的操作符分组。 当该规则比较两个操作符时，，如果操作符在同一分组内，该规则会进行检查。否则这规则忽略它。它值是个列表组。这个组是二元操作符列表。默认为各种操作符的组。 

- **选项 "allowSamePrecedence  "**:  (boolean) - 指定允许使用混合的两个操作符，前提是它们有同样的优先级。 默认为 true.

##### 选项 {"groups": [["&", "|", "^", "~", "<<", ">>", ">>>"], ["&&", "||"]]} 的 错误 代码示例：

```python
/*eslint no-mixed-operators: ["error", {"groups": [["&", "|", "^", "~", "<<", ">>", ">>>"], ["&&", "||"]]}]*/

var foo = a && b < 0 || c > 0 || d + 1 === 0;
var foo = a & b | c;
```

##### 选项 {"groups": [["&", "|", "^", "~", "<<", ">>", ">>>"], ["&&", "||"]]} 的 正确 代码示例：

```python
/*eslint no-mixed-operators: ["error", {"groups": [["&", "|", "^", "~", "<<", ">>", ">>>"], ["&&", "||"]]}]*/

var foo = a || b > 0 || c + 1 === 0;
var foo = a && b > 0 && c + 1 === 0;
var foo = (a && b < 0) || c > 0 || d + 1 === 0;
var foo = a && (b < 0 ||  c > 0 || d + 1 === 0);
var foo = (a & b) | c;
var foo = a & (b | c);
var foo = a + b * c;
var foo = a + (b * c);
var foo = (a + b) * c;
```

##### 选项 {"allowSamePrecedence": false} 的 错误 代码示例：

```python
/*eslint no-mixed-operators: ["error", {"allowSamePrecedence": false}]*/

// + and - have the same precedence.
var foo = a + b - c;
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="no-multi-str">禁止多行字符串 (no-multi-str)</a>
```python
'no-multi-str': 'warn'
```

- **等级 : "warn"**

##### 错误 代码示例：

```python
/*eslint no-multi-str: "error"*/
var x = "Line 1 \
         Line 2";
```
##### 正确 代码示例：

```python
/*eslint no-multi-str: "error"*/

var x = "Line 1\n" +
        "Line 2";
```
**[⬆ 回到顶部](#table-of-contents)**

## <a name="no-native-resssign">禁止重新分配本地对象（no-native-resssign）</a>
此规则在ESLint v3.3.0 中已弃用，并由no-global-assign规则取代。
```python
'no-native-reassign': 'warn'
```

- **等级 : "warn"**

##### 错误 代码示例：

```python
/*eslint no-native-reassign: "error"*/

Object = null
undefined = 1
/*eslint no-native-reassign: "error"*/
/*eslint-env browser*/

window = {}
length = 1
top = 1
/*eslint no-native-reassign: "error"*/
/*globals a:false*/

a = 1
```
##### 正确 代码示例：

```python
/*eslint no-native-reassign: "error"*/

a = 1
var b = 1
b = 2
/*eslint no-native-reassign: "error"*/
/*eslint-env browser*/

onload = function() {}
/*eslint no-native-reassign: "error"*/
/*globals a:true*/

a = 1
```
**[⬆ 回到顶部](#table-of-contents)**

## <a name="no-negated-in-lhs">不允许在in表达式中否定左操作数（no-negated-in-lhs）</a>
这个规则在ESLint v3.3.0中被弃用，并被no-unsafe-negation取代。
```python
'no-negated-in-lhs': 'warn'
```

- **等级 : "warn"**

##### 错误 代码示例：

```python
/*eslint no-negated-in-lhs: "error"*/

if(!key in object) {
    // operator precedence makes it equivalent to (!key) in object
    // and type conversion makes it equivalent to (key ? "false" : "true") in object
}
```
##### 正确 代码示例：

```python
/*eslint no-negated-in-lhs: "error"*/

if(!(key in object)) {
    // key is not in object
}

if(('' + !key) in object) {
    // make operator precedence and type conversion explicit
    // in a rare situation when that is the intended meaning
}
```
**[⬆ 回到顶部](#table-of-contents)**
