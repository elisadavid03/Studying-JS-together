# Template literals

Template literals are a feature in JavaScript that allow for easier and more readable string manipulation. They were introduced in ES6 (ECMAScript 2015) and provide a more powerful way to work with strings compared to traditional string concatenation methods.

### Basic Syntax

Template literals are enclosed by backticks (`) instead of single quotes (') or double quotes (").
```javascript
const name = 'Alice';

const greeting = `Hello, ${name}!`;

console.log(greeting); // Output: Hello, Alice!
```
### Key Features

**1. Interpolation**

Template literals support string interpolation, which allows you to embed expressions within the string using ${expression}.
```javascript
const age = 25;

const message = `I am ${age} years old.`;

console.log(message); // Output: I am 25 years old.
```

**2. Multi-line Strings**

Template literals allow for multi-line strings without the need for escape characters like \n.
```javascript
const poem = `Roses are red,

Violets are blue,

Sugar is sweet,

And so are you.`;

console.log(poem);

/\*

Output:

Roses are red,

Violets are blue,

Sugar is sweet,

And so are you.

\*/
```

**3. Expression Embedding**

You can embed any valid JavaScript expression inside a template literal.
```javascript
const a = 10;

const b = 20;

const result = `The sum of a and b is ${a + b}.`;

console.log(result); // Output: The sum of a and b is 30.
```
**4. Tagged Templates**

Tagged templates allow you to parse template literals with a function. The function can process the string and the embedded expressions before combining them.
```javascript
function highlight(strings, ...values) {

`  `return strings.reduce((result, string, i) => {

`    `return `${result}${string}<span>${values[i] || ''}</span>`;

`  `}, '');

}

const name = 'Alice';

const age = 25;

const bio = highlight`Name: ${name}, Age: ${age}`;

console.log(bio); // Output: Name: <span>Alice</span>, Age: <span>25</span>
```
### Advantages of Template Literals

- **Readability**: Code is easier to read and write, especially when dealing with multi-line strings or string interpolation.
- **Convenience**: No need for string concatenation operators (+).
- **Expression Embedding**: Directly embed expressions within strings, making the code cleaner.

### Examples

**Example 1: Simple Interpolation**
```javascript
const firstName = 'John';

const lastName = 'Doe';

const fullName = `${firstName} ${lastName}`;

console.log(fullName); // Output: John Doe
```
**Example 2: Multi-line String**
```javascript
const address = `123 Main Street

Apt 4B

Springfield, USA`;

console.log(address);

/\*

Output:

123 Main Street

Apt 4B

Springfield, USA

\*/
```
**Example 3: Complex Expression**
```javascript
const price = 100;

const discount = 0.1;

const finalPrice = `The final price after discount is $${price \* (1 - discount)}.`;

console.log(finalPrice); // Output: The final price after discount is $90.
```
**Example 4: Tagged Template**
```javascript
function upper(strings, ...values) {

`  `return strings.reduce((result, string, i) => {

`    `return `${result}${string}${values[i] ? values[i].toUpperCase() : ''}`;

`  `}, '');

}

const city = 'New York';

const country = 'USA';

const location = upper`City: ${city}, Country: ${country}`;

console.log(location); // Output: City: NEW YORK, Country: USA
```
Template literals make string manipulation in JavaScript more intuitive and efficient, enhancing the overall coding experience.
