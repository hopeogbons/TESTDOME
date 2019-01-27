# JavaScript Interview Wuestions & Answers

### Question 1: Ensure

Implement the ensure function so that it throws an error if called without arguments or the argument is undefined. Otherwise it should return the given value.

Starting code:

```sh
function ensure(value) {

}
```

### Solution 1: Ensure

```sh
function ensure(value) {
  if (value !== undefined) return value;
  throw 'Error';
}
```

### Question 2: Remove Property

Implement the removeProperty function which takes an object and property name, and does the following:

If the object obj has a property prop, the function removes the property from the object and returns true; in all other cases it returns false.

Starting code:

```sh
function removeProperty(obj, prop) {
  return null;
}
```

### Solution 2

```sh
function removeProperty(obj, prop) {
  return (Object.keys(obj).indexOf(prop) > -1) ? delete obj[prop] : false;
}
```
