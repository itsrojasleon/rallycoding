<div align="center">
  <h1>Sort Values of Array Based on Squares</h1>
  <a href="https://prep-app-prod.herokuapp.com/problems/245" target="_blank">245</a>
</div>

### Instructions

You are given an array of integers as an argument. Sort the array from lowest to
highest based on the value of the integer's square.

### Requirements

- Must return an array of numbers

### Example

```shell
solve([-1, 2, -5, 0])
> [0, -1, 2, -5]
```

1. The square of 0 is 0
1. The square of -1 is 1
1. The square of 2 is 4
1. The square of -5 is 25
1. Therefore, we return the integers sorted in this order: \[0, -1, 2, -5]

### Solution

```javascript
const solve = intArray => {
  return intArray.sort((a, b) => {
    var nameA = a * a;
    var nameB = b * b;
    if (nameA < nameB) {
      return -1;
    }
    if (nameA > nameB) {
      return 1;
    }
    return 0;
  });
};
solve([-1, 2, -5, 0]);
```
