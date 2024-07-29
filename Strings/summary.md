### Detailed Theory of JavaScript Strings

**Definition**:
- Strings in JavaScript are sequences of characters enclosed within single quotes (`'`) or double quotes (`"`).
- They can contain letters, numbers, symbols, and whitespace.

**String Length**:
- The `length` property of a string returns the number of characters in the string.
- This property is read-only and provides a way to determine the size of the string.

**Accessing Characters**:
- Characters in a string can be accessed using bracket notation (e.g., `string[index]`).
- The index is zero-based, meaning the first character is at index 0.

**String Methods**:
- Concatenation:
  - Combine two or more strings using the `+` operator or the `concat()` method.

- Substring:
  - Extract a part of a string using `substring(startIndex, endIndex)` or `slice(startIndex, endIndex)`.
  - `substring()` does not accept negative indices; `slice()` can accept negative indices to count from the end of the string.

- Case Conversion:
  - Convert all characters in a string to uppercase using `toUpperCase()`.
  - Convert all characters to lowercase using `toLowerCase()`.

- Finding Index:
  - Find the position of the first occurrence of a substring using `indexOf(substring)`.
  - Find the position of the last occurrence of a substring using `lastIndexOf(substring)`.
  - Returns `-1` if the substring is not found.

- Replacing:
  - Replace parts of a string with another string using `replace(substring, newSubstring)`.
  - Only the first occurrence of the substring is replaced unless a regular expression with the global flag is used.

- Splitting:
  - Split a string into an array of substrings using `split(separator)`.
  - The separator can be a string or a regular expression.

**Template Literals**:
- Introduced in ES6, template literals use backticks (``) instead of single or double quotes.
- Allow for embedding expressions inside a string using `${expression}`.
- Support multi-line strings without needing escape characters for new lines.

**Escaping Characters**:
- Certain characters within a string need to be escaped using a backslash (`\`) to avoid syntax errors.
- Examples include escaping quotes, newlines (`\n`), and tabs (`\t`).

Immutable:
- Strings in JavaScript are immutable, meaning their values cannot be changed after they are created.
- Any method that seems to modify a string actually returns a new string with the modification, leaving the original string unchanged.

By understanding these detailed aspects of strings in JavaScript, developers can efficiently manipulate and work with text in their applications.