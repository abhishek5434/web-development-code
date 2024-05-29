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

# Overview of the JS environment:
<kbd>
  <img src="https://github.com/abhishek5434/web-development-code/assets/86175919/0a2ae98e-0212-4df1-badf-126962c9d1d4">
</kbd>

**NOTE:**
you can delete the console using `Window + L` but it doesn't remove the defined variable. To delete the variables you need to do hard reload the browser by holding the reload button:

<kbd>
  <img src="https://github.com/abhishek5434/web-development-code/assets/86175919/360d701b-b674-453c-8526-1837dcfa74fa">
</kbd>

# Declaring Variable
In JavaScript, there are three main ways to declare variables: using `var`, `let`, and `const`. Each has its own characteristics and scope rules. Here's a detailed explanation of each:

### 1. `var`
- **Scope**: `var` is function-scoped, meaning it is only accessible within the function it is declared in. If declared outside of a function, it becomes globally scoped.
- **Hoisting**: `var` declarations are hoisted to the top of their scope. This means the variable can be used before its declaration, but it will be `undefined`.
- **Re-declaration**: Variables declared with `var` can be re-declared within the same scope.

```javascript
function example() {
    console.log(a); // Output: undefined (due to hoisting)
    var a = 10;
    console.log(a); // Output: 10
}

var b = 20;
var b = 30; // Re-declaration is allowed
console.log(b); // Output: 30
```

### 2. `let`
- **Scope**: `let` is block-scoped, meaning it is only accessible within the block (enclosed by `{}`) it is declared in.
- **Hoisting**: `let` declarations are hoisted but not initialized. Accessing the variable before declaration results in a `ReferenceError`.
- **Re-declaration**: Variables declared with `let` cannot be re-declared within the same scope.

```javascript
function example() {
    // console.log(a); // ReferenceError: Cannot access 'a' before initialization
    let a = 10;
    console.log(a); // Output: 10
}

let b = 20;
// let b = 30; // SyntaxError: Identifier 'b' has already been declared
console.log(b); // Output: 20
```

### 3. `const`
- **Scope**: `const` is block-scoped, similar to `let`.
- **Hoisting**: `const` declarations are hoisted but not initialized. Accessing the variable before declaration results in a `ReferenceError`.
- **Re-declaration**: Variables declared with `const` cannot be re-declared within the same scope.
- **Immutability**: The value of a `const` variable cannot be changed through reassignment. However, if the variable is an object or an array, its properties or elements can be modified.

```javascript
function example() {
    // console.log(a); // ReferenceError: Cannot access 'a' before initialization
    const a = 10;
    console.log(a); // Output: 10
    // a = 20; // TypeError: Assignment to constant variable.
}

const b = 20;
// const b = 30; // SyntaxError: Identifier 'b' has already been declared
console.log(b); // Output: 20

const c = { name: "Alice" };
c.name = "Bob"; // Allowed: Properties of objects can be changed
console.log(c.name); // Output: Bob
```

### Summary of Differences
- **Scope**:
  - `var`: Function-scoped
  - `let` and `const`: Block-scoped
- **Hoisting**:
  - `var`: Hoisted and initialized with `undefined`
  - `let` and `const`: Hoisted but not initialized
- **Re-declaration**:
  - `var`: Can be re-declared
  - `let` and `const`: Cannot be re-declared in the same scope
- **Immutability**:
  - `var` and `let`: Values can be changed
  - `const`: Value cannot be changed through reassignment (except for object properties and array elements)

Understanding these differences is crucial for writing clean, bug-free JavaScript code. Using `let` and `const` is generally preferred in modern JavaScript due to their block scope and safer behavior with hoisting.
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

# Most used Math functions
JavaScript provides a robust `Math` object that includes various functions to perform mathematical operations. Here are some of the most commonly used `Math` functions in JavaScript:

1. **`Math.abs(x)`**: Returns the absolute value of a number.
   ```javascript
   console.log(Math.abs(-5)); // Output: 5
   ```

2. **`Math.ceil(x)`**: Rounds a number upwards to the nearest integer.
   ```javascript
   console.log(Math.ceil(4.2)); // Output: 5
   ```

3. **`Math.floor(x)`**: Rounds a number downwards to the nearest integer.
   ```javascript
   console.log(Math.floor(4.8)); // Output: 4
   ```

4. **`Math.round(x)`**: Rounds a number to the nearest integer.
   ```javascript
   console.log(Math.round(4.5)); // Output: 5
   console.log(Math.round(4.4)); // Output: 4
   ```

5. **`Math.max(...values)`**: Returns the largest of zero or more numbers.
   ```javascript
   console.log(Math.max(1, 2, 3, 4, 5)); // Output: 5
   ```

6. **`Math.min(...values)`**: Returns the smallest of zero or more numbers.
   ```javascript
   console.log(Math.min(1, 2, 3, 4, 5)); // Output: 1
   ```

7. **`Math.random()`**: Returns a pseudo-random number between 0 (inclusive) and 1 (exclusive).
   ```javascript
   console.log(Math.random()); // Output: A random number between 0 and 1
   ```

8. **`Math.sqrt(x)`**: Returns the square root of a number.
   ```javascript
   console.log(Math.sqrt(16)); // Output: 4
   ```

9. **`Math.pow(base, exponent)`**: Returns the base to the exponent power, that is, `base^exponent`.
   ```javascript
   console.log(Math.pow(2, 3)); // Output: 8
   ```

10. **`Math.exp(x)`**: Returns `E^x`, where `E` is Euler's number (approximately 2.718).
    ```javascript
    console.log(Math.exp(1)); // Output: 2.718281828459045
    ```

11. **`Math.log(x)`**: Returns the natural logarithm (base `E`) of a number.
    ```javascript
    console.log(Math.log(10)); // Output: 2.302585092994046
    ```

12. **`Math.sin(x)`**: Returns the sine of a number (angle in radians).
    ```javascript
    console.log(Math.sin(Math.PI / 2)); // Output: 1
    ```

13. **`Math.cos(x)`**: Returns the cosine of a number (angle in radians).
    ```javascript
    console.log(Math.cos(0)); // Output: 1
    ```

14. **`Math.tan(x)`**: Returns the tangent of a number (angle in radians).
    ```javascript
    console.log(Math.tan(Math.PI / 4)); // Output: 1
    ```

These functions cover a wide range of mathematical operations and are frequently used in various programming tasks. For more detailed information, we can refer to the [MDN Web Docs on Math](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math).

# Control Flow
Control flow in JavaScript determines the order in which statements are executed. The flow of control can be altered using various statements such as conditionals, loops, and other control structures. Here are the key elements of control flow in JavaScript:

### 1. Sequential Execution
By default, JavaScript code is executed from top to bottom, line by line.

```javascript
console.log("Start");
console.log("Middle");
console.log("End");
```

### 2. Conditional Statements
Conditional statements allow you to execute code based on certain conditions.

#### `if` statement
Executes a block of code if the specified condition is true.

```javascript
let age = 18;
if (age >= 18) {
    console.log("You are an adult.");
}
```

#### `if...else` statement
Executes one block of code if the condition is true, and another block if the condition is false.

```javascript
let age = 16;
if (age >= 18) {
    console.log("You are an adult.");
} else {
    console.log("You are a minor.");
}
```

#### `if...else if...else` statement
Tests multiple conditions.

```javascript
let score = 85;
if (score >= 90) {
    console.log("Grade: A");
} else if (score >= 80) {
    console.log("Grade: B");
} else if (score >= 70) {
    console.log("Grade: C");
} else {
    console.log("Grade: F");
}
```

#### `switch` statement
Executes one of many blocks of code based on the value of an expression.

```javascript
let day = 3;
switch (day) {
    case 1:
        console.log("Monday");
        break;
    case 2:
        console.log("Tuesday");
        break;
    case 3:
        console.log("Wednesday");
        break;
    default:
        console.log("Another day");
}
```

### 3. Looping Statements
Loops allow you to execute a block of code multiple times.

#### `for` loop
Loops through a block of code a specified number of times.

```javascript
for (let i = 0; i < 5; i++) {
    console.log("Iteration " + i);
}
```

#### `while` loop
Executes a block of code as long as a specified condition is true.

```javascript
let i = 0;
while (i < 5) {
    console.log("Iteration " + i);
    i++;
}
```

#### `do...while` loop
Executes a block of code once, and then repeats the loop as long as the specified condition is true.

```javascript
let i = 0;
do {
    console.log("Iteration " + i);
    i++;
} while (i < 5);
```

### 4. Control Flow Interruptions
These statements alter the normal flow of control.

#### `break` statement
Exits a loop or switch statement prematurely.

```javascript
for (let i = 0; i < 10; i++) {
    if (i === 5) {
        break; // Exit the loop when i is 5
    }
    console.log(i);
}
```

#### `continue` statement
Skips the rest of the code inside the loop for the current iteration and jumps to the next iteration.

```javascript
for (let i = 0; i < 10; i++) {
    if (i % 2 === 0) {
        continue; // Skip the even numbers
    }
    console.log(i);
}
```

#### `return` statement
Exits a function and optionally returns a value.

```javascript
function add(a, b) {
    return a + b;
}
console.log(add(2, 3)); // Output: 5
```

Understanding these control flow elements is crucial for writing efficient and effective JavaScript code. They allow you to control the execution path and perform complex operations based on dynamic conditions.

# Comparators and Equality Operators
In JavaScript, comparators and equality operators are used to compare values. There are several types of these operators, each serving different purposes and having different behaviors. Understanding the distinctions among them is crucial for writing accurate and predictable code.

### Equality Operators
1. **`==` (Loose Equality)**
   - Compares two values for equality, after converting both values to a common type (type coercion).
   - Returns `true` if the values are equal after type conversion.

   ```javascript
   console.log(5 == '5'); // true
   console.log(true == 1); // true
   console.log(null == undefined); // true
   ```

2. **`===` (Strict Equality)**
   - Compares two values for equality without converting their types (no type coercion).
   - Returns `true` only if the values are of the same type and equal.

   ```javascript
   console.log(5 === '5'); // false
   console.log(true === 1); // false
   console.log(null === undefined); // false
   ```

3. **`!=` (Loose Inequality)**
   - Compares two values for inequality, after converting both values to a common type (type coercion).
   - Returns `true` if the values are not equal after type conversion.

   ```javascript
   console.log(5 != '5'); // false
   console.log(true != 1); // false
   console.log(null != undefined); // false
   ```

4. **`!==` (Strict Inequality)**
   - Compares two values for inequality without converting their types (no type coercion).
   - Returns `true` only if the values are not of the same type or not equal.

   ```javascript
   console.log(5 !== '5'); // true
   console.log(true !== 1); // true
   console.log(null !== undefined); // true
   ```

### Relational Comparators
1. **`>` (Greater Than)**
   - Returns `true` if the left operand is greater than the right operand.

   ```javascript
   console.log(5 > 3); // true
   console.log('apple' > 'banana'); // false (lexicographical comparison)
   ```

2. **`<` (Less Than)**
   - Returns `true` if the left operand is less than the right operand.

   ```javascript
   console.log(3 < 5); // true
   console.log('apple' < 'banana'); // true (lexicographical comparison)
   ```

3. **`>=` (Greater Than or Equal To)**
   - Returns `true` if the left operand is greater than or equal to the right operand.

   ```javascript
   console.log(5 >= 3); // true
   console.log(5 >= 5); // true
   ```

4. **`<=` (Less Than or Equal To)**
   - Returns `true` if the left operand is less than or equal to the right operand.

   ```javascript
   console.log(3 <= 5); // true
   console.log(5 <= 5); // true
   ```

### Special Considerations
1. **Type Coercion**
   - Loose equality (`==` and `!=`) operators perform type coercion, which can lead to unexpected results.
   - Example:

     ```javascript
     console.log('' == false); // true (empty string is coerced to false)
     console.log('0' == 0); // true (string '0' is coerced to number 0)
     ```

2. **NaN Comparison**
   - `NaN` is not equal to anything, including itself.

   ```javascript
   console.log(NaN == NaN); // false
   console.log(NaN === NaN); // false
   ```

3. **Object Comparison**
   - Equality operators compare object references, not their values.

   ```javascript
   let obj1 = { key: 'value' };
   let obj2 = { key: 'value' };
   let obj3 = obj1;

   console.log(obj1 == obj2); // false
   console.log(obj1 === obj2); // false
   console.log(obj1 == obj3); // true
   console.log(obj1 === obj3); // true
   ```

### Best Practices
- Use `===` and `!==` for comparisons to avoid issues with type coercion.
- Be cautious with objects and arrays, as they are compared by reference.
- Be aware of special cases like `NaN`, `null`, and `undefined`.


