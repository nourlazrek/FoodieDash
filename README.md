# 🍴 FoodieDash  

![GitHub last commit](https://img.shields.io/github/last-commit/YOUR-USERNAME/foodiedash?color=orange)  
![GitHub repo size](https://img.shields.io/github/repo-size/YOUR-USERNAME/foodiedash?color=brightgreen)  
![GitHub Pages](https://img.shields.io/badge/deployed-GitHub%20Pages-orange)  

FoodieDash is a **demo food delivery website** built with **HTML, CSS, and JavaScript**.  
It simulates a modern multi-page flow for food ordering:  

➡️ **Home → Restaurant Menu → Cart → Checkout**  

Perfect for learning how to structure a simple multi-page website, use localStorage for cart data, and deploy with GitHub Pages.  

---

## ✨ Features
- 🎨 **Professional UI** with an orange-themed modern design.  
- 🏠 Homepage with categories, featured restaurants, and sample dishes.  
- 🍕 Restaurant page with dish listings and **Add to Cart** buttons.  
- 🛒 Shopping cart with **remove item + total price calculation**.  
- 💳 Checkout page with a **form + order confirmation message**.  
- 💾 Persistent cart data using **localStorage** (works across all pages).  
- 🌐 Deployable instantly via GitHub Pages.
- <!-- =========================
   index.html (Homepage)
========================= -->
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>FoodieDash - Home</title>
  <link rel="stylesheet" href="style.css"/>
</head>
<body>
  <header>
    <h1>🍴 FoodieDash</h1>
    <nav>
      <a href="index.html">Home</a>
      <a href="cart.html">Cart 🛒</a>
    </nav>
  </header>

  <section class="hero">
    <h2>Delicious food, delivered fast.</h2>
    <p>Explore top restaurants and your favorite dishes.</p>
  </section>

  <section class="categories">
    <h3>Categories</h3>
    <div class="grid">
      <div class="card">🍕 Pizza</div>
      <div class="card">🍔 Burgers</div>
      <div class="card">🥗 Salads</div>
      <div class="card">🍣 Sushi</div>
    </div>
  </section>

  <section class="restaurants">
    <h3>Popular Restaurants</h3>
    <div class="grid">
      <a href="restaurant.html" class="card">
        <img src="https://source.unsplash.com/300x200/?pizza" alt="Pizza Palace"/>
        <h4>Pizza Palace</h4>
      </a>
      <a href="restaurant.html" class="card">
        <img src="https://source.unsplash.com/300x200/?burger" alt="Burger Haven"/>
        <h4>Burger Haven</h4>
      </a>
      <a href="restaurant.html" class="card">
        <img src="https://source.unsplash.com/300x200/?sushi" alt="Sushi World"/>
        <h4>Sushi World</h4>
      </a>
    </div>
  </section>

  <footer>
    <p>© 2025 FoodieDash</p>
  </footer>
</body>
</html>


<!-- =========================
   restaurant.html (Menu Page)
========================= -->
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>FoodieDash - Restaurant</title>
  <link rel="stylesheet" href="style.css"/>
  <script src="script.js" defer></script>
</head>
<body>
  <header>
    <h1>🍴 FoodieDash</h1>
    <nav>
      <a href="index.html">Home</a>
      <a href="cart.html">Cart 🛒</a>
    </nav>
  </header>

  <section class="menu">
    <h2>Pizza Palace Menu</h2>
    <div class="grid">
      <div class="card">
        <img src="https://source.unsplash.com/300x200/?pepperoni-pizza" alt="Pepperoni Pizza"/>
        <h4>Pepperoni Pizza</h4>
        <p>$12</p>
        <button onclick="addToCart('Pepperoni Pizza', 12)">Add to Cart</button>
      </div>
      <div class="card">
        <img src="https://source.unsplash.com/300x200/?veggie-pizza" alt="Veggie Pizza"/>
        <h4>Veggie Pizza</h4>
        <p>$10</p>
        <button onclick="addToCart('Veggie Pizza', 10)">Add to Cart</button>
      </div>
      <div class="card">
        <img src="https://source.unsplash.com/300x200/?margherita" alt="Margherita"/>
        <h4>Margherita</h4>
        <p>$9</p>
        <button onclick="addToCart('Margherita', 9)">Add to Cart</button>
      </div>
    </div>
  </section>

  <footer>
    <p>© 2025 FoodieDash</p>
  </footer>
</body>
</html>


<!-- =========================
   cart.html (Cart Page)
========================= -->
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>FoodieDash - Cart</title>
  <link rel="stylesheet" href="style.css"/>
  <script src="script.js" defer></script>
</head>
<body>
  <header>
    <h1>🍴 FoodieDash</h1>
    <nav>
      <a href="index.html">Home</a>
      <a href="cart.html">Cart 🛒</a>
    </nav>
  </header>

  <section class="cart">
    <h2>Your Cart</h2>
    <div id="cart-items"></div>
    <div class="cart-summary">
      <p id="cart-total">Total: $0</p>
      <a href="checkout.html" class="btn">Proceed to Checkout</a>
    </div>
  </section>

  <footer>
    <p>© 2025 FoodieDash</p>
  </footer>
</body>
</html>


<!-- =========================
   checkout.html (Checkout Page)
========================= -->
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>FoodieDash - Checkout</title>
  <link rel="stylesheet" href="style.css"/>
  <script src="script.js" defer></script>
</head>
<body>
  <header>
    <h1>🍴 FoodieDash</h1>
    <nav>
      <a href="index.html">Home</a>
      <a href="cart.html">Cart 🛒</a>
    </nav>
  </header>

  <section class="checkout">
    <h2>Checkout</h2>
    <form id="checkout-form">
      <label>Name:<br><input type="text" required></label><br>
      <label>Address:<br><input type="text" required></label><br>
      <label>Payment Method:<br>
        <select required>
          <option>Credit Card</option>
          <option>PayPal</option>
          <option>Cash on Delivery</option>
        </select>
      </label><br>
      <button type="submit">Place Order</button>
    </form>
    <p id="confirmation" style="display:none;">✅ Thank you! Your order has been placed.</p>
  </section>

  <footer>
    <p>© 2025 FoodieDash</p>
  </footer>
</body>
</html>


<!-- =========================
   style.css (Shared Styles)
========================= -->
body {
  margin: 0;
  font-family: Arial, sans-serif;
  background: #fffaf5;
  color: #333;
}
header {
  background: linear-gradient(90deg, #ff7a18, #ffb347);
  color: white;
  padding: 1rem 2rem;
  display: flex;
  justify-content: space-between;
  align-items: center;
}
header h1 { margin: 0; }
header nav a {
  margin-left: 1rem;
  color: white;
  text-decoration: none;
  font-weight: bold;
}
.hero {
  text-align: center;
  padding: 2rem;
  background: #ffe5d0;
}
.grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 1rem;
  padding: 1rem;
}
.card {
  background: white;
  border-radius: 12px;
  overflow: hidden;
  box-shadow: 0 4px 6px rgba(0,0,0,0.1);
  padding: 1rem;
  text-align: center;
}
.card img { width: 100%; border-radius: 8px; }
.card button {
  background: #ff7a18;
  color: white;
  border: none;
  padding: 0.5rem 1rem;
  margin-top: 0.5rem;
  border-radius: 6px;
  cursor: pointer;
}
.card button:hover { background: #e66900; }
footer {
  background: #ff7a18;
  color: white;
  text-align: center;
  padding: 1rem;
  margin-top: 2rem;
}
.btn {
  display: inline-block;
  background: #ff7a18;
  color: white;
  padding: 0.7rem 1.2rem;
  text-decoration: none;
  border-radius: 6px;
}
.btn:hover { background: #e66900; }


<!-- =========================
   script.js (Cart Logic)
========================= -->
function getCart() {
  return JSON.parse(localStorage.getItem("cart") || "[]");
}

function saveCart(cart) {
  localStorage.setItem("cart", JSON.stringify(cart));
}

function addToCart(name, price) {
  const cart = getCart();
  cart.push({ name, price });
  saveCart(cart);
  alert(`${name} added to cart!`);
}

function displayCart() {
  const cart = getCart();
  const cartItemsDiv = document.getElementById("cart-items");
  const cartTotal = document.getElementById("cart-total");
  if (!cartItemsDiv) return;

  cartItemsDiv.innerHTML = "";
  let total = 0;
  cart.forEach((item, index) => {
    total += item.price;
    const div = document.createElement("div");
    div.className = "cart-item";
    div.innerHTML = `
      ${item.name} - $${item.price}
      <button onclick="removeFromCart(${index})">Remove</button>
    `;
    cartItemsDiv.appendChild(div);
  });
  cartTotal.textContent = `Total: $${total}`;
}

function removeFromCart(index) {
  const cart = getCart();
  cart.splice(index, 1);
  saveCart(cart);
  displayCart();
}

document.addEventListener("DOMContentLoaded", () => {
  if (document.getElementById("cart-items")) displayCart();

  const form = document.getElementById("checkout-form");
  if (form) {
    form.addEventListener("submit", (e) => {
      e.preventDefault();
      localStorage.removeItem("cart");
      document.getElementById("confirmation").style.display = "block";
      form.style.display = "none";
    });
  }
});

