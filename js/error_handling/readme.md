# Error Handling

When trying to access an undefined variable or call undefined function we ran into runtime error

```
try {
  // code that may throw an error
} catch (err) {
  // code to be executed if an error occurs
} finally {
  // code to be executed regardless of an error occurs or not
}
```

**try** : Wrap suspicious code that may throw an error in try block. the try statement allows us to define a block of code to be tested for errors while it is being executed.

**catch** : Write code to do something in catch block when an error occurs. the catch block can have parameters that will give an information about error. it's used to log an error or display specific messages to the user.

**finally** : Finally block will always be executed regardless of the occurance of an error. this block can be used to complete the remaining task or reset variables that might have changed before error occured in try block.

```
try {
  let lastName = 'Baraik'
  let fullName = firstName + ' ' + lastName
} catch (err) {
  console.log(err) //ReferenceError: firstName is not defined at <anonymous>:13:28
}
```

```
try {
    let lastName = 'Baraik'
    let fullName = firstName + ' ' + lastName
} catch (err) {
    console.error(err); //index.html:28 ReferenceError: firstName is not defined <anonymous>:26:28
} finally {
    console.log('In any case I will be executed') //In any case I will be executed
}
```

```
try {
    let lastName = 'Baraik'
    let fullName = firstName + ' ' + lastName
} catch (err) {
    console.log(err.name); //ReferenceError
    console.log(err.message); //firstName is not defined
    console.error(err); //index.html:28 ReferenceError: firstName is not defined <anonymous>:26:28
} finally {
    console.log('In any case I will be executed') //In any case I will be executed
}
```

The catch block takes a parameter as an object & it has `name` & `message` keys.

**throw** : the throw statement allows us to create a custom error. we can throw a string, number, boolean or an object. use `throw` statement to throw an exception. when you throw an exception, expression specifies the value of the exception. each of the below throws an exception-

```
throw 'Error2' // generates an exception with a string value
throw 42 // generates an exception with the value 42
throw true // generates an exception with the value true
throw new Error('Required') // generates an error object with the message of Required
```

```
const throwErrorExampleFun = () => {
    let message
    let x = prompt('Enter a number: ')
    try {
        if (x == '') throw 'empty'
        if (isNaN(x)) throw 'not a number'
        x = Number(x)
        if (x < 5) throw 'too low'
        if (x > 10) throw 'too high'
    } catch (err) {
        console.error(err)
    }
}
throwErrorExampleFun()
```

# Error Types

- ReferenceError : An illegal reference has occurred. A ReferenceError is thrown if we use a variable that has not been declared.

```
let firstName = 'Anand'
let fullName = firstName + ' ' + lastName
console.log(fullName)
```

- SyntaxError : A syntax error has occurred

```
let square = 2 x 2
console.log(square)
console.log('Hello, world")
```

- TypeError : A type error has occurred

```
let num = 10
console.log(num.toLowerCase())
```
