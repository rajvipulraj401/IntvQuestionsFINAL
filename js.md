### note1 - **(NEED what and HOW ) bs isi trh bologe tum humesha:------**

Note 2 \*HOW TO deal with question you don't know completely ?
--- Pehle bolo phir ye last me bolo --- ( how to say no to a question)
Ans :- Sir ,This is what i know at the moment and i am not exactly sure if i am explaining it correctly but i would love to get back to this question right after the interview .

note 2.1 ) How to deal when you completely dont know ?
Ans :- Sir currently i am not able to come up with the right answer to this question but i would love to get back to this question right after this interview

# --------- **Javascript** :--------- (----read in fe 102 lect 5 onwards notes ----)

# **(A)** _Basic :--------_

## Q0.0) What are all falsy values in javascript ?

### 🔥 Here's the full list of **all falsy values in JS**:

--There are total 8 kinds of falsy values
There are basically 6 kinds of falsy value in javascript :---0 ka bs teen type hai ek -ve wala ek positive wala ek bs big int wla

| Value       | Type      | Description                                              |
| ----------- | --------- | -------------------------------------------------------- |
| `false`     | Boolean   | Literally false                                          |
| `0`         | Number    | The number zero                                          |
| `-0`        | Number    | Negative zero                                            |
| `0n`        | BigInt    | BigInt representation of zero                            |
| `""`        | String    | Empty string                                             |
| `null`      | Object    | Null value (**Represents intentional absence**)          |
| `undefined` | Undefined | Undefined value (**Variable declared but not assigned**) |
| `NaN`       | Number    | Not-a-Number                                             |

---

### Q0) what is js ?what are different ways you can write js ? what tag we use to define inline js and internal js and external js and what tag we use to link external js file in html ?

## Q0) What is JavaScript?

Ans :--  
(generate the need)

---

### **Need (Why do we need JavaScript?)**

When we build web pages using just HTML and CSS, we can only build **static websites** — like headings, paragraphs, buttons, etc. But if we want to interact with the page — like responding to clicks or fetching data from a server

we cannot do that and in order to do that in our website and make it **interactive and dynamic**, we need to use JavaScript.

---

### **What (What exactly is JavaScript?)**

JavaScript is a **high-level** ( code that's close to normal english and not like low level which is close to machine like C OR C++), **interpreted programming language** (A code which run line by line by something called an interpreter and is not compiled into machine language (thats why usually slower than compiled language but FASTER to debug and test))
`that runs **inside the browser**. It allows us to **create dynamic and interactive web pages**.`

<!-- ye pdho neeche 👇🏼👇🏼👇🏼👇🏼 -->

JavaScript is a **high-level, interpreted programming language** that runs **inside the browser**. It allows us to **create dynamic and interactive web pages**.

Using JS, we can:

- Modify HTML and CSS dynamically
- and Respond to user actions like (clicks, timer, fetching data etc.)

So whatever we want to show when a user does some interaction with our website for that we need javascript .
we can understand this by a real word analogy of a car so the parts of the car are like html and the design and size of parts are css and the engine is Javascript .

---

### **How (How do we use JavaScript in a project?)**

### 📺 Sir can I share my screen to show this with an example

So There are **three main ways** to add JavaScript to an HTML page:

---

1. First we have **Inline JavaScript**  
    In this JS is written directly inside an element using the `onclick` or similar event attributes.

   ```html
   <!DOCTYPE html>
   <html lang="en">
     <head>
       <meta charset="UTF-8" />
       <title>Inline JS Example</title>
     </head>
     <body>
       <h1>Inline JavaScript Demo</h1>
     </body>
   </html>
   ```

  <!-- ✅ Inline JS inside the onclick attribute -->

<button onclick="alert('Bhai, inline JS chal gaya!')">Click Me</button>

</body>
</html>
```

---

2. Then we have the **Internal JavaScript**
   In this We write JavaScript inside a `<script>` tag in the HTML document usually at the bottom of <body>.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <title>Internal JS Example</title>
  </head>
  <body>
    <h1>Welcome, Bhai!</h1>
    <button id="clickBtn">Click Me</button>
  </body>
</html>
```

  <!-- ✅ Internal JS at the end of body -->
  <script>
    <!-- // JavaScript yahan likha gaya hai — DOM ke baad chalega -->

    document.getElementById("clickBtn").addEventListener("click", function () {
      alert("Bhai, button click ho gaya!");
    });
  </script>
</body>
</html>
   ```

---

3. **External JavaScript (Most Recommended)**  
   We write JavaScript in a separate `.js` file and link it using the `<script src="">` tag.

   ```html
   <script type="module" src="script.js"></script>
   ```

   <!-- (module auto defer krta hai aur isme imprt export ka feature bhi hota hai ) -->

   In `script.js`:

   ```js
   function greet() {
     alert("Hello from external JS file!");
   }
   ```

1) What are REST APIs and why are they so popular?

2) What is an API and different rest methods we use?

3) Can you explain the difference between a REST and SOAP API?

4)What are async and defer?

5)What is the difference between querySelector and QuerySelectorAll?

6)What is setTimeout?

7)What is async-await and how does it work?

8)What is a promise and what is its type?

9)What is the difference between Synchronous and Asynchronous functions?

10)What are the different ways of fetching data?

11)Define Callback Hell in Javascript.

12)What is asynchronous JavaScript and what is synchronous javascript?

13)What is async API?

13.1) what is an Api Endpoints and what does it includes ?

14. What is fetch API in Javascript? How does it handle JSON responses?

----read in fe 102 lect 5 onwards notes ----

----js 101 ka questions----
15)what are the different data types in JS ?

---

<!-----

  ---------15--------

--- -->

## 16) What is the difference between `==` and `===` in JavaScript?

---

### 🟢 **Similarity**

In JavaScript `==` and `===` are **comparison operators** used for comparison, but they differ in how they compare values.

---

Note - In case of Non primitive == and === will just the reference so both will return false for example []==[] (this will be false ) and also []===[] (this will also be false kyunki diff reference memory
location is different where this object /array is stored)

### 🔀 **Difference between `==` and `===`**

1. **Type Coercion**

   - `==`: Performs type coercion and converts values to a common type before comparison.
   - while `===`: Does not perform type coercion. It checks for both value and type equality.

2. **Strictness**
   - `==`: is Known as the **loose or abstract equality** operator as It allows equality comparison after type conversion.
   - and `===`: is Known as the **strict equality** operator as It requires both values and type to be same .

---

### 📺 Sir, can I share my screen to show this with an example?

```js
// Using ==
console.log(5 == "5"); // true → because it converts "5" to 5

// Using ===
console.log(5 === "5"); // false → number and string are different types

// Another example
console.log(null == undefined); // true
console.log(null === undefined); // false
```

> So, use `===` when you want **strict and safer comparison**.  
> And avoid `==` unless you know exactly how coercion will behave.

---

<!-----

  ---------17--------

--- -->

17)Explain the difference between null and undefined.

<!-----

  ---------18--------

--- -->

## 18) What are the differences between `var`, `let`, and `const`?

Ans :-

---

### ✅ First, the similarity:

`var`, `let`, and `const` are keywords which are used to **declare variables** in JavaScript.

But... there are some **key differences** between them 👇

---

### 🧠 The first major difference is in their: **Scope**

- `var` is **function-scoped**, which means it is only accessible within the function in which it is declared.
- while`let` and `const` are **block-scoped**, meaning they are accessible only within the {} block in which they are declared.

```js
function test() {
  if (true) {
    var x = 5;
    let y = 10;
  }
  console.log(x); // ✅ 5
  console.log(y); // ❌ ReferenceError
}
```

---

### 🧠 Secondly: **Re-declaration and re-assignment**

- variable declared with `var` **can be re-declared and reassigned** in the same scope.
- and variable declared with`let` can be **re-assigned** but not **redeclared** in the same scope
- and variable declared with `const` **can be neither re-declared nor reassigned** (in the same scope).

```js
var a = 10;
var a = 20; // ✅ Allowed

let b = 10;
// let b = 20; ❌ Error

const c = 30;
// const c = 40; ❌ Error
```

---

### 🧠 Thirdly: **Hoisting Behavior**

- Another difference is in how they are hoisted
  - variable declared with`var` is hoisted **and initialized with `undefined`**.
  - while variable declared with `let` and `const` are hoisted too, **but not initialized** — and they stay in a **Temporal Dead Zone (TDZ)** until the line where they are declared.

```js
console.log(a); // ✅ undefined
var a = 5;

console.log(b); // ❌ ReferenceError
let b = 10;
```

---

### 📺 Sir, can I share my screen to show this with a side-by-side example?

```js
function check() {
  console.log(x); // undefined
  // console.log(y); // ReferenceError
  // console.log(z); // ReferenceError

  var x = 10;
  let y = 20;
  const z = 30;
}
```

---

> 👉 **In short**:
>
> - `var` → old-school, function-scoped, re-assignable re-declarable
> - `let` → modern, block-scoped, re-assignable not re-declarable
> - `const` → modern, block-scoped, not re-assignable not re-declarable

---

<!-----

  ---------19--------

--- -->

## 19) Explain Hoisting in JS

---

### 🔍 **Need**

In JavaScript, sometimes variables or functions work even **before** they are even declared in the code as we can access them .This is known as **hoisting**.

---

### 📖 **What is it**

**Hoisting** in javascript is a phenomena where a variable declared with var keyword and function declaration are **move to the top of the code** and only the variable declaration is hoisted to the top not the initialization which basically means that we can access them even before they are declared.
It leads to bugs and problems in code .
For example if we try to print a variable a which is decalred using var even before its declaration we will get undefined as output as only the declaration part is moved to the Top not the initialization .

So in order to tackle the issues caused by hoisting, ES6 introduced two new keywords for declaring variables: let and const. what happens is that When variables are declared using let and const, they are also hoisted, but they enter a “temporal dead zone” (TDZ) from the start of the block until the declaration is encountered. This means you cannot access them before their declaration, and attempting to do so will result in a ReferenceError.

```javascript
console.log(a); // Output: undefined
var a = 5;
```

The above code should be visualized like this so that why we get undefined .

```javascript
var a;
console.log(a);
a = 5;
```

- **Output:** `undefined` because `var a;` is hoisted to the top, but the assignment happens later.

### Hoisting with `let` and `const`:

```javascript
console.log(a);
let a = 10;
```

- **Output:** `ReferenceError`(reference error as we cannot access it before initialization )
  because even though`let` and `const` are hoisted too, but they are in a **"temporal dead zone"**, so accessing them before declaration throws an error.

### ---------**\***EXTRA STARTS HERE**\*\***\*\*\*\***\*\***----------

`Extra --Variables declared with let and const are in what's called the Temporal Dead Zone from the start of the block until the line where they are declared.So if you try to access them before the actual declaration line, JavaScript will throw a ReferenceError.`

##### ex 3--

```javascript
func();
function func() {
  console.log("hello"); //  Hello   Because the entire function is hoisted at the top
}
```

Note - function declaration is hoisted entirely . (other function is hoisted partially (IT MEANS ONLY VARIABLE IS HOISTED AND uska type nahi pata ki wo variable function hai so if we call that function it will throw TypeError not undefined because we are making undefined call as function so this leads to error as we cannot make funciton call on undefined.) only if the function is declared using var cause of only declaration hoisted at top in var keyword and not assignment and if the function expression or arrow function is declared using let or const it will not be hoisted .(because let and const are not hoisted )

#### Function Hoisting

##### 1. **Function Declarations**:

- **Entirely Hoisted**: Function declarations are hoisted entirely to the top of their scope. This means you can call the function before its declaration in the code.
- **Example**:

  ```javascript
  console.log(myFunction()); // Works because myFunction is hoisted

  function myFunction() {
    return "Hello, world!";
  }
  ```

- **Example 2**:

```javascript
console.log(myFunction); // undefined, because only the declaration is hoisted
myFunction(); // TypeError: myFunction is not a function
var myFunction = function () {
  return "Hello, world!";
};
```

##### Explanation:

1. **Hoisting**: In JavaScript, variable declarations (but not initializations) are hoisted to the top of their scope. This means that the declaration of `myFunction` is hoisted, but its assignment (`function() { return "Hello, world!"; }`) is not.

2. **First `console.log(myFunction)`**: At this point, `myFunction` is declared but not yet assigned, so it logs `undefined`.

3. **Calling `myFunction()`**: Since `myFunction` is `undefined` at this point, trying to call it results in a `TypeError`, not a `ReferenceError`. The error message will be: `TypeError: myFunction is not a function`.

4. **Assignment**: After the assignment, `myFunction` becomes a function that returns `"Hello, world!"`.

#### 2. **Function Expressions and Arrow Functions**:

- **Hoisted Partially with `var`**: If a function expression is declared using `var`, only the variable declaration is hoisted, not the assignment.

- **Not Hoisted with `let` or `const`**: If a function expression or arrow function is declared using `let` or `const`, it is not hoisted.
- **Example**:

  ```javascript
  console.log(myFunction); // ReferenceError, because let and const are not hoisted

  let myFunction = () => {
    return "Hello, world!";
  };
  ```

#### Special Case with Function Expressions:

```javascript
funcExp();
var funcExp = function display() {
  console.log("Will this work?");
};
```

- **Output:** `TypeError` because `funcExp` is hoisted as `undefined`, but the function is not assigned yet.

---

### ---------**\***EXTRA ends HERE**\*\***\*\*\*\***\*\***----------

> In simple terms:  
> ✅ Variable and function **declarations are hoisted**,  
> ❌ but **initializations/assignments are NOT**.

---

### 🛠️ **How to implement / see it**

---

### 📺 Sir, can I share my screen to show this with an example?

```js
// Function hoisting works fine
greet(); // Output: Hello

function greet() {
  console.log("Hello");
}

// Variable hoisting
console.log(x); // Output: undefined
var x = 10;

// But let/const variables are hoisted in a different way
console.log(y); // ❌ ReferenceError: Cannot access 'y' before initialization
let y = 20;
```

---

> ✅ Function declarations are fully hoisted (you can call them before defining).  
> ⚠️ `var` is hoisted but its **value is `undefined`** until it is initialized.  
> ❌ `let` and `const` are hoisted too, but they are in a **"temporal dead zone"**, so accessing them before declaration throws an error.

---

## Let me know if you want the **real-world bug** that happens due to hoisting — it helps impress in interviews 💥

<!-----

  ---------20--------

--- -->

## 20) What are Closures in JavaScript?

---

### 🔍 **Need**

when we are building a counter kind of application in javascript that counts everytime a button gets clicked .

So to count the number of clicks we might want to store a variable in global scope so that whenever the button is clicked we update the count variable but the problem in this is that if we create a variable in the global variable that global counter variable can be changed from outside from any script on the page or even from just the browser.

and also if we declare the count variable insida a function that function will reset the count variable every time we call that function .

and So in order to create a variable that **remembers its value** but is still **protected** from outside source ? we need something known as **Closures**

---

### 📖 **What is a Closure?**

Function + lexical Environment .
A **closure** is a `combination of a function and its lexical environment`. It allows a function to access variables from its outer scope, even after the outer function has returned.
It **remembers the environment** in which it was created — this allows us to create **private variables** and maintain state.

---

### **How** ?

### 📺 Sir, can I share my screen to show this with an example?

```js
// Closure Example
const clickCounter = (function () {
  let counter = 0; // private variable

  return function () {
    counter++;
    console.log("Total clicks:", counter);
  };
})();

clickCounter(); // Total clicks: 1
clickCounter(); // Total clicks: 2
clickCounter(); // Total clicks: 3
```

```js
function counter() {
  let count = 0;

  return function countInner() {
    count++;
    return count;
  };
}
const myCounter = counter();

// counter function return kr rha hai ek function aur jab wo returned
// function ko humlog call krte hai toh wo outer function
// ka variable access.

console.log(myCounter()); // 1
console.log(myCounter()); // 2
console.log(myCounter()); // 3
```

```javascript
function parent() {
  const msg = "I am from function parent";
  function child() {
    console.log(msg + " called from child function");
  }
  return child;
}
let result = parent();
result(); // Output: I am from function parent called from child function
```

Here, the inner function still has access to the `counter` variable, even though the outer function has already executed — this is closure in action.

---

> ✅ Closures help you **preserve data privately** and **maintain state** without relying on global variables.

---

### **EXTRAS---**

NoteQ) BUT HOW CAN WE ACCESSING THIS msg variable here ???

Answer -- Cause when we are returning the function we are not only returning the function we are also returning its lexical environment so that's why the variable which were accessible in it .

The `child` function remembers its lexical scope (the `msg` variable) even after the `parent` function has returned.

So In conclusion

If a function is created inside another function , it retains access to the scope of that outer function function even after that outer function returns , because the outer function is in the lexical scope of the inner function .

---

Q) How closures are formed in javascripts?

**Need for Closures:**

- Closures are a powerful feature of JavaScript, enabling function encapsulation and private data management.
- They are fundamental to functional programming in JavaScript and are crucial for writing efficient and modular code.

**How Closures are Used:**

- Closures are often used to create private variables or functions.
- Since JavaScript doesn’t have built-in support for private variables, closures can encapsulate variables, making them accessible only to certain functions.
- This is useful for data encapsulation and object data privacy.
- Closures are also used in event handling, callbacks, and maintaining state in asynchronous operations.

Ans --- vvimp

### Practical Example of Closures:

```javascript
function multiply(storedNum) {
  return function (num) {
    return storedNum * num;
  };
}

const multiplyTwo = multiply(2);
const multiplyThree = multiply(3);
const multiplyFour = multiply(4);

console.log(multiplyTwo(5)); // 10
console.log(multiplyThree(6)); // 18
console.log(multiplyFour(7)); // 24
```

Explanation -- The above is returning a function and the below is calling that function as now the other varaible has the access to the returned function so it can call using its own name(`in this case multiplyTwo()` ab us variable me function return hoke aaya`).and access the parent function due to having the access of its lexical scope due to closure.

Note --The inner function returned by `multiply` retains access to `storedNum` due to closures.

---

<!-----

  ---------21--------

--- -->

## 21) Differentiate between `map()`, `filter()` and `reduce()` in JavaScript

---

### ✅ **Similarity**

All three — `map()`, `filter()`, and `reduce()` — are **array methods** in JavaScript. which are used to perform array operations in a **declarative style**. **and they do not mutate the original array** and are ideal for writing concise ,clean and functional code and chaining together .

But they have some differences in their use cases.

### 🔄 **Difference between `map()`, `filter()`, and `reduce()`**

### 🧠 1. `map()` – **Map method is used to Transform each element and return a new array**

- It takes a **callback function**
  and the callback function takes three things in the parameter **current element, current index and entire array**.
- and it performs some operation to each array element and
- Returns a **new array** with the transformed values.

```js
const nums = [1, 2, 3];
const doubled = nums.map((n) => n * 2); // [2, 4, 6]
```

✅ Use `map()` when: You want to **transform** data.

---

### 🧠 2. `filter()` – **and Filter method is used to filter for elements that satisy a certain condition**

- It also takes a **callback function similar like map method**.
- and it Returns a **new array** with **only those elements** which return true for the specified condition .

```js
const nums = [1, 2, 3, 4];
const evens = nums.filter((n) => n % 2 === 0); // [2, 4]
```

✅ Use `filter()` when: You want to **select** or **exclude** items based on condition.

---

### 🧠 3. `reduce()` – **on the other hand reduce method is used to Reduce the array to a single value**

- It takes two things in the argument one is a **callback function** and the other is an **initial value of accumulator**.

- The callback function in the reduce method is also known as **accumulator function** .

The callback function inside the reduce method takes **4 thing in the parameter** accumulator , current element, current index and entire array.which is different from map and filter method.

The reduce method just do operation with current element using the accumulator and return us the single value .(not an array unlike map and filter).

```js
const nums = [1, 2, 3, 4];
const sum = nums.reduce((acc, val) => acc + val, 0); // 10
```

✅ Use `reduce()` when: You want to **calculate a single result** (like sum, product, object, etc).

---

### 📺 Sir, can I share my screen to show this with an example?

```js
const arr = [1, 2, 3, 4, 5];

// map → Multiply each number by 2
const mapped = arr.map((num) => num * 2); // [2, 4, 6, 8, 10]

// filter → Keep only even numbers
const filtered = arr.filter((num) => num % 2 === 0); // [2, 4]

// reduce → Find sum of all numbers
const reduced = arr.reduce((acc, num) => acc + num, 0); // 15

console.log(mapped, filtered, reduced);
```

---

> ✅ Use `map()` when you want to **transform** data.  
> ✅ Use `filter()` when you want to **select** specific items.  
> ✅ Use `reduce()` when you want to **summarize or combine** everything into one result.

---

<!-----

  ---------22.0--------

--- -->

22.0)What are rest and spread operators ?

<!-----

  ---------22.1--------

--- -->

22.1)Differentiate between the rest and spread operators in javascript

<!-----

  ---------23--------

--- -->

## 23) What is a Callback Function in JavaScript?

---

Ans :--

### 🔍 **Need**

In real-world web apps, many tasks take **some time** — like **getting data from a server**, **reading a file**, or **waiting for the user to click a button**.
If we don’t handle these properly, our app can **freeze** or stop responding until the task is done.
So In such cases, we often want to **do something after the task is finished**.  
For example:

- After data is fetched, we may want to show it on the screen
- or When a button is clicked, we may want to do something.

so To handle such situations, we use **callback functions**

---

### 📖 **What is it**

A **callback functions** is a type of a function which is passed as an argument to a higher order function (as In JavaScript, functions are first-class objects, and we can pass functions as parameters to other functions and call them inside the other function) . The **callback function** is usually executed after some action has been performed and we want to do something after that action and so in order to perform that action we pass a **callback function**.

`> "Callback" means: **call me back when you're done.**`

---

### 🛠️ **How to implement**

### 📺 Sir, can I share my screen to show this with an example?

```js
// A basic function that takes a callback
function greetUser(name, callback) {
  console.log(`Hi, ${name}`);
  callback(); // calling the callback
}

// Define the callback
function sayBye() {
  console.log("Bye!");
}

// Pass the callback to the function
greetUser("Ravi", sayBye);

// Output:
// Hi, Ravi
// Bye!
```

### Benefit of using callback function.

The main reason of using callback function is that it is **very concise** and by using a callback function we can pass n no function inside our main function so this makes our **function dynamic** as oppose to it being hardcoded for one specific function.

---

Ek simple **calculator** ka example dete hain jisme hum **callback functions** ka use karke `add`, `subtract`, `multiply`, aur `divide` operations karenge. Isse clearly samajh aayega ki callback se function kaise dynamic ban jaata hai.

---

#### 🔧 JavaScript Calculator Example Using Callback Functions

```javascript
// Main calculator function that takes two numbers and a callback operation
function calculator(a, b, operation) {
  return operation(a, b);
}

// Different callback functions for each operation
function add(x, y) {
  return x + y;
}

function subtract(x, y) {
  return x - y;
}

function multiply(x, y) {
  return x * y;
}

function divide(x, y) {
  if (y === 0) {
    return "Cannot divide by zero!";
  }
  return x / y;
}

// Using calculator with different operations
console.log("Addition:", calculator(10, 5, add)); // ➝ 15
console.log("Subtraction:", calculator(10, 5, subtract)); // ➝ 5
console.log("Multiplication:", calculator(10, 5, multiply)); // ➝ 50
console.log("Division:", calculator(10, 5, divide)); // ➝ 2
```

---

### 📌 Callback Use Karne Ka Fayda Yahaan:

1. **Single calculator function** banayi — har operation ke liye alag se function likhne ki zarurat nahi.
2. **Dynamic behavior** — calculator function har tarah ka calculation kar sakta hai bas callback badal do.
3. **Code reusable & clean** — naye operation add karne hain? Sirf ek naya function bana ke callback mein pass kar do.

---

**Why Use Callbacks?**

- Callbacks make functions more flexible and reusable by allowing different functions to be executed at different times without modifying the higher-order function's code.

> ✅ Callback functions allow **control over flow**.  
> ✅ Used heavily in **event handling**, **timers**, **APIs**, and **functional programming**.  
> ❌ But they can cause **callback hell** — that’s why promises and async/await were introduced later.

---

<!-----

  ---------23.1----------

--- -->

## 23.1) What is a Higher-Order Function in JavaScript?

Ans:---

---

### 🔍 **Need**

In JavaScript, functions are **first-class objects**, which means they can be treated like any other data type — assigned to variables, passed as arguments, or returned from other functions.

Now, when building real-world applications, sometimes we want to write code that is more **flexible**, **reusable**, and **cleaner** by letting functions **work with other functions** — for example, passing a function to customize behavior or returning a function for delayed execution.

To do this, we need **Higher-Order Functions**

---

### 📖 **What is it**

A **Higher-Order Function (HOF)** is a function that:

- **Takes one or more functions as arguments**, or
- **Returns a function as its result**

Basically, it’s a function that **operates on functions**, either by receiving them or returning them.

---

### 🛠️ **How to implement**

You can create HOFs by accepting functions as parameters or returning functions from inside other functions.

---

### 📺 Sir, can I share my screen to show this with an example?

\*_Show the example of map method sort method koi bhi inbuild function jo ek callback function argument me leta hai bs hogya AND APNA SE BHI KRKE DIKHAO CALLBACK FUNCTION USE_

- **Example:**

  ```javascript
  function higherOrderFunction(callback) {
    callback();
  }

  function myCallback() {
    console.log("I am a callback function");
  }

  higherOrderFunction(myCallback);
  ```

In this example:

- `myCallback` is the **callback function** because it is passed as an argument to `higherOrderFunction`.
- `higherOrderFunction` is the **higher-order function** because it takes another function (`myCallback`) as an argument.

---

### Key Points:

- A callback function is not necessarily called inside another function; it is passed to another function to be called later.

---

### Benefits of using callback function

> ✅ Higher-Order Functions help in **abstracting behavior**, **code reuse**, and **functional programming** patterns.  
> ✅ Common examples in JS include built-in methods like `.map()`, `.filter()`, and `.reduce()`, which all take functions as arguments.

---

<!-----

  ---------24--------

--- -->

24)Explain array destructuring and object destructuring in JavaScript.

<!-----

  ---------25--------

--- -->

25)Describe the features described in ES6.

<!-----

  ---------26.0--------

--- -->

## 26.0) What is shallow copy deep copy in JavaScript?

---

### 🔍 **Need**

In JavaScript, when we copy an object or an array, sometimes the changes in the copied version also affect the original one — which is not expected. And in order to understand why this happens, we need to understand the **difference between shallow copy and deep copy**.

---

### 📖 **What is it**

A **shallow copy** means copying just the reference of the variable which is holding the address of **non-primitive data type**, and in case of object it means copying only the **top-level properties**. If the object contains nested objects, those are **still shared** between the original and the copy.

On the other hand, a **deep copy** means creating a new object (array or object) and then manually copying each element of that object into it, so that changing the copied object does not affect the original object.

**Note** —  
In JS we can use the **spread operator** to solve shallow copying problems for the first layer of objects. But if the object is deeply nested, we need to use `JSON.stringify()` and `JSON.parse()` or libraries like Lodash, because spread also does shallow copying in the case of nested object as — it just copies references of nested objects.

> 🔥 **Bonus:** In modern JavaScript (ES2022+), we also have a native method called `structuredClone()` that can perform deep cloning and supports more data types like `Date`, `Map`, `Set`, etc., unlike JSON methods.

---

### 🛠️ **How to implement**

### 📺 Sir, can I share my screen to show this with an example?

```js
const obj1 = { arun: 1, boy: { cat: 2 } };

// Shallow Copy using spread
const shallow = { ...obj1 };

// Deep Copy using JSON
const deep = JSON.parse(JSON.stringify(obj1));

// Deep Copy using structuredClone (modern way)
const deepModern = structuredClone(obj1);

shallow.boy.cat = 100;
console.log(obj1.boy.cat); // 100 (shallow copy affected original)

deep.boy.cat = 200;
console.log(obj1.boy.cat); // 100 (deep copy didn’t affect original)

deepModern.boy.cat = 300;
console.log(obj1.boy.cat); // 100 (structuredClone also didn’t affect original)
```

---

> ✅ Use **shallow copy** when you’re sure the object has no nested structure.  
> ✅ Use **deep copy** when your object has **nested objects/arrays** and you want full independence.  
> ✅ Use `structuredClone()` in modern environments for better performance and data-type support than JSON METHODS

---

<!-----

  ---------26.1--------

--- -->

26.1)Can you explain the difference between a shallow copy and a deep copy of an object in JavaScript?

27)What are the differences between arrow functions and function expressions in JS?

28)How are arrays different from objects in JavaScript?

29)Can you explain the difference between dot notation and square bracket notation when accessing object properties? When would you use one over the other?

## ---------js 101 question ends----

30. What is a Date method in js and how do we use it to get date and what are some of its method ?

31) Can you tell what is the difference between putting the <script> tag inside <body> and puting <script> tag inside <head> Can you tell the reason where should we put our script tag and why?

32)What is the difference between html collections and node list ?

33)Difference between the innerText and textContent and and innerHtml?

34. How to create a Html element in javascript and then append it to our Html Dom? what are those 4 steps

35)How to give style in javascript using style object?

36. What are the 5 ways of selecting element?

Ans :-- All 5 ways of selecting element

1. getElementsByTagName
2. getElementsByClassName("")
<!-- no need to give . in class name here
only in query Selecotr ones we need to do that -->
3. getElementById
4. querySelector
5. querySelectorAll("")

   37)What does the "window" object represent in JavaScript?

Ans :-- The browser window or tab.

38)what is dom and why do we need dom?

39. How to do crud application on dom?

Ans --

create - using .createElement

Read- All 5 ways to select the elements

Update- In order to update it we use ( textContent, innerText, innerHtml)

Delete- remove method

--- One liner questions :-----

40. In which type does innerHtml returns the content of an Element?

Ans :-- string

41. what is an event loop ?macrotask queue and microtask queue ? explain the whole working

42. what is a callstack in javascript and how many callstack does javascript have?

43. What is the raw data format in which we format we get data and why we convert it to json ?

## -----fe 103 ka questions:---- (watch videos and apna notes)

<!-----

  ---------19--------

--- -->

## 44) What are Event Listeners?

Ans :-

---

### 🔍 **Need**

In real-world web apps, users interact with the UI by **clicking buttons**, **typing in inputs**, **hovering over elements**, etc.  
To make our web page **respond** to these actions — like showing a popup when a button is clicked — we need a way to **listen to those actions in javascript**.

so for this we need something known as **Event Listeners** .

---

### 📖 **What is it**

An **Event Listener** is a function in JavaScript that **waits for a specific event to happen** (like a click, keypress, hover, etc.) on a specific element — and **runs a function when that event occurs**.

It's like telling the browser:

> “Hey, when the user clicks this button, call this function.”

---

### 🛠️ **How to implement**

We use the `.addEventListener()` method to attach an event to any DOM element.

```js
const btn = document.getElementById("myBtn");

btn.addEventListener("click", function () {
  alert("Button clicked!");
});
```

- `"click"` is the event type.
- The function inside will run **only when** the button is clicked.

---

### 📺 Sir, can I share my screen to show this with an example?

```html
<button id="greetBtn">Greet Me</button>

<script>
  const greetBtn = document.getElementById("greetBtn");

  greetBtn.addEventListener("click", () => {
    console.log("Hello, User!");
  });
</script>
```

🧠 Pro Tip:  
You can use Event Listeners for **mouse events, keyboard events, input events**, and even **custom events** to create dynamic, interactive web experiences.

---

<!-----

  ---------19--------

--- -->

45)What is an event loop? How does JavaScript event loop work and how does it contribute to the language's asynchronous nature? Can you explain the concept of the call stack and the message queue in this context?

46)How to console params and query in JavaScript?

47)What is Event Bubbling in JavaScript?

48. Describe Web Storage.

49)What are cookies and how are they used?

<!-----

  ---------50--------

--- -->

## 50. Explain the differences between localStorage and Session Storage.

Ans:--

### Similarity first

Both **localStorage** and **sessionStorage** are part of the **Web Storage API** They allow us to store data in the browser in key-value pairs. —They are often used to store data like: user preferences , tokens .

### Then diff

But There are some **key differences** between them

---

1. **The first major difference is that .**

   - The `localStorage` stores data **permanently** — unless we remove it manually or the browser cache is cleared.
   - But `sessionStorage` stores data **only for that specific tab session** — and the data gets cleared automatically when the tab is closed.

---

2. **Secondly, their usage across tabs is different.**

   - Data in `localStorage` is **shared across all tabs** of the same origin (website). So if you open multiple tabs of the same site, they can all access the same localStorage data.
   - But `sessionStorage` is **tab-specific** — each tab has its own sessionStorage, and it’s not shared between tabs.

---

3. **Thirdly, both store data as strings — but there’s a difference in intent.**

   - Use `localStorage` when you want to store data like theme, auth token, or user preferences that should be **available even after refreshing or reopening the browser**.
   - Use `sessionStorage` when you want to keep temporary data like form values or one-time user flow data that **should reset on tab close**.

---

4. **Also, both have a storage limit of around 5MB** — but that can vary a bit depending on the browser.

---

### 📺 Sir, can I share my screen to show this with an example?

```js
// Storing data
localStorage.setItem("user", "John");
sessionStorage.setItem("token", "abc123");

// Getting data
console.log(localStorage.getItem("user")); // "John"
console.log(sessionStorage.getItem("token")); // "abc123"

// Removing data
localStorage.removeItem("user");
sessionStorage.removeItem("token");
```

> 👉 So the key difference is:  
> localStorage = long-term across tabs,  
> sessionStorage = short-term and tab-specific.

<!-----

  ---------51--------

--- -->

51)what is the difference between event propagation and event deleegation , event bubbling ? (javascript.info and web.dev)

52)How to do form validations make notes on it you know it just speak in your words and match with chatgpt ?

53. How javascript handle asynchronous code ?

54. What is the difference between type coercion and type conversion ?
