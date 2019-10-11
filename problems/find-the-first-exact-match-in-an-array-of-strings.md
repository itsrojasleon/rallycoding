<div align="center">
  <h1>Find the First Exact Match in a Array of Strings</h1>
  <a href="https://prep-app-prod.herokuapp.com/problems/275" target="_blank">275</a>
</div>

### Instructions

You are given an array of single characters and an array of lowercase strings as
arguments. Return the first string that contains all of the characters from the
array of characters.

### Requirements

- Must return a string

### Examples

#### Example 1:

```shell
solve(['p', 'p', 'l', 'a', 'e'], ['orange', 'banana', 'apple'])
> 'apple'
```

#### Example 2:

```shell
solve(['p', 'p', 'l', 'a', 'e'], ['applesauce', 'orange', 'banana', 'apple'])
> 'applesauce'
```

_Even though apple is an exact match, we return applesauce since it is the first
string to include all of the characters in the character array._

### Solution

```javascript
const solve = (charArray, strArray) => {
  let result = '';
  let sum = 0;

  for (let i = 0; i < strArray.length; i++) {
    for (let j = 0; j < charArray.length; j++) {
      if (strArray[i].includes(charArray[j])) {
        sum++;
      }
    }
    if (sum === charArray.length) {
      result = strArray[i];
      break;
    }
    sum = 0;
  }
  return result;
};

solve(
  ['s', 'p', 'p', 'l', 'a', 'e'],
  ['applesauce', 'apples', 'orange', 'banana'],
);
```
