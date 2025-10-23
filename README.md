## Paradise Nursery — E-Plant Shopping Web App

**Paradise Nursery** is a simple React-based e-commerce web application where users can browse, select, and manage plant purchases. The app demonstrates React component composition, Redux state management, and responsive UI design for a clean shopping experience.

---

#### Features

#### Product Listing
- Displays multiple plant categories, each with its own selection of plants.
- Each plant card shows an image, name, description, and price.
- “Add to Cart” button changes to “Added to Cart” once an item is in the cart.

#### Shopping Cart
- Fully functional cart page that displays all selected plants.
- Supports incrementing and decrementing quantities.
- Shows live total per item and total cart value.
- Items merge by **name** (same plant increases quantity).
- Includes **“Continue Shopping”** and **“Checkout”** actions.

#### Cart Counter Badge
- A live **cart item count** is displayed as a badge on the cart icon in the navbar.
- The badge updates instantly as products are added or removed.

---

#### Tech Stack

| Layer | Technology |
|-------|-------------|
| **Frontend** | React (Functional Components, Hooks) |
| **State Management** | Redux Toolkit |
| **Styling** | CSS + inline styles |
| **Bundler** |  Vite-compatible setup |
| **Language** | JavaScript (ES6+) |

---

#### Functional Flow

1. Adding to Cart  
Clicking the “Add to Cart” button dispatches `addItem(product)`.
If the item already exists, its quantity is incremented; otherwise, it is added as a new entry.

2. Cart Display    
Items in the Redux store are displayed inside CartItem.jsx.
The user can increase or decrease quantity, or remove an item entirely.

3. Cart Counter     
The total number of cart items is displayed in the navbar as a live counter using
`cart.items.reduce((sum, item) => sum + item.quantity, 0)`.

4. Total Calculation     
Product prices are stored as strings (e.g. "$15") and converted safely into numbers for arithmetic operations.


#### Future Enhancements

• Add a checkout process including payment and order confirmation.     
• Persist cart items using localStorage or a backend API.     
• Add search, sorting, and filtering for products.     
