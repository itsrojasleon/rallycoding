<div align="center">
  <h1>Array as a Single Integer</h1>
  <a href="https://prep-app-prod.herokuapp.com/problems/233" target="_blank">233</a>
</div>

### Instructions

You are given an array of single-digit integers that represents a number and an
integer K as arguments. Add the integer K to this "number" and return the result
as an array of single digit integers.

### Requirements

- Must return an array of integers

### Example

#### Example 1:

```shell
solve([9, 8, 7, 6], 39 )
> [9, 9, 1, 5]
```

_We add 39 to 9876 which gives us 9915, so we return this integer as \[9,9,1,5]_

#### Example 2:

```shell
solve([2,1,0,5], 100 )
> [2, 2, 0, 5]
```

_We add 100 to 2105 which gives us 2205, so we return this integer as
\[2,2,0,5]_

### Solution

```javascript
const solve = (intArray, int) => {
  let n = Number(intArray.join('')) + int;
  return n
    .toString()
    .split('')
    .map(Number);
};
solve([9, 8, 7, 6], 39);
```
