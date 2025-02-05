<!-- #title -->
# Avoid Using "continue" Statement

<!-- #severity -->
*Major*

<!-- #categories -->
- Readability
- Maintainability

<!-- #description -->
## What is it?
Using the `continue` statement within loops can make the code harder to read and understand. It forces readers to track the flow of control, making debugging and maintenance more difficult.

## Why apply it?
Avoiding `continue` statements improves readability and maintainability. Instead of skipping iterations abruptly, restructuring the loop logic makes it clearer and easier to follow.

## How to Fix it?
Instead of using `continue`, use an `if` condition to handle the undesired case gracefully, making the control flow easier to understand.

<!-- #examples -->

## Example 1: 
### Positive
<!-- #positive example description -->
This version avoids using `continue`, making the loop logic clearer and easier to follow.

```js
for (let i = 0; i < 10; i++) {
  if (i !== 5) {  /* Compliant */
    alert("i = " + i);
  }
}
```

### Negative
<!-- #negative example description -->
This version uses `continue`, making the loop harder to read and maintain.

```js
for (let i = 0; i < 10; i++) {
  if (i === 5) {
    continue;  /* Noncompliant */
  }
  alert("i = " + i);
}
