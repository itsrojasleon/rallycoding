<div align="center">
  <h1>Find Integer in Array</h1>
  <a href="https://prep-app-prod.herokuapp.com/problems/159" target="_blank">159</a>
</div>

### Instructions

You are given an array of integers and an integer N as arguments. Return the
number in the array at the index of Integer N.

Integer N will never be more than the length of the argument array - 1.

### Requirements

- Must return an integer

### Examples

#### Example 1:

```shell
solve([20, 30, 40], 0)
> 20
```

#### Example 2:

```shell
solve([3, 0, -1, 8], 2)
> -1
```

### Solution

```javascript
const solve = (intArray, n) => {
  return intArray.find((num, i) => i === n);
};
solve([20, 30, 40], 0);
```
