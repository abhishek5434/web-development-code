# Intro
Setting --> JS --> Content setting --> switch it off
JavaScript earlier known as LiveScript --> Jscript(Microsoft) --> European created ECMA to standardize the language. That is why it is called ECMAScript.
This is why it is written as ES

## How we can practice JS in the web browser
Go to inspect --> Sources --> Arrow to the left --> Snippets --> go to index.js
![image](https://github.com/abhishek5434/web-development-code/assets/86175919/39eb1d3b-c326-458b-8e4e-d5bfd1673e3a)

Helpful Doc: https://developer.mozilla.org/en-US/docs/Web/JavaScript

# Data Types
String: "Hello"
Numbers: 123
Boolean: false/true

typeof function can help show the data type of the value. Ex: `typeof('Abhishek')` `Result: Abhishek`

# Defining Variable

```JS
var myname= 'Abhishek'
alert(myname)
typeof(myname)
```
Overview of the JS environment:
<kbd>
  <img src="https://github.com/abhishek5434/web-development-code/assets/86175919/0a2ae98e-0212-4df1-badf-126962c9d1d4">
</kbd>

**NOTE:**
you can delete the console using `Window + L` but it doesn't remove the defined variable. To delete the variables you need to do hard reload the browser by holding the reload button:

<kbd>
  <img src="https://github.com/abhishek5434/web-development-code/assets/86175919/360d701b-b674-453c-8526-1837dcfa74fa">
</kbd>


# Naming convention of variable
- Variable can't be started with number
- Always advised to use meaningful name
- We can't use reserved word in the variable but variable can contain reserved word. eg `var var=10` is not correct but `var myvar = 10` is correct!
- Advised to use camelCase where first letter starts with lowercase and all the subsequent word starts with Uppercase

# String
- We can concatenate with strings.Eg: `"Hello" + " World"`
- word.length can be used to know the length
```Js
var myname= 'Abhishek'
myname.length; //8
```
**Challenge: Character counter**
```JS
var mytweet= prompt('Please write your tweet: ')
alert("You have written "+ mytweet.length + "characters, you have "+ (200- mytweet.length)+ " characters left");
//This is single line comment
/* This is
multiline comment
*/
```
**Slicing of string:**
Works same as other programming language like python.
```JS
var myTweet= prompt('Please write your tweet: ')
var slicedTweet= mytweet.slice(0,140)
alert(slicedTweet);
```
**UpperCase/LowerCase**
```JS
// Challenge: Ask the name of the user, Convert first letter in lower case and other letter in upper case

var nameOfUser = prompt("Please provide your name: ")
var firstLetter = nameOfUser.slice(0,1)
var capitalFirstLetter = firstLetter.toUpperCase()
alert(capitalFirstLetter+nameOfUser.slice(1,nameOfUser.length).toLowerCase())
```
# Function in JS
Sure, here are comprehensive notes on functions in JavaScript:

### Functions in JavaScript

Functions are fundamental building blocks in JavaScript. They are reusable blocks of code designed to perform a particular task, executed when invoked.

#### 1. **Function Declaration**

A function declaration defines a function with the specified parameters.

```javascript
function functionName(parameters) {
  // code to be executed
}
```

**Example:**

```javascript
function greet(name) {
  console.log('Hello, ' + name);
}

greet('Alice');  // Output: Hello, Alice
```

#### 2. **Function Expression**

A function expression defines a function as part of a larger expression syntax (typically a variable assignment).

```javascript
const functionName = function(parameters) {
  // code to be executed
};
```

**Example:**

```javascript
const greet = function(name) {
  console.log('Hello, ' + name);
};

greet('Bob');  // Output: Hello, Bob
```

#### 3. **Anonymous Functions**

Anonymous functions are functions without a name. They are typically used as arguments to other functions.

**Example:**

```javascript
setTimeout(function() {
  console.log('This runs after 2 seconds');
}, 2000);
```

#### 4. **Immediately Invoked Function Expressions (IIFE)**

An IIFE is a function that runs as soon as it is defined.

```javascript
(function() {
  // code to be executed
})();
```

**Example:**

```javascript
(function() {
  console.log('IIFE executed');
})();
```

#### 5. **Parameters and Arguments**

- **Parameters** are the names listed in the function definition.
- **Arguments** are the values passed to the function when it is invoked.

**Example:**

```javascript
function add(a, b) {
  return a + b;
}

console.log(add(5, 3));  // Output: 8
```

#### 6. **Default Parameters**

Default parameters allow named parameters to be initialized with default values if no value or `undefined` is passed.

**Example:**

```javascript
function greet(name = 'Guest') {
  console.log('Hello, ' + name);
}

greet();  // Output: Hello, Guest
```

#### 7. **Rest Parameters**

Rest parameters allow a function to accept an indefinite number of arguments as an array.

**Example:**

```javascript
function sum(...numbers) {
  return numbers.reduce((total, num) => total + num, 0);
}

console.log(sum(1, 2, 3));  // Output: 6
```
# Arithmetic Operators
JavaScript provides several arithmetic operators that you can use to perform basic mathematical operations. Here are all the arithmetic operators in JavaScript:

### 1. Addition (`+`)

Adds two numbers.

**Syntax:**
```javascript
let result = a + b;
```

**Example:**
```javascript
let sum = 5 + 3;  // Output: 8
```

### 2. Subtraction (`-`)

Subtracts the second number from the first.

**Syntax:**
```javascript
let result = a - b;
```

**Example:**
```javascript
let difference = 5 - 3;  // Output: 2
```

### 3. Multiplication (`*`)

Multiplies two numbers.

**Syntax:**
```javascript
let result = a * b;
```

**Example:**
```javascript
let product = 5 * 3;  // Output: 15
```

### 4. Division (`/`)

Divides the first number by the second.

**Syntax:**
```javascript
let result = a / b;
```

**Example:**
```javascript
let quotient = 15 / 3;  // Output: 5
```

### 5. Modulus (`%`)

Returns the remainder of dividing the first number by the second.

**Syntax:**
```javascript
let result = a % b;
```

**Example:**
```javascript
let remainder = 5 % 2;  // Output: 1
```

### 6. Exponentiation (`**`)

Raises the first number to the power of the second number.

**Syntax:**
```javascript
let result = a ** b;
```

**Example:**
```javascript
let power = 2 ** 3;  // Output: 8
```

### 7. Increment (`++`)

Increases a number by one. Can be used as a prefix or postfix.

**Syntax:**
```javascript
let result = ++a;  // Prefix
let result = a++;  // Postfix
```

**Example:**
```javascript
let a = 5;
let prefixIncrement = ++a;  // Output: 6 (a is now 6)
let postfixIncrement = a++; // Output: 6 (a is now 7 after this statement)
```

### 8. Decrement (`--`)

Decreases a number by one. Can be used as a prefix or postfix.

**Syntax:**
```javascript
let result = --a;  // Prefix
let result = a--;  // Postfix
```

**Example:**
```javascript
let a = 5;
let prefixDecrement = --a;  // Output: 4 (a is now 4)
let postfixDecrement = a--; // Output: 4 (a is now 3 after this statement)
```

### Summary of Arithmetic Operators

| Operator  | Name          | Description                                       | Example               | Result |
|-----------|---------------|---------------------------------------------------|-----------------------|--------|
| `+`       | Addition      | Adds two numbers                                  | `5 + 3`               | `8`    |
| `-`       | Subtraction   | Subtracts the second number from the first        | `5 - 3`               | `2`    |
| `*`       | Multiplication| Multiplies two numbers                            | `5 * 3`               | `15`   |
| `/`       | Division      | Divides the first number by the second            | `15 / 3`              | `5`    |
| `%`       | Modulus       | Returns the remainder of dividing the first by the second | `5 % 2` | `1`    |
| `**`      | Exponentiation| Raises the first number to the power of the second| `2 ** 3`              | `8`    |
| `++`      | Increment     | Increases a number by one                         | `let a = 5; a++`      | `6`    |
| `--`      | Decrement     | Decreases a number by one                         | `let a = 5; a--`      | `4`    |

These arithmetic operators are fundamental to performing calculations and manipulating numerical values in JavaScript.
