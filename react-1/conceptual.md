### Conceptual Exercise

Answer the following questions below:

- What is React? When and why would you use it?  
  React is a popular front-end library that simplifies building user interfaces. It excels at managing dynamic and interactive web pages with minimal code duplication. Consider using React when you need to create reusable UI components, manage complex state changes, or build performant single-page applications (SPAs).

- What is Babel?  
  Babel acts as a transpiler, transforming modern JavaScript code into a format compatible with older browsers. This ensures your cutting-edge code can still run on browsers that haven't adopted the latest JavaScript features.

- What is JSX?  
  JSX stands for JavaScript XML. It's a syntax extension that allows you to write HTML-like structures within JavaScript code. This enables you to define the look and feel of your components directly within your React code, improving readability and maintainability.

- How is a Component created in React?  
  React components are the building blocks of your user interface. They are typically defined as functions (or classes in older versions) that utilize JSX to describe the component's appearance. These functions return the JSX code that React will render on the screen.

- What are some difference between state and props?  
  - Props: Props act like arguments passed into a component function. They provide a way to send data from parent components down to their children. Props are always received as objects and are immutable within the receiving component.
  - State: State represents data specific to a component that may change over time. Unlike props, state can be modified within the component using the `useState` hook. This allows components to react to user interactions or external events.

- What does "downward data flow" refer to in React?  
  In React, data typically flows downwards from parent to child components. This promotes a clear separation of concerns and makes it easier to manage complex UIs. Parent components act as "smart" components, managing data and passing it down to simpler child components that focus on presentation.

- What is a controlled component?  
  Controlled components are forms where React manages the input values. Each input element's value is stored within the component's state, and any changes are reflected back into the form. This approach offers more control over form data validation and manipulation.

- What is an uncontrolled component?  
  Uncontrolled components represent a simpler form approach. Here, the form elements hold their own values, and React retrieves them when the form is submitted. This method is suitable for basic forms where immediate state management isn't critical.

- What is the purpose of the `key` prop when rendering a list of components?  
  The `key` prop is essential when rendering lists of components. It acts as a unique identifier for each item, allowing React to efficiently track changes and optimize re-renders. Using keys helps React determine which components need to be updated, added, or removed when the list data changes.

- Why is using an array index a poor choice for a `key` prop when rendering a list of components?  
  While tempting, using array indexes as keys is generally discouraged. This is because indexes can change if items are reordered in the list. This can lead to unexpected behavior and make it harder for React to identify the correct components to update.

- Describe useEffect.  What use cases is it used for in React components?  
  The `useEffect` hook allows you to perform side effects within functional components. Side effects include actions like fetching data from APIs, setting up subscriptions, or manipulating the DOM. You can optionally configure `useEffect` to run only on specific conditions or after specific state changes.

- What does useRef do?  Does a change to a ref value cause a rerender of a component?  
  The `useRef` hook creates a reference object that persists throughout the component lifecycle. It allows you to directly access DOM elements, store mutable values, or create references to timers. Importantly, changes to the ref value itself don't trigger re-renders.

- When would you use a ref? When wouldn't you use one?  
  Refs are ideal for situations where state management isn't the best solution. Common use cases include accessing DOM elements for manual manipulation, focusing form elements, or persisting values across re-renders that don't affect the component's appearance. However, avoid using refs for data management that could be handled with state.

- What is a custom hook in React? When would you want to write one?  
  Custom hooks are functions that allow you to create reusable pieces of logic that utilize other React hooks. They are ideal for encapsulating common patterns or side effects that can be shared across multiple components in your application. This promotes code organization and reduces redundancy.
