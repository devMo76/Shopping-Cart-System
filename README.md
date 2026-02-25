# Shopping Cart

A React shopping cart application that uses the **useReducer** hook to manage complex cart state.

## useReducer Implementation

The cart state management lives in `src/store/shopping-cart-context.jsx`. Instead of using multiple `useState` calls to handle cart operations, the app centralizes state updates through `useReducer` with a `shoppinCartReducer` function that handles two action types:

- **ADD_ITEM** — Adds a new product to the cart or increments the quantity if it already exists.
- **UPDATE_ITEM** — Adjusts the quantity of an existing cart item and removes it if the quantity drops to zero.

The reducer is paired with React Context (`CartContext`) so that any component in the tree can dispatch cart actions without prop drilling.

## Project Structure

```
src/
├── store/
│   └── shopping-cart-context.jsx   # useReducer + Context provider
├── components/
│   ├── Header.jsx                  # Navigation with cart button
│   ├── Cart.jsx                    # Cart items list
│   ├── CartModal.jsx               # Modal wrapper for the cart
│   ├── Product.jsx                 # Product card with "Add to Cart"
│   └── Shop.jsx                    # Product grid layout
├── dummy-products.js               # Static product data
└── App.jsx                         # Root component
```

## Getting Started

```bash
npm install
npm run dev
```
