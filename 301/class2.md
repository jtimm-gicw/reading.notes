# 301-Read_02

## Questions

1. Based off the diagram, what happens first, the ‘render’ or the ‘**componentDidMount**’?
*componentDidMount*, This method is invoked immediately after a component is mounted.
2. What is the very first thing to happen in the lifecycle of React?
Mounting
3. Put the following things in the order that they happen: componentDidMount, render, constructor, componentWillUnmount, React Updates
**Final Order of Execution:**
1️⃣ constructor() → (if present)
2️⃣ render() → (UI is generated)
3️⃣ componentDidMount() → (Runs after mounting, e.g., fetching data)
4️⃣ React Updates → (Component re-renders if state/props change)
5️⃣ componentWillUnmount() → (Cleanup before the component is removed)
4. What does componentDidMount do?
**componentDidMount()** is a lifecycle method in React that runs after a component has been added to the DOM (mounted).

👉 It is mainly used for:
✅ Fetching data from an API
✅ Setting up event listeners
✅ Subscribing to services
✅ Updating the state after the initial render
### Notes
React lets you define components as *classes or functions*. The **methods** that you are able to use on these are called **lifecycle events**.
Methods can be **called** during the **lifecycle of a component**, and they allow you to update the UI and application states.

### Video
1. What types of things can you pass in the props?
In React, you can pass various types of data as props to components. 
- strings
- booleans
- numbers 
- null
- objects
- arrays
- function (callback functions)
- JSX components 
- React elements

2. What is the big difference between props and state?
The big difference between props and state in React is:
**Props are immutable (read-only) and passed from *parent to child* components.** They allow data to flow down the component tree but cannot be changed by the receiving component.
**State is mutable (changeable) and managed *within* a component.** It allows a component to track and update data dynamically.

3. When do we re-render our application?
**State Changes →** If you update a component's state using useState or this.setState, React re-renders that component.
**Props Change →** If a parent component passes new props to a child component, the child re-renders.

4. What are some examples of things that we could store in state?
1️⃣ User Input (Forms)
- Storing values typed by a user in an input field.
2️⃣ Counters & Numbers
- Storing and updating a counter value.
3️⃣ Boolean Flags (UI State)
- Tracking things like modals, dropdowns, or dark mode.
4️⃣ Lists & Arrays
- Keeping track of multiple items (e.g., a to-do list).
5️⃣ Objects (User Data, API Responses)
- Storing data like user profiles.
6️⃣ Fetched Data (from APIs)
- Storing API responses dynamically.
7️⃣ Theme (Dark Mode, Language)
- Switching between light and dark mode.

### Additional Notes


