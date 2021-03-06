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
1. [禁用未使用过的标签 (no-unused-labels)](#no-unused-labels)
1. [禁止定义前使用 (no-use-before-define)](#no-use-before-define)
1. [不允许在对象上使用不必要的计算属性键(no-useless-computed-key)](#no-useless-computed-key)
1. [禁止没有必要的字符拼接 (no-useless-concat)](#no-useless-concat)
1. [禁用不必要的构造函数 (no-useless-constructor)](#no-useless-constructor)
1. [禁用不必要的转义 (no-useless-escape)](#no-useless-escape)
1. [禁止将import， export和destructured assignments重命名为相同的名称（no-useless-rename）](#no-useless-rename)
1. [禁用 with 语句 (no-with)](#no-with)
1. [禁止属性前有空白 (no-whitespace-before-property)](#no-whitespace-before-property)
1. [要求必须有基数 (radix)](#radix)
1. [禁用函数内没有yield的 generator 函数（require-yield）](#require-yield)
1. [强制限制扩展运算符及其表达式之间的空格（rest-spread-spacing）](#rest-spread-spacing)
1. [要求或禁止使用严格模式指令 (strict)](#strict)
1. [要求或禁止使用 Unicode 字节顺序标记 (BOM) (unicode-bom)](#unicode-bom)
1. [要求调用 isNaN()检查 NaN (use-isnan)](#use-isnan)
1. [强制 typeof 表达式与有效的字符串进行比较 (valid-typeof)](#valid-typeof)
1. [禁止某些对象属性 (no-restricted-properties)](#no-restricted-properties)

1. [import/first](#import/first)
1. [import/no-amd](#import/no-amd)
1. [import/no-webpack-loader-syntax](#import/no-webpack-loader-syntax)

1. [防止将注释作为文本节点插入(react/jsx-no-comment-textnodes)](#react/jsx-no-comment-textnodes)
1. [禁止JSX中的重复属性(react/jsx-no-duplicate-props)](#react/jsx-no-duplicate-props)
1. [禁止使用不安全target='_blank'(react/jsx-no-target-blank)](#react/jsx-no-target-blank)
1. [在JSX中禁止未声明的变量(react/jsx-no-undef)](#react/jsx-no-undef)
1. [为用户定义的JSX组件强制实施PascalCase(react/jsx-pascal-case)](#react/jsx-pascal-case)
1. [防止React被错误地标记为未使用(react/jsx-uses-react)](#react/jsx-uses-react)
1. [防止在JSX中使用的变量被错误地标记为未使用（react/jsx-uses-vars）](#react/jsx-uses-vars)
1. [禁止children和props.dangerouslySetInnerHTML同时使用的问题（react/no-danger-with-children）](#react/no-danger-with-children)  
1. [禁止使用已弃用的方法（react/no-deprecated）](#react/no-deprecated)  
1. [禁止this.state的直接变化（react/no-deprecated）](#react/no-deprecated)  
1. [禁止isMounted的使用（react/no-is-mounted）](#react/no-is-mounted) 
1. [禁止在JSX使用缺失的React（react/react-in-jsx-scope）](#react/react-in-jsx-scope) 
1. [强制ES5或ES6类在渲染函数中返回值（react/require-render-return）](#react/require-render-return) 
1. [样式属性值强制作为对象（react/style-prop-object）](#react/style-prop-object)
 
1. [访问-表情符号（jsx-a11y/accessible-emoji）](#jsx-a11y/accessible-emoji)
1. [alt-文本（jsx-a11y/alt-text）](#jsx-a11y/alt-text)
1. [锚点-的-内容（jsx-a11y/anchor-has-content）](#jsx-a11y/anchor-has-content)
1. [aria-activedescendant-的TabIndex（jsx-a11y/aria-activedescendant-has-tabindex）](#jsx-a11y/aria-activedescendant-has-tabindex)
1. [元素不能使用无效的aria属性（jsx-a11y/aria-props）](#jsx-a11y/aria-props)
1. [aria状态和属性值必须有效（jsx-a11y/aria-proptypes）](#jsx-a11y/aria-proptypes)
1. [元素必须使用有效的aria角色（jsx-a11y/aria-role）](#jsx-a11y/aria-role)
1. [aria不受支持的元素（jsx-a11y/aria-unsupported-elements）](#jsx-a11y/aria-unsupported-elements)
1. [标题要有内容（jsx-a11y/heading-has-content）](#jsx-a11y/heading-has-content)
1. [href必须是有效性的（jsx-a11y/href-no-hash）](#jsx-a11y/href-no-hash)
1. [iframe的标题（jsx-a11y/iframe-has-title）](#jsx-a11y/iframe-has-title)
1. [img-多余的-alt（jsx-a11y/img-redundant-alt）](#jsx-a11y/img-redundant-alt)
1. [禁止access-key（jsx-a11y/no-access-key）](#jsx-a11y/no-access-key)
1. [禁用废弃的元素（jsx-a11y/no-distracting-elements）](#jsx-a11y/no-distracting-elements)
1. [禁用多余的roles（jsx-a11y/no-redundant-roles）](#jsx-a11y/no-redundant-roles)
1. [role有要求的aria props（jsx-a11y/role-has-required-aria-props）](#jsx-a11y/role-has-required-aria-props)
1. [role-支持的-aria-props（jsx-a11y/role-supports-aria-props）](#jsx-a11y/role-supports-aria-props)
1. [范围（jsx-a11y/scope）](#jsx-a11y/scope)


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
##### 选项 { "allowShortCircuit": true } 的 错误 代码示例：
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


## <a name="no-unused-labels">禁用未使用过的标签 (no-unused-labels)</a>
命令行中的 --fix 选项可以自动修复一些该规则报告的问题。
>该规则旨在消除未使用过的标签。
```javascript
'no-unused-labels': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
/*eslint no-unused-labels: "error"*/

A: var foo = 0;

B: {
    foo();
}

C:
for (let i = 0; i < 10; ++i) {
    foo();
}
```
##### 正确 代码示例：
```javascript
/*eslint no-unused-labels: "error"*/

A: {
    if (foo()) {
        break A;
    }
    bar();
}

B:
for (let i = 0; i < 10; ++i) {
    if (foo()) {
        break B;
    }
    bar();
}
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="no-use-before-define">禁止定义前使用 (no-use-before-define)</a>
>当使用一个还未声明的标示符是会报警告。
```javascript
'no-use-before-define': [
  'warn',
  {
    functions: false,
    classes: false,
    variables: false,
  },
]
```
- **等级 : "warn"**
- **选项 "functions"**: 这个参数表示该规则是否要检测函数的声明。 如果参数是 true，该规则会在引用一个未提前声明的函数时发出警报。 否则，忽略这些引用。因为函数声明作用域会被提升，所以这样做是安全的。 参数默认值是 true。
- **选项 "classes"**: 这个参数表示是否要检测上层作用域中的类声明。 如果参数是 true，该规则会在引用一个未提前声明的类时发出警报。 否则，该规则会忽略对上层作用域中的类声明的引用。 因为类声明作用域不会被提升，所以这样做可能是危险的。 参数默认是 true。
- **选项 "variables"**: 这个参数表示是否要在上层作用域内检测变量声明。 如果参数是 true，该规则会在引用一个未提前声明的变量时发出警报。 否则，该规则会忽略在上层作用域中变量声明的引用，然而仍然会报告对同一作用域中的变量声明的引用。 参数默认是 true。
##### 选项{ "functions": false }的 正确 代码示例：
```javascript
/*eslint no-use-before-define: ["error", { "functions": false }]*/

f();
function f() {}
```
##### 选项{ "classes": false }的 错误 代码示例：
```javascript
/*eslint no-use-before-define: ["error", { "classes": false }]*/
/*eslint-env es6*/

new A();
class A {
}
```
##### 选项{ "classes": false }的 正确 代码示例：
```javascript
/*eslint no-use-before-define: ["error", { "classes": false }]*/
/*eslint-env es6*/

function foo() {
    return new A();
}

class A {
}
```
##### 选项 { "variables": false } 的 错误 代码示例：
```javascript
/*eslint no-use-before-define: ["error", { "variables": false }]*/

console.log(foo);
var foo = 1;
```
##### 选项 { "variables": false } 的 正确 代码示例：
```javascript
/*eslint no-use-before-define: ["error", { "variables": false }]*/

function baz() {
    console.log(foo);
}

var foo = 1;
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="no-useless-computed-key">不允许在对象上使用不必要的计算属性键(no-useless-computed-key)</a>
命令行中的 --fix 选项可以自动修复一些该规则报告的问题。
>此规则不允许对计算属性键进行不必要的使用。
```javascript
'no-useless-computed-key': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
/*eslint-env es6*/

var a = { ['0']: 0 };
var a = { ['0+1,234']: 0 };
var a = { [0]: 0 };
var a = { ['x']: 0 };
var a = { ['x']() {} };
```
##### 正确 代码示例：
```javascript
/*eslint no-useless-computed-key: "error"*/

var c = { 'a': 0 };
var c = { 0: 0 };
var a = { x() {} };
var c = { a: 0 };
var c = { '0+1,234': 0 };
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="no-useless-concat">禁止没有必要的字符拼接 (no-useless-concat)</a>
>此规则目的在于标记可以组合成单个字面量的两个字面量的拼接。字面量可以是字符串或者模板字面量。
```javascript
'no-useless-concat': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
/*eslint no-useless-concat: "error"*/
/*eslint-env es6*/

// these are the same as "10"
var a = `some` + `string`;
var a = '1' + '0';
var a = '1' + `0`;
var a = `1` + '0';
var a = `1` + `0`;
```
##### 正确 代码示例：
```javascript
/*eslint no-useless-concat: "error"*/

// when a non string is included
var c = a + b;
var c = '1' + a;
var a = 1 + '1';
var c = 1 - 2;
// when the string concatenation is multiline
var c = "foo" +
    "bar";
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="no-useless-constructor">禁用不必要的构造函数 (no-useless-constructor)</a>
>该规则标记可以被安全移除但又不改变类的行为的构造函数。
```javascript
'no-useless-constructor': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
/*eslint no-useless-constructor: "error"*/
/*eslint-env es6*/

class A {
    constructor () {
    }
}

class A extends B {
    constructor (...args) {
      super(...args);
    }
}
```
##### 正确 代码示例：
```javascript
/*eslint no-useless-constructor: "error"*/

class A { }

class A {
    constructor () {
        doSomething();
    }
}

class A extends B {
    constructor() {
        super('foo');
    }
}

class A extends B {
    constructor() {
        super();
        doSomething();
    }
}
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="no-useless-escape">禁用不必要的转义 (no-useless-escape)</a>
>该规则标记在不改变代码行为的情况下可以安全移除的转义。
```javascript
'no-useless-escape': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
/*eslint no-useless-escape: "error"*/

"\'";
'\"';
"\#";
"\e";
`\"`;
`\"${foo}\"`;
`\#{foo}`;
/\!/;
/\@/;
```
##### 正确 代码示例：
```javascript
/*eslint no-useless-escape: "error"*/

"\"";
'\'';
"\x12";
"\u00a9";
"\371";
"xs\u2111";
`\``;
`\${${foo}\}`;
`$\{${foo}\}`;
/\\/g;
/\t/g;
/\w\$\*\^\./;
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="no-useless-rename">禁止将import， export和destructured assignments重命名为相同的名称（no-useless-rename）</a>
>此规则不允许将import， export和destructured assignments重命名为相同的名称。
```javascript
'no-useless-rename': [
  'warn',
  {
    ignoreDestructuring: false,
    ignoreImport: false,
    ignoreExport: false,
  },
]
```
- **等级 : "warn"**
- **选项 "ignoreDestructuring"**: 设置为时false，此规则检查解构分配（默认）
- **选项 "ignoreImport"**: 设置为此时false，此规则检查导入（默认）
- **选项 "ignoreExport"**: 设置为此时false，此规则检查导出（默认）
##### 默认情况下此规则的代码不正确的示例：
```javascript
/*eslint no-useless-rename: "error"*/

import { foo as foo } from "bar";
export { foo as foo };
export { foo as foo } from "bar";
let { foo: foo } = bar;
let { 'foo': foo } = bar;
function foo({ bar: bar }) {}
({ foo: foo }) => {}
```
##### 默认情况下此规则的正确代码示例：
```javascript
/*eslint no-useless-rename: "error"*/

import * as foo from "foo";
import { foo } from "bar";
import { foo as bar } from "baz";

export { foo };
export { foo as bar };
export { foo as bar } from "foo";

let { foo } = bar;
let { foo: bar } = baz;
let { [foo]: foo } = bar;

function foo({ bar }) {}
function foo({ bar: baz }) {}

({ foo }) => {}
({ foo: bar }) => {}
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="no-with">禁用 with 语句 (no-with)</a>
>此规则目的在于排除 with 语句。
 
>如果 ESLint 在严格模式下解析代码，解析器（不是该规则）将报告这样的错误。
```javascript
'no-with': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
/*eslint no-with: "error"*/

with (point) {
    r = Math.sqrt(x * x + y * y); // is r a member of point?
}
```
##### 正确 代码示例：
```javascript
/*eslint no-with: "error"*/
/*eslint-env es6*/

const r = ({x, y}) => Math.sqrt(x * x + y * y);
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="no-whitespace-before-property">禁止属性前有空白 (no-whitespace-before-property)</a>
命令行中的 --fix 选项可以自动修复一些该规则报告的问题。
>该规则禁止在点号周围或对象属性之前的左括号前出现空白。如果对象和属性不在同一行上，这种情况，该规则允许使用空白，因为对级联的属性增加新行是一种很普遍的行为。
```javascript
'no-whitespace-before-property': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
/*eslint no-whitespace-before-property: "error"*/

foo [bar]

foo. bar

foo .bar

foo. bar. baz

foo. bar()
  .baz()

foo
  .bar(). baz()
```
##### 正确 代码示例：
```javascript
/*eslint no-whitespace-before-property: "error"*/

foo.bar

foo[bar]

foo[ bar ]

foo.bar.baz

foo
  .bar().baz()

foo
  .bar()
  .baz()

foo.
  bar().
  baz()
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="radix">要求必须有基数 (radix)</a>
>该规则旨在防止出现不确定的字符串对数字的转换或防止在现代环境中出现多余的基数 10。
```javascript
'radix': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
/*eslint radix: "error"*/

var num = parseInt("071");

var num = parseInt(someValue);

var num = parseInt("071", "abc");

var num = parseInt();
```
##### 正确 代码示例：
```javascript
/*eslint radix: "error"*/

var num = parseInt("071", 10);

var num = parseInt("071", 8);

var num = parseFloat(someValue);
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="require-yield">禁用函数内没有yield的 generator 函数（require-yield）</a>
>如果 generator 函数内部没有yield关键字，该规则将发出警告。
```javascript
'radix': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
/*eslint require-yield: "error"*/
/*eslint-env es6*/

function* foo() {
  return 10;
}
```
##### 正确 代码示例：
```javascript
/*eslint require-yield: "error"*/
/*eslint-env es6*/

function* foo() {
  yield 5;
  return 10;
}

function foo() {
  return 10;
}

// This rule does not warn on empty generator functions.
function* foo() { }
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="rest-spread-spacing">强制限制扩展运算符及其表达式之间的空格（rest-spread-spacing）</a>
命令行中的 --fix 选项可以自动修复一些该规则报告的问题。
>这条规则的目的是强制限制扩展运算符及其表达式之间的空格。该规则还支持当前的对象在启用时扩展属性。
```javascript
'rest-spread-spacing': ['warn', 'never']
```
- **等级 : "warn"**
- **选项 "never"**: (默认)扩展运算符及其表达式之间不允许有空格。 
##### 此规则的错误代码示例"never"：
```javascript
/*eslint rest-spread-spacing: ["error", "never"]*/

fn(... args)
[... arr, 4, 5, 6]
let [a, b, ... arr] = [1, 2, 3, 4, 5];
function fn(... args) { console.log(args); }
let { x, y, ... z } = { x: 1, y: 2, a: 3, b: 4 };
let n = { x, y, ... z };
```
##### 此规则的正确代码示例"never"：
```javascript
/*eslint rest-spread-spacing: ["error", "never"]*/

fn(...args)
[...arr, 4, 5, 6]
let [a, b, ...arr] = [1, 2, 3, 4, 5];
function fn(...args) { console.log(args); }
let { x, y, ...z } = { x: 1, y: 2, a: 3, b: 4 };
let n = { x, y, ...z };
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="strict">要求或禁止使用严格模式指令 (strict)</a>
命令行中的 --fix 选项可以自动修复一些该规则报告的问题。
>该规则要求或禁止严格模式指令。
```javascript
strict: ['warn', 'never']
```
- **等级 : "warn"**
- **选项 "never"**: 禁用严格模式指令 
##### 选项 "never" 的 错误 代码示例：
```javascript
/*eslint strict: ["error", "never"]*/

"use strict";

function foo() {
}
/*eslint strict: ["error", "never"]*/

function foo() {
    "use strict";
}
```
##### 选项 "never" 的 正确 代码示例：
```javascript
/*eslint strict: ["error", "never"]*/

function foo() {
}
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="unicode-bom">要求或禁止使用 Unicode 字节顺序标记 (BOM) (unicode-bom)</a>
命令行中的 --fix 选项可以自动修复一些该规则报告的问题。
>如果使用了 "always" 选项，该规则要求文件始终以 Unicode BOM 字符 U+FEFF 开头。如果是 "never"，文件决不能以 U+FEFF 开始。
```javascript
'unicode-bom': ['warn', 'never']
```
- **等级 : "warn"**
- **选项 "never"**: (默认) 文件不能以 Unicode BOM 开头
##### 选项 "never" 的 错误 代码示例：
```javascript
/*eslint unicode-bom: ["error", "never"]*/

U+FEFF
var abc;
```
##### 选项 "never" 的 正确 代码示例：
```javascript
/*eslint unicode-bom: ["error", "never"]*/

var abc;
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="use-isnan">要求调用 isNaN()检查 NaN (use-isnan)</a>
>该规则禁止与 ‘NaN’ 的比较。
```javascript
'use-isnan': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
/*eslint use-isnan: "error"*/

if (foo == NaN) {
    // ...
}

if (foo != NaN) {
    // ...
}
```
##### 正确 代码示例：
```javascript
/*eslint use-isnan: "error"*/

if (isNaN(foo)) {
    // ...
}

if (!isNaN(foo)) {
    // ...
}
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="valid-typeof">强制 typeof 表达式与有效的字符串进行比较 (valid-typeof)</a>
>该规则强制 typeof 表达式与有效的字符串进行比较。
```javascript
'valid-typeof': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
/*eslint valid-typeof: "error"*/

typeof foo === "strnig"
typeof foo == "undefimed"
typeof bar != "nunber"
typeof bar !== "fucntion"
```
##### 正确 代码示例：
```javascript
/*eslint valid-typeof: "error"*/

typeof foo === "string"
typeof bar == "undefined"
typeof foo === baz
typeof bar === typeof qux
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="no-restricted-properties">禁止某些对象属性 (no-restricted-properties)</a>
>此规则查找访问给定对象名称上的给定属性键，无论是在读取属性的值还是将其作为函数调用时。您可以指定一个可选消息来指示替代API或限制原因。
```javascript
'no-restricted-properties': [
  'error',
  {
    object: 'System',
    property: 'import',
    message: 'Please use import() instead.',
  },
]
```
- **等级 : "error"**
- **选项 "object"**: 不允许的类名
- **选项 "property"**: 不允许的属性名
- **选项 "message"**: 提示信息

**[⬆ 回到顶部](#table-of-contents)**


## <a name="import/first">import/first</a>
>该规则报告任何在非导入语句之后的导入。
```javascript
'import/first': 'error'
```
- **等级 : "error"**
##### 错误 代码示例：
```javascript
import foo from './foo'

// some module-level initializer
initWith(foo)

import bar from './bar' // <- reported
```
##### 正确 代码示例：
```javascript
import foo from './foo'
import bar from './bar'

// some module-level initializer
initWith(foo)


```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="import/no-amd">import/no-amd</a>
>在模块范围的报告require([array], ...)和define([array], ...)函数调用。如果参数！= 2不会警告，或者第一个参数不是一个字符串数组。
```javascript
'import/no-amd': 'error'
```
- **等级 : "error"**
##### 错误 代码示例：
```javascript
define（[ “ a ”，“ b ” ]，函数（a，b）{ / * ... * / }）

require（[ “ b ”，“ c ” ]，函数（b，c）{ / * ... * / }）
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="import/no-webpack-loader-syntax">import/no-webpack-loader-syntax</a>
>禁止在导入中使用Webpack加载器语法
```javascript
'import/no-webpack-loader-syntax': 'error'
```
- **等级 : "error"**
##### 错误 代码示例：
```javascript
import myModule from 'my-loader!my-module';
import theme from 'style!css!./theme.css';

var myModule = require('my-loader!./my-module');
var theme = require('style!css!./theme.css');
```
##### 正确 代码示例：
```javascript
import myModule from 'my-module';
import theme from './theme.css';

var myModule = require('my-module');
var theme = require('./theme.css');
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="react/jsx-no-comment-textnodes">防止将注释作为文本节点插入(react/jsx-no-comment-textnodes)</a>
>这个规则防止注释字符串（例如，以//或开始/*）被意外注入为JSX语句中的文本节点。
```javascript
'react/jsx-no-comment-textnodes': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
var Hello = createReactClass({
  render: function() {
    return (
      <div>// empty div</div>
    );
  }
});

var Hello = createReactClass({
  render: function() {
    return (
      <div>
        /* empty div */
      </div>
    );
  }
});
```
##### 正确 代码示例：
```javascript
var Hello = createReactClass({
  displayName: 'Hello',
  render: function() {
    return <div>{/* empty div */}</div>;
  }
});

var Hello = createReactClass({
  displayName: 'Hello',
  render: function() {
    return <div /* empty div */></div>;
  }
});

var Hello = createReactClass({
  displayName: 'Hello',
  render: function() {
    return <div className={'foo' /* temp class */}</div>;
  }
});
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="react/jsx-no-duplicate-props">禁止JSX中的重复属性(react/jsx-no-duplicate-props)</a>
>使用重复的props创建JSX元素可能会导致应用程序出现意外的行为。
```javascript
'react/jsx-no-duplicate-props': ['warn', { ignoreCase: true }]
```
- **等级 : "warn"**
- **选项 "ignoreCase"**: 忽略大小写。默认为false。
##### 错误 代码示例：
```javascript
< Hello  name = “ John ”  name = “ John ” />;
```
##### 正确 代码示例：
```javascript
< Hello  firstname = “ John ”  lastname = “ Doe ” />;
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="react/jsx-no-target-blank">禁止使用不安全target='_blank'(react/jsx-no-target-blank)</a>
>禁止使用不安全target='_blank' (外链)
```javascript
'react/jsx-no-target-blank': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
var Hello = <a target='_blank' href="http://example.com/"></a>
```
##### 正确 代码示例：
```javascript
var Hello = <p target='_blank'></p>
var Hello = <a target='_blank' rel='noopener noreferrer' href="http://example.com"></a>
var Hello = <a target='_blank' href="relative/path/in/the/host"></a>
var Hello = <a target='_blank' href="/absolute/path/in/the/host"></a>
var Hello = <a></a>
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="react/jsx-no-undef">在JSX中禁止未声明的变量(react/jsx-no-undef)</a>
>在JSX中禁止未声明的变量
```javascript
'react/jsx-no-undef': 'error'
```
- **等级 : "error"**
##### 错误 代码示例：
```javascript
<Hello name="John" />;
// will ignore Text in the global scope and warn
var Hello = React.createClass({
  render: function() {
    return <Text>Hello</Text>;
  }
});
module.exports = Hello;
```
##### 正确 代码示例：
```javascript
var Hello = require('./Hello');

<Hello name="John" />;
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="react/jsx-pascal-case">为用户定义的JSX组件强制实施PascalCase(react/jsx-pascal-case)</a>
>强化用户定义的JSX组件在PascalCase中定义和引用的编码风格。

>请注意，由于React的JSX使用大小写约定来区分本地组件类和HTML标签，因此此规则不会警告以小写字母开头的组件。
```javascript
'react/jsx-pascal-case': [
  'warn',
  {
    allowAllCaps: true,
    ignore: [],
  },
]
```
- **等级 : "warn"**
- **选项 "allowAllCaps"**: 可选布尔值设置为true允许所有大写字母的组件名称（默认为false）。
- **选项 "ignore"**: 验证期间可忽略的组件名称的可选数组

**[⬆ 回到顶部](#table-of-contents)**


## <a name="react/jsx-uses-react">防止React被错误地标记为未使用(react/jsx-uses-react)</a>
>防止React被错误地标记为未使用
```javascript
'react/jsx-uses-react': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
var React = require('react');

// nothing to do with React
/** @jsx Foo */
var React = require('react');

var Hello = <div>Hello {this.props.name}</div>;
```
##### 正确 代码示例：
```javascript
var React = require('react');

var Hello = <div>Hello {this.props.name}</div>;
/** @jsx Foo */
var Foo = require('foo');

var Hello = <div>Hello {this.props.name}</div>;
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="react/jsx-uses-vars">防止在JSX中使用的变量被错误地标记为未使用（react/jsx-uses-vars）</a>
>防止在JSX中使用的变量被错误地标记为未使用
```javascript
'react/jsx-uses-vars': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
var Hello = require('./Hello');
```
##### 正确 代码示例：
```javascript
var Hello = require('./Hello');

<Hello name="John" />;
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="react/no-danger-with-children">禁止children和props.dangerouslySetInnerHTML同时使用的问题（react/no-danger-with-children）</a>
>此规则有助于阻止由于同时使用children和props.dangerouslySetInnerHTML而导致的问题。如果此规则被忽略，React将会发出警告。
```javascript
'react/no-danger-with-children': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
<div dangerouslySetInnerHTML={{ __html: "HTML" }}>
  Children
</div>

<Hello dangerouslySetInnerHTML={{ __html: "HTML" }}>
  Children
</Hello>
React.createElement("div", { dangerouslySetInnerHTML: { __html: "HTML" } }, "Children");

React.createElement("Hello", { dangerouslySetInnerHTML: { __html: "HTML" } }, "Children");
```
##### 正确 代码示例：
```javascript
<div dangerouslySetInnerHTML={{ __html: "HTML" }} />

<Hello dangerouslySetInnerHTML={{ __html: "HTML" }} />

<div>
  Children
</div>

<Hello>
  Children
</Hello>
React.createElement("div", { dangerouslySetInnerHTML: { __html: "HTML" } });

React.createElement("Hello", { dangerouslySetInnerHTML: { __html: "HTML" } });

React.createElement("div", {}, "Children");

React.createElement("Hello", {}, "Children");
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="react/no-deprecated">禁止使用已弃用的方法（react/no-deprecated）</a>
>React版本之间已经废弃了几种方法。如果您尝试使用不推荐使用的方法，此规则会警告您。使用共享设置指定React版本。
```javascript
'react/no-deprecated': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
React.render(<MyComponent />, root);

React.unmountComponentAtNode(root);

React.findDOMNode(this.refs.foo);

React.renderToString(<MyComponent />);

React.renderToStaticMarkup(<MyComponent />);

React.createClass({ /* Class object */ });

const propTypes = {
  foo: PropTypes.bar,
};

//Any factories under React.DOM
React.DOM.div();

import React, { PropTypes } from 'react';
```
##### 正确 代码示例：
```javascript
ReactDOM.render(<MyComponent />, root);

// When [1, {"react": "0.13.0"}]
ReactDOM.findDOMNode(this.refs.foo);

import { PropTypes } from 'prop-types';
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="react/no-direct-mutation-state">禁止this.state的直接变化（react/no-direct-mutation-state）</a>
>阻止this.state直接变化，因为setState()后来调用可能会取代你所做的变化。把this.state它看作是不可改变的。
 
>唯一可以分配this.state的地方是在ES6 class组件构造函数中。
```javascript
'react/no-direct-mutation-state': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
var Hello = createReactClass({
  componentDidMount: function() {
    this.state.name = this.props.name.toUpperCase();
  },
  render: function() {
    return <div>Hello {this.state.name}</div>;
  }
});

class Hello extends React.Component {
  constructor(props) {
    super(props)

    // Assign at instance creation time, not on a callback
    doSomethingAsync(() => {
      this.state = 'bad';
    });
  }
}
```
##### 正确 代码示例：
```javascript
var Hello = createReactClass({
  componentDidMount: function() {
    this.setState({
      name: this.props.name.toUpperCase();
    });
  },
  render: function() {
    return <div>Hello {this.state.name}</div>;
  }
});

class Hello extends React.Component {
  constructor(props) {
    super(props)

    this.state = {
      foo: 'bar',
    }
  }
}
```
**[⬆ 回到顶部](#table-of-contents)**



## <a name="react/no-is-mounted">禁止isMounted的使用（react/no-is-mounted）</a>
>isMounted是一种反模式，在使用ES6类时是不可用的，并且正在被官方弃用。
```javascript
'react/no-is-mounted': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
var Hello = createReactClass({
  handleClick: function() {
    setTimeout(function() {
      if (this.isMounted()) {
        return;
      }
    });
  },
  render: function() {
    return <div onClick={this.handleClick.bind(this)}>Hello</div>;
  }
});
```
##### 正确 代码示例：
```javascript
var Hello = createReactClass({
  render: function() {
    return <div onClick={this.props.handleClick}>Hello</div>;
  }
});
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="react/react-in-jsx-scope">禁止在JSX使用缺失的React（react/react-in-jsx-scope）</a>
>当使用JSX时，`<a />`扩展到React.createElement("a")。因此 React变量必须在范围内。
 如果您使用@jsx编译指示，则此规则将检查指定的变量而不是React一个。
```javascript
'react/react-in-jsx-scope': 'error'
```
- **等级 : "error"**
##### 错误 代码示例：
```javascript
var Hello = <div>Hello {this.props.name}</div>;
/** @jsx Foo.bar */
var React = require('react');

var Hello = <div>Hello {this.props.name}</div>;
```
##### 正确 代码示例：
```javascript
import React from 'react';

var Hello = <div>Hello {this.props.name}</div>;
var React = require('react');

var Hello = <div>Hello {this.props.name}</div>;
/** @jsx Foo.bar */
var Foo = require('foo');

var Hello = <div>Hello {this.props.name}</div>;
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="react/require-render-return">强制ES5或ES6类在渲染函数中返回值（react/require-render-return）</a>
>render在组件中编写方法时，很容易忘记返回JSX内容。如果return声明丢失，此规则将会发出警告。
```javascript
'react/require-render-return': 'error'
```
- **等级 : "error"**
##### 错误 代码示例：
```javascript
var Hello = createReactClass({
  render() {
    <div>Hello</div>;
  }
});

class Hello extends React.Component {
  render() {
    <div>Hello</div>;
  }
}
```
##### 正确 代码示例：
```javascript
var Hello = createReactClass({
  render() {
    return <div>Hello</div>;
  }
});

class Hello extends React.Component {
  render() {
    return <div>Hello</div>;
  }
}
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="react/style-prop-object">样式属性值强制作为对象（react/style-prop-object）</a>
>要求prop的值style是一个对象或是一个对象的变量。
```javascript
'react/style-prop-object': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
<div style="color: 'red'" />

<div style={true} />

<Hello style={true} />

const styles = true;
<div style={styles} />
React.createElement("div", { style: "color: 'red'" });

React.createElement("div", { style: true });

React.createElement("Hello", { style: true });

const styles = true;
React.createElement("div", { style: styles });
```
##### 正确 代码示例：
```javascript
<div style={{ color: "red" }} />

<Hello style={{ color: "red" }} />

const styles = { color: "red" };
<div style={styles} />
React.createElement("div", { style: { color: 'red' }});

React.createElement("Hello", { style: { color: 'red' }});

const styles = { height: '100px' };
React.createElement("div", { style: styles });
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="jsx-a11y/accessible-emoji">访问-表情符号（jsx-a11y/accessible-emoji）</a>
>表情符号已经成为向最终用户传达内容的常用方式。然而，对于使用屏幕阅读器的人来说，他/她可能根本不知道这个内容在那里。通过在屏幕阅读器中包装表情符号<span>，给予role="img"和提供有用的描述aria-label，屏幕阅读器将表情符号视为可访问树中的图像，并为最终用户提供可访问的名称。
```javascript
'jsx-a11y/accessible-emoji': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
<span role="img" aria-label="Snowman">&#9731;</span>
<span role="img" aria-label="Panda">🐼</span>
<span role="img" aria-labelledby="panda1">🐼</span> 
```
##### 正确 代码示例：
```javascript
<span>🐼</span>
<i role="img" aria-label="Panda">🐼</i>
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="jsx-a11y/alt-text">alt-文本（jsx-a11y/alt-text）</a>
>强制要求所有需要替代文本的元素都有有意义的信息传递给最终用户。这是屏幕阅读器用户可访问性的重要组成部分，以便他们了解内容在页面上的用途。默认情况下，此规则将检查以下内容替代文本：`<img>，<area>，<input type="image">，和<object>`。
```javascript
'jsx-a11y/alt-text': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
<img src="foo" />
<img {...props} />
<img {...props} alt /> // Has no value
<img {...props} alt={undefined} /> // Has no value
<img {...props} alt={`${undefined}`} /> // Has no value
<img src="foo" role="presentation" /> // Avoid ARIA if it can be achieved without
<img src="foo" role="none" /> // Avoid ARIA if it can be achieved without

<object {...props} />

<area {...props} />

<input type="image" {...props} />
```
##### 正确 代码示例：
```javascript
<img src="foo" alt="Foo eating a sandwich." />
<img src="foo" alt={"Foo eating a sandwich."} />
<img src="foo" alt={altText} />
<img src="foo" alt={`${person} smiling`} />
<img src="foo" alt="" />

<object aria-label="foo" />
<object aria-labelledby="id1" />
<object>Meaningful description</object>
<object title="An object" />

<area aria-label="foo" />
<area aria-labelledby="id1" />
<area alt="This is descriptive!" />

<input type="image" alt="This is descriptive!" />
<input type="image" aria-label="foo" />
<input type="image" aria-labelledby="id1" />
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="jsx-a11y/anchor-has-content">锚点-的-内容（jsx-a11y/anchor-has-content）</a>
>强制锚具有内容，屏幕阅读器可以访问内容。可访问性意味着它不会使用aria-hidden道具隐藏。
```javascript
'jsx-a11y/anchor-has-content': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
<a />
<a><TextWrapper aria-hidden /></a>
```
##### 正确 代码示例：
```javascript
<a>Anchor Content!</a>
<a><TextWrapper /><a>
<a dangerouslySetInnerHTML={{ __html: 'foo' }} />
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="jsx-a11y/aria-activedescendant-has-tabindex">aria-activedescendant-的TabIndex（jsx-a11y/aria-activedescendant-has-tabindex）</a>
>aria-activedescendant用于管理复合小部件中的焦点。具有该属性的元素aria-activedescendant保留活动文档焦点; 它通过将该元素的ID分配给值来指示它的哪个子元素具有次要焦点aria-activedescendant。这个模式用于构建一个像搜索类型的选择列表。搜索输入框保留文档焦点，以便用户可以键入输入。如果按下向下箭头键并突出显示搜索建议，则建议元素的ID将作为aria-activedescendant输入元素的值应用。
 
>由于一个元素aria-activedescendant必须是可放大的，它必须有一个固有tabIndex的零或者tabIndex用tabIndex 属性声明一个零。
```javascript
'jsx-a11y/aria-activedescendant-has-tabindex': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
<div aria-activedescendant={someID} />
<div aria-activedescendant={someID} tabIndex={-1} />
<div aria-activedescendant={someID} tabIndex="-1" />
<input aria-activedescendant={someID} tabIndex={-1} />
```
##### 正确 代码示例：
```javascript
<CustomComponent />
<CustomComponent aria-activedescendant={someID} />
<CustomComponent aria-activedescendant={someID} tabIndex={0} />
<CustomComponent aria-activedescendant={someID} tabIndex={-1} />
<div />
<input />
<div tabIndex={0} />
<div aria-activedescendant={someID} tabIndex={0} />
<div aria-activedescendant={someID} tabIndex="0" />
<div aria-activedescendant={someID} tabIndex={1} />
<input aria-activedescendant={someID} />
<input aria-activedescendant={someID} tabIndex={0} />
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="jsx-a11y/aria-props">元素不能使用无效的aria属性（jsx-a11y/aria-props）</a>
>元素不能使用无效的aria属性。如果找到WAI-ARIA状态和属性规范中aria-*没有列出的属性，将会失败。
```javascript
'jsx-a11y/aria-props': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
<!-- Bad: Labeled using incorrectly spelled aria-labeledby -->
<div id="address_label">Enter your address</div>
<input aria-labeledby="address_label">
```
##### 正确 代码示例：
```javascript
<!-- Good: Labeled using correctly spelled aria-labelledby -->
<div id="address_label">Enter your address</div>
<input aria-labelledby="address_label">
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="jsx-a11y/aria-proptypes">aria状态和属性值必须有效（jsx-a11y/aria-proptypes）</a>
>aria状态和属性值必须有效
```javascript
'jsx-a11y/aria-proptypes': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
<!-- Bad: the aria-hidden state is of type true/false -->
<span aria-hidden="yes">foo</span>
```
##### 正确 代码示例：
```javascript
<!-- Good: the aria-hidden state is of type true/false -->
<span aria-hidden="true">foo</span>
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="jsx-a11y/aria-role">元素必须使用有效的aria角色（jsx-a11y/aria-role）(#jsx-a11y/aria-props)</a>
>具有aria角色的元素必须使用有效的，非抽象的aria角色。
```javascript
'jsx-a11y/aria-role': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
<div role="datepicker"></div> <!-- Bad: "datepicker" is not an ARIA role -->
<div role="range"></div>      <!-- Bad: "range" is an _abstract_ ARIA role -->
<div role=""></div>           <!-- Bad: An empty ARIA role is not allowed -->
<Foo role={role}></Foo>       <!-- Bad: ignoreNonDOM is set to false or not set -->
```
##### 正确 代码示例：
```javascript
<div role="button"></div>     <!-- Good: "button" is a valid ARIA role -->
<div role={role}></div>       <!-- Good: role is a variable & cannot be determined until runtime. -->
<div></div>                   <!-- Good: No ARIA role -->
<Foo role={role}></Foo>       <!-- Good: ignoreNonDOM is set to true -->
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="jsx-a11y/aria-unsupported-elements">aria不受支持的元素（jsx-a11y/aria-unsupported-elements）</a>
>某些保留的DOM元素不支持aria角色，状态和属性。这往往是因为他们是不可见的，例如meta，html，script，style。此规则强制这些DOM元素不包含role和/或aria-* props。
```javascript
'jsx-a11y/aria-unsupported-elements': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
<!-- Bad: the meta element should not be given any ARIA attributes -->
<meta charset="UTF-8" aria-hidden="false" />
```
##### 正确 代码示例：
```javascript
<!-- Good: the meta element should not be given any ARIA attributes -->
<meta charset="UTF-8" />
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="jsx-a11y/heading-has-content">标题要有内容（jsx-a11y/heading-has-content）</a>
>强制执行标题元素（h1，h2等）为内容和内容的屏幕读取器访问。可访问性意味着它不会使用aria-hidden prop隐藏。
```javascript
'jsx-a11y/heading-has-content': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
<h1 />
<h1><TextWrapper aria-hidden />
```
##### 正确 代码示例：
```javascript
<h1>Heading Content!</h1>
<h1><TextWrapper /><h1>
<h1 dangerouslySetInnerHTML={{ __html: 'foo' }} />
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="jsx-a11y/href-no-hash">href必须是有效性的（jsx-a11y/href-no-hash）</a>
>`<a>`具有有效href属性的HTML 元素被正式定义为表示超链接。也就是说，一个HTML文档与另一个HTML文档之间的链接，或者HTML文档中的一个位置与同一文档内的另一个位置之间的链接。
```javascript
'jsx-a11y/href-no-hash': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
/*Anchors should be a button:*/
<a onClick={foo} />
<a href="#" onClick={foo} />
<a href={"#"} onClick={foo} />
<a href={`#`} onClick={foo} />
<a href="javascript:void(0)" onClick={foo} />
<a href={"javascript:void(0)"} onClick={foo} />
<a href={`javascript:void(0)`} onClick={foo} />

/*Missing href attribute:*/
<a />
<a href={undefined} />
<a href={null} />

/*Invalid href attribute:*/
<a href="#" />
<a href={"#"} />
<a href={`#`} />
<a href="javascript:void(0)" />
<a href={"javascript:void(0)"} />
<a href={`javascript:void(0)`} />
```
##### 正确 代码示例：
```javascript
<a href="https://github.com" />
<a href="#section" />
<a href="foo" />
<a href="/foo/bar" />
<a href={someValidPath} />
<a href="https://github.com" onClick={foo} />
<a href="#section" onClick={foo} />
<a href="foo" onClick={foo} />
<a href="/foo/bar" onClick={foo} />
<a href={someValidPath} onClick={foo} />
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="jsx-a11y/iframe-has-title">iframe的标题（jsx-a11y/iframe-has-title）</a>
>`<iframe>` 元素必须具有唯一的标题属性以向用户指示其内容。
```javascript
'jsx-a11y/iframe-has-title': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
<iframe />
<iframe {...props} />
<iframe title="" />
<iframe title={''} />
<iframe title={``} />
<iframe title={undefined} />
<iframe title={false} />
<iframe title={true} />
<iframe title={42} />
```
##### 正确 代码示例：
```javascript
<iframe title="This is a unique title" />
<iframe title={uniqueTitle} />
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="jsx-a11y/img-redundant-alt">img-多余的-alt（jsx-a11y/img-redundant-alt）</a>
>强制img alt属性不包含单词图像，图片或照片。屏幕阅读器已经将img元素宣布为图片。不需要使用图像，照片和/或图片等文字。
```javascript
'jsx-a11y/img-redundant-alt': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
<img src="foo" alt="Photo of foo being weird." />
<img src="bar" alt="Image of me at a bar!" />
<img src="baz" alt="Picture of baz fixing a bug." />
```
##### 正确 代码示例：
```javascript
<img src="foo" alt="Foo eating a sandwich." />
<img src="bar" aria-hidden alt="Picture of me taking a photo of an image" /> // Will pass because it is hidden.
<img src="baz" alt={`Baz taking a ${photo}`} /> // This is valid since photo is a variable name.
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="jsx-a11y/no-access-key">禁止access-key（jsx-a11y/no-access-key）</a>
>强制元素没有accessKey prop。访问键是允许Web开发人员将键盘快捷键分配给元素的HTML属性。屏幕阅读器和键盘所使用的键盘快捷键和键盘命令之间的不一致会造成无障碍复杂性，因此为避免复杂化，不应使用快捷键。
```javascript
'jsx-a11y/no-access-key': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
<div accessKey="h" />
```
##### 正确 代码示例：
```javascript
<div />
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="jsx-a11y/no-distracting-elements">禁用废弃的元素（jsx-a11y/no-distracting-elements）</a>
>这些元素很可能被弃用，应该避免。默认情况下，下列元素在视觉上分散注意力：`<marquee>和<blink>`。
```javascript
'jsx-a11y/no-distracting-elements': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
<marquee />
<blink />
```
##### 正确 代码示例：
```javascript
<div />
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="jsx-a11y/no-redundant-roles">禁用多余的roles（jsx-a11y/no-redundant-roles）</a>
>一些HTML元素具有由浏览器实现的本地语义。这包括默认/隐含的ARIA角色。设置匹配其默认/隐含角色的ARIA角色是多余的，因为它已经被浏览器设置。
```javascript
'jsx-a11y/no-redundant-roles': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
<button role="button" />
<img role="img" src="foo.jpg" />
```
##### 正确 代码示例：
```javascript
<div />
<button role="presentation" />
<MyComponent role="main" />
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="jsx-a11y/role-has-required-aria-props">role有要求的aria props（jsx-a11y/role-has-required-aria-props）</a>
>具有aria role的元素必须具有该角色的所有必需属性。
```javascript
'jsx-a11y/role-has-required-aria-props': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
<!-- Bad: the checkbox role requires the aria-checked state -->
<span role="checkbox" aria-labelledby="foo" tabindex="0"></span>
```
##### 正确 代码示例：
```javascript
<!-- Good: the checkbox role requires the aria-checked state -->
<span role="checkbox" aria-checked="false" aria-labelledby="foo" tabindex="0"></span>
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="jsx-a11y/role-supports-aria-props">role-支持的-aria-props（jsx-a11y/role-supports-aria-props）</a>
>强制定义显式或隐式角色的元素仅包含aria-*由其支持的属性role。许多ARIA属性（状态和属性）只能用于具有特定角色的元素。一些元素具有隐含的角色，例如`<a href="#" />`，将解析为role="link"。
```javascript
'jsx-a11y/role-supports-aria-props': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
<!-- Bad: the radio role does not support the aria-required property -->
<ul role="radiogroup" aria-labelledby="foo">
    <li aria-required tabIndex="-1" role="radio" aria-checked="false">Rainbow Trout</li>
    <li aria-required tabIndex="-1" role="radio" aria-checked="false">Brook Trout</li>
    <li aria-required tabIndex="0" role="radio" aria-checked="true">Lake Trout</li>
</ul>
```
##### 正确 代码示例：
```javascript
<!-- Good: the radiogroup role does support the aria-required property -->
<ul role="radiogroup" aria-required aria-labelledby="foo">
    <li tabIndex="-1" role="radio" aria-checked="false">Rainbow Trout</li>
    <li tabIndex="-1" role="radio" aria-checked="false">Brook Trout</li>
    <li tabIndex="0" role="radio" aria-checked="true">Lake Trout</li>
</ul>
```
**[⬆ 回到顶部](#table-of-contents)**


## <a name="jsx-a11y/scope">范围（jsx-a11y/scope）</a>
>scope的范围应该只在< th >元素上使用。
```javascript
'jsx-a11y/scope': 'warn'
```
- **等级 : "warn"**
##### 错误 代码示例：
```javascript
<div scope />
```
##### 正确 代码示例：
```javascript
<th scope="col" />
<th scope={scope} />
```
**[⬆ 回到顶部](#table-of-contents)**



