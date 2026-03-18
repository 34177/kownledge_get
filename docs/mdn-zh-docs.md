---
# Source: index.md
---
---
title: JavaScript
slug: Web/JavaScript
l10n:
  sourceCommit: 26e2f9883e0e73def04c0e86fec6da3ec42e66b3
---

**JavaScript**（**JS**）是一种具有{{Glossary("First-class Function", "函数优先")}}特性的轻量级、解释型或者说[即时编译型](https://zh.wikipedia.org/wiki/即時編譯)的编程语言。虽然作为 Web 页面中的脚本语言被人所熟知，但是它也被用到了很多[非浏览器环境](https://zh.wikipedia.org/wiki/JavaScript#其他)中，例如 {{Glossary("Node.js")}}、[Apache CouchDB](https://couchdb.apache.org)、[Adobe Acrobat](https://opensource.adobe.com/dc-acrobat-sdk-docs/acrobatsdk/) 等。进一步说，JavaScript 是一种[基于原型](/zh-CN/docs/Glossary/Prototype-based_programming)、多范式、[单线程](/zh-CN/docs/Glossary/Thread)的[动态](/zh-CN/docs/Glossary/Dynamic_typing)语言，并且支持面向对象、命令式和声明式（如函数式编程）风格。

JavaScript 的动态特性包括运行时对象的构造、变量参数列表、函数变量、动态脚本创建（通过 [`eval`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/eval)）、对象内枚举（通过 [`for...in`](/zh-CN/docs/Web/JavaScript/Reference/Statements/for...in) 和 [`Object` 工具方法](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Object#静态方法)）和源代码恢复（JavaScript 函数会存储其源代码文本，可以使用 [`toString()`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Function/toString) 进行检索）。

本部分文档将专注于 JavaScript 语言本身，而不是专注于 Web 页面或其他宿主环境特有的那部分。想要了解 Web 页面特有的 {{Glossary("API")}} 信息，请参考 [Web API](/zh-CN/docs/Web/API) 以及 {{Glossary("DOM")}}。

JavaScript 标准是 [ECMAScript 语言规范](https://tc39.es/ecma262/)（ECMA-262）和 [ECMAScript 国际化 API 规范](https://tc39.es/ecma402/)（ECMA-402）。只要某个浏览器实现了某个特性，我们就会尝试详细记录这个特性。这意味着，当某个 [ECMAScript 新特性的提案](https://github.com/tc39/proposals)在浏览器中实现时，文档和 MDN 文章中的示例可能会使用这些新特性。大多数时候发生在[阶段](https://tc39.es/process-document/) 3 和阶段 4 之间，通常在正式发布之前。

不要将 JavaScript 与 [Java 编程语言](https://zh.wikipedia.org/wiki/Java)弄混——**JavaScript _不是_“解释型的 Java”**。“Java”和“JavaScript”都是 Oracle 公司在美国和其他国家注册（或未注册）的商标。然而，这两门编程语言有着非常不同的语法、语义和用途。

JavaScript 核心语言特性（大部分是纯 [ECMAScript](/zh-CN/docs/Web/JavaScript/Reference/JavaScript_technologies_overview)）的文档包含以下内容：

- [JavaScript 指南](/zh-CN/docs/Web/JavaScript/Guide)
- [JavaScript 参考](/zh-CN/docs/Web/JavaScript/Reference)

有关 JavaScript 规范和相关技术的更多信息，请参阅 [JavaScript 技术概述](/zh-CN/docs/Web/JavaScript/Reference/JavaScript_technologies_overview)。

## 教程

借助指南和教程来学习如何用 JavaScript 编程。

### 面向纯新手

如果你想学习 JavaScript，却从未接触过 JavaScript 或编程，你可以投入到我们的 [JavaScript 主题学习区](/zh-CN/docs/Learn_web_development/Core/Scripting)。下面列出了这部分的所有章节：

- [JavaScript 第一步](/zh-CN/docs/Learn_web_development/Core/Scripting)
  - : 回答一些基本问题，比如“JavaScript 是什么？”、“它长什么样子？”、“它可以用来做什么？”等，还谈及如变量、字符串、数字、数组等 JavaScript 关键特性。
- [创建 JavaScript 代码块](/zh-CN/docs/Learn_web_development/Core/Scripting)
  - : 继续介绍 JavaScript 的关键基本特性，将注意力转向常见的代码块类型，如条件语句、循环、函数、事件等。
- [介绍 JavaScript 对象](/zh-CN/docs/Learn_web_development/Extensions/Advanced_JavaScript_objects)
  - : 如果你想进一步提高对语言的了解并编写出更高效的代码，理解 JavaScript 面向对象的本质很重要，因此我们为你准备了这个模块。
- [异步 JavaScript](/zh-CN/docs/Learn_web_development/Extensions/Async_JS)
  - : 探讨异步 JavaScript、为什么它很重要、如何使用它有效地处理潜在的阻塞操作（如从服务器获取资源）。
- [客户端 web API](/zh-CN/docs/Learn_web_development/Extensions/Client-side_APIs)
  - : 探讨 API 是什么、如何使用一些开发工作中最常见的 API。

### JavaScript 指南

- [JavaScript 指南](/zh-CN/docs/Web/JavaScript/Guide)
  - : 一份非常详细的 JavaScript 指南，适用于有过 JavaScript 或其他语言编程经验的读者。

### 中级

- [理解客户端 Javascript 框架](/zh-CN/docs/Learn_web_development/Core/Frameworks_libraries)
  - : JavaScript 框架是现代前端 Web 开发中不可或缺的一部分，它为开发者提供了构建可扩展、交互式 Web 应用的成熟工具。如今，许多企业已将框架作为标准开发工具链的一部分，因此越来越多的前端开发岗位都要求具备框架使用经验。本系列文章将提供一个轻松的入门指南，帮助你开始学习这些框架。
- [JavaScript 语言概述](/zh-CN/docs/Web/JavaScript/Guide/Language_overview)
  - : JavaScript 基础语法和语义概述：帮助来自其他编程语言的读者加速学习。
- [JavaScript 数据结构](/zh-CN/docs/Web/JavaScript/Guide/Data_structures)
  - : JavaScript 数据结构概述。
- [相等比较和相同](/zh-CN/docs/Web/JavaScript/Guide/Equality_comparisons_and_sameness)
  - : JavaScript 提供了三种不同的值比较运算：严格相等运算符 `===`、非严格相等运算符 `==`，以及 {{jsxref("Global_Objects/Object/is", "Object.is()")}} 方法。
- [属性的可枚举性和所有权](/zh-CN/docs/Web/JavaScript/Guide/Enumerability_and_ownership_of_properties)
  - : 不同的处理属性的可枚举性和所有权的方法——一个接着一个的访问一组对象属性。
- [闭包](/zh-CN/docs/Web/JavaScript/Guide/Closures)
  - : 闭包是由函数及其声明所在的词法环境结合而成。

### 高级

- [继承与原型链](/zh-CN/docs/Web/JavaScript/Guide/Inheritance_and_the_prototype_chain)
  - : 解释被广泛误解与低估的基于原型的继承。
- [内存管理](/zh-CN/docs/Web/JavaScript/Guide/Memory_management)
  - : JavaScript 的内存生命周期和垃圾回收。
- [事件循环](/zh-CN/docs/Web/JavaScript/Reference/Execution_model)
  - : JavaScript 拥有基于“事件循环”的运行时模型。

## 参考

浏览完整的 [JavaScript 参考](/zh-CN/docs/Web/JavaScript/Reference)文档。

- [标准对象](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects)
  - : 了解 {{jsxref("Array")}}、{{jsxref("Boolean")}}、{{jsxref("Date")}}、{{jsxref("Error")}}、{{jsxref("Function")}}、{{jsxref("JSON")}}、{{jsxref("Math")}}、{{jsxref("Number")}}、{{jsxref("Object")}}、{{jsxref("RegExp")}}、{{jsxref("String")}}、{{jsxref("Map")}}、{{jsxref("Set")}}、{{jsxref("WeakMap")}} 、{{jsxref("WeakSet")}} 等标准内置对象。
- [表达式和运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators)
  - : 学习运算符 {{jsxref("Operators/instanceof", "instanceof")}}、{{jsxref("Operators/typeof", "typeof")}}、{{jsxref("Operators/new", "new")}}、{{jsxref("Operators/this", "this")}}，[运算符优先级](/zh-CN/docs/Web/JavaScript/Reference/Operators/Operator_precedence)，以及其他运算符的行为。
- [语句和声明](/zh-CN/docs/Web/JavaScript/Reference/Statements)
  - : 学习 {{jsxref("Statements/do...while", "do-while")}}、{{jsxref("Statements/for...in", "for-in")}}、{{jsxref("Statements/for...of", "for-of")}}、{{jsxref("Statements/try...catch", "try-catch")}}、{{jsxref("Statements/let", "let")}}、{{jsxref("Statements/var", "var")}}、{{jsxref("Statements/const", "const")}}、{{jsxref("Statements/if...else", "if-else")}}、{{jsxref("Statements/switch", "switch")}} 以及其他语句和关键字的作用。
- [函数](/zh-CN/docs/Web/JavaScript/Reference/Functions)
  - : 学习如何使用 JavaScript 函数开发应用。
- [类](/zh-CN/docs/Web/JavaScript/Reference/Classes)
  - : JavaScript 类是最适合面向对象编程的方式。

---
# Source: index.md
---
---
title: 模板字符串
slug: Web/JavaScript/Reference/Template_literals
---

**模板字面量**是用反引号（`` ` ``）分隔的字面量，允许[多行字符串](#多行字符串)、带嵌入表达式的[字符串插值](#字符串插值)和一种叫[带标签的模板](#带标签的模板)的特殊结构。

模板字面量有时被非正式地叫作*模板字符串*，因为它们最常被用作[字符串插值](#字符串插值)（通过替换占位符来创建字符串）。然而，带标签的模板字面量可能不会产生字符串——它可以与自定义[标签函数](#带标签的模板)一起使用，来对模板字面量的不同部分执行任何操作。

## 语法

```js-nolint
`string text`

`string text line 1
 string text line 2`

`string text ${expression} string text`

tagFunction`string text ${expression} string text`
```

### 参数

- `string text`
  - : 将成为模板字面量的一部分的字符串文本。几乎允许所有字符，包括[换行符](/zh-CN/docs/Web/JavaScript/Reference/Lexical_grammar#行终止符)和其他[空白字符](/zh-CN/docs/Web/JavaScript/Reference/Lexical_grammar#空白符)。但是，除非使用了[标签函数](#带标签的模版字面量及转义序列)，否则无效的转义序列将导致语法错误。
- `expression`
  - : 要插入当前位置的表达式，其值被转换为字符串或传递给 `tagFunction`。
- `tagFunction`
  - : 如果指定，将使用模板字符串数组和替换表达式调用它，返回值将成为模板字面量的值。见[带标签的模板](#带标签的模板)。

## 描述

模板字面量用反引号（`` ` ``）括起来，而不是双引号（`"`）或单引号（`'`）。
除了普通字符串外，模板字面量还可以包含*占位符*——一种由美元符号和大括号分隔的嵌入式表达式：`${expression}`。字符串和占位符被传递给一个函数（要么是默认函数，要么是自定义函数）。默认函数（当未提供自定义函数时）只执行[字符串插值](#字符串插值)来替换占位符，然后将这些部分拼接到一个字符串中。

若要提供自定义函数，需在模板字面量之前加上函数名（结果被称为[**带标签的模板**](#带标签的模板)）。此时，模板字面量被传递给你的标签函数，然后就可以在那里对模板文本的不同部分执行任何操作。

若要转义模板字面量中的反引号（`` ` ``），需在反引号之前加一个反斜杠（`\`）。

```js
`\`` === "`"; // true
```

美元符号 `$` 也可以被转义，来阻止插值。

```js
`\${1}` === "${1}"; // true
```

### 多行字符串

在源码中插入的任何换行符都是模板字面量的一部分。

使用普通字符串，可以通过下面的方式得到多行字符串：

```js
console.log("string text line 1\n" + "string text line 2");
// "string text line 1
// string text line 2"
```

使用模板字面量，下面的代码同样可以做到：

```js
console.log(`string text line 1
string text line 2`);
// "string text line 1
// string text line 2"
```

### 字符串插值

如果没有模板字面量，当你想组合表达式的输出与字符串时，可以使用[加法运算符 `+`](/zh-CN/docs/Web/JavaScript/Reference/Operators/Addition) [连接它们](/zh-CN/docs/Learn_web_development/Core/Scripting/Strings#连接字符串)：

```js
const a = 5;
const b = 10;
console.log("Fifteen is " + (a + b) + " and\nnot " + (2 * a + b) + ".");
// "Fifteen is 15 and
// not 20."
```

这可能很难阅读，尤其是当存在多个表达式时。

有了模板字面量，就可以通过使用占位符 `${expression}` 嵌入待替换的表达式，从而避免串联运算符，并提高代码的可读性：

```js
const a = 5;
const b = 10;
console.log(`Fifteen is ${a + b} and
not ${2 * a + b}.`);
// "Fifteen is 15 and
// not 20."
```

注意，这两种语法有一点小区别：模板字面量直接将其表达式[强制转换为字符串](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/String#字符串强制转换)，而加法则会先强制转换为原语类型。更多相关信息，参见[加法（`+`）运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Addition)。

### 嵌套模板

在某些情况下，嵌套模板是具有可配置字符串的最简单的（也许还是更可读的）方法。在反引号分隔的模板中，允许在占位符 `${expression}` 中使用内层的反引号。

例如，不用模板字面量的情况下，如果你想根据特定条件返回某个值，可以执行以下操作：

```js example-bad
let classes = "header";
classes += isLargeScreen()
  ? ""
  : item.isCollapsed
    ? " icon-expander"
    : " icon-collapser";
```

用模板字面量但不嵌套时，你可以这么做：

```js example-bad
const classes = `header ${
  isLargeScreen() ? "" : item.isCollapsed ? "icon-expander" : "icon-collapser"
}`;
```

用嵌套模板字面量时，你可以这么做：

```js example-good
const classes = `header ${
  isLargeScreen() ? "" : `icon-${item.isCollapsed ? "expander" : "collapser"}`
}`;
```

### 带标签的模板

*带标签的*模板是模板字面量的一种更高级的形式，它允许你使用函数解析模板字面量。标签函数的第一个参数包含一个字符串数组，其余的参数与表达式相关。你可以用标签函数对这些参数执行任何操作，并返回被操作过的字符串（或者，也可返回完全不同的内容，见下面的示例）。用作标签的函数名没有限制。

```js
const person = "Mike";
const age = 28;

function myTag(strings, personExp, ageExp) {
  const str0 = strings[0]; // "That "
  const str1 = strings[1]; // " is a "
  const str2 = strings[2]; // "."

  const ageStr = ageExp > 99 ? "centenarian" : "youngster";

  // 我们甚至可以返回使用模板字面量构建的字符串
  return `${str0}${personExp}${str1}${ageStr}${str2}`;
}

const output = myTag`That ${person} is a ${age}.`;

console.log(output);
// That Mike is a youngster.
```

标签不必是普通的标识符，你可以使用任何[优先级](/zh-CN/docs/Web/JavaScript/Reference/Operators/Operator_precedence#%e6%b1%87%e6%80%bb%e8%a1%a8)大于 16 的表达式，包括[属性访问](/zh-CN/docs/Web/JavaScript/Reference/Operators/Property_accessors)、函数调用、[new 表达式](/zh-CN/docs/Web/JavaScript/Reference/Operators/new)，甚至其他带标签的模板字面量。

```js
console.log`Hello`; // [ 'Hello' ]
console.log.bind(1, 2)`Hello`; // 2 [ 'Hello' ]
new Function("console.log(arguments)")`Hello`; // [Arguments] { '0': [ 'Hello' ] }

function recursive(strings, ...values) {
  console.log(strings, values);
  return recursive;
}
recursive`Hello``World`;
// [ 'Hello' ] []
// [ 'World' ] []
```

虽然语法从技术上允许这么做，但*不带标签的*模板字面量是字符串，并且在链式调用时会抛出 {{jsxref("TypeError")}}。

```js
console.log(`Hello``World`); // TypeError: "Hello" is not a function
```

唯一的例外是可选链，这将抛出语法错误。

```js example-bad
console.log?.`Hello`; // SyntaxError: Invalid tagged template on optional chain
console?.log`Hello`; // SyntaxError: Invalid tagged template on optional chain
```

请注意，这两个表达式仍然是可解析的。这意味着它们将不受[自动分号补全](/zh-CN/docs/Web/JavaScript/Reference/Lexical_grammar#自动分号补全)的影响，其只会插入分号来修复无法解析的代码。

```js example-bad
// 仍是语法错误
const a = console?.log
`Hello`
```

标签函数甚至不需要返回字符串！

```js
function template(strings, ...keys) {
  return (...values) => {
    const dict = values[values.length - 1] || {};
    const result = [strings[0]];
    keys.forEach((key, i) => {
      const value = Number.isInteger(key) ? values[key] : dict[key];
      result.push(value, strings[i + 1]);
    });
    return result.join("");
  };
}

const t1Closure = template`${0}${1}${0}!`;
// const t1Closure = template(["","","","!"],0,1,0);
t1Closure("Y", "A"); // "YAY!"

const t2Closure = template`${0} ${"foo"}!`;
// const t2Closure = template([""," ","!"],0,"foo");
t2Closure("Hello", { foo: "World" }); // "Hello World!"

const t3Closure = template`I'm ${"name"}. I'm almost ${"age"} years old.`;
// const t3Closure = template(["I'm ", ". I'm almost ", " years old."], "name", "age");
t3Closure("foo", { name: "MDN", age: 30 }); // "I'm MDN. I'm almost 30 years old."
t3Closure({ name: "MDN", age: 30 }); // "I'm MDN. I'm almost 30 years old."
```

标签函数接收到的第一个参数是一个字符串数组。对于任何模板字面量，其长度等于替换次数（`${…}` 出现次数）加一，因此总是非空的。对于任何特定的带标签的模板字面量表达式，无论对字面量求值多少次，都将始终使用完全相同的字面量数组调用标签函数。

```js
const callHistory = [];

function tag(strings, ...values) {
  callHistory.push(strings);
  // Return a freshly made object
  return {};
}

function evaluateLiteral() {
  return tag`Hello, ${"world"}!`;
}

console.log(evaluateLiteral() === evaluateLiteral()); // false; each time `tag` is called, it returns a new object
console.log(callHistory[0] === callHistory[1]); // true; all evaluations of the same tagged literal would pass in the same strings array
```

这允许标签函数以其第一个参数作为标识来缓存结果。为了进一步确保数组值不变，第一个参数及其 [`raw` 属性](#原始字符串)都会被[冻结](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Object/isFrozen)，因此你将无法改变它们。

### 原始字符串

在标签函数的第一个参数中，存在一个特殊的属性 `raw` ，我们可以通过它来访问模板字符串的原始字符串，而无需[转义特殊字符](/zh-CN/docs/Web/JavaScript/Guide/Grammar_and_types#在字符串中使用的特殊字符)。

```js
function tag(strings) {
  console.log(strings.raw[0]);
}

tag`string text line 1 \n string text line 2`;
// logs "string text line 1 \n string text line 2" ,
// including the two characters '\' and 'n'
```

另外，使用 {{jsxref("String.raw()")}} 方法创建原始字符串和使用默认模板函数和字符串连接创建是一样的。

```js
let str = String.raw`Hi\n${2+3}!`;
// "Hi\\n5!"

str.length;.
// 6

str.split('').join(',');.
// "H,i,\\,n,5,!"
```

如果字面量不包含任何转义序列，`String.raw` 函数就像一个“identity”标签。如果你想要一个始终像不带标签的字面量那样的实际标识标签，可以用自定义函数，将“cooked”（例如，经转义序列处理过的）字面量数组传递给 `String.raw`，将它们当成原始字符串。

```js
const identity = (strings, ...values) =>
  String.raw({ raw: strings }, ...values);
console.log(identity`Hi\n${2 + 3}!`);
// Hi
// 5!
```

这对于许多工具来说很有用，它们要对以特定名称为标签的字面量作特殊处理。

```js
const html = (strings, ...values) => String.raw({ raw: strings }, ...values);
// 一些格式化程序会将此字面量的内容格式化为 HTML
const doc = html`<!doctype html>
  <html lang="en-US">
    <head>
      <title>Hello</title>
    </head>
    <body>
      <h1>Hello world!</h1>
    </body>
  </html>`;
```

### 带标签的模板字面量及转义序列

在普通模板字面量中，字符串字面量中的转义序列都是允许的，任何其他格式不正确的转义序列都是语法错误，包括：

- `\` 后跟 `0` 以外的任何十进制数字，或 `\0` 后跟一个十进制数字，例如 `\9` 和 `\07`（这是一种[已弃用的语法](/zh-CN/docs/Web/JavaScript/Reference/Deprecated_and_obsolete_features#转义序列)）
- `\x` 后跟两位以下十六进制数字，例如`\xz`
- `\u` 后不跟 `{`，并且后跟四个以下十六进制数字，例如 `\uz`
- `\u{}` 包含无效的 Unicode 码点——包含一个非十六进制数字，或者它的值大于 10FFFF，例如 `\u{110000}` 和 `\u{z}`

> [!NOTE]
> `\` 后面跟着其他字符，虽然它们可能没有用，因为没有转义，但它们不是语法错误。

然而，这对于带标签的模板来说是有问题的，除了“cooked”字面量外，这些模板还可以访问原始字面量（转义序列按原样保留）。带标签的模板应该允许嵌入语言（例如 [DSL](https://zh.wikipedia.org/wiki/领域特定语言) 或 [LaTeX](https://zh.wikipedia.org/wiki/LaTeX)），在这些语言里其他转义序列是常见的。因此，从带标签的模板中删除了转义序列诸多格式的语法限制。

不过，非法转义序列在“cooked”当中仍然会体现出来。它们将以 {{jsxref("undefined")}} 元素的形式存在于“cooked”数组之中：

```js
function latex(str) {
  return { cooked: str[0], raw: str.raw[0] };
}

latex`\unicode`;

// { cooked: undefined, raw: "\\unicode" }
```

值得注意的是，这一转义序列限制只对带标签的模板字面量移除，而不包括不带标签的模板字面量：

```js example-bad
const bad = `bad escape sequence: \unicode`;
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- {{jsxref("String")}}
- {{jsxref("String.raw()")}}
- [词法语法](/zh-CN/docs/Web/JavaScript/Reference/Lexical_grammar)
- [ES3 中的类模板字符串](https://gist.github.com/WebReflection/8f227532143e63649804)
- [hacks.mozilla.org 上的《深度学习 ES6 之模板字面量》](https://hacks.mozilla.org/2015/05/es6-in-depth-template-strings-2/)

---
# Source: index.md
---
---
title: 逻辑或赋值（||=）
slug: Web/JavaScript/Reference/Operators/Logical_OR_assignment
---

逻辑或赋值（`x ||= y`）运算仅在 `x` 为{{Glossary("falsy", "假")}}值时为其赋值。

{{InteractiveExample("JavaScript Demo: Expressions - Logical OR assignment")}}

```js interactive-example
const a = { duration: 50, title: "" };

a.duration ||= 10;
console.log(a.duration);
// Expected output: 50

a.title ||= "title is empty.";
console.log(a.title);
// Expected output: "title is empty."
```

## 语法

```js-nolint
expr1 ||= expr2
```

## 描述

逻辑或的[_短路运算_](/zh-CN/docs/Web/JavaScript/Reference/Operators/Operator_precedence#短路运算)意味着 `x ||= y` 与下式等价：

```js
x || (x = y);
```

如果左操作数不为假值，则由于[逻辑或](/zh-CN/docs/Web/JavaScript/Reference/Operators/Logical_OR)运算符的短路运算，不进行赋值操作。例如，由于 `x` 为 `const`（常量），以下式子不会抛出错误：

```js
const x = 1;
x ||= 2;
```

也不会触发 setter 函数：

```js
const x = {
  get value() {
    return 1;
  },
  set value(v) {
    console.log("调用了 setter");
  },
};

x.value ||= 2;
```

实际上，如果 `x` 为真值，则根本不会对 `y` 求值。

```js
const x = 1;
x ||= console.log("y 进行了求值");
// 什么都不会输出
```

## 示例

### 设定默认内容

当“lyrics”元素为空时，则显示默认值：

```js
document.getElementById("lyrics").textContent ||= "没有歌词。";
```

在这里，短路运算特别有用，因为元素不会产生不必要的更新，也不会引起诸如额外的解析、渲染、失去焦点等副作用。

注意：请注意检查 API 返回的值。如果返回的是空字符串（是{{Glossary("falsy", "假")}}值），则必须使用 `||=`，以显示“没有歌词。”而不是空内容。然而，如果接口返回 [`null`](/zh-CN/docs/Web/JavaScript/Reference/Operators/null) 或 {{jsxref("undefined")}}，则应该使用 [`??=`](/zh-CN/docs/Web/JavaScript/Reference/Operators/Nullish_coalescing_assignment)（空值合并赋值）运算符代替空白内容。

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- [逻辑或（||）](/zh-CN/docs/Web/JavaScript/Reference/Operators/Logical_OR)
- [空值合并运算符（`??`）](/zh-CN/docs/Web/JavaScript/Reference/Operators/Nullish_coalescing)
- [按位或赋值（`|=`）](/zh-CN/docs/Web/JavaScript/Reference/Operators/Bitwise_OR_assignment)
- {{Glossary("Truthy","真值")}}
- {{Glossary("Falsy","假值")}}

---
# Source: index.md
---
---
title: 函数表达式
slug: Web/JavaScript/Reference/Operators/function
---

**`function`** 关键字可以用来在一个表达式中定义一个函数。

你也可以使用 [`Function`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Function) 构造函数和一个[函数声明](/zh-CN/docs/Web/JavaScript/Reference/Statements/function)来定义函数。

## 语法

```plain
let function_expression = function [name]([param1[, param2[, ..., paramN]]]) {
   statements
};
```

从 [ES2015](/zh-CN/docs/Web)开始，你也可以使用[箭头函数](/zh-CN/docs/Web/JavaScript/Reference/Functions/Arrow_functions) 。

### 参数

- `name`
  - : 函数名称。可被省略，此种情况下的函数是匿名函数（_anonymous_）。函数名称只是函数体中的一个本地变量。
- `paramN`
  - : 被传递给函数的一个参数名称。一个函数至多拥有 255 个参数。
- `statements`
  - : 构成函数体的语句。

## 描述

函数表达式（function expression）非常类似于函数声明（function statement）（详情查看[函数声明](/zh-CN/docs/Web/JavaScript/Reference/Statements/function)），并且两者拥有几乎相同的语法。函数表达式与函数声明的最主要区别是函数名称（_function name_），在函数表达式中可省略它，从而创建匿名函数（_anonymous_ functions）。一个函数表达式可以被用作一个 IIFE（Immediately Invoked Function Expression，即时调用的函数表达式），它一旦定义就运行。更多信息请查看[函数](/zh-CN/docs/Web/JavaScript/Reference/Functions)。

### 函数表达式提升 (Function expression hoisting)

JavaScript 中的函数表达式没有提升，不像函数声明，你在定义函数表达式之前不能使用函数表达式：

```js
notHoisted(); // TypeError: notHoisted is not a function

var notHoisted = function () {
  console.log("bar");
};
```

### 具名函数表达式

如果你想在函数体内部引用当前函数，则需要创建一个具名函数表达式。**然后函数名称将会（且只会）作为函数体（作用域内）的本地变量**。这样也可以避免使用非标准的 [arguments.callee](/zh-CN/docs/Web/JavaScript/Reference/Functions/arguments/callee) 属性。

```js
var math = {
  factorial: function factorial(n) {
    if (n <= 1) return 1;
    return n * factorial(n - 1);
  },
};
```

被函数表达式赋值的那个变量会有一个 name 属性，如果你把这个变量赋值给另一个变量的话，这个 name 属性的值也不会改变。如果函数是一个匿名函数，那 name 属性的值就是被赋值的变量的名称（隐藏值）。如果函数不是匿名的话，那 name 属性的值就是这个函数的名称（显性值）。这对于[箭头函数](/zh-CN/docs/Web/JavaScript/Reference/Functions/Arrow_functions)也同样适用（箭头函数没有名字，所以你只能赋予 name 属性一个隐性名）。

```js
var foo = function () {};
foo.name; // "foo"

var foo2 = foo;
foo2.name; // "foo"

var bar = function baz() {};
bar.name; // "baz"

console.log(foo === foo2); //true
console.log(typeof baz); // undefined
console.log(bar === baz); // false (errors because baz == undefined)
```

## 示例

下面的例子定义了一个匿名函数并把它赋值给变量 x。这个函数返回它参数的平方：

```js
var x = function (y) {
  return y * y;
};
```

更多情况下被当作[回调函数](/zh-CN/docs/Mozilla/js-ctypes/Using_js-ctypes/Declaring_and_Using_Callbacks)使用：

```js
button.addEventListener("click", function (event) {
  console.log("button is clicked!");
});
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- {{jsxref("Functions/Arrow_functions", "箭头函数", "", 1)}}
- {{jsxref("Functions", "函数", "", 1)}}
- {{jsxref("Function")}}
- {{jsxref("Statements/function", "function 语句", "", 1)}}

---
# Source: index.md
---
---
title: 小于等于（<=）
slug: Web/JavaScript/Reference/Operators/Less_than_or_equal
---

小于等于运算符（`<=`）在左操作数小于等于右操作数时返回 `true`，否则返回 `false`。

{{InteractiveExample("JavaScript Demo: Expressions - Less than or equal operator")}}

```js interactive-example
console.log(5 <= 3);
// Expected output: false

console.log(3 <= 3);
// Expected output: true

// Compare bigint to number
console.log(3n <= 5);
// Expected output: true

console.log("aa" <= "ab");
// Expected output: true
```

## 语法

```js-nolint
x <= y
```

## 描述

操作数比较使用与[小于](/zh-CN/docs/Web/JavaScript/Reference/Operators/Less_than)运算符相同的算法，除了相等的值（在尝试转换后）会返回 `true`。

## 示例

### 字符串与字符串比较

```js
console.log("a" <= "b"); // true
console.log("a" <= "a"); // true
console.log("a" <= "3"); // false
```

### 字符串与数值比较

```js
console.log("5" <= 3); // false
console.log("3" <= 3); // true
console.log("3" <= 5); // true

console.log("hello" <= 5); // false
console.log(5 <= "hello"); // false
```

### 数值与数值比较

```js
console.log(5 <= 3); // false
console.log(3 <= 3); // true
console.log(3 <= 5); // true
```

### 数值与大整型比较

```js
console.log(5n <= 3); // false
console.log(3 <= 3n); // true
console.log(3 <= 5n); // true
```

### 比较 Boolean、null、undefined 和 NaN

```js
console.log(true <= false); // false
console.log(true <= true); // true
console.log(false <= true); // true

console.log(true <= 0); // false
console.log(true <= 1); // true

console.log(null <= 0); // true
console.log(1 <= null); // false

console.log(undefined <= 3); // false
console.log(3 <= undefined); // false

console.log(3 <= NaN); // false
console.log(NaN <= 3); // false
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- [大于运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Greater_than)
- [大于等于运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Greater_than_or_equal)
- [小于运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Less_than)

---
# Source: index.md
---
---
title: 逻辑空赋值（??=）
slug: Web/JavaScript/Reference/Operators/Nullish_coalescing_assignment
---

逻辑空赋值运算符（`x ??= y`）仅在 `x` 是{{Glossary("nullish", "空值")}}（`null` 或 `undefined`）时对其赋值。

{{InteractiveExample("JavaScript Demo: Expressions - Nullish coalescing assignment")}}

```js interactive-example
const a = { duration: 50 };

a.speed ??= 25;
console.log(a.speed);
// Expected output: 25

a.duration ??= 10;
console.log(a.duration);
// Expected output: 50
```

## 语法

```js-nolint
expr1 ??= expr2
```

## 描述

### 短路评估

[空值合并](/zh-CN/docs/Web/JavaScript/Reference/Operators/Nullish_coalescing)运算符从左至右求值，其使用以下规则测试是否可能进行语法短路求值：

`(结果非 null 或 undefined 的表达式) ?? expr` 被短路求值为左侧表达式，当左侧证明为既非 `null` 也非 `undefined`.

语法短路意味着 `expr` 部分**尚未被求值**，因此任何与其求值产生的相关副作用都不会生效（例如，如果 `expr` 是一个函数调用，则该调用将不会发生）。

逻辑空赋值的语法短路也意味着 `x ??= y` 等价于：

```js
x ?? (x = y);
```

而不等价于如下的表达式，因为其一定会发生赋值：

```js example-bad
x = x ?? y;
```

## 示例

### 使用逻辑空赋值

```js
function config(options) {
  options.duration ??= 100;
  options.speed ??= 25;
  return options;
}

config({ duration: 125 }); // { duration: 125, speed: 25 }
config({}); // { duration: 100, speed: 25 }
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- [空值合并运算符（`??`）](/zh-CN/docs/Web/JavaScript/Reference/Operators/Nullish_coalescing)
- {{Glossary("Nullish", "空值")}}
- {{Glossary("Truthy", "真值")}}
- {{Glossary("Falsy", "假值")}}

---
# Source: index.md
---
---
title: new.target
slug: Web/JavaScript/Reference/Operators/new.target
l10n:
  sourceCommit: 8cb0caef8175e1772f13ef7bc761f9616e2c5a4b
---

**`new.target`** 元属性允许你检测函数或构造函数是否是通过 [`new`](/zh-CN/docs/Web/JavaScript/Reference/Operators/new) 运算符被调用的。在通过 [`new`](/zh-CN/docs/Web/JavaScript/Reference/Operators/new) 运算符执行的函数或构造函数中，`new.target` 返回一个指向 `new` 调用的构造函数或函数的引用。在普通的函数调用中，`new.target` 的值是 {{jsxref("undefined")}}。

{{InteractiveExample("JavaScript Demo: Expressions - new.target")}}

```js interactive-example
function Foo() {
  if (!new.target) {
    throw new TypeError("calling Foo constructor without new is invalid");
  }
}

try {
  Foo();
} catch (e) {
  console.log(e);
  // Expected output: TypeError: calling Foo constructor without new is invalid
}
```

## 语法

```js-nolint
new.target
```

### 值

`new.target` 保证是一个可构造的函数值或 `undefined`。

- 在类构造函数中，它指向 `new` 调用的类，这可能是当前构造函数的子类，因为子类通过 [`super()`](/zh-CN/docs/Web/JavaScript/Reference/Operators/super) 传递调用了父类的构造函数。
- 在普通函数中，如果函数是直接通过 [`new`](/zh-CN/docs/Web/JavaScript/Reference/Operators/new) 构造的，则 `new.target` 指向函数本身。如果函数不是通过 `new` 调用的，则 `new.target` 是 {{jsxref("undefined")}}。函数可以被用作 [`extends`](/zh-CN/docs/Web/JavaScript/Reference/Classes/extends) 的基类，这种情况下 `new.target` 可能指向子类。
- 如果构造函数（类或者函数）是通过 [`Reflect.construct()`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Reflect/construct) 调用的，那么 `new.target` 指向作为 `newTarget` 传递的值（默认为 `target`）。
- 在[箭头函数](/zh-CN/docs/Web/JavaScript/Reference/Functions/Arrow_functions)中，`new.target` 是从周围的作用域继承的。如果箭头函数不是在另一个具有 `new.target` {{Glossary("binding", "绑定")}}的类或函数中定义的，则会抛出语法错误。
- 在[静态初始化块](/zh-CN/docs/Web/JavaScript/Reference/Classes/Static_initialization_blocks)中，`new.target` 是 {{jsxref("undefined")}}。

## 描述

`new.target` 语法由关键字 `new`、点和标识符 `target` 组成。由于 `new` 是[保留字](/zh-CN/docs/Web/JavaScript/Reference/Lexical_grammar#保留字)而非标识符；其并不是[属性访问器](/zh-CN/docs/Web/JavaScript/Reference/Operators/Property_accessors)，而是一种特殊的表达式语法。

`new.target` 元属性在所有的函数/类主体均可用。在函数或类的外部使用 `new.target` 会导致语法错误。

## 示例

### 函数调用中的 new\.target

在普通的函数调用中（和构造函数调用相对），`new.target` 的值是 {{jsxref("undefined")}}。这使得你可以检测一个函数是否是作为构造函数通过 [`new`](/zh-CN/docs/Web/JavaScript/Reference/Operators/new) 被调用的。

```js
function Foo() {
  if (!new.target) {
    throw new Error("必须通过 new 来调用 Foo()");
  }
  console.log("Foo 是通过 new 进行初始化的");
}

new Foo(); // 记录“Foo 是通过 new 进行初始化的”
Foo(); // 抛出“必须通过 new 来调用 Foo()”
```

### 构造函数中的 new\.target

在类的构造函数中，`new.target` 指向直接被 `new` 执行的构造函数。如果构造函数位于父类中，并且是由子类的构造函数委托的，情况也是如此。`new.target` 指向被 `new` 所调用的类。例如，当通过 `new B()` 初始化 `b` 时，打印出了 `B` 的名称；类似地，对于 `a`，打印出了类 `A` 的名称。

```js
class A {
  constructor() {
    console.log(new.target.name);
  }
}

class B extends A {
  constructor() {
    super();
  }
}

const a = new A(); // 记录“A”
const b = new B(); // 记录“B”
```

### 使用 Reflect.construct() 的 new\.target

在 {{jsxref("Reflect.construct()")}} 和类出现之前，通常通过传递 [`this`](/zh-CN/docs/Web/JavaScript/Reference/Operators/this) 的值，并让基类构造函数对其进行更改来实现继承。

```js example-bad
function Base() {
  this.name = "基类";
}

function Extended() {
  // 让 Base() 构造函数可在现有的 `this` 值上工作，
  // 而不是在 `new` 创建的新对象上工作的唯一方法。
  Base.call(this);
  this.otherProperty = "子类";
}

Object.setPrototypeOf(Extended.prototype, Base.prototype);
Object.setPrototypeOf(Extended, Base);

console.log(new Extended()); // Extended { name: '基类', otherProperty: '子类' }
```

然而，{{jsxref("Function/call", "call()")}} 和 {{jsxref("Function/apply", "apply()")}} 实际上是对函数进行*调用*而非*构造*，所以 `new.target` 的值是 `undefined`。这意味着如果 `Base()` 检查它是否是通过 `new` 构造的，将会抛出错误（或者可能表现出其他意外的行为）。例如，你不能通过这种方式扩展 [`Map`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Map/Map)，因为 `Map()` 构造函数不能在不使用 `new` 的情况下调用。

所有内置构造函数都通过读取 `new.target.prototype` 直接构造新实例的整个原型链。因此，为了确保（1）`Base` 是通过 `new` 构造的，以及（2）`new.target` 指向子类而不是 `Base` 本身，我们需要使用 {{jsxref("Reflect.construct()")}}。

```js
function BetterMap(entries) {
  // 调用基类构造函数，但将 `new.target` 设置为子类，
  // 因此创建的实例具有正确的原型链。
  return Reflect.construct(Map, [entries], BetterMap);
}

BetterMap.prototype.upsert = function (key, actions) {
  if (this.has(key)) {
    this.set(key, actions.update(this.get(key)));
  } else {
    this.set(key, actions.insert());
  }
};

Object.setPrototypeOf(BetterMap.prototype, Map.prototype);
Object.setPrototypeOf(BetterMap, Map);

const map = new BetterMap([["a", 1]]);
map.upsert("a", {
  update: (value) => value + 1,
  insert: () => 1,
});
console.log(map.get("a")); // 2
```

> [!NOTE]
> 实际上，由于缺少 `Reflect.construct()`，在转译为 ES6 以前的代码时，无法正确地对内置对象进行子类化（例如 [`Error` 子类化](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Error#自定义错误类型)）。

但是，如果你正在编写 ES6 代码，最好使用类和 `extends`，因为它更易读且更少出错。

```js
class BetterMap extends Map {
  // 构造函数被省略，因为它只是默认的

  upsert(key, actions) {
    if (this.has(key)) {
      this.set(key, actions.update(this.get(key)));
    } else {
      this.set(key, actions.insert());
    }
  }
}

const map = new BetterMap([["a", 1]]);
map.upsert("a", {
  update: (value) => value + 1,
  insert: () => 1,
});
console.log(map.get("a")); // 2
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- [函数](/zh-CN/docs/Web/JavaScript/Reference/Functions)
- [类](/zh-CN/docs/Web/JavaScript/Reference/Classes)
- [`new`](/zh-CN/docs/Web/JavaScript/Reference/Operators/new)
- [`this`](/zh-CN/docs/Web/JavaScript/Reference/Operators/this)

---
# Source: index.md
---
---
title: 无符号右移赋值（>>>=）
slug: Web/JavaScript/Reference/Operators/Unsigned_right_shift_assignment
---

**无符号右移赋值**（**`>>>=`**）运算符向右移动移动指定（二进制）位数，并将结果赋值给变量。

{{InteractiveExample("JavaScript Demo: Expressions - Unsigned right shift assignment operator")}}

```js interactive-example
let a = 5; //  00000000000000000000000000000101

a >>>= 2; //  00000000000000000000000000000001
console.log(a);
// Expected output: 1

let b = -5; // -00000000000000000000000000000101

b >>>= 2; //  00111111111111111111111111111110
console.log(b);
// Expected output: 1073741822
```

## 语法

```js-nolint
x >>>= y // x = x >>> y
```

## 示例

### 使用无符号右移位赋值

```js
let a = 5; //   (00000000000000000000000000000101)
a >>>= 2; // 1 (00000000000000000000000000000001)

let b = -5; // (-00000000000000000000000000000101)
b >>>= 2; // 1073741822 (00111111111111111111111111111110)
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- [JS 指南中的赋值运算符](/zh-CN/docs/Web/JavaScript/Guide/Expressions_and_operators#赋值运算符)
- [无符号右移位运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Unsigned_right_shift)

---
# Source: index.md
---
---
title: 自减（--）
slug: Web/JavaScript/Reference/Operators/Decrement
---

**自减**（**`--`**）运算符对其操作数进行自减（减一），并根据运算符的位置返回自减之前或之后的值。

{{InteractiveExample("JavaScript Demo: Expressions - Decrement operator")}}

```js interactive-example
let x = 3;
const y = x--;

console.log(`x:${x}, y:${y}`);
// Expected output: "x:2, y:3"

let a = 3;
const b = --a;

console.log(`a:${a}, b:${b}`);
// Expected output: "a:2, b:2"
```

## 语法

```js-nolint
x--
--x
```

## 描述

如果使用后缀式，即将运算符放在操作数的后面（如，`x--`），操作数会减一，然后返回减一之前的值。

如果使用前缀式，即将运算符放在操作数的前面（如，`--x`），操作数会减一，然后返回减一之后的值。

自减运算符只能应用于引用的操作数（变量和对象属性，即有效的[赋值目标](/zh-CN/docs/Web/JavaScript/Reference/Operators/Assignment)）。`--x` 本身的计算结果是一个值，而不是一个引用，因此不能将多个自减运算符链接在一起。

```js example-bad
--(--x); // SyntaxError: Invalid left-hand side expression in prefix operation
```

## 示例

### 后缀式

```js
let x = 3;
const y = x--;

// x = 2
// y = 3
```

### 前缀式

```js
let x = 3;
const y = --x;

// x = 2
// y = 2
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- [加法运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Addition)
- [减法运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Subtraction)
- [除法运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Division)
- [乘法运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Multiplication)
- [取余运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Remainder)
- [幂运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Exponentiation)
- [自增运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Increment)
- [一元减运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Unary_negation)
- [一元加运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Unary_plus)

---
# Source: index.md
---
---
title: 逻辑非（!）
slug: Web/JavaScript/Reference/Operators/Logical_NOT
---

**逻辑非**（`!`，逻辑连接取反）运算符将真值或假值转换为对应的相反值，经常用于布尔（逻辑）值。当与非布尔值使用时，如果其操作数可以转化为 `true`，则返回 `false`，否则返回 `true`。

{{InteractiveExample("JavaScript Demo: Expressions - Logical NOT", "shorter")}}

```js interactive-example
const a = 3;
const b = -2;

console.log(!(a > 0 || b > 0));
// Expected output: false
```

## 语法

```js-nolint
!expr
```

## 描述

如果其操作数可以转化为 `true`，则返回 `false`，否则返回 `true`。

能够转化为 `true` 的值叫做{{Glossary("truthy","真值")}}，能够转化为 `false` 的值叫做{{Glossary("falsy","假值")}}。

能够转化为 false 的表达式的示例如下：

- `null`；
- `NaN`；
- `0`；
- 空字符串（`""` 或 `''` 或 ` `` `）；
- `undefined`。

尽管 `!` 运算符可以与非布尔操作数一起使用，但它仍然被认为是一个布尔运算符，因为它的返回值总是可以被转换为[布尔基本类型](/zh-CN/docs/Web/JavaScript/Guide/Data_structures#boolean_类型)。要明确地将其返回值（或任何一般的表达式）转换为相应的布尔值，请使用双非运算符（`!!`）或 {{jsxref("Global_Objects/Boolean/Boolean", "Boolean")}} 构造函数。

## 示例

### 使用非运算符

下列代码展示了 `!`（逻辑非）运算符的用法。

```js
!true; // !t returns false
!false; // !f returns true
!""; // !f returns true
!"Cat"; // !t returns false
```

### 双非运算符（`!!`）

可以使用几个非运算符串联起来，明确地强制将任何值转换为相应的[布尔基本类型](/zh-CN/docs/Web/JavaScript/Guide/Data_structures#boolean_类型)。这种转换是基于值的“真实性”或“虚假性”（详见{{Glossary("truthy","真值")}}和{{Glossary("falsy","假值")}}）。

也可以使用 {{jsxref("Global_Objects/Boolean/Boolean", "Boolean")}} 函数完成转换。

```js
!!true; // !!truthy returns true
!!{}; // !!truthy returns true: any object is truthy...
!!new Boolean(false); // ...even Boolean objects with a false .valueOf()!
!!false; // !!falsy returns false
!!""; // !!falsy returns false
!!Boolean(false); // !!falsy returns false
```

### 非运算符转换

下述涉及到**布尔值**的运算：

```js-nolint
!!bCondition
```

总是与此表达式相同：

```js-nolint
bCondition
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- {{jsxref("Boolean")}}
- {{Glossary("Truthy","真值")}}
- {{Glossary("Falsy","假值")}}

---
# Source: index.md
---
---
title: 赋值（=）
slug: Web/JavaScript/Reference/Operators/Assignment
---

简单赋值运算符（`=`）用于给变量赋值。赋值表达式本身的值为要赋值的值。为了将一个值赋给多个变量，可以链式使用赋值运算符。

{{InteractiveExample("JavaScript Demo: Expressions - Assignment")}}

```js interactive-example
let x = 2;
const y = 3;

console.log(x);
// Expected output: 2

console.log((x = y + 1)); // 3 + 1
// Expected output: 4

console.log((x = x * y)); // 4 * 3
// Expected output: 12
```

## 语法

```js-nolint
x = y
```

## 示例

### 简单赋值和链式赋值

```js
// 假设已经存在以下变量
//  x = 5
//  y = 10
//  z = 25

x = y; // x 为 10
x = y = z; // x, y 都为 25
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- [JS 指南中的赋值运算符](/zh-CN/docs/Web/JavaScript/Guide/Expressions_and_operators#赋值运算符)

---
# Source: index.md
---
---
title: 乘法赋值（*=）
slug: Web/JavaScript/Reference/Operators/Multiplication_assignment
---

**乘法赋值**（**`*=`**）运算符将变量乘以右操作数的值，并将结果赋值给该变量。

{{InteractiveExample("JavaScript Demo: Expressions - Multiplication assignment operator")}}

```js interactive-example
let a = 2;

console.log((a *= 3));
// Expected output: 6

console.log((a *= "hello"));
// Expected output: NaN
```

## 语法

```js-nolint
x *= y // x = x * y
```

## 示例

### 使用乘法赋值

```js
let bar = 5;

bar *= 2; // 10
bar *= "foo"; // NaN
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- [JS 指南中的赋值操作符](/zh-CN/docs/Web/JavaScript/Guide/Expressions_and_operators#赋值运算符)
- [乘法运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Multiplication)

---
# Source: index.md
---
---
title: async function* 表达式
slug: Web/JavaScript/Reference/Operators/async_function*
---

**`async function*`** 关键字可用于在表达式中定义一个异步生成器函数。

你也可以使用 [`async function*` 声明](/zh-CN/docs/Web/JavaScript/Reference/Statements/async_function*)定义一个异步生成器函数。

{{InteractiveExample("JavaScript Demo: Expressions - Async Function Asterisk", "taller")}}

```js interactive-example
async function* foo() {
  yield await Promise.resolve("a");
  yield await Promise.resolve("b");
  yield await Promise.resolve("c");
}

let str = "";

async function generate() {
  for await (const val of foo()) {
    str = str + val;
  }
  console.log(str);
}

generate();
// Expected output: "abc"
```

## 语法

```js-nolint
async function* (param0) {
  statements
}
async function* (param0, param1) {
  statements
}
async function* (param0, param1, /* … ,*/ paramN) {
  statements
}

async function* name(param0) {
  statements
}
async function* name(param0, param1) {
  statements
}
async function* name(param0, param1, /* … ,*/ paramN) {
  statements
}
```

> [!NOTE]
> 为了避免 [`async function*` 声明](/zh-CN/docs/Web/JavaScript/Reference/Statements/async_function*)所带来的歧义，[表达式语句](/zh-CN/docs/Web/JavaScript/Reference/Statements/Expression_statement)不能以关键字 `async function` 开头。`async function` 关键字仅在上下文中无法接受语句时，才会被视为表达式的开头。

### 参数

- `name` {{optional_inline}}
  - : 函数名。在这种情况下，函数名是*匿名的*，可以被省略。该名称仅在函数主体的内部有效。
- `paramN` {{optional_inline}}
  - : 传递给函数的参数名称。
- `statements` {{optional_inline}}
  - : 构成函数主体的语句。

## 描述

`async function*` 表达式与 [`async function*` 声明](/zh-CN/docs/Web/JavaScript/Reference/Statements/async_function*)非常相似，语法几乎相同。*函数名*是 `async function*` 表达式和 `async function*` 声明之间最主要的区别，在 `async function*` 表达式中，可以创建*匿名*函数去忽略函数名。`async function*` 表达式可以用作[立即调用函数表达式（IIFE）](/zh-CN/docs/Glossary/IIFE)，该表达式在被定义后立即运行，允许你去创建一个临时的[异步的可迭代对象](/zh-CN/docs/Web/JavaScript/Reference/Iteration_protocols#异步迭代器和异步可迭代协议)。有关更多信息，请参见[函数](/zh-CN/docs/Web/JavaScript/Reference/Functions)这个章节。

## 示例

### 使用 async function\*

以下示例定义了一个没有名称的异步生成器函数并将它分配给变量 `x`。这个函数产生它参数的平方。

```js
const x = async function* (y) {
  yield Promise.resolve(y * y);
};
x(6)
  .next()
  .then((res) => console.log(res.value)); // 36
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- {{jsxref("Statements/async_function*", "async function*")}} 语句
- {{jsxref("AsyncGeneratorFunction")}} 对象
- [迭代协议](/zh-CN/docs/Web/JavaScript/Reference/Iteration_protocols)
- {{jsxref("GeneratorFunction")}} 对象
- {{jsxref("Operators/yield", "yield")}}
- {{jsxref("Operators/yield*", "yield*")}}
- {{jsxref("Function")}} 对象
- {{jsxref("Functions", "函数", "", 1)}}

---
# Source: index.md
---
---
title: 大于等于（>=）
slug: Web/JavaScript/Reference/Operators/Greater_than_or_equal
---

大于等于运算符（`>=`）在左操作数大于等于右操作数时返回 `true`，否则返回 `false`。

{{InteractiveExample("JavaScript Demo: Expressions - Greater than or equal operator")}}

```js interactive-example
console.log(5 >= 3);
// Expected output: true

console.log(3 >= 3);
// Expected output: true

// Compare bigint to number
console.log(3n >= 5);
// Expected output: false

console.log("ab" >= "aa");
// Expected output: true
```

## 语法

```js-nolint
x >= y
```

## 描述

操作数比较使用与[小于](/zh-CN/docs/Web/JavaScript/Reference/Operators/Less_than)运算符相同的算法，除了两个操作数为相等的值（在尝试转换后）会返回 `true`。

## 示例

### 字符串与字符串比较

```js
console.log("a" >= "b"); // false
console.log("a" >= "a"); // true
console.log("a" >= "3"); // true
```

### 字符串与数值比较

```js
console.log("5" >= 3); // true
console.log("3" >= 3); // true
console.log("3" >= 5); // false

console.log("hello" >= 5); // false
console.log(5 >= "hello"); // false
```

### 数值与数值比较

```js
console.log(5 >= 3); // true
console.log(3 >= 3); // true
console.log(3 >= 5); // false
```

### 数值与大整型比较

```js
console.log(5n >= 3); // true
console.log(3 >= 3n); // true
console.log(3 >= 5n); // false
```

### 比较 Boolean、null、undefined 和 NaN

```js
console.log(true >= false); // true
console.log(true >= true); // true
console.log(false >= true); // false

console.log(true >= 0); // true
console.log(true >= 1); // true

console.log(null >= 0); // true
console.log(1 >= null); // true

console.log(undefined >= 3); // false
console.log(3 >= undefined); // false

console.log(3 >= NaN); // false
console.log(NaN >= 3); // false
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## See also

- [大于运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Greater_than)
- [小于运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Less_than)
- [小于等于运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Less_than_or_equal)

---
# Source: index.md
---
---
title: import.meta
slug: Web/JavaScript/Reference/Operators/import.meta
l10n:
  sourceCommit: 4f86aad2b0b66c0d2041354ec81400c574ab56ca
---

**`import.meta`** 元属性将特定上下文的元数据暴露给 JavaScript 模块。它包含了这个模块的信息，例如这个模块的 URL。

## 语法

```js-nolint
import.meta
```

### 值

`import.meta` 是一个宿主环境创建的可扩展的 [`null` 原型](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Object#null_原型对象)对象，其所有属性均可写、可配置、可枚举。规范没有在对象上明确定义任何属性，但是宿主环境通常会定义以下属性：

- `url`
  - : 到此模块的完整 URL，包括查询参数和片段标识符（在 `?` 和 `#` 之后）。在浏览器中，它是可获取此脚本的 URL（对外部脚本）或者是包含此脚本的文档的 URL（对内联脚本）。在 Node.js 中，它是文件路径（包括 `file://` 协议部分）。
- [`resolve`](/zh-CN/docs/Web/JavaScript/Reference/Operators/import.meta/resolve)
  - : 将一个模块的标识符解析为相对于当前模块的 URL。

## 描述

`import.meta` 语法由关键字 `import`、一个点符号和 `meta` 标识符组成。因为 `import` 是[保留字](/zh-CN/docs/Web/JavaScript/Reference/Lexical_grammar#保留字)而不是标识符，其并不是[属性访问器](/zh-CN/docs/Web/JavaScript/Reference/Operators/Property_accessors)而是特殊的表达式语法。

`import.meta` 元属性在 JavaScript 模块中可用；在模块之外（包括在模块中[直接调用 `eval()`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/eval#直接和间接_eval)）使用 `import.meta` 是语法错误。

## 示例

### 传递查询参数

在 `import` 声明中使用查询参数允许为特定模块传递参数，可作为应用程序内从 [`window.location`](/zh-CN/docs/Web/API/Window/location)（或在 Node.js 中从 `process.env`）读取参数的补充方式。例如下面的 HTML：

```html
<script type="module">
  import "./index.mjs?someURLInfo=5";
</script>
```

`index.mjs` 模块可以通过 `import.meta` 获取 `someURLInfo` 参数：

```js
// index.mjs
new URL(import.meta.url).searchParams.get("someURLInfo"); // 5
```

在脚本中引入别的脚本同样生效：

```js
// index.mjs
import "./index2.mjs?someURLInfo=5";

// index2.mjs
new URL(import.meta.url).searchParams.get("someURLInfo"); // 5
```

Node.js 中 ES 模块的实现支持在解析模块的标识符中含有查询参数和片段标识符，如上述示例所示。然而，从命令行指定模块标识符时无法使用查询参数和片段标识符（例如 `node index.mjs?someURLInfo=5`），因为命令行的入口点使用了类似于 CommonJS 的解析模式，将整个路径视为文件而非 URL。要将参数传递给入口点模块，需要改用命令行参数，并从 `precess.argv` 读取（如 `node index.mjs --someURLInfo=5`）。

### 相对当前文件解析文件路径

在 Node.js 的 CommonJS 模块中，有专门的 `__dirname` 变量，值为包含当前文件的文件夹的绝对路径，可以用来解析相对路径。但是，ES 模块除了 `import.meta` 之外没有上下文变量。因此，要解析相对路径的文件，可以使用 `import.meta.url`。注意这个属性使用的是 URL 而非文件系统的路径。

之前（CommonJS）：

```js
const fs = require("fs/promises");
const path = require("path");

const filePath = path.join(__dirname, "someFile.txt");
fs.readFile(filePath, "utf8").then(console.log);
```

之后（ES 模块）：

```js
import fs from "node:fs/promises";

const fileURL = new URL("./someFile.txt", import.meta.url);
fs.readFile(fileURL, "utf8").then(console.log);
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- [`import`](/zh-CN/docs/Web/JavaScript/Reference/Statements/import)
- [`export`](/zh-CN/docs/Web/JavaScript/Reference/Statements/export)

---
# Source: index.md
---
---
title: 幂赋值（**=）
slug: Web/JavaScript/Reference/Operators/Exponentiation_assignment
l10n:
  sourceCommit: 145e8c316fcdd8f67f3595fc52b0bbfacf7b949d
---



**幂赋值**（**`**=`**）对两个操作数执行[幂运算](/zh-CN/docs/Web/JavaScript/Reference/Operators/Exponentiation)，并将结果赋给左操作数。

{{InteractiveExample("JavaScript Demo: Expressions - Exponentiation assignment operator")}}

```js interactive-example
let a = 3;

console.log((a **= 2));
// Expected output: 9

console.log((a **= 0));
// Expected output: 1

console.log((a **= 'hello'));
// Expected output: NaN
```

## 语法

```js-nolint
x **= y
```

## 描述

`x **= y` 和 `x = x ** y` 是等价的，不同之处在于前者的 `x` 只被计算一次。

## 示例

### 使用数字进行幂赋值

```js
let bar = 5;
bar **= 2; // 25
```

其他非 BigInt 值会被强制转换为数字：

```js
let baz = 5;
baz **= "foo"; // NaN
```

### 使用 BigInt 进行幂赋值

```js
let foo = 3n;
foo **= 2n; // 9n
foo **= 1; // TypeError: Cannot mix BigInt and other types, use explicit conversions
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- [JS 指南中的赋值运算符](/zh-CN/docs/Web/JavaScript/Guide/Expressions_and_operators#赋值运算符)
- [幂运算符（`**`）](/zh-CN/docs/Web/JavaScript/Reference/Operators/Exponentiation)

---
# Source: index.md
---
---
title: 对象初始化器
slug: Web/JavaScript/Reference/Operators/Object_initializer
---

**对象初始化器**是一个用大括号（`{}`）括起来的以逗号分隔的列表，包含了一个对象的零个或多个属性名称和相关值。可以通过 [`Object.create()`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Object/create) 方法，或者使用 [`new`](/zh-CN/docs/Web/JavaScript/Reference/Operators/new) 运算符[调用其构造函数](/zh-CN/docs/Web/JavaScript/Guide/Working_with_objects#使用构造函数)而初始化一个对象。

{{InteractiveExample("JavaScript Demo: Expressions - Object initializer", "taller")}}

```js interactive-example
const object1 = { a: "foo", b: 42, c: {} };

console.log(object1.a);
// Expected output: "foo"

const a = "foo";
const b = 42;
const c = {};
const object2 = { a: a, b: b, c: c };

console.log(object2.b);
// Expected output: 42

const object3 = { a, b, c };

console.log(object3.a);
// Expected output: "foo"
```

## 语法

```js-nolint
o = {
  a: "foo",
  b: 42,
  c: {},
  1: "number literal property",
  "foo:bar": "string literal property",

  shorthandProperty,

  method(parameters) {
    // …
  },

  get property() {},
  set property(value) {},

  [expression]: "computed property",

  __proto__: prototype,

  ...spreadProperty,
};
```

## 描述

对象初始化器是一个描述 {{jsxref("Object")}} 初始化的表达式。对象由用于描述对象的*属性*组成。对象属性的值可以包含[基本](/zh-CN/docs/Glossary/Primitive)数据类型或其他对象。

### 对象字面语法与 JSON 的对比

对象字面的语法与 **J**ava**S**cript **O**bject **N**otation（[JSON](/zh-CN/docs/Glossary/JSON)）不一样。虽然它们看起来很相似，但它们之间还是有区别的：

- JSON *只*允许使用 `"property": value` 的语法进行属性定义。属性名必须是双引号，而且定义不能简写。计算属性名也是不允许的。
- JSON 对象的属性值只能是字符串、数字、`true`、`false`、`null`、数组或其他 JSON 对象。这意味着 JSON 不能表达方法或非普通对象，如 [`Date`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Date) 或 [`RegExp`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/RegExp)。
- 在 JSON 中，`"__proto__"` 是一个普通的属性键。在对象字面中，它[设置对象的原型](#原型_setter)。

JSON 是对象字面语法的一个*真*子集，意味着每一个有效的 JSON 文本都可以被解析为对象字面，并且不会引起语法错误。唯一的例外是，对象字面语法禁止重复的 `__proto__` 键，这不适用于 [`JSON.parse()`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/JSON/parse)。后者将 `__proto__` 像普通的属性一样对待，并将最后一次出现的对象作为该属性的值。它们所代表的对象值（也就是它们的语义）唯一不同的时候，也就是当源码包含 `__proto__` 键的时候——对于对象字面，它设置对象的原型；对于 JSON，它是一个普通的属性。

```js
console.log(JSON.parse('{ "__proto__": 0, "__proto__": 1 }')); // {__proto__: 1}
console.log({ "__proto__": 0, "__proto__": 1 }); // SyntaxError: Duplicate __proto__ fields are not allowed in object literals
console.log(JSON.parse('{ "__proto__": {} }')); // { __proto__: {} }
console.log({ "__proto__": {} }); // {}（其原型为 {}）
```

## 示例

### 创建对象

没有属性的空对象可以用以下方式创建：

```js
const object = {};
```

*字面初始化器*符号的优势在于能够快速创建带有大括号内属性的对象，可以快速记录下一个以逗号分隔的 `key: value` 对的列表。

如下代码创建了一个含三个属性的对象，键分别为 `"foo"`、`"age"` 和 `"baz"`。这些键对应的值，分别是字符串 `"bar"`，数字 `42` 和另一个对象。

```js
const object = {
  foo: "bar",
  age: 42,
  baz: { myProp: 12 },
};
```

### 访问属性

创建对象后，可以读取或者修改它。对象属性可以用下标小圆点标记或者方括号标记访问。参见[属性访问器](/zh-CN/docs/Web/JavaScript/Reference/Operators/Property_accessors)获取更多信息。

```js
object.foo; // "bar"
object["age"]; // 42
object.baz; // {myProp: 12}
object.baz.myProp; //12
```

### 属性定义

上面学习了如何用初始化语法对象属性。经常能遇到希望将代码中的变量放到对象中的情况。可能遇到如下代码：

```js
const a = "foo";
const b = 42;
const c = {};

const o = {
  a: a,
  b: b,
  c: c,
};
```

有更简短的标记可以实现同样的效果：

```js
const a = "foo";
const b = 42;
const c = {};

// 简写属性名
const o = { a, b, c };

// 也就是说，
console.log(o.a === { a }.a); // true
```

#### 重复属性名

属性使用了同样的名称时，后面的属性会覆盖前面的属性。

```js
const a = { x: 1, x: 2 };
console.log(a); // {x: 2}
```

在 ES2015 之后，任何地方都允许重复属性名出现，也包括[严格模式](/zh-CN/docs/Web/JavaScript/Reference/Strict_mode#duplicate_property_names)。你也可以在[类](/zh-CN/docs/Web/JavaScript/Reference/Classes)中使用重复的属性名。唯一的例外是[私有元素](/zh-CN/docs/Web/JavaScript/Reference/Classes/Private_elements)，在整个类中它必须是唯一的。

### 方法定义

对象属性也可以是一个[函数](/zh-CN/docs/Web/JavaScript/Reference/Functions)、[getter](/zh-CN/docs/Web/JavaScript/Reference/Functions/get) 或 [setter](/zh-CN/docs/Web/JavaScript/Reference/Functions/set) 方法。

```js
const o = {
  property: function (parameters) {},
  get property() {},
  set property(value) {},
};
```

存在一种更简短的写法，关键字 `function` 也可以省略。

```js
// 简写属性名
const o = {
  property(parameters) {},
};
```

也可以简短地定义生成器方法。

```js
const o = {
  *generator() {
    // …
  },
};
```

这相当于这个类似 ES5 的符号（但注意 ECMAScript 5 没有生成器）：

```js
const o = {
  generator: function* () {
    // …
  },
};
```

有关方法的更多信息和例子，请参见[方法定义](/zh-CN/docs/Web/JavaScript/Reference/Functions/Method_definitions)。

### 计算属性名

对象初始化器的语法也支持计算的属性名称。这允许你把一个表达式放在中括号 `[]` 中，它将被计算并作为属性名使用。这让人想起[属性访问器](/zh-CN/docs/Web/JavaScript/Reference/Operators/Property_accessors)语法中的括号符号，你可能已经用它来读取和设置属性。

现在你也可以在对象字面量上使用类似的语法：

```js
// 计算属性名
let i = 0;
const a = {
  [`foo${++i}`]: i,
  [`foo${++i}`]: i,
  [`foo${++i}`]: i,
};

console.log(a.foo1); // 1
console.log(a.foo2); // 2
console.log(a.foo3); // 3

const items = ["A", "B", "C"];
const obj = {
  [items]: "Hello",
};
console.log(obj); // A,B,C: "Hello"
console.log(obj["A,B,C"]); // "Hello"

const param = "size";
const config = {
  [param]: 12,
  [`mobile${param.charAt(0).toUpperCase()}${param.slice(1)}`]: 4,
};

console.log(config); // {size: 12, mobileSize: 4}
```

### 扩展属性

对象字面量支持[扩展语法](/zh-CN/docs/Web/JavaScript/Reference/Operators/Spread_syntax)。它将自己提供的对象的枚举属性复制到一个新的对象上。

现在可以使用比 {{jsxref("Object.assign()")}} 更短的语法来实现浅拷贝（不包括 `prototype`）或合并对象。

```js
const obj1 = { foo: "bar", x: 42 };
const obj2 = { foo: "baz", y: 13 };

const clonedObj = { ...obj1 };
// { foo: "bar", x: 42 }

const mergedObj = { ...obj1, ...obj2 };
// { foo: "baz", x: 42, y: 13 }
```

> [!WARNING]
> 请注意，{{jsxref("Object.assign()")}} 会触发 [setter](/zh-CN/docs/Web/JavaScript/Reference/Functions/set)，而展开语法不会！

### 原型 setter

一个形式为 `__proto__: value` 或 `"__proto__": value` 的属性定义并没有创建一个名称为 `__proto__` 的属性。相反，如果提供的值是一个对象或 [`null`](/zh-CN/docs/Web/JavaScript/Reference/Operators/null) 值，它将创建对象的 `[[Prototype]]` 指向该值（如果该值不是一个对象或 `null`，该对象不会被改变）。

请注意，`__proto__` 键是标准化的语法，与非标准且性能不佳的 [`Object.prototype.__proto__`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Object/proto) 访问器不同。它在创建对象时设置了 `[[Prototype]]`，类似于 {{jsxref("Object.create")}}——而不是变更原型链。

```js-nolint
const obj1 = {};
console.log(Object.getPrototypeOf(obj1) === Object.prototype); // true

const obj2 = { __proto__: null };
console.log(Object.getPrototypeOf(obj2)); // null

const protoObj = {};
const obj3 = { "__proto__": protoObj };
console.log(Object.getPrototypeOf(obj3) === protoObj); // true

const obj4 = { __proto__: "not an object or null" };
console.log(Object.getPrototypeOf(obj4) === Object.prototype); // true
console.log(Object.hasOwn(obj4, "__proto__")); // false
```

在对象字面值中，仅允许有一个原型 setter；多个原型 setter 会被视为语法错误。

不使用“冒号”标记法的属性定义不是原型 setter。它们是属性定义，其行为与使用任何其他名称的类似定义相同。

```js
const __proto__ = "variable";

const obj1 = { __proto__ };
console.log(Object.getPrototypeOf(obj1) === Object.prototype); // true
console.log(Object.hasOwn(obj1, "__proto__")); // true
console.log(obj1.__proto__); // "variable"

const obj2 = { __proto__() { return "hello"; } };
console.log(obj2.__proto__()); // "hello"

const obj3 = { ["__proto__"]: 17 };
console.log(obj3.__proto__); // 17

// 将原型 setter 与正常的使用“__proto__”键的自有属性混合在一起
const obj4 = { ["__proto__"]: 17, __proto__: {} }; // {__proto__: 17} （原型为 {}）
const obj5 = {
  ["__proto__"]: 17,
  __proto__: {},
  __proto__: null, // SyntaxError: Duplicate __proto__ fields are not allowed in object literals
};

const obj6 = {
  ["__proto__"]: 17,
  ["__proto__"]: "hello",
  __proto__: null,
}; // {__proto__: "hello"}（原型为 null）
const obj7 =  {
  ["__proto__"]: 17,
  __proto__,
  __proto__: null,
}; // {__proto__: "variable"}（原型为 null）
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- [属性访问器](/zh-CN/docs/Web/JavaScript/Reference/Operators/Property_accessors)
- [`get`](/zh-CN/docs/Web/JavaScript/Reference/Functions/get) / [`set`](/zh-CN/docs/Web/JavaScript/Reference/Functions/set)
- [方法定义](/zh-CN/docs/Web/JavaScript/Reference/Functions/Method_definitions)
- [词法和语法](/zh-CN/docs/Web/JavaScript/Reference/Lexical_grammar)

---
# Source: index.md
---
---
title: 表达式和运算符
slug: Web/JavaScript/Reference/Operators
l10n:
  sourceCommit: fb85334ffa4a2c88d209b1074909bee0e0abd57a
---

该章节说明了 JavaScript 语言所有的运算符、表达式和关键字。

## 表达式和运算符分类

要查看按字母顺序排列的列表，请参阅左边的侧边栏。

### 主要表达式

JavaScript 中的基本关键字和常用表达式。这些表达式具有最高的优先级（高于[运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Operator_precedence)）。

- {{jsxref("Operators/this", "this")}}
  - : `this` 关键字指向执行上下文的特殊属性。
- [字面量](/zh-CN/docs/Web/JavaScript/Reference/Lexical_grammar#字面量)
  - : 基本的 `null`、布尔、数字和字符串字面量。
- {{jsxref("Array", "[]")}}
  - : 数组初始化或字面量语法。
- {{jsxref("Operators/Object_initializer", "{}")}}
  - : 对象初始化或字面量语法。
- {{jsxref("Operators/function", "function")}}
  - : `function` 关键字定义了函数表达式。
- {{jsxref("Operators/class", "class")}}
  - : `class` 关键字定义了类表达式。
- {{jsxref("Operators/function*", "function*")}}
  - : `function*` 关键字定义了一个生成器函数表达式。
- {{jsxref("Operators/async_function", "async function")}}
  - : `async function` 定义一个异步函数表达式。
- {{jsxref("Operators/async_function*", "async function*")}}
  - : `async function*` 定义了一个异步生成器函数表达式。
- {{jsxref("RegExp", "/ab+c/i")}}
  - : 正则表达式字面量语法。
- {{jsxref("Template_literals", "`string`")}}
  - : 模版字面量语法。
- {{jsxref("Operators/Grouping", "( )")}}
  - : 分组运算符。

### 左表达式

左边的值是赋值的目标。

- {{jsxref("Operators/Property_accessors", "属性访问符", "", 1)}}
  - : 成员运算符用于访问对象的属性或方法（`object.property` 和 `object["property"]`）。
- {{jsxref("Operators/Optional_chaining", "?.")}}
  - : 如果引用是[空值](/zh-CN/docs/Glossary/Nullish)（[`null`](/zh-CN/docs/Web/JavaScript/Reference/Operators/null) 或 [`undefined`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/undefined)），可选链运算符将返回 `undefined` 而不是导致错误。
- {{jsxref("Operators/new", "new")}}
  - : `new` 运算符创建了构造函数实例。
- {{jsxref("Operators/new%2Etarget", "new.target")}}
  - : 在构造函数中，`new.target` 指向 {{jsxref("Operators/new", "new")}} 调用的构造函数。
- {{jsxref("Operators/import%2Emeta", "import.meta")}}
  - : 向 JavaScript 模块暴露特定上下文的元数据属性的对象。
- {{jsxref("Operators/super", "super")}}
  - : `super` 关键字调用父类的构造函数或用于访问父类对象的属性。
- {{jsxref("Operators/import", "import()")}}
  - : `import()` 语法允许将模块异步且动态地加载到可能为非模块环境的上下文中。

### 自增和自减

前置或后置自增运算符和前置或后置自减运算符。

- {{jsxref("Operators/Increment", "A++")}}
  - : 后置自增运算符。
- {{jsxref("Operators/Decrement", "A--")}}
  - : 后置自减运算符。
- {{jsxref("Operators/Increment", "++A")}}
  - : 前置自增运算符。
- {{jsxref("Operators/Decrement", "--A")}}
  - : 前置自减运算符。

### 一元运算符

一元运算符只有一个操作数。

- {{jsxref("Operators/delete", "delete")}}
  - : `delete` 运算符用来删除对象的属性。
- {{jsxref("Operators/void", "void")}}
  - : `void` 运算符执行表达式并丢弃其返回值。
- {{jsxref("Operators/typeof", "typeof")}}
  - : `typeof` 运算符用来判断给定对象的类型。
- {{jsxref("Operators/Unary_plus", "+")}}
  - : 一元加运算符将操作数转换为 Number 类型。
- {{jsxref("Operators/Unary_negation", "-")}}
  - : 一元减运算符将操作数转换为 Number 类型并取反。
- {{jsxref("Operators/Bitwise_NOT", "~")}}
  - : 按位非运算符。
- {{jsxref("Operators/Logical_NOT", "!")}}
  - : 逻辑非运算符。
- {{jsxref("Operators/await", "await")}}
  - : 暂停或恢复执行异步函数，并等待 promise 的兑现或拒绝。

### 算术运算符

算术运算符以二个数值（字面量或变量）作为操作数，并返回单个数值。

- {{jsxref("Operators/Exponentiation", "**")}}
  - : 求幂运算符。
- {{jsxref("Operators/Multiplication", "*")}}
  - : 乘法运算符。
- {{jsxref("Operators/Division", "/")}}
  - : 除法运算符。
- {{jsxref("Operators/Remainder", "%")}}
  - : 取模运算符。
- {{jsxref("Operators/Addition", "+")}}（加）
  - : 加法运算符。
- {{jsxref("Operators/Subtraction", "-")}}
  - : 减法运算符。

### 关系运算符

比较运算符比较两个操作数并返回基于比较结果的布尔值。

- {{jsxref("Operators/Less_than", "&lt;")}}（小于）
  - : 小于运算符。
- {{jsxref("Operators/Greater_than", "&gt;")}}（大于）
  - : 大于运算符。
- {{jsxref("Operators/Less_than_or_equal", "&lt;=")}}
  - : 小于等于运算符。
- {{jsxref("Operators/Greater_than_or_equal", "&gt;=")}}
  - : 大于等于运算符。
- {{jsxref("Operators/instanceof", "instanceof")}}
  - : `instanceof` 运算符判断一个对象是否是另一个对象的实例。
- {{jsxref("Operators/in", "in")}}
  - : `in` 运算符用来判断对象是否拥有给定属性。

> [!NOTE]
> `=>` 不是运算符，而是[箭头函数](/zh-CN/docs/Web/JavaScript/Reference/Functions/Arrow_functions)的表示符。

### 相等运算符

相等运算符的求值结果始终是布尔类型（基于比较是否为 true）。

- {{jsxref("Operators/Equality", "==")}}
  - : 相等运算符。
- {{jsxref("Operators/Inequality", "!=")}}
  - : 不等运算符。
- {{jsxref("Operators/Strict_equality", "===")}}
  - : 严格相等运算符。
- {{jsxref("Operators/Strict_inequality", "!==")}}
  - : 严格不相等运算符。

### 位移运算符

对操作数的所有二进制位进行移动操作。

- {{jsxref("Operators/Left_shift", "&lt;&lt;")}}
  - : 按位左移运算符。
- {{jsxref("Operators/Right_shift", "&gt;&gt;")}}
  - : 按位右移运算符。
- {{jsxref("Operators/Unsigned_right_shift", "&gt;&gt;&gt;")}}
  - : 按位无符号右移运算符。

### 二进制位运算符

二进制运算符将它们的操作数作为 32 个二进制位（0 或 1）的集合，并返回标准的 JavaScript 数值。

- {{jsxref("Operators/Bitwise_AND", "&amp;")}}
  - : 按位与（AND）。
- {{jsxref("Operators/Bitwise_OR", "|")}}
  - : 按位或（OR）。
- {{jsxref("Operators/Bitwise_XOR", "^")}}
  - : 按位异或（XOR）。

### 二元逻辑运算符

逻辑运算符实现布尔（逻辑）值运算，并具有[短路](/zh-CN/docs/Web/JavaScript/Reference/Operators/Operator_precedence#短路)行为。

- {{jsxref("Operators/Logical_AND", "&amp;&amp;")}}
  - : 逻辑与（AND）。
- {{jsxref("Operators/Logical_OR", "||")}}
  - : 逻辑或（OR）。
- {{jsxref("Operators/Nullish_coalescing", "??")}}
  - : 空值合并运算符。

### 条件（三元）运算符

- {{jsxref("Operators/Conditional_operator", "(condition ? ifTrue : ifFalse)")}}
  - : 条件运算符返回两个值中符合条件逻辑值的那个值。

### 赋值运算符

赋值运算符将右边的操作数的值赋给左边的操作数。

- {{jsxref("Operators/Assignment", "=")}}
  - : 赋值运算符。
- {{jsxref("Operators/Multiplication_assignment", "*=")}}
  - : 赋值乘积。
- {{jsxref("Operators/Division_assignment", "/=")}}
  - : 赋值商。
- {{jsxref("Operators/Remainder_assignment", "%=")}}
  - : 赋值求余。
- {{jsxref("Operators/Addition_assignment", "+=")}}
  - : 赋值求和。
- {{jsxref("Operators/Subtraction_assignment", "-=")}}
  - : 赋值求差。
- {{jsxref("Operators/Left_shift_assignment", "&lt;&lt;=")}}
  - : 左位移。
- {{jsxref("Operators/Right_shift_assignment", "&gt;&gt;=")}}
  - : 右位移。
- {{jsxref("Operators/Unsigned_right_shift_assignment", "&gt;&gt;&gt;=")}}
  - : 无符号右位移。
- {{jsxref("Operators/Bitwise_AND_assignment", "&amp;=")}}
  - : 赋值与（AND）。
- {{jsxref("Operators/Bitwise_XOR_assignment", "^=")}}
  - : 赋值按位异或（XOR）。
- {{jsxref("Operators/Bitwise_OR_assignment", "|=")}}
  - : 赋值或（OR）。
- {{jsxref("Operators/Exponentiation_assignment", "**=")}}
  - : 求幂赋值。
- {{jsxref("Operators/Logical_AND_assignment", "&amp;&amp;=")}}
  - : 逻辑和赋值运算符。
- {{jsxref("Operators/Logical_OR_assignment", "||=")}}
  - : 逻辑或赋值运算符。
- {{jsxref("Operators/Nullish_coalescing_assignment", "??=")}}
  - : 逻辑空赋值运算符。
- [`[a, b] = arr`、`{ a, b } = obj`](/zh-CN/docs/Web/JavaScript/Reference/Operators/Destructuring)
  - : 解构允许你使用类似于数组或对象字面量的语法将数组或对象的属性赋值给变量。

### Yield 运算符

- {{jsxref("Operators/yield", "yield")}}
  - : 暂停和恢复生成器函数。
- {{jsxref("Operators/yield*", "yield*")}}
  - : 委派给另外一个生成器函数或可迭代对象。

### 展开语法

- {{jsxref("Operators/Spread_syntax", "...obj")}}
  - : 展开语法允许在需要零个或多个参数（对于函数调用）或者元素（对于数组字面量）的地方展开可迭代对象（例如，数组或字符串）。而在对象字面量中，展开语法枚举对象的属性，并将其键值对添加到正在创建的对象中。

### 逗号运算符

- {{jsxref("Operators/Comma_operator", ",")}}
  - : 逗号运算符允许在单个语句中对多个表达式进行求值，并返回最后一个表达式的结果。

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- [运算符优先级](/zh-CN/docs/Web/JavaScript/Reference/Operators/Operator_precedence)

---
# Source: index.md
---
---
title: 左移赋值（<<=）
slug: Web/JavaScript/Reference/Operators/Left_shift_assignment
---

左移赋值运算符（`<<=`）将变量向左移动指定的位数，并将结果赋值给变量。

{{InteractiveExample("JavaScript Demo: Expressions - Left shift assignment operator", "shorter")}}

```js interactive-example
let a = 5; // 00000000000000000000000000000101

a <<= 2; // 00000000000000000000000000010100

console.log(a);
// Expected output: 20
```

## 语法

```js-nolint
x <<= y // x = x << y
```

## 示例

### 使用左移赋值

```js
let a = 5;
// 00000000000000000000000000000101

a <<= 2; // 20
// 00000000000000000000000000010100
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参考

- [JS 指南中的赋值运算符](/zh-CN/docs/Web/JavaScript/Guide/Expressions_and_operators#赋值运算符)
- [左移运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Left_shift)

---
# Source: index.md
---
---
title: 圆括号运算符
slug: Web/JavaScript/Reference/Operators/Grouping
---

圆括号运算符 `( )` 用于控制表达式中的运算优先级。

{{InteractiveExample("JavaScript Demo: Expressions - Grouping operator")}}

```js interactive-example
console.log(1 + 2 * 3); // 1 + 6
// Expected output: 7

console.log(1 + 2 * 3); // 1 + 6
// Expected output: 7

console.log((1 + 2) * 3); // 3 * 3
// Expected output: 9

console.log(1 * 3 + 2 * 3); // 3 + 6
// Expected output: 9
```

## 语法

```js-nolint
(expression)
```

## 说明

圆括号运算符由一对圆括号组成，包裹表达式和子表达式用来覆盖常规的[运算符优先级](/zh-CN/docs/Web/JavaScript/Reference/Operators/Operator_precedence)，达到低优先级的表达式比高优先级的表达式更早运算。

## 示例

下面的代码展示了加法运算先于乘法运算的情况。

```js-nolint
const a = 1;
const b = 2;
const c = 3;

// 默认优先级
a + b * c; // 7
// 默认运算顺序同下
a + (b * c); // 7

// 现在优先考虑乘法之前的加法
(a + b) * c; // 9

// 这相当于
a * c + b * c; // 9
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- [运算符优先级](/zh-CN/docs/Web/JavaScript/Reference/Operators/Operator_precedence)
- {{jsxref("Operators/delete", "delete")}}
- {{jsxref("Operators/typeof", "typeof")}}

---
# Source: index.md
---
---
title: 除法（/）
slug: Web/JavaScript/Reference/Operators/Division
---

**除法**（**`/`**）运算符计算两个操作数的商，其中左操作数是被除数，右操作数是除数。

{{InteractiveExample("JavaScript Demo: Expressions - Division operator")}}

```js interactive-example
console.log(12 / 2);
// Expected output: 6

console.log(3 / 2);
// Expected output: 1.5

console.log(6 / "3");
// Expected output: 2

console.log(2 / 0);
// Expected output: Infinity
```

## 语法

```js-nolint
x / y
```

## 示例

### 基本除法

```js
1 / 2; // 0.5

Math.floor(3 / 2); // 1

1.0 / 2.0; // 0.5
```

### 除以零

```js
2.0 / 0; // Infinity

2.0 / 0.0; // Infinity, because 0.0 === 0

2.0 / -0.0; // -Infinity
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- [加法运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Addition)
- [减法运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Subtraction)
- [乘法运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Multiplication)
- [取余运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Remainder)
- [幂运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Exponentiation)
- [自增运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Increment)
- [自减运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Decrement)
- [一元减运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Unary_negation)
- [一元加运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Unary_plus)

---
# Source: index.md
---
---
title: function* 表达式
slug: Web/JavaScript/Reference/Operators/function*
---

**`function*`** 关键字可以在表达式内部定义一个生成器函数。

{{InteractiveExample("JavaScript Demo: Expressions - function* expression")}}

```js interactive-example
const foo = function* () {
  yield "a";
  yield "b";
  yield "c";
};

let str = "";
for (const val of foo()) {
  str = str + val;
}

console.log(str);
// Expected output: "abc"
```

## 语法

```plain
function* [name]([param1[, param2[, ..., paramN]]]) {
   statements
}
```

### 参数

- `name`
  - : 函数名。在声明*匿名函数*时可以省略。函数名称只是函数体中的一个本地变量。
- `paramN`
  - : 传入函数的一个参数名。一个函数最多有 255 个参数。
- `statements`
  - : 函数体。

## 描述

`function*`表达式和{{jsxref('Statements/function*', 'function* 声明')}}比较相似，并具有几乎相同的语法。`function*`表达式和`function*`声明之间主要区别就是函数名，即在创建匿名函数时，`function*`表达式可以省略函数名。阅读{{jsxref('Function', '函数')}}章节了解更多信息。

## 示例

下面的示例定义了一个未命名的生成器函数并把它赋值给`x`。函数产出它的传入参数的平方：

```js
var x = function* (y) {
  yield y * y;
};
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- {{jsxref("Statements/function*", "function*")}}
- {{jsxref("GeneratorFunction")}}
- [迭代器协议](/zh-CN/docs/Web/JavaScript/Reference/Iteration_protocols)
- {{jsxref("Operators/yield", "yield")}}
- {{jsxref("Operators/yield*", "yield*")}}

---
# Source: index.md
---
---
title: void 运算符
slug: Web/JavaScript/Reference/Operators/void
---

**`void` 运算符**对给定的表达式进行求值，然后返回 {{jsxref("undefined")}}。

{{InteractiveExample("JavaScript Demo: Expressions - void operator", "taller")}}

```js interactive-example
const output = void 1;
console.log(output);
// Expected output: undefined

void console.log("expression evaluated");
// Expected output: "expression evaluated"

void (function iife() {
  console.log("iife is executed");
})();
// Expected output: "iife is executed"

void function test() {
  console.log("test function executed");
};
try {
  test();
} catch (e) {
  console.log("test function is not defined");
  // Expected output: "test function is not defined"
}
```

## 语法

```js-nolint
void expression
```

## 描述

这个运算符允许在表达式执行完成时，产生（某些地方）期望获得的 {{jsxref("undefined")}} 值。

`void` 运算符通常只用于获取 `undefined` 的原始值，一般使用 `void(0)`（等同于 `void 0`）。在上述情况中，也可以使用全局变量 {{jsxref("undefined")}} 来代替。

需要注意考虑 `void` 运算符的[优先级](/zh-CN/docs/Web/JavaScript/Reference/Operators/Operator_precedence)，以下加括号的表达式的例子可以帮助你清楚地理解 `void` 操作符的优先级：

```js
void 2 === "2"; // (void 2) === '2'，返回 false
void (2 === "2"); // void (2 === '2')，返回 undefined
```

## 示例

### 立即调用的函数表达式

在使用[立即调用的函数表达式](/zh-CN/docs/Glossary/IIFE)时，`function` 关键字不可直接位于语句开头，因为该表达式会被解析为[函数声明](/zh-CN/docs/Web/JavaScript/Reference/Statements/function)，并会在解析到代表调用的括号时产生语法错误。如果是匿名函数，那么如果函数被解析为声明，就会立即产生语法错误。

```js example-bad
function iife() {
  console.log("Executed!");
}(); // SyntaxError: Unexpected token ')'

function () {
  console.log("Executed!");
}(); // SyntaxError: Function statements require a function name
```

为了使函数被解析为[表达式](/zh-CN/docs/Web/JavaScript/Reference/Operators/function)，`function` 关键字必须出现在一个只接受表达式而不是语句的位置。这可以通过在关键字前加一个[一元运算符](/zh-CN/docs/Web/JavaScript/Guide/Expressions_and_operators#一元运算符)来实现，它只接受表达式作为操作数。函数调用的[优先级](/zh-CN/docs/Web/JavaScript/Reference/Operators/Operator_precedence)比一元运算符高，所以它将被首先执行。它的返回值（几乎总是 `undefined`）将被传递给一元运算符，然后立即被丢弃。

在所有的一元运算符中，`void` 提供了最好的语义，因为它明确表示函数调用的返回值应该被丢弃。

```js
void (function () {
  console.log("Executed!");
})();

// Output: "Executed!"
```

这比用圆括号包裹函数表达式要长一些，圆括号的作用是强迫 `function` 关键字被解析为表达式的开始，而不是语句。

```js
(function () {
  console.log("Executed!");
})();
```

### JavaScript URI

当用户点击一个以 `javascript:` 开头的 URI 时，它会执行 URI 中的代码，然后用返回的值替换页面内容，除非返回的值是 {{jsxref("undefined")}}。`void` 运算符可用于返回 `undefined`。例如：

```html
<a href="javascript:void(0);"> 这个链接点击之后不会做任何事情 </a>

<a href="javascript:void(document.body.style.backgroundColor='green');">
  点击这个链接会让页面背景变成绿色。
</a>
```

> [!NOTE]
> 利用 `javascript:` 伪协议来执行 JavaScript 代码是不推荐的，推荐的做法是为链接元素绑定事件。

### 在箭头函数中避免泄漏

箭头函数标准中，允许在函数体不使用括号来直接返回值。如果右侧调用了一个原本没有返回值的函数，其返回值改变后，则会导致非预期的副作用。安全起见，当函数返回值不会被使用到的时候，应该使用 `void` 运算符，来确保 API 改变时，并不会改变箭头函数的行为。

```js
button.onclick = () => void doSomething();
```

这确保了当 `doSomething` 的返回值从 `undefined` 变为 `true` 的时候，不会改变代码的行为。

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- {{jsxref("undefined")}}

---
# Source: index.md
---
---
title: typeof
slug: Web/JavaScript/Reference/Operators/typeof
---

**`typeof`** 运算符返回一个字符串，表示操作数的类型。

{{InteractiveExample("JavaScript Demo: Expressions - typeof")}}

```js interactive-example
console.log(typeof 42);
// Expected output: "number"

console.log(typeof "blubber");
// Expected output: "string"

console.log(typeof true);
// Expected output: "boolean"

console.log(typeof undeclaredVariable);
// Expected output: "undefined"
```

## 语法

```js-nolint
typeof operand
```

### 参数

- `operand`
  - : 表示要返回类型的对象或[基本类型](/zh-CN/docs/Glossary/Primitive)的表达式。

## 描述

下表总结了 `typeof` 可能的返回值。有关类型和基本类型的更多信息，可查看 [JavaScript 数据结构](/zh-CN/docs/Web/JavaScript/Guide/Data_structures) 页面。

| 类型                                                                                                                                              | 结果                               |
| ------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------- |
| [Undefined](/zh-CN/docs/Glossary/Undefined)                                                                                                       | `"undefined"`                      |
| [Null](/zh-CN/docs/Glossary/Null)                                                                                                                 | `"object"`（[原因](#typeof_null)） |
| [Boolean](/zh-CN/docs/Glossary/Boolean)                                                                                                           | `"boolean"`                        |
| [Number](/zh-CN/docs/Glossary/Number)                                                                                                             | `"number"`                         |
| [BigInt](/zh-CN/docs/Glossary/BigInt)                                                                                                             | `"bigint"`                         |
| [String](/zh-CN/docs/Glossary/String)                                                                                                             | `"string"`                         |
| [Symbol](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Symbol)                                                                              | `"symbol"`                         |
| [Function](/zh-CN/docs/Glossary/Function)（在 ECMA-262 中实现 [[Call]]；[classes](/zh-CN/docs/Web/JavaScript/Reference/Statements/class)也是函数) | `"function"`                       |
| 其他任何对象                                                                                                                                      | `"object"`                         |

这个值列表是详尽的。没有符合规范的引擎曾被报告过产生（或历史上产生过）除列出的值之外的值。在规范删除 `typeof` 为不可调用的非标准外来对象返回实现定义的字符串的行为之前，旧的 Internet Explorer 是已知的唯一一个[实现额外返回值](https://github.com/tc39/ecma262/issues/1440#issuecomment-461963872)的浏览器。

## 示例

### 基本用法

```js
// 数值
typeof 37 === "number";
typeof 3.14 === "number";
typeof 42 === "number";
typeof Math.LN2 === "number";
typeof Infinity === "number";
typeof NaN === "number"; // 尽管它是 "Not-A-Number" (非数值) 的缩写
typeof Number(1) === "number"; // Number 会尝试把参数解析成数值
typeof Number("shoe") === "number"; // 包括不能将类型强制转换为数字的值

typeof 42n === "bigint";

// 字符串
typeof "" === "string";
typeof "bla" === "string";
typeof `template literal` === "string";
typeof "1" === "string"; // 注意内容为数字的字符串仍是字符串
typeof typeof 1 === "string"; // typeof 总是返回一个字符串
typeof String(1) === "string"; // String 将任意值转换为字符串，比 toString 更安全

// 布尔值
typeof true === "boolean";
typeof false === "boolean";
typeof Boolean(1) === "boolean"; // Boolean() 会基于参数是真值还是虚值进行转换
typeof !!1 === "boolean"; // 两次调用 !（逻辑非）运算符相当于 Boolean()

// Symbols
typeof Symbol() === "symbol";
typeof Symbol("foo") === "symbol";
typeof Symbol.iterator === "symbol";

// Undefined
typeof undefined === "undefined";
typeof declaredButUndefinedVariable === "undefined";
typeof undeclaredVariable === "undefined";

// 对象
typeof { a: 1 } === "object";

// 使用 Array.isArray 或者 Object.prototype.toString.call
// 区分数组和普通对象
typeof [1, 2, 4] === "object";

typeof new Date() === "object";
typeof /regex/ === "object";

// 下面的例子令人迷惑，非常危险，没有用处。避免使用它们。
typeof new Boolean(true) === "object";
typeof new Number(1) === "object";
typeof new String("abc") === "object";

// 函数
typeof function () {} === "function";
typeof class C {} === "function";
typeof Math.sin === "function";
```

### typeof null

```js
// JavaScript 诞生以来便如此
typeof null === "object";
```

在 JavaScript 最初的实现中，JavaScript 中的值是由一个表示类型的标签和实际数据值表示的。对象的类型标签是 0。由于 `null` 代表的是空指针（大多数平台下值为 0x00），因此，null 的类型标签是 0，`typeof null` 也因此返回 `"object"`。（[参考来源](https://www.2ality.com/2013/10/typeof-null.html)）

曾有一个 ECMAScript 的修复提案（通过选择性加入的方式），但[被拒绝了](http://wiki.ecmascript.org/doku.php?id=harmony:typeof_null)。该提案会导致 `typeof null === 'null'`。

### 使用 new 操作符

所有使用 [`new`](/zh-CN/docs/Web/JavaScript/Reference/Operators/new) 调用的构造函数都将返回非基本类型（`"object"` 或 `"function"`）。大多数返回对象，但值得注意的例外是 [`Function`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Function)，它返回一个函数。

```js
const str = new String("String");
const num = new Number(100);

typeof str; // "object"
typeof num; // "object"

const func = new Function();

typeof func; // "function"
```

### 语法中需要圆括号

`typeof` 操作符的[优先级](/zh-CN/docs/Web/JavaScript/Reference/Operators/Operator_precedence)高于加法（`+`）等二进制操作符。因此，需要用括号来计算加法结果的类型。

```js
// 括号有无将决定表达式的类型。
const someData = 99;

typeof someData + " Wisen"; // "number Wisen"
typeof (someData + " Wisen"); // "string"
```

### 与未声明和未初始化变量的交互

`typeof` 通常总是保证为它提供的任何操作数返回一个字符串。即使使用未声明的标识符，`typeof` 也会返回 `"undefined"`，而不是抛出错误。

```js
typeof undeclaredVariable; // "undefined"
```

但在加入了块级作用域的 [let](/zh-CN/docs/Web/JavaScript/Reference/Statements/let) 和 [const](/zh-CN/docs/Web/JavaScript/Reference/Statements/const) 之后，在其被声明之前对块中的 `let` 和 `const` 变量使用 `typeof` 会抛出一个 [ReferenceError](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/ReferenceError)。块作用域变量在块的头部处于“[暂存死区](/zh-CN/docs/Web/JavaScript/Reference/Statements/let#temporal_dead_zone_and_errors_with_let)”，直至其被初始化，在这期间，访问变量将会引发错误。

```js example-bad
typeof newLetVariable; // ReferenceError
typeof newConstVariable; // ReferenceError
typeof newClass; // ReferenceError

let newLetVariable;
const newConstVariable = "hello";
class newClass {}
```

### document.all 的异常行为

当前所有浏览器都公开了一个类型为 `undefined` 的非标准宿主对象 [`Document.All`](/zh-CN/docs/Web/API/Document/all)。

```js
typeof document.all === "undefined";
```

虽然 `document.all` 也是[假值](/zh-CN/docs/Glossary/Falsy)，与 `undefined` [非严格相等](/zh-CN/docs/Web/JavaScript/Reference/Operators/Equality)，但它不是 [`undefined`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/undefined)。在 Web 标准中，`document.all` 具有 `"undefined"` 类型的情况被归类为“故意违反”原始 ECMAScript Web 兼容性标准。

### 获取具体类型的自定义方法

`typeof` 是非常有用的，但它不像需要的那样万能。例如，`typeof []` 是 `"object"`，以及 `typeof new Date()`、`typeof /abc/` 等。

为了更明确地检查类型，这里我们提供了一个自定义的 `type(value)` 函数，它主要模仿 `typeof` 的行为，但对于非基本类型（即对象和函数），它在可能的情况下返回更详细的类型名。

```js
function type(value) {
  if (value === null) {
    return "null";
  }
  const baseType = typeof value;
  // 基本类型
  if (!["object", "function"].includes(baseType)) {
    return baseType;
  }

  // Symbol.toStringTag 通常指定对象类的“display name”
  // 它在 Object.prototype.toString() 中使用。
  const tag = value[Symbol.toStringTag];
  if (typeof tag === "string") {
    return tag;
  }

  // 如果它是一个函数，其源代码以 "class" 关键字开头
  if (
    baseType === "function" &&
    Function.prototype.toString.call(value).startsWith("class")
  ) {
    return "class";
  }

  // 构造函数的名称；例如 `Array`、`GeneratorFunction`、`Number`、`String`、`Boolean` 或 `MyCustomClass`
  const className = value.constructor.name;
  if (typeof className === "string" && className !== "") {
    return className;
  }

  // 在这一点上，没有合适的方法来获取值的类型，因此我们使用基本实现。
  return baseType;
}
```

要检查可能不存在的变量，否则会抛出 {{JSxRef("ReferenceError")}}，请使用 `typeof nonExistentVar === 'undefined'`，因为自定义代码无法模仿这种行为。

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- {{JSxRef("Operators/instanceof", "instanceof")}}
- [`document.all` willful violation of the standard](https://github.com/tc39/ecma262/issues/668)

---
# Source: index.md
---
---
title: 空值合并运算符（??）
slug: Web/JavaScript/Reference/Operators/Nullish_coalescing
l10n:
  sourceCommit: 59a92ab5609f0a021602f11843f3b00b16e67e6d
---

**空值合并运算符**（**`??`**）是一个逻辑运算符，当左侧的操作数为 [`null`](/zh-CN/docs/Web/JavaScript/Reference/Operators/null) 或者 {{jsxref("undefined")}} 时，返回其右侧操作数，否则返回左侧操作数。

{{InteractiveExample("JavaScript Demo: Expressions - Nullish coalescing operator")}}

```js interactive-example
const foo = null ?? "default string";
console.log(foo);
// Expected output: "default string"

const baz = 0 ?? 42;
console.log(baz);
// Expected output: 0
```

## 语法

```js-nolint
leftExpr ?? rightExpr
```

## 描述

空值合并运算符可以视为[逻辑或运算符（`||`）](/zh-CN/docs/Web/JavaScript/Reference/Operators/Logical_OR)的特例。后者在左侧操作数为*任何*{{Glossary("Falsy", "假值")}}时返回右侧操作数，而不仅仅是 `null` 或 `undefined`。换句话说，如果你使用 `||` 为另一个变量 `foo` 提供某些默认值，而你将某些假值视为可用值（例如 `''` 或 `0`），则可能会遇到意外的行为。更多示例参见[下方](#为变量赋默认值)。

空值合并运算符的[运算符优先级](/zh-CN/docs/Web/JavaScript/Reference/Operators/Operator_precedence)是第五低的，直接低于 `||` 且直接高于[条件（三元）运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Conditional_operator)。

将 `??` 直接与逻辑与（`&&`）和逻辑或（`||`）运算符组合使用是不可取的。这种情况下会抛出[语法错误](/zh-CN/docs/Web/JavaScript/Reference/Errors/Cant_use_nullish_coalescing_unparenthesized)。

```js-nolint example-bad
null || undefined ?? "foo"; // 抛出 SyntaxError
true && undefined ?? "foo"; // 抛出 SyntaxError
```

相反，请提供括号以明确表示优先级：

```js example-good
(null || undefined) ?? "foo"; // 返回“foo”
```

## 示例

### 使用空值合并运算符

在这个例子中，我们使用空值合并运算符为常量提供默认值，保证常量不为 `null` 或者 `undefined`。

```js
const nullValue = null;
const emptyText = ""; // 假值
const someNumber = 42;

const valA = nullValue ?? "valA 的默认值";
const valB = emptyText ?? "valB 的默认值";
const valC = someNumber ?? 0;

console.log(valA); // "valA 的默认值"
console.log(valB); // ""（空字符串虽然是假值，但不是 null 或者 undefined）
console.log(valC); // 42
```

### 为变量赋默认值

以前，如果想为一个变量赋默认值，通常的做法是使用逻辑或运算符（[`||`](/zh-CN/docs/Web/JavaScript/Reference/Operators/Logical_OR)）：

```js
let foo;

// foo 从未被赋予任何值，因此它仍然是未定义的
let someDummyText = foo || "Hello!";
```

然而，由于 `||` 是一个布尔逻辑运算符，左侧的操作数会被强制转换成布尔值用于求值。任何*假值*（`0`、`''`、`NaN`、`false`等等）都不会被返回。如果你使用 `0`、`''` 或 `NaN` 作为有效值，就会出现不可预料的后果。

```js
const count = 0;
const text = "";

const qty = count || 42;
const message = text || "hi!";
console.log(qty); // 42，而不是 0
console.log(message); // "hi!"，而不是 ""
```

空值合并运算符可以避免这种陷阱，其只在第一个操作数为 `null` 或 `undefined` 时（而不是其他假值）返回第二个操作数：

```js
const myText = ""; // 空字符串（其也是假值）

const notFalsyText = myText || "Hello world";
console.log(notFalsyText); // Hello world

const preservingFalsy = myText ?? "Hi neighborhood";
console.log(preservingFalsy); // ''（myText 既不是 undefined 也不是 null）
```

### 短路

与 OR 和 AND 逻辑运算符相似，当左表达式不为 `null` 或 `undefined` 时，不会对右表达式进行求值。

```js
function A() {
  console.log("函数 A 被调用了");
  return undefined;
}
function B() {
  console.log("函数 B 被调用了");
  return false;
}
function C() {
  console.log("函数 C 被调用了");
  return "foo";
}

console.log(A() ?? C());
// 依次打印 "函数 A 被调用了"、"函数 C 被调用了"、"foo"
// A() 返回了 undefined，所以运算符两边的表达式都被执行了

console.log(B() ?? C());
// 依次打印 "函数 B 被调用了"、"false"
// B() 返回了 false（既不是 null 也不是 undefined）
// 所以右侧表达式没有被执行
```

### 与可选链运算符（`?.`）的关系

空值合并运算符将 `undefined` 与 `null` 视为特殊值，[可选链运算符（`?.`）](/zh-CN/docs/Web/JavaScript/Reference/Operators/Optional_chaining)也是如此。该运算符在访问可能为 `null` 或 `undefined` 的对象属性时非常有用。将这两者结合，可以安全地访问可能为空值的对象属性，并在其为空值时提供默认值。

```js
const foo = { someFooProp: "hi" };

console.log(foo.someFooProp?.toUpperCase() ?? "not available"); // "HI"
console.log(foo.someBarProp?.toUpperCase() ?? "not available"); // "not available"
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- [逻辑空赋值运算符（`??=`）](/zh-CN/docs/Web/JavaScript/Reference/Operators/Nullish_coalescing_assignment)
- [可选链运算符（`?.`）](/zh-CN/docs/Web/JavaScript/Reference/Operators/Optional_chaining)
- [逻辑或运算符（`||`）](/zh-CN/docs/Web/JavaScript/Reference/Operators/Logical_OR)
- [默认参数](/zh-CN/docs/Web/JavaScript/Reference/Functions/Default_parameters)

---
# Source: index.md
---
---
title: 不相等（!=）
slug: Web/JavaScript/Reference/Operators/Inequality
---

不相等运算符（`!=`）检查其两个操作数是否不相等，并返回布尔结果。与[严格不相等](/zh-CN/docs/Web/JavaScript/Reference/Operators/Strict_inequality)运算符不同，它会转换并比较不同类型的操作数。

{{InteractiveExample("JavaScript Demo: Expressions - Inequality operator")}}

```js interactive-example
console.log(1 != 1);
// Expected output: false

console.log("hello" != "hello");
// Expected output: false

console.log("1" != 1);
// Expected output: false

console.log(0 != false);
// Expected output: false
```

## 语法

```js-nolint
x != y
```

## 描述

不等式运算符检查其操作数是否不相等。这是[相等](/zh-CN/docs/Web/JavaScript/Reference/Operators/Equality)运算符的否定，因此以下两行将始终给出相同的结果：

```js
x != y;

!(x == y);
```

有关比较算法的详细信息，请参见[相等](/zh-CN/docs/Web/JavaScript/Reference/Operators/Equality)运算符的页面。

与相等运算符一样，不相等运算符将尝试转换和比较不同类型的操作数：

```js
3 != "3"; // false
```

为避免这种情况，并要求将不同类型视为不同，请使用[严格不相等](/zh-CN/docs/Web/JavaScript/Reference/Operators/Strict_inequality)运算符：

```js
3 !== "3"; // true
```

## 示例

### 没有类型转换的比较

```js
1 != 2; // true
"hello" != "hola"; // true

1 != 1; // false
"hello" != "hello"; // false
```

### 有类型转换的比较

```js
"1" != 1; // false
1 != "1"; // false
0 != false; // false
0 != null; // true
0 != undefined; // true
0 != !!null; // false，看看逻辑非运算符
0 != !!undefined; // false，看看逻辑非运算符
null != undefined; // false

const number1 = new Number(3);
const number2 = new Number(3);
number1 != 3; // false
number1 != number2; // true
```

### 比较对象

```js
const object1 = {
  key: "value",
};

const object2 = {
  key: "value",
};

console.log(object1 != object2); // true
console.log(object1 != object1); // false
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- [相等运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Equality)
- [严格相等运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Strict_equality)
- [严格不相等运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Strict_inequality)

---
# Source: index.md
---
---
title: super
slug: Web/JavaScript/Reference/Operators/super
---

**super** 关键字用于访问对象字面量或类的原型（[[Prototype]]）上的属性，或调用父类的构造函数。

`super.prop` 和 `super[expr]` 表达式在[类](/zh-CN/docs/Web/JavaScript/Reference/Classes)和[对象字面量](/zh-CN/docs/Web/JavaScript/Reference/Operators/Object_initializer)任何[方法定义](/zh-CN/docs/Web/JavaScript/Reference/Functions/Method_definitions)中都是有效的。`super(...args)` 表达式在类的构造函数中有效。

## 语法

```js-nolint
super([arguments]) // 调用父类的构造函数
super.propertyOnParent
super[expression]
```

## 描述

`super` 关键字有两种使用方式：作为“函数调用”（`super(...args)`），或作为“属性查询”（`super.prop` 和 `super[expr]`）。

> [!NOTE]
> `super` 是一个关键字，并且有一些特殊的语法结构。`super` 不是一个指向原型对象的变量。试图读取 `super` 本身会导致 {{jsxref("SyntaxError")}}。
>
> ```js example-bad
> const child = {
>   myParent() {
>     console.log(super); // SyntaxError: 'super' keyword unexpected here
>   },
> };
> ```

在派生类的构造函数体中（使用 `extends`），`super` 关键字可以作为“函数调用”（`super(...args)`）出现，它必须在使用 `this` 关键字之前和构造函数返回之前被调用。它调用父类的构造函数并绑定父类的公共字段，之后派生类的构造函数可以进一步访问和修改 `this`。

“属性查询”形式可以用来访问一个对象字面或类的 [[Prototype]] 的方法和属性。在一个类的主体中，`super` 的引用可以是父类的构造函数本身，也可以是构造函数的 `prototype`，这取决于执行环境是实例创建还是类的初始化。更多细节请参见示例部分。

注意，`super` 的引用是由 `super` 声明的类或对象字面决定的，而不是方法被调用的对象。因此，取消绑定或重新绑定一个方法并不会改变其中 `super` 的引用（尽管它们会改变 [`this`](/zh-CN/docs/Web/JavaScript/Reference/Operators/this) 的引用）。你可以把 `super` 看作是类或对象字面范围内的一个变量，这些方法在它上面创建了一个闭包。(但也要注意，它实际上并不是一个变量，正如上面所解释的那样)。

当通过 `super` 设置属性时，该属性将被设置在 `this` 上。

## 示例

### 在类中使用 `super`

以下代码片段来自于 [classes sample](https://github.com/GoogleChrome/samples/blob/gh-pages/classes-es6/index.html)（[在线演示](https://googlechrome.github.io/samples/classes-es6/index.html)）。这里调用 `super()` 是为了避免重复在 `Rectangle` 与 `Square` 的构造函数之间共同的部分。

```js
class Polygon {
  constructor(height, width) {
    this.name = "Rectangle";
    this.height = height;
    this.width = width;
  }
  sayName() {
    console.log("Hi, I am a ", this.name + ".");
  }
  get area() {
    return this.height * this.width;
  }
  set area(value) {
    this._area = value;
  }
}

class Square extends Polygon {
  constructor(length) {
    this.height; // ReferenceError，super 需要先被调用！

    // 这里，它调用父类的构造函数并传入 length
    // 作为 Polygon 的 height, width
    super(length, length);

    // 注意：在派生的类中，在你可以使用 'this' 之前，必须先调用 super()。
    // 现在可以使用 'this' 了，忽略 'this' 将导致引用错误（ReferenceError）
    this.name = "Square";
  }
}
```

### 调用父类上的静态方法

你也可以用 `super` 调用父类的[静态](/zh-CN/docs/Web/JavaScript/Reference/Classes/static)方法。

```js
class Rectangle {
  static logNbSides() {
    return "I have 4 sides";
  }
}

class Square extends Rectangle {
  static logDescription() {
    return `${super.logNbSides()} which are all equal`;
  }
}
Square.logDescription(); // 'I have 4 sides which are all equal'
```

### 在类字段声明中访问 super

`super` 也可以在类字段初始化时被访问。`super` 的引用取决于当前字段是一个实例字段还是一个静态字段。

```js
class Base {
  static baseStaticField = 90;
  baseMethod() {
    return 10;
  }
}
class Extended extends Base {
  extendedField = super.baseMethod(); // 10
  static extendedStaticField = super.baseStaticField; // 90
}
```

注意，实例字段是在实例上设置的，而不是在构造函数的原型上，所以你不能用 `super` 来访问父类的实例字段。

```js example-bad
class Base {
  baseField = 10;
}
class Extended extends Base {
  extendedField = super.baseField; // undefined
}
```

在这里，`extendedField` 是 `undefined` 而不是 10，因为 `baseField` 被定义为 `Base` 实例的自有属性，而不是 `Base.prototype`。在这种情况下，`super` 只查找 `Base.prototype` 的属性，因为它是 `Extended.prototype` 的 [[Prototype]]。

### 删除 super 上的属性将抛出异常

你不能使用 [delete 操作符](/zh-CN/docs/Web/JavaScript/Reference/Operators/delete)加 `super.prop` 或者 `super[expr]` 去删除父类的属性，这样做会抛出 {{jsxref("ReferenceError")}}。

```js
class Base {
  foo() {}
}
class Derived extends Base {
  delete() {
    delete super.foo; // 这很糟糕
  }
}

new Derived().delete(); // ReferenceError: invalid delete involving 'super'.
```

### 在对象字面量中使用 super.prop

`super` 也可以在[对象初始化器/对象字面量](/zh-CN/docs/Web/JavaScript/Reference/Operators/Object_initializer)符号中使用。在这个例子中，两个对象定义了一个方法。在第二个对象中，`super` 调用第一个对象的方法。这是在 {{jsxref("Object.setPrototypeOf()")}} 的帮助下实现的，我们将 `obj2` 的原型设置为 `obj1`，这样 `super` 就能够在 `obj1` 上找到 `method1`。

```js
const obj1 = {
  method1() {
    console.log("method 1");
  },
};
const obj2 = {
  method2() {
    super.method1();
  },
};
Object.setPrototypeOf(obj2, obj1);
obj2.method2(); // logs "method 1"
```

### 读取 super.prop 的方法在绑定到其他对象时不会有不同的表现

访问 `super.x` 的行为类似于 `Reflect.get(Object.getPrototypeOf(objectLiteral), "x", this)`，这意味着该属性总是在对象字面/类声明的原型上寻找，取消绑定和重新绑定方法不会改变 `super` 的引用。

```js
class Base {
  baseGetX() {
    return 1;
  }
}
class Extended extends Base {
  getX() {
    return super.baseGetX();
  }
}
const e = new Extended();
console.log(e.getX()); // 1
const { getX } = e;
console.log(getX()); // 1
```

同样的情况也发生在对象字面量中。

```js
const parent1 = { prop: 1 };
const parent2 = { prop: 2 };
const child = {
  myParent() {
    console.log(super.prop);
  },
};
Object.setPrototypeOf(child, parent1);
child.myParent(); // 打印 "1"
const myParent = child.myParent;
myParent(); // 依然打印 "1"
const anotherChild = { __proto__: parent2, myParent };
anotherChild.myParent(); //依然打印 "1"
```

只有重设整个继承链才能改变 `super` 的引用。

```js
class Base {
  baseGetX() {
    return 1;
  }
  static staticBaseGetX() {
    return 3;
  }
}
class AnotherBase {
  baseGetX() {
    return 2;
  }
  static staticBaseGetX() {
    return 4;
  }
}
class Extended extends Base {
  getX() {
    return super.baseGetX();
  }
  static staticGetX() {
    return super.staticBaseGetX();
  }
}
const e = new Extended();
// 重置实例部分的继承
Object.setPrototypeOf(Extended.prototype, AnotherBase.prototype);
console.log(e.getX()); // 打印 "2" 而不是 "1", 因为原型链已经改变
console.log(Extended.staticGetX()); // 依然打印 "3", 因为我们还没有修改静态部分。
// 重置静态部分的继承
Object.setPrototypeOf(Extended, AnotherBase);
console.log(Extended.staticGetX()); //现在打印 "4"
```

### 设置 super.prop 将在此基础上设置属性

设置 `super` 的属性，比如 `super.x = 1`，就像 `Reflect.set(Object.getPrototypeOf(objectLiteral), "x", 1, this)` 的行为。这是一个将 `super` 简单理解为“原型对象的引用”的情况，因为它实际上是在 `this` 上设置属性。

```js
class A {}
class B extends A {
  setX() {
    super.x = 1;
  }
}
const b = new B();
b.setX();
console.log(b); // B { x: 1 }
console.log(Object.hasOwn(b, "x")); // true
```

`super.x = 1` 将在 `A.prototype` 上寻找 `x` 的属性描述符（并调用那里定义的 setter），但 `this` 的值将被设置为 `this`，在这种情况下就是 `b`。你可以阅读 [`Reflect.set`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Reflect/set) 以了解更多关于 `target` 和 `receiver` 不同情况的细节。

这意味着，虽然 _get_ `super.prop` 的方法通常不会受到 `this` 上下文的影响，但 _set_ `super.prop` 的方法却容易受到影响。

```js example-bad
/* Reusing same declarations as above */
const b2 = new B();
b2.setX.call(null); // TypeError: Cannot assign to read only property 'x' of object 'null'
```

然而，`super.x = 1` 仍然会查询原型对象的属性描述符，这意味着你不能重写不可写的属性，而且 setter 会被调用。

```js
class X {
  constructor() {
    // Create a non-writable property
    Object.defineProperty(this, "prop", {
      configurable: true,
      writable: false,
      value: 1,
    });
  }
}
class Y extends X {
  constructor() {
    super();
  }
  foo() {
    super.prop = 2; // Cannot overwrite the value.
  }
}
const y = new Y();
y.foo(); // TypeError: "prop" is read-only
console.log(y.prop); // 1
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- [类](/zh-CN/docs/Web/JavaScript/Reference/Classes)

---
# Source: index.md
---
---
title: 条件（三元）运算符
slug: Web/JavaScript/Reference/Operators/Conditional_operator
---

**条件（三元）运算符**是 JavaScript 唯一使用三个操作数的运算符：一个条件后跟一个问号（`?`），如果条件为{{Glossary("truthy", "真值")}}，则执行冒号（`:`）前的表达式；若条件为{{Glossary("falsy", "假值")}}，则执行最后的表达式。该运算符经常当作 [`if...else`](/zh-CN/docs/Web/JavaScript/Reference/Statements/if...else) 语句的简捷形式来使用。

{{InteractiveExample("JavaScript Demo: Expressions - Conditional operator")}}

```js interactive-example
function getFee(isMember) {
  return isMember ? "$2.00" : "$10.00";
}

console.log(getFee(true));
// Expected output: "$2.00"

console.log(getFee(false));
// Expected output: "$10.00"

console.log(getFee(null));
// Expected output: "$10.00"
```

## 语法

```js-nolint
condition ? exprIfTrue : exprIfFalse
```

### 参数

- `condition`
  - : 计算结果用作条件的表达式。
- `exprIfTrue`
  - : 如果 `condition` 的计算结果为{{Glossary("truthy", "真值")}}（等于或可以转换为 `true` 的值），则执行该表达式。
- `exprIfFalse`
  - : 如果 `condition` 为{{Glossary("falsy", "假值")}}（等于或可以转换为 `false` 的值）时执行的表达式。

## 描述

除了 `false`，可能的假值表达式还有：`null`、`NaN`、`0`、空字符串（`""`）和 `undefined`。如果 `condition` 是其中任何一个，那么条件表达式的结果就是 `exprIfFalse` 表达式执行的结果。

## 示例

### 简单的例子

```js
const age = 26;
const beverage = age >= 21 ? "Beer" : "Juice";
console.log(beverage); // "Beer"
```

### 处理 null 值

一个常见的用法是处理可能为 `null` 的值：

```js
const greeting = (person) => {
  const name = person ? person.name : "stranger";
  return `Howdy, ${name}`;
};

console.log(greeting({ name: "Alice" })); // "Howdy, Alice"
console.log(greeting(null)); // "Howdy, stranger"
```

### 条件链

三元运算符是右结合的，这意味着它可以按以下方式“链接”起来，类似于 `if … else if … else if … else` 链：

```js
function example() {
  return condition1
    ? value1
    : condition2
      ? value2
      : condition3
        ? value3
        : value4;
}
```

这等价于以下 [`if...else`](/zh-CN/docs/Web/JavaScript/Reference/Statements/if...else) 链。

```js
function example() {
  if (condition1) {
    return value1;
  } else if (condition2) {
    return value2;
  } else if (condition3) {
    return value3;
  } else {
    return value4;
  }
}
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- [if 语句](/zh-CN/docs/Web/JavaScript/Reference/Statements/if...else)
- [空值合并运算符（`??`）](/zh-CN/docs/Web/JavaScript/Reference/Operators/Nullish_coalescing)
- [可选链运算符（`?.`）](/zh-CN/docs/Web/JavaScript/Reference/Operators/Optional_chaining)
- [在代码中做决定——条件语句](/zh-CN/docs/Learn_web_development/Core/Scripting/Conditionals)
- [表达式与运算符](/zh-CN/docs/Web/JavaScript/Guide/Expressions_and_operators)

---
# Source: index.md
---
---
title: 按位与（&）
slug: Web/JavaScript/Reference/Operators/Bitwise_AND
---

**按位与**（**`&`**）运算符在两个操作数对应的二进位都为 `1` 时，该位的结果值才为 `1`。

{{InteractiveExample("JavaScript Demo: Expressions - Bitwise AND", "shorter")}}

```js interactive-example
const a = 5; // 00000000000000000000000000000101
const b = 3; // 00000000000000000000000000000011

console.log(a & b); // 00000000000000000000000000000001
// Expected output: 1
```

## 语法

```js-nolint
a & b
```

## 描述

操作数被转换为 32 位整数，并由一系列位（0 和 1）表示。超过 32 位的数字将丢弃其最高有效位。例如，以下大于 32 位的整数将被转换为 32 位整数：

```plain
Before: 11100110111110100000000000000110000000000001
After:              10100000000000000110000000000001
```

第一个操作数中的每个位都与第二个操作数中的相应位配对：*第一位*到*第一位*，*第二位*到*第二位*，依此类推。

将运算符应用于每对位，然后按位构造结果。

与运算的真值表：

| a   | b   | a AND b |
| --- | --- | ------- |
| 0   | 0   | 0       |
| 0   | 1   | 0       |
| 1   | 0   | 0       |
| 1   | 1   | 1       |

```plain
     9 (base 10) = 00000000000000000000000000001001 (base 2)
    14 (base 10) = 00000000000000000000000000001110 (base 2)
                   --------------------------------
14 & 9 (base 10) = 00000000000000000000000000001000 (base 2) = 8 (base 10)
```

任何数字 `x` 与 `0` 进行按位与运算都会得到 `0`。

## 示例

### 使用按位与

```js
// 5: 00000000000000000000000000000101
// 2: 00000000000000000000000000000010
5 & 2; // 0
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- [JS 指南中的位运算符](/zh-CN/docs/Web/JavaScript/Guide/Expressions_and_operators#位运算符)
- [按位与赋值运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Bitwise_AND_assignment)

---
# Source: index.md
---
---
title: 相等（==）
slug: Web/JavaScript/Reference/Operators/Equality
l10n:
  sourceCommit: f616cb604af851f77f8cd59368e94ee3e43a8838
---

**相等**（**`==`**）运算符检查其两个操作数是否相等，返回一个布尔值结果。与[严格相等](/zh-CN/docs/Web/JavaScript/Reference/Operators/Strict_equality)运算符不同，它会尝试转换不同类型的操作数，并进行比较。

{{InteractiveExample("JavaScript Demo: Expressions - Equality operator")}}

```js interactive-example
console.log(1 == 1);
// Expected output: true

console.log("hello" == "hello");
// Expected output: true

console.log("1" == 1);
// Expected output: true

console.log(0 == false);
// Expected output: true
```

## 语法

```js-nolint
x == y
```

## 描述

相等运算符（`==` 和 `!=`）提供[非严格相等](/zh-CN/docs/Web/JavaScript/Guide/Equality_comparisons_and_sameness#使用_进行宽松相等比较)语义。这可以大致总结如下：

1. 如果操作数具有相同的类型，则按如下方式进行比较：
   - 对象（Object）：仅当两个操作数引用同一个对象时返回 `true`。
   - 字符串（String）：仅当两个操作数具有相同的字符且顺序相同时返回 `true`。
   - 数字（Number）：如果两个操作数的值相同，则返回 `true`。`+0` 和 `-0` 被视为相同的值。如果任何一个操作数是 `NaN`，返回 `false`；所以，`NaN` 永远不等于 `NaN`。
   - 布尔值（Boolean）：仅当操作数都为 `true` 或都为 `false` 时返回 `true`。
   - 大整型（BigInt）：仅当两个操作数的值相同时返回 `true`。
   - 符号（Symbol）：仅当两个操作数引用相同的符号时返回 `true`。
2. 如果其中一个操作数为 `null` 或 `undefined`，另一个操作数也必须为 `null` 或 `undefined` 以返回 `true`。否则返回 `false`。
3. 如果其中一个操作数是对象，另一个是原始值，则[将对象转换为原始值](/zh-CN/docs/Web/JavaScript/Guide/Data_structures#原始值强制转换)。
4. 在这一步，两个操作数都被转换为原始值（字符串、数字、布尔值、符号和大整型中的一个）。剩余的转换将分情况完成。
   - 如果是相同的类型，使用步骤 1 进行比较。
   - 如果其中一个操作数是符号而另一个不是，返回 `false`。
   - 如果其中一个操作数是布尔值而另一个不是，则[将布尔值转换为数字](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Number#number_强制转换)：`true` 转换为 1，`false` 转换为 0。然后再次对两个操作数进行宽松比较。
   - 数字与字符串：[将字符串转换为数字](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Number#number_强制转换)。转换失败将导致 `NaN`，这将保证相等比较为 `false`。
   - 数字与大整型：按数值进行比较。如果数字的值为 ±∞ 或 `NaN`，返回 `false`。
   - 字符串与大整型：使用与 [`BigInt()`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/BigInt/BigInt) 构造函数相同的算法将字符串转换为大整型数。如果转换失败，返回 `false`。

宽松相等是*对称的*：`A == B` 对于 `A` 和 `B` 的任何值总是具有与 `B == A` 相同的语义（应用转换的顺序除外）。

该运算符与[严格相等](/zh-CN/docs/Web/JavaScript/Reference/Operators/Strict_equality)（`===`）运算符之间最显著的区别是，严格相等运算符不尝试类型转换。相反，严格相等运算符总是认为不同类型的操作数是不同的。严格相等运算符本质上只执行第 1 步，然后对所有其他情况返回 `false`。

上面的算法有一个“故意违反”：如果其中一个操作数是 [`document.all`](/zh-CN/docs/Web/API/Document/all)，则它被视为 `undefined`。这意味着 `document.all == null` 是 `true`，但 `document.all === undefined && document.all === null` 是 `false`。

## 示例

### 没有类型转换的比较

```js
1 == 1; // true
"hello" == "hello"; // true
```

### 有类型转换的比较

```js
"1" == 1; // true
1 == "1"; // true
0 == false; // true
0 == null; // false
0 == undefined; // false
0 == !!null; // true，看看逻辑非运算符
0 == !!undefined; // true，看看逻辑非运算符
null == undefined; // true

const number1 = new Number(3);
const number2 = new Number(3);
number1 == 3; // true
number1 == number2; // false
```

### 比较对象

```js
const object1 = {
  key: "value",
};

const object2 = {
  key: "value",
};

console.log(object1 == object2); // false
console.log(object1 == object1); // true
```

### 比较字符串和 String 对象

请注意，使用 `new String()` 构造的字符串是对象。如果将其中之一与字符串字面量进行比较，则该 `String` 对象将被转换为字符串字面量并对其内容进行比较。但是，如果两个操作数都是 `String` 对象，则将它们作为对象进行比较，并且必须引用相同的对象才会相等：

```js
const string1 = "hello";
const string2 = String("hello");
const string3 = new String("hello");
const string4 = new String("hello");

console.log(string1 == string2); // true
console.log(string1 == string3); // true
console.log(string2 == string3); // true
console.log(string3 == string4); // false
console.log(string4 == string4); // true
```

### 比较日期和字符串

```js
const d = new Date("December 17, 1995 03:24:00");
const s = d.toString(); // 例如：“Sun Dec 17 1995 03:24:00 GMT+0800 (中国标准时间)”
console.log(d == s); // true
```

### 比较数组和字符串

```js
const a = [1, 2, 3];
const b = "1,2,3";
a == b; // true，`a` 转换为字符串

const c = [true, 0.5, "hey"];
const d = c.toString(); // "true,0.5,hey"
c == d; // true
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- [不相等（`!=`）](/zh-CN/docs/Web/JavaScript/Reference/Operators/Inequality)
- [严格相等（`===`）](/zh-CN/docs/Web/JavaScript/Reference/Operators/Strict_equality)
- [严格不相等（`!==`）](/zh-CN/docs/Web/JavaScript/Reference/Operators/Strict_inequality)

---
# Source: index.md
---
---
title: 逻辑与赋值（&&=）
slug: Web/JavaScript/Reference/Operators/Logical_AND_assignment
---

**逻辑与赋值**（`x &&= y`）运算仅在 `x` 为{{Glossary("truthy","真")}}值时为其赋值。

{{InteractiveExample("JavaScript Demo: Expressions - Logical AND assignment")}}

```js interactive-example
let a = 1;
let b = 0;

a &&= 2;
console.log(a);
// Expected output: 2

b &&= 2;
console.log(b);
// Expected output: 0
```

## 语法

```js-nolint
expr1 &&= expr2
```

## 描述

逻辑与的[_短路运算_](/zh-CN/docs/Web/JavaScript/Reference/Operators/Operator_precedence#短路运算)意味着 `x &&= y` 与下式等价：

```js
x && (x = y);
```

如果左操作数不为真值，则由于[逻辑与](/zh-CN/docs/Web/JavaScript/Reference/Operators/Logical_AND)运算符的短路运算，不进行赋值操作。例如，由于 `x` 为 `const`（常量），以下式子不会抛出错误：

```js
const x = 0;
x &&= 2;
```

也不会触发 setter 函数：

```js
const x = {
  get value() {
    return 0;
  },
  set value(v) {
    console.log("调用了 setter");
  },
};
x.value &&= 2;
```

实际上，如果 `x` 不为真值，则根本不会对 `y` 求值。

```js
const x = 0;
x &&= console.log("y 进行了求值");
// 什么都不会输出
```

## 示例

### 使用逻辑与赋值

```js
let x = 0;
let y = 1;

x &&= 0; // 0
x &&= 1; // 0
y &&= 1; // 1
y &&= 0; // 0
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- [逻辑与（&&）](/zh-CN/docs/Web/JavaScript/Reference/Operators/Logical_AND)
- [空值合并运算符（`??`）](/zh-CN/docs/Web/JavaScript/Reference/Operators/Nullish_coalescing)
- [按位与赋值（`&=`）](/zh-CN/docs/Web/JavaScript/Reference/Operators/Bitwise_AND_assignment)
- {{Glossary("Truthy","真值")}}
- {{Glossary("Falsy","假值")}}

---
# Source: index.md
---
---
title: yield*
slug: Web/JavaScript/Reference/Operators/yield*
---

**`yield*` 表达式**用于委托给另一个{{jsxref("Statements/function*", "generator")}} 或可迭代对象。

## 语法

```plain
 yield* [[expression]];
```

- `expression`
  - : 返回一个可迭代对象的表达式。

## 描述

`yield*` 表达式迭代操作数，并产生它返回的每个值。

`yield*` 表达式本身的值是当迭代器关闭时返回的值（即`done`为`true`时）。

## 示例

### 委托给其他生成器

以下代码中，`g1()` `yield` 出去的每个值都会在 `g2()` 的 `next()` 方法中返回，就像那些 `yield` 语句是写在 `g2()` 里一样。

```js
function* g1() {
  yield 2;
  yield 3;
  yield 4;
}

function* g2() {
  yield 1;
  yield* g1();
  yield 5;
}

var iterator = g2();

console.log(iterator.next()); // { value: 1, done: false }
console.log(iterator.next()); // { value: 2, done: false }
console.log(iterator.next()); // { value: 3, done: false }
console.log(iterator.next()); // { value: 4, done: false }
console.log(iterator.next()); // { value: 5, done: false }
console.log(iterator.next()); // { value: undefined, done: true }
```

### 委托给其他可迭代对象

除了生成器对象这一种可迭代对象，`yield*` 还可以 `yield` 其他任意的可迭代对象，比如说数组、字符串、`arguments` 对象等等。

```js
function* g3() {
  yield* [1, 2];
  yield* "34";
  yield* arguments;
}

var iterator = g3(5, 6);

console.log(iterator.next()); // { value: 1, done: false }
console.log(iterator.next()); // { value: 2, done: false }
console.log(iterator.next()); // { value: "3", done: false }
console.log(iterator.next()); // { value: "4", done: false }
console.log(iterator.next()); // { value: 5, done: false }
console.log(iterator.next()); // { value: 6, done: false }
console.log(iterator.next()); // { value: undefined, done: true }
```

### `yield*` 表达式的值

`yield*` 是一个表达式，不是语句，所以它会有自己的值。

```js
function* g4() {
  yield* [1, 2, 3];
  return "foo";
}

var result;

function* g5() {
  result = yield* g4();
}

var iterator = g5();

console.log(iterator.next()); // { value: 1, done: false }
console.log(iterator.next()); // { value: 2, done: false }
console.log(iterator.next()); // { value: 3, done: false }
console.log(iterator.next()); // { value: undefined, done: true },
// 此时 g4() 返回了 { value: "foo", done: true }

console.log(result); // "foo"
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- [迭代器协议](/zh-CN/docs/Web/JavaScript/Reference/Iteration_protocols)
- {{jsxref("Statements/function*", "function*")}}
- [`function*` 表达式](/zh-CN/docs/Web/JavaScript/Reference/Operators/function*)
- {{jsxref("Operators/yield", "yield")}}

---
# Source: index.md
---
---
title: 按位或赋值（|=）
slug: Web/JavaScript/Reference/Operators/Bitwise_OR_assignment
---

**按位或赋值**（**`|=`**) 运算符使用两个操作数的二进制表示，对它们执行按位或运算并将结果分配给变量。

{{InteractiveExample("JavaScript Demo: Expressions - Bitwise OR assignment", "shorter")}}

```js interactive-example
let a = 5; // 00000000000000000000000000000101
a |= 3; // 00000000000000000000000000000011

console.log(a); // 00000000000000000000000000000111
// Expected output: 7
```

## 语法

```js-nolint
x |= y // x = x | y
```

## 示例

### 使用按位或赋值

```js
let a = 5;
a |= 2; // 7
// 5: 00000000000000000000000000000101
// 2: 00000000000000000000000000000010
// -----------------------------------
// 7: 00000000000000000000000000000111
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- [JS 指南中的赋值运算符](/zh-CN/docs/Web/JavaScript/Guide/Expressions_and_operators#赋值运算符)
- [按位或运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Bitwise_OR)
- [逻辑或赋值（`||=`）](/zh-CN/docs/Web/JavaScript/Reference/Operators/Logical_OR_assignment)

---
# Source: index.md
---
---
title: 取余赋值（%=）
slug: Web/JavaScript/Reference/Operators/Remainder_assignment
---

**取余赋值**（**`%=`**）运算符将变量除以右操作数的值，并将余数赋值给该变量。

{{InteractiveExample("JavaScript Demo: Expressions - Remainder assignment operator")}}

```js interactive-example
let a = 3;

console.log((a %= 2));
// Expected output: 1

console.log((a %= 0));
// Expected output: NaN

console.log((a %= "hello"));
// Expected output: NaN
```

## 语法

```js-nolint
x %= y // x = x % y
```

## 示例

### 使用取余赋值

```js
let bar = 5;

bar %= 2; // 1
bar %= "foo"; // NaN
bar %= 0; // NaN
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- [JS 指南中的赋值运算符](/zh-CN/docs/Web/JavaScript/Guide/Expressions_and_operators#赋值运算符)
- [取余运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Remainder)

---
# Source: index.md
---
---
title: 除法赋值（/=）
slug: Web/JavaScript/Reference/Operators/Division_assignment
---

**除法赋值**（**`/=`**）运算符将变量除以右操作数的值，并将结果赋值给该变量。

{{InteractiveExample("JavaScript Demo: Expressions - Division assignment operator")}}

```js interactive-example
let a = 3;

a /= 2;
console.log(a);
// Expected output: 1.5

a /= 0;
console.log(a);
// Expected output: Infinity

a /= "hello";
console.log(a);
// Expected output: NaN
```

## 语法

```js-nolint
x /= y // x = x / y
```

## 示例

### 使用除法赋值

```js
let bar = 5;

bar /= 2; // 2.5
bar /= 2; // 1.25
bar /= 0; // Infinity
bar /= "foo"; // NaN
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- [JS 指南中的赋值运算符](/zh-CN/docs/Web/JavaScript/Guide/Expressions_and_operators#赋值运算符)
- [除法运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Division)

---
# Source: index.md
---
---
title: 按位与赋值（&=）
slug: Web/JavaScript/Reference/Operators/Bitwise_AND_assignment
---

按位与赋值运算符（`&=`）使用两个操作数的二进制表示，对它们进行按位与运算并将结果赋值给变量。

{{InteractiveExample("JavaScript Demo: Expressions - Bitwise AND assignment", "shorter")}}

```js interactive-example
let a = 5; // 00000000000000000000000000000101
a &= 3; // 00000000000000000000000000000011

console.log(a); // 00000000000000000000000000000001
// Expected output: 1
```

## 语法

```js-nolint
x &= y // x = x & y
```

## 示例

### 使用按位与赋值

```js
let a = 5;
// 5:     00000000000000000000000000000101
// 2:     00000000000000000000000000000010
a &= 2; // 0
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- [JS 指南中的赋值运算符](/zh-CN/docs/Web/JavaScript/Guide/Expressions_and_operators#赋值运算符)
- [按位与运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Bitwise_AND)

---
# Source: index.md
---
---
title: 逻辑或（||）
slug: Web/JavaScript/Reference/Operators/Logical_OR
---

对于一组操作数的**逻辑或**（`||`，逻辑析取）运算符，当且仅当其一个或多个操作数为真，其运算结果为真。它通常与布尔（逻辑）值一起使用。当它是布尔值时，返回一个布尔值。然而，`||` 运算符实际上是返回一个指定的操作数的值，所以如果这个运算符被用于非布尔值，它将返回一个非布尔值。

{{InteractiveExample("JavaScript Demo: Expressions - Logical OR", "shorter")}}

```js interactive-example
const a = 3;
const b = -2;

console.log(a > 0 || b > 0);
// Expected output: true
```

## 语法

```js-nolint
expr1 || expr2
```

## 描述

如果 `expr1` 能转化为 `true`，返回 `expr1`；否则返回 `expr2`。

能够转化为 `true` 的值叫做{{Glossary("truthy","真值")}}，能够转化为 `false` 的值叫做{{Glossary("falsy","假值")}}。

能够转化为 false 的表达式的示例如下：

- `null`；
- `NaN`；
- `0`；
- 空字符串（`""` 或 `''` 或 ` `` `）；
- `undefined`。

尽管 `||` 运算符可以与非布尔操作数一起使用，但它仍然被认为是一个布尔运算符，因为它的返回值总是可以被转换为[布尔基本类型](/zh-CN/docs/Web/JavaScript/Guide/Data_structures#boolean_类型)。要明确地将其返回值（或任何一般的表达式）转换为相应的布尔值，请使用双{{JSxRef("Operators/Logical_NOT", "非运算符", "", 1)}}或 {{jsxref("Global_Objects/Boolean/Boolean", "Boolean")}} 构造函数。

### 短路求值

逻辑或从左到右进行求值，它使用如下规则进行“短路”测试：

`(some truthy expression) || expr` 被短路评估为真值。

短路意味着上面的 `expr` 部分**不被求值**，因此不会发生任何副作用（例如，如果 `expr` 是一个函数调用，调用就不会发生）。这是因为在对第一个操作数进行评估后，操作数的值已经确定。参见下述示例：

```js
function A() {
  console.log("调用了 A");
  return false;
}
function B() {
  console.log("调用了 B");
  return true;
}

console.log(B() || A());
// 由于调用了 B 函数，故会输出 "called B" 到控制台，
// 然后输出 true（运算符的运算结果）
```

### 运算符优先级

以下表达式看起来等价，但实际上不是，因为 `&&` 运算符比 `||` 运算符先执行（参见[运算符优先级](/zh-CN/docs/Web/JavaScript/Reference/Operators/Operator_precedence)）。

```js-nolint
true || false && false; // 返回 true，因为 && 先执行
(true || false) && false; // 返回 false，因为分组运算符优先级更高
```

## 示例

### 使用或运算符

下列代码展示了 `||`（逻辑或）运算符的用法。

```js
true || true; // t || t returns true
false || true; // f || t returns true
true || false; // t || f returns true
false || 3 === 4; // f || f returns false
"Cat" || "Dog"; // t || t returns "Cat"
false || "Cat"; // f || t returns "Cat"
"Cat" || false; // t || f returns "Cat"
"" || false; // f || f returns false
false || ""; // f || f returns ""
false || varObject; // f || object returns varObject
```

> [!NOTE]
> 如果你使用这个操作符为某些变量提供默认值，要注意任何*假*值都不会被使用。如果你只需要过滤掉 [`null`](/zh-CN/docs/Web/JavaScript/Reference/Operators/null) 或 {{jsxref("undefined")}}，可以考虑使用[空值合并运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Nullish_coalescing)。

### 布尔值转化规则

#### 与运算符转化为或运算符

下述涉及到**布尔**运算符的运算：

```js-nolint
bCondition1 && bCondition2
```

总是与此表达式相同：

```js-nolint
!(!bCondition1 || !bCondition2)
```

#### 或运算符转化为与运算符

下述涉及到**布尔**运算符的运算：

```js-nolint
bCondition1 || bCondition2
```

总是与此表达式相同：

```js-nolint
!(!bCondition1 && !bCondition2)
```

### 去除嵌套的括号

由于逻辑表达式是从左到右进行求值的，只要遵循一定的规则，总是可以从一个复杂的表达式中删除括号。

下述涉及到**布尔**运算符的复杂运算：

```js-nolint
bCondition1 && (bCondition2 || bCondition3)
```

总是与此表达式相同：

```js-nolint
!(!bCondition1 || !bCondition2 && !bCondition3)
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- [空值合并运算符（`??`）](/zh-CN/docs/Web/JavaScript/Reference/Operators/Nullish_coalescing)
- {{jsxref("Boolean")}}
- {{Glossary("Truthy","真值")}}
- {{Glossary("Falsy","假值")}}

---
# Source: index.md
---
---
title: 大于（>）
slug: Web/JavaScript/Reference/Operators/Greater_than
---

大于运算符（`>`）在左操作数大于右操作数时返回 `true`，否则返回 `false`。

{{InteractiveExample("JavaScript Demo: Expressions - Greater than operator")}}

```js interactive-example
console.log(5 > 3);
// Expected output: true

console.log(3 > 3);
// Expected output: false

// Compare bigint to number
console.log(3n > 5);
// Expected output: false

console.log("ab" > "aa");
// Expected output: true
```

## 语法

```js-nolint
x > y
```

## 描述

操作数比较使用与[小于](/zh-CN/docs/Web/JavaScript/Reference/Operators/Less_than)运算符相同的算法，只是两个操作数交换了。

## 示例

### 字符串与字符串比较

```js
console.log("a" > "b"); // false
console.log("a" > "a"); // false
console.log("a" > "3"); // true
```

### 字符串与数值比较

```js
console.log("5" > 3); // true
console.log("3" > 3); // false
console.log("3" > 5); // false

console.log("hello" > 5); // false
console.log(5 > "hello"); // false

console.log("5" > 3n); // true
console.log("3" > 5n); // false
```

### 数值与数值比较

```js
console.log(5 > 3); // true
console.log(3 > 3); // false
console.log(3 > 5); // false
```

### 数值与大整型比较

```js
console.log(5n > 3); // true
console.log(3 > 5n); // false
```

### 比较 Boolean、null、undefined 和 NaN

```js
console.log(true > false); // true
console.log(false > true); // false

console.log(true > 0); // true
console.log(true > 1); // false

console.log(null > 0); // false
console.log(1 > null); // true

console.log(undefined > 3); // false
console.log(3 > undefined); // false

console.log(3 > NaN); // false
console.log(NaN > 3); // false
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- [大于等于运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Greater_than_or_equal)
- [小于运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Less_than)
- [小于等于运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Less_than_or_equal)

---
# Source: index.md
---
---
title: 按位或（|）
slug: Web/JavaScript/Reference/Operators/Bitwise_OR
---

**按位或**（**`|`**）运算符在其中一个或两个操作数对应的二进制位为 `1` 时，该位的结果值为 `1`。

{{InteractiveExample("JavaScript Demo: Expressions - Bitwise OR", "shorter")}}

```js interactive-example
const a = 5; // 00000000000000000000000000000101
const b = 3; // 00000000000000000000000000000011

console.log(a | b); // 00000000000000000000000000000111
// Expected output: 7
```

## 语法

```js-nolint
a | b
```

## 描述

操作数被转换为 32 位整数并由一系列二进制位（0 和 1）表示。超过 32 位的数字会丢弃其最高有效位。例如，以下超过 32 位的整数将被转换为 32 位整数：

```plain
Before: 11100110111110100000000000000110000000000001
After:              10100000000000000110000000000001
```

第一个操作数中的每个位都与第二个操作数中的相应位配对：*第一位*到*第一位*，*第二位*到*第二位*，依此类推。

运算符应用于每一对位，结果按位构造。

或运算的真值表为：

| a   | b   | a OR b |
| --- | --- | ------ |
| 0   | 0   | 0      |
| 0   | 1   | 1      |
| 1   | 0   | 1      |
| 1   | 1   | 1      |

```plain
     9 (base 10) = 00000000000000000000000000001001 (base 2)
    14 (base 10) = 00000000000000000000000000001110 (base 2)
                   --------------------------------
14 | 9 (base 10) = 00000000000000000000000000001111 (base 2) = 15 (base 10)
```

将任何数字 `x` 与 `0` 进行按位或运算得到 `x`。

## 示例

### 使用按位或

```js
// 9  (00000000000000000000000000001001)
// 14 (00000000000000000000000000001110)

14 | 9;
// 15 (00000000000000000000000000001111)
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- [JS 指南中的位运算符](/zh-CN/docs/Web/JavaScript/Guide/Expressions_and_operators#位运算符)
- [按位或赋值运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Bitwise_OR_assignment)

---
# Source: index.md
---
---
title: 可选链运算符（?.）
slug: Web/JavaScript/Reference/Operators/Optional_chaining
l10n:
  sourceCommit: 8cb0caef8175e1772f13ef7bc761f9616e2c5a4b
---

**可选链运算符（`?.`）** 用于访问对象的属性或调用函数。如果使用此运算符访问的对象或调用的函数是 {{jsxref("undefined")}} 或 [`null`](/zh-CN/docs/Web/JavaScript/Reference/Operators/null)，则表达式会短路并计算为 {{jsxref("undefined")}}，而不是抛出错误。

{{InteractiveExample("JavaScript Demo: Expressions - Optional chaining operator", "taller")}}

```js interactive-example
const adventurer = {
  name: "Alice",
  cat: {
    name: "Dinah",
  },
};

const dogName = adventurer.dog?.name;
console.log(dogName);
// Expected output: undefined

console.log(adventurer.someNonExistentMethod?.());
// Expected output: undefined
```

## 语法

```js-nolint
obj.val?.prop
obj.val?.[expr]
obj.func?.(args)
```

## 描述

`?.` 运算符与 `.` 链式运算符相似，不同之处在于，如果引用是[空值](/zh-CN/docs/Glossary/Nullish)（[`null`](/zh-CN/docs/Web/JavaScript/Reference/Operators/null) 或 {{jsxref("undefined")}}），它不会导致错误，而是使表达式短路并返回 `undefined`。当用于函数调用时，如果给定函数不存在，它也会返回 `undefined`。

当访问链式属性时，如果存在引用可能缺失的情况，这将使表达式更简洁、更简短。在探索对象内容且无法确定哪些属性是必需的时，它也会很有帮助。

例如，考虑一个具有嵌套结构的对象 `obj`。如果没有可选链，查找深层嵌套的子属性需要验证中间的引用，例如：

```js
const nestedProp = obj.first && obj.first.second;
```

在访问 `obj.first.second` 之前，要保证 `obj.first` 的值不是 `null`（也不是 `undefined`）。这样做可以避免在不对 `obj.first` 进行校验情况下直接访问 `obj.first.second` 而可能引发的错误。

这是 JavaScript 中的一个惯用模式，但当链很长时，它会变得冗长，且不安全。例如，如果 `obj.first` 是一个非 `null` 或 `undefined` 的{{Glossary("Falsy", "假值")}}，比如 `0`，它仍然会短路并使 `nestedProp` 变为 `0`，这可能是不可取的。

然而，使用可选链运算符（`?.`），在访问 `obj.first.second` 之前，不再需要基于 `obj.first` 的状态进行明确的测试和短路操作了：

```js
const nestedProp = obj.first?.second;
```

通过使用 `?.` 运算符取代 `.` 运算符，JavaScript 会在尝试访问 `obj.first.second` 之前，先隐式地检查并确定 `obj.first` 既不是 `null` 也不是 `undefined`。如果 `obj.first` 是 `null` 或者 `undefined`，表达式将会自动短路，并返回 `undefined`。

这等价于以下表达式，但实际上没有创建临时变量：

```js
const temp = obj.first;
const nestedProp =
  temp === null || temp === undefined ? undefined : temp.second;
```

可选链运算符不能用于未声明的根对象，但可以用于值为 `undefined` 的根对象。

```js example-bad
undeclaredVar?.prop; // ReferenceError: undeclaredVar is not defined
```

### 函数调用中的可选链

当尝试调用一个可能不存在的方法时也可以使用可选链。例如，当使用某个 API 时，如果由于实现版本过旧或用户设备不具备某项功能而导致某个方法不可用时，可选链就很有用。

函数调用时如果被调用的方法不存在，使用可选链可以使表达式自动返回 `undefined` 而不是抛出一个异常。

```js
const result = someInterface.customMethod?.();
```

然而，如果存在一个具有这样名称的属性且不是函数，使用 `?.` 仍然会引发一个 {{jsxref("TypeError")}} 异常，即“`someInterface.customMethod` is not a function（不是一个函数）”。

> [!NOTE]
> 如果 `someInterface` 自身是 `null` 或者 `undefined`，{{JSxRef("TypeError")}} 异常仍会被抛出（`someInterface is null`）。如果你希望允许 `someInterface` 自身也为 `null` 或者 `undefined`，你需要在这个位置使用 `?.`：`someInterface?.customMethod?.()`。

`eval?.()` 是进入[_间接求值_](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/eval#direct_and_indirect_eval)模式的最短方式。

### 表达式中的可选链

你也可以将可选链运算符与[方括号表示法](/zh-CN/docs/Web/JavaScript/Reference/Operators/Property_accessors#方括号表示法)结合使用，它允许将表达式作为属性名传递：

```js
const nestedProp = obj?.["prop" + "Name"];
```

这对于数组尤其有用，因为数组索引必须使用方括号来使用。

```js
function printMagicIndex(arr) {
  console.log(arr?.[42]);
}

printMagicIndex([0, 1, 2, 3, 4, 5]); // undefined
printMagicIndex(); // undefined；如果未使用 ?. 运算符，这将抛出一个错误：“Cannot read properties of undefined (reading '42')”
```

### 无效的可选链

尝试为可选链表达式的结果赋值是无效的：

```js-nolint example-bad
const object = {};
object?.property = 1; // SyntaxError: Invalid left-hand side in assignment
```

[模板字符串标签](/zh-CN/docs/Web/JavaScript/Reference/Template_literals#带标签的模板)不能是可选链（参见 [SyntaxError: tagged template cannot be used with optional chain](/zh-CN/docs/Web/JavaScript/Reference/Errors/Bad_optional_template)）：

```js-nolint example-bad
String?.raw`Hello, world!`;
String.raw?.`Hello, world!`; // SyntaxError: Invalid tagged template on optional chain
```

{{jsxref("Operators/new", "new")}} 表达式的构造函数不能是可选链（参见 [SyntaxError: new keyword cannot be used with an optional chain](/zh-CN/docs/Web/JavaScript/Reference/Errors/Bad_new_optional)）：

```js-nolint example-bad
new Intl?.DateTimeFormat(); // SyntaxError: Invalid optional chain from new expression
new Map?.();
```

### 短路

在使用可选链时，如果左操作数是 `null` 或 `undefined`，则表达式将不会被求值。例如：

```js
const potentiallyNullObj = null;
let x = 0;
const prop = potentiallyNullObj?.[x++];

console.log(x); // x 未被递增，因此为 0
```

后续的属性访问也不会被求值。

```js
const potentiallyNullObj = null;
const prop = potentiallyNullObj?.a.b;
// 这不会抛出错误，因为求值已经在第一个可选链处停止了
```

这等价于：

```js
const potentiallyNullObj = null;
const prop =
  potentiallyNullObj === null || potentiallyNullObj === undefined
    ? undefined
    : potentiallyNullObj.a.b;
```

然而，这种短路行为只会在一个连续的属性访问“链”中发生。如果你将链中的某一部分进行[分组](/zh-CN/docs/Web/JavaScript/Reference/Operators/Grouping)，那么后续的属性访问仍然会被求值。

```js
const potentiallyNullObj = null;
const prop = (potentiallyNullObj?.a).b;
// TypeError: Cannot read properties of undefined (reading 'b')
```

这等价于：

```js
const potentiallyNullObj = null;
const temp = potentiallyNullObj?.a;
const prop = temp.b;
```

除了没有创建 `temp` 变量。

## 示例

### 基本示例

此示例在一个不含 `bar` 成员的 Map 中查找 `bar` 成员的 `name` 属性，因此结果是 `undefined`。

```js
const myMap = new Map();
myMap.set("foo", { name: "baz", desc: "inga" });

const nameBar = myMap.get("bar")?.name;
```

### 处理可选的回调函数或事件处理器

如果使用[解构](/zh-CN/docs/Web/JavaScript/Reference/Operators/Destructuring)来解构的一个对象的回调函数或 fetch 方法，你可能得到不能当做函数直接调用的不存在的值，除非你已经校验了它们的存在性。你可以使用 `?.` 来忽略这些额外的校验：

```js
// 不使用可选链的写法
function doSomething(onContent, onError) {
  try {
    // 用数据做些事情
  } catch (err) {
    // 校验 onError 是否真的存在
    if (onError) {
      onError(err.message);
    }
  }
}
```

```js
// 使用可选链进行函数调用
function doSomething(onContent, onError) {
  try {
    // 用数据做些事情
  } catch (err) {
    onError?.(err.message); // 如果 onError 是 undefined 也不会有异常
  }
}
```

### 连用可选链运算符

在嵌套结构中，可以多次使用可选链：

```js
const customer = {
  name: "Carl",
  details: {
    age: 82,
    location: "Paradise Falls", // details 的 address 属性未有定义
  },
};
const customerCity = customer.details?.address?.city;

// 可选链也可以和函数调用一起使用
const customerName = customer.name?.getName?.(); // 方法不存在，customerName 未定义
```

### 使用空值合并运算符

当未找到任何值时，可以在可选链之后使用[空值合并运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Nullish_coalescing)来构建一个默认值：

```js
function printCustomerCity(customer) {
  const customerCity = customer?.city ?? "未知城市";
  console.log(customerCity);
}

printCustomerCity({
  name: "Nathan",
  city: "Paris",
}); // "Paris"
printCustomerCity({
  name: "Carl",
  details: { age: 82 },
}); // "未知城市"
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- [空值合并运算符（??）](/zh-CN/docs/Web/JavaScript/Reference/Operators/Nullish_coalescing)

---
# Source: index.md
---
---
title: 乘法（*）
slug: Web/JavaScript/Reference/Operators/Multiplication
---

**乘法**（**`*`**）运算符计算操作数的乘积。

{{InteractiveExample("JavaScript Demo: Expressions - Multiplication operator")}}

```js interactive-example
console.log(3 * 4);
// Expected output: 12

console.log(-3 * 4);
// Expected output: -12

console.log("3" * 2);
// Expected output: 6

console.log("foo" * 2);
// Expected output: NaN
```

## 语法

```js-nolint
x * y
```

## 示例

### 数值乘法

```js
2 * 2; // 4
-2 * 2; // -4
```

### 与 Infinity 相乘

```js
Infinity * 0; // NaN
Infinity * Infinity; // Infinity
```

### 非数值乘法

```js
"foo" * 2; // NaN
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- [加法运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Addition)
- [减法运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Subtraction)
- [除法运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Division)
- [取余运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Remainder)
- [幂运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Exponentiation)
- [自增运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Increment)
- [自减运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Decrement)
- [一元减运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Unary_negation)
- [一元加运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Unary_plus)

---
# Source: index.md
---
---
title: import()
slug: Web/JavaScript/Reference/Operators/import
l10n:
  sourceCommit: eb7cf694c19b31ee8826f22eaac6c12e808b1e50
---

**`import()`** 语法（通常被称为*动态导入*）是一种允许异步和动态地将 ECMAScript 模块加载到一个潜在的非模块环境中的类函数表达式。

跟[与之对应的声明式风格](/zh-CN/docs/Web/JavaScript/Reference/Statements/import)不同，动态导入只有在被需要时才会求值，并提供了更强大的语法灵活性。

## 语法

```js-nolint
import(moduleName)
import(moduleName, options)
```

`import()` 调用是一个类似于函数调用的语法，但 `import` 本身是一个关键字，而不是一个函数。你不能像 `const myImport = import` 那样为其添加别名，这会抛出 {{jsxref("SyntaxError")}}。

只有在运行时也支持 `options` 时，[尾后逗号](/zh-CN/docs/Web/JavaScript/Reference/Trailing_commas)才被允许使用。请查看[浏览器兼容性](#浏览器兼容性)部分。

### 参数

- `moduleName`
  - : 要导入的模块。标识符的求值是宿主特异的（host-specified），但始终遵循与静态的 [import 声明](/zh-CN/docs/Web/JavaScript/Reference/Statements/import)相同的算法。
- `options`
  - : 一个包含了导入选项的对象。以下是可识别的键：
    - `with`
      - : [import 属性](/zh-CN/docs/Web/JavaScript/Reference/Statements/import/with)。

### 返回值

返回一个 promise：

- 如果引用的模块被成功加载和求值，则兑现为一个[模块命名空间对象](#模块命名空间对象)：一个包含 `moduleName` 中所有导出的对象。
- 如果对 `moduleName` 做[字符串强制转换](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/String#字符串强制转换)时抛出错误，则以抛出的错误拒绝。
- 如果 `moduleName` 引用的模块不存在，则以实现定义的错误拒绝（Node 使用通用的 `Error`，而所有浏览器使用 `TypeError`）。
- 如果引用的模块在求值时抛出错误，则以抛出的错误拒绝。

> [!NOTE]
> `import()` 从来不会同步地抛出错误。

## 描述

import 声明语法（`import something from "somewhere"`）是静态的，并且总是会在一加载时就对导入的模块求值。动态导入允许绕过 import 声明的语法刚性（syntactic rigidity），并有条件地或按需加载模块。以下是你可能需要使用动态导入的一些原因：

- 当静态导入显著减慢你的代码加载，或增加你的程序内存使用时，那么你很可能不需要正要导入的代码，或者以后才会需要它。
- 当你正要导入的模块在加载时并不存在时。
- 当导入标识符字符串需要动态构建时。（静态导入仅支持静态标识符。）
- 当你正要导入的模块有副作用，并且你仅在某些条件下才希望有这些副作用。（建议模块中不要有任何副作用，但有时模块的依赖项中是否有副作用也无法控制）
- 当你处于非模块化的环境（例如，`eval` 或脚本文件）时。

仅在必要时使用动态导入。静态导入更适合加载初始依赖项，并且可以更容易地从静态分析工具和[摇树优化](/zh-CN/docs/Glossary/Tree_shaking)中获益。

如果你的文件不是作为模块运行的（如果它在 HTML 文件中被引用，脚本标签必须有 `type="module"` 属性），你将无法使用静态导入声明。而另一方面，异步的动态导入语法却始终可用，它允许你将模块导入到非模块环境中。

`options` 参数允许不同类型的导入选项。例如 [import 属性](/zh-CN/docs/Web/JavaScript/Reference/Statements/import/with)：

```js
import("./data.json", { with: { type: "json" } });
```

动态模块导入并不在所有执行上下文中都可使用。例如，`import()` 可以在主线程、共享/专用 worker 中使用，但如果在 [service worker](/zh-CN/docs/Web/API/Service_Worker_API) 或 [worklet](/zh-CN/docs/Web/API/Worklet) 中调用，则会抛出错误。

### 模块命名空间对象

*模块命名空间对象*是一个描述模块所有导出的对象。它是一个静态对象，在模块被求值时创建。有两种方式可以访问模块的模块命名空间对象：通过[命名空间导入](/zh-CN/docs/Web/JavaScript/Reference/Statements/import#命名空间导入)（`import * as name from moduleName`）或通过动态导入的兑现值。

模块命名空间对象是一个[密封](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Object/isSealed)的、具有 [`null` 原型](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Object#null_原型对象)的对象。也就是说，对象的所有字符串键对应于模块的导出，并且永远不会有额外的键。所有键都是以字典序[可枚举的](/zh-CN/docs/Web/JavaScript/Guide/Enumerability_and_ownership_of_properties)（即 [`Array.prototype.sort()`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Array/sort#描述) 的默认行为），默认导出以名为 `default` 的键可用。此外，模块命名空间对象具有一个值为 `"Module"` 的 [`[Symbol.toStringTag]`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Symbol/toStringTag) 属性，在 {{jsxref("Object.prototype.toString()")}} 中被使用。

在使用 {{jsxref("Object.getOwnPropertyDescriptors()")}} 获取它们的描述符时会发现，字符串属性是不可配置的和可写入的。然而它们实际上是只读的，因为你不能给属性重新赋一个新的值。这些值可以由导出它们的模块重新赋值，但不能由导入它们的模块重新赋值——这种行为反映了静态导入所创建的“[实时绑定](/zh-CN/docs/Web/JavaScript/Reference/Statements/import#导入的值只能由导出者修改)”。属性的可写入性反映了值是可能发生变化的，因为不可配置和不可写入的属性必须是常量。例如，你可以重新给一个导出的变量赋值，并且可以在模块命名空间对象中观察到新的值。

每个模块标识符对应一个唯一的模块命名空间对象，所以下面的代码通常是正确的：

```js
import * as mod from "/my-module.js";

import("/my-module.js").then((mod2) => {
  console.log(mod === mod2); // true
});
```

除了一个奇怪的情况：由于 promise 对象永远不会兑现为 [thenable](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Promise#thenable)，如果 `my-module.js` 模块恰好导出了一个名为 `then()` 的函数，那么该函数将在动态导入的 promise 兑现时自动被调用，因为这是 [promise 解决](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Promise/Promise#resolve_函数)处理流程的一部分。

```js
// my-module.js
export function then(resolve) {
  console.log("then() 已被调用");
  resolve(1);
}
```

```js
// main.js
import * as mod from "/my-module.js";

import("/my-module.js").then((mod2) => {
  // 打印“then() 已被调用”
  console.log(mod === mod2); // false
});
```

> [!WARNING]
> 不要从模块中导出名为 `then()` 的函数。这将导致模块在动态导入和静态导入时的行为不同。

## 示例

### 仅导入模块以获取其副作用

```js
(async () => {
  if (somethingIsTrue) {
    // 导入模块以获取其副作用
    await import("/modules/my-module.js");
  }
})();
```

如果你的项目使用导出 ESM 的包，你也可以仅导入它们以获取其副作用。这将仅运行包的入口点文件（以及它导入的任何文件）中的代码。

### 导入默认值

如果你正在解构导入的模块命名空间对象，那么你必须重命名 `default` 键，因为 `default` 是保留字。

```js
(async () => {
  if (somethingIsTrue) {
    const {
      default: myDefault,
      foo,
      bar,
    } = await import("/modules/my-module.js");
  }
})();
```

### 根据用户操作按需导入

这个示例展示了如何根据用户操作（在本例中为按钮点击）将功能加载到页面上，然后在该模块中调用一个函数。这不是实现此功能的唯一方式。`import()` 函数也支持 `await`。

```js
const main = document.querySelector("main");
for (const link of document.querySelectorAll("nav > a")) {
  link.addEventListener("click", (e) => {
    e.preventDefault();

    import("/modules/my-module.js")
      .then((module) => {
        module.loadPageInto(main);
      })
      .catch((err) => {
        main.textContent = err.message;
      });
  });
}
```

### 根据环境导入不同的模块

在服务器端渲染等过程中，你可能需要在服务器或浏览器中加载不同的逻辑，因为它们与不同的全局对象或模块交互（例如，浏览器代码可以访问 `document` 和 `navigator` 等 Web API，而服务器代码可以访问服务器文件系统）。你可以通过条件动态导入来实现这一点。

```js
let myModule;

if (typeof window === "undefined") {
  myModule = await import("module-used-on-server");
} else {
  myModule = await import("module-used-in-browser");
}
```

### 使用非字面量标识符导入模块

动态导入允许任何表达式作为模块标识符，而不仅仅是字符串字面量。

这里，我们同时加载 10 个模块（如 `/modules/module-0.js`、`/modules/module-1.js` 等），并调用每个模块导出的 `load` 函数。

```js
Promise.all(
  Array.from({ length: 10 }).map(
    (_, index) => import(`/modules/module-${index}.js`),
  ),
).then((modules) => modules.forEach((module) => module.load()));
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- [`import`](/zh-CN/docs/Web/JavaScript/Reference/Statements/import)

---
# Source: index.md
---
---
title: in
slug: Web/JavaScript/Reference/Operators/in
---

如果指定的属性在指定的对象或其原型链中，则 **`in`** **运算符**返回 `true`。

{{InteractiveExample("JavaScript Demo: Expressions - in operator")}}

```js interactive-example
const car = { make: "Honda", model: "Accord", year: 1998 };

console.log("make" in car);
// Expected output: true

delete car.make;
if ("make" in car === false) {
  car.make = "Suzuki";
}

console.log(car.make);
// Expected output: "Suzuki"
```

## 语法

```plain
prop in object
```

### 参数

- `prop`
  - : 一个字符串类型或者 symbol 类型的属性名或者数组索引（非 symbol 类型将会强制转为字符串）。
- `objectName`
  - : 检查它（或其原型链）是否包含具有指定名称的属性的对象。

## 描述

下面的例子演示了一些 `in` 运算符的用法。

```js
// 数组
var trees = new Array("redwood", "bay", "cedar", "oak", "maple");
0 in trees; // 返回 true
3 in trees; // 返回 true
6 in trees; // 返回 false
"bay" in trees; // 返回 false (必须使用索引号，而不是数组元素的值)

"length" in trees; // 返回 true (length 是一个数组属性)

Symbol.iterator in trees; // 返回 true (数组可迭代，只在 ES2015+ 上有效)

// 内置对象
"PI" in Math; // 返回 true

// 自定义对象
var mycar = { make: "Honda", model: "Accord", year: 1998 };
"make" in mycar; // 返回 true
"model" in mycar; // 返回 true
```

`in`右操作数必须是一个对象值。例如，你可以指定使用`String`构造函数创建的字符串，但不能指定字符串文字。

```js
var color1 = new String("green");
"length" in color1; // 返回 true
var color2 = "coral";
"length" in color2; // 报错 (color2 不是对象)
```

### 对被删除或值为 undefined 的属性使用`in`

如果你使用 [`delete`](/zh-CN/docs/Web/JavaScript/Reference/Operators/delete) 运算符删除了一个属性，则 `in` 运算符对所删除属性返回 `false`。

```js
var mycar = { make: "Honda", model: "Accord", year: 1998 };
delete mycar.make;
"make" in mycar; // 返回 false

var trees = new Array("redwood", "bay", "cedar", "oak", "maple");
delete trees[3];
3 in trees; // 返回 false
```

如果你只是将一个属性的值赋值为{{jsxref("Global_Objects/undefined", "undefined")}}，而没有删除它，则 `in` 运算仍然会返回`true`。

```js
var mycar = { make: "Honda", model: "Accord", year: 1998 };
mycar.make = undefined;
"make" in mycar; // 返回 true
```

```js
var trees = new Array("redwood", "bay", "cedar", "oak", "maple");
trees[3] = undefined;
3 in trees; // 返回 true
```

### 继承属性

如果一个属性是从原型链上继承来的，`in` 运算符也会返回 `true`。

```js
"toString" in {}; // 返回 true
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- [`for...in`](/zh-CN/docs/Web/JavaScript/Reference/Statements/for...in)
- [`delete`](/zh-CN/docs/Web/JavaScript/Reference/Operators/delete)
- {{jsxref("Object.hasOwn()")}}
- {{jsxref("Reflect.has()")}}
- [属性的可枚举性和所有权](/zh-CN/docs/Web/JavaScript/Guide/Enumerability_and_ownership_of_properties)

---
# Source: index.md
---
---
title: 加法（+）
slug: Web/JavaScript/Reference/Operators/Addition
---

**加法**（**`+`**）运算符计算数字操作数或字符串连接的总和。

{{InteractiveExample("JavaScript Demo: Expressions - Addition operator")}}

```js interactive-example
console.log(2 + 2);
// Expected output: 4

console.log(2 + true);
// Expected output: 3

console.log("hello " + "everyone");
// Expected output: "hello everyone"

console.log(2001 + ": A Space Odyssey");
// Expected output: "2001: A Space Odyssey"
```

## 语法

```js-nolint
x + y
```

## 描述

加法运算符（`+`）为两种不同的运算重载：数字加法和字符串连接。在求值时，它首先[将两个操作数强制转换为基本类型](/zh-CN/docs/Web/JavaScript/Guide/Data_structures#强制原始值转换)。然后，检查两个操作数的类型：

- 如果有一方是字符串，另一方则会被[转换为字符串](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/String#字符串强制转换)，并且它们连接起来。
- 如果双方都是 [BigInt](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/BigInt)，则执行 BigInt 加法。如果一方是 BigInt 而另一方不是，会抛出 {{jsxref("TypeError")}}。
- 否则，双方都会被[转换为数字](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Number#number_强制转换)，执行数字加法。

字符串连接经常被认为等价于[模板字符串](/zh-CN/docs/Web/JavaScript/Reference/Template_literals)或者 [`String.prototype.concat()`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/String/concat)，但并非如此。加法强制将表达式转为*基本类型*，它优先调用 [`valueOf()`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Object/valueOf)；另一方面，模板字符串和 `concat()` 则强制将表达式转为*字符串*，它们优先调用 [`toString()`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Object/toString)。如果表达式有 [`[Symbol.toPrimitive]()`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Symbol/toPrimitive) 方法，字符串连接时会用 `"default"` 作为 `hint` 调用它，然而模板字符串则用 `"string"`。这对于具有不同的字符串和原始值表现的对象来说很重要——例如 [Temporal](https://github.com/tc39/proposal-temporal)，它的 `valueOf()` 方法会抛出错误。

```js
const t = Temporal.Now.instant();
"" + t; // 抛出 TypeError
`${t}`; // '2022-07-31T04:48:56.113918308Z'
"".concat(t); // '2022-07-31T04:48:56.113918308Z'
```

建议不要使用 `"" + x` 来执行[字符串强制转换](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/String#字符串强制转换)。

## 示例

### 数字加法

```js
// Number + Number -> addition
1 + 2; // 3

// Boolean + Number -> addition
true + 1; // 2

// Boolean + Boolean -> addition
false + false; // 0
```

### 字符串连接

```js
// String + String -> concatenation
"foo" + "bar"; // "foobar"

// Number + String -> concatenation
5 + "foo"; // "5foo"

// String + Boolean -> concatenation
"foo" + false; // "foofalse"

// String + Number -> concatenation
"2" + 2; // "22"
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- [减法运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Subtraction)
- [除法运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Division)
- [乘法运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Multiplication)
- [取余运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Remainder)
- [求幂运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Exponentiation)
- [自增运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Increment)
- [自减运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Decrement)
- [一元减运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Unary_negation)
- [一元加运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Unary_plus)

---
# Source: index.md
---
---
title: 一元减（-）
slug: Web/JavaScript/Reference/Operators/Unary_negation
---

**一元减**（**`-`**）运算符在其操作数之前，并对其取反。

{{InteractiveExample("JavaScript Demo: Expressions - Unary negation operator")}}

```js interactive-example
const x = 4;
const y = -x;

console.log(y);
// Expected output: -4

const a = "4";
const b = -a;

console.log(b);
// Expected output: -4
```

## 语法

```js-nolint
-x
```

## 示例

### 数字取反

```js
const x = 3;
const y = -x;

// y = -3
// x = 3
```

### 非数字取反

一元减运算符可以[将非数字转换为数字](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Number#number_强制转换)。

```js
const x = "4";
const y = -x;

// y = -4
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- [加法运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Addition)
- [减法运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Subtraction)
- [除法运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Division)
- [乘法运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Multiplication)
- [取余运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Remainder)
- [求幂运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Exponentiation)
- [自增运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Increment)
- [自减运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Decrement)
- [一元加运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Unary_plus)

---
# Source: index.md
---
---
title: 严格相等（===）
slug: Web/JavaScript/Reference/Operators/Strict_equality
---

严格相等运算符（`===`）会检查它的两个操作数是否相等，并且返回一个布尔值结果。与[相等](/zh-CN/docs/Web/JavaScript/Reference/Operators/Equality)运算符不同，严格相等运算符总是认为不同类型的操作数是不同的。

{{InteractiveExample("JavaScript Demo: Expressions - Strict equality operator")}}

```js interactive-example
console.log(1 === 1);
// Expected output: true

console.log("hello" === "hello");
// Expected output: true

console.log("1" === 1);
// Expected output: false

console.log(0 === false);
// Expected output: false
```

## 语法

```js-nolint
x === y
```

## 描述

严格相等运算符（`===` 和 `!==`）提供了[严格相等判定](/zh-CN/docs/Web/JavaScript/Guide/Equality_comparisons_and_sameness#严格相等)语义。

- 如果操作数的类型不同，则返回 `false`。
- 如果两个操作数都是对象，只有当它们指向同一个对象时才返回 `true`。
- 如果两个操作数都为 `null`，或者两个操作数都为 `undefined`，返回 `true`。
- 如果两个操作数有任意一个为 `NaN`，返回 `false`。
- 否则，比较两个操作数的值：
  - 数字类型必须拥有相同的数值。`+0` 和 `-0` 会被认为是相同的值。
  - 字符串类型必须拥有相同顺序的相同字符。
  - 布尔运算符必须同时为 `true` 或同时为 `false`。

严格相等运算符与[相等](/zh-CN/docs/Web/JavaScript/Reference/Operators/Equality)（`==`）运算符最显著的区别是，如果操作数的类型不同，`==` 运算符会在比较之前尝试将它们转换为相同的类型。

## 示例

### 比较相同类型的操作数

```js
"hello" === "hello"; // true
"hello" === "hola"; // false

3 === 3; // true
3 === 4; // false

true === true; // true
true === false; // false

null === null; // true
```

### 比较不同类型的操作数

```js
"3" === 3; // false
true === 1; // false
null === undefined; // false
```

### 比较对象

```js
const object1 = {
  key: "value",
};

const object2 = {
  key: "value",
};

console.log(object1 === object2); // false
console.log(object1 === object1); // true
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- [相等运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Equality)
- [不相等运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Inequality)
- [严格不相等运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Strict_inequality)

---
# Source: index.md
---
---
title: 类表达式
slug: Web/JavaScript/Reference/Operators/class
---

**`class`** 关键字可用于在表达式中定义类。类似于[函数表达式](/zh-CN/docs/Web/JavaScript/Reference/Operators/function)，类表达式可以是命名的，也可以是匿名的。如果命名，则类的名称只能在类体内部才能访问到。

{{InteractiveExample("JavaScript Demo: Expressions - class expression")}}

```js interactive-example
const Rectangle = class {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }
  area() {
    return this.height * this.width;
  }
};

console.log(new Rectangle(5, 8).area());
// Expected output: 40
```

## 语法

```js-nolint
const MyClass = class [className] [extends otherClassName] {
  // class body
}
```

## 描述

类表达式的语法类似于{{jsxref("Statements/class", "类声明", "", 1)}}。与 `class` 声明一样，`class` 表达式的主体在{{jsxref("Strict_mode", "严格模式", "", 1)}}下执行。

类表达式和{{jsxref("Statements/class", "类声明", "", 1)}}之间存在一些差异，但是：

- 类表达式可以省略类名（“绑定标识符”），这在{{jsxref("Statements/class", "类声明", "", 1)}}中是不可能的。
- 类表达式允许你重新定义（重新声明）类**而不会抛出** {{jsxref("Global_Objects/SyntaxError", "SyntaxError")}}。{{jsxref("Statements/class", "类声明", "", 1)}}不是这种情况。

`constructor` 方法是可选的。使用类表达式生成的类将始终响应 {{jsxref("Operators/typeof", "typeof")}} 值为 `"function"`。

```js
"use strict";
let Foo = class {}; // constructor property is optional
Foo = class {}; // Re-declaration is allowed

typeof Foo; // returns "function"
typeof class {}; // returns "function"

Foo instanceof Object; // true
Foo instanceof Function; // true
class Foo {} // Throws SyntaxError (class declarations do not allow re-declaration)
```

## 示例

### 一个简单的类表达式

这只是一个简单的匿名类表达式，你可以使用变量 `Foo` 来引用它。

```js
const Foo = class {
  constructor() {}
  bar() {
    return "Hello World!";
  }
};

const instance = new Foo();
instance.bar(); // "Hello World!"
Foo.name; // "Foo"
```

### 命名类表达式

如果你想在类体内引用当前类，你可以创建一个*命名类表达式*。该名称仅在类表达式本身的范围内可见。

```js
const Foo = class NamedFoo {
  constructor() {}
  whoIsThere() {
    return NamedFoo.name;
  }
};
const bar = new Foo();
bar.whoIsThere(); // "NamedFoo"
NamedFoo.name; // ReferenceError: NamedFoo is not defined
Foo.name; // "NamedFoo"
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- {{jsxref("Operators/function", "函数表达式", "", 1)}}
- {{jsxref("Statements/class", "类声明", "", 1)}}
- {{jsxref("Classes", "类", "", 1)}}

---
# Source: index.md
---
---
title: yield
slug: Web/JavaScript/Reference/Operators/yield
---

`yield` 关键字用于暂停和恢复[生成器函数](/zh-CN/docs/Web/JavaScript/Reference/Statements/function*)。

{{InteractiveExample("JavaScript Demo: Expressions - yield", "taller")}}

```js interactive-example
function* foo(index) {
  while (index < 2) {
    yield index;
    index++;
  }
}

const iterator = foo(0);

console.log(iterator.next().value);
// Expected output: 0

console.log(iterator.next().value);
// Expected output: 1
```

## 语法

```plain
[rv] = yield [expression];
```

- `expression`
  - : 定义通过[迭代器协议](/zh-CN/docs/Web/JavaScript/Reference/Iteration_protocols#iterator)从生成器函数返回的值。如果省略，则返回 `undefined`。
- `rv`
  - : 返回传递给生成器的 `next()` 方法的可选值，以恢复其执行。

## 描述

`yield` 关键字使生成器函数执行暂停，`yield` 关键字后面的表达式的值返回给生成器的调用者。它可以被认为是一个基于生成器的版本的 `return` 关键字。

`yield` 关键字实际返回一个 `IteratorResult` 对象，它有两个属性，`value` 和 `done`。`value` 属性是对 `yield` 表达式求值的结果，而 `done` 是 `false`，表示生成器函数尚未完全完成。

一旦遇到 `yield` 表达式，生成器的代码将被暂停运行，直到生成器的 `next()` 方法被调用。每次调用生成器的 `next()` 方法时，生成器都会恢复执行，直到达到以下某个值：

- `yield`，导致生成器再次暂停并返回生成器的新值。下一次调用 `next()` 时，在 `yield` 之后紧接着的语句继续执行。
- {{jsxref("Statements/throw", "throw")}} 用于从生成器中抛出异常。这让生成器完全停止执行，并在调用者中继续执行，正如通常情况下抛出异常一样。
- 到达生成器函数的结尾。在这种情况下，生成器的执行结束，并且 `IteratorResult` 给调用者返回 `value` 的值是 {{jsxref("undefined")}} 并且 `done` 为 `true`。
- 到达 {{jsxref("Statements/return", "return")}} 语句。在这种情况下，生成器的执行结束，并将 `IteratorResult` 返回给调用者，其 `value` 的值是由 `return` 语句指定的，并且 `done` 为 `true`。

如果将参数传递给生成器的 `next()` 方法，则该值将成为生成器当前 `yield` 操作返回的值。

在生成器的代码路径中的 `yield` 运算符，以及通过将其传递给 {{jsxref("Generator.prototype.next()")}} 指定新的起始值的能力之间，生成器提供了强大的控制力。

> [!WARNING]
> 不幸地是，`next()` 是不对称的，但这并不是没有帮助：它总是向当前暂停的 `yield` 发送一个值，但是返回的是 `yield` 之后表达式的运算结果。

## 示例

### 使用 yield

以下代码是一个生成器函数的声明。

```js
function* countAppleSales() {
  const saleList = [3, 7, 5];
  for (let i = 0; i < saleList.length; i++) {
    yield saleList[i];
  }
}
```

一旦生成器函数已定义，可以通过构造一个迭代器来使用它。

```js
const appleStore = countAppleSales(); // Generator { }
console.log(appleStore.next()); // { value: 3, done: false }
console.log(appleStore.next()); // { value: 7, done: false }
console.log(appleStore.next()); // { value: 5, done: false }
console.log(appleStore.next()); // { value: undefined, done: true }
```

你也可以将带有 `next(value)` 的值发送给生成器。在 `rv = yield expression` 这个语法中，`step` 用于接收返回值——尽管第一次调用 `next()` 时忽略传递给生成器 `next()` 方法的值。

```js
function* counter(value) {
  let step;

  while (true) {
    step = yield value++;
    if (step) {
      value += step;
    }
  }
}

const generatorFunc = counter(0);
console.log(generatorFunc.next().value); // 0
console.log(generatorFunc.next().value); // 1
console.log(generatorFunc.next().value); // 2
console.log(generatorFunc.next().value); // 3
console.log(generatorFunc.next(10).value); // 14
console.log(generatorFunc.next().value); // 15
console.log(generatorFunc.next(10).value); // 26
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- [迭代协议](/zh-CN/docs/Web/JavaScript/Reference/Iteration_protocols)
- {{jsxref("Statements/function*", "function*")}}
- [`function*` 表达式](/zh-CN/docs/Web/JavaScript/Reference/Operators/function*)
- {{jsxref("Operators/yield*", "yield*")}}

---
# Source: index.md
---
---
title: 加法赋值（+=）
slug: Web/JavaScript/Reference/Operators/Addition_assignment
---

加法赋值运算符（`+=`）将右操作数的值添加到变量，并将结果分配给该变量。两个操作数的类型决定了加法赋值运算符的行为，可能为加法或拼接。

{{InteractiveExample("JavaScript Demo: Expressions - Addition assignment operator")}}

```js interactive-example
let a = 2;
let b = "hello";

console.log((a += 3)); // Addition
// Expected output: 5

console.log((b += " world")); // Concatenation
// Expected output: "hello world"
```

## 语法

```js-nolint
x += y // x = x + y
```

## 示例

### 使用加法赋值

```js
let baz = true;

// Boolean + Number -> 加法
baz += 1; // 2

// Number + Boolean -> 加法
baz += false; // 2
```

```js
let foo = "foo";

// String + Boolean -> 拼接
foo += false; // "foofalse"

// String + String -> 拼接
foo += "bar"; // "foofalsebar"
```

```js
let bar = 5;

// Number + Number -> 加法
bar += 2; // 7

// Number + String -> 拼接
bar += "foo"; // "7foo"
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- [JS 指南中的赋值运算符](/zh-CN/docs/Web/JavaScript/Guide/Expressions_and_operators#赋值运算符)
- [加法运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Addition)

---
# Source: index.md
---
---
title: 按位非（~）
slug: Web/JavaScript/Reference/Operators/Bitwise_NOT
---

按位非运算符（`~`）将操作数的位反转。如同其他位运算符一样，它将操作数转化为 32 位的有符号整型。

{{InteractiveExample("JavaScript Demo: Expressions - Bitwise NOT")}}

```js interactive-example
const a = 5; // 00000000000000000000000000000101
const b = -3; // 11111111111111111111111111111101

console.log(~a); // 11111111111111111111111111111010
// Expected output: -6

console.log(~b); // 00000000000000000000000000000010
// Expected output: 2
```

## 语法

```js-nolint
~a
```

## 描述

操作数被转换为 32 位有符号整型，并以一系列比特（0 和 1）表示。超过 32 位的数字将丢弃其最高有效位。如下例子中，超过 32 位的整数将转换为 32 位整数：

```plain
Before: 11100110111110100000000000000110000000000001
After:              10100000000000000110000000000001
```

运算结果的每一位数都由操作数相应位反转而来。

`NOT` 运算的真值表如下所示：

| a   | NOT a |
| --- | ----- |
| 0   | 1     |
| 1   | 0     |

```plain
 9 (base 10) = 00000000000000000000000000001001 (base 2)
               --------------------------------
~9 (base 10) = 11111111111111111111111111110110 (base 2) = -10 (base 10)
```

32 位有符号整数操作数根据[补码](https://zh.wikipedia.org/zh-cn/补码)运算规则进行反转，也就是说，最高有效位表示负数。

按位非运算时，任何数字 `x` 的运算结果都是 `-(x + 1)`。例如，`~-5` 运算结果为 `4`。

请注意，由于数字 `~-1` 和 `~4294967295`（2<sup>32</sup> - 1）均使用 32 位表示形式，它们的运算结果均为 `0`。

## 示例

### 使用按位取反

```js
~0; // -1
~-1; // 0
~1; // -2
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- [JavaScript 指南：位运算符](/zh-CN/docs/Web/JavaScript/Guide/Expressions_and_operators#位运算符)

---
# Source: index.md
---
---
title: 右移赋值（>>=）
slug: Web/JavaScript/Reference/Operators/Right_shift_assignment
---

右移赋值运算符（`>>=`）将变量向右移动指定的位数，并将结果赋值给变量。

{{InteractiveExample("JavaScript Demo: Expressions - Right shift assignment operator")}}

```js interactive-example
let a = 5; //  00000000000000000000000000000101

a >>= 2; //  00000000000000000000000000000001
console.log(a);
// Expected output: 1

let b = -5; //  11111111111111111111111111111011

b >>= 2; //  11111111111111111111111111111110
console.log(b);
// Expected output: -2
```

## 语法

```js-nolint
x >>= y // x = x >> y
```

## 示例

### 使用右移赋值

```js
let a = 5; //   (00000000000000000000000000000101)
a >>= 2; // 1 (00000000000000000000000000000001)

let b = -5; //  (-00000000000000000000000000000101)
b >>= 2; // -2 (-00000000000000000000000000000010)
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参考

- [JS 指南中的赋值运算符](/zh-CN/docs/Web/JavaScript/Guide/Expressions_and_operators#赋值运算符)
- [右移运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Right_shift)

---
# Source: index.md
---
---
title: 取余（%）
slug: Web/JavaScript/Reference/Operators/Remainder
---

**取余**（**`%`**）运算符返回左侧操作数除以右侧操作数的余数。它总是与被除数的符号保持一致。

{{InteractiveExample("JavaScript Demo: Expressions - Remainder operator")}}

```js interactive-example
console.log(13 % 5);
// Expected output: 3

console.log(-13 % 5);
// Expected output: -3

console.log(4 % 2);
// Expected output: 0

console.log(-4 % 2);
// Expected output: -0
```

## 语法

```js-nolint
x % y
```

## 描述

对于运算：`n % d`，其中 `n` 被称为被除数，`d` 被称为除数。如果其中的任意一个操作数为 `NaN`，或 `n` 为正负无穷（±Infinity），又或者 `d` 为 ±0，则该运算返回 `NaN`。否则，如果 `d` 为正负无穷（±Infinity），或 `n` 为 ±0，则返回被除数 `n`。

如果两个操作数都非零且有限（非正负无穷）时，余数 `r` 将通过 `r := n - d * q` 计算获得，其中 `q` 是一个使得 `r` 与被除数 `n` 具有相同符号，并且会使 `r` 尽可能地接近于 0 的整数。

请注意，虽然在大多数语言中，`%` 是取余运算符，但在某些语言（例如：[Python 和 Perl](https://zh.wikipedia.org/wiki/模除#定义与余数的计算)）中，它是取模运算符。取模运算被定义为 `k := n - d * q`，其中 `q` 是一个使得 `k` 与除数具有相同符号，并且会使 `k` 尽可能地接近于 0 的整数。对于同号的两根操作数，两者是等价的，但在操作数具有不同的符号时，取模运算的结果总是与*除数*同号，而取余运算则是余数与*被除数*同号，`d` 的符号即可使两者的结果不相同。为了在 JavaScript 中使用 `n % d` 实现取模运算，可以使用 `((n % d) + d) % d`。在 JavaScript 中，模运算（没有专用的运算符）用于规范化按位移位运算符（[`<<`](/zh-CN/docs/Web/JavaScript/Reference/Operators/Left_shift)、[`>>`](/zh-CN/docs/Web/JavaScript/Reference/Operators/Right_shift)，等等）的第二个操作数，以使得偏移量始终为一个正数。

## 示例

### 被除数为正数

```js
13 % 5; // 3
1 % -2; // 1
1 % 2; // 1
2 % 3; // 2
5.5 % 2; // 1.5
```

### 被除数为负数

```js
-13 % 5; // -3
-1 % 2; // -1
-4 % 2; // -0
```

### 被除数为 NaN

```js
NaN % 2; // NaN
```

### 被除数为 Infinity

```js
Infinity % 2; // NaN
Infinity % 0; // NaN
Infinity % Infinity; // NaN
2 % Infinity; // 2
0 % Infinity; // 0
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- [加法运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Addition)
- [减法运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Subtraction)
- [除法运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Division)
- [乘法运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Multiplication)
- [幂运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Exponentiation)
- [自增运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Increment)
- [自减运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Decrement)
- [一元减运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Unary_negation)
- [一元加运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Unary_plus)
- [取余运算和取模运算的区别](https://2ality.com/2019/08/remainder-vs-modulo.html)

---
# Source: index.md
---
---
title: "null"
slug: Web/JavaScript/Reference/Operators/null
l10n:
  sourceCommit: fb85334ffa4a2c88d209b1074909bee0e0abd57a
---

`null` 值特指未不存在任何对象值。它是 JavaScript 的[原始值](/zh-CN/docs/Glossary/Primitive)之一，且在布尔运算中被视为[假值](/zh-CN/docs/Glossary/Falsy)。

{{InteractiveExample("JavaScript Demo: Standard built-in objects - Null")}}

```js interactive-example
function getVowels(str) {
  const m = str.match(/[aeiou]/gi);
  if (m === null) {
    return 0;
  }
  return m.length;
}

console.log(getVowels("sky"));
// Expected output: 0
```

## 语法

```js-nolint
null
```

## 描述

值 `null` 被写作字面量：`null`。不像 {{jsxref("undefined")}}，`null` 不是全局对象的属性。相反，`null` 是表示缺少的标识，指示变量未指向任何对象。在 API 中，`null` 常在预期的值应是一个对象，但又没有关联的对象的地方使用。

```js
// foo 不存在。它从未被定义或初始化：
foo; //ReferenceError: foo is not defined
```

```js
// 已知 foo 现在已经存在，但它没有类型和值：
const foo = null;
foo; //null
```

## 示例

### `null` 与 `undefined` 的不同点

当检查值是否为 `null` 或 `undefined` 时，请注意[相等（==）与全等（===）运算符的区别](/zh-CN/docs/Web/JavaScript/Reference/Operators)，前者会执行类型转换：

```js
typeof null; // "object"（因历史原因而不是 "null"）
typeof undefined; // "undefined"
null === undefined; // false
null == undefined; // true
null === null; // true
null == null; // true
!null; // true
Number.isNaN(1 + null); // false
Number.isNaN(1 + undefined); // true
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- {{jsxref("undefined")}}
- {{jsxref("NaN")}}
- {{jsxref("Operators/void", "void")}}

---
# Source: index.md
---
---
title: 按位异或赋值 (^=)
slug: Web/JavaScript/Reference/Operators/Bitwise_XOR_assignment
---

按位异或赋值操作符 (`^=`) 使用二进制表示操作数，进行一次按位异或操作并赋值。

{{InteractiveExample("JavaScript Demo: Expressions - Bitwise XOR assignment")}}

```js interactive-example
let a = 5; // 00000000000000000000000000000101
a ^= 3; // 00000000000000000000000000000011

console.log(a); // 00000000000000000000000000000110
// Expected output: 6
```

## 语法

```plain
Operator: x ^= y
Meaning:  x  = x ^ y
```

## 示例

### 使用按位异或赋值

```js
let a = 5; // 00000000000000000000000000000101
a ^= 3; // 00000000000000000000000000000011

console.log(a); // 00000000000000000000000000000110
// 6

let b = 5; // 00000000000000000000000000000101
b ^= 0; // 00000000000000000000000000000000

console.log(b); // 00000000000000000000000000000101
// 5
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- [Assignment operators in the JS guide](/zh-CN/docs/Web/JavaScript/Guide/Expressions_and_operators#赋值运算符)
- [Bitwise XOR operator](/zh-CN/docs/Web/JavaScript/Reference/Operators/Bitwise_XOR)

---
# Source: index.md
---
---
title: 运算符优先级
slug: Web/JavaScript/Reference/Operators/Operator_precedence
---

**运算符的优先级**决定了表达式中运算执行的先后顺序。优先级高的运算符会作为优先级低的运算符的操作数。

{{InteractiveExample("JavaScript Demo: Expressions - Operator precedence")}}

```js interactive-example
console.log(3 + 4 * 5); // 3 + 20
// Expected output: 23

console.log(4 * 3 ** 2); // 4 * 9
// Expected output: 36

let a;
let b;

console.log((a = b = 5));
// Expected output: 5
```

## 优先级和结合性

考虑由下面的表示法描述的表达式。其中，OP<sub>1</sub> 和 OP<sub>2</sub> 都是操作符的占位符。

```js
a OP1 b OP2 c
```

如果 `OP1` 和 `OP2` 具有不同的优先级（见下表），则优先级最高的运算符先执行，不用考虑结合性。观察乘法如何具有比加法更高的优先级并首先执行，即使加法是首先写入代码的。

```js-nolint
console.log(3 + 10 * 2); // 输出 23
console.log(3 + (10 * 2)); // 输出 23 因为这里的括号是多余的
console.log((3 + 10) * 2); // 输出 26 因为括号改变了优先级
```

左结合（左到右）相当于把左边的子表达式加上小括号 `(a OP b) OP c`，右结合（右到左）相当于 `a OP (b OP c)`。赋值运算符是右结合的，所以你可以这么写：

```js
a = b = 5; // 相当于 a = (b = 5);
```

预期结果是 `a` 和 `b` 的值都会成为 5。这是因为赋值运算符的返回结果就是赋值运算符右边的那个值，具体过程是：首先 `b` 被赋值为 5，然后 `a` 也被赋值为 `b = 5` 的返回值，也就是 5。

另一个例子是，只有幂运算符是右结合的，而其他算术运算符都是左结合的。有趣的是，无论结合性和优先级如何，求值顺序总是从左到右。

<table class="standard-table">
    <tbody>
        <tr>
            <td>代码</td>
            <td>输出</td>
        </tr>
        <tr>
            <td>
                <pre class="brush: js">
function echo(name, num) {
    console.log("Evaluating the " + name + " side");
    return num;
}
// 注意这里的除法运算符 (/)
console.log(echo("left", 6) / echo("right", 2));
</pre>
            </td>
            <td>
                <pre class="brush: plain">
Evaluating the left side
Evaluating the right side
3
</pre>
            </td>
        </tr>
        <tr>
            <td>
                <pre class="brush: js">
function echo(name, num) {
    console.log("Evaluating the " + name + " side");
    return num;
}
// 注意这里的幂运算符 (**)
console.log(echo("left", 2) ** echo("right", 3));</pre>
            </td>
            <td>
                <pre class="brush: plain">
Evaluating the left side
Evaluating the right side
8</pre>
            </td>
        </tr>
    </tbody>
</table>

当有多个具有相同优先级的运算符时，结合性的差异就会发挥作用。仅使用一个或多个不同优先级的运算符时，结合性不会影响输出，如上面的例子所示。在下面的示例中，观察使用多个相同运算符时结合性会如何影响输出。

<table class="standard-table">
    <tbody>
        <tr>
            <td>代码</td>
            <td>输出</td>
        </tr>
        <tr>
            <td>
                <pre class="brush: js">
function echo(name, num) {
    console.log("Evaluating the " + name + " side");
    return num;
}
// 注意这里的除法运算符 (/)
console.log(echo("left", 6) / echo("middle", 2) / echo("right", 3));
</pre>
            </td>
            <td>
                <pre class="brush: plain">
Evaluating the left side
Evaluating the middle side
Evaluating the right side
1
</pre>
            </td>
        </tr>
        <tr>
            <td>
                <pre class="brush: js">
function echo(name, num) {
    console.log("Evaluating the " + name + " side");
    return num;
}
// 注意这里的幂运算符 (**)
console.log(echo("left", 2) ** echo("middle", 3) ** echo("right", 2));
</pre>
            </td>
            <td>
                <pre class="brush: plain">
Evaluating the left side
Evaluating the middle side
Evaluating the right side
512
</pre>
            </td>
        </tr>
        <tr>
            <td>
                <pre class="brush: js">
function echo(name, num) {
    console.log("Evaluating the " + name + " side");
    return num;
}
// 注意这里左边和中间的被圆括号包围的求幂表达式
console.log((echo("left", 2) ** echo("middle", 3)) ** echo("right", 2));</pre>
            </td>
            <td>
                <pre class="brush: plain">
Evaluating the left side
Evaluating the middle side
Evaluating the right side
64</pre>
            </td>
        </tr>
    </tbody>
</table>

观察上面的代码片段，`6 / 3 / 2` 与 `(6 / 3) / 2` 是相同的，因为除法是左结合的。而幂运算符是右结合的，所以 `2 ** 3 ** 2` 与 `2 ** (3 ** 2)` 是相同的。因此，`(2 ** 3) ** 2` 会更改执行顺序，并导致输出上表中的 64。

请记住，判断执行顺序的时候，优先级在结合性之前。所以，混合求除法和幂时，求幂会先于除法。例如，`2 ** 3 / 3 ** 2` 的结果是 0.8888888888888888，因为它相当于 `(2 ** 3) / (3 ** 2)`。

### 分组和短路的注意事项

在下表中，**分组（Grouping）** 具有最高优先级。然而，这并不意味着总是优先对分组符号 `( … )` 内的表达式进行求值，尤其是涉及短路时。

短路是条件求值的术语。例如，在表达式 `a && (b + c)` 中，如果 `a` 为虚值（{{Glossary("falsy")}}），那么即使 `(b + c)` 在圆括号中，也不会被求值。我们可以说逻辑或运算符（“OR”）是“短路的”。除了逻辑或运算符外，其他短路运算符还包括逻辑与（“AND”）、空值合并、可选链和条件（三元）运算符。下面有更多例子：

```js
a || b * c; // 首先对 `a` 求值，如果 `a` 为真值则直接返回 `a`
a && b < c; // 首先对 `a` 求值，如果 `a` 为虚值则直接返回 `a`
a ?? (b || c); // 首先对 `a` 求值，如果 `a` 不是 `null` 或 `undefined` 则直接返回 `a`
a?.b.c; // 首先对 `a` 求值，如果 `a` 是 `null` 或 `undefined` 则直接返回 `undefined`
```

## 示例

```js
3 > 2 && 2 > 1;
// 返回 true

3 > 2 > 1;
// 返回 false，因为 3 > 2 是 true，然后 true 会在比较运算符中
// 被隐式转换为 1，因此 true > 1 会变为 1 > 1，结果是 false
// 加括号可以更清楚：(3 > 2) > 1
```

## 汇总表

下面的表格将所有运算符按照优先级的不同从高（19）到低（1）排列。

请注意，下表中故意不包含[展开语法](/zh-CN/docs/Web/JavaScript/Reference/Operators/Spread_syntax)——原因可以引用 [Stack Overflow 上的一个回答](https://stackoverflow.com/a/48656377)，“[展开语法不是一个运算符](https://stackoverflow.com/q/44934828/1048572)，因此没有优先级。它是数组字面量和函数调用（和对象字面量）语法的一部分。”

<table class="fullwidth-table">
    <tbody>
        <tr>
            <th>优先级</th>
            <th>运算符类型</th>
            <th>结合性</th>
            <th>运算符</th>
        </tr>
        <tr>
            <td>19</td>
            <td>{{jsxref("Operators/Grouping", "分组", "", 1)}}</td>
            <td>n/a（不相关）</td>
            <td><code>( … )</code></td>
        </tr>
        <tr>
            <td rowspan="5">18</td>
            <td>{{jsxref("Operators/Property_accessors", "成员访问", "#点号表示法", 1)}}</td>
            <td>从左到右</td>
            <td><code>… . …</code></td>
        </tr>
        <tr>
            <td>{{jsxref("Operators/Property_accessors", "需计算的成员访问", "#方括号表示法", 1)}}</td>
            <td>从左到右</td>
            <td><code>… [ … ]</code></td>
        </tr>
        <tr>
            <td>{{jsxref("Operators/new","new")}}（带参数列表）</td>
            <td>n/a</td>
            <td><code>new … ( … )</code></td>
        </tr>
        <tr>
            <td><a href="/zh-CN/docs/Web/JavaScript/Guide/Functions">函数调用</a></td>
            <td>从左到右</td>
            <td><code>… ( <var>… </var>)</code></td>
        </tr>
        <tr>
            <td><a href="/zh-CN/docs/Web/JavaScript/Reference/Operators/Optional_chaining">可选链（Optional chaining）</a></td>
            <td>从左到右</td>
            <td><code>?.</code></td>
        </tr>
        <tr>
            <td>17</td>
            <td>{{jsxref("Operators/new","new")}}（无参数列表）</td>
            <td>从右到左</td>
            <td><code>new …</code></td>
        </tr>
        <tr>
            <td rowspan="2">16</td>
            <td>{{jsxref("Operators","后置递增","#自增和自减", 1)}}</td>
            <td rowspan="2">n/a</td>
            <td><code>… ++</code></td>
        </tr>
        <tr>
            <td>{{jsxref("Operators","后置递减","#自增和自减", 1)}}</td>
            <td><code>… --</code></td>
        </tr>
        <tr>
            <td rowspan="10">15</td>
            <td><a href="/zh-CN/docs/Web/JavaScript/Reference/Operators/Logical_NOT">逻辑非 (!)</a></td>
            <td rowspan="10">从右到左</td>
            <td><code>! …</code></td>
        </tr>
        <tr>
            <td><a href="/zh-CN/docs/Web/JavaScript/Reference/Operators/Bitwise_NOT">按位非 (~)</a></td>
            <td><code>~ …</code></td>
        </tr>
        <tr>
            <td><a href="/zh-CN/docs/Web/JavaScript/Reference/Operators/Unary_plus">一元加法 (+)</a></td>
            <td><code>+ …</code></td>
        </tr>
        <tr>
            <td><a href="/zh-CN/docs/Web/JavaScript/Reference/Operators/Unary_negation">一元减法 (-)</a></td>
            <td><code>- …</code></td>
        </tr>
        <tr>
            <td>{{jsxref("Operators","前置递增","#自增和自减", 1)}}</td>
            <td><code>++ …</code></td>
        </tr>
        <tr>
            <td>{{jsxref("Operators","前置递减","#自增和自减", 1)}}</td>
            <td><code>-- …</code></td>
        </tr>
        <tr>
            <td>{{jsxref("Operators/typeof", "typeof")}}</td>
            <td><code>typeof …</code></td>
        </tr>
        <tr>
            <td>{{jsxref("Operators/void", "void")}}</td>
            <td><code>void …</code></td>
        </tr>
        <tr>
            <td>{{jsxref("Operators/delete", "delete")}}</td>
            <td><code>delete …</code></td>
        </tr>
        <tr>
            <td>{{jsxref("Operators/await", "await")}}</td>
            <td><code>await …</code></td>
        </tr>
        <tr>
            <td>14</td>
            <td><a href="/zh-CN/docs/Web/JavaScript/Reference/Operators/Exponentiation">幂 (**)</a></td>
            <td>从右到左</td>
            <td><code>… ** …</code></td>
        </tr>
        <tr>
            <td rowspan="3">13</td>
            <td><a href="/zh-CN/docs/Web/JavaScript/Reference/Operators/Multiplication">乘法 (*)</a></td>
            <td rowspan="3">从左到右</td>
            <td><code>… * …</code></td>
        </tr>
        <tr>
            <td><a href="/zh-CN/docs/Web/JavaScript/Reference/Operators/Division">除法 (/)</a></td>
            <td><code>… / …</code></td>
        </tr>
        <tr>
            <td><a href="/zh-CN/docs/Web/JavaScript/Reference/Operators/Remainder">取余 (%)</a></td>
            <td><code>… % …</code></td>
        </tr>
        <tr>
            <td rowspan="2">12</td>
            <td><a href="/zh-CN/docs/Web/JavaScript/Reference/Operators/Addition">加法 (+)</a></td>
            <td rowspan="2">从左到右</td>
            <td><code>… + …</code></td>
        </tr>
        <tr>
            <td><a href="/zh-CN/docs/Web/JavaScript/Reference/Operators/Subtraction">减法 (-)</a></td>
            <td><code>… - …</code></td>
        </tr>
        <tr>
            <td rowspan="3">11</td>
            <td><a href="/zh-CN/docs/Web/JavaScript/Reference/Operators/Left_shift">按位左移 (&lt;&lt;)</a></td>
            <td rowspan="3">从左到右</td>
            <td><code>… &lt;&lt; …</code></td>
        </tr>
        <tr>
            <td><a href="/zh-CN/docs/Web/JavaScript/Reference/Operators/Right_shift">按位右移 (&gt;&gt;)</a></td>
            <td><code>… &gt;&gt; …</code></td>
        </tr>
        <tr>
            <td><a href="/zh-CN/docs/Web/JavaScript/Reference/Operators/Unsigned_right_shift">无符号右移 (&gt;&gt;&gt;)</a></td>
            <td><code>… &gt;&gt;&gt; …</code></td>
        </tr>
        <tr>
            <td rowspan="6">10</td>
            <td><a href="/zh-CN/docs/Web/JavaScript/Reference/Operators/Less_than">小于 (&lt;)</a></td>
            <td rowspan="6">从左到右</td>
            <td><code>… &lt; …</code></td>
        </tr>
        <tr>
            <td><a href="/zh-CN/docs/Web/JavaScript/Reference/Operators/Less_than_or_equal">小于等于 (&lt;=)</a></td>
            <td><code>… &lt;= …</code></td>
        </tr>
        <tr>
            <td><a href="/zh-CN/docs/Web/JavaScript/Reference/Operators/Greater_than">大于 (&gt;)</a></td>
            <td><code>… &gt; …</code></td>
        </tr>
        <tr>
            <td><a href="/zh-CN/docs/Web/JavaScript/Reference/Operators/Greater_than_or_equal">大于等于 (&gt;=)</a></td>
            <td><code>… &gt;= …</code></td>
        </tr>
        <tr>
            <td>{{jsxref("Operators/in", "in")}}</td>
            <td><code>… in …</code></td>
        </tr>
        <tr>
            <td>{{jsxref("Operators/instanceof", "instanceof")}}</td>
            <td><code>… instanceof …</code></td>
        </tr>
        <tr>
            <td rowspan="4">9</td>
            <td><a href="/zh-CN/docs/Web/JavaScript/Reference/Operators/Equality">相等 (==)</a></td>
            <td rowspan="4">从左到右</td>
            <td><code>… == …</code></td>
        </tr>
        <tr>
            <td><a href="/zh-CN/docs/Web/JavaScript/Reference/Operators/Inequality">不相等 (!=)</a></td>
            <td><code>… != …</code></td>
        </tr>
        <tr>
            <td><a href="/zh-CN/docs/Web/JavaScript/Reference/Operators/Strict_equality">一致/严格相等 (===)</a></td>
            <td><code>… === …</code></td>
        </tr>
        <tr>
            <td><a href="/zh-CN/docs/Web/JavaScript/Reference/Operators/Strict_inequality">不一致/严格不相等 (!==)</a></td>
            <td><code>… !== …</code></td>
        </tr>
        <tr>
            <td>8</td>
            <td><a href="/zh-CN/docs/Web/JavaScript/Reference/Operators/Bitwise_AND">按位与 (&amp;)</a></td>
            <td>从左到右</td>
            <td><code>… &amp; …</code></td>
        </tr>
        <tr>
            <td>7</td>
            <td><a href="/zh-CN/docs/Web/JavaScript/Reference/Operators/Bitwise_XOR">按位异或 (^)</a></td>
            <td>从左到右</td>
            <td><code>… ^ …</code></td>
        </tr>
        <tr>
            <td>6</td>
            <td><a href="/zh-CN/docs/Web/JavaScript/Reference/Operators/Bitwise_OR">按位或 (|)</a></td>
            <td>从左到右</td>
            <td><code>… | …</code></td>
        </tr>
        <tr>
            <td>5</td>
            <td><a href="/zh-CN/docs/Web/JavaScript/Reference/Operators/Logical_AND">逻辑与 (&amp;&amp;)</a></td>
            <td>从左到右</td>
            <td><code>… &amp;&amp; …</code></td>
        </tr>
        <tr>
            <td rowspan="2">4</td>
            <td><a href="/zh-CN/docs/Web/JavaScript/Reference/Operators/Logical_OR">逻辑或 (||)</a></td>
            <td>从左到右</td>
            <td><code>… || …</code></td>
        </tr>
        <tr>
            <td><a href="/zh-CN/docs/Web/JavaScript/Reference/Operators/Nullish_coalescing">空值合并 (??)</a></td>
            <td>从左到右</td>
            <td><code>… ?? …</code></td>
        </tr>
        <tr>
            <td>3</td>
            <td><a href="/zh-CN/docs/Web/JavaScript/Reference/Operators/Conditional_operator">条件（三元）运算符</a></td>
            <td>从右到左</td>
            <td><code>… ? … : …</code></td>
        </tr>
        <tr>
            <td rowspan="16">2</td>
            <td rowspan="16"><a href="/zh-CN/docs/Web/JavaScript/Reference/Operators#赋值运算符">赋值</a></td>
            <td rowspan="16">从右到左</td>
            <td><code>… = …</code></td>
        </tr>
        <tr>
            <td><code>… += …</code></td>
        </tr>
        <tr>
            <td><code>… -= …</code></td>
        </tr>
        <tr>
            <td><code>… **= …</code></td>
        </tr>
        <tr>
            <td><code>… *= …</code></td>
        </tr>
        <tr>
            <td><code>… /= …</code></td>
        </tr>
        <tr>
            <td><code>… %= …</code></td>
        </tr>
        <tr>
            <td><code>… &lt;&lt;= …</code></td>
        </tr>
        <tr>
            <td><code>… &gt;&gt;= …</code></td>
        </tr>
        <tr>
            <td><code>… &gt;&gt;&gt;= …</code></td>
        </tr>
        <tr>
            <td><code>… &amp;= …</code></td>
        </tr>
        <tr>
            <td><code>… ^= …</code></td>
        </tr>
        <tr>
            <td><code>… |= …</code></td>
        </tr>
        <tr>
            <td><code>… &amp;&amp;= …</code></td>
        </tr>
        <tr>
            <td><code>… ||= …</code></td>
        </tr>
        <tr>
            <td><code>… ??= …</code></td>
        </tr>
        <tr>
            <td>1</td>
            <td><a href="/zh-CN/docs/Web/JavaScript/Reference/Operators/Comma_operator">逗号 / 序列</a></td>
            <td>从左到右</td>
            <td><code>… , …</code></td>
        </tr>
    </tbody>
</table>

---
# Source: index.md
---
---
title: 异步函数（async function）表达式
slug: Web/JavaScript/Reference/Operators/async_function
---

**`async function`** 关键字可用于定义表达式中的异步函数。

你还可以使用[异步函数声明](/zh-CN/docs/Web/JavaScript/Reference/Statements/async_function)。

## 语法

```js-nolint
async function (param0) {
  statements
}
async function (param0, param1) {
  statements
}
async function (param0, param1, /* … ,*/ paramN) {
  statements
}

async function name(param0) {
  statements
}
async function name(param0, param1) {
  statements
}
async function name(param0, param1, /* … ,*/ paramN) {
  statements
}
```

异步函数也可以使用[箭头语法](/zh-CN/docs/Web/JavaScript/Reference/Functions/Arrow_functions)进行定义。

### 参数

- `name` {{optional_inline}}
  - : 函数名称，可省略。如果省略则这个函数将成为*匿名*函数。该名称仅可在本函数中使用。
- `paramN` {{optional_inline}}
  - : 传入函数的形参名称。
- `statements` {{optional_inline}}
  - : 构成函数主体的语句。

## 描述

`async function` 表达式与{{jsxref("Statements/async_function", "异步函数语句", "", 1)}}非常相似，语法也基本相同。异步 `function` 表达式和异步 `function` 语句之间的主要区别在于*函数名称*，它可以在 `async function` 表达式中省略，从而创建一个*匿名*函数。`async function` 表达式可以用作 [IIFE](/zh-CN/docs/Glossary/IIFE)（立即执行函数表达式，Immediately Invoked Function Expression），它在定义后立即运行。参见[函数](/zh-CN/docs/Web/JavaScript/Reference/Functions)章节以获取更多信息。

## 示例

### 简单示例

```js
function resolveAfter2Seconds(x) {
  return new Promise((resolve) => {
    setTimeout(() => {
      resolve(x);
    }, 2000);
  });
}

// 赋值给变量的异步函数表达式
const add = async function (x) {
  const a = await resolveAfter2Seconds(20);
  const b = await resolveAfter2Seconds(30);
  return x + a + b;
};

add(10).then((v) => {
  console.log(v); // 4 秒后打印 60
});

// 用作 IIFE 的异步函数表达式
(async function (x) {
  const p1 = resolveAfter2Seconds(20);
  const p2 = resolveAfter2Seconds(30);
  return x + (await p1) + (await p2);
})(10).then((v) => {
  console.log(v); // 2 秒后打印 60
});
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- {{jsxref("Statements/async_function", "异步函数", "", 1)}}
- {{jsxref("AsyncFunction")}} 对象
- {{jsxref("Operators/await", "await")}}

---
# Source: index.md
---
---
title: 严格不相等（!==）
slug: Web/JavaScript/Reference/Operators/Strict_inequality
---

严格不相等运算符（`!==`）检查它的两个对象是否不相等，返回一个布尔结果。与[不相等](/zh-CN/docs/Web/JavaScript/Reference/Operators/Inequality)运算符不同，严格不相等运算符总是认为不同类型的对象是不同的。

{{InteractiveExample("JavaScript Demo: Expressions - Strict inequality operator")}}

```js interactive-example
console.log(1 !== 1);
// Expected output: false

console.log("hello" !== "hello");
// Expected output: false

console.log("1" !== 1);
// Expected output: true

console.log(0 !== false);
// Expected output: true
```

## 语法

```js-nolint
x !== y
```

## 描述

严格不相等运算符检查其对象是否不相等。它是[严格相等](/zh-CN/docs/Web/JavaScript/Reference/Operators/Strict_equality)运算符的否定，因此下面两行总是会给出相同的结果：

```js
x !== y;

!(x === y);
```

有关比较算法的详细信息，请参阅[严格相等](/zh-CN/docs/Web/JavaScript/Reference/Operators/Strict_equality)运算符的页面。

与严格相等运算符一样，严格不相等算符始终认为不同类型的对象是不同的：

```js
3 !== "3"; // true
```

## 示例

### 比较相同类型的对象

```js
"hello" !== "hello"; // false
"hello" !== "hola"; // true

3 !== 3; // false
3 !== 4; // true

true !== true; // false
true !== false; // true

null !== null; // false
```

### 比较不同类型的操作数

```js
"3" !== 3; // true
true !== 1; // true
null !== undefined; // true
```

### 比较对象

```js
const object1 = {
  key: "value",
};

const object2 = {
  key: "value",
};

console.log(object1 !== object2); // true
console.log(object1 !== object1); // false
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- [相等运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Equality)
- [不相等运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Inequality)
- [严格相等运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Strict_equality)

---
# Source: index.md
---
---
title: 右移（>>）
slug: Web/JavaScript/Reference/Operators/Right_shift
---

**右移运算符**（**`>>`**）将一个操作数的二进制表示形式向右移动指定位数，该操作数可以是数值或者 BigInt 类型。右边移出位被丢弃，左边移出的空位补符号位（最左边那位）。该操作也称为“符号位传播右移”（sign-propagating right shift）或“算术右移”（arithmetic right shift），因为返回值的符号位与第一个操作数的符号位相同。

{{InteractiveExample("JavaScript Demo: Expressions - Right shift operator")}}

```js interactive-example
const a = 5; //  00000000000000000000000000000101
const b = 2; //  00000000000000000000000000000010
const c = -5; //  11111111111111111111111111111011

console.log(a >> b); //  00000000000000000000000000000001
// Expected output: 1

console.log(c >> b); //  11111111111111111111111111111110
// Expected output: -2
```

## 语法

```js-nolint
x >> y
```

## 描述

`>>` 运算符针对这两种操作数的类型进行了重载：数值和 [BigInt](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/BigInt)。对于数值，该运算符返回一个 32 位整数；对于 BigInt 类型，该运算符返回一个 BigInt。右移运算符首先[将两个操作数强制转换为数值](/zh-CN/docs/Web/JavaScript/Guide/Data_structures#强制数字类型转换)并测试它们的类型。如果两个操作数都转换成 BigInt，则执行 BigInt 右移；否则，它将两个操作数都转换为 [32 位整数](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Number#固定宽度数值转换)并执行数值右移。如果一个操作数变为 BigInt 而另一个变为数值，则会抛出 {{jsxref("TypeError")}}。

由于新的数字最左边位与之前数字的最左边位是相同值，故符号位（最左边的位）不会改变，因此被称为“符号位传播”（sign-propagating）。

运算符以[二进制补码](https://zh.wikipedia.org/wiki/二補數)的形式对左操作数进行运算。考虑十进制（以 10 为底）数字 `9` 和 `-9` 的 `32` 位二进制表示：

```js
     9 (十进制): 00000000000000000000000000001001 (二进制)
    -9 (十进制): 11111111111111111111111111110111 (二进制)
```

十进制（以 10 为底）负数 `-9` 的二进制补码表示是将其相反数（即 `9`）的二进制表示 `00000000000000000000000000001001` 的所有位取反，再加 `1`。

这两个数的二进制表示的符号位由其最左边的位决定：对于十进制正数 `9`，二进制表示的最左边位为 `0`，对于十进制负数 `-9`，二进制表示的最左边位是 `1`。

给定十进制（以 10 为底）数 `9` 和 `-9` 的二进制表示：

`9 >> 2` 得到 `2`：

```js
     9 (十进制): 00000000000000000000000000001001 (二进制)
                  --------------------------------
9 >> 2 (十进制): 00000000000000000000000000000010 (二进制) = 2 (十进制)
```

请注意最右边的 `01` 是如何移出的，最左边的 `00` 是如何从左边移入的。

`-9 >> 2` 得到 `-3`：

```js
     -9 (十进制): 11111111111111111111111111110111 (二进制)
                   --------------------------------
-9 >> 2 (十进制): 11111111111111111111111111111101 (二进制) = -3 (十进制)
```

请注意最右边的 `11` 是如何移出的。但最左边的位情况稍有不同：由于 `-9` 是负数，它的符号位（即最左边的位）是 `1`，因此右移 2 位时会在最左边补上 `11`，这便保留了负号。

二进制表示 `11111111111111111111111111111101` 等于十进制（以 10 为底）负数 `-3`，因为所有负整数都以[二进制补码](https://zh.wikipedia.org/wiki/二補數)的形式存储，而 `-3` 的二进制补码可以通过将十进制（以 10 为底）正数 `3` 的二进制表示（即 `00000000000000000000000000000011`）的所有位先取反，然后加 `1`。

如果左操作数是一个超过 32 位的数字，则会丢弃最高有效位。例如，以下超过 32 位的整数将被转换为 32 位整数：

<!-- autocorrect-disable -->

```plain
丢弃前：11100110111110100000000000000110000000000001
丢弃后：            10100000000000000110000000000001
```

<!-- autocorrect-enable -->

右操作数将被转换为无符号 32 位整数，然后取模 32，因此实际移位偏移量将始终是 0 到 31 之间的正整数，包括 0 和 31。例如，`100 >> 32` 与 `100 >> 0` 相同（结果都是 `100`），因为 32 模 32 为 0。

BigInt 在使用右移时不会产生截断现象。从概念上讲，正 BigInt 具有无限数量的前导位 `0`，而负 BigInt 具有无限数量的前导位 `1`。

将任何数字 `x` 右移 `0` 可以将 `x` 转换为 32 位整数。不要使用 `>> 0` 将数字截断为整数；使用 [`Math.trunc()`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Math/trunc) 代替。

## 示例

### 使用右移操作

```js
9 >> 2; //  2
-9 >> 2; // -3

9n >> 2n; // 2n
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- [JS 指南中的位运算](/zh-CN/docs/Web/JavaScript/Guide/Expressions_and_operators#位运算符)
- [右移赋值运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Right_shift_assignment)
- [无符号右移运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Unsigned_right_shift)

---
# Source: index.md
---
---
title: 展开语法（...）
slug: Web/JavaScript/Reference/Operators/Spread_syntax
---

**spread (`...`)** 语法允许迭代数组或字符串等可迭代字符串在预期有零个或更多参数（用于函数调用）或元素（用于数组字面量）的地方进行扩展。在对象字面量中，扩展语法枚举对象的属性，并将键值对添加到正在创建的对象中。

展开语法看起来与剩余参数语法一模一样。在某种程度上，扩展语法与剩余参数语法正好相反。扩展语法是将数组“扩展”为元素，而其余语法是将多个元素收集起来，然后“浓缩”为一个元素。请参阅[剩余参数](/zh-CN/docs/Web/JavaScript/Reference/Functions/rest_parameters)和[剩余属性](/zh-CN/docs/Web/JavaScript/Reference/Operators/Destructuring#剩余属性和剩余元素) 。

{{InteractiveExample("JavaScript Demo: Spread syntax (...)")}}

```js interactive-example
function sum(x, y, z) {
  return x + y + z;
}

const numbers = [1, 2, 3];

console.log(sum(...numbers));
// Expected output: 6

console.log(sum.apply(null, numbers));
// Expected output: 6
```

## 语法

```js-nolint
myFunction(a, ...iterableObj, b)
[1, ...iterableObj, '4', 'five', 6]
{ ...obj, key: 'value' }
```

## 示例

### 在函数调用时使用展开语法

#### 等价于 apply 的方式

如果想将数组元素迭代为函数参数，一般使用{{jsxref( "Function.prototype.apply")}} 的方式进行调用。

```js
function myFunction(x, y, z) {}
var args = [0, 1, 2];
myFunction.apply(null, args);
```

有了展开语法，可以这样写：

```js
function myFunction(x, y, z) {}
var args = [0, 1, 2];
myFunction(...args);
```

所有参数都可以通过展开语法来传值，也不限制多次使用展开语法。

```js
function myFunction(v, w, x, y, z) {}
var args = [0, 1];
myFunction(-1, ...args, 2, ...[3]);
```

#### 在 new 表达式中应用

使用 `new` 关键字来调用构造函数时，不能**直接**使用数组 + `apply` 的方式（`apply` 执行的是调用 `[[Call]]` , 而不是构造 `[[Construct]]`）。当然，有了展开语法，将数组展开为构造函数的参数就很简单了：

```js
var dateFields = [1970, 0, 1]; // 1970 年 1 月 1 日
var d = new Date(...dateFields);
```

如果不使用展开语法，想将数组元素传给构造函数，实现方式可能是这样的：

```js
function applyAndNew(constructor, args) {
  function partial() {
    return constructor.apply(this, args);
  }
  if (typeof constructor.prototype === "object") {
    partial.prototype = Object.create(constructor.prototype);
  }
  return partial;
}

function myConstructor() {
  console.log("arguments.length: " + arguments.length);
  console.log(arguments);
  this.prop1 = "val1";
  this.prop2 = "val2";
}

var myArguments = ["hi", "how", "are", "you", "mr", null];
var myConstructorWithArguments = applyAndNew(myConstructor, myArguments);

console.log(new myConstructorWithArguments());
// (myConstructor 构造函数中):           arguments.length: 6
// (myConstructor 构造函数中):           ["hi", "how", "are", "you", "mr", null]
// ("new myConstructorWithArguments"中): {prop1: "val1", prop2: "val2"}
```

### 构造字面量数组时使用展开语法

#### 构造字面量数组时更给力！

没有展开语法的时候，只能组合使用 `push`, `splice`, `concat` 等方法，来将已有数组元素变成新数组的一部分。有了展开语法，通过字面量方式，构造新数组会变得更简单、更优雅：

```js
var parts = ["shoulders", "knees"];
var lyrics = ["head", ...parts, "and", "toes"];
// ["head", "shoulders", "knees", "and", "toes"]
```

和参数列表的展开类似， `...` 在构造字面量数组时，可以在任意位置多次使用。

#### 数组拷贝 (copy)

```js
var arr = [1, 2, 3];
var arr2 = [...arr]; // like arr.slice()
arr2.push(4);

// arr2 此时变成 [1, 2, 3, 4]
// arr 不受影响
```

**提示：** 实际上，展开语法和 {{jsxref("Object.assign()")}} 行为一致，执行的都是浅拷贝 (只遍历一层)。如果想对多维数组进行深拷贝，下面的示例就有些问题了。

```js
var a = [[1], [2], [3]];
var b = [...a];
b.shift().shift(); // 1
// Now array a is affected as well: [[], [2], [3]]
```

#### 连接多个数组

{{jsxref("Array.concat")}} 函数常用于将一个数组连接到另一个数组的后面。如果不使用展开语法，代码可能是下面这样的：

```js
var arr1 = [0, 1, 2];
var arr2 = [3, 4, 5];
// 将 arr2 中所有元素附加到 arr1 后面并返回
var arr3 = arr1.concat(arr2);
```

使用展开语法：

```js
var arr1 = [0, 1, 2];
var arr2 = [3, 4, 5];
var arr3 = [...arr1, ...arr2];
```

{{jsxref("Array.unshift")}} 方法常用于在数组的开头插入新元素/数组。不使用展开语法，示例如下：

```js
var arr1 = [0, 1, 2];
var arr2 = [3, 4, 5];
// 将 arr2 中的元素插入到 arr1 的开头
Array.prototype.unshift.apply(arr1, arr2); // arr1 现在是 [3, 4, 5, 0, 1, 2]
```

如果使用展开语法，代码如下：\[请注意，这里使用展开语法创建了一个新的 `arr1` 数组， {{jsxref("Array.unshift")}} 方法则是修改了原本存在的 `arr1` 数组]:

```js
var arr1 = [0, 1, 2];
var arr2 = [3, 4, 5];
arr1 = [...arr2, ...arr1]; // arr1 现在为 [3, 4, 5, 0, 1, 2]
```

### 构造字面量对象时使用展开语法

[Rest/Spread Properties for ECMAScript](https://github.com/tc39/proposal-object-rest-spread) 提议 (stage 4) 对 [字面量对象](/zh-CN/docs/Web/JavaScript/Reference/Operators/Object_initializer) 增加了展开特性。其行为是，将已有对象的所有可枚举 (enumerable) 属性拷贝到新构造的对象中。

浅拷贝 (Shallow-cloning，不包含 prototype) 和对象合并，可以使用更简短的展开语法。而不必再使用 {{jsxref("Object.assign()")}} 方式。

```js
var obj1 = { foo: "bar", x: 42 };
var obj2 = { foo: "baz", y: 13 };

var clonedObj = { ...obj1 };
// 克隆后的对象：{ foo: "bar", x: 42 }

var mergedObj = { ...obj1, ...obj2 };
// 合并后的对象：{ foo: "baz", x: 42, y: 13 }
```

**提示**: {{jsxref("Object.assign()")}} 函数会触发 [setters](/zh-CN/docs/Web/JavaScript/Reference/Functions/set)，而展开语法则不会。

**提示**: 不能替换或者模拟 {{jsxref("Object.assign()")}} 函数：

```plain
var obj1 = { foo: 'bar', x: 42 };
var obj2 = { foo: 'baz', y: 13 };
const merge = ( ...objects ) => ( { ...objects } );

var mergedObj = merge ( obj1, obj2);
// Object { 0: { foo: 'bar', x: 42 }, 1: { foo: 'baz', y: 13 } }

var mergedObj = merge ( {}, obj1, obj2);
// Object { 0: {}, 1: { foo: 'bar', x: 42 }, 2: { foo: 'baz', y: 13 } }
```

在这段代码中，展开操作符 (spread operator) 并没有按预期的方式执行：而是先将多个解构变为剩余参数 (rest parameter), 然后再将剩余参数展开为字面量对象。

### 只能用于可迭代对象

在数组或函数参数中使用展开语法时，该语法只能用于 [可迭代对象](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Symbol/iterator)：

```js
var obj = { key1: "value1" };
var array = [...obj]; // TypeError: obj is not iterable
```

### 展开多个值

在函数调用时使用展开语法，请注意不能超过 JavaScript 引擎限制的最大参数个数。更多详细信息，请参考：[`apply()`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Function/apply)。

## 剩余语法（剩余参数）

剩余语法 (Rest syntax) 看起来和展开语法完全相同，不同点在于，剩余参数用于解构数组和对象。从某种意义上说，剩余语法与展开语法是相反的：展开语法将数组展开为其中的各个元素，而剩余语法则是将多个元素收集起来并“凝聚”为单个元素。请参考：[剩余参数](/zh-CN/docs/Web/JavaScript/Reference/Functions/rest_parameters)。

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- [剩余参数](/zh-CN/docs/Web/JavaScript/Reference/Functions/rest_parameters)
- [剩余属性](/zh-CN/docs/Web/JavaScript/Reference/Operators/Destructuring#剩余属性)
- {{jsxref("Function.prototype.apply()")}}

---
# Source: index.md
---
---
title: 左移 (<<)
slug: Web/JavaScript/Reference/Operators/Left_shift
---

**左移操作符 (`<<`)** 将第一个操作数向左移动指定位数，左边超出的位数将会被清除，右边将会补零。

{{InteractiveExample("JavaScript Demo: Expressions - Left shift operator")}}

```js interactive-example
const a = 5; // 00000000000000000000000000000101
const b = 2; // 00000000000000000000000000000010

console.log(a << b); // 00000000000000000000000000010100
// Expected output: 20
```

## 语法

```plain
a << b
```

## 描述

左移操作符将第一个操作数向左移动指定位数，左边超出的位数将会被清除，右边将会补零。

例如， `9 << 2` 得出 36：

```js
     9 (十进制): 00000000000000000000000000001001 (二进制)
                 --------------------------------

9 << 2 (十进制): 00000000000000000000000000100100 (二进制) = 36 (十进制)
```

移动任意数字 `x` 至左边 `y` 位，得出 `x * 2 ** y`。
所以例如：`9 << 3` 等价于 `9 * 2³ = 9 * 8 = 72`。

## 示例

### 使用左移

```js
9 << 3; // 72

// 9 * 2³ = 9 * 8 = 72
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- [Bitwise operators in the JS guide](/zh-CN/docs/Web/JavaScript/Guide/Expressions_and_operators#位运算符)
- [Left shift assignment operator](/zh-CN/docs/Web/JavaScript/Reference/Operators/Left_shift_assignment)

---
# Source: index.md
---
---
title: 按位异或（^）
slug: Web/JavaScript/Reference/Operators/Bitwise_XOR
---

**按位异或**（**`^`**）运算符在两个操作数有且仅有一个对应的二进制位为 `1` 时，该位的结果值为 `1`。

{{InteractiveExample("JavaScript Demo: Expressions - Bitwise XOR", "shorter")}}

```js interactive-example
const a = 5; // 00000000000000000000000000000101
const b = 3; // 00000000000000000000000000000011

console.log(a ^ b); // 00000000000000000000000000000110
// Expected output: 6
```

## 语法

```js-nolint
a ^ b
```

## 描述

操作数被转换为 32 位整数并由一系列二进制位（0 和 1）表示。超过 32 位的数字会丢弃其最高有效位。例如，以下超过 32 位的整数将被转换为 32 位整数：

```plain
Before: 11100110111110100000000000000110000000000001
After:              10100000000000000110000000000001
```

第一个操作数中的每个位都与第二个操作数中的相应位配对：*第一位*到*第一位*、*第二位*到*第二位*，以此类推。

运算符应用于每一对位，结果按位构造。

异或或运算的真值表为：

| a   | b   | a XOR b |
| --- | --- | ------- |
| 0   | 0   | 0       |
| 0   | 1   | 1       |
| 1   | 0   | 1       |
| 1   | 1   | 0       |

```plain
     9 (base 10) = 00000000000000000000000000001001 (base 2)
    14 (base 10) = 00000000000000000000000000001110 (base 2)
                   --------------------------------
14 ^ 9 (base 10) = 00000000000000000000000000000111 (base 2) = 7 (base 10)
```

将任意数字 `x` 与 `0` 进行按位异或运算得到 `x`。

## 示例

### 使用按位异或

```js
// 9  (00000000000000000000000000001001)
// 14 (00000000000000000000000000001110)

14 ^ 9;
// 7  (00000000000000000000000000000111)
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- [JS 指南中的位运算符](/zh-CN/docs/Web/JavaScript/Guide/Expressions_and_operators#位运算符)
- [按位异或赋值运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Bitwise_XOR_assignment)

---
# Source: index.md
---
---
title: 无符号右移（>>>）
slug: Web/JavaScript/Reference/Operators/Unsigned_right_shift
---

**无符号右移运算符（`>>>`）**（零填充右移）将左操作数计算为无符号数，并将该数字的二进制表示形式移位为右操作数指定的位数，取模 32。向右移动的多余位将被丢弃，零位从左移入。其符号位变为 `0`，因此结果始终为非负数。与其他按位运算符不同，零填充右移返回一个无符号 32 位整数。

{{InteractiveExample("JavaScript Demo: Expressions - Unsigned right shift operator")}}

```js interactive-example
const a = 5; //  00000000000000000000000000000101
const b = 2; //  00000000000000000000000000000010
const c = -5; //  11111111111111111111111111111011

console.log(a >>> b); //  00000000000000000000000000000001
// Expected output: 1

console.log(c >>> b); //  00111111111111111111111111111110
// Expected output: 1073741822
```

## 语法

```js-nolint
a >>> b
```

## 描述

该运算符将第一个操作数向右移动指定的位数。向右移动的多余位将被丢弃。零位从左侧移入。其符号位变为 `0`，因此其表示的结果始终为非负数。与其他按位运算符不同，零填充右移返回无符号 32 位整数。

以十进制（以 10 为基数）数字 `9` 和 `-9` 的 32 位二进制表示为例：

```plain
     9 (base 10): 00000000000000000000000000001001 (base 2)
    -9 (base 10): 11111111111111111111111111110111 (base 2)
```

请注意，负十进制（以 10 为基数）数字 `-9` 的二进制表示形式是正十进制（以 10 为基数）数字 `9` 的[二进制补码](https://zh.wikipedia.org/wiki/二補數)。也就是说，它是通过反转 `00000000000000000000000000001001` 的所有位并添加 `1` 来计算的。

在这两种情况下，二进制数的符号都由其最左边的位给出：对于正十进制数 `9`，二进制表示的最左边位是 `0`，对于负十进制数 `-9`，二进制表示的最左边位是 `1`。

对于正数 `9`，零填充右移和[符号传播右移](/zh-CN/docs/Web/JavaScript/Reference/Operators/Right_shift)产生相同的结果：`9 >>> 2` 产生 `2`，与 `9 >> 2` 相同：

```plain
      9 (base 10): 00000000000000000000000000001001 (base 2)
                   --------------------------------
9 >>  2 (base 10): 00000000000000000000000000000010 (base 2) = 2 (base 10)
9 >>> 2 (base 10): 00000000000000000000000000000010 (base 2) = 2 (base 10)
```

请注意，最右边的两个位 `01` 被移出，两个零从左边移入。

但是，请注意 `-9` 会发生什么情况：`-9 >> 2`（[符号传播右移](/zh-CN/docs/Web/JavaScript/Reference/Operators/Right_shift)）产生 `-3`，但 `-9 >>> 2`（零填充右移）产生 1073741821：

```plain
      -9 (base 10): 11111111111111111111111111110111 (base 2)
                    --------------------------------
-9 >>  2 (base 10): 11111111111111111111111111111101 (base 2) = -3 (base 10)
-9 >>> 2 (base 10): 00111111111111111111111111111101 (base 2) = 1073741821 (base 10)
```

请注意最右边的两个位 `11` 是如何移出的。对于 `-9 >> 2`（[符号传播右移](/zh-CN/docs/Web/JavaScript/Reference/Operators/Right_shift)），最左边的 `1` 位的两个副本已从左侧移入，这保留了负号。另一方面，对于 `-9 >>> 2`（零填充右移），零从左移入，因此不会保留数字的负号，结果是一个（大）正数。

左操作数将被转换为无符号 32 位整数，这意味着浮点数将被截断，而超出 32 位边界的数字将溢出/下溢。

右操作数将转换为无符号的 32 位整数，然后取模 32，因此实际移位偏移量将始终是介于 0 和 31 之间的正整数（包括 0 和 31）。例如，`100 >>> 32` 与 `100 >>> 0` 相同（并产生 `100`），因为 32 模 32 是 0。

## 示例

### 使用无符号右移

```js
9 >>> 2; // 2
-9 >>> 2; // 1073741821
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- [JS 指南：位运算符](/zh-CN/docs/Web/JavaScript/Guide/Expressions_and_operators#位运算符)
- [无符号右移赋值运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Unsigned_right_shift_assignment)

---
# Source: index.md
---
---
title: instanceof
slug: Web/JavaScript/Reference/Operators/instanceof
---

**`instanceof`** 运算符用于检测构造函数的 `prototype` 属性是否出现在某个实例对象的原型链上。其返回值是一个布尔值。可以通过 [`Symbol.hasInstance`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Symbol/hasInstance) 来自定义该运算符的行为。

{{InteractiveExample("JavaScript Demo: instanceof operator")}}

```js interactive-example
function Car(make, model, year) {
  this.make = make;
  this.model = model;
  this.year = year;
}
const auto = new Car("Honda", "Accord", 1998);

console.log(auto instanceof Car);
// 预期输出：true

console.log(auto instanceof Object);
// 预期输出：true
```

## 语法

```js-nolint
object instanceof constructor
```

### 参数

- `object`
  - : 要测试的对象
- `constructor`
  - : 测试对照的构造函数

### 异常

- {{jsxref("TypeError")}}
  - : 如果 `constructor` 不是对象，或 `constructor` 没有 [`[Symbol.hasInstance]()`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Symbol/hasInstance) 方法（那么它一定是一个函数），则抛出该异常。

## 描述

`instanceof` 运算符用来检测 `constructor.prototype` 是否存在于参数 `object` 的原型链上。

```js
// 定义构造函数
function C() {}
function D() {}

const o = new C();

// true，因为：Object.getPrototypeOf(o) === C.prototype
o instanceof C;

// false，因为 D.prototype 不在 o 的原型链上
o instanceof D;

o instanceof Object; // true，原因如下：
C.prototype instanceof Object; // true

// 重新赋值 `constructor.prototype`：在实践中很罕见
C.prototype = {};
const o2 = new C();

o2 instanceof C; // true

// false，C.prototype 指向了一个空对象，这个空对象不在 o 的原型链上
o instanceof C;

D.prototype = new C(); // 继承
const o3 = new D();
o3 instanceof D; // true
o3 instanceof C; // true 因为 C.prototype 现在在 o3 的原型链上
```

需要注意的是，如果表达式 `obj instanceof Foo` 返回 `true`，则并不意味着该表达式会永远返回 `true`，因为 `Foo.prototype` 属性的值有可能会改变，改变之后的值很有可能不存在于 `obj` 的原型链上，这时原表达式的值就会成为 `false`。另外一种情况下，原表达式的值也会改变，就是改变对象 `obj` 的原型链的情况，虽然在目前的 ES 规范中，我们只能读取对象的原型而不能改变它，但借助于非标准的 `__proto__` 伪属性，是可以实现的。比如执行 `obj.__proto__ = {}` 之后，`obj instanceof Foo` 就会返回 `false` 了。

### `instanceof` 和多全局对象 (例如：多个 frame 或多个 window 之间的交互)

在浏览器中，我们的脚本可能需要在多个窗口之间进行交互。多个窗口意味着多个全局环境，不同的全局环境拥有不同的全局对象，从而拥有不同的内置类型构造函数。这可能会引发一些问题。比如，表达式 `[] instanceof window.frames[0].Array` 会返回 `false`，因为 `Array.prototype !== window.frames[0].Array.prototype`，并且数组从前者继承。

起初，你会认为这样并没有意义，但是当你在你的脚本中开始处理多个 frame 或多个 window 以及通过函数将对象从一个窗口传到另一个窗口时，这就是一个有效而强大的话题。比如，实际上你可以通过使用`Array.isArray(myObj)` 或者`Object.prototype.toString.call(myObj) === "[object Array]"` 来安全的检测传过来的对象是否是一个数组。

比如检测一个 `Nodes` 在另一个窗口中是不是 `SVGElement`，你可以使用`myNode instanceof myNode.ownerDocument.defaultView.SVGElement`

> [!NOTE]
> 在代码中使用 XPCOM `instanceof` 有特殊影响：如果查询接口成功执行后，`obj instanceof` _`xpcomInterface`_ (e.g. `Components.interfaces.nsIFile`) 调用`obj.QueryInterface(xpcomInterface)` 并且返回 `true` 。这种调用的副作用是在一次成功的 `instanceof` 测试后，你可以在 `obj` 上使用`xpcomInterface` 的属性。这与标准的 `JavaScript` 全局变量不同，即使 `obj` 来自不同的作用域，`obj instanceof xpcomInterface` 也可以按预期产生作用。

## 示例

### 演示 `String` 对象和 `Date` 对象都属于 `Object` 类型和一些特殊情况

下面的代码使用了 `instanceof` 来证明：`String` 和 `Date` 对象同时也属于`Object` 类型（他们是由 `Object` 类派生出来的）。

但是，使用对象字面量符号创建的对象在这里是一个例外：虽然原型未定义，但 `instanceof Object` 返回 `true`。

```js
var simpleStr = "This is a simple string";
var myString = new String();
var newStr = new String("String created with constructor");
var myDate = new Date();
var myObj = {};
var myNonObj = Object.create(null);

simpleStr instanceof String; // 返回 false，非对象实例，因此返回 false
myString instanceof String; // 返回 true
newStr instanceof String; // 返回 true
myString instanceof Object; // 返回 true

myObj instanceof Object; // 返回 true，尽管原型没有定义
({}) instanceof Object; // 返回 true，同上
myNonObj instanceof Object; // 返回 false，一种创建非 Object 实例的对象的方法

myString instanceof Date; //返回 false

myDate instanceof Date; // 返回 true
myDate instanceof Object; // 返回 true
myDate instanceof String; // 返回 false
```

### 演示 `mycar` 属于 `Car` 类型的同时又属于 `Object` 类型

下面的代码创建了一个类型 `Car`，以及该类型的对象实例 `mycar`. `instanceof` 运算符表明了这个 `mycar` 对象既属于 `Car` 类型，又属于 `Object` 类型。

```js
function Car(make, model, year) {
  this.make = make;
  this.model = model;
  this.year = year;
}
var mycar = new Car("Honda", "Accord", 1998);
var a = mycar instanceof Car; // 返回 true
var b = mycar instanceof Object; // 返回 true
```

### 不是...的实例

要检测对象不是某个构造函数的实例时，你可以这样做

```js
if (!(mycar instanceof Car)) {
  // Do something, like mycar = new Car(mycar)
}
```

这和以下代码完全不同

```js
if (!mycar instanceof Car)
```

这段代码永远会得到 `false`（`!mycar` 将在 `instanceof` 之前被处理，所以你总是在验证一个布尔值是否是 `Car` 的一个实例）。

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- [typeof](/zh-CN/docs/Web/JavaScript/Reference/Operators/typeof)
- {{jsxref("Symbol.hasInstance")}}
- {{jsxref("Object.prototype.isPrototypeOf")}}

---
# Source: index.md
---
---
title: 属性访问器
slug: Web/JavaScript/Reference/Operators/Property_accessors
l10n:
  sourceCommit: fad67be4431d8e6c2a89ac880735233aa76c41d4
---

**属性访问器**通过使用点或方括号符号来访问对象的属性。

{{InteractiveExample("JavaScript 演示：属性访问器", "taller")}}

```js interactive-example
const person1 = {};
person1["firstName"] = "张";
person1["lastName"] = "三";

console.log(person1.firstName);
// 期望输出："张"

const person2 = {
  firstName: "李",
  lastName: "四",
};

console.log(person2["lastName"]);
// 期望输出："四"
```

## 语法

```js-nolint
object.propertyName
object[expression]
object.#privateProperty
```

## 描述

我们可以将对象看做是一个*关联数组*（也称为：_映射_、_字典_、_散列表_、_查询表_）。这个数组中的*键*就是这个对象中[属性](/zh-CN/docs/Glossary/Property/JavaScript)的名称。

访问属性有两种方式：*点表示法*和*方括号表示法*。

### 点号表示法

在 `object.propertyName` 语法中，`propertyName` 必须是一个有效的 JavaScript [标识符](/zh-CN/docs/Web/JavaScript/Reference/Lexical_grammar#标识符)，也可以是一个[保留字](/zh-CN/docs/Web/JavaScript/Reference/Lexical_grammar#关键字)。例如，`object.$1` 有效，而 `object.1` 无效。

```js
const variable = object.propertyName;
object.propertyName = value;
```

```js
const object = {};
object.$1 = "foo";
console.log(object.$1); // 'foo'
```

```js-nolint example-bad
const object = {};
object.1 = "bar"; // SyntaxError
console.log(object.1); // SyntaxError
```

在这里，我们从 `document` 中访问了一个名为 `createElement` 的方法，并调用了它。

```js
document.createElement("pre");
```

如果对数字字面量使用方法，并且数字字面量没有指数且没有小数点，请在方法调用之前的点之前留出[空白字符](/zh-CN/docs/Glossary/Whitespace)，以防止点被解释为小数点。

```js-nolint
77 .toExponential();
// 或
77
.toExponential();
// 或
(77).toExponential();
// 或
77..toExponential();
// 或
77.0.toExponential();
// 因为 77. === 77.0，没有歧义
```

此外，[私有元素](/zh-CN/docs/Web/JavaScript/Reference/Classes/Private_elements)只能在定义它们的类中使用点符号访问。

### 方括号表示法

在 `object[expression]` 语法中，`expression` 应求值为表示属性名称的字符串或 [Symbol](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Symbol)。因此，它可以是任何字符串字面量形式，例如，包括 `1foo'`、`'!bar!'`，甚至是 `' '`（空格）。

```js
const variable = object[propertyName];
object[propertyName] = value;
```

以下调用的效果与前一个示例完全相同：

```js
document["createElement"]("pre");
```

方括号表示之前允许有空格。

```js-nolint
document ["createElement"]("pre");
```

传递对属性名求值的表达式与直接传递属性名的作用相同。

```js
const key = "name";
const getKey = () => "name";
const Obj = { name: "张三" };

Obj["name"]; // 返回“张三”
Obj[key]; // 求值为 Obj["name"]，并返回“张三”
Obj[getKey()]; // 求值为 Obj["name"]，并返回“张三”
```

不过，请注意不要使用方括号访问由外部输入给出名称的属性。这可能会使你的代码受到[对象注入攻击](https://github.com/eslint-community/eslint-plugin-security/blob/main/docs/the-dangers-of-square-bracket-notation.md)。

### 属性名称

属性名称必须是字符串或 [Symbol](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Symbol)。任何其他值，包括数值，都会被强制转换为字符串。由于 `1` 被强制转换为 `'1'`，因此以下示例会输出 `'值'`。

```js
const object = {};
object["1"] = "值";
console.log(object[1]);
```

以下代码也会输出 `'值'`，因为 `foo` 和 `bar` 被转换为相同的字符串（`"[object Object]"`）。

```js
const foo = { uniqueProp: 1 };
const bar = { uniqueProp: 2 };
const object = {};
object[foo] = "值";
console.log(object[bar]);
```

### 方法绑定

在谈到对象的属性时，通常会区分属性和方法。然而，属性/方法之间的区别不过是一种约定俗成的说法。方法是一种可以被调用的属性（例如，如果它的值是对 {{jsxref("Function")}} 实例的引用）。

方法并不与作为其属性的对象绑定。具体来说，方法中的 `this` 并不固定，也不一定指包含该方法的对象。相反，`this` 被函数调用“传递”。请参阅 [`this` 的引用](/zh-CN/docs/Web/JavaScript/Reference/Operators/this)。

## 示例

### 方括号表示法与 eval()

JavaScript 新手经常会犯一个错误，就是在可以使用方括号表示法的情况下使用了 {{jsxref("Global_Objects/eval", "eval()")}} 代替。

例如，许多脚本中经常出现以下语法。

```js
const x = eval(`document.forms.form_name.elements.${strFormControl}.value`);
```

`eval()` 很慢，应尽可能避免使用。而且，此时 `strFormControl` 必须是一个合法的标识符，这在一些表单控件的 name、`id` 值之中并不是必要的。所以，使用方括号表示法来代替会更好一些：

```js
const x = document.forms.form_name.elements[strFormControl].value;
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- {{jsxref("Object")}}
- {{jsxref("Object.defineProperty()")}}
- [可选链（`?.`）](/zh-CN/docs/Web/JavaScript/Reference/Operators/Optional_chaining)

---
# Source: index.md
---
---
title: 幂（**）
slug: Web/JavaScript/Reference/Operators/Exponentiation
---



**幂**（**`**`**）运算符返回第一个操作数取第二个操作数的幂的结果。它等价于 {{jsxref("Math.pow()")}}，不同之处在于，它还接受 [BigInt](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/BigInt) 作为操作数。

{{InteractiveExample("JavaScript Demo: Expressions - Exponentiation operator")}}

```js interactive-example
console.log(3 ** 4);
// Expected output: 81

console.log(10 ** -2);
// Expected output: 0.01

console.log(2 ** (3 ** 2));
// Expected output: 512

console.log((2 ** 3) ** 2);
// Expected output: 64
```

## 语法

```js-nolint
x ** y
```

## 描述

幂运算符是右结合的：`a ** b ** c` 等于 `a ** (b ** c)`。

在大多数语言里，比如 PHP、Python 等那些有幂运算符（`**`）的语言，幂运算符被定义有一个比一元运算符，比如一元的 `+` 和一元的 `-` 更高的运算顺序，但有一些例外。在 Bash 语言里，`**` 运算符被定义有一个比一元运算符更低的运算顺序。

在 JavaScript 中，不可能写出模棱两可的幂表达式。也就是说，你不能将一元运算符（`+/-/~/!/delete/void/typeof`）放在底数之前；[这样做会导致语法错误](/zh-CN/docs/Web/JavaScript/Reference/Errors/Unparenthesized_unary_expr_lhs_exponentiation)。

例如，`-2 ** 2` 在 Bash 中为 4，但在其他语言（如 Python）中为 -4。这在 JavaScript 中是无效的，因为操作不明确。你必须在两边加上括号——例如，作为 `-(2 ** 2)`——以使意图明确。

请注意，某些编程语言使用插入符号 <kbd>^</kbd> 进行求幂，但 JavaScript 使用该符号表示[逻辑异或运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Bitwise_XOR)。

`NaN ** 0`（和等价的 `Math.pow(NaN, 0)`）是 {{jsxref("NaN")}} 不通过数学运算传播的唯一情况——尽管操作数是 `NaN`，但它返回 `1`。此外，`base` 为 1 且 `exponent` 为非有限（±Infinity 或 `NaN`）的行为与 IEEE 754 不同，IEEE 754 指定结果应为 1，而 JavaScript 返回 `NaN` 以保持与其原始行为的向后兼容性。

## 示例

### 基本求幂

```js
2 ** 3; // 8
3 ** 2; // 9
3 ** 2.5; // 15.588457268119896
10 ** -1; // 0.1
NaN ** 2; // NaN
NaN ** 0; // 1
1 ** Infinity; // NaN
```

### 结合性

```js-nolint
2 ** 3 ** 2; // 512
2 ** (3 ** 2); // 512
(2 ** 3) ** 2; // 64
```

### 与一元运算符一起使用

取幂表达式的值的相反数：

```js
-(2 ** 2); // -4
```

将幂表达式的底数转化为一个负数：

```js
(-2) ** 2; // 4
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- [加法运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Addition)
- [减法运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Subtraction)
- [除法运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Division)
- [乘法运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Multiplication)
- [取余运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Remainder)
- [自增运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Increment)
- [自减运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Decrement)
- [一元减运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Unary_negation)
- [一元加运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Unary_plus)

---
# Source: index.md
---
---
title: 一元加（+）
slug: Web/JavaScript/Reference/Operators/Unary_plus
---

**一元加**（**`+`**）运算符在其操作数之前并计算其操作数，但会尝试将其[转换为数字](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Number#number_强制转换)，如果它还不是的话。

{{InteractiveExample("JavaScript Demo: Expressions - Unary plus operator", "taller")}}

```js interactive-example
const x = 1;
const y = -1;

console.log(+x);
// Expected output: 1

console.log(+y);
// Expected output: -1

console.log(+"");
// Expected output: 0

console.log(+true);
// Expected output: 1

console.log(+false);
// Expected output: 0

console.log(+"hello");
// Expected output: NaN
```

## 语法

```js-nolint
+x
```

## 描述

虽然一元减（`-`）也可以转换非数字，但一元加是将某些东西转换为数字的最快和首选方法，因为它不对数字执行任何其他操作。它可以转换整数和浮点数的字符串表示形式，以及非字符串值 `true`、`false` 和 `null`。支持十进制和十六进制（以 `0x` 为前缀）格式的整数。支持负数（但不适用于十六进制）。对 BigInt 值使用该运算符会引发 TypeError。如果它无法解析特定值，它将计算为 {{jsxref("NaN")}}。

## 示例

### 数字用法

```js
const x = 1;
const y = -1;

console.log(+x);
// 1
console.log(+y);
// -1
```

### 非数字用法

```js-nolint
+true  // 1
+false // 0
+null  // 0
+function (val) { return val; } // NaN
+1n    // throws TypeError: Cannot convert BigInt value to number
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- [加法运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Addition)
- [减法运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Subtraction)
- [除法运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Division)
- [乘法运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Multiplication)
- [取余运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Remainder)
- [求幂运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Exponentiation)
- [自增运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Increment)
- [自减运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Decrement)
- [一元减运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Unary_negation)

---
# Source: index.md
---
---
title: 自增（++）
slug: Web/JavaScript/Reference/Operators/Increment
---

**自增**（**`++`**）运算符对其操作数进行自增（加一），并根据运算符的位置返回自增之前或之后的值。

{{InteractiveExample("JavaScript Demo: Expressions - Increment operator")}}

```js interactive-example
let x = 3;
const y = x++;

console.log(`x:${x}, y:${y}`);
// Expected output: "x:4, y:3"

let a = 3;
const b = ++a;

console.log(`a:${a}, b:${b}`);
// Expected output: "a:4, b:4"
```

## 语法

```js-nolint
x++
++x
```

## 描述

如果使用后缀式，即将运算符放在操作数的后面（例如 `x++`），操作数会加一，然后返回加一之前的值。

如果使用前缀式，即将运算符放在操作数的前面（例如 `++x`），操作数会加一，然后返回加一之后的值。

自增运算符只能应用于引用的操作数（变量和对象属性，即有效的[赋值目标](/zh-CN/docs/Web/JavaScript/Reference/Operators/Assignment)）。`++x` 本身的计算结果是一个值，而不是一个引用，因此不能将多个自增运算符链接在一起。

```js example-bad
++(++x); // SyntaxError: Invalid left-hand side expression in prefix operation
```

## 示例

### 后缀式

```js
let x = 3;
const y = x++;

// x = 4
// y = 3
```

### 前缀式

```js
let x = 3;
const y = ++x;

// x = 4
// y = 4
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- [加法运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Addition)
- [减法运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Subtraction)
- [除法运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Division)
- [乘法运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Multiplication)
- [取余运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Remainder)
- [幂运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Exponentiation)
- [自减运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Decrement)
- [一元减运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Unary_negation)
- [一元加运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Unary_plus)

---
# Source: index.md
---
---
title: 解构
slug: Web/JavaScript/Reference/Operators/Destructuring
---

**解构**语法是一种 Javascript 语法。可以将数组中的值或对象的属性取出，赋值给其他变量。它可以在接收数据的位置使用（例如赋值的左侧或创建新标识符绑定的任何位置）。

{{InteractiveExample("JavaScript Demo: Expressions - Destructuring", "taller")}}

```js interactive-example
let a, b, rest;
[a, b] = [10, 20];

console.log(a);
// 期望输出：10

console.log(b);
// 期望输出：20

[a, b, ...rest] = [10, 20, 30, 40, 50];

console.log(rest);
// 期望输出：Array [30, 40, 50]
```

## 语法

```js-nolint
const [a, b] = array;
const [a, , b] = array;
const [a = aDefault, b] = array;
const [a, b, ...rest] = array;
const [a, , b, ...rest] = array;
const [a, b, ...{ pop, push }] = array;
const [a, b, ...[c, d]] = array;

const { a, b } = obj;
const { a: a1, b: b1 } = obj;
const { a: a1 = aDefault, b = bDefault } = obj;
const { a, b, ...rest } = obj;
const { a: a1, b: b1, ...rest } = obj;
const { [key]: a } = obj;

let a, b, a1, b1, c, d, rest, pop, push;
[a, b] = array;
[a, , b] = array;
[a = aDefault, b] = array;
[a, b, ...rest] = array;
[a, , b, ...rest] = array;
[a, b, ...{ pop, push }] = array;
[a, b, ...[c, d]] = array;

({ a, b } = obj); // brackets are required
({ a: a1, b: b1 } = obj);
({ a: a1 = aDefault, b = bDefault } = obj);
({ a, b, ...rest } = obj);
({ a: a1, b: b1, ...rest } = obj);
```

## 描述

对象和数组字面量表达式提供了一种简单的方法来创建*临时的*数据包。

```js
const arr = [a, b, c];
```

解构使用类似的语法，但在赋值的左侧定义了要从原变量中取出哪些值。

```js
const arr = [1, 2, 3];
const [a, b, c] = arr;
// a = 1, b = 2, c = 3
```

同样，你可以在赋值语句的左侧解构对象。

```js
const obj = { a, b, c };
const { a, b, c } = obj;
// 等同于：
// const a = obj.a, b = obj.b, c = obj.c;

const obj = { prop1: x, prop2: y, prop3: z };
const { prop1: x, prop2: y, prop3: z } = obj;
// 等同于：
// const x = obj.prop1, y = obj.prop2, z = obj.prop3;
```

这种功能类似于 Perl 和 Python 等语言中存在的特性。

有关数组或对象解构的特定功能，请参阅下面的各个[示例](#示例)。

### 绑定与赋值

对于对象和数组的解构，有两种解构模式：*{{Glossary("binding", "绑定")}}模式*和*赋值模式*，它们的语法略有不同。

在绑定模式中，模式以声明关键字（`var`、`let` 或 `const`）开始。然后，每个单独的属性必须绑定到一个变量或进一步解构。

```js
const obj = { a: 1, b: { c: 2 } };
const {
  a,
  b: { c: d },
} = obj;
// 变量 `a` 和 `d` 被绑定
```

所有变量共享相同的声明，因此，如果你希望某些变量可重新分配，而其他变量是只读的，则可能需要解构两次——一次使用 `let`，一次使用 `const`。

```js
const obj = { a: 1, b: { c: 2 } };
const { a } = obj; // a 为常量
let {
  b: { c: d },
} = obj; // d 可被重新赋值
```

你也可以在其他许多为你绑定变量的语法中，使用绑定解构模式。这些包括：

- [`for...in`](/zh-CN/docs/Web/JavaScript/Reference/Statements/for...in)、[`for...of`](/zh-CN/docs/Web/JavaScript/Reference/Statements/for...of) 和 [`for await...of`](/zh-CN/docs/Web/JavaScript/Reference/Statements/for-await...of) 循环中的循环变量，
- [函数](/zh-CN/docs/Web/JavaScript/Reference/Functions)参数，
- [`catch`](/zh-CN/docs/Web/JavaScript/Reference/Statements/try...catch) 绑定变量。

在赋值模式中，模式不以关键字开头。每个解构属性都被赋值给一个赋值目标——这个赋值目标可以事先用 `var` 或 `let` 声明，也可以是另一个对象的属性——一般来说，可以是任何可以出现在赋值表达式左侧的东西。

```js
const numbers = [];
const obj = { a: 1, b: 2 };
({ a: numbers[0], b: numbers[1] } = obj);
// 属性 `a` 和 `b` 被赋值给了 `numbers` 的属性
```

> [!NOTE]
> 当使用对象字面量解构而不带声明时，在赋值语句周围必须添加括号 `( ... )`。
>
> `{ a, b } = { a: 1, b: 2 }` 不是有效的独立语法，因为左侧的 `{a, b}` 被视为块而不是对象字面量。但是，`({ a, b } = { a: 1, b: 2 })` 是有效的，`const { a, b } = { a: 1， b: 2 }` 也是有效的。
>
> 如果你的编码风格不包括尾随分号，则 `( ... )` 表达式前面需要有一个分号，否则它可能用于执行前一行的函数。

请注意，上述代码在等效的*绑定模式*中不是有效的语法：

```js-nolint example-bad
const numbers = [];
const obj = { a: 1, b: 2 };
const { a: numbers[0], b: numbers[1] } = obj;

// 等同于：
//   const numbers[0] = obj.a;
//   const numbers[1] = obj.b;
// 无效代码
```

你只能在[赋值](/zh-CN/docs/Web/JavaScript/Reference/Operators/Assignment)运算符的左侧使用赋值模式。不能与复合赋值运算符如 `+=` 或 `*=` 一起使用。

### 默认值

每个解构属性都可以有一个*默认值*。当属性不存在或值为 `undefined` 时，将使用默认值。如果属性的值为 `null`，则不使用默认值。

```js
const [a = 1] = []; // a 是 1
const { b = 2 } = { b: undefined }; // b 是 2
const { c = 2 } = { c: null }; // c 是 null
```

默认值可以是任何表达式。仅在必要时对其进行求值。

```js
const { b = console.log("hey") } = { b: 2 };
// 不会输出任何东西，因为 `b` 的值已经被定义，所以不需要求默认值。
```

### 剩余属性和剩余元素

你可以使用剩余属性（`...rest`）结束解构模式。对数组解构时，此模式会将数组的剩余元素存储到新的名为 `rest`（或在代码中指定的其他名字）的数组中。对对象解构时，此模式会将对象剩余的可枚举属性存储到新的名为 `rest` 的对象中。

更正式的说，`...rest` 语法在数组解构中被称作“剩余元素”，在对象解构中被称作“剩余属性”，但我们通常统称其为“剩余属性”。

```js
const { a, ...others } = { a: 1, b: 2, c: 3 };
console.log(others); // { b: 2, c: 3 }

const [first, ...others2] = [1, 2, 3];
console.log(others2); // [2, 3]
```

剩余属性必须是模式中的最后一个，并且不能有尾随逗号。

```js-nolint example-bad
const [a, ...b,] = [1, 2, 3];

// SyntaxError: rest element may not have a trailing comma
// 始终考虑将剩余运算符作为最后一个元素
```

## 示例

### 解构数组

#### 基本变量赋值

```js
const foo = ["one", "two", "three"];

const [red, yellow, green] = foo;
console.log(red); // "one"
console.log(yellow); // "two"
console.log(green); // "three"
```

#### 解构比源更多的元素

在从赋值语句右侧指定的长度为 _N_ 的数组解构的数组中，如果赋值语句左侧指定的变量数量大于 _N_，则只有前 _N_ 个变量被赋值。其余变量的值将是未定义。

```js
const foo = ["one", "two"];

const [red, yellow, green, blue] = foo;
console.log(red); // "one"
console.log(yellow); // "two"
console.log(green); // undefined
console.log(blue); //undefined
```

#### 交换变量

可以在一个解构表达式中交换两个变量的值。

没有解构的情况下，交换两个变量需要一个临时变量（或者用低级语言中的[异或交换技巧](https://en.wikipedia.org/wiki/XOR_swap_algorithm)）。

```js
let a = 1;
let b = 3;

[a, b] = [b, a];
console.log(a); // 3
console.log(b); // 1

const arr = [1, 2, 3];
[arr[2], arr[1]] = [arr[1], arr[2]];
console.log(arr); // [1, 3, 2]
```

#### 解析一个从函数返回的数组

从一个函数返回一个数组是十分常见的情况。解构使得处理返回值为数组时更加方便。

在下面例子中，要让 `f()` 返回值 `[1, 2]` 作为其输出，可以使用解构在一行内完成解析。

```js
function f() {
  return [1, 2];
}

const [a, b] = f();
console.log(a); // 1
console.log(b); // 2
```

#### 忽略某些返回值

你可以忽略你不感兴趣的返回值：

```js
function f() {
  return [1, 2, 3];
}

const [a, , b] = f();
console.log(a); // 1
console.log(b); // 3

const [c] = f();
console.log(c); // 1
```

你也可以忽略全部返回值：

```js
[, ,] = f();
```

#### 使用绑定模式作为剩余属性

数组解构的剩余属性可以是另一个数组或对象绑定模式。这允许你同时提取数组的属性和索引。

```js
const [a, b, ...{ pop, push }] = [1, 2];
console.log(a, b); // 1 2
console.log(pop, push); // [Function pop] [Function push]
```

```js
const [a, b, ...[c, d]] = [1, 2, 3, 4];
console.log(a, b, c, d); // 1 2 3 4
```

这些绑定模式甚至可以嵌套，只要每个剩余属性都在列表的最后。

```js
const [a, b, ...[c, d, ...[e, f]]] = [1, 2, 3, 4, 5, 6];
console.log(a, b, c, d, e, f); // 1 2 3 4 5 6
```

另一方面，对象解构只能有一个标识符作为剩余属性。

```js example-bad
const { a, ...{ b } } = { a: 1, b: 2 };
// SyntaxError: `...` must be followed by an identifier in declaration contexts

let a, b;
({ a, ...{ b } } = { a: 1, b: 2 });
// SyntaxError: `...` must be followed by an assignable reference in assignment contexts
```

#### 从正则表达式匹配项中提取值

当正则表达式的 [`exec()`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/RegExp/exec) 方法找到匹配项时，它将返回一个数组，该数组首先包含字符串的整个匹配部分，然后返回与正则表达式中每个括号组匹配的字符串部分。解构允许你轻易地提取出需要的部分，如果不需要，则忽略完整匹配。

```js
function parseProtocol(url) {
  const parsedURL = /^(\w+):\/\/([^/]+)\/(.*)$/.exec(url);
  if (!parsedURL) {
    return false;
  }
  console.log(parsedURL);
  // ["https://developer.mozilla.org/zh-CN/docs/Web/JavaScript",
  // "https", "developer.mozilla.org", "zh-CN/docs/Web/JavaScript"]

  const [, protocol, fullhost, fullpath] = parsedURL;
  return protocol;
}

console.log(
  parseProtocol("https://developer.mozilla.org/zh-CN/docs/Web/JavaScript"),
);
// "https"
```

#### 在任何可迭代对象上使用数组解构

数组解构调用右侧的[迭代协议](/zh-CN/docs/Web/JavaScript/Reference/Iteration_protocols)。因此，任何可迭代对象（不一定是数组）都可以解构。

```js
const [a, b] = new Map([
  [1, 2],
  [3, 4],
]);
console.log(a, b); // [1, 2] [3, 4]
```

不可迭代对象不能解构为数组。

```js example-bad
const obj = { 0: "a", 1: "b", length: 2 };
const [a, b] = obj;
// TypeError: obj is not iterable
```

只有在分配所有绑定之前，才会迭代可迭代对象。

```js
const obj = {
  *[Symbol.iterator]() {
    for (const v of [0, 1, 2, 3]) {
      console.log(v);
      yield v;
    }
  },
};
const [a, b] = obj; // Only logs 0 and 1
```

其余的绑定会提前求值并创建一个新数组，而不是使用旧的迭代器。

```js
const obj = {
  *[Symbol.iterator]() {
    for (const v of [0, 1, 2, 3]) {
      console.log(v);
      yield v;
    }
  },
};
const [a, b, ...rest] = obj; // Logs 0 1 2 3
console.log(rest); // [2, 3] (an array)
```

### 解构对象

#### 基本赋值

```js
const user = {
  id: 42,
  isVerified: true,
};

const { id, isVerified } = user;

console.log(id); // 42
console.log(isVerified); // true
```

#### 赋值给新的变量名

可以从对象中提取属性，并将其赋值给名称与对象属性不同的变量。

```js
const o = { p: 42, q: true };
const { p: foo, q: bar } = o;

console.log(foo); // 42
console.log(bar); // true
```

举个例子，`const { p: foo } = o` 从对象 `o` 中获取名为 `p` 的属性，并将其赋值给名为 `foo` 的局部变量。

#### 赋值到新的变量名并提供默认值

一个属性可以同时是两者：

- 从对象提取并分配给具有不同名称的变量。
- 指定一个默认值，以防获取的值为 `undefined`。

```js
const { a: aa = 10, b: bb = 5 } = { a: 3 };

console.log(aa); // 3
console.log(bb); // 5
```

#### 从作为函数参数传递的对象中提取属性

传递给函数参数的对象也可以提取到变量中，然后可以在函数体内访问这些变量。至于对象赋值，解构语法允许新变量具有与原始属性相同或不同的名称，并为原始对象未定义属性的情况分配默认值。

请考虑此对象，其中包含有关用户的信息。

```js
const user = {
  id: 42,
  displayName: "jdoe",
  fullName: {
    firstName: "Jane",
    lastName: "Doe",
  },
};
```

在这里，我们展示了如何将传递对象的属性提取到具有相同名称的变量。参数值 `{ id }` 表示传递给函数的对象的 `id` 属性应该被提取到一个同名变量中，然后可以在函数中使用。

```js
function userId({ id }) {
  return id;
}

console.log(userId(user)); // 42
```

你可以定义提取变量的名称。在这里，我们提取名为 `displayName` 的属性，并将其重命名为 `dname`，以便在函数体内使用。

```js
function userDisplayName({ displayName: dname }) {
  return dname;
}

console.log(userDisplayName(user)); // `jdoe`
```

嵌套对象也可以提取。下面的示例展示了属性 `fullname.firstName` 被提取到名为 `name` 的变量中。

```js
function whois({ displayName, fullName: { firstName: name } }) {
  return `${displayName} is ${name}`;
}

console.log(whois(user)); // "jdoe is Jane"
```

#### 设置函数参数的默认值

默认值可以使用 `=` 指定，如果指定的属性在传递的对象中不存在，则将其用作变量值。

下面我们展示了一个默认大小为 `big`的函数，默认坐标为 `x: 0, y: 0`，默认半径为 25。

```js
function drawChart({
  size = "big",
  coords = { x: 0, y: 0 },
  radius = 25,
} = {}) {
  console.log(size, coords, radius);
  // do some chart drawing
}

drawChart({
  coords: { x: 18, y: 30 },
  radius: 30,
});
```

在上面 `drawChart` 的函数签名中，解构的左侧具有空对象 `= {}` 的默认值。

你也可以在没有该默认值的情况下编写该函数。但是，如果你省略该默认值，该函数将在调用时寻找至少一个参数来提供，而在当前形式下，你可以在不提供任何参数的情况下调用 `drawChart()`。否则，你至少需要提供一个空对象字面量。

有关详细信息，请参阅[默认参数值 > 有默认值的解构参数](/zh-CN/docs/Web/JavaScript/Reference/Functions/Default_parameters#有默认值的解构参数)。

#### 解构嵌套对象和数组

```js
const metadata = {
  title: "Scratchpad",
  translations: [
    {
      locale: "de",
      localization_tags: [],
      last_edit: "2014-04-14T08:43:37",
      url: "/de/docs/Tools/Scratchpad",
      title: "JavaScript-Umgebung",
    },
  ],
  url: "/zh-CN/docs/Tools/Scratchpad",
};

let {
  title: englishTitle, // rename
  translations: [
    {
      title: localeTitle, // rename
    },
  ],
} = metadata;

console.log(englishTitle); // "Scratchpad"
console.log(localeTitle); // "JavaScript-Umgebung"
```

#### For of 迭代和解构

```js
const people = [
  {
    name: "Mike Smith",
    family: {
      mother: "Jane Smith",
      father: "Harry Smith",
      sister: "Samantha Smith",
    },
    age: 35,
  },
  {
    name: "Tom Jones",
    family: {
      mother: "Norah Jones",
      father: "Richard Jones",
      brother: "Howard Jones",
    },
    age: 25,
  },
];

for (const {
  name: n,
  family: { father: f },
} of people) {
  console.log(`Name: ${n}, Father: ${f}`);
}

// "Name: Mike Smith, Father: Harry Smith"
// "Name: Tom Jones, Father: Richard Jones"
```

#### 对象属性计算名和解构

计算属性名，如[对象字面量](/zh-CN/docs/Web/JavaScript/Reference/Operators/Object_initializer#计算属性名)，可以被解构。

```js
const key = "z";
const { [key]: foo } = { z: "bar" };

console.log(foo); // "bar"
```

#### 无效的 JavaScript 标识符作为属性名称

通过提供有效的替代标识符，解构可以与不是有效的 JavaScript [标识符](/zh-CN/docs/Glossary/Identifier)的属性名称一起使用。

```js
const foo = { "fizz-buzz": true };
const { "fizz-buzz": fizzBuzz } = foo;

console.log(fizzBuzz); // true
```

### 解构基本类型

对象解构几乎等同于[属性访问](/zh-CN/docs/Web/JavaScript/Reference/Operators/Property_accessors)。这意味着，如果尝试解构基本类型的值，该值将被包装到相应的包装器对象中，并且在包装器对象上访问该属性。

```js
const { a, toFixed } = 1;
console.log(a, toFixed); // undefined ƒ toFixed() { [native code] }
```

与访问属性相同，解构 `null` 或 `undefined` 会抛出 {{jsxref("TypeError")}}。

```js example-bad
const { a } = undefined; // TypeError: Cannot destructure property 'a' of 'undefined' as it is undefined.
const { a } = null; // TypeError: Cannot destructure property 'b' of 'null' as it is null.
```

即使模式为空，也会发生这种情况。

```js example-bad
const {} = null; // TypeError: Cannot destructure 'null' as it is null.
```

#### 组合数组和对象解构

数组和对象解构可以组合使用。假设你想要下面 `props` 数组中的第三个元素，然后你想要对象中的 `name` 属性，你可以执行以下操作：

```js
const props = [
  { id: 1, name: "Fizz" },
  { id: 2, name: "Buzz" },
  { id: 3, name: "FizzBuzz" },
];

const [, , { name }] = props;

console.log(name); // "FizzBuzz"
```

#### 解构对象时查找原型链

当解构一个对象时，如果属性本身没有被访问，它将沿着原型链继续查找。

```js
const obj = {
  self: "123",
  __proto__: {
    prot: "456",
  },
};
const { self, prot } = obj;

console.log(self); // "123"
console.log(prot); // "456"
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- [赋值运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators#赋值运算符)
- ["ES6 in Depth: Destructuring" on hacks.mozilla.org](https://hacks.mozilla.org/2015/05/es6-in-depth-destructuring/)

---
# Source: index.md
---
---
title: 减法赋值（-=）
slug: Web/JavaScript/Reference/Operators/Subtraction_assignment
---

**减法赋值**（**`-=`**）运算符从变量中减去右操作数的值，并将结果赋值给该变量。

{{InteractiveExample("JavaScript Demo: Expressions - Subtraction assignment operator")}}

```js interactive-example
let a = 2;

console.log((a -= 3));
// Expected output: -1

console.log((a -= "Hello"));
// Expected output: NaN
```

## 语法

```js-nolint
x -= y // x = x - y
```

## 示例

### 使用减法赋值

```js
let bar = 5;

bar -= 2; // 3
bar -= "foo"; // NaN
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- [JS 指南中的赋值运算符](/zh-CN/docs/Web/JavaScript/Guide/Expressions_and_operators#赋值运算符)
- [减法运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Subtraction)

---
# Source: index.md
---
---
title: 小于（<）
slug: Web/JavaScript/Reference/Operators/Less_than
---

**小于**（`<`）运算符在左操作数比右操作数小时返回 `true`，否则返回 `false`。

{{InteractiveExample("JavaScript Demo: Expressions - Less than operator")}}

```js interactive-example
console.log(5 < 3);
// Expected output: false

console.log(3 < 3);
// Expected output: false

// Compare bigint to number
console.log(3n < 5);
// Expected output: true

console.log("aa" < "ab");
// Expected output: true
```

## 语法

```js-nolint
x < y
```

## 描述

操作数经过多轮强制比较，可以总结为以下几点：

首先，通过依次调用其 [`[Symbol.toPrimitive]()`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Symbol/toPrimitive)（以 `"number"` 作为提示）、[`valueOf()`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Object/valueOf) 和 [`toString()`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Object/toString) 方法，将对象[转换为原始类型](/zh-CN/docs/Web/JavaScript/Guide/Data_structures#强制原始值转换)。左边的操作数总是在右边的操作数之前被强制转换。请注意，尽管 `[Symbol.toPrimitive]()` 被调用时带有 `"number"` 的提示（意味着有一点倾向于将对象变成数字），但返回值并没有[转换为数字](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Number#number_强制转换)，因为字符串仍然被特别处理。

- 如果两个值都是字符串，则根据它们所包含的 Unicode 码位的值，将它们作为字符串进行比较。
- 否则，JavaScript 会尝试将非数值类型转化为数值类型：
  - 布尔值 `true` 和 `false` 分别转化为 1 和 0。
  - `null` 转化为 0。
  - `undefined` 转化为 `NaN`。
  - 字符串根据其包含的值进行转换，如果不包含数字值，则转换为 `NaN`。
- 如果任意一个值为 [`NaN`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/NaN)，则运算符返回 `false`。
- 否则，这些值将作为数值进行比较。BigInt 和数值可以一起比较。

其他运算符，包括 [`>`](/zh-CN/docs/Web/JavaScript/Reference/Operators/Greater_than)、[`>=`](/zh-CN/docs/Web/JavaScript/Reference/Operators/Greater_than_or_equal) 和 [`<=`](/zh-CN/docs/Web/JavaScript/Reference/Operators/Less_than_or_equal) 使用与 `<` 相同的算法。有两种情况，所有四个运算符都返回 `false`：

- 如果其中一个操作数被转换为 BigInt，而另一个被转换为无法转换为 BigInt 值的字符串（当传递给 [`BigInt()`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/BigInt)时，它会抛出[语法错误](/zh-CN/docs/Web/JavaScript/Reference/Errors/Invalid_BigInt_syntax)）。
- 如果其中一个操作数被转化为 `NaN`，如不能转化为数字的字符串，或 `undefined`。

对于所有其他情况，这四种运算符有以下关系：

```js
x < y === !(x >= y);
x <= y === !(x > y);
x > y === y < x;
x >= y === y <= x;
```

> [!NOTE]
> `<` 和 `>` 之间一个明显区别是强制的顺序，特别是当强制转化为原始值有副作用时。所有的比较操作符都是先强制转化左操作数再强制转化右操作数。

## 示例

### 字符串之间的比较

```js
"a" < "b"; // true
"a" < "a"; // false
"a" < "3"; // false
```

### 字符串与数值比较

```js
"5" < 3; // false
"3" < 3; // false
"3" < 5; // true

"hello" < 5; // false
5 < "hello"; // false

"5" < 3n; // false
"3" < 5n; // true
```

### 数值之间的比较

```js
5 < 3; // false
3 < 3; // false
3 < 5; // true
```

### 数值与 BigInt 之间的比较

```js
5n < 3; // false
3 < 5n; // true
```

### 比较布尔值、null、undefined 和 NaN

```js
true < false; // false
false < true; // true

0 < true; // true
true < 1; // false

null < 0; // false
null < 1; // true

undefined < 3; // false
3 < undefined; // false

3 < NaN; // false
NaN < 3; // false
```

### 含有副作用的比较

比较总是将其操作数强制转化为原始值。这意味着同一个对象在一个比较表达式中可能最终会有不同的值。例如，你可能有两个既大于又小于对方的值。

```js
class Mystery {
  static #coercionCount = -1;
  valueOf() {
    Mystery.#coercionCount++;
    // 左侧操作数先强制转化，所以对右操作数会先返回 0 再返回 1
    return Mystery.#coercionCount % 2;
  }
}
const l = new Mystery();
const r = new Mystery();
console.log(l < r && r < l);
// true
```

> [!WARNING]
> 这可能是混乱的根源。如果你的对象提供了自定义的原始值转换逻辑，请确保它是*幂等的*：多次强制转化应该返回相同的值。

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- [大于运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Greater_than)
- [大于等于运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Greater_than_or_equal)
- [小于等于运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Less_than_or_equal)

---
# Source: index.md
---
---
title: await
slug: Web/JavaScript/Reference/Operators/await
---

`await` 操作符用于等待一个 {{jsxref("Promise")}} 兑现并获取它兑现之后的值。它只能在{{jsxref("Statements/async_function", "异步函数", "", 1)}}或者[模块](/zh-CN/docs/Web/JavaScript/Guide/Modules)顶层中使用。

## 语法

```js-nolint
await expression;
```

### 参数

- `expression`
  - : 要等待的 {{jsxref("Promise")}} 实例，Thenable 对象，或任意类型的值。

### 返回值

返回从 `Promise` 实例或 thenable 对象取得的处理结果。如果等待的值不符合 thenable，则返回表达式本身的值。

### 异常

拒绝（reject）的原因会被作为异常抛出。

## 描述

`await` 通常用于拆开 promise 的包装，使用方法是传递一个 {{jsxref("Promise")}} 作为 `expression`。使用 `await` 总会暂停当前异步函数的执行，在该 `Promise` 敲定（settled，指兑现或拒绝）后继续执行。函数的执行恢复（resume）时，`await` 表达式的值已经变成了 `Promise` 兑现的值。

若该 `Promise` 被拒绝（rejected），`await` 表达式会把拒绝的原因（reason）抛出。当前函数（`await` 所在的函数）会出现在抛出的错误的[栈追踪](#改善栈追溯)（stack trace），否则当前函数就不会在栈追踪出现。

`await` 总会同步地对表达式求值并处理，处理的行为与 {{jsxref("Promise.resolve()")}} 一致，不属于原生 `Promise` 的值全都会被隐式地转换为 `Promise` 实例后等待。处理的规则为，若表达式：

- 是一个原生 `Promise`（原生{{jsxref("Promise")}} 的实例或其派生类的实例，且满足 `expression.constructor === Promise`），会被直接用于等待，等待由原生代码实现，该对象的 `then()` 不会被调用。
- 是 thenable 对象（包括非原生的 `Promise` 实例、polyfill、Proxy、派生类等），会构造一个新 `Promise` 用于等待，构造时会调用该对象的 `then()` 方法。
- 不是 thenable 对象，会被包装进一个已兑现的 `Promise` 用于等待，其结果就是表达式的值。

## 示例

### 等待 Promise 的兑现

当一个 `Promise` 被传递给 `await` 操作符，`await` 将等待该 `Promise` 兑现，并在兑现后返回该 `Promise` 兑现的值。

```js
function resolveAfter2Seconds(x) {
  return new Promise((resolve) => {
    setTimeout(() => {
      resolve(x);
    }, 2000);
  });
}

async function f1() {
  let x = await resolveAfter2Seconds(10);
  console.log(x); // 10
}

f1();
```

### 转换为 promise

若表达式的值不是 `Promise`，`await` 会把该值转换为已兑现的 `Promise`，然后返回其结果。

```js
async function f3() {
  const y = await 20;
  console.log(y); // 20

  const obj = {};
  console.log((await obj) === obj); // true
}

f3();
```

### promise 被拒绝

如果 `Promise` 被拒绝，则抛出拒绝的原因。

```js
async function f4() {
  try {
    const z = await Promise.reject(30);
  } catch (e) {
    console.error(e); // 30
  }
}

f4();
```

### 处理被拒绝的 promise

你可以链式调用 [`catch()`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Promise/catch)（而不是使用 `try`）以在等待 promise 兑现之前处理被拒绝的 promise。

```js
const response = await promisedFunction().catch((err) => {
  console.error(err);
  return "default response";
});
// response will be "default response" if the promise is rejected
```

### 在顶层使用 await

在[模块](/zh-CN/docs/Web/JavaScript/Guide/Modules)的顶层，你可以单独使用关键字 `await`（异步函数的外面）。也就是说一个模块如果包含用了 `await` 的子模块，该模块就会等待该子模块，这一过程并不会阻塞其他子模块。

下面是一个在 [`export`](/zh-CN/docs/Web/JavaScript/Reference/Statements/export) 表达式中使用了 [Fetch API](/zh-CN/docs/Web/API/Fetch_API) 的例子。任何文件只要导入这个模块，后面的代码就会等待，直到 fetch 完成。

```js
// fetch request
const colors = fetch("../data/colors.json").then((response) => response.json());

export default await colors;
```

### await 对执行过程的影响

当函数执行到 `await` 时，被等待的表达式会立即执行，所有依赖该表达式的值的代码会被暂停，并推送进[微任务队列（microtask queue）](/zh-CN/docs/Web/JavaScript/Reference/Execution_model)。然后主线程被释放出来，用于事件循环中的下一个任务。即使等待的值是已经敲定的 promise 或不是 promise，也会发生这种情况。例如，考虑以下代码：

```js
async function foo(name) {
  console.log(name, "start");
  console.log(name, "middle");
  console.log(name, "end");
}

foo("First");
foo("Second");

// First start
// First middle
// First end
// Second start
// Second middle
// Second end
```

对应到 `Promise` 的写法是：

```js
function foo(name) {
  return new Promise((resolve) => {
    console.log(name, "start");
    console.log(name, "middle");
    console.log(name, "end");
    resolve();
  });
}
```

执行到 `await` 时，后面的代码就会整体被安排进一个新的微任务，此后的函数体变为异步执行。

```js
async function foo(name) {
  console.log(name, "start");
  await console.log(name, "middle");
  console.log(name, "end");
}

foo("First");
foo("Second");

// First start
// First middle
// Second start
// Second middle
// First end
// Second end
```

对应的 `Promise` 写法是：

```js
function foo(name) {
  return new Promise((resolve) => {
    console.log(name, "start");
    resolve(console.log(name, "middle"));
  }).then(() => {
    console.log(name, "end");
  });
}
```

虽然这里的 `then()` 看起来很多余，其中的代码完全可以被合并到构造器的回调里，但不管该 `Promise` 的状态如何，`then()` 的回调**总会被异步执行**，`await` 的行为也一样。因此，只要情况不是必须或可能需要等待 `Promise` 的结果，就应该避免使用 `await`。

其他微任务能在函数执行恢复之前执行：

```js
let i = 0;

queueMicrotask(function test() {
  i++;
  console.log("microtask", i);
  if (i < 3) {
    queueMicrotask(test);
  }
});

(async () => {
  console.log("async function start");
  for (let i = 1; i < 3; i++) {
    await null;
    console.log("async function resume", i);
  }
  await null;
  console.log("async function end");
})();

queueMicrotask(() => {
  console.log("queueMicrotask() after calling async function");
});

console.log("script sync part end");

// Logs:
// async function start
// script sync part end
// microtask 1
// async function resume 1
// queueMicrotask() after calling async function
// microtask 2
// async function resume 2
// microtask 3
// async function end
```

此案例中，`test()` 总会在异步函数恢复执行前被调用，呈现轮流的调度。微任务被执行的顺序通常就是入队的先后顺序，而 `console.log("queueMicrotask() after calling async function");` 比 `await` 晚入队，因此 `"queueMicrotask() after calling async function"` 在异步函数第一次恢复之后才输出。

### 改善栈追踪

有时，当异步函数直接返回一个 `Promise` 时我们会省略 `await`。

```js
async function noAwait() {
  // Some actions...

  return /* await */ lastAsyncTask();
}
```

但是假如这个 `Promise` 的由来是调用了异步函数，且该异步函数的异步部分抛出了错误：

```js
async function lastAsyncTask() {
  await null;
  throw new Error("failed");
}

async function noAwait() {
  return lastAsyncTask();
}

noAwait();

// Error: failed
//    at lastAsyncTask
```

栈追踪中只出现了 `lastAsyncTask`，这是因为抛出错误时 `noAwait` 已经返回——某种意义上该 `Promise` 已经与 `noAwait` 无关。若要改善栈追踪，你可以用 `await` 提前等待，错误就会在函数体结束前抛出，接着该错误会被包装进一个新的 `Promise`，因错误被 `await` 在主调函数的函数体抛出，主调函数将会出现在栈追踪。

```js
async function lastAsyncTask() {
  await null;
  throw new Error("failed");
}

async function withAwait() {
  return await lastAsyncTask();
}

withAwait();

// Error: failed
//    at lastAsyncTask
//    at async withAwait
```

但是，这样会有一点性能牺牲，毕竟 `Promise` 会被拆装了又再次包装。

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- {{jsxref("Statements/async_function", "async 函数")}}
- {{jsxref("Operators/async_function", "async 函数表达式")}}
- {{jsxref("AsyncFunction")}} 对象
- v8.dev 上的 [Top level await](https://v8.dev/features/top-level-await)

---
# Source: index.md
---
---
title: 减法（-）
slug: Web/JavaScript/Reference/Operators/Subtraction
---

**减法**（**`-`**）运算符将两个操作数相减，并产生两者之差。

{{InteractiveExample("JavaScript Demo: Expressions - Subtraction operator")}}

```js interactive-example
console.log(5 - 3);
// Expected output: 2

console.log(3.5 - 5);
// Expected output: -1.5

console.log(5 - "hello");
// Expected output: NaN

console.log(5 - true);
// Expected output: 4
```

## 语法

```js-nolint
x - y
```

## 描述

减法运算符[将两个操作数转换为数值](/zh-CN/docs/Web/JavaScript/Guide/Data_structures#强制数字类型转换)，并根据两个操作数的类型执行数字减法或 [BigInt](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/BigInt) 减法。如果类型不匹配，则抛出 {{jsxref("TypeError")}}。

## 示例

### 数值减法

```js
// Number - Number -> subtraction
5 - 3; // 2

// Number - Number -> subtraction
3 - 5; // -2
```

### 非数值减法

```js
// String - Number -> subtraction
"foo" - 3; // NaN; "foo" is converted to the number NaN

// Number - String -> subtraction
5 - "3"; // 2; "3" is converted to the number 3
```

### BigInt 减法

```js
// BigInt - BigInt -> subtraction
2n - 1n; // 1n
```

你不能在减法中混合使用 BigInt 和数字操作数。

```js example-bad
2n - 1; // TypeError: Cannot mix BigInt and other types, use explicit conversions
2 - 1n; // TypeError: Cannot mix BigInt and other types, use explicit conversions
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- [加法运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Addition)
- [除法运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Division)
- [乘法运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Multiplication)
- [取余运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Remainder)
- [幂运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Exponentiation)
- [自增运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Increment)
- [自减运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Decrement)
- [一元减运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Unary_negation)
- [一元加运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Unary_plus)

---
# Source: index.md
---
---
title: this
slug: Web/JavaScript/Reference/Operators/this
---

与其他语言相比，**函数的 `this` 关键字**在 JavaScript 中的表现略有不同，此外，在[严格模式](/zh-CN/docs/Web/JavaScript/Reference/Strict_mode)和非严格模式之间也会有一些差别。

在绝大多数情况下，函数的调用方式决定了 `this` 的值（运行时绑定）。`this` 不能在执行期间被赋值，并且在每次函数被调用时 `this` 的值也可能会不同。ES5 引入了 [bind](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Function/bind) 方法来设置函数的 `this` 值，而不用考虑函数如何被调用的。ES2015 引入了[箭头函数](/zh-CN/docs/Web/JavaScript/Reference/Functions/Arrow_functions)，箭头函数不提供自身的 this 绑定（`this` 的值将保持为闭合词法上下文的值）。

{{InteractiveExample("JavaScript Demo: Expressions - this")}}

```js interactive-example
const test = {
  prop: 42,
  func: function () {
    return this.prop;
  },
};

console.log(test.func());
// Expected output: 42
```

## 语法

```plain
this
```

### 值

在非严格模式下，`this` 总是指向一个对象，在严格模式下可以是任意值。有关如何确定该值的更多信息，请参阅下面的描述。

## 描述

`this` 的值取决于它出现的上下文：函数、类或全局。

### 函数上下文

在函数内部，`this` 的值取决于函数如何被调用。可以将 `this` 看作是函数的一个隐藏参数（就像函数定义中声明的参数一样），`this` 是语言在函数体被执行时为你创建的绑定。

对于典型的函数，`this` 的值是函数被访问的对象。换句话说，如果函数调用的形式是 `obj.f()`，那么 `this` 就指向 `obj`。例如：

```js
function getThis() {
  return this;
}

const obj1 = { name: "obj1" };
const obj2 = { name: "obj2" };

obj1.getThis = getThis;
obj2.getThis = getThis;

console.log(obj1.getThis()); // { name: 'obj1', getThis: [Function: getThis] }
console.log(obj2.getThis()); // { name: 'obj2', getThis: [Function: getThis] }
```

注意，虽然函数是相同的，但是根据其调用的方式，`this` 的值是不同的。这与函数参数的工作方式类似。

`this` 的值不是拥有此函数作为自己属性的对象，而是用于调用此函数的对象。你可以通过调用对象在[原型链](/zh-CN/docs/Web/JavaScript/Guide/Inheritance_and_the_prototype_chain)中的方法来证明这一点。

```js
const obj3 = {
  __proto__: obj1,
  name: "obj3",
};

console.log(obj3.getThis()); // { name: 'obj3' }
```

`this` 的值总是根据调用函数的方式而改变，即使函数是在创建对象时定义的：

```js
const obj4 = {
  name: "obj4",
  getThis() {
    return this;
  },
};

const obj5 = { name: "obj5" };

obj5.getThis = obj4.getThis;
console.log(obj5.getThis()); // { name: 'obj5', getThis: [Function: getThis] }
```

如果方法被访问的值是一个原始值，`this` 也将是一个原始值——但只有当函数处于严格模式下会如此。

```js
function getThisStrict() {
  "use strict"; // 进入严格模式
  return this;
}

// 仅用于演示——你不应该改变内置的原型对象
Number.prototype.getThisStrict = getThisStrict;
console.log(typeof (1).getThisStrict()); // "number"
```

如果函数在没有被任何东西访问的情况下被调用，`this` 将是 `undefined`——但只有在函数处于严格模式下会如此。

```js
console.log(typeof getThisStrict()); // "undefined"
```

在非严格模式下，一个特殊的过程称为 [`this` 替换](/zh-CN/docs/Web/JavaScript/Reference/Strict_mode#非_this_替换)确保 `this` 的值总是一个对象。这意味着：

- 如果一个函数被调用时 `this` 被设置为 `undefined` 或 `null`，`this` 会被替换为 {{jsxref("globalThis")}}。
- 如果函数被调用时 `this `被设置为一个原始值，`this` 会被替换为原始值的包装对象。

```js
function getThis() {
  return this;
}

// 仅用于演示——你不应该修改内置的原型对象
Number.prototype.getThis = getThis;
console.log(typeof (1).getThis()); // "object"
console.log(getThis() === globalThis); // true
```

在典型的函数调用中，`this` 是通过函数的前缀（点之前的部分）隐式传递的，就像一个参数。你也可以使用 {{jsxref("Function.prototype.call()")}}、{{jsxref("Function.prototype.apply()")}} 或 {{jsxref("Reflect.apply()")}} 方法显式设置 `this` 的值。使用 {{jsxref("Function.prototype.bind()")}}，你可以创建一个新的函数，无论函数如何被调用，其 `this` 的值都不会改变。当使用这些方法时，如果函数是在非严格模式下，上述 `this` 替换规则仍然适用。

#### 回调

当一个函数作为回调函数传递时，`this` 的值取决于如何调用回调，这由 API 的实现者决定。回调函数通常以 `undefined` 作为 `this` 的值被调用（直接调用，而不附加到任何对象上），这意味着如果函数是在非严格模式，`this` 的值会是全局对象（{{jsxref("globalThis")}}）。这在[迭代数组方法](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Array#迭代方法)、[`Promise()`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Promise/Promise) 构造函数等例子中都是适用的。

```js
function logThis() {
  "use strict";
  console.log(this);
}

[1, 2, 3].forEach(logThis); // undefined、undefined、undefined
```

一些 API 允许你为回调函数的调用设置一个 `this` 值。例如，所有的迭代数组方法和相关的方法，如{{jsxref("Set.prototype.forEach()")}}，都接受一个可选的 `thisArg` 参数。

```js
[1, 2, 3].forEach(logThis, { name: "obj" });
// { name: 'obj' }, { name: 'obj' }, { name: 'obj' }
```

偶尔，回调函数会以一个非 `undefined` 的 `this` 值被调用。例如，{{jsxref("JSON.parse()")}} 的 `reviver` 参数和 {{jsxref("JSON.stringify()")}} 的 `replacer` 参数都会把 `this` 设置为正在被解析/序列化的属性所属的对象。

#### 箭头函数

在[箭头函数](/zh-CN/docs/Web/JavaScript/Reference/Functions/Arrow_functions)中，`this` 保留了闭合词法上下文的 `this` 值。换句话说，当对箭头函数求值时，语言不会创建一个新的 `this` 绑定。

例如，在全局代码中，无论是否在严格模式下，由于[全局上下文](#全局上下文)绑定，`this` 值总是 `globalThis`。

```js
const globalObject = this;
const foo = () => this;
console.log(foo() === globalObject); // true
```

箭头函数在其周围的作用域上创建一个 `this` 值的[闭包](/zh-CN/docs/Web/JavaScript/Guide/Closures)，这意味着箭头函数的行为就像它们是“自动绑定”的——无论如何调用，`this` 都绑定到函数创建时的值（在上面的例子中，是全局对象）。在其他函数内部创建的箭头函数也是如此：它们的 `this` 值保持为闭合词法上下文的 `this`。[参见下面的例子](#箭头函数中的_this)。

此外，当使用 `call()`、`bind()` 或 `apply()` 调用箭头函数时，`thisArg` 参数会被忽略。不过，你仍然可以使用这些方法传递其他参数。

```js
const obj = { name: "obj" };

// 尝试使用 call 设置 this
console.log(foo.call(obj) === globalObject); // true

// 尝试使用 bind 设置 this
const boundFoo = foo.bind(obj);
console.log(boundFoo() === globalObject); // true
```

#### 构造函数

当一个函数被用作构造函数（使用 {{jsxref("Operators/new", "new")}} 关键字）时，无论构造函数是在哪个对象上被访问的，其 `this` 都会被绑定到正在构造的新对象上。除非构造函数返回另一个非原始值，不然 `this` 的值会成为 `new` 表达式的值。

```js
function C() {
  this.a = 37;
}

let o = new C();
console.log(o.a); // 37

function C2() {
  this.a = 37;
  return { a: 38 };
}

o = new C2();
console.log(o.a); // 38
```

在第二个例子（`C2`）中，因为在构造过程中返回了一个对象，`this` 被绑定的新对象被丢弃。（这基本上使得语句 `this.a = 37;` 成为了死代码。它并不完全是死代码，因为它被执行了，但是它可以被消除而不产生任何外部效果。）

#### super

当一个函数以 `super.method()` 的形式被调用时，`method` 函数内的 `this` 与 `super.method()` 调用周围的 `this` 值相同，通常不等于 `super` 所指向的对象。这是因为 `super.method` 不是像上面的对象成员访问——它是一种特殊的语法，有不同的绑定规则。有关示例，请参见 [`super` 参考](/zh-CN/docs/Web/JavaScript/Reference/Operators/super#通过_super_调用方法)。

### 类上下文

一个[类](/zh-CN/docs/Web/JavaScript/Reference/Classes)可以被分为两个上下文：静态和实例。[构造函数](/zh-CN/docs/Web/JavaScript/Reference/Classes/constructor)、方法和实例字段初始化器（[公有](/zh-CN/docs/Web/JavaScript/Reference/Classes/Public_class_fields)或[私有](/zh-CN/docs/Web/JavaScript/Reference/Classes/Private_elements)）属于实例上下文。[静态](/zh-CN/docs/Web/JavaScript/Reference/Classes/static)方法、静态字段初始化器和[静态初始化块](/zh-CN/docs/Web/JavaScript/Reference/Classes/Static_initialization_blocks)属于静态上下文。`this` 值在每个上下文中都是不同的。

类构造函数总是通过 `new` 调用，所以它们的行为与[构造函数](#构造函数)相同：`this` 值是正在创建的新实例。类方法的行为像对象字面量中的方法——`this` 值是方法被访问的对象。如果方法没有转移到另一个对象，`this` 通常是类的一个实例。

静态方法不是 `this` 的属性。它们是类本身的属性。因此，它们通常在类上访问，`this` 是类（或子类）的值。静态初始化块也是在 `this` 设置为当前类的情况下进行求值的。

字段初始化器也在类的上下文中执行。实例字段是在 `this` 被设置为正在构造的实例的情况下被初始化的。静态字段是在 `this` 被设置为当前类的情况下被初始化的。这就是为什么字段初始化器中的箭头函数[对于实例字段绑定到实例，对于静态字段绑定到类](/zh-CN/docs/Web/JavaScript/Reference/Functions/Arrow_functions#不能用作方法)。

```js
class C {
  instanceField = this;
  static staticField = this;
}

const c = new C();
console.log(c.instanceField === c); // true
console.log(C.staticField === C); // true
```

#### 派生类构造函数

与基类构造函数不同，派生构造函数没有初始的 `this` 绑定。调用 {{jsxref("Operators/super", "super()")}} 在构造函数中创建一个 `this` 绑定，基本上和求值以下代码的效果类似，其中 `Base` 是基类：

```js-nolint
this = new Base();
```

> [!WARNING]
> 在调用 `super()` 之前引用 `this` 将抛出错误。

派生类在调用 `super()` 之前不能有返回，除非构造函数返回一个对象（这样 `this` 值就会被覆盖）或者类根本没有构造函数。

```js
class Base {}
class Good extends Base {}
class AlsoGood extends Base {
  constructor() {
    return { a: 5 };
  }
}
class Bad extends Base {
  constructor() {}
}

new Good();
new AlsoGood();
new Bad(); // ReferenceError: Must call super constructor in derived class before accessing 'this' or returning from derived constructor
```

### 全局上下文

在全局执行上下文中（在任何函数或类之外；可能在全局范围内定义的[块](/zh-CN/docs/Web/JavaScript/Reference/Statements/block)或[箭头函数](#箭头函数)内部），`this` 值取决于脚本运行的执行上下文。像[回调](#回调)一样，`this` 值由运行时环境（调用者）确定。

在脚本的顶层，无论是否在严格模式下，`this` 会指向{{jsxref("globalThis")}}。这通常与全局对象相同——例如，如果源代码放在 HTML 的 [`<script>`](/zh-CN/docs/Web/HTML/Reference/Elements/script) 元素内并作为脚本执行，`this === window`。

> [!NOTE]
> `globalThis` 通常与全局对象的概念相同（即向 `globalThis` 添加属性会使它们成为全局变量）——这对于浏览器和 Node 是这样的——但主机可以为 `globalThis` 提供与全局对象无关的不同值。

```js
// 在网页浏览器中，window 对象也是全局对象：
console.log(this === window); // true

this.b = "MDN";
console.log(window.b); // "MDN"
console.log(b); // "MDN"
```

如果源代码作为[模块](/zh-CN/docs/Web/JavaScript/Guide/Modules)加载（对于 HTML，这意味着在 `<script>` 标签中添加 `type="module"`），在顶层，`this` 总是 `undefined`。

如果源代码使用 [`eval()`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/eval) 执行，`this` 与[直接调用 eval](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/eval#直接和间接调用_eval) 的闭合上下文相同，或者与间接调用 eval 的 `globalThis`（就像它在单独的全局脚本中运行一样）相同。

```js
function test() {
  // 直接调用 eval
  console.log(eval("this") === this);
  // 间接调用 eval，非严格模式
  console.log(eval?.("this") === globalThis);
  // 间接调用 eval，严格模式
  console.log(eval?.("'use strict'; this") === globalThis);
}

test.call({ name: "obj" }); // 输出 3 个 "true"
```

请注意，某些源代码虽然看起来像全局作用域，但在执行时实际上被包装在一个函数中。例如，Node.js CommonJS 模块被包装在一个函数中，并且 `this` 值设置为 `module.exports`。[事件处理器属性](#内联事件处理器中的_this)执行时，`this` 设置为它们附加到的元素。

对象字面量不创建 `this` 作用域——只有在对象内定义的函数（方法）才会这样做。在对象字面量中使用 `this` 会从周围的作用域继承值。

```js
const obj = {
  a: this,
};

console.log(obj.a === window); // true
```

## 示例

### 函数上下文中的 this

`this` 参数的值取决于函数如何被调用，而不是它如何被定义。

```js
// 对象可以作为第一个参数传递给 'call' 或 'apply'，
// 并且 'this' 将被绑定到它。
const obj = { a: "Custom" };

// 使用 var 声明的变量成为 'globalThis' 的属性。
var a = "Global";

function whatsThis() {
  return this.a; // 'this' 取决于函数如何被调用
}

whatsThis(); // 'Global'; 在非严格模式下，'this' 参数默认为 'globalThis'
obj.whatsThis = whatsThis;
obj.whatsThis(); // 'Custom'; 'this' 参数被绑定到 obj
```

使用 `call()` 和 `apply()`，你可以对 `this` 进行传值，就像它是一个显式参数。

```js
function add(c, d) {
  return this.a + this.b + c + d;
}

const o = { a: 1, b: 3 };

// 第一个参数被绑定到隐式的 'this' 参数；
// 剩余的参数被绑定到命名参数。
add.call(o, 5, 7); // 16

// 第一个参数被绑定到隐式的 'this' 参数；
// 第二个参数是一个数组，其成员被绑定到命名参数。
add.apply(o, [10, 20]); // 34
```

### this 和对象转换

在非严格模式下，如果一个函数被调用时其 `this` 值不是一个对象，那么 `this` 值会被替换为一个对象。`null` 和 `undefined` 会变成 `globalThis`。像 `7` 或 `'foo'` 这样的原始值会使用相关的构造函数转换为对象，所以原始数值 `7` 会被转换为一个 {{jsxref("Number")}} 包装类，字符串 `'foo'` 会被转换为一个 {{jsxref("String")}} 包装类。

```js
function bar() {
  console.log(Object.prototype.toString.call(this));
}

bar.call(7); // [object Number]
bar.call("foo"); // [object String]
bar.call(undefined); // [object Window]
```

### bind() 方法

调用 [`f.bind(someObject)`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Function/bind) 会创建一个新函数，这个新函数具有与 `f` 相同的函数体和作用域，但 `this` 的值永久绑定到 `bind` 的第一个参数，无论函数如何被调用。

```js
function f() {
  return this.a;
}

const g = f.bind({ a: "azerty" });
console.log(g()); // azerty

const h = g.bind({ a: "yoo" }); // bind 只能生效一次！
console.log(h()); // azerty

const o = { a: 37, f, g, h };
console.log(o.a, o.f(), o.g(), o.h()); // 37 37 azerty azerty
```

### 箭头函数中的 this

箭头函数在闭合执行上下文中创建了 `this` 值的闭包。在下面的例子中，我们创建了一个对象 `obj`，它有一个方法 `getThisGetter`，该方法返回一个函数，这个函数返回 `this` 的值。返回的函数是作为箭头函数的形式创建的，所以它的 `this` 永久地绑定到其执行上下文中的 `this`。`getThisGetter` 内部的 `this` 值可以在调用中设置，这反过来又设置了返回函数的返回值。我们假设 `getThisGetter` 是一个非严格函数，这意味着它包含在一个非严格模式的脚本中，并且没有进一步嵌套在类或严格模式的函数中。

```js
const obj = {
  getThisGetter() {
    const getter = () => this;
    return getter;
  },
};
```

我们可以作为 `obj` 的方法调用 `getThisGetter`，这将在其主体内部将 `this` 绑定到 `obj`。返回的函数被赋值给一个变量 `fn`。现在，当调用 `fn` 时，返回的 `this` 值仍然是通过调用 `getThisGetter` 设置的值，即 `obj`。如果返回的函数不是箭头函数，那么这样的调用会导致 `this` 值为 `globalThis`，因为 `getThisGetter` 是非严格模式的。

```js
const fn = obj.getThisGetter();
console.log(fn() === obj); // true
```

但是，如果你解绑 `obj` 的方法而不调用它，需要小心，因为 `getThisGetter` 仍然是一个方法，它有一个可变的 `this` 值。在下面的例子中，调用 `fn2()()` 将返回 `globalThis`，因为它遵循 `fn2()` 的 `this`，由于它没有附加到任何对象上进行调用，所以是 `globalThis`。

```js
const fn2 = obj.getThisGetter;
console.log(fn2()() === globalThis); // 在非严格模式下为 true
```

这种行为在定义回调时非常有用。通常，每个函数表达式都创建自己的 `this` 绑定，这会遮蔽上层作用域的 `this` 值。现在，如果你不关心 `this` 值，你可以将函数定义为箭头函数，并且只在你需要的地方创建 `this` 绑定（例如，在类方法中）。参见 [`setTimeout()` 的示例](/zh-CN/docs/Web/JavaScript/Reference/Functions/Arrow_functions#使用_call、bind_和_apply)。

### getter 或 setter 中的 this

在 getter 和 setter 中，`this` 是基于访问属性的对象，而不是定义属性的对象。用作 getter 或 setter 的函数会将其 `this` 绑定到正在设置或获取属性的对象。

```js
function sum() {
  return this.a + this.b + this.c;
}

const o = {
  a: 1,
  b: 2,
  c: 3,
  get average() {
    return (this.a + this.b + this.c) / 3;
  },
};

Object.defineProperty(o, "sum", {
  get: sum,
  enumerable: true,
  configurable: true,
});

console.log(o.average, o.sum); // 2 6
```

### DOM 事件处理器中的 this

当一个函数被用作事件处理器时，它的 `this` 参数绑定到放置监听器的 DOM 元素上（一些浏览器对于使用 {{domxref("EventTarget/addEventListener", "addEventListener()")}} 以外的方法动态添加的监听器并不遵循这个约定）。

```js
// 当作为监听器调用时，将相关元素变为蓝色
function bluify(e) {
  // 总是为 true
  console.log(this === e.currentTarget);
  // 当 currentTarget 和 target 是同一个对象时为 true
  console.log(this === e.target);
  this.style.backgroundColor = "#A5D9F3";
}

// 获取文档中的每一个元素
const elements = document.getElementsByTagName("*");

// 添加 bluify 作为点击监听器，所以当元素被点击时，它会变蓝
for (const element of elements) {
  element.addEventListener("click", bluify, false);
}
```

### 内联事件处理器中的 this

当代码从内联[事件处理器属性](/zh-CN/docs/Web/HTML/Reference/Attributes#event_handler_attributes)调用时，它的 `this` 绑定到放置监听器的 DOM 元素上：

```html
<button onclick="alert(this.tagName.toLowerCase());">Show this</button>
```

上面的 alert 会显示 `button`。注意只有外层代码中的 `this` 是这样设置的：

```html
<button onclick="alert((function(){return this})());">Show inner this</button>
```

在这种情况下，内部函数的 `this` 指向 `globalThis` 对象（即非严格模式下，调用的函数未设置 `this` 时指向的默认对象）。

### 类中的绑定方法

和其他普通函数一样，方法中的 `this` 值取决于它们如何被调用。有时，改写这个行为，让类中的 `this` 值总是指向这个类实例会很有用。为了做到这一点，可在构造函数中绑定类方法：

```js
class Car {
  constructor() {
    // 绑定 sayBye 而不是 sayHi 来展示差异
    this.sayBye = this.sayBye.bind(this);
  }
  sayHi() {
    console.log(`Hello from ${this.name}`);
  }
  sayBye() {
    console.log(`Bye from ${this.name}`);
  }
  get name() {
    return "Ferrari";
  }
}

class Bird {
  get name() {
    return "Tweety";
  }
}

const car = new Car();
const bird = new Bird();

// 方法中 'this' 的值取决于它们的调用者
car.sayHi(); // Hello from Ferrari
bird.sayHi = car.sayHi;
bird.sayHi(); // Hello from Tweety

// 对于绑定方法，'this' 不依赖于调用者
bird.sayBye = car.sayBye;
bird.sayBye(); // Bye from Ferrari
```

> [!NOTE]
> 类总是在严格模式下。如果一个方法试图访问 `this` 上的属性，使用未定义的 `this` 值调用该方法将会抛出错误。
>
> ```js example-bad
> const carSayHi = car.sayHi;
> carSayHi(); // TypeError because the 'sayHi' method tries to access 'this.name', but 'this' is undefined in strict mode.
> ```

然而，请注意，自动绑定的方法遭受的问题与[使用箭头函数作为类属性](/zh-CN/docs/Web/JavaScript/Reference/Functions/Arrow_functions#不能用作方法)相同：类的每个实例都会有其方法的自己的副本，这会增加内存使用。只在绝对必要的地方使用它。你也可以模仿 [`Intl.NumberFormat.prototype.format()`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Intl/DateTimeFormat/format#将_format_与_map_一起使用) 的实现：定义属性作为一个 getter，当访问时返回一个绑定函数并保存它，这样函数只创建一次，并且只会在必要时创建。

### with 语句中的 this

尽管 [`with`](/zh-CN/docs/Web/JavaScript/Reference/Statements/with) 语句已被弃用，并且在严格模式下不可用，但它们仍然是正常 `this` 绑定规则的一个例外。如果在 `with` 语句中调用了一个函数，并且该函数是作用域对象的属性，那么 `this` 值会绑定到作用域对象，就好像存在 `obj1.` 前缀一样。

```js
const obj1 = {
  foo() {
    return this;
  },
};

with (obj1) {
  console.log(foo() === obj1); // true
}
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- [严格模式](/zh-CN/docs/Web/JavaScript/Reference/Strict_mode)
- {{jsxref("globalThis")}}

---
# Source: index.md
---
---
title: new
slug: Web/JavaScript/Reference/Operators/new
l10n:
  sourceCommit: c6f0f106b9083984dbf597678def6561729bb459
---

**`new`** 运算符允许开发人员创建一个用户定义的对象类型的实例或具有构造函数的内置对象的实例。

{{InteractiveExample("JavaScript Demo: Expressions - new operator")}}

```js interactive-example
function Car(make, model, year) {
  this.make = make;
  this.model = model;
  this.year = year;
}

const car1 = new Car("Eagle", "Talon TSi", 1993);

console.log(car1.make);
// Expected output: "Eagle"
```

## 语法

```js-nolint
new constructor
new constructor()
new constructor(arg1)
new constructor(arg1, arg2)
new constructor(arg1, arg2, /* …, */ argN)
```

### 参数

- `constructor`
  - : 一个指定对象实例的类型的类或函数。
- `arg1`、`arg2`、……、`argN`
  - : 一个用于被 `constructor` 调用的值列表。`new Foo` 与 `new Foo()` 等价，换句话说：如果没有指定参数列表，则在不带参数的情况下调用 `Foo`。

## 描述

当使用 **`new`** 关键字调用函数时，该函数将被用作构造函数。`new` 将执行以下操作：

1. 创建一个空的简单 JavaScript 对象。为方便起见，我们称之为 `newInstance`。
2. 如果构造函数的 `prototype` 属性是一个{{jsxref("Object", "对象", "", 1)}}，则将 `newInstance` 的 [[Prototype]] 指向构造函数的 `prototype` 属性，否则 `newInstance` 将保持为一个普通对象，其 [[Prototype]] 为 `Object.prototype`。

   > [!NOTE]
   > 因此，通过构造函数创建的所有实例都可以访问添加到构造函数 `prototype` 属性中的属性/对象。

3. 使用给定参数执行构造函数，并将 `newInstance` 绑定为 [`this`](/zh-CN/docs/Web/JavaScript/Reference/Operators/this) 的上下文（换句话说，在构造函数中的所有 `this` 引用都指向 `newInstance`）。
4. 如果构造函数返回[非原始值](/zh-CN/docs/Web/JavaScript/Guide/Data_structures#原始值)，则该返回值成为整个 `new` 表达式的结果。否则，如果构造函数未返回任何值或返回了一个原始值，则返回 `newInstance`。（通常构造函数不返回值，但可以选择返回值，以覆盖正常的对象创建过程。）

[类](/zh-CN/docs/Web/JavaScript/Reference/Classes)只能用 `new` 运算符实例化——尝试不使用 `new` 调用一个类将抛出 `TypeError`。

创建一个用户自定义的对象需要两步：

1. 通过编写指定对象名称和属性的函数来定义对象类型。例如，创建 `Foo` 对象的构造函数看起来可能像这样：

   ```js
   function Foo(bar1, bar2) {
     this.bar1 = bar1;
     this.bar2 = bar2;
   }
   ```

2. 通过 `new` 来创建对象实例。

   ```js
   const myFoo = new Foo("Bar 1", 2021);
   ```

> [!NOTE]
> 对象的属性可以是另一个对象。请参阅下面的示例。

你始终可以对已定义的对象添加新的属性。例如，`car1.color = "black"` 语句给 `car1` 添加了一个新的属性 `color`，并将其赋值为 `"black"`。

但是，这不会影响任何其他对象。要将新属性添加到相同类型的所有对象，你必须将该属性添加到构造函数的 `prototype` 属性中。其定义了由该函数创建的所有对象所共享的属性，而不仅仅是对象类型的其中一个实例。以下代码将一个值为 `"原色"` 的 `color` 属性添加到 `Car` 类型的所有对象，然后仅在实例对象 `car1` 中用字符串 `"黑色"` 覆盖该值。请参见[原型](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Function/prototype)以了解更多信息。

```js
function Car() {}
car1 = new Car();
car2 = new Car();

console.log(car1.color); // undefined

Car.prototype.color = "原色";
console.log(car1.color); // '原色'

car1.color = "黑色";
console.log(car1.color); // '黑色'

console.log(Object.getPrototypeOf(car1).color); // '原色'
console.log(Object.getPrototypeOf(car2).color); // '原色'
console.log(car1.color); // '黑色'
console.log(car2.color); // '原色'
```

> [!NOTE]
> 虽然构造函数可以像任何常规函数一样被调用（即不使用 `new` 运算符），但在这种情况下并不会创建一个新的对象，`this` 的值也是不一样的。

函数可以通过检查 [`new.target`](/zh-CN/docs/Web/JavaScript/Reference/Operators/new.target) 来知道它是否是通过 `new` 被调用的。当函数在没有使用 `new` 的情况下被调用时，`new.target` 的值为 `undefined`。例如，你可以有一个在被调用时和被构造时具有不同表现的函数：

```js
function Car(color) {
  if (!new.target) {
    // 以函数的形式被调用。
    return `${color}车`;
  }
  // 通过 new 被调用。
  this.color = color;
}

const a = Car("红"); // a 是“红车”
const b = new Car("红"); // b 是 `Car { color: "红" }`
```

在 ES6（引入了[类](/zh-CN/docs/Web/JavaScript/Reference/Classes)）之前，大多数 JavaScript 内置对象既可调用也可构造，尽管其中许多对象表现出不同的行为。举几个例子：

- [`Array()`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Array/Array)、[`Error()`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Error/Error) 以及 [`Function()`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Function/Function) 在被调用时和被构造时表现一致。
- [`Boolean()`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Boolean/Boolean)、[`Number()`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Number/Number) 以及 [`String()`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/String/String) 在被调用时将它们的参数强制转换为相应的原始类型，而在被构造时返回包装对象。
- [`Date()`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Date/Date) 在被调用时返回表示当前日期的字符串，相当于 `new Date().toString()`。

在 ES6 之后，语言对哪些是构造函数、哪些是函数有更严格的要求。例如：

- [`Symbol()`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Symbol/Symbol) 和 [`BigInt()`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/BigInt/BigInt) 只能在不使用 `new` 的情况下被调用。尝试构造它们将抛出 `TypeError`。
- [`Proxy`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Proxy/Proxy) 和 [`Map`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Map/Map) 只能通过 `new` 构造。尝试调用它们将抛出 `TypeError`。

## 示例

### 对象类型和对象实例

假设你要创建一个汽车的对象类型。你希望这个类型叫做 `Car`，这个类型具备 make、model、year 属性。要做到这些，你需要编写以下函数：

```js
function Car(make, model, year) {
  this.make = make;
  this.model = model;
  this.year = year;
}
```

现在，你可以如下所示创建一个 `myCar` 的对象：

```js
const myCar = new Car("鹰牌", "Talon TSi", 1993);
```

该语句创建了 `myCar` 并将其属性赋为指定的值。于是 `myCar.make` 的值“鹰牌”，`myCar.year` 的值为整数 1993，以此类推。

你可以通过调用 `new` 来创建任意个 `car` 对象。例如：

```js
const kensCar = new Car("尼桑", "300ZX", 1992);
```

### 对象属性为其他对象

假设你定义了一个叫做 `Person` 的对象：

```js
function Person(name, age, sex) {
  this.name = name;
  this.age = age;
  this.sex = sex;
}
```

然后实例化了两个新的 `Person` 对象如下：

```js
const rand = new Person("兰德·麦克纳利", 33, "男性");
const ken = new Person("肯·琼斯", 39, "男性");
```

然后你可以重写 `Car` 的定义，添加一个值为 `Person` 对象的 `owner` 属性，如下：

```js
function Car(make, model, year, owner) {
  this.make = make;
  this.model = model;
  this.year = year;
  this.owner = owner;
}
```

要实例化新的对象，你可以用如下代码：

```js
const car1 = new Car("鹰牌", "Talon TSi", 1993, rand);
const car2 = new Car("尼桑", "300ZX", 1992, ken);
```

创建对象时，并没有传字符串或数字，而是将对象 `rand` 和 `ken` 作为参数传递，来代表所有者。要查找 `car2` 的所有者的名称，你可以访问以下属性：

```js
car2.owner.name;
```

### 使用 `new` 和类

```js
class Person {
  constructor(name) {
    this.name = name;
  }
  greet() {
    console.log(`你好，我的名字是${this.name}`);
  }
}

const p = new Person("卡罗琳");
p.greet(); // 你好，我的名字是卡罗琳
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- {{jsxref("Function")}}
- {{jsxref("Reflect.construct()")}}
- {{jsxref("Object")}}

---
# Source: index.md
---
---
title: 逗号运算符（,）
slug: Web/JavaScript/Reference/Operators/Comma_operator
---

**逗号**（**`,`**）运算符对它的每个操作数从左到右求值，并返回最后一个操作数的值。这让你可以创建一个复合表达式，其中多个表达式被评估，复合表达式的最终值是其成员表达式中最右边的值。这通常用于为 [`for`](/zh-CN/docs/Web/JavaScript/Reference/Statements/for) 循环提供多个参数。

{{InteractiveExample("JavaScript Demo: Expressions - Comma operator")}}

```js interactive-example
let x = 1;

x = (x++, x);

console.log(x);
// Expected output: 2

x = (2, 3);

console.log(x);
// Expected output: 3
```

## 语法

```js-nolint
expr1, expr2, expr3/* , … */
```

## 参数

- `expr1`、`expr2`、`expr3`……
  - : 一个或多个表达式，最后一个表达式的返回值会作为当前复合表达式的值。

## 描述

当你想要在期望一个表达式的位置包含多个表达式时，可以使用逗号运算符。这个运算符最常用的一种情况是：在 `for` 循环中提供多个参数。

逗号运算符与数组、对象和函数参数中的逗号含义完全不同。

## 示例

假设 `a` 是一个二维数组，每一维度包含 10 个元素，以下代码通过使用逗号运算符，可以同时递增 `i` 和递减 `j`。

下面的代码打印一个二维数组中斜线方向的元素：

```js
for (let i = 0, j = 9; i <= 9; i++, j--) {
  console.log(`a[${i}][${j}] = ${a[i][j]}`);
}
```

请注意，赋值中的逗号运算符可能看起来没有逗号运算符的正常效果，因为它们并不存在于表达式中。在以下示例中，`a` 被设置为 `b=3` 的值（它是 3），但是表达式 `c=4` 仍然会经过评估，且它的值（也就是 4）会返回至控制台。这是由于[运算符的优先级和结合性](/zh-CN/docs/Web/JavaScript/Reference/Operators/Operator_precedence)。

```js-nolint
let a, b, c;

a = b = 3, c = 4; // 值 4 返回到控制台
console.log(a); // 3 (left-most)

let x, y, z;

x = (y = 5, z = 6); // 值 6 返回到控制台
console.log(x); // 6 (right-most)
```

### 处理后返回

另一个使用逗号运算符的例子是在返回值前处理一些操作。如前所述，逗号运算符只会返回最后一个元素，但其他表达式都会被求值。所以，可以这么做：

```js-nolint
function myFunc() {
  let x = 0;

  return (x += 1, x); // 与 return ++x; 等价
}
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- [`for` 循环](/zh-CN/docs/Web/JavaScript/Reference/Statements/for)

---
# Source: index.md
---
---
title: delete 运算符
slug: Web/JavaScript/Reference/Operators/delete
---

**`delete`** 运算符用于删除对象的一个属性；如果该属性的值是一个对象，并且没有更多对该对象的引用，该属性所持有的对象最终会自动释放。

{{InteractiveExample("JavaScript Demo: Expressions - delete operator")}}

```js interactive-example
const Employee = {
  firstname: "Maria",
  lastname: "Sanchez",
};

console.log(Employee.firstname);
// Expected output: "Maria"

delete Employee.firstname;

console.log(Employee.firstname);
// Expected output: undefined
```

## 语法

```js-nolint
delete object.property
delete object[property]
```

> [!NOTE]
> 该语法允许在 `delete` 运算符之后使用多种类型的表达式，但只有上述形式才能产生有意义的行为。

### 参数

- `object`
  - : 对象的名称，或计算结果为对象的表达式。
- `property`
  - : 要删除的属性。

### 返回值

对于大多数情况都是 `true`；如果属性是一个[自身](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Object/hasOwn)[不可配置](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Object/defineProperty#可配置属性)的属性，在这种情况下，非严格模式返回 `false`。

### 异常

- {{jsxref("TypeError")}}
  - : 如果属性是自身不可配置的属性且处于[严格模式](/zh-CN/docs/Web/JavaScript/Reference/Strict_mode)中，则会抛出该异常。
- {{jsxref("ReferenceError")}}
  - : 当 `object` 是 [`super`](/zh-CN/docs/Web/JavaScript/Reference/Operators/super) 时抛出。

## 描述

`delete` 运算符与其他像 [`typeof`](/zh-CN/docs/Web/JavaScript/Reference/Operators/typeof) 这样的一元运算符具有相同的[优先级](/zh-CN/docs/Web/JavaScript/Reference/Operators/Operator_precedence)。因此，它接受任何由更高优先级的运算符形成的表达式。然而，在[严格模式](/zh-CN/docs/Web/JavaScript/Reference/Strict_mode)下，以下形式会导致早期语法错误：

```js example-bad
delete identifier;
delete object.#privateProperty;
```

因为[类](/zh-CN/docs/Web/JavaScript/Reference/Classes)自动处于严格模式，而[私有元素](/zh-CN/docs/Web/JavaScript/Reference/Classes/Private_elements)只能在类体内合法引用，这意味着私有元素永远不能被删除。虽然 `delete identifier` 在 `identifier` 指的是全局对象的可配置属性时[可能有效](#删除全局属性)，但是你应该避免这种形式，而是用 [`globalThis`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/globalThis) 作为前缀。

虽然其他表达式是可以接受的，但是它们并不导致有意义的行为：

```js example-bad
delete console.log(1);
// 输出 1，返回 true，但是没有删除任何东西
```

`delete` 运算符从一个对象中删除一个给定的属性。在成功删除时，它将返回 `true`，否则将返回 `false`。不像一般人认为的那样（也许是由于其他编程语言，如 [C++ 中的 delete](https://docs.microsoft.com/cpp/cpp/delete-operator-cpp?view=msvc-170)），`delete` 操作符与直接释放内存**没有**关系。内存管理是通过破坏引用间接完成的。更多细节请参见[内存管理](/zh-CN/docs/Web/JavaScript/Guide/Memory_management)页面。

但是，以下情况需要重点考虑：

- 如果你试图删除的属性不存在，那么 `delete` 将不会起任何作用，但仍会返回 `true`。
- `delete` 只影响自身属性。如果对象的原型链上有一个与待删除属性同名的属性，那么删除属性之后，对象会使用原型链上的那个属性。
- 不可配置的属性不能被移除。这意味着像 {{jsxref("Math")}}、{{jsxref("Array")}}、{{jsxref("Object")}} 这些内置对象的属性以及使用 {{jsxref("Object.defineProperty()")}} 方法设置为不可配置的属性不能被删除。
- 删除包括函数参数内的变量永远不会奏效。`delete variable` 会在严格模式下抛出 {{jsxref("SyntaxError")}} 错误，非严格模式下不会有任何效果。
  - 任何使用 {{jsxref("Statements/var","var")}} 声明的属性不能从全局作用域或函数的作用域中删除，因为即使它们可能附加到[全局对象](/zh-CN/docs/Glossary/Global_object)上，它们也是不可配置的。
  - 任何使用 {{jsxref("Statements/let","let")}} 或 {{jsxref("Statements/const","const")}} 声明的属性不能够从它被声明的作用域中删除，因为它们没有附加到任何对象上。

## 示例

### 使用 delete

> [!NOTE]
> 以下示例使用了仅非严格模式下的功能，如隐式创建全局变量和删除标识符，这在严格模式下是禁止的。

```js
// 在全局作用域创建 empCount 属性
// 因为我们使用了 var，它会标记为不可配置
var empCount = 43;

// 在全局作用域创建 adminName 属性
// 因为没有使用 var，它会标记为可配置
adminName = "xyz";

EmployeeDetails = {
  name: "xyz",
  age: 5,
  designation: "Developer",
};

// delete 可用于删除对象的属性
delete EmployeeDetails.name; // 返回 true

// 甚至属性不存在，它也会返回 "true"
delete EmployeeDetails.salary; // 返回 true

// EmployeeDetails 是全局作用域的一个属性。
delete EmployeeDetails; // 返回 true

// 相反，empCount 是不可配置的，
// 因为创建它时使用了 var。
delete empCount; // 返回 false

// adminName 是全局作用域的一个属性。
// 因为它不是用 var 创建的，所以可以删除。
// 因此，它是可配置的。
delete adminName; // 返回 true

// delete 对内建静态属性不起作用
// 这些属性是不可配置的
delete Math.PI; // 返回 false

function f() {
  var z = 44;

  // delete 对局部变量名不起作用
  delete z; // 返回 false
}
```

### delete 和原型链

在下面的示例中，我们删除一个对象的自有属性，而原型链上具有相同名称的属性可用：

```js
function Foo() {
  this.bar = 10;
}

Foo.prototype.bar = 42;

var foo = new Foo();

// foo.bar 指代了自身属性
console.log(foo.bar); // 10

// 删除 foo 对象的自身属性
delete foo.bar; // 返回 true

// foo.bar 仍然在原型链上可用。
console.log(foo.bar); //42

// 从原型上删除属性
delete Foo.prototype.bar; // 返回 true

// 由于已删除“bar”属性，因此不能再从 Foo 继承它。
console.log(foo.bar); //undefined
```

### 删除数组元素

当你删除一个数组元素时，数组的长度（`length`）不受影响。即便你删除了数组的最后一个元素也是如此。

当用 `delete` 运算符删除一个数组元素时，被删除的元素已经不再属于该数组。下面的例子中用 `delete` 删除了 `trees[3]`。

```js
const trees = ["redwood", "bay", "cedar", "oak", "maple"];
delete trees[3];
console.log(3 in trees); // false
```

以上操作创建了一个[稀疏数组](/zh-CN/docs/Web/JavaScript/Guide/Indexed_collections#稀疏数组)，如果你想让一个数组元素继续存在，但是其值是 `undefined`，那么可以将 `undefined` 赋值给这个元素而不是使用 `delete`。下面的例子中，`trees[3]` 被赋值为 `undefined`，但该数组元素仍然存在。

```js
const trees = ["redwood", "bay", "cedar", "oak", "maple"];
trees[3] = undefined;
console.log(3 in trees); // true
```

如果你想通过改变数组的内容来移除一个数组元素，请使用 {{jsxref("Array/splice()", "splice()")}} 方法。在下面的例子中，通过使用 {{jsxref("Array/splice()", "splice()")}}，将 `trees[3]` 从数组中移除。

```js
const trees = ["redwood", "bay", "cedar", "oak", "maple"];
trees.splice(3, 1);
console.log(trees); // ["redwood", "bay", "cedar", "maple"]
```

### 删除不可配置属性

当一个属性被标记为不可配置时，`delete` 不会有任何效果，并将返回 `false`。在严格模式下，会抛出 `TypeError`。

```js
const Employee = {};
Object.defineProperty(Employee, "name", { configurable: false });

console.log(delete Employee.name); // 返回 false
```

{{jsxref("Statements/var","var")}} 会创建不可配置的属性，它不能用 `delete` 运算符删除。

```js
// 由于“nameOther”是使用 var 关键字声明的，
// 它被标记为不可配置的
var nameOther = "XYZ";

// 我们可以通过以下代码访问这个全局属性：
Object.getOwnPropertyDescriptor(globalThis, "nameOther");
// {
//   value: "XYZ",
//   writable: true,
//   enumerable: true,
//   configurable: false
// }

delete globalThis.nameOther; // 返回 false
```

在严格模式下，会抛出异常。

### 删除全局属性

如果一个全局属性是可配置的（例如，通过直接的属性赋值），它可以被删除，随后将它们作为全局变量的引用将产生 {{jsxref("ReferenceError")}}。

```js
globalThis.globalVar = 1;
console.log(globalVar); // 1
// 在非严格模式下，也可以使用 `delete globalVar`
delete globalThis.globalVar;
console.log(globalVar); // ReferenceError: globalVar is not defined
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- [深入分析 delete](http://perfectionkills.com/understanding-delete/)
- {{jsxref("Reflect.deleteProperty()")}}
- {{jsxref("Map.prototype.delete()")}}

---
# Source: index.md
---
---
title: 逻辑与（&&）
slug: Web/JavaScript/Reference/Operators/Logical_AND
---

当且仅当所有操作数为 `true` 时，一组布尔操作数的**逻辑与**（**`&&`**，逻辑连接）运算结果为 `true`，否则为 `false`。

一般来说，当从左到右求值时，该操作符返回第一个{{Glossary("falsy","假值")}}操作数的值；如果它们都是{{Glossary("truthy","真值")}}，则返回最后一个操作数的值。

{{InteractiveExample("JavaScript Demo: Expressions - Logical AND", "shorter")}}

```js interactive-example
const a = 3;
const b = -2;

console.log(a > 0 && b > 0);
// Expected output: false
```

## 语法

```js-nolint
expr1 && expr2
```

## 描述

逻辑与（`&&`）运算符从左到右对操作数求值，遇到第一个{{Glossary("falsy","假值")}}操作数时立即返回；如果所有的操作数都是{{Glossary("truthy","真值")}}，则返回最后一个操作数的值。

能够转化为 `true` 的值叫做{{Glossary("truthy","真值")}}，能够转化为 `false` 的值叫做{{Glossary("falsy","假值")}}。

能够转化为 false 的表达式的示例如下：

- `false`；
- `null`；
- `NaN`；
- `0`；
- 空字符串（`""` 或 `''` 或 ` `` `）；
- `undefined`。

与运算符会保留所有非布尔值，并原样返回它们：

```js
result = "" && "foo"; // 结果被赋值为 ""（空字符串）
result = 2 && 0; // 结果被赋值为 0
result = "foo" && 4; // 结果被赋值为 4
```

尽管 `&&` 运算符可以与非布尔操作数一起使用，但它仍然被认为是一个布尔运算符，因为它的返回值总是可以被转换为[布尔基本类型](/zh-CN/docs/Web/JavaScript/Guide/Data_structures#boolean_类型)。要明确地将其返回值（或任何一般的表达式）转换为相应的布尔值，请使用双[`非运算符`](/zh-CN/docs/Web/JavaScript/Reference/Operators/Logical_NOT)或 {{jsxref("Global_Objects/Boolean/Boolean", "Boolean")}} 构造函数。

### 短路求值

逻辑与是一种短路运算符。当每个操作数被转换为布尔值时，如果发现一个转换的结果是 `false`，那么逻辑与运算符就会停止，并返回该假操作数的原始值；它**不会**对任何其余的操作数求值。

考虑如下伪代码。

```plain
(some falsy expression) && expr
```

`expr` 部分**永远不会被求值**，因为第一个操作数 `(some falsy expression)` 被求值为{{Glossary("falsy","假值")}}。如果 `expr` 是一个函数，它将不会被调用。查看如下示例：

```js
function A() {
  console.log("调用了 A");
  return false;
}
function B() {
  console.log("调用了 B");
  return true;
}
console.log(A() && B());
// 由于调用了 A 函数，故会输出“调用了 A”到控制台，
// && 求值结果为 false（A 函数返回 false），然后输出 false 到控制台；
// 与运算符在这里短路，忽略了 B 函数
```

### 运算符优先级

与运算符的优先级高于或运算符，这意味着 `&&` 运算符在 `||` 运算符前执行（参见[运算符优先级](/zh-CN/docs/Web/JavaScript/Reference/Operators/Operator_precedence)）。

```js
true || (false && false); // true
true && (false || false); // false
2 === 3 || (4 < 0 && 1 === 1); // false
```

## 示例

### 使用与运算符

下列代码展示了 `&&`（逻辑与）运算符的用法。

```js
a1 = true && true; // t && t returns true
a2 = true && false; // t && f returns false
a3 = false && true; // f && t returns false
a4 = false && 3 === 4; // f && f returns false
a5 = "Cat" && "Dog"; // t && t returns "Dog"
a6 = false && "Cat"; // f && t returns false
a7 = "Cat" && false; // t && f returns false
a8 = "" && false; // f && f returns ""
a9 = false && ""; // f && f returns false
```

### 布尔值转化规则

#### 与运算符转化为或运算符

下述涉及到**布尔**运算符的运算：

```js-nolint
bCondition1 && bCondition2
```

总是与此表达式相同：

```js-nolint
!(!bCondition1 || !bCondition2)
```

#### 或运算符转化为与运算符

下述涉及到**布尔**运算符的运算：

```js-nolint
bCondition1 || bCondition2
```

总是与此表达式相同：

```js-nolint
!(!bCondition1 && !bCondition2)
```

### 去除嵌套的括号

由于逻辑表达式是从左到右进行求值的，只要遵循一定的规则，总是可以从一个复杂的表达式中删除括号。

下述涉及到**布尔**运算符的复杂运算：

```js-nolint
bCondition1 || (bCondition2 && bCondition3)
```

总是与此表达式相同：

```js-nolint
bCondition1 || bCondition2 && bCondition3
```

## 规范

{{Specifications}}

## 浏览器兼容性

{{Compat}}

## 参见

- {{jsxref("Boolean")}}
- {{Glossary("Truthy","真值")}}
- {{Glossary("Falsy","假值")}}

---
# Source: index.md
---
---
title: 废弃和过时的特性
slug: Web/JavaScript/Reference/Deprecated_and_obsolete_features
---

本附录列出了那些已经废弃（仍然可用，但是已计划删除）或者过时（已被删除，无法使用）的 JavaScript 特性。

## 废弃的特性

这些废弃的特性仍然可以使用，但是使用时一定要保持谨慎，因为它们很可能会在未来的某个时间点被移除。应当将其从需要使用的代码中移除。

ECMAScript 规范的 [Annex B](https://tc39.es/ecma262/#sec-additional-ecmascript-features-for-web-browsers) 部分列出了其中的一些废弃功能。这一部分被描述为规范性的可选功能，也就是说，web 浏览器主机必须实现这些功能，而非 web 主机可以不实现。这些功能很可能是稳定的，因为删除它们会导致向下兼容的问题，并破坏传统的网站（JavaScript 的设计目标是“不要破坏 web”）。尽管如此，它们还是不能跨平台移植，而且可能不被所有的分析工具所支持，所以建议你不要使用它们，正如 Annex B 的介绍所说：

> … All of the language features and behaviors specified in this annex have one or more undesirable characteristics and in the absence of legacy usage would be removed from this specification.（本附录中规定的所有语言特性和行为都有一个或多个不理想的特性，在没有遗留使用的情况下，将从本规范中删除。） …
>
> … Programmers should not use or assume the existence of these features and behaviors when writing new ECMAScript code.（程序员在编写新的 ECMAScript 代码时，不应该使用或假设这些特性和行为的存在。） …

其他一些，尽管在规范主体中，也被标记为规范性可选，不应该依赖它们。

### HTML 注释

如果 JavaScript 源码被作为脚本代码解析，它允许 HTML 注释，就像这些脚本是 `<script>` 的标签一部分那样。

以下是在 web 浏览器（或使用支持 Chrome 的 V8 引擎的 Node.js）中运行的有效 JavaScript 代码：

```js
<!-- 注释
console.log("a"); <!-- 另外一段注释
console.log("b");
--> 更多注释
// 输出 "a" 和 "b"
```

`<!--` 和 `-->` 的作用都与 `//` 类似，即起始行注释。`-->` 只在行首有效（以避免与紧跟大于运算符的后缀式自减相混淆），而 `<!--` 可以出现在行的任何地方。

### RegExp

下面的这些属性已经被废弃。这并不影响它们在[替换字符串](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/String/replace)中的使用。

- {{jsxref("RegExp/n", "$1–$9")}}
  - : 括号内的子串匹配结果。
- {{jsxref("RegExp.input", "input, $_")}}
  - : 用于匹配正则表达式的字符串。
- {{jsxref("RegExp.lastMatch", "lastMatch, $&amp;")}}
  - : 最后匹配的子串。
- {{jsxref("RegExp.lastParen", "lastParen, $+")}}
  - : 最后一个括号内的子串匹配。
- {{jsxref("RegExp.leftContext", "leftContext, $`")}}
  - : 最近一次匹配前的子串。
- {{jsxref("RegExp.rightContext", "rightContext, $'")}}
  - : 最近一次匹配后的子串。

> [!WARNING]
> 避免使用这些静态属性，因为它们可能导致[与外部代码交互时的问题](https://github.com/tc39/proposal-regexp-legacy-features/blob/master/subclass-restriction-motivation.md#legacy-static-properties-regexp1-etc)！

{{jsxref("RegExp/compile", "compile()")}} 方法已被废弃，请构造一个新的 `RegExp` 实例。

### Function

- 函数的 {{jsxref("Global_Objects/Function/caller", "caller")}} 和 [`arguments.callee`](/zh-CN/docs/Web/JavaScript/Reference/Functions/arguments/callee) 属性在严格模式中废弃且不可用。
- 应该在函数闭包中使用 {{jsxref("Functions/arguments", "arguments")}} 对象，而不是将 `arguments` 作为函数的一个属性来访问。

{{jsxref("Global_Objects/Function/caller", "caller")}} 和 {{jsxref("Global_Objects/Function/arguments", "arguments")}} 属性已经废弃，因为它们会泄漏调用函数的对象。应当在函数内部使用 `arguments` 对象来代替函数的 `arguments` 属性。

### Object

- [`Object.prototype.__proto__`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Object/proto) 访问器已被废弃。使用 [`Object.getPrototypeOf`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Object/getPrototypeOf) 和 [`Object.setPrototypeOf`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Object/setPrototypeOf) 代替。这不适用于对象字面量中的 `__proto__` 字面键。
- [`Object.prototype.__defineGetter__`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Object/__defineGetter__)、[`Object.prototype.__defineSetter__`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Object/__defineSetter__)、[`Object.prototype.__lookupGetter__`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Object/__lookupGetter__) 和 [`Object.prototype.__lookupSetter__`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Object/__lookupSetter__) 方法已被废弃。使用 [`Object.getOwnPropertyDescriptor`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Object/getOwnPropertyDescriptor) 和 [`Object.defineProperty`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Object/defineProperty)代替。

### String

- HTML 包装方法，如 {{jsxref("String.prototype.fontsize")}} 和 {{jsxref("String.prototype.big")}}。
- {{jsxref("String.prototype.substr")}} 可能不会很快被删除，但它被定义在 Annex B 中，因此是规范性的可选项。
- `String.prototype.trimLeft` 和 `String.prototype.trimRight` 应替换为 {{jsxref("String.prototype.trimStart")}} 和 {{jsxref("String.prototype.trimEnd")}}。

### Date

- {{jsxref("Global_Objects/Date/getYear", "getYear()")}} 和 {{jsxref("Global_Objects/Date/setYear", "setYear()")}}方法受千年虫问题影响，已并入 {{jsxref("Global_Objects/Date/getFullYear", "getFullYear")}} 和 {{jsxref("Global_Objects/Date/setFullYear", "setFullYear")}} 中。
- `toGMTString()` 方法已被弃用，请使用 {{jsxref("Global_Objects/Date/toUTCString", "toUTCString()")}} 方法。

### 转义序列

- 在字符串和正则表达式字面中，八进制转义序列（\ 后跟一个、两个或三个八进制数字）被弃用。
- {{jsxref("Global_Objects/escape", "escape")}} 和 {{jsxref("Global_Objects/unescape", "unescape")}} 函数已被弃用。使用 {{jsxref("Global_Objects/encodeURI", "encodeURI")}}、{{jsxref("Global_Objects/encodeURIComponent", "encodeURIComponent")}}、{{jsxref("Global_Objects/decodeURI", "decodeURI")}} 或 {{jsxref("Global_Objects/decodeURIComponent", "decodeURIComponent")}} 来对特殊字符的转义序列进行编码和解码。

### 语句

[`with`](/zh-CN/docs/Web/JavaScript/Reference/Statements/with) 语句在严格模式中已被弃用且不可用。

在严格模式下，[`for...in`](/zh-CN/docs/Web/JavaScript/Reference/Statements/for...in) 循环头的 `var` 声明中的初始化器被弃用并产生[语法错误](/zh-CN/docs/Web/JavaScript/Reference/Errors/Invalid_for-in_initializer)。在非严格模式下，它们会被静默地忽略。

## 过时的特性

这些过时的功能已经从 JavaScript 中完全删除，从指定的 JavaScript 版本开始就不能再使用了。

### RegExp

以下是 `RegExp` 实例的属性，不再是 `RegExp` 构造函数的属性：

| 属性                                                                | 描述                                                                             |
| ------------------------------------------------------------------- | -------------------------------------------------------------------------------- |
| {{jsxref("RegExp/global", "global")}}                               | 是否针对字符串中所有可能的匹配进行正则表达式测试，或者只针对第一个匹配进行测试。 |
| {{jsxref("RegExp/ignoreCase", "ignoreCase")}}                       | 在尝试匹配一个字符串时是否忽略大小写。                                           |
| {{jsxref("RegExp/lastIndex", "lastIndex")}}                         | 开始下一次匹配的索引。                                                           |
| {{jsxref("RegExp/multiline", "multiline")}}（也可通过 `RegExp.$*`） | 是否在多行的字符串中搜索。                                                       |
| {{jsxref("RegExp/source", "source")}}                               | 模式的文本。                                                                     |

`valueOf()` 方法不再专门用于 `RegExp`。它使用 {{jsxref("Object.prototype.valueOf()")}}，并返回它本身。

### Function

- Function 的 `arity` 属性已经过时，请使用 [`length`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Function/length) 代替。

### Object

| 属性                         | 描述                                                                       | 替代方法                                                                                                                                                            |
| ---------------------------- | -------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `__count__`                  | 返回直接在用户定义的对象上的可枚举属性的数量。                             | [`Object.keys()`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Object/keys)                                                                                  |
| `__parent__`                 | 指向对象的上下文                                                           | 没有直接的替换方法                                                                                                                                                  |
| `__iterator__`               | 和[遗留的生成器和迭代器](#遗留的生成器和迭代器)一起使用。                  | [`Symbol.iterator`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Symbol/iterator) 和新的[迭代协议](/zh-CN/docs/Web/JavaScript/Reference/Iteration_protocols) |
| `__noSuchMethod__`           | 当一个不存在的属性被作为方法调用时，这个方法被调用。                       | {{jsxref("Proxy")}}                                                                                                                                                 |
| `Object.prototype.eval()`    | 在指定对象的上下文中评估 JavaScript 代码字符串。                           | 没有直接的替换方法                                                                                                                                                  |
| `Object.observe()`           | 异步地观察一个对象的变化。                                                 | {{jsxref("Proxy")}}                                                                                                                                                 |
| `Object.unobserve()`         | 移除观察器。                                                               | {{jsxref("Proxy")}}                                                                                                                                                 |
| `Object.getNotifier()`       | 创建一个通知者对象，允许用 `Object.observe()` 来综合触发一个变化的观察者。 | 没有直接的替换方法                                                                                                                                                  |
| `Object.prototype.watch()`   | 在一个属性上附加一个处理器回调，当属性被分配时被调用。                     | {{jsxref("Proxy")}}                                                                                                                                                 |
| `Object.prototype.unwatch()` | 移除一个属性上的观察处理器。                                               | {{jsxref("Proxy")}}                                                                                                                                                 |

### String

- 非标准的字符串通用方法，如 `String.slice(myStr, 0, 12)`、`String.replace(myStr, /\./g, "!")` 等，在 Firefox 1.5（JavaScript 1.6）中引入，在 Firefox 53 中被废弃，并在 Firefox 68 中删除。你可以使用 {{jsxref("String", "String.prototype", "实例方法")}} 和 {{jsxref("Function.call")}} 来代替。
- `String.prototype.quote` 已在 Firefox 37 中移除。
- {{jsxref("String.prototype.search")}}、{{jsxref("String.prototype.match")}} 和 {{jsxref("String.prototype.replace")}} 中非标准的 `flags` 参数已被淘汰。

### WeakMap

- `WeakMap.prototype.clear()` 在 Firefox 20 中添加，在 Firefox 46 中移除。不可能遍历一个 [`WeakMap`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/WeakMap) 中的所有键。

### Date

- `Date.prototype.toLocaleFormat()` 使用与 C 语言中 `strftime()` 函数所期望的格式相同的格式字符串，已经过时了。使用 [`toLocaleString()`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Date/toLocaleString) 或 [`Intl.DateTimeFormat`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Intl/DateTimeFormat) 代替。

### Array

非标准的 Array 通用方法，如 `Array.slice(myArr, 0, 12)`、`Array.forEach(myArr, myFn)` 等，在 Firefox 1.5（JavaScript 1.6）中引入，在 Firefox 68 中被废弃，并在 Firefox 71 中删除。你可以使用 {{jsxref("Array", "Array.prototype", "实例方法")}} 和 {{jsxref("Function.call")}} 来代替。

| 属性                | 描述                 | 替代                |
| ------------------- | -------------------- | ------------------- |
| `Array.observe()`   | 异步地观察数组的变化 | {{jsxref("Proxy")}} |
| `Array.unobserve()` | 移除观察器。         | {{jsxref("Proxy")}} |

### Number

- `Number.toInteger()` 已经过时了。使用 [`Math.floor`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Math/floor)、[`Math.round`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Math/round) 或其他方法代替。

### Proxy

- `Proxy.create` 和 `Proxy.createFunction` 已经过时了，请使用 {{jsxref("Proxy/Proxy", "Proxy()")}} 构造函数。
- 下列陷入已经过时：
  - `hasOwn`（[bug 980565](https://bugzil.la/980565)，Firefox 33）
  - `getEnumerablePropertyKeys`（[bug 783829](https://bugzil.la/783829)，Firefox 37）
  - `getOwnPropertyNames`（[bug 1007334](https://bugzil.la/1007334)，Firefox 33）
  - `keys`（[bug 1007334](https://bugzil.la/1007334)，Firefox 33）

### ParallelArray

- `ParallelArray` 已过时。

### 语句

- `for each...in` 已经过时了，使用 {{jsxref("Statements/for...of", "for...of")}} 代替。
- let 块和 let 表达式已经过时了。
- 表达式闭包（`function () 1` 作为`function () { return 1; }` 的缩写）已经过时。使用常规的 {{jsxref("Operators/function", "function")}} 或{{jsxref("Functions/Arrow_functions", "箭头函数", "", 1)}}代替。

### 获取源文本

数组、数字、字符串等的 `toSource()` 方法和 `uneval()` 全局函数已经过时。使用 [`toString()`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Object/toString)，或者编写你自己的序列化方法来代替。

### 遗留的生成器和迭代器

遗留的生成器函数语句和遗留的生成器函数表达式被移除。传统的生成器函数语法重用了 `function` 关键字，当主体中有一个或多个 `yield` 表达式时，它自动成为生成器函数——现在这是一个语法错误。使用 [`function*` 语句](/zh-CN/docs/Web/JavaScript/Reference/Statements/function*)和 [`function*` 表达式](/zh-CN/docs/Web/JavaScript/Reference/Operators/function*)代替。

数组推导式和生成器推导式已被移除。

```js-nolint
// 遗留的数组推导式
[for (x of iterable) x]
[for (x of iterable) if (condition) x]
[for (x of iterable) for (y of iterable) x + y]

// 遗留的生成器推导式
(for (x of iterable) x)
(for (x of iterable) if (condition) x)
(for (x of iterable) for (y of iterable) x + y)
```

Firefox 26 版本之前实现了另一个迭代器协议，与标准的[迭代器协议](/zh-CN/docs/Web/JavaScript/Reference/Iteration_protocols)类似。当一个对象实现了 `next()` 方法时，它就是一个遗留的迭代器，该方法在每次调用时产生一个值，并在迭代结束时抛出一个 `StopIteration` 对象。这种遗留迭代器协议与标准迭代器协议不同：

- 值直接作为调用 `next()` 的返回值，而不是 `IteratorResult` 对象的 `value` 属性。
- 迭代终止是通过抛出一个 `StopIteration` 对象，而不是通过 `IteratorResult` 对象的 `done` 属性来表达。

这个功能，连同 `StopIteration` 全局构造函数，在 Firefox 58+ 中被移除。未来可以使用 [`for...of`](/zh-CN/docs/Web/JavaScript/Reference/Statements/for...of) 循环和[迭代器协议](/zh-CN/docs/Web/JavaScript/Reference/Iteration_protocols)。

### 变量引用语法（Sharp variable）

变量引用语法已经过时。要创建循环结构，请使用临时变量代替。

---
# Source: index.md
---
---
title: "Warning: -file- is being assigned a //# sourceMappingURL, but already has one"
slug: Web/JavaScript/Reference/Errors/Already_has_pragma
l10n:
  sourceCommit: a71b8929628a2187794754c202ad399fe357141b
---

当给定的 JavaScript 源文件被指定了多次源码映射时，JavaScript 会发出“-file- is being assigned a //# sourceMappingURL, but already has one.”警告。

## 错误信息

```plain
Warning: -file- is being assigned a //# sourceMappingURL, but already has one.
```

## 错误类型

警告。JavaScript 的执行不会中止。

## 什么地方出错了？

对于给定的 JavaScript 源码，源码映射规定了不止一次。

JavaScript 源码通常被组合和压缩，使其从服务器传递更加高效。使用[源码映射](https://www.html5rocks.com/en/tutorials/developertools/sourcemaps/)，调试器能够将执行的源码映射到原始的源码。有两种指派源码映射的方式，通过注释，或者对 JavaScript 设置标头。

## 示例

### 设置源码映射

使用文件中的注释来设置源码映射：

```js example-good
//# sourceMappingURL=http://example.com/path/to/your/sourcemap.map
```

或者，你可以对你的 JavaScript 文件设置标头：

```js example-good
X-SourceMap: /path/to/file.js.map
```

## 参见

- 火狐源代码文档中的[使用源码映射](https://firefox-source-docs.mozilla.org/devtools-user/debugger/how_to/use_a_source_map/index.html)
- 在 developer.chrome.google.cn 上的 [JavaScript 源码映射简介](https://developer.chrome.google.cn/blog/sourcemaps)（2012）

---
# Source: index.md
---
---
title: "Warning: unreachable code after return statement"
slug: Web/JavaScript/Reference/Errors/Stmt_after_return
l10n:
  sourceCommit: a71b8929628a2187794754c202ad399fe357141b
---

当在 {{jsxref("Statements/return", "return")}} 语句之后使用别的语句，或在无分号返回语句之后直接在后面跟随表达式，会出现 JavaScript 警告“unreachable code after return statement”。

## 错误信息

```plain
Warning: unreachable code after return statement (Firefox)
```

## 错误类型

警告

## 什么地方出错了？

在 `return` 语句之后的不可达的语句会在下列情形中产生：

- 在 {{jsxref("Statements/return", "return")}} 语句之后出现其他表达式；
- 在省略分号的 return 语句之后直接跟随一个表达式。

当一个表达式出现在一个有效的 `return` 表达式之后时，会出现这个警告，用以说明在 `return` 语句之后的表达式不可达，即这条语句之后的表达式永远不会运行。

为什么需要在 `return` 语句之后添加分号？在省略分号的 `return` 语句之后，开发者想要终止当前函数的执行还是返回 return 之后表达式的结果的意图是不明确的。这个警告表明这种情况下 `return` 语句的表述具有二义性。

当在省略分号的 return 语句之后出现下列语句时，不会出现警告：

- {{jsxref("Statements/throw", "throw")}}
- {{jsxref("Statements/break", "break")}}
- {{jsxref("Statements/var", "var")}}
- {{jsxref("Statements/function", "function")}}

## 示例

### 无效的例子

```js-nolint example-bad
function f() {
  let x = 3;
  x += 4;
  return x;   // return 立刻退出函数
  x -= 3;     // 因此这一行永远不会执行；它是不可到达的代码。
}

function g() {
  return     // 这被视为 `return;`
    3 + 4;   // 因此函数返回，这行永不执行。
}
```

### 有效的例子

```js-nolint example-good
function f() {
  let x = 3;
  x += 4;
  x -= 3;
  return x; // OK：在所有其他语句之后返回。
}

function g() {
  return 3 + 4 // OK：在同一行上，无需分号的返回表达式。
}
```

## 参见

- [自动分号补全](/zh-CN/docs/Web/JavaScript/Reference/Lexical_grammar#自动分号补全)

---
# Source: index.md
---
---
title: "SyntaxError: string literal contains an unescaped line break"
slug: Web/JavaScript/Reference/Errors/String_literal_EOL
---

## 信息

```plain
SyntaxError: Invalid or unexpected token (V8-based)
SyntaxError: '' string literal contains an unescaped line break (Firefox)
SyntaxError: Unexpected EOF (Safari)
```

## 错误类型

{{jsxref("SyntaxError")}}

## 哪里出错了？

某处 js 解析字符串出错。字符串必须使用单引号或双引号来正确的关闭。在 Javascript 中使用单引号的字符和双引号的字符串是没有区别的。字符串用[转义字符](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/String#转义序列)不是单引号就是双引。为解决这个错误，检查一下：

- 你字符串的引号是否成对。
- 你是否正确使用了转义序列
- 你的字符串是否在多行中解析正常。

## 示例

### 多行字符串

在 javascript 中你不能够直接使用多行字符串赋值给一个变量。如下：

```js example-bad
var longString = "This is a very long string which needs
                  to wrap across multiple lines because
                  otherwise my code is unreadable.";
// SyntaxError: unterminated string literal
```

可以使用["+"运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators#addition)，反斜杠，或[模板字符串](/zh-CN/docs/Web/JavaScript/Reference/Template_literals)来代替多行。“+”运算符的使用如下：

```js example-good
var longString =
  "This is a very long string which needs " +
  "to wrap across multiple lines because " +
  "otherwise my code is unreadable.";
```

或者你可以使用“\”在每一行的末尾，以表示该字符串在下一行继续。要确保“\“之后没有没有空格和任何其他的字符，及缩进，否则该“\”将不会起作用。使用方法如下：

```js example-good
var longString =
  "This is a very long string which needs \
to wrap across multiple lines because \
otherwise my code is unreadable.";
```

另一种方式是使用 ES 2015 的环境所支持[模板字符串](/zh-CN/docs/Web/JavaScript/Reference/Template_literals)（反引号\` \`）。

```js example-good
var longString = `This is a very long string which needs
                  to wrap across multiple lines because
                  otherwise my code is unreadable.`;
```

## 相关

- {{jsxref("String")}}
- [模板字符串](/zh-CN/docs/Web/JavaScript/Reference/Template_literals)

---
# Source: index.md
---
---
title: 'TypeError: "x" has no properties'
slug: Web/JavaScript/Reference/Errors/No_properties
---

## 错误信息

```plain
TypeError: null has no properties
TypeError: undefined has no properties
```

## 错误类型

{{jsxref("TypeError")}}.

## 哪里出错了？

{{jsxref("null")}} 和 {{jsxref("undefined")}}中，没有你需要的属性。

## 示例

```js example-bad
null.foo;
// 错误类型：null 没有这个属性

undefined.bar;
// 错误类型：undefined 没有这个属性
```

## 参考

- {{jsxref("null")}}
- {{jsxref("undefined")}}

---
# Source: index.md
---
---
title: 'TypeError: invalid assignment to const "x"'
slug: Web/JavaScript/Reference/Errors/Invalid_const_assignment
---

## 错误提示

```plain
TypeError: invalid assignment to const "x" (Firefox)
TypeError: Assignment to constant variable. (Chrome)
TypeError: Redeclaration of const 'x' (IE/Edge)
```

## 错误类型

{{jsxref("TypeError")}}

## 哪里出错了？

常量指的是无法在程序正常运行过程中进行修改的值。一方面无法通过重新赋值进行修改，另外一方面也无法进行重新声明。在 JavaScript 中，常量通过关键字 [`const`](/zh-CN/docs/Web/JavaScript/Reference/Statements/const) 来声明。

## 示例

### 不合法的二次声明

在同一作用域内为相同的常量名进行赋值会报错。

```js example-bad
const COLUMNS = 80;

// ...

COLUMNS = 120; // TypeError: invalid assignment to const `COLUMNS'
```

### 问题修复

修复的方式有很多种。可以根据你想要达到的目的来有针对性地对其进行处理。

#### 重新命名

如果想要声明另一个变量，那么请选择其他名称对其重新命名。原来的常量名在该作用域中已经被占有。

```js example-good
const COLUMNS = 80;
const WIDE_COLUMNS = 120;
```

#### `const`, `let` or `var`?

如果你的目的不是为了创建一个常量的话，那么就不要使用 const 关键字。可以使用 [`let`](/zh-CN/docs/Web/JavaScript/Reference/Statements/let) 关键字来声明一个拥有块作用域的变量，或者使用 `var` 来声明一个全局变量。

```js example-good
let columns = 80;

// ...

let columns = 120;
```

#### 作用域

检查一下作用域是否正确。例如这个常量是否应该出现在当前作用域，还是应该出现在函数内部？

```js example-good
const COLUMNS = 80;

function setupBigScreenEnvironment() {
  const COLUMNS = 120;
}
```

### `const 与不可变性`

const 声明语句创建了一个对值的只读引用。这并**不**意味着它指向的值是不可变的，而是说这个变量标记符不能被再次分配。例如，在值是对象的情况下，引用的对象自身内容依然是可以改变的。不能改变该变量的引用：

```js example-bad
const obj = { foo: "bar" };
obj = { foo: "baz" }; // TypeError: invalid assignment to const `obj'
```

但是可以改变它引用的值的属性：

```js example-good
obj.foo = "baz";
obj; // Object { foo: "baz" }
```

## 相关内容

- [`const`](/zh-CN/docs/Web/JavaScript/Reference/Statements/const)
- [`let`](/zh-CN/docs/Web/JavaScript/Reference/Statements/let)
- [`var`](/zh-CN/docs/Web/JavaScript/Reference/Statements/var)

---
# Source: index.md
---
---
title: 'ReferenceError: "x" is not defined'
slug: Web/JavaScript/Reference/Errors/Not_defined
l10n:
  sourceCommit: 1b2c87c20466d2a3eec9b3551c269f9aff8f5762
---

当某个地方引用了一个不存在的变量时，就会出现“_variable_ is not defined”JavaScript 异常。

## 错误信息

```plain
ReferenceError: "x" is not defined (V8-based & Firefox)
ReferenceError: Can't find variable: x (Safari)
```

## 错误类型

{{jsxref("ReferenceError")}}。

## 什么地方出错了？

在某处引用了一个不存在的变量。需要声明该变量，或确保它在当前脚本或[作用域](/zh-CN/docs/Glossary/Scope)中可用。

> [!NOTE]
> 在加载库（例如 jQuery）时，确保在访问库变量（例如“$”）之前先加载该库。将加载库的 {{HTMLElement("script")}} 元素放在使用该库的代码之前。

## 示例

### 未声明的变量

```js example-bad
foo.substring(1); // ReferenceError: foo is not defined
```

“foo”变量在任何地方都没有定义。它需要是一个字符串，以便 {{jsxref("String.prototype.substring()")}} 方法能够正常工作。

```js example-good
const foo = "bar";
foo.substring(1); // "ar"
```

### 错误的作用域

变量需要在当前执行上下文中可用。在[函数](/zh-CN/docs/Web/JavaScript/Reference/Functions)内部定义的变量无法在函数外部访问，因为该变量只在函数的作用域内定义。

```js example-bad
function numbers() {
  const num1 = 2;
  const num2 = 3;
  return num1 + num2;
}

console.log(num1); // ReferenceError num1 is not defined.
```

然而，函数可以访问在其定义的作用域内定义的所有变量和函数。换句话说，定义在全局作用域中的函数可以访问在全局作用域中定义的所有变量。

```js example-good
const num1 = 2;
const num2 = 3;

function numbers() {
  return num1 + num2;
}

console.log(numbers()); // 5
```

## 参见

- [作用域](/zh-CN/docs/Glossary/Scope)
- [JavaScript 指南中的变量声明](/zh-CN/docs/Web/JavaScript/Guide/Grammar_and_types#声明变量)
- [JavaScript 指南中的函数作用域](/zh-CN/docs/Web/JavaScript/Guide/Functions#函数作用域)

---
# Source: index.md
---
---
title: "SyntaxError: for-in loop head declarations may not have initializers"
slug: Web/JavaScript/Reference/Errors/Invalid_for-in_initializer
---

## 错误提示

```plain
SyntaxError: for-in loop head declarations may not have initializers (Firefox)

SyntaxError: for-in loop variable declaration may not have an initializer. (Chrome)
```

## 错误类型

该 {{jsxref("SyntaxError")}} 只出现于[严格模式](/zh-CN/docs/Web/JavaScript/Reference/Strict_mode)下。

## 哪里出错了？

在 [for...in](/zh-CN/docs/Web/JavaScript/Reference/Statements/for...in) 循环的头部存在初始化表达式。也就是存在变量声明并且被赋值，例如 |`for (var i = 0 in obj)`|。在非严格模式下，这种在循环头部的变量声明会被静默忽略，语句的表现形式与 `|for (var i in obj)|`相同。而在[严格模式](/zh-CN/docs/Web/JavaScript/Reference/Strict_mode)下，会报语法错误。

## 示例

下面这个示例会报语法错误（`SyntaxError`）：

```js-nolint example-bad
const obj = { a: 1, b: 2, c: 3 };

for (const i = 0 in obj) {
  console.log(obj[i]);
}

// SyntaxError: for-in loop head declarations may not have initializers
```

### 合法的 for-in 循环

可以把初始化语句 (`i = 0`) 从 for-in 循环的头部移除。

```js example-good
"use strict";

var obj = { a: 1, b: 2, c: 3 };

for (var i in obj) {
  console.log(obj[i]);
}
```

### 数组迭代

for...in 循环[不应该应用于数组迭代中](/zh-CN/docs/Web/JavaScript/Reference/Statements/for...in#array_iteration_and_for...in)。是否考虑使用 [`for`](/zh-CN/docs/Web/JavaScript/Reference/Statements/for) 循环而不是 `for-in` 循环来遍历数组（{{jsxref("Array")}}）？在 for 循环中是允许使用初始化语句的：

```js example-good
var arr = ["a", "b", "c"];

for (var i = 2; i < arr.length; i++) {
  console.log(arr[i]);
}

// "c"
```

## 相关内容

- [`for...in`](/zh-CN/docs/Web/JavaScript/Reference/Statements/for...in)
- [`for...of`](/zh-CN/docs/Web/JavaScript/Reference/Statements/for...of) – 无论是在严格模式下还是非严格模式下也都不允许使用初始化语句。
- [`for`](/zh-CN/docs/Web/JavaScript/Reference/Statements/for) – 更适用于数组迭代，因为允许使用初始化语句。

---
# Source: index.md
---
---
title: "TypeError: cyclic object value"
slug: Web/JavaScript/Reference/Errors/Cyclic_object_value
---

在[JSON](https://www.json.org/)中出现循环引用时，JavaScript 会抛出 "cyclic object value" 的异常。{{jsxref("JSON.stringify()")}}并不会尝试解决这个问题，因此导致运行失败。

## 提示信息

```js
TypeError: cyclic object value (Firefox)
TypeError: Converting circular structure to JSON (Chrome and Opera)
TypeError: Circular reference in value argument not supported (Edge)
```

## 错误类型

{{jsxref("TypeError")}}

## 哪里出错了？

[JSON 格式](https://www.json.org/)本身不支持循环引用对象（尽管存在[IETF 草案](https://datatracker.ietf.org/doc/html/draft-pbryan-zyp-json-ref-03))，因此 {{jsxref("JSON.stringify()")}} 并不会尝试解决这个问题而是直接运行失败。

## 示例

### 循环引用

在如下循环结构中：

```js
var circularReference = { otherData: 123 };
circularReference.myself = circularReference;
```

{{jsxref("JSON.stringify()")}} 将会报错

```js example-bad
JSON.stringify(circularReference);
// TypeError: cyclic object value
```

要处理循环引用的 JSON，可以使用支持这种结构的库 (例如[cycle.js](https://github.com/douglascrockford/JSON-js/blob/master/cycle.js)))，或者自己实现，需要通过可序列化值查找、替换或者移除循环引用。

下面的代码片段演示了如何使用{{jsxref("JSON.stringify()")}}的 `replacer` 参数查找和过滤（会导致数据丢失）循环引用。

```js
const getCircularReplacer = () => {
  const seen = new WeakSet();
  return (key, value) => {
    if (typeof value === "object" && value !== null) {
      if (seen.has(value)) {
        return;
      }
      seen.add(value);
    }
    return value;
  };
};

JSON.stringify(circularReference, getCircularReplacer());
// {"otherData":123}
```

## 参见

- {{jsxref("JSON.stringify")}}
- [cycle.js](https://github.com/douglascrockford/JSON-js/blob/master/cycle.js)
  – 介绍两个方法，`JSON.decycle` 和
  `JSON.retrocycle`，这两个方法能够对循环对象引用结构进行编码和解码，并且使之成为一种扩展的且向下兼容的 JSON 格式。

---
# Source: index.md
---
---
title: "RangeError: invalid date"
slug: Web/JavaScript/Reference/Errors/Invalid_date
---

## 消息

```plain
范围错误：非法数据 (Firefox)
范围错误：非法时间值 (Chrome)
范围错误：提供的数据不是有效的 (Chrome)
```

## 错误类型

{{jsxref("RangeError")}}

## 哪里出错了？

为 {{jsxref("Date")}} 或 {{jsxref("Date.parse()")}} 提供了一个会导致无效日期的字符串。

## 示例

### 错误示例

ISO 格式化字符串中不可识别的字符串或者包含非法元素值的日期一般会返回 {{jsxref("NaN")}}。然而，根据实现的不同，不符合 ISO 格式的字符串可能也会抛出 `RangeError: invalid date`，比如在火狐浏览器中有以下情形：

```js example-bad
new Date("foo-bar 2014");
new Date("2014-25-23").toISOString();
new Date("foo-bar 2014").toString();
```

然而下面这种情形会返回 {{jsxref("NaN")}} ：

```js example-bad
Date.parse("foo-bar 2014"); // NaN
```

参见 {{jsxref("Date.parse()")}} 文档，了解更多详情。

### 正确示例

```js example-good
new Date("05 October 2011 14:48 UTC");
```

## 参见

- {{jsxref("Date")}}
- {{jsxref("Date.prototype.parse()")}}
- {{jsxref("Date.prototype.toISOString()")}}

---
# Source: index.md
---
---
title: "TypeError: Reduce of empty array with no initial value"
slug: Web/JavaScript/Reference/Errors/Reduce_of_empty_array_with_no_initial_value
---

## 消息

```plain
TypeError: reduce of empty array with no initial value
```

## 错误类型

{{jsxref("TypeError")}}

## 哪里出问题了？

在 JavaScript 中，有一些 reduce 函数：

- {{jsxref("Array.prototype.reduce()")}}，{{jsxref("Array.prototype.reduceRight()")}} 和
- {{jsxref("TypedArray.prototype.reduce()")}}， {{jsxref("TypedArray.prototype.reduceRight()")}})。

这些函数有选择性的接收 `initialValue` (将会被用作回调函数第一次被调用的参数)。然而，如果没有初始值提供，它会用 {{jsxref("Array")}} 或 {{jsxref("TypedArray")}} 的第一个元素作为初始值。当提供一个空数组的时候这个错误会出现，因为那种情况下没有初始值被返回。

## 示例

### 无效的情况

当和过滤器（{{jsxref("Array.prototype.filter()")}}、{{jsxref("TypedArray.prototype.filter()")}}）结合使用的时候，可能会出现列表中所有元素被移除的情况。因此导致初始值为空。

```js example-bad
var ints = [0, -1, -2, -3, -4, -5];
ints
  .filter((x) => x > 0) // removes all elements
  .reduce((x, y) => x + y); // no more elements to use for the initial value.
```

类似的，当选择器中有瑕疵的时候相同的问题会发生，或者是列表中未预期的数量的元素：

```js example-bad
var names = document.getElementsByClassName("names");
var name_list = Array.prototype.reduce.call(
  names,
  (acc, name) => acc + ", " + name,
);
```

### 有效的情况

这个问题有两种可能的解决办法：

一种是提供一个初始值作为操作符的中立元素，比如加法里的 0，乘法里的 1，或者是合并中的一个空字符串。

```js example-good
var ints = [0, -1, -2, -3, -4, -5];
ints
  .filter((x) => x < 0) // removes all elements
  .reduce((x, y) => x + y, 0); // the initial value is the neutral element of the addition
```

另一种办法是两方处理空的情况，要么在调用 `reduce` 之前，或者是在添加一个未预料的初始虚拟址后的回调函数中：

```js example-good
var names = document.getElementsByClassName("names");

var name_list1 = "";
if (names1.length >= 1)
  name_list1 = Array.prototype.reduce.call(
    names,
    (acc, name) => acc + ", " + name,
  );
// name_list1 == "" when names is empty.

var name_list2 = Array.prototype.reduce.call(
  names,
  (acc, name) => {
    if (acc == "")
      // initial value
      return name;
    return acc + ", " + name;
  },
  "",
);
// name_list2 == "" when names is empty.
```

## 参见

- {{jsxref("Array.prototype.reduce()")}}
- {{jsxref("Array.prototype.reduceRight()")}}
- {{jsxref("TypedArray.prototype.reduce()")}}
- {{jsxref("TypedArray.prototype.reduceRight()")}}
- {{jsxref("Array")}}
- {{jsxref("TypedArray")}}
- {{jsxref("Array.prototype.filter()")}}
- {{jsxref("TypedArray.prototype.filter()")}}

---
# Source: index.md
---
---
title: "SyntaxError: missing } after property list"
slug: Web/JavaScript/Reference/Errors/Missing_curly_after_property_list
---

## 信息

```plain
SyntaxError: missing } after property list
```

## 错误类型

{{jsxref("SyntaxError")}}

## 哪里出错了？

在[对象初始化](/zh-CN/docs/Web/JavaScript/Reference/Operators/Object_initializer)的时候语法出错了。可能是遗漏了一个大括号，也可能是遗漏了逗号。还要检查是否以正确的顺序关闭了大括号或括号。缩进或格式化代码也许可以更好帮助你看清这些芜杂的。

## 示例

### 遗漏的逗号

很多情况下，对象初始值代码会中缺少逗号：

```js example-bad
var obj = {
  a: 1,
  b: { myProp: 2 }
  c: 3
};
```

正确的是：

```js example-good
var obj = {
  a: 1,
  b: { myProp: 2 },
  c: 3,
};
```

## 相关

- [Object initializer](/zh-CN/docs/Web/JavaScript/Reference/Operators/Object_initializer)

---
# Source: index.md
---
---
title: 'TypeError: "x" is not a function'
slug: Web/JavaScript/Reference/Errors/Not_a_function
---

JavaScript 异常"is not a function"会在试图去调用一个像函数一样的值，但是该值实际上不是函数时被抛出。

## 信息

```plain
TypeError: Object doesn't support property or method {x} (Edge)
TypeError: "x" is not a function
```

## 错误类型

{{jsxref("TypeError")}}

## 哪里出错了？

问题出在你试图去调用一个像函数一样的值，但是该值实际上不是函数，有时候你的代码需要调用一些函数，但是那种值并不能当作函数来被调用。

也许函数名称上有错别字？也许你正在调用 Object 对象没有这个方法？例如，在 JavaScript 中单纯的对象 (Object) 没有**map**函数，但是 JavaScript 数组 (Array) 对象却有这个函数。

再比如，在 JavaScript 中很多原生对象的内置方法需要你提供一个（回调）函数。所以你必须提供一个函数，以使这些方法正常工作：

- 当你在使用 {{jsxref("Array")}} 或 {{jsxref("TypedArray")}} 对象时：
  - {{jsxref("Array.prototype.every()")}}, {{jsxref("Array.prototype.some()")}}, {{jsxref("Array.prototype.forEach()")}}, {{jsxref("Array.prototype.map()")}}, {{jsxref("Array.prototype.filter()")}}, {{jsxref("Array.prototype.reduce()")}}, {{jsxref("Array.prototype.reduceRight()")}}, {{jsxref("Array.prototype.find()")}}

- 当你在使用 {{jsxref("Map")}} 和 {{jsxref("Set")}} 对象时：
  - {{jsxref("Map.prototype.forEach()")}} and {{jsxref("Set.prototype.forEach()")}}

## 示例

### 函数的名称错误

函数的名称拼写错误，这种情况是经常发生的：

```js example-bad
var x = document.getElementByID("foo");
// TypeError: document.getElementByID is not a function
```

正确的方法名应该是 `getElementById：`

```js example-good
var x = document.getElementById("foo");
```

### 调用 Object 类型中不存在的方法

对于某些特殊的方法，它只属于某些特定的原生对象中，你必须提供一个回调函数才能正常运行。例如：这里调用了一个 {{jsxref("Array.prototype.map()")}} 方法，但是这方法只能被 {{jsxref("Array")}} 对象所调用。

```js example-bad
var obj = { a: 13, b: 37, c: 42 };

obj.map(function (num) {
  return num * 2;
});

// TypeError: obj.map is not a function
```

正确的做法，使用一个数组来代替：

```js example-good
var numbers = [1, 4, 9];

numbers.map(function (num) {
  return num * 2;
});

// Array [ 2, 8, 18 ]
```

### 函数与已有属性重名

当你在创建类时，可能会存在某个属性和某个方法的名称相同，当你在调用该函数时，编译器会认为该函数不存在。

```js example-bad
var Dog = function () {
  this.age = 11;
  this.color = "black";
  this.name = "Ralph";
  return this;
};

Dog.prototype.name = function (name) {
  this.name = name;
  return this;
};

var myNewDog = new Dog();
myNewDog.name("Cassidy"); //Uncaught TypeError: myNewDog.name is not a function
```

正确的做法是使用不同的变量名。

```js example-good
var Dog = function () {
  this.age = 11;
  this.color = "black";
  this.dogName = "Ralph"; //Using this.dogName instead of .name
  return this;
};

Dog.prototype.name = function (name) {
  this.dogName = name;
  return this;
};

var myNewDog = new Dog();
myNewDog.name("Cassidy"); //Dog { age: 11, color: 'black', dogName: 'Cassidy' }
```

### 使用括号进行乘法运算

在数学中，你可以将 2 × (3 + 5) 写为 2\*(3 + 5) 或者省略为 2(3 + 5).

使用后者时将会抛出错误：

```js example-bad
const sixteen = 2(3 + 5);
alert("2 x (3 + 5) is " + String(sixteen));
//Uncaught TypeError: 2 is not a function
```

你可以添加乘法运算符 `*` 来改正代码：

```js example-good
const sixteen = 2 * (3 + 5);
alert("2 x (3 + 5) is " + String(sixteen));
//2 x (3 + 5) is 16
```

### 正确地导入和导出模块

确保正确导入模块。

以下为一个示例模块 (`helpers.js`)

```plain
let helpers = function () { };

helpers.groupBy = function (objectArray, property) {
  return objectArray.reduce(function (acc, obj) {
    var key = obj[property];
    if (!acc[key]) {
      acc[key] = [];
    }
    acc[key].push(obj);
    return acc;
  },
{});
}

export default helpers;
```

在 `App.js`中正确导入该模块：

```plain
import helpers from './helpers'
```

## 相关

- [Functions](/zh-CN/docs/Web/JavaScript/Reference/Functions)

---
# Source: index.md
---
---
title: 'TypeError: property "x" is non-configurable and can''t be deleted'
slug: Web/JavaScript/Reference/Errors/Cant_delete
---

## 消息

```plain
TypeError: property "x" is non-configurable and can't be deleted. (Firefox)
TypeError: Cannot delete property 'x' of #<Object> (Chrome)
```

## 错误类型

{{jsxref("TypeError")}} 只出现在严格模式下。

## 哪里有问题？

尝试删除某个属性，但是这个属性是[不可配置的](/zh-CN/docs/Web/JavaScript/Guide/Data_structures#属性)。`configurable` 属性控制是否该属性能从对象上删除，以及它的属性（除了`writable`）能否被修改。

这个错误仅仅在[严格模式](/zh-CN/docs/Web/JavaScript/Reference/Strict_mode)下出现。在非严格模式下，这个操作返回 `false`。

## 示例

不可配置的属性并不特别常见，但是它们可以使用 {{jsxref("Object.defineProperty()")}} 或 {{jsxref("Object.freeze()")}} 创建。

```js example-bad
"use strict";
var obj = Object.freeze({ name: "Elsa", score: 157 });
delete obj.score; // TypeError

("use strict");
var obj = {};
Object.defineProperty(obj, "foo", { value: 2, configurable: false });
delete obj.foo; // TypeError

("use strict");
var frozenArray = Object.freeze([0, 1, 2]);
frozenArray.pop(); // TypeError
```

也有一些内建于 JavaScript 的不可配置属性。你可能会尝试删除一个数学常量。

```js example-bad
"use strict";
delete Math.PI; // TypeError
```

## 参见

- [delete operator](/zh-CN/docs/Web/JavaScript/Reference/Operators/delete)
- {{jsxref("Object.defineProperty()")}}
- {{jsxref("Object.freeze()")}}

---
# Source: index.md
---
---
title: "SyntaxError: invalid assignment left-hand side"
slug: Web/JavaScript/Reference/Errors/Invalid_assignment_left-hand_side
l10n:
  sourceCommit: ee1599cba00284fd6af713e61e96dae61bb10287
---

当在代码中出现意外的赋值情况时，JavaScript 就会抛出“invalid assignment left-hand side”的异常。当使用单个 `=` 符号而不是 `==` 或 `===` 时，可能会触发此异常。

## 错误信息

```plain
SyntaxError: Invalid left-hand side in assignment (V8-based)
SyntaxError: invalid assignment left-hand side (Firefox)
SyntaxError: Left side of assignment is not a reference. (Safari)
```

## 错误类型

{{jsxref("SyntaxError")}} 或 {{jsxref("ReferenceError")}}，根据语法情况来定。

## 什么地方出错了？

在某处出现了意外的赋值情况。比如说，这可能是因为[赋值运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators#赋值运算符)与[相等运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators#相等运算符)不匹配。单个 `=` 符号用于给变量赋值，而 `==` 或 `===` 运算符则是用于比较值。

## 示例

### 典型的无效赋值情况

```js-nolint example-bad
if (Math.PI + 1 = 3 || Math.PI + 1 = 4) {
  console.log("没门！");
}
// SyntaxError: invalid assignment left-hand side

const str = "你好，" += "你是在" += "找我吗？";
// SyntaxError: invalid assignment left-hand side
```

在 `if` 语句中，你需要使用严格相等运算符（`===`），而对于字符串拼接，则需要使用加号（`+`）运算符。

```js-nolint example-good
if (Math.PI + 1 === 3 || Math.PI + 1 === 4) {
  console.log("没门！");
}

const str = "你好，" + "来自" + "另一个世界！";
```

### 导致 ReferenceError 的赋值操作

无效的赋值操作不一定会产生语法错误。有时语法几乎是正确的，但在运行过程中，左侧表达式计算得出的是一个*值*而非*引用*，因此赋值仍然无效。这类错误会在程序执行到该语句时发生，即在实际执行阶段出现。

```js-nolint example-bad
function foo() {
  return { a: 1 };
}
foo() = 1; // ReferenceError: invalid assignment left-hand side
```

函数调用、[`new`](/zh-CN/docs/Web/JavaScript/Reference/Operators/new) 调用、[`super()`](/zh-CN/docs/Web/JavaScript/Reference/Operators/super) 和 [`this`](/zh-CN/docs/Web/JavaScript/Reference/Operators/this) 都是值而不是引用。如果你想在左侧使用它们，赋值目标需要是它们产生的属性值。

```js example-good
function foo() {
  return { a: 1 };
}
foo().a = 1;
```

> [!NOTE]
> 在 Firefox 和 Safari 中，第一个示例在非严格模式下会产生 `ReferenceError` 错误，而在[严格模式](/zh-CN/docs/Web/JavaScript/Reference/Strict_mode)下则会产生 `SyntaxError` 错误。Chrome 在严格模式和非严格模式下都会抛出运行时的 `ReferenceError` 错误。

### 使用可选链运算符作为赋值目标

[可选链运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators/Optional_chaining)不是有效的赋值目标。

```js-nolint example-bad
obj?.foo = 1; // SyntaxError: invalid assignment left-hand side
```

相反，你必须首先处理可能为空值的情况。

```js example-good
if (obj) {
  obj.foo = 1;
}
```

## 参见

- [赋值运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators#赋值运算符)
- [相等运算符](/zh-CN/docs/Web/JavaScript/Reference/Operators#相等运算符)

---
# Source: index.md
---
---
title: "RangeError: repeat count must be non-negative"
slug: Web/JavaScript/Reference/Errors/Negative_repetition_count
---

## 信息

```plain
RangeError: repeat count must be non-negative (Firefox)
RangeError: Invalid count value (Chrome)
```

## 错误类型

{{jsxref("RangeError")}}

## 发生了什么？

代码中使用了 {{jsxref("String.prototype.repeat()")}}方法。它有一个计数参数，表示重复该字符串的次数。该参数必须在 0 及正 {{jsxref("Infinity")}} 之间，且不能为负数。该值的合法范围可以这样表示： \[0, +∞)。

## 示例

### 无效的

```js example-bad
"abc".repeat(-1); // RangeError
```

### 有效的

```js example-good
"abc".repeat(0); // ''
"abc".repeat(1); // 'abc'
"abc".repeat(2); // 'abcabc'
"abc".repeat(3.5); // 'abcabcabc' (count will be converted to integer)
```

## See also

- {{jsxref("String.prototype.repeat()")}}

---
# Source: index.md
---
---
title: "SyntaxError: Unexpected token"
slug: Web/JavaScript/Reference/Errors/Unexpected_token
---

JavaScript 异常“unexpected token”会在解析器在给定位置没有识别到它可以理解的标记（而无法理解程序的结构）时发生。这可能只是一个简单的拼写错误。

## 信息

```plain
SyntaxError: Unexpected token ';' (V8-based)
SyntaxError: Unexpected identifier 'x' (V8-based)
SyntaxError: Unexpected number (V8-based)
SyntaxError: Unexpected string (V8-based)
SyntaxError: Unexpected regular expression (V8-based)
SyntaxError: Unexpected template string (V8-based)
SyntaxError: unexpected token: identifier (Firefox)
SyntaxError: expected expression, got "x" (Firefox)
SyntaxError: expected property name, got "x" (Firefox)
SyntaxError: expected target, got "x" (Firefox)
SyntaxError: expected meta, got "x" (Firefox)
SyntaxError: expected rest argument name, got "x" (Firefox)
SyntaxError: expected closing parenthesis, got "x" (Firefox)
```

## 错误类型

{{jsxref("SyntaxError")}}

## 哪里出错了？

期望获得一个特定的语法结构，但得到了其他的。可能只是一个简单的错字。

## 示例

### 期望的表达式

例如，在调用函数时，不允许使用尾随逗号。有尾逗号的时候，JavaScript 会期望有另一个参数，可以是任何表达式。

```js-nolint example-bad
Math.max(2, 42,);
// SyntaxError: expected expression, got ')'
```

正确的方法是省略最后一个逗号或添加另一个参数：

```js example-good
Math.max(2, 42);
Math.max(2, 42, 13 + 37);
```

## 参见

- {{jsxref("SyntaxError")}}

---
# Source: index.md
---
---
title: "TypeError: invalid Array.prototype.sort argument"
slug: Web/JavaScript/Reference/Errors/Array_sort_argument
l10n:
  sourceCommit: d311eaee27eef2a590de711bb545b741044cb9b8
---

JavaScript 异常“invalid Array.prototype.sort argument”会在 {{jsxref("Array.prototype.sort()")}} 方法（以及其相关方法：{{jsxref("Array.prototype.toSorted()")}}、{{jsxref("TypedArray.prototype.sort()")}}、{{jsxref("TypedArray.prototype.toSorted()")}}）的参数既不是 {{jsxref("undefined")}} 也不是用于比较其操作数的函数时触发。

## 消息

```plain
TypeError: The comparison function must be either a function or undefined（基于 V8）

TypeError: invalid Array.prototype.sort argument (Firefox)
TypeError: non-function passed to Array.prototype.toSorted (Firefox)
TypeError: invalid %TypedArray%.prototype.sort argument (Firefox)

TypeError: Array.prototype.sort requires the comparator argument to be a function or undefined (Safari)
TypeError: Array.prototype.toSorted requires the comparator argument to be a function or undefined (Safari)
TypeError: TypedArray.prototype.sort requires the comparator argument to be a function or undefined (Safari)
TypeError: TypedArray.prototype.toSorted requires the comparator argument to be a function or undefined (Safari)
```

## 错误类型

{{jsxref("TypeError")}}

## 什么地方出错了？

{{jsxref("Array.prototype.sort()")}} 方法（以及其相关方法：{{jsxref("Array.prototype.toSorted()")}}、{{jsxref("TypedArray.prototype.sort()")}}、{{jsxref("TypedArray.prototype.toSorted()")}}）的参数应为 {{jsxref("undefined")}} 或用于比较其操作数的函数。

## 示例

### 无效示例

```js example-bad
[1, 3, 2].sort(5); // TypeError
students.toSorted("name"); // TypeError
```

### 有效示例

```js example-good
[1, 3, 2].sort(); // [1, 2, 3]
[1, 3, 2].sort((a, b) => a - b); // [1, 2, 3]
students.toSorted((a, b) => a.name.localeCompare(b.name));
```

## 参见

- {{jsxref("Array.prototype.sort()")}}
- {{jsxref("Array.prototype.toSorted()")}}
- {{jsxref("TypedArray.prototype.sort()")}}
- {{jsxref("TypedArray.prototype.toSorted()")}}

---
# Source: index.md
---
---
title: "RangeError: BigInt division by zero"
slug: Web/JavaScript/Reference/Errors/BigInt_division_by_zero
l10n:
  sourceCommit: c6f0f106b9083984dbf597678def6561729bb459
---

当一个 {{jsxref("BigInt")}} 被 `0n` 除时，会产生 JavaScript 异常“BigInt division by zero”。

## 错误信息

```plain
RangeError: Division by zero (V8-based)
RangeError: BigInt division by zero (Firefox)
RangeError: 0 is an invalid divisor value (Safari)
```

## 错误类型

{{jsxref("RangeError")}}

## 哪里出错了？

当使用[除法](/zh-CN/docs/Web/JavaScript/Reference/Operators/Division)或者[取余](/zh-CN/docs/Web/JavaScript/Reference/Operators/Remainder)运算符时，如果除数为 `0n` 则会触发该错误。在 {{jsxref("Number")}} 运算中，除以 `0n` 会得到 [`Infinity`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/Infinity)，但在 BigInt 中不存在“Infinity”这一值，因此会抛出错误。在使用除法前，请先检查除数是否为 `0n`。

## 示例

### 被 0n 除

```js example-bad
const a = 1n;
const b = 0n;
const quotient = a / b;
// RangeError: BigInt division by zero
```

相反，应首先检查除数是否为 `0n`，并给出更友好的提示或者使用其他值，例如 `Infinity` 或 `undefined`。

```js example-good
const a = 1n;
const b = 0n;
const quotient = b === 0n ? undefined : a / b;
```

## 参见

- [`BigInt`](/zh-CN/docs/Web/JavaScript/Reference/Global_Objects/BigInt)
- [除法（`/`）](/zh-CN/docs/Web/JavaScript/Reference/Operators/Division)
- [取余（`%`）](/zh-CN/docs/Web/JavaScript/Reference/Operators/Remainder)

---
# Source: index.md
---
---
title: 'TypeError: can''t redefine non-configurable property "x"'
slug: Web/JavaScript/Reference/Errors/Cant_redefine_property
---

## 错误提示

```plain
TypeError: can't redefine non-configurable property "x" (Firefox)
TypeError: Cannot redefine property: "x" (Chrome)
```

## 错误类型

{{jsxref("TypeError")}}

## 哪里出错了？

这种错误的起因在于试图给对象重新定义一个属性，但是该属性是[不可配置的](/zh-CN/docs/Web/JavaScript/Guide/Data_structures#属性)。 `configurable` 特性控制着该属性是否可以从对象中删除，以及它的各个特性（除 writable 之外）是否可以修改。通常使用[对象初始化语句](/zh-CN/docs/Web/JavaScript/Reference/Operators/Object_initializer)定义的对象属性是可配置的。而使用 {{jsxref("Object.defineProperty()")}} 定义的属性则默认不可配置。

## 示例

### 使用 object.defineProperty 创建的不可配置属性

在使用 {{jsxref("Object.defineProperty()")}} 创建属性的时候，如果没有明确将其设定为可配置的，那么创建出来的属性就是不可配置的。

```js example-bad
var obj = Object.create({});
Object.defineProperty(obj, "foo", { value: "bar" });

Object.defineProperty(obj, "foo", { value: "baz" });
// TypeError: can't redefine non-configurable property "foo"
```

如果想要稍后重新定义的话，那么需要将 "foo" 属性设置为可配置的。

```js example-good
var obj = Object.create({});
Object.defineProperty(obj, "foo", { value: "bar", configurable: true });
Object.defineProperty(obj, "foo", { value: "baz", configurable: true });
```

## 参见

- [\[\[Configurable\]\]](/zh-CN/docs/Web/JavaScript/Guide/Data_structures#属性)
- {{jsxref("Object.defineProperty()")}}

---
# Source: index.md
---
---
title: "SyntaxError: illegal character"
slug: Web/JavaScript/Reference/Errors/Illegal_character
---

## 错误提示

```plain
SyntaxError: illegal character (Firefox)
SyntaxError: Invalid or unexpected token (Chrome)
```

## 错误类型

{{jsxref("SyntaxError")}}

## 哪里出错了？

在代码中有非法的或者不期望出现的标记符号出现在不该出现的位置。请使用支持语法高亮功能的编辑器仔细检查你的代码，看看是否存在张冠李戴的情况，比如减号 (`-`) 与连接符 (`–`) ，或者是英文双引号 (`"`) 与中文双引号 (`“`)。

## 示例

### 错配字符

一些字符看起来会很相像，但是会导致于语法解析器解析代码失败。

```js example-bad
“This looks like a string”;
// SyntaxError: illegal character

42 – 13;
// SyntaxError: illegal character
```

下面这样是可以正常运行的：

```js example-good
"This is actually a string";

42 - 13;
```

### 遗漏的字符

很容易就会在这里或那里遗漏一些字符。

```js example-bad
var colors = ['#000', #333', '#666'];
// SyntaxError: illegal character
```

把遗漏的引号给 '#333' 添加上。

```js example-good
var colors = ["#000", "#333", "#666"];
```

### 隐藏字符

当从外部复制粘贴代码的时候，有可能就有非法的隐藏字符的存在，需要引起注意！

```js example-bad
var foo = 'bar';​
// SyntaxError: illegal character
```

当使用文本编辑器如 VIM 进行探测的时候，可以发现这里存在一个零宽空格 [(ZWSP) (U+200B)](https://en.wikipedia.org/wiki/Zero-width_space)。

```js
var foo = 'bar';​<200b>
```

## 相关内容

- [Lexical grammar](/zh-CN/docs/Web/JavaScript/Reference/Lexical_grammar)

---
# Source: index.md
---
---
title: JavaScript 错误参考
slug: Web/JavaScript/Reference/Errors
---

下面列出了 JavaScript 抛出的错误。这些错误是有用的调试帮助，但报告的问题并不总是十分明了。下面的页面提供有关这些错误的详细信息。每个错误都是基于 {{jsxref("Error")}} 的对象，并且具有名称和消息。

Web 控制台中显示的错误可能包含指向下面相应页面的链接，以帮助你快速理解代码中的问题。

## 错误列表

在此列表中，每个页面按名称（错误类型）和信息（更详细的容易理解的错误信息）列出。总之，这两者提供了理解和解决错误的线索。有关更多信息，请按照以下链接！

{{ListSubPages("/zh-CN/docs/Web/JavaScript/Reference/Errors")}}

---
# Source: index.md
---
---
title: 'TypeError: setting getter-only property "x"'
slug: Web/JavaScript/Reference/Errors/Getter_only
---

## 错误提示

```plain
TypeError: setting getter-only property "x" (Firefox)
TypeError: Cannot set property "prop" of #<Object> which has only a getter (Chrome)
```

## 错误类型

仅在[严格模式](/zh-CN/docs/Web/JavaScript/Reference/Strict_mode)下报 {{jsxref("TypeError")}} 错误。

## 哪里出错了？

该错误提示出现于试图给一个仅仅设置了 [getter](/zh-CN/docs/Web/JavaScript/Reference/Functions/get) 特性的属性赋新值的时候。在非严格模式下会被静默忽略，而在[严格模式](/zh-CN/docs/Web/JavaScript/Reference/Strict_mode)下会报 {{jsxref("TypeError")}} 错误。

## 示例

下面的例子展示了如何为一个属性设置 getter 特性。由于没有设置 [setter](/zh-CN/docs/Web/JavaScript/Reference/Functions/set) 特性，所以在试图将 temperature 属性值设置为 30 的时候会报 TypeError 的错误。相关细节信息可以参考 {{jsxref("Object.defineProperty()")}} 页面。

```js example-bad
"use strict";

function Archiver() {
  var temperature = null;
  Object.defineProperty(this, "temperature", {
    get: function () {
      console.log("get!");
      return temperature;
    },
  });
}

var arc = new Archiver();
arc.temperature; // 'get!'

arc.temperature = 30;
// TypeError: setting getter-only property "temperature"
```

至于修复问题的方法，可以将第 16 行的代码移除，因为它试图为 temperature 属性赋值，或者是为它添加一个 [setter](/zh-CN/docs/Web/JavaScript/Reference/Functions/set) 特性，就像下面这样：

```js example-good
"use strict";

function Archiver() {
  var temperature = null;
  var archive = [];

  Object.defineProperty(this, "temperature", {
    get: function () {
      console.log("get!");
      return temperature;
    },
    set: function (value) {
      temperature = value;
      archive.push({ val: temperature });
    },
  });

  this.getArchive = function () {
    return archive;
  };
}

var arc = new Archiver();
arc.temperature; // 'get!'
arc.temperature = 11;
arc.temperature = 13;
arc.getArchive(); // [{ val: 11 }, { val: 13 }]
```

## 相关内容

- {{jsxref("Object.defineProperty()")}}
- {{jsxref("Object.defineProperties()")}}

