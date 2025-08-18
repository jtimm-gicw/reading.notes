# 401-Read_26

## Questions

### React Quick Start

1. What are the building blocks of a React app?
# 🏠 React App Building Blocks (Cheat Sheet)

A React app is like a house, and the building blocks are the materials you use to construct it.

---

## 🧱 1. Components
- Core unit of a React app  
- Think Lego blocks → build small pieces and combine them into a whole app  
- Types:  
  - Functional components (modern, with hooks)  
  - Class components (older, less common)  

---

## 🧱 2. JSX
- Syntax extension: HTML-like code inside JavaScript  
- Makes UI code more readable  
- Lets you mix JavaScript and UI structure in one place  

---

## 🧱 3. Props
- Inputs to components (like function parameters)  
- Passed **from parent to child**  
- **Immutable** inside the child  
- Used for customizing and reusing components  

---

## 🧱 4. State
- Internal memory of a component  
- **Can change** (unlike props)  
- Updating state automatically re-renders UI  
- Used for things like form inputs, toggles, counters  

---

## 🧱 5. Events
- Handle **user interactions** (clicks, typing, form submissions)  
- React uses **camelCase event handlers** (`onClick`, `onChange`, etc.)  
- Allow apps to respond to user actions  

---

## 🧱 6. Hooks
- Special functions to use React features  
- Common ones:  
  - `useState` → manage state  
  - `useEffect` → handle side effects (fetching data, timers)  
  - `useContext` → share global state  
- Enable functional components to be powerful and stateful  

---

## 🧱 7. Virtual DOM
- React keeps a **virtual copy** of the DOM in memory  
- Compares new vs old virtual DOM (**diffing**)  
- Updates only what changed in the real DOM  
- Makes React **fast and efficient**  

---

## 🧱 8. React Router (navigation)
- Handles page navigation in **Single Page Apps (SPA)**  
- Lets you switch views without full page reloads  
- Keeps app feeling fast and seamless  

---

## 🧱 9. Data Fetching
- React doesn’t fetch data on its own  
- Use tools like `fetch`, Axios, or React Query  
- Often paired with `useEffect` to load data when a component mounts  

---

## 🧱 10. Context / State Management (advanced)
- Fixes **prop drilling** (passing props through many layers)  
- Solutions:  
  - **Context API** (built-in to React)  
  - External libraries: Redux, Zustand, Recoil, etc.  
- Useful for managing global state across the whole app  

---

# 🔑 Quick Summary
- **Components** → building blocks  
- **JSX** → describe UI  
- **Props** → input from outside  
- **State** → internal memory  
- **Events** → interactions  
- **Hooks** → tools for state/effects  
- **Virtual DOM** → efficiency engine  
- **Router** → navigation  
- **Data fetching** → connect to APIs  
- **Context/Redux** → global state  

2. What is the difference between an HTML element and a React component?
    1. *HTML Element*
     basic building block of a webpage.
     Comes from the HTML language itself.
    2. *React Component*
     A custom building block that you define in JavaScript/JSX.
     Can return one or more HTML elements (or other components).
     Always capitalized by convention.

➡️ Think of a React component as a prefab structure you design — like a custom “house block” built using bricks (HTML elements).

3. What is JSX and why do we use it?
# 🧩 JSX (JavaScript XML)

- A **syntax extension** for JavaScript  
- Lets you write **HTML-like code inside JavaScript**  
- React converts JSX into plain JavaScript under the hood  

---

## 🎯 Why We Use JSX

    1. **Cleaner + More Readable**  
   - Looks like HTML but is actually JavaScript  
   - Easier to read and write  

    2. **Mix Logic with Markup**  
   - Embed dynamic values inside `{ }`  

    3. **Consistency**  
   - No separate HTML and JS files  
   - UI + logic in one place → easier to debug and maintain  

    4. **Full JavaScript Power**  
   - Use conditionals, loops, and functions directly in JSX  


4. Describe the process of embedding JavaScript expressions in JSX.
    # 🔑 Embedding JavaScript in JSX

## 1. Use Curly Braces {}
- Anything inside `{ }` in JSX is treated as **JavaScript**, not plain text  

---

## 2. What Can You Put Inside {}
- Any **valid JavaScript expression** (like variables, function calls, math, ternaries)  
- Remember: **expressions work, statements don’t**  

---

## 3. What You Can’t Put Inside {}
- **Statements** like `if`, `for`, or `while` cannot go directly inside JSX  
- ❌ Wrong: `{ if (isLoggedIn) "Welcome" }`  
- ✅ Instead: use **ternary**, **logical AND**, or calculate values **before the JSX**  

5. Does React or JSX have any special features for iteration or conditional logic?
# 🔑 Embedding JavaScript in JSX

## 1. Use Curly Braces {}
- Anything inside `{ }` in JSX is treated as **JavaScript**, not plain text  

---

## 2. What Can You Put Inside {}
- Any **valid JavaScript expression** (like variables, function calls, math, ternaries)  
- Remember: **expressions work, statements don’t**  

---

## 3. What You Can’t Put Inside {}
- **Statements** like `if`, `for`, or `while` cannot go directly inside JSX  
- ❌ Wrong: `{ if (isLoggedIn) "Welcome" }`  
- ✅ Instead: use **ternary**, **logical AND**, or calculate values **before the JSX**  

*Iteration* → use `.map()` inside `{}` to render lists.


*Conditionals* → use ternary (? :), logical AND (&&), or pre-calc variables.

JSX doesn’t invent new syntax — it just lets you use JavaScript expressions directly inside markup.

- How does React know to respond to a user’s inputs?
- How does React know to respond to a user’s inputs?
- What word indicates that a React component manages data with a Hook?

6. How does React know to respond to a user’s inputs?
React knows to respond to a user’s inputs because of **event handlers** tied to its state system.

Here’s the flow in simple terms:

*Event Listener Added* – You attach an event (like `onClick`, `onChange`, `onSubmit`) to a JSX element.

<button onClick={handleClick}>Click Me</button>

*User Interaction Happens* – The user clicks, types, or interacts. React’s synthetic event system catches it.

*State Update* – The event handler usually calls a state updater (setState or useState).

function handleClick() {
  setCount(count + 1);  // triggers re-render
}

*Re-render + UI Update* – React re-renders the component with the new state, and the UI changes accordingly.

So: **User action → Event handler → State change → Re-render → Updated UI**.

7. What word indicates that a React component manages data with a Hook?
The key word is **use**.

In React, any function that starts with `use` (like `useState`, `useEffect`, `useContext`) is a *Hook*, which lets a component **manage data or lifecycle logic**.

So if you see a function name starting with `use`, that *indicates it’s a Hook being used to manage data or behavior*.

8. How can two react components share data?
Two React components can share data in these main ways:

*Parent → Child* (Props):
Pass data down from a parent to its child with props.

<Child name={userName} />

*Child → Parent* (Callback Functions):
Parent gives the child a function, child calls it to send data back up.

<Child onUpdate={setUserName} />


*Between Siblings* (Lift State Up):
Put the shared state in the closest common parent, and pass it to both children via props.

*Global Sharing* (Context or State Library):
**Use React Context, Redux, or another state manager for data many components need.**

👉 In simple terms: *pass with props, lift state up, or use context* for wider sharing.

### Render and Commit

1. What are the three steps of refreshing a React UI?
The three steps of refreshing a React UI are:
*State or Props Change* – Something in the component’s state or props updates.
*Re-render* – React re-executes the component to generate the updated JSX.
*DOM Update (Reconciliation)* – React compares the new JSX with the previous Virtual DOM and updates only the changed parts in the actual browser DOM.

**In short: Change → Re-render → Update DOM.**

2. How do you trigger updates to a component after the initial render?
You can trigger updates to a React component after the initial render in a few common ways:
    1. Updating State:
    Use useState (functional components) or this.setState (class components).

    2. Receiving New Props:
    If a parent passes new props to a child component, the child will re-render         automatically.

    3. Using Effects with Dependencies (useEffect):
    You can run code that updates state or triggers side effects after render.

So basically: **change state, receive new props, or run an effect that updates state will trigger a component update**.

3. Does React recreate DOM nodes on every rerender?
**No**, React does not recreate actual DOM nodes on every rerender.
Here’s what happens:
On a rerender, *React re-executes the component function (or render() in class components) to produce new JSX*.

React creates a Virtual DOM representation of the updated UI.

React diffs the new Virtual DOM against the previous one (reconciliation) to figure out what actually changed.

Only the changed parts of the real DOM are updated. Unchanged DOM nodes are reused, not recreated.

4. After React has updated the DOM, what still needs to happen before the user sees the change?
After React updates the DOM, the browser still needs to repaint/reflow the UI so the user actually sees the changes.
**Here’s the sequence in simple terms:**
- React updates the virtual DOM.
- React diffs the virtual DOM against the previous version to find changes.
- React updates the real DOM with only the necessary changes.
- Browser renders the changes – this is called reflow and repaint, where the layout and visuals are updated on the screen.

So, even after React does its work, the final step is the browser painting the updated UI, which is what the user actually sees.


