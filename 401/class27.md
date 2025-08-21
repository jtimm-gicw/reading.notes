# 401-Read_27

## Questions

### Thinking in React

1. Summarize the five steps of thinking in react.
    1. Break the UI into a component hierarchy
        - Look at the design and divide it into small, reusable pieces (components).
        - Each box or section of the UI is usually a separate component.
    2. Build a static version in React
        - First, make the app show data correctly with props.
        - No interactivity yet (no state changes, no user input handling).
        - Focus on getting the structure and components working.
    3. Find the minimal but complete representation of UI state
        - State is the changing data that React remembers.
        - *Rule of thumb*: Keep state minimal and avoid duplicates.
        - *Example*: In a shopping list app, store the array of items as state. If you  need the number of items, calculate items.length instead of storing a separate count.
    4. Identify where your state should live
        - State should be owned by the closest common parent of the components that use it.
        - Process:
            - Find all components that need the state.
            - Locate their nearest common parent.
            - Put the state there and pass it down via props.
    5. Add inverse data flow (make it interactive)
        - Data normally flows downward (parent → child) with props.
        - But when a child needs to update parent state (e.g., typing in a search box), the parent must pass a callback function (like setState) down.
        - This way, children can trigger state changes in parents.

### State: A Component’s Memory

1. What is one reason a local variable isn’t sufficient for managing a React component?
A *local variable isn’t enough* because it resets every render, while state (useState) remembers values across renders and updates the UI correctly.

2. What is the argument to the useState hook, and what are the two parts of its return array?
**Argument to useState**
    - The argument is the initial value you want your state to start with.


*Example:* `useState`(0) → the state starts at `0`.

    - You can use any type: number, string, boolean, array, object, etc.


**Two parts of the return array**
 `useState` returns *an array with two elements*:


*Current state value*  -->
The current value of the state variable.
*Setter function*  -->
A function to update the state. Calling this triggers a re-render.

**explanation:**
const [`count`, `setCount`] = `useState`(0);
0 → argument → initial value
count → current state value (*starts at 0*)
setCount → function to update count

3. How can Component A access state from Component B?
**Components cannot directly access each other’s state in React**.
To share state between Component A and Component B:
*Lift the state up*
    - Move the state to their closest common parent component.
    - The parent now “owns” the state.

*Pass state down via props*
    - The parent sends the state to both A and B through props.

*Update state via callbacks (if needed)*
    - If a child (like B) needs to change the state, the parent passes a setter function (setState) down as a prop.

**B calls this function** → **parent updates state** →   
**A and B re-render with the new state**.


