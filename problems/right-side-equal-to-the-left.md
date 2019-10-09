<div align="center">
  <h1>Right Side Equal to the Left</h1>
  <a href="https://prep-app-prod.herokuapp.com/problems/207" target="_blank">207</a>
</div>

### Instructions

You are given an array of integers as an argument. Return true if there is a
point in the array where the sum of the left hand side would be equal to the sum
of the right hand side.

The argument array will always have an odd number of 3 or more elements.

### Requirements

- Must return true or false
- Must account for negative integers

### Examples

#### Example 1:

```shell
solve([5,4,3,9])
> true
```

Using 3 as the breakpoint, 5 + 4 on the left would equal 9 on the right, so we
return true.\_

#### Example 2:

```shell
solve([5,1,3,9])
> false
```

_Using 1 as the breakpoint. 3 + 9 on the right would not equal 5 on the left.
Using 3 as the breakpoint 5 + 1 on the left would not equal 9 on the right, so
we return false_

#### Example 3:

```shell
solve([5,5,-1,3,9])
> true
```

_Using 3 as the breakpoint, 5 + 5 - 1 on the left would equal 9 on the right, so
we return true_

### Solution

```javascript
const solve = intArray => {
  let sum = 0;
  let leftSum = 0;

  for (let i = 0; i < intArray.length; i++) {
    sum += intArray[i];
  }

  for (let i = 0; i < intArray.length; i++) {
    sum -= intArray[i];

    if (leftSum === sum) return true;

    leftSum += intArray[i];
  }

  return false;
};
solve([10, 25, 2, 8]);
```
