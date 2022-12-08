# Regular Expressions

A regular expression or RegExp is a small programming language that helps to find pattern in data. A RegExp can be used to check if some pattern exists in a different data types. To use RegExp in JavaScript either we use RegExp constructor or we can declare a RegExp pattern using two forward slashes followed by a flag.

# RegExp parameters

A regular expression takes two parameters. One required search pattern and an optional flag.

- Pattern : A pattern could be a text or any form of pattern which some sort of similarity.
- Flags : Flags are optional parameters in a regular expression which determine the type of searching.
  - g: a global flag which means looking for a pattern in whole text
  - i: case insensitive flag(it searches for both lowercase and uppercase)
  - m: multiline

# Creating a pattern with RegExp Constructor

Declaring regular expression without global flag and case insensitive flag.

```
// without flag
let pattern = 'anand'
let regEx = new RegExp(pattern)
```

Declaring regular expression with global flag and case insensitive flag.

```
let pattern = 'anand'
let flag = 'gi'
let regEx = new RegExp(pattern, flag)
```

# Creating a pattern without RegExp Constructor

Declaring regular expression with global flag and case insensitive flag.

```
let regEx= /anand/gi
```

# RegExp Object Methods

- **Testing for a match**
  test(): Tests for a match in a string. It returns true or false.

```
const str = 'I love JavaScript'
const pattern = /love/
const result = pattern.test(str)
console.log(result) //true
```

- **Array containing all of the match**
  match():Returns an array containing all of the matches, including capturing groups, or null if no match is found. If we do not use a global flag, match() returns an array containing the pattern, index, input and group.

```
const str = 'I love JavaScript'
const pattern = /love/
const result = str.match(pattern)
console.log(result) //['love', index: 2, input: 'I love JavaScript', groups: undefined]
```

```
const str = 'I love JavaScript'
const pattern = /love/g
const result = str.match(pattern)
console.log(result) //["love"]
```

search(): Tests for a match in a string. It returns the index of the match, or -1 if the search fails.

```
const str = 'I love JavaScript'
const pattern = /love/g
const result = str.search(pattern)
console.log(result) //2
```

- **Replacing a substring**
  replace(): Executes a search for a match in a string, and replaces the matched substring with a replacement substring.

```
const txt = 'Python is the most beautiful language that a human being has ever created.\
I recommend python for a first programming language'

matchReplaced = txt.replace(/Python|python/, 'JavaScript')
console.log(matchReplaced)
//JavaScript is the most beautiful language that a human being has ever created.I recommend python for a first programming language
```

```
const txt = 'Python is the most beautiful language that a human being has ever created.\
I recommend python for a first programming language'

matchReplaced = txt.replace(/Python|python/g, 'JavaScript')
console.log(matchReplaced)
//JavaScript is the most beautiful language that a human being has ever created.I recommend JavaScript for a first programming language
```

```
const txt = 'Python is the most beautiful language that a human being has ever created.\
I recommend python for a first programming language'

matchReplaced = txt.replace(/Python/gi, 'JavaScript')
console.log(matchReplaced) //JavaScript is the most beautiful language that a human being has ever created.I recommend JavaScript for a first programming language

```

```
const txt = '%I a%m te%%a%%che%r% a%n%d %% I l%o%ve te%ach%ing.\
T%he%re i%s n%o%th%ing as m%ore r%ewarding a%s e%duc%at%i%ng a%n%d e%m%p%ow%er%ing \
p%e%o%ple.\
I fo%und te%a%ching m%ore i%n%t%er%%es%ting t%h%an any other %jobs.\
D%o%es thi%s m%ot%iv%a%te %y%o%u to b%e a t%e%a%cher.'

matches = txt.replace(/%/g, '')
console.log(matches) //I am teacher and  I love teaching.There is nothing as more rewarding as educating and empowering people.I found teaching more interesting than any other jobs.Does this motivate you to be a teacher.

```

- []: A set of characters

  - [a-c] means, a or b or c
  - [a-z] means, any letter a to z
  - [A-Z] means, any character A to Z
  - [0-3] means, 0 or 1 or 2 or 3
  - [0-9] means any number 0 to 9
  - [A-Za-z0-9] any character which is a to z, A to Z, 0 to 9

- \: uses to escape special characters
  - \d mean: match where the string contains digits (numbers from 0-9)
  - \D mean: match where the string does not contain digits
- . : any character except new line character(\n)

- ^: starts with

  - r'^substring' eg r'^love', a sentence which starts with a word love
  - r'[^abc] mean not a, not b, not c.

- $: ends with

  - r'substring$' eg r'love$', sentence ends with a word love

- `*`: zero or more times

  - r'[a]\*' means a optional or it can occur many times.

- +: one or more times

  - r'[a]+' means at least once or more times

- ?: zero or one times

  - r'[a]?' means zero times or once

- \b: word bounder, matches with the beginning or ending of a word
- {3}: Exactly 3 characters
- {3,}: At least 3 characters
- {3,8}: 3 to 8 characters
- |: Either or
  - r'apple|banana' mean either of an apple or a banana
- (): Capture and group

![regex](https://user-images.githubusercontent.com/31516195/206526659-b4c33101-ec3a-486b-af9a-348fe8b8f14c.png)

## Let's use example to clarify the above meta characters

Let's use square bracket to include lower and upper case

```
const pattern = '[Aa]pple' // this square bracket means either A or a
const txt = 'Apple and banana are fruits. An old cliche says an apple a day keeps the  doctor way has been replaced by a banana a day keeps the doctor far far away. '
const matches = txt.match(pattern)

console.log(matches) //["Apple", index: 0, input: "Apple and banana are fruits. An old cliche says an apple a day keeps the  doctor way has been replaced by a banana a day keeps the doctor far far away.", groups: undefined]

```

```
const pattern = /[Aa]pple/g // this square bracket means either A or a
const txt = 'Apple and banana are fruits. An old cliche says an apple a day a doctor way has been replaced by a banana a day keeps the doctor far far away. '
const matches = txt.match(pattern)

console.log(matches) //["Apple", "apple"]
```
