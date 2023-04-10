# React
## Basic
**Q: What is React?**  
React is a JavaScript library for building user interfaces. It is based on the concept of components, which are reusable UI building blocks that can be composed together to create complex UIs. React was developed by Facebook and is widely used in web development.

**Q: What is JSX?**  
JSX is a syntax extension for JavaScript that allows you to write HTML-like code in your JavaScript files. It is used to describe the UI components in React.

**Q: What is the difference between props and state in React?**  
Props and state are both used to pass data to a React component, but there are some key differences between them. Props are passed down from a parent component to a child component, and are read-only. State is used to manage the internal state of a component, and can be updated using the setState method.

**Q: What is the virtual DOM in React?**  
The virtual DOM is a concept in React that allows for efficient updates to the UI. Instead of updating the actual DOM directly, React maintains a virtual copy of the DOM in memory. When a change is made to the UI, React compares the virtual DOM to the real DOM and only updates the parts that have changed.

**Q: What is a higher-order component (HOC) in React?**  
A higher-order component is a function that takes a component and returns a new component with additional functionality. HOCs are used to abstract common functionality into a reusable component.

**Q: What is the difference between a controlled and an uncontrolled component in React?**  
In a controlled component, the state of the component is managed by React. Changes to the state are handled by the component's props and are passed down from the parent component. In an uncontrolled component, the state is managed by the DOM. Changes to the state are handled by the user input directly.

**Q: What is Redux in React?**  
Redux is a state management library for React. It provides a centralized store for managing the state of the application. Redux is often used in large-scale React applications to manage complex state and make it easier to reason about.

**Q: What is the difference between a presentational component and a container component in React?**  
A presentational component is focused on rendering UI elements and is often used to define the look and feel of a component. A container component is focused on data management and typically manages the state of one or more presentational components.

**Q: What is the difference between componentDidMount and componentDidUpdate in React?**  
componentDidMount is called once the component has mounted and is rendered for the first time. componentDidUpdate is called after a component updates and re-renders.

**Q: What are React hooks?**  
React hooks are functions that allow you to use state and other React features without writing a class component. Hooks were introduced in React 16.8 and include useState, useEffect, useContext, and more. They make it easier to write reusable and composable React components.

**Q: Why do we need to use the key property in React? What are the benefits of using key when rendering a list of elements?**  
A: In React, the key property is used to identify individual elements in a list of elements that are rendered dynamically. When rendering a list of elements using an array in React, each element needs a unique identifier so that React can efficiently update and re-render the list when necessary.

Here's why we need the key property in React:

- Efficient updates: When a list of elements is rendered dynamically, React needs to keep track of the individual elements so that it can efficiently update and re-render them when necessary. Without a key property, React would have to compare each element in the list to determine which elements have changed and need to be re-rendered, which can be slow and inefficient.

- Prevent errors: Using a key property helps prevent errors that can occur when rendering a list of elements. If two elements in the list have the same key property, React will throw an error, as each element in the list needs to have a unique identifier.

- Maintain state: When a list of elements is re-rendered, React maintains the state of the individual elements using their key property. This means that if an element changes position in the list, React can still maintain its state and prevent it from being re-initialized.

In summary, the key property in React is used to identify individual elements in a list of elements so that React can efficiently update and re-render the list when necessary, prevent errors, and maintain the state of the individual elements.

**Q: How to prevent components from re-rendering?**  
1. Use shouldComponentUpdate or React.memo: You can implement the shouldComponentUpdate lifecycle method or use the React.memo higher-order component to tell React when a component should re-render. By implementing shouldComponentUpdate, you can define conditions that must be met before a component re-renders. React.memo, on the other hand, is a higher-order component that wraps a functional component and memoizes it so that it only re-renders when its props change.

2. Use PureComponent: You can use the PureComponent class component in React, which automatically implements the shouldComponentUpdate method by performing a shallow comparison of the component's props and state. If the props and state are the same as the previous render, the component won't re-render.

3. Use a key property: When rendering a list of components, you can assign a unique key to each component to help React efficiently update the list without re-rendering unnecessary components. If the key remains the same, React will know that the component hasn't changed and won't re-render it.

4. Use state management libraries: Using state management libraries such as Redux or MobX can also help prevent unnecessary re-renders by optimizing the flow of data between components.

In summary, there are several ways to prevent components from re-rendering in React, including implementing shouldComponentUpdate or React.memo, using PureComponent, using a key property, and using state management libraries. Choosing the appropriate method depends on the specific use case and the requirements of the application.
## Advanced
**Q: Imagine you have a React application with a parent component, a child component, and a grandchild component. Can you describe in what order the lifecycle methods of each component are called during the mounting, updating, and unmounting phases?**  
A: When a parent component renders its child component, and the child component renders its own child component, the lifecycle methods are called in the following order:

**Mounting:**

- Parent component: constructor() -> getDerivedStateFromProps() -> render() -> componentDidMount()
- Child component: constructor() -> getDerivedStateFromProps() -> render() -> componentDidMount()
- Grandchild component: constructor() -> getDerivedStateFromProps() -> render() -> componentDidMount()

**Updating:**

When a state or prop change occurs in the parent component, the following methods are called in order:

- Parent component: getDerivedStateFromProps() -> shouldComponentUpdate() -> render() -> getSnapshotBeforeUpdate() -> componentDidUpdate()
- Child component: getDerivedStateFromProps() -> shouldComponentUpdate() -> render() -> getSnapshotBeforeUpdate() -> componentDidUpdate()
- Grandchild component: getDerivedStateFromProps() -> shouldComponentUpdate() -> render() -> getSnapshotBeforeUpdate() -> componentDidUpdate()
When a state or prop change occurs in the child component, the following methods are called in order:

- Child component: getDerivedStateFromProps() -> shouldComponentUpdate() -> render() -> getSnapshotBeforeUpdate() -> componentDidUpdate()
- Grandchild component: getDerivedStateFromProps() -> shouldComponentUpdate() -> render() -> getSnapshotBeforeUpdate() -> componentDidUpdate()

Note that the parent component's lifecycle methods are not called in this scenario.

**Unmounting:**

When the parent component is unmounted, the following method is called in order:

- Parent component: componentWillUnmount()
- Child component: componentWillUnmount()
- Grandchild component: componentWillUnmount()

Note that when the child or grandchild component is unmounted, only its own componentWillUnmount() method is called. The parent component's lifecycle methods are not affected by the unmounting of its child components.

**Q: What is the difference between using const and Object.freeze() in JavaScript when it comes to creating immutable variables? Can you give an example of how each works and when you would choose one over the other?**  
In JavaScript, const and Object.freeze() are both used to create immutable variables, but they have different use cases and behaviors.

const is used to declare a variable that cannot be reassigned, meaning its reference to the value it holds cannot be changed. However, it doesn't make the value itself immutable. This means that if the variable holds an object or an array, the properties or elements of the object or array can still be modified.

For example:

    const myObj = {name: 'John'};
    myObj.name = 'Jane'; // Valid, but reassigning myObj would not be allowed
On the other hand, Object.freeze() is used to create an immutable object by preventing any changes to its properties or elements. Once an object is frozen, it cannot be modified in any way, including adding or removing properties or changing the values of existing properties.

For example:

    const myFrozenObj = Object.freeze({name: 'John'});
    myFrozenObj.name = 'Jane'; // Invalid, since myFrozenObj is immutable
To summarize, const is used to declare a variable that cannot be reassigned, whereas Object.freeze() is used to create an immutable object that cannot be modified.

**Q: What is the difference between controlled and uncontrolled components in React? When would you use one over the other?**  
In React, there are two ways to manage form inputs: controlled components and uncontrolled components. The main difference between the two is how they handle and update the input values.

Controlled Components:

- Controlled components are components in which the value of the input is controlled by the component's state.
- When the user types something into the input, it triggers an onChange event which updates the component's state, which in turn updates the value of the input.
- The value of the input is always synced with the component's state, so you can easily access and manipulate it through the state.
- Controlled components are often used when you need to have more control over the form data and need to perform some validation or formatting before submitting the data.

Uncontrolled Components:

- Uncontrolled components are components in which the value of the input is handled by the DOM.
- When the user types something into the input, the DOM handles the value and the component does not have any direct control over it.
- To get the value of the input, you need to use a ref to access the DOM node.
- Uncontrolled components are often used when you don't need to do any validation or formatting on the data and just want to get the data and submit it as is.

In summary, controlled components use React state to manage the value of the input, while uncontrolled components rely on the DOM to handle the value. Controlled components give you more control and flexibility over the form data, while uncontrolled components are simpler to use and require less code.

