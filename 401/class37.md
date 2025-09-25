# 401-Read_37  

## Multiple Reducers — Quick Notes  

---

### ❓ Why create multiple reducers?  

- 🧩 **Keep things small & focused** — each reducer handles one slice of state (e.g., `auth`, `todos`, `ui`).  
- 🔍 **Separation of concerns** → easier to reason about and debug.  
- 📈 **Scalability** — add features without editing one giant reducer.  
- 🧪 **Easier to test** — unit-test small reducers instead of one huge one.  
- 👥 **Team-friendly** — different devs can own different reducers.  
- ⚡ **Performance** — smaller updates and less chance of unintended state changes.  

---

### ❓ How would you combine multiple reducers?  

- ✅ Use **`combineReducers` (Redux)** to build a root reducer.  
- 🧩 Each slice reducer manages its own part of state (e.g., `state.auth`, `state.todos`).  
- 🔄 Alternatively, write a manual root reducer if you need custom merge logic.  
- 🗂️ **Resulting app state shape** is tidy and predictable, e.g.:  
  ```js
  { auth: { … }, todos: [ … ] }

### ❓ How will you manage state as an immutable object? Why?

*Why immutable?*
🎯 Predictability → reducers return new state instead of mutating old state.
⚡ Fast change detection → shallow equality checks enable efficient re-renders.
⏳ Time-travel debugging → enables undo/redo and history tracking.
🛡️ Avoids bugs → prevents accidental shared references.

*How to keep state immutable:*
✨ Use object & array spread for shallow updates.
🛠️ For deeper updates, use helpers or Immer to simplify immutable logic.
🚫 Never mutate state directly (push, splice, direct assignment).
✅ Always return either the original state (if unchanged) or a new copy (if changed).

📚 **Redux Docs — Using Combined Reducers**
1️⃣ What does combineReducers simplify?
    ✅ It simplifies writing reducer functions.
    💡 Breaks state into smaller “slices” and stitches them together into a root reducer.

2️⃣ How does combineReducers assemble the state tree?
    🧩 Each key in the state tree corresponds to a slice reducer.
    🛠️ combineReducers calls each reducer with its slice of state + the action.
    📦 Results are combined into a new state object.
    🎯 Each reducer only manages its own slice, but the full tree is assembled cleanly.

3️⃣ How is initial state defined with combineReducers?
    🏗️ Each reducer defines its own initial state internally.
    🧩 Redux uses each reducer’s initial state to build the overall root state.
    🔍 The root state = combination of all slice initial states.
    🌟 You can preload custom state when creating the store.

📚 **Redux Docs — Combined Reducer Syntax**
1️⃣ Why split reducers as apps grow?
    🧩 Separation of concerns — one slice per reducer.
    🔍 Easier to debug — smaller reducers are clearer.
    🧪 Easier to test — isolate logic in small functions.
    📈 Scalability — add new reducers instead of bloating one.
    👥 Team-friendly — devs can work independently.

2️⃣ Which helper function combines slice reducers?
    ✅ combineReducers → turns an object of slice reducers into one big reducer.
    ✅ That root reducer is passed to createStore.

3️⃣ What’s a common naming convention for reducers?
    📝 Name reducers after the slice they manage:
        authReducer → manages state.auth
        todosReducer → manages state.todos
        settingsReducer → manages state.settings

    🔑 Convention makes state easy to read and maintain.
✅ **Quick Recap**
    🧩 Split reducers → clean, testable, scalable logic.
    🔗 Use combineReducers → pass to createStore.
    📝 Follow convention → reducer name = state slice.