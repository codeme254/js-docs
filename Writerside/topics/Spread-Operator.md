# Spread Operator

The spread operator (`...`) allows you to expand elements of an iterable (like arrays, objects, or strings)
into individual elements.

## Use Cases of The Spread Operator
### Expanding an array
The spread operator takes the array elements and spreads them individually.
```JavaScript
const numbers = [1, 2, 3];
console.log(...numbers); // 1 2 3

const names = ["John", "Doe"];
console.log(...names); // John Doe
```

### Copying arrays
The spread operator can be used to copy array elements, which helps avoid mutate the original array.

For example, instead of:
```JavaScript
const original = [1, 2, 3];
const copy = original;

copy.push(55);
```

We can copy an array as shown:
```JavaScript
const original = [1, 2, 3];
const copy = [...original];
```

### Merging arrays
We can use the spread operator to merge an array:
```JavaScript
const arr1 = [1, 2, 3];
const arr2 = [4, 5, 6];
const merged = [...arr1, ...arr2];

console.log(merged); // [1, 2, 3, 4, 5, 6]
```

### Adding elements from one array to another
```JavaScript
const numbers = [2, 3, 4];
const newNumbers = [1, ...numbers, 5];

console.log(newNumbers); // [1, 2, 3, 4, 5]
```

### Copying objects
```JavaScript
const person = { name: "John", age: 25 };
const copy = { ...person };

console.log(copy); // Output: { name: "John", age: 25 }
```

### Merging objects
```JavaScript
const obj1 = { name: "John" };
const obj2 = { age: 25 };
const merged = { ...obj1, ...obj2 };

console.log(merged); //  { name: "John", age: 25 }
```

### Overwriting Properties
```JavaScript
const user = { name: "John", role: "User" };
const updatedUser = { ...user, role: "Admin" };

console.log(updatedUser); // { name: "John", role: "Admin" }
```
