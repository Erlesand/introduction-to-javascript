# Exercise: Unique

Write a function which removes all duplicate values from an array and then returns the new array.

At this point in the course we have only looked at ES5 syntax, but I have also provided a solution using ES6 syntax.

## Example

```js
square([1, 2, 3, 4]);

// -> [1, 2, 3]
```

## Solution (ES5)

```js
function reducer(acc, number) {
  acc.push(number * 2);
  return acc;
}

function double(numbers) {
  return numbers.reduce(reducer, []);
}
```

## Explanation

We create one function, `reducer()`, which is the function that `reduce()` will receive as its first argument.

The function takes two input arguments, an accumulator `acc`, and a value `number`.

We double the number and pass this value to the `acc` array. Finally we return the array.

```js
function reducer(acc, number) {
  acc.push(number * 2);
  return acc;
}
```

`double()` takes an array of numbers as argument. Inside the function we use `reduce()`.

`reduce()` takes two arguments: the first one is a reducer function. This is the `reducer()` which we previously created. The second argument is an initializer, an empty array in our case, `[]`. This is the initial value of `acc`.

```js
function double(numbers) {
  return numbers.reduce(reducer, []);
}
```

## Solution (ES6)

```js
const reducer = (acc, number) => {
  acc.push(number * 2);
  return acc;
};

const double = (numbers) => numbers.reduce(reducer, []);
```
