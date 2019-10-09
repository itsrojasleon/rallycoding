<div align="center">
  <h1>Reverse List of Strings</h1>
  <a href="https://prep-app-prod.herokuapp.com/problems/825" target="_blank">825</a>
</div>

### Instructions

You are given an array containing multiple strings as an argument. Return a new
array that has all of the strings listed in opposite order

### Requirements

- Must return an array of strings
- Must work with upper and lowercase letters as well as special characters

### Examples

#### Example 1:

```shell
solve(["Cat","Dog","Skunk","Bird"])
> ["Bird","Skunk","Dog","Cat"]
```

#### Example 2:

```shell
solve(["owl","ferret","Mouse!","Eagle"])
> ["Eagle","Mouse!","ferret","owl"]
```

### Solution

```javascript
const solve = strArray => {
  return strArray.reverse();
};
solve(['Cat', 'Dog', 'Skunk', 'Bird']);
```
