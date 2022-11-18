# React

- [React](#react)
  - [Introduction of React](#introduction-of-react)
    - [What is React?](#what-is-react)
    - [Why React is fast](#why-react-is-fast)
    - [React History](#react-history)
    - [Prerequisites for React](#prerequisites-for-react)
    - [About React](#about-react)
    - [Extension for React in VS Code](#extension-for-react-in-vs-code)
  - [React Installation](#react-installation)
    - [Without Installation](#without-installation)
    - [With Installation](#with-installation)
    - [File and Folder Structure](#file-and-folder-structure)
  - [Basic React](#basic-react)
    - [Component-Based Working in React](#component-based-working-in-react)
    - [Hello World Program](#hello-world-program)
    - [JSX in React](#jsx-in-react)
    - [Passing Multiple elements using parent div](#passing-multiple-elements-using-parent-div)
    - [Using import for importing modules](#using-import-for-importing-modules)
    - [Using an array to pass elements](#using-an-array-to-pass-elements)
    - [Using React Fragments to pass elements](#using-react-fragments-to-pass-elements)
    - [Create a basic structure using react](#create-a-basic-structure-using-react)
    - [JSX Expression](#jsx-expression)
    - [Basic Program using React](#basic-program-using-react)
    - [JSX Attributes](#jsx-attributes)
    - [Styling in React](#styling-in-react)
    - [import and export modules](#import-and-export-modules)
    - [Components](#components)
    - [Create App.js file](#create-appjs-file)
    - [Props](#props)

## Introduction of React

### What is React?

1. React is a javascript library
2. The main focus is building UI as fast as possible
3. So this is used for Single Page Application
4. This means a Complete website on a single page

### Why React is fast

1. React Use Virtual DOM

For ex:

```html
<ul>
  <li>Item 1</li>
  <li>Item 2</li>
  <li>Item 3</li>
</ul>
```

Real DOM Update Complete List

Virtual DOM Update Only Required List

### React History

1. React was first designed by Jorden Walke, a software engineer at Facebook.
2. It was first deployed for Facebook News Feed around 2011
3. In 2013, React was open source at the JS conference

### Prerequisites for React

1. HTML, CSS, Javascript
2. ES6 understanding will make you comfortable with ReactJs
3. Basic understanding of npm

### About React

1. Component-Based Approach
2. Uses a Declarative Approach
3. DOM updates are handled gracefully
4. Reusable Code
5. React is designed for speed, speed of implementation the application simplicity and scalability.

### Extension for React in VS Code

1. babel javascript
2. Javascript (ES6) code snippets
3. VS Code icons
4. live server

## React Installation

### Without Installation

1. React is Generally used with npm
2. But we can also use CDN

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>React App</title>
    <script
      crossorigin
      src="https://unpkg.com/react@16/umd/react.production.min.js"
    ></script>
    <script
      crossorigin
      src="https://unpkg.com/react-dom@16/umd/react-dom.production.min.js"
    ></script>
    <script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>
  </head>
  <body>
    <div id="root"></div>
    <script type="text/babel">
      class Hello extends React.Component {
        render() {
          return <h1>Hello React</h1>;
        }
      }
      ReactDOM.render(<Hello />, document.getElementById("root"));
    </script>
  </body>
</html>
```

### With Installation

1. Install NodeJS and NPM
2. Install VS Code/ Sublime/ Atom/ Brackets
3. Install React from terminal
   1. npm install -g create-react-app
   2. create-react-app --version
   3. create-react-app &lt;project_name&gt;
   4. cd &lt;project_name&gt;
   5. npm start

### File and Folder Structure

1. the package.json file is the most important in your project
2. package-lock.json contains the history and control version of the package.json file
3. .gitignore file is used to ignore files and folders in your project
4. the src folder is used to store all your source files
5. app.css used for styling
6. app.js main file where to start your code
7. app.test.js is used to test your code
8. index.css is a style index.js file
9. index.js is the entry point of your project
10. logo.svg is used for the logo
11. reportWebVitals is used for reporting web vitals
12. setupTests.js is used for testing
13. the public folder is used to store all your public files
14. favicon.ico is used for favicon
15. index.html is the main file of your project
16. manifest.json is a metafile of your project
17. robots.txt is used for google search engine
18. node_modules is used to store all your node modules

## Basic React

### Component-Based Working in React

Without React

```html
<div class="container">
  <div class="cards">
    <div class="card">
      <div class="card_title">Card Title</div>
      <div class="card_desc">Card Description</div>
    </div>
    <div class="card">
      <div class="card_title">Card Title</div>
      <div class="card_desc">Card Description</div>
    </div>
    <div class="card">
      <div class="card_title">Card Title</div>
      <div class="card_desc">Card Description</div>
    </div>
    <div class="card">
      <div class="card_title">Card Title</div>
      <div class="card_desc">Card Description</div>
    </div>
  </div>
</div>
```

With React

```js
ReactDOM.render(
  <>
    <div class="container">
      <div class="cards">
        <Card>
          <div class="card_title">Card Title</div>
          <div class="card_desc">Card Description</div>
        </Card>
      </div>
    </div>
  </>,
  document.getElementById("root")
);
```

### Hello World Program

1. React = React Module
2. ReactDOM = React DOM Module
3. ReactDOM.render = Render Method

```js
ReactDOM.render("What to show", "Where to show", "callback()");
```

```html
<!-- ./public/index.html -->
<body>
  <div id="root"></div>
</body>
```

```js
// ./src/index.js
var React = require("react");
var ReactDOM = require("react-dom");

ReactDOM.render(<h1>Hello World</h1>, document.getElementById("root"));
```

### JSX in React

JSX: JavaScript XML

JSX is defined inside the React Module. We use React module for JSX Element.

Inside HTML we call `<tag></tag>` as **HTMl element**

```html
<body>
  <h1>Heading 1</h1>
</body>
```

But in React we call `<tag></tag>` as **JSX Element**

```html
<>
  <h1>Heading 1</h1>
</>
```

### Passing Multiple elements using parent div

Without wrapping

```js
var React = require("react");
var ReactDOM = require("react-dom");

ReactDOM.render(
  <h1>Heading 1</h1>
  <h2>Heading 2</h2>, document.getElementById("root"));
```

This is throwing as many errors, We cannot pass multiple elements without wrapping them

With wrapping

We use `<div></div>` for wrapping

```js
var React = require("react");
var ReactDOM = require("react-dom");

ReactDOM.render(
  <div>
    <h1>Heading 1</h1>
    <h2>Heading 2</h2>
  </div>,
  document.getElementById("root")
);
```

It's showing the expected output without any errors.

### Using import for importing modules

We use `require` for importing modules

```js
var React = require("react");
var ReactDOM = require("react-dom");
```

But now we use `import` for importing modules

```js
import React from "react";
import ReactDOM from "react-dom";
```

### Using an array to pass elements

We used `<div></div>` for passing elements but we use an array instead of `<div>`.

```js
import React from "react";
import ReactDOM from "react-dom";

ReactDOM.render(
  [<h1>Heading 1</h1>, <h2>Heading 2</h2>],
  document.getElementById("root")
);
```

### Using React Fragments to pass elements

Normal Div

```js
import React from "react";
import ReactDOM from "react-dom";

ReactDOM.render(
  <div>
    <h1>Heading 1</h1>
    <h2>Heading 2</h2>
  </div>,
  document.getElementById("root")
);
```

React Fragments

```js
import React from "react";
import ReactDOM from "react-dom";

ReactDOM.render(
  <React.Fragment>
    <h1>Heading 1</h1>
    <h2>Heading 2</h2>
  </React.Fragment>,
  document.getElementById("root")
);
```

React Fragments Syntactic Suger Form

```js
import React from "react";
import ReactDOM from "react-dom";

ReactDOM.render(
  <>
    <h1>Heading 1</h1>
    <h2>Heading 2</h2>
  </>,
  document.getElementById("root")
);
```

### Create a basic structure using react

```js
var React = require("react");
var ReactDOM = require("react-dom");

ReactDOM.render(
  <>
    <h1>This is Headng</h1>
    <p>This is paragraph</p>
    <ul>
      <li>List items 1</li>
      <li>List items 2</li>
      <li>List items 3</li>
    </ul>
  </>,
  document.getElementById("root")
);
```

### JSX Expression

Using Javascript inside JSX elements

```js
var React = require("react");
var ReactDOM = require("react-dom");

let name = "Akash Patil";

ReactDOM.render(
  <>
    <h1>Hello my name is {name}</h1>
  </>,
  document.getElementById("root")
);
```

Using Template Literals

```js
import React from "react";
import ReactDOM from "react-dom";

let fname = "Akash";
let lname = "Patil";

ReactDOM.render(
  <>
    <h1>{`Hello my name is ${fname} ${lname}`}</h1>
  </>,
  document.getElementById("root")
);
```

### Basic Program using React

Show the current date and time

```js
import React from "react";
import ReactDOM from "react-dom";

let now = new Date();

ReactDOM.render(
  <>
    <h1>My Name is Akash Patil</h1>
    <p>{`Today is ${now.toLocaleDateString()}`}</p>
    <p>{`Current time is ${now.toLocaleTimeString()}`}</p>
  </>,
  document.getElementById("root")
);
```

### JSX Attributes

We call HTML `<tag></tag>` as JSX Element, also we call HTML attributes `href` as JSX attributes

```js
import React from "react";
import ReactDOM from "react-dom";

ReactDOM.render(
  <>
    <h1>Hello World</h1>
    <a href="https://www.ehackhow.com">ehackhow</a>
  </>,
  document.getElementById("root")
);
```

Attributes examples

| html            | jsx             |
| --------------- | --------------- |
| href            | href            |
| contenteditable | contentEditable |
| class           | className       |
| http-equiv      | httpEquiv       |

`class` is a defined keyword in `react` that's why we use `className` instead of `class`.

### Styling in React

1. Inline
2. Internal
3. External

1: Inline

```js
import React from "react";
import ReactDOM from "react-dom";

ReactDOM.render(
  <>
    <h1
      style={{
        color: "#f48044",
        textTransform: "uppercase",
      }}
    >
      Hello World
    </h1>
  </>,
  document.getElementById("root")
);
```

2: Internal

```js
import React from "react";
import ReactDOM from "react-dom";

let title = {
  color: "#f48044",
  textTransform: "uppercase",
};

ReactDOM.render(
  <>
    <h1 style={title}>Hello World</h1>
  </>,
  document.getElementById("root")
);
```

3: External

Using `className` to apply CSS on **elements**

```js
import React from "react";
import ReactDOM from "react-dom";
import "./index.css";

ReactDOM.render(
  <>
    <h1 className="title">Hello World</h1>
  </>,
  document.getElementById("root")
);
```

### import and export modules

1. import
2. export

1: Import

We use require in js to include any module in the project

```js
var React = require("react");
var ReactDOM = require("react-dom");
```

But after ES6 we use the `import` and `export` feature to include any module in the project

```js
import React from "react";
import ReactDOM from "react-dom";
```

We want to import any variable or function from any file in the current file so we use the `import` functionality

There are two types of imports

1. Default import
2. Specific imports

1: default import

```js
import React from "react";
```

This is the `default export` from `react`

2: specific imports

```js
import { num } from "number";
```

Here a `number` is our file where we store `num` as a variable with an assigned value.

We use `{ }` to show this is exported from any file but not the `default export`

2: Export

1. Default export
2. Specific export

1: Default export

In every file, we export **any one** thing and the rest of all are exported specifically.

```js
var num = 25;

export default num;
```

```js
function demo() {
  let a = 10;
  return a;
}

export default demo;

// or

export default function demo() {
  let a = 10;
  return a;
}
```

2: Specific export

```js
var num = 25;

export { num };
```

### Components

Components are independent and reusable bits of code.

1. A piece of code that can reuse
2. Such a Function
3. But more powerful than the function
4. Header, Footer is the best example

Component Types

1. Class Components
2. Functional Components
3. Other

Without Using Components

```js
import React from "react";
import ReactDOM from "react-dom";
import "./index.css";

ReactDOM.render(
  <>
    <h1>This is heading</h1>
    <p>This is paragraph</p>
    <ul>
      <li>item 1</li>
      <li>item 2</li>
      <li>item 3</li>
      <li>item 4</li>
      <li>item 5</li>
    </ul>
  </>,
  document.getElementById("root")
);
```

With using components

1: Class Components

index.js

```js
import React from "react";
import ReactDOM from "react-dom";
import Heading from "./Heading";
import "./index.css";

ReactDOM.render(<Heading />, document.getElementById("root"));
```

Heading.jsx

```js
import React from "react";

class Heading extends React.Component {
  render() {
    return <h1>This is Heading</h1>;
  }
}

export default Heading;
```

2: Functional Components

index.js file

```js
import React from "react";
import ReactDOM from "react-dom";
import "./index.css";
import Heading from "./Heading";
import Para from "./Para";
import List from "./List";

ReactDOM.render(
  <>
    <Heading />
    <Para />
    <List />
  </>,
  document.getElementById("root")
);
```

Components File Code

```js
// Heading Component
import React from "react";

function heading() {
  return <h1>This is heading</h1>;
}

export default heading;

// Paragraph Component
import React from "react";

function para() {
  return <p>This is paragraph</p>;
}

export default para;

// List Component
import React from "react";

function list() {
  return (
    <ul>
      <li>item 1</li>
      <li>item 2</li>
      <li>item 3</li>
      <li>item 4</li>
      <li>item 5</li>
    </ul>
  );
}

export default list;
```

### Create App.js file

`App.js` file is used to define the `App` component. Mainly we use this file to manage our all work and `index.js` is used to import other pages and manage them.

We create a `components` folder and store `Heading`, `Para` & `Litt` components in it.

index.js

```js
import React from "react";
import ReactDOM from "react-dom";
import "./index.css";
import App from "./App";

ReactDOM.render(<App />, document.getElementById("root"));
```

app.jsx

```js
import Heading from "./components/Heading";
import Para from "./components/Para";
import List from "./components/List";

function App() {
  return (
    <>
      <Heading />
      <Para />
      <List />
    </>
  );
}

export default App;
```

Component Program

public/index.html

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>React App</title>
  </head>
  <body>
    <div id="root"></div>
  </body>
</html>
```

src/index.js

```js
import React from "react";
import ReactDOM from "react-dom";
import "./index.css";
import App from "./App";

ReactDOM.render(<App />, document.getElementById("root"));
```

src/index.css

```css
*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
  list-style: none;
}

body {
  font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto,
    Oxygen, Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
  background: #282a36;
  min-height: 100vh;
  color: #fff;
  display: flex;
  flex-flow: column;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.container {
  display: flex;
  flex-flow: column;
  justify-content: center;
  align-items: center;
  gap: 1rem;
}

.title {
  text-transform: uppercase;
  color: #f48044;
  font-size: 2.5rem;
}

.city {
  font-size: 1.9rem;
}

.listTitle {
  font-size: 1.5rem;
}

.list {
  font-size: 1.2rem;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1rem;
}

.list li {
  background: #f48044;
  padding: 1rem;
  color: #282a36;
  font-weight: bold;
  cursor: pointer;
}
```

src/app.js

```js
import React from "react";
import Container from "./components/Container";

export default function App() {
  return <Container />;
}
```

src/components/container.jsx

```js
import React from "react";

let obj = {
  name: "Akash Patil",
  city: "Islampur",
  lang: ["C", "C++", "HTML", "CSS", "JavaScript", "PHP"],
};

let { name, city, lang } = obj;

function lng(i) {
  return lang[i];
}

export default class Container extends React.Component {
  render() {
    return (
      <div className="container">
        <h1 className="title">My name is {name}</h1>
        <p className="city">I'm from {city}</p>
        <p className="listTitle">My fav languages</p>
        <ul className="list">
          <li>{lng(0)}</li>
          <li>{lng(1)}</li>
          <li>{lng(2)}</li>
          <li>{lng(3)}</li>
          <li>{lng(4)}</li>
          <li>{lng(5)}</li>
        </ul>
      </div>
    );
  }
}
```

### Props

`props` are the properties that we pass to the component with value then we pass `props` to the function component as arguments that pass those values to the `jsx` element.

How we use `props`

1: Create an `index.html` file inside the `public` folder and add code

index.html

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>React App</title>
  </head>
  <body>
    <div id="root"></div>
  </body>
</html>
```

2: Create an `index.js` file inside the `src` folder and add the code

> Note: For testing purposes

index.js

```js
import React from "react";
import ReactDOM from "react-dom";

ReactDOM.render(<h1>Hello World</h1>, document.getElementById("root"));
```

3: Create an `App.jsx` file inside the `src` folder and add the code

App.jsx

```js
import React from "react";

const App = () => <h1>App</h1>;

export default App;
```

4: Pass the `App` component to the `ReactDOM.render()` method

index.js

```js
import React from "react";
import ReactDOM from "react-dom";
import App from "./App";

ReactDOM.render(<App />, document.getElementById("root"));
```

5: Create the `card` structure inside an `App` component

App.jsx

```js
import React from "react";

const App = () => (
  <div className="cards">
    <div className="card">
      <h1 className="title">Name</h1>
      <h2 className="desg">Designation</h2>
      <h3 className="desc">Description</h3>
      <button className="card_btn">Read More</button>
    </div>
  </div>
);

export default App;
```

6: Create an `index.css` file inside the `src` folder and add code and `import` inside `index.js` file

index.css

```css
*,
*::after,
*::before {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

html {
  font-size: 62.5%;
}

body {
  font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto,
    Oxygen, Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
  background: #282a36;
  color: #fff;
  min-height: 100vh;
  width: 100%;
  font-size: 1.6rem;
}
```

index.js

```js
import React from "react";
import ReactDOM from "react-dom";
import "./index.css";
import App from "./App";

ReactDOM.render(<App />, document.getElementById("root"));
```

7: Create a `functional component` on top of the `App` component `inside` an `App.jsx` file and `call` 5 times inside `cards` div

App.jsx

```js
import React from "react";

const Card = () => (
  <div className="card">
    <h1 className="title">Name</h1>
    <h2 className="desg">Designation</h2>
    <h3 className="desc">Description</h3>
    <button className="card_btn">Read More</button>
  </div>
);

const App = () => (
  <div className="cards">
    <Card />
    <Card />
    <Card />
    <Card />
    <Card />
  </div>
);

export default App;
```

8: Design the card using CSS

index.css

```css
*,
*::after,
*::before {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

html {
  font-size: 62.5%;
}

body {
  font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto,
    Oxygen, Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
  background: #282a36;
  color: #fff;
  min-height: 100vh;
  width: 100%;
  font-size: 1.6rem;
}

.cards {
  width: 100%;
  max-width: 120rem;
  min-height: 100vh;
  margin-inline: auto;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  padding: 2rem;
  gap: 2rem;
}

.card {
  background: #f48044;
  color: #282a36;
  display: flex;
  flex-flow: column;
  align-items: center;
  justify-content: center;
  text-align: center;
  gap: 1rem;
  padding: 5rem 0;
  cursor: pointer;
}

.card .card_btn {
  background: #282a36;
  padding: 1rem 2rem;
  text-transform: uppercase;
  color: #fff;
  font-weight: bold;
  border-radius: 1rem;
}

@media screen and (max-width: 1100px) {
  .cards {
    grid-template-columns: repeat(2, 1fr);
    gap: 2rem;
  }
}

@media screen and (max-width: 800px) {
  .cards {
    grid-template-columns: 1fr;
    gap: 2rem;
  }
}
```

9: Pass parameter to `Card` component in `App.jsx` file

App.jsx

```js
import React from "react";

const Card = () => (
  <div className="card">
    <h1 className="title">Name</h1>
    <h2 className="desg">Designation</h2>
    <h3 className="desc">Description</h3>
    <button className="card_btn">Read More</button>
  </div>
);

const App = () => (
  <div className="cards">
    <Card title="Name" desg="Designation" desc="Description" btn="Read More" />
  </div>
);

export default App;
```

10: Pass `props` as an argument to the `Card` component and Pass `properties` as an expression to the `jsx elements`

> Note: `props` is a object

App.jsx

```js
import React from "react";

const Card = (props) => (
  <div className="card">
    <h1 className="title">{props.title}</h1>
    <h2 className="desg">{props.desg}</h2>
    <h3 className="desc">{props.desc}</h3>
    <button className="card_btn">Read More</button>
  </div>
);

const App = () => (
  <div className="cards">
    <Card title="Name" desg="Designation" desc="Description" />
  </div>
);

export default App;
```

11: Use `object destructuring` to reduce the length of the code

App.jsx

```js
import React from "react";

const Card = (props) => {
  const { title, desg, desc } = props;
  return (
    <div className="card">
      <h1 className="title">{title}</h1>
      <h2 className="desg">{desg}</h2>
      <h3 className="desc">{desc}</h3>
      <button className="card_btn">Read More</button>
    </div>
  );
};

const App = () => (
  <div className="cards">
    <Card title="Name" desg="Designation" desc="Description" />
  </div>
);

export default App;
```

12: Passing some data to `Card` component in `App.jsx` file

App.jsx

```js
import React from "react";

const Card = (props) => {
  const { title, desg, desc } = props;
  return (
    <div className="card">
      <h1 className="title">{title}</h1>
      <h2 className="desg">{desg}</h2>
      <h3 className="desc">{desc}</h3>
      <button className="card_btn">Read More</button>
    </div>
  );
};

const App = () => (
  <div className="cards">
    <Card
      title="Akash Patil"
      desg="Developer"
      desc="Interested to learn new things"
    />
    <Card
      title="Anupravi Garg"
      desg="Developer"
      desc="Interested in YouTube & Teaching"
    />
    <Card title="Abhi Pawar" desg="Student" desc="Creative Thinking" />
    <Card title="Anjali Takale" desg="Student" desc="New to development" />
    <Card title="Chanchal Khatri" desg="Student" desc="Learning new skills" />
    <Card title="Pooja Patil" desg="Student" desc="Developed some projects" />
    <Card title="Pranali Kale" desg="Student" desc="Learn and Develope" />
    <Card
      title="Trupti Jadhav"
      desg="Student"
      desc="Creative thinking and develop some projects"
    />
    <Card title="Tushar Mohite" desg="Student" desc="Just learning" />
  </div>
);

export default App;
```

13: Create an array of objects to store all data inside `App.jsx` file

```js
import React from "react";

const cardData = [
  {
    title: "Akash Patil",
    desg: "Developer",
    desc: "Interested to learn new things",
  },
  {
    title: "Anupravi Garg",
    desg: "Developer",
    desc: "Interested in YouTube & Teaching",
  },
  {
    title: "Abhi Pawar",
    desg: "Student",
    desc: "Creative Thinking",
  },
  {
    title: "Anjali Takale",
    desg: "Student",
    desc: "New to development",
  },
  {
    title: "Chanchal Khatri",
    desg: "Student",
    desc: "Learning new skills",
  },
  {
    title: "Pooja Patil",
    desg: "Student",
    desc: "Developed some projects",
  },
  {
    title: "Pranali Kale",
    desg: "Student",
    desc: "Learn and Develope",
  },
  {
    title: "Trupti Jadhav",
    desg: "Student",
    desc: "Creative thinking and develop some projects",
  },
  {
    title: "Tushar Mohite",
    desg: "Student",
    desc: "Just learning",
  },
];

const Card = (props) => {
  const { title, desg, desc } = props;
  return (
    <div className="card">
      <h1 className="title">{title}</h1>
      <h2 className="desg">{desg}</h2>
      <h3 className="desc">{desc}</h3>
      <button className="card_btn">Read More</button>
    </div>
  );
};

const App = () => (
  <div className="cards">
    <Card
      title="Akash Patil"
      desg="Developer"
      desc="Interested to learn new things"
    />
    <Card
      title="Anupravi Garg"
      desg="Developer"
      desc="Interested in YouTube & Teaching"
    />
    <Card title="Abhi Pawar" desg="Student" desc="Creative Thinking" />
    <Card title="Anjali Takale" desg="Student" desc="New to development" />
    <Card title="Chanchal Khatri" desg="Student" desc="Learning new skills" />
    <Card title="Pooja Patil" desg="Student" desc="Developed some projects" />
    <Card title="Pranali Kale" desg="Student" desc="Learn and Develope" />
    <Card
      title="Trupti Jadhav"
      desg="Student"
      desc="Creative thinking and develop some projects"
    />
    <Card title="Tushar Mohite" desg="Student" desc="Just learning" />
  </div>
);

export default App;
```

14: Pass array value to `Card` component as value

App.jsx

```js
import React from "react";

const cardData = [
  {
    title: "Akash Patil",
    desg: "Developer",
    desc: "Interested to learn new things",
  },
  {
    title: "Anupravi Garg",
    desg: "Developer",
    desc: "Interested in YouTube & Teaching",
  },
  {
    title: "Abhi Pawar",
    desg: "Student",
    desc: "Creative Thinking",
  },
  {
    title: "Anjali Takale",
    desg: "Student",
    desc: "New to development",
  },
  {
    title: "Chanchal Khatri",
    desg: "Student",
    desc: "Learning new skills",
  },
  {
    title: "Pooja Patil",
    desg: "Student",
    desc: "Developed some projects",
  },
  {
    title: "Pranali Kale",
    desg: "Student",
    desc: "Learn and Develope",
  },
  {
    title: "Trupti Jadhav",
    desg: "Student",
    desc: "Creative thinking and develop some projects",
  },
  {
    title: "Tushar Mohite",
    desg: "Student",
    desc: "Just learning",
  },
];

const Card = (props) => {
  const { title, desg, desc } = props;
  return (
    <div className="card">
      <h1 className="title">{title}</h1>
      <h2 className="desg">{desg}</h2>
      <h3 className="desc">{desc}</h3>
      <button className="card_btn">Read More</button>
    </div>
  );
};

const App = () => (
  <div className="cards">
    <Card
      title={cardData[0].title}
      desg={cardData[0].desg}
      desc={cardData[0].desc}
    />
    <Card
      title={cardData[1].title}
      desg={cardData[1].desg}
      desc={cardData[1].desc}
    />
    <Card
      title={cardData[2].title}
      desg={cardData[2].desg}
      desc={cardData[2].desc}
    />
    <Card
      title={cardData[3].title}
      desg={cardData[3].desg}
      desc={cardData[3].desc}
    />
    <Card
      title={cardData[4].title}
      desg={cardData[4].desg}
      desc={cardData[4].desc}
    />
    <Card
      title={cardData[5].title}
      desg={cardData[5].desg}
      desc={cardData[5].desc}
    />
    <Card
      title={cardData[6].title}
      desg={cardData[6].desg}
      desc={cardData[6].desc}
    />
    <Card
      title={cardData[7].title}
      desg={cardData[7].desg}
      desc={cardData[7].desc}
    />
    <Card
      title={cardData[8].title}
      desg={cardData[8].desg}
      desc={cardData[8].desc}
    />
  </div>
);

export default App;
```

15: Create a `components` folder inside the `src` folder and create a `cardData.jsx` file inside it and remove `cardData` array from `App.jsx` file and add it to the `cardData.jsx` file and `import` `cardData.jsx` file in `App.jsx` file

App.jsx

```js
import React from "react";
import cardData from "./components/cardData";

const Card = (props) => {
  const { title, desg, desc } = props;
  return (
    <div className="card">
      <h1 className="title">{title}</h1>
      <h2 className="desg">{desg}</h2>
      <h3 className="desc">{desc}</h3>
      <button className="card_btn">Read More</button>
    </div>
  );
};

const App = () => (
  <div className="cards">
    <Card
      title={cardData[0].title}
      desg={cardData[0].desg}
      desc={cardData[0].desc}
    />
    <Card
      title={cardData[1].title}
      desg={cardData[1].desg}
      desc={cardData[1].desc}
    />
    <Card
      title={cardData[2].title}
      desg={cardData[2].desg}
      desc={cardData[2].desc}
    />
    <Card
      title={cardData[3].title}
      desg={cardData[3].desg}
      desc={cardData[3].desc}
    />
    <Card
      title={cardData[4].title}
      desg={cardData[4].desg}
      desc={cardData[4].desc}
    />
    <Card
      title={cardData[5].title}
      desg={cardData[5].desg}
      desc={cardData[5].desc}
    />
    <Card
      title={cardData[6].title}
      desg={cardData[6].desg}
      desc={cardData[6].desc}
    />
    <Card
      title={cardData[7].title}
      desg={cardData[7].desg}
      desc={cardData[7].desc}
    />
    <Card
      title={cardData[8].title}
      desg={cardData[8].desg}
      desc={cardData[8].desc}
    />
  </div>
);

export default App;
```

cardData.jsx

```js
const cardData = [
  {
    title: "Akash Patil",
    desg: "Developer",
    desc: "Interested to learn new things",
  },
  {
    title: "Anupravi Garg",
    desg: "Developer",
    desc: "Interested in YouTube & Teaching",
  },
  {
    title: "Abhi Pawar",
    desg: "Student",
    desc: "Creative Thinking",
  },
  {
    title: "Anjali Takale",
    desg: "Student",
    desc: "New to development",
  },
  {
    title: "Chanchal Khatri",
    desg: "Student",
    desc: "Learning new skills",
  },
  {
    title: "Pooja Patil",
    desg: "Student",
    desc: "Developed some projects",
  },
  {
    title: "Pranali Kale",
    desg: "Student",
    desc: "Learn and Develope",
  },
  {
    title: "Trupti Jadhav",
    desg: "Student",
    desc: "Creative thinking and develop some projects",
  },
  {
    title: "Tushar Mohite",
    desg: "Student",
    desc: "Just learning",
  },
];

export default cardData;
```

16: Create a `Card.jsx` file and add a `Card` component to it from `App.jsx` file

Card.jsx

```js
import React from "react";

const Card = (props) => {
  const { title, desg, desc } = props;
  return (
    <div className="card">
      <h1 className="title">{title}</h1>
      <h2 className="desg">{desg}</h2>
      <h3 className="desc">{desc}</h3>
      <button className="card_btn">Read More</button>
    </div>
  );
};

export default Card;
```

App.jsx

```js
import React from "react";
import Card from "./components/Card";
import cardData from "./components/cardData";

const App = () => (
  <div className="cards">
    <Card
      title={cardData[0].title}
      desg={cardData[0].desg}
      desc={cardData[0].desc}
    />
  </div>
);

export default App;
```

17: Use the `map` method to reduce code repetition and use it for iteration

App.jsx

```js
import React from "react";
import Card from "./components/Card";
import cardData from "./components/cardData";

const nData = (val) => (
  <Card title={val.title} desg={val.desg} desc={val.desc} />
);
const App = () => <div className="cards">{cardData.map(nData)}</div>;

export default App;
```

or

App.jsx

```js
import React from "react";
import Card from "./components/Card";
import cardData from "./components/cardData";

const App = () => (
  <div className="cards">
    {cardData.map((val) => (
      <Card title={val.title} desg={val.desg} desc={val.desc} />
    ))}
  </div>
);

export default App;
```
