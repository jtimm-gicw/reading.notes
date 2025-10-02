# 📘 State Management Overview: Redux Toolkit (RTK), Redux Fundamentals & MobX

---

## 🔍 Redux Fundamentals: Key Takeaways
[Redux Toolkit - Fundamentals: Redux from the Ground Up](https://redux-toolkit.js.org/tutorials/overview#redux-fundamentals-redux-from-the-ground-up)

1. **🏗 Manual Redux Setup**  
   - Demonstrates Redux **without abstractions**.  
   - Shows raw building blocks before Toolkit.

2. **📦 Core Redux Concepts**  
   - **Actions** → Plain objects describing state changes.  
   - **Reducers** → Pure functions that update state based on actions.  
   - **Store** → Holds state, provides `getState()`, and allows dispatch.

3. **🔄 State Flow**  
   - Action is **dispatched** → Reducer processes it → Store updates → UI re-renders.

4. **⚙️ Manual Store Configuration**  
   - Uses `createStore()` and manually applies middleware.  
   - Demonstrates underlying Redux mechanics.

5. **🚀 Why Redux Toolkit (RTK) is Recommended**  
   - Manual setup = **boilerplate + complexity**.  
   - RTK simplifies with `configureStore`, `createSlice`, Immer immutability, DevTools, and async helpers.

---

## 🛠 Redux Toolkit (RTK)

1. **✨ What concerns are addressed by Redux Toolkit?**  
   - 📝 Reduces boilerplate (actions, reducers, types auto-generated).  
   - 🔒 Safer immutable updates (via Immer).  
   - ⚙️ Simplifies store setup (`configureStore`).  
   - ⏳ Async helpers with `createAsyncThunk`.  
   - 📏 Encourages slice-based structure.  
   - 🐞 DevTools integration + easier testing.

2. **🛠 What does `configureStore()` do?**  
   - 🏗 Creates the Redux store with sensible defaults.  
   - ✅ Auto: combines reducers, applies `redux-thunk`, enables DevTools, sets middleware.  
   - 📦 Accepts options: `reducer`, `middleware`, `preloadedState`, `enhancers`.

   ```js
   import { configureStore } from '@reduxjs/toolkit';
   import todosReducer from './todosSlice';

   const store = configureStore({
     reducer: { todos: todosReducer },
   });

1. 📝 How would I use createSlice()?

- 🎯 Defines state + reducers + action creators in one place.
- 💡 Reducers can "mutate" state safely (Immer handles immutability).
- ⚡ Returns { actions, reducer }.
- 🌳 MobX

2. ❓ What is MobX?

- ⚡ Reactive state management library.
- 🔍 Core idea: observables (state) + computed (derived values) + observers (UI).
- ✍️ Minimal boilerplate: mutate state directly, MobX tracks automatically.
- 🚀 Very fast, fine-grained reactivity.

3. 🔒 How does MobX avoid inconsistent state?

- 🧩 Automatic dependency tracking ensures updates in the right order.
- 🏗 Actions batch updates → observers only see final result.
- ⏱ Derived values update before UI renders → no half-applied states.

4. 💻 How to build a reactive UI with MobX?

✅ **Steps:**
    - Make state observable (makeAutoObservable).
    - Define computed values (get or computed).
    - Wrap React components with observer.
    - Update state via actions (class methods).
    -Use reaction / autorun for side effects if needed.

✅ **Bottom Line**
- **Redux Fundamentals:** Understand the core (actions, reducers, store, manual setup).
- **Redux Toolkit (RTK):** Modern, simplified, opinionated — recommended for real apps.
- **MobX:** Reactive, minimal boilerplate, great for fine-grained state tracking.