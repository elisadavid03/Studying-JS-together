# Switch Statement

The switch statement evaluates an expression and executes a block of code based on matching cases.

## Syntax
```javascript
switch (expression) {

    case value1:

        // code to be executed if expression === value1

        break;

    case value2:

        // code to be executed if expression === value2

        break;

    default:

        // code to be executed if expression doesn't match any case

}
```
## Example:
```javascript
let day = 'Monday';

switch (day) {

    case 'Monday':

        console.log('Today is Monday');

        break;

    case 'Tuesday':

        console.log('Today is Tuesday');

        break;

    default:

        console.log('Not a weekday');

}

// Output: Today is Monday
```
