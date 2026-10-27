<h1>
  <span class="headline">Intro to JavaScript Arrays</span>
  <span class="subhead">Instructor Guide</span>
</h1>

## You Do solution - books

Here's a possible solution to the main You Do section:

```js
const books = [];

books.push('The Shining', 'Pride and Prejudice');

console.log(books[1]);

books[1] = 'Dune';

books.forEach((book) => console.log(book));
```

## Teaching the Applying Arrays section

Suggested pacing: **45–65 minutes total** for the five short lessons and their practice. The final **Build a Game Board** challenge can be started together and completed independently.

| Lesson | Teaching emphasis |
| --- | --- |
| Checking Array Values | Contrast `includes()` with checking one specific index. `includes('')` means *at least one* empty space. |
| Random Array Selection | Trace the values produced by `Math.random() * choices.length` before applying `Math.floor()`. |
| Arrays as Game State | Emphasize the difference between replacing a value (`board[0] = 'X'`) and adding an item (`push()`). |
| Connecting Array Indexes | Draw two columns and number their indexes so students can see the relationship. |
| Nested Arrays | Read inside-out: `board[line[1]]` becomes `board[1]`. |
| Build a Game Board | Ask for console output after each action. The goal is array problem-solving, not a complete Tic-Tac-Toe game. |

Common mistakes to watch for:

- Treating an index of `0` as the first *value* instead of the first *position*.
- Using `Math.round()` instead of `Math.floor()` and sometimes selecting an invalid index.
- Forgetting that `includes()` is case-sensitive when working with strings.
- Using `push()` when the intention is to change an existing board position.
- Mistaking `linesToCheck[0][1]` (a number) for `board[linesToCheck[0][1]]` (a board value).
- Assuming a full board is automatically a tie without checking for a winner.

### Build a Game Board: example solution

```js
let board = ['', '', '', '', '', '', '', '', ''];
console.log(board, board.length);

board[0] = 'X';
board[4] = 'O';
board[8] = 'X';
console.log(board, board.length);

if (board[4] === '') {
  console.log('Center square is empty.');
} else {
  console.log('Center square is taken.');
}

if (board.includes('')) {
  console.log('There are empty squares.');
} else {
  console.log('There are no empty squares.');
}

const positionNames = [
  'Top left', 'Top middle', 'Top right',
  'Middle left', 'Center', 'Middle right',
  'Bottom left', 'Bottom middle', 'Bottom right'
];

board.forEach((value, index) => {
  console.log(`${positionNames[index]}: ${value}`);
});

const linesToCheck = [[0, 1, 2], [0, 4, 8]];
const selectedLine = linesToCheck[1];
console.log(selectedLine);
console.log(board[selectedLine[0]], board[selectedLine[1]], board[selectedLine[2]]);

board = ['', '', '', '', '', '', '', '', ''];
console.log(board.length, board.includes(''));
```

## General tips

- **Start with the Basics**: Before diving into complex methods, ensure students understand the fundamental concept of arrays as ordered collections of elements. Use real-life analogies, such as a list of groceries or a line of students in a classroom, to illustrate the point.

- **Hands-on Practice**: Encourage students to actively code along during the lesson. Frequent, short exercises or challenges will help reinforce concepts and boost their confidence in working with arrays.

- **Highlight Common Pitfalls**: Address typical mistakes beginners make, such as off-by-one errors with indexing, or the mutable nature of arrays that can lead to unintended side-effects. Demonstrating these common errors and their solutions can be highly beneficial.

- **Connect to Real-World Scenarios**: Provide practical examples of when and why arrays are used in real programming projects. This not only enhances understanding but also showcases the relevance of the topic in actual software development.

---

🏗️ **Under Construction**

We are constantly working to improve our resources for instructors and students.

**Have something to contribute to this Instructor Guide?** [Let us know](https://pages.git.generalassemb.ly/modular-curriculum-all-courses/universal-resources-internal/module-feedback).
