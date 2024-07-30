# Destructuring

Destructuring is a convenient way of extracting multiple values from data stored in objects and arrays. It was introduced in ES6 (ECMAScript 2015) and makes it easier to work with complex data structures.

## Array Destructuring

Array destructuring allows you to unpack values from arrays into distinct variables.

### Basic Syntax
```javascript
const numbers = [1, 2, 3];

const [a, b, c] = numbers;

console.log(a); // Output: 1

console.log(b); // Output: 2

console.log(c); // Output: 3
```
### Skipping Elements

You can skip elements by leaving empty spaces between commas.
```javascript
const numbers = [1, 2, 3, 4];

const [first, , third] = numbers;

console.log(first); // Output: 1

console.log(third); // Output: 3
```
### Default Values

You can assign default values to variables if the array element is undefined.
```javascript
const numbers = [1];

const [a, b = 2] = numbers;

console.log(a); // Output: 1

console.log(b); // Output: 2
```
### Swapping Variables

Array destructuring can be used to swap variables easily.
```javascript
let x = 1;

let y = 2;

[x, y] = [y, x];

console.log(x); // Output: 2

console.log(y); // Output: 1
```
## Object Destructuring

Object destructuring allows you to unpack values from objects into distinct variables.

### Basic Syntax
```javascript
const person = { name: 'Alice', age: 25 };

const { name, age } = person;

console.log(name); // Output: Alice

console.log(age); // Output: 25
```
### Renaming Variables

You can rename the variables when destructuring.
```javascript
const person = { name: 'Alice', age: 25 };

const { name: fullName, age: years } = person;

console.log(fullName); // Output: Alice

console.log(years); // Output: 25
```
### Default Values

You can assign default values to variables if the property is undefined.
```javascript
const person = { name: 'Alice' };

const { name, age = 30 } = person;

console.log(name); // Output: Alice

console.log(age); // Output: 30
```
### Nested Object Destructuring

You can destructure nested objects easily.
```javascript
const person = { name: 'Alice', address: { city: 'Wonderland', zip: 12345 } };

const { name, address: { city, zip } } = person;

console.log(name); // Output: Alice

console.log(city); // Output: Wonderland

console.log(zip); // Output: 12345
```
## Practical Examples

### Function Parameters

Destructuring can be used directly in function parameters.
```javascript
function greet({ name, age }) {

`  `return `Hello, my name is ${name} and I am ${age} years old.`;

}

const person = { name: 'Alice', age: 25 };

console.log(greet(person)); // Output: Hello, my name is Alice and I am 25 years old.
```
### Extracting Data from Arrays

Destructuring is useful for extracting data from arrays returned by functions.
```javascript
function getCoordinates() {

`  `return [10, 20];

}

const [x, y] = getCoordinates();

console.log(x); // Output: 10

console.log(y); // Output: 20
```
### Ignoring Some Returned Values

You can ignore some of the returned values using commas.
```javascript
function getNumbers() {

`  `return [1, 2, 3, 4];

}

const [first, , third] = getNumbers();

console.log(first); // Output: 1

console.log(third); // Output: 3
```
## Summary

Destructuring is a powerful feature in JavaScript that allows for more concise and readable code when working with arrays and objects. It simplifies extracting values, renaming variables, and providing default values. Whether used in variable assignments, function parameters, or complex data structures, destructuring enhances the efficiency of handling data in JavaScript.