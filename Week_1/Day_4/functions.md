# Functions as Objects

* Functions can be stored in variables and passed around 
* Functions can do everything that other objects can do 

## Callback Function

* A function passed into another function
* Reciever function is accepting behavior to perform by calling the callback function
* Reciever can decide to call the callback function at any time as many times as it wants 

```js
const findWaldo = function(names, found) {
  for (let i = 0; i < names.length; i++) {
    let name = names[i];
    if (name === "Waldo") {
      found();   // execute callback
    }
  }
}

const actionWhenFound = function() {
  console.log("Found him!");
}

findWaldo(["Alice", "Bob", "Waldo", "Winston"], actionWhenFound);
```

Function can be treated like an ordinary value and passed in to a function
 
 actionWhenFound is a CALLBACK function