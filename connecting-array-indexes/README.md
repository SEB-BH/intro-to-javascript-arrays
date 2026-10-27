<h1>
  <span class="headline">Intro to JavaScript Arrays</span>
  <span class="subhead">Connecting Array Indexes</span>
</h1>

**Learning objective:** By the end of this lesson, students will be able to use the same index to access related information in two arrays.

## One index can connect two lists

Imagine two arrays that store information about the same team. The item at index `0` in each array belongs together.

```js
const employees = ['Sara', 'Ali', 'Fatima'];
const departments = ['Engineering', 'Design', 'Quality Assurance'];

console.log(employees[0]); // Sara
console.log(departments[0]); // Engineering
```

Both values are at **index 0**, so we know Sara works in Engineering.

## Connect the values with a loop

The `forEach()` method provides an `index` parameter, which we learned earlier.

```js
const employees = ['Sara', 'Ali', 'Fatima'];
const departments = ['Engineering', 'Design', 'Quality Assurance'];

employees.forEach((employee, index) => {
  console.log(`${employee} works in ${departments[index]}`);
});
```

Output:

```text
Sara works in Engineering
Ali works in Design
Fatima works in Quality Assurance
```

In each loop, `index` tells us **which position** we are reading from both arrays.

| Loop | `index` | `employee` | `departments[index]` |
| --- | --- | --- | --- |
| First | 0 | Sara | Engineering |
| Second | 1 | Ali | Design |
| Third | 2 | Fatima | Quality Assurance |

> 💡 This works when the arrays are in the same order. If the arrays have different lengths or their positions no longer match, the information may be wrong. Later, we will learn other ways to organize related data.

## Connecting an index to a game board

We can also use indexes to connect board values with board positions:

```js
const board = ['X', '', 'O'];
const positionNames = ['Left', 'Middle', 'Right'];

board.forEach((value, index) => {
  console.log(`${positionNames[index]}: ${value}`);
});
```

The same strategy will be useful when we learn the **DOM**: we can use an index to connect a value in an array to a square on a web page. We will not need the DOM yet for this lesson.

## 🎓 You Do

```js
const tasks = ['Build the homepage', 'Review the code', 'Test the app'];
const owners = ['Huda', 'Ali', 'Sara'];
```

1. Use `forEach()` to print each task and its owner's name on the same line.
2. Add a fourth task and a fourth owner at the same index.
3. Run your code again. Confirm that each task still matches the correct owner.
4. What would happen if one array had fewer items than the other?

**Check:** Your result should include `Build the homepage - Huda`.
