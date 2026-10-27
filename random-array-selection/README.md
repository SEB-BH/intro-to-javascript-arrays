<h1>
  <span class="headline">Intro to JavaScript Arrays</span>
  <span class="subhead">Random Array Selection</span>
</h1>

**Learning objective:** By the end of this lesson, students will be able to select a random element from an array using `Math.random()`, `Math.floor()`, and `length`.

## Choosing one item at random

A game might need to choose a move for the computer. A support application might need to randomly select a practice question. We can solve both problems with the same pattern.

Start with an array:

```js
const choices = ['rock', 'paper', 'scissors'];
```

JavaScript provides two useful tools:

- [`Math.random()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/random) produces a random number from **0 up to, but not including, 1**.
- [`Math.floor()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/floor) rounds a number **down** to the nearest integer.

Try these expressions in your console:

```js
console.log(Math.random()); // A decimal such as 0.42
console.log(Math.floor(2.9)); // 2
```

## Turn a random number into an array index

An array with three items has indexes `0`, `1`, and `2`.

```js
const choices = ['rock', 'paper', 'scissors'];

const randomIndex = Math.floor(Math.random() * choices.length);
const computerChoice = choices[randomIndex];

console.log(randomIndex);
console.log(computerChoice);
```

Read it from the inside out:

1. `Math.random()` gives a decimal from 0 up to (but not including) 1.
2. Multiply it by `choices.length`. Our result is from 0 up to (but not including) 3.
3. `Math.floor()` rounds down. We get `0`, `1`, or `2`.
4. `choices[randomIndex]` reads the item at that position.

> 💡 Use `.length` instead of typing `3`. If the array grows, the code still works.

> ⚠️ This pattern needs a non-empty array. With an empty array, there is no item to choose.

## 🎓 You Do

```js
const teamMembers = ['Sara', 'Ali', 'Fatima', 'Huda'];
```

1. Create a variable named `randomIndex` using the pattern above.
2. Use it to store a randomly selected name in `selectedMember`.
3. Log the selected name.
4. Run the file several times. Does the selected name change?
5. Add another name to the array. Does the code still work without changing the random-selection expression?

**Check:** Every result should be one of the names in `teamMembers`.
