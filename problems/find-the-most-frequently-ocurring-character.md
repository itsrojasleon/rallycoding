<div align="center">
  <h1>Find the Most Frquently Ocurring Character</h1>
  <a href="https://prep-app-prod.herokuapp.com/problems/178" target="_blank">178</a>
</div>

### Instructions

You are given a string and integer K as arguments. Return the Kth most
frequently occurring character.

### Requirements

- Must return a single character string

### Examples

#### Example 1:

```shell
solve("aaabbc", 2)
> "b"
```

#### Example 2:

```shell
solve("bbbbxyyzzz", 3)
> "y"
```

### Solution

```javascript
const solve = (strArg, k) => {
  return [...new Set(strArg)][k - 1];
};
solve('bbbbxyyzzz', 3);
```
