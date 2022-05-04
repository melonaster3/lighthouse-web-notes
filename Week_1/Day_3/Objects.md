## Objects 

* Contains a key-value pair, each key maps to a value
* Keys are always a string or a symbol
* Unique keys, same key cannot appear more than once
* Key points to value which can be of any type 

``` javascript
const tinyObject = {size : "Tiny"};
```

Objects are like two column tables, key and value. 

* Sci_Fi (Key)  :   Terminator (Value)
* Comedy (Key)  :   극한직업 (Value)

Object values can be any types 

``` javascript
const myObject = {
  a: 6,       // Number
  b: "abc",   // String
  c: true,    // Boolean
  d: null,    // Null
}
```

When accesing the object value through key, if using square brackets, it needs to be a string to access it. 

## Assigning new value to a key 

Use square bracket notations to assign a new value to keys 

```javascript
const mary = { name: "Mary Sue" };
mary["name"] = "Mary Jane";
mary["age"]  = 22;
mary // shows the resulting object with both properties
```

## Objects as Values 

We can nest objects within objects! Key value pair in an object can have a value that is another object.

```javascript
const person = {
  name: "Paul",
  address: {
    street: "310 W 95th",
    city: "New York",
    zipCode: 10027
  }
};

person["address"]["city"]; // => "New York"
```

## Arrays as Values 

We could input arrays as values for certain keys in object. If we use typeof it would give us as objects.

If we use instanceof Object, or Array, it would deem true but false for String. 

## Object Keys
* Keys are always strings
* Key is unique
* Key is associated with exactly ONE value (Another object or array is considered one value)

Key is always string so we can omit the quotations 

If we use Object.keys(), we are able to get an array of keys. 

## Iteration 

We cant iterate over Objects like we do in Arrays! 

We can use for in loops. 

```javascript
var planetMoons = {
  mercury: 0,
  venus: 0,
  earth: 1,
  mars: 2,
  jupiter: 67,
  saturn: 62,
  uranus: 27,
  neptune: 14
};

for (var planet in planetMoons) {
  var numberOfMoons = planetMoons[planet];
  console.log("Planet: " + planet + ", # of Moons: "+ numberOfMoons);
}
```

Limitations: 

Object can sometimes have properties that are different. Additional filtering could be needed 

```javascript
for (var planet in planetMoons) {
  // additional filter for object properties:
  if (planetMoons.hasOwnProperty(planet)) {
    //  ...
  }
}
```
