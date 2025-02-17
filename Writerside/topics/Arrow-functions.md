# Arrow functions

Arrow functions (`=>`) were introduced in ES6 to provide a more concise syntax for writing functions in JavaScript.

They remove the need for the `function` keyword and have a shorter syntax.

<compare>
<code-block lang="JavaScript">
function add(a, b) {
  return a + b;
}

console.log(add(4, 12));
</code-block>
<code-block lang="JavaScript">
const add = (a, b) => a + b;

console.log(add(4, 12));
</code-block>
</compare>


Arrow functions don't have their own `this` keyword. This means they cannot be used as object methods.

Arrow functions, however, excel in scenarios such as **call back for array methods, event listeners, and situations 
where we want to simplify our code (function)**

[Learn more about arrow functions](Functions.md#arrow-functions)