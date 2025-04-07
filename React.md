### note1 - **(NEED what and HOW ) bs isi trh bologe tum humesha:------**

Note 2 \*HOW TO deal with question you don't know completely ?
--- Pehle bolo phir ye last me bolo --- ( how to say no to a question)
Ans :- Sir ,This is what i know at the moment and i am not exactly sure if i am explaining it correctly but i would love to get back to this question right after the interview .

note 2.1 ) How to deal when you completely dont know ?
Ans :- Sir currently i am not able to come up with the right answer to this question but i would love to get back to this question right after this interview

# --------------------- Follow Need what HOW ?-------------

## **(A)** Hooks topics and routing question (Refer wo hooks video for hooks baaki khud se)------------

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

## **(B)** Basic and core cocncept

### Q2) What is jsx ?

Ans :--

**Need (Why do we need JSX?)**

When we build React components, we often need to mix **HTML with JavaScript**. Writing UI elements using `document.createElement()` or plain JavaScript can be **complex and less readable**. To solve this problem, **React introduced JSX**, which makes writing UI code inside JavaScript much easier and cleaner.

---

**What (What is JSX?)**

JSX stands for **JavaScript XML**. it allows us to write HTML-like code inside JavaScript and place them in the Dom without using functions
like append child or create element
Basically it just provide us the syntatic sugar for the `react. createElement` and it makes the code more readalbe and expressive by combining JavaScript expressions
with an HTML-like template syntax .

---

**How (How does JSX work & its rules?)**
**"There are some important rules in JSX that we need to follow:**

- First, **all the JSX tags must be closed**, even self-closing ones of html. For example, in HTML, we might write `<img src="image.jpg">`, but in JSX, we must write it as `<img src="image.jpg" />`.

- Secondly, **attribute names in JSX should follow camelCase.** So instead of writing `class`, we write `className`, and instead of `onclick`, we use `onClick` where C is capital.

- Third, **any JavaScript logic inside JSX should be placed inside curly braces `{}`**. For example, if we want to display a variable inside an `<h1>` tag, we write `<h1>{title}</h1>`.

- Lastly, **all JSX elements must be wrapped inside a single parent element**, because a React component can only return **one** root element. so If we need multiple elements, we usually wrap them inside a `<div>` or a React Fragment (`<>...</>`).

**📺 Share Screen (Live Example)**

🖥 _Okay, so in order to understand how we use this can i share my screen and show ._
so sir in order to understand how we use this , can i share my screen to show this with an example:----

```jsx
import React from "react"; // Importing React

const App = () => {
  // Creating a functional component
  return (
    <>
      <h1>Welcome to JSX</h1>
      <p>This is an example of JSX inside a React component.</p>
    </>
  );
};

export default App; // Exporting the component
```

---

### Q5) what is a singlepage application ?

Ans:--
**Need? ---**
So, whenever we build a website or a project, we need to implement multiple pages. Usually, websites have different sections, like in a **navbar**, where we see different options linking to various pages.

In a traditional **Multi-Page Application (MPA)**, clicking on a link reloads the entire page, which slows down performance. This happens because every time we navigate to a different page, the browser fetches and loads a completely new HTML file.

To solve this, **Single Page Applications (SPAs)** were introduced, especially after **React** became popular.

**What is an SPA?**

A Single Page Application is a web application where we have only **one main HTML file**, and all other content is dynamically loaded inside it without refreshing the page. Instead of fetching a new HTML file, it only updates specific sections, making the app feel much faster.
**How do we handle multiple pages inside an SPA?**

We achieve this using **React Router**, which is a library in React that allows us to create multiple sections (or views) within the same page. When we click on a link, instead of reloading the page, it just updates the view by changing the route.

**Steps to implement an SPA:**

1. Use **React (a JavaScript library)** to build the application.
2. Use **React Router** to handle different routes within the same page.

This is how we create a smooth, fast, and efficient **Single Page Application (SPA).**

---

<!------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------>

## **(c)**

### Q2) Explain the concept of Lifting State up ?

Ans :--

<!------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------>

## **(d)**
