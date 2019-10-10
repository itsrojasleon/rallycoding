<div align="center">
  <h1>Find the Non-Duplicated String</h1>
  <a href="https://prep-app-prod.herokuapp.com/problems/284" target="_blank">284</a>
</div>

### Instructions

You are given an array of strings containing some duplicates as an argument.
Return the string that is not duplicated.

The argument array will only have one string that matches this criteria.

### Requirements

- Must return a single string

### Example

```shell
solve(["orange", "apple", "banana", "apple", "orange"] )
> "banana"
```

### Solution

```javascript
const solve = strArray => {
  let charMap = {};
  let result = '';

  for (let word of strArray) {
    charMap[word] = charMap[word] + 1 || 1;
  }

  for (let char in charMap) {
    if (charMap[char] === 1) {
      result = char;
    }
  }

  return result;
};
solve(['orange', 'apple', 'banana', 'apple', 'orange']);
```
