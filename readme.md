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

### What is a high order component in React?
Higher-order components (HOCs) are a powerful feature of the React library. They allow you to reuse component logic across multiple components. In React, a higher-order component is **a function that takes a component as an argument and returns a new component that wraps the original component**.

### What are stateless components?
Stateless components, also known as functional components, are a type of React component that is defined as a simple JavaScript function rather than a class. These components are called "stateless" because they don't have their own state. Instead, they receive data and behaviors through props and are primarily used for rendering UI based on the props they receive.

Here's an example of a stateless component in React:

```jsx
import React from 'react';

// Stateless Component (Functional Component)
const Greeting = (props) => {
  return (
    <div>
      <h1>Hello, {props.name}!</h1>
    </div>
  );
};

// Usage of the Stateless Component
const App = () => {
  return (
    <div>
      <Greeting name="John" />
      <Greeting name="Jane" />
    </div>
  );
};

export default App;
```

In this example, `Greeting` is a stateless component. It is a simple function that takes `props` as an argument and returns JSX representing the UI. The `App` component uses the `Greeting` component twice, passing different names as props.

Key characteristics of stateless components:

1. **No State:**
   - Stateless components do not have their own state. They receive data via props and render based on that data.

2. **Functional Syntax:**
   - Stateless components are defined using a functional syntax, as opposed to class components. They are just JavaScript functions.

3. **No Lifecycle Methods:**
   - Stateless components do not have lifecycle methods like `componentDidMount`, `componentDidUpdate`, etc. These methods are specific to class components.

4. **Simpler Syntax:**
   - Stateless components have a simpler syntax and are often used for simple presentational components that don't require internal state or lifecycle methods.

Functional components have become more powerful with the introduction of React Hooks, which allow functional components to use state and other React features traditionally associated with class components. Hooks make it easier to manage stateful logic in functional components, reducing the need for class components in many cases.

### What are stateful components?
Stateful components, also known as class components, are a type of React component that is defined using ES6 class syntax. Unlike stateless components (functional components), stateful components have the ability to maintain and manage their own internal state using the `setState` method. Stateful components are typically used when a component needs to manage changing data or respond to user interactions over time.

### Explain the callback function.
A callback function is a function that is passed as an argument to another function and is executed after the completion of some asynchronous operation or at a later time. Callback functions are commonly used in JavaScript to handle events, manage asynchronous tasks, and achieve non-blocking behavior.

Here's a simple example to illustrate the concept of a callback function in JavaScript:

```javascript
// Example of a Callback Function
function doSomethingAsync(callback) {
  setTimeout(function () {
    console.log("Async operation completed.");
    callback(); // Execute the callback function
  }, 1000);
}

// Usage of the Callback Function
function handleCallback() {
  console.log("Callback executed!");
}

// Pass the callback function to doSomethingAsync
doSomethingAsync(handleCallback);
```

In this example:

1. The `doSomethingAsync` function takes a callback function as an argument.
2. Inside `doSomethingAsync`, there is a `setTimeout` function that simulates an asynchronous operation (in this case, a delay of 1000 milliseconds).
3. After the asynchronous operation completes, the provided callback function (`callback()`) is executed.

In the usage part, the `handleCallback` function is passed as a callback to `doSomethingAsync`. When the asynchronous operation inside `doSomethingAsync` is completed, it calls the provided callback function (`handleCallback` in this case).

Callbacks are particularly common in scenarios where you're working with asynchronous operations, such as AJAX requests, setTimeout, event handling, and more. While callbacks are a valid and widely used pattern, they can sometimes lead to callback hell (nested and hard-to-read code) when dealing with multiple asynchronous operations.

Modern JavaScript has introduced features like Promises and async/await to handle asynchronous code more cleanly and manageably. Promises and async/await can be seen as alternatives to callback patterns for handling asynchronous operations in a more structured and readable way.

### Mention one difference between Props and State.

One key difference between props and state in React is that props are passed into a component, while state is managed within the component.

1. **Props:**
   - **Immutable:** Props are passed to a component by its parent component, and the component cannot modify its props. They are immutable and are used to pass data from a parent component to a child component.

   ```jsx
   // Parent Component
   const App = () => {
     return <ChildComponent name="John" />;
   };

   // Child Component
   const ChildComponent = (props) => {
     return <p>Hello, {props.name}!</p>;
   };
   ```

2. **State:**
   - **Mutable:** State, on the other hand, is managed within the component and can be modified using the `setState` method. State is used for managing data that may change over time within the component.

   ```jsx
   // Stateful Component
   class Counter extends React.Component {
     constructor(props) {
       super(props);
       this.state = {
         count: 0,
       };
     }

     incrementCount = () => {
       // Modifying the state using setState
       this.setState((prevState) => ({ count: prevState.count + 1 }));
     };

     render() {
       return (
         <div>
           <p>Count: {this.state.count}</p>
           <button onClick={this.incrementCount}>Increment</button>
         </div>
       );
     }
   }
   ```

In summary, props are used for passing data from a parent component to a child component, and they are immutable within the child component. State, on the other hand, is used for managing internal data within a component, and it can be modified through the use of the `setState` method.


### What are pure components in ReactJS?
A React component is considered to be pure if it produces the same output when given the same set of state and props.

While pure components can improve performance by reducing unnecessary renders, it's important to note that they are effective when dealing with simple data types and shallow data structures. For complex data structures or nested objects, you might need to consider other techniques, such as using the `shouldComponentUpdate` method manually or using memoization libraries like `memo` for functional components.

### Explain Lifting State Up in React.
When multiple components need to share the same data, it is advised to lift the shared state up to their parent. This means when two child components share the same data from their parent, the state is lifted up to the parent instead of the child components.


### how you can update props in React
In React, props are used to pass data from a parent component to a child component. Once props are passed to a child component, they are immutable, meaning that the child component cannot directly modify the props it receives. However, the parent component, which owns the data, can update the props and trigger a re-render of the child component with the updated data.


Here's how you can update props in React:
#### 1. Parent Component State:

The most common way to update props is by managing the data in the state of the parent component. When the state of the parent component changes, it triggers a re-render, and the updated data is passed as new props to the child component.

Example:

```jsx
import React, { useState } from 'react';
import ChildComponent from './ChildComponent';

const ParentComponent = () => {
  const [data, setData] = useState('Initial Data');

  const updateData = () => {
    // Update the state, triggering a re-render
    setData('Updated Data');
  };

  return (
    <div>
      <ChildComponent data={data} />
      <button onClick={updateData}>Update Data</button>
    </div>
  );
};

export default ParentComponent;
```

#### 2. Prop Drilling:

Prop drilling involves passing down a function from a parent component to a child component as a prop. The child component can then call this function to request updates to the props. While this is a valid approach, it may not be suitable for deep component hierarchies, as passing the function through multiple layers of components can become cumbersome.

Example:

```jsx
import React, { useState } from 'react';
import ChildComponent from './ChildComponent';

const ParentComponent = () => {
  const [data, setData] = useState('Initial Data');

  const updateData = () => {
    // Update the state, triggering a re-render
    setData('Updated Data');
  };

  return (
    <div>
      <ChildComponent data={data} updateData={updateData} />
    </div>
  );
};

export default ParentComponent;
```

In `ChildComponent`:

```jsx
import React from 'react';

const ChildComponent = ({ data, updateData }) => {
  return (
    <div>
      <p>{data}</p>
      <button onClick={updateData}>Update Data</button>
    </div>
  );
};

export default ChildComponent;
```

#### 3. Context API:

For more complex scenarios where prop drilling becomes impractical, you can use React Context to manage shared state at a higher level and provide it to components without passing props explicitly.

Example:

```jsx
import React, { useState, createContext, useContext } from 'react';
import ChildComponent from './ChildComponent';

const DataContext = createContext();

const ParentComponent = () => {
  const [data, setData] = useState('Initial Data');

  const updateData = () => {
    // Update the state, triggering a re-render
    setData('Updated Data');
  };

  return (
    <DataContext.Provider value={{ data, updateData }}>
      <ChildComponent />
    </DataContext.Provider>
  );
};

export default ParentComponent;
```

In `ChildComponent`:

```jsx
import React, { useContext } from 'react';
import { DataContext } from './ParentComponent';

const ChildComponent = () => {
  const { data, updateData } = useContext(DataContext);

  return (
    <div>
      <p>{data}</p>
      <button onClick={updateData}>Update Data</button>
    </div>
  );
};

export default ChildComponent;
```

Using any of these methods, you can effectively update props in React by managing the data at the parent level and passing it down to child components. The choice between these methods depends on the complexity and structure of your application.

### What are refs?
Refs, short for "references," are a feature in React that provide a way to interact with the DOM (Document Object Model) or to reference React elements. Refs allow you to access and interact with a DOM element or a React component directly. They are useful in scenarios where you need to imperatively manipulate the DOM, manage focus, trigger animations, or access methods and properties of a child component.

There are two types of refs in React: **string refs** (legacy) and **function refs** (modern).

Function Refs (Modern):

Function refs involve using a callback function as a ref, which receives the reference to the DOM element or React component as an argument. This is the recommended approach for creating refs in modern React.

Example:

```jsx
import React, { useRef, useEffect } from 'react';

function MyComponent() {
  const myInput = useRef(null);

  useEffect(() => {
    myInput.current.focus(); // access the DOM element
  }, []);

  return <input ref={myInput} />;
}
```

#### Key points about refs:

- Refs are created using the `useRef` hook in functional components or by creating a class property and initializing it with `React.createRef()` in class components.
- Refs can be attached to both functional and class components.
- When using function refs, the ref object (`myInput` in the example) persists across renders, so it can be accessed outside the render function.
- Refs are commonly used for accessing DOM elements, managing focus, triggering animations, or communicating with child components.

While refs provide a way to access and interact with the DOM, it's important to use them sparingly and favor declarative approaches when possible. Direct DOM manipulation should generally be avoided in React, as it can lead to harder-to-maintain code and potential performance issues.







## Coding 
Interviewer:
Could you describe a scenario where you've had to implement a feature that involves multiple select options, such as selecting a city and its corresponding zones, and how you approached it using React?
```jsx
import React, { useState } from 'react';

const citiesData = {
  'New York': ['Manhattan', 'Brooklyn', 'Queens'],
  'Los Angeles': ['Hollywood', 'Downtown', 'Santa Monica'],
  Chicago: ['Loop', 'Near North Side', 'West Loop'],
};

const LoadZoneData = () => {
  const [selectedCity, setSelectedCity] = useState('');
  const [selectedZone, setSelectedZone] = useState('');
  const [zones, setZones] = useState([]);

  const handleCityChange = (e) => {
    const city = e.target.value;
    setSelectedCity(city);
    setSelectedZone('');
    setZones(citiesData[city] || []);
  };

  const handleZoneChange = (e) => {
    setSelectedZone(e.target.value);
  };

  return (
    <div className="container">
      <h1>Select City and Zone</h1>
      <div className="select-container">
        <label htmlFor="citySelect">Select City:</label>
        <select
          id="citySelect"
          value={selectedCity}
          onChange={handleCityChange}
        >
          <option value="">Select a city</option>
          {Object.keys(citiesData).map((city) => (
            <option key={city} value={city}>
              {city}
            </option>
          ))}
        </select>
      </div>
      <div className="select-container">
        <label htmlFor="zoneSelect">Select Zone:</label>
        <select
          id="zoneSelect"
          value={selectedZone}
          onChange={handleZoneChange}
          disabled={!selectedCity || zones.length === 0}
        >
          <option value="">Select a zone</option>
          {zones.map((zone) => (
            <option key={zone} value={zone}>
              {zone}
            </option>
          ))}
        </select>
      </div>
      {!selectedCity && <p className="error">Please select a city</p>}
      {selectedCity && zones.length === 0 && (
        <p className="error">No zones available for selected city</p>
      )}
    </div>
  );
};

export default LoadZoneData;
```
### Interviewer: Can you explain how the sort() function works in JavaScript?

#### Description of sort() function:

The sort() function in JavaScript is used to sort the elements of an array in place and returns the sorted array. By default, the elements are sorted in ascending order, based on their UTF-16 code unit values. However, you can provide a custom sorting function as an argument to define your own sorting criteria.

#### Why use sort() and when to use it:

sort() is incredibly useful whenever you need to organize elements in an array, especially when dealing with data that needs to be presented in a specific order. Whether it's numbers, strings, or complex objects, sort() provides a convenient way to arrange data according to various criteria. It's particularly handy in scenarios like generating sorted lists, implementing search algorithms, or arranging user-generated content.

Real-life example use of sort() using React:

In a React application, imagine you have an array of objects representing tasks in a to-do list, and you want to display them sorted by priority. You can utilize sort() to dynamically reorder the tasks based on their priority attribute.

import React, { useState } from 'react';
```
const ToDoList = () => {
  const [tasks, setTasks] = useState([
    { id: 1, description: 'Complete assignment', priority: 2 },
    { id: 2, description: 'Prepare for meeting', priority: 1 },
    { id: 3, description: 'Send out emails', priority: 3 }
  ]);

  const sortByPriority = () => {
    const sortedTasks = [...tasks].sort((a, b) => a.priority - b.priority);
    setTasks(sortedTasks);
  };

  return (
    <div>
      <button onClick={sortByPriority}>Sort by Priority</button>
      <ul>
        {tasks.map(task => (
          <li key={task.id}>{task.description} (Priority: {task.priority})</li>
        ))}
      </ul>
    </div>
  );
};

export default ToDoList;
```
