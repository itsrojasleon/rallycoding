<div align="center">
  <h1>Greatest Difference Between Two Integers</h1>
  <a href="https://prep-app-prod.herokuapp.com/problems/248" target="_blank">248</a>
</div>

### Instructions

You are given an array of non-negative integers as an argument. Return the
greatest difference between any two integers in the array.

### Requirements

- Must return an integer

### Example

```shell
solve([1,3,10,11,13])
> 12
```

_13 - 1 returns 12, the largest difference between two numbers._

### Solution

```javascript
const solve = intArray => {
  return Math.max(...intArray) - Math.min(...intArray);
};
solve([1, 3, 10, 11, 13]);
```
