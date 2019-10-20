<div align="center">
  <h1>Find String in 2d Array of Strings</h1>
  <a href="https://prep-app-prod.herokuapp.com/problems/300" target="_blank">300</a>
</div>

### Instructions

You are given a two dimensional array containing arrays of single character
strings and a single string as an argument. Return true if the argument string
can be found across any of the arrays in any orientation, and false if not.

### Requirements

- Must return either true or false

### Examples

#### Example 1:

```shell
solve([["a","z","d"],["r","q","s"],["b","c","p"],["l","t","j"], ["abc"]])
> true
```

_The "abc" string's characters can all be found in the arrays of single
character strings, so we return true._

#### Example 2:

```shell
solve([["a","z","d"],["r","q","s"],["b","c","p"],["l","t","j"], ["truck"]])
> true
```

_The "truck" string's characters "t", "r" and "c" can be found but not "u" or
"k" so we return false._

### Solution

```javascript
const solve = strArray => {
  let result = '';
  let lastArr = strArray.pop().join('');
  let arr = strArray.flat(Infinity);

  for (let i = 0; i < arr.length; i++) {
    if (lastArr.includes(arr[i])) {
      result += arr[i];
    }
  }
  return result === lastArr || result.length >= lastArr.length;
};
solve([
  ['a', 'z', 'd'],
  ['r', 'q', 's'],
  ['b', 'c', 'p'],
  ['l', 't', 'j'],
  ['abc'],
]);
```
