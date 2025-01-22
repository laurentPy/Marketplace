# no-constant-condition

## What
Disallow constant expressions in conditions.

## Why
Conditions that are always true or false can lead to logic errors and unreachable code.

## Fix
Avoid using constant values in conditions.

## Positive Example

```javascript
let x = 5;
if (x > 3) {
  console.log('x is greater than 3');
}
```

## Negative Example

```javascript
if (true) {
  console.log('This will always execute');
}
```
