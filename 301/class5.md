# 301-Read_05

## Questions

### Thinking in React
1. What is the single responsibility principle and how does it apply to components?

2. What does it mean to build a ‘static’ version of your application? 
The **Single Responsibility Principle (SRP)** is one of the SOLID principles of software design. It states *that a module, class, or function should have only one reason to change*—in other words, it should only be responsible for one aspect of the application.

3. Once you have a static application, what do you need to add?
    *State Management*
Use React’s useState hook to store and update dynamic data.
Move the state up to a common ancestor if multiple components need access.
    *Event Handling*
Add event listeners (e.g., onClick, onChange) to handle user interactions.
Define functions to update state based on user actions.
    *Props and State Coordination*
Pass props from parent to child components.
Lift state up when multiple components need to share data.
    *Lifecycle Effects (useEffect)*
Fetch data from an API or perform side effects using useEffect.
    *Routing (Optional)*
If your app has multiple pages, use React Router to add navigation.
4. What are the three questions you can ask to determine if something is state?
To determine if something should be state in a React application, ask yourself these three questions:
    *Can the data be computed from existing props or state?*
If the value can be derived from props or other state, it should not be state.
Instead, compute it dynamically using a function or derived value.
    *Does the data change over time?*
If the value remains static and does not change (e.g., fixed config, constant text), it should not be state.
If it does change (e.g., user input, API response), it should be state.
    *Does the data need to persist after a re-render?*
If the value needs to persist across renders, it should be state.
    *Does the data need to persist after a re-render?*
If the value needs to persist across renders, it should be state.
If it's only used temporarily within a function or component lifecycle, use a variable instead.
    **Final Rule of Thumb**
If the answer to any of these three questions is YES, then it should probably be state!
    *Otherwise, consider props, derived values, or variables instead.*

5. How can you identify where state needs to live?
    *Identify Every Component That Needs the State*
Determine which components rely on the state to render or update.
If multiple components need access, the state should not be kept in only one of them.
    *Find the Closest Common Parent Component*
The state should live in the lowest common ancestor of all components that need it.
This allows state to be passed as props to child components.
    *Should State Be Lifted?*
If two sibling components need the same state, lift it up to their parent.
The parent can pass it down as props.
    *Can State Be Moved Closer to Where It’s Used?*
Avoid unnecessary lifting—if only one component needs state, keep it local.


### Higher Order Function
1. What is a “higher-order function”?
A higher-order function is a function that either:

- Takes another function as an argument, or
  Returns a function as its result
- This makes higher-order functions a powerful      tool for abstraction, reusability, and functional programming in JavaScript.

*Why Use Higher-Order Functions?*
✅ **Code Reusability** → Functions become more modular and reusable.
 ✅ **Abstraction** → Simplifies complex logic by breaking it into smaller parts.
 ✅ **Functional Programming** → Enables techniques `like map()`, `filter()`, `reduce()`.

2. Explore the greaterThan function as defined in the reading. In your own words, what is line 2 of this function doing?
The greaterThan function from the reading is likely structured like this:
function greaterThan(n) {
  return function (m) {
    `return m > n`;
  };
}

3. Explain how either map or reduce operates, with regards to higher-order functions.
    **How map() Operates as a Higher-Order Function**
The `map()` method is a higher-order function because it takes a function as an argument and applies it to each element in an array, returning a new array.
    **How map() Works**
Takes a *callback function as an argument*.
Iterates over each element in the array.
Applies the callback function to each element.
Returns a new array with the transformed values.
