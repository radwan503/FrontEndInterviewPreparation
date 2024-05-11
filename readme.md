# Front End Engineer Interview Question and Answer
### Click ⭐if you like the project. Pull Request are highly appreciated. Follow me @radwanahmedanik for more updates.


### What is React Js
- React Js is open source javascript library. which is develop for single page web app and complex UI
  
### Some Feature of React
 - use virtual DOM,insted for real DOM
 - Render HTML files in server side, That means server side rendering
 - React js pass data top bottom that means unidirectional flow
### Advantage of React
- Enhanced the performance of application
   - React's virtual DOM and efficient diffing algorithm contribute to enhanced performance. Components only update the parts of the DOM that have changed, reducing unnecessary re-rendering.
- easy to write reusable code
- easy to testing
- readability of code is higher because of JSX
- Is can used from client side as well as server side
   - React supports both client-side and server-side rendering, improving initial load times and SEO.

### What is .js and .jsx different in React
JSX stands for **JavaScript XML**. JSX allows us to write HTML in React.JSX is the syntax extension for Javascript in React.js.
#### Example using `.js` Extension:
**App.js:**
```javascript
// App.js with JSX code written in a .js file
import React from 'react';

const App = () => {
  return (
    <div>
      <h1>Hello, World!</h1>
    </div>
  );
};

export default App;
```
In this example, JSX code is written inside a file with a `.js` extension. To make this work, you would typically configure Babel with `@babel/preset-react` in your project's `.babelrc` or `babel.config.js` file.

#### Example using `.jsx` Extension:

**App.jsx:**
```jsx
// App.jsx with JSX code written in a .jsx file
import React from 'react';

const App = () => {
  return (
    <div>
      <h1>Hello, World!</h1>
    </div>
  );
};

export default App;
```

In this example, JSX code is written inside a file with a `.jsx` extension. This is a common convention in React projects, and using the `.jsx` extension helps convey that the file likely contains JSX code without the need for additional configuration.

While both examples achieve the same result, using the `.jsx` extension is a convention that aids in codebase readability and understanding, as it signals the presence of JSX to developers and tools.

### Why are keys used in react js
- In React.js, keys are used in lists to help React identify which items have changed, been added, or been removed. When rendering a dynamic list of components or elements, React uses keys to efficiently update the DOM and manage component state.
- Keys help React identify the uniqueness of each item in a list. When an item is added, removed, or re-ordered, React can efficiently update the DOM by selectively modifying only the necessary parts of the UI.
- Without keys, React might re-render the entire list when there are changes. Keys enable React to identify specific elements and only re-render the components that have changed or need updating.

### Difference between Real DOM Vs Virtual DOM

The fundamental contrast between the DOM and Virtual DOM is that **the DOM represents the actual HTML structure of a web page, while the Virtual DOM is a lightweight copy of the DOM used by React to enhance performance while updating the actual DOM.

#### Real DOM
- Real DOM represent actual structure of the webpage.
- DOM manipulation is very expensive
- There is too much memory wastage
- It updates Slow
- It can directly update HTML

#### Virtual DOM
- Virtual DOM represent the virtual/memory representation of the Webpage.
- DOM manipulation is very easy
- No memory wastage
- It updates fast
- It can’t update HTML directly
