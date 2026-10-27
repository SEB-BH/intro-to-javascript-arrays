<h1>
  <span class="headline">Intro to JavaScript Arrays</span>
  <span class="subhead">Concepts</span>
</h1>

**Learning objective:** By the end of this lesson, students will be able to explain an array as an ordered list of values.

## Start with a list

Imagine a training centre which offers three courses: HTML, CSS, and JavaScript.

We could store each course in a separate variable:

```js
const firstCourse = 'HTML';
const secondCourse = 'CSS';
const thirdCourse = 'JavaScript';
```

This becomes difficult when the centre offers 30 courses. We need one place to keep the list.

An **array** stores a list of values under one variable name:

```js
const courses = ['HTML', 'CSS', 'JavaScript'];

console.log(courses);
```

> 📚 An **array** is an _ordered_ list of values. Each value in the list is called an **element** or **item**.

Here, `'HTML'` is one element. `'CSS'` is another. The array contains three elements.

## Order matters

The first course in this list is HTML. The second is CSS. The third is JavaScript.

| Position in our list | Value |
| --- | --- |
| First | `'HTML'` |
| Second | `'CSS'` |
| Third | `'JavaScript'` |

An array keeps this order until our code changes it. It does not sort the values automatically.

An array can contain duplicate values. For example, a list of customer orders might contain `'Notebook'` more than once.

## Why developers use arrays

Arrays can store products in a shopping basket, temperatures recorded in a city, completed tasks, or available choices in a game.

Keeping related values together lets us read one item, add an item, check the list, or repeat an action for every item.

JavaScript arrays can grow and shrink. They can also start empty.

## Values inside arrays

An array can contain strings, numbers, booleans, or other arrays. Later, we will also use arrays containing objects.

For now, we will usually keep one kind of value in each list, though it is possible to mix data types in an array in JavaScript.

> 💡 An **array element** is an item in a list. This is a different use of the word “element” from an HTML element such as `<p>`.

## 🎓 You Do

Without writing code yet:

1. Write a list of three things a delivery app needs to track.
2. Choose one kind of thing from your list, such as delivery locations.
3. Write three example values for that array.
4. Explain to a partner why keeping those values in one list could help a developer.

Read more: [MDN — Arrays for beginners](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Scripting/Arrays).
