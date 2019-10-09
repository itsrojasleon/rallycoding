<div align="center">
  <h1>Remove Duplicated Strings</h1>
  <a href="https://prep-app-prod.herokuapp.com/problems/196" target="_blank">196</a>
</div>

### Instructions

You are given an array of strings containing some duplicates as an argument.
Return an array without any duplicated strings.

### Requirements

- Must return an array of strings
- Must be able to handle uppercase, lowercase and special characters
- Must also work with strings of words as well as single character strings

### Example

#### Example 1:

```shell
solve(["a","b","b","a","c","d"])
> ["a","b","c","d"]
```

#### Example 2:

```shell
solve(["a","b","b","Hello!","c","goodbye", "Hello!"])
> ["a","b","Hello!","c","goodbye"]
```

### Solution

```javascript
const solve = strArray => {
  return [...new Set(strArray)];
};
solve(['a', 'b', 'b', 'a', 'c', 'd']);
```
