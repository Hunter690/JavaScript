# JavaScript
Learning to build and design website

## General Notes

syntax with semicolon on ends of lines

### Introduction

console.log() prints material
"" or '' creates a string
4 data types:
1. String
2. Number
3. Boolean
4. Null
5. undefined

### Built-in Methods

[List of JavaScript Methods](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/prototype)  
[List of Math Methods](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math)  
[List of Number Methods](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)  
```javascript
.length 
.toUpperCase()
.startsWith(letter) #produces boolean
// single line comment
/*
multiline comment
*/
const var_name = ; //const stands for constant and creates a variable with a value that cannot change
//camelCasing is when each new word begins with a capitalized letter
let var_name = ;
var_name = ; //resets the variable to another value
//let var allows for the value that var_name has to be changed
//if a let var is not set to a value, it becomes undefined
let var_name;
console.log(var_name);
//string interpolation allows to print variables
const favoriteAnimal = 'human';
console.log('My favorite animal' + favoriteAnimal);
//another form of string interpolation known as ES6
const myName = 'Hunter';
const myCity = 'NYC';
console.log(`My name is ${myName}. My favorite city is ${myCity}.`);
+=
-=
*=
++
--
=== //equavilent
! //changes truthy to falsy 
<
>
<=
>=
!==
&&
||

typeof //tells what data type a variable is
```


### Control Flow

```javascript
if (condition_name) {
  block
} else {
  block
}

//can use a variable condition that has a string bc every variable has a truthy or falsy value
let variableOne = 'I Exist!';
if (variableOne) {
// This code will run because variableOne contains a truthy value.
} else {
// This code will not run because the first block ran.
}

switch //like an if/else statement without all of the syntax
let groceryItem = 'papaya';

switch (groceryItem) {
  case 'tomato':
    console.log('Tomatoes are $0.49');
    break;
  case 'lime':
    console.log('Limes are $1.49');
    break;
  case 'papaya':
    console.log('Papayas are $1.29');
    break;
  default:
    console.log('Invalid item');
    break;
}

//Ternary operator is another replacement for if/else

isNightTime ? 
console.log('Turn on the lights!') : 
console.log('Turn off the lights!');
```
### Functions

```javascript
//Function expression is used to declare a function
() => //arrow function syntax that indicates a variable will store a function
let calculatorIsOn = false;

const pressPowerButton = () => { //put parameters in ()
  if (calculatorIsOn) {
    console.log('Calculator turning off.');
    calculatorIsOn = false;
  } else {
    console.log('Calculator turning on.');
    calculatorIsOn = true;
  }
};

pressPowerButton();
// Output: Calculator turning on.

pressPowerButton();
// Output: Calculator turning off.

//function declaration can also create a function just with different syntax
function square (number) {
  return number * number; 
}

console.log(square(5));
// Output: 25.
```

### Loops

`for` loop syntax:

```javascript
for (start_condition; stop_condition; incrementation_value) {
}
```

`while` loop syntax:

```javascript
while (condition) {
  // code block that loops until condition is false
}
```

### Arrays

`let array_name = [thing_one, thing_two, thing_n]; //creates an array with thing_one through thing_n;`  
`array_name[index] = new_value;`  
`.push()` adds items to the end of an array  
`.pop()` removes the last item of an array  
`.shift()` removes the first item of an array  
`.unshift()` adds element(s) to the beginning of an array  
`.slice(init_index, final_index)` creates a new array with the items from in between the index  
`.forEach()` executes the same code on each element of an array  
Ex.

```javascript
let groceries = ['whole wheat flour', 'brown sugar', 'salt', 'cranberries', 'walnuts']; 

groceries.forEach(function(groceryItem) {
  console.log(' - ' + groceryItem);
});
//OR
groceries.forEach(groceryItem => console.log(' - ' + groceryItem));

.map() //iterates through array and allows programmer to change elements  
//Ex. 
let numbers = [1, 2, 3, 4, 5]; 

let bigNumbers = numbers.map(function(number) {
  return number * 10;
});
//OR
let bigNumbers = numbers.map(numbers => numbers * 10);

.filter() //returns a new array with indexes that meet a condition
//Ex. 
let words = ['chair', 'music', 'pillow', 'brick', 'pen', 'door']; 

let shortWords = words.filter(function(word) {
  return word.length < 6;
});
//OR
let shortWords = words.filter(word => word.length < 6);

.some(condition) //returns true if condition is met atleast once
.every() //returns true if each index meets the condition
```

### Objects

- Objects are dictionaries, they store values using a key
Ex.
```javascript
let restaurant = {
  name: 'Italian Bistro',
  seatingCapacity: 120,
  hasDineInSpecial: true,
  entrees: ['Penne alla Bolognese', 'Chicken Cacciatore', 'Linguine Pesto']
};
//access a key by taking the variable_name.key_name or variable_name['key_name']
//add or replace a key in an object: variable_name.new_key_name = value
//a function in a key is known as a method
//Ex.
const restaurant = {
  name: 'Italian Bistro',
  seatingCapacity: 120,
  hasDineInSpecial: true,
  entrees: ['Penne alla Bolognese', 'Chicken Cacciatore', 'Linguine pesto'],
  openRestaurant: () => {
    return 'Unlock the door, flip the open sign. We are open for business!';
  },
};
//OR
const restaurant = {
  name: 'Italian Bistro',
  seatingCapacity: 120,
  hasDineInSpecial: true,
  entrees: ['Penne alla Bolognese', 'Chicken Cacciatore', 'Linguine pesto'],

  openRestaurant() {
    return 'Unlock the door, flip the open sign. We are open for business!';
  },
};
//if a method inside of a dictionary needs to access a key in that dictionary, use this as a keyword
//Ex.
this.key_name
//whenever calling a method, use brackets
```

#### Getter and Setter

- Setters are used to make sure that when a key is changed, the same datatype is entered  
- An underscore is used to indicate that a key is not supposed to be modified by code directly  
Ex. 
```javascript
  set key_name(new_key_value) {
  
},
//note the comma because still in object
//in order to call the setter, just reset the key to a new value and the setter automatically runs
//getter just extracts the value associated with a key and, therefore, does not need any perameters
get set key_name() {
  
},
//notice that get does not have any parameters
```

### Class
- Class like an object, but always has the constructor method
```javascript
class ClassName {

}
//when calling an instance of a class, let var_name = new ClassName(parameters);
//use getters and setters in classes as well
set key_name(new_key_value) {
  
}
get set key_name() {
  
}
//notice the lack of commas
```

#### Class Inheritance

- If there a multiple classes that use the have the same properties and methods, you can create
a parent class and then create subclasses

```javascript
class subclass_name extends parent_class_name {
  constructor(parameter_one...) {
    super(name);
  }
}
//extends makes the methods of the parent class available in the subclass
//super calls the constructor form the parent class
//always put the constructor method first

