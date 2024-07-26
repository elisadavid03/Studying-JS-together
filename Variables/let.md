### let Keyword in JavaScript

1. **Block Scope**:

Variables declared with let are block-scoped. This means they are limited to the block (delimited by {}) in which they are defined. This includes blocks such as if, for, while, and also function blocks.

if (true) {

    let message = 'Hello!';

    console.log(message);  // Output: Hello!

}

console.log(message);  // Error: message is not defined

**In the example above**:

message is declared with let inside the if block.

It can be accessed within the block where it's defined (console.log(message) inside the if block).

Attempting to access message outside the block results in an error because it's out of scope.

2. **Variable Reassignment**:

Variables declared with let can have their values reassigned.

let score = 80;

score = 90;  // Updating the value of score

console.log(score);  // Output: 90

Here, score is initially assigned the value 80. Later, its value is updated to 90 without any issues.

3. **Redeclaration**:

Unlike variables declared with var, you cannot redeclare a variable with let in the same scope.

let num = 1;

let num = 2;  // Error: Identifier 'num' has already been declared

This helps avoid accidental variable redeclaration and potential bugs in your code.

4. **Temporal Dead Zone (TDZ)**:

Variables declared with let have a temporal dead zone (TDZ) before their declaration point in the code. This means you cannot access them before their declaration, unlike variables declared with var.

console.log(age);  // ReferenceError: Cannot access 'age' before initialization

let age = 30;

In this example, trying to access age before its declaration results in a ReferenceError. This ensures variables are used only after they have been properly initialized.

5. **Use Cases**:

Loops: let is often used in for loops to avoid unintended behavior caused by var.

for (let i = 0; i < 5; i++) {

    setTimeout(function() {

        console.log(i);  // Outputs 0, 1, 2, 3, 4

    }, 100);

}

Using let in the for loop ensures that each iteration creates a new variable i, preserving its value for each iteration of setTimeout.

Block-scoped Variables: When you need variables that are scoped to a specific block of code and not accessible outside of it, let is the preferred choice.

**Summary**:

- let is used to declare block-scoped variables in JavaScript.

- It prevents variable redeclaration within the same scope.

- Variables declared with let can be reassigned.

- Accessing a let variable before its declaration results in a ReferenceError.

- Use let for variables that are scoped to specific blocks or when you need to reassign values.