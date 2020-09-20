# What's OOP?

Stands for Object Oriented Programming, which is a style of programming that mimics real life by using `Classes` and `Objects` to store data related to each other. The data can be of any kind and they become the object's `methods`.

For example, If you go to buy a dog, you can find many different types, names and colors of dogs. But, they're still "Class"ified as dogs, right?

That's the same for `Objects` in programming, they can be very similar to each other or have completely different properties, but belong to the same `Class` or constructor.

## Objects in Javascript :

A type of data structures that can hold complex data.

1- **Creating Objects** :

To create an Object, we use curly braces ( `{}` ).

```javascript
const person = {
    name: "Alex",
    age: 27,
    married: true,
    kids: [
        "Amanda",
        "Sam"
    ]
};
```

>As you can see, the object has different types of data like strings, numbers, booleans, arrays, etc...

2- **Accessing Data** :

To access data from Objects, we use `Dot Notation` or `Bracket Notation`.

```javascript
const person = {
    name: "Alex",
    age: 27
};

console.log(person.name); // Alex (Dot Notation)
console.log(person["name"]); // Alex (Bracket Notation)
```

3- **Object methods** :

To make methods, we define normal functions inside Objects.

```javascript
const person = {
    name: "Alex",
    age: 27,
    sayName: function() {
        console.log("Alex");
    }
};
person.sayName();
```

4- **this** keyword :

Used in Javascript OOP, it solves a lot of problems that objects have like changing the properties keys or values.

```javascript
const person = {
    name: "Alex",
    age: 27,
    sayName: function() {
        console.log(this.name);
    }
};
person.sayName();
```

5- **constructor** function :

A function used to make new objects with the same properties in it.

We create new objects with the `new` keyword.

```javascript
function Bird() {
  this.name = "Albert";
  this.color = "blue";
  this.numLegs = 2;
}

let bird1 = new Bird();
```

>### Note :
>All constructors are defined with the first letter capitalized and they define the properties each new object will have.

6- Making constructors more dynamic :

When we create new objects from constructors ( like in the previous example ), they inherit the same properties and values from the constructor.

If we want to make them more dynamic and not have to assign new values each time, we can do something like this :

```javascript
function Bird(name, color) {
  this.name = name;
  this.color = color;
  this.numLegs = 2;
}

let bird1 = new Bird("Albert", "blue");
let bird2 = new Bird("Norman", "red");
let bird3 = new Bird("Shroud", "silver");
```

>We passed arguments that can be changed as we create each new object. Exciting stuff!!

7- To verify that an object belongs to a certain constructor, we use the `instanceof` operator

```javascript
function Bird() { this.name = "Albert"; }

let crow = new Bird();
let canary = { name = "Tom" };

crow instanceof Bird; // true
canary instanceof Bird; // false
```

8- **Own Properties** :

Objects created from a constructor have their own copy of that constructor's properties. These are called **own** properties

>To check for these kinds of properties, we use the `hasOwnProperty()` method.

```javascript
function Bird() { this.name = "Albert"; }

let crow = new Bird();

crow.hasOwnProperty(name); // true
```

9- **Prototype Properties** :

We use these properties to avoid repeating code and to write the shared values among objects.

```javascript
function Bird() {
    this.name = "Albert"; // own property
}
Bird.prototype.legs = 2; // prototype property
let crow = new Bird();

console.log(crow.legs); // 2
```

>### Note :
>Prototype Properties are objects by themselves, so you can assign an entire object to them. ( Go to number 11 for more... )

10- The **constructor** property :

Every object has a constructor property which points to the constructor that made this object

```javascript
function Bird(name, color) {
  this.name = name;
  this.color = color;
  this.numLegs = 2;
}

let crow = new Bird("Albert", "blue");

console.log(crow.constructor === Bird); // true
```

11- The `Object` default constructor :

When we assign an object to prototype properties, we override the original value of the object's constructor and it turns into `Object`

To fix this, we have to assign it in the prototype object to its original value.

```javascript
function Bird() {
  this.name = "Albert";
}

Bird.prototype = {
    legs: 2,
    color: "brown"
}

let crow = new Bird();

crow.constructor === Bird; // returns false :/
crow.constructor === Object; // returns true
crow instanceof Bird; // returns true
```
>### Note:
>The crow object is still an instance of the Bird constructor, but it's not its constructor anymore.

So, we assign the original value of the constructor to it again like this :

```javascript
function Bird() {
  this.name = "Albert";
}

Bird.prototype = {
    constructor: Bird,
    legs: 2,
    color: "brown"
}

let crow = new Bird();
crow.constructor === Bird; // returns true 
```

12- Objects inherit the prototype property of their original constructor :

To check for this, we use the `isPrototypeOf()` method.

```javascript
function Bird() {
    this.name = "Albert";
}

let crow = new Bird();

Bird.prototype.isPrototypeOf(crow) // returns true
```

13- The prototype chain :

From the previous example, we see that **Bird** is the constructor and `supertype` for **crow** and **crow** is a `subtype` for it.

As for the `Object` constructor, it's a supertype for both of them!!

This means that **crow** inherits from **Bird** and **Bird** inherits from Object.

14- We can inherit supertype behaviors by using the `Object.create()` syntax.

```javascript
function Animal() { }
Animal.prototype.eat = function() {
  console.log("nom nom");
};

let animal = Object.create(Animal.prototype);
```