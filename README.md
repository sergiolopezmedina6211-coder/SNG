<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>SNG — GOD STAYS NEAR</title>

  <meta name="description" content="SNG Streetwear — GOD STAYS NEAR">

  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800;900&display=swap" rel="stylesheet">

  <style>

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      font-family: "Inter", sans-serif;
      background: #080808;
      color: white;
      overflow-x: hidden;
    }

    button {
      font-family: inherit;
    }

    /* =========================
       NAVBAR
    ========================= */

    nav {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 75px;
      z-index: 1000;

      display: flex;
      align-items: center;
      justify-content: space-between;

      padding: 0 5%;

      background: rgba(8,8,8,.78);
      backdrop-filter: blur(18px);

      border-bottom: 1px solid rgba(255,255,255,.08);
    }

    .logo {
      font-size: 27px;
      font-weight: 900;
      letter-spacing: -2px;
    }

    .logo span {
      opacity: .35;
    }

    .nav-links {
      display: flex;
      gap: 35px;
      list-style: none;
    }

    .nav-links a {
      color: white;
      text-decoration: none;
      font-size: 13px;
      font-weight: 600;
      letter-spacing: 1px;
      text-transform: uppercase;
      transition: .3s;
    }

    .nav-links a:hover {
      opacity: .45;
    }

    .cart-button {
      border: 1px solid rgba(255,255,255,.25);
      background: transparent;
      color: white;
      padding: 10px 17px;
      border-radius: 30px;
      cursor: pointer;
      transition: .3s;
    }

    .cart-button:hover {
      background: white;
      color: black;
    }

    /* =========================
       HERO
    ========================= */

    .hero {
      min-height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;

      position: relative;
      overflow: hidden;

      background:
        radial-gradient(circle at 50% 40%, #252525 0%, #0b0b0b 42%, #050505 80%);
    }

    .hero::before {
      content: "SNG";
      position: absolute;

      font-size: min(40vw, 600px);
      font-weight: 900;

      color: transparent;
      -webkit-text-stroke: 1px rgba(255,255,255,.06);

      pointer-events: none;
    }

    .hero-content {
      position: relative;
      z-index: 2;
      text-align: center;
      padding: 30px;
    }

    .hero-small {
      font-size: 11px;
      letter-spacing: 7px;
      text-transform: uppercase;
      opacity: .55;
      margin-bottom: 25px;
    }

    .hero h1 {
      font-size: clamp(80px, 18vw, 240px);
      line-height: .75;
      font-weight: 900;
      letter-spacing: -10px;
    }

    .hero-slogan {
      margin-top: 35px;
      font-size: 14px;
      letter-spacing: 9px;
      font-weight: 500;
    }

    .hero-button {
      display: inline-block;
      margin-top: 45px;

      padding: 17px 35px;

      color: black;
      background: white;

      text-decoration: none;
      font-size: 12px;
      font-weight: 800;
      letter-spacing: 2px;

      transition: .35s;
    }

    .hero-button:hover {
      transform: translateY(-5px);
      background: #d8d8d8;
    }

    /* =========================
       MARQUEE
    ========================= */

    .marquee {
      overflow: hidden;
      white-space: nowrap;
      border-top: 1px solid #222;
      border-bottom: 1px solid #222;

      padding: 17px 0;
      background: #000;
    }

    .marquee-track {
      display: inline-block;
      animation: marquee 18s linear infinite;
    }

    .marquee span {
      margin-right: 50px;
      font-size: 12px;
      font-weight: 700;
      letter-spacing: 4px;
    }

    @keyframes marquee {
      from {
        transform: translateX(0);
      }
      to {
        transform: translateX(-50%);
      }
    }

    /* =========================
       PRODUCTS
    ========================= */

    .shop {
      padding: 120px 5%;
      max-width: 1500px;
      margin: auto;
    }

    .section-title {
      display: flex;
      justify-content: space-between;
      align-items: end;
      margin-bottom: 45px;
    }

    .section-title h2 {
      font-size: clamp(35px, 6vw, 75px);
      letter-spacing: -4px;
      line-height: .9;
    }

    .section-title p {
      max-width: 300px;
      font-size: 12px;
      line-height: 1.7;
      opacity: .45;
    }

    .filters {
      display: flex;
      gap: 10px;
      margin-bottom: 35px;
      flex-wrap: wrap;
    }

    .filter {
      background: transparent;
      color: white;
      border: 1px solid #333;
      padding: 10px 18px;
      border-radius: 50px;
      cursor: pointer;
      font-size: 11px;
      text-transform: uppercase;
      letter-spacing: 1px;
      transition: .3s;
    }

    .filter:hover,
    .filter.active {
      background: white;
      color: black;
    }

    .products {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 18px;
    }

    .product {
      background: #111;
      position: relative;
      cursor: pointer;
      overflow: hidden;
    }

    .product-image {
      aspect-ratio: 4 / 5;
      display: flex;
      align-items: center;
      justify-content: center;
      position: relative;
      overflow: hidden;
    }

    .product-image::after {
      content: "";
      position: absolute;
      inset: 0;
      background: linear-gradient(
        to top,
        rgba(0,0,0,.3),
        transparent 50%
      );
    }

    .shirt {
      width: 63%;
      height: 70%;
      background: #eee;

      clip-path: polygon(
        20% 0,
        35% 8%,
        50% 12%,
        65% 8%,
        80% 0,
        100% 25%,
        83% 37%,
        76% 29%,
        76% 100%,
        24% 100%,
        24% 29%,
        17% 37%,
        0 25%
      );

      display: flex;
      align-items: center;
      justify-content: center;

      transition: transform .5s;
    }

    .product:hover .shirt {
      transform: scale(1.08) rotate(-2deg);
    }

    .shirt.black {
      background: #050505;
      border: 1px solid #222;
    }

    .shirt.cream {
      background: #d7d0c2;
    }

    .shirt.green {
      background: #30382d;
    }

    .shirt.brown {
      background: #4a372d;
    }

    .shirt.blue {
      background: #172535;
    }

    .shirt-logo {
      font-size: 26px;
      font-weight: 900;
      letter-spacing: -3px;
    }

    .shirt.black .shirt-logo,
    .shirt.green .shirt-logo,
    .shirt.brown .shirt-logo,
    .shirt.blue .shirt-logo {
      color: white;
    }

    .product-info {
      padding: 17px;
      background: #101010;
    }

    .product-info h3 {
      font-size: 13px;
      margin-bottom: 7px;
    }

    .product-info p {
      font-size: 11px;
      opacity: .45;
    }

    .price {
      margin-top: 13px;
      font-weight: 700;
      font-size: 13px;
    }

    .tag {
      position: absolute;
      top: 15px;
      left: 15px;
      z-index: 5;

      background: white;
      color: black;

      padding: 7px 10px;

      font-size: 9px;
      font-weight: 800;
      letter-spacing: 1px;
    }

    /* =========================
       BRAND
    ========================= */

    .brand {
      min-height: 75vh;

      display: flex;
      align-items: center;
      justify-content: center;

      text-align: center;

      padding: 100px 20px;

      background: #f1f1ed;
      color: #080808;
    }

    .brand-inner {
      max-width: 900px;
    }

    .brand-logo {
      font-size: clamp(80px, 15vw, 200px);
      font-weight: 900;
      letter-spacing: -12px;
      line-height: .7;
    }

    .brand h2 {
      margin-top: 55px;
      font-size: clamp(25px, 4vw, 55px);
      letter-spacing: -2px;
    }

    .brand p {
      max-width: 520px;
      margin: 25px auto 0;
      font-size: 13px;
      line-height: 1.8;
      opacity: .6;
    }

    /* =========================
       LOOKBOOK
    ========================= */

    .lookbook {
      padding: 120px 5%;
      max-width: 1500px;
      margin: auto;
    }

    .lookbook-grid {
      display: grid;
      grid-template-columns: 1.5fr 1fr 1fr;
      gap: 15px;
    }

    .look {
      min-height: 420px;
      background:
        linear-gradient(
          135deg,
          #151515,
          #303030
        );

      display: flex;
      align-items: end;
      padding: 25px;

      position: relative;
      overflow: hidden;
    }

    .look:nth-child(2) {
      min-height: 600px;
      background: linear-gradient(145deg,#302f2c,#111);
    }

    .look:nth-child(3) {
      background: linear-gradient(145deg,#273028,#101010);
    }

    .look::before {
      content: "SNG";
      position: absolute;
      font-size: 150px;
      font-weight: 900;
      opacity: .06;
      transform: rotate(-10deg);
    }

    .look-content {
      position: relative;
      z-index: 2;
    }

    .look-content small {
      font-size: 9px;
      letter-spacing: 3px;
      opacity: .5;
    }

    .look-content h3 {
      margin-top: 8px;
      font-size: 24px;
    }

    /* =========================
       NEWSLETTER
    ========================= */

    .newsletter {
      padding: 120px 20px;
      text-align: center;
      background: #111;
    }

    .newsletter h2 {
      font-size: clamp(35px, 7vw, 80px);
      letter-spacing: -5px;
    }

    .newsletter p {
      margin: 20px auto 30px;
      opacity: .5;
      font-size: 12px;
    }

    .email-box {
      display: flex;
      max-width: 500px;
      margin: auto;
    }

    .email-box input {
      flex: 1;
      background: #181818;
      border: 1px solid #333;
      color: white;
      padding: 16px;
      outline: none;
    }

    .email-box button {
      background: white;
      color: black;
      border: none;
      padding: 0 25px;
      font-weight: 800;
      cursor: pointer;
    }

    /* =========================
       FOOTER
    ========================= */

    footer {
      padding: 60px 5%;
      border-top: 1px solid #222;

      display: flex;
      justify-content: space-between;
      gap: 30px;
      flex-wrap: wrap;
    }

    footer strong {
      font-size: 20px;
    }

    footer p {
      font-size: 11px;
      opacity: .4;
      margin-top: 8px;
    }

    .footer-links {
      display: flex;
      gap: 25px;
    }

    .footer-links a {
      color: white;
      text-decoration: none;
      font-size: 11px;
      opacity: .5;
    }

    /* =========================
       CART
    ========================= */

    .cart {
      position: fixed;
      top: 0;
      right: -420px;

      width: min(420px, 100%);
      height: 100vh;

      background: #111;
      z-index: 2000;

      padding: 30px;

      transition: .4s;

      border-left: 1px solid #333;
    }

    .cart.open {
      right: 0;
    }

    .cart-header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 40px;
    }

    .close-cart {
      background: none;
      border: none;
      color: white;
      font-size: 25px;
      cursor: pointer;
    }

    #cartItems {
      max-height: 60vh;
      overflow-y: auto;
    }

    .cart-item {
      display: flex;
      justify-content: space-between;
      border-bottom: 1px solid #292929;
      padding: 15px 0;
      font-size: 12px;
    }

    .cart-total {
      margin-top: 30px;
      display: flex;
      justify-content: space-between;
      font-weight: 800;
    }

    .checkout {
      width: 100%;
      margin-top: 25px;
      padding: 17px;

      background: white;
      border: none;
      color: black;

      font-weight: 900;
      cursor: pointer;
    }

    /* =========================
       MODAL
    ========================= */

    .modal {
      position: fixed;
      inset: 0;
      background: rgba(0,0,0,.8);
      backdrop-filter: blur(12px);

      display: none;
      align-items: center;
      justify-content: center;

      z-index: 1500;
      padding: 20px;
    }

    .modal.show {
      display: flex;
    }

    .modal-box {
      background: #111;
      max-width: 800px;
      width: 100%;

      display: grid;
      grid-template-columns: 1fr 1fr;

      border: 1px solid #333;
    }

    .modal-product {
      min-height: 500px;
      display: flex;
      justify-content: center;
      align-items: center;
      background: #171717;
    }

    .modal-info {
      padding: 40px;
    }

    .modal-info h2 {
      font-size: 35px;
      margin-bottom: 15px;
    }

    .modal-info p {
      font-size: 12px;
      line-height: 1.8;
      opacity: .55;
    }

    .sizes {
      display: flex;
      gap: 8px;
      margin: 25px 0;
    }

    .size {
      width: 45px;
      height: 40px;

      background: transparent;
      border: 1px solid #333;
      color: white;

      cursor: pointer;
    }

    .size.selected {
      background: white;
      color: black;
    }

    .add {
      width: 100%;
      padding: 16px;

      background: white;
      color: black;

      border: none;
      font-weight: 900;

      cursor: pointer;
    }

    .modal-close {
      position: absolute;
      top: 25px;
      right: 30px;

      background: none;
      border: none;
      color: white;
      font-size: 30px;
      cursor: pointer;
    }

    /* =========================
       RESPONSIVE
    ========================= */

    @media(max-width: 900px) {

      .nav-links {
        display: none;
      }

      .products {
        grid-template-columns: repeat(2,1fr);
      }

      .lookbook-grid {
        grid-template-columns: 1fr;
      }

      .look:nth-child(2) {
        min-height: 420px;
      }

      .modal-box {
        grid-template-columns: 1fr;
        max-height: 90vh;
        overflow-y: auto;
      }

      .modal-product {
        min-height: 300px;
      }

    }

    @media(max-width: 500px) {

      .products {
        grid-template-columns: 1fr;
      }

      .hero h1 {
        letter-spacing: -5px;
      }

      .hero-slogan {
        letter-spacing: 4px;
        font-size: 11px;
      }

      .email-box {
        flex-direction: column;
        gap: 8px;
      }

      .email-box button {
        padding: 15px;
      }

    }

  </style>
</head>

<body>

<!-- =========================
     NAV
========================= -->

<nav>

  <div class="logo">
    SNG<span>®</span>
  </div>

  <ul class="nav-links">
    <li><a href="#shop">Shop</a></li>
    <li><a href="#lookbook">Lookbook</a></li>
    <li><a href="#brand">About</a></li>
  </ul>

  <button class="cart-button" onclick="openCart()">
    BAG <span id="cartCount">0</span>
  </button>

</nav>


<!-- =========================
     HERO
========================= -->

<section class="hero">

  <div class="hero-content">

    <div class="hero-small">
      SNG STREETWEAR
    </div>

    <h1>SNG</h1>

    <div class="hero-slogan">
      GOD STAYS NEAR
    </div>

    <a href="#shop" class="hero-button">
      SHOP COLLECTION
    </a>

  </div>

</section>


<!-- =========================
     MARQUEE
========================= -->

<div class="marquee">

  <div class="marquee-track">

    <span>SNG</span>
    <span>GOD STAYS NEAR</span>
    <span>NEW DROP</span>
    <span>SNG STREETWEAR</span>
    <span>GOD STAYS NEAR</span>
    <span>NEW DROP</span>

    <span>SNG</span>
    <span>GOD STAYS NEAR</span>
    <span>NEW DROP</span>
    <span>SNG STREETWEAR</span>
    <span>GOD STAYS NEAR</span>
    <span>NEW DROP</span>

  </div>

</div>


<!-- =========================
     SHOP
========================= -->

<section class="shop" id="shop">

  <div class="section-title">

    <div>
      <div style="font-size:10px;opacity:.4;letter-spacing:3px;margin-bottom:15px;">
        COLLECTION 01
      </div>

      <h2>THE<br>DROP.</h2>
    </div>

    <p>
      Designed for those who move differently.
      Minimal pieces. Strong identity.
    </p>

  </div>


  <div class="filters">

    <button class="filter active" onclick="filterProducts('all',this)">
      All
    </button>

    <button class="filter" onclick="filterProducts('shirts',this)">
      T-Shirts
    </button>

    <button class="filter" onclick="filterProducts('hoodies',this)">
      Hoodies
    </button>

    <button class="filter" onclick="filterProducts('pants',this)">
      Pants
    </button>

    <button class="filter" onclick="filterProducts('caps',this)">
      Caps
    </button>

  </div>


  <div class="products">


    <!-- PRODUCT 1 -->

    <article class="product" data-category="shirts"
      onclick="openProduct('SNG Essential Tee',29.99,'white')">

      <div class="product-image">

        <span class="tag">NEW</span>

        <div class="shirt">
          <div class="shirt-logo">SNG</div>
        </div>

      </div>

      <div class="product-info">

        <h3>SNG Essential Tee</h3>

        <p>White / Cotton</p>

        <div class="price">29,99 €</div>

      </div>

    </article>


    <!-- PRODUCT 2 -->

    <article class="product" data-category="shirts"
      onclick="openProduct('SNG Blackout Tee',29.99,'black')">

      <div class="product-image">

        <div class="shirt black">
          <div class="shirt-logo">SNG</div>
        </div>

      </div>

      <div class="product-info">

        <h3>SNG Blackout Tee</h3>

        <p>Black / Heavy Cotton</p>

        <div class="price">29,99 €</div>

      </div>

    </article>


    <!-- PRODUCT 3 -->

    <article class="product" data-category="shirts"
      onclick="openProduct('SNG Olive Tee',34.99,'green')">

      <div class="product-image">

        <span class="tag">DROP</span>

        <div class="shirt green">
          <div class="shirt-logo">SNG</div>
        </div>

      </div>

      <div class="product-info">

        <h3>SNG Olive Tee</h3>

        <p>Olive / Oversized</p>

        <div class="price">34,99 €</div>

      </div>

    </article>


    <!-- PRODUCT 4 -->

    <article class="product" data-category="hoodies"
      onclick="openProduct('GOD STAYS NEAR Hoodie',59.99,'black')">

      <div class="product-image">

        <span class="tag">BESTSELLER</span>

        <div class="shirt black" style="height:75%;width:70%;">
          <div class="shirt-logo">SNG</div>
        </div>

      </div>

      <div class="product-info">

        <h3>GOD STAYS NEAR Hoodie</h3>

        <p>Black / Oversized</p>

        <div class="price">59,99 €</div>

      </div>

    </article>


    <!-- PRODUCT 5 -->

    <article class="product" data-category="hoodies"
      onclick="openProduct('SNG Brown Hoodie',59.99,'brown')">

      <div class="product-image">

        <div class="shirt brown" style="height:75%;width:70%;">
          <div class="shirt-logo">SNG</div>
        </div>

      </div>

      <div class="product-info">

        <h3>SNG Brown Hoodie</h3>

        <p>Brown / Heavyweight</p>

        <div class="price">59,99 €</div>

      </div>

    </article>


    <!-- PRODUCT 6 -->

    <article class="product" data-category="pants"
      onclick="openProduct('SNG Cargo Pants',64.99,'black')">

      <div class="product-image">

        <div class="shirt black"
             style="height:75%;width:48%;clip-path:none;border-radius:10px;">
          <div class="shirt-logo">SNG</div>
        </div>

      </div>

      <div class="product-info">

        <h3>SNG Cargo Pants</h3>

        <p>Black / Utility</p>

        <div class="price">64,99 €</div>

      </div>

    </article>


    <!-- PRODUCT 7 -->

    <article class="product" data-category="pants"
      onclick="openProduct('SNG Summer Shorts',39.99,'blue')">

      <div class="product-image">

        <div class="shirt blue"
             style="height:45%;width:65%;clip-path:none;border-radius:8px;">
          <div class="shirt-logo">SNG</div>
        </div>

      </div>

      <div class="product-info">

        <h3>SNG Summer Shorts</h3>

        <p>Navy / Relaxed</p>

        <div class="price">39,99 €</div>

      </div>

    </article>


    <!-- PRODUCT 8 -->

    <article class="product" data-category="caps"
      onclick="openProduct('SNG Signature Cap',24.99,'black')">

      <div class="product-image">

        <div style="
          width:65%;
          height:35%;
          background:#050505;
          border-radius:80px 80px 15px 15px;
          display:flex;
          align-items:center;
          justify-content:center;
          font-weight:900;
          font-size:28px;
        ">
          SNG
        </div>

      </div>

      <div class="product-info">

        <h3>SNG Signature Cap</h3>

        <p>Black / Embroidered</p>

        <div class="price">24,99 €</div>

      </div>

    </article>

  </div>

</section>


<!-- =========================
     BRAND
========================= -->

<section class="brand" id="brand">

  <div class="brand-inner">

    <div class="brand-logo">
      SNG
    </div>

    <h2>
      GOD STAYS NEAR.
    </h2>

    <p>
      SNG is more than clothing.
      It's a reminder to stay close to what matters.
      Clean silhouettes, strong details and a message
      that goes beyond the clothes.
    </p>

  </div>

</section>


<!-- =========================
     LOOKBOOK
========================= -->

<section class="lookbook" id="lookbook">

  <div class="section-title">

    <div>
      <div style="font-size:10px;opacity:.4;letter-spacing:3px;margin-bottom:15px;">
        SNG WORLD
      </div>

      <h2>LOOK<br>BOOK.</h2>
    </div>

  </div>


  <div class="lookbook-grid">

    <div class="look">

      <div class="look-content">

        <small>SNG / 001</small>

        <h3>STAY<br>NEAR.</h3>

      </div>

    </div>


    <div class="look">

      <div class="look-content">

        <small>SNG / 002</small>

        <h3>MOVE<br>DIFFERENT.</h3>

      </div>

    </div>


    <div class="look">

      <div class="look-content">

        <small>SNG / 003</small>

        <h3>GOD<br>STAYS NEAR.</h3>

      </div>

    </div>

  </div>

</section>


<!-- =========================
     NEWSLETTER
========================= -->

<section class="newsletter">

  <h2>STAY NEAR.</h2>

  <p>
    Be the first to know about new drops.
  </p>

  <form class="email-box"
        onsubmit="subscribe(event)">

    <input
      type="email"
      placeholder="YOUR EMAIL"
      required
    >

    <button>
      JOIN SNG
    </button>

  </form>

</section>


<!-- =========================
     FOOTER
========================= -->

<footer>

  <div>

    <strong>SNG®</strong>

    <p>
      GOD STAYS NEAR.
    </p>

  </div>

  <div class="footer-links">

    <a href="#">Instagram</a>
    <a href="#">TikTok</a>
    <a href="#">Contact</a>

  </div>

</footer>


<!-- =========================
     CART
========================= -->

<aside class="cart" id="cart">

  <div class="cart-header">

    <h2>YOUR BAG</h2>

    <button
      class="close-cart"
      onclick="closeCart()">
      ×
    </button>

  </div>


  <div id="cartItems">

    <p style="opacity:.4;font-size:12px;">
      Your bag is empty.
    </p>

  </div>


  <div class="cart-total">

    <span>TOTAL</span>

    <span id="cartTotal">
      0,00 €
    </span>

  </div>


  <button class="checkout"
          onclick="checkout()">

    CHECKOUT

  </button>

</aside>


<!-- =========================
     PRODUCT MODAL
========================= -->

<div class="modal" id="modal">

  <button
    class="modal-close"
    onclick="closeProduct()">
    ×
  </button>


  <div class="modal-box">

    <div class="modal-product">

      <div id="modalShirt"
           class="shirt"
           style="width:65%;height:70%;">

        <div class="shirt-logo">
          SNG
        </div>

      </div>

    </div>


    <div class="modal-info">

      <h2 id="modalName">
        SNG
      </h2>

      <h3 id="modalPrice">
        29,99 €
      </h3>

      <p style="margin-top:20px;">
        SNG streetwear.
        Designed with a minimal identity and
        the message GOD STAYS NEAR.
      </p>


      <div class="sizes">

        <button class="size"
          onclick="selectSize(this)">
          XS
        </button>

        <button class="size"
          onclick="selectSize(this)">
          S
        </button>

        <button class="size"
          onclick="selectSize(this)">
          M
        </button>

        <button class="size"
          onclick="selectSize(this)">
          L
        </button>

        <button class="size"
          onclick="selectSize(this)">
          XL
        </button>

      </div>


      <button
        class="add"
        onclick="addToCart()">

        ADD TO BAG

      </button>

    </div>

  </div>

</div>


<script>

  /* =========================
     CART
  ========================= */

  let cart = [];

  let currentProduct = null;

  let selectedSize = "M";


  function openCart() {

    document
      .getElementById("cart")
      .classList.add("open");

  }


  function closeCart() {

    document
      .getElementById("cart")
      .classList.remove("open");

  }


  function updateCart() {

    const container =
      document.getElementById("cartItems");

    const count =
      document.getElementById("cartCount");

    const total =
      document.getElementById("cartTotal");


    count.innerText = cart.length;


    if(cart.length === 0){

      container.innerHTML =
        `<p style="opacity:.4;font-size:12px;">
          Your bag is empty.
        </p>`;

      total.innerText = "0,00 €";

      return;

    }


    let totalPrice = 0;


    container.innerHTML = cart.map((item,index)=>{

      totalPrice += item.price;

      return `
        <div class="cart-item">

          <div>

            <strong>
              ${item.name}
            </strong>

            <br>

            <span style="opacity:.4">
              Size ${item.size}
            </span>

          </div>

          <div>

            ${item.price.toFixed(2)} €

            <button
              onclick="removeItem(${index})"
              style="
                background:none;
                border:none;
                color:#777;
                cursor:pointer;
                margin-left:10px;
              ">
              ×
            </button>

          </div>

        </div>
      `;

    }).join("");


    total.innerText =
      totalPrice.toFixed(2).replace(".",",") + " €";

  }


  function removeItem(index){

    cart.splice(index,1);

    updateCart();

  }


  /* =========================
     PRODUCT MODAL
  ========================= */

  function openProduct(name,price,color){

    currentProduct = {
      name:name,
      price:price,
      color:color
    };


    document
      .getElementById("modalName")
      .innerText = name;


    document
      .getElementById("modalPrice")
      .innerText =
      price.toFixed(2).replace(".",",") + " €";


    const shirt =
      document.getElementById("modalShirt");


    shirt.className =
      "shirt " + color;


    document
      .getElementById("modal")
      .classList.add("show");

  }


  function closeProduct(){

    document
      .getElementById("modal")
      .classList.remove("show");

  }


  function selectSize(button){

    document
      .querySelectorAll(".size")
      .forEach(b =>
        b.classList.remove("selected")
      );


    button.classList.add("selected");

    selectedSize =
      button.innerText;

  }


  function addToCart(){

    if(!currentProduct) return;


    cart.push({

      name: currentProduct.name,

      price: currentProduct.price,

      size: selectedSize

    });


    updateCart();

    closeProduct();

    openCart();

  }


  /* =========================
     FILTERS
  ========================= */

  function filterProducts(category,button){

    document
      .querySelectorAll(".filter")
      .forEach(b =>
        b.classList.remove("active")
      );


    button.classList.add("active");


    document
      .querySelectorAll(".product")
      .forEach(product => {

        if(
          category === "all" ||
          product.dataset.category === category
        ){

          product.style.display = "";

        }else{

          product.style.display = "none";

        }

      });

  }


  /* =========================
     CHECKOUT
  ========================= */

  function checkout(){

    if(cart.length === 0){

      alert("Tu carrito está vacío.");

      return;

    }


    alert(
      "Aquí conectaríamos tu sistema de pago."
    );

  }


  /* =========================
     NEWSLETTER
  ========================= */

  function subscribe(event){

    event.preventDefault();

    alert(
      "¡Bienvenido a SNG! GOD STAYS NEAR."
    );

  }


  /* =========================
     ESCAPE
  ========================= */

  document.addEventListener(
    "keydown",
    function(event){

      if(event.key === "Escape"){

        closeProduct();

        closeCart();

      }

    }
  );


  updateCart();

</script>

</body>
</html>
