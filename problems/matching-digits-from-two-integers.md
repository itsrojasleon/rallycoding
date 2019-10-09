<div align="center">
  <h1>Matching Digits From Two Integers</h1>
  <a href="https://prep-app-prod.herokuapp.com/problems/259" target="_blank">259</a>
</div>

### Instructions

You are given two non-negative integers as an argument. Return an array of
integers containing the matching digits from the two integers.

### Requirements

- Must return an array of integers

### Examples

#### Example 1:

```shell
solve(3762, 72996)
> [7,6,2]
```

#### Example 2:

```shell
solve(1456, 172496)
> [1,4,6]
```

### Solution

```javascript
const solve = (intOne, intTwo) => {
  let result = [];
  let one = intOne.toString().split('');
  let two = intTwo.toString().split('');

  for (let num of one) {
    if (two.includes(num)) {
      result.push(Number(num));
    }
  }
  return result;
};
solve(3762, 72996);
```
