# React + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react/README.md) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

# Filterable Product Table 🛍️🛒

## Where is State Used?

1️⃣ filterText (String)

- Stores the text entered in the search bar.
- Used to filter products based on their name.
- Updated using setFilterText whenever the user types in the search input.
  inStockOnly (Boolean)

2️⃣ Stores whether the "Only show products in stock" checkbox is checked.
Filters the product list based on stock availability.
Updated using setInStockOnly when the checkbox is clicked.

## How Props Are Used?

1. FilterableProductTable → SearchBar
   FilterableProductTable manages the state (filterText, inStockOnly).
   These state values are passed as props to SearchBar, so it can display the current values.

2. FilterableProductTable → ProductTable
   The products array (static data) is passed as a prop to ProductTable.
   The filterText and inStockOnly state values are also passed down.

3. ProductTable → ProductRow & ProductCategoryRow
   ProductTable iterates through products and passes individual data as props to:
   ProductRow (For each product)
   ProductCategoryRow (For category headers)
