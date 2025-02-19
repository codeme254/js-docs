# Promises

When working with asynchronous code, we never know beforehand when we will get the results, also, we don't know if the
results will be a success or a failure.

When working with asynchronous JavaScript, there is the concept of **producing code** and **consuming code**.

- **Producing code**: is code that will take some time to complete e.g. fetching user information from a database.
- **Consuming code**: code that must wait for results from producing code

**A promise** is an object that links producing and consuming code.

It is an object that also represents the eventual completion (or failure) of an asynchronous operation and its resulting
value.

It is a readable way to handle asynchronous operations compared to callbacks.

A promise has three states:
- **Pending**: initial state; neither fulfilled nor rejected.
- **Fulfilled**: the operation is completed successfully.
- **Rejection**: the operation has failed.

## Creating a promise
A promise is created using the `new Promise()` constructor.

The `new Promise()` constructor accepts a single argument, which is a function called **executor**.

The promise executes the **executor function** immediately.

The executor function takes two parameters: the first parameter is a function to call with a value when the promise is
fulfilled _(mostly referred to as resolve)_, and the second is a function to call when the promise fails _(mostly
referred to as reject)_

```JavaScript
let myPromise = new Promise(function (resolve, reject) {
  let x = 1;
  if (x === 1) {
    resolve("x is 1");
  } else {
    reject("x is not 1");
  }
});
```

## Consuming a promise
We can then use `.then()` to handle resolved value and `.catch()` to handle errors (rejected value).

`.then()` takes a callback function, which receives the resolved value of the Promise as its argument.

`.catch()` also takes a callback function, which receives the error (rejected value) as its argument 
when the Promise is rejected.

```JavaScript
let myPromise = new Promise(function (resolve, reject) {
  let x = 5;
  if (x === 1) {
    resolve("x is 1");
  } else {
    reject("x is not 1");
  }
});

myPromise
  .then((result) => {
    console.log(result);
  })
  .catch((error) => {
    console.log(error);
  });
```

There is also `.finally()` which gets executed regardless of whether the promise was a success or failure;

```JavaScript
let myPromise = new Promise(function (resolve, reject) {
  let x = 1;
  if (x === 1) {
    resolve("x is 1");
  } else {
    reject("x is not 1");
  }
});

myPromise
  .then((result) => {
    console.log(result);
  })
  .catch((error) => {
    console.log(error);
  })
  .finally(() => {
    console.log("It was nice working with this promise");
  });
```

## Returning a promise from a function
we can also return a promise from a function:

```JavaScript
function fetchUser() {
  return new Promise(function (resolve, reject) {
    let error = false;
    if (error === true) {
      reject("There was an error");
    } else {
      resolve({ username: "_john", role: "Admin" });
    }
  });
}

fetchUser()
  .then((user) => {
    console.log(`Username: ${user.username}, Role: ${user.role}`);
  })
  .catch((error) => {
    console.log(error);
  });
```