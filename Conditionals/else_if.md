# Else-if Statement

The else-if statement allows you to check multiple conditions. It is used in conjunction with if and else to execute a block of code if one of several conditions is true.

## Syntax
```javascript
if (condition1) {

    // code to be executed if condition1 is true

} else if (condition2) {

    // code to be executed if condition2 is true

} else {

    // code to be executed if none of the conditions are true

}
```
## Example:
```javascript
let num = 3;

if (num > 5) {

    console.log('Number is greater than 5');

} else if (num === 5) {

    console.log('Number is equal to 5');

} else {

    console.log('Number is less than 5');

}

// Output: Number is less than 5
```
