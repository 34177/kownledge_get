---
# Source: CODE_OF_CONDUCT.md
---
# Code of Conduct

## Our Pledge

In the interest of fostering an open and welcoming environment, we as
contributors and maintainers pledge to make participation in our project and
our community a harassment-free experience for everyone, regardless of age, body
size, disability, ethnicity, sex characteristics, gender identity and expression,
level of experience, education, socio-economic status, nationality, personal
appearance, race, religion, or sexual identity and orientation.

## Our Standards

Examples of behavior that contributes to creating a positive environment
include:

* Using welcoming and inclusive language
* Being respectful of differing viewpoints and experiences
* Gracefully accepting constructive criticism
* Focusing on what is best for the community
* Showing empathy towards other community members

Examples of unacceptable behavior by participants include:

* The use of sexualized language or imagery and unwelcome sexual attention or
  advances
* Trolling, insulting/derogatory comments, and personal or political attacks
* Public or private harassment
* Publishing others' private information, such as a physical or electronic
  address, without explicit permission
* Other conduct which could reasonably be considered inappropriate in a
  professional setting

## Our Responsibilities

Project maintainers are responsible for clarifying the standards of acceptable
behavior and are expected to take appropriate and fair corrective action in
response to any instances of unacceptable behavior.

Project maintainers have the right and responsibility to remove, edit, or
reject comments, commits, code, wiki edits, issues, and other contributions
that are not aligned to this Code of Conduct, or to ban temporarily or
permanently any contributor for other behaviors that they deem inappropriate,
threatening, offensive, or harmful.

## Scope

This Code of Conduct applies within all project spaces, and it also applies when
an individual is representing the project or its community in public spaces.
Examples of representing a project or community include using an official
project e-mail address, posting via an official social media account, or acting
as an appointed representative at an online or offline event. Representation of
a project may be further defined and clarified by project maintainers.

## Enforcement

Instances of abusive, harassing, or otherwise unacceptable behavior may be
reported by contacting the project team at <opensource-conduct@fb.com>. All
complaints will be reviewed and investigated and will result in a response that
is deemed necessary and appropriate to the circumstances. The project team is
obligated to maintain confidentiality with regard to the reporter of an incident.
Further details of specific enforcement policies may be posted separately.

Project maintainers who do not follow or enforce the Code of Conduct in good
faith may face temporary or permanent repercussions as determined by other
members of the project's leadership.

## Attribution

This Code of Conduct is adapted from the [Contributor Covenant][homepage], version 1.4,
available at https://www.contributor-covenant.org/version/1/4/code-of-conduct.html

[homepage]: https://www.contributor-covenant.org

For answers to common questions about this code of conduct, see
https://www.contributor-covenant.org/faq

---
# Source: CLAUDE.md
---
# CLAUDE.md

This file provides guidance to Claude Code when working with this repository.

## Project Overview

This is the React documentation website (react.dev), built with Next.js 15.1.11 and React 19. Documentation is written in MDX format.

## Development Commands

```bash
yarn build         # Production build
yarn lint          # Run ESLint
yarn lint:fix      # Auto-fix lint issues
yarn tsc           # TypeScript type checking
yarn check-all     # Run prettier, lint:fix, tsc, and rss together
```

## Project Structure

```
src/
├── content/           # Documentation content (MDX files)
│   ├── learn/         # Tutorial/learning content
│   ├── reference/     # API reference docs
│   ├── blog/          # Blog posts
│   └── community/     # Community pages
├── components/        # React components
├── pages/             # Next.js pages
├── hooks/             # Custom React hooks
├── utils/             # Utility functions
└── styles/            # CSS/Tailwind styles
```

## Code Conventions

### TypeScript/React
- Functional components only
- Tailwind CSS for styling

### Documentation Style

When editing files in `src/content/`, the appropriate skill will be auto-suggested:
- `src/content/learn/` - Learn page structure and tone
- `src/content/reference/` - Reference page structure and tone

For MDX components (DeepDive, Pitfall, Note, etc.), invoke `/docs-components`.
For Sandpack code examples, invoke `/docs-sandpack`.

See `.claude/docs/react-docs-patterns.md` for comprehensive style guidelines.

Prettier is used for formatting (config in `.prettierrc`).

---
# Source: docs-reviewer.md
---
---
name: docs-reviewer
description: "Lean docs reviewer that dispatches reviews docs for a particular skill."
model: opus
color: cyan
---

You are a direct, critical, expert reviewer for React documentation. 

Your role is to use given skills to validate given doc pages for consistency, correctness, and adherence to established patterns.

Complete this process:

## Phase 1: Task Creation
1. CRITICAL: Read the skill requested.
2. Understand the skill's requirements.
3. Create a task list to validate skills requirements.

## Phase 2: Validate

1. Read the docs files given.
2. Review each file with the task list to verify.

## Phase 3: Respond

You must respond with a checklist of the issues you identified, and line number.

DO NOT respond with passed validations, ONLY respond with the problems. 

---
# Source: SKILL.md
---
---
name: docs-writer-learn
description: Use when writing or editing files in src/content/learn/. Provides Learn page structure and tone.
---

# Learn Page Writer

## Persona

**Voice:** Patient teacher guiding a friend through concepts
**Tone:** Conversational, warm, encouraging

## Voice & Style

For tone, capitalization, jargon, and prose patterns, invoke `/docs-voice`.

## Page Structure Variants

### 1. Standard Learn Page (Most Common)

```mdx
---
title: Page Title
---

<Intro>
1-3 sentences introducing the concept. Use *italics* for new terms.
</Intro>

<YouWillLearn>

* Learning outcome 1
* Learning outcome 2
* Learning outcome 3-5

</YouWillLearn>

## Section Name {/*section-id*/}

Content with Sandpack examples, Pitfalls, Notes, DeepDives...

## Another Section {/*another-section*/}

More content...

<Recap>

* Summary point 1
* Summary point 2
* Summary points 3-9

</Recap>

<Challenges>

#### Challenge title {/*challenge-id*/}

Description...

<Hint>
Optional guidance (single paragraph)
</Hint>

<Sandpack>
{/* Starting code */}
</Sandpack>

<Solution>
Explanation...

<Sandpack>
{/* Fixed code */}
</Sandpack>
</Solution>

</Challenges>
```

### 2. Chapter Introduction Page

For pages that introduce a chapter (like describing-the-ui.md, managing-state.md):

```mdx
<YouWillLearn isChapter={true}>

* [Sub-page title](/learn/sub-page-name) to learn...
* [Another page](/learn/another-page) to learn...

</YouWillLearn>

## Preview Section {/*section-id*/}

Preview description with mini Sandpack example

<LearnMore path="/learn/sub-page-name">

Read **[Page Title](/learn/sub-page-name)** to learn how to...

</LearnMore>

## What's next? {/*whats-next*/}

Head over to [First Page](/learn/first-page) to start reading this chapter page by page!
```

**Important:** Chapter intro pages do NOT include `<Recap>` or `<Challenges>` sections.

### 3. Tutorial Page

For step-by-step tutorials (like tutorial-tic-tac-toe.md):

```mdx
<Intro>
Brief statement of what will be built
</Intro>

<Note>
Alternative learning path offered
</Note>

Table of contents (prose listing of major sections)

## Setup {/*setup*/}
...

## Main Content {/*main-content*/}
Progressive code building with ### subsections

No YouWillLearn, Recap, or Challenges

Ends with ordered list of "extra credit" improvements
```

### 4. Reference-Style Learn Page

For pages with heavy API documentation (like typescript.md):

```mdx
<YouWillLearn>

* [Link to section](#section-anchor)
* [Link to another section](#another-section)

</YouWillLearn>

## Sections with ### subsections

## Further learning {/*further-learning*/}

No Recap or Challenges
```

## Heading ID Conventions

All headings require IDs in `{/*kebab-case*/}` format:

```markdown
## Section Title {/*section-title*/}
### Subsection Title {/*subsection-title*/}
#### DeepDive Title {/*deepdive-title*/}
```

**ID Generation Rules:**
- Lowercase everything
- Replace spaces with hyphens
- Remove apostrophes, quotes
- Remove or convert special chars (`:`, `?`, `!`, `.`, parentheses)

**Examples:**
- "What's React?" → `{/*whats-react*/}`
- "Step 1: Create the context" → `{/*step-1-create-the-context*/}`
- "Conditional (ternary) operator (? :)" → `{/*conditional-ternary-operator--*/}`

## Teaching Patterns

### Problem-First Teaching

Show broken/problematic code BEFORE the solution:

1. Present problematic approach with `// 🔴 Avoid:` comment
2. Explain WHY it's wrong (don't just say it is)
3. Show the solution with `// ✅ Good:` comment
4. Invite experimentation

### Progressive Complexity

Build understanding in layers:
1. Show simplest working version
2. Identify limitation or repetition
3. Introduce solution incrementally
4. Show complete solution
5. Invite experimentation: "Try changing..."

### Numbered Step Patterns

For multi-step processes:

**As section headings:**
```markdown
### Step 1: Action to take {/*step-1-action*/}
### Step 2: Next action {/*step-2-next-action*/}
```

**As inline lists:**
```markdown
To implement this:
1. **Declare** `inputRef` with the `useRef` Hook.
2. **Pass it** as `<input ref={inputRef}>`.
3. **Read** the input DOM node from `inputRef.current`.
```

### Interactive Invitations

After Sandpack examples, encourage experimentation:
- "Try changing X to Y. See how...?"
- "Try it in the sandbox above!"
- "Click each button separately:"
- "Have a guess!"
- "Verify that..."

### Decision Questions

Help readers build intuition:
> "When you're not sure whether some code should be in an Effect or in an event handler, ask yourself *why* this code needs to run."

## Component Placement Order

1. `<Intro>` - First after frontmatter
2. `<YouWillLearn>` - After Intro (standard/chapter pages)
3. Body content with `<Note>`, `<Pitfall>`, `<DeepDive>` placed contextually
4. `<Recap>` - Before Challenges (standard pages only)
5. `<Challenges>` - End of page (standard pages only)

For component structure and syntax, invoke `/docs-components`.

## Code Examples

For Sandpack file structure, naming conventions, code style, and pedagogical markers, invoke `/docs-sandpack`.

## Cross-Referencing

### When to Link

**Link to /learn:**
- Explaining concepts or mental models
- Teaching how things work together
- Tutorials and guides
- "Why" questions

**Link to /reference:**
- API details, Hook signatures
- Parameter lists and return values
- Rules and restrictions
- "What exactly" questions

### Link Formats

```markdown
[concept name](/learn/page-name)
[`useState`](/reference/react/useState)
[section link](/learn/page-name#section-id)
[MDN](https://developer.mozilla.org/...)
```

## Section Dividers

**Important:** Learn pages typically do NOT use `---` dividers. The heading hierarchy provides sufficient structure. Only consider dividers in exceptional cases like separating main content from meta/contribution sections.

## Do's and Don'ts

**Do:**
- Use "you" to address the reader
- Show broken code before fixes
- Explain behavior before naming concepts
- Build concepts progressively
- Include interactive Sandpack examples
- Use established analogies consistently
- Place Pitfalls AFTER explaining concepts
- Invite experimentation with "Try..." phrases

**Don't:**
- Use "simple", "easy", "just", or time estimates
- Reference concepts not yet introduced
- Skip required components for page type
- Use passive voice without reason
- Place Pitfalls before teaching the concept
- Use `---` dividers between sections
- Create unnecessary abstraction in examples
- Place consecutive Pitfalls or Notes without separating prose (combine or separate)

## Critical Rules

1. **All headings require IDs:** `## Title {/*title-id*/}`
2. **Chapter intros use `isChapter={true}` and `<LearnMore>`**
3. **Tutorial pages omit YouWillLearn/Recap/Challenges**
4. **Problem-first teaching:** Show broken → explain → fix
5. **No consecutive Pitfalls/Notes:** See `/docs-components` Callout Spacing Rules

For component patterns, invoke `/docs-components`. For Sandpack patterns, invoke `/docs-sandpack`.

---
# Source: SKILL.md
---
---
name: docs-writer-reference
description: Reference page structure, templates, and writing patterns for src/content/reference/. For components, see /docs-components. For code examples, see /docs-sandpack.
---

# Reference Page Writer

## Quick Reference

### Page Type Decision Tree

1. Is it a Hook? Use **Type A (Hook/Function)**
2. Is it a React component (`<Something>`)? Use **Type B (Component)**
3. Is it a compiler configuration option? Use **Type C (Configuration)**
4. Is it a directive (`'use something'`)? Use **Type D (Directive)**
5. Is it an ESLint rule? Use **Type E (ESLint Rule)**
6. Is it listing multiple APIs? Use **Type F (Index/Category)**

### Component Selection

For component selection and patterns, invoke `/docs-components`.

---

## Voice & Style

**Voice:** Authoritative technical reference writer
**Tone:** Precise, comprehensive, neutral

For tone, capitalization, jargon, and prose patterns, invoke `/docs-voice`.

**Do:**
- Start with single-line description: "`useState` is a React Hook that lets you..."
- Include Parameters, Returns, Caveats sections for every API
- Document edge cases most developers will encounter
- Use section dividers between major sections
- Include "See more examples below" links
- Be assertive, not hedging - "This is designed for..." not "This helps avoid issues with..."
- State facts, not benefits - "The callback always accesses the latest values" not "This helps avoid stale closures"
- Use minimal but meaningful names - `onEvent` or `onTick` over `onSomething`

**Don't:**
- Skip the InlineToc component
- Omit error cases or caveats
- Use conversational language
- Mix teaching with reference (that's Learn's job)
- Document past bugs or fixed issues
- Include niche edge cases (e.g., `this` binding, rare class patterns)
- Add phrases explaining "why you'd want this" - the Usage section examples do that
- Exception: Pitfall and DeepDive asides can use slightly conversational phrasing

---

## Page Templates

### Type A: Hook/Function

**When to use:** Documenting React hooks and standalone functions (useState, useEffect, memo, lazy, etc.)

```mdx
---
title: hookName
---

<Intro>

`hookName` is a React Hook that lets you [brief description].

```js
const result = hookName(arg)
```

</Intro>

<InlineToc />

---

## Reference {/*reference*/}

### `hookName(arg)` {/*hookname*/}

Call `hookName` at the top level of your component to...

```js
[signature example with annotations]
```

[See more examples below.](#usage)

#### Parameters {/*parameters*/}
* `arg`: Description of the parameter.

#### Returns {/*returns*/}
Description of return value.

#### Caveats {/*caveats*/}
* Important caveat about usage.

---

## Usage {/*usage*/}

### Common Use Case {/*common-use-case*/}
Explanation with Sandpack examples...

---

## Troubleshooting {/*troubleshooting*/}

### Common Problem {/*common-problem*/}
How to solve it...
```

---

### Type B: Component

**When to use:** Documenting React components (Suspense, Fragment, Activity, StrictMode)

```mdx
---
title: <ComponentName>
---

<Intro>

`<ComponentName>` lets you [primary action].

```js
<ComponentName prop={value}>
  <Children />
</ComponentName>
```

</Intro>

<InlineToc />

---

## Reference {/*reference*/}

### `<ComponentName>` {/*componentname*/}

[Component purpose and behavior]

#### Props {/*props*/}

* `propName`: Description of the prop...
* **optional** `optionalProp`: Description...

#### Caveats {/*caveats*/}

* [Caveats specific to this component]
```

**Key differences from Hook pages:**
- Title uses JSX syntax: `<ComponentName>`
- Uses `#### Props` instead of `#### Parameters`
- Reference heading uses JSX: `` ### `<ComponentName>` ``

---

### Type C: Configuration

**When to use:** Documenting React Compiler configuration options

```mdx
---
title: optionName
---

<Intro>

The `optionName` option [controls/specifies/determines] [what it does].

</Intro>

```js
{
  optionName: 'value' // Quick example
}
```

<InlineToc />

---

## Reference {/*reference*/}

### `optionName` {/*optionname*/}

[Description of the option's purpose]

#### Type {/*type*/}

```
'value1' | 'value2' | 'value3'
```

#### Default value {/*default-value*/}

`'value1'`

#### Options {/*options*/}

- **`'value1'`** (default): Description
- **`'value2'`**: Description
- **`'value3'`**: Description

#### Caveats {/*caveats*/}

* [Usage caveats]
```

---

### Type D: Directive

**When to use:** Documenting directives like 'use server', 'use client', 'use memo'

```mdx
---
title: "'use directive'"
titleForTitleTag: "'use directive' directive"
---

<RSC>

`'use directive'` is for use with [React Server Components](/reference/rsc/server-components).

</RSC>

<Intro>

`'use directive'` marks [what it marks] for [purpose].

```js {1}
function MyComponent() {
  'use directive';
  // ...
}
```

</Intro>

<InlineToc />

---

## Reference {/*reference*/}

### `'use directive'` {/*use-directive*/}

Add `'use directive'` at the beginning of [location] to [action].

#### Caveats {/*caveats*/}

* `'use directive'` must be at the very beginning...
* The directive must be written with single or double quotes, not backticks.
* [Other placement/syntax caveats]
```

**Key characteristics:**
- Title includes quotes: `title: "'use server'"`
- Uses `titleForTitleTag` for browser tab title
- `<RSC>` block appears before `<Intro>`
- Caveats focus on placement and syntax requirements

---

### Type E: ESLint Rule

**When to use:** Documenting ESLint plugin rules

```mdx
---
title: rule-name
---

<Intro>
Validates that [what the rule checks].
</Intro>

## Rule Details {/*rule-details*/}

[Explanation of why this rule exists and React's underlying assumptions]

## Common Violations {/*common-violations*/}

[Description of violation patterns]

### Invalid {/*invalid*/}

Examples of incorrect code for this rule:

```js
// X Missing dependency
useEffect(() => {
  console.log(count);
}, []); // Missing 'count'
```

### Valid {/*valid*/}

Examples of correct code for this rule:

```js
// checkmark All dependencies included
useEffect(() => {
  console.log(count);
}, [count]);
```

## Troubleshooting {/*troubleshooting*/}

### [Problem description] {/*problem-slug*/}

[Solution]

## Options {/*options*/}

[Configuration options if applicable]
```

**Key characteristics:**
- Intro is a single "Validates that..." sentence
- Uses "Invalid"/"Valid" sections with emoji-prefixed code comments
- Rule Details explains "why" not just "what"

---

### Type F: Index/Category

**When to use:** Overview pages listing multiple APIs in a category

```mdx
---
title: "Built-in React [Type]"
---

<Intro>

*Concept* let you [purpose]. Brief scope statement.

</Intro>

---

## Category Name {/*category-name*/}

*Concept* explanation with [Learn section link](/learn/topic).

To [action], use one of these [Type]:

* [`apiName`](/reference/react/apiName) lets you [action].
* [`apiName`](/reference/react/apiName) declares [thing].

```js
function Example() {
  const value = useHookName(args);
}
```

---

## Your own [Type] {/*your-own-type*/}

You can also [define your own](/learn/topic) as JavaScript functions.
```

**Key characteristics:**
- Title format: "Built-in React [Type]"
- Italicized concept definitions
- Horizontal rules between sections
- Closes with "Your own [Type]" section

---

## Advanced Patterns

### Multi-Function Documentation

**When to use:** When a hook returns a function that needs its own documentation (useState's setter, useReducer's dispatch)

```md
### `hookName(args)` {/*hookname*/}

[Main hook documentation]

#### Parameters {/*parameters*/}
#### Returns {/*returns*/}
#### Caveats {/*caveats*/}

---

### `set` functions, like `setSomething(nextState)` {/*setstate*/}

The `set` function returned by `hookName` lets you [action].

#### Parameters {/*setstate-parameters*/}
#### Returns {/*setstate-returns*/}
#### Caveats {/*setstate-caveats*/}
```

**Key conventions:**
- Horizontal rule (`---`) separates main hook from returned function
- Heading IDs include prefix: `{/*setstate-parameters*/}` vs `{/*parameters*/}`
- Use generic names: "set functions" not "setCount"

---

### Compound Return Objects

**When to use:** When a function returns an object with multiple properties/methods (createContext)

```md
### `createContext(defaultValue)` {/*createcontext*/}

[Main function documentation]

#### Returns {/*returns*/}

`createContext` returns a context object.

**The context object itself does not hold any information.** It represents...

* `SomeContext` lets you provide the context value.
* `SomeContext.Consumer` is an alternative way to read context.

---

### `SomeContext` Provider {/*provider*/}

[Documentation for Provider]

#### Props {/*provider-props*/}

---

### `SomeContext.Consumer` {/*consumer*/}

[Documentation for Consumer]

#### Props {/*consumer-props*/}
```

---

## Writing Patterns

### Opening Lines by Page Type

| Page Type | Pattern | Example |
|-----------|---------|---------|
| Hook | `` `hookName` is a React Hook that lets you [action]. `` | "`useState` is a React Hook that lets you add a state variable to your component." |
| Component | `` `<ComponentName>` lets you [action]. `` | "`<Suspense>` lets you display a fallback until its children have finished loading." |
| API | `` `apiName` lets you [action]. `` | "`memo` lets you skip re-rendering a component when its props are unchanged." |
| Configuration | `` The `optionName` option [controls/specifies/determines] [what]. `` | "The `target` option specifies which React version the compiler generates code for." |
| Directive | `` `'directive'` [marks/opts/prevents] [what] for [purpose]. `` | "`'use server'` marks a function as callable from the client." |
| ESLint Rule | `` Validates that [condition]. `` | "Validates that dependency arrays for React hooks contain all necessary dependencies." |

---

### Parameter Patterns

**Simple parameter:**
```md
* `paramName`: Description of what it does.
```

**Optional parameter:**
```md
* **optional** `paramName`: Description of what it does.
```

**Parameter with special function behavior:**
```md
* `initialState`: The value you want the state to be initially. It can be a value of any type, but there is a special behavior for functions. This argument is ignored after the initial render.
  * If you pass a function as `initialState`, it will be treated as an _initializer function_. It should be pure, should take no arguments, and should return a value of any type.
```

**Callback parameter with sub-parameters:**
```md
* `subscribe`: A function that takes a single `callback` argument and subscribes it to the store. When the store changes, it should invoke the provided `callback`. The `subscribe` function should return a function that cleans up the subscription.
```

**Nested options object:**
```md
* **optional** `options`: An object with options for this React root.
  * **optional** `onCaughtError`: Callback called when React catches an error in an Error Boundary.
  * **optional** `onUncaughtError`: Callback called when an error is thrown and not caught.
  * **optional** `identifierPrefix`: A string prefix React uses for IDs generated by `useId`.
```

---

### Return Value Patterns

**Single value return:**
```md
`hookName` returns the current value. The value will be the same as `initialValue` during the first render.
```

**Array return (numbered list):**
```md
`useState` returns an array with exactly two values:

1. The current state. During the first render, it will match the `initialState` you have passed.
2. The [`set` function](#setstate) that lets you update the state to a different value and trigger a re-render.
```

**Object return (bulleted list):**
```md
`createElement` returns a React element object with a few properties:

* `type`: The `type` you have passed.
* `props`: The `props` you have passed except for `ref` and `key`.
* `ref`: The `ref` you have passed. If missing, `null`.
* `key`: The `key` you have passed, coerced to a string. If missing, `null`.
```

**Promise return:**
```md
`prerender` returns a Promise:
- If rendering is successful, the Promise will resolve to an object containing:
  - `prelude`: a [Web Stream](MDN-link) of HTML.
  - `postponed`: a JSON-serializable object for resumption.
- If rendering fails, the Promise will be rejected.
```

**Wrapped function return:**
```md
`cache` returns a cached version of `fn` with the same type signature. It does not call `fn` in the process.

When calling `cachedFn` with given arguments, it first checks if a cached result exists. If cached, it returns the result. If not, it calls `fn`, stores the result, and returns it.
```

---

### Caveats Patterns

**Standard Hook caveat (almost always first for Hooks):**
```md
* `useXxx` is a Hook, so you can only call it **at the top level of your component** or your own Hooks. You can't call it inside loops or conditions. If you need that, extract a new component and move the state into it.
```

**Stable identity caveat (for returned functions):**
```md
* The `set` function has a stable identity, so you will often see it omitted from Effect dependencies, but including it will not cause the Effect to fire.
```

**Strict Mode caveat:**
```md
* In Strict Mode, React will **call your render function twice** in order to help you find accidental impurities. This is development-only behavior and does not affect production.
```

**Caveat with code example:**
```md
* It's not recommended to _suspend_ a render based on a store value returned by `useSyncExternalStore`. For example, the following is discouraged:

  ```js
  const selectedProductId = useSyncExternalStore(...);
  const data = use(fetchItem(selectedProductId)) // X Don't suspend based on store value
  ```
```

**Canary caveat:**
```md
* <CanaryBadge /> If you want to pass `ref` to a Fragment, you can't use the `<>...</>` syntax.
```

---

### Troubleshooting Patterns

**Heading format (first person problem statements):**
```md
### I've updated the state, but logging gives me the old value {/*old-value*/}

### My initializer or updater function runs twice {/*runs-twice*/}

### I want to read the latest state from a callback {/*read-latest-state*/}
```

**Error message format:**
```md
### I'm getting an error: "Too many re-renders" {/*too-many-rerenders*/}

### I'm getting an error: "Rendered more hooks than during the previous render" {/*more-hooks*/}
```

**Lint error format:**
```md
### I'm getting a lint error: "[exact error message]" {/*lint-error-slug*/}
```

**Problem-solution structure:**
1. State the problem with code showing the issue
2. Explain why it happens
3. Provide the solution with corrected code
4. Link to Learn section for deeper understanding

---

### Code Comment Conventions

For code comment conventions (wrong/right, legacy/recommended, server/client labeling, bundle size annotations), invoke `/docs-sandpack`.

---

### Link Description Patterns

| Pattern | Example |
|---------|---------|
| "lets you" + action | "`memo` lets you skip re-rendering when props are unchanged." |
| "declares" + thing | "`useState` declares a state variable that you can update directly." |
| "reads" + thing | "`useContext` reads and subscribes to a context." |
| "connects" + thing | "`useEffect` connects a component to an external system." |
| "Used with" | "Used with [`useContext`.](/reference/react/useContext)" |
| "Similar to" | "Similar to [`useTransition`.](/reference/react/useTransition)" |

---

## Component Patterns

For comprehensive MDX component patterns (Note, Pitfall, DeepDive, Recipes, Deprecated, RSC, Canary, Diagram, Code Steps), invoke `/docs-components`.

For Sandpack-specific patterns and code style, invoke `/docs-sandpack`.

### Reference-Specific Component Rules

**Component placement in Reference pages:**
- `<RSC>` goes before `<Intro>` at top of page
- `<Deprecated>` goes after `<Intro>` for page-level deprecation
- `<Deprecated>` goes after method heading for method-level deprecation
- `<Canary>` wrapper goes inline within `<Intro>`
- `<CanaryBadge />` appears in headings, props lists, and caveats

**Troubleshooting-specific components:**
- Use first-person problem headings
- Cross-reference Pitfall IDs when relevant

**Callout spacing:**
- Never place consecutive Pitfalls or consecutive Notes
- Combine related warnings into one with titled subsections, or separate with prose/code
- Consecutive DeepDives OK for multi-part explorations
- See `/docs-components` Callout Spacing Rules

---

## Content Principles

### Intro Section
- **One sentence, ~15 words max** - State what the Hook does, not how it works
- ✅ "`useEffectEvent` is a React Hook that lets you separate events from Effects."
- ❌ "`useEffectEvent` is a React Hook that lets you extract non-reactive logic from your Effects into a reusable function called an Effect Event."

### Reference Code Example
- Show just the API call (5-10 lines), not a full component
- Move full component examples to Usage section

### Usage Section Structure
1. **First example: Core mental model** - Show the canonical use case with simplest concrete example
2. **Subsequent examples: Canonical use cases** - Name the *why* (e.g., "Avoid reconnecting to external systems"), show a concrete *how*
   - Prefer broad canonical use cases over multiple narrow concrete examples
   - The section title IS the teaching - "When would I use this?" should be answered by the heading

### What to Include vs. Exclude
- **Never** document past bugs or fixed issues
- **Include** edge cases most developers will encounter
- **Exclude** niche edge cases (e.g., `this` binding, rare class patterns)

### Caveats Section
- Include rules the linter enforces or that cause immediate errors
- Include fundamental usage restrictions
- Exclude implementation details unless they affect usage
- Exclude repetition of things explained elsewhere
- Keep each caveat to one sentence when possible

### Troubleshooting Section
- Error headings only: "I'm getting an error: '[message]'" format
- Never document past bugs - if it's fixed, it doesn't belong here
- Focus on errors developers will actually encounter today

### DeepDive Content
- **Goldilocks principle** - Deep enough for curious developers, short enough to not overwhelm
- Answer "why is it designed this way?" - not exhaustive technical details
- Readers who skip it should miss nothing essential for using the API
- If the explanation is getting long, you're probably explaining too much

---

## Domain-Specific Guidance

### Hooks

**Returned function documentation:**
- Document setter/dispatch functions as separate `###` sections
- Use generic names: "set functions" not "setCount"
- Include stable identity caveat for returned functions

**Dependency array documentation:**
- List what counts as reactive values
- Explain when dependencies are ignored
- Link to removing effect dependencies guide

**Recipes usage:**
- Group related examples with meaningful titleText
- Each recipe has brief intro, Sandpack, and `<Solution />`

---

### Components

**Props documentation:**
- Use `#### Props` instead of `#### Parameters`
- Mark optional props with `**optional**` prefix
- Use `<CanaryBadge />` inline for canary-only props

**JSX syntax in titles/headings:**
- Frontmatter title: `title: <Suspense>`
- Reference heading: `` ### `<Suspense>` {/*suspense*/} ``

---

### React-DOM

**Common props linking:**
```md
`<input>` supports all [common element props.](/reference/react-dom/components/common#common-props)
```

**Props categorization:**
- Controlled vs uncontrolled props grouped separately
- Form-specific props documented with action patterns
- MDN links for standard HTML attributes

**Environment-specific notes:**
```mdx
<Note>

This API is specific to Node.js. Environments with [Web Streams](MDN-link), like Deno and modern edge runtimes, should use [`renderToReadableStream`](/reference/react-dom/server/renderToReadableStream) instead.

</Note>
```

**Progressive enhancement:**
- Document benefits for users without JavaScript
- Explain Server Function + form action integration
- Show hidden form field and `.bind()` patterns

---

### RSC

**RSC banner (before Intro):**
Always place `<RSC>` component before `<Intro>` for Server Component-only APIs.

**Serialization type lists:**
When documenting Server Function arguments, list supported types:
```md
Supported types for Server Function arguments:

* Primitives
	* [string](MDN-link)
	* [number](MDN-link)
* Iterables containing serializable values
	* [Array](MDN-link)
	* [Map](MDN-link)

Notably, these are not supported:
* React elements, or [JSX](/learn/writing-markup-with-jsx)
* Functions (other than Server Functions)
```

**Bundle size comparisons:**
- Show "Not included in bundle" for server-only imports
- Annotate client bundle sizes with gzip: `// 35.9K (11.2K gzipped)`

---

### Compiler

**Configuration page structure:**
- Type (union type or interface)
- Default value
- Options/Valid values with descriptions

**Directive documentation:**
- Placement requirements are critical
- Mode interaction tables showing combinations
- "Use sparingly" + "Plan for removal" patterns for escape hatches

**Library author guides:**
- Audience-first intro
- Benefits/Why section
- Numbered step-by-step setup

---

### ESLint

**Rule Details section:**
- Explain "why" not just "what"
- Focus on React's underlying assumptions
- Describe consequences of violations

**Invalid/Valid sections:**
- Standard intro: "Examples of [in]correct code for this rule:"
- Use X emoji for invalid, checkmark for valid
- Show inline comments explaining the violation

**Configuration options:**
- Show shared settings (preferred)
- Show rule-level options (backward compatibility)
- Note precedence when both exist

---

## Edge Cases

For deprecated, canary, and version-specific component patterns (placement, syntax, examples), invoke `/docs-components`.

**Quick placement rules:**
- `<Deprecated>` after `<Intro>` for page-level, after heading for method-level
- `<Canary>` wrapper inline in Intro, `<CanaryBadge />` in headings/props/caveats
- Version notes use `<Note>` with "Starting in React 19..." pattern

**Removed APIs on index pages:**
```md
## Removed APIs {/*removed-apis*/}

These APIs were removed in React 19:

* [`render`](https://18.react.dev/reference/react-dom/render): use [`createRoot`](/reference/react-dom/client/createRoot) instead.
```

Link to previous version docs (18.react.dev) for removed API documentation.

---

## Critical Rules

1. **Heading IDs required:** `## Title {/*title-id*/}` (lowercase, hyphens)
2. **Sandpack main file needs `export default`**
3. **Active file syntax:** ` ```js src/File.js active `
4. **Error headings in Troubleshooting:** Use `### I'm getting an error: "[message]" {/*id*/}`
5. **Section dividers (`---`)** required between headings (see Section Dividers below)
6. **InlineToc required:** Always include `<InlineToc />` after Intro
7. **Consistent parameter format:** Use `* \`paramName\`: description` with `**optional**` prefix for optional params
8. **Numbered lists for array returns:** When hooks return arrays, use numbered lists in Returns section
9. **Generic names for returned functions:** Use "set functions" not "setCount"
10. **Props vs Parameters:** Use `#### Props` for Components (Type B), `#### Parameters` for Hooks/APIs (Type A)
11. **RSC placement:** `<RSC>` component goes before `<Intro>`, not after
12. **Canary markers:** Use `<Canary>` wrapper inline in Intro, `<CanaryBadge />` in headings/props
13. **Deprecated placement:** `<Deprecated>` goes after `<Intro>` for page-level, after heading for method-level
14. **Code comment emojis:** Use X for wrong, checkmark for correct in code examples
15. **No consecutive Pitfalls/Notes:** Combine into one component with titled subsections, or separate with prose/code (see `/docs-components`)

For component heading level conventions (DeepDive, Pitfall, Note, Recipe headings), see `/docs-components`.

### Section Dividers

Use `---` horizontal rules to visually separate major sections:

- **After `<InlineToc />`** - Before `## Reference` heading
- **Between API subsections** - Between different function/hook definitions (e.g., between `useState()` and `set functions`)
- **Before `## Usage`** - Separates API reference from examples
- **Before `## Troubleshooting`** - Separates content from troubleshooting
- **Between EVERY Usage subsections** - When switching to a new major use case

Always have a blank line before and after `---`.

### Section ID Conventions

| Section | ID Format |
|---------|-----------|
| Main function | `{/*functionname*/}` |
| Returned function | `{/*setstate*/}`, `{/*dispatch*/}` |
| Sub-section of returned function | `{/*setstate-parameters*/}` |
| Troubleshooting item | `{/*problem-description-slug*/}` |
| Pitfall | `{/*pitfall-description*/}` |
| Deep dive | `{/*deep-dive-topic*/}` |

---
# Source: SKILL.md
---
---
name: review-docs
description: Use when reviewing React documentation for structure, components, and style compliance
---
CRITICAL: do not load these skills yourself.

Run these tasks in parallel for the given file(s). Each agent checks different aspects—not all apply to every file:

- [ ] Ask docs-reviewer agent to review {files} with docs-writer-learn (only for files in src/content/learn/).
- [ ] Ask docs-reviewer agent to review {files} with docs-writer-reference (only for files in src/content/reference/).
- [ ] Ask docs-reviewer agent to review {files} with docs-writer-blog (only for files in src/content/blog/).
- [ ] Ask docs-reviewer agent to review {files} with docs-voice (all documentation files).
- [ ] Ask docs-reviewer agent to review {files} with docs-components (all documentation files).
- [ ] Ask docs-reviewer agent to review {files} with docs-sandpack (files containing Sandpack examples).

If no file is specified, check git status for modified MDX files in `src/content/`.

The docs-reviewer will return a checklist of the issues it found. Respond with the full checklist and line numbers from all agents, and prompt the user to create a plan to fix these issues.



---
# Source: SKILL.md
---
---
name: react-expert
description: Use when researching React APIs or concepts for documentation. Use when you need authoritative usage examples, caveats, warnings, or errors for a React feature.
---

# React Expert Research Skill

## Overview

This skill produces exhaustive documentation research on any React API or concept by searching authoritative sources (tests, source code, PRs, issues) rather than relying on LLM training knowledge.

<CRITICAL>
**Skepticism Mandate:** You must be skeptical of your own knowledge. Claude is often trained on outdated or incorrect React patterns. Treat source material as the sole authority. If findings contradict your prior understanding, explicitly flag this discrepancy.

**Red Flags - STOP if you catch yourself thinking:**
- "I know this API does X" → Find source evidence first
- "Common pattern is Y" → Verify in test files
- Generating example code → Must have source file reference
</CRITICAL>

## Invocation

```
/react-expert useTransition
/react-expert suspense boundaries
/react-expert startTransition
```

## Sources (Priority Order)

1. **React Repo Tests** - Most authoritative for actual behavior
2. **React Source Code** - Warnings, errors, implementation details
3. **Git History** - Commit messages with context
4. **GitHub PRs & Comments** - Design rationale (via `gh` CLI)
5. **GitHub Issues** - Confusion/questions (facebook/react + reactjs/react.dev)
6. **React Working Group** - Design discussions for newer APIs
7. **Flow Types** - Source of truth for type signatures
8. **TypeScript Types** - Note discrepancies with Flow
9. **Current react.dev docs** - Baseline (not trusted as complete)

**No web search** - No Stack Overflow, blog posts, or web searches. GitHub API via `gh` CLI is allowed.

## Workflow

### Step 1: Setup React Repo

First, ensure the React repo is available locally:

```bash
# Check if React repo exists, clone or update
if [ -d ".claude/react" ]; then
  cd .claude/react && git pull origin main
else
  git clone --depth=100 https://github.com/facebook/react.git .claude/react
fi
```

Get the current commit hash for the research document:
```bash
cd .claude/react && git rev-parse --short HEAD
```

### Step 2: Dispatch 6 Parallel Research Agents

Spawn these agents IN PARALLEL using the Task tool. Each agent receives the skepticism preamble:

> "You are researching React's `<TOPIC>`. CRITICAL: Do NOT rely on your prior knowledge about this API. Your training may contain outdated or incorrect patterns. Only report what you find in the source files. If your findings contradict common understanding, explicitly highlight this discrepancy."

| Agent | subagent_type | Focus | Instructions |
|-------|---------------|-------|--------------|
| test-explorer | Explore | Test files for usage patterns | Search `.claude/react/packages/*/src/__tests__/` for test files mentioning the topic. Extract actual usage examples WITH file paths and line numbers. |
| source-explorer | Explore | Warnings/errors in source | Search `.claude/react/packages/*/src/` for console.error, console.warn, and error messages mentioning the topic. Document trigger conditions. |
| git-historian | Explore | Commit messages | Run `git log --all --grep="<topic>" --oneline -50` in `.claude/react`. Read full commit messages for context. |
| pr-researcher | Explore | PRs introducing/modifying API | Run `gh pr list -R facebook/react --search "<topic>" --state all --limit 20`. Read key PR descriptions and comments. |
| issue-hunter | Explore | Issues showing confusion | Search issues in both `facebook/react` and `reactjs/react.dev` repos. Look for common questions and misunderstandings. |
| types-inspector | Explore | Flow + TypeScript signatures | Find Flow types in `.claude/react/packages/*/src/*.js` (look for `@flow` annotations). Find TS types in `.claude/react/packages/*/index.d.ts`. Note discrepancies. |

### Step 3: Agent Prompts

Use these exact prompts when spawning agents:

#### test-explorer
```
You are researching React's <TOPIC>.

CRITICAL: Do NOT rely on your prior knowledge about this API. Your training may contain outdated or incorrect patterns. Only report what you find in the source files.

Your task: Find test files in .claude/react that demonstrate <TOPIC> usage.

1. Search for test files: Glob for `**/__tests__/**/*<topic>*` and `**/__tests__/**/*.js` then grep for <topic>
2. For each relevant test file, extract:
   - The test description (describe/it blocks)
   - The actual usage code
   - Any assertions about behavior
   - Edge cases being tested
3. Report findings with exact file paths and line numbers

Format your output as:
## Test File: <path>
### Test: "<test description>"
```javascript
<exact code from test>
```
**Behavior:** <what the test asserts>
```

#### source-explorer
```
You are researching React's <TOPIC>.

CRITICAL: Do NOT rely on your prior knowledge about this API. Only report what you find in the source files.

Your task: Find warnings, errors, and implementation details for <TOPIC>.

1. Search .claude/react/packages/*/src/ for:
   - console.error mentions of <topic>
   - console.warn mentions of <topic>
   - Error messages mentioning <topic>
   - The main implementation file
2. For each warning/error, document:
   - The exact message text
   - The condition that triggers it
   - The source file and line number

Format your output as:
## Warnings & Errors
| Message | Trigger Condition | Source |
|---------|------------------|--------|
| "<exact message>" | <condition> | <file:line> |

## Implementation Notes
<key details from source code>
```

#### git-historian
```
You are researching React's <TOPIC>.

CRITICAL: Do NOT rely on your prior knowledge. Only report what you find in git history.

Your task: Find commit messages that explain <TOPIC> design decisions.

1. Run: cd .claude/react && git log --all --grep="<topic>" --oneline -50
2. For significant commits, read full message: git show <hash> --stat
3. Look for:
   - Initial introduction of the API
   - Bug fixes (reveal edge cases)
   - Behavior changes
   - Deprecation notices

Format your output as:
## Key Commits
### <short hash> - <subject>
**Date:** <date>
**Context:** <why this change was made>
**Impact:** <what behavior changed>
```

#### pr-researcher
```
You are researching React's <TOPIC>.

CRITICAL: Do NOT rely on your prior knowledge. Only report what you find in PRs.

Your task: Find PRs that introduced or modified <TOPIC>.

1. Run: gh pr list -R facebook/react --search "<topic>" --state all --limit 20 --json number,title,url
2. For promising PRs, read details: gh pr view <number> -R facebook/react
3. Look for:
   - The original RFC/motivation
   - Design discussions in comments
   - Alternative approaches considered
   - Breaking changes

Format your output as:
## Key PRs
### PR #<number>: <title>
**URL:** <url>
**Summary:** <what it introduced/changed>
**Design Rationale:** <why this approach>
**Discussion Highlights:** <key points from comments>
```

#### issue-hunter
```
You are researching React's <TOPIC>.

CRITICAL: Do NOT rely on your prior knowledge. Only report what you find in issues.

Your task: Find issues that reveal common confusion about <TOPIC>.

1. Search facebook/react: gh issue list -R facebook/react --search "<topic>" --state all --limit 20 --json number,title,url
2. Search reactjs/react.dev: gh issue list -R reactjs/react.dev --search "<topic>" --state all --limit 20 --json number,title,url
3. For each issue, identify:
   - What the user was confused about
   - What the resolution was
   - Any gotchas revealed

Format your output as:
## Common Confusion
### Issue #<number>: <title>
**Repo:** <facebook/react or reactjs/react.dev>
**Confusion:** <what they misunderstood>
**Resolution:** <correct understanding>
**Gotcha:** <if applicable>
```

#### types-inspector
```
You are researching React's <TOPIC>.

CRITICAL: Do NOT rely on your prior knowledge. Only report what you find in type definitions.

Your task: Find and compare Flow and TypeScript type signatures for <TOPIC>.

1. Flow types (source of truth): Search .claude/react/packages/*/src/*.js for @flow annotations related to <topic>
2. TypeScript types: Search .claude/react/packages/*/index.d.ts and @types/react
3. Compare and note any discrepancies

Format your output as:
## Flow Types (Source of Truth)
**File:** <path>
```flow
<exact type definition>
```

## TypeScript Types
**File:** <path>
```typescript
<exact type definition>
```

## Discrepancies
<any differences between Flow and TS definitions>
```

### Step 4: Synthesize Results

After all agents complete, combine their findings into a single research document.

**DO NOT add information from your own knowledge.** Only include what agents found in sources.

### Step 5: Save Output

Write the final document to `.claude/research/<topic>.md`

Replace spaces in topic with hyphens (e.g., "suspense boundaries" → "suspense-boundaries.md")

## Output Document Template

```markdown
# React Research: <topic>

> Generated by /react-expert on YYYY-MM-DD
> Sources: React repo (commit <hash>), N PRs, M issues

## Summary

[Brief summary based SOLELY on source findings, not prior knowledge]

## API Signature

### Flow Types (Source of Truth)

[From types-inspector agent]

### TypeScript Types

[From types-inspector agent]

### Discrepancies

[Any differences between Flow and TS]

## Usage Examples

### From Tests

[From test-explorer agent - with file:line references]

### From PRs/Issues

[Real-world patterns from discussions]

## Caveats & Gotchas

[Each with source link]

- **<gotcha>** - Source: <link>

## Warnings & Errors

| Message | Trigger Condition | Source File |
|---------|------------------|-------------|
[From source-explorer agent]

## Common Confusion

[From issue-hunter agent]

## Design Decisions

[From git-historian and pr-researcher agents]

## Source Links

### Commits
- <hash>: <description>

### Pull Requests
- PR #<number>: <title> - <url>

### Issues
- Issue #<number>: <title> - <url>
```

## Common Mistakes to Avoid

1. **Trusting prior knowledge** - If you "know" something about the API, find the source evidence anyway
2. **Generating example code** - Every code example must come from an actual source file
3. **Skipping agents** - All 6 agents must run; each provides unique perspective
4. **Summarizing without sources** - Every claim needs a file:line or PR/issue reference
5. **Using web search** - No Stack Overflow, no blog posts, no social media

## Verification Checklist

Before finalizing the research document:

- [ ] React repo is at `.claude/react` with known commit hash
- [ ] All 6 agents were spawned in parallel
- [ ] Every code example has a source file reference
- [ ] Warnings/errors table has source locations
- [ ] No claims made without source evidence
- [ ] Discrepancies between Flow/TS types documented
- [ ] Source links section is complete

---
# Source: SKILL.md
---
---
name: docs-voice
description: Use when writing any React documentation. Provides voice, tone, and style rules for all doc types.
---

# React Docs Voice & Style

## Universal Rules

- **Capitalize React terms** when referring to the React concept in headings or as standalone concepts:
  - Core: Hook, Effect, State, Context, Ref, Component, Fragment
  - Concurrent: Transition, Action, Suspense
  - Server: Server Component, Client Component, Server Function, Server Action
  - Patterns: Error Boundary
  - Canary: Activity, View Transition, Transition Type
  - **In prose:** Use lowercase when paired with descriptors: "state variable", "state updates", "event handler". Capitalize when the concept stands alone or in headings: "State is isolated and private"
  - General usage stays lowercase: "the page transitions", "takes an action"
- **Product names:** ESLint, TypeScript, JavaScript, Next.js (not lowercase)
- **Bold** for key concepts: **state variable**, **event handler**
- **Italics** for new terms being defined: *event handlers*
- **Inline code** for APIs: `useState`, `startTransition`, `<Suspense>`
- **Avoid:** "simple", "easy", "just", time estimates
- Frame differences as "capabilities" not "advantages/disadvantages"
- Avoid passive voice and jargon

## Tone by Page Type

| Type | Tone | Example |
|------|------|---------|
| Learn | Conversational | "Here's what that looks like...", "You might be wondering..." |
| Reference | Technical | "Call `useState` at the top level...", "This Hook returns..." |
| Blog | Accurate | Focus on facts, not marketing |

**Note:** Pitfall and DeepDive components can use slightly more conversational phrasing ("You might wonder...", "It might be tempting...") even in Reference pages, since they're explanatory asides.

## Avoiding Jargon

**Pattern:** Explain behavior first, then name it.

✅ "React waits until all code in event handlers runs before processing state updates. This is called *batching*."

❌ "React uses batching to process state updates atomically."

**Terms to avoid or explain:**
| Jargon | Plain Language |
|--------|----------------|
| atomic | all-or-nothing, batched together |
| idempotent | same inputs, same output |
| deterministic | predictable, same result every time |
| memoize | remember the result, skip recalculating |
| referentially transparent | (avoid - describe the behavior) |
| invariant | rule that must always be true |
| reify | (avoid - describe what's being created) |

**Allowed technical terms in Reference pages:**
- "stale closures" - standard JS/React term, can be used in Caveats
- "stable identity" - React term for consistent object references across renders
- "reactive" - React term for values that trigger re-renders when changed
- These don't need explanation in Reference pages (readers are expected to know them)

**Use established analogies sparingly—once when introducing a concept, not repeatedly:**

| Concept | Analogy |
|---------|---------|
| Components/React | Kitchen (components as cooks, React as waiter) |
| Render phases | Restaurant ordering (trigger/render/commit) |
| State batching | Waiter collecting full order before going to kitchen |
| State behavior | Snapshot/photograph in time |
| State storage | React storing state "on a shelf" |
| State purpose | Component's memory |
| Pure functions | Recipes (same ingredients → same dish) |
| Pure functions | Math formulas (y = 2x) |
| Props | Adjustable "knobs" |
| Children prop | "Hole" to be filled by parent |
| Keys | File names in a folder |
| Curly braces in JSX | "Window into JavaScript" |
| Declarative UI | Taxi driver (destination, not turn-by-turn) |
| Imperative UI | Turn-by-turn navigation |
| State structure | Database normalization |
| Refs | "Secret pocket" React doesn't track |
| Effects/Refs | "Escape hatch" from React |
| Context | CSS inheritance / "Teleportation" |
| Custom Hooks | Design system |

## Common Prose Patterns

**Wrong vs Right code:**
```mdx
\`\`\`js
// 🚩 Don't mutate state:
obj.x = 10;
\`\`\`

\`\`\`js
// ✅ Replace with new object:
setObj({ ...obj, x: 10 });
\`\`\`
```

**Table comparisons:**
```mdx
| passing a function | calling a function |
| `onClick={handleClick}` | `onClick={handleClick()}` |
```

**Linking:**
```mdx
[Read about state](/learn/state-a-components-memory)
[See `useState` reference](/reference/react/useState)
```

## Code Style

- Prefer JSX over createElement
- Use const/let, never var
- Prefer named function declarations for top-level functions
- Arrow functions for callbacks that need `this` preservation

## Version Documentation

When APIs change between versions:

```mdx
Starting in React 19, render `<Context>` as a provider:
\`\`\`js
<SomeContext value={value}>{children}</SomeContext>
\`\`\`

In older versions:
\`\`\`js
<SomeContext.Provider value={value}>{children}</SomeContext.Provider>
\`\`\`
```

Patterns:
- "Starting in React 19..." for new APIs
- "In older versions of React..." for legacy patterns

---
# Source: SKILL.md
---
---
name: docs-sandpack
description: Use when adding interactive code examples to React docs.
---

# Sandpack Patterns

## Quick Start Template

Most examples are single-file. Copy this and modify:

```mdx
<Sandpack>

` ` `js
import { useState } from 'react';

export default function Example() {
  const [value, setValue] = useState(0);

  return (
    <button onClick={() => setValue(value + 1)}>
      Clicked {value} times
    </button>
  );
}
` ` `

</Sandpack>
```

---

## File Naming

| Pattern | Usage |
|---------|-------|
| ` ```js ` | Main file (no prefix) |
| ` ```js src/FileName.js ` | Supporting files |
| ` ```js src/File.js active ` | Active file (reference pages) |
| ` ```js src/data.js hidden ` | Hidden files |
| ` ```css ` | CSS styles |
| ` ```json package.json ` | External dependencies |

**Critical:** Main file must have `export default`.

## Line Highlighting

```mdx
```js {2-4}
function Example() {
  // Lines 2-4
  // will be
  // highlighted
  return null;
}
```

## Code References (numbered callouts)

```mdx
```js [[1, 4, "age"], [2, 4, "setAge"]]
// Creates numbered markers pointing to "age" and "setAge" on line 4
```

## Expected Errors (intentionally broken examples)

```mdx
```js {expectedErrors: {'react-compiler': [7]}}
// Line 7 shows as expected error
```

## Multi-File Example

```mdx
<Sandpack>

```js src/App.js
import Gallery from './Gallery.js';

export default function App() {
  return <Gallery />;
}
```

```js src/Gallery.js
export default function Gallery() {
  return <h1>Gallery</h1>;
}
```

```css
h1 { color: purple; }
```

</Sandpack>
```

## External Dependencies

```mdx
<Sandpack>

```js
import { useImmer } from 'use-immer';
// ...
```

```json package.json
{
  "dependencies": {
    "immer": "1.7.3",
    "use-immer": "0.5.1",
    "react": "latest",
    "react-dom": "latest",
    "react-scripts": "latest"
  }
}
```

</Sandpack>
```

## Code Style in Sandpack (Required)

Sandpack examples are held to strict code style standards:

1. **Function declarations** for components (not arrows)
2. **`e`** for event parameters
3. **Single quotes** in JSX
4. **`const`** unless reassignment needed
5. **Spaces in destructuring**: `({ props })` not `({props})`
6. **Two-line createRoot**: separate declaration and render call
7. **Multiline if statements**: always use braces

### Don't Create Hydration Mismatches

Sandpack examples must produce the same output on server and client:

```js
// 🚫 This will cause hydration warnings
export default function App() {
  const isClient = typeof window !== 'undefined';
  return <div>{isClient ? 'Client' : 'Server'}</div>;
}
```

### Use Ref for Non-Rendered State

```js
// 🚫 Don't trigger re-renders for non-visual state
const [mounted, setMounted] = useState(false);
useEffect(() => { setMounted(true); }, []);

// ✅ Use ref instead
const mounted = useRef(false);
useEffect(() => { mounted.current = true; }, []);
```

## forwardRef and memo Patterns

### forwardRef - Use Named Function
```js
// ✅ Named function for DevTools display name
const MyInput = forwardRef(function MyInput(props, ref) {
  return <input {...props} ref={ref} />;
});

// 🚫 Anonymous loses name
const MyInput = forwardRef((props, ref) => { ... });
```

### memo - Use Named Function
```js
// ✅ Preserves component name
const Greeting = memo(function Greeting({ name }) {
  return <h1>Hello, {name}</h1>;
});
```

## Line Length

- Prose: ~80 characters
- Code: ~60-70 characters
- Break long lines to avoid horizontal scrolling

## Anti-Patterns

| Pattern | Problem | Fix |
|---------|---------|-----|
| `const Comp = () => {}` | Not standard | `function Comp() {}` |
| `onClick={(event) => ...}` | Conflicts with global | `onClick={(e) => ...}` |
| `useState` for non-rendered values | Re-renders | Use `useRef` |
| Reading `window` during render | Hydration mismatch | Check in useEffect |
| Single-line if without braces | Harder to debug | Use multiline with braces |
| Chained `createRoot().render()` | Less clear | Two statements |
| `//...` without space | Inconsistent | `// ...` with space |
| Tabs | Inconsistent | 2 spaces |
| `ReactDOM.render` | Deprecated | Use `createRoot` |
| Fake package names | Confusing | Use `'./your-storage-layer'` |
| `PropsWithChildren` | Outdated | `children?: ReactNode` |
| Missing `key` in lists | Warnings | Always include key |

## Additional Code Quality Rules

### Always Include Keys in Lists
```js
// ✅ Correct
{items.map(item => <li key={item.id}>{item.name}</li>)}

// 🚫 Wrong - missing key
{items.map(item => <li>{item.name}</li>)}
```

### Use Realistic Import Paths
```js
// ✅ Correct - descriptive path
import { fetchData } from './your-data-layer';

// 🚫 Wrong - looks like a real npm package
import { fetchData } from 'cool-data-lib';
```

### Console.log Labels
```js
// ✅ Correct - labeled for clarity
console.log('User:', user);
console.log('Component Stack:', errorInfo.componentStack);

// 🚫 Wrong - unlabeled
console.log(user);
```

### Keep Delays Reasonable
```js
// ✅ Correct - 1-1.5 seconds
setTimeout(() => setLoading(false), 1000);

// 🚫 Wrong - too long, feels sluggish
setTimeout(() => setLoading(false), 3000);
```

## Updating Line Highlights

When modifying code in examples with line highlights (`{2-4}`), **always update the highlight line numbers** to match the new code. Incorrect line numbers cause rendering crashes.

## File Name Conventions

- Capitalize file names for component files: `Gallery.js` not `gallery.js`
- After initially explaining files are in `src/`, refer to files by name only: `Gallery.js` not `src/Gallery.js`

## Naming Conventions in Code

**Components:** PascalCase
- `Profile`, `Avatar`, `TodoList`, `PackingList`

**State variables:** Destructured pattern
- `const [count, setCount] = useState(0)`
- Booleans: `[isOnline, setIsOnline]`, `[isPacked, setIsPacked]`
- Status strings: `'typing'`, `'submitting'`, `'success'`, `'error'`

**Event handlers:**
- `handleClick`, `handleSubmit`, `handleAddTask`

**Props for callbacks:**
- `onClick`, `onChange`, `onAddTask`, `onSelect`

**Custom Hooks:**
- `useOnlineStatus`, `useChatRoom`, `useFormInput`

**Reducer actions:**
- Past tense: `'added'`, `'changed'`, `'deleted'`
- Snake_case compounds: `'changed_selection'`, `'sent_message'`

**Updater functions:** Single letter
- `setCount(n => n + 1)`

### Pedagogical Code Markers

**Wrong vs right code:**
```js
// 🔴 Avoid: redundant state and unnecessary Effect
// ✅ Good: calculated during rendering
```

**Console.log for lifecycle teaching:**
```js
console.log('✅ Connecting...');
console.log('❌ Disconnected.');
```

### Server/Client Labeling

```js
// Server Component
async function Notes() {
  const notes = await db.notes.getAll();
}

// Client Component
"use client"
export default function Expandable({children}) {
  const [expanded, setExpanded] = useState(false);
}
```

### Bundle Size Annotations

```js
import marked from 'marked'; // 35.9K (11.2K gzipped)
import sanitizeHtml from 'sanitize-html'; // 206K (63.3K gzipped)
```

---

## Sandpack Example Guidelines

### Package.json Rules

**Include package.json when:**
- Using external npm packages (immer, remarkable, leaflet, toastify-js, etc.)
- Demonstrating experimental/canary React features
- Requiring specific React versions (`react: beta`, `react: 19.0.0-rc-*`)

**Omit package.json when:**
- Example uses only built-in React features
- No external dependencies needed
- Teaching basic hooks, state, or components

**Always mark package.json as hidden:**
```mdx
```json package.json hidden
{
  "dependencies": {
    "react": "latest",
    "react-dom": "latest",
    "react-scripts": "latest",
    "immer": "1.7.3"
  }
}
```
```

**Version conventions:**
- Use `"latest"` for stable features
- Use exact versions only when compatibility requires it
- Include minimal dependencies (just what the example needs)

### Hidden File Patterns

**Always hide these file types:**

| File Type | Reason |
|-----------|--------|
| `package.json` | Configuration not the teaching point |
| `sandbox.config.json` | Sandbox setup is boilerplate |
| `public/index.html` | HTML structure not the focus |
| `src/data.js` | When it contains sample/mock data |
| `src/api.js` | When showing API usage, not implementation |
| `src/styles.css` | When styling is not the lesson |
| `src/router.js` | Supporting infrastructure |
| `src/actions.js` | Server action implementation details |

**Rationale:**
- Reduces cognitive load
- Keeps focus on the primary concept
- Creates cleaner, more focused examples

**Example:**
```mdx
```js src/data.js hidden
export const items = [
  { id: 1, name: 'Item 1' },
  { id: 2, name: 'Item 2' },
];
```
```

### Active File Patterns

**Mark as active when:**
- File contains the primary teaching concept
- Learner should focus on this code first
- Component demonstrates the hook/pattern being taught

**Effect of the `active` marker:**
- Sets initial editor tab focus when Sandpack loads
- Signals "this is what you should study"
- Works with hidden files to create focused examples

**Most common active file:** `src/index.js` or `src/App.js`

**Example:**
```mdx
```js src/App.js active
// This file will be focused when example loads
export default function App() {
  // ...
}
```
```

### File Structure Guidelines

| Scenario | Structure | Reason |
|----------|-----------|--------|
| Basic hook usage | Single file | Simple, focused |
| Teaching imports | 2-3 files | Shows modularity |
| Context patterns | 4-5 files | Realistic structure |
| Complex state | 3+ files | Separation of concerns |

**Single File Examples (70% of cases):**
- Use for simple concepts
- 50-200 lines typical
- Best for: Counter, text inputs, basic hooks

**Multi-File Examples (30% of cases):**
- Use when teaching modularity/imports
- Use for context patterns (4-5 files)
- Use when component is reused

**File Naming:**
- Main component: `App.js` (capitalized)
- Component files: `Gallery.js`, `Button.js` (capitalized)
- Data files: `data.js` (lowercase)
- Utility files: `utils.js` (lowercase)
- Context files: `TasksContext.js` (named after what they provide)

### Code Size Limits

- Single file: **<200 lines**
- Multi-file total: **150-300 lines**
- Main component: **100-150 lines**
- Supporting files: **20-40 lines each**

### CSS Guidelines

**Always:**
- Include minimal CSS for demo interactivity
- Use semantic class names (`.panel`, `.button-primary`, `.panel-dark`)
- Support light/dark themes when showing UI concepts
- Keep CSS visible (never hidden)

**Size Guidelines:**
- Minimal (5-10 lines): Basic button styling, spacing
- Medium (15-30 lines): Panel styling, form layouts
- Complex (40+ lines): Only for layout-focused examples

---
# Source: SKILL.md
---
---
name: docs-components
description: Comprehensive MDX component patterns (Note, Pitfall, DeepDive, Recipes, etc.) for all documentation types. Authoritative source for component usage, examples, and heading conventions.
---

# MDX Component Patterns

## Quick Reference

### Component Decision Tree

| Need | Component |
|------|-----------|
| Helpful tip or terminology | `<Note>` |
| Common mistake warning | `<Pitfall>` |
| Advanced technical explanation | `<DeepDive>` |
| Canary-only feature | `<Canary>` or `<CanaryBadge />` |
| Server Components only | `<RSC>` |
| Deprecated API | `<Deprecated>` |
| Experimental/WIP | `<Wip>` |
| Visual diagram | `<Diagram>` |
| Multiple related examples | `<Recipes>` |
| Interactive code | `<Sandpack>` (see `/docs-sandpack`) |
| Console error display | `<ConsoleBlock>` |
| End-of-page exercises | `<Challenges>` (Learn pages only) |

### Heading Level Conventions

| Component | Heading Level |
|-----------|---------------|
| DeepDive title | `####` (h4) |
| Titled Pitfall | `#####` (h5) |
| Titled Note | `####` (h4) |
| Recipe items | `####` (h4) |
| Challenge items | `####` (h4) |

### Callout Spacing Rules

Callout components (Note, Pitfall, DeepDive) require a **blank line after the opening tag** before content begins.

**Never place consecutively:**
- `<Pitfall>` followed by `<Pitfall>` - Combine into one with titled subsections, or separate with prose
- `<Note>` followed by `<Note>` - Combine into one, or separate with prose

**Allowed consecutive patterns:**
- `<DeepDive>` followed by `<DeepDive>` - OK for multi-part explorations (see useMemo.md)
- `<Pitfall>` followed by `<DeepDive>` - OK when DeepDive explains "why" behind the Pitfall

**Separation content:** Prose paragraphs, code examples (Sandpack), or section headers.

**Why:** Consecutive warnings create a "wall of cautions" that overwhelms readers and causes important warnings to be skimmed.

**Incorrect:**
```mdx
<Pitfall>
Don't do X.
</Pitfall>

<Pitfall>
Don't do Y.
</Pitfall>
```

**Correct - combined:**
```mdx
<Pitfall>

##### Don't do X {/*pitfall-x*/}
Explanation.

##### Don't do Y {/*pitfall-y*/}
Explanation.

</Pitfall>
```

**Correct - separated:**
```mdx
<Pitfall>
Don't do X.
</Pitfall>

This leads to another common mistake:

<Pitfall>
Don't do Y.
</Pitfall>
```

---

## `<Note>`

Important clarifications, conventions, or tips. Less severe than Pitfall.

### Simple Note

```mdx
<Note>

The optimization of caching return values is known as [_memoization_](https://en.wikipedia.org/wiki/Memoization).

</Note>
```

### Note with Title

Use `####` (h4) heading with an ID.

```mdx
<Note>

#### There is no directive for Server Components. {/*no-directive*/}

A common misunderstanding is that Server Components are denoted by `"use server"`, but there is no directive for Server Components. The `"use server"` directive is for Server Functions.

</Note>
```

### Version-Specific Note

```mdx
<Note>

Starting in React 19, you can render `<SomeContext>` as a provider.

In older versions of React, use `<SomeContext.Provider>`.

</Note>
```

---

## `<Pitfall>`

Common mistakes that cause bugs. Use for errors readers will likely make.

### Simple Pitfall

```mdx
<Pitfall>

We recommend defining components as functions instead of classes. [See how to migrate.](#alternatives)

</Pitfall>
```

### Titled Pitfall

Use `#####` (h5) heading with an ID.

```mdx
<Pitfall>

##### Calling different memoized functions will read from different caches. {/*pitfall-different-caches*/}

To access the same cache, components must call the same memoized function.

</Pitfall>
```

### Pitfall with Wrong/Right Code

```mdx
<Pitfall>

##### `useFormStatus` will not return status information for a `<form>` rendered in the same component. {/*pitfall-same-component*/}

```js
function Form() {
  // 🔴 `pending` will never be true
  const { pending } = useFormStatus();
  return <form action={submit}></form>;
}
```

Instead call `useFormStatus` from inside a component located inside `<form>`.

</Pitfall>
```

---

## `<DeepDive>`

Optional deep technical content. **First child must be `####` heading with ID.**

### Standard DeepDive

```mdx
<DeepDive>

#### Is using an updater always preferred? {/*is-updater-preferred*/}

You might hear a recommendation to always write code like `setAge(a => a + 1)` if the state you're setting is calculated from the previous state. There's no harm in it, but it's also not always necessary.

In most cases, there is no difference between these two approaches. React always makes sure that for intentional user actions, like clicks, the `age` state variable would be updated before the next click.

</DeepDive>
```

### Comparison DeepDive

For comparing related concepts:

```mdx
<DeepDive>

#### When should I use `cache`, `memo`, or `useMemo`? {/*cache-memo-usememo*/}

All mentioned APIs offer memoization but differ in what they memoize, who can access the cache, and when their cache is invalidated.

#### `useMemo` {/*deep-dive-usememo*/}

In general, you should use `useMemo` for caching expensive computations in Client Components across renders.

#### `cache` {/*deep-dive-cache*/}

In general, you should use `cache` in Server Components to memoize work that can be shared across components.

</DeepDive>
```

---

## `<Recipes>`

Multiple related examples showing variations. Each recipe needs `<Solution />`.

```mdx
<Recipes titleText="Basic useState examples" titleId="examples-basic">

#### Counter (number) {/*counter-number*/}

In this example, the `count` state variable holds a number.

<Sandpack>
{/* code */}
</Sandpack>

<Solution />

#### Text field (string) {/*text-field-string*/}

In this example, the `text` state variable holds a string.

<Sandpack>
{/* code */}
</Sandpack>

<Solution />

</Recipes>
```

**Common titleText/titleId combinations:**
- "Basic [hookName] examples" / `examples-basic`
- "Examples of [concept]" / `examples-[concept]`
- "The difference between [A] and [B]" / `examples-[topic]`

---

## `<Challenges>`

End-of-page exercises. **Learn pages only.** Each challenge needs problem + solution Sandpack.

```mdx
<Challenges>

#### Fix the bug {/*fix-the-bug*/}

Problem description...

<Hint>
Optional hint text.
</Hint>

<Sandpack>
{/* problem code */}
</Sandpack>

<Solution>

Explanation...

<Sandpack>
{/* solution code */}
</Sandpack>

</Solution>

</Challenges>
```

**Guidelines:**
- Only at end of standard Learn pages
- No Challenges in chapter intros or tutorials
- Each challenge has `####` heading with ID

---

## `<Deprecated>`

For deprecated APIs. Content should explain what to use instead.

### Page-Level Deprecation

```mdx
<Deprecated>

In React 19, `forwardRef` is no longer necessary. Pass `ref` as a prop instead.

`forwardRef` will be deprecated in a future release. Learn more [here](/blog/2024/04/25/react-19#ref-as-a-prop).

</Deprecated>
```

### Method-Level Deprecation

```mdx
### `componentWillMount()` {/*componentwillmount*/}

<Deprecated>

This API has been renamed from `componentWillMount` to [`UNSAFE_componentWillMount`.](#unsafe_componentwillmount)

Run the [`rename-unsafe-lifecycles` codemod](codemod-link) to automatically update.

</Deprecated>
```

---

## `<RSC>`

For APIs that only work with React Server Components.

### Basic RSC

```mdx
<RSC>

`cache` is only for use with [React Server Components](/reference/rsc/server-components).

</RSC>
```

### Extended RSC (for Server Functions)

```mdx
<RSC>

Server Functions are for use in [React Server Components](/reference/rsc/server-components).

**Note:** Until September 2024, we referred to all Server Functions as "Server Actions".

</RSC>
```

---

## `<Canary>` and `<CanaryBadge />`

For features only available in Canary releases.

### Canary Wrapper (inline in Intro)

```mdx
<Intro>

`<Fragment>` lets you group elements without a wrapper node.

<Canary>Fragments can also accept refs, enabling interaction with underlying DOM nodes.</Canary>

</Intro>
```

### CanaryBadge in Section Headings

```mdx
### <CanaryBadge /> FragmentInstance {/*fragmentinstance*/}
```

### CanaryBadge in Props Lists

```mdx
* <CanaryBadge /> **optional** `ref`: A ref object from `useRef` or callback function.
```

### CanaryBadge in Caveats

```mdx
* <CanaryBadge /> If you want to pass `ref` to a Fragment, you can't use the `<>...</>` syntax.
```

---

## `<Diagram>`

Visual explanations of module dependencies, render trees, or data flow.

```mdx
<Diagram name="use_client_module_dependency" height={250} width={545} alt="A tree graph with the top node representing the module 'App.js'. 'App.js' has three children...">
`'use client'` segments the module dependency tree, marking `InspirationGenerator.js` and all dependencies as client-rendered.
</Diagram>
```

**Attributes:**
- `name`: Diagram identifier (used for image file)
- `height`: Height in pixels
- `width`: Width in pixels
- `alt`: Accessible description of the diagram

---

## `<CodeStep>` (Use Sparingly)

Numbered callouts in prose. Pairs with code block annotations.

### Syntax

In code blocks:
```mdx
```js [[1, 4, "age"], [2, 4, "setAge"], [3, 4, "42"]]
import { useState } from 'react';

function MyComponent() {
  const [age, setAge] = useState(42);
}
```
```

Format: `[[step_number, line_number, "text_to_highlight"], ...]`

In prose:
```mdx
1. The <CodeStep step={1}>current state</CodeStep> initially set to the <CodeStep step={3}>initial value</CodeStep>.
2. The <CodeStep step={2}>`set` function</CodeStep> that lets you change it.
```

### Guidelines

- Maximum 2-3 different colors per explanation
- Don't highlight every keyword - only key concepts
- Use for terms in prose, not entire code blocks
- Maintain consistent usage within a section

✅ **Good use** - highlighting key concepts:
```mdx
React will compare the <CodeStep step={2}>dependencies</CodeStep> with the dependencies you passed...
```

🚫 **Avoid** - excessive highlighting:
```mdx
When an <CodeStep step={1}>Activity</CodeStep> boundary is <CodeStep step={2}>hidden</CodeStep> during its <CodeStep step={3}>initial</CodeStep> render...
```

---

## `<ConsoleBlock>`

Display console output (errors, warnings, logs).

```mdx
<ConsoleBlock level="error">
Uncaught Error: Too many re-renders.
</ConsoleBlock>
```

**Levels:** `error`, `warning`, `info`

---

## Component Usage by Page Type

### Reference Pages

For component placement rules specific to Reference pages, invoke `/docs-writer-reference`.

Key placement patterns:
- `<RSC>` goes before `<Intro>` at top of page
- `<Deprecated>` goes after `<Intro>` for page-level deprecation
- `<Deprecated>` goes after method heading for method-level deprecation
- `<Canary>` wrapper goes inline within `<Intro>`
- `<CanaryBadge />` appears in headings, props lists, and caveats

### Learn Pages

For Learn page structure and patterns, invoke `/docs-writer-learn`.

Key usage patterns:
- Challenges only at end of standard Learn pages
- No Challenges in chapter intros or tutorials
- DeepDive for optional advanced content
- CodeStep should be used sparingly

### Blog Pages

For Blog page structure and patterns, invoke `/docs-writer-blog`.

Key usage patterns:
- Generally avoid deep technical components
- Note and Pitfall OK for clarifications
- Prefer inline explanations over DeepDive

---

## Other Available Components

**Version/Status:** `<Experimental>`, `<ExperimentalBadge />`, `<RSCBadge />`, `<NextMajor>`, `<Wip>`

**Visuals:** `<DiagramGroup>`, `<Illustration>`, `<IllustrationBlock>`, `<CodeDiagram>`, `<FullWidth>`

**Console:** `<ConsoleBlockMulti>`, `<ConsoleLogLine>`

**Specialized:** `<TerminalBlock>`, `<BlogCard>`, `<TeamMember>`, `<YouTubeIframe>`, `<ErrorDecoder />`, `<LearnMore>`, `<Math>`, `<MathI>`, `<LanguageList>`

See existing docs for usage examples of these components.

---
# Source: SKILL.md
---
---
name: docs-writer-blog
description: Use when writing or editing files in src/content/blog/. Provides blog post structure and conventions.
---

# Blog Post Writer

## Persona

**Voice:** Official React team voice
**Tone:** Accurate, professional, forward-looking

## Voice & Style

For tone, capitalization, jargon, and prose patterns, invoke `/docs-voice`.

---

## Frontmatter Schema

All blog posts use this YAML frontmatter structure:

```yaml
---
title: "Title in Quotes"
author: Author Name(s)
date: YYYY/MM/DD
description: One or two sentence summary.
---
```

### Field Details

| Field | Format | Example |
|-------|--------|---------|
| `title` | Quoted string | `"React v19"`, `"React Conf 2024 Recap"` |
| `author` | Unquoted, comma + "and" for multiple | `The React Team`, `Dan Abramov and Lauren Tan` |
| `date` | `YYYY/MM/DD` with forward slashes | `2024/12/05` |
| `description` | 1-2 sentences, often mirrors intro | Summarizes announcement or content |

### Title Patterns by Post Type

| Type | Pattern | Example |
|------|---------|---------|
| Release | `"React vX.Y"` or `"React X.Y"` | `"React v19"` |
| Upgrade | `"React [VERSION] Upgrade Guide"` | `"How to Upgrade to React 18"` |
| Labs | `"React Labs: [Topic] – [Month Year]"` | `"React Labs: What We've Been Working On – February 2024"` |
| Conf | `"React Conf [YEAR] Recap"` | `"React Conf 2024 Recap"` |
| Feature | `"Introducing [Feature]"` or descriptive | `"Introducing react.dev"` |
| Security | `"[Severity] Security Vulnerability in [Component]"` | `"Critical Security Vulnerability in React Server Components"` |

---

## Author Byline

Immediately after frontmatter, add a byline:

```markdown
---

Month DD, YYYY by [Author Name](social-link)

---
```

### Conventions

- Full date spelled out: `December 05, 2024`
- Team posts link to `/community/team`: `[The React Team](/community/team)`
- Individual authors link to Twitter/X or Bluesky
- Multiple authors: Oxford comma before "and"
- Followed by horizontal rule `---`

**Examples:**

```markdown
December 05, 2024 by [The React Team](/community/team)

---
```

```markdown
May 3, 2023 by [Dan Abramov](https://bsky.app/profile/danabra.mov), [Sophie Alpert](https://twitter.com/sophiebits), and [Andrew Clark](https://twitter.com/acdlite)

---
```

---

## Universal Post Structure

All blog posts follow this structure:

1. **Frontmatter** (YAML)
2. **Author byline** with date
3. **Horizontal rule** (`---`)
4. **`<Intro>` component** (1-3 sentences)
5. **Horizontal rule** (`---`) (optional)
6. **Main content sections** (H2 with IDs)
7. **Closing section** (Changelog, Thanks, etc.)

---

## Post Type Templates

### Major Release Announcement

```markdown
---
title: "React vX.Y"
author: The React Team
date: YYYY/MM/DD
description: React X.Y is now available on npm! In this post, we'll give an overview of the new features.
---

Month DD, YYYY by [The React Team](/community/team)

---

<Intro>

React vX.Y is now available on npm!

</Intro>

In our [Upgrade Guide](/blog/YYYY/MM/DD/react-xy-upgrade-guide), we shared step-by-step instructions for upgrading. In this post, we'll give an overview of what's new.

- [What's new in React X.Y](#whats-new)
- [Improvements](#improvements)
- [How to upgrade](#how-to-upgrade)

---

## What's new in React X.Y {/*whats-new*/}

### Feature Name {/*feature-name*/}

[Problem this solves. Before/after code examples.]

For more information, see the docs for [`Feature`](/reference/react/Feature).

---

## Improvements in React X.Y {/*improvements*/}

### Improvement Name {/*improvement-name*/}

[Description of improvement.]

---

## How to upgrade {/*how-to-upgrade*/}

See [How to Upgrade to React X.Y](/blog/YYYY/MM/DD/react-xy-upgrade-guide) for step-by-step instructions.

---

## Changelog {/*changelog*/}

### React {/*react*/}

* Add `useNewHook` for [purpose]. ([#12345](https://github.com/facebook/react/pull/12345) by [@contributor](https://github.com/contributor))

---

_Thanks to [Name](url) for reviewing this post._
```

### Upgrade Guide

```markdown
---
title: "React [VERSION] Upgrade Guide"
author: Author Name
date: YYYY/MM/DD
description: Step-by-step instructions for upgrading to React [VERSION].
---

Month DD, YYYY by [Author Name](social-url)

---

<Intro>

[Summary of upgrade and what this guide covers.]

</Intro>

<Note>

#### Stepping stone version {/*stepping-stone*/}

[If applicable, describe intermediate upgrade steps.]

</Note>

In this post, we will guide you through the steps for upgrading:

- [Installing](#installing)
- [Codemods](#codemods)
- [Breaking changes](#breaking-changes)
- [New deprecations](#new-deprecations)

---

## Installing {/*installing*/}

```bash
npm install --save-exact react@^X.Y.Z react-dom@^X.Y.Z
```

## Codemods {/*codemods*/}

<Note>

#### Run all React [VERSION] codemods {/*run-all-codemods*/}

```bash
npx codemod@latest react/[VERSION]/migration-recipe
```

</Note>

## Breaking changes {/*breaking-changes*/}

### Removed: `apiName` {/*removed-api-name*/}

`apiName` was deprecated in [Month YYYY (vX.X.X)](link).

```js
// Before
[old code]

// After
[new code]
```

<Note>

Codemod [description]:

```bash
npx codemod@latest react/[VERSION]/codemod-name
```

</Note>

## New deprecations {/*new-deprecations*/}

### Deprecated: `apiName` {/*deprecated-api-name*/}

[Explanation and migration path.]

---

Thanks to [Contributor](link) for reviewing this post.
```

### React Labs Research Update

```markdown
---
title: "React Labs: What We've Been Working On – [Month Year]"
author: Author1, Author2, and Author3
date: YYYY/MM/DD
description: In React Labs posts, we write about projects in active research and development.
---

Month DD, YYYY by [Author1](url), [Author2](url), and [Author3](url)

---

<Intro>

In React Labs posts, we write about projects in active research and development. We've made significant progress since our [last update](/blog/previous-labs-post), and we'd like to share our progress.

</Intro>

[Optional: Roadmap disclaimer about timelines]

---

## Feature Name {/*feature-name*/}

<Note>

`<FeatureName />` is now available in React's Canary channel.

</Note>

[Description of feature, motivation, current status.]

### Subsection {/*subsection*/}

[Details, examples, use cases.]

---

## Research Area {/*research-area*/}

[Problem space description. Status communication.]

This research is still early. We'll share more when we're further along.

---

_Thanks to [Reviewer](url) for reviewing this post._

Thanks for reading, and see you in the next update!
```

### React Conf Recap

```markdown
---
title: "React Conf [YEAR] Recap"
author: Author1 and Author2
date: YYYY/MM/DD
description: Last week we hosted React Conf [YEAR]. In this post, we'll summarize the talks and announcements.
---

Month DD, YYYY by [Author1](url) and [Author2](url)

---

<Intro>

Last week we hosted React Conf [YEAR] [where we announced [key announcements]].

</Intro>

---

The entire [day 1](youtube-url) and [day 2](youtube-url) streams are available online.

## Day 1 {/*day-1*/}

_[Watch the full day 1 stream here.](youtube-url)_

[Description of day 1 opening and keynote highlights.]

Watch the full day 1 keynote here:

<YouTubeIframe src="https://www.youtube.com/embed/VIDEO_ID" />

## Day 2 {/*day-2*/}

_[Watch the full day 2 stream here.](youtube-url)_

[Day 2 summary.]

<YouTubeIframe src="https://www.youtube.com/embed/VIDEO_ID" />

## Q&A {/*q-and-a*/}

* [Q&A Title](youtube-url) hosted by [Host](url)

## And more... {/*and-more*/}

We also heard talks including:
* [Talk Title](youtube-url) by [Speaker](url)

## Thank you {/*thank-you*/}

Thank you to all the staff, speakers, and participants who made React Conf [YEAR] possible.

See you next time!
```

### Feature/Tool Announcement

```markdown
---
title: "Introducing [Feature Name]"
author: Author Name
date: YYYY/MM/DD
description: Today we are announcing [feature]. In this post, we'll explain [what this post covers].
---

Month DD, YYYY by [Author Name](url)

---

<Intro>

Today we are [excited/thrilled] to announce [feature]. [What this means for users.]

</Intro>

---

## tl;dr {/*tldr*/}

* Key announcement point with [relevant link](/path).
* What users can do now.
* Availability or adoption information.

## What is [Feature]? {/*what-is-feature*/}

[Explanation of the feature/tool.]

## Why we built this {/*why-we-built-this*/}

[Motivation, history, problem being solved.]

## Getting started {/*getting-started*/}

To install [feature]:

<TerminalBlock>
npm install package-name
</TerminalBlock>

[You can find more documentation here.](/path/to/docs)

## What's next {/*whats-next*/}

[Future plans and next steps.]

## Thank you {/*thank-you*/}

[Acknowledgments to contributors.]

---

Thanks to [Reviewer](url) for reviewing this post.
```

### Security Announcement

```markdown
---
title: "[Severity] Security Vulnerability in [Component]"
author: The React Team
date: YYYY/MM/DD
description: Brief summary of the vulnerability. A fix has been published. We recommend upgrading immediately.

---

Month DD, YYYY by [The React Team](/community/team)

---

<Intro>

[One or two sentences summarizing the vulnerability.]

We recommend upgrading immediately.

</Intro>

---

On [date], [researcher] reported a security vulnerability that allows [description].

This vulnerability was disclosed as [CVE-YYYY-NNNNN](https://www.cve.org/CVERecord?id=CVE-YYYY-NNNNN) and is rated CVSS [score].

The vulnerability is present in versions [list] of:

* [package-name](https://www.npmjs.com/package/package-name)

## Immediate Action Required {/*immediate-action-required*/}

A fix was introduced in versions [linked versions]. Upgrade immediately.

### Affected frameworks {/*affected-frameworks*/}

[List of affected frameworks with npm links.]

### Vulnerability overview {/*vulnerability-overview*/}

[Technical explanation of the vulnerability.]

## Update Instructions {/*update-instructions*/}

### Framework Name {/*update-framework-name*/}

```bash
npm install package@version
```

## Timeline {/*timeline*/}

* **November 29th**: [Researcher] reported the vulnerability.
* **December 1st**: Fix was created and validated.
* **December 3rd**: Fix published and CVE disclosed.

## Attribution {/*attribution*/}

Thank you to [Researcher Name](url) for discovering and reporting this vulnerability.
```

---

## Heading Conventions

### ID Syntax

All headings require IDs using CSS comment syntax:

```markdown
## Heading Text {/*heading-id*/}
```

### ID Rules

- Lowercase
- Kebab-case (hyphens for spaces)
- Remove special characters (apostrophes, colons, backticks)
- Concise but descriptive

### Heading Patterns

| Context | Example |
|---------|---------|
| Feature section | `## New Feature: Automatic Batching {/*new-feature-automatic-batching*/}` |
| New hook | `### New hook: \`useActionState\` {/*new-hook-useactionstate*/}` |
| API in backticks | `### \`<Activity />\` {/*activity*/}` |
| Removed API | `#### Removed: \`propTypes\` {/*removed-proptypes*/}` |
| tl;dr section | `## tl;dr {/*tldr*/}` |

---

## Component Usage Guide

### Blog-Appropriate Components

| Component | Usage in Blog |
|-----------|---------------|
| `<Intro>` | **Required** - Opening summary after byline |
| `<Note>` | Callouts, caveats, important clarifications |
| `<Pitfall>` | Warnings about common mistakes |
| `<DeepDive>` | Optional technical deep dives (use sparingly) |
| `<TerminalBlock>` | CLI/installation commands |
| `<ConsoleBlock>` | Console error/warning output |
| `<ConsoleBlockMulti>` | Multi-line console output |
| `<YouTubeIframe>` | Conference video embeds |
| `<Diagram>` | Visual explanations |
| `<InlineToc />` | Auto-generated table of contents |

### `<Intro>` Pattern

Always wrap opening paragraph:

```markdown
<Intro>

React 19 is now available on npm!

</Intro>
```

### `<Note>` Patterns

**Simple note:**
```markdown
<Note>

For React Native users, React 18 ships with the New Architecture.

</Note>
```

**Titled note (H4 inside):**
```markdown
<Note>

#### React 18.3 has also been published {/*react-18-3*/}

To help with the upgrade, we've published `react@18.3`...

</Note>
```

### `<TerminalBlock>` Pattern

```markdown
<TerminalBlock>
npm install react@latest react-dom@latest
</TerminalBlock>
```

### `<YouTubeIframe>` Pattern

```markdown
<YouTubeIframe src="https://www.youtube.com/embed/VIDEO_ID" />
```

---

## Link Patterns

### Internal Links

| Type | Pattern | Example |
|------|---------|---------|
| Blog post | `/blog/YYYY/MM/DD/slug` | `/blog/2024/12/05/react-19` |
| API reference | `/reference/react/HookName` | `/reference/react/useState` |
| Learn section | `/learn/topic-name` | `/learn/react-compiler` |
| Community | `/community/team` | `/community/team` |

### External Links

| Type | Pattern |
|------|---------|
| GitHub PR | `[#12345](https://github.com/facebook/react/pull/12345)` |
| GitHub user | `[@username](https://github.com/username)` |
| Twitter/X | `[@username](https://x.com/username)` |
| Bluesky | `[Name](https://bsky.app/profile/handle)` |
| CVE | `[CVE-YYYY-NNNNN](https://www.cve.org/CVERecord?id=CVE-YYYY-NNNNN)` |
| npm package | `[package](https://www.npmjs.com/package/package)` |

### "See docs" Pattern

```markdown
For more information, see the docs for [`useActionState`](/reference/react/useActionState).
```

---

## Changelog Format

### Bullet Pattern

```markdown
* Add `useTransition` for concurrent rendering. ([#10426](https://github.com/facebook/react/pull/10426) by [@acdlite](https://github.com/acdlite))
* Fix `useReducer` observing incorrect props. ([#22445](https://github.com/facebook/react/pull/22445) by [@josephsavona](https://github.com/josephsavona))
```

**Structure:** `Verb` + backticked API + description + `([#PR](url) by [@user](url))`

**Verbs:** Add, Fix, Remove, Make, Improve, Allow, Deprecate

### Section Organization

```markdown
## Changelog {/*changelog*/}

### React {/*react*/}

* [changes]

### React DOM {/*react-dom*/}

* [changes]
```

---

## Acknowledgments Format

### Post-closing Thanks

```markdown
---

Thanks to [Name](url), [Name](url), and [Name](url) for reviewing this post.
```

Or italicized:

```markdown
_Thanks to [Name](url) for reviewing this post._
```

### Update Notes

For post-publication updates:

```markdown
<Note>

[Updated content]

-----

_Updated January 26, 2026._

</Note>
```

---

## Tone & Length by Post Type

| Type | Tone | Length | Key Elements |
|------|------|--------|--------------|
| Release | Celebratory, informative | Medium-long | Feature overview, upgrade link, changelog |
| Upgrade | Instructional, precise | Long | Step-by-step, codemods, breaking changes |
| Labs | Transparent, exploratory | Medium | Status updates, roadmap disclaimers |
| Conf | Enthusiastic, community-focused | Medium | YouTube embeds, speaker credits |
| Feature | Excited, explanatory | Medium | tl;dr, "why", getting started |
| Security | Urgent, factual | Short-medium | Immediate action, timeline, CVE |

---

## Do's and Don'ts

**Do:**
- Focus on facts over marketing
- Say "upcoming" explicitly for unreleased features
- Include FAQ sections for major announcements
- Credit contributors and link to GitHub
- Use "we" voice for team posts
- Link to upgrade guides from release posts
- Include table of contents for long posts
- End with acknowledgments

**Don't:**
- Promise features not yet available
- Rewrite history (add update notes instead)
- Break existing URLs
- Use hyperbolic language ("revolutionary", "game-changing")
- Skip the `<Intro>` component
- Forget heading IDs
- Use heavy component nesting in blogs
- Make time estimates or predictions

---

## Updating Old Posts

- Never break existing URLs; add redirects when URLs change
- Don't rewrite history; add update notes instead:
  ```markdown
  <Note>

  [Updated information]

  -----

  _Updated Month Year._

  </Note>
  ```

---

## Critical Rules

1. **Heading IDs required:** `## Title {/*title-id*/}`
2. **`<Intro>` required:** Every post starts with `<Intro>` component
3. **Byline required:** Date + linked author(s) after frontmatter
4. **Date format:** Frontmatter uses `YYYY/MM/DD`, byline uses `Month DD, YYYY`
5. **Link to docs:** New APIs must link to reference documentation
6. **Security posts:** Always include "We recommend upgrading immediately"

---

## Components Reference

For complete MDX component patterns, invoke `/docs-components`.

Blog posts commonly use: `<Intro>`, `<Note>`, `<Pitfall>`, `<TerminalBlock>`, `<ConsoleBlock>`, `<YouTubeIframe>`, `<DeepDive>`, `<Diagram>`.

Prefer inline explanations over heavy component usage.

---
# Source: LICENSE-DOCS.md
---
Attribution 4.0 International

=======================================================================

Creative Commons Corporation ("Creative Commons") is not a law firm and
does not provide legal services or legal advice. Distribution of
Creative Commons public licenses does not create a lawyer-client or
other relationship. Creative Commons makes its licenses and related
information available on an "as-is" basis. Creative Commons gives no
warranties regarding its licenses, any material licensed under their
terms and conditions, or any related information. Creative Commons
disclaims all liability for damages resulting from their use to the
fullest extent possible.

Using Creative Commons Public Licenses

Creative Commons public licenses provide a standard set of terms and
conditions that creators and other rights holders may use to share
original works of authorship and other material subject to copyright
and certain other rights specified in the public license below. The
following considerations are for informational purposes only, are not
exhaustive, and do not form part of our licenses.

     Considerations for licensors: Our public licenses are
     intended for use by those authorized to give the public
     permission to use material in ways otherwise restricted by
     copyright and certain other rights. Our licenses are
     irrevocable. Licensors should read and understand the terms
     and conditions of the license they choose before applying it.
     Licensors should also secure all rights necessary before
     applying our licenses so that the public can reuse the
     material as expected. Licensors should clearly mark any
     material not subject to the license. This includes other CC-
     licensed material, or material used under an exception or
     limitation to copyright. More considerations for licensors:
  wiki.creativecommons.org/Considerations_for_licensors

     Considerations for the public: By using one of our public
     licenses, a licensor grants the public permission to use the
     licensed material under specified terms and conditions. If
     the licensor's permission is not necessary for any reason--for
     example, because of any applicable exception or limitation to
     copyright--then that use is not regulated by the license. Our
     licenses grant only permissions under copyright and certain
     other rights that a licensor has authority to grant. Use of
     the licensed material may still be restricted for other
     reasons, including because others have copyright or other
     rights in the material. A licensor may make special requests,
     such as asking that all changes be marked or described.
     Although not required by our licenses, you are encouraged to
     respect those requests where reasonable. More_considerations
     for the public:
  wiki.creativecommons.org/Considerations_for_licensees

=======================================================================

Creative Commons Attribution 4.0 International Public License

By exercising the Licensed Rights (defined below), You accept and agree
to be bound by the terms and conditions of this Creative Commons
Attribution 4.0 International Public License ("Public License"). To the
extent this Public License may be interpreted as a contract, You are
granted the Licensed Rights in consideration of Your acceptance of
these terms and conditions, and the Licensor grants You such rights in
consideration of benefits the Licensor receives from making the
Licensed Material available under these terms and conditions.


Section 1 -- Definitions.

  a. Adapted Material means material subject to Copyright and Similar
     Rights that is derived from or based upon the Licensed Material
     and in which the Licensed Material is translated, altered,
     arranged, transformed, or otherwise modified in a manner requiring
     permission under the Copyright and Similar Rights held by the
     Licensor. For purposes of this Public License, where the Licensed
     Material is a musical work, performance, or sound recording,
     Adapted Material is always produced where the Licensed Material is
     synched in timed relation with a moving image.

  b. Adapter's License means the license You apply to Your Copyright
     and Similar Rights in Your contributions to Adapted Material in
     accordance with the terms and conditions of this Public License.

  c. Copyright and Similar Rights means copyright and/or similar rights
     closely related to copyright including, without limitation,
     performance, broadcast, sound recording, and Sui Generis Database
     Rights, without regard to how the rights are labeled or
     categorized. For purposes of this Public License, the rights
     specified in Section 2(b)(1)-(2) are not Copyright and Similar
     Rights.

  d. Effective Technological Measures means those measures that, in the
     absence of proper authority, may not be circumvented under laws
     fulfilling obligations under Article 11 of the WIPO Copyright
     Treaty adopted on December 20, 1996, and/or similar international
     agreements.

  e. Exceptions and Limitations means fair use, fair dealing, and/or
     any other exception or limitation to Copyright and Similar Rights
     that applies to Your use of the Licensed Material.

  f. Licensed Material means the artistic or literary work, database,
     or other material to which the Licensor applied this Public
     License.

  g. Licensed Rights means the rights granted to You subject to the
     terms and conditions of this Public License, which are limited to
     all Copyright and Similar Rights that apply to Your use of the
     Licensed Material and that the Licensor has authority to license.

  h. Licensor means the individual(s) or entity(ies) granting rights
     under this Public License.

  i. Share means to provide material to the public by any means or
     process that requires permission under the Licensed Rights, such
     as reproduction, public display, public performance, distribution,
     dissemination, communication, or importation, and to make material
     available to the public including in ways that members of the
     public may access the material from a place and at a time
     individually chosen by them.

  j. Sui Generis Database Rights means rights other than copyright
     resulting from Directive 96/9/EC of the European Parliament and of
     the Council of 11 March 1996 on the legal protection of databases,
     as amended and/or succeeded, as well as other essentially
     equivalent rights anywhere in the world.

  k. You means the individual or entity exercising the Licensed Rights
     under this Public License. Your has a corresponding meaning.


Section 2 -- Scope.

  a. License grant.

       1. Subject to the terms and conditions of this Public License,
          the Licensor hereby grants You a worldwide, royalty-free,
          non-sublicensable, non-exclusive, irrevocable license to
          exercise the Licensed Rights in the Licensed Material to:

            a. reproduce and Share the Licensed Material, in whole or
               in part; and

            b. produce, reproduce, and Share Adapted Material.

       2. Exceptions and Limitations. For the avoidance of doubt, where
          Exceptions and Limitations apply to Your use, this Public
          License does not apply, and You do not need to comply with
          its terms and conditions.

       3. Term. The term of this Public License is specified in Section
          6(a).

       4. Media and formats; technical modifications allowed. The
          Licensor authorizes You to exercise the Licensed Rights in
          all media and formats whether now known or hereafter created,
          and to make technical modifications necessary to do so. The
          Licensor waives and/or agrees not to assert any right or
          authority to forbid You from making technical modifications
          necessary to exercise the Licensed Rights, including
          technical modifications necessary to circumvent Effective
          Technological Measures. For purposes of this Public License,
          simply making modifications authorized by this Section 2(a)
          (4) never produces Adapted Material.

       5. Downstream recipients.

            a. Offer from the Licensor -- Licensed Material. Every
               recipient of the Licensed Material automatically
               receives an offer from the Licensor to exercise the
               Licensed Rights under the terms and conditions of this
               Public License.

            b. No downstream restrictions. You may not offer or impose
               any additional or different terms or conditions on, or
               apply any Effective Technological Measures to, the
               Licensed Material if doing so restricts exercise of the
               Licensed Rights by any recipient of the Licensed
               Material.

       6. No endorsement. Nothing in this Public License constitutes or
          may be construed as permission to assert or imply that You
          are, or that Your use of the Licensed Material is, connected
          with, or sponsored, endorsed, or granted official status by,
          the Licensor or others designated to receive attribution as
          provided in Section 3(a)(1)(A)(i).

  b. Other rights.

       1. Moral rights, such as the right of integrity, are not
          licensed under this Public License, nor are publicity,
          privacy, and/or other similar personality rights; however, to
          the extent possible, the Licensor waives and/or agrees not to
          assert any such rights held by the Licensor to the limited
          extent necessary to allow You to exercise the Licensed
          Rights, but not otherwise.

       2. Patent and trademark rights are not licensed under this
          Public License.

       3. To the extent possible, the Licensor waives any right to
          collect royalties from You for the exercise of the Licensed
          Rights, whether directly or through a collecting society
          under any voluntary or waivable statutory or compulsory
          licensing scheme. In all other cases the Licensor expressly
          reserves any right to collect such royalties.


Section 3 -- License Conditions.

Your exercise of the Licensed Rights is expressly made subject to the
following conditions.

  a. Attribution.

       1. If You Share the Licensed Material (including in modified
          form), You must:

            a. retain the following if it is supplied by the Licensor
               with the Licensed Material:

                 i. identification of the creator(s) of the Licensed
                    Material and any others designated to receive
                    attribution, in any reasonable manner requested by
                    the Licensor (including by pseudonym if
                    designated);

                ii. a copyright notice;

               iii. a notice that refers to this Public License;

                iv. a notice that refers to the disclaimer of
                    warranties;

                 v. a URI or hyperlink to the Licensed Material to the
                    extent reasonably practicable;

            b. indicate if You modified the Licensed Material and
               retain an indication of any previous modifications; and

            c. indicate the Licensed Material is licensed under this
               Public License, and include the text of, or the URI or
               hyperlink to, this Public License.

       2. You may satisfy the conditions in Section 3(a)(1) in any
          reasonable manner based on the medium, means, and context in
          which You Share the Licensed Material. For example, it may be
          reasonable to satisfy the conditions by providing a URI or
          hyperlink to a resource that includes the required
          information.

       3. If requested by the Licensor, You must remove any of the
          information required by Section 3(a)(1)(A) to the extent
          reasonably practicable.

       4. If You Share Adapted Material You produce, the Adapter's
          License You apply must not prevent recipients of the Adapted
          Material from complying with this Public License.


Section 4 -- Sui Generis Database Rights.

Where the Licensed Rights include Sui Generis Database Rights that
apply to Your use of the Licensed Material:

  a. for the avoidance of doubt, Section 2(a)(1) grants You the right
     to extract, reuse, reproduce, and Share all or a substantial
     portion of the contents of the database;

  b. if You include all or a substantial portion of the database
     contents in a database in which You have Sui Generis Database
     Rights, then the database in which You have Sui Generis Database
     Rights (but not its individual contents) is Adapted Material; and

  c. You must comply with the conditions in Section 3(a) if You Share
     all or a substantial portion of the contents of the database.

For the avoidance of doubt, this Section 4 supplements and does not
replace Your obligations under this Public License where the Licensed
Rights include other Copyright and Similar Rights.


Section 5 -- Disclaimer of Warranties and Limitation of Liability.

  a. UNLESS OTHERWISE SEPARATELY UNDERTAKEN BY THE LICENSOR, TO THE
     EXTENT POSSIBLE, THE LICENSOR OFFERS THE LICENSED MATERIAL AS-IS
     AND AS-AVAILABLE, AND MAKES NO REPRESENTATIONS OR WARRANTIES OF
     ANY KIND CONCERNING THE LICENSED MATERIAL, WHETHER EXPRESS,
     IMPLIED, STATUTORY, OR OTHER. THIS INCLUDES, WITHOUT LIMITATION,
     WARRANTIES OF TITLE, MERCHANTABILITY, FITNESS FOR A PARTICULAR
     PURPOSE, NON-INFRINGEMENT, ABSENCE OF LATENT OR OTHER DEFECTS,
     ACCURACY, OR THE PRESENCE OR ABSENCE OF ERRORS, WHETHER OR NOT
     KNOWN OR DISCOVERABLE. WHERE DISCLAIMERS OF WARRANTIES ARE NOT
     ALLOWED IN FULL OR IN PART, THIS DISCLAIMER MAY NOT APPLY TO YOU.

  b. TO THE EXTENT POSSIBLE, IN NO EVENT WILL THE LICENSOR BE LIABLE
     TO YOU ON ANY LEGAL THEORY (INCLUDING, WITHOUT LIMITATION,
     NEGLIGENCE) OR OTHERWISE FOR ANY DIRECT, SPECIAL, INDIRECT,
     INCIDENTAL, CONSEQUENTIAL, PUNITIVE, EXEMPLARY, OR OTHER LOSSES,
     COSTS, EXPENSES, OR DAMAGES ARISING OUT OF THIS PUBLIC LICENSE OR
     USE OF THE LICENSED MATERIAL, EVEN IF THE LICENSOR HAS BEEN
     ADVISED OF THE POSSIBILITY OF SUCH LOSSES, COSTS, EXPENSES, OR
     DAMAGES. WHERE A LIMITATION OF LIABILITY IS NOT ALLOWED IN FULL OR
     IN PART, THIS LIMITATION MAY NOT APPLY TO YOU.

  c. The disclaimer of warranties and limitation of liability provided
     above shall be interpreted in a manner that, to the extent
     possible, most closely approximates an absolute disclaimer and
     waiver of all liability.


Section 6 -- Term and Termination.

  a. This Public License applies for the term of the Copyright and
     Similar Rights licensed here. However, if You fail to comply with
     this Public License, then Your rights under this Public License
     terminate automatically.

  b. Where Your right to use the Licensed Material has terminated under
     Section 6(a), it reinstates:

       1. automatically as of the date the violation is cured, provided
          it is cured within 30 days of Your discovery of the
          violation; or

       2. upon express reinstatement by the Licensor.

     For the avoidance of doubt, this Section 6(b) does not affect any
     right the Licensor may have to seek remedies for Your violations
     of this Public License.

  c. For the avoidance of doubt, the Licensor may also offer the
     Licensed Material under separate terms or conditions or stop
     distributing the Licensed Material at any time; however, doing so
     will not terminate this Public License.

  d. Sections 1, 5, 6, 7, and 8 survive termination of this Public
     License.


Section 7 -- Other Terms and Conditions.

  a. The Licensor shall not be bound by any additional or different
     terms or conditions communicated by You unless expressly agreed.

  b. Any arrangements, understandings, or agreements regarding the
     Licensed Material not stated herein are separate from and
     independent of the terms and conditions of this Public License.


Section 8 -- Interpretation.

  a. For the avoidance of doubt, this Public License does not, and
     shall not be interpreted to, reduce, limit, restrict, or impose
     conditions on any use of the Licensed Material that could lawfully
     be made without permission under this Public License.

  b. To the extent possible, if any provision of this Public License is
     deemed unenforceable, it shall be automatically reformed to the
     minimum extent necessary to make it enforceable. If the provision
     cannot be reformed, it shall be severed from this Public License
     without affecting the enforceability of the remaining terms and
     conditions.

  c. No term or condition of this Public License will be waived and no
     failure to comply consented to unless expressly agreed to by the
     Licensor.

  d. Nothing in this Public License constitutes or may be interpreted
     as a limitation upon, or waiver of, any privileges and immunities
     that apply to the Licensor or You, including from the legal
     processes of any jurisdiction or authority.


=======================================================================

Creative Commons is not a party to its public licenses.
Notwithstanding, Creative Commons may elect to apply one of its public
licenses to material it publishes and in those instances will be
considered the "Licensor." Except for the limited purpose of indicating
that material is shared under a Creative Commons public license or as
otherwise permitted by the Creative Commons policies published at
creativecommons.org/policies, Creative Commons does not authorize the
use of the trademark "Creative Commons" or any other trademark or logo
of Creative Commons without its prior written consent including,
without limitation, in connection with any unauthorized modifications
to any of its public licenses or any other arrangements,
understandings, or agreements concerning use of licensed material. For
the avoidance of doubt, this paragraph does not form part of the public
licenses.

Creative Commons may be contacted at creativecommons.org.

---
# Source: malformed-metadata.md
---
```jsx {expectedErrors: {'react-compiler': 'invalid'}}
import {useState} from 'react';
function Counter() {
  const [count, setCount] = useState(0);
  setCount(count + 1);
  return <div>{count}</div>;
}
```

---
# Source: suppressed-error.md
---
```jsx {expectedErrors: {'react-compiler': [4]}}
import {useState} from 'react';
function Counter() {
  const [count, setCount] = useState(0);
  setCount(count + 1);
  return <div>{count}</div>;
}
```

---
# Source: mixed-language.md
---
```bash
setCount()
```

```txt
import {useState} from 'react';
```

---
# Source: stale-expected-error.md
---
```jsx {expectedErrors: {'react-compiler': [3]}}
function Hello() {
  return <h1>Hello</h1>;
}
```

---
# Source: basic-error.md
---
```jsx
import {useState} from 'react';
function Counter() {
  const [count, setCount] = useState(0);
  setCount(count + 1);
  return <div>{count}</div>;
}
```

---
# Source: duplicate-metadata.md
---
```jsx title="Counter" {expectedErrors: {'react-compiler': [99]}} {expectedErrors: {'react-compiler': [2]}}
import {useState} from 'react';
function Counter() {
  const [count, setCount] = useState(0);
  setCount(count + 1);
  return <div>{count}</div>;
}
```

---
# Source: CONTRIBUTING.md
---
# Contributing

Thank you for your interest in contributing to the React Docs!

## Code of Conduct

Facebook has adopted a Code of Conduct that we expect project
participants to adhere to. Please [read the full text](https://code.facebook.com/codeofconduct)
so that you can understand what actions will and will not be tolerated.

## Technical Writing Tips

This is a [good summary](https://medium.com/@kvosswinkel/coding-like-a-journalist-ee52360a16bc) for things to keep in mind when writing technical docs.

## Guidelines for Text

**Different sections intentionally have different styles.**

The documentation is divided into sections to cater to different learning styles and use cases. When editing an article, try to match the surrounding text in tone and style. When creating a new article, try to match the tone of the other articles in the same section. Learn about the motivation behind each section below.

**[Learn React](https://react.dev/learn)** is designed to introduce fundamental concepts in a step-by-step way. Each individual article in Learn React builds on the knowledge from the previous ones, so make sure not to add any "cyclical dependencies" between them. It is important that the reader can start with the first article and work their way to the last Learn React article without ever having to "look ahead" for a definition. This explains some ordering choices (e.g. that state is explained before events, or that "thinking in React" doesn't use refs). Learn React also serves as a reference manual for React concepts, so it is important to be very strict about their definitions and relationships between them.

**[API Reference](https://react.dev/reference/react)** is organized by APIs rather than concepts. It is intended to be exhaustive. Any corner cases or recommendations that were skipped for brevity in Learn React should be mentioned in the reference documentation for the corresponding APIs.

**Try to follow your own instructions.**

When writing step-by-step instructions (e.g. how to install something), try to forget everything you know about the topic, and actually follow the instructions you wrote, a single step at time. Often you will discover that there is implicit knowledge that you forgot to mention, or that there are missing or out-of-order steps in the instructions. Bonus points for getting *somebody else* to follow the steps and watching what they struggle with. Often it would be something very simple that you have not anticipated.

## Guidelines for Code Examples

### Syntax

#### Prefer JSX to `createElement`.

Ignore this if you're specifically describing `createElement`.

#### Use `const` where possible, otherwise `let`. Don't use `var`.

Ignore this if you're specifically writing about ES5.

#### Don't use ES6 features when equivalent ES5 features have no downsides.

Remember that ES6 is still new to a lot of people. While we use it in many places (`const` / `let`, classes, arrow functions), if the equivalent ES5 code is just as straightforward and readable, consider using it.

In particular, you should prefer named `function` declarations over `const myFunction = () => ...` arrows for top-level functions. However, you *should* use arrow functions where they provide a tangible improvement (such as preserving `this` context inside a component). Consider both sides of the tradeoff when deciding whether to use a new feature.

#### Don't use features that aren't standardized yet.

For example, **don't** write this:

```js
class MyComponent extends React.Component {
  state = {value: ''};
  handleChange = (e) => {
    this.setState({value: e.target.value});
  };
}
```

Instead, **do** write this:

```js
class MyComponent extends React.Component {
  constructor(props) {
    super(props);
    this.handleChange = this.handleChange.bind(this);
    this.state = {value: ''};
  }
  handleChange(e) {
    this.setState({value: e.target.value});
  }
}
```

Ignore this rule if you're specifically describing an experimental proposal. Make sure to mention its experimental nature in the code and in the surrounding text.

### Style

- Use semicolons.
- No space between function names and parens (`method() {}` not `method () {}`).
- When in doubt, use the default style favored by [Prettier](https://prettier.io/playground/).
- Always capitalize React concepts such as Hooks, Effects, and Transitions.

### Highlighting

Use `js` as the highlighting language in Markdown code blocks:

````
```js
// code
```
````

Sometimes you'll see blocks with numbers.  
They tell the website to highlight specific lines.

You can highlight a single line:

````
```js {2}
function hello() {
  // this line will get highlighted
}
```
````

A range of lines:

````
```js {2-4}
function hello() {
  // these lines
  // will get
  // highlighted
}
```
````

Or even multiple ranges:

````
```js {2-4,6}
function hello() {
  // these lines
  // will get
  // highlighted
  console.log('hello');
  // also this one
  console.log('there');
}
```
````

Be mindful that if you move some code in an example with highlighting, you also need to update the highlighting.

Don't be afraid to often use highlighting! It is very valuable when you need to focus the reader's attention on a particular detail that's easy to miss.

---
# Source: README.md
---
# [React 中文文档](https://zh-hans.react.dev/)

此仓库包含 [React 中文文档](https://zh-hans.react.dev/) 的文档及源码，并由官方实时同步。

## 参与贡献

目前，大部分的翻译工作都已经完成。现在主要工作是同步和完善已有翻译。

**参与贡献前，请仔细阅读 [Wiki](https://github.com/reactjs/zh-hans.react.dev/wiki) ，并遵循相关指南。**

主要关注下面的：
- **[React 中文文档译文规范](https://github.com/reactjs/zh-hans.react.dev/wiki/React-Translation-Guide)**。
- **[词汇表](https://github.com/reactjs/zh-hans.react.dev/wiki/The-Glossary-Sheet)**

翻译问题直接提交 pr 修改即可，其他问题在 issue 提出来进行讨论。

---

# react.dev

This repo contains the source code and documentation powering [react.dev](https://react.dev/).

## Getting started

### Prerequisites

1. Git
1. Node: any version starting with v16.8.0 or greater
1. Yarn: See [Yarn website for installation instructions](https://yarnpkg.com/lang/en/docs/install/)
1. A fork of the repo (for any contributions)
1. A clone of the [react.dev repo](https://github.com/reactjs/react.dev) on your local machine

### Installation

1. `cd react.dev` to go into the project root
3. `yarn` to install the website's npm dependencies

### Running locally

1. `yarn dev` to start the development server (powered by [Next.js](https://nextjs.org/))
1. `open http://localhost:3000` to open the site in your favorite browser

## Contributing

### Guidelines

The documentation is divided into several sections with a different tone and purpose. If you plan to write more than a few sentences, you might find it helpful to get familiar with the [contributing guidelines](https://github.com/reactjs/react.dev/blob/main/CONTRIBUTING.md#guidelines-for-text) for the appropriate sections.

### Create a branch

1. `git checkout main` from any folder in your local `react.dev` repository
1. `git pull origin main` to ensure you have the latest main code
1. `git checkout -b the-name-of-my-branch` (replacing `the-name-of-my-branch` with a suitable name) to create a branch

### Make the change

1. Follow the ["Running locally"](#running-locally) instructions
1. Save the files and check in the browser
  1. Changes to React components in `src` will hot-reload
  1. Changes to markdown files in `content` will hot-reload
  1. If working with plugins, you may need to remove the `.cache` directory and restart the server

### Test the change

1. If possible, test any visual changes in all latest versions of common browsers, on both desktop and mobile.
2. Run `yarn check-all`. (This will run Prettier, ESLint and validate types.)

### Push it

1. `git add -A && git commit -m "My message"` (replacing `My message` with a commit message, such as `Fix header logo on Android`) to stage and commit your changes
1. `git push my-fork-name the-name-of-my-branch`
1. Go to the [react.dev repo](https://github.com/reactjs/react.dev) and you should see recently pushed branches.
1. Follow GitHub's instructions.
1. If possible, include screenshots of visual changes. A preview build is triggered after your changes are pushed to GitHub.

## Translation

If you are interested in translating `react.dev`, please see the current translation efforts [here](https://github.com/reactjs/react.dev/issues/4135).

## License
Content submitted to [react.dev](https://react.dev/) is CC-BY-4.0 licensed, as found in the [LICENSE-DOCS.md](https://github.com/reactjs/react.dev/blob/main/LICENSE-DOCS.md) file.

---
# Source: index.md
---
---
title: React Blog
---

<Intro>

这个博客是 React 团队更新的官方来源。任何重要的内容，包括发布说明或弃用通知，都会首先在这里发布。

你也可以在 Bluesky 上关注 [@react.dev](https://bsky.app/profile/react.dev)，或者在 Twitter 上关注 [@reactjs](https://twitter.com/reactjs)。不过只要你阅读这个博客，就不会错过任何重要内容。
</Intro>

<div className="sm:-mx-5 flex flex-col gap-5 mt-12">

<BlogCard title="React 服务器组件中的拒绝服务和源代码泄露" date="2025 年 12 月 11 日" url="/blog/2025/12/11/denial-of-service-and-source-code-exposure-in-react-server-components">

安全研究员在尝试利用上周公布的严重漏洞补丁时，又发现了 React 服务器组件中的两个漏洞并进行披露……

</BlogCard>

<BlogCard title="服务器组件中的严重安全漏洞" date="2025 年 12 月 3 日" url="/blog/2025/12/03/critical-security-vulnerability-in-react-server-components">

服务器组件中存在未经身份验证的远程代码执行漏洞。版本 19.0.1、19.1.2 和 19.2.1 已经修复该漏洞。我们建议立即升级。

</BlogCard>

<BlogCard title="回顾 React Conf 2025" date="2025 年 10 月 16 日" url="/blog/2025/10/16/react-conf-2025-recap">

上周我们举办了 React Conf 2025，在本文中，我们总结了会议的演讲和公告……

</BlogCard>

<BlogCard title="React Compiler v1.0" date="October 7, 2025" url="/blog/2025/10/07/react-compiler-1">

我们今天将发布 React Compiler 的第一个稳定发布版，以及 linting 和工具改进，使采用更加容易。

</BlogCard>

<BlogCard title="Introducing the React Foundation" date="October 7, 2025" url="/blog/2025/10/07/introducing-the-react-foundation">

Today, we're announcing our plans to create the React Foundation and a new technical governance structure ...

</BlogCard>

<BlogCard title="React 19.2" date="October 1, 2025" url="/blog/2025/10/01/react-19-2">

React 19.2 adds new features like Activity, React Performance Tracks, useEffectEvent, and more. In this post ...

</BlogCard>

<BlogCard title="React Labs: View Transitions, Activity, and more" date="April 23, 2025" url="/blog/2025/04/23/react-labs-view-transitions-activity-and-more">

In React Labs posts, we write about projects in active research and development. In this post, we're sharing two new experimental features that are ready to try today, and sharing other areas we're working on now ...

</BlogCard>

<BlogCard title="逐步淘汰 Create React App" date="February 14, 2025" url="/blog/2025/02/14/sunsetting-create-react-app">

今日起，我们将正式弃用 Create React App 作为新应用的推荐工具，并建议现有应用迁移至框架或构建工具（如 Vite、Parcel 和 RSBuild）。我们还提供了相关文档用于这些情况：你的项目不适合使用框架、你想要构建自己的框架，或者只是想通过从零开始构建一个 React 应用来了解 React 的工作原理等等……

</BlogCard>

<BlogCard title="React v19 " date="December 5, 2024" url="/blog/2024/12/05/react-19">

在我们的 React 19 升级指南中, 我们分享了将应用程序升级到 React 19 的分步说明。在这篇文章中，我们将概述 React 19 的新特性，以及如何使用它们……

</BlogCard>

<BlogCard title="React Compiler 发布 Beta 版本" date="October 21, 2024" url="/blog/2024/10/21/react-compiler-beta-release">

我们在 React Conf 2024 上宣布了 React Compiler 的实验性版本。从那时起我们已经取得了很多进展，在这篇文章中，我们将分享 React Compiler 下一步要做的事情……

</BlogCard>

<BlogCard title="回顾 React Conf 2024" date="May 22, 2024" url="/blog/2024/05/22/react-conf-2024-recap">

上周我们在内华达州亨德森举办了为期两天的 React Conf 2024 大会，有 700 多名与会者亲临现场，讨论 UI 工程领域的最新进展。这是我们自 2019 年以来首次举办线下会议，我们很高兴能够再次将社区团结在一起……

</BlogCard>

<BlogCard title="React 19 升级指南" date="April 25, 2024" url="/blog/2024/04/25/react-19-upgrade-guide">

React 19 中新增的改进需要一些破坏性变更，但我们已经尽力让升级过程尽可能平滑，我们预计这些变更不会影响大多数应用。在这篇文章中，我们将指导你完成将库升级到 React 19 的步骤……

</BlogCard>

<BlogCard title="React Labs：我们正在努力的方向——2024 年 2 月" date="February 15, 2024" url="/blog/2024/02/15/react-labs-what-we-have-been-working-on-february-2024">

在 React Labs 的文章中，我们讲述了正在进行研究与开发的项目。自从上次更新以来，我们在 React 编译器、新功能和 React 19 方面取得了重大进展，除此之外我们还想要分享我们从中学到的东西。

</BlogCard>

<BlogCard title="React Canaries：在 Meta 之外逐步推出新功能" date="May 3, 2023" url="/blog/2023/05/03/react-canaries">

在过去，React 的新功能将仅在 Meta 中使用，然后才会在开源版本中发布。我们希望为 React 社区提供一种选择，使他们能够在新功能设计接近最终状态时立即采用这些功能——类似于 Meta 内部使用 React 的方式。我们正在推出一个新的官方支持的 Canary 发布渠道。它允许像框架这样的精选设置，对单个 React 功能的采用与 React 发布计划分离开。

</BlogCard>

<BlogCard title="React Labs：我们正在努力的方向——2023 年 3 月" date="2023 年 3 月 22 日" url="/blog/2023/03/22/react-labs-what-we-have-been-working-on-march-2023">

在 React Labs 的文章中，我们讲述了正在进行研究和开发的项目。自上次更新以来，我们在 React 服务器组件、资产加载、优化编译器、离屏渲染和过渡追踪方面取得了重要进展，并希望分享我们所学到的知识。

</BlogCard>


<BlogCard title="介绍 react.dev" date="2023 年 3 月 16 日" url="/blog/2023/03/16/introducing-react-dev">

今天，我们非常高兴推出 react.dev，React 及其文档的新家。在本文中，我们想带你参观新网站。

</BlogCard>


<BlogCard title="React Labs：我们正在努力的方向——2022 年 6 月" date="2022 年 6 月 15 日" url="/blog/2022/06/15/react-labs-what-we-have-been-working-on-june-2022">
React 18 经过多年的努力才得以问世，它为 React 团队带来了宝贵的经验教训。它的发布是多年的研究和探索的结果。其中一些路径是成功的，但更多的是死胡同，但是也带来了新的见解。我们学到的一个教训是，对社区来说，在等待新功能时没有了解我们正在探索的路径是令人沮丧的。
</BlogCard>

<BlogCard title="React v18.0" date="2022 年 3 月 29 日" url="/blog/2022/03/29/react-v18">
React 18 现已在 npm 上发布！在我们上一篇文章中，我们分享了应用程序升级到 React 18 的逐步说明。在本文中，我们将概述 React 18 的新功能，以及它对未来的意义……
</BlogCard>

<BlogCard title="如何升级到 React 18" date="2022 年 3 月 8 日" url="/blog/2022/03/08/react-18-upgrade-guide">
正如我们在文章中所分享的那样，React 18 引入了由我们的新并发渲染器提供支持的功能，并采用了逐步采用策略，以适用于现有应用程序。在本文中，我们将指导完成升级到 React 18 的步骤……
</BlogCard>

<BlogCard title="回顾 React Conf 2021" date="2021 年 12 月 17 日" url="/blog/2021/12/17/react-conf-2021-recap">
上周，我们举办了第六届 React Conf。在以往的几年中，我们在 React Conf 的舞台上发布了行业改变的信息，如 React Native 和 React Hooks。今年，我们从发布 React 18 和逐步采用并发功能开始，分享了我们对 React 的多平台愿景……
</BlogCard>

<BlogCard title="React 18 的有关计划" date="2021 年 6 月 8 日" url="/blog/2021/06/08/the-plan-for-react-18">
React 团队很高兴分享一些更新：

- 我们已经开始了 React 18 的开发工作，这将是我们的下一个主要版本。
- 我们创建了一个工作组，为社区逐步采用 React 18 的新功能做准备。
- 我们发布了 React 18 Alpha，以便库作者可以尝试并提供反馈……
</BlogCard>

<BlogCard title="介绍零打包大小的 React 服务器组件" date="2020 年 12 月 21 日" url="/blog/2020/12/21/data-fetching-with-react-server-components">
2020 年是漫长的一年。随着它的结束，我们想在节日里分享一份特别的更新，介绍我们对零打包大小的 React 服务器组件的研究。为了介绍 React 服务器组件，我们准备了一次演讲和演示。如果你愿意，在假期期间或新年工作重新开始后查看它们……
</BlogCard>

</div>

---

### 所有的发布笔记 {/*all-release-notes*/}

并不是每个 React 版本都值得拥有专属博客文章，但是你可以在 React 仓库的 `CHANGELOG.md` 或 [发布页面](https://github.com/facebook/react/releases) 中找到每个版本的详细变更。

---

### 更早的文章 {/*older-posts*/}

你可以在 [这里](https://reactjs.org/blog/all.html) 查看更早的文章。

<div className="h-12"></div>

---
# Source: react-compiler-beta-release.md
---
---
title: "React 编译器发布 Beta 版本"
author: Lauren Tan
date: 2024/10/21
description: 在 React Conf 2024 上，我们宣布了 React 编译器的实验性版本，这是一个构建时工具，可通过自动记忆化来优化 React 应用程序。在这篇文章中，我们想分享开源的下一步发展，以及我们在编译器方面的进展。

---

October 21, 2024 by [Lauren Tan](https://twitter.com/potetotes).

---

<Note>

### React 编译器现在处于稳定版本！{/*react-compiler-is-now-in-rc*/}

有关详细信息，请参阅 [稳定版博客文章](/blog/2025/10/07/react-compiler-1)。

</Note>

<Intro>

React 团队很高兴分享新的内容：

</Intro>

1. 今天我们发布了 React 编译器的 Beta 版本，以便早期采用者和库维护者可以尝试它并提供反馈。
2. 我们通过可选的 `react-compiler-runtime` 包来正式支持在 React 17+ 上的应用程序使用 React 编译器。
3. 我们正在开放 [React 编译器工作组](https://github.com/reactwg/react-compiler) 的公共成员资格，为社区逐步采用该编译器做好准备。

---

在 [React Conf 2024](/blog/2024/05/22/react-conf-2024-recap) 上，我们宣布了 React 编译器的实验版本，这是一个构建时工具，可通过自动记忆化来优化 React 应用程序。[你可以在这里找到对 React 编译器的介绍](/learn/react-compiler)。

自第一个版本以来，我们修复了 React 社区报告的许多错误, 收到了多个高质量的错误修复和对编译器的贡献 [^1]，使编译器能够更好地适应多种 JavaScript 模式，并继续在 Meta 上更广泛地推出编译器。

在这篇文章中，我们想分享 React 编译器的下一步发展。

## 从今天起开始尝试 React 编译器的 Beta 版本吧 {/*try-react-compiler-beta-today*/}

在 [React India 2024](https://www.youtube.com/watch?v=qd5yk2gxbtg) 上，我们分享了 React 编译器的更新。今天，我们很高兴地宣布 React 编译器和 ESLint 插件的新 Beta 版本。新的测试版使用 `@beta` 标签发布到 npm。

使用下面的方式来安装 React 编译器的 Beta 版本：

<TerminalBlock>
npm install -D babel-plugin-react-compiler@beta eslint-plugin-react-compiler@beta
</TerminalBlock>

或者使用 Yarn：

<TerminalBlock>
yarn add -D babel-plugin-react-compiler@beta eslint-plugin-react-compiler@beta
</TerminalBlock>

你可以在此处观看 [Sathya Gunasekaran](https://twitter.com/_gsathya) 在 React India 的演讲：

<YouTubeIframe src="https://www.youtube.com/embed/qd5yk2gxbtg" />

## 从今天起我们建议大家使用 React 编译器的 linter {/*we-recommend-everyone-use-the-react-compiler-linter-today*/}

React 编译器的 ESLint 插件可帮助开发人员主动识别和纠正对于 [React 规则](/reference/rules) 的违规行为。**我们强烈建议大家从今天开始就使用 linter**。linter 不需要安装编译器，因此即使你还没有准备好尝试编译器，也可以独立使用它。

安装 linter 只需要执行：

<TerminalBlock>
npm install -D eslint-plugin-react-compiler@beta
</TerminalBlock>

或者使用 Yarn：

<TerminalBlock>
yarn add -D eslint-plugin-react-compiler@beta
</TerminalBlock>

安装后你可以通过[将其添加到 ESLint 配置](/learn/react-compiler/installation#eslint-integration) 来启用 linter。使用 linter 有助于发现破坏 React 规则的地方，从而在编译器完全发布后更容易采用它。

## 向后兼容性 {/*backwards-compatibility*/}

React 编译器生成的代码依赖于 React 19 中添加的运行时 API，但我们后来添加了对 React 17 和 18 的支持。如果你还没有使用 React 19，在 Beta 版本中可以通过在 compiler 配置中设置 `target` 来使用 React 编译器，并添加 `react-compiler-runtime` 作为依赖项。[你可以在这里找到相关文档](/reference/react-compiler/configuration#react-17-18)。

## 在库中使用 React 编译器 {/*using-react-compiler-in-libraries*/}

我们的初始版本侧重于识别在应用程序中使用编译器的主要问题。从那时起我们得到了很好的反馈，并对编译器进行了实质性改进。我们现在已准备好接受社区的广泛反馈，并让库作者尝试编译器以提高性能和维护体验。

React 编译器还可以用来编译库。由于 React 编译器需要在代码转换之前的源码上运行，因此应用程序无法使用 pipeline 来编译所使用的库。因此我们建议库维护人员使用编译器独立编译和测试他们的库，并将编译后的代码发布到 npm。

由于库的代码是预编译的，因此用户无需启用 Compiler 即可从编译器的自动记忆化中受益。如果库的 target 不是 React 19，请指定一个最小的 [`target` 并且将 `react-compiler-runtime` 添加为直接依赖](#using-react-compiler-with-react-17-or-18)。这个运行时包将根据应用程序的版本使用正确的 API 实现，并在必要时填充缺失的 API。

[你可以在此处找到更多相关文档。](/reference/react-compiler/compiling-libraries)

## 向所有人开放 React 编译器工作组 {/*opening-up-react-compiler-working-group-to-everyone*/}

我们之前在 React Conf 上宣布成立邀请制的 [React 编译器工作组](https://github.com/reactwg/react-compiler) 以提供反馈、提出问题并就编译器的实验版本进行协作。

从今天开始，随着 React 编译器的测试版发布，我们向所有人开放工作组成员资格。React 编译器工作组的目标是为生态系统做好准备，以便现有应用程序和库顺利、逐步采用 React 编译器。请继续在 [React 仓库中](https://github.com/facebook/react) 提交错误报告，但是在 [工作组论坛](https://github.com/reactwg/react-compiler/discussions) 中留下反馈、提出问题或分享想法。

核心团队还将使用工作组论坛来分享我们的研究成果。随着稳定版本的临近，任何重要信息也将发布在该论坛上。

## React 编译器在 Meta {/*react-compiler-at-meta*/}

在 [React Conf](/blog/2024/05/22/react-conf-2024-recap) 上，我们分享了在 Quest Store 和 Instagram 上成功推出编译器的消息。从那时起，我们在包括 [Facebook](https://www.facebook.com) 和 [Threads](https://www.threads.net) 的几个主要 Web 应用程序中部署了 React 编译器。这意味着如果你最近使用过这些应用程序中的任何一个，你的体验可能是由编译器提供支持的。我们能够在包含超过 100,000 个 React 组件的 monorepo 中将这些应用程序加载到编译器上，只需进行少量代码更改。

我们发现所有这些应用程序的性能都有显着提高。随着编译器的推出，我们将继续看到 [之前在 ReactConf 上分享的成功经验](https://youtu.be/lyEKhv8-3n0?t=3223) 的结果。多年来 Meta 工程师和 React 专家对这些应用程序经过了大量手工调整和优化，因此即使是几个百分点的改进对我们来说也是一个巨大的胜利。

我们还预计 React 编译器会提高开发人员的生产力。为了衡量这一点，我们与 Meta[^2] 的数据科学合作伙伴合作，将手动记忆化对生产力的影响进行了彻底的统计分析。在 Meta 推出编译器之前，我们发现只有大约 8% 的 React PR 使用手动记忆化，并且这些 PR 的编写时间比其他 PR 增加了 31-46%[^3]。这证实了我们的直觉，即手动记忆化会带来认知开销，我们预计 React 编译器将带来更高效的代码创作和审查。值得注意的是，React 编译器还确保默认情况下记忆 **所有** 代码，而不仅仅是（在我们的例子中）开发人员明确记忆化的 8%。

## 稳定版本路线图 {/*roadmap-to-stable*/}

**这不是最终的路线图，可能会发生变化。**

我们打算在 Beta 版本发布后不久发布编译器的候选版本，届时大多数遵循 React 规则的应用程序和库已被证明可以与编译器良好配合。经过一段时间的社区最终反馈后，我们计划为编译器提供稳定版本。稳定版本将标志着 React 新基础的开始，强烈建议所有应用程序和库使用编译器和 ESLint 插件。

* ✅ 实验性（Experimental）：在 React Conf 2024 上发布，主要是为了获得早期采用者的反馈。 
* ✅ 公开测试版（Public Beta）：现已推出，以获取更广泛社区的反馈。
* 🚧 候选发布版（RC）： React 编译器适用于大多数遵循规则的应用程序和库，不会引入任何问题。
* 🚧 普遍适用（General Availability）：在社区的最终反馈期结束后。

这些版本还包括编译器的 ESLint 插件，该插件提供编译器静态分析的诊断信息。我们计划将现有的 eslint-plugin-react-hooks 插件与编译器的 ESLint 插件结合起来，因此最终只需要安装一个插件。

稳定后，我们计划在少改动甚至不改动产品代码的情况下添加更多对编译器的优化和改进，这包括了对自动记忆化的持续优化和新的整体优化。升级到每个新版本的编译器都是为了更加简单明了，每次升级都将继续提高性能并更好地处理不同的 JavaScript 和 React 模式。

在整个过程中，我们还计划为 React 制作一个 IDE 扩展原型。研究还处于早期阶段，因此我们希望能够在未来的 React Labs 博客文章中与你分享更多我们的发现。

---

感谢 [Sathya Gunasekaran](https://twitter.com/_gsathya)、[Joe Savona](https://twitter.com/en_JS)、[Ricky Hanlon](https://twitter.com/rickhanlonii)、[Alex Taylor](https://github.com/alexmckenley)、[Jason Bonta](https://twitter.com/someextent) 和 [Eli White](https://twitter.com/Eli_White) 对本篇博客的审阅和编辑。

---

[^1]: 感谢 [@nikeee](https://github.com/facebook/react/pulls?q=is%3Apr+author%3Anikeee)、[@henryqdineen](https://github.com/facebook/react/pulls?q=is%3Apr+author%3Ahenryqdineen)、[@TrickyPi](https://github.com/facebook/react/pulls?q=is%3Apr+author%3ATrickyPi) 以及其他为编译器做出贡献的人。

[^2]: 感谢 [Vaishali Garg](https://www.linkedin.com/in/vaishaligarg09) 在 Meta 领导这项关于 React 编译器的研究，并审阅这篇文章。

[^3]: 在平衡了作者任期、代码 diff 长度和复杂性以及其他潜在的混杂因素之后。
---
# Source: react-19-upgrade-guide.md
---
---
title: "React 19 Upgrade Guide"
author: Ricky Hanlon
date: 2024/04/25
description: The improvements added to React 19 require some breaking changes, but we've worked to make the upgrade as smooth as possible and we don't expect the changes to impact most apps. In this post, we will guide you through the steps for upgrading apps and libraries to React 19.
---

April 25, 2024 by [Ricky Hanlon](https://twitter.com/rickhanlonii)

---


<Intro>

The improvements added to React 19 require some breaking changes, but we've worked to make the upgrade as smooth as possible, and we don't expect the changes to impact most apps.

</Intro>

<Note>

#### React 18.3 has also been published {/*react-18-3*/}

To help make the upgrade to React 19 easier, we've published a `react@18.3` release that is identical to 18.2 but adds warnings for deprecated APIs and other changes that are needed for React 19. 

We recommend upgrading to React 18.3 first to help identify any issues before upgrading to React 19.

For a list of changes in 18.3 see the [Release Notes](https://github.com/facebook/react/blob/main/CHANGELOG.md#1830-april-25-2024).

</Note>

In this post, we will guide you through the steps for upgrading to React 19:

- [Installing](#installing)
- [Codemods](#codemods)
- [Breaking changes](#breaking-changes)
- [New deprecations](#new-deprecations)
- [Notable changes](#notable-changes)
- [TypeScript changes](#typescript-changes)
- [Changelog](#changelog)

If you'd like to help us test React 19, follow the steps in this upgrade guide and [report any issues](https://github.com/facebook/react/issues/new?assignees=&labels=React+19&projects=&template=19.md&title=%5BReact+19%5D) you encounter. For a list of new features added to React 19, see the [React 19 release post](/blog/2024/12/05/react-19).

---
## Installing {/*installing*/}

<Note>

#### New JSX Transform is now required {/*new-jsx-transform-is-now-required*/}

We introduced a [new JSX transform](https://legacy.reactjs.org/blog/2020/09/22/introducing-the-new-jsx-transform.html) in 2020 to improve bundle size and use JSX without importing React. In React 19, we're adding additional improvements like using ref as a prop and JSX speed improvements that require the new transform.

If the new transform is not enabled, you will see this warning:

<ConsoleBlockMulti>

<ConsoleLogLine level="error">

Your app (or one of its dependencies) is using an outdated JSX transform. Update to the modern JSX transform for faster performance: https://react.dev/link/new-jsx-transform

</ConsoleLogLine>

</ConsoleBlockMulti>


We expect most apps will not be affected since the transform is enabled in most environments already. For manual instructions on how to upgrade, please see the [announcement post](https://legacy.reactjs.org/blog/2020/09/22/introducing-the-new-jsx-transform.html).

</Note>


To install the latest version of React and React DOM:

```bash
npm install --save-exact react@^19.0.0 react-dom@^19.0.0
```

Or, if you're using Yarn:

```bash
yarn add --exact react@^19.0.0 react-dom@^19.0.0
```

If you're using TypeScript, you also need to update the types.
```bash
npm install --save-exact @types/react@^19.0.0 @types/react-dom@^19.0.0
```

Or, if you're using Yarn:
```bash
yarn add --exact @types/react@^19.0.0 @types/react-dom@^19.0.0
```

We're also including a codemod for the most common replacements. See [TypeScript changes](#typescript-changes) below.

## Codemods {/*codemods*/}

To help with the upgrade, we've worked with the team at [codemod.com](https://codemod.com) to publish codemods that will automatically update your code to many of the new APIs and patterns in React 19.

All codemods are available in the [`react-codemod` repo](https://github.com/reactjs/react-codemod) and the Codemod team have joined in helping maintain the codemods. To run these codemods, we recommend using the `codemod` command instead of the `react-codemod` because it runs faster, handles more complex code migrations, and provides better support for TypeScript.


<Note>

#### Run all React 19 codemods {/*run-all-react-19-codemods*/}

Run all codemods listed in this guide with the React 19 `codemod` recipe:

```bash
npx codemod@latest react/19/migration-recipe
```

This will run the following codemods from `react-codemod`:
- [`replace-reactdom-render`](https://github.com/reactjs/react-codemod?tab=readme-ov-file#replace-reactdom-render) 
- [`replace-string-ref`](https://github.com/reactjs/react-codemod?tab=readme-ov-file#replace-string-ref)
- [`replace-act-import`](https://github.com/reactjs/react-codemod?tab=readme-ov-file#replace-act-import)
- [`replace-use-form-state`](https://github.com/reactjs/react-codemod?tab=readme-ov-file#replace-use-form-state) 
- [`prop-types-typescript`](https://github.com/reactjs/react-codemod#react-proptypes-to-prop-types)

This does not include the TypeScript changes. See [TypeScript changes](#typescript-changes) below.

</Note>

Changes that include a codemod include the command below. 

For a list of all available codemods, see the [`react-codemod` repo](https://github.com/reactjs/react-codemod).

## Breaking changes {/*breaking-changes*/}

### Errors in render are not re-thrown {/*errors-in-render-are-not-re-thrown*/}

In previous versions of React, errors thrown during render were caught and rethrown. In DEV, we would also log to `console.error`, resulting in duplicate error logs. 

In React 19, we've [improved how errors are handled](/blog/2024/04/25/react-19#error-handling) to reduce duplication by not re-throwing:

- **Uncaught Errors**: Errors that are not caught by an Error Boundary are reported to `window.reportError`.
- **Caught Errors**: Errors that are caught by an Error Boundary are reported to `console.error`.

This change should not impact most apps, but if your production error reporting relies on errors being re-thrown, you may need to update your error handling. To support this, we've added new methods to `createRoot` and `hydrateRoot` for custom error handling:

```js [[1, 2, "onUncaughtError"], [2, 5, "onCaughtError"]]
const root = createRoot(container, {
  onUncaughtError: (error, errorInfo) => {
    // ... log error report
  },
  onCaughtError: (error, errorInfo) => {
    // ... log error report
  }
});
```

For more info, see the docs for [`createRoot`](https://react.dev/reference/react-dom/client/createRoot) and [`hydrateRoot`](https://react.dev/reference/react-dom/client/hydrateRoot).


### Removed deprecated React APIs {/*removed-deprecated-react-apis*/}

#### Removed: `propTypes` and `defaultProps` for functions {/*removed-proptypes-and-defaultprops*/}
`PropTypes` were deprecated in [April 2017 (v15.5.0)](https://legacy.reactjs.org/blog/2017/04/07/react-v15.5.0.html#new-deprecation-warnings).

In React 19, we're removing the `propType` checks from the React package, and using them will be silently ignored. If you're using `propTypes`, we recommend migrating to TypeScript or another type-checking solution.

We're also removing `defaultProps` from function components in place of ES6 default parameters. Class components will continue to support `defaultProps` since there is no ES6 alternative.

```js
// Before
import PropTypes from 'prop-types';

function Heading({text}) {
  return <h1>{text}</h1>;
}
Heading.propTypes = {
  text: PropTypes.string,
};
Heading.defaultProps = {
  text: 'Hello, world!',
};
```
```ts
// After
interface Props {
  text?: string;
}
function Heading({text = 'Hello, world!'}: Props) {
  return <h1>{text}</h1>;
}
```

<Note>

Codemod `propTypes` to TypeScript with:

```bash
npx codemod@latest react/prop-types-typescript
```

</Note>

#### Removed: Legacy Context using `contextTypes` and `getChildContext` {/*removed-removing-legacy-context*/}

Legacy Context was deprecated in [October 2018 (v16.6.0)](https://legacy.reactjs.org/blog/2018/10/23/react-v-16-6.html).

Legacy Context was only available in class components using the APIs `contextTypes` and `getChildContext`, and was replaced with `contextType` due to subtle bugs that were easy to miss. In React 19, we're removing Legacy Context to make React slightly smaller and faster.

If you're still using Legacy Context in class components, you'll need to migrate to the new `contextType` API:

```js {5-11,19-21}
// Before
import PropTypes from 'prop-types';

class Parent extends React.Component {
  static childContextTypes = {
    foo: PropTypes.string.isRequired,
  };

  getChildContext() {
    return { foo: 'bar' };
  }

  render() {
    return <Child />;
  }
}

class Child extends React.Component {
  static contextTypes = {
    foo: PropTypes.string.isRequired,
  };

  render() {
    return <div>{this.context.foo}</div>;
  }
}
```

```js {2,7,9,15}
// After
const FooContext = React.createContext();

class Parent extends React.Component {
  render() {
    return (
      <FooContext value='bar'>
        <Child />
      </FooContext>
    );
  }
}

class Child extends React.Component {
  static contextType = FooContext;

  render() {
    return <div>{this.context}</div>;
  }
}
```

#### Removed: string refs {/*removed-string-refs*/}
String refs were deprecated in [March, 2018 (v16.3.0)](https://legacy.reactjs.org/blog/2018/03/27/update-on-async-rendering.html).

Class components supported string refs before being replaced by ref callbacks due to [multiple downsides](https://github.com/facebook/react/issues/1373). In React 19, we're removing string refs to make React simpler and easier to understand.

If you're still using string refs in class components, you'll need to migrate to ref callbacks:

```js {4,8}
// Before
class MyComponent extends React.Component {
  componentDidMount() {
    this.refs.input.focus();
  }

  render() {
    return <input ref='input' />;
  }
}
```

```js {4,8}
// After
class MyComponent extends React.Component {
  componentDidMount() {
    this.input.focus();
  }

  render() {
    return <input ref={input => this.input = input} />;
  }
}
```

<Note>

Codemod string refs with `ref` callbacks:

```bash
npx codemod@latest react/19/replace-string-ref
```

</Note>

#### Removed: Module pattern factories {/*removed-module-pattern-factories*/}
Module pattern factories were deprecated in [August 2019 (v16.9.0)](https://legacy.reactjs.org/blog/2019/08/08/react-v16.9.0.html#deprecating-module-pattern-factories).

This pattern was rarely used and supporting it causes React to be slightly larger and slower than necessary. In React 19, we're removing support for module pattern factories, and you'll need to migrate to regular functions:

```js
// Before
function FactoryComponent() {
  return { render() { return <div />; } }
}
```

```js
// After
function FactoryComponent() {
  return <div />;
}
```

#### Removed: `React.createFactory` {/*removed-createfactory*/}
`createFactory` was deprecated in [February 2020 (v16.13.0)](https://legacy.reactjs.org/blog/2020/02/26/react-v16.13.0.html#deprecating-createfactory).

Using `createFactory` was common before broad support for JSX, but it's rarely used today and can be replaced with JSX. In React 19, we're removing `createFactory` and you'll need to migrate to JSX:

```js
// Before
import { createFactory } from 'react';

const button = createFactory('button');
```

```js
// After
const button = <button />;
```

#### Removed: `react-test-renderer/shallow` {/*removed-react-test-renderer-shallow*/}

In React 18, we updated `react-test-renderer/shallow` to re-export [react-shallow-renderer](https://github.com/enzymejs/react-shallow-renderer). In React 19, we're removing `react-test-render/shallow` to prefer installing the package directly:

```bash
npm install react-shallow-renderer --save-dev
```
```diff
- import ShallowRenderer from 'react-test-renderer/shallow';
+ import ShallowRenderer from 'react-shallow-renderer';
```

<Note>

##### Please reconsider shallow rendering {/*please-reconsider-shallow-rendering*/}

Shallow rendering depends on React internals and can block you from future upgrades. We recommend migrating your tests to [@testing-library/react](https://testing-library.com/docs/react-testing-library/intro/) or [@testing-library/react-native](https://testing-library.com/docs/react-native-testing-library/intro). 

</Note>

### Removed deprecated React DOM APIs {/*removed-deprecated-react-dom-apis*/}

#### Removed: `react-dom/test-utils` {/*removed-react-dom-test-utils*/}

We've moved `act` from `react-dom/test-utils` to the `react` package:

<ConsoleBlockMulti>

<ConsoleLogLine level="error">

`ReactDOMTestUtils.act` is deprecated in favor of `React.act`. Import `act` from `react` instead of `react-dom/test-utils`. See https://react.dev/warnings/react-dom-test-utils for more info.

</ConsoleLogLine>

</ConsoleBlockMulti>

To fix this warning, you can import `act` from `react`:

```diff
- import {act} from 'react-dom/test-utils'
+ import {act} from 'react';
```

All other `test-utils` functions have been removed. These utilities were uncommon, and made it too easy to depend on low level implementation details of your components and React. In React 19, these functions will error when called and their exports will be removed in a future version.

See the [warning page](https://react.dev/warnings/react-dom-test-utils) for alternatives.

<Note>

Codemod `ReactDOMTestUtils.act` to `React.act`:

```bash
npx codemod@latest react/19/replace-act-import
```

</Note>

#### Removed: `ReactDOM.render` {/*removed-reactdom-render*/}

`ReactDOM.render` was deprecated in [March 2022 (v18.0.0)](https://react.dev/blog/2022/03/08/react-18-upgrade-guide). In React 19, we're removing `ReactDOM.render` and you'll need to migrate to using [`ReactDOM.createRoot`](https://react.dev/reference/react-dom/client/createRoot):

```js
// Before
import {render} from 'react-dom';
render(<App />, document.getElementById('root'));

// After
import {createRoot} from 'react-dom/client';
const root = createRoot(document.getElementById('root'));
root.render(<App />);
```

<Note>

Codemod `ReactDOM.render` to `ReactDOMClient.createRoot`:

```bash
npx codemod@latest react/19/replace-reactdom-render
```

</Note>

#### Removed: `ReactDOM.hydrate` {/*removed-reactdom-hydrate*/}

`ReactDOM.hydrate` was deprecated in [March 2022 (v18.0.0)](https://react.dev/blog/2022/03/08/react-18-upgrade-guide). In React 19, we're removing `ReactDOM.hydrate` you'll need to migrate to using [`ReactDOM.hydrateRoot`](https://react.dev/reference/react-dom/client/hydrateRoot),

```js
// Before
import {hydrate} from 'react-dom';
hydrate(<App />, document.getElementById('root'));

// After
import {hydrateRoot} from 'react-dom/client';
hydrateRoot(document.getElementById('root'), <App />);
```

<Note>

Codemod `ReactDOM.hydrate` to `ReactDOMClient.hydrateRoot`:

```bash
npx codemod@latest react/19/replace-reactdom-render
```

</Note>

#### Removed: `unmountComponentAtNode` {/*removed-unmountcomponentatnode*/}

`ReactDOM.unmountComponentAtNode` was deprecated in [March 2022 (v18.0.0)](https://react.dev/blog/2022/03/08/react-18-upgrade-guide). In React 19, you'll need to migrate to using `root.unmount()`.


```js
// Before
unmountComponentAtNode(document.getElementById('root'));

// After
root.unmount();
```

For more see `root.unmount()` for [`createRoot`](https://react.dev/reference/react-dom/client/createRoot#root-unmount) and [`hydrateRoot`](https://react.dev/reference/react-dom/client/hydrateRoot#root-unmount).

<Note>

Codemod `unmountComponentAtNode` to `root.unmount`:

```bash
npx codemod@latest react/19/replace-reactdom-render
```

</Note>

#### Removed: `ReactDOM.findDOMNode` {/*removed-reactdom-finddomnode*/}

`ReactDOM.findDOMNode` was [deprecated in October 2018 (v16.6.0)](https://legacy.reactjs.org/blog/2018/10/23/react-v-16-6.html#deprecations-in-strictmode). 

We're removing `findDOMNode` because it was a legacy escape hatch that was slow to execute, fragile to refactoring, only returned the first child, and broke abstraction levels (see more [here](https://legacy.reactjs.org/docs/strict-mode.html#warning-about-deprecated-finddomnode-usage)). You can replace `ReactDOM.findDOMNode` with [DOM refs](/learn/manipulating-the-dom-with-refs):

```js
// Before
import {findDOMNode} from 'react-dom';

function AutoselectingInput() {
  useEffect(() => {
    const input = findDOMNode(this);
    input.select()
  }, []);

  return <input defaultValue="Hello" />;
}
```

```js
// After
function AutoselectingInput() {
  const ref = useRef(null);
  useEffect(() => {
    ref.current.select();
  }, []);

  return <input ref={ref} defaultValue="Hello" />
}
```

## New deprecations {/*new-deprecations*/}

### Deprecated: `element.ref` {/*deprecated-element-ref*/}

React 19 supports [`ref` as a prop](/blog/2024/04/25/react-19#ref-as-a-prop), so we're deprecating the `element.ref` in place of `element.props.ref`.

Accessing `element.ref` will warn:

<ConsoleBlockMulti>

<ConsoleLogLine level="error">

Accessing element.ref is no longer supported. ref is now a regular prop. It will be removed from the JSX Element type in a future release.

</ConsoleLogLine>

</ConsoleBlockMulti>

### Deprecated: `react-test-renderer` {/*deprecated-react-test-renderer*/}

We are deprecating `react-test-renderer` because it implements its own renderer environment that doesn't match the environment users use, promotes testing implementation details, and relies on introspection of React's internals.

The test renderer was created before there were more viable testing strategies available like [React Testing Library](https://testing-library.com), and we now recommend using a modern testing library instead.

In React 19, `react-test-renderer` logs a deprecation warning, and has switched to concurrent rendering. We recommend migrating your tests to [@testing-library/react](https://testing-library.com/docs/react-testing-library/intro/) or [@testing-library/react-native](https://testing-library.com/docs/react-native-testing-library/intro) for a modern and well supported testing experience.

## Notable changes {/*notable-changes*/}

### StrictMode changes {/*strict-mode-improvements*/}

React 19 includes several fixes and improvements to Strict Mode.

When double rendering in Strict Mode in development, `useMemo` and `useCallback` will reuse the memoized results from the first render during the second render. Components that are already Strict Mode compatible should not notice a difference in behavior.

As with all Strict Mode behaviors, these features are designed to proactively surface bugs in your components during development so you can fix them before they are shipped to production. For example, during development, Strict Mode will double-invoke ref callback functions on initial mount, to simulate what happens when a mounted component is replaced by a Suspense fallback.

### Improvements to Suspense {/*improvements-to-suspense*/}

In React 19, when a component suspends, React will immediately commit the fallback of the nearest Suspense boundary without waiting for the entire sibling tree to render. After the fallback commits, React schedules another render for the suspended siblings to "pre-warm" lazy requests in the rest of the tree:

<Diagram name="prerender" height={162} width={1270} alt="Diagram showing a tree of three components, one parent labeled Accordion and two children labeled Panel. Both Panel components contain isActive with value false.">

Previously, when a component suspended, the suspended siblings were rendered and then the fallback was committed.

</Diagram>

<Diagram name="prewarm" height={162} width={1270} alt="The same diagram as the previous, with the isActive of the first child Panel component highlighted indicating a click with the isActive value set to true. The second Panel component still contains value false." >

In React 19, when a component suspends, the fallback is committed and then the suspended siblings are rendered.

</Diagram>

This change means Suspense fallbacks display faster, while still warming lazy requests in the suspended tree.

### UMD builds removed {/*umd-builds-removed*/}

UMD was widely used in the past as a convenient way to load React without a build step. Now, there are modern alternatives for loading modules as scripts in HTML documents. Starting with React 19, React will no longer produce UMD builds to reduce the complexity of its testing and release process. 

To load React 19 with a script tag, we recommend using an ESM-based CDN such as [esm.sh](https://esm.sh/).

```html
<script type="module">
  import React from "https://esm.sh/react@19/?dev"
  import ReactDOMClient from "https://esm.sh/react-dom@19/client?dev"
  ...
</script>
```

### Libraries depending on React internals may block upgrades {/*libraries-depending-on-react-internals-may-block-upgrades*/}

This release includes changes to React internals that may impact libraries that ignore our pleas to not use internals like `SECRET_INTERNALS_DO_NOT_USE_OR_YOU_WILL_BE_FIRED`. These changes are necessary to land improvements in React 19, and will not break libraries that follow our guidelines.

Based on our [Versioning Policy](https://react.dev/community/versioning-policy#what-counts-as-a-breaking-change), these updates are not listed as breaking changes, and we are not including docs for how to upgrade them. The recommendation is to remove any code that depends on internals.

To reflect the impact of using internals, we have renamed the `SECRET_INTERNALS` suffix to: 

`_DO_NOT_USE_OR_WARN_USERS_THEY_CANNOT_UPGRADE`

In the future we will more aggressively block accessing internals from React to discourage usage and ensure users are not blocked from upgrading.

## TypeScript changes {/*typescript-changes*/}

### Removed deprecated TypeScript types {/*removed-deprecated-typescript-types*/}

We've cleaned up the TypeScript types based on the removed APIs in React 19. Some of the removed have types been moved to more relevant packages, and others are no longer needed to describe React's behavior.

<Note>
We've published [`types-react-codemod`](https://github.com/eps1lon/types-react-codemod/) to migrate most type related breaking changes:

```bash
npx types-react-codemod@latest preset-19 ./path-to-app
```

If you have a lot of unsound access to `element.props`, you can run this additional codemod:

```bash
npx types-react-codemod@latest react-element-default-any-props ./path-to-your-react-ts-files
```

</Note>

Check out [`types-react-codemod`](https://github.com/eps1lon/types-react-codemod/) for a list of supported replacements. If you feel a codemod is missing, it can be tracked in the [list of missing React 19 codemods](https://github.com/eps1lon/types-react-codemod/issues?q=is%3Aissue+is%3Aopen+sort%3Aupdated-desc+label%3A%22React+19%22+label%3Aenhancement).


### `ref` cleanups required {/*ref-cleanup-required*/}

_This change is included in the `react-19` codemod preset as [`no-implicit-ref-callback-return
`](https://github.com/eps1lon/types-react-codemod/#no-implicit-ref-callback-return)._

Due to the introduction of ref cleanup functions, returning anything else from a ref callback will now be rejected by TypeScript. The fix is usually to stop using implicit returns:

```diff [[1, 1, "("], [1, 1, ")"], [2, 2, "{", 15], [2, 2, "}", 1]]
- <div ref={current => (instance = current)} />
+ <div ref={current => {instance = current}} />
```

The original code returned the instance of the `HTMLDivElement` and TypeScript wouldn't know if this was supposed to be a cleanup function or not.

### `useRef` requires an argument {/*useref-requires-argument*/}

_This change is included in the `react-19` codemod preset as [`refobject-defaults`](https://github.com/eps1lon/types-react-codemod/#refobject-defaults)._

A long-time complaint of how TypeScript and React work has been `useRef`. We've changed the types so that `useRef` now requires an argument. This significantly simplifies its type signature. It'll now behave more like `createContext`.

```ts
// @ts-expect-error: Expected 1 argument but saw none
useRef();
// Passes
useRef(undefined);
// @ts-expect-error: Expected 1 argument but saw none
createContext();
// Passes
createContext(undefined);
```

This now also means that all refs are mutable. You'll no longer hit the issue where you can't mutate a ref because you initialised it with `null`:

```ts
const ref = useRef<number>(null);

// Cannot assign to 'current' because it is a read-only property
ref.current = 1;
```

`MutableRef` is now deprecated in favor of a single `RefObject` type which `useRef` will always return:

```ts
interface RefObject<T> {
  current: T
}

declare function useRef<T>: RefObject<T>
```

`useRef` still has a convenience overload for `useRef<T>(null)` that automatically returns `RefObject<T | null>`. To ease migration due to the required argument for `useRef`, a convenience overload for `useRef(undefined)` was added that automatically returns `RefObject<T | undefined>`.

Check out [[RFC] Make all refs mutable](https://github.com/DefinitelyTyped/DefinitelyTyped/pull/64772) for prior discussions about this change.

### Changes to the `ReactElement` TypeScript type {/*changes-to-the-reactelement-typescript-type*/}

_This change is included in the [`react-element-default-any-props`](https://github.com/eps1lon/types-react-codemod#react-element-default-any-props) codemod._

The `props` of React elements now default to `unknown` instead of `any` if the element is typed as `ReactElement`. This does not affect you if you pass a type argument to `ReactElement`:

```ts
type Example2 = ReactElement<{ id: string }>["props"];
//   ^? { id: string }
```

But if you relied on the default, you now have to handle `unknown`:

```ts
type Example = ReactElement["props"];
//   ^? Before, was 'any', now 'unknown'
```

You should only need it if you have a lot of legacy code relying on unsound access of element props. Element introspection only exists as an escape hatch, and you should make it explicit that your props access is unsound via an explicit `any`.

### The JSX namespace in TypeScript {/*the-jsx-namespace-in-typescript*/}
This change is included in the `react-19` codemod preset as [`scoped-jsx`](https://github.com/eps1lon/types-react-codemod#scoped-jsx)

A long-time request is to remove the global `JSX` namespace from our types in favor of `React.JSX`. This helps prevent pollution of global types which prevents conflicts between different UI libraries that leverage JSX.

You'll now need to wrap module augmentation of the JSX namespace in `declare module "....":

```diff
// global.d.ts
+ declare module "react" {
    namespace JSX {
      interface IntrinsicElements {
        "my-element": {
          myElementProps: string;
        };
      }
    }
+ }
```

The exact module specifier depends on the JSX runtime you specified in the `compilerOptions` of your `tsconfig.json`:

- For `"jsx": "react-jsx"` it would be `react/jsx-runtime`.
- For `"jsx": "react-jsxdev"` it would be `react/jsx-dev-runtime`.
- For `"jsx": "react"` and `"jsx": "preserve"` it would be `react`.

### Better `useReducer` typings {/*better-usereducer-typings*/}

`useReducer` now has improved type inference thanks to [@mfp22](https://github.com/mfp22).

However, this required a breaking change where `useReducer` doesn't accept the full reducer type as a type parameter but instead either needs none (and rely on contextual typing) or needs both the state and action type.

The new best practice is _not_ to pass type arguments to `useReducer`.
```diff
- useReducer<React.Reducer<State, Action>>(reducer)
+ useReducer(reducer)
```
This may not work in edge cases where you can explicitly type the state and action, by passing in the `Action` in a tuple:
```diff
- useReducer<React.Reducer<State, Action>>(reducer)
+ useReducer<State, [Action]>(reducer)
```
If you define the reducer inline, we encourage to annotate the function parameters instead:
```diff
- useReducer<React.Reducer<State, Action>>((state, action) => state)
+ useReducer((state: State, action: Action) => state)
```
This is also what you'd also have to do if you move the reducer outside of the `useReducer` call:

```ts
const reducer = (state: State, action: Action) => state;
```

## Changelog {/*changelog*/}

### Other breaking changes {/*other-breaking-changes*/}

- **react-dom**: Error for javascript URLs in `src` and `href` [#26507](https://github.com/facebook/react/pull/26507)
- **react-dom**: Remove `errorInfo.digest` from `onRecoverableError` [#28222](https://github.com/facebook/react/pull/28222)
- **react-dom**: Remove `unstable_flushControlled` [#26397](https://github.com/facebook/react/pull/26397)
- **react-dom**: Remove `unstable_createEventHandle` [#28271](https://github.com/facebook/react/pull/28271)
- **react-dom**: Remove `unstable_renderSubtreeIntoContainer` [#28271](https://github.com/facebook/react/pull/28271)
- **react-dom**: Remove `unstable_runWithPriority` [#28271](https://github.com/facebook/react/pull/28271)
- **react-is**: Remove deprecated methods from `react-is` [28224](https://github.com/facebook/react/pull/28224)

### Other notable changes {/*other-notable-changes*/}

- **react**: Batch sync, default and continuous lanes [#25700](https://github.com/facebook/react/pull/25700)
- **react**: Don't prerender siblings of suspended component [#26380](https://github.com/facebook/react/pull/26380)
- **react**: Detect infinite update loops caused by render phase updates [#26625](https://github.com/facebook/react/pull/26625)
- **react-dom**: Transitions in popstate are now synchronous [#26025](https://github.com/facebook/react/pull/26025)
- **react-dom**: Remove layout effect warning during SSR [#26395](https://github.com/facebook/react/pull/26395)
- **react-dom**: Warn and don’t set empty string for src/href (except anchor tags) [#28124](https://github.com/facebook/react/pull/28124)

For a full list of changes, please see the [Changelog](https://github.com/facebook/react/blob/main/CHANGELOG.md#1900-december-5-2024).

---

Thanks to [Andrew Clark](https://twitter.com/acdlite), [Eli White](https://twitter.com/Eli_White), [Jack Pope](https://github.com/jackpope), [Jan Kassens](https://github.com/kassens), [Josh Story](https://twitter.com/joshcstory), [Matt Carroll](https://twitter.com/mattcarrollcode), [Noah Lemen](https://twitter.com/noahlemen), [Sophie Alpert](https://twitter.com/sophiebits), and [Sebastian Silbermann](https://twitter.com/sebsilbermann) for reviewing and editing this post.

---
# Source: react-19.md
---
---
title: "React v19"
author: The React Team
date: 2024/12/05
description: React 19 版现在可以在 npm 上使用了! 在这篇文章中，我们将概述 React 19 的新特性，以及如何使用它们。
---

2024 年 12 月 05 日 [The React Team](/community/team)

---
<Note>

### React 19 现已稳定！ {/*react-19-is-now-stable*/}

从 4 月份发布这篇介绍 React 19 RC 的博客以来有以下新增内容：

- **预热 suspend 树**：阅读 [改善 Suspense](/blog/2024/04/25/react-19-upgrade-guide#improvements-to-suspense) 来了解更多。
- **React DOM 静态 API**：阅读 [新的 React DOM 静态 API](#new-react-dom-static-apis) 来了解更多。

__本文的日期已更新，以反映稳定版的发布日期。__

</Note>

<Intro>

React 19 版本现在可以在 npm 上使用了!

</Intro>

在我们的 [React 19 升级指南](/blog/2024/04/25/react-19-upgrade-guide) 中, 我们分享了将应用程序升级到 React 19 的分步说明。在这篇文章中，我们将概述 React 19 的新特性，以及如何使用它们。

- [React 19 中的新功能](#whats-new-in-react-19)
- [React 19 中的改进](#improvements-in-react-19)
- [如何升级](#how-to-upgrade)

有关破坏性更改的列表，请参阅 [升级指南](/blog/2024/04/25/react-19-upgrade-guide)。

---

## React 19 中的新功能 {/*whats-new-in-react-19*/}

### Actions {/*actions*/}

在 React 应用中，一个常见的用例是执行数据变更，然后响应更新状态。例如，当用户提交一个表单来更改他们的名字，你会发起一个 API 请求，然后处理响应。在过去，你需要手动处理待定状态、错误、乐观更新和顺序请求。

例如，你可以在 `useState` 中处理待定和错误状态：

```js
// 没有 Actions 之前
function UpdateName({}) {
  const [name, setName] = useState("");
  const [error, setError] = useState(null);
  const [isPending, setIsPending] = useState(false);

  const handleSubmit = async () => {
    setIsPending(true);
    const error = await updateName(name);
    setIsPending(false);
    if (error) {
      setError(error);
      return;
    } 
    redirect("/path");
  };

  return (
    <div>
      <input value={name} onChange={(event) => setName(event.target.value)} />
      <button onClick={handleSubmit} disabled={isPending}>
        Update
      </button>
      {error && <p>{error}</p>}
    </div>
  );
}
```

在 React 19 中，我们正在添加在过渡中使用异步函数的支持，以自动处理待定状态、错误、表单和乐观更新。

例如，你可以使用 `useTransition` 来为你处理待定状态：

```js
// 使用 Actions 中的待定状态
function UpdateName({}) {
  const [name, setName] = useState("");
  const [error, setError] = useState(null);
  const [isPending, startTransition] = useTransition();

  const handleSubmit = () => {
    startTransition(async () => {
      const error = await updateName(name);
      if (error) {
        setError(error);
        return;
      } 
      redirect("/path");
    })
  };

  return (
    <div>
      <input value={name} onChange={(event) => setName(event.target.value)} />
      <button onClick={handleSubmit} disabled={isPending}>
        Update
      </button>
      {error && <p>{error}</p>}
    </div>
  );
}
```

异步过渡会立即将 `isPending` 状态设置为 true，发出异步请求，然后在任何过渡后将 `isPending` 切换为 `false`。这使你能够在数据变化时保持当前 UI 的响应性和交互性。

<Note>

#### 按照惯例，使用异步过渡的函数被称为 "Actions"。 {/*by-convention-functions-that-use-async-transitions-are-called-actions*/}

Actions 自动为你管理数据提交：

- **待定状态**: Actions 提供一个待定状态，该状态在请求开始时启动，并在最终状态更新提交时自动重置。
- **乐观更新**: Actions 支持新的 [`useOptimistic`](#new-hook-optimistic-updates)  Hook，因此你可以在请求提交时向用户显示即时反馈。
- **错误处理**: Actions 提供错误处理，因此当请求失败时，你可以显示错误边界，并自动将乐观更新恢复到其原始值。
- **表单**: `<form>` 元素现在支持将函数传递给 `action` 和 `formAction` 属性。将函数传递给 `action` 属性默认使用 Actions，并在提交后自动重置表单。

</Note>

在 Actions 的基础上，React 19 引入了 [`useOptimistic`](#new-hook-optimistic-updates) 来管理乐观更新，以及一个新的 Hook [`React.useActionState`](#new-hook-useactionstate) 来处理 Actions 的常见情况。在 `react-dom` 中我们添加了 [`<form>` Actions](#form-actions) 来自动管理表单和 `useFormStatus` 来支持表单中 Actions 的常见情况。

在 React 19 中，上述示例可以简化为：

```js
// 使用表单的 Actions 和 useActionState
function ChangeName({ name, setName }) {
  const [error, submitAction, isPending] = useActionState(
    async (previousState, formData) => {
      const error = await updateName(formData.get("name"));
      if (error) {
        return error;
      }
      redirect("/path");
      return null;
    },
    null,
  );

  return (
    <form action={submitAction}>
      <input type="text" name="name" />
      <button type="submit" disabled={isPending}>Update</button>
      {error && <p>{error}</p>}
    </form>
  );
}
```

在下一节中，我们将详细介绍 React 19 中的每一个新的 Action 功能。

### 新的 Hook: `useActionState` {/*new-hook-useactionstate*/}

为了使 Actions 的常见情况更加简单，我们添加了一个名为 `useActionState` 的新 Hook：

```js
const [error, submitAction, isPending] = useActionState(
  async (previousState, newName) => {
    const error = await updateName(newName);
    if (error) {
      // 你可以返回操作的任何结果。
      // 这里，我们只返回错误。
      return error;
    }

    // 处理成功的情况。
    return null;
  },
  null,
);
```

`useActionState` 接受一个函数（"Action"），并返回一个被包装的用于调用的 Action。这是因为 Actions 是可以组合的。当调用被包装的 Action 时，`useActionState` 将返回 Action 的最后结果作为 `data`，以及 Action 的待定状态作为 `pending`。

<Note>

`React.useActionState` 在 Canary 版本中曾被称为 `ReactDOM.useFormState`，但我们已经将其重命名并弃用了 `useFormState`。

有关更多信息，请参见 [#28491](https://github.com/facebook/react/pull/28491)。

</Note>

相关的更多信息，请参阅文档 [`useActionState`](/reference/react/useActionState)。

### React DOM: `<form>` Actions {/*form-actions*/}

Actions 也与 React 19 的新 `<form>` 功能集成在 `react-dom` 中。我们已经添加了对将函数作为 `<form>`、`<input>` 和 `<button>` 元素的 `action` 和 `formAction` 属性的支持，以便使用 Actions 自动提交表单：

```js [[1,1,"actionFunction"]]
<form action={actionFunction}>
```

当 `<form>` Action 成功时，React 将自动为非受控组件重置表单。如果你需要手动重置 `<form>`，你可以调用新的 `requestFormReset` React DOM API。

有关更多信息，请参阅 `react-dom` 文档中的 [`<form>`](/reference/react-dom/components/form)、[`<input>`](/reference/react-dom/components/input) 和 `<button>`。

### React DOM: 新 Hook: `useFormStatus` {/*new-hook-useformstatus*/}

在设计系统中，常常需要编写设计一类能够访问其所在的 `<form>` 的信息而无需将属性传递到组件内的组件。这可以通过 Context 来实现，但为了使这类常见情况更简单，我们添加了一个新的 Hook `useFormStatus`：

```js [[1, 4, "pending"], [1, 5, "pending"]]
import {useFormStatus} from 'react-dom';

function DesignButton() {
  const {pending} = useFormStatus();
  return <button type="submit" disabled={pending} />
}
```

`useFormStatus` 读取父 `<form>` 的状态，就像表单是一个 Context 提供者一样。

有关更多信息，请参阅 `react-dom` 文档中的 [`useFormStatus`](/reference/react-dom/hooks/useFormStatus)。

### 新 Hook: `useOptimistic` {/*new-hook-optimistic-updates*/}

执行数据变更时的另一个常见 UI 模式是在异步请求进行时乐观地显示最终状态。在 React 19 中，我们添加了一个名为 `useOptimistic` 的新 Hook，以便更容易实现这一点：

```js {2,6,13,19}
function ChangeName({currentName, onUpdateName}) {
  const [optimisticName, setOptimisticName] = useOptimistic(currentName);

  const submitAction = async formData => {
    const newName = formData.get("name");
    setOptimisticName(newName);
    const updatedName = await updateName(newName);
    onUpdateName(updatedName);
  };

  return (
    <form action={submitAction}>
      <p>Your name is: {optimisticName}</p>
      <p>
        <label>Change Name:</label>
        <input
          type="text"
          name="name"
          disabled={currentName !== optimisticName}
        />
      </p>
    </form>
  );
}
```

`useOptimistic` Hook 会在 `updateName` 请求进行时立即渲染 `optimisticName`。当更新完成或出错时，React 将自动切换回 `currentName` 值。

有关更多信息，请参阅 [`useOptimistic`](/reference/react/useOptimistic) 文档。

### 新的 API: `use` {/*new-feature-use*/}

在 React 19 中，我们引入了一个新的 API 来在渲染中读取资源：`use`。

例如，你可以使用 `use` 读取一个 promise，React 将挂起，直到 promise 解析完成：

```js {1,5}
import {use} from 'react';

function Comments({commentsPromise}) {
  // `use` 将被暂停直到 promise 被解决.
  const comments = use(commentsPromise);
  return comments.map(comment => <p key={comment.id}>{comment}</p>);
}

function Page({commentsPromise}) {
  // 当“use”在注释中暂停时,
  // 将显示此悬念边界。
  return (
    <Suspense fallback={<div>Loading...</div>}>
      <Comments commentsPromise={commentsPromise} />
    </Suspense>
  )
}
```

<Note>

#### `use` 不支持在渲染中创建的 promises。 {/*use-does-not-support-promises-created-in-render*/}

如果你尝试将在渲染中创建的 promise 传递给 `use`，React 将发出警告：

<ConsoleBlockMulti>

<ConsoleLogLine level="error">

A component was suspended by an uncached promise. Creating promises inside a Client Component or hook is not yet supported, except via a Suspense-compatible library or framework.

</ConsoleLogLine>

</ConsoleBlockMulti>

为了解决这个问题，你需要从支持 promise 缓存的 Suspense 强化库或框架中传递一个 promise。在未来，我们计划推出功能，使在渲染中缓存 promise 更加容易。

</Note>

你也可以使用 `use` 读取 context，这使你能够在如提前返回之后的情况下有条件地读取 Context：

```js {1,11}
import {use} from 'react';
import ThemeContext from './ThemeContext'

function Heading({children}) {
  if (children == null) {
    return null;
  }
  
  // 因为过早的返回
  // 这里 useContext 无法正常工作。
  const theme = use(ThemeContext);
  return (
    <h1 style={{color: theme.color}}>
      {children}
    </h1>
  );
}
```

`use` API 只能在渲染中被调用，类似于 hooks。与 hooks 不同，`use` 可以被有条件地调用。在未来，我们计划支持在渲染中使用 `use` 消费更多资源的方式。

有关更多信息，请参阅 [`use`](/reference/react/use) 文档。

## New React DOM Static APIs {/*new-react-dom-static-apis*/}

We've added two new APIs to `react-dom/static` for static site generation:
- [`prerender`](/reference/react-dom/static/prerender)
- [`prerenderToNodeStream`](/reference/react-dom/static/prerenderToNodeStream)

These new APIs improve on `renderToString` by waiting for data to load for static HTML generation. They are designed to work with streaming environments like Node.js Streams and Web Streams. For example, in a Web Stream environment, you can prerender a React tree to static HTML with `prerender`: 

```js
import { prerender } from 'react-dom/static';

async function handler(request) {
  const {prelude} = await prerender(<App />, {
    bootstrapScripts: ['/main.js']
  });
  return new Response(prelude, {
    headers: { 'content-type': 'text/html' },
  });
}
```

Prerender APIs will wait for all data to load before returning the static HTML stream. Streams can be converted to strings, or sent with a streaming response. They do not support streaming content as it loads, which is supported by the existing [React DOM server rendering APIs](/reference/react-dom/server).

For more information, see [React DOM Static APIs](/reference/react-dom/static).

## React 服务器组件 {/*react-server-components*/}

### 服务器组件 {/*server-components*/}

服务器组件是一种新的选项，允许在打包前提前渲染组件，在与你的客户端应用程序或 SSR 服务器不同的环境中。这个独立的环境就是 React 服务器组件中的 "服务器"。服务器组件可以在你的 CI 服务器上在构建时运行一次，或者可以在每次请求时使用 web 服务器运行。

React 19 包含了所有从 Canary 渠道引入的 React 服务器组件功能。这意味着，现在可以将 React 19 作为 peer 依赖项来发布带有服务器组件的库，使用 `react-server` [导出条件](https://github.com/reactjs/rfcs/blob/main/text/0227-server-module-conventions.md#react-server-conditional-exports) 用于支持 [全栈 React 架构](/learn/creating-a-react-app#which-features-make-up-the-react-teams-full-stack-architecture-vision) 的框架。


<Note>

#### 如何构建对服务器组件的支持? {/*how-do-i-build-support-for-server-components*/}

虽然 React 19 中的 React 服务器组件是稳定的，并且在主版本之间不会发生破坏，但用于实现 React 服务器组件打包器或框架的底层 API 不遵循 semver，并可能在 React 19.x 的小版本之间发生破坏。

为了支持 React 服务器组件作为打包器或框架，我们建议固定到特定的 React 版本，或者使用 Canary 发行版。我们将继续与打包器和框架合作，以稳定用于实现 React 服务器组件的 API。

</Note>


有关更多信息，请参阅文档 [React Server Components](/reference/rsc/server-components).

### 服务器操作 {/*server-actions*/}

服务器 Actions 允许客户端组件调用在服务器上执行的异步函数。

当使用 `"use server"` 指令定义服务器 Action 时，你的框架将自动创建一个指向服务器函数的引用，并将该引用传递给客户端组件。当在客户端调用该函数时，React 将向服务器发送一个请求来执行该函数，并返回结果。

<Note>

#### 服务器组件没有指令 {/*there-is-no-directive-for-server-components*/}

一个常见的误解是服务器组件由 `"use server"` 指示，但服务器组件没有指令。`"use server"` 指令用于服务器 Actions。

有关更多信息，请参阅 [指令](/reference/rsc/directives) 文档。

</Note>

服务器 Actions 可以在服务器组件中创建并作为 props 传递给客户端组件，或者可以在客户端组件中导入和使用。

有关更多信息，请参阅 [React 服务器 Actions](/reference/rsc/server-actions) 文档。

## React 19 中的改进 {/*improvements-in-react-19*/}

### `ref` 作为一个属性 {/*ref-as-a-prop*/}

从 React 19 开始，你现在可以在函数组件中将 `ref` 作为 prop 进行访问：

```js [[1, 1, "ref"], [1, 2, "ref", 45], [1, 6, "ref", 14]]
function MyInput({placeholder, ref}) {
  return <input placeholder={placeholder} ref={ref} />
}

//...
<MyInput ref={ref} />
```

新的函数组件将不再需要 `forwardRef`，我们将发布一个 codemod 来自动更新你的组件以使用新的 `ref` prop。在未来的版本中，我们将弃用并移除 `forwardRef`。

<Note>

在类组件中，`ref` 不作为 props 传递，因为它们引用的是组件实例。

</Note>

### 激活错误的差异 {/*diffs-for-hydration-errors*/}

在 `react-dom` 中，我们也改进了水合错误的错误报告。例如，现在不再在 DEV 中记录多个没有任何不匹配信息的错误：

<ConsoleBlockMulti>

<ConsoleLogLine level="error">

Warning: Text content did not match. Server: "Server" Client: "Client"
{'  '}at span
{'  '}at App

</ConsoleLogLine>

<ConsoleLogLine level="error">

Warning: An error occurred during hydration. The server HTML was replaced with client content in \<div\>.

</ConsoleLogLine>

<ConsoleLogLine level="error">

Warning: Text content did not match. Server: "Server" Client: "Client"
{'  '}at span
{'  '}at App

</ConsoleLogLine>

<ConsoleLogLine level="error">

Warning: An error occurred during hydration. The server HTML was replaced with client content in \<div\>.

</ConsoleLogLine>

<ConsoleLogLine level="error">

Uncaught Error: Text content does not match server-rendered HTML.
{'  '}at checkForUnmatchedText
{'  '}...

</ConsoleLogLine>

</ConsoleBlockMulti>

现在我们会记录一条带有不匹配差异的单一消息：


<ConsoleBlockMulti>

<ConsoleLogLine level="error">

Uncaught Error: Hydration failed because the server rendered HTML didn't match the client. As a result this tree will be regenerated on the client. This can happen if an SSR-ed Client Component used:{'\n'}
\- A server/client branch `if (typeof window !== 'undefined')`.
\- Variable input such as `Date.now()` or `Math.random()` which changes each time it's called.
\- Date formatting in a user's locale which doesn't match the server.
\- External changing data without sending a snapshot of it along with the HTML.
\- Invalid HTML tag nesting.{'\n'}
It can also happen if the client has a browser extension installed which messes with the HTML before React loaded.{'\n'}
https://react.dev/link/hydration-mismatch {'\n'}
{'  '}\<App\>
{'    '}\<span\>
{'+    '}Client
{'-    '}Server{'\n'}
{'  '}at throwOnHydrationMismatch
{'  '}...

</ConsoleLogLine>

</ConsoleBlockMulti>

### `<Context>` 作为提供者 {/*context-as-a-provider*/}

在 React 19 中，你可以将 `<Context>` 渲染为提供者，就无需再使用 `<Context.Provider>` 了：


```js {5,7}
const ThemeContext = createContext('');

function App({children}) {
  return (
    <ThemeContext value="dark">
      {children}
    </ThemeContext>
  );  
}
```

新的 Context 提供者可以使用 `<Context>`，我们将发布一个 codemod 来转换现有的提供者。在未来的版本中，我们将弃用 `<Context.Provider>`。

### refs 支持清理函数 {/*cleanup-functions-for-refs*/}

这将使得在 `ref` 改变时执行清理操作变得更加容易。例如，你可以在 `ref` 改变时取消订阅事件：

```js {7-9}
<input
  ref={(ref) => {
    // ref 创建

    // 新特性: 当元素从 DOM 中被移除时
    // 返回一个清理函数来重置 ref
    return () => {
      // ref cleanup
    };
  }}
/>
```

当组件卸载时，React 将调用从 `ref` 回调返回的清理函数。这适用于 DOM refs，类组件的 refs，以及 `useImperativeHandle`。

<Note>

以前，当卸载组件时，React 会用 `null` 调用 `ref` 函数。如果你的 `ref` 返回一个清理函数，React 现在将跳过这一步。

在未来的版本中，我们将弃用在卸载组件时用 `null` 调用 refs。

</Note>

由于引入了 `ref` 清理函数，现在 TypeScript 将拒绝从 `ref` 回调中返回任何其他内容。通常的解决方法是停止使用隐式返回，例如：

```diff [[1, 1, "("], [1, 1, ")"], [2, 2, "{", 15], [2, 2, "}", 1]]
- <div ref={current => (instance = current)} />
+ <div ref={current => {instance = current}} />
```

原始代码返回了 `HTMLDivElement` 的实例，TypeScript 不知道这是否应该是一个清理函数，或者你是否不想返回一个清理函数。

你可以使用 [`no-implicit-ref-callback-return`](https://github.com/eps1lon/types-react-codemod/#no-implicit-ref-callback-return) 这个 codemod 来转换这种模式。

### `useDeferredValue` 初始化 value {/*use-deferred-value-initial-value*/}

我们为 `useDeferredValue` 添加了一个 `initialValue` 选项：

```js [[1, 1, "deferredValue"], [1, 4, "deferredValue"], [2, 4, "''"]]
function Search({deferredValue}) {
  // On initial render the value is ''.
  // Then a re-render is scheduled with the deferredValue.
  const value = useDeferredValue(deferredValue, '');
  
  return (
    <Results query={value} />
  );
}
````

当提供了 <CodeStep step={2}>initialValue</CodeStep>, `useDeferredValue` 将在组件的初始渲染中返回它作为 `value` , 并在后台安排一个使用返回的  <CodeStep step={1}>deferredValue</CodeStep> 重新渲染。

有关更多信息，请参阅 [`useDeferredValue`](/reference/react/useDeferredValue)。

### 支持文档元数据 {/*support-for-metadata-tags*/}

在 HTML 中，像 `<title>`、`<link>` 和 `<meta>` 这样的文档元数据标签被保留在文档的 `<head>` 部分。在 React 中，决定应用程序适合的元数据的组件可能与你渲染 `<head>` 的地方相距甚远，或者 React 根本不渲染 `<head>`。在过去，这些元素需要在效果中手动插入，或者通过像 [`react-helmet`](https://github.com/nfl/react-helmet) 这样的库，并在服务器渲染 React 应用程序时需要小心处理。

在 React 19 中，我们将原生支持在组件中渲染文档元数据标签：

```js {5-8}
function BlogPost({post}) {
  return (
    <article>
      <h1>{post.title}</h1>
      <title>{post.title}</title>
      <meta name="author" content="Josh" />
      <link rel="author" href="https://twitter.com/joshcstory/" />
      <meta name="keywords" content={post.keywords} />
      <p>
        Eee equals em-see-squared...
      </p>
    </article>
  );
}
```

当 React 渲染这个组件时，它会看到 `<title>`、`<link>` 和 `<meta>` 标签，并自动将它们提升到文档的 `<head>` 部分。通过原生支持这些元数据标签，我们能够确保它们与仅客户端应用、流式 SSR 和服务器组件一起工作。

<Note>

#### 你可能仍然需要一个元数据库 {/*you-may-still-want-a-metadata-library*/}

对于简单的用例，渲染文档元数据为标签可能是合适的，但库可以提供更强大的功能，如基于当前路由用特定的元数据覆盖通用元数据。这些功能使得像 [`react-helmet`](https://github.com/nfl/react-helmet) 这样的框架和库更容易支持元数据标签，而不是替换它们。

</Note>

有关更多信息，请参阅文档 [`<title>`](/reference/react-dom/components/title), [`<link>`](/reference/react-dom/components/link), and [`<meta>`](/reference/react-dom/components/meta).

### 支持样式表 {/*support-for-stylesheets*/}

样式表，无论是外部链接的 (`<link rel="stylesheet" href="...">`) 还是内联的 (`<style>...</style>`)，都需要在 DOM 中进行精确的定位，因为样式优先级规则。构建一个允许在组件内部进行组合的样式表功能是困难的，所以用户通常要么将所有的样式远离可能依赖它们的组件加载，要么使用一个封装了这种复杂性的样式库。

在 React 19 中，我们正在解决这个复杂性，并提供更深入的集成到客户端的并发渲染和服务器的流式渲染，内置支持样式表。如果你告诉 React 你的样式表的 `precedence`，它将管理样式表在 DOM 中的插入顺序，并确保在显示依赖于这些样式规则的内容之前加载样式表（如果是外部的）。

```js {4,5,17}
function ComponentOne() {
  return (
    <Suspense fallback="loading...">
      <link rel="stylesheet" href="foo" precedence="default" />
      <link rel="stylesheet" href="bar" precedence="high" />
      <article class="foo-class bar-class">
        {...}
      </article>
    </Suspense>
  )
}

function ComponentTwo() {
  return (
    <div>
      <p>{...}</p>
      <link rel="stylesheet" href="baz" precedence="default" />  <-- will be inserted between foo & bar
    </div>
  )
}
```

在服务器端渲染时，React 会在 `<head>` 中包含样式表，确保浏览器在加载完样式表之前不会进行绘制。如果在已经开始流式传输后才发现样式表，React 会确保在揭示依赖于该样式表的 Suspense 边界的内容之前，将样式表插入到客户端的 `<head>` 中。

在客户端渲染时，React 会等待新渲染的样式表加载完成后再提交渲染。如果你在应用程序的多个地方渲染此组件，React 会只在文档中包含一次样式表：

```js {5}
function App() {
  return <>
    <ComponentOne />
    ...
    <ComponentOne /> // won't lead to a duplicate stylesheet link in the DOM
  </>
}
```

对于习惯于手动加载样式表的用户来说，这是一个机会，可以将这些样式表放在依赖它们的组件旁边，从而更好地进行本地推理，并确保只加载你实际依赖的样式表。

样式库和与打包器的样式集成也可以采用这种新的功能，所以即使你不直接渲染你自己的样式表，你也可以从你的工具升级到使用这个特性中受益。

有关更多详细信息，请阅读 [`<link>`](/reference/react-dom/components/link) 和 [`<style>`](/reference/react-dom/components/style) 的文档。

### 支持异步脚本 {/*support-for-async-scripts*/}

在 HTML 中，普通脚本 (`<script src="...">`) 和延迟脚本 (`<script defer="" src="...">`) 按照文档顺序加载，这使得在组件树深处渲染这些类型的脚本变得具有挑战性。然而，异步脚本 (`<script async="" src="...">`) 将以任意顺序加载。

在 React 19 中，我们通过允许你在组件树的任何位置，即实际依赖脚本的组件内部，渲染它们，从而为异步脚本提供了更好的支持，无需管理脚本实例的重新定位和去重。

```js {4,15}
function MyComponent() {
  return (
    <div>
      <script async={true} src="..." />
      Hello World
    </div>
  )
}

function App() {
  <html>
    <body>
      <MyComponent>
      ...
      <MyComponent> // won't lead to duplicate script in the DOM
    </body>
  </html>
}
```

在所有渲染环境中，异步脚本将被去重，因此即使它被多个不同的组件渲染，React 也只会加载并执行脚本一次。

在服务器端渲染中，异步脚本将被包含在 `<head>` 中，并优先于阻塞绘制的更关键的资源，如样式表、字体和图片预加载。

有关更多详细信息，请阅读 [`<script>`](/reference/react-dom/components/script) 的文档。

### 支持预加载资源 {/*support-for-preloading-resources*/}

在初始文档加载和客户端更新时，尽早告诉浏览器它可能需要加载的资源，可以显著提高页面性能。

React 19 包含了一些新的 API，用于加载和预加载浏览器资源，使得构建不受资源加载效率影响的优秀体验变得尽可能容易。

```js
import { prefetchDNS, preconnect, preload, preinit } from 'react-dom'
function MyComponent() {
  preinit('https://.../path/to/some/script.js', {as: 'script' }) // loads and executes this script eagerly
  preload('https://.../path/to/font.woff', { as: 'font' }) // preloads this font
  preload('https://.../path/to/stylesheet.css', { as: 'style' }) // preloads this stylesheet
  prefetchDNS('https://...') // when you may not actually request anything from this host
  preconnect('https://...') // when you will request something but aren't sure what
}
```
```html
<!-- the above would result in the following DOM/HTML -->
<html>
  <head>
    <!-- links/scripts are prioritized by their utility to early loading, not call order -->
    <link rel="prefetch-dns" href="https://...">
    <link rel="preconnect" href="https://...">
    <link rel="preload" as="font" href="https://.../path/to/font.woff">
    <link rel="preload" as="style" href="https://.../path/to/stylesheet.css">
    <script async="" src="https://.../path/to/some/script.js"></script>
  </head>
  <body>
    ...
  </body>
</html>
```

这些 API 可以通过将像字体这样的额外资源的发现从样式表加载中移出来，优化初始页面加载。它们还可以通过预取预期导航使用的资源列表，然后在点击或甚至悬停时积极预加载这些资源，使客户端更新更快。

有关更多详细信息，请参阅 [资源预加载 API](/reference/react-dom#resource-preloading-apis)。

### 兼容第三方脚本和扩展 {/*compatibility-with-third-party-scripts-and-extensions*/}

我们改进了激活机制，以考虑第三方脚本和浏览器扩展。

在激活过程中，如果在客户端渲染的元素与从服务器获取的 HTML 中找到的元素不匹配，React 将强制进行客户端重新渲染以修复内容。以前，如果一个元素是由第三方脚本或浏览器扩展插入的，它会触发一个不匹配的错误并进行客户端渲染。

在 React 19 中，`<head>` 和 `<body>` 中的意外标签将被跳过，避免了不匹配的错误。如果 React 需要由于无关的激活不匹配而重新渲染整个文档，它将保留由第三方脚本和浏览器扩展插入的样式表。

### 更好的错误报告 {/*error-handling*/}

在 React 19 中，我们改进了错误处理，以消除重复并提供处理捕获和未捕获错误的选项。例如，当在由错误边界捕获的渲染中出现错误时，以前 React 会抛出两次错误（一次是原始错误，然后在自动恢复失败后再次抛出），然后调用 `console.error` 提供错误发生的信息。

这导致每个捕获的错误都有三个错误：

<ConsoleBlockMulti>

<ConsoleLogLine level="error">

Uncaught Error: hit
{'  '}at Throws
{'  '}at renderWithHooks
{'  '}...

</ConsoleLogLine>

<ConsoleLogLine level="error">

Uncaught Error: hit<span className="ms-2 text-gray-30">{'    <--'} Duplicate</span>
{'  '}at Throws
{'  '}at renderWithHooks
{'  '}...

</ConsoleLogLine>

<ConsoleLogLine level="error">

The above error occurred in the Throws component:
{'  '}at Throws
{'  '}at ErrorBoundary
{'  '}at App{'\n'}
React will try to recreate this component tree from scratch using the error boundary you provided, ErrorBoundary.

</ConsoleLogLine>

</ConsoleBlockMulti>

在 React 19 中，我们记录一个包含所有错误信息的单一错误：

<ConsoleBlockMulti>

<ConsoleLogLine level="error">

Error: hit
{'  '}at Throws
{'  '}at renderWithHooks
{'  '}...{'\n'}
The above error occurred in the Throws component:
{'  '}at Throws
{'  '}at ErrorBoundary
{'  '}at App{'\n'}
React will try to recreate this component tree from scratch using the error boundary you provided, ErrorBoundary.
{'  '}at ErrorBoundary
{'  '}at App

</ConsoleLogLine>

</ConsoleBlockMulti>

此段代码介绍了 React 19 中添加的两个新的根选项，用于补充 `onRecoverableError`：

- `onCaughtError`：当 React 在错误边界中捕获错误时调用。
- `onUncaughtError`：当抛出错误并且未被错误边界捕获时调用。
- `onRecoverableError`：当抛出错误并自动恢复时调用。

有关更多信息和示例，请参阅 [`createRoot`](/reference/react-dom/client/createRoot) 和 [`hydrateRoot`](/reference/react-dom/client/hydrateRoot) 的文档。

### 支持自定义元素 {/*support-for-custom-elements*/}

React 19 添加了对自定义元素的全面支持，并通过了 [Custom Elements Everywhere](https://custom-elements-everywhere.com/) 上的所有测试。

在过去的版本中，使用 React 中的自定义元素很困难，因为 React 将无法识别的 props 视为 HTML attribute 而不是 DOM property。在 React 19 中，我们添加了对 DOM property 的支持，该支持在客户端和 SSR 期间都有效，策略如下：

- **服务器端渲染**：传递给自定义元素的 props 将作为 HTML attribute 渲染，如果它们的类型是原始值，如 `string`、`number`，或者值为 `true`。具有非原始类型的 props，如 `object`、`symbol`、`function`，或者值为 `false` 的 props 将被省略。
- **客户端渲染**：匹配自定义元素实例上的属性的 props 将被赋值为 DOM property，否则它们将被赋值为 HTML attribute。

感谢 [Joey Arhar](https://github.com/josepharhar) 在 React 中推动自定义元素支持的设计和实现。

#### 如何升级 {/*how-to-upgrade*/}

请查看 [React 19 升级指南](/blog/2024/04/25/react-19-upgrade-guide) 以获取逐步指导和完整的破坏性和显著变化列表。

__注意：这篇文章最初发布于 2024 年 4 月 25 日，并已将内容更新至 2024 年 12 月 5 日发布的稳定版本。__

---
# Source: react-labs-what-we-have-been-working-on-february-2024.md
---
---
title: "React Labs：我们正在努力的方向——2024 年 2 月"
author: Joseph Savona, Ricky Hanlon, Andrew Clark, Matt Carroll, and Dan Abramov
date: 2024/02/15
description: 在 React Labs 的文章中，我们讲述了正在进行研究与开发的项目。自上次更新以来，我们又取得了巨大进展，现在我们想将这些内容分享给大家。
---

2024 年 2 月 15 日 [Joseph Savona](https://twitter.com/en_JS)、[Ricky Hanlon](https://twitter.com/rickhanlonii)、[Andrew Clark](https://twitter.com/acdlite)、[Matt Carroll](https://twitter.com/mattcarrollcode) 与 [Dan Abramov](https://bsky.app/profile/danabra.mov)

---

<Intro>

在 React Labs 的文章中，我们讲述了正在进行研究与开发的项目。自 [上次更新](/blog/2023/03/22/react-labs-what-we-have-been-working-on-march-2023) 以来，我们又取得了巨大进展，现在我们想将这些内容分享给大家。

</Intro>

---

## React 编译器 {/*react-compiler*/}

React 编译器不再是一个研究项目：该编译器现在已经在生产环境中为 instagram.com 提供动力，并且我们正在努力将该编译器推广到 Meta 的其他平台，并准备进行第一次开源发布。

正如我们在 [之前的文章](/blog/2023/03/22/react-labs-what-we-have-been-working-on-march-2023#react-optimizing-compiler) 中所讨论的，当状态发生变化时，React 有时会过度重新渲染。自 React 早期以来，我们对这种情况的解决方案一直是手动记忆化。在我们当前的 API 中，这意味着使用 [`useMemo`](/reference/react/useMemo)、[`useCallback`](/reference/react/useCallback) 和 [`memo`](/reference/react/memo) API 手动调整 React 在状态变化时重新渲染的程度。但是手动记忆化是一种妥协。它会使我们的代码变得混乱、很容易出错，并且需要额外的工作来保持更新。

手动记忆化是一个合理的妥协，但我们并不满意。我们的愿景是当状态发生变化时 React 可以自动重新渲染 UI 的恰当部分，而不是向 React 的核心心智模型妥协。我们相信 React 的方式——将 UI 视为状态的简单函数，使用标准的 JavaScript 值和习惯用法——是 React 为许多开发人员提供可接近性的关键部分。这就是我们投资于构建 React 的优化编译器的原因。

JavaScript 是一个因其松散规则和动态特性而闻名的具有挑战性的语言。React 编译器能够通过模拟 JavaScript 的规则和“React 的规则”来安全地编译代码。例如，React 组件必须是幂等的——给定相同的输入返回相同的值——并且不能突变 props 或状态值。这些规则限制了开发人员可以做的事情，并为编译器优化开辟了一个安全的空间。

当然，我们理解开发人员有时会在规则上有所放宽，我们的目标是使 React 编译器能够在尽可能多的代码上立即生效。编译器会尝试检测代码是否严格遵循 React 的规则，如果安全则编译代码，否则跳过编译。我们正在针对 Meta 庞大且多样化的代码库进行测试，以帮助验证这种方法。

对于那些对确保其代码遵循 React 规则感兴趣的开发人员，我们建议 [启用严格模式](/reference/react/StrictMode) 并 [配置 React 的 ESLint 插件](/learn/editor-setup#linting)。这些工具可以帮助捕获 React 代码中的微妙错误，提高应用程序的质量，并为即将推出的功能（如 React 编译器）做好准备。我们还正在努力整理 React 规则的综合文档并更新我们的 ESLint 插件，以帮助团队理解和应用这些规则，从而创建更健壮的应用程序。

欢迎查看我们 [去年秋季的演讲](https://www.youtube.com/watch?v=qOQClO3g8-Y) 以查看编译器的实际效果。在演讲时，我们从尝试在 instagram.com 的一个页面上使用 React 编译器获取了早期的实验数据。自那时以来，我们已将编译器推广到了 instagram.com 的生产环境。我们还扩大了团队规模，加快了在 Meta 的其他平台和开源的推出速度。我们对未来的道路充满期待，并将在未来几个月内分享更多内容。

## Action {/*actions*/}


我们 [之前分享过](/blog/2023/03/22/react-labs-what-we-have-been-working-on-march-2023#react-server-components)，我们正在探索使用服务器操作将数据从客户端发送到服务器的解决方案，以便可以执行数据库变更和实现表单。在开发 Server Action 期间，我们扩展了这些 API，以支持仅客户端应用程序中的数据处理。

我们将含有此更广泛含义的操作称为 Action。Action 允许将一个函数传递给诸如 [`<form/>`](/reference/react-dom/components/form) 等 DOM 元素：

```js
<form action={search}>
  <input name="query" />
  <button type="submit">搜索</button>
</form>
```

`action` 函数可以同步或异步执行。你可以在客户端使用标准 JavaScript 定义它们，也可以在服务器上使用 [`'use server'`](/reference/rsc/use-server) 指示符。当使用 action 时，React 将帮助管理数据提交的生命周期，提供类似 [`useFormStatus`](/reference/react-dom/hooks/useFormStatus) 和 [`useActionState`](/reference/react/useActionState) 的 Hook，以访问表单操作的当前 state 与响应。

默认情况下，Action 在 [transition](/reference/react/useTransition) 中提交，使当前页面在操作处理过程中保持交互性。由于 Action 支持异步函数，我们还添加了在 transitions 中使用 `async/await` 的功能，这允许在异步请求（如 `fetch`）开始时使用转换的 `isPending` 状态显示待处理 UI，并在应用更新时始终显示待处理 UI。

除了 Action，我们还引入了一个名为 [`useOptimistic`](/reference/react/useOptimistic) 的功能，用于管理乐观状态更新。使用此 Hook 可以应用临时更新，一旦最终状态提交，它们就会自动回滚。对于 Action，这将帮助乐观地设置客户端数据的最终状态，假设提交成功，并恢复为从服务器接收到的数据值。它使用常规的 `async`/`await`，因此无论是在客户端上使用 `fetch` 还是在服务器上使用 Server Action，都可以工作。

库作者可以使用 `useTransition` 在自己的组件中实现自定义 `action={fn}` props。我们的目的是，当设计他们的组件 API 时，库应采用 Action 模式，为 React 开发人员提供一致的体验。例如，如果你的库提供了一个 `<Calendar onSelect={eventHandler}>` 组件，则还可以考虑暴露一个 `<Calendar selectAction={action}>` API。

尽管我们最初专注于 Server Action 用于客户端/服务器数据传输，但我们对 React 的理念是在所有平台和环境中提供相同的编程模型。在可能的情况下，如果我们在客户端引入一个功能，我们也会使它在服务器上起作用，反之亦然。这一理念使我们能够创建一组 API，无论你的应用在何处运行，都可以工作，从而使以后更容易升级到不同的环境。

Action 现在在 Canary 渠道中可用，并将在下一个 React 发布版本中发布。

## React Canary 版本中的新特性 {/*new-features-in-react-canary*/}

我们将 [React Canaries](/blog/2023/05/03/react-canaries) 作为一个选项引入，可以在它们的设计接近完成时立即采用个别新的稳定功能，然后再发布到稳定的 semver 版本中。

Canaries 是我们开发 React 的一种变化。以前，功能会在 Meta 内部进行研究和构建，因此用户只会在发布到 Stable 时看到最终成品。通过 Canaries，我们正在社区的帮助下公开构建，以完成我们在 React Labs 博客系列中分享的功能。这意味着开发者能够更早地了解新功能，因为它们正在完成而不是已经完成。

React 服务器组件、资源加载、文档元数据与 Action 都已经加入了 React Canary，并且我们已经在 react.dev 上为这些功能添加了文档：

- **指示符**：[`"use client"`](/reference/rsc/use-client) 与 [`"use server"`](/reference/rsc/use-server) 是设计用于全栈 React 框架的打包功能。它们标记了两个环境之间的“分割点”：use client 指示符指示打包工具生成一个 `<script>` 标签（类似于 [Astro Islands](https://docs.astro.build/en/concepts/islands/#creating-an-island)），而 use server 告诉打包工具生成一个 POST 端点（类似于 [tRPC Mutations](https://trpc.io/docs/concepts)）。它们让你可以编写将客户端交互性与相关的服务器端逻辑组合在一起的可重用组件。

- **文档元数据**：我们内置支持在组件树中的任何位置渲染 [`<title>`](/reference/react-dom/components/title)、[`<meta>`](/reference/react-dom/components/meta) 和元数据 [`<link>`](/reference/react-dom/components/link) 标签。这些在所有环境中都以相同的方式工作，包括完全客户端代码、SSR 和 RSC。这为像 [React Helmet](https://github.com/nfl/react-helmet) 这样的库开创的功能提供了内置支持。

- **资源加载**：我们将 Suspense 与样式表、字体和脚本等资源的加载生命周期集成在一起，以便 React 考虑它们来确定像 [`<style>`](/reference/react-dom/components/style)、[`<link>`](/reference/react-dom/components/link) 和 [`<script>`](/reference/react-dom/components/script) 这样的元素中的内容是否已准备就绪。我们还添加了新的 [资源加载 API](/reference/react-dom#resource-preloading-apis)，如 `preload` 和 `preinit`，以提供更大的控制权，指示何时应加载和初始化资源。

- **Action**：如上所述，我们已将 Action 添加到管理从客户端发送数据到服务器的功能中。现在可以将 `action` 添加到像 [`<form/>`](/reference/react-dom/components/form) 这样的元素中，使用 [`useFormStatus`](/reference/react-dom/hooks/useFormStatus) 访问状态，使用 [`useActionState`](/reference/react/useActionState) 处理结果，并使用 [`useOptimistic`](/reference/react/useOptimistic) 乐观地更新 UI。

由于所有这些功能是相互配合的，因此单独在稳定渠道中发布它们是困难的。发布 Action 而不带有用于访问表单状态的补充 Hook 会限制 Action 的实际可用性。引入 React 服务器组件而不集成 Server Action 会把在服务器上修改数据变得复杂化。

在我们可以将一组功能发布到稳定渠道之前，我们需要确保它们能够协同工作，并且开发人员拥有在生产环境中使用它们所需的一切。React Canaries 允许我们逐个开发这些功能，并逐步释放稳定的 API，直到整个功能集完成。

目前在 React Canary 中的功能已经完整并且准备发布。

## React 的下一个主要版本 {/*the-next-major-version-of-react*/}

经过几年的迭代，`react@canary` 现在已经准备好发布到 `react@latest`。上面提到的新功能与应用程序运行的任何环境兼容，提供了生产使用所需的一切。由于资源加载与文档元数据可能对一些应用程序造成破坏性变化，因此下一个 React 版本将是一个主要版本：**React 19**。

我们仍然需要做更多准备工作才能发布。在 React 19 中，我们还将添加一些长期请求的改进，这些改进需要进行破坏性更改，如支持 Web Components。我们现在的重点是完成这些改进、为新功能制定最终文档，并发布关于包含哪些内容的公告。

在接下来的几个月中，我们将分享有关 React 19 包含的所有内容、如何采用新的客户端功能以及如何为 React 服务器组件构建支持的更多信息。

## Offscreen（已经重命名为 Activity） {/*offscreen-renamed-to-activity*/}

自上次更新以来，我们已经将我们正在研究的一个功能从“Offscreen”重命名为“Activity”。“Offscreen”意味着它仅适用于不可见的应用程序部分，但在研究该功能时，我们意识到应用程序的某些部分可能是可见但不活动的，例如模态框后面的内容。新名称更贴近于标记应用程序的某些部分为“active”或“inactive”的行为。

Activity 仍处于研究阶段，我们剩下的工作是最终确定向库开发人员公开的基本原语。在我们专注于发布更完整功能的同时，我们已将此领域的优先级降低。

* * *

除了此更新之外，我们的团队还在会议上发表了演讲并在播客中露面，更多地讲述我们的工作并回答问题。

- [Sathya Gunasekaran](https://github.com/gsathya) 在 [React India](https://www.youtube.com/watch?v=kjOacmVsLSE) 大会上介绍了 React 编译器。

- [Dan Abramov](/community/team#dan-abramov) 在 [RemixConf](https://www.youtube.com/watch?v=zMf_xeGPn6s) 上发表了名为“React from Another Dimension”的演讲，探讨了 React 服务器组件与 Action 可能是如何创建的另一种历史。

- [Dan Abramov](/community/team#dan-abramov) 在 [the Changelog’s JS Party podcast](https://changelog.com/jsparty/311) 上接受了关于 React 服务器组件的采访

- [Matt Carroll](/community/team#matt-carroll) 在 [Front-End Fire podcast](https://www.buzzsprout.com/2226499/14462424-interview-the-two-reacts-with-rachel-nabors-evan-bacon-and-matt-carroll) 上接受了采访，他讨论了 [The Two Reacts](https://overreacted.io/the-two-reacts/)。

感谢 [Lauren Tan](https://twitter.com/potetotes)、[Sophie Alpert](https://twitter.com/sophiebits)、[Jason Bonta](https://threads.net/someextent)、[Eli White](https://twitter.com/Eli_White) 和 [Sathya Gunasekaran](https://twitter.com/_gsathya) 对本文的审核。

感谢你的阅读，期待在 [React Conf](https://conf.react.dev/) 见到你！

---
# Source: react-conf-2024-recap.md
---
---
title: "回顾 React Conf 2024"
author: Ricky Hanlon
date: 2024/05/22
description: 上周我们在内华达州亨德森举办了为期两天的 React Conf 2024 大会，有 700 多名与会者亲临现场，讨论 UI 工程领域的最新进展。在这篇文章中，我们将总结这次活动的演讲和公告。
---

2024 年 5 月 22 日 [Ricky Hanlon](https://twitter.com/rickhanlonii)

---

<Intro>

上周我们在内华达州亨德森举办了为期两天的 React Conf 2024 大会，有 700 多名与会者亲临现场，讨论 UI 工程领域的最新进展。这是我们自 2019 年以来首次举办线下会议，我们很高兴能够再次将社区团结在一起。

</Intro>

---

在 React Conf 2024 上，我们宣布了 [React 19 RC](/blog/2024/12/05/react-19)、[React Native 新架构 Beta 版](https://github.com/reactwg/react-native-new-architecture/discussions/189)，以及 [React 编译器](/learn/react-compiler) 的实验版本。社区同时登台宣布了 [React Router v7](https://remix.run/blog/merging-remix-and-react-router)、Expo Router 中的 [通用服务器组件](https://www.youtube.com/watch?v=T8TZQ6k4SLE&t=20765s)、[RedwoodJS](https://redwoodjs.com/blog/rsc-now-in-redwoodjs) 中的 React 服务器组件等等。

完整的 [第一天](https://www.youtube.com/watch?v=T8TZQ6k4SLE) 和 [第二天](https://www.youtube.com/watch?v=0ckOUBiuxVY) 的直播已经可以在线观看了。在这篇文章中，我们将总结活动中的演讲和公告。

## 第一天 {/*day-1*/}

_[点击这里观看第一天完整直播。](https://www.youtube.com/watch?v=T8TZQ6k4SLE&t=973s)_

第一天由 Meta 的首席技术官 [Andrew "Boz" Bosworth](https://www.threads.net/@boztank) 发表欢迎致辞，随后由 Meat 的 React 组织负责人 [Seth Webster](https://twitter.com/sethwebster) 以及主持人 [Ashley Narcisse](https://twitter.com/_darkfadr) 进行演讲。

在第一天的主题演讲中，[Joe Savona](https://twitter.com/en_JS) 分享了我们对 React 的目标和愿景：帮助任何人更加轻松构建卓越的用户体验。[Lauren Tan](https://twitter.com/potetotes) 随后带来了 React 的现状报告：React 在 2023 年下载量超过 10 亿次，并且有 37% 的新开发者通过 React 学习编程。最后她强调，是 React 社区成就了 React 的今天。

更多内容，请查看会议随后带来的来自社区的演讲：

- [原生 React](https://www.youtube.com/watch?v=T8TZQ6k4SLE&t=5542s)，来自 [Ryan Florence](https://twitter.com/ryanflorence)
- [React 节奏布鲁斯](https://www.youtube.com/watch?v=0ckOUBiuxVY&t=12728s)，来自 [Lee Robinson](https://twitter.com/leeerob)
- [RedwoodJS 现已支持 React 服务器组件](https://www.youtube.com/watch?v=T8TZQ6k4SLE&t=26815s)，来自 [Amy Dutton](https://twitter.com/selfteachme)
- [介绍 Expo Router 中的通用 React 服务器组件](https://www.youtube.com/watch?v=T8TZQ6k4SLE&t=20765s)，来自 [Evan Bacon](https://twitter.com/Baconbrix)

接下来的主题演讲中，[Josh Story](https://twitter.com/joshcstory) 和 [Andrew Clark](https://twitter.com/acdlite) 分享了 React 19 即将推出的新功能，并宣布了 React 19 RC，该版本已准备好用于生产环境测试。你可以在 [React 19 RC](/blog/2024/12/05/react-19) 这篇文章中查看 React 19 的全部功能，也可以查看以下关于新功能深入分析的演讲：

- [React 19 有哪些更新](https://www.youtube.com/watch?v=T8TZQ6k4SLE&t=8880s)，来自 [Lydia Hallie](https://twitter.com/lydiahallie)
- [React 解读：React 19 路线图](https://www.youtube.com/watch?v=T8TZQ6k4SLE&t=10112s)，来自 [Sam Selikoff](https://twitter.com/samselikoff)
- [React 19 深入：协调 HTML](https://www.youtube.com/watch?v=T8TZQ6k4SLE&t=24916s)，来自 [Josh Story](https://twitter.com/joshcstory)
- [使用 React 服务器组件增强表单](https://www.youtube.com/watch?v=0ckOUBiuxVY&t=25280s)，来自 [Aurora Walberg Scharff](https://twitter.com/aurorascharff)
- [为两台计算机设计的 React](https://www.youtube.com/watch?v=T8TZQ6k4SLE&t=18825s)，来自 [Dan Abramov](https://bsky.app/profile/danabra.mov)
- [现在你应该理解了 React 服务器组件](https://www.youtube.com/watch?v=0ckOUBiuxVY&t=11256s)，来自 [Kent C. Dodds](https://twitter.com/kentcdodds)

最后，[Joe Savona](https://twitter.com/en_JS)、[Sathya Gunasekaran](https://twitter.com/_gsathya) 和 [Mofei Zhang](https://twitter.com/zmofei) 宣布 React 编译器现已 [开源](https://github.com/facebook/react/pull/29061)，并分享了一个实验版本的 React 编译器供大家尝试。

有关使用 React Compile 及其工作原理的更多信息，请查看[文档](/learn/react-compiler)以及如下演讲：

- [忘了 Memo 吧](https://www.youtube.com/watch?v=T8TZQ6k4SLE&t=12020s)，来自 [Lauren Tan](https://twitter.com/potetotes)
- [深入解析 React 编译器](https://www.youtube.com/watch?v=0ckOUBiuxVY&t=9313s)，来自 [Sathya Gunasekaran](https://twitter.com/_gsathya) 和 [Mofei Zhang](https://twitter.com/zmofei)

观看完整的第一天主题演讲：

<YouTubeIframe src="https://www.youtube.com/embed/T8TZQ6k4SLE?t=973s" />

## 第二天 {/*day-2*/}

_[点击这里观看第二天完整直播。](https://www.youtube.com/watch?v=0ckOUBiuxVY&t=1720s)_

第二天由 [Seth Webster](https://twitter.com/sethwebster) 发表欢迎致辞，随后是 [Eli White](https://x.com/Eli_White) 的感谢致辞，以及我们的首席氛围官 [Ashley Narcisse](https://twitter.com/_darkfadr) 的介绍。

在第二天的主题演讲中，[Nicola Corti](https://twitter.com/cortinico) 分享了 React Native 的现状，包括 2023 年的 7800 万次下载量。他还强调了使用 React Native 的应用，包括了 Meta 内部使用的 2000 多个页面；Facebook 市场中的产品详情页面，该页面每天访问量超过 20 亿次；以及微软 Windows 开始菜单的一些部分，和几乎每个微软 Office 产品的移动和桌面版本中的一些功能。

Nicola 还强调了社区为支持 React Native 所做的所有工作，包括库、框架和多平台。更多内容，请查看来自社区的这些演讲：

- [React Native，不仅仅是移动和桌面应用](https://www.youtube.com/watch?v=0ckOUBiuxVY&t=5798s)，来自 [Chris Traganos](https://twitter.com/chris_trag) 和 [Anisha Malde](https://twitter.com/anisha_malde)
- [使用 React 进行空间计算](https://www.youtube.com/watch?v=0ckOUBiuxVY&t=22525s)，来自 [Michał Pierzchała](https://twitter.com/thymikee)

[Riccardo Cipolleschi](https://twitter.com/cipolleschir) 继续第二天的主题演讲，他宣布 React Native 新架构现已进入 Beta 阶段，并准备好在生产环境中使用。他分享了新架构中的新功能和改进，并分享了 React Native 未来的路线图。更多内容，请查看：

- [跨平台 React](https://www.youtube.com/watch?v=0ckOUBiuxVY&t=26569s)，来自 [Olga Zinoveva](https://github.com/SlyCaptainFlint) 和 [Naman Goel](https://twitter.com/naman34)

在接下来在主题演讲中，Nicola 宣布官方建议所有使用 React Native 创建的新应用都使用 Expo 这样的框架启动。与此同时他还宣布了全新的 React Native 主页和入门文档。可以在 [React Native docs](https://reactnative.dev/docs/next/environment-setup) 中查看新的入门指南。

最后，在本次主题演讲的末尾，[Kadi Kraman](https://twitter.com/kadikraman) 分享了 Expo 的最新功能和改进，以及如何使用 Expo 开始 React Native 开发。

观看完整的第二天主题演讲：

<YouTubeIframe src="https://www.youtube.com/embed/0ckOUBiuxVY?t=1720s" />

## 问答环节 {/*q-and-a*/}

React 和 React Native 团队也在每天结束时进行了问答环节：

- [React 问答](https://www.youtube.com/watch?v=T8TZQ6k4SLE&t=27518s) 由 [Michael Chan](https://twitter.com/chantastic) 主持
- [React Native 问答](https://www.youtube.com/watch?v=0ckOUBiuxVY&t=27935s) 由 [Jamon Holmgren](https://twitter.com/jamonholmgren) 主持

## 还有更多... {/*and-more*/}

大会还进行了关于可访问性、错误报告、CSS 等方面的演讲：

- [揭秘 React 应用中的可访问性](https://www.youtube.com/watch?v=0ckOUBiuxVY&t=20655s)，来自 [Kateryna Porshnieva](https://twitter.com/krambertech)
- [Pigment CSS，服务器组件时代的 CSS](https://www.youtube.com/watch?v=0ckOUBiuxVY&t=21696s)，来自 [Olivier Tassinari](https://twitter.com/olivtassinari)
- [实时 React 服务器组件](https://www.youtube.com/watch?v=T8TZQ6k4SLE&t=24070s)，来自 [Sunil Pai](https://twitter.com/threepointone)
- [打破 React 规则](https://www.youtube.com/watch?v=T8TZQ6k4SLE&t=25862s)，来自 [Charlotte Isambert](https://twitter.com/c_isambert)
- [解决 100% 的错误](https://www.youtube.com/watch?v=0ckOUBiuxVY&t=19881s)，来自 [Ryan Albrecht](https://github.com/ryan953)

## 致谢 {/*thank-you*/}

感谢所有使 React Conf 2024 成为可能的工作人员、演讲者和参与者。感谢名单太长不能一一列出，但我们想特别感谢一些人。

感谢 [Barbara Markiewicz](https://twitter.com/barbara_markie)、[Callstack](https://www.callstack.com/) 团队和我们的 React 团队开发者倡导者 [Matt Carroll](https://twitter.com/mattcarrollcode) 帮助策划整个活动；感谢 [Sunny Leggett](https://zeroslopeevents.com/about) 和 [Zero Slope](https://zeroslopeevents.com) 的所有人帮助组织活动。

感谢 [Ashley Narcisse](https://twitter.com/_darkfadr) 担任我们的主持人和首席氛围官；感谢 [Michael Chan](https://twitter.com/chantastic) 和 [Jamon Holmgren](https://twitter.com/jamonholmgren) 主持问答环节。

感谢 [Seth Webster](https://twitter.com/sethwebster) 和 [Eli White](https://x.com/Eli_White) 每天欢迎我们，并提供结构和内容方面的指导；感谢 [Tom Occhino](https://twitter.com/tomocchino) 在聚会后加入我们，并发表特别讯息。

感谢 [Ricky Hanlon](https://www.youtube.com/watch?v=FxTZL2U-uKg&t=1263s) 提供关于演讲的详细反馈，设计幻灯片，以及总体上填补细节方面的空缺。

感谢 [Callstack](https://www.callstack.com/) 建设大会网站；感谢 [Kadi Kraman](https://twitter.com/kadikraman) 和 [Expo](https://expo.dev/) 团队建设大会移动应用。

感谢所有赞助商使本次活动得以实现：[Remix](https://remix.run/)、[Amazon](https://developer.amazon.com/apps-and-games?cmp=US_2024_05_3P_React-Conf-2024&ch=prtnr&chlast=prtnr&pub=ref&publast=ref&type=org&typelast=org)、[MUI](https://mui.com/)、[Sentry](https://sentry.io/for/react/?utm_source=sponsored-conf&utm_medium=sponsored-event&utm_campaign=frontend-fy25q2-evergreen&utm_content=logo-reactconf2024-learnmore)、[Abbott](https://www.jobs.abbott/software)、[Expo](https://expo.dev/)、[RedwoodJS](https://rwsdk.com/) 以及 [Vercel](https://vercel.com)。

感谢音视频团队为我们提供的视觉、舞台和声音；感谢威斯汀酒店为我们提供的住宿。

感谢所有与社区分享他们的知识和经验的演讲者。

最后，感谢所有现场以及在线参加大会的每一位。是你们成就了 React 的今天。React 不仅仅是一个库，它更是一个社区，看到大家聚在一起分享和共同学习真是鼓舞人心。

下次见！


---
# Source: introducing-react-dev.md
---
---
title: "介绍 react.dev"
author: Dan Abramov and Rachel Nabors
date: 2023/03/16
description: 今天，我们非常高兴推出 react.dev，React 及其文档的新家。在本文中，我们想带你参观新网站。
---

2023 年 3 月 16 日 [Dan Abramov](https://bsky.app/profile/danabra.mov) 与 [Rachel Nabors](https://twitter.com/rachelnabors)

---

<Intro>

今天，我们非常高兴推出 react.dev，React 及其文档的新家。在本文中，我们想带你参观新网站。

</Intro>

---

## tl;dr {/*tldr*/}

* 新的 React 文档网站（[react.dev](https://react.dev)）将介绍使用函数式组件和 Hook 的现代 React。
* 新网站包括了图表、插图、挑战和超过 600 个新的交互式示例。
* 旧的 React 文档网站现在已经迁移到 [legacy.reactjs.org](https://legacy.reactjs.org)。

## 新网站，新域名，新主页 {/*new-site-new-domain-new-homepage*/}

首先，介绍一些小的背景。

为了庆祝新文档的发布，更重要的是为了清晰区分新旧内容，我们已经将域名更改为更短的 [react.dev](https://react.dev)；旧的 [reactjs.org](https://reactjs.org) 域名现在将重定向到此处。

旧的 React 文档现在已经存档于 [legacy.reactjs.org](https://legacy.reactjs.org)。以避免“破坏网络”，所有现有的指向旧内容的链接将自动重定向到那里，但是旧网站将不会再得到新的更新。

不敢相信，React 很快就要十岁了。在 JavaScript 的年代里，这就像整整一个世纪！我们 [更新了 React 主页](https://react.dev)，以反映我们为什么认为 React 是创建用户界面的绝佳方式，并更新了入门指南，更突出地提到基于现代 React 的框架。

如果你还没有看过新主页，请快去看看！

## 进入使用 Hook 的现代 React {/*going-all-in-on-modern-react-with-hooks*/}

当 React 在 2018 年发布 Hook 时，Hook 文档假定读者熟悉类组件。这有助于社区非常迅速地采用 Hook，但是一段时间后，旧的文档无法为新读者服务，因为新读者不得不学习两次 React：一次是使用类式组件，然后再学习在函数式组件中使用 Hook。

**新文档从一开始就使用 Hook 来介绍 React**。新文档分为两个主要部分：

* **[学习 React](/learn)** 是一个自学课程，从头开始介绍 React。
* **[API 参考](/reference)** 提供了每个 React API 的详细信息和使用示例。

让我们更仔细地看看可以从每个部分中找到什么。

<Note>

仍有一些罕见的类式组件尚未有基于 Hook 的替代品。React 仍然支持类式组件，并且在新网站的 [legacy API](/reference/react/legacy) 部分中有文档记录。

</Note>

## 快速入门 {/*quick-start*/}

学习部分从 [快速入门](/learn) 页面开始。它是 React 的一个简短介绍性导览，介绍了诸如组件、props 和 state 等概念，但并不详细介绍如何使用它们。

如果你喜欢通过实践来学习，我们建议你接下来查看 [井字棋教程](/learn/tutorial-tic-tac-toe)。它会带领你一步步构建一个小游戏，同时介绍你每天都会用到的技能。这是你将要构建的内容：

<Sandpack>

```js src/App.js
import { useState } from 'react';

function Square({ value, onSquareClick }) {
  return (
    <button className="square" onClick={onSquareClick}>
      {value}
    </button>
  );
}

function Board({ xIsNext, squares, onPlay }) {
  function handleClick(i) {
    if (calculateWinner(squares) || squares[i]) {
      return;
    }
    const nextSquares = squares.slice();
    if (xIsNext) {
      nextSquares[i] = 'X';
    } else {
      nextSquares[i] = 'O';
    }
    onPlay(nextSquares);
  }

  const winner = calculateWinner(squares);
  let status;
  if (winner) {
    status = 'Winner: ' + winner;
  } else {
    status = 'Next player: ' + (xIsNext ? 'X' : 'O');
  }

  return (
    <>
      <div className="status">{status}</div>
      <div className="board-row">
        <Square value={squares[0]} onSquareClick={() => handleClick(0)} />
        <Square value={squares[1]} onSquareClick={() => handleClick(1)} />
        <Square value={squares[2]} onSquareClick={() => handleClick(2)} />
      </div>
      <div className="board-row">
        <Square value={squares[3]} onSquareClick={() => handleClick(3)} />
        <Square value={squares[4]} onSquareClick={() => handleClick(4)} />
        <Square value={squares[5]} onSquareClick={() => handleClick(5)} />
      </div>
      <div className="board-row">
        <Square value={squares[6]} onSquareClick={() => handleClick(6)} />
        <Square value={squares[7]} onSquareClick={() => handleClick(7)} />
        <Square value={squares[8]} onSquareClick={() => handleClick(8)} />
      </div>
    </>
  );
}

export default function Game() {
  const [history, setHistory] = useState([Array(9).fill(null)]);
  const [currentMove, setCurrentMove] = useState(0);
  const xIsNext = currentMove % 2 === 0;
  const currentSquares = history[currentMove];

  function handlePlay(nextSquares) {
    const nextHistory = [...history.slice(0, currentMove + 1), nextSquares];
    setHistory(nextHistory);
    setCurrentMove(nextHistory.length - 1);
  }

  function jumpTo(nextMove) {
    setCurrentMove(nextMove);
  }

  const moves = history.map((squares, move) => {
    let description;
    if (move > 0) {
      description = 'Go to move #' + move;
    } else {
      description = 'Go to game start';
    }
    return (
      <li key={move}>
        <button onClick={() => jumpTo(move)}>{description}</button>
      </li>
    );
  });

  return (
    <div className="game">
      <div className="game-board">
        <Board xIsNext={xIsNext} squares={currentSquares} onPlay={handlePlay} />
      </div>
      <div className="game-info">
        <ol>{moves}</ol>
      </div>
    </div>
  );
}

function calculateWinner(squares) {
  const lines = [
    [0, 1, 2],
    [3, 4, 5],
    [6, 7, 8],
    [0, 3, 6],
    [1, 4, 7],
    [2, 5, 8],
    [0, 4, 8],
    [2, 4, 6],
  ];
  for (let i = 0; i < lines.length; i++) {
    const [a, b, c] = lines[i];
    if (squares[a] && squares[a] === squares[b] && squares[a] === squares[c]) {
      return squares[a];
    }
  }
  return null;
}
```

```css src/styles.css
* {
  box-sizing: border-box;
}

body {
  font-family: sans-serif;
  margin: 20px;
  padding: 0;
}

.square {
  background: #fff;
  border: 1px solid #999;
  float: left;
  font-size: 24px;
  font-weight: bold;
  line-height: 34px;
  height: 34px;
  margin-right: -1px;
  margin-top: -1px;
  padding: 0;
  text-align: center;
  width: 34px;
}

.board-row:after {
  clear: both;
  content: '';
  display: table;
}

.status {
  margin-bottom: 10px;
}
.game {
  display: flex;
  flex-direction: row;
}

.game-info {
  margin-left: 20px;
}
```

</Sandpack>

我们还想强调一下 [React 哲学](/learn/thinking-in-react) ——这是许多人理解 React 的教程。**我们使用了函数式组件和 Hook 更新了这两个经典教程**。

<Note>

上面的例子使用了 sandbox。我们在整个网站上添加了超过 600 个 sandbox。你可以编辑所有的 sandbox，或者点击右上角的 Fork 按钮，然后在单独的标签页中打开它。sandbox 可以让你快速体验 React API，探索你的想法并检查你的理解。

</Note>

## 一步步学习 React {/*learn-react-step-by-step*/}

我们希望世界上每个人都有平等机会自学 React。

这就是为什么“学习”部分被组织成一个自学课程的章节。前两章描述了 React 的基本知识。如果你是初次尝试 React，或者想要刷新你对 React 的记忆，可以从这里开始：

- **[描述 UI](/learn/describing-the-ui)** 章节介绍了如何使用组件显示信息。
- **[添加交互性](/learn/adding-interactivity)** 章节介绍了如何在响应用户输入时更新屏幕。

接下来的两章持续深入，将带你了解更棘手的部分：

- **[管理状态](/learn/managing-state)** 章节介绍了如何在应用程序变得越来越复杂时组织逻辑。
- **[脱围机制](/learn/escape-hatches)** 章节介绍了如何“走出”React，并在何时做出最明智的决策。

每个章节都由几个相关的页面组成。其中大部分页面将介绍特定的技能或技术，例如 [使用 JSX 编写标记](/learn/writing-markup-with-jsx)、[更新状态中的对象](/learn/updating-objects-in-state) 或 [在组件间共享状态](/learn/sharing-state-between-components)。一些页面聚焦于解释一个概念，例如 [渲染和提交](/learn/render-and-commit) 或 [将状态作为快照（snapshot）](/learn/state-as-a-snapshot)。还有一些页面如 [你可能不需要 Effect](/learn/you-might-not-need-an-effect) 是基于我们多年的经验而分享的建议。

你不必完全按顺序阅读这些章节，谁有这个时间呢？！不过也许你可以。学习部分的页面只依赖于早期页面介绍的概念。如果你想像读书一样阅读它，那就去吧！

### 使用挑战（challenge）检查你的理解 {/*check-your-understanding-with-challenges*/}

“学习”章节的大多数页面都以一些挑战结尾，以检查你的理解情况。例如以下是有关 [条件渲染](/learn/conditional-rendering#challenges) 页面上的一些挑战。

除非你真的如此想，不然不必现在就解决它们！

<Challenges noTitle={true}>

#### 使用 `? :` 显示不完整 item 的图标 {/*show-an-icon-for-incomplete-items-with--*/}

如果 `isPacked` 不为 `true`，使用条件运算符（`cond ? a : b`）渲染 ❌。

<Sandpack>

```js
function Item({ name, isPacked }) {
  return (
    <li className="item">
      {name} {isPacked && '✅'}
    </li>
  );
}

export default function PackingList() {
  return (
    <section>
      <h1>Sally Ride's Packing List</h1>
      <ul>
        <Item 
          isPacked={true} 
          name="Space suit" 
        />
        <Item 
          isPacked={true} 
          name="Helmet with a golden leaf" 
        />
        <Item 
          isPacked={false} 
          name="Photo of Tam" 
        />
      </ul>
    </section>
  );
}
```

</Sandpack>

<Solution>

<Sandpack>

```js
function Item({ name, isPacked }) {
  return (
    <li className="item">
      {name} {isPacked ? '✅' : '❌'}
    </li>
  );
}

export default function PackingList() {
  return (
    <section>
      <h1>Sally Ride's Packing List</h1>
      <ul>
        <Item 
          isPacked={true} 
          name="Space suit" 
        />
        <Item 
          isPacked={true} 
          name="Helmet with a golden leaf" 
        />
        <Item 
          isPacked={false} 
          name="Photo of Tam" 
        />
      </ul>
    </section>
  );
}
```

</Sandpack>

</Solution>

#### 使用 `&&` 展示 item 的重要性 {/*show-the-item-importance-with-*/}

在这个例子中，每个 `Item` 组件都会接收一个数字类型的 `importance` 属性。使用 `&&` 运算符来渲染斜体 "_(Importance: X)_"，但只有在 `importance` 属性不为零时才渲染。你的列表应该看起来像下面一样：

* Space suit _(Importance: 9)_
* Helmet with a golden leaf
* Photo of Tam _(Importance: 6)_

不要忘记在 label 之间添加一个空格！

<Sandpack>

```js
function Item({ name, importance }) {
  return (
    <li className="item">
      {name}
    </li>
  );
}

export default function PackingList() {
  return (
    <section>
      <h1>Sally Ride's Packing List</h1>
      <ul>
        <Item 
          importance={9} 
          name="Space suit" 
        />
        <Item 
          importance={0} 
          name="Helmet with a golden leaf" 
        />
        <Item 
          importance={6} 
          name="Photo of Tam" 
        />
      </ul>
    </section>
  );
}
```

</Sandpack>

<Solution>

应该这样来实现：

<Sandpack>

```js
function Item({ name, importance }) {
  return (
    <li className="item">
      {name}
      {importance > 0 && ' '}
      {importance > 0 &&
        <i>(Importance: {importance})</i>
      }
    </li>
  );
}

export default function PackingList() {
  return (
    <section>
      <h1>Sally Ride's Packing List</h1>
      <ul>
        <Item 
          importance={9} 
          name="Space suit" 
        />
        <Item 
          importance={0} 
          name="Helmet with a golden leaf" 
        />
        <Item 
          importance={6} 
          name="Photo of Tam" 
        />
      </ul>
    </section>
  );
}
```

</Sandpack>

请注意，你必须写成 `importance > 0 && ...` 而不是 `importance && ...`，这样如果 `importance` 的值为 `0` 时，就不会将 `0` 作为结果进行渲染！

在这个解决方案中，使用了两个独立的条件来在名称和 importance label 之间插入一个空格。或者，你可以使用带有前导空格的 Fragment：`importance > 0 && <> <i>...</i></>`，或者在 `<i>` 标签内立即添加一个空格：`importance > 0 && <i> ...</i>`。

</Solution>

</Challenges>

请注意左下角的“显示解决方案”按钮。如果你想要检查自己的代码，它会很有用！

### 通过图表和插图来建立直觉 {/*build-an-intuition-with-diagrams-and-illustrations*/}

当我们无法弄清楚如何仅用代码和文字来解释某些内容时，我们添加了有助于提供一些直觉的图表。例如，下面是 [保存和重置 state](/learn/preserving-and-resetting-state) 中的图表之一：

<Diagram name="preserving_state_diff_same_pt1" height={350} width={794} alt="图表包含三个部分，每个部分之间有一个箭头过渡。 第一部分包含一个标记为 `div` 的 React 组件，其中有一个标记为 `section` 的子组件，该组件有一个标记为 `Counter` 的子组件，其中包含一个标记为 `count`、值为 3 的 state 气泡。中间部分具有相同的 `div` 父组件，但子组件现已被删除，由黄色“proof”图像指示。第三部分再次具有相同的 `div` 父级，现在有一个由黄色突出显示并且标记为 `div` 的新子级，还有一个标记为 `Counter` 的新子级，其中包含一个标记为 `count` 且值为 0 的 state 气泡。她们都使用黄色进行了高亮。">

当 `section` 被改变为 `div` 时，`section` 会被删除而新的 `div` 会被添加。

</Diagram>

在文档中还有一些插图——这是其中一个 [浏览器绘制屏幕的示意图](/learn/render-and-commit#epilogue-browser-paint)。

<Illustration alt="浏览器正在绘制“带有卡片元素的静物画”" src="/images/docs/illustrations/i_browser-paint.png" />

我们已经与浏览器厂商确认，这个描绘是 100% 科学准确的。

## 新的并且更细致的 API 参考 {/*a-new-detailed-api-reference*/}

在 [API 参考](/reference/react) 中，每个 React API 现在都有一个专门的页面。这包括各种类型的 API：

- 内置 Hook，比如 [`useState`](/reference/react/useState)。
- 内置组件，比如 [`<Suspense>`](/reference/react/Suspense)。
- 内置浏览器组件，比如 [`<input>`](/reference/react-dom/components/input)。
- 面向框架的 API，比如 [`renderToPipeableStream`](/reference/react-dom/server/renderToReadableStream)。
- 其他 React API，比如 [`memo`](/reference/react/memo)。

你会注意到，每个 API 页面至少被分成两个部分：**参考** 和 **用法**。

[参考](/reference/react/useState#reference) 通过列举参数与返回值描述了正式的 API。这一部分比较简洁，但如果你不熟悉该 API，你可能会感觉有点抽象。“参考”描述了一个 API 做什么，但不是如何使用它。

[用法](/reference/react/useState#usage) 展示了为什么需要以及如何在实践中使用这个 API，就像同事或朋友可能会解释的那样。它展示了 React 团队设计每个 API 的 **典型使用场景**。我们添加了彩色代码片段、使用不同 API 的示例以及可以复制和粘贴的示例。

<Recipes titleText="useState 的基础示例" titleId="examples-basic">

#### 数字计数 {/*counter-number*/}

在这个例子中，`count` state 变量保存了一个数字。点击按钮会将其递增。

<Sandpack>

```js
import { useState } from 'react';

export default function Counter() {
  const [count, setCount] = useState(0);

  function handleClick() {
    setCount(count + 1);
  }

  return (
    <button onClick={handleClick}>
      你点击了 {count} 次
    </button>
  );
}
```

</Sandpack>

<Solution />

#### 输入文本（字符串） {/*text-field-string*/}

在这个例子中，`text` state 变量保存一个字符串。当你输入时，`handleChange` 从浏览器输入 DOM 元素中读取最新的输入值，并调用 `setText` 来更新 state。这使得你可以在下方显示当前的 `text`。

<Sandpack>

```js
import { useState } from 'react';

export default function MyInput() {
  const [text, setText] = useState('你好');

  function handleChange(e) {
    setText(e.target.value);
  }

  return (
    <>
      <input value={text} onChange={handleChange} />
      <p>你输入了：{text}</p>
      <button onClick={() => setText('你好')}>
        重置
      </button>
    </>
  );
}
```

</Sandpack>

<Solution />

#### 多选框（布尔值） {/*checkbox-boolean*/}

在这个例子中，`liked` state 变量保存一个布尔值。当你点击输入框时，`setLiked` 用浏览器复选框输入是否被选中更新 `liked` state 变量。`liked` 变量被用于渲染复选框下方的文本。

<Sandpack>

```js
import { useState } from 'react';

export default function MyCheckbox() {
  const [liked, setLiked] = useState(true);

  function handleChange(e) {
    setLiked(e.target.checked);
  }

  return (
    <>
      <label>
        <input
          type="checkbox"
          checked={liked}
          onChange={handleChange}
        />
        我喜欢这个
      </label>
      <p>你 {liked ? '喜欢' : '不喜欢'} 这个。</p>
    </>
  );
}
```

</Sandpack>

<Solution />

#### 表单（使用两个 state） {/*form-two-variables*/}

你可以在同一个组件中定义两个 state 变量。每一个 state 变量都是完全独立的。

<Sandpack>

```js
import { useState } from 'react';

export default function Form() {
  const [name, setName] = useState('Taylor');
  const [age, setAge] = useState(42);

  return (
    <>
      <input
        value={name}
        onChange={e => setName(e.target.value)}
      />
      <button onClick={() => setAge(age + 1)}>
        增大年龄。
      </button>
      <p>你好，{name}。你现在 {age} 岁。</p>
    </>
  );
}
```

```css
button { display: block; margin-top: 10px; }
```

</Sandpack>

<Solution />

</Recipes>

一些 API 页面还包括针对常见问题的 [故障排除](/reference/react/useEffect#troubleshooting) 和针对弃用 API 的 [替代方案](/reference/react-dom/findDOMNode#alternatives)。

我们希望 API 参考不仅仅是用来查找参数，还可以用来查看任何给定 API 可以做的所有不同事情以及与其他 API 相关联的方法。

## 接下来还有什么 {/*whats-next*/}

对新文档的介绍到此结束！浏览一下新网站，看看你喜欢或不喜欢什么，欢迎在 [匿名调查](https://www.surveymonkey.co.uk/r/PYRPF3X) 或 [问题跟踪器](https://github.com/reactjs/react.dev/issues) 中提供反馈。

我们承认这个项目花费了很长时间才发布。我们希望 React 社区保持应该拥有的高质量标准。在编写这些文档和创建所有示例的过程中，我们发现了一些自己解释中的错误、React 中的错误，甚至是 React 设计中的空缺，我们现在正在努力解决。我们希望新文档将帮助我们在未来将 React 本身保持在更高的标准上。

我们听到了许多想要扩展网站内容和功能的请求，例如：

- 为所有示例提供 TypeScript 版本；
- 创建更新的性能、测试和可访问性指南；
- 独立记录 React 服务器组件，而不是依赖于支持它们的框架；
- 与我们的国际社区合作，将新文档翻译成各种语言；
- 在新网站中添加缺少的功能（例如，此博客的 RSS）

[react.dev](https://react.dev/) 已经发布，我们希望将重心从“追赶”第三方 React 教育资源转向添加新信息并进一步改进我们的新网站。

我们认为现在是学习 React 的最好的时机。

## 贡献者 {/*who-worked-on-this*/}

在 React 团队中，[Rachel Nabors](https://twitter.com/rachelnabors/) 领导了该项目并提供了插图，而 [Dan Abramov](https://bsky.app/profile/danabra.mov) 设计了课程。他们也共同撰写了大部分内容。

当然，没有一个这么大的项目是孤立进行的。我们有很多想要感谢的人！

[Sylwia Vargas](https://twitter.com/SylwiaVargas) 改进了我们的示例，而不是继续使用“foo/bar/baz”、kitten，和来自世界各地的科学家、艺术家和城市。[Maggie Appleton](https://twitter.com/Mappletons) 将我们的涂鸦转化成了清晰的图表系统。

感谢 [David McCabe](https://twitter.com/mcc_abe)、[Sophie Alpert](https://twitter.com/sophiebits)、[Rick Hanlon](https://twitter.com/rickhanlonii)、[Andrew Clark](https://twitter.com/acdlite) 和 [Matt Carroll](https://twitter.com/mattcarrollcode) 提供额外的写作贡献。我们还要感谢 [Natalia Tepluhina](https://twitter.com/n_tepluhina) 和 [Sebastian Markbåge](https://twitter.com/sebmarkbage) 提供的想法和反馈。

感谢 [Dan Lebowitz](https://twitter.com/lebo) 设计了网站，[Razvan Gradinar](https://dribbble.com/GradinarRazvan) 设计了 sandbox。

在开发方面，感谢 [Jared Palmer](https://twitter.com/jaredpalmer) 进行原型开发。感谢 [Dane Grant](https://twitter.com/danecando) 和来自 [ThisDotLabs](https://www.thisdot.co/) 的 [Dustin Goodman](https://twitter.com/dustinsgoodman) 为 UI 开发提供了支持。感谢 [Ives van Hoorne](https://twitter.com/CompuIves)、[Alex Moldovan](https://twitter.com/alexnmoldovan)、[Jasper De Moor](https://twitter.com/JasperDeMoor) 和来自 [CodeSandbox](https://codesandbox.io/) 的 [Danilo Woznica](https://twitter.com/danilowoz) 为集成 sandbox 做出了贡献。感谢 [Rick Hanlon](https://twitter.com/rickhanlonii) 进行开发和设计工作，完善我们的颜色和细节。感谢 [Harish Kumar](https://www.strek.in/) 和 [Luna Ruan](https://twitter.com/lunaruan) 为网站添加新功能并帮助维护它。

非常感谢那些自愿参加 alpha 和 beta 测试计划的人。你们的热情和宝贵的反馈帮助我们塑造了这些文档。特别感谢我们的 beta 测试人员 [Debbie O'Brien](https://twitter.com/debs_obrien)，她在 React Conf 2021 上分享了她使用 React 文档的经验。

最后，感谢 React 社区的启发，是你们促使我们完成了这个新的项目。我们希望新文档将帮助大家使用 React 构建任何你想要的用户界面。

---
# Source: react-labs-what-we-have-been-working-on-march-2023.md
---
---
title: "React Labs：我们正在努力的方向——2023 年 3 月"
author: Joseph Savona, Josh Story, Lauren Tan, Mengdi Chen, Samuel Susla, Sathya Gunasekaran, Sebastian Markbage, and Andrew Clark
date: 2023/03/22
description: 在 React Labs 的文章中，我们讲述了正在进行研究和开发的项目。自上次更新以来，我们取得了重要进展，希望能分享我们所学到的知识。
---

2023 年 3 月 22 日 [Joseph Savona](https://twitter.com/en_JS)、[Josh Story](https://twitter.com/joshcstory)、[Lauren Tan](https://twitter.com/potetotes)、[Mengdi Chen](https://twitter.com/mengdi_en)、[Samuel Susla](https://twitter.com/SamuelSusla)、[Sathya Gunasekaran](https://twitter.com/_gsathya)、[Sebastian Markbåge](https://twitter.com/sebmarkbage) 与 [Andrew Clark](https://twitter.com/acdlite)

---

<Intro>

在 React Labs 的文章中，我们讲述了正在进行研究和开发的项目。自 [上次更新](/blog/2022/06/15/react-labs-what-we-have-been-working-on-june-2022) 以来，我们在 React 服务器组件、资产加载、优化编译器、离屏渲染和过渡追踪方面取得了重要进展，并希望分享我们所学到的知识。

</Intro>

---

## React 服务器组件 {/*react-server-components*/}

React 服务器组件（React Server Components，简称 RSC）是由 React 团队设计的新的应用架构。

我们之前在 [introductory talk](/blog/2020/12/21/data-fetching-with-react-server-components) 与 [RFC](https://github.com/reactjs/rfcs/pull/188) 中分享了有关 RSC 的研究。之前我们提到，我们引入了一种新的组件类型——服务器组件。服务器组件会提前运行，并在打包时被排除在外。服务器组件也可以在构建期间运行，并允许你从文件系统中读取或提取静态内容。它们也可以在服务器上运行，让你可以访问数据层而不必构建 API。你可以通过 props 将数据从服务器组件传递到浏览器中的交互式客户端组件中。

RSC 将面向服务器的多页面应用程序的简单“请求/响应”思维模型与面向客户端的单页面应用程序的无缝交互性相结合，为你提供了两者的最佳结合。

自上次更新以来，我们已将 [RFC](https://github.com/reactjs/rfcs/blob/main/text/0188-server-components.md) 合并以批准提案。我们解决了 [React 服务器模块约定](https://github.com/reactjs/rfcs/blob/main/text/0227-server-module-conventions.md) 提案中未解决的问题，并与我们的合作伙伴达成共识，采用 `use client` 协定。这些文件还作为符合 RSC 兼容实现应支持的规范。

最大的变化是我们引入了 [`async` / `await`](https://github.com/reactjs/rfcs/pull/229) 作为从服务器组件中进行数据提取的主要方式。我们还计划通过引入一个名为 `use` 的新 Hook，从客户端支持数据加载，该 Hook 也将取消 Promises。虽然我们不能在仅限客户端的应用程序中的任意组件中支持 `async / await`，但我们计划在将客户端仅应用程序结构化类似于 RSC 应用程序的方式时添加支持。

现在我们已经相当好地解决了数据提取的问题，我们正在探索另一个方向：从客户端向服务器发送数据，以便可以执行数据库变更和实现表单。我们通过在服务器/客户端边界传递 Server Action 函数来实现这一点。客户端可以调用该函数，提供无缝 RPC。而在 JavaScript 加载之前，Server Action 还可以提供逐步增强的表单。

RSC 已经在 [Next.js App Router](/learn/creating-a-react-app#nextjs-app-router) 中发布，展示了一个真正深度集成的路由器，它使用了 RSC 并将其作为 primitive。但这不是构建 RSC 兼容的路由器和框架的唯一方法。RSC 规范和实现提供了特定功能的明确分离，旨在成为适用于兼容 React 框架的组件规范。

我们通常建议使用现有的框架，但你仍然可以构建自定义框架。由于需要深度集成 bundler，构建自定义 RSC 兼容的框架并不像想象中那么容易。当前的若代 bundler 非常适合在客户端使用，但它们并没有专门为将单个模块图分割为服务器和客户端提供一流的支持而设计。因此我们选择直接与 bundler 开发人员合作，以将内置 RSC 作为 primitive。

## 资源加载 {/*asset-loading*/}

[Suspense](/reference/react/Suspense) 指定在组件的数据或代码仍在加载时显示在屏幕上的内容。这能够让页面正在加载，或者因为路由导航需要加载更多数据和代码时，用户逐步看到更多内容。然而，从用户的角度来看，数据加载和渲染并不能完全说明新内容是否已准备就绪。默认情况下，浏览器独立地加载样式表、字体和图像，这可能会导致 UI 的跳跃以及不断的布局变化。

我们正在努力将 Suspense 与样式表、字体和图像的加载生命周期完全集成，以便 React 能够了解它们是否已经准备好然后显示它们。在不更改已编写的 React 组件的方式的情况下，更新将以更连贯和令人愉悦的方式进行。作为优化，我们还将提供一种手动方式，可以直接从组件中预加载类似字体之类的资源。

我们目前正在实现这些功能，很快将有更多内容分享。

## Document Metadata {/*document-metadata*/}

应用程序中的不同页面和屏幕可能具有不同的 metadata，如 `<title>` 标签、描述（description）和其他特定于此屏幕的 `<meta>` 标签。从维护的角度来看，将此信息保持接近该页面或屏幕的 React 组件更具可扩展性。然而，metadata 的 HTML 标签被包含在文档的 `<head>` 中，通常在应用程序的根组件中渲染。

现在可以通过以下两种技术解决此问题。

一种技术是渲染一个特殊的第三方组件，将 `<title>`、`<meta>` 和其他标签移动到其中，并将其放在 document `<head>` 中。这适用于主流浏览器，但也有许多不运行 JavaScript 的客户端，如 Open Graph 解析器（parser），因此这种技术不是普遍适用的。

另一种技术是将页面分为两部分进行服务器渲染。首先，渲染主要内容并收集所有这些标签；然后渲染 `<head>` 与这些标签；最后将 `<head>` 和主要内容发送到浏览器。这种方法是可行的，但它会阻止利用 [React 18 的流式服务器渲染器](/reference/react-dom/server/renderToReadableStream)，因为你必须在发送 `<head>` 之前等待所有内容渲染完成。

这就是为什么我们正在添加内置支持，以便在组件树中的任何位置渲染 `<title>`、`<meta>` 和 metadata `<link>` 标签。它将在所有环境中以相同的方式工作，包括完全客户端代码、SSR 和未来的 RSC。我们将很快分享更多关于此的详细信息。

## React 优化编译器 {/*react-optimizing-compiler*/}

自从上次更新以来，我们一直在积极迭代 [React Forget](/blog/2022/06/15/react-labs-what-we-have-been-working-on-june-2022#react-compiler) 的设计，这是 React 的一个优化编译器。我们之前曾将其称为“自动记忆化编译器”，在某种意义上这是正确的。但是构建编译器帮助我们更深入地理解了 React 的编程模型。更好地理解 React Forget 的方法是将其视为一种自动的 **reactive** 编译器。

React 的核心思想是开发人员将其 UI 定义为当前状态的函数。可以使用普通的 JavaScript 值，如数字、字符串、数组、对象，并使用标准的 JavaScript 语法，如 if/else、for 等，来描述组件逻辑。其思维模型是，当应用程序状态发生更改时，React 将重新渲染。我们认为，这种简单的思维模型和与 JavaScript 语义密切相关的原则是 React 编程模型中的重要原则。

问题在于，React 有时会过于 **reactive**：它可能会重新渲染太多次。例如，在 JavaScript 中，我们没有简单的方法来比较两个对象或数组是否相等（具有相同的键和值），因此在每次渲染时创建一个新对象或数组都可能会导致 React 执行更多的工作。这意味着开发人员必须显式地记忆化组件，以免对更改做出过度的反应。

我们的目标是通过 React Forget 确保 React 应用程序默认具有恰当的 reactive：只有在状态值 **有意义** 地更改时才重新渲染应用程序。从实现的角度来看，这意味着自动记忆化，但我们相信，reactive 框架是更好地理解 React 和 Forget 的一种方法。一种思考方式是，当对象标识发生更改时 React 会重新渲染。而使用 Forget，当语义值发生更改时，React 就会重新渲染——但不会产生深层比较的运行时成本。

就具体进展而言，自上次更新以来，我们已经迭代了大量编译器的设计，以符合这种自动 reactive 的方法，并融入了内部使用编译器的反馈意见。在去年末对编译器进行了一些重大重构后，我们现在已经开始在 Meta 的有限生产环境中使用编译器。我们计划在生产环境中证明它后开源。

最后，许多人对编译器的工作原理表示出很大的兴趣。我们期待在验证编译器并开源它时分享更多细节。但现在有一些细节可以分享：

编译器的核心与 Babel 几乎完全解耦，核心编译器 API（大致上）是旧 AST 输入，新 AST 输出（同时保留源位置数据）。在底层，我们使用自定义代码表示和转换管道（pipeline），以进行低级语义分析。然而，编译器的主要公共接口将通过 Babel 和其他构建系统插件提供。为了方便测试，我们目前有一个 Babel 插件，它是一个非常薄的包装器，将调用编译器生成每个函数的新版本并替换它。

在过去的几个月中，我们对编译器进行了重构，希望专注于细化核心编译模型，以确保我们可以处理诸如条件语句、循环、reassignment 和 mutation 等复杂问题。然而，JavaScript 在表达每个特性的上都可能有很多方式：if/else、三目运算符、for、for-in、for-of 等。如果试图一开始就支持整个语言会延迟我们验证核心模型的时间点。相反，我们从语言的一个较小但有代表性的子集开始：let/const、if/else、for 循环、对象、数组、原始类型、函数调用和其他一些特性。随着我们对核心模型的信心增强和内部抽象的完善，我们扩展了支持的语言子集。我们还明确了我们尚不支持的语法，记录诊断信息并跳过不受支持的输入的编译。我们有工具可以在 Meta 的代码库上尝试编译器，并查看哪些不受支持的特性最常见，以便我们下一个优先考虑它们。我们将继续逐步扩展，以支持整个语言。

在 React 组件中使原生 JavaScript 变得 reactive 需要一个具有深刻理解语义的编译器，以便它能准确理解代码正在做什么。通过采取这种方法，我们正在创建一个用于在 JavaScript 中实现 reactive 的系统，它将帮助开发者使用语言的全部表达能力编写任何复杂度的产品代码，而不仅仅局限于领域特定语言。

## 离屏渲染 {/*offscreen-rendering*/}

离屏渲染是 React 即将推出的一种功能，用于在后台渲染屏幕，而无需额外的性能开销。可以将其视为 [`content-visibility` CSS 属性](https://developer.mozilla.org/ch-ZN/docs/Web/CSS/content-visibility) 的一个版本，它不仅适用于 DOM 元素，还适用于 React 组件。在我们的研究中，我们发现了各种用例：

- 路由可以在后台预渲染屏幕，以便当用户导航到它们时，可以立即使用。
- 切换选项卡组件可以保留隐藏选项卡的状态，以便用户可以在不丢失进度的情况下在它们之间切换。
- 虚拟化列表组件可以在可见窗口的上方和下方预渲染额外的行。
- 当打开模态或弹出窗口时，整个应用程序可以进入“后台”模式，以便除模态框外的所有内容都禁用事件和更新。

大多数 React 开发人员不会直接与 React 的离屏 API 交互。相反，离屏渲染将集成到路由器和 UI 库等内容中，然后使用这些库的开发人员将自动受益，而无需额外的工作。

我们的想法是，开发者应该能够在不更改组件编写方式的情况下，将任何 React 树渲染到屏幕外。当组件被离屏渲染时，它实际上并没有 **挂载**，直到组件变为可见状态——其效果不会被触发。例如，如果组件使用 `useEffect` 在首次出现时记录分析数据，预渲染不会影响数据的准确性。同样，当组件离开屏幕时，其效果也会被卸载。离屏渲染的一个关键特性是，可以切换组件的可见性，而不会失去其状态。

自上次更新以来，我们在 Meta 的 React Native 应用程序上测试了一个实验性的预渲染版本，包括 Android 和 iOS，性能表现良好。我们还改进了离屏渲染与 Suspense 的配合方式——在离屏树中挂起（suspend）但不会触发 Suspense 后备方案。我们剩下的工作是完成向库开发人员公开的基本组件。我们预计将于今年晚些时候发布一个 RFC，同时发布一个实验性的 API 用于测试和反馈。

## 追踪 Transition {/*transition-tracing*/}

追踪 Transition 的 API 可以检测 [React Transition](/reference/react/useTransition) 变慢的原因，并调查为什么会变慢。在上次更新后，我们完成了 API 的初始设计，并发布了一个 [RFC](https://github.com/reactjs/rfcs/pull/238)，基本功能也已经实现。该项目目前处于暂停状态。我们欢迎对 RFC 进行反馈，并期待恢复其开发，为 React 提供更好的性能测量工具。这将特别对基于 React Transition 构建的路由非常有用，例如 [Next.js App Router](/learn/creating-a-react-app#nextjs-app-router)。

* * *
除了这个更新，我们的团队最近还在社区播客和直播中客串，更多地讲述我们的工作并回答问题。

* [Dan Abramov](https://bsky.app/profile/danabra.mov) 和 [Joe Savona](https://twitter.com/en_JS) 在 [Kent C. Dodds 的 YouTube 频道](https://www.youtube.com/watch?v=h7tur48JSaw) 上接受了采访，讨论了关于 React 服务器组件的问题。
* [Dan Abramov](https://bsky.app/profile/danabra.mov) 和 [Joe Savona](https://twitter.com/en_JS) 在 [JSParty podcast](https://jsparty.fm/267) 上作为嘉宾，分享了他们对 React 未来的看法。

感谢 [Andrew Clark](https://twitter.com/acdlite)、[Dan Abramov](https://bsky.app/profile/danabra.mov)、[Dave McCabe](https://twitter.com/mcc_abe)、[Luna Wei](https://twitter.com/lunaleaps)、[Matt Carroll](https://twitter.com/mattcarrollcode)、[Sean Keegan](https://twitter.com/DevRelSean)、[Sebastian Silbermann](https://twitter.com/sebsilbermann)、[Seth Webster](https://twitter.com/sethwebster) 和 [Sophie Alpert](https://twitter.com/sophiebits) 对本篇文章进行审查。

感谢阅读，我们下次更新见！

---
# Source: react-canaries.md
---
---
title: "React Canaries：在 Meta 之外逐步推出新功能"
author: Dan Abramov, Sophie Alpert, Rick Hanlon, Sebastian Markbage, and Andrew Clark
date: 2023/05/03
description: 我们希望为 React 社区提供一种选择，使他们能够在新功能设计接近最终状态时立即采用这些功能——类似于 Meta 内部使用 React 的方式。我们正在推出一个新的官方支持的 [Canary 发布渠道](/community/versioning-policy#canary-channel)。它允许如框架一样的 curated setup，将对单个 React 功能的采用与 React 发布计划分离开。
---

2023 年 5 月 3 日 [Dan Abramov](https://bsky.app/profile/danabra.mov)、[Sophie Alpert](https://twitter.com/sophiebits)、[Rick Hanlon](https://twitter.com/rickhanlonii)、[Sebastian Markbåge](https://twitter.com/sebmarkbage) 与 [Andrew Clark](https://twitter.com/acdlite)

---

<Intro>

我们希望为 React 社区提供一种选择，使他们能够在新功能设计接近最终状态时立即采用这些功能——类似于 Meta 内部使用 React 的方式。我们正在推出一个新的官方支持的 [Canary 发布渠道](/community/versioning-policy#canary-channel)。它允许如框架一样的 curated setup，将对单个 React 功能的采用与 React 发布计划分离开。

</Intro>

---

## tl;dr {/*tldr*/}

我们正在引入一个官方支持的 React [Canary 发布渠道](/community/versioning-policy#canary-channel)。由于它得到了官方支持，如果出现任何回归（regression）问题，我们将像处理稳定版本的错误一样予以处理。
Canary 能够让你在它们出现在 semver 稳定版本之前开始使用单个新的 React 功能。
与 [实验性](/community/versioning-policy#experimental-channel) 渠道不同，React Canary 仅包括我们认为准备采用的合理功能。我们鼓励框架考虑锁定 Canary React 发布版本。
即使有关内容已经出现在了 Canary 版本中，我们仍将在博客中宣布重大变更和新功能。
**一如既往，React 在每个稳定版本中都遵循 semver 语义化版本控制模块**。

## 新功能通常是如何开发的 {/*how-react-features-are-usually-developed*/}

通常，每个 React 功能都将经历以下相同阶段：

1. 开发初始版本，并添加前缀 `experimental_` 或 `unstable_`，表示该功能仅在 `experimental` 发布渠道中可用。此时，该功能预计会发生重大变化。
2. 找到一个愿意帮助我们测试该功能并提供反馈的 Meta 团队，这将导致一轮变更。随着功能变得更加稳定，我们与更多的 Meta 团队一起尝试它。
3. 最终，我们对此设计感到有信心。我们从 API 名称中删除对应前缀，并使该功能默认在 `main` 分支上可用，表示大多数 Meta 产品都在使用。此时，任何 Meta 团队都可以使用此功能。
4. 当我们对该方向有信心时，我们也会发布一个新功能的 RFC。此时，我们知道此设计适用于广泛的情况，但可能会进行最后一些调整。
5. 当我们接近发布一项开源版本时，我们将为该功能编写文档，并最终在稳定的 React 版本中发布该功能。

这个流程对我们迄今发布的大多数功能都有效。但是，新功能在“通常可以使用（步骤 3）”与“在开源中发布（步骤 5）”之间可能存在显著差距。

**我们希望为 React 社区提供与 Meta 相同的选择，让单个新功能（在其可用时）可以更早地被采用，而无需等待 React 的下一个发布周期**。

与往常一样，所有 React 功能最终都将进入稳定的版本。

## 能否只发布更多的小版本更新？ {/*can-we-just-do-more-minor-releases*/}

通常情况下，我们确实会使用小版本更新来引入新功能。

然而，这并非总是可行的。有时，新功能与其他尚未完全完成且仍在积极迭代的新功能相互关联。由于它们的实现相关联，因此无法分别发布。同样，因为它们可能会影响相同的软件包（例如 `react` 和 `react-dom`），我们也不能将它们分别版本化。我们需要不断对尚未准备就绪的部分进行迭代，所以不会出现大量主要版本发布，这是 semver 要求我们做到的。

在 Meta，我们通过从 `main` 分支构建 React，并手动将其更新为每周的特定锁定提交来解决这个问题。这也是 React Native 发布在过去几年中一直遵循的方法。每个 *稳定的* React Native 发布都锁定在 React 仓库的 `main` 分支的特定提交上。这使得 React Native 可以包含重要的错误修复，并在框架级别逐步采用新的 React 功能，而不会与全局 React 发布时间表耦合。

我们希望将这种工作流程提供给其他框架和 curated setup。例如，在破坏性更改进入稳定性发布之前，它允许基于 React 的框架包含与 React 相关的破坏性更改。由于一些破坏性更改仅影响框架集成，因此这会特别有用。这使得框架可以在其自己的小版本中发布此类更改而不会破坏 semver。

Canary 的滚动发布将允许我们拥有更紧密的反馈循环，并确保新功能在社区中得到全面测试。这种工作流程更接近于 TC39——JavaScript 标准委员会——[处理编号阶段中的更改](https://tc39.es/process-document/) 的方式。在 React 稳定发布之前，建立在 React 之上的框架中可能会提供新的 React 功能，就像在浏览器中提供新的 JavaScript 功能一样，尽管它们尚未被正式批准为规范的一部分。

## 为什么不使用实验性发布？ {/*why-not-use-experimental-releases-instead*/}

虽然在技术上可以使用 [实验性发布](/community/versioning-policy#canary-channel)，但我们建议不要在生产环境中使用它们，因为实验性 API 在稳定之前可能会经历重大的破坏性更改（甚至可能完全被删除）。而尽管 Canary 也可能包含错误（与任何版本发布一样），但我们会计划在博客上宣布 Canary 中的任何重大破坏性更改。Canary 最接近 Meta 内部运行的代码，所以它们通常是相对稳定的。但是，在更新锁定提交之间，你需要锁定版本并手动检查 GitHub 提交日志。

**我们预计，在未经策划设置（如框架）的情况下使用 React 的大多数人将希望继续使用稳定版本**。但是，如果你正在构建一个框架，你可能想考虑锁定一个特定提交的 Canary 版本的 React，并以你自己的节奏进行更新。这样做的好处是，它可以按照你自己的发布计划，更早为你的用户提供单独完成的 React 功能和错误修复。这类似于 React Native 在过去几年中一直在做的。缺点是，你需要承担额外的责任来审核哪些 React 提交应该被 pull，并向你的用户传达哪些 React 更改包含在你的发布中。

如果你是一个框架作者，想尝试这种方法，请与我们联系。

## 更早宣布破坏性更改与新功能 {/*announcing-breaking-changes-and-new-features-early*/}

Canary 发布代表了我们在任何时候对下一个稳定版本的 React 所做的最佳猜测。

传统上，我们只在发布周期的 **最后**（进行主要发布时）宣布破坏性更改。现在，Canary 发布是一种正式支持的使用 React 的方式，我们计划改为在 Canary 中 **已经出现** 破坏性更改和重大新功能时就宣布它们。例如，如果我们合并一个将在 Canary 中发布的破坏性更改，我们将在 React 博客上写一篇关于它的文章，包括必要的 codemods 和迁移说明。然后，如果你是一个框架作者，正在处理一个主要版本的发布，以更新锁定的 React Canary 以包含该更改，你可以在你的发布说明中链接到我们的博客文章。最后，当 React 的稳定主要版本准备好时，我们将链接到那些已经发布的博客文章，我们希望这将帮助我们的团队更快地取得进展。

我们计划记录在 Canary 中已经准备好的 API，即使这些 API 尚未在外部提供。仅在 Canary 中可用的 API 将在相应页面上用特殊注释标记。这将包括像 [`use`](https://github.com/reactjs/rfcs/pull/229) 这样的API，以及一些其他 API（如 `cache` 和 `createServerContext`），我们将为其发送 RFC。

## 锁定 Canary 版本 {/*canaries-must-be-pinned*/}

如果你决定为你的应用程序或框架采用 Canary 工作流，请确保始终锁定 Canary 的 **确切** 版本。由于 Canary 是预发布版本，它们可能仍然包含破坏性更改。

## 例子：React 服务器组件 {/*example-react-server-components*/}

正如我们在三月份 [宣布的那样](/blog/2023/03/22/react-labs-what-we-have-been-working-on-march-2023#react-server-components)，React 服务器组件的规范已经最终确定，并且我们不希望出现与用户界面 API 相关的破坏性更改。然而，我们还在继续处理几个相互关联的仅与框架有关的功能（比如 [资源加载](/blog/2023/03/22/react-labs-what-we-have-been-working-on-march-2023#asset-loading)），我们预计在这方面还会有更多的破坏性更改。

这意味着 React 服务器组件已经准备好被框架采用。然而在下一个主要的 React 版本发布之前，框架采用它们的唯一方式是锁定 Canary 发布的 React 版本（为了避免捆绑两个 React 副本，希望这样做的框架需要强制解析 `react` 和 `react-dom` 到他们框架中锁定的 Canary 版本，并向他们的用户解释。Next.js App Router 就是这样做的）。

## 同时针对稳定版本和 Canary 版本的测试库 {/*testing-libraries-against-both-stable-and-canary-versions*/}

我们不希望库作者测试每个 Canary 版本，因为这将极其困难。然而，就像我们在三年前 [介绍不同的 React 预发布渠道](https://legacy.reactjs.org/blog/2019/10/22/react-release-channels.html) 时一样，我们鼓励库针对 **最新的** 稳定版本和 Canary 版本运行测试。如果你看到了未经宣布的行为变化，请在 React 仓库中提交一个错误报告，以便我们可以帮助诊断它。我们希望随着这种做法的广泛采用，它将减少升级库到最新 React 主要版本所需的工作量，因为在使用它们时会发现意外的回归问题（regressions）。

<Note>

严格来说，Canary 不是一个 **新的** 发布渠道——它曾经被称为 Next。后来我们决定更名以避免与 Next.js 混淆。我们宣布它是一个 **新的** 发布渠道，也是为了传达新的期望：比如 Canary 是一种正式支持使用 React 的方式。

</Note>

## 稳定版本的发布流程与之前一样 {/*stable-releases-work-like-before*/}

我们不会对稳定性 React 版本进行任何更改。




---
# Source: react-labs-what-we-have-been-working-on-june-2022.md
---
---
title: "React Labs：我们正在努力的方向——2022 年 6 月"
author:  Andrew Clark, Dan Abramov, Jan Kassens, Joseph Savona, Josh Story, Lauren Tan, Luna Ruan, Mengdi Chen, Rick Hanlon, Robert Zhang, Sathya Gunasekaran, Sebastian Markbage, and Xuan Huang
date: 2022/06/15
description: React 18 经过多年的努力才得以问世，它为 React 团队带来了宝贵的经验教训。它的发布是多年的研究和探索的结果。其中一些路径是成功的，但更多的是死胡同，但是也带来了新的见解。我们学到的一个教训是，对社区来说，在等待新功能时没有了解我们正在探索的路径是令人沮丧的。
---

2022 年 6 月 15 日 [Andrew Clark](https://twitter.com/acdlite)、[Dan Abramov](https://bsky.app/profile/danabra.mov)、[Jan Kassens](https://twitter.com/kassens)、[Joseph Savona](https://twitter.com/en_JS)、[Josh Story](https://twitter.com/joshcstory)、[Lauren Tan](https://twitter.com/potetotes)、[Luna Ruan](https://twitter.com/lunaruan)、[Mengdi Chen](https://twitter.com/mengdi_en)、[Rick Hanlon](https://twitter.com/rickhanlonii)、[Robert Zhang](https://twitter.com/jiaxuanzhang01)、[Sathya Gunasekaran](https://twitter.com/_gsathya)、[Sebastian Markbåge](https://twitter.com/sebmarkbage) 与 [Xuan Huang](https://twitter.com/Huxpro)

---

<Intro>

[React 18](/blog/2022/03/29/react-v18) 经过多年的努力才得以问世，它为 React 团队带来了宝贵的经验教训。它的发布是多年的研究和探索的结果。其中一些路径是成功的，但更多的是死胡同，但是也带来了新的见解。我们学到的一个教训是，对社区来说，在等待新功能时没有了解我们正在探索的路径是令人沮丧的。

</Intro>

---

我们通常会同时进行多个项目，从更具实验性的项目到明确定义的项目不一而足。展望未来，我们希望开始定期与社区分享我们在这些项目中的工作。

我们并不在此给出具有明确时间表的路线图：许多项目正在积极研究中，很难确定具体的发布日期。根据我们的学习情况，它们甚至可能在当前迭代中不会发布。相反，我们想与你分享我们正在积极思考的问题领域以及我们迄今为止学到的东西。

## 服务器组件 {/*server-components*/}

我们在 2020 年 12 月发布了 [React 服务器组件](https://legacy.reactjs.org/blog/2020/12/21/data-fetching-with-react-server-components.html)（RSC）的实验性演示。从那时起，我们一直在完成 React 18 中的依赖项，并根据实验性反馈进行改进。

特别地，我们放弃了拥有分叉 I/O 库（例如 react-fetch）的想法，转而采用了具有更好兼容性的 async/await 模型。这从技术上讲并不阻碍 RSC 的发布，因为还可以使用路由器进行数据获取。另一个变化是我们也放弃了文件扩展名的方法，而是采用了 [注释边界](https://github.com/reactjs/rfcs/pull/189#issuecomment-1116482278) 的方式。

我们正在与 Vercel 和 Shopify 合作，在 webpack 和 Vite 中统一打包器（bundler）对共享语义的支持。在发布之前，我们希望确保整个 React 生态系统中的 RSC 的语义是一致的。这是达到稳定状态的主要障碍。

## 资源加载 {/*asset-loading*/}

目前，像脚本、外部样式、字体和图像等资源通常是通过外部系统预加载和加载的。这可能在新的环境（如跨流媒体、服务器组件等）之间协调起来比较棘手。

我们正在考虑添加 API，以通过适用于所有 React 环境的 React API 来预加载和加载经过重复数据删除的外部资源。

我们还正在研究如何支持 Suspense，这样就可以拥有在加载完成之前阻塞显示的图像、CSS 和字体，但不会阻塞流媒体和并发渲染。这可以帮助避免视觉上的 [popcorning](https://twitter.com/sebmarkbage/status/1516852731251724293) 现象，即视觉效果的突然出现和布局的变化

## 静态服务器渲染优化 {/*static-server-rendering-optimizations*/}

静态站点生成（SSG）和增量静态再生成（ISR）是提高可缓存页面性能的好方法，但我们认为我们可以添加功能来改进动态服务器端渲染（SSR）的性能，特别是当大部分但不是全部内容都是可缓存的时候。我们正在探索利用编译和静态传递来优化服务器渲染的方式。

## React 优化编译器 {/*react-compiler*/}

我们在 React Conf 2021 上提供了 React Forget 的 [早期预览](https://www.youtube.com/watch?v=lGEMwh32soc)。它是一个编译器，可以自动生成等效的 `useMemo` 和 `useCallback` 调用，以最小化重新渲染的成本，同时保留 React 的编程模型。

最近，我们完成了编译器的重写，使其更可靠且功能更强大。这种新的架构使我们能够分析和缓存更复杂的模式，比如使用 [local mutation](/learn/keeping-components-pure#local-mutation-your-components-little-secret)，并开启了许多新的编译时优化机会，不仅仅与记忆化 hook 持平。

我们还正在开发一个用于探索编译器多个方面的 playground。尽管 playground 的目标是使编译器的开发变得更容易，但我们认为它将使尝试和建立对编译器工作方式的直观感觉变得更容易。它揭示了编译器在幕后的各种工作原理，并且可以在输入时实时渲染编译器的输出。它将与编译器一起发布。

## 离屏渲染 {/*offscreen*/}

如今，如果你想隐藏和显示一个组件，有两种选择。一种是完全从树中添加或删除。这种方法的问题在于，每次卸载组件时，包括在 DOM 中存储的滚动位置在内的 UI 状态都会丢失。

另一种选择是保持组件挂载，并使用 CSS 在视觉上切换外观。这样可以保留 UI 的状态，但会带来性能损耗，因为每当 React 接收到新的更新时，它必须继续渲染隐藏的组件及其所有子组件。

离屏渲染（Offscreen）引入了第三种选择：在视觉上隐藏 UI，但将其内容降低优先级。这个想法本质上类似于 `content-visibility` CSS 属性：当内容被隐藏时，它不需要与其他 UI 保持同步。React 可以将渲染工作推迟到应用程序的其他部分处于空闲状态，或者直到内容再次变得可见为止。

离屏渲染是一个低级能力，可以实现高级功能。类似于 React 的其他并发功能（如 `startTransition`），在大多数情况下，你不会直接与 Offscreen API 交互，而是通过一个偏好的框架来实现以下模式：

* **即时过渡**。一些路由框架已经预取数据以加快后续导航，例如在悬停在链接上时。使用离屏渲染，它们还可以在后台预渲染下一个屏幕。
* **可重用状态**。类似地，在路由或选项卡之间导航时，你可以使用离屏渲染来保留上一个屏幕的状态，以便你可以切换回来并继续之前的操作。
* **虚拟化列表渲染**。显示大型项目列表时，虚拟化列表框架将预先渲染比当前可见行数更多的行。你可以使用离屏渲染以比列表中可见项目更低的优先级预渲染隐藏的行。
* **后台内容**。我们还在探索一项相关功能，可以将后台内容降低优先级而不隐藏它，例如显示模态覆盖层时。

## Transition Tracing {/*transition-tracing*/}

目前，React 有两个性能分析工具。[原始的 Profiler](https://legacy.reactjs.org/blog/2018/09/10/introducing-the-react-profiler.html) 显示了性能分析会话中的所有提交的概览。对于每个提交，它还显示了所有已渲染组件以及它们渲染所花费的时间。我们还在 React 18 中引入了一个 [Timeline Profiler](https://github.com/reactwg/react-18/discussions/76) 的测试版本，它显示了组件何时安排更新以及 React 在这些更新上的工作时间。这两个性能分析工具都有助于开发人员在代码中识别性能问题。

我们意识到，开发人员并不认为单独了解缓慢的提交或组件是有用的，更有用的是了解导致缓慢提交的实际原因。开发人员希望能够跟踪特定的交互（例如按钮点击、初始加载或页面导航），以便观察性能回归，并理解为什么交互缓慢以及如何修复它。

我们之前尝试通过创建一个 [交互追踪 API](https://gist.github.com/bvaughn/8de925562903afd2e7a12554adcdda16) 来解决这个问题，但它存在一些基本的设计缺陷，降低了追踪交互缓慢原因的准确性，有时导致交互永远无法结束。由于这些问题，我们最终 [移除了这个API](https://github.com/facebook/react/pull/20037)。

我们正在开发一个新版本的交互追踪 API（由于它通过 `startTransition` 发起，我们将其暂时称为 Transition Tracing），来解决这些问题。

## 新版文档 {/*new-react-docs*/}

去年，我们宣布了新版文档网站的测试版本（[后来发布为 react.dev](/blog/2023/03/16/introducing-react-dev)）。新的学习材料首先介绍了 Hook，并提供了新的图表、插图，以及许多交互式示例和挑战。之前我们暂时中断了这项工作，专注于 React 18 的发布；但现在 React 18 已经发布，我们正在积极努力完成和发布新的文档。

我们目前正在撰写关于 Effect 的详细部分，因为我们听说这是对新手和有经验的 React 用户来说最具挑战性的主题之一。[与 Effect 保持同步](/learn/synchronizing-with-effects) 是系列中首个发布的页面，接下来的几周还会有更多页面发布。当我们开始撰写关于 Effect 的详细部分时，我们意识到许多常见的 Effect 模式可以通过向 React 添加一个新的原语来简化。我们在 [useEvent RFC](https://github.com/reactjs/rfcs/pull/220) 中分享了一些初步想法。目前还处于早期研究阶段，我们仍在对这个想法进行迭代。我们非常感谢社区对 RFC 的意见，以及对正在进行的文档重写的 [反馈](https://github.com/reactjs/react.dev/issues/3308) 和贡献。我们特别要感谢 [Harish Kumar](https://github.com/harish-sethuraman) 为新网站实现提交和审查了许多改进的工作。

感谢 [Sophie Alpert](https://twitter.com/sophiebits) 对本篇博客文章的审查！

---
# Source: react-18-upgrade-guide.md
---
---
title: "如何升级到 React 18"
author: Rick Hanlon
date: 2022/03/08
description: 正如我们在发布报告中分享的那样，React 18 借助新的并发渲染引入了许多新特性，对于已经存在的应用可以采用渐进式策略。在这篇文章中，我们会指导你如何逐步升级到 React 18。
---

2022 年 8 月 3 日 [Rick Hanlon](https://twitter.com/rickhanlonii)

---

<Intro>

正如我们在 [发布报告](/blog/2022/03/29/react-v18) 中分享的那样，React 18 借助新的并发渲染引入了许多新特性，对于已经存在的应用可以采用渐进式策略。在这篇文章中，我们会指导你如何逐步升级到 React 18。

如果你在升级的过程中遇到任何问题，可以在 GitHub [提 issue](https://github.com/facebook/react/issues/new/choose)。

</Intro>

<Note>

对于 React Native 用户来说， React 18 会在 React Native 的未来版本中出现。因为 React 18 依赖于新的 React Native 架构才能受益于这篇文章中提出的新的能力。想了解更多信息，请查看 [这里的 React 会议纪要](https://www.youtube.com/watch?v=FZ0cG47msEk&t=1530s)。

</Note>

---

## 安装 {/*installing*/}

安装最新版的 React：

```bash
npm install react react-dom
```

或者也可以使用 yarn：

```bash
yarn add react react-dom
```

## 客户端渲染 API 的更新 {/*updates-to-client-rendering-apis*/}

当你第一次安装 React 18 的时候，控制台会出现如下警告：

<ConsoleBlock level="error">

ReactDOM.render is no longer supported in React 18. Use createRoot instead. Until you switch to the new API, your app will behave as if it's running React 17. Learn more: https://reactjs.org/link/switch-to-createroot

</ConsoleBlock>

React 18 引入了一个新的 root API，它提供了更好的操作根节点的方式。新的 root API 还启用了新的并发渲染器，使开发者能够选择使用并发特性。

```js
// 之前
import { render } from 'react-dom';
const container = document.getElementById('app');
render(<App tab="home" />, container);

// 现在
import { createRoot } from 'react-dom/client';
const container = document.getElementById('app');
const root = createRoot(container); // 如果你使用 TypeScript，请使用 createRoot(container!)
root.render(<App tab="home" />);
```

我们也已经将 `unmountComponentAtNode` 修改为 `root.unmount`：

```js
// 之前
unmountComponentAtNode(container);

// 现在
root.unmount();
```

我们从 render 中移除了回调函数，因为当使用 Suspense 的时候通常不是预期的结果：

```js
// 之前
const container = document.getElementById('app');
render(<App tab="home" />, container, () => {
  console.log('rendered');
});

// 现在
function AppWithCallbackAfterRender() {
  useEffect(() => {
    console.log('rendered');
  });

  return <App tab="home" />
}

const container = document.getElementById('app');
const root = createRoot(container);
root.render(<AppWithCallbackAfterRender />);
```

<Note>

对于旧的 render 回调函数 API 没有一对一的替换——它取决于你的用例。查看工作组的 [使用 createRoot 替换 render](https://github.com/reactwg/react-18/discussions/5) 博文了解更多信息。

</Note>

最后如果应用通过激活使用了服务端渲染，你需要将 `hydrate` 升级到 `hydrateRoot`：

```js
// 之前
import { hydrate } from 'react-dom';
const container = document.getElementById('app');
hydrate(<App tab="home" />, container);

// 现在
import { hydrateRoot } from 'react-dom/client';
const container = document.getElementById('app');
const root = hydrateRoot(container, <App tab="home" />);
// 和 createRoot 不一样，在这里你不需要单独的 root.render()。
```

了解更多信息，请查看 [工作组的讨论](https://github.com/reactwg/react-18/discussions/5)。

<Note>

**如果你的应用升级后无法工作，请检查它是否被 `<StrictMode>` 包裹**。[严格模式在 React 18 中变得更加严格](#updates-to-strict-mode)，并不是所有组件都可以弹性应对它在开发模式中添加的新检查。如果移除严格模式可以修复你的应用，你可以在升级期间移除它，然后等你修复它指出的问题之后再在树的顶部或者其中一部分添加回来。

</Note>

## 服务端渲染 API 的更新 {/*updates-to-server-rendering-apis*/}

在这次发布中，我们修改 `react-dom/server` API 使它完全支持服务端的 Suspense 和 流式 SSR。作为这些变化的一部分，我们正在废弃旧的 Node 流式 API，因为它不支持服务端的增量 Suspense 流。

现在使用这个 API 会发出警告：

* `renderToNodeStream`：**废弃 ⛔️️**

取而代之的是，对于 Node 环境中的流我们使用：
* `renderToPipeableStream`：**新增 ✨**

同时也引入了新的 API 借助 Suspense 为像 Deno 和 Cloudflare workers 这样的现代分布式运行时环境来支持流式 SSR：
* `renderToReadableStream`：**新增 ✨**

下面的 API 会继续工作，但是对于 Suspense 支持是有限的：
* `renderToString`：**有限制** ⚠️
* `renderToStaticMarkup`：**有限制** ⚠️

最后这个 API 会继续用于渲染电子邮件：
* `renderToStaticNodeStream`

更多关于服务端渲染 API 的变化信息，可以查看工作组文章 [在服务端升级到 React 18](https://github.com/reactwg/react-18/discussions/22)，[深入探讨新的 Suspense SSR 架构](https://github.com/reactwg/react-18/discussions/37)，以及 [Shaundai 个人](https://twitter.com/shaundai) 在 React 2021 会议上关于 [使用 Suspense 的流式服务端渲染](https://www.youtube.com/watch?v=pj5N-Khihgc) 的演讲。

## 更新 TypeScript 类型定义 {/*updates-to-typescript-definitions*/}

如果项目使用了 TypeScript，你需要更新 `@types/react` 和 `@types/react-dom` 依赖到最新版。新的类型更加安全并且能捕获过去常常被类型检查器忽略的问题。最值得注意的变化是，现在定义 props 时，`children` prop 需要被明确列出来，例如：

```typescript{3}
interface MyButtonProps {
  color: string;
  children?: React.ReactNode;
}
```

查看 [React 18 类型 PR](https://github.com/DefinitelyTyped/DefinitelyTyped/pull/56210) 查看只有类型变了的完整清单。它链接到了在类型库中修复的例子，你可以从中了解如何调整你自己的代码。你可以使用 [自动迁移脚本](https://github.com/eps1lon/types-react-codemod) 来帮助你的应用代码更快变更到更安全的新类型。

如果你发现了类型中的问题，请在 DefinitelyTyped 仓库 [提交 issue](https://github.com/DefinitelyTyped/DefinitelyTyped/discussions/new?category=issues-with-a-types-package)。

## 自动批处理 {/*automatic-batching*/}

React 18 通过默认做更多批量处理来增加开箱即用性能提升。批量处理指的是 React 为了提高性能将多个 state 更新分组到一个单独的重渲染。React 18 之前，我们只在 React 事件处理函数内部实现批量更新，而 promise、setTimeout、本地事件处理函数或者其他事件中更新状态，在 React 中默认是不进行批量处理的：

```js
// React 18 之前，只有 React 事件会被批量处理

function handleClick() {
  setCount(c => c + 1);
  setFlag(f => !f);
  // React 只会在结束的时候重新渲染一次（这就是批量处理！）
}

setTimeout(() => {
  setCount(c => c + 1);
  setFlag(f => !f);
  // React 会渲染两次，每一个 state 更新的时候渲染一次（非批量处理）
}, 1000);
```


从使用 `createRoot` 的 React 18 开始，无论来自于哪里，所有的更新都会自动批量处理。这意味着 timeout、promise、本地事件处理函数或者其他任何事件的更新都会和 React 事件内部的更新一样批量处理：

```js
// React 18 中 timeout、promise、
// 本地事件处理函数或者其他任何事件的更新都会批量处理。

function handleClick() {
  setCount(c => c + 1);
  setFlag(f => !f);
  // React 只会在结束的时候重新渲染一次（这就是批量处理！）
}

setTimeout(() => {
  setCount(c => c + 1);
  setFlag(f => !f);
  // React 只会在结束的时候重新渲染一次（这就是批量处理！）
}, 1000);
```

这是一个破坏性变更，但是我们期望这个变更可以产生更少的渲染工作，从而提高应用的性能表现。为了有选择性地使用自动化处理，你可以使用 `flushSync` 包裹：

```js
import { flushSync } from 'react-dom';

function handleClick() {
  flushSync(() => {
    setCounter(c => c + 1);
  });
  // React 现在已经更新了 DOM
  flushSync(() => {
    setFlag(f => !f);
  });
  // React 现在已经更新了 DOM
}
```

更多信息请查看 [深入探索自动批处理](https://github.com/reactwg/react-18/discussions/21)。

## 新 API {/*new-apis-for-libraries*/}

在 React 18 工作组，我们和第三方库的维护者合作，创建需要支持 styles 和外部存储中的特定用例的并发渲染的新 API。为了支持 React 18，一些第三方库可能需要切换到下面的 API 之一：

* `useSyncExternalStore` 是一个新增 Hook，它允许外部存储通过对 store 的强制更新保持同步从而支持并发读取。这个新 API 推荐用于任何和 React 的外部状态集成的库。了解更多信息请查看 [useSyncExternalStore 概览](https://github.com/reactwg/react-18/discussions/70) 和 [useSyncExternalStore API 细节](https://github.com/reactwg/react-18/discussions/86)。
* `useInsertionEffect` 是一个新增 Hook，它可以让 CSS-in-JS 库解决渲染中注入样式的性能问题。我们希望只有在你已经构建了一个 CSS-in-JS 库的情况下才使用它。这个 Hook 会在 DOM 变化之后，layout Effect 读取新的布局之前运行。这解决了 React 17 及其以下就已经存在但是在 React 18 更重要的问题，因为在并发渲染期间 React 会阻止浏览器，给了它一个重新计算布局的机会。了解更多信息，查看 [`<style>` 库升级指南](https://github.com/reactwg/react-18/discussions/110)。

React 18 也引入了一些并发渲染的新 API，例如 `startTransition`、`useDeferredValue` 以及 `useId`，关于此更多信息我们在 [发布报告](/blog/2022/03/29/react-v18) 中有所分享。

## 严格模式的变化 {/*updates-to-strict-mode*/}

在未来，我们想要添加一个特性，它允许 React 在保存 state 的时候添加和移除 UI 块。例如，当用户离开当前 tab 页面又返回时，React 应该能够立刻展示之前的页面。为了达到这个目的，React 会使用和之前一样的组件状态来卸载和重新加载树。

这个特性会让 React 拥有更好的开箱即用性能，但是它需要组件能够灵活应对多次加载和销毁的 effect。大部分 Effect 工作方式没有任何变化，但是一些 Effect 希望它们只加载或者销毁一次。

为了帮助让这些问题浮出水面，React 18 向严格模式中引入了一个只在开发环境进行的新检查。每当组件第一次加载时，新的检查会自动卸载和重新加载每一个组件，并在第二次加载的时候存储之前的状态。

在这些变化之前，React 会加载组件和创建 effect：

```
* React 加载组件。
    * 创建 Layout effect。
    * 创建 Effect effect。
```

在 React 18 的严格模式中，React 会在开发模式下模仿卸载和重新加载组件：

```
* React 加载组件。
    * 创建 Layout effect。
    * 创建 Effect effect。
* React 模仿卸载组件。
    * 销毁 Layout effect。
    * 销毁 Effect effect。
* React 模仿加载有上一个状态的组件。
    * 运行 Layout Effect setup 代码
    * 运行 Effect Effect setup 代码
```

了解更多信息，可以查看工作组的文章：[向严格模式添加可复用的状态](https://github.com/reactwg/react-18/discussions/19) 和 [如何支持 Effect 中的可复用状态](https://github.com/reactwg/react-18/discussions/18)。

## 配置测试环境 {/*configuring-your-testing-environment*/}

第一次更新测试环境使用 `createRoot`，你可能在测试环境的控制台看到这个警告：

<ConsoleBlock level="error">

The current testing environment is not configured to support act(...)

</ConsoleBlock>

为了修复这个问题，需要在运行测试之前将 `globalThis.IS_REACT_ACT_ENVIRONMENT` 设置为 `true`：

```js
// 测试配置文件中
globalThis.IS_REACT_ACT_ENVIRONMENT = true;
```

这个配置项的目的是告诉 React 它正运行于一个类似单元测试的环境中。如果你忘记用 `act` 包裹一个更新的话，React 会记录有帮助的告警信息。

你也可以将其设置为 `false` 告诉 React 不需要 `act`。这对于要模拟完整浏览器环境的端到端测试非常有用。

最终我们希望测试库会自动为你配置这些。例如，[下一个版本的 React Testing Library 对于 React 18 提供了内置支持](https://github.com/testing-library/react-testing-library/issues/509#issuecomment-917989936) 而不需要额外的配置。

[更多关于 `act` 测试 API 的背景资料和相关的修改](https://github.com/reactwg/react-18/discussions/102) 可在工作组获取。

## 放弃对 Internet Explorer 的支持 {/*dropping-support-for-internet-explorer*/}

在本次发布中，React 正在放弃对 Internet Explorer 的支持，[最终会在 2022 年 6 月 15 日完全放弃](https://blogs.windows.com/windowsexperience/2021/05/19/the-future-of-internet-explorer-on-windows-10-is-in-microsoft-edge)。我们现在正在做这一变更，因为 React 18 中引入的新特性是使用现代浏览器特性构建的，例如在 IE 中不能 polyfill 的微任务。

如果你需要支持 Internet Explorer，我们推荐你保持在 React 17。

## 废弃 {/*deprecations*/}

* `react-dom`：`ReactDOM.render` 已经被废弃。使用它会发出警告并且让应用运行在 React 17 模式下。
* `react-dom`：`ReactDOM.hydrate` 已经被废弃。使用它会发出警告并且让应用运行在 React 17 模式下。
* `react-dom`：`ReactDOM.unmountComponentAtNode` 已经被废弃。
* `react-dom`：`ReactDOM.renderSubtreeIntoContainer` 已经被废弃。
* `react-dom/server`：`ReactDOMServer.renderToNodeStream` 已经被废弃。

## 其他破坏性变更 {/*other-breaking-changes*/}

* **一致的 useEffect 时间**：现在，如果更新是在类似点击或者敲击键盘事件这样的离散用户输入事件期间触发，React 总是同步刷新 Effect 函数。而之前的行为不是一直可预测或者一致的。
* **更严格的激活报错**：由于缺失或者额外的文本而导致的激活内容不匹配现在会作为错误而不是告警对待。React 将不再试图通过在客户端增加或删除节点来“修补”单个节点来匹配服务端标记，并且将会回退客户端渲染到树中最近的 `<Suspense>` 边界。这可以保证激活树保持一致并且避免可能由激活内容不匹配导致的隐私和安全漏洞。
* **Suspense 树一直保持一致**：如果一个组件在它完全被添加到树上之前挂起，React 将不会把它以不完整的状态添加到树或者触发它的 effect。React 会完全扔掉新树，等待异步操作结束，然后重新尝试从头开始再次渲染。React 会同时渲染重试尝试，并且不会阻塞浏览器。
* **使用 Suspense 的 Layout Effect**：当一个树重新挂起并恢复为后备方案时，现在的 React 会清理 layout effect，然后在边界内的内容再次显示时重新创建它们。这修复了一个在与 Suspense 一起使用时的问题：阻止组件库正确测量布局。
* **新的 JavaScript 环境要求**：React 现在依赖于现代浏览器特性，包括 `Promise`、`Symbol` 和 `Object.assign`。如果你需要支持像 Internet Explorer 这样较老版本的浏览器和设备，它们本身不提供现代浏览器特性或者有不兼容的实现，可以考虑在打包后的应用中包含全局的 polyfill。

## 其他值得注意的变化 {/*other-notable-changes*/}

### React {/*react*/}

* **组件现在可以渲染 `undefined`**：如果你从组件返回 `undefined`，React 不会再发出告警。这使得允许的组件返回值与组件树中间允许的值能够保持一致。我们建议使用代码检查工具来防止像忘记在 JSX 前面的 `return` 语句这样的错误。
* **在测试中，`act` 告警现在是可选的**：如果你正在运行端对端的测试，`act` 告警是非必要的。我们已经引入了一个 [可选](https://github.com/reactwg/react-18/discussions/102) 机制，这样你就可以只在有用且有益的单元测试开启它们。
* **未加载的组件取消了关于 `setState` 的告警**：之前每当你在未加载的组件中调用 `setState`，React 就会发出内存泄漏告警。这个告警是为订阅添加的，但是人们经常在设置状态完好遇见它并且解决方法会让代码变得更加糟糕。所以我们已经 [移除](https://github.com/facebook/react/pull/22114) 了这个告警。
* **不抑制控制台打印**：当你使用 Strict Mode 时，React 会将每个组件渲染两次来帮助你找到不符合预期的副作用。在 React 17 中，我们已经抑制了两次渲染之一的控制台打印让其更容易阅读。为了响应关于这会令人难以理解的 [社区反馈](https://github.com/facebook/react/issues/21783)，我们移除了这个抑制。取而代之的是，如果你安装了 React DevTool，第二次记录的渲染将会以灰色的文字展示并且会有一个选项（默认关闭）来抑制它们。
* **改进了内存使用**：React 现在在卸载的时候会清理更多内部区域，这使得可能存在于应用代码中的未修复内存泄露的影响不那么严重。

### React DOM Server {/*react-dom-server*/}

* **`renderToString`**：当在服务端挂起时，它不再会报错。而是会为最接近的 `<Suspense>` 边界发射后备 HTML，然后在客户端尝试渲染同样的内容。我们仍然推荐你切换到像 `renderToPipeableStream` 或者 `renderToReadableStream` 这样的流式 API。
* **`renderToStaticMarkup`**：当在服务端挂起时，它不再会报错。而是会为最接近的 `<Suspense>` 边界发射后备 HTML。

## 更新日志 {/*changelog*/}

你可以在这里查看 [完整更新日志](https://github.com/facebook/react/blob/main/CHANGELOG.md)。

---
# Source: react-v18.md
---
---
title: "React v18.0"
author: The React Team
date: 2022/03/08
description: React 18 现在可以在 npm 上使用啦！在我们的上一篇文章里，我们分享了将你的应用更新到 React 18 的分步说明。在这篇文章里，我们将会概述 React 18 究竟有哪些更新，以及这些更新对于未来的意义。
---

2022 年 3 月 29 日，由 [React 团队](/community/team) 发布

---

<Intro>

React 18 现在可以在 npm 上使用啦！在我们的上一篇文章里，我们分享了 [将你的应用更新到 React 18](/blog/2022/03/08/react-18-upgrade-guide) 的每一个步骤。在这篇文章里，我们将会概述 React 18 究竟有哪些更新，以及这些更新对于未来的意义。

</Intro>

---

我们最新的主要版本包含了开箱即用的改进，如自动批处理、`startTransition` 等新 API，以及支持 Suspense 的流式服务端渲染。

React 18 的许多新功能都建立在新推出的并发渲染特性之上，也就是一种解锁全新能力的底层变动。并发模式 React 是选择性启用的——只有当你使用了一个并发功能的时候才会开启——但是我们认为它将会对人们构建应用的方式产生巨大的影响。

我们花了很多年时间来研发 React 的并发渲染，同时我们也还考虑为现有用户提供一种过渡的路径。去年夏天，[我们成立了 React 18 工作组](/blog/2021/06/08/the-plan-for-react-18) 来收集社区专家们的反馈信息，保证整个 React 生态都能有一个丝滑的升级体验。

如果你忘了，我们在 React 大会 2021 上公开提出了这个愿景：

* 在 [摘要](https://www.youtube.com/watch?v=FZ0cG47msEk&list=PLNG_1j3cPCaZZ7etkzWA7JfdmKWT0pMsa) 中，我们解释了 React 18 为什么能够实现让开发者创造更好的用户体验这一使命。
* [Shruti Kapoor](https://twitter.com/shrutikapoor08) [示范了如何使用 React 18 中的新功能](https://www.youtube.com/watch?v=ytudH8je5ko&list=PLNG_1j3cPCaZZ7etkzWA7JfdmKWT0pMsa&index=2)。
* [Shaundai Person](https://twitter.com/shaundai) 为我们大概介绍了 [支持 Suspense 的流式服务端渲染](https://www.youtube.com/watch?v=pj5N-Khihgc&list=PLNG_1j3cPCaZZ7etkzWA7JfdmKWT0pMsa&index=3)。

以下是一个在此版本中对需要关注的内容的总结，先从并发渲染开始介绍。

<Note>

对于 React Native 用户而言，React 18 将会伴随新的 React Native 体系结构发布。想了解更多信息，可以阅读 [React Conf 摘要](https://www.youtube.com/watch?v=FZ0cG47msEk&t=1530s)。

</Note>

## 什么是并发 React？ {/*what-is-concurrent-react*/}

React 18 中最重要的更新内容是我们希望你永远不会考虑的：并发。我们认为这对于应用开发者而言是一件非常好的事情，尽管这对于库的维护者来说可能有点复杂。

并发渲染本身并不是一个功能。它是一个新的底层机制，使得 React 能够同时准备多个版本的 UI。你可以把并发视为一种底层实现的细节——它解锁了许多新功能因而非常有价值。React 在底层实现上使用了非常复杂的技术，如优先队列和多级缓冲。但是你不会在任何公共 API 中感知到这些。

在设计 API 时，我们刻意隐藏了实现细节。作为一名 React 开发者，你只需要关注视图是 **什么** 样子，然后由 React 来处理 **如何** 来实现，所以我们不需要 React 开发者了解并发的底层运行原理。

不过，并发模式 React 比典型的实现细节更重要──它是 React 核心渲染模型的基础性更新。因此，尽管了解并发渲染底层工作原理不是很重要，但如果是为了追求更高的技术层次，倒是值得去了解它。

并发模式的一个关键特性是渲染可中断。当首次升级到 React 18，在加入任何并发功能之前，更新内容渲染的方式和 React 之前的版本一样——通过一个单一的且不可中断的同步事务进行处理。同步渲染意味着，一旦开始渲染就无法中断，直到用户可以在屏幕上看到渲染结果。

在并发渲染中，情况并不总是如此。React 可能开始渲染一个更新，然后中途挂起，稍后又继续。它甚至可能完全放弃一个正在进行的渲染。React 保证即使渲染被中断，UI 也会保持一致。为了实现这一点，它会在整个 DOM 树被计算完毕前一直等待，完毕后再执行 DOM 变更。这样做，React 就可以在后台提前准备新的屏幕内容，而不阻塞主线程。这意味着用户输入可以被立即响应，即使存在大量渲染任务，也能有流畅的用户体验。

另一个例子是可重用状态。并发 React 可以从屏幕中移除部分 UI，然后在稍后将它们再添加回来，并重用之前的状态。例如，当用户来回切换标签页，React 应该能够立即将屏幕恢复到它先前的状态。在即将到来的次要版本中，我们计划添加一个新的名为 `<Offscreen>` 的组件，它实现了这种模式。同样地，你将能够使用 Offscreen 在后台准备新的 UI，在显示前就准备完毕以便快速响应。

并发渲染是一个 React 中非常强大的工具，并且我们大多数新功能都是利用了它的优势来创建的，包括 Suspense，transition 和流式服务端渲染。但是在并发渲染这个方向，React 18 也仅仅只是实现我们最终目标的第一步。

## 渐进式采用并发特性 {/*gradually-adopting-concurrent-features*/}

从技术上讲，并发渲染是一个破坏性变更。因为并发渲染是可中断的，因此在并发模式下组件的行为会略微不同。

在我们的测试过程中，我们已经把几千个组件更新到了 React 18。我们发现，几乎所有现有的组件都能在并发渲染下“正常工作”。然而部分组件可能需要一些额外的迁移工作。这种变化通常很小，你仍然可以按照自己的节奏进行使用。React 18 中的新渲染行为 **只在你的应用中使用新功能的部分启用**。

整体的升级策略是使你的应用基于 React 18 运行而不用破坏现存的代码，然后你可以渐进地按照你的节奏开始添加并发功能。你可以在开发环境中使用 [`<StrictMode>`](/reference/react/StrictMode) 以利于暴露并发模式相关的问题。严格模式是不影响生产环境的，但是在开发环境中它将会记录额外的警告日志，并且被视为幂等的函数将被调用两次。这没办法捕获所有异常，但是能够有效预防大部分常见的错误类型。

在升级到 React 18 后，可以立即开始使用并发模式的功能。例如，你可以使用 `startTransition` 在屏幕内容之间进行导航，而不会阻塞用户输入；或者使用 `useDeferredValue` 来节流处理开销巨大的重新渲染。

长远来看，我们希望你在应用中添加并发渲染能力的主要方式是，使用支持并发渲染的库或者框架。在大多数情况中，你不用与并发模式的 API 直接交互。例如，在导航到一个新的屏幕时，开发者无需调用 `startTransition`，路由库会自动将导航操作包裹在 `startTransition` 中。

这些库升级到兼容并发模式可能需要一些时间。我们已经提供了新的 API，使这些库更容易利用并发功能。同时，在我们努力逐步迁移 React 生态系统的过程中，请对维护者保持耐心。

如果想了解更多信息，可以查看我们之前的文章：[如何升级到 React 18](/blog/2022/03/08/react-18-upgrade-guide)。

## 数据框架中的 Suspense {/*suspense-in-data-frameworks*/}

在 React 18 中，你可以在 Relay，Next.js，Hydrogen 或者 Remix 等框架中获取数据。临时使用 [Suspense](/reference/react/Suspense) 获取数据在技术上是可行的，但是不建议作为一般方案。

在未来，我们可能会暴露更多原语，使你能用 `Suspense` 更容易地获取数据，那时也就不一定必须要使用某个的框架。不过，Suspense 被深度整合到你的应用结构中时能产生最好的效果：你的路由，你的数据层，你的服务端渲染环境。因此我们预计，即使在未来相当长一段时间里，库和框架也还会在 React 生态中发挥关键作用。

就像在过去的 React 的版本中，你总是可以使用 Suspense 与客户端侧的 `React.lazy` 配合进行代码分割。但是我们的对 Suspense 的期望并不仅仅是加载代码——最终的目标是扩展对 Suspense 的支持，以至于相同的声明式 Suspense 后备方案能够处理任何异步操作（加载代码，数据，图片等）。

## 服务器组件仍在开发中 {/*server-components-is-still-in-development*/}

[**服务器组件**](/blog/2020/12/21/data-fetching-with-react-server-components) 是一个即将到来的功能，允许开发者构建跨越服务端和客户端的应用，结合客户端应用丰富的交互性和传统服务端渲染的优良性能，服务器组件和并发模式 React 并不是强耦合的，但是它设计的初衷就是为了配合 Suspense 和流式服务端渲染这样的并发功能。

服务器组件仍然是实验性的，但是我们预计会在 18.x 的一个小版本中正式发布。同时，我们正在与 Next.js，Hydrogen 和 Remix 等框架合作，以推进提案，并使其准备好被广泛采用。

## React 18 的新内容 {/*whats-new-in-react-18*/}

### 新功能：自动批处理 {/*new-feature-automatic-batching*/}

批处理是指，当 React 在一个单独的重渲染事件中批量处理多个状态更新以此实现优化性能。如果没有自动批处理的话，我们仅能够在 React 事件处理程序中批量更新。在 React 18 之前，默认情况下 `promise`、`setTimeout`、原生应用的事件处理程序以及任何其他事件中的更新都不会被批量处理；但现在，这些更新内容都会被自动批处理：


```js
// 以前: 只有 React 事件会被批处理。
setTimeout(() => {
  setCount(c => c + 1);
  setFlag(f => !f);
  // React 会渲染两次，每次更新一个状态（没有批处理）
}, 1000);

// 现在: 超时，promise，本机事件处理程序
// 原生应用时间处理程序或者任何其他时间都被批处理了
setTimeout(() => {
  setCount(c => c + 1);
  setFlag(f => !f);
  // 最终，React 将仅会重新渲染一次（这就是批处理！）
}, 1000);
```

想要了解更多信息，可以阅读 [React 18 中能减少渲染次数的自动批处理机制](https://github.com/reactwg/react-18/discussions/21)。

### 新功能：过渡更新 {/*new-feature-transitions*/}

过渡（transition）更新是 React 中一个新的概念，用于区分紧急和非紧急的更新。

* **紧急更新** 对应直接的交互，如输入，点击，按压等。
* **过渡更新** 将 UI 从一个视图过渡到另一个。

像输入，点击，按压等紧急更新，需要立刻响应以符合人们对物理对象行为的预期。否则，他们就会觉得“不对劲”。但是，过渡更新不太一样，因为用户对感知到屏幕上的每一个中间值这件事是没有预期的。

举个例子，当我们在一个下拉菜单中选择了一个过滤器，你期望的是这个过滤器按钮在你点击的时候立即就能响应。然而，实际结果可能是不连贯的过渡。这样一个较短的延迟是难以察觉的，而且这往往也是能符合预期的。并且如果你在渲染完成之前，再次改变了过滤器，你需要关心的其实只是最新的结果。

通常情况下，为了更好的用户体验，一个用户输入应该同时产生一个紧急更新和一个过渡更新。你可以在一个输入事件中使用 `startTransition` API 告诉 React 哪些更新是紧急更新，哪些又是过渡更新：


```js
import { startTransition } from 'react';

// 紧急更新: 显示输入的内容
setInputValue(input);

// 将任何内部的状态更新都标记为过渡更新
startTransition(() => {
  // 过渡更新: 展示结果
  setSearchQuery(input);
});
```


被包裹在 `startTransition` 中的更新会被处理为过渡更新，如果有紧急更新出现，比如点击或者按键，则会中断过渡更新。如果一个过渡更新被用户中断（比如，快速输入多个字符），React 将会抛弃未完成的渲染结果，然后仅渲染最新的内容。


* `useTransition`： 一个用于开启过渡更新的 Hook，用于跟踪待定转场状态。
* `startTransition`： 当 Hook 不能使用时，用于开启过渡的方法。

并发渲染中将会加入过渡更新，允许更新被中断。如果更新内容被重新挂起，过渡机制也会告诉 React 在后台渲染过渡内容时继续展示当前内容（查看 [Suspense 意见征求](https://github.com/reactjs/rfcs/blob/main/text/0213-suspense-in-react-18.md) 了解更多信息）。

[更多内容请参阅 Transition 相关的文档](/reference/react/useTransition)。

### 新的 Suspense 特性 {/*new-suspense-features*/}

Suspense 允许你声明式地为一部分还没有准备好被展示的组件树指定加载状态：

```js
<Suspense fallback={<Spinner />}>
  <Comments />
</Suspense>
```

Suspense 使得“UI 加载状态”成为了 React 编程模型中最高级的声明式概念。我们基于此能够构建更高级的功能。

几年前，我们推出了一个受限制版的 Suspense。但是唯一支持的场景就是用 `React.lazy` 拆分代码，而且在服务端渲染时完全没有作用。

在 React 18 中，我们已经支持了服务端 Suspense，并且使用并发渲染特性扩展了其功能。

React 18 中的 Suspense 在与 Transition API 结合时效果最好。如果你在 Transition 期间挂起，React 不会让已显示的内容被后备方案取代。相反，React 会延迟渲染，直到有足够的数据，以防止出现加载状态错误。

更多内容参见 [React 18 中的 Suspense](https://github.com/reactjs/rfcs/blob/main/text/0213-suspense-in-react-18.md) 的意见征求。

### 新的客户端和服务端渲染 APIs {/*new-client-and-server-rendering-apis*/}

我们利用这次版本更新的机会，重新设计了我们为在客户端和服务端进行渲染所暴露的 API。这些更改允许用户在升级到 React 18 使用新的 API 时，也能继续使用 React 17 中的旧 API。

#### React DOM Client {/*react-dom-client*/}

这些新的 API 现在可以从 `react-dom/client` 中导出：

* `createRoot`：为 `render` 或者 `unmount` 创建根节点的新方法。请用它替代 `ReactDOM.render`。如果没有它，React 18 中的新功能就无法生效。
* `hydrateRoot`：hydrate 服务端渲染的应用的新方法。使用它来替代 `ReactDOM.hydrate` 与新的 React DOM 服务端 API 一起使用。如果没有它，React 18 中的新功能就无法生效。

`createRoot` 和 `hydrateRoot` 都能接受一个新的可选参数叫做 `onRecoverableError`，它能在 React 在渲染或者激活过程发生错误后又恢复时，做日志记录对你进行通知。默认情况下，React 会使用 [`reportError`](https://developer.mozilla.org/en-US/docs/Web/API/reportError)，如果在老旧版本浏览器中，则会使用 `console.error`。


[参阅 React DOM Client 的文档](/reference/react-dom/client)。

#### React DOM Server {/*react-dom-server*/}

这些新的 API 现在可以从 `react-dom/server` 中导出，并且在服务端端完全支持流式 Suspense：

* `renderToPipeableStream`：用于 Node 环境中的流式渲染。
* `renderToReadableStream`：对新式的非主流运行时环境，比如 Deno 和 Cloudflare workers。

现有的 `renderToString` 方法仍然可以使用，但是并不推荐这样做。

[参阅 React DOM Server 的文档](/reference/react-dom/server)。
### 新的严格模式行为 {/*new-strict-mode-behaviors*/}

在未来，我们希望新增一个功能，允许 React 在保留状态的同时添加和移除 UI。例如，当一个用户标签页切出又切回时，React 应该能够立即将之前的页面内容恢复到它先前的状态。为了实现这一点，React 将在卸载后又重新挂载组件树时，复用之前的状态。

这个功能将给 React 应用带来更好的开箱即用能力，但要求组件能够灵活应对多次安装和销毁的副作用。对于大多数副作用不需要任何改动也依然能够生效，但是部分副作用需要保证它们只进行一次挂载或销毁。

为了利于暴露这些问题，React 18 为严格模式下的开发环境引入了一个新的检查机制。每当组件第一次挂载时，这个检查机制将自动卸载又重新挂载每个组件，并在第二次挂载时复用先前的状态。

在这个变更之前，React 是在挂载组件时产生一些副作用：

```
* React 装载组件
  * layout Effect 创建
  * Effect 创建
```


在 React 18 的严格模式下，React 在开发模式下将会模拟组件的卸载和挂载：

```
* React 挂载组件
  * layout Effect 创建
  * Effect 创建
* React 模拟卸载组件
  * layout Effect 销毁
  * Effect 销毁
* React 模拟挂载组件，并复用之前的状态
  * layout Effect 创建
  * Effect 创建
```

[参阅确保状态可复用的文档](/reference/react/StrictMode#fixing-bugs-found-by-re-running-effects-in-development)。

### 新的 Hook {/*new-hooks*/}

#### useId {/*useid*/}

`useId` 是一个新的Hook，用于生成在客户端和服务端两侧都独一无二的 id，避免激活后两侧内容不匹配。它主要用于需要唯一 id 的，具有集成 API 的组件库。这个更新不仅解决了一个在 React 17 及更低版本中的存在的问题，而且它会在 React 18 中发挥更重要的作用，因为新的流式服务端渲染响应 HTML 的方式将是无序的，需要独一无二的 id 作为索引。[参阅文档](/reference/react/useId)。

> Note
>
> `useId` **不是** 为了生成 [列表中的 key](/learn/rendering-lists#where-to-get-your-key)。key 应该根据你的数据生成。

#### useTransition {/*usetransition*/}

`useTransition` 和 `startTransition` 让你能够将一些状态更新标记为过渡更新。默认情况下，状态更新都被视为紧急更新。React 将允许紧急更新（例如，更新一个文本输入内容）打断过渡更新（例如，渲染一个搜索结果列表）。[参阅文档](/reference/react/useTransition)。

#### useDeferredValue {/*usedeferredvalue*/}

`useDeferredValue` 允许推迟渲染树的非紧急更新。这和防抖操作非常相似，但是有一些改进。它没有固定的延迟时间，React 会在第一次渲染在屏幕上出现后立即尝试延迟渲染。延迟渲染是可中断的，它不会阻塞用户输入。[参阅文档](/reference/react/useDeferredValue)。

#### useSyncExternalStore {/*usesyncexternalstore*/}

`useSyncExternalStore` 是一个新的 Hook，允许使用第三方状态管理来支持并发模式，并且能通过对 store 进行强制更新实现数据同步。对第三方数据源的订阅能力的实现上，消除了对 `useEffect` 的依赖，推荐任何 React 相关的第三方状态管理库使用这个新特性。[参阅文档](/reference/react/useSyncExternalStore)。

> Note
>
> `useSyncExternalStore` 旨在供库使用，而不是应用程序代码。

#### useInsertionEffect {/*useinsertioneffect*/}

`useInsertionEffect` 是一个新的 Hook ，允许 CSS-in-JS 库解决在渲染中注入样式的性能问题。除非你已经建立了一个 CSS-in-JS 库，否则我们不希望你使用它。这个 Hook 将在 DOM 变更发生后，在 layout Effect 获取新布局之前运行。这个功能不仅解决了一个在 React 17 及以下版本中已经存在的问题，而且在 React 18 中更加重要，因为 React 在并发渲染时会为浏览器让步，给它一个重新计算布局的机会。[参阅文档](/reference/react/useInsertionEffect)。

> Note
>
> `useInsertionEffect` 旨在供库使用，而不是应用程序代码。

## 如何更新 {/*how-to-upgrade*/}

请参阅 [如何升级到 React 18](/blog/2022/03/08/react-18-upgrade-guide) 以获取分步说明和完整的中断列表以及值得注意的变化。

## 修改日志 {/*changelog*/}

### React {/*react*/}

* 添加 `useTransition` 和 `useDeferredValue` 以将紧急更新和过渡更新分开。([#10426](https://github.com/facebook/react/pull/10426)，[#10715](https://github.com/facebook/react/pull/10715)，[#15593](https://github.com/facebook/react/pull/15593)，[#15272](https://github.com/facebook/react/pull/15272)，[#15578](https://github.com/facebook/react/pull/15578)，[#15769](https://github.com/facebook/react/pull/15769)，[#17058](https://github.com/facebook/react/pull/17058)，[#18796](https://github.com/facebook/react/pull/18796)，[#19121](https://github.com/facebook/react/pull/19121)，[#19703](https://github.com/facebook/react/pull/19703)，[#19719](https://github.com/facebook/react/pull/19719)，[#19724](https://github.com/facebook/react/pull/19724)，[#20672](https://github.com/facebook/react/pull/20672)，[#20976](https://github.com/facebook/react/pull/20976) [@acdlite](https://github.com/acdlite)，[@lunaruan](https://github.com/lunaruan)，[@rickhanlonii](https://github.com/rickhanlonii)，and [@sebmarkbage](https://github.com/sebmarkbage))
* 添加 `useId` 用于生成唯一 ID。([#17322](https://github.com/facebook/react/pull/17322)，[#18576](https://github.com/facebook/react/pull/18576)，[#22644](https://github.com/facebook/react/pull/22644)，[#22672](https://github.com/facebook/react/pull/22672)，[#21260](https://github.com/facebook/react/pull/21260) [@acdlite](https://github.com/acdlite)，[@lunaruan](https://github.com/lunaruan)，and [@sebmarkbage](https://github.com/sebmarkbage))
* 添加 `useSyncExternalStore` 以帮助外部存储库与 React 集成。([#15022](https://github.com/facebook/react/pull/15022)，[#18000](https://github.com/facebook/react/pull/18000)，[#18771](https://github.com/facebook/react/pull/18771)，[#22211](https://github.com/facebook/react/pull/22211)，[#22292](https://github.com/facebook/react/pull/22292)，[#22239](https://github.com/facebook/react/pull/22239)，[#22347](https://github.com/facebook/react/pull/22347)，[#23150](https://github.com/facebook/react/pull/23150) [@acdlite](https://github.com/acdlite)，[@bvaughn](https://github.com/bvaughn)，and [@drarmstr](https://github.com/drarmstr))
* 添加 `startTransition` 作为 `useTransition` 的一个版本，不需要等待反馈。 ([#19696](https://github.com/facebook/react/pull/19696) [@rickhanlonii](https://github.com/rickhanlonii))
* 添加 `useInsertionEffect` 用于 CSS-in-JS 库。([#21913](https://github.com/facebook/react/pull/21913) [@rickhanlonii](https://github.com/rickhanlonii))
* 当内容重新出现时，使 Suspense 重新装载 layout effect。([#19322](https://github.com/facebook/react/pull/19322)，[#19374](https://github.com/facebook/react/pull/19374)，[#19523](https://github.com/facebook/react/pull/19523)，[#20625](https://github.com/facebook/react/pull/20625)，[#21079](https://github.com/facebook/react/pull/21079) [@acdlite](https://github.com/acdlite)，[@bvaughn](https://github.com/bvaughn)，and [@lunaruan](https://github.com/lunaruan))
* 使 `<StrictMode>` 重新运行 Effect 以检查可恢复的状态。([#19523](https://github.com/facebook/react/pull/19523) ，[#21418](https://github.com/facebook/react/pull/21418) [@bvaughn](https://github.com/bvaughn) and [@lunaruan](https://github.com/lunaruan))
* 假设 `Symbols` 总是可用的。([#23348](https://github.com/facebook/react/pull/23348) [@sebmarkbage](https://github.com/sebmarkbage))
* 移除 `object-assign` polyfill。([#23351](https://github.com/facebook/react/pull/23351) [@sebmarkbage](https://github.com/sebmarkbage))
* 移除不支持的 `unstable_changedBits` API。([#20953](https://github.com/facebook/react/pull/20953) [@acdlite](https://github.com/acdlite))
* 允许组件渲染 undefined。([#21869](https://github.com/facebook/react/pull/21869) [@rickhanlonii](https://github.com/rickhanlonii))
* 从个别事件（如点击），同步送出 useEffect 结果。([#21150](https://github.com/facebook/react/pull/21150) [@acdlite](https://github.com/acdlite))
* Suspense `fallback={undefined}` 现在与 `null` 的行为相同，不会被忽略。([#21854](https://github.com/facebook/react/pull/21854) [@rickhanlonii](https://github.com/rickhanlonii))
* 考虑所有 `lazy()` 解析为相同的等效组件。([#20357](https://github.com/facebook/react/pull/20357) [@sebmarkbage](https://github.com/sebmarkbage))
* 首次渲染时不要 patch 控制台。([#22308](https://github.com/facebook/react/pull/22308) [@lunaruan](https://github.com/lunaruan))
* 提高内存利用率。([#21039](https://github.com/facebook/react/pull/21039) [@bgirard](https://github.com/bgirard))
* 如果字符串强制抛出（Temporal.*，Symbol，等），改进提示信息。([#22064](https://github.com/facebook/react/pull/22064) [@justingrant](https://github.com/justingrant))
*使用 setImmediate 当它在 MessageChannel 上可用时。([#20834](https://github.com/facebook/react/pull/20834) [@gaearon](https://github.com/gaearon))
* 修复上下文无法在挂起的树内传播。([#23095](https://github.com/facebook/react/pull/23095) [@gaearon](https://github.com/gaearon))
* 通过移除紧急处理机制，修复 `useReducer` 观察到不正确的参数。([#22445](https://github.com/facebook/react/pull/22445) [@josephsavona](https://github.com/josephsavona))
* 修复 Safari 在追加 iframe 时忽略 `setState` 的问题。([#23111](https://github.com/facebook/react/pull/23111) [@gaearon](https://github.com/gaearon))
* 修复在树中渲染 `ZonedDateTime` 时的崩溃。([#20617](https://github.com/facebook/react/pull/20617) [@dimaqq](https://github.com/dimaqq))
* 修复在测试中文档被设置为 `null` 时的崩溃问题。([#22695](https://github.com/facebook/react/pull/22695) [@SimenB](https://github.com/SimenB))
* 修复 onLoad 在开启并发特性时不触发的问题。([#23316](https://github.com/facebook/react/pull/23316) [@gnoff](https://github.com/gnoff))
* 修复选择器返回 `NaN` 时的警告。([#23333](https://github.com/facebook/react/pull/23333) [@hachibeeDI](https://github.com/hachibeeDI))
* 修复在测试中文档被设置为 `null` 时的崩溃问题。([#22695](https://github.com/facebook/react/pull/22695) [@SimenB](https://github.com/SimenB))
* 修复生成的 License 头。([#23004](https://github.com/facebook/react/pull/23004) [@vitaliemiron](https://github.com/vitaliemiron))
* 添加 `package.json` 作为入口点之一。 ([#22954](https://github.com/facebook/react/pull/22954) [@Jack](https://github.com/Jack-Works))
* 允许在 Suspense 边界外挂起。([#23267](https://github.com/facebook/react/pull/23267) [@acdlite](https://github.com/acdlite))
* 每当激活失败时记录一个可恢复的错误。([#23319](https://github.com/facebook/react/pull/23319) [@acdlite](https://github.com/acdlite))

### React DOM {/*react-dom*/}

* 添加 `createRoot` 和 `hydrateRoot`。([#10239](https://github.com/facebook/react/pull/10239)，[#11225](https://github.com/facebook/react/pull/11225)，[#12117](https://github.com/facebook/react/pull/12117)，[#13732](https://github.com/facebook/react/pull/13732)，[#15502](https://github.com/facebook/react/pull/15502)，[#15532](https://github.com/facebook/react/pull/15532)，[#17035](https://github.com/facebook/react/pull/17035)，[#17165](https://github.com/facebook/react/pull/17165)，[#20669](https://github.com/facebook/react/pull/20669)，[#20748](https://github.com/facebook/react/pull/20748)，[#20888](https://github.com/facebook/react/pull/20888)，[#21072](https://github.com/facebook/react/pull/21072)，[#21417](https://github.com/facebook/react/pull/21417)，[#21652](https://github.com/facebook/react/pull/21652)，[#21687](https://github.com/facebook/react/pull/21687)，[#23207](https://github.com/facebook/react/pull/23207)，[#23385](https://github.com/facebook/react/pull/23385) [@acdlite](https://github.com/acdlite)，[@bvaughn](https://github.com/bvaughn)，[@gaearon](https://github.com/gaearon)，[@lunaruan](https://github.com/lunaruan)，[@rickhanlonii](https://github.com/rickhanlonii)，[@trueadm](https://github.com/trueadm)，and [@sebmarkbage](https://github.com/sebmarkbage))
* 添加选择性激活。([#14717](https://github.com/facebook/react/pull/14717)，[#14884](https://github.com/facebook/react/pull/14884)，[#16725](https://github.com/facebook/react/pull/16725)，[#16880](https://github.com/facebook/react/pull/16880)，[#17004](https://github.com/facebook/react/pull/17004)，[#22416](https://github.com/facebook/react/pull/22416)，[#22629](https://github.com/facebook/react/pull/22629)，[#22448](https://github.com/facebook/react/pull/22448)，[#22856](https://github.com/facebook/react/pull/22856)，[#23176](https://github.com/facebook/react/pull/23176) [@acdlite](https://github.com/acdlite)，[@gaearon](https://github.com/gaearon)，[@salazarm](https://github.com/salazarm)，and [@sebmarkbage](https://github.com/sebmarkbage))
* 在已知的 ARIA 属性列表中增加 `aria-description`。([#22142](https://github.com/facebook/react/pull/22142) [@mahyareb](https://github.com/mahyareb))
* 为 video 元素添加 `onResize` 事件。([#21973](https://github.com/facebook/react/pull/21973) [@rileyjshaw](https://github.com/rileyjshaw))
* 将 `imageSizes` 和 `imageSrcSet` 添加到已知属性中。([#22550](https://github.com/facebook/react/pull/22550) [@eps1lon](https://github.com/eps1lon))
* 若提供了 `value`，允许非字符串 `<option>` 子元素。  ([#21431](https://github.com/facebook/react/pull/21431) [@sebmarkbage](https://github.com/sebmarkbage))
* 修复 `aspectRatio` 样式未被应用的问题。 ([#21100](https://github.com/facebook/react/pull/21100) [@gaearon](https://github.com/gaearon))
* 若 `renderSubtreeIntoContainer` 被调用，发出警告。 ([#23355](https://github.com/facebook/react/pull/23355) [@acdlite](https://github.com/acdlite))

### React DOM Server {/*react-dom-server-1*/}

* 添加新的流式渲染器。([#14144](https://github.com/facebook/react/pull/14144)，[#20970](https://github.com/facebook/react/pull/20970)，[#21056](https://github.com/facebook/react/pull/21056)，[#21255](https://github.com/facebook/react/pull/21255)，[#21200](https://github.com/facebook/react/pull/21200)，[#21257](https://github.com/facebook/react/pull/21257)，[#21276](https://github.com/facebook/react/pull/21276)，[#22443](https://github.com/facebook/react/pull/22443)，[#22450](https://github.com/facebook/react/pull/22450)，[#23247](https://github.com/facebook/react/pull/23247)，[#24025](https://github.com/facebook/react/pull/24025)，[#24030](https://github.com/facebook/react/pull/24030) [@sebmarkbage](https://github.com/sebmarkbage))
* 修复 SSR 中的上下文提供者在处理多个请求时的问题。([#23171](https://github.com/facebook/react/pull/23171) [@frandiox](https://github.com/frandiox))
* 文本不匹配时恢复到客户端渲染。([#23354](https://github.com/facebook/react/pull/23354) [@acdlite](https://github.com/acdlite))
* 弃用 `renderToNodeStream`。([#23359](https://github.com/facebook/react/pull/23359) [@sebmarkbage](https://github.com/sebmarkbage))
* 修复新服务端渲染器中一个有误的错误日志。([#24043](https://github.com/facebook/react/pull/24043) [@eps1lon](https://github.com/eps1lon))
* 修复新服务端渲染器中的一个错误。([#22617](https://github.com/facebook/react/pull/22617) [@shuding](https://github.com/shuding))
* 忽略服务端自定义元素内的函数和符号值。([#21157](https://github.com/facebook/react/pull/21157) [@sebmarkbage](https://github.com/sebmarkbage))

### React DOM Test Utils {/*react-dom-test-utils*/}

* 在生产环境使用 `act` 时抛出错误。 ([#21686](https://github.com/facebook/react/pull/21686) [@acdlite](https://github.com/acdlite))
* 支持使用 `global.IS_REACT_ACT_ENVIRONMENT` 禁用 act 警告。 ([#22561](https://github.com/facebook/react/pull/22561) [@acdlite](https://github.com/acdlite))
* 扩大 act 警告，以覆盖所有可能预计 React 工作的 API。([#22607](https://github.com/facebook/react/pull/22607) [@acdlite](https://github.com/acdlite))
* 使 act 批量更新。([#21797](https://github.com/facebook/react/pull/21797) [@acdlite](https://github.com/acdlite))
* 移除对被挂起的 Effect 的警告。([#22609](https://github.com/facebook/react/pull/22609) [@acdlite](https://github.com/acdlite))

### React Refresh {/*react-refresh*/}

* 在快速刷新中跟踪后期装载的 root。([#22740](https://github.com/facebook/react/pull/22740) [@anc95](https://github.com/anc95))
* 在 `package.json` 中添加 `exports` 字段。([#23087](https://github.com/facebook/react/pull/23087) [@otakustay](https://github.com/otakustay))

### 实验性的服务器组件 {/*server-components-experimental*/}

* 增加服务端上下文支持。([#23244](https://github.com/facebook/react/pull/23244) [@salazarm](https://github.com/salazarm))
* 增加对 `lazy` 的支持。 ([#24068](https://github.com/facebook/react/pull/24068) [@gnoff](https://github.com/gnoff))
* 更新 webpack 插件以支持 webpack 5。([#22739](https://github.com/facebook/react/pull/22739) [@michenly](https://github.com/michenly))
* 修正 Noder loader 中的一个错误。([#22537](https://github.com/facebook/react/pull/22537) [@btea](https://github.com/btea))
* 在边缘环境中使用 `globalThis` 而不是 `window`。([#22777](https://github.com/facebook/react/pull/22777) [@huozhi](https://github.com/huozhi))

---
# Source: data-fetching-with-react-server-components.md
---
---
title: "介绍零打包大小的 React 服务器组件"
author: Dan Abramov, Lauren Tan, Joseph Savona, and Sebastian Markbage
date: 2020/12/21
description: 2020 年是漫长的一年。随着它的结束，我们想在节日里分享一份特别的更新，介绍我们对零打包大小的 React 服务器组件的研究。
---

2020 年 12 月 21 日 [Dan Abramov](https://bsky.app/profile/danabra.mov)、[Lauren Tan](https://twitter.com/potetotes)、[Joseph Savona](https://twitter.com/en_JS) 与 [Sebastian Markbåge](https://twitter.com/sebmarkbage)

---

<Intro>

2020 年是漫长的一年。随着它的结束，我们想在节日里分享一份特别的更新，介绍我们对零打包大小的 **React 服务器组件** 的研究。

</Intro>

---

为了介绍 React 服务器组件，我们准备了一次演讲和演示。如果你愿意，在假期期间或新年工作重新开始后查看它们。

<YouTubeIframe src="https://www.youtube.com/embed/TQQPAU21ZUw" />

**React 服务器组件仍处于研究和开发阶段**。我们将以透明的精神分享这项工作，并希望从 React 社区获得初步反馈。这个过程需要很多时间，所以 **你现在不必急着赶上进展**！

如果你想了解它们，我们建议按照以下顺序进行查看：

1. **观看演讲** 以了解 React 服务器组件并观看演示。

2. **[克隆演示](http://github.com/reactjs/server-components-demo)** 并在你的计算机上尝试使用 React 服务器组件。

3. **[阅读 RFC（文末有FAQ）](https://github.com/reactjs/rfcs/pull/188)** 以深入了解技术细节并提供反馈意见。

我们非常期待你对 RFC 的反馈或者通过 [@reactjs](https://twitter.com/reactjs) 的 Twitter 账号回复我们。祝你度过愉快的假期，保重，明年再见！

---
# Source: the-plan-for-react-18.md
---
---
title: "React 18 的有关计划"
author: Andrew Clark, Brian Vaughn, Christine Abernathy, Dan Abramov, Rachel Nabors, Rick Hanlon, Sebastian Markbage, and Seth Webster
date: 2021/06/08
description: React 团队很高兴分享一些更新。我们已经开始推进 React 18 的更新，也正是我们的下一个主要版本。我们已经创建了一些工作组，筹备 React 18 新功能在社区内逐步推广的相关工作。我们已经发布了一个 React 18 Alpha 版本，以便于一些库的作者们能够测试并反馈……
---

2021 年 7 月 8 日 [Andrew Clark](https://twitter.com/acdlite)、[Brian Vaughn](https://github.com/bvaughn)、[Christine Abernathy](https://twitter.com/abernathyca)、[Dan Abramov](https://bsky.app/profile/danabra.mov)、[Rachel Nabors](https://twitter.com/rachelnabors)、[Rick Hanlon](https://twitter.com/rickhanlonii)、[Sebastian Markbåge](https://twitter.com/sebmarkbage) 与 [Seth Webster](https://twitter.com/sethwebster)

---

<Intro>

React 团队很高兴分享一些更新：

1. 我们已经开始推进 React 18 的更新，也正是我们的下一个主要版本。
2. 我们已经创建了一些工作组，筹备 React 18 新功能在社区内逐步推广的相关工作。
3. 我们已经发布了一个 React 18 Alpha 版本，以便于一些库的作者们能够测试并反馈。

这些更新主要针对于第三方库的维护者们。如果你正在学习，教授或者使用 React 来构建面向用户的应用程序，你可以忽略这篇文章。但是如果你对此感到好奇，我们也非常欢迎你关注 React 18 工作组中的讨论。

---

</Intro>

## React 18 带来了什么 {/*whats-coming-in-react-18*/}

当 React 18 发布时，它将会有更好的开箱即用能力（如 [自动批处理](https://github.com/reactwg/react-18/discussions/21)），全新的 API（如 [`startTransition`](https://github.com/reactwg/react-18/discussions/41)），以及支持 `React.lazy` 的 [全新的流式服务端渲染](https://github.com/reactwg/react-18/discussions/37)。

这些功能之所以能够实现，要归功于我们在 React 18 中新加入的可选择性启用的机制，“并发渲染”，并且它使得 React 可以同时准备多个版本的 UI。这些大部分都是对底层的改动，但是也为你的应用程序提高其真实性能和用户感知性能创造了新的可能性，

如果你一直在关注我们对 React 的未来的研究（我们并不希望你这么做！），你可能已经听说过“并发模式”，或许还听说过它可能会对你的应用程序造成破坏性变更。为了回应社区对此的反馈，我们已经重新设计了渐进式的升级策略。相比于之前要么不升级，要么全部升级这样一刀切的方式，现在的只有被并发渲染相关的新功能触发的更新才会启用并发渲染。这对于工程实践的意义是，**你无需重写代码即可直接使用 React 18，并且可以根据自己的节奏和需求来尝试新特性**。

## 渐进式应用策略 {/*a-gradual-adoption-strategy*/}

由于并发机制在 React 18 中是一个可选功能，没有对组件行为造成明显的破坏性变更。**你几乎不需要对应用程序中的代码进行任何改动，就可以直接升级到 React 18，这比以往的 React 版本升级要容易许多**。根据我们自己将几个应用程序升级到 React 18 的经验来看，预计大多数用户能在一个下午的时间内完成升级工作。

我们在 Facebook 上成功地将并发功能赋予给了数以万计的组件，并且以我们的实践经验来看，大部分的 React 组件无需任何改动就能正常工作。今天我们成立了 React 18 工作组，我们将致力于保证整个社区都能顺利升级。

## 与社区合作 {/*working-with-the-community*/}

在这次更新中，我们正在尝试一些新的可能：我们邀请了 React 社区的专家、开发者、库的作者以及教育者参与我们的 [React 18 工作组](https://github.com/reactwg/react-18)，以提供反馈，咨询问题以及参与版本更新。我们没有没办法将所有人都邀请到这个刚建立的小群体，但是如果这次试验成功的话，我们也期待更多人的加入。

**React 18 工作组的目标是为生态做好准备，使现有的应用程序和库能够顺利、渐进地采用 React 18**。该工作组被托管在 [GitHub 讨论区](https://github.com/reactwg/react-18/discussions) 以供公众阅读。工作组的成员也可以留下反馈，咨询问题以及分享想法。核心团队也将会使用这个代码仓库的讨论区来分享我们的研发成果。在新版本变得越来越稳定的同时，所有重要信息都会在博客上发布。

想要了解关于升级到 React 18 的更多信息，或者关于该版本的其他资源，请参阅 [React 18 公告](https://github.com/reactwg/react-18/discussions/4)。

## 访问 React 18 工作组 {/*accessing-the-react-18-working-group*/}

每个人都可以阅读在 [React 18 工作组代码仓库](https://github.com/reactwg/react-18) 中的讨论信息。

我们预计对工作组感兴趣的人数会激增，所以目前只允许被邀请的成员可以创建或评论主题。不过，这些过程是完全公开的，所以每个人都能得到一致的信息。我们相信这是一个很好的折衷方案，既能为工作组的成员创造一个利于工作的环境，又能保持对广大社区的开放性。

和从前一样，你仍然可以在我们的 [issue](https://github.com/facebook/react/issues) 中发布错误报告、疑难问题和反馈等信息。

## 如何体验 React 18 alpha {/*how-to-try-react-18-alpha-today*/}

新的 alpha 版本是 [将 `@alpha` 标签定期发布到 npm 中](https://github.com/reactwg/react-18/discussions/9)。这些版本是由我们仓库主分支上最新的提交内容构建的。当一个新功能或者漏洞补丁被合并到主分支时，这些内容将在下一个工作日中出现在 alpha 版本中。

在 alpha 版本之间可能会有重大的行为逻辑或者 API 的变动。请谨记，**alpha 版本不建议在面向用户的生产环境应用中使用**。

## React 18 的预计发布时间 {/*projected-react-18-release-timeline*/}

我们没有明确的版本更新排期，但是我们预计在 React 18 可以满足大部分的生产环境应用之前，需要几个月的时间来收集反馈和迭代更新。

* 库的 Alpha 版本：今天可用
* 公开的 Beta 版：至少几个月
* RC 版本：至少在 Beta 版发布后的几周
* 正式版：至少在 RC 版本发布之后的几周

关于发布任务排期的更多细节都在 [走近工作组](https://github.com/reactwg/react-18/discussions/9)。当临近公开发布时，我们会在这个博客上发布更新。

---
# Source: react-conf-2021-recap.md
---
---
title: "回顾 React Conf 2021"
author: Jesslyn Tannady and Rick Hanlon
date: 2021/12/17
description: 上周，我们举办了第六届 React Conf。在以往的几年中，我们在 React Conf 的舞台上发布了行业改变的信息，如 React Native 和 React Hooks。今年，我们从发布 React 18 和逐步采用并发功能开始，分享了我们对 React 的多平台愿景。
---

2021 年 12 月 17 日 [Jesslyn Tannady](https://twitter.com/jtannady) 与 [Rick Hanlon](https://twitter.com/rickhanlonii)

---

<Intro>

上周，我们举办了第六届 React Conf。在以往的几年中，我们在 React Conf 的舞台上发布了行业改变的信息，如 [**React Native**](https://engineering.fb.com/2015/03/26/android/react-native-bringing-modern-web-techniques-to-mobile/) 和 [**React Hooks**](https://reactjs.org/docs/hooks-intro.html)。今年，我们从发布 React 18 和逐步采用并发功能开始，分享了我们对 React 的多平台愿景。

</Intro>

---

这是 React Conf 首次在线举办，并且免费直播，并翻译成 8 种不同的语言。来自世界各地的参与者参加了我们的会议 Discord 和针对所有时区都可访问的重播活动。超过 50000 人注册，19 场演讲总共有超过 60000 次观看，Discord 平台上两个活动共有 5000 名参与者。

所有的演讲都可以 [在线播放](https://www.youtube.com/watch?v=FZ0cG47msEk&list=PLNG_1j3cPCaZZ7etkzWA7JfdmKWT0pMsa)。

以下是大会分享内容的摘要：

## React 18 和并发特性 {/*react-18-and-concurrent-features*/}

在主题演讲中，我们分享了从 React 18 开始对未来 React 的愿景。

在没有引入任何重大的破坏性变化的情况下，React 18 添加了期待已久的并发渲染器和对 Suspense 的更新。应用程序可以升级到 React 18 并开始逐步采用并发功能，其工作量与任何其他主要版本相当。

**这意味着没有并发模式，只有并发功能**。

在主题演讲中，我们还分享了对 Suspense、服务器组件、新 React 工作组的愿景，以及对 React Native 的长期多平台愿景。

请在此处观看 [Andrew Clark](https://twitter.com/acdlite)、[Juan Tejada](https://twitter.com/_jstejada)、[Lauren Tan](https://twitter.com/potetotes) 和 [Rick Hanlon](https://twitter.com/rickhanlonii) 的完整主题演讲：

<YouTubeIframe src="https://www.youtube.com/embed/FZ0cG47msEk" />

## 面向应用程序开发人员的 React 18 {/*react-18-for-application-developers*/}

在主题演讲中，我们还宣布 React 18 RC 现已可供试用。在等待进一步的反馈之前，这是我们将于明年初发布稳定版的 React 版本。

要尝试 React 18 RC，请升级你的依赖项：

```bash
npm install react@rc react-dom@rc
```

并切换到新的 **createRoot** API：

```js
// 切换前
const container = document.getElementById('root');
ReactDOM.render(<App />, container);

// 切换后
const container = document.getElementById('root');
const root = ReactDOM.createRoot(container);
root.render(<App/>);
```

有关升级到 React 18 的演示，请参阅 [Shruti Kapoor](https://twitter.com/shrutikapoor08) 的演讲：

<YouTubeIframe src="https://www.youtube.com/embed/ytudH8je5ko" />

## Suspense 串流服务端渲染 {/*streaming-server-rendering-with-suspense*/}

React 18 还包括使用 Suspense 对服务端渲染性能的改进。

串流服务端渲染允许你从服务器上的 React 组件生成 HTML，并将该 HTML 流式传输给用户。在 React 18 中，你可以使用 **Suspense** 将应用程序分解为更小的独立单元，这些单元可以彼此独立地进行流式传输，而不会阻塞应用程序的其余部分。这意味着用户将更快地看到你的内容，并能够更快地开始与之交互。

如需深入了解，请参阅 [Shaundai Person](https://twitter.com/shaundai) 的演讲：

<YouTubeIframe src="https://www.youtube.com/embed/pj5N-Khihgc" />

## 第一个 React 工作组 {/*the-first-react-working-group*/}

对于 React 18，我们创建了第一个工作组，与专家、开发人员、库维护人员和教育工作者小组合作。我们共同制定了逐步采用策略并完善了新的 API，例如 **useId**、**useSyncExternalStore** 和 **useInsertionEffect**。

有关这项工作的概述，请参阅 [Aakansha' Doshi](https://twitter.com/aakansha1216) 的演讲：

<YouTubeIframe src="https://www.youtube.com/embed/qn7gRClrC9U" />

## React 开发者工具 {/*react-developer-tooling*/}

为了支持此版本中的新功能，我们还宣布了新成立的 React DevTools 团队和新的 Timeline Profiler，以帮助开发人员调试他们的 React 应用程序。

有关新 DevTools 功能的更多信息和演示，请参阅 [Brian Vaughn](https://twitter.com/brian_d_vaughn) 的演讲：

<YouTubeIframe src="https://www.youtube.com/embed/oxDfrke8rZg" />

## 没有 memo 的 React {/*react-without-memo*/}

展望未来，[Xuan Huang (黄玄)](https://twitter.com/Huxpro) 分享了我们的 React Labs 对自动记忆编译器的研究的更新。查看此演讲以获取更多信息和编译器原型的演示：

<YouTubeIframe src="https://www.youtube.com/embed/lGEMwh32soc" />

## React 文档主题演讲 {/*react-docs-keynote*/}

[Rachel Nabors](https://twitter.com/rachelnabors) 开始了有关 React 学习和设计的部分演讲，并发表了关于我们对 React 新文档（[现已作为 React.dev 发布](/blog/2023/03/16/introducing-react-dev)）的投入的主题演讲：

<YouTubeIframe src="https://www.youtube.com/embed/mneDaMYOKP8" />

## 以及更多 {/*and-more*/}

**我们还听到了有关使用 React 进行学习和设计的演讲**：

* 由 Debbie O'Brien 演讲的 [Things I learnt from the new React docs](https://youtu.be/-7odLW_hG7s)。
* 由 Sarah Rainsberger 演讲的 [Learning in the Browser](https://youtu.be/5X-WEQflCL0)。
* 由 Linton Ye 演讲的 [The ROI of Designing with React](https://youtu.be/7cPWmID5XAk)。
* 由 Delba de Oliveira 演讲的 [Interactive playgrounds with React](https://youtu.be/zL8cz2W0z34)。

**来自 Relay、React Native 和 PyTorch 团队的演讲**：

* 由 Robert Balicki 演讲的 [Re-introducing Relay](https://youtu.be/lhVGdErZuN4)。
* 由 Eric Rozell 和 Steven Moyes 演讲的 [React Native Desktop](https://youtu.be/9L4FFrvwJwY)。
* 由 Roman Rädle 演讲的 [On-device Machine Learning for React Native](https://youtu.be/NLj73vrc2I8)。

**社区中关于可访问性、工具和服务器组件的演讲**：

* 由 Daishi Kato 演讲的 [React 18 for External Store Libraries](https://youtu.be/oPfSC5bQPR8)。
* 由 Diego Haz 演讲的 [Building Accessible Components in React 18](https://youtu.be/dcm8fjBfro8)。
* 由 Tafu Nakazaki 演讲的 [Accessible Japanese Form Components with React](https://youtu.be/S4a0QlsH0pU).
* 由 Lyle Troxell 演讲的 [UI tools for artists](https://youtu.be/b3l4WxipFsE)。
* 由 Helen Lin 演讲的 [Hydrogen + React 18](https://youtu.be/HS6vIYkSNks)。

## 感谢 {/*thank-you*/}

这是我们自己策划会议的第一年，我们要感谢很多人。

首先，感谢所有演讲者 [Aakansha Doshi](https://twitter.com/aakansha1216),、 [Andrew Clark](https://twitter.com/acdlite)、[Brian Vaughn](https://twitter.com/brian_d_vaughn)、[Daishi Kato](https://twitter.com/dai_shi)、[Debbie O'Brien](https://twitter.com/debs_obrien)、[Delba de Oliveira](https://twitter.com/delba_oliveira)、[Diego Haz](https://twitter.com/diegohaz)、[Eric Rozell](https://twitter.com/EricRozell)、[Helen Lin](https://twitter.com/wizardlyhel)、[Juan Tejada](https://twitter.com/_jstejada)、[Lauren Tan](https://twitter.com/potetotes)、[Linton Ye](https://twitter.com/lintonye)、[Lyle Troxell](https://twitter.com/lyle)、[Rachel Nabors](https://twitter.com/rachelnabors)、[Rick Hanlon](https://twitter.com/rickhanlonii)、[Robert Balicki](https://twitter.com/StatisticsFTW)、[Roman Rädle](https://twitter.com/raedle)、[Sarah Rainsberger](https://twitter.com/sarah11918)、[Shaundai Person](https://twitter.com/shaundai)、[Shruti Kapoor](https://twitter.com/shrutikapoor08)、[Steven Moyes](https://twitter.com/moyessa)、[Tafu Nakazaki](https://twitter.com/hawaiiman0) 和 [Xuan Huang (黄玄)](https://twitter.com/Huxpro)。

感谢所有为会谈提供反馈的人，包括  [Andrew Clark](https://twitter.com/acdlite)、[Dan Abramov](https://bsky.app/profile/danabra.mov)、[Dave McCabe](https://twitter.com/mcc_abe)、[Eli White](https://twitter.com/Eli_White)、[Joe Savona](https://twitter.com/en_JS)、 [Lauren Tan](https://twitter.com/potetotes)、[Rachel Nabors](https://twitter.com/rachelnabors) 和 [Tim Yung](https://twitter.com/yungsters)。

感谢 [Lauren Tan](https://twitter.com/potetotes) 组织了 Discord 会议并担任我们的 Discord 管理员。

感谢 [Seth Webster](https://twitter.com/sethwebster) 对总体方向的反馈，并确保我们专注于多样性和包容性。

感谢 [Rachel Nabors](https://twitter.com/rachelnabors) 领导我们的审核工作，感谢 [Aisha Blake](https://twitter.com/AishaBlake) 创建我们的审核指南、领导我们的审核团队、培训翻译人员和审核人员以及帮助审核这两项活动。

感谢我们的会议主席 [Jesslyn Tannady](https://twitter.com/jtannady)、[Suzie Grange](https://twitter.com/missuze)、[Becca Bailey](https://twitter.com/beccaliz)、[Luna Wei](https://twitter.com/lunaleaps)、[Joe Previte](https://twitter.com/jsjoeio)、[Nicola Corti](https://twitter.com/Cortinico)、[Gijs Weterings](https://twitter.com/gweterings)、[Claudio Procida](https://twitter.com/claudiopro)、Julia Neumann、Mengdi Chen、Jean Zhang、Ricky Li 和 [Xuan Huang (黄玄)](https://twitter.com/Huxpro)。

感谢来自 [React India](https://www.reactindia.io/) 的 [Manjula Dube](https://twitter.com/manjula_dube)、[Sahil Mhapsekar](https://twitter.com/apheri0) 和 Vihang Patel，以及来自 [React China](https://twitter.com/ReactChina) 的 [Jasmine Xie](https://twitter.com/jasmine_xby)、[QiChang Li](https://twitter.com/QCL15) 和 [YanLun Li](https://twitter.com/anneincoding) 帮助主持我们的重播活动并保持其对社区的吸引力。

感谢 Vercel 发布了会议网站所基于的 [虚拟活动入门套件](https://vercel.com/virtual-event-starter-kit)，并感谢 [Lee Robinson](https://twitter.com/leeerob) 和 [Delba de Oliveira](https://twitter.com/delba_oliveira) 分享了他们举办 Next.js Conf 的经验。

感谢 [Leah Silber](https://twitter.com/wifelette) 分享她举办会议的经验、从举办 [RustConf](https://rustconf.com/) 中学到的知识，以及她的书 [《事件驱动》](https://leanpub.com/eventdriven/) 及其包含的关于举办会议的建议。

感谢 [Kevin Lewis](https://twitter.com/_phzn) 和 [Rachel Nabors](https://twitter.com/rachelnabors) 分享了她们举办 Women of React Conf 的经验。

感谢 [Aakansha Doshi](https://twitter.com/aakansha1216)、[Laurie Barth](https://twitter.com/laurieontech)、[Michael Chan](https://twitter.com/chantastic) 和 [Shaundai Person](https://twitter.com/shaundai) 在整个规划过程中提供的建议和想法。

感谢 [Dan Lebowitz](https://twitter.com/lebo) 帮助设计和构建会议网站和门票。

感谢 Laura Podolak Waddell、Desmond Osei-Acheampong、Mark Rossi、Josh Toberman 以及 Facebook 视频制作团队的其他人员录制了主题演讲和 Meta 员工演讲的视频。

感谢我们的合作伙伴 HitPlay 帮助组织会议、编辑直播中的所有视频、翻译所有演讲以及以多种语言主持 Discord。

最后，感谢所有参与者让本次 React Conf 变得精彩！

---
# Source: react-compiler-1.md
---
---
title: "React Compiler v1.0"
author: Lauren Tan, Joe Savona, and Mofei Zhang
date: 2025/10/07
description: We are releasing the compiler's first stable release today.

---

Oct 7, 2025 by [Lauren Tan](https://x.com/potetotes), [Joe Savona](https://x.com/en_JS), and [Mofei Zhang](https://x.com/zmofei).

---

<Intro>

The React team is excited to share new updates:

</Intro>

1. React Compiler 1.0 is available today.
2. Compiler-powered lint rules ship in `eslint-plugin-react-hooks`'s `recommended` and `recommended-latest` preset.
3. We've published an incremental adoption guide, and partnered with Expo, Vite, and Next.js so new apps can start with the compiler enabled.

---

We are releasing the compiler's first stable release today. React Compiler works on both React and React Native, and automatically optimizes components and hooks without requiring rewrites. The compiler has been battle tested on major apps at Meta and is fully production-ready.

[React Compiler](/learn/react-compiler) is a build-time tool that optimizes your React app through automatic memoization. Last year, we published React Compiler's [first beta](/blog/2024/10/21/react-compiler-beta-release) and received lots of great feedback and contributions. We're excited about the wins we've seen from folks adopting the compiler (see case studies from [Sanity Studio](https://github.com/reactwg/react-compiler/discussions/33) and [Wakelet](https://github.com/reactwg/react-compiler/discussions/52)) and are excited to bring the compiler to more users in the React community.

This release is the culmination of a huge and complex engineering effort spanning almost a decade. The React team's first exploration into compilers started with [Prepack](https://github.com/facebookarchive/prepack) in 2017. While this project was eventually shut down, there were many learnings that informed the team on the design of Hooks, which were designed with a future compiler in mind. In 2021, [Xuan Huang](https://x.com/Huxpro) demoed the [first iteration](https://www.youtube.com/watch?v=lGEMwh32soc) of a new take on React Compiler.

Although this first version of the new React Compiler was eventually rewritten, the first prototype gave us increased confidence that this was a tractable problem, and the learnings that an alternative compiler architecture could precisely give us the memoization characteristics we wanted. [Joe Savona](https://x.com/en_JS), [Sathya Gunasekaran](https://x.com/_gsathya), [Mofei Zhang](https://x.com/zmofei), and [Lauren Tan](https://x.com/potetotes) worked through our first rewrite, moving the compiler's architecture into a Control Flow Graph (CFG) based High-Level Intermediate Representation (HIR). This paved the way for much more precise analysis and even type inference within React Compiler. Since then, many significant portions of the compiler have been rewritten, with each rewrite informed by our learnings from the previous attempt. And we have received significant help and contributions from many members of the [React team](/community/team) along the way.

This stable release is our first of many. The compiler will continue to evolve and improve, and we expect to see it become a new foundation and era for the next decade and more of React.

You can jump straight to the [quickstart](/learn/react-compiler), or read on for the highlights from React Conf 2025.

<DeepDive>

#### How does React Compiler work? {/*how-does-react-compiler-work*/}

React Compiler is an optimizing compiler that optimizes components and hooks through automatic memoization. While it is implemented as a Babel plugin currently, the compiler is largely decoupled from Babel and lowers the Abstract Syntax Tree (AST) provided by Babel into its own novel HIR, and through multiple compiler passes, carefully understands data-flow and mutability of your React code. This allows the compiler to granularly memoize values used in rendering, including the ability to memoize conditionally, which is not possible through manual memoization.

```js {8}
import { use } from 'react';

export default function ThemeProvider(props) {
  if (!props.children) {
    return null;
  }
  // The compiler can still memoize code after a conditional return
  const theme = mergeTheme(props.theme, use(ThemeContext));
  return (
    <ThemeContext value={theme}>
      {props.children}
    </ThemeContext>
  );
}
```
_See this example in the [React Compiler Playground](https://playground.react.dev/#N4Igzg9grgTgxgUxALhASwLYAcIwC4AEwBUYCBAvgQGYwQYEDkMCAhnHowNwA6AdvwQAPHPgIATBNVZQANoWpQ+HNBD4EAKgAsEGBAAU6ANzSSYACix0sYAJRF+BAmmoFzAQisQbAOjha0WXEWPntgRycCFjxYdT45WV51Sgi4NTBCPB09AgBeAj0YAHMEbV0ES2swHyzygBoSMnMyvQBhNTxhPFtbJKdo2LcIpwAeFoR2vk6hQiNWWSgEXOBavQoAPmHI4C9ff0DghD4KLZGAenHJ6bxN5N7+ChA6kDS+ajQilHRsXEyATyw5GI+gWRTQfAA8lg8Ko+GBKDQ6AxGAAjVgohCyAC0WFB4KxLHYeCxaWwgQQMDO4jQGW4-H45nCyTOZ1JWECrBhagAshBJMgCDwQPNZEKHgQwJyae8EPCQVAwZDobC7FwnuAtBAAO4ASSmFL48zAKGksjIFCAA)_

In addition to automatic memoization, React Compiler also has validation passes that run on your React code. These passes encode the [Rules of React](/reference/rules), and uses the compiler's understanding of data-flow and mutability to provide diagnostics where the Rules of React are broken. These diagnostics often expose latent bugs hiding in React code, and are primarily surfaced through `eslint-plugin-react-hooks`.

To learn more about how the compiler optimizes your code, visit the [Playground](https://playground.react.dev).

</DeepDive>

## Use React Compiler Today {/*use-react-compiler-today*/}
To install the compiler:

npm
<TerminalBlock>
npm install --save-dev --save-exact babel-plugin-react-compiler@latest
</TerminalBlock>

pnpm
<TerminalBlock>
pnpm add --save-dev --save-exact babel-plugin-react-compiler@latest
</TerminalBlock>

yarn
<TerminalBlock>
yarn add --dev --exact babel-plugin-react-compiler@latest
</TerminalBlock>

As part of the stable release, we've been making React Compiler easier to add to your projects and added optimizations to how the compiler generates memoization. React Compiler now supports optional chains and array indices as dependencies. These improvements ultimately result in fewer re-renders and more responsive UIs, while letting you keep writing idiomatic declarative code.

You can find more details on using the Compiler in [our docs](/learn/react-compiler).

## What we're seeing in production {/*react-compiler-at-meta*/}
[The compiler has already shipped in apps like Meta Quest Store](https://youtu.be/lyEKhv8-3n0?t=3002). We've seen initial loads and cross-page navigations improve by up to 12%, while certain interactions are more than 2.5× faster. Memory usage stays neutral even with these wins. Although your mileage may vary, we recommend experimenting with the compiler in your app to see similar performance gains.

## Backwards Compatibility {/*backwards-compatibility*/}
As noted in the Beta announcement, React Compiler is compatible with React 17 and up. If you are not yet on React 19, you can use React Compiler by specifying a minimum target in your compiler config, and adding `react-compiler-runtime` as a dependency. You can find docs on this [here](/reference/react-compiler/target#targeting-react-17-or-18).

## Enforce the Rules of React with compiler-powered linting {/*migrating-from-eslint-plugin-react-compiler-to-eslint-plugin-react-hooks*/}
React Compiler includes an ESLint rule that helps identify code that breaks the [Rules of React](/reference/rules). The linter does not require the compiler to be installed, so there's no risk in upgrading eslint-plugin-react-hooks. We recommend everyone upgrade today.

If you have already installed `eslint-plugin-react-compiler`, you can now remove it and use `eslint-plugin-react-hooks@latest`. Many thanks to [@michaelfaith](https://bsky.app/profile/michael.faith) for contributing to this improvement!

To install:

npm
<TerminalBlock>
npm install --save-dev eslint-plugin-react-hooks@latest
</TerminalBlock>

pnpm
<TerminalBlock>
pnpm add --save-dev eslint-plugin-react-hooks@latest
</TerminalBlock>

yarn
<TerminalBlock>
yarn add --dev eslint-plugin-react-hooks@latest
</TerminalBlock>

```js {6}
// eslint.config.js (Flat Config)
import reactHooks from 'eslint-plugin-react-hooks';
import { defineConfig } from 'eslint/config';

export default defineConfig([
  reactHooks.configs.flat.recommended,
]);
```

```js {3}
// eslintrc.json (Legacy Config)
{
  "extends": ["plugin:react-hooks/recommended"],
  // ...
}
```

To enable React Compiler rules, we recommend using the `recommended` preset. You can also check out the [README](https://github.com/facebook/react/blob/main/packages/eslint-plugin-react-hooks/README.md) for more instructions. Here are a few examples we featured at React Conf:

- Catching `setState` patterns that cause render loops with [`set-state-in-render`](/reference/eslint-plugin-react-hooks/lints/set-state-in-render).
- Flagging expensive work inside effects via [`set-state-in-effect`](/reference/eslint-plugin-react-hooks/lints/set-state-in-effect).
- Preventing unsafe ref access during render with [`refs`](/reference/eslint-plugin-react-hooks/lints/refs).

## What should I do about useMemo, useCallback, and React.memo? {/*what-should-i-do-about-usememo-usecallback-and-reactmemo*/}
By default, React Compiler will memoize your code based on its analysis and heuristics. In most cases, this memoization will be as precise, or moreso, than what you may have written — and as noted above, the compiler can memoize even in cases where `useMemo`/`useCallback` cannot be used, such as after an early return.

However, in some cases developers may need more control over memoization. The `useMemo` and `useCallback` hooks can continue to be used with React Compiler as an escape hatch to provide control over which values are memoized. A common use-case for this is if a memoized value is used as an effect dependency, in order to ensure that an effect does not fire repeatedly even when its dependencies do not meaningfully change.

For new code, we recommend relying on the compiler for memoization and using `useMemo`/`useCallback` where needed to achieve precise control.

For existing code, we recommend either leaving existing memoization in place (removing it can change compilation output) or carefully testing before removing the memoization.

## New apps should use React Compiler {/*new-apps-should-use-react-compiler*/}
We have partnered with the Expo, Vite, and Next.js teams to add the compiler to the new app experience.

[Expo SDK 54](https://docs.expo.dev/guides/react-compiler/) and up has the compiler enabled by default, so new apps will automatically be able to take advantage of the compiler from the start.

<TerminalBlock>
npx create-expo-app@latest
</TerminalBlock>

[Vite](https://vite.dev/guide/) and [Next.js](https://nextjs.org/docs/app/api-reference/cli/create-next-app) users can choose the compiler enabled templates in `create-vite` and `create-next-app`.

<TerminalBlock>
npm create vite@latest
</TerminalBlock>

<br />

<TerminalBlock>
npx create-next-app@latest
</TerminalBlock>

## Adopt React Compiler incrementally {/*adopt-react-compiler-incrementally*/}
If you're maintaining an existing application, you can roll out the compiler at your own pace. We published a step-by-step [incremental adoption guide](/learn/react-compiler/incremental-adoption) that covers gating strategies, compatibility checks, and rollout tooling so you can enable the compiler with confidence.

## swc support (experimental) {/*swc-support-experimental*/}
React Compiler can be installed across [several build tools](/learn/react-compiler#installation) such as Babel, Vite, and Rsbuild.

In addition to those tools, we have been collaborating with Kang Dongyoon ([@kdy1dev](https://x.com/kdy1dev)) from the [swc](https://swc.rs/) team on adding additional support for React Compiler as an swc plugin. While this work isn't done, Next.js build performance should now be considerably faster when the [React Compiler is enabled in your Next.js app](https://nextjs.org/docs/app/api-reference/config/next-config-js/reactCompiler).

We recommend using Next.js [15.3.1](https://github.com/vercel/next.js/releases/tag/v15.3.1) or greater to get the best build performance.

Vite users can continue to use [vite-plugin-react](https://github.com/vitejs/vite-plugin-react) to enable the compiler, by adding it as a [Babel plugin](/learn/react-compiler/installation#vite). We are also working with the [oxc](https://oxc.rs/) team to [add support for the compiler](https://github.com/oxc-project/oxc/issues/10048). Once [rolldown](https://github.com/rolldown/rolldown) is officially released and supported in Vite and oxc support is added for React Compiler, we'll update the docs with information on how to migrate.

## Upgrading React Compiler {/*upgrading-react-compiler*/}
React Compiler works best when the auto-memoization applied is strictly for performance. Future versions of the compiler may change how memoization is applied, for example it could become more granular and precise.

However, because product code may sometimes break the [rules of React](/reference/rules) in ways that aren't always statically detectable in JavaScript, changing memoization can occasionally have unexpected results. For example, a previously memoized value might be used as a dependency for a `useEffect` somewhere in the component tree. Changing how or whether this value is memoized can cause over or under-firing of that `useEffect`. While we encourage [useEffect only for synchronization](/learn/synchronizing-with-effects), your codebase may have `useEffect`s that cover other use cases, such as effects that needs to only run in response to specific values changing.

In other words, changing memoization may under rare circumstances cause unexpected behavior. For this reason, we recommend following the Rules of React and employing continuous end-to-end testing of your app so you can upgrade the compiler with confidence and identify any rules of React violations that might cause issues.

If you don't have good test coverage, we recommend pinning the compiler to an exact version (eg `1.0.0`) rather than a SemVer range (eg `^1.0.0`). You can do this by passing the `--save-exact` (npm/pnpm) or `--exact` flags (yarn) when upgrading the compiler. You should then do any upgrades of the compiler manually, taking care to check that your app still works as expected.

---

Thanks to [Jason Bonta](https://x.com/someextent), [Jimmy Lai](https://x.com/feedthejim), [Kang Dongyoon](https://x.com/kdy1dev) (@kdy1dev), and [Dan Abramov](https://bsky.app/profile/danabra.mov) for reviewing and editing this post.

---
# Source: introducing-the-react-foundation.md
---
---
title: "Introducing the React Foundation"
author: Seth Webster, Matt Carroll, Joe Savona
date: 2025/10/07
description: Today, we're announcing our plans to create the React Foundation a new technical governance structure
---

October 7, 2025 by [Seth Webster](https://x.com/sethwebster), [Matt Carroll](https://x.com/mattcarrollcode), [Joe Savona](https://x.com/en_JS), [Sophie Alpert](https://x.com/sophiebits)

---


<div style={{display: 'flex', justifyContent: 'center', marginBottom: '1rem', marginLeft: '7rem', marginRight: '7rem' }}>
  <picture >
      <source srcset="/images/blog/react-foundation/react_foundation_logo.png" />
      <img className="w-full light-image" src="/images/blog/react-foundation/react_foundation_logo.webp" />
  </picture>
  <picture >
      <source srcset="/images/blog/react-foundation/react_foundation_logo_dark.png" />
      <img className="w-full dark-image" src="/images/blog/react-foundation/react_foundation_logo_dark.webp" />
  </picture>
</div>

<Intro>

Today, we're announcing our plans to create the React Foundation and a new technical governance structure.

</Intro>

---

We open sourced React over a decade ago to help developers build great user experiences. From its earliest days, React has received substantial contributions from contributors outside of Meta. Over time, the number of contributors and the scope of their contributions has grown significantly. What started out as a tool developed for Meta has expanded into a project that spans multiple companies with regular contributions from across the ecosystem. React has outgrown the confines of any one company.

To better serve the React community, we are announcing our plans to move React and React Native from Meta to a new React Foundation. As a part of this change, we will also be implementing a new independent technical governance structure. We believe these changes will enable us to give React ecosystem projects more resources.

## The React Foundation {/*the-react-foundation*/}

We will make the React Foundation the new home for React, React Native, and some supporting projects like JSX. The React Foundation’s mission will be to support the React community and ecosystem. Once implemented, the React Foundation will

* Maintain React’s infrastructure like GitHub, CI, and trademarks
* Organize React Conf
* Create initiatives to support the React ecosystem like financial support of ecosystem projects, issuing grants, and creating programs

The React Foundation will be governed by a board of directors, with Seth Webster serving as the executive director. This board will direct funds and resources to support React’s development, community, and ecosystem. We believe that this is the best structure to ensure that the React Foundation is vendor-neutral and reflects the best interests of the community.

The founding corporate members of the React Foundation will be Amazon, Callstack, Expo, Meta, Microsoft, Software Mansion, and Vercel. These companies have had a major impact on the React and React Native ecosystems and we are grateful for their support. We are excited to welcome even more members in the future.

<div style={{display: 'flex', justifyContent: 'center', margin: '2rem'}}>
  <picture >
      <source srcset="/images/blog/react-foundation/react_foundation_member_logos.png" />
      <img className="w-full light-image" src="/images/blog/react-foundation/react_foundation_member_logos.webp" />
  </picture>
  <picture >
      <source srcset="/images/blog/react-foundation/react_foundation_member_logos_dark.png" />
      <img className="w-full dark-image" src="/images/blog/react-foundation/react_foundation_member_logos_dark.webp" />
  </picture>
</div>

## React’s technical governance {/*reacts-technical-governance*/}

We believe that React's technical direction should be set by the people who contribute to and maintain React. As React moves to a foundation, it is important that no single company or organization is overrepresented. To achieve this, we plan to define a new technical governance structure for React that is independent from the React Foundation.

As a part of creating React’s new technical governance structure we will reach out to the community for feedback. Once finalized, we will share details in a future post.

## Thank you {/*thank-you*/}

React's incredible growth is thanks to the thousands of people, companies, and projects that have shaped React. The creation of the React Foundation is a testament to the strength and vibrancy of the React community. Together, the React Foundation and React’s new technical governance will ensure that React’s future is secure for years to come.

---
# Source: react-conf-2025-recap.md
---
---
title: "回顾 React Conf 2025"
author: Matt Carroll and Ricky Hanlon
date: 2025/10/16
description: 上周我们举办了 React Conf 2025，在本文中，我们总结了会议的演讲和公告...
---

2025 年 10 月 16 日 [Matt Carroll](https://x.com/mattcarrollcode) 和 [Ricky Hanlon](https://bsky.app/profile/ricky.fm)

---

<Intro>

上周我们举办了 React Conf 2025 大会，会上我们宣布了 [React 基金会](/blog/2025/10/07/introducing-the-react-foundation)，并展示了 React 和 React Native 即将推出的新特性。

</Intro>

---

React Conf 2025 于 2025 年 10 月 7-8 日在内华达州亨德森举行。

完整的 [第一天](https://www.youtube.com/watch?v=zyVRg2QR6LA&t=1067s) 和 [第二天](https://www.youtube.com/watch?v=p9OcztRyDl0&t=2299s) 的直播已经可以在线观看了。你可以在 [这里](https://conf.react.dev/photos) 查看活动照片。

在这篇文章中，我们将总结活动中的演讲和公告。


## 第一天 {/*day-1-keynote*/}

__[点击这里观看第一天完整直播。](https://www.youtube.com/watch?v=zyVRg2QR6LA&t=1067s)__

在第一天的主题演讲中，Joe Savona 分享了自上届 React Conf 以来团队和社区的更新，以及 React 19.0 和 19.1 的亮点。

Mofei Zhang 重点介绍了 React 19.2 的新特性，包括：
* [`<Activity />`](https://react.dev/reference/react/Activity) —— 一个用于管理可见性的新组件。
* [`useEffectEvent`](https://react.dev/reference/react/useEffectEvent) 用于从 Effects 中触发事件。
* [性能追踪](https://react.dev/reference/dev-tools/react-performance-tracks) —— DevTools 中的新性能分析工具。
* [部分预渲染](https://react.dev/blog/2025/10/01/react-19-2#partial-pre-rendering) 预先渲染应用的一部分，并在稍后恢复渲染以填充动态内容。

Jack Pope 宣布了 Canary 版本中的新特性，包括：

* [`<ViewTransition />`](https://react.dev/reference/react/ViewTransition) —— 用于为页面过渡添加动画的新组件。
* [Fragment Refs](https://react.dev/reference/react/Fragment#fragmentinstance) —— 与 Fragment 包裹的 DOM 节点交互的新方式。

Lauren Tan 宣布 [React 编译器 v1.0](https://react.dev/blog/2025/10/07/react-compiler-1)，并建议所有应用使用 React 编译器，可以获得以下好处：
* 能够理解 React 代码的 [自动记忆化](/learn/react-compiler/introduction#what-does-react-compiler-do)。
* 由 React 编译器提供的 [新 lint 规则](/learn/react-compiler/installation#eslint-integration) ，用于传授最佳实践。
* 在 Vite、Next.js 和 Expo 中为新应用提供 [默认支持](/learn/react-compiler/installation#basic-setup)。
* 为准备迁移到 React 编译器的现有应用提供 [迁移指南](/learn/react-compiler/incremental-adoption)。

最后，Seth Webster 宣布成立 [React 基金会](/blog/2025/10/07/introducing-the-react-foundation) 来管理 React 的开源开发和社区。

观看完整的第一天主题演讲：

<YouTubeIframe src="https://www.youtube.com/embed/zyVRg2QR6LA?si=z-8t_xCc12HwGJH_&t=1067s" />

## 第二天 {/*day-2-keynote*/}

__[点击这里观看第二天完整直播。](https://www.youtube.com/watch?v=p9OcztRyDl0&t=2299s)__

在第二天的主题演讲中，Jorge Cohen 和 Nicola Corti 开场就重点介绍了 React Native 的惊人增长 —— 每周下载量达 400 万次（同比增长 100%），以及 Shopify、Zalando 和 HelloFresh 等公司值得关注的应用迁移，RISE、RUNNA 和 Partyful 等获奖应用，以及来自 Mistral、Replit 和 v0 的 AI 应用。

Riccardo Cipolleschi 分享了 React Native 的两个重大公告：
- [React Native 0.82 将仅支持新架构](https://reactnative.dev/blog/2025/10/08/react-native-0.82#new-architecture-only)
- [实验性 Hermes V1 支持](https://reactnative.dev/blog/2025/10/08/react-native-0.82#experimental-hermes-v1)

Ruben Norte 和 Alex Hunt 继续主题演讲，宣布了：
- [新的与 Web 标准对齐的 DOM API](https://reactnative.dev/blog/2025/10/08/react-native-0.82#dom-node-apis)，提高了 React Native 与 Web 的兼容性。
- [新的性能 API](https://reactnative.dev/blog/2025/10/08/react-native-0.82#web-performance-apis-canary) 配备新的网络面板和桌面应用。

观看完整的第二天主题演讲：

<YouTubeIframe src="https://www.youtube.com/embed/p9OcztRyDl0?si=qPTHftsUE07cjZpS&t=2299s" />


## React 团队演讲 {/*react-team-talks*/}

整个会议期间，React 团队进行了多场演讲，包括：
* [Async React 第一部分](https://www.youtube.com/watch?v=zyVRg2QR6LA&t=10907s) 和 [第二部分](https://www.youtube.com/watch?v=p9OcztRyDl0&t=29073s)，来自 [Ricky Hanlon](https://x.com/rickhanlonii)，展示了过去 10 年创新所带来的可能性。
* [探索 React 性能](https://www.youtube.com/watch?v=zyVRg2QR6LA&t=20274s)，来自 [Joe Savona](https://x.com/en_js)，展示了我们的 React 性能研究结果。
* [重新构想 React Native 中的列表](https://www.youtube.com/watch?v=p9OcztRyDl0&t=10382s)，来自 [Luna Wei](https://x.com/lunaleaps)，介绍了 Virtual View，一个用于列表的新原语，它通过基于模式的渲染（隐藏/预渲染/可见）来管理可见性。
* [使用 React 性能追踪进行性能分析](https://www.youtube.com/watch?v=zyVRg2QR6LA&t=8276s)，来自 [Ruslan Lesiutin](https://x.com/ruslanlesiutin)，展示了如何使用新的 React 性能追踪来调试性能问题并构建优秀的应用。
* [React Strict DOM](https://www.youtube.com/watch?v=p9OcztRyDl0&t=9026s)，来自 [Nicolas Gallagher](https://nicolasgallagher.com/)，讨论了 Meta 在原生平台上使用 Web 代码的方法。
* [View Transitions 和 Activity](https://www.youtube.com/watch?v=zyVRg2QR6LA&t=4870s)，来自 [Chance Strickland](https://x.com/chancethedev)，Chance 与 React 团队合作，展示了如何使用 `<Activity />` 和 `<ViewTransition />` 来构建快速且具有原生体验的动画。
* [错过了 Memo？](https://www.youtube.com/watch?v=zyVRg2QR6LA&t=9525s)，来自 [Cody Olsen](https://bsky.app/profile/codey.bsky.social)，Cody 与 React 团队合作，在 Sanity Studio 中采用了 React 编译器，并分享了使用经验。
## React 框架演讲 {/*react-framework-talks*/}

第二天下半场进行了一系列来自 React 框架团队的演讲，包括：

* [React Native，增强版](https://www.youtube.com/watch?v=p9OcztRyDl0&t=5737s)，来自 [Giovanni Laquidara](https://x.com/giolaq) 和 [Eric Fahsl](https://x.com/efahsl)
* [React 无处不在：将 React 引入原生应用](https://www.youtube.com/watch?v=p9OcztRyDl0&t=18213s)，来自 [Mike Grabowski](https://x.com/grabbou)
* [Parcel 如何打包 React 服务器组件](https://www.youtube.com/watch?v=p9OcztRyDl0&t=19538s)，来自 [Devon Govett](https://x.com/devonovett)
* [设计页面过渡效果](https://www.youtube.com/watch?v=p9OcztRyDl0&t=20640s)，来自 [Delba de Oliveira](https://x.com/delba_oliveira)
* [快速构建，更快部署 —— 2025 年的 Expo](https://www.youtube.com/watch?v=p9OcztRyDl0&t=21350s)，来自 [Evan Bacon](https://x.com/baconbrix)
* [React Router 对 RSC 的看法](https://www.youtube.com/watch?v=p9OcztRyDl0&t=22367s)，来自 [Kent C. Dodds](https://x.com/kentcdodds)
* [RedwoodSDK：Web 标准驱动的全栈 React](https://www.youtube.com/watch?v=p9OcztRyDl0&t=24992s)，来自 [Peter Pistorius](https://x.com/appfactory) 和 [Aurora Scharff](https://x.com/aurorascharff)
* [TanStack Start](https://www.youtube.com/watch?v=p9OcztRyDl0&t=26065s)，来自 [Tanner Linsley](https://x.com/tannerlinsley)

## 问答环节 {/*q-and-a*/}
会议期间有三场问答环节：

* [Meta 公司 React 团队的问答环节](https://www.youtube.com/watch?v=zyVRg2QR6LA&t=26304s)，由 [Shruti Kapoor](https://x.com/shrutikapoor08) 主持
* [React 框架问答](https://www.youtube.com/watch?v=p9OcztRyDl0&t=26812s)，由 [Jack Herrington](https://x.com/jherr) 主持
* [React 和 AI 圆桌讨论](https://www.youtube.com/watch?v=zyVRg2QR6LA&t=18741s)，由 [Lee Robinson](https://x.com/leerob) 主持

## 还有更多... {/*and-more*/}

我们还听到了来自社区的演讲，包括：
* [构建 MCP 服务器](https://www.youtube.com/watch?v=zyVRg2QR6LA&t=24204s)，来自 [James Swinton](https://x.com/JamesSwintonDev)（[AG Grid](https://www.ag-grid.com/?utm_source=react-conf&utm_medium=react-conf-homepage&utm_campaign=react-conf-sponsorship-2025)）
* [使用 React 创建现代电子邮件](https://www.youtube.com/watch?v=zyVRg2QR6LA&t=25521s)，来自 [Zeno Rocha](https://x.com/zenorocha)（[Resend](https://resend.com/)）
* [为什么 React Native 应用最赚钱](https://www.youtube.com/watch?v=zyVRg2QR6LA&t=24917s)，来自 [Perttu Lähteenlahti](https://x.com/plahteenlahti)（[RevenueCat](https://www.revenuecat.com/)）
* [卓越用户体验的隐形技艺](https://www.youtube.com/watch?v=zyVRg2QR6LA&t=23400s)，来自 [Michał Dudak](https://x.com/michaldudak)（[MUI](https://mui.com/)）

## 致谢 {/*thanks*/}

感谢所有使 React Conf 2025 成为可能的工作人员、演讲者和参与者。感谢名单太长不能一一列出，但我们想特别感谢一些人。

感谢 [Matt Carroll](https://x.com/mattcarrollcode) 策划整个活动并搭建了大会网站。

感谢 [Michael Chan](https://x.com/chantastic) 以极大的热忱和活力主持了 React Conf，在整个活动中，他不仅为每个演讲者做了精心的介绍，还带来了有趣的笑话，展现出了真挚的热情。感谢 [Jorge Cohen](https://x.com/JorgeWritesCode) 主持直播，采访每位演讲者，并将现场的 React Conf 体验搬到了线上。

感谢 [Mateusz Kornacki](https://x.com/mat_kornacki)、[Mike Grabowski](https://x.com/grabbou)、[Kris Lis](https://www.linkedin.com/in/krzysztoflisakakris/) 和 [Callstack](https://www.callstack.com/) 团队共同组织 React Conf，并提供设计、工程和营销支持。感谢 [ZeroSlope 团队](https://zeroslopeevents.com/contact-us/) 的 Sunny Leggett、Tracey Harrison、Tara Larish、Whitney Pogue 和 Brianne Smythia 帮助组织活动。

感谢 [Jorge Cabiedes Acosta](https://github.com/jorge-cab)、[Gijs Weterings](https://x.com/gweterings)、[Tim Yung](https://x.com/yungsters) 和 [Jason Bonta](https://x.com/someextent) 将 Discord 中的问题带到直播中。感谢 [Lynn Yu](https://github.com/lynnshaoyu) 负责 Discord 的管理工作。感谢 [Seth Webster](https://x.com/sethwebster) 每天迎接我们；感谢 [Christopher Chedeau](https://x.com/vjeux)、[Kevin Gozali](https://x.com/fkgozali) 和 [Pieter De Baets](https://x.com/Javache) 在会后派对上为我们带来了特别寄语。

感谢 [Kadi Kraman](https://x.com/kadikraman)、[Beto](https://x.com/betomoedano) 和 [Nicolas Solerieu](https://www.linkedin.com/in/nicolas-solerieu/) 开发了大会的移动应用。感谢 [Wojtek Szafraniec](https://x.com/wojteg1337) 为大会网站提供的帮助。感谢 [Mustache](https://www.mustachepower.com/) & [Cornerstone](https://cornerstoneav.com/) 为我们提供的视觉、舞台和音响支持；感谢威斯汀酒店为我们提供的住宿。

感谢所有赞助商使本次活动得以实现：[Amazon](https://www.developer.amazon.com)、[MUI](https://mui.com/)、[Vercel](https://vercel.com/)、[Expo](https://expo.dev/)、[RedwoodSDK](https://rwsdk.com)、[Ag Grid](https://www.ag-grid.com)、[RevenueCat](https://www.revenuecat.com/)、[Resend](https://resend.com)、[Mux](https://www.mux.com/)、[Old Mission](https://www.oldmissioncapital.com/)、[Arcjet](https://arcjet.com)、[Infinite Red](https://infinite.red/) 以及 [RenderATL](https://renderatl.com)。

感谢所有与社区分享他们的知识和经验的演讲者。

最后，感谢所有现场以及在线参加大会的每一位，正是因为有你们，React 才成为了今天的 React。React 不仅仅是一个库，它更是一个社区，看到大家齐聚一堂、共同分享和学习，真是令人鼓舞。

下次见！

---
# Source: react-19-2.md
---
---
title: "React 19.2"
author: The React Team
date: 2025/10/01
description: React 19.2 adds new features like Activity, React Performance Tracks, useEffectEvent, and more.
---

October 1, 2025 by [The React Team](/community/team)

---

<Intro>

React 19.2 is now available on npm!

</Intro>

This is our third release in the last year, following React 19 in December and React 19.1 in June. In this post, we'll give an overview of the new features in React 19.2, and highlight some notable changes.

<InlineToc />

---

## New React Features {/*new-react-features*/}

### `<Activity />` {/*activity*/}

`<Activity>` lets you break your app into "activities" that can be controlled and prioritized.

You can use Activity as an alternative to conditionally rendering parts of your app:

```js
// Before
{isVisible && <Page />}

// After
<Activity mode={isVisible ? 'visible' : 'hidden'}>
  <Page />
</Activity>
```

In React 19.2, Activity supports two modes: `visible` and `hidden`.

- `hidden`: hides the children, unmounts effects, and defers all updates until React has nothing left to work on.
- `visible`: shows the children, mounts effects, and allows updates to be processed normally.

This means you can pre-render and keep rendering hidden parts of the app without impacting the performance of anything visible on screen.

You can use Activity to render hidden parts of the app that a user is likely to navigate to next, or to save the state of parts the user navigates away from. This helps make navigations quicker by loading data, css, and images in the background, and allows back navigations to maintain state such as input fields.

In the future, we plan to add more modes to Activity for different use cases.

For examples on how to use Activity, check out the [Activity docs](/reference/react/Activity).

---

### `useEffectEvent` {/*use-effect-event*/}

One common pattern with `useEffect` is to notify the app code about some kind of "events" from an external system. For example, when a chat room gets connected, you might want to display a notification:

```js {5,11}
function ChatRoom({ roomId, theme }) {
  useEffect(() => {
    const connection = createConnection(serverUrl, roomId);
    connection.on('connected', () => {
      showNotification('Connected!', theme);
    });
    connection.connect();
    return () => {
      connection.disconnect()
    };
  }, [roomId, theme]);
  // ...
```

The problem with the code above is that a change to any values used inside such an "event" will cause the surrounding Effect to re-run. For example, changing the `theme` will cause the chat room to reconnect. This makes sense for values related to the Effect logic itself, like `roomId`, but it doesn't make sense for `theme`.

To solve this, most users just disable the lint rule and exclude the dependency. But that can lead to bugs since the linter can no longer help you keep the dependencies up to date if you need to update the Effect later.

With `useEffectEvent`, you can split the "event" part of this logic out of the Effect that emits it:

```js {2,3,4,9}
function ChatRoom({ roomId, theme }) {
  const onConnected = useEffectEvent(() => {
    showNotification('Connected!', theme);
  });

  useEffect(() => {
    const connection = createConnection(serverUrl, roomId);
    connection.on('connected', () => {
      onConnected();
    });
    connection.connect();
    return () => connection.disconnect();
  }, [roomId]); // ✅ All dependencies declared (Effect Events aren't dependencies)
  // ...
```

Similar to DOM events, Effect Events always “see” the latest props and state.

**Effect Events should _not_ be declared in the dependency array**. You'll need to upgrade to `eslint-plugin-react-hooks@latest` so that the linter doesn't try to insert them as dependencies. Note that Effect Events can only be declared in the same component or Hook as "their" Effect. These restrictions are verified by the linter.

<Note>

#### When to use `useEffectEvent` {/*when-to-use-useeffectevent*/}

You should use `useEffectEvent` for functions that are conceptually "events" that happen to be fired from an Effect instead of a user event (that's what makes it an "Effect Event"). You don't need to wrap everything in `useEffectEvent`, or to use it just to silence the lint error, as this can lead to bugs.

For a deep dive on how to think about Event Effects, see: [Separating Events from Effects](/learn/separating-events-from-effects#extracting-non-reactive-logic-out-of-effects).

</Note>

---

### `cacheSignal` {/*cache-signal*/}

<RSC>

`cacheSignal` is only for use with [React Server Components](/reference/rsc/server-components).

</RSC>

`cacheSignal` allows you to know when the [`cache()`](/reference/react/cache) lifetime is over:

```
import {cache, cacheSignal} from 'react';
const dedupedFetch = cache(fetch);

async function Component() {
  await dedupedFetch(url, { signal: cacheSignal() });
}
```

This allows you to clean up or abort work when the result will no longer be used in the cache, such as:

- React has successfully completed rendering
- The render was aborted
- The render has failed

For more info, see the [`cacheSignal` docs](/reference/react/cacheSignal).

---

### Performance Tracks {/*performance-tracks*/}

React 19.2 adds a new set of [custom tracks](https://developer.chrome.com/docs/devtools/performance/extension) to Chrome DevTools performance profiles to provide more information about the performance of your React app:

<div style={{display: 'flex', justifyContent: 'center', marginBottom: '1rem'}}>
  <picture >
      <source srcset="/images/blog/react-labs-april-2025/perf_tracks.png" />
      <img className="w-full light-image" src="/images/blog/react-labs-april-2025/perf_tracks.webp" />
  </picture>
  <picture >
      <source srcset="/images/blog/react-labs-april-2025/perf_tracks_dark.png" />
      <img className="w-full dark-image" src="/images/blog/react-labs-april-2025/perf_tracks_dark.webp" />
  </picture>
</div>

The [React Performance Tracks docs](/reference/dev-tools/react-performance-tracks) explain everything included in the tracks, but here is a high-level overview.

#### Scheduler ⚛ {/*scheduler-*/}

The Scheduler track shows what React is working on for different priorities such as "blocking" for user interactions, or "transition" for updates inside startTransition. Inside each track, you will see the type of work being performed such as the event that scheduled an update, and when the render for that update happened.

We also show information such as when an update is blocked waiting for a different priority, or when React is waiting for paint before continuing. The Scheduler track helps you understand how React splits your code into different priorities, and the order it completed the work.

See the [Scheduler track](/reference/dev-tools/react-performance-tracks#scheduler) docs to see everything included.

#### Components ⚛ {/*components-*/}

The Components track shows the tree of components that React is working on either to render or run effects. Inside you'll see labels such as "Mount" for when children mount or effects are mounted, or "Blocked" for when rendering is blocked due to yielding to work outside React.

The Components track helps you understand when components are rendered or run effects, and the time it takes to complete that work to help identify performance problems.

See the [Components track docs](/reference/dev-tools/react-performance-tracks#components) for see everything included.

---

## New React DOM Features {/*new-react-dom-features*/}

### Partial Pre-rendering {/*partial-pre-rendering*/}

In 19.2 we're adding a new capability to pre-render part of the app ahead of time, and resume rendering it later.

This feature is called "Partial Pre-rendering", and allows you to pre-render the static parts of your app and serve it from a CDN, and then resume rendering the shell to fill it in with dynamic content later.

To pre-render an app to resume later, first call `prerender` with an `AbortController`:

```
const {prelude, postponed} = await prerender(<App />, {
  signal: controller.signal,
});

// Save the postponed state for later
await savePostponedState(postponed);

// Send prelude to client or CDN.
```

Then, you can return the `prelude` shell to the client, and later call `resume` to "resume" to a SSR stream:

```
const postponed = await getPostponedState(request);
const resumeStream = await resume(<App />, postponed);

// Send stream to client.
```

Or you can call `resumeAndPrerender` to resume to get static HTML for SSG:

```
const postponedState = await getPostponedState(request);
const { prelude } = await resumeAndPrerender(<App />, postponedState);

// Send complete HTML prelude to CDN.
```

For more info, see the docs for the new APIs:
- `react-dom/server`
  - [`resume`](/reference/react-dom/server/resume): for Web Streams.
  - [`resumeToPipeableStream`](/reference/react-dom/server/resumeToPipeableStream) for Node Streams.
- `react-dom/static`
  - [`resumeAndPrerender`](/reference/react-dom/static/resumeAndPrerender) for Web Streams.
  - [`resumeAndPrerenderToNodeStream`](/reference/react-dom/static/resumeAndPrerenderToNodeStream) for Node Streams.

Additionally, the prerender apis now return a `postpone` state to pass to the `resume` apis.

---

## Notable Changes {/*notable-changes*/}

### Batching Suspense Boundaries for SSR {/*batching-suspense-boundaries-for-ssr*/}

We fixed a behavioral bug where Suspense boundaries would reveal differently depending on if they were rendered on the client or when streaming from server-side rendering.

Starting in 19.2, React will batch reveals of server-rendered Suspense boundaries for a short time, to allow more content to be revealed together and align with the client-rendered behavior.

<Diagram name="19_2_batching_before" height={162} width={1270} alt="Diagram with three sections, with an arrow transitioning each section in between. The first section contains a page rectangle showing a glimmer loading state with faded bars. The second panel shows the top half of the page revealed and highlighted in blue. The third panel shows the entire the page revealed and highlighted in blue.">

Previously, during streaming server-side rendering, suspense content would immediately replace fallbacks.

</Diagram>

<Diagram name="19_2_batching_after" height={162} width={1270} alt="Diagram with three sections, with an arrow transitioning each section in between. The first section contains a page rectangle showing a glimmer loading state with faded bars. The second panel shows the same page. The third panel shows the entire the page revealed and highlighted in blue.">

In React 19.2, suspense boundaries are batched for a small amount of time, to allow revealing more content together.

</Diagram>

This fix also prepares apps for supporting `<ViewTransition>` for Suspense during SSR. By revealing more content together, animations can run in larger batches of content, and avoid chaining animations of content that stream in close together.

<Note>

React uses heuristics to ensure throttling does not impact core web vitals and search ranking.

For example, if the total page load time is approaching 2.5s (which is the time considered "good" for [LCP](https://web.dev/articles/lcp)), React will stop batching and reveal content immediately so that the throttling is not the reason to miss the metric.

</Note>

---

### SSR: Web Streams support for Node {/*ssr-web-streams-support-for-node*/}

React 19.2 adds support for Web Streams for streaming SSR in Node.js:
- [`renderToReadableStream`](/reference/react-dom/server/renderToReadableStream) is now available for Node.js
- [`prerender`](/reference/react-dom/static/prerender) is now available for Node.js

As well as the new `resume` APIs:
- [`resume`](/reference/react-dom/server/resume) is available for Node.js.
- [`resumeAndPrerender`](/reference/react-dom/static/resumeAndPrerender) is available for Node.js.


<Pitfall>

#### Prefer Node Streams for server-side rendering in Node.js {/*prefer-node-streams-for-server-side-rendering-in-nodejs*/}

In Node.js environments, we still highly recommend using the Node Streams APIs:

- [`renderToPipeableStream`](/reference/react-dom/server/renderToPipeableStream)
- [`resumeToPipeableStream`](/reference/react-dom/server/resumeToPipeableStream)
- [`prerenderToNodeStream`](/reference/react-dom/static/prerenderToNodeStream)
- [`resumeAndPrerenderToNodeStream`](/reference/react-dom/static/resumeAndPrerenderToNodeStream)

This is because Node Streams are much faster than Web Streams in Node, and Web Streams do not support compression by default, leading to users accidentally missing the benefits of streaming.

</Pitfall>

---

### `eslint-plugin-react-hooks` v6 {/*eslint-plugin-react-hooks*/}

We also published `eslint-plugin-react-hooks@latest` with flat config by default in the `recommended` preset, and opt-in for new React Compiler powered rules.

To continue using the legacy config, you can change to `recommended-legacy`:

```diff
- extends: ['plugin:react-hooks/recommended']
+ extends: ['plugin:react-hooks/recommended-legacy']
```

For a full list of compiler enabled rules, [check out the linter docs](/reference/eslint-plugin-react-hooks#recommended).

Check out the `eslint-plugin-react-hooks` [changelog for a full list of changes](https://github.com/facebook/react/blob/main/packages/eslint-plugin-react-hooks/CHANGELOG.md#610).

---

### Update the default `useId` prefix {/*update-the-default-useid-prefix*/}

In 19.2, we're updating the default `useId` prefix from `:r:` (19.0.0) or `«r»` (19.1.0) to `_r_`.

The original intent of using a special character that was not valid for CSS selectors was that it would be unlikely to collide with IDs written by users. However, to support View Transitions, we need to ensure that IDs generated by `useId` are valid for `view-transition-name` and XML 1.0 names.

---

## Changelog {/*changelog*/}

Other notable changes
- `react-dom`: Allow nonce to be used on hoistable styles [#32461](https://github.com/facebook/react/pull/32461)
- `react-dom`: Warn for using a React owned node as a Container if it also has text content [#32774](https://github.com/facebook/react/pull/32774)

Notable bug fixes
- `react`: Stringify context as "SomeContext" instead of "SomeContext.Provider" [#33507](https://github.com/facebook/react/pull/33507)
- `react`: Fix infinite useDeferredValue loop in popstate event [#32821](https://github.com/facebook/react/pull/32821)
- `react`: Fix a bug when an initial value was passed to useDeferredValue [#34376](https://github.com/facebook/react/pull/34376)
- `react`: Fix a crash when submitting forms with Client Actions [#33055](https://github.com/facebook/react/pull/33055)
- `react`: Hide/unhide the content of dehydrated suspense boundaries if they resuspend [#32900](https://github.com/facebook/react/pull/32900)
- `react`: Avoid stack overflow on wide trees during Hot Reload [#34145](https://github.com/facebook/react/pull/34145)
- `react`: Improve component stacks in various places [#33629](https://github.com/facebook/react/pull/33629), [#33724](https://github.com/facebook/react/pull/33724), [#32735](https://github.com/facebook/react/pull/32735), [#33723](https://github.com/facebook/react/pull/33723)
- `react`: Fix a bug with React.use inside React.lazy-ed Component [#33941](https://github.com/facebook/react/pull/33941)
- `react-dom`: Stop warning when ARIA 1.3 attributes are used [#34264](https://github.com/facebook/react/pull/34264)
- `react-dom`: Fix a bug with deeply nested Suspense inside Suspense fallbacks [#33467](https://github.com/facebook/react/pull/33467)
- `react-dom`: Avoid hanging when suspending after aborting while rendering [#34192](https://github.com/facebook/react/pull/34192)

For a full list of changes, please see the [Changelog](https://github.com/facebook/react/blob/main/CHANGELOG.md).


---

_Thanks to [Ricky Hanlon](https://bsky.app/profile/ricky.fm) for [writing this post](https://www.youtube.com/shorts/T9X3YkgZRG0), [Dan Abramov](https://bsky.app/profile/danabra.mov), [Matt Carroll](https://twitter.com/mattcarrollcode), [Jack Pope](https://jackpope.me), and [Joe Savona](https://x.com/en_JS) for reviewing this post._

---
# Source: react-labs-view-transitions-activity-and-more.md
---
---
title: "React Labs：视图过渡、Activity 等功能"
author: Ricky Hanlon
date: 2025/04/23
description: 在 React Labs 系列文章中，我们会介绍正在积极研究和开发的项目。本文将分享两个已经可供测试的新实验性功能，以及其他正在开发中功能的最新进展。
---

2025 年 4 月 23 日，作者：[Ricky Hanlon](https://twitter.com/rickhanlonii)

---

<Intro>

在 React Labs 系列文章中，我们会介绍正在积极研究和开发的项目。本文将分享两个已经可供测试的新实验性功能，以及其他正在开发中功能的最新进展。

</Intro>


今天，我们很高兴发布两个可供测试的新实验性功能的文档：

- [视图过渡（View Transitions）](#view-transitions)
- [Activity](#activity)

我们还分享了目前正在开发的新功能的最新进展：
- [React 性能追踪（Performance Tracks）](#react-performance-tracks)
- [编译器 IDE 扩展](#compiler-ide-extension)
- [自动 Effect 依赖](#automatic-effect-dependencies)
- [Fragment Refs](#fragment-refs)
- [并发存储（Concurrent Stores）](#concurrent-stores)

---

# 新的实验性功能 {/*new-experimental-features*/}

<Note>

`<Activity />` 已在 `react@19.2` 中发布。

`<ViewTransition />` 和 `addTransitionType` 现在可以在 `react@canary` 中使用。

</Note>

视图过渡和 Activity 现在已经可以在 `react@experimental` 中进行测试。这些功能已经在生产环境中经过测试并且稳定，但最终的 API 可能会随着我们采纳反馈而发生变化。

你可以通过将 React 包升级到最新的实验版本来尝试它们：

- `react@experimental`
- `react-dom@experimental`

继续阅读以了解如何在你的应用中使用这些功能，或者查看新发布的文档：

- [`<ViewTransition>`](/reference/react/ViewTransition)：一个让你为 Transition 激活动画的组件。
- [`addTransitionType`](/reference/react/addTransitionType)：一个允许你指定 Transition 原因的函数。
- [`<Activity>`](/reference/react/Activity)：一个让你隐藏和显示 UI 部分的组件。

## 视图过渡 {/*view-transitions*/}

React 视图过渡是一个新的实验性功能，它让你能更轻松地为应用中的 UI 过渡添加动画效果。在底层，这些动画使用了大多数现代浏览器提供的新 [`startViewTransition`](https://developer.mozilla.org/en-US/docs/Web/API/Document/startViewTransition) API。

要选择为元素添加动画，请将其包装在新的 `<ViewTransition>` 组件中：

```js
// "要"动画的内容
<ViewTransition>
  <div>为我添加动画</div>
</ViewTransition>
```

这个新组件让你可以声明式地定义"要"在动画激活时进行动画处理的内容。

你可以通过使用以下三种触发器之一来定义"何时"进行动画：

```js
// "何时"进行动画

// Transitions
startTransition(() => setState(...));

// 延迟值
const deferred = useDeferredValue(value);

// Suspense
<Suspense fallback={<Fallback />}>
  <div>加载中...</div>
</Suspense>
```

默认情况下，这些动画使用[视图过渡的默认 CSS 动画](https://developer.mozilla.org/en-US/docs/Web/API/View_Transition_API/Using#customizing_your_animations)（通常是平滑的交叉淡入淡出）。你可以使用[视图过渡伪选择器](https://developer.mozilla.org/en-US/docs/Web/API/View_Transition_API/Using#the_view_transition_pseudo-element_tree)来定义动画"如何"运行。例如，你可以使用 `*` 来更改所有过渡的默认动画：

```
// "如何"进行动画
::view-transition-old(*) {
  animation: 300ms ease-out fade-out;
}
::view-transition-new(*) {
  animation: 300ms ease-in fade-in;
}
```

当 DOM 因动画触发器（如 `startTransition`、`useDeferredValue` 或 `Suspense` 后备方案切换到内容）而更新时，React 将使用[声明式启发法](/reference/react/ViewTransition#viewtransition)自动确定要为动画激活哪些 `<ViewTransition>` 组件。然后浏览器将运行在 CSS 中定义的动画。

如果你熟悉浏览器的视图过渡 API 并想了解 React 如何支持它，请查看文档中的[`<ViewTransition>` 如何工作](/reference/react/ViewTransition#how-does-viewtransition-work)。

在本文中，让我们看几个使用视图过渡的例子。

我们将从这个应用开始，它不会为以下任何交互添加动画：
- 点击视频查看详情。
- 点击“返回”回到信息流。
- 在列表中输入以筛选视频。

<Sandpack>

```js src/App.js active
import TalkDetails from './Details'; import Home from './Home'; import {useRouter} from './router';

export default function App() {
  const {url} = useRouter();

  // 🚩这个版本还没有包含任何动画
  return url === '/' ? <Home /> : <TalkDetails />;
}
```

```js src/Details.js
import { fetchVideo, fetchVideoDetails } from "./data";
import { Thumbnail, VideoControls } from "./Videos";
import { useRouter } from "./router";
import Layout from "./Layout";
import { use, Suspense } from "react";
import { ChevronLeft } from "./Icons";

function VideoInfo({ id }) {
  const details = use(fetchVideoDetails(id));
  return (
    <>
      <p className="info-title">{details.title}</p>
      <p className="info-description">{details.description}</p>
    </>
  );
}

function VideoInfoFallback() {
  return (
    <>
      <div className="fallback title"></div>
      <div className="fallback description"></div>
    </>
  );
}

export default function Details() {
  const { url, navigateBack } = useRouter();
  const videoId = url.split("/").pop();
  const video = use(fetchVideo(videoId));

  return (
    <Layout
      heading={
        <div
          className="fit back"
          onClick={() => {
            navigateBack("/");
          }}
        >
          <ChevronLeft /> Back
        </div>
      }
    >
      <div className="details">
        <Thumbnail video={video} large>
          <VideoControls />
        </Thumbnail>
        <Suspense fallback={<VideoInfoFallback />}>
          <VideoInfo id={video.id} />
        </Suspense>
      </div>
    </Layout>
  );
}

```

```js src/Home.js
import { Video } from "./Videos";
import Layout from "./Layout";
import { fetchVideos } from "./data";
import { useId, useState, use } from "react";
import { IconSearch } from "./Icons";

function SearchInput({ value, onChange }) {
  const id = useId();
  return (
    <form className="search" onSubmit={(e) => e.preventDefault()}>
      <label htmlFor={id} className="sr-only">
        Search
      </label>
      <div className="search-input">
        <div className="search-icon">
          <IconSearch />
        </div>
        <input
          type="text"
          id={id}
          placeholder="Search"
          value={value}
          onChange={(e) => onChange(e.target.value)}
        />
      </div>
    </form>
  );
}

function filterVideos(videos, query) {
  const keywords = query
    .toLowerCase()
    .split(" ")
    .filter((s) => s !== "");
  if (keywords.length === 0) {
    return videos;
  }
  return videos.filter((video) => {
    const words = (video.title + " " + video.description)
      .toLowerCase()
      .split(" ");
    return keywords.every((kw) => words.some((w) => w.includes(kw)));
  });
}

export default function Home() {
  const videos = use(fetchVideos());
  const count = videos.length;
  const [searchText, setSearchText] = useState("");
  const foundVideos = filterVideos(videos, searchText);
  return (
    <Layout heading={<div className="fit">{count} Videos</div>}>
      <SearchInput value={searchText} onChange={setSearchText} />
      <div className="video-list">
        {foundVideos.length === 0 && (
          <div className="no-results">No results</div>
        )}
        <div className="videos">
          {foundVideos.map((video) => (
            <Video key={video.id} video={video} />
          ))}
        </div>
      </div>
    </Layout>
  );
}

```

```js src/Icons.js
export function ChevronLeft() {
  return (
    <svg
      className="chevron-left"
      xmlns="http://www.w3.org/2000/svg"
      width="20"
      height="20"
      viewBox="0 0 20 20">
      <g fill="none" fillRule="evenodd" transform="translate(-446 -398)">
        <path
          fill="currentColor"
          fillRule="nonzero"
          d="M95.8838835,240.366117 C95.3957281,239.877961 94.6042719,239.877961 94.1161165,240.366117 C93.6279612,240.854272 93.6279612,241.645728 94.1161165,242.133883 L98.6161165,246.633883 C99.1042719,247.122039 99.8957281,247.122039 100.383883,246.633883 L104.883883,242.133883 C105.372039,241.645728 105.372039,240.854272 104.883883,240.366117 C104.395728,239.877961 103.604272,239.877961 103.116117,240.366117 L99.5,243.982233 L95.8838835,240.366117 Z"
          transform="translate(356.5 164.5)"
        />
        <polygon points="446 418 466 418 466 398 446 398" />
      </g>
    </svg>
  );
}

export function PauseIcon() {
  return (
    <svg
      className="control-icon"
      style={{padding: '4px'}}
      width="100"
      height="100"
      viewBox="0 0 512 512"
      fill="none"
      xmlns="http://www.w3.org/2000/svg">
      <path
        fillRule="evenodd"
        clipRule="evenodd"
        d="M256 0C114.617 0 0 114.615 0 256s114.617 256 256 256 256-114.615 256-256S397.383 0 256 0zm-32 320c0 8.836-7.164 16-16 16h-32c-8.836 0-16-7.164-16-16V192c0-8.836 7.164-16 16-16h32c8.836 0 16 7.164 16 16v128zm128 0c0 8.836-7.164 16-16 16h-32c-8.836 0-16-7.164-16-16V192c0-8.836 7.164-16 16-16h32c8.836 0 16 7.164 16 16v128z"
        fill="currentColor"
      />
    </svg>
  );
}

export function PlayIcon() {
  return (
    <svg
      className="control-icon"
      width="100"
      height="100"
      viewBox="0 0 72 72"
      fill="none"
      xmlns="http://www.w3.org/2000/svg">
      <path
        fillRule="evenodd"
        clipRule="evenodd"
        d="M36 69C54.2254 69 69 54.2254 69 36C69 17.7746 54.2254 3 36 3C17.7746 3 3 17.7746 3 36C3 54.2254 17.7746 69 36 69ZM52.1716 38.6337L28.4366 51.5801C26.4374 52.6705 24 51.2235 24 48.9464V23.0536C24 20.7764 26.4374 19.3295 28.4366 20.4199L52.1716 33.3663C54.2562 34.5034 54.2562 37.4966 52.1716 38.6337Z"
        fill="currentColor"
      />
    </svg>
  );
}
export function Heart({liked, animate}) {
  return (
    <>
      <svg
        className="absolute overflow-visible"
        viewBox="0 0 24 24"
        fill="none"
        xmlns="http://www.w3.org/2000/svg">
        <circle
          className={`circle ${liked ? 'liked' : ''} ${animate ? 'animate' : ''}`}
          cx="12"
          cy="12"
          r="11.5"
          fill="transparent"
          strokeWidth="0"
          stroke="currentColor"
        />
      </svg>

      <svg
        className={`heart ${liked ? 'liked' : ''} ${animate ? 'animate' : ''}`}
        viewBox="0 0 24 24"
        fill="none"
        xmlns="http://www.w3.org/2000/svg">
        {liked ? (
          <path
            d="M12 23a.496.496 0 0 1-.26-.074C7.023 19.973 0 13.743 0 8.68c0-4.12 2.322-6.677 6.058-6.677 2.572 0 5.108 2.387 5.134 2.41l.808.771.808-.771C12.834 4.387 15.367 2 17.935 2 21.678 2 24 4.558 24 8.677c0 5.06-7.022 11.293-11.74 14.246a.496.496 0 0 1-.26.074V23z"
            fill="currentColor"
          />
        ) : (
          <path
            fillRule="evenodd"
            clipRule="evenodd"
            d="m12 5.184-.808-.771-.004-.004C11.065 4.299 8.522 2.003 6 2.003c-3.736 0-6 2.558-6 6.677 0 4.47 5.471 9.848 10 13.079.602.43 1.187.82 1.74 1.167A.497.497 0 0 0 12 23v-.003c.09 0 .182-.026.26-.074C16.977 19.97 24 13.737 24 8.677 24 4.557 21.743 2 18 2c-2.569 0-5.166 2.387-5.192 2.413L12 5.184zm-.002 15.525c2.071-1.388 4.477-3.342 6.427-5.47C20.72 12.733 22 10.401 22 8.677c0-1.708-.466-2.855-1.087-3.55C20.316 4.459 19.392 4 18 4c-.726 0-1.63.364-2.5.9-.67.412-1.148.82-1.266.92-.03.025-.037.031-.019.014l-.013.013L12 7.949 9.832 5.88a10.08 10.08 0 0 0-1.33-.977C7.633 4.367 6.728 4.003 6 4.003c-1.388 0-2.312.459-2.91 1.128C2.466 5.826 2 6.974 2 8.68c0 1.726 1.28 4.058 3.575 6.563 1.948 2.127 4.352 4.078 6.423 5.466z"
            fill="currentColor"
          />
        )}
      </svg>
    </>
  );
}

export function IconSearch(props) {
  return (
    <svg width="1em" height="1em" viewBox="0 0 20 20">
      <path
        d="M14.386 14.386l4.0877 4.0877-4.0877-4.0877c-2.9418 2.9419-7.7115 2.9419-10.6533 0-2.9419-2.9418-2.9419-7.7115 0-10.6533 2.9418-2.9419 7.7115-2.9419 10.6533 0 2.9419 2.9418 2.9419 7.7115 0 10.6533z"
        stroke="currentColor"
        fill="none"
        strokeWidth="2"
        fillRule="evenodd"
        strokeLinecap="round"
        strokeLinejoin="round"></path>
    </svg>
  );
}
```

```js src/Layout.js
import { useIsNavPending } from "./router";

export default function Page({ heading, children }) {
  const isPending = useIsNavPending();
  return (
    <div className="page">
      <div className="top">
        <div className="top-nav">
          {heading}
          {isPending && <span className="loader"></span>}
        </div>
      </div>

      <div className="bottom">
        <div className="content">{children}</div>
      </div>
    </div>
  );
}
```

```js src/LikeButton.js
import {useState} from 'react';
import {Heart} from './Icons';

// 这是一个技巧，因为我们实际上没有后端。
// 与本地状态不同，这在视频被筛选时仍然保留。
const likedVideos = new Set();

export default function LikeButton({video}) {
  const [isLiked, setIsLiked] = useState(() => likedVideos.has(video.id));
  const [animate, setAnimate] = useState(false);
  return (
    <button
      className={`like-button ${isLiked && 'liked'}`}
      aria-label={isLiked ? 'Unsave' : 'Save'}
      onClick={() => {
        const nextIsLiked = !isLiked;
        if (nextIsLiked) {
          likedVideos.add(video.id);
        } else {
          likedVideos.delete(video.id);
        }
        setAnimate(true);
        setIsLiked(nextIsLiked);
      }}>
      <Heart liked={isLiked} animate={animate} />
    </button>
  );
}
```

```js src/Videos.js
import { useState } from "react";
import LikeButton from "./LikeButton";
import { useRouter } from "./router";
import { PauseIcon, PlayIcon } from "./Icons";
import { startTransition } from "react";

export function VideoControls() {
  const [isPlaying, setIsPlaying] = useState(false);

  return (
    <span
      className="controls"
      onClick={() =>
        startTransition(() => {
          setIsPlaying((p) => !p);
        })
      }
    >
      {isPlaying ? <PauseIcon /> : <PlayIcon />}
    </span>
  );
}

export function Thumbnail({ video, children }) {
  return (
    <div
      aria-hidden="true"
      tabIndex={-1}
      className={`thumbnail ${video.image}`}
    >
      {children}
    </div>
  );
}

export function Video({ video }) {
  const { navigate } = useRouter();

  return (
    <div className="video">
      <div
        className="link"
        onClick={(e) => {
          e.preventDefault();
          navigate(`/video/${video.id}`);
        }}
      >
        <Thumbnail video={video}></Thumbnail>

        <div className="info">
          <div className="video-title">{video.title}</div>
          <div className="video-description">{video.description}</div>
        </div>
      </div>
      <LikeButton video={video} />
    </div>
  );
}
```


```js src/data.js hidden
const videos = [
  {
    id: '1',
    title: 'First video',
    description: 'Video description',
    image: 'blue',
  },
  {
    id: '2',
    title: 'Second video',
    description: 'Video description',
    image: 'red',
  },
  {
    id: '3',
    title: 'Third video',
    description: 'Video description',
    image: 'green',
  },
  {
    id: '4',
    title: 'Fourth video',
    description: 'Video description',
    image: 'purple',
  },
  {
    id: '5',
    title: 'Fifth video',
    description: 'Video description',
    image: 'yellow',
  },
  {
    id: '6',
    title: 'Sixth video',
    description: 'Video description',
    image: 'gray',
  },
];

let videosCache = new Map();
let videoCache = new Map();
let videoDetailsCache = new Map();
const VIDEO_DELAY = 1;
const VIDEO_DETAILS_DELAY = 1000;
export function fetchVideos() {
  if (videosCache.has(0)) {
    return videosCache.get(0);
  }
  const promise = new Promise((resolve) => {
    setTimeout(() => {
      resolve(videos);
    }, VIDEO_DELAY);
  });
  videosCache.set(0, promise);
  return promise;
}

export function fetchVideo(id) {
  if (videoCache.has(id)) {
    return videoCache.get(id);
  }
  const promise = new Promise((resolve) => {
    setTimeout(() => {
      resolve(videos.find((video) => video.id === id));
    }, VIDEO_DELAY);
  });
  videoCache.set(id, promise);
  return promise;
}

export function fetchVideoDetails(id) {
  if (videoDetailsCache.has(id)) {
    return videoDetailsCache.get(id);
  }
  const promise = new Promise((resolve) => {
    setTimeout(() => {
      resolve(videos.find((video) => video.id === id));
    }, VIDEO_DETAILS_DELAY);
  });
  videoDetailsCache.set(id, promise);
  return promise;
}
```

```js src/router.js
import {
  useState,
  createContext,
  use,
  useTransition,
  useLayoutEffect,
  useEffect,
} from "react";

const RouterContext = createContext({ url: "/", params: {} });

export function useRouter() {
  return use(RouterContext);
}

export function useIsNavPending() {
  return use(RouterContext).isPending;
}

export function Router({ children }) {
  const [routerState, setRouterState] = useState({
    pendingNav: () => {},
    url: document.location.pathname,
  });
  const [isPending, startTransition] = useTransition();

  function go(url) {
    setRouterState({
      url,
      pendingNav() {
        window.history.pushState({}, "", url);
      },
    });
  }
  function navigate(url) {
    // Update router state in transition.
    startTransition(() => {
      go(url);
    });
  }

  function navigateBack(url) {
    // Update router state in transition.
    startTransition(() => {
      go(url);
    });
  }

  useEffect(() => {
    function handlePopState() {
      // This should not animate because restoration has to be synchronous.
      // Even though it's a transition.
      startTransition(() => {
        setRouterState({
          url: document.location.pathname + document.location.search,
          pendingNav() {
            // Noop. URL has already updated.
          },
        });
      });
    }
    window.addEventListener("popstate", handlePopState);
    return () => {
      window.removeEventListener("popstate", handlePopState);
    };
  }, []);
  const pendingNav = routerState.pendingNav;
  useLayoutEffect(() => {
    pendingNav();
  }, [pendingNav]);

  return (
    <RouterContext
      value={{
        url: routerState.url,
        navigate,
        navigateBack,
        isPending,
        params: {},
      }}
    >
      {children}
    </RouterContext>
  );
}
```

```css src/styles.css
@font-face {
  font-family: Optimistic Text;
  src: url(https://react.dev/fonts/Optimistic_Text_W_Rg.woff2) format("woff2");
  font-weight: 400;
  font-style: normal;
  font-display: swap;
}

@font-face {
  font-family: Optimistic Text;
  src: url(https://react.dev/fonts/Optimistic_Text_W_Md.woff2) format("woff2");
  font-weight: 500;
  font-style: normal;
  font-display: swap;
}

@font-face {
  font-family: Optimistic Text;
  src: url(https://react.dev/fonts/Optimistic_Text_W_Bd.woff2) format("woff2");
  font-weight: 600;
  font-style: normal;
  font-display: swap;
}

@font-face {
  font-family: Optimistic Text;
  src: url(https://react.dev/fonts/Optimistic_Text_W_Bd.woff2) format("woff2");
  font-weight: 700;
  font-style: normal;
  font-display: swap;
}

* {
  box-sizing: border-box;
}

html {
  background-image: url(https://react.dev/images/meta-gradient-dark.png);
  background-size: 100%;
  background-position: -100%;
  background-color: rgb(64 71 86);
  background-repeat: no-repeat;
  height: 100%;
  width: 100%;
}

body {
  font-family: Optimistic Text, -apple-system, ui-sans-serif, system-ui, sans-serif, Apple Color Emoji, Segoe UI Emoji, Segoe UI Symbol, Noto Color Emoji;
  padding: 10px 0 10px 0;
  margin: 0;
  display: flex;
  justify-content: center;
}

#root {
  flex: 1 1;
  height: auto;
  background-color: #fff;
  border-radius: 10px;
  max-width: 450px;
  min-height: 600px;
  padding-bottom: 10px;
}

h1 {
  margin-top: 0;
  font-size: 22px;
}

h2 {
  margin-top: 0;
  font-size: 20px;
}

h3 {
  margin-top: 0;
  font-size: 18px;
}

h4 {
  margin-top: 0;
  font-size: 16px;
}

h5 {
  margin-top: 0;
  font-size: 14px;
}

h6 {
  margin-top: 0;
  font-size: 12px;
}

code {
  font-size: 1.2em;
}

ul {
  padding-inline-start: 20px;
}

.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  padding: 0;
  margin: -1px;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  white-space: nowrap;
  border-width: 0;
}

.absolute {
  position: absolute;
}

.overflow-visible {
  overflow: visible;
}

.visible {
  overflow: visible;
}

.fit {
  width: fit-content;
}


/* Layout */
.page {
  display: flex;
  flex-direction: column;
  height: 100%;
}

.top-hero {
  height: 200px;
  display: flex;
  justify-content: center;
  align-items: center;
  background-image: conic-gradient(
      from 90deg at -10% 100%,
      #2b303b 0deg,
      #2b303b 90deg,
      #16181d 1turn
  );
}

.bottom {
  flex: 1;
  overflow: auto;
}

.top-nav {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 0;
  padding: 0 12px;
  top: 0;
  width: 100%;
  height: 44px;
  color: #23272f;
  font-weight: 700;
  font-size: 20px;
  z-index: 100;
  cursor: default;
}

.content {
  padding: 0 12px;
  margin-top: 4px;
}


.loader {
  color: #23272f;
  font-size: 3px;
  width: 1em;
  margin-right: 18px;
  height: 1em;
  border-radius: 50%;
  position: relative;
  text-indent: -9999em;
  animation: loading-spinner 1.3s infinite linear;
  animation-delay: 200ms;
  transform: translateZ(0);
}

@keyframes loading-spinner {
  0%,
  100% {
    box-shadow: 0 -3em 0 0.2em,
    2em -2em 0 0em, 3em 0 0 -1em,
    2em 2em 0 -1em, 0 3em 0 -1em,
    -2em 2em 0 -1em, -3em 0 0 -1em,
    -2em -2em 0 0;
  }
  12.5% {
    box-shadow: 0 -3em 0 0, 2em -2em 0 0.2em,
    3em 0 0 0, 2em 2em 0 -1em, 0 3em 0 -1em,
    -2em 2em 0 -1em, -3em 0 0 -1em,
    -2em -2em 0 -1em;
  }
  25% {
    box-shadow: 0 -3em 0 -0.5em,
    2em -2em 0 0, 3em 0 0 0.2em,
    2em 2em 0 0, 0 3em 0 -1em,
    -2em 2em 0 -1em, -3em 0 0 -1em,
    -2em -2em 0 -1em;
  }
  37.5% {
    box-shadow: 0 -3em 0 -1em, 2em -2em 0 -1em,
    3em 0em 0 0, 2em 2em 0 0.2em, 0 3em 0 0em,
    -2em 2em 0 -1em, -3em 0em 0 -1em, -2em -2em 0 -1em;
  }
  50% {
    box-shadow: 0 -3em 0 -1em, 2em -2em 0 -1em,
    3em 0 0 -1em, 2em 2em 0 0em, 0 3em 0 0.2em,
    -2em 2em 0 0, -3em 0em 0 -1em, -2em -2em 0 -1em;
  }
  62.5% {
    box-shadow: 0 -3em 0 -1em, 2em -2em 0 -1em,
    3em 0 0 -1em, 2em 2em 0 -1em, 0 3em 0 0,
    -2em 2em 0 0.2em, -3em 0 0 0, -2em -2em 0 -1em;
  }
  75% {
    box-shadow: 0em -3em 0 -1em, 2em -2em 0 -1em,
    3em 0em 0 -1em, 2em 2em 0 -1em, 0 3em 0 -1em,
    -2em 2em 0 0, -3em 0em 0 0.2em, -2em -2em 0 0;
  }
  87.5% {
    box-shadow: 0em -3em 0 0, 2em -2em 0 -1em,
    3em 0 0 -1em, 2em 2em 0 -1em, 0 3em 0 -1em,
    -2em 2em 0 0, -3em 0em 0 0, -2em -2em 0 0.2em;
  }
}

/* LikeButton */
.like-button {
  outline-offset: 2px;
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
  width: 2.5rem;
  height: 2.5rem;
  cursor: pointer;
  border-radius: 9999px;
  border: none;
  outline: none 2px;
  color: #5e687e;
  background: none;
}

.like-button:focus {
  color: #a6423a;
  background-color: rgba(166, 66, 58, .05);
}

.like-button:active {
  color: #a6423a;
  background-color: rgba(166, 66, 58, .05);
  transform: scaleX(0.95) scaleY(0.95);
}

.like-button:hover {
  background-color: #f6f7f9;
}

.like-button.liked {
  color: #a6423a;
}

/* Icons */
@keyframes circle {
  0% {
    transform: scale(0);
    stroke-width: 16px;
  }

  50% {
    transform: scale(.5);
    stroke-width: 16px;
  }

  to {
    transform: scale(1);
    stroke-width: 0;
  }
}

.circle {
  color: rgba(166, 66, 58, .5);
  transform-origin: center;
  transition-property: all;
  transition-duration: .15s;
  transition-timing-function: cubic-bezier(.4,0,.2,1);
}

.circle.liked.animate {
  animation: circle .3s forwards;
}

.heart {
  width: 1.5rem;
  height: 1.5rem;
}

.heart.liked {
  transform-origin: center;
  transition-property: all;
  transition-duration: .15s;
  transition-timing-function: cubic-bezier(.4, 0, .2, 1);
}

.heart.liked.animate {
  animation: scale .35s ease-in-out forwards;
}

.control-icon {
  color: hsla(0, 0%, 100%, .5);
  filter:  drop-shadow(0 20px 13px rgba(0, 0, 0, .03)) drop-shadow(0 8px 5px rgba(0, 0, 0, .08));
}

.chevron-left {
  margin-top: 2px;
  rotate: 90deg;
}


/* Video */
.thumbnail {
  position: relative;
  aspect-ratio: 16 / 9;
  display: flex;
  overflow: hidden;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  border-radius: 0.5rem;
  outline-offset: 2px;
  width: 8rem;
  vertical-align: middle;
  background-color: #ffffff;
  background-size: cover;
  user-select: none;
}

.thumbnail.blue {
  background-image: conic-gradient(at top right, #c76a15, #087ea4, #2b3491);
}

.thumbnail.red {
  background-image: conic-gradient(at top right, #c76a15, #a6423a, #2b3491);
}

.thumbnail.green {
  background-image: conic-gradient(at top right, #c76a15, #388f7f, #2b3491);
}

.thumbnail.purple {
  background-image: conic-gradient(at top right, #c76a15, #575fb7, #2b3491);
}

.thumbnail.yellow {
  background-image: conic-gradient(at top right, #c76a15, #FABD62, #2b3491);
}

.thumbnail.gray {
  background-image: conic-gradient(at top right, #c76a15, #4E5769, #2b3491);
}

.video {
  display: flex;
  flex-direction: row;
  gap: 0.75rem;
  align-items: center;
}

.video .link {
  display: flex;
  flex-direction: row;
  flex: 1 1 0;
  gap: 0.125rem;
  outline-offset: 4px;
  cursor: pointer;
}

.video .info {
  display: flex;
  flex-direction: column;
  justify-content: center;
  margin-left: 8px;
  gap: 0.125rem;
}

.video .info:hover {
  text-decoration: underline;
}

.video-title {
  font-size: 15px;
  line-height: 1.25;
  font-weight: 700;
  color: #23272f;
}

.video-description {
  color: #5e687e;
  font-size: 13px;
}

/* Details */
.details .thumbnail {
  position: relative;
  aspect-ratio: 16 / 9;
  display: flex;
  overflow: hidden;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  border-radius: 0.5rem;
  outline-offset: 2px;
  width: 100%;
  vertical-align: middle;
  background-color: #ffffff;
  background-size: cover;
  user-select: none;
}

.video-details-title {
  margin-top: 8px;
}

.video-details-speaker {
  display: flex;
  gap: 8px;
  margin-top: 10px
}

.back {
  display: flex;
  align-items: center;
  margin-left: -5px;
  cursor: pointer;
}

.back:hover {
  text-decoration: underline;
}

.info-title {
  font-size: 1.5rem;
  font-weight: 700;
  line-height: 1.25;
  margin: 8px 0 0 0 ;
}

.info-description {
  margin: 8px 0 0 0;
}

.controls {
  cursor: pointer;
}

.fallback {
  background: #f6f7f8 linear-gradient(to right, #e6e6e6 5%, #cccccc 25%, #e6e6e6 35%) no-repeat;
  background-size: 800px 104px;
  display: block;
  line-height: 1.25;
  margin: 8px 0 0 0;
  border-radius: 5px;
  overflow: hidden;

  animation: 1s linear 1s infinite shimmer;
  animation-delay: 300ms;
  animation-duration: 1s;
  animation-fill-mode: forwards;
  animation-iteration-count: infinite;
  animation-name: shimmer;
  animation-timing-function: linear;
}


.fallback.title {
  width: 130px;
  height: 30px;

}

.fallback.description {
  width: 150px;
  height: 21px;
}

@keyframes shimmer {
  0% {
    background-position: -468px 0;
  }

  100% {
    background-position: 468px 0;
  }
}

.search {
  margin-bottom: 10px;
}
.search-input {
  width: 100%;
  position: relative;
}

.search-icon {
  position: absolute;
  top: 0;
  bottom: 0;
  inset-inline-start: 0;
  display: flex;
  align-items: center;
  padding-inline-start: 1rem;
  pointer-events: none;
  color: #99a1b3;
}

.search-input input {
  display: flex;
  padding-inline-start: 2.75rem;
  padding-top: 10px;
  padding-bottom: 10px;
  width: 100%;
  text-align: start;
  background-color: rgb(235 236 240);
  outline: 2px solid transparent;
  cursor: pointer;
  border: none;
  align-items: center;
  color: rgb(35 39 47);
  border-radius: 9999px;
  vertical-align: middle;
  font-size: 15px;
}

.search-input input:hover, .search-input input:active {
  background-color: rgb(235 236 240/ 0.8);
  color: rgb(35 39 47/ 0.8);
}

/* Home */
.video-list {
  position: relative;
}

.video-list .videos {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  overflow-y: auto;
  height: 100%;
}
```

```js src/index.js hidden
import React, {StrictMode} from 'react';
import {createRoot} from 'react-dom/client';
import './styles.css';

import App from './App';
import {Router} from './router';

const root = createRoot(document.getElementById('root'));
root.render(
  <StrictMode>
    <Router>
      <App />
    </Router>
  </StrictMode>
);
```

```json package.json hidden
{
  "dependencies": {
    "react": "canary",
    "react-dom": "canary",
    "react-scripts": "latest"
  },
  "scripts": {
    "start": "react-scripts start",
    "build": "react-scripts build",
    "test": "react-scripts test --env=jsdom",
    "eject": "react-scripts eject"
  }
}
```

</Sandpack>

<Note>

#### 视图过渡不会替代由 CSS 和 JS 驱动的动画 {/*view-transitions-do-not-replace-css-and-js-driven-animations*/}

视图过渡旨在用于 UI 过渡，如导航、展开、打开或重新排序。它们并不是为了替代应用中的所有动画。

在我们上面的示例应用中，请注意当你点击"喜欢"按钮以及在 Suspense 后备方案闪烁时已经有动画了。这些是 CSS 动画的良好用例，因为它们是为特定元素添加动画。

</Note>

### 为导航添加动画 {/*animating-navigations*/}

我们的应用包含一个支持 Suspense 的路由器，其中[页面过渡已标记为 Transitions](/reference/react/useTransition#building-a-suspense-enabled-router)，这意味着导航是通过 `startTransition` 执行的：

```js
function navigate(url) {
  startTransition(() => {
    go(url);
  });
}
```

`startTransition` 是一个视图过渡触发器，因此我们可以添加 `<ViewTransition>` 来为页面之间的切换添加动画：

```js
// "要"动画的内容
<ViewTransition key={url}>
  {url === '/' ? <Home /> : <TalkDetails />}
</ViewTransition>
```

当 `url` 改变时，`<ViewTransition>` 和新路由会被渲染。由于 `<ViewTransition>` 是在 `startTransition` 内部更新的，因此 `<ViewTransition>` 会被激活以进行动画处理。


默认情况下，视图过渡包含浏览器默认的交叉淡入淡出动画。将其添加到我们的示例中，现在每当我们在页面之间导航时都会有交叉淡入淡出效果：

<Sandpack>

```js src/App.js active
import {ViewTransition} from 'react'; import Details from './Details';
import Home from './Home'; import {useRouter} from './router';

export default function App() {
  const {url} = useRouter();

  // 使用 ViewTransition 在页面间进行动画。
  // 默认情况下不需要添加 CSS。
  return (
    <ViewTransition>
      {url === '/' ? <Home /> : <Details />}
    </ViewTransition>
  );
}
```

```js src/Details.js hidden
import { fetchVideo, fetchVideoDetails } from "./data";
import { Thumbnail, VideoControls } from "./Videos";
import { useRouter } from "./router";
import Layout from "./Layout";
import { use, Suspense } from "react";
import { ChevronLeft } from "./Icons";

function VideoInfo({ id }) {
  const details = use(fetchVideoDetails(id));
  return (
    <>
      <p className="info-title">{details.title}</p>
      <p className="info-description">{details.description}</p>
    </>
  );
}

function VideoInfoFallback() {
  return (
    <>
      <div className="fallback title"></div>
      <div className="fallback description"></div>
    </>
  );
}

export default function Details() {
  const { url, navigateBack } = useRouter();
  const videoId = url.split("/").pop();
  const video = use(fetchVideo(videoId));

  return (
    <Layout
      heading={
        <div
          className="fit back"
          onClick={() => {
            navigateBack("/");
          }}
        >
          <ChevronLeft /> Back
        </div>
      }
    >
      <div className="details">
        <Thumbnail video={video} large>
          <VideoControls />
        </Thumbnail>
        <Suspense fallback={<VideoInfoFallback />}>
          <VideoInfo id={video.id} />
        </Suspense>
      </div>
    </Layout>
  );
}

```

```js src/Home.js hidden
import { Video } from "./Videos";
import Layout from "./Layout";
import { fetchVideos } from "./data";
import { useId, useState, use } from "react";
import { IconSearch } from "./Icons";

function SearchInput({ value, onChange }) {
  const id = useId();
  return (
    <form className="search" onSubmit={(e) => e.preventDefault()}>
      <label htmlFor={id} className="sr-only">
        Search
      </label>
      <div className="search-input">
        <div className="search-icon">
          <IconSearch />
        </div>
        <input
          type="text"
          id={id}
          placeholder="Search"
          value={value}
          onChange={(e) => onChange(e.target.value)}
        />
      </div>
    </form>
  );
}

function filterVideos(videos, query) {
  const keywords = query
    .toLowerCase()
    .split(" ")
    .filter((s) => s !== "");
  if (keywords.length === 0) {
    return videos;
  }
  return videos.filter((video) => {
    const words = (video.title + " " + video.description)
      .toLowerCase()
      .split(" ");
    return keywords.every((kw) => words.some((w) => w.includes(kw)));
  });
}

export default function Home() {
  const videos = use(fetchVideos());
  const count = videos.length;
  const [searchText, setSearchText] = useState("");
  const foundVideos = filterVideos(videos, searchText);
  return (
    <Layout heading={<div className="fit">{count} Videos</div>}>
      <SearchInput value={searchText} onChange={setSearchText} />
      <div className="video-list">
        {foundVideos.length === 0 && (
          <div className="no-results">No results</div>
        )}
        <div className="videos">
          {foundVideos.map((video) => (
            <Video key={video.id} video={video} />
          ))}
        </div>
      </div>
    </Layout>
  );
}

```

```js src/Icons.js hidden
export function ChevronLeft() {
  return (
    <svg
      className="chevron-left"
      xmlns="http://www.w3.org/2000/svg"
      width="20"
      height="20"
      viewBox="0 0 20 20">
      <g fill="none" fillRule="evenodd" transform="translate(-446 -398)">
        <path
          fill="currentColor"
          fillRule="nonzero"
          d="M95.8838835,240.366117 C95.3957281,239.877961 94.6042719,239.877961 94.1161165,240.366117 C93.6279612,240.854272 93.6279612,241.645728 94.1161165,242.133883 L98.6161165,246.633883 C99.1042719,247.122039 99.8957281,247.122039 100.383883,246.633883 L104.883883,242.133883 C105.372039,241.645728 105.372039,240.854272 104.883883,240.366117 C104.395728,239.877961 103.604272,239.877961 103.116117,240.366117 L99.5,243.982233 L95.8838835,240.366117 Z"
          transform="translate(356.5 164.5)"
        />
        <polygon points="446 418 466 418 466 398 446 398" />
      </g>
    </svg>
  );
}

export function PauseIcon() {
  return (
    <svg
      className="control-icon"
      style={{padding: '4px'}}
      width="100"
      height="100"
      viewBox="0 0 512 512"
      fill="none"
      xmlns="http://www.w3.org/2000/svg">
      <path
        fillRule="evenodd"
        clipRule="evenodd"
        d="M256 0C114.617 0 0 114.615 0 256s114.617 256 256 256 256-114.615 256-256S397.383 0 256 0zm-32 320c0 8.836-7.164 16-16 16h-32c-8.836 0-16-7.164-16-16V192c0-8.836 7.164-16 16-16h32c8.836 0 16 7.164 16 16v128zm128 0c0 8.836-7.164 16-16 16h-32c-8.836 0-16-7.164-16-16V192c0-8.836 7.164-16 16-16h32c8.836 0 16 7.164 16 16v128z"
        fill="currentColor"
      />
    </svg>
  );
}

export function PlayIcon() {
  return (
    <svg
      className="control-icon"
      width="100"
      height="100"
      viewBox="0 0 72 72"
      fill="none"
      xmlns="http://www.w3.org/2000/svg">
      <path
        fillRule="evenodd"
        clipRule="evenodd"
        d="M36 69C54.2254 69 69 54.2254 69 36C69 17.7746 54.2254 3 36 3C17.7746 3 3 17.7746 3 36C3 54.2254 17.7746 69 36 69ZM52.1716 38.6337L28.4366 51.5801C26.4374 52.6705 24 51.2235 24 48.9464V23.0536C24 20.7764 26.4374 19.3295 28.4366 20.4199L52.1716 33.3663C54.2562 34.5034 54.2562 37.4966 52.1716 38.6337Z"
        fill="currentColor"
      />
    </svg>
  );
}
export function Heart({liked, animate}) {
  return (
    <>
      <svg
        className="absolute overflow-visible"
        viewBox="0 0 24 24"
        fill="none"
        xmlns="http://www.w3.org/2000/svg">
        <circle
          className={`circle ${liked ? 'liked' : ''} ${animate ? 'animate' : ''}`}
          cx="12"
          cy="12"
          r="11.5"
          fill="transparent"
          strokeWidth="0"
          stroke="currentColor"
        />
      </svg>

      <svg
        className={`heart ${liked ? 'liked' : ''} ${animate ? 'animate' : ''}`}
        viewBox="0 0 24 24"
        fill="none"
        xmlns="http://www.w3.org/2000/svg">
        {liked ? (
          <path
            d="M12 23a.496.496 0 0 1-.26-.074C7.023 19.973 0 13.743 0 8.68c0-4.12 2.322-6.677 6.058-6.677 2.572 0 5.108 2.387 5.134 2.41l.808.771.808-.771C12.834 4.387 15.367 2 17.935 2 21.678 2 24 4.558 24 8.677c0 5.06-7.022 11.293-11.74 14.246a.496.496 0 0 1-.26.074V23z"
            fill="currentColor"
          />
        ) : (
          <path
            fillRule="evenodd"
            clipRule="evenodd"
            d="m12 5.184-.808-.771-.004-.004C11.065 4.299 8.522 2.003 6 2.003c-3.736 0-6 2.558-6 6.677 0 4.47 5.471 9.848 10 13.079.602.43 1.187.82 1.74 1.167A.497.497 0 0 0 12 23v-.003c.09 0 .182-.026.26-.074C16.977 19.97 24 13.737 24 8.677 24 4.557 21.743 2 18 2c-2.569 0-5.166 2.387-5.192 2.413L12 5.184zm-.002 15.525c2.071-1.388 4.477-3.342 6.427-5.47C20.72 12.733 22 10.401 22 8.677c0-1.708-.466-2.855-1.087-3.55C20.316 4.459 19.392 4 18 4c-.726 0-1.63.364-2.5.9-.67.412-1.148.82-1.266.92-.03.025-.037.031-.019.014l-.013.013L12 7.949 9.832 5.88a10.08 10.08 0 0 0-1.33-.977C7.633 4.367 6.728 4.003 6 4.003c-1.388 0-2.312.459-2.91 1.128C2.466 5.826 2 6.974 2 8.68c0 1.726 1.28 4.058 3.575 6.563 1.948 2.127 4.352 4.078 6.423 5.466z"
            fill="currentColor"
          />
        )}
      </svg>
    </>
  );
}

export function IconSearch(props) {
  return (
    <svg width="1em" height="1em" viewBox="0 0 20 20">
      <path
        d="M14.386 14.386l4.0877 4.0877-4.0877-4.0877c-2.9418 2.9419-7.7115 2.9419-10.6533 0-2.9419-2.9418-2.9419-7.7115 0-10.6533 2.9418-2.9419 7.7115-2.9419 10.6533 0 2.9419 2.9418 2.9419 7.7115 0 10.6533z"
        stroke="currentColor"
        fill="none"
        strokeWidth="2"
        fillRule="evenodd"
        strokeLinecap="round"
        strokeLinejoin="round"></path>
    </svg>
  );
}
```

```js src/Layout.js
import {ViewTransition} from 'react'; import { useIsNavPending } from "./router";

export default function Page({ heading, children }) {
  const isPending = useIsNavPending();

  return (
    <div className="page">
      <div className="top">
        <div className="top-nav">
          {heading}
          {isPending && <span className="loader"></span>}
        </div>
      </div>
      {/* Opt-out of ViewTransition for the content. */}
      {/* Content can define it's own ViewTransition. */}
      <ViewTransition default="none">
        <div className="bottom">
          <div className="content">{children}</div>
        </div>
      </ViewTransition>
    </div>
  );
}
```

```js src/LikeButton.js hidden
import {useState} from 'react';
import {Heart} from './Icons';

// A hack since we don't actually have a backend.
// Unlike local state, this survives videos being filtered.
const likedVideos = new Set();

export default function LikeButton({video}) {
  const [isLiked, setIsLiked] = useState(() => likedVideos.has(video.id));
  const [animate, setAnimate] = useState(false);
  return (
    <button
      className={`like-button ${isLiked && 'liked'}`}
      aria-label={isLiked ? 'Unsave' : 'Save'}
      onClick={() => {
        const nextIsLiked = !isLiked;
        if (nextIsLiked) {
          likedVideos.add(video.id);
        } else {
          likedVideos.delete(video.id);
        }
        setAnimate(true);
        setIsLiked(nextIsLiked);
      }}>
      <Heart liked={isLiked} animate={animate} />
    </button>
  );
}
```

```js src/Videos.js hidden
import { useState } from "react";
import LikeButton from "./LikeButton";
import { useRouter } from "./router";
import { PauseIcon, PlayIcon } from "./Icons";
import { startTransition } from "react";

export function VideoControls() {
  const [isPlaying, setIsPlaying] = useState(false);

  return (
    <span
      className="controls"
      onClick={() =>
        startTransition(() => {
          setIsPlaying((p) => !p);
        })
      }
    >
      {isPlaying ? <PauseIcon /> : <PlayIcon />}
    </span>
  );
}

export function Thumbnail({ video, children }) {
  return (
    <div
      aria-hidden="true"
      tabIndex={-1}
      className={`thumbnail ${video.image}`}
    >
      {children}
    </div>
  );
}

export function Video({ video }) {
  const { navigate } = useRouter();

  return (
    <div className="video">
      <div
        className="link"
        onClick={(e) => {
          e.preventDefault();
          navigate(`/video/${video.id}`);
        }}
      >
        <Thumbnail video={video}></Thumbnail>

        <div className="info">
          <div className="video-title">{video.title}</div>
          <div className="video-description">{video.description}</div>
        </div>
      </div>
      <LikeButton video={video} />
    </div>
  );
}
```


```js src/data.js hidden
const videos = [
  {
    id: '1',
    title: 'First video',
    description: 'Video description',
    image: 'blue',
  },
  {
    id: '2',
    title: 'Second video',
    description: 'Video description',
    image: 'red',
  },
  {
    id: '3',
    title: 'Third video',
    description: 'Video description',
    image: 'green',
  },
  {
    id: '4',
    title: 'Fourth video',
    description: 'Video description',
    image: 'purple',
  },
  {
    id: '5',
    title: 'Fifth video',
    description: 'Video description',
    image: 'yellow',
  },
  {
    id: '6',
    title: 'Sixth video',
    description: 'Video description',
    image: 'gray',
  },
];

let videosCache = new Map();
let videoCache = new Map();
let videoDetailsCache = new Map();
const VIDEO_DELAY = 1;
const VIDEO_DETAILS_DELAY = 1000;
export function fetchVideos() {
  if (videosCache.has(0)) {
    return videosCache.get(0);
  }
  const promise = new Promise((resolve) => {
    setTimeout(() => {
      resolve(videos);
    }, VIDEO_DELAY);
  });
  videosCache.set(0, promise);
  return promise;
}

export function fetchVideo(id) {
  if (videoCache.has(id)) {
    return videoCache.get(id);
  }
  const promise = new Promise((resolve) => {
    setTimeout(() => {
      resolve(videos.find((video) => video.id === id));
    }, VIDEO_DELAY);
  });
  videoCache.set(id, promise);
  return promise;
}

export function fetchVideoDetails(id) {
  if (videoDetailsCache.has(id)) {
    return videoDetailsCache.get(id);
  }
  const promise = new Promise((resolve) => {
    setTimeout(() => {
      resolve(videos.find((video) => video.id === id));
    }, VIDEO_DETAILS_DELAY);
  });
  videoDetailsCache.set(id, promise);
  return promise;
}
```

```js src/router.js
import {useState, createContext,use,useTransition,useLayoutEffect,useEffect} from "react";

export function Router({ children }) {
  const [isPending, startTransition] = useTransition();

  function navigate(url) {
    // 在过渡中更新路由器状态。
    startTransition(() => {
      go(url);
    });
  }




  const [routerState, setRouterState] = useState({
    pendingNav: () => {},
    url: document.location.pathname,
  });


  function go(url) {
    setRouterState({
      url,
      pendingNav() {
        window.history.pushState({}, "", url);
      },
    });
  }


  function navigateBack(url) {
    startTransition(() => {
      go(url);
    });
  }

  useEffect(() => {
    function handlePopState() {
      // This should not animate because restoration has to be synchronous.
      // Even though it's a transition.
      startTransition(() => {
        setRouterState({
          url: document.location.pathname + document.location.search,
          pendingNav() {
            // Noop. URL has already updated.
          },
        });
      });
    }
    window.addEventListener("popstate", handlePopState);
    return () => {
      window.removeEventListener("popstate", handlePopState);
    };
  }, []);
  const pendingNav = routerState.pendingNav;
  useLayoutEffect(() => {
    pendingNav();
  }, [pendingNav]);

  return (
    <RouterContext
      value={{
        url: routerState.url,
        navigate,
        navigateBack,
        isPending,
        params: {},
      }}
    >
      {children}
    </RouterContext>
  );
}

const RouterContext = createContext({ url: "/", params: {} });

export function useRouter() {
  return use(RouterContext);
}

export function useIsNavPending() {
  return use(RouterContext).isPending;
}
```

```css src/styles.css hidden
@font-face {
  font-family: Optimistic Text;
  src: url(https://react.dev/fonts/Optimistic_Text_W_Rg.woff2) format("woff2");
  font-weight: 400;
  font-style: normal;
  font-display: swap;
}

@font-face {
  font-family: Optimistic Text;
  src: url(https://react.dev/fonts/Optimistic_Text_W_Md.woff2) format("woff2");
  font-weight: 500;
  font-style: normal;
  font-display: swap;
}

@font-face {
  font-family: Optimistic Text;
  src: url(https://react.dev/fonts/Optimistic_Text_W_Bd.woff2) format("woff2");
  font-weight: 600;
  font-style: normal;
  font-display: swap;
}

@font-face {
  font-family: Optimistic Text;
  src: url(https://react.dev/fonts/Optimistic_Text_W_Bd.woff2) format("woff2");
  font-weight: 700;
  font-style: normal;
  font-display: swap;
}

* {
  box-sizing: border-box;
}

html {
  background-image: url(https://react.dev/images/meta-gradient-dark.png);
  background-size: 100%;
  background-position: -100%;
  background-color: rgb(64 71 86);
  background-repeat: no-repeat;
  height: 100%;
  width: 100%;
}

body {
  font-family: Optimistic Text, -apple-system, ui-sans-serif, system-ui, sans-serif, Apple Color Emoji, Segoe UI Emoji, Segoe UI Symbol, Noto Color Emoji;
  padding: 10px 0 10px 0;
  margin: 0;
  display: flex;
  justify-content: center;
}

#root {
  flex: 1 1;
  height: auto;
  background-color: #fff;
  border-radius: 10px;
  max-width: 450px;
  min-height: 600px;
  padding-bottom: 10px;
}

h1 {
  margin-top: 0;
  font-size: 22px;
}

h2 {
  margin-top: 0;
  font-size: 20px;
}

h3 {
  margin-top: 0;
  font-size: 18px;
}

h4 {
  margin-top: 0;
  font-size: 16px;
}

h5 {
  margin-top: 0;
  font-size: 14px;
}

h6 {
  margin-top: 0;
  font-size: 12px;
}

code {
  font-size: 1.2em;
}

ul {
  padding-inline-start: 20px;
}

.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  padding: 0;
  margin: -1px;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  white-space: nowrap;
  border-width: 0;
}

.absolute {
  position: absolute;
}

.overflow-visible {
  overflow: visible;
}

.visible {
  overflow: visible;
}

.fit {
  width: fit-content;
}


/* Layout */
.page {
  display: flex;
  flex-direction: column;
  height: 100%;
}

.top-hero {
  height: 200px;
  display: flex;
  justify-content: center;
  align-items: center;
  background-image: conic-gradient(
      from 90deg at -10% 100%,
      #2b303b 0deg,
      #2b303b 90deg,
      #16181d 1turn
  );
}

.bottom {
  flex: 1;
  overflow: auto;
}

.top-nav {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 0;
  padding: 0 12px;
  top: 0;
  width: 100%;
  height: 44px;
  color: #23272f;
  font-weight: 700;
  font-size: 20px;
  z-index: 100;
  cursor: default;
}

.content {
  padding: 0 12px;
  margin-top: 4px;
}


.loader {
  color: #23272f;
  font-size: 3px;
  width: 1em;
  margin-right: 18px;
  height: 1em;
  border-radius: 50%;
  position: relative;
  text-indent: -9999em;
  animation: loading-spinner 1.3s infinite linear;
  animation-delay: 200ms;
  transform: translateZ(0);
}

@keyframes loading-spinner {
  0%,
  100% {
    box-shadow: 0 -3em 0 0.2em,
    2em -2em 0 0em, 3em 0 0 -1em,
    2em 2em 0 -1em, 0 3em 0 -1em,
    -2em 2em 0 -1em, -3em 0 0 -1em,
    -2em -2em 0 0;
  }
  12.5% {
    box-shadow: 0 -3em 0 0, 2em -2em 0 0.2em,
    3em 0 0 0, 2em 2em 0 -1em, 0 3em 0 -1em,
    -2em 2em 0 -1em, -3em 0 0 -1em,
    -2em -2em 0 -1em;
  }
  25% {
    box-shadow: 0 -3em 0 -0.5em,
    2em -2em 0 0, 3em 0 0 0.2em,
    2em 2em 0 0, 0 3em 0 -1em,
    -2em 2em 0 -1em, -3em 0 0 -1em,
    -2em -2em 0 -1em;
  }
  37.5% {
    box-shadow: 0 -3em 0 -1em, 2em -2em 0 -1em,
    3em 0em 0 0, 2em 2em 0 0.2em, 0 3em 0 0em,
    -2em 2em 0 -1em, -3em 0em 0 -1em, -2em -2em 0 -1em;
  }
  50% {
    box-shadow: 0 -3em 0 -1em, 2em -2em 0 -1em,
    3em 0 0 -1em, 2em 2em 0 0em, 0 3em 0 0.2em,
    -2em 2em 0 0, -3em 0em 0 -1em, -2em -2em 0 -1em;
  }
  62.5% {
    box-shadow: 0 -3em 0 -1em, 2em -2em 0 -1em,
    3em 0 0 -1em, 2em 2em 0 -1em, 0 3em 0 0,
    -2em 2em 0 0.2em, -3em 0 0 0, -2em -2em 0 -1em;
  }
  75% {
    box-shadow: 0em -3em 0 -1em, 2em -2em 0 -1em,
    3em 0em 0 -1em, 2em 2em 0 -1em, 0 3em 0 -1em,
    -2em 2em 0 0, -3em 0em 0 0.2em, -2em -2em 0 0;
  }
  87.5% {
    box-shadow: 0em -3em 0 0, 2em -2em 0 -1em,
    3em 0 0 -1em, 2em 2em 0 -1em, 0 3em 0 -1em,
    -2em 2em 0 0, -3em 0em 0 0, -2em -2em 0 0.2em;
  }
}

/* LikeButton */
.like-button {
  outline-offset: 2px;
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
  width: 2.5rem;
  height: 2.5rem;
  cursor: pointer;
  border-radius: 9999px;
  border: none;
  outline: none 2px;
  color: #5e687e;
  background: none;
}

.like-button:focus {
  color: #a6423a;
  background-color: rgba(166, 66, 58, .05);
}

.like-button:active {
  color: #a6423a;
  background-color: rgba(166, 66, 58, .05);
  transform: scaleX(0.95) scaleY(0.95);
}

.like-button:hover {
  background-color: #f6f7f9;
}

.like-button.liked {
  color: #a6423a;
}

/* Icons */
@keyframes circle {
  0% {
    transform: scale(0);
    stroke-width: 16px;
  }

  50% {
    transform: scale(.5);
    stroke-width: 16px;
  }

  to {
    transform: scale(1);
    stroke-width: 0;
  }
}

.circle {
  color: rgba(166, 66, 58, .5);
  transform-origin: center;
  transition-property: all;
  transition-duration: .15s;
  transition-timing-function: cubic-bezier(.4,0,.2,1);
}

.circle.liked.animate {
  animation: circle .3s forwards;
}

.heart {
  width: 1.5rem;
  height: 1.5rem;
}

.heart.liked {
  transform-origin: center;
  transition-property: all;
  transition-duration: .15s;
  transition-timing-function: cubic-bezier(.4, 0, .2, 1);
}

.heart.liked.animate {
  animation: scale .35s ease-in-out forwards;
}

.control-icon {
  color: hsla(0, 0%, 100%, .5);
  filter:  drop-shadow(0 20px 13px rgba(0, 0, 0, .03)) drop-shadow(0 8px 5px rgba(0, 0, 0, .08));
}

.chevron-left {
  margin-top: 2px;
  rotate: 90deg;
}


/* Video */
.thumbnail {
  position: relative;
  aspect-ratio: 16 / 9;
  display: flex;
  overflow: hidden;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  border-radius: 0.5rem;
  outline-offset: 2px;
  width: 8rem;
  vertical-align: middle;
  background-color: #ffffff;
  background-size: cover;
  user-select: none;
}

.thumbnail.blue {
  background-image: conic-gradient(at top right, #c76a15, #087ea4, #2b3491);
}

.thumbnail.red {
  background-image: conic-gradient(at top right, #c76a15, #a6423a, #2b3491);
}

.thumbnail.green {
  background-image: conic-gradient(at top right, #c76a15, #388f7f, #2b3491);
}

.thumbnail.purple {
  background-image: conic-gradient(at top right, #c76a15, #575fb7, #2b3491);
}

.thumbnail.yellow {
  background-image: conic-gradient(at top right, #c76a15, #FABD62, #2b3491);
}

.thumbnail.gray {
  background-image: conic-gradient(at top right, #c76a15, #4E5769, #2b3491);
}

.video {
  display: flex;
  flex-direction: row;
  gap: 0.75rem;
  align-items: center;
}

.video .link {
  display: flex;
  flex-direction: row;
  flex: 1 1 0;
  gap: 0.125rem;
  outline-offset: 4px;
  cursor: pointer;
}

.video .info {
  display: flex;
  flex-direction: column;
  justify-content: center;
  margin-left: 8px;
  gap: 0.125rem;
}

.video .info:hover {
  text-decoration: underline;
}

.video-title {
  font-size: 15px;
  line-height: 1.25;
  font-weight: 700;
  color: #23272f;
}

.video-description {
  color: #5e687e;
  font-size: 13px;
}

/* Details */
.details .thumbnail {
  position: relative;
  aspect-ratio: 16 / 9;
  display: flex;
  overflow: hidden;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  border-radius: 0.5rem;
  outline-offset: 2px;
  width: 100%;
  vertical-align: middle;
  background-color: #ffffff;
  background-size: cover;
  user-select: none;
}

.video-details-title {
  margin-top: 8px;
}

.video-details-speaker {
  display: flex;
  gap: 8px;
  margin-top: 10px
}

.back {
  display: flex;
  align-items: center;
  margin-left: -5px;
  cursor: pointer;
}

.back:hover {
  text-decoration: underline;
}

.info-title {
  font-size: 1.5rem;
  font-weight: 700;
  line-height: 1.25;
  margin: 8px 0 0 0 ;
}

.info-description {
  margin: 8px 0 0 0;
}

.controls {
  cursor: pointer;
}

.fallback {
  background: #f6f7f8 linear-gradient(to right, #e6e6e6 5%, #cccccc 25%, #e6e6e6 35%) no-repeat;
  background-size: 800px 104px;
  display: block;
  line-height: 1.25;
  margin: 8px 0 0 0;
  border-radius: 5px;
  overflow: hidden;

  animation: 1s linear 1s infinite shimmer;
  animation-delay: 300ms;
  animation-duration: 1s;
  animation-fill-mode: forwards;
  animation-iteration-count: infinite;
  animation-name: shimmer;
  animation-timing-function: linear;
}


.fallback.title {
  width: 130px;
  height: 30px;

}

.fallback.description {
  width: 150px;
  height: 21px;
}

@keyframes shimmer {
  0% {
    background-position: -468px 0;
  }

  100% {
    background-position: 468px 0;
  }
}

.search {
  margin-bottom: 10px;
}
.search-input {
  width: 100%;
  position: relative;
}

.search-icon {
  position: absolute;
  top: 0;
  bottom: 0;
  inset-inline-start: 0;
  display: flex;
  align-items: center;
  padding-inline-start: 1rem;
  pointer-events: none;
  color: #99a1b3;
}

.search-input input {
  display: flex;
  padding-inline-start: 2.75rem;
  padding-top: 10px;
  padding-bottom: 10px;
  width: 100%;
  text-align: start;
  background-color: rgb(235 236 240);
  outline: 2px solid transparent;
  cursor: pointer;
  border: none;
  align-items: center;
  color: rgb(35 39 47);
  border-radius: 9999px;
  vertical-align: middle;
  font-size: 15px;
}

.search-input input:hover, .search-input input:active {
  background-color: rgb(235 236 240/ 0.8);
  color: rgb(35 39 47/ 0.8);
}

/* Home */
.video-list {
  position: relative;
}

.video-list .videos {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  overflow-y: auto;
  height: 100%;
}
```

```js src/index.js hidden
import React, {StrictMode} from 'react';
import {createRoot} from 'react-dom/client';
import './styles.css';

import App from './App';
import {Router} from './router';

const root = createRoot(document.getElementById('root'));
root.render(
  <StrictMode>
    <Router>
      <App />
    </Router>
  </StrictMode>
);
```

```json package.json hidden
{
  "dependencies": {
    "react": "canary",
    "react-dom": "canary",
    "react-scripts": "latest"
  },
  "scripts": {
    "start": "react-scripts start",
    "build": "react-scripts build",
    "test": "react-scripts test --env=jsdom",
    "eject": "react-scripts eject"
  }
}
```

</Sandpack>

由于我们的路由器已经使用 `startTransition` 更新路由，添加 `<ViewTransition>` 的这一行更改就会激活默认的交叉淡入淡出动画。

如果你好奇这是如何工作的，请查看文档中的 [`<ViewTransition>` 如何工作？](/reference/react/ViewTransition#how-does-viewtransition-work)

<Note>

#### 退出 `<ViewTransition>` 动画 {/*opting-out-of-viewtransition-animations*/}

在这个例子中，为了简单起见，我们将应用的根部分包装在 `<ViewTransition>` 中，但这意味着应用中的所有过渡都将有动画效果，这可能会导致意外的动画。

为了解决这个问题，我们用 `"none"` 包装路由子组件，这样每个页面都可以控制自己的动画：

```js
// Layout.js
<ViewTransition default="none">
  {children}
</ViewTransition>
```

在实践中，导航应该通过 "enter" 和 "exit" 属性或使用 Transition Types 来完成。

</Note>

### 自定义动画 {/*customizing-animations*/}

默认情况下，`<ViewTransition>` 包含浏览器默认的交叉淡入淡出效果。

要自定义动画，你可以根据 [`<ViewTransition>` 的激活方式](/reference/react/ViewTransition#props)，为 `<ViewTransition>` 组件提供属性来指定要使用的动画。

例如，我们可以减慢 `default` 交叉淡入淡出动画：

```js
<ViewTransition default="slow-fade">
  <Home />
</ViewTransition>
```

并使用[视图过渡类](/reference/react/ViewTransition#view-transition-class)在 CSS 中定义 `slow-fade`：

```css
::view-transition-old(.slow-fade) {
    animation-duration: 500ms;
}

::view-transition-new(.slow-fade) {
    animation-duration: 500ms;
}
```

现在，交叉淡入淡出更慢了：

<Sandpack>

```js src/App.js active
import { ViewTransition } from "react";
import Details from "./Details";
import Home from "./Home";
import { useRouter } from "./router";

export default function App() {
  const { url } = useRouter();

  // Define a default animation of .slow-fade.
  // See animations.css for the animation definition.
  return (
    <ViewTransition default="slow-fade">
      {url === '/' ? <Home /> : <Details />}
    </ViewTransition>
  );
}
```

```js src/Details.js hidden
import { fetchVideo, fetchVideoDetails } from "./data";
import { Thumbnail, VideoControls } from "./Videos";
import { useRouter } from "./router";
import Layout from "./Layout";
import { use, Suspense } from "react";
import { ChevronLeft } from "./Icons";

function VideoInfo({ id }) {
  const details = use(fetchVideoDetails(id));
  return (
    <>
      <p className="info-title">{details.title}</p>
      <p className="info-description">{details.description}</p>
    </>
  );
}

function VideoInfoFallback() {
  return (
    <>
      <div className="fallback title"></div>
      <div className="fallback description"></div>
    </>
  );
}

export default function Details() {
  const { url, navigateBack } = useRouter();
  const videoId = url.split("/").pop();
  const video = use(fetchVideo(videoId));

  return (
    <Layout
      heading={
        <div
          className="fit back"
          onClick={() => {
            navigateBack("/");
          }}
        >
          <ChevronLeft /> Back
        </div>
      }
    >
      <div className="details">
        <Thumbnail video={video} large>
          <VideoControls />
        </Thumbnail>
        <Suspense fallback={<VideoInfoFallback />}>
          <VideoInfo id={video.id} />
        </Suspense>
      </div>
    </Layout>
  );
}

```

```js src/Home.js hidden
import { Video } from "./Videos";
import Layout from "./Layout";
import { fetchVideos } from "./data";
import { useId, useState, use } from "react";
import { IconSearch } from "./Icons";

function SearchInput({ value, onChange }) {
  const id = useId();
  return (
    <form className="search" onSubmit={(e) => e.preventDefault()}>
      <label htmlFor={id} className="sr-only">
        Search
      </label>
      <div className="search-input">
        <div className="search-icon">
          <IconSearch />
        </div>
        <input
          type="text"
          id={id}
          placeholder="Search"
          value={value}
          onChange={(e) => onChange(e.target.value)}
        />
      </div>
    </form>
  );
}

function filterVideos(videos, query) {
  const keywords = query
    .toLowerCase()
    .split(" ")
    .filter((s) => s !== "");
  if (keywords.length === 0) {
    return videos;
  }
  return videos.filter((video) => {
    const words = (video.title + " " + video.description)
      .toLowerCase()
      .split(" ");
    return keywords.every((kw) => words.some((w) => w.includes(kw)));
  });
}

export default function Home() {
  const videos = use(fetchVideos());
  const count = videos.length;
  const [searchText, setSearchText] = useState("");
  const foundVideos = filterVideos(videos, searchText);
  return (
    <Layout heading={<div className="fit">{count} Videos</div>}>
      <SearchInput value={searchText} onChange={setSearchText} />
      <div className="video-list">
        {foundVideos.length === 0 && (
          <div className="no-results">No results</div>
        )}
        <div className="videos">
          {foundVideos.map((video) => (
            <Video key={video.id} video={video} />
          ))}
        </div>
      </div>
    </Layout>
  );
}

```

```js src/Icons.js hidden
export function ChevronLeft() {
  return (
    <svg
      className="chevron-left"
      xmlns="http://www.w3.org/2000/svg"
      width="20"
      height="20"
      viewBox="0 0 20 20">
      <g fill="none" fillRule="evenodd" transform="translate(-446 -398)">
        <path
          fill="currentColor"
          fillRule="nonzero"
          d="M95.8838835,240.366117 C95.3957281,239.877961 94.6042719,239.877961 94.1161165,240.366117 C93.6279612,240.854272 93.6279612,241.645728 94.1161165,242.133883 L98.6161165,246.633883 C99.1042719,247.122039 99.8957281,247.122039 100.383883,246.633883 L104.883883,242.133883 C105.372039,241.645728 105.372039,240.854272 104.883883,240.366117 C104.395728,239.877961 103.604272,239.877961 103.116117,240.366117 L99.5,243.982233 L95.8838835,240.366117 Z"
          transform="translate(356.5 164.5)"
        />
        <polygon points="446 418 466 418 466 398 446 398" />
      </g>
    </svg>
  );
}

export function PauseIcon() {
  return (
    <svg
      className="control-icon"
      style={{padding: '4px'}}
      width="100"
      height="100"
      viewBox="0 0 512 512"
      fill="none"
      xmlns="http://www.w3.org/2000/svg">
      <path
        fillRule="evenodd"
        clipRule="evenodd"
        d="M256 0C114.617 0 0 114.615 0 256s114.617 256 256 256 256-114.615 256-256S397.383 0 256 0zm-32 320c0 8.836-7.164 16-16 16h-32c-8.836 0-16-7.164-16-16V192c0-8.836 7.164-16 16-16h32c8.836 0 16 7.164 16 16v128zm128 0c0 8.836-7.164 16-16 16h-32c-8.836 0-16-7.164-16-16V192c0-8.836 7.164-16 16-16h32c8.836 0 16 7.164 16 16v128z"
        fill="currentColor"
      />
    </svg>
  );
}

export function PlayIcon() {
  return (
    <svg
      className="control-icon"
      width="100"
      height="100"
      viewBox="0 0 72 72"
      fill="none"
      xmlns="http://www.w3.org/2000/svg">
      <path
        fillRule="evenodd"
        clipRule="evenodd"
        d="M36 69C54.2254 69 69 54.2254 69 36C69 17.7746 54.2254 3 36 3C17.7746 3 3 17.7746 3 36C3 54.2254 17.7746 69 36 69ZM52.1716 38.6337L28.4366 51.5801C26.4374 52.6705 24 51.2235 24 48.9464V23.0536C24 20.7764 26.4374 19.3295 28.4366 20.4199L52.1716 33.3663C54.2562 34.5034 54.2562 37.4966 52.1716 38.6337Z"
        fill="currentColor"
      />
    </svg>
  );
}
export function Heart({liked, animate}) {
  return (
    <>
      <svg
        className="absolute overflow-visible"
        viewBox="0 0 24 24"
        fill="none"
        xmlns="http://www.w3.org/2000/svg">
        <circle
          className={`circle ${liked ? 'liked' : ''} ${animate ? 'animate' : ''}`}
          cx="12"
          cy="12"
          r="11.5"
          fill="transparent"
          strokeWidth="0"
          stroke="currentColor"
        />
      </svg>

      <svg
        className={`heart ${liked ? 'liked' : ''} ${animate ? 'animate' : ''}`}
        viewBox="0 0 24 24"
        fill="none"
        xmlns="http://www.w3.org/2000/svg">
        {liked ? (
          <path
            d="M12 23a.496.496 0 0 1-.26-.074C7.023 19.973 0 13.743 0 8.68c0-4.12 2.322-6.677 6.058-6.677 2.572 0 5.108 2.387 5.134 2.41l.808.771.808-.771C12.834 4.387 15.367 2 17.935 2 21.678 2 24 4.558 24 8.677c0 5.06-7.022 11.293-11.74 14.246a.496.496 0 0 1-.26.074V23z"
            fill="currentColor"
          />
        ) : (
          <path
            fillRule="evenodd"
            clipRule="evenodd"
            d="m12 5.184-.808-.771-.004-.004C11.065 4.299 8.522 2.003 6 2.003c-3.736 0-6 2.558-6 6.677 0 4.47 5.471 9.848 10 13.079.602.43 1.187.82 1.74 1.167A.497.497 0 0 0 12 23v-.003c.09 0 .182-.026.26-.074C16.977 19.97 24 13.737 24 8.677 24 4.557 21.743 2 18 2c-2.569 0-5.166 2.387-5.192 2.413L12 5.184zm-.002 15.525c2.071-1.388 4.477-3.342 6.427-5.47C20.72 12.733 22 10.401 22 8.677c0-1.708-.466-2.855-1.087-3.55C20.316 4.459 19.392 4 18 4c-.726 0-1.63.364-2.5.9-.67.412-1.148.82-1.266.92-.03.025-.037.031-.019.014l-.013.013L12 7.949 9.832 5.88a10.08 10.08 0 0 0-1.33-.977C7.633 4.367 6.728 4.003 6 4.003c-1.388 0-2.312.459-2.91 1.128C2.466 5.826 2 6.974 2 8.68c0 1.726 1.28 4.058 3.575 6.563 1.948 2.127 4.352 4.078 6.423 5.466z"
            fill="currentColor"
          />
        )}
      </svg>
    </>
  );
}

export function IconSearch(props) {
  return (
    <svg width="1em" height="1em" viewBox="0 0 20 20">
      <path
        d="M14.386 14.386l4.0877 4.0877-4.0877-4.0877c-2.9418 2.9419-7.7115 2.9419-10.6533 0-2.9419-2.9418-2.9419-7.7115 0-10.6533 2.9418-2.9419 7.7115-2.9419 10.6533 0 2.9419 2.9418 2.9419 7.7115 0 10.6533z"
        stroke="currentColor"
        fill="none"
        strokeWidth="2"
        fillRule="evenodd"
        strokeLinecap="round"
        strokeLinejoin="round"></path>
    </svg>
  );
}
```

```js src/Layout.js hidden
import {ViewTransition} from 'react'; import { useIsNavPending } from "./router";

export default function Page({ heading, children }) {
  const isPending = useIsNavPending();

  return (
    <div className="page">
      <div className="top">
        <div className="top-nav">
          {heading}
          {isPending && <span className="loader"></span>}
        </div>
      </div>
      {/* Opt-out of ViewTransition for the content. */}
      {/* Content can define it's own ViewTransition. */}
      <ViewTransition default="none">
        <div className="bottom">
          <div className="content">{children}</div>
        </div>
      </ViewTransition>
    </div>
  );
}
```

```js src/LikeButton.js hidden
import {useState} from 'react';
import {Heart} from './Icons';

// A hack since we don't actually have a backend.
// Unlike local state, this survives videos being filtered.
const likedVideos = new Set();

export default function LikeButton({video}) {
  const [isLiked, setIsLiked] = useState(() => likedVideos.has(video.id));
  const [animate, setAnimate] = useState(false);
  return (
    <button
      className={`like-button ${isLiked && 'liked'}`}
      aria-label={isLiked ? 'Unsave' : 'Save'}
      onClick={() => {
        const nextIsLiked = !isLiked;
        if (nextIsLiked) {
          likedVideos.add(video.id);
        } else {
          likedVideos.delete(video.id);
        }
        setAnimate(true);
        setIsLiked(nextIsLiked);
      }}>
      <Heart liked={isLiked} animate={animate} />
    </button>
  );
}
```

```js src/Videos.js hidden
import { useState } from "react";
import LikeButton from "./LikeButton";
import { useRouter } from "./router";
import { PauseIcon, PlayIcon } from "./Icons";
import { startTransition } from "react";

export function VideoControls() {
  const [isPlaying, setIsPlaying] = useState(false);

  return (
    <span
      className="controls"
      onClick={() =>
        startTransition(() => {
          setIsPlaying((p) => !p);
        })
      }
    >
      {isPlaying ? <PauseIcon /> : <PlayIcon />}
    </span>
  );
}

export function Thumbnail({ video, children }) {
  return (
    <div
      aria-hidden="true"
      tabIndex={-1}
      className={`thumbnail ${video.image}`}
    >
      {children}
    </div>
  );
}

export function Video({ video }) {
  const { navigate } = useRouter();

  return (
    <div className="video">
      <div
        className="link"
        onClick={(e) => {
          e.preventDefault();
          navigate(`/video/${video.id}`);
        }}
      >
        <Thumbnail video={video}></Thumbnail>

        <div className="info">
          <div className="video-title">{video.title}</div>
          <div className="video-description">{video.description}</div>
        </div>
      </div>
      <LikeButton video={video} />
    </div>
  );
}
```


```js src/data.js hidden
const videos = [
  {
    id: '1',
    title: 'First video',
    description: 'Video description',
    image: 'blue',
  },
  {
    id: '2',
    title: 'Second video',
    description: 'Video description',
    image: 'red',
  },
  {
    id: '3',
    title: 'Third video',
    description: 'Video description',
    image: 'green',
  },
  {
    id: '4',
    title: 'Fourth video',
    description: 'Video description',
    image: 'purple',
  },
  {
    id: '5',
    title: 'Fifth video',
    description: 'Video description',
    image: 'yellow',
  },
  {
    id: '6',
    title: 'Sixth video',
    description: 'Video description',
    image: 'gray',
  },
];

let videosCache = new Map();
let videoCache = new Map();
let videoDetailsCache = new Map();
const VIDEO_DELAY = 1;
const VIDEO_DETAILS_DELAY = 1000;
export function fetchVideos() {
  if (videosCache.has(0)) {
    return videosCache.get(0);
  }
  const promise = new Promise((resolve) => {
    setTimeout(() => {
      resolve(videos);
    }, VIDEO_DELAY);
  });
  videosCache.set(0, promise);
  return promise;
}

export function fetchVideo(id) {
  if (videoCache.has(id)) {
    return videoCache.get(id);
  }
  const promise = new Promise((resolve) => {
    setTimeout(() => {
      resolve(videos.find((video) => video.id === id));
    }, VIDEO_DELAY);
  });
  videoCache.set(id, promise);
  return promise;
}

export function fetchVideoDetails(id) {
  if (videoDetailsCache.has(id)) {
    return videoDetailsCache.get(id);
  }
  const promise = new Promise((resolve) => {
    setTimeout(() => {
      resolve(videos.find((video) => video.id === id));
    }, VIDEO_DETAILS_DELAY);
  });
  videoDetailsCache.set(id, promise);
  return promise;
}
```

```js src/router.js hidden
import {
  useState,
  createContext,
  use,
  useTransition,
  useLayoutEffect,
  useEffect,
} from "react";

const RouterContext = createContext({ url: "/", params: {} });

export function useRouter() {
  return use(RouterContext);
}

export function useIsNavPending() {
  return use(RouterContext).isPending;
}

export function Router({ children }) {
  const [routerState, setRouterState] = useState({
    pendingNav: () => {},
    url: document.location.pathname,
  });
  const [isPending, startTransition] = useTransition();

  function go(url) {
    setRouterState({
      url,
      pendingNav() {
        window.history.pushState({}, "", url);
      },
    });
  }
  function navigate(url) {
    // Update router state in transition.
    startTransition(() => {
      go(url);
    });
  }

  function navigateBack(url) {
    // Update router state in transition.
    startTransition(() => {
      go(url);
    });
  }

  useEffect(() => {
    function handlePopState() {
      // This should not animate because restoration has to be synchronous.
      // Even though it's a transition.
      startTransition(() => {
        setRouterState({
          url: document.location.pathname + document.location.search,
          pendingNav() {
            // Noop. URL has already updated.
          },
        });
      });
    }
    window.addEventListener("popstate", handlePopState);
    return () => {
      window.removeEventListener("popstate", handlePopState);
    };
  }, []);
  const pendingNav = routerState.pendingNav;
  useLayoutEffect(() => {
    pendingNav();
  }, [pendingNav]);

  return (
    <RouterContext
      value={{
        url: routerState.url,
        navigate,
        navigateBack,
        isPending,
        params: {},
      }}
    >
      {children}
    </RouterContext>
  );
}
```

```css src/styles.css hidden
@font-face {
  font-family: Optimistic Text;
  src: url(https://react.dev/fonts/Optimistic_Text_W_Rg.woff2) format("woff2");
  font-weight: 400;
  font-style: normal;
  font-display: swap;
}

@font-face {
  font-family: Optimistic Text;
  src: url(https://react.dev/fonts/Optimistic_Text_W_Md.woff2) format("woff2");
  font-weight: 500;
  font-style: normal;
  font-display: swap;
}

@font-face {
  font-family: Optimistic Text;
  src: url(https://react.dev/fonts/Optimistic_Text_W_Bd.woff2) format("woff2");
  font-weight: 600;
  font-style: normal;
  font-display: swap;
}

@font-face {
  font-family: Optimistic Text;
  src: url(https://react.dev/fonts/Optimistic_Text_W_Bd.woff2) format("woff2");
  font-weight: 700;
  font-style: normal;
  font-display: swap;
}

* {
  box-sizing: border-box;
}

html {
  background-image: url(https://react.dev/images/meta-gradient-dark.png);
  background-size: 100%;
  background-position: -100%;
  background-color: rgb(64 71 86);
  background-repeat: no-repeat;
  height: 100%;
  width: 100%;
}

body {
  font-family: Optimistic Text, -apple-system, ui-sans-serif, system-ui, sans-serif, Apple Color Emoji, Segoe UI Emoji, Segoe UI Symbol, Noto Color Emoji;
  padding: 10px 0 10px 0;
  margin: 0;
  display: flex;
  justify-content: center;
}

#root {
  flex: 1 1;
  height: auto;
  background-color: #fff;
  border-radius: 10px;
  max-width: 450px;
  min-height: 600px;
  padding-bottom: 10px;
}

h1 {
  margin-top: 0;
  font-size: 22px;
}

h2 {
  margin-top: 0;
  font-size: 20px;
}

h3 {
  margin-top: 0;
  font-size: 18px;
}

h4 {
  margin-top: 0;
  font-size: 16px;
}

h5 {
  margin-top: 0;
  font-size: 14px;
}

h6 {
  margin-top: 0;
  font-size: 12px;
}

code {
  font-size: 1.2em;
}

ul {
  padding-inline-start: 20px;
}

.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  padding: 0;
  margin: -1px;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  white-space: nowrap;
  border-width: 0;
}

.absolute {
  position: absolute;
}

.overflow-visible {
  overflow: visible;
}

.visible {
  overflow: visible;
}

.fit {
  width: fit-content;
}


/* Layout */
.page {
  display: flex;
  flex-direction: column;
  height: 100%;
}

.top-hero {
  height: 200px;
  display: flex;
  justify-content: center;
  align-items: center;
  background-image: conic-gradient(
      from 90deg at -10% 100%,
      #2b303b 0deg,
      #2b303b 90deg,
      #16181d 1turn
  );
}

.bottom {
  flex: 1;
  overflow: auto;
}

.top-nav {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 0;
  padding: 0 12px;
  top: 0;
  width: 100%;
  height: 44px;
  color: #23272f;
  font-weight: 700;
  font-size: 20px;
  z-index: 100;
  cursor: default;
}

.content {
  padding: 0 12px;
  margin-top: 4px;
}


.loader {
  color: #23272f;
  font-size: 3px;
  width: 1em;
  margin-right: 18px;
  height: 1em;
  border-radius: 50%;
  position: relative;
  text-indent: -9999em;
  animation: loading-spinner 1.3s infinite linear;
  animation-delay: 200ms;
  transform: translateZ(0);
}

@keyframes loading-spinner {
  0%,
  100% {
    box-shadow: 0 -3em 0 0.2em,
    2em -2em 0 0em, 3em 0 0 -1em,
    2em 2em 0 -1em, 0 3em 0 -1em,
    -2em 2em 0 -1em, -3em 0 0 -1em,
    -2em -2em 0 0;
  }
  12.5% {
    box-shadow: 0 -3em 0 0, 2em -2em 0 0.2em,
    3em 0 0 0, 2em 2em 0 -1em, 0 3em 0 -1em,
    -2em 2em 0 -1em, -3em 0 0 -1em,
    -2em -2em 0 -1em;
  }
  25% {
    box-shadow: 0 -3em 0 -0.5em,
    2em -2em 0 0, 3em 0 0 0.2em,
    2em 2em 0 0, 0 3em 0 -1em,
    -2em 2em 0 -1em, -3em 0 0 -1em,
    -2em -2em 0 -1em;
  }
  37.5% {
    box-shadow: 0 -3em 0 -1em, 2em -2em 0 -1em,
    3em 0em 0 0, 2em 2em 0 0.2em, 0 3em 0 0em,
    -2em 2em 0 -1em, -3em 0em 0 -1em, -2em -2em 0 -1em;
  }
  50% {
    box-shadow: 0 -3em 0 -1em, 2em -2em 0 -1em,
    3em 0 0 -1em, 2em 2em 0 0em, 0 3em 0 0.2em,
    -2em 2em 0 0, -3em 0em 0 -1em, -2em -2em 0 -1em;
  }
  62.5% {
    box-shadow: 0 -3em 0 -1em, 2em -2em 0 -1em,
    3em 0 0 -1em, 2em 2em 0 -1em, 0 3em 0 0,
    -2em 2em 0 0.2em, -3em 0 0 0, -2em -2em 0 -1em;
  }
  75% {
    box-shadow: 0em -3em 0 -1em, 2em -2em 0 -1em,
    3em 0em 0 -1em, 2em 2em 0 -1em, 0 3em 0 -1em,
    -2em 2em 0 0, -3em 0em 0 0.2em, -2em -2em 0 0;
  }
  87.5% {
    box-shadow: 0em -3em 0 0, 2em -2em 0 -1em,
    3em 0 0 -1em, 2em 2em 0 -1em, 0 3em 0 -1em,
    -2em 2em 0 0, -3em 0em 0 0, -2em -2em 0 0.2em;
  }
}

/* LikeButton */
.like-button {
  outline-offset: 2px;
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
  width: 2.5rem;
  height: 2.5rem;
  cursor: pointer;
  border-radius: 9999px;
  border: none;
  outline: none 2px;
  color: #5e687e;
  background: none;
}

.like-button:focus {
  color: #a6423a;
  background-color: rgba(166, 66, 58, .05);
}

.like-button:active {
  color: #a6423a;
  background-color: rgba(166, 66, 58, .05);
  transform: scaleX(0.95) scaleY(0.95);
}

.like-button:hover {
  background-color: #f6f7f9;
}

.like-button.liked {
  color: #a6423a;
}

/* Icons */
@keyframes circle {
  0% {
    transform: scale(0);
    stroke-width: 16px;
  }

  50% {
    transform: scale(.5);
    stroke-width: 16px;
  }

  to {
    transform: scale(1);
    stroke-width: 0;
  }
}

.circle {
  color: rgba(166, 66, 58, .5);
  transform-origin: center;
  transition-property: all;
  transition-duration: .15s;
  transition-timing-function: cubic-bezier(.4,0,.2,1);
}

.circle.liked.animate {
  animation: circle .3s forwards;
}

.heart {
  width: 1.5rem;
  height: 1.5rem;
}

.heart.liked {
  transform-origin: center;
  transition-property: all;
  transition-duration: .15s;
  transition-timing-function: cubic-bezier(.4, 0, .2, 1);
}

.heart.liked.animate {
  animation: scale .35s ease-in-out forwards;
}

.control-icon {
  color: hsla(0, 0%, 100%, .5);
  filter:  drop-shadow(0 20px 13px rgba(0, 0, 0, .03)) drop-shadow(0 8px 5px rgba(0, 0, 0, .08));
}

.chevron-left {
  margin-top: 2px;
  rotate: 90deg;
}


/* Video */
.thumbnail {
  position: relative;
  aspect-ratio: 16 / 9;
  display: flex;
  overflow: hidden;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  border-radius: 0.5rem;
  outline-offset: 2px;
  width: 8rem;
  vertical-align: middle;
  background-color: #ffffff;
  background-size: cover;
  user-select: none;
}

.thumbnail.blue {
  background-image: conic-gradient(at top right, #c76a15, #087ea4, #2b3491);
}

.thumbnail.red {
  background-image: conic-gradient(at top right, #c76a15, #a6423a, #2b3491);
}

.thumbnail.green {
  background-image: conic-gradient(at top right, #c76a15, #388f7f, #2b3491);
}

.thumbnail.purple {
  background-image: conic-gradient(at top right, #c76a15, #575fb7, #2b3491);
}

.thumbnail.yellow {
  background-image: conic-gradient(at top right, #c76a15, #FABD62, #2b3491);
}

.thumbnail.gray {
  background-image: conic-gradient(at top right, #c76a15, #4E5769, #2b3491);
}

.video {
  display: flex;
  flex-direction: row;
  gap: 0.75rem;
  align-items: center;
}

.video .link {
  display: flex;
  flex-direction: row;
  flex: 1 1 0;
  gap: 0.125rem;
  outline-offset: 4px;
  cursor: pointer;
}

.video .info {
  display: flex;
  flex-direction: column;
  justify-content: center;
  margin-left: 8px;
  gap: 0.125rem;
}

.video .info:hover {
  text-decoration: underline;
}

.video-title {
  font-size: 15px;
  line-height: 1.25;
  font-weight: 700;
  color: #23272f;
}

.video-description {
  color: #5e687e;
  font-size: 13px;
}

/* Details */
.details .thumbnail {
  position: relative;
  aspect-ratio: 16 / 9;
  display: flex;
  overflow: hidden;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  border-radius: 0.5rem;
  outline-offset: 2px;
  width: 100%;
  vertical-align: middle;
  background-color: #ffffff;
  background-size: cover;
  user-select: none;
}

.video-details-title {
  margin-top: 8px;
}

.video-details-speaker {
  display: flex;
  gap: 8px;
  margin-top: 10px
}

.back {
  display: flex;
  align-items: center;
  margin-left: -5px;
  cursor: pointer;
}

.back:hover {
  text-decoration: underline;
}

.info-title {
  font-size: 1.5rem;
  font-weight: 700;
  line-height: 1.25;
  margin: 8px 0 0 0 ;
}

.info-description {
  margin: 8px 0 0 0;
}

.controls {
  cursor: pointer;
}

.fallback {
  background: #f6f7f8 linear-gradient(to right, #e6e6e6 5%, #cccccc 25%, #e6e6e6 35%) no-repeat;
  background-size: 800px 104px;
  display: block;
  line-height: 1.25;
  margin: 8px 0 0 0;
  border-radius: 5px;
  overflow: hidden;

  animation: 1s linear 1s infinite shimmer;
  animation-delay: 300ms;
  animation-duration: 1s;
  animation-fill-mode: forwards;
  animation-iteration-count: infinite;
  animation-name: shimmer;
  animation-timing-function: linear;
}


.fallback.title {
  width: 130px;
  height: 30px;

}

.fallback.description {
  width: 150px;
  height: 21px;
}

@keyframes shimmer {
  0% {
    background-position: -468px 0;
  }

  100% {
    background-position: 468px 0;
  }
}

.search {
  margin-bottom: 10px;
}
.search-input {
  width: 100%;
  position: relative;
}

.search-icon {
  position: absolute;
  top: 0;
  bottom: 0;
  inset-inline-start: 0;
  display: flex;
  align-items: center;
  padding-inline-start: 1rem;
  pointer-events: none;
  color: #99a1b3;
}

.search-input input {
  display: flex;
  padding-inline-start: 2.75rem;
  padding-top: 10px;
  padding-bottom: 10px;
  width: 100%;
  text-align: start;
  background-color: rgb(235 236 240);
  outline: 2px solid transparent;
  cursor: pointer;
  border: none;
  align-items: center;
  color: rgb(35 39 47);
  border-radius: 9999px;
  vertical-align: middle;
  font-size: 15px;
}

.search-input input:hover, .search-input input:active {
  background-color: rgb(235 236 240/ 0.8);
  color: rgb(35 39 47/ 0.8);
}

/* Home */
.video-list {
  position: relative;
}

.video-list .videos {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  overflow-y: auto;
  height: 100%;
}
```


```css src/animations.css
/* Define .slow-fade using view transition classes */
::view-transition-old(.slow-fade) {
    animation-duration: 500ms;
}

::view-transition-new(.slow-fade) {
    animation-duration: 500ms;
}
```

```js src/index.js hidden
import React, {StrictMode} from 'react';
import {createRoot} from 'react-dom/client';
import './styles.css';
import './animations.css';

import App from './App';
import {Router} from './router';

const root = createRoot(document.getElementById('root'));
root.render(
  <StrictMode>
    <Router>
      <App />
    </Router>
  </StrictMode>
);
```

```json package.json hidden
{
  "dependencies": {
    "react": "canary",
    "react-dom": "canary",
    "react-scripts": "latest"
  },
  "scripts": {
    "start": "react-scripts start",
    "build": "react-scripts build",
    "test": "react-scripts test --env=jsdom",
    "eject": "react-scripts eject"
  }
}
```

</Sandpack>

有关样式化 `<ViewTransition>` 的完整指南，请参阅[样式化视图过渡](/reference/react/ViewTransition#styling-view-transitions)。

### 共享元素过渡 {/*shared-element-transitions*/}

当两个页面包含相同的元素时，你通常希望将其从一个页面动画到下一个页面。

要做到这一点，你可以为 `<ViewTransition>` 添加一个唯一的 `name`：

```js
<ViewTransition name={`video-${video.id}`}>
  <Thumbnail video={video} />
</ViewTransition>
```

现在视频缩略图在两个页面之间有动画效果：

<Sandpack>

```js src/App.js
import { ViewTransition } from "react";
import Details from "./Details";
import Home from "./Home";
import { useRouter } from "./router";

export default function App() {
  const { url } = useRouter();

  // Keeping our default slow-fade.
  // This allows the content not in the shared
  // element transition to cross-fade.
  return (
    <ViewTransition default="slow-fade">
      {url === "/" ? <Home /> : <Details />}
    </ViewTransition>
  );
}
```

```js src/Details.js hidden
import { fetchVideo, fetchVideoDetails } from "./data";
import { Thumbnail, VideoControls } from "./Videos";
import { useRouter } from "./router";
import Layout from "./Layout";
import { use, Suspense } from "react";
import { ChevronLeft } from "./Icons";

function VideoInfo({ id }) {
  const details = use(fetchVideoDetails(id));
  return (
    <>
      <p className="info-title">{details.title}</p>
      <p className="info-description">{details.description}</p>
    </>
  );
}

function VideoInfoFallback() {
  return (
    <>
      <div className="fallback title"></div>
      <div className="fallback description"></div>
    </>
  );
}

export default function Details() {
  const { url, navigateBack } = useRouter();
  const videoId = url.split("/").pop();
  const video = use(fetchVideo(videoId));

  return (
    <Layout
      heading={
        <div
          className="fit back"
          onClick={() => {
            navigateBack("/");
          }}
        >
          <ChevronLeft /> Back
        </div>
      }
    >
      <div className="details">
        <Thumbnail video={video} large>
          <VideoControls />
        </Thumbnail>
        <Suspense fallback={<VideoInfoFallback />}>
          <VideoInfo id={video.id} />
        </Suspense>
      </div>
    </Layout>
  );
}

```

```js src/Home.js hidden
import { Video } from "./Videos";
import Layout from "./Layout";
import { fetchVideos } from "./data";
import { useId, useState, use } from "react";
import { IconSearch } from "./Icons";

function SearchInput({ value, onChange }) {
  const id = useId();
  return (
    <form className="search" onSubmit={(e) => e.preventDefault()}>
      <label htmlFor={id} className="sr-only">
        Search
      </label>
      <div className="search-input">
        <div className="search-icon">
          <IconSearch />
        </div>
        <input
          type="text"
          id={id}
          placeholder="Search"
          value={value}
          onChange={(e) => onChange(e.target.value)}
        />
      </div>
    </form>
  );
}

function filterVideos(videos, query) {
  const keywords = query
    .toLowerCase()
    .split(" ")
    .filter((s) => s !== "");
  if (keywords.length === 0) {
    return videos;
  }
  return videos.filter((video) => {
    const words = (video.title + " " + video.description)
      .toLowerCase()
      .split(" ");
    return keywords.every((kw) => words.some((w) => w.includes(kw)));
  });
}

export default function Home() {
  const videos = use(fetchVideos());
  const count = videos.length;
  const [searchText, setSearchText] = useState("");
  const foundVideos = filterVideos(videos, searchText);
  return (
    <Layout heading={<div className="fit">{count} Videos</div>}>
      <SearchInput value={searchText} onChange={setSearchText} />
      <div className="video-list">
        {foundVideos.length === 0 && (
          <div className="no-results">No results</div>
        )}
        <div className="videos">
          {foundVideos.map((video) => (
            <Video key={video.id} video={video} />
          ))}
        </div>
      </div>
    </Layout>
  );
}

```

```js src/Icons.js hidden
export function ChevronLeft() {
  return (
    <svg
      className="chevron-left"
      xmlns="http://www.w3.org/2000/svg"
      width="20"
      height="20"
      viewBox="0 0 20 20">
      <g fill="none" fillRule="evenodd" transform="translate(-446 -398)">
        <path
          fill="currentColor"
          fillRule="nonzero"
          d="M95.8838835,240.366117 C95.3957281,239.877961 94.6042719,239.877961 94.1161165,240.366117 C93.6279612,240.854272 93.6279612,241.645728 94.1161165,242.133883 L98.6161165,246.633883 C99.1042719,247.122039 99.8957281,247.122039 100.383883,246.633883 L104.883883,242.133883 C105.372039,241.645728 105.372039,240.854272 104.883883,240.366117 C104.395728,239.877961 103.604272,239.877961 103.116117,240.366117 L99.5,243.982233 L95.8838835,240.366117 Z"
          transform="translate(356.5 164.5)"
        />
        <polygon points="446 418 466 418 466 398 446 398" />
      </g>
    </svg>
  );
}

export function PauseIcon() {
  return (
    <svg
      className="control-icon"
      style={{padding: '4px'}}
      width="100"
      height="100"
      viewBox="0 0 512 512"
      fill="none"
      xmlns="http://www.w3.org/2000/svg">
      <path
        fillRule="evenodd"
        clipRule="evenodd"
        d="M256 0C114.617 0 0 114.615 0 256s114.617 256 256 256 256-114.615 256-256S397.383 0 256 0zm-32 320c0 8.836-7.164 16-16 16h-32c-8.836 0-16-7.164-16-16V192c0-8.836 7.164-16 16-16h32c8.836 0 16 7.164 16 16v128zm128 0c0 8.836-7.164 16-16 16h-32c-8.836 0-16-7.164-16-16V192c0-8.836 7.164-16 16-16h32c8.836 0 16 7.164 16 16v128z"
        fill="currentColor"
      />
    </svg>
  );
}

export function PlayIcon() {
  return (
    <svg
      className="control-icon"
      width="100"
      height="100"
      viewBox="0 0 72 72"
      fill="none"
      xmlns="http://www.w3.org/2000/svg">
      <path
        fillRule="evenodd"
        clipRule="evenodd"
        d="M36 69C54.2254 69 69 54.2254 69 36C69 17.7746 54.2254 3 36 3C17.7746 3 3 17.7746 3 36C3 54.2254 17.7746 69 36 69ZM52.1716 38.6337L28.4366 51.5801C26.4374 52.6705 24 51.2235 24 48.9464V23.0536C24 20.7764 26.4374 19.3295 28.4366 20.4199L52.1716 33.3663C54.2562 34.5034 54.2562 37.4966 52.1716 38.6337Z"
        fill="currentColor"
      />
    </svg>
  );
}
export function Heart({liked, animate}) {
  return (
    <>
      <svg
        className="absolute overflow-visible"
        viewBox="0 0 24 24"
        fill="none"
        xmlns="http://www.w3.org/2000/svg">
        <circle
          className={`circle ${liked ? 'liked' : ''} ${animate ? 'animate' : ''}`}
          cx="12"
          cy="12"
          r="11.5"
          fill="transparent"
          strokeWidth="0"
          stroke="currentColor"
        />
      </svg>

      <svg
        className={`heart ${liked ? 'liked' : ''} ${animate ? 'animate' : ''}`}
        viewBox="0 0 24 24"
        fill="none"
        xmlns="http://www.w3.org/2000/svg">
        {liked ? (
          <path
            d="M12 23a.496.496 0 0 1-.26-.074C7.023 19.973 0 13.743 0 8.68c0-4.12 2.322-6.677 6.058-6.677 2.572 0 5.108 2.387 5.134 2.41l.808.771.808-.771C12.834 4.387 15.367 2 17.935 2 21.678 2 24 4.558 24 8.677c0 5.06-7.022 11.293-11.74 14.246a.496.496 0 0 1-.26.074V23z"
            fill="currentColor"
          />
        ) : (
          <path
            fillRule="evenodd"
            clipRule="evenodd"
            d="m12 5.184-.808-.771-.004-.004C11.065 4.299 8.522 2.003 6 2.003c-3.736 0-6 2.558-6 6.677 0 4.47 5.471 9.848 10 13.079.602.43 1.187.82 1.74 1.167A.497.497 0 0 0 12 23v-.003c.09 0 .182-.026.26-.074C16.977 19.97 24 13.737 24 8.677 24 4.557 21.743 2 18 2c-2.569 0-5.166 2.387-5.192 2.413L12 5.184zm-.002 15.525c2.071-1.388 4.477-3.342 6.427-5.47C20.72 12.733 22 10.401 22 8.677c0-1.708-.466-2.855-1.087-3.55C20.316 4.459 19.392 4 18 4c-.726 0-1.63.364-2.5.9-.67.412-1.148.82-1.266.92-.03.025-.037.031-.019.014l-.013.013L12 7.949 9.832 5.88a10.08 10.08 0 0 0-1.33-.977C7.633 4.367 6.728 4.003 6 4.003c-1.388 0-2.312.459-2.91 1.128C2.466 5.826 2 6.974 2 8.68c0 1.726 1.28 4.058 3.575 6.563 1.948 2.127 4.352 4.078 6.423 5.466z"
            fill="currentColor"
          />
        )}
      </svg>
    </>
  );
}

export function IconSearch(props) {
  return (
    <svg width="1em" height="1em" viewBox="0 0 20 20">
      <path
        d="M14.386 14.386l4.0877 4.0877-4.0877-4.0877c-2.9418 2.9419-7.7115 2.9419-10.6533 0-2.9419-2.9418-2.9419-7.7115 0-10.6533 2.9418-2.9419 7.7115-2.9419 10.6533 0 2.9419 2.9418 2.9419 7.7115 0 10.6533z"
        stroke="currentColor"
        fill="none"
        strokeWidth="2"
        fillRule="evenodd"
        strokeLinecap="round"
        strokeLinejoin="round"></path>
    </svg>
  );
}
```

```js src/Layout.js hidden
import {ViewTransition} from 'react'; import { useIsNavPending } from "./router";

export default function Page({ heading, children }) {
  const isPending = useIsNavPending();

  return (
    <div className="page">
      <div className="top">
        <div className="top-nav">
          {heading}
          {isPending && <span className="loader"></span>}
        </div>
      </div>
      {/* Opt-out of ViewTransition for the content. */}
      {/* Content can define it's own ViewTransition. */}
      <ViewTransition default="none">
        <div className="bottom">
          <div className="content">{children}</div>
        </div>
      </ViewTransition>
    </div>
  );
}
```

```js src/LikeButton.js hidden
import {useState} from 'react';
import {Heart} from './Icons';

// A hack since we don't actually have a backend.
// Unlike local state, this survives videos being filtered.
const likedVideos = new Set();

export default function LikeButton({video}) {
  const [isLiked, setIsLiked] = useState(() => likedVideos.has(video.id));
  const [animate, setAnimate] = useState(false);
  return (
    <button
      className={`like-button ${isLiked && 'liked'}`}
      aria-label={isLiked ? 'Unsave' : 'Save'}
      onClick={() => {
        const nextIsLiked = !isLiked;
        if (nextIsLiked) {
          likedVideos.add(video.id);
        } else {
          likedVideos.delete(video.id);
        }
        setAnimate(true);
        setIsLiked(nextIsLiked);
      }}>
      <Heart liked={isLiked} animate={animate} />
    </button>
  );
}
```

```js src/Videos.js active
import { useState, ViewTransition } from "react"; import LikeButton from "./LikeButton"; import { useRouter } from "./router"; import { PauseIcon, PlayIcon } from "./Icons"; import { startTransition } from "react";

export function Thumbnail({ video, children }) {
  // Add a name to animate with a shared element transition.
  // This uses the default animation, no additional css needed.
  return (
    <ViewTransition name={`video-${video.id}`}>
      <div
        aria-hidden="true"
        tabIndex={-1}
        className={`thumbnail ${video.image}`}
      >
        {children}
      </div>
    </ViewTransition>
  );
}

export function VideoControls() {
  const [isPlaying, setIsPlaying] = useState(false);

  return (
    <span
      className="controls"
      onClick={() =>
        startTransition(() => {
          setIsPlaying((p) => !p);
        })
      }
    >
      {isPlaying ? <PauseIcon /> : <PlayIcon />}
    </span>
  );
}

export function Video({ video }) {
  const { navigate } = useRouter();

  return (
    <div className="video">
      <div
        className="link"
        onClick={(e) => {
          e.preventDefault();
          navigate(`/video/${video.id}`);
        }}
      >
        <Thumbnail video={video}></Thumbnail>

        <div className="info">
          <div className="video-title">{video.title}</div>
          <div className="video-description">{video.description}</div>
        </div>
      </div>
      <LikeButton video={video} />
    </div>
  );
}
```


```js src/data.js hidden
const videos = [
  {
    id: '1',
    title: 'First video',
    description: 'Video description',
    image: 'blue',
  },
  {
    id: '2',
    title: 'Second video',
    description: 'Video description',
    image: 'red',
  },
  {
    id: '3',
    title: 'Third video',
    description: 'Video description',
    image: 'green',
  },
  {
    id: '4',
    title: 'Fourth video',
    description: 'Video description',
    image: 'purple',
  },
  {
    id: '5',
    title: 'Fifth video',
    description: 'Video description',
    image: 'yellow',
  },
  {
    id: '6',
    title: 'Sixth video',
    description: 'Video description',
    image: 'gray',
  },
];

let videosCache = new Map();
let videoCache = new Map();
let videoDetailsCache = new Map();
const VIDEO_DELAY = 1;
const VIDEO_DETAILS_DELAY = 1000;
export function fetchVideos() {
  if (videosCache.has(0)) {
    return videosCache.get(0);
  }
  const promise = new Promise((resolve) => {
    setTimeout(() => {
      resolve(videos);
    }, VIDEO_DELAY);
  });
  videosCache.set(0, promise);
  return promise;
}

export function fetchVideo(id) {
  if (videoCache.has(id)) {
    return videoCache.get(id);
  }
  const promise = new Promise((resolve) => {
    setTimeout(() => {
      resolve(videos.find((video) => video.id === id));
    }, VIDEO_DELAY);
  });
  videoCache.set(id, promise);
  return promise;
}

export function fetchVideoDetails(id) {
  if (videoDetailsCache.has(id)) {
    return videoDetailsCache.get(id);
  }
  const promise = new Promise((resolve) => {
    setTimeout(() => {
      resolve(videos.find((video) => video.id === id));
    }, VIDEO_DETAILS_DELAY);
  });
  videoDetailsCache.set(id, promise);
  return promise;
}
```

```js src/router.js hidden
import {
  useState,
  createContext,
  use,
  useTransition,
  useLayoutEffect,
  useEffect,
} from "react";

const RouterContext = createContext({ url: "/", params: {} });

export function useRouter() {
  return use(RouterContext);
}

export function useIsNavPending() {
  return use(RouterContext).isPending;
}

export function Router({ children }) {
  const [routerState, setRouterState] = useState({
    pendingNav: () => {},
    url: document.location.pathname,
  });
  const [isPending, startTransition] = useTransition();

  function go(url) {
    setRouterState({
      url,
      pendingNav() {
        window.history.pushState({}, "", url);
      },
    });
  }
  function navigate(url) {
    // Update router state in transition.
    startTransition(() => {
      go(url);
    });
  }

  function navigateBack(url) {
    // Update router state in transition.
    startTransition(() => {
      go(url);
    });
  }

  useEffect(() => {
    function handlePopState() {
      // This should not animate because restoration has to be synchronous.
      // Even though it's a transition.
      startTransition(() => {
        setRouterState({
          url: document.location.pathname + document.location.search,
          pendingNav() {
            // Noop. URL has already updated.
          },
        });
      });
    }
    window.addEventListener("popstate", handlePopState);
    return () => {
      window.removeEventListener("popstate", handlePopState);
    };
  }, []);
  const pendingNav = routerState.pendingNav;
  useLayoutEffect(() => {
    pendingNav();
  }, [pendingNav]);

  return (
    <RouterContext
      value={{
        url: routerState.url,
        navigate,
        navigateBack,
        isPending,
        params: {},
      }}
    >
      {children}
    </RouterContext>
  );
}
```

```css src/styles.css hidden
@font-face {
  font-family: Optimistic Text;
  src: url(https://react.dev/fonts/Optimistic_Text_W_Rg.woff2) format("woff2");
  font-weight: 400;
  font-style: normal;
  font-display: swap;
}

@font-face {
  font-family: Optimistic Text;
  src: url(https://react.dev/fonts/Optimistic_Text_W_Md.woff2) format("woff2");
  font-weight: 500;
  font-style: normal;
  font-display: swap;
}

@font-face {
  font-family: Optimistic Text;
  src: url(https://react.dev/fonts/Optimistic_Text_W_Bd.woff2) format("woff2");
  font-weight: 600;
  font-style: normal;
  font-display: swap;
}

@font-face {
  font-family: Optimistic Text;
  src: url(https://react.dev/fonts/Optimistic_Text_W_Bd.woff2) format("woff2");
  font-weight: 700;
  font-style: normal;
  font-display: swap;
}

* {
  box-sizing: border-box;
}

html {
  background-image: url(https://react.dev/images/meta-gradient-dark.png);
  background-size: 100%;
  background-position: -100%;
  background-color: rgb(64 71 86);
  background-repeat: no-repeat;
  height: 100%;
  width: 100%;
}

body {
  font-family: Optimistic Text, -apple-system, ui-sans-serif, system-ui, sans-serif, Apple Color Emoji, Segoe UI Emoji, Segoe UI Symbol, Noto Color Emoji;
  padding: 10px 0 10px 0;
  margin: 0;
  display: flex;
  justify-content: center;
}

#root {
  flex: 1 1;
  height: auto;
  background-color: #fff;
  border-radius: 10px;
  max-width: 450px;
  min-height: 600px;
  padding-bottom: 10px;
}

h1 {
  margin-top: 0;
  font-size: 22px;
}

h2 {
  margin-top: 0;
  font-size: 20px;
}

h3 {
  margin-top: 0;
  font-size: 18px;
}

h4 {
  margin-top: 0;
  font-size: 16px;
}

h5 {
  margin-top: 0;
  font-size: 14px;
}

h6 {
  margin-top: 0;
  font-size: 12px;
}

code {
  font-size: 1.2em;
}

ul {
  padding-inline-start: 20px;
}

.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  padding: 0;
  margin: -1px;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  white-space: nowrap;
  border-width: 0;
}

.absolute {
  position: absolute;
}

.overflow-visible {
  overflow: visible;
}

.visible {
  overflow: visible;
}

.fit {
  width: fit-content;
}


/* Layout */
.page {
  display: flex;
  flex-direction: column;
  height: 100%;
}

.top-hero {
  height: 200px;
  display: flex;
  justify-content: center;
  align-items: center;
  background-image: conic-gradient(
      from 90deg at -10% 100%,
      #2b303b 0deg,
      #2b303b 90deg,
      #16181d 1turn
  );
}

.bottom {
  flex: 1;
  overflow: auto;
}

.top-nav {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 0;
  padding: 0 12px;
  top: 0;
  width: 100%;
  height: 44px;
  color: #23272f;
  font-weight: 700;
  font-size: 20px;
  z-index: 100;
  cursor: default;
}

.content {
  padding: 0 12px;
  margin-top: 4px;
}


.loader {
  color: #23272f;
  font-size: 3px;
  width: 1em;
  margin-right: 18px;
  height: 1em;
  border-radius: 50%;
  position: relative;
  text-indent: -9999em;
  animation: loading-spinner 1.3s infinite linear;
  animation-delay: 200ms;
  transform: translateZ(0);
}

@keyframes loading-spinner {
  0%,
  100% {
    box-shadow: 0 -3em 0 0.2em,
    2em -2em 0 0em, 3em 0 0 -1em,
    2em 2em 0 -1em, 0 3em 0 -1em,
    -2em 2em 0 -1em, -3em 0 0 -1em,
    -2em -2em 0 0;
  }
  12.5% {
    box-shadow: 0 -3em 0 0, 2em -2em 0 0.2em,
    3em 0 0 0, 2em 2em 0 -1em, 0 3em 0 -1em,
    -2em 2em 0 -1em, -3em 0 0 -1em,
    -2em -2em 0 -1em;
  }
  25% {
    box-shadow: 0 -3em 0 -0.5em,
    2em -2em 0 0, 3em 0 0 0.2em,
    2em 2em 0 0, 0 3em 0 -1em,
    -2em 2em 0 -1em, -3em 0 0 -1em,
    -2em -2em 0 -1em;
  }
  37.5% {
    box-shadow: 0 -3em 0 -1em, 2em -2em 0 -1em,
    3em 0em 0 0, 2em 2em 0 0.2em, 0 3em 0 0em,
    -2em 2em 0 -1em, -3em 0em 0 -1em, -2em -2em 0 -1em;
  }
  50% {
    box-shadow: 0 -3em 0 -1em, 2em -2em 0 -1em,
    3em 0 0 -1em, 2em 2em 0 0em, 0 3em 0 0.2em,
    -2em 2em 0 0, -3em 0em 0 -1em, -2em -2em 0 -1em;
  }
  62.5% {
    box-shadow: 0 -3em 0 -1em, 2em -2em 0 -1em,
    3em 0 0 -1em, 2em 2em 0 -1em, 0 3em 0 0,
    -2em 2em 0 0.2em, -3em 0 0 0, -2em -2em 0 -1em;
  }
  75% {
    box-shadow: 0em -3em 0 -1em, 2em -2em 0 -1em,
    3em 0em 0 -1em, 2em 2em 0 -1em, 0 3em 0 -1em,
    -2em 2em 0 0, -3em 0em 0 0.2em, -2em -2em 0 0;
  }
  87.5% {
    box-shadow: 0em -3em 0 0, 2em -2em 0 -1em,
    3em 0 0 -1em, 2em 2em 0 -1em, 0 3em 0 -1em,
    -2em 2em 0 0, -3em 0em 0 0, -2em -2em 0 0.2em;
  }
}

/* LikeButton */
.like-button {
  outline-offset: 2px;
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
  width: 2.5rem;
  height: 2.5rem;
  cursor: pointer;
  border-radius: 9999px;
  border: none;
  outline: none 2px;
  color: #5e687e;
  background: none;
}

.like-button:focus {
  color: #a6423a;
  background-color: rgba(166, 66, 58, .05);
}

.like-button:active {
  color: #a6423a;
  background-color: rgba(166, 66, 58, .05);
  transform: scaleX(0.95) scaleY(0.95);
}

.like-button:hover {
  background-color: #f6f7f9;
}

.like-button.liked {
  color: #a6423a;
}

/* Icons */
@keyframes circle {
  0% {
    transform: scale(0);
    stroke-width: 16px;
  }

  50% {
    transform: scale(.5);
    stroke-width: 16px;
  }

  to {
    transform: scale(1);
    stroke-width: 0;
  }
}

.circle {
  color: rgba(166, 66, 58, .5);
  transform-origin: center;
  transition-property: all;
  transition-duration: .15s;
  transition-timing-function: cubic-bezier(.4,0,.2,1);
}

.circle.liked.animate {
  animation: circle .3s forwards;
}

.heart {
  width: 1.5rem;
  height: 1.5rem;
}

.heart.liked {
  transform-origin: center;
  transition-property: all;
  transition-duration: .15s;
  transition-timing-function: cubic-bezier(.4, 0, .2, 1);
}

.heart.liked.animate {
  animation: scale .35s ease-in-out forwards;
}

.control-icon {
  color: hsla(0, 0%, 100%, .5);
  filter:  drop-shadow(0 20px 13px rgba(0, 0, 0, .03)) drop-shadow(0 8px 5px rgba(0, 0, 0, .08));
}

.chevron-left {
  margin-top: 2px;
  rotate: 90deg;
}


/* Video */
.thumbnail {
  position: relative;
  aspect-ratio: 16 / 9;
  display: flex;
  overflow: hidden;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  border-radius: 0.5rem;
  outline-offset: 2px;
  width: 8rem;
  vertical-align: middle;
  background-color: #ffffff;
  background-size: cover;
  user-select: none;
}

.thumbnail.blue {
  background-image: conic-gradient(at top right, #c76a15, #087ea4, #2b3491);
}

.thumbnail.red {
  background-image: conic-gradient(at top right, #c76a15, #a6423a, #2b3491);
}

.thumbnail.green {
  background-image: conic-gradient(at top right, #c76a15, #388f7f, #2b3491);
}

.thumbnail.purple {
  background-image: conic-gradient(at top right, #c76a15, #575fb7, #2b3491);
}

.thumbnail.yellow {
  background-image: conic-gradient(at top right, #c76a15, #FABD62, #2b3491);
}

.thumbnail.gray {
  background-image: conic-gradient(at top right, #c76a15, #4E5769, #2b3491);
}

.video {
  display: flex;
  flex-direction: row;
  gap: 0.75rem;
  align-items: center;
}

.video .link {
  display: flex;
  flex-direction: row;
  flex: 1 1 0;
  gap: 0.125rem;
  outline-offset: 4px;
  cursor: pointer;
}

.video .info {
  display: flex;
  flex-direction: column;
  justify-content: center;
  margin-left: 8px;
  gap: 0.125rem;
}

.video .info:hover {
  text-decoration: underline;
}

.video-title {
  font-size: 15px;
  line-height: 1.25;
  font-weight: 700;
  color: #23272f;
}

.video-description {
  color: #5e687e;
  font-size: 13px;
}

/* Details */
.details .thumbnail {
  position: relative;
  aspect-ratio: 16 / 9;
  display: flex;
  overflow: hidden;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  border-radius: 0.5rem;
  outline-offset: 2px;
  width: 100%;
  vertical-align: middle;
  background-color: #ffffff;
  background-size: cover;
  user-select: none;
}

.video-details-title {
  margin-top: 8px;
}

.video-details-speaker {
  display: flex;
  gap: 8px;
  margin-top: 10px
}

.back {
  display: flex;
  align-items: center;
  margin-left: -5px;
  cursor: pointer;
}

.back:hover {
  text-decoration: underline;
}

.info-title {
  font-size: 1.5rem;
  font-weight: 700;
  line-height: 1.25;
  margin: 8px 0 0 0 ;
}

.info-description {
  margin: 8px 0 0 0;
}

.controls {
  cursor: pointer;
}

.fallback {
  background: #f6f7f8 linear-gradient(to right, #e6e6e6 5%, #cccccc 25%, #e6e6e6 35%) no-repeat;
  background-size: 800px 104px;
  display: block;
  line-height: 1.25;
  margin: 8px 0 0 0;
  border-radius: 5px;
  overflow: hidden;

  animation: 1s linear 1s infinite shimmer;
  animation-delay: 300ms;
  animation-duration: 1s;
  animation-fill-mode: forwards;
  animation-iteration-count: infinite;
  animation-name: shimmer;
  animation-timing-function: linear;
}


.fallback.title {
  width: 130px;
  height: 30px;

}

.fallback.description {
  width: 150px;
  height: 21px;
}

@keyframes shimmer {
  0% {
    background-position: -468px 0;
  }

  100% {
    background-position: 468px 0;
  }
}

.search {
  margin-bottom: 10px;
}
.search-input {
  width: 100%;
  position: relative;
}

.search-icon {
  position: absolute;
  top: 0;
  bottom: 0;
  inset-inline-start: 0;
  display: flex;
  align-items: center;
  padding-inline-start: 1rem;
  pointer-events: none;
  color: #99a1b3;
}

.search-input input {
  display: flex;
  padding-inline-start: 2.75rem;
  padding-top: 10px;
  padding-bottom: 10px;
  width: 100%;
  text-align: start;
  background-color: rgb(235 236 240);
  outline: 2px solid transparent;
  cursor: pointer;
  border: none;
  align-items: center;
  color: rgb(35 39 47);
  border-radius: 9999px;
  vertical-align: middle;
  font-size: 15px;
}

.search-input input:hover, .search-input input:active {
  background-color: rgb(235 236 240/ 0.8);
  color: rgb(35 39 47/ 0.8);
}

/* Home */
.video-list {
  position: relative;
}

.video-list .videos {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  overflow-y: auto;
  height: 100%;
}
```


```css src/animations.css
/* No additional animations needed */









/* Previously defined animations below */





::view-transition-old(.slow-fade) {
    animation-duration: 500ms;
}

::view-transition-new(.slow-fade) {
    animation-duration: 500ms;
}
```

```js src/index.js hidden
import React, {StrictMode} from 'react';
import {createRoot} from 'react-dom/client';
import './styles.css';
import './animations.css';

import App from './App';
import {Router} from './router';

const root = createRoot(document.getElementById('root'));
root.render(
  <StrictMode>
    <Router>
      <App />
    </Router>
  </StrictMode>
);
```

```json package.json hidden
{
  "dependencies": {
    "react": "canary",
    "react-dom": "canary",
    "react-scripts": "latest"
  },
  "scripts": {
    "start": "react-scripts start",
    "build": "react-scripts build",
    "test": "react-scripts test --env=jsdom",
    "eject": "react-scripts eject"
  }
}
```

</Sandpack>

默认情况下，React 会为每个激活过渡的元素自动生成一个唯一的 `name`（参见 [`<ViewTransition>` 如何工作](/reference/react/ViewTransition#how-does-viewtransition-work)）。当 React 看到一个带有 `name` 的 `<ViewTransition>` 被移除，而一个带有相同 `name` 的新 `<ViewTransition>` 被添加时，它将激活共享元素过渡。

有关更多信息，请参阅文档中的[为共享元素添加动画](/reference/react/ViewTransition#animating-a-shared-element)。

### 基于原因的动画 {/*animating-based-on-cause*/}

有时，你可能希望元素根据触发方式以不同方式进行动画。对于这种用例，我们添加了一个名为 `addTransitionType` 的新 API 来指定过渡的原因：

```js {4,11}
function navigate(url) {
  startTransition(() => {
    // 原因为“向前导航”的过渡类型
    addTransitionType('nav-forward');
    go(url);
  });
}
function navigateBack(url) {
  startTransition(() => {
    // 原因为“向后导航”的过渡类型
    addTransitionType('nav-back');
    go(url);
  });
}
```

通过过渡类型，你可以通过 `<ViewTransition>` 的属性提供自定义动画。让我们为“6 个视频”和“返回”的标题添加共享元素过渡：

```js {4,5}
<ViewTransition
  name="nav"
  share={{
    'nav-forward': 'slide-forward',
    'nav-back': 'slide-back',
  }}>
  {heading}
</ViewTransition>
```

Here we pass a `share` prop to define how to animate based on the transition type. When the share transition activates from `nav-forward`, the view transition class `slide-forward` is applied. When it's from `nav-back`, the `slide-back` animation is activated. Let's define these animations in CSS:

```css
::view-transition-old(.slide-forward) {
    /* when sliding forward, the "old" page should slide out to left. */
    animation: ...
}

::view-transition-new(.slide-forward) {
    /* when sliding forward, the "new" page should slide in from right. */
    animation: ...
}

::view-transition-old(.slide-back) {
    /* when sliding back, the "old" page should slide out to right. */
    animation: ...
}

::view-transition-new(.slide-back) {
    /* when sliding back, the "new" page should slide in from left. */
    animation: ...
}
```

Now we can animate the header along with thumbnail based on navigation type:

<Sandpack>

```js src/App.js hidden
import { ViewTransition } from "react";
import Details from "./Details";
import Home from "./Home";
import { useRouter } from "./router";

export default function App() {
  const { url } = useRouter();

  // Keeping our default slow-fade.
  return (
    <ViewTransition default="slow-fade">
      {url === "/" ? <Home /> : <Details />}
    </ViewTransition>
  );
}
```

```js src/Details.js hidden
import { fetchVideo, fetchVideoDetails } from "./data";
import { Thumbnail, VideoControls } from "./Videos";
import { useRouter } from "./router";
import Layout from "./Layout";
import { use, Suspense } from "react";
import { ChevronLeft } from "./Icons";

function VideoInfo({ id }) {
  const details = use(fetchVideoDetails(id));
  return (
    <>
      <p className="info-title">{details.title}</p>
      <p className="info-description">{details.description}</p>
    </>
  );
}

function VideoInfoFallback() {
  return (
    <>
      <div className="fallback title"></div>
      <div className="fallback description"></div>
    </>
  );
}

export default function Details() {
  const { url, navigateBack } = useRouter();
  const videoId = url.split("/").pop();
  const video = use(fetchVideo(videoId));

  return (
    <Layout
      heading={
        <div
          className="fit back"
          onClick={() => {
            navigateBack("/");
          }}
        >
          <ChevronLeft /> Back
        </div>
      }
    >
      <div className="details">
        <Thumbnail video={video} large>
          <VideoControls />
        </Thumbnail>
        <Suspense fallback={<VideoInfoFallback />}>
          <VideoInfo id={video.id} />
        </Suspense>
      </div>
    </Layout>
  );
}

```

```js src/Home.js hidden
import { Video } from "./Videos";
import Layout from "./Layout";
import { fetchVideos } from "./data";
import { useId, useState, use } from "react";
import { IconSearch } from "./Icons";

function SearchInput({ value, onChange }) {
  const id = useId();
  return (
    <form className="search" onSubmit={(e) => e.preventDefault()}>
      <label htmlFor={id} className="sr-only">
        Search
      </label>
      <div className="search-input">
        <div className="search-icon">
          <IconSearch />
        </div>
        <input
          type="text"
          id={id}
          placeholder="Search"
          value={value}
          onChange={(e) => onChange(e.target.value)}
        />
      </div>
    </form>
  );
}

function filterVideos(videos, query) {
  const keywords = query
    .toLowerCase()
    .split(" ")
    .filter((s) => s !== "");
  if (keywords.length === 0) {
    return videos;
  }
  return videos.filter((video) => {
    const words = (video.title + " " + video.description)
      .toLowerCase()
      .split(" ");
    return keywords.every((kw) => words.some((w) => w.includes(kw)));
  });
}

export default function Home() {
  const videos = use(fetchVideos());
  const count = videos.length;
  const [searchText, setSearchText] = useState("");
  const foundVideos = filterVideos(videos, searchText);
  return (
    <Layout heading={<div className="fit">{count} Videos</div>}>
      <SearchInput value={searchText} onChange={setSearchText} />
      <div className="video-list">
        {foundVideos.length === 0 && (
          <div className="no-results">No results</div>
        )}
        <div className="videos">
          {foundVideos.map((video) => (
            <Video key={video.id} video={video} />
          ))}
        </div>
      </div>
    </Layout>
  );
}

```

```js src/Icons.js hidden
export function ChevronLeft() {
  return (
    <svg
      className="chevron-left"
      xmlns="http://www.w3.org/2000/svg"
      width="20"
      height="20"
      viewBox="0 0 20 20">
      <g fill="none" fillRule="evenodd" transform="translate(-446 -398)">
        <path
          fill="currentColor"
          fillRule="nonzero"
          d="M95.8838835,240.366117 C95.3957281,239.877961 94.6042719,239.877961 94.1161165,240.366117 C93.6279612,240.854272 93.6279612,241.645728 94.1161165,242.133883 L98.6161165,246.633883 C99.1042719,247.122039 99.8957281,247.122039 100.383883,246.633883 L104.883883,242.133883 C105.372039,241.645728 105.372039,240.854272 104.883883,240.366117 C104.395728,239.877961 103.604272,239.877961 103.116117,240.366117 L99.5,243.982233 L95.8838835,240.366117 Z"
          transform="translate(356.5 164.5)"
        />
        <polygon points="446 418 466 418 466 398 446 398" />
      </g>
    </svg>
  );
}

export function PauseIcon() {
  return (
    <svg
      className="control-icon"
      style={{padding: '4px'}}
      width="100"
      height="100"
      viewBox="0 0 512 512"
      fill="none"
      xmlns="http://www.w3.org/2000/svg">
      <path
        fillRule="evenodd"
        clipRule="evenodd"
        d="M256 0C114.617 0 0 114.615 0 256s114.617 256 256 256 256-114.615 256-256S397.383 0 256 0zm-32 320c0 8.836-7.164 16-16 16h-32c-8.836 0-16-7.164-16-16V192c0-8.836 7.164-16 16-16h32c8.836 0 16 7.164 16 16v128zm128 0c0 8.836-7.164 16-16 16h-32c-8.836 0-16-7.164-16-16V192c0-8.836 7.164-16 16-16h32c8.836 0 16 7.164 16 16v128z"
        fill="currentColor"
      />
    </svg>
  );
}

export function PlayIcon() {
  return (
    <svg
      className="control-icon"
      width="100"
      height="100"
      viewBox="0 0 72 72"
      fill="none"
      xmlns="http://www.w3.org/2000/svg">
      <path
        fillRule="evenodd"
        clipRule="evenodd"
        d="M36 69C54.2254 69 69 54.2254 69 36C69 17.7746 54.2254 3 36 3C17.7746 3 3 17.7746 3 36C3 54.2254 17.7746 69 36 69ZM52.1716 38.6337L28.4366 51.5801C26.4374 52.6705 24 51.2235 24 48.9464V23.0536C24 20.7764 26.4374 19.3295 28.4366 20.4199L52.1716 33.3663C54.2562 34.5034 54.2562 37.4966 52.1716 38.6337Z"
        fill="currentColor"
      />
    </svg>
  );
}
export function Heart({liked, animate}) {
  return (
    <>
      <svg
        className="absolute overflow-visible"
        viewBox="0 0 24 24"
        fill="none"
        xmlns="http://www.w3.org/2000/svg">
        <circle
          className={`circle ${liked ? 'liked' : ''} ${animate ? 'animate' : ''}`}
          cx="12"
          cy="12"
          r="11.5"
          fill="transparent"
          strokeWidth="0"
          stroke="currentColor"
        />
      </svg>

      <svg
        className={`heart ${liked ? 'liked' : ''} ${animate ? 'animate' : ''}`}
        viewBox="0 0 24 24"
        fill="none"
        xmlns="http://www.w3.org/2000/svg">
        {liked ? (
          <path
            d="M12 23a.496.496 0 0 1-.26-.074C7.023 19.973 0 13.743 0 8.68c0-4.12 2.322-6.677 6.058-6.677 2.572 0 5.108 2.387 5.134 2.41l.808.771.808-.771C12.834 4.387 15.367 2 17.935 2 21.678 2 24 4.558 24 8.677c0 5.06-7.022 11.293-11.74 14.246a.496.496 0 0 1-.26.074V23z"
            fill="currentColor"
          />
        ) : (
          <path
            fillRule="evenodd"
            clipRule="evenodd"
            d="m12 5.184-.808-.771-.004-.004C11.065 4.299 8.522 2.003 6 2.003c-3.736 0-6 2.558-6 6.677 0 4.47 5.471 9.848 10 13.079.602.43 1.187.82 1.74 1.167A.497.497 0 0 0 12 23v-.003c.09 0 .182-.026.26-.074C16.977 19.97 24 13.737 24 8.677 24 4.557 21.743 2 18 2c-2.569 0-5.166 2.387-5.192 2.413L12 5.184zm-.002 15.525c2.071-1.388 4.477-3.342 6.427-5.47C20.72 12.733 22 10.401 22 8.677c0-1.708-.466-2.855-1.087-3.55C20.316 4.459 19.392 4 18 4c-.726 0-1.63.364-2.5.9-.67.412-1.148.82-1.266.92-.03.025-.037.031-.019.014l-.013.013L12 7.949 9.832 5.88a10.08 10.08 0 0 0-1.33-.977C7.633 4.367 6.728 4.003 6 4.003c-1.388 0-2.312.459-2.91 1.128C2.466 5.826 2 6.974 2 8.68c0 1.726 1.28 4.058 3.575 6.563 1.948 2.127 4.352 4.078 6.423 5.466z"
            fill="currentColor"
          />
        )}
      </svg>
    </>
  );
}

export function IconSearch(props) {
  return (
    <svg width="1em" height="1em" viewBox="0 0 20 20">
      <path
        d="M14.386 14.386l4.0877 4.0877-4.0877-4.0877c-2.9418 2.9419-7.7115 2.9419-10.6533 0-2.9419-2.9418-2.9419-7.7115 0-10.6533 2.9418-2.9419 7.7115-2.9419 10.6533 0 2.9419 2.9418 2.9419 7.7115 0 10.6533z"
        stroke="currentColor"
        fill="none"
        strokeWidth="2"
        fillRule="evenodd"
        strokeLinecap="round"
        strokeLinejoin="round"></path>
    </svg>
  );
}
```

```js src/Layout.js active
import {ViewTransition} from 'react'; import { useIsNavPending } from "./router";

export default function Page({ heading, children }) {
  const isPending = useIsNavPending();
  return (
    <div className="page">
      <div className="top">
        <div className="top-nav">
          {/* Custom classes based on transition type. */}
          <ViewTransition
            name="nav"
            share={{
              'nav-forward': 'slide-forward',
              'nav-back': 'slide-back',
            }}>
            {heading}
          </ViewTransition>
          {isPending && <span className="loader"></span>}
        </div>
      </div>
      {/* Opt-out of ViewTransition for the content. */}
      {/* Content can define it's own ViewTransition. */}
      <ViewTransition default="none">
        <div className="bottom">
          <div className="content">{children}</div>
        </div>
      </ViewTransition>
    </div>
  );
}
```

```js src/LikeButton.js hidden
import {useState} from 'react';
import {Heart} from './Icons';

// A hack since we don't actually have a backend.
// Unlike local state, this survives videos being filtered.
const likedVideos = new Set();

export default function LikeButton({video}) {
  const [isLiked, setIsLiked] = useState(() => likedVideos.has(video.id));
  const [animate, setAnimate] = useState(false);
  return (
    <button
      className={`like-button ${isLiked && 'liked'}`}
      aria-label={isLiked ? 'Unsave' : 'Save'}
      onClick={() => {
        const nextIsLiked = !isLiked;
        if (nextIsLiked) {
          likedVideos.add(video.id);
        } else {
          likedVideos.delete(video.id);
        }
        setAnimate(true);
        setIsLiked(nextIsLiked);
      }}>
      <Heart liked={isLiked} animate={animate} />
    </button>
  );
}
```

```js src/Videos.js hidden
import { useState, ViewTransition } from "react";
import LikeButton from "./LikeButton";
import { useRouter } from "./router";
import { PauseIcon, PlayIcon } from "./Icons";
import { startTransition } from "react";

export function Thumbnail({ video, children }) {
  // Add a name to animate with a shared element transition.
  // This uses the default animation, no additional css needed.
  return (
    <ViewTransition name={`video-${video.id}`}>
      <div
        aria-hidden="true"
        tabIndex={-1}
        className={`thumbnail ${video.image}`}
      >
        {children}
      </div>
    </ViewTransition>
  );
}

export function VideoControls() {
  const [isPlaying, setIsPlaying] = useState(false);

  return (
    <span
      className="controls"
      onClick={() =>
        startTransition(() => {
          setIsPlaying((p) => !p);
        })
      }
    >
      {isPlaying ? <PauseIcon /> : <PlayIcon />}
    </span>
  );
}

export function Video({ video }) {
  const { navigate } = useRouter();

  return (
    <div className="video">
      <div
        className="link"
        onClick={(e) => {
          e.preventDefault();
          navigate(`/video/${video.id}`);
        }}
      >
        <Thumbnail video={video}></Thumbnail>

        <div className="info">
          <div className="video-title">{video.title}</div>
          <div className="video-description">{video.description}</div>
        </div>
      </div>
      <LikeButton video={video} />
    </div>
  );
}
```


```js src/data.js hidden
const videos = [
  {
    id: '1',
    title: 'First video',
    description: 'Video description',
    image: 'blue',
  },
  {
    id: '2',
    title: 'Second video',
    description: 'Video description',
    image: 'red',
  },
  {
    id: '3',
    title: 'Third video',
    description: 'Video description',
    image: 'green',
  },
  {
    id: '4',
    title: 'Fourth video',
    description: 'Video description',
    image: 'purple',
  },
  {
    id: '5',
    title: 'Fifth video',
    description: 'Video description',
    image: 'yellow',
  },
  {
    id: '6',
    title: 'Sixth video',
    description: 'Video description',
    image: 'gray',
  },
];

let videosCache = new Map();
let videoCache = new Map();
let videoDetailsCache = new Map();
const VIDEO_DELAY = 1;
const VIDEO_DETAILS_DELAY = 1000;
export function fetchVideos() {
  if (videosCache.has(0)) {
    return videosCache.get(0);
  }
  const promise = new Promise((resolve) => {
    setTimeout(() => {
      resolve(videos);
    }, VIDEO_DELAY);
  });
  videosCache.set(0, promise);
  return promise;
}

export function fetchVideo(id) {
  if (videoCache.has(id)) {
    return videoCache.get(id);
  }
  const promise = new Promise((resolve) => {
    setTimeout(() => {
      resolve(videos.find((video) => video.id === id));
    }, VIDEO_DELAY);
  });
  videoCache.set(id, promise);
  return promise;
}

export function fetchVideoDetails(id) {
  if (videoDetailsCache.has(id)) {
    return videoDetailsCache.get(id);
  }
  const promise = new Promise((resolve) => {
    setTimeout(() => {
      resolve(videos.find((video) => video.id === id));
    }, VIDEO_DETAILS_DELAY);
  });
  videoDetailsCache.set(id, promise);
  return promise;
}
```

```js src/router.js
import {useState, createContext, use, useTransition, useLayoutEffect, useEffect, addTransitionType} from "react";

export function Router({ children }) {
  const [isPending, startTransition] = useTransition();

  function navigate(url) {
    startTransition(() => {
      // 原因为“向前导航”的过渡类型
      addTransitionType('nav-forward');
      go(url);
    });
  }
  function navigateBack(url) {
    startTransition(() => {
      // Transition type for the cause "nav backward"
      addTransitionType('nav-back');
      go(url);
    });
  }


  const [routerState, setRouterState] = useState({pendingNav: () => {}, url: document.location.pathname});

  function go(url) {
    setRouterState({
      url,
      pendingNav() {
        window.history.pushState({}, "", url);
      },
    });
  }

  useEffect(() => {
    function handlePopState() {
      // 因为恢复必须是同步的，所以应该没有动画。
      // Even though it's a transition.
      startTransition(() => {
        setRouterState({
          url: document.location.pathname + document.location.search,
          pendingNav() {
            // Noop. URL has already updated.
          },
        });
      });
    }
    window.addEventListener("popstate", handlePopState);
    return () => {
      window.removeEventListener("popstate", handlePopState);
    };
  }, []);
  const pendingNav = routerState.pendingNav;
  useLayoutEffect(() => {
    pendingNav();
  }, [pendingNav]);

  return (
    <RouterContext
      value={{
        url: routerState.url,
        navigate,
        navigateBack,
        isPending,
        params: {},
      }}
    >
      {children}
    </RouterContext>
  );
}

const RouterContext = createContext({ url: "/", params: {} });

export function useRouter() {
  return use(RouterContext);
}

export function useIsNavPending() {
  return use(RouterContext).isPending;
}

```

```css src/styles.css hidden
@font-face {
  font-family: Optimistic Text;
  src: url(https://react.dev/fonts/Optimistic_Text_W_Rg.woff2) format("woff2");
  font-weight: 400;
  font-style: normal;
  font-display: swap;
}

@font-face {
  font-family: Optimistic Text;
  src: url(https://react.dev/fonts/Optimistic_Text_W_Md.woff2) format("woff2");
  font-weight: 500;
  font-style: normal;
  font-display: swap;
}

@font-face {
  font-family: Optimistic Text;
  src: url(https://react.dev/fonts/Optimistic_Text_W_Bd.woff2) format("woff2");
  font-weight: 600;
  font-style: normal;
  font-display: swap;
}

@font-face {
  font-family: Optimistic Text;
  src: url(https://react.dev/fonts/Optimistic_Text_W_Bd.woff2) format("woff2");
  font-weight: 700;
  font-style: normal;
  font-display: swap;
}

* {
  box-sizing: border-box;
}

html {
  background-image: url(https://react.dev/images/meta-gradient-dark.png);
  background-size: 100%;
  background-position: -100%;
  background-color: rgb(64 71 86);
  background-repeat: no-repeat;
  height: 100%;
  width: 100%;
}

body {
  font-family: Optimistic Text, -apple-system, ui-sans-serif, system-ui, sans-serif, Apple Color Emoji, Segoe UI Emoji, Segoe UI Symbol, Noto Color Emoji;
  padding: 10px 0 10px 0;
  margin: 0;
  display: flex;
  justify-content: center;
}

#root {
  flex: 1 1;
  height: auto;
  background-color: #fff;
  border-radius: 10px;
  max-width: 450px;
  min-height: 600px;
  padding-bottom: 10px;
}

h1 {
  margin-top: 0;
  font-size: 22px;
}

h2 {
  margin-top: 0;
  font-size: 20px;
}

h3 {
  margin-top: 0;
  font-size: 18px;
}

h4 {
  margin-top: 0;
  font-size: 16px;
}

h5 {
  margin-top: 0;
  font-size: 14px;
}

h6 {
  margin-top: 0;
  font-size: 12px;
}

code {
  font-size: 1.2em;
}

ul {
  padding-inline-start: 20px;
}

.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  padding: 0;
  margin: -1px;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  white-space: nowrap;
  border-width: 0;
}

.absolute {
  position: absolute;
}

.overflow-visible {
  overflow: visible;
}

.visible {
  overflow: visible;
}

.fit {
  width: fit-content;
}


/* Layout */
.page {
  display: flex;
  flex-direction: column;
  height: 100%;
}

.top-hero {
  height: 200px;
  display: flex;
  justify-content: center;
  align-items: center;
  background-image: conic-gradient(
      from 90deg at -10% 100%,
      #2b303b 0deg,
      #2b303b 90deg,
      #16181d 1turn
  );
}

.bottom {
  flex: 1;
  overflow: auto;
}

.top-nav {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 0;
  padding: 0 12px;
  top: 0;
  width: 100%;
  height: 44px;
  color: #23272f;
  font-weight: 700;
  font-size: 20px;
  z-index: 100;
  cursor: default;
}

.content {
  padding: 0 12px;
  margin-top: 4px;
}


.loader {
  color: #23272f;
  font-size: 3px;
  width: 1em;
  margin-right: 18px;
  height: 1em;
  border-radius: 50%;
  position: relative;
  text-indent: -9999em;
  animation: loading-spinner 1.3s infinite linear;
  animation-delay: 200ms;
  transform: translateZ(0);
}

@keyframes loading-spinner {
  0%,
  100% {
    box-shadow: 0 -3em 0 0.2em,
    2em -2em 0 0em, 3em 0 0 -1em,
    2em 2em 0 -1em, 0 3em 0 -1em,
    -2em 2em 0 -1em, -3em 0 0 -1em,
    -2em -2em 0 0;
  }
  12.5% {
    box-shadow: 0 -3em 0 0, 2em -2em 0 0.2em,
    3em 0 0 0, 2em 2em 0 -1em, 0 3em 0 -1em,
    -2em 2em 0 -1em, -3em 0 0 -1em,
    -2em -2em 0 -1em;
  }
  25% {
    box-shadow: 0 -3em 0 -0.5em,
    2em -2em 0 0, 3em 0 0 0.2em,
    2em 2em 0 0, 0 3em 0 -1em,
    -2em 2em 0 -1em, -3em 0 0 -1em,
    -2em -2em 0 -1em;
  }
  37.5% {
    box-shadow: 0 -3em 0 -1em, 2em -2em 0 -1em,
    3em 0em 0 0, 2em 2em 0 0.2em, 0 3em 0 0em,
    -2em 2em 0 -1em, -3em 0em 0 -1em, -2em -2em 0 -1em;
  }
  50% {
    box-shadow: 0 -3em 0 -1em, 2em -2em 0 -1em,
    3em 0 0 -1em, 2em 2em 0 0em, 0 3em 0 0.2em,
    -2em 2em 0 0, -3em 0em 0 -1em, -2em -2em 0 -1em;
  }
  62.5% {
    box-shadow: 0 -3em 0 -1em, 2em -2em 0 -1em,
    3em 0 0 -1em, 2em 2em 0 -1em, 0 3em 0 0,
    -2em 2em 0 0.2em, -3em 0 0 0, -2em -2em 0 -1em;
  }
  75% {
    box-shadow: 0em -3em 0 -1em, 2em -2em 0 -1em,
    3em 0em 0 -1em, 2em 2em 0 -1em, 0 3em 0 -1em,
    -2em 2em 0 0, -3em 0em 0 0.2em, -2em -2em 0 0;
  }
  87.5% {
    box-shadow: 0em -3em 0 0, 2em -2em 0 -1em,
    3em 0 0 -1em, 2em 2em 0 -1em, 0 3em 0 -1em,
    -2em 2em 0 0, -3em 0em 0 0, -2em -2em 0 0.2em;
  }
}

/* LikeButton */
.like-button {
  outline-offset: 2px;
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
  width: 2.5rem;
  height: 2.5rem;
  cursor: pointer;
  border-radius: 9999px;
  border: none;
  outline: none 2px;
  color: #5e687e;
  background: none;
}

.like-button:focus {
  color: #a6423a;
  background-color: rgba(166, 66, 58, .05);
}

.like-button:active {
  color: #a6423a;
  background-color: rgba(166, 66, 58, .05);
  transform: scaleX(0.95) scaleY(0.95);
}

.like-button:hover {
  background-color: #f6f7f9;
}

.like-button.liked {
  color: #a6423a;
}

/* Icons */
@keyframes circle {
  0% {
    transform: scale(0);
    stroke-width: 16px;
  }

  50% {
    transform: scale(.5);
    stroke-width: 16px;
  }

  to {
    transform: scale(1);
    stroke-width: 0;
  }
}

.circle {
  color: rgba(166, 66, 58, .5);
  transform-origin: center;
  transition-property: all;
  transition-duration: .15s;
  transition-timing-function: cubic-bezier(.4,0,.2,1);
}

.circle.liked.animate {
  animation: circle .3s forwards;
}

.heart {
  width: 1.5rem;
  height: 1.5rem;
}

.heart.liked {
  transform-origin: center;
  transition-property: all;
  transition-duration: .15s;
  transition-timing-function: cubic-bezier(.4, 0, .2, 1);
}

.heart.liked.animate {
  animation: scale .35s ease-in-out forwards;
}

.control-icon {
  color: hsla(0, 0%, 100%, .5);
  filter:  drop-shadow(0 20px 13px rgba(0, 0, 0, .03)) drop-shadow(0 8px 5px rgba(0, 0, 0, .08));
}

.chevron-left {
  margin-top: 2px;
  rotate: 90deg;
}


/* Video */
.thumbnail {
  position: relative;
  aspect-ratio: 16 / 9;
  display: flex;
  overflow: hidden;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  border-radius: 0.5rem;
  outline-offset: 2px;
  width: 8rem;
  vertical-align: middle;
  background-color: #ffffff;
  background-size: cover;
  user-select: none;
}

.thumbnail.blue {
  background-image: conic-gradient(at top right, #c76a15, #087ea4, #2b3491);
}

.thumbnail.red {
  background-image: conic-gradient(at top right, #c76a15, #a6423a, #2b3491);
}

.thumbnail.green {
  background-image: conic-gradient(at top right, #c76a15, #388f7f, #2b3491);
}

.thumbnail.purple {
  background-image: conic-gradient(at top right, #c76a15, #575fb7, #2b3491);
}

.thumbnail.yellow {
  background-image: conic-gradient(at top right, #c76a15, #FABD62, #2b3491);
}

.thumbnail.gray {
  background-image: conic-gradient(at top right, #c76a15, #4E5769, #2b3491);
}

.video {
  display: flex;
  flex-direction: row;
  gap: 0.75rem;
  align-items: center;
}

.video .link {
  display: flex;
  flex-direction: row;
  flex: 1 1 0;
  gap: 0.125rem;
  outline-offset: 4px;
  cursor: pointer;
}

.video .info {
  display: flex;
  flex-direction: column;
  justify-content: center;
  margin-left: 8px;
  gap: 0.125rem;
}

.video .info:hover {
  text-decoration: underline;
}

.video-title {
  font-size: 15px;
  line-height: 1.25;
  font-weight: 700;
  color: #23272f;
}

.video-description {
  color: #5e687e;
  font-size: 13px;
}

/* Details */
.details .thumbnail {
  position: relative;
  aspect-ratio: 16 / 9;
  display: flex;
  overflow: hidden;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  border-radius: 0.5rem;
  outline-offset: 2px;
  width: 100%;
  vertical-align: middle;
  background-color: #ffffff;
  background-size: cover;
  user-select: none;
}

.video-details-title {
  margin-top: 8px;
}

.video-details-speaker {
  display: flex;
  gap: 8px;
  margin-top: 10px
}

.back {
  display: flex;
  align-items: center;
  margin-left: -5px;
  cursor: pointer;
}

.back:hover {
  text-decoration: underline;
}

.info-title {
  font-size: 1.5rem;
  font-weight: 700;
  line-height: 1.25;
  margin: 8px 0 0 0 ;
}

.info-description {
  margin: 8px 0 0 0;
}

.controls {
  cursor: pointer;
}

.fallback {
  background: #f6f7f8 linear-gradient(to right, #e6e6e6 5%, #cccccc 25%, #e6e6e6 35%) no-repeat;
  background-size: 800px 104px;
  display: block;
  line-height: 1.25;
  margin: 8px 0 0 0;
  border-radius: 5px;
  overflow: hidden;

  animation: 1s linear 1s infinite shimmer;
  animation-delay: 300ms;
  animation-duration: 1s;
  animation-fill-mode: forwards;
  animation-iteration-count: infinite;
  animation-name: shimmer;
  animation-timing-function: linear;
}


.fallback.title {
  width: 130px;
  height: 30px;

}

.fallback.description {
  width: 150px;
  height: 21px;
}

@keyframes shimmer {
  0% {
    background-position: -468px 0;
  }

  100% {
    background-position: 468px 0;
  }
}

.search {
  margin-bottom: 10px;
}
.search-input {
  width: 100%;
  position: relative;
}

.search-icon {
  position: absolute;
  top: 0;
  bottom: 0;
  inset-inline-start: 0;
  display: flex;
  align-items: center;
  padding-inline-start: 1rem;
  pointer-events: none;
  color: #99a1b3;
}

.search-input input {
  display: flex;
  padding-inline-start: 2.75rem;
  padding-top: 10px;
  padding-bottom: 10px;
  width: 100%;
  text-align: start;
  background-color: rgb(235 236 240);
  outline: 2px solid transparent;
  cursor: pointer;
  border: none;
  align-items: center;
  color: rgb(35 39 47);
  border-radius: 9999px;
  vertical-align: middle;
  font-size: 15px;
}

.search-input input:hover, .search-input input:active {
  background-color: rgb(235 236 240/ 0.8);
  color: rgb(35 39 47/ 0.8);
}

/* Home */
.video-list {
  position: relative;
}

.video-list .videos {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  overflow-y: auto;
  height: 100%;
}
```


```css src/animations.css
/* Animations for view transition classed added by transition type */
::view-transition-old(.slide-forward) {
    /* when sliding forward, the "old" page should slide out to left. */
    animation: 150ms cubic-bezier(0.4, 0, 1, 1) both fade-out,
    400ms cubic-bezier(0.4, 0, 0.2, 1) both slide-to-left;
}

::view-transition-new(.slide-forward) {
    /* when sliding forward, the "new" page should slide in from right. */
    animation: 210ms cubic-bezier(0, 0, 0.2, 1) 150ms both fade-in,
    400ms cubic-bezier(0.4, 0, 0.2, 1) both slide-from-right;
}

::view-transition-old(.slide-back) {
    /* when sliding back, the "old" page should slide out to right. */
    animation: 150ms cubic-bezier(0.4, 0, 1, 1) both fade-out,
    400ms cubic-bezier(0.4, 0, 0.2, 1) both slide-to-right;
}

::view-transition-new(.slide-back) {
    /* when sliding back, the "new" page should slide in from left. */
    animation: 210ms cubic-bezier(0, 0, 0.2, 1) 150ms both fade-in,
    400ms cubic-bezier(0.4, 0, 0.2, 1) both slide-from-left;
}

/* New keyframes to support our animations above. */
@keyframes fade-in {
    from {
        opacity: 0;
    }
}

@keyframes fade-out {
    to {
        opacity: 0;
    }
}

@keyframes slide-to-right {
    to {
        transform: translateX(50px);
    }
}

@keyframes slide-from-right {
    from {
        transform: translateX(50px);
    }
    to {
        transform: translateX(0);
    }
}

@keyframes slide-to-left {
    to {
        transform: translateX(-50px);
    }
}

@keyframes slide-from-left {
    from {
        transform: translateX(-50px);
    }
    to {
        transform: translateX(0);
    }
}

/* Previously defined animations. */

/* Default .slow-fade. */
::view-transition-old(.slow-fade) {
    animation-duration: 500ms;
}

::view-transition-new(.slow-fade) {
    animation-duration: 500ms;
}
```

```js src/index.js hidden
import React, {StrictMode} from 'react';
import {createRoot} from 'react-dom/client';
import './styles.css';
import './animations.css';

import App from './App';
import {Router} from './router';

const root = createRoot(document.getElementById('root'));
root.render(
  <StrictMode>
    <Router>
      <App />
    </Router>
  </StrictMode>
);
```

```json package.json hidden
{
  "dependencies": {
    "react": "canary",
    "react-dom": "canary",
    "react-scripts": "latest"
  },
  "scripts": {
    "start": "react-scripts start",
    "build": "react-scripts build",
    "test": "react-scripts test --env=jsdom",
    "eject": "react-scripts eject"
  }
}
```

</Sandpack>

### 为 Suspense 边界添加动画 {/*animating-suspense-boundaries*/}

Suspense 也会激活视图过渡。

要为后备方案到内容的过渡添加动画，我们可以用 `<ViewTransition>` 包装 `Suspense`：

```js
<ViewTransition>
  <Suspense fallback={<VideoInfoFallback />}>
    <VideoInfo />
  </Suspense>
</ViewTransition>
```

通过添加这个，后备方案将交叉淡入淡出到内容。点击一个视频，看看视频信息如何动画显示：

<Sandpack>

```js src/App.js hidden
import { ViewTransition } from "react";
import Details from "./Details";
import Home from "./Home";
import { useRouter } from "./router";

export default function App() {
  const { url } = useRouter();

  // Default slow-fade animation.
  return (
    <ViewTransition default="slow-fade">
      {url === "/" ? <Home /> : <Details />}
    </ViewTransition>
  );
}
```

```js src/Details.js active
import { use, Suspense, ViewTransition } from "react"; import { fetchVideo, fetchVideoDetails } from "./data"; import { Thumbnail, VideoControls } from "./Videos"; import { useRouter } from "./router"; import Layout from "./Layout"; import { ChevronLeft } from "./Icons";

function VideoDetails({ id }) {
  // Cross-fade the fallback to content.
  return (
    <ViewTransition default="slow-fade">
      <Suspense fallback={<VideoInfoFallback />}>
          <VideoInfo id={id} />
      </Suspense>
    </ViewTransition>
  );
}

function VideoInfoFallback() {
  return (
    <div>
      <div className="fit fallback title"></div>
      <div className="fit fallback description"></div>
    </div>
  );
}

export default function Details() {
  const { url, navigateBack } = useRouter();
  const videoId = url.split("/").pop();
  const video = use(fetchVideo(videoId));

  return (
    <Layout
      heading={
        <div
          className="fit back"
          onClick={() => {
            navigateBack("/");
          }}
        >
          <ChevronLeft /> Back
        </div>
      }
    >
      <div className="details">
        <Thumbnail video={video} large>
          <VideoControls />
        </Thumbnail>
        <VideoDetails id={video.id} />
      </div>
    </Layout>
  );
}

function VideoInfo({ id }) {
  const details = use(fetchVideoDetails(id));
  return (
    <div>
      <p className="fit info-title">{details.title}</p>
      <p className="fit info-description">{details.description}</p>
    </div>
  );
}
```

```js src/Home.js hidden
import { Video } from "./Videos";
import Layout from "./Layout";
import { fetchVideos } from "./data";
import { useId, useState, use } from "react";
import { IconSearch } from "./Icons";

function SearchInput({ value, onChange }) {
  const id = useId();
  return (
    <form className="search" onSubmit={(e) => e.preventDefault()}>
      <label htmlFor={id} className="sr-only">
        Search
      </label>
      <div className="search-input">
        <div className="search-icon">
          <IconSearch />
        </div>
        <input
          type="text"
          id={id}
          placeholder="Search"
          value={value}
          onChange={(e) => onChange(e.target.value)}
        />
      </div>
    </form>
  );
}

function filterVideos(videos, query) {
  const keywords = query
    .toLowerCase()
    .split(" ")
    .filter((s) => s !== "");
  if (keywords.length === 0) {
    return videos;
  }
  return videos.filter((video) => {
    const words = (video.title + " " + video.description)
      .toLowerCase()
      .split(" ");
    return keywords.every((kw) => words.some((w) => w.includes(kw)));
  });
}

export default function Home() {
  const videos = use(fetchVideos());
  const count = videos.length;
  const [searchText, setSearchText] = useState("");
  const foundVideos = filterVideos(videos, searchText);
  return (
    <Layout heading={<div className="fit">{count} Videos</div>}>
      <SearchInput value={searchText} onChange={setSearchText} />
      <div className="video-list">
        {foundVideos.length === 0 && (
          <div className="no-results">No results</div>
        )}
        <div className="videos">
          {foundVideos.map((video) => (
            <Video key={video.id} video={video} />
          ))}
        </div>
      </div>
    </Layout>
  );
}

```

```js src/Icons.js hidden
export function ChevronLeft() {
  return (
    <svg
      className="chevron-left"
      xmlns="http://www.w3.org/2000/svg"
      width="20"
      height="20"
      viewBox="0 0 20 20">
      <g fill="none" fillRule="evenodd" transform="translate(-446 -398)">
        <path
          fill="currentColor"
          fillRule="nonzero"
          d="M95.8838835,240.366117 C95.3957281,239.877961 94.6042719,239.877961 94.1161165,240.366117 C93.6279612,240.854272 93.6279612,241.645728 94.1161165,242.133883 L98.6161165,246.633883 C99.1042719,247.122039 99.8957281,247.122039 100.383883,246.633883 L104.883883,242.133883 C105.372039,241.645728 105.372039,240.854272 104.883883,240.366117 C104.395728,239.877961 103.604272,239.877961 103.116117,240.366117 L99.5,243.982233 L95.8838835,240.366117 Z"
          transform="translate(356.5 164.5)"
        />
        <polygon points="446 418 466 418 466 398 446 398" />
      </g>
    </svg>
  );
}

export function PauseIcon() {
  return (
    <svg
      className="control-icon"
      style={{padding: '4px'}}
      width="100"
      height="100"
      viewBox="0 0 512 512"
      fill="none"
      xmlns="http://www.w3.org/2000/svg">
      <path
        fillRule="evenodd"
        clipRule="evenodd"
        d="M256 0C114.617 0 0 114.615 0 256s114.617 256 256 256 256-114.615 256-256S397.383 0 256 0zm-32 320c0 8.836-7.164 16-16 16h-32c-8.836 0-16-7.164-16-16V192c0-8.836 7.164-16 16-16h32c8.836 0 16 7.164 16 16v128zm128 0c0 8.836-7.164 16-16 16h-32c-8.836 0-16-7.164-16-16V192c0-8.836 7.164-16 16-16h32c8.836 0 16 7.164 16 16v128z"
        fill="currentColor"
      />
    </svg>
  );
}

export function PlayIcon() {
  return (
    <svg
      className="control-icon"
      width="100"
      height="100"
      viewBox="0 0 72 72"
      fill="none"
      xmlns="http://www.w3.org/2000/svg">
      <path
        fillRule="evenodd"
        clipRule="evenodd"
        d="M36 69C54.2254 69 69 54.2254 69 36C69 17.7746 54.2254 3 36 3C17.7746 3 3 17.7746 3 36C3 54.2254 17.7746 69 36 69ZM52.1716 38.6337L28.4366 51.5801C26.4374 52.6705 24 51.2235 24 48.9464V23.0536C24 20.7764 26.4374 19.3295 28.4366 20.4199L52.1716 33.3663C54.2562 34.5034 54.2562 37.4966 52.1716 38.6337Z"
        fill="currentColor"
      />
    </svg>
  );
}
export function Heart({liked, animate}) {
  return (
    <>
      <svg
        className="absolute overflow-visible"
        viewBox="0 0 24 24"
        fill="none"
        xmlns="http://www.w3.org/2000/svg">
        <circle
          className={`circle ${liked ? 'liked' : ''} ${animate ? 'animate' : ''}`}
          cx="12"
          cy="12"
          r="11.5"
          fill="transparent"
          strokeWidth="0"
          stroke="currentColor"
        />
      </svg>

      <svg
        className={`heart ${liked ? 'liked' : ''} ${animate ? 'animate' : ''}`}
        viewBox="0 0 24 24"
        fill="none"
        xmlns="http://www.w3.org/2000/svg">
        {liked ? (
          <path
            d="M12 23a.496.496 0 0 1-.26-.074C7.023 19.973 0 13.743 0 8.68c0-4.12 2.322-6.677 6.058-6.677 2.572 0 5.108 2.387 5.134 2.41l.808.771.808-.771C12.834 4.387 15.367 2 17.935 2 21.678 2 24 4.558 24 8.677c0 5.06-7.022 11.293-11.74 14.246a.496.496 0 0 1-.26.074V23z"
            fill="currentColor"
          />
        ) : (
          <path
            fillRule="evenodd"
            clipRule="evenodd"
            d="m12 5.184-.808-.771-.004-.004C11.065 4.299 8.522 2.003 6 2.003c-3.736 0-6 2.558-6 6.677 0 4.47 5.471 9.848 10 13.079.602.43 1.187.82 1.74 1.167A.497.497 0 0 0 12 23v-.003c.09 0 .182-.026.26-.074C16.977 19.97 24 13.737 24 8.677 24 4.557 21.743 2 18 2c-2.569 0-5.166 2.387-5.192 2.413L12 5.184zm-.002 15.525c2.071-1.388 4.477-3.342 6.427-5.47C20.72 12.733 22 10.401 22 8.677c0-1.708-.466-2.855-1.087-3.55C20.316 4.459 19.392 4 18 4c-.726 0-1.63.364-2.5.9-.67.412-1.148.82-1.266.92-.03.025-.037.031-.019.014l-.013.013L12 7.949 9.832 5.88a10.08 10.08 0 0 0-1.33-.977C7.633 4.367 6.728 4.003 6 4.003c-1.388 0-2.312.459-2.91 1.128C2.466 5.826 2 6.974 2 8.68c0 1.726 1.28 4.058 3.575 6.563 1.948 2.127 4.352 4.078 6.423 5.466z"
            fill="currentColor"
          />
        )}
      </svg>
    </>
  );
}

export function IconSearch(props) {
  return (
    <svg width="1em" height="1em" viewBox="0 0 20 20">
      <path
        d="M14.386 14.386l4.0877 4.0877-4.0877-4.0877c-2.9418 2.9419-7.7115 2.9419-10.6533 0-2.9419-2.9418-2.9419-7.7115 0-10.6533 2.9418-2.9419 7.7115-2.9419 10.6533 0 2.9419 2.9418 2.9419 7.7115 0 10.6533z"
        stroke="currentColor"
        fill="none"
        strokeWidth="2"
        fillRule="evenodd"
        strokeLinecap="round"
        strokeLinejoin="round"></path>
    </svg>
  );
}
```

```js src/Layout.js hidden
import {ViewTransition} from 'react';
import { useIsNavPending } from "./router";

export default function Page({ heading, children }) {
  const isPending = useIsNavPending();
  return (
    <div className="page">
      <div className="top">
        <div className="top-nav">
          {/* Custom classes based on transition type. */}
          <ViewTransition
            name="nav"
            share={{
              'nav-forward': 'slide-forward',
              'nav-back': 'slide-back',
            }}>
            {heading}
          </ViewTransition>
          {isPending && <span className="loader"></span>}
        </div>
      </div>
      {/* Opt-out of ViewTransition for the content. */}
      {/* Content can define it's own ViewTransition. */}
      <ViewTransition default="none">
        <div className="bottom">
          <div className="content">{children}</div>
        </div>
      </ViewTransition>
    </div>
  );
}
```

```js src/LikeButton.js hidden
import {useState} from 'react';
import {Heart} from './Icons';

// A hack since we don't actually have a backend.
// Unlike local state, this survives videos being filtered.
const likedVideos = new Set();

export default function LikeButton({video}) {
  const [isLiked, setIsLiked] = useState(() => likedVideos.has(video.id));
  const [animate, setAnimate] = useState(false);
  return (
    <button
      className={`like-button ${isLiked && 'liked'}`}
      aria-label={isLiked ? 'Unsave' : 'Save'}
      onClick={() => {
        const nextIsLiked = !isLiked;
        if (nextIsLiked) {
          likedVideos.add(video.id);
        } else {
          likedVideos.delete(video.id);
        }
        setAnimate(true);
        setIsLiked(nextIsLiked);
      }}>
      <Heart liked={isLiked} animate={animate} />
    </button>
  );
}
```

```js src/Videos.js hidden
import { useState, ViewTransition } from "react";
import LikeButton from "./LikeButton";
import { useRouter } from "./router";
import { PauseIcon, PlayIcon } from "./Icons";
import { startTransition } from "react";

export function Thumbnail({ video, children }) {
  // Add a name to animate with a shared element transition.
  // This uses the default animation, no additional css needed.
  return (
    <ViewTransition name={`video-${video.id}`}>
      <div
        aria-hidden="true"
        tabIndex={-1}
        className={`thumbnail ${video.image}`}
      >
        {children}
      </div>
    </ViewTransition>
  );
}

export function VideoControls() {
  const [isPlaying, setIsPlaying] = useState(false);

  return (
    <span
      className="controls"
      onClick={() =>
        startTransition(() => {
          setIsPlaying((p) => !p);
        })
      }
    >
      {isPlaying ? <PauseIcon /> : <PlayIcon />}
    </span>
  );
}

export function Video({ video }) {
  const { navigate } = useRouter();

  return (
    <div className="video">
      <div
        className="link"
        onClick={(e) => {
          e.preventDefault();
          navigate(`/video/${video.id}`);
        }}
      >
        <Thumbnail video={video}></Thumbnail>

        <div className="info">
          <div className="video-title">{video.title}</div>
          <div className="video-description">{video.description}</div>
        </div>
      </div>
      <LikeButton video={video} />
    </div>
  );
}
```


```js src/data.js hidden
const videos = [
  {
    id: '1',
    title: 'First video',
    description: 'Video description',
    image: 'blue',
  },
  {
    id: '2',
    title: 'Second video',
    description: 'Video description',
    image: 'red',
  },
  {
    id: '3',
    title: 'Third video',
    description: 'Video description',
    image: 'green',
  },
  {
    id: '4',
    title: 'Fourth video',
    description: 'Video description',
    image: 'purple',
  },
  {
    id: '5',
    title: 'Fifth video',
    description: 'Video description',
    image: 'yellow',
  },
  {
    id: '6',
    title: 'Sixth video',
    description: 'Video description',
    image: 'gray',
  },
];

let videosCache = new Map();
let videoCache = new Map();
let videoDetailsCache = new Map();
const VIDEO_DELAY = 1;
const VIDEO_DETAILS_DELAY = 1000;
export function fetchVideos() {
  if (videosCache.has(0)) {
    return videosCache.get(0);
  }
  const promise = new Promise((resolve) => {
    setTimeout(() => {
      resolve(videos);
    }, VIDEO_DELAY);
  });
  videosCache.set(0, promise);
  return promise;
}

export function fetchVideo(id) {
  if (videoCache.has(id)) {
    return videoCache.get(id);
  }
  const promise = new Promise((resolve) => {
    setTimeout(() => {
      resolve(videos.find((video) => video.id === id));
    }, VIDEO_DELAY);
  });
  videoCache.set(id, promise);
  return promise;
}

export function fetchVideoDetails(id) {
  if (videoDetailsCache.has(id)) {
    return videoDetailsCache.get(id);
  }
  const promise = new Promise((resolve) => {
    setTimeout(() => {
      resolve(videos.find((video) => video.id === id));
    }, VIDEO_DETAILS_DELAY);
  });
  videoDetailsCache.set(id, promise);
  return promise;
}
```

```js src/router.js hidden
import {useState, createContext, use, useTransition, useLayoutEffect, useEffect, addTransitionType} from "react";

export function Router({ children }) {
  const [isPending, startTransition] = useTransition();
  const [routerState, setRouterState] = useState({pendingNav: () => {}, url: document.location.pathname});
  function navigate(url) {
    startTransition(() => {
      // Transition type for the cause "nav forward"
      addTransitionType('nav-forward');
      go(url);
    });
  }
  function navigateBack(url) {
    startTransition(() => {
      // Transition type for the cause "nav backward"
      addTransitionType('nav-back');
      go(url);
    });
  }

  function go(url) {
    setRouterState({
      url,
      pendingNav() {
        window.history.pushState({}, "", url);
      },
    });
  }

  useEffect(() => {
    function handlePopState() {
      // 因为恢复必须是同步的，所以应该没有动画。
      // Even though it's a transition.
      startTransition(() => {
        setRouterState({
          url: document.location.pathname + document.location.search,
          pendingNav() {
            // Noop. URL has already updated.
          },
        });
      });
    }
    window.addEventListener("popstate", handlePopState);
    return () => {
      window.removeEventListener("popstate", handlePopState);
    };
  }, []);
  const pendingNav = routerState.pendingNav;
  useLayoutEffect(() => {
    pendingNav();
  }, [pendingNav]);

  return (
    <RouterContext
      value={{
        url: routerState.url,
        navigate,
        navigateBack,
        isPending,
        params: {},
      }}
    >
      {children}
    </RouterContext>
  );
}

const RouterContext = createContext({ url: "/", params: {} });

export function useRouter() {
  return use(RouterContext);
}

export function useIsNavPending() {
  return use(RouterContext).isPending;
}

```

```css src/styles.css hidden
@font-face {
  font-family: Optimistic Text;
  src: url(https://react.dev/fonts/Optimistic_Text_W_Rg.woff2) format("woff2");
  font-weight: 400;
  font-style: normal;
  font-display: swap;
}

@font-face {
  font-family: Optimistic Text;
  src: url(https://react.dev/fonts/Optimistic_Text_W_Md.woff2) format("woff2");
  font-weight: 500;
  font-style: normal;
  font-display: swap;
}

@font-face {
  font-family: Optimistic Text;
  src: url(https://react.dev/fonts/Optimistic_Text_W_Bd.woff2) format("woff2");
  font-weight: 600;
  font-style: normal;
  font-display: swap;
}

@font-face {
  font-family: Optimistic Text;
  src: url(https://react.dev/fonts/Optimistic_Text_W_Bd.woff2) format("woff2");
  font-weight: 700;
  font-style: normal;
  font-display: swap;
}

* {
  box-sizing: border-box;
}

html {
  background-image: url(https://react.dev/images/meta-gradient-dark.png);
  background-size: 100%;
  background-position: -100%;
  background-color: rgb(64 71 86);
  background-repeat: no-repeat;
  height: 100%;
  width: 100%;
}

body {
  font-family: Optimistic Text, -apple-system, ui-sans-serif, system-ui, sans-serif, Apple Color Emoji, Segoe UI Emoji, Segoe UI Symbol, Noto Color Emoji;
  padding: 10px 0 10px 0;
  margin: 0;
  display: flex;
  justify-content: center;
}

#root {
  flex: 1 1;
  height: auto;
  background-color: #fff;
  border-radius: 10px;
  max-width: 450px;
  min-height: 600px;
  padding-bottom: 10px;
}

h1 {
  margin-top: 0;
  font-size: 22px;
}

h2 {
  margin-top: 0;
  font-size: 20px;
}

h3 {
  margin-top: 0;
  font-size: 18px;
}

h4 {
  margin-top: 0;
  font-size: 16px;
}

h5 {
  margin-top: 0;
  font-size: 14px;
}

h6 {
  margin-top: 0;
  font-size: 12px;
}

code {
  font-size: 1.2em;
}

ul {
  padding-inline-start: 20px;
}

.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  padding: 0;
  margin: -1px;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  white-space: nowrap;
  border-width: 0;
}

.absolute {
  position: absolute;
}

.overflow-visible {
  overflow: visible;
}

.visible {
  overflow: visible;
}

.fit {
  width: fit-content;
}


/* Layout */
.page {
  display: flex;
  flex-direction: column;
  height: 100%;
}

.top-hero {
  height: 200px;
  display: flex;
  justify-content: center;
  align-items: center;
  background-image: conic-gradient(
      from 90deg at -10% 100%,
      #2b303b 0deg,
      #2b303b 90deg,
      #16181d 1turn
  );
}

.bottom {
  flex: 1;
  overflow: auto;
}

.top-nav {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 0;
  padding: 0 12px;
  top: 0;
  width: 100%;
  height: 44px;
  color: #23272f;
  font-weight: 700;
  font-size: 20px;
  z-index: 100;
  cursor: default;
}

.content {
  padding: 0 12px;
  margin-top: 4px;
}


.loader {
  color: #23272f;
  font-size: 3px;
  width: 1em;
  margin-right: 18px;
  height: 1em;
  border-radius: 50%;
  position: relative;
  text-indent: -9999em;
  animation: loading-spinner 1.3s infinite linear;
  animation-delay: 200ms;
  transform: translateZ(0);
}

@keyframes loading-spinner {
  0%,
  100% {
    box-shadow: 0 -3em 0 0.2em,
    2em -2em 0 0em, 3em 0 0 -1em,
    2em 2em 0 -1em, 0 3em 0 -1em,
    -2em 2em 0 -1em, -3em 0 0 -1em,
    -2em -2em 0 0;
  }
  12.5% {
    box-shadow: 0 -3em 0 0, 2em -2em 0 0.2em,
    3em 0 0 0, 2em 2em 0 -1em, 0 3em 0 -1em,
    -2em 2em 0 -1em, -3em 0 0 -1em,
    -2em -2em 0 -1em;
  }
  25% {
    box-shadow: 0 -3em 0 -0.5em,
    2em -2em 0 0, 3em 0 0 0.2em,
    2em 2em 0 0, 0 3em 0 -1em,
    -2em 2em 0 -1em, -3em 0 0 -1em,
    -2em -2em 0 -1em;
  }
  37.5% {
    box-shadow: 0 -3em 0 -1em, 2em -2em 0 -1em,
    3em 0em 0 0, 2em 2em 0 0.2em, 0 3em 0 0em,
    -2em 2em 0 -1em, -3em 0em 0 -1em, -2em -2em 0 -1em;
  }
  50% {
    box-shadow: 0 -3em 0 -1em, 2em -2em 0 -1em,
    3em 0 0 -1em, 2em 2em 0 0em, 0 3em 0 0.2em,
    -2em 2em 0 0, -3em 0em 0 -1em, -2em -2em 0 -1em;
  }
  62.5% {
    box-shadow: 0 -3em 0 -1em, 2em -2em 0 -1em,
    3em 0 0 -1em, 2em 2em 0 -1em, 0 3em 0 0,
    -2em 2em 0 0.2em, -3em 0 0 0, -2em -2em 0 -1em;
  }
  75% {
    box-shadow: 0em -3em 0 -1em, 2em -2em 0 -1em,
    3em 0em 0 -1em, 2em 2em 0 -1em, 0 3em 0 -1em,
    -2em 2em 0 0, -3em 0em 0 0.2em, -2em -2em 0 0;
  }
  87.5% {
    box-shadow: 0em -3em 0 0, 2em -2em 0 -1em,
    3em 0 0 -1em, 2em 2em 0 -1em, 0 3em 0 -1em,
    -2em 2em 0 0, -3em 0em 0 0, -2em -2em 0 0.2em;
  }
}

/* LikeButton */
.like-button {
  outline-offset: 2px;
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
  width: 2.5rem;
  height: 2.5rem;
  cursor: pointer;
  border-radius: 9999px;
  border: none;
  outline: none 2px;
  color: #5e687e;
  background: none;
}

.like-button:focus {
  color: #a6423a;
  background-color: rgba(166, 66, 58, .05);
}

.like-button:active {
  color: #a6423a;
  background-color: rgba(166, 66, 58, .05);
  transform: scaleX(0.95) scaleY(0.95);
}

.like-button:hover {
  background-color: #f6f7f9;
}

.like-button.liked {
  color: #a6423a;
}

/* Icons */
@keyframes circle {
  0% {
    transform: scale(0);
    stroke-width: 16px;
  }

  50% {
    transform: scale(.5);
    stroke-width: 16px;
  }

  to {
    transform: scale(1);
    stroke-width: 0;
  }
}

.circle {
  color: rgba(166, 66, 58, .5);
  transform-origin: center;
  transition-property: all;
  transition-duration: .15s;
  transition-timing-function: cubic-bezier(.4,0,.2,1);
}

.circle.liked.animate {
  animation: circle .3s forwards;
}

.heart {
  width: 1.5rem;
  height: 1.5rem;
}

.heart.liked {
  transform-origin: center;
  transition-property: all;
  transition-duration: .15s;
  transition-timing-function: cubic-bezier(.4, 0, .2, 1);
}

.heart.liked.animate {
  animation: scale .35s ease-in-out forwards;
}

.control-icon {
  color: hsla(0, 0%, 100%, .5);
  filter:  drop-shadow(0 20px 13px rgba(0, 0, 0, .03)) drop-shadow(0 8px 5px rgba(0, 0, 0, .08));
}

.chevron-left {
  margin-top: 2px;
  rotate: 90deg;
}


/* Video */
.thumbnail {
  position: relative;
  aspect-ratio: 16 / 9;
  display: flex;
  overflow: hidden;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  border-radius: 0.5rem;
  outline-offset: 2px;
  width: 8rem;
  vertical-align: middle;
  background-color: #ffffff;
  background-size: cover;
  user-select: none;
}

.thumbnail.blue {
  background-image: conic-gradient(at top right, #c76a15, #087ea4, #2b3491);
}

.thumbnail.red {
  background-image: conic-gradient(at top right, #c76a15, #a6423a, #2b3491);
}

.thumbnail.green {
  background-image: conic-gradient(at top right, #c76a15, #388f7f, #2b3491);
}

.thumbnail.purple {
  background-image: conic-gradient(at top right, #c76a15, #575fb7, #2b3491);
}

.thumbnail.yellow {
  background-image: conic-gradient(at top right, #c76a15, #FABD62, #2b3491);
}

.thumbnail.gray {
  background-image: conic-gradient(at top right, #c76a15, #4E5769, #2b3491);
}

.video {
  display: flex;
  flex-direction: row;
  gap: 0.75rem;
  align-items: center;
}

.video .link {
  display: flex;
  flex-direction: row;
  flex: 1 1 0;
  gap: 0.125rem;
  outline-offset: 4px;
  cursor: pointer;
}

.video .info {
  display: flex;
  flex-direction: column;
  justify-content: center;
  margin-left: 8px;
  gap: 0.125rem;
}

.video .info:hover {
  text-decoration: underline;
}

.video-title {
  font-size: 15px;
  line-height: 1.25;
  font-weight: 700;
  color: #23272f;
}

.video-description {
  color: #5e687e;
  font-size: 13px;
}

/* Details */
.details .thumbnail {
  position: relative;
  aspect-ratio: 16 / 9;
  display: flex;
  overflow: hidden;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  border-radius: 0.5rem;
  outline-offset: 2px;
  width: 100%;
  vertical-align: middle;
  background-color: #ffffff;
  background-size: cover;
  user-select: none;
}

.video-details-title {
  margin-top: 8px;
}

.video-details-speaker {
  display: flex;
  gap: 8px;
  margin-top: 10px
}

.back {
  display: flex;
  align-items: center;
  margin-left: -5px;
  cursor: pointer;
}

.back:hover {
  text-decoration: underline;
}

.info-title {
  font-size: 1.5rem;
  font-weight: 700;
  line-height: 1.25;
  margin: 8px 0 0 0 ;
}

.info-description {
  margin: 8px 0 0 0;
}

.controls {
  cursor: pointer;
}

.fallback {
  background: #f6f7f8 linear-gradient(to right, #e6e6e6 5%, #cccccc 25%, #e6e6e6 35%) no-repeat;
  background-size: 800px 104px;
  display: block;
  line-height: 1.25;
  margin: 8px 0 0 0;
  border-radius: 5px;
  overflow: hidden;

  animation: 1s linear 1s infinite shimmer;
  animation-delay: 300ms;
  animation-duration: 1s;
  animation-fill-mode: forwards;
  animation-iteration-count: infinite;
  animation-name: shimmer;
  animation-timing-function: linear;
}


.fallback.title {
  width: 130px;
  height: 30px;

}

.fallback.description {
  width: 150px;
  height: 21px;
}

@keyframes shimmer {
  0% {
    background-position: -468px 0;
  }

  100% {
    background-position: 468px 0;
  }
}

.search {
  margin-bottom: 10px;
}
.search-input {
  width: 100%;
  position: relative;
}

.search-icon {
  position: absolute;
  top: 0;
  bottom: 0;
  inset-inline-start: 0;
  display: flex;
  align-items: center;
  padding-inline-start: 1rem;
  pointer-events: none;
  color: #99a1b3;
}

.search-input input {
  display: flex;
  padding-inline-start: 2.75rem;
  padding-top: 10px;
  padding-bottom: 10px;
  width: 100%;
  text-align: start;
  background-color: rgb(235 236 240);
  outline: 2px solid transparent;
  cursor: pointer;
  border: none;
  align-items: center;
  color: rgb(35 39 47);
  border-radius: 9999px;
  vertical-align: middle;
  font-size: 15px;
}

.search-input input:hover, .search-input input:active {
  background-color: rgb(235 236 240/ 0.8);
  color: rgb(35 39 47/ 0.8);
}

/* Home */
.video-list {
  position: relative;
}

.video-list .videos {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  overflow-y: auto;
  height: 100%;
}
```


```css src/animations.css
/* Slide the fallback down */
::view-transition-old(.slide-down) {
    animation: 150ms ease-out both fade-out, 150ms ease-out both slide-down;
}

/* Slide the content up */
::view-transition-new(.slide-up) {
    animation: 210ms ease-in 150ms both fade-in, 400ms ease-in both slide-up;
}

/* Define the new keyframes */
@keyframes slide-up {
    from {
        transform: translateY(10px);
    }
    to {
        transform: translateY(0);
    }
}

@keyframes slide-down {
    from {
        transform: translateY(0);
    }
    to {
        transform: translateY(10px);
    }
}

/* Previously defined animations below */

/* Animations for view transition classed added by transition type */
::view-transition-old(.slide-forward) {
    /* when sliding forward, the "old" page should slide out to left. */
    animation: 150ms cubic-bezier(0.4, 0, 1, 1) both fade-out,
    400ms cubic-bezier(0.4, 0, 0.2, 1) both slide-to-left;
}

::view-transition-new(.slide-forward) {
    /* when sliding forward, the "new" page should slide in from right. */
    animation: 210ms cubic-bezier(0, 0, 0.2, 1) 150ms both fade-in,
    400ms cubic-bezier(0.4, 0, 0.2, 1) both slide-from-right;
}

::view-transition-old(.slide-back) {
    /* when sliding back, the "old" page should slide out to right. */
    animation: 150ms cubic-bezier(0.4, 0, 1, 1) both fade-out,
    400ms cubic-bezier(0.4, 0, 0.2, 1) both slide-to-right;
}

::view-transition-new(.slide-back) {
    /* when sliding back, the "new" page should slide in from left. */
    animation: 210ms cubic-bezier(0, 0, 0.2, 1) 150ms both fade-in,
    400ms cubic-bezier(0.4, 0, 0.2, 1) both slide-from-left;
}

/* Keyframes to support our animations above. */
@keyframes fade-in {
    from {
        opacity: 0;
    }
}

@keyframes fade-out {
    to {
        opacity: 0;
    }
}

@keyframes slide-to-right {
    to {
        transform: translateX(50px);
    }
}

@keyframes slide-from-right {
    from {
        transform: translateX(50px);
    }
    to {
        transform: translateX(0);
    }
}

@keyframes slide-to-left {
    to {
        transform: translateX(-50px);
    }
}

@keyframes slide-from-left {
    from {
        transform: translateX(-50px);
    }
    to {
        transform: translateX(0);
    }
}

/* Default .slow-fade. */
::view-transition-old(.slow-fade) {
    animation-duration: 500ms;
}

::view-transition-new(.slow-fade) {
    animation-duration: 500ms;
}
```

```js src/index.js hidden
import React, {StrictMode} from 'react';
import {createRoot} from 'react-dom/client';
import './styles.css';
import './animations.css';

import App from './App';
import {Router} from './router';

const root = createRoot(document.getElementById('root'));
root.render(
  <StrictMode>
    <Router>
      <App />
    </Router>
  </StrictMode>
);
```

```json package.json hidden
{
  "dependencies": {
    "react": "canary",
    "react-dom": "canary",
    "react-scripts": "latest"
  },
  "scripts": {
    "start": "react-scripts start",
    "build": "react-scripts build",
    "test": "react-scripts test --env=jsdom",
    "eject": "react-scripts eject"
  }
}
```

</Sandpack>

我们还可以使用后备方案上的 `exit` 和内容上的 `enter` 提供自定义动画：

```js {3,8}
<Suspense
  fallback={
    <ViewTransition exit="slide-down">
      <VideoInfoFallback />
    </ViewTransition>
  }
>
  <ViewTransition enter="slide-up">
    <VideoInfo id={id} />
  </ViewTransition>
</Suspense>
```

以下是我们如何在 CSS 中定义 `slide-down` 和 `slide-up`：

```css {1, 6}
::view-transition-old(.slide-down) {
  /* Slide the fallback down */
  animation: ...;
}

::view-transition-new(.slide-up) {
  /* Slide the content up */
  animation: ...;
}
```

Now, the Suspense content replaces the fallback with a sliding animation:

<Sandpack>

```js src/App.js hidden
import { ViewTransition } from "react";
import Details from "./Details";
import Home from "./Home";
import { useRouter } from "./router";

export default function App() {
  const { url } = useRouter();

  // Default slow-fade animation.
  return (
    <ViewTransition default="slow-fade">
      {url === "/" ? <Home /> : <Details />}
    </ViewTransition>
  );
}
```

```js src/Details.js active
import { use, Suspense, ViewTransition } from "react"; import { fetchVideo, fetchVideoDetails } from "./data"; import { Thumbnail, VideoControls } from "./Videos"; import { useRouter } from "./router"; import Layout from "./Layout"; import { ChevronLeft } from "./Icons";

function VideoDetails({ id }) {
  return (
    <Suspense
      fallback={
        // Animate the fallback down.
        <ViewTransition exit="slide-down">
          <VideoInfoFallback />
        </ViewTransition>
      }
    >
      {/* Animate the content up */}
      <ViewTransition enter="slide-up">
        <VideoInfo id={id} />
      </ViewTransition>
    </Suspense>
  );
}

function VideoInfoFallback() {
  return (
    <>
      <div className="fallback title"></div>
      <div className="fallback description"></div>
    </>
  );
}

export default function Details() {
  const { url, navigateBack } = useRouter();
  const videoId = url.split("/").pop();
  const video = use(fetchVideo(videoId));

  return (
    <Layout
      heading={
        <div
          className="fit back"
          onClick={() => {
            navigateBack("/");
          }}
        >
          <ChevronLeft /> Back
        </div>
      }
    >
      <div className="details">
        <Thumbnail video={video} large>
          <VideoControls />
        </Thumbnail>
        <VideoDetails id={video.id} />
      </div>
    </Layout>
  );
}

function VideoInfo({ id }) {
  const details = use(fetchVideoDetails(id));
  return (
    <>
      <p className="info-title">{details.title}</p>
      <p className="info-description">{details.description}</p>
    </>
  );
}
```

```js src/Home.js hidden
import { Video } from "./Videos";
import Layout from "./Layout";
import { fetchVideos } from "./data";
import { useId, useState, use } from "react";
import { IconSearch } from "./Icons";

function SearchInput({ value, onChange }) {
  const id = useId();
  return (
    <form className="search" onSubmit={(e) => e.preventDefault()}>
      <label htmlFor={id} className="sr-only">
        Search
      </label>
      <div className="search-input">
        <div className="search-icon">
          <IconSearch />
        </div>
        <input
          type="text"
          id={id}
          placeholder="Search"
          value={value}
          onChange={(e) => onChange(e.target.value)}
        />
      </div>
    </form>
  );
}

function filterVideos(videos, query) {
  const keywords = query
    .toLowerCase()
    .split(" ")
    .filter((s) => s !== "");
  if (keywords.length === 0) {
    return videos;
  }
  return videos.filter((video) => {
    const words = (video.title + " " + video.description)
      .toLowerCase()
      .split(" ");
    return keywords.every((kw) => words.some((w) => w.includes(kw)));
  });
}

export default function Home() {
  const videos = use(fetchVideos());
  const count = videos.length;
  const [searchText, setSearchText] = useState("");
  const foundVideos = filterVideos(videos, searchText);
  return (
    <Layout heading={<div className="fit">{count} Videos</div>}>
      <SearchInput value={searchText} onChange={setSearchText} />
      <div className="video-list">
        {foundVideos.length === 0 && (
          <div className="no-results">No results</div>
        )}
        <div className="videos">
          {foundVideos.map((video) => (
            <Video key={video.id} video={video} />
          ))}
        </div>
      </div>
    </Layout>
  );
}

```

```js src/Icons.js hidden
export function ChevronLeft() {
  return (
    <svg
      className="chevron-left"
      xmlns="http://www.w3.org/2000/svg"
      width="20"
      height="20"
      viewBox="0 0 20 20">
      <g fill="none" fillRule="evenodd" transform="translate(-446 -398)">
        <path
          fill="currentColor"
          fillRule="nonzero"
          d="M95.8838835,240.366117 C95.3957281,239.877961 94.6042719,239.877961 94.1161165,240.366117 C93.6279612,240.854272 93.6279612,241.645728 94.1161165,242.133883 L98.6161165,246.633883 C99.1042719,247.122039 99.8957281,247.122039 100.383883,246.633883 L104.883883,242.133883 C105.372039,241.645728 105.372039,240.854272 104.883883,240.366117 C104.395728,239.877961 103.604272,239.877961 103.116117,240.366117 L99.5,243.982233 L95.8838835,240.366117 Z"
          transform="translate(356.5 164.5)"
        />
        <polygon points="446 418 466 418 466 398 446 398" />
      </g>
    </svg>
  );
}

export function PauseIcon() {
  return (
    <svg
      className="control-icon"
      style={{padding: '4px'}}
      width="100"
      height="100"
      viewBox="0 0 512 512"
      fill="none"
      xmlns="http://www.w3.org/2000/svg">
      <path
        fillRule="evenodd"
        clipRule="evenodd"
        d="M256 0C114.617 0 0 114.615 0 256s114.617 256 256 256 256-114.615 256-256S397.383 0 256 0zm-32 320c0 8.836-7.164 16-16 16h-32c-8.836 0-16-7.164-16-16V192c0-8.836 7.164-16 16-16h32c8.836 0 16 7.164 16 16v128zm128 0c0 8.836-7.164 16-16 16h-32c-8.836 0-16-7.164-16-16V192c0-8.836 7.164-16 16-16h32c8.836 0 16 7.164 16 16v128z"
        fill="currentColor"
      />
    </svg>
  );
}

export function PlayIcon() {
  return (
    <svg
      className="control-icon"
      width="100"
      height="100"
      viewBox="0 0 72 72"
      fill="none"
      xmlns="http://www.w3.org/2000/svg">
      <path
        fillRule="evenodd"
        clipRule="evenodd"
        d="M36 69C54.2254 69 69 54.2254 69 36C69 17.7746 54.2254 3 36 3C17.7746 3 3 17.7746 3 36C3 54.2254 17.7746 69 36 69ZM52.1716 38.6337L28.4366 51.5801C26.4374 52.6705 24 51.2235 24 48.9464V23.0536C24 20.7764 26.4374 19.3295 28.4366 20.4199L52.1716 33.3663C54.2562 34.5034 54.2562 37.4966 52.1716 38.6337Z"
        fill="currentColor"
      />
    </svg>
  );
}
export function Heart({liked, animate}) {
  return (
    <>
      <svg
        className="absolute overflow-visible"
        viewBox="0 0 24 24"
        fill="none"
        xmlns="http://www.w3.org/2000/svg">
        <circle
          className={`circle ${liked ? 'liked' : ''} ${animate ? 'animate' : ''}`}
          cx="12"
          cy="12"
          r="11.5"
          fill="transparent"
          strokeWidth="0"
          stroke="currentColor"
        />
      </svg>

      <svg
        className={`heart ${liked ? 'liked' : ''} ${animate ? 'animate' : ''}`}
        viewBox="0 0 24 24"
        fill="none"
        xmlns="http://www.w3.org/2000/svg">
        {liked ? (
          <path
            d="M12 23a.496.496 0 0 1-.26-.074C7.023 19.973 0 13.743 0 8.68c0-4.12 2.322-6.677 6.058-6.677 2.572 0 5.108 2.387 5.134 2.41l.808.771.808-.771C12.834 4.387 15.367 2 17.935 2 21.678 2 24 4.558 24 8.677c0 5.06-7.022 11.293-11.74 14.246a.496.496 0 0 1-.26.074V23z"
            fill="currentColor"
          />
        ) : (
          <path
            fillRule="evenodd"
            clipRule="evenodd"
            d="m12 5.184-.808-.771-.004-.004C11.065 4.299 8.522 2.003 6 2.003c-3.736 0-6 2.558-6 6.677 0 4.47 5.471 9.848 10 13.079.602.43 1.187.82 1.74 1.167A.497.497 0 0 0 12 23v-.003c.09 0 .182-.026.26-.074C16.977 19.97 24 13.737 24 8.677 24 4.557 21.743 2 18 2c-2.569 0-5.166 2.387-5.192 2.413L12 5.184zm-.002 15.525c2.071-1.388 4.477-3.342 6.427-5.47C20.72 12.733 22 10.401 22 8.677c0-1.708-.466-2.855-1.087-3.55C20.316 4.459 19.392 4 18 4c-.726 0-1.63.364-2.5.9-.67.412-1.148.82-1.266.92-.03.025-.037.031-.019.014l-.013.013L12 7.949 9.832 5.88a10.08 10.08 0 0 0-1.33-.977C7.633 4.367 6.728 4.003 6 4.003c-1.388 0-2.312.459-2.91 1.128C2.466 5.826 2 6.974 2 8.68c0 1.726 1.28 4.058 3.575 6.563 1.948 2.127 4.352 4.078 6.423 5.466z"
            fill="currentColor"
          />
        )}
      </svg>
    </>
  );
}

export function IconSearch(props) {
  return (
    <svg width="1em" height="1em" viewBox="0 0 20 20">
      <path
        d="M14.386 14.386l4.0877 4.0877-4.0877-4.0877c-2.9418 2.9419-7.7115 2.9419-10.6533 0-2.9419-2.9418-2.9419-7.7115 0-10.6533 2.9418-2.9419 7.7115-2.9419 10.6533 0 2.9419 2.9418 2.9419 7.7115 0 10.6533z"
        stroke="currentColor"
        fill="none"
        strokeWidth="2"
        fillRule="evenodd"
        strokeLinecap="round"
        strokeLinejoin="round"></path>
    </svg>
  );
}
```

```js src/Layout.js hidden
import {ViewTransition} from 'react';
import { useIsNavPending } from "./router";

export default function Page({ heading, children }) {
  const isPending = useIsNavPending();
  return (
    <div className="page">
      <div className="top">
        <div className="top-nav">
          {/* Custom classes based on transition type. */}
          <ViewTransition
            name="nav"
            share={{
              'nav-forward': 'slide-forward',
              'nav-back': 'slide-back',
            }}>
            {heading}
          </ViewTransition>
          {isPending && <span className="loader"></span>}
        </div>
      </div>
      {/* Opt-out of ViewTransition for the content. */}
      {/* Content can define it's own ViewTransition. */}
      <ViewTransition default="none">
        <div className="bottom">
          <div className="content">{children}</div>
        </div>
      </ViewTransition>
    </div>
  );
}
```

```js src/LikeButton.js hidden
import {useState} from 'react';
import {Heart} from './Icons';

// A hack since we don't actually have a backend.
// Unlike local state, this survives videos being filtered.
const likedVideos = new Set();

export default function LikeButton({video}) {
  const [isLiked, setIsLiked] = useState(() => likedVideos.has(video.id));
  const [animate, setAnimate] = useState(false);
  return (
    <button
      className={`like-button ${isLiked && 'liked'}`}
      aria-label={isLiked ? 'Unsave' : 'Save'}
      onClick={() => {
        const nextIsLiked = !isLiked;
        if (nextIsLiked) {
          likedVideos.add(video.id);
        } else {
          likedVideos.delete(video.id);
        }
        setAnimate(true);
        setIsLiked(nextIsLiked);
      }}>
      <Heart liked={isLiked} animate={animate} />
    </button>
  );
}
```

```js src/Videos.js hidden
import { useState, ViewTransition } from "react";
import LikeButton from "./LikeButton";
import { useRouter } from "./router";
import { PauseIcon, PlayIcon } from "./Icons";
import { startTransition } from "react";

export function Thumbnail({ video, children }) {
  // Add a name to animate with a shared element transition.
  // This uses the default animation, no additional css needed.
  return (
    <ViewTransition name={`video-${video.id}`}>
      <div
        aria-hidden="true"
        tabIndex={-1}
        className={`thumbnail ${video.image}`}
      >
        {children}
      </div>
    </ViewTransition>
  );
}

export function VideoControls() {
  const [isPlaying, setIsPlaying] = useState(false);

  return (
    <span
      className="controls"
      onClick={() =>
        startTransition(() => {
          setIsPlaying((p) => !p);
        })
      }
    >
      {isPlaying ? <PauseIcon /> : <PlayIcon />}
    </span>
  );
}

export function Video({ video }) {
  const { navigate } = useRouter();

  return (
    <div className="video">
      <div
        className="link"
        onClick={(e) => {
          e.preventDefault();
          navigate(`/video/${video.id}`);
        }}
      >
        <Thumbnail video={video}></Thumbnail>

        <div className="info">
          <div className="video-title">{video.title}</div>
          <div className="video-description">{video.description}</div>
        </div>
      </div>
      <LikeButton video={video} />
    </div>
  );
}
```


```js src/data.js hidden
const videos = [
  {
    id: '1',
    title: 'First video',
    description: 'Video description',
    image: 'blue',
  },
  {
    id: '2',
    title: 'Second video',
    description: 'Video description',
    image: 'red',
  },
  {
    id: '3',
    title: 'Third video',
    description: 'Video description',
    image: 'green',
  },
  {
    id: '4',
    title: 'Fourth video',
    description: 'Video description',
    image: 'purple',
  },
  {
    id: '5',
    title: 'Fifth video',
    description: 'Video description',
    image: 'yellow',
  },
  {
    id: '6',
    title: 'Sixth video',
    description: 'Video description',
    image: 'gray',
  },
];

let videosCache = new Map();
let videoCache = new Map();
let videoDetailsCache = new Map();
const VIDEO_DELAY = 1;
const VIDEO_DETAILS_DELAY = 1000;
export function fetchVideos() {
  if (videosCache.has(0)) {
    return videosCache.get(0);
  }
  const promise = new Promise((resolve) => {
    setTimeout(() => {
      resolve(videos);
    }, VIDEO_DELAY);
  });
  videosCache.set(0, promise);
  return promise;
}

export function fetchVideo(id) {
  if (videoCache.has(id)) {
    return videoCache.get(id);
  }
  const promise = new Promise((resolve) => {
    setTimeout(() => {
      resolve(videos.find((video) => video.id === id));
    }, VIDEO_DELAY);
  });
  videoCache.set(id, promise);
  return promise;
}

export function fetchVideoDetails(id) {
  if (videoDetailsCache.has(id)) {
    return videoDetailsCache.get(id);
  }
  const promise = new Promise((resolve) => {
    setTimeout(() => {
      resolve(videos.find((video) => video.id === id));
    }, VIDEO_DETAILS_DELAY);
  });
  videoDetailsCache.set(id, promise);
  return promise;
}
```

```js src/router.js hidden
import {useState, createContext, use, useTransition, useLayoutEffect, useEffect, addTransitionType} from "react";

export function Router({ children }) {
  const [isPending, startTransition] = useTransition();
  const [routerState, setRouterState] = useState({pendingNav: () => {}, url: document.location.pathname});
  function navigate(url) {
    startTransition(() => {
      // Transition type for the cause "nav forward"
      addTransitionType('nav-forward');
      go(url);
    });
  }
  function navigateBack(url) {
    startTransition(() => {
      // Transition type for the cause "nav backward"
      addTransitionType('nav-back');
      go(url);
    });
  }

  function go(url) {
    setRouterState({
      url,
      pendingNav() {
        window.history.pushState({}, "", url);
      },
    });
  }

  useEffect(() => {
    function handlePopState() {
      // 因为恢复必须是同步的，所以应该没有动画。
      // Even though it's a transition.
      startTransition(() => {
        setRouterState({
          url: document.location.pathname + document.location.search,
          pendingNav() {
            // Noop. URL has already updated.
          },
        });
      });
    }
    window.addEventListener("popstate", handlePopState);
    return () => {
      window.removeEventListener("popstate", handlePopState);
    };
  }, []);
  const pendingNav = routerState.pendingNav;
  useLayoutEffect(() => {
    pendingNav();
  }, [pendingNav]);

  return (
    <RouterContext
      value={{
        url: routerState.url,
        navigate,
        navigateBack,
        isPending,
        params: {},
      }}
    >
      {children}
    </RouterContext>
  );
}

const RouterContext = createContext({ url: "/", params: {} });

export function useRouter() {
  return use(RouterContext);
}

export function useIsNavPending() {
  return use(RouterContext).isPending;
}

```

```css src/styles.css hidden
@font-face {
  font-family: Optimistic Text;
  src: url(https://react.dev/fonts/Optimistic_Text_W_Rg.woff2) format("woff2");
  font-weight: 400;
  font-style: normal;
  font-display: swap;
}

@font-face {
  font-family: Optimistic Text;
  src: url(https://react.dev/fonts/Optimistic_Text_W_Md.woff2) format("woff2");
  font-weight: 500;
  font-style: normal;
  font-display: swap;
}

@font-face {
  font-family: Optimistic Text;
  src: url(https://react.dev/fonts/Optimistic_Text_W_Bd.woff2) format("woff2");
  font-weight: 600;
  font-style: normal;
  font-display: swap;
}

@font-face {
  font-family: Optimistic Text;
  src: url(https://react.dev/fonts/Optimistic_Text_W_Bd.woff2) format("woff2");
  font-weight: 700;
  font-style: normal;
  font-display: swap;
}

* {
  box-sizing: border-box;
}

html {
  background-image: url(https://react.dev/images/meta-gradient-dark.png);
  background-size: 100%;
  background-position: -100%;
  background-color: rgb(64 71 86);
  background-repeat: no-repeat;
  height: 100%;
  width: 100%;
}

body {
  font-family: Optimistic Text, -apple-system, ui-sans-serif, system-ui, sans-serif, Apple Color Emoji, Segoe UI Emoji, Segoe UI Symbol, Noto Color Emoji;
  padding: 10px 0 10px 0;
  margin: 0;
  display: flex;
  justify-content: center;
}

#root {
  flex: 1 1;
  height: auto;
  background-color: #fff;
  border-radius: 10px;
  max-width: 450px;
  min-height: 600px;
  padding-bottom: 10px;
}

h1 {
  margin-top: 0;
  font-size: 22px;
}

h2 {
  margin-top: 0;
  font-size: 20px;
}

h3 {
  margin-top: 0;
  font-size: 18px;
}

h4 {
  margin-top: 0;
  font-size: 16px;
}

h5 {
  margin-top: 0;
  font-size: 14px;
}

h6 {
  margin-top: 0;
  font-size: 12px;
}

code {
  font-size: 1.2em;
}

ul {
  padding-inline-start: 20px;
}

.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  padding: 0;
  margin: -1px;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  white-space: nowrap;
  border-width: 0;
}

.absolute {
  position: absolute;
}

.overflow-visible {
  overflow: visible;
}

.visible {
  overflow: visible;
}

.fit {
  width: fit-content;
}


/* Layout */
.page {
  display: flex;
  flex-direction: column;
  height: 100%;
}

.top-hero {
  height: 200px;
  display: flex;
  justify-content: center;
  align-items: center;
  background-image: conic-gradient(
      from 90deg at -10% 100%,
      #2b303b 0deg,
      #2b303b 90deg,
      #16181d 1turn
  );
}

.bottom {
  flex: 1;
  overflow: auto;
}

.top-nav {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 0;
  padding: 0 12px;
  top: 0;
  width: 100%;
  height: 44px;
  color: #23272f;
  font-weight: 700;
  font-size: 20px;
  z-index: 100;
  cursor: default;
}

.content {
  padding: 0 12px;
  margin-top: 4px;
}


.loader {
  color: #23272f;
  font-size: 3px;
  width: 1em;
  margin-right: 18px;
  height: 1em;
  border-radius: 50%;
  position: relative;
  text-indent: -9999em;
  animation: loading-spinner 1.3s infinite linear;
  animation-delay: 200ms;
  transform: translateZ(0);
}

@keyframes loading-spinner {
  0%,
  100% {
    box-shadow: 0 -3em 0 0.2em,
    2em -2em 0 0em, 3em 0 0 -1em,
    2em 2em 0 -1em, 0 3em 0 -1em,
    -2em 2em 0 -1em, -3em 0 0 -1em,
    -2em -2em 0 0;
  }
  12.5% {
    box-shadow: 0 -3em 0 0, 2em -2em 0 0.2em,
    3em 0 0 0, 2em 2em 0 -1em, 0 3em 0 -1em,
    -2em 2em 0 -1em, -3em 0 0 -1em,
    -2em -2em 0 -1em;
  }
  25% {
    box-shadow: 0 -3em 0 -0.5em,
    2em -2em 0 0, 3em 0 0 0.2em,
    2em 2em 0 0, 0 3em 0 -1em,
    -2em 2em 0 -1em, -3em 0 0 -1em,
    -2em -2em 0 -1em;
  }
  37.5% {
    box-shadow: 0 -3em 0 -1em, 2em -2em 0 -1em,
    3em 0em 0 0, 2em 2em 0 0.2em, 0 3em 0 0em,
    -2em 2em 0 -1em, -3em 0em 0 -1em, -2em -2em 0 -1em;
  }
  50% {
    box-shadow: 0 -3em 0 -1em, 2em -2em 0 -1em,
    3em 0 0 -1em, 2em 2em 0 0em, 0 3em 0 0.2em,
    -2em 2em 0 0, -3em 0em 0 -1em, -2em -2em 0 -1em;
  }
  62.5% {
    box-shadow: 0 -3em 0 -1em, 2em -2em 0 -1em,
    3em 0 0 -1em, 2em 2em 0 -1em, 0 3em 0 0,
    -2em 2em 0 0.2em, -3em 0 0 0, -2em -2em 0 -1em;
  }
  75% {
    box-shadow: 0em -3em 0 -1em, 2em -2em 0 -1em,
    3em 0em 0 -1em, 2em 2em 0 -1em, 0 3em 0 -1em,
    -2em 2em 0 0, -3em 0em 0 0.2em, -2em -2em 0 0;
  }
  87.5% {
    box-shadow: 0em -3em 0 0, 2em -2em 0 -1em,
    3em 0 0 -1em, 2em 2em 0 -1em, 0 3em 0 -1em,
    -2em 2em 0 0, -3em 0em 0 0, -2em -2em 0 0.2em;
  }
}

/* LikeButton */
.like-button {
  outline-offset: 2px;
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
  width: 2.5rem;
  height: 2.5rem;
  cursor: pointer;
  border-radius: 9999px;
  border: none;
  outline: none 2px;
  color: #5e687e;
  background: none;
}

.like-button:focus {
  color: #a6423a;
  background-color: rgba(166, 66, 58, .05);
}

.like-button:active {
  color: #a6423a;
  background-color: rgba(166, 66, 58, .05);
  transform: scaleX(0.95) scaleY(0.95);
}

.like-button:hover {
  background-color: #f6f7f9;
}

.like-button.liked {
  color: #a6423a;
}

/* Icons */
@keyframes circle {
  0% {
    transform: scale(0);
    stroke-width: 16px;
  }

  50% {
    transform: scale(.5);
    stroke-width: 16px;
  }

  to {
    transform: scale(1);
    stroke-width: 0;
  }
}

.circle {
  color: rgba(166, 66, 58, .5);
  transform-origin: center;
  transition-property: all;
  transition-duration: .15s;
  transition-timing-function: cubic-bezier(.4,0,.2,1);
}

.circle.liked.animate {
  animation: circle .3s forwards;
}

.heart {
  width: 1.5rem;
  height: 1.5rem;
}

.heart.liked {
  transform-origin: center;
  transition-property: all;
  transition-duration: .15s;
  transition-timing-function: cubic-bezier(.4, 0, .2, 1);
}

.heart.liked.animate {
  animation: scale .35s ease-in-out forwards;
}

.control-icon {
  color: hsla(0, 0%, 100%, .5);
  filter:  drop-shadow(0 20px 13px rgba(0, 0, 0, .03)) drop-shadow(0 8px 5px rgba(0, 0, 0, .08));
}

.chevron-left {
  margin-top: 2px;
  rotate: 90deg;
}


/* Video */
.thumbnail {
  position: relative;
  aspect-ratio: 16 / 9;
  display: flex;
  overflow: hidden;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  border-radius: 0.5rem;
  outline-offset: 2px;
  width: 8rem;
  vertical-align: middle;
  background-color: #ffffff;
  background-size: cover;
  user-select: none;
}

.thumbnail.blue {
  background-image: conic-gradient(at top right, #c76a15, #087ea4, #2b3491);
}

.thumbnail.red {
  background-image: conic-gradient(at top right, #c76a15, #a6423a, #2b3491);
}

.thumbnail.green {
  background-image: conic-gradient(at top right, #c76a15, #388f7f, #2b3491);
}

.thumbnail.purple {
  background-image: conic-gradient(at top right, #c76a15, #575fb7, #2b3491);
}

.thumbnail.yellow {
  background-image: conic-gradient(at top right, #c76a15, #FABD62, #2b3491);
}

.thumbnail.gray {
  background-image: conic-gradient(at top right, #c76a15, #4E5769, #2b3491);
}

.video {
  display: flex;
  flex-direction: row;
  gap: 0.75rem;
  align-items: center;
}

.video .link {
  display: flex;
  flex-direction: row;
  flex: 1 1 0;
  gap: 0.125rem;
  outline-offset: 4px;
  cursor: pointer;
}

.video .info {
  display: flex;
  flex-direction: column;
  justify-content: center;
  margin-left: 8px;
  gap: 0.125rem;
}

.video .info:hover {
  text-decoration: underline;
}

.video-title {
  font-size: 15px;
  line-height: 1.25;
  font-weight: 700;
  color: #23272f;
}

.video-description {
  color: #5e687e;
  font-size: 13px;
}

/* Details */
.details .thumbnail {
  position: relative;
  aspect-ratio: 16 / 9;
  display: flex;
  overflow: hidden;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  border-radius: 0.5rem;
  outline-offset: 2px;
  width: 100%;
  vertical-align: middle;
  background-color: #ffffff;
  background-size: cover;
  user-select: none;
}

.video-details-title {
  margin-top: 8px;
}

.video-details-speaker {
  display: flex;
  gap: 8px;
  margin-top: 10px
}

.back {
  display: flex;
  align-items: center;
  margin-left: -5px;
  cursor: pointer;
}

.back:hover {
  text-decoration: underline;
}

.info-title {
  font-size: 1.5rem;
  font-weight: 700;
  line-height: 1.25;
  margin: 8px 0 0 0 ;
}

.info-description {
  margin: 8px 0 0 0;
}

.controls {
  cursor: pointer;
}

.fallback {
  background: #f6f7f8 linear-gradient(to right, #e6e6e6 5%, #cccccc 25%, #e6e6e6 35%) no-repeat;
  background-size: 800px 104px;
  display: block;
  line-height: 1.25;
  margin: 8px 0 0 0;
  border-radius: 5px;
  overflow: hidden;

  animation: 1s linear 1s infinite shimmer;
  animation-delay: 300ms;
  animation-duration: 1s;
  animation-fill-mode: forwards;
  animation-iteration-count: infinite;
  animation-name: shimmer;
  animation-timing-function: linear;
}


.fallback.title {
  width: 130px;
  height: 30px;

}

.fallback.description {
  width: 150px;
  height: 21px;
}

@keyframes shimmer {
  0% {
    background-position: -468px 0;
  }

  100% {
    background-position: 468px 0;
  }
}

.search {
  margin-bottom: 10px;
}
.search-input {
  width: 100%;
  position: relative;
}

.search-icon {
  position: absolute;
  top: 0;
  bottom: 0;
  inset-inline-start: 0;
  display: flex;
  align-items: center;
  padding-inline-start: 1rem;
  pointer-events: none;
  color: #99a1b3;
}

.search-input input {
  display: flex;
  padding-inline-start: 2.75rem;
  padding-top: 10px;
  padding-bottom: 10px;
  width: 100%;
  text-align: start;
  background-color: rgb(235 236 240);
  outline: 2px solid transparent;
  cursor: pointer;
  border: none;
  align-items: center;
  color: rgb(35 39 47);
  border-radius: 9999px;
  vertical-align: middle;
  font-size: 15px;
}

.search-input input:hover, .search-input input:active {
  background-color: rgb(235 236 240/ 0.8);
  color: rgb(35 39 47/ 0.8);
}

/* Home */
.video-list {
  position: relative;
}

.video-list .videos {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  overflow-y: auto;
  height: 100%;
}
```


```css src/animations.css
/* Slide the fallback down */
::view-transition-old(.slide-down) {
    animation: 150ms ease-out both fade-out, 150ms ease-out both slide-down;
}

/* Slide the content up */
::view-transition-new(.slide-up) {
    animation: 210ms ease-in 150ms both fade-in, 400ms ease-in both slide-up;
}

/* Define the new keyframes */
@keyframes slide-up {
    from {
        transform: translateY(10px);
    }
    to {
        transform: translateY(0);
    }
}

@keyframes slide-down {
    from {
        transform: translateY(0);
    }
    to {
        transform: translateY(10px);
    }
}

/* Previously defined animations below */

/* Animations for view transition classed added by transition type */
::view-transition-old(.slide-forward) {
    /* when sliding forward, the "old" page should slide out to left. */
    animation: 150ms cubic-bezier(0.4, 0, 1, 1) both fade-out,
    400ms cubic-bezier(0.4, 0, 0.2, 1) both slide-to-left;
}

::view-transition-new(.slide-forward) {
    /* when sliding forward, the "new" page should slide in from right. */
    animation: 210ms cubic-bezier(0, 0, 0.2, 1) 150ms both fade-in,
    400ms cubic-bezier(0.4, 0, 0.2, 1) both slide-from-right;
}

::view-transition-old(.slide-back) {
    /* when sliding back, the "old" page should slide out to right. */
    animation: 150ms cubic-bezier(0.4, 0, 1, 1) both fade-out,
    400ms cubic-bezier(0.4, 0, 0.2, 1) both slide-to-right;
}

::view-transition-new(.slide-back) {
    /* when sliding back, the "new" page should slide in from left. */
    animation: 210ms cubic-bezier(0, 0, 0.2, 1) 150ms both fade-in,
    400ms cubic-bezier(0.4, 0, 0.2, 1) both slide-from-left;
}

/* Keyframes to support our animations above. */
@keyframes fade-in {
    from {
        opacity: 0;
    }
}

@keyframes fade-out {
    to {
        opacity: 0;
    }
}

@keyframes slide-to-right {
    to {
        transform: translateX(50px);
    }
}

@keyframes slide-from-right {
    from {
        transform: translateX(50px);
    }
    to {
        transform: translateX(0);
    }
}

@keyframes slide-to-left {
    to {
        transform: translateX(-50px);
    }
}

@keyframes slide-from-left {
    from {
        transform: translateX(-50px);
    }
    to {
        transform: translateX(0);
    }
}

/* Default .slow-fade. */
::view-transition-old(.slow-fade) {
    animation-duration: 500ms;
}

::view-transition-new(.slow-fade) {
    animation-duration: 500ms;
}
```

```js src/index.js hidden
import React, {StrictMode} from 'react';
import {createRoot} from 'react-dom/client';
import './styles.css';
import './animations.css';

import App from './App';
import {Router} from './router';

const root = createRoot(document.getElementById('root'));
root.render(
  <StrictMode>
    <Router>
      <App />
    </Router>
  </StrictMode>
);
```

```json package.json hidden
{
  "dependencies": {
    "react": "canary",
    "react-dom": "canary",
    "react-scripts": "latest"
  },
  "scripts": {
    "start": "react-scripts start",
    "build": "react-scripts build",
    "test": "react-scripts test --env=jsdom",
    "eject": "react-scripts eject"
  }
}
```

</Sandpack>


### 为列表添加动画 {/*animating-lists*/}

你还可以使用 `<ViewTransition>` 为重新排序的项目列表添加动画，例如在可搜索的项目列表中：

```js {3,5}
<div className="videos">
  {filteredVideos.map((video) => (
    <ViewTransition key={video.id}>
      <Video video={video} />
    </ViewTransition>
  ))}
</div>
```

要激活 ViewTransition，我们可以使用 `useDeferredValue`：

```js {2}
const [searchText, setSearchText] = useState('');
const deferredSearchText = useDeferredValue(searchText);
const filteredVideos = filterVideos(videos, deferredSearchText);
```

Now the items animate as you type in the search bar:

<Sandpack>

```js src/App.js hidden
import { ViewTransition } from "react";
import Details from "./Details";
import Home from "./Home";
import { useRouter } from "./router";

export default function App() {
  const { url } = useRouter();

  // Default slow-fade animation.
  return (
    <ViewTransition default="slow-fade">
      {url === "/" ? <Home /> : <Details />}
    </ViewTransition>
  );
}
```

```js src/Details.js hidden
import { use, Suspense, ViewTransition } from "react";
import { fetchVideo, fetchVideoDetails } from "./data";
import { Thumbnail, VideoControls } from "./Videos";
import { useRouter } from "./router";
import Layout from "./Layout";
import { ChevronLeft } from "./Icons";

function VideoDetails({id}) {
  // Animate from Suspense fallback to content
  return (
    <Suspense
      fallback={
        // Animate the fallback down.
        <ViewTransition exit="slide-down">
          <VideoInfoFallback />
        </ViewTransition>
      }
    >
      {/* Animate the content up */}
      <ViewTransition enter="slide-up">
        <VideoInfo id={id} />
      </ViewTransition>
    </Suspense>
  );
}

function VideoInfoFallback() {
  return (
    <>
      <div className="fallback title"></div>
      <div className="fallback description"></div>
    </>
  );
}

export default function Details() {
  const { url, navigateBack } = useRouter();
  const videoId = url.split("/").pop();
  const video = use(fetchVideo(videoId));

  return (
    <Layout
      heading={
        <div
          className="fit back"
          onClick={() => {
            navigateBack("/");
          }}
        >
          <ChevronLeft /> Back
        </div>
      }
    >
      <div className="details">
        <Thumbnail video={video} large>
          <VideoControls />
        </Thumbnail>
        <VideoDetails id={video.id} />
      </div>
    </Layout>
  );
}

function VideoInfo({ id }) {
  const details = use(fetchVideoDetails(id));
  return (
    <>
      <p className="info-title">{details.title}</p>
      <p className="info-description">{details.description}</p>
    </>
  );
}
```

```js src/Home.js
import { useId, useState, use, useDeferredValue, ViewTransition } from "react";import { Video } from "./Videos";import Layout from "./Layout";import { fetchVideos } from "./data";import { IconSearch } from "./Icons";

function SearchList({searchText, videos}) {
  // 通过 useDeferredValue来激活(何时) 
  const deferredSearchText = useDeferredValue(searchText);
  const filteredVideos = filterVideos(videos, deferredSearchText);
  return (
    <div className="video-list">
      <div className="videos">
        {filteredVideos.map((video) => (
          // 对列表中的每一个子项目进行动画（何地）
          <ViewTransition key={video.id}>
            <Video video={video} />
          </ViewTransition>
        ))}
      </div>
      {filteredVideos.length === 0 && (
        <div className="no-results">No results</div>
      )}
    </div>
  );
}

export default function Home() {
  const videos = use(fetchVideos());
  const count = videos.length;
  const [searchText, setSearchText] = useState('');

  return (
    <Layout heading={<div className="fit">{count} Videos</div>}>
      <SearchInput value={searchText} onChange={setSearchText} />
      <SearchList videos={videos} searchText={searchText} />
    </Layout>
  );
}

function SearchInput({ value, onChange }) {
  const id = useId();
  return (
    <form className="search" onSubmit={(e) => e.preventDefault()}>
      <label htmlFor={id} className="sr-only">
        Search
      </label>
      <div className="search-input">
        <div className="search-icon">
          <IconSearch />
        </div>
        <input
          type="text"
          id={id}
          placeholder="Search"
          value={value}
          onChange={(e) => onChange(e.target.value)}
        />
      </div>
    </form>
  );
}

function filterVideos(videos, query) {
  const keywords = query
    .toLowerCase()
    .split(" ")
    .filter((s) => s !== "");
  if (keywords.length === 0) {
    return videos;
  }
  return videos.filter((video) => {
    const words = (video.title + " " + video.description)
      .toLowerCase()
      .split(" ");
    return keywords.every((kw) => words.some((w) => w.includes(kw)));
  });
}
```

```js src/Icons.js hidden
export function ChevronLeft() {
  return (
    <svg
      className="chevron-left"
      xmlns="http://www.w3.org/2000/svg"
      width="20"
      height="20"
      viewBox="0 0 20 20">
      <g fill="none" fillRule="evenodd" transform="translate(-446 -398)">
        <path
          fill="currentColor"
          fillRule="nonzero"
          d="M95.8838835,240.366117 C95.3957281,239.877961 94.6042719,239.877961 94.1161165,240.366117 C93.6279612,240.854272 93.6279612,241.645728 94.1161165,242.133883 L98.6161165,246.633883 C99.1042719,247.122039 99.8957281,247.122039 100.383883,246.633883 L104.883883,242.133883 C105.372039,241.645728 105.372039,240.854272 104.883883,240.366117 C104.395728,239.877961 103.604272,239.877961 103.116117,240.366117 L99.5,243.982233 L95.8838835,240.366117 Z"
          transform="translate(356.5 164.5)"
        />
        <polygon points="446 418 466 418 466 398 446 398" />
      </g>
    </svg>
  );
}

export function PauseIcon() {
  return (
    <svg
      className="control-icon"
      style={{padding: '4px'}}
      width="100"
      height="100"
      viewBox="0 0 512 512"
      fill="none"
      xmlns="http://www.w3.org/2000/svg">
      <path
        fillRule="evenodd"
        clipRule="evenodd"
        d="M256 0C114.617 0 0 114.615 0 256s114.617 256 256 256 256-114.615 256-256S397.383 0 256 0zm-32 320c0 8.836-7.164 16-16 16h-32c-8.836 0-16-7.164-16-16V192c0-8.836 7.164-16 16-16h32c8.836 0 16 7.164 16 16v128zm128 0c0 8.836-7.164 16-16 16h-32c-8.836 0-16-7.164-16-16V192c0-8.836 7.164-16 16-16h32c8.836 0 16 7.164 16 16v128z"
        fill="currentColor"
      />
    </svg>
  );
}

export function PlayIcon() {
  return (
    <svg
      className="control-icon"
      width="100"
      height="100"
      viewBox="0 0 72 72"
      fill="none"
      xmlns="http://www.w3.org/2000/svg">
      <path
        fillRule="evenodd"
        clipRule="evenodd"
        d="M36 69C54.2254 69 69 54.2254 69 36C69 17.7746 54.2254 3 36 3C17.7746 3 3 17.7746 3 36C3 54.2254 17.7746 69 36 69ZM52.1716 38.6337L28.4366 51.5801C26.4374 52.6705 24 51.2235 24 48.9464V23.0536C24 20.7764 26.4374 19.3295 28.4366 20.4199L52.1716 33.3663C54.2562 34.5034 54.2562 37.4966 52.1716 38.6337Z"
        fill="currentColor"
      />
    </svg>
  );
}
export function Heart({liked, animate}) {
  return (
    <>
      <svg
        className="absolute overflow-visible"
        viewBox="0 0 24 24"
        fill="none"
        xmlns="http://www.w3.org/2000/svg">
        <circle
          className={`circle ${liked ? 'liked' : ''} ${animate ? 'animate' : ''}`}
          cx="12"
          cy="12"
          r="11.5"
          fill="transparent"
          strokeWidth="0"
          stroke="currentColor"
        />
      </svg>

      <svg
        className={`heart ${liked ? 'liked' : ''} ${animate ? 'animate' : ''}`}
        viewBox="0 0 24 24"
        fill="none"
        xmlns="http://www.w3.org/2000/svg">
        {liked ? (
          <path
            d="M12 23a.496.496 0 0 1-.26-.074C7.023 19.973 0 13.743 0 8.68c0-4.12 2.322-6.677 6.058-6.677 2.572 0 5.108 2.387 5.134 2.41l.808.771.808-.771C12.834 4.387 15.367 2 17.935 2 21.678 2 24 4.558 24 8.677c0 5.06-7.022 11.293-11.74 14.246a.496.496 0 0 1-.26.074V23z"
            fill="currentColor"
          />
        ) : (
          <path
            fillRule="evenodd"
            clipRule="evenodd"
            d="m12 5.184-.808-.771-.004-.004C11.065 4.299 8.522 2.003 6 2.003c-3.736 0-6 2.558-6 6.677 0 4.47 5.471 9.848 10 13.079.602.43 1.187.82 1.74 1.167A.497.497 0 0 0 12 23v-.003c.09 0 .182-.026.26-.074C16.977 19.97 24 13.737 24 8.677 24 4.557 21.743 2 18 2c-2.569 0-5.166 2.387-5.192 2.413L12 5.184zm-.002 15.525c2.071-1.388 4.477-3.342 6.427-5.47C20.72 12.733 22 10.401 22 8.677c0-1.708-.466-2.855-1.087-3.55C20.316 4.459 19.392 4 18 4c-.726 0-1.63.364-2.5.9-.67.412-1.148.82-1.266.92-.03.025-.037.031-.019.014l-.013.013L12 7.949 9.832 5.88a10.08 10.08 0 0 0-1.33-.977C7.633 4.367 6.728 4.003 6 4.003c-1.388 0-2.312.459-2.91 1.128C2.466 5.826 2 6.974 2 8.68c0 1.726 1.28 4.058 3.575 6.563 1.948 2.127 4.352 4.078 6.423 5.466z"
            fill="currentColor"
          />
        )}
      </svg>
    </>
  );
}

export function IconSearch(props) {
  return (
    <svg width="1em" height="1em" viewBox="0 0 20 20">
      <path
        d="M14.386 14.386l4.0877 4.0877-4.0877-4.0877c-2.9418 2.9419-7.7115 2.9419-10.6533 0-2.9419-2.9418-2.9419-7.7115 0-10.6533 2.9418-2.9419 7.7115-2.9419 10.6533 0 2.9419 2.9418 2.9419 7.7115 0 10.6533z"
        stroke="currentColor"
        fill="none"
        strokeWidth="2"
        fillRule="evenodd"
        strokeLinecap="round"
        strokeLinejoin="round"></path>
    </svg>
  );
}
```

```js src/Layout.js hidden
import {ViewTransition} from 'react';
import { useIsNavPending } from "./router";

export default function Page({ heading, children }) {
  const isPending = useIsNavPending();
  return (
    <div className="page">
      <div className="top">
        <div className="top-nav">
          {/* Custom classes based on transition type. */}
          <ViewTransition
            name="nav"
            share={{
              'nav-forward': 'slide-forward',
              'nav-back': 'slide-back',
            }}>
            {heading}
          </ViewTransition>
          {isPending && <span className="loader"></span>}
        </div>
      </div>
      {/* Opt-out of ViewTransition for the content. */}
      {/* Content can define it's own ViewTransition. */}
      <ViewTransition default="none">
        <div className="bottom">
          <div className="content">{children}</div>
        </div>
      </ViewTransition>
    </div>
  );
}
```

```js src/LikeButton.js hidden
import {useState} from 'react';
import {Heart} from './Icons';

// A hack since we don't actually have a backend.
// Unlike local state, this survives videos being filtered.
const likedVideos = new Set();

export default function LikeButton({video}) {
  const [isLiked, setIsLiked] = useState(() => likedVideos.has(video.id));
  const [animate, setAnimate] = useState(false);
  return (
    <button
      className={`like-button ${isLiked && 'liked'}`}
      aria-label={isLiked ? 'Unsave' : 'Save'}
      onClick={() => {
        const nextIsLiked = !isLiked;
        if (nextIsLiked) {
          likedVideos.add(video.id);
        } else {
          likedVideos.delete(video.id);
        }
        setAnimate(true);
        setIsLiked(nextIsLiked);
      }}>
      <Heart liked={isLiked} animate={animate} />
    </button>
  );
}
```

```js src/Videos.js hidden
import { useState, ViewTransition } from "react";
import LikeButton from "./LikeButton";
import { useRouter } from "./router";
import { PauseIcon, PlayIcon } from "./Icons";
import { startTransition } from "react";

export function Thumbnail({ video, children }) {
  // Add a name to animate with a shared element transition.
  // This uses the default animation, no additional css needed.
  return (
    <ViewTransition name={`video-${video.id}`}>
      <div
        aria-hidden="true"
        tabIndex={-1}
        className={`thumbnail ${video.image}`}
      >
        {children}
      </div>
    </ViewTransition>
  );
}

export function VideoControls() {
  const [isPlaying, setIsPlaying] = useState(false);

  return (
    <span
      className="controls"
      onClick={() =>
        startTransition(() => {
          setIsPlaying((p) => !p);
        })
      }
    >
      {isPlaying ? <PauseIcon /> : <PlayIcon />}
    </span>
  );
}

export function Video({ video }) {
  const { navigate } = useRouter();

  return (
    <div className="video">
      <div
        className="link"
        onClick={(e) => {
          e.preventDefault();
          navigate(`/video/${video.id}`);
        }}
      >
        <Thumbnail video={video}></Thumbnail>

        <div className="info">
          <div className="video-title">{video.title}</div>
          <div className="video-description">{video.description}</div>
        </div>
      </div>
      <LikeButton video={video} />
    </div>
  );
}
```


```js src/data.js hidden
const videos = [
  {
    id: '1',
    title: 'First video',
    description: 'Video description',
    image: 'blue',
  },
  {
    id: '2',
    title: 'Second video',
    description: 'Video description',
    image: 'red',
  },
  {
    id: '3',
    title: 'Third video',
    description: 'Video description',
    image: 'green',
  },
  {
    id: '4',
    title: 'Fourth video',
    description: 'Video description',
    image: 'purple',
  },
  {
    id: '5',
    title: 'Fifth video',
    description: 'Video description',
    image: 'yellow',
  },
  {
    id: '6',
    title: 'Sixth video',
    description: 'Video description',
    image: 'gray',
  },
];

let videosCache = new Map();
let videoCache = new Map();
let videoDetailsCache = new Map();
const VIDEO_DELAY = 1;
const VIDEO_DETAILS_DELAY = 1000;
export function fetchVideos() {
  if (videosCache.has(0)) {
    return videosCache.get(0);
  }
  const promise = new Promise((resolve) => {
    setTimeout(() => {
      resolve(videos);
    }, VIDEO_DELAY);
  });
  videosCache.set(0, promise);
  return promise;
}

export function fetchVideo(id) {
  if (videoCache.has(id)) {
    return videoCache.get(id);
  }
  const promise = new Promise((resolve) => {
    setTimeout(() => {
      resolve(videos.find((video) => video.id === id));
    }, VIDEO_DELAY);
  });
  videoCache.set(id, promise);
  return promise;
}

export function fetchVideoDetails(id) {
  if (videoDetailsCache.has(id)) {
    return videoDetailsCache.get(id);
  }
  const promise = new Promise((resolve) => {
    setTimeout(() => {
      resolve(videos.find((video) => video.id === id));
    }, VIDEO_DETAILS_DELAY);
  });
  videoDetailsCache.set(id, promise);
  return promise;
}
```

```js src/router.js hidden
import {useState, createContext, use, useTransition, useLayoutEffect, useEffect, addTransitionType} from "react";

export function Router({ children }) {
  const [isPending, startTransition] = useTransition();
  const [routerState, setRouterState] = useState({pendingNav: () => {}, url: document.location.pathname});
  function navigate(url) {
    startTransition(() => {
      // Transition type for the cause "nav forward"
      addTransitionType('nav-forward');
      go(url);
    });
  }
  function navigateBack(url) {
    startTransition(() => {
      // Transition type for the cause "nav backward"
      addTransitionType('nav-back');
      go(url);
    });
  }

  function go(url) {
    setRouterState({
      url,
      pendingNav() {
        window.history.pushState({}, "", url);
      },
    });
  }

  useEffect(() => {
    function handlePopState() {
      // 因为恢复必须是同步的，所以应该没有动画。
      // Even though it's a transition.
      startTransition(() => {
        setRouterState({
          url: document.location.pathname + document.location.search,
          pendingNav() {
            // Noop. URL has already updated.
          },
        });
      });
    }
    window.addEventListener("popstate", handlePopState);
    return () => {
      window.removeEventListener("popstate", handlePopState);
    };
  }, []);
  const pendingNav = routerState.pendingNav;
  useLayoutEffect(() => {
    pendingNav();
  }, [pendingNav]);

  return (
    <RouterContext
      value={{
        url: routerState.url,
        navigate,
        navigateBack,
        isPending,
        params: {},
      }}
    >
      {children}
    </RouterContext>
  );
}

const RouterContext = createContext({ url: "/", params: {} });

export function useRouter() {
  return use(RouterContext);
}

export function useIsNavPending() {
  return use(RouterContext).isPending;
}

```

```css src/styles.css hidden
@font-face {
  font-family: Optimistic Text;
  src: url(https://react.dev/fonts/Optimistic_Text_W_Rg.woff2) format("woff2");
  font-weight: 400;
  font-style: normal;
  font-display: swap;
}

@font-face {
  font-family: Optimistic Text;
  src: url(https://react.dev/fonts/Optimistic_Text_W_Md.woff2) format("woff2");
  font-weight: 500;
  font-style: normal;
  font-display: swap;
}

@font-face {
  font-family: Optimistic Text;
  src: url(https://react.dev/fonts/Optimistic_Text_W_Bd.woff2) format("woff2");
  font-weight: 600;
  font-style: normal;
  font-display: swap;
}

@font-face {
  font-family: Optimistic Text;
  src: url(https://react.dev/fonts/Optimistic_Text_W_Bd.woff2) format("woff2");
  font-weight: 700;
  font-style: normal;
  font-display: swap;
}

* {
  box-sizing: border-box;
}

html {
  background-image: url(https://react.dev/images/meta-gradient-dark.png);
  background-size: 100%;
  background-position: -100%;
  background-color: rgb(64 71 86);
  background-repeat: no-repeat;
  height: 100%;
  width: 100%;
}

body {
  font-family: Optimistic Text, -apple-system, ui-sans-serif, system-ui, sans-serif, Apple Color Emoji, Segoe UI Emoji, Segoe UI Symbol, Noto Color Emoji;
  padding: 10px 0 10px 0;
  margin: 0;
  display: flex;
  justify-content: center;
}

#root {
  flex: 1 1;
  height: auto;
  background-color: #fff;
  border-radius: 10px;
  max-width: 450px;
  min-height: 600px;
  padding-bottom: 10px;
}

h1 {
  margin-top: 0;
  font-size: 22px;
}

h2 {
  margin-top: 0;
  font-size: 20px;
}

h3 {
  margin-top: 0;
  font-size: 18px;
}

h4 {
  margin-top: 0;
  font-size: 16px;
}

h5 {
  margin-top: 0;
  font-size: 14px;
}

h6 {
  margin-top: 0;
  font-size: 12px;
}

code {
  font-size: 1.2em;
}

ul {
  padding-inline-start: 20px;
}

.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  padding: 0;
  margin: -1px;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  white-space: nowrap;
  border-width: 0;
}

.absolute {
  position: absolute;
}

.overflow-visible {
  overflow: visible;
}

.visible {
  overflow: visible;
}

.fit {
  width: fit-content;
}


/* Layout */
.page {
  display: flex;
  flex-direction: column;
  height: 100%;
}

.top-hero {
  height: 200px;
  display: flex;
  justify-content: center;
  align-items: center;
  background-image: conic-gradient(
      from 90deg at -10% 100%,
      #2b303b 0deg,
      #2b303b 90deg,
      #16181d 1turn
  );
}

.bottom {
  flex: 1;
  overflow: auto;
}

.top-nav {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 0;
  padding: 0 12px;
  top: 0;
  width: 100%;
  height: 44px;
  color: #23272f;
  font-weight: 700;
  font-size: 20px;
  z-index: 100;
  cursor: default;
}

.content {
  padding: 0 12px;
  margin-top: 4px;
}


.loader {
  color: #23272f;
  font-size: 3px;
  width: 1em;
  margin-right: 18px;
  height: 1em;
  border-radius: 50%;
  position: relative;
  text-indent: -9999em;
  animation: loading-spinner 1.3s infinite linear;
  animation-delay: 200ms;
  transform: translateZ(0);
}

@keyframes loading-spinner {
  0%,
  100% {
    box-shadow: 0 -3em 0 0.2em,
    2em -2em 0 0em, 3em 0 0 -1em,
    2em 2em 0 -1em, 0 3em 0 -1em,
    -2em 2em 0 -1em, -3em 0 0 -1em,
    -2em -2em 0 0;
  }
  12.5% {
    box-shadow: 0 -3em 0 0, 2em -2em 0 0.2em,
    3em 0 0 0, 2em 2em 0 -1em, 0 3em 0 -1em,
    -2em 2em 0 -1em, -3em 0 0 -1em,
    -2em -2em 0 -1em;
  }
  25% {
    box-shadow: 0 -3em 0 -0.5em,
    2em -2em 0 0, 3em 0 0 0.2em,
    2em 2em 0 0, 0 3em 0 -1em,
    -2em 2em 0 -1em, -3em 0 0 -1em,
    -2em -2em 0 -1em;
  }
  37.5% {
    box-shadow: 0 -3em 0 -1em, 2em -2em 0 -1em,
    3em 0em 0 0, 2em 2em 0 0.2em, 0 3em 0 0em,
    -2em 2em 0 -1em, -3em 0em 0 -1em, -2em -2em 0 -1em;
  }
  50% {
    box-shadow: 0 -3em 0 -1em, 2em -2em 0 -1em,
    3em 0 0 -1em, 2em 2em 0 0em, 0 3em 0 0.2em,
    -2em 2em 0 0, -3em 0em 0 -1em, -2em -2em 0 -1em;
  }
  62.5% {
    box-shadow: 0 -3em 0 -1em, 2em -2em 0 -1em,
    3em 0 0 -1em, 2em 2em 0 -1em, 0 3em 0 0,
    -2em 2em 0 0.2em, -3em 0 0 0, -2em -2em 0 -1em;
  }
  75% {
    box-shadow: 0em -3em 0 -1em, 2em -2em 0 -1em,
    3em 0em 0 -1em, 2em 2em 0 -1em, 0 3em 0 -1em,
    -2em 2em 0 0, -3em 0em 0 0.2em, -2em -2em 0 0;
  }
  87.5% {
    box-shadow: 0em -3em 0 0, 2em -2em 0 -1em,
    3em 0 0 -1em, 2em 2em 0 -1em, 0 3em 0 -1em,
    -2em 2em 0 0, -3em 0em 0 0, -2em -2em 0 0.2em;
  }
}

/* LikeButton */
.like-button {
  outline-offset: 2px;
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
  width: 2.5rem;
  height: 2.5rem;
  cursor: pointer;
  border-radius: 9999px;
  border: none;
  outline: none 2px;
  color: #5e687e;
  background: none;
}

.like-button:focus {
  color: #a6423a;
  background-color: rgba(166, 66, 58, .05);
}

.like-button:active {
  color: #a6423a;
  background-color: rgba(166, 66, 58, .05);
  transform: scaleX(0.95) scaleY(0.95);
}

.like-button:hover {
  background-color: #f6f7f9;
}

.like-button.liked {
  color: #a6423a;
}

/* Icons */
@keyframes circle {
  0% {
    transform: scale(0);
    stroke-width: 16px;
  }

  50% {
    transform: scale(.5);
    stroke-width: 16px;
  }

  to {
    transform: scale(1);
    stroke-width: 0;
  }
}

.circle {
  color: rgba(166, 66, 58, .5);
  transform-origin: center;
  transition-property: all;
  transition-duration: .15s;
  transition-timing-function: cubic-bezier(.4,0,.2,1);
}

.circle.liked.animate {
  animation: circle .3s forwards;
}

.heart {
  width: 1.5rem;
  height: 1.5rem;
}

.heart.liked {
  transform-origin: center;
  transition-property: all;
  transition-duration: .15s;
  transition-timing-function: cubic-bezier(.4, 0, .2, 1);
}

.heart.liked.animate {
  animation: scale .35s ease-in-out forwards;
}

.control-icon {
  color: hsla(0, 0%, 100%, .5);
  filter:  drop-shadow(0 20px 13px rgba(0, 0, 0, .03)) drop-shadow(0 8px 5px rgba(0, 0, 0, .08));
}

.chevron-left {
  margin-top: 2px;
  rotate: 90deg;
}


/* Video */
.thumbnail {
  position: relative;
  aspect-ratio: 16 / 9;
  display: flex;
  overflow: hidden;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  border-radius: 0.5rem;
  outline-offset: 2px;
  width: 8rem;
  vertical-align: middle;
  background-color: #ffffff;
  background-size: cover;
  user-select: none;
}

.thumbnail.blue {
  background-image: conic-gradient(at top right, #c76a15, #087ea4, #2b3491);
}

.thumbnail.red {
  background-image: conic-gradient(at top right, #c76a15, #a6423a, #2b3491);
}

.thumbnail.green {
  background-image: conic-gradient(at top right, #c76a15, #388f7f, #2b3491);
}

.thumbnail.purple {
  background-image: conic-gradient(at top right, #c76a15, #575fb7, #2b3491);
}

.thumbnail.yellow {
  background-image: conic-gradient(at top right, #c76a15, #FABD62, #2b3491);
}

.thumbnail.gray {
  background-image: conic-gradient(at top right, #c76a15, #4E5769, #2b3491);
}

.video {
  display: flex;
  flex-direction: row;
  gap: 0.75rem;
  align-items: center;
}

.video .link {
  display: flex;
  flex-direction: row;
  flex: 1 1 0;
  gap: 0.125rem;
  outline-offset: 4px;
  cursor: pointer;
}

.video .info {
  display: flex;
  flex-direction: column;
  justify-content: center;
  margin-left: 8px;
  gap: 0.125rem;
}

.video .info:hover {
  text-decoration: underline;
}

.video-title {
  font-size: 15px;
  line-height: 1.25;
  font-weight: 700;
  color: #23272f;
}

.video-description {
  color: #5e687e;
  font-size: 13px;
}

/* Details */
.details .thumbnail {
  position: relative;
  aspect-ratio: 16 / 9;
  display: flex;
  overflow: hidden;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  border-radius: 0.5rem;
  outline-offset: 2px;
  width: 100%;
  vertical-align: middle;
  background-color: #ffffff;
  background-size: cover;
  user-select: none;
}

.video-details-title {
  margin-top: 8px;
}

.video-details-speaker {
  display: flex;
  gap: 8px;
  margin-top: 10px
}

.back {
  display: flex;
  align-items: center;
  margin-left: -5px;
  cursor: pointer;
}

.back:hover {
  text-decoration: underline;
}

.info-title {
  font-size: 1.5rem;
  font-weight: 700;
  line-height: 1.25;
  margin: 8px 0 0 0 ;
}

.info-description {
  margin: 8px 0 0 0;
}

.controls {
  cursor: pointer;
}

.fallback {
  background: #f6f7f8 linear-gradient(to right, #e6e6e6 5%, #cccccc 25%, #e6e6e6 35%) no-repeat;
  background-size: 800px 104px;
  display: block;
  line-height: 1.25;
  margin: 8px 0 0 0;
  border-radius: 5px;
  overflow: hidden;

  animation: 1s linear 1s infinite shimmer;
  animation-delay: 300ms;
  animation-duration: 1s;
  animation-fill-mode: forwards;
  animation-iteration-count: infinite;
  animation-name: shimmer;
  animation-timing-function: linear;
}


.fallback.title {
  width: 130px;
  height: 30px;

}

.fallback.description {
  width: 150px;
  height: 21px;
}

@keyframes shimmer {
  0% {
    background-position: -468px 0;
  }

  100% {
    background-position: 468px 0;
  }
}

.search {
  margin-bottom: 10px;
}
.search-input {
  width: 100%;
  position: relative;
}

.search-icon {
  position: absolute;
  top: 0;
  bottom: 0;
  inset-inline-start: 0;
  display: flex;
  align-items: center;
  padding-inline-start: 1rem;
  pointer-events: none;
  color: #99a1b3;
}

.search-input input {
  display: flex;
  padding-inline-start: 2.75rem;
  padding-top: 10px;
  padding-bottom: 10px;
  width: 100%;
  text-align: start;
  background-color: rgb(235 236 240);
  outline: 2px solid transparent;
  cursor: pointer;
  border: none;
  align-items: center;
  color: rgb(35 39 47);
  border-radius: 9999px;
  vertical-align: middle;
  font-size: 15px;
}

.search-input input:hover, .search-input input:active {
  background-color: rgb(235 236 240/ 0.8);
  color: rgb(35 39 47/ 0.8);
}

/* Home */
.video-list {
  position: relative;
}

.video-list .videos {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  overflow-y: auto;
  height: 100%;
}
```


```css src/animations.css
/* No additional animations needed */









/* Previously defined animations below */






/* Slide animation for Suspense */
::view-transition-old(.slide-down) {
    animation: 150ms ease-out both fade-out, 150ms ease-out both slide-down;
}

::view-transition-new(.slide-up) {
    animation: 210ms ease-in 150ms both fade-in, 400ms ease-in both slide-up;
}

/* Animations for view transition classed added by transition type */
::view-transition-old(.slide-forward) {
    /* when sliding forward, the "old" page should slide out to left. */
    animation: 150ms cubic-bezier(0.4, 0, 1, 1) both fade-out,
    400ms cubic-bezier(0.4, 0, 0.2, 1) both slide-to-left;
}

::view-transition-new(.slide-forward) {
    /* when sliding forward, the "new" page should slide in from right. */
    animation: 210ms cubic-bezier(0, 0, 0.2, 1) 150ms both fade-in,
    400ms cubic-bezier(0.4, 0, 0.2, 1) both slide-from-right;
}

::view-transition-old(.slide-back) {
    /* when sliding back, the "old" page should slide out to right. */
    animation: 150ms cubic-bezier(0.4, 0, 1, 1) both fade-out,
    400ms cubic-bezier(0.4, 0, 0.2, 1) both slide-to-right;
}

::view-transition-new(.slide-back) {
    /* when sliding back, the "new" page should slide in from left. */
    animation: 210ms cubic-bezier(0, 0, 0.2, 1) 150ms both fade-in,
    400ms cubic-bezier(0.4, 0, 0.2, 1) both slide-from-left;
}

/* Keyframes to support our animations above. */
@keyframes slide-up {
    from {
        transform: translateY(10px);
    }
    to {
        transform: translateY(0);
    }
}

@keyframes slide-down {
    from {
        transform: translateY(0);
    }
    to {
        transform: translateY(10px);
    }
}

@keyframes fade-in {
    from {
        opacity: 0;
    }
}

@keyframes fade-out {
    to {
        opacity: 0;
    }
}

@keyframes slide-to-right {
    to {
        transform: translateX(50px);
    }
}

@keyframes slide-from-right {
    from {
        transform: translateX(50px);
    }
    to {
        transform: translateX(0);
    }
}

@keyframes slide-to-left {
    to {
        transform: translateX(-50px);
    }
}

@keyframes slide-from-left {
    from {
        transform: translateX(-50px);
    }
    to {
        transform: translateX(0);
    }
}


/* Default .slow-fade. */
::view-transition-old(.slow-fade) {
    animation-duration: 500ms;
}

::view-transition-new(.slow-fade) {
    animation-duration: 500ms;
}
```

```js src/index.js hidden
import React, {StrictMode} from 'react';
import {createRoot} from 'react-dom/client';
import './styles.css';
import './animations.css';

import App from './App';
import {Router} from './router';

const root = createRoot(document.getElementById('root'));
root.render(
  <StrictMode>
    <Router>
      <App />
    </Router>
  </StrictMode>
);
```

```json package.json hidden
{
  "dependencies": {
    "react": "canary",
    "react-dom": "canary",
    "react-scripts": "latest"
  },
  "scripts": {
    "start": "react-scripts start",
    "build": "react-scripts build",
    "test": "react-scripts test --env=jsdom",
    "eject": "react-scripts eject"
  }
}
```

</Sandpack>

### Final result {/*final-result*/}

By adding a few `<ViewTransition>` components and a few lines of CSS, we were able to add all the animations above into the final result.

We're excited about View Transitions and think they will level up the apps you're able to build. They're ready to start trying today in the experimental channel of React releases.

Let's remove the slow fade, and take a look at the final result:

<Sandpack>

```js src/App.js
import {ViewTransition} from 'react'; import Details from './Details'; import Home from './Home'; import {useRouter} from './router';

export default function App() {
  const {url} = useRouter();

  // Animate with a cross fade between pages.
  return (
    <ViewTransition key={url}>
      {url === '/' ? <Home /> : <Details />}
    </ViewTransition>
  );
}
```

```js src/Details.js
import { use, Suspense, ViewTransition } from "react"; import { fetchVideo, fetchVideoDetails } from "./data"; import { Thumbnail, VideoControls } from "./Videos"; import { useRouter } from "./router"; import Layout from "./Layout"; import { ChevronLeft } from "./Icons";

function VideoDetails({id}) {
  // Animate from Suspense fallback to content
  return (
    <Suspense
      fallback={
        // Animate the fallback down.
        <ViewTransition exit="slide-down">
          <VideoInfoFallback />
        </ViewTransition>
      }
    >
      {/* Animate the content up */}
      <ViewTransition enter="slide-up">
        <VideoInfo id={id} />
      </ViewTransition>
    </Suspense>
  );
}

function VideoInfoFallback() {
  return (
    <>
      <div className="fallback title"></div>
      <div className="fallback description"></div>
    </>
  );
}

export default function Details() {
  const { url, navigateBack } = useRouter();
  const videoId = url.split("/").pop();
  const video = use(fetchVideo(videoId));

  return (
    <Layout
      heading={
        <div
          className="fit back"
          onClick={() => {
            navigateBack("/");
          }}
        >
          <ChevronLeft /> Back
        </div>
      }
    >
      <div className="details">
        <Thumbnail video={video} large>
          <VideoControls />
        </Thumbnail>
        <VideoDetails id={video.id} />
      </div>
    </Layout>
  );
}

function VideoInfo({ id }) {
  const details = use(fetchVideoDetails(id));
  return (
    <>
      <p className="info-title">{details.title}</p>
      <p className="info-description">{details.description}</p>
    </>
  );
}
```

```js src/Home.js
import { useId, useState, use, useDeferredValue, ViewTransition } from "react";import { Video } from "./Videos";import Layout from "./Layout";import { fetchVideos } from "./data";import { IconSearch } from "./Icons";

function SearchList({searchText, videos}) {
  // 通过 useDeferredValue来激活(何时) 
  const deferredSearchText = useDeferredValue(searchText);
  const filteredVideos = filterVideos(videos, deferredSearchText);
  return (
    <div className="video-list">
      <div className="videos">
        {filteredVideos.map((video) => (
          // 对列表中的每一个子项目进行动画（何地）
          <ViewTransition key={video.id}>
            <Video video={video} />
          </ViewTransition>
        ))}
      </div>
      {filteredVideos.length === 0 && (
        <div className="no-results">No results</div>
      )}
    </div>
  );
}

export default function Home() {
  const videos = use(fetchVideos());
  const count = videos.length;
  const [searchText, setSearchText] = useState('');

  return (
    <Layout heading={<div className="fit">{count} Videos</div>}>
      <SearchInput value={searchText} onChange={setSearchText} />
      <SearchList videos={videos} searchText={searchText} />
    </Layout>
  );
}

function SearchInput({ value, onChange }) {
  const id = useId();
  return (
    <form className="search" onSubmit={(e) => e.preventDefault()}>
      <label htmlFor={id} className="sr-only">
        Search
      </label>
      <div className="search-input">
        <div className="search-icon">
          <IconSearch />
        </div>
        <input
          type="text"
          id={id}
          placeholder="Search"
          value={value}
          onChange={(e) => onChange(e.target.value)}
        />
      </div>
    </form>
  );
}

function filterVideos(videos, query) {
  const keywords = query
    .toLowerCase()
    .split(" ")
    .filter((s) => s !== "");
  if (keywords.length === 0) {
    return videos;
  }
  return videos.filter((video) => {
    const words = (video.title + " " + video.description)
      .toLowerCase()
      .split(" ");
    return keywords.every((kw) => words.some((w) => w.includes(kw)));
  });
}
```

```js src/Icons.js hidden
export function ChevronLeft() {
  return (
    <svg
      className="chevron-left"
      xmlns="http://www.w3.org/2000/svg"
      width="20"
      height="20"
      viewBox="0 0 20 20">
      <g fill="none" fillRule="evenodd" transform="translate(-446 -398)">
        <path
          fill="currentColor"
          fillRule="nonzero"
          d="M95.8838835,240.366117 C95.3957281,239.877961 94.6042719,239.877961 94.1161165,240.366117 C93.6279612,240.854272 93.6279612,241.645728 94.1161165,242.133883 L98.6161165,246.633883 C99.1042719,247.122039 99.8957281,247.122039 100.383883,246.633883 L104.883883,242.133883 C105.372039,241.645728 105.372039,240.854272 104.883883,240.366117 C104.395728,239.877961 103.604272,239.877961 103.116117,240.366117 L99.5,243.982233 L95.8838835,240.366117 Z"
          transform="translate(356.5 164.5)"
        />
        <polygon points="446 418 466 418 466 398 446 398" />
      </g>
    </svg>
  );
}

export function PauseIcon() {
  return (
    <svg
      className="control-icon"
      style={{padding: '4px'}}
      width="100"
      height="100"
      viewBox="0 0 512 512"
      fill="none"
      xmlns="http://www.w3.org/2000/svg">
      <path
        fillRule="evenodd"
        clipRule="evenodd"
        d="M256 0C114.617 0 0 114.615 0 256s114.617 256 256 256 256-114.615 256-256S397.383 0 256 0zm-32 320c0 8.836-7.164 16-16 16h-32c-8.836 0-16-7.164-16-16V192c0-8.836 7.164-16 16-16h32c8.836 0 16 7.164 16 16v128zm128 0c0 8.836-7.164 16-16 16h-32c-8.836 0-16-7.164-16-16V192c0-8.836 7.164-16 16-16h32c8.836 0 16 7.164 16 16v128z"
        fill="currentColor"
      />
    </svg>
  );
}

export function PlayIcon() {
  return (
    <svg
      className="control-icon"
      width="100"
      height="100"
      viewBox="0 0 72 72"
      fill="none"
      xmlns="http://www.w3.org/2000/svg">
      <path
        fillRule="evenodd"
        clipRule="evenodd"
        d="M36 69C54.2254 69 69 54.2254 69 36C69 17.7746 54.2254 3 36 3C17.7746 3 3 17.7746 3 36C3 54.2254 17.7746 69 36 69ZM52.1716 38.6337L28.4366 51.5801C26.4374 52.6705 24 51.2235 24 48.9464V23.0536C24 20.7764 26.4374 19.3295 28.4366 20.4199L52.1716 33.3663C54.2562 34.5034 54.2562 37.4966 52.1716 38.6337Z"
        fill="currentColor"
      />
    </svg>
  );
}
export function Heart({liked, animate}) {
  return (
    <>
      <svg
        className="absolute overflow-visible"
        viewBox="0 0 24 24"
        fill="none"
        xmlns="http://www.w3.org/2000/svg">
        <circle
          className={`circle ${liked ? 'liked' : ''} ${animate ? 'animate' : ''}`}
          cx="12"
          cy="12"
          r="11.5"
          fill="transparent"
          strokeWidth="0"
          stroke="currentColor"
        />
      </svg>

      <svg
        className={`heart ${liked ? 'liked' : ''} ${animate ? 'animate' : ''}`}
        viewBox="0 0 24 24"
        fill="none"
        xmlns="http://www.w3.org/2000/svg">
        {liked ? (
          <path
            d="M12 23a.496.496 0 0 1-.26-.074C7.023 19.973 0 13.743 0 8.68c0-4.12 2.322-6.677 6.058-6.677 2.572 0 5.108 2.387 5.134 2.41l.808.771.808-.771C12.834 4.387 15.367 2 17.935 2 21.678 2 24 4.558 24 8.677c0 5.06-7.022 11.293-11.74 14.246a.496.496 0 0 1-.26.074V23z"
            fill="currentColor"
          />
        ) : (
          <path
            fillRule="evenodd"
            clipRule="evenodd"
            d="m12 5.184-.808-.771-.004-.004C11.065 4.299 8.522 2.003 6 2.003c-3.736 0-6 2.558-6 6.677 0 4.47 5.471 9.848 10 13.079.602.43 1.187.82 1.74 1.167A.497.497 0 0 0 12 23v-.003c.09 0 .182-.026.26-.074C16.977 19.97 24 13.737 24 8.677 24 4.557 21.743 2 18 2c-2.569 0-5.166 2.387-5.192 2.413L12 5.184zm-.002 15.525c2.071-1.388 4.477-3.342 6.427-5.47C20.72 12.733 22 10.401 22 8.677c0-1.708-.466-2.855-1.087-3.55C20.316 4.459 19.392 4 18 4c-.726 0-1.63.364-2.5.9-.67.412-1.148.82-1.266.92-.03.025-.037.031-.019.014l-.013.013L12 7.949 9.832 5.88a10.08 10.08 0 0 0-1.33-.977C7.633 4.367 6.728 4.003 6 4.003c-1.388 0-2.312.459-2.91 1.128C2.466 5.826 2 6.974 2 8.68c0 1.726 1.28 4.058 3.575 6.563 1.948 2.127 4.352 4.078 6.423 5.466z"
            fill="currentColor"
          />
        )}
      </svg>
    </>
  );
}

export function IconSearch(props) {
  return (
    <svg width="1em" height="1em" viewBox="0 0 20 20">
      <path
        d="M14.386 14.386l4.0877 4.0877-4.0877-4.0877c-2.9418 2.9419-7.7115 2.9419-10.6533 0-2.9419-2.9418-2.9419-7.7115 0-10.6533 2.9418-2.9419 7.7115-2.9419 10.6533 0 2.9419 2.9418 2.9419 7.7115 0 10.6533z"
        stroke="currentColor"
        fill="none"
        strokeWidth="2"
        fillRule="evenodd"
        strokeLinecap="round"
        strokeLinejoin="round"></path>
    </svg>
  );
}
```

```js src/Layout.js
import {ViewTransition} from 'react'; import { useIsNavPending } from "./router";

export default function Page({ heading, children }) {
  const isPending = useIsNavPending();
  return (
    <div className="page">
      <div className="top">
        <div className="top-nav">
          {/* Custom classes based on transition type. */}
          <ViewTransition
            name="nav"
            share={{
              'nav-forward': 'slide-forward',
              'nav-back': 'slide-back',
            }}>
            {heading}
          </ViewTransition>
          {isPending && <span className="loader"></span>}
        </div>
      </div>
      {/* Opt-out of ViewTransition for the content. */}
      {/* Content can define it's own ViewTransition. */}
      <ViewTransition default="none">
        <div className="bottom">
          <div className="content">{children}</div>
        </div>
      </ViewTransition>
    </div>
  );
}
```

```js src/LikeButton.js hidden
import {useState} from 'react';
import {Heart} from './Icons';

// A hack since we don't actually have a backend.
// Unlike local state, this survives videos being filtered.
const likedVideos = new Set();

export default function LikeButton({video}) {
  const [isLiked, setIsLiked] = useState(() => likedVideos.has(video.id));
  const [animate, setAnimate] = useState(false);
  return (
    <button
      className={`like-button ${isLiked && 'liked'}`}
      aria-label={isLiked ? 'Unsave' : 'Save'}
      onClick={() => {
        const nextIsLiked = !isLiked;
        if (nextIsLiked) {
          likedVideos.add(video.id);
        } else {
          likedVideos.delete(video.id);
        }
        setAnimate(true);
        setIsLiked(nextIsLiked);
      }}>
      <Heart liked={isLiked} animate={animate} />
    </button>
  );
}
```

```js src/Videos.js
import { useState, ViewTransition } from "react"; import LikeButton from "./LikeButton"; import { useRouter } from "./router"; import { PauseIcon, PlayIcon } from "./Icons"; import { startTransition } from "react";

export function Thumbnail({ video, children }) {
  // Add a name to animate with a shared element transition.
  return (
    <ViewTransition name={`video-${video.id}`}>
      <div
        aria-hidden="true"
        tabIndex={-1}
        className={`thumbnail ${video.image}`}
      >
        {children}
      </div>
    </ViewTransition>
  );
}



export function VideoControls() {
  const [isPlaying, setIsPlaying] = useState(false);

  return (
    <span
      className="controls"
      onClick={() =>
        startTransition(() => {
          setIsPlaying((p) => !p);
        })
      }
    >
      {isPlaying ? <PauseIcon /> : <PlayIcon />}
    </span>
  );
}

export function Video({ video }) {
  const { navigate } = useRouter();

  return (
    <div className="video">
      <div
        className="link"
        onClick={(e) => {
          e.preventDefault();
          navigate(`/video/${video.id}`);
        }}
      >
        <Thumbnail video={video}></Thumbnail>

        <div className="info">
          <div className="video-title">{video.title}</div>
          <div className="video-description">{video.description}</div>
        </div>
      </div>
      <LikeButton video={video} />
    </div>
  );
}
```


```js src/data.js hidden
const videos = [
  {
    id: '1',
    title: 'First video',
    description: 'Video description',
    image: 'blue',
  },
  {
    id: '2',
    title: 'Second video',
    description: 'Video description',
    image: 'red',
  },
  {
    id: '3',
    title: 'Third video',
    description: 'Video description',
    image: 'green',
  },
  {
    id: '4',
    title: 'Fourth video',
    description: 'Video description',
    image: 'purple',
  },
  {
    id: '5',
    title: 'Fifth video',
    description: 'Video description',
    image: 'yellow',
  },
  {
    id: '6',
    title: 'Sixth video',
    description: 'Video description',
    image: 'gray',
  },
];

let videosCache = new Map();
let videoCache = new Map();
let videoDetailsCache = new Map();
const VIDEO_DELAY = 1;
const VIDEO_DETAILS_DELAY = 1000;
export function fetchVideos() {
  if (videosCache.has(0)) {
    return videosCache.get(0);
  }
  const promise = new Promise((resolve) => {
    setTimeout(() => {
      resolve(videos);
    }, VIDEO_DELAY);
  });
  videosCache.set(0, promise);
  return promise;
}

export function fetchVideo(id) {
  if (videoCache.has(id)) {
    return videoCache.get(id);
  }
  const promise = new Promise((resolve) => {
    setTimeout(() => {
      resolve(videos.find((video) => video.id === id));
    }, VIDEO_DELAY);
  });
  videoCache.set(id, promise);
  return promise;
}

export function fetchVideoDetails(id) {
  if (videoDetailsCache.has(id)) {
    return videoDetailsCache.get(id);
  }
  const promise = new Promise((resolve) => {
    setTimeout(() => {
      resolve(videos.find((video) => video.id === id));
    }, VIDEO_DETAILS_DELAY);
  });
  videoDetailsCache.set(id, promise);
  return promise;
}
```

```js src/router.js
import {useState, createContext, use, useTransition, useLayoutEffect, useEffect, addTransitionType} from "react";

export function Router({ children }) {
  const [isPending, startTransition] = useTransition();
  function navigate(url) {
    startTransition(() => {
      // Transition type for the cause "nav forward"
      addTransitionType('nav-forward');
      go(url);
    });
  }
  function navigateBack(url) {
    startTransition(() => {
      // Transition type for the cause "nav backward"
      addTransitionType('nav-back');
      go(url);
    });
  }

  const [routerState, setRouterState] = useState({pendingNav: () => {}, url: document.location.pathname});

  function go(url) {
    setRouterState({
      url,
      pendingNav() {
        window.history.pushState({}, "", url);
      },
    });
  }

  useEffect(() => {
    function handlePopState() {
      // This should not animate because restoration has to be synchronous.
      // Even though it's a transition.
      startTransition(() => {
        setRouterState({
          url: document.location.pathname + document.location.search,
          pendingNav() {
            // Noop. URL has already updated.
          },
        });
      });
    }
    window.addEventListener("popstate", handlePopState);
    return () => {
      window.removeEventListener("popstate", handlePopState);
    };
  }, []);
  const pendingNav = routerState.pendingNav;
  useLayoutEffect(() => {
    pendingNav();
  }, [pendingNav]);

  return (
    <RouterContext
      value={{
        url: routerState.url,
        navigate,
        navigateBack,
        isPending,
        params: {},
      }}
    >
      {children}
    </RouterContext>
  );
}

const RouterContext = createContext({ url: "/", params: {} });

export function useRouter() {
  return use(RouterContext);
}

export function useIsNavPending() {
  return use(RouterContext).isPending;
}

```

```css src/styles.css hidden
@font-face {
  font-family: Optimistic Text;
  src: url(https://react.dev/fonts/Optimistic_Text_W_Rg.woff2) format("woff2");
  font-weight: 400;
  font-style: normal;
  font-display: swap;
}

@font-face {
  font-family: Optimistic Text;
  src: url(https://react.dev/fonts/Optimistic_Text_W_Md.woff2) format("woff2");
  font-weight: 500;
  font-style: normal;
  font-display: swap;
}

@font-face {
  font-family: Optimistic Text;
  src: url(https://react.dev/fonts/Optimistic_Text_W_Bd.woff2) format("woff2");
  font-weight: 600;
  font-style: normal;
  font-display: swap;
}

@font-face {
  font-family: Optimistic Text;
  src: url(https://react.dev/fonts/Optimistic_Text_W_Bd.woff2) format("woff2");
  font-weight: 700;
  font-style: normal;
  font-display: swap;
}

* {
  box-sizing: border-box;
}

html {
  background-image: url(https://react.dev/images/meta-gradient-dark.png);
  background-size: 100%;
  background-position: -100%;
  background-color: rgb(64 71 86);
  background-repeat: no-repeat;
  height: 100%;
  width: 100%;
}

body {
  font-family: Optimistic Text, -apple-system, ui-sans-serif, system-ui, sans-serif, Apple Color Emoji, Segoe UI Emoji, Segoe UI Symbol, Noto Color Emoji;
  padding: 10px 0 10px 0;
  margin: 0;
  display: flex;
  justify-content: center;
}

#root {
  flex: 1 1;
  height: auto;
  background-color: #fff;
  border-radius: 10px;
  max-width: 450px;
  min-height: 600px;
  padding-bottom: 10px;
}

h1 {
  margin-top: 0;
  font-size: 22px;
}

h2 {
  margin-top: 0;
  font-size: 20px;
}

h3 {
  margin-top: 0;
  font-size: 18px;
}

h4 {
  margin-top: 0;
  font-size: 16px;
}

h5 {
  margin-top: 0;
  font-size: 14px;
}

h6 {
  margin-top: 0;
  font-size: 12px;
}

code {
  font-size: 1.2em;
}

ul {
  padding-inline-start: 20px;
}

.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  padding: 0;
  margin: -1px;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  white-space: nowrap;
  border-width: 0;
}

.absolute {
  position: absolute;
}

.overflow-visible {
  overflow: visible;
}

.visible {
  overflow: visible;
}

.fit {
  width: fit-content;
}


/* Layout */
.page {
  display: flex;
  flex-direction: column;
  height: 100%;
}

.top-hero {
  height: 200px;
  display: flex;
  justify-content: center;
  align-items: center;
  background-image: conic-gradient(
      from 90deg at -10% 100%,
      #2b303b 0deg,
      #2b303b 90deg,
      #16181d 1turn
  );
}

.bottom {
  flex: 1;
  overflow: auto;
}

.top-nav {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 0;
  padding: 0 12px;
  top: 0;
  width: 100%;
  height: 44px;
  color: #23272f;
  font-weight: 700;
  font-size: 20px;
  z-index: 100;
  cursor: default;
}

.content {
  padding: 0 12px;
  margin-top: 4px;
}


.loader {
  color: #23272f;
  font-size: 3px;
  width: 1em;
  margin-right: 18px;
  height: 1em;
  border-radius: 50%;
  position: relative;
  text-indent: -9999em;
  animation: loading-spinner 1.3s infinite linear;
  animation-delay: 200ms;
  transform: translateZ(0);
}

@keyframes loading-spinner {
  0%,
  100% {
    box-shadow: 0 -3em 0 0.2em,
    2em -2em 0 0em, 3em 0 0 -1em,
    2em 2em 0 -1em, 0 3em 0 -1em,
    -2em 2em 0 -1em, -3em 0 0 -1em,
    -2em -2em 0 0;
  }
  12.5% {
    box-shadow: 0 -3em 0 0, 2em -2em 0 0.2em,
    3em 0 0 0, 2em 2em 0 -1em, 0 3em 0 -1em,
    -2em 2em 0 -1em, -3em 0 0 -1em,
    -2em -2em 0 -1em;
  }
  25% {
    box-shadow: 0 -3em 0 -0.5em,
    2em -2em 0 0, 3em 0 0 0.2em,
    2em 2em 0 0, 0 3em 0 -1em,
    -2em 2em 0 -1em, -3em 0 0 -1em,
    -2em -2em 0 -1em;
  }
  37.5% {
    box-shadow: 0 -3em 0 -1em, 2em -2em 0 -1em,
    3em 0em 0 0, 2em 2em 0 0.2em, 0 3em 0 0em,
    -2em 2em 0 -1em, -3em 0em 0 -1em, -2em -2em 0 -1em;
  }
  50% {
    box-shadow: 0 -3em 0 -1em, 2em -2em 0 -1em,
    3em 0 0 -1em, 2em 2em 0 0em, 0 3em 0 0.2em,
    -2em 2em 0 0, -3em 0em 0 -1em, -2em -2em 0 -1em;
  }
  62.5% {
    box-shadow: 0 -3em 0 -1em, 2em -2em 0 -1em,
    3em 0 0 -1em, 2em 2em 0 -1em, 0 3em 0 0,
    -2em 2em 0 0.2em, -3em 0 0 0, -2em -2em 0 -1em;
  }
  75% {
    box-shadow: 0em -3em 0 -1em, 2em -2em 0 -1em,
    3em 0em 0 -1em, 2em 2em 0 -1em, 0 3em 0 -1em,
    -2em 2em 0 0, -3em 0em 0 0.2em, -2em -2em 0 0;
  }
  87.5% {
    box-shadow: 0em -3em 0 0, 2em -2em 0 -1em,
    3em 0 0 -1em, 2em 2em 0 -1em, 0 3em 0 -1em,
    -2em 2em 0 0, -3em 0em 0 0, -2em -2em 0 0.2em;
  }
}

/* LikeButton */
.like-button {
  outline-offset: 2px;
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
  width: 2.5rem;
  height: 2.5rem;
  cursor: pointer;
  border-radius: 9999px;
  border: none;
  outline: none 2px;
  color: #5e687e;
  background: none;
}

.like-button:focus {
  color: #a6423a;
  background-color: rgba(166, 66, 58, .05);
}

.like-button:active {
  color: #a6423a;
  background-color: rgba(166, 66, 58, .05);
  transform: scaleX(0.95) scaleY(0.95);
}

.like-button:hover {
  background-color: #f6f7f9;
}

.like-button.liked {
  color: #a6423a;
}

/* Icons */
@keyframes circle {
  0% {
    transform: scale(0);
    stroke-width: 16px;
  }

  50% {
    transform: scale(.5);
    stroke-width: 16px;
  }

  to {
    transform: scale(1);
    stroke-width: 0;
  }
}

.circle {
  color: rgba(166, 66, 58, .5);
  transform-origin: center;
  transition-property: all;
  transition-duration: .15s;
  transition-timing-function: cubic-bezier(.4,0,.2,1);
}

.circle.liked.animate {
  animation: circle .3s forwards;
}

.heart {
  width: 1.5rem;
  height: 1.5rem;
}

.heart.liked {
  transform-origin: center;
  transition-property: all;
  transition-duration: .15s;
  transition-timing-function: cubic-bezier(.4, 0, .2, 1);
}

.heart.liked.animate {
  animation: scale .35s ease-in-out forwards;
}

.control-icon {
  color: hsla(0, 0%, 100%, .5);
  filter:  drop-shadow(0 20px 13px rgba(0, 0, 0, .03)) drop-shadow(0 8px 5px rgba(0, 0, 0, .08));
}

.chevron-left {
  margin-top: 2px;
  rotate: 90deg;
}


/* Video */
.thumbnail {
  position: relative;
  aspect-ratio: 16 / 9;
  display: flex;
  overflow: hidden;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  border-radius: 0.5rem;
  outline-offset: 2px;
  width: 8rem;
  vertical-align: middle;
  background-color: #ffffff;
  background-size: cover;
  user-select: none;
}

.thumbnail.blue {
  background-image: conic-gradient(at top right, #c76a15, #087ea4, #2b3491);
}

.thumbnail.red {
  background-image: conic-gradient(at top right, #c76a15, #a6423a, #2b3491);
}

.thumbnail.green {
  background-image: conic-gradient(at top right, #c76a15, #388f7f, #2b3491);
}

.thumbnail.purple {
  background-image: conic-gradient(at top right, #c76a15, #575fb7, #2b3491);
}

.thumbnail.yellow {
  background-image: conic-gradient(at top right, #c76a15, #FABD62, #2b3491);
}

.thumbnail.gray {
  background-image: conic-gradient(at top right, #c76a15, #4E5769, #2b3491);
}

.video {
  display: flex;
  flex-direction: row;
  gap: 0.75rem;
  align-items: center;
}

.video .link {
  display: flex;
  flex-direction: row;
  flex: 1 1 0;
  gap: 0.125rem;
  outline-offset: 4px;
  cursor: pointer;
}

.video .info {
  display: flex;
  flex-direction: column;
  justify-content: center;
  margin-left: 8px;
  gap: 0.125rem;
}

.video .info:hover {
  text-decoration: underline;
}

.video-title {
  font-size: 15px;
  line-height: 1.25;
  font-weight: 700;
  color: #23272f;
}

.video-description {
  color: #5e687e;
  font-size: 13px;
}

/* Details */
.details .thumbnail {
  position: relative;
  aspect-ratio: 16 / 9;
  display: flex;
  overflow: hidden;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  border-radius: 0.5rem;
  outline-offset: 2px;
  width: 100%;
  vertical-align: middle;
  background-color: #ffffff;
  background-size: cover;
  user-select: none;
}

.video-details-title {
  margin-top: 8px;
}

.video-details-speaker {
  display: flex;
  gap: 8px;
  margin-top: 10px
}

.back {
  display: flex;
  align-items: center;
  margin-left: -5px;
  cursor: pointer;
}

.back:hover {
  text-decoration: underline;
}

.info-title {
  font-size: 1.5rem;
  font-weight: 700;
  line-height: 1.25;
  margin: 8px 0 0 0 ;
}

.info-description {
  margin: 8px 0 0 0;
}

.controls {
  cursor: pointer;
}

.fallback {
  background: #f6f7f8 linear-gradient(to right, #e6e6e6 5%, #cccccc 25%, #e6e6e6 35%) no-repeat;
  background-size: 800px 104px;
  display: block;
  line-height: 1.25;
  margin: 8px 0 0 0;
  border-radius: 5px;
  overflow: hidden;

  animation: 1s linear 1s infinite shimmer;
  animation-delay: 300ms;
  animation-duration: 1s;
  animation-fill-mode: forwards;
  animation-iteration-count: infinite;
  animation-name: shimmer;
  animation-timing-function: linear;
}


.fallback.title {
  width: 130px;
  height: 30px;

}

.fallback.description {
  width: 150px;
  height: 21px;
}

@keyframes shimmer {
  0% {
    background-position: -468px 0;
  }

  100% {
    background-position: 468px 0;
  }
}

.search {
  margin-bottom: 10px;
}
.search-input {
  width: 100%;
  position: relative;
}

.search-icon {
  position: absolute;
  top: 0;
  bottom: 0;
  inset-inline-start: 0;
  display: flex;
  align-items: center;
  padding-inline-start: 1rem;
  pointer-events: none;
  color: #99a1b3;
}

.search-input input {
  display: flex;
  padding-inline-start: 2.75rem;
  padding-top: 10px;
  padding-bottom: 10px;
  width: 100%;
  text-align: start;
  background-color: rgb(235 236 240);
  outline: 2px solid transparent;
  cursor: pointer;
  border: none;
  align-items: center;
  color: rgb(35 39 47);
  border-radius: 9999px;
  vertical-align: middle;
  font-size: 15px;
}

.search-input input:hover, .search-input input:active {
  background-color: rgb(235 236 240/ 0.8);
  color: rgb(35 39 47/ 0.8);
}

/* Home */
.video-list {
  position: relative;
}

.video-list .videos {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  overflow-y: auto;
  height: 100%;
}
```


```css src/animations.css
/* Slide animations for Suspense the fallback down */
::view-transition-old(.slide-down) {
    animation: 150ms ease-out both fade-out, 150ms ease-out both slide-down;
}

::view-transition-new(.slide-up) {
    animation: 210ms ease-in 150ms both fade-in, 400ms ease-in both slide-up;
}

/* Animations for view transition classed added by transition type */
::view-transition-old(.slide-forward) {
    /* when sliding forward, the "old" page should slide out to left. */
    animation: 150ms cubic-bezier(0.4, 0, 1, 1) both fade-out,
    400ms cubic-bezier(0.4, 0, 0.2, 1) both slide-to-left;
}

::view-transition-new(.slide-forward) {
    /* when sliding forward, the "new" page should slide in from right. */
    animation: 210ms cubic-bezier(0, 0, 0.2, 1) 150ms both fade-in,
    400ms cubic-bezier(0.4, 0, 0.2, 1) both slide-from-right;
}

::view-transition-old(.slide-back) {
    /* when sliding back, the "old" page should slide out to right. */
    animation: 150ms cubic-bezier(0.4, 0, 1, 1) both fade-out,
    400ms cubic-bezier(0.4, 0, 0.2, 1) both slide-to-right;
}

::view-transition-new(.slide-back) {
    /* when sliding back, the "new" page should slide in from left. */
    animation: 210ms cubic-bezier(0, 0, 0.2, 1) 150ms both fade-in,
    400ms cubic-bezier(0.4, 0, 0.2, 1) both slide-from-left;
}

/* Keyframes to support our animations above. */
@keyframes slide-up {
    from {
        transform: translateY(10px);
    }
    to {
        transform: translateY(0);
    }
}

@keyframes slide-down {
    from {
        transform: translateY(0);
    }
    to {
        transform: translateY(10px);
    }
}

@keyframes fade-in {
    from {
        opacity: 0;
    }
}

@keyframes fade-out {
    to {
        opacity: 0;
    }
}

@keyframes slide-to-right {
    to {
        transform: translateX(50px);
    }
}

@keyframes slide-from-right {
    from {
        transform: translateX(50px);
    }
    to {
        transform: translateX(0);
    }
}

@keyframes slide-to-left {
    to {
        transform: translateX(-50px);
    }
}

@keyframes slide-from-left {
    from {
        transform: translateX(-50px);
    }
    to {
        transform: translateX(0);
    }
}
```

```js src/index.js hidden
import React, {StrictMode} from 'react';
import {createRoot} from 'react-dom/client';
import './styles.css';
import './animations.css';

import App from './App';
import {Router} from './router';

const root = createRoot(document.getElementById('root'));
root.render(
  <StrictMode>
    <Router>
      <App />
    </Router>
  </StrictMode>
);
```

```json package.json hidden
{
  "dependencies": {
    "react": "canary",
    "react-dom": "canary",
    "react-scripts": "latest"
  },
  "scripts": {
    "start": "react-scripts start",
    "build": "react-scripts build",
    "test": "react-scripts test --env=jsdom",
    "eject": "react-scripts eject"
  }
}
```

</Sandpack>

如果你想了解更多关于它们如何工作的信息，请查看文档中的[`<ViewTransition>` 如何工作](/reference/react/ViewTransition#how-does-viewtransition-work)。

**关于我们如何构建视图过渡的更多背景信息，请参阅：[#31975](https://github.com/facebook/react/pull/31975)、[#32105](https://github.com/facebook/react/pull/32105)、[#32041](https://github.com/facebook/react/pull/32041)、[#32734](https://github.com/facebook/react/pull/32734)、[#32797](https://github.com/facebook/react/pull/32797)、[#31999](https://github.com/facebook/react/pull/31999)、[#32031](https://github.com/facebook/react/pull/32031)、[#32050](https://github.com/facebook/react/pull/32050)、[#32820](https://github.com/facebook/react/pull/32820)、[#32029](https://github.com/facebook/react/pull/32029)、[#32028](https://github.com/facebook/react/pull/32028) 和 [#32038](https://github.com/facebook/react/pull/32038)，由 [@sebmarkbage](https://twitter.com/sebmarkbage) 完成（感谢 Seb！）。**

---

## Activity {/*activity*/}

<Note>

**`<Activity />` 现在可以在 React Canary 版本使用。**

[了解更多关于 React 版本发布的内容](/community/versioning-policy#all-release-channels)。

</Note>

在[过去](/blog/2022/06/15/react-labs-what-we-have-been-working-on-june-2022#offscreen)的[更新](/blog/2024/02/15/react-labs-what-we-have-been-working-on-february-2024#offscreen-renamed-to-activity)中，我们分享了我们正在研究一个 API，允许组件在视觉上被隐藏并降低优先级，相比卸载或使用 CSS 隐藏，这种方式能以更低的性能成本保留 UI 状态。

现在我们准备分享这个 API 及其工作原理，这样你就可以开始在实验性 React 版本中测试它了。

`<Activity>` 是一个用于隐藏和显示 UI 部分的新组件：

```js [[1, 1, "'visible'"], [2, 1, "'hidden'"]]
<Activity mode={isVisible ? 'visible' : 'hidden'}>
  <Page />
</Activity>
```

当 Activity 处于 <CodeStep step={1}>visible</CodeStep>（可见）状态时，它会正常渲染。当 Activity 处于 <CodeStep step={2}>hidden</CodeStep>（隐藏）状态时，它会被卸载，但会保存其状态并继续以低于屏幕上任何可见内容的优先级进行渲染。

你可以使用 `Activity` 来保存用户当前未使用的 UI 部分的状态，或预渲染用户可能接下来会使用的部分。

让我们看一些改进上面视图过渡示例的例子。

<Note>

**当 Activity 处于 hidden 状态的时候 Effect 不会启动**

当 `<Activity>` 处于 `hidden` 状态时，Effect 会被卸载。从概念上讲，组件被卸载了，但 React 会保存状态以供以后使用。

在实践中，如果你遵循了[你可能不需要 Effect](/learn/you-might-not-need-an-effect)指南，这将按预期工作。为了及早发现有问题的 Effect，我们建议添加 [`<StrictMode>`](/reference/react/StrictMode)，它将积极执行 Activity 的卸载和挂载，以捕获任何意外的副作用。

</Note>

### 使用 Activity 恢复状态 {/*restoring-state-with-activity*/}

当用户离开一个页面时，通常会停止渲染旧页面：

```js {6,7}
function App() {
  const { url } = useRouter();

  return (
    <>
      {url === '/' && <Home />}
      {url !== '/' && <Details />}
    </>
  );
}
```

然而，这意味着如果用户返回到旧页面，所有之前的状态都会丢失。例如，如果 `<Home />` 页面有一个 `<input>` 字段，当用户离开页面时，`<input>` 会被卸载，他们输入的所有文本都会丢失。

Activity 允许你在用户切换页面时保留状态，这样当他们返回时可以从离开的地方继续。这是通过将树的一部分包装在 `<Activity>` 中并切换 `mode` 来实现的：

```js {6-8}
function App() {
  const { url } = useRouter();

  return (
    <>
      <Activity mode={url === '/' ? 'visible' : 'hidden'}>
        <Home />
      </Activity>
      {url !== '/' && <Details />}
    </>
  );
}
```

通过这个更改，我们可以改进上面的视图过渡示例。之前，当你搜索视频、选择一个视频并返回时，你的搜索过滤器会丢失。使用 Activity，你的搜索过滤器会被恢复，你可以从离开的地方继续。

尝试搜索一个视频，选择它，然后点击“返回”：

<Sandpack>

```js src/App.js
import { Activity, ViewTransition } from "react"; import Details from "./Details"; import Home from "./Home"; import { useRouter } from "./router";

export default function App() {
  const { url } = useRouter();

  return (
    // 视图过渡知道如何处理 Activity
    <ViewTransition>
      {/* Render Home in Activity so we don't lose state */}
      <Activity mode={url === '/' ? 'visible' : 'hidden'}>
        <Home />
      </Activity>
      {url !== '/' && <Details />}
    </ViewTransition>
  );
}
```

```js src/Details.js hidden
import { use, Suspense, ViewTransition } from "react";
import { fetchVideo, fetchVideoDetails } from "./data";
import { Thumbnail, VideoControls } from "./Videos";
import { useRouter } from "./router";
import Layout from "./Layout";
import { ChevronLeft } from "./Icons";

function VideoDetails({id}) {
  // Animate from Suspense fallback to content
  return (
    <Suspense
      fallback={
        // Animate the fallback down.
        <ViewTransition exit="slide-down">
          <VideoInfoFallback />
        </ViewTransition>
      }
    >
      {/* Animate the content up */}
      <ViewTransition enter="slide-up">
        <VideoInfo id={id} />
      </ViewTransition>
    </Suspense>
  );
}

function VideoInfoFallback() {
  return (
    <>
      <div className="fallback title"></div>
      <div className="fallback description"></div>
    </>
  );
}

export default function Details() {
  const { url, navigateBack } = useRouter();
  const videoId = url.split("/").pop();
  const video = use(fetchVideo(videoId));

  return (
    <Layout
      heading={
        <div
          className="fit back"
          onClick={() => {
            navigateBack("/");
          }}
        >
          <ChevronLeft /> Back
        </div>
      }
    >
      <div className="details">
        <Thumbnail video={video} large>
          <VideoControls />
        </Thumbnail>
        <VideoDetails id={video.id} />
      </div>
    </Layout>
  );
}

function VideoInfo({ id }) {
  const details = use(fetchVideoDetails(id));
  return (
    <>
      <p className="info-title">{details.title}</p>
      <p className="info-description">{details.description}</p>
    </>
  );
}
```

```js src/Home.js hidden
import { useId, useState, use, useDeferredValue, ViewTransition } from "react";import { Video } from "./Videos";import Layout from "./Layout";import { fetchVideos } from "./data";import { IconSearch } from "./Icons";

function SearchList({searchText, videos}) {
  // 通过 useDeferredValue来激活(何时) 
  const deferredSearchText = useDeferredValue(searchText);
  const filteredVideos = filterVideos(videos, deferredSearchText);
  return (
    <div className="video-list">
      {filteredVideos.length === 0 && (
        <div className="no-results">No results</div>
      )}
      <div className="videos">
        {filteredVideos.map((video) => (
          // 对列表中的每一个子项目进行动画（何地）
          <ViewTransition key={video.id}>
            <Video video={video} />
          </ViewTransition>
        ))}
      </div>
    </div>
  );
}

export default function Home() {
  const videos = use(fetchVideos());
  const count = videos.length;
  const [searchText, setSearchText] = useState('');

  return (
    <Layout heading={<div className="fit">{count} Videos</div>}>
      <SearchInput value={searchText} onChange={setSearchText} />
      <SearchList videos={videos} searchText={searchText} />
    </Layout>
  );
}

function SearchInput({ value, onChange }) {
  const id = useId();
  return (
    <form className="search" onSubmit={(e) => e.preventDefault()}>
      <label htmlFor={id} className="sr-only">
        Search
      </label>
      <div className="search-input">
        <div className="search-icon">
          <IconSearch />
        </div>
        <input
          type="text"
          id={id}
          placeholder="Search"
          value={value}
          onChange={(e) => onChange(e.target.value)}
        />
      </div>
    </form>
  );
}

function filterVideos(videos, query) {
  const keywords = query
    .toLowerCase()
    .split(" ")
    .filter((s) => s !== "");
  if (keywords.length === 0) {
    return videos;
  }
  return videos.filter((video) => {
    const words = (video.title + " " + video.description)
      .toLowerCase()
      .split(" ");
    return keywords.every((kw) => words.some((w) => w.includes(kw)));
  });
}
```

```js src/Icons.js hidden
export function ChevronLeft() {
  return (
    <svg
      className="chevron-left"
      xmlns="http://www.w3.org/2000/svg"
      width="20"
      height="20"
      viewBox="0 0 20 20">
      <g fill="none" fillRule="evenodd" transform="translate(-446 -398)">
        <path
          fill="currentColor"
          fillRule="nonzero"
          d="M95.8838835,240.366117 C95.3957281,239.877961 94.6042719,239.877961 94.1161165,240.366117 C93.6279612,240.854272 93.6279612,241.645728 94.1161165,242.133883 L98.6161165,246.633883 C99.1042719,247.122039 99.8957281,247.122039 100.383883,246.633883 L104.883883,242.133883 C105.372039,241.645728 105.372039,240.854272 104.883883,240.366117 C104.395728,239.877961 103.604272,239.877961 103.116117,240.366117 L99.5,243.982233 L95.8838835,240.366117 Z"
          transform="translate(356.5 164.5)"
        />
        <polygon points="446 418 466 418 466 398 446 398" />
      </g>
    </svg>
  );
}

export function PauseIcon() {
  return (
    <svg
      className="control-icon"
      style={{padding: '4px'}}
      width="100"
      height="100"
      viewBox="0 0 512 512"
      fill="none"
      xmlns="http://www.w3.org/2000/svg">
      <path
        fillRule="evenodd"
        clipRule="evenodd"
        d="M256 0C114.617 0 0 114.615 0 256s114.617 256 256 256 256-114.615 256-256S397.383 0 256 0zm-32 320c0 8.836-7.164 16-16 16h-32c-8.836 0-16-7.164-16-16V192c0-8.836 7.164-16 16-16h32c8.836 0 16 7.164 16 16v128zm128 0c0 8.836-7.164 16-16 16h-32c-8.836 0-16-7.164-16-16V192c0-8.836 7.164-16 16-16h32c8.836 0 16 7.164 16 16v128z"
        fill="currentColor"
      />
    </svg>
  );
}

export function PlayIcon() {
  return (
    <svg
      className="control-icon"
      width="100"
      height="100"
      viewBox="0 0 72 72"
      fill="none"
      xmlns="http://www.w3.org/2000/svg">
      <path
        fillRule="evenodd"
        clipRule="evenodd"
        d="M36 69C54.2254 69 69 54.2254 69 36C69 17.7746 54.2254 3 36 3C17.7746 3 3 17.7746 3 36C3 54.2254 17.7746 69 36 69ZM52.1716 38.6337L28.4366 51.5801C26.4374 52.6705 24 51.2235 24 48.9464V23.0536C24 20.7764 26.4374 19.3295 28.4366 20.4199L52.1716 33.3663C54.2562 34.5034 54.2562 37.4966 52.1716 38.6337Z"
        fill="currentColor"
      />
    </svg>
  );
}
export function Heart({liked, animate}) {
  return (
    <>
      <svg
        className="absolute overflow-visible"
        viewBox="0 0 24 24"
        fill="none"
        xmlns="http://www.w3.org/2000/svg">
        <circle
          className={`circle ${liked ? 'liked' : ''} ${animate ? 'animate' : ''}`}
          cx="12"
          cy="12"
          r="11.5"
          fill="transparent"
          strokeWidth="0"
          stroke="currentColor"
        />
      </svg>

      <svg
        className={`heart ${liked ? 'liked' : ''} ${animate ? 'animate' : ''}`}
        viewBox="0 0 24 24"
        fill="none"
        xmlns="http://www.w3.org/2000/svg">
        {liked ? (
          <path
            d="M12 23a.496.496 0 0 1-.26-.074C7.023 19.973 0 13.743 0 8.68c0-4.12 2.322-6.677 6.058-6.677 2.572 0 5.108 2.387 5.134 2.41l.808.771.808-.771C12.834 4.387 15.367 2 17.935 2 21.678 2 24 4.558 24 8.677c0 5.06-7.022 11.293-11.74 14.246a.496.496 0 0 1-.26.074V23z"
            fill="currentColor"
          />
        ) : (
          <path
            fillRule="evenodd"
            clipRule="evenodd"
            d="m12 5.184-.808-.771-.004-.004C11.065 4.299 8.522 2.003 6 2.003c-3.736 0-6 2.558-6 6.677 0 4.47 5.471 9.848 10 13.079.602.43 1.187.82 1.74 1.167A.497.497 0 0 0 12 23v-.003c.09 0 .182-.026.26-.074C16.977 19.97 24 13.737 24 8.677 24 4.557 21.743 2 18 2c-2.569 0-5.166 2.387-5.192 2.413L12 5.184zm-.002 15.525c2.071-1.388 4.477-3.342 6.427-5.47C20.72 12.733 22 10.401 22 8.677c0-1.708-.466-2.855-1.087-3.55C20.316 4.459 19.392 4 18 4c-.726 0-1.63.364-2.5.9-.67.412-1.148.82-1.266.92-.03.025-.037.031-.019.014l-.013.013L12 7.949 9.832 5.88a10.08 10.08 0 0 0-1.33-.977C7.633 4.367 6.728 4.003 6 4.003c-1.388 0-2.312.459-2.91 1.128C2.466 5.826 2 6.974 2 8.68c0 1.726 1.28 4.058 3.575 6.563 1.948 2.127 4.352 4.078 6.423 5.466z"
            fill="currentColor"
          />
        )}
      </svg>
    </>
  );
}

export function IconSearch(props) {
  return (
    <svg width="1em" height="1em" viewBox="0 0 20 20">
      <path
        d="M14.386 14.386l4.0877 4.0877-4.0877-4.0877c-2.9418 2.9419-7.7115 2.9419-10.6533 0-2.9419-2.9418-2.9419-7.7115 0-10.6533 2.9418-2.9419 7.7115-2.9419 10.6533 0 2.9419 2.9418 2.9419 7.7115 0 10.6533z"
        stroke="currentColor"
        fill="none"
        strokeWidth="2"
        fillRule="evenodd"
        strokeLinecap="round"
        strokeLinejoin="round"></path>
    </svg>
  );
}
```

```js src/Layout.js hidden
import {ViewTransition} from 'react'; import { useIsNavPending } from "./router";

export default function Page({ heading, children }) {
  const isPending = useIsNavPending();
  return (
    <div className="page">
      <div className="top">
        <div className="top-nav">
          {/* Custom classes based on transition type. */}
          <ViewTransition
            name="nav"
            share={{
              'nav-forward': 'slide-forward',
              'nav-back': 'slide-back',
            }}>
            {heading}
          </ViewTransition>
          {isPending && <span className="loader"></span>}
        </div>
      </div>
      {/* Opt-out of ViewTransition for the content. */}
      {/* Content can define it's own ViewTransition. */}
      <ViewTransition default="none">
        <div className="bottom">
          <div className="content">{children}</div>
        </div>
      </ViewTransition>
    </div>
  );
}
```

```js src/LikeButton.js hidden
import {useState} from 'react';
import {Heart} from './Icons';

// A hack since we don't actually have a backend.
// Unlike local state, this survives videos being filtered.
const likedVideos = new Set();

export default function LikeButton({video}) {
  const [isLiked, setIsLiked] = useState(() => likedVideos.has(video.id));
  const [animate, setAnimate] = useState(false);
  return (
    <button
      className={`like-button ${isLiked && 'liked'}`}
      aria-label={isLiked ? 'Unsave' : 'Save'}
      onClick={() => {
        const nextIsLiked = !isLiked;
        if (nextIsLiked) {
          likedVideos.add(video.id);
        } else {
          likedVideos.delete(video.id);
        }
        setAnimate(true);
        setIsLiked(nextIsLiked);
      }}>
      <Heart liked={isLiked} animate={animate} />
    </button>
  );
}
```

```js src/Videos.js hidden
import { useState, ViewTransition } from "react";
import LikeButton from "./LikeButton";
import { useRouter } from "./router";
import { PauseIcon, PlayIcon } from "./Icons";
import { startTransition } from "react";

export function Thumbnail({ video, children }) {
  // Add a name to animate with a shared element transition.
  // This uses the default animation, no additional css needed.
  return (
    <ViewTransition name={`video-${video.id}`}>
      <div
        aria-hidden="true"
        tabIndex={-1}
        className={`thumbnail ${video.image}`}
      >
        {children}
      </div>
    </ViewTransition>
  );
}

export function VideoControls() {
  const [isPlaying, setIsPlaying] = useState(false);

  return (
    <span
      className="controls"
      onClick={() =>
        startTransition(() => {
          setIsPlaying((p) => !p);
        })
      }
    >
      {isPlaying ? <PauseIcon /> : <PlayIcon />}
    </span>
  );
}

export function Video({ video }) {
  const { navigate } = useRouter();

  return (
    <div className="video">
      <div
        className="link"
        onClick={(e) => {
          e.preventDefault();
          navigate(`/video/${video.id}`);
        }}
      >
        <Thumbnail video={video}></Thumbnail>

        <div className="info">
          <div className="video-title">{video.title}</div>
          <div className="video-description">{video.description}</div>
        </div>
      </div>
      <LikeButton video={video} />
    </div>
  );
}
```


```js src/data.js hidden
const videos = [
  {
    id: '1',
    title: 'First video',
    description: 'Video description',
    image: 'blue',
  },
  {
    id: '2',
    title: 'Second video',
    description: 'Video description',
    image: 'red',
  },
  {
    id: '3',
    title: 'Third video',
    description: 'Video description',
    image: 'green',
  },
  {
    id: '4',
    title: 'Fourth video',
    description: 'Video description',
    image: 'purple',
  },
  {
    id: '5',
    title: 'Fifth video',
    description: 'Video description',
    image: 'yellow',
  },
  {
    id: '6',
    title: 'Sixth video',
    description: 'Video description',
    image: 'gray',
  },
];

let videosCache = new Map();
let videoCache = new Map();
let videoDetailsCache = new Map();
const VIDEO_DELAY = 1;
const VIDEO_DETAILS_DELAY = 1000;
export function fetchVideos() {
  if (videosCache.has(0)) {
    return videosCache.get(0);
  }
  const promise = new Promise((resolve) => {
    setTimeout(() => {
      resolve(videos);
    }, VIDEO_DELAY);
  });
  videosCache.set(0, promise);
  return promise;
}

export function fetchVideo(id) {
  if (videoCache.has(id)) {
    return videoCache.get(id);
  }
  const promise = new Promise((resolve) => {
    setTimeout(() => {
      resolve(videos.find((video) => video.id === id));
    }, VIDEO_DELAY);
  });
  videoCache.set(id, promise);
  return promise;
}

export function fetchVideoDetails(id) {
  if (videoDetailsCache.has(id)) {
    return videoDetailsCache.get(id);
  }
  const promise = new Promise((resolve) => {
    setTimeout(() => {
      resolve(videos.find((video) => video.id === id));
    }, VIDEO_DETAILS_DELAY);
  });
  videoDetailsCache.set(id, promise);
  return promise;
}
```

```js src/router.js hidden
import {useState, createContext, use, useTransition, useLayoutEffect, useEffect, addTransitionType} from "react";

export function Router({ children }) {
  const [isPending, startTransition] = useTransition();
  const [routerState, setRouterState] = useState({pendingNav: () => {}, url: document.location.pathname});
  function navigate(url) {
    startTransition(() => {
      // Transition type for the cause "nav forward"
      addTransitionType('nav-forward');
      go(url);
    });
  }
  function navigateBack(url) {
    startTransition(() => {
      // Transition type for the cause "nav backward"
      addTransitionType('nav-back');
      go(url);
    });
  }

  function go(url) {
    setRouterState({
      url,
      pendingNav() {
        window.history.pushState({}, "", url);
      },
    });
  }

  useEffect(() => {
    function handlePopState() {
      // 因为恢复必须是同步的，所以应该没有动画。
      // Even though it's a transition.
      startTransition(() => {
        setRouterState({
          url: document.location.pathname + document.location.search,
          pendingNav() {
            // Noop. URL has already updated.
          },
        });
      });
    }
    window.addEventListener("popstate", handlePopState);
    return () => {
      window.removeEventListener("popstate", handlePopState);
    };
  }, []);
  const pendingNav = routerState.pendingNav;
  useLayoutEffect(() => {
    pendingNav();
  }, [pendingNav]);

  return (
    <RouterContext
      value={{
        url: routerState.url,
        navigate,
        navigateBack,
        isPending,
        params: {},
      }}
    >
      {children}
    </RouterContext>
  );
}

const RouterContext = createContext({ url: "/", params: {} });

export function useRouter() {
  return use(RouterContext);
}

export function useIsNavPending() {
  return use(RouterContext).isPending;
}

```

```css src/styles.css hidden
@font-face {
  font-family: Optimistic Text;
  src: url(https://react.dev/fonts/Optimistic_Text_W_Rg.woff2) format("woff2");
  font-weight: 400;
  font-style: normal;
  font-display: swap;
}

@font-face {
  font-family: Optimistic Text;
  src: url(https://react.dev/fonts/Optimistic_Text_W_Md.woff2) format("woff2");
  font-weight: 500;
  font-style: normal;
  font-display: swap;
}

@font-face {
  font-family: Optimistic Text;
  src: url(https://react.dev/fonts/Optimistic_Text_W_Bd.woff2) format("woff2");
  font-weight: 600;
  font-style: normal;
  font-display: swap;
}

@font-face {
  font-family: Optimistic Text;
  src: url(https://react.dev/fonts/Optimistic_Text_W_Bd.woff2) format("woff2");
  font-weight: 700;
  font-style: normal;
  font-display: swap;
}

* {
  box-sizing: border-box;
}

html {
  background-image: url(https://react.dev/images/meta-gradient-dark.png);
  background-size: 100%;
  background-position: -100%;
  background-color: rgb(64 71 86);
  background-repeat: no-repeat;
  height: 100%;
  width: 100%;
}

body {
  font-family: Optimistic Text, -apple-system, ui-sans-serif, system-ui, sans-serif, Apple Color Emoji, Segoe UI Emoji, Segoe UI Symbol, Noto Color Emoji;
  padding: 10px 0 10px 0;
  margin: 0;
  display: flex;
  justify-content: center;
}

#root {
  flex: 1 1;
  height: auto;
  background-color: #fff;
  border-radius: 10px;
  max-width: 450px;
  min-height: 600px;
  padding-bottom: 10px;
}

h1 {
  margin-top: 0;
  font-size: 22px;
}

h2 {
  margin-top: 0;
  font-size: 20px;
}

h3 {
  margin-top: 0;
  font-size: 18px;
}

h4 {
  margin-top: 0;
  font-size: 16px;
}

h5 {
  margin-top: 0;
  font-size: 14px;
}

h6 {
  margin-top: 0;
  font-size: 12px;
}

code {
  font-size: 1.2em;
}

ul {
  padding-inline-start: 20px;
}

.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  padding: 0;
  margin: -1px;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  white-space: nowrap;
  border-width: 0;
}

.absolute {
  position: absolute;
}

.overflow-visible {
  overflow: visible;
}

.visible {
  overflow: visible;
}

.fit {
  width: fit-content;
}


/* Layout */
.page {
  display: flex;
  flex-direction: column;
  height: 100%;
}

.top-hero {
  height: 200px;
  display: flex;
  justify-content: center;
  align-items: center;
  background-image: conic-gradient(
      from 90deg at -10% 100%,
      #2b303b 0deg,
      #2b303b 90deg,
      #16181d 1turn
  );
}

.bottom {
  flex: 1;
  overflow: auto;
}

.top-nav {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 0;
  padding: 0 12px;
  top: 0;
  width: 100%;
  height: 44px;
  color: #23272f;
  font-weight: 700;
  font-size: 20px;
  z-index: 100;
  cursor: default;
}

.content {
  padding: 0 12px;
  margin-top: 4px;
}


.loader {
  color: #23272f;
  font-size: 3px;
  width: 1em;
  margin-right: 18px;
  height: 1em;
  border-radius: 50%;
  position: relative;
  text-indent: -9999em;
  animation: loading-spinner 1.3s infinite linear;
  animation-delay: 200ms;
  transform: translateZ(0);
}

@keyframes loading-spinner {
  0%,
  100% {
    box-shadow: 0 -3em 0 0.2em,
    2em -2em 0 0em, 3em 0 0 -1em,
    2em 2em 0 -1em, 0 3em 0 -1em,
    -2em 2em 0 -1em, -3em 0 0 -1em,
    -2em -2em 0 0;
  }
  12.5% {
    box-shadow: 0 -3em 0 0, 2em -2em 0 0.2em,
    3em 0 0 0, 2em 2em 0 -1em, 0 3em 0 -1em,
    -2em 2em 0 -1em, -3em 0 0 -1em,
    -2em -2em 0 -1em;
  }
  25% {
    box-shadow: 0 -3em 0 -0.5em,
    2em -2em 0 0, 3em 0 0 0.2em,
    2em 2em 0 0, 0 3em 0 -1em,
    -2em 2em 0 -1em, -3em 0 0 -1em,
    -2em -2em 0 -1em;
  }
  37.5% {
    box-shadow: 0 -3em 0 -1em, 2em -2em 0 -1em,
    3em 0em 0 0, 2em 2em 0 0.2em, 0 3em 0 0em,
    -2em 2em 0 -1em, -3em 0em 0 -1em, -2em -2em 0 -1em;
  }
  50% {
    box-shadow: 0 -3em 0 -1em, 2em -2em 0 -1em,
    3em 0 0 -1em, 2em 2em 0 0em, 0 3em 0 0.2em,
    -2em 2em 0 0, -3em 0em 0 -1em, -2em -2em 0 -1em;
  }
  62.5% {
    box-shadow: 0 -3em 0 -1em, 2em -2em 0 -1em,
    3em 0 0 -1em, 2em 2em 0 -1em, 0 3em 0 0,
    -2em 2em 0 0.2em, -3em 0 0 0, -2em -2em 0 -1em;
  }
  75% {
    box-shadow: 0em -3em 0 -1em, 2em -2em 0 -1em,
    3em 0em 0 -1em, 2em 2em 0 -1em, 0 3em 0 -1em,
    -2em 2em 0 0, -3em 0em 0 0.2em, -2em -2em 0 0;
  }
  87.5% {
    box-shadow: 0em -3em 0 0, 2em -2em 0 -1em,
    3em 0 0 -1em, 2em 2em 0 -1em, 0 3em 0 -1em,
    -2em 2em 0 0, -3em 0em 0 0, -2em -2em 0 0.2em;
  }
}

/* LikeButton */
.like-button {
  outline-offset: 2px;
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
  width: 2.5rem;
  height: 2.5rem;
  cursor: pointer;
  border-radius: 9999px;
  border: none;
  outline: none 2px;
  color: #5e687e;
  background: none;
}

.like-button:focus {
  color: #a6423a;
  background-color: rgba(166, 66, 58, .05);
}

.like-button:active {
  color: #a6423a;
  background-color: rgba(166, 66, 58, .05);
  transform: scaleX(0.95) scaleY(0.95);
}

.like-button:hover {
  background-color: #f6f7f9;
}

.like-button.liked {
  color: #a6423a;
}

/* Icons */
@keyframes circle {
  0% {
    transform: scale(0);
    stroke-width: 16px;
  }

  50% {
    transform: scale(.5);
    stroke-width: 16px;
  }

  to {
    transform: scale(1);
    stroke-width: 0;
  }
}

.circle {
  color: rgba(166, 66, 58, .5);
  transform-origin: center;
  transition-property: all;
  transition-duration: .15s;
  transition-timing-function: cubic-bezier(.4,0,.2,1);
}

.circle.liked.animate {
  animation: circle .3s forwards;
}

.heart {
  width: 1.5rem;
  height: 1.5rem;
}

.heart.liked {
  transform-origin: center;
  transition-property: all;
  transition-duration: .15s;
  transition-timing-function: cubic-bezier(.4, 0, .2, 1);
}

.heart.liked.animate {
  animation: scale .35s ease-in-out forwards;
}

.control-icon {
  color: hsla(0, 0%, 100%, .5);
  filter:  drop-shadow(0 20px 13px rgba(0, 0, 0, .03)) drop-shadow(0 8px 5px rgba(0, 0, 0, .08));
}

.chevron-left {
  margin-top: 2px;
  rotate: 90deg;
}


/* Video */
.thumbnail {
  position: relative;
  aspect-ratio: 16 / 9;
  display: flex;
  overflow: hidden;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  border-radius: 0.5rem;
  outline-offset: 2px;
  width: 8rem;
  vertical-align: middle;
  background-color: #ffffff;
  background-size: cover;
  user-select: none;
}

.thumbnail.blue {
  background-image: conic-gradient(at top right, #c76a15, #087ea4, #2b3491);
}

.thumbnail.red {
  background-image: conic-gradient(at top right, #c76a15, #a6423a, #2b3491);
}

.thumbnail.green {
  background-image: conic-gradient(at top right, #c76a15, #388f7f, #2b3491);
}

.thumbnail.purple {
  background-image: conic-gradient(at top right, #c76a15, #575fb7, #2b3491);
}

.thumbnail.yellow {
  background-image: conic-gradient(at top right, #c76a15, #FABD62, #2b3491);
}

.thumbnail.gray {
  background-image: conic-gradient(at top right, #c76a15, #4E5769, #2b3491);
}

.video {
  display: flex;
  flex-direction: row;
  gap: 0.75rem;
  align-items: center;
}

.video .link {
  display: flex;
  flex-direction: row;
  flex: 1 1 0;
  gap: 0.125rem;
  outline-offset: 4px;
  cursor: pointer;
}

.video .info {
  display: flex;
  flex-direction: column;
  justify-content: center;
  margin-left: 8px;
  gap: 0.125rem;
}

.video .info:hover {
  text-decoration: underline;
}

.video-title {
  font-size: 15px;
  line-height: 1.25;
  font-weight: 700;
  color: #23272f;
}

.video-description {
  color: #5e687e;
  font-size: 13px;
}

/* Details */
.details .thumbnail {
  position: relative;
  aspect-ratio: 16 / 9;
  display: flex;
  overflow: hidden;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  border-radius: 0.5rem;
  outline-offset: 2px;
  width: 100%;
  vertical-align: middle;
  background-color: #ffffff;
  background-size: cover;
  user-select: none;
}

.video-details-title {
  margin-top: 8px;
}

.video-details-speaker {
  display: flex;
  gap: 8px;
  margin-top: 10px
}

.back {
  display: flex;
  align-items: center;
  margin-left: -5px;
  cursor: pointer;
}

.back:hover {
  text-decoration: underline;
}

.info-title {
  font-size: 1.5rem;
  font-weight: 700;
  line-height: 1.25;
  margin: 8px 0 0 0 ;
}

.info-description {
  margin: 8px 0 0 0;
}

.controls {
  cursor: pointer;
}

.fallback {
  background: #f6f7f8 linear-gradient(to right, #e6e6e6 5%, #cccccc 25%, #e6e6e6 35%) no-repeat;
  background-size: 800px 104px;
  display: block;
  line-height: 1.25;
  margin: 8px 0 0 0;
  border-radius: 5px;
  overflow: hidden;

  animation: 1s linear 1s infinite shimmer;
  animation-delay: 300ms;
  animation-duration: 1s;
  animation-fill-mode: forwards;
  animation-iteration-count: infinite;
  animation-name: shimmer;
  animation-timing-function: linear;
}


.fallback.title {
  width: 130px;
  height: 30px;

}

.fallback.description {
  width: 150px;
  height: 21px;
}

@keyframes shimmer {
  0% {
    background-position: -468px 0;
  }

  100% {
    background-position: 468px 0;
  }
}

.search {
  margin-bottom: 10px;
}
.search-input {
  width: 100%;
  position: relative;
}

.search-icon {
  position: absolute;
  top: 0;
  bottom: 0;
  inset-inline-start: 0;
  display: flex;
  align-items: center;
  padding-inline-start: 1rem;
  pointer-events: none;
  color: #99a1b3;
}

.search-input input {
  display: flex;
  padding-inline-start: 2.75rem;
  padding-top: 10px;
  padding-bottom: 10px;
  width: 100%;
  text-align: start;
  background-color: rgb(235 236 240);
  outline: 2px solid transparent;
  cursor: pointer;
  border: none;
  align-items: center;
  color: rgb(35 39 47);
  border-radius: 9999px;
  vertical-align: middle;
  font-size: 15px;
}

.search-input input:hover, .search-input input:active {
  background-color: rgb(235 236 240/ 0.8);
  color: rgb(35 39 47/ 0.8);
}

/* Home */
.video-list {
  position: relative;
}

.video-list .videos {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  overflow-y: auto;
  height: 100%;
}
```


```css src/animations.css
/* No additional animations needed */









/* Previously defined animations below */






/* Slide animations for Suspense the fallback down */
::view-transition-old(.slide-down) {
    animation: 150ms ease-out both fade-out, 150ms ease-out both slide-down;
}

::view-transition-new(.slide-up) {
    animation: 210ms ease-in 150ms both fade-in, 400ms ease-in both slide-up;
}

/* Animations for view transition classed added by transition type */
::view-transition-old(.slide-forward) {
    /* when sliding forward, the "old" page should slide out to left. */
    animation: 150ms cubic-bezier(0.4, 0, 1, 1) both fade-out,
    400ms cubic-bezier(0.4, 0, 0.2, 1) both slide-to-left;
}

::view-transition-new(.slide-forward) {
    /* when sliding forward, the "new" page should slide in from right. */
    animation: 210ms cubic-bezier(0, 0, 0.2, 1) 150ms both fade-in,
    400ms cubic-bezier(0.4, 0, 0.2, 1) both slide-from-right;
}

::view-transition-old(.slide-back) {
    /* when sliding back, the "old" page should slide out to right. */
    animation: 150ms cubic-bezier(0.4, 0, 1, 1) both fade-out,
    400ms cubic-bezier(0.4, 0, 0.2, 1) both slide-to-right;
}

::view-transition-new(.slide-back) {
    /* when sliding back, the "new" page should slide in from left. */
    animation: 210ms cubic-bezier(0, 0, 0.2, 1) 150ms both fade-in,
    400ms cubic-bezier(0.4, 0, 0.2, 1) both slide-from-left;
}

/* Keyframes to support our animations above. */
@keyframes slide-up {
    from {
        transform: translateY(10px);
    }
    to {
        transform: translateY(0);
    }
}

@keyframes slide-down {
    from {
        transform: translateY(0);
    }
    to {
        transform: translateY(10px);
    }
}

@keyframes fade-in {
    from {
        opacity: 0;
    }
}

@keyframes fade-out {
    to {
        opacity: 0;
    }
}

@keyframes slide-to-right {
    to {
        transform: translateX(50px);
    }
}

@keyframes slide-from-right {
    from {
        transform: translateX(50px);
    }
    to {
        transform: translateX(0);
    }
}

@keyframes slide-to-left {
    to {
        transform: translateX(-50px);
    }
}

@keyframes slide-from-left {
    from {
        transform: translateX(-50px);
    }
    to {
        transform: translateX(0);
    }
}

/* Default .slow-fade. */
::view-transition-old(.slow-fade) {
    animation-duration: 500ms;
}

::view-transition-new(.slow-fade) {
    animation-duration: 500ms;
}
```

```js src/index.js hidden
import React, {StrictMode} from 'react';
import {createRoot} from 'react-dom/client';
import './styles.css';
import './animations.css';

import App from './App';
import {Router} from './router';

const root = createRoot(document.getElementById('root'));
root.render(
  <StrictMode>
    <Router>
      <App />
    </Router>
  </StrictMode>
);
```

```json package.json hidden
{
  "dependencies": {
    "react": "canary",
    "react-dom": "canary",
    "react-scripts": "latest"
  },
  "scripts": {
    "start": "react-scripts start",
    "build": "react-scripts build",
    "test": "react-scripts test --env=jsdom",
    "eject": "react-scripts eject"
  }
}
```

</Sandpack>

### Pre-rendering with Activity {/*prerender-with-activity*/}

Sometimes, you may want to prepare the next part of the UI a user is likely to use ahead of time, so it's ready by the time they are ready to use it. This is especially useful if the next route needs to suspend on data it needs to render, because you can help ensure the data is already fetched before the user navigates.

For example, our app currently needs to suspend to load the data for each video when you select one. We can improve this by rendering all of the pages in a hidden `<Activity>` until the user navigates:

```js {2,5,8}
<ViewTransition>
  <Activity mode={url === '/' ? 'visible' : 'hidden'}>
    <Home />
  </Activity>
  <Activity mode={url === '/details/1' ? 'visible' : 'hidden'}>
    <Details id={id} />
  </Activity>
  <Activity mode={url === '/details/1' ? 'visible' : 'hidden'}>
    <Details id={id} />
  </Activity>
<ViewTransition>
```

With this update, if the content on the next page has time to pre-render, it will animate in without the Suspense fallback. Click a video, and notice that the video title and description on the Details page render immediately, without a fallback:

<Sandpack>

```js src/App.js
import { Activity, ViewTransition, use } from "react"; import Details from "./Details"; import Home from "./Home"; import { useRouter } from "./router"; import {fetchVideos} from './data';

export default function App() {
  const { url } = useRouter();
  const videoId = url.split("/").pop();
  const videos = use(fetchVideos());

  return (
    <ViewTransition>
      {/* 在视图过渡中渲染视频以预渲染它们 */}
      {videos.map(({id}) => (
        <Activity key={id} mode={videoId === id ? 'visible' : 'hidden'}>
          <Details id={id}/>
        </Activity>
      ))}
      <Activity mode={url === '/' ? 'visible' : 'hidden'}>
        <Home />
      </Activity>
    </ViewTransition>
  );
}
```

```js src/Details.js
import { use, Suspense, ViewTransition } from "react"; import { fetchVideo, fetchVideoDetails } from "./data"; import { Thumbnail, VideoControls } from "./Videos"; import { useRouter } from "./router"; import Layout from "./Layout"; import { ChevronLeft } from "./Icons";

function VideoDetails({id}) {
  // Animate from Suspense fallback to content.
  // If this is pre-rendered then the fallback
  // won't need to show.
  return (
    <Suspense
      fallback={
        // Animate the fallback down.
        <ViewTransition exit="slide-down">
          <VideoInfoFallback />
        </ViewTransition>
      }
    >
      {/* Animate the content up */}
      <ViewTransition enter="slide-up">
        <VideoInfo id={id} />
      </ViewTransition>
    </Suspense>
  );
}

function VideoInfoFallback() {
  return (
    <>
      <div className="fallback title"></div>
      <div className="fallback description"></div>
    </>
  );
}

export default function Details({id}) {
  const { url, navigateBack } = useRouter();
  const video = use(fetchVideo(id));

  return (
    <Layout
      heading={
        <div
          className="fit back"
          onClick={() => {
            navigateBack("/");
          }}
        >
          <ChevronLeft /> Back
        </div>
      }
    >
      <div className="details">
        <Thumbnail video={video} large>
          <VideoControls />
        </Thumbnail>
        <VideoDetails id={video.id} />
      </div>
    </Layout>
  );
}

function VideoInfo({ id }) {
  const details = use(fetchVideoDetails(id));
  return (
    <>
      <p className="info-title">{details.title}</p>
      <p className="info-description">{details.description}</p>
    </>
  );
}
```

```js src/Home.js hidden
import { useId, useState, use, useDeferredValue, ViewTransition } from "react";import { Video } from "./Videos";import Layout from "./Layout";import { fetchVideos } from "./data";import { IconSearch } from "./Icons";

function SearchList({searchText, videos}) {
  // 通过 useDeferredValue来激活(何时) 
  const deferredSearchText = useDeferredValue(searchText);
  const filteredVideos = filterVideos(videos, deferredSearchText);
  return (
    <div className="video-list">
      {filteredVideos.length === 0 && (
        <div className="no-results">No results</div>
      )}
      <div className="videos">
        {filteredVideos.map((video) => (
          // 对列表中的每一个子项目进行动画（何地）
          <ViewTransition key={video.id}>
            <Video video={video} />
          </ViewTransition>
        ))}
      </div>
    </div>
  );
}

export default function Home() {
  const videos = use(fetchVideos());
  const count = videos.length;
  const [searchText, setSearchText] = useState('');

  return (
    <Layout heading={<div className="fit">{count} Videos</div>}>
      <SearchInput value={searchText} onChange={setSearchText} />
      <SearchList videos={videos} searchText={searchText} />
    </Layout>
  );
}

function SearchInput({ value, onChange }) {
  const id = useId();
  return (
    <form className="search" onSubmit={(e) => e.preventDefault()}>
      <label htmlFor={id} className="sr-only">
        Search
      </label>
      <div className="search-input">
        <div className="search-icon">
          <IconSearch />
        </div>
        <input
          type="text"
          id={id}
          placeholder="Search"
          value={value}
          onChange={(e) => onChange(e.target.value)}
        />
      </div>
    </form>
  );
}

function filterVideos(videos, query) {
  const keywords = query
    .toLowerCase()
    .split(" ")
    .filter((s) => s !== "");
  if (keywords.length === 0) {
    return videos;
  }
  return videos.filter((video) => {
    const words = (video.title + " " + video.description)
      .toLowerCase()
      .split(" ");
    return keywords.every((kw) => words.some((w) => w.includes(kw)));
  });
}
```

```js src/Icons.js hidden
export function ChevronLeft() {
  return (
    <svg
      className="chevron-left"
      xmlns="http://www.w3.org/2000/svg"
      width="20"
      height="20"
      viewBox="0 0 20 20">
      <g fill="none" fillRule="evenodd" transform="translate(-446 -398)">
        <path
          fill="currentColor"
          fillRule="nonzero"
          d="M95.8838835,240.366117 C95.3957281,239.877961 94.6042719,239.877961 94.1161165,240.366117 C93.6279612,240.854272 93.6279612,241.645728 94.1161165,242.133883 L98.6161165,246.633883 C99.1042719,247.122039 99.8957281,247.122039 100.383883,246.633883 L104.883883,242.133883 C105.372039,241.645728 105.372039,240.854272 104.883883,240.366117 C104.395728,239.877961 103.604272,239.877961 103.116117,240.366117 L99.5,243.982233 L95.8838835,240.366117 Z"
          transform="translate(356.5 164.5)"
        />
        <polygon points="446 418 466 418 466 398 446 398" />
      </g>
    </svg>
  );
}

export function PauseIcon() {
  return (
    <svg
      className="control-icon"
      style={{padding: '4px'}}
      width="100"
      height="100"
      viewBox="0 0 512 512"
      fill="none"
      xmlns="http://www.w3.org/2000/svg">
      <path
        fillRule="evenodd"
        clipRule="evenodd"
        d="M256 0C114.617 0 0 114.615 0 256s114.617 256 256 256 256-114.615 256-256S397.383 0 256 0zm-32 320c0 8.836-7.164 16-16 16h-32c-8.836 0-16-7.164-16-16V192c0-8.836 7.164-16 16-16h32c8.836 0 16 7.164 16 16v128zm128 0c0 8.836-7.164 16-16 16h-32c-8.836 0-16-7.164-16-16V192c0-8.836 7.164-16 16-16h32c8.836 0 16 7.164 16 16v128z"
        fill="currentColor"
      />
    </svg>
  );
}

export function PlayIcon() {
  return (
    <svg
      className="control-icon"
      width="100"
      height="100"
      viewBox="0 0 72 72"
      fill="none"
      xmlns="http://www.w3.org/2000/svg">
      <path
        fillRule="evenodd"
        clipRule="evenodd"
        d="M36 69C54.2254 69 69 54.2254 69 36C69 17.7746 54.2254 3 36 3C17.7746 3 3 17.7746 3 36C3 54.2254 17.7746 69 36 69ZM52.1716 38.6337L28.4366 51.5801C26.4374 52.6705 24 51.2235 24 48.9464V23.0536C24 20.7764 26.4374 19.3295 28.4366 20.4199L52.1716 33.3663C54.2562 34.5034 54.2562 37.4966 52.1716 38.6337Z"
        fill="currentColor"
      />
    </svg>
  );
}
export function Heart({liked, animate}) {
  return (
    <>
      <svg
        className="absolute overflow-visible"
        viewBox="0 0 24 24"
        fill="none"
        xmlns="http://www.w3.org/2000/svg">
        <circle
          className={`circle ${liked ? 'liked' : ''} ${animate ? 'animate' : ''}`}
          cx="12"
          cy="12"
          r="11.5"
          fill="transparent"
          strokeWidth="0"
          stroke="currentColor"
        />
      </svg>

      <svg
        className={`heart ${liked ? 'liked' : ''} ${animate ? 'animate' : ''}`}
        viewBox="0 0 24 24"
        fill="none"
        xmlns="http://www.w3.org/2000/svg">
        {liked ? (
          <path
            d="M12 23a.496.496 0 0 1-.26-.074C7.023 19.973 0 13.743 0 8.68c0-4.12 2.322-6.677 6.058-6.677 2.572 0 5.108 2.387 5.134 2.41l.808.771.808-.771C12.834 4.387 15.367 2 17.935 2 21.678 2 24 4.558 24 8.677c0 5.06-7.022 11.293-11.74 14.246a.496.496 0 0 1-.26.074V23z"
            fill="currentColor"
          />
        ) : (
          <path
            fillRule="evenodd"
            clipRule="evenodd"
            d="m12 5.184-.808-.771-.004-.004C11.065 4.299 8.522 2.003 6 2.003c-3.736 0-6 2.558-6 6.677 0 4.47 5.471 9.848 10 13.079.602.43 1.187.82 1.74 1.167A.497.497 0 0 0 12 23v-.003c.09 0 .182-.026.26-.074C16.977 19.97 24 13.737 24 8.677 24 4.557 21.743 2 18 2c-2.569 0-5.166 2.387-5.192 2.413L12 5.184zm-.002 15.525c2.071-1.388 4.477-3.342 6.427-5.47C20.72 12.733 22 10.401 22 8.677c0-1.708-.466-2.855-1.087-3.55C20.316 4.459 19.392 4 18 4c-.726 0-1.63.364-2.5.9-.67.412-1.148.82-1.266.92-.03.025-.037.031-.019.014l-.013.013L12 7.949 9.832 5.88a10.08 10.08 0 0 0-1.33-.977C7.633 4.367 6.728 4.003 6 4.003c-1.388 0-2.312.459-2.91 1.128C2.466 5.826 2 6.974 2 8.68c0 1.726 1.28 4.058 3.575 6.563 1.948 2.127 4.352 4.078 6.423 5.466z"
            fill="currentColor"
          />
        )}
      </svg>
    </>
  );
}

export function IconSearch(props) {
  return (
    <svg width="1em" height="1em" viewBox="0 0 20 20">
      <path
        d="M14.386 14.386l4.0877 4.0877-4.0877-4.0877c-2.9418 2.9419-7.7115 2.9419-10.6533 0-2.9419-2.9418-2.9419-7.7115 0-10.6533 2.9418-2.9419 7.7115-2.9419 10.6533 0 2.9419 2.9418 2.9419 7.7115 0 10.6533z"
        stroke="currentColor"
        fill="none"
        strokeWidth="2"
        fillRule="evenodd"
        strokeLinecap="round"
        strokeLinejoin="round"></path>
    </svg>
  );
}
```

```js src/Layout.js hidden
import {ViewTransition} from 'react'; import { useIsNavPending } from "./router";

export default function Page({ heading, children }) {
  const isPending = useIsNavPending();
  return (
    <div className="page">
      <div className="top">
        <div className="top-nav">
          {/* Custom classes based on transition type. */}
          <ViewTransition
            name="nav"
            share={{
              'nav-forward': 'slide-forward',
              'nav-back': 'slide-back',
            }}>
            {heading}
          </ViewTransition>
          {isPending && <span className="loader"></span>}
        </div>
      </div>
      {/* Opt-out of ViewTransition for the content. */}
      {/* Content can define it's own ViewTransition. */}
      <ViewTransition default="none">
        <div className="bottom">
          <div className="content">{children}</div>
        </div>
      </ViewTransition>
    </div>
  );
}
```

```js src/LikeButton.js hidden
import {useState} from 'react';
import {Heart} from './Icons';

// A hack since we don't actually have a backend.
// Unlike local state, this survives videos being filtered.
const likedVideos = new Set();

export default function LikeButton({video}) {
  const [isLiked, setIsLiked] = useState(() => likedVideos.has(video.id));
  const [animate, setAnimate] = useState(false);
  return (
    <button
      className={`like-button ${isLiked && 'liked'}`}
      aria-label={isLiked ? 'Unsave' : 'Save'}
      onClick={() => {
        const nextIsLiked = !isLiked;
        if (nextIsLiked) {
          likedVideos.add(video.id);
        } else {
          likedVideos.delete(video.id);
        }
        setAnimate(true);
        setIsLiked(nextIsLiked);
      }}>
      <Heart liked={isLiked} animate={animate} />
    </button>
  );
}
```

```js src/Videos.js hidden
import { useState, ViewTransition } from "react";
import LikeButton from "./LikeButton";
import { useRouter } from "./router";
import { PauseIcon, PlayIcon } from "./Icons";
import { startTransition } from "react";

export function Thumbnail({ video, children }) {
  // Add a name to animate with a shared element transition.
  // This uses the default animation, no additional css needed.
  return (
    <ViewTransition name={`video-${video.id}`}>
      <div
        aria-hidden="true"
        tabIndex={-1}
        className={`thumbnail ${video.image}`}
      >
        {children}
      </div>
    </ViewTransition>
  );
}

export function VideoControls() {
  const [isPlaying, setIsPlaying] = useState(false);

  return (
    <span
      className="controls"
      onClick={() =>
        startTransition(() => {
          setIsPlaying((p) => !p);
        })
      }
    >
      {isPlaying ? <PauseIcon /> : <PlayIcon />}
    </span>
  );
}

export function Video({ video }) {
  const { navigate } = useRouter();

  return (
    <div className="video">
      <div
        className="link"
        onClick={(e) => {
          e.preventDefault();
          navigate(`/video/${video.id}`);
        }}
      >
        <Thumbnail video={video}></Thumbnail>

        <div className="info">
          <div className="video-title">{video.title}</div>
          <div className="video-description">{video.description}</div>
        </div>
      </div>
      <LikeButton video={video} />
    </div>
  );
}
```


```js src/data.js hidden
const videos = [
  {
    id: '1',
    title: 'First video',
    description: 'Video description',
    image: 'blue',
  },
  {
    id: '2',
    title: 'Second video',
    description: 'Video description',
    image: 'red',
  },
  {
    id: '3',
    title: 'Third video',
    description: 'Video description',
    image: 'green',
  },
  {
    id: '4',
    title: 'Fourth video',
    description: 'Video description',
    image: 'purple',
  },
  {
    id: '5',
    title: 'Fifth video',
    description: 'Video description',
    image: 'yellow',
  },
  {
    id: '6',
    title: 'Sixth video',
    description: 'Video description',
    image: 'gray',
  },
];

let videosCache = new Map();
let videoCache = new Map();
let videoDetailsCache = new Map();
const VIDEO_DELAY = 1;
const VIDEO_DETAILS_DELAY = 1000;
export function fetchVideos() {
  if (videosCache.has(0)) {
    return videosCache.get(0);
  }
  const promise = new Promise((resolve) => {
    setTimeout(() => {
      resolve(videos);
    }, VIDEO_DELAY);
  });
  videosCache.set(0, promise);
  return promise;
}

export function fetchVideo(id) {
  if (videoCache.has(id)) {
    return videoCache.get(id);
  }
  const promise = new Promise((resolve) => {
    setTimeout(() => {
      resolve(videos.find((video) => video.id === id));
    }, VIDEO_DELAY);
  });
  videoCache.set(id, promise);
  return promise;
}

export function fetchVideoDetails(id) {
  if (videoDetailsCache.has(id)) {
    return videoDetailsCache.get(id);
  }
  const promise = new Promise((resolve) => {
    setTimeout(() => {
      resolve(videos.find((video) => video.id === id));
    }, VIDEO_DETAILS_DELAY);
  });
  videoDetailsCache.set(id, promise);
  return promise;
}
```

```js src/router.js hidden
import {useState, createContext, use, useTransition, useLayoutEffect, useEffect, addTransitionType} from "react";

export function Router({ children }) {
  const [isPending, startTransition] = useTransition();
  const [routerState, setRouterState] = useState({pendingNav: () => {}, url: document.location.pathname});
  function navigate(url) {
    startTransition(() => {
      // Transition type for the cause "nav forward"
      addTransitionType('nav-forward');
      go(url);
    });
  }
  function navigateBack(url) {
    startTransition(() => {
      // Transition type for the cause "nav backward"
      addTransitionType('nav-back');
      go(url);
    });
  }

  function go(url) {
    setRouterState({
      url,
      pendingNav() {
        window.history.pushState({}, "", url);
      },
    });
  }

  useEffect(() => {
    function handlePopState() {
      // 因为恢复必须是同步的，所以应该没有动画。
      // Even though it's a transition.
      startTransition(() => {
        setRouterState({
          url: document.location.pathname + document.location.search,
          pendingNav() {
            // Noop. URL has already updated.
          },
        });
      });
    }
    window.addEventListener("popstate", handlePopState);
    return () => {
      window.removeEventListener("popstate", handlePopState);
    };
  }, []);
  const pendingNav = routerState.pendingNav;
  useLayoutEffect(() => {
    pendingNav();
  }, [pendingNav]);

  return (
    <RouterContext
      value={{
        url: routerState.url,
        navigate,
        navigateBack,
        isPending,
        params: {},
      }}
    >
      {children}
    </RouterContext>
  );
}

const RouterContext = createContext({ url: "/", params: {} });

export function useRouter() {
  return use(RouterContext);
}

export function useIsNavPending() {
  return use(RouterContext).isPending;
}

```

```css src/styles.css hidden
@font-face {
  font-family: Optimistic Text;
  src: url(https://react.dev/fonts/Optimistic_Text_W_Rg.woff2) format("woff2");
  font-weight: 400;
  font-style: normal;
  font-display: swap;
}

@font-face {
  font-family: Optimistic Text;
  src: url(https://react.dev/fonts/Optimistic_Text_W_Md.woff2) format("woff2");
  font-weight: 500;
  font-style: normal;
  font-display: swap;
}

@font-face {
  font-family: Optimistic Text;
  src: url(https://react.dev/fonts/Optimistic_Text_W_Bd.woff2) format("woff2");
  font-weight: 600;
  font-style: normal;
  font-display: swap;
}

@font-face {
  font-family: Optimistic Text;
  src: url(https://react.dev/fonts/Optimistic_Text_W_Bd.woff2) format("woff2");
  font-weight: 700;
  font-style: normal;
  font-display: swap;
}

* {
  box-sizing: border-box;
}

html {
  background-image: url(https://react.dev/images/meta-gradient-dark.png);
  background-size: 100%;
  background-position: -100%;
  background-color: rgb(64 71 86);
  background-repeat: no-repeat;
  height: 100%;
  width: 100%;
}

body {
  font-family: Optimistic Text, -apple-system, ui-sans-serif, system-ui, sans-serif, Apple Color Emoji, Segoe UI Emoji, Segoe UI Symbol, Noto Color Emoji;
  padding: 10px 0 10px 0;
  margin: 0;
  display: flex;
  justify-content: center;
}

#root {
  flex: 1 1;
  height: auto;
  background-color: #fff;
  border-radius: 10px;
  max-width: 450px;
  min-height: 600px;
  padding-bottom: 10px;
}

h1 {
  margin-top: 0;
  font-size: 22px;
}

h2 {
  margin-top: 0;
  font-size: 20px;
}

h3 {
  margin-top: 0;
  font-size: 18px;
}

h4 {
  margin-top: 0;
  font-size: 16px;
}

h5 {
  margin-top: 0;
  font-size: 14px;
}

h6 {
  margin-top: 0;
  font-size: 12px;
}

code {
  font-size: 1.2em;
}

ul {
  padding-inline-start: 20px;
}

.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  padding: 0;
  margin: -1px;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  white-space: nowrap;
  border-width: 0;
}

.absolute {
  position: absolute;
}

.overflow-visible {
  overflow: visible;
}

.visible {
  overflow: visible;
}

.fit {
  width: fit-content;
}


/* Layout */
.page {
  display: flex;
  flex-direction: column;
  height: 100%;
}

.top-hero {
  height: 200px;
  display: flex;
  justify-content: center;
  align-items: center;
  background-image: conic-gradient(
      from 90deg at -10% 100%,
      #2b303b 0deg,
      #2b303b 90deg,
      #16181d 1turn
  );
}

.bottom {
  flex: 1;
  overflow: auto;
}

.top-nav {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 0;
  padding: 0 12px;
  top: 0;
  width: 100%;
  height: 44px;
  color: #23272f;
  font-weight: 700;
  font-size: 20px;
  z-index: 100;
  cursor: default;
}

.content {
  padding: 0 12px;
  margin-top: 4px;
}


.loader {
  color: #23272f;
  font-size: 3px;
  width: 1em;
  margin-right: 18px;
  height: 1em;
  border-radius: 50%;
  position: relative;
  text-indent: -9999em;
  animation: loading-spinner 1.3s infinite linear;
  animation-delay: 200ms;
  transform: translateZ(0);
}

@keyframes loading-spinner {
  0%,
  100% {
    box-shadow: 0 -3em 0 0.2em,
    2em -2em 0 0em, 3em 0 0 -1em,
    2em 2em 0 -1em, 0 3em 0 -1em,
    -2em 2em 0 -1em, -3em 0 0 -1em,
    -2em -2em 0 0;
  }
  12.5% {
    box-shadow: 0 -3em 0 0, 2em -2em 0 0.2em,
    3em 0 0 0, 2em 2em 0 -1em, 0 3em 0 -1em,
    -2em 2em 0 -1em, -3em 0 0 -1em,
    -2em -2em 0 -1em;
  }
  25% {
    box-shadow: 0 -3em 0 -0.5em,
    2em -2em 0 0, 3em 0 0 0.2em,
    2em 2em 0 0, 0 3em 0 -1em,
    -2em 2em 0 -1em, -3em 0 0 -1em,
    -2em -2em 0 -1em;
  }
  37.5% {
    box-shadow: 0 -3em 0 -1em, 2em -2em 0 -1em,
    3em 0em 0 0, 2em 2em 0 0.2em, 0 3em 0 0em,
    -2em 2em 0 -1em, -3em 0em 0 -1em, -2em -2em 0 -1em;
  }
  50% {
    box-shadow: 0 -3em 0 -1em, 2em -2em 0 -1em,
    3em 0 0 -1em, 2em 2em 0 0em, 0 3em 0 0.2em,
    -2em 2em 0 0, -3em 0em 0 -1em, -2em -2em 0 -1em;
  }
  62.5% {
    box-shadow: 0 -3em 0 -1em, 2em -2em 0 -1em,
    3em 0 0 -1em, 2em 2em 0 -1em, 0 3em 0 0,
    -2em 2em 0 0.2em, -3em 0 0 0, -2em -2em 0 -1em;
  }
  75% {
    box-shadow: 0em -3em 0 -1em, 2em -2em 0 -1em,
    3em 0em 0 -1em, 2em 2em 0 -1em, 0 3em 0 -1em,
    -2em 2em 0 0, -3em 0em 0 0.2em, -2em -2em 0 0;
  }
  87.5% {
    box-shadow: 0em -3em 0 0, 2em -2em 0 -1em,
    3em 0 0 -1em, 2em 2em 0 -1em, 0 3em 0 -1em,
    -2em 2em 0 0, -3em 0em 0 0, -2em -2em 0 0.2em;
  }
}

/* LikeButton */
.like-button {
  outline-offset: 2px;
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
  width: 2.5rem;
  height: 2.5rem;
  cursor: pointer;
  border-radius: 9999px;
  border: none;
  outline: none 2px;
  color: #5e687e;
  background: none;
}

.like-button:focus {
  color: #a6423a;
  background-color: rgba(166, 66, 58, .05);
}

.like-button:active {
  color: #a6423a;
  background-color: rgba(166, 66, 58, .05);
  transform: scaleX(0.95) scaleY(0.95);
}

.like-button:hover {
  background-color: #f6f7f9;
}

.like-button.liked {
  color: #a6423a;
}

/* Icons */
@keyframes circle {
  0% {
    transform: scale(0);
    stroke-width: 16px;
  }

  50% {
    transform: scale(.5);
    stroke-width: 16px;
  }

  to {
    transform: scale(1);
    stroke-width: 0;
  }
}

.circle {
  color: rgba(166, 66, 58, .5);
  transform-origin: center;
  transition-property: all;
  transition-duration: .15s;
  transition-timing-function: cubic-bezier(.4,0,.2,1);
}

.circle.liked.animate {
  animation: circle .3s forwards;
}

.heart {
  width: 1.5rem;
  height: 1.5rem;
}

.heart.liked {
  transform-origin: center;
  transition-property: all;
  transition-duration: .15s;
  transition-timing-function: cubic-bezier(.4, 0, .2, 1);
}

.heart.liked.animate {
  animation: scale .35s ease-in-out forwards;
}

.control-icon {
  color: hsla(0, 0%, 100%, .5);
  filter:  drop-shadow(0 20px 13px rgba(0, 0, 0, .03)) drop-shadow(0 8px 5px rgba(0, 0, 0, .08));
}

.chevron-left {
  margin-top: 2px;
  rotate: 90deg;
}


/* Video */
.thumbnail {
  position: relative;
  aspect-ratio: 16 / 9;
  display: flex;
  overflow: hidden;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  border-radius: 0.5rem;
  outline-offset: 2px;
  width: 8rem;
  vertical-align: middle;
  background-color: #ffffff;
  background-size: cover;
  user-select: none;
}

.thumbnail.blue {
  background-image: conic-gradient(at top right, #c76a15, #087ea4, #2b3491);
}

.thumbnail.red {
  background-image: conic-gradient(at top right, #c76a15, #a6423a, #2b3491);
}

.thumbnail.green {
  background-image: conic-gradient(at top right, #c76a15, #388f7f, #2b3491);
}

.thumbnail.purple {
  background-image: conic-gradient(at top right, #c76a15, #575fb7, #2b3491);
}

.thumbnail.yellow {
  background-image: conic-gradient(at top right, #c76a15, #FABD62, #2b3491);
}

.thumbnail.gray {
  background-image: conic-gradient(at top right, #c76a15, #4E5769, #2b3491);
}

.video {
  display: flex;
  flex-direction: row;
  gap: 0.75rem;
  align-items: center;
}

.video .link {
  display: flex;
  flex-direction: row;
  flex: 1 1 0;
  gap: 0.125rem;
  outline-offset: 4px;
  cursor: pointer;
}

.video .info {
  display: flex;
  flex-direction: column;
  justify-content: center;
  margin-left: 8px;
  gap: 0.125rem;
}

.video .info:hover {
  text-decoration: underline;
}

.video-title {
  font-size: 15px;
  line-height: 1.25;
  font-weight: 700;
  color: #23272f;
}

.video-description {
  color: #5e687e;
  font-size: 13px;
}

/* Details */
.details .thumbnail {
  position: relative;
  aspect-ratio: 16 / 9;
  display: flex;
  overflow: hidden;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  border-radius: 0.5rem;
  outline-offset: 2px;
  width: 100%;
  vertical-align: middle;
  background-color: #ffffff;
  background-size: cover;
  user-select: none;
}

.video-details-title {
  margin-top: 8px;
}

.video-details-speaker {
  display: flex;
  gap: 8px;
  margin-top: 10px
}

.back {
  display: flex;
  align-items: center;
  margin-left: -5px;
  cursor: pointer;
}

.back:hover {
  text-decoration: underline;
}

.info-title {
  font-size: 1.5rem;
  font-weight: 700;
  line-height: 1.25;
  margin: 8px 0 0 0 ;
}

.info-description {
  margin: 8px 0 0 0;
}

.controls {
  cursor: pointer;
}

.fallback {
  background: #f6f7f8 linear-gradient(to right, #e6e6e6 5%, #cccccc 25%, #e6e6e6 35%) no-repeat;
  background-size: 800px 104px;
  display: block;
  line-height: 1.25;
  margin: 8px 0 0 0;
  border-radius: 5px;
  overflow: hidden;

  animation: 1s linear 1s infinite shimmer;
  animation-delay: 300ms;
  animation-duration: 1s;
  animation-fill-mode: forwards;
  animation-iteration-count: infinite;
  animation-name: shimmer;
  animation-timing-function: linear;
}


.fallback.title {
  width: 130px;
  height: 30px;

}

.fallback.description {
  width: 150px;
  height: 21px;
}

@keyframes shimmer {
  0% {
    background-position: -468px 0;
  }

  100% {
    background-position: 468px 0;
  }
}

.search {
  margin-bottom: 10px;
}
.search-input {
  width: 100%;
  position: relative;
}

.search-icon {
  position: absolute;
  top: 0;
  bottom: 0;
  inset-inline-start: 0;
  display: flex;
  align-items: center;
  padding-inline-start: 1rem;
  pointer-events: none;
  color: #99a1b3;
}

.search-input input {
  display: flex;
  padding-inline-start: 2.75rem;
  padding-top: 10px;
  padding-bottom: 10px;
  width: 100%;
  text-align: start;
  background-color: rgb(235 236 240);
  outline: 2px solid transparent;
  cursor: pointer;
  border: none;
  align-items: center;
  color: rgb(35 39 47);
  border-radius: 9999px;
  vertical-align: middle;
  font-size: 15px;
}

.search-input input:hover, .search-input input:active {
  background-color: rgb(235 236 240/ 0.8);
  color: rgb(35 39 47/ 0.8);
}

/* Home */
.video-list {
  position: relative;
}

.video-list .videos {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  overflow-y: auto;
  height: 100%;
}
```


```css src/animations.css
/* No additional animations needed */









/* Previously defined animations below */






/* Slide animations for Suspense the fallback down */
::view-transition-old(.slide-down) {
    animation: 150ms ease-out both fade-out, 150ms ease-out both slide-down;
}

::view-transition-new(.slide-up) {
    animation: 210ms ease-in 150ms both fade-in, 400ms ease-in both slide-up;
}

/* Animations for view transition classed added by transition type */
::view-transition-old(.slide-forward) {
    /* when sliding forward, the "old" page should slide out to left. */
    animation: 150ms cubic-bezier(0.4, 0, 1, 1) both fade-out,
    400ms cubic-bezier(0.4, 0, 0.2, 1) both slide-to-left;
}

::view-transition-new(.slide-forward) {
    /* when sliding forward, the "new" page should slide in from right. */
    animation: 210ms cubic-bezier(0, 0, 0.2, 1) 150ms both fade-in,
    400ms cubic-bezier(0.4, 0, 0.2, 1) both slide-from-right;
}

::view-transition-old(.slide-back) {
    /* when sliding back, the "old" page should slide out to right. */
    animation: 150ms cubic-bezier(0.4, 0, 1, 1) both fade-out,
    400ms cubic-bezier(0.4, 0, 0.2, 1) both slide-to-right;
}

::view-transition-new(.slide-back) {
    /* when sliding back, the "new" page should slide in from left. */
    animation: 210ms cubic-bezier(0, 0, 0.2, 1) 150ms both fade-in,
    400ms cubic-bezier(0.4, 0, 0.2, 1) both slide-from-left;
}

/* Keyframes to support our animations above. */
@keyframes slide-up {
    from {
        transform: translateY(10px);
    }
    to {
        transform: translateY(0);
    }
}

@keyframes slide-down {
    from {
        transform: translateY(0);
    }
    to {
        transform: translateY(10px);
    }
}

@keyframes fade-in {
    from {
        opacity: 0;
    }
}

@keyframes fade-out {
    to {
        opacity: 0;
    }
}

@keyframes slide-to-right {
    to {
        transform: translateX(50px);
    }
}

@keyframes slide-from-right {
    from {
        transform: translateX(50px);
    }
    to {
        transform: translateX(0);
    }
}

@keyframes slide-to-left {
    to {
        transform: translateX(-50px);
    }
}

@keyframes slide-from-left {
    from {
        transform: translateX(-50px);
    }
    to {
        transform: translateX(0);
    }
}

/* Default .slow-fade. */
::view-transition-old(.slow-fade) {
    animation-duration: 500ms;
}

::view-transition-new(.slow-fade) {
    animation-duration: 500ms;
}
```

```js src/index.js hidden
import React, {StrictMode} from 'react';
import {createRoot} from 'react-dom/client';
import './styles.css';
import './animations.css';

import App from './App';
import {Router} from './router';

const root = createRoot(document.getElementById('root'));
root.render(
  <StrictMode>
    <Router>
      <App />
    </Router>
  </StrictMode>
);
```

```json package.json hidden
{
  "dependencies": {
    "react": "canary",
    "react-dom": "canary",
    "react-scripts": "latest"
  },
  "scripts": {
    "start": "react-scripts start",
    "build": "react-scripts build",
    "test": "react-scripts test --env=jsdom",
    "eject": "react-scripts eject"
  }
}
```

</Sandpack>

### 使用 Activity 进行服务端渲染 {/*server-side-rendering-with-activity*/}

在使用服务端渲染（SSR）的页面上使用 Activity 时，有额外的优化。

如果页面的一部分使用 `mode="hidden"` 渲染，那么它将不会包含在 SSR 响应中。相反，React 会在页面其余部分进行水合（hydrate）的同时，为 Activity 内部的内容安排客户端渲染，优先处理屏幕上可见的内容。

对于使用 `mode="visible"` 渲染的 UI 部分，React 会降低 Activity 内容的水合优先级，类似于 Suspense 内容以较低优先级进行水合的方式。如果用户与页面交互，我们会在需要时优先处理边界内的水合。

这些是高级用例，但它们展示了 Activity 考虑的额外好处。

### Activity 的未来模式 {/*future-modes-for-activity*/}

未来，我们可能会为 Activity 添加更多模式。

例如，一个常见的用例是渲染模态框，其中之前的“非活动”页面在“活动”模态视图后面可见。“hidden”模式不适用于这种情况，因为它不可见且不包含在 SSR 中。

相反，我们正在考虑一种新模式，它会保持内容可见——并包含在 SSR 中——但保持它卸载并降低更新优先级。这种模式可能还需要“暂停”DOM 更新，因为在模态框打开时看到背景内容更新可能会分散注意力。

我们正在考虑的 Activity 的另一种模式是，如果使用了太多内存，能够自动销毁隐藏的 Activity 的状态。由于组件已经卸载，与消耗过多资源相比，销毁应用中最近最少使用的隐藏部分的状态可能更可取。

这些是我们仍在探索的领域，随着进展我们会分享更多信息。有关 Activity 当前包含的功能的更多信息，[请查看文档](/reference/react/Activity)。

---

# 正在开发的功能 {/*features-in-development*/}

我们还在开发功能来帮助解决以下常见问题。

在我们迭代可能的解决方案时，你可能会看到我们正在测试的一些潜在 API，这些 API 基于我们正在合并的 PR 进行分享。请记住，当我们尝试不同的想法时，我们通常会在尝试后更改或删除不同的解决方案。

如果我们过早分享正在开发的解决方案，可能会在社区中造成混乱和困惑。为了平衡透明度和减少困惑，我们只分享了当前正在为其开发解决方案的问题，而不分享我们心中的特定解决方案。

随着这些功能的进展，我们将在博客上宣布它们，并附上文档，以便你可以尝试它们。

## React 性能追踪 {/*react-performance-tracks*/}

我们正在开发一套新的自定义性能分析器追踪功能，使用浏览器 API [允许添加自定义追踪](https://developer.chrome.com/docs/devtools/performance/extension)，以提供有关 React 应用性能的更多信息。

这个功能仍在开发中，因此我们还没有准备好发布文档将其作为实验性功能完全发布。当使用 React 的实验版本时，你可以获得一个预览，它会自动将性能追踪添加到分析中：

<div style={{display: 'flex', justifyContent: 'center', marginBottom: '1rem'}}>
  <picture >
      <source srcset="/images/blog/react-labs-april-2025/perf_tracks.png" />
      <img className="w-full light-image" src="/images/blog/react-labs-april-2025/perf_tracks.webp" />
  </picture>
  <picture >
      <source srcset="/images/blog/react-labs-april-2025/perf_tracks_dark.png" />
      <img className="w-full dark-image" src="/images/blog/react-labs-april-2025/perf_tracks_dark.webp" />
  </picture>
</div>

我们计划解决一些已知问题，如性能问题，以及调度器追踪不总是能在 Suspended 树之间“连接”工作，所以它还不完全可用。我们还在收集早期采用者的反馈，以改进追踪的设计和可用性。

一旦我们解决了这些问题，我们将发布实验性文档并分享它已准备好供尝试。

---

## 自动 Effect 依赖 {/*automatic-effect-dependencies*/}

当我们发布 hooks 时，我们有三个动机：

- **在组件之间共享代码**：hooks 替代了像 render props 和高阶组件这样的模式，允许你在不改变组件层次结构的情况下重用有状态逻辑。
- **以函数而非生命周期的方式思考**：hooks 让你可以根据相关的部分（如设置订阅或获取数据）将一个组件拆分成更小的函数，而不是强制基于生命周期方法进行拆分。
- **支持提前编译**：hooks 的设计支持提前编译，减少了由生命周期方法和类的限制导致的无意去优化的陷阱。

自发布以来，hooks 在 **在组件之间共享代码** 方面取得了成功。Hooks 现在是在组件之间共享逻辑的首选方式，render props 和高阶组件的使用场景减少了。Hooks 还成功支持了像 Fast Refresh 这样的功能，这在类组件中是不可能实现的。

### Effects 可能很难理解 {/*effects-can-be-hard*/}

不幸的是，有些 hooks 仍然很难以函数而非生命周期的方式思考。特别是 Effects 仍然很难理解，是我们从开发者那里听到的最常见的痛点。去年，我们花了大量时间研究 Effects 的使用方式，以及如何简化这些用例并使其更容易理解。

我们发现，困惑通常来自于在不需要的情况下使用 Effect。[你可能不需要 Effect](/learn/you-might-not-need-an-effect) 指南涵盖了许多 Effects 不是正确解决方案的情况。然而，即使 Effect 是解决问题的正确选择，Effects 仍然可能比类组件生命周期更难理解。

我们认为造成困惑的原因之一是开发者从 **组件** 的角度（像生命周期一样）思考 Effects，而不是从 **Effects** 的角度（Effect 做什么）思考。

让我们看一个[文档中的例子](/learn/lifecycle-of-reactive-effects#thinking-from-the-effects-perspective)：

```js
useEffect(() => {
  // 你的 Effect 连接到由 roomId 指定的房间...
  const connection = createConnection(serverUrl, roomId);
  connection.connect();
  return () => {
    // ...直到它断开连接
    connection.disconnect();
  };
}, [roomId]);
```

许多用户会将这段代码理解为“在挂载时，连接到 roomId。每当 `roomId` 改变时，断开与旧房间的连接并重新创建连接”。然而，这是从组件的生命周期角度思考，这意味着你需要考虑每个组件生命周期状态才能正确编写 Effect。这可能很困难，所以当使用组件角度时，Effects 看起来比类生命周期更难理解是可以理解的。

### 没有依赖的 Effects {/*effects-without-dependencies*/}

相反，最好从 Effect 的角度思考。Effect 不了解组件的生命周期。它只描述如何开始同步和如何停止同步。当用户以这种方式思考 Effects 时，他们的 Effects 往往更容易编写，并且更能适应根据需要多次启动和停止。

我们花了一些时间研究为什么 Effects 会从组件角度思考，我们认为原因之一是依赖数组。由于你必须编写它，它就在那里，提醒你你在"响应"什么，并引导你进入"当这些值改变时做这件事"的心智模型。

当我们发布 hooks 时，我们知道可以通过提前编译使它们更易于使用。使用 React 编译器，你现在可以在大多数情况下避免自己编写 `useCallback` 和 `useMemo`。对于 Effects，编译器可以为你插入依赖项：

```js
useEffect(() => {
  const connection = createConnection(serverUrl, roomId);
  connection.connect();
  return () => {
    connection.disconnect();
  };
}); // 编译器插入的依赖项。
```

使用这段代码，React 编译器可以为你推断依赖项并自动插入它们，这样你就不需要看到或编写它们。通过像[IDE 扩展](#compiler-ide-extension)和[`useEffectEvent`](/reference/react/useEffectEvent)这样的功能，我们可以提供一个 CodeLens 来显示编译器在你需要调试时插入的内容，或通过移除依赖项来优化。这有助于强化编写 Effects 的正确心智模型，即 Effects 可以在任何时候运行，以将你的组件或 hook 的状态与其他内容同步。

我们希望自动插入依赖项不仅更容易编写，而且通过迫使你从 Effect 的作用角度思考，而不是从组件生命周期角度思考，使它们更容易理解。

---

## 编译器 IDE 扩展 {/*compiler-ide-extension*/}

2025 晚些时候 [我们分享了](/blog/2025/10/07/react-compiler-1) React 编译器第一个稳定版本，我们将继续投资来进行更多改进。

我们还开始探索使用 React 编译器提供信息的方法，以改进对代码的理解和调试。我们开始探索的一个想法是一个由 React 编译器驱动的基于 LSP 的新实验性 React IDE 扩展，类似于 [Lauren Tan 在 React Conf 演讲](https://conf2024.react.dev/talks/5)中使用的扩展。

我们的想法是，我们可以使用编译器的静态分析直接在你的 IDE 中提供更多信息、建议和优化机会。例如，我们可以为违反 React 规则的代码提供诊断，悬停显示组件和 hooks 是否被编译器优化，或者提供 CodeLens 来查看[自动插入的 Effect 依赖项](#automatic-effect-dependencies)。

IDE 扩展仍处于早期探索阶段，但我们将在未来的更新中分享我们的进展。

---

## Fragment Refs {/*fragment-refs*/}

许多 DOM API，如事件管理、定位和焦点等，在使用 React 编写时很难组合。这通常导致开发者求助于 Effects，管理多个 Refs，或使用像 `findDOMNode`（在 React 19 中已移除）这样的 API。

我们正在探索向 Fragment 添加 refs，这些 refs 将指向一组 DOM 元素，而不仅仅是单个元素。我们希望这将简化管理多个子元素，并在调用 DOM API 时使编写可组合的 React 代码变得更容易。

Fragment refs 仍在研究中。当我们接近完成最终 API 时，我们将分享更多信息。

---

## 手势动画 {/*gesture-animations*/}

我们还在研究增强视图过渡以支持手势动画的方法，例如滑动打开菜单或滚动浏览照片轮播。

手势因以下几个原因带来新的挑战：

- **手势是连续的**：当你滑动时，动画与你的手指放置时间相关联，而不是触发并运行到完成。
- **手势不一定完成**：当你释放手指时，手势动画可以运行到完成，或者根据你滑动的距离恢复到原始状态（比如当你只是部分打开菜单时）。
- **手势颠倒了旧状态和新状态**：在动画过程中，你希望你正在从中进行动画的页面保持“活跃”和可交互。这颠倒了浏览器视图过渡模型，在该模型中，“旧”状态是快照，而“新”状态是实时 DOM。

我们相信已经找到了一种行之有效的方法，并可能引入一个新的 API 来触发手势过渡。目前，我们专注于发布 `<ViewTransition>`，之后再重新审视手势相关功能。

---

## 并发存储 {/*concurrent-stores*/}

当我们发布带有并发渲染的 React 18 时，我们还发布了 `useSyncExternalStore`，这样不使用 React 状态或上下文的外部存储库可以通过在存储更新时强制同步渲染来[支持并发渲染](https://github.com/reactwg/react-18/discussions/70)。

使用 `useSyncExternalStore` 是有代价的，因为它会强制退出过渡等并发功能，并强制现有内容显示 Suspense 后备方案。

现在 React 19 已经发布，我们正在重新审视这个问题领域，创建一个原语，通过 `use` API 完全支持并发外部存储：

```js
const value = use(store);
```

我们的目标是允许在渲染期间读取外部状态而不会撕裂，并与 React 提供的所有并发功能无缝协作。

这项研究仍处于早期阶段。当我们进一步推进时，我们将分享更多信息，以及新 API 的样子。

---

**感谢 [Aurora Scharff](https://bsky.app/profile/aurorascharff.no)、[Dan Abramov](https://bsky.app/profile/danabra.mov)、[Eli White](https://twitter.com/Eli_White)、[Lauren Tan](https://bsky.app/profile/no.lol)、[Luna Wei](https://github.com/lunaleaps)、[Matt Carroll](https://twitter.com/mattcarrollcode)、[Jack Pope](https://jackpope.me)、[Jason Bonta](https://threads.net/someextent)、[Jordan Brown](https://github.com/jbrown215)、[Jordan Eldredge](https://bsky.app/profile/capt.dev)、[Mofei Zhang](https://threads.net/z_mofei)、[Sebastien Lorber](https://bsky.app/profile/sebastienlorber.com)、[Sebastian Markbåge](https://bsky.app/profile/sebmarkbage.calyptus.eu) 和 [Tim Yung](https://github.com/yungsters) 审阅本文。**

---
# Source: critical-security-vulnerability-in-react-server-components.md
---
---
title: "Critical Security Vulnerability in React Server Components"
author: The React Team
date: 2025/12/03
description: There is an unauthenticated remote code execution vulnerability in React Server Components. A fix has been published in versions 19.0.1, 19.1.2, and 19.2.1. We recommend upgrading immediately.

---

December 3, 2025 by [The React Team](/community/team)

---

<Intro>

There is an unauthenticated remote code execution vulnerability in React Server Components.

We recommend upgrading immediately.

</Intro>

---

On November 29th, Lachlan Davidson reported a security vulnerability in React that allows unauthenticated remote code execution by exploiting a flaw in how React decodes payloads sent to React Server Function endpoints.

Even if your app does not implement any React Server Function endpoints it may still be vulnerable if your app supports React Server Components.

This vulnerability was disclosed as [CVE-2025-55182](https://www.cve.org/CVERecord?id=CVE-2025-55182) and is rated CVSS 10.0.

The vulnerability is present in versions 19.0, 19.1.0, 19.1.1, and 19.2.0 of:

* [react-server-dom-webpack](https://www.npmjs.com/package/react-server-dom-webpack)
* [react-server-dom-parcel](https://www.npmjs.com/package/react-server-dom-parcel)
* [react-server-dom-turbopack](https://www.npmjs.com/package/react-server-dom-turbopack?activeTab=readme)

## Immediate Action Required {/*immediate-action-required*/}

A fix was introduced in versions [19.0.1](https://github.com/facebook/react/releases/tag/v19.0.1), [19.1.2](https://github.com/facebook/react/releases/tag/v19.1.2), and [19.2.1](https://github.com/facebook/react/releases/tag/v19.2.1). If you are using any of the above packages please upgrade to any of the fixed versions immediately.

If your app’s React code does not use a server, your app is not affected by this vulnerability. If your app does not use a framework, bundler, or bundler plugin that supports React Server Components, your app is not affected by this vulnerability.

### Affected frameworks and bundlers {/*affected-frameworks-and-bundlers*/}

Some React frameworks and bundlers depended on, had peer dependencies for, or included the vulnerable React packages. The following React frameworks & bundlers are affected: [next](https://www.npmjs.com/package/next), [react-router](https://www.npmjs.com/package/react-router), [waku](https://www.npmjs.com/package/waku), [@parcel/rsc](https://www.npmjs.com/package/@parcel/rsc), [@vitejs/plugin-rsc](https://www.npmjs.com/package/@vitejs/plugin-rsc), and [rwsdk](https://www.npmjs.com/package/rwsdk).

See the [update instructions below](#update-instructions) for how to upgrade to these patches.

### Hosting Provider Mitigations {/*hosting-provider-mitigations*/}

We have worked with a number of hosting providers to apply temporary mitigations.

You should not depend on these to secure your app, and still update immediately.

### Vulnerability overview {/*vulnerability-overview*/}

[React Server Functions](https://react.dev/reference/rsc/server-functions) allow a client to call a function on a server. React provides integration points and tools that frameworks and bundlers use to help React code run on both the client and the server. React translates requests on the client into HTTP requests which are forwarded to a server. On the server, React translates the HTTP request into a function call and returns the needed data to the client.

An unauthenticated attacker could craft a malicious HTTP request to any Server Function endpoint that, when deserialized by React, achieves remote code execution on the server. Further details of the vulnerability will be provided after the rollout of the fix is complete.

## Update Instructions {/*update-instructions*/}

<Note>

These instructions have been updated to include the new vulnerabilities:

- **Denial of Service - High Severity**: [CVE-2025-55184](https://www.cve.org/CVERecord?id=CVE-2025-55184) and [CVE-2025-67779](https://www.cve.org/CVERecord?id=CVE-2025-67779) (CVSS 7.5)
- **Source Code Exposure - Medium Severity**: [CVE-2025-55183](https://www.cve.org/CVERecord?id=CVE-2025-55183) (CVSS 5.3)
- **Denial of Service - High Severity**: January 26, 2026 [CVE-2026-23864](https://www.cve.org/CVERecord?id=CVE-2026-23864) (CVSS 7.5)

See the [follow-up blog post](/blog/2025/12/11/denial-of-service-and-source-code-exposure-in-react-server-components) for more info.

-----

_Updated January 26, 2026._
</Note>

### Next.js {/*update-next-js*/}

All users should upgrade to the latest patched version in their release line:

```bash
npm install next@14.2.35  // for 13.3.x, 13.4.x, 13.5.x, 14.x
npm install next@15.0.8   // for 15.0.x
npm install next@15.1.12  // for 15.1.x
npm install next@15.2.9   // for 15.2.x
npm install next@15.3.9   // for 15.3.x
npm install next@15.4.11  // for 15.4.x
npm install next@15.5.10  // for 15.5.x
npm install next@16.0.11  // for 16.0.x
npm install next@16.1.5   // for 16.1.x

npm install next@15.6.0-canary.60   // for 15.x canary releases
npm install next@16.1.0-canary.19   // for 16.x canary releases
```

15.0.8, 15.1.12, 15.2.9, 15.3.9, 15.4.10, 15.5.10, 15.6.0-canary.61, 16.0.11, 16.1.5

If you are on version `13.3` or later version of Next.js 13 (`13.3.x`, `13.4.x`, or `13.5.x`) please upgrade to version `14.2.35`.

If you are on `next@14.3.0-canary.77` or a later canary release, downgrade to the latest stable 14.x release:

```bash
npm install next@14
```

See the [Next.js blog](https://nextjs.org/blog/security-update-2025-12-11) for the latest update instructions and the [previous changelog](https://nextjs.org/blog/CVE-2025-66478) for more info.

### React Router {/*update-react-router*/}

If you are using React Router's unstable RSC APIs, you should upgrade the following package.json dependencies if they exist:

```bash
npm install react@latest
npm install react-dom@latest
npm install react-server-dom-parcel@latest
npm install react-server-dom-webpack@latest
npm install @vitejs/plugin-rsc@latest
```

### Expo {/*expo*/}

To learn more about mitigating, read the article on [expo.dev/changelog](https://expo.dev/changelog/mitigating-critical-security-vulnerability-in-react-server-components).

### Redwood SDK {/*update-redwood-sdk*/}

Ensure you are on rwsdk>=1.0.0-alpha.0

For the latest beta version:

```bash
npm install rwsdk@latest
```

Upgrade to the latest `react-server-dom-webpack`:

```bash
npm install react@latest react-dom@latest react-server-dom-webpack@latest
```

See [Redwood docs](https://docs.rwsdk.com/migrating/) for more migration instructions.

### Waku {/*update-waku*/}

Upgrade to the latest `react-server-dom-webpack`:

```bash
npm install react@latest react-dom@latest react-server-dom-webpack@latest waku@latest
```

See [Waku announcement](https://github.com/wakujs/waku/discussions/1823) for more migration instructions.

### `@vitejs/plugin-rsc` {/*vitejs-plugin-rsc*/}

Upgrade to the latest RSC plugin:

```bash
npm install react@latest react-dom@latest @vitejs/plugin-rsc@latest
```

### `react-server-dom-parcel` {/*update-react-server-dom-parcel*/}

Update to the latest version:

 ```bash
 npm install react@latest react-dom@latest react-server-dom-parcel@latest
 ```

### `react-server-dom-turbopack` {/*update-react-server-dom-turbopack*/}

Update to the latest version:

 ```bash
 npm install react@latest react-dom@latest react-server-dom-turbopack@latest
 ```

### `react-server-dom-webpack` {/*update-react-server-dom-webpack*/}

Update to the latest version:

 ```bash
npm install react@latest react-dom@latest react-server-dom-webpack@latest
 ```


### React Native {/*react-native*/}

For React Native users not using a monorepo or `react-dom`, your `react` version should be pinned in your `package.json`, and there are no additional steps needed.

If you are using React Native in a monorepo, you should update _only_ the impacted packages if they are installed:

- `react-server-dom-webpack`
- `react-server-dom-parcel`
- `react-server-dom-turbopack`

This is required to mitigate the security advisory, but you do not need to update `react` and `react-dom` so this will not cause the version mismatch error in React Native.

See [this issue](https://github.com/facebook/react-native/issues/54772#issuecomment-3617929832) for more information.


## Timeline {/*timeline*/}

* **November 29th**: Lachlan Davidson reported the security vulnerability via [Meta Bug Bounty](https://bugbounty.meta.com/).
* **November 30th**: Meta security researchers confirmed and began working with the React team on a fix.
* **December 1st**: A fix was created and the React team began working with affected hosting providers and open source projects to validate the fix, implement mitigations and roll out the fix
* **December 3rd**: The fix was published to npm and the publicly disclosed as CVE-2025-55182.

## Attribution {/*attribution*/}

Thank you to [Lachlan Davidson](https://github.com/lachlan2k) for discovering, reporting, and working to help fix this vulnerability.

---
# Source: denial-of-service-and-source-code-exposure-in-react-server-components.md
---
---
title: "Denial of Service and Source Code Exposure in React Server Components"
author: The React Team
date: 2025/12/11
description: Security researchers have found and disclosed two additional vulnerabilities in React Server Components while attempting to exploit the patches in last week’s critical vulnerability. High vulnerability Denial of Service (CVE-2025-55184), and medium vulnerability Source Code Exposure (CVE-2025-55183)


---

December 11, 2025 by [The React Team](/community/team)

_Updated January 26, 2026._

---

<Intro>

Security researchers have found and disclosed two additional vulnerabilities in React Server Components while attempting to exploit the patches in last week’s critical vulnerability.

**These new vulnerabilities do not allow for Remote Code Execution.** The patch for React2Shell remains effective at mitigating the Remote Code Execution exploit.

</Intro>

---

The new vulnerabilities are disclosed as:

- **Denial of Service - High Severity**: [CVE-2025-55184](https://www.cve.org/CVERecord?id=CVE-2025-55184), [CVE-2025-67779](https://www.cve.org/CVERecord?id=CVE-2025-67779), and [CVE-2026-23864](https://www.cve.org/CVERecord?id=CVE-2026-23864) (CVSS 7.5)
- **Source Code Exposure - Medium Severity**: [CVE-2025-55183](https://www.cve.org/CVERecord?id=CVE-2025-55183) (CVSS 5.3)

We recommend upgrading immediately due to the severity of the newly disclosed vulnerabilities.

<Note>

#### The patches published earlier are vulnerable. {/*the-patches-published-earlier-are-vulnerable*/}

If you already updated for the previous vulnerabilities, you will need to update again.

If you updated to 19.0.3, 19.1.4, and 19.2.3, [these are incomplete](#additional-fix-published), and you will need to update again.

Please see [the instructions in the previous post](/blog/2025/12/03/critical-security-vulnerability-in-react-server-components#update-instructions) for upgrade steps.

-----

_Updated January 26, 2026._

</Note>

Further details of these vulnerabilities will be provided after the rollout of the fixes are complete.

## Immediate Action Required {/*immediate-action-required*/}

These vulnerabilities are present in the same packages and versions as [CVE-2025-55182](/blog/2025/12/03/critical-security-vulnerability-in-react-server-components).

This includes 19.0.0, 19.0.1, 19.0.2, 19.0.3, 19.1.0, 19.1.1, 19.1.2, 19.1.3, 19.2.0, 19.2.1, 19.2.2, and 19.2.3 of:

* [react-server-dom-webpack](https://www.npmjs.com/package/react-server-dom-webpack)
* [react-server-dom-parcel](https://www.npmjs.com/package/react-server-dom-parcel)
* [react-server-dom-turbopack](https://www.npmjs.com/package/react-server-dom-turbopack?activeTab=readme)

Fixes were backported to versions 19.0.4, 19.1.5, and 19.2.4. If you are using any of the above packages please upgrade to any of the fixed versions immediately.

As before, if your app’s React code does not use a server, your app is not affected by these vulnerabilities. If your app does not use a framework, bundler, or bundler plugin that supports React Server Components, your app is not affected by these vulnerabilities.

<Note>

#### It’s common for critical CVEs to uncover follow‑up vulnerabilities. {/*its-common-for-critical-cves-to-uncover-followup-vulnerabilities*/}

When a critical vulnerability is disclosed, researchers scrutinize adjacent code paths looking for variant exploit techniques to test whether the initial mitigation can be bypassed.

This pattern shows up across the industry, not just in JavaScript. For example, after [Log4Shell](https://nvd.nist.gov/vuln/detail/cve-2021-44228), additional CVEs ([1](https://nvd.nist.gov/vuln/detail/cve-2021-45046), [2](https://nvd.nist.gov/vuln/detail/cve-2021-45105)) were reported as the community probed the original fix.

Additional disclosures can be frustrating, but they are generally a sign of a healthy response cycle.

</Note>

### Affected frameworks and bundlers {/*affected-frameworks-and-bundlers*/}

Some React frameworks and bundlers depended on, had peer dependencies for, or included the vulnerable React packages. The following React frameworks & bundlers are affected: [next](https://www.npmjs.com/package/next), [react-router](https://www.npmjs.com/package/react-router), [waku](https://www.npmjs.com/package/waku), [@parcel/rsc](https://www.npmjs.com/package/@parcel/rsc), [@vite/rsc-plugin](https://www.npmjs.com/package/@vitejs/plugin-rsc), and [rwsdk](https://www.npmjs.com/package/rwsdk).

Please see [the instructions in the previous post](/blog/2025/12/03/critical-security-vulnerability-in-react-server-components#update-instructions) for upgrade steps.

### Hosting Provider Mitigations {/*hosting-provider-mitigations*/}

As before, we have worked with a number of hosting providers to apply temporary mitigations.

You should not depend on these to secure your app, and still update immediately.

### React Native {/*react-native*/}

For React Native users not using a monorepo or `react-dom`, your `react` version should be pinned in your `package.json`, and there are no additional steps needed.

If you are using React Native in a monorepo, you should update _only_ the impacted packages if they are installed:

- `react-server-dom-webpack`
- `react-server-dom-parcel`
- `react-server-dom-turbopack`

This is required to mitigate the security advisories, but you do not need to update `react` and `react-dom` so this will not cause the version mismatch error in React Native.

See [this issue](https://github.com/facebook/react-native/issues/54772#issuecomment-3617929832) for more information.

---

## High Severity: Multiple Denial of Service {/*high-severity-multiple-denial-of-service*/}

**CVEs:** [CVE-2026-23864](https://www.cve.org/CVERecord?id=CVE-2026-23864)
**Base Score:** 7.5 (High)
**Date**: January 26, 2025

Security researchers discovered additional DoS vulnerabilities still exist in React Server Components.

The vulnerabilities are triggered by sending specially crafted HTTP requests to Server Function endpoints, and could lead to server crashes, out-of-memory exceptions or excessive CPU usage; depending on the vulnerable code path being exercised, the application configuration and application code.

The patches published January 26th mitigate these DoS vulnerabilities.

<Note>

#### Additional fixes published {/*additional-fix-published*/}

The original fix addressing the DoS in [CVE-2025-55184](https://www.cve.org/CVERecord?id=CVE-2025-55184) was incomplete.

This left previous versions vulnerable. Versions 19.0.4, 19.1.5, 19.2.4 are safe.

-----

_Updated January 26, 2026._

</Note>

---

## High Severity: Denial of Service {/*high-severity-denial-of-service*/}

**CVEs:** [CVE-2025-55184](https://www.cve.org/CVERecord?id=CVE-2025-55184) and [CVE-2025-67779](https://www.cve.org/CVERecord?id=CVE-2025-67779)
**Base Score:** 7.5 (High)

Security researchers have discovered that a malicious HTTP request can be crafted and sent to any Server Functions endpoint that, when deserialized by React, can cause an infinite loop that hangs the server process and consumes CPU. Even if your app does not implement any React Server Function endpoints it may still be vulnerable if your app supports React Server Components.

This creates a vulnerability vector where an attacker may be able to deny users from accessing the product, and potentially have a  performance impact on the server environment.

The patches published today mitigate by preventing the infinite loop.

## Medium Severity: Source Code Exposure {/*low-severity-source-code-exposure*/}

**CVE:** [CVE-2025-55183](https://www.cve.org/CVERecord?id=CVE-2025-55183)
**Base Score**: 5.3 (Medium)

A security researcher has discovered that a malicious HTTP request sent to a vulnerable Server Function may unsafely return the source code of any Server Function. Exploitation requires the existence of a Server Function which explicitly or implicitly exposes a stringified argument:

```javascript
'use server';

export async function serverFunction(name) {
  const conn = db.createConnection('SECRET KEY');
  const user = await conn.createUser(name); // implicitly stringified, leaked in db

  return {
   id: user.id,
   message: `Hello, ${name}!` // explicitly stringified, leaked in reply
  }}
```

An attacker may be able to leak the following:

```txt
0:{"a":"$@1","f":"","b":"Wy43RxUKdxmr5iuBzJ1pN"}
1:{"id":"tva1sfodwq","message":"Hello, async function(a){console.log(\"serverFunction\");let b=i.createConnection(\"SECRET KEY\");return{id:(await b.createUser(a)).id,message:`Hello, ${a}!`}}!"}
```

The patches published today prevent stringifying the Server Function source code.

<Note>

#### Only secrets in source code may be exposed. {/*only-secrets-in-source-code-may-be-exposed*/}

Secrets hardcoded in source code may be exposed, but runtime secrets such as `process.env.SECRET` are not affected.

The scope of the exposed code is limited to the code inside the Server Function, which may include other functions depending on the amount of inlining your bundler provides. 

Always verify against production bundles.

</Note>

---

## Timeline {/*timeline*/}
* **December 3rd**: Leak reported to Vercel and [Meta Bug Bounty](https://bugbounty.meta.com/) by [Andrew MacPherson](https://github.com/AndrewMohawk).
* **December 4th**: Initial DoS reported to [Meta Bug Bounty](https://bugbounty.meta.com/) by [RyotaK](https://ryotak.net).
* **December 6th**: Both issues confirmed by the React team, and the team began investigating.
* **December 7th**: Initial fixes created and the React team began verifying and planning new patch.
* **December 8th**: Affected hosting providers and open source projects notified.
* **December 10th**: Hosting provider mitigations in place and patches verified.
* **December 11th**: Additional DoS reported to [Meta Bug Bounty](https://bugbounty.meta.com/) by Shinsaku Nomura.
* **December 11th**: Patches published and publicly disclosed as [CVE-2025-55183](https://www.cve.org/CVERecord?id=CVE-2025-55183) and [CVE-2025-55184](https://www.cve.org/CVERecord?id=CVE-2025-55184).
* **December 11th**: Missing DoS case found internally, patched and publicly disclosed as [CVE-2025-67779](https://www.cve.org/CVERecord?id=CVE-2025-67779).
* **January 26th**: Additional DoS cases found, patched, and publicly disclosed as [CVE-2026-23864](https://www.cve.org/CVERecord?id=CVE-2026-23864).
---

## Attribution {/*attribution*/}

Thank you to [Andrew MacPherson (AndrewMohawk)](https://github.com/AndrewMohawk) for reporting the Source Code Exposure, [RyotaK](https://ryotak.net) from GMO Flatt Security Inc and Shinsaku Nomura of Bitforest Co., Ltd. for reporting the Denial of Service vulnerabilities. Thank you to [Mufeed VH](https://x.com/mufeedvh) from [Winfunc Research](https://winfunc.com), [Joachim Viide](https://jviide.iki.fi), [RyotaK](https://ryotak.net) from [GMO Flatt Security Inc](https://flatt.tech/en/) and Xiangwei Zhang of Tencent Security YUNDING LAB for reporting the additional DoS vulnerabilities.

---
# Source: sunsetting-create-react-app.md
---
---
title: "逐步淘汰 Create React App"
author: Matt Carroll 和 Ricky Hanlon
date: 2025/02/14
description: 今天，我们正式宣布弃用 Create React App 作为新应用的推荐工具，并建议现有应用迁移至主流框架（如 Next.js、Remix 等），或迁移到 Vite、Parcel、RSBuild 等现代构建工具。我们还同步更新了相关文档，涵盖以下场景：当框架不适合你的项目时；当你希望自行构建框架时；以及当你希望通过从零开始搭建 React 应用来深入理解其工作原理时。
---

2025 年 2 月 14 日，作者：[Matt Carroll](https://twitter.com/mattcarrollcode) 和 [Ricky Hanlon](https://bsky.app/profile/ricky.fm)

---

<Intro>

今日起，我们将正式弃用 [Create React App](https://create-react-app.dev/) 作为新应用的推荐工具，并建议现有应用迁移至 [框架](#how-to-migrate-to-a-framework)，或迁移至 [构建工具](#how-to-migrate-to-a-build-tool)（如 Vite、Parcel 或 RSBuild）。

我们还提供了相关文档，适用于你的项目不适合使用框架的情况、你想要构建自己的框架，或者你只是想通过 [从零开始构建一个 React 应用](/learn/build-a-react-app-from-scratch) 来了解 React 的工作原理。

</Intro>

-----

当我们在 2016 年发布 Create React App 时，还没有一种明确的方式来构建一个新的 React 应用。

要创建一个 React 应用，你必须安装一堆工具，并手动将它们配置在一起，以支持 JSX、代码检查（linting）和热更新（hot reloading）等基本功能。这很难正确的完成，因此 [社区](https://github.com/react-boilerplate/react-boilerplate) 为 [常见的](https://github.com/gaearon/react-hot-boilerplate) [设置](https://github.com/erikras/react-redux-universal-hot-example) [创建](https://github.com/kriasoft/react-starter-kit)  了 [模板代码](https://github.com/petehunt/react-boilerplate)。然而，模板代码很难更新，而且代码碎片化的情况使得 React 难以推出新功能。

Create React App 通过将多个工具整合到一个推荐的配置中，解决了这些问题。这使得应用程序能够以简单的方式升级到新的工具特性，同时也让 React 团队能够将重要的工具变更（如快速刷新支持、React Hook 的 lint 规则）部署给尽可能广泛的用户群体。

这种模式变得非常流行，以至于如今有一整类工具都采用这种方式工作。

## 弃用 Create React App {/*deprecating-create-react-app*/}

虽然 Create React App 让入门变得简单，[但其存在的若干限制](#limitations-of-build-tools) 使得构建高性能的生产级应用颇具挑战。理论上，我们可以通过将其逐步发展为 [框架](#why-we-recommend-frameworks) 的方式来解决这些问题。

然而，由于 Create React App 目前没有活跃的维护者，并且已经有许多现有的框架能够解决这些问题，我们决定弃用 Create React App。

从今天开始，如果你安装一个新的应用程序，你会看到一个弃用警告：

<ConsoleBlockMulti>
<ConsoleLogLine level="error">

create-react-app is deprecated.
{'\n\n'}
You can find a list of up-to-date React frameworks on react.dev
For more info see: react.dev/link/cra
{'\n\n'}
This error message will only be shown once per install.

</ConsoleLogLine>
</ConsoleBlockMulti>

我们已在 Create React App 的 [官网](https://create-react-app.dev/) 和 GitHub [代码仓库](https://github.com/facebook/create-react-app) 添加了弃用通知。Create React App 将以维护模式继续运行，并发布了与 React 19 兼容的新版本 Create React App。

## 如何迁移到框架 {/*how-to-migrate-to-a-framework*/}
我们推荐使用 [框架创建新的 React 应用](/learn/creating-a-react-app)。所有推荐的框架均支持客户端渲染（[CSR](https://developer.mozilla.org/en-US/docs/Glossary/CSR)）和单页面应用（[SPA](https://developer.mozilla.org/zh-CN/docs/Glossary/SPA)），并可通过 CDN 或静态托管服务部署，无需服务器支持。

对于现有的应用程序，这些指南将帮助你迁移到仅客户端的单页应用（SPA）：

* [Next.js 的 Create React App 迁移指南](https://nextjs.org/docs/app/building-your-application/upgrading/from-create-react-app)
* [React Router 的框架适配指南](https://reactrouter.com/upgrading/component-routes).
* [Expo webpack 到 Expo Router 的迁移指南](https://docs.expo.dev/router/migrate/from-expo-webpack/)

## 如何迁移到构建工具 {/*how-to-migrate-to-a-build-tool*/}

如果你的应用程序有特殊的限制，或者你更喜欢通过构建自己的框架来解决这些问题，或者你只是想从头学习 React 的工作原理，你可以使用 Vite、Parcel 或 Rsbuild 来定制自己的 React 设置。

针对现有应用，以下指南将协助你迁移至构建工具：

* [Create React App 到 Vite 迁移指南](https://www.robinwieruch.de/vite-create-react-app/)
* [Create React App 到 Parcel 迁移指南](https://parceljs.org/migration/cra/)
* [Create React App 到 Rsbuild 迁移指南](https://rsbuild.dev/guide/migration/cra)

为帮助开发者快速上手 Vite、Parcel 或 Rsbuild，我们新增了 [从零开始构建 React 应用](/learn/build-a-react-app-from-scratch) 文档。

<DeepDive>

#### 是否需要使用框架？ {/*do-i-need-a-framework*/}

大多数应用都能从使用框架中获益，但在某些合理场景下从零开始构建 React 应用也是可行的。经验法则是：若你的应用需要路由功能，使用框架将更具优势。

正如 Svelte 拥有 SvelteKit、Vue 拥有 Nuxt、Solid 拥有 SolidStart，[React 推荐使用框架](#why-we-recommend-frameworks)——这类框架已原生集成路由功能，并与数据获取、代码分割等特性深度整合。此举可避免开发者陷入自行编写复杂配置的困境，本质上规避了重复造轮子的风险。

不过，你仍可选择使用 Vite、Parcel 或 Rsbuild 等 [构建工具从零搭建 React 应用](/learn/build-a-react-app-from-scratch)。

</DeepDive>

请继续阅读以深入了解 [构建工具的局限性](#limitations-of-build-tools) 以及 [我们推荐框架的原因](#why-we-recommend-frameworks)。

## 构建工具的局限性 {/*limitations-of-build-tools*/}

Create React App 及类似的构建工具使得开始构建 React 应用程序变得非常容易。运行 `npx create-react-app my-app` 后，你会得到一个完全配置好的 React 应用程序，包括开发服务器、代码检查和生产构建。

例如，如果你正在构建一个内部管理工具，你可以从一个落地页开始：

```js
export default function App() {
  return (
    <div>
      <h1>Welcome to the Admin Tool!</h1>
    </div>
  )
}
```

这让你能够立即开始用 React 进行编码，同时可以使用诸如 JSX、默认的代码检查规则，还有一个能在开发和生产环境中运行的打包工具。不过，这种设置缺少构建一个真正的生产应用程序所需的工具。

大多数生产应用程序需要解决诸如路由、数据获取和代码分割等方面的问题。

### 路由 {/*routing*/}

Create React App 并未包含特定的路由解决方案。如果你刚刚开始开发，一种选择是使用 `useState` 来在不同路由间进行切换。但这样做意味着你无法分享应用的链接，每个链接都会指向同一页面，而且随着时间推移，对应用进行架构设计会变得困难。

```js
import {useState} from 'react';

import Home from './Home';
import Dashboard from './Dashboard';

export default function App() {
  // ❌ 状态管理式路由无法生成有效 URL
  const [route, setRoute] = useState('home');
  return (
    <div>
      {route === 'home' && <Home />}
      {route === 'dashboard' && <Dashboard />}
    </div>
  )
}
```

这就是为什么大多数使用 Create React App 的应用会借助像 [React Router](https://reactrouter.com/) 或 [Tanstack Router](https://tanstack.com/router/latest) 这样的路由库来添加路由功能。使用路由库，你可以为应用添加额外的路由，这有助于规划应用的结构，还能让你开始分享指向特定路由的链接。例如，使用 React Router 你可以定义路由：

```js
import {RouterProvider, createBrowserRouter} from 'react-router';

import Home from './Home';
import Dashboard from './Dashboard';

// ✅ 每个路由对应独立 URL
const router = createBrowserRouter([
  {path: '/', element: <Home />},
  {path: '/dashboard', element: <Dashboard />}
]);

export default function App() {
  return (
    <RouterProvider value={router} />
  )
}
```

通过这一改动，你可以分享指向 `/dashboard` 的链接，应用会导航至仪表盘页面。一旦你使用了路由库，就可以添加诸如嵌套路由、路由守卫和路由过渡效果等额外功能，而如果没有路由库，这些功能很难实现。

这里存在一个权衡：路由库会增加应用的复杂性，但它也能带来一些没有它就很难实现的功能。 

### 数据获取 {/*data-fetching*/}

React 应用开发中的另一个常见问题是数据获取。Create React App 并没有内置特定的数据获取解决方案。如果你刚刚入门，常见的做法是在副作用中使用 fetch 方法来加载数据。

但是，这样做意味着数据是在组件渲染之后才获取的，这可能会导致 网络瀑布流问题（network waterfalls）。网络瀑布流问题的产生是因为数据是在应用程序渲染时才开始获取的，而不是在代码下载的同时并行获取数据：

```js
export default function Dashboard() {
  const [data, setData] = useState(null);

  // ❌ 在组件内获取数据会引发网络瀑布流
  useEffect(() => {
    fetch('/api/data')
      .then(response => response.json())
      .then(data => setData(data));
  }, []);

  return (
    <div>
      {data.map(item => <div key={item.id}>{item.name}</div>)}
    </div>
  )
}
```

在副作用中获取数据意味着用户需要等待更长时间才能看到内容，即使这些数据本可以更早地获取。为了解决这个问题，你可以使用一些数据获取库，例如：[TanStack Query](https://tanstack.com/query/)、[SWR](https://swr.vercel.app/)、[Apollo](https://www.apollographql.com/docs/react) 或 [Relay](https://relay.dev/)，这些库提供了预取数据的功能，使得请求可以在组件渲染之前就开始，从而减少用户等待时间并提升性能。

这些库在与路由的“loader”模式集成时效果最佳，可以在路由级别指定数据依赖关系，从而使路由器能够优化数据获取：

```js
export async function loader() {
  const response = await fetch(`/api/data`);
  const data = await response.json();
  return data;
}

// ✅ 在代码下载期间并行获取数据
export default function Dashboard({loaderData}) {
  return (
    <div>
      {loaderData.map(item => <div key={item.id}>{item.name}</div>)}
    </div>
  )
}
```

在首次加载时，路由器可以在渲染路由之前立即获取数据。当用户在应用中进行导航时，路由器能够同时获取数据和路由，实现并行获取。这减少了用户在屏幕上看到内容所需的时间，并且可以改善用户体验。

然而，这需要在你的应用中正确配置加载器，并且要在性能提升和复杂度增加之间进行权衡。 

### 代码分割 {/*code-splitting*/}

Create React App 中的另一个常见问题是 [代码分割](https://www.patterns.dev/vanilla/bundle-splitting)。Create React App 并未包含特定的代码分割解决方案。如果你刚刚开始开发，你可能根本不会考虑代码分割。

这意味着你的应用会作为一个单一的 bundle 进行发布。

```txt
- bundle.js    75kb
```

但为了达到理想的性能表现，你应该将代码“分割”成多个独立的代码包，这样用户只需下载他们所需要的部分。通过仅下载查看当前页面所需的代码，就能减少用户加载应用的等待时间。

```txt
- core.js      25kb
- home.js      25kb
- dashboard.js 25kb
```

实现代码分割的一种方法是使用 `React.lazy`。不过，这意味着代码要到组件渲染时才会被获取，这可能会导致网络瀑布效应。更优的解决方案是利用路由器的一项功能，在代码下载的同时并行获取代码。例如，React Router 提供了一个 `lazy` 选项，用于指定某个路由应进行代码分割，并对其加载时机进行优化：

```js
import Home from './Home';
import Dashboard from './Dashboard';

// ✅ 路由代码在渲染前完成加载
const router = createBrowserRouter([
  {path: '/', lazy: () => import('./Home')},
  {path: '/dashboard', lazy: () => import('Dashboard')}
]);
```

优化代码分割很难做到恰到好处，而且很容易犯错，导致用户下载的代码超出实际所需。当代码分割与路由和数据加载解决方案集成时，效果最佳，这样可以最大限度地利用缓存、并行获取数据，并支持 ["交互时导入"](https://www.patterns.dev/vanilla/import-on-interaction) 模式。

### 更多内容… {/*and-more*/}

这些只是 Create React App 的一些限制示例。

一旦你集成了路由、数据获取和代码分割，你现在还需要考虑挂起状态、导航中断、向用户显示错误信息以及数据的重新验证。用户需要解决一系列问题，例如：

<div style={{display: 'flex', width: '100%', justifyContent: 'space-around'}}>
  <ul>
    <li>无障碍设施</li>
    <li>资源加载</li>
    <li>验证</li>
    <li>缓存</li>
  </ul>
  <ul>
    <li>错误处理</li>
    <li>数据变更</li>
    <li>导航</li>
    <li>乐观更新</li>
  </ul>
  <ul>
    <li>渐进增强</li>
    <li>服务器端渲染</li>
    <li>静态站点生成</li>
    <li>流媒体</li>
  </ul>
</div>

所有这些共同作用，以打造出最理想的 [加载顺序](https://www.patterns.dev/vanilla/loading-sequence)。

在 Create React App 中逐个解决这些问题可能颇具难度，因为每个问题都相互关联，而且解决这些问题可能需要用户深入掌握他们或许并不熟悉的领域的专业知识。为了解决这些问题，用户最终会在 Create React App 的基础上构建自己的定制化解决方案，而这恰恰是 Create React App 最初试图解决的问题。

## 为什么我们推荐框架 {/*why-we-recommend-frameworks*/}

虽然你可以自己使用 Create React App、Vite 或 Parcel 等构建工具解决所有这些问题，但要做好却并非易事。就像 Create React App 本身将多个构建工具集成在一起一样，你需要一个工具将所有这些功能集成在一起，以便为用户提供最佳体验。

这类能够集成构建工具、渲染、路由、数据获取和代码分割等功能的工具被称作“框架”。或者，如果你倾向于将 React 本身视为一个框架，那么你可以把它们称为“元框架”。

框架会对应用的架构设计提出一些规范建议，目的是为用户带来更好的体验，这就如同构建工具会给出一些规范建议以使工具的使用更加便捷一样。这就是我们开始为新项目推荐像 [Next.js](https://nextjs.org/)、[React Router](https://reactrouter.com/) 和 [Expo](https://expo.dev/) 这类框架的原因。

框架提供了与 Create React App 相同的入门体验，但同时也为用户在实际生产应用中必须解决的问题提供了解决方案。

<DeepDive>

#### 服务器端渲染是可选的 {/*server-rendering-is-optional*/}

我们推荐的框架都提供了创建 [客户端渲染（CSR）](https://developer.mozilla.org/zh-CN/docs/Glossary/CSR) 应用的选项。

在某些情况下，客户端渲染（CSR）对于某个页面来说是正确的选择，但很多时候并非如此。即使你的应用大部分采用客户端渲染，通常也会有一些单独的页面能够从服务器端渲染特性中获益，比如 [静态网站生成（SSG）](https://developer.mozilla.org/zh-CN/docs/Glossary/SSG) 或 [服务器端渲染（SSR）](https://developer.mozilla.org/zh-CN/docs/Glossary/SSR)，例如服务条款页面或文档页面。

服务器渲染通常会向客户端发送更少的JavaScript代码，并生成一个完整的HTML文档，这通过减少 [总阻塞时间（TBT）](https://web.dev/articles/tbt) 来提高 [首次内容绘制（FCP）](https://web.dev/articles/fcp) 的速度，同时也可能降低 [下一次绘制的交互时间（INP）](https://web.dev/articles/inp)。这就是为什么 [Chrome 团队鼓励](https://web.dev/articles/rendering-on-the-web) 开发者考虑使用静态或服务器端渲染，而不是完全的客户端渲染方法，以实现最佳性能。

使用服务器渲染存在一定的权衡，它并不总是每个页面的最佳选择。在服务器上生成页面会产生额外的成本，并且需要时间来完成，这可能会增加 [首字节时间（TTFB）](https://web.dev/articles/ttfb)。性能最佳的应用程序能够根据每种策略的权衡，在逐页的基础上选择正确的渲染策略。

框架提供了在任何页面上使用服务器的选项，但并不会强制你使用服务器。这允许你为应用程序中的每个页面选择最合适的渲染策略。

#### 关于服务器组件 {/*server-components*/}

我们推荐的框架还支持 React 服务器组件。

服务器组件通过将路由和数据获取操作移至服务器端来帮助解决这些问题。它允许基于渲染的数据（而非仅仅基于所渲染的路由）对客户端组件进行代码分割，并且减少发送的 JavaScript 代码量，以实现尽可能理想的 [加载顺序](https://www.patterns.dev/vanilla/loading-sequence)。

服务器组件并不一定需要实时运行的服务器支持。它们既可以在持续集成（CI）服务器的构建阶段运行，以创建一个静态网站生成（SSG）应用；也可以在 Web 服务器的运行时阶段使用，从而实现服务器端渲染（SSR）应用。

有关更多信息，请参阅 [介绍零 bundle 大小的 React 服务器组件](/blog/2020/12/21/data-fetching-with-react-server-components) 和 [相关文档](/reference/rsc/server-components)。

</DeepDive>

<Note>

#### 服务器渲染不仅仅用于 SEO {/*server-rendering-is-not-just-for-seo*/}

一个常见的误解是，服务器端渲染仅仅是为了 [SEO](https://developer.mozilla.org/zh-CN/docs/Glossary/SEO)。

虽然服务器端渲染可以提升搜索引擎优化效果，但它还能通过减少用户在看到屏幕上的内容之前需要下载和解析的 JavaScript 代码量来提高性能。 

这就是为什么 Chrome 团队 [已经鼓励](https://web.dev/articles/rendering-on-the-web) 开发者考虑采用静态渲染或服务器端渲染，而非完全的客户端渲染方式，以实现尽可能最佳的性能。

</Note>

---

感谢 [Dan Abramov](https://bsky.app/profile/danabra.mov) 创建了 Create React App，也感谢 [Joe Haddad](https://github.com/Timer)、[Ian Schmitz](https://github.com/ianschmitz)、[Brody McKee](https://github.com/mrmckeb) 以及 [其他众多贡献者](https://github.com/facebook/create-react-app/graphs/contributors) 多年来对 Create React App 的维护。感谢 [Brooks Lybrand](https://bsky.app/profile/brookslybrand.bsky.social)、[Dan Abramov](https://bsky.app/profile/danabra.mov)、[Devon Govett](https://bsky.app/profile/devongovett.bsky.social)、[Eli White](https://x.com/Eli_White)、[Jack Herrington](https://bsky.app/profile/jherr.dev)、[Joe Savona](https://x.com/en_JS)、[Lauren Tan](https://bsky.app/profile/no.lol)、[Lee Robinson](https://x.com/leeerob)、[Mark Erikson](https://bsky.app/profile/acemarke.dev)、[Ryan Florence](https://x.com/ryanflorence)、[Sophie Alpert](https://bsky.app/profile/sophiebits.com)、[Tanner Linsley](https://bsky.app/profile/tannerlinsley.com) 和 [Theo Browne](https://x.com/theo) 对这篇文章进行审阅并提供反馈。


---
# Source: versions.md
---
---
title: React 版本
---

<Intro>

React 文档位于 [react.dev](https://react.dev)，提供最新版本 React 的文档。

</Intro>

我们致力于在主要版本内保持文档的更新，并不会为每个次要版本或补丁版本发布单独的文档版本。当一个新的主要版本发布时，我们会将前一个版本的文档存档为 `x.react.dev`。有关更多信息，请参阅我们的[版本控制政策](/community/versioning-policy)。

你可以在下方找到以前主要版本的存档。
## 最新版本：19.2 {/*latest-version*/}

- [react.dev](https://react.dev) {/*docs-19*/}

## 历史版本 {/*previous-versions*/}

- [18.react.dev](https://18.react.dev) {/*docs-18*/}
- [17.react.dev](https://17.react.dev) {/*docs-17*/}
- [16.react.dev](https://16.react.dev) {/*docs-16*/}
- [15.react.dev](https://15.react.dev) {/*docs-15*/}

<Note>

#### 旧版文档 {/*legacy-docs*/}

在 2023 年，我们为 React 18 [推出了全新文档](/blog/2023/03/16/introducing-react-dev)，并将其托管在 [react.dev](https://react.dev)。旧版 React 18 文档可在 [legacy.reactjs.org](https://legacy.reactjs.org) 查看。React 17 及更早版本的文档托管在旧版网站上。

对于早于 React 15 的版本，请参阅 [15.react.dev](https://15.react.dev)。

</Note>

## 更新日志 {/*changelog*/}

### React 19 {/*react-19*/}

**博客文章**
- [React v19](/blog/2024/12/05/react-19)
- [React 19 Upgrade Guide](/blog/2024/04/25/react-19-upgrade-guide)
- [React Compiler Beta Release](/blog/2024/10/21/react-compiler-beta-release)
- [React Compiler v1.0](/blog/2025/10/07/react-compiler-1)
- [React 19.2](/blog/2025/10/01/react-19-2)

**Talks**
- [React 19 Keynote](https://www.youtube.com/watch?v=lyEKhv8-3n0)
- [A Roadmap to React 19](https://www.youtube.com/watch?v=R0B2HsSM78s)
- [What's new in React 19](https://www.youtube.com/watch?v=AJOGzVygGcY)
- [React for Two Computers](https://www.youtube.com/watch?v=ozI4V_29fj4)
- [React Compiler Deep Dive](https://www.youtube.com/watch?v=uA_PVyZP7AI)
- [React Compiler Case Studies](https://www.youtube.com/watch?v=lvhPq5chokM)
- [React 19 Deep Dive: Coordinating HTML](https://www.youtube.com/watch?v=IBBN-s77YSI)

**发布版本**
- [v19.2.1 (December, 2025)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1922-dec-11-2025)
- [v19.2.1 (December, 2025)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1921-dec-3-2025)
- [v19.2.0 (October, 2025)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1920-october-1st-2025)
- [v19.1.3 (December, 2025)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1913-dec-11-2025)
- [v19.1.2 (December, 2025)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1912-dec-3-2025)
- [v19.1.1 (July, 2025)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1911-july-28-2025)
- [v19.1.0 (March, 2025)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1910-march-28-2025)
- [v19.0.2 (December, 2025)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1902-dec-11-2025)
- [v19.0.1 (December, 2025)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1901-dec-3-2025)
- [v19.0.0 (December, 2024)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1900-december-5-2024)

### React 18 {/*react-18*/}

**博客文章**
- [React v18.0](/blog/2022/03/29/react-v18)
- [How to Upgrade to React 18](/blog/2022/03/08/react-18-upgrade-guide)
- [The Plan for React 18](/blog/2021/06/08/the-plan-for-react-18)

**演讲**
- [React 18 Keynote](https://www.youtube.com/watch?v=FZ0cG47msEk)
- [React 18 for app developers](https://www.youtube.com/watch?v=ytudH8je5ko)
- [Streaming Server Rendering with Suspense](https://www.youtube.com/watch?v=pj5N-Khihgc)
- [React without memo](https://www.youtube.com/watch?v=lGEMwh32soc)
- [React Docs Keynote](https://www.youtube.com/watch?v=mneDaMYOKP8)
- [React Developer Tooling](https://www.youtube.com/watch?v=oxDfrke8rZg)
- [The first React Working Group](https://www.youtube.com/watch?v=qn7gRClrC9U)
- [React 18 for External Store Libraries](https://www.youtube.com/watch?v=oPfSC5bQPR8)

**发布版本**
- [v18.3.1 (April, 2024)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1831-april-26-2024)
- [v18.3.0 (April, 2024)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1830-april-25-2024)
- [v18.2.0 (June, 2022)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1820-june-14-2022)
- [v18.1.0 (April, 2022)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1810-april-26-2022)
- [v18.0.0 (March 2022)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1800-march-29-2022)

### React 17 {/*react-17*/}

**博客文章**
- [React v17.0](https://legacy.reactjs.org/blog/2020/10/20/react-v17.html)
- [Introducing the New JSX Transform](https://legacy.reactjs.org/blog/2020/09/22/introducing-the-new-jsx-transform.html)
- [React v17.0 Release Candidate: No New Features](https://legacy.reactjs.org/blog/2020/08/10/react-v17-rc.html)

**发布版本**
- [v17.0.2 (March 2021)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1702-march-22-2021)
- [v17.0.1 (October 2020)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1701-october-22-2020)
- [v17.0.0 (October 2020)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1700-october-20-2020)

### React 16 {/*react-16*/}

**博客文章**
- [React v16.0](https://legacy.reactjs.org/blog/2017/09/26/react-v16.0.html)
- [DOM Attributes in React 16](https://legacy.reactjs.org/blog/2017/09/08/dom-attributes-in-react-16.html)
- [Error Handling in React 16](https://legacy.reactjs.org/blog/2017/07/26/error-handling-in-react-16.html)
- [React v16.2.0: Improved Support for Fragments](https://legacy.reactjs.org/blog/2017/11/28/react-v16.2.0-fragment-support.html)
- [React v16.4.0: Pointer Events](https://legacy.reactjs.org/blog/2018/05/23/react-v-16-4.html)
- [React v16.4.2: Server-side vulnerability fix](https://legacy.reactjs.org/blog/2018/08/01/react-v-16-4-2.html)
- [React v16.6.0: lazy, memo and contextType](https://legacy.reactjs.org/blog/2018/10/23/react-v-16-6.html)
- [React v16.7: No, This Is Not the One With Hooks](https://legacy.reactjs.org/blog/2018/12/19/react-v-16-7.html)
- [React v16.8: The One With Hooks](https://legacy.reactjs.org/blog/2019/02/06/react-v16.8.0.html)
- [React v16.9.0 and the Roadmap Update](https://legacy.reactjs.org/blog/2019/08/08/react-v16.9.0.html)
- [React v16.13.0](https://legacy.reactjs.org/blog/2020/02/26/react-v16.13.0.html)

**发布版本**
- [v16.14.0 (October 2020)](https://github.com/facebook/react/blob/main/CHANGELOG.md#16140-october-14-2020)
- [v16.13.1 (March 2020)](https://github.com/facebook/react/blob/main/CHANGELOG.md#16131-march-19-2020)
- [v16.13.0 (February 2020)](https://github.com/facebook/react/blob/main/CHANGELOG.md#16130-february-26-2020)
- [v16.12.0 (November 2019)](https://github.com/facebook/react/blob/main/CHANGELOG.md#16120-november-14-2019)
- [v16.11.0 (October 2019)](https://github.com/facebook/react/blob/main/CHANGELOG.md#16110-october-22-2019)
- [v16.10.2 (October 2019)](https://github.com/facebook/react/blob/main/CHANGELOG.md#16102-october-3-2019)
- [v16.10.1 (September 2019)](https://github.com/facebook/react/blob/main/CHANGELOG.md#16101-september-28-2019)
- [v16.10.0 (September 2019)](https://github.com/facebook/react/blob/main/CHANGELOG.md#16100-september-27-2019)
- [v16.9.0 (August 2019)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1690-august-8-2019)
- [v16.8.6 (March 2019)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1686-march-27-2019)
- [v16.8.5 (March 2019)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1685-march-22-2019)
- [v16.8.4 (March 2019)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1684-march-5-2019)
- [v16.8.3 (February 2019)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1683-february-21-2019)
- [v16.8.2 (February 2019)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1682-february-14-2019)
- [v16.8.1 (February 2019)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1681-february-6-2019)
- [v16.8.0 (February 2019)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1680-february-6-2019)
- [v16.7.0 (December 2018)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1670-december-19-2018)
- [v16.6.3 (November 2018)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1663-november-12-2018)
- [v16.6.2 (November 2018)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1662-november-12-2018)
- [v16.6.1 (November 2018)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1661-november-6-2018)
- [v16.6.0 (October 2018)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1660-october-23-2018)
- [v16.5.2 (September 2018)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1652-september-18-2018)
- [v16.5.1 (September 2018)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1651-september-13-2018)
- [v16.5.0 (September 2018)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1650-september-5-2018)
- [v16.4.2 (August 2018)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1642-august-1-2018)
- [v16.4.1 (June 2018)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1641-june-13-2018)
- [v16.4.0 (May 2018)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1640-may-23-2018)
- [v16.3.3 (August 2018)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1633-august-1-2018)
- [v16.3.2 (April 2018)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1632-april-16-2018)
- [v16.3.1 (April 2018)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1631-april-3-2018)
- [v16.3.0 (March 2018)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1630-march-29-2018)
- [v16.2.1 (August 2018)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1621-august-1-2018)
- [v16.2.0 (November 2017)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1620-november-28-2017)
- [v16.1.2 (August 2018)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1612-august-1-2018)
- [v16.1.1 (November 2017)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1611-november-13-2017)
- [v16.1.0 (November 2017)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1610-november-9-2017)
- [v16.0.1 (August 2018)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1601-august-1-2018)
- [v16.0 (September 2017)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1600-september-26-2017)

### React 15 {/*react-15*/}

**博客文章**
- [React v15.0](https://legacy.reactjs.org/blog/2016/04/07/react-v15.html)
- [React v15.0 Release Candidate 2](https://legacy.reactjs.org/blog/2016/03/16/react-v15-rc2.html)
- [React v15.0 Release Candidate](https://legacy.reactjs.org/blog/2016/03/07/react-v15-rc1.html)
- [New Versioning Scheme](https://legacy.reactjs.org/blog/2016/02/19/new-versioning-scheme.html)
- [Discontinuing IE 8 Support in React DOM](https://legacy.reactjs.org/blog/2016/01/12/discontinuing-ie8-support.html)
- [Introducing React's Error Code System](https://legacy.reactjs.org/blog/2016/07/11/introducing-reacts-error-code-system.html)
- [React v15.0.1](https://legacy.reactjs.org/blog/2016/04/08/react-v15.0.1.html)
- [React v15.4.0](https://legacy.reactjs.org/blog/2016/11/16/react-v15.4.0.html)
- [React v15.5.0](https://legacy.reactjs.org/blog/2017/04/07/react-v15.5.0.html)
- [React v15.6.0](https://legacy.reactjs.org/blog/2017/06/13/react-v15.6.0.html)
- [React v15.6.2](https://legacy.reactjs.org/blog/2017/09/25/react-v15.6.2.html)

**发布版本**
- [v15.7.0 (October 2017)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1570-october-14-2020)
- [v15.6.2 (September 2017)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1562-september-25-2017)
- [v15.6.1 (June 2017)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1561-june-14-2017)
- [v15.6.0 (June 2017)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1560-june-13-2017)
- [v15.5.4 (April 2017)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1554-april-11-2017)
- [v15.5.3 (April 2017)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1553-april-7-2017)
- [v15.5.2 (April 2017)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1552-april-7-2017)
- [v15.5.1 (April 2017)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1551-april-7-2017)
- [v15.5.0 (April 2017)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1550-april-7-2017)
- [v15.4.2 (January 2016)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1542-january-6-2017)
- [v15.4.1 (November 2016)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1541-november-22-2016)
- [v15.4.0 (November 2016)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1540-november-16-2016)
- [v15.3.2 (September 2016)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1532-september-19-2016)
- [v15.3.1 (August 2016)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1531-august-19-2016)
- [v15.3.0 (July 2016)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1530-july-29-2016)
- [v15.2.1 (July 2016)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1521-july-8-2016)
- [v15.2.0 (July 2016)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1520-july-1-2016)
- [v15.1.0 (May 2016)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1510-may-20-2016)
- [v15.0.2 (April 2016)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1502-april-29-2016)
- [v15.0.1 (April 2016)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1501-april-8-2016)
- [v15.0.0 (April 2016)](https://github.com/facebook/react/blob/main/CHANGELOG.md#1500-april-7-2016)

### React 0.14 {/*react-14*/}

**博客文章**
- [React v0.14](https://legacy.reactjs.org/blog/2015/10/07/react-v0.14.html)
- [React v0.14 Release Candidate](https://legacy.reactjs.org/blog/2015/09/10/react-v0.14-rc1.html)
- [React v0.14 Beta 1](https://legacy.reactjs.org/blog/2015/07/03/react-v0.14-beta-1.html)
- [New React Developer Tools](https://legacy.reactjs.org/blog/2015/09/02/new-react-developer-tools.html)
- [New React Devtools Beta](https://legacy.reactjs.org/blog/2015/08/03/new-react-devtools-beta.html)
- [React v0.14.1](https://legacy.reactjs.org/blog/2015/10/28/react-v0.14.1.html)
- [React v0.14.2](https://legacy.reactjs.org/blog/2015/11/02/react-v0.14.2.html)
- [React v0.14.3](https://legacy.reactjs.org/blog/2015/11/18/react-v0.14.3.html)
- [React v0.14.4](https://legacy.reactjs.org/blog/2015/12/29/react-v0.14.4.html)
- [React v0.14.8](https://legacy.reactjs.org/blog/2016/03/29/react-v0.14.8.html)

**发布版本**
- [v0.14.10 (October 2020)](https://github.com/facebook/react/blob/main/CHANGELOG.md#01410-october-14-2020)
- [v0.14.8 (March 2016)](https://github.com/facebook/react/blob/main/CHANGELOG.md#0148-march-29-2016)
- [v0.14.7 (January 2016)](https://github.com/facebook/react/blob/main/CHANGELOG.md#0147-january-28-2016)
- [v0.14.6 (January 2016)](https://github.com/facebook/react/blob/main/CHANGELOG.md#0146-january-6-2016)
- [v0.14.5 (December 2015)](https://github.com/facebook/react/blob/main/CHANGELOG.md#0145-december-29-2015)
- [v0.14.4 (December 2015)](https://github.com/facebook/react/blob/main/CHANGELOG.md#0144-december-29-2015)
- [v0.14.3 (November 2015)](https://github.com/facebook/react/blob/main/CHANGELOG.md#0143-november-18-2015)
- [v0.14.2 (November 2015)](https://github.com/facebook/react/blob/main/CHANGELOG.md#0142-november-2-2015)
- [v0.14.1 (October 2015)](https://github.com/facebook/react/blob/main/CHANGELOG.md#0141-october-28-2015)
- [v0.14.0 (October 2015)](https://github.com/facebook/react/blob/main/CHANGELOG.md#0140-october-7-2015)

### React 0.13 {/*react-13*/}

**博客文章**
- [React Native v0.4](https://legacy.reactjs.org/blog/2015/04/17/react-native-v0.4.html)
- [React v0.13](https://legacy.reactjs.org/blog/2015/03/10/react-v0.13.html)
- [React v0.13 RC2](https://legacy.reactjs.org/blog/2015/03/03/react-v0.13-rc2.html)
- [React v0.13 RC](https://legacy.reactjs.org/blog/2015/02/24/react-v0.13-rc1.html)
- [React v0.13.0 Beta 1](https://legacy.reactjs.org/blog/2015/01/27/react-v0.13.0-beta-1.html)
- [Streamlining React Elements](https://legacy.reactjs.org/blog/2015/02/24/streamlining-react-elements.html)
- [Introducing Relay and GraphQL](https://legacy.reactjs.org/blog/2015/02/20/introducing-relay-and-graphql.html)
- [Introducing React Native](https://legacy.reactjs.org/blog/2015/03/26/introducing-react-native.html)
- [React v0.13.1](https://legacy.reactjs.org/blog/2015/03/16/react-v0.13.1.html)
- [React v0.13.2](https://legacy.reactjs.org/blog/2015/04/18/react-v0.13.2.html)
- [React v0.13.3](https://legacy.reactjs.org/blog/2015/05/08/react-v0.13.3.html)

**发布版本**
- [v0.13.3 (May 2015)](https://github.com/facebook/react/blob/main/CHANGELOG.md#0133-may-8-2015)
- [v0.13.2 (April 2015)](https://github.com/facebook/react/blob/main/CHANGELOG.md#0132-april-18-2015)
- [v0.13.1 (March 2015)](https://github.com/facebook/react/blob/main/CHANGELOG.md#0131-march-16-2015)
- [v0.13.0 (March 2015)](https://github.com/facebook/react/blob/main/CHANGELOG.md#0130-march-10-2015)

### React 0.12 {/*react-12*/}

**博客文章**
- [React v0.12](https://legacy.reactjs.org/blog/2014/10/28/react-v0.12.html)
- [React v0.12 RC](https://legacy.reactjs.org/blog/2014/10/16/react-v0.12-rc1.html)
- [Introducing React Elements](https://legacy.reactjs.org/blog/2014/10/14/introducing-react-elements.html)
- [React v0.12.2](https://legacy.reactjs.org/blog/2014/12/18/react-v0.12.2.html)

**发布版本**
- [v0.12.2 (December 2014)](https://github.com/facebook/react/blob/main/CHANGELOG.md#0122-december-18-2014)
- [v0.12.1 (November 2014)](https://github.com/facebook/react/blob/main/CHANGELOG.md#0121-november-18-2014)
- [v0.12.0 (October 2014)](https://github.com/facebook/react/blob/main/CHANGELOG.md#0120-october-28-2014)

### React 0.11 {/*react-11*/}

**博客文章**
- [React v0.11](https://legacy.reactjs.org/blog/2014/07/17/react-v0.11.html)
- [React v0.11 RC](https://legacy.reactjs.org/blog/2014/07/13/react-v0.11-rc1.html)
- [One Year of Open-Source React](https://legacy.reactjs.org/blog/2014/05/29/one-year-of-open-source-react.html)
- [The Road to 1.0](https://legacy.reactjs.org/blog/2014/03/28/the-road-to-1.0.html)
- [React v0.11.1](https://legacy.reactjs.org/blog/2014/07/25/react-v0.11.1.html)
- [React v0.11.2](https://legacy.reactjs.org/blog/2014/09/16/react-v0.11.2.html)
- [Introducing the JSX Specificaion](https://legacy.reactjs.org/blog/2014/09/03/introducing-the-jsx-specification.html)

**发布版本**
- [v0.11.2 (September 2014)](https://github.com/facebook/react/blob/main/CHANGELOG.md#0112-september-16-2014)
- [v0.11.1 (July 2014)](https://github.com/facebook/react/blob/main/CHANGELOG.md#0111-july-24-2014)
- [v0.11.0 (July 2014)](https://github.com/facebook/react/blob/main/CHANGELOG.md#0110-july-17-2014)

### React 0.10 及以下 {/*react-10-and-below*/}

**博客文章**
- [React v0.10](https://legacy.reactjs.org/blog/2014/03/21/react-v0.10.html)
- [React v0.10 RC](https://legacy.reactjs.org/blog/2014/03/19/react-v0.10-rc1.html)
- [React v0.9](https://legacy.reactjs.org/blog/2014/02/20/react-v0.9.html)
- [React v0.9 RC](https://legacy.reactjs.org/blog/2014/02/16/react-v0.9-rc1.html)
- [React Chrome Developer Tools](https://legacy.reactjs.org/blog/2014/01/02/react-chrome-developer-tools.html)
- [React v0.8](https://legacy.reactjs.org/blog/2013/12/19/react-v0.8.0.html)
- [React v0.5.2, v0.4.2](https://legacy.reactjs.org/blog/2013/12/18/react-v0.5.2-v0.4.2.html)
- [React v0.5.1](https://legacy.reactjs.org/blog/2013/10/29/react-v0-5-1.html)
- [React v0.5](https://legacy.reactjs.org/blog/2013/10/16/react-v0.5.0.html)
- [React v0.4.1](https://legacy.reactjs.org/blog/2013/07/26/react-v0-4-1.html)
- [React v0.4.0](https://legacy.reactjs.org/blog/2013/07/17/react-v0-4-0.html)
- [New in React v0.4: Prop Validation and Default Values](https://legacy.reactjs.org/blog/2013/07/11/react-v0-4-prop-validation-and-default-values.html)
- [New in React v0.4: Autobind by Default](https://legacy.reactjs.org/blog/2013/07/02/react-v0-4-autobind-by-default.html)
- [React v0.3.3](https://legacy.reactjs.org/blog/2013/07/02/react-v0-4-autobind-by-default.html)

**发布版本**
- [v0.10.0 (March 2014)](https://github.com/facebook/react/blob/main/CHANGELOG.md#0100-march-21-2014)
- [v0.9.0 (February 2014)](https://github.com/facebook/react/blob/main/CHANGELOG.md#090-february-20-2014)
- [v0.8.0 (December 2013)](https://github.com/facebook/react/blob/main/CHANGELOG.md#080-december-19-2013)
- [v0.5.2 (December 2013)](https://github.com/facebook/react/blob/main/CHANGELOG.md#052-042-december-18-2013)
- [v0.5.1 (October 2013)](https://github.com/facebook/react/blob/main/CHANGELOG.md#051-october-29-2013)
- [v0.5.0 (October 2013)](https://github.com/facebook/react/blob/main/CHANGELOG.md#050-october-16-2013)
- [v0.4.1 (July 2013)](https://github.com/facebook/react/blob/main/CHANGELOG.md#041-july-26-2013)
- [v0.4.0 (July 2013)](https://github.com/facebook/react/blob/main/CHANGELOG.md#040-july-17-2013)
- [v0.3.3 (June 2013)](https://github.com/facebook/react/blob/main/CHANGELOG.md#033-june-20-2013)
- [v0.3.2 (May 2013)](https://github.com/facebook/react/blob/main/CHANGELOG.md#032-may-31-2013)
- [v0.3.1 (May 2013)](https://github.com/facebook/react/blob/main/CHANGELOG.md#031-may-30-2013)
- [v0.3.0 (May 2013)](https://github.com/facebook/react/blob/main/CHANGELOG.md#031-may-30-2013)

### 初始提交 {/*initial-commit*/}

React 于 2013 年 5 月 29 日开源。初始提交为：[`75897c`: Initial public release](https://github.com/facebook/react/commit/75897c2dcd1dd3a6ca46284dd37e13d22b4b16b4)。

请参阅第一篇博客文章：[Why did we build React?](https://legacy.reactjs.org/blog/2013/06/05/why-react.html)

React 于 2013 年在 Facebook 西雅图办公室开源：

<iframe width="560" height="315" src="https://www.youtube.com/embed/XxVg_s8xAms?si=466vSJrnXTn05j9A" title="YouTube 视频播放器" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

---
# Source: 377.md
---
<Intro>

In the minified production build of React, we avoid sending down full error messages in order to reduce the number of bytes sent over the wire.

</Intro>

We highly recommend using the development build locally when debugging your app since it tracks additional debug info and provides helpful warnings about potential problems in your apps, but if you encounter an exception while using the production build, this page will reassemble the original error message.

The full text of the error you just encountered is:

<ErrorDecoder />

This error occurs when you pass a BigInt value from a Server Component to a Client Component.

---
# Source: index.md
---
<Intro>

在为生产环境所构建的压缩版 React 中，我们避免发送完整的错误信息，以减少网络传输的字节数。

</Intro>


我们强烈建议你在本地调试应用时使用开发环境构建，因为它会追踪额外的调试信息，并针对应用中的潜在问题提供有用的警告。但是，如果你在使用生产环境构建时遇到异常，错误信息将只包含一个指向相关错误文档的链接。

参阅 [https://react.dev/errors/149](/errors/149) 查看示例。

---
# Source: generic.md
---
<Intro>

In the minified production build of React, we avoid sending down full error messages in order to reduce the number of bytes sent over the wire.

</Intro>

We highly recommend using the development build locally when debugging your app since it tracks additional debug info and provides helpful warnings about potential problems in your apps, but if you encounter an exception while using the production build, this page will reassemble the original error message.

The full text of the error you just encountered is:

<ErrorDecoder />

---
# Source: index.md
---
---
id: home
title: React 官方中文文档
permalink: index.html
---

{/* See HomeContent.js */}

---
# Source: conditional-rendering.md
---
---
title: 条件渲染
translators:
  - Alienover
---

<Intro>

通常你的组件会需要根据不同的情况显示不同的内容。在 React 中，你可以通过使用 JavaScript 的 `if` 语句、`&&` 和 `? :` 运算符来选择性地渲染 JSX。

</Intro>

<YouWillLearn>

* 如何根据不同条件返回不同的 JSX
* 如何根据不同条件包含或者去掉部分 JSX
* 一些你会在 React 代码库里遇到的常用的条件语法快捷表达式

</YouWillLearn>

## 条件返回 JSX {/*conditionally-returning-jsx*/}

假设有一个 `PackingList` 组件，里面渲染多个 `Item` 组件，每个物品可标记为打包与否：

<Sandpack>

```js
function Item({ name, isPacked }) {
  return <li className="item">{name}</li>;
}

export default function PackingList() {
  return (
    <section>
      <h1>Sally Ride 的行李清单</h1>
      <ul>
        <Item 
          isPacked={true} 
          name="宇航服" 
        />
        <Item 
          isPacked={true} 
          name="带金箔的头盔" 
        />
        <Item 
          isPacked={false} 
          name="Tam 的照片" 
        />
      </ul>
    </section>
  );
}
```

</Sandpack>

需要注意的是，有些 `Item` 组件的 `isPacked` 属性是被设为 `true` 而不是 `false`。你可以在那些满足 `isPacked={true}` 条件的物品旁加上一个勾选符号（✅）。

你可以用 [if/else 语句](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Statements/if...else) 去判断：

```js
if (isPacked) {
  return <li className="item">{name} ✅</li>;
}
return <li className="item">{name}</li>;
```

如果 `isPacked` 属性是 `true`，这段代码会**返回一个不一样的 JSX**。通过这样的改动，一些物品的名字后面会出现一个勾选符号：

<Sandpack>

```js
function Item({ name, isPacked }) {
  if (isPacked) {
    return <li className="item">{name} ✅</li>;
  }
  return <li className="item">{name}</li>;
}

export default function PackingList() {
  return (
    <section>
      <h1>Sally Ride 的行李清单</h1>
      <ul>
        <Item 
          isPacked={true} 
          name="宇航服" 
        />
        <Item 
          isPacked={true} 
          name="带金箔的头盔" 
        />
        <Item 
          isPacked={false} 
          name="Tam 的照片" 
        />
      </ul>
    </section>
  );
}
```

</Sandpack>

动手尝试一下，看看各种情况会出现什么不同的结果！

留意这里你是怎么使用 JavaScript 的 `if` 和 `return` 语句来写分支逻辑。在 React 中，是由 JavaScript 来处理控制流的（比如条件）。

### 选择性地返回 `null` {/*conditionally-returning-nothing-with-null*/}

在一些情况下，你不想有任何东西进行渲染。比如，你不想显示已经打包好的物品。但一个组件必须返回一些东西。这种情况下，你可以直接返回 `null`。

```js
if (isPacked) {
  return null;
}
return <li className="item">{name}</li>;
```

如果组件的 `isPacked` 属性为 `true`，那么它将只返回 `null`。否则，它将返回相应的 JSX 用来渲染。

<Sandpack>

```js
function Item({ name, isPacked }) {
  if (isPacked) {
    return null;
  }
  return <li className="item">{name}</li>;
}

export default function PackingList() {
  return (
    <section>
      <h1>Sally Ride 的行李清单</h1>
      <ul>
        <Item 
          isPacked={true} 
          name="宇航服" 
        />
        <Item 
          isPacked={true} 
          name="带金箔的头盔" 
        />
        <Item 
          isPacked={false} 
          name="Tam 的照片" 
        />
      </ul>
    </section>
  );
}
```

</Sandpack>

实际上，在组件里返回 `null` 并不常见，因为这样会让想使用它的开发者感觉奇怪。通常情况下，你可以在父组件里选择是否要渲染该组件。让我们接着往下看吧！

## 选择性地包含 JSX {/*conditionally-including-jsx*/}

在之前的例子里，你在组件内部控制哪些 JSX 树（如果有的话！）会返回。你可能已经发现了在渲染输出里会有一些重复的内容：

```js
<li className="item">{name} ✅</li>
```

和下面的写法很像：

```js
<li className="item">{name}</li>
```

两个条件分支都会返回 `<li className="item">...</li>`：

```js
if (isPacked) {
  return <li className="item">{name} ✅</li>;
}
return <li className="item">{name}</li>;
```

虽然这些重复的内容没什么害处，但这样可能会导致你的代码更难维护。比如你想更改 `className`？你就需要修改两个地方！针对这种情况，你可以通过选择性地包含一小段 JSX 来让你的代码更加 [DRY](https://en.wikipedia.org/wiki/Don%27t_repeat_yourself)。

### 三目运算符（`? :`） {/*conditional-ternary-operator--*/}

JavaScript 有一种紧凑型语法来实现条件判断表达式——[条件运算符](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Operators/Conditional_Operator) 又称“三目运算符”。

除了这样：

```js
if (isPacked) {
  return <li className="item">{name} ✅</li>;
}
return <li className="item">{name}</li>;
```

你还可以这样实现：

```js
return (
  <li className="item">
    {isPacked ? name + ' ✅' : name}
  </li>
);
```

你可以认为，*“如果 `isPacked` 为 true 时，则（`?`）渲染 `name + ' ✅'`，否则（`:`）渲染 `name`。”*

<DeepDive>

#### 两个例子完全一样吗？ {/*are-these-two-examples-fully-equivalent*/}

如果你之前是习惯面向对象开发的，你可能会认为上面的两个例子略有不同，因为其中一个可能会创建两个不同的 `<li>` “实例”。但 JSX 元素不是“实例”，因为它们没有内部状态也不是真实的 DOM 节点。它们只是一些简单的描述，就像图纸一样。所以上面这两个例子事实上是完全相同的。在 [状态的保持和重置](/learn/preserving-and-resetting-state) 里会深入探讨其原因。

</DeepDive>

现在，假如你想将对应物品的文本放到另一个 HTML 标签里，比如用 `<del>` 来显示删除线。你可以添加更多的换行和括号，以便在各种情况下更好地去嵌套 JSX：

<Sandpack>

```js
function Item({ name, isPacked }) {
  return (
    <li className="item">
      {isPacked ? (
        <del>
          {name + ' ✅'}
        </del>
      ) : (
        name
      )}
    </li>
  );
}

export default function PackingList() {
  return (
    <section>
      <h1>Sally Ride 的行李清单</h1>
      <ul>
        <Item 
          isPacked={true} 
          name="宇航服" 
        />
        <Item 
          isPacked={true} 
          name="带金箔的头盔" 
        />
        <Item 
          isPacked={false} 
          name="Tam 的照片" 
        />
      </ul>
    </section>
  );
}
```

</Sandpack>

对于简单的条件判断，这样的风格可以很好地实现，但需要适量使用。如果你的组件里有很多的嵌套式条件表达式，则需要考虑通过提取为子组件来简化这些嵌套表达式。在 React 里，标签也是你代码中的一部分，所以你可以使用变量和函数来整理一些复杂的表达式。

### 与运算符（`&&`） {/*logical-and-operator-*/}

你会遇到的另一个常见的快捷表达式是 [JavaScript 逻辑与（`&&`）运算符](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Operators/Logical_AND#:~:text=The%20logical%20AND%20(%20%26%26%20)%20operator,it%20returns%20a%20Boolean%20value.)。在 React 组件里，通常用在当条件成立时，你想渲染一些 JSX，**或者不做任何渲染**。使用 `&&`，你也可以实现仅当 `isPacked` 为 `true` 时，渲染勾选符号。

```js
return (
  <li className="item">
    {name} {isPacked && '✅'}
  </li>
);
```

你可以认为，*“当 `isPacked` 为真值时，则（`&&`）渲染勾选符号，否则，不渲染。”*

下面为具体的例子：

<Sandpack>

```js
function Item({ name, isPacked }) {
  return (
    <li className="item">
      {name} {isPacked && '✅'}
    </li>
  );
}

export default function PackingList() {
  return (
    <section>
      <h1>Sally Ride 的行李清单</h1>
      <ul>
        <Item 
          isPacked={true} 
          name="宇航服" 
        />
        <Item 
          isPacked={true} 
          name="带金箔的头盔" 
        />
        <Item 
          isPacked={false} 
          name="Tam 的照片" 
        />
      </ul>
    </section>
  );
}
```

</Sandpack>

当 [JavaScript && 表达式](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Operators/Logical_AND) 的左侧（我们的条件）为 `true` 时，它则返回其右侧的值（在我们的例子里是勾选符号）。但条件的结果是 `false`，则整个表达式会变成 `false`。在 JSX 里，React 会将 `false` 视为一个“空值”，就像 `null` 或者 `undefined`，这样 React 就不会在这里进行任何渲染。


<Pitfall>

**切勿将数字放在 `&&` 左侧.**

JavaScript 会自动将左侧的值转换成布尔类型以判断条件成立与否。然而，如果左侧是 `0`，整个表达式将变成左侧的值（`0`），React 此时则会渲染 `0` 而不是不进行渲染。

例如，一个常见的错误是 `messageCount && <p>New messages</p>`。其原本是想当 `messageCount` 为 0 的时候不进行渲染，但实际上却渲染了 `0`。

为了更正，可以将左侧的值改成布尔类型：`messageCount > 0 && <p>New messages</p>`。

</Pitfall>

### 选择性地将 JSX 赋值给变量 {/*conditionally-assigning-jsx-to-a-variable*/}

当这些快捷方式妨碍写普通代码时，可以考虑使用 `if` 语句和变量。因为你可以使用 [`let`](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Reference/Statements/let) 进行重复赋值，所以一开始你可以将你想展示的（这里指的是物品的名字）作为默认值赋予给该变量。

```js
let itemContent = name;
```

结合 `if` 语句，当 `isPacked` 为 `true` 时，将 JSX 表达式的值重新赋值给 `itemContent`：

```js
if (isPacked) {
  itemContent = name + " ✅";
}
```

[在 JSX 中通过大括号使用 JavaScript](/learn/javascript-in-jsx-with-curly-braces#using-curly-braces-a-window-into-the-javascript-world)。将变量用大括号嵌入在返回的 JSX 树中，来嵌套计算好的表达式与 JSX：

```js
<li className="item">
  {itemContent}
</li>
```

这种方式是最冗长的，但也是最灵活的。下面是相关的例子：

<Sandpack>

```js
function Item({ name, isPacked }) {
  let itemContent = name;
  if (isPacked) {
    itemContent = name + " ✅";
  }
  return (
    <li className="item">
      {itemContent}
    </li>
  );
}

export default function PackingList() {
  return (
    <section>
      <h1>Sally Ride 的行李清单</h1>
      <ul>
        <Item 
          isPacked={true} 
          name="宇航服" 
        />
        <Item 
          isPacked={true} 
          name="带金箔的头盔" 
        />
        <Item 
          isPacked={false} 
          name="Tam 的照片" 
        />
      </ul>
    </section>
  );
}
```

</Sandpack>

跟之前的一样，这个方式不仅仅适用于文本，任意的 JSX 均适用：

<Sandpack>

```js
function Item({ name, isPacked }) {
  let itemContent = name;
  if (isPacked) {
    itemContent = (
      <del>
        {name + " ✅"}
      </del>
    );
  }
  return (
    <li className="item">
      {itemContent}
    </li>
  );
}

export default function PackingList() {
  return (
    <section>
      <h1>Sally Ride 的行李清单</h1>
      <ul>
        <Item 
          isPacked={true} 
          name="宇航服" 
        />
        <Item 
          isPacked={true} 
          name="带金箔的头盔" 
        />
        <Item 
          isPacked={false} 
          name="Tam 的照片" 
        />
      </ul>
    </section>
  );
}
```

</Sandpack>

如果对 JavaScript 不熟悉，这些不同的风格一开始可能会让你感到不知所措。但是，学习这些将有助于你理解和写任何的 JavaScript 代码，而不仅仅是 React 组件。一开始可以选择一个你喜欢的来用，然后当你忘记其他的怎么用时，可以再翻阅这份参考资料。

<Recap>

* 在 React，你可以使用 JavaScript 来控制分支逻辑。
* 你可以使用 `if` 语句来选择性地返回 JSX 表达式。
* 你可以选择性地将一些 JSX 赋值给变量，然后用大括号将其嵌入到其他 JSX 中。
* 在 JSX 中，`{cond ? <A /> : <B />}` 表示 *“当 `cond` 为真值时, 渲染 `<A />`，否则 `<B />`”*。
* 在 JSX 中，`{cond && <A />}` 表示 *“当 `cond` 为真值时, 渲染 `<A />`，否则不进行渲染”*。
* 快捷的表达式很常见，但如果你更倾向于使用 `if`，你也可以不使用它们。

</Recap>



<Challenges>

#### 用 `? :` 给未完成的物品加上图标 {/*show-an-icon-for-incomplete-items-with--*/}

当 `isPacked` 不为 `true` 时，使用条件运算符 （`cond ? a : b`） 来渲染 ❌

<Sandpack>

```js
function Item({ name, isPacked }) {
  return (
    <li className="item">
      {name} {isPacked && '✅'}
    </li>
  );
}

export default function PackingList() {
  return (
    <section>
      <h1>Sally Ride 的行李清单</h1>
      <ul>
        <Item 
          isPacked={true} 
          name="宇航服" 
        />
        <Item 
          isPacked={true} 
          name="带金箔的头盔" 
        />
        <Item 
          isPacked={false} 
          name="Tam 的照片" 
        />
      </ul>
    </section>
  );
}
```

</Sandpack>

<Solution>

<Sandpack>

```js
function Item({ name, isPacked }) {
  return (
    <li className="item">
      {name} {isPacked ? '✅' : '❌'}
    </li>
  );
}

export default function PackingList() {
  return (
    <section>
      <h1>Sally Ride 的行李清单</h1>
      <ul>
        <Item 
          isPacked={true} 
          name="宇航服" 
        />
        <Item 
          isPacked={true} 
          name="带金箔的头盔" 
        />
        <Item 
          isPacked={false} 
          name="Tam 的照片" 
        />
      </ul>
    </section>
  );
}
```

</Sandpack>

</Solution>

#### 用 `&&` 展示物品的重要性 {/*show-the-item-importance-with-*/}

在这个例子里，每个 `Item` 接收一个名为 `importance` 的数字类型属性。使用 `&&` 运算符渲染 “_（重要性：X）_”，以斜体呈现，但仅作用于那些难度值为非零的物品。你的物品列表后最终应该如下：

* 宇航服 _（重要性: 9）_
* 带金箔的头盔
* Tam 的照片 _（重要性: 6）_

注意别忘了在这两个标签之间加上一个空格！

<Sandpack>

```js
function Item({ name, importance }) {
  return (
    <li className="item">
      {name}
    </li>
  );
}

export default function PackingList() {
  return (
    <section>
      <h1>Sally Ride 的行李清单</h1>
      <ul>
        <Item 
          importance={9} 
          name="宇航服" 
        />
        <Item 
          importance={0} 
          name="带金箔的头盔" 
        />
        <Item 
          importance={6} 
          name="Tam 的照片" 
        />
      </ul>
    </section>
  );
}
```

</Sandpack>

<Solution>

这样应该可以实现：

<Sandpack>

```js
function Item({ name, importance }) {
  return (
    <li className="item">
      {name}
      {importance > 0 && ' '}
      {importance > 0 &&
        <i>（重要性: {importance}）</i>
      }
    </li>
  );
}

export default function PackingList() {
  return (
    <section>
      <h1>Sally Ride 的行李清单</h1>
      <ul>
        <Item 
          importance={9} 
          name="宇航服" 
        />
        <Item 
          importance={0} 
          name="带金箔的头盔" 
        />
        <Item 
          importance={6} 
          name="Tam 的照片" 
        />
      </ul>
    </section>
  );
}
```

</Sandpack>

需注意的是，你必须使用 `importance > 0 && ...` 而不是 `importance && ...`，这样如果 `importantce` 是 `0`， `0` 就不会被渲染出来了！

在这个解决方案里，分别用了两个条件判断在名字和重要性标签里插入一个空格。另外，你也可以通过一个带前导空格的 Fragment ：`importance > 0 && <> <i>...</i></>`，或者将空格放在 `<i>` 标签内：`importance > 0 && <i> ...</i>`, 来实现相同的效果。

</Solution>

#### 用 `if` 和变量重构多余的 `? :` {/*refactor-a-series-of---to-if-and-variables*/}

这个 `Drink` 组件使用了一系列的 `? :` 条件语句，根据 `name` 属性是 `"tea"` 还是 `"coffee"` 来显示不同的信息。问题是，每个饮品的信息是在不同的条件判断里的。请去掉那三个 `? :` 条件，使用一个 `if` 语句来重构这段代码。

<Sandpack>

```js
function Drink({ name }) {
  return (
    <section>
      <h1>{name}</h1>
      <dl>
        <dt>Part of plant</dt>
        <dd>{name === 'tea' ? 'leaf' : 'bean'}</dd>
        <dt>Caffeine content</dt>
        <dd>{name === 'tea' ? '15–70 mg/cup' : '80–185 mg/cup'}</dd>
        <dt>Age</dt>
        <dd>{name === 'tea' ? '4,000+ years' : '1,000+ years'}</dd>
      </dl>
    </section>
  );
}

export default function DrinkList() {
  return (
    <div>
      <Drink name="tea" />
      <Drink name="coffee" />
    </div>
  );
}
```

</Sandpack>

当你使用 `if` 语句完成了以上代码的重构，你会不会有其他的想法去简化它？

<Solution>

很多的方法可以解决这个问题，这是只是其中一个可以切入的点：

<Sandpack>

```js
function Drink({ name }) {
  let part, caffeine, age;
  if (name === 'tea') {
    part = 'leaf';
    caffeine = '15–70 mg/cup';
    age = '4,000+ years';
  } else if (name === 'coffee') {
    part = 'bean';
    caffeine = '80–185 mg/cup';
    age = '1,000+ years';
  }
  return (
    <section>
      <h1>{name}</h1>
      <dl>
        <dt>Part of plant</dt>
        <dd>{part}</dd>
        <dt>Caffeine content</dt>
        <dd>{caffeine}</dd>
        <dt>Age</dt>
        <dd>{age}</dd>
      </dl>
    </section>
  );
}

export default function DrinkList() {
  return (
    <div>
      <Drink name="tea" />
      <Drink name="coffee" />
    </div>
  );
}
```

</Sandpack>

这个例子中，每种饮品的信息是放在一起的，而没有将其分散到多个条件判断里。这会让我们以后可以更容易地增加更多的饮品。

还可以通过将饮品信息存入对象中，从而去掉所有的条件判断语句：

<Sandpack>

```js
const drinks = {
  tea: {
    part: 'leaf',
    caffeine: '15–70 mg/cup',
    age: '4,000+ years'
  },
  coffee: {
    part: 'bean',
    caffeine: '80–185 mg/cup',
    age: '1,000+ years'
  }
};

function Drink({ name }) {
  const info = drinks[name];
  return (
    <section>
      <h1>{name}</h1>
      <dl>
        <dt>Part of plant</dt>
        <dd>{info.part}</dd>
        <dt>Caffeine content</dt>
        <dd>{info.caffeine}</dd>
        <dt>Age</dt>
        <dd>{info.age}</dd>
      </dl>
    </section>
  );
}

export default function DrinkList() {
  return (
    <div>
      <Drink name="tea" />
      <Drink name="coffee" />
    </div>
  );
}
```

</Sandpack>

</Solution>

</Challenges>

---
# Source: responding-to-events.md
---
---
title: 响应事件
translators:
  - Jiacheng787
  - QC-L
  - Neo42
  - Zhou Chenyang
---

<Intro>

使用 React 可以在 JSX 中添加 **事件处理函数**。其中事件处理函数为自定义函数，它将在响应交互（如点击、悬停、表单输入框获得焦点等）时触发。

</Intro>

<YouWillLearn>

* 编写事件处理函数的不同方法
* 如何从父组件传递事件处理逻辑
* 事件如何传播以及如何停止它们

</YouWillLearn>

## 添加事件处理函数 {/*adding-event-handlers*/}

如需添加一个事件处理函数，你需要先定义一个函数，然后 [将其作为 prop 传入](/learn/passing-props-to-a-component) 合适的 JSX 标签。例如，这里有一个没绑定任何事件的按钮：

<Sandpack>

```js
export default function Button() {
  return (
    <button>
      未绑定任何事件
    </button>
  );
}
```

</Sandpack>

按照如下三个步骤，即可让它在用户点击时显示消息：

1. 在 `Button` 组件 **内部** 声明一个名为 `handleClick` 的函数。
2. 实现函数内部的逻辑（使用 `alert` 来显示消息）。
3. 添加 `onClick={handleClick}` 到 `<button>` JSX 中。

<Sandpack>

```js
export default function Button() {
  function handleClick() {
    alert('你点击了我！');
  }

  return (
    <button onClick={handleClick}>
      点我
    </button>
  );
}
```

```css
button { margin-right: 10px; }
```

</Sandpack>

你可以定义 `handleClick` 函数然后 [将其作为 prop 传入](/learn/passing-props-to-a-component) `<button>`。其中 `handleClick` 是一个 **事件处理函数** 。事件处理函数有如下特点:

* 通常在你的组件 **内部** 定义。
* 名称以 `handle` 开头，后跟事件名称。

> 按照惯例，通常将事件处理程序命名为 `handle`，后接事件名。你会经常看到 `onClick={handleClick}`，`onMouseEnter={handleMouseEnter}` 等。

或者，你也可以在 JSX 中定义一个内联的事件处理函数：

```jsx
<button onClick={function handleClick() {
  alert('你点击了我！');
}}>
```

或者，直接使用更为简洁箭头函数：

```jsx
<button onClick={() => {
  alert('你点击了我！');
}}>
```

以上所有方式都是等效的。当函数体较短时，内联事件处理函数会很方便。

<Pitfall>

传递给事件处理函数的函数应直接传递，而非调用。例如：

| 传递一个函数（正确）     | 调用一个函数（错误）     |
| -------------------------------- | ---------------------------------- |
| `<button onClick={handleClick}>` | `<button onClick={handleClick()}>` |

区别很微妙。在第一个示例中，`handleClick` 函数作为 `onClick` 事件处理函数传递。这会让 React 记住它，并且只在用户点击按钮时调用你的函数。

在第二个示例中，`handleClick()` 中最后的 `()` 会在 [渲染](/learn/render-and-commit) 过程中 **立即** 触发函数，即使没有任何点击。这是因为位于 [JSX `{}`](/learn/javascript-in-jsx-with-curly-braces) 之间的 JavaScript 会立即执行。

当你编写内联代码时，同样的陷阱可能会以不同的方式出现：

| 传递一个函数（正确）            | 调用一个函数（错误）    |
| --------------------------------------- | --------------------------------- |
| `<button onClick={() => alert('...')}>` | `<button onClick={alert('...')}>` |


如果按如下方式传递内联代码，并不会在点击时触发，而是会在每次组件渲染时触发：

```jsx
// 这个 alert 在组件渲染时触发，而不是点击时触发！
<button onClick={alert('你点击了我！')}>
```

如果你想要定义内联事件处理函数，请将其包装在匿名函数中，如下所示：

```jsx
<button onClick={() => alert('你点击了我！')}>
```

这里创建了一个稍后调用的函数，而不会在每次渲染时执行其内部代码。

在这两种情况下，你都应该传递一个函数：

* `<button onClick={handleClick}>` 传递了 `handleClick` 函数。
* `<button onClick={() => alert('...')}>` 传递了 `() => alert('...')` 函数。

> [了解更多箭头函数的信息](https://zh.javascript.info/arrow-functions-basics)。

</Pitfall>

### 在事件处理函数中读取 props {/*reading-props-in-event-handlers*/}

由于事件处理函数声明于组件内部，因此它们可以直接访问组件的 props。示例中的按钮，当点击时会弹出带有 `message` prop 的 alert：

<Sandpack>

```js
function AlertButton({ message, children }) {
  return (
    <button onClick={() => alert(message)}>
      {children}
    </button>
  );
}

export default function Toolbar() {
  return (
    <div>
      <AlertButton message="正在播放！">
        播放电影
      </AlertButton>
      <AlertButton message="正在上传！">
        上传图片
      </AlertButton>
    </div>
  );
}
```

```css
button { margin-right: 10px; }
```

</Sandpack>

此处有两个按钮，会展示不同的消息。你可以尝试更改传递给它们的消息。

### 将事件处理函数作为 props 传递 {/*passing-event-handlers-as-props*/}

通常，我们会在父组件中定义子组件的事件处理函数。比如：置于不同位置的 `Button` 组件，可能最终执行的功能也不同 —— 也许是播放电影，也许是上传图片。

为此，将组件从父组件接收的 prop 作为事件处理函数传递，如下所示：

<Sandpack>

```js
function Button({ onClick, children }) {
  return (
    <button onClick={onClick}>
      {children}
    </button>
  );
}

function PlayButton({ movieName }) {
  function handlePlayClick() {
    alert(`正在播放 ${movieName}！`);
  }

  return (
    <Button onClick={handlePlayClick}>
      播放 "{movieName}"
    </Button>
  );
}

function UploadButton() {
  return (
    <Button onClick={() => alert('正在上传！')}>
      上传图片
    </Button>
  );
}

export default function Toolbar() {
  return (
    <div>
      <PlayButton movieName="魔女宅急便" />
      <UploadButton />
    </div>
  );
}
```

```css
button { margin-right: 10px; }
```

</Sandpack>

示例中，`Toolbar` 组件渲染了一个 `PlayButton` 组件和 `UploadButton` 组件：

- `PlayButton` 将 `handlePlayClick` 作为 `onClick` prop 传入 `Button` 组件内部。
- `UploadButton` 将 `() => alert('正在上传！')` 作为 `onClick` prop 传入 `Button` 组件内部。

最后，你的 `Button` 组件接收一个名为 `onClick` 的 prop。它直接将这个 prop 以 `onClick={onClick}` 方式传递给浏览器内置的 `<button>`。当点击按钮时，React 会调用传入的函数。

如果你遵循某个 [设计系统](https://uxdesign.cc/everything-you-need-to-know-about-design-systems-54b109851969) 时，按钮之类的组件通常会包含样式，但不会指定行为。而 `PlayButton` 和 `UploadButton` 之类的组件则会向下传递事件处理函数。

### 命名事件处理函数 prop {/*naming-event-handler-props*/}

内置组件（`<button>` 和 `<div>`）仅支持 [浏览器事件名称](/reference/react-dom/components/common#common-props)，例如 `onClick`。但是，当你构建自己的组件时，你可以按你个人喜好命名事件处理函数的 prop。

> 按照惯例，事件处理函数 props 应该以 `on` 开头，后跟一个大写字母。

例如，`Button` 组件的 `onClick` prop 本来也可以被命名为 `onSmash`：

<Sandpack>

```js
function Button({ onSmash, children }) {
  return (
    <button onClick={onSmash}>
      {children}
    </button>
  );
}

export default function App() {
  return (
    <div>
      <Button onSmash={() => alert('正在播放！')}>
        播放电影
      </Button>
      <Button onSmash={() => alert('正在上传！')}>
        上传图片
      </Button>
    </div>
  );
}
```

```css
button { margin-right: 10px; }
```

</Sandpack>

上述示例中，`<button onClick={onSmash}>` 代表浏览器内置的 `<button>`（小写）仍然需要使用 `onClick` prop，而自定义的 `Button` 组件接收到的 prop 名称可由你决定！

当你的组件支持多种交互时，你可以根据不同的应用程序命名事件处理函数 prop。例如，一个 `Toolbar` 组件接收 `onPlayMovie` 和 `onUploadImage` 两个事件处理函数：

<Sandpack>

```js
export default function App() {
  return (
    <Toolbar
      onPlayMovie={() => alert('正在播放！')}
      onUploadImage={() => alert('正在上传！')}
    />
  );
}

function Toolbar({ onPlayMovie, onUploadImage }) {
  return (
    <div>
      <Button onClick={onPlayMovie}>
        播放电影
      </Button>
      <Button onClick={onUploadImage}>
        上传图片
      </Button>
    </div>
  );
}

function Button({ onClick, children }) {
  return (
    <button onClick={onClick}>
      {children}
    </button>
  );
}
```

```css
button { margin-right: 10px; }
```

</Sandpack>

请注意，`App` 组件并不需要知道 `Toolbar` 将会对 `onPlayMovie` 和 `onUploadImage` 做 **什么** 。上述示例是 `Toolbar` 的实现细节。其中，`Toolbar` 将它们作为 `onClick` 处理函数传递给了 `Button` 组件，其实还可以通过键盘快捷键来触发它们。根据应用程序特定的交互方式（如 `onPlayMovie`）来命名 prop ，可以让你灵活地更改以后使用它们的方式。

<Note>

确保为事件处理程序使用适当的 HTML 标签。例如，要处理点击事件，请使用 [`<button onClick={handleClick}>`](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/button) 而不是 `<div onClick={handleClick}>`。使用真正的浏览器 `<button>` 启用内置的浏览器行为，如键盘导航。如果你不喜欢按钮的默认浏览器样式，并且想让它看起来更像一个链接或不同的 UI 元素，你可以使用 CSS 来实现。[了解有关编写无障碍标签的更多信息](https://developer.mozilla.org/zh-CN/docs/Learn/Accessibility/HTML)。

</Note>

## 事件传播 {/*event-propagation*/}

事件处理函数还将捕获任何来自子组件的事件。通常，我们会说事件会沿着树向上“冒泡”或“传播”：它从事件发生的地方开始，然后沿着树向上传播。

下面这个 `<div>` 包含两个按钮。`<div>` 和每个按钮都有自己的 `onClick` 处理函数。你认为点击按钮时会触发哪些处理函数？

<Sandpack>

```js
export default function Toolbar() {
  return (
    <div className="Toolbar" onClick={() => {
      alert('你点击了 toolbar ！');
    }}>
      <button onClick={() => alert('正在播放！')}>
        播放电影
      </button>
      <button onClick={() => alert('正在上传！')}>
        上传图片
      </button>
    </div>
  );
}
```

```css
.Toolbar {
  background: #aaa;
  padding: 5px;
}
button { margin: 5px; }
```

</Sandpack>

如果你点击任一按钮，它自身的 `onClick` 将首先执行，然后父级 `<div>` 的 `onClick` 会接着执行。因此会出现两条消息。如果你点击 toolbar 本身，将只有父级 `<div>` 的 `onClick` 会执行。

<Pitfall>

在 React 中所有事件都会传播，除了 `onScroll`，它仅适用于你附加到的 JSX 标签。

</Pitfall>

### 阻止传播 {/*stopping-propagation*/}

事件处理函数接收一个 **事件对象** 作为唯一的参数。按照惯例，它通常被称为 `e` ，代表 "event"（事件）。你可以使用此对象来读取有关事件的信息。

这个事件对象还允许你阻止传播。如果你想阻止一个事件到达父组件，你需要像下面 `Button` 组件那样调用 `e.stopPropagation()` ：

<Sandpack>

```js
function Button({ onClick, children }) {
  return (
    <button onClick={e => {
      e.stopPropagation();
      onClick();
    }}>
      {children}
    </button>
  );
}

export default function Toolbar() {
  return (
    <div className="Toolbar" onClick={() => {
      alert('你点击了 toolbar ！');
    }}>
      <Button onClick={() => alert('正在播放！')}>
        播放电影
      </Button>
      <Button onClick={() => alert('正在上传！')}>
        上传图片
      </Button>
    </div>
  );
}
```

```css
.Toolbar {
  background: #aaa;
  padding: 5px;
}
button { margin: 5px; }
```

</Sandpack>

当你点击按钮时：

1. React 调用了传递给 `<button>` 的 `onClick` 处理函数。
2. 定义在 `Button` 中的处理函数执行了如下操作：
   * 调用 `e.stopPropagation()`，阻止事件进一步冒泡。
   * 调用 `onClick` 函数，它是从 `Toolbar` 组件传递过来的 prop。
3. 在 `Toolbar` 组件中定义的函数，显示按钮对应的 alert。
4. 由于传播被阻止，父级 `<div>` 的 `onClick` 处理函数不会执行。

由于调用了 `e.stopPropagation()`，点击按钮现在将只显示一个 alert（来自 `<button>`），而并非两个（分别来自 `<button>` 和父级 toolbar `<div>`）。点击按钮与点击周围的 toolbar 不同，因此阻止传播对这个 UI 是有意义的。

<DeepDive>

#### 捕获阶段事件 {/*capture-phase-events*/}

极少数情况下，你可能需要捕获子元素上的所有事件，**即便它们阻止了传播**。例如，你可能想对每次点击进行埋点记录，传播逻辑暂且不论。那么你可以通过在事件名称末尾添加 `Capture` 来实现这一点：

```js
<div onClickCapture={() => { /* 这会首先执行 */ }}>
  <button onClick={e => e.stopPropagation()} />
  <button onClick={e => e.stopPropagation()} />
</div>
```

每个事件分三个阶段传播：

1. 它向下传播，调用所有的 `onClickCapture` 处理函数。
2. 它执行被点击元素的 `onClick` 处理函数。 
3. 它向上传播，调用所有的 `onClick` 处理函数。

捕获事件对于路由或数据分析之类的代码很有用，但你可能不会在应用程序代码中使用它们。

</DeepDive>

### 传递处理函数作为事件传播的替代方案 {/*passing-handlers-as-alternative-to-propagation*/}

注意，此处的点击事件处理函数先执行了一行代码，**然后**调用了父组件传递的 `onClick` prop：

```js {4,5}
function Button({ onClick, children }) {
  return (
    <button onClick={e => {
      e.stopPropagation();
      onClick();
    }}>
      {children}
    </button>
  );
}
```

你也可以在调用父元素 `onClick` 函数之前，向这个处理函数添加更多代码。此模式是事件传播的另一种 **替代方案** 。它让子组件处理事件，同时也让父组件指定一些额外的行为。与事件传播不同，它并非自动。但使用这种模式的好处是你可以清楚地追踪因某个事件的触发而执行的整条代码链。

如果你依赖于事件传播，而且很难追踪哪些处理程序在执行，及其执行的原因，可以尝试这种方法。

### 阻止默认行为 {/*preventing-default-behavior*/}

某些浏览器事件具有与事件相关联的默认行为。例如，点击 `<form>` 表单内部的按钮会触发表单提交事件，默认情况下将重新加载整个页面：

<Sandpack>

```js
export default function Signup() {
  return (
    <form onSubmit={() => alert('提交表单！')}>
      <input />
      <button>发送</button>
    </form>
  );
}
```

```css
button { margin-left: 5px; }
```

</Sandpack>

你可以调用事件对象中的 `e.preventDefault()` 来阻止这种情况发生：

<Sandpack>

```js
export default function Signup() {
  return (
    <form onSubmit={e => {
      e.preventDefault();
      alert('提交表单！');
    }}>
      <input />
      <button>发送</button>
    </form>
  );
}
```

```css
button { margin-left: 5px; }
```

</Sandpack>

不要混淆 `e.stopPropagation()` 和 `e.preventDefault()`。它们都很有用，但二者并不相关：

* [`e.stopPropagation()`](https://developer.mozilla.org/docs/Web/API/Event/stopPropagation) 阻止触发绑定在外层标签上的事件处理函数。
* [`e.preventDefault()`](https://developer.mozilla.org/docs/Web/API/Event/preventDefault) 阻止少数事件的默认浏览器行为。

## 事件处理函数可以包含副作用吗？ {/*can-event-handlers-have-side-effects*/}

当然可以！事件处理函数是执行副作用的最佳位置。

与渲染函数不同，事件处理函数不需要是 [纯函数](/learn/keeping-components-pure)，因此它是用来 *更改* 某些值的绝佳位置。例如，更改输入框的值以响应键入，或者更改列表以响应按钮的触发。但是，为了更改某些信息，你首先需要某种方式存储它。在 React 中，这是通过 [state（组件的记忆）](/learn/state-a-components-memory) 来完成的。你将在下一章节了解所有相关信息。

<Recap>

* 你可以通过将函数作为 prop 传递给元素如 `<button>` 来处理事件。
* 必须传递事件处理函数，**而非函数调用！** `onClick={handleClick}` ，不是 `onClick={handleClick()}`。
* 你可以单独或者内联定义事件处理函数。
* 事件处理函数在组件内部定义，所以它们可以访问 props。
* 你可以在父组件中定义一个事件处理函数，并将其作为 prop 传递给子组件。
* 你可以根据特定于应用程序的名称定义事件处理函数的 prop。
* 事件会向上传播。通过事件的第一个参数调用 `e.stopPropagation()` 来防止这种情况。
* 事件可能具有不需要的浏览器默认行为。调用 `e.preventDefault()` 来阻止这种情况。
* 从子组件显式调用事件处理函数 prop 是事件传播的另一种优秀替代方案。

</Recap>



<Challenges>

#### 修复事件处理函数 {/*fix-an-event-handler*/}

点击此按钮理论上应该在黑白主题之间切换页面背景。然而，当你点击它时，什么也没有发生。解决这个问题。（无需担心 `handleClick` 的内部逻辑。）

<Sandpack>

```js {expectedErrors: {'react-compiler': [5, 7]}}
export default function LightSwitch() {
  function handleClick() {
    let bodyStyle = document.body.style;
    if (bodyStyle.backgroundColor === 'black') {
      bodyStyle.backgroundColor = 'white';
    } else {
      bodyStyle.backgroundColor = 'black';
    }
  }

  return (
    <button onClick={handleClick()}>
      切换背景
    </button>
  );
}
```

</Sandpack>

<Solution>

这是由于 `<button onClick={handleClick()}>` 在渲染过程中 _调用_ 了 `handleClick` 函数，而没有将其进行 _传递_。移除 `()` 调用改为 `<button onClick={handleClick}>` 进而修复问题：

<Sandpack>

```js
export default function LightSwitch() {
  function handleClick() {
    let bodyStyle = document.body.style;
    if (bodyStyle.backgroundColor === 'black') {
      bodyStyle.backgroundColor = 'white';
    } else {
      bodyStyle.backgroundColor = 'black';
    }
  }

  return (
    <button onClick={handleClick}>
      切换背景
    </button>
  );
}
```

</Sandpack>

或者，你可以把函数调用包裹在另一个函数内，例如 `<button onClick={() => handleClick()}>` ：

<Sandpack>

```js
export default function LightSwitch() {
  function handleClick() {
    let bodyStyle = document.body.style;
    if (bodyStyle.backgroundColor === 'black') {
      bodyStyle.backgroundColor = 'white';
    } else {
      bodyStyle.backgroundColor = 'black';
    }
  }

  return (
    <button onClick={() => handleClick()}>
      切换背景
    </button>
  );
}
```

</Sandpack>

</Solution>

#### 关联事件 {/*wire-up-the-events*/}

`ColorSwitch` 组件渲染了一个按钮。它应该改变页面颜色。将它与从父组件接收的 `onChangeColor` 事件处理函数关联，以便在点击按钮时改变颜色。

如此操作后，你会发现点击按钮时，也会增加页面点击计数器的值。而编写父组件的同事坚持认为 `onChangeColor` 不应该使得计数器的值递增。应该如何处理？修改问题使得点击按钮 **只** 改变颜色，并且 **不** 增加计数器。

<Sandpack>

```js src/ColorSwitch.js active
export default function ColorSwitch({
  onChangeColor
}) {
  return (
    <button>
      改变颜色
    </button>
  );
}
```

```js src/App.js hidden
import { useState } from 'react';
import ColorSwitch from './ColorSwitch.js';

export default function App() {
  const [clicks, setClicks] = useState(0);

  function handleClickOutside() {
    setClicks(c => c + 1);
  }

  function getRandomLightColor() {
    let r = 150 + Math.round(100 * Math.random());
    let g = 150 + Math.round(100 * Math.random());
    let b = 150 + Math.round(100 * Math.random());
    return `rgb(${r}, ${g}, ${b})`;
  }

  function handleChangeColor() {
    let bodyStyle = document.body.style;
    bodyStyle.backgroundColor = getRandomLightColor();
  }

  return (
    <div style={{ width: '100%', height: '100%' }} onClick={handleClickOutside}>
      <ColorSwitch onChangeColor={handleChangeColor} />
      <br />
      <br />
      <h2>页面点击次数：{clicks}</h2>
    </div>
  );
}
```

</Sandpack>

<Solution>

首先，你需要添加事件处理函数，例如 `<button onClick={onChangeColor}>`。

然而，同时又引入了计数器递增的问题。正如你的同事所坚持的那样，`onChangeColor` 并不符合预期，这主要是因为事件发生向上传播，并且上层的某些事件处理函数执行了递增操作。为了解决这个问题，你需要阻止事件冒泡。但是不要忘记调用 `onChangeColor`。

<Sandpack>

```js src/ColorSwitch.js active
export default function ColorSwitch({
  onChangeColor
}) {
  return (
    <button onClick={e => {
      e.stopPropagation();
      onChangeColor();
    }}>
      改变颜色
    </button>
  );
}
```

```js src/App.js hidden
import { useState } from 'react';
import ColorSwitch from './ColorSwitch.js';

export default function App() {
  const [clicks, setClicks] = useState(0);

  function handleClickOutside() {
    setClicks(c => c + 1);
  }

  function getRandomLightColor() {
    let r = 150 + Math.round(100 * Math.random());
    let g = 150 + Math.round(100 * Math.random());
    let b = 150 + Math.round(100 * Math.random());
    return `rgb(${r}, ${g}, ${b})`;
  }

  function handleChangeColor() {
    let bodyStyle = document.body.style;
    bodyStyle.backgroundColor = getRandomLightColor();
  }

  return (
    <div style={{ width: '100%', height: '100%' }} onClick={handleClickOutside}>
      <ColorSwitch onChangeColor={handleChangeColor} />
      <br />
      <br />
      <h2>页面点击次数：{clicks}</h2>
    </div>
  );
}
```

</Sandpack>

</Solution>

</Challenges>

