# Cheatsheet for Daisy

A compilation of usefull notes, examples and reminders.

---

## `map`

The `map()` method transforms each element of an array and returns a new array with the new values. Use `map()` when you have an array of elements, and you want to get a new array with something else based on those elements.

### Example #1

```js
const numbers = [1, 2, 3];
const doubled = numbers.map((num) => { return num * 2 }); 
// num is whatever name I decided to give to the element I'll receive in the function, can be anything, I gave it num since I know its going to be a number

// The array 'numbers' has 3 elements, therefore we will have 3 iterations in our function, once for each element, 
// and whatever we return will be placed in a new array in the same index of the element we are iterating.

// ITERATION 1 - The element will be '1', therefore (1) => { return 1 * 2 } , which will be '2'
// ITERATION 2 - The element will be '2', therefore (2) => { return 2 * 2 } , which will be '4'
// ITERATION 3 - The element will be '3', therefore (3) => { return 3 * 2 } , which will be '6'

console.log(doubled); // [2, 4, 6]
```

### Example #2

```js
const users = [ { id: 1, name: "Alice", age: 21 }, { id: 2, name: "Bobby", age: 27 } ];
const names = numbers.map((user) => { return user.name });
// user is whatever name I decided to give to the element I'll receive in the function, can be anything, I gave it user since I know its going to be an object representing a user

// The array 'users' has 2 elements, therefore we will have 2 iterations in our function, once for each element, 
// and whatever we return will be placed in a new array in the same index of the element we are iterating.

// ITERATION 1 - The element will be '{ id: 1, name: "Alice", age: 21 }', therefore (user) => { return user.name } , which will be 'Alice'
// ITERATION 2 - The element will be '{ id: 2, name: "Bobby", age: 27 }', therefore (user) => { return user.name } , which will be 'Bobby'

console.log(names); // ["Alice", "Bobby"]
```

## `find`

The `find()` method returns the first element in the array that matches a condition. If no element matches, it returns undefined. Use `find()` when you’re looking for a single specific element in an array based on a condition.

### Example

```js
const users = [ { id: 1, name: "Alice", age: 21 }, { id: 2, name: "Bobby", age: 27 }, { id: 3, name: "Sammy", age: 4 } ];
const userId = 2;
const foundUser = users.find((user) => { return user.id === userId });
// user is whatever name I decided to give to the element I'll receive in the function, can be anything, I gave it user since I know its going to be an object representing a user

// The array 'users' has 3 elements, therefore we will have 3 iterations in our function, once for each element, 
// as soon as one of the iterations returns true, the element of that iteration is assigned your variable and we stop iterating

// ITERATION 1 - The element will be '{ id: 1, name: "Alice", age: 21 }'
// Here, user.id is '1' and userId is 2, hence the comparison returns false, we will go to the next iteration.

// ITERATION 2 - The element will be '{ id: 2, name: "Bobby", age: 27 }'
// Here, user.id is '2' and userId is 2, hence the comparison returns true, the user { id: 2, name: "Bobby", age: 27 } will be the value of 'foundUser'.

// ITERATION 3 - Since we found what we wanted in ITERATION 2, this third iteration is not needed anymore, therefore skipped.

console.log(foundUser); // { id: 2, name: "Bobby", age: 27 }
```

## `filter`

The `filter()` method returns a new array with the elements whose iterations return true as the result of a condition. Use `filter()` when you want have a list but you want a new list with only some of them that meet a specific condition.

### Example #1

```js
const ages = [12, 25, 17, 30];
const adultAges = ages.filter((age) => { return age >= 18 });
// age is whatever name I decided to give to the element I'll receive in the function, can be anything, I gave it age since I know its going to be a number representing an age

// ITERATION 1 - The element will be '12', therefore (12) => { return 12 >= 18 } , which is false, therefore 12 will NOT be part of the new array 'adultAges'
// ITERATION 2 - The element will be '25', therefore (25) => { return 25 >= 18 } , which is true, therefore 25 will be part of the new array 'adultAges'
// ITERATION 3 - The element will be '17', therefore (17) => { return 17 >= 18 } , which is false, therefore 17 will NOT be part of the new array 'adultAges'
// ITERATION 4 - The element will be '30', therefore (30) => { return 30 >= 18 } , which is true, therefore 30 will be part of the new array 'adultAges'

console.log(adultsAges); // [25, 30]
```

### Example #2

```js
const users = [ { id: 1, name: "Alice", age: 21 }, { id: 2, name: "Bobby", age: 27 }, { id: 3, name: "Sammy", age: 4 } ];
const adultUsers = ages.filter((user) => { return user.age >= 18 });
// user is whatever name I decided to give to the element I'll receive in the function, can be anything, I gave it user since I know its going to be an object representing a user

// ITERATION 1 - The element will be { id: 1, name: "Alice", age: 21 }
// Here, user.age is '21' and we check if it's equal or bigger than 18, which is true, therefore 'Alice' user will be part of 'adultUsers'

// ITERATION 2 - The element will be { id: 2, name: "Bobby", age: 27 }
// Here, user.age is '27' and we check if it's equal or bigger than 18, which is true, therefore 'Bobby' user will be part of 'adultUsers'

// ITERATION 3 - The element will be { id: 3, name: "Sammy", age: 4 }
// Here, user.age is '4' and we check if it's equal or bigger than 18, which is false, therefore 'Sammy' user will NOT be part of 'adultUsers'

console.log(adultUsers); // [ { id: 1, name: "Alice", age: 21 }, { id: 2, name: "Bobby", age: 27 } ]
```
