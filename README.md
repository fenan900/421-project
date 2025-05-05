womens-fashion/
├── index.html
├── style.css
├── script.js
└── images/ (add your product images here)


index.html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Women's Fashion Store</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>

  <!-- Store Team Section -->
  <section id="store-team">
    <h2>Our Store Team</h2>
    <div class="team">
      <div class="manager"><h3>Fenan</h3><p>CEO</p></div>
      <div class="manager"><h3>Hana</h3><p>Products Manager</p></div>
      <div class="manager"><h3>Tasneem</h3><p>App & Website Manager</p></div>
      <div class="manager"><h3>Rima</h3><p>Shipping & Delivery</p></div>
    </div>
  </section>

  <!-- Home Page Section -->
  <section id="home-page">
    <h2>Women's Fashion Products</h2>

    <h3>Shoes and Heels</h3>
    <div class="products">
      <div class="product"><p>Red Heels - $50</p><button onclick="addToCart(50)">Add to Cart</button></div>
      <div class="product"><p>White Sneakers - $40</p><button onclick="addToCart(40)">Add to Cart</button></div>
    </div>

    <h3>Accessories and Jewelry</h3>
    <div class="products">
      <div class="product"><p>Gold Necklace - $70</p><button onclick="addToCart(70)">Add to Cart</button></div>
      <div class="product"><p>Bracelet Set - $30</p><button onclick="addToCart(30)">Add to Cart</button></div>
    </div>

    <h3>Outfits</h3>
    <div class="products">
      <div class="product"><p>Floral Dress - $60</p><button onclick="addToCart(60)">Add to Cart</button></div>
      <div class="product"><p>Denim Jacket - $80</p><button onclick="addToCart(80)">Add to Cart</button></div>
      <div class="product"><p>Cotton T-Shirt - $25</p><button onclick="addToCart(25)">Add to Cart</button></div>
      <div class="product"><p>Silk Skirt - $45</p><button onclick="addToCart(45)">Add to Cart</button></div>
    </div>
  </section>

  <!-- Cart and Payment Section -->
  <section id="cart-payment">
    <h2>Your Cart</h2>
    <p>Total: $<span id="total">0</span></p>

    <h3>Payment Method</h3>
    <select id="payment-method">
      <option value="online">Online Payment</option>
      <option value="cod">Cash on Delivery</option>
      <option value="tamara">Tamara</option>
    </select>

    <h3>Discount Code</h3>
    <input type="text" id="discount-code" placeholder="Enter code"/>
    <button onclick="applyDiscount()">Apply Discount</button>
  </section>

  <!-- Delivery & Shipping Section -->
  <section id="delivery-shipping">
    <h2>Delivery & Shipping</h2>
    <p>After successful payment, your order will be shipped within 3–5 business days.</p>
    <p>Track your order on the shipping dashboard for updates.</p>
  </section>

  <script src="script.js"></script>
</body>
</html>



style.css

/* General Styles */
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
  background-color: #fff9f9;
  color: #333;
}

h2 {
  background-color: #ffccd5;
  padding: 10px;
}

section {
  padding: 20px;
  border-bottom: 1px solid #ddd;
}

/* Store Team Section */
.team {
  display: flex;
  gap: 20px;
}

.manager {
  background-color: #ffeef1;
  padding: 10px;
  border-radius: 8px;
  flex: 1;
  text-align: center;
}

/* Product Listing */
.products {
  display: flex;
  flex-wrap: wrap;
  gap: 15px;
}

.product {
  background-color: #fef2f4;
  padding: 10px;
  border: 1px solid #ffc0cb;
  border-radius: 5px;
  width: 200px;
}

/* Cart and Payment */
#cart-payment input,
#cart-payment select {
  margin: 10px 0;
  padding: 5px;
  width: 200px;
}


script.js

// JavaScript functionality for cart total and discounts

let cartTotal = 0;

// Function to add a product price to the cart total
function addToCart(price) {
  cartTotal += price;
  document.getElementById("total").innerText = cartTotal.toFixed(2);
}

// Function to apply a discount if the correct code is entered
function applyDiscount() {
  const code = document.getElementById("discount-code").value;
  if (code === "FASHION10") {
    cartTotal *= 0.9; // Apply 10% discount
    alert("Discount applied!");
    document.getElementById("total").innerText = cartTotal.toFixed(2);
  } else {
    alert("Invalid discount code.");
  }
}

WOMEN'S FASHION STORE - FINAL WEB PROJECT

Submitted by:
Fenan - ID: XXXX (CEO)
Hana - ID: XXXX (Product Manager)
Tasneem - ID: XXXX (Website Manager)
Rima - ID: XXXX (Shipping & Delivery)

