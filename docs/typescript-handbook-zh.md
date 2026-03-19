---
# Source: README.md
---
### Playground Handbook

This package is structured similar to the main documentation section of the repo, and handles the content for the Playground documentation.

---
# Source: Type Acquisition.md
---
## Type Acquisition

No Playground is an island. Well, not strictly, no playground _needs_ to be an island. One of the first problem we hit when adding support for `.tsx`/`.jsx` to the Playground was that to **_really_** use JSX to write React components - you need the types for React.

This left us with the dilemma of needing to either bundle React's evolving types into the Playground, or to replicate the feature found in JavaScript projects utilizing TypeScript: Automatic Type Acquisition. The idea behind Automatic Type Acquisition (ATA) is that behind the scenes the Playground will look at any `import` / `require` / [`/// <reference types"`](/docs/handbook/triple-slash-directives.html) and understand what npm modules have been referenced.

For these referenced modules, TypeScript will search through the npm package contents, and potentially in the `@types` equivalent for `.d.ts` files to describe how the library works. This means to get the types for React, you would create a playground like:

```ts
import React from "react"

const myComponent = () => <h1>Hello, world</h1>
```

Type Acquisition will:

- look in the package `react` on npm, see there are no `.d.ts` files in its contents
- look to see if `@types/react` exists, downloads all of the `.d.ts` files
- read the `.d.ts` files in `@types/react`, and discover they import from `csstype` and `prop-types`
  - look in the package `csstype` for `.d.ts` files and downloads them
  - look in the package `prop-types` for `.d.ts` files and finds none
  - look to see if `@types/prop-types` exists and download the `.d.ts` files from that

That one import line has downloaded the `.d.ts` files from `@types/react`, `@types/prop-types` and `csstype`. These are added to the Playground's TypeScript project's `node_modules` folder and TypeScript picks them up.

This is all built on the [jsdelivr CDN](https://www.jsdelivr.com/) which has kept the complexity down, and the type acquisition system is available for other projects to use via npm on [`@typescript/ata`](https://www.npmjs.com/package/@typescript/ata).

If you need more control over the version of the types which are imported into the Playground, you can append `// types: npm_tag_or_version`

```
import { xy } from "xyz" // types: beta
```

The type acquisition as-is is quite eager and may start pulling your types before you've set the npm tag or version. In that case, you can reload your browser once it's written to get the right version.

---
# Source: Overview.md
---
## Welcome to the Playground Handbook

The TypeScript playground is an online environment where people can write and share TypeScript-ish code. We say "ish" because you can work with `.ts`, `.tsx`, `.js`, `.jsx` and `.d.ts` files inside the playground. The goal for the Playground is to be a safe environment which requires no setup, is a single text document, can be trivially shared with others, where URLs still works years down the line. In summary, a teaching tool where you can safely experiment.

From [day one in 2012](https://web.archive.org/web/20121031123957/http://www.typescriptlang.org/Playground/), the TypeScript website has featured a playground as a way to highlight the difference between the TypeScript code you write and the JavaScript which is emitted. Today, the Playground has a massive set of features because the needs of developers using TypeScript has grown in scope - there's over a hundred [`tsconfig.json`](https://www.typescriptlang.org/tsconfig) flags. Developers need a safe way to be able to reproduce a particular TypeScript environment which can be shared with others.

This handbook will guide you through the feature set of the Playground, explain why these features exist and help you master them. It is generally meant to be read in order, and you should be able to get through the handbook in about 25 minutes. Assuming you don't dive into too many rabbit holes. That said, the rabbit holes tend to be where the fun complexity lives and time is an illusion anyway. So, we'll get started over at the [Compiler Settings](/play#handbook-1) page.

---
# Source: Running Code.md
---
## Running Code

The TypeScript playground has an obvious focus on TypeScript — I mean it's in the name (right?), and types in TypeScript are ephemeral (they don't affect the running code) so earlier versions of the Playground did not have support for running the code in your browser.

This turned out to be an oversight, because there are cases where the TypeScript types cannot perfectly map the JavaScript runtime and `eval`ing that code can sometimes be a great way to understand whether the types you have written match the runtime results of your code.

In the editor toolbar, the one which is not visible because you're reading this handbook, is a "Run" button. Hitting this run button will:

- Take the code in the editor and convert it to JS
- Remove references to `"reflect-metadata"` if you are using decorators
- Run that code within the context of your current browser session
- Capture any `console.log`, `.error`, `.warn` and `.debug` calls and show them in the sidebar "Logs" tab.

You can also use the key command <kbd>ctrl</kbd>/<kbd>cmd</kbd> + <kbd>enter</kbd> to trigger running your code.

Your code running in your browser means that you can experiment with the DOM APIs inside a TypeScript environment. The Playground includes examples for working with [the DOM](https://www.typescriptlang.org/play?useJavaScript=trueq=185#example/typescript-with-web) and with [WebGL](https://www.typescriptlang.org/play/?useJavaScript=trueq=461#example/typescript-with-webgl) which are good showcases of how that can work.

Conveniently, that’s kind of the perfect segue to the [Examples section of the handbook](/play#handbook-2)

---
# Source: Twoslash Annotations.md
---
## Twoslash Annotations

[Twoslash](https://www.npmjs.com/package/@typescript/twoslash) is an annotation format for TypeScript which uses specially crafted comments (two slashes `//`) as a markup format for writing code samples (available on npm at [`@typescript/twoslash`](https://www.npmjs.com/package/@typescript/twoslash)). It powers all the code samples in the TypeScript website, you can learn more about it [here](https://shikijs.github.io/twoslash/).

#### Twoslash Queries

The Playground supports showing the types at a certain location by using an empty comment with a `^?` to indicate the symbol you're interested in:

```ts
const abc = "Hello"
//    ^?
```

Would add a realtime inline annotation about what the type of `abc` is into the editor. This can make typing complex types easier, and make it much more obvious when sharing code what you think is important.

#### Twoslash Compiler Flags

A more arcane, but very ergonomic way to set a compiler setting is via compiler flag which are comments starting with `// @`.

The editor will auto-complete twoslash commands for any compiler setting for the current version of TypeScript in your Playground. If the setting is a boolean, you don't need to set a value:

```ts
// @isolatedModules
```

Would have `isolatedModules` turned on in your Playground. You can set the values via `true/false`:

```ts
// @strictPropertyInitialization: false
```

For more settings with more choices of values, you can use the same descriptive string that is available in a `tsconfig.json`:

```ts
// @target: esnext
// @module: nodenext
```

You can write a list with a comma separated string:

```ts
// @lib: es2015,dom
```

Writing a twoslash command will set the compiler flag as you type, and will be set instantly if you reload or share the URL with another person. This can act as a power-user tool for setting compiler flags _and_ making that change much more explicit than a query param (which may require looking up in the TS Config dropdown.)

<details>
<summary>Did you know?</summary>

The twoslash system replicates how the TypeScript Compiler is tested, which is ~60k integration tests which uses specially crafted comments to set up isolated compiler runs. It's quite a cool system, you can learn about them in more depth over at [`orta/typescript-notes`](https://github.com/orta/typescript-notes/tree/master/systems/testing).

</details>

---
# Source: Compiler Settings.md
---
## Compiler Settings

There isn't a `tsconfig.json` file in a Playground, but you need to be able to set the compiler flags in order to accurately re-create a particular environment. Even for the simplest code, the difference in how TypeScript acts between `strict: true` and `strict: false` is pretty drastic and not being able to set that to match would suck.

Above this prose there are two toolbars, one is the site navigation in bright blue - under that is the Playground's toolbar. This toolbar has a button "TS Config", clicking that will show you the main interface for setting compiler options in the Playground. You can do it now by the way, then click "Close" to get back to this text.

### TS Config Panel

The TS Config panel contains a focused list of the TypeScript compiler options available inside a `tsconfig.json`. It starts off with some dropdowns for some of the most important compiler options and then it moves down to categories with boolean check boxes. This list has grown organically over time and generally represents the settings which people use most. If you need to set a value which isn't in that list, there is a way to set any option via [twoslash annotations](/play?#handbook-12) which we'll get to later in the handbook.

Changing a compiler flag will update the URL in your browser (unless you have that disabled in the settings.) The URL structure works by comparing the current compiler options versus the default settings (covered below) and only showing compiler options which differ from the defaults. For example, the default for a Playground is to have `esModuleInterop: true` enabled, thus turning `esModuleInterop` to `false` would append `?esModuleInterop=false` to the URL:

```diff
# Before
- https://www.typescriptlang.org/play

# After turning esModuleInterop off
+ https://www.typescriptlang.org/play?esModuleInterop=false
```

This helps keep Playground URLs on the short side, or at least doesn't add to their size needlessly. You might notice that sometimes the compiler flags aren't the exact same in the URL as the user interface, for example `?target=6` is `target: ES2019` this is us saving characters by using the enum's numerical value rather than the string representation.

<details>
<summary>The defaults for the compiler in a Playground</summary>

_In rough_, the Playground has settings which can be summed up as this:

```json
{
  "compilerOptions": {
    "strict": true,
    "module": "esnext",
    "moduleResolution": "node",
    "target": "es2017",
    "jsx": "react",

    "experimentalDecorators": true,
    "emitDecoratorMetadata": true
  }
}
```

The reality is (of course) a tad more complex, we detect if a compiler setting is in the following list as a cue for showing the compiler setting in the TS Config panel user interface and only add a setting to the URL if it differs from this list.

So, the full specification for the default compiler settings (as of TypeScript 4.5) looks like this:

```ts
export function getDefaultSandboxCompilerOptions(config: SandboxConfig, monaco: Monaco) {
  const useJavaScript = config.filetype === "js"
  const settings: CompilerOptions = {
    strict: true,

    noImplicitAny: true,
    strictNullChecks: !useJavaScript,
    strictFunctionTypes: true,
    strictPropertyInitialization: true,
    strictBindCallApply: true,
    noImplicitThis: true,
    noImplicitReturns: true,
    noUncheckedIndexedAccess: false,

    useDefineForClassFields: false,

    alwaysStrict: true,
    allowUnreachableCode: false,
    allowUnusedLabels: false,

    downlevelIteration: false,
    noEmitHelpers: false,
    noLib: false,
    noStrictGenericChecks: false,
    noUnusedLocals: false,
    noUnusedParameters: false,

    esModuleInterop: true,
    preserveConstEnums: false,
    removeComments: false,
    skipLibCheck: false,

    checkJs: useJavaScript,
    allowJs: useJavaScript,
    declaration: true,

    importHelpers: false,

    experimentalDecorators: true,
    emitDecoratorMetadata: true,
    moduleResolution: monaco.languages.typescript.ModuleResolutionKind.NodeJs,

    target: monaco.languages.typescript.ScriptTarget.ES2017,
    jsx: monaco.languages.typescript.JsxEmit.React,
    module: monaco.languages.typescript.ModuleKind.ESNext,
  }

  return { ...settings, ...config.compilerOptions }
}
```

This includes a lot of values which are set to their default value too. Which actually can make setting up a _perfect_ environment tricky because 'no value set' can differ from 'false' for some settings, but breaking this system would break backwards compatibility (URLs would change) and make URLs longer, thus it stays the way it is.

</details>

That's that for the compiler settings. Next up, [Examples](/play#handbook-2).

---
# Source: URL Structure.md
---
## URL Structures

Because the Playground runs in the browser, we strive to represent all possible environmental setting inside the URL so that you can easily share your Playground. This include the code, compiler flags and settings.

The Playground supports two forms of inputs from the URL: The Hash and queries.

### The Hash

The hash generally represents the state of the editor:

- `#code/PRAz3dDc3...` - A base64 and zipped version of the code which should live in the editor. You can use [`LZString.compressToEncodedURIComponent`](https://github.com/pieroxy/lz-string/blob/master/libs/lz-string.js#L93) from the [`lz-string`](https://github.com/pieroxy/lz-string) package to construct URLs for arbitrary pieces of code
- `#src=The%20code...` - URLEncoded way to have the code for the editor (used for backwards-compatibility with older URLs)
- `#example/generic-functions` - Grab the code from a Playground example with the id generic-functions
- `#handbook-2` - The Playground handbook with the page number

Or to trigger some action in the Playground UI by default:

- `#show-examples` - When the app is loaded, show the "Examples" panel
- `#show-whatisnew` - When the app is loaded, show the "What is New" panel

### The Query

Then the query string tend to be about changing the state of the Playground setup from the default:

- `?ts=3.9.2` - Sets the TypeScript version, the list of supported versions is in these [two](https://playgroundcdn.typescriptlang.org/indexes/pre-releases.json) [json](https://playgroundcdn.typescriptlang.org/indexes/releases.json) files.

  There are two special cases for the `ts` option:

  - `ts=next`: Use the most recent [nightly build](https://www.typescriptlang.org/docs/handbook/nightly-builds.html).
  - `ts=dev`: Use your [local developer's build of TypeScript](https://github.com/microsoft/TypeScript/blob/main/scripts/createPlaygroundBuild.js)

- `?flag=value` - Any compiler flag referenced in can be set from a query
- `?filetype=js|ts|dts` - Tells the Playground to set the editor's language

---
# Source: Examples.md
---
## Examples

The Playground examples are an interactive set of tutorials, and overviews into parts of TypeScript with a very tight focus. They are not as comprehensive as [the TypeScript handbook](/docs/handbook/intro.html), but they aim to offer a 2nd explanation (with different metaphors and ideas) inside comments of a Playground which invites the writer to fidget with the code and see how the pieces come together.

<details><summary>Speaking as the author, ...</summary>

Speaking as the author, I, _Orta_, think there are many ways for people to learn a complex subject. I don't think it's possible to just pick up a single book and _" :tada: I understand X."_ We're not learning kung-fu in a second, something like TypeScript takes a while to learn.

I believe that studying something complex revolves around creating a mesh of understanding by mixing learning and doing. The TypeScript handbook does a great job of covering all the primitives of TypeScript, and you can study it, but with the Playground we have a space for a 2nd explanation on the same topics with an environment structured for play and safe failure. The Examples in the Playground are built to encourage exploration of ideas.

</details>

You can access the examples via the Playground toolbar for both "Examples" and "What's New" - there's also links in the footer of every page (except the homepage.)

The Playground examples are structured into 3 main sections:

- **TypeScript** - covering type syntax primitives, terms which may be new to people, and language extensions
- **JavaScript** - showing how TypeScript types can interact with runtime code, how to work with different environments and existing JavaScript structures
- **What's new** - Per-release feature specific explanations of new language changes

The examples that you have read are tracked in your browser via `localStorage`, and you get see a blue dot next to something you have read in the dropdown. If that blue dot is empty, it means the example has been updated since you last read it.

---
# Source: JS + DTS sidebars.md
---
## .JS + .D.TS Sidebars

### .JS Emit

Two of the key arguments for using TypeScript are its JavaScript interoperability and "downleveling" the emitted JavaScript to (an older version of) JavaScript. You may have heard of "downleveling" as "transpile" or "backport" but the rough gist is taking modern syntax and re-implementing it using older syntax for older browsers and JavaScript engines.

Because understanding the JavaScript output from your TypeScript can be valuable, we made it the default view in the Playground. The "JS" sidebar shows what happens when the code in your editor is converted to a JavaScript version (mostly) according to your `target` compiler setting, which defaults to `ES2017`. This works with `.tsx`, `.ts`, `.js` files, and `.d.ts` files are (accurately) shown to have no JavaScript equivalent. The "JS" sidebar will update as you type.

### .D.TS Emit

`.d.ts` files are the behind-the-scenes tooling which power the editing experiences for working with JavaScript libraries. If you're writing TypeScript all day and interact mainly with TypeScript codebases, you might not need to write and understand the output of a `.d.ts` too often. However, this isn't the case for everyone and the `.d.ts` sidebar tab helps you understand how TypeScript will generate a `.d.ts` for your code.

There are two use cases for using the `.d.ts` tab:

- **TypeScript to `.d.ts`**. Understanding the effects of `export` in your code and how TypeScript resolves your types.

- **JavaScript to `.d.ts`**. When you are writing a library in JavaScript and use a mix of type inference and [JSDoc support](https://www.typescriptlang.org/docs/handbook/jsdoc-supported-types.html) to add type annotations.

### Other files

No-one has really asked for `.map` support, which is the other file the TypeScript compiler could emit. However, you could turn on [`inlineSourceMap`](https://www.typescriptlang.org/tsconfig#inlineSourceMap) to have it included in the `.js` emit [for example](https://www.typescriptlang.org/play?inlineSourceMap=true#code/PTAEAEEsDsBsYKYGUD2BXATgYwQWQIYAOAUFitAM4Auo+oAvKAEQDyA0k0A).

---
# Source: Localization.md
---
## Localization

Like the rest of this website, the TypeScript Playground is localized. As of 2021, the current list of supported languages are:

- [`es`](/es/play)
- [`fr`](/fr/play)
- [`id`](/id/play)
- [`ja`](/ja/play)
- [`ko`](/ko/play)
- [`pt`](/pt/play)
- [`vo`](/vo/play)
- [`zh`](/zh/play)

Ideally this helps folks for whom English is a second language!

---
# Source: Settings Panel.md
---
## Settings Panel

Hidden in the top right corner, under "Search Docs" is the "Settings" button where you can access the settings for the Playground. There are not many settings in the Playground.

### Playground Options

**"Disable ATA"**

Turns off [Type Acquisition](/play#handbook-5) which means that when importing code, the Playground will not try to acquire the types via the internet.

**"Disable Save-On-Type"**

When the editor loses focus, or compiler flags change, the Playground will replace the URL in your browser. This doesn't change the behavior of the back button, but it does add history entries in the browser. You can turn off this behavior via this setting, and you can use the 'Share' (or press <kbd>cmd/ctrl</kbd> + <kbd>s</kbd>) to copy the sharable URL.

### Sidebar Tabs

You can choose which tabs are available in the Playground sidebar via the toggle boxes under above Playground Options.

---
# Source: Exporting Your Code.md
---
## Exporting Code

Outside of learning for yourself, you will need to have ways to share the work you've done with others. Throughout this handbook, we've focused on the browser's URL as the way to share the Playground but that's not the only option. All of the export options are available under "Export" in the editor toolbar. There are three main sections:

### Exporting To Markdown

We have ways of generating useful markdown from your playground, either for reporting a bug to the TypeScript or for providing a summary link in a chat.

### Exporting To Similar Tools

You can send the current playground code to another Playground-like system, for example the [TypeScript AST Viewer](https://ts-ast-viewer.com).

### Exporting For More Features

Because the Playground has a strong focus on only presenting a single text file, that comes with limitations.

There are very good general purpose systems for running a node project in a browser like [CodeSandbox](https://codesandbox.io) and [StackBlitz](https://stackblitz.com/) — the Playground will generate a very close approximation of the current environment with corresponding `package.json`, `tsconfig.json` and `index.{ts, tsx, js, jsx, .d.ts}` files and recreate that node project in one of the other services. This export gives you the chance to carry on working when you hit a wall with the available features in the Playground.

There's also a "Tweet this Playground" because why not?

---
# Source: Writing JavaScript.md
---
## Writing JavaScript

"Write JavaScript in the _TypeScript_ Playground, madness!" - maybe, but there's a few major cases for why you would want to do this:

1. **Learning typed-JavaScript** - JSDoc-flavoured JavaScript is TypeScript-lite without the tooling overhead and with weirder syntax. JSDoc-flavoured JavaScript is both a legitimate stepping stone to migrating to TypeScript and a perfectly good stopping point for getting richer tools without additional complexity.

1. **Debugging JavaScript .d.ts conversion** - TypeScript can generate `.d.ts` files from `.js` files, which gives library authors the chance to stay in JavaScript but still offer a rich developer experience to their users. The `.d.ts` sidebar tab offers a fast-feedback cycle for understanding how the code is understood by TypeScript.

1. **Experiment with code flow analysis and `jsconfig.json` settings** - A JavaScript project can use a `jsconfig.json` file to set up their tooling experience, and the Playground can be used to emulate that environment.

1. **Running JavaScript locally** - You can copy in modern JavaScript syntax, and it will be automatically downleveled to older JavaScript syntax which means you can reliably run it. Making it easy to do a quick 'does this work' playground and hit Run to see the output.

You can turn on JavaScript mode by opening the "TS Config" menu and changing the "language" to "JavaScript". This will add `?filetype=js` to the URL (note `?isJavaScript=true` is also supported for older links) and reload the Playground into a JavaScript context instead.

---
# Source: TypeScript Versions.md
---
## TypeScript Versions

The TypeScript Playground supports TypeScript versions all the way back to `3.3.3` (which was versioned as [`3.3.3333`](https://github.com/Microsoft/TypeScript/issues/30032)) up to the latest nightly build.

The ability to switch the version of TypeScript makes it easy to figure out potential regressions and to be able to let people test out new language features without having to upgrade their projects to (potentially) an unstable version of TypeScript. You can access the list of production TypeScript versions via a dropdown in the editor's toolbar inside the Playground. If there's a current beta or rc, that will show at the top.

The dropdown shows the highest patch version for a TypeScript release, but that is not every version available. You can refer to these two JSON files for the full list of [release versions](https://playgroundcdn.typescriptlang.org/indexes/releases.json) and [pre-release versions](https://playgroundcdn.typescriptlang.org/indexes/pre-releases.json).

Setting a TypeScript version will append `?ts=[version]` to your URL and reload. For example, setting the TypeScript version to 4.3.5 will add `?ts=4.3.5` to the URL, which is an OK segue to the overview of the [URL's structure](/play#handbook-10).

There's one special case where `?ts=next` will find the latest version of the TypeScript which was built for the Playground and use that.

---
# Source: Writing DTS Files.md
---
## Writing `.d.ts` Files

Those of us who have been doing TypeScript for a while will know that feeling when you first realise that you may have wrote a lot of TypeScript in a `.ts` file - but you find yourself having to start looking things up again when you are in a `.d.ts` file.

There are _a lot_ of similarities between a `.ts` file, but the rules are often subtly different in a `.d.ts` files and having a place where you can share and debug `.d.ts` files becomes extremely useful then.

The `.d.ts` mode can be turned on by changing the language to "TypeScript Definition" inside the "TS Config" panel.

---
# Source: README.md
---
# TypeScript Example Code

The English examples can be found in [`en/`](en/).

# TypeScript Example Code

These samples are built for hyperlinking between each-other
in a sandboxed environment like the TypeScript Playground.

Each example aims to cover one or two specific features to
either how JavaScript works in TypeScript, or features which
TypeScript has added to the language.

An example should make assumptions that the reader is in a
monaco/IDE-like environment which has a TSServer running for
to provide extra analysis. As well as a minor fluency in
JavaScript.

These examples are not set in stone, and we're open to new
ideas. If you'd like to help out and speak more than one
language, we'd love to see translations.

## Adding a new example section

Create a folder in the english section of the [`copy`](./copy) folder,
then add sub-folders per section which you'd want to have as headers
with 3-5 examples.

## Adding a localization

All localizations live inside the `copy` folder:

- There must be a `sections.json` in the root of each language
- A language is created by copying over an english example with the same path, and then translating it
- Any examples not copied over fall back to the english version
- You can change the name of an example for your language by having `//// { "title": 'c0d3 fl0w', ... }` in the first line of the example

Languages are compiled to TOC JSON files in [`generated`](./generated), one per language.

# Deployment

There is a table of contents JSON file which contains
all the useful metadata about the hierarchy and sort
order for the docs.

It's likely that we'll need to create this per translation
in the future, but for now the table of contents will
default to english.

The script is in [`scripts/generateTOC.js`](scripts/generateTOC.js), with  
\output of the build process is then copied into the `typescriptlang-org`
module under `static/js/examples` in [`scripts/copyFiles.js`](scripts/copyFiles.js).

---
# Source: CHANGELOG.md
---
# @typescript/vfs

## 1.6.4

### Patch Changes

- [#3509](https://github.com/microsoft/TypeScript-Website/pull/3509) [`0daa298`](https://github.com/microsoft/TypeScript-Website/commit/0daa298f2f4526f8c66baff00b8df0290e37a4d4) Thanks [@jakebailey](https://github.com/jakebailey)! - Bump dependencies

## 1.6.3

### Patch Changes

- [#3502](https://github.com/microsoft/TypeScript-Website/pull/3502) [`5e2b828`](https://github.com/microsoft/TypeScript-Website/commit/5e2b8285e01edffd888aa97002d082f6975f7bc1) Thanks [@jakebailey](https://github.com/jakebailey)! - Update for compatibility with TypeScript 6.0.

## 1.6.2

### Patch Changes

- [#3450](https://github.com/microsoft/TypeScript-Website/pull/3450) [`1843cf4`](https://github.com/microsoft/TypeScript-Website/commit/1843cf45e06193b3dc072088785fe2bfad477de5) Thanks [@yamcodes](https://github.com/yamcodes)! - Modify localStorage check to prevent crashes in Node 25

## 1.6.1

### Patch Changes

- [#3324](https://github.com/microsoft/TypeScript-Website/pull/3324) [`4a30b02`](https://github.com/microsoft/TypeScript-Website/commit/4a30b022bc0c1df6b6abb71c99c104f3b19f2c91) Thanks [@jakebailey](https://github.com/jakebailey)! - Update hardcoded list of known lib files

## 1.6.0

### Minor Changes

- [#3173](https://github.com/microsoft/TypeScript-Website/pull/3173) [`725841a`](https://github.com/microsoft/TypeScript-Website/commit/725841adc9e5b734ccb0663fccb2ba05d0dcca62) Thanks [@marklundin](https://github.com/marklundin)! - Adds `deleteFile` to the vfs api to which allows file to be removed from the file system.

### Patch Changes

- [#3165](https://github.com/microsoft/TypeScript-Website/pull/3165) [`441338c`](https://github.com/microsoft/TypeScript-Website/commit/441338c04fbbef834ffa1ac6dc0dc8816e9137fc) Thanks [@edemaine](https://github.com/edemaine)! - Use System's getDirectories if it's provided when constructing Host

## 1.5.3

### Patch Changes

- [#3038](https://github.com/microsoft/TypeScript-Website/pull/3038) [`0ea84b5`](https://github.com/microsoft/TypeScript-Website/commit/0ea84b59ae291aba677fe77ca059c4112e45fb9b) Thanks [@xiaoxiyao](https://github.com/xiaoxiyao)! - Fix the exception when file content is empty

- [#3038](https://github.com/microsoft/TypeScript-Website/pull/3038) [`0ea84b5`](https://github.com/microsoft/TypeScript-Website/commit/0ea84b59ae291aba677fe77ca059c4112e45fb9b) Thanks [@xiaoxiyao](https://github.com/xiaoxiyao)! - Fix `moduleDetection` compiler option is not working

- [#3015](https://github.com/microsoft/TypeScript-Website/pull/3015) [`6168ef4`](https://github.com/microsoft/TypeScript-Website/commit/6168ef49a4d08c0b5658732d23625bbcc6049109) Thanks [@antfu](https://github.com/antfu)! - support non-hoisted `node_module` structure

- [#3072](https://github.com/microsoft/TypeScript-Website/pull/3072) [`9f8dea2`](https://github.com/microsoft/TypeScript-Website/commit/9f8dea2c19a3b6028148090f5e8cba8eea086ec3) Thanks [@KiranJKurian](https://github.com/KiranJKurian)! - Fix missing typescript peer dependency

- [#3140](https://github.com/microsoft/TypeScript-Website/pull/3140) [`26f3e56`](https://github.com/microsoft/TypeScript-Website/commit/26f3e566aa8fff235a8f6927ef2c33b28be4fe89) Thanks [@jakebailey](https://github.com/jakebailey)! - Don't depend on DOM types in createDefaultMapFromCDN

- [#3000](https://github.com/microsoft/TypeScript-Website/pull/3000) [`71776ae`](https://github.com/microsoft/TypeScript-Website/commit/71776aecc1b56289ab56d240a9272ce83686ef1a) Thanks [@antfu](https://github.com/antfu)! - Handle `.d.cts` and `.d.mts` files

## 1.5.2

### Patch Changes

- 642ea11: Move playground CDN to new, stable URL

## 1.5.1

### Patch Changes

- 46eba14: Initial bump for changesets

### 1.5

- Makes `createDefaultMapFromNodeModules` pull all the `.d.ts` files from the node_modules folder, not just the `.d.ts` files which were known ahead of time.
- Updates the known .d.s files to include ones from TypeScript 5.1 beta.

### 1.3

- Adds a JS file into the npm tarball for using with a vanilla script tag, which sets `global.tsvfs` with exported function.

Unpkg URLS:

- https://unpkg.com/browse/@typescript/vfs@dist/vfs.globals.js

### 1.2

Updates `createFSBackedSystem` to rely more on the default TypeScript system object which should see twoslash code samples re-using the node_modules from the local project.

### 0.0 - 1.0 - 1.1

Created the lib, got it working

---
# Source: README.md
---
### TypeScript VFS

A Map based TypeScript Virtual File System.

Useful when you need to:

- Run TypeScript in the browser
- Run virtual TypeScript environments where files on disk aren't the source of truth

### Usage

You start with creating a map which represents all the files in the virtual `ts.System`:

```ts
import { createSystem } from "@typescript/vfs"

const fsMap = new Map<string, string>()
fsMap.set("index.ts", 'const a = "Hello World"')

const system = createSystem(fsMap)
```

Then you can create a virtual TypeScript Environment:

```ts
import { createSystem, createVirtualTypeScriptEnvironment } from "@typescript/vfs"
import ts from "typescript"

const fsMap = new Map<string, string>()
const system = createSystem(fsMap)

const compilerOpts = {}
const env = createVirtualTypeScriptEnvironment(system, ["index.ts"], ts, compilerOpts)

// You can then interact with the languageService to introspect the code
env.languageService.getDocumentHighlights("index.ts", 0, ["index.ts"])
```

When working in tests, or in environments with file system access, you can switch your virtual system with `ts.sys` to use the real filesystem with the virtual environment.

## API

You're most likely interested in the API available in `env.languageService`, here it is as of 3.7.4:

<!-- prettier-ignore-start -->

```ts
interface LanguageService {
    cleanupSemanticCache(): void;
    getSyntacticDiagnostics(fileName: string): DiagnosticWithLocation[];
    getSemanticDiagnostics(fileName: string): Diagnostic[];
    getSuggestionDiagnostics(fileName: string): DiagnosticWithLocation[];
    getCompilerOptionsDiagnostics(): Diagnostic[];
    getEncodedSyntacticClassifications(fileName: string, span: TextSpan): Classifications;
    getEncodedSemanticClassifications(fileName: string, span: TextSpan): Classifications;
    getCompletionsAtPosition(fileName: string, position: number, options: GetCompletionsAtPositionOptions | undefined): WithMetadata<CompletionInfo> | undefined;
    getCompletionEntryDetails(fileName: string, position: number, name: string, formatOptions: FormatCodeOptions | FormatCodeSettings | undefined, source: string | undefined, preferences: UserPreferences | undefined): CompletionEntryDetails | undefined;
    getCompletionEntrySymbol(fileName: string, position: number, name: string, source: string | undefined): Symbol | undefined;
    getQuickInfoAtPosition(fileName: string, position: number): QuickInfo | undefined;
    getNameOrDottedNameSpan(fileName: string, startPos: number, endPos: number): TextSpan | undefined;
    getBreakpointStatementAtPosition(fileName: string, position: number): TextSpan | undefined;
    getSignatureHelpItems(fileName: string, position: number, options: SignatureHelpItemsOptions | undefined): SignatureHelpItems | undefined;
    getRenameInfo(fileName: string, position: number, options?: RenameInfoOptions): RenameInfo;
    findRenameLocations(fileName: string, position: number, findInStrings: boolean, findInComments: boolean, providePrefixAndSuffixTextForRename?: boolean): readonly RenameLocation[] | undefined;
    getSmartSelectionRange(fileName: string, position: number): SelectionRange;
    getDefinitionAtPosition(fileName: string, position: number): readonly DefinitionInfo[] | undefined;
    getDefinitionAndBoundSpan(fileName: string, position: number): DefinitionInfoAndBoundSpan | undefined;
    getTypeDefinitionAtPosition(fileName: string, position: number): readonly DefinitionInfo[] | undefined;
    getImplementationAtPosition(fileName: string, position: number): readonly ImplementationLocation[] | undefined;
    getReferencesAtPosition(fileName: string, position: number): ReferenceEntry[] | undefined;
    findReferences(fileName: string, position: number): ReferencedSymbol[] | undefined;
    getDocumentHighlights(fileName: string, position: number, filesToSearch: string[]): DocumentHighlights[] | undefined;
    getNavigateToItems(searchValue: string, maxResultCount?: number, fileName?: string, excludeDtsFiles?: boolean): NavigateToItem[];
    getNavigationBarItems(fileName: string): NavigationBarItem[];
    getNavigationTree(fileName: string): NavigationTree;
    getOutliningSpans(fileName: string): OutliningSpan[];
    getTodoComments(fileName: string, descriptors: TodoCommentDescriptor[]): TodoComment[];
    getBraceMatchingAtPosition(fileName: string, position: number): TextSpan[];
    getIndentationAtPosition(fileName: string, position: number, options: EditorOptions | EditorSettings): number;
    getFormattingEditsForRange(fileName: string, start: number, end: number, options: FormatCodeOptions | FormatCodeSettings): TextChange[];
    getFormattingEditsForDocument(fileName: string, options: FormatCodeOptions | FormatCodeSettings): TextChange[];
    getFormattingEditsAfterKeystroke(fileName: string, position: number, key: string, options: FormatCodeOptions | FormatCodeSettings): TextChange[];
    getDocCommentTemplateAtPosition(fileName: string, position: number): TextInsertion | undefined;
    isValidBraceCompletionAtPosition(fileName: string, position: number, openingBrace: number): boolean;
    getJsxClosingTagAtPosition(fileName: string, position: number): JsxClosingTagInfo | undefined;
    getSpanOfEnclosingComment(fileName: string, position: number, onlyMultiLine: boolean): TextSpan | undefined;
    toLineColumnOffset(fileName: string, position: number): LineAndCharacter;
    getCodeFixesAtPosition(fileName: string, start: number, end: number, errorCodes: readonly number[], formatOptions: FormatCodeSettings, preferences: UserPreferences): readonly CodeFixAction[];
    getCombinedCodeFix(scope: CombinedCodeFixScope, fixId: {}, formatOptions: FormatCodeSettings, preferences: UserPreferences): CombinedCodeActions;
    applyCodeActionCommand(action: CodeActionCommand, formatSettings?: FormatCodeSettings): Promise<ApplyCodeActionCommandResult>;
    applyCodeActionCommand(action: CodeActionCommand[], formatSettings?: FormatCodeSettings): Promise<ApplyCodeActionCommandResult[]>;
    applyCodeActionCommand(action: CodeActionCommand | CodeActionCommand[], formatSettings?: FormatCodeSettings): Promise<ApplyCodeActionCommandResult | ApplyCodeActionCommandResult[]>;
    getApplicableRefactors(fileName: string, positionOrRange: number | TextRange, preferences: UserPreferences | undefined): ApplicableRefactorInfo[];
    getEditsForRefactor(fileName: string, formatOptions: FormatCodeSettings, positionOrRange: number | TextRange, refactorName: string, actionName: string, preferences: UserPreferences | undefined): RefactorEditInfo | undefined;
    organizeImports(scope: OrganizeImportsScope, formatOptions: FormatCodeSettings, preferences: UserPreferences | undefined): readonly FileTextChanges[];
    getEditsForFileRename(oldFilePath: string, newFilePath: string, formatOptions: FormatCodeSettings, preferences: UserPreferences | undefined): readonly FileTextChanges[];
    getEmitOutput(fileName: string, emitOnlyDtsFiles?: boolean, forceDtsEmit?: boolean): EmitOutput;
    getProgram(): Program | undefined;
}
```
<!-- prettier-ignore-end -->

## Usage

#### When working with Web

It's **very** likely that you will need to set up your lib `*.d.ts` files to use this.

If you are running in an environment where you have access to the `node_modules` folder, then you can can write some code like this:

```ts
const getLib = (name: string) => {
  const lib = dirname(require.resolve("typescript"))
  return readFileSync(join(lib, name), "utf8")
}

const addLib = (name: string, map: Map<string, string>) => {
  map.set("/" + name, getLib(name))
}

const createDefaultMap2015 = () => {
  const fsMap = new Map<string, string>()
  addLib("lib.es2015.d.ts", fsMap)
  addLib("lib.es2015.collection.d.ts", fsMap)
  addLib("lib.es2015.core.d.ts", fsMap)
  addLib("lib.es2015.generator.d.ts", fsMap)
  addLib("lib.es2015.iterable.d.ts", fsMap)
  addLib("lib.es2015.promise.d.ts", fsMap)
  addLib("lib.es2015.proxy.d.ts", fsMap)
  addLib("lib.es2015.reflect.d.ts", fsMap)
  addLib("lib.es2015.symbol.d.ts", fsMap)
  addLib("lib.es2015.symbol.wellknown.d.ts", fsMap)
  addLib("lib.es5.d.ts", fsMap)
  return fsMap
}
```

This list is the default set of definitions (it's important to note that different options for `target` or `lib` will affect what this list looks like) and you are grabbing the library's content from the local dependency of TypeScript.

Keeping on top of this list is quite a lot of work, so this library ships functions for generating a map with with these pre-filled from a version of TypeScript available on disk.

Note: it's possible for this list to get out of sync with TypeScript over time. It was last synced with TypeScript 3.8.0-rc.

```ts
import { createDefaultMapFromNodeModules } from "@typescript/vfs"
import ts from "typescript"

const fsMap = createDefaultMapFromNodeModules({ target: ts.ScriptTarget.ES2015 })
fsMap.set("index.ts", "const hello = 'hi'")
// ...
```

If you don't have access to `node_modules`, then you can use the TypeScript CDN or unpkg to fetch the lib files. This could be up to about 1.5MB, and you should probably store the values in `localStorage` so that users only have to grab it once.

This is handled for you via `createDefaultMapFromCDN`.

```ts
import { createDefaultMapFromCDN } from "@typescript/vfs"
import ts from "typescript"
import lzstring from "lz-string"

const start = async () => {
  const shouldCache = true
  // This caches the lib files in the site's localStorage
  const fsMap = await createDefaultMapFromCDN({ target: ts.ScriptTarget.ES2015 }, "3.7.3", shouldCache, ts)

  // This stores the lib files as a zipped string to save space in the cache
  const otherMap = await createDefaultMapFromCDN({ target: ts.ScriptTarget.ES2015 }, "3.7.3", shouldCache, ts, lzstring)

  fsMap.set("index.ts", "const hello = 'hi'")
  // ...
}

start()
```

The CDN cache:

- Automatically purges items which use a different version of TypeScript to save space
- Can use a copy of the lz-string module for compressing/decompressing the lib files

#### When working with node

If you can reliably access the file-system, then you can have a simpler time:

```ts
const compilerOpts: ts.CompilerOptions = { target: ts.ScriptTarget.ES2016, esModuleInterop: true }
const fsMap = new Map<string, string>()

// If using imports where the types don't directly match up to their FS representation (like the
// imports for node) then use triple-slash directives to make sure globals are set up first.
const content = `/// <reference types="node" />\nimport * as path from 'path';\npath.`
fsMap.set("index.ts", content)

// By providing a project root, then the system knows how to resolve node_modules correctly
const projectRoot = path.join(__dirname, "..")
const system = createFSBackedSystem(fsMap, projectRoot)
const env = createVirtualTypeScriptEnvironment(system, ["index.ts"], ts, compilerOpts)

// Requests auto-completions at `path.|`
const completions = env.languageService.getCompletionsAtPosition("index.ts", content.length, {})
```

`createFSBackedSystem` will let you hover a virtual environment on top of the file system at a particular path.

### A full example

What does a full example look like? This comes basically verbatim from the TypeScript Sandbox codebase:

```ts
import ts from "typescript"
import tsvfs from "@typescript/vfs"
import lzstring from "lz-string"

const fsMap = await tsvfs.createDefaultMapFromCDN(compilerOptions, ts.version, true, ts, lzstring)
fsMap.set("index.ts", "// main TypeScript file content")

const system = tsvfs.createSystem(fsMap)
const host = tsvfs.createVirtualCompilerHost(system, compilerOptions, ts)

const program = ts.createProgram({
  rootNames: [...fsMap.keys()],
  options: compilerOptions,
  host: host.compilerHost,
})

// This will update the fsMap with new files
// for the .d.ts and .js files
program.emit()

// Now I can look at the AST for the .ts file too
const index = program.getSourceFile("index.ts")
```

## Using this Dependency

This package can be used as a commonjs import, an esmodule and directly via a script tag which edits the global namespace. All of these files are embedded inside the released packages.

---
# Source: CHANGELOG.md
---
# @typescript/ata

## 0.9.8

### Patch Changes

- [#3391](https://github.com/microsoft/TypeScript-Website/pull/3391) [`5e10fd0`](https://github.com/microsoft/TypeScript-Website/commit/5e10fd05e4fd5ac42ac4e95baecaa7b8b0e8fa19) Thanks [@ChaseMalik](https://github.com/ChaseMalik)! - Remove duplicate modules from getReferencesForModule

## 0.9.7

### Patch Changes

- [#3191](https://github.com/microsoft/TypeScript-Website/pull/3191) [`1d0af97`](https://github.com/microsoft/TypeScript-Website/commit/1d0af97318b79943fe0bfa8871ee6e8c584c9af5) Thanks [@Renegade334](https://github.com/Renegade334)! - Always treat `node:` modules as Node, expand list of known Node modules

## 0.9.6

### Patch Changes

- [#2977](https://github.com/microsoft/TypeScript-Website/pull/2977) [`7691811`](https://github.com/microsoft/TypeScript-Website/commit/7691811c180e3b352cf4e888387d1edfc10f5252) Thanks [@curran](https://github.com/curran)! - Widen typescript peer dependency range

- [#3000](https://github.com/microsoft/TypeScript-Website/pull/3000) [`71776ae`](https://github.com/microsoft/TypeScript-Website/commit/71776aecc1b56289ab56d240a9272ce83686ef1a) Thanks [@antfu](https://github.com/antfu)! - Handle `.d.cts` and `.d.mts` files

- [#3002](https://github.com/microsoft/TypeScript-Website/pull/3002) [`fd776c0`](https://github.com/microsoft/TypeScript-Website/commit/fd776c05bb8fa9c897d18fa237af39ae8da03a7c) Thanks [@antfu](https://github.com/antfu)! - Fix return type of `setupTypeAcquisition`

## 0.9.5

### Patch Changes

- 46eba14: Initial bump for changesets

---
# Source: README.md
---
# TypeScript - Automatic Type Acquisition

A dependency for downloading `*.d.ts` files corresponding to a Node.js source file. Relies on API's provided by [jsdelivr](https://www.jsdelivr.com).

### Usage

```ts
// Create the function for running ATA with a series of callbacks
const ata = setupTypeAcquisition({
  projectName: "My ATA Project",
  typescript: ts,
  logger: console,
  delegate: {
    receivedFile: (code: string, path: string) => {
      // Add code to your runtime at the path...
    },
    started: () => {
      console.log("ATA start")
    },
    progress: (downloaded: number, total: number) => {
      console.log(`Got ${downloaded} out of ${total}`)
    },
    finished: vfs => {
      console.log("ATA done", vfs)
    },
  },
})

// Run that function with the new sourcefile
ata(`import danger from "danger"`)
```

You can call `ata` when it is convenient to you, it will not grab the same dependencies twice. The callbacks for `started` and `finished` are only triggered when some work is going to happen, so you can use those for UI elements show/hide. `progress` is triggered every 5 downloads.

### How it works

At a high level, for this input code:

```
import danger from "danger"
```

The library will

- Look for the latest npm module of "danger", then get its file list
- As there are `.d.ts` files to download in the dep, then it triggers `started`
- Download the `*.d.ts` files for "danger" from the npm module "danger"
- Read those `.d.ts` and look at these modules from usage:
  - `"node-fetch"` - it sees that "node-fetch" has no `.d.ts` files and gets them from "@types/node-fetch"
  - `"commander"` - it sees that command ships its own types
  - `"@octokit/rest"` - it sees that octokit/rest ships its own types
  - `"gitlab"` - it also sees
- Recurse though their dependencies too.
- Once those are done, trigger `finished` with a Map of the `vfs` if you prefer to set them in bulk.

### Niceties

Users can give a specific npm version or tag to work from instead of the default "latest":

```ts
import { xy } from "xyz" // types: beta
```

If this isn't something you want, I'm not against a flag to disable it.

---
# Source: CHANGELOG.md
---
# @typescript/sandbox

## 0.1.14

### Patch Changes

- [#3523](https://github.com/microsoft/TypeScript-Website/pull/3523) [`9953d5b`](https://github.com/microsoft/TypeScript-Website/commit/9953d5bf9168335e3ddad7b1752b3213f3f9a636) Thanks [@Josh-Cena](https://github.com/Josh-Cena)! - getInitialCode should not use URL hash without full prefix

## 0.1.13

### Patch Changes

- [#3505](https://github.com/microsoft/TypeScript-Website/pull/3505) [`2072484`](https://github.com/microsoft/TypeScript-Website/commit/20724842b6eaf09f5c5d0ee40272c5569fe5c37d) Thanks [@DanielRosenwasser](https://github.com/DanielRosenwasser)! - Fix Ctrl+arrow keys in Firefox.

## 0.1.12

### Patch Changes

- Updated dependencies [[`0daa298`](https://github.com/microsoft/TypeScript-Website/commit/0daa298f2f4526f8c66baff00b8df0290e37a4d4)]:
  - @typescript/vfs@1.6.4

## 0.1.11

### Patch Changes

- Updated dependencies [[`5e2b828`](https://github.com/microsoft/TypeScript-Website/commit/5e2b8285e01edffd888aa97002d082f6975f7bc1)]:
  - @typescript/vfs@1.6.3

## 0.1.10

### Patch Changes

- Updated dependencies [[`1843cf4`](https://github.com/microsoft/TypeScript-Website/commit/1843cf45e06193b3dc072088785fe2bfad477de5)]:
  - @typescript/vfs@1.6.2

## 0.1.9

### Patch Changes

- Updated dependencies [[`5e10fd0`](https://github.com/microsoft/TypeScript-Website/commit/5e10fd05e4fd5ac42ac4e95baecaa7b8b0e8fa19)]:
  - @typescript/ata@0.9.8

## 0.1.8

### Patch Changes

- Updated dependencies [[`4a30b02`](https://github.com/microsoft/TypeScript-Website/commit/4a30b022bc0c1df6b6abb71c99c104f3b19f2c91)]:
  - @typescript/vfs@1.6.1

## 0.1.7

### Patch Changes

- Updated dependencies [[`1d0af97`](https://github.com/microsoft/TypeScript-Website/commit/1d0af97318b79943fe0bfa8871ee6e8c584c9af5)]:
  - @typescript/ata@0.9.7

## 0.1.6

### Patch Changes

- Updated dependencies [[`441338c`](https://github.com/microsoft/TypeScript-Website/commit/441338c04fbbef834ffa1ac6dc0dc8816e9137fc), [`725841a`](https://github.com/microsoft/TypeScript-Website/commit/725841adc9e5b734ccb0663fccb2ba05d0dcca62)]:
  - @typescript/vfs@1.6.0

## 0.1.5

### Patch Changes

- [#3000](https://github.com/microsoft/TypeScript-Website/pull/3000) [`71776ae`](https://github.com/microsoft/TypeScript-Website/commit/71776aecc1b56289ab56d240a9272ce83686ef1a) Thanks [@antfu](https://github.com/antfu)! - Handle `.d.cts` and `.d.mts` files

- Updated dependencies [[`0ea84b5`](https://github.com/microsoft/TypeScript-Website/commit/0ea84b59ae291aba677fe77ca059c4112e45fb9b), [`7691811`](https://github.com/microsoft/TypeScript-Website/commit/7691811c180e3b352cf4e888387d1edfc10f5252), [`0ea84b5`](https://github.com/microsoft/TypeScript-Website/commit/0ea84b59ae291aba677fe77ca059c4112e45fb9b), [`6168ef4`](https://github.com/microsoft/TypeScript-Website/commit/6168ef49a4d08c0b5658732d23625bbcc6049109), [`9f8dea2`](https://github.com/microsoft/TypeScript-Website/commit/9f8dea2c19a3b6028148090f5e8cba8eea086ec3), [`26f3e56`](https://github.com/microsoft/TypeScript-Website/commit/26f3e566aa8fff235a8f6927ef2c33b28be4fe89), [`71776ae`](https://github.com/microsoft/TypeScript-Website/commit/71776aecc1b56289ab56d240a9272ce83686ef1a), [`fd776c0`](https://github.com/microsoft/TypeScript-Website/commit/fd776c05bb8fa9c897d18fa237af39ae8da03a7c)]:
  - @typescript/vfs@1.5.3
  - @typescript/ata@0.9.6

## 0.1.4

### Patch Changes

- Updated dependencies [642ea11]
  - @typescript/vfs@1.5.2

## 0.1.3

### Patch Changes

- 46eba14: Initial bump for changesets
- Updated dependencies [46eba14]
  - @typescript/vfs@1.5.1
  - @typescript/ata@0.9.5

---
# Source: README.md
---
# TypeScript Sandbox

The TypeScript Sandbox is the editor part of the TypeScript Playground. It's effectively an opinionated fork of
monaco-typescript with extra extension points so that projects like the TypeScript Playground can exist.

This project is useful to you if:

- You want to present users of your library with a JS editor which has a typed API (in JS or TS)
- You want to work with monaco at a higher abstraction level

## Goals

- Support multiple versions of TypeScript (via supporting older builds of monaco-typescript)
- Easy to use when trying to replace code inline on a website
- Support extension points required to build Playground
- High level APIs for things like Automatic Type Acquisition or DTS additions

## Builds

This library is published to the CDN as an AMD module. This is the same format that vscode/monaco use, and so you can use
the same runtime loader patterns for importing into your web page. This package is also available as an ESM and CJS module on NPM.

## Installation

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
  </head>
  <div id="loader">Loading...</div>
  <div id="monaco-editor-embed" style="height: 800px;" />
  <script>
    // First set up the VSCode loader in a script tag
    const getLoaderScript = document.createElement("script")
    getLoaderScript.src = "https://www.typescriptlang.org/js/vs.loader.js"
    getLoaderScript.async = true
    getLoaderScript.onload = () => {
      // Now the loader is ready, tell require where it can get the version of monaco, and the sandbox
      // This version uses the latest version of the sandbox, which is used on the TypeScript website

      // For the monaco version you can use unpkg or the TypeScript web infra CDN
      // You can see the available releases for TypeScript here:
      // https://playgroundcdn.typescriptlang.org/indexes/releases.json
      //
      require.config({
        paths: {
          vs: "https://playgroundcdn.typescriptlang.org/cdn/4.0.5/monaco/min/vs",
          // vs: 'https://unpkg.com/@typescript-deploys/monaco-editor@4.0.5/min/vs',
          sandbox: "https://www.typescriptlang.org/js/sandbox",
        },
        // This is something you need for monaco to work
        ignoreDuplicateModules: ["vs/editor/editor.main"],
      })

      // Grab a copy of monaco, TypeScript and the sandbox
      require(["vs/editor/editor.main", "vs/language/typescript/tsWorker", "sandbox/index"], (
        main,
        _tsWorker,
        sandboxFactory
      ) => {
        const initialCode = `import {markdown, danger} from "danger"

export default async function () {
    // Check for new @types in devDependencies
    const packageJSONDiff = await danger.git.JSONDiffForFile("package.json")
    const newDeps = packageJSONDiff.devDependencies.added
    const newTypesDeps = newDeps?.filter(d => d.includes("@types")) ?? []
    if (newTypesDeps.length){
        markdown("Added new types packages " + newTypesDeps.join(", "))
    }
}
`

        const isOK = main && window.ts && sandboxFactory
        if (isOK) {
          document.getElementById("loader").parentNode.removeChild(document.getElementById("loader"))
        } else {
          console.error("Could not get all the dependencies of sandbox set up!")
          console.error("main", !!main, "ts", !!window.ts, "sandbox", !!sandbox)
          return
        }

        // Create a sandbox and embed it into the div #monaco-editor-embed
        const sandboxConfig = {
          text: initialCode,
          compilerOptions: {},
          domID: "monaco-editor-embed",
        }

        const sandbox = sandboxFactory.createTypeScriptSandbox(sandboxConfig, main, window.ts)
        sandbox.editor.focus()
      })
    }

    document.body.appendChild(getLoaderScript)
  </script>
</html>
```

---
# Source: README.md
---
# TypeScript Playground

This is the JS tooling which powers the https://www.typescriptlang.org/play/

It is more or less vanilla DOM-oriented JavaScript with as few dependencies as possible. Originally based on the
work by [Artem Tyurin](https://github.com/agentcooper/typescript-play) but now it's diverged far from that fork.

## Architecture

The playground library sits above the [TypeScript sandbox](../sandbox), and provides features like:

- The code samples support
- The navigation bars, and compiler flags UI
- The sidebar plugin infrastructure for showing JS/DTS/etc
- The export to Code Sandbox/TS AST Viewer/etc features

When deciding where to add a feature to the TypeScript playground, consider if it would be useful to anyone showing
TypeScript in a REPL. If yes, add it to the sandbox and expose a function for the playground to use. For example
Automatic Type Acquisition is a feature which lives in the sandbox and not the playground because pretty much anyone showing TypeScript code would want it.

## Link Syntax

The Playground supports a set of query inputs from the URL. The hash is used to reflect the code:

- `#code/PRA` - A base64 and zipped version of the code which should live in the editor
- `#src=The%20code` - URLEncoded way to have the code for the editor
- `#example/generic-functions` - Grab the code from an example with the id generic-functions

Or to trigger some action by default:

- `#show-examples` - When the app is loaded, show the examples popover
- `#show-whatisnew` - When the app is loaded, show the examples popover

Then queries tend to be about changing the state of the Playground setup from the default:

- `?ts=3.9.2` - Sets the TypeScript version, the list of supported versions is in these [two](https://playgroundcdn.typescriptlang.org/indexes/pre-releases.json) [json](https://playgroundcdn.typescriptlang.org/indexes/releases.json) files.

  There are two special cases for the `ts` option:

  - `ts=next`: Use the most recent [nightly build](https://www.typescriptlang.org/docs/handbook/nightly-builds.html).
  - `ts=dev`: Use your [local developer's build of TypeScript](https://github.com/microsoft/TypeScript/blob/main/scripts/createPlaygroundBuild.js)

- `?flag=value` - Any compiler flag referenced in can be set from a query
- `?filetype=js|ts|dts` - Tells the Playground to set the editor's type

---
# Source: README.md
---
## TypeScript Website

This a pretty traditional Gatsby site. You can start it up via:

```sh
pnpm start
```

Which starts up a dev server.

---
# Source: README.md
---
## Default Pages are not really used in this repo

Only things which are completely unlocalized, like the `/dev/x` pages use this part of Gatsbys. The real pages are
found in [`src/templates/pages`](../templates/pages).

---
# Source: README.md
---
### Generating the TSConfig Reference

This "package" hosts multi-lingual docs for the TSConfig. As much as possible is based
off pulling data from `require("typescript")` then augmented with markdown from inside the
[`./copy`](./copy) folder.

Roughly:

```sh
TypeScript Compiler + `tsconfigRules.ts` -> `generateJSON.ts` -> JSON (in output) -> `generateMarkdown.ts` -> Markdown (in output)
```

This happens per-language with fallbacks to English for any missing docs.

## Contributing

To improve a single compiler option's documentation; all you need to do is go into the [`./copy`](./copy) folder and
edit the page option in markdown and send a PR. No need to leave GitHub.

Then, during a deploy, all of the markdown files are bundled together and any merged changes are uploaded.

## Contributing a new language

If you'd like to create a new language:

Create a new subfolder in `./copy` with your language code and then make sure the files you work on have the same
name as English and your changes will overwrite the English version. You will need

## Building

The TSConfig reference is created by a two step process:

- Creating the JSON dump of all the useful info via [`./scripts/generateJSON.ts`](scripts/generateJSON.ts) which you can find in [`./data`](./data).
- A script which uses the JSON, and the copy to generate per-language markdown docs which are picked up by the typescriptlang-org Gatsby site at `http://localhost:8000/tsconfig`

You can run these commands from the root of the repo:

```sh
pnpm run --filter=tsconfig-reference generate-json

pnpm run --filter=tsconfig-reference generate-markdown
```

You can validate any codeblocks which use twoslash via the script:

```sh
pnpm run --filter=tsconfig-reference test

# or to just run the linter without a build
pnpm run --filter=tsconfig-reference lint

# or to just one one linter
pnpm run --filter=tsconfig-reference lint resolveJson
```

You can debug twoslash by setting the environment var `DEBUG="*"` in all of these too.

---
# Source: include.md
---
---
display: "Include"
oneline: "Specify a list of modules which to acquire types for."
---

If you have a JavaScript project where TypeScript needs additional guidance to understand global dependencies, or have disabled the built-in inference via [`disableFilenameBasedTypeAcquisition`](#disableFilenameBasedTypeAcquisition).

You can use `include` to specify which types should be used from DefinitelyTyped:

```json
{
  "typeAcquisition": {
    "include": ["jquery"]
  }
}
```

---
# Source: exclude.md
---
---
display: "Exclude"
oneline: "Specify a list of modules which to exclude from type acquisition."
---

Offers a config for disabling the type-acquisition for a certain module in JavaScript projects. This can be useful for projects which include other libraries in testing infrastructure which aren't needed in the main application.

```json
{
  "typeAcquisition": {
    "exclude": ["jest", "mocha"]
  }
}
```

---
# Source: explainFiles.md
---
---
display: "Explain Files"
oneline: "Print files read during the compilation including why it was included."
---

Print names of files which TypeScript sees as a part of your project and the reason they are part of the compilation.

For example, with this project of just a single `index.ts` file

```sh
example
├── index.ts
├── package.json
└── tsconfig.json
```

Using a `tsconfig.json` which has `explainFiles` set to true:

```json
{
  "compilerOptions": {
    "target": "es5",
    "module": "commonjs",
    "explainFiles": true
  }
}
```

Running TypeScript against this folder would have output like this:

```
❯ tsc
node_modules/typescript/lib/lib.d.ts
  Default library for target 'es5'
node_modules/typescript/lib/lib.es5.d.ts
  Library referenced via 'es5' from file 'node_modules/typescript/lib/lib.d.ts'
node_modules/typescript/lib/lib.dom.d.ts
  Library referenced via 'dom' from file 'node_modules/typescript/lib/lib.d.ts'
node_modules/typescript/lib/lib.webworker.importscripts.d.ts
  Library referenced via 'webworker.importscripts' from 
    file 'node_modules/typescript/lib/lib.d.ts'
node_modules/typescript/lib/lib.scripthost.d.ts
  Library referenced via 'scripthost' 
    from file 'node_modules/typescript/lib/lib.d.ts'
index.ts
  Matched by include pattern '**/*' in 'tsconfig.json'
```

The output above show:

- The initial lib.d.ts lookup based on [`target`](#target), and the chain of `.d.ts` files which are referenced
- The `index.ts` file located via the default pattern of [`include`](#include)

This option is intended for debugging how a file has become a part of your compile.

---
# Source: strictNullChecks.md
---
---
display: "Strict Null Checks"
oneline: "When type checking, take into account `null` and `undefined`."
---

When `strictNullChecks` is `false`, `null` and `undefined` are effectively ignored by the language.
This can lead to unexpected errors at runtime.

When `strictNullChecks` is `true`, `null` and `undefined` have their own distinct types and you'll get a type error if you try to use them where a concrete value is expected.

For example with this TypeScript code, `users.find` has no guarantee that it will actually find a user, but you can
write code as though it will:

```ts twoslash
// @strictNullChecks: false
// @target: ES2015
declare const loggedInUsername: string;

const users = [
  { name: "Oby", age: 12 },
  { name: "Heera", age: 32 },
];

const loggedInUser = users.find((u) => u.name === loggedInUsername);
console.log(loggedInUser.age);
```

Setting `strictNullChecks` to `true` will raise an error that you have not made a guarantee that the `loggedInUser` exists before trying to use it.

```ts twoslash
// @errors: 2339 2532 18048
// @target: ES2020
// @strictNullChecks
declare const loggedInUsername: string;

const users = [
  { name: "Oby", age: 12 },
  { name: "Heera", age: 32 },
];

const loggedInUser = users.find((u) => u.name === loggedInUsername);
console.log(loggedInUser.age);
```

The second example failed because the array's `find` function looks a bit like this simplification:

```ts
// When strictNullChecks: true
type Array = {
  find(predicate: (value: any, index: number) => boolean): S | undefined;
};

// When strictNullChecks: false the undefined is removed from the type system,
// allowing you to write code which assumes it always found a result
type Array = {
  find(predicate: (value: any, index: number) => boolean): S;
};
```

---
# Source: baseUrl.md
---
---
display: "Base URL"
oneline: "Specify the base directory to resolve bare specifier module names."
---

Sets a base directory from which to resolve bare specifier module names. For example, in the directory structure:

```
project
├── ex.ts
├── hello
│   └── world.ts
└── tsconfig.json
```

With `"baseUrl": "./"`, TypeScript will look for files starting at the same folder as the `tsconfig.json`:

```ts
import { helloWorld } from "hello/world";

console.log(helloWorld);
```

This resolution has higher priority than lookups from `node_modules`.

This feature was designed for use in conjunction with AMD module loaders in the browser, and is not recommended in any other context. As of TypeScript 4.1, `baseUrl` is no longer required to be set when using [`paths`](#paths).
---
# Source: generateTrace.md
---
---
display: "generateTrace"
oneline: "Generates an event trace and a list of types."
---
Generates an event trace and a list of types.
 

---
# Source: files.md
---
---
display: "Files"
oneline: "Include a list of files. This does not support glob patterns, as opposed to [`include`](#include)."
---

Specifies an allowlist of files to include in the program. An error occurs if any of the files can't be found.

```json tsconfig
{
  "compilerOptions": {},
  "files": [
    "core.ts",
    "sys.ts",
    "types.ts",
    "scanner.ts",
    "parser.ts",
    "utilities.ts",
    "binder.ts",
    "checker.ts",
    "tsc.ts"
  ]
}
```

This is useful when you only have a small number of files and don't need to use a glob to reference many files.
If you need that then use [`include`](#include).

---
# Source: downlevelIteration.md
---
---
display: "Downlevel Iteration"
oneline: "Emit more compliant, but verbose and less performant JavaScript for iteration."
---

Downleveling is TypeScript's term for transpiling to an older version of JavaScript.
This flag is to enable support for a more accurate implementation of how modern JavaScript iterates through new concepts in older JavaScript runtimes.

ECMAScript 6 added several new iteration primitives: the `for / of` loop (`for (el of arr)`), Array spread (`[a, ...b]`), argument spread (`fn(...args)`), and `Symbol.iterator`.
`downlevelIteration` allows for these iteration primitives to be used more accurately in ES5 environments if a `Symbol.iterator` implementation is present.

#### Example: Effects on `for / of`

With this TypeScript code:

```ts twoslash
const str = "Hello!";
for (const s of str) {
  console.log(s);
}
```

Without `downlevelIteration` enabled, a `for / of` loop on any object is downleveled to a traditional `for` loop:

```ts twoslash
// @target: ES5
// @showEmit
const str = "Hello!";
for (const s of str) {
  console.log(s);
}
```

This is often what people expect, but it's not 100% compliant with ECMAScript iteration protocol.
Certain strings, such as emoji (😜), have a `.length` of 2 (or even more!), but should iterate as 1 unit in a `for-of` loop.
See [this blog post by Jonathan New](https://blog.jonnew.com/posts/poo-dot-length-equals-two) for a longer explanation.

When `downlevelIteration` is enabled, TypeScript will use a helper function that checks for a `Symbol.iterator` implementation (either native or polyfill).
If this implementation is missing, you'll fall back to index-based iteration.

```ts twoslash
// @target: ES5
// @downlevelIteration
// @showEmit
const str = "Hello!";
for (const s of str) {
  console.log(s);
}
```

You can use [tslib](https://www.npmjs.com/package/tslib) via [`importHelpers`](#importHelpers) to reduce the amount of inline JavaScript too:

```ts twoslash
// @target: ES5
// @downlevelIteration
// @importHelpers
// @showEmit
const str = "Hello!";
for (const s of str) {
  console.log(s);
}
```

**Note:** enabling `downlevelIteration` does not improve compliance if `Symbol.iterator` is not present in the runtime.

#### Example: Effects on Array Spreads

This is an array spread:

```js
// Make a new array whose elements are 1 followed by the elements of arr2
const arr = [1, ...arr2];
```

Based on the description, it sounds easy to downlevel to ES5:

```js
// The same, right?
const arr = [1].concat(arr2);
```

However, this is observably different in certain rare cases.

For example, if a source array is missing one or more items (contains a hole), the spread syntax will replace each empty item with `undefined`, whereas `.concat` will leave them intact.

```js
// Make an array where the element at index 1 is missing
let arrayWithHole = ['a', , 'c'];
let spread = [...arrayWithHole];
let concatenated = [].concat(arrayWithHole);

console.log(arrayWithHole)
// [ 'a', <1 empty item>, 'c' ]
console.log(spread)
// [ 'a', undefined, 'c' ]
console.log(concatenated)
// [ 'a', <1 empty item>, 'c' ]
```

Just as with `for / of`, `downlevelIteration` will use `Symbol.iterator` (if present) to more accurately emulate ES 6 behavior.

---
# Source: noImplicitThis.md
---
---
display: "No Implicit This"
oneline: "Enable error reporting when `this` is given the type `any`."
---

Raise error on 'this' expressions with an implied 'any' type.

For example, the class below returns a function which tries to access `this.width` and `this.height` – but the context
for `this` inside the function inside `getAreaFunction` is not the instance of the Rectangle.

```ts twoslash
// @errors: 2683
class Rectangle {
  width: number;
  height: number;

  constructor(width: number, height: number) {
    this.width = width;
    this.height = height;
  }

  getAreaFunction() {
    return function () {
      return this.width * this.height;
    };
  }
}
```

---
# Source: alwaysStrict.md
---
---
display: "Always Strict"
oneline: "Ensure 'use strict' is always emitted."
---

Ensures that your files are parsed in the ECMAScript strict mode, and emit "use strict" for each source file.

[ECMAScript strict](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Strict_mode) mode was introduced in ES5 and provides behavior tweaks to the runtime of the JavaScript engine to improve performance, and makes a set of errors throw instead of silently ignoring them.

---
# Source: typeAcquisition.md
---
---
display: "Type Acquisition"
oneline: "Specify options for automatic acquisition of declaration files."
---

When you have a JavaScript project in your editor, TypeScript will provide types for your `node_modules` automatically using the DefinitelyTyped set of `@types` definitions.
This is called automatic type acquisition, and you can customize it using the `typeAcquisition` object in your configuration.

If you would like to disable or customize this feature, create a `jsconfig.json` in the root of your project:

```json
{
  "typeAcquisition": {
    "enable": false
  }
}
```

If you have a specific module which should be included (but isn't in `node_modules`):

```json
{
  "typeAcquisition": {
    "include": ["jest"]
  }
}
```

If a module should not be automatically acquired, for example if the library is available in your `node_modules` but your team has agreed to not use it:

```json
{
  "typeAcquisition": {
    "exclude": ["jquery"]
  }
}
```

---
# Source: isolatedDeclarations.md
---
---
display: "isolatedDeclarations"
oneline: "Require sufficient annotation on exports so other tools can trivially generate declaration files." 
---
Require sufficient annotation on exports so other tools can trivially generate declaration files.
 
For more information, see the [5.5 release notes](/docs/handbook/release-notes/typescript-5-5.html#isolated-declarations)

---
# Source: erasableSyntaxOnly.md
---
---
display: "Erasable Syntax Only"
oneline: "Do not allow runtime constructs that are not part of ECMAScript."
---

Node.js [supports running TypeScript files directly](https://nodejs.org/api/typescript.html#type-stripping) as of v23.6;
however, only TypeScript-specific syntax that does not have runtime semantics are supported under this mode.
In other words, it must be possible to easily *erase* any TypeScript-specific syntax from a file, leaving behind a valid JavaScript file.

That means the following constructs are not supported:

* `enum` declarations
* `namespace`s and `module`s with runtime code
* parameter properties in classes
* Non-ECMAScript `import =` and `export =` assignments
* `<prefix>`-style type assertions

```ts
// ❌ error: An `import ... = require(...)` alias
import foo = require("foo");

// ❌ error: A namespace with runtime code.
namespace container {
    foo.method();

    export type Bar = string;
}

// ❌ error: An `import =` alias
import Bar = container.Bar;

class Point {
    // ❌ error: Parameter properties
    constructor(public x: number, public y: number) { }
}

// ❌ error: An `export =` assignment.
export = Point;

// ❌ error: An enum declaration.
enum Direction {
    Up,
    Down,
    Left,
    Right,
}

// ❌ error: <prefix>-style type assertion.
const num = <number>1;
```

Similar tools like [ts-blank-space](https://github.com/bloomberg/ts-blank-space) or [Amaro](https://github.com/nodejs/amaro) (the underlying library for type-stripping in Node.js) have the same limitations.
These tools will provide helpful error messages if they encounter code that doesn't meet these requirements, but you still won't find out your code doesn't work until you actually try to run it.

The `--erasableSyntaxOnly` flag will cause TypeScript to error on most TypeScript-specific constructs that have runtime behavior.

```ts
class C {
    constructor(public x: number) { }
    //          ~~~~~~~~~~~~~~~~
    // error! This syntax is not allowed when 'erasableSyntaxOnly' is enabled.
    }
}
```

Typically, you will want to combine this flag with the `--verbatimModuleSyntax`, which ensures that a module contains the appropriate import syntax, and that import elision does not take place.

---
# Source: disableReferencedProjectLoad.md
---
---
display: "Disable Referenced Project Load"
oneline: "Reduce the number of projects loaded automatically by TypeScript."
---

In multi-project TypeScript programs, TypeScript will load all of the available projects into memory in order to provide accurate results for editor responses which require a full knowledge graph like 'Find All References'.

If your project is large, you can use the flag `disableReferencedProjectLoad` to disable the automatic loading of all projects. Instead, projects are loaded dynamically as you open files through your editor.

---
# Source: noImplicitAny.md
---
---
display: "No Implicit Any"
oneline: "Enable error reporting for expressions and declarations with an implied `any` type."
---

In some cases where no type annotations are present, TypeScript will fall back to a type of `any` for a variable when it cannot infer the type.

This can cause some errors to be missed, for example:

```ts twoslash
// @noImplicitAny: false
function fn(s) {
  // No error?
  console.log(s.subtr(3));
}
fn(42);
```

Turning on `noImplicitAny` however TypeScript will issue an error whenever it would have inferred `any`:

```ts twoslash
// @errors: 7006
function fn(s) {
  console.log(s.subtr(3));
}
```

---
# Source: strictPropertyInitialization.md
---
---
display: "Strict Property Initialization"
oneline: "Check for class properties that are declared but not set in the constructor."
---

When set to true, TypeScript will raise an error when a class property was declared but not set in the constructor.

```ts twoslash
// @errors: 2564
class UserAccount {
  name: string;
  accountType = "user";

  email: string;
  address: string | undefined;

  constructor(name: string) {
    this.name = name;
    // Note that this.email is not set
  }
}
```

In the above case:

- `this.name` is set specifically.
- `this.accountType` is set by default.
- `this.email` is not set and raises an error.
- `this.address` is declared as potentially `undefined` which means it does not have to be set.

---
# Source: moduleSuffixes.md
---
---
display: "Module Suffixes"
oneline: "List of file name suffixes to search when resolving a module."
---

Provides a way to override the default list of file name suffixes to search when resolving a module.

```json tsconfig
{
    "compilerOptions": {
        "moduleSuffixes": [".ios", ".native", ""]
    }
}
```

Given the above configuration, an import like the following:

```ts
import * as foo from "./foo";
```

TypeScript will look for the relative files `./foo.ios.ts`, `./foo.native.ts`, and finally `./foo.ts`.

Note the empty string `""` in [`moduleSuffixes`](#moduleSuffixes) which is necessary for TypeScript to also look-up `./foo.ts`.

This feature can be useful for React Native projects where each target platform can use a separate tsconfig.json with differing `moduleSuffixes`.

---
# Source: tsBuildInfoFile.md
---
---
display: "TS Build Info File"
oneline: "The file to store `.tsbuildinfo` incremental build information in."
---

This setting lets you specify a file for storing incremental compilation information as a part of composite projects which enables faster
building of larger TypeScript codebases. You can read more about composite projects [in the handbook](/docs/handbook/project-references.html).

The default depends on a combination of other settings:

- If `outFile` is set, the default is `<outFile>.tsbuildinfo`.
- If `rootDir` and `outDir` are set, then the file is `<outDir>/<relative path to config from rootDir>/<config name>.tsbuildinfo`
  For example, if `rootDir` is `src`, `outDir` is `dest`, and the config is
  `./tsconfig.json`, then the default is `./tsconfig.tsbuildinfo`
  as the relative path from `src/` to `./tsconfig.json` is `../`.
- If `outDir` is set, then the default is `<outDir>/<config name>.tsbuildInfo`
- Otherwise, the default is `<config name>.tsbuildInfo`

---
# Source: esModuleInterop.md
---
---
display: "ES Module Interop"
oneline: "Emit additional JavaScript to ease support for importing CommonJS modules. This enables [`allowSyntheticDefaultImports`](#allowSyntheticDefaultImports) for type compatibility."
---

By default (with `esModuleInterop` false or not set) TypeScript treats CommonJS/AMD/UMD modules similar to ES6 modules. In doing this, there are two parts in particular which turned out to be flawed assumptions:

- a namespace import like `import * as moment from "moment"` acts the same as `const moment = require("moment")`

- a default import like `import moment from "moment"` acts the same as `const moment = require("moment").default`

This mis-match causes these two issues:

- the ES6 modules spec states that a namespace import (`import * as x`) can only be an object, by having TypeScript
  treating it the same as `= require("x")` then TypeScript allowed for the import to be treated as a function and be callable. That's not valid according to the spec.

- while accurate to the ES6 modules spec, most libraries with CommonJS/AMD/UMD modules didn't conform as strictly as TypeScript's implementation.

Turning on `esModuleInterop` will fix both of these problems in the code transpiled by TypeScript. The first changes the behavior in the compiler, the second is fixed by two new helper functions which provide a shim to ensure compatibility in the emitted JavaScript:

```ts
import * as fs from "fs";
import _ from "lodash";

fs.readFileSync("file.txt", "utf8");
_.chunk(["a", "b", "c", "d"], 2);
```

With `esModuleInterop` disabled:

```ts twoslash
// @noErrors
// @showEmit
// @esModuleInterop: false
// @module: commonjs
import * as fs from "fs";
import _ from "lodash";

fs.readFileSync("file.txt", "utf8");
_.chunk(["a", "b", "c", "d"], 2);
```

With `esModuleInterop` set to `true`:

```ts twoslash
// @noErrors
// @showEmit
// @esModuleInterop
// @module: commonjs
import * as fs from "fs";
import _ from "lodash";

fs.readFileSync("file.txt", "utf8");
_.chunk(["a", "b", "c", "d"], 2);
```

_Note_: The namespace import `import * as fs from "fs"` only accounts for properties which [are owned](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object/hasOwnProperty) (basically properties set on the object and not via the prototype chain) on the imported object. If the module you're importing defines its API using inherited properties, you need to use the default import form (`import fs from "fs"`), or disable `esModuleInterop`.

_Note_: You can make JS emit terser by enabling [`importHelpers`](#importHelpers):

```ts twoslash
// @noErrors
// @showEmit
// @esModuleInterop
// @importHelpers
// @module: commonjs
import * as fs from "fs";
import _ from "lodash";

fs.readFileSync("file.txt", "utf8");
_.chunk(["a", "b", "c", "d"], 2);
```

Enabling `esModuleInterop` will also enable [`allowSyntheticDefaultImports`](#allowSyntheticDefaultImports).

---
# Source: noErrorTruncation.md
---
---
display: "No Error Truncation"
oneline: "Disable truncating types in error messages."
---

Do not truncate error messages.

With `false`, the default.

```ts twoslash
// @errors: 2322 2454
var x: {
  propertyWithAnExceedinglyLongName1: string;
  propertyWithAnExceedinglyLongName2: string;
  propertyWithAnExceedinglyLongName3: string;
  propertyWithAnExceedinglyLongName4: string;
  propertyWithAnExceedinglyLongName5: string;
  propertyWithAnExceedinglyLongName6: string;
  propertyWithAnExceedinglyLongName7: string;
  propertyWithAnExceedinglyLongName8: string;
};

// String representation of type of 'x' should be truncated in error message
var s: string = x;
```

With `true`

```ts twoslash
// @errors: 2322 2454
// @noErrorTruncation: true
var x: {
  propertyWithAnExceedinglyLongName1: string;
  propertyWithAnExceedinglyLongName2: string;
  propertyWithAnExceedinglyLongName3: string;
  propertyWithAnExceedinglyLongName4: string;
  propertyWithAnExceedinglyLongName5: string;
  propertyWithAnExceedinglyLongName6: string;
  propertyWithAnExceedinglyLongName7: string;
  propertyWithAnExceedinglyLongName8: string;
};

// String representation of type of 'x' should be truncated in error message
var s: string = x;
```

---
# Source: disableSolutionSearching.md
---
---
display: "Disable Solution Searching"
oneline: "Opt a project out of multi-project reference checking when editing."
---

When working with [composite TypeScript projects](/docs/handbook/project-references.html), this option provides a way to declare that you do not want a project to be included when using features like _find all references_ or _jump to definition_ in an editor.

This flag is something you can use to increase responsiveness in large composite projects.

---
# Source: resolveJsonModule.md
---
---
display: "Resolve JSON Module"
oneline: "Enable importing .json files."
---

Allows importing modules with a `.json` extension, which is a common practice in node projects. This includes
generating a type for the `import` based on the static JSON shape.

TypeScript does not support resolving JSON files by default:

```ts twoslash
// @errors: 2732
// @filename: settings.json
{
    "repo": "TypeScript",
    "dry": false,
    "debug": false
}
// @filename: index.ts
import settings from "./settings.json";

settings.debug === true;
settings.dry === 2;
```

Enabling the option allows importing JSON, and validating the types in that JSON file.

```ts twoslash
// @errors: 2367
// @resolveJsonModule
// @module: commonjs
// @moduleResolution: node
// @filename: settings.json
{
    "repo": "TypeScript",
    "dry": false,
    "debug": false
}
// @filename: index.ts
import settings from "./settings.json";

settings.debug === true;
settings.dry === 2;
```

---
# Source: locale.md
---
---
display: "Locale"
oneline: "Set the language of the messaging from TypeScript. This does not affect emit."
---

TypeScript supports a number of languages, however this cannot be set via the `tsconfig.json`, only
via the host environment or the CLI flag `--locale`. E.g. `tsc --locale ru`.

### Locales supported as of TypeScript 3.7

| Name                  | Locale  |
| --------------------- | ------- |
| Brazilian Portuguese  | `pr-BR` |
| Chinese (Simplified)  | `zh-TW` |
| Chinese (Traditional) | `zh-CN` |
| Czech                 | `cs-CZ` |
| English (US)          | `en-US` |
| French                | `fr-FR` |
| German                | `de-DE` |
| Italian               | `it-IT` |
| Japanese              | `ja-JP` |
| Korean                | `ko-KR` |
| Polish                | `pl-PL` |
| Russian               | `ru-RU` |
| Spanish               | `es-ES` |
| Turkish               | `tr-TR` |

---
# Source: diagnostics.md
---
---
display: "Diagnostics"
oneline: "Output compiler performance information after building."
---

Used to output diagnostic information for debugging. This command is a subset of [`extendedDiagnostics`](#extendedDiagnostics) which are more user-facing results, and easier to interpret.

If you have been asked by a TypeScript compiler engineer to give the results using this flag in a compile, in which there is no harm in using [`extendedDiagnostics`](#extendedDiagnostics) instead.

