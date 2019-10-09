<div align="center">
  <h1>Find the Character That Doesn't Belong</h1>
  <a href="https://prep-app-prod.herokuapp.com/problems/210" target="_blank">210</a>
</div>

### Instructions

You are given two lowercase single word strings as arguments. The strings are
identical except one has a random character inserted. Return the random inserted
character.

### Requirements

- Must return a single character string

### Examples

```shell
solve("flooding", "floodring")
> "r"
```

### Solution

```javascript
const solve = (strOne, strTwo) => {
  let result = '';

  if (strOne.length >= strTwo.length) {
    for (let i = 0; i < strOne.length; i++) {
      if (strOne[i] !== strTwo[i]) {
        result = strOne[i];
        break;
      }
    }
  } else {
    for (let i = 0; i < strOne.length; i++) {
      if (strOne[i] !== strTwo[i]) {
        result = strTwo[i];
        break;
      }
    }
  }
  return result;
};
solve('congratulatioins', 'congratulations');
```
