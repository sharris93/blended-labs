# React Single Page Exercise

## Overview

In this exercise, you'll build a simple single-page React application using Vite and style it using a CSS framework like Bulma. The page will include four sections:

1. Navbar  
2. Hero  
3. Main Content  
4. Footer  

You will use local JavaScript variables to store some of the content for each section. For example:

```js
const titleText = 'Hello World';
```

> Note: You should not use multiple React components for this exercise. Everything should be written in the `App.jsx` file, as you have not yet learned about props or component composition.

---

## Step 1: Bootstrap a New React App with Vite

1. Open your terminal and run the following to create a new Vite + React project - when prompted, select `React` then `JavaScript` from the options provided:

```bash
npm create vite@latest my-react-page
```

2. Move into your new project folder:

```bash
cd my-react-page
```

3. Install all dependencies pre-packaged with the Vite template:

```bash
npm install
```

4. Install Bulma (a CSS framework that will allow us to add styling without needing a CSS file):

```bash
npm install bulma
```

5. Open the `my-react-page` folder in Visual Studio Code:
`code .`

6. Import Bulma into your `main.jsx` file below the `index.css` import. This will make the Bulma styles available app-wide:

```js
import 'bulma/css/bulma.min.css';
```

---

## Step 2: Clean Up the Starter Code

1. Open `App.jsx` and delete all the existing JSX inside the `return()` statement, except for the `<></>` wrapping the rest of the markup.
2. Delete all imports at the top of the file.
3. Remove the `const [count, setCount] = useState(0)`
4. In `main.jsx`, remove the `index.css` import line. We won't be needing it.
5. Delete the `index.css` and `App.css` files from the project.
6. Start the development server:

```bash
npm run dev
```

You should now see a blank page in your browser.

---

## Step 3: Create Local Data Variables

Inside `App.jsx`, add variables for each section like this:

```js
const navbarTitle = 'My Site';
const heroHeading = 'Welcome to My Site';
const mainParagraphs = [
  'This is the first paragraph of the main content.',
  'Here is another bit of content to display on the page.',
  'You can keep adding more text as needed!'
]
const footerText = '© 2025 My Site. All rights reserved.';
```

You will use these variables when building out your sections.

---

## Step 4: Add the Navbar

Add the following JSX inside the `return()` of your `App` function. This should go INSIDE the fragment (`<></>`):

```jsx
<nav className="navbar is-primary" role="navigation" aria-label="main navigation">
  <div className="navbar-brand">
    <a className="navbar-item" href="#">
      
    </a>
  </div>
</nav>
```

Explanation:

- `navbar is-primary`: Bulma classes that style the navbar with a primary color.
- `className`: In React, we use `className` instead of `class` because `class` is a reserved keyword in JavaScript.


Now, inside the `<a>` tag, render the name of your site using the `navbarTitle` variable and inline JS:
```jsx
<a className="navbar-item" href="#">
  {navbarTitle}
</a>
```

---

## Step 5: Add the Hero Section

Below the navbar, add the following, but also rendering the `heroHeading` inside the `<h1>`:

```jsx
<section className="hero is-info is-medium">
  <div className="hero-body">
    <div className="container has-text-centered">
      <h1 className="title">
        
      </h1>
    </div>
  </div>
</section>
```

Explanation:

- `hero is-info is-medium`: Creates a large banner area with a blue (info) color.
- `has-text-centered`: Centers the text horizontally.

---

## Step 6: Add the Main Content

Below the hero section, add the below markup. Inside of the `.container` div, render each of the `mainParagraphs` strings using `.map()`. Ensure each is string of text is rendered inside of a `<p>` tag:

```jsx
<main className="section">
  <div className="container has-text-centered">
    
  </div>
</main>
```

Explanation:

- We are using an array of strings to represent different pieces of content.
- `.map()` lets us loop over the array and return a paragraph element for each item.
- Don't forget - the `key` prop is required in React when rendering lists. It helps React identify which items have changed or been removed. In this case, you can use the `index` from the `.map()` method as the key (which is okay for simple, static lists like this).


---

## Step 7: Add the Footer

Finally, add the footer at the bottom, rendering `footerText` inside the `<p>` tag:

```jsx
<footer className="footer">
  <div className="content has-text-centered">
    <p></p>
  </div>
</footer>
```

---

## Final Touches

- Double-check your file for any typos or syntax errors.
- You should now have a clean, styled single-page React app with a navbar, hero, content section, and footer.
- You can tweak the content of your variables to personalize the app.

---

## Optional Challenge

Try changing the colors or text styles by adding different Bulma classes. You can explore the Bulma documentation at:

https://bulma.io/documentation/

---

Happy coding!