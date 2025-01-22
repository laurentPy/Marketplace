# Avoid using `==` for comparison

## What
The `==` operator performs type coercion before comparison, which can lead to unexpected results.

## Why
Using `==` can result in bugs due to implicit type conversion. It is safer and more predictable to use `===`.

## Fix
Always use `===` for strict equality checks to ensure predictable behavior.

## Positive Example

```javascript
// Using strict equality
let a = 0;
console.log(a === false); // Output: false (Compliant)
```

## Negative Example

```javascript
// Using loose equality
let a = 0;
console.log(a == false); // Output: true (Noncompliant: Implicit type coercion)
```
