<div align="center">
  <h1>Reversing an Array of Integers</h1>
  <a href="https://prep-app-prod.herokuapp.com/problems/286" target="_blank">286</a>
</div>

### Instructions

You are given an array of integers as an argument. Reverse the elements in the
array without using any built in 'reverse' functions and return it.

### Requirements

- Must return an array of integers

### Example

```shell
solve([1,2,3,4,5)
> [5,4,3,2,1]
```

### Solution

```javascript
const solve = intArray => {
  let result = [];

  for (let i = intArray.length - 1; i >= 0; i--) {
    result.push(intArray[i]);
  }
  return result;
};

solve([1000, 2, 3, 4, 5]);
```
