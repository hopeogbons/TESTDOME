# JavaScript Interview Questions & Answers

### Question 1: Ensure

Implement the ensure function so that it throws an error if called without arguments or the argument is undefined. Otherwise it should return the given value.

Starting code:

```sh
function ensure(value) {

}
```

Solution:

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

Solution:

```sh
function removeProperty(obj, prop) {
  return (Object.keys(obj).indexOf(prop) > -1) ? delete obj[prop] : false;
}
```

### Question 3: Check Digit

Your company assigns each customer a membership ID, and you are implementing a check digit for those IDs.

The check digit should be calculated by adding up all digits in each membership ID. If the result of the sum is a number with more than a single digit, another iteration is required, and the digits of the result also should be added together. This process should repeat until a single-digit number is calculated.

For example, for the membership ID "55555" the sum of all digits is 25. Because this is not a single-digit number, 2 and 5 would be added, and the result, 7, would be the check digit.

Starting code:

```sh
/**
 * @prop {string} membershipId: The customer's membership ID.
 * @return {number} The check digit.
 */
function createCheckDigit(membershipId) {
  // Write the code that goes here.
  return 0;
}

console.log(createCheckDigit("55555"));
```

Solution:

```sh
/**
 * @prop {string} membershipId: The customer's membership ID.
 * @return {number} The check digit.
 */
function createCheckDigit(membershipId) {
  let sumMembershipId = aggregator(membershipId);
  while (parseInt(sumMembershipId) > 9) sumMembershipId = aggregator(sumMembershipId);
  return sumMembershipId;
}

function aggregator(strMembershipId) {
  return strMembershipId.toString().split('').reduce((a, b) => parseInt(a) + parseInt(b), 0);
}

console.log(createCheckDigit("55555"));
```

### Question 4: Date

Write a function that converts user entered date formatted as M/D/YYYY to a format required by an API (YYYYMMDD). The parameter "userDate" and the return value are strings.

For example, it should convert user entered date "12/31/2014" to "20141231" suitable for the API.

Starting code:

```sh
function formatDate(userDate) {
  // format from M/D/YYYY to YYYYMMDD
}

console.log(formatDate("12/31/2014"));
```

Solution:

```sh
function formatDate(userDate) {
  const x = userDate.split('/');
  return `${x[2]}${x[1]}${x[0]}`;
}

console.log(formatDate("12/31/2014"));
```
