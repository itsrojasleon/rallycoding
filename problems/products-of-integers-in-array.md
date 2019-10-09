<div align="center">
  <h1>Products of Integers in Array</h1>
  <a href="https://prep-app-prod.herokuapp.com/problems/306" target="_blank">306</a>
</div>

### Instructions

You are given an array of integers and an integer K as arguments. Return the
product of every integer in the array except for K.

K is guaranteed to always be present in the argument array.

### Requirements

- Must return an integer

### Example

```shell
solve([1,2,3,4,5], 3)
> 40
```

_We skip the number 3 so 1 \ 2 \* 4 \* 5 = 40\*_

### Solution

```javascript
const solve = (intArray, k) => {
  let result = 1;

  for (let i = 0; i < intArray.length; i++) {
    if (intArray[i] !== k) {
      result *= intArray[i];
    }
  }
  return result;
};
```
