# Default parameters

Default parameters in JavaScript allow you to initialize function parameters with default values if no arguments are provided or if undefined is passed. This feature, introduced in ES6 (ECMAScript 2015), helps make functions more robust and easier to use by providing fallback values for parameters.

## Basic Syntax

You can set a default value for a parameter by using the assignment operator (=) in the function definition.
```javascript
function greet(name = 'Guest') {

  return `Hello, ${name}!`;

}

console.log(greet()); // Output: Hello, Guest!

console.log(greet('Alice')); // Output: Hello, Alice!
```
## Key Features

### 1. Default Values for Parameters

If no argument is provided for a parameter, the default value is used.
```javascript
function add(a = 0, b = 0) {

  return a + b;

}


console.log(add()); // Output: 0

console.log(add(5)); // Output: 5

console.log(add(5, 10)); // Output: 15
```
### 2. Handling undefined

Default parameters only apply when the argument is undefined.
```javascript
function log(message = 'No message provided') {

  console.log(message);

}


log(); // Output: No message provided

log(undefined); // Output: No message provided

log(null); // Output: null

log('Hello!'); // Output: Hello!
```
### 3. Using Expressions as Default Values

You can use expressions to set default values for parameters.
```javascript
function calculatePrice(price, tax = price * 0.1) {

  return price + tax;

}


console.log(calculatePrice(100)); // Output: 110

console.log(calculatePrice(100, 20)); // Output: 120
```
### 4. Using Functions as Default Values

You can also use functions as default values for parameters.
```javascript
function getDefaultValue() {

  return 42;

}


function process(value = getDefaultValue()) {

  return value;

}


console.log(process()); // Output: 42

console.log(process(100)); // Output: 100
```
## Practical Examples

### Example 1: Function with Multiple Default Parameters

A function that creates a user object with default values.
```javascript
function createUser(name = 'Anonymous', age = 18, isAdmin = false) {

  return {

    name,

    age,

    isAdmin

  };

}


console.log(createUser()); // Output: { name: 'Anonymous', age: 18, isAdmin: false }

console.log(createUser('Alice', 25)); // Output: { name: 'Alice', age: 25, isAdmin: false }

console.log(createUser('Bob', 30, true)); // Output: { name: 'Bob', age: 30, isAdmin: true }
```
### Example 2: Logging with a Default Log Level

A function that logs messages with a default log level.
```javascript
function logMessage(message, level = 'info') {

  console.log(`[${level.toUpperCase()}] ${message}`);

}


logMessage('Server started'); // Output: [INFO] Server started

logMessage('User not found', 'error'); // Output: [ERROR] User not found
```
### Example 3: Fetching Data with Default Parameters

A function that fetches data from an API with default parameters.
```javascript
function fetchData(url, method = 'GET', headers = {'Content-Type': 'application/json'}) {

  return fetch(url, { method, headers })

    .then(response => response.json())

    .then(data => console.log(data))

    .catch(error => console.error('Error:', error));

}


fetchData('https://api.example.com/data'); // Uses GET method and default headers

fetchData('https://api.example.com/data', 'POST'); // Uses POST method and default headers
```
## Summary

Default parameters in JavaScript make functions more flexible and robust by providing default values for parameters. This feature simplifies function definitions and usage, ensuring that functions can handle missing or undefined arguments gracefully. By leveraging default parameters, you can write cleaner, more maintainable code with sensible fallback values for function arguments.
