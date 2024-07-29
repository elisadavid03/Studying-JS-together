### const Keyword in JavaScript

1. **Constant Declaration**:

Variables declared with const are block-scoped like variables declared with let. However, unlike let, variables declared with const must be initialized with a value, and this value cannot be changed through reassignment.

`const pi = 3.14;`

In this example, pi is declared as a constant with the value 3.14.

2. **Immutability**:

Once a value is assigned to a const variable, it cannot be reassigned or redeclared.

`const pi = 3.14;`

`pi = 3.14159;  // Error: Assignment to constant variable`

Attempting to reassign pi to 3.14159 will result in an error (TypeError: Assignment to constant variable). This immutability ensures that constants retain their initial value throughout the program's execution.

3. **Block Scope**:

Like let, variables declared with const are block-scoped. They exist only within the block in which they are defined.

`if (true) {`

    const message = 'Hello!';

    console.log(message);  // Output: Hello!

`}`

`console.log(message);  // Error: message is not defined`

Here, message is scoped to the if block and cannot be accessed outside of it.

4. **Declaration and Initialization**:

When you declare a variable with const, you must initialize it with a value. Unlike let, you cannot declare a constvariable without assigning a value.

`const name;  // SyntaxError: Missing initializer in const declaration`

5. **Use Cases**:

Constants: Use const for values that should not change throughout the execution of your program, such as mathematical constants or configuration values.

`const TAX_RATE = 0.08;`

Object and Array Constants: When using const with objects or arrays, the variable itself is immutable, but its properties or elements can still be changed.

`const person = {`

    name: 'Alice',

    age: 30

`};`



`person.age = 31;  // Valid, modifies the age property of person`

`person = {};      // Error, cannot reassign person`

In this example, person cannot be reassigned (person = {} would throw an error), but you can modify its properties (person.age = 31).


**Summary**:

- const is used to declare constants in JavaScript.

- Constants must be initialized at the time of declaration and cannot be reassigned.

- Variables declared with const are block-scoped.

- Use const for values that should not change throughout your program's execution, such as mathematical constants, configuration values, or object references that you do not want to reassign.
