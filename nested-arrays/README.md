<h1>
  <span class="headline">Intro to JavaScript Arrays</span>
  <span class="subhead">Nested Arrays</span>
</h1>

**Learning objective:** By the end of this lesson, students will be able to access values inside nested arrays and use one array's values as indexes into another array.

## Arrays can contain other arrays

An array can store other arrays. This is called a **nested array**.

For example, we can group employee names by shift:

```js
const shifts = [
  ['Sara', 'Ali'],
  ['Fatima', 'Huda']
];

console.log(shifts[0]); // ['Sara', 'Ali']
console.log(shifts[1]); // ['Fatima', 'Huda']
```

To access a value **inside** one of these arrays, use two pairs of square brackets:

```js
console.log(shifts[0][1]); // Ali
```

Read it in two steps:

1. `shifts[0]` gets the first inner array: `['Sara', 'Ali']`.
2. `[1]` gets the second item from that inner array: `'Ali'`.

## An array can store positions

In a game, an array can store positions we want to examine together:

```js
const linesToCheck = [
  [0, 1, 2],
  [3, 4, 5],
  [6, 7, 8]
];

console.log(linesToCheck[0]); // [0, 1, 2]
console.log(linesToCheck[0][2]); // 2
```

Each inner array is one **group of indexes**.

## Use indexes from one array to read another

```js
const board = ['X', 'X', 'X', '', 'O', '', '', '', ''];
const line = [0, 1, 2];

console.log(line[0]); // 0
console.log(board[line[0]]); // X
console.log(board[line[1]]); // X
console.log(board[line[2]]); // X
```

`board[line[1]]` may look confusing at first. Read it from the inside out:

- `line[1]` is `1`.
- `board[1]` is `'X'`.

This lets an application **store positions separately from the values at those positions**.

## Compare values

Once we can read different positions, we can use `===` to compare their values:

```js
const board = ['X', 'X', 'X', '', 'O', '', '', '', ''];

console.log(board[0] === board[1]); // true
console.log(board[1] === board[4]); // false
```

> 🧠 When checking matching game pieces, remember that two empty strings also match each other. Check that the value is **not empty** when that matters.

## 🎓 You Do

```js
const board = ['X', 'O', 'X', '', 'O', '', 'X', '', ''];
const linesToCheck = [
  [0, 3, 6],
  [1, 4, 7]
];
```

1. Log the first array inside `linesToCheck`.
2. Log the **last index** stored in the first inner array.
3. Use that index to read the matching value from `board`.
4. Use the second inner array to print its three corresponding board values.
5. Compare two of those values using `===`.

**Check:** The first inner array is `[0, 3, 6]`; the value at `board[6]` is `'X'`.
