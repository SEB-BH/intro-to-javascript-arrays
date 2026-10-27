<h1>
  <span class="headline">Intro to JavaScript Arrays</span>
  <span class="subhead">Iteration</span>
</h1>

**Learning objective:** By the end of this lesson, students will be able to use a `for` loop to iterate through arrays and manipulate each element.

> 📚 *Iteration* is the process of repeatedly executing a set of instructions or looping through a collection of items (like an array or string) one by one until a specific condition is met or until no more items are left to process.

## Using a `for` loop

A standard `for` loop can iterate through an array. Initialize the loop with `idx` set to `0` - the index of the first element. End iteration at the index of the last element:

```js
// as a reminder, movies is ['Barbie', 'Arrival', 'Harry Potter', 'Dune', 'The Dark Knight']

for (let idx = 0; idx < movies.length; idx++) {
  console.log(movies[idx]);
}
```

Inside the loop, `idx` serves as the index to retrieve elements from the `movies` array. It increments by 1 after the code inside of the `{ }` has been executed until the condition statement (`idx < movies.length`) is no longer true.

We use the `length` property of `movies` to ensure that this loop is dynamic to the size of the array - as elements are added or removed, this same loop will still function.

For our `['Barbie', 'Arrival', 'Harry Potter', 'Dune', 'The Dark Knight']` array, this will result in the following output:

```text
Barbie
Arrival
Harry Potter
Dune
The Dark Knight
```

This loop doesn't do much, but we could do anything we want to inside the `for` loop. Let's number each item.

```js
for (let idx = 0; idx < movies.length; idx++) {
  console.log(`${idx + 1}. ${movies[idx]}`);
}
```

For the same array, this will be the result:

```text
1. Barbie
2. Arrival
3. Harry Potter
4. Dune
5. The Dark Knight
```

## 🎓 You Do

```js
const stockCounts = [8, 3, 12, 1];
```

1. Use a `for` loop to log each index and its stock count.
2. Inside that `for` loop, add an `if` statement. Log `'Low stock'` for counts below `5`.
3. Use `push()` to add another element (for example, `10`) **before the loops**. Run the code again without changing either loop and observe the results.

> ⚠️ JavaScript also provides a `for...in` loop. It's designed mainly for iterating over an object's properties rather than array items. Be sure you're using the correct loop for your needs. A `for...of` loop also exists and has a couple of extra unique features in addition to this more declarative approach.
