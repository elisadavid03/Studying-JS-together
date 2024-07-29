In JavaScript, values that are considered "falsy" are treated as false in boolean contexts. 
These include false, 0, '' (empty string), null, undefined, and NaN. 
All other values are considered "truthy" and let falsyValue = 0;

```javascript
let truthyValue = 'Hello';


console.log(Boolean(falsyValue));   // Output: false

console.log(Boolean(truthyValue));  // Output: true
