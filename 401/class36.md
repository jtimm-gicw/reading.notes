# 📌 Phase 1 Overview

Phase 1 is all about **scaffolding and foundation**.
That means:

* Setting up the file structure
* Adding initial styling (Material UI + SCSS if desired)
* Creating the basic components (`Header`, `Footer`, `Categories`, `Products`)
* Hooking up **Redux state management** for categories and products
* Making sure clicking a category updates the active category and shows the right products

---

# 🏗️ What You’ll Build in Phase 1

### Components

* **`App.jsx`** → The main container (wraps everything).
* **`Header`** → Displays the store name (like a navbar).
* **`Footer`** → Copyright/contact info.
* **`Categories`** → Shows a list of categories. When clicked, dispatches an action to set the active category.
* **`Products`** → Displays products filtered by the active category.

### Redux Store

* **Categories Slice (`store/categories/index.js`)**

  * Holds list of categories
  * Keeps track of the **active category**
  * Provides an action to set active category
* **Products Slice (`store/products.js`)**

  * Holds list of all products
  * Filters products based on the active category
* **Store Index (`store/index.js`)**

  * Combines reducers
  * Exports the store to be used in `<Provider>`

---

# 🧑‍💻 Step-by-Step (Phase 1)

### 1. Setup Project

* Run `npx create-react-app storefront`
* Install **Material UI**:

  ```bash
  npm install @mui/material @emotion/react @emotion/styled
  ```
* Install **Redux Toolkit + React Redux**:

  ```bash
  npm install @reduxjs/toolkit react-redux
  ```

---

### 2. App Container

```jsx
import Header from './Components/Header';
import Footer from './Components/Footer';
import Categories from './Components/Categories';
import Products from './Components/Products';

function App() {
  return (
    <>
      <Header />
      <Categories />
      <Products />
      <Footer />
    </>
  );
}

export default App;
```

---

### 3. Header & Footer

**Header**

```jsx
import { AppBar, Toolbar, Typography } from '@mui/material';

export default function Header() {
  return (
    <AppBar position="static">
      <Toolbar>
        <Typography variant="h5">My Virtual Store</Typography>
      </Toolbar>
    </AppBar>
  );
}
```

**Footer**

```jsx
import { Typography } from '@mui/material';

export default function Footer() {
  return (
    <footer style={{ textAlign: 'center', marginTop: '2rem' }}>
      <Typography variant="body2">© 2025 My Virtual Store | Contact: info@store.com</Typography>
    </footer>
  );
}
```

---

### 4. Categories (with Redux)

**Slice:** `store/categories/index.js`

```js
import { createSlice } from '@reduxjs/toolkit';

const initialState = {
  categories: [
    { name: 'electronics', displayName: 'Electronics', description: 'Gadgets and devices' },
    { name: 'clothing', displayName: 'Clothing', description: 'Apparel and accessories' },
    { name: 'food', displayName: 'Food', description: 'Groceries and snacks' },
  ],
  activeCategory: '',
};

const categoriesSlice = createSlice({
  name: 'categories',
  initialState,
  reducers: {
    setActiveCategory: (state, action) => {
      state.activeCategory = action.payload;
    }
  }
});

export const { setActiveCategory } = categoriesSlice.actions;
export default categoriesSlice.reducer;
```

**Component:** `Components/Categories/index.jsx`

```jsx
import { useSelector, useDispatch } from 'react-redux';
import { Button } from '@mui/material';
import { setActiveCategory } from '../../store/categories';

export default function Categories() {
  const categories = useSelector(state => state.categories.categories);
  const dispatch = useDispatch();

  return (
    <div style={{ margin: '1rem' }}>
      <h2>Browse Categories</h2>
      {categories.map(cat => (
        <Button
          key={cat.name}
          variant="outlined"
          onClick={() => dispatch(setActiveCategory(cat.name))}
          style={{ margin: '0.5rem' }}
        >
          {cat.displayName}
        </Button>
      ))}
    </div>
  );
}
```

---

### 5. Products (with Redux)

**Slice:** `store/products.js`

```js
import { createSlice } from '@reduxjs/toolkit';

const initialState = {
  products: [
    { name: 'Laptop', category: 'electronics', description: 'Portable computer', price: 999, inventory: 5 },
    { name: 'T-Shirt', category: 'clothing', description: '100% cotton', price: 20, inventory: 30 },
    { name: 'Chips', category: 'food', description: 'Crunchy snack', price: 3, inventory: 100 },
  ]
};

const productsSlice = createSlice({
  name: 'products',
  initialState,
  reducers: {},
});

export default productsSlice.reducer;
```

**Component:** `Components/Products/index.jsx`

```jsx
import { useSelector } from 'react-redux';
import { Card, CardContent, Typography } from '@mui/material';

export default function Products() {
  const products = useSelector(state => state.products.products);
  const activeCategory = useSelector(state => state.categories.activeCategory);

  const filtered = activeCategory
    ? products.filter(p => p.category === activeCategory)
    : [];

  return (
    <div style={{ margin: '1rem' }}>
      <h2>Products</h2>
      {filtered.map(product => (
        <Card key={product.name} style={{ margin: '0.5rem', width: '200px', display: 'inline-block' }}>
          <CardContent>
            <Typography variant="h6">{product.name}</Typography>
            <Typography>{product.description}</Typography>
            <Typography>${product.price}</Typography>
          </CardContent>
        </Card>
      ))}
    </div>
  );
}
```

---

### 6. Store Setup

**`store/index.js`**

```js
import { configureStore } from '@reduxjs/toolkit';
import categoriesReducer from './categories';
import productsReducer from './products';

const store = configureStore({
  reducer: {
    categories: categoriesReducer,
    products: productsReducer,
  },
});

export default store;
```

**`main.jsx`**

```jsx
import React from 'react';
import ReactDOM from 'react-dom/client';
import { Provider } from 'react-redux';
import store from './store';
import App from './App';

ReactDOM.createRoot(document.getElementById('root')).render(
  <Provider store={store}>
    <App />
  </Provider>
);
```

---

# ✅ What Phase 1 Accomplishes

* Categories list is shown
* Clicking a category updates active state
* Products filtered by category display correctly
* UI uses **Material UI** for styling
* State is managed centrally with **Redux**
* Base project structure is in place for scaling
