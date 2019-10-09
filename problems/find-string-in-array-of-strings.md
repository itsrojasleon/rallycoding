<div align="center">
  <h1>Find String in Array of Strings</h1>
  <a href="https://prep-app-prod.herokuapp.com/problems/271" target="_blank">271</a>
</div>

### Instructions

You are given an array of strings and a single string as arguments. Return true
if the single string is also present in the array.

### Requirements

- Must return either true or false

### Examples

#### Example 1:

```shell
solve(['apple', 'orange', 'banana'], 'orange' )
> true
```

#### Example 2:

```shell
solve(['apple', 'orange', 'banana'], 'pear' )
> false
```

### Solution

```javascript
const solve = (strArray, strArg) => {
  return strArray.some(el => strArg === el);
};
solve(['apple', 'orange', 'banana'], 'pear');
```
