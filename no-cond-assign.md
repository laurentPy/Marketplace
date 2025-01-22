# no-cond-assign

## What
Disallow assignment operators in conditional expressions.

## Why
Assignments in conditionals can lead to unexpected behavior and make the code harder to read.

## Fix
Use comparison operators instead of assignment operators in conditionals.

## Positive Example

```javascript
if (x === 10) {
  console.log('x is 10');
}
```

## Negative Example

```javascript
if (x = 10) {
  console.log('This always evaluates to true and assigns 10 to x');
}
```
