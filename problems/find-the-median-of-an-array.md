<div align="center">
  <h1>Find the Median of an Array</h1>
  <a href="https://prep-app-prod.herokuapp.com/problems/214" target="_blank">214</a>
</div>

### Instructions

You are given an array of unsorted integers. Return the median integer of the
array.

The argument array will always have an odd number of at least 3 elements.

### Requirements

- Must return an integer
- Must also handle negative integers

### Example

#### Example 1:

```shell
solve([1, 5, 4, 3, 2])
> 3
```

#### Example 2:

```shell
solve([-5, -12, 3, -3, 95])
> -3
```

### Solution

```javascript
const solve = intArray => {
  let midpoint = Math.floor(intArray.length / 2);
  const sorted = intArray.sort((a, b) => a - b);
  return [...new Set(sorted)][midpoint];
};
solve([1, 5, 4, 3, 2]);
```
