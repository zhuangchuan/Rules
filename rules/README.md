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
1. [禁用Function构造函数 (no-new-func)](#no-new-func)
1. [禁止使用 Object 构造函数 (no-new-object)](#no-new-object)
1. [禁止Symbol构造函数 (no-new-symbol)](#no-new-symbol)
1. [禁止原始包装实例 (no-new-wrappers)](#no-new-wrappers)
1. [禁止将全局对象当作函数进行调用 (no-obj-calls)](#no-obj-calls)
1. [禁用八进制字面量 (no-octal)](#no-octal)
1. [禁止在字符串字面量中使用八进制转义序列 (no-octal-escape)](#no-octal-escape)
1. [禁止重新声明变量 (no-redeclare)](#no-redeclare)
1. [禁止正则表达式字面量中出现多个空格 (no-regex-spaces)](#no-regex-spaces)  
1. [禁止使用特定的语法 (no-restricted-syntax)](#no-restricted-syntax)
1. [禁用 Script URL (no-script-url)](#no-script-url)
1. [禁止自身赋值 (no-self-assign)](#no-self-assign)
1. [禁止自身比较（no-self-compare）](#no-self-compare)
1. [不允许使用逗号操作符 (no-sequences)](#no-sequences)
1. [关键字不能被遮蔽 (no-shadow-restricted-names)](#no-shadow-restricted-names)  
1. [禁用稀疏数组 (no-sparse-arrays)](#no-sparse-arrays)
1. [不允许在常规字符串中使用模板字面量占位符语法 (no-template-curly-in-string)](#no-template-curly-in-string)
1. [在构造函数中禁止在调用super()之前使用this或super。 (no-this-before-super)](#no-this-before-super)
1. [限制可以被抛出的异常 (no-throw-literal) ](#no-throw-literal)
1. [禁用未声明的变量 (no-undef)](#no-undef)
1. [禁用特定的全局变量 (no-restricted-globals)](#no-restricted-globals)
1. [禁止使用令人困惑的多行表达式 (no-unexpected-multiline)](#no-unexpected-multiline)
1. [禁止在 return、throw、continue 和 break 语句后出现不可达代码 (no-unreachable)](#no-unreachable)
1. [禁止未使用过的表达式 (no-unused-expressions)](#no-unused-expressions)

1. [禁用 eval()（no-eval）](#no-eval)
1. [禁用 eval()（no-eval）](#no-eval)
1. [禁用 eval()（no-eval）](#no-eval)
1. [禁用 eval()（no-eval）](#no-eval)
1. [禁用 eval()（no-eval）](#no-eval)
1. [禁用 eval()（no-eval）](#no-eval)
1. [禁用 eval()（no-eval）](#no-eval)
1. [禁用 eval()（no-eval）](#no-eval)
1. [禁用 eval()（no-eval）](#no-eval)
1. [禁用 eval()（no-eval）](#no-eval)
1. [禁用 eval()（no-eval）](#no-eval)
1. [禁用 eval()（no-eval）](#no-eval)
1. [禁用 eval()（no-eval）](#no-eval)
1. [禁用 eval()（no-eval）](#no-eval)
  
  
# 代码规范常见问题


## <a name="semi">要求或禁止使用分号代替 ASI (semi)</a>
命令行中的 --fix 选项可以自动修复一些该规则报告的问题。
>该规则强制使用一致的分号。
```javascript
semi: ['error', 'always']
```
- **等级 : "error"**
- **选项 "always"**: (默认) 要求在语句末尾使用分号
##### 默认选项 "always" 的 <font color=#f00>错误</font> 代码示例：
```javascript
/*eslint semi: ["error", "always"]*/

var name = "ESLint"

object.method = function() {
    // ...
}
```
##### 默认选项 "always" 的 正确 代码示例：
```javascript
/*eslint semi: "error"*/

var name = "ESLint";

object.method = function() {
    // ...
};
```
**[⬆ 回到顶部](#table-of-contents)**
   
   
## <a name="no-unused-vars">禁止未使用过的变量 (no-unused-vars)</a>
>此规则旨在消除未使用过的变量，方法和方法中的参数名，当发现这些存在，发出警告。
 符合下面条件的变量被认为是可以使用的:
 
> * 作为回调函数
> * 被读取 (var y = x)
> * 传入函数中作为argument对象(doSomething(x))
> * 在传入到另一个函数的函数中被读取

>一个变量仅仅是被赋值为 (var x = 5) 或者是被声明过，则认为它是没被考虑使用。
```javascript
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
```javascript
/*eslint no-unused-vars: ["error", { "args": "none" }]*/
    
(function(foo, bar, baz) {
    return bar;
})();
```
##### 选项 { "ignoreRestSiblings": true } 的 正确 代码示例：
```javascript
/*eslint no-unused-vars: ["error", { "ignoreRestSiblings": true }]*/
// 'type' is ignored because it has a rest property sibling.
var { type, ...coords } = data;
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="no-console">禁用 console (no-console)</a>
>该规则禁止调用 console 对象的方法。
```javascript
'no-console': 'off'
```
- **选项 "off"**: 关闭禁用

**[⬆ 回到顶部](#table-of-contents)**


## <a name="array-callback-return">强制数组方法的回调函数中有 return 语句 (array-callback-return)</a>
>该规则发现以下方法的回调函数，然后检查return语句的使用。
> * Array.from
> * Array.prototype.every
> * Array.prototype.filter
> * Array.prototype.find
> * Array.prototype.findIndex
> * Array.prototype.map
> * Array.prototype.reduce
> * Array.prototype.reduceRight
> * Array.prototype.some
> * Array.prototype.sort
> * 以上类型的数据。
```javascript
'array-callback-return': 'off'
```
- **选项 "off"**: 关闭禁用
**[⬆ 回到顶部](#table-of-contents)**


 ## <a name="default-case">要求 Switch 语句中有 Default 分支 (default-case)</a>
 >此规则的目的是在 switch 语句中强制声明 default 分支。或者也可以在最后一个 case 分支下，使用 // no default 来表明此处不需要 default 分支。注释可以任何形式出现，比如 // No Default。
 ```javascript
 'default-case': ['warn', { commentPattern: '^no default$' }]
 ```
 - **等级 : "warn"**
 - **选项 "commentPattern "**: 设置 commentPattern 为一个正则表达式字符串，来改变默认的 /^no default$/i 注释匹配模式
 此规则的目的是在 switch 语句中强制声明 default 分支。或者也可以在最后一个 case 分支下，使用 // no default 来表明此处不需要 default 分支。注释可以任何形式出现，比如 // No Default。
##### 错误 代码示例：
```javascript
/*eslint default-case: "error"*/
 
switch (a) {
case 1:
     /* code */
     break;
}
```
##### 正确 代码示例：
```javascript
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
>该规则旨在强制成员表达式中强制换行的一致性。防止既在点号操作之前也在之后使用换行符。
 ```javascript
'dot-location': ['warn', 'property']
 ```
- **等级 : "warn"**
- **选项 "property"**: 表达式中的点号操作符应该和属性在同一行。   
##### 选项 "property" 的 错误 代码示例：
```javascript
/*eslint dot-location: ["error", "property"]*/
var foo = object.
property;
```
##### 选项 "property" 的 正确 代码示例：
```javascript
/*eslint dot-location: ["error", "property"]*/
   
var foo = object
.property;
var bar = object.property;
```   
**[⬆ 回到顶部](#table-of-contents)**


## <a name="eqeqeq">要求使用 === 和 !== (eqeqeq)</a>
命令行中的 --fix 选项可以自动修复一些该规则报告的问题。
>该规则旨在消除非类型安全的相等操作符。
 ```javascript
eqeqeq: ['warn', 'allow-null']
 ```
- **等级 : "warn"**
- **选项 "allow-null"**: 使用 “always”，然后传一个 “null” 选项，属性值为 “ignore” 代替。这将告诉 eslint 除了与 null 字面量进行比较时，总是强制使用绝对相等。
   
**[⬆ 回到顶部](#table-of-contents)**


## <a name="new-parens">要求调用无参构造函数时带括号 (new-parens)</a>
命令行中的 --fix 选项可以自动修复一些该规则报告的问题。
>该规则目的在于，当通过 new 关键字调用构造函数时，要求使用圆括号，以此提高代码的清晰度。
```javascript
'new-parens': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
/*eslint new-parens: "error"*/

var person = new Person;
var person = new (Person);
```
##### 正确 代码示例：
```javascript
/*eslint new-parens: "error"*/

var person = new Person();
var person = new (Person)();
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="no-array-constructor">禁止使用 Array 构造函数 (no-array-constructor)</a>
>该规则禁止使用 Array 构造函数。
```javascript
'no-array-constructor': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
/*eslint no-array-constructor: "error"*/

Array(0, 1, 2)
/*eslint no-array-constructor: "error"*/

new Array(0, 1, 2)
```
##### 正确 代码示例：
```javascript
/*eslint no-array-constructor: "error"*/

Array(500)
/*eslint no-array-constructor: "error"*/

new Array(someOtherArray.length)
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="no-caller">禁用 caller 或 callee (no-caller)</a>
>此规则目的在于阻止使用已弃用的代码和次优的代码，而且禁止使用 arguments.caller 和 arguments.callee。因此，当 arguments.caller 和 arguments.callee 被使用时，该规则将会发出警告。
```javascript
'no-caller': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例
```javascript
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
```javascript
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
>该规则禁止在 if、for、while 和 do...while 语句中出现模棱两可的赋值操作符。
```javascript
'no-cond-assign': ['warn', 'always']
```
- **等级 : "warn"**
- **选项 "always"**: 禁止条件语句中出现赋值语句。
##### 选项 "always" 的 错误 代码示例：

```javascript
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
```javascript
/*eslint no-cond-assign: ["error", "always"]*/

// Assignment replaced by comparison
var x;
if (x === 0) {
    var b = 1;
}
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="no-const-assign">不允许改变用const声明的变量 (no-const-assign)</a>
>该规则旨在标记修改用const关键字声明的变量。
```javascript
'no-const-assign': 'warn'
```
- **等级 : "warn"**

##### 错误 代码示例：
```javascript
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
```javascript
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
>该规则禁止在正则表达式中出现控制字符。
```javascript
'no-control-regex': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
/*eslint no-control-regex: "error"*/

var pattern1 = /\x1f/;
var pattern2 = new RegExp("\x1f");
```
##### 正确 代码示例：
```javascript
/*eslint no-control-regex: "error"*/

var pattern1 = /\x20/;
var pattern2 = new RegExp("\x20");
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="no-delete-var">禁止删除变量 (no-delete-var)</a>
>该规则禁止对变量使用 delete 操作符。
 
>如果 ESLint 是在严格模式下解析代码，解析器（而不是该规则）会报告错误。
```javascript
'no-delete-var': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
/*eslint no-delete-var: "error"*/

var x;
delete x;
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="no-dupe-args">禁止在 function 定义中出现重复的参数 (no-dupe-args)</a>
>该规则禁止在函数定义或表达中出现重名参数。该规则并不适用于箭头函数或类方法，因为解析器会报告这样的错误。

>如果 ESLint 在严格模式下解析代码，解析器（不是该规则）将报告这样的错误。
```javascript
'no-dupe-args': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
/*eslint no-dupe-args: "error"*/

function foo(a, b, a) {
    console.log("value of the second a:", a);
}

var bar = function (a, b, a) {
    console.log("value of the second a:", a);
};
```
##### 正确 代码示例：
```javascript
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
>该规则旨在标记类成员中重复名称的使用。
```javascript
'no-dupe-class-members': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
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
```javascript
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
>该规则禁止在对象字面量中出现重复的键。
```javascript
'no-dupe-keys': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
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
```javascript
/*eslint no-dupe-keys: "error"*/

var foo = {
    bar: "baz",
    quxx: "qux"
};
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="no-duplicate-case">禁止重复 case 标签（no-duplicate-case）</a>
>该规则禁止在 switch 语句中的 case 子句中出现重复的测试表达式。
```javascript
'no-duplicate-case': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
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
```javascript
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
>该规则禁止在正则表达式中出现空字符集。
```javascript
'no-empty-character-class': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
/*eslint no-empty-character-class: "error"*/

/^abc[]/.test("abcdefg"); // false
"abcdefg".match(/^abc[]/); // null
```
##### 正确 代码示例：
```javascript
/*eslint no-empty-character-class: "error"*/

/^abc/.test("abcdefg"); // true
"abcdefg".match(/^abc/); // ["abc"]

/^abc[a-z]/.test("abcdefg"); // true
"abcdefg".match(/^abc[a-z]/); // ["abcd"]
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="no-empty-pattern">禁止使用空解构模式 (no-empty-pattern)</a>
>此规则目的在于标记出在解构对象和数组中的任何的空模式，每当遇到一个这样的空模式，该规则就会报告一个问题。
```javascript
'no-empty-pattern': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
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
```javascript
/*eslint no-empty-pattern: "error"*/

var {a = {}} = foo;
var {a = []} = foo;
function foo({a = {}}) {}
function foo({a = []}) {}
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="no-eval">禁用 eval()（no-eval）</a>
>此规则目的在于通过禁止使用 eval() 函数来避免潜在地危险、不必要的和运行效率低下的代码。因此，当时使用 eval() 函数时，该规则将发出警告。
```javascript
'no-eval': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
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
```javascript
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
>该规则禁止对 catch 子句中的异常重新赋值。
```javascript
'no-ex-assign': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
/*eslint no-ex-assign: "error"*/

try {
    // code
} catch (e) {
    e = 10;
}
```
##### 正确 代码示例：
```javascript
/*eslint no-ex-assign: "error"*/

try {
    // code
} catch (e) {
    var foo = 10;
}
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="no-extend-native">禁止扩展原生对象 (no-extend-native)</a>
>禁止直接修改内建对象的属性。
```javascript
'no-extend-native': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
/*eslint no-extend-native: "error"*/

Object.prototype.a = "a";
Object.defineProperty(Array.prototype, "times", { value: 999 });
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="no-extra-bind">禁止不必要的函数绑定 (no-extra-bind)</a>
命令行中的 --fix 选项可以自动修复一些该规则报告的问题。
>此规则目的在于避免不必要的 bind() 使用，并且当立即执行的函数表达式 (IIFE) 使用 bind()，但是没有一个合适的 this 值时，该规则会发出警告。此规则不会标记有函数参数绑定的bind() 的使用情况。

>注意：箭头函数不能通过使用 bind() 设置它们的自己 this 值。此规则把所有使用bind() 的箭头函数标记为是有问题的。
```javascript
'no-extra-bind': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
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
```javascript
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
>该规则旨在消除不必要的标签。
```javascript
'no-extra-label': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
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
```javascript
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
>该规则旨在消除非故意 case 落空行为。因此，它会标记处没有使用注释标明的落空情况。
```javascript
'no-fallthrough': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
/*eslint no-fallthrough: "error"*/

switch(foo) {
    case 1:
        doSomething();

    case 2:
        doSomething();
}
```
##### 正确 代码示例：
```javascript
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
>该规则禁止对 function 声明重新赋值。
```javascript
'no-func-assign': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
/*eslint no-func-assign: "error"*/

function foo() {}
foo = bar;

function foo() {
    foo = bar;
}
```
##### 正确 代码示例：
```javascript
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
>此规则目的在于消除使用 setTimeout()、setInterval() 或 execScript() 时隐式的 eval()。因此，当它们中的任何一个使用字符串作为第一个参数时，该规则将发出警告。
```javascript
'no-implied-eval': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
/*eslint no-implied-eval: "error"*/

setTimeout("alert('Hi!');", 100);

setInterval("alert('Hi!');", 100);

execScript("alert('Hi!')");

window.setTimeout("count = 5", 10);

window.setInterval("foo = bar", 10);
```
##### 正确 代码示例：
```javascript
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
>该规则禁止在 RegExp 构造函数中出现无效的正则表达式。
```javascript
'no-invalid-regexp': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
/*eslint no-invalid-regexp: "error"*/

RegExp('[')

RegExp('.', 'z')

new RegExp('\\')
```
##### 正确 代码示例：
```javascript
/*eslint no-invalid-regexp: "error"*/

RegExp('.')

new RegExp

this.RegExp('[')
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="no-iterator">禁用迭代器 (no-iterator)</a>
>此规则目的在于防止因使用 __iterator__属性而出现的错误，并不是所有浏览器都实现了这个属性。因此，当遇到 __iterator__属性时，该规则将会发出警告。
```javascript
'no-iterator': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
/*eslint no-iterator: "error"*/

Foo.prototype.__iterator__ = function() {
    return new FooIterator(this);
};

foo.__iterator__ = function () {};

foo["__iterator__"] = function () {};
```
##### 正确 代码示例：
```javascript
/*eslint no-iterator: "error"*/

var __iterator__ = foo; // Not using the `__iterator__` property.
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="no-label-var">禁用与变量同名的标签 (no-label-var)</a>
>该规则旨在通过禁止使用同一作用域下的同名的变量做为标签，来创建更清晰的代码。
```javascript
'no-label-var': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
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
```javascript
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
>此规则旨在消除 JavaScript 中标签的使用。当遇到标签语句时，该规则将发出警告。
```javascript
'no-labels': ['warn', { allowLoop: true, allowSwitch: false }]
```
- **等级 : "warn"**
- **选项 "allowLoop"**: (boolean，默认是 false) - 如果这个选项被设置为 true，该规则忽略循环语句中的标签。
##### 选项 { "allowLoop": true } 的 正确 代码示例：
```javascript
/*eslint no-labels: ["error", { "allowLoop": true }]*/

label:
    while (true) {
        break label;
    }
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="no-lone-blocks">禁用不必要的嵌套块 (no-lone-blocks)</a>
>该规则旨在消除脚本顶部或其它块中不必要的和潜在的令人困惑的代码块。
```javascript
'no-lone-blocks': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
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
```javascript
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
>这个错误的出现会导致代码不能如你期望的那样运行，也表明你对 JavaScript 这门语言存在误解。 如果你不修复这个错误，你的代码可能会正常运行，带在某些情况下，可能会出现意想不到的行为。
```javascript
'no-loop-func': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
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
```javascript
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
>该规则检查 BinaryExpression 和 LogicalExpression。
 该规则可能与 no-extra-parens 规则。如果你同时使用该规则和no-extra-parens 规则，你需要使用 no-extra-parens 规则的 nestedBinaryExpressions 的选项。
```javascript
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
```javascript
/*eslint no-mixed-operators: ["error", {"groups": [["&", "|", "^", "~", "<<", ">>", ">>>"], ["&&", "||"]]}]*/

var foo = a && b < 0 || c > 0 || d + 1 === 0;
var foo = a & b | c;
```
##### 选项 {"groups": [["&", "|", "^", "~", "<<", ">>", ">>>"], ["&&", "||"]]} 的 正确 代码示例：
```javascript
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
```javascript
/*eslint no-mixed-operators: ["error", {"allowSamePrecedence": false}]*/

// + and - have the same precedence.
var foo = a + b - c;
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="no-multi-str">禁止多行字符串 (no-multi-str)</a>
>该规则是为了防止多行字符串的使用。
```javascript
'no-multi-str': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
/*eslint no-multi-str: "error"*/
var x = "Line 1 \
         Line 2";
```
##### 正确 代码示例：
```javascript
/*eslint no-multi-str: "error"*/

var x = "Line 1\n" +
        "Line 2";
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="no-native-resssign">禁止重新分配本地对象（no-native-resssign）</a>
此规则在ESLint v3.3.0 中已弃用，并由no-global-assign规则取代。
>这个规则不允许修改只读的全局变量。
ESLint能够将全局变量配置为只读。
> * 指定环境
> * 指定全局
```javascript
'no-native-reassign': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
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
```javascript
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
>该规则不允许否定in表达式中的左操作数。
```javascript
'no-negated-in-lhs': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
/*eslint no-negated-in-lhs: "error"*/

if(!key in object) {
    // operator precedence makes it equivalent to (!key) in object
    // and type conversion makes it equivalent to (key ? "false" : "true") in object
}
```
##### 正确 代码示例：
```javascript
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


## <a name="no-new-func">禁用Function构造函数 (no-new-func)</a>
>该规则会高亮标记出不好的实践的使用。把一个字符串传给 Function 构造函数，你需要引擎解析该字符串，这一点同调用 eval 函数一样。
```javascript
'no-new-func': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
/*eslint no-new-func: "error"*/

var x = new Function("a", "b", "return a + b");
var x = Function("a", "b", "return a + b");
```
##### 正确 代码示例：
```javascript
/*eslint no-new-func: "error"*/

var x = function (a, b) {
    return a + b;
};
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="no-new-object">禁止使用 Object 构造函数 (no-new-object)</a>
>该规则禁止使用 Object 构造函数。。
```javascript
'no-new-object': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：

```javascript
/*eslint no-new-object: "error"*/

var myObject = new Object();

var myObject = new Object;
```
##### 正确 代码示例：

```javascript
/*eslint no-new-object: "error"*/

var myObject = new CustomObject();

var myObject = {};
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="no-new-symbol">禁止使用 Symbol 构造函数 (no-new-symbol)</a>
>这个规则是为了防止Symbol与new操作员的意外调用。
```javascript
'no-new-symbol': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
/*eslint no-new-symbol: "error"*/
/*eslint-env es6*/

var foo = new Symbol('foo');
```
##### 正确 代码示例：

```javascript
/*eslint no-new-symbol: "error"*/
/*eslint-env es6*/

var foo = Symbol('foo');


// Ignores shadowed Symbol.
function bar(Symbol) {
    const baz = new Symbol("baz");
}

```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="no-new-wrappers">禁止原始包装实例 (no-new-wrappers)</a>
>此规则目的在于消除通过 new 操作符使用 String、Number 和 Boolean 。因此，每当遇到 new String、new Number 或者 new Boolean，该规则都会发出警告。
```javascript
'no-new-wrappers': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
/*eslint no-new-wrappers: "error"*/

var stringObject = new String("Hello world");
var numberObject = new Number(33);
var booleanObject = new Boolean(false);

var stringObject = new String;
var numberObject = new Number;
var booleanObject = new Boolean;
```
##### 正确 代码示例：
```javascript
/*eslint no-new-wrappers: "error"*/

var text = String(someValue);
var num = Number(someValue);

var object = new MyString();
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="no-obj-calls">禁止将全局对象当作函数进行调用 (no-obj-calls)</a>
>该规则禁止将 Math、JSON 和 Reflect 对象当作函数进行调用。
```javascript
'no-obj-calls': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
/*eslint no-obj-calls: "error"*/

var math = Math();
var json = JSON();
var reflect = Reflect();
```
##### 正确 代码示例：
```javascript
/*eslint no-obj-calls: "error"*/

function area(r) {
    return Math.PI * r * r;
}
var object = JSON.parse("{}");
var value = Reflect.get({ x: 1, y: 2 }, "x");
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="no-obj-calls">禁用八进制字面量 (no-octal)</a>
```javascript
'no-octal': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
/*eslint no-octal: "error"*/

var num = 071;
var result = 5 + 07;
```
##### 正确 代码示例：
```javascript
/*eslint no-octal: "error"*/

var num  = "071";
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="no-octal-escape">禁止在字符串字面量中使用八进制转义序列 (no-octal-escape)</a>
>该规则禁止在字符串字面量中使用八进制转义序列。
如果 ESLint 是在严格模式下解析代码，解析器（而不是该规则）会报告错误。
```javascript
'no-octal-escape': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
/*eslint no-octal-escape: "error"*/

var foo = "Copyright \251";
```
##### 正确 代码示例：
```javascript
/*eslint no-octal-escape: "error"*/

var foo = "Copyright \u00A9";   // unicode

var foo = "Copyright \xA9";     // hexadecimal
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="no-redeclare">禁止重新声明变量 (no-redeclare)</a>
>此规则目旨在消除同一作用域中多次声明同一变量。
```javascript
'no-redeclare': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
/*eslint no-redeclare: "error"*/

var a = 3;
var a = 10;
```
##### 正确 代码示例：
```javascript
/*eslint no-redeclare: "error"*/

var a = 3;
// ...
a = 10;
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="no-regex-spaces">禁止正则表达式字面量中出现多个空格 (no-regex-spaces)</a>
>该规则禁止在正则表达式字面量中出现多个空格。
```javascript
'no-regex-spaces': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
/*eslint no-regex-spaces: "error"*/

var re = /foo   bar/;
var re = new RegExp("foo   bar");
```
##### 正确 代码示例：
```javascript
/*eslint no-regex-spaces: "error"*/

var re = /foo {3}bar/;
var re = new RegExp("foo {3}bar");
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="no-restricted-syntax">禁止使用特定的语法 (no-restricted-syntax)</a>
>该规则禁止使用特定的（由用户来指定）语法。
```javascript
'no-restricted-syntax': ['warn', 'WithStatement']
```
- **等级 : "warn"**
- **选项 "WithStatement"**: 禁用with 
##### 选项对话"FunctionExpression", "WithStatement", BinaryExpression[operator='in']的错误代码示例：
```javascript
/* eslint no-restricted-syntax: ["error", "FunctionExpression", "WithStatement", "BinaryExpression[operator='in']"] */

with (me) {
    dontMess();
}

var doSomething = function () {};

foo in bar;
```
##### 选项对话"FunctionExpression", "WithStatement"的正确代码示例：
```javascript
/* eslint no-restricted-syntax: ["error", "FunctionExpression", "WithStatement", "BinaryExpression[operator='in']"] */

me.dontMess();

function doSomething() {};

foo instanceof bar;
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="no-script-url">禁用 Script URL (no-script-url)</a>
```javascript
'no-script-url': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
/*eslint no-script-url: "error"*/

location.href = "javascript:void(0)";
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="no-self-assign">禁止自身赋值 (no-self-assign)</a>
>该规则旨在消除自身赋值的情况。
```javascript
'no-self-assign': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
/*eslint no-self-assign: "error"*/

foo = foo;

[a, b] = [a, b];

[a, ...b] = [x, ...b];

({a, b} = {a, x});
```
##### 正确 代码示例：
```javascript
/*eslint no-self-assign: "error"*/

foo = bar;
[a, b] = [b, a];

// This pattern is warned by the `no-use-before-define` rule.
let foo = foo;

// The default values have an effect.
[foo = 1] = [foo];
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="no-self-compare">禁止自身比较（no-self-compare）</a>
>该规则为了突出一个潜在的令人困惑的、无意义的代码。几乎没有场景需要你比较变量本身。
```javascript
'no-self-compare': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
/*eslint no-self-compare: "error"*/

var x = 10;
if (x === x) {
    x = 20;
}
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="no-sequences">不允许使用逗号操作符 (no-sequences)</a>
> 此规则禁止逗号操作符的使用，以下情况除外：
> * 在初始化或者更新部分 for 语句时。
> * 如果表达式序列被明确包裹在括号中。
```javascript
'no-sequences': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
/*eslint no-sequences: "error"*/

foo = doSomething(), val;

0, eval("doSomething();");

do {} while (doSomething(), !!test);

for (; doSomething(), !!test; );

if (doSomething(), !!test);

switch (val = foo(), val) {}

while (val = foo(), val < 42);

with (doSomething(), val) {}
```
##### 正确 代码示例：
```javascript
/*eslint no-sequences: "error"*/

foo = (doSomething(), val);

(0, eval)("doSomething();");

do {} while ((doSomething(), !!test));

for (i = 0, j = 10; i < j; i++, j--);

if ((doSomething(), !!test));

switch ((val = foo(), val)) {}

while ((val = foo(), val < 42));

// with ((doSomething(), val)) {}
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="no-shadow-restricted-names">关键字不能被遮蔽 (no-shadow-restricted-names)</a>
```javascript
'no-shadow-restricted-names': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
/*eslint no-shadow-restricted-names: "error"*/

function NaN(){}

!function(Infinity){};

var undefined;

try {} catch(eval){}
```
##### 正确 代码示例：
```javascript
/*eslint no-shadow-restricted-names: "error"*/

var Object;

function f(a, b){}
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="no-sparse-arrays">禁用稀疏数组 (no-sparse-arrays)</a>
>该规则禁止使用稀疏数组，也就是逗号之前没有任何元素的数组。该规则不适用于紧随最后一个元素的拖尾逗号的情况。
```javascript
'no-sparse-arrays': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
/*eslint no-sparse-arrays: "error"*/

var items = [,];
var colors = [ "red",, "blue" ];
```
##### 正确 代码示例：
```javascript
/*eslint no-sparse-arrays: "error"*/

var items = [];
var items = new Array(23);

// trailing comma (after the last element) is not a problem
var colors = [ "red", "blue", ];
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="no-template-curly-in-string">不允许在常规字符串中使用模板字面量占位符语法 (no-template-curly-in-string)</a>
>这个规则的目的是警告当一个常规字符串包含了一个模板字面上的占位符。它将在发现包含模板文字的位置符($ {something})的字符串时发出警告($ {something})，它使用“或”引用引号。
```javascript
'no-template-curly-in-string': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
/*eslint no-template-curly-in-string: "error"*/
"Hello ${name}!";
'Hello ${name}!';
"Time: ${12 * 60 * 60 * 1000}";
```
##### 正确 代码示例：
```javascript
/*eslint no-template-curly-in-string: "error"*/
`Hello ${name}!`;
`Time: ${12 * 60 * 60 * 1000}`;

templateFunction`Hello ${name}`;
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="no-this-before-super">在构造函数中禁止在调用super()之前使用this或super。 (no-this-before-super)</a>
>该规则旨在标记出在调用 super() 之前使用 this 或 super 的情况。
```javascript
'no-this-before-super': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
/*eslint no-this-before-super: "error"*/
/*eslint-env es6*/

class A extends B {
    constructor() {
        this.a = 0;
        super();
    }
}

class A extends B {
    constructor() {
        this.foo();
        super();
    }
}

class A extends B {
    constructor() {
        super.foo();
        super();
    }
}

class A extends B {
    constructor() {
        super(this.foo());
    }
}
```
##### 正确 代码示例：
```javascript
/*eslint no-this-before-super: "error"*/
/*eslint-env es6*/

class A {
    constructor() {
        this.a = 0; // OK, this class doesn't have an `extends` clause.
    }
}

class A extends B {
    constructor() {
        super();
        this.a = 0; // OK, this is after `super()`.
    }
}

class A extends B {
    foo() {
        this.a = 0; // OK. this is not in a constructor.
    }
}
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="no-throw-literal">限制可以被抛出的异常 (no-throw-literal)</a>
>此规则目的在于保持异常抛出的一致性，通过禁止抛出字面量和那些不可能是 Error 对象的表达式。
```javascript
'no-throw-literal': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
/*eslint no-throw-literal: "error"*/
/*eslint-env es6*/

throw "error";

throw 0;

throw undefined;

throw null;

var err = new Error();
throw "an " + err;
// err is recast to a string literal

var err = new Error();
throw `${err}`
```
##### 正确 代码示例：
```javascript
/*eslint no-throw-literal: "error"*/

throw new Error();

throw new Error("error");

var e = new Error("error");
throw e;

try {
    throw new Error("error");
} catch (e) {
    throw e;
}
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="no-undef">禁用未声明的变量 (no-undef)</a>
>对任何未声明的变量的引用都会引起一个警告，除非显式地在 /*global ...*/ 注释中指定。
```javascript
'no-undef': 'error'
```
- **等级 : "error"**
##### 错误 代码示例：
```javascript
/*eslint no-undef: "error"*/

var a = someFunction();
b = 10;
```
##### 有 global 声明时，该规则的 正确 代码示例：
```javascript
//*global someFunction b:true*/
 /*eslint no-undef: "error"*/
 
 var a = someFunction();
 b = 10;
```
##### 有 global 声明时，该规则的 错误 代码示例：
```javascript
/*global b*/
/*eslint no-undef: "error"*/

b = 10;
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="no-restricted-globals">禁用特定的全局变量 (no-restricted-globals)</a>
>该规则允许你指定你不想在你的应用中使用的全局变量的名称。
```javascript
'no-restricted-globals': ['error'].concat(restrictedGlobals)
```
- **等级 : "error"**
- **选项 "restrictedGlobals"**: 全局变量
##### 全局变量 "event", "fdescribe" 的 错误 代码示例：
```javascript
/*global event, fdescribe*/
/*eslint no-restricted-globals: ["error", "event", "fdescribe"]*/

function onClick() {
    console.log(event);
}

fdescribe("foo", function() {
});
```
##### 全局变量 "event" 的 正确 代码示例：
```javascript
/*global event*/
/*eslint no-restricted-globals: ["error", "event"]*/

import event from "event-module";
/*global event*/
/*eslint no-restricted-globals: ["error", "event"]*/

var event = 1;
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="no-unexpected-multiline">禁止使用令人困惑的多行表达式 (no-unexpected-multiline)</a>
>该规则禁止使用令人困惑的多行表达式。
```javascript
'no-unexpected-multiline': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
/*eslint no-unexpected-multiline: "error"*/

var foo = bar
(1 || 2).baz();

var hello = 'world'
[1, 2, 3].forEach(addNumber);

let x = function() {}
`hello`

let x = function() {}
x
`hello`

let x = foo
/regex/g.test(bar)
```
##### 正确 代码示例：
```javascript
var foo = bar;
(1 || 2).baz();

var foo = bar
;(1 || 2).baz()

var hello = 'world';
[1, 2, 3].forEach(addNumber);

var hello = 'world'
void [1, 2, 3].forEach(addNumber);

let x = function() {};
`hello`

let tag = function() {}
tag `hello`
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="no-unexpected-multiline">禁止使用令人困惑的多行表达式 (no-unexpected-multiline)</a>
>该规则禁止在 return、throw、continue 和 break 语句后出现不可达代码。
```javascript
'no-unexpected-multiline': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
/*eslint no-unreachable: "error"*/

function foo() {
    return true;
    console.log("done");
}

function bar() {
    throw new Error("Oops!");
    console.log("done");
}

while(value) {
    break;
    console.log("done");
}

throw new Error("Oops!");
console.log("done");

function baz() {
    if (Math.random() < 0.5) {
        return;
    } else {
        throw new Error();
    }
    console.log("done");
}

for (;;) {}
console.log("done");
```
##### 正确 代码示例：
```javascript
/*eslint no-unreachable: "error"*/

function foo() {
    return bar();
    function bar() {
        return 1;
    }
}

function bar() {
    return x;
    var x;
}

switch (foo) {
    case 1:
        break;
        var x;
}
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="no-unused-expressions">禁止未使用过的表达式 (no-unused-expressions)</a>
>此规则的目的在于消除未使用过的表达式，它们在程序中不起任何作用。
 该规则不适用于使用 new 操作符的函数或构造函数调用，因为它们可能会有副作用
```javascript
'no-unused-expressions': [
  'warn',
  {
    allowShortCircuit: true,
    allowTernary: true,
    allowTaggedTemplates: true,
  },
]
```
- **等级 : "warn"**
- **选项 "allowShortCircuit"**: 设置为 true 将允许你在表达式中使用逻辑短路求值。（默认为 false）
- **选项 "allowTernary"**: 设置为 true 将允许你在表达式中使用类似逻辑短路求值的三元运算符。（默认为 false）。
- **选项 "allowTaggedTemplates"**: 设置为 true 将允许你在表达式中使用带标签的模板字面量 (默认: false)。
#####选项 { "allowShortCircuit": true } 的 错误 代码示例：
```javascript
/*eslint no-unused-expressions: ["error", { "allowShortCircuit": true }]*/

a || b
```
##### 选项 { "allowShortCircuit": true } 的 正确 代码示例：
```javascript
/*eslint no-unused-expressions: ["error", { "allowShortCircuit": true }]*/

a && b()
a() || (b = c)
```
##### 选项 { "allowTernary": true } 的 错误 代码示例：
```javascript
/*eslint no-unused-expressions: ["error", { "allowTernary": true }]*/

a ? b : 0
a ? b : c()
```
##### 选项 { "allowTernary": true } 的 正确 代码示例：
```javascript
/*eslint no-unused-expressions: ["error", { "allowTernary": true }]*/

a ? b() : c()
a ? (b = c) : d()
```
##### 选项 { "allowTaggedTemplates": true } 的 错误 代码示例：
```javascript
/*eslint no-unused-expressions: ["error", { "allowTaggedTemplates": true }]*/

`some untagged template string`;
```
##### 选项 { "allowTaggedTemplates": true } 的 正确 代码示例：
```javascript
/*eslint no-unused-expressions: ["error", { "allowTaggedTemplates": true }]*/

tag`some tagged template string`;
```
**[⬆ 回到顶部](#table-of-contents)**
