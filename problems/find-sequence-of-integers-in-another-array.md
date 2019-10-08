<div align="center">
  <h1>Find Sequence of integers in another array</h1>
</div>

### Instructions

You are given an array of integers and a shorter array containing a sequence of integers as arguments. Return true if the sequence of integers can be found in the first array.

### Requirements

- Must return either true or false

### Examples

#### Example 1:

```shell
solve([1, 2, 3, 4, 5, 6], [3, 4, 5])
> true
```

#### Example 2:

```shell
solve([1, 2, 3, 4, 5, 6], [3, 5])
> false
```

#### Example 3:

```shell
solve([1, 3, 5, 7], [3, 5])
> true
```


### Solution

```javascript
const solve = (intArray, sequence) => {
  return intArray.toString().includes(sequence.toString())
};

solve([1, 3, 5, 7], [3, 5]);
```