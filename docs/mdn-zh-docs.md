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

---
# Source: CODE_OF_CONDUCT.md
---
# Community Participation Guidelines

This repository is governed by Mozilla's code of conduct and etiquette guidelines.
For more details, please read the
[Mozilla Community Participation Guidelines](https://www.mozilla.org/about/governance/policies/participation/).

## How to Report

For more information on how to report violations of the Community Participation Guidelines, please read our [How to Report](https://www.mozilla.org/about/governance/policies/participation/reporting/) page.

---
# Source: glossary.md
---
# 简体中文 web 术语翻译对照表

## 特定领域术语

### API

| 英文词汇    | 翻译     | 备注                                              | 引用来源                                                                     |
| ----------- | -------- | ------------------------------------------------- | ---------------------------------------------------------------------------- |
| light DOM   | 常规 DOM | 与影子 DOM 相对                                   | 同 shadow DOM                                                                |
| shadow DOM  | 影子 DOM | DOM 节点的附属树，在常规 DOM 中不可见（web 组件） | https://github.com/mdn/translated-content/pull/13432#issuecomment-1575018754 |
| shadow host | 影子宿主 | web 组件的宿主元素                                | 同 shadow DOM                                                                |
| shadow tree | 影子树   | 隐藏的 DOM 子树                                   | 同 shadow DOM                                                                |

### CSS

| 英文词汇         | 翻译    | 备注                     | 引用来源                                               |
| ---------------- | ------- | ------------------------ | ------------------------------------------------------ |
| block            | 区块    | 用于表示布局、书写模式等 | https://github.com/mdn/translated-content/issues/12632 |
| block direction  | 块向    |                          | 同 `block`                                             |
| block end/start  | 块末/首 |                          | 同 `block`                                             |
| block-level      | 块级    |                          | 同 `block`                                             |
| inline           | 行内    | 用于表示布局、书写模式等 | https://github.com/mdn/translated-content/issues/12632 |
| inline direction | 行向    |                          | 同 `inline`                                            |
| inline end/start | 行末/首 |                          | 同 `inline`                                            |
| inline-level     | 行级    |                          | 同 `inline`                                            |

### HTML

| 英文词汇        | 翻译     | 备注 | 引用来源                                                                    |
| --------------- | -------- | ---- | --------------------------------------------------------------------------- |
| light dismiss   | 轻触关闭 |      | https://github.com/mdn/translated-content/pull/13609#discussion_r1222377850 |
| Living Standard | 动态标准 |      | https://github.com/mdn/translated-content/pull/13406#discussion_r1206197135 |

### HTTP

| 英文词汇      | 翻译         | 备注                                                                                 | 引用来源                                                                    |
| ------------- | ------------ | ------------------------------------------------------------------------------------ | --------------------------------------------------------------------------- |
| cache busting | 缓存破坏     | 通过修改引用资源的文件名，强制浏览器重新下载新文件。实际使用可译作“（使）缓存失效”。 | https://github.com/mdn/translated-content/pull/18335#discussion_r1508540582 |
| CORS          | 跨源资源共享 | 使用“域”并不准确，来源包括协议、域名和端口。                                         | https://github.com/mdn/translated-content/pull/3096#issuecomment-1114015297 |
| cross-origin  | 跨源         |                                                                                      | 同 `CORS`                                                                   |
| Header        | 标头         | HTTP 消息中的附加信息。                                                              | 来自 Google Chrome 控制台                                                   |

### JavaScript

| 英文词汇           | 翻译                   | 备注                                                                                     | 引用来源                                                                    |
| ------------------ | ---------------------- | ---------------------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| bare module        | 裸模块                 | Vite.js 官方将其翻译为“裸模块”，其意为“没有任何路径的模块”。                             | https://github.com/mdn/translated-content/pull/12852#discussion_r1174339277 |
| brand check        | 特定类型检查           | 通过一段代码来对特定的数据类型进行检查。                                                 | https://github.com/mdn/translated-content/pull/13381#discussion_r1205437483 |
| constructor        | 构造函数               |                                                                                          | https://github.com/mdn/translated-content/issues/18211                      |
| exotic object      | 特异对象               |                                                                                          |                                                                             |
| handler            | 处理器                 |                                                                                          | https://github.com/mdn/translated-content/issues/18211                      |
| interface          | 接口                   |                                                                                          | https://zh.wikipedia.org/wiki/介面_(資訊科技)                               |
| normative optional | 可选标准               |                                                                                          | https://github.com/mdn/translated-content/pull/13627#discussion_r1224014687 |
| primitive          | 原始值/类型            | 基本类型包括对象，而原始类型不包括对象。                                                 | https://github.com/mdn/translated-content/pull/14040#discussion_r1276966303 |
| unscopable         | 不可绑定作用域（属性） |                                                                                          | https://github.com/mdn/translated-content/pull/12793#discussion_r1170694183 |
| well-known symbol  | 内置通用符号           |                                                                                          | https://github.com/mdn/translated-content/pull/10338#discussion_r1036997921 |
| tree shake         | 摇树优化               | 入口文件虽然依赖了某个模块，但实际只使用其中的某些功能，通过该优化可以删除未使用的代码。 | https://github.com/mdn/translated-content/pull/18335#discussion_r1505225794 |

## 标题/表格

| 英文词汇               | 翻译         | 备注               | 引用来源                                                                     |
| ---------------------- | ------------ | ------------------ | ---------------------------------------------------------------------------- |
| Accessibility concerns | 无障碍考虑   |                    | https://github.com/mdn/translated-content/issues/11456                       |
| Active learning        | 动手练习     |                    | https://github.com/mdn/translated-content/pull/12696#discussion_r1164859935  |
| Associated interfaces  | 相关接口     |                    |                                                                              |
| Associated roles       | 相关角色     |                    |                                                                              |
| Browser compatibility  | 浏览器兼容性 |                    |                                                                              |
| Conclusion             | 总结         |                    | https://github.com/mdn/translated-content/pull/13329#discussion_r1199677894  |
| Demo                   | 演示         | 交互示例的标题     |                                                                              |
| Examples               | 示例         |                    |                                                                              |
| Exceptions             | 异常         |                    |                                                                              |
| Expected output        | 期望输出     | 交互示例的文字提示 |                                                                              |
| Formal Definition      | 形式定义     |                    | https://zh.wikipedia.org/zh-cn/形式文法                                      |
| Formal syntax          | 形式语法     |                    | https://zh.wikipedia.org/zh-cn/形式文法                                      |
| Learning outcomes      | 学习成果     | 在学习区表格中使用 |                                                                              |
| Objective              | 目标         | 在学习区表格中使用 |                                                                              |
| Parameters             | 参数         |                    |                                                                              |
| Prerequisites          | 前提         | 在学习区表格中使用 |                                                                              |
| See also               | 参见         |                    |                                                                              |
| Specifications         | 规范         |                    |                                                                              |
| Technical summary      | 技术概要     |                    | https://github.com/mdn/translated-content/issues/11456                       |
| Test your skills       | 技能测试     |                    |                                                                              |
| Usage context          | 使用上下文   |                    | https://github.com/mdn/translated-content/pull/23257#issuecomment-2309852450 |
| Usage notes            | 使用说明     |                    | https://github.com/mdn/translated-content/pull/12600#discussion_r1161045585  |

## 通用术语

| 英文词汇   | 翻译 | 备注                     | 引用来源                                                                    |
| ---------- | ---- | ------------------------ | --------------------------------------------------------------------------- |
| color stop | 色标 | 标记某点的颜色，用于渐变 | https://github.com/mdn/translated-content/pull/13725#discussion_r1230347134 |
| repository | 仓库 | 用于存储代码的“仓库”。   | https://github.com/progit/progit2-zh/issues/98                              |

---
# Source: translation-guide.md
---
# 针对 MDN 文档的本地化指南

本文是针对简体中文（zh-CN）文档的翻译指南。如果你所使用的语言尚未有翻译指南，而你又希望新建的话，欢迎你联系[我们负责该语言的翻译团队](https://github.com/mdn/translated-content/blob/main/PEERS_GUIDELINES.md#review-teams)。

同样地，如果你对本文的指南有任何改进的建议，请提出问题（issue）或发起 PR。我们对此表示欢迎。下面进入简体中文翻译指南的正文部分。

> 若你对 MDN 上使用的 Markdown 格式不熟悉，请参阅[如何使用 markdown 来撰写文档][]。

## 元数据

每个文档的开头都会有元数据，但在翻译本地化文档时，我们不需要将上游文档中的所有元数据字段都复制到本地化文档中。对于 `page-type`、`browser-compat` 和 `spec-urls` 等元数据被用于站点管理和自动化数据处理，本地化文档中无需包含它们。此外，出于追踪文档同步情况的目的，我们在基本的元数据类别的基础上引入了 `l10n.sourceCommit`，用于记录对应英文文档的最新提交。本地化文档中应该使用的元数据说明如下：

- `title`（必须）：为文档的大标题
- `short-title`（可选）：为显示在侧边栏和面包屑中的短标题，若本地化文档采用的短标题与英文文档相同，则无需添加该元数据
- `slug`（必须）：为与网页 URL 相关的元数据（URL path 部分的规则为：`/<locale>/docs/<slug>`），请与对应的英文文档保持一致
- `l10n.sourceCommit`（可选）：为对应英文文档的最新提交的 SHA 值，请在完整同步英文文档翻译后更新或添加该元数据

最终在简体中文文档中呈现的元数据如下所示：

```yaml
title: HTMLAnchorElement：hash 属性
slug: Web/API/HTMLAnchorElement/hash
l10n:
  sourceCommit: a3d9f61a8990ba7b53bda9748d1f26a9e9810b18
```

## 翻译标题和 ID

文档中的目录导航、与代码块相关联的运行实例等会使用到 HTML ID。而对于 Markdown 文档，其渲染得到的 HTML 文件的 ID 则与 Markdown 文档中的标题相对应（但这并不意味着两者相等，rari 平台对于半角空格、标点等有特殊处理）。

例如，对于标题：

```md
## Examples
```

在简体中文文档中的翻译应该是：

```md
## 示例
```

## 翻译示例代码块

对于英文的示例代码块，可以选择翻译其中的注释、字符串、输出结果等等，但不建议对变量、函数、方法等名称进行翻译。

一些示例代码块会有与之对应的“实例”（即对示例代码运行效果的实时展示）。这些实例是通过 `{{EmbedLiveSample}}` 等宏来实现的，因为在本地化文档中会翻译英文标题，请**注意一并修改运行实例宏的第一个参数为相对应的中文标题**（参见：[运行实例][]）。

## 站内链接翻译

在翻译文档时，请记得将 MDN 站内网页的链接中的语言替换为 `zh-CN`，以便读者能够访问与之对应的本地化文档。此外，对于站内链接，请只保留 URL 中的路径及其之后的部分（去除协议和域名）。

例如：

```md
If you are new to HTML, CSS, JavaScript, etc., try our [Learn web development](/en-US/docs/Learn_web_development) tutorials.
```

在翻译时，应该将 URL 路径开头的 `/en-US` 替换为 `/zh-CN`：

```md
如果你刚刚开始了解 HTML、CSS、JavaScript 等相关知识，你可以试着完成我们的[学习 Web 开发](/zh-CN/docs/Learn_web_development)。
```

还需特别注意路径后带有片段标识（fragment）的站内链接，请同步更新片段标识为本地化文档中指定标题的 ID（若不清楚标题和 ID 之间的转换规则，可以在浏览器的开发者工具中查找对应标题的 ID）。

例如，对于以下链接：

```md
Reference to [Live sample macros](/en-US/docs/MDN/Writing_guidelines/Page_structures/Live_samples#live_sample_macros).
```

请对应中文文档，更新其片段标识：

```md
参考：[运行实例宏](/zh-CN/docs/MDN/Writing_guidelines/Page_structures/Live_samples#运行实例宏)。
```

> 请注意，无论指向的本地化文档是否存在，都请让链接指向本地化文档。rari 平台可以在指向本地化文档的链接不存在的情况下，自动将其回落到对应英文版本的链接。

## 中文翻译的常见问题

为保证简体中文文档格式的一致性，翻译指南列出了部分规范。

### 标点符号

除了代码中使用的符号以及一些特殊情况外，请将英文（半角）符号替换成中文（大部分为全角）符号。

> 但请注意，请不要使用**全角数字**（特殊情况除外）。

示例如下：

- 正确：`我们可以学习 JavaScript——一种很酷的语言`
- 错误：`我们可以学习 JavaScript--一种很酷的语言`
- 正确：`以下示例是“可交互的”`
- 错误：`以下示例是"可交互的"`

另外，请注意并列的词语间应使用顿号而非逗号：

- 原文：`a, b, and c`
- 宜：`a、b 和 c`
- 不宜：`a，b，和 c`

#### 常见中/英文标点

<!-- markdownlint-disable search-replace -->

| 名称   | 中文 | 英文    |
| ------ | ---- | ------- |
| 括号   | （） | ()      |
| 冒号   | ：   | :       |
| 引号   | “”   | ""      |
| 破折号 | ——   | -- 、 — |

<!-- markdownlint-enable search-replace -->

简体中文标点符号参考资源：

- [GB/T 15834―2011 标点符号用法](<https://people.ubuntu.com/~happyaron/l10n/GB(T)15834-2011.html>)
- [维基百科：标点符号](https://zh.wikipedia.org/zh-cn/标点符号)

### 中文和拉丁语系文字间加空格

对于简体中文文档，请在中文和拉丁语系文字之间保留**一个空格**，但在拉丁语系文字和中文标点之间，则无需保留空格。

示例如下：

- 正确：`学习 Web 开发`
- 错误：`学习Web开发`
- 正确：`学习 JavaScript、HTML、CSS 等`
- 错误：`学习 JavaScript、 HTML、 CSS 等`
- 正确：`应用程序接口（API）`
- 错误：`应用程序接口（ API ）`

对于链接文字和非链接文字部分，同样适用此规则：

- 正确：`它指向一个[示例](#示例)`
- 错误：`它指向一个 [示例](#示例)`
- 正确：`指向 [MDN 开发者文档](https://developer.mozilla.org/)的链接`
- 错误：`指向[MDN开发者文档](https://developer.mozilla.org/)的链接`

请注意，数字与中文之间也请保留空格：

- 正确：`需 10 个小时完成`
- 错误：`需10个小时完成`

### 排版

英文文档中，对于较长的段落，会通过断行的形式截断，以方便维护文档。但在 Markdown 中，断行会引入空格，在简体中文翻译中，我们有如下约定：

- 在段落不是特别长的情况下（200 个字符以内），请不要断行。
- 若段落过长，也请在中文与拉丁语系文字、数字之间，或是句子末尾断行。

例如：

```md
This is an example.
We usually write a paragraph into multiple lines.
Like this.
```

而在中文文档中，应该使它们在同一行内：

```md
这是一个示例。我们不应该断行写这一段话。就像这样。
```

### 词语翻译

### 代名词

<!-- markdownlint-disable search-replace -->

我们无需将“you”翻译为“您”，在文档正文部分的翻译中，请统一使用“你”。

<!-- markdownlint-enable search-replace -->

### 复数形式

英文文档中，为了使语句的语法正确，会使用大量的复数形式。在中文翻译中，则无需保留这些复数的形式（未翻译的英文名词也同理）。

- 原文：`Application Programming Interfaces (APIs)`
- 宜：`应用程序接口（API）`
- 不宜：`应用程序接口（APIs）`
- 不宜：`应用程序接口们（APIs）`

### 术语表

我们在仓库中维护了一个[术语表](glossary.md)，旨在统一目前还未有明确中文翻译的术语。在翻译文档时，请尽量使用术语表中的术语，以保证文档的一致性。

> 如果术语表中缺少某些术语，或者你对其中的术语翻译有任何疑问，欢迎提出[议题](https://github.com/mdn/translated-content/issues/new/choose)或发起 PR。

### 常用标题

英文文档中使用了一些常见标题，为了保持简体中文文档的一致性，请在翻译时参考术语表中的[标题和表格的翻译](glossary.md#标题表格)。

[如何使用 markdown 来撰写文档]: https://developer.mozilla.org/zh-CN/docs/MDN/Writing_guidelines/Howto/Markdown_in_MDN
[运行实例]: https://developer.mozilla.org/zh-CN/docs/MDN/Writing_guidelines/Page_structures/Live_samples

---
# Source: README.md
---
# Bienvenido a la localización de MDN en español

Puedes comenzar en la siguiente [guía de contribución][]

## Pasos para configurar el entorno local

> Puedes ver: <https://youtu.be/pFeW0vUYbkg>

## Pasos para abrir un Pull Request

### Desde tu computadora

> Crear rama, hacer commit, crear pull request, esperar revisiones.
>
> - Acceder a GitHub: <https://github.com/login/>
> - Ir a <https://github.com/mdn/translated-content>
> - ![Screenshot 2022-03-01 at 17-13-20 mdn translated-content All translated MDN content in raw form](https://user-images.githubusercontent.com/13079269/156264660-afcba14a-14a0-4c66-9a33-c1e2ad41737b.png) hacer Fork al repositorio en nuestra cuenta de GitHub.
> - Clonar el repositorio de nuestra cuenta de GitHub `git clone git@github.com:TU_USUARIO/translated-content.git`
> - `cd translated-content` #Entrar al directorio
> - `git switch -c patch-error-on-123-issue` #Crear rama para trabajar
> - Hacer nuestros cambios
> - `git add files/es/archivo.md` #Agregamos los archivos modificados
> - `git rm files/es/archivo.html` #Removemos los archivos eliminados (si los hubiera)
> - `git commit -m "Corregido el error 123 [es]"` #Hacemos commit con una descripción de lo realizado y agregamos `[es]`
> - `git push -u origin patch-error-on-123-issue` #Subimos nuestra rama a nuestro repositorio
> - Ir a nuestro repositorio <https://github.com/TU_USUARIO/translated-content> y solicitar el Pull Request

A continuación puedes ver un ejemplo en video: <https://youtu.be/pFeW0vUYbkg>

## Pasos para traducir un documento

Ejemplificaremos el proceso a realizar cuando se desea traducir el contenido de una página.
Ejemplo:

Digamos que desea traducir el contenido de la página que se observa en esta dirección.
![image](https://user-images.githubusercontent.com/7331511/152851642-5dea4df9-f771-4323-bc13-b238dec511ef.png)

1. Buscar la [versión original (en inglés)](https://github.com/mdn/content/tree/main/files/en-us) del documento que desea traducir.
   Debería buscar en el repositorio [en inglés (mdn/content)](https://github.com/mdn/content) el archivo correspondiente al documento, en este caso la dirección sería [`files/en-us/web/javascript/reference/global_objects/array/index.md`](https://github.com/mdn/content/blob/main/files/en-us/web/javascript/reference/global_objects/array/index.md)

2. Buscar la [versión en español](https://github.com/mdn/translated-content/blob/main/files/es/) del [documento](https://github.com/mdn/translated-content/blob/main/files/es/web/javascript/reference/global_objects/array/index.html) que desea traducir. En este caso la dirección seria [`files/es/web/javascript/reference/global_objects/array/index.{html|md}`](https://github.com/mdn/translated-content/blob/main/files/es/web/javascript/reference/global_objects/array/index.html)

   > NOTA:
   >
   > - Si el archivo no existe, deberá crearlo en formato `Markdown` imitando la ruta que tiene la versión en inglés.
   > - Es posible que el archivo en la versión en español se encuentre en formato `HTML`, en cuyo caso tendrá que reemplazarlo por el formato `Markdown`.

3. Utilizar el texto y formato en inglés como guía para traducir al español.

## Arreglar "flaws" (defectos)

Al usar `npm start` en localhost para el repositorio `mdn/content`, es posible ver una previsualización en tu servidor local de los cambios que has hecho y como lucirán. Esto también es posible creando un PR, el bot se encargará de generar una "preview URL" donde puedes observar el mismo resultado. En ambas pantallas, podrás, en la parte superior del documento, mostrar los "flaws" que el motor indique, y que contendrá aquellos defectos detectados de manera automática para ser corregidos, y, en algunos casos, la corrección disponible con un clic, o una sugerencia.

## Convención en traducciones

La comunidad de español sugiere utilizar las siguientes convenciones al traducir el contenido.

| Término original                | Traducción                     |
| ------------------------------- | ------------------------------ |
| Event listener                  | Detector de eventos            |
| Event handler                   | Manejador de eventos           |
| See also                        | Véase también                  |
| Specifications                  | Especificaciones               |
| Browser compatibility           | Compatibilidad con navegadores |
| HTML Content o HTML             | HTML                           |
| JavaScript Content o JavaScript | JavaScript                     |
| Warning                         | Advertencia                    |
| Framework                       | Framework                      |

### Formatos especiales

| Inglés         | Español            |
| -------------- | ------------------ |
| `**Note:**`    | `**Nota:**`        |
| `**Warning:**` | `**Advertencia:**` |
| `**Callout:**` | `**Observación:**` |

## Formateo

| Expresión     | Como escribirlo |
| ------------- | --------------- |
| 2<sup>5</sup> | 2^5             |

Actualmente trabajando en: <https://github.com/mdn/translated-content/issues/8635>

## Charla con nosotros

Telegram: <https://t.me/+Dr6qKQCAepw4MjFj>

Matrix: <https://chat.mozilla.org/#/room/#mdn-l10n-es:mozilla.org>

MDN Discord, canal #spanish: <https://discord.gg/aZqEtMrbr7>

<details>
  <summary><h2>Enlaces relevantes</h2></summary>

Documentación por prioridad.
<https://developer.mozilla.org/en-US/docs/MDN/Contribute/Documentation_priorities>

Proyecto `ES` en GitHub
<https://github.com/mdn/translated-content/projects/7>

Telegram link
<https://t.me/+Dr6qKQCAepw4MjFj>

Matrix link
<https://chat.mozilla.org/#/room/!cIEBGoIHFpsXNeVUwp:mozilla.org>

Grupo en community
<https://community.mozilla.org/en/groups/mdn-localizacion-espanol/>

Los `tags` no se usan para las traducciones de la documentación, borremoslo.
<https://github.com/mdn/translated-content/pull/4058#discussion_r802298455>

Tutorial para crear el ambiente de desarrollo para MDN
<https://www.youtube.com/watch?v=pFeW0vUYbkg>

Guía de markdown
<https://developer.mozilla.org/en-US/docs/MDN/Contribute/Markdown_in_MDN>

</details>

Más información [aqui](https://github.com/mdn/translated-content/discussions/4029)

[guía de contribución]: https://developer.mozilla.org/es/docs/MDN/Contribute

---
# Source: orphaned_and_conflicting.md
---
# Orphaned and conflicting documents

In this guide, we will look at how to deal with the files in `files/<locale>/orphaned` and `files/<locale>/conflicting`. Ideally, those folders should be empty, but in practice, some regular maintenance is needed from each localization team and some more work might be needed if this has not been done since the MDN migration to GitHub.

## What they are

Yari relies on file structure/hierarchy being the same between `files/en-us/` from `mdn/content` and `files/<locale>/` from `mdn/translated-content`. However, from time to time, some differences occur and must be solved by a human maintainer. Such differences are pushed into `files/<locale>/orphaned` and `files/<locale>/conflicting` directories.

### Orphaned pages

When a page does not exists anymore in English (or didn't exist at all, like it was possible to have in Kuma) but exists in a given locale, it is moved to `files/<locale>/orphaned`. The locale team should then decide if this content should be deleted/redirected or migrated to another page.

In practice, deleting-redirecting per the `en-US` structure is enough (see below).

### Conflicting pages

When an English page is redirected/moved to a new location, but the target already exists in `<locale>`, the localized page is moved to `files/<locale>/conflicting`. Basically, a locale team member should decide which version take priority over the other.

## How they are generated

This "structure" synchronization between `mdn/content` and `mdn/translated-content` occurs daily with this GitHub Actions workflow <https://github.com/mdn/mdn-translated-content/blob/main/.github/workflows/sync-translated-content.yml> (the logic can be found at <https://github.com/mdn/rari/blob/main/crates/rari-tools/src/sync_translated_content.rs>)

Before #8378 (16th Sep. 2022), this synchronization automatically added commits (see [an example](https://github.com/mdn/translated-content/commit/81b40438ed59fc3d5990eae0d1eb333ad7b5dd27), or [another](https://github.com/mdn/translated-content/commit/51268ca7b9bdf3ead1c1775dee61bcc90445f0dc)). Now, a PR is created with the changes for each locale (see #9029, #9026).

## How to deal with them

The goal of this process is to have 0 files under `files/<locale>/conflicting` / `files/<locale>/orphaned`. In the following sections, we assume that you setup both `mdn/content` and `mdn/translated-content` repositories on your local machine.

### Deal with "first gen" files

If your locale already contains a `conflicting` or `orphaned` directory, it has been populated by earlier sync commits. For each page, you will need to decide a course of action. Afterwards, rinse and repeat for the other pages.

Depending on your team and on the directory you are processing, you may either go with a pull request dealing with only on page or with a PR for a small set of pages (e.g. processing the whole `conflicting/web/svg` directory at once if it contains 5-10 pages).

#### Dealing with orphaned pages

For an orphaned page, the generic approach consists of the following:

1. Identify the `mdn/content` commit for the deletion using:

   ```bash
   git log -n 1 -- files/en-us/slug/of/deleted/doc/index.md
   ```

   This will give you something like

   ```console
   commit d387c1fe9d861cf0578a5d05b29a47d3a1d5e986
   Author: John Doe <jdoe@example.com>
   Date:   Mon Sep 12 03:36:39 2022 -0400

   Remove Glossary/jQuery (#20569)
   ```

2. Check the corresponding PR to have a better understanding of the change (in the previous example, this is [#20569](https://github.com/mdn/content/pull/20569)).
3. Check if there is an active redirect for the corresponding page in English (see <https://github.com/mdn/content/blob/main/files/en-us/_redirects.txt>)
4. Depending on the presence of a redirect, use either

   ```bash
   npm run content delete <orphaned/slug/of/page> <locale> -- --redirect <other/slug>
   ```

   or

   ```bash
   npm run content delete <orphaned/slug/of/page> <locale>
   ```

#### Dealing with conflicting pages

A conflicting page might need more work as content may have been moved/rewritten on the target page as well and redirection might not suffice. That being written, dealing with a conflicting page usually involves:

1. Identify the `mdn/content` commit for the move using:

   ```bash
   git log -n 1 -- files/en-us/slug/of/redirected/doc/index.md
   ```

   This will give you something like

   ```console
   commit be2279c2425d7d3eabe5956bc920025b025bdc2c
   Author: John Doe <john.doe@example.com>
   Date:   Wed Sep 21 23:51:39 2022 -0400

    Merge "SAB planned changes" into the main page (#20863)
   ```

2. Check the corresponding PR to have a better understanding of the change (in the previous example, this is [#20863](https://github.com/mdn/content/pull/20863)).
3. Applying the same redirect as per `mdn/content` for the source page:

   ```bash
   npm run content delete <conflicting/slug/of/page> <locale> -- --redirect <other/slug>
   ```

4. Updating the target page to reflect the movement of content in English. You might need to reuse content from the "conflicting" page into the existing target page to follow the English evolution.

### Deal with generated PRs

With the automated PRs workflow, it is now easier to "catch" orphaned or conflicting pages before they fill the stack of pages to be removed in the repository.

The process stays the same as above (using `npm run content delete bla/bla locale -- --redirect foo/foo` most of the time). However, the changes should be made on the branch created by the bot rather than on a new PR (checkout the existing branch rather than creating your own on your fork).

Be careful though, if left opened, the PR will be force-pushed updated by the bot every 24h and your changes might be lost. Be sure to keep a local/forked branch with your changes or to review such changes swiftly within your team.

### "Nice to have's"

The following steps are not mandatory, but improve the quality of the end result:

1. Update any existing link to the previous slug of a page under `files/<locale>/` (will touch a larger number of files)
2. Update the existing target page so that it completely matches the current English state (might take a bit longer)

---
# Source: README.md
---
# Translation guidelines for MDN translated content

This document describes the general guidelines for translating MDN content, which apply to every locale.

For guidelines relating to specific locales, we have locale-specific docs in subdirectories:

- [Spanish guide / Guía en español](es/README.md)
- [Japanese translation guide / 日本語翻訳ガイド](ja/README.md)
- [Korean translation guide / 한국 번역 지침](ko/README.md)
- [Russian translation guide / Руководство по переводу на русский язык](ru/README.md)
- [Simplified Chinese Guide / 简体中文翻译指南](zh-cn/translation-guide.md)
- [Traditional Chinese Guide / 正體中文翻譯指南](zh-tw/translation-guide.md)

> [!NOTE]
> If you want to add a guide to document some specific guidelines for your locale and it does not already appear here, you are welcome to add one, or [talk to the locale teams](https://github.com/mdn/translated-content/blob/main/PEERS_GUIDELINES.md#review-teams) about it.

## Do not copy all front matter properties from English pages

In upstream content, pages will have many front matter properties, including `page-type` and `browser-compat`. However, these properties do not need to be copied to translated pages; Yari merges the front matter of the English and translated versions of a page. Localized documents should only have the following front matter properties:

- `title` - A long title for the page; to localize
- `short-title` - A short title for the page which appears in sidebars; also to localize
- `slug` - needs to match the original page's `slug`
- `l10n.sourceCommit` - The commit hash of the upstream commit the translation is synchronized with

This guideline is enforced by a linter.

## Do not partially translate a document

At the time of writing, there are numerous documents throughout the repository that are partially translated. The documents were created in the wiki era before this project transitioned to GitHub, where anyone could make changes to the pages without review. Partially translated pages are bad for numerous reasons:

- They provide a negative user experience if only part of the page is in their requested locale
- They produce a negative SEO score because of the above reason
- The upstream content may have changed, but contributors will likely continue working on the English content in that file

If you are translating a document, please follow through and translate the entire page. If you need assistance translating a section, please ask a member of your locale for help.

## Do not use machine translation

Using machine translation services can be helpful to discern the meaning of a word you may not know, and machine translations have greatly improved over the years. However, machines are not able to _localize_ content. They cannot discern complete context, and may over-translate or use different words for the same terms in different sentences. Do not use machine translations to localize content; only use them as a reference.

## Localizing code blocks

Many code blocks are present in MDN pages. We encourage the localization of code blocks, as long as you follow the following guidelines:

- Translate comments, strings and output representations
  - Translating variable and function names is not recommended, except in learn/
- Do not translate syntax (`await`, `console`, etc.) which would break the code
- Ensure that the code example is not completely rewritten, unless it is absolutely essential
  - If a code block must be rewritten to meet a locale's requirements, add a comment explaining why

Also, when considering translating examples, bear in mind that some examples will link to a live version or source code on a separate repo. You might also want to consider creating a translated version of the external code examples to link to from your translated page.

---
# Source: translation-guide.md
---
# 針對 MDN 翻譯內容的一般指導原則

本文是針對正體中文（zh-TW）地區的翻譯指南。如果你所在的地區尚未有文件指南，而你又想新建的話，歡迎你開始建立或聯絡[我們負責該地區的翻譯團隊](https://github.com/mdn/translated-content/blob/main/PEERS_GUIDELINES.md#review-teams)。

同樣的，如果你對一般指導原則有一些不錯的想法想要補充，不用客氣，去發起問題（issue）來跟我們談談吧。以下進入正體中文翻譯指導原則的主要內容。

## 翻譯標題 ID

基於自動產生文章內的導覽、識別程式碼區塊用於建立實際範例、以及其他的原因，我們的文章會使用到 HTML ID。而對於 Markdown 文件，其渲染得到的 HTML 文件的 ID 則與 Markdown 文件中的標題相對應（但這並不意味著兩者相同，rari 平台對於空格、半角標點等有特殊處理）。

> 對於 [Live Sample][] 等需要用到 HTML ID 的地方，可以透過查看網頁原始碼的方式確定標題對應的 ID。

例如：

```md
## Tutorials
```

在 `zh-TW` 地區的翻譯應該是

```md
## 教學
```

## 翻譯程式碼區塊

當翻譯程式碼片段時，針對註解、字串、輸出結果進行翻譯都是可以的，但不建議對變數、函數、方法等名稱進行中文翻譯。

然而，不要對實際的程式碼術語進行翻譯，好比語法。你要確保範例在翻譯後仍可正常執行。

當試圖翻譯範例時，請記得有些範例會連向實際的版本或獨立的原始碼倉庫。你可以考慮建立對應的翻譯版本，然後在翻譯頁面中連向這些經翻譯的外部程式碼。

## HTML 原始碼的換行

在某些文章的原始碼中，你可能會發現區塊等級元素中有無關緊要的換行，例如：

````md
The
**`HTMLCanvasElement.transferControlToOffscreen()`**
method transfers control to an {{domxref("OffscreenCanvas")}} object, either on the main
thread or on a worker.

```js
OffscreenCanvas HTMLCanvasElement.transferControlToOffscreen()
```
````

一般而言，我們並不會在原始碼中使用如此的換行，所以你可以選擇把它們移除，而且當你在進行新的翻譯時也不要把它們加進來。但毋須浪費太多時間移除這些多餘的換行，因為在最終呈現的結果上並不會有差異。

## 站內連結翻譯

在翻譯文章時，記得把 MDN 內部頁面連結中的語系轉換成 `/zh-TW`，以便讀者在點選連結時，能夠正確的跳轉到該主題的中文翻譯頁面。

例如：

```md
For example, consider the [JavaScript](/en-US/docs/Web/JavaScript) guide, which is structured as follows:
```

在翻譯時應該是（請注意 `/zh-TW` 替換了原本的 `/en-US`）

```md
以 [JavaScript](/zh-TW/docs/Web/JavaScript) 指南為例，它的結構如下：
```

## 中文翻譯的常見問題

基於台灣的島國文化受到外來文化的影響頗深，對中文掌握的程度也因人而異，中文輸入法又無統一規範等種種原因，在翻譯文章時難免發生不少錯誤。以下針對不同主題，整理相關常見的錯誤。

### 標點符號

錯誤使用中文標點是台灣在地化翻譯常見的問題之一，譯者往往不知道如何正確使用中文（全形）標點符號。

#### 中文標點符號

在翻譯文章時，應使用全形中文標點符號（除非在引述外文的文字中），例如：

- 正確：`雖然「Java」和「JavaScript」都是 Oracle 公司`
- 不正確：`雖然 "Java" 和 "JavaScript" 都是Oracle公司`
- 正確：`請前往 JavaScript——動態的用戶端指令。`
- 不正確：`請前往 JavaScript -動態的用戶端指令。`

當引述的內容為外文時，應保留其原有的標點符號：

- 正確：`我們將變數 myHeading 中 innerHTML 特性的值設為「Hello, world!」。`
- 不正確：`我們將變數 myHeading 中 innerHTML 特性的值設為「Hello，world！」。`

#### 常見錯誤

常見錯誤使用的標點符號（包含但不限於下列的例子）：

<!-- markdownlint-disable search-replace -->

| 名稱   | 正確     | 錯誤     |
| ------ | -------- | -------- |
| 夾注號 | （）     | ()       |
| 冒號   | ：       | :        |
| 引號   | 「『』」 | “” 、 "" |
| 破折號 | ——       | -- 、 —  |

<!-- markdownlint-enable search-replace -->

#### 如何輸入全形標點符號

在「微軟新注音」輸入法中，透過前導字元 <kbd>\`</kbd>（數字 1 左邊的按鍵），或使用 <kbd>shift</kbd> + <kbd>space</kbd> 切換全形模式，這樣可以快速輸入全形中文。其他輸入法也應有相應的機制，請自行探索。

#### 中文標點符號參考資源

- [教育部《重訂標點符號手冊》修訂版](https://language.moe.gov.tw/001/upload/files/site_content/m0001/hau/haushou.htm)。
- [維基百科標點符號](https://zh.wikipedia.org/wiki/标点符号)。

### 中文及拉丁語系文字間不加修飾空白

中文網路界，有一派習慣是在中文字與半形英數、符號字元間，手動加入半形空格，以便視覺上美觀（如[盤古之白](https://github.com/vinta/pangu.js/blob/master/README.md)倡議）；但也有人主張中英文間不應手動加入空白，而應以系統來調整顯示樣式（如 [W3C 中文排版需求草案](https://www.w3.org/TR/clreq/#mixed_text_composition_in_horizontal_writing_mode)、[Fred Jame](https://fredjame.wordpress.com/2014/09/14/中英文之間為什麼要有空格我問/)、及[中文維基百科](https://zh.wikipedia.org/wiki/Wikipedia_talk:格式手册/存档5#提議修改格式手冊中的空格章節)之討論）。

~~經 MDN 在地化團隊[討論](https://t.me/c/1099275693/2056)，著眼於簡化格式規範，並考量作業系統與瀏覽器層級中英文混排的 kerning 實作將越來越良好（如 iOS 13、macOS 10.15 ），MDN 上「不」在中英文間手動插入空白字元。~~

基於多數應用程式都並未很對中西文混排進行最佳化處理、不手動修飾仍對閱讀上造成一定的障礙、`zh-CN` 也偏向於手動修正等理由，重新採取須手動修飾的原則。請貢獻者盡可能確保格式的正確，審核人員也會協助你找出遺漏的部分。以下手動增加修飾空白的範例：

- 正確：`使用 Git 作為版本控制。`
- 不正確：`使用Git作為版本控制。`

全形標點符號與拉丁字符間也要加空白

- 正確：`JavaScript 是一個成熟的動態程式語言，應用於 HTML 文件（document）上時`
- 不正確：`JavaScript是一個成熟的動態程式語言，應用於HTML文件（document）上時`

我們也展望 MDN 未來能透過技術上的處理（如[漢字標準格式](https://hanzi.pro/manual/)或 [pangu.js](https://github.com/vinta/pangu.js)），讓中英文混排的文件，在尚未最佳化的系統上也能美觀顯示。

### 常見標題或詞彙

原文中經常出現某些常見的標題或用詞，為了避免因未翻譯上的差異導致讀者產生疑惑，請參考下表進行翻譯：

| 原文                  | 翻譯         |
| --------------------- | ------------ |
| Browser compatibility | 瀏覽器相容性 |
| Examples              | 範例         |
| Formal definition     | 形式定義     |
| Formal syntax         | 形式語法     |
| See also              | 參見         |
| Specifications        | 規範         |

### 慣用語及術語

因地緣及文化等因素，加上中國人口與市場的蓬勃發展，簡體中文資訊量龐大且強勢，台灣譯者容易受到中國慣用語的影響而不自知。

以下列舉部分常見的原文、台灣慣用翻譯、中國慣用翻譯做為參考：

| 英文                 | 台灣慣用翻譯                               | 中國慣用翻譯 |
| -------------------- | ------------------------------------------ | ------------ |
| video                | 視訊                                       | 視頻         |
| audio                | 音訊                                       | 音頻         |
| component            | 元件                                       | 組件         |
| custom               | 自訂                                       | 自定義       |
| support              | 支援（實際行動的，意圖或精神上的則為支持） | 支持         |
| network              | 網路                                       | 網絡         |
| code                 | 程式碼                                     | 代碼         |
| source code          | 原始碼                                     | 源代碼       |
| programming          | 程式設計／程設                             | 編程         |
| config/configuration | 組態                                       | 配置         |
| (browser) extension  | 套件／擴充功能                             | 插件         |
| plugin               | 外掛                                       | 插件         |
| (file) extension     | 副檔名                                     | 擴展名       |
| array                | 陣列                                       | 數組         |
| object               | 物件                                       | 對象         |

當台灣譯者在翻譯時，應盡可能地使用台灣的慣用翻譯或詞彙。若碰到不確定的情況，可以參考下列的資源。由於機器翻譯多未考慮在地語彙，請不要仰賴線上翻譯服務（譬如 Google 翻譯）。

### 台灣慣用詞彙參考資源

專業術語可參考相關權威單位，例如：

- [國家教育研究院 雙語詞彙、學術名詞暨辭書資訊網](https://terms.naer.edu.tw/)
- [微軟語言入口網站](https://www.microsoft.com/zh-tw/language/)

特定領域術語可參考當地該領域專家的相關著作，例如：

- JavaScript 可參考林信良。
- CSS 可參考李建杭。
- Git 可參考高見龍。

其他日常用語

- [行政院陸委會正簡體對照表](https://www.mac.gov.tw/Content_List.aspx?n=87AE0F44904650AB)
- [政治大學正簡體對照表](https://nccur.lib.nccu.edu.tw/bitstream/140.119/35617/12/031112.pdf)
- [陸委會大陸資訊及研究中心](https://www.mac.gov.tw/MAIRC/cp.aspx?n=78790EF4BAE05CCF)

### 中文相關文法

中文和英文分屬兩種不同的語系，彼此之間並不一定存在對方語文中的某些概念。但在國際化的今天，中文讀者往往也容易被英文所影響。

以下是一些在翻譯中文時常碰到的問題，包含但不限於中英文之間的差異。

#### 語態

英文有主動語態（active voice）及被動語態（passive voice）。中文雖然也具有主被動語態的觀念，但以主動語態為主。因此在翻譯時，應盡可能的使用主動語態，以避免造成閱讀與理解上的困難，最典型的就是「被」的濫用以及照搬英文的倒裝句。

- 原文：`Publishing a website is a complex topic because there are many ways to go about it.`
- 宜：`因為有太多方法能夠發佈網站，所以這不是一個幾句話就能說完的課題。`
- 不宜：`發佈網站並不是一個幾句話就能說得完的課題，主要是因為有太多方法能夠發佈網站。`

#### 敬語

英文的代名詞並無敬語的觀念，然而某些中文譯者，往往習慣性地在翻譯時把代名詞譯為敬語，這是不需要的。文件敘述的語氣，毋須刻意展現謙卑的態度，使用貼近口語的說法即可，不需要太過正式（嚴肅）。

- 原文：`generally, you have to connect to your web server using details provided by your hosting company`
- 宜：`一般來說，你可以用你的公司提供的資訊登入網頁伺服器。`
- 不宜：`一般來說，您可以用您的公司提供的資訊登入網頁伺服器。`

#### 代名詞

英文文章的敘述中，常會充斥大量的第二或第三人代名詞。但在翻譯為中文時，這種過度出現的代名詞，實際上會使得閱讀變得不通順。適度地減少代名詞的使用，能讓中文的閱讀更加順暢。

- 原文：`After you have finished your instructions, follow the numbered list with a brief closing summary.`
- 宜：`在完成操作指南後，接續著有序清單給予簡略結語。`
- 不宜：`在你完成你的操作指南之後，接續著有序清單給予簡略結語。`

#### 複數形式

相對英文而言，中文並沒有複數（名詞）的概念，因此在翻譯文章時也請去除原文中複數的形式。

- 原文：`Browser Application Programming Interfaces (APIs)`
- 宜：`瀏覽器應用程式介面（API）`
- 不宜：`瀏覽器應用程式介面（APIs）`
- 不宜：`瀏覽器應用程式介面們（APIs）`

## Mozilla 正體中文在地化規範

Mozilla 各專案一致性的在地化規範與翻譯原則，請參閱 [Mozilla L10n Style Guide](https://mozilla-l10n.github.io/styleguides/zh-TW/)。

## 結語

我們很難對翻譯這項工作訂定絕對的準則，語言的正確使用與否也難有絕對的標準。因此，在面對上述的指導原則及問題時，希望你不會感到太大的壓力，如果你有任何疑問，請隨時聯絡在地化翻譯團隊，向我們提出你的問題。

儘管嘗試送出你的翻譯吧，審核人員會協助你進行除錯，找出你可能大意的地方。一旦問題都解決了，他們就會合併你的翻譯內容。

如果你還沒有做好直接貢獻翻譯的準備也沒有關係，你可以嘗試協助我們找出 MDN 上有瑕疵的翻譯，並透過問題（issue）回報給我們。又或是找到那些不太難且尚未解決的問題，並嘗試修正這些問題。這是相對簡單的方式邁出翻譯貢獻的第一步。我們衷心期待你的貢獻。

[Live Sample]: https://developer.mozilla.org/docs/MDN/Writing_guidelines/Page_structures/Live_samples

---
# Source: github-actions-guide.md
---
# Github Actions 안내서

발생하는 모든 오류는 기본적으로 Github Actions에서 발생하는 로그를 참고하여, 기여자가 직접 수정해야 합니다. 해결에 어려움이 있다면 주저말고 배정된 리뷰어 분을 멘션해주세요.

다음은 염두에 두어야 할 몇 가지 지침입니다.

## Redirects Files

보통의 경우 파일 삭제시 [\_redirects.txt](https://github.com/mdn/translated-content/blob/main/files/ko/_redirects.txt)를 갱신해주어야 합니다.

[yari](https://github.com/mdn/yari)에서 아래 명령어를 통해 [translated-content](https://github.com/mdn/translated-content)의 [\_redirects.txt](https://github.com/mdn/translated-content/blob/main/files/ko/_redirects.txt) 파일을 검증 및 갱신할 수 있습니다.

```bash
npm run content validate-redirects ko
npm run content fix-redirects ko
```

혹은 [content repo](https://github.com/mdn/content)에서 아래 명령어를 통해 검증 및 갱신할 수 있습니다.

```bash
npm run content validate-redirects ko
npm run content fix-redirects ko
```

## Markdown Lint

### 한국 가이드 파일들에 대한 링크 규칙 (해당되는 파일 경로: `/docs/ko/guides/*.*`)

/files/ko 폴더 하위에 있는 마크다운 파일들은 오류가 발생하지 않지만, /docs/ko/guides 폴더 하위에 있는 안내서와 관련된 파일들은 린트 오류가 발생하여 다음 방법으로 해결 할 수 있습니다. [참고](https://github.com/mdn/translated-content/pull/11031#discussion_r1066091908)

Markdown Lint 규칙을 우회하기위해 `https://developer.mozilla.org/`로 시작하는 링크들은 맨 아래로 이동해서 작성합니다.

예를들어, `[CSS 기본 박스 모델 입문](https://developer.mozilla.org/ko/docs/Web/CSS/CSS_Box_Model/Introduction_to_the_CSS_box_model)`에서 `[CSS 기본 박스 모델 입문]` 부분은 `[CSS 기본 박스 모델 입문][]`로 작성하고,

```md
| Padding | 안쪽 여백(패딩) | | [CSS 기본 박스 모델 입문][] |
```

`(https://developer.mozilla.org/ko/docs/Web/CSS/CSS_Box_Model/Introduction_to_the_CSS_box_model)`부분은 페이지 가장 하단에 아래와 같이 작성해야합니다.

```md
[CSS 기본 박스 모델 입문]: https://developer.mozilla.org/ko/docs/Web/CSS/CSS_Box_Model/Introduction_to_the_CSS_box_model
```

---
# Source: organizer-guide.md
---
# MDN yari-content-ko 팀에 대한 일반 안내서

## yari-content-ko 구성원 변경에 대한 일반 안내서

1. 구성원 변경 요청.
2. [PEERS_GUIDELINES.md](https://github.com/mdn/translated-content/blob/main/PEERS_GUIDELINES.md) 페이지의 `Korea (ko) content — the @ko-content team, which consists of:` 수정.
3. [Localizing MDN][] 페이지의 `Active locales/Korea (ko)/Current contributors` 수정.

## 리뷰어 안내서

1. 최대 2주 이내에 모든 pull request를 검토하고 조치한다.
2. [MDN 번역 콘텐츠에 대한 일반 안내서](/docs/ko/README.md#여러-안내서)를 숙지한다.
3. [용어 안내서](./glossary-guide.md)을 숙지하여 일관된 용어를 사용한다.

## yari-content-ko 팀 안내서

1. 1개월 이내에 실행 가능한 모든 문제를 분류하고 수정한다.
2. MDN의 Tier 1 콘텐츠를 en-US 버전과 동기화된 상태로 유지하는데 매주 조금의 진전을 보인다.

## Hall of Fame

### 과거 구성원

- [@GwangYeol-Im](https://github.com/GwangYeol-Im) 2021.04 ~ 2023.10
- [@yujo11](https://github.com/yujo11) 2021.04 ~ 2023.09
- [@nKiNk](https://github.com/nKiNk) 2021.04 ~ 2023.01
- [@pje1740](https://github.com/pje1740) 2021.04 ~ 2024.04
- [@swimjiy](https://github.com/swimjiy) 2023.03 ~ 2024.04
- [@cos18](https://github.com/cos18) 2021.04 ~ 2024.04
- [@jho2301](https://github.com/jho2301) 2023.03 ~ 2024.05

### 현재 구성원

- [@1ilsang](https://github.com/1ilsang) 2024.03 ~
- [@sunhpark42](https://github.com/sunhpark42) 2023.03 ~
- [@wisedog](https://github.com/wisedog) 2023.03 ~
- [@yechoi42](https://github.com/yechoi42) 2021.04 ~
- [@hochan222](https://github.com/hochan222) 2021.04 ~

## 참고 사항

- [mozilla mdn chat](https://chat.mozilla.org/#/room/#mdn:mozilla.org) 채널 및 [yari-content-ko](https://github.com/orgs/mdn/teams/yari-content-ko)에서 질문 및 토론을 할 수 있습니다.

[Localizing MDN]: https://developer.mozilla.org/en-US/docs/MDN/Contribute/Localize

---
# Source: markdown-guide.md
---
# 마크다운 안내서

## 표 (table)

`alt` + `z`로 줄 바꿈을 제거하여, 수월하게 확인하고 수정할 수 있습니다.

## 후행 구두점 (Trailing punctuation)

문장 형식으로 된 제목이나 표어 등에는 마침표를 쓰지 않는 것을 원칙으로 합니다. 단, 제목이나 표어 등에 꼭 필요하다고 판단될 때에는 예외적으로 마침표를 쓸 수도 있습니다. (참고: [국립국어원](https://korean.go.kr/front/onlineQna/onlineQnaView.do?mn_id=216&qna_seq=225670&pageIndex=1), [MD026 - Trailing punctuation in header](https://github.com/updownpress/markdown-lint/blob/master/rules/026-no-trailing-punctuation.md), [ko: Remove trailing punctuation in headers PR](https://github.com/mdn/translated-content/pull/14236))

### 나쁜 예시

```
## 블록이 무너지면 점수를 갱신합니다.
```

### 올바른 예시

```
## 블록이 무너지면 점수를 갱신합니다
```

---
# Source: etc-guide.md
---
# 기타 안내서

## 충돌 해결 방법

> **This branch has conflicts that must be resolved**

충돌 발생 시 아래와 같은 방법으로 해결할 수 있습니다.

### `Resolve conflicts` 버튼이 눌리는 경우

아래와 같이 표시된 충돌 지점들을 해결해야 합니다.

#### AS IS

```
1 <<<<<<< ko/variables
2       <p>현재 PR(ko/variables 브랜치)의 내용</p>
3 =======
4       <p>main 브랜치의 내용</p>
5 >>>>>>> main
```

#### TO BE

- 현재 PR(ko/variables 브랜치)의 내용 반영 시

```
1       <p>현재 PR(ko/variables 브랜치)의 내용</p>
```

- main 브랜치의 내용 반영 시

```
1       <p>main 브랜치의 내용</p>
```

### `Resolve conflicts` 버튼이 눌리지 않는 경우

(1) 기여한 PR의 저장소를 `git clone` 합니다.

```sh
git clone https://github.com/---user-id---/translated-content.git
```

(2) 기여한 PR의 브랜치로 `git switch` 합니다.

```sh
git switch ---기여한 PR의 브랜치 이름---
```

(3) `mdn/translated-content` 저장소의 최신 내용을 현재 브랜치에 병합하기 위해 url을 `git remote`로 등록합니다.

```sh
git remote add upstream https://github.com/mdn/translated-content
```

(4) 등록한 `upstream`을 fetch와 merge 합니다.

```sh
git fetch upstream
git merge upstream/main
```

merge 이후 자동 병합에 실패할 때 메시지는 아래와 같습니다.

> 자동 병합: files/ko/learn/javascript/---path---/---filename---.md
>
> 충돌 (내용): files/ko/learn/javascript/---path---/---filename---.md에 병합 충돌
>
> 자동 병합이 실패했습니다. 충돌을 바로잡고 결과물을 커밋하십시오.

(4-1) 자동 병합에 실패했을 때, 발생한 모든 충돌을 해결합니다. 반영할 내용으로 수정합니다.

#### AS IS

```
1 <<<<<<< HEAD
2       <td>현재 PR(ko/variables 브랜치)의 내용</td>
3 =======
4       <td>upstream/main 브랜치의 내용</td>
5 >>>>>>> upstream/main
```

#### TO BE

```
1       <td>현재 PR(ko/variables 브랜치)의 내용</td>
```

(5) 현재 PR에 반영합니다.

```sh
git add ---filename---.md
git commit -m "---커밋 메시지---"
git push
```

---
# Source: markdown-conversion-guide.md
---
# MDN ko locale Markdown 번역에 대한 일반 안내서

> 참고: 2022.11월부터 모든 .html 파일들이 .md 파일로 변환 되었습니다. 이 파일을 참고용으로만 사용 부탁드립니다.

## .html 확장자에서 .md 확장자로의 파일 변경일 경우

아래 두 가지 경우에 총 2개의 commit으로 구분해서 PR을 제출해주세요.

1. 확장자만 `html`에서 `md`로 바꾸고 commit 해주세요.
2. `html` 형식에서 `md` 형식으로 변경한 뒤 commit을 해주세요.

html 파일에 대한 commit은 오로지 확장자를 바꾸는 것만 허용됩니다. 또한, 전체 commit 개수를 2개를 넘지 않도록 합니다(`squash and merge`가 아닌 `rebase and merge`를 해야하기 때문입니다.). `squash and merge`를 하거나 확장자 변경 작업이 없을 경우 Git History가 소멸되는데, 이전 기여자들의 기록을 남기기 위함입니다. 예시는 [확장자 변경 PR](https://github.com/mdn/translated-content/pull/1769/commits/c7937cf2194d218d98394cd7f5f8acebd2e88aa0)를 참고해주세요.

다음 [PR](https://github.com/mdn/translated-content/pull/1771)은 모범적인 PR입니다.

현재 진행 사항은 [[ko] Markdown conversion for ko RoadMap](https://github.com/mdn/translated-content/issues/2894)을 참고 부탁드립니다.

## 리뷰

리뷰로 인해 수정사항이 발생할 경우, 예외적으로 **수정 사항에 대해서 commit의 개수를 1개를 추가적으로 허용합니다.**

> 참고
> `git log --follow (파일)` 로 해당 파일의 git history를 볼 수 있습니다.

## 그 이외의 경우 (이미 md 파일이 존재하거나, 해당 번역 페이지가 없는 경우)

일반 PR 방식대로 진행합니다.

## MDN ko locale Markdown 번역에 대한 일반 안내서 (리뷰어)

1. `존재하는 파일에 대한 변경 (존재하는 파일이 .html 확장자일 경우)`에 대해서는 `squash and merge`가 아닌 `rebase and merge`를 진행해야합니다.
2. 파일에 대한 Git History가 유지되는지 확인해주세요.
3. commit의 개수는 최소가 되어야 합니다.

---
# Source: html-guide.md
---
# HTML 번역 안내서

## heading ID 번역

기사 제목에는 거의 항상 ID가 주어지는데, 기사 내에서 네비게이션을 자동으로 생성하고 실시간 샘플을 생성하기 위한 코드 블록을 식별하는 등의 이유가 있습니다. 제목을 번역 할 때 ID도 같이 번역 할 필요가 없습니다. 나머지 슬러그는 번역되지 않으므로 모든 것이 일관되게 유지됩니다.

예를 들면:

```html
<h2 id="tutorials">Tutorials</h2>
```

`ko` 지역 에서

```html
<h2 id="tutorials">튜토리얼</h2>
```

일반적으로 모든 ID를 소문자로 작성하는 것이 좋습니다. 플랫폼은 어쨌든 렌더링시 자동으로 변환하지만 소문자로 유지하면 변환으로 인해 수동으로 만든 앵커 링크가 작동하지 않을 가능성이 적습니다.

## HTML 소스의 줄 바꿈

일부 기사 소스 코드에서, 반드시 필요하지 않은 블록 수준 요소에서 줄 바꿈을 찾을 수 있습니다. 예를 들면 다음과 같습니다.

```html
<p>
  The <code><strong>HTMLCanvasElement</strong></code
  ><strong><code>.transferControlToOffscreen()</code></strong> method transfers
  control to an {{domxref("OffscreenCanvas")}} object, either on the main thread
  or on a worker.
</p>

<pre class="brush: js">
OffscreenCanvas HTMLCanvasElement.transferControlToOffscreen()</pre
>
```

일반적으로 소스 코드에서 이와 같은 줄 바꿈을 사용하지 않으므로 원하는 경우 자유롭게 제거 할 수 있으며 새 번역을 만들 때 추가하지 마십시오. 그러나 최종 렌더링 결과에 영향을 미치지 않으므로 이를 제거하는 데 너무 많은 시간을 소비하지 마십시오.

---
# Source: macro-guide.md
---
# macro 안내서

## 명세서

명세서 영역은 [Replace old-style compatibility/specification tables with new macro](https://github.com/mdn/translated-content/issues/5618)에 따라 아래와 같이 작성합니다.

```
## 명세서

{{Specifications}}
```

## 브라우저 호환성

브라우저 호환성 영역은 [Replace old-style compatibility/specification tables with new macro](https://github.com/mdn/translated-content/issues/5618)에 따라 아래와 같이 작성합니다.

```
## 브라우저 호환성

{{Compat}}
```

## [EmbedLiveSample](/en-US/docs/MDN/Writing_guidelines/Page_structures/Live_samples)

### EmbedLiveSample 오류 발생하는 문서 찾는 스크립트

EmbedLiveSample/MacroLiveSampleError 오류 찾는 [스크립트 링크 참고](https://gist.github.com/hochan222/f7d3fead51f75c73b732dbd3697220bf) ([Thanks to SphinxKnight - All Korean pages with an EmbedLiveSample error](https://github.com/mdn/translated-content/issues/2848))

## 매크로 수정 및 번역

MDN은 초창기에 [kuma](https://github.com/mdn/kuma) 플랫폼으로 MDN 웹 문서를 구동해왔습니다. 그 당시 사용한 많은 매크로들이 레거시로 남아 있습니다. 레거시로 남은 매크로를 [Kumascript](https://github.com/mdn/kumascript)라고 부릅니다. 현재는 [yari 저장소 내의 kumascript 폴더](https://github.com/mdn/yari/tree/main/kumascript)로 대체되어 사용되고 있습니다([참고](https://egas.tistory.com/168#%EB%AF%B8%EC%82%AC%EC%9A%A9-macro-%EC%A0%9C%EA%B1%B0)).

---
# Source: meta-data-guide.md
---
# Meta Data 안내서

## 메타데이터 사용

문서의 상단에 있는 메타데이터는 `title`, `short-title`, `slug` 그리고 `l10n.*`만 사용합니다. (참고: [#7412](https://github.com/mdn/translated-content/issues/7412))

영어 원문

```markdown
---
title: Proxy
slug: Web/JavaScript/Reference/Global_Objects/Proxy
tags:
  - Class
  - ECMAScript 2015
  - JavaScript
  - Proxy
- browser-compat: javascript.builtins.Proxy
---

{{JSRef}}

The `Proxy` object enables you to create a proxy for another ...
:
```

번역본

```markdown
---
title: Proxy
slug: Web/JavaScript/Reference/Global_Objects/Proxy
l10n:
  sourceCommit: 2eb202adbe3d83292500ed46344d63fbbae410b5
---

{{JSRef}}

**`Proxy`** 객체는 기본적인 동작(속성 접근, 할당, 순회, 열거, 함수 ...
:
```

<details>
<summary>참고 문서</summary>

- 2023.05.01: `original_slug` 필수 항목에서 제거 ([링크](https://github.com/mdn/translated-content/issues/7412#issuecomment-1518546547))
- 2023.05.01: `short-title` 필수 항목에 추가 ([링크](https://github.com/mdn/yari/issues/8647#issuecomment-1520722736))

</details>

## 문서 갱신 표시

번역된 문서가 `en-US` 문서에 대해 얼마나 뒤쳐져 있는지 알 수 있는 마땅한 방법이 없습니다. `l10n.sourceCommit` 메타데이터를 추가하여 현재 문서가 명시된 `en-US`의 hash 까지 최신 상태를 유지하고 있음을 나타낼 수 있습니다. (참고: [How to indicate "content parity" of localized documents vs en-US counterparts?](https://github.com/orgs/mdn/discussions/129))

- sourceCommit: 기여하는 문서와 동일한 `en-US` 문서의 가장 최신 40자리 hash를 명시합니다. (예: `slug: Glossary/Array` 문서에 대해 기여할 때, [content 저장소](https://github.com/mdn/content)의 `slug: Glossary/Array` 문서에서 가장 최신 40자리 hash를 명시합니다.)

> **주의:** content 저장소의 가장 최신 hash가 아닌, content 저장소에서 기여하는 문서와 동일한 위치의 파일에 대한 hash 입니다.

```markdown
---
title: TypedArray.prototype.entries()
slug: Web/JavaScript/Reference/Global_Objects/TypedArray/entries
l10n:
  sourceCommit: 2eb202adbe3d83292500ed46344d63fbbae410b5
---

{{JSRef}}

**`entries()`** 메서드는 해당 배열의 각 인덱스에 대한 키/값 쌍을 포함하는 새로운 {{jsxref("Array", "배열")}} 반복자 객체를 반환합니다.
```

작성한 hash는 <https://github.com/mdn/content/commit/2eb202adbe3d83292500ed46344d63fbbae410b5>로 접근 가능한 hash 입니다.

---
# Source: translation-guide.md
---
# 번역 안내서

## 문서 연결 경로

한글 문서가 존재하지 않더라도 `/en-US` 문서로 넘겨주기 때문에 한국 문서의 모든 경로는 `/ko`로 표기합니다.

```
// bad
[`Array`](/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)

// good
[`Array`](/ko/docs/Web/JavaScript/Reference/Global_Objects/Array)
```

## 이미지 파일

`translate-content` 저장소에서 더 이상 `mdn/content`의 이미지 파일들을 복사하지 않아도 됩니다.

#### 참고 PR

- [deleted duplicated mdn/content images/assets #4545](https://github.com/mdn/translated-content/pull/5031)
- [Remove unused assets](https://github.com/mdn/translated-content/pull/14664)

## Inline code

원문의 인라인 코드는 번역하지 않습니다.

## Block code

코드 블록을 번역 할 때 주석, 문자열, 변수 이름 및 출력물을 번역하는 것이 좋습니다.

그러나 구문과 같은 실제 코드 용어를 번역하지 마십시오. 예제는 작업을 마친 후에도 계속 작동해야합니다.

또한, 예제 번역을 고려할 때, 일부 예제는 별도의 저장소에 있는 라이브 버전 또는 소스 코드에 연결된다는 점을 염두에 두십시오. 여러분은 또한 번역 된 페이지에서 링크 할 외부 코드 예제의 번역 된 버전을 만드는 것을 고려할 수도 있습니다.

## 안내 문구

각 페이지의 안내 문구에 대한 단어 정의입니다.

**사전 순으로 용어집을 편집해주세요.**

| 용어          | 번역             | 참고 링크                     |
| ------------- | ---------------- | ----------------------------- |
| Objective     | 목표             | [링크][What_is_accessibility] |
| Prerequisites | 필요한 사전 지식 | [링크][What_is_accessibility] |

### 교육 과정 callout

```markdown
> [!CALLOUT]
>
> #### 프론트엔드 웹 개발자가 되고자 하시나요?
>
> 프론트엔드 웹 개발자가 되고 싶지만 무엇을 먼저 배워야 할지 모르겠다면, MDN 커리큘럼을 참고해 학습 계획을 세우는 것을 추천합니다. 이 커리큘럼은 성공적인 프론트엔드 개발자가 되기 위한 필수 기술과 실습을 체계적으로 학습할 수 있는 경로를 제공하며, 추천 학습 자료도 함께 제공합니다.
>
> [**시작하기**](/ko/curriculum/)
```

## GFM Alerts

`> [!NOTE]`, `> [!TIP]`, `> [!IMPORTANT]`, `> [!CAUTION]`, `> [!WARNING]`은 새로 추가된 github markdown으로 영어 문법만 사용할 수 있습니다.

```markdown
// bad

> [!참고]
> ...
```

- [[Markdown] An option to highlight a "Note" and "Warning" using blockquote (Beta)](https://github.com/orgs/community/discussions/16925)
- [Incorrect formatting for highlighted notes in GitHub flavoured Markdown](https://github.com/prettier/prettier/issues/16454)

## 역주/역자주

그동안의 MDN 문서에서는 역주로 인한 자의적인 해석이 많았고, 전체적인 문서의 품질을 낮췄습니다. 역주가 꼭 필요한 상황이 아니라면 역주는 남기지 않으며, 남기더라도 따로 역주를 표시하지 않고 본문에 포함합니다.
예시: [다음 링크 참고](https://github.com/mdn/translated-content/pull/1385#discussion_r667509255)

## 기울임꼴

한글은 기울임꼴에 적합하지 않습니다. 전용 이탤릭체가 없다는 것이 첫 이유이고, 문자의 조형이 (정)사각형인 것이 두 번째 이유입니다. [세부 내용 다음 링크 참고](https://github.com/mdn/translated-content/issues/1537)

- 기본 방침은 생략하며, 기여자에 재량에 따라 아래 두 가지 규칙을 따른다.
  - 한글일 경우 '' 를 tag 대신에 기입한다.
  - 한글이 아닐 경우 생략한다.

다만 진짜 강조를 해야하는 상황에는, 따옴표로 강조하고 PR로 소명합니다.

## `:` 쌍점, `;` 쌍반점

뒤의 문장 예시를 강조하기 위해 쌍점을 사용하는 경우에 `: 쌍점`은 한글 문법에 적합하지 않습니다. [(참고 이슈 링크)](https://github.com/mdn/translated-content/pull/2747#issuecomment-964241518)

`한글맞춤법-부록-문장 부호` 부분의 `: 쌍점`에 대한 규정만 존재하고, `; 쌍반점`에 대한 규정은 존재하지 않습니다. 따라서, 해당 경우가 아니면 `: 쌍점`을 `. 온점`으로 치환하는 것을 권장합니다. `; 쌍반점`의 경우는 `. 온점`으로 치환하는 것을 권장합니다.

```
<한글맞춤법-부록-문장부호>

쌍점( : )

(1) 내포되는 종류를 들 적에 쓴다.

문장 부호: 마침표, 쉼표, 따옴표, 묶음표 등 문방사우: 붓, 먹, 벼루, 종이

(2) 소표제 뒤에 간단한 설명이 붙을 때에 쓴다.

일시: 1984 년 10 월 15 일 10 시
마침표: 문장이 끝남을 나타낸다.

(3) 저자명 다음에 저서명을 적을 때에 쓴다.

정약용: 목민심서, 경세유표
주시경: 국어 문법, 서울 박문 서관, 1910.

(4) 시(時)와 분(分), 장(章)과 절(節) 따위를 구별할 때나, 둘 이상을 대비할 때에 쓴다.

오전 10:20 (오전 10 시 20 분)
요한 3:16 (요한복음 3 장 16 절)
대비 65:60 (65 대 60)
```

- 원문 [(참고 링크)][]

```
The properties of these objects are as follows:
```

- 변경 전

```
이 객체들의 속성은 다음과 같습니다:
```

- 변경 후

```
이 객체들의 속성은 다음과 같습니다.
```

## `—` 대시

`: 쌍점,  ; 쌍반점 안내서`과 같은 맥락에서 `. 온점`으로 치환하는 것을 권장합니다. [(참고 이슈 링크)](https://github.com/mdn/translated-content/pull/2747#issuecomment-965500282)

- 원문

```
A value of 0.01 was used for the value to ramp down to in the last function rather than 0, as an invalid or illegal string error is thrown if 0 is used — the value needs to be positive.
```

- 변경 전

```
오류가 발생되기 때문입니다 — 이 값은 양수일 필요가 있습니다.
```

- 변경 후

```
오류가 발생되기 때문입니다. 이 값은 양수일 필요가 있습니다.
```

[(참고 링크)]: https://developer.mozilla.org/en-US/docs/Web/API/AudioWorkletProcessor/parameterDescriptors

## 표현

MDN 문서는 구어체의 격식체를 **권장**하고 있습니다. 하지만, 상황에 따른 적절한 표현이 다르기 떄문에 강제하고 있지 않습니다.

아래는 구어체의 격식체와 비격식체의 차이입니다.

### 구어체 - 격식체

> 가장 먼저 해야할 일은 간격/레이아웃을 정렬하는 것입니다. 기본 표 스타일은 너무 비좁습니다! 이렇게 하려면, style.css 파일에 다음 CSS 를 추가하십시오.

### 구어체 - 비격식체

> 가장 먼저 해야할 일은 간격/레이아웃을 정렬하는 것이에요. 기본 표 스타일은 너무 비좁아요! 이렇게 하려면, style.css 파일에 다음 CSS 를 추가하세요.

## 따옴표

둥근 따옴표(smart quotes)를 사용하지 않고, **일반 따옴표(normal quotes)를 사용**해야 합니다. ([ko: Replace smart quotes](https://github.com/mdn/translated-content/pull/14218) 참고)

### 나쁜 예시

```
(1) 일반적으로 눈에 띄게 “Get a domain name” 이라는 글자가 있습니다.
(2) We’re adding an event listener to...
(3) ‘문단’이나 ‘이미지’와 같은 페이지의 부분을 정의하는 것처럼
```

### 올바른 예시

```
(1) 일반적으로 눈에 띄게 "Get a domain name" 이라는 글자가 있습니다
(2) We're adding an event listener to...
(3) '문단'이나 '이미지'와 같은 페이지의 부분을 정의하는 것처럼
```

## 괄호 표기 지양

괄호 사용을 지양합니다. 괄호가 남용되는 사례가 너무 많았고, 남용되지 않더라도 원문에 존재하지 않은 괄호는 가독성을 저하시키고 기여자의 의견을 작성하는 용도로 많이 사용되어서 지양합니다.

예외적으로 `한글(영어)` 표기는 좋은 방법은 아니지만, 필요한 경우에 리뷰어와 협의하여 사용할 수 있습니다.

## 원문과 동일한 문서

번역 후의 줄 수와 원문의 줄 수가 같도록 해주세요. 이는 원문과 달라진 부분을 빨리 찾을 수 있으므로 유지보수에 도움이 됩니다.

관련 논의는 [Exploring Guidelines for Line Length and Newline in Markdown Documentation. #655](https://github.com/orgs/mdn/discussions/655#discussioncomment-9251708)에서 확인할 수 있습니다.

---
# Source: glossary-guide.md
---
# 용어 안내서

새로운 용어를 추가할 때, 기존 문서의 레거시와 [국립 국어원 한국어 어문 규범](https://korean.go.kr/kornorms/main/main.do)을 고려해 추가할 것을 권장합니다. [국립 국어원 온라인가나다](https://www.korean.go.kr/front/onlineQna/onlineQnaList.do?mn_id=216)에서 어문 규범, 어법, 표준국어대사전 내용 등에 대하여 문의할 수 있습니다.

## 공통

- 브랜드 이름은 번역하지 않습니다.

  ```diff
  - 자바스크립트
  - 씨에스에스
  - 모질라
  + JavaScript
  + CSS
  + Mozilla
  ```

- "무슨무슨 값" (numeric value, integer value, ...) 같은 경우, 항상 띄어서 표기합니다.
  - 통일성을 위해 "반환 값" 같은 경우 띄어서 표기합니다.
  - 예: 정수 값, 소수 값, 반환 값, 기본 값
  - 틀린 예: 정숫값, 소숫값, 반환값, 기본값

## 용어 안내서 `참고 링크` 우선 순위

1. 해당 단어에 대한 의견을 나눈 PR 링크
2. 적절한 ko MDN 문서 링크
3. 적절한 en-us MDN 문서 링크

## Section Title

각 페이지의 Section Title에 대한 단어 정의입니다.

**사전 순으로 용어집을 편집해주세요.**

| 용어                   | 번역            | 참고 링크                                                                                                                               |
| ---------------------- | --------------- | --------------------------------------------------------------------------------------------------------------------------------------- |
| Access                 | 접근            |                                                                                                                                         |
| Accessibility concerns | 접근성 고려사항 |                                                                                                                                         |
| Advanced Topics        | 고급 주제       |                                                                                                                                         |
| Advantages             | 장점            | [링크][Introduction_to_HTML5_Game_Development]                                                                                          |
| Aliasing               | 별칭            | [링크](https://github.com/mdn/translated-content/pull/1779/files)                                                                       |
| Brief history          | 간략한 역사     | [링크][HTML#%EA%B0%84%EB%9E%B5%ED%95%9C_%EC%97%AD%EC%82%AC]                                                                             |
| Browser compatibility  | 브라우저 호환성 | [링크](https://github.com/mdn/translated-content/pull/1779/files)                                                                       |
| Browser support        | 브라우저 지원   | [링크][Using_IIR_filters]                                                                                                               |
| Concept                | 개념            |                                                                                                                                         |
| Conclusion             | 결론            |                                                                                                                                         |
| Contact us             | 문의하기        |                                                                                                                                         |
| Demo                   | 데모            | [링크][GLSL_Shaders]                                                                                                                    |
| Description            | 설명            | [링크][Array]                                                                                                                           |
| Example                | 예제            | [링크][target]                                                                                                                          |
| Examples               | 예제            | [링크](https://github.com/mdn/translated-content/blob/main/files/ko/web/javascript/reference/global_objects/proxy/proxy/apply/index.md) |
| Exceptions             | 예외            |                                                                                                                                         |
| Guides                 | 안내서          |                                                                                                                                         |
| In this module         | 이번 과정에서는 | [링크][React_getting_started]                                                                                                           |
| Instance properties    | 인스턴스 속성   |                                                                                                                                         |
| Instance methods       | 인스턴스 메서드 |                                                                                                                                         |
| Learn More             | 더 알아보기     | [링크][Mutable]                                                                                                                         |
| Next steps             | 다음 단계       | [링크][2D_breakout_game_Phaser]                                                                                                         |
| Overview               | 개요            |                                                                                                                                         |
| Polyfill               | 폴리필          | [링크](https://github.com/mdn/translated-content/pull/1779/files)                                                                       |
| Recommendations        | 권장 사항       |                                                                                                                                         |
| Reference              | 참고서          |                                                                                                                                         |
| Return Value           | 반환 값         |                                                                                                                                         |
| See also               | 같이 보기       | [링크][target]                                                                                                                          |
| Specifications         | 명세서          | [링크](https://github.com/mdn/translated-content/pull/1779/files)                                                                       |
| Static properties      | 정적 속성       |                                                                                                                                         |
| Static methods         | 정적 메서드     |                                                                                                                                         |
| Sticky activation      | 고정 활성화     |                                                                                                                                         |
| Summary                | 요약            |                                                                                                                                         |
| Syntax                 | 구문            | [링크][target]                                                                                                                          |
| Tools & resources      | 도구 & 리소스   | [링크][JavaScript]                                                                                                                      |
| Transient activation   | 임시 활성화     |                                                                                                                                         |
| Tutorial               | 자습서          |                                                                                                                                         |
| Usage context          | 사용 맥락       |                                                                                                                                         |
| Usage notes            | 사용 일람       |                                                                                                                                         |
| Web Technologies       | 웹 기술들       | [링크][Introduction_to_HTML5_Game_Development]                                                                                          |

## Section Subtitle

각 페이지의 Section Subtitle에 대한 단어 정의입니다.

**사전 순으로 용어집을 편집해주세요.**

| 용어                | 번역             | 참고 링크                                                                              |
| ------------------- | ---------------- | -------------------------------------------------------------------------------------- |
| Compatibility notes | 호환성 참고 사항 | [링크][target]                                                                         |
| Directives          | 지시어           | [링크](https://github.com/mdn/translated-content/issues/11093#issuecomment-1411005106) |
| Guide               | 안내서           | [링크](https://github.com/mdn/translated-content/issues/11093#issuecomment-1411005106) |
| Instruction         | 지침             | [링크](https://github.com/mdn/translated-content/issues/11093#issuecomment-1411005106) |
| Learning Outcomes   | 학습 성과        |                                                                                        |
| Naming              | 이름 지정        |                                                                                        |
| Parameters          | 매개변수         | [링크][AudioWorkletNode]                                                               |
| Prerequisites       | 선행 지식        |                                                                                        |
| Requirements        | 요구 사항        |                                                                                        |
| Value               | 값               | [링크][target]                                                                         |

## 공통 용어

**사전 순으로 용어집을 편집해주세요.**

| 용어                | 번역            | 기타                                                                           |
| ------------------- | --------------- | ------------------------------------------------------------------------------ |
| Application         | 애플리케이션    |                                                                                |
| Assertion           | 어설션          |                                                                                |
| Attribute           | 특성            |                                                                                |
| Boolean             | 불리언          |                                                                                |
| Capture             | 캡처            |                                                                                |
| Class               | 클래스          |                                                                                |
| Command line        | 명령줄          |                                                                                |
| Content(s)          | 콘텐츠          |                                                                                |
| Context             | 맥락            |                                                                                |
| Control             | 컨트롤          |                                                                                |
| Cross-browser       | 크로스 브라우저 |                                                                                |
| Custom              | 사용자 정의     |                                                                                |
| Decoding            | 디코딩          | [링크](https://github.com/mdn/translated-content/issues/12452)                 |
| Document            | 문서            |                                                                                |
| Editor              | 편집기          |                                                                                |
| Element             | 요소            |                                                                                |
| Encoding            | 인코딩          | [링크](https://github.com/mdn/translated-content/issues/12452)                 |
| Entity              | 개체            |                                                                                |
| Enumerated          | 열거형          |                                                                                |
| Error               | 오류            |                                                                                |
| Event               | 이벤트          |                                                                                |
| Expression          | 표현식 또는 식  |                                                                                |
| Fallback            | 폴백            |                                                                                |
| Framework           | 프레임워크      |                                                                                |
| Global              | 전역            |                                                                                |
| Glossary            | 용어 사전       |                                                                                |
| Grammar             | 문법            |                                                                                |
| Hash                | 해시            |                                                                                |
| In modern browsers  | 최신 브라우저   |                                                                                |
| Library             | 라이브러리      |                                                                                |
| License             | 라이선스        |                                                                                |
| Literal             | 리터럴          |                                                                                |
| Mantissa            | 가수부          |                                                                                |
| Mechanism           | 메커니즘        |                                                                                |
| Media               | 미디어          |                                                                                |
| Method              | 메서드          | method [meθəd] 메서드                                                          |
| Mime                | MIME            |                                                                                |
| Module              | 모듈            | ESM에서 명시하는 모듈의 경우 '모듈'로 변역한다.                                |
| Module              | 과정            | 어떠한 교육 과정, 단위에 의한 표현은 '과정'으로 번역한다. (예: In this module) |
| Object              | 객체            |                                                                                |
| On-demand(onDemand) | 온디맨드        |                                                                                |
| Origin              | 출처            |                                                                                |
| Override            | 재정의          |                                                                                |
| Primitive           | 원시 (값)       |                                                                                |
| Profile             | 프로필          |                                                                                |
| Property            | 속성            |                                                                                |
| Protocol            | 프로토콜        |                                                                                |
| Psuedo-             | 의사-           |                                                                                |
| Reference           | 참고서          |                                                                                |
| Regular expression  | 정규 표현식     |                                                                                |
| Rendering           | 렌더링          |                                                                                |
| Section             | 구획            |                                                                                |
| Space bar           | 스페이스 바     |                                                                                |
| Statement           | 명령문 또는 문  |                                                                                |
| Tag                 | 태그            |                                                                                |
| Tip                 | 팁              |                                                                                |
| Trigger             | 트리거          |                                                                                |
| Tutorial            | 튜토리얼        |                                                                                |
| User agent          | 사용자 에이전트 |                                                                                |
| Update              | 갱신            |                                                                                |
| Workflow            | 워크플로우      |                                                                                |
| Truthy              | 참 같은         |                                                                                |
| Falsy               | 거짓 같은       |                                                                                |

## CSS

명세 이름은 번역하지 않습니다.

```diff
- CSS 글꼴 모듈 레벨 4
+ CSS Fonts Module Level 4
```

명세 이름이 본문에 나오더라도 번역하지 않습니다. (예: "`<number>` 구문은 CSS Fonts Level 4가 추가했습니다.")

**사전 순으로 용어집을 편집해주세요.**

| 용어               | 번역            | 기타                        | 참고 링크                                                                               |
| ------------------ | --------------- | --------------------------- | --------------------------------------------------------------------------------------- |
| At-rule            | @규칙           |                             |                                                                                         |
| Block              | 블록            |                             |                                                                                         |
| Border             | 테두리          |                             |                                                                                         |
| Box                | 박스            |                             |                                                                                         |
| Cascade            | 캐스케이드      |                             | [참고링크](https://github.com/mdn/translated-content/pull/15519#discussion_r1320588159) |
| Descriptor         | 설명자          |                             |                                                                                         |
| Flexbox            | 플렉스박스      |                             |                                                                                         |
| Flow               | 플로            | 레이아웃 방식일 경우에 한정 |                                                                                         |
| Formal definition  | 형식 정의       |                             |                                                                                         |
| Formal syntax      | 형식 구문       |                             |                                                                                         |
| Grid               | 그리드          |                             |                                                                                         |
| Inline             | 인라인          |                             |                                                                                         |
| Layout             | 레이아웃        |                             |                                                                                         |
| Longhand property  | 본디 속성       |                             |                                                                                         |
| Margin             | 바깥 여백       |                             |                                                                                         |
| Padding            | 안쪽 여백(패딩) |                             | [CSS 기본 박스 모델 입문][]                                                             |
| Shorthand property | 단축 속성       |                             |                                                                                         |

## API/JavaScript

**사전 순으로 용어집을 편집해주세요.**

| 용어                    | 번역            | 기타              | 참고 링크                                                                                |
| ----------------------- | --------------- | ----------------- | ---------------------------------------------------------------------------------------- |
| Argument                | 전달인자, 인수  |                   | [참고 링크](https://github.com/mdn/translated-content/pull/3888)                         |
| Blocking operation      | 블로킹 연산     |                   |                                                                                          |
| Callback                | 콜백            |                   |                                                                                          |
| Decimal equivalent      | 10진수 변환 값  |                   |                                                                                          |
| Dictionary              | 사전            |                   | [참고 링크](https://github.com/mdn/translated-content/pull/10976#discussion_r1073704799) |
| Fulfilled               | 이행(함)        |                   |                                                                                          |
| Fetch                   | 페치            | Patch와 음차 구분 | [참고 링크](https://ko.dict.naver.com/#/search?query=fetch)                              |
| Handler                 | 처리기          | 이벤트 처리기     |                                                                                          |
| Interface               | 인터페이스      |                   |                                                                                          |
| Iterate                 | 순회            |                   |                                                                                          |
| Iterator                | 반복자          |                   |                                                                                          |
| Listener                | 수신기          | 이벤트 수신기     |                                                                                          |
| Mixin                   | 믹스인          |                   |                                                                                          |
| Mutating method         | 변경 메서드     |                   |                                                                                          |
| Non-blocking operation  | 논블로킹 연산   |                   |                                                                                          |
| Parameter               | 매개변수        |                   |                                                                                          |
| Patch                   | 패치            |                   |                                                                                          |
| Pending                 | 대기            |                   |                                                                                          |
| Promise                 | 프로미스        |                   | [참고 링크](https://github.com/mdn/translated-content/pull/1081#issuecomment-878333558)  |
| Promise chaining        | 프로미스 체이닝 |                   |                                                                                          |
| Prototype               | 프로토타입      |                   |                                                                                          |
| Reject                  | 거부            |                   |                                                                                          |
| Resolve                 | 이행            |                   |                                                                                          |
| Rest parameters         | 나머지 매개변수 |                   | [참고 링크](https://github.com/mdn/translated-content/pull/2549/files)                   |
| Scope                   | 범위            |                   |                                                                                          |
| Settled                 | 처리            |                   |                                                                                          |
| Sparse array            | 희소 배열       |                   |                                                                                          |
| Spread                  | 전개            |                   | [참고 링크](https://github.com/mdn/translated-content/pull/14898#discussion_r1296533201) |
| Temporal Dead Zone, TDZ | 일시적 사각지대 |                   | [참고 링크](https://github.com/mdn/translated-content/pull/2626/files)                   |
| TypedArray              | 형식화 배열     |                   |                                                                                          |

## HTTP

| 용어          | 번역      | 기타 | 참고 링크                                                        |
| ------------- | --------- | ---- | ---------------------------------------------------------------- |
| Idempotent    | 멱등성    |      |                                                                  |
| Payload       | 페이로드  |      | [참고 링크](https://github.com/mdn/translated-content/pull/2737) |
| Request Body  | 요청 본문 |      |                                                                  |
| Response Body | 응답 본문 |      |                                                                  |

## React

| 용어  | 번역  | 기타 | 참고 링크                                                                                |
| ----- | ----- | ---- | ---------------------------------------------------------------------------------------- |
| Props | props |      | [참고 링크](https://github.com/mdn/translated-content/pull/14898#discussion_r1299129511) |
| hooks | hooks |      |                                                                                          |

[AudioWorkletNode]: https://developer.mozilla.org/en-US/docs/Web/API/AudioWorkletNode/AudioWorkletNode#parameters
[Using_IIR_filters]: https://developer.mozilla.org/en-US/docs/Web/API/Web_Audio_API/Using_IIR_filters#browser_support
[CSS 기본 박스 모델 입문]: https://developer.mozilla.org/ko/docs/Web/CSS/CSS_Box_Model/Introduction_to_the_CSS_box_model
[Introduction_to_HTML5_Game_Development]: https://developer.mozilla.org/en-US/docs/Games/Introduction_to_HTML5_Game_Development
[HTML#%EA%B0%84%EB%9E%B5%ED%95%9C_%EC%97%AD%EC%82%AC]: https://developer.mozilla.org/ko/docs/Glossary/HTML#%EA%B0%84%EB%9E%B5%ED%95%9C_%EC%97%AD%EC%82%AC
[target]: https://developer.mozilla.org/en-US/docs/Web/API/Event/target
[GLSL_Shaders]: https://developer.mozilla.org/en-US/docs/Games/Techniques/3D_on_the_web/GLSL_Shaders#demo
[Array]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array#description
[JavaScript]: https://developer.mozilla.org/en-US/docs/Web/JavaScript
[React_getting_started]: https://developer.mozilla.org/ko/docs/Learn/Tools_and_testing/Client-side_JavaScript_frameworks/React_getting_started#in_this_module
[Mutable]: https://developer.mozilla.org/en-US/docs/Glossary/Mutable
[2D_breakout_game_Phaser]: https://developer.mozilla.org/ko/docs/Games/Tutorials/2D_breakout_game_Phaser#%EB%8B%A4%EC%9D%8C_%EB%8B%A8%EA%B3%84

---
# Source: README.md
---
# 목차

1. **[MDN 번역 콘텐츠에 대한 일반 안내서](#MDN-번역-콘텐츠에-대한-일반-안내서)**
2. **[첫 기여자들을 위한 안내서](#첫-기여자들을-위한-안내서)**
3. **[yari 빠른 사용법](#yari-빠른-사용법)**
4. **[여러 안내서](#여러-안내서)**
5. **[자주 묻는 질문](#자주-묻는-질문)**
6. **[맺음말](#맺음말)**

---

## MDN 번역 콘텐츠에 대한 일반 안내서

이 문서는 한국(ko) 지역에 대한 번역 안내서입니다. 몇 가지 특정 안내서를 문서화하는 페이지를 추가하고 싶은 경우, 현재 경로에 추가하거나 [Locale Teams](https://github.com/mdn/translated-content/blob/main/PEERS_GUIDELINES.md#review-teams)에 문의해주세요.

마찬가지로 추가하려는 일반 안내서에 대한 좋은 아이디어가 있는 경우 환영합니다. Issue를 열고 문제에 대해 이야기해주세요. 다음은 한국어 번역 안내서 원칙의 주요 내용입니다.

> 어떻게 시작해야 할지 어려우신가요?
> [MDN Discord #korean 채널](https://discord.com/channels/1009925603572600863/1070064829466939503) 혹은 [Google Groups (yari-content-ko)](https://groups.google.com/g/yari-content-ko)으로 어려운 사항들 이야기해주세요!

## 첫 기여자들을 위한 안내서

MDN의 모든 로케일은 `en-us`를 기준으로 변역이 진행되고 있습니다. 한국 로케일[(translated-content)](https://github.com/mdn/translated-content)도 `en-us`[(content)](https://github.com/mdn/content)를 기반으로 번역이 진행되고 있습니다. **따라서, `ko`와 `en-us` 문서 사이에 차이가 있다면, 마크업을 포함하여 `en-us` 문서를 기준으로 번역하여 `translated-content` 저장소에 기여할 수 있습니다.**

[번역 안내서](./guides/translation-guide.md), [용어 안내서](./guides/glossary-guide.md) 및 [macro 안내서](./guides/macro-guide.md)을 숙지 후 기여해주세요.

### 관리자의 편집 허용

PR 생성 시 `Create pull request` 버튼 옆에 있는 `Allow edits by maintainers`를 꼭 활성화해 주세요.

### Prettier, Husky 설정

`npm install`명령어를 실행하여 git commit 실행 전에 Prettier와 Husky 활성화해 주세요.

### PR 파일 개수

PR 생성시에 한국 리뷰어들은 라운드 로빈 방식으로 배정이 되고 있습니다. 한 리뷰어에게 너무 많은 리뷰가 몰리지 않도록 번역 PR의 경우 1개의 파일을 넘지 않는 것을 권장합니다.

사소한 변화 및 일괄적인 작업 PR에 대해서는 30개의 파일을 넘지 않는 것을 권장합니다.

### PR 규칙

- `ko-locale`에 존재하지 않는 새로운 파일에 대한 번역을 진행할 때, **파일 전체 번역** 을 원칙으로 합니다. (단, [CORS][] 와 같이 분량이 많은 파일에 대해서는 부분 번역을 허용합니다. 이때, 번역되지 않은 부분은 `en-us locale` 원본으로 대체합니다.)
- `PR`의 `Merge` 우선 순위는 관련 이슈에서 가장 처음 언급된 `PR`이 병합 우선권을 갖습니다. 리뷰어는 우선 순위가 있는 PR을 먼저 병합하는것을 원칙으로 합니다. 따라서, 번역을 진행하기 전에, `PR`과 관련된 이슈가 없다면 이슈를 생성하는 것을 권장합니다. [ko-locale PR 목록](https://github.com/mdn/translated-content/pulls?q=is%3Apr+is%3Aopen+label%3Al10n-ko+)
- 위 규칙들로 우선 순위를 정하기 힘든 경우 리뷰어는 기여자에게 충돌 해결을 요청 드릴 수 있습니다. 이 경우에는 충돌 해결 후 병합을 진행합니다.

### ko-locale 현황판

어디서부터 기여해야 될지 모르겠다면 현황판에 등록된 `Level 0`, `Level 1`, `Level 2` 각자 MDN의 이해도에 맞는 이슈를 처리해보세요! 새로운 이슈를 제보하는 것도 기여에 큰 도움이 됩니다.

- [ko-locale 현황판](https://github.com/mdn/translated-content/projects/2)

첫 기여자분들을 위해 다음 [issue 827](https://github.com/mdn/translated-content/issues/827)에 기여 방법을 작성했습니다. 참고해주세요.

## yari 빠른 사용법

yari 가 content repo에 내장돼있습니다. 세부 절차는 [다음 링크](https://github.com/mdn/yari?tab=readme-ov-file#quickstart)를 참고해주세요.

1. [content](https://github.com/mdn/content)와 (Fork된 본인 레포의) [translated-content](https://github.com/mdn/translated-content)를 클론합니다.
2. content 폴더에 들어가서 `npm install`을 통해 yari 등 필요한 패키지를 다운받습니다.
3. content 폴더 root에 .env 파일을 추가합니다. (translated-content/files 경로 추가, vscode editor의 경우 `EDITOR=code` 추가)

   ```
   CONTENT_TRANSLATED_ROOT=/path/to/translated-content/files
   EDITOR=code
   ```

4. `npm start`

다음과 같이 진행하면 아래와 같이 실시간으로 반영사항을 확인할 수 있습니다.
![image](https://github.com/mdn/translated-content/assets/23524849/c0247523-a8d2-4279-b17e-1156c15d08ce)

## 여러 안내서

안내서는 기여 과정을 원활하고 효율적으로 만드는 데 매우 유용합니다. 기여하기 전에 다음 안내서들을 주의 깊게 읽어주세요.

- [번역 안내서](./guides/translation-guide.md)
- [메타 데이터 안내서](./guides/meta-data-guide.md)
- [용어 안내서](./guides/glossary-guide.md)
- [macro 안내서](./guides/macro-guide.md)
- [github actions 안내서](./guides/github-actions-guide.md)
- [기타 안내서](./guides/etc-guide.md)

다음은 리뷰어를 위한 안내서입니다.

- [MDN yari-content-ko 팀 안내서](./guides/organizer-guide.md)

다음은 보관된 안내서입니다.

- [마크다운 변환 안내서](./guides/archived/markdown-conversion-guide.md)
- [HTML 번역 안내서](./guides/archived/html-guide.md)

## 자주 묻는 질문

[FAQ](./faq.md) 참고 부탁드립니다.

## 맺음말

번역 작업에 대한 절대적 기준을 설정하는 것도 어렵고, 올바른 언어 사용을 위한 절대적 기준을 마련하는 것도 어렵습니다. 따라서, 위의 원칙과 문제에 직면했을 때 큰 부담을 느끼지 않으셨으면 좋겠습니다. 궁금한 점이 있으시면 현지 번역팀에 부담없이 문의 해주시기 바랍니다.

번역을 보내 주시면 검토자가 디버깅을 돕고 부주의 한 부분이 무엇인지 알아낼 것입니다. 문제가 해결되면 번역을 병합합니다.

번역에 직접 기여할 준비가 되지 않은 경우에는 문제가되지 않습니다. MDN에서 결함이있는 번역을 찾아 issue를 통해 알릴 수 있습니다. 또는, 너무 어렵지 않고 해결되지 않은 문제를 찾아서 해결해보세요. 이것은 번역 기여의 첫 단계를 수행하는 비교적 간단한 방법입니다. 여러분의 기여를 진심으로 환영합니다.

[CORS]: https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS

---
# Source: faq.md
---
# 자주 묻는 질문

**1. 한국어로된 MDN 사이트는 못보나요?**

<https://developer.mozilla.org/en-US/docs/Web/HTML> 와같이 영문 페이지라면 중간에 en-US만 <https://developer.mozilla.org/ko/docs/Web/HTML> 와같이 ko로 바꿔주시면 번역본으로 보실 수 있습니다.

페이지가 존재하지 않는 경우 번역을 통해 기여를 하실 수 있습니다. 한국 페이지로 노출되더라도 동일한 방법으로 영문 페이지로 전환하실 수 있습니다.

**2. MDN 강의를 보면서 공부를 하고 있는데 다음과 같은 문장을 보게 되었습니다. 번역이 이상합니다.**

MDN 문서의 편집이 자유로운 특정 기간으로 인해 이상한 번역이 많습니다. PR이나 issue 생성 혹은 직접적인 기여로 해당 페이지를 수정하실 수 있습니다.

**3. 제가 초보라서 번역에 어떻게 기여하는지, 또 따라야 할 공식 지침 같은 것이 있는지 몰라서 손을 못 대고 있는 상황입니다.**

단순한 제보는 <https://github.com/mdn/translated-content/issues> 에서 **New issue를** 통해 제보 할 수 있습니다. 직접 문제를 해결하는 것을 원하신다면, <https://github.com/mdn/translated-content/issues/827> 의 절차를 참고하여 진행하실 수 있습니다.

**4. Issue의 라벨은 어떻게 붙이나요?**

라벨은 Git Action으로 [labeler.yml](https://github.com/mdn/translated-content/blob/main/.github/labeler.yml) 설정 파일을 통해 자동으로 PR을 생성하여 리뷰 요청 시 붙여지고 있습니다. label을 붙이는 권한은 `@mdn/ko-content` 팀에게 있으므로, 오류가 있다면 배정 받은 리뷰어에게 말씀드려서 해결하실 수 있습니다.

**5. content(en) 레포에는 index.md 파일로 저장되어 있는데, translated-content(ko) 레포에는 index.html 으로 되어 있습니다. 이런 경우에는 translated-content 레포의 index.html 파일이 번역된 index.md 파일로 교체되어도 되는건가요? 꼭 .html 포멧을 지켜야 한다 같은 규칙이 있는지 궁금합니다.**

2021년 10월 17일 기준 html 형식에서 md 형식으로 옮겨가고 있는 과도기에 있습니다. 자세한 내용은 [다음 링크](https://egas.tistory.com/m/52)를 참고해주세요.

> 2022.11월부터 모든 .html 파일들이 .md 파일로 변환 되었습니다. (참고: [[MDN] Markdown 변환 완료 및 앞으로의 방향성](https://egas.tistory.com/168))

현재는 md 확장자만 사용해서 기여 부탁드립니다.

---
# Source: Web_HTTP_Headers_Set-Cookie.md
---
---
title: Set-Cookie
slug: Web/HTTP/Headers/Set-Cookie
---

**`Set-Cookie`** HTTP 응답 헤더는 서버에서 사용자 브라우저에 쿠키를 전송하기 위해 사용됩니다.

자세한 정보를 보려면 [HTTP cookies](/ko/docs/Web/HTTP/Cookies)에 수록된 가이드를 읽으세요.

<table class="properties">
  <tbody>
    <tr>
      <th scope="row">Header type</th>
      <td>{{Glossary("Response header")}}</td>
    </tr>
    <tr>
      <th scope="row">{{Glossary("Forbidden header name")}}</th>
      <td>no</td>
    </tr>
  </tbody>
</table>

## 문법

```
Set-Cookie: <cookie-name>=<cookie-value>
Set-Cookie: <cookie-name>=<cookie-value>; Expires=<date>
Set-Cookie: <cookie-name>=<cookie-value>; Max-Age=<non-zero-digit>
Set-Cookie: <cookie-name>=<cookie-value>; Domain=<domain-value>
Set-Cookie: <cookie-name>=<cookie-value>; Path=<path-value>
Set-Cookie: <cookie-name>=<cookie-value>; Secure
Set-Cookie: <cookie-name>=<cookie-value>; HttpOnly

Set-Cookie: <cookie-name>=<cookie-value>; SameSite=Strict
Set-Cookie: <cookie-name>=<cookie-value>; SameSite=Lax

// Multiple directives are also possible, for example:
Set-Cookie: <cookie-name>=<cookie-value>; Domain=<domain-value>; Secure; HttpOnly
```

## 디렉티브

- `<cookie-name>=<cookie-value>`
  - : 쿠키는 "이름-값" 페어로 시작됩니다.
    - `<cookie-name>` 는 제어 문자 및 공백, 탭(\t)를 제외한 아스키 문자로 구성되어야 합니다. 또한, "( ) < > @ , ; : \ " / \[ ] ? = { }" 같은 문자도 포함할 수 없습니다.
    - A `<cookie-value>` 는 필요하다면 쌍 따운표로 묶여질 수 있고 아스키 코드 문자로 구성되어야 하고, `<cookie-name>`처럼 제어 문자, 공백, 쌍 따운표, 콤마, 세미콜론, 역 슬래쉬(\\)는 사용할 수 없습니다. **엔코딩**: 쿠기 값에 대해서 URL 엔코딩을 사용하는 구현 기법들이 많지만, RFC 명세에서 요구하는 것은 아닙니다. 단지, \<cookie-value>에 허용된 문자에 대한 요구사항을 만족시킬 뿐이죠.
    - **`__Secure-` 프리픽스**: `__Secure-` (대쉬는 프리픽스의 일부입니다)로 시작되는 쿠키 이름은 반드시 `secure` 플래그가 설정되어야 하고, 보안 페이지(HTTPS)여야 합니다.
    - **`__Host-` 프리픽스**: `__Host-` 로 시작되는 쿠키들은 `secure` 플래그가 설정되어야 하며, 마찬가지로 보안 페이지(HTTPS)여야 하고, 도메인이 지정되지 않아야 합니다. (따라서 서브 도메인에 쿠키를 공유할 수 없습니다) 그리고, 경로는 반드시 "/"여야 합니다.

- Expires=\<date> {{optional_inline}}
  - : HTTP 타임스템프로 기록된 쿠키의 최대 생존 시간(수명). 세부 형태를 확인하려면 {{HTTPHeader("Date")}}를 참조하세요. 지정되지 않았다면, **세션 쿠키**로서 취급되며, 클라이언트가 종료될 때 파기 됩니다. 그러나 많은 웹 브라우져에서 세션이라고 불리는 기능(그러니까 모든 탭을 기억했다가 브라우져를 다시 켜면 복구된다던지 하는 기능)을 구현합니다. 쿠키들 또한 함께 복원되므로, 정확히 말해서 브라우져를 닫은 적이 없는 게 되는 것이죠.

    만료 시간이 지정되면, 시간 및 날자로 이뤄진 값은 서버가 아니라 클라이언트에 상대적인 값으로 취급됩니다.

- Max-Age=\<number> {{optional_inline}}
  - : 쿠키가 만료될 때 까지의 시간 (초 단위). 0 또는 음수가 지정되면 해당 쿠키는 즉시 만료되며, 오래된 브라우저(ie6, ie7 그리고 ie8)은 이 헤더를 지원하지 않습니다. 다른 브라우저들은 둘 다(`Expires` 와 `Max-Age)` 지정되었을 때 `Max-Age` 값을 더 우선시합니다.
- Domain=\<domain-value> {{optional_inline}}
  - : 쿠키가 적용되어야 하는 호스트를 지정. 지정되어 있지 않으면 현재 문서 URI를 기준으로 적용됩니다만, 서브 도메인을 포함하지 않습니다. 이전의 설계와 달리, 도메인의 선두에 위치한 점들은 무시됩니다. 도메인이 지정되면, 서브도메인들은 항상 포함됩니다.
- Path=\<path-value> {{optional_inline}}
  - : 쿠키 헤더를 보내기 전에 요청 된 리소스에 있어야하는 URL 경로를 나타냅니다. % x2F ( "/") 문자는 디렉토리 구분 기호로 해석되며 하위 디렉토리도 일치합니다 (예: path=/docs, "/docs", "/docs/Web/"또는 "/docs/Web/HTTP "가 모두 일치합니다).
- Secure {{optional_inline}}
  - : 보안 쿠키들은 서버에서 요청이 SSL을 사용하며, HTTPS 프로토콜을 사용할 때에만 전송됩니다. 그러나 기밀 정보나 민감한 정보들은 HTTP 쿠키에 보관되거나 그걸로 전송되어선 안됩니다. 왜냐하면, 그 전체 메커니즘이 본질적으로 보안이 결여되어 있고, 거기 들어있는 어떤 정보도 암호화되지 않기 때문입니다.

    > **참고:** **노트:** 비 보안 사이트(`http:`)들은 "보안" 쿠키를 더이상 설정할 수 없습니다(Chrome 52+ 및 Firefox 52+).

- HttpOnly {{optional_inline}}
  - : HTTP-only cookies aren't accessible via JavaScript through the property, the {{domxref("XMLHttpRequest")}} and {{domxref("Request")}} APIs to mitigate attacks against cross-site scripting ({{Glossary("XSS")}}).
- SameSite=Strict
  SameSite=Lax {{optional_inline}} {{experimental_inline}}
  - : Allows servers to assert that a cookie ought not to be sent along with cross-site requests, which provides some protection against cross-site request forgery attacks ({{Glossary("CSRF")}}).

## Examples

### Session cookie

Session cookies will get removed when the client is shut down. They don't specify the `Expires` or `Max-Age` directives. Note that web browser have often enabled session restoring.

```
Set-Cookie: sessionid=38afes7a8; HttpOnly; Path=/
```

### Permanent cookie

Instead of expiring when the client is closed, permanent cookies expire at a specific date (`Expires`) or after a specific length of time (`Max-Age`).

```
Set-Cookie: id=a3fWa; Expires=Wed, 21 Oct 2015 07:28:00 GMT; Secure; HttpOnly
```

### Invalid domains

A cookie belonging to a domain that does not include the origin server [should be rejected by the user agent](https://tools.ietf.org/html/rfc6265#section-4.1.2.3). The following cookie will be rejected if it was set by a server hosted on originalcompany.com.

```
Set-Cookie: qwerty=219ffwef9w0f; Domain=somecompany.co.uk; Path=/; Expires=Wed, 30 Aug 2019 00:00:00 GMT
```

### Cookie prefixes

Cookies names with the prefixes `__Secure-` and `__Host-` can be used only if they are set with the `secure` directive from a secure (HTTPS) origin. In addition, cookies with the `__Host-` prefix must have a path of "/" (the entire host) and must not have a domain attribute. For clients that don't implement cookie prefixes, you cannot count on having these additional assurances and the cookies will always be accepted.

```
// Both accepted when from a secure origin (HTTPS)
Set-Cookie: __Secure-ID=123; Secure; Domain=example.com
Set-Cookie: __Host-ID=123; Secure; Path=/

// Rejected due to missing Secure directive
Set-Cookie: __Secure-id=1

// Rejected due to the missing Path=/ directive
Set-Cookie: __Host-id=1; Secure

// Rejected due to setting a domain
Set-Cookie: __Host-id=1; Secure; Path=/; domain=example.com
```

## 명세서

{{Specifications}}

## 브라우저 호환성

{{Compat}}

## Compatibility notes

- Starting with Chrome 52 and Firefox 52, insecure sites (`http:`) can't set cookies with the "secure" directive anymore.

## See also

- [HTTP cookies](/ko/docs/Web/HTTP/Cookies)
- {{HTTPHeader("Cookie")}}
- {{domxref("Document.cookie")}}

---
# Source: Web_HTML_Element_input.md
---
---
title: "<input>: 입력 요소"
slug: Web/HTML/Element/input
---

{{HTMLSidebar}}

**HTML `<input>` 요소**는 웹 기반 양식에서 사용자의 데이터를 받을 수 있는 대화형 컨트롤을 생성합니다. {{glossary("user agent", "사용자 에이전트")}}에 따라서 다양한 종류의 입력 데이터 유형과 컨트롤 위젯이 존재합니다. 입력 유형과 특성의 다양한 조합 가능성으로 인해, `<input>` 요소는 HTML에서 제일 강력하고 복잡한 요소 중 하나입니다.

{{InteractiveExample("HTML Demo: &lt;input type=&quot;text&quot;&gt;", "tabbed-shorter")}}

```html interactive-example
<label for="name">Name (4 to 8 characters):</label>

<input
  type="text"
  id="name"
  name="name"
  required
  minlength="4"
  maxlength="8"
  size="10" />
```

```css interactive-example
label {
  display: block;
  font:
    1rem "Fira Sans",
    sans-serif;
}

input,
label {
  margin: 0.4rem 0;
}
```

## `<input>` 유형

`<input>` 요소의 동작 방식은 [`type`](/ko/docs/Web/HTML/Global_attributes#type) 특성에 따라 현격히 달라지므로, 각각의 유형은 별도의 참고 문서에서 더 자세히 확인할 수 있습니다. 특성을 지정하지 않은 경우, 기본값은 `text`입니다.

가능한 유형은 다음과 같습니다.

<table class="standard-table">
  <colgroup>
    <col />
    <col style="width: 50%" />
    <col />
  </colgroup>
  <thead>
    <tr>
      <th>유형</th>
      <th>설명</th>
      <th>기본 예제</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>{{HTMLElement("input/button", "button")}}</td>
      <td>
        기본 행동을 가지지 않으며 <a href="/ko/docs/Web/HTML/Element/input#value"><code>value</code></a>을
        레이블로 사용하는 푸시 버튼.
      </td>
      <td id="examplebutton">
        <pre class="brush: html hidden notranslate">
&#x3C;input type="button" name="button" /></pre
        >
        {{EmbedLiveSample("examplebutton",200,55,"","", "nobutton")}}
      </td>
    </tr>
    <tr>
      <td>{{HTMLElement("input/checkbox", "checkbox")}}</td>
      <td>단일 값을 선택하거나 선택 해제할 수 있는 체크박스.</td>
      <td id="examplecheckbox">
        <pre class="brush: html hidden notranslate">
&#x3C;input type="checkbox" name="checkbox"/></pre
        >
        {{EmbedLiveSample("examplecheckbox",200,55,"","", "nobutton")}}
      </td>
    </tr>
    <tr>
      <td>{{HTMLElement("input/color", "color")}}</td>
      <td>
        색을 지정할 수 있는 컨트롤. 브라우저가 지원하는 경우, 활성화 시 색상
        선택기를 열어줍니다.
      </td>
      <td id="examplecolor">
        <pre class="brush: html hidden notranslate">
&#x3C;input type="color" name="color"/></pre
        >
        {{EmbedLiveSample("examplecolor",200,55,"","", "nobutton")}}
      </td>
    </tr>
    <tr>
      <td>{{HTMLElement("input/date", "date")}}</td>
      <td>
        날짜(연월일, 시간 없음)를 지정할 수 있는 컨트롤. 브라우저가 지원하는
        경우, 활성화 시 날짜를 선택할 수 있는 달력 등을 열어줍니다.
      </td>
      <td id="exampledate">
        <pre class="brush: html hidden notranslate">
&#x3C;input type="date" name="date"/></pre
        >
        {{EmbedLiveSample("exampledate",200,55,"","", "nobutton")}}
      </td>
    </tr>
    <tr>
      <td>
        {{HTMLElement("input/datetime-local", "datetime-local")}}
      </td>
      <td>
        날짜와 시간을 지정할 수 있는 컨트롤. 시간대는 지정할 수 없습니다.
        브라우저가 지원하는 경우, 활성화 시 날짜를 선택할 수 있는 달력과, 시계
        등을 열어줍니다.
      </td>
      <td id="exampledtl">
        <pre class="brush: html hidden notranslate">
&#x3C;input type="datetime-local" name="datetime-local"/></pre
        >
        {{EmbedLiveSample("exampledtl",200,55,"","", "nobutton")}}
      </td>
    </tr>
    <tr>
      <td>{{HTMLElement("input/email", "email")}}</td>
      <td>
        이메일 주소를 편집할 수 있는 필드. 텍스트 입력 필드처럼 보이지만 유효성
        검증 매개변수가 존재하며, 브라우저와 장치가 동적 키보드를 지원하는 경우
        이메일에 적합한 키보드를 보여줍니다.
      </td>
      <td id="exampleemail">
        <pre class="brush: html hidden notranslate">
&#x3C;input type="email" name="email"/></pre
        >
        {{EmbedLiveSample("exampleemail",200,55,"","", "nobutton")}}
      </td>
    </tr>
    <tr>
      <td>{{HTMLElement("input/file", "file")}}</td>
      <td>
        파일을 지정할 수 있는 컨트롤.
        <a href="/ko/docs/Web/HTML/Element/input#accept"><code>accept</code></a> 특성을 사용하면
        허용하는 파일 유형을 지정할 수 있습니다.
      </td>
      <td id="examplefile">
        <pre class="brush: html hidden notranslate">
&#x3C;input type="file" accept="image/*, text/*" name="file"/></pre
        >
        {{EmbedLiveSample("examplefile",'100%',55,"","", "nobutton")}}
      </td>
    </tr>
    <tr>
      <td>{{HTMLElement("input/hidden", "hidden")}}</td>
      <td>
        보이지 않지만 값은 서버로 전송하는 컨트롤. 오른쪽 칸에 예제가 있지만
        숨겨져서 안보이네요!
      </td>
      <td></td>
    </tr>
    <tr>
      <td>{{HTMLElement("input/image", "image")}}</td>
      <td>
        <code>src</code> 특성에 지정한 이미지로 나타나는 시각적 제출 버튼.
        이미지의 <a href="#src">src</a>를 누락한 경우
        <a href="#alt">alt</a> 특성의 텍스트를 대신 보여줍니다.
      </td>
      <td id="exampleimage">
        <pre class="brush: html hidden notranslate">
&#x3C;input type="image" name="image" src="" alt="image input"/></pre
        >
        {{EmbedLiveSample("exampleimage",200,55,"","", "nobutton")}}
      </td>
    </tr>
    <tr>
      <td>{{HTMLElement("input/month", "month")}}</td>
      <td>연과 월을 지정할 수 있는 컨트롤. 시간대는 지정할 수 없습니다.</td>
      <td id="examplemonth">
        <pre class="brush: html hidden notranslate">
&#x3C;input type="month" name="month"/></pre
        >
        {{EmbedLiveSample("examplemonth",200,55,"","", "nobutton")}}
      </td>
    </tr>
    <tr>
      <td>{{HTMLElement("input/number", "number")}}</td>
      <td>
        <p>
          숫자를 입력하기 위한 컨트롤. 스피너를 표시하고 지원되는 기본 확인을
          추가합니다. 몇몇 장치에서는 동적 키패드들과 숫자 키패드를 표시합니다.
        </p>
      </td>
      <td id="examplenumber">
        <pre class="brush: html hidden notranslate">
&#x3C;input type="number" name="number"/></pre
        >
        {{EmbedLiveSample("examplenumber",200,55,"","", "nobutton")}}
      </td>
    </tr>
    <tr>
      <td>{{HTMLElement("input/password", "password")}}</td>
      <td>
        <p>
          값이 가려진 한줄 텍스트 필드. 사이트가 안전하지 않으면 사용자에게
          경고합니다.
        </p>
      </td>
      <td id="examplepassword">
        <pre class="brush: html hidden notranslate">
&#x3C;input type="password" name="password"/></pre
        >
        {{EmbedLiveSample("examplepassword",200,55,"","", "nobutton")}}
      </td>
    </tr>
    <tr>
      <td>{{HTMLElement("input/radio", "radio")}}</td>
      <td>
        <p>
          같은 <a href="#name">name</a> 값을 가진 여러개의 선택중에서 하나의
          값을 선택하게 하는 라디오 버튼입니다.
        </p>
      </td>
      <td id="exampleradio">
        <pre class="brush: html hidden notranslate">
&#x3C;input type="radio" name="radio"/></pre
        >
        {{EmbedLiveSample("exampleradio",200,55,"","", "nobutton")}}
      </td>
    </tr>
    <tr>
      <td>{{HTMLElement("input/range", "range")}}</td>
      <td>
        <p>
          값이 가려진 숫자를 입력하는 컨트롤. 디폴트 값이 중간값인 범위 위젯으로
          표시합니다. 접속사 <a href="#min">min</a> 와
          <a href="#max">max</a> 사이에 사용되며 수용가능한 값의 범위를
          정의합니다.
        </p>
      </td>
      <td id="examplerange">
        <pre class="brush: html hidden notranslate">
&#x3C;input type="range" name="range" min="0" max="25"/></pre
        >
        {{EmbedLiveSample("examplerange",200,55,"","", "nobutton")}}
      </td>
    </tr>
    <tr>
      <td>{{HTMLElement("input/reset", "reset")}}</td>
      <td>
        양식의 내용을 디폴트값(기본값)으로 초기화하는 버튼. 권장되지 않습니다.
      </td>
      <td id="examplereset">
        <pre class="brush: html hidden notranslate">
&#x3C;input type="reset" name="reset"/></pre
        >
        {{EmbedLiveSample("examplereset",200,55,"","", "nobutton")}}
      </td>
    </tr>
    <tr>
      <td>{{HTMLElement("input/search", "search")}}</td>
      <td>
        <p>
          검색문자열을 입력하는 한줄 텍스트 필드. 줄바꿈 문자는 입력값에서
          자동으로 제거됩니다. 지원 브라우저에서 필드를 클리어하기 위해 사용되는
          삭제 아이콘이 포함됩니다. 동적 키패드들이 있는 몇몇 장치에서 엔터키
          대신에 검색 아이콘을 표시합니다.
        </p>
      </td>
      <td id="examplesearch">
        <pre class="brush: html hidden notranslate">
&#x3C;input type="search" name="search"/></pre
        >
        {{EmbedLiveSample("examplesearch",200,55,"","", "nobutton")}}
      </td>
    </tr>
    <tr>
      <td>{{HTMLElement("input/submit", "submit")}}</td>
      <td>양식을 전송하는 버튼</td>
      <td id="examplesubmit">
        <pre class="brush: html hidden notranslate">
&#x3C;input type="submit" name="submit"/></pre
        >
        {{EmbedLiveSample("examplesubmit",200,55,"","", "nobutton")}}
      </td>
    </tr>
    <tr>
      <td>{{HTMLElement("input/tel", "tel")}}</td>
      <td>
        전화번호를 입력하는 컨트롤. 몇몇 장치에서 동적 키패드들과 전화번호
        입력기를 표시한다.
      </td>
      <td id="exampletel">
        <pre class="brush: html hidden notranslate">
&#x3C;input type="tel" name="tel"/></pre
        >
        {{EmbedLiveSample("exampletel",200,55,"","", "nobutton")}}
      </td>
    </tr>
    <tr>
      <td>{{HTMLElement("input/text", "text")}}</td>
      <td>
        <p>
          디폴트 값. 한줄의 텍스트 필드입니다. 새줄 문자는 입력값으로부터
          자동으로 제거됩니다.
        </p>
      </td>
      <td id="exampletext">
        <pre class="brush: html hidden notranslate">
&#x3C;input type="text" name="text"/></pre
        >
        {{EmbedLiveSample("exampletext",200,55,"","", "nobutton")}}
      </td>
    </tr>
    <tr>
      <td>{{HTMLElement("input/time", "time")}}</td>
      <td>시간대가 없는 시간값을 입력하는 콘트롤</td>
      <td id="exampletime">
        <pre class="brush: html hidden notranslate">
&#x3C;input type="time" name="time"/></pre
        >
        {{EmbedLiveSample("exampletime",200,55,"","", "nobutton")}}
      </td>
    </tr>
    <tr>
      <td>{{HTMLElement("input/url", "url")}}</td>
      <td>
        URL을 입력하는 필드. 텍스트 입력처럼 보이지만, 검증 매개변수가 있습니다.
        동적 키보드들을 지원하는 브라우저와 장치들에 관련된 키보드가 있습니다.
      </td>
      <td id="exampleurl">
        <pre class="brush: html hidden notranslate">
&#x3C;input type="url" name="url"/></pre
        >
        {{EmbedLiveSample("exampleurl",200,55,"","", "nobutton")}}
      </td>
    </tr>
    <tr>
      <td>{{HTMLElement("input/week", "week")}}</td>
      <td>
        시간대가 없는 주-년 값과 주의 값을 구성하는 날짜를 입력하는
        컨트롤입니다.
      </td>
      <td id="exampleweek">
        <pre class="brush: html hidden notranslate">
&#x3C;input type="week" name="week"/></pre
        >
        {{EmbedLiveSample("exampleweek",200,55,"","", "nobutton")}}
      </td>
    </tr>
  </tbody>
</table>

## 속성

`<input>` 요소가 강력한 이유는 바로 다양한 속성 때문입니다. 그 중에서도, 위의 표에서 확인할 수 있는 [`type`](/ko/docs/Web/HTML/Element/input#type) 속성이 제일 중요합니다. 모든 `<input>` 요소는 유형에 상관하지 않고 {{domxref("HTMLInputElement")}} 인터페이스에 기반하므로, 기술적으로는 모든 `<input>`이 동일한 속성을 가집니다. 그러나 사실 대부분의 속성은 일부 유형에서만 효과를 보입니다. 게다가, 어떤 속성은 유형별로 그 영향이 달라집니다.

여기에서는 모든 속성값들에 대해 간략한 설명을 담은 표를 제공합니다. 이 표 다음에는 각각의 속성을 더욱 상세하게 설명하는 목록이 나오는데, 그들이 연관된 input 유형과 함께 나옵니다. 대부분의 혹은 모든 input 유형에 공통적인 속성들은 그 아래 더욱 상세하게 설명되어 있습니다. 몇몇 input 유형에만 특정하게 해당하는 속성들이나 모든 유형에 공통적으로 해당하지만 특정 유형에 사용될 때 특정한 행동양식을 나타내는 속성들은 그 유형의 해당 페이지에 대신 기술되어 있습니다. 이 요소에는 글로벌 속성들도 포함됩니다. input에 관련된 특별히 중요한 속성들은 하이라이트로 표시되었습니다.

| 특성                                              | 유형                             | 설명                                                                                  |
| ------------------------------------------------- | -------------------------------- | ------------------------------------------------------------------------------------- |
| [accept](#htmlattrdefaccept)                      | file                             | 파일을 업로드 컨트롤에서 기대하는 파일 유형을 암시                                    |
| [alt](#htmlattrdefalt)                            | image                            | 이미지 유형에 대한 대체 속성. accessibiltiy 측면에서 필요.                            |
| [autocomplete](#htmlattrdefautocomplete)          | all                              | 양식 자동생성 기능 (form autofill) 암시                                               |
| [autofocus](#htmlattrdefautofocus)                | all                              | 페이지가 로딩될때 양식 제어에 오토포커스                                              |
| [capture](#htmlattrdefcapture)                    | file                             | 파일 업로드 제어에서 input 방식에서 미디어 capture                                    |
| [checked](#htmlattrdefchecked)                    | radio, checkbox                  | 커맨드나 컨트롤이 체크 되었는지의 여부                                                |
| [dirname](#htmlattrdefdirname)                    | text, search                     | 양식 전송시 요소의 방향성을 전송할 때 양식 필드의 Name                                |
| [disabled](#htmlattrdefdisabled)                  | all                              | 양식 컨트롤이 비활성화되었는지의 여부                                                 |
| [form](#htmlattrdefform)                          | all                              | 컨트롤을 양식 요소와 연결                                                             |
| [formaction](#htmlattrdefformaction)              | image, submit                    | 양식 전송시 URL 사용하기                                                              |
| [formenctype](#htmlattrdefformenctype)            | image, submit                    | 양식의 데이터 인코딩 유형이 양식 전송시 사용될 것                                     |
| [formmethod](#htmlattrdefformmethod)              | image, submit                    | 양식 전송시 HTTP 방식을 사용                                                          |
| [formnovalidate](#htmlattrdefformnovalidate)      | image, submit                    | 양식 전송시 양식 컨트롤 확인을 무시하기                                               |
| [formtarget](#htmlattrdefformtarget)              | image, submit                    | 양식 전송시 브라우징 맥락                                                             |
| [height](#htmlattrdefheight)                      | image                            | 이미지 높이에서 `height` 속성과 같음                                                  |
| [list](#htmlattrdeflist)                          | almost all                       | datalist 자동입력 옵션의 id 속성값                                                    |
| [max](#htmlattrdefmax)                            | numeric types                    | 최대값                                                                                |
| [maxlength](#htmlattrdefmaxlength)                | password, search, tel, text, url | `value`의 최대 길이 (문자수)                                                          |
| [min](#htmlattrdefmin)                            | numeric types                    | 최소값                                                                                |
| [minlength](#htmlattrdefminlength)                | password, search, tel, text, url | `value`의 최소 길이 (문자수)                                                          |
| [multiple](#htmlattrdefmultiple)                  | email, file                      | 불리언값. 여러 값을 허용할지의 여부                                                   |
| [name](#htmlattrdefname)                          | all                              | input 양식 컨트롤의 이름. 이름/값 짝(name/value pair)의 일부로서 양식과 함께 전송된다 |
| [pattern](#htmlattrdefpattern)                    | password, text, tel              | `value` 가 유효하기 위해 일치해야 하는 패턴                                           |
| [placeholder](#htmlattrdefplaceholder)            | password, search, tel, text, url | 양식 컨트롤이 비어있는 때 양식 컨트롤에 나타나는 내용                                 |
| [readonly](/ko/docs/Web/HTML/Attributes/readonly) | almost all                       | 불리언값. 이 값은 수정이 불가능함                                                     |
| [required](/ko/docs/Web/HTML/Attributes/required) | almost all                       | 불리언값. 양식이 전송되기 위해서 반드시 입력하거나 확인이 필요한 값                   |
| [size](#htmlattrdefsize)                          | email, password, tel, text       | 컨트롤의 크기                                                                         |
| [src](#htmlattrdefsrc)                            | image                            | 이미지 출처의 주소에서 `src` 와 같은 속성                                             |
| [step](#htmlattrdefstep)                          | numeric types                    | 유효한 증분적인 (Incremental)값                                                       |
| [type](#htmlattrdeftype)                          | all                              | input 양식 컨트롤의 유형                                                              |
| [value](#htmlattrdefvalue)                        | all                              | 양식 컨트롤의 현재 값. 이름/값 짝(name/value pair)의 일부로서 양식과 함께 전송된다    |
| [width](#htmlattrdefwidth)                        | image                            | 이미지의 `width` 속성과 같다                                                          |

A few additional non-standard attributes are listed following the descriptions of the standard attributes

### 개별 속성

- `accept`
  - : Valid for the `file` input type only, the `accept` property defines which file types are selectable in a `file` upload control. See the {{HTMLElement("input/file", "file")}} input type.
- `alt`
  - : Valid for the `image` button only, the alt attribute provides alternative text for the image, displaying the value of the attribute if the image [src](#src) is missing or otherwise fails to load. See the {{HTMLElement("input/image", "image")}} input type.
- `autocomplete`
  - : **Not** a Boolean attribute, the [`autocomplete`](/ko/docs/Web/HTML/Attributes/autocomplete) attribute takes as its value a space separated string that describes what, if any, type of autocomplete functionality the input should provide. A typical implementation of autocomplete simply recalls previous values entered in the same input field, but more complex forms of autocomplete can exist. For instance, a browser could integrate with a device's contacts list to autocomplete email addresses in an email input field. See [Values](/ko/docs/Web/HTML/Attributes/autocomplete#값) for permitted values.

    The `autocomplete` attribute is valid on `hidden`, `text`, `search`, `url`, `tel`, `email`, `date`, `month`, `week`, `time`, `datetime-local`, `number`, `range`, `color` and `password`. This attribute has no effect on input types that do not return numeric or text data, being valid for all input types except `checkbox`, `radio`, `file`, or any of the button types. See [The HTML autocomplete attribute](/ko/docs/Web/HTML/Attributes/autocomplete) for additional information, including information on password security and how `autocomplete` is slightly different for `hidden` than for other input types.

- `autofocus`
  - : A Boolean attribute which, if present, indicates that the input should automatically have focus when the page has finished loading (or when the {{HTMLElement("dialog")}} containing the element has been displayed).

    > **참고:** An element with the `autofocus` attribute may gain focus before the {{domxref("DOMContentLoaded")}} event is fired.

    No more than one element in the document may have the `autofocus` attribute, and `autofocus` cannot be used on inputs of type `hidden`, because hidden inputs can't be focused. If put on more than one element, the first one with the attribute receives focus .

    > **경고:** Automatically focusing a form control can confuse visually-impaired people using screen-reading technology and people with cognitive impairments. When `autofocus` is assigned, screen-readers "teleport" their user to the form control without warning them beforehand.

    For better usability, avoid using `autofocus`. Automatically focusing on a form control can cause the page to scroll on load. The focus can also cause dynamic keyboards to display on some touch devices. While a screen reader will announce the label of the form control receiving focus, the screen reader will not announce anything before the label, and the sighted user on a small device will equally miss the context created by the preceding content.

- `capture`
  - : Introduced in the HTML Media Capture specification and valid for the `file` input type only, the `capture` attribute defines which media - microphone, video, or camera - should be used to capture a new file for upload with `file` upload control in supporting scenarios. See the {{HTMLElement("input/file", "file")}} input type.
- `checked`
  - : Valid for both `radio` and `checkbox` types, `checked` is a Boolean attribute. If present on a radio type, it indicates that that radio button is the currently selected one in the group of same-named radio buttons. If present on a `checkbox` type, it indicates that the checkbox is checked by default (when the page loads). It does _not_ indicate whether this checkbox is currently checked: if the checkbox's state is changed, this content attribute does not reflect the change. (Only the [`HTMLInputElement`'s `checked` IDL attribute](/ko/docs/Web/API/HTMLInputElement) is updated.)

    > **참고:** Unlike other input controls, a checkboxes and radio buttons value are only included in the submitted data if they are currently `checked`. If they are, the name and the value(s) of the checked controls are submitted.
    >
    > For example, if a checkbox whose `name` is `fruit` has a `value` of `cherry`, and the checkbox is checked, the form data submitted will include `fruit=cherry`. If the checkbox isn't active, it isn't listed in the form data at all. The default `value` for checkboxes and radio buttons is `on`.

- `dirname`
  - : Valid for `text` and `search` input types only, the `dirname` attribute enables the submission of the directionality of the element. When included, the form control will submit with two name/value pairs: the first being the [name](#name) and [value](#value), the second being the value of the `dirname` as the name with the value of `ltr` or `rtl` being set by the browser.

    ```
    <form action="page.html" method="post">
      <label>Fruit: <input type="text" name="fruit" dirname="fruit.dir" value="cherry"></label>
      <input type="submit"/>
    </form>
    <!-- page.html?fruit=cherry&fruit.dir=ltr -->
    ```

    When the form above is submitted, the input cause both the `name` / `value` pair of `fruit=cherry` and the `dirname` / direction pair of `fruit.dir=ltr` to be sent.

- `disabled`
  - : A Boolean attribute which, if present, indicates that the user should not be able to interact with the input. Disabled inputs are typically rendered with a dimmer color or using some other form of indication that the field is not available for use.

    Specifically, disabled inputs do not receive the [`click`](/ko/docs/Web/API/Element/click_event) event, and disabled inputs are not submitted with the form.

    > **참고:** Although not required by the specification, Firefox will by default [persist the dynamic disabled state](https://stackoverflow.com/questions/5985839/bug-with-firefox-disabled-attribute-of-input-not-resetting-when-refreshing) of an `<input>` across page loads. Use the [`autocomplete`](/ko/docs/Web/HTML/Element/input#autocomplete) attribute to control this feature.

- `form`
  - : A string specifying the {{HTMLElement("form")}} element with which the input is associated (that is, its **form owner**). This string's value, if present, must match the [`id`](/ko/docs/Web/HTML/Global_attributes#id) of a `<form>` element in the same document. If this attribute isn't specified, the `<input>` element is associated with the nearest containing form, if any.

    The `form` attribute lets you place an input anywhere in the document but have it included with a form elsewhere in the document.

    > **참고:** An input can only be associated with one form.

- `formaction`
  - : Valid for the `image` and `submit` input types only. See the {{HTMLElement("input/submit", "submit")}} input type for more information.
- `formenctype`
  - : Valid for the `image` and `submit` input types only. See the {{HTMLElement("input/submit", "submit")}} input type for more information.
- `formmethod`
  - : Valid for the `image` and `submit` input types only. See the {{HTMLElement("input/submit", "submit")}} input type for more information.
- `formnovalidate`
  - : Valid for the `image` and `submit` input types only. See the {{HTMLElement("input/submit", "submit")}} input type for more information.
- `formtarget`
  - : Valid for the `image` and `submit` input types only. See the {{HTMLElement("input/submit", "submit")}} input type for more information.
- `height`
  - : Valid for the `image` input button only, the `height` is the height of the image file to display to represent the graphical submit button. See the {{HTMLElement("input/image", "image")}} input type.
- `id`
  - : Global attribute valid for all elements, including all the input types, it defines a unique identifier (ID) which must be unique in the whole document. Its purpose is to identify the element when linking. The value is used as the value of the {{htmlelement('label')}}'s `for` attribute to link the label with the form control. See the [the label element](#the_label_element) below.
- `inputmode`
  - : Global value valid for all elements, it provides a hint to browsers as to the type of virtual keyboard configuration to use when editing this element or its contents. Values include none
    `text`, `tel`, `url`, `email`, `numeric`, `decimal`, and `search`
- `list`
  - : The values of the list attribute is the {{domxref("Element.id", "id")}} of a {{HTMLElement("datalist")}} element located in the same document. The `<datalist>` provides a list of predefined values to suggest to the user for this input. Any values in the list that are not compatible with the [`type`](/ko/docs/Web/HTML/Element/input#type) are not included in the suggested options. The values provided are suggestions, not requirements: users can select from this predefined list or provide a different value.

    ```html hidden
    <datalist id="colorsxx">
      <option>#ff0000</option>
      <option>#ee0000</option>
      <option>#dd0000</option>
      <option>#cc0000</option>
      <option>#bb0000</option>
    </datalist>
    <datalist id="numbersxx">
      <option>0</option>
      <option>2</option>
      <option>4</option>
      <option>8</option>
      <option>16</option>
      <option>32</option>
      <option>64</option>
    </datalist>
    <datalist id="fruitsxx">
      <option>cherry</option>
      <option>banana</option>
      <option>mango</option>
      <option>orange</option>
      <option>blueberry</option>
    </datalist>
    <datalist id="urlsxx">
      <option>https://developer.mozilla.org</option>
      <option>https://caniuse.com/</option>
      <option>https://mozilla.com</option>
      <option>https://mdn.github.io</option>
      <option>https://www.youtube.com/user/firefoxchannel</option>
    </datalist>

    <p>
      <label for="textx">Text</label>
      <input type="text" list="fruitsxx" id="textx" />
    </p>
    <p>
      <label for="colorx">Color</label>
      <input type="color" list="colorsxx" id="colorx" />
    </p>
    <p>
      <label for="rangex">Range</label>
      <input type="range" min="0" max="64" list="numbersxx" id="rangex" />
    </p>
    <p>
      <label for="numberx">Number</label>
      <input type="number" min="0" max="64" list="numbersxx" id="numberx" />
    </p>
    <p>
      <label for="urlx">URL</label> <input type="url" list="urlsxx" id="urlx" />
    </p>
    ```

    {{EmbedLiveSample("datalist",400,275,"","", "nobutton")}}

    It is valid on `text`, `search`, `url`, `tel`, `email`, `date`, `month`, `week`, `time`, `datetime-local`, `number`, `range`, and `color.`Per the specifications, the `list` attribute is not supported by the `hidden`, `password`, `checkbox`, `radio`, `file`, or any of the button types.

    Depending on the browser, the user may see a custom color palette suggested, tic marks along a range, or even a input that opens like a select but allows for non-listed values. Check out the [browser compatibility table](/ko/docs/Web/HTML/Element/datalist#Browser_compatibility) for the other input types.

    See the {{htmlelement('datalist')}} element.

- [`max`](/ko/docs/Web/HTML/Attributes/max)
  - : Valid for `date`, `month`, `week`, `time`, `datetime-local`, `number`, and `range`, it defines the greatest value in the range of permitted values. If the [`value`](/ko/docs/Web/HTML/Element/input#value) entered into the element exceeds this, the element fails [constraint validation](/ko/docs/Web/Guide/HTML/HTML5/Constraint_validation). If the value of the `max` attribute isn't a number, then the element has no maximum value.
- `maxlength`
  - : Valid for `text`, `search`, `url`, `tel`, `email`, and `password`, it defines the maximum number of characters (as UTF-16 code units) the user can enter into the field. This must be an integer value 0 or higher. If no `maxlength` is specified, or an invalid value is specified, the field has no maximum length. This value must also be greater than or equal to the value of `minlength`.

    The input will fail [constraint validation](/ko/docs/Web/Guide/HTML/HTML5/Constraint_validation) if the length of the text entered into the field is greater than `maxlength` UTF-16 code units long. By default, browsers prevent users from entering more characters than allowed by the `maxlength` attribute. See [Client-side validation](#client-side_validation) for more information.

- `min`
  - : Valid for `date`, `month`, `week`, `time`, `datetime-local`, `number`, and `range`, it defines the most negative value in the range of permitted values. If the [`value`](/ko/docs/Web/HTML/Element/input#value) entered into the element is less than this this, the element fails [constraint validation](/ko/docs/Web/Guide/HTML/HTML5/Constraint_validation). If the value of the `min` attribute isn't a number, then the element has no minimum value.

    This value must be less than or equal to the value of the `max` attribute. If the `min` attribute is present by is not specified or is invalid, no `min` value is applied. If the `min` attribute is valid and a non-empty value is less than the minimum allowed by the `min` attribute, constraint validation will prevent form submission. See [Client-side validation](#client-side_validation) for more information.

- `minlength`
  - : Valid for `text`, `search`, `url`, `tel`, `email`, and `password`, it defines the minimum number of characters (as UTF-16 code units) the user can enter into the entry field. This must be an non-negative integer value smaller than or equal to the value specified by `maxlength`. If no `minlength` is specified, or an invalid value is specified, the input has no minimum length.

    The input will fail [constraint validation](/ko/docs/Web/Guide/HTML/HTML5/Constraint_validation) if the length of the text entered into the field is fewer than `minlength` UTF-16 code units long, preventing form submission. See [Client-side validation](#client-side_validation) for more information.

- `multiple`
  - : The Boolean multiple attribute, if set, means the user can enter comma separated email addresses in the email widget or can choose more than one file with the `file` input. See the {{HTMLElement("input/email", "email")}} and {{HTMLElement("input/file", "file")}} input type.
- `name`
  - : A string specifying a name for the input control. This name is submitted along with the control's value when the form data is submitted.

##### What's in a name

Consider the `name` a required attribute (even though it's not). If an input has no `name` specified, or `name` is empty, the input's value is not submitted with the form. (Disabled controls, unchecked radio buttons, unchecked checkboxes, and reset buttons are also not sent.)

There are two special cases:

1. `_charset_` : If used as the name of an `<input>` element of type [`hidden`](/ko/docs/Web/HTML/Element/input/hidden), the input's `value` is automatically set by the [user agent](/ko/docs/Glossary/user_agent) to the character encoding being used to submit the form.
2. `isindex`: For historical reasons, the name [`isindex`](https://html.spec.whatwg.org/multipage/form-control-infrastructure.html#attr-fe-name) is not allowed.

##### `name` and radio buttons

The [name](#name) attribute creates a unique behavior for radio buttons.

Only one radio button in a same-named group of radio buttons can be checked at a time. Selecting any radio button in that group automatically deselects any currently-selected radio button in the same group. The value of that one checked radio button is sent along with the name if the form is submitted,

When tabbing into a series of same-named group of radio buttons, if one is checked, that one will receive focus. If they aren't grouped together in source order, if one of the group is checked, tabbing into the group starts when the first one in the group is encountered, skipping all those that aren't checked. In other words, if one is checked, tabbing skips the unchecked radio buttons in the group. If none are checked, the radio button group receives focus when the first button in the same name group is reached.

Once one of the radio buttons in a group has focus, using the arrow keys will navigate thru all the radio buttons of the same name, even if the radio buttons are not grouped together in the source order.

##### {{domxref("HTMLFormElement.elements")}}

When an input element is given a `name`, that name becomes a property of the owning form element's {{domxref("HTMLFormElement.elements")}} property. If you have an input whose `name` is set to `guest` and another whose `name` is `hat-size`, the following code can be used:

```js
let form = document.querySelector("form");

let guestName = form.elements.guest;
let hatSize = form.elements["hat-size"];
```

When this code has run, `guestName` will be the {{domxref("HTMLInputElement")}} for the `guest` field, and `hatSize` the object for the `hat-size` field.

> **경고:** You should avoid giving form elements a `name` that corresponds to a built-in property of the form, since you would then override the predefined property or method with this reference to the corresponding input.

- `pattern`
  - : The `pattern` attribute, when specified, is a regular expression that the input's [`value`](/ko/docs/Web/HTML/Global_attributes#value) must match in order for the value to pass [constraint validation](/ko/docs/Web/Guide/HTML/HTML5/Constraint_validation). It must be a valid JavaScript regular expression, as used by the {{jsxref("RegExp")}} type, and as documented in our [guide on regular expressions](/ko/docs/Web/JavaScript/Guide/Regular_Expressions); the `'u'` flag is specified when compiling the regular expression, so that the pattern is treated as a sequence of Unicode code points, instead of as ASCII. No forward slashes should be specified around the pattern text.

    If the `pattern` attribute is present but is not specified or is invalid, no regular expression is applied and this attribute is ignored completely. If the pattern attribute is valid and a non-empty value does not match the pattern, constraint validation will prevent form submission.

    > **참고:** **Tip:** If using the `pattern` attribute, inform the user about the expected format by including explanatory text nearby. You can also include a [`title`](/ko/docs/Web/HTML/Element/input#title) attribute to explain what the requirements are to match the pattern; most browsers will display this title as as a tooltip The visible explanation is required for accessibilty. The tooltip is an enhancement.

    See [Client-side validation](#client-side_validation) for more information.

- `placeholder`
  - : The `placeholder` attribute is a string that provides a brief hint to the user as to what kind of information is expected in the field. It should be a word or short phrase that demonstrates the expected type of data, rather than an explanatory message. The text _must not_ include carriage returns or line feeds.

    > **참고:** The `placeholder` attribute is not as semantically useful as other ways to explain your form, and can cause unexpected technical issues with your content. See [Labels and placeholders](/ko/docs/Web/HTML/Element/input#labels) for more information.

- `readonly`
  - : A Boolean attribute which, if present, indicates that the user should not be able to edit the value of the input. The `readonly` attribute is supported `text`, `search`, `url`, `tel`, `email`, `date`, `month`, `week`, `time`, `datetime-local`, `number`, and `password` input types.

    See the [HTML attribute: `readonly`](/ko/docs/Web/HTML/Attributes/readonly) for more information.

- `required`
  - : `required` is a Boolean attribute which, if present, indicates that the user must specify a value for the input before the owning form can be submitted. The `required` attribute is supported `text`, `search`, `url`, `tel`, `email`, `date`, `month`, `week`, `time`, `datetime-local`, `number`, `password`, `checkbox`, `radio`, and `file`.

    See [Client-side validation](#client-side_validation) and the [HTML attribute: `required`](/ko/docs/Web/HTML/Attributes/required) for more information.

- `size`
  - : Valid for `email`, `password`, `tel`, and text `input` types only. Specifies how much of the input is shown. Basically creates same result as setting CSS `width` property with a few specialities. The actual unit of the value depends on the input type. For password and text it's number of characters (or `em` units) and `pixel`s for others. CSS width takes precedence over size attribute.
- `src`
  - : Valid for the `image` input button only, the `src` is string specifying the URL of the image file to display to represent the graphical submit button. See the {{HTMLElement("input/image", "image")}} input type.
- `step`
  - : Valid for the numeric input types, including `number`, date/time input types, and `range`, the [`step`](/ko/docs/Web/HTML/Attributes/step) attribute is a number that specifies the granularity that the value must adhere to.

    If not explicitly included, `step` defaults to 1 for `number` and `range`, and 1 unit type (second, week, month, day) for the date/time input types. The value can must be a positive number - integer or float — or the special value `any`, which means no stepping is implied, and any value is allowed (barring other constraints, such as [`min`](#min) and [`max`](#max)).

    If `any` is not explicity set, valid values for the `number`, date/time input types, and `range` input types are equal to the basis for stepping - the [`min`](#min) value and increments of the step value, up to the [`max`](#max) value, if specified. For example, if we have `<input type="number" min="10" step="2">` any even integer, 10 or great, is valid. If omitted, `<input type="number">`, any integer is valid, but floats, like 4.2, are not valid, as `step` defaults to 1. For 4.2 to be valid, `step` would have had to be set to `any`, 0.1, 0.2, or any the min value would have had to be a number ending in .2, such as `<input type="number" min="-5.2">`

    > **참고:** When the data entered by the user doesn't adhere to the stepping configuration, the value is considered invalid in contraint validation and will match the :invalid pseudoclass

    The default stepping value for `number` inputs is 1, allowing only integers to be entered, _unless_ the stepping base is not an integer. The default stepping value for `time` is 1 second, with 900 being equal to 15 minutes.

    See [Client-side validation](#client-side_validation) for more information.

- `tabindex`
  - : Global attribute valid for all elements, including all the input types, an integer attribute indicating if the element can take input focus (is focusable), if it should participate to sequential keyboard navigation. As all input types except for input of type hidden are focusable, this attribute should not be used on form controls, because doing so would require the management of the focus order for all elements within the document with the risk of harming usability and accessibility if done incorrectly.
- `title`
  - : Global attribute valid for all elements, including all input types, containing a text representing advisory information related to the element it belongs to. Such information can typically, but not necessarily, be presented to the user as a tooltip. The title should NOT be used as the primary explanation of the purpose of the form control. Instead, use the {{htmlelement('label')}} element with a `for` attribute set to the form control's [`id`](#id) attribute. See [Labels](#labels) below.
- `type`
  - : A string specifying the type of control to render. For example, to create a checkbox, a value of `checkbox` is used. If omitted (or an unknown value is specified), the input type `text` is used, creating a plaintext input field.

    Permitted values are listed in [\<input> types](#input_types) above.

- `value`
  - : The input control's value. When specified in the HTML, this is the initial value, and from then on it can be altered or retrieved at any time using JavaScript to access the respective {{domxref("HTMLInputElement")}} object's `value` property. The `value` attribute is always optional, though should be considered mandatory for `checkbox`, `radio`, and `hidden`.
- `width`
  - : Valid for the `image` input button only, the `width` is the width of the image file to display to represent the graphical submit button. See the {{HTMLElement("input/image", "image")}} input type.

## 예제

### A simple input box

```html
<!-- A basic input -->
<input type="text" name="input" value="Type here" />
```

### A common use-case scenario

```html
<!-- A common form that includes input tags -->
<form action="getform.php" method="get">
  <label>First name: <input type="text" name="first_name" /></label><br />
  <label>Last name: <input type="text" name="last_name" /></label><br />
  <label>E-mail: <input type="email" name="user_email" /></label><br />
  <input type="submit" value="Submit" />
</form>
```

## 명세

{{Specifications}}

## 브라우저 호환성

{{Compat}}

---
# Source: Web_JavaScript_Reference_Global_Objects_RegExp_exec.md
---
---
title: RegExp.prototype.exec()
slug: Web/JavaScript/Reference/Global_Objects/RegExp/exec
---

{{JSRef}}

**`exec()`** 메서드는 주어진 문자열에서 일치 탐색을 수행한 결과를 배열 혹은 {{jsxref("null")}}로 반환합니다.

JavaScript {{jsxref("RegExp")}} 객체는 {{jsxref("RegExp.global", "global")}} 또는 {{jsxref("RegExp.sticky", "sticky")}} 플래그를 설정(`/foo/g`, `/foo/y` 등)한 경우 이전 일치의 인덱스를 저장하므로 **상태를 가지고**(stateful) 있습니다. 이를 내부적으로 사용하여, {{jsxref("String.prototype.match()")}}와는 다르게 (캡처 그룹을 포함한) 문자열 내의 일치 다수를 반복해 순회할 수 있습니다.

(캡처 그룹을 포함한) 문자열 내의 다수 일치를 수행할 수 있는 보다 간편한 신규 메서드, {{jsxref("String.prototype.matchAll()")}}이 제안된 상태입니다.

단순히 `true`/`false`가 필요한 경우 {{jsxref("RegExp.prototype.test()")}} 메서드 혹은 {{jsxref("String.prototype.search()")}}를 사용하세요.

{{InteractiveExample("JavaScript Demo: RegExp.prototype.exec()")}}

```js interactive-example
const regex1 = RegExp("foo*", "g");
const str1 = "table football, foosball";
let array1;

while ((array1 = regex1.exec(str1)) !== null) {
  console.log(`Found ${array1[0]}. Next starts at ${regex1.lastIndex}.`);
  // Expected output: "Found foo. Next starts at 9."
  // Expected output: "Found foo. Next starts at 19."
}
```

## 구문

```js
regexObj.exec(str);
```

### 매개변수

- `str`
  - : 정규 표현식 검색을 수행할 대상 문자열.

### 반환 값

정규 표현식이 일치하면, `exec()` 메서드는 배열(추가 속성 `index`와 `input` 포함, 아래 설명을 참고하세요)을 반환하고, 정규 표현식 객체의 {{jsxref("RegExp.lastIndex", "lastIndex")}} 속성을 업데이트합니다. 반환하는 배열은 일치한 텍스트를 첫 번째 원소로, 각각의 괄호 캡처 그룹을 이후 원소로 포함합니다.

정규표현식 검색에 실패하면, `exec()` 메서드는 {{jsxref("null")}}을 반환하고 {{jsxref("RegExp.lastIndex", "lastIndex")}}를 `0`으로 설정합니다.

## 설명

다음과 같은 예제를 고려해보세요.

```js
// Match "quick brown" followed by "jumps", ignoring characters in between
// Remember "brown" and "jumps"
// Ignore case
let re = /quick\s(brown).+?(jumps)/gi;
let result = re.exec("The Quick Brown Fox Jumps Over The Lazy Dog");
```

다음의 표는 이 스크립트의 결과에 대해 보여줍니다.

<table class="fullwidth-table standard-table">
  <thead>
    <tr>
      <th scope="row">객체</th>
      <th scope="col">속성/인덱스</th>
      <th scope="col">설명</th>
      <th scope="col">예제</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th colspan="1" rowspan="4" scope="row" style="vertical-align: top">
        <code>result</code>
      </th>
      <td><code>[0]</code></td>
      <td>일치한 전체 문자.</td>
      <td><code>"Quick Brown Fox Jumps"</code></td>
    </tr>
    <tr>
      <td><code>[1], ...[<var>n</var>]</code></td>
      <td>
        <p>(존재하는 경우) 괄호로 감싼 부분문자열.</p>
        <p>괄호로 감싼 부분문자열 숫자의 제한은 없습니다.</p>
      </td>
      <td>
        <p><code>result[1] === "Brown"</code></p>
        <p><code>result[2] === "Jumps"</code></p>
      </td>
    </tr>
    <tr>
      <td><code>index</code></td>
      <td>일치가 문자열에서 위치하는 인덱스. (0 시작)</td>
      <td><code>4</code></td>
    </tr>
    <tr>
      <td><code>input</code></td>
      <td>원본 문자열.</td>
      <td><code>"The Quick Brown Fox Jumps Over The Lazy Dog"</code></td>
    </tr>
    <tr>
      <th colspan="1" rowspan="5" scope="row" style="vertical-align: top">
        <code>re</code>
      </th>
      <td><code>lastIndex</code></td>
      <td>
        <p>다음 일치를 시작할 인덱스.</p>
        <p><code>g</code>를 누락하면 항상 <code>0</code>입니다.</p>
      </td>
      <td><code>25</code></td>
    </tr>
    <tr>
      <td><code>ignoreCase</code></td>
      <td><code>i</code> 플래그로 대소문자를 무시했는지 여부.</td>
      <td><code>true</code></td>
    </tr>
    <tr>
      <td><code>global</code></td>
      <td><code>g</code> 플래그로 전역 일치를 수행하는지 여부.</td>
      <td><code>true</code></td>
    </tr>
    <tr>
      <td><code>multiline</code></td>
      <td><code>m</code> 플래그로 여러 줄에 걸친 탐색을 수행하는지 여부.</td>
      <td><code>false</code></td>
    </tr>
    <tr>
      <td><code>source</code></td>
      <td>패턴 문자열.</td>
      <td><code>"quick\s(brown).+?(jumps)"</code></td>
    </tr>
  </tbody>
</table>

## 예제

### Finding successive matches

If your regular expression uses the "`g`" flag, you can use the `exec()` method multiple times to find successive matches in the same string. When you do so, the search starts at the substring of `str` specified by the regular expression's {{jsxref("RegExp.lastIndex", "lastIndex")}} property ({{jsxref("RegExp.prototype.test()", "test()")}} will also advance the {{jsxref("RegExp.lastIndex", "lastIndex")}} property). For example, assume you have this script:

```js
var myRe = /ab*/g;
var str = "abbcdefabh";
var myArray;
while ((myArray = myRe.exec(str)) !== null) {
  var msg = "Found " + myArray[0] + ". ";
  msg += "Next match starts at " + myRe.lastIndex;
  console.log(msg);
}
```

This script displays the following text:

```
Found abb. Next match starts at 3
Found ab. Next match starts at 9
```

Note: Do not place the regular expression literal (or {{jsxref("RegExp")}} constructor) within the `while` condition or it will create an infinite loop if there is a match due to the {{jsxref("RegExp.lastIndex", "lastIndex")}} property being reset upon each iteration. Also be sure that the global flag is set or a loop will occur here also.

### Using `exec()` with `RegExp` literals

You can also use `exec()` without creating a {{jsxref("RegExp")}} object:

```js
var matches = /(hello \S+)/.exec("This is a hello world!");
console.log(matches[1]);
```

This will log a message containing 'hello world!'.

## 명세

{{Specifications}}

## 브라우저 호환성

{{Compat}}

## 같이 보기

- [Regular Expressions](/ko/docs/Web/JavaScript/Guide/Regular_Expressions) chapter in the [JavaScript Guide](/ko/docs/Web/JavaScript/Guide)
- {{jsxref("RegExp")}}

---
# Source: Web_CSS_CSS_flexible_box_layout_Aligning_items_in_a_flex_container.md
---
---
title: Aligning Items in a Flex Container
slug: Web/CSS/CSS_flexible_box_layout/Aligning_items_in_a_flex_container
---

{{CSSRef}}

flexbox가 웹 개발자들의 관심 받게된 이유 중 하나는 웹 최초로 최초로 적절한 정렬 기능을 제공했기 때문입니다. flexbox의 수직 정렬 기능을 이용하여 우리는 드디어 쉽게 박스(역주: 여기서 박스는 **flex 컨테이너**를 의미합니다) 내부를 중앙 정렬 할 수 있게 되었습니다. 이 가이드에서 우리는 flexbox의 정렬 및 끝 맞추기 기능에 대해 자세히 살펴볼 것입니다.

박스 내부를 중앙 정렬 하기 위해 박스에 `align-items` 속성을 지정하면 교차 축에 대해 flex 항목을 정렬할 수 있습니다. 아래 경우, 교차 축은 수직 축입니다. `justify-content` 속성을 지정하면 flex 항목을 주축에 대해 정렬 할 수 있습니다. 아래 경우, 주축은 수평 방향입니다.

![A containing element with another box centered inside it.](align1.png)

아래 예제의 코드를 살펴보세요. flex 컨테이너(역주: .box로 지정된 div 태그)나 flex 항목(역주: .box div로 지정된 div 태그)의 크기를 조절해도 flex 컨테이너 내부는 중앙 정렬됨을 보실 수 있습니다.

{{EmbedGHLiveSample("css-examples/flexbox/alignment/intro.html", '100%', 700)}}

## 정렬 제어용 속성 목록

이 글에서 살펴볼 속성들은 다음과 같습니다.

- {{cssxref("justify-content")}} — 주축에 대해 flex 항목들을 정렬하는 방식을 제어. flex 컨테이너에 지정하는 속성.
- {{cssxref("align-items")}} — 교차축에 대해 flex 항목들을 정렬하는 방식을 제어. flex 컨테이너에 지정하는 속성.
- {{cssxref("align-self")}} — 개별 flex 항목을 교차 축에 대해 정렬 하는 방식을 제어. flex 항목에 지정하는 속성.
- {{cssxref("align-content")}} — described in the spec as for "packing flex lines"; controls space between flex lines on the cross axis.

또한, 이글에서 flexbox기반 정렬에서 margin 속성 값이 어떨게 쓰이는지 살펴볼 것입니다.

> **참고:** The alignment properties in Flexbox have been placed into their own specification — [CSS Box Alignment Level 3](https://www.w3.org/TR/css-align-3/). It is expected that this spec will ultimately supersede the properties as defined in Flexbox Level One.

## 교차축

`align-items`와 `align-self` 속성들은 flex 항목들을 교차축으로 정렬하는 것을 제어합니다. 만약, `flex-direction`이 `row`로 설정되어있다면 열 (column) 아래로 정렬을 하게되고, `flex-direction`이 `column`으로 설정되어있다면 행 (row)을 따라 정렬됩니다.

가장 간단한 flex예시는 교차축을 이용합니다. `display: flex`를 컨테이너에 추가하게되면, 모든 자식 항목들이 열 (row), 즉 가로 방향으로 정렬이 되는 flex 항목이 됩니다. 이 경우 가장 큰 y축의 크기, 즉 높이가 가장 큰 자식 항목이 교차축의 높이를 정의하게 되고, 나머지 자식 항목들은 이 높이에 맞추어 높이가 늘어나게 됩니다. 만약 flex 컨테이너의 높이가 지정이 되어있다면, 자식 항목 내용에 상관없이 지정된 높이 만큼 모든 자식 항목들이 늘어나게됩니다.

![Three items, one with additional text causing it to be taller than the others.](align2.png)

![Three items stretched to 200 pixels tall](align3.png)

모든 항목들이 같은 높이를 갖게되는 이유는 교차축을 중심으로 정렬을 제어하는 속성인 `align-items`에 지정된 초기값이 `stretch`로 설정이 되어있기 때문입니다.

이외에도 다른 값을 지정해서 항목들이 정렬되는 방식을 다르게 정의 할 수 있습니다:

- `align-items: flex-start`
- `align-items: flex-end`
- `align-items: center`
- `align-items: stretch`
- `align-items: baseline`

아래의 예시를 보면, `align-items`값이 `stretch`로 지정이 되어있습니다. 여기에 다른 값들을 넣어서 항목들이 flex 컨테이너 안에서 어떻게 정렬이 되는지 확인해보세요.

{{EmbedGHLiveSample("css-examples/flexbox/alignment/align-items.html", '100%', 520)}}

### `align-self`로 항목 한 개를 정렬하기

The `align-items` property sets the `align-self` property on all of the flex items as a group. This means you can explicitly declare the `align-self` property to target a single item. The `align-self` property accepts all of the same values as `align-items` plus a value of `auto`, which will reset the value to that which is defined on the flex container.

In this next live example, the flex container has `align-items: flex-start`, which means the items are all aligned to the start of the cross axis. I have targeted the first item using a `first-child` selector and set that item to `align-items: stretch`; another item has been selected using its class of `selected` and given `align-self: center`. You can change the value of `align-items` or change the values of `align-self` on the individual items to see how this works.

{{EmbedGHLiveSample("css-examples/flexbox/alignment/align-self.html", '100%', 650)}}

### Changing the main axis

So far we have looked at the behaviour when our `flex-direction` is `row`, and while working in a language written top to bottom. This means that the main axis runs along the row horizontally, and our cross axis alignment moves the items up and down.

![Three items, the first aligned to flex-start, second to center, third to flex-end. Aligning on the vertical axis.](align4.png)

If we change our `flex-direction` to column, `align-items` and `align-self` will align the items to the left and right.

![Three items, the first aligned to flex-start, second to center, third to flex-end. Aligning on the horizontal axis.](align5.png)

You can try this out in the example below, which has a flex container with `flex-direction: column` yet otherwise is exactly the same as the previous example.

{{EmbedGHLiveSample("css-examples/flexbox/alignment/align-self-column.html", '100%', 730)}}

## Aligning content on the cross axis — the align-content property

So far we have been aligning the items, or an individual item inside the area defined by the flex-container. If you have a wrapped multiple-line flex container then you might also want to use the `align-content` property to control the distribution of space between the rows. In the specification this is described as [packing flex lines](https://drafts.csswg.org/css-flexbox/#align-content-property).

For `align-content` to work you need more height in your flex container than is required to display the items. It then works on all the items as a set, and dictates what happens with that free space, and the alignment of the entire set of items within it.

The `align-content` property takes the following values:

- `align-content: flex-start`
- `align-content: flex-end`
- `align-content: center`
- `align-content: space-between`
- `align-content: space-around`
- `align-content: stretch`
- `align-content: space-evenly` (not defined in the Flexbox specification)

In the live example below, the flex container has a height of 400 pixels, which is more than needed to display our items. The value of `align-content` is `space-between`, which means that the available space is shared out _between_ the flex lines, which are placed flush with the start and end of the container on the cross axis.

Try out the other values to see how the `align-content` property works.

{{EmbedGHLiveSample("css-examples/flexbox/alignment/align-content.html", '100%', 850)}}

Once again we can switch our `flex-direction` to `column` in order to see how this property behaves when we are working by column. As before, we need enough space in the cross axis to have some free space after displaying all of the items.

{{EmbedGHLiveSample("css-examples/flexbox/alignment/align-content-column.html", '100%', 860)}}

> **참고:** the value `space-evenly` is not defined in the flexbox specification and is a later addition to the Box Alignment specification. Browser support for this value is not as good as that of the values defined in the flexbox spec.

See the [documentation for `justify-content` on MDN](/ko/docs/Web/CSS/justify-content) for more details on all of these values and browser support.

## Aligning content on the main axis

Now that we have seen how alignment works on the cross axis, we can take a look at the main axis. Here we only have one property available to us — `justify-content`. This is because we are only dealing with items as a group on the main axis. With `justify-content` we control what happens with available space, should there be more space than is needed to display the items.

In our initial example with `display: flex` on the container, the items display as a row and all line up at the start of the container. This is due to the initial value of `justify-content` being `flex-start`. Any available space is placed at the end of the items.

![Three items, each 100 pixels wide in a 500 pixel container. The available space is at the end of the items.](align6.png)

The `justify-content` property accepts the same values as `align-content`.

- `justify-content: flex-start`
- `justify-content: flex-end`
- `justify-content: center`
- `justify-content: space-between`
- `justify-content: space-around`
- `justify-content: stretch`
- `justify-content: space-evenly` (not defined in the Flexbox specification)

In the example below, the value of `justify-content` is `space-between`. The available space after displaying the items is distributed between the items. The left and right item line up flush with the start and end.

{{EmbedGHLiveSample("css-examples/flexbox/alignment/justify-content.html", '100%', 480)}}

If the main axis is in the block direction because `flex-direction` is set to `column`, then `justify-content` will distribute space between items in that dimension as long as there is space in the flex container to distribute.

{{EmbedGHLiveSample("css-examples/flexbox/alignment/justify-content-column.html", '100%', 880)}}

### Alignment and Writing Modes

Remember that with all of these alignment methods, the values of `flex-start` and `flex-end` are writing mode-aware. If the value of `justify-content` is `start` and the writing mode is left-to-right as in English, the items will line up starting at the left side of the container.

![Three items lined up on the left](basics5.png)

However if the writing mode is right-to-left as in Arabic, the items will line up starting at the right side of the container.

![Three items lined up from the right](basics6.png)

The live example below has the `direction` property set to `rtl` to force a right-to-left flow for our items. You can remove this, or change the values of `justify-content` to see how flexbox behaves when the start of the inline direction is on the right.

{{EmbedGHLiveSample("css-examples/flexbox/alignment/justify-content-writing-mode.html", '100%', 440)}}

## Alignment and flex-direction

The start line will also change if you change the `flex-direction` property — for example using `row-reverse` instead of `row`.

In this next example I have items laid out with `flex-direction: row-reverse` and `justify-content: flex-end`. In a left to right language the items all line up on the left. Try changing `flex-direction: row-reverse` to `flex-direction: row`. You will see that the items now move to the right hand side.

{{EmbedGHLiveSample("css-examples/flexbox/alignment/justify-content-reverse.html", '100%', 440)}}

While this may all seem a little confusing, the rule to remember is that unless you do something to change it, flex items lay themselves out in the direction that words are laid out in the language of your document along the inline, row axis. `flex-start` will be where the start of a sentence of text would begin.

![Diagram showing start on the left and end on the right.](align8.png)

You can switch them to display in the block direction for the language of your document by selecting `flex-direction: column`. Then `flex-start` will then be where the top of your first paragraph of text would start.

![Diagram showing start at the top and end at the bottom.](align10.png)

If you change flex-direction to one of the reverse values, then they will lay themselves out from the end axis and in the reverse order to the way words are written in the language of your document. `flex-start` will then change to the end of that axis — so to the location where your lines would wrap if working in rows, or at the end of your last paragraph of text in the block direction.

![Diagram showing start on the right and end on the left.](align9.png)

![Diagram showing end at the top and start at the bottom](align11.png)

## Using auto margins for main axis alignment

We don't have a `justify-items` or `justify-self` property available to us on the main axis as our items are treated as a group on that axis. However it is possible to do some individual alignment in order to separate an item or a group of items from others by using auto margins along with flexbox.

A common pattern is a navigation bar where some key items are aligned to the right, with the main group on the left. You might think that this should be a use case for a `justify-self` property, however consider the image below. I have three items on one side and two on the other. If I were able to use `justify-self` on item _d_, it would also change the alignment of item _e_ that follows, which may or may not be my intention.

![Five items, in two groups. Three on the left and two on the right.](align7.png)

Instead we can target item 4 and separate it from the first three items by giving it a `margin-left` value of `auto`. Auto margins will take up all of the space that they can in their axis — it is how centering a block with margin auto left and right works. Each side tries to take as much space as it can, and so the block is pushed into the middle.

In this live example, I have flex items arranged simply into a row with the basic flex values, and the class `push` has `margin-left: auto`. You can try removing this, or adding the class to another item to see how it works.

{{EmbedGHLiveSample("css-examples/flexbox/alignment/auto-margins.html", '100%', 470)}}

## Future alignment features for Flexbox

At the beginning of this article I explained that the alignment properties currently contained in the Level 1 flexbox specification are also included in Box Alignment Level 3, which may well extend these properties and values in the future. We have already seen one place where this has happened, with the introduction of the `space-evenly` value for `align-content` and `justify-content` properties.

The Box Alignment module also includes other methods of creating space between items, such as the `column-gap` and `row-gap` feature as seen in [CSS Grid Layout](/ko/docs/Web/CSS/CSS_Grid_Layout). The inclusion of these properties in Box Alignment means that in future we should be able to use `column-gap` and `row-gap` in flex layouts too, and in Firefox 63 you will find the first browser implementation of the gap properties in flex layout.

My suggestion when exploring flexbox alignment in depth is to do so alongside looking at alignment in Grid Layout. Both specifications use the alignment properties as detailed in the Box Alignment specification. You can see how these properties behave when working with a grid in the MDN article [Box Alignment in Grid Layout](/ko/docs/Web/CSS/CSS_Grid_Layout/Box_Alignment_in_CSS_Grid_Layout), and I have also compared how alignment works in these specifications in my [Box Alignment Cheatsheet](https://rachelandrew.co.uk/css/cheatsheets/box-alignment).

## See Also

- [Box Alignment](/ko/docs/Web/CSS/CSS_Box_Alignment)
- [Box Alignment in Flexbox](/ko/docs/Web/CSS/CSS_Box_Alignment/Box_Alignment_in_Flexbox)
- [Box Alignment in Grid Layout](/ko/docs/Web/CSS/CSS_Box_Alignment/Box_Alignment_In_Grid_Layout)

---
# Source: Web_CSS_display.md
---
---
title: display
slug: Web/CSS/display
---

{{CSSRef}}

**`display`** [CSS](/ko/docs/Web/CSS) 속성은 요소를
[블록과 인라인](/ko/docs/Web/CSS/CSS_Flow_Layout) 요소 중 어느 쪽으로 처리할지와 함께,
[플로우](/ko/docs/Web/CSS/CSS_Flow_Layout), [그리드](/ko/docs/Web/CSS/CSS_Grid_Layout),
[플렉스](/ko/docs/Web/CSS/CSS_Flexible_Box_Layout)처럼 자식 요소를 배치할 때 사용할 레이아웃을 설정합니다.

`display` 속성은, 형식적으로는 요소의 내부와 외부 디스플레이 유형을 설정합니다. 외부 디스플레이 유형은
플로우 레이아웃에 요소가 참여하는 방법을 나타내고, 내부 디스플레이 유형은 자식의 레이아웃 방식을 설정합니다.
`display`의 일부 값은 자신만의 명세를 가지고 있습니다. 이 문서의 끝에서 찾을 수 있는 명세표를 참고하세요.

## 구문

`display` 속성은 키워드 값을 사용해 지정합니다. 키워드는 6개의 카테고리로 분류할 수 있습니다.

```
.container {
  display: <display-keyword>;
}
```

### 바깥쪽

- {{CSSxRef("&lt;display-outside&gt;")}}
  - : 요소의 외부 디스플레이 유형을 설정하는 키워드입니다. 외부 디스플레이 유형은 플로우 레이아웃에서 요소 자신의 역할과
    마찬가지입니다.
  - `block`
    - : The element generates a block element box, generating line breaks both before and after the element when in
      the normal flow.
  - `inline`
    - : The element generates one or more inline element boxes that do not generate line breaks before or after
      themselves. In normal flow, the next element will be on the same line if there is space

> **참고:** Browsers that support the two-value syntax, on finding the outer value only, such as when
> `display: block` or `display: inline` is specified, will set the inner value to
> `flow`. This will result in expected behavior; for example, if you specify an element to be block, you
> would expect that the children of that element would participate in block and inline normal flow layout.

### 안쪽

- {{CSSxRef("&lt;display-inside&gt;")}}
  - : 요소의 내부 디스플레이 유형을 설정하는 키워드입니다. 내부 디스플레이 유형은 대체 요소가 아닌 요소의 콘텐츠 서식과
    배치 방법을 나타냅니다.
    - `flow` {{Experimental_Inline}}
      - : The element lays out its contents using flow layout (block-and-inline layout).

        If its outer display type is `inline` or `run-in`, and it is participating in a block or
        inline formatting context, then it generates an inline box. Otherwise it generates a block container box.

        Depending on the value of other properties (such as {{CSSxRef("position")}}, {{CSSxRef("float")}}, or
        {{CSSxRef("overflow")}}) and whether it is itself participating in a block or inline formatting context, it
        either establishes a new
        [block formatting context](/ko/docs/Web/Guide/CSS/Block_formatting_context) (BFC) for its contents
        or integrates its contents into its parent formatting context.

    - `flow-root`
      - : The element generates a block element box that establishes a new
        [block formatting context](/ko/docs/Web/Guide/CSS/Block_formatting_context), defining where the
        formatting root lies.
    - `table`
      - : These elements behave like HTML {{HTMLElement("table")}} elements. It defines a block-level box.
    - `flex`
      - : The element behaves like a block element and lays out its content according to the
        [flexbox model](/ko/docs/Web/CSS/CSS_Flexible_Box_Layout).
    - `grid`
      - : The element behaves like a block element and lays out its content according to the
        [grid model](/ko/docs/Web/CSS/CSS_Grid_Layout/Basic_Concepts_of_Grid_Layout).
    - `ruby` {{Experimental_Inline}}
      - : The element behaves like an inline element and lays out its content according to the ruby formatting model. It
        behaves like the corresponding HTML {{HTMLElement("ruby")}} elements.

> **참고:** Browsers that support the two-value syntax, on finding the inner value only, such as when
> `display: flex` or `display: grid` is specified, will set their outer value to
> `block`. This will result in expected behavior; for example, if you specify an element to be
> `display: grid`, you would expect that the box created on the grid container would be a block-level box.

### 리스트 아이템

- {{cssxref("&lt;display-listitem&gt;")}}
  - : 요소가 콘텐츠 블록 박스를 생성하고, 리스트 아이템 인라인 박스를 분리합니다.

A single value of `list-item` will cause the element to behave like a list item. This can be used together
with {{CSSxRef("list-style-type")}} and {{CSSxRef("list-style-position")}}.

`list-item` can also be combined with any {{CSSxRef("&lt;display-outside&gt;")}} keyword and the
`flow` or `flow-root` {{CSSxRef("&lt;display-inside&gt;")}} keywords.

> **참고:** In browsers that support the two-value syntax, if no inner value is specified, it will
> default to `flow`. If no outer value is specified, the principal box will have an outer display type of
> `block`.

### 내부적

- {{cssxref("&lt;display-internal&gt;")}}
  - : `table`, `ruby` 등 일부 레이아웃 모델은 복잡한 내부 구조를 가지며, 자식과 자손이 채워넣을
    여러가지 역할을 지닙니다. 이 항목은 그런 특정 레이아웃 모드에서만 의미를 갖는 "내부적"인 값을 정의합니다.
    - `table-row-group`
      - : These elements behave like {{HTMLElement("tbody")}} HTML elements.
    - `table-header-group`
      - : These elements behave like {{HTMLElement("thead")}} HTML elements.
    - `table-footer-group`
      - : These elements behave like {{HTMLElement("tfoot")}} HTML elements.
    - `table-row`
      - : These elements behave like {{HTMLElement("tr")}} HTML elements.
    - `table-cell`
      - : These elements behave like {{HTMLElement("td")}} HTML elements.
    - `table-column-group`
      - : These elements behave like {{HTMLElement("colgroup")}} HTML elements.
    - `table-column`
      - : These elements behave like {{HTMLElement("col")}} HTML elements.
    - `table-caption`
      - : These elements behave like {{HTMLElement("caption")}} HTML elements.
    - `ruby-base` {{Experimental_Inline}}
      - : These elements behave like {{HTMLElement("rb")}} HTML elements.
    - `ruby-text` {{Experimental_Inline}}
      - : These elements behave like {{HTMLElement("rt")}} HTML elements.
    - `ruby-base-container` {{Experimental_Inline}}
      - : These elements behave like {{HTMLElement("rbc")}} HTML elements generated as anonymous boxes.
    - `ruby-text-container` {{Experimental_Inline}}
      - : These elements behave like {{HTMLElement("rtc")}} HTML elements.

### 박스

- {{CSSxRef("&lt;display-box&gt;")}}
  - : 요소의 디스플레이 박스를 생성해야 하는지 지정합니다.
    - `contents`
      - : These elements don't produce a specific box by themselves. They are replaced by their pseudo-box and their
        child boxes. Please note that the CSS Display Level 3 spec defines how the `contents` value should
        affect "unusual elements" — elements that aren't rendered purely by CSS box concepts such as replaced
        elements. See
        [Appendix B: Effects of display: contents on Unusual Elements](https://drafts.csswg.org/css-display/#unbox)
        for more details.

        _Due to a bug in browsers, this will currently remove the element from the accessibility tree — screen
        readers will not look at what's inside. See the
        [Accessibility concerns](#accessibility_concerns) section below for more details._

    - `none`
      - : 레이아웃에 영향을 주지 않도록 요소의 display를 끄게 합니다(웹문서는 마치 해당 요소가 존재하지 않는 것처럼 렌더링되어집니다). 모든 하위 요소들 또한 display를 끄게 합니다. 요소가 정상적으로 본연의 공간을 가지고 있게 하면서 해당 공간에 아무것도 렌더링되지 않게 하려면, {{CSSxRef("visibility")}} 속성으로 대체하여 사용하시기 바랍니다.

### 레거시

- {{CSSxRef("&lt;display-legacy&gt;")}}
  - : CSS 2는 `display` 속성에 단일 키워드만 사용했으므로, 같은 레이아웃 모드를 위해 블록 레벨과 인라인 레벨
    키워드를 각각 필요로 했습니다.
    - `inline-block`
      - : The element generates a block element box that will be flowed with surrounding content as if it were a single
        inline box (behaving much like a replaced element would).

        It is equivalent to `inline flow-root`.

    - `inline-table`
      - : The `inline-table` value does not have a direct mapping in HTML. It behaves like an HTML
        {{HTMLElement("table")}} element, but as an inline box, rather than a block-level box. Inside the table box is
        a block-level context.

        It is equivalent to `inline table`.

    - `inline-flex`
      - : The element behaves like an inline element and lays out its content according to the flexbox model.

        It is equivalent to `inline flex`.

    - `inline-grid`
      - : The element behaves like an inline element and lays out its content according to the grid model.

        It is equivalent to `inline grid`.

### Which syntax should you use now?

The Level 3 specification details two values for the `display` property — enabling the specification of the
outer and inner display type explicitly — but this is not yet well-supported by browsers.

The `<display-legacy>` methods allow the same results with single keyword values, and should be
favoured by developers until the two keyword values are better supported. For example, using two values you might
specify an inline flex container as follows:

```css
.container {
  display: inline flex;
}
```

This can currently be specified using a single value.

```css
.container {
  display: inline-flex;
}
```

For more information on these changes to the specification, see the article
[Adapting to the new two-value syntax of display](/ko/docs/Web/CSS/display/two-value_syntax_of_display).

### Global

```css
/* Global values */
display: inherit;
display: initial;
display: unset;
```

## 안내서 및 예제

The individual pages for the different types of value that `display` can have set on it feature multiple
examples of those values in action — see the [Syntax](#syntax) section. In addition, see the following material,
which covers the various values of display in depth.

### CSS Flow Layout (`display: block`, `display: inline`)

- [Block and Inline Layout in Normal Flow](/ko/docs/Web/CSS/CSS_Flow_Layout/Block_and_Inline_Layout_in_Normal_Flow)
- [Flow Layout and Overflow](/ko/docs/Web/CSS/CSS_Flow_Layout/Flow_Layout_and_Overflow)
- [Flow Layout and Writing Modes](/ko/docs/Web/CSS/CSS_Flow_Layout/Flow_Layout_and_Writing_Modes)
- [Formatting Contexts Explained](/ko/docs/Web/CSS/CSS_Flow_Layout/Formatting_Contexts_Explained)
- [In Flow and Out of Flow](/ko/docs/Web/CSS/CSS_Flow_Layout/In_Flow_and_Out_of_Flow)

### `display: flex`

- [Basic concepts of flexbox](/ko/docs/Web/CSS/CSS_Flexible_Box_Layout/Basic_Concepts_of_Flexbox)
- [Aligning Items in a Flex Container](/ko/docs/Web/CSS/CSS_Flexible_Box_Layout/Aligning_Items_in_a_Flex_Container)
- [Controlling Ratios of Flex Items Along the Main Axis](/ko/docs/Web/CSS/CSS_Flexible_Box_Layout/Controlling_Ratios_of_Flex_Items_Along_the_Main_Ax)
- [Cross-browser Flexbox mixins](/ko/docs/Web/CSS/CSS_Flexible_Box_Layout/Mixins)
- [Mastering Wrapping of Flex Items](/ko/docs/Web/CSS/CSS_Flexible_Box_Layout/Mastering_Wrapping_of_Flex_Items)
- [Ordering Flex Items](/ko/docs/Web/CSS/CSS_Flexible_Box_Layout/Ordering_Flex_Items)
- [Relationship of flexbox to other layout methods](/ko/docs/Web/CSS/CSS_Flexible_Box_Layout/Relationship_of_Flexbox_to_Other_Layout_Methods)
- [Backwards Compatibility of Flexbox](/ko/docs/Web/CSS/CSS_Flexible_Box_Layout/Backwards_Compatibility_of_Flexbox)
- [Typical use cases of Flexbox](/ko/docs/Web/CSS/CSS_Flexible_Box_Layout/Typical_Use_Cases_of_Flexbox)

### `display: grid`

- [Basic Concepts of Grid Layout](/ko/docs/Web/CSS/CSS_Grid_Layout/Basic_Concepts_of_Grid_Layout)
- [Relationship to other layout methods](/ko/docs/Web/CSS/CSS_Grid_Layout/Relationship_of_Grid_Layout)
- [Line-based placement](/ko/docs/Web/CSS/CSS_Grid_Layout/Line-based_Placement_with_CSS_Grid)
- [Grid template areas](/ko/docs/Web/CSS/CSS_Grid_Layout/Grid_Template_Areas)
- [Layout using named grid lines](/ko/docs/Web/CSS/CSS_Grid_Layout/Layout_using_Named_Grid_Lines)
- [Auto-placement in grid layout](/ko/docs/Web/CSS/CSS_Grid_Layout/Auto-placement_in_CSS_Grid_Layout)
- [Box alignment in grid layout](/ko/docs/Web/CSS/CSS_Grid_Layout/Box_Alignment_in_CSS_Grid_Layout)
- [Grids, logical values and writing modes](/ko/docs/Web/CSS/CSS_Grid_Layout/CSS_Grid,_Logical_Values_and_Writing_Modes)
- [CSS Grid Layout and Accessibility](/ko/docs/Web/CSS/CSS_Grid_Layout/CSS_Grid_Layout_and_Accessibility)
- [CSS Grid Layout and Progressive Enhancement](/ko/docs/Web/CSS/CSS_Grid_Layout/CSS_Grid_and_Progressive_Enhancement)
- [Realizing common layouts using grids](/ko/docs/Web/CSS/CSS_Grid_Layout/Realizing_common_layouts_using_CSS_Grid_Layout)

## 접근성 고려사항

### `display: none`

Using a `display` value of `none` on an element will remove it from the
[accessibility tree](/ko/docs/Learn/Accessibility/What_is_accessibility#Accessibility_APIs). This will
cause the element and all its descendant elements to no longer be announced by screen reading technology.

If you want to visually hide the element, a more accessible alternative is to use
[a combination of properties](https://gomakethings.com/hidden-content-for-better-a11y/#hiding-the-link)
to remove it visually from the screen but keep it parseable by assistive technology such as screen readers.

### `display: contents`

Current implementations in most browsers will remove from the
[accessibility tree](/ko/docs/Learn/Accessibility/What_is_accessibility#Accessibility_APIs) any element
with a `display` value of `contents` (but descendants will remain). This will cause the element
itself to no longer be announced by screen reading technology. This is incorrect behavior according to the
[CSS specification](https://drafts.csswg.org/css-display/#valdef-display-contents).

- [More accessible markup with display: contents | Hidde de Vries](https://hiddedevries.nl/en/blog/2018-04-21-more-accessible-markup-with-display-contents)
- [Display: Contents Is Not a CSS Reset | Adrian Roselli](http://adrianroselli.com/2018/05/display-contents-is-not-a-css-reset.html)

### Tables

Changing the `display` value of a {{HTMLElement("table")}} element to `block`,
`grid`, or `flex` will alter its representation in the
[accessibility tree](/ko/docs/Learn/Accessibility/What_is_accessibility#Accessibility_APIs). This will
cause the table to no longer be announced properly by screen reading technology.

- [Short note on what CSS display properties do to table semantics — The Paciello Group](https://developer.paciellogroup.com/blog/2018/03/short-note-on-what-css-display-properties-do-to-table-semantics/)
- [Hidden content for better a11y | Go Make Things](https://gomakethings.com/hidden-content-for-better-a11y/)
- [MDN Understanding WCAG, Guideline 1.3 explanations](/ko/docs/Web/Accessibility/Understanding_WCAG/Perceivable#Guideline_1.3_%E2%80%94_Create_content_that_can_be_presented_in_different_ways)
- [Understanding Success Criterion 1.3.1 | W3C Understanding WCAG 2.0](https://www.w3.org/TR/UNDERSTANDING-WCAG20/content-structure-separation-programmatic.html)

## 명세

{{Specifications}}

{{cssinfo}}

## 브라우저 호환성

{{Compat}}

## 같이 보기

- [Block and Inline Layout in Normal Flow](/ko/docs/Web/CSS/CSS_Flow_Layout/Block_and_Inline_Layout_in_Normal_Flow)
- [Formatting contexts explained](/ko/docs/Web/CSS/CSS_Flow_Layout/Formatting_Contexts_Explained)
- {{CSSxRef("visibility")}}, {{CSSxRef("float")}}, {{CSSxRef("position")}}
- {{CSSxRef("grid")}}, {{CSSxRef("flex")}}

---
# Source: Web_API_MediaDevices_getUserMedia.md
---
---
title: MediaDevices.getUserMedia()
slug: Web/API/MediaDevices/getUserMedia
---

{{APIRef("Media Capture and Streams")}}

{{domxref("MediaDevices")}} 인터페이스의 **`getUserMedia()`** 메서드는 사용자에게 미디어 입력 장치 사용 권한을 요청하며, 사용자가 수락하면 요청한 미디어 종류의 트랙을 포함한 {{domxref("MediaStream")}}을 반환합니다. 스트림은 카메라, 비디오 녹화 장치, 스크린 공유 장치 등 하드웨어와 가장 비디오 소스가 생성하는 비디오 트랙과, 마이크, A/D 변환기 등 물리적과 가상 오디오 장치가 생성하는 오디오 스트림, 그리고 그 외의 다른 종류의 스트림을 포함할 수 있습니다.

반환하는 값은 {{domxref("MediaStream")}} 객체로 이행하는 {{jsxref("Promise")}}입니다. 사용자가 권한 요청을 거부했거나 일치하는 유형의 미디어를 사용할 수 없는 경우, 프로미스는 각각 `NonAllowedError`와 `NotFoundError`로 거부합니다.

> **참고:** 사용자가 권한 요청에 대한 선택을 하지 않고 완전히 무시할 수도 있기 때문에, 프로미스 또한 이행도 거부도 하지 않을 수 있습니다.

보통, {{domxref("MediaDevices")}} 싱글톤 객체는 다음과 같이 {{domxref("navigator.mediaDevices")}}를 사용해 접근합니다.

```js
async function getMedia(constraints) {
  let stream = null;

  try {
    stream = await navigator.mediaDevices.getUserMedia(constraints);
    /* 스트림 사용 */
  } catch (err) {
    /* 오류 처리 */
  }
}
```

프로미스를 직접 사용할 경우 다음과 같습니다.

```js
navigator.mediaDevices
  .getUserMedia(constraints)
  .then(function (stream) {
    /* 스트림 사용 */
  })
  .catch(function (err) {
    /* 오류 처리 */
  });
```

> **참고:** 현재 문서를 안전하게 불러온 경우가 아니라면 `navigator.mediaDevices`는 `undefined`이므로 `getUserMedia()`도 사용할 수 없습니다. [개인정보와 보안](#개인정보와_보안) 항목에서 `getUserMedia()`와 관련된 보안 문제를 자세히 살펴보세요.

## 구문

```js
const promise = navigator.mediaDevices.getUserMedia(constraints);
```

### 매개변수

- `constraints`
  - : 요청할 미디어 유형과 각각에 대한 요구사항을 지정하는 {{domxref("MediaStreamConstraints")}} 객체.`constraints` 매개변수는 두 개의 구성 요소, `video`와 `audio`를 가지는 객체로, 요청할 미디어 유형에 대해 설명합니다. 둘 중 적어도 하나는 지정해야 합니다. 브라우저가 주어진 유형과 제약을 만족하는 미디어 트랙을 하나도 찾을 수 없는 경우 프로미스는 `NotFoundError`와 함께 거부합니다.다음은 특별한 요구사항 없이 오디오와 비디오 둘 다 요청하는 매개변수입니다.

    ```js
    { audio: true, video: true }
    ```

    미디어 타입에 true 가 지정된 경우 각 타입에 맞는 장치가 사용 준비된 상태이어야 하며, 만약 사용 준비가 안 된 상태에서 getUserMedia() 를 호출하면 오류를 반환합니다.constraints 매개변수에 세부사항을 지정하여 카메라와 마이크에 세부적인 요청을 할 수 있습니다. 아래의 코드는 비디오의 해상도를 1280x720로 지정하는 예제입니다.

    ```js
    { audio: true, video: { width: 1280, height: 720 } }
    ```

    브라우저는 지정한 해상도의 비디오 트랙을 가져오기 위해 시도하지만, 어떤 이유로든 지정한 해상도의 트랙을 가져올 수 없다면 다른 해상도의 비디오 트랙을 반환합니다.아래와 같이 `min`, `max` 키워드를 사용하여 최소 해상도를 1280x720으로 지정할 수도 있으며, `exact` (논리적으로 `min == max` 와 같음) 키워드를 사용하여 특정 해상도를 지정할 수도 있습니다.

    ```js
    { audio: true, video: { width: { min: 1280 }, height: { min: 720 } } }
    ```

    만약 카메라에서 지원하는 해상도 중에서 1280x720해상도가 없거나 이 이상의 해상도 역시 없는 경우 promise는 rejected 상태로 `OverconstrainedError` 를 반환하며, 사용자에게 미디어 장치 사용 권한 요청을 하지 않습니다.`min`, `max` 키워드만 사용한 경우 최소, 최대 해상도를 지정할 수는 있지만, 브라우저는 최솟값을 기준으로 제공할 수 있는 해상도를 찾아 미디어 스트림을 반환합니다. 일반적으로 이러한 동작은 우리의 의도와 다릅니다. 그래서 `ideal` 키워드를 사용하여 이상적인 해상도를 지정할 수 있습니다.아래의 코드를 논리적으로 해석하면 1024x776 - 1120x800 - 1350x1020 - 1920x1080 와 같이 지원하는 여러 해상도가 있으면 브라우저는 `ideal` 해상도와 가장 근사하는 1120x800 해상도를 미디어 장치에 요청 후 반환합니다.

    ```js
    { audio: true, video: { width: { min: 1024, ideal: 1280, max: 1920 }, height: { min: 776, ideal: 720, max: 1080 } } }
    ```

    아래와 같이 최솟값 최댓값 지정 없이 `ideal` 해상도만 지정할 수도 있습니다.

    ```js
    { audio: true, video: { width: { ideal: 1280 }, height: { ideal: 720 } } }
    ```

    모바일 장치의 전면 카메라를 요청하기 위한 코드:

    ```js
    { audio: true, video: { facingMode: "user" } }
    ```

    모바일 장치의 후면 카메라를 요청하기 위한 코드:

    ```js
    { audio: true, video: { facingMode: { exact: "environment" } } }
    ```

### 반환 값

요청한 미디어를 성공적으로 얻었다면 {{domxref("MediaStream")}} 을 수신하는 핸들러가 {{jsxref("Promise")}} 형태로 스트림을 반환합니다.

### 예외

promise 이행이 실패하면 실패 처리 핸들러로 {{domxref("DOMException")}} 에러 객체가 전달됩니다. 발생 가능한 에러 종류:

- `AbortError`
  - : 사용자와 운영체제에서 하드웨어 장치 사용 권한을 부여받고 `NotReadableError` 에러를 발생시키는 하드웨어 문제가 발생하지 않았지만, 다른 프로그램에서 해당 장치를 사용 중인 경우 이 에러가 발생합니다.
- `NotAllowedError`
  - : 사용자가 브라우저 설정을 통해 장치에 대한 접근권한을 차단하였거나 장치 사용 권한 요청에 거부한 경우 이 에러가 발생합니다. 이 외에도 어떤 식으로든 장치에 대한 접근을 차단하였다면 이 에러가 발생합니다.> **참고:** 이전 버전의 규격에서는 이 에러와 `SecurityError` 를 동일한 의미로 사용하였지만, 현재 버전에서는 다른 의미로 사용하므로 혼용하여선 안 됩니다.
- `NotFoundError`
  - : constraints 매개변수 조건에 맞는 미디어 트랙이 없는 경우 이 에러가 발생합니다.
- `NotReadableError`
  - : 사용자가 접근 권한을 부여했고 조건에 맞는 미디어 트랙도 있지만 어떤 이유로든 장치에 액세스 할 수 없어서 운영체제, 브라우저, 웹 페이지 레벨에서 하드웨어 에러가 발생하여 이 에러가 발생합니다.
- `OverconstrainedError`
  - : The specified constraints resulted in no candidate devices which met the criteria requested. The error is an object of type `OverconstrainedError`, and has a `constraint` property whose string value is the name of a constraint which was impossible to meet, and a `message` property containing a human-readable string explaining the problem.> **참고:** Because this error can occur even when the user has not yet granted permission to use the underlying device, it can potentially be used as a fingerprinting surface.
- `SecurityError`
  - : User media support is disabled on the {{domxref("Document")}} on which `getUserMedia()` was called. The mechanism by which user media support is enabled and disabled is left up to the individual user agent.
- `TypeError`
  - : The list of constraints specified is empty, or has all constraints set to `false`.

## User privacy

As an API that may involve significant privacy concerns, `getUserMedia()` is held by the specification to very specific requirements for user notification and permission management. First, `getUserMedia()` must always get user permission before opening any media gathering input such as a webcam or microphone. Browsers may offer a once-per-domain permission feature, but they must ask at least the first time, and the user must specifically grant ongoing permission if they choose to do so.

Of equal importance are the rules around notification. Browsers are required to display an indicator that shows that a camera or microphone is in use, above and beyond any hardware indicator that may exist. They must also show an indicator that permission has been granted to use a device for input, even if the device is not actively recording at the moment.

In Firefox, for example, the URL bar displays a pulsing red icon to indicate that recording is underway. The icon is gray if the permission is in place but recording is not currently underway. The device's physical light is used to indicate whether or not recording is currently active. If you've muted your camera (so-called "facemuting"), your camera's activity light goes out to indicate that the camera is not actively recording you, without discarding the permission to resume using the camera once muting is over.

## Examples

### Width and height

This example gives a preference for camera resolution, and assigns the resulting {{domxref("MediaStream")}} object to a video element.

```js
// Prefer camera resolution nearest to 1280x720.
var constraints = { audio: true, video: { width: 1280, height: 720 } };

navigator.mediaDevices
  .getUserMedia(constraints)
  .then(function (mediaStream) {
    var video = document.querySelector("video");
    video.srcObject = mediaStream;
    video.onloadedmetadata = function (e) {
      video.play();
    };
  })
  .catch(function (err) {
    console.log(err.name + ": " + err.message);
  }); // always check for errors at the end.
```

### Using the new API in older browsers

Here's an example of using `navigator.mediaDevices.getUserMedia()`, with a polyfill to cope with older browsers. Note that this polyfill does not correct for legacy differences in constraints syntax, which means constraints won't work well across browsers. It is recommended to use the [adapter.js](https://github.com/webrtc/adapter) polyfill instead, which does handle constraints.

```js
// Older browsers might not implement mediaDevices at all, so we set an empty object first
if (navigator.mediaDevices === undefined) {
  navigator.mediaDevices = {};
}

// Some browsers partially implement mediaDevices. We can't just assign an object
// with getUserMedia as it would overwrite existing properties.
// Here, we will just add the getUserMedia property if it's missing.
if (navigator.mediaDevices.getUserMedia === undefined) {
  navigator.mediaDevices.getUserMedia = function (constraints) {
    // First get ahold of the legacy getUserMedia, if present
    var getUserMedia =
      navigator.webkitGetUserMedia || navigator.mozGetUserMedia;

    // Some browsers just don't implement it - return a rejected promise with an error
    // to keep a consistent interface
    if (!getUserMedia) {
      return Promise.reject(
        new Error("getUserMedia is not implemented in this browser"),
      );
    }

    // Otherwise, wrap the call to the old navigator.getUserMedia with a Promise
    return new Promise(function (resolve, reject) {
      getUserMedia.call(navigator, constraints, resolve, reject);
    });
  };
}

navigator.mediaDevices
  .getUserMedia({ audio: true, video: true })
  .then(function (stream) {
    var video = document.querySelector("video");
    // Older browsers may not have srcObject
    if ("srcObject" in video) {
      video.srcObject = stream;
    } else {
      // Avoid using this in new browsers, as it is going away.
      video.src = window.URL.createObjectURL(stream);
    }
    video.onloadedmetadata = function (e) {
      video.play();
    };
  })
  .catch(function (err) {
    console.log(err.name + ": " + err.message);
  });
```

### Frame rate

Lower frame-rates may be desirable in some cases, like WebRTC transmissions with bandwidth restrictions.

```js
var constraints = { video: { frameRate: { ideal: 10, max: 15 } } };
```

### Front and back camera

On mobile phones.

```js
var front = false;
document.getElementById("flip-button").onclick = function () {
  front = !front;
};

var constraints = { video: { facingMode: front ? "user" : "environment" } };
```

## Permissions

To use `getUserMedia()` in an installable app (for example, a [Firefox OS app](/en-US/Apps/Build/Building_apps_for_Firefox_OS/Firefox_OS_app_beginners_tutorial)), you need to specify one or both of the following fields inside your manifest file:

```js
"permissions": {
  "audio-capture": {
    "description": "Required to capture audio using getUserMedia()"
  },
  "video-capture": {
    "description": "Required to capture video using getUserMedia()"
  }
}
```

See [permission: audio-capture](/en-US/Apps/Developing/App_permissions#audio-capture) and [permission: video-capture](/en-US/Apps/Developing/App_permissions#video-capture) for more information.

## 명세서

{{Specifications}}

## 브라우저 호환성

{{Compat}}

## See also

- The older {{domxref("navigator.getUserMedia()")}} legacy API.
- {{domxref("mediaDevices.enumerateDevices()")}}: Learn the types and number of devices the user has available.
- [WebRTC API](/ko/docs/Web/API/WebRTC_API)
- [Media Capture and Streams API (Media Streams)](/ko/docs/Web/API/Media_Streams_API)
- [Taking webcam photos](/ko/docs/Web/API/WebRTC_API/Taking_still_photos): A tutorial on using `getUserMedia()` to taking photos rather than video.

---
# Source: Web_HTML_Element_tbody.md
---
---
title: "<tbody>: 표 본문 요소"
slug: Web/HTML/Element/tbody
---

{{HTMLSidebar}}

**HTML** **`<tbody>`** 요소는 표의 여러 행({{htmlelement("tr")}})을 묶어서 표 본문을 구성합니다.

{{InteractiveExample("HTML Demo: &lt;tbody&gt;", "tabbed-taller")}}

```html interactive-example
<table>
  <caption>
    Council budget (in £) 2018
  </caption>
  <thead>
    <tr>
      <th scope="col">Items</th>
      <th scope="col">Expenditure</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">Donuts</th>
      <td>3,000</td>
    </tr>
    <tr>
      <th scope="row">Stationery</th>
      <td>18,000</td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <th scope="row">Totals</th>
      <td>21,000</td>
    </tr>
  </tfoot>
</table>
```

```css interactive-example
thead,
tfoot {
  background-color: #2c5e77;
  color: #fff;
}

tbody {
  background-color: #e4f0f5;
}

table {
  border-collapse: collapse;
  border: 2px solid rgb(140 140 140);
  font-family: sans-serif;
  font-size: 0.8rem;
  letter-spacing: 1px;
}

caption {
  caption-side: bottom;
  padding: 10px;
}

th,
td {
  border: 1px solid rgb(160 160 160);
  padding: 8px 10px;
}

td {
  text-align: center;
}
```

`<tbody>` 요소와 그 사촌인 {{HTMLElement("thead")}}, {{HTMLElement("tfoot")}} 요소는 화면과 프린터에 렌더링 할 때 뿐만 아니라 {{Glossary("accessibility", "접근성")}} 차원에서도 유용한 의미를 표의 행에 부여합니다.

<table class="properties">
  <tbody>
    <tr>
      <th scope="row">
        <a href="/ko/docs/Web/Guide/HTML/Content_categories">콘텐츠 카테고리</a>
      </th>
      <td>없음.</td>
    </tr>
    <tr>
      <th scope="row">가능한 콘텐츠</th>
      <td>0개 이상의 {{htmlelement("tr")}} 요소.</td>
    </tr>
    <tr>
      <th scope="row">태그 생략</th>
      <td>
        <code>&#x3C;tbody></code> 요소는 부모 {{HTMLElement("table")}}
        요소의 렌더링에 반드시 필요한 요소는 아닙니다. 그러나
        <code>&#x3C;table></code> 요소의 자식 중
        {{ HTMLElement("tr") }} 요소가 존재하면 사용할 수 없습니다.
      </td>
    </tr>
    <tr>
      <th scope="row">가능한 부모 요소</th>
      <td>
        {{ HTMLElement("table") }} 요소.
        {{ HTMLElement("caption") }},
        {{HTMLElement("colgroup") }},
        {{ HTMLElement("thead") }} 요소가 존재하는 경우, 그 뒤에
        위치할 수 있습니다.
      </td>
    </tr>
    <tr>
      <th scope="row">가능한 ARIA 역할</th>
      <td>모두</td>
    </tr>
    <tr>
      <th scope="row">DOM 인터페이스</th>
      <td>{{domxref("HTMLTableSectionElement")}}</td>
    </tr>
  </tbody>
</table>

## 특성

이 요소는 [전역 특성](/ko/docs/Web/HTML/Global_attributes)만 포함합니다.

### Deprecated attributes

- `align` {{deprecated_inline}}
  - : This enumerated attribute specifies how horizontal alignment of each cell content will be handled. Possible values are:
    - `left`, aligning the content to the left of the cell
    - `center`, centering the content in the cell
    - `right`, aligning the content to the right of the cell
    - `justify`, inserting spaces into the textual content so that the content is justified in the cell
    - `char`, aligning the textual content on a special character with a minimal offset, defined by the [`char`](/ko/docs/Web/HTML/Element/tbody#char) and [`charoff`](/ko/docs/Web/HTML/Element/tbody#charoff) attributes.

    If this attribute is not set, the `left` value is assumed.

    As this attribute is deprecated, use the CSS {{cssxref("text-align")}} property instead.

    > **Note:** The equivalent `text-align` property for the `align="char"` is not implemented in any browsers yet. See the [`text-align`'s browser compatibility section](/ko/docs/Web/CSS/text-align#Browser_compatibility) for the `&#x3C;string>` value.

- `bgcolor` {{Deprecated_inline}}
  - : The background color of the table. It is a [6-digit hexadecimal RGB code](/ko/docs/Web/CSS/color_value#RGB_colors), prefixed by a '`#`'. One of the predefined [color kewords](/ko/docs/Web/CSS/color_value#Color_keywords) can also be used.

    As this attribute is deprecated, use the CSS {{cssxref("background-color")}} property instead.

- `char` {{deprecated_inline}}
  - : This attribute is used to set the character to align the cells in a column on. Typical values for this include a period (`.`) when attempting to align numbers or monetary values. If [`align`](/ko/docs/Web/HTML/Element/tbody#align) is not set to `char`, this attribute is ignored.
- `charoff` {{deprecated_inline}}
  - : This attribute is used to indicate the number of characters to offset the column data from the alignment characters specified by the `char` attribute.
- `valign` {{deprecated_inline}}
  - : This attribute specifies the vertical alignment of the text within each row of cells of the table header. Possible values for this attribute are:
    - `baseline`, which will put the text as close to the bottom of the cell as it is possible, but align it on the [baseline](https://en.wikipedia.org/wiki/Baseline_%28typography%29) of the characters instead of the bottom of them. If characters are all of the size, this has the same effect as `bottom`.
    - `bottom`, which will put the text as close to the bottom of the cell as it is possible;
    - `middle`, which will center the text in the cell;
    - and `top`, which will put the text as close to the top of the cell as it is possible.

  As this attribute is deprecated, use the CSS {{cssxref("vertical-align")}} property instead.

## 사용 일람

- 표의 헤더 행을 나타내기 위해 {{HTMLElement("thead")}} 요소를 사용한 경우, `<tbody>` 요소는 반드시 그 뒤에 위치해야 합니다.
- `<tbody>`를 사용할 경우, {{HTMLElement("table")}}의 바로 밑 자식이면서 `<tbody>`에 속하지 않는 {{htmlelement("tr")}} 요소는 사용할 수 없습니다. 모든 비 헤더, 비 푸터 행은 반드시 `<tbody>`의 자식으로 존재해야 합니다.
- 문서 출력 시, `<thead>`와 {{htmlelement("tfoot")}} 요소는 모든 페이지에서 같거나 거의 같은 정보를 나타내고, `<tbody>` 요소는 서로 다른 정보를 나타냅니다.
- 표를 화면 맥락(브라우저 창 등)에서 표시할 때, 화면이 표 전체를 보여주기에 충분히 크지 않은 경우 {{Glossary("user agent", "사용자 에이전트")}}는 같은 부모의 `<thead>`, `<tbody>`, `<tfoot>`, {{HTMLElement("caption")}} 요소를 서로 따로 스크롤 가능토록 설정할 수 있습니다.
- 하나의 표에 다수의 `<tbody>`를 연속적으로 사용할 수 있으며, 이를 통해 커다란 표의 행을 구획으로 나눌 수 있습니다. 필요한 경우 각 구획에 서로 다른 서식을 적용할 수도 있습니다.

## 예제

다음은 `<tbody>` 요소 사용법을 보이는 예제입니다. 더 많은 예제는 {{ HTMLElement("table", "", "#예제") }}에서도 볼 수 있습니다.

### 기본 예제

이번 예제는 {{HTMLElement("thead")}}와 {{HTMLElement("tbody")}}를 사용해 학생 그룹의 정보를 나열하는 표를 생성합니다.

#### HTML

표의 HTML은 다음과 같습니다. 학생의 정보를 나타내는 표 본문 칸이 모두 하나의 `<tbody>` 요소에 속함에 주의하세요.

```html
<table>
  <thead>
    <tr>
      <th>Student ID</th>
      <th>Name</th>
      <th>Major</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>3741255</td>
      <td>Jones, Martha</td>
      <td>Computer Science</td>
    </tr>
    <tr>
      <td>3971244</td>
      <td>Nim, Victor</td>
      <td>Russian Literature</td>
    </tr>
    <tr>
      <td>4100332</td>
      <td>Petrov, Alexandra</td>
      <td>Astrophysics</td>
    </tr>
  </tbody>
</table>
```

#### CSS

다음은 표에 적용할 CSS 스타일입니다.

```css
table {
  border: 2px solid #555;
  border-collapse: collapse;
  font:
    16px "Lucida Grande",
    "Helvetica",
    "Arial",
    sans-serif;
}
```

우선 표의 전반적인 스타일을 설정합니다.외부 테두리의 굵기, 스타일, 색을 설정하고, {{cssxref("border-collapse")}}를 이용해 각 칸의 테두리가 서로 분리되지 않고 공유하도록 지정합니다. {{cssxref("font")}}를 사용해 표의 기본 글씨체도 설정합니다.

```css
th,
td {
  border: 1px solid #bbb;
  padding: 2px 8px 0;
  text-align: left;
}
```

그 다음은 대부분의 칸에 적용할 스타일입니다. 1픽셀 두께의 밝은 회색 테두리를 추가하고 안쪽 여백을 조정하며, {{cssxref("text-align")}}을 사용해 모두 좌측 정렬로 설정합니다.

```css
thead > tr > th {
  background-color: #cce;
  font-size: 18px;
  border-bottom: 2px solid #999;
}
```

마지막으로 {{HTMLElement("thead")}} 안에 위치하는 헤더 칸에 추가 스타일을 부여합니다. 보다 어두운 {{cssxref("background-color")}}, 더 큰 글씨 크기, 그리고 다른 테두리보다 두껍고 어두운 아래쪽 테두리를 적용합니다.

#### 결과

결과는 다음과 같습니다.

{{EmbedLiveSample("기본_예제", 650, 150)}}

### 다중 본문

You can create multiple sections within a table by using multiple `<tbody>` elements. Each may potentially have its own header row or rows; however, _there can be only one {{HTMLElement("thead")}} per table!_ Because of that, you need to use a {{HTMLElement("tr")}} filled with {{HTMLElement("th")}} elements to create headers within each `<tbody>`. Let's see how that's done.

Let's take the previous example, add some more students to the list, and update the table so that instead of listing each student's major on every row, the students are grouped by major, with heading rows for each major.

#### Result

First, the resulting table, so you know what we're building:

{{EmbedLiveSample("다중_본문", 650, 250)}}

#### HTML

The revised HTML looks like this:

```html
<table>
  <thead>
    <tr>
      <th>Student ID</th>
      <th>Name</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th colspan="2">Computer Science</th>
    </tr>
    <tr>
      <td>3741255</td>
      <td>Jones, Martha</td>
    </tr>
    <tr>
      <td>4077830</td>
      <td>Pierce, Benjamin</td>
    </tr>
    <tr>
      <td>5151701</td>
      <td>Kirk, James</td>
    </tr>
  </tbody>
  <tbody>
    <tr>
      <th colspan="2">Russian Literature</th>
    </tr>
    <tr>
      <td>3971244</td>
      <td>Nim, Victor</td>
    </tr>
  </tbody>
  <tbody>
    <tr>
      <th colspan="2">Astrophysics</th>
    </tr>
    <tr>
      <td>4100332</td>
      <td>Petrov, Alexandra</td>
    </tr>
    <tr>
      <td>8892377</td>
      <td>Toyota, Hiroko</td>
    </tr>
  </tbody>
</table>
```

Notice that each major is placed in a separate `<tbody>` block, the first row of which contains a single {{HTMLElement("th")}} element with a [`colspan`](/ko/docs/Web/HTML/Element/th#colspan) attribute that spans the entire width of the table. That heading lists the name of the major contained within the `<tbody>`.

Then each remaining row in each major's `<tbody>` consists of two cells: the first for the student's ID and the second for their name.

#### CSS

```css hidden
table {
  border: 2px solid #555;
  border-collapse: collapse;
  font:
    16px "Lucida Grande",
    "Helvetica",
    "Arial",
    sans-serif;
}

th,
td {
  border: 1px solid #bbb;
  padding: 2px 8px 0;
  text-align: left;
}

thead > tr > th {
  background-color: #cce;
  font-size: 18px;
  border-bottom: 2px solid #999;
}
```

Most of the CSS is unchanged. We do, however, add a slightly more subtle style for header cells contained directly within a `<tbody>` (as opposed to those which reside in a {{HTMLElement("thead")}}). This is used for the headers indicating each table section's corresponding major.

```css
tbody > tr > th {
  background-color: #dde;
  border-bottom: 1.5px solid #bbb;
  font-weight: normal;
}
```

## 명세

{{Specifications}}

## 브라우저 호환성

{{Compat}}

## 같이 보기

- CSS properties and [pseudo-classes](/ko/docs/Web/CSS/Pseudo-classes) that may be specially useful to style the `<tbody>` element:
  - the {{ cssxref(":nth-child") }} pseudo-class to set the alignment on the cells of the column;
  - the {{ cssxref("text-align") }} property to align all cells content on the same character, like '.'.

---
# Source: Web_API_Service_Worker_API_Using_Service_Workers.md
---
---
title: Using Service Workers
slug: Web/API/Service_Worker_API/Using_Service_Workers
---

{{DefaultAPISidebar("Service Workers API")}}

{{ SeeCompatTable() }}

본 문서에서는 서비스 워커를 시작하기 위한 기본적인 아키텍처, 서비스 워커 등록, 새로운 서비스 워커의 설치와 활성화 과정, 서비스 워커 업데이트, 캐시 제어 및 사용자 정의 응답에 대한 정보를 오프라인 기능을 갖춘 간단한 예제를 통해 제공합니다.

## 서비스 워커에 앞서서

웹 사용자들이 몇 년 동안 겪었던 가장 중요한 문제 중 하나는 인터넷 연결이 끊어지면 작동하지 않는겁니다. 세계 최고의 웹 앱조차 연결이 없을 때는 끔찍한 사용자 경험을 제공합니다. 우리의 [오프라인](/en-US/Apps/Build/Offline) 페이지가 보여주듯이, 이 문제를 해결하기 위한 기술을 개발하기 위한 여러가지 시도가 있었고, 일부 문제는 해결되었습니다. 그러나 가장 중요한 문제는 리소스 캐싱과 커스텀 네트워크(예를 들어 WebSocket등을 이용한 리소스 로드) 통신 제어 메커니즘이 여전히 좋지 않다는 점입니다.

직전의 시도였던 [AppCache](/ko/docs/Web/HTML/Using_the_application_cache) 는 캐싱할 리소스를 쉽게 지정할 수 있었기 때문에 좋은 생각이였던것 처럼 보였지만, 당신이 지정한 동작에 대한 가정을 앱이 정확하게 따르지 않을 경우 앱이 끔찍하게 망가집니다. 자세히 알고 싶으면 Jake Archibald의 [Application Cache is a Douchebag](http://alistapart.com/article/application-cache-is-a-douchebag) 을 참고하세요.

> **참고:** Firefox 44에서 [AppCache](/ko/docs/Web/HTML/Using_the_application_cache) 를 사용해서 페이지의 오프라인 지원을 제공할 경우 콘솔에 [서비스 워커](/ko/docs/Web/API/Service_Worker_API/Using_Service_Workers) 를 대신 사용하는것에 대한 제안이 경고로 표시됩니다. ([Firefox bug 1204581](https://bugzil.la/1204581))

서비스 워커는 최종적으로 이러한 문제를 해결해야 합니다. 서비스 워커 구문은 [AppCache](/ko/docs/Web/HTML/Using_the_application_cache) 보다 복잡하지만, JavaScript를 사용해서 세밀하게 [AppCache](/ko/docs/Web/HTML/Using_the_application_cache) 의 암묵적인 동작들을 제어할 수 있으므로 이 문제 그 이상을 처리 할 수 있습니다. 서비스 워커를 사용하면 먼저 캐싱된 리소스를 사용하도록 앱을 설정해서 오프라인일 경우에도 일관적인 경험을 제공한다음 네트워크 연결이 돌아올 때 더 많은 데이터를 불러오게 할 수 있습니다. (보통 [오프라인 우선](http://offlinefirst.org/) 이라고 함) 이 기능은 네이티브 앱에서는 이미 널리 사용되는 구현법이며, 이는 네이티브 앱이 웹 앱 대신 선택되는 주된 이유 중 하나입니다.

## 서비스워커 개발을 위한 환경 설정

서비스워커가 지원되는 최신 브라우저에서 많은 서비스 워커 기능들이 활성화되어 있습니다. 만약 현재 사용하시는 브라우저에서 데모 코드가 돌아가지 않으면, 아래와 같이 환경을 설정해주세요.

- **Firefox Nightly**: `about:config` 로 가서 `dom.serviceWorkers.enabled` 값을 true 로 변경하고, 브라우저 재시작
- **Chrome Canary**: `chrome://flags` 로 가서 `experimental-web-platform-features` 을 키고, 브라우저 재시작 (몇몇 기능은 크롬에서도 활성화되어 있습니다)
- **Opera**: `opera://flags` 로 가서 `Support for ServiceWorker` 를 활성화 하고, 브라우저 재시작

애플리케이션을 HTTPS 에서 실행시키세요 - 서비스워커는 보안상의 이유로 HTTPS 에서만 동작합니다. Github 은 HTTPS 를 지원하기 때문에 서비스워커를 시험해보기 좋은 사이트입니다. 이외에 localhost 도 https 로 간주되니 로컬 개발환경도 활용해보세요.

## 기본 구조

다음의 단계들은 서비스 워커의 기본적인 설정법입니다:

1. {{domxref("serviceWorkerContainer.register()")}}을 통해서 서비스 워커 URL을 가져오고, 등록합니다.
2. 등록에 성공하면, {{domxref("ServiceWorkerGlobalScope") }} 범위에서 서비스 워커가 실행됩니다. 이는 (메인 스크립트 실행 쓰레드를 running off하면서) 기본적으로 DOM 접근이 없는 작업 문맥을 갖습니다.
3. 이제 서비스 워커는 이벤트를 처리할 준비가 되었습니다.
4. 서비스 워커가 제어하는 페이지들에 연속적으로 접근하게 될 때 서비스 워커 설치를 시도하게 됩니다. 서비스 워커는 항상 처음으로 설치 이벤트를 받습니다.(설치 이벤트는 IndexedDB를 생성하고, 사이트 assets을 캐싱하는 처리를 시작할 때 사용될 수 있습니다.) 설치 이벤트는 모든 것을 오프라인에서 사용할 수 있게 하는, 네이티브 또는 Firefox OS 앱을 설치하는 프로시저와 같은 종류입니다.
5. `oninstall` 핸들러가 완료되면, 서비스 워커가 설치되었다고 할 수 있습니다.
6. 다음은 활성(activation) 이벤트입니다. 서비스 워커가 설치되면, 활성 이벤트를 받게 됩니다. `onactivate` 는 이전 버전의 서비스 워커 스크립트에서 사용된 리소스들을 삭제하는 용도로서 주로 사용됩니다.
7. 이제 서비스 워커가 페이지들을 제어하게 될 것이지만, 오직 `register()` 가 성공적으로 수행된 후에 페이지들이 열리게 될 것입니다. 즉, 문서는 서비스 워커와 함께, 또는 없이도 라이프를 시작하고 유지합니다. 따라서 문서는 실제로 서비스 워커에 제어되기 위해서 재시작 되어야 할 것입니다.

![](sw-lifecycle.png)

The below graphic shows a summary of the available service worker events:

![install, activate, message, fetch, sync, push](sw-events.png)

### Promises

[Promises](/ko/docs/Web/JavaScript/Reference/Global_Objects/Promise) are a great mechanism for running async operations, with success dependant on one another. This is central to the way service workers work.

Promises can do a great many things, but for now, all you need to know is that if something returns a promise, you can attach `.then()` to the end and include callbacks inside it for success, failure, etc., or you can insert `.catch()` on the end if you want to include a failure callback.

Let's compare a traditional synchronous callback structure to its asynchronous promise equivalent.

#### sync

```js
try {
  var value = myFunction();
  console.log(value);
} catch (err) {
  console.log(err);
}
```

#### async

```js
myFunction()
  .then(function (value) {
    console.log(value);
  })
  .catch(function (err) {
    console.log(err);
  });
```

In the first example, we have to wait for `myFunction()` to run and return `value` before any more of the code can execute. In the second example, `myFunction()` returns a promise for `value`, then the rest of the code can carry on running. When the promise resolves, the code inside `then` will be run, asynchronously.

Now for a real example — what if we wanted to load images dynamically, but we wanted to make sure the images were loaded before we tried to display them? This is a standard thing to want to do, but it can be a bit of a pain. We can use `.onload` to only display the image after it's loaded, but what about events that start happening before we start listening to them? We could try to work around this using `.complete`, but it's still not foolproof, and what about multiple images? And, ummm, it's still synchronous, so blocks the main thread.

Instead, we could build our own promise to handle this kind of case. (See our [Promises test](https://github.com/mdn/promises-test) example for the source code, or [look at it running live](https://mdn.github.io/promises-test/).)

> **Note:** A real service worker implementation would use caching and onfetch rather than the deprecated XMLHttpRequest API. Those features are not used here so that you can focus on understanding Promises.

```js
function imgLoad(url) {
  return new Promise(function (resolve, reject) {
    var request = new XMLHttpRequest();
    request.open("GET", url);
    request.responseType = "blob";

    request.onload = function () {
      if (request.status == 200) {
        resolve(request.response);
      } else {
        reject(
          Error(
            "Image didn't load successfully; error code:" + request.statusText,
          ),
        );
      }
    };

    request.onerror = function () {
      reject(Error("There was a network error."));
    };

    request.send();
  });
}
```

We return a new promise using the `Promise()` constructor, which takes as an argument a callback function with `resolve` and `reject` parameters. Somewhere in the function, we need to define what happens for the promise to resolve successfully or be rejected — in this case return a 200 OK status or not — and then call `resolve` on success, or `reject` on failure. The rest of the contents of this function is fairly standard XHR stuff, so we won't worry about that for now.

When we come to call the `imgLoad()` function, we call it with the url to the image we want to load, as we might expect, but the rest of the code is a little different:

```js
var body = document.querySelector("body");
var myImage = new Image();

imgLoad("myLittleVader.jpg").then(
  function (response) {
    var imageURL = window.URL.createObjectURL(response);
    myImage.src = imageURL;
    body.appendChild(myImage);
  },
  function (Error) {
    console.log(Error);
  },
);
```

On to the end of the function call, we chain the promise `then()` method, which contains two functions — the first one is executed when the promise successfully resolves, and the second is called when the promise is rejected. In the resolved case, we display the image inside `myImage` and append it to the body (it's argument is the `request.response` contained inside the promise's `resolve` method); in the rejected case we return an error to the console.

This all happens asynchronously.

> **참고:** You can also chain promise calls together, for example:
> `myPromise().then(success, failure).then(success).catch(failure);`

> **참고:** You can find a lot more out about promises by reading Jake Archibald's excellent [JavaScript Promises: there and back again](http://www.html5rocks.com/en/tutorials/es6/promises/).

## Service workers demo

To demonstrate just the very basics of registering and installing a service worker, we have created a simple demo called [sw-test](https://github.com/mdn/sw-test), which is a simple Star wars Lego image gallery. It uses a promise-powered function to read image data from a JSON object and load the images using Ajax, before displaying the images in a line down the page. We've kept things static and simple for now. It also registers, installs, and activates a service worker, and when more of the spec is supported by browsers it will cache all the files required so it will work offline!

![](demo-screenshot.png)

You can see the [source code on GitHub](https://github.com/mdn/sw-test/), and [view the example live](https://mdn.github.io/sw-test/). The one bit we'll call out here is the promise (see [app.js lines 22-47](https://github.com/mdn/sw-test/blob/gh-pages/app.js#L22-L47)), which is a modified version of what you read about above, in the [Promises test demo](https://github.com/mdn/promises-test). It is different in the following ways:

1. In the original, we only passed in a URL to an image we wanted to load. In this version, we pass in a JSON fragment containing all the data for a single image (see what they look like in [image-list.js](https://github.com/mdn/sw-test/blob/gh-pages/image-list.js)). This is because all the data for each promise resolve has to be passed in with the promise, as it is asynchronous. If you just passed in the url, and then tried to access the other items in the JSON separately when the `for()` loop is being iterated through later on, it wouldn't work, as the promise wouldn't resolve at the same time as the iterations are being done (that is a synchronous process.)
2. We actually resolve the promise with an array, as we want to make the loaded image blob available to the resolving function later on in the code, but also the image name, credits and alt text (see [app.js lines 31-34](https://github.com/mdn/sw-test/blob/gh-pages/app.js#L31-L34)). Promises will only resolve with a single argument, so if you want to resolve with multiple values, you need to use an array/object.
3. To access the resolved promise values, we then access this function as you'd then expect (see [app.js lines 60-64](https://github.com/mdn/sw-test/blob/gh-pages/app.js#L60-L64)). This may seem a bit odd at first, but this is the way promises work.

## Enter service workers

Now let's get on to service workers!

### Registering your worker

The first block of code in our app's JavaScript file — `app.js` — is as follows. This is our entry point into using service workers.

```js
if ("serviceWorker" in navigator) {
  navigator.serviceWorker
    .register("/sw-test/sw.js", { scope: "/sw-test/" })
    .then(function (reg) {
      // registration worked
      console.log("Registration succeeded. Scope is " + reg.scope);
    })
    .catch(function (error) {
      // registration failed
      console.log("Registration failed with " + error);
    });
}
```

1. The outer block performs a feature detection test to make sure service workers are supported before trying to register one.
2. Next, we use the {{domxref("ServiceWorkerContainer.register()") }} function to register the service worker for this site, which is just a JavaScript file residing inside our app (note this is the file's URL relative to the origin, not the JS file that references it.)
3. The `scope` parameter is optional, and can be used to specify the subset of your content that you want the service worker to control. In this case, we have specified '`/sw-test/'`, which means all content under the app's origin. If you leave it out, it will default to this value anyway, but we specified it here for illustration purposes.
4. The `.then()` promise function is used to chain a success case onto our promise structure. When the promise resolves successfully, the code inside it executes.
5. Finally, we chain a `.catch()` function onto the end that will run if the promise is rejected.

This registers a service worker, which runs in a worker context, and therefore has no DOM access. You then run code in the service worker outside of your normal pages to control their loading.

A single service worker can control many pages. Each time a page within your scope is loaded, the service worker is installed against that page and operates on it. Bear in mind therefore that you need to be careful with global variables in the service worker script: each page doesn't get its own unique worker.

> **참고:** Your service worker functions like a proxy server, allowing you to modify requests and responses, replace them with items from its own cache, and more.

> **참고:** One great thing about service workers is that if you use feature detection like we've shown above, browsers that don't support service workers can just use your app online in the normal expected fashion. Furthermore, if you use AppCache and SW on a page, browsers that don't support SW but do support AppCache will use that, and browsers that support both will ignore the AppCache and let SW take over.

#### Why is my service worker failing to register?

This could be for the following reasons:

1. You are not running your application through HTTPS.
2. The path to your service worker file is not written correctly — it needs to be written relative to the origin, not your app's root directory. In our example, the worker is at `https://mdn.github.io/sw-test/sw.js`, and the app's root is `https://mdn.github.io/sw-test/`. But the path needs to be written as `/sw-test/sw.js`, not `/sw.js`.
3. The service worker being pointed to is on a different origin to that of your app. This is also not allowed.

![](important-notes.png)

Also note:

- The service worker will only catch requests from clients under the service worker's scope.
- The max scope for a service worker is the location of the worker.
- If your server worker is active on a client being served with the `Service-Worker-Allowed` header, you can specify a list of max scopes for that worker.
- In Firefox, Service Worker APIs are hidden and cannot be used when the user is in [private browsing mode](https://support.mozilla.org/en-US/kb/private-browsing-use-firefox-without-history).

### Install and activate: populating your cache

After your service worker is registered, the browser will attempt to install then activate the service worker for your page/site.

The install event is fired when an install is successfully completed. The install event is generally used to populate your browser's offline caching capabilities with the assets you need to run your app offline. To do this, we use Service Worker's brand new storage API — {{domxref("cache")}} — a global on the service worker that allows us to store assets delivered by responses, and keyed by their requests. This API works in a similar way to the browser's standard cache, but it is specific to your domain. It persists until you tell it not to — again, you have full control.

> **참고:** The Cache API is not supported in every browser. (See the [Browser support](#browser_support) section for more information.) If you want to use this now, you could consider using a polyfill like the one available in [Google's Topeka demo](https://github.com/Polymer/topeka/blob/master/sw.js), or perhaps store your assets in [IndexedDB](/ko/docs/Web/API/IndexedDB_API).

Let's start this section by looking at a code sample — this is the [first block you'll find in our service worker](https://github.com/mdn/sw-test/blob/gh-pages/sw.js#L1-L18):

```js
this.addEventListener("install", function (event) {
  event.waitUntil(
    caches.open("v1").then(function (cache) {
      return cache.addAll([
        "/sw-test/",
        "/sw-test/index.html",
        "/sw-test/style.css",
        "/sw-test/app.js",
        "/sw-test/image-list.js",
        "/sw-test/star-wars-logo.jpg",
        "/sw-test/gallery/",
        "/sw-test/gallery/bountyHunters.jpg",
        "/sw-test/gallery/myLittleVader.jpg",
        "/sw-test/gallery/snowTroopers.jpg",
      ]);
    }),
  );
});
```

1. Here we add an `install` event listener to the service worker (hence `this`), and then chain a {{domxref("ExtendableEvent.waitUntil()") }} method onto the event — this ensures that the service worker will not install until the code inside `waitUntil()` has successfully occurred.
2. Inside `waitUntil()` we use the [`caches.open()`](/ko/docs/Web/API/CacheStorage/open) method to create a new cache called `v1`, which will be version 1 of our site resources cache. This returns a promise for a created cache; once resolved, we then call a function that calls `addAll()` on the created cache, which for its parameter takes an array of origin-relative URLs to all the resources you want to cache.
3. If the promise is rejected, the install fails, and the worker won't do anything. This is ok, as you can fix your code and then try again the next time registration occurs.
4. After a successful installation, the service worker activates. This doesn't have much of a distinct use the first time your service worker is installed/activated, but it means more when the service worker is updated (see the [Updating your service worker](#updating_your_service_worker) section later on.)

> **참고:** [localStorage](/ko/docs/Web/Guide/API/DOM/Storage) works in a similar way to service worker cache, but it is synchronous, so not allowed in service workers.

> **참고:** [IndexedDB](/ko/docs/Web/API/IndexedDB_API) can be used inside a service worker for data storage if you require it.

### Custom responses to requests

Now you've got your site assets cached, you need to tell service workers to do something with the cached content. This is easily done with the `fetch` event.

![](sw-fetch.png)

A `fetch` event fires every time any resource controlled by a service worker is fetched, which includes the documents inside the specified scope, and any resources referenced in those documents (for example if `index.html` makes a cross origin request to embed an image, that still goes through its service worker.)

You can attach a `fetch` event listener to the service worker, then call the `respondWith()` method on the event to hijack our HTTP responses and update them with your own magic.

```js
this.addEventListener("fetch", function (event) {
  event
    .respondWith
    // magic goes here
    ();
});
```

We could start by simply responding with the resource whose url matches that of the network request, in each case:

```js
this.addEventListener("fetch", function (event) {
  event.respondWith(caches.match(event.request));
});
```

`caches.match(event.request)` allows us to match each resource requested from the network with the equivalent resource available in the cache, if there is a matching one available. The matching is done via url and vary headers, just like with normal HTTP requests.

Let's look at a few other options we have when defining our magic (see our [Fetch API documentation](/ko/docs/Web/API/Fetch_API) for more information about {{domxref("Request")}} and {{domxref("Response")}} objects.)

1. The `{{domxref("Response.Response","Response()")}}` constructor allows you to create a custom response. In this case, we are just returning a simple text string:

   ```js
   new Response("Hello from your friendly neighbourhood service worker!");
   ```

2. This more complex `Response` below shows that you can optionally pass a set of headers in with your response, emulating standard HTTP response headers. Here we are just telling the browser what the content type of our synthetic response is:

   ```js
   new Response(
     "<p>Hello from your friendly neighbourhood service worker!</p>",
     {
       headers: { "Content-Type": "text/html" },
     },
   );
   ```

3. If a match wasn't found in the cache, you could tell the browser to simply {{domxref("GlobalFetch.fetch","fetch")}} the default network request for that resource, to get the new resource from the network if it is available:

   ```js
   fetch(event.request);
   ```

4. If a match wasn't found in the cache, and the network isn't available, you could just match the request with some kind of default fallback page as a response using {{domxref("CacheStorage.match","match()")}}, like this:

   ```js
   caches.match("/fallback.html");
   ```

5. You can retrieve a lot of information about each request by calling parameters of the {{domxref("Request")}} object returned by the {{domxref("FetchEvent")}}:

   ```js
   event.request.url;
   event.request.method;
   event.request.headers;
   event.request.body;
   ```

## Recovering failed requests

So `caches.match(event.request)` is great when there is a match in the service worker cache, but what about cases when there isn't a match? If we didn't provide any kind of failure handling, our promise would resolve with `undefined` and we wouldn't get anything returned.

Fortunately service workers' promise-based structure makes it trivial to provide further options towards success. We could do this:

```js
this.addEventListener("fetch", function (event) {
  event.respondWith(
    caches.match(event.request).then(function (response) {
      return response || fetch(event.request);
    }),
  );
});
```

If the resources isn't in the cache, it is requested from the network.

If we were being really clever, we would not only request the resource from the network; we would also save it into the cache so that later requests for that resource could be retrieved offline too! This would mean that if extra images were added to the Star Wars gallery, our app could automatically grab them and cache them. The following would do the trick:

```js
this.addEventListener("fetch", function (event) {
  event.respondWith(
    caches.match(event.request).then(function (resp) {
      return (
        resp ||
        fetch(event.request).then(function (response) {
          return caches.open("v1").then(function (cache) {
            cache.put(event.request, response.clone());
            return response;
          });
        })
      );
    }),
  );
});
```

Here we return the default network request with `return fetch(event.request)`, which returns a promise. When this promise is resolved, we respond by running a function that grabs our cache using `caches.open('v1')`; this also returns a promise. When that promise resolves, `cache.put()` is used to add the resource to the cache. The resource is grabbed from `event.request`, and the response is then cloned with `response.clone()` and added to the cache. The clone is put in the cache, and the original response is returned to the browser to be given to the page that called it.

Cloning the response is necessary because request and response streams can only be read once. In order to return the response to the browser and put it in the cache we have to clone it. So the original gets returned to the browser and the clone gets sent to the cache. They are each read once.

The only trouble we have now is that if the request doesn't match anything in the cache, and the network is not available, our request will still fail. Let's provide a default fallback so that whatever happens, the user will at least get something:

```js
this.addEventListener("fetch", function (event) {
  event.respondWith(
    caches
      .match(event.request)
      .then(function (resp) {
        return (
          resp ||
          fetch(event.request).then(function (response) {
            caches.open("v1").then(function (cache) {
              cache.put(event.request, response.clone());
            });
            return response;
          })
        );
      })
      .catch(function () {
        return caches.match("/sw-test/gallery/myLittleVader.jpg");
      }),
  );
});
```

We have opted for this fallback image because the only updates that are likely to fail are new images, as everything else is depended on for installation in the `install` event listener we saw earlier.

## <a id="Updating your service worker" name="Updating your service worker">Updating your service worker</a>

If your service worker has previously been installed, but then a new version of the worker is available on refresh or page load, the new version is installed in the background, but not yet activated. It is only activated when there are no longer any pages loaded that are still using the old service worker. As soon as there are no more such pages still loaded, the new service worker activates.

You'll want to update your `install` event listener in the new service worker to something like this (notice the new version number):

```js
this.addEventListener('install', function(event) {
  event.waitUntil(
    caches.open('v2').then(function(cache) {
      return cache.addAll([
        '/sw-test/',
        '/sw-test/index.html',
        '/sw-test/style.css',
        '/sw-test/app.js',
        '/sw-test/image-list.js',

        …

        // include other new resources for the new version...
      ]);
    })
  );
});
```

While this happens, the previous version is still responsible for fetches. The new version is installing in the background. We are calling the new cache `v2`, so the previous `v1` cache isn't disturbed.

When no pages are using the current version, the new worker activates and becomes responsible for fetches.

### Deleting old caches

You also get an `activate` event. This is a generally used to do stuff that would have broken the previous version while it was still running, for example getting rid of old caches. This is also useful for removing data that is no longer needed to avoid filling up too much disk space — each browser has a hard limit on the amount of cache storage that a given service worker can use. The browser does its best to manage disk space, but it may delete the Cache storage for an origin. The browser will generally delete all of the data for an origin or none of the data for an origin.

Promises passed into `waitUntil()` will block other events until completion, so you can rest assured that your clean-up operation will have completed by the time you get your first `fetch` event on the new cache.

```js
this.addEventListener("activate", function (event) {
  var cacheWhitelist = ["v2"];

  event.waitUntil(
    caches.keys().then(function (keyList) {
      return Promise.all(
        keyList.map(function (key) {
          if (cacheWhitelist.indexOf(key) === -1) {
            return caches.delete(key);
          }
        }),
      );
    }),
  );
});
```

## Developer tools

Chrome has `chrome://inspect/#service-workers`, which shows current service worker activity and storage on a device, and `chrome://serviceworker-internals`, which shows more detail and allows you to start/stop/debug the worker process. In the future they will have throttling/offline modes to simulate bad or non-existent connections, which will be a really good thing.

Firefox has also started to implement some useful tools related to service workers:

- You can navigate to [`about:debugging`](/ko/docs/Tools/about:debugging) to see what SWs are registered and update/remove them.
- When testing you can get around the HTTPS restriction by checking the "Enable Service Workers over HTTP (when toolbox is open)" option in the [Firefox Developer Tools settings](/ko/docs/Tools/Settings).

> **참고:** You may serve your app from `http://localhost` (e.g. using `me@localhost:/my/app$ python -m SimpleHTTPServer`) for local development. See [Security considerations](https://www.w3.org/TR/service-workers/#security-considerations)

## 명세서

{{Specifications}}

## See also

- [The Service Worker Cookbook](https://github.com/mdn/serviceworker-cookbook/)
- [Is ServiceWorker ready?](https://jakearchibald.github.io/isserviceworkerready/)
- Download the [Service Workers 101 cheatsheet](sw101.png).
- [Promises](/ko/docs/Web/JavaScript/Reference/Global_Objects/Promise)
- [Using web workers](/ko/docs/Web/Guide/Performance/Using_web_workers)

---
# Source: Web_CSS_font-family.md
---
---
title: font-family
slug: Web/CSS/font-family
---

{{CSSRef}}

CSS **`font-family`** 속성은 선택된 요소에 우선 순위가 지정된 font family 이름과 generic family 이름을 지정할 수 있게 해줍니다.

{{InteractiveExample("CSS Demo: font-family")}}

```css interactive-example-choice
font-family: Georgia, serif;
```

```css interactive-example-choice
font-family: "Gill Sans", sans-serif;
```

```css interactive-example-choice
font-family: sans-serif;
```

```css interactive-example-choice
font-family: serif;
```

```css interactive-example-choice
font-family: cursive;
```

```css interactive-example-choice
font-family: system-ui;
```

```html interactive-example
<section id="default-example">
  <p id="example-element">
    London. Michaelmas term lately over, and the Lord Chancellor sitting in
    Lincoln's Inn Hall. Implacable November weather. As much mud in the streets
    as if the waters had but newly retired from the face of the earth, and it
    would not be wonderful to meet a Megalosaurus, forty feet long or so,
    waddling like an elephantine lizard up Holborn Hill.
  </p>
</section>
```

```css interactive-example
section {
  font-size: 1.2em;
}
```

값은 콤마로 구분하여 대체가 될 수 있음을 나타냅니다. 브라우저는 폰트 목록에서 컴퓨터에 설치되어 있거나 {{cssxref("@font-face")}} 규칙을 이용하여 다운로드 받을 수 있는 폰트 중 가장 첫번째 폰트를 선택할 것입니다.

웹 제작자는 font-family 목록에 최소 한 개의 generic family를 추가해야 하는데, 시스템이나 {{cssxref("@font-face")}} 규칙을 이용 해 다운로드 받은 폰트 중에 특정 폰트가 있다는 것을 보장할 수 없기 때문입니다. generic family는 브라우저가 대체할 수 있는 폰트가 필요한 경우 선택할 수 있게 해줍니다.

font-size를 설정하거나 다른 폰트 관련 속성들을 한꺼번에 지정하는 경우 {{cssxref("font")}}가 단축형으로 자주 사용됩니다.

## 구문

```css
/* A font family name and a generic family name */
font-family:
  Gill Sans Extrabold,
  sans-serif;
font-family: "Goudy Bookletter 1911", sans-serif;

/* A generic family name only */
font-family: serif;
font-family: sans-serif;
font-family: monospace;
font-family: cursive;
font-family: fantasy;
font-family: system-ui;

/* Global values */
font-family: inherit;
font-family: initial;
font-family: unset;
```

The `font-family` property lists one or more font families, separated by commas. Each font family is specified as either a [\<family-name>](#family-name) or a [\<generic-name>](#generic-name) value.

The example below lists two font families, the first with a `<family-name>` and the second with a `<generic-name>`:

```
font-family: Gill Sans Extrabold, sans-serif;
```

### 값

- `<family-name>`
  - : The name of a font family. For example, "Times" and "Helvetica" are font families. Font family names containing whitespace should be quoted.

- `<generic-name>`
  - : Generic font families are a fallback mechanism, a means of preserving some of the style sheet author's intent when none of the specified fonts are available. Generic family names are keywords and must not be quoted. A generic font family should be the last item in the list of font family names. The following keywords are defined:
    - `serif`
      - : Glyphs have finishing strokes, flared or tapering ends, or have actual serifed endings.
        E.g. Lucida Bright, Lucida Fax, Palatino, "Palatino Linotype", Palladio, "URW Palladio", serif.
    - `sans-serif`
      - : Glyphs have stroke endings that are plain.
        E.g. "Open Sans", "Fira Sans", "Lucida Sans", "Lucida Sans Unicode", "Trebuchet MS", "Liberation Sans", "Nimbus Sans L", sans-serif.
    - `monospace`
      - : All glyphs have the same fixed width.
        E.g. "Fira Mono", "DejaVu Sans Mono", Menlo, Consolas, "Liberation Mono", Monaco, "Lucida Console", monospace.
    - `cursive`
      - : Glyphs in cursive fonts generally have either joining strokes or other cursive characteristics beyond those of italic typefaces. The glyphs are partially or completely connected, and the result looks more like handwritten pen or brush writing than printed letterwork.
        E.g. "Brush Script MT", "Brush Script Std", "Lucida Calligraphy", "Lucida Handwriting", "Apple Chancery", cursive.
    - `fantasy`
      - : Fantasy fonts are primarily decorative fonts that contain playful representations of characters.
        E.g. Papyrus, Herculanum, Party LET, Curlz MT, Harrington, fantasy.
    - `system-ui`
      - : Glyphs are taken from the default user interface font on a given platform. Because typographic traditions vary widely across the world, this generic is provided for typefaces that don't map cleanly into the other generics.

### 유효한 폰트 패밀리 이름

Font family names must either be given quoted as strings, or unquoted as a sequence of one or more identifiers. This means that punctuation characters and digits at the start of each token must be escaped in unquoted font family names.

For example, the following declarations are valid:

```css
font-family:
  Gill Sans Extrabold,
  sans-serif;
font-family: "Goudy Bookletter 1911", sans-serif;
```

The following declarations are **invalid**:

```css example-bad
font-family:
  Goudy Bookletter 1911,
  sans-serif;
font-family: Red/Black, sans-serif;
font-family:
  "Lucida" Grande,
  sans-serif;
font-family: Ahem!, sans-serif;
font-family:
  test @foo,
  sans-serif;
font-family: #POUND, sans-serif;
font-family:
  Hawaii 5-0,
  sans-serif;
```

### 형식 구문

{{csssyntax}}

## 예제

### Some common font families

```css
.serif {
  font-family:
    Times,
    Times New Roman,
    Georgia,
    serif;
}

.sansserif {
  font-family: Verdana, Arial, Helvetica, sans-serif;
}

.monospace {
  font-family:
    Lucida Console,
    Courier,
    monospace;
}

.cursive {
  font-family: cursive;
}

.fantasy {
  font-family: fantasy;
}
```

```html hidden
<div class="serif">This is an example of a serif font.</div>
<div class="sansserif">This is an example of a sans-serif font.</div>
<div class="monospace">This is an example of a monospace font.</div>
<div class="cursive">This is an example of a cursive font.</div>
<div class="fantasy">This is an example of a fantasy font.</div>
```

{{ EmbedLiveSample('Some_common_font_families','600','220') }}

## 명세

{{Specifications}}

{{cssinfo}}

## 브라우저 호환성

{{Compat}}

---
# Source: Web_HTML_Element_select.md
---
---
title: <select>
slug: Web/HTML/Element/select
---

{{HTMLSidebar}}

**HTML `<select>` 요소**는 옵션 메뉴를 제공하는 컨트롤을 나타냅니다.

{{InteractiveExample("HTML Demo: &lt;select&gt;", "tabbed-standard")}}

```html interactive-example
<label for="pet-select">Choose a pet:</label>

<select name="pets" id="pet-select">
  <option value="">--Please choose an option--</option>
  <option value="dog">Dog</option>
  <option value="cat">Cat</option>
  <option value="hamster">Hamster</option>
  <option value="parrot">Parrot</option>
  <option value="spider">Spider</option>
  <option value="goldfish">Goldfish</option>
</select>
```

```css interactive-example
label {
  font-family: sans-serif;
  font-size: 1rem;
  padding-right: 10px;
}

select {
  font-size: 0.9rem;
  padding: 2px 5px;
}
```

위의 예제는 일반적인 `<select>` 사용법을 시연합니다. {{htmlelement("label")}}과 연결해 접근성을 향상할 수 있도록 [`id`](/ko/docs/Web/HTML/Global_attributes#id) 특성을, 서버로 전송할 데이터의 이름을 위해 [`name`](/ko/docs/Web/HTML/Element/select#name) 특성을 적용했습니다. 메뉴의 각 옵션은 `<select>` 안의 {{htmlelement("option")}}으로 정의합니다.

모든 `<option>`은 자신이 선택됐을 때 값으로써 사용할 [`value`](/ko/docs/Web/HTML/Element/option#value) 특성이 필요합니다. 그러나 `value` 특성을 지정하지 않은 경우, 대신 자기 안의 텍스트를 값으로 사용합니다. [`selected`](/ko/docs/Web/HTML/Element/option#selected) 특성을 지정하면 해당 옵션을 선택한 상태로 페이지를 불러옵니다.

`<select>` 요소를 조작할 때 사용할 수 있는 여러가지 고유 특성이 존재합니다. [`multiple`](/ko/docs/Web/HTML/Element/select#multiple) 특성을 사용하면 다수의 항목을 동시에 선택할 수 있고, [`size`](/ko/docs/Web/HTML/Element/select#size) 특성은 한 번에 노출되는 항목의 수를 조절할 수 있습니다. `required`, `disabled`, `autofocus` 등 일반적인 양식 입력 요소의 특성도 사용할 수 있습니다.

`<option>` 요소를 {{htmlelement("optgroup")}} 요소 안에 배치하면 드롭다운 내에서 옵션 그룹을 나눌 수 있습니다.

For further examples, see [The native form widgets: Drop-down content](/ko/docs/Learn/HTML/Forms/The_native_form_widgets#Drop-down_content).

## 특성

이 요소는 [전역 특성](/ko/docs/Web/HTML/Global_attributes)을 포함합니다.

- `autocomplete`
  - : {{glossary("user agent", "사용자 에이전트")}}의 자동완성 기능을 지원하는 {{domxref("DOMString")}}. 가능한 값의 전체 목록과, 자동완성의 상세 사용법은 [HTML `autocomplete` 특성](/ko/docs/Web/HTML/Attributes/autocomplete) 문서를 참고하세요.
- `autofocus`
  - : 지정한 경우, 페이지를 불러왔을 때 자동으로 포커스를 부여합니다. 문서 내에서 하나의 양식 요소만 `autofocus` 특성을 가질 수 있습니다.
- `disabled`
  - : 지정한 경우, 사용자와 `<select>` 요소의 모든 상호작용을 막습니다. 지정하지 않은 경우에도 {{htmlelement("fieldset")}} 등 부모 요소의 `disabled` 특성을 상속하므로 비활성 상태가 될 수 있습니다.
- `form`
  - : `<select>`와 연결할 {{HTMLElement("form")}} 요소("양식 소유자"). 같은 문서에 존재하는 `<form>` 요소의 [`id`](/ko/docs/Web/HTML/Global_attributes#id) 특성 값을 사용해야 합니다. `form` 특성을 지정하지 않았으나 조상 중 `<form>` 요소가 존재하면 해당 `<form>`과 연결됩니다.
  - : `form` 특성을 사용하면 `<select>`를 `<form>` 요소에 넣지 않고도 연결할 수 있고, 조상 중 `<form>`이 있더라도 소유자를 재정의할 수 있습니다.
- `multiple`
  - : 지정한 경우, 메뉴에서 다수의 옵션을 선택할 수 있습니다. 지정하지 않은 경우 하나만 선택 가능합니다. 대부분의 브라우저는 `multiple` 특성이 존재하면 드롭다운 메뉴 대신 스크롤 가능한 목록 상자를 보여줍니다.
- `name`
  - : 컨트롤의 이름.
- `required`
  - : 옵션 중 값으로 비어있지 않은 문자열을 값으로 하는 항목을 반드시 선택해야 함을 나타냅니다.
- `size`
  - : `<select>`를 (`multiple` 특성 사용 등의 이유로) 스크롤 가능한 목록 상자로 표현할 때 지정한 경우, 목록에서 한 번에 볼 수 있는 옵션 줄 수를 나타냅니다. 브라우저가 `<select>` 요소를 반드시 스크롤 가능한 목록 상자로 표현해야 하는 것은 아닙니다. 기본값은 0입니다.

> **참고:** HTML5 명세에 따르면 `size`의 기본값은 1이어야 합니다. 그러나 실제로 기본값을 1로 적용하면 일부 웹 사이트가 망가지는 것으로 밝혀졌으며 어떠한 브라우저도 기본값으로 1을 사용하지 않습니다. Mozilla도 당분간 Firefox의 기본값을 0으로 유지하기로 결정했습니다.

## Usage notes

### Selecting multiple options

On a desktop computer, there are a number of ways to select multiple options in a `<select>` element with a `multiple` attribute:

Mouse users can hold the <kbd>Ctrl</kbd>, <kbd>Command</kbd>, or <kbd>Shift</kbd> keys (depending on what makes sense for your operating system) and then click multiple options to select/deselect them.</p>

> **Warning:** The mechanism for selecting multiple non-contiguous items via the keyboard described below currently only seems to work in Firefox. Also note that on macOS, the <kbd>Ctrl</kbd> + <kbd>Up</kbd> and <kbd>Ctrl</kbd> + <kbd>Down</kbd> shortcuts conflict with the OS default shortcuts for <em>Mission Control</em> and <em>Application windows</em>, so you'll have to turn these off before it will work.

Keyboard users can select multiple contiguous items by:

- Focusing on the `<select>` element (e.g. using <kbd>Tab</kbd>).
- Selecting an item at the top or bottom of the range they want to select using the <kbd>Up</kbd> and <kbd>Down</kbd> cursor keys to go up and down the options.
- Holding down the <kbd>Shift</kbd> key and then using the <kbd>Up</kbd> and <kbd>Down</kbd> cursor keys to increase or decrease the range of items selected.

Keyboard users can select multiple non-contiguous items by:

- Focusing on the `<select>` element (e.g. using <kbd>Tab</kbd>).
- Holding down the <kbd>Ctrl</kbd> key then using the <kbd>Up</kbd> and <kbd>Down</kbd> cursor keys to change the "focused" select option, i.e. the one that will be selected if you choose to do so. The "focused" select option is highlighted with a dotted outline, in the same way as a keyboard-focused link.
- Pressing <kbd>Space</kbd> to select/deselect "focused" select options.

## CSS 스타일링

`<select>` 요소는 CSS를 사용해 스타일을 적용하기 어렵기로 유명합니다. 물론 [박스 모델](/ko/docs/Web/CSS/CSS_Box_Model/Introduction_to_the_CSS_box_model)이나 [글씨체](/ko/docs/Web/CSS/CSS_Fonts) 등 일부분은 다른 요소처럼 바꿀 수 있으며, {{cssxref("appearance")}} 속성을 사용하면 기본 시스템 외형을 제거할 수도 있습니다.

그러나 `<select>` 요소의 내부 구조는 복잡해 통제하기 힘들며, 브라우저간의 차이로 인해 일관적이지 않은 결과가 나올 수도 있습니다. 요소의 모든 부분을 통제해야 할 경우 적합한 스타일링 방법을 제공하는 라이브러리를 고려하세요. 아니면 다른 요소와 JavaScript, [WAI-ARIA](/ko/docs/Learn/Accessibility/WAI-ARIA_basics)를 사용해 완전히 별도의 드롭다운 메뉴를 만들어보세요.

## 예제

### 기본 메뉴

```html
<!-- 두 번째 값이 처음부터 선택된 상태 -->
<select name="choice">
  <option value="first">First Value</option>
  <option value="second" selected>Second Value</option>
  <option value="third">Third Value</option>
</select>
```

{{EmbedLiveSample("기본_메뉴", "", "100")}}

### 여러 기능을 갖춘 복잡한 메뉴

```html
<label
  >Please choose one or more pets:
  <select name="pets" multiple size="4">
    <optgroup label="4-legged pets">
      <option value="dog">Dog</option>
      <option value="cat">Cat</option>
      <option value="hamster" disabled>Hamster</option>
    </optgroup>
    <optgroup label="Flying pets">
      <option value="parrot">Parrot</option>
      <option value="macaw">Macaw</option>
      <option value="albatross">Albatross</option>
    </optgroup>
  </select>
</label>
```

{{EmbedLiveSample("여러_기능을_갖춘_복잡한_메뉴", "", "100")}}

- `multiple` 특성으로 인해 여러 옵션을 같이 선택할 수 있습니다.
- `size` 특성으로 인해 최대 4개의 옵션만 보입니다.
- {{htmlelement("optgroup")}} 요소를 사용해 옵션을 두 개의 분리된 그룹으로 나눴습니다. 옵션 그룹은 순전히 시각적인 구분으로, 보통 굵은 글씨체의 옵션명 및 들여쓰기한 옵션 구성원으로 표현합니다.
- "Hamster" 옵션에는 `disabled` 특성이 있으므로 선택할 수 없습니다.

## 기술 요약

<table class="properties">
  <tbody>
    <tr>
      <th scope="row">
        <a href="/ko/docs/Web/Guide/HTML/Content_categories">콘텐츠 카테고리</a>
      </th>
      <td>
        <a href="/ko/docs/Web/Guide/HTML/Content_categories#플로우_콘텐츠"
          >플로우 콘텐츠</a
        >,
        <a href="/ko/docs/Web/Guide/HTML/Content_categories#구문_콘텐츠"
          >구문 콘텐츠</a
        >,
        <a href="/ko/docs/Web/Guide/HTML/Content_categories#대화형_콘텐츠"
          >대화형 콘텐츠</a
        >,
        <a href="/ko/docs/Web/Guide/HTML/Content_categories#양식_관련_콘텐츠"
          >양식 관련 콘텐츠</a
        >(<a href="/ko/docs/Web/Guide/HTML/Content_categories#나열됨">나열됨</a
        >,
        <a href="/ko/docs/Web/Guide/HTML/Content_categories#레이블_가능"
          >레이블 가능</a
        >,
        <a href="/ko/docs/Web/Guide/HTML/Content_categories#초기화_가능"
          >초기화 가능</a
        >,
        <a href="/ko/docs/Web/Guide/HTML/Content_categories#제출_가능"
          >제출 가능</a
        >).
      </td>
    </tr>
    <tr>
      <th scope="row">가능한 콘텐츠</th>
      <td>
        0개 이상의 {{HTMLElement("option")}} 또는
        {{HTMLElement("optgroup")}} 요소.
      </td>
    </tr>
    <tr>
      <th scope="row">태그 생략</th>
      <td>{{no_tag_omission}}</td>
    </tr>
    <tr>
      <th scope="row">가능한 부모 요소</th>
      <td>
        <a href="/ko/docs/Web/Guide/HTML/Content_categories#구문_콘텐츠"
          >구문 콘텐츠</a
        >를 허용하는 모든 요소.
      </td>
    </tr>
    <tr>
      <th scope="row">가능한 ARIA 역할</th>
      <td><a href='/ko/docs/Web/Accessibility/ARIA/Roles/menu_role'><code>menu</code></a></td>
    </tr>
    <tr>
      <th scope="row">DOM 인터페이스</th>
      <td>{{domxref("HTMLSelectElement")}}</td>
    </tr>
  </tbody>
</table>

## 명세

{{Specifications}}

## 브라우저 호환성

{{Compat}}

## 같이 보기

- `<select>`가 발사하는 이벤트: {{event("change")}}, {{event("input")}}

---
# Source: Web_API_IndexedDB_API_Basic_Terminology.md
---
---
title: IndexedDB key characteristics and basic terminology
slug: Web/API/IndexedDB_API/Basic_Terminology
---

{{DefaultAPISidebar("IndexedDB")}}

이 문서에서는 IndexedDB의 주요 특성을 설명하고, IndexedDB API를 이해하는 데 관련된 몇 가지 필수적인 용어를 소개합니다.

유용한 문서들:

- API 사용법에 대한 상세한 튜토리얼을 원한다면 [IndexedDB 사용하기](/ko/docs/Web/API/IndexedDB_API/Using_IndexedDB)를 확인해보세요.
- IndexedDB API의 참조 문서를 원한다면, [IndexedDB API](/ko/docs/Web/API/IndexedDB_API) 문서와 IndexedDB에서 사용되는 객체 타입에 대한 하위 문서들을 확인하세요.
- 브라우저가 어떻게 백그라운드에서 데이터를 저장하는지에 대한 더 자세한 정보는 [Browser storage quotas and eviction criteria](/ko/docs/Web/API/Storage_API/Storage_quotas_and_eviction_criteria)에서 확인하세요.

## 주요 특성

IndexedDB는 데이터를 사용자의 브라우저에 영구적으로 저장하는 방법입니다. 네트워크 가용성에 관계 없이 풍부한 쿼리 기능을 갖춘 웹 어플리케이션을 만들 수 있기 때문에, 온라인과 오프라인에서 모두 동작합니다. IndexedDB는 대규모 데이터(예: 도서관의 DVD 목록)를 저장하고 지속적인 인터넷 연결을 필요로 하지 않는 작업(예: 메일 클라이언트, 투두 리스트, 메모장)을 위한 어플리케이션에 유용합니다.

IndexedDB는 "키"로 인덱싱된 객체를 저장하고 검색할 수 있습니다. 데이터베이스의 모든 변화는 트랜잭션 내에서 일어납니다. 대부분의 웹 스토리지 솔루션처럼, IndexedDB는 [동일 출처 정책](https://www.w3.org/Security/wiki/Same_Origin_Policy)을 따릅니다. 그래서 어떤 도메인에서 저장된 데이터는 다른 도메인에서 접근할 수 없습니다.

만약 다른 종류의 데이터베이스를 사용하고 있다면, IndexedDB를 사용하면서 당황할 수 있습니다. 그렇기 때문에 IndexedDB의 다음 주요 특성들을 염두에 두어야 합니다:

- **IndexedDB 데이터베이스는 키-값 쌍을 저장합니다.** 값은 복잡한 구조의 객체일 수 있고, 키는 그러한 객체의 프로퍼티일 수 있습니다. 인덱스는 빠른 검색이나 정렬된 열거를 위해 객체의 아무 프로퍼티나 사용하여 생성할 수 있습니다. 키는 이진 객체일 수 있습니다.
- **IndexedDB는 트랜잭션 데이터베이스 모델에 기반합니다.** IndexedDB에서 일어나는 모든 일은 [트랜잭션](#transaction) 내에서 일어납니다. IndexedDB API는 인덱스, 테이블, 커서 등을 나타내는 다양한 객체를 제공하지만, 이 객체들은 모두 특정 트랜잭션에 얽매여 있습니다. 그러므로, 트랜잭션 밖에서 명령을 실행하거나 커서를 열 수 없습니다. 트랜잭션은 지정된 수명이 있기 때문에 종료된 후에 트랜잭션을 사용하려고 시도하면 예외를 발생시킵니다. 또한, 트랜잭션은 자동으로 커밋되며 수동으로 커밋될 수 없습니다.

  이 트랜잭션 모델은 유저가 웹 어플리케이션을 두 개의 다른 탭에서 동시에 열었을 때를 고려하면 매우 유용합니다. 트랜잭션 작업이 없으면, 두 인스턴스는 서로의 변경에 개입할 수 있습니다. 만약 데이터베이스의 트랜잭션이 친숙하지 않다면, [트랜잭션에 대한 Wikipedia 문서](https://en.wikipedia.org/wiki/Database_transaction)를 읽어보세요. 정의 섹션에서 [트랜잭션](#transaction) 문서도 확인해보세요.

- **IndexedDB API는 대체로 비동기적입니다.** API는 값을 반환하여 데이터를 제공하지 않습니다. 대신 콜백 함수를 전달해야 합니다. 동기적으로 데이터베이스에 값을 "저장"하거나, 데이터베이스에서 값을 "검색"할 수 없습니다. 대신, 데이터베이스 동작이 일어날 것을 "요청"합니다. 동작이 끝나면 DOM 이벤트가 발생하게 되고, 해당 이벤트의 타입을 통해 동작이 성공했는지 실패했는지를 알 수 있습니다. 처음에는 조금 복잡하게 들리겠지만, 이 방식에는 안전장치가 내장되어 있습니다. 이것은 [XMLHttpRequest](/ko-KR/docs/Web/API/XMLHttpRequest)가 동작하는 방식과 크게 다르지 않습니다.
- **IndexedDB는 많은 요청을 사용합니다.** 요청은 앞서 언급했던 성공 또는 실패 DOM 이벤트를 받는 객체를 말합니다. 이 객체는 `onsuccess`와 `onerror` 프로퍼티를 가지며, `addEventListener()`와 `removeEventListener()`를 호출할 수 있습니다. 또한 요청의 상태를 나타내는 `readyState`, `result`, `errorCode`와 같은 프로퍼티를 가집니다. `result` 프로퍼티는 요청이 어떻게 생성되었는지(예: `IDBCursor`의 인스턴스 또는 데이터베이스에 추가한 어떤 값의 키)에 따라 특별하게 동작합니다.
- **IndexedDB는 결과를 사용할 수 있을 때 DOM 이벤트를 통해 통지합니다.** DOM 이벤트는 항상 `type` 프로퍼티를 가집니다 (IndexedDB에서는 거의 대부분 `"success"` 또는 `"error"`로 설정됩니다.). DOM 이벤트는 이벤트가 향하는 곳이 어디인지를 나타내는 `target` 프로퍼티도 가집니다. 대부분의 경우에, 이벤트의 `target` 프로퍼티는 데이터베이스 동작의 결과로 생성된 `IDBRequest` 객체를 가리킵니다. 성공 이벤트는 버블링을 일으키지 않으며, 취소될 수 없습니다. 에러 이벤트는 반대로 버블링을 일으키고, 취소될 수도 있습니다. 에러 이벤트는 취소되지 않는 한 실행 중인 모든 트랜잭션을 중단하므로 이는 매우 중요합니다.
- **IndexedDB는 객체지향적입니다.** IndexedDB는 행과 열의 컬렉션으로 대표되는 테이블을 사용하는 관계형 데이터베이스가 아닙니다. 이는 어플리케이션을 설계하고 구축하는 방식에 영향을 끼치는 중요하고 근본적인 차이입니다.

  전통적인 관계형 데이터 저장소에서는 데이터 행의 컬렉션과 명명된 자료형의 데이터 열을 저장하는 테이블을 갖습니다. 반면에 IndexedDB는 특정 타입의 데이터를 저장할 객체 저장소를 생성하고, JavaScript 객체를 저장소에 저장합니다. 각 객체 저장소는 쿼리와 순회를 효율적으로 만들어주는 인덱스 컬렉션을 갖습니다. 만약 객체지향 데이터베이스 관리 시스템에 친숙하지 않다면, [객체지향 데이터베이스에 대한 Wikipedia 문서](https://en.wikipedia.org/wiki/Object_database)를 읽어보세요.

- **IndexedDB does not use Structured Query Language (SQL).** It uses queries on an index that produces a cursor, which you use to iterate across the result set. If you are not familiar with NoSQL systems, read the [Wikipedia article on NoSQL](https://en.wikipedia.org/wiki/NoSQL).
- **IndexedDB adheres to a same-origin policy**. An origin is the domain, application layer protocol, and port of a URL of the document where the script is being executed. Each origin has its own associated set of databases. Every database has a name that identifies it within an origin.

  The security boundary imposed on IndexedDB prevents applications from accessing data with a different origin. For example, while an app or a page in `http://www.example.com/app/` can retrieve data from `http://www.example.com/dir/`, because they have the same origin, it cannot retrieve data from `http://www.example.com:8080/dir/` (different port) or `https://www.example.com/dir/` (different protocol), because they have different origins.

  > **Note:** Third party window content (e.g. {{htmlelement("iframe")}} content) can access the IndexedDB store for the origin it is embedded into, unless the browser is set to [never accept third party cookies](https://support.mozilla.org/en-US/kb/third-party-cookies-firefox-tracking-protection) (see [Firefox bug 1147821](https://bugzil.la/1147821).)

### Limitations

IndexedDB is designed to cover most cases that need client-side storage. However, it is not designed for a few cases like the following:

- Internationalized sorting. Not all languages sort strings in the same way, so internationalized sorting is not supported. While the database can't store data in a specific internationalized order, you can sort the data that you've read out of the database yourself. Note, however, that [locale-aware sorting](/ko/docs/Web/API/IndexedDB_API/Using_IndexedDB#locale-aware_sorting) has been allowed with an experimental flag enabled (currently for Firefox only) since Firefox 43.
- Synchronizing. The API is not designed to take care of synchronizing with a server-side database. You have to write code that synchronizes a client-side indexedDB database with a server-side database.
- Full text searching. The API does not have an equivalent of the `LIKE` operator in SQL.

In addition, be aware that browsers can wipe out the database, such as in the following conditions:

- The user requests a wipe out. Many browsers have settings that let users wipe all data stored for a given website, including cookies, bookmarks, stored passwords, and IndexedDB data.
- The browser is in private browsing mode. Some browsers, have "private browsing" (Firefox) or "incognito" (Chrome) modes. At the end of the session, the browser wipes out the database.
- The disk or quota limit has been reached.
- The data is corrupt.
- An incompatible change is made to the feature.

The exact circumstances and browser capabilities change over time, but the general philosophy of the browser vendors is to make the best effort to keep the data when possible.

## Core terminology

This section defines and explains core terminology relevant to understanding the IndexedDB API.

### Database

#### database

A repository of information, typically comprising one or more [_object stores_](#object_store). Each database must have the following:

- Name. This identifies the database within a specific origin and stays constant throughout its lifetime. The name can be any string value (including an empty string).
- Current [_version_](#version). When a database is first created, its version is the integer 1 if not specified otherwise. Each database can have only one version at any given time.

#### database connection

An operation created by opening a _[database](#database)_. A given database can have multiple connections at the same time.

#### durable

In Firefox, IndexedDB used to be **durable**, meaning that in a readwrite transaction a {{domxref("IDBTransaction.complete_event", "complete")}} event was fired only when all data was guaranteed to have been flushed to disk.

As of Firefox 40, IndexedDB transactions have relaxed durability guarantees to increase performance (see [Webkit bug 1112702](https://bugzil.la/1112702)), which is the same behavior as other IndexedDB-supporting browsers. In this case the {{domxref("IDBTransaction.complete_event", "complete")}} event is fired after the OS has been told to write the data but potentially before that data has actually been flushed to disk. The event may thus be delivered quicker than before, however, there exists a small chance that the entire transaction will be lost if the OS crashes or there is a loss of system power before the data is flushed to disk. Since such catastrophic events are rare, most consumers should not need to concern themselves further.

> **Note:** In Firefox, if you wish to ensure durability for some reason (e.g. you're storing critical data that cannot be recomputed later) you can force a transaction to flush to disk before delivering the `complete` event by creating a transaction using the experimental (non-standard) `readwriteflush` mode (see {{domxref("IDBDatabase.transaction")}}.) This is currently experimental, and can only be used if the `dom.indexedDB.experimental` pref is set to `true` in `about:config`.

#### index

An index is a specialized object store for looking up records in another object store, called the _referenced object store_. The index is a persistent key-value storage where the value part of its records is the key part of a record in the referenced object store. The records in an index are automatically populated whenever records in the referenced object store are inserted, updated, or deleted. Each record in an index can point to only one record in its referenced object store, but several indexes can reference the same object store. When the object store changes, all indexes that refer to the object store are automatically updated.

Alternatively, you can also look up records in an object store using the [key](#key).

To learn more on using indexes, see [Using IndexedDB](/ko/docs/Web/API/IndexedDB_API/Using_IndexedDB#using_an_index). For the reference documentation on index, see [IDBKeyRange](/ko/docs/Web/API/IDBKeyRange).

#### object store

The mechanism by which data is stored in the database. The object store persistently holds records, which are key-value pairs. Records within an object store are sorted according to the _[keys](#key)_ in an ascending order.

Every object store must have a name that is unique within its database. The object store can optionally have a _[key generator](#key_generator)_ and a _[key path](#key_path)_. If the object store has a key path, it is using _[in-line keys](#in-line_key)_; otherwise, it is using _[out-of-line keys](#out-of-line_key)_.

For the reference documentation on object store, see {{domxref("IDBObjectStore")}}.

#### request

The operation by which reading and writing on a database is done. Every request represents one read or write operation.

#### transaction

An atomic set of data-access and data-modification operations on a particular database. It is how you interact with the data in a database. In fact, any reading or changing of data in the database must happen in a transaction.

A database connection can have several active transactions associated with it at a time, so long as the writing transactions do not have overlapping [_scopes_](#scope). The scope of transactions, which is defined at creation, determines which object stores the transaction can interact with and remains constant for the lifetime of the transaction. So, for example, if a database connection already has a writing transaction with a scope that just covers the `flyingMonkey` object store, you can start a second transaction with a scope of the `unicornCentaur` and `unicornPegasus` object stores. As for reading transactions, you can have several of them — even overlapping ones.

Transactions are expected to be short-lived, so the browser can terminate a transaction that takes too long, in order to free up storage resources that the long-running transaction has locked. You can abort the transaction, which rolls back the changes made to the database in the transaction. And you don't even have to wait for the transaction to start or be active to abort it.

The three modes of transactions are: `readwrite`, `readonly`, and `versionchange`. The only way to create and delete object stores and indexes is by using a [`versionchange`](/ko/docs/Web/API/IDBDatabase/versionchange_event) transaction. To learn more about transaction types, see the reference article for [IndexedDB](/ko/docs/Web/API/IndexedDB_API).

Because everything happens within a transaction, it is a very important concept in IndexedDB. To learn more about transactions, especially on how they relate to versioning, see {{domxref("IDBTransaction")}}, which also has reference documentation.

#### version

When a database is first created, its version is the integer 1. Each database has one version at a time; a database can't exist in multiple versions at once. The only way to change the version is by opening it with a greater version than the current one.

### Key and value

#### in-line key

A key that is stored as part of the stored value. It is found using a _key path_. An in-line key can be generated using a generator. After the key has been generated, it can then be stored in the value using the key path or it can also be used as a key.

#### key

A data value by which stored values are organized and retrieved in the object store. The object store can derive the key from one of three sources: a _[key generator](#key_generator)_, a _[key path](#key_path)_, or an explicitly specified value. The key must be of a data type that has a number that is greater than the one before it. Each record in an object store must have a key that is unique within the same store, so you cannot have multiple records with the same key in a given object store.

A key can be one of the following types: [string](/ko/docs/Web/JavaScript/Reference/Global_Objects/String), [date](/ko/docs/Web/JavaScript/Reference/Global_Objects/Date), float, a binary blob, and [array](/ko/docs/Web/JavaScript/Reference/Global_Objects/Array). For arrays, the key can range from an empty value to infinity. And you can include an array within an array.

Alternatively, you can also look up records in an object store using the _[index](#index)._

#### key generator

A mechanism for producing new keys in an ordered sequence. If an object store does not have a key generator, then the application must provide keys for records being stored. Generators are not shared between stores. This is more a browser implementation detail, because in web development, you don't really create or access key generators.

#### key path

Defines where the browser should extract the key from in the object store or index. A valid key path can include one of the following: an empty string, a JavaScript identifier, or multiple JavaScript identifiers separated by periods or an array containing any of those. It cannot include spaces.

#### out-of-line key

A key that is stored separately from the value being stored.

#### value

Each record has a value, which could include anything that can be expressed in JavaScript, including [boolean](/ko/docs/Web/JavaScript/Reference/Global_Objects/Boolean), [number](/ko/docs/Web/JavaScript/Reference/Global_Objects/Number), [string](/ko/docs/Web/JavaScript/Reference/Global_Objects/String), [date](/ko/docs/Web/JavaScript/Reference/Global_Objects/Date), [object](/ko/docs/Web/JavaScript/Reference/Global_Objects/Object), [array](/ko/docs/Web/JavaScript/Reference/Global_Objects/Array), [regexp](/ko/docs/Web/JavaScript/Reference/Global_Objects/RegExp), [undefined](/ko/docs/Web/JavaScript/Reference/Global_Objects/undefined), and null.

When an object or array is stored, the properties and values in that object or array can also be anything that is a valid value.

[Blobs](/ko/docs/Web/API/Blob) and files can be stored, cf. [specification](https://w3c.github.io/IndexedDB/).

### Range and scope

#### cursor

A mechanism for iterating over multiple records with a _key range_. The cursor has a source that indicates which index or object store it is iterating. It has a position within the range, and moves in a direction that is increasing or decreasing in the order of record keys. For the reference documentation on cursors, see {{domxref("IDBCursor")}}.

#### key range

A continuous interval over some data type used for keys. Records can be retrieved from object stores and indexes using keys or a range of keys. You can limit or filter the range using lower and upper bounds. For example, you can iterate over all values of a key between x and y.

For the reference documentation on key range, see {{domxref("IDBKeyRange")}}.

#### scope

The set of object stores and indexes to which a transaction applies. The scopes of read-only transactions can overlap and execute at the same time. On the other hand, the scopes of writing transactions cannot overlap. You can still start several transactions with the same scope at the same time, but they just queue up and execute one after another.

## Next steps

With an understanding of IndexedDB's key characteristics and core terminology under our belts, we can get to more concrete stuff. For a tutorial on how to use the API, see [Using IndexedDB](/ko/docs/Web/API/IndexedDB_API/Using_IndexedDB).

## See also

- [Indexed Database API Specification](https://www.w3.org/TR/IndexedDB/)
- [IndexedDB API Reference](/ko/docs/Web/API/IndexedDB_API)
- [Using IndexedDB](/ko/docs/Web/API/IndexedDB_API/Using_IndexedDB)
- [IndexedDB — The Store in Your Browser](<https://docs.microsoft.com/previous-versions/msdn10/gg679063(v=msdn.10)>)

---
# Source: Web_API_WebSockets_API_Writing_WebSocket_servers.md
---
---
title: 웹소켓 서버 작성하기
slug: Web/API/WebSockets_API/Writing_WebSocket_servers
---

{{APIRef("Websockets API")}}

## 개요

웹 소켓 서버는 특정한 프로토콜을 따르는 서버의 임의 포트를 리스닝하고 있는 TCP 어플리케이션입니다. 사용자 서버를 만드는 작업은 두려운 일일수도 있습니다. 하지만, 당신이 선택한 플랫폼상에서 간단한 웹 소켓 서버를 구현하는것은 쉬울것입니다.

웹 소켓 서버는 C(++), Python, [PHP](/ko/docs/PHP), [server-side JavaScript](/ko/docs/Web/JavaScript/Server-Side_JavaScript)등과 같은 [Berkeley sockets](https://en.wikipedia.org/wiki/Berkeley_sockets)을 지원하는 어떠한 server-side 프로그래밍 언어로도 개발될 수 있습니다. 이것은 어느 특정한 언어의 자습서는 아니지만, 당신 자신의 서버를 개발하는것을 용이하게 하는 지침으로써의 역할을 합니다.

당신은 HTTP가 작동하는 방식과 중간정도의 개발 경험이 있어야만 합니다. 개발언어에서 제공하는 TCP 소켓에 대한 지식이 요구될 수도 있습니다. 이 지침의 범위는 당신이 웹 소켓서버를 개발하기위해 필요한 최소한의 지식에 대해 소개하는것입니다.

> **참고:** 최신의 공식 웹 소켓 문서인 [RFC 6455](http://datatracker.ietf.org/doc/rfc6455/?include_text=1)를 읽으세요. 1과 4-7 섹션이 특별히 서버개발자에게 흥미로운 부분입니다. 10 섹션에서는 보안에 대해 논의하며, 당신의 서버를 공개하기전 해당 부분을 반드시 정독하여 읽어보셔야만합니다.

이 페이지에서 웹 소켓 서버는 매우 약간만 설명되어 있습니다. 웹 소켓 서버는 종종 다른 특정한 이유로 인해 분리되거나 전문화됩니다. 따라서 웹 소켓과의 핸드 쉐이크를 감지하거나 미리 처리하거나 또는 클라이언트들을 실제 웹 소켓 서버에 보내기위해 일반적으로 HTTP 서버와 같은 [reverse proxy](https://en.wikipedia.org/wiki/Reverse_proxy)를 사용합니다. 이는 쿠키나 인증을 처리하기 위해 당신의 서버 코드를 잔뜩 작성하지 않아도 된다는 것을 의미합니다.

## <a name="Handshake">Step 1: The WebSocket Handshake</a>

먼저 서버는 표준 TCP 소켓을 사용하여 연결하려는 소켓을 위해 반드시 듣고 있어야 합니다. 당신의 플랫폼에 따라 서버는 이미 준비가 되어있을수도 있습니다. 예를들어, 당신의 서버가 example.com에 port가 8000인 채로 듣고 있다고 가정해봅시다.

> **경고:** 서버에서 아무 포트나 선택하여 연결할 수 있지만, 80 또는 443 포트가 아닌 다른 연결은 방화벽/프록시에 의해 문제를 일으킬 수 있습니다. TLS/SSL 보안 연결인 443 포트와의 연결이 가장 쉬울 것입니다. 현재 대부분의 브라우저(특히 Firefox 8+)는 안전한 페이지라 할지라도 보안 연결이 아닌 웹소켓 연결은 허용되지 않습니다.

웹소켓의 핸드셰이크 과정은 HTTP를 바탕으로 이루어집니다. 자세한 연결 과정은 다루지 않으나, 각 요청자는 연결 과정이 제대로 이루어질때까지 요청을 보류합니다. 서버는 클라이언트가 요청하는 모든 것을 주의깊게 이해해야 하고, 그렇지 않을 경우 보안 이슈가 일어날 수 있습니다.

### 클라이언트 핸드쉐이크 요청

당신이 웹 소켓 서버를 개발 중이라도, 클라이언트는 여전히 웹 소켓 핸드쉐이킹 과정을 시작합니다. 따라서, 당신은 클라이언트의 요청을 이해하기 위한 방법을 이해해야합니다. 클라이언트는 아래와 같아 보이는 매우 표준적인 HTTP 요청을 보낼것입니다.(HTTP 버전은 반드시 1.1. 혹은 그 이상이어하며, 반드시 GET방식이어야합니다.)

```
GET /chat HTTP/1.1
Host: example.com:8000
Upgrade: websocket
Connection: Upgrade
Sec-WebSocket-Key: dGhlIHNhbXBsZSBub25jZQ==
Sec-WebSocket-Version: 13
```

이외에도 클라이언트는 여러 메세지나 서브프로토콜을 추가해 보낼 수도 있습니다. `User-Agent`, `Referer`, `Cookie`와 같은 공통 헤더나, 인증 헤더도 말이죠. 자세한 [사항](#Miscellaneous)은 다음을 참조하세요. 원하는 대로 요청에 무엇이든지 첨부하여 보낼 수 있으며 웹소켓과 관련이 없을 경우 무시합니다. 통상적으로, 리버스 프록시가 이미 그런 기능을 담당하고 있을 겁니다.

잘못된 값을 가지거나 형식이 잘못된 헤더의 경우, 서버는 "[400 Bad Request](/ko/docs/HTTP/Response_codes#400)" 응답을 보내 즉시 소켓을 종료시켜야 합니다. HTTP 응답 바디에 핸드셰이크에 실패한 이유가 명시되어 있지만, 브라우저 상에서 명시적으로 나타내진 않습니다. 서버가 웹소켓의 버전 인식을 실패할 경우, 인식 가능한 버전을 명시해 `Sec-WebSocket-Version` 요청을 보내야 합니다. (최신 가이드 v13에서 설명되어 있습니다) 이제, 가장 흥미로운 헤더인 `Sec-WebSocket-Key`을 살펴봅니다.

> **참고:** **팁:** 모든 **브라우저는** [`Origin` header](/ko/docs/HTTP/Access_control_CORS#Origin)를 보냅니다. 이 헤더는 보안을 위해 활용되며, (checking for same origin, whitelisting/ blacklisting, etc.) 활용하고 싶지 않다면 [403 Forbidden](/ko/docs/HTTP/Response_codes#403)을 보냅니다. 하지만 non-browser 에이전트가 위조된 `Origin`을 보낼수도 있다는 것을 명심해야 합니다. 따라서 대부분의 애플리케이션은 이 헤더가 없는 요청을 거부합니다.

> **참고:** **Tip:** The request-uri (`/chat` here) has no defined meaning in the spec. So many people cleverly use it to let one server handle multiple WebSocket applications. For example, `example.com/chat` could invoke a multiuser chat app, while `/game` on the same server might invoke a multiplayer game.

> **참고:** [Regular HTTP status codes](/ko/docs/HTTP/Response_codes) can only be used before the handshake. After the handshake succeeds, you have to use a different set of codes (defined in section 7.4 of the spec).

### 서버가 보내는 핸드쉐이크 응답

위와 같은 요청을 받으면 서버 역시도 HTTP 구조의 응답을 보내주어야 합니다. 자세한 내용은 아래와 같습니다.(각각의 헤더 끝에는 \r\n을 그리고 가장 마지막에는 한번 더 \r\n을 넣는걸 잊지 마세요.)

```
HTTP/1.1 101 Switching Protocols
Upgrade: websocket
Connection: Upgrade
Sec-WebSocket-Accept: s3pPLMBiTxaQ9kYGzzhZRbK+xOo=
```

Additionally, the server can decide on extension/subprotocol requests here; see [Miscellaneous](#Miscellaneous) for details. The `Sec-WebSocket-Accept` part is interesting. The server must derive it from the `Sec-WebSocket-Key` that the client sent. To get it, concatenate the client's `Sec-WebSocket-Key` and "`258EAFA5-E914-47DA-95CA-C5AB0DC85B11`" together (it's a "[magic string](https://en.wikipedia.org/wiki/Magic_string)"), take the [SHA-1 hash](https://en.wikipedia.org/wiki/SHA-1) of the result, and return the [base64](https://en.wikipedia.org/wiki/Base64) encoding of the hash.

> **참고:** **FYI:** This seemingly overcomplicated process exists so that it's obvious to the client whether or not the server supports WebSockets. This is important because security issues might arise if the server accepts a WebSockets connection but interprets the data as a HTTP request.

So if the Key was "`dGhlIHNhbXBsZSBub25jZQ==`", the Accept will be "`s3pPLMBiTxaQ9kYGzzhZRbK+xOo=`". Once the server sends these headers, the handshake is complete and you can start swapping data!

> **참고:** The server can send other headers like Set-Cookie, or ask for authentication or redirects via other status codes, before sending the reply handshake.

### 클라이언트 추적

웹소켓 프로토콜과 직접적인 연관은 없지만, 이 항목에서 언급할만한 의미가 있습니다. 웹소켓 서버는 이미 연결된 클라이언트들의 반복적인 연결(hand shaking)을 막기위해 클라이언트의 소켓 상태를 추적해야합니다. 같은 IP 주소를 가지는 클라이언트는 여러번 연결을 시도 할 수 있습니다.(하지만, 서버는 [Denial-of-Service attacks](https://en.wikipedia.org/wiki/Denial_of_service) 을 위해 너무 많은 연결 요청을 거부할 수 있습니다).

## Step 2: 데이터 프레임 교환

Either the client or the server can choose to send a message at any time — that's the magic of WebSockets. However, extracting information from these so-called "frames" of data is a not-so-magical experience. Although all frames follow the same specific format, data going from the client to the server is masked using [XOR encryption](https://en.wikipedia.org/wiki/XOR_cipher) (with a 32-bit key). Section 5 of the specification describes this in detail.

### 데이터 프레임 포멧

모든 데이터 프레임 (서버->클라이언트 / 클라이언트 -> 서버) 은 아래의 구조를 따릅니다:

<pre style="float: left; margin-right: 20px;"> <strong>0</strong>               <strong>1</strong>               <strong>2</strong>               3
 0 1 2 3 4 5 6 7 0 1 2 3 4 5 6 7 0 1 2 3 4 5 6 7 0 1 2 3 4 5 6 7
+-+-+-+-+-------+-+-------------+-------------------------------+
|F|R|R|R| opcode|M| Payload len |    Extended payload length    |
|I|S|S|S| (4)   |A|     (7)     |             (16/64)           |
|N|V|V|V|       |S|             |   (if payload len==126/127)   |
| |1|2|3|       |K|             |                               |
+-+-+-+-+-------+-+-------------+ - - - - - - - - - - - - - - - +
 4               5               6               7
+ - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - +
|     Extended payload length continued, if payload len == 127  |
+ - - - - - - - - - - - - - - - +-------------------------------+
 8               9               <strong>10</strong>              11
+ - - - - - - - - - - - - - - - +-------------------------------+
|                               |Masking-key, if MASK set to 1  |
+-------------------------------+-------------------------------+
 12              13              <strong>14</strong>              15
+-------------------------------+-------------------------------+
| Masking-key (continued)       |          Payload Data         |
+-------------------------------- - - - - - - - - - - - - - - - +
:                     Payload Data continued ...                :
+ - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - - +
|                     Payload Data continued ...                |
+---------------------------------------------------------------+</pre>

RSV1-3 는 사용되지 않습니다. 이 필드들은 확장 프로토콜 또는 미래를 위해 예약되었습니다.

MASK 비트는 메세지가 인코딩되어있는지의 여부를 나타냅니다.클라이언트가 서버로 보내는 메세지는 항상 마스킹되어야합니다. 따라서 서버는 클라이언트로부터 받은 이 필드가 항상 1임을 기대할 수 있습니다. (만약 클라이언트가 마스킹되지 않은 메세지를 보낸다면 서버는 연결을 종료해야 합니다. 참고 : [section 5.1 of the spec](http://tools.ietf.org/html/rfc6455#section-5.1) ).
서버가 클라이언트에게 보내는 메세지는 MASK 필드가 항상 0이고 데이터는 마스킹되지 않은 상태여야 합니다. 마스킹이 어떻게 이루어지는지 / 마스킹된 메세지를 어떻게 디코딩하는지는 나중에 설명합니다.
(주의: wss 연결이라고 하더라도 클라이언트가 보내는 패킷은 항상 마스킹되어야 합니다.)

opcode 필드는 뒤따라오는 payload 데이터가 어떠한 포멧인지를 나타냅니다. 0x0은 continuation, 0x1은 텍스트(항상 UTF-8), 0x2는 바이너리 데이터 / 나머지 값은 "컨트롤 코드"에 사용됩니다. (컨트롤 코드에 대해서는 나중에 다루게 됩니다.) 현재 버전의 웹소켓 프로토콜에서는 0x3 / 0x7 / 0xB\~0xF는 아무런 의미도 지니고있지 않습니다.

FIN 비트는 이 메세지가 마지막임을 나타냅니다. 만약 FIN 비트가 0이라면 서버는 뒤에 더 따라오게 될 메세지들까지 수신해야 합니다. FIN 비트가 1일 경우에는 전체 메세지가 수신되었으므로 이를 처리합니다. 이 부분에 대해서는 뒤에 다시 설명합니다.

### Payload 길이 알아내기

수신한 프레임으로부터 payload 데이터를 읽기 위해서는 payload length 필드를 읽어야 합니다. 불행히도 이는 약간 복잡한 작업을 거치는데 아래 순서대로 처리해 주세요.

1. 9번째부터 15번째까지의 비트를 읽습니다. 이를 unsigned integer로 취급한 다음 값이 125거나 이보다 작을 경우 이 자체가 payload length 입니다. 이 경우에는 2, 3 과정은 필요 없습니다. 하지만 126이면 2번으로, 127일 경우 3번으로 가주세요
2. 다음 16비트를 읽습니다. 이를 unsigned integer로 처리하고 payload length 값으로 사용합니다.
3. 다음 64비트를 읽습니다. 이를 unsigned integer로 처리하고 payload length 값으로 사용합니다. ([최상위 비트](https://ko.wikipedia.org/wiki/%EC%B5%9C%EC%83%81%EC%9C%84_%EB%B9%84%ED%8A%B8)는 항상 0이어야 합니다.)

### 마스킹된 Payload 데이터 디코딩하기

MASK 비트가 설정되어 있디만 32비트 사이즈의 Masking-Key 필드 또한 존재하게 됩니다.
아래 의사코드는 Payload 데이터를 **ENCODED** / Masking-Key 필드를 **MASK** 라고 가정하고 데이터를 디코딩하는 방법을 보여줍니다. **ENCODED**값을 0부터 순회하면서 **MASK**의 i % 4에 해당하는 1바이트와 XOR 연산을 수행합니다.

If the MASK bit was set (and it should be, for client-to-server messages), read the next 4 octets (32 bits); this is the masking key. Once the payload length and masking key is decoded, you can go ahead and read that number of bytes from the socket. Let's call the data **ENCODED**, and the key **MASK**. To get **DECODED**, loop through the octets (bytes a.k.a. characters for text data) of **ENCODED** and XOR the octet with the (i modulo 4)th octet of MASK. In pseudo-code (that happens to be valid JavaScript):

```js
var DECODED = "";
for (var i = 0; i < ENCODED.length; i++) {
  DECODED[i] = ENCODED[i] ^ MASK[i % 4];
}
```

이제 **DECODED** 데이터를 가지고 프로토콜에 맞게 활용하면 됩니다.

### Message Fragmentation

The FIN and opcode fields work together to send a message split up into separate frames. This is called message fragmentation. Fragmentation is only available on opcodes `0x0` to `0x2`.

Recall that the opcode tells what a frame is meant to do. If it's `0x1`, the payload is text. If it's `0x2`, the payload is binary data. However, if it's `0x0,` the frame is a continuation frame. This means the server should concatenate the frame's payload to the last frame it received from that client. Here is a rough sketch, in which a server reacts to a client sending text messages. The first message is sent in a single frame, while the second message is sent across three frames. FIN and opcode details are shown only for the client:

<pre style="font-size: 14px;"><strong>Client:</strong> FIN=1, opcode=0x1, msg="hello"
<strong>Server:</strong> <em>(process complete message immediately) </em>Hi.
<strong>Client:</strong> FIN=0, opcode=0x1, msg="and a"
<strong>Server:</strong> <em>(listening, new message containing text started)</em>
<strong>Client:</strong> FIN=0, opcode=0x0, msg="happy new"
<strong>Server:</strong> <em>(listening, payload concatenated to previous message)</em>
<strong>Client:</strong> FIN=1, opcode=0x0, msg="year!"
<strong>Server:</strong> <em>(process complete message) </em>Happy new year to you too!</pre>

Notice the first frame contains an entire message (has `FIN=1` and `opcode!=0x0`), so the server can process or respond as it sees fit. The second frame sent by the client has a text payload (`opcode=0x1`), but the entire message has not arrived yet (`FIN=0`). All remaining parts of that message are sent with continuation frames (`opcode=0x0`), and the final frame of the message is marked by `FIN=1`. [Section 5.4 of the spec](http://tools.ietf.org/html/rfc6455#section-5.4) describes message fragmentation.

## Pings and Pongs: The Heartbeat of WebSockets

핸드쉐이크가 끝난 시점부터 서버 혹은 클라이언트는 언제든지 ping 패킷을 보낼 수 있습니다. 만약 ping 패킷이 수신되면 수신자는 가능한 빨리 응답으로 pong 패킷을 보내야 합니다. (ping에서 전달된 payload와 동일한 payload를 붙여서 pong을 보냅니다. 이 경우 최대 payload length는 125입니다.) 서버는 주기적으로 ping을 보내 클라이언트가 아직 살아있는 상태인지 체크할 수 있습니다.

A ping or pong is just a regular frame, but it's a **control frame**. Pings have an opcode of `0x9`, and pongs have an opcode of `0xA`. When you get a ping, send back a pong with the exact same Payload Data as the ping (for pings and pongs, the max payload length is 125). You might also get a pong without ever sending a ping; ignore this if it happens.

> **참고:** If you have gotten more than one ping before you get the chance to send a pong, you only send one pong.

## Step 4: Closing the connection

To close a connection either the client or server can send a control frame with data containing a specified control sequence to begin the closing handshake (detailed in [Section 5.5.1](http://tools.ietf.org/html/rfc6455#section-5.5.1)). Upon receiving such a frame, the other peer sends a Close frame in response. The first peer then closes the connection. Any further data received after closing of connection is then discarded.

## <a name="Miscellaneous">Miscellaneous</a>

> **참고:** WebSocket codes, extensions, subprotocols, etc. are registered at the [IANA WebSocket Protocol Registry](http://www.iana.org/assignments/websocket/websocket.xml).

WebSocket extensions and subprotocols are negotiated via headers during [the handshake](#Handshake). Sometimes extensions and subprotocols seem too similar to be different things, but there is a clear distinction. Extensions control the WebSocket **frame** and **modify** the payload, while subprotocols structure the WebSocket **payload** and **never modify** anything. Extensions are optional and generalized (like compression); subprotocols are mandatory and localized (like ones for chat and for MMORPG games).

### Extensions

> **참고:** **This section needs expansion. Please edit if you are equipped to do so.**

Think of an extension as compressing a file before e-mailing it to someone. Whatever you do, you're sending the _same_ data in different forms. The recipient will eventually be able to get the same data as your local copy, but it is sent differently. That's what an extension does. WebSockets defines a protocol and a simple way to send data, but an extension such as compression could allow sending the same data but in a shorter format.

> **참고:** Extensions are explained in sections 5.8, 9, 11.3.2, and 11.4 of the spec.

### 서브프로토콜

Think of a subprotocol as a custom [XML schema](https://en.wikipedia.org/wiki/XML_schema) or [doctype declaration](https://en.wikipedia.org/wiki/Document_Type_Definition). You're still using XML and its syntax, but you're additionally restricted by a structure you agreed on. WebSocket subprotocols are just like that. They do not introduce anything fancy, they just establish structure. Like a doctype or schema, both parties must agree on the subprotocol; unlike a doctype or schema, the subprotocol is implemented on the server and cannot be externally refered to by the client.

> **참고:** Subprotocols are explained in sections 1.9, 4.2, 11.3.4, and 11.5 of the spec.

클라이언트는 핸드쉐이크 요청 시에 특정한 서브프로콜의 목록을 같이 보낼 수 있습니다. **Sec-WebSocket-Protocol** 헤더에 사용하기를 원하는 서브프로토콜의 목록을 같이 보냅니다.

```
GET /chat HTTP/1.1
...
Sec-WebSocket-Protocol: soap, wamp
```

또는 아래와 같이 보낼 수도 있습니다.:

```
...
Sec-WebSocket-Protocol: soap
Sec-WebSocket-Protocol: wamp
```

클라이언트로부터 서브프로토콜 요청을 받으면, 서버는 그 중에서 자신이 지원할 수 있는 서브프로토콜을 **하나** 골라야 합니다. 만약 클라이언트가 보낸 목록 중, 여러개를 지원할 수 있다면 지원하는 목록 중 가장 첫번째 서브프로토콜을 보내주세요.

Imagine our server can use both `soap` and `wamp`. Then, in the response handshake, it'll send:

```
Sec-WebSocket-Protocol: soap
```

> **경고:** `서버는 반드시 하나의 Sec-Websocket-Protocol 헤더만을 송신해야 합니다.` > `만약 서버가 어떠한 서브프로토콜도 지원하고 싶지 않다면 Sec-Websocket-Protocol 헤더를 빼고 보내주세요. 빈 값을 넣어서 보내도 안됩니다.`
> 서버가 아무 서브프로토콜을 지원하지 않겠다고 한다면 클라이언트는 연결을 닫아버릴수도 있습니다.

If you want your server to obey certain subprotocols, then naturally you'll need extra code on the server. Let's imagine we're using a subprotocol `json`. In this subprotocol, all data is passed as [JSON](https://en.wikipedia.org/wiki/JSON). If the client solicits this protocol and the server wants to use it, the server will need to have a JSON parser. Practically speaking, this will be part of a library, but the server will need to pass the data around.

> **참고:** **Tip:** To avoid name conflict, it's recommended to make your subprotocol name part of a domain string. If you are building a custom chat app that uses a proprietary format exclusive to Example Inc., then you might use this: `Sec-WebSocket-Protocol: chat.example.com`. For different versions, a widely-used method is to add a `/` followed by the version number, like `chat.example.com/2.0`. Note that this isn't required, it's just an optional convention, and you can use any string you wish.

## 같이 보기

- [Tutorial: Websocket server in C#](/ko/docs/WebSockets/Writing_WebSocket_server)
- [Writing WebSocket client applications](/ko/docs/WebSockets/Writing_WebSocket_client_applications)
- [Tutorial: Websocket server in VB.NET](/ko/docs/WebSockets/WebSocket_Server_Vb.NET)

---
# Source: Web_HTML_Element_audio.md
---
---
title: <audio>
slug: Web/HTML/Element/audio
---

{{HTMLSidebar}}

**HTML `<audio>` 요소**는 문서에 소리 콘텐츠를 포함할 때 사용합니다. `src` 특성 또는 {{htmlelement("source")}} 요소를 사용해 한 개 이상의 오디오 소스를 지정할 수 있으며, 다수를 지정한 경우 가장 적절한 소스를 브라우저가 고릅니다. {{domxref("MediaStream")}}을 사용하면 미디어 스트림을 바라볼 수도 있습니다.

{{InteractiveExample("HTML Demo: &lt;audio&gt;", "tabbed-standard")}}

```html interactive-example
<figure>
  <figcaption>Listen to the T-Rex:</figcaption>
  <audio controls src="/shared-assets/audio/t-rex-roar.mp3"></audio>
  <a href="/shared-assets/audio/t-rex-roar.mp3"> Download audio </a>
</figure>
```

```css interactive-example
figure {
  margin: 0;
}
```

## 특성

이 요소는 [전역 특성](/ko/docs/Web/HTML/Global_attributes)을 포함합니다.

- `autoplay`
  - : 지정한 경우, 전체 오디오 파일의 다운로드를 기다리지 않고 가능한 빠른 시점에 재생을 시작합니다.

    > **참고:** 오디오 및 오디오를 가진 비디오를 자동으로 재생하는 사이트는 사용자 경험에 악영향을 끼칠 수 있으므로 피해야 합니다. 반드시 자동 재생을 제공해야 한다면 사용자의 명시적인 동의를 얻어야 하도록 해야 합니다. 그러나, 미디어 소스가 사용자의 선택에 의해 나중에 정해지는 경우라면 자동 재생이 유용할 수 있습니다. [자동 재생 안내서](/ko/docs/Web/Media/Autoplay_guide)를 방문하고 추가 정보와 적절한 사용법을 알아보세요.

- `controls`
  - : 지정한 경우 오디오 재생, 볼륨, 탐색, 일시 정지 컨트롤을 브라우저에서 제공합니다.
- `crossorigin`
  - : CORS를 사용해 지정한 오디오 파일을 가져올지 나타내는 열거형 특성. [교차 출처 활성화 리소스](/ko/docs/Web/HTML/CORS_enabled_image)는 {{HTMLElement("canvas")}} 요소에 사용해도 캔버스를 "오염"시키지 않습니다. 가능한 값은 다음과 같습니다.
    - `anonymous`
      - : 자격 증명 없이 교차 출처 요청을 전송합니다. 즉, `Origin:` HTTP 헤더를 쿠키, X.509 인증서, HTTP Basic 인증 없이 전송합니다. 서버에서 `Access-Control-Allow-Origin:` HTTP 헤더를 지정하지 않음으로써 요청 출처 사이트에 자격 증명을 보내지 않는다면 이미지는 "오염"되고, 사용처가 제한됩니다.
    - `use-credentials`
      - : 자격 증명과 함께 교차 출처 요청을 전송합니다. 즉, `Origin:` HTTP 헤더를 쿠키, X 509 인증서, 또는 HTTP Basic 이증과 함께 전송합니다. 서버에서 `Access-Control-Allow-Origin:` HTTP 헤더를 통한 자격 증명을 요청 출처 사이트에 보내지 않는다면 이미지는 "오염"되고, 사용처가 제한됩니다.

    특성이 존재하지 않으면 리소스를 CORS 요청 없이(`Origin:` HTTP 헤더 없이) 가져오므로, {{htmlelement("canvas")}}를 오염시키게 됩니다. 유효하지 않은 값의 경우 anonymous 키워드를 사용한 것으로 간주합니다.

- `currentTime`
  - : Reading `currentTime` returns a double-precision floating-point value indicating the current playback position, in seconds, of the audio. If the audio's metadata isn't available yet—thereby preventing you from knowing the media's start time or duration—`currentTime` instead indicates, and can be used to change, the time at which playback will begin. Otherwise, setting `currentTime` sets the current playback position to the given time and seeks the media to that position if the media is currently loaded.

    If the audio is being streamed, it's possible that the {{Glossary("user agent")}} may not be able to obtain some parts of the resource if that data has expired from the media buffer. Other audio may have a media timeline that doesn't start at 0 seconds, so setting `currentTime` to a time before that would fail. For example, if the audio's media timeline starts at 12 hours, setting `currentTime` to 3600 would be an attempt to set the current playback position well before the beginning of the media, and would fail. The {{domxref("HTMLMediaElement.getStartDate", "getStartDate()")}} method can be used to determine the beginning point of the media timeline's reference frame.

- `disableRemotePlayback` {{experimental_inline}}
  - : A Boolean attribute used to disable the capability of remote playback in devices that are attached using wired (HDMI, DVI, etc.) and wireless technologies (Miracast, Chromecast, DLNA, AirPlay, etc). See [this proposed specification](https://www.w3.org/TR/remote-playback/#the-disableremoteplayback-attribute) for more information.

    > **참고:** In Safari, you can use [`x-webkit-airplay="deny"`](https://developer.apple.com/library/archive/documentation/AudioVideo/Conceptual/AirPlayGuide/OptingInorOutofAirPlay/OptingInorOutofAirPlay.html) as a fallback.

- `duration` {{ReadOnlyInline}}
  - : A double-precision floating-point value which indicates the duration (total length) of the audio in seconds, on the media's timeline. If no media is present on the element, or the media is not valid, the returned value is `NaN`. If the media has no known end (such as for live streams of unknown duration, web radio, media incoming from [WebRTC](/ko/docs/Web/API/WebRTC_API), and so forth), this value is `+Infinity`.
- `loop`
  - : A Boolean attribute: if specified, the audio player will automatically seek back to the start upon reaching the end of the audio.
- `muted`
  - : A Boolean attribute that indicates whether the audio will be initially silenced. Its default value is `false`.
- `preload`
  - : This enumerated attribute is intended to provide a hint to the browser about what the author thinks will lead to the best user experience. It may have one of the following values:
    - `none`: Indicates that the audio should not be preloaded.
    - `metadata`: Indicates that only audio metadata (e.g. length) is fetched.
    - `auto`: Indicates that the whole audio file can be downloaded, even if the user is not expected to use it.
    - _empty string_: A synonym of the `auto` value.

    The default value is different for each browser. The spec advises it to be set to `metadata`.

    > **참고:** **Usage notes:**- The `autoplay` attribute has precedence over `preload`. If `autoplay` is specified, the browser would obviously need to start downloading the audio for playback.
    >
    > - The browser is not forced by the specification to follow the value of this attribute; it is a mere hint.

- `src`
  - : The URL of the audio to embed. This is subject to [HTTP access controls](/ko/docs/HTTP_access_control). This is optional; you may instead use the {{htmlelement("source")}} element within the audio block to specify the audio to embed.

Time offsets are specified as float values indicating the number of seconds to offset.

> **참고:** The time offset value definition has not yet been completed in the HTML5 specification and is subject to change.

## 이벤트

| 이벤트 이름                                                            | 발생 조건                                                                                                                                                                                                                            |
| ---------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| {{Event("audioprocess")}}                                              | The input buffer of a {{DOMxRef("ScriptProcessorNode")}} is ready to be processed.                                                                                                                                                   |
| {{domxref("HTMLMediaElement.canplay_event", 'canplay')}}               | The browser can play the media, but estimates that not enough data has been loaded to play the media up to its end without having to stop for further buffering of content.                                                          |
| {{domxref("HTMLMediaElement.canplaythrough_event", 'canplaythrough')}} | The browser estimates it can play the media up to its end without stopping for content buffering.                                                                                                                                    |
| {{Event("complete")}}                                                  | The rendering of an {{DOMxRef("OfflineAudioContext")}} is terminated.                                                                                                                                                                |
| {{domxref("HTMLMediaElement.durationchange_event", 'durationchange')}} | The `duration` attribute has been updated.                                                                                                                                                                                           |
| {{domxref("HTMLMediaElement.emptied_event", 'emptied')}}               | The media has become empty; for example, this event is sent if the media has already been loaded (or partially loaded), and the [`load()`](/ko/docs/XPCOM_Interface_Reference/NsIDOMHTMLMediaElement) method is called to reload it. |
| {{domxref("HTMLMediaElement.ended_event", 'ended')}}                   | Playback has stopped because the end of the media was reached.                                                                                                                                                                       |
| {{domxref("HTMLMediaElement.loadeddata_event", 'loadeddata')}}         | The first frame of the media has finished loading.                                                                                                                                                                                   |
| {{domxref("HTMLMediaElement.loadedmetadata_event", 'loadedmetadata')}} | The metadata has been loaded.                                                                                                                                                                                                        |
| {{domxref("HTMLMediaElement.pause_event", 'pause')}}                   | Playback has been paused.                                                                                                                                                                                                            |
| {{domxref("HTMLMediaElement.play_event", 'play')}}                     | Playback has begun.                                                                                                                                                                                                                  |
| {{domxref("HTMLMediaElement.playing_event", 'playing ')}}              | Playback is ready to start after having been paused or delayed due to lack of data.                                                                                                                                                  |
| {{domxref("HTMLMediaElement.ratechange_event", 'ratechange')}}         | The playback rate has changed.                                                                                                                                                                                                       |
| {{domxref("HTMLMediaElement.seeked_event", 'seeked')}}                 | A _seek_ operation completed.                                                                                                                                                                                                        |
| {{domxref("HTMLMediaElement.seeking_event", 'seeking')}}               | A _seek_ operation began.                                                                                                                                                                                                            |
| {{domxref("HTMLMediaElement.stalled_event", 'stalled')}}               | The user agent is trying to fetch media data, but data is unexpectedly not forthcoming.                                                                                                                                              |
| {{domxref("HTMLMediaElement.suspend_event", 'suspend')}}               | Media data loading has been suspended.                                                                                                                                                                                               |
| {{domxref("HTMLMediaElement.timeupdate_event", 'timeupdate')}}         | The time indicated by the `currentTime` attribute has been updated.                                                                                                                                                                  |
| {{domxref("HTMLMediaElement.volumechange_event", 'volumechange')}}     | The volume has changed.                                                                                                                                                                                                              |
| {{domxref("HTMLMediaElement.waiting_event", 'waiting')}}               | Playback has stopped because of a temporary lack of data                                                                                                                                                                             |

## 사용 일람

Browsers don't all support the same [file types](/ko/docs/Web/Media/Formats/Containers) and [audio codecs](/ko/docs/Web/Media/Formats/Audio_codecs); you can provide multiple sources inside nested {{htmlelement("source")}} elements, and the browser will then use the first one it understands:

```html
<audio controls>
  <source src="myAudio.mp3" type="audio/mpeg" />
  <source src="myAudio.ogg" type="audio/ogg" />
  <p>
    Your browser doesn't support HTML5 audio. Here is a
    <a href="myAudio.mp4">link to the audio</a> instead.
  </p>
</audio>
```

We offer a substantive and thorough [guide to media file types](/ko/docs/Web/Media/Formats) and the [audio codecs that can be used within them](/ko/docs/Web/Media/Formats/Audio_codecs). Also available is [a guide to the codecs supported for video](/ko/docs/Web/Media/Formats/Video_codecs).

Other usage notes:

- If you don't specify the `controls` attribute, the audio player won't include the browser's default controls. You can, however, create your own custom controls using JavaScript and the {{domxref("HTMLMediaElement")}} API.
- To allow precise control over your audio content, `HTMLMediaElement`s fire many different [events](/ko/docs/Web/Guide/Events/Media_events). This also provides a way to monitor the audio's fetching process so you can watch for errors or detect when enough is available to begin to play or manipulate it.
- You can also use the [Web Audio API](/ko/docs/Web/API/Web_Audio_API) to directly generate and manipulate audio streams from JavaScript code rather than streaming pre-existing audio files.
- `<audio>` elements can't have subtitles or captions associated with them in the same way that `<video>` elements can. See [WebVTT and Audio](https://www.iandevlin.com/blog/2015/12/html5/webvtt-and-audio) by Ian Devlin for some useful information and workarounds.

A good general source of information on using HTML `<audio>` is the [Video and audio content](/ko/docs/Learn/HTML/Multimedia_and_embedding/Video_and_audio_content) beginner's tutorial.

### Styling with CSS

The `<audio>` element has no intrinsic visual output of its own unless the `controls` attribute is specified, in which case the browser's default controls are shown.

The default controls have a {{cssxref("display")}} value of `inline` by default, and it is often a good idea set the value to `block` to improve control over positioning and layout, unless you want it to sit within a text block or similar.

You can style the default controls with properties that affect the block as a single unit, so for example you can give it a {{cssxref("border")}} and {{cssxref("border-radius")}}, {{cssxref("padding")}}, {{cssxref("margin")}}, etc. You can't however style the individual components inside the audio player (e.g. change the button size or icons, change the font, etc.), and the controls are different across the different browsers.

To get a consistent look and feel across browsers, you'll need to create custom controls; these can be marked up and styled in whatever way you want, and then JavaScript can be used along with the {{domxref("HTMLMediaElement")}} API to wire up their functionality.

[Video player styling basics](/ko/docs/Web/Apps/Fundamentals/Audio_and_video_delivery/Video_player_styling_basics) provides some useful styling techniques — it is written in the context of `<video>`, but much of it is equally applicable to `<audio>`.

### Detecting addition and removal of tracks

You can detect when tracks are added to and removed from an `<audio>` element using the {{event("addtrack")}} and {{event("removetrack")}} events. However, these events aren't sent directly to the `<audio>` element itself. Instead, they're sent to the track list object within the `<audio>` element's {{domxref("HTMLMediaElement")}} that corresponds to the type of track that was added to the element:

- {{domxref("HTMLMediaElement.audioTracks")}}
  - : An {{domxref("AudioTrackList")}} containing all of the media element's audio tracks. You can add a listener for `addtrack` to this object to be alerted when new audio tracks are added to the element.
- {{domxref("HTMLMediaElement.videoTracks")}}
  - : Add an `addtrack` listener to this {{domxref("VideoTrackList")}} object to be informed when video tracks are added to the element.
- {{domxref("HTMLMediaElement.textTracks")}}
  - : Add an `addtrack` event listener to this {{domxref("TextTrackList")}} to be notified when new text tracks are added to the element.

> **참고:** Even though it's an `<audio>` element, it still has video and text track lists, and can in fact be used to present video, although the use interface implications can be odd.

For example, to detect when audio tracks are added to or removed from an `<audio>` element, you can use code like this:

```js
var elem = document.querySelector("audio");

elem.audioTrackList.onaddtrack = function (event) {
  trackEditor.addTrack(event.track);
};

elem.audioTrackList.onremovetrack = function (event) {
  trackEditor.removeTrack(event.track);
};
```

This code watches for audio tracks to be added to and removed from the element, and calls a hypothetical function on a track editor to register and remove the track from the editor's list of available tracks.

You can also use {{domxref("EventTarget.addEventListener", "addEventListener()")}} to listen for the {{event("addtrack")}} and {{event("removetrack")}} events.

## 예제

### Basic usage

The following example shows simple usage of the `<audio>` element to play an OGG file. It will autoplay due to the `autoplay` attribute—if the page has permission to do so—and also includes fallback content.

```html
<!-- Simple audio playback -->
<audio src="AudioTest.ogg" autoplay>
  Your browser does not support the <code>audio</code> element.
</audio>
```

For details on when autoplay works, how to get permission to use autoplay, and how and when it's appropriate to use autoplay, see our [autoplay guide](/ko/docs/Web/Media/Autoplay_guide).

### \<audio> element with \<source> element

This example specifies which audio track to embed using the `src` attribute on a nested `<source>` element rather than directly on the `<audio>` element. It is always useful to include the file's MIME type inside the `type` attribute, as the browser is able to instantly tell if it can play that file, and not waste time on it if not.

```html
<audio controls>
  <source src="foo.wav" type="audio/wav" />
  Your browser does not support the <code>audio</code> element.
</audio>
```

### \<audio> with multiple \<source> elements

This example includes multiple `<source>` elements. The browser tries to load the first source element (Opus) if it is able to play it; if not it falls back to the second (Vorbis) and finally back to MP3:

```html
<audio controls>
  <source src="foo.opus" type="audio/ogg; codecs=opus" />
  <source src="foo.ogg" type="audio/ogg; codecs=vorbis" />
  <source src="foo.mp3" type="audio/mpeg" />
</audio>
```

## 접근성 고려사항

Audio with spoken dialog should provide both captions and transcripts that accurately describe its content. Captions, which are specified using [WebVTT](/ko/docs/Web/API/WebVTT_API), allow people who are experiencing hearing loss to understand an audio recording's content as the recording is being played, while transcripts allow people who need additional time to be able to review the recording's content at a pace and format that is comfortable for them.

If automatic captioning services are used, it is important to review the generated content to ensure it accurately represents the source audio.

The `<audio>` element doesn't directly support WebVTT. You will have to find a library or framework that provides the capability for you, or write the code to display captions yourself. One option is to play your audio using a {{HTMLElement("video")}} element, which does support WebVTT.

In addition to spoken dialog, subtitles and transcripts should also identify music and sound effects that communicate important information. This includes emotion and tone. For example, in the WebVTT below, note the use of square brackets to provide tone and emotional insight to the viewer; this can help establish the mood otherwise provided using music, nonverbal sounds and crucial sound effects, and so forth.

```
1
00:00:00 --> 00:00:45
[Energetic techno music]

2
00:00:46 --> 00:00:51
Welcome to the Time Keeper's podcast! In this episode we're discussing which Swisswatch is a wrist switchwatch?

16
00:00:52 --> 00:01:02
[Laughing] Sorry! I mean, which wristwatch is a Swiss wristwatch?
```

Also it's a good practice to provide some content (such as the direct download link) as a fallback for viewers who use a browser in which the `<audio>` element is not supported:

```html
<audio controls>
  <source src="myAudio.mp3" type="audio/mpeg" />
  <source src="myAudio.ogg" type="audio/ogg" />
  <p>
    Your browser doesn't support HTML5 audio. Here is a
    <a href="myAudio.mp4">link to download the audio</a> instead.
  </p>
</audio>
```

- [MDN Subtitles and closed caption — Plugins](/ko/docs/Plugins/Flash_to_HTML5/Video/Subtitles_captions)
- [Web Video Text Tracks Format (WebVTT)](/ko/docs/Web/API/WebVTT_API)
- [WebAIM: Captions, Transcripts, and Audio Descriptions](https://webaim.org/techniques/captions/)
- [MDN Understanding WCAG, Guideline 1.2 explanations](/ko/docs/Web/Accessibility/Understanding_WCAG/Perceivable#Guideline_1.2_—_Providing_text_alternatives_for_time-based_media)
- [Understanding Success Criterion 1.2.1 | W3C Understanding WCAG 2.0](https://www.w3.org/TR/UNDERSTANDING-WCAG20/media-equiv-av-only-alt.html)
- [Understanding Success Criterion 1.2.2 | W3C Understanding WCAG 2.0](https://www.w3.org/TR/UNDERSTANDING-WCAG20/media-equiv-captions.html)

## 기술 요약

<table class="properties">
  <tbody>
    <tr>
      <th scope="row">
        <a href="/ko/docs/Web/Guide/HTML/Content_categories">콘텐츠 카테고리</a>
      </th>
      <td>
        <a href="/ko/docs/Web/Guide/HTML/Content_categories#플로우_콘텐츠"
          >플로우 콘텐츠</a
        >,
        <a href="/ko/docs/Web/Guide/HTML/Content_categories#구문_콘텐츠"
          >구문 콘텐츠</a
        >,
        <a href="/ko/docs/Web/Guide/HTML/Content_categories#내장_콘텐츠"
          >내장 콘텐츠</a
        >. <a href="/ko/docs/Web/HTML/Element/audio#controls"><code>controls</code></a> 특성을 가진 경우,
        <a href="/ko/docs/Web/Guide/HTML/Content_categories#대화형_콘텐츠"
          >대화형 콘텐츠</a
        >
        및 뚜렷한 콘텐츠.
      </td>
    </tr>
    <tr>
      <th scope="row">가능한 콘텐츠</th>
      <td>
        <p>
          <a href="/ko/docs/Web/HTML/Element/audio#src"><code>src</code></a> 특성을 가진 경우 0개
          이상의 {{htmlelement("track")}} 요소와 그 이후의 투명한
          콘텐츠. 단, 다른 {{htmlelement("audio")}}와
          {{htmlelement("video")}} 요소는 불가능.
        </p>
        <p>
          그 외의 경우 0개 이상의 {{HTMLElement("source")}} 요소와 0개
          이상의 {{HTMLElement("track")}} 요소, 그리고 이후의 투명한
          콘텐츠. 단, 다른 {{htmlelement("audio")}}와
          {{htmlelement("video")}} 요소는 불가능.
        </p>
      </td>
    </tr>
    <tr>
      <th scope="row">태그 생략</th>
      <td>{{no_tag_omission}}</td>
    </tr>
    <tr>
      <th scope="row">가능한 부모 요소</th>
      <td>
        <a href="/ko/docs/Web/Guide/HTML/Content_categories#내장_콘텐츠"
          >내장 콘텐츠</a
        >를 허용하는 모든 요소.
      </td>
    </tr>
    <tr>
      <th scope="row">암시적 ARIA 역할</th>
      <td>
        <a href="https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role"
          >대응하는 역할 없음</a
        >
      </td>
    </tr>
    <tr>
      <th scope="row">가능한 ARIA 역할</th>
      <td><a href='/ko/docs/Web/Accessibility/ARIA/Roles/application_role'><code>application</code></a></td>
    </tr>
    <tr>
      <th scope="row">DOM 인터페이스</th>
      <td>{{domxref("HTMLAudioElement")}}</td>
    </tr>
  </tbody>
</table>

## 명세

{{Specifications}}

## 브라우저 호환성

{{Compat}}

## 같이 보기

- [Web media technologies](/ko/docs/Web/Media)
  - [Media container formats (file types)](/ko/docs/Web/Media/Formats/Containers)
  - [Guide to audio codecs used on the web](/ko/docs/Web/Media/Formats/Audio_codecs)

- [Web Audio API](/ko/docs/Web_Audio_API)
- {{domxref("HTMLAudioElement")}}
- {{htmlelement("source")}}
- {{htmlelement("video")}}
- [Learning area: Video and audio content](/ko/docs/Learn/HTML/Multimedia_and_embedding/Video_and_audio_content)
- [Cross-browser audio basics](/en-US/Apps/Fundamentals/Audio_and_video_delivery/Cross-browser_audio_basics)

---
# Source: Web_API_Window_window.md
---
---
title: Window.window
slug: Web/API/Window/window
---

{{APIRef}}

## 요약

window 객체의 window 프로퍼티는 자기 자신의 window 객체를 가리킨다. 즉, 아래의 표현들은 같은 window 객체를 반환하게 된다:

```js
window.window
window.window.window
window.window.window.window
...
```

웹페이지에서 window 객체는 전역 객체이기도 하다. 다시 말해서:

1. 스크립트의 전역 변수는 사실 window 객체의 프로퍼티이다.

   ```js
   var global = { data: 0 };
   alert(global === window.global); // true를 반환한다.
   ```

2. window 객체의 내장된 프로퍼티들은 window. 접두사 없이도 참조가 가능하다.

   ```js
   setTimeout("alert('Hi!')", 50); // window.setTimeout. 을 사용한 것과 동일하다.
   alert(window === window.window); // true를 반환한다.
   ```

자기 자신을 참조하는 window 라는 프로퍼티가 있다는 것은 (아마도) 전역 객체를 쉽게 참조하기 위함으로 생각된다.(없다면 스크립트 첫 부분에 다음과 같이 직접 만들어주었어야 했다. var window = this;)

다른 이유로는, 만약 이 프로퍼티가 없다면 다음과 같이 작성이 불가능하기 때문이다: "{{domxref("window.open","window.open('http://google.com/')")}}" - 대신 다음과 같이 적어야 할 것이다. "open('http\://google.com/')"

Yet another reason to use this property is for libraries which wish to offer OOP-versions and non-OOP versions (especially JavaScript modules). If, for example, we refer to "this.window\.location.href", a [JavaScript module](/ko/docs/Mozilla/JavaScript_code_modules) could define a property called "window" inside of a class it defined (since no global "window" variable exists for it by default) which, could be created, for example, after passing in a window object to the module class' constructor. Thus, "this.window" inside of its functions would refer to that window object. In the non-namespaced version, "this.window" would simply refer back to "window", and also be able to get the document location without trouble. Another advantage is that the objects of such a class (even if the class were defined outside of a module) could change their reference to the window at will, as they would not be able to do if they had hard-coded a reference to "window" (yet the default in the class could still be set as the current window object).

## Specification

- [HTML Standard](http://www.whatwg.org/specs/web-apps/current-work/multipage/browsers.html#dom-window)

---
# Source: Web_CSS_box-shadow.md
---
---
title: box-shadow
slug: Web/CSS/box-shadow
---

{{ CSSRef }}

`box-shadow` CSS 속성은 요소의 테두리를 감싼 그림자 효과를 추가합니다. 쉼표로 구문해서 여러 그림자 효과를 입힐 수 있습니다. 박스 그림자는 요소에서의 수평수직 거리(오프셋), 흐릿함과 확산 정도, 색상으로 이루어집니다.

{{InteractiveExample("CSS Demo: box-shadow")}}

```css interactive-example-choice
box-shadow: 10px 5px 5px red;
```

```css interactive-example-choice
box-shadow: 60px -16px teal;
```

```css interactive-example-choice
box-shadow: 12px 12px 2px 1px rgba(0, 0, 255, 0.2);
```

```css interactive-example-choice
box-shadow: inset 5em 1em gold;
```

```css interactive-example-choice
box-shadow:
  3px 3px red,
  -1em 0 0.4em olive;
```

```html interactive-example
<section id="default-example">
  <div class="transition-all" id="example-element">
    <p>This is a box with a box-shadow around it.</p>
  </div>
</section>
```

```css interactive-example
#example-element {
  margin: 20px auto;
  padding: 0;
  border: 2px solid #333;
  width: 80%;
  text-align: center;
}
```

`box-shadow` 속성은 거의 모든 요소의 테두리에서 그림자를 드리울 수 있도록 도와줍니다. {{cssxref("border-radius")}}가 요소에 함께 적용됐다면 박스 그림자의 모서리도 똑같이 둥근 모서리를 갖게 됩니다. 여러 그림자의 z축 순서는 {{cssxref("text-shadow")}}와 동일하게 처음 그림자일수록 위로 올라옵니다.

[박스 그림자 생성기](/ko/docs/Web/CSS/CSS_Background_and_Borders/Box-shadow_generator)는 상호작용형 도구로, 쉽게 `box-shadow`의 값을 생성할 수 있습니다.

## 구문

```css
/* offset-x | offset-y | color */
box-shadow: 60px -16px teal;

/* offset-x | offset-y | blur-radius | color */
box-shadow: 10px 5px 5px black;

/* offset-x | offset-y | blur-radius | spread-radius | color */
box-shadow: 2px 2px 2px 1px rgba(0, 0, 0, 0.2);

/* inset | offset-x | offset-y | color */
box-shadow: inset 5em 1em gold;

/* Any number of shadows, separated by commas */
box-shadow:
  3px 3px red,
  -1em 0 0.4em olive;

/* Global keywords */
box-shadow: inherit;
box-shadow: initial;
box-shadow: unset;
```

하나의 `box-shadow`는 다음 구성요소로 지정할 수 있습니다.

- 두 개에서 네 개의 {{cssxref("&lt;length&gt;")}} 값.
  - 두 개의 값을 사용하면 `<offset-x><offset-y>`로 분석합니다.
  - 세 번째 값이 주어지면 `<blur-radius>`로 분석합니다.
  - 네 번째 값이 주어지면 `<spread-radius>`로 분석합니다.

- 선택사항으로 `inset` 키워드.
- 선택사항으로 {{cssxref("&lt;color&gt;")}} 값.

### 값

- `inset`
  - : 값을 지정하지 않으면(기본값) 요소가 공중에 떠있는 것처럼 밖에 드리우는 그림자가 됩니다.

    `inset` 키워드가 존재하면 요소가 움푹 들어간 것처럼 그림자가 요소의 테두리 안, 배경색 위, 내부 콘텐츠 밑에 그려집니다.

- `<offset-x>` `<offset-y>`
  - : 그림자의 위치를 설정하는 두 개의 {{cssxref("&lt;length&gt;")}} 값입니다. `<offset-x>`는 수평 거리를 의미하며 음수 값은 그림자를 요소의 왼쪽에 표시합니다. `<offset-y>`는 수직 거리를 의미하며 음수 값은 그림자를 요소의 위쪽에 표시합니다. 가능한 단위는 {{cssxref("&lt;length&gt;")}}를 참고하세요.

  두 값이 모두 `0`이면 그림자가 요소 바로 뒤쪽에 위치하며, `<blur-radius>` 또는 `<spread-radius>`가 존재하면 흐려지는 효과를 볼 수 있습니다.

- `<blur-radius>`
  - : 세 번째 {{cssxref("&lt;length&gt;")}} 값입니다. 크면 클 수록 그림자 테두리가 흐려지므로 크기는 더 커지고 색은 더 밝아집니다. 음수 값은 사용할 수 없습니다. 값을 설정하지 않으면 `0`이 되어 테두리가 선명해집니다. 명세는 흐림 효과의 지름을 어떻게 계산해야 하는지 정확한 알고리즘은 명시하지 않았지만 대신 다음과 같이 설명하고 있습니다.

  …for a long, straight shadow edge, this should create a color transition the length of the blur distance that is perpendicular to and centered on the shadow's edge, and that ranges from the full shadow color at the radius endpoint inside the shadow to fully transparent at the endpoint outside it.

- `<spread-radius>`
  - : 네 번째 {{cssxref("&lt;length&gt;")}} 값입니다. 양수 값은 그림자가 더 커지고 확산하며, 음수 값은 그림자가 줄어듭니다. 기본값은 `0`(그림자와 요소 크기 동일)입니다.
- `<color>`
  - : 가능한 키워드와 표기법은 {{cssxref("&lt;color&gt;")}}를 참고하세요.

    기본값은 브라우저에 따라 다릅니다. 보통 {{cssxref("color")}} 속성의 값을 사용하지만, Safari는 투명한 그림자가 기본값입니다.

### 보간

Each shadow in the list (treating `none` as a 0-length list) is interpolated via the color (as color) component, and x, y, blur, and (when appropriate) spread (as length) components. For each shadow, if both input shadows are or are not `inset`, then the interpolated shadow must match the input shadows in that regard. If any pair of input shadows has one `inset` and the other not `inset`, the entire shadow list is uninterpolable. If the lists of shadows have different lengths, then the shorter list is padded at the end with shadows whose color is `transparent`, all lengths are `0`, and whose `inset` (or not) matches the longer list.

### 형식 구문

{{csssyntax}}

## 예제

- [box-shadow test](http://www.elektronotdienst-nuernberg.de/bugs/box-shadow_inset.html)
- [box-shadow tutorial and examples](http://markusstange.wordpress.com/2009/02/15/fun-with-box-shadows/)

## 명세

{{Specifications}}

{{cssinfo}}

## 브라우저 호환성

{{Compat}}

## 같이 보기

- {{cssxref("&lt;color&gt;")}} 자료형
- Other color-related properties: {{cssxref("color")}}, {{cssxref("background-color")}}, {{cssxref("border-color")}}, {{cssxref("outline-color")}}, {{cssxref("text-decoration-color")}}, {{cssxref("text-emphasis-color")}}, {{cssxref("caret-color")}}, and {{cssxref("column-rule-color")}}
- [Applying color to HTML elements using CSS](/ko/docs/Web/HTML/Applying_color)

---
# Source: Web_API_Web_Workers_API_Using_web_workers.md
---
---
title: 웹 워커 사용하기
slug: Web/API/Web_Workers_API/Using_web_workers
---

웹 워커는 웹 컨텐츠를 위해서 백그라운드 스레드에서 스크립트를 실행할 간편한 방법을 제공합니다. 워커 스레드는 사용자 인터페이스(UI)를 방해하지 않고 작업을 수행할 수 있습니다. 또한 워커는 ( `responseXML` 과 `channel`속성이 언제나 null이지만) [`XMLHttpRequest`](/en/nsIXMLHttpRequest) 를 사용하여 I/O작업을 수행할 수도 있습니다. 워커는 생성이 된 후에 생성자가 명시한 이벤트 핸들러로 메세지를 올려서 자신의 하위 작업(spawning task)에 메세지를 전달할 수 도 있습니다. 본 글에서 전용 워커와 공유 워커에 대하여 소개합니다.

## Web Workers API

Worker는 생성자(예를 들면 {{domxref("Worker.Worker", "Worker()")}})를 사용하여 생성된 객체이며 이름있는 JavaScript 파일(이 파일은 Worker 스레드에서 실행하는 코드를 가집니다)을 실행합니다. 또한 Worker는 현재의 {{domxref("window")}}와는 다른 글로벌 컨텍스트에서 실행됩니다. 따라서 {{domxref("Worker")}} 내에서 현재의 글로벌 스코프를 접근하기 위해 ({{domxref("window.self","self")}} 대신에) {{domxref("window")}}를 사용해도 오류가 돌아옵니다.

Worker의 콘텍스트는 Dedicated Workers(한 개의 스크립트가 이용하는 표준적인 Workers)일 경우{{domxref("DedicatedWorkerGlobalScope")}} 객체로 제공됩니다. (Shared Workers의 경우는 {{domxref("SharedWorkerGlobalScope")}}). Dedicated Worker 는 Worker 를 처음에 생성한 스크립트만 액세스 할 수 있습니다. 반면에 Shared Worker는, 복수의 스크립트에서 액세스 할 수 있습니다.

> **참고:** **메모**: Worker 의 레퍼런스 문서나 추가적인 가이드에 대해서는 [The Web Workers API landing page](/ko/docs/Web/API/Web_Workers_API)를 봐 주세요.

Worker Thread에서는 몇 가지 제한 하에서 어떤 코드라도 실행할 수 있습니다. 예를 들어, Worker내에서는 직접 DOM 를 조작할 수 없습니다. 그리고 {{domxref("window")}} 객체의 기본 메서드나 속성에서 사용할 수 없는 것들이 있습니다. 그럼에도 [WebSockets](/ko/docs/Web/API/WebSockets_API)과 [IndexedDB](/ko/docs/Web/API/IndexedDB_API), [Data Store API](/ko/docs/Web/API/Data_Store_API)(Firefox OS 한정)와 같은 데이터 스토리지 메커니즘 등, `window`에 있는 다수의 아이템을 사용할 수 있습니다.자세한 것은 [Functions and classes available to workers](/ko/docs/Web/API/Worker/Functions_and_classes_available_to_workers)를 봐 주세요.

Worker와 메인 스레드 사이에서는 메시지 시스템을 통해 데이터를 발송합니다. 양쪽 모두 `postMessage()` 메서드를 사용하여 메시지를 발송하고, `onmessage`이벤트 핸들러에 의해 메시지에 응답합니다(메시지는 {{event("Message")}}이벤트의 data 속성에 들어갑니다). 데이터는 공유되지 않고 복사됩니다.

Worker 는 새로운 Worker 를 작성할 수 있습니다만, 생성된 Worker는 같은 부모 페이지일 경우에 한합니다. 추가적으로 Worker는 네트워크 I/O를 위한 [`XMLHttpRequest`](/ko/docs/Web/API/XMLHttpRequest)를 사용할 수 있으나, `responseXML`의 exception과 `channel`속성의 `XMLHttpRequest`는 항상 null을 반환합니다.

## Dedicated workers

As mentioned above, a dedicated worker is only accessible by the script that called it. In this section we'll discuss the JavaScript found in our [Basic dedicated worker example](https://github.com/mdn/simple-web-worker) ([run dedicated worker](https://mdn.github.io/simple-web-worker/)): This allows you to enter two numbers to be multiplied together. The numbers are sent to a dedicated worker, multiplied together, and the result is returned to the page and displayed.

This example is rather trivial, but we decided to keep it simple while introducing you to basic worker concepts. More advanced details are covered later on in the article.

### Worker feature detection

For slightly more controlled error handling and backwards compatibility, it is a good idea to wrap your worker accessing code in the following ([main.js](https://github.com/mdn/simple-web-worker/blob/gh-pages/main.js)):

```js
if (window.Worker) {

  ...

}
```

### Spawning a dedicated worker

Creating a new worker is simple. All you need to do is call the {{domxref("Worker.Worker", "Worker()")}} constructor, specifying the URI of a script to execute in the worker thread ([main.js](https://github.com/mdn/simple-web-worker/blob/gh-pages/main.js)):

```js
var myWorker = new Worker("worker.js");
```

### Sending messages to and from a dedicated worker

The magic of workers happens via the {{domxref("Worker.postMessage", "postMessage()")}} method and the {{domxref("Worker.onmessage", "onmessage")}} event handler. When you want to send a message to the worker, you post messages to it like this ([main.js](https://github.com/mdn/simple-web-worker/blob/gh-pages/main.js)):

```js
first.onchange = function () {
  myWorker.postMessage([first.value, second.value]);
  console.log("Message posted to worker");
};

second.onchange = function () {
  myWorker.postMessage([first.value, second.value]);
  console.log("Message posted to worker");
};
```

So here we have two {{htmlelement("input")}} elements represented by the variables `first` and `second`; when the value of either is changed, `myWorker.postMessage([first.value,second.value])` is used to send the value inside both to the worker, as an array. You can send pretty much anything you like in the message.

In the worker, we can respond when the message is received by writing an event handler block like this ([worker.js](https://github.com/mdn/simple-web-worker/blob/gh-pages/worker.js)):

```js
onmessage = function (e) {
  console.log("Message received from main script");
  var workerResult = "Result: " + e.data[0] * e.data[1];
  console.log("Posting message back to main script");
  postMessage(workerResult);
};
```

The `onmessage` handler allows us to run some code whenever a message is received, with the message itself being available in the `message` event's `data` attribute. Here we simply multiply together the two numbers then use `postMessage()` again, to post the result back to the main thread.

Back in the main thread, we use `onmessage` again, to respond to the message sent back from the worker:

```js
myWorker.onmessage = function (e) {
  result.textContent = e.data;
  console.log("Message received from worker");
};
```

Here we grab the message event data and set it as the `textContent` of the result paragraph, so the user can see the result of the calculation.

> **참고:** Notice that `onmessage` and `postMessage()` need to be hung off the `Worker` object when used in the main script thread, but not when used in the worker. This is because, inside the worker, the worker is effectively the global scope.

> **참고:** When a message is passed between the main thread and worker, it is copied or "transferred" (moved), not shared. Read [Transferring data to and from workers: further details](#transferring_data_to_and_from_workers_further_details) for a much more thorough explanation.

### Terminating a worker

If you need to immediately terminate a running worker from the main thread, you can do so by calling the worker's {{domxref("Worker", "terminate")}} method:

```js
myWorker.terminate();
```

The worker thread is killed immediately without an opportunity to complete its operations or clean up after itself.

In the worker thread, workers may close themselves by calling their own {{domxref("WorkerGlobalScope", "close")}} method:

```js
close();
```

### Handling errors

When a runtime error occurs in the worker, its `onerror` event handler is called. It receives an event named `error` which implements the `ErrorEvent` interface.

The event doesn't bubble and is cancelable; to prevent the default action from taking place, the worker can call the error event's [`preventDefault()`](/ko/docs/Web/API/Event/preventDefault) method.

The error event has the following three fields that are of interest:

- `message`
  - : A human-readable error message.
- `filename`
  - : The name of the script file in which the error occurred.
- `lineno`
  - : The line number of the script file on which the error occurred.

### Spawning subworkers

Workers may spawn more workers if they wish. So-called sub-workers must be hosted within the same origin as the parent page. Also, the URIs for subworkers are resolved relative to the parent worker's location rather than that of the owning page. This makes it easier for workers to keep track of where their dependencies are.

### Importing scripts and libraries

Worker threads have access to a global function, `importScripts()`, which lets them import scripts. It accepts zero or more URIs as parameters to resources to import; all of the following examples are valid:

```js
importScripts(); /* imports nothing */
importScripts("foo.js"); /* imports just "foo.js" */
importScripts("foo.js", "bar.js"); /* imports two scripts */
importScripts(
  "//example.com/hello.js",
); /* You can import scripts from other origins */
```

The browser loads each listed script and executes it. Any global objects from each script may then be used by the worker. If the script can't be loaded, `NETWORK_ERROR` is thrown, and subsequent code will not be executed. Previously executed code (including code deferred using {{domxref("window.setTimeout()")}}) will still be functional though. Function declarations **after** the `importScripts()`method are also kept, since these are always evaluated before the rest of the code.

> **참고:** Scripts may be downloaded in any order, but will be executed in the order in which you pass the filenames into `importScripts()` . This is done synchronously; `importScripts()` does not return until all the scripts have been loaded and executed.

## Shared workers

A shared worker is accessible by multiple scripts — even if they are being accessed by different windows, iframes or even workers. In this section we'll discuss the JavaScript found in our [Basic shared worker example](https://github.com/mdn/simple-shared-worker) ([run shared worker](https://mdn.github.io/simple-shared-worker/)): This is very similar to the basic dedicated worker example, except that it has two functions available handled by different script files: _multiplying two numbers_, or _squaring a number_. Both scripts use the same worker to do the actual calculation required.

Here we'll concentrate on the differences between dedicated and shared workers. Note that in this example we have two HTML pages, each with JavaScript applied that uses the same single worker file.

> **참고:** If SharedWorker can be accessed from several browsing contexts, all those browsing contexts must share the exact same origin (same protocol, host, and port).

> **참고:** In Firefox, shared workers cannot be shared between documents loaded in private and non-private windows ([Firefox bug 1177621](https://bugzil.la/1177621)).

### Spawning a shared worker

Spawning a new worker is pretty much the same as with a dedicated worker, but with a different constructor name (see [index.html](https://github.com/mdn/simple-shared-worker/blob/gh-pages/index.html) and [index2.html](https://mdn.github.io/simple-shared-worker/index2.html)) — each one has to spin up the worker using code like the following:

```js
var myWorker = new SharedWorker("worker.js");
```

One big difference is that with a shared worker you have to communicate via a `port` object — an explicit port is opened that the scripts can use to communicate with the worker (this is done implicitly in the case of dedicated workers).

The port connection needs to be started either implicitly by use of the `onmessage` event handler or explicitly with the `start()`method before any messages can be posted. Although the [multiply.js](https://github.com/mdn/simple-shared-worker/blob/gh-pages/multiply.js) and [worker.js](https://github.com/mdn/simple-shared-worker/blob/gh-pages/worker.js) files in the demo currently call the `start()`method, those calls are not necessary since the `onmessage` event handler is being used. Calling `start()` is only needed if the `message` event is wired up via the `addEventListener()` method.

When using the `start()` method to open the port connection, it needs to be called from both the parent thread and the worker thread if two-way communication is needed.

```js
myWorker.port.start(); // called in parent thread
```

```js
port.start(); // called in worker thread, assuming the port variable references a port
```

### Sending messages to and from a shared worker

Now messages can be sent to the worker as before, but the `postMessage()` method has to be invoked through the port object (again, you'll see similar constructs in both [multiply.js](https://github.com/mdn/simple-shared-worker/blob/gh-pages/multiply.js) and [square.js](https://github.com/mdn/simple-shared-worker/blob/gh-pages/square.js)):

```js
squareNumber.onchange = function () {
  myWorker.port.postMessage([squareNumber.value, squareNumber.value]);
  console.log("Message posted to worker");
};
```

Now, on to the worker. There is a bit more complexity here as well ([worker.js](https://github.com/mdn/simple-shared-worker/blob/gh-pages/worker.js)):

```js
onconnect = function (e) {
  var port = e.ports[0];

  port.onmessage = function (e) {
    var workerResult = "Result: " + e.data[0] * e.data[1];
    port.postMessage(workerResult);
  };
};
```

First, we use an `onconnect` handler to fire code when a connection to the port happens (i.e. when the `onmessage` event handler in the parent thread is setup, or when the `start()` method is explicitly called in the parent thread).

We use the `ports` attribute of this event object to grab the port and store it in a variable.

Next, we add a `message` handler on the port to do the calculation and return the result to the main thread. Setting up this `message`handler in the worker thread also implicitly opens the port connection back to the parent thread, so the call to `port.start()` is not actually needed, as noted above.

Finally, back in the main script, we deal with the message (again, you'll see similar constructs in both [multiply.js](https://github.com/mdn/simple-shared-worker/blob/gh-pages/multiply.js) and [square.js](https://github.com/mdn/simple-shared-worker/blob/gh-pages/square.js)):

```js
myWorker.port.onmessage = function (e) {
  result2.textContent = e.data;
  console.log("Message received from worker");
};
```

When a message comes back through the port from the worker, we check what result type it is, then insert the calculation result inside the appropriate result paragraph.

## About thread safety

The {{domxref("Worker")}} interface spawns real OS-level threads, and mindful programmers may be concerned that concurrency can cause "interesting" effects in your code if you aren't careful.

However, since web workers have carefully controlled communication points with other threads, it's actually very hard to cause concurrency problems. There's no access to non-threadsafe components or the DOM. And you have to pass specific data in and out of a thread through serialized objects. So you have to work really hard to cause problems in your code.

## Content security policy

Workers are considered to have their own execution context, distinct from the document that created them. For this reasons they are, in general, not governed by the [content security policy](/ko/docs/Mozilla/Add-ons/WebExtensions/Content_Security_Policy) of the document (or parent worker) that created them. So for example, suppose a document is served with the following header:

```
Content-Security-Policy: script-src 'self'
```

Among other things, this will prevent any scripts it includes from using [`eval()`](/ko/docs/Web/JavaScript/Reference/Global_Objects/eval). However, if the script constructs a worker, code running in the worker's context _will_ be allowed to use `eval()`.

To specify a content security policy for the worker, set a [Content-Security-Policy](/ko/docs/Web/HTTP/Headers/Content-Security-Policy) response header for the request which delivered the worker script itself.

The exception to this is if the worker script's origin is a globally unique identifier (for example, if its URL has a scheme of data or blob). In this case, the worker does inherit the CSP of the document or worker than created it.

## Transferring data to and from workers: further details

Data passed between the main page and workers is **copied**, not shared. Objects are serialized as they're handed to the worker, and subsequently, de-serialized on the other end. The page and worker **do not share the same instance**, so the end result is that **a duplicate** is created on each end. Most browsers implement this feature as [structured cloning](/ko/docs/Web/Guide/API/DOM/The_structured_clone_algorithm).

To illustrate this, let's create for didactical purpose a function named `emulateMessage()`, which will simulate the behavior of a value that is _cloned and not shared_ during the passage from a `worker` to the main page or vice versa:

```js
function emulateMessage(vVal) {
  return eval("(" + JSON.stringify(vVal) + ")");
}

// Tests

// test #1
var example1 = new Number(3);
console.log(typeof example1); // object
console.log(typeof emulateMessage(example1)); // number

// test #2
var example2 = true;
console.log(typeof example2); // boolean
console.log(typeof emulateMessage(example2)); // boolean

// test #3
var example3 = new String("Hello World");
console.log(typeof example3); // object
console.log(typeof emulateMessage(example3)); // string

// test #4
var example4 = {
  name: "John Smith",
  age: 43,
};
console.log(typeof example4); // object
console.log(typeof emulateMessage(example4)); // object

// test #5
function Animal(sType, nAge) {
  this.type = sType;
  this.age = nAge;
}
var example5 = new Animal("Cat", 3);
alert(example5.constructor); // Animal
alert(emulateMessage(example5).constructor); // Object
```

A value that is cloned and not shared is called _message_. As you will probably know by now, _messages_ can be sent to and from the main thread by using `postMessage()`, and the `message` event's {{domxref("MessageEvent.data", "data")}} attribute contains data passed back from the worker.

**example.html**: (the main page):

```js
var myWorker = new Worker("my_task.js");

myWorker.onmessage = function (oEvent) {
  console.log("Worker said : " + oEvent.data);
};

myWorker.postMessage("ali");
```

**my_task.js** (the worker):

```js
postMessage("I'm working before postMessage('ali').");

onmessage = function (oEvent) {
  postMessage("Hi " + oEvent.data);
};
```

The [structured cloning](/ko/docs/Web/Guide/API/DOM/The_structured_clone_algorithm) algorithm can accept JSON and a few things that JSON can't — like circular references.

### Passing data examples

#### Example #1: Create a generic "asynchronous `eval()`"

The following example shows how to use a worker in order to **asynchronously** execute any JavaScript code allowed in a worker, through [`eval()`](/ko/docs/Web/JavaScript/Reference/Global_Objects/eval) within the worker:

```js
// Syntax: asyncEval(code[, listener])

var asyncEval = (function () {
  var aListeners = [],
    oParser = new Worker(
      "data:text/javascript;charset=US-ASCII,onmessage%20%3D%20function%20%28oEvent%29%20%7B%0A%09postMessage%28%7B%0A%09%09%22id%22%3A%20oEvent.data.id%2C%0A%09%09%22evaluated%22%3A%20eval%28oEvent.data.code%29%0A%09%7D%29%3B%0A%7D",
    );

  oParser.onmessage = function (oEvent) {
    if (aListeners[oEvent.data.id]) {
      aListeners[oEvent.data.id](oEvent.data.evaluated);
    }
    delete aListeners[oEvent.data.id];
  };

  return function (sCode, fListener) {
    aListeners.push(fListener || null);
    oParser.postMessage({
      id: aListeners.length - 1,
      code: sCode,
    });
  };
})();
```

The [data URL](/ko/docs/Web/HTTP/data_URIs) is equivalent to a network request, with the following response:

```js
onmessage = function (oEvent) {
  postMessage({
    id: oEvent.data.id,
    evaluated: eval(oEvent.data.code),
  });
};
```

Sample usage:

```js
// asynchronous alert message...
asyncEval("3 + 2", function (sMessage) {
  alert("3 + 2 = " + sMessage);
});

// asynchronous print message...
asyncEval('"Hello World!!!"', function (sHTML) {
  document.body.appendChild(document.createTextNode(sHTML));
});

// asynchronous void...
asyncEval(
  '(function () {\n\tvar oReq = new XMLHttpRequest();\n\toReq.open("get", "http://www.mozilla.org/", false);\n\toReq.send(null);\n\treturn oReq.responseText;\n})()',
);
```

#### Example #2: Advanced passing JSON Data and creating a switching system

If you have to pass some complex data and have to call many different functions both on the main page and in the Worker, you can create a system which groups everything together.

First, we create a QueryableWorker class that takes the url of the worker, a default listener, and an error handler, and this class is gonna keep track of a list of listeners and help us communicate wirh the worker:

```js
function QueryableWorker(url, defaultListener, onError) {
  var instance = this,
    worker = new Worker(url),
    listeners = {};

  this.defaultListener = defaultListener || function () {};

  if (onError) {
    worker.onerror = onError;
  }

  this.postMessage = function (message) {
    worker.postMessage(message);
  };

  this.terminate = function () {
    worker.terminate();
  };
}
```

Then we add the methods of adding/removing listeners:

```js
this.addListeners = function (name, listener) {
  listeners[name] = listener;
};

this.removeListeners = function (name) {
  delete listeners[name];
};
```

Here we let the worker handle two simple operations for illuatration: getting the difference of two numbers and making an alert after three seconds. In order to acheieve that we first implement a sendQuery method which queries if the worker actually has the corresponding methods to do what we want.

```js
/*
  This functions takes at least one argument, the method name we want to query.
  Then we can pass in the arguments that the method needs.
 */
this.sendQuery = function () {
  if (arguments.length < 1) {
    throw new TypeError(
      "QueryableWorker.sendQuery takes at least one argument",
    );
    return;
  }
  worker.postMessage({
    queryMethod: arguments[0],
    queryArguments: Array.prototype.slice.call(arguments, 1),
  });
};
```

We finish QueryableWorker with the `onmessage` method. If the worker has the corresponding methods we queried, it should return the name of the corresponding listener and the arguments it needs, we just need to find it in `listeners`.:

```js
worker.onmessage = function (event) {
  if (
    event.data instanceof Object &&
    event.data.hasOwnProperty("queryMethodListener") &&
    event.data.hasOwnProperty("queryMethodArguments")
  ) {
    listeners[event.data.queryMethodListener].apply(
      instance,
      event.data.queryMethodArguments,
    );
  } else {
    this.defaultListener.call(instance, event.data);
  }
};
```

Now onto the worker. First we need to have the methods to handle the two simple operations:

```js
var queryableFunctions = {
  getDifference: function (a, b) {
    reply("printStuff", a - b);
  },
  waitSomeTime: function () {
    setTimeout(function () {
      reply("doAlert", 3, "seconds");
    }, 3000);
  },
};

function reply() {
  if (arguments.length < 1) {
    throw new TypeError("reply - takes at least one argument");
    return;
  }
  postMessage({
    queryMethodListener: arguments[0],
    queryMethodArguments: Array.prototype.slice.call(arguments, 1),
  });
}

/* This method is called when main page calls QueryWorker's postMessage method directly*/
function defaultReply(message) {
  // do something
}
```

And the `onmessage` method is now trivial:

```js
onmessage = function (event) {
  if (
    event.data instanceof Object &&
    event.data.hasOwnProperty("queryMethod") &&
    event.data.hasOwnProperty("queryMethodArguments")
  ) {
    queryableFunctions[event.data.queryMethod].apply(
      self,
      event.data.queryMethodArguments,
    );
  } else {
    defaultReply(event.data);
  }
};
```

Here are the full implementation:

**example.html** (the main page):

```html
<!doctype html>
<html>
  <head>
    <meta charset="UTF-8" />
    <title>MDN Example - Queryable worker</title>
    <script type="text/javascript">
      /*
      QueryableWorker instances methods:
        * sendQuery(queryable function name, argument to pass 1, argument to pass 2, etc. etc): calls a Worker's queryable function
        * postMessage(string or JSON Data): see Worker.prototype.postMessage()
        * terminate(): terminates the Worker
        * addListener(name, function): adds a listener
        * removeListener(name): removes a listener
      QueryableWorker instances properties:
        * defaultListener: the default listener executed only when the Worker calls the postMessage() function directly
     */
      function QueryableWorker(url, defaultListener, onError) {
        var instance = this,
          worker = new Worker(url),
          listeners = {};

        this.defaultListener = defaultListener || function () {};

        if (onError) {
          worker.onerror = onError;
        }

        this.postMessage = function (message) {
          worker.postMessage(message);
        };

        this.terminate = function () {
          worker.terminate();
        };

        this.addListeners = function (name, listener) {
          listeners[name] = listener;
        };

        this.removeListeners = function (name) {
          delete listeners[name];
        };

        worker.onmessage = function (event) {
          if (
            event.data instanceof Object &&
            event.data.hasOwnProperty("queryMethodListener") &&
            event.data.hasOwnProperty("queryMethodArguments")
          ) {
            listeners[event.data.queryMethodListener].apply(
              instance,
              event.data.queryMethodArguments,
            );
          } else {
            this.defaultListener.call(instance, event.data);
          }
        };
      }

      // your custom "queryable" worker
      var myTask = new QueryableWorker("my_task.js");

      // your custom "listeners"
      myTask.addListener("printStuff", function (result) {
        document
          .getElementById("firstLink")
          .parentNode.appendChild(
            document.createTextNode(" The difference is " + result + "!"),
          );
      });

      myTask.addListener("doAlert", function (time, unit) {
        alert("Worker waited for " + time + " " + unit + " :-)");
      });
    </script>
  </head>
  <body>
    <ul>
      <li>
        <a
          id="firstLink"
          href="javascript:myTask.sendQuery('getDifference', 5, 3);"
          >What is the difference between 5 and 3?</a
        >
      </li>
      <li>
        <a href="javascript:myTask.sendQuery('waitSomeTime');"
          >Wait 3 seconds</a
        >
      </li>
      <li>
        <a href="javascript:myTask.terminate();">terminate() the Worker</a>
      </li>
    </ul>
  </body>
</html>
```

**my_task.js** (the worker):

```js
var queryableFunctions = {
  // example #1: get the difference between two numbers:
  getDifference: function (nMinuend, nSubtrahend) {
    reply("printSomething", nMinuend - nSubtrahend);
  },
  // example #2: wait three seconds
  waitSomeTime: function () {
    setTimeout(function () {
      reply("doAlert", 3, "seconds");
    }, 3000);
  },
};

// system functions

function defaultReply(message) {
  // your default PUBLIC function executed only when main page calls the queryableWorker.postMessage() method directly
  // do something
}

function reply() {
  if (arguments.length < 1) {
    throw new TypeError("reply - not enough arguments");
    return;
  }
  postMessage({
    queryMethodListener: arguments[0],
    queryMethodArguments: Array.prototype.slice.call(arguments, 1),
  });
}

onmessage = function (oEvent) {
  if (
    oEvent.data instanceof Object &&
    oEvent.data.hasOwnProperty("queryMethod") &&
    oEvent.data.hasOwnProperty("queryMethodArguments")
  ) {
    queryableFunctions[oEvent.data.queryMethod].apply(
      self,
      oEvent.data.queryMethodArguments,
    );
  } else {
    defaultReply(oEvent.data);
  }
};
```

It is possible to switch the content of each mainpage -> worker and worker -> mainpage message. And the property names "queryMethod", "queryMethodListeners", "queryMethodArguments" can be anything as long as they are consistent in `QueryableWorker` and the `worker`.

### Passing data by transferring ownership (transferable objects)

Google Chrome 17+ and Firefox 18+ contain an additional way to pass certain types of objects (transferable objects, that is objects implementing the {{domxref("Transferable")}} interface) to or from a worker with high performance. Transferable objects are transferred from one context to another with a zero-copy operation, which results in a vast performance improvement when sending large data sets. Think of it as pass-by-reference if you're from the C/C++ world. However, unlike pass-by-reference, the 'version' from the calling context is no longer available once transferred. Its ownership is transferred to the new context. For example, when transferring an {{domxref("ArrayBuffer")}} from your main app to a worker script, the original {{domxref("ArrayBuffer")}} is cleared and no longer usable. Its content is (quite literally) transferred to the worker context.

```js
// Create a 32MB "file" and fill it.
var uInt8Array = new Uint8Array(1024 * 1024 * 32); // 32MB
for (var i = 0; i < uInt8Array.length; ++i) {
  uInt8Array[i] = i;
}

worker.postMessage(uInt8Array.buffer, [uInt8Array.buffer]);
```

> **참고:** For more information on transferable objects, performance, and feature-detection for this method, read [Transferable Objects: Lightning Fast!](http://updates.html5rocks.com/2011/12/Transferable-Objects-Lightning-Fast) on HTML5 Rocks.

## Embedded workers

There is not an "official" way to embed the code of a worker within a web page, like {{HTMLElement("script")}} elements do for normal scripts. But a {{HTMLElement("script")}} element that does not have a `src` attribute and has a `type` attribute that does not identify an executable MIME type can be considered a data block element that JavaScript could use. "Data blocks" is a more general feature of HTML5 that can carry almost any textual data. So, a worker could be embedded in this way:

```js
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8" />
<title>MDN Example - Embedded worker</title>
<script type="text/js-worker">
  // This script WON'T be parsed by JS engines because its MIME type is text/js-worker.
  var myVar = "Hello World!";
  // Rest of your worker code goes here.
</script>
<script type="text/javascript">
  // This script WILL be parsed by JS engines because its MIME type is text/javascript.
  function pageLog (sMsg) {
    // Use a fragment: browser will only render/reflow once.
    var oFragm = document.createDocumentFragment();
    oFragm.appendChild(document.createTextNode(sMsg));
    oFragm.appendChild(document.createElement("br"));
    document.querySelector("#logDisplay").appendChild(oFragm);
  }
</script>
<script type="text/js-worker">
  // This script WON'T be parsed by JS engines because its MIME type is text/js-worker.
  onmessage = function (oEvent) {
    postMessage(myVar);
  };
  // Rest of your worker code goes here.
</script>
<script type="text/javascript">
  // This script WILL be parsed by JS engines because its MIME type is text/javascript.

  // In the past...:
  // blob builder existed
  // ...but now we use Blob...:
  var blob = new Blob(Array.prototype.map.call(document.querySelectorAll("script[type=\"text\/js-worker\"]"), function (oScript) { return oScript.textContent; }),{type: "text/javascript"});

  // Creating a new document.worker property containing all our "text/js-worker" scripts.
  document.worker = new Worker(window.URL.createObjectURL(blob));

  document.worker.onmessage = function (oEvent) {
    pageLog("Received: " + oEvent.data);
  };

  // Start the worker.
  window.onload = function() { document.worker.postMessage(""); };
</script>
</head>
<body><div id="logDisplay"></div></body>
</html>
```

The embedded worker is now nested into a new custom `document.worker` property.

It is also worth noting that you can also convert a function into a Blob, then generate an object URL from that blob. For example:

```js
function fn2workerURL(fn) {
  var blob = new Blob(["(" + fn.toString() + ")()"], {
    type: "application/javascript",
  });
  return URL.createObjectURL(blob);
}
```

## Further examples

This section provides further examples of how to use web workers.

### Performing computations in the background

Workers are mainly useful for allowing your code to perform processor-intensive calculations without blocking the user interface thread. In this example, a worker is used to calculate Fibonacci numbers.

#### The JavaScript code

The following JavaScript code is stored in the "fibonacci.js" file referenced by the HTML in the next section.

```js
var results = [];

function resultReceiver(event) {
  results.push(parseInt(event.data));
  if (results.length == 2) {
    postMessage(results[0] + results[1]);
  }
}

function errorReceiver(event) {
  throw event.data;
}

onmessage = function (event) {
  var n = parseInt(event.data);

  if (n == 0 || n == 1) {
    postMessage(n);
    return;
  }

  for (var i = 1; i <= 2; i++) {
    var worker = new Worker("fibonacci.js");
    worker.onmessage = resultReceiver;
    worker.onerror = errorReceiver;
    worker.postMessage(n - i);
  }
};
```

The worker sets the property `onmessage` to a function which will receive messages sent when the worker object's `postMessage()` is called (note that this differs from defining a global _variable_ of that name, or defining a _function_ with that name. `var onmessage` and `function onmessage` will define global properties with those names, but they will not register the function to receive messages sent by the web page that created the worker). This starts the recursion, spawning new copies of itself to handle each iteration of the calculation.

#### The HTML code

```html
<!doctype html>
<html>
  <head>
    <meta charset="UTF-8" />
    <title>Test threads fibonacci</title>
  </head>
  <body>
    <div id="result"></div>

    <script language="javascript">
      var worker = new Worker("fibonacci.js");

      worker.onmessage = function (event) {
        document.getElementById("result").textContent = event.data;
        dump("Got: " + event.data + "\n");
      };

      worker.onerror = function (error) {
        dump("Worker error: " + error.message + "\n");
        throw error;
      };

      worker.postMessage("5");
    </script>
  </body>
</html>
```

The web page creates a `div` element with the ID `result` , which gets used to display the result, then spawns the worker. After spawning the worker, the `onmessage` handler is configured to display the results by setting the contents of the `div` element, and the `onerror` handler is set to [dump](/ko/docs/Debugging_JavaScript#dump.28.29) the error message.

Finally, a message is sent to the worker to start it.

[Try this example](/samples/workers/fibonacci).

### Performing web I/O in the background

You can find an example of this in the article [Using workers in extensions](/ko/docs/Using_workers_in_extensions) .

### Dividing tasks among multiple workers

As multi-core computers become increasingly common, it's often useful to divide computationally complex tasks among multiple workers, which may then perform those tasks on multiple-processor cores.

## Other types of worker

In addition to dedicated and shared web workers, there are other types of worker available:

- [ServiceWorkers](/ko/docs/Web/API/ServiceWorker_API) essentially act as proxy servers that sit between web applications, and the browser and network (when available). They are intended to (amongst other things) enable the creation of effective offline experiences, intercepting network requests and taking appropriate action based on whether the network is available and updated assets reside on the server. They will also allow access to push notifications and background sync APIs.
- Chrome Workers are a Firefox-only type of worker that you can use if you are developing add-ons and want to use workers in extensions and have access to [js-ctypes](/en/js-ctypes) in your worker. See {{domxref("ChromeWorker")}} for more details.
- [Audio Workers](/ko/docs/Web/API/Web_Audio_API#Audio_Workers) provide the ability for direct scripted audio processing to be done in a web worker context.

## Functions and interfaces available in workers

You can use most standard JavaScript features inside a web worker, including:

- {{domxref("Navigator")}}
- {{domxref("XMLHttpRequest")}}
- {{jsxref("Global_Objects/Array", "Array")}}, {{jsxref("Global_Objects/Date", "Date")}}, {{jsxref("Global_Objects/Math", "Math")}}, and {{jsxref("Global_Objects/String", "String")}}
- {{domxref("Window.requestAnimationFrame")}}, {{domxref("WindowTimers.setTimeout")}}, and {{domxref("WindowTimers.setInterval")}}

The main thing you _can't_ do in a Worker is directly affect the parent page. This includes manipulating the DOM and using that page's objects. You have to do it indirectly, by sending a message back to the main script via {{domxref("DedicatedWorkerGlobalScope.postMessage")}}, then actioning the changes from there.

> **참고:** For a complete list of functions available to workers, see [Functions and interfaces available to workers](/ko/docs/Web/Reference/Functions_and_classes_available_to_workers).

## 명세서

{{Specifications}}

## See also

- [`Worker`](/ko/docs/Web/API/Worker) interface
- [`SharedWorker`](/ko/docs/Web/API/SharedWorker) interface
- [Functions available to workers](/ko/docs/Web/API/Worker/Functions_and_classes_available_to_workers)
- [Advanced concepts and examples](/ko/docs/Web/API/Web_Workers_API/Using_web_workers)

---
# Source: Web_CSS_CSS_images_Using_CSS_gradients.md
---
---
title: CSS 그레이디언트 사용하기
slug: Web/CSS/CSS_images/Using_CSS_gradients
---

{{CSSRef}}

**CSS 그레이디언트**는 {{cssxref("&lt;image&gt;")}} 자료형의 특별한 종류인 {{cssxref("&lt;gradient&gt;")}}로 나타내며 두 개 이상의 색 간의 점진적 전환을 표현합니다. 그레이디언트에는 선형({{cssxref("linear-gradient")}} 함수), 방사형({{cssxref("radial-gradient")}} 함수), 각진 원형({{cssxref("conic-gradient")}} 함수) 세 종류가 있으며, 각각의 변형본으로 계속해서 반복하는 {{cssxref("repeating-linear-gradient")}}, {{cssxref("repeating-radial-gradient")}}, {{cssxref("repeating-conic-gradient")}} 함수도 있습니다.

그레이디언트는 배경처럼 `<image>`를 사용하는 곳에는 어디에나 적용할 수 있습니다. 그레이디언트는 동적으로 생성하므로, 비슷한 효과를 보기 위해 래스터 이미지를 사용하는 방식을 사용하지 않아도 됩니다. 또한 브라우저가 직접 생성하므로 확대했을 때 래스터 이미지보다 좋은 품질을 보이며 크기 조절도 즉시 가능합니다.

우선 선형 그레이디언트의 소개로 시작하여, 모든 유형의 그레이디언트에서 통용되는 기능을 선형으로 설명하고, 그 후에 방사형과 각진 원형, 마지막으로 반복 그레이디언트에 대해 알아보겠습니다.

## 선형 그레이디언트 사용하기

선형 그레이디언트는 직선으로 진행하는 색상 무늬를 생성합니다.

### 기본 선형 그레이디언트

가장 기본적인 그레이디언트 종류를 생성하기 위해서는 두 가지의 색만 지정하면 됩니다. 각각의 색을 "색상 정지점"이라고 부릅니다. 최소 두 가지가 필요하지만, 제한 없이 원하는 만큼 추가할 수 있습니다.

```html hidden
<div class="simple-linear"></div>
```

```css hidden
div {
  width: 120px;
  height: 120px;
}
```

```css
.simple-linear {
  background: linear-gradient(blue, pink);
}
```

{{ EmbedLiveSample('기본_선형_그레이디언트', 120, 120) }}

### 방향 전환

기본적으로, 선형 그레이디언트는 위에서 아래로 진행합니다. 그러나 방향을 지정함으로써 그레이디언트를 회전할 수 있습니다.

```html hidden
<div class="horizontal-gradient"></div>
```

```css hidden
div {
  width: 120px;
  height: 120px;
}
```

```css
.horizontal-gradient {
  background: linear-gradient(to right, blue, pink);
}
```

{{ EmbedLiveSample('방향_전환', 120, 120) }}

### 대각선 그레이디언트

그레이디언트가 한쪽 모서리에서 다른 쪽 모서리를 잇는 대각선 방향으로 진행하도록 할 수도 있습니다.

```html hidden
<div class="diagonal-gradient"></div>
```

```css hidden
div {
  width: 200px;
  height: 100px;
}
```

```css
.diagonal-gradient {
  background: linear-gradient(to bottom right, blue, pink);
}
```

{{ EmbedLiveSample('대각선_그레이디언트', 200, 100) }}

### 각도 사용

더 정밀하게 방향을 지정하고 싶다면 특정 각도를 지정할 수 있습니다.

```html hidden
<div class="angled-gradient"></div>
```

```css hidden
div {
  width: 120px;
  height: 120px;
}
```

```css
.angled-gradient {
  background: linear-gradient(70deg, blue, pink);
}
```

{{ EmbedLiveSample('각도_사용', 120, 120) }}

각도를 사용할 때 `0deg` 는 아래쪽에서 위쪽으로 진행하는 선형 그레이디언트를, `90deg` 는 왼쪽에서 오른쪽으로, 등등 시계 방향으로 회전합니다. 음의 각도는 시계 반대 방향으로 회전합니다.

![linear_redangles.png](/files/3811/linear_red_angles.png)

## 색상 선언 & 효과 생성

모든 CSS 그레이디언트 유형은 위치에 따라 변하는 색상의 범위입니다. CSS 그레이디언트가 생성하는 색상은 위치에 따라 연속적으로 변하며 부드러운 색상 전환을 이룹니다. 또한, 단색 띠를 만들거나 두 색상 간의 뚜렷한 전환을 생성하는 것도 가능합니다. 다음 사항들은 모든 그레이디언트 함수에 적용됩니다.

### 두 개보다 많은 색 사용하기

색상의 수는 두 가지로 제한되지 않으며, 원하는 만큼 사용할 수 있습니다! 기본적으로 색상은 그레이디언트에 따라 균일하게 배치됩니다.

```html hidden
<div class="auto-spaced-linear-gradient"></div>
```

```css hidden
div {
  width: 120px;
  height: 120px;
}
```

```css
.auto-spaced-linear-gradient {
  background: linear-gradient(red, yellow, blue, orange);
}
```

{{ EmbedLiveSample('두_개보다_많은_색_사용하기', 120, 120) }}

### 색상 정지점 위치 지정하기

색상 정지점을 기본 위치에 두지 않아도 됩니다. 위치를 세밀하게 조정하려면 각 정지점에 0개, 1개 또는 2개의 퍼센티지 값을 지정하거나, 방사형 및 선형 그레이디언트의 경우 절대 길이 값을 지정할 수 있습니다. 위치를 퍼센티지로 지정하면 0%는 시작 지점을, `100%`는 끝 지점을 나타냅니다. 그러나 원하는 효과를 얻기 위해 이 범위를 벗어나는 값을 사용할 수도 있습니다. 위치를 지정하지 않으면 첫 번째 색상 정지점은 자동으로 0%에, 마지막 색상 정지점은 `100%`에 배치되며, 나머지 색상 정지점은 인접한 색상 정지점의 중간에 자동으로 배치됩니다.

```html hidden
<div class="multicolor-linear"></div>
```

```css hidden
div {
  width: 120px;
  height: 120px;
}
```

```css
.multicolor-linear {
  background: linear-gradient(to left, lime 28px, red 77%, cyan);
}
```

{{ EmbedLiveSample('Positioning_color_stops', 120, 120) }}

### 경계선 만들기

두 색상 사이에 점진적인 전환 대신 명확한 경계선을 만들어 줄무늬를 만들려면, 인접한 색상 정지점을 동일한 위치에 설정할 수 있습니다. 이 예제에서는 색상들이 그레이디언트의 중간 지점인 `50%` 위치에서 색상 정지점을 공유합니다.

```html hidden
<div class="striped"></div>
```

```css hidden
div {
  width: 120px;
  height: 120px;
}
```

```css
.striped {
  background: linear-gradient(to bottom left, cyan 50%, palegoldenrod 50%);
}
```

{{ EmbedLiveSample('Creating_hard_lines', 120, 120) }}

### 그레이디언트 힌트

기본적으로 그레이디언트는 한 색상에서 다음 색상으로 고르게 전환됩니다. 그러나 전환의 중간점을 특정 지점으로 옮기기 위해 색상 힌트를 추가할 수 있습니다. 이 예제에서는 전환의 중간점을 50% 지점에서 10% 지점으로 옮겼습니다.

```html hidden
<div class="color-hint"></div>
<div class="simple-linear"></div>
```

```css hidden
div {
  width: 120px;
  height: 120px;
  float: left;
  margin-right: 10px;
}
```

```css
.color-hint {
  background: linear-gradient(blue, 10%, pink);
}
.simple-linear {
  background: linear-gradient(blue, pink);
}
```

{{ EmbedLiveSample('Gradient_hints', 120, 120) }}

### 색상 띠와 줄무늬 만들기

그레이디언트 안에 단색 영역을 만들려면 색상 정지점에 두 개의 위치를 지정하면 됩니다. 이렇게 하면 하나의 색상이 두 위치에 걸쳐 유지됩니다. 이는 동일한 색상이 서로 다른 위치에 두 개의 연속된 색상 정지점을 가지는 것과 동일합니다. 색상은 첫 번째 위치에서 색상이 완전히 나타나고, 두 번째 위치까지 그대로 유지됩니다. 그런 다음 인접한 색상 정지점에서 다음 색상으로 부드럽게 전환됩니다.

```html hidden
<div class="multiposition-stops"></div>
<div class="multiposition-stop2"></div>
```

```css hidden
div {
  width: 120px;
  height: 120px;
  float: left;
  margin-right: 10px;
  box-sizing: border-box;
}
```

```css
.multiposition-stops {
  background: linear-gradient(
    to left,
    lime 20%,
    red 30%,
    red 45%,
    cyan 55%,
    cyan 70%,
    yellow 80%
  );
  background: linear-gradient(
    to left,
    lime 20%,
    red 30% 45%,
    cyan 55% 70%,
    yellow 80%
  );
}
.multiposition-stop2 {
  background: linear-gradient(
    to left,
    lime 25%,
    red 25%,
    red 50%,
    cyan 50%,
    cyan 75%,
    yellow 75%
  );
  background: linear-gradient(
    to left,
    lime 25%,
    red 25% 50%,
    cyan 50% 75%,
    yellow 75%
  );
}
```

{{ EmbedLiveSample('Creating_color_bands_stripes', 120, 120) }}

In the first example above, the lime goes from the 0% mark, which is implied, to the 20% mark, transitions from lime to red over the next 10% of the width of the gradient, reach solid red at the 30% mark, and staying solid red up until 45% through the gradient, where it fades to cyan, being fully cyan for 15% of the gradient, and so on.

In the second example, the second color stop for each color is at the same location as the first color stop for the adjacent color, creating a striped effect.

In both examples, the gradient is written twice: the first is the CSS Images Level 3 method of repeating the color for each stop and the second example is the CSS Images Level 4 multiple color stop method of including two color-stop-lengths in a linear-color-stop declaration.

### Controlling the progression of a gradient

By default, a gradient evenly progresses between the colors of two adjacent color stops, with the midpoint between those two color stops being the midpoint color value. You can control the interpolation, or progression, between two color stops by including a color hint location. In this example, the color reaches the midpoint between lime and cyan 20% of the way through the gradient rather than 50% of the way through. The second example does not contain the hint to hilight the difference the color hint can make:

```html hidden
<div class="colorhint-gradient"></div>
<div class="regular-progression"></div>
```

```css hidden
div {
  width: 120px;
  height: 120px;
  float: left;
  margin-right: 10px;
  box-sizing: border-box;
}
```

```css
.colorhint-gradient {
  background: linear-gradient(to top, black, 20%, cyan);
}
.regular-progression {
  background: linear-gradient(to top, black, cyan);
}
```

{{ EmbedLiveSample('Controlling_the_progression_of_a_gradient', 120, 120) }}

### Overlaying gradients

Gradients support transparency, so you can stack multiple backgrounds to achieve some pretty fancy effects. The backgrounds are stacked from top to bottom, with the first specified being on top.

```html hidden
<div class="layered-image"></div>
```

```css hidden
div {
  width: 300px;
  height: 150px;
}
```

```css
.layered-image {
  background:
    linear-gradient(to right, transparent, mistyrose), url("critters.png");
}
```

{{ EmbedLiveSample('Overlaying_gradients', 300, 150) }}

### Stacked gradients

You can even stack gradients with other gradients. As long as the top gradients aren't entirely opaque, the gradients below will still be visible.

```html hidden
<div class="stacked-linear"></div>
```

```css hidden
div {
  width: 200px;
  height: 200px;
}
```

```css
.stacked-linear {
  background:
    linear-gradient(217deg, rgba(255, 0, 0, 0.8), rgba(255, 0, 0, 0) 70.71%),
    linear-gradient(127deg, rgba(0, 255, 0, 0.8), rgba(0, 255, 0, 0) 70.71%),
    linear-gradient(336deg, rgba(0, 0, 255, 0.8), rgba(0, 0, 255, 0) 70.71%);
}
```

{{ EmbedLiveSample('Stacked_gradients', 200, 200) }}

## Using radial gradients

Radial gradients are similar to linear gradients, except that they radiate out from a central point. You can dictate where that central point is. You can also make them circular or elliptical.

### A basic radial gradient

As with linear gradients, all you need to create a radial gradient are two colors. By default, the center of the gradient is at the 50% 50% mark, and the gradient is elliptical matching the aspect ratio of it's box:

```html hidden
<div class="simple-radial"></div>
```

```css hidden
div {
  width: 240px;
  height: 120px;
}
```

```css
.simple-radial {
  background: radial-gradient(red, blue);
}
```

{{ EmbedLiveSample('A_basic_radial_gradient', 120, 120) }}

### Positioning radial color stops

Again like linear gradients, you can position each radial color stop with a percentage or absolute length.

```html hidden
<div class="radial-gradient"></div>
```

```css hidden
div {
  width: 120px;
  height: 120px;
}
```

```css
.radial-gradient {
  background: radial-gradient(red 10px, yellow 30%, #1e90ff 50%);
}
```

{{ EmbedLiveSample('Positioning_radial_color_stops', 120, 120) }}

### Positioning the center of the gradient

You can position the center of the gradient with keyterms, percentage, or absolute lengths, length and percentage values repeating if only one is present, otherwise in the order of position from the left and position from the top.

```html hidden
<div class="radial-gradient"></div>
```

```css hidden
div {
  width: 120px;
  height: 240px;
}
```

```css
.radial-gradient {
  background: radial-gradient(at 0% 30%, red 10px, yellow 30%, #1e90ff 50%);
}
```

{{ EmbedLiveSample('Positioning_the_center_of_the_gradient', 120, 120) }}

### Sizing radial gradients

Unlike linear gradients, you can specify the size of radial gradients. Possible values include closest-corner, closest-side, farthest-corner, and farthest-side, with farthest-corner being the default.

#### Example: closest-side for ellipses

This example uses the `closest-side` size value, which means the size is set by the distance from the starting point (the center) to the closest side of the enclosing box.

```html hidden
<div class="radial-ellipse-side"></div>
```

```css hidden
div {
  width: 240px;
  height: 100px;
}
```

```css
.radial-ellipse-side {
  background: radial-gradient(
    ellipse closest-side,
    red,
    yellow 10%,
    #1e90ff 50%,
    beige
  );
}
```

{{ EmbedLiveSample('Example_closest-side_for_ellipses', 240, 100) }}

#### Example: farthest-corner for ellipses

This example is similar to the previous one, except that its size is specified as `farthest-corner`, which sets the size of the gradient by the distance from the starting point to the farthest corner of the enclosing box from the starting point.

```html hidden
<div class="radial-ellipse-far"></div>
```

```css hidden
div {
  width: 240px;
  height: 100px;
}
```

```css
.radial-ellipse-far {
  background: radial-gradient(
    ellipse farthest-corner at 90% 90%,
    red,
    yellow 10%,
    #1e90ff 50%,
    beige
  );
}
```

{{ EmbedLiveSample('Example_farthest-corner_for_ellipses', 240, 100) }}

#### Example: closest-side for circles

This example uses `closest-side`, which makes the circle's size to be the distance between the starting point (the center) and the closest side. The circle's radius is the distance between the center of the gradient and the closest edge, which due to the positioning of the 25% from the top and 25% from the bottom, is closest to the bottom, since the height in this case is narrower than the width.

```html hidden
<div class="radial-circle-close"></div>
```

```css hidden
div {
  width: 240px;
  height: 120px;
}
```

```css
.radial-circle-close {
  background: radial-gradient(
    circle closest-side at 25% 75%,
    red,
    yellow 10%,
    #1e90ff 50%,
    beige
  );
}
```

{{ EmbedLiveSample('Example_closest-side_for_circles', 240, 120) }}

### Stacked radial gradients

Just like linear gradients, you can also stack radial gradients. The first specified is on top, the last on the bottom.

```html hidden
<div class="stacked-radial"></div>
```

```css hidden
div {
  width: 200px;
  height: 200px;
}
```

```css
.stacked-radial {
  background:
    radial-gradient(
      circle at 50% 0,
      rgba(255, 0, 0, 0.5),
      rgba(255, 0, 0, 0) 70.71%
    ),
    radial-gradient(
      circle at 6.7% 75%,
      rgba(0, 0, 255, 0.5),
      rgba(0, 0, 255, 0) 70.71%
    ),
    radial-gradient(
        circle at 93.3% 75%,
        rgba(0, 255, 0, 0.5),
        rgba(0, 255, 0, 0) 70.71%
      )
      beige;
  border-radius: 50%;
}
```

{{ EmbedLiveSample('Stacked_radial_gradients', 200, 200) }}

## Using conic gradients

The **`conic-gradient()`** [CSS](/ko/docs/Web/CSS) function creates an image consisting of a gradient with color transitions rotated around a center point (rather than radiating from the center). Example conic gradients include pie charts and color wheels, but they can also be used for creating checker boards and other intersting effects.

The conic-gradient syntax is similar to the radial-gradient syntax, but the color-stops are placed around a gradient arc, the circumference of a circle, rather than on the gradient line emerging from the center of the gradient, and the color-stops are percentages or degrees: absolute lengths are not valid.

In a radial gradient, the colors transition from the center of an ellipse, outward, in all directions. With conic gradients, the colors transition as as if spun around the center of a circle, starting at the top and going clockwise. Similar to radial gradients, you can position the center of the gradient. Similar to linear gradients, you can change the gradient angle.

### A basic conic gradient

As with linear and radial gradients, all you need to create a conic gradient are two colors. By default, the center of the gradient is at the 50% 50% mark, with the start of the gradient facing up:

```html hidden
<div class="simple-conic"></div>
```

```css hidden
div {
  width: 120px;
  height: 120px;
}
```

```css
.simple-conic {
  background: conic-gradient(red, blue);
}
```

{{ EmbedLiveSample('A_basic_conic_gradient', 120, 120) }}

### Positioning the conic center

Like radial gradients, you can position the center of the conic gradient with keyterms, percentage, or absolute lengths, with the keyword "at"

```html hidden
<div class="conic-gradient"></div>
```

```css hidden
div {
  width: 120px;
  height: 120px;
}
```

```css
.conic-gradient {
  background: conic-gradient(at 0% 30%, red 10%, yellow 30%, #1e90ff 50%);
}
```

{{ EmbedLiveSample('Positioning_the_conic_center', 120, 120) }}

### Changing the angle

Like radial gradients, you can position the center of the conic gradient with keyterms, percentage, or absolute lengths, with the keyword "at"

```html hidden
<div class="conic-gradient"></div>
```

```css hidden
div {
  width: 120px;
  height: 120px;
}
```

```css
.conic-gradient {
  background: conic-gradient(
    from 45deg,
    red,
    orange,
    yellow,
    green,
    blue,
    purple
  );
}
```

{{ EmbedLiveSample('Changing_the_angle', 120, 120) }}

## Using repeating gradients

The {{cssxref("linear-gradient")}}, {{cssxref("radial-gradient")}}, and {{cssxref("conic-gradient")}} functions don't support automatically repeated color stops. However, the {{cssxref("repeating-linear-gradient")}}, {{cssxref("repeating-radial-gradient")}}, and {{cssxref("repeating-conic-gradient")}} functions are available to offer this functionality.

The size of the gradient line or arc that repeats is the length between the first color stop value and the last color stop length value. If the first color stop just has a color and no color stop length, the value defaults to 0. If the last color stop has just a color and no color stop length, the value defaults to 100%. If neither is declared, the gradient line is 100% meaning the linear and conic gradients will not repeat and the radial gradient will only repeat if the radius of the gradient is smaller than the length between the center of the gradient and the farthest corner. If the first color stop is declared, and the value is greater than 0, the gradient will repeat, as the size of the line or arc is the difference between the first color stop and last color stop is less than 100% or 360 degrees.

### Repeating linear gradients

This example uses {{cssxref("repeating-linear-gradient")}} to create a gradient that progresses repeatedly in a straight line. The colors get cycled over again as the gradient repeats. In this case the gradient line is 10px long.

```html hidden
<div class="repeating-linear"></div>
```

```css hidden
div {
  width: 120px;
  height: 120px;
}
```

```css
.repeating-linear {
  background: repeating-linear-gradient(
    -45deg,
    red,
    red 5px,
    blue 5px,
    blue 10px
  );
}
```

{{ EmbedLiveSample('Repeating_linear_gradients', 120, 120) }}

### Multiple repeating linear gradients

Similar to regular linear and radial gradients, you can include multiple gradients, one on top of the other. This only makes sense if the gradients are partially transparent allowing subsequent gradients to show through the transparent areas, or if you include different [background-sizes](/ko/docs/Web/CSS/background-size), optionally with different [background-position](/ko/docs/Web/CSS/background-position) property values, for each gradient image. We are using transparency.

In this case the gradient lines are 300px, 230px, and 300px long.

```html hidden
<div class="multi-repeating-linear"></div>
```

```css hidden
div {
  width: 600px;
  height: 400px;
}
```

```css
.multi-repeating-linear {
  background:
    repeating-linear-gradient(
      190deg,
      rgba(255, 0, 0, 0.5) 40px,
      rgba(255, 153, 0, 0.5) 80px,
      rgba(255, 255, 0, 0.5) 120px,
      rgba(0, 255, 0, 0.5) 160px,
      rgba(0, 0, 255, 0.5) 200px,
      rgba(75, 0, 130, 0.5) 240px,
      rgba(238, 130, 238, 0.5) 280px,
      rgba(255, 0, 0, 0.5) 300px
    ),
    repeating-linear-gradient(
      -190deg,
      rgba(255, 0, 0, 0.5) 30px,
      rgba(255, 153, 0, 0.5) 60px,
      rgba(255, 255, 0, 0.5) 90px,
      rgba(0, 255, 0, 0.5) 120px,
      rgba(0, 0, 255, 0.5) 150px,
      rgba(75, 0, 130, 0.5) 180px,
      rgba(238, 130, 238, 0.5) 210px,
      rgba(255, 0, 0, 0.5) 230px
    ),
    repeating-linear-gradient(
      23deg,
      red 50px,
      orange 100px,
      yellow 150px,
      green 200px,
      blue 250px,
      indigo 300px,
      violet 350px,
      red 370px
    );
}
```

{{ EmbedLiveSample('Multiple_repeating_linear_gradients', 600, 400) }}

### Plaid gradient

To create plaid we include several overlapping gradients with transparency. In the first background declaration we listed every color stop separately. The second background property declaration using the multiple position color stop syntax:

```html hidden
<div class="plaid-gradient"></div>
```

```css hidden
div {
  width: 200px;
  height: 200px;
}
```

```css
.plaid-gradient {
  background:
    repeating-linear-gradient(
      90deg,
      transparent,
      transparent 50px,
      rgba(255, 127, 0, 0.25) 50px,
      rgba(255, 127, 0, 0.25) 56px,
      transparent 56px,
      transparent 63px,
      rgba(255, 127, 0, 0.25) 63px,
      rgba(255, 127, 0, 0.25) 69px,
      transparent 69px,
      transparent 116px,
      rgba(255, 206, 0, 0.25) 116px,
      rgba(255, 206, 0, 0.25) 166px
    ),
    repeating-linear-gradient(
      0deg,
      transparent,
      transparent 50px,
      rgba(255, 127, 0, 0.25) 50px,
      rgba(255, 127, 0, 0.25) 56px,
      transparent 56px,
      transparent 63px,
      rgba(255, 127, 0, 0.25) 63px,
      rgba(255, 127, 0, 0.25) 69px,
      transparent 69px,
      transparent 116px,
      rgba(255, 206, 0, 0.25) 116px,
      rgba(255, 206, 0, 0.25) 166px
    ),
    repeating-linear-gradient(
      -45deg,
      transparent,
      transparent 5px,
      rgba(143, 77, 63, 0.25) 5px,
      rgba(143, 77, 63, 0.25) 10px
    ),
    repeating-linear-gradient(
      45deg,
      transparent,
      transparent 5px,
      rgba(143, 77, 63, 0.25) 5px,
      rgba(143, 77, 63, 0.25) 10px
    );

  background:
    repeating-linear-gradient(
      90deg,
      transparent 0 50px,
      rgba(255, 127, 0, 0.25) 50px 56px,
      transparent 56px 63px,
      rgba(255, 127, 0, 0.25) 63px 69px,
      transparent 69px 116px,
      rgba(255, 206, 0, 0.25) 116px 166px
    ),
    repeating-linear-gradient(
      0deg,
      transparent 0 50px,
      rgba(255, 127, 0, 0.25) 50px 56px,
      transparent 56px 63px,
      rgba(255, 127, 0, 0.25) 63px 69px,
      transparent 69px 116px,
      rgba(255, 206, 0, 0.25) 116px 166px
    ),
    repeating-linear-gradient(
      -45deg,
      transparent 0 5px,
      rgba(143, 77, 63, 0.25) 5px 10px
    ),
    repeating-linear-gradient(
      45deg,
      transparent 0 5px,
      rgba(143, 77, 63, 0.25) 5px 10px
    );
}
```

{{ EmbedLiveSample('Plaid_gradient', 200, 200) }}

### Repeating radial gradients

This example uses {{cssxref("repeating-radial-gradient")}} to create a gradient that radiates repeatedly from a central point. The colors get cycled over and over as the gradient repeats.

```html hidden
<div class="repeating-radial"></div>
```

```css hidden
div {
  width: 120px;
  height: 120px;
}
```

```css
.repeating-radial {
  background: repeating-radial-gradient(
    black,
    black 5px,
    white 5px,
    white 10px
  );
}
```

{{ EmbedLiveSample('Repeating_radial_gradients', 120, 120) }}

### Multiple repeating radial gradients

```html hidden
<div class="multi-target"></div>
```

```css hidden
div {
  width: 250px;
  height: 150px;
}
```

```css
.multi-target {
  background:
    repeating-radial-gradient(
        ellipse at 80% 50%,
        rgba(0, 0, 0, 0.5),
        rgba(0, 0, 0, 0.5) 15px,
        rgba(255, 255, 255, 0.5) 15px,
        rgba(255, 255, 255, 0.5) 30px
      )
      top left no-repeat,
    repeating-radial-gradient(
        ellipse at 20% 50%,
        rgba(0, 0, 0, 0.5),
        rgba(0, 0, 0, 0.5) 10px,
        rgba(255, 255, 255, 0.5) 10px,
        rgba(255, 255, 255, 0.5) 20px
      )
      top left no-repeat yellow;
  background-size:
    200px 200px,
    150px 150px;
}
```

{{ EmbedLiveSample('Multiple_repeating_radial_gradients', 250, 150) }}

## 같이 보기

- Gradient functions: {{cssxref("linear-gradient")}}, {{cssxref("radial-gradient")}}, {{cssxref("conic-gradient")}}, {{cssxref("repeating-linear-gradient")}}, {{cssxref("repeating-radial-gradient")}}, {{cssxref("repeating-conic-gradient")}}
- Gradient-related CSS data types: {{cssxref("&lt;gradient&gt;")}}, {{cssxref("&lt;image&gt;")}}
- Gradient-related CSS properties: {{cssxref("background")}}, {{cssxref("background-image")}}
- [CSS Gradients Patterns Gallery, by Lea Verou](http://lea.verou.me/css3patterns/)
- [CSS3 Gradients Library, by Estelle Weyl](http://standardista.com/cssgradients)
- [Gradient CSS Generator](https://cssgenerator.org/gradient-css-generator.html)

---
# Source: Web_API_Web_Storage_API_Using_the_Web_Storage_API.md
---
---
title: Web Storage API 사용하기
slug: Web/API/Web_Storage_API/Using_the_Web_Storage_API
---

{{DefaultAPISidebar("Web Storage API")}}

Web Storage API는 브라우저에서 쿠키를 사용하는 것보다 훨씬 직관적으로 key/value 데이터를 안전하게 저장할 수 있는 메커니즘을 제공합니다.

이 글은 본 기술을 어떻게 사용하는지 설명합니다.

## 기본 컨셉

Storage 객체는 단순한 key-value 저장소이며, 이는 객체와 비슷합니다. 하지만 이 데이터들은 페이지 로딩에도 온전하게 유지됩니다. key와 그 value는 항상 문자열입니다. (만약 정수로 키를 사용할 경우 이는 자동으로 string으로 변경됩니다, JavaScript 객체의 동작방식을 생각해보세요) 객체를 사용하듯이 쉽게 값에 접근할 수 있으며, 이 때 {{domxref("Storage.getItem()")}}과 {{domxref("Storage.setItem()")}} 메서드를 사용할 수 있습니다. 아래 세 줄은 (동일한) colorSetting 엔트리에 값을 설정하는 방법입니다.

<pre style="white-space: pre;">localStorage.colorSetting = '#a4509b';
localStorage['colorSetting'] = '#a4509b';
localStorage.setItem('colorSetting', '#a4509b');
</pre>

> **참고:** 일반 객체를 key-value 저장소로 사용할 때 [pitfalls](http://www.2ality.com/2012/01/objects-as-maps.html)과 관련된 사항을 막기 위해 Web Storage API(`setItem`, `getItem`, `removeItem`, `key`, `length`)를 사용하는 걸 권장합니다.

Web Storage는 두 메커니즘을 가지고 있습니다.

- `sessionStorage` 는 페이지의 세션이 유지되는 동안 사용할 수 있는 각 origin별로 별도의 스토리지를 관리합니다. (페이지 리로딩 및 복원을 포함한, 브라우저가 열려있는 한 최대한 긴 시간 동안)
- `localStorage` 도 같은 일을 하지만, 브라우저가 닫히거나 다시 열리더라도 유지합니다.

이 메커니즘들은 {{domxref("Window.sessionStorage")}}와 {{domxref("Window.localStorage")}} 속성(좀 더 정확히 말하자면, 지원하는 브라우저에서 `Window` 객체는 `localStorage` 및 `sessionStorage` 속성 사용이 중단되는 `WindowLocalStorage`과 `WindowSessionStorage`로 구현됩니다)으로 사용 가능합니다. 이 중 하나를 호출하면 데이터를 설정, 검색 및 제거할 수 있는 {{domxref("Storage")}} 객체의 인스턴스가 생성됩니다. 각 Storage 객체는 각 origin 별 `sessionStorage` 나 `localStorage`로 사용됩니다. 동작도 제각기 동작합니다.

예를 들면, 문서에서 `localStorage`를 호출하면 {{domxref("Storage")}} 객체를 반환합니다. 문서에서 `sessionStorage`를 호출하면 다른 {{domxref("Storage")}} 객체를 반환합니다. 둘 다 같은 방법으로 조작할 수 있지만, 서로 다릅니다.

## localStorage 기능 지원 감지

localStorage를 사용하려면 먼저 현재 브라우징 세션에서 지원되고 사용 가능한지 확인해야합니다.

### 사용 가능 검사

localStorage를 지원하는 브라우저는 windows 객체에 localStorage라는 property가 존재 합니다. 그러나 여러 가지 이유로 인해 예외가 발생할 수 있습니다. 존재한다 해도 다양한 브라우저가 localStorage를 비활성화하는 설정을 제공하기 때문에 localStorage가 실제로 사용 가능하다는 보장은 없습니다. 따라서 브라우저가 localStorage를 지원한다고 해도 스크립트에서 사용 하지 못 할 수도 있습니다. 예를 들어 Safari 브라우저의 사생활 보호 모드에서 할당량이 0 인 빈 localStorage 개체를 제공하므로 효과적으로 사용할 수 없게 만듭니다. 이때 QuotaExceededError를 얻을 수도 있습니다. 이는 사용가능한 저장공간을 모두 소모 했다는 의미로, localStorage를 사용할 수 없음을 뜻합니다. 이러한 시나리오를 고려하여 사용가능 여부를 검사하여야 합니다.

다음은 localStorage가 지원되고 사용 가능한지 여부를 감지하는 함수입니다.

```js
function storageAvailable(type) {
  var storage;
  try {
    storage = window[type];
    var x = "__storage_test__";
    storage.setItem(x, x);
    storage.removeItem(x);
    return true;
  } catch (e) {
    return (
      e instanceof DOMException &&
      // Firefox를 제외한 모든 브라우저
      (e.code === 22 ||
        // Firefox
        e.code === 1014 ||
        // 코드가 존재하지 않을 수도 있기 떄문에 이름 필드도 확인합니다.
        // Firefox를 제외한 모든 브라우저
        e.name === "QuotaExceededError" ||
        // Firefox
        e.name === "NS_ERROR_DOM_QUOTA_REACHED") &&
      // 이미 저장된 것이있는 경우에만 QuotaExceededError를 확인하십시오.
      storage &&
      storage.length !== 0
    );
  }
}
```

위 함수를 다음과 같이 사용할 수 있습니다.

```js
if (storageAvailable("localStorage")) {
  // 야호! 우리는 localStorage를 사용할 수 있습니다.
} else {
  // 슬픈 소식, localStorage를 사용할 수 없습니다.
}
```

`storageAvailable('sessionStorage')`를 호출하여 sessionStorage 사용 가능 여부도 확인할 수 있습니다.

여기서 [로컬 스토리지 기능이 존재하는지 확인하는 방법에 대한 기록](https://gist.github.com/paulirish/5558557)을 볼 수 있습니다.

## 예제

To illustrate some typical web storage usage, we have created a simple example, imaginatively called **Web Storage Demo**. The [landing page](https://mdn.github.io/dom-examples/web-storage/) provides controls that can be used to customize the color, font, and decorative image:

![](landing.png)다른 색상을 선택하면, 페이지에 바로 적용됩니다. 또한 선택한 값을 `localStorage`에 저장했다면, 페이지를 나갔다가 나중에 다시 들어왔을 떄 이전에 저장한 값을 기억하고 있습니다.

We have also provided an [event output page](https://mdn.github.io/dom-examples/web-storage/event.html) — if you load this page in another tab, then make changes to your choices in the landing page, you'll see the updated storage information outputted as a {{domxref("StorageEvent")}} is fired.

![](event-output.png)

> **참고:** As well as viewing the example pages live using the above links, you can also [check out the source code](https://github.com/mdn/dom-examples/tree/master/web-storage).

### Testing whether your storage has been populated

To start with on [main.js](https://github.com/mdn/dom-examples/blob/master/web-storage/main.js), we will test whether the storage object has already been populated (i.e., the page was previously accessed):

```js
if (!localStorage.getItem("bgcolor")) {
  populateStorage();
} else {
  setStyles();
}
```

The {{domxref("Storage.getItem()")}} method is used to get a data item from storage; in this case, we are testing to see whether the `bgcolor` item exists; if not, we run `populateStorage()` to add the existing customization values to the storage. If there are already values there, we run `setStyles()` to update the page styling with the stored values.

**Note**: You could also use {{domxref("Storage.length")}} to test whether the storage object is empty or not.

### Getting values from storage

As noted above, values can be retrieved from storage using {{domxref("Storage.getItem()")}}. This takes the key of the data item as an argument, and returns the data value. For example:

```js
function setStyles() {
  var currentColor = localStorage.getItem("bgcolor");
  var currentFont = localStorage.getItem("font");
  var currentImage = localStorage.getItem("image");

  document.getElementById("bgcolor").value = currentColor;
  document.getElementById("font").value = currentFont;
  document.getElementById("image").value = currentImage;

  htmlElem.style.backgroundColor = "#" + currentColor;
  pElem.style.fontFamily = currentFont;
  imgElem.setAttribute("src", currentImage);
}
```

Here, the first three lines grab the values from local storage. Next, we set the values displayed in the form elements to those values, so that they keep in sync when you reload the page. Finally, we update the styles/decorative image on the page, so your customization options come up again on reload.

### Setting values in storage

{{domxref("Storage.setItem()")}} is used both to create new data items, and (if the data item already exists) update existing values. This takes two arguments — the key of the data item to create/modify, and the value to store in it.

```js
function populateStorage() {
  localStorage.setItem("bgcolor", document.getElementById("bgcolor").value);
  localStorage.setItem("font", document.getElementById("font").value);
  localStorage.setItem("image", document.getElementById("image").value);

  setStyles();
}
```

The `populateStorage()` function sets three items in local storage — the background color, font, and image path. It then runs the `setStyles()` function to update the page styles, etc.

We've also included an `onchange` handler on each form element so that the data and styling are updated whenever a form value is changed:

```js
bgcolorForm.onchange = populateStorage;
fontForm.onchange = populateStorage;
imageForm.onchange = populateStorage;
```

### Responding to storage changes with the StorageEvent

The {{domxref("StorageEvent")}} is fired whenever a change is made to the {{domxref("Storage")}} object (note that this event is not fired for sessionStorage changes). This won't work on the same page that is making the changes — it is really a way for other pages on the domain using the storage to sync any changes that are made. Pages on other domains can't access the same storage objects.

On the events page (see [events.js](https://github.com/mdn/dom-examples/blob/master/web-storage/event.js)) the only JavaScript is as follows:

```js
window.addEventListener("storage", function (e) {
  document.querySelector(".my-key").textContent = e.key;
  document.querySelector(".my-old").textContent = e.oldValue;
  document.querySelector(".my-new").textContent = e.newValue;
  document.querySelector(".my-url").textContent = e.url;
  document.querySelector(".my-storage").textContent = JSON.stringify(
    e.storageArea,
  );
});
```

Here we add an event listener to the `window` object that fires when the {{domxref("Storage")}} object associated with the current origin is changed. As you can see above, the event object associated with this event has a number of properties containing useful information — the key of the data that changed, the old value before the change, the new value after that change, the URL of the document that changed the storage, and the storage object itself (which we've stringified so you can see its content).

### 데이터 제거하기

웹 스토리지에서는 데이터를 삭제하기 위한 두 가지 간단한 메소드를 제공합니다. 데모에서 사용하지는 않았지만, 간단하게 프로젝트에 추가할 수 있습니다:

- {{domxref("Storage.removeItem()")}}는 — 삭제하고 싶은 데이터의 키 — 한 개의 인자를 받습니다. 그리고 해당 도메인의 저장소 객체에서 데이터를 제거합니다.
- {{domxref("Storage.clear()")}}는 아무 인자도 받지 않습니다. 그리고 해당 도메인의 저장소 객체 전체를 비워버립니다.

## 명세서

{{Specifications}}

## 브라우저 호환성

{{Compat}}

All browsers have varying capacity levels for both localStorage and sessionStorage. Here is a [detailed rundown of all the storage capacities for various browsers](http://dev-test.nemikor.com/web-storage/support-test/).

## See also

- [Web Storage API landing page](/ko/docs/Web/API/Web_Storage_API)

---
# Source: Web_HTML_Element_area.md
---
---
title: <area>
slug: Web/HTML/Element/area
---

{{HTMLSidebar}}

**HTML `<area>` 요소**는 이미지의 핫스팟 영역을 정의하고 {{glossary("hyperlink", "하이퍼링크")}}를 추가할 수 있습니다. {{htmlelement("map")}} 요소 안에서만 사용할 수 있습니다.

{{InteractiveExample("HTML Demo: &lt;area&gt;", "tabbed-taller")}}

```html interactive-example
<map name="infographic">
  <area
    shape="poly"
    coords="129,0,260,95,129,138"
    href="https://developer.mozilla.org/docs/Web/HTTP"
    alt="HTTP" />
  <area
    shape="poly"
    coords="260,96,209,249,130,138"
    href="https://developer.mozilla.org/docs/Web/HTML"
    alt="HTML" />
  <area
    shape="poly"
    coords="209,249,49,249,130,139"
    href="https://developer.mozilla.org/docs/Web/JavaScript"
    alt="JavaScript" />
  <area
    shape="poly"
    coords="48,249,0,96,129,138"
    href="https://developer.mozilla.org/docs/Web/API"
    alt="Web APIs" />
  <area
    shape="poly"
    coords="0,95,128,0,128,137"
    href="https://developer.mozilla.org/docs/Web/CSS"
    alt="CSS" />
</map>
<img
  usemap="#infographic"
  src="/shared-assets/images/examples/mdn-info.png"
  alt="MDN infographic" />
```

```css interactive-example
img {
  display: block;
  margin: 0 auto;
  width: 260px;
  height: 260px;
}
```

<table class="properties">
  <tbody>
    <tr>
      <th scope="row">
        <a href="/ko/docs/Web/Guide/HTML/Content_categories">콘텐츠 카테고리</a>
      </th>
      <td>
        <a href="/ko/docs/Web/Guide/HTML/Content_categories#플로우_콘텐츠"
          >플로우 콘텐츠</a
        >,
        <a href="/ko/docs/Web/Guide/HTML/Content_categories#구문_콘텐츠"
          >구문 콘텐츠</a
        >.
      </td>
    </tr>
    <tr>
      <th scope="row">가능한 콘텐츠</th>
      <td>
        없음. {{glossary("empty element", "빈 요소")}}입니다.
      </td>
    </tr>
    <tr>
      <th scope="row">태그 생략</th>
      <td>여는 태그는 존재해야 하며 닫는 태그는 존재해선 안됩니다.</td>
    </tr>
    <tr>
      <th scope="row">가능한 부모 요소</th>
      <td>
        <a href="/ko/docs/Web/Guide/HTML/Content_categories#구문_콘텐츠"
          >구문 콘텐츠</a
        >를 허용하는 모든 요소. 단, 조상 중 {{htmlelement("map")}} 요소가
        존재해야 합니다.
      </td>
    </tr>
    <tr>
      <th scope="row">암시적 ARIA 역할</th>
      <td>
        <a href="/ko/docs/Web/HTML/Element/area#href"><code>href</code></a> 특성이 존재하면
        <a href='/ko/docs/Web/Accessibility/ARIA/Roles/link_role'><code>link</code></a>, 그 외의 경우
        <a href="https://www.w3.org/TR/html-aria/#dfn-no-corresponding-role"
          >대응하는 역할 없음</a
        >
      </td>
    </tr>
    <tr>
      <th scope="row">가능한 ARIA 역할</th>
      <td>없음</td>
    </tr>
    <tr>
      <th scope="row">DOM 인터페이스</th>
      <td>{{domxref("HTMLAreaElement")}}</td>
    </tr>
  </tbody>
</table>

## 특성

이 요소는 [전역 특성](/ko/docs/Web/HTML/Global_attributes)을 포함합니다.

- `alt`
  - : 이미지를 출력하지 않는 브라우저에서 대신 표시할 대안 텍스트입니다. 텍스트의 내용은 대안 텍스트 없이 이미지만 표시할 때와 동일한 수준의 선택지를 나타낼 수 있어야 합니다. [`href`](/ko/docs/Web/HTML/Element/area#href) 특성이 존재할 경우 필수 사항입니다.

- `coords`
  - : 핫스팟 영역을 지정하는 일련의 좌표입니다. 값의 수와 의미는 `shape` 특성의 값에 따라 달라집니다.
    - `rect`: 좌상단과 우하단을 나타내는 두 개의 x, y 쌍입니다.
    - `circle`: `x,y,r`로서 `x,y`는 원의 중심 좌표이며 `r`은 반지름입니다.
    - `poly`: 다각형의 꼭지점을 나타내는 다수의 x, y 쌍(`x1,y1,x2,y2,x3,y3,...`)입니다.

    값의 단위는 CSS 픽셀입니다.

- `download`

특성이 존재할 경우, 이 하이퍼링크는 리소스 다운로드 용도로 사용하는 것을 의도했음을 나타냅니다. {{htmlelement("a")}}의 [`download`](/ko/docs/Web/HTML/Element/a#download) 특성 설명에서 전체 설명을 볼 수 있습니다.</dl>

- `href`
  - : `<area>` 하이퍼링크의 대상입니다. 유효한 URL이야 합니다. 생략할 경우, 이 `<area>` 요소는 하이퍼링크를 나타내지 않습니다.
- `hreflang`
  - : 연결한 리소스의 언어를 나타냅니다. 가능한 값은 [BCP47](https://www.ietf.org/rfc/bcp/bcp47.txt)에 따릅니다. [`href`](/ko/docs/Web/HTML/Element/area#href) 특성이 존재할 때만 사용하세요.
- `ping`
  - : 하이퍼링크를 따라갈 때, 백그라운드에서 브라우저가 {{HTTPMethod("POST")}} 요청을 본문 `PING`으로 전송할 URL의 목록입니다. 공백으로 구분하며 주로 추적용으로 사용합니다.

- `referrerpolicy` {{experimental_inline}}
  - : A string indicating which referrer to use when fetching the resource:
    - `"no-referrer"` meaning that the `Referer:` header will not be sent.
    - "`no-referrer-when-downgrade`" meaning that no `Referer:` header will be sent when navigating to an origin without TLS (HTTPS). This is a user agent's default behavior, if no policy is otherwise specified.
    - `"origin"` meaning that the referrer will be the origin of the page, that is roughly the scheme, the host and the port.
    - "origin-when-cross-origin" meaning that navigations to other origins will be limited to the scheme, the host and the port, while navigations on the same origin will include the referrer's path.
    - `"unsafe-url"` meaning that the referrer will include the origin and the path (but not the fragment, password, or username). This case is unsafe because it can leak origins and paths from TLS-protected resources to insecure origins.

- `rel`
  - : For anchors containing the **href** attribute, this attribute specifies the relationship of the target object to the link object. The value is a comma-separated list of [link types values](/ko/docs/Web/HTML/Link_types). The values and their semantics will be registered by some authority that might have meaning to the document author. The default relationship, if no other is given, is void. Use this attribute only if the **href** attribute is present.
- `shape`
  - : 관련된 핫 스폿의 모양. The specifications for HTML 5 and HTML 4 define the values `rect`, which defines a rectangular region; `circle`, which defines a circular region; `poly`, which defines a polygon; and `default`, which indicates the entire region beyond any defined shapes. Many browsers, notably Internet Explorer 4 and higher, support `circ`, `polygon`, and `rectangle` as valid values for **shape**; these values are {{Non-standard_inline}}.

- `target`
  - : 이 속성은 링크된 리소스가 어디에 표시될지 지정합니다. HTML4에서 이것은 프레임의 이름이나 키워드가 될수 있습니다. HTML5에서는, 브라우징 컨텍스트(탭,윈도우,인라인 프레임)의 이름이나 키워드가 될수 있습니다. 다음 키워드들은 특별한 의미를 가지고 있습니다.
    - `_self`: 결과를 현재 HTML4 프레임 또는 HTML5 브라우징 컨텍스트에 로드합니다. 이 target 속성이 정의되어있지 않은경우 이 값이 기본값이 됩니다.
    - `_blank`: 결과를 이름없는 새로운 HTML4 윈도우나 HTML5 브라우징 컨텍스트에 로드합니다.
    - `_parent`: 결과를 현재 HTML4 프레임의 부모 프레임셋에 로드하거나 부모 HTML5 브라우징 컨텍스트에 로드합니다. 만약 부모가 없을 경우 \_self와 동일하게 여겨집니다.
    - `_top`: HTML4에서는, 다른 모든 프레임을 취소하고 결과를 꽉찬 본래의 윈도우에 로드합니다. HTML5에서는, 결과를 최상위 브라우징 컨텍스트에 로드합니다. 만약 부모가 없다면, 이 옵션은 \_self와 같이 행동합니다.

    이 속성은 **href** 속성이 존재할떄만 사용합니다.

### Deprecated attributes

- `name` {{deprecated_inline}}

Define a names for the clickable area so that it can be scripted by older browsers.

- `nohref` {{deprecated_inline}}

Indicates that no hyperlink exists for the associated area.

> **Note:** Since HTML5, omitting the `href` attribute is sufficient.

- `tabindex` {{deprecated_inline}}

A numeric value specifying the position of the defined area in the browser tabbing order. This attribute is global in HTML5.

- `type` {{deprecated_inline}}

No effect. Browsers ignore it. (The W3C 5.3 fork of the HTML specification defines it as valid, but [the canonical HTML specification](https://html.spec.whatwg.org/multipage/#the-area-element) doesn't, and it has no effect in any user agents.)

## 예제

```html
<map name="primary">
  <area shape="circle" coords="200,250,25" href="another.htm" />
  <area shape="default" nohref />
</map>
<img usemap="#primary" src="http://placehold.it/350x150" alt="350 x 150 pic" />
```

### 결과

{{EmbedLiveSample('예제', 360, 160)}}

## 명세

{{Specifications}}

## 브라우저 호환성

{{Compat}}

---
# Source: Web_CSS_CSS_colors_Applying_color.md
---
---
title: CSS로 HTML 요소에 색 입히기
slug: Web/CSS/CSS_colors/Applying_color
---

{{HTMLSidebar}}

색은 인간의 감정을 표현하는 기본적인 형태입니다. 아이들은 뭔가 그릴 수 있는 민첩성을 갖추기도 전에 색을 가지고 놉니다. 사람들이 웹 사이트를 개발할 때 보통 색을 제일 먼저 입혀보고 싶어 하는 건 이런 이유일지도 모릅니다. [CSS](/ko/docs/Web/CSS)와 함께라면 무궁무진한 방법으로 여러분의 [HTML](/ko/docs/Web/HTML) [요소](/ko/docs/Web/HTML/Element)에 색을 넣어 원하는 모습을 만들 수 있습니다. 이 글은 CSS 색을 HTML에 적용하는 기초를 소개합니다.

다행히도 HTML에 색을 추가하는 건 정말 쉽고 거의 모든 곳에 할 수 있는 일입니다.

[색을 입힐 수 있는 목록, 그때 사용할 CSS 속성](#색을_입힐_수_있는_것), [색을 나타내는 법](#색을_나타내는_법), [실제로 색 사용하기](#색_사용하기) 등 색을 쓸 때 알아야 할 주제는 대부분 짚고 가겠습니다. [사용자가 색을 선택](#사용자의_색_선택)할 수 있는 방법도 확인해보겠습니다.

마지막으로는 적절한 색을 고르고, 서로 다른 시각적 조건을 가진 사람들을 고려하는 등 [현명한 색 선택](#현명하게_색_고르기)에 대해 간단히 알아보겠습니다.

## 색을 입힐 수 있는 것

요소 차원에서 보자면 HTML의 모든 것에 색을 입힐 수 있습니다. 대신에 글씨와 테두리처럼, 요소 안에 그려지는 것의 종류에 따라 알아보겠습니다. 각각의 종류에 적용할 수 있는 CSS 속성의 목록도 보겠습니다.

가장 기초적인 단계로는 {{cssxref("color")}} 속성이 HTML 요소의 콘텐츠 전경색을 지정하고, {{cssxref("background-color")}} 속성이 요소의 배경색을 지정합니다. 두 속성은 거의 모든 요소에 사용할 수 있습니다.

### 글씨

요소를 렌더링할 때 글씨, 글씨 배경과 기타 꾸미기 효과의 색은 아래에 나열한 속성이 결정합니다.

- {{cssxref("color")}}
  - : 글씨와 글씨 장식(밑줄, 윗줄, 취소선 등)을 그릴 때 사용할 색입니다.
- {{cssxref("background-color")}}
  - : 글씨의 배경색입니다.
- {{cssxref("text-shadow")}}
  - : 글씨의 그림자 효과를 설정합니다. 여러 옵션 중에서 그림자 색을 정할 수 있습니다. (이후 다른 옵션에 따라 흐려지고 배경과 섞입니다)

    See [Text drop shadows](/ko/docs/Learn/CSS/Styling_text/Fundamentals#text_drop_shadows) to learn more.

- {{cssxref("text-decoration-color")}}
  - : 기본 설정에서 글씨 장식(밑줄, 윗줄, 취소선 등)은 `color` 속성의 값을 색으로 사용합니다. 그러나 `text-decoration-color` 속성을 지정하면 다른 색으로 바꿀 수 있습니다.
- {{cssxref("text-emphasis-color")}}
  - : 글씨 위에 표시할 강조 표시의 색입니다.
- {{cssxref("caret-color")}}
  - : 요소의 {{Glossary("caret", "캐럿")}}(글씨 입력 커서) 색입니다. {{HTMLElement("input")}}이나 {{HTMLElement("textarea")}}, HTML [`contenteditable`](/ko/docs/Web/HTML/Global_attributes#contenteditable) 속성을 설정한 요소처럼 편집 가능한 경우에만 유용합니다.

### 박스

모든 요소는 모종의 콘텐츠를 가진 박스로, 콘텐츠 외에도 배경과 테두리를 가질 수 있습니다.

- [테두리](#테두리)
  - [: 테두리](#테두리) 항목에서 박스 테두리에 사용할 수 있는 CSS 속성의 목록을 확인하세요.
- {{cssxref("background-color")}}
  - : 전경 콘텐츠가 없는 곳에 표시할 배경색입니다.
- {{cssxref("column-rule-color")}}
  - : 긴 글씨를 여러 단으로 나눌 때 그릴 구분선의 색입니다.
- {{cssxref("outline-color")}}
  - : 요소의 바깥에 외곽선을 그릴 때 사용할 색입니다. 외곽선은 문서에서 공간을 차지하지 않아서 다른 요소를 가릴 수 있다는 점에서 테두리와 다릅니다. 보통 현재 선택돼 입력 이벤트를 받을 수 있는 요소를 강조할 때 사용합니다.

### 테두리

모든 요소는 주위에 테두리를 가질 수 있습니다. 기본적인 테두리는 요소 콘텐츠의 모서리를 따라 그리는 선입니다. See [Box properties](/ko/docs/Learn/CSS/Introduction_to_CSS/Box_model#box_properties) to learn about the relationship between elements and their borders, and the article [Styling borders using CSS](/ko/docs/Learn/CSS/Building_blocks/Backgrounds_and_borders) to learn more about applying styles to borders.

{{cssxref("border")}} 단축 속성을 사용하면 색은 물론 [너비](/ko/docs/Web/CSS/border-width)와 [스타일](/ko/docs/Web/CSS/border-style)(실선, 점선 등)같은 속성을 한 번에 설정할 수 있습니다.

- {{cssxref("border-color")}}
  - : 모든 면의 테두리가 사용할 단색입니다.
- {{cssxref("border-left-color")}}, {{cssxref("border-right-color")}}, {{cssxref("border-top-color")}}, {{cssxref("border-bottom-color")}}
  - : 테두리 색을 방향에 따라 다르게 설정할 수 있습니다.
- {{cssxref("border-block-start-color")}}, {{cssxref("border-block-end-color")}}
  - : With these, you can set the color used to draw the borders which are closest to the start and end of the block the border surrounds. In a left-to-right writing mode (such as the way English is written), the block start border is the top edge and the block end is the bottom. This differs from the inline start and end, which are the left and right edges (corresponding to where each line of text in the box begins and ends).
- {{cssxref("border-inline-start-color")}}, {{cssxref("border-inline-end-color")}}
  - : These let you color the edges of the border closest to to the beginning and the end of the start of lines of text within the box. Which side this is will vary depending on the {{cssxref("writing-mode")}}, {{cssxref("direction")}}, and {{cssxref("text-orientation")}} properties, which are typically (but not always) used to adjust text directionality based on the language being displayed. For example, if the box's text is being rendered right-to-left, then the `border-inline-start-color` is applied to the right side of the border.

### 다른 방법

웹 기술에서 CSS만 색을 지원하는건 아닙니다. 웹에서 사용할 수 있는 다른 그래픽 기술에서도 색을 지원합니다.

- HTML [Canvas API](/ko/docs/Web/API/Canvas_API)
  - : {{HTMLElement("canvas")}} 요소로 2D 비트맵 그래픽을 그릴 수 있습니다. [캔버스 자습서](/ko/docs/Web/API/Canvas_API/Tutorial)를 방문해 더 알아보세요.
- [SVG](/ko/docs/Web/SVG) (Scalable Vector Graphics)
  - : 선, 패턴, 특정 모양의 형태를 그리는 명령어를 사용해 이미지를 그릴 수 있습니다. SVG 명령어는 XML 형식을 따르며, 웹 페이지에 바로 삽입할 수도 있고, 다른 이미지처럼 {{HTMLElement("img")}} 요소에 넣을 수도 있습니다.
- [WebGL](/ko/docs/Web/API/WebGL_API)
  - : Web Graphics Library는 OpenGL ES 기반의 API로, 웹에서 고성능 2D 및 3D 그래픽을 그릴 수 있습니다. [WebGL 자습서](/ko/docs/Web/API/WebGL_API/Tutorial/Getting_started_with_WebGL)를 방문해 더 알아보세요.

## 색을 나타내는 법

CSS에서 색을 나타내려면 우선 "색"이라는 개념을, 원색이나 밝기 등 구성 요소를 분리해 수치로 표기하는 등 컴퓨터가 이해할 수 있는 디지털 형태로 변환해야 합니다. 변환 방법이 여러 가지이듯 CSS가 색을 표현하는 방법도 여러 가지입니다.

각각의 형태에 대한 더 자세한 내용은 CSS {{cssxref("&lt;color&gt;")}} 단위 문서를 참고하세요.

### 키워드

CSS 표준은 다수의 색 키워드를 사전에 정의하고 있으므로, 원하는 색을 가리키는 키워드가 있다면 숫자형 표현 대신 사용할 수 있습니다. 색 키워드는 원색과 2차색(`red`, `blue`, `orange` 등), 단계별 무채색(`black`에서 `white`까지, `darkgray`와 `lightgrey` 등) 외에도 `lightseagreen`, `cornflowerblue`, `rebeccapurple`처럼 다양한 종류의 혼합색을 포함하고 있습니다.

사용할 수 있는 모든 색 키워드의 목록은 [`<color>`의 색상 키워드 항목](/ko/docs/Web/CSS/color_value#%EC%83%89%EC%83%81_%ED%82%A4%EC%9B%8C%EB%93%9C)을 참고하세요.

### RGB 값

RGB 색은 세 가지 방법으로 표현할 수 있습니다.

#### 16진수 문자열 표기법

16진수 문자열 표기법은 색의 구성요소(빨강, 초록, 파랑)를 16진수 숫자로 표현합니다. 네 번째 구성 요소로 알파 채널(불투명도)을 포함할 수도 있습니다. 하나의 구성 요소는 0에서 255 사이(0x00에서 0xFF)를 숫자 두 개로, 또는 0에서 15 사이(0x0에서 0xF)를 숫자 한 개로 표기합니다. 단, 모든 구성 요소는 같은 수의 문자로 표기해야 합니다. 한 자릿수(0\~F)로 표기한다면, 구성 요소의 최종 값은 자신의 문자를 두 번씩 사용해 계산합니다. 즉, `"#D"`의 값은 `"#DD"`입니다.

16진수 문자열 표기법은 항상 `"#"`으로 시작해야 하고, 16진수 숫자는 그 후에 위치합니다. 문자열은 대소문자를 구분하지 않습니다.

- `"#rrggbb"`
  - : 완전히 불투명한 색을 지정합니다. 구성 요소 중 빨강은 16진수 `0xrr`, 초록은 `0xgg`, 파랑은 `0xbb`입니다.
- `"#rrggbbaa"`
  - : 구성 요소 중 빨강은 16진수 `0xrr`, 초록은 `0xgg`, 파랑은 `0xbb`인 색을 지정합니다. 알파 채널의 값은 `0xaa`로, 값이 낮을 수록 색은 더 투명해집니다.
- `"#rgb"`
  - : 완전히 불투명한 색을 지정합니다. 구성 요소 중 빨강은 16진수 `0xrr`, 초록은 `0xgg`, 파랑은 `0xbb`입니다.
- `"#rgba"`
  - : 구성 요소 중 빨강은 16진수 `0xrr`, 초록은 `0xgg`, 파랑은 `0xbb`인 색을 지정합니다. 알파 채널의 값은 `0xaa`로, 값이 낮을 수록 색은 더 투명해집니다.

예를 하나 들자면 불투명한 파랑은 `"#0000ff"`이나 `"#00f"`로 표현할 수 있습니다. 25%만 불투명한 파랑으로 만들 땐 `"#0000ff44"` 또는 `"#00f4"`로 표기합니다.

#### RGB 함수형 표기법

16진수 문자열 표기법과 같이, RGB(Red/Green/Blue) 함수 표기법은 빨강, 초록, 파랑, 그리고 불투명도를 나타낼 선택적 알파 채널 구성요소를 사용해 색을 나타냅니다. 그러나 문자열 표기법과 달리 CSS 함수 {{cssxref("color_value", "rgb()", "#rgb()")}}를 사용합니다. `rgb()` 함수의 세 매개변수는 순서대로 빨강, 파랑, 초록 값이며, 생략 가능한 마지막 네 번째 매개변수가 알파 채널을 나타냅니다.

각 매개변수의 유효한 값은 다음과 같습니다.

- `red`, `green`, `blue`
  - : 각각 0 이상, 255 이하인 {{cssxref("&lt;integer&gt;")}}이거나, 또는 0% 이상 100% 이하인 {{cssxref("&lt;percentage&gt;")}}여야 합니다.
- `alpha`
  - : 0.0(완전히 투명) 이상, 1.0(완전히 불투명) 이하의 숫자여야 합니다. 백분율도 사용할 수 있으며, 0%는 0.0, 100%는 1.0에 대응합니다.

예를 들어, 50% 불투명도의 밝은 빨강은 `rgb(255, 0, 0, 0.5)`와 `rgb(100%, 0, 0, 50%)` 두 방법으로 만들 수 있습니다.

### HSL 함수형 표기법

많은 경우, 디자이너와 아티스트는 HSL(색조/채도/명도) 모델을 사용한 색을 선호합니다. 웹에서 HSL 색상은 HSL 함수 표기법을 사용해 나타냅니다. CSS `hsl()` 함수의 사용법 자체는 `rgb()` 함수와 매우 유사합니다.

The diagram below shows an HSL color cylinder. Hue defines the actual color based on the position along a circular {{glossary("color wheel")}} representing the colors of the visible spectrum. Saturation is a percentage of how much of the way between being a shade of gray and having the maximum possible amount of the given hue. As the value of luminance (or lightness) increases, the color transitions from the darkest possible to the brightest possible (from black to white). Image courtesy of user [SharkD](https://commons.wikimedia.org/wiki/User:SharkD) on [Wikipedia](https://www.wikipedia.org/), distributed under the [CC BY-SA 3.0](https://creativecommons.org/licenses/by-sa/3.0/) license.

![HSL color cylinder](640px-hsl_color_solid_cylinder.png)

The value of the hue (H) component of an HSL color is an angle from red around through yellow, green, cyan, blue, and magenta (ending up back at red again at 360°) that identifies what the base color is. The value can be specified in any {{cssxref("&lt;angle&gt;")}} unit supported by CSS, including degrees (`deg`), radians (`rad`), gradians (`grad`), or turns (`turn`). But this doesn't control how vivid or dull, or how bright or dark the color is.

The saturation (S) component of the color specifies what percentage of the final color is comprised of the specified hue. The rest is defined by the grey level provided by the luminance (L) component.

Think of it like creating the perfect paint color:

1. You start with base paint that's the maximum intensity possible for a given color, such as the most intense blue that can be represented by the user's screen. This is the **hue** (H) component: a value representing the angle around the {{glossary("color wheel")}} for the vivid hue we want to use as our base.
2. Then select a greyscale paint that corresponds how bright you want the color to be; this is the luminance. Do you want it to be very bright and nearly white, or very dark and closer to black, or somewhere in between? This is specified using a percentage, where 0% is perfectly black and 100% is perfectly white (regardless of the saturation or hue). In between values are a literal grey area.
3. Now that you have a grey paint and a perfectly vivid color, you need to mix them together. The saturation (S) component of the color indicates what percentage of the final color should be comprised of that perfectly vivid color. The rest of the final color is made up of the grey paint that represents the saturation.

You can also optionally include an alpha channel, to make the color less than 100% opaque.

Here are some sample colors in HSL notation:

```css hidden
table {
  border: 1px solid black;
  font:
    16px "Open Sans",
    Helvetica,
    Arial,
    sans-serif;
  border-spacing: 0;
  border-collapse: collapse;
}

th,
td {
  border: 1px solid black;
  padding: 4px 6px;
  text-align: left;
}

th {
  background-color: hsl(0, 0%, 75%);
}
```

```html
<table>
  <thead>
    <tr>
      <th scope="col">Color in HSL notation</th>
      <th scope="col">Example</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><code>hsl(90deg, 100%, 50%)</code></td>
      <td style="background-color: hsl(90deg, 100%, 50%);">&nbsp;</td>
    </tr>
    <tr>
      <td><code>hsl(90, 100%, 50%)</code></td>
      <td style="background-color: hsl(90, 100%, 50%);">&nbsp;</td>
    </tr>
    <tr>
      <td><code>hsl(0.15turn, 50%, 75%)</code></td>
      <td style="background-color: hsl(0.15turn, 50%, 75%);">&nbsp;</td>
    </tr>
    <tr>
      <td><code>hsl(0.15turn, 90%, 75%)</code></td>
      <td style="background-color: hsl(0.15turn, 90%, 75%);">&nbsp;</td>
    </tr>
    <tr>
      <td><code>hsl(0.15turn, 90%, 50%)</code></td>
      <td style="background-color: hsl(0.15turn, 90%, 50%);">&nbsp;</td>
    </tr>
    <tr>
      <td><code>hsl(270deg, 90%, 50%)</code></td>
      <td style="background-color: hsl(270deg, 90%, 50%);">&nbsp;</td>
    </tr>
  </tbody>
</table>
```

{{EmbedLiveSample("HSL_functional_notation", 300, 260)}}

> **Note:** When you omit the hue's unit, it's assumed to be in degrees (`deg`).

### HWB functional notation

Much like the HSL functional notation above, the [hwb()](/ko/docs/Web/CSS/color_value/hwb) function uses the same hue value. But instead of lightness and saturation you specify whiteness and blackness values in percentages. Values are **not** separated with a comma and an optional alpha value can be included (it must be preceded by a forward slash `/`).

Here are some examples of using HWB notation:

```css
/* These examples all specify varying shades of a lime green. */
hwb(90 10% 10%)
hwb(90 10% 10%)
hwb(90 50% 10%)
hwb(90deg 10% 10%)
hwb(1.5708rad 60% 0%)
hwb(.25turn 0% 40%)

/* Same lime green but with an alpha value */
hwb(90 10% 10% / 0.5)
hwb(90 10% 10% / 50%)
```

## Using color

Now that you know what CSS properties exist that let you apply color to elements and the formats you can use to describe colors, you can put this together to begin to make use of color. As you may have seen from the list under [Things that can have color](#things_that_can_have_color), there are plenty of things you can color with CSS. Let's look at this from two sides: using color within a {{Glossary("stylesheet")}}, and adding and changing color using {{Glossary("JavaScript")}} code to alter the styles of elements.

### Specifying colors in stylesheets

The easiest way to apply color to elements—and the way you'll usually do it—is to specify colors in the CSS that's used when rendering elements. While we won't use every single property mentioned previously, we'll look at a couple of examples. The concept is the same anywhere you use color.

Let's take a look at an example, starting by looking at the results we're trying to achieve:

{{EmbedLiveSample("Specifying_colors_in_stylesheets", 650, 150)}}

#### HTML

The HTML responsible for creating the above example is shown here:

```html
<div class="wrapper">
  <div class="box boxLeft">
    <p>This is the first box.</p>
  </div>
  <div class="box boxRight">
    <p>This is the second box.</p>
  </div>
</div>
```

This is pretty simple, using a {{HTMLElement("div")}} as a wrapper around the contents, which consists of two more `<div>`s, each styled differently with a single paragraph ({{HTMLElement("p")}}) in each box.

The magic happens, as usual, in the CSS, where we'll apply colors define the layout for the HTML above.

#### CSS

We'll look at the CSS to create the above results a piece at a time, so we can review the interesting parts one by one.

```css
.wrapper {
  width: 620px;
  height: 110px;
  margin: 0;
  padding: 10px;
  border: 6px solid mediumturquoise;
}
```

The `.wrapper` class is used to assign styles to the {{HTMLElement("div")}} that encloses all of our other content. This establishes the size of the container using {{cssxref("width")}} and {{cssxref("height")}} as well as its {{cssxref("margin")}} and {{cssxref("padding")}}.

Of more interest to our discussion here is the use of the {{cssxref("border")}} property to establish a border around the outside edge of the element. This border is a solid line, 6 pixels wide, in the color `mediumturquoise`.

Our two colored boxes share a number of properties in common, so next we establish a class, `.box`, that defines those shared properties:

```css
.box {
  width: 290px;
  height: 100px;
  margin: 0;
  padding: 4px 6px;
  font:
    28px "Marker Felt",
    "Zapfino",
    cursive;
  display: flex;
  justify-content: center;
  align-items: center;
}
```

In brief, `.box` establishes the size of each box, as well as the configuration of the font used within. We also take advantage of [CSS Flexbox](/ko/docs/Web/CSS/CSS_Flexible_Box_Layout) to easily center the contents of each box. We enable `flex` mode using {{cssxref("display", "display: flex")}}, and set both {{cssxref("justify-content")}} and {{cssxref("align-items")}} to `center`. Then we can create a class for each of the two boxes that defines the properties that differ between the two.

```css
.boxLeft {
  float: left;
  background-color: rgb(245, 130, 130);
  outline: 2px solid darkred;
}
```

The `.boxLeft` class—which, cleverly, is used to style the box on the left—floats the box to the left, then sets up the colors:

- The box's background color is set by changing the value of the CSS {{cssxref("background-color")}} property to `rgb(245, 130, 130)`.
- An outline is defined for the box. Unlike the more commonly used `border`, {{cssxref("outline")}} doesn't affect layout at all; it draws over the top of whatever may happen to be outside the element's box instead of making room as `border` does. This outline is a solid, dark red line that's two pixels thick. Note the use of the `darkred` keyword when specifying the color.
- Notice that we're not explicitly setting the text color. That means the value of {{cssxref("color")}} will be inherited from the nearest containing element that defines it. By default, that's black.

```css
.boxRight {
  float: right;
  background-color: hsl(270deg, 50%, 75%);
  outline: 4px dashed rgb(110, 20, 120);
  color: hsl(0deg, 100%, 100%);
  text-decoration: underline wavy #88ff88;
  text-shadow: 2px 2px 3px black;
}
```

> **Note:** When you try to show it in Safari, it will not show properly. Because Safari doesn't support `text-decoration: underline wavy #88ff88`.

Finally, the `.boxRight` class describes the unique properties of the box that's drawn on the right. It's configured to float the box to the right so that it appears next to the previous box. Then the following colors are established:

- The `background-color` is set using the HSL value specified using `hsl(270deg, 50%, 75%)`. This is a medium purple color.
- The box's `outline` is used to specify that the box should be enclosed in a four pixel thick dashed line whose color is a somewhat deeper purple (`rgb(110, 20, 120)`).
- The foreground (text) color is specified by setting the {{cssxref("color")}} property to `hsl(0deg, 100%, 100%)`. This is one of many ways to specify the color white.
- We add a green wavy line under the text with {{cssxref("text-decoration")}}.
- Finally, a bit of a shadow is added to the text using {{cssxref("text-shadow")}}. Its `color` parameter is set to `black`.

## Letting the user pick a color

There are many situations in which your website may need to let the user select a color. Perhaps you have a customizable user interface, or you're implementing a drawing app. Maybe you have editable text and need to let the user choose the text color. Or perhaps your app lets the user assign colors to folders or items. Although historically it's been necessary to implement your own [color picker](https://en.wikipedia.org/wiki/Color_picker), HTML now provides support for browsers to provide one for your use through the {{HTMLElement("input")}} element, by using `"color"` as the value of its [`type`](/ko/docs/Web/HTML/Element/input#type) attribute.

The `<input>` element represents a color only in the [hexadecimal string notation](#hexadecimal_string_notation) covered above.

### Example: Picking a color

Let's look at a simple example, in which the user can choose a color. As the user adjusts the color, the border around the example changes to reflect the new color. After finishing up and picking the final color, the color picker's value is displayed.

{{EmbedLiveSample("Example_Picking_a_color", 525, 275)}}

> **Note:** On macOS, you indicate that you've finalized selection of the color by closing the color picker window.

#### HTML

The HTML here creates a box that contains a color picker control (with a label created using the {{HTMLElement("label")}} element) and an empty paragraph element ({{HTMLElement("p")}}) into which we'll output some text from our JavaScript code.

```html
<div id="box">
  <label for="colorPicker">Border color:</label>
  <input type="color" value="#8888ff" id="colorPicker" />
  <p id="output"></p>
</div>
```

#### CSS

The CSS establishes a size for the box and some basic styling for appearances. The border is also established with a 2-pixel width and a border color.

```css
#box {
  width: 500px;
  height: 200px;
  border: 2px solid rgb(245, 220, 225);
  padding: 4px 6px;
  font:
    16px "Lucida Grande",
    "Helvetica",
    "Arial",
    "sans-serif";
}
```

#### JavaScript

The script here handles the task of updating the starting color of the border to match the color picker's value. Then two event handlers are added to deal with input from the [`<input type="color">`](/ko/docs/Web/HTML/Element/input/color) element.

```js
const colorPicker = document.getElementById("colorPicker");
const box = document.getElementById("box");
const output = document.getElementById("output");

box.style.borderColor = colorPicker.value;

colorPicker.addEventListener(
  "input",
  (event) => {
    box.style.borderColor = event.target.value;
  },
  false,
);

colorPicker.addEventListener(
  "change",
  (event) => {
    output.innerText = `Color set to ${colorPicker.value}.`;
  },
  false,
);
```

The {{domxref("HTMLElement/input_event", "input")}} event is sent every time the value of the element changes; that is, every time the user adjusts the color in the color picker. Each time this event arrives, we set the box's border color to match the color picker's current value.

The {{domxref("HTMLElement/change_event", "change")}} event is received when the color picker's value is finalized. We respond by setting the contents of the `<p>` element with the ID `"output"` to a string describing the finally selected color.

## Using color wisely

Making the right choices when selecting colors when designing a website can be a tricky process, especially if you aren't well-grounded in art, design, or at least basic color theory. The wrong color choice can render your site unattractive, or even worse, leave the content unreadable due to problems with contrast or conflicting colors. Worse still, if using the wrong colors can result in your content being outright unusable by people with certain vision problems, particularly color blindness.

### Finding the right colors

Coming up with just the right colors can be tricky, especially without training in art or design. Fortunately, there are tools available that can help you. While they can't replace having a good designer helping you make these decisions, they can definitely get you started.

#### Base color

The first step is to choose your **base color**. This is the color that in some way defines your website or the subject matter of the site. Just as we associate green with the beverage [Mountain Dew](https://en.wikipedia.org/wiki/Mountain_Dew) and one might think of the color blue in relationship with the sky or the ocean, choosing an appropriate base color to represent your site is a good place to start. There are plenty of ways to select a base color; a few ideas include:

- A color that is naturally associated with the topic of your content, such as the existing color identified with a product or idea or a color representative of the emotion you wish to convey.
- A color that comes from imagery associated with what your content is about. If you're creating a website about a given item or product, choose a color that's physically present on that item.
- Browse websites that let you look at lots of existing color palettes and images to find inspiration.

When trying to decide upon a base color, you may find that browser extensions that let you select colors from web content can be particularly handy. Some of these are even specifically designed to help with this sort of work. For example, the website [ColorZilla](https://www.colorzilla.com/) offers an extension ([Chrome](https://www.colorzilla.com/chrome/) / [Firefox](https://www.colorzilla.com/firefox/)) that offers an eyedropper tool for picking colors from the web. It can also take averages of the colors of pixels in various sized areas or even a selected area of the page.

> **Note:** The advantage to averaging colors can be that often what looks like a solid color is actually a surprisingly varied number of related colors all used in concert, blending to create a desired effect. Picking just one of these pixels can result in getting a color that on its own looks very out of place.

#### Fleshing out the palette

Once you have decided on your base color, there are plenty of online tools that can help you build out a palette of appropriate colors to use along with your base color by applying color theory to your base color to determine appropriate added colors. Many of these tools also support viewing the colors filtered so you can see what they would look like to people with various forms of color blindness. See [Color and accessibility](#color_and_accessibility) for a brief explanation of why this matters.

A few examples (all free to use as of the time this list was last revised):

- [MDN's color picker tool](/ko/docs/Web/CSS/CSS_Colors/Color_picker_tool)
- [Paletton](https://paletton.com/)
- [Adobe Color CC online color wheel](https://color.adobe.com/create/color-wheel)

When designing your palette, be sure to keep in mind that in addition to the colors these tools typically generate, you'll probably also need to add some core neutral colors such as white (or nearly white), black (or nearly black), and some number of shades of gray.

> **Note:** Usually, you are far better off using the smallest number of colors possible. By using color to accentuate rather than adding color to everything on the page, you keep your content easy to read and the colors you do use have far more impact.

### Color theory resources

A full review of color theory is beyond the scope of this article, but there are plenty of articles about color theory available, as well as courses you can find at nearby schools and universities. A couple of useful resources about color theory:

- [Color Science](https://www.khanacademy.org/computing/pixar/color) ([Khan Academy](https://www.khanacademy.org/) in association with [Pixar](https://www.pixar.com/))
  - : An online course which introduces concepts such as what color is, how it's perceived, and how to use colors to express ideas. Presented by Pixar artists and designers.
- [Color theory](https://en.wikipedia.org/wiki/Color_theory) on Wikipedia
  - : Wikipedia's entry on color theory, which has a lot of great information from a technical perspective. It's not really a resource for helping you with the color selection process, but is still full of useful information.

### Color and accessibility

There are several ways color can be an {{Glossary("accessibility")}} problem. Improper or careless use of color can result in a website or app that a percentage of your target audience may not be able to use adequately, resulting in lost traffic, lost business, and possibly even a public relations problem. So it's important to consider your use of color carefully.

You should do at least basic research into [color blindness](https://en.wikipedia.org/wiki/Color_blindness). There are several kinds; the most common is red-green color blindness, which causes people to be unable to differentiate between the colors red and green. There are others, too, ranging from inabilities to tell the difference between certain colors to total inability to see color at all.

> **Note:** The most important rule: never use color as the only way to know something. If, for example, you indicate success or failure of an operation by changing the color of a shape from white to green for success and red for failure, users with red-green color-blindness won't be able to use your site properly. Instead, perhaps use both text and color together, so that everyone can understand what's happening.

For more information about color blindness, see the following articles:

- [Medline Plus: Color Blindness](https://medlineplus.gov/colorblindness.html) (United States National Institute of Health)
- [American Academy of Ophthalmology: What Is Color Blindness?](https://www.aao.org/eye-health/diseases/what-is-color-blindness)
- [Color Blindness & Web Design](https://www.usability.gov/get-involved/blog/2010/02/color-blindness.html) (Usability.gov: United States Department of Health and Human Services)

### Palette design example

Let's consider a quick example of selecting an appropriate color palette for a site. Imagine that you're building a website for a new game that takes place on the planet Mars. So let's do a [Google search for photos of Mars](https://www.google.com/search?q=Mars&tbm=isch). Lots of good examples of Martian coloration there. We carefully avoid the mockups and the photos from movies. And we decide to use a photo taken by one of the Mars landers humanity has parked on the surface over the last few decades, since the game takes place on the planet's surface. We use a color picker tool to select a sample of the color we choose.

Using an eyedropper tool, we identify a color we like and determine that the color in question is `#D79C7A`, which is an appropriate rusty orange-red color that's so stereotypical of the Martian surface.

Having selected our base color, we need to build out our palette. We decide to use [Paletton](https://www.paletton.com/) to come up with the other colors we need. Upon opening Paletton, we see:

![Right after loading Paletton.](paletton1.png)

Next, we enter our color's hex code (`D79C7A`) into the "Base RGB" box at the bottom-left corner of the tool:

![After entering base color](paletton2.png)

We now see a monochromatic palette based on the color we picked from the Mars photo. If you need a lot of related colors for some reason, those are likely to be good ones. But what we really want is an accent color. Something that will pop along side the base color. To find that, we click the "add complementary" toggle underneath the menu that lets you select the palette type (currently "Monochromatic"). Paletton computes an appropriate accent color; clicking on the accent color down in the bottom-right corner tells us that this color is `#508D7C`.

![Now with complementary colors included.](paletton3.png)

If you're unhappy with the color that's proposed to you, you can change the color scheme, to see if you find something you like better. For example, if we don't like the proposed greenish-blue color, we can click the Triad color scheme icon, which presents us with the following:

![Triad color scheme selected](paletton4.png)

That greyish blue in the top-right looks pretty good. Clicking on it, we find that it's `#556E8D`. That would be used as the accent color, to be used sparingly to make things stand out, such as in headlines or in the highlighting of tabs or other indicators on the site:

![Triad color scheme selected](paletton-color-detail.png)

Now we have our base color and our accent. On top of that, we have a few complementary shades of each, just in case we need them for gradients and the like. The colors can then be exported in a number of formats so you can make use of them.

Once you have these colors, you will probably still need to select appropriate neutral colors. Common design practice is to try to find the sweet spot where there's just enough contrast that the text is crisp and readable but not enough contrast to become harsh for the eyes. It's easy to go too far in one way or another so be sure to get feedback on your colors once you've selected them and have examples of them in use available. If the contrast is too low, your text will tend to be washed out by the background, leaving it unreadable, but if your contrast is too high, the user may find your site garish and unpleasant to look at.

### Color, backgrounds, contrast, and printing

What looks good on screen may look very different on paper.
In addition, ink can be expensive, and if a user is printing your page, they don't necessarily need all the backgrounds and such using up their precious ink when all that matters is the text itself.
Most browsers, by default, remove background images when printing documents.

If your background colors and images have been selected carefully and/or are crucial to the usefulness of the content, you can use the CSS {{cssxref("print-color-adjust")}} property to tell the browser that it should not make adjustments to the appearance of content.

The default value of `print-color-adjust`, `economy`, indicates that the browser is allowed to make appearance changes as it deems necessary in order to try to optimize the legibility and/or print economy of the content, given the type of output device the document is being drawn onto.

You can set `print-color-adjust` to `exact` to tell the browser that the element or elements on which you use it have been designed specifically to best work with the colors and images left as they are.
With this set, the browser won't tamper with the appearance of the element, and will draw it as indicated by your CSS.

> **Note:** There is no guarantee, though, that `print-color-adjust: exact` will result in your CSS being used exactly as given.
> If the browser provides user preferences to change the output (such as a "don't print backgrounds" checkbox in a print dialog box), that overrides the value of `print-color-adjust`.

## See also

- [Drawing graphics](/ko/docs/Learn/JavaScript/Client-side_web_APIs/Drawing_graphics)
- [Graphics on the web](/ko/docs/Web/Guide/Graphics)
- [MDN's color picker tool](/ko/docs/Web/CSS/CSS_Colors/Color_picker_tool)

---
# Source: Web_JavaScript_Reference_Statements_trycatch.md
---
---
title: try...catch
slug: Web/JavaScript/Reference/Statements/try...catch
---

{{jsSidebar("Statements")}}

**`try...catch`** 문은 실행할 코드블럭을 표시하고 예외(exception)가 발생(throw)할 경우의 응답을 지정합니다.

{{InteractiveExample("JavaScript Demo: Statement - Try...Catch")}}

```js interactive-example
try {
  nonExistentFunction();
} catch (error) {
  console.error(error);
  // Expected output: ReferenceError: nonExistentFunction is not defined
  // (Note: the exact output may be browser-dependent)
}
```

## 문법

```js
    try {
      try_statements
    }
    [catch (exception_var) {
      catch_statements
    }]
    [finally {
      finally_statements
    }]
```

- `try_statements`
  - : 실행될 선언들
- `catch_statements`
  - : try 블록에서 예외가 발생했을 때 실행될 선언들
- `exception_var`
  - : catch 블록과 관련된 예외 객체를 담기 위한 식별자
- `finally_statements`
  - : try 선언이 완료된 이후에 실행된 선언들. 이 선언들은 예외 발생 여부와 상관없이 실행된다.

## 설명

try 선언의 구성은 하나 혹은 그 이상의 선언을 포함한 try 블록 및 catch 항목이나 finally 항목 중 최소한 하나 혹은 둘 다 포함하여 이루어진다. 즉, try 선언에는 세 가지 형식이 존재한다.

1. `try...catch`
2. `try...finally`
3. `try...catch...finally`

`catch` 블록은 `try` 블록 안에서 예외가 발생(throw)하는 경우 무엇을 할지 명시하는 코드를 포함합니다. `try` 블록 (또는 `try` 블록 내에서 호출된 함수) 내의 명령문이 예외를 throw 하면 제어가 `catch` 블록으로 이동합니다. `try` 블록에 예외가 발생하지 않으면 `catch` 블록을 건너뜁니다.

`finally` 블록은 `try` 블록과 `catch` 블록(들)이 실행을 마친 후 항상 실행됩니다. 예외가 발생했는지에 관계없이 항상 실행됩니다.

하나 이상의 `try` 문을 중첩 할 수 있습니다. 내부의 `try` 문에 `catch` 블록이 없으면, 둘러싼 `try` 문의 `catch` 블록이 입력됩니다.

또한 `try` 문을 사용하여 예외처리를 합니다. 예외처리에 대해 더 알고 싶다면, [JavaScript Guide](/ko/docs/Web/JavaScript/Guide) 를 참고하세요.

### 무조건적 `catch` 문

`try`-block 내에서 예외가 발생하면 `catch`-block이 실행됩니다. 예를 들어, 다음 코드에서 예외가 발생하면 제어가 `catch` 블록으로 전송됩니다.

```js
try {
  throw "myException"; // generates an exception
} catch (e) {
  // statements to handle any exceptions
  logMyErrors(e); // pass exception object to error handler
}
```

### 조건적 `catch` 문

다음과 같이 `try...catch`블록을 `if...else if...else` 구조와 결합하여 '조건부 `catch`-blocks'을 만들 수 있습니다.

```js
try {
  myroutine(); // may throw three types of exceptions
} catch (e) {
  if (e instanceof TypeError) {
    // statements to handle TypeError exceptions
  } else if (e instanceof RangeError) {
    // statements to handle RangeError exceptions
  } else if (e instanceof EvalError) {
    // statements to handle EvalError exceptions
  } else {
    // statements to handle any unspecified exceptions
    logMyErrors(e); // pass exception object to error handler
  }
}
```

이에 대한 일반적인 사용 사례는 예상 오류의 작은 하위 집합 만 포착 (및 침묵) 한 다음 다른 경우에 오류를 다시 발생시키는 것입니다.

```js
try {
  myRoutine();
} catch (e) {
  if (e instanceof RangeError) {
    // statements to handle this very common expected error
  } else {
    throw e; // re-throw the error unchanged
  }
}
```

### The exception identifier

`try`-block에서 예외가 발생하면 `exception_var` (즉, `catch (e)`내부의 `e`)가 예외 값을 보유합니다. 이 식별자를 사용하여 발생한 예외에 대한 정보를 얻을 수 있습니다. 이 식별자는 `catch`-block의 {{Glossary("Scope", "scope")}}에서만 사용할 수 있습니다.

```js
function isValidJSON(text) {
  try {
    JSON.parse(text);
    return true;
  } catch {
    return false;
  }
}
```

### The finally-block

The `finally`-block contains statements to execute after the `try`-block and `catch`-block(s) execute, but before the statements following the `try...catch...finally`-block. Note that the `finally`-block executes regardless of whether an exception is thrown. Also, if an exception is thrown, the statements in the `finally`-block execute even if no `catch`-block handles the exception.

The following example shows one use case for the `finally`-block. The code opens a file and then executes statements that use the file; the `finally`-block makes sure the file always closes after it is used even if an exception was thrown.

```js
openMyFile();
try {
  // tie up a resource
  writeMyFile(theData);
} finally {
  closeMyFile(); // always close the resource
}
```

## Examples

### Nested try-blocks

First, let's see what happens with this:

```js
try {
  try {
    throw new Error("oops");
  } finally {
    console.log("finally");
  }
} catch (ex) {
  console.error("outer", ex.message);
}

// Output:
// "finally"
// "outer" "oops"
```

Now, if we already caught the exception in the inner `try`-block by adding a `catch`-block

```js
try {
  try {
    throw new Error("oops");
  } catch (ex) {
    console.error("inner", ex.message);
  } finally {
    console.log("finally");
  }
} catch (ex) {
  console.error("outer", ex.message);
}

// Output:
// "inner" "oops"
// "finally"
```

And now, let's rethrow the error.

```js
try {
  try {
    throw new Error("oops");
  } catch (ex) {
    console.error("inner", ex.message);
    throw ex;
  } finally {
    console.log("finally");
  }
} catch (ex) {
  console.error("outer", ex.message);
}

// Output:
// "inner" "oops"
// "finally"
// "outer" "oops"
```

Any given exception will be caught only once by the nearest enclosing `catch`-block unless it is rethrown. Of course, any new exceptions raised in the "inner" block (because the code in `catch`-block may do something that throws), will be caught by the "outer" block.

### Returning from a finally-block

If the `finally`-block returns a value, this value becomes the return value of the entire `try-catch-finally` statement, regardless of any `return` statements in the `try` and `catch`-blocks. This includes exceptions thrown inside of the `catch`-block:

```js
(function () {
  try {
    try {
      throw new Error("oops");
    } catch (ex) {
      console.error("inner", ex.message);
      throw ex;
    } finally {
      console.log("finally");
      return;
    }
  } catch (ex) {
    console.error("outer", ex.message);
  }
})();

// Output:
// "inner" "oops"
// "finally"
```

The outer "oops" is not thrown because of the return in the `finally`-block. The same would apply to any value returned from the `catch`-block.

## 명세서

{{Specifications}}

## 브라우저 호환성

{{Compat}}

## See also

- {{jsxref("Error")}}
- {{jsxref("Statements/throw", "throw")}}

---
# Source: Web_CSS_basic-shape.md
---
---
title: <basic-shape>
slug: Web/CSS/basic-shape
---

{{CSSRef}}

**`<basic-shape>`** [CSS](/ko/docs/Web/CSS) [자료형](/ko/docs/Web/CSS/CSS_Types)은 {{cssxref("clip-path")}}, {{cssxref("shape-outside")}}, {{cssxref("offset-path")}} 속성이 사용할 형태를 정의합니다.

{{InteractiveExample("CSS Demo: &lt;basic-shape&gt;")}}

```css interactive-example-choice
clip-path: inset(22% 12% 15px 35px);
```

```css interactive-example-choice
clip-path: circle(6rem at 12rem 8rem);
```

```css interactive-example-choice
clip-path: ellipse(115px 55px at 50% 40%);
```

```css interactive-example-choice
clip-path: polygon(
  50% 2.4%,
  34.5% 33.8%,
  0% 38.8%,
  25% 63.1%,
  19.1% 97.6%,
  50% 81.3%,
  80.9% 97.6%,
  75% 63.1%,
  100% 38.8%,
  65.5% 33.8%
);
```

```css interactive-example-choice
clip-path: path("M 50,245 A 160,160 0,0,1 360,120 z");
```

```html interactive-example
<section class="default-example" id="default-example">
  <div class="transition-all" id="example-element"></div>
</section>
```

```css interactive-example
#default-example {
  background: #fe9;
}

#example-element {
  background: linear-gradient(to bottom right, #f52, #05f);
  width: 100%;
  height: 100%;
}
```

## 구문

`<basic-shape>` 자료형은 아래의 기본 형태 함수 중 하나를 사용해 정의합니다.

형태를 생성할 때, 형태의 기준 상자는 `<basic-shape>` 값을 사용하는 속성이 결정합니다. 형태의 좌표계는 기준 상자의 좌상단을 원점으로 하고, X축은 오른쪽, Y축은 아래쪽으로 나가게 됩니다. 백분율료 표현한 모든 길이는 기준 상자의 크기를 사용해 계산합니다.

### 형태 함수

다음의 형태를 지원합니다. 모든 `<basic-shape>` 값은 함수형 표기법을 사용하고, 여기서는 [값 정의 구문](/ko/docs/Web/CSS/Value_definition_syntax)을 통해 정의합니다.

- `inset()`
  - :

    ```
    inset( <shape-arg>{1,4} [round <border-radius>]? )
    ```

    인셋(inset) 사각형을 정의합니다.

    매개변수 네 개를 모두 제공했을 땐 기준 상자의 상, 우, 하, 좌측 모서리에서 각각의 값만큼 안쪽으로 이동하여 인셋 사각형의 모서리를 구성합니다. 매개변수는 여백 단축 속성의 구분을 따르므로 네 모서리를 한 개, 두 개 등의 값만으로 정의할 수 있습니다.

    선택적 {{cssxref("border-radius", "&lt;border-radius&gt;")}} 매개변수를 `border-radius` 단축 속성 구문을 사용해 지정하면 인셋 사각형의 모서리를 둥글게 만들 수 있습니다.

    좌우 인셋 각각 75%처럼, 한 축의 인셋 쌍 값의 합이 요소가 차지하는 크기보다 큰 경우 면적 없는 형태를 정의합니다. For this specification, this results in an empty float area.

- `circle()`
  - :

    ```
    circle( [<shape-radius>]? [at <position>]? )
    ```

    `<shape-radius>` 매개변수는 원의 반지름 *r*을 지정합니다. 음수는 유효하지 않습니다. 백분율 값을 사용하면 기준 상자의 너비와 높이를 공식 `sqrt(width^2+height^2)/sqrt(2)`에 대입한 결과가 최종 값이 됩니다.

    {{cssxref("&lt;position&gt;")}} 매개변수는 원의 중심을 지정합니다. 생략할 경우 중앙을 기본값으로 사용합니다.

- `ellipse()`
  - :

    ```
    ellipse( [<shape-radius>{2}]? [at <position>]? )
    ```

    `<shape-radius>` 매개변수는 타원의 X축, Y축 반지름인 rx와 ry를 순서대로 지정합니다. 두 값 모두 음수는 유효하지 않습니다. 백분율 값을 사용하면 기준 상자의 너비(rx)와 높이(ry)를 사용해 계산합니다.

    {{cssxref("&lt;position&gt;")}} 매개변수는 타원의 중심을 지정합니다. 생략할 경우 중앙을 기본값으로 사용합니다.

- `polygon()`
  - :

    ```
    polygon( [<fill-rule>,]? [<shape-arg> <shape-arg>]# )
    ```

    `<fill-rule>` represents the [filling rule](/ko/docs/Web/SVG/Attribute/fill-rule) used to determine the interior of the polygon. Possible values are `nonzero` and `evenodd`. Default value when omitted is `nonzero`.

    Each pair argument in the list represents _xi_ and _yi_ - the x and y axis coordinates of the ith vertex of the polygon.

- `path()`
  - :

    ```
    path( [<fill-rule>,]? <string>)
    ```

    The optional `<fill-rule>` represents the [filling rule](/ko/docs/Web/SVG/Attribute/fill-rule) used to determine the interior of the path. Possible values are `nonzero` and `evenodd`. Default value when omitted is `nonzero`.

    The required \<string> is an [SVG Path](/ko/docs/SVG/Attribute/d) string encompassed in quotes

The arguments not defined above are defined as follows:

```
<shape-arg> = <length> | <percentage>
<shape-radius> = <length> | <percentage> | closest-side | farthest-side
```

Defines a radius for a circle or ellipse. If omitted it defaults to `closest-side`.

`closest-side` uses the length from the center of the shape to the closest side of the reference box. For circles, this is the closest side in any dimension. For ellipses, this is the closest side in the radius dimension.

`farthest-side` uses the length from the center of the shape to the farthest side of the reference box. For circles, this is the farthest side in any dimension. For ellipses, this is the farthest side in the radius dimension.

## 기본 형태의 계산값

The values in a `<basic-shape>` function are computed as specified, with these exceptions:

- Omitted values are included and compute to their defaults.
- A {{cssxref("&lt;position&gt;")}} value in `circle()` or `ellipse()` is computed as a pair of offsets (horizontal then vertical) from the top left origin, each given as a combination of an absolute length and a percentage.
- A [`<border-radius>`](/ko/docs/Web/CSS/border-radius) value in `inset()` is computed as an expanded list of all eight {{cssxref("length")}} or percentage values.

## 기본 형태의 보간법

When animating between one `<basic-shape>` and another, the rules below are applied. The values in the shape functions interpolate as a simple list. The list values interpolate as {{cssxref("&lt;length&gt;")}}, {{cssxref("&lt;percentage&gt;")}}, or {{cssxref("calc()")}} where possible. If list values are not one of those types but are identical, those values do interpolate.

- Both shapes must use the same reference box.
- If both shapes are the same type, that type is `ellipse()` or `circle()`, and none of the radii use the `closest-side` or `farthest-side` keywords, interpolate between each value in the shape functions.
- If both shapes are of type `inset()`, interpolate between each value in the shape functions.
- If both shapes are of type `polygon()`, both polygons have the same number of vertices, and use the same `<fill-rule>`, interpolate between each value in the shape functions.
- If both shapes are of type `path()`, both paths strings have the same number and types of path data commands in the same order, interpolate each path data command as real numbers.
- In all other cases no interpolation occurs.

## Examples

### Animated polygon

In this example, we use the [@keyframes](/ko/docs/Web/CSS/@keyframes) at-rule to animate a clip path between two polygons. Note that both polygons have the same number of vertices, which is necessary for this type of animation to work.

#### HTML

```html
<div></div>
```

#### CSS

```css
div {
  width: 300px;
  height: 300px;
  background: repeating-linear-gradient(red, orange 50px);
  clip-path: polygon(
    50% 0%,
    60% 40%,
    100% 50%,
    60% 60%,
    50% 100%,
    40% 60%,
    0% 50%,
    40% 40%
  );
  animation: 4s poly infinite alternate ease-in-out;
  margin: 10px auto;
}

@keyframes poly {
  from {
    clip-path: polygon(
      50% 0%,
      60% 40%,
      100% 50%,
      60% 60%,
      50% 100%,
      40% 60%,
      0% 50%,
      40% 40%
    );
  }

  to {
    clip-path: polygon(
      50% 30%,
      100% 0%,
      70% 50%,
      100% 100%,
      50% 70%,
      0% 100%,
      30% 50%,
      0% 0%
    );
  }
}
```

#### Result

{{EmbedLiveSample('Animated_polygon','340', '340')}}

## 명세서

{{Specifications}}

## 브라우저 호환성

{{Compat}}

## See also

- Properties that use this data type: {{cssxref("clip-path")}}, {{cssxref("shape-outside")}}
- [Edit Shape Paths in CSS — Firefox Developer Tools](https://firefox-source-docs.mozilla.org/devtools-user/page_inspector/how_to/edit_css_shapes/index.html)
- [Overview of CSS Shapes](/ko/docs/Web/CSS/CSS_Shapes/Overview_of_CSS_Shapes)

---
# Source: Web_CSS_before.md
---
---
title: "::before (:before)"
slug: Web/CSS/::before
---

{{CSSRef}}

CSS에서, **`::before`** 는 선택한 요소의 첫 자식으로 [의사 요소](/ko/docs/Web/CSS/Pseudo-elements)를 하나 생성합니다. 보통 {{cssxref("content")}} 속성과 함께 짝지어, 요소에 장식용 콘텐츠를 추가할 때 사용합니다. 기본값은 인라인입니다.

```css
/* 링크 앞에 하트 추가 */
a::after {
  content: "♥";
}
```

> **참고:** `::before`와 `::after`로 생성한 의사 요소는 [원본 요소의 서식 박스에 포함되므로](https://www.w3.org/TR/CSS2/generate.html#before-after-content), {{HTMLElement("img")}}나 {{HTMLElement("br")}} 등 [대체 요소](/ko/docs/Web/CSS/Replaced_element)에 적용할 수 없습니다.

## 구문

{{csssyntax}}

> **참고:** [의사 클래스](/ko/docs/Web/CSS/Pseudo-classes)와 [의사 요소](/ko/docs/Web/CSS/Pseudo-elements)를 구분하기 위해 CSS3부터`::before` 구문을 도입했습니다. 그러나 브라우저는 CSS2 구문인 `:before`도 허용합니다.

## 예제

### 인용 표시 추가

One simple example of using `::before` pseudo-elements is to provide quotation marks. Here we use both `::before` and `{{Cssxref("::after")}}` to insert quotation characters.

#### HTML

```html
<q>Some quotes,</q> he said, <q>are better than none.</q>
```

#### CSS

```css
q::before {
  content: "«";
  color: blue;
}

q::after {
  content: "»";
  color: red;
}
```

#### Result

{{EmbedLiveSample('인용_표시_추가', '500', '50', '')}}

### 장식 예제

We can style text or images in the {{cssxref("content")}} property almost any way we want.

#### HTML

```html
<span class="ribbon">Notice where the orange box is.</span>
```

#### CSS

```css
.ribbon {
  background-color: #5bc8f7;
}

.ribbon::before {
  content: "Look at this orange box.";
  background-color: #ffba10;
  border-color: black;
  border-style: dotted;
}
```

#### Result

{{EmbedLiveSample('장식_예제', 450, 60)}}

### 할 일 목록

In this example we will create a simple to-do list using pseudo-elements. This method can often be used to add small touches to the UI and improve user experience.

#### HTML

```html
<ul>
  <li>Buy milk</li>
  <li>Take the dog for a walk</li>
  <li>Exercise</li>
  <li>Write code</li>
  <li>Play music</li>
  <li>Relax</li>
</ul>
```

#### CSS

```css
li {
  list-style-type: none;
  position: relative;
  margin: 2px;
  padding: 0.5em 0.5em 0.5em 2em;
  background: lightgrey;
  font-family: sans-serif;
}

li.done {
  background: #ccff99;
}

li.done::before {
  content: "";
  position: absolute;
  border-color: #009933;
  border-style: solid;
  border-width: 0 0.3em 0.25em 0;
  height: 1em;
  top: 1.3em;
  left: 0.6em;
  margin-top: -1em;
  transform: rotate(45deg);
  width: 0.5em;
}
```

#### JavaScript

```js
var list = document.querySelector("ul");
list.addEventListener(
  "click",
  function (ev) {
    if (ev.target.tagName === "LI") {
      ev.target.classList.toggle("done");
    }
  },
  false,
);
```

Here is the above code example running live. Note that there are no icons used, and the check-mark is actually the `::before` that has been styled in CSS. Go ahead and get some stuff done.

#### Result

{{EmbedLiveSample('할_일_목록', 400, 300)}}

### 특수문자

As this is CSS; not HTML, you can **not** use markup entities in content values. If you need to use a special character, and can not enter it literally into your CSS content string, use a unicodeescape sequence, consistingof a backslash followed by the hexadecimal unicode value.

#### HTML

```html
<ol>
  <li>Crack Eggs into bowl</li>
  <li>Add Milk</li>
  <li>Add Flour</li>
  <li aria-current="step">Mix thoroughly into a smooth batter</li>
  <li>Pour a ladleful of batter onto a hot, greased, flat frying pan</li>
  <li>Fry until the top of the pancake loses its gloss</li>
  <li>Flip it over and fry for a couple more minutes</li>
  <li>serve with your favorite topping</li>
</ol>
```

#### CSS

```css
li {
  padding: 0.5em;
}

li[aria-current="step"] {
  font-weight: bold;
}

li[aria-current="step"]::after {
  content: " \21E6"; /* Hexadecimal for Unicode Leftwards white arrow*/
  display: inline;
}
```

#### Result

{{EmbedLiveSample('특수문자', 400, 200)}}

## 명세

{{Specifications}}

## 브라우저 호환성

{{Compat}}

## 같이 보기

- {{Cssxref("::after")}}
- {{Cssxref("content")}}

---
# Source: Web_JavaScript_Reference_Lexical_grammar.md
---
---
title: 어휘 문법
slug: Web/JavaScript/Reference/Lexical_grammar
---

{{JsSidebar("More")}}

이 페이지는 JavaScript의 어휘 문법(lexical grammar)을 설명합니다. ECMAScript 소스 본문은 왼쪽에서 오른쪽 방향으로 분석되고 토큰, 제어문자, 줄바꿈, 주석, 또는 공백으로 구성되는 입력 요소 시퀀스로 바뀝니다. 또한 ECMAScript는 특별한 키워드와 리터럴을 정의하고 있으며 명령문 끝에 자동으로 세미콜론을 추가하는 규칙이 있습니다.

## 제어 문자

제어 문자는 눈에 보이지 않지만 스크립트 소스 본문 해석을 제어하는 데 사용됩니다.

<table class="standard-table">
  <caption>
    유니코드 형식 제어 문자
  </caption>
  <tbody>
    <tr>
      <th>코드 포인트</th>
      <th>이름</th>
      <th>축약형</th>
      <th>설명</th>
    </tr>
    <tr>
      <td><code>U+200C</code></td>
      <td>Zero width non-joiner</td>
      <td>&#x3C;ZWNJ></td>
      <td>
        <p>
          특정 언어에서 문자들이 연결선으로 묶이지 않게 하기 위해 문자 사이에
          위치한다(<a href="http://en.wikipedia.org/wiki/Zero-width_non-joiner"
            >Wikipedia</a
          >).
        </p>
      </td>
    </tr>
    <tr>
      <td><code>U+200D</code></td>
      <td>Zero width joiner</td>
      <td>&#x3C;ZWJ></td>
      <td>
        <p>
          특정 언어에서, 보통은 연결되지 않는 문자이나 해당 문자를 연결된 형태로
          그리기 위해서(to be rendered) 사용하며 문자 사이에 위치한다(<a
            href="http://en.wikipedia.org/wiki/Zero-width_joiner"
            >Wikipedia</a
          >).
        </p>
      </td>
    </tr>
    <tr>
      <td><code>U+FEFF</code></td>
      <td>Byte order mark</td>
      <td>&#x3C;BOM></td>
      <td>
        <p>
          스크립트 맨 앞에 두어 스크립트 본문의 byte order와 유니코드를 표시하는
          데에 사용한다.(<a href="http://en.wikipedia.org/wiki/Byte_order_mark"
            >Wikipedia</a
          >).
        </p>
      </td>
    </tr>
  </tbody>
</table>

## 공백

공백 문자는 소스 본문을 읽기 좋게 만들고 토큰을 구분합니다. 이 공백 문자들은 보통 코드의 기능에 필요한 것은 아닙니다. 최소화 도구([Minification tools](http://en.wikipedia.org/wiki/Minification_%28programming%29))는 종종 전송해야하는 데이터 크기를 줄이기 위해서 공백을 제거합니다.

| 코드 포인트 | 이름                           | 축약형  | 설명                                                                                                     | 이스케이프 시퀀스 |
| ----------- | ------------------------------ | ------- | -------------------------------------------------------------------------------------------------------- | ----------------- |
| U+0009      | Character tabulation           | \<HT>   | Horizontal tabulation                                                                                    | \t                |
| U+000B      | Line tabulation                | \<VT>   | Vertical tabulation                                                                                      | \v                |
| U+000C      | Form feed                      | \<FF>   | Page breaking control character ([Wikipedia](http://en.wikipedia.org/wiki/Page_break#Form_feed)).        | \f                |
| U+0020      | Space                          | \<SP>   | Normal space                                                                                             |                   |
| U+00A0      | No-break space                 | \<NBSP> | Normal space, but no point at which a line may break                                                     |                   |
| Others      | Other Unicode space characters | \<USP>  | [Spaces in Unicode on Wikipedia](http://en.wikipedia.org/wiki/Space_%28punctuation%29#Spaces_in_Unicode) |                   |

## 개행 문자

공백문자와 더불어, 개행 문자는 소스 본문의 가독성을 향상시킵니다. 하지만, 몇몇 상황에서 개행 문자는 코드 내부에 숨겨지기 때문에 JavaScript 코드 실행에 영향을 미칩니다. 개행 문자는 자동 새미콜론 삽입([automatic semicolon insertion](#Automatic_semicolon_insertion)) 규칙에도 영향을 줍니다. 개행 문자는 표준 표현방식([regular expressions](/ko/docs/Web/JavaScript/Guide/Regular_Expressions))의 클래스인 \s로 매치됩니다.

아래의 유니코드 문자만이 ECMAScript에서 라인 종결자로 다뤄지며, 라인을 바꾸는 다른 문자들은 공백으로 생각하시면 됩니다(예를 들어, Next Line, NEL, U+0085는 공백으로 간주).

| 코드 포인트 | 이름                | 축약형 | 설명                                                   | 이스케이프 시퀀스 |
| ----------- | ------------------- | ------ | ------------------------------------------------------ | ----------------- |
| U+000A      | Line Feed           | \<LF>  | New line character in UNIX systems.                    | \n                |
| U+000D      | Carriage Return     | \<CR>  | New line character in Commodore and early Mac systems. | \r                |
| U+2028      | Line Separator      | \<LS>  | [Wikipedia](http://en.wikipedia.org/wiki/Newline)      |                   |
| U+2029      | Paragraph Separator | \<PS>  | [Wikipedia](http://en.wikipedia.org/wiki/Newline)      |                   |

## 주석

주석은 힌트, 필기, 제안이나 주의할 점들을 JavaScript 코드에 넣을 때 사용합니다. 이는 더 쉽게 읽고 이해할 수 있게 도와줍니다. 또한 특정 코드가 실행되지 않도록 막아주기도 합니다. 따라서 주석은 유용한 디버깅 도구라고도 할 수 있습니다.

JavaScript에는 코드 속에 주석을 쓰는 두 가지 방식이 있습니다.

첫 번째, '//'로 첨언하기입니다. 이는 아래의 예시처럼 같은 줄에 있는 모든 코드를 주석으로 바꿉니다.

```js
function comment() {
  // JavaScript의 각주 한 줄입니다.
  console.log("Hello world!");
}
comment();
```

두 번째, 좀 더 유연하게 쓸 수 있는 '/\* \*/'로 첨언하기입니다.

예를 들면, 한 줄에 첨언할 때는 이렇게 쓸 수 있습니다 :

```js
function comment() {
  /* JavaScript 각주 한 줄입니다. */
  console.log("Hello world!");
}
comment();
```

여러 줄로 첨언할 때는, 이렇게 씁니다 :

```js
function comment() {
  /* This comment spans multiple lines. Notice
     that we don't need to end the comment until we're done. */
  console.log("Hello world!");
}
comment();
```

원한다면, 라인 중간에도 사용할 수 있습니다. 물론 코드의 가독성이 떨어지게 됩니다. 그러니 주의를 기울여 사용해야 합니다:

```js
function comment(x) {
  console.log("Hello " + x /* insert the value of x */ + " !");
}
comment("world");
```

게다가, 코드 실행을 막기 위해 코드를 무용화 시키는데도 사용할 수 있습니다. 아래처럼 코드를 코멘트로 감싸는 거죠:

```js
function comment() {
  /* console.log("Hello world!"); */
}
comment();
```

In this case, the `console.log()` call is never issued, since it's inside a comment. Any number of lines of code can be disabled this way.

## 해시뱅 주석

A specialized third comment syntax, the **hashbang comment**, is in the process of being standardized in ECMAScript (see the [Hashbang Grammar proposal](https://github.com/tc39/proposal-hashbang)).

A hashbang comment behaves exactly like a single line-only (`//`) comment, but it instead begins with `#!` and **is only valid at the absolute start of a script or module**. Note also that no whitespace of any kind is permitted before the `#!`. The comment consists of all the characters after `#!` up to the end of the first line; only one such comment is permitted.

The hashbang comment specifies the path to a specific JavaScript interpreter
that you want to use to execute the script. An example is as follows:

```js
#!/usr/bin/env node

console.log("Hello world");
```

> **Note:** Hashbang comments in JavaScript mimic [shebangs in Unix](<https://en.wikipedia.org/wiki/Shebang_(Unix)>) used to run files with proper interpreter.

> **Warning:** Although [BOM](https://en.wikipedia.org/wiki/Byte_order_mark) before hashbang comment will work in a browser it is not advised to use BOM in a script with hasbang. BOM will not work when you try to run the script in Unix/Linux. So use UTF-8 without BOM if you want to run scripts directly from shell.

You must only use the `#!` comment style to specify a JavaScript interpreter. In all other cases just use a `//` comment (or mulitiline comment).

## 키워드

### ECMAScript 2015 기준 예약 키워드

- {{jsxref("Statements/break", "break")}}
- {{jsxref("Statements/switch", "case")}}
- {{jsxref("Statements/try...catch", "catch")}}
- {{jsxref("Statements/class", "class")}}
- {{jsxref("Statements/const", "const")}}
- {{jsxref("Statements/continue", "continue")}}
- {{jsxref("Statements/debugger", "debugger")}}
- {{jsxref("Statements/default", "default")}}
- {{jsxref("Operators/delete", "delete")}}
- {{jsxref("Statements/do...while", "do")}}
- {{jsxref("Statements/if...else", "else")}}
- {{jsxref("Statements/export", "export")}}
- {{jsxref("Statements/class", "extends")}}
- {{jsxref("Statements/try...catch", "finally")}}
- {{jsxref("Statements/for", "for")}}
- {{jsxref("Statements/function", "function")}}
- {{jsxref("Statements/if...else", "if")}}
- {{jsxref("Statements/import", "import")}}
- {{jsxref("Operators/in", "in")}}
- {{jsxref("Operators/instanceof", "instanceof")}}
- {{jsxref("Operators/new", "new")}}
- {{jsxref("Statements/return", "return")}}
- {{jsxref("Operators/super", "super")}}
- {{jsxref("Statements/switch", "switch")}}
- {{jsxref("Operators/this", "this")}}
- {{jsxref("Statements/throw", "throw")}}
- {{jsxref("Statements/try...catch", "try")}}
- {{jsxref("Operators/typeof", "typeof")}}
- {{jsxref("Statements/var", "var")}}
- {{jsxref("Operators/void", "void")}}
- {{jsxref("Statements/while", "while")}}
- {{jsxref("Statements/with", "with")}}
- {{jsxref("Operators/yield", "yield")}}

### 확장 예약 키워드

The following are reserved as future keywords by the ECMAScript specification. They have no special functionality at present, but they might at some future time, so they cannot be used as identifiers.

These are always reserved:

- `enum`

The following are only reserved when they are found in strict mode code:

- `implements`
- `interface`
- {{jsxref("Statements/let", "let")}}
- `package`
- `private`
- `protected`
- `public`
- `static`

The following are only reserved when they are found in module code:

- `await`

#### 구형 표준의 확장 예약 키워드

The following are reserved as future keywords by older ECMAScript specifications (ECMAScript 1 till 3).

- `abstract`
- `boolean`
- `byte`
- `char`
- `double`
- `final`
- `float`
- `goto`
- `int`
- `long`
- `native`
- `short`
- `synchronized`
- `throws`
- `transient`
- `volatile`

Additionally, the literals `null`, `true`, and `false` cannot be used as identifiers in ECMAScript.

### 예약어 사용법

Reserved words actually only apply to Identifiers (vs. `IdentifierNames`) . As described in [es5.github.com/#A.1](http://es5.github.com/#A.1), these are all `IdentifierNames` which do not exclude `ReservedWords`.

```js
a.import
a['import']
a = { import: 'test' }.
```

On the other hand the following is illegal because it's an `Identifier`, which is an `IdentifierName` without the reserved words. Identifiers are used for `FunctionDeclaration, FunctionExpression, VariableDeclaration` and so on. `IdentifierNames` are used for `MemberExpression, CallExpression` and so on.

```js
function import() {} // Illegal.
```

## 리터럴

### Null 리터럴

See also [`null`](/ko/docs/Web/JavaScript/Reference/Global_Objects/null) for more information.

```js
null;
```

### 불리언 리터럴

See also [`Boolean`](/ko/docs/Web/JavaScript/Reference/Global_Objects/Boolean) for more information.

```js
true;
false;
```

### 숫자 리터럴

#### 10진법

```js
1234567890;
42;

// Caution when using with a leading zero:
0888; // 888 parsed as decimal
0777; // parsed as octal, 511 in decimal
```

Note that decimal literals can start with a zero (`0`) followed by another decimal digit, but If all digits after the leading `0` are smaller than 8, the number is interpreted as an octal number. This won't throw in JavaScript, see [Firefox bug 957513](https://bugzil.la/957513). See also the page about [`parseInt()`](/ko/docs/Web/JavaScript/Reference/Global_Objects/parseInt#Octal_interpretations_with_no_radix).

##### Exponential

The decimal exponential literal is specified by the following format: `beN`; where `b` is a base number (integer or floating), followed by `e` char (which serves as separator or _exponent indicator_) and _`N`_, which is _exponent_ or _power_ number – a signed integer (as per 2019 ECMA-262 specs):

```
    0e-5   // => 0
    0e+5   // => 0
    5e1    // => 50
    175e-2 // => 1.75
    1e3    // => 1000
    1e-3   // => 0.001
```

#### 2진법

Binary number syntax uses a leading zero followed by a lowercase or uppercase Latin letter "B" (`0b` or `0B`). Because this syntax is new in ECMAScript 2015, see the browser compatibility table, below. If the digits after the `0b` are not 0 or 1, the following [`SyntaxError`](/ko/docs/Web/JavaScript/Reference/Global_Objects/SyntaxError) is thrown: "Missing binary digits after 0b".

```js
var FLT_SIGNBIT = 0b10000000000000000000000000000000; // 2147483648
var FLT_EXPONENT = 0b01111111100000000000000000000000; // 2139095040
var FLT_MANTISSA = 0b00000000011111111111111111111111; // 8388607
```

#### 8진법

Octal number syntax uses a leading zero followed by a lowercase or uppercase Latin letter "O" (`0o` or `0O)`. Because this syntax is new in ECMAScript 2015, see the browser compatibility table, below. If the digits after the `0o` are outside the range (01234567), the following [`SyntaxError`](/ko/docs/Web/JavaScript/Reference/Global_Objects/SyntaxError) is thrown: "Missing octal digits after 0o".

```js
var n = 0o755; // 493
var m = 0o644; // 420

// Also possible with just a leading zero (see note about decimals above)
0755;
0644;
```

#### 16진법

Hexadecimal number syntax uses a leading zero followed by a lowercase or uppercase Latin letter "X" (`0x` or `0X)`. If the digits after 0x are outside the range (0123456789ABCDEF), the following [`SyntaxError`](/ko/docs/Web/JavaScript/Reference/Global_Objects/SyntaxError) is thrown: "Identifier starts immediately after numeric literal".

```js
0xfffffffffffffffff; // 295147905179352830000
0x123456789abcdef; // 81985529216486900
0xa; // 10
```

#### BigInt literal

The {{jsxref("BigInt")}} type is a numeric primitive in JavaScript that can represent integers with arbitrary precision. BigInt literals are created by appending `n` to the end of an integer.

```
    123456789123456789n     // 123456789123456789
    0o777777777777n         // 68719476735
    0x123456789ABCDEFn      // 81985529216486895‬
    0b11101001010101010101n // 955733
```

Note that legacy octal numbers with just a leading zero won't work for `BigInt`:

```plain example-bad
// 0755n
// SyntaxError: invalid BigInt syntax
```

For octal `BigInt` numbers, always use zero followed by the letter "o" (uppercase or lowercase):

```plain example-good
0o755n
```

For more information about `BigInt`, see also [JavaScript data structures](/ko/docs/Web/JavaScript/Data_structures#BigInt_type).

#### Numeric separators

To improve readability for numeric literals, underscores (`_`, `U+005F`) can be used as separators:

```
    // separators in decimal numbers
    1_000_000_000_000
    1_050.95

    // separators in binary numbers
    0b1010_0001_1000_0101

    // separators in octal numbers
    0o2_2_5_6

    // separators in hex numbers
    0xA0_B0_C0

    // separators in BigInts
    1_000_000_000_000_000_000_000n
```

Note these limitations:

```plain example-bad
// More than one underscore in a row is not allowed
100__000; // SyntaxError

// Not allowed at the end of numeric literals
100_; // SyntaxError

// Can not be used after leading 0
0_1; // SyntaxError
```

### 객체 리터럴

See also {{jsxref("Object")}} and [Object initializer](/ko/docs/Web/JavaScript/Reference/Operators/Object_initializer) for more information.

```js
var o = { a: "foo", b: "bar", c: 42 };

// shorthand notation. New in ES2015
var a = "foo",
  b = "bar",
  c = 42;
var o = { a, b, c };

// instead of
var o = { a: a, b: b, c: c };
```

### 배열 리터럴

See also {{jsxref("Array")}} for more information.

```js
[1954, 1974, 1990, 2014];
```

### 문자열 리터럴

A string literal is zero or more Unicode code points enclosed in single or double quotes. Unicode code points may also be represented by an escape sequence. All code points may appear literally in a string literal except for these closing quote code points:

- U+005C (backslash),
- U+000D \<CR>,
- and U+000A \<LF>.

Prior to the [proposal to make all JSON text valid ECMA-262](https://github.com/tc39/proposal-json-superset), U+2028 \<LS> and U+2029 \<PS>, were also disallowed from appearing unescaped in string literals.

Any code points may appear in the form of an escape sequence. String literals evaluate to ECMAScript String values. When generating these String values Unicode code points are UTF-16 encoded.

```js-nolint
'foo';
"bar";
```

#### 16진수 이스케이프 시퀀스

Hexadecimal escape sequences consist of `\x` followed by exactly two hexadecimal digits representing a code unit or code point in the range 0x0000 to 0x00FF.

```js
"\xA9"; // "©"
```

#### 유니코드 이스케이프 시퀀스

A Unicode escape sequence consists of exactly four hexadecimal digits following `\u`. It represents a code unit in the UTF-16 encoding. For code points U+0000 to U+FFFF, the code unit is equal to the code point. Code points U+10000 to U+10FFFF require two escape sequences representing the two code units (a surrogate pair) used to encode the character; the surrogate pair is distinct from the code point.

See also {{jsxref("String.fromCharCode()")}} and {{jsxref("String.prototype.charCodeAt()")}}.

```js
"\u00A9"; // "©" (U+A9)
```

#### 유니코드 코드 포인트 시퀀스

A Unicode code point escape consists of `\u{`, followed by a code point in hexadecimal base, followed by `}`. The value of the hexadecimal digits must be in the range 0 and 0x10FFFF inclusive. Code points in the range U+10000 to U+10FFFF do not need to be represented as a surrogate pair. Code point escapes were added to JavaScript in ECMAScript 2015 (ES6).

See also {{jsxref("String.fromCodePoint()")}} and {{jsxref("String.prototype.codePointAt()")}}.

```js
"\u{2F804}"; // CJK COMPATIBILITY IDEOGRAPH-2F804 (U+2F804)

// the same character represented as a surrogate pair
"\uD87E\uDC04";
```

### 정규 표현식 리터럴

See also [`RegExp`](/ko/docs/Web/JavaScript/Reference/Global_Objects/RegExp) for more information.

```js
/ab+c/g

// An "empty" regular expression literal
// The empty non-capturing group is necessary
// to avoid ambiguity with single-line comments.
/(?:)/
```

### 템플릿 리터럴

See also [template strings](/ko/docs/Web/JavaScript/Reference/template_strings) for more information.

```js
`string text`;

`string text line 1
 string text line 2`;

`string text ${expression} string text`;

tag`string text ${expression} string text`;
```

## 자동 세미콜론 삽입

Some [JavaScript statements](/ko/docs/Web/JavaScript/Reference/Statements) must be terminated with semicolons and are therefore affected by automatic semicolon insertion (ASI):

- Empty statement
- `let`, `const`, variable statement
- `import`, `export`, module declaration
- Expression statement
- `debugger`
- `continue`, `break`, `throw`
- `return`

The ECMAScript specification mentions [three rules of semicolon insertion](https://tc39.github.io/ecma262/#sec-rules-of-automatic-semicolon-insertion).

1. A semicolon is inserted before, when a [Line terminator](#Line_terminators) or "}" is encountered that is not allowed by the grammar.

   ```js-nolint
   { 1 2 } 3

   // is transformed by ASI into

   { 1 2 ;} 3;
   ```

2. A semicolon is inserted at the end, when the end of the input stream of tokens is detected and the parser is unable to parse the single input stream as a complete program.

   Here `++` is not treated as a [postfix operator](/ko/docs/Web/JavaScript/Reference/Operators/Arithmetic_Operators#Increment) applying to variable `b`, because a line terminator occurs between `b` and `++`.

   ```js-nolint
   a = b
   ++c

   // is transformend by ASI into

   a = b;
   ++c;
   ```

3. A semicolon is inserted at the end, when a statement with restricted productions in the grammar is followed by a line terminator. These statements with "no LineTerminator here" rules are:
   - PostfixExpressions (`++` and `--`)
   - `continue`
   - `break`
   - `return`
   - `yield`, `yield*`
   - `module`

   ```js-nolint
   return
   a + b

   // is transformed by ASI into

   return;
   a + b;
   ```

## 명세

{{Specifications}}

## 브라우저 호환성

{{Compat}}

## 같이 보기

- {{jsxref("Boolean")}}
- {{jsxref("Number")}}
- {{jsxref("RegExp")}}
- {{jsxref("String")}}
- [Jeff Walden: Binary and octal numbers](http://whereswalden.com/2013/08/12/micro-feature-from-es6-now-in-firefox-aurora-and-nightly-binary-and-octal-numbers/)
- [Mathias Bynens: JavaScript character escape sequences](http://mathiasbynens.be/notes/javascript-escapes)

---
# Source: Web_API_Window_pageYOffset.md
---
---
title: Window.pageYOffset
slug: Web/API/Window/pageYOffset
---

{{ APIRef("CSSOM View") }}

{{domxref("Window")}} 인터페이스의 **`pageYOffset`** 읽기 전용 속성은 {{domxref("Window.scrollY", "scrollY")}}의 다른 이름으로, 문서가 수직으로 얼마나 스크롤됐는지 픽셀 단위로 반환합니다.

일부 오래된 브라우저는 `scrollY` 대신 `pageYOffset`만 지원하는 경우가 있지만, 노후 환경을 신경쓰지 않아도 된다면 둘 중 아무거나 사용해도 괜찮습니다.

수평 스크롤을 나타내는 {{domxref("Window.pageXOffset", "pageXOffset")}} 속성 역시 {{domxref("Window.scrollX", "scrollX")}}의 다른 이름입니다.

## 구문

```js
yOffset = window.pageYOffset;
```

### 값

{{domxref("Window")}} 안의 {{domxref("Document")}}가 수직 방향으로 스크롤된 거리를 픽셀 단위로 나타낸 부동소숫점 수. 단일 픽셀보다 높은 수준의 정밀도를 가지므로 정수가 아닐 수 있습니다. `0.0`은 창의 콘텐츠 영역과 문서의 위쪽 모서리 위치가 일치함을 나타냅니다.

`pageYOffset`은 {{domxref("Window.scrollY")}}의 다른 이름이므로, 값에 대한 더 자세한 정보는 해당 문서를 방문해주세요.

## 예제

```js hidden
var contentHTML = `
    <h2 id="introduction">Introduction</h2>
  <p>Lorem ipsum dolor sit amet, consectetur adipiscing
elit. Aenean volutpat vitae felis non dictum. Ut auctor
eros tortor, vel elementum arcu rhoncus nec. Donec non
laoreet massa. Donec pretium nisi et condimentum convallis.
Nullam dictum molestie finibus. Nullam vitae lorem non
augue mattis cursus.</p>
  <p>Maecenas nec tortor tincidunt, sollicitudin mi eget,
fermentum turpis. Vestibulum ac ante et libero efficitur
faucibus id eget ex. Pellentesque tempor pharetra
tincidunt. Suspendisse potenti. Nulla vulputate nunc sit
amet hendrerit faucibus. Nullam metus dui, venenatis
lacinia nunc nec, vestibulum viverra nunc. Quisque interdum
quam tortor, sit amet varius neque consectetur at. Quisque
vel turpis justo.</p>
  <h2 id="overview">Overview</h2>
  <p>Lorem ipsum dolor sit amet, consectetur adipiscing
elit. Etiam dui dolor, pulvinar sed diam id, eleifend
dapibus odio. Duis vitae ante nibh. Integer bibendum
imperdiet suscipit. Fusce ligula leo, consectetur ac ante
eget, gravida laoreet purus. Cras sodales efficitur risus,
sed feugiat sem. Pellentesque justo augue, placerat non leo
sit amet, laoreet fringilla arcu.</p>
  <p>Class aptent taciti sociosqu ad litora torquent per
conubia nostra, per inceptos himenaeos. Proin in gravida
libero. Vivamus placerat, lacus eget condimentum sagittis,
enim nunc bibendum nisi, quis varius erat felis sit amet
risus.</p>
<p>Sed non finibus ligula. Fusce a magna auctor, molestie
nibh eget, sodales felis. Donec imperdiet facilisis mi ut
aliquam. Etiam sodales suscipit urna, eget hendrerit neque
elementum a. Vivamus fringilla sodales est ut ultricies.
Nulla convallis congue maximus. Nullam consectetur felis
vitae ultricies accumsan. Mauris at aliquam felis. Mauris
efficitur tellus massa, id ullamcorper ipsum fermentum eu.
Aenean mollis dignissim ultrices. Nunc gravida, sem sit
amet lobortis iaculis, dolor ligula convallis nibh, id
condimentum metus libero nec odio. Quisque nec ante
pretium, viverra neque nec, facilisis risus. Duis
condimentum sapien non felis cursus blandit. Integer
euismod lectus a ipsum pellentesque lacinia.</p>
`;

document.getElementById("frame").contentDocument.body.innerHTML = contentHTML;
```

In this example, an {{HTMLElement("iframe")}} is created and filled with content, then a specific element within the document is scrolled into view in the frame. Once that's done, the vertical scroll position is checked by looking at the value of `pageYOffset` in the frame's {{domxref("HTMLIFrameElement.contentWindow", "contentWindow")}}.

### HTML

HTML은 단 두 개의 요소를 가진 짧은 코드입니다. 하나는 스크롤할 문서를 담은 {{HTMLElement("iframe")}}이고, 다른 하나는 스크롤을 끝냈을 때 `pageYOffset`의 값을 기록할 {{HTMLElement("div")}}입니다.

```html
<iframe id="frame"> </iframe>

<div id="info"></div>
```

### JavaScript

```js
var frame = document.getElementById("frame");
var frameDoc = frame.contentDocument;
var info = document.getElementById("info");

var target = frameDoc.getElementById("overview");
frameDoc.scrollingElement.scrollTop = target.offsetTop;

info.innerText =
  "스크롤 후 Y축 차이: " + frame.contentWindow.pageYOffset + " 픽셀";
```

The JavaScript code begins by getting into `frame` and `info` the `<iframe>` element that contains our content as well as the `<div>` element into which we'll output the result of our scroll position check. It then gets a reference to the element we want to scroll into view calling {{domxref("Document.getElementById", "getElementById()")}} on the frame's {{domxref("HTMLIFrameElement.contentDocument")}}.

With the target element in hand, we set the {{domxref("Element.scrollTop", "scrollTop")}} of the frame's {{domxref("Document.scrollingElement", "scrollingElement")}} to the {{domxref("Element.offsetTop", "offsetTop")}} of the target element. By doing so, we set the vertical scrolling position of the frame's document so that it's the same as the top edge of the target element.

This will automatically set the scrolling position to the maximum possible value if the attempted scroll would exceed the maximum. This prevents us from falling off the edge of the document. Nobody wants to know what's out there. There might be dragons.

```css hidden
iframe {
  width: 620px;
  height: 450px;
  border: 1px solid black;
}

#info {
  margin-top: 20px;
  font:
    16px "Open Sans",
    "Helvetica",
    "Arial";
}
```

### 결과

The result follows. Note that the frame's contents have been scrolled to show the section named "Overview", and that the value of the `pageYOffset` property is shown with the corresponding value.

{{EmbedLiveSample("예제", 650, 500)}}

## 명세

{{Specifications}}

## 브라우저 호환성

{{Compat}}

## 같이 보기

- {{domxref("Window.pageXOffset", "pageXOffset")}}
- {{domxref("Window.scrollY", "scrollY")}} and {{domxref("Window.scrollX", "scrollX")}}
- {{domxref("Window.scroll", "scroll()")}}, {{domxref("Window.scrollBy", "scrollBy()")}}, and {{domxref("window.scrollTo", "scrollTo()")}}

---
# Source: Web_JavaScript_Reference_Operators_delete.md
---
---
title: delete 연산자
slug: Web/JavaScript/Reference/Operators/delete
---

{{jsSidebar("Operators")}}

**`delete`** **연산자** 는 객체의 속성을 제거합니다. 제거한 객체의 참조를 어디에서도 사용하지 않는다면 나중에 자원을 회수합니다.

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

## 구문

```js
delete expression;
```

`expression`은 속성 참조여야 합니다. 예컨대,

```js
delete object.property;
delete object["property"];
```

### 매개변수

- `object`
  - : 객체의 이름, 또는 평가했을 때 객체를 반환하는 표현식.
- `property`
  - : 제거하려는 속성.

### 반환 값

`true`. 단, 비엄격 모드에서 속성이 {{jsxref("Object.prototype.hasOwnProperty", "자신의 속성", "", 0)}}이며 [설정 불가능](/ko/docs/Web/JavaScript/Reference/Errors/Cant_delete)한 경우 `false`.

### 예외

엄격 모드에서, 속성이 자신의 속성이며 설정 불가능한 경우 {{jsxref("TypeError")}}.

## 설명

일반적으로 생각하고 있는것과는 다르게 `delete` 는 메모리 해제에 관하여 직접적으로 어떠한 작업도 하지 않습니다. 메모리 관리는 breaking references를 통하여 간접적으로 일어납니다. 자세한 걸 알고 싶다면 [memory management](/ko/docs/Web/JavaScript/Memory_Management) 를 보세요.

**`delete`** 연산자는 오브젝트로 부터 해당 프로퍼티를 삭제합니다. 삭제를 하면 true를 반환, 아니면 false를 반환합니다. 그렇지만 아래 경우를 고려해야만 합니다.

- 만약 존재하지 않는 속성을 삭제하려고 하면 delete는 어떠한 작업도 없이 true를 반환합니다.
- 오브젝트의 프로토타입 체인에 같은 이름의 속성이 있다면, 삭제 후에, 오브젝트의 프로토타입체인을 통해 프로퍼티를 사용 할 수 있습니다. (즉, `delete`는 오직 자신의 프로퍼티만 삭제 합니다.
- {{jsxref("Statements/var","var")}}로 선언된 어떠한 프로퍼티라도 글로벌 스코프나 펑션 스코프로부터 삭제될 수 없습니다.
  - 결국, `delete`는 글로벌 스코프의 어떤 함수도 삭제 할 수 없습니다. (함수 정의식이건 함수 표현식이건 삭제 불가)
  - 오브젝트의 속성으로 있는 함수인 경우(글로벌 스코프를 제외하고)는 `delete`로 삭제할 수 있습니다.

- {{jsxref("Statements/let","let")}}과 {{jsxref("Statements/const","const")}}로 선언한 속성은 어느 스코프에 정의되어 있건 삭제 할 수 없습니다.
- Non-configurable 속성은 삭제 할 수 없습니다. 이것은 {{jsxref("Math")}}, {{jsxref("Array")}}, {{jsxref("Object")}}와 같은 built-in objects의 속성들이나 {{jsxref("Object.defineProperty()")}} 같은 메소드로 만든 non-configurable속성들을 포함합니다.

간단한 예제입니다.

```js
var Employee = {
  age: 28,
  name: "abc",
  designation: "developer",
};

console.log(delete Employee.name); // returns true
console.log(delete Employee.age); // returns true

// 존재하지 않는 속성을 삭제하려하면
// true를 리턴합니다.
console.log(delete Employee.salary); // returns true
```

### 설정 불가능한 속성

non-configurable 속성은 `delete`로 삭제할 수 없으며, `false`를 반환할 것입니다(\*strict mode에서는 `SyntaxError`를 발생시킴).

```js
var Employee = {};
Object.defineProperty(Employee, "name", { configurable: false });

console.log(delete Employee.name); // returns false
```

{{jsxref("Statements/var","var")}}, {{jsxref("Statements/let","let")}}, {{jsxref("Statements/const","const")}}로 선언된 변수는 non-configurable 속성으로 구분되며, `delete`로 삭제될 수 없습니다.

```js
var nameOther = "XYZ";

// 우리는 이를 사용해 글로벌 속성에 접근 할 수 있습니다:
Object.getOwnPropertyDescriptor(window, "nameOther");

// output: Object { value: "XYZ",
//                  writable: true,
//                  enumerable: true,
//                  configurable: false }

// "nameOther"은 var로 선언되었기 때문에
// 이는 "non-configurable" 속성으로 구분됩니다.

delete nameOther; // return false
```

strict mode, this would have raised an exception.

### 엄격 vs. 비엄격 모드

엄격 모드에서 `delete`로 변수나 함수를 삭제하려고 하면 {{jsxref("SyntaxError")}}가 발생합니다.

`var`로 정의된 변수는 non-configurable로 구분됩니다. 다음 예제에서, `salary`는 non-configurable이며 삭제될 수 없습니다. non-strict mode에서 non-configurable에 `delete`를 쓰면 `false`를 반환합니다.

```js
function Employee() {
  delete salary;
  var salary;
}

Employee();
```

그러나 strict mode에서는 `false`를 반환하는 대신, `SyntaxError`를 발생시킵니다.

```js
"use strict";

function Employee() {
  delete salary; // SyntaxError
  var salary;
}

// 이와 마찬가지로, delete로 함수를 삭제하는 것도
// SyntaxError를 발생시킵니다.

function DemoFunction() {
  //some code
}

delete DemoFunction; // SyntaxError
```

## 예제

```js
// 전역스코프에 adminName라는 프로퍼티를 만듭니다.
adminName = "xyz";

// 전역스코프에 empCount라는 프로퍼티를 만듭니다.
// var를 사용해서 선언했으므로, 이는 non-configurable로 구분됩니다.
// let 이나 const를 사용하더라도 마찬가지로 non-configurable 입니다.
var empCount = 43;

EmployeeDetails = {
  name: "xyz",
  age: 5,
  designation: "Developer",
};

// adminName은 전역변수입니다.
// 이는 var를 사용하여 선언되지 않았기에 configurable하며 delete로 삭제될 수 있습니다.
delete adminName; // returns true

// 이와 반대로, empCount는 var를 사용하였기에 non-configurable이며
// 그러므로 delete로 삭제할 수 없습니다.
delete empCount; // returns false

// delete는 객체의 프로퍼티를 지울 때 사용됩니다.
delete EmployeeDetails.name; // returns true

// 해당 프로퍼티가 존재하지 않는 상황에서도 "true"를 리턴합니다.
delete EmployeeDetails.salary; // returns true

// 내장되어있는 정적 프로퍼티에는 delete가 영향을 미치지 않습니다.
delete Math.PI; // returns false

// EmployeeDetails 은 전역스코프의 프로퍼티 입니다.
// "var"를 사용하지 않고 선언되었기 때문에 이는 configurable입니다.
delete EmployeeDetails; // returns true

function f() {
  var z = 44;

  // 지역변수에는 delete가 영향을 미치지 않습니다.
  delete z; // returns false
}
```

### `delete`와 프로토타입 체인

In the following example, we delete an own property of an object while a property with the same name is available on the prototype chain:

```js
function Foo() {
  this.bar = 10;
}

Foo.prototype.bar = 42;

var foo = new Foo();

// Returns true, since the own property
// has been deleted on the foo object
delete foo.bar;

// foo.bar is still available, since it
// is available in the prototype chain.
console.log(foo.bar);

// We delete the property on the prototype
delete Foo.prototype.bar;

// logs "undefined" since the property
// is no longer inherited
console.log(foo.bar);
```

### 객체 요소 제거하기

When you delete an array element, the array length is not affected. This holds even if you delete the last element of the array.

When the `delete` operator removes an array element, that element is no longer in the array. In the following example, `trees[3]` is removed with `delete`.

```js
var trees = ["redwood", "bay", "cedar", "oak", "maple"];
delete trees[3];
if (3 in trees) {
  // this does not get executed
}
```

If you want an array element to exist but have an undefined value, use the `undefined` value instead of the `delete` operator. In the following example, `trees[3]` is assigned the value undefined, but the array element still exists:

```js
var trees = ["redwood", "bay", "cedar", "oak", "maple"];
trees[3] = undefined;
if (3 in trees) {
  // this gets executed
}
```

## 명세서

{{Specifications}}

## 브라우저 호환성

{{Compat}}

## 크로스 브라우저 참고사항

Although ECMAScript makes iteration order of objects implementation-dependent, it may appear that all major browsers support an iteration order based on the earliest added property coming first (at least for properties not on the prototype). However, in the case of Internet Explorer, when one uses `delete` on a property, some confusing behavior results, preventing other browsers from using simple objects like object literals as ordered associative arrays. In Explorer, while the property _value_ is indeed set to undefined, if one later adds back a property with the same name, the property will be iterated in its _old_ position--not at the end of the iteration sequence as one might expect after having deleted the property and then added it back.

If you want to use an ordered associative array in a cross-browser environment, use a {{jsxref("Map")}} object if available, or simulate this structure with two separate arrays (one for the keys and the other for the values), or build an array of single-property objects, etc.

## 같이 보기

- [In depth analysis on delete](http://perfectionkills.com/understanding-delete/)
- {{jsxref("Reflect.deleteProperty()")}}
- {{jsxref("Map.prototype.delete()")}}

---
# Source: Web_Accessibility_ARIA_Roles_dialog_role.md
---
---
title: "ARIA: dialog role"
slug: Web/Accessibility/ARIA/Roles/dialog_role
---

{{draft()}}

{{ariaref}}

[`dialog`](http://www.w3.org/TR/2009/WD-wai-aria-20091215/roles#dialog) 역할(role)은 HTML 기반의 애플리케이션의 다이얼로그 또는 콘텐츠를 분리하는 창 또는 다른 웹 애플리케이션의 UI 혹은 페이지를 마크업하는데 사용됩니다. 다이얼로그는 일반적으로 오버레이를 사용하여 페이지 위에 표시됩니다. 다이얼로그는 비모달(non-modal) (열린 이후에도 다이얼로그 바깥의 콘텐츠와 상호작용할 수 있습니다) 또는 모달(오로지 다이얼로그 콘텐츠와 상호작용할 수 있습니다) 형태일 수 있습니다.

```html
<div
  role="dialog"
  aria-labelledby="dialog1Title"
  aria-describedby="dialog1Desc">
  <h2 id="dialog1Title">귀하의 개인정보가 성공적으로 갱신되었습니다.</h2>
  <p id="dialog1Desc">
    <a href="/account">개인정보 관리</a> 페이지에서 언제든지 개인정보를 수정할
    수 있습니다.
  </p>
  <button>닫기</button>
</div>
```

## 설명

다이얼로그 요소를 마크업하는 것은 보조 기술(Assistive Technology)이 다이얼로그의 콘텐츠가 그룹하 되어 페이지의 나머지 콘텐츠와 분리됨을 식별하는 것을 돕습니다. 하지만, 단순히 `role="dialog"`를 추가하는 것으로 다이얼로그의 접근성을 높이지 못합니다. 추가적으로 다음 항목들이 충족되어야 합니다:

- 다이얼로그의 레이블이 올바르게 지정되어야 합니다.
- 키보드 포커스가 올바르게 관리되어야 합니다.

아래 섹션들은 이 두가지 요구 사항을 어떻게 만족시킬 수 있을지 설명합니다.

#### 레이블링

다이얼로그 요소 자체가 포커스를 가질 필요는 없지만, 여전히 레이블링을 할 필요가 있습니다. 다이얼로그에 주어진 레이블은 다이얼로그 내 상호작용 가능한 컨트롤들에 contextual information를 제공합니다. 예를 들어, 다이얼로그의 레이블은 내부의 컨트롤들의 레이블의 그롭화된 레이블처럼 작동합니다. (`<legend>` 요소가 내부의 `<fieldset>` 요소에 그룹화된 레이블을 제공하는 것과 비슷합니다)

만약 다이얼로그가 이미 눈에 보이는 타이틀바를 가지고 있다면, 그 안속의 텍스트는 다이얼로그를 레이블하는데 사용될 수 있습니다. 이를 이루기 위해 `role="dialog"` 속성을 가진 요소에 `aria-labelledby` 속성을 사용합니다. 또한, 만약 다이얼로그에 제목 외의 추가적인 설명 텍스트가 있다면, 그 텍스트는 `aria-describedby` 속성을 사용하여 다이얼로그에 관련되게 만들 수 있습니다. 이러한 방법은 아래 코드를 통해 확인하실 수 있습니다:

```html
<div
  role="dialog"
  aria-labelledby="dialog1Title"
  aria-describedby="dialog1Desc">
  <h2 id="dialog1Title">귀하의 개인정보가 성공적으로 갱신되었습니다.</h2>
  <p id="dialog1Desc">
    <a href="/account">개인정보 관리</a> 페이지에서 언제든지 개인정보를 수정할
    수 있습니다.
  </p>
  <button>닫기</button>
</div>
```

> **참고:** 비가상 모드에서 작동하는 스크린 판독기에 의해 인지되기 위해서는 다이얼로그 제목과 설명 텍스트가 포커스가 가능하지 않아야 한다는 점을 유의하십시오. ARIA 다이얼로그 역할과 레이블링 기술은 다이얼로그로 포커스가 이동하였을 때 스크린 판독기가 다이얼로그의 정보를 인지할 수 있도록 합니다.

#### Focus management 포커스 관리

다이얼로그는 키보드 포커스를 관리하는 방법에 대한 특별한 요구 사항이 있습니다.

- 다이얼로그는 최소한 한 개 이상의 포커스 가능한 컨트롤이 있어야 합니다. 대부분의 다이얼로그는 "닫기", "확인" 또는 "취소"와 같은 버튼들이 존재합니다. 더 나아가 폼 또는 탭 같은 위젯 컨테이너 등 얼마든지 포커스 가능한 요소들을 가질 수 있습니다.
- 다이얼로그가 화면에 나타났을 때, 다이얼로그 안의 기본 포커스 가능한 컨트롤로 키보드 포커스를 이동시켜야 합니다. 예를 들어 간단한 메시지만을 제공하는 다이얼로그라면 "확인" 버튼이, 폼을 제공하는 다이얼로그의 경우는 폼의 첫 번째 필드가 기본으로 포커스 될 것입니다.
- 다이얼로그가 닫힌 이후, 키보드 포커스는 다이얼로그를 열기 전에 있었던 곳으로 다시 이동해야 합니다. 그렇지 않으면 포커스가 페이지의 첫 번째 부분으로 초기화될 수 있습니다.
- 대부분의 다이얼로그는 탭 순서가 _감싸지길_ 기대합니다. 이는 사용자가 다이얼로그 안의 마지막 포커스 가능한 요소에 도달했을 때, 탭을 누르면 첫 번째 포커스 가능한 요소로 포커스가 이동하길 원합니다. 즉, 탭 순서는 다이얼로그 안에 갇혀 있어야 합니다. (_역자 : "Focus Trap"으로 관련 자료들을 열람하실 수 있습니다_)
- 만약 다이얼로그가 움직이거나 크기가 변경될 수 있는 경우, 마우스를 사용하는 사용자가 수행하는 동작을 키보드를 사용하는 사용자도 거의 비슷하게 조작할 수 있도록 보장하십시오. 비슷하게, 만약 다이얼로그가 툴바 또는 context menus 처럼 특별한 기능을 제공하는 경우, 이들 또한 키보드 사용자에 의해서도 접근 가능하고 조작이 가능해야 합니다.
- 다이얼로그는 모달 또는 비모달일 수 있습니다. 만약 모달 다이얼로그가 화면에 나타나면, 다이얼로그 밖의 페이지 콘텐츠들과 상호작용하는 것은 불가능합니다. 다른 말로, 모달 다이얼로그가 나타나 있는한 메인 애플리케이션의 UI 또는 페이지 콘텐츠는 일시적으로 비활성화 상태여야 합니다. 비모달 다이얼로그는 열러 있는 동안에도 다이얼로그 바깥의 콘텐츠들과 상호작용이 가능합니다. 비모달 다이얼로그를 위해서 열려 있는 다이얼로그와 메인 페이지간에 포커스를 이동시킬 수 있는 전역 키보드 단축키가 필요하다는 점을 유의하십시오.

### 관련된 ARIA 역할, 상태 및 속성

- `aria-labelledby`
  - : 다이얼로그에 label을 하려면 이 속성을 사용하십시오. 보통, 다이얼로그의 제목 요소의 id값이 aria-labelledby 속성의 값이 됩니다.
- `aria-describedby`
  - : 다이얼로그의 콘텐츠를 묘사하기 위해 이 속성을 사용하십시오.

### Possible effects on user agents and assistive technology

When the `dialog` role is used, the user agent should do the following:

- Expose the element as a dialog in the operating system's accessibility API.

When the dialog is correctly labeled and focus is moved to a control inside the dialog, screen readers should announce the dialog's accessible role, name and optionally description before announcing the focused element.

> **참고:** Opinions may differ on how assistive technology should handle this technique. The information provided above is one of those opinions and therefore not normative.

### 예제

#### 예제 1: 폼을 포함하는 다이얼로그

```html
<div
  role="dialog"
  aria-labelledby="dialog1Title"
  aria-describedby="dialog1Desc">
  <h2 id="dialog1Title">구독하기</h2>
  <p id="dialog1Desc">우리는 이 정보를 제 3자에게 제공하지 않습니다.</p>
  <form>
    <p>
      <label for="firstName">이름</label>
      <input id="firstName" type="text" />
    </p>
    <p>
      <label for="lastName">성</label>
      <input id="lastName" type="text" />
    </p>
    <p>
      <label for="interests">관심분야</label>
      <textarea id="interests"></textarea>
    </p>
    <p>
      <input type="submit" value="정보 저장하기" />
    </p>
  </form>
</div>
```

#### Example 2: A dialog based on a Fieldset as fallback content

To support browsers or AT products that do not support ARIA mark up, it's also possible to use apply the dialog markup to a fieldset element as fallback content. This way the dialog title will still be announced correctly:

```html
<fieldset
  role="dialog"
  aria-labelledby="dialog1Title"
  aria-describedby="dialog1Desc">
  <legend>
    <span id="dialog1Title"
      >Your personal details were successfully updated.</span
    >
    <span id="dialog1Desc"
      >You can change your details at any time in the user account
      section.</span
    >
  </legend>

  <button>Close</button>
</fieldset>
```

#### 작업된 예제

- [jQuery-UI Dialog](http://jqueryui.com/demos/dialog/)

### Notes

> **참고:** While it is possible to prevent keyboard users from moving focus to elements outside of the dialog, screen reader users may still be able to navigate that content virtually to use their screen reader's virtual cursor. Because of this, dialogs are considered to be a special case of the application role: They are expected to be navigated by screen reader users in a non-virtual navigation mode.

### 사용되는 ARIA 속성

- [dialog](http://www.w3.org/TR/wai-aria/roles#dialog)
- [aria-labelledby](http://www.w3.org/TR/wai-aria/states_and_properties#aria-labelledby)
- [aria-describedby](http://www.w3.org/TR/wai-aria/states_and_properties#aria-describedby)

### 관련된 ARIA 기술

- [Using the alertdialog role](/en/ARIA/ARIA_Techniques/Using_the_alertdialog_role)

### Compatibility

TBD: Add support information for common UA and AT product combinations

### Additional resources

---
# Source: Web_Guide_Audio_and_video_delivery_Adding_captions_and_subtitles_to_HTML5_video.md
---
---
title: HTML5 영상에 캡션과 자막 붙이기
slug: Web/Guide/Audio_and_video_delivery/Adding_captions_and_subtitles_to_HTML5_video
---

우리는 다른 글에서 {{ domxref("HTMLMediaElement") }}과(와) {{ domxref("Window.fullScreen") }} API를 활용하여 [다양한 브라우저에서 호환되는 영상 플레이어를 제작하는 방법](/en-US/Apps/Build/Manipulating_media/cross_browser_video_player)과 [플레이어에 스타일을 적용하는 방법](/en-US/Apps/Build/Manipulating_media/Video_player_styling_basics)을 살펴보았습니다. 이번 글에서는 위에서 제작했던 플레이어를 활용하여 {{ domxref("Web_Video_Text_Tracks_Format","WebVTT 포맷 파일") }}과(와) {{ htmlelement("track") }} 엘리먼트를 이용해 캡션과 자막을 붙이는 방법을 살펴보려고 합니다.

## 캡션이 포함된 영상 예제

캡션이 포함된 영상 플레이어를 예시로 설명하기 위하여 [Blender Foundation](http://www.blender.org/foundation/)에서 만든 [Sintel open movie](http://www.sintel.org/)를 발췌하여 사용할 것입니다.

![Video player with stand controls such as play, stop, volume, and captions on and off. The video playing shows a scene of a man holding a spear-like weapon, and a caption reads "Esta hoja tiene pasado oscuro."](video-player-with-captions.png)

> **참고:** [소스코드](https://github.com/iandevlin/iandevlin.github.io/tree/master/mdn/video-player-with-captions)는 Github 에서 받을 수 있으며 [데모](http://iandevlin.github.io/mdn/video-player-with-captions/) 또한 확인해보실 수 있습니다.

## HTML5와 영상 캡션

영상에 캡션을 붙이는 법을 살펴보기 전에, 몇가지 짚고 넢어가야 할 것들이 있습니다.

### 캡션 vs 자막

[캡션과 자막은 다른 개념입니다](http://web.archive.org/web/20160117160743/http://screenfont.ca/learn/): 이 두가지는 명백히 다른 개념이며 서로 다른 정보를 전달합니다. 이 두가지에 대해 명확하게 이해하고 있지 않다면 두 개념의 차이를 먼저 이해하고 오는 것이 좋습니다. 개념적으로는 다르더라도 기술적으로는 같은 방식을 따르기 때문에, 이 글에서 설명하는 것은 두 개념 모두에 적용됩니다.

이 글에서는 화면에 보여지는 텍스트를 자막으로 간주하고 설명하고 있습니다. 여기서 자막은 영상의 언어를 이해하기 어려운 사람들을 위한 텍스트를 의미하며, 듣는 능력에 장애가 있는 사람들을 위한 텍스트를 의미하는 것은 아닙니다.

### \<track> 엘리먼트

HTML5에서는 {{ htmlelement("track") }}를 이용하여 자막을 특정해서 보여줄 수 있습니다. 엘리먼트에서 제공하는 다양한 속성을 이용하여 추가하려는 컨텐트 유형, 언어, 자막 파일 등을 지정할 수 있습니다.

### WebVTT

자막 데이터를 담고있는 파일은 특정한 파일 포맷을 따르는데, 이 글에서는 [Web Video Text Tracks](/ko/docs/HTML/WebVTT) (WebVTT)를 이용합니다. [WebVTT 스펙](http://dev.w3.org/html5/webvtt/) 은 아직 개발 단계에 있지만 대부분 주요 기능은 안정화 단계에 있기 떄문에 지금도 충분히 사용 가능합니다.

영상 제공자([Blender Foundation](http://www.blender.org/foundation/)같은)들은 영상과 함께 캡션과 자막을 텍스트 파일로 제공하는데 보통 SubRip Text(SRT) 포맷을 사용합니다. SRT 파일은 온라인에서 쉽게 찾을 수 있는 [srt2vtt](https://atelier.u-sub.net/srt2vtt/)같은 변환기를 이용해 WebVTT로 변환할 수 있습니다.

## HTML과 CSS 수정

이번 섹션에서는 영상에 자막을 추가하기 위하여 이전 글에서 작성했던 코드의 마크업을 수정해볼 것입니다. 혹시 이번 섹션은 별로 관심이 없거나 바로 JavaScript 혹은 직접적인 CSS를 수정하는데에 더 관심이 있다면, [Subtitle implementation](#subtitle_implementation) 섹션으로 건너뛰어도 무방합니다.

이번 예제에서는 [Sintel](http://www.sintel.org/)이라는 다른 영상을 사용해보겠습니다. 이 영상은 연설하는 내용을 담고있기 떄문에 자막이 동작하는 것을 이해하는데 훨씬 더 적합할 것입니다.

### HTML 마크업

위에서 언급한대로, 자막 파일을 HTML5 영상에 추가하기 위해서는 새로운 HTML5 `<track>` 엘리먼트를 활용해야 합니다. 우리는 지금 3가지 다른 언어의 자막— 영어, 독일어, 스페인어 —을 가지고 있기 때문에 HTML5 `<video>` 엘리먼트 안에 `<track>` 엘리먼트를 추가하여 3가지 언어에 대응하는 VTT 파일을 지정해주어야 합니다.:

```html
<video id="video" controls preload="metadata">
  <source src="video/sintel-short.mp4" type="video/mp4" />
  <source src="video/sintel-short.webm" type="video/webm" />
  <track
    label="English"
    kind="subtitles"
    srclang="en"
    src="captions/vtt/sintel-en.vtt"
    default />
  <track
    label="Deutsch"
    kind="subtitles"
    srclang="de"
    src="captions/vtt/sintel-de.vtt" />
  <track
    label="Español"
    kind="subtitles"
    srclang="es"
    src="captions/vtt/sintel-es.vtt" />
</video>
```

위 코드에서 보듯, 각각의 `<track>` 엘리먼트는 다음의 속성 세트를 갖습니다:

- `subtitles`값을 갖고 있는 `kind` 는 해당 파일이 가지고 있는 내용의 유형을 가리킵니다.
- `label` 은 자막 세트가 갖는 언어를 상징하는 값입니다. — 예를 들어 `English` 혹은 `Deutsch` — 이 값들은 UI 상에서 사용자가 쉽게 원하는 자막을 선택할 수 있도록 보여지는데 사용됩니다.
- `src` 은 각 자막에 해당하는 WebVTT 파일 URL입니다.
- `srclang` 각 자막 파일의 언어 값을 가리킵니다.
- English `<track>` 엘리먼트에 지정되어있는 `default` 속성은 브라우저로 하여금 기본 자막 파일이라고 알려주는 역할을 합니다. 자막 설정은 켜져있고 사용자가 아무런 선택도 하지 않을 경우 기본으로 보여질 자막을 의미합니다.

In addition to adding the `<track>` elements, we have also added a new button to control the subtitles menu that we will build. As a consequence, the video controls now look as follows:

```js
<div id="video-controls" class="controls" data-state="hidden">
  <button id="playpause" type="button" data-state="play">
    Play/Pause
  </button>
  <button id="stop" type="button" data-state="stop">
    Stop
  </button>
  <div class="progress">
    <progress id="progress" value="0" min="0">
      <span id="progress-bar"></span>
    </progress>
  </div>
  <button id="mute" type="button" data-state="mute">
    Mute/Unmute
  </button>
  <button id="volinc" type="button" data-state="volup">
    Vol+
  </button>
  <button id="voldec" type="button" data-state="voldown">
    Vol-
  </button>
  <button id="fs" type="button" data-state="go-fullscreen">
    Fullscreen
  </button>
  <button id="subtitles" type="button" data-state="subtitles">
    CC
  </button>
</div>
```

### CSS Changes

The video controls have undergone some minor changes in order to make space for the extra button, but these are relatively straightforward.

No image is used for the captions button, so it is simply styled as:

```css
.controls button[data-state="subtitles"] {
  height: 85%;
  text-indent: 0;
  font-size: 16px;
  font-size: 1rem;
  font-weight: bold;
  color: #666;
  background: #000;
  border-radius: 2px;
}
```

There are also other CSS changes that are specific to some extra JavaScript implementation, but these will be mentioned at the appropriate place below.

## Subtitle implementation

A lot of what we do to access the video subtitles revolves around JavaScript. Similar to the video controls, if a browser supports HTML5 video subtitles, there will be a button provided within the native control set to access them. However, since we have defined our own video controls, this button is hidden, and we need to define our own.

Browsers do vary as to what they support, so we will be attempting to bring a more unified UI to each browser where possible. There's more on browser compatibility issues later on.

### Initial setup

As with all the other buttons, one of the first things we need to do is store a handle to the subtitles' button:

```js
var subtitles = document.getElementById("subtitles");
```

We also initially turn off all subtitles, in case the browser turns any of them on by default:

```js
for (var i = 0; i < video.textTracks.length; i++) {
  video.textTracks[i].mode = "hidden";
}
```

The `video.textTracks` property contains an array of all the text tracks attached to the video. We loop through each one and set its `mode` to `hidden`.

Note: The [WebVTT API](http://dev.w3.org/html5/webvtt/#api) gives us access to all the text tracks that are defined for an HTML5 video using the `<track>` element.

### Building a caption menu

Our aim is to use the `subtitles` button we added earlier to display a menu that allows users to choose which language they want the subtitles displayed in, or to turn them off entirely.

We have added the button, but before we make it do anything, we need to build the menu that goes with it. This menu is built dynamically, so that languages can be added or removed later by simply editing the `<track>` elements within the video's markup.

All we need to do is to go through the video's `textTracks`, reading their properties and building the menu up from there:

```js
var subtitlesMenu;
if (video.textTracks) {
  var df = document.createDocumentFragment();
  var subtitlesMenu = df.appendChild(document.createElement("ul"));
  subtitlesMenu.className = "subtitles-menu";
  subtitlesMenu.appendChild(createMenuItem("subtitles-off", "", "Off"));
  for (var i = 0; i < video.textTracks.length; i++) {
    subtitlesMenu.appendChild(
      createMenuItem(
        "subtitles-" + video.textTracks[i].language,
        video.textTracks[i].language,
        video.textTracks[i].label,
      ),
    );
  }
  videoContainer.appendChild(subtitlesMenu);
}
```

This code creates a {{ domxref("documentFragment") }}, which is used to hold an unordered list containing our subtitles menu. First of all an option is added to allow the user to switch all subtitles off, and then buttons are added for each text track, reading the language and label from each one.

The creation of each list item and button is done by the `createMenuItem()` function, which is defined as follows:

```js
var subtitleMenuButtons = [];
var createMenuItem = function (id, lang, label) {
  var listItem = document.createElement("li");
  var button = listItem.appendChild(document.createElement("button"));
  button.setAttribute("id", id);
  button.className = "subtitles-button";
  if (lang.length > 0) button.setAttribute("lang", lang);
  button.value = label;
  button.setAttribute("data-state", "inactive");
  button.appendChild(document.createTextNode(label));
  button.addEventListener("click", function (e) {
    // Set all buttons to inactive
    subtitleMenuButtons.map(function (v, i, a) {
      subtitleMenuButtons[i].setAttribute("data-state", "inactive");
    });
    // Find the language to activate
    var lang = this.getAttribute("lang");
    for (var i = 0; i < video.textTracks.length; i++) {
      // For the 'subtitles-off' button, the first condition will never match so all will subtitles be turned off
      if (video.textTracks[i].language == lang) {
        video.textTracks[i].mode = "showing";
        this.setAttribute("data-state", "active");
      } else {
        video.textTracks[i].mode = "hidden";
      }
    }
    subtitlesMenu.style.display = "none";
  });
  subtitleMenuButtons.push(button);
  return listItem;
};
```

This function builds the required {{ htmlelement("li") }} and {{ htmlelement("button") }} elements, and returns them so they can be added to the subtitles menu list. It also sets up the required event listeners on the button to toggle the relevant subtitle set on or off. This is done by simply setting the required subtlte's `mode` attribute to `showing`, and setting the others to `hidden`.

Once the menu is built, it is then inserted into the DOM at the bottom of the videoContainer.

Initially the menu is hidden by default, so an event listener needs to be added to our subtitles button to toggle it:

```js
subtitles.addEventListener("click", function (e) {
  if (subtitlesMenu) {
    subtitlesMenu.style.display =
      subtitlesMenu.style.display == "block" ? "none" : "block";
  }
});
```

### Subtitle menu CSS

We also added some rudimentary styling for the newly created subtitles menu:

```css
.subtitles-menu {
  display: none;
  position: absolute;
  bottom: 14.8%;
  right: 20px;
  background: #666;
  list-style-type: none;
  margin: 0;
  padding: 0;
  width: 100px;
  padding: 10px;
}

.subtitles-menu li {
  padding: 0;
  text-align: center;
}

.subtitles-menu li button {
  border: none;
  background: #000;
  color: #fff;
  cursor: pointer;
  width: 90%;
  padding: 2px 5px;
  border-radius: 2px;
}
```

## Styling the displayed subtitles

One of the less well known about and supported features of WebVTT is the ability to style the individual subtitles (something called text cues) via [CSS Extensions](http://dev.w3.org/html5/webvtt/#css-extensions).

The `::cue` pseudo-element is the key to targetting individual text track cues for styling, as it matches any defined cue. There are only a handful of CSS properties that can be applied to a text cue:

- {{ cssxref("color") }}
- {{ cssxref("opacity") }}
- {{ cssxref("visibility") }}
- {{ cssxref("text-decoration") }}
- {{ cssxref("text-shadow") }}
- {{ cssxref("background") }} shorthand properties
- {{ cssxref("outline") }} shorthand properties
- {{ cssxref("font") }} shorthand properties, including {{ cssxref("line-height") }}
- {{ cssxref("white-space") }}

For example, to change the text colour of the text track cues you can write:

```css
::cue {
  color: #ccc;
}
```

If the WebVTT file uses [voice spans](http://dev.w3.org/html5/webvtt/#dfn-webvtt-cue-voice-span), which allow cues to be defined as having a particular "voice":

```
0
00:00:00.000 --> 00:00:12.000
<v Test>[Test]</v>
```

Then this specific 'voice' will be stylable like so:

```css
::cue(v[voice="Test"]) {
  color: #fff;
  background: #0095dd;
}
```

> **참고:** Some of the styling of cues with ::cue currently works on Chrome, Opera, and Safari, but not yet on Firefox.

## Browser Compatibility

[Browser support for WebVTT and the `<track>` element](http://caniuse.com/webvtt) is fairly good, although some browsers differ slightly in their implementation.

### Internet Explorer

Internet Explorer 10+ subtitles are enabled by default, and the default controls contain a button and a menu that offers the same functionality as the menu we just built. The `default` attribute is also supported.

> **참고:** IE will completely ignore WebVTT files unless you define the MIME type. This can easily be done by adding an `.htaccess` file to an appropriate directory that contains `AddType text/vtt .vtt`.

### Safari

Safari 6.1+ has similar support to Internet Explorer 10+, displaying a menu with the different available options, with the addition of an "Auto" option, which allows the browser to choose.

### Chrome and Opera

These browsers have similar implementations again: subtitles are enabled by default and the default control set contains a 'cc' button that turns subtitles on and off. Chrome and Opera ignore the `default` attribute on the `<track>` element and will instead try to match the browser's language to the subtitle's language.

### Firefox

Firefox's implementation was completely broken due to a [bug](https://bugzilla.mozilla.org/show_bug.cgi?id=981280), leading to Mozilla turning off WebVTT support by default (you can turn it on via the `media.webvtt.enabled` flag.) However, ~~this bug looks to have been fixed and WebVTT support re-enabled as of Gecko 31, so this will not be a problem for Firefox final release users for much longer (on Gecko 29 as of the time of this writing)~~ this has been fixed as of Firefox 31, and everything works as it should.

## Plugins

If, after reading through this article you decide that you can't be bothered to do all of this and want someone else to do it for you, there are plenty of plugins out there that offer caption and subtitle support that you can use.

- [plyr.io](http://plyr.io)
  - : This modern video player implements subtitles in both SRT and WebVTT file formats.
- [playr](http://www.delphiki.com/html5/playr/)
  - : This small plugin implements subtitles, captions, and chapters as well as both WebVTT and SRT file formats.
- [Flowplayer](https://flowplayer.org/player/)
  - : HTML5 player supporting WebVTT.
- [jwplayer](http://www.jwplayer.com/)
  - : This video player is very extensive and does a lot more than simply support video captions. It supports the WebVTT, SRT and DFXP formats.
- [MediaElement.js](http://mediaelementjs.com/)
  - : Another complete video player that also support video captions, albeit only in SRT format.
- [LeanBack Player](http://www.leanbackplayer.com/)
  - : Yet another video player that supports WebVTT captions as well as providing other standard player functionality.
- [SublimeVideo](http://sublimevideo.net)
  - : This player also supports captions through WebVTT and SRT files.
- [Video.js](http://www.videojs.com/)
  - : Supports WebVTT video subtitles.
- [Radiant Media Player](https://www.radiantmediaplayer.com)
  - : Supports multi-languages WebVTT closed captions

> **참고:** You can find an excellent list of HTML5 Video Players and their current "state" at [HTML5 Video Player Comparison](http://praegnanz.de/html5video/).

---
# Source: Web_API_HTML_Drag_and_Drop_API_Drag_operations.md
---
---
title: Drag Operations
slug: Web/API/HTML_Drag_and_Drop_API/Drag_operations
---

{{DefaultAPISidebar("HTML Drag and Drop API")}}

다음은 드래그 & 드랍(drag & drop) 동작 실행 시 각 단계에 대한 설명입니다.

> **참고:** 이 문서에 설명된 드래그 동작은 {{domxref("DataTransfer")}} 인터페이스를 사용합니다. 이 문서에서는 {{domxref("DataTransferItem")}} 인터페이스나 {{domxref("DataTransferItemList")}} 인터페이스를 사용하지 않습니다.

## Draggable 속성

웹 페이지 안에서 특정 상황에 기본 드래그(default drag) 행위가 사용될 경우가 있습니다. 선택된 텍스트(text selections), 이미지 또는 링크가 여기에 포함됩니다. 이미지나 링크가 드래그될 때, 이미지나 링크의 URL이 드래그 데이터(drag data)로 설정되고 드래그가 시작됩니다. 다른 요소의 경우, 기본 드래그가 발생할 선택(selections)에 포함되어 있어야 합니다(For other elements, they must be part of a selection for a default drag to occur). 이 효과를 보기 위해서는 웹 페이지의 어떤 영역을 선택하고 마우스를 클릭한 채로 드래그하면 됩니다. 드래그가 발생할 때 마우스 포인터로 선택 영역에 대한 OS별 렌더링이 표시됩니다. 이 행위는 기본 드래그 행위인 경우에만 발생하는 것으로 드래그되는 데이터를 조정할 리스너가 없는 경우에는 작동하지 않습니다.

HTML에서 이미지나 링크 그리고 선택(selections)에 대한 기본 행위를 제외한 나머지 요소는 기본적으로 드래그되지 않습니다. [XUL](/ko/docs/Mozilla/Tech/XUL)에서는 모든 요소가 드래그 가능합니다.

다른 HTML 요소를 드래그할 수 있게 하려면 세 가지가 이루어져야 합니다:

- 드래그가 가능하도록 만들고자 하는 요소에 대한 `[`draggable`](/ko/docs/Web/HTML/Global_attributes#draggable)` 속성이 `true`로 설정되어야 합니다.
- `{{event("dragstart")}}` 이벤트에 대한 리스너를 추가합니다.
- 위에서 정의한 리스너에 {{domxref("DataTransfer.setData","Set the drag data")}}를 설정합니다.

컨텐츠의 일부 영역을 드래그할 수 있도록 만드는 예제는 다음과 같습니다.

```html
<div
  draggable="true"
  ondragstart="event.dataTransfer.setData('text/plain', 'This text may be dragged')">
  This text <strong>may</strong> be dragged.
</div>
```

요소를 드래그할 수 있게 하기 위해서는 `[`draggable`](/ko/docs/Web/HTML/Global_attributes#draggable)` 속성이 true로 설정되어야 합니다. 이 속성이 생략되거나 false로 설정되면 해당 요소는 드래그할 수 없으며, 대신 텍스트가 선택됩니다. `[`draggable`](/ko/docs/Web/HTML/Global_attributes#draggable)` 속성은 이미지나 링크를 포함한 어떤 요소에서도 사용할 수 있습니다. 하지만, 이미지나 링크에 대해서는 기본값이 true로 설정되어 있으므로 이들 요소에 대해 드래깅할 수 없게 만들 경우에만 `[`draggable`](/ko/docs/Web/HTML/Global_attributes#draggable)` 속성의 값을 false로 설정하면 됩니다.

어떤 요소가 드래그 가능한 경우, 해당 요소 내의 텍스트나 다른 요소는 마우스를 클릭하고 드래그하는 통상적인 방식으로는 선택할 수 없게 됩니다. 대신, 사용자가 <kbd>alt</kbd> 키를 누른채로 마우스로 텍스트를 선택하거나 키보드를 이용해 선택할 수 있습니다.

XUL 요소에 대해서는 `[`draggable`](/ko/docs/Web/HTML/Global_attributes#draggable)` 속성을 사용할 필요가 없으며, 모든 XUL 요소는 드래그가 가능합니다.

```html
<button
  label="Drag Me"
  ondragstart="event.dataTransfer.setData('text/plain', 'Drag Me Button');"></button>
```

## 드래그 작업 시작

이 예제에서는 `{{domxref("GlobalEventHandlers.ondragstart","ondragstart")}}` 속성을 이용하여 {{event("dragstart")}} 이벤트에 대한 리스너를 추가합니다.

```html
<div
  draggable="true"
  ondragstart="event.dataTransfer.setData('text/plain', 'This text may be dragged')">
  This text <strong>may</strong> be dragged.
</div>
```

사용자가 드래그를 시작할 때, {{event("dragstart")}} 이벤트가 발생합니다. 이 예제에서는 드래그할 요소에 {{event("dragstart")}} 리스너가 추가되었습니다; 하지만, 대부분의 다른 이벤트가 그렇듯이 상위 요소에서 드래그 이벤트를 포착할 수 있습니다. {{event("dragstart")}} 이벤트 내에서 아래에서 설명하는 바와 같이 피드백 이미지(feedback image)나 드래그 효과와 그리고 드래그 데이터를 명시할 수 있습니다. 기본 이미지나 드래그 효과는 대부분의 상황에 적합하게 되어 있으며, 드래그 데이터만 필요합니다.

## 데이터 드래그

모든 {{domxref("DragEvent","drag events")}}는 드래그 데이터를 가지고 있는 {{domxref("DragEvent.dataTransfer","dataTransfer")}}라는 속성이 존재합니다 (`dataTransfer`는 {{domxref("DataTransfer")}} 객체입니다).

드래그가 발생할 때, 데이터는 어떤 것이 드래그되는지를 구분할 수 있는 드래그와 연관되어야 합니다(When a drag occurs, data must be associated with the drag which identifies _what_ is being dragged). 예를 들어, 선택된 텍스트가 드래그될 경우 드래그 데이터 항목에 연관된 데이터는 텍스트 자체입니다. 이와 유사하게, 웹 페이지 상의 링크가 드래그될 경우에 드래그 데이터 항목은 링크의 URL이됩니다.

{{domxref("DataTransfer","drag data")}}는 두 가지 정보를 담고 있는데, 데이터의 유형(또는 형식)과 데이터 값입니다. 형식은 (텍스트 데이터에 해당하는 [text/plain](/ko/docs/DragDrop/Recommended_Drag_Types#text)과 같은) 형식 문자열(type string) 값이고, 값은 텍스트의 문자열입니다. 드래그가 시작되면, 데이터와 형식을 제공하는 데이터를 추가해야 합니다. 드래그되는 동안, `{{event("dragenter")}}` 이벤트와 `{{event("dragover")}}` 이벤트에 대한 이벤트 리스너에서 드래그되는 데이터의 형식을 사용해 드랍이 허용되는지 확인할 수 있습니다. 예를 들어, 링크가 허용되는 드랍 대상(drop target)은 [text/uri-list](/ko/docs/DragDrop/Recommended_Drag_Types#link) 형식의 링크인지 확인합니다. 드랍 이벤트 동안 리스너는 드래그 대상(being dragged)으로부터 데이터를 추출해 드랍되는 위치에 삽입합니다.

{{domxref("DataTransfer","drag data's")}}의 {{domxref("DataTransfer.types","types")}} 속성은 [text/plain](/ko/docs/DragDrop/Recommended_Drag_Types#text) or [image/jpeg](/ko/docs/DragDrop/Recommended_Drag_Types#image)과 같은 {{domxref("DOMString")}} MIME-type 목록을 반환홥니다. 여러분은 자신만의 형식을 만들 수도 있습니다. 가장 흔하게 사용되는 형식은 권장 드래그 데이터 형식([Recommended Drag Types](/ko/docs/DragDrop/Recommended_Drag_Types))에서 소개하고 있습니다.

드래그에는 여러 가지 다른 형식의 데이터 항목이 포함될 수 있습니다. 이를 통해 사용자 정의 형식(custom types)과 같은 보다 특정한 형식의 데이터를 주로 제공하지만, 특정한 유형을 지원하지 않는 드롭 대상에 대해 대체 데이터(fallback data)를 제공할 수도 있습니다. [text/plain](/ko/docs/DragDrop/Recommended_Drag_Types#text) 형식의 일반적인 텍스트 데이터가 가장 단순한 형식의 데이터일 것입니다.이 형식의 데이터는 단순히 텍스트 형식으로 표시될 것입니다.

{{domxref("DragEvent.dataTransfer","dataTransfer")}} 내에 드래그 데이터 항목(drag data item)을 설정하기 위해서는 {{domxref("DataTransfer.setData","setData()")}} 메서드를 이용합니다. 이 메서드는 각각 데이터 형식과 데이터 값인 두 개의 인자가 필요합니다. 예를 들어:

```js
event.dataTransfer.setData("text/plain", "Text to drag");
```

이 경우, 데이터 값은 "Text to drag"이고 형식은 [text/plain](/ko/docs/DragDrop/Recommended_Drag_Types#text)입니다.

여러 형식의 데이터를 제공할 수도 있습니다. 이를 위해서는 서로 다른 형식으로 {{domxref("DataTransfer.setData","setData()")}} 메서드를 여러 번 호출합니다. 이 때, 가장 세부적인 형식에서 덜 세부적인 형식의 순으로 호출해야 합니다.

```js
var dt = event.dataTransfer;
dt.setData("application/x-bookmark", bookmarkString);
dt.setData("text/uri-list", "http://www.mozilla.org");
dt.setData("text/plain", "http://www.mozilla.org");
```

여기서 데이터는 세가지 유형으로 추가됩니다. 첫번째 형식의 'application2x-bookmark'는 사용자 지정 형식입니다. 다른 응용 프로그램에서는 이 형식을 지원하지 않지만 동일한 사이트 또는 응용 프로그램의 영역 간 드래그할 경우, 이 사용자 지정 형식을 사용할 수 있습니다. 또한 다른 형식의 데이터를 제공함으로써 덜 세부적인 형태로 다른 애플리케이션으로의 드래그도 지원할 수 있습니다. 다른 형식이 하나의 URL또는 텍스트 형식만 제공할 때, 'application2x-bookmark' 형식은 해당 어플리케이션 내에서 사용될 경우 더 상세한 데이터를 제공할 수 있습니다

이 예제에서 [text/uri-list](/ko/docs/DragDrop/Recommended_Drag_Types#link)와 [text/plain](/ko/docs/DragDrop/Recommended_Drag_Types#text)은 동일한 데이터를 담고있음에 주목하시기 바랍니다. 이렇게 해도 되지만, 꼭 이럴 필요는 없습니다.

동일한 형식으로 데이터를 두 번 추가하려고 하면 새로운 데이터가 기존 데이터를 대체하지만 형식 목록 내에서 이전 데이터(old data)와 같은 위치에 있게 됩니다.

{{domxref("DataTransfer.clearData","clearData()")}} 메서드를 이용해 해당 데이터를 지울 수 있는데, 이 메서드는 지우고자 하는 데이터의 형식을 인자로 가집니다.

```js
event.dataTransfer.clearData("text/uri-list");
```

{{domxref("DataTransfer.clearData","clearData()")}} 메서드에 대한 형식 인자는 선택적입니다. 형식을 지정하지 않으면 모든 형식과 연관된 데이터가 지워집니다. 드래그할 때, 드래그 데이터 항목이 없거나 이후에 모든 항목이 삭제되면 드래그가 발생하지 않습니다.

## 드래그 피드백 이미지 설정

드래그가 발생할 때, 드래그 대상("{{event("dragstart")}}" 이벤트가 발생한 요소)으로부터 반투명한 이미지가 생성되고 드래그 하는 동안 마우스 포인터를 따라 움직입니다. 이 이미지는 자동으로 생성되며, 따로 생성할 필요가 없습니다. 하지만, {{domxref("DataTransfer.setDragImage","setDragImage()")}}를 이용해 사용자 정의 드래그 피드백 이미지를 지정할 수 있습니다.

```js
event.dataTransfer.setDragImage(image, xOffset, yOffset);
```

세 개의 인자는 필수입니다. 첫 번째 인자는 이미지에 대한 참조(reference)입니다. 이 참조는 일반적으로 이미지에 대한 참조이나 캔버스(canvas)나 다른 요소를 지정할 수도 있습니다. 피드백 이미지는 단순하게 화면에 표시된 이미지의 모양으로부터 생성되지만, 이미지의 경우 원래 크기로 그려집니다. {{domxref("DataTransfer.setDragImage","setDragImage()")}} 메서드의 두 번째와 세 번째 인자는 마우스 포인터에 대해 상대적인 옵셋(offsets)으로 이미지가 나타날 위치를 의미합니다.

문서 내에 있지 않은 이미지나 캔버스를 사용하는 것 역시 가능합니다. 이 기법은 다음의 예제와 같이 캔버스 요소를 이용해 드래그 이미지를 사용자 정의 형태로 그리고자 할 때 유용합니다:

```js
function dragWithCustomImage(event) {
  var canvas = document.createElementNS(
    "http://www.w3.org/1999/xhtml",
    "canvas",
  );
  canvas.width = canvas.height = 50;

  var ctx = canvas.getContext("2d");
  ctx.lineWidth = 4;
  ctx.moveTo(0, 0);
  ctx.lineTo(50, 50);
  ctx.moveTo(0, 50);
  ctx.lineTo(50, 0);
  ctx.stroke();

  var dt = event.dataTransfer;
  dt.setData("text/plain", "Data to Drag");
  dt.setDragImage(canvas, 25, 25);
}
```

이 예제에서, 드래그 이미지를 표시할 캔버스를 하나 생성합니다. 캔버스는 너비가 와 높이가 모두 50 픽셀이고, 마우스 포인터가 이미지의 중앙에 위치하도록 옵셋(offsets)을 너비와 높이의 절반(25)으로 설정했습니다.

## 드래그 효과

드래그할 때, 여러 가지 작업이 수행될 수 있습니다. `copy` 작업은 드래그되는 데이터가 현재 위치에서 드랍되는 위치로 복사될 것임을 나타냅니다. `move` 작업은 드래그되는 데이터가 이동될 것임을 나타내고, `link` 작업은 특정 형태의 관계(relationship)나 연결(connection)이 소스와 드랍되는 위치 사이에 생성될 것임을 나타냅니다.

드래그 소스(drag source)에 대해 `{{event("dragstart")}}` 이벤트 리스너의 {{domxref("DataTransfer.effectAllowed","effectAllowed")}} 속성을 설정함으로써, 이 세 가지 작업 중 어떤 것을 허용할 것인지를 지정할 수 있습니다.

```js
event.dataTransfer.effectAllowed = "copy";
```

이 예제에서는, 복사만 허용됩니다. 다양한 방식으로 값을 조합할 수 있습니다:

- none
  - : 어떤 작업도 허용하지 않음.
- copy
  - : 복사만 허용
- move
  - : 이동만 허용
- link
  - : 연결만 허용
- copyMove
  - : 복사 또는 이동만 허용
- copyLink
  - : 복사 또는 연결만 허용
- linkMove
  - : 연결 또는 이동만 허용
- all
  - : 복사, 이동 및 연결 모두 허용

이 값들은 반드시 위에 나열한 것과 정확하게 일치해야 함에 유의하시기 바랍니다. 예를 들어, {{domxref("DataTransfer.effectAllowed","effectAllowed")}} 속성을 `copyMove`로 설정하면 복사와 이동 작업이 허용되나 연결(link) 작업은 금지됩니다. {{domxref("DataTransfer.effectAllowed","effectAllowed")}} 속성을 변경하지 않으면 'all' 값과 마찬가지로 어떤 작업도 허용됩니다. 따라서, 특정한 유형의 작업을 제외시키고 싶지 않다면 이 속성을 조정할 필요가 없습니다.

드래그 작업 중에 `{{event("dragenter")}}` 또는 `{{event("dragover")}}` 이벤트에 대한 리스너는 어떤 작업이 허용되어 있는지 알기 위해 {{domxref("DataTransfer.effectAllowed","effectAllowed")}} 속성을 확인할 수 있습니다. 관련된 속성으로, {{domxref("DataTransfer.dropEffect","dropEffect")}}는 이들 이벤트 중 하나에서 수행되어야 하는 단일 작업을 지정하기 위해 설정되어야 할 속성입니다. {{domxref("DataTransfer.dropEffect","dropEffect")}}에 유효한 값은 `none`, `copy`, `move`, 또는 `link`입니다. 이 속성에 값의 조합은 허용되지 않습니다.

`{{event("dragenter")}}`나 `{{event("dragover")}}` 이벤트가 발생하면 사용자가 요청하는 효과로 {{domxref("DataTransfer.dropEffect","dropEffect")}} 속성이 초기화됩니다. 사용자는 한정자 키를 눌러 원하는 효과로 수정할 수 있습니다. 플랫폼에 따라 정확한 키가 달라질 수 있지만, 일반적으로 쉬프트(Shift)와 컨트롤(Control) 키가 복사하기, 이동하기, 연결하기 간 전환에 사용됩니다. 마우스 포인터를 원하는 작업을 나타내도록 변경할 수 있습니다; 예를 들어, 복사 작업에 대해서는 마우스 포인터 옆에 더하기 기호가 표시된 커서가 나타날 수 있습니다.

`{{event("dragenter")}}` 또는 `{{event("dragover")}}` 이벤트가 발생하는 동안 {{domxref("DataTransfer.dropEffect","dropEffect")}} 속성을 변경할 수 있는데, 예를 들자면, 특정 작업만 지원되는 특수한 드랍 대상(drop target)일 경우가 그렇습니다. {{domxref("DataTransfer.dropEffect","dropEffect")}} 속성을 수정하여 사용자 효과(user effect)를 오버라이드하여 특정한 드랍 작업이 발생하게 할 수 있습니다. 이 효과는 {{domxref("DataTransfer.effectAllowed","effectAllowed")}} 속성에 열거된 것 중의 하나 이어야 함에 유의하시기 바랍니다. 그렇지 않을 경우, 허용되는 대체 값으로 설정되게 됩니다.

```js
event.dataTransfer.dropEffect = "copy";
```

이 예제에서는 복사가 수행될 효과입니다.

이 경우에는 이벤트를 취소하지 않는 것이 좋지만 `none` 값을 사용하여 이 위치에서 드롭이 허용되지 않음을 나타낼 수 있습니다.

`{{event("drop")}}`와 `{{event("dragend")}}` 이벤트 내에서{{domxref("DataTransfer.dropEffect","dropEffect")}} 속성을 확인하면 최종적으로 어떤 효과가 선택되었는지를 알 수 있습니다. 선택된 효과가 "move"였다면, `{{event("dragend")}}` 이벤트 내에서 드래그 소스의 원본 데이터가 삭제되어야 합니다.

## 드랍 대상 지정하기

`{{event("dragenter")}}`와 `{{event("dragover")}}` 이벤트에 대한 리스너는 유효한 드랍 대상인지, 즉 드래그된 아이템이 드랍될 수 있는 곳인지를 나타내는데 사용할 수 있습니다. 웹 페이지 또는 어플리케이션의 대부분의 영역은 데이터를 드랍할 수 있는 유효한 영역이 아닙니다. 따라서, 이들 이벤트에 대한 기본적인 처리는 드랍을 허용하지 않는 것입니다.

드랍을 허용하길 원한다면, 해당 이벤트를 취소하는 기본 처리를 막아야 합니다. 속성 정의(attribute-defined) 이벤트 리스너로부터 `false`를 반환 받거나 해당 이벤트의 {{domxref("Event.preventDefault","preventDefault()")}} 메서드를 호출하면 됩니다. 후자는 별도의 스크립트에 정의된 함수에 더 적합합니다.

```html
<div ondragover="return false">
  <div ondragover="event.preventDefault()"></div>
</div>
```

`{{event("dragenter")}}` and `{{event("dragover")}}` 두 이벤트 모두에서 {{domxref("Event.preventDefault","preventDefault()")}} 메서드를 호출하는 것은 그 위치에 드랍이 허용되는 것을 나타냅니다. 하지만, 일반적으로 특정한 상황에서만, 예를 들자면 링크가 드래그될 때만 {{domxref("Event.preventDefault","preventDefault()")}} 메서드를 호출하길 원할 것입니다. 이렇게 하기 위해서는 조건을 확인하여 조건이 충족될 때에만 해당 이벤트를 취소하는 함수를 호출합니다. 조건이 충족되지 않을 경우, 이벤트를 취소하지 않으면 사용자가 마우스 버튼을 놓더라도 드랍은 발생하지 않을 것입니다.

data transfer의 드래그 데이터 형식에 따라 드랍을 허용하거나 기각하는 경우가 대부분일 것입니다(예를 들어, 이미지나 링크를 허용하거나 둘 다 허용하는 경우). 이렇게 하기 위해서는 이벤트의 {{domxref("DragEvent.dataTransfer","dataTransfer")}} 속성의 {{domxref("DataTransfer.types","types")}} 속성을 확인합니다. {{domxref("DataTransfer.types","types")}} 속성은 드래그가 시작될 때 추가된 형식 문자열의 배열을 반환하는데, 그 순서는 가장 세부적인 형식에서 가장 덜 세부적인 형식의 순서입니다.

```js
function contains(list, value) {
  for (var i = 0; i < list.length; ++i) {
    if (list[i] === value) return true;
  }
  return false;
}

function doDragOver(event) {
  var isLink = contains(event.dataTransfer.types, "text/uri-list");
  if (isLink) {
    event.preventDefault();
  }
}
```

이 예제에서 형식 목록 내에 [text/uri-list](/ko/docs/DragDrop/Recommended_Drag_Types#link) 형식이 존재하는지 확인하기 위해 `contains` 메서드를사용합니다. 존재할 경우에는 드랍을 허용하기 위해 이벤트가 취소될 것입니다. 드래그 데이터가 링크를 포함하지 않았다면, 해당 이벤트는 취소되지 않을 것이고 그 위치에 대한 드랍이 발생하지 않을 것입니다.

수행되어야 하는 작업 형식을 더 세부적으로 설정하길 원한다면, {{domxref("DataTransfer.effectAllowed","effectAllowed")}}나 {{domxref("DataTransfer.dropEffect","dropEffect")}} 속성을 각각 설정하거나 동시에 둘 다를 설정하고 싶을 것입니다. 두 속성을 변경하더라도 해당 이벤트를 취소하지 않으면 아무런 영향이 없을 것입니다.

### Updates to DataTransfer.types

최신 스펙에는 {{domxref("DataTransfer.types")}}이 {{domxref("DOMStringList")}}(이 속성은 Fiirefox 52 이상에서 지원됨)이 아닌 {{domxref("DOMString")}} 형식의 고정배열(fronzen array)을 반환하도록 명시하고 있음에 유의하시기 바랍니다.

그 결과로, [contains](/ko/docs/Web/API/Node/contains) 메서드는 해당 속성에 대해 더 이상 동작하지 않으며; 특정 형식의 데이터가 제공되는지 확인하기 위해서는 다음 코드와 같이 [includes](/ko/docs/Web/JavaScript/Reference/Global_Objects/Array/includes) 메서드를 사용해야 합니다:

```js
if ([...event.dataTransfer.types].includes("text/html")) {
  // Do something
}
```

일부 특성 검출(feature detection)을 이용해 `types`에 대해 어떤 메서드가 지원되는지를 판별하고 적절하게 코드를 실행할 수 있습니다.

## Drop Feedback

There are several ways in which you can indicate to the user that a drop is allowed at a certain location. The mouse pointer will update as necessary depending on the value of the {{domxref("DataTransfer.dropEffect","dropEffect")}} property. Although the exact appearance depends on the user's platform, typically a plus sign icon will appear for a 'copy' for example, and a 'cannot drop here' icon will appear when a drop is not allowed. This mouse pointer feedback is sufficient in many cases.

However, you can also update the user interface with an insertion point or highlight as needed. For simple highlighting, you can use the `-moz-drag-over` CSS pseudoclass on a drop target.

```css
.droparea:-moz-drag-over {
  border: 1px solid black;
}
```

In this example, the element with the class `droparea` will receive a 1 pixel black border while it is a valid drop target, that is, if the {{domxref("Event.preventDefault","preventDefault()")}} method was called during the `{{event("dragenter")}}` event. Note that you must cancel the `{{event("dragenter")}}` event for this pseudoclass to apply, as this state is not checked for the `{{event("dragover")}}` event.

For more complex visual effects, you can also perform other operations during the `{{event("dragenter")}}` event, for example, by inserting an element at the location where the drop will occur. For example, this might be an insertion marker or an element that represents the dragged element in its new location. To do this, you could create an [image](/ko/docs/XUL/image) or [separator](/ko/docs/XUL/separator) element, for example, and simply insert it into the document during the `{{event("dragenter")}}` event.

The `{{event("dragover")}}` event will fire at the element the mouse is pointing at. Naturally, you may need to move the insertion marker around a `{{event("dragover")}}` event as well. You can use the event's {{domxref("MouseEvent.clientX","clientX")}} and {{domxref("MouseEvent.clientY","clientY")}} properties as with other mouse events to determine the location of the mouse pointer.

Finally, the `{{event("dragleave")}}` event will fire at an element when the drag leaves the element. This is the time when you should remove any insertion markers or highlighting. You do not need to cancel this event. Any highlighting or other visual effects specified using the `-moz-drag-over` pseudoclass will be removed automatically. The `{{event("dragleave")}}` event will always fire, even if the drag is cancelled, so you can always ensure that any insertion point cleanup can be done during this event.

## Performing a Drop

When the user releases the mouse, the drag and drop operation ends. If the mouse was released over an element that is a valid drop target, that is, one that cancelled the last `{{event("dragenter")}}` or `{{event("dragover")}}` event, and then the drop will be successful, and a `{{event("drop")}}` event will fire at the target. Otherwise, the drag operation is cancelled, and no `{{event("drop")}}` event is fired.

During the `{{event("drop")}}` event, you should retrieve that data that was dropped from the event and insert it at the drop location. You can use the {{domxref("DataTransfer.dropEffect","dropEffect")}} property to determine which drag operation was desired.

As with all drag-related events, the event's `{{domxref("DataTransfer","dataTransfer")}}` property will hold the data that is being dragged. The {{domxref("DataTransfer.getData","getData()")}} method may be used to retrieve the data again.

```js
function onDrop(event) {
  var data = event.dataTransfer.getData("text/plain");
  event.target.textContent = data;
  event.preventDefault();
}
```

The {{domxref("DataTransfer.getData","getData()")}} method takes one argument, the type of data to retrieve. It will return the string value that was set when {{domxref("DataTransfer.setData","setData()")}} was called at the beginning of the drag operation. An empty string will be returned if data of that type does not exist. Naturally, though, you would likely know that the right type of data was available, as it was previously checked during a `{{event("dragover")}}` event.

In the example here, once we have retrieved the data, we insert the string as the textual content of the target. This has the effect of inserting the dragged text where it was dropped, assuming that the drop target is an area of text such as a `p` or `div` element.

In a web page, you should call the {{domxref("Event.preventDefault","preventDefault()")}} method of the event if you have accepted the drop so that the default browser handling does not handle the dropped data as well. For example, when a link is dragged to a web page, Firefox will open the link. By cancelling the event, this behavior will be prevented.

You can retrieve other types of data as well. If the data is a link, it should have the type [text/uri-list](/ko/docs/DragDrop/Recommended_Drag_Types#link). You could then insert a link into the content.

```js
function doDrop(event) {
  var lines = event.dataTransfer.getData("text/uri-list").split("\n");
  for (let line of lines) {
    if (line.startsWith("#")) continue;

    let link = document.createElement("a");
    link.href = line;
    link.textContent = line;
    event.target.appendChild(link);
  }
  event.preventDefault();
}
```

This example inserts a link from the dragged data. As you might be able to guess from the name, the [text/uri-list](/ko/docs/DragDrop/Recommended_Drag_Types#link) type actually may contain a list of URLs, each on a separate line. In this code, we use the [split](/ko/docs/JavaScript/Reference/Global_Objects/String/split) to split the string into lines, then iterate over the list of lines, inserting each as a link into the document. Note also that we skip links starting with a number sign (#) as these are comments.

For simple cases, you can use the special type `URL` just to retrieve the first valid URL in the list. For example:

```js
var link = event.dataTransfer.getData("URL");
```

This eliminates the need to check for comments or iterate through lines yourself; however, it is limited to only the first URL in the list.

The `URL` type is a special type used only as a shorthand, and it does not appear within the list of types specified in the {{domxref("DataTransfer.types","types")}} property.

Sometimes you may support some different formats, and you want to retrieve the data that is most specific that is supported. In this example, three formats are supported by a drop target.

The following example returns the data associated with the best-supported format:

```js
function doDrop(event) {
  var types = event.dataTransfer.types;
  var supportedTypes = [
    "application/x-moz-file",
    "text/uri-list",
    "text/plain",
  ];
  types = supportedTypes.filter((value) => types.includes(value));
  if (types.length) var data = event.dataTransfer.getData(types[0]);
  event.preventDefault();
}
```

This method relies on JavaScript functionality available in Firefox 3. However, the code could be adjusted to support other platforms.

## Finishing a Drag

Once the drag is complete, a `{{event("dragend")}}` event is fired at the source of the drag (the same element that received the `{{event("dragstart")}}` event). This event will fire if the drag was successful\[1] or if it was cancelled. However, you can use the {{domxref("DataTransfer.dropEffect","dropEffect")}} property to determine what drop operation occurred.

If the {{domxref("DataTransfer.dropEffect","dropEffect")}} property has the value `none` during a `{{event("dragend")}}`, then the drag was cancelled. Otherwise, the effect specifies which operation was performed. The source can use this information after a move operation to remove the dragged item from the old location. The {{domxref("DataTransfer.mozUserCancelled","mozUserCancelled")}} property will be set to true if the user cancelled the drag (by pressing Escape), and false if the drag was cancelled for other reasons such as an invalid drop target, or if it was successful.

A drop can occur inside the same window or over another application. The `{{event("dragend")}}` event will always fire regardless. The event's {{domxref("MouseEvent.screenX","screenX")}} and {{domxref("MouseEvent.screenY","screenY")}} properties will be set to the screen coordinate where the drop occurred.

After the `{{event("dragend")}}` event has finished propagating, the drag and drop operation is complete.

\[1] In Gecko, {{event("dragend")}} is not dispatched if the source node is moved or removed during the drag (e.g. on drop or {{event("dragover")}}). [bug 460801](https://bugzilla.mozilla.org/show_bug.cgi?id=460801)

## See also

- [HTML Drag and Drop API (Overview)](/ko/docs/Web/API/HTML_Drag_and_Drop_API)
- [Dragging and Dropping Multiple Items](/ko/docs/Web/Guide/HTML/Dragging_and_Dropping_Multiple_Items)
- [Recommended Drag Types](/ko/docs/Web/Guide/HTML/Recommended_Drag_Types)
- [HTML5 Living Standard: Drag and Drop](https://html.spec.whatwg.org/multipage/interaction.html#dnd)

---
# Source: Web_API_WebGL_API_WebGL_best_practices.md
---
---
title: WebGL best practices
slug: Web/API/WebGL_API/WebGL_best_practices
---

{{DefaultAPISidebar("WebGL")}}

이 기사는 당신의 WebGL 콘텐트 질을 향상시키기 위한 제안과 팁을 제시합니다. 다음의 제안들을 따르면, 당신의 웹 애플리케이션이 더 많은 장치들과 브라우저들과의 호환성을 높일 수 있을 뿐만 아니라, 성능도 향상시킬 수 있게 도와줍니다.

## 피해야 할 것들

- 당신의 웹 애플리케이션이 getError()가 리턴한 어떠한 WebGL 에러도 생성하지 않도록 항상 확실시 하세요.
- 당신은 WebGL 셰이더에서 절대로 #ifdef GL_ES를 사용해선 안 됩니다; 비록 초기의 몇몇 예제들은 이를 사용했더라도, 이제는 꼭 필요하지 않습니다. 왜냐하면 이 조건은 WebGL 셰이더에서 항상 참이기 때문입니다.
- 프래그먼트 셰이더에서 highdp 정밀도를 사용하는 것은 당신의 콘텐트가 몇몇의 구식 모바일 하드웨어에서 작동하는 것을 방해할 것입니다. 대신에 mediump를 사용할 수 있습니다. 하지만 이것은 종종 정밀도의 부족 때문에 대부분의 모바일 장치에서 오염된 렌더링을 초래합니다. 그리고 그 오염은 전형적인 데스크톱 컴퓨터에서는 보이지 않을 것입니다. 일반적으로, 셰이더가 다양한 플랫폼에서 철저하게 테스트되지 않았다면 정점, 프래그먼트 셰이더에서는 오직 highdp만 사용하는 것이 더 안전합니다. WebGL getShaderPrecisionFormat() 함수가 구현된 Firefox11에서 시작하는 것은 당신이 highdp 정밀도가 지원되는지 검사하도록 허용하고, 더 일반적으로, 지원되는 모든 정밀도 한정자의 실제 정밀도를 조회할 수 있게 해줍니다.

## 마음에 새겨야 할 것들

- 몇몇의 WebGL의 능력들은 클라이언트에 의존합니다. 그들에게 의존하기 전에, 당신은 WebGL getParameter() 함수를 사용해서 클라이언트 측에서 무슨 값들이 지원되는지 결정해야 합니다. 예를 들면, 2D 텍스처의 최대 크기는 webgl.getParameter(webgl.MAX_TEXTURE_SIZE)로 주어집니다. Firefox10에서의 `webgl.min_capability_mode` preference는 이식성 검사를 위해 능력의 최소한의 값들을 시뮬레이팅 하도록 허락해 줍니다.
- In particular, note that usage of textures in vertex shaders is only possible if `webgl.getParameter(webgl.MAX_VERTEX_TEXTURE_IMAGE_UNITS)` is greater than zero. Typically, this fails on current mobile hardware.
- The availability of most WebGL extensions depends on the client. When using WebGL extensions, if possible, try to make them optional by gracefully adapting to the case there they are not supported. Starting in Firefox 10, the `webgl.disable-extensions` preference allows simulating the absence of all extensions, to test portability.
- Rendering to a floating-point texture may not be supported, even if the `OES_texture_float` extension is supported. Typically, this fails on current mobile hardware. To check if this is supported, you have to call the WebGL `checkFramebufferStatus()` function.
- Rendering to a canvas can be done at a different resolution than the style sheet will eventually force the canvas to appear at. If struggling with performance you should consider rendering to a low resolution WebGL context and using CSS to upscale its canvas to the size you intend.

## 일반적인 성능 팁들

- Anything that requires syncing the CPU and GPU sides is potentially very slow, so if possible you should try to avoid doing that in your main rendering loops. This includes the following WebGL calls: `getError()`, `readPixels()`, and `finish()`. WebGL getter calls such as `getParameter()` and `getUniformLocation()` should be considered slow too, so try to cache their results in a JavaScript variable.
- Fewer, larger draw operations will improve performance. If you have 1000 sprites to paint, try to do it as a single `drawArrays()` or `drawElements()` call. You can draw degenerate (flat) triangles if you need to draw discontinuous objects as a single `drawArrays()` call.
- Fewer state changes will also improve performance. In particular, if you can pack multiple images into a single texture and select them by using the appropriate texture coordinates, that can help you do fewer texture binding changes, which improves performance.
  - In some rare cases, packing greyscale textures which belong together into the color channels of a single texture might help.

- Smaller textures perform better than larger ones. For this reason, mipmapping can be a performance win.
- Simpler shaders perform better than complex ones. In particular, if you can remove an `if` statement from a shader, that will make it run faster. Division and math functions like `log()` should be considered expensive too.
  - However, nowadays even mobile devices possess powerful GPUs that are capable of running even relatively complex shader programs. Moreover, because shaders are compiled, the eventual machine code that actually runs on the hardware may be highly optimized. What may seem like an expensive function call may in fact compile into only few (or even a single) machine instructions. This is particularly true for {{Glossary("GLSL")}} functions that typically operate on vectors, such as `normalize()`, `dot()` and `mix()`. The best advice in that regard is to use the built-in functions, rather than try to implement, for example, one's own version of a dot-product or linear interpolation, which may in fact compile to larger and less optimized machine code. Finally, it is important to keep in mind that GPUs are constructed to do complex mathematical calculations in hardware, and therefore, may support math functions, such as `sin()`, `cos()` and other, through dedicated machine instructions.

- Do as much as you can in the vertex shader, rather than in the fragment shader. Because, per rendering pass, fragment shaders run many more times than vertex shaders, any calculation that can be done on the vertices and then just interpolated among fragments is a performance boon (this interpolation is done "automagically" for you, through the fixed functionality rasterization phase of the OpenGL pipeline). For example, a simple animation of a textured surface can be achieved through a time-dependent transformation of texture coordinates (simplest case is to add a uniform vector to the texture coordinates attribute vector). If visually acceptable, one can transform the texture coordinates in the vertex shader rather than in the fragment shader, to get better performance.
- Always have vertex attrib 0 array enabled. If you draw with vertex attrib 0 array disabled, you will force the browser to do complicated emulation when running on desktop OpenGL (e.g. on Mac OSX). This is because in desktop OpenGL, nothing gets drawn if vertex attrib 0 is not array-enabled. You can use `bindAttribLocation()` to force a vertex attribute to use location `0`, and use `enableVertexAttribArray()` to make it array-enabled.

---
# Source: Web_API_Node_insertBefore.md
---
---
title: Node.insertBefore()
slug: Web/API/Node/insertBefore
---

{{APIRef("DOM")}}

**`Node.insertBefore()`** 메소드는 참조된 노드 앞에 특정 부모 노드의 자식 노드를 삽입합니다. 만약 주어진 자식 노드가 document에 존재하는 노드를 참조한다면, `insertBefore()` 가 자식 노드를 현재 위치에서 새로운 위치로 옮깁니다. (노드를 다른 노드에 추가하기 전에 상위 노드에서 제거할 필요가 없습니다)

이것은 노드가 document에 동시에 두 곳에 존재할 수 없다는 것을 의미합니다. 그러므로 노드가 이미 부모를 가지고 있다면, 노드가 제거된 뒤에 새로운 위치에 삽입됩니다. {{domxref("Node.cloneNode()")}} 로 노드를 새로운 부모 아래에 추가하기 전에 복사본을 만들수 있습니다. `cloneNode` 로 만들어진 복사본들은 자동으로 동기화 상태를 유지하지 않는다는 것을 알아두십시오.

만약 참조 노드가 `null` 이라면, 노드는 부모 노드의 자식 노드 리스트 맨 끝에 추가됩니다.

만약 자식 노드가 {{domxref("DocumentFragment")}} 이라면, {{domxref("DocumentFragment")}} 의 콘텐츠 전체는 부모 노드의 자식 리스트로 이동됩니다.

## Syntax

```js
var insertedNode = parentNode.insertBefore(newNode, referenceNode);
```

`referenceNode` 가 `null` 이라면, `newNode` 가 자식 노드의 리스트의 끝에 삽입됩니다.

> **참고:** _`referenceNode`_ 는 **선택 인자가 아닙니다.** — 명시적으로 `Node` 나 `null` 를 전달해야 합니다. 전달하지 않거나 잘못된 값을 전달하면 브라우저 버전에 따라 다른 결과를 얻게 됩니다.

## Returns

반환값은 추가된 자식 노드입니다. 다만 `newNode` 가 {{domxref("DocumentFragment")}} 일 경우, 빈 {{domxref("DocumentFragment")}} 이 반환됩니다.

## Example 1

```html
<div id="parentElement">
  <span id="childElement">foo bar</span>
</div>

<script>
  // Create the new node to insert
  var newNode = document.createElement("span");

  // Get a reference to the parent node
  var parentDiv = document.getElementById("childElement").parentNode;

  // Begin test case [ 1 ] : Exist a childElement --> All working correctly
  var sp2 = document.getElementById("childElement");
  parentDiv.insertBefore(newNode, sp2);
  // End test case [ 1 ]

  // Begin test case [ 2 ] : childElement is of Type undefined
  var sp2 = undefined; // Not exist a node of id "childElement"
  parentDiv.insertBefore(newNode, sp2); // Implicit dynamic cast to type Node
  // End test case [ 2 ]

  // Begin test case [ 3 ] : childElement is of Type "undefined" ( string )
  var sp2 = "undefined"; // Not exist a node of id "childElement"
  parentDiv.insertBefore(newNode, sp2); // Generate "Type Error: Invalid Argument"
  // End test case [ 3 ]
</script>
```

- `insertedNode` The node being inserted, that is `newNode`
- `parentNode` The parent of the newly inserted node.
- `newNode` The node to be inserted.
- `referenceNode` The node before which `newNode` is inserted.

## Example 2

```html
<div id="parentElement">
  <span id="childElement">foo bar</span>
</div>

<script>
  // Create a new, plain <span> element
  var sp1 = document.createElement("span");

  // Get a reference to the element, before we want to insert the element
  var sp2 = document.getElementById("childElement");
  // Get a reference to the parent element
  var parentDiv = sp2.parentNode;

  // Insert the new element into the DOM before sp2
  parentDiv.insertBefore(sp1, sp2);
</script>
```

There is no `insertAfter` method. It can be emulated by combining the `insertBefore` method with [`nextSibling`](/ko/docs/DOM/Node.nextSibling).

In the previous example, `sp1` could be inserted after `sp2` using:

```js
parentDiv.insertBefore(sp1, sp2.nextSibling);
```

If `sp2` does not have a next sibling, then it must be the last child — `sp2.nextSibling` returns `null`, and `sp1` is inserted at the end of the child node list (immediately after `sp2`).

## Example 3

Insert an element before the first child element, using the [firstChild](/ko/docs/DOM/Node.firstChild) property.

```js
// Get a reference to the element in which we want to insert a new node
var parentElement = document.getElementById("parentElement");
// Get a reference to the first child
var theFirstChild = parentElement.firstChild;

// Create a new element
var newElement = document.createElement("div");

// Insert the new element before the first child
parentElement.insertBefore(newElement, theFirstChild);
```

When the element does not have a first child, then `firstChild` is `null`. The element is still appended to the parent, after the last child. Since the parent element did not have a first child, it did not have a last child either. Consequently, the new element is the only element, after insertion.

## 브라우저 호환성

{{Compat}}

## 명세서

{{Specifications}}

## See also

- {{domxref("Node.removeChild()")}}
- {{domxref("Node.replaceChild()")}}
- {{domxref("Node.appendChild()")}}
- {{domxref("Node.hasChildNodes()")}}
- {{domxref("Element.insertAdjacentElement()")}}
- {{domxref("ParentNode.prepend()")}}

