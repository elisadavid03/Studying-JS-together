Booleans are often used with logical operators (&&, ||, !) to perform logical operations:

**&& (logical AND)**: Returns true if both operands are true, otherwise returns false.

**|| (logical OR)**: Returns true if at least one operand is true, otherwise returns false.

**! (logical NOT)**: Returns the opposite boolean value of the operand (true becomes false and vice versa).

```javascript
let x = true;

let y = false;


console.log(x && y);  // Output: false

console.log(x || y);  // Output: true

console.log(!x);      // Output: false