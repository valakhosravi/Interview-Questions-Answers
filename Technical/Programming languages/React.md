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



