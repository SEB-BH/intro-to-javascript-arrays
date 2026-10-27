<h1>
  <span class="headline">Intro to JavaScript Arrays</span>
  <span class="subhead">Build a Game Board</span>
</h1>

**Learning objective:** By the end of this lesson, students will be able to combine array indexing, updates, loops, `includes()`, and nested arrays to model a simple game board.

## 🎓 You Do: Console-based game board

This challenge uses **only JavaScript and the console**. We have not learned DOM manipulation yet, so we do not need buttons or HTML elements.

Use the same `app.js` file from the lesson. Comment out older examples if their variables cause conflicts.

### Part 1: Create a board

1. Create a variable named `board` with **nine empty strings**.
2. Log the board and its `.length`.
3. Imagine the indexes in this arrangement:

   ```text
   0 | 1 | 2
   ---------
   3 | 4 | 5
   ---------
   6 | 7 | 8
   ```

### Part 2: Update the board

1. Change index `0` to `'X'`.
2. Change index `4` to `'O'`.
3. Change index `8` to `'X'`.
4. Log the board again.
5. Confirm that `.length` is still `9`.

### Part 3: Check the state

1. Use `if` and `===` to check whether index `4` is empty.
2. Use `includes('')` to check whether **any** empty spaces remain.
3. Log a useful message for each check.

### Part 4: Connect board positions and names

Use this array:

```js
const positionNames = [
  'Top left', 'Top middle', 'Top right',
  'Middle left', 'Center', 'Middle right',
  'Bottom left', 'Bottom middle', 'Bottom right'
];
```

Use a `forEach()` loop to print each position name beside its current board value. The index should connect the two arrays.

**Example output for a single line:** `Top left: X`

### Part 5: Read a group of positions

```js
const linesToCheck = [
  [0, 1, 2],
  [0, 4, 8]
];
```

1. Log `linesToCheck[1]`.
2. Store it in a variable named `selectedLine`.
3. Read the three corresponding values from `board` using the numbers in `selectedLine`.
4. Log those three values.

### Part 6: Reset the board

Reassign `board` to a new array of nine empty strings. Confirm that `.length` is `9` and that `board.includes('')` returns `true`.

## Success checklist

- [ ] My board always contains exactly nine elements.
- [ ] I can update a position using an index.
- [ ] I can check for an empty value using `includes()`.
- [ ] I can match a position name with a board value using the same index.
- [ ] I can read board values using a nested array of positions.
- [ ] I can reset the board.

## 🚀 Level Up (optional)

Use the random-selection pattern to pick a random number from `0` to `8`. Log whether the square at that index is empty or already taken. You do **not** need to build a complete game.

> 🧠 Developer habit: After each change, use `console.log()` to check whether your data looks the way you expect. Small checks make debugging easier.
