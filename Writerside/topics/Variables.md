# Variables

A **variable** in JavaScript is like a labeled container that holds a piece of information.

Think of it as a box with a name where you can store something and retrieve it later when needed.

A value is the actual piece of data stored inside a variable. It could be a number, text, a list, or even a function.

A constant is a value that does not change.

## Declaring Variables in JavaScript

JavaScript provides three ways to declare variables:

1. `var`: old, not recommended for modern code
2. `let`: preferred for variables that change
3. `const`: used for values that should not change

```JavaScript
let age = 25; // A variable named "age" holding the value 25
const name = "Dennis"; // A constant variable holding a text value
var city = "Nairobi"; // Old way of declaring variables
```

## Updating Variables

With `let` and `var`, you can update a variable's value.

```JavaScript
let score = 10;
score = 15; // Now the value of "score" is updated to 15

var player = "CR";
player = "Messi";
```

But `const` cannot be changed once assigned:

```JavaScript
const country = "Kenya";
country = "Uganda"; // ❌ This will cause an error!
```

## Declaring vs. Initializing variables

### Declaring Variables

Declaring a variable means creating it without assigning a value. This tells JavaScript that a variable exists,
but it does not have any value yet.

When you try to read the value of a variable that has been declared but has not been initialized, you will
get `undefined` as the output.

```JavaScript
let age; // Declared but not initialized
console.log(age); // Output: undefined
```

You can then define the variable later

```JavaScript
let age; // Declared but not initialized
age = 25;
console.log(age); // Output: 25
```

### Initializing a variable

Initializing a variable means assigning it an initial value at the time of declaration.

```JavaScript
let age = 25; // Declared AND initialized with a value
console.log(age); // Output: 25
```

**NOTE: `const` must be initialized immediately**
