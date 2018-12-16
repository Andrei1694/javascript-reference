# Javascript Reference
## Resurse
https://nodeschool.io/
## 0. Code Exercises
### 1.0 Javascript Snake
## 2. Functions
### 2.1 Hoisting
```javascript
  var a = 3;
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
