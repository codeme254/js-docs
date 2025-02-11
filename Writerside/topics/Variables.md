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

## Rules for naming variables
### Variable names can only start with a letter, underscore (_), or dollar sign ($).

✅Valid examples:
```JavaScript
let name = "Dennis";
let _score = 100;
let $price = 49.99; 
```
❌ Invalid Example:
```JavaScript
let 1stPlace = "Gold"; // ❌ Cannot start with a number
```

### Variable names cannot be JavaScript reserved keywords

❌ Invalid Examples:
```JavaScript
let let = "Hello"; // ❌ "let" is a reserved keyword
let function = 25; // ❌ "function" is a reserved keyword
```

### Variable names can only contain letters, numbers, underscore and the dollar sign, no special characters or spaces
✅ Valid Examples:
```JavaScript
let userAge = 25;
let _totalAmount = 100;
let $discount = 5;
```
❌ Invalid Example:
```JavaScript
let user-age = 25; // ❌ Hyphens are not allowed
let total amount = 100; // ❌ Spaces are not allowed
```

### Variable names are case-sensitive
JavaScript differentiates between uppercase and lowercase letters.
```JavaScript
let Age = 30;
let age = 25;
console.log(Age); // 30
console.log(age); // 25
```
Even though the names look similar, they are treated as separate variables.

### Use meaningful and descriptive names
✅ Good Practice:
```JavaScript
let userName = "John"; 
let totalPrice = 150;
let isLoggedIn = true;
```
❌ Bad Practice:
```JavaScript
let x = "John"; // ❌ Not descriptive
let tp = 150;   // ❌ Unclear what "tp" stands for
```

### If a variable name is made up of multiple words, use the camel case convention
```JavaScript
let userName = "John"; 
let totalPrice = 150;
let isLoggedIn = true;
```