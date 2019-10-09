<div align="center">
  <h1>Arrays of Integers</h1>
  <a href="https://prep-app-prod.herokuapp.com/problems/163" target="_blank">163</a>
</div>

### Instructions

You are given two arrays of integers as arguments. Return true if they contain
the exact same elements in any order.

### Requirements

- Must return either true or false
- Must account for negative integers

### Example

#### Example 1:

```shell
solve([1,2,7],[7,1,2])
> true
```

#### Example 2:

```shell
solve([5,7],[7,1])
> false
```

#### Example 3:

```shell
solve([5,-7],[-7,5])
> true
```

### Solution

```javascript
const solve = (arrOne, arrTwo) => {
  let a = arrOne.sort((a, b) => a - b);
  let b = arrTwo.sort((a, b) => a - b);

  return a.join('') === b.join('');
};
solve([1, 2, 7], [7, 1, 2]);
```
