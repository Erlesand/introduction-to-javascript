# Exercise: Double All with map()

Write a function which doubles all values in an array and returns it.

At this point in the course we have only looked at ES5 syntax, but I have also provided a solution using ES6 syntax.

## Example

```js
double([1, 2, 3, 4]);

// -> [2, 4, 6, 8]
```

## Solution (ES5)

```js
function double(numbers) {
  return numbers.map(function (number) {
    return number * 2;
  });
}
```

## Explanation

We create a function by using the `function` keyword. In the example above we also provide an **argument**, which is what we use to pass data to the function.

```js
function double(numbers) {
  // ...
}
```

The `map()` method creates a new array and calls a function on each element in the array.

Note that we return this array directly, without using an intermediate array to store the result.

```js
return numbers.map(fn);
```

The function receives the element as its input, and we then return a value; in this case we double the value which was passed to the anonymous function.

```js
function(number) {
    return number * 2;
}
```

## Solution (ES6)

In ES6 we can use arrow functions to create more concise anonymous functions. These are very frequently used when writing modern JavaScript code.

```js
const double = (numbers) => numbers.map((number) => number * 2);
```
