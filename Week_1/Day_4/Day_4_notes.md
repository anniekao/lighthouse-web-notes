# Day 4

## Functions 
### Functions as Objects
1. Functions can be stored as variables and passed around.
2. Functions can do everything that other objects do (like having properties assigned to them).

## Callback Functions
Definition:
* A function passed (by reference) into another function (the *receiver* function)
* *Receiver* function accepts behaviour to perform by calling the *callback* function that it now has access to
* *Receiver* function can decide to call the *callback* function at any time, as many times it wants

_Note:_ Functions that take in callbacks and *operate* on other functions are referred to as *Higher Order Functions*.

```
// The second argument/parameter is expected to be a (callback) function
// The second argument/parameter is expected to be a (callback) function
const findWaldo = function(names, found) {
  names.forEach((person, idx) => {
    if (person === "Waldo") {
      found(idx);
    }
  });
};

const actionWhenFound = function(index) {
  console.log(`Found him at index ${index}!`);
};

findWaldo(["Alice", "Bob", "Waldo", "Winston"], actionWhenFound);
```

## Anonymous Functions
Last example as an anonymous function, written inline:
```
findWaldo(["Alice", "Bob", "Waldo", "Winston"], function(index) {
  console.log("Waldo is located at:", index);
});
```
Anonymous functions are often declared  while being passed in as callbacks to other functions because the receiving function that takes in the anonymous function will that parameter a name anyway.

## Arrow Functions
* Do not have this.
* Do not have arguments.
* Can’t be called with new.
* Don't a super

Example:
```
[1,2,3].forEach(num => console.log('num: ', num));
```
Common characteristics: small, inline, single purpose

## .sort()
* sorts elements of an array *in place* and returns the sorted array
* sort order is built on converting elements into strings and comparing their sequences of UTF-16 code values

## Closures
Definition: A function that references bindings from local scopes around it (from _Eloquent JavaScript_)

Example: 
```
function makeIdGenerator() {
  let id = 0;

  // The following is the closure function
  return function() {
    // This inner function accesses and assigns the value of
    // the variable id, which was defined in the parent function
    id += 1;
    return id;
  }
}

// makeIdGenerator returns a function which is assigned to
// the variable nextId
const nextId = makeIdGenerator();

console.log(nextId()); // Logs: 1
console.log(nextId()); // Logs: 2
```

## Helpful Links
[fun fun function video on arrow functions](https://www.youtube.com/watch?v=6sQDTgOqh-I)
[Article on Medium about Arrow Functions](https://medium.com/humans-create-software/arrow-functions-in-javascript-what-why-and-how-fun-fun-function-32-d08e9cd33c)
[Sorting a JS array using sort()](http://www.javascriptkit.com/javatutors/arraysort.shtml)