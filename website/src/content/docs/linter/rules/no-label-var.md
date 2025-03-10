---
title: noLabelVar (since v1.0.0)
---


:::note
This rule is recommended by Biome. A diagnostic error will appear when linting your code.
:::

Disallow labels that share a name with a variable

## Examples

### Invalid

```jsx
const x1 = "test";
x1: expr;
```

<pre class="language-text"><code class="language-text">suspicious/noLabelVar.js:2:1 <a href="https://biomejs.dev/linter/rules/no-label-var">lint/suspicious/noLabelVar</a> ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

<strong><span style="color: Tomato;">  </span></strong><strong><span style="color: Tomato;">✖</span></strong> <span style="color: Tomato;">Do not use the </span><span style="color: Tomato;"><strong>x1</strong></span><span style="color: Tomato;"> variable name as a label</span>
  
    <strong>1 │ </strong>const x1 = &quot;test&quot;;
<strong><span style="color: Tomato;">  </span></strong><strong><span style="color: Tomato;">&gt;</span></strong> <strong>2 │ </strong>x1: expr;
   <strong>   │ </strong><strong><span style="color: Tomato;">^</span></strong><strong><span style="color: Tomato;">^</span></strong>
    <strong>3 │ </strong>
  
<strong><span style="color: rgb(38, 148, 255);">  </span></strong><strong><span style="color: rgb(38, 148, 255);">ℹ</span></strong> <span style="color: rgb(38, 148, 255);">The variable is declared here</span>
  
<strong><span style="color: Tomato;">  </span></strong><strong><span style="color: Tomato;">&gt;</span></strong> <strong>1 │ </strong>const x1 = &quot;test&quot;;
   <strong>   │ </strong>      <strong><span style="color: Tomato;">^</span></strong><strong><span style="color: Tomato;">^</span></strong>
    <strong>2 │ </strong>x1: expr;
    <strong>3 │ </strong>
  
<strong><span style="color: rgb(38, 148, 255);">  </span></strong><strong><span style="color: rgb(38, 148, 255);">ℹ</span></strong> <span style="color: rgb(38, 148, 255);">Creating a label with the same name as an in-scope variable leads to confusion.</span>
  
</code></pre>

### Valid

```jsx
const x = "test";
z: expr;
```

## Related links

- [Disable a rule](/linter/#disable-a-lint-rule)
- [Rule options](/linter/#rule-options)
