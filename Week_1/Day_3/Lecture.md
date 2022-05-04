# Lecture Notes 

Types of primitive 

```js
const str = 'string';
const num = 42;
const bool = true
const undef = undefined;
const null = null;
const sym = Symbol('symbol');
const bigInt = 42n;
```

* Primitives are stored directly in memory 
* They are immutable. Cant be changed after they are set. 

## Data Structures 
Primitives 

```js
const arr = [];
const obj = {};
```

Objects are collection of key/value pairs
Hash, dictionary, associative array 


```js
const studentOne = {
  username: "Alice"
};

console.log(studentOne);
```

We can use either 
```js
const username = studentOne.username;
const username = studentOne['username'];
```

If we know name of the key, use dot notation! 
If key is unknown, (In a variable), use square bracket notation!

```js
const key = 'username';
studentOne.key // -> aient gon work! 
studentOne['username'];
```

## New Example

```js
const puppy = {};

//color 
puppy.color = "brown";

//cuteness 
puppy['cuteness'] = true; 

// color a key that already exists
puppy.color = "black";
```
Everything in JS that isnt primitive is an object. 

We could put an object inside an array. 
and we can do puppies.push(puppy)
or do puppies[0].color


Objects = describes a particular thing ('user', 'puppy')
Array = Collections of things ('users','puppies')


When we pass a value in to a function, we get a copy of the value in the function, not the actual value. 

When we pass an object into a function, the object DOES CHANGE. Passed by reference! (Geting the OG thing) When we get the new copy, both gets passed in and change. Arrays are also passed by reference! So passing in an array and objct into a function will change it! If we want the original one to stay, we create a copy value and insert it in! 

Primitives are passed by value, we get a copy! 
Objects/Arrays are passed by reference means we get the original! 

Functions are objects, so name could be key, what happens is value 

Inside an object, a function could be a value! 


## THIS

Interact with this for whatever you want to interat with in the object. If we want to reference something in object, use this.

This goes to the nearest object


## Looping in Object

We can use for..of or for..in

```js
const dogs = ['Henri', 'Lola', 'Dioji'];

for (const dog of dogs) {
  console.log(dog);
}
// for of loops will give each elements 


for (const in dogs) {
  console.log(index); // < This will give index the numbers
  console.log(`${dogs[index]} is a good dog!`); 
};

```

Objects cannot be iterated like arrays. We cant use for of loops for objects! 

We should use for in for objects! 


```js
for (const key in user) {
  console.log(key); // get key
  console.log(user[key]); // get value
}
```

Object.keys() = Get all keys in to an array 
so we can use

```js
for (const key of Object.eys(user)) {
  
}
```