<div align="center">
  <h1>Find indentical characters in a row</h1>
  <a href="https://prep-app-prod.herokuapp.com/problems/265" target="_blank">265</a>
</div>

### Instructions

You are given a single word string as an argument. Return true if it contains
two identical characters in a row, false if not.

### Requirements

- Must return true or false
- Should also work with special characters

### Examples

#### Example 1:

```shell
solve("terrific")
> true
```

#### Example 2:

```shell
solve("cats")
> false
```

#### Example 3:

```shell
solve("cats!!")
> true
```

### Solution

```javascript
const solve = strArg => {
  let result = false;
  for (let i = 0; i < strArg.length; i++) {
    if (strArg[i] === strArg[i + 1]) {
      result = true;
    }
  }
  return result;
};
solve('terrific');
```
