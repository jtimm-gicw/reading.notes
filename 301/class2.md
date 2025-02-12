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
