<div align="center">
  <h1>Add Arrays like Single Numbers</h1>
  <a href="https://prep-app-prod.herokuapp.com/problems/239" target="_blank">239</a>
</div>

### Instructions

You are given two arrays containing single digit integers as arguments.
Interpret all of the elements in the arrays as one large single number instead
of individual numbers and add them together. Return the resulting sum as an
array of individual single digit integers.

### Requirements

- Must return an array of integers

### Example

```shell
solve([1, 8, 7, 6], [1, 2, 3, 4])
> [3, 1, 1, 0]
```

1. We add the number 1876 with 1234 to get 3110.
1. We then return this as an array of single digits \[3, 1, 1, 0].

### Solution

```javascript
const getNumber = arr => {
  return Number(arr.join(''));
};

const solve = (arrOne, arrTwo) => {
  let one = getNumber(arrOne);
  let two = getNumber(arrTwo);

  return (one + two)
    .toString()
    .split('')
    .map(Number);
};
solve([1, 8, 7, 6], [1, 2, 3, 4]);
```
