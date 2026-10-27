<h1>
  <span class="headline">Intro to JavaScript Arrays</span>
  <span class="subhead">Checking Array Values</span>
</h1>

**Learning objective:** By the end of this lesson, students will be able to use `includes()` to check whether an array contains a value.

## Does this array contain the value?

Imagine you are building a registration system. Before adding someone to a session, you may want to check whether they are already registered.

The [`includes()`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/includes) method checks whether an array contains a value. It returns a **Boolean**: `true` or `false`.

```js
const registeredNames = ['Sara', 'Ali', 'Fatima'];

console.log(registeredNames.includes('Ali')); // true
console.log(registeredNames.includes('Huda')); // false
```

Use the result in an `if` statement:

```js
const registeredNames = ['Sara', 'Ali', 'Fatima'];

if (registeredNames.includes('Ali')) {
  console.log('Already registered');
} else {
  console.log('Not registered yet');
}
```

> 💡 `includes()` checks for an **exact value**. It is case-sensitive: `'Ali'` and `'ali'` are different strings.

## Checking for missing values

A game might store guesses in an array:

```js
const guessedLetters = ['a', 'e', 'i'];
const newGuess = 'e';

if (guessedLetters.includes(newGuess)) {
  console.log('You already guessed this letter.');
}
```

Sometimes we want to check that a value is **not** in an array. Use the `!` (NOT) operator:

```js
const guessedLetters = ['a', 'e', 'i'];
const newGuess = 'o';

if (!guessedLetters.includes(newGuess)) {
  guessedLetters.push(newGuess);
}

console.log(guessedLetters); // ['a', 'e', 'i', 'o']
```

## Finding empty positions

An empty string (`''`) can represent an unused position in a game board:

```js
const board = ['X', 'O', 'X', '', 'O', '', 'X', '', ''];

console.log(board.includes('')); // true: some spaces are empty
```

If the array no longer includes an empty string, the board is full:

```js
const board = ['X', 'O', 'X', 'X', 'O', 'O', 'O', 'X', 'X'];

if (!board.includes('')) {
  console.log('The board is full.');
}
```

> ⚠️ A full board does **not** automatically mean a tie. A game must also check whether someone has won.

## 🎓 You Do

1. Create an array named `completedTasks` containing `'setup'`, `'design'`, and `'testing'`.
2. Use `includes()` to check whether `'design'` is completed.
3. Create a variable named `newTask` with the value `'deployment'`.
4. If `newTask` is **not** in the array, add it using `push()`.
5. Log the updated array and check your result.

**Check:** The final array should contain four tasks, with no duplicate `'deployment'` entry.
