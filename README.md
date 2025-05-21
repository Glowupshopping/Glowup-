<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>GlowUp - Online Skincare Shop</title>
  <style>
    /* Reset & base */
    * {
      box-sizing: border-box;
      margin: 0; padding: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    }
    body {
      background: #fff0f6;
      color: #333;
      line-height: 1.6;
      min-height: 100vh;
      display: flex;
      flex-direction: column;
    }
    a {
      text-decoration: none;
      color: inherit;
    }

    /* Header */
    header {
      background: #f8bbd0;
      padding: 20px 40px;
      display: flex;
      justify-content: space-between;
      align-items: center;
      box-shadow: 0 2px 8px rgba(0,0,0,0.1);
      position: sticky;
      top: 0;
      z-index: 100;
    }
    header h1 {
      font-size: 2rem;
      color: #880e4f;
    }
    nav a {
      margin-left: 25px;
      font-weight: 600;
      color: #880e4f;
      transition: color 0.3s;
    }
    nav a:hover {
      color: #ad1457;
    }
    .cart-btn {
      background: #ad1457;
      color: white;
      border: none;
      padding: 10px 18px;
      border-radius: 5px;
      cursor: pointer;
      font-weight: 700;
      transition: background 0.3s;
    }
    .cart-btn:hover {
      background: #880e4f;
    }

    /* Hero Section */
    .hero {
      background: linear-gradient(135deg, #fce4ec 0%, #f8bbd0 100%);
      text-align: center;
      padding: 100px 20px 80px;
      color: #880e4f;
    }
    .hero h2 {
      font-size: 3.5rem;
      margin-bottom: 20px;
      font-weight: 900;
    }
    .hero p {
      font-size: 1.25rem;
      margin-bottom: 30px;
      max-width: 600px;
      margin-left: auto;
      margin-right: auto;
      font-weight: 500;
    }
    .hero button {
      background: #ad1457;
      color: white;
      padding: 15px 40px;
      font-size: 1.2rem;
      border: none;
      border-radius: 30px;
      cursor: pointer;
      font-weight: 700;
      transition: background 0.3s;
    }
    .hero button:hover {
      background: #880e4f;
    }

    /* Products Section */
    .products {
      padding: 50px 40px;
      max-width: 1100px;
      margin: 0 auto;
      display: grid;
      grid-template-columns: repeat(auto-fit,minmax(280px,1fr));
      gap: 30px;
    }
    .product-card {
      background: white;
      border-radius: 10px;
      box-shadow: 0 6px 15px rgba(173, 20, 87, 0.2);
      padding: 20px;
      text-align: center;
      transition: transform 0.3s, box-shadow 0.3s;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
    }
    .product-card:hover {
      transform: translateY(-8px);
      box-shadow: 0 10px 25px rgba(173, 20, 87, 0.3);
    }
    .product-name {
      font-size: 1.5rem;
      font-weight: 700;
      color: #880e4f;
      margin-bottom: 10px;
    }
    .product-price {
      font-weight: 800;
      color: #ad1457;
      font-size: 1.3rem;
      margin-bottom: 15px;
    }
    .product-desc {
      flex-grow: 1;
      color: #555;
      margin-bottom: 20px;
    }
    .add-btn {
      background: #ad1457;
      color: white;
      border: none;
      padding: 12px 25px;
      font-weight: 700;
      font-size: 1rem;
      border-radius: 30px;
      cursor: pointer;
      transition: background 0.3s;
    }
    .add-btn:hover {
      background: #880e4f;
    }

    /* Footer */
    footer {
      background: #f8bbd0;
      color: #880e4f;
      text-align: center;
      padding: 20px 10px;
      font-weight: 600;
      margin-top: auto;
    }

    /* Responsive */
    @media (max-width: 480px) {
      .hero h2 {
        font-size: 2.5rem;
      }
      .hero p {
        font-size: 1rem;
      }
      header {
        flex-direction: column;
        align-items: flex-start;
      }
      nav {
        margin-top: 10px;
      }
      nav a {
        margin-left: 0;
        margin-right: 15px;
      }
    }
  </style>
</head>
<body>
  <header>
    <h1>GlowUp</h1>
    <nav>
      <a href="#products">Products</a>
      <a href="#contact">Contact</a>
      <button class="cart-btn">Cart</button>
    </nav>
  </header>

  <section class="hero">
    <h2>Your Glow Starts Here</h2>
    <p>Skincare made simple, effective, and radiant. Discover your perfect routine with GlowUp.</p>
    <button onclick="document.getElementById('products').scrollIntoView({behavior:'smooth'})">Shop Now</button>
  </section>

  <section id="products" class="products">
    <div class="product-card">
      <h3 class="product-name">Glow Serum</h3>
      <p class="product-price">$29.99</p>
      <p class="product-desc">Brightens and hydrates your skin for a radiant glow.</p>
      <button class="add-btn">Add to Cart</button>
    </div>
    <div class="product-card">
      <h3 class="product-name">Radiance Cream</h3>
      <p class="product-price">$39.99</p>
      <p class="product-desc">Moisturizes deeply, leaving your skin soft and luminous.</p>
      <button class="add-btn">Add to Cart</button>
    </div>
    <div class="product-card">
      <h3 class="product-name">Hydrating Cleanser</h3>
      <p class="product-price">$19.99</p>
      <p class="product-desc">Gentle cleanser that refreshes without drying your skin.</p>
      <button class="add-btn">Add to Cart</button>
    </div>
  </section>

  <footer id="contact">
    &copy; 2025 GlowUp Skincare. All rights reserved.
  </footer>

  <script>
    // Optional: simple cart button alert
    document.querySelectorAll('.add-btn').forEach(btn =>
      btn.addEventListener('click', () => alert('Added to cart!'))
    );
  </script>
</body>
</html># Glowup-
