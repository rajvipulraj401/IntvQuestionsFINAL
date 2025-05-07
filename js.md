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

<!-----

  ---------14--------

--- -->

14.What is Fetch API in JavaScript? How does it handle JSON responses?

---

### 🔍 **Need**

In modern web apps, we often need to **communicate with servers** to fetch or send data — like getting product listings, sending form data, etc.  
To do this, JavaScript provides the inbuild **Fetch API**, which is a modern way to make HTTP requests in javascript without relying on any external libraries like axios.

---

### 📖 What is Fetch API?

The **Fetch API** is a built-in JavaScript feature that allows us to make network requests (like GET, POST) to servers and work with the responses using **Promises**.

SO when we call the `fetch` method with a URL . we get in return a **Promise** that will either be **fulfilled** or **rejected** based on the response coming from the server . and if it gets resolved it resolves to a **Response object**, which contains info like status, headers, and body.

---

### 📦 How does it handle JSON?

So ,By default the `fetch()` method returns a **Response object**, not the actual data.  
To read JSON data from the response, we call the `.json()` method on the response, which also returns us a **Promise** and we have to handle that to get our original data.

---

### 📺 Sir, can I share my screen to show this with a live API?

<!-- fetch("https://jsonplaceholder.typicode.com/posts/1") -->
<!-- fetch("https://api.example.com/users") -->

```js
const response = fetch("https://jsonplaceholder.typicode.com/todos")
  .then((res) => {
    // .json() ko .then() ke andar handle kar rahe ho
    return res.json();
  })
  .then((data) => {
    console.log(data); // Yahaan pe real JSON data aayega
  })
  .catch((err) => {
    console.log("Error:", err); // Agar koi error ho, toh yahaan handle hoga
  });

console.log(response); // Yeh abhi bhi Promise hi log karega

/* ------------method 2-------- */
const handleMethod = async () => {
  try {
    const data = await fetch("https://jsonplaceholder.typicode.com/todos");
    const response = await data.json();
    console.log(response);
    return response;
  } catch (err) {
    console.log(err);
  }
};

handleMethod();
```

---

### ✅ Summary

| Feature                | Explanation                                           |
| ---------------------- | ----------------------------------------------------- |
| **Purpose**            | Used to make HTTP requests (GET, POST, etc.)          |
| **Returns**            | A Promise that resolves to a `Response` object        |
| **To get JSON data**   | Use `.json()` method on the response                  |
| **Modern alternative** | Cleaner and Promise-based, replacing `XMLHttpRequest` |

---

> 🔥 Pro Tip: Always handle `.json()` with `await` or `.then()` because it’s asynchronous too!

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

## 22.0) What are the Rest and Spread Operators?

---

### 🔍 **Need**

In real-world JavaScript projects, we often face two types of problems:

1. Sometimes, we don’t know **how many values** a user will pass — like in a function that accepts any number of arguments (e.g. `sum(1, 2, 3, 4, ...)`).
2. and Other times, when we need to **expand** arrays or objects — for example, when copying, merging, or passing data into functions.

So, in order to do this quickly and efficiently, JavaScript (in ES6) introduced the **Rest operator** and **Spread operator**.  
Both use the triple-dot `...` syntax, but they have **different use cases**.

---

### 📖 What is it

---

1. **The first major difference is their purpose.**

(**R**) - The **rest operator** is used to **gather multiple values into a single array or object** —
we mostly use the rest parameter in a function parameter, it collects all the various arguments passed to it .The arguments that we passed as comma-separated into an array or object.

     for example :-- If we pass numbers from 1 to 10 in a function to calculate the sum, the rest parameter will collect all the elements into an array.

(**S**) - On The other hand the **spread operator** is Used to **spread the elements out of an array or object into another variables** .

- For Example: In the same example above, we get all the elements in an array. Now, we can use the spread operator to destructure them into different variables. like if we have two array and then we want to create another array containing the two elements and with this new array we can use spread syntax and get all of them in one new array by spreading them in one

---

2. **Secondly, their use cases differ.**

   - Use **rest** when you're handling **dynamic function arguments**, like when you don’t know how many values the user will pass.
   - Use **spread** when you want to **copy, merge, or pass values**, like cloning arrays or spreading props in React.

---

3. **Their placement also matters.**

- Also The **rest operator** has to be the **last parameter in function definitions and in destructring**
  The spread operator, on the other hand, **can be used anywhere (in start mid ,end anywhre)** — such as in function calls, or spreading array or object .

---

### 📺 Sir, can I share my screen to show this with an example?

Example :-- **(rest operator)**

```js
function sum(...args) {
  return args.reduce((a, b) => a + b, 0);
}

const [a, ...rest] = [1, 2, 3]; // a = 1, rest = [2, 3]

const person = {
  name: "John",
  age: 30,
  country: "USA",
};

// Destructuring with rest to collect remaining properties into an object
const { name, age, ...rest } = person;

console.log(name); // 'John'
console.log(rest); // { country: 'USA' }

const { x, ...others } = { x: 10, y: 20, z: 30 }; // x = 10, others = { y: 20, z: 30 }
```

Example **(spread operator)**

```js
const arr1 = [1, 2];
const arr2 = [...arr1, 3, 4]; // [1, 2, 3, 4]

const obj1 = { a: 1, b: 2 };
const obj2 = { ...obj1, c: 3 }; // { a: 1, b: 2, c: 3 }

const nums = [1, 2, 3];
Math.max(...nums); // Same as Math.max(1, 2, 3)
```

---

> 👉 So the key difference is:  
> **Rest = Gather** into one (for input)  
> **Spread = Expand** out (for output)

---

### 🧠 **Quick Tips**

- **Rest parameter:**

  - Used **in function definitions** to collect multiple arguments into an array.
  - Must be the **last parameter**.
  - Always collects into an **array**.in the function parameter
  - And in case of destructring into any variable use at last and there it can get object while destructring obje and array while destructing arr to get the rest of obj or rest of arr in it.

- **Spread operator:**
  - Used **when calling functions**, or inside **arrays/objects** to expand elements or properties.
  - Can be used **anywhere** (no positional restriction).
  - Works for **arrays and objects**.

---

---

<!-----

  ---------22.1--------

--- -->

## 22.1) Differentiate between the rest and spread operators in JavaScript?

---

### ✅ **Similarity first**

Both **rest** and **spread** operators are represented by three dots (...)  
They help us **work with arrays, objects, or function arguments** in a flexible way. Despite being represented by **same syntax** —
, they have differenet use cases.

---

### 🔄 **But there are some key differences between them**:

---

1. **The first major difference is their purpose.**

(**R**) - The **rest operator** is used to **gather multiple values into a single array or object** —
we mostly use the rest parameter in a function parameter, it collects all the various arguments passed to it .The arguments that we passed as comma-separated into an array or object.

     for example :-- If we pass numbers from 1 to 10 in a function to calculate the sum, the rest parameter will collect all the elements into an array.

(**S**) - On The other hand the **spread operator** is Used to **spread the elements out of an array or object into another variables** .

- For Example: In the same example above, we get all the elements in an array. Now, we can use the spread operator to destructure them into different variables. like if we have two array and then we want to create another array containing the two elements and with this new array we can use spread syntax and get all of them in one new array by spreading them in one

---

2. **Secondly, their use cases differ.**

   - Use **rest** when you're handling **dynamic function arguments**, like when you don’t know how many values the user will pass.
   - Use **spread** when you want to **copy, merge, or pass values**, like cloning arrays or spreading props in React.

---

3. **Their placement also matters.**

- Also The **rest operator** has to be the **last parameter in function definitions and in destructring**
  The spread operator, on the other hand, **can be used anywhere (in start mid ,end anywhre)** — such as in function calls, or spreading array or object .

---

**So in Conclusion:**

- `Use the rest operator when we have multiple arguments passed to a function and we want to collect them in one variable.`
- **and Use the spread operator when we want to destructure all the elements from an array into variables or merge and create a new array with another array.**

### 📺 Sir, can I share my screen to show this with an example?

Example :-- **(rest operator)**

```js
function sum(...args) {
  return args.reduce((a, b) => a + b, 0);
}

const [a, ...rest] = [1, 2, 3]; // a = 1, rest = [2, 3]

const { x, ...others } = { x: 10, y: 20, z: 30 }; // x = 10, others = { y: 20, z: 30 }
```

Example **(spread operator)**

```js
const arr1 = [1, 2];
const arr2 = [...arr1, 3, 4]; // [1, 2, 3, 4]

const obj1 = { a: 1, b: 2 };
const obj2 = { ...obj1, c: 3 }; // { a: 1, b: 2, c: 3 }

const nums = [1, 2, 3];
Math.max(...nums); // Same as Math.max(1, 2, 3)
```

---

> 👉 So the key difference is:  
> **Rest = Gather** into one (for input)  
> **Spread = Expand** out (for output)

---

<!-----

  ---------22.2--------

--- -->

## 22.2) Diff in working of Spread Syntax with Objects and Arrays ?

**Objects**:

- **Explanation**: When spreading an object, if a property already exists, it updates the property with the new value; otherwise, it adds the new property.
- **Example**:

  ```javascript
  const existingUser = {
    id: 123,
    name: "Alex Johnson",
    email: "Alex.johnson@ex.com",
    age: 28,
    membershipStatus: "active",
  };

  const updatedInfo = {
    email: "alexj@example.net",
    age: 29,
    membershipStatus: "premium",
  };

  let finalObj = { ...existingUser, ...updatedInfo };
  console.log(finalObj);
  ```

**Output:**

```javascript
{
    id: 123,
    name: "Alex Johnson",
    email: "alexj@example.net",
    age: 29,
    membershipStatus: "premium"
}
```

**In Arrays**:

- When spreading arrays, elements are combined into a new array. Each element is added in the order it appears, without any special handling for existing values.

**Example**:

```javascript
const fruits = ["apple", "banana"];
const additionalFruits = ["cherry", "date"];

// Adding new elements to the beginning and end of the array
const allFruits = ["kiwi", ...fruits, "mango", ...additionalFruits];
console.log(allFruits);
```

**Output**:

```javascript
["kiwi", "apple", "banana", "mango", "cherry", "date"];
```

**Explanation**:

- Arrays are combined by simply appending the elements in order, so there is no concept of overwriting like objects.

---

Now why this happens in case of objects ?

Ans --- In case of array it merge because there we follow concept of indexing and in case of object we follow the concept of naming so if the property name exists update it else add it.

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

25)Describe the features described in ES6. ❌

Ans -- ES6, also known as ECMAScript 2015, introduced several new features and improvements to the JavaScript language.

For Example :--

1. Introduction to two new keywords let and const: ES6 introduced block-scoped variables using the let and const keywords. let allows declaring variables that are limited to the block scope, while const is used for declaring constants that cannot be reassigned.

2. Arrow Functions: Arrow functions provide a more concise syntax for writing function expressions. They have a shorter syntax, lexical this binding, and implicit return for one-liner functions.

3. Introduction to Template Literals: Template literals allow embedding expressions inside string literals using backticks (`). This feature provides an easier way to concatenate strings and variables, making the code more readable.

4. Introduction to Destructuring : Destructuring allows extracting values from arrays or objects into individual variables. It provides a concise way to assign values and access nested properties.

5. Spread Operator: The spread operator (...) allows expanding elements of an iterable (like an array or string) into individual elements. It can be used for array concatenation, function arguments, and object cloning.

6. Promises: Promises provide a cleaner way to handle asynchronous operations. It solved the problem of callback Hell. They represent the eventual completion (or failure) of an asynchronous operation and allow chaining multiple asynchronous operations together.

Classes: ES6 introduced class syntax for creating objects with a constructor and methods. It provides a more familiar syntax for defining classes and inheritance in JavaScript.

Modules: ES6 introduced a standardized module system using the import and export keywords. Modules allow organizing code into separate files and provide better encapsulation and reusability.

Default Parameters: ES6 allows defining default values for function parameters. If a parameter is not provided, the default value will be used instead.
Enhanced Object Literals: ES6 introduced enhancements to object literals, including shorthand property and method definitions, computed property names, and the ability to define setters and getters.

These are just a few of the many features introduced in ES6. These additions have significantly improved the JavaScript language, making it more powerful, expressive, and easier to work with.

---

# Note --_Read more about Es6 in jonas copy and also about all different function in his copy_

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

Exp2 :--

```js
// const message = 'Hello world' // Try edit me

// // Update header text
// document.querySelector('#header').innerHTML = message

// // Log to console
// console.log(message)

const arr = [2, 345, 6];
const arr2 = arr;
console.log(arr);
// arr2[1] = 3;
// console.log(arr)
const arr3 = JSON.parse(JSON.stringify(arr));
//this way we do deep copy
console.log(arr3);
arr3[1] = "lan";
console.log(`arr1 ${arr}`);
console.log(`arr3 ${arr3}`);

const arr4 = structuredClone(arr);

//This is a global method not any method specific to array

console.log(arr4);
```

<!-----

  ---------27--------

--- -->

(write again)
27)What are the differences between arrow functions and function expressions in JS?

**Answer:---**

- Arrow function was introduced in ES6 version of JavaScript.
- The difference between arrow function and function expression lies in its syntax and some of its use cases.

**When we talk about Arrow Function:**

- The Arrow function make use of an arrow `=>`like syntax instead of writing function keyword which makes it different from other types of funciton .
- The benefit it has over function expression is that it is concise.
  - For example, when we have a single line of code in a function, we can omit the curly brackets as well as the `return` keyword.
  - Not only that, when we have a single parameter, we can even omit the small bracket around the parameter and keep only the parameter name there. In this way, the function becomes concise.

**In contrast when talking about Function Expression:**

- This type of function is used to store an anonymous function in a variable.
- While arrow functions also do that, the main difference between them is that arrow functions are concise but do not have the `this` keyword.
  - This is crucial whenever dealing with methods inside objects.and also trying to create constructor and trying to use with new keyword as arrow function cannot do this.

**Additional Note:**

- The main reason for the introduction of these two functions was that earlier, function declarations were hoisted to the top of the code, which used to create bugs as they could be called even before they were declared and this two new functions are not hoisted to the top of their scope .
  In conclusion use Function expression whenver we want to make use of a function with its own this keyword or want to use a function as a constructor and use arrow function whenver we want to write callback function as well as want our function to be concise.

---

<!-----

  ---------28--------

--- -->

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

Ans :---

बिलकुल भाई, मैं पूरी तरह से सुन रहा हूँ — और अब जो फॉर्मैट तुमने बोला (Need → What → How), उसी में आगे बढ़ते हैं। चलो पहले तुम्हारा स्टार्टिंग हिस्सा पकड़ते हैं और फिर मैं तुम्हारी बात को क्लीयर, इंटरव्यू-रेडी और स्ट्रक्चर्ड तरीके से जमाने में मदद करता हूँ।

---

## ✅ **Need (क्यों DOM चाहिए?)**

> In JavaScript or in web development, when we create websites, the browser doesn't understand our HTML and CSS as-is. Instead, it parses the entire HTML structure and converts it into a tree-like format so that JavaScript can interact with each element efficiently. This tree structure allows dynamic manipulation of content — like updating text, changing styles, handling events, etc. That's why we need the DOM — to bridge HTML with JavaScript.

---

## ✅ **What is DOM?**

> DOM stands for **Document Object Model**.
> It's a **programmatic representation** of the HTML page loaded in the browser.
> It represents the **structure** of the page as a **tree of nodes** — where every tag becomes a node, and JavaScript can access or modify any part of it.

Example:

```html
<body>
  <h1>Hello</h1>
  <p>World</p>
</body>
```

DOM Tree for this:

```
Document
 └── html
     └── body
         ├── h1
         └── p
```

---

## ✅ **How do we use DOM in JavaScript?**

> We use the **DOM API** to select, create, modify, or delete elements on the webpage.

### Examples:

**1. Select an element:**

```js
let heading = document.querySelector("h1");
```

**2. Change content:**

```js
heading.textContent = "Welcome!";
```

**3. Create a new element:**

```js
let newPara = document.createElement("p");
newPara.textContent = "This is a new paragraph.";
document.body.append(newPara);
```

**4. Delete an element:**

```js
newPara.remove();
```

---

## 🔥 Final Wrap (Interview-Style):

> So the DOM is essential because it gives JavaScript the ability to **interact with HTML content** dynamically. We use it to create interactive, real-time updated user interfaces.

---

\_---

39. How to do crud application on dom?

Ans --

create - using .createElement

Read- All 5 ways to select the elements (see old notes of fe103)

Update- In order to update it we use ( textContent, innerText, innerHtml)

Delete- remove method

```js
/* select the element */
let select = document.querySelector("#heading");
console.log(select.textContent);

/* create element */

let newElm = document.createElement("h3");

/* update element */
newElm.textContent = "hello div";

/* append kr diya wo elment */
let appendElm = document.querySelector(".appender");
appendElm.append(newElm);

/* deleting the elemetn using remove method */
/* appendElm.remove(newElm); */

newElm.remove();
```

--- One liner questions :-----

40. In which type does innerHtml returns the content of an Element?

Ans :-- string

41. what is an event loop ?macrotask queue and microtask queue ? explain the whole working

42. what is a callstack in javascript and how many callstack does javascript have?

Exampless Ans :---

### 1. **Need (Why do we need a call stack?)**

> In JavaScript, we often write several functions that call each other. To keep track of which function is currently being executed, and where to return after a function completes, we need some kind of system.
> That's where the **call stack** comes in—it helps JavaScript keep track of function execution in the correct order.

---

### 2. **What (What is a call stack?)**

> A **call stack** is a data structure that works on the **LIFO** principle—**Last In, First Out**.
> It stores the function calls in the order they're made. When a function is called, it's added to the top of the stack. When it's finished, it's removed from the top.
> JavaScript is **single-threaded**, so it has **only one call stack**. That means it can only do one thing at a time.

---

### 3. **How (How does it work? + With example)**

> Along with the call stack, JavaScript also uses the **event loop**, **microtask queue**, and **macrotask queue** to handle asynchronous operations.
> Here's a quick breakdown:
>
> - **Synchronous tasks** go directly into the call stack.
> - **Microtasks** (like promises) go into the **microtask queue**.
> - **Macrotasks** (like `setTimeout`) go into the **macrotask queue**.

> Let’s say we have the following code:

```javascript
console.log("Hello");
setTimeout(() => console.log("from timeout"), 0);
Promise.resolve().then(() => console.log("from promise"));
console.log("Goodbye");
```

> Here's what happens:
>
> 1. `"Hello"` is logged immediately (synchronous).
> 2. `setTimeout` is scheduled → goes to **macrotask queue**.
> 3. The `.then()` callback is scheduled → goes to **microtask queue**.
> 4. `"Goodbye"` is logged (synchronous).
> 5. After the stack is empty, microtasks run → logs `"from promise"`.
> 6. Then the macrotask (`setTimeout`) runs → logs `"from timeout"`.

> This is how JavaScript handles both **synchronous** and **asynchronous** code using the **call stack** and the **event loop system**.

---

## 🎤 Final Tip on Speaking

जब आप बोलते हो, तो ध्यान रखें कि आप तीन चीज़ें साफ़ करें:

1. **आप क्यों बता रहे हो (Need)**
2. **क्या है वो चीज़ (What)**
3. **कैसे काम करती है (How – with example/code)**

इस फॉर्मैट से आपका जवाब structured और professional लगेगा, जो interview में बहुत असरदार होता है।

---

क्या आप चाहेंगे कि मैं आपके लिए इस पूरे corrected जवाब का एक **स्क्रिप्टेड स्पीकिंग वर्शन** बनाऊँ जिससे आप प्रैक्टिस कर सकें बिल्कुल natural English में?

---

43. What is the raw data format in which we format we get data and why we convert it to json ?

Anss :----

---

### 1. **Need (Why do we need to convert data to JSON?)**

> When we make API calls in JavaScript, we receive data from a server.
> This data usually comes in **raw format**, like a **text stream** or **binary stream**, and we can't directly work with it in our JavaScript code.
> So, to make it **readable and usable**, we need to **convert or parse** this data into a structured format like JSON.

---

### 2. **What (What is JSON and why is it used?)**

> **JSON (JavaScript Object Notation)** is a lightweight, text-based format used to represent structured data.
> It's easy to read and write, and more importantly, it's easy to **convert into JavaScript objects** using `JSON.parse`.
> Most APIs send data in JSON format because it's **language-independent**, but works natively with JavaScript.

---

### 3. **How (How does this work in code?)**

> Let's say we're calling an API using `fetch`. Here's a simplified example:

```javascript
async function getData() {
  try {
    const response = await fetch("https://api.example.com/data");
    const data = await response.json(); // This converts raw response to usable JSON
    console.log(data); // Now 'data' is a JS object or array
  } catch (error) {
    console.error("Error fetching data:", error);
  }
}
```

> In this example:
>
> - The `fetch()` method returns a **Response object**.
> - We call `.json()` on that response to **parse the raw stream into a JSON object**.
> - Once parsed, we can easily access its properties like any other JavaScript object.

---

### 🔁 Summary

> So, in summary, data received from an API is often in raw form, like a stream.
> We convert it to **JSON** so we can work with it as a **JavaScript object** using `.json()` and `JSON.parse`.
> That makes the data easier to **manipulate, render, or store** in our applications.

---

## 🎙️ Speaking Tips (Based on Your Original)

- Avoid repeating phrases like “we actually”, “we make use of” too often.
- Use clear sentence breaks and transitions.
- Practice pronouncing technical terms confidently: "`response.json()`", "JSON.parse", "JavaScript object", etc.
- Instead of saying “I think readable”, say directly “in raw text format which is not directly readable”.

---

---

## -----fe 103 ka questions:---- (watch videos and apna notes)

<!-----

  ---------19--------

--- -->

## 44) What are Event Listeners?

Ans :-

---

### 🔍 **Need**

In real-world web apps, we want users to interact with the UI by **clicking buttons**, **typing in inputs**, **hovering over elements**, etc.  
So To make our web page interactive and **respond** to these actions — we need a way to **listen to those actions in javascript**.

and for this we need something known as **Event Listeners** .

---

### 📖 What is it

An **event listener** in JavaScript is basically a way to make your webpage interactive. It **listens for certain actions (events)** like clicks, scrolls, or hovers from the user. Whatever interaction the user does on the page is known as an **event**, and the job of an event listener is to **listen** for those events.

To listen to an event, we use the .addEventListener() method, which we need to attach to the element we want to listen to.

The `addEventListener` method takes **three things in its argument**:

1. The **type of event** (like `'click'`, `'scroll'`, `'mouseover'`, etc.)
2. The **callback function** — which tells what needs to happen when the event occurs
3. and An **options parameter** which is optional and it is— used for advanced control like whether the event should bubble or capture (not always needed)

` used for advanced control like event bubbling or capturing (not always required)`

---

### 🛠️ How to implement

We use the `.addEventListener()` method to attach an event to any DOM element.

```js
element.addEventListener("eventType", callbackFunction, options);
```

- `element`: The HTML element you want to listen to.
- `'eventType'`: The type of event you want to listen for (string).
- `callbackFunction`: The function to execute when the event happens.
- `options` (optional): An object or boolean controlling event propagation behavior.

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

## 45)What is an event loop? How does JavaScript event loop work and how does it contribute to the language's asynchronous nature? Can you explain the concept of the call stack and the message queue in this context?

46)How to console params and query in JavaScript?

ans:---That's a great start—and I really appreciate that you're trying to **speak in a structured format (Need → What → How)** and even acknowledging when you're unsure. That’s honest and human. Let’s go through what you said, line-by-line first, and then I’ll give you a **corrected, complete version** of the answer using the same speaking style you're practicing.

---

## 🧾 **Your Spoken Answer (Original - As Spoken)**

> So, when we actually make any API calls or whenever we actually went to any server, we can see that in the URL, we have, after the question mark, we can see some of the things which are written.
> So, those things, like for example, we went to a URL called [www.xyz.com](http://www.xyz.com) and then slash page, then question mark, event equal to something. And then and equal to, and place equal to something.
> So, whatever that is written after the question mark is actually a parameter, a query and parameter of the URL.
> So, in order to console.log that thing in JavaScript, I don't know what to do. I actually forgot it.

✅ You're trying to explain something correctly but got stuck on the **"how"** part—which is totally fine in practice mode.

---

## ✅ **Corrected & Complete Answer in “Need → What → How” Format**

---

### 1. **Need (Why do we need to access query parameters?)**

> When working on web applications, we often receive data through the URL in the form of **query parameters**.
> These are typically used for filtering, tracking, pagination, or passing small bits of data between pages.
> So, we need a way in JavaScript to **read and work with** those query parameters.

---

### 2. **What (What are query parameters?)**

> Query parameters are the key-value pairs that appear **after the `?` in a URL**.
> For example:
> `https://www.xyz.com/page?event=webinar&place=delhi`
> In this case, `event=webinar` and `place=delhi` are query parameters.
> They're not part of the path—they’re extra data sent in the URL.

---

### 3. **How (How to access or log them using JavaScript)**

> Sir, I would like to share my screen to show this with an example. Let me write some code to demonstrate:

```javascript
// Let's say our URL is:
// https://www.xyz.com/page?event=webinar&place=delhi

const params = new URLSearchParams(window.location.search);

const event = params.get("event");
const place = params.get("place");

console.log("Event:", event); // Output: webinar
console.log("Place:", place); // Output: delhi
```

> In this code:
>
> - `window.location.search` gives us everything after the `?` in the URL.
> - `URLSearchParams` is a built-in JavaScript object that makes it easy to extract individual query values.
> - We use `.get("key")` to retrieve the value for each parameter.

---

### 🔁 Summary

> So, we use the **URLSearchParams API** to read query parameters in JavaScript.
> It's simple, built-in, and works directly on the URL. This is helpful in real-world projects when we want to personalize pages based on the URL or fetch filtered results.

---

## 💬 Final Tip for Interview Speaking

When you forget something during an interview, it’s better to calmly say:

> “I’m forgetting the exact method right now, but I believe we use something like `URLSearchParams` on `window.location.search` to extract query values. I’d be happy to check or demo it live.”

## Would you like me to make a short **audio script** for this answer so you can rehearse it aloud just like in an interview?

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

<!-----

  ---------52--------

--- -->

52)How to do form validations make notes on it you know it just speak in your words and match with chatgpt ?

<!-----

  ---------53--------

--- -->

## 53. How does JavaScript handle asynchronous code?

---

### 🔍 **Need**

In modern web applications, JavaScript often needs to handle **tasks like fetching data** from a server, reading files, or waiting for user input. Since these tasks can take time, we **can't let the program freeze** waiting for them to complete.  
JavaScript handles this situation by using **asynchronous programming**, allowing the program to continue running while waiting for a task to finish.

---

Note ---
`No callback = no action, but it does not cause the code to block. Missing a callback doesn't make the code synchronous or blocking, it just means the event or timeout won't trigger any specific action`

**Blocking occurs only with synchronous code**, such as an **infinite loop**, **`prompt()`**, or **`alert()`**, which **pause the execution of the code** until that specific line or operation is completed. On the other hand, **asynchronous code** (like **`setTimeout()`**, **`fetch()`**, or event listeners) is **non-blocking**, meaning it allows the program to continue executing other tasks while waiting for an operation to finish.

---

---

### 📖 What is it

JavaScript handles **asynchronous code** by allowing some operations to run **in the background**, without blocking the main thread. This is crucial for tasks like fetching data, timers, or handling UI events, ensuring that the user experience isn’t interrupted.

JavaScript provides **three main approaches** for handling asynchronous operations:

1. **Callbacks**: Functions passed into other functions that get executed once an asynchronous task finishes.
2. **Promises**: A **Promise** is an object that holds the response coming from a future value, like the response coming from a server when we call the `fetch` method with a URL.and we get in return a promise that will either be **fulfilled** or **rejected** based on the response coming from the server .

3. **Async/Await**: Syntactic sugar over promises, making asynchronous code look and behave more like synchronous code.

---

### 🛠️ How to implement

### 📺 Sir, can I share my screen to show this with an example?

#### 1. **Callbacks**

```js
setTimeout(() => {
  console.log("This is a callback!");
}, 1000); // Will run after 1 second
```

#### 2. **Promises**

```js
const myPromise = new Promise((resolve, reject) => {
  const success = true;
  if (success) {
    resolve("Task completed successfully!");
  } else {
    reject("Task failed.");
  }
});

myPromise
  .then((result) => console.log(result)) // Success
  .catch((error) => console.log(error)); // Failure
```

#### 3. **Async/Await**

```js
const fetchData = async () => {
  let data = await fetch("https://api.example.com/data");
  let jsonData = await data.json();
  console.log(jsonData);
};

fetchData();
```

---

EXAMPLE 2 ----(MY PRACTISE)

```js
// Callback Example
setTimeout(() => {
  console.log("Callback: Data fetched");
}, 2000);

// Promise Example
const dataPromise = new Promise((resolve) => {
  setTimeout(() => resolve("Promise: Data fetched"), 2000);
});
dataPromise.then(console.log);

// Async/Await Example
const fetchData = async () => {
  const result = await new Promise((resolve) =>
    setTimeout(() => resolve("Async/Await: Data fetched"), 2000)
  );
  console.log(result);
};
fetchData();
```

---

### Summary

- **Callbacks**: Handled by passing functions to be executed later, but can lead to **callback hell** if nested deeply.
- **Promises**: Handle asynchronous flow using `.then()` and `.catch()`, making the code more readable.
- **Async/Await**: Makes promises behave like synchronous code, providing a cleaner syntax.

> **Pro Tip**: **Async/Await** is the most modern and preferred way for handling asynchronous code due to its simplicity.

---

Example 2

```js
const handleFunction = async function () {
  try {
    const data = await new Promise((resolve, reject) => {
      setTimeout(function () {
        // resolve("Hello Jaanu");
        reject("bye jaanu");
      }, 2000);
    });

    return data;
  } catch (err) {
    // console.log(err);
    return err;
  }
};

const handleValue = async function () {
  try {
    const val = await handleFunction();
    console.log(val);
  } catch (err) {
    console.log(err);
  }
};
// console.log(handleValue())
handleValue();
console.log("hello late hogya");
```

---

<!-----

  ---------54--------

--- -->

54. What is the difference between type coercion and type conversion ?

<!-----

  ---------55--------

--- -->

## 55) What is the difference between Pass-by-Value and Pass-by-Reference?

---

### ✅ **Similarity First**

## Both Pass-by-Value and Pass-by-Reference are **ways of passing data** into a function in JavaScript — whenever we pass a variable (like a number, string, object, or array), JS needs to decide whether it's passing a **copy of the value** or a **reference to the original memory**.

### 🔄 **Difference**

Now here’s the **main difference** between the two:

---

1. **Pass-by-Value**
   - Happens with **primitive types** (like `Number`, `String`, `Boolean`, `undefined`, `null`, `Symbol`, `BigInt`) so when we pass a primitive data type to a function
   - A **copy of the original value** is passed to the function. So changes made inside the function do **not affect** the original variable. This type of copy is known as deep copy .
   - ✅ Example: It's like giving someone your notes, and they create their own notes by copying yours. but Any changes they make to their notes will not affect your original notes.

---

2. **Pass-by-Reference**
   While pass reference Happens whenver dealing with **non-primitive types** (like `Object`, `Array`, `Function`)cause instead of its value
   - A **reference to the original object** is passed. So if the function changes the object, the changes are reflected in the original object also. This type of copyis known as shallow copy as only the reference is copied instead of copying the entire value.
   - ✅ Example: Its like giving someone keys to your house and when some one go to your location in this case my house and do some changes this changes will show to my house because they have done changes in my house.

---

### 📺 Sir, can I share my screen to show this with an example?

```js
// 🔹 Pass-by-Value
let a = 10;
function update(x) {
  x = x + 5;
}
update(a);
console.log(a); // 👉 10 (original not changed)

// 🔹 Pass-by-Reference
let person = { name: "John" };
function rename(obj) {
  obj.name = "Doe";
}
rename(person);
console.log(person.name); // 👉 "Doe" (original object changed)
```

---

**Solution**: --

In order to deal with shallow copy in Objects in javascript we have some ways

1. json.stringify and json.parse

2. structuredClone() // note this is a global method.

3. - **Spread Syntax**: Creates a shallow copy of the original object, allowing you to work with a new object without modifying the original one. But this only work for normal objects and fails for the nested object as spread syntax also do shallow copy .

- **Example**:
  ```javascript
  let obj = { name: "Kevin" };
  let copy_obj = { ...obj };
  copy_obj.name = "Austin";
  console.log(obj.name); // Output: Kevin
  console.log(copy_obj.name); // Output: Austin
  ```

---

```js
const obj1 = { arun: 1, boy: { cat: 2 } };

// Shallow Copy using spread
const shallow = { ...obj1 };

// Deep Copy using JSON
const deep = JSON.parse(JSON.stringify(obj1));

// Deep Copy using structuredClone (modern way)
const deepModern = structuredClone(obj1); // THIS IS A GLOBAL method not method of any object or array so use like this only

shallow.boy.cat = 100;
console.log(obj1.boy.cat); // 100 (shallow copy affected original)

deep.boy.cat = 200;
console.log(obj1.boy.cat); // 100 (deep copy didn’t affect original)

deepModern.boy.cat = 300;
console.log(obj1.boy.cat); // 100 (structuredClone also didn’t affect original)
```

<!-----

  ---------56--------

--- -->

56. What are JavaScript currying functions?

Ans :---

### 🔍 **Need**

In many real-world scenarios, we don’t always have **all the data at once**. We might want to build a function in such a way that:

- We **pass arguments one by one**,
- And **reuse** the same function for multiple use cases.

Also, breaking functions into smaller steps improves **code reusability**, **readability**, and supports concepts like **partial application**. That’s where **currying** helps.

---

### 📖 What is Currying?

**Currying** is a functional programming technique in JavaScript where:

- Instead of taking **all arguments at once**, a function takes **one argument at a time**.
- Each function returns another function, until all arguments are provided.

> ✅ A curried function **remembers** the previous arguments via **closures** and keeps returning new functions until it has everything it needs.

---

### 🛠️ How to implement Currying

### 📺 Sir, can I share my screen to show this with an example?

- I’ll show the difference between normal and curried functions.
- Then I’ll show how you can use currying to create **reusable filters** or **logger functions**.

Let’s say you want to add 3 numbers — a normal function would look like:

```js
function add(a, b, c) {
  return a + b + c;
}
console.log(add(1, 2, 3)); // 6
```

Here’s a **curried version**:

```js
function curriedAdd(a) {
  return function (b) {
    return function (c) {
      return a + b + c;
    };
  };
}

console.log(curriedAdd(1)(2)(3)); // 6
```

You can also write this with arrow functions:

```js
const curriedAdd = (a) => (b) => (c) => a + b + c;
```

<!-- Step 1 (by using clousres) -->

### Example code of Infinite currying ( this uses recursion)

eg curriedAdd()()()().....

```js

```

## <!-- Step 2 (by using bind method) -->

### ✅ Pro Tip:

- **Currying is especially useful in React**, Redux, and libraries like Lodash or Ramda.
- It allows you to create **customized versions of functions** for different needs by **pre-filling arguments**.

---

<!-----

  ---------57--------

--- -->

57. what is a callback hell?

Ans :---

### 🔍 **Need**

In JavaScript, when we deal with **asynchronous operations** (like fetching data, or using listeners and timeouts),
and To handle these async tasks, we have three ways

1. using a callback function
2. using promises
3. and using async/await.

So when we use a callback function it means that we are passing a function insie another higher order function But if we have **many async tasks** that depend on each other and each one is inside another callback —
it creates a **deep nesting structure** and that is known as callback hell .

---

### 📖 What is Callback Hell?

**A Callback Hell** refers to a situation when there are **multiple nested callbacks**, which results in complex hard to read code and hard to debug code .This deeply nested code often results in a triangular or pyramid-like structure, which is commonly known in programming as the **“pyramid of doom”** .

---

### 🧠 Why it’s bad:

- ❌ Hard to **understand** the flow of logic
- ❌ Difficult to **handle errors**
- ❌ Not **scalable** — if the logic grows, so does the nesting

---

### 📺 Sir, can I share my screen to show this with an example?

Sure! Here's how you can change your example to use `setTimeout` for simulating asynchronous behavior and demonstrate **Callback Hell**:

### Example of Callback Hell with `setTimeout`:

```js
// Simulating a series of asynchronous tasks with setTimeout
setTimeout(function () {
  console.log("Task 1 completed");

  setTimeout(function () {
    console.log("Task 2 completed");

    setTimeout(function () {
      console.log("Task 3 completed");

      setTimeout(function () {
        console.log("Task 4 completed");
      }, 1000);
    }, 1000);
  }, 1000);
}, 1000);
```

### Visualizing it:

```txt
setTimeout
  ↳ setTimeout
      ↳ setTimeout
          ↳ setTimeout
              ↳ console.log
```

This **deep nesting** is Callback Hell.

---

### 💡 Pro Tip:

- **Callback hell = Bad structure**, not callbacks themselves.
- Callbacks are fine when shallow — avoid nesting.
- Prefer **Promises or async/await** in modern JavaScript for **clean and readable async code**.

---

> 👉 Callback Hell = Nested callbacks inside callbacks, leads to unreadable and unmaintainable code.

---

<!-----

  ---------58--------

--- -->

## 58. What is the difference between arrow function and normal function ?

Ans :--

### ✅ **Similarity first**

Both **arrow functions** and **normal functions** in JavaScript allow you to define functions, and they can be used for performing tasks like calculations, manipulating data, or handling events. They both are function definitions, but the key difference lies in **how they handle certain things**, particularly **`this`** and how they are written.

---

### 🔄 **But there are some key differences between them:**

---

1. **The first major difference is their syntax.**

   - **Arrow function** has a **shorter syntax**, which makes it more concise:

     ```js
     const add = (a, b) => a + b;
     ```

   - **Normal function** uses the traditional `function` keyword:

     ```js
     function add(a, b) {
       return a + b;
     }
     ```

---

2. **Secondly, their behavior with `this` is different.**

   - **Arrow functions** do **not have their own `this`**. They **lexically inherit `this`** from the surrounding scope, meaning `this` inside an arrow function refers to the `this` of its surrounding context.

     ```js
     const person = {
       name: "Alice",
       greet: () => console.log(this.name), // `this` doesn't refer to `person` here
     };
     person.greet(); // undefined (because `this` refers to the global scope)
     ```

   - **Normal functions** **have their own `this`** and it refers to the object or context from which they are called.

     ```js
     const person = {
       name: "Alice",
       greet: function () {
         console.log(this.name);
       },
     };
     person.greet(); // "Alice" (because `this` refers to `person`)
     ```

---

3. **Third, their usage in `constructor functions` differs.**

   - **Arrow functions** **cannot be used as constructor functions**. They do not have their own `this`, so they cannot be invoked with `new`.

     ```js
     const Person = (name) => {
       this.name = name; // `this` doesn't work here
     };
     const person = new Person("Alice"); // TypeError: Person is not a constructor
     ```

   - **Normal functions** **can be used as constructor functions**. When called with `new`, they create new objects.

     ```js
     function Person(name) {
       this.name = name;
     }
     const person = new Person("Alice");
     console.log(person.name); // "Alice"
     ```

---

4. **Also, arrow functions** **cannot have their own `arguments` object**. They inherit the `arguments` object from the outer function scope.

   - **Normal functions** have their own `arguments` object, which is an array-like object containing all the passed parameters.

     ```js
     function normalFunction() {
       console.log(arguments);
     }
     normalFunction(1, 2, 3); // [1, 2, 3]
     ```

     Arrow functions do not have `arguments`, and trying to use it inside an arrow function will give an error:

     ```js
     const arrowFunction = () => {
       console.log(arguments); // ReferenceError: arguments is not defined
     };
     arrowFunction(1, 2, 3);
     ```

---

### 📺 Sir, can I share my screen to show this with an example?

#### Example of Arrow Function vs Normal Function

```js
// Arrow function example
const greetArrow = () => console.log("Hello from Arrow Function");
greetArrow(); // "Hello from Arrow Function"

// Normal function example
function greetNormal() {
  console.log("Hello from Normal Function");
}
greetNormal(); // "Hello from Normal Function"
```

---

### ✨ Final Summary:

- **Arrow functions** are concise, **don’t have their own `this`**, **cannot be used as constructors**, and **cannot access `arguments`**.
- **Normal functions** have their own `this`, can be used as constructors, and have access to the `arguments` object.

---

> 👉 The key difference is:
> **Arrow functions** — concise, lexically bound `this` > **Normal functions** — traditional, have their own `this`

---

Shall I move to the next question?

---Perfect, Vipul! Since this is a **difference-type question**, I’ll answer it in your **Type 2 format** — with similarities, differences, and examples.

---

<!-----

  ---------25--------

--- -->

## 25) What is the difference between Arrow Function and Normal Function in JavaScript?

---

### ✅ **Similarity first**:

Both **arrow functions** and **normal functions** are used to **declare functions** in JavaScript, and both can be used to:

- Accept parameters
- Return values
- Be assigned to variables
- Be passed as arguments or returned from other functions

---

### 🔄 **But there are some key differences between them**:

---

### 1. **Syntax and Clean Code**

**Arrow Function:**

- Shorter and more concise syntax
- Great for writing **small callbacks or one-liners**

```js
const add = (a, b) => a + b;
```

**Normal Function:**

- More traditional and flexible syntax
- Useful when you need **more control**, like using `this`, `arguments`, or hoisting

```js
function add(a, b) {
  return a + b;
}
```

---

### 2. **`this` Binding**

This is the **biggest difference**:

**Arrow Function:**

- **Does not have its own `this`** — it uses the `this` from the surrounding scope (lexical scoping)
- Commonly used in React or callbacks to avoid binding issues

**Normal Function:**

- **Has its own `this`** context
- `this` depends on how the function is called (can be unpredictable)

```js
const obj = {
  name: "Vipul",
  arrowFn: () => console.log(this.name), // undefined
  normalFn() {
    console.log(this.name);
  }, // "Vipul"
};
obj.arrowFn();
obj.normalFn();
```

---

### 3. **`arguments` Object**

**Arrow Function:**

- **Does not have** its own `arguments` object

**Normal Function:**

- Has access to the **`arguments` object**, useful when handling unknown number of inputs

```js
function test() {
  console.log(arguments);
}
test(1, 2); // [1, 2]

const testArrow = () => {
  console.log(arguments);
};
testArrow(1, 2); // ❌ Error: arguments is not defined
```

---

### 4. **Can Be Used as Constructor?**

**Arrow Function:**

- ❌ **Cannot be used as constructors**
- Will throw error if used with `new`

**Normal Function:**

- ✅ Can be used with `new` to create object instances

```js
function Person(name) {
  this.name = name;
}
const p = new Person("Vipul"); // Works

const PersonArrow = (name) => {
  this.name = name;
};
// new PersonArrow("Vipul"); ❌ Error
```

---

### 5. **Hoisting Behavior**

**Arrow Function:**

- **Not hoisted**. You must declare it before use.

**Normal Function:**

- ✅ **Hoisted** to the top of its scope. You can call it before its definition.

```js
greet(); // Works
function greet() {
  console.log("Hello");
}

sayHi(); // ❌ Error
const sayHi = () => console.log("Hi");
```

---

### 📺 Sir, can I share my screen to show both functions in action?

```js
// Normal function
function multiply(a, b) {
  return a * b;
}

// Arrow function
const multiplyArrow = (a, b) => a * b;

console.log(multiply(2, 3)); // 6
console.log(multiplyArrow(2, 3)); // 6
```

---

### 🔚 In Conclusion:

| Feature             | Arrow Function                        | Normal Function                      |
| ------------------- | ------------------------------------- | ------------------------------------ |
| `this`              | Lexical `this` (inherits from parent) | Own `this` (dynamic based on caller) |
| `arguments` object  | ❌ Not available                      | ✅ Available                         |
| Used as constructor | ❌ Not possible                       | ✅ Possible                          |
| Hoisting            | ❌ Not hoisted                        | ✅ Hoisted                           |
| Syntax              | Concise                               | Verbose but flexible                 |

---

> ✅ **Use arrow functions** for short callbacks and when you want to avoid `this` confusion.
> ✅ **Use normal functions** when you need `this`, `arguments`, or to define methods inside classes or objects.

---

Ready for the next one, Vipul?

---

<!-----

  ---------58--------

--- -->

## 26) What is **Prototype** in JavaScript?

---

### 🔍 **Need**

In JavaScript, we often create **multiple objects** that share **common properties or methods**.

But if we define the same method inside each object, it leads to **code duplication** and **waste of memory**.

✅ That's where the **Prototype** helps.
It allows us to **share methods and properties** between objects efficiently.

---

### 📖 **What is Prototype?**

In JavaScript, every function and object has a hidden property called `[[Prototype]]`, which can be accessed using:

```js
__proto__; // old way
Object.getPrototypeOf(obj); // preferred modern way
```

When you access a property or method on an object, JavaScript looks:

1. Inside the object itself.
2. If not found, it goes up the **prototype chain** to look into its prototype.

---

### 🧠 Think of it like this:

> A prototype is like a **backup object** — if JavaScript doesn't find something in the object, it looks inside its prototype.

---

### 👨‍🏫 Real-world Analogy:

Imagine you’re a student and you don’t know the answer to a question.
But your **teacher (prototype)** does.
So, you ask your teacher (i.e., the prototype chain resolves the missing property).

---

### 🔧 Example:

```js
function Person(name) {
  this.name = name;
}

// Adding method to prototype
Person.prototype.sayHello = function () {
  console.log(`Hello, my name is ${this.name}`);
};

const p1 = new Person("Vipul");
const p2 = new Person("Rahul");

p1.sayHello(); // Hello, my name is Vipul
p2.sayHello(); // Hello, my name is Rahul
```

✔️ `sayHello()` is not copied to every object.
✔️ It's shared via the prototype — **memory efficient**.

---

### 🔄 Prototype Chain:

```js
p1.hasOwnProperty("name"); // true (own property)
p1.hasOwnProperty("sayHello"); // false (from prototype)

console.log(p1.__proto__ === Person.prototype); // true
```

➡️ If property/method is not found in `p1`, JavaScript looks in `Person.prototype`, and then eventually up to `Object.prototype`.

---

### ✅ Pro Tip:

- Every JavaScript object is linked to a prototype object.
- This is how **inheritance** works in JavaScript.
- **Built-in objects** like `Array`, `Function`, and `Object` also have prototypes.

```js
const arr = [1, 2, 3];
console.log(arr.__proto__ === Array.prototype); // true
```

---

### 🔚 In Conclusion:

- Prototypes allow us to **share methods across objects** efficiently.
- JavaScript uses a **prototype chain** to look up properties and methods.
- It is the **backbone of inheritance** in JavaScript.

---

Would you like me to explain **prototype inheritance** next or something else?

<!-----

  ---------60--------

--- -->

## 60) How does the prototypal inheritance work in JavaScript?

Ans :--- Ans:-- So, **Prototypal Inheritance** in JavaScript is a way for objects to inherit properties and methods from other objects. Instead of using classes (like in Java or C++),
JavaScript uses **prototypes** to enable inheritance.

---

### 🔹 How does it work?

1️⃣ Every JavaScript object has a hidden property called **`[[Prototype]]`**, which refers to another object (its prototype).  
2️⃣ If we try to access a property or method that doesn't exist in the object, JavaScript automatically looks for it in the object's **prototype**.  
3️⃣ This lookup continues up the chain **until it reaches `null`**, which means the end of the prototype chain.

---

### 🔹 Example to understand it better:

Let’s say we have an object **`car`** with a method, and another object **`electricCar`** wants to use that method **without redefining it**.

1. First, we create a `car` object with a method.
2. Then, we create `electricCar` and set its prototype to `car`.
3. Now, `electricCar` can access methods from `car` because of prototypal inheritance.

---

### 🔥 Key Points

✅ Objects in JavaScript **inherit** from other objects, not classes.  
✅ The `__proto__` property (or `Object.getPrototypeOf()`) lets us see an object’s prototype.  
✅ This allows **method sharing** without duplicating code.  
✅ If JavaScript can’t find a property in the object itself, it **looks up the prototype chain** until it finds it or reaches `null`.

That’s how prototypal inheritance works! 🚀

---

<!-----

  ---------61--------

--- -->

## 61. Describe JavaScript Global execution context ?

Ans :--

## 28) What is the **Global Execution Context** (GEC) in JavaScript?

---

### 🔍 **Need to understand it first**

To understand how JavaScript **runs your code**, you must know how it **creates an environment** for execution.
Every time you run a JS program, it needs a **context** to manage memory, variables, and function calls.

That’s where the **Global Execution Context (GEC)** comes in.

---

### 🌐 **What is GEC?**

**Global Execution Context** is the **first execution context** created by JavaScript when your code starts running.

It is the base environment in which the **global code** runs — i.e., the code that is **not inside any function**.

---

### 🧠 Think of it like:

> You're setting up the **main room** before calling any function.
> That room has access to **everything globally declared** — like `var`, `function`, `console`, `window`, etc.

---

### ⚙️ Two phases of GEC

When JS creates the GEC, it runs in **two phases**:

#### 1. **Memory Creation Phase (Hoisting)**

- JavaScript scans the code.
- All `var` variables are stored with `undefined`.
- All function declarations are stored with their entire function definition.
- `let` and `const` are placed in the **temporal dead zone**.

#### 2. **Code Execution Phase**

- JS executes the code **line by line**.
- Assigns actual values to variables.
- Calls functions, creates new execution contexts if needed.

---

### 🖼️ Example:

```js
var x = 10;
function greet() {
  console.log("Hello");
}
greet();
```

During GEC creation:

| Memory Phase (Hoisting)  | Execution Phase        |
| ------------------------ | ---------------------- |
| x → undefined            | x = 10                 |
| greet → function() {...} | greet() → logs "Hello" |

---

### ✅ Key Features of GEC:

- Only **one GEC** is created per program.
- It forms the **base** of the **call stack**.
- It is where your **global variables** and **functions** live.
- `this` in GEC refers to **`window` (browser)** or **`global` (Node.js)**.

---

### 📌 Bonus: What happens after GEC?

- When a function is called, a **new execution context** is created for that function.
- These function execution contexts are **pushed onto the call stack**.
- When the function ends, its context is **popped off**, and control goes back to the GEC.

---

### 🧠 Interview Tip:

> ✅ "Every JavaScript program starts with one Global Execution Context, which handles global variables and functions. From there, function calls create their own local execution contexts, forming the execution stack."

---

Let me know if you want a **diagram** of the Call Stack with GEC and FEC!

---

<!-----

  ---------62--------

--- -->

## 62. What is the type of undefined and null?

Ans :--

Note --- ( `Remember this null === null (is true ) but NaN=== NaN is false (AND nan is the only value in javscript which is not equal to itsel(only primitive  value i mean))`)

Note -- type of NaN is number

---

## ✅ What is the type of `undefined` and `null` in JavaScript?

---

### 🔹 `undefined`:

- It means **a variable has been declared but not assigned any value yet**.
- JavaScript automatically assigns `undefined` to variables that are declared but not initialized.

```js
let x;
console.log(x); // undefined
```

👉 **Type of `undefined`** is:

```js
typeof undefined; // 🔁 "undefined"
```

✔️ So `undefined` is a **primitive type**.

---

### 🔹 `null`:

- It represents **intentional absence of any object value**.
- Often used to explicitly clear or reset a variable.

```js
let person = null;
```

👉 **Type of `null`** is:

```js
typeof null; // 🔁 "object" ❗ (this is actually a bug in JavaScript!)
```

> 📌 This is a **known bug** in JavaScript from its early days — `null` returns `"object"` even though it's not an object.

---

### ✅ Final Summary:

| Value       | Meaning                            | `typeof` result |
| ----------- | ---------------------------------- | --------------- |
| `undefined` | Variable declared but not assigned | `"undefined"`   |
| `null`      | Intentional absence of value       | `"object"` ❗   |

---

<!-----

  ---------63--------

--- -->

## 63. What is the process of **hoisting** for **normal** and **arrow** functions, and what are the differences between them?

Ans :--

### 🔍 First, let’s understand what **hoisting** is:

> **Hoisting** is JavaScript's behavior of moving **declarations** (variables and functions) to the top of their scope **before execution**.

But how hoisting works **differs** for different types of functions.

---

### 📌 1) **Normal Function Declarations** (✅ Fully Hoisted)

```js
sayHi(); // ✅ Works fine
function sayHi() {
  console.log("Hello!");
}
```

- Here, the **entire function** is hoisted, **including its body**.
- So you can call it **before it's defined**.

---

### ⚠️ 2) **Arrow Functions** (❌ Not fully hoisted)

```js
greet(); // ❌ TypeError: greet is not a function
const greet = () => {
  console.log("Hi!");
};
```

- Arrow functions are stored in a **variable**, and **only the variable declaration** is hoisted — **not the function body**.
- Until the line runs, the variable is in the **Temporal Dead Zone** (TDZ), so calling it before initialization throws an error.

---

### 🧠 What’s the core difference?

| Feature                  | Normal Function    | Arrow Function                                   |
| ------------------------ | ------------------ | ------------------------------------------------ |
| Hoisting behavior        | ✅ Fully hoisted   | ❌ Not fully hoisted                             |
| Can be called before?    | ✅ Yes             | ❌ No                                            |
| Type after hoisting      | Function           | `undefined` (for `var`) or TDZ (for `let/const`) |
| Context (`this` binding) | Has its own `this` | Inherits `this` from parent                      |

---

### ✅ Conclusion:

> - **Normal functions** are fully hoisted — can be safely called before their definition.
> - **Arrow functions** are **not hoisted like normal functions** — they're just variables, and cannot be used before their definition.

---

<!-- ------EXTRA PRACTISE QUESTION OF YOUTUBE------ -->

```JS

// Code to print a grid of the number
let count = 1;
let stringNo ="";

for(let i = 1 ; i<4 ;i++){

    for(let j = 1 ; j<4 ;j++){

    // console.log(count);
    stringNo+= `${count} `;
    // stringNo+= count + " ";
    count++;



    }
    console.log(stringNo);
    stringNo ="";
    // console.log("\n") ;

}

```
