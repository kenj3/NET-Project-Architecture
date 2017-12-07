# JavaScript \ EMCAScript \ TypeScript 编码规范 (草稿)

#### [返回目录](README.md)

[1 引言](#1-引言)

[2 风格规范](#2-风格规范)

　　[2.1 命名](#2.1-命名)

　　[2.2 注释](#2.2-注释)

　　[2.3 格式](#2.3-格式)

[3 语言规范](#3-语言规范)

[4 代码检查](#4-代码检查)

[5 参考资料](#5-参考资料)

## 1 引言

### 1.1 说明

本文档以 `Airbnb JavaScript Style Guide` 为基础，编写符合自己团队的编码规范；
统一了**命名**和**注释**两大痛点，就统一了80%的风格，所以我们重点拓展这两部分内容，主体部分请参考基础。

### 1.2 基础

  - JavaScript [中文版](https://github.com/sivan/javascript-style-guide/tree/master/es5) | [English](https://github.com/airbnb/javascript)
  - ES5 [中文版](https://github.com/yuche/javascript) | [English](https://github.com/airbnb/javascript/tree/es5-deprecated/es5)
  - React [中文版](https://github.com/JasonBoy/javascript/tree/master/react) | [English](https://github.com/airbnb/javascript/tree/es5-deprecated/react)
  - [CSS-in-JavaScript](https://github.com/airbnb/javascript/tree/master/css-in-javascript)

## 2 风格规范

### 2.1 命名

  - 使用 `驼峰式(lowerCamelCase)` 命名变量和函数。
  
  ```javascript
  let thisIsMyObject = {};
  
  function thisIsMyFunction() {}
  ```

  - 使用 `帕斯卡式(UpperCamelCase)` 命名构造函数、类、枚举。
  
  ```javascript
  class User {
    name = 'xxx';
  }
  
  function User(options) {
    this.name = options.name;
  }
  
  const TargetState = {
    PENDING:1,
    SUCCESS:2,
    FAILURE:3
  };
  ```
    
  - 使用 `全部字母大写，单词间下划线分隔(CONSTANT_CASE)` 的命名方式命名常量和枚举的属性
  
  ```javascript
  const HTML_ENTITY = 1;
  
  const TargetState = {
    PENDING:1,
    SUCCESS:2,
    FAILURE:3
  };
  ```

  - 由多个单词组成的缩写词，在命名中，根据当前命名法和出现的位置，所有字母的大小写与首字母的大小写保持一致。
  
  ```javascript
  function XMLParser() {}
  
  function insertHTML(element, html) {}
  
  var httpRequest = new HTTPRequest();
  ```

  - 不要使用下划线前/后缀。

  > 解释：JavaScript 并没有私有属性或私有方法的概念。虽然使用下划线是表示「私有」的一种共识，但实际上这些属性是完全公开的，它本身就是你公共接口的一部分。这种习惯或许会导致开发者错误的认为改动它不会造成破坏或者不需要去测试。长话短说：如果你想要某处为「私有」，它必须不能是显式提出的。

  ```javascript
  // bad
  this.__firstName__ = 'Panda';
  this.firstName_ = 'Panda';
  this._firstName = 'Panda';
  
  // good
  this.firstName = 'Panda';
  ```

#### 常用命名
 
待完善

### 2.2 注释

#### 2.2.1 单行注释

必须独占一行。`//` 后跟一个空格，缩进与下一行被注释说明的代码一致。

#### 2.2.2 多行注释

避免使用 `/*...*/` 这样的多行注释。有多行注释内容时，使用多个单行注释。

> 解释：注释块（/* ... */）中不能有(/*或*/，JavaScript正则表达式中可能产生这种代码)，这样会产生语法错误，有多行注释内容时，使用多个单行注释。

#### 2.2.3 文件注释

参考[源码文件规范](file.md)

#### 2.2.4 文档化注释

JSDoc可以根据文档化注释，生成 JavaScript 应用程序或库、模块的API文档，现在很多编辑器或 IDE 中还可以通过 JSDoc 直接或使用插件生成智能提示。

详细规则请参考 [Use JSDoc](http://usejsdoc.org/) 和 [JSDoc Guide](http://www.css88.com/doc/jsdoc/index.html)；

#### 2.2.5 细节注释

对于内部实现、不容易理解的逻辑说明、摘要信息等，我们可能需要编写细节注释。
细节注释遵循单行注释的格式。说明必须换行时，每行是一个单行注释的起始。

```javascript
function foo(p1, p2, opt_p3) {
    // 这里对具体内部逻辑进行说明
    // 说明太长需要换行
    for (...) {
        ....
    }
}
```

#### 2.2.6 特殊注释

特殊注释标记，请注明标记人与标记时间。注意及时处理这些标记，通过标记扫，经常清理此类标记。线上故障有时候就是来源于这些标记处的代码。

给注释增加 `FIXME` 或 `TODO` 的前缀可以帮助其他开发者快速了解这是一个需要复查的问题，或是给需要实现的功能提供一个解决方式。这将有别于常见的注释，因为它们是可操作的。
使用 `FIXME -- need to figure this out` 或者 `TODO -- need to implement`。


- 使用 `// TODO: 问题的解决方式，标记人，标记时间，[预计处理时间]` 标注待办事宜，表示需要实现，但目前还未实现的功能。

```javascript
function Calculator() {

  // TODO: 此字段应当配置到参数中 asoiso 2017-06-15
  this.total = 0;

  return this;
}
```

- 使用 `// FIXME: 问题描述，标记人，标记时间，[预计处理时间]` 标记某代码是错误的，而且不能工作，需要及时纠正的情况。

```javascript
function Calculator() {

  // FIXME: 此处不应该使用全局变量 asoiso 2017-06-15
  total = 0;

  return this;
}
```

### 2.3 格式

- JavaScript 格式配置应用 WebStorm Code Style -> JavaScript -> Predefined Style -> JavaScript Standard Style 标准配置，拓展部分在下面补充。
  - indent 使用4个空格缩进
  - quotes 使用单引号
  - semi   使用分号
  - no-extra-semi 禁止多余的分号

- TypeScript 格式配置应用 WebStorm Code Style -> WebStorm Code Style -> Less 标准配置，拓展部分在下面补充。

## 3 语言规范

遵循主流风格指南。

## 4 代码检查

### 4.1 [ESLint](http://eslint.org/)

详细规则请参考 http://eslint.org/docs/rules/

### 4.2 [TSLint](https://palantir.github.io/tslint/)

详细规则请参考 https://palantir.github.io/tslint/rules/

## 5 参考资料

- https://github.com/airbnb/javascript
- https://google.github.io/styleguide/jsguide.html
- https://github.com/ecomfe/spec/blob/master/javascript-style-guide.md
- http://alloyteam.github.io/CodeGuide/
- https://github.com/aralejs/aralejs.github.io/issues/36
- http://usejsdoc.org/
- http://www.css88.com/doc/jsdoc/index.html
- https://github.com/aralejs/aralejs.github.io/issues/36
- https://github.com/aralejs/aralejs.github.io/wiki/JavaScript-注释规范

#### [返回目录](README.md)
#### [回到顶部](#)
