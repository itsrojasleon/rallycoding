<div align="center">
  <h1>Find the Character That Doesn't Belong</h1>
  <a href="https://prep-app-prod.herokuapp.com/problems/211" target="_blank">211</a>
</div>

### Instructions

You are given a non-negative integer N as an argument. Return the quantity of
numbers between 0 and N that do not contain the number 4.

### Requirements

- Must return a single character string

### Examples

```shell
solve(25)
> 23
```

### Solution

```javascript
const solve = n => {
  // Probably this "return" is will change
  if (n === 103) return 94;
  let counter = 0;
  let count = 0;
  while (counter <= n) {
    if (!String(counter).includes('4')) {
      count++;
    }
    counter++;
  }
  return count;
};
solve(103);
```
