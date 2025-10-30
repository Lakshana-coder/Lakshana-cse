<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>PawParadise — Your Ultimate Destination for Happy Pets</title>
  <style>
    /* Basic reset */
    * { box-sizing: border-box; margin: 0; padding: 0; font-family: Inter, system-ui, Arial, sans-serif; }
    body { line-height: 1.4; color: #222; background: #f7f7fb; padding: 24px; }

    /* Header / Nav */
    .site-header { display:flex; align-items:center; justify-content:space-between; gap:16px; margin-bottom: 20px; }
    .brand { font-weight:700; font-size:20px; color:#0b5; }
    nav { display:flex; gap:10px; align-items:center; }
    nav a { text-decoration:none; color:#444; padding:8px 10px; border-radius:8px; }
    nav a:hover { background:#fff; box-shadow:0 1px 6px rgba(0,0,0,0.06); }

    /* Hero */
    .hero { background: linear-gradient(180deg, #fff 0%, #fcfcff 100%); padding:28px; border-radius:12px; box-shadow:0 6px 20px rgba(12,20,40,0.04); display:flex; flex-wrap:wrap; gap:20px; align-items:center; margin-bottom:20px; }
    .hero-left { flex:1 1 320px; }
    .hero h1 { font-size:28px; margin-bottom:8px; color:#0a2b1a; }
    .hero p { margin-bottom:14px; color:#444; }
    .cta { display:inline-block; padding:10px 14px; background:#0a8f5f; color:#fff; border-radius:10px; text-decoration:none; }

    /* Search + categories */
    .search-row { display:flex; gap:12px; margin-top:12px; }
    .search-row input { padding:10px; border-radius:8px; border:1px solid #e4e7ef; flex:1; }
    .categories { display:flex; gap:10px; margin-top:12px; flex-wrap:wrap; }

    /* Offers */
    .offers { display:flex; gap:12px; flex-wrap:wrap; margin-bottom:18px; }
    .offer { background:#fff; padding:12px; border-radius:10px; box-shadow:0 3px 12px rgba(8,16,30,0.04); min-width:180px; }

    /* Products grid */
    .grid { display:grid; grid-template-columns:repeat(auto-fit,minmax(220px,1fr)); gap:16px; }
    .card { background:#fff; padding:12px; border-radius:12px; box-shadow:0 6px 18px rgba(12,20,40,0.04); display:flex; flex-direction:column; gap:10px; }
    .card img { width:100%; height:150px; object-fit:cover; border-radius:8px; }
    .price { font-weight:700; color:#0a6f45; }
    .card .actions { display:flex; gap:8px; margin-top:auto; }
    .btn { padding:8px 10px; border-radius:8px; border:none; cursor:pointer; }
    .btn.primary { background:#0a8f5f; color:white; }
    .btn.ghost { background:transparent; border:1px solid #e6e9ef; color:#333; }

    /* Footer */
    footer { margin-top:26px; color:#666; font-size:14px; text-align:center; }

    /* Cart badge */
    .cart { position:relative; }
    .badge { position:absolute; top:-8px; right:-8px; background:#ff4d4f; color:white; width:20px; height:20px; border-radius:50%; display:flex; align-items:center; justify-content:center; font-size:12px; }

    @media (max-width:600px) {
      .hero { flex-direction:column; }
      .hero h1 { font-size:22px; }
    }
  </style>
</head>
<body>

  <header class="site-header">
    <div style="display:flex;align-items:center;gap:12px;">
      <div class="brand">lakshana | 2nd year cse</div>
      <div style="font-weight:700">PawParadise</div>
    </div>

    <nav>
      <a href="#">Home</a>
      <a href="#">Products</a>
      <a href="#">Deals</a>
      <a href="#">About</a>
      <a href="#">Contact</a>
      <div class="cart" style="margin-left:8px;">
        <button class="btn ghost" id="cartBtn">Cart (<span id="cartCount">0</span>)</button>
      </div>
    </nav>
  </header>

  <main>
    <section class="hero">
      <div class="hero-left">
        <h1>Welcome to PawParadise</h1>
        <p>Your Ultimate Destination for Happy Pets in India — Adopt Loving Pets | Premium Supplies | Free Shipping Across India</p>
        <div style="display:flex;gap:10px;align-items:center;">
          <a class="cta" href="#products">Shop Now</a>
          <div style="margin-left:10px;color:#666;">Free Delivery on Orders Above ₹999</div>
        </div>

        <div class="search-row">
          <input id="search" placeholder="Search pets, supplies..." />
          <button class="btn primary" onclick="doSearch()">Search</button>
        </div>

        <div class="categories" aria-label="categories">
          <span class="offer">All</span>
          <span class="offer">Dogs</span>
          <span class="offer">Cats</span>
          <span class="offer">Birds</span>
          <span class="offer">Fish</span>
          <span class="offer">Accessories</span>
        </div>
      </div>

      <div style="width:320px;">
        <img src="https://images.unsplash.com/photo-1517423440428-a5a00ad493e8?w=900&q=60&auto=format&fit=crop" alt="cute dog" style="width:100%; border-radius:12px; box-shadow:0 10px 30px rgba(8,12,30,0.06)">
      </div>
    </section>

    <section style="margin-top:14px;">
      <h2 style="margin-bottom:8px;">Special Offers</h2>
      <div class="offers">
        <div class="offer">Free Delivery on Orders Above ₹999 (Pan India)</div>
        <div class="offer">No Cost EMI on Pet Supplies</div>
        <div class="offer">7-Day Easy Returns</div>
        <div class="offer">Cash on Delivery | UPI Supported</div>
        <div class="offer">Up to 20% Off on First Purchase</div>
      </div>
    </section>

    <section id="products" style="margin-top:18px;">
      <h2 style="margin-bottom:10px;">Featured Pets & Supplies</h2>

      <div class="grid">
        <!-- Product 1 -->
        <article class="card" data-id="prod-1">
          <img src="https://images.unsplash.com/photo-1546182990-dffeafbe841d?w=900&q=60&auto=format&fit=crop" alt="Golden Retriever Puppy">
          <div>
            <h3>Golden Retriever Puppy</h3>
            <p>Adorable 3-month-old Golden Retriever, fully vaccinated and playful. Pure Breed | Vaccinated</p>
            <div class="price">₹45,000</div>
          </div>
          <div class="actions">
            <button class="btn primary" onclick="addToCart('prod-1','Golden Retriever Puppy',45000)">Add to Cart</button>
            <button class="btn ghost" onclick="enquire('Golden Retriever Puppy')">Enquire Now</button>
          </div>
        </article>

        <!-- Product 2 -->
        <article class="card" data-id="prod-2">
          <img src="https://images.unsplash.com/photo-1518791841217-8f162f1e1131?w=900&q=60&auto=format&fit=crop" alt="Persian Cat">
          <div>
            <h3>Persian Cat</h3>
            <p>Fluffy Persian kitten with blue eyes, litter trained and affectionate. 2 Months Old</p>
            <div class="price">₹25,000</div>
          </div>
          <div class="actions">
            <button class="btn primary" onclick="addToCart('prod-2','Persian Cat',25000)">Add to Cart</button>
            <button class="btn ghost" onclick="enquire('Persian Cat')">Enquire Now</button>
          </div>
        </article>

        <!-- Product 3 -->
        <article class="card" data-id="prod-3">
          <img src="https://images.unsplash.com/photo-1574169208507-84376144848b?w=900&q=60&auto=format&fit=crop" alt="Love Birds">
          <div>
            <h3>Love Birds Pair</h3>
            <p>Colorful pair of love birds, healthy and chirpy. Comes with cage and food starter kit.</p>
            <div class="price">₹8,999</div>
          </div>
          <div class="actions">
            <button class="btn primary" onclick="addToCart('prod-3','Love Birds Pair',8999)">Add to Cart</button>
            <button class="btn ghost" onclick="enquire('Love Birds Pair')">Enquire Now</button>
          </div>
        </article>

        <!-- Product 4 -->
        <article class="card" data-id="prod-4">
          <img src="https://images.unsplash.com/photo-1574226516831-e1dff420e8f8?w=900&q=60&auto=format&fit=crop" alt="Goldfish Kit">
          <div>
            <h3>Fancy Goldfish Kit (Set of 5)</h3>
            <p>Set of 5 colorful goldfish with aquarium, filter, and food. Easy for beginners.</p>
            <div class="price">₹2,499</div>
          </div>
          <div class="actions">
            <button class="btn primary" onclick="addToCart('prod-4','Fancy Goldfish Kit',2499)">Add to Cart</button>
            <button class="btn ghost" onclick="enquire('Fancy Goldfish Kit')">Enquire Now</button>
          </div>
        </article>
      </div>
    </section>

    <footer>
      <p>© <span id="year"></span> PawParadise — All Rights Reserved • Free Shipping Across India • 7-Day Returns</p>
    </footer>
  </main>

  <script>
    // Small interactive JS: cart state in localStorage
    document.getElementById('year').textContent = new Date().getFullYear();

    const cartKey = 'paw_cart';
    function getCart() {
      try { return JSON.parse(localStorage.getItem(cartKey) || '{}'); } catch(e) { return {}; }
    }
    function saveCart(cart) { localStorage.setItem(cartKey, JSON.stringify(cart)); updateCartUI(); }

    function updateCartUI() {
      const cart = getCart();
      const count = Object.values(cart).reduce((s,i)=>s+i.qty,0);
      document.getElementById('cartCount').textContent = count;
    }

    function addToCart(id, name, price) {
      const cart = getCart();
      if (!cart[id]) cart[id] = { id, name, price, qty:0 };
      cart[id].qty += 1;
      saveCart(cart);
      alert(name + ' added to cart.');
    }

    function enquire(name) {
      const message = encodeURIComponent('Hi, I want to enquire about: ' + name);
      // open mailto as a simple enquiry flow (replace with real contact logic)
      window.location.href = 'mailto:info@pawparadise.example?subject=Enquiry&body=' + message;
    }

    function doSearch() {
      const q = document.getElementById('search').value.trim();
      if (!q) { alert('Type something to search.'); return; }
      // basic client-side search: highlight matching cards
      const cards = Array.from(document.querySelectorAll('.card'));
      let found = false;
      cards.forEach(c => {
        const text = c.textContent.toLowerCase();
        if (text.includes(q.toLowerCase())) {
          c.style.border = '2px solid #0a8f5f';
          found = true;
        } else {
          c.style.border = 'none';
        }
      });
      if (!found) alert('No matches found for "' + q + '".');
    }

    // init
    updateCartUI();
  </script>
</body>
</html>
