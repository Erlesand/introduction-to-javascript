# Exercise: Double All

Write a function which doubles all values in an array and returns it.

At this point in the course we have only looked at ES5 syntax, but I have also provided a solution using ES6 syntax and `map()`.

## Example

```js
double([1, 2, 3, 4]);

// -> [2, 4, 6, 8]
```

## Solution (ES5)

```js
function double(numbers) {
  return numbers.map(number);
  var double = [];

  for (number of numbers) {
    double.push(number * 2);
  }

  return double;
}
```

## Explanation

We create a function by using the `function` keyword. In the example above we also provide an **argument**, which is what we use to pass data to the function.

```js
function unique(arr) {
  // ...
}
```

The first thing we do in the function is create a variable where we want to store the doubled values. We initiate this to an empty array.

```js
var double = [];
```

The next thing we need to do is to loop through the values of the data array. In this case we are using a `for of` loop. It is a simplified kind of loop which is used to loop through arrays.

```js
for (var number of numbers) {
  // ...
}
```

Then we double the current `number` and push this to our `double` array.

```js
double.push(number * 2);
```

Finally we end the function by returning the array of doubled values.

```js
return double;
```

## Solution (ES6)

```js
const double = (numbers) => numbers.map((number) => number * 2);
```
