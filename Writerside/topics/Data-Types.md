# Data Types

JavaScript has the following basic data types which are also the primitive data types in JavaScript 
(more about this later):
- **String**
- **Number**
- **Boolean**
- **null**
- **undefined**
- **Bigint**
- **Symbol**

## String
Refers to a sequence of characters enclosed within single quotes (`'`), double quotes (`"`) or backticks.

```JavaScript
let firstName = "john";
let lastName = "doe";
let username = `john_doe`;
```

## Number
JavaScript has only one type for numbers: it can store both integers and decimals.
```JavaScript
let age = 25; // Integer
let price = 99.99; // Decimal
let notANumber = NaN; // Not a Number (invalid math operation)
```

## Boolean
Booleans represent true or false values, often used for decision-making.

Boolean can either be `true` or `false`.
```JavaScript
let isMale = true;
let isFemale = false;
```

## `undefined`
Refers to a variable that has been declared but not initialized

```JavaScript
let country;
console.log(country); // Output: undefined
```

## `null`
`null` is an intentional absence of a value. Unlike `undefined`, which means "not assigned," 
null means "empty on purpose."

```JavaScript
let car = null; // No car yet
```

## BigInt
Used for numbers beyond JavaScript’s `Number.MAX_SAFE_INTEGER` (9,007,199,254,740,991).

```JavaScript
let bigNumber = 123456789012345678901234567890n; // "n" at the end makes it a BigInt
console.log(bigNumber);
```

## Checking the type of a variable using the `typeof` operator
You can check the type of a variable using the `typeof` operator in JavaScript.

```JavaScript
let bigNumber = 123456789012345678901234567890n;
console.log(typeof bigNumber); // bigint
// OR
console.log(typeof bigNumber); // bigint

const age = 25;
const fullName = "John Doe";

console.log(typeof age); // number
console.log(typeof fullName); // string
```