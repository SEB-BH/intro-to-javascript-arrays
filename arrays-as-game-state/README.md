<h1>
  <span class="headline">Intro to JavaScript Arrays</span>
  <span class="subhead">Arrays as Game State</span>
</h1>

**Learning objective:** By the end of this lesson, students will be able to represent and update changing game information using an array.

## An array can describe the current situation

So far, we have used arrays to store lists. Arrays can also represent the **state** of an application.

**State** means the information that describes what is happening **right now**. In a game, state might include the current board, the player's guesses, or the score.

Imagine a game board with nine squares:

```text
0 | 1 | 2
---------
3 | 4 | 5
---------
6 | 7 | 8
```

We can represent those positions with one array:

```js
let board = [
  '', '', '',
  '', '', '',
  '', '', ''
];
```

Each **index** matches one position on the board. Each **value** tells us what is currently in that position.

## Update state after an action

If a player chooses the first square, change the value at index `0`:

```js
let board = ['', '', '', '', '', '', '', '', ''];

board[0] = 'X';
board[4] = 'O';

console.log(board);
// ['X', '', '', '', 'O', '', '', '', '']
```

We did not add new items. We **updated the existing positions**. The array still contains nine elements.

Why might this matter? A board game needs a fixed position for each square. `push('X')` would add a tenth item instead of updating a square.

## Read state to make a decision

```js
let board = ['X', '', '', '', 'O', '', '', '', ''];

if (board[0] === '') {
  console.log('Square 0 is free.');
} else {
  console.log('Square 0 is already taken.');
}
```

This is a common programming strategy:

**Read the current state → make a decision → update the state.**

## Reset state

To begin a new game, we can assign a new empty board:

```js
let board = ['X', 'O', 'X', '', '', '', '', '', ''];

board = ['', '', '', '', '', '', '', '', ''];

console.log(board);
```

We use `let` here because we reassign `board` to a new array. If we only updated positions, `const` would also work.

## 🎓 You Do

1. Create an array of nine empty strings named `board`.
2. Place an `'X'` at index `2` and an `'O'` at index `4`.
3. Log the complete board.
4. Write an `if` statement that checks whether index `2` is empty.
5. Check whether the board still contains **any** empty strings using `includes()`.
6. Reset the board to nine empty strings and log it again.

**Check:** The array should always have nine elements.
