## Before We Begin

This course is for complete beginners. HTML and CSS are prerquisites

Focus on the programming syntax. We are going to learn the fundamentals

Unlike other videos in the channel, this is a crash course and is longer in length

# What is JavaScript?

JavaScript is a high level (often) just-in-time compiled programming language that conforms to the ECMAScript specification

_high level_ >>> means it is a more a friendlier language to write code with

_just-in-time compiled_ >>> means the code we write is compiled during excution rather than before excution

_ECMAScript specification_ >>> is a standard that Javascript adheres to which ensures the code we write will work across any browser

# We Learn JavaScript

_The first reason_ is that Javascript, alongside HTML and CSS is one of core technologies of the world wide web. pretty much every website you come across uses Javascript to handle interactivity and updates, which is not a problem because web browsers have a dedicated Javascript engine to execute the code on the user's computer

JavaScript can be used to build server side applictions.

JavaScript is also used in mobile app development to create cross platform apps that can run on both iOS and android

JavaScript is also used to create desktop applications

JavaScript is the most popular programming language according to the 2021 Stack Overflow developer survey

In this crash course, we will focus on the JavaScript language syntax and the core concepts

---

# How to run JavaScript code?

- **Browser**
  1. Execute JavaScript is in the browser console.
     This is only suited for short snippets and not when we have to write several lines of code
  1. From Within an HTML File, Just Befor The Closing body Tag Add a Pair Of Script Tags.
     It will run when the html file is loaded in the browser.
  1. Have an External JavaScript linked to the html file.
     The option of using an external script tag in the html file is the most suited way to run JavaScript.
- **Node.js runtime**

Using VS Code' terminal to write node commands >> start with the keyword _node_

# Variables:

---

Variables are used to store information.

The information can be cost of an item, the name of the user or any data that might be needed in the code

**Two Recomended Ways To Declare Variables:**

Using the **let** and **const** keywords

---

We use the **let** keyword follwoed by the name of the variable

**All const declerations** must be initialized and once initialized you cannot reassign a new value.

A good rule of thumb is to always use **const** declerations, unless the variable value is going to change in which case you can make use of **let**.

( القاعدة الأساسية الجيدة هي استخدام تصريحات _const_ دائمًا ما لم تتغير قيمة المتغير وفي هذه الحالة يمكنك الاستفادة من _Let_ )

# Data Types

JavaScript is dynamically typed language:

- which means you do not have to specify the data type of a variable when you declare it.

- which also means the data types are automatically converted as needed during execution.

```js
// automatically converted as needed during execution
let a = 10;
a = "Afrah";
a = true;

console.log(a); // display last  assigned value >> true
```

**In JavaScript Data Types Can Be Categorized Into:**

- Primitive Types ( There are 7 primitive types )

  - **String type**

    - Is a sequence of characters that represent a text value.
    - Surrounded by quotes ' ', double quotes " ", or even backticks ``.
    - Ex:

    ```js
    const namee = "Afrah";
    const language = "JavaScript";
    const gender = `Female`;
    ```

  - **Number type**

    - Represents _integer_ and _floating_ point numbers.
    - Ex:

    ```js
    // Integer
    const total = 0;

    // Float
    const PI = 3.14;
    ```

  - **Boolean type**

    - Represents logical entities
    - Can only have one of two values _true_ or _false_
    - Are often used to run code conditionally based on the value being _true_ or _false_
      ( تُستخدم غالبًا لتشغيل التعليمات البرمجية بشكل مشروط استنادًا إلى القيمة _true_ أو _false_ ).
    - Ex:

    ```js
    const isPrimaryNumber = true;
    const isNewUser = false;
    ```

  - **Undefined type**

    - Represents value that is not assigned.
    - If a variable is declared but the value is not assigned, then the value of that variable will be undefined
    - You can also set a value of undefined explicitly
      ( يمكن أيضًا تعيين قيمة غير محددة بشكل صريح )
    - Is used to denote a value that is not yet defined.
    - Ex:

    ```js
    let result;

    // set a value of undefined explicitly
    const res = undefined;

    // Recommended that if you want to explicitly assign a value not known do not use undefined but instead use null
    const res = null;
    ```

  - **Null type**

    - Is a special value that represents empty or unknown value in JavaScript.
    - Is used to denote a null value.
    - Ex:

    ```js
    const data = null;
    ```

  - **BigInt type**

    - Is a very recent addition.
    - Is used to denote an integer value larger than what the number data type can hold.

  - **Symbol type**
    - Is data type introduced in 2015
    - Is used to denote a vlue that is unique and unchangeable.

> **Note:** A primitive value is written as an actual value.

---

- Non-primitive Types ( There are 1 non-primitive type )

  Non-primitive Type is a collection of values.

  - Objects

    - In JavaScript an object is a complex data type.
    - Containes properties defined as key-value pairs.
    - The property also called as key, can only be strings or of the symbol data type.
    - The value on the other hand can be any data type.
    - The following syntax is known as object literal, and is one way to store a collection of data:

    ```js
    // Object literal
    const person = {
      firstName: "Afrah",
      lastName: "Al-Mahdi",
      age: 22,
    };

    // You can use the dot notation to access a property in this object
    console.log(person.firstName);
    ```

---

## **Array Type:**

- Arrays are written with square brackets [ ] and the items in an array are separated by commas.

- Multiple values are stored in one collection variable called _variableName_.

- Can be accessed based on the position

- Ex:

```js
// Array syntax
const oddNumbers = [1, 3, 5, 7, 9];

// To access a value in an array we use the position of the item
console.log(oddNumbers[0]);
```

# Operators

In JavaScript an operator is a special symbol used to perform operations on values and variables.

- Assignment Operators

  Are used to assign values to variables.

  Ex:

  ```js
  let x = 10;
  ```

- Arithmetic Operators

  Are used to perform arithmetic calculations.

  (+, -, \*, /, %)

  (Plus, Minus, Multiplay, Divided, Modulus, Increment, Decrement)

  Ex:

  ```js
  let x = 7,
    y = 5;
  console.log(++x); // Increments x by 1
  console.log(--y); // Decrements y by 1
  ```

- Comparison Operators

  Compare two values and return a boolean value either true or false, which checks if x and y are equal.

  Are primarily used in loops and branching statements (if)

  Ex:

  ```js
  console.log(x == y); // Equal ... Will return false

  console.log(x != y); // Not Equal ... Will return true

  // Compares not just the value but also the data type
  console.log(x === y);

  console.log(x > y); // Greater than Or Less than <

  console.log(x >= y); // Greater than and equal Or <=
  ```

- Logical Operators

  Perform logical operations and return either true or false.

  They are very helpful when combining comparison operators results to make a decision.

  (&&, ||, !)

  (And, Or, Not)

  Ex:

  ```js
  let x = 10;
  let y = 5;

  const isValidNumber = x > 8 && 8 > y;
  console.log(isValidNumber); // Return true

  const isValid = false;
  console.log(!isValid); // Return true
  ```

- String Operators

  The _plus_ operator performs concatenation when used with strings

  Ex:

  ```js
  console.log("Afrah " + "Al-Mahdi");
  ```

- Other Operators

  - **Ternary Operator** it returns a value based on the codition.

  Is used quite often.

  Ex:

  ```js
  const isEven = 10 % 2 === 0 ? "Number Is Even" : "Number Is Odd";
  console.log(isEven);
  ```

# Type Conversions

### Implicit Conversion

also known as type coercion where JavaScript itself will automatically convert the type, to be able to run the code you've written

Ex:

```js
// The + operand will converted into a string
console.log(2 + "3"); //Return >> 23

// Using -, /, % oprend the numeric string is automatically converted into a number
console.log(2 - "3"); // Return >> -1

console.log("Afrah" - "Al-Mahdi"); // NaN >>> Not A Number
```

### Explicit Conversion

where you manually convert the type

To convert a string or boolean to numeric types you can use:

**Number global method** >>> To convert other data types to number

Ex:

```js
console.log(Number("5")); // Return 5
console.log(Number(true)); // Return 1
console.log(Number("")); // Return 0
console.log(parseInt("5")); // Return 5
console.log(parseInt("3.14")); // Return 3
console.log(parseFloat("3.14")); // Return 3.14
```

**String global method** >>> To convert other data types to string

Ex:

```js
console.log(String(500)); // Return 500 as string
console.log(String(true)); // Return true
console.log(String(null)); // Return null
console.log(String(undefined)); // Return undefined

// Alternative Of String Method and it will not work with null and undefined
console.log((500).toString()); // Return 500
console.log(true.toString()); // Return true
```

**Global boolean method** >>> To convert other data types to boolean

Worth noting that [ null, undefined, 0, ' ', NaN ] all return false when converted to boolean, everything else will return true.

```js
// All these return false
console.log(Boolean(null)); // Return false
console.log(Boolean(undefined)); // Return false
console.log(Boolean(0)); // Return false
console.log(Boolean("")); // Return false
console.log(Boolean(NaN)); // Return false

// Will return true
console.log(Boolean(10)); // Return true
console.log(Boolean("   ")); // Return true
```

# Equality

Have Two Types:

- Double Equals

  == (Allows coercion)

  JavaScript coerces the valuse to the same type (converted type automatically and then compared)

  ```js
  const var1 = 10;
  const var2 = "10";
  console.log(var1 == var2); // Return true
  ```

- Triple Equals

  === (Does not allow coercion)

  is more strict and ensures both constants must be of the same types, and will not convert implicitly.

  use triple equals to check equality

```js
const var1 = 10;
const var2 = "10";
console.log(var1 === var2); // Return false
```

> All the valuse we have just seen are treeted as faulty values in JavaScript, and double equals we'll treat them as equals.

# Conditional Statements

Conditional statements are used to perform different actions based on different conditions

- if
- else
- else if
- switch

> break >> this will prevent the next case from being executed.

# Looping Code

Loops used to repeat a block of code

1. **For loop**

   - Syntax:

     ```js
     for (initializer; condition, final-expression) {
         // code to run
     }

     // Example:
     for(let i=1; i<=5; i++) {
         console.log('Welcome JavaScript ' + i);
     }
     ```

     **initializer** >> is run before starting the loop.

     **condition** >> is checked to see if the loop should stop.

     **final-expression** >> is run each time the loop has gone through an iteration.

   ***

1. **While loop**

   - Syntax:

     ```js
     initializer;
     while (condition) {
       // code to run

       final - expression;
     }

     // Example:
     let j = 1;
     while (j <= 5) {
       console.log("Welocme JavaScript " + j);

       j++;
     }
     ```

   ***

1. **Do..while loop**

   - It is always executed at least once, because the condition comes after the code inside the loop.

   - Syntax:

     ```js
     initializer;
     do {
       // code to run

       final - expression;
     } while (condition);

     // Example:
     let i = 1;
     do {
       console.log("Welocme JavaScript " + i);

       i++;
     } while (i <= 5);
     ```

   ***

1. **For..of loop**

   - Syntax:

     ```js
     for (const item of  array)
        // code to run
     ```

   - It is best suited for a collection of data as it abstracts away two things:

     - **First:**

       You don't have to keep track of a variable to increment the iteration count.

     - **Second:**

       You don't have to figure out how to access the item in the collection

   - You just have to worry about the code that needs to be run.

---

# Functions
A JavsScript function is a block of code designed to perform a particular task.

Ex: Add two numbers, multiply two numbers etc.

Functions are reusable as they can be defined once and can be called with different values resulting in different results.

Functions help divide a complex problem into smaller chunks and makes your program easy to understand and maintain.

Passing different arguments to produce different results

It also helps organize code into smaller maintainable code blocks

Syntax:
```js
function name(parameter1, parameter2, parameter3) {
    // code to be executed
}
// username >> Called function parameter

// Examples:
function greet(username) {
    console.log('Welcome ' + username);
}

greet('Afrah') // Afrah >> Called function argument

//------------------------------------------------------

function add(num1, num2) {
    return num1 + num2
}

const sum = add(8, 8)

console.log(sum);
```

**Arrow Function**

With arrow functions we do have a more concise syntax.

Ex:
```js
const arrowSum = (a, b) => {
    return a + b
}

const sum = arrowSum(8, 8)

console.log(sum);

// => : Called fat arrow
```

If you just have one statement that is returned, you can omit the curly braces and the return keyword.

Ex:
```js
const arrowSum = (num1, num2) => num1 + num2

const sum = arrowSum(8, 8)

console.log(sum);
```

If you just have one argument, you can if you want to omit the parantheses around the argument.

Ex:
```js
const arrowSum = num => num

const sum = arrowSum(8)

console.log(sum);
```