<div align="center">
  <h1>Reverse Characters in a String</h1>
  <a href="https://prep-app-prod.herokuapp.com/problems/192" target="_blank">192</a>
</div>

### Instructions

You are given a string that forms a sentence as an argument. Reverse the
characters in each word, but not the words themselves. Return the resulting
string.

### Requirements

- Must return a single string
- Must handle uppercase and lowercase characters
- Special characters should also be reversed.
-

### Example

```shell
solve("How are you?")
> "woH era ?uoy"
```

_Adding each digit of the integer argument 6+3+6+8+2+0+6 gives us 31._

### Solution

```javascript
const solve = strArray => {
  let result = [];

  for (let word of strArray.split(' ')) {
    result.push(
      word
        .split('')
        .reverse()
        .join(''),
    );
  }
  return result.join(' ');
};
solve('How are you?');
```
