### note1 - **(NEED what and HOW ) bs isi trh bologe tum humesha:------**

Note 2 \*HOW TO deal with question you don't know completely ?
--- Pehle bolo phir ye last me bolo --- ( how to say no to a question)
Ans :- Sir ,This is what i know at the moment and i am not exactly sure if i am explaining it correctly but i would love to get back to this question right after the interview .

note 2.1 ) How to deal when you completely dont know ?
Ans :- Sir currently i am not able to come up with the right answer to this question but i would love to get back to this question right after this interview

# --------- **css** :--------- (----read in fe 102 lect 5 onwards notes ----)

# **(A)** _Basic :--------_

### Q0) What is CSS?

Ans :--
(generate the need)

---

**Need (Why do we need CSS?)**

When we create web pages using HTML, the structure of our webpage gets ready but our whole website is not colorful not have any sizes or any layout or responsive and in order
to do that we need to use CSS . as it allows to do separation of concern by separating our structure file from design file .

---

**What (What exactly is CSS?)**

So ,what is css --> CSS stands for **Cascading Style Sheets**.  
It is a stylesheet language used to **style HTML elements** on a web page.

Using CSS, we can control:

The design of our website like layout, colors, sizes animation and responsive design .

---

**How (How do we use CSS in a project?)**

So ,There are **three main ways** to apply CSS to a webpage:

1. **Inline CSS**  
   Using this we add `style` attribute directly to an HTML element.

   ```html
   <p style="color: blue; font-size: 20px;">Hello World</p>
   ```

2. Then we have **Internal CSS**  
   using this we write CSS inside a `<style>` tag in the HTML `<head>` element.

   ```html
   <style>
     p {
       color: green;
       font-size: 20px;
     }
   </style>
   ```

3. **External CSS (Most Recommended)**  
   And then we have the external stylesheet using which we link a separate `.css` file to the HTML using `<link>` tag.

   ```html
   <link rel="stylesheet" href="styles.css" />
   ```

   In `styles.css`:

   ```css
   p {
     color: red;
     font-size: 20px;
   }
   ```

---

So in short we can say that HTML is like a skeleton of our webpage like parts of a car and css is like the design the colors of the part of the car how much size elments the car will have

**📺 Share Screen (Live Example)**

🖥 \_Sir can i share my screen to show this with an example (SHOW all three ways to do )

```html
<!-- index.html -->
<!DOCTYPE html>
<html>
  <head>
    <title>CSS Example</title>
    <link rel="stylesheet" href="styles.css" />
  </head>
  <body>
    <h1>Hello CSS!</h1>
    <p>This text is styled using external CSS.</p>
  </body>
</html>
```

```css
/* styles.css */
h1 {
  color: blue;
  text-align: center;
}

p {
  color: gray;
  font-size: 18px;
}
```

---

---

### Q1) What is CSS Box Model? (crio)

Ans :--

**Need (Why do we need the CSS Box Model?)**

So when we design a webpage, one of the most important things is to see **how much space each element takes**, and how much gap it has **inside and outside**. so in order to correctly understand it the browser treats every element like a rectangular box and this is known as css box Model .

It helps us **clearly control the spacing, borders, and total size** of elements on the page.

---

**What (What exactly is the CSS Box Model?)**

The **CSS Box Model** is a way to describe the structure and layout of elements on a webpage. where Every element is represented as a rectangular box, and this box consists of **4 layers**, from **inside to outside**:

1. **Content** – First we have is the content which is the innermost part of the box .This is where the actual text or image goes.
2. **Padding** – Then we have is the padding it is The space **between the content and the border**.
3. **Border** – and then have is a border which A line that surround padding and content.
4. **Margin** – and finally we have the margin which is The outermost space that separates our element from other element.

**How:---**

## Sir can i share my screen to show this with an example (NOT needed in this question)

---

---

### Q2) What are the differences between CSS Grids and Flexbox?

---

**Need (Why do we need Grid and Flexbox in CSS?)**

when we build layouts in CSS, especially responsive ones, we often need to align and arrange elements in rows and columns.  
In order to do that layout easily CSS introduced **Flexbox** and **Grid** —

---

**What (What are Grid and Flexbox?)**

- In which **Flexbox** is a **one-dimensional layout system**, which means it’s best used when we want to arrange items in **a single row or a single column**.
  for example creating navigation bars, aligning buttons

- On the other hand **CSS Grid** is a **two-dimensional layout system**,
  which means it allows us to control **both rows and columns at the same time** —
  and It is ideal for creating complex layouts, like entire page structures, where you need to position and size elements across both horizontal and vertical axes. .With Grid, We can define areas, place items in specific spots, and control spacing between rows and columns.

So in conclusion

- Use **Grid** when you need to design the entire layout of our webpage, like deciding where sections of a page will go. and
- Use **Flexbox** when working with elements inside those sections, like aligning items within a row or column and mainly for 1 dimensional layout.

---

**How (Key Differences between Flexbox and Grid)**

## 📺 Sir can I share my screen to show this with an example

```html
<!-- Flexbox example -->
<style>
  .flex-container {
    display: flex;
    gap: 10px;
  }
  .flex-item {
    background-color: lightblue;
    padding: 20px;
    text-align: center;
  }
</style>

<div class="flex-container">
  <div class="flex-item">Item 1</div>
  <div class="flex-item">Item 2</div>
  <div class="flex-item">Item 3</div>
</div>
```

```html
<!-- Grid example -->
<style>
  .grid-container {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 10px;
  }
  .grid-item {
    background-color: lightgreen;
    padding: 20px;
    text-align: center;
  }
</style>

<div class="grid-container">
  <div class="grid-item">Box 1</div>
  <div class="grid-item">Box 2</div>
  <div class="grid-item">Box 3</div>
</div>
```

---

---

### Q3)
