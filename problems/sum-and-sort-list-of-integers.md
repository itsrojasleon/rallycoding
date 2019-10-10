<div align="center">
  <h1>Sum and Sort List of Integers</h1>
  <a href="https://prep-app-prod.herokuapp.com/problems/182" target="_blank">182</a>
</div>

### Instructions

You are given an array containing some repeated integers as an argument. Sum all
of the identical integers, then return an array containing the unique integers
and the sum sorted in ascending order.

### Requirements

- Must return an array of integers
- Must work with negative integers

### Examples

#### Example 1:

```shell
solve([5,5,5,5,21])
> [20, 21]
```

#### Example 2:

```shell
solve([-1,-1,1,1,3,3,5])
> [-2, 2, 5, 6]
```

### Solution

```javascript
const solve = intArray => {
  let map = {};
  let result = [];

  for (let num of intArray) {
    map[num] = map[num] + 1 || 1;
  }

  for (let n in map) {
    result.push(Number(n) * map[n]);
  }
  return result.sort((a, b) => a - b);
};
solve([5, 5, 5, 5, 21]);
```
