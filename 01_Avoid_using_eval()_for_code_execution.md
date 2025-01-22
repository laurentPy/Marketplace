# Avoid using `eval()` for code execution

## What
The `eval()` function evaluates or executes a string of JavaScript code.

## Why
Using `eval()` can lead to security vulnerabilities, such as code injection attacks, and can degrade performance.

## Fix
Avoid using `eval()`; instead, use safer alternatives like `JSON.parse()` for parsing JSON strings or other appropriate functions.

## Positive Example

```javascript
// Using JSON.parse() to parse a JSON string
const jsonString = '{"name": "John", "age": 30}';
const obj = JSON.parse(jsonString);
console.log(obj.name); // Output: John
```

## Negative Example

```javascript
// Using eval() to evaluate a JSON string
const jsonString = '{"name": "John", "age": 30}';
const obj = eval('(' + jsonString + ')');
console.log(obj.name); // Output: John
// Noncompliant: Using eval() can lead to code injection vulnerabilities
```
