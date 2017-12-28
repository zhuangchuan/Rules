# **rules**

*代码规范*

## <a name="table-of-contents">目录</a>

  1. [分号 (semi)](#semi)
  1. [未使用过的变量 (no-unused-vars)](#no-unused-vars)
  1. [禁用 console (no-console)](#no-console)
  1. [强制数组方法的回调函数中有 return 语句 (array-callback-return)](#array-callback-return)
  1. [要求 Switch 语句中有 Default 分支 (default-case)](#default-case)
  1. [dot-location](#dot-location)
  1. [eqeqeq](#eqeqeq)
  1. [new-parens](#new-parens)
  1. [no-array-constructor](#no-array-constructor)
  1. [no-caller](#no-caller)
  1. [no-cond-assign](#no-cond-assign)
  1. [no-const-assign](#no-const-assign)
  1. [no-control-regex](#no-control-regex)
  1. [no-delete-var](#no-delete-var)
  1. [no-dupe-args](#no-dupe-args)
  1. [no-dupe-class-members](#no-dupe-class-members)
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
  
## 代码规范常见问题

### <a name="semi">要求或禁止使用分号代替 ASI (semi)</a>

命令行中的 --fix 选项可以自动修复一些该规则报告的问题。

  - **选项 "always"**: (默认) 要求在语句末尾使用分号

   `错误 代码示例：`
    
    
    /*eslint semi: ["error", "always"]*/
    
    var name = "ESLint"
    
    object.method = function() {
        // ...
    }
  `正确 代码示例：`
      
      
      /*eslint semi: "error"*/
      
      var name = "ESLint";
      
      object.method = function() {
          // ...
      };
  



### <a name="no-unused-vars">禁止未使用过的变量 (no-unused-vars)</a>


  - **选项 "args"**: none - 不检查参数
  - **选项 "ignoreRestSiblings"**: 选项是个布尔类型 (默认: false)。使用 Rest 属性 可能会“省略”对象中的属性，但是默认情况下，其兄弟属性被标记为 “unused”。使用该选项可以使 rest 属性的兄弟属性被忽略。
  




### <a name="no-console">禁用 console (no-console) (semi)</a>


  - **选项 "off"**: 禁止禁用



### <a name="array-callback-return">强制数组方法的回调函数中有 return 语句 (array-callback-return)</a>


  - **选项 "off"**: 禁止禁用

 ### <a name="default-case">要求 Switch 语句中有 Default 分支 (default-case)</a>
 
 
   - **选项 "commentPattern "**: 设置 commentPattern 为一个正则表达式字符串，来改变默认的 /^no default$/i 注释匹配模式
 
    `错误 代码示例：`
     
     
     /*eslint default-case: "error"*/
     
     switch (a) {
         case 1:
             /* code */
             break;
     }

   `正确 代码示例：`
       
       
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
   
 
  

**[⬆ 回到顶部](#table-of-contents)**
