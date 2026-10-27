<h1>
  <span class="headline">Intro to JavaScript Arrays</span>
  <span class="subhead">Manipulation</span>
</h1>

**Learning objective:** By the end of this lesson, students will be able to update existing array elements and utilize methods like `push()` and `pop()` to add or remove elements at the start or end of an array.


## Change an existing element

```js
const tasks = ['Check stock', 'Send invoice', 'Book delivery'];

tasks[1] = 'Email invoice';

console.log(tasks);
// ['Check stock', 'Email invoice', 'Book delivery']
```

Read `tasks[1] = 'Email invoice'` as: “Replace the value at index 1.” The other elements keep their positions. The length stays `3`.

## Changing contents and replacing the array

We declared `tasks` with `const`. That stops us assigning a different value to the variable. It still allows changes **inside the existing array**.

```js
tasks[0] = 'Count stock'; // Allowed: change an item in the existing array.

// Do not run this line:
// tasks = ['Prepare report']; // TypeError: reassigning a const.
```

Changing an existing array is called **mutation**. Assigning the variable a different array is called **reassignment**.

If a program needs reassignment, declare that variable with `let`. We will use that when resetting application data later.

## Call an array method

A **method** is a function we use through a value, such as an array. The pattern is `arrayName.methodName(arguments)`.

The parentheses call the method. An **argument** is information we pass into that call.

### Add to the end with `push()`

```js
tasks.push('Prepare report');

console.log(tasks);
// ['Count stock', 'Email invoice', 'Book delivery', 'Prepare report']
```

`push()` changes the array by adding an element to the end. It can also add several elements in one call:

```js
tasks.push('Review budget', 'Update calendar');

console.log(tasks);
// ['Count stock', 'Email invoice', 'Book delivery', 'Prepare report', 'Review budget', 'Update calendar']
```

`push()` **returns** the new length. A return value is a value a method gives back to our code. The return value is separate from the change to the array.

```js
const newLength = movies.push('Dune', 'The Dark Knight');

console.log(newLength); // 5
console.log(tasks.length); // 5
```

> 🧠 Use `tasks.push('New task');` to update the list. Do not accidentally replace your array variable with the result of `push()`; that result is a number.

### Remove from the end with `pop()`

```js
const removedTask = tasks.pop();

console.log(removedTask); // Update calendar
console.log(tasks);
// ['Count stock', 'Email invoice', 'Book delivery', 'Prepare report', 'Review budget']
```

`pop()` removes one element from the end and returns the removed value. It takes no arguments.

```js
const noTasks = [];
const removedFromEmpty = noTasks.pop();

console.log(removedFromEmpty); // undefined
console.log(noTasks); // []
```

## Choose the right action

| Goal | Code | Does the length change? |
| --- | --- | --- |
| Replace an existing value | `tasks[1] = 'Check invoice';` | No |
| Add to the end | `tasks.push('Check invoice');` | Yes |
| Remove from the end | `tasks.pop();` | Yes, unless already empty |

Use existing indexes when updating a position. Writing to a far-away index, such as `tasks[20]`, can leave gaps in the array. Use `push()` when you mean “add to the end.”


## 🎓 You Do

1. Create `const books = [];`.
2. Add `'Learning JavaScript'` and `'Web Design Basics'` with one `push()` call.
3. Log the second book.
4. Replace the second book with `'Accessible Websites'`.
5. Add `'Working with Data'`.
6. Use `pop()` and save its return value in `removedBook`.
7. Log `books`, `removedBook`, and `books.length`.

Your final array should contain two books: `'Learning JavaScript'` and `'Accessible Websites'`.
