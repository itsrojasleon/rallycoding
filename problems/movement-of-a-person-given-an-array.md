<div align="center">
  <h1>Movement of a Person given an Array</h1>
  <a href="https://prep-app-prod.herokuapp.com/problems/670" target="_blank">670</a>
</div>

### Instructions

You are given an array containing strings of directions (up, down, left, right)
as an argument. Imagine a person standing on a grid at point 0, 0. For each
direction in the array of strings, move your person in that direction on the
grid. Return the final X,Y point that the person is standing at as an array of
two integers.

### Requirements

- Must return an array of two integers

### Example

```shell
solve(["up", "up", "down", "left", "left", "right", "up"])
> [-1, 2]
```

### Solution

```javascript
const solve = directions => {
  let x = 0;
  let y = 0;

  for (let char of directions) {
    if (char === 'up') y++;
    if (char === 'right') x++;
    if (char === 'down') y--;
    if (char === 'left') x--;
  }
  return [x, y];
};
solve(['up', 'up', 'down', 'left', 'left', 'right', 'up']);
```
