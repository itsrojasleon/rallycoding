<div align="center">
  <h1>Additional Characters Needed to Make up a String</h1>
  <a href="https://prep-app-prod.herokuapp.com/problems/193" target="_blank">193</a>
</div>

### Instructions

You are given a lowercase string and an array of lowercase characters as
arguments. Return the number of additional characters that would need to be
added to the array of characters to form the string.

The array of characters will never include characters that are not found in the
argument string.

### Requirements

- Must return a single integer

### Examples

#### Example 1:

```shell
solve("terminal", ["t", "m", "l")
> 5
```

_The array of characters would need five more characters, "e", "r", "i", "n",
"a" to match the argument string, so we return the number 5._

#### Example 2:

```shell
solve("test", ["t", "s", "t")
> 1
```

_The array of characters would need one more character, "e", to match the
argument string, so we return the number 1._

### Solution

```javascript
const solve = (strArg, charArray) => {
  return strArg.length - charArray.length;
};
solve('terminal', ['t', 'm', 'l']);
```
