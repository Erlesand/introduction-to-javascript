# Exercise: Get first letter

Write a function which takes a sentence as an argument and returns the first letter of each word as an array.

At this point in the course we have only looked at the old JavaScript syntax (ES5), but I have also provided a ES6 solution to see what it would look like using modern JavaScript syntax.

## Example

```js
getFirstLetters('Apple Banana Cherry');

// -> ['A', 'B', 'C']
```

## Solution (ES5)

```js
function getFirstLetters(sentence) {
  var words = sentence.split(' ');
  var results = [];

  for (var i = 0; i < words.length; i++) {
    var letter = words[i].charAt(0);
    results.push(letter);
  }

  return results;
}
```

## Explanation

We create a function by using the `function` keyword. In the example above we also provide an **argument**, which is what we use to pass data to the function.

```js
function getFirstLetters(sentence) {
  // ...
}
```

The first thing we do in the function is to split the sentence into an array of words. For this we use `split()`, which is used to split a string into an array of substrings. The argument we provide is the separator, which it the character upon which we want to split the string.

The array is then saved to the variable `words`

```js
var words = sentence.split(' ');
```

We then define a variable and initiate it with an empty array. We need to define it outside the `for`; if we provide the function with an empty sentence, we won't enter the loop, but we still want to be able to return a value (an empty array).

```js
var results = [];
```

Then we set up a loop to loop through all of the words. `words.length` returns the number of items in the array `words`. In the case of `Apple Banana Cherry` it will return 3.

```js
for (var i = 0; i < words.length; i++) {
  // ...
}
```

`words[i]` returns the word in the array at position `i`. For the case when `i` = `0`, then it will return `Apple`.

`charAt(0)` returns the character at position 0. `A` for the case when the string is `Apple`.

```js
var letter = words[i].charAt(0);
```

The last thing we do inside the loop is to push the letter to our `results` array. Push is a method that we have access to when working with arrays, and we use it to add new data at the end of the array.

```js
results.push(letter);
```

Finally we return our `results` array by using the keyword `return` followed by what we want to return.

```
return results
```

## Solution (ES6)

```js
const getFirstLetters = (sentence) =>
  sentence.split(' ').map((word) => word[0]);
```
