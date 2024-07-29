If you declare a variable with const you have to immediately assign a value to it.

Correctness: **Correct**.

- **Explanation**: When you declare a variable using const in JavaScript, you must assign it a value immediately. You cannot declare a const variable without initializing it. For example:

`const constantValue = 10;`

`const anotherConstant;  // SyntaxError: Missing initializer in const declaration`

- This ensures that const variables are always initialized and cannot be left undefined.
