# **rules**

*代码规范*

## <a name="table-of-contents">目录</a>

  1. [分号（semi）](#semi)
  1. [未使用过的变量（no-unused-vars）](#no-unused-vars)
  1. [no-console](#no-console)
  1. [array-callback-return](#array-callback-return)
  1. [default-case](#default-case)
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

## <a name="semi">semi 要求或禁止使用分号代替 ASI (semi)</a>

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
  

**[⬆ 回到顶部](#table-of-contents)**

