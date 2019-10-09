<div align="center">
  <h1>Find the First Duplicate</h1>
  <a href="https://prep-app-prod.herokuapp.com/problems/195" target="_blank">195</a>
</div>

### Instructions

You are given an array of integers containing some duplicates as an argument.
Return the first element in the array that is duplicated twice.

### Requirements

- Must return an integer
- Must also handle negative integers
- Must be able to handle cases with multiple duplicate elements

### Example

#### Example 1:

```shell
solve([6, 2, 5, 1, 0, 12, 2])
> 2
```

#### Example 2:

```shell
solve([-6, 1, 5, -6, 0, -2, 3])
> -6
```

#### Example 3:

```shell
solve([3, 1, 5, 1, 0, -2, 3, 5])
> 1
```

_Adding each digit of the integer argument 6+3+6+8+2+0+6 gives us 31._

### Solution

```javascript
const solve = intArray => {
  let charMap = {};
  let max;

  for (let n of intArray) {
    charMap[n] = charMap[n] + 1 || 1;
  }

  for (let char in charMap) {
    if (charMap[char] >= 2) {
      max = char;
      break;
    }
  }
  return Number(max);
};

solve([10, 12, 15, 7, 10, 12, 15]);
```
