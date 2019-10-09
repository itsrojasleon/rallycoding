<div align="center">
  <h1>Find the Missing Number</h1>
  <a href="https://prep-app-prod.herokuapp.com/problems/199" target="_blank">199</a>
</div>

### Instructions

You are given an unsorted array of integers as an argument. When sorted, the
numbers in the array will form a sequence. One number in the sequence is
missing. Return the missing number.

### Requirements

- Must return a single integer.
- Number returned must be between the 0th and Kth index of the given array when
  sorted.
- Must also work with negative integers

### Examples

#### Example 1:

```shell
solve([5, 0, 2, 1, 3])
> 4
```

_Sorted, the array will be 0,1,2,3,5, The missing number in this sequence is 4_

#### Example 2:

```shell
solve([-5, 0, -2, -1, -3])
> 4
```

_Sorted, the array will be -5, -3, -2, -1, 0, The missing number in this
sequence is -4_

### Solution

```javascript
const solve = intArray => {
  let result = '';
  let sorted = intArray.sort((a, b) => a - b);

  for (let i = 0; i < sorted.length; i++) {
    if (i !== sorted.length - 1) {
      if (sorted[i + 1] - sorted[i] !== 1) {
        result = sorted[i] + 1;
      }
    }
  }

  return result;
};
solve([5, 0, 2, 1, 3]);
```
