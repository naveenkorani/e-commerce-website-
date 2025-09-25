<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width,initial-scale=1">
  <title>Copper-Fit — Clothing E‑commerce</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700;800&display=swap" rel="stylesheet">
  <meta name="description" content="Orion Threads — a responsive demo clothing e-commerce site built with HTML & CSS">
  <style>
      :root{
      --bg:#f6f7fb;
      --card:#ffffff;
      --accent:#0b6cf7;
      --muted:#6b7280;
      --radius:14px;
      --shadow: 0 6px 18px rgba(12,24,60,0.08);
      --max-width:1200px;
      --gap:20px;
      --glass: rgba(255,255,255,0.6);
    }
    *{box-sizing:border-box}
    html,body{height:100%}
    body{
      margin:0;
      font-family:Inter, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
      background:linear-gradient(180deg,var(--bg),#fff);
      color:#111827;
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      line-height:1.4;
    }
    .container{max-width:var(--max-width);
        margin:24px auto;padding:0 18px}
header{
      display:flex;align-items:center;
      justify-content:space-between;
      padding:16px 0;
    }
    .brand{display:flex;
        gap:12px;
        align-items:center}
    .logo{
      width:46px;
      height:46px;
      border-radius:10px;
      background:linear-gradient(135deg,var(--accent),#6b21a8);
      display:flex;align-items:center;
      justify-content:center;color:white;
      font-weight:800;
      font-size:18px;
      box-shadow:var(--shadow)
    }
    nav{display:flex;gap:18px;align-items:center}
    .nav-link{color:var(--muted);text-decoration:none;
        font-weight:600}
    .searchbar{display:flex;
        align-items:center;
        gap:10px;background:var(--card);
        padding:8px 12px;
        border-radius:999px;
        min-width:240px;
        box-shadow:var(--shadow)}
    .searchbar input{border:0;
        outline:none;
        background:transparent;
        font-size:14px}
    .icon-btn{background:transparent;
        border:0;
        padding:8px;
        border-radius:10px;
        cursor:pointer}
    .actions{display:flex;
        align-items:center;
        gap:10px}
    .cta{background:var(--accent);
        color:#fff;
        padding:10px 14px;
        border-radius:10px;
        border:0;cursor:pointer;
        font-weight:700}
    .hero{display:grid;
        grid-template-columns:1fr 420px;
        gap:24px;
        align-items:center;
        margin-top:12px}
    .hero-card{background:linear-gradient(180deg, rgba(255,255,255,0.8), rgba(255,255,255,0.6));
        padding:28px;
        border-radius:20px;
        box-shadow:var(--shadow)}
    .hero h1{font-size:32px;
        margin:0 0 12px}
    .hero p{color:var(--muted);
        margin:0 0 18px}
    .hero .shop-btn{background:transparent;
        border:2px solid var(--accent);
        color:var(--accent);
        padding:10px 16px;
        border-radius:12px;
        font-weight:700;
        cursor:pointer}
    .hero-image{background:linear-gradient(120deg,#fff 0%, #f0f7ff 100%);
        border-radius:20px;
        padding:18px;
        display:flex;
        align-items:center;
        justify-content:center;
        height:260px}
    .hero-image img{max-width:100%;
        max-height:100%;
        border-radius:12px;
        object-fit:cover}
    .grid{display:grid;
        grid-template-columns:260px 1fr;
        gap:var(--gap);
        margin-top:20px}
    .sidebar{background:var(--card);
        padding:18px;
        border-radius:16px;
        box-shadow:var(--shadow)}
    .filter-title{font-weight:700;
        margin-bottom:12px}
    .category{display:flex;
        flex-wrap:wrap;
        gap:8px}
    .pill{padding:8px 10px;
        background:#f3f4f6;
        border-radius:999px;
        font-weight:600;
        font-size:13px;
        color:#374151}
    .range{margin:14px 0}
    .checkbox-list{display:flex;
        flex-direction:column;
        gap:10px}
    .checkbox-list label{display:flex;
        align-items:center;
        gap:10px;
        color:var(--muted)}
    .products{display:grid;
        grid-template-columns:repeat(3,1fr);
        gap:18px}
    .product{background:var(--card);
        border-radius:20px;
        padding:12px;
        box-shadow:var(--shadow);
        display:flex;
        flex-direction:column;
        gap:20px}
    .product img{width:100%;
        height:400px;
        object-fit:cover;
        border-radius:20px}
    .product h3{margin:6px 0 0;
        font-size:16px}
    .price-row{display:flex;
        align-items:center;
        justify-content:space-between}
    .price{font-weight:800}
    .old{color:var(--muted);
        text-decoration:line-through;
        font-weight:600}
    .tag{background:#fef3c7;
        color:#92400e;
        padding:6px 8px;
        border-radius:8px;
        font-weight:700;
        font-size:12px}
    .product .btn-row{display:flex;
        gap:8px}
    .btn{flex:1;
        padding:10px;
        border-radius:10px;
        border:1px solid transparent;
        cursor:pointer;
        font-weight:700}
    .btn-add{background:var(--accent);
        color:white}
    .btn-view{background:transparent;
        border:1px solid #0b6cf7}
    .product:hover{transform:translateY(-6px);
        transition:transform 220ms ease}
    footer{margin-top:28px;
        padding:28px 0;
        color:var(--muted)}
    .footer-grid{display:flex;
        justify-content:space-between;
        gap:20px;flex-wrap:wrap}   
    @media (max-width:1000px){
      .hero{grid-template-columns:1fr}
      .grid{grid-template-columns:1fr}
      .products{grid-template-columns:repeat(2,1fr)}
    }
    @media (max-width:640px){
      header{flex-direction:column;align-items:flex-start;gap:12px}
      .searchbar{min-width:unset;width:100%}
      .products{grid-template-columns:1fr}
      .hero-image{height:200px}
    }
    .muted{color:var(--muted)}
input[type="checkbox"].modal-toggle{display:none}
    .modal{position:fixed;
        inset:0;display:flex;
        align-items:center;
        justify-content:center;
        background:rgba(2,6,23,0.5);
        opacity:0;
        pointer-events:none;
        transition:opacity 200ms ease}
    .modal-card{background:var(--card);
        border-radius:16px;
        padding:18px;
        max-width:920px;
        width:95%;
        box-shadow:0 20px 60px rgba(2,6,23,0.45);
        display:grid;
        grid-template-columns:1fr 1fr;
        gap:18px}
    .modal-toggle:checked + .modal{opacity:1;
        pointer-events:auto}
    .modal img{width:100%;
        eight:100%;
        object-fit:cover;
        border-radius:10px}
    .modal h2{margin:0}
    .close-btn{background:#f3f4f6;
        border:0;
        padding:8px 12px;
        border-radius:10px;
        cursor:pointer}
    .small{font-size:13px}
  </style>
</head>
<body>
  <div class="container">
    <header>
      <div class="brand">
        <div class="logo">CF</div>
        <div>
          <div style="font-weight:800">Copper-Fit</div>
          <div style="font-size:12px;color:var(--muted);margin-top:2px">Sustainable • Curated • Stylish</div>
        </div>
      </div>
      <nav>
        <div class="searchbar" role="search" aria-label="Search products">
          <svg width="16" height="16" viewBox="0 0 24 24" fill="none" aria-hidden style="opacity:0.7"><path d="M21 21l-4.35-4.35" stroke="#6b7280" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"></path><circle cx="11" cy="11" r="6" stroke="#6b7280" stroke-width="1.5"></circle></svg>
          <input type="search" placeholder="Search for shirts, jeans, accessories...">
        </div>
        <a class="nav-link" href="#">Men</a>
        <a class="nav-link" href="#">New</a>
      </nav>
      <div class="actions">
        <button class="icon-btn" aria-label="Wishlist">♥</button>
        <button class="icon-btn" aria-label="Account">👤</button>
        <button class="cta">Cart (0)</button>
      </div>
    </header>
    <section class="hero">
      <div class="hero-card">
        <h1>Upgrade your wardrobe — responsibly</h1>
        <p>Discover curated pieces, seasonal drops, and everyday essentials crafted for comfort and longevity.</p>
        <div style="display:flex;gap:10px">
          <button class="shop-btn">Contect us.</button>
          <button class="shop-btn" style="border-style:solid;border-color:#000;background:#000;color:#fff">Shop Men's</button>
        </div>
        <div style="margin-top:18px;color:var(--muted);font-size:14px">
          Free shipping on orders over ₹1999 • 30-day returns
        </div>
      </div>
      <div class="hero-image">
        <img src="https://images.unsplash.com/photo-1541099649105-f69ad21f3246?q=80&w=1200&auto=format&fit=crop&ixlib=rb-4.0.3&s=7a8b4f0d8b2b1678a2c6bb6b2f0b6f70" alt="fashion hero">
      </div>
    </section>
        <div style="margin-top:18px;font-size:13px;color:var(--muted)"></div>
      </aside>
      <main>
        <div style="display:flex;align-items:center;justify-content:space-between;margin-bottom:12px">
          <div>
            <div style="font-weight:800">Results</div>
            <div class="muted small">Showing All Products</div>
          </div>
                  </div>
<section class="products" aria-live="polite">
          <article class="product">
            <img src="https://encrypted-tbn0.gstatic.com/shopping?q=tbn:ANd9GcQ6T8P0DTFZy6OQKAWvNeqn9oXXuxbfon3GVin9ALqJ_Dg-LzEwVCZXk8lKT9q17UvfWUwlqL1bPwyjkDY_480sZ-3HLYTGZ27Mrj2EYqKiS5wwTJvFykcMn31b" alt="Shirts">
            <div style="display:flex;align-items:center;justify-content:space-between">
              <h3>White Shirts</h3>
              <div class="tag">Bestseller</div>
            </div>
            <div class="muted">Made from organic cotton</div>
            <div class="price-row"><div class="price">₹1099</div><div class="old">₹1599</div></div>
            <div class="btn-row">
              <label for="modal-1" class="btn btn-view" style="text-align: center;">Add to Cart</label>
              <button class="btn btn-add">Quick View</button>
            </div>
          </article>
          <article class="product">
            <img src="https://encrypted-tbn1.gstatic.com/shopping?q=tbn:ANd9GcS3lgI0_uBibIefJx_7OwAaZeY3s2qy-XA9mKTOdtd6Yy7kcVd_ViqMfQcHKdIV8gZ9hdAxzBZshSQ0NV_ZMUiOhXRhl98umyyagAtB24KA1953rZ1NmkdGz46b" alt="Shirts">
            <div style="display:flex;align-items:center;justify-content:space-between">
              <h3>Black T-Shirts</h3>
              <div class="tag">Bestseller</div>
            </div>
            <div class="muted">Made from organic cotton</div>
            <div class="price-row"><div class="price">₹999</div><div class="old">₹1499</div></div>
            <div class="btn-row">
              <label for="modal-2" class="btn btn-view" style="text-align: center;">Add to Cart</label>
              <button class="btn btn-add">Quick View</button>
            </div>
          </article>
          <article class="product">
            <img src="https://encrypted-tbn3.gstatic.com/shopping?q=tbn:ANd9GcT75vRHGRzKir7dtaTgM4xZoDmwGe-IM5ZdEZjZOKJXxXWUnz4E2BzGvQ_t3RQR2vp-SpAv4irmDI9QfsEtS-eJVlJ_Wb7GJSKmnf16EJiwhyCz-zAF58iB8LE" alt="Shirts">
            <div style="display:flex;align-items:center;justify-content:space-between">
              <h3>Brown Shirt</h3>
              <div class="tag">Bestseller</div>
            </div>
            <div class="muted">Made from organic cotton</div>
            <div class="price-row"><div class="price">₹1599</div><div class="old">₹2199</div></div>
            <div class="btn-row">
              <label for="modal-3" class="btn btn-view" style="text-align: center;">Add to Cart</label>
              <button class="btn btn-add">Quick View</button>
            </div>
          </article>
          <article class="product">
            <img src="https://encrypted-tbn1.gstatic.com/shopping?q=tbn:ANd9GcRLfhsZExF8t_U9aGxOIjvNmh4xY95sLC5nZVWg4-SKJSLoqKxLiJzT7kAkUaL5vLx9M7wg4X_W4jYTLp8YElobhBuPb4TMI7PGxp681Inn-uiShaY7AddX2kEs" alt="Denim jacket">
            <h3>Beige Polo T-Shirt</h3>
            <div class="muted">Stone wash, unisex</div>
            <div class="price-row"><div class="price">₹1899</div><div class="old">₹2499</div></div>
            <div class="btn-row">
              <label for="modal-4" class="btn btn-view" style="text-align: center;">Add to Cart</label>
              <button class="btn btn-add">Quick View</button>
            </div>
          </article>
          <article class="product">
            <img src="https://encrypted-tbn0.gstatic.com/shopping?q=tbn:ANd9GcSPEwu9FDZ8qRq9UZNrt-C3loJessGrCEASLobcxia22gon0yLt19HhUPQt9Q8VYaYx-UHl8j5DfUHTE4FwPjFphdqRtXo3Ym5dXT5holQgk5a6SLLhf48MCK2b" alt="Casual chinos">
            <h3>Maroon Polo T-Shirt</h3>
            <div class="muted">Slim fit, machine washable</div>
            <div class="price-row"><div class="price">₹1899</div><div class="old">₹2499</div></div>
            <div class="btn-row">
              <label for="modal-5" class="btn btn-view" style="text-align: center;">Add to Cart</label>
              <button class="btn btn-add">Quick View</button>
            </div>
          </article>
          <article class="product">
            <img src="https://encrypted-tbn0.gstatic.com/shopping?q=tbn:ANd9GcTFZe1NrAI6yhm2WMPjNkhFo-UGkIsSI6VoXGQCJS1MsbWMyp4Qm1EjbBazBHwXD8z9f9Epu_v5E9KjOtKD9K6Xn-MPxfanliJPS8M3ZDFcfBLbkE9eZxCqf-6m" alt="Striped shirt">
            <h3>Lite Blue Linen Shirt</h3>
            <div class="muted">Lightweight summer linen</div>
            <div class="price-row"><div class="price">₹1099</div><div class="old">₹1599</div></div>
            <div class="btn-row">
              <label for="modal-6" class="btn btn-view" style="text-align: center;">Add to Cart</label>
              <button class="btn btn-add">Quick View</button>
            </div>
          </article>
          <article class="product">
            <img src="https://encrypted-tbn2.gstatic.com/shopping?q=tbn:ANd9GcRvjzmXRkTocpdVv2zXRwTEKkWxO36mOBjDFeki-aqPD6B1wBZhRI6wgxBfUiRJ8rp5xqLL7OyB98E1VcsoWyit-0qoQLmzr2Nl3_AkWh44SPrsFvFWC_86Od8" alt="Athletic hoodie">
            <h3>Black n White Shirt</h3>
            <div class="muted">Brushed interior for warmth</div>
            <div class="price-row"><div class="price">₹1299</div><div class="old">₹1799</div></div>
            <div class="btn-row">
              <label for="modal-7" class="btn btn-view" style="text-align: center;">Add to Cart</label>
              <button class="btn btn-add">Quick View</button>
            </div>
          </article>
          <article class="product">
            <img src="https://encrypted-tbn3.gstatic.com/shopping?q=tbn:ANd9GcQOts1p4mHdrshZXz_WHwros1U0KQIXT5u89LBA83vrvNOcl2GWCd3O5gpc0-PY8Ltaafx3qE_7TtSVChh--ZiXc4fW5BJk9-OQY07zWKKlm-pwL2sRiIYcm5o" alt="Patterned scarf">
            <h3>Green Linen Shirt</h3>
            <div class="muted">Hand‑finished edges</div>
            <div class="price-row"><div class="price">₹1099</div><div class="old">₹1599</div></div>
            <div class="btn-row">
              <label for="modal-8" class="btn btn-view" style="text-align: center;">Add to Cart</label>
              <button class="btn btn-add">Quick View</button>
            </div>
          </article>
          <article class="product">
            <img src="https://encrypted-tbn0.gstatic.com/shopping?q=tbn:ANd9GcQIAhfK12fzPNo2984GQpISRRFZLbQxyvRG5OCSgulQhmZId3PO7fcoRiC-osInXx6_JkhVNSBZgWEC04hS5wC1mtcpMq7RT91JWGXQRLs3EMWVbgrxHPM-siQ" alt="Patterned scarf">
            <h3>Yellow n White Shirt</h3>
            <div class="muted">Hand‑finished edges</div>
            <div class="price-row"><div class="price">₹1099</div><div class="old">₹1599</div></div>
            <div class="btn-row">
              <label for="modal-9" class="btn btn-view" style="text-align: center;">Add to Cart</label>
              <button class="btn btn-add">Quick View</button>
            </div>
          </article>
          <article class="product">
            <img src="https://encrypted-tbn1.gstatic.com/shopping?q=tbn:ANd9GcR04TCCMkoa7aUJ-wZ0Q-3RfutpEJeEVfBvTG3dd3B-X3Y1EpzthgL8rwXBo6EJCyiLFr7frYz7kQakVx-zRR4_AaVS_9mDm8g5JL4Iw5k25Wen7BNzrSF9zg" alt="Patterned scarf">
            <h3>Lite Blue Regular-Fit Jeens</h3>
            <div class="muted">Hand‑finished edges</div>
            <div class="price-row"><div class="price">₹2599</div><div class="old">₹3599</div></div>
            <div class="btn-row">
              <label for="modal-10" class="btn btn-view" style="text-align: center;">Add to Cart</label>
              <button class="btn btn-add">Quick View</button>
            </div>
          </article>
          <article class="product">
            <img src="https://encrypted-tbn1.gstatic.com/shopping?q=tbn:ANd9GcTmvO4pjOcleNNyVwherFagXYxPNs13tyhIEdHcSOqA6ErlaHRSR6lXVXgHYrFQYioPOxH-ydv_CeKldilgV6rypvuo11jfBYRcFAuqYPDJ" alt="Patterned scarf">
            <h3>Black Regular-Fit Jeens</h3>
            <div class="muted">Hand‑finished edges</div>
            <div class="price-row"><div class="price">₹2599</div><div class="old">₹3599</div></div>
            <div class="btn-row">
              <label for="modal-11" class="btn btn-view" style="text-align: center;">Add to Cart</label>
              <button class="btn btn-add">Quick View</button>
            </div>
          </article>
          <article class="product">
            <img src="https://encrypted-tbn1.gstatic.com/shopping?q=tbn:ANd9GcSIkQxgOVLBKHSPwxl_0iaaC_x-yY2mucP_zlpykVxQFjDABjqCf00mr6Rpua1OGUDmze2KGFwd9TpEan3t83b6sVQjBcRXg8iFE8nxZWM-1OaHVAFqxu1H" alt="Patterned scarf">
            <h3>White Regular-Fit Jeens</h3>
            <div class="muted">Hand‑finished edges</div>
            <div class="price-row"><div class="price">₹2599</div><div class="old">₹3599</div></div>
            <div class="btn-row">
              <label for="modal-12" class="btn btn-view" style="text-align: center;">Add to Cart</label>
              <button class="btn btn-add">Quick View</button>
            </div>
          </article>
        </section>
        <div style="margin-top:18px;display:flex;justify-content:center">
          <button class="btn" style="padding:10px 22px;background:#eef2ff;border-radius:12px;font-weight:800">Load more</button>
        </div>
      </main>
    </div>
    <input id="modal-1" class="modal-toggle" type="checkbox">
    <div class="modal" aria-hidden="true">
      <div class="modal-card">
        <img src="https://encrypted-tbn0.gstatic.com/shopping?q=tbn:ANd9GcQ6T8P0DTFZy6OQKAWvNeqn9oXXuxbfon3GVin9ALqJ_Dg-LzEwVCZXk8lKT9q17UvfWUwlqL1bPwyjkDY_480sZ-3HLYTGZ27Mrj2EYqKiS5wwTJvFykcMn31b" alt="Product large">
        <div>
          <h2>White Shirt</h2>
          <p class="muted">Perfect for everyday wear. Organic cotton, regular fit.</p>
          <div style="margin-top:12px;font-weight:800;font-size:22px">₹1099 <span class="old" style="font-weight:600;font-size:14px;margin-left:8px">₹1599</span></div>
          <div style="margin-top:12px">
            <div style="font-weight:700;margin-bottom:6px">Size</div>
            <div style="display:flex;gap:8px;margin-bottom:12px"><button class="pill">S</button><button class="pill">M</button><button class="pill">L</button></div>
            <div style="font-weight:700;margin-bottom:6px">Quantity</div>
            <div style="display:flex;gap:8px;align-items:center"><button class="close-btn">−</button><div style="min-width:34px;text-align:center">1</div><button class="close-btn">+</button></div>
          </div>
          <div style="margin-top:18px;display:flex;gap:10px">
            <label for="modal-1" class="close-btn">Close</label>
            <button class="cta">Add to cart</button>
          </div>
        </div>
      </div>
    </div>
    <input id="modal-2" class="modal-toggle" type="checkbox">
    <div class="modal" aria-hidden="true">
      <div class="modal-card">
        <img src="https://encrypted-tbn1.gstatic.com/shopping?q=tbn:ANd9GcS3lgI0_uBibIefJx_7OwAaZeY3s2qy-XA9mKTOdtd6Yy7kcVd_ViqMfQcHKdIV8gZ9hdAxzBZshSQ0NV_ZMUiOhXRhl98umyyagAtB24KA1953rZ1NmkdGz46b" alt="Product large">
        <div>
          <h2>Black T-Shirt</h2>
          <p class="muted">Perfect for everyday wear. Organic cotton, regular fit.</p>
          <div style="margin-top:12px;font-weight:800;font-size:22px">₹999 <span class="old" style="font-weight:600;font-size:14px;margin-left:8px">₹1499</span></div>
          <div style="margin-top:12px">
            <div style="font-weight:700;margin-bottom:6px">Size</div>
            <div style="display:flex;gap:8px;margin-bottom:12px"><button class="pill">S</button><button class="pill">M</button><button class="pill">L</button></div>
            <div style="font-weight:700;margin-bottom:6px">Quantity</div>
            <div style="display:flex;gap:8px;align-items:center"><button class="close-btn">−</button><div style="min-width:34px;text-align:center">1</div><button class="close-btn">+</button></div>
          </div>
          <div style="margin-top:18px;display:flex;gap:10px">
            <label for="modal-2" class="close-btn">Close</label>
            <button class="cta">Add to cart</button>
          </div>
        </div>
      </div>
    </div>
    <input id="modal-3" class="modal-toggle" type="checkbox">
    <div class="modal" aria-hidden="true">
      <div class="modal-card">
        <img src="https://encrypted-tbn3.gstatic.com/shopping?q=tbn:ANd9GcT75vRHGRzKir7dtaTgM4xZoDmwGe-IM5ZdEZjZOKJXxXWUnz4E2BzGvQ_t3RQR2vp-SpAv4irmDI9QfsEtS-eJVlJ_Wb7GJSKmnf16EJiwhyCz-zAF58iB8LE" alt="Product large">
        <div>
          <h2>Black T-Shirt</h2>
          <p class="muted">Perfect for everyday wear. Organic cotton, regular fit.</p>
          <div style="margin-top:12px;font-weight:800;font-size:22px">₹1599 <span class="old" style="font-weight:600;font-size:14px;margin-left:8px">₹2199</span></div>
          <div style="margin-top:12px">
            <div style="font-weight:700;margin-bottom:6px">Size</div>
            <div style="display:flex;gap:8px;margin-bottom:12px"><button class="pill">S</button><button class="pill">M</button><button class="pill">L</button></div>
            <div style="font-weight:700;margin-bottom:6px">Quantity</div>
            <div style="display:flex;gap:8px;align-items:center"><button class="close-btn">−</button><div style="min-width:34px;text-align:center">1</div><button class="close-btn">+</button></div>
          </div>
          <div style="margin-top:18px;display:flex;gap:10px">
            <label for="modal-3" class="close-btn">Close</label>
            <button class="cta">Add to cart</button>
          </div>
        </div>
      </div>
    </div>
    <input id="modal-4" class="modal-toggle" type="checkbox">
    <div class="modal" aria-hidden="true">
      <div class="modal-card">
        <img src="https://encrypted-tbn1.gstatic.com/shopping?q=tbn:ANd9GcRLfhsZExF8t_U9aGxOIjvNmh4xY95sLC5nZVWg4-SKJSLoqKxLiJzT7kAkUaL5vLx9M7wg4X_W4jYTLp8YElobhBuPb4TMI7PGxp681Inn-uiShaY7AddX2kEs" alt="Product large">
        <div>
          <h2>Beige Polo T-Shirt</h2>
          <p class="muted">Perfect for everyday wear. Organic cotton, regular fit.</p>
          <div style="margin-top:12px;font-weight:800;font-size:22px">₹1899 <span class="old" style="font-weight:600;font-size:14px;margin-left:8px">₹2499</span></div>
          <div style="margin-top:12px">
            <div style="font-weight:700;margin-bottom:6px">Size</div>
            <div style="display:flex;gap:8px;margin-bottom:12px"><button class="pill">S</button><button class="pill">M</button><button class="pill">L</button></div>
            <div style="font-weight:700;margin-bottom:6px">Quantity</div>
            <div style="display:flex;gap:8px;align-items:center"><button class="close-btn">−</button><div style="min-width:34px;text-align:center">1</div><button class="close-btn">+</button></div>
          </div>
          <div style="margin-top:18px;display:flex;gap:10px">
            <label for="modal-4" class="close-btn">Close</label>
            <button class="cta">Add to cart</button>
          </div>
        </div>
      </div>
    </div>
    <input id="modal-5" class="modal-toggle" type="checkbox">
    <div class="modal" aria-hidden="true">
      <div class="modal-card">
        <img src="https://encrypted-tbn0.gstatic.com/shopping?q=tbn:ANd9GcSPEwu9FDZ8qRq9UZNrt-C3loJessGrCEASLobcxia22gon0yLt19HhUPQt9Q8VYaYx-UHl8j5DfUHTE4FwPjFphdqRtXo3Ym5dXT5holQgk5a6SLLhf48MCK2b" alt="Product large">
        <div>
          <h2>Maroon Polo T-Shirt</h2>
          <p class="muted">Perfect for everyday wear. Organic cotton, regular fit.</p>
          <div style="margin-top:12px;font-weight:800;font-size:22px">₹1899 <span class="old" style="font-weight:600;font-size:14px;margin-left:8px">₹2499</span></div>
          <div style="margin-top:12px">
            <div style="font-weight:700;margin-bottom:6px">Size</div>
            <div style="display:flex;gap:8px;margin-bottom:12px"><button class="pill">S</button><button class="pill">M</button><button class="pill">L</button></div>
            <div style="font-weight:700;margin-bottom:6px">Quantity</div>
            <div style="display:flex;gap:8px;align-items:center"><button class="close-btn">−</button><div style="min-width:34px;text-align:center">1</div><button class="close-btn">+</button></div>
          </div>
          <div style="margin-top:18px;display:flex;gap:10px">
            <label for="modal-5" class="close-btn">Close</label>
            <button class="cta">Add to cart</button>
          </div>
        </div>
      </div>
    </div>
    <input id="modal-6" class="modal-toggle" type="checkbox">
    <div class="modal" aria-hidden="true">
      <div class="modal-card">
        <img src="https://encrypted-tbn0.gstatic.com/shopping?q=tbn:ANd9GcTFZe1NrAI6yhm2WMPjNkhFo-UGkIsSI6VoXGQCJS1MsbWMyp4Qm1EjbBazBHwXD8z9f9Epu_v5E9KjOtKD9K6Xn-MPxfanliJPS8M3ZDFcfBLbkE9eZxCqf-6m" alt="Product large">
        <div>
          <h2>Lite Blue Linen Shirt</h2>
          <p class="muted">Perfect for everyday wear. Organic cotton, regular fit.</p>
          <div style="margin-top:12px;font-weight:800;font-size:22px">₹1099 <span class="old" style="font-weight:600;font-size:14px;margin-left:8px">₹1599</span></div>
          <div style="margin-top:12px">
            <div style="font-weight:700;margin-bottom:6px">Size</div>
            <div style="display:flex;gap:8px;margin-bottom:12px"><button class="pill">S</button><button class="pill">M</button><button class="pill">L</button></div>
            <div style="font-weight:700;margin-bottom:6px">Quantity</div>
            <div style="display:flex;gap:8px;align-items:center"><button class="close-btn">−</button><div style="min-width:34px;text-align:center">1</div><button class="close-btn">+</button></div>
          </div>
          <div style="margin-top:18px;display:flex;gap:10px">
            <label for="modal-6" class="close-btn">Close</label>
            <button class="cta">Add to cart</button>
          </div>
        </div>
      </div>
    </div>
    <input id="modal-7" class="modal-toggle" type="checkbox">
    <div class="modal" aria-hidden="true">
      <div class="modal-card">
        <img src="https://encrypted-tbn2.gstatic.com/shopping?q=tbn:ANd9GcRvjzmXRkTocpdVv2zXRwTEKkWxO36mOBjDFeki-aqPD6B1wBZhRI6wgxBfUiRJ8rp5xqLL7OyB98E1VcsoWyit-0qoQLmzr2Nl3_AkWh44SPrsFvFWC_86Od8" alt="Product large">
        <div>
          <h2>Black n White Shirt</h2>
          <p class="muted">Perfect for everyday wear. Organic cotton, regular fit.</p>
          <div style="margin-top:12px;font-weight:800;font-size:22px">₹1299 <span class="old" style="font-weight:600;font-size:14px;margin-left:8px">₹1799</span></div>
          <div style="margin-top:12px">
            <div style="font-weight:700;margin-bottom:6px">Size</div>
            <div style="display:flex;gap:8px;margin-bottom:12px"><button class="pill">S</button><button class="pill">M</button><button class="pill">L</button></div>
            <div style="font-weight:700;margin-bottom:6px">Quantity</div>
            <div style="display:flex;gap:8px;align-items:center"><button class="close-btn">−</button><div style="min-width:34px;text-align:center">1</div><button class="close-btn">+</button></div>
          </div>
          <div style="margin-top:18px;display:flex;gap:10px">
            <label for="modal-7" class="close-btn">Close</label>
            <button class="cta">Add to cart</button>
          </div>
        </div>
      </div>
    </div>
    <input id="modal-8" class="modal-toggle" type="checkbox">
    <div class="modal" aria-hidden="true">
      <div class="modal-card">
        <img src="https://encrypted-tbn3.gstatic.com/shopping?q=tbn:ANd9GcQOts1p4mHdrshZXz_WHwros1U0KQIXT5u89LBA83vrvNOcl2GWCd3O5gpc0-PY8Ltaafx3qE_7TtSVChh--ZiXc4fW5BJk9-OQY07zWKKlm-pwL2sRiIYcm5o" alt="Product large">
        <div>
          <h2>Green Linen Shirt</h2>
          <p class="muted">Perfect for everyday wear. Organic cotton, regular fit.</p>
          <div style="margin-top:12px;font-weight:800;font-size:22px">₹1099 <span class="old" style="font-weight:600;font-size:14px;margin-left:8px">₹1599</span></div>
          <div style="margin-top:12px">
            <div style="font-weight:700;margin-bottom:6px">Size</div>
            <div style="display:flex;gap:8px;margin-bottom:12px"><button class="pill">S</button><button class="pill">M</button><button class="pill">L</button></div>
            <div style="font-weight:700;margin-bottom:6px">Quantity</div>
            <div style="display:flex;gap:8px;align-items:center"><button class="close-btn">−</button><div style="min-width:34px;text-align:center">1</div><button class="close-btn">+</button></div>
          </div>
          <div style="margin-top:18px;display:flex;gap:10px">
            <label for="modal-8" class="close-btn">Close</label>
            <button class="cta">Add to cart</button>
          </div>
        </div>
      </div>
    </div>
    <input id="modal-9" class="modal-toggle" type="checkbox">
    <div class="modal" aria-hidden="true">
      <div class="modal-card">
        <img src="https://encrypted-tbn0.gstatic.com/shopping?q=tbn:ANd9GcQIAhfK12fzPNo2984GQpISRRFZLbQxyvRG5OCSgulQhmZId3PO7fcoRiC-osInXx6_JkhVNSBZgWEC04hS5wC1mtcpMq7RT91JWGXQRLs3EMWVbgrxHPM-siQ" alt="Product large">
        <div>
          <h2>Yellow n White Shirt</h2>
          <p class="muted">Perfect for everyday wear. Organic cotton, regular fit.</p>
          <div style="margin-top:12px;font-weight:800;font-size:22px">₹1099 <span class="old" style="font-weight:600;font-size:14px;margin-left:8px">₹1599</span></div>
          <div style="margin-top:12px">
            <div style="font-weight:700;margin-bottom:6px">Size</div>
            <div style="display:flex;gap:8px;margin-bottom:12px"><button class="pill">S</button><button class="pill">M</button><button class="pill">L</button></div>
            <div style="font-weight:700;margin-bottom:6px">Quantity</div>
            <div style="display:flex;gap:8px;align-items:center"><button class="close-btn">−</button><div style="min-width:34px;text-align:center">1</div><button class="close-btn">+</button></div>
          </div>
          <div style="margin-top:18px;display:flex;gap:10px">
            <label for="modal-9" class="close-btn">Close</label>
            <button class="cta">Add to cart</button>
          </div>
        </div>
      </div>
    </div>
    <input id="modal-10" class="modal-toggle" type="checkbox">
    <div class="modal" aria-hidden="true">
      <div class="modal-card">
        <img src="https://encrypted-tbn1.gstatic.com/shopping?q=tbn:ANd9GcR04TCCMkoa7aUJ-wZ0Q-3RfutpEJeEVfBvTG3dd3B-X3Y1EpzthgL8rwXBo6EJCyiLFr7frYz7kQakVx-zRR4_AaVS_9mDm8g5JL4Iw5k25Wen7BNzrSF9zg" alt="Product large">
        <div>
          <h2>Lite Blue Regular-Fit Jeens</h2>
          <p class="muted">Perfect for everyday wear. Organic cotton, regular fit.</p>
          <div style="margin-top:12px;font-weight:800;font-size:22px">₹2599 <span class="old" style="font-weight:600;font-size:14px;margin-left:8px">₹3599</span></div>
          <div style="margin-top:12px">
            <div style="font-weight:700;margin-bottom:6px">Size</div>
            <div style="display:flex;gap:8px;margin-bottom:12px"><button class="pill">S</button><button class="pill">M</button><button class="pill">L</button></div>
            <div style="font-weight:700;margin-bottom:6px">Quantity</div>
            <div style="display:flex;gap:8px;align-items:center"><button class="close-btn">−</button><div style="min-width:34px;text-align:center">1</div><button class="close-btn">+</button></div>
          </div>
          <div style="margin-top:18px;display:flex;gap:10px">
            <label for="modal-10" class="close-btn">Close</label>
            <button class="cta">Add to cart</button>
          </div>
        </div>
      </div>
    </div>
    <input id="modal-11" class="modal-toggle" type="checkbox">
    <div class="modal" aria-hidden="true">
      <div class="modal-card">
        <img src="https://encrypted-tbn1.gstatic.com/shopping?q=tbn:ANd9GcTmvO4pjOcleNNyVwherFagXYxPNs13tyhIEdHcSOqA6ErlaHRSR6lXVXgHYrFQYioPOxH-ydv_CeKldilgV6rypvuo11jfBYRcFAuqYPDJ" alt="Product large">
        <div>
          <h2>Black Regular-Fit Jeens</h2>
          <p class="muted">Perfect for everyday wear. Organic cotton, regular fit.</p>
          <div style="margin-top:12px;font-weight:800;font-size:22px">₹2599 <span class="old" style="font-weight:600;font-size:14px;margin-left:8px">₹2599</span></div>
          <div style="margin-top:12px">
            <div style="font-weight:700;margin-bottom:6px">Size</div>
            <div style="display:flex;gap:8px;margin-bottom:12px"><button class="pill">S</button><button class="pill">M</button><button class="pill">L</button></div>
            <div style="font-weight:700;margin-bottom:6px">Quantity</div>
            <div style="display:flex;gap:8px;align-items:center"><button class="close-btn">−</button><div style="min-width:34px;text-align:center">1</div><button class="close-btn">+</button></div>
          </div>
          <div style="margin-top:18px;display:flex;gap:10px">
            <label for="modal-11" class="close-btn">Close</label>
            <button class="cta">Add to cart</button>
          </div>
        </div>
      </div>
    </div>
 <input id="modal-12" class="modal-toggle" type="checkbox">
    <div class="modal" aria-hidden="true">
      <div class="modal-card">
        <img src="https://encrypted-tbn1.gstatic.com/shopping?q=tbn:ANd9GcSIkQxgOVLBKHSPwxl_0iaaC_x-yY2mucP_zlpykVxQFjDABjqCf00mr6Rpua1OGUDmze2KGFwd9TpEan3t83b6sVQjBcRXg8iFE8nxZWM-1OaHVAFqxu1H" alt="Product large">
        <div>
          <h2>White Regular-Fit Jeens</h2>
          <p class="muted">Perfect for everyday wear. Organic cotton, regular fit.</p>
          <div style="margin-top:12px;font-weight:800;font-size:22px">₹2599 <span class="old" style="font-weight:600;font-size:14px;margin-left:8px">₹2599</span></div>
          <div style="margin-top:12px">
            <div style="font-weight:700;margin-bottom:6px">Size</div>
            <div style="display:flex;gap:8px;margin-bottom:12px"><button class="pill">S</button><button class="pill">M</button><button class="pill">L</button></div>
            <div style="font-weight:700;margin-bottom:6px">Quantity</div>
            <div style="display:flex;gap:8px;align-items:center"><button class="close-btn">−</button><div style="min-width:34px;text-align:center">1</div><button class="close-btn">+</button></div>
          </div>
          <div style="margin-top:18px;display:flex;gap:10px">
            <label for="modal-12" class="close-btn">Close</label>
            <button class="cta">Add to cart</button>
          </div>
        </div>
      </div>
    </div>
    <footer>
      <div class="footer-grid">
        <div>
          <div style="font-weight:800">Copper Fit</div>
          <div class="muted small">Quality clothing made consciously.</div>
        </div>
        <div style="display:flex;gap:36px;flex-wrap:wrap">
            <div>
                <div style="font-weight:700">MADE BY-</div>
                <div class="muted small">HIMANSHU SACHANI & NAVEEN KORANI</div>
              </div>
          <div>
            <div style="font-weight:700">Company</div>
            <div class="muted small">About • Careers • Press</div>
          </div>
          <div>
            <div style="font-weight:700">Help</div>
            <div class="muted small">Shipping • Returns • FAQs</div>
          </div>
        </div>
        <div class="small muted">© Copper Fit 2025</div>
      </div>
    </footer>
</body>
</html>
