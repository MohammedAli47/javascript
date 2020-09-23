# Functional Programming :

A style of programming focused on using simple and effective functions that don't make any unnecessary changes to global variables.

## Some Terminology :

### 1- Callback Functions:

Functions that are passed as parameters inside other functions.

Example :

```javascript
let x = [1, 2, 3, 4];
console.log(x.filter(x => x > 2));
// The arrow function is a callback function
```

### 2- First Class Functions :

Functions that can be treated as normal values ( can be assigned to a variable, passed into another functions or returned from another function ).

>All Javascript functions are `First Class Functions`.

### 3- Higher Order Functions :

Functions that take other ones as parameters or return them as a value.

### 4- Lambda Functions ( Anonymous Functions ) :

Functions that are passed through or returned from other ones.

### 5- Mutations ( Side Effects ) :

Changing or altering something in the program using functions. This can be avoided by passing the input or global variables as function arguments or assigning the value of that input into a variable inside the function.