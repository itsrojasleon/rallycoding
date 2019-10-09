<div align="center">
  <h1>Merging Two Sorted Arrays of Strings</h1>
  <a href="https://prep-app-prod.herokuapp.com/problems/237" target="_blank">237</a>
</div>

### Instructions

You are given two sorted arrays of lowercase strings as arguments. Merge the
arrays of strings into one alphabetically sorted array and return the result.

### Requirements

- Must return an array of strings

### Examples

```shell
solve(["x","y","z"],["r","s","w"])
> ["r","s","w","x","y","z"]
```

### Solution

```javascript
const solve = (arrOne, arrTwo) => {
  return [...arrOne, ...arrTwo].sort();
};
solve(['x', 'y', 'z'], ['r', 's', 'w']);
```
