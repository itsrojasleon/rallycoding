<div align="center">
  <h1>Sum of Strings</h1>
  <a href="https://prep-app-prod.herokuapp.com/problems/849" target="_blank">849</a>
</div>

### Instructions

Find the sum of two integers represented as strings.

For example, given the string `"123"` and the string `"111"`, your code should
return the string `"234"`.

### Requirements

- Must return an integer

### Examples

| First Argument | Second Argument | Expected Output |
| -------------- | --------------- | --------------- |
| "10"           | "20"            | "30"            |
| "48"           | "2"             | "50"            |
| "-500"         | "500"           | "0"             |

### Solution

```javascript
const solve = (strOne, strTwo) => {
  return (Number(strOne) + Number(strTwo)).toString();
};
solve('-10', '20');
```
