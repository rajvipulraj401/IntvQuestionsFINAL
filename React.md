### note1 - **(NEED what and HOW ) bs isi trh bologe tum humesha:------**

Note 2 \*HOW TO deal with question you don't know completely ?
--- Pehle bolo phir ye last me bolo --- ( how to say no to a question)
Ans :- Sir ,This is what i know at the moment and i am not exactly sure if i am explaining it correctly but i would love to get back to this question right after the interview .

note 2.1 ) How to deal when you completely dont know ?
Ans :- Sir currently i am not able to come up with the right answer to this question but i would love to get back to this question right after this interview

# --------------------- Follow Need what HOW ?-------------

## **(A)** Basic and core cocncept (_aSK on 16th april_)

### Q1) What is React?

**Ans :--**

---

**Need (Why do we need React?)**

When we build small websites, HTML, CSS, and JS (or even jQuery) are enough.
But when the application becomes large and complex, these traditional methods become harder to manage like we have to create same kind of ui again and again and creating that kind of website using core technologies becomes very messy and it is even harder to maintain.
So thats why we have front end library and framework and one such library is react .

**What (What is React?)**----

So, React is an open source front end **JavaScript library** which is used to build **user interfaces**, especially for **single-page applications**. It is helpful
in building complex application as it follows the component based approach and divides the whole page into small reusable components and makes it **easy to update just the parts that changes** without refreshing the whole page.

Some key features of react are :-

1. React uses jsx syntax (whuch combines js and Html)
2. It uses virtual dom instead of Real DOM
3. It follows unidirectional from paret to child which simplify the data management.
4. It supports server side rendering which is useful for Seo.

---

## 📺 Sir can I share my screen to show this with an example

🖥 _Let me share my screen and show you how a simple React component looks like:_

```jsx
// App.js
import React from "react";

const App = () => {
  const name = "React";

  return (
    <>
      <h1>Hello {name}!</h1>
      <p>This is a basic React component using JSX.</p>
    </>
  );
};

export default App;
```

<!-- ---

--------------------------------2-----

--- -->

### Q2) What is JSX?

Ans :--

---

**Need (Why do we need JSX?)**

whenever we build React apps, we need to mix **HTML and JavaScript** to show dynamic data in the UI.  
and earlier we had to do that using `document.createElement()` which was **complex and less readable** . So inorder To solve this problem, **React introduced JSX** .

---

**What (What exactly is JSX?)**

JSX stands for **JavaScript XML**. It allows us to write HTML-like code inside JavaScript and place them in the Dom without using functions like **append child** or **create element**
Basically it just provide us the syntatic sugar for the `react. createElement (types, props , ..children)` and it makes the code more readable and expressive by combining JavaScript expressions
with an HTML-like template syntax .

`EXTRA dont speak`
But JSX doesn’t work directly in the browser — React converts it behind the scenes to `React.createElement()` calls.
In short — JSX makes React code **look like HTML**, but it’s still JavaScript.

---

**How (How do we use JSX and what are the rules?)**

some important **rules** OF JSX that we need to follow are:

1. **All JSX tags must be closed**, even self-closing ones.

for eg:--

```jsx
<img src="logo.png" /> // ✅ valid in JSX
```

2. **All Attribute nameing should be in camelCase**.

   - Use `className` instead of `class`
   - Use `onClick` instead of `onclick`

3. **Use curly braces `{}` to write JS expressions inside JSX**.

   ```jsx
   const name = "React";
   <h1>Hello {name}</h1>;
   ```

4. **JSX should only return one parent element so Wrap multiple elements inside one parent** (either a `<div>` or a React fragment `<>...</>`).
   ```jsx
   return (
     <>
       <h1>Hello</h1>
       <p>World</p>
     </>
   );
   ```

---

## 📺 Sir can I share my screen to show this with an example

🖥 Sir let me share my screen and show a small example of how JSX works in React.

```jsx
// App.js
import React from "react";

const App = () => {
  const username = "Crio Learner";

  return (
    <>
      <h1>Hello {username}</h1>
      <p>This is JSX in action inside a React component.</p>
    </>
  );
};

export default App;
```

<!-- ---

--------------------------------3-----

--- -->

### Q3) What is Virtual DOM in React?

Ans :--

---

when we make any web application using the core technologies and in the websites there are many parts that keep changing — like when we type, click buttons, or get new data from the server.then for the websites created using just the core-technologies re -renderes the DOM for every small changes we do in our ui and the whole page is painted again and again so in turn it makes our big application **slow and inefficient**
and in order To solve this problem, React team introduced the concept of **Virtual DOM**.

---

**What (What exactly is Virtual DOM?)**

Virtual DOM is a **lightweight in-memory virtual representaion of the real Dom** . (it's not actual copy of DOM ) .
It is kept inside the memory and it is synced with the real DOM ( by a library called react DOM).

---

**How (How does React use Virtual DOM?)**

Now let's understand how this exactly works .

1. When state or props of our component changes then react creates a new Virtual DOM in memory and then it compares it with the old virtual dom adn finds the difference part of it
2. and then instead of re -rendering the entire DOM react only updates the difference part inside the real dom.
3. This comparison of old and new version of virtual Dom is called **diffing** which is short for Diffing algoritm
   and This whole whole process is known as **Reconciliation process**.

   and using this process we **efficiently and quickly update our web applications** which makes our app **fast and smooth**.

---

## 📺 Sir can I share my screen to show this with an example

🖥 Sir let me share my screen and show how React uses Virtual DOM in action.

```jsx
// App.js
import React, { useState } from "react";

const App = () => {
  const [count, setCount] = useState(0);

  return (
    <>
      <h1>Counter: {count}</h1>
      <button onClick={() => setCount(count + 1)}>Increment</button>
    </>
  );
};

export default App;
```

In this example, when we click the button:

- Only the `<h1>` tag gets updated,
- React does not reload or re-render the full page.
- This is because of Virtual DOM and the efficient update it handles behind the scenes.

<!-- ---4--------

--- -->

4. What is the difference between Virtual DOM and Real DOM in React?

Ans :--

1. DOM stands for Document Object Model, and it is a tree-like structure that the browser creates from an HTML page. For example, when we create any element in HTML, that element becomes a part of this DOM tree.
   while the virtual dom is a lightweight in-memory representation of the real dom It is only kept inside the memory and is synced with the real dom .

2. Also when we update the dom directly it is actually very slow as the browser needs to re-render the entire DOM tree On the other hand, updating the Virtual DOM is much faster because React only updates the parts that have actually changed — this process is called reconciliation. which uses the diffing algorith to compare the two virtual dom and only updates the real dom with the change part.

3. The third difference is that we can directly manipulate the Real DOM using JavaScript do crud operation in dom (like adding, removing, or updating elements). But we cannot directly change the Virtual DOM — it is managed internally by React using the **react-dom** library.

<!-----

  ---------5--------

--- -->

### Q5) What is Reconciliation in React?

Ans :--

---

**Need (Why do we need Reconciliation?)**

In React apps, when data changes (like state or props), the UI should also update.  
But we don’t want to update the whole page unnecessarily and re-render the enire dom and in order to prevent that we have a process in react known as reconcilliation process.

---

**What (What exactly is Reconciliation?)**

**Reconciliation** is the process by which React **compares the old Virtual DOM with the new Virtual DOM**, and it finds the actual difference to update in ral dom , and then updates only those changed parts in the real DOM.

---

**How (How does Reconciliation work?)**

Now let's understand how this exactly works .

1. When state or props of our component changes then react creates a new Virtual DOM in memory and then it compares it with the old virtual dom adn finds the difference part of it
2. and then instead of re -rendering the entire DOM react only updates the difference part inside the real dom.
3. This comparison of old and new version of virtual Dom is called **diffing** which is short for Diffing algoritm
   and This whole whole process is known as **Reconciliation process**.

   and using this process we **efficiently and quickly update our web applications** which makes our app **fast and smooth**.

---

🧠 Extra Point (for follow-up or bonus)

React uses **keys** (especially in lists) to help in reconciliation. Keys help React identify which items changed, added, or removed.

---

## 📺 Sir can I share my screen to show this with an example?

```jsx
// App.js
import React, { useState } from "react";

const App = () => {
  const [count, setCount] = useState(0);

  return (
    <>
      <h1>Count: {count}</h1>
      <button onClick={() => setCount(count + 1)}>Increment</button>
      <h2> hello World </h2>
    </>
  );
};

export default App;
```

In this example:

- Every time we click the button, React creates a new virtual DOM.
- It compares it with the old one.
- Finds that only the `<h1>` text changed.
- So it updates only that part — not the whole page.

This is how reconciliation process keeps Application made in React fast and efficient 🔥

---

<!-----

  ---------6--------

--- -->

6. What is the need of ReactJS if we already have HTML, CSS, JS, or jQuery?

Ans :---

When we build small websites, HTML, CSS, and JS (or even jQuery) are enough.
But when the application becomes large and complex, these traditional methods become harder to manage like we have to create same kind of ui again and again and creating that kind of website using core technologies becomes very messy and it is even harder to maintain.
So thats why we have front end library and framework and one such library is react .

Some key features of react are :-

1. React uses jsx syntax (whuch combines js and Html)
2. It uses virtual dom instead of Real DOM .
3. It follows unidirectional from paret to child which simplify the data management.
4. It supports server side rendering which is useful for Seo.
5. It make use of reusable component instead of creating same component again and again we can make use of one
   component and pass props to make it change little bit or even use children props to make that component as a wrapper.

6. It provides hooks to manage state management in react and it is very easy to do that in react as compare to in core technologies.

Your answer is good and has the right intention! You're explaining **why React is useful** when HTML, CSS, JS, or jQuery aren't enough. But to make it more **polished, professional, and interview-ready**, let's clean it up a bit — while keeping your conversational style intact.

---

`Extra DO NOT say`

1. **JSX Syntax**

   - React uses JSX, which allows us to write HTML-like code inside JavaScript. It makes the code easier to read and write, especially for building UI components.

2. **Virtual DOM**

   - React uses a virtual DOM to efficiently update only the parts of the UI that change, instead of re-rendering the entire page like traditional methods.

3. **Component-Based Architecture**

   - Instead of writing the same HTML again and again, we can create **reusable components** and use them wherever needed. We can pass **props** to customize them or even use **children** props to make wrapper components.

4. **Unidirectional Data Flow**

   - React follows a one-way data binding (from parent to child), which makes the data flow predictable and easier to debug.

5. **State Management with Hooks**

   - Managing state is much easier in React using **Hooks** like `useState`, `useEffect`, etc. This simplifies logic that would otherwise be complex in plain JS or jQuery.

6. **Support for Server-Side Rendering (SSR)**
   - With frameworks like Next.js (built on React), we can enable SSR which helps in better SEO and performance.

---

### 🧠 Summary:

React is needed not because HTML/CSS/JS are not capable — but because **React makes it easier to manage and scale modern web applications** with better structure, performance, and maintainability.

---

<!-----

  ---------7--------

--- -->

## Q7) what is a singlepage application ?

Ans:--

## **Need? ---**

whenever we build a website or a project, we need to implement multiple pages. Usually, websites have different sections, like in a **navbar**, where we see different options linking to various pages.
and In a traditional **Multi-Page Application (MPA)**, clicking on a link reloads the entire page, which slows down performance. This happens because every time we navigate to a different page, the browser fetches and loads a completely new HTML file.

This makes our application slower and in order to solve this, **Single Page Applications (SPAs)** were introduced .

## **What is an SPA?**

A Single Page Application is a web application where we have only **one main HTML file**, and all other content is dynamically loaded inside it without refreshing the page.

So, instead of loading new HTML pages from the server, it uses JavaScript (React, Angular, etc.) to dynamically update specific sections, which makes our app faster.

## **How do we handle multiple pages inside an SPA?**

So in order to achieve routing inside our spa we use **React Router** , which is a library in React that allows us to create multiple sections (or views) within the same page. like for example we have a navbar and we have different pages linked inside our navbar and we can then make use of react router library and define all the application inside the **<>Browser Router** component provided by React router and then make use of **Routes and Route component**
and specify the Route we want to link our component and using the **<Link>** component we can link our component to different pages and it does not reload our whole page **like anchor tag <a>** instead , it just updates the view by changing the route.

So this way we just make use of Single page application with just one html file and still have multiple pages linked to our single page application.

---

## 📺 Sir can I share my screen to show this with an example?

```jsx
// App.js
import { BrowserRouter, Routes, Route, Link } from "react-router-dom";

const Home = () => <h2>Home Page</h2>;
const About = () => <h2>About Page</h2>;

function App() {
  return (
    <BrowserRouter>
      <nav>
        <Link to="/">Home</Link> | <Link to="/about">About</Link>
      </nav>

      <Routes>
        <Route path="/" element={<Home />} />
        <Route path="/about" element={<About />} />
      </Routes>
    </BrowserRouter>
  );
}
```

> When you click “About”, React loads the new component **without reloading the page** — that’s a SPA behavior.

---

<!-----

  ---------8--------

--- -->

### **2️⃣ Difference between SPA vs Traditional Multi-Page Application (MPA) is that **

🔴 **in Traditional Multi-Page Application (MPA)**

- Every interaction (e.g., clicking a link) **triggers a full-page reload** from the server.
- and hence the application becomes Slower because the entire page reloads every time.

✅ **while in Single Page Application (SPA)**

- Only **relevant content** gets updates, and not the whole page is updated hence it makes our application Faster and gives smooth user experience.

---

### **3️⃣ some Examples of webiste made from SPAs are**

- Gmail
- Facebook
- Twitter etc

--- IntvAns ends here ----------------------------------------

### **4️⃣ Benefits of SPAs**

✔ **Faster Performance** – No full-page reloads, only necessary data updates.  
✔ **Better User Experience** – Feels more like a mobile app.  
✔ **Reduced Server Load** – Fewer requests since only data is fetched, not entire pages.

---

### **5️⃣ Drawbacks of SPAs**

❌ **SEO Challenges** – Since content is loaded dynamically, search engines may struggle to index it.  
❌ **Initial Load Time** – The first load can be slow because all scripts are downloaded at once.  
❌ **Browser Back/Forward Issues** – Requires extra handling for navigation since the page doesn’t reload.

---

<!--------------------------

  -----------------------------------SECTION B-----------------------------  (ask on 17th ,18th april) 7pm

--- ----------------------------->

## **(b)** _Class-based Components (Legacy React)_

## Q8) What is `super` in class components in ReactJS?

Ans :------

### #✅ **Need (Why do we use `super`?)**

When we create a class component in React, it extends from `React.Component` , which means our class inherits methods and properties from `React.Component`. So to properly initialize this inheritance, we need to call the parent class's constructor using `super() keyword`.

---

### #**What is `super`?**

`super` is a method in JavaScript that is used to **call the constructor of the parent class**. In the case of React class components, `super` method is used inside the constructor to call the constructor of `React.Component` which itself is a class and we want to inherit its property, which will enable us to access the `this` keyword and initialize state and props correctly to our component.

If we don’t do that, we’ll get an error — and we won’t be able to use `this.props` or set the state properly.

---

### #**How is `super` used?**

In a React class component, the `super()` method must be called before using `this keyword` inside the constructor. If we need to access `this.props` inside the constructor, we must call `super(props) method` to initialize the component properly.

---

### 📺 Sir can I share my screen to show this with an example?

#### **Example – Using `super` in a Class Component**

```jsx
import React, { Component } from "react";

class MyComponent extends Component {
  constructor(props) {
    super(props); // Calling parent constructor
    this.state = { message: "Hello, World!" };
  }

  render() {
    return <h1>{this.state.message}</h1>;
  }
}

export default MyComponent;
```

#### **4) Explanation of the Example**

- We **extend `React.Component`** → So we must call `super()`.
- If we use `this.state` inside the constructor, we need `super()` first.
- If we need to access `this.props` inside the constructor, we must use `super(props)`.

---

**Extras :---**

#### ✅ **What happens if we don’t use `super()`?**

If we try to use `this keyword` before calling `super() method`, React will throw an error:  
❌ **"Must call super constructor in derived class before accessing 'this' or returning from derived constructor"**

---

#### ✅ **Conclusion**

In short, `super method` is essential in React class components to call the parent class (`React.Component`) constructor and properly initialize the component before using `this`keyword and setting the state of the new component.

---

<!-----

  ---------9--------

--- -->

## 9. What are the lifecycle methods in React?

Ans:--

### **Need? -----------**

In React, components go through a series of stages during their life cycle — from creation to removal. and These stages require different actions to be taken, like fetching data or updating the UI. So in order to manage these stages React provides us **lifecycle methods** , which heps us to control the component behavior during its life.

### **What are Lifecycle Methods? -----------**

Component life cycle method refers to the different stages or phases a component has to go throughout its lifetime.

The component life cycle method can be broken down into three parts:

1. **Number one is mounting** – Mounting occurs when the component is first rendered to the DOM. Life cycle methods like `componentDidMount` are executed during this phase.

2. **Second is updating phase** – This phase occurs when the component is re-rendered or updated either when the **state or props** of the component changes.

   - This phase includes lifecycle methods such as `shouldComponentUpdate`, `render`, and `componentDidUpdate`.

3. **Lastly, we have the unmounting phase** – This phase occurs when the component is removed from the DOM, and this phase includes lifecycle methods like `componentWillUnmount`.

### 🧠 Functional Components Note:-------

Functional components do not have traditional lifecycle methods. Instead, they use the **`useEffect()`** hook to handle side effects and lifecycle behavior like mounting, updating, and unmounting.

### **How are these methods used in React? -----------**

### 📺 Sir, can I share my screen to show this with an example?

```jsx
import React, { Component } from "react";

class MyComponent extends Component {
  constructor(props) {
    super(props);
    this.state = { count: 0 };
    console.log("constructor called");
  }

  static getDerivedStateFromProps(nextProps, nextState) {
    console.log("getDerivedStateFromProps called");
    return null; // Used for state updates from props
  }

  shouldComponentUpdate(nextProps, nextState) {
    console.log("shouldComponentUpdate called");
    return true; // Return false to prevent re-rendering
  }

  render() {
    console.log("render called");
    return (
      <div>
        <h1>{this.state.count}</h1>
        <button onClick={() => this.setState({ count: this.state.count + 1 })}>
          Increment
        </button>
      </div>
    );
  }

  componentDidMount() {
    console.log("componentDidMount called");
  }

  componentDidUpdate(prevProps, prevState) {
    console.log("componentDidUpdate called");
  }

  componentWillUnmount() {
    console.log("componentWillUnmount called");
  }
}

export default MyComponent;
```

> The console will log the lifecycle methods at each phase, showing when the component mounts, updates, and unmounts.

---

<!-----

  ---------10--------

--- -->

## 10. How can you pass data from parent component to child component?

**Ans :--**

### **Need** (Why do we need to pass data from parent to child?)

When we create any application using react we often divide our UI into reusable component like when we want to create a button and we want to use that button in several other section in our react application and in order to use that small component in several other place that **component need some data so that that component can be reused** again and again and so as in react we can only send data in unidirectional way so a parent has to send its **data in the form of props** .

---

### **What is it**

#### What does it mean to pass data to child?

In React, **"props" (short for properties)** are used to pass data from a **parent components to child components**.  
This is a **unidirectional data flow**, meaning data can only move from parent component to child component and not the other way . Also Props are **read-only**, which means a component receiving props **cannot modify them directly**. and only the parent component which is sending the props can modify it via state.

---

### **How to implement**

Now lets understand how do we implement this

### 📺 **Sir, can I share my screen to show this with an example?**

```jsx
// ParentComponent.js
import React from "react";
import ChildComponent from "./ChildComponent";

function ParentComponent() {
  const username = "Rahul";
  return <ChildComponent name={username} />;
}

export default ParentComponent;


// ChildComponent.js
import React from "react";

function ChildComponent(props) {
  return <h2>Welcome, {props.name}!</h2>;
}

export default ChildComponent;
```

---

> In this example, the `ParentComponent` passes the `username` as a prop named `name` to `ChildComponent`, which then displays it using `props.name`.

### \*_Some benefits of using props are :--_

✅ Props help in **making components reusable**.  
✅ Props **cannot be modified inside the child component**.  
✅ Props **allow components to communicate** with each other.

---

<!-----

  ---------11--------

--- -->

11. What is the difference between functional components and class-based components?

<!-----

  ---------12--------

--- -->

12. Advantages of functional components over class-based components?

<!-----

  ---------13--------

--- -->

13. Differentiate between stateful and stateless components in React?

---

<!--------------------------

  -----------------------------------SECTION c-----------------------------  (ask on 18th april)7pm

--- ----------------------------->

### _Functional Components & Hooks_

14. What are hooks?

<!-----

  ---------14--------

--- -->

15. Why not use variable instead of useState?
16. How to implement different lifecycle methods using useEffect?
17. How does useEffect's behavior change with its dependency array?
18. Differentiate between useState and useEffect Hooks in React.

---

<!--------------------------

  -----------------------------------SECTION c-----------------------------  (ask on 19th april)7pm

--- ----------------------------->

### _React Props & State_

19. What are props in React?
20. Why shouldn’t we directly update the state in React?
21. Explain that if a parent component renders, do the child components also re-render?
22. Describe controlled and uncontrolled components.

---

<!--------------------------

  -----------------------------------SECTION D-----------------------------  (ask on 20th april)7pm

--- ----------------------------->

### _React Keys & List Rendering_

23. What is a key in React? why are they used in list in react ?
24. Why do we need a key in React?
25. What happens if we don’t use keys or use the same key for multiple items?
26. Why does React have a key attribute? Why not just use id?
27. How does key work in React?
28. Why won’t id work instead of key?
29. If we can use an array index as key, why not use it as id?
30. What are the issues with using an array index as key in React?
31. When is it okay to use an array index as key?
32. What is the difference between key and id in React?
33. How does React track UI updates using keys?
34. Why is key important for React's reconciliation process?
35. How does React identify changes in the virtual DOM?
36. Why is key necessary when rendering lists in React?
37. Can we use a random value as key?
38. What is the best practice for selecting a key in React?
39. Does React re-render all items if a key changes?
40. What happens if we use a non-unique key?
41. How does React handle state updates when keys change?
42. What impact do keys have on component lifecycle methods?
43. How does React handle key mismatches?
44. What happens if we don’t specify a key at all?
45. How does key affect performance in React?

---

### _React Routing & Conditional Rendering_

46. What are the React Router methods?
    46.1) What is React router and is it Different from React-router-dom ?What happpend after the version 7 update to them ?
    46.2) What is Link and Navlink component provided by React-Router ?
47. What is conditional rendering? How does it work? Explain with an example.  
    **47.1.** What is the Difference between React-router and react-router-dom ?

### _JavaScript Core Concepts_

48. How does prototypal inheritance work in JavaScript?
49. Explain call(), apply(), and bind() methods in JavaScript.
50. What is the this keyword in JavaScript?  
    51.What are Promises? Explain Promise.allSettled() promise API with example.
51. How to manage 3 Parallel API calls?
52. what is promise.any , promise.race ? (jonas se pdho)

## _React techniques and hooks_:--

53. what is useState Hook ? and why we need state why can't we just use variable ?
54. What does "debouncing" mean, and how can you implement it in React?
55. Explain the concept of ‘Lifting State Up’ in React ?
56. What is useRef Hook in React?
    56.5) Explain all the types of hooks achhe se ? also what is custom hook and create 2 custom hook
    _use the fe 202 intv question notes and that hooks videos for this_ ?
57. What are the differences between the useRef hook and the useState hook?
58. Explain the difference between useCallback and useMemo hooks.
59. What is the useContext hook? and how it is used
60. What are the React custom hooks? How can custom hooks be created?
61. How to increase the performance of a ReactJS application?
62. How to implement UI in frontend using Figma design?
63. **When should you consider creating a custom hook?**
64. **What is Prop Drilling in React?**
65. **What is the primary purpose of the useCallback hook in React?**

## basic questions remaining:------

66. What is the difference between state and props in React
67. What are Higher Order Components in React ?
68. When rendering lists in React, what helps determine what needs to be re-rendered when a chance occurs?
69. Explain how use effect hook can be used as component did mount method ?
70. Why cant we mutate the states in React?
71. What is a pure component in React?
72. How to do cleanup tasks in react functionall component like cancelling netwrok requests removing timers?

## Advance questions :-----

73. How to mock api calls ? (see fe 202 session 1 again )
74. What is useReducer Hook in React
75. Explain the process of making an HTTP request to a server
76. Name different types of HTTP requests
77. What is lazy loading and debouncing?
78. How to increase performance in React?

---

## Extra question which i got while making react projects :--

Read them in vs code
(React uestion jo maine project meseekha.md)

<!------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------>

## **(c)** Hooks topics and routing question (Refer wo hooks video for hooks baaki khud se)------------

### Q14) Explain the concept of Lifting State up ?

Ans :--

### Q0) What is React router Dom and is it Different from React-router ?What happpend after the version 7 update to them ?

### Q0.1) What is Link and Navlink component provided by React-Router ?

### Q1) what is useState Hook ?and why we need state why can't we just use variable ?

Ans :--

### Q2) What is useEffect hook ?

Ans :--

(Example with a cleanup function) --- For example we want to show what is the current width of the window screen whenever we are resizing then we will use useEffect

```js
import { useEffect, useState } from "react";

function WindowResizeTracker() {
  const [width, setWidth] = useState(window.innerWidth);

  useEffect(() => {
    const handleResize = () => setWidth(window.innerWidth);

    window.addEventListener("resize", handleResize);

    return () => {
      console.log("Cleanup: Removing resize listener");
      window.removeEventListener("resize", handleResize);
    };
  }, []);

  return (
    <div>
      <p>Window Width: {width}px</p>
    </div>
  );
}

export default WindowResizeTracker;
```

### Q3) What is useRef hooks?

Ans :---

<!------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------>
