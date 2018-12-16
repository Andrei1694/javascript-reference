# Javascript Reference
## Usefull Resources
https://nodeschool.io/
https://www.w3schools.com/
## 0. Code Exercises
### 1.0 Javascript Snake
## 2. Functions
### 2.1 Execution Contexts and the Execution Stack

### 2.1 Hoisting
JavaScript only hoists declarations, not initializations. If a variable is declared and initialized after using it, the value will be undefined. For example:
```javascript
  console.log(num); // Returns undefined 
  var num;
  num = 6;
```
```javascript
  console.log(num); // Returns undefined 
  var num;
  num = 6;
```
The below two examples demonstrate the same behavior.
```javascript
    var x = 1; // Initialize x
    console.log(x + " " + y); // '1 undefined'
    var y = 2; // Initialize y

    // The above example is implicitly understood as this: 
    var x; // Declare x
    var y; // Declare y
    // End of the hoisting.

    x = 1; // Initialize x
    console.log(x + " " + y); // '1 undefined'
    y = 2; // Initialize y
```
## 3. Objects

### 3.1 Objects and Proprieties
#### Object create using literal
```javascript
// Object literal
var john = {
    firstName: 'John',
    lastName: 'Smith',
    birthYear: 1990,
    family: ['Jane', 'Mark', 'Bob', 'Emily'],
    job: 'teacher',
    isMarried: false
};

console.log(john.firstName);
console.log(john['lastName']);
var x = 'birthYear';
console.log(john[x]);

john.job = 'designer';
john['isMarried'] = true;
console.log(john);
```

```javascript
// new Object syntax
var jane = new Object();
jane.firstName = 'Jane';
jane.birthYear = 1969;
jane['lastName'] = 'Smith';
console.log(jane);
```

### 3.1 Objects and Methods
#### How To create a Method inside a JavaScript Object
```javascript
var john = {
    firstName: 'John',
    lastName: 'Smith',
    birthYear: 1992,
    family: ['Jane', 'Mark', 'Bob', 'Emily'],
    job: 'teacher',
    isMarried: false,
    calcAge: function() {
        this.age = 2018 - this.birthYear;
    }
};

john.calcAge();
console.log(john);
```
