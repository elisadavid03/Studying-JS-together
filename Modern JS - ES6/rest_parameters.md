# Rest parameters

Rest parameters in JavaScript allow you to represent an indefinite number of arguments as an array. This feature, introduced in ES6 (ECMAScript 2015), makes it easier to work with functions that accept a variable number of arguments.

### Basic Syntax

Rest parameters are indicated by three dots (...) followed by the name of the array that will contain the remaining arguments.
```javascript
function sum(...numbers) {

  return numbers.reduce((total, num) => total + num, 0);

}


console.log(sum(1, 2, 3)); // Output: 6

console.log(sum(1, 2, 3, 4, 5)); // Output: 15
```
## Key Features

### 1. Collecting All Arguments

Rest parameters collect all remaining arguments into an array.
```javascript
function logArguments(...args) {

  console.log(args);

}

logArguments(1, 'a', true); // Output: [1, 'a', true]
```
### 2. Combining with Regular Parameters

You can combine rest parameters with regular parameters, but rest parameters must be the last parameter in the function definition.
```javascript
function multiply(multiplier, ...numbers) {

  return numbers.map(number => number * multiplier);

}

console.log(multiply(2, 1, 2, 3)); // Output: [2, 4, 6]
```
### 3. Default Values

Rest parameters can work alongside parameters with default values.
```javascript
function greet(greeting = 'Hello', ...names) {

  return `${greeting} ${names.join(', ')}`;

}

console.log(greet('Hi', 'Alice', 'Bob')); // Output: Hi Alice, Bob

console.log(greet(undefined, 'Alice', 'Bob')); // Output: Hello Alice, Bob
```
## Practical Examples

### Example 1: Handling Multiple Arguments

A function that calculates the average of any number of arguments.
```javascript
function average(...numbers) {

  const total = numbers.reduce((sum, num) => sum + num, 0);

  return total / numbers.length;

}

console.log(average(1, 2, 3, 4, 5)); // Output: 3
```
### Example 2: Using Rest Parameters with Regular Parameters

A function that takes a required first parameter and any number of additional arguments.
```javascript
function describePerson(name, ...attributes) {

  return `${name} is ${attributes.join(', ')}`;

}

console.log(describePerson('Alice', 'smart', 'kind', 'brave')); // Output: Alice is smart, kind, brave
```
### Example 3: Collecting Additional Arguments

A function that logs a message with a variable number of tags.
```javascript
function logMessage(message, ...tags) {

  console.log(`${message} [${tags.join(', ')}]`);

}

logMessage('System update', 'info', 'system'); // Output: System update [info, system]
```
## Comparison with Arguments Object

Before rest parameters were introduced, functions used the arguments object to access all arguments passed to the function. However, the arguments object is not a true array, which makes it less convenient to work with.
```javascript
function oldSum() {

  const args = Array.prototype.slice.call(arguments);

  return args.reduce((total, num) => total + num, 0);

}


console.log(oldSum(1, 2, 3)); // Output: 6
```
With rest parameters, the code is more readable and straightforward.
```javascript
function newSum(...numbers) {

  return numbers.reduce((total, num) => total + num, 0);

}


console.log(newSum(1, 2, 3)); // Output: 6
```
## Summary

Rest parameters provide a cleaner and more efficient way to handle functions that accept a variable number of arguments in JavaScript. By representing these arguments as an array, rest parameters simplify tasks such as summing numbers, concatenating strings, or any operation that involves a list of values. They are more flexible and easier to use than the traditional arguments object, enhancing both code readability and functionality.
