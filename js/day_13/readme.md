# Object

In JavaScript, an object is a standalone entity, with properties and type. Compare it with a cup, for example. A cup is an object, with properties. A cup has a color, a design, weight, a material it is made of, etc. The same way, JavaScript objects can have properties, which define their characteristics.

# Creating new objects

```js
// empty object
const object = {};
```

```js
// object with 3 properties
const object = {
  foo: "bar",
  age: 42,
  baz: { myProp: 12 },
};
```

```js
// Using a constructor function
function Person(name, age, sex) {
  this.name = name;
  this.age = age;
  this.sex = sex;
}
const rand = new Person("Rand McKinnon", 33, "M");
console.log(rand); //{name: 'Rand McKinnon', age: 33, sex: 'M'}
```

```js
// Using the Object.create() method
// Animal properties and method encapsulation
const Animal = {
  type: "Invertebrates", // Default value of properties
  displayType() {
    // Method which will display type of Animal
    console.log(this.type);
  },
};

// Create new animal type called animal1
const animal = Object.create(Animal);
animal1.displayType(); // Logs: Invertebrates
```

```js
// Accessing properties (accessed by dot(.) notation or bracket([]) notation or Object destructuring)
const object = {
  foo: "bar",
  age: 42,
  baz: { myProp: 12 },
};
object.foo; // "bar"
object["age"]; // 42
object.baz; // {myProp: 12}
object.baz.myProp; //12
const { myProp } = object.baz; //12

//Alias variable for obect key
const { myProp: bazValue } = object.baz; //12
console.log(bazValue); //12
```

### Duplicate property names

When using the same name for your properties, the second property will overwrite the first.

```js
const a = { x: 1, x: 2 };
console.log(a); // {x: 2}
```

## Computed property names

The object initializer syntax also supports computed property names. That allows you to put an expression in brackets [], that will be computed and used as the property name.

```js
const items = ["A", "B", "C"];
const obj = {
  [items]: "Hello",
};
console.log(obj); // A,B,C: "Hello"
console.log(obj["A,B,C"]); // "Hello"
```

## Spread properties

Object literals supports the spread synatx(...). The spread (...) syntax allows an iterable, such as an array/string, to be expanded in places where zero or more arguments (for function calls) or elements (for array literals) are expected.

```js
const obj1 = { foo: "bar", x: 42 };
const obj2 = { foo: "baz", y: 13 };

const clonedObj = { ...obj1 };
// { foo: "bar", x: 42 }

const mergedObj = { ...obj1, ...obj2 };
// { foo: "baz", x: 42, y: 13 }
```
