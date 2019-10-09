<div align="center">
  <h1>Integers in Range of X, Y</h1>
  <a href="https://prep-app-prod.herokuapp.com/problems/158" target="_blank">158</a>
</div>

### Instructions

You are given an array of integers and an array containing a range of integers
(in the form of \[X, Y]) as arguments. Return an array containing all of the
elements from the array of integers that are contained in the range.

X will always be a smaller number than Y.

There will always be at least one integer from the array found the X,Y range.

### Requirements

- Must return an array of integers
- Must work with both positive and negative integers

### Examples

#### Example 1:

```shell
solve([1,2,3,5,6,7], [2,6])
> [3, 5]
```

#### Example 2:

```shell
solve([1,2,3,4,5,10,20], [4,7])
> [4,5]
```

### Solution

```javascript
const solve = (intArray, range) => {
  let result = [];
  for (let i = 0; i < intArray.length; i++) {
    if (intArray[i] > range[0] && intArray[i] < range[1]) {
      result.push(intArray[i]);
    }
  }
  return result;
};
solve([1, 2, 3, 5, 6, 7], [2, 6]);
```
