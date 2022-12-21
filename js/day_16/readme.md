# Classes

Everything in JavScript is an object, with its properties and methods. We create class to create an object. A Class is like an object constructor, or a "blueprint" for creating objects. We instantiate a class to create an object. The class defines attributes and the behavior of the object, while the object, on the other hand, represents the class.

Once we create a class we can create object from it whenever we want. Creating an object from a class is called class instantiation.

# Defining a classes

```
// syntax
class ClassName {
    //  code goes here
}
```

To define a class in JavaScript we need the keyword class , the name of a class in CamelCase and block code(two curly brackets).

# Class Instantiation

Instantiation class means creating an object from a class. We need the keyword new and we call the name of the class after the word new.

```
class Person {
  // code goes here
}
const person = new Person()
console.log(person) //Person {}
```

# Class Constructor

The constructor is a built-in function which allows as to create a blueprint for our object. The constructor function starts with a keyword constructor followed by a parenthesis. Inside the parenthesis we pass the properties of the object as parameter. We use the `this` keyword to attach the constructor parameters with the class.

```
class Person {
  constructor(firstName, lastName) {
    console.log(this) // Check the output from here
    this.firstName = firstName
    this.lastName = lastName
  }
}

const person = new Person()

console.log(person)
```

- once we create a class we can create many object using the class
- we can pass Default values with constructor

```
class Person {
  constructor(
    firstName = 'A',
    lastName = 'B',
    age = 25,
    country = 'I',
    city = 'O'
  ) {
    this.firstName = firstName
    this.lastName = lastName
    this.age = age
    this.country = country
    this.city = city
  }
}

const person1 = new Person() // it will take the default values
const person2 = new Person('P', 'L', 26, 'U', 'G')

console.log(person1)
console.log(person2)
```

# Class methods

The constructor inside a class is a builtin function which allow us to create a blueprint for the object. In a class we can create class methods. Methods are JavaScript functions inside the class. Let us create some class methods.

```
class Person {
  constructor(
    firstName = 'A',
    lastName = 'B',
    age = 25,
    country = 'I',
    city = 'O'
  ) {
    this.firstName = firstName
    this.lastName = lastName
    this.age = age
    this.country = country
    this.city = city
  }
  getFullName() {
    const fullName = this.firstName + ' ' + this.lastName
    return fullName
  }
}

const person1 = new Person() // it will take the default values
const person2 = new Person('P', 'L', 26, 'U', 'G')

console.log(person1.getFullName())
console.log(person2.getFullName())
```

# Properties with initial value & getter

The get method allow us to access value from the object. We write a get method using keyword `get` followed by a function. Instead of accessing properties directly from the object we use getter to get the value.

```
class Person {
  constructor(firstName, lastName, age, country, city) {
    this.firstName = firstName
    this.lastName = lastName
    this.age = age
    this.country = country
    this.city = city
    this.score = 0
    this.skills = []
  }
  getFullName() {
    const fullName = this.firstName + ' ' + this.lastName
    return fullName
  }
  get getScore() {
    return this.score
  }
  get getSkills() {
    return this.skills
  }
}

const person1 = new Person('A', 'B', 25, 'I', 'O')
const person2 = new Person('P', 'L', 28, 'U', 'G')

console.log(person1.getScore) // We do not need parenthesis to call a getter method
console.log(person2.getScore)

console.log(person1.getSkills)
console.log(person2.getSkills)
```

# setter

The setter method allow us to modify the value of certain properties. We write a setter method using keyword `set` followed by a function.
