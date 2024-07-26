1. JavaScript provides various methods to manipulate strings, such as:
   
      1. **Concatenation**: Combining two or more strings using the + operator or concat() method.
  
         ```javascript
         let firstName = 'John';

         let lastName = 'Doe';

         let fullName = firstName + ' ' + lastName;  // 'John Doe'

         // or

         let fullName = firstName.concat(' ', lastName);  // 'John Doe'

      1. **Substring**: Extracting a portion of a string using substring() or slice() methods.
         ```javascript
         let message = 'Hello, world!';

         let substring = message.substring(0, 5);  // 'Hello'

         // or

         let slice = message.slice(0, 5);  // 'Hello'

      1. **UpperCase / LowerCase**: Converting the case of characters using toUpperCase() and toLowerCase() methods.
         ```javascript
         let text = 'JavaScript';

         console.log(text.toUpperCase());  // 'JAVASCRIPT'

         console.log(text.toLowerCase());  // 'javascript'

      1. **Finding Index**: Finding the index of a substring within a string using indexOf() or lastIndexOf()methods.
         ```javascript
         let sentence = 'Learn JavaScript basics';

         console.log(sentence.indexOf('JavaScript'));  // 6

      1. **Replacing**: Replacing parts of a string using replace() method.
         ```javascript
         let message = 'Hello, world!';

         let newMessage = message.replace('world', 'JavaScript');  // 'Hello, JavaScript!'

      1. **Splitting**: Splitting a string into an array of substrings using split() method.
         ```javascript
         let sentence = 'Learn JavaScript basics';

         let words = sentence.split(' ');  // ['Learn', 'JavaScript', 'basics']
