# Day 3

## Notes
### Six types of primitives:
* 1. undefined
* 2. null
* 3. boolean
* 4. string
* 5. number
* 6. symbol (introduced in ES6)

_Anything not in this list is an Object_
These six primitive types, plus objects, make up the seven fundamental types of JS.

### Objects
Generally, objects 
 * contain key-values pairs: each key maps to a value
 * contain keys: always strings (or symbols, less common)
 * have _unique_ keys: same value cannot appear twice in an object
 * Have their keys point to values which can be of any type

#### Create new object
Use: const objName = {}

#### Retrieve values
To retrieve a value within an object, use square-bracket notation, e.g. const firstPerson = person['firstName'];, or alternatively dot notation, e.g. const firstPerson = person.firstName;

Square-bracket notation can be used to assign new values to new or existing keys.


### Create new/change existing values
```
const mary = { name: "Mary Sue" };
mary["name"] = "Mary Jane";
mary["age"]  = 22;
mary // shows the resulting object with both properties
```

### Access object keys
To access an object's keys, use Object.keys(objName) that returns an array of keys.

## Objects and iteration
### For ... in 
```
for (var planet in planetMoons) {
  // additional filter for object properties:
  if (planetMoons.hasOwnProperty(planet)) {
    //  ...
  }
}
```

## Primitives vs. Objects
* Objects: mutable by default, have unique identities and are compared *by reference*, i.e. two objects are only equal if they have the same identity -- it doesn't matter if they have the same content or not
* Variables: hold references to objects
* Primitives: immutable, compared *by value*, don't have individual identities, are not the instance of any object

## Useful methods
* .search() - The search() method searches a string for a specified value, and returns the position of the match. The search value can be string or a regular expression. This method returns -1 if no match is found.

## Useful Links
* [Stack Overflow: How to loop through/enumerate a JS object](https://stackoverflow.com/questions/684672/how-do-i-loop-through-or-enumerate-a-javascript-object)


 
