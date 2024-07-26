**Strings in JavaScript are immutable, meaning their values cannot be changed once they are created. Methods that modify strings actually return new strings.**

Example:
```javascript
let greeting = 'Hello';

greeting[0] = 'h';  // This has no effect, greeting is still 'Hello'
