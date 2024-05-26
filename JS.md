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
