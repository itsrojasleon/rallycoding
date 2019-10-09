<div align="center">
  <h1>Sum Each Digit of an Integer</h1>
  <a href="https://prep-app-prod.herokuapp.com/problems/189" target="_blank">189</a>
</div>

### Instructions

You are given a non-negative integer as an argument. Add each digit of the
integer together and return the sum.

### Requirements

- Must return an integer

### Example

```shell
solve(6368206)
> 31
```

_Adding each digit of the integer argument 6+3+6+8+2+0+6 gives us 31._

### Solution

```javascript
const solve = intArg => {
  return intArg
    .toString()
    .split('')
    .map(n => parseInt(n))
    .reduce((a, b) => a + b, 0);
};
solve(6368206);
```
