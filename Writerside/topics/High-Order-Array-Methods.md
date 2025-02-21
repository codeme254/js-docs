# High Order Array Methods

JavaScript provides a range of powerful tools for working with arrays, and higher-order methods are among the 
most versatile and expressive.

These methods simplify operations on arrays by allowing us to apply functions to elements directly, improving 
both readability and maintainability.

They include:

## `forEach`
Executes a function on each array element but does not return anything.

Best used when you want to perform an action on each item

It does not create a new array.

```JavaScript
const numbers = [1, 2, 3, 4, 5];

numbers.forEach((num) => {
  console.log(num * 2);
});
// Output: 2, 4, 6, 8, 10
```

## `map`
The `map()` method creates a new array populated with the results of calling a provided function on every element
in the calling array.

Best for transforming array elements without modifying the original array.

It returns a new array.

```JavaScript
const numbers = [1, 2, 3, 4, 5];

const doubled = numbers.map((num) => num * 2);
console.log(doubled);
// Output: [2, 4, 6, 8, 10]
```

## `filter`
The `filter()` method creates a new array with all elements that pass the test implemented by the provided function.

Best for selecting specific elements from an array.

It returns a new array

```JavaScript
const numbers = [1, 2, 3, 4, 5];

const evenNumbers = numbers.filter((num) => num % 2 === 0);
console.log(evenNumbers);
// Output: [2, 4]
```

## `reduce`
The `reduce()` method executes a reducer function (that you provide) on each element of the array, resulting in a 
single output value.

Best for calculating totals, aggregations, or combining values.

It does not return a new array, but it returns the value that the original array has been reduced to.

```JavaScript
const numbers = [1, 2, 3, 4, 5];

const sum = numbers.reduce((acc, num) => acc + num, 0);
console.log(sum);
// Output: 15
```

## `find`
The `find()` method returns the value of the first element in the array that satisfies the provided testing function. 
Otherwise, it returns undefined.

Does not return new but returns the found number instead:

```JavaScript
const numbers = [1, 2, 3, 4];
const found = numbers.find((num) => num === 3);
console.log(found); // Output: 3
```

## `findIndex`
Returns the index of the first element that matches a condition.

```JavaScript
const numbers = [10, 20, 30, 40, 50];

const index = numbers.findIndex((num) => num > 25);
console.log(index);
// 2 
```

## `some`
Checks if at least one element passes a condition.

If so, it returns true, otherwise, it returns false.

```JavaScript
const numbers = [1, 3, 5, 7];

const hasEven = numbers.some((num) => num % 2 === 0);
console.log(hasEven);
// false
```

## `every`
Checks if all elements in an array pass a condition.

If so, it returns true, otherwise it returns false.

```JavaScript
const numbers = [2, 4, 6, 8];

const allEven = numbers.every((num) => num % 2 === 0);
console.log(allEven);
// true
```