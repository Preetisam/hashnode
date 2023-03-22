---
title: "What is Temporal Dead Zone(TDZ)"
datePublished: Wed Feb 01 2023 10:16:57 GMT+0000 (Coordinated Universal Time)
cuid: cldlikymm000h09l6h2wh8qib
slug: what-is-temporal-dead-zonetdz
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1675248555791/418f704a-ab04-4fd8-bb19-c9b0fc8b47e6.png
tags: js, javascript, tdz

---

Temporal Dead Zone (TDZ) is a concept in JavaScript that refers to the time period between the declaration of a variable and its assignment, during which the variable is in an undefined state.

In JavaScript, variables declared with the "var" keyword are hoisted to the top of the scope in which they are declared. This means that they are available throughout the entire scope, even before they are declared and assigned a value.

However, variables declared with "let" or "const" is not hoisted, and are only available within the block in which they are declared. Before the variable is assigned a value, it is in a TDZ, and attempting to access the variable during this time will result in a ReferenceError.

Here's an example of TDZ in action:

```plaintext
console.log(x);  // ReferenceError: x is not defined
let x = 5;
```

In the example above, `x` is declared with `let` and is in the TDZ before it is assigned the value of `5`. Accessing `x` before it is assigned a value will result in a ReferenceError.

It's important to be aware of the TDZ when working with variables declared with `let` or `const` to avoid unintended reference errors in your code.