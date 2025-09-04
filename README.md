# 🍴 FoodieDash

![Last Commit](https://img.shields.io/github/last-commit/nourlazrek/FoodieDash?color=orange)
![Repo Size](https://img.shields.io/github/repo-size/nourlazrek/FoodieDash?color=brightgreen)
![Deployed](https://img.shields.io/badge/deployed-GitHub%20Pages-orange)

**FoodieDash** is a demo food delivery website built with **HTML, CSS, and JavaScript**.  
It simulates a modern multi-page flow for food ordering:

➡️ **Home → Restaurant Menu → Cart → Checkout**

Perfect for learning how to structure a simple multi-page website, use localStorage for cart data, and deploy with GitHub Pages.

---

## ✨ Features

- 🎨 **Modern orange-themed UI**
- 🏠 Homepage with categories, featured restaurants, and sample dishes
- 🍕 Restaurant menu page with dish listings and **Add to Cart** buttons
- 🛒 Shopping cart with **remove item** and **total price calculation**
- 💳 Checkout page with a form and order confirmation
- 💾 Persistent cart data using **localStorage** (works across all pages)
- 🌐 Instant deployment via GitHub Pages

---

## 📁 Project Structure

```
FoodieDash/
│
├── index.html          # Homepage
├── restaurant.html     # Restaurant menu
├── cart.html           # Shopping cart
├── checkout.html       # Checkout
├── style.css           # Shared styles
└── script.js           # Cart logic
```

---

## 🚀 Quick Start

1. **Clone the repo:**
   ```bash
   git clone https://github.com/nourlazrek/FoodieDash.git
   cd FoodieDash
   ```
2. **Open `index.html` in your browser.**
3. **Deploy to GitHub Pages:**  
   Go to your repository settings → Pages → select the root folder.

---

## 🖥️ Demo Pages Overview

### **Homepage (`index.html`)**

- Categories (Pizza, Burgers, Salads, Sushi)
- Popular restaurants with images
- Navigation bar and hero section

### **Restaurant Menu (`restaurant.html`)**

- Dish cards with images, names, prices
- **Add to Cart** button for each dish

### **Cart (`cart.html`)**

- Lists items in the cart
- Remove items from cart
- Shows total price
- Proceed to checkout button

### **Checkout (`checkout.html`)**

- Simple checkout form (Name, Address, Payment)
- Order confirmation message on submit

---

## 🛠️ Core Logic (script.js)

- **Cart Storage:** Uses `localStorage` for cart persistence
- **Add/Remove Cart Items:** Handles adding and removing items
- **Cart Rendering:** Dynamically updates cart display and total
- **Checkout:** Handles order submission and confirmation

---

## 🎨 Style Highlights (style.css)

- Responsive grid layouts
- Orange gradient header/footer
- Card UI for restaurants, dishes, cart items
- Clean, mobile-friendly design

---

## 🤝 Contributing

Pull requests and suggestions welcome!  
Open an [issue](https://github.com/nourlazrek/FoodieDash/issues) or fork the repo to get started.

---

## 📄 Sample Code Snippets

<details>
  <summary><strong>Cart Logic (script.js)</strong></summary>

  ```js
  function getCart() {
    return JSON.parse(localStorage.getItem("cart") || "[]");
  }

  function addToCart(name, price) {
    const cart = getCart();
    cart.push({ name, price });
    localStorage.setItem("cart", JSON.stringify(cart));
    alert(`${name} added to cart!`);
  }

  function displayCart() {
    const cart = getCart();
    // ...renders cart items and total price
  }
  ```
</details>

<details>
  <summary><strong>Menu Card Example (restaurant.html)</strong></summary>

  ```html
  <div class="card">
    <img src="https://source.unsplash.com/300x200/?pepperoni-pizza" alt="Pepperoni Pizza"/>
    <h4>Pepperoni Pizza</h4>
    <p>$12</p>
    <button onclick="addToCart('Pepperoni Pizza', 12)">Add to Cart</button>
  </div>
  ```
</details>

---

## 📬 License

MIT

---

© 2025 FoodieDash by [nourlazrek](https://github.com/nourlazrek)
