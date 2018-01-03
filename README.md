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
var_name = ;
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

#### Other Math Operators

+=
-=
*=
++
--
