# Array Exercises

### Exercise #1

```js
// I want a list of all the full names

const users = [
  { first: "Alice", last: "Brown" },
  { first: "Bob", last: "White" },
];

// Your code

console.log(listOfFullNames) 
// ["Alice Brown", "Bob White"]
```

### Exercise #2

```js
// I want a list of booleans, true or false, for each user, depending on whether they are adults or not

const users = [
  { first: "Alice", last: "Brown",  age: 21 },
  { first: "Bob", last: "White", age: 4 },
  { first: "Sandra", last: "Green", age: 17 },
];

// Your code

console.log(listOfAreTheyAdultsOrNot) 
// [ true, false, true]
```

### Exercise #3

```js
// I want a list of the same users, but with increased score by 6

const users = [
  { first: "Alice", last: "Brown",  score: 7 },
  { first: "Bob", last: "White", score: 2 }
];

// Your code

console.log(usersWithIncreasedScore) 
// [ 
//  { first: "Alice", last: "Brown",  score: 13 }, 
//  { first: "Bob", last: "White", score: 8 }
// ]
```

### Exercise #4

```js
// I want to add a new property to each user, “isAdult” with true or false.

const users = [
  { first: "Alice", last: "Brown",  age: 17 },
  { first: "Bob", last: "White", age: 26 }
];

// Your code

console.log(usersWithIncreasedScore) 
// [ 
//  { first: "Alice", last: "Brown"  age: 17 ,  isAdult: true }, 
//  { first: "Bob", last: "White"  age: 26 , isAdult: false }
// ]
```

### Exercise #5

```js
// I want a list of only the users that are adults

const users = [ 
  { first: "Alice", last: "Brown" ,  isAdult: true }, 
  { first: "Bob", last: "White", isAdult: false },  
  { first: “Sandra”, last: “Green”, isAdult: true }
  ]

// Your code

console.log(onlyAdultUsers) 
// [ 
//  { first: "Alice", last: "Brown" ,  isAdult: true },
//  { first: “Sandra”, last: “Green”, isAdult: true }
// ]
```

### Exercise #6

```js
// I want to know the index of Bob in the list of users

const users = [ 
  { first: 'Alice', last: 'Brown', isAdult: true }, 
  { first: 'Bob', last: 'White', isAdult: false }, 
  { first: 'Sandra', last: 'Green', isAdult: true } 
  ]

// Your code

console.log(indexOfBob) 
// 1
```

### Exercise #7

```js
// I want a list of all dad names, additionally I want also a list of all the dad objects

const users = [
  {
    first: 'Alice',
    last: 'Brown',
    parents: {
      mom: {
        name: 'Sara',
        last: 'Jones',
      },
      dad: {
        name: 'Davy',
        last: 'Smith',
      },
    },
  },
  {
    first: 'Bobby',
    last: 'Lee',
    parents: {
      mom: {
        name: 'Elizabeth',
        last: 'Black',
      },
      dad: {
        name: 'John',
        last: 'Brown',
      },
    },
  },
]

// Your code

console.log(namesOfTheDads) 
// [ "Davy", "John" ]

console.log(dadObjects) 
// [{ name : "Davy", "Smith" }, { name : "John", "Brown" } ]
```