<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>SNG — GOD STAYS NEAR</title>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800;900&display=swap" rel="stylesheet">

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

html{
    scroll-behavior:smooth;
}

body{
    font-family:Inter,sans-serif;
    background:#fff;
    color:#080808;
    overflow-x:hidden;
}

button{
    font-family:inherit;
    cursor:pointer;
}

/* NAV */

nav{
    position:fixed;
    top:0;
    left:0;
    width:100%;
    height:75px;

    display:flex;
    align-items:center;
    justify-content:space-between;

    padding:0 5%;

    background:rgba(255,255,255,.85);
    backdrop-filter:blur(18px);

    border-bottom:1px solid #e8e8e8;

    z-index:1000;
}

.logo{
    font-size:25px;
    font-weight:900;
    letter-spacing:-2px;
}

.logo span{
    opacity:.3;
}

.nav-links{
    display:flex;
    gap:35px;
    list-style:none;
}

.nav-links a{
    text-decoration:none;
    color:#080808;
    font-size:11px;
    font-weight:700;
    letter-spacing:2px;
}

.nav-links a:hover{
    opacity:.4;
}

.cart-button{
    background:#080808;
    color:white;
    border:0;
    padding:11px 18px;
    border-radius:30px;
    font-size:11px;
    font-weight:700;
}

/* HERO */

.hero{
    min-height:100vh;

    display:flex;
    align-items:center;
    justify-content:center;

    position:relative;
    overflow:hidden;

    background:#fff;
}

.hero-logo{
    position:absolute;

    width:min(700px,85vw);
    height:min(700px,85vw);

    background-image:url("images/logo.png");
    background-size:contain;
    background-position:center;
    background-repeat:no-repeat;

    opacity:.055;

    pointer-events:none;
}

.hero-content{
    position:relative;
    z-index:2;

    text-align:center;

    max-width:850px;
    padding:40px;
}

.hero-small{
    font-size:10px;
    letter-spacing:7px;
    font-weight:700;

    margin-bottom:35px;

    opacity:.45;
}

.hero h1{
    font-size:clamp(55px,9vw,125px);

    line-height:.9;
    letter-spacing:-6px;

    font-weight:900;
}

.hero-description{
    max-width:570px;

    margin:35px auto 0;

    font-size:13px;
    line-height:1.9;

    color:#555;
}

.hero-button{
    margin-top:40px;

    padding:17px 32px;

    border:1px solid #111;

    background:#080808;
    color:white;

    font-size:11px;
    font-weight:800;

    letter-spacing:2px;

    transition:.35s;
}

.hero-button:hover{
    background:white;
    color:#080808;

    transform:translateY(-4px);
}

/* MARQUEE */

.marquee{
    overflow:hidden;

    white-space:nowrap;

    border-top:1px solid #e5e5e5;
    border-bottom:1px solid #e5e5e5;

    padding:15px 0;
}

.marquee-track{
    display:inline-block;

    animation:marquee 18s linear infinite;
}

.marquee span{
    margin-right:60px;

    font-size:10px;
    font-weight:800;

    letter-spacing:4px;
}

@keyframes marquee{
    0%{
        transform:translateX(0);
    }

    100%{
        transform:translateX(-50%);
    }
}

/* ABOUT */

.about{
    padding:140px 7%;

    background:#f7f7f5;
}

.about-container{
    max-width:1200px;

    margin:auto;

    display:grid;

    grid-template-columns:1fr 1fr;

    gap:100px;

    align-items:center;
}

.about-label{
    font-size:10px;

    font-weight:800;

    letter-spacing:4px;

    opacity:.4;

    margin-bottom:20px;
}

.about h2{
    font-size:clamp(45px,6vw,80px);

    line-height:.9;

    letter-spacing:-5px;
}

.about-text{
    font-size:14px;

    line-height:2;

    color:#555;
}

.about-text p{
    margin-bottom:20px;
}

.about-box{
    margin-top:30px;

    display:grid;

    grid-template-columns:repeat(3,1fr);

    border-top:1px solid #ddd;
    border-bottom:1px solid #ddd;
}

.about-stat{
    padding:25px 10px;

    border-right:1px solid #ddd;
}

.about-stat:last-child{
    border-right:0;
}

.about-stat strong{
    font-size:25px;
    display:block;
}

.about-stat span{
    font-size:9px;
    letter-spacing:1px;
    opacity:.45;
}

/* LOOKBOOK */

.lookbook-section{
    padding:120px 7%;

    display:grid;

    grid-template-columns:.8fr 1.2fr;

    gap:70px;

    align-items:center;

    background:#fff;
}

.lookbook-copy h2{
    font-size:clamp(45px,6vw,82px);

    line-height:.9;

    letter-spacing:-5px;
}

.lookbook-copy p{
    margin-top:28px;

    max-width:420px;

    font-size:13px;

    line-height:1.9;

    color:#666;
}

.lookbook-section img{
    width:100%;

    display:block;

    transition:.5s;
}

.lookbook-section img:hover{
    transform:scale(.99);
}

/* COLLECTION */

.collection-intro{
    display:none;

    padding:130px 7% 70px;

    text-align:center;
}

.collection-intro.visible{
    display:block;
}

.collection-intro h2{
    font-size:clamp(45px,7vw,90px);

    letter-spacing:-5px;
}

.collection-intro p{
    margin:20px auto;

    max-width:500px;

    font-size:12px;

    line-height:1.8;

    color:#666;
}

/* SHOP */

.shop{
    display:none;

    padding:30px 7% 130px;

    max-width:1500px;

    margin:auto;
}

.shop.visible{
    display:block;
}

.filters{
    display:flex;

    gap:10px;

    margin-bottom:40px;

    flex-wrap:wrap;
}

.filter{
    padding:10px 18px;

    background:white;

    border:1px solid #ddd;

    border-radius:50px;

    font-size:10px;

    font-weight:700;

    letter-spacing:1px;

    transition:.3s;
}

.filter:hover,
.filter.active{
    background:#080808;

    color:white;

    border-color:#080808;
}

/* PRODUCTS */

.products{
    display:grid;

    grid-template-columns:repeat(4,1fr);

    gap:20px;
}

.product{
    background:#f5f5f3;

    overflow:hidden;

    transition:.4s;

    cursor:pointer;
}

.product:hover{
    transform:translateY(-8px);
}

.product-image{
    aspect-ratio:4/5;

    position:relative;

    overflow:hidden;

    background:#f1f1ef;
}

.product-image img{
    width:100%;
    height:100%;

    object-fit:cover;

    display:block;

    transition:.5s;
}

.product:hover .product-image img{
    transform:scale(1.04);
}

.tag{
    position:absolute;

    top:15px;
    left:15px;

    background:#080808;

    color:white;

    padding:7px 10px;

    font-size:8px;

    font-weight:800;

    z-index:3;
}

.product-info{
    padding:18px;

    background:white;
}

.product-info h3{
    font-size:13px;

    margin-bottom:7px;
}

.product-info p{
    font-size:10px;

    color:#777;
}

.price{
    margin-top:12px;

    font-size:12px;

    font-weight:800;
}

/* MANIFESTO */

.manifesto{
    padding:160px 20px;

    text-align:center;

    background:#080808;

    color:white;
}

.manifesto-small{
    font-size:9px;

    letter-spacing:5px;

    opacity:.4;
}

.manifesto h2{
    font-size:clamp(45px,8vw,120px);

    letter-spacing:-7px;

    margin-top:25px;
}

.manifesto p{
    max-width:550px;

    margin:35px auto 0;

    font-size:13px;

    line-height:2;

    color:#aaa;
}

/* NEWSLETTER */

.newsletter{
    padding:130px 20px;

    text-align:center;
}

.newsletter h2{
    font-size:clamp(40px,7vw,90px);

    letter-spacing:-6px;
}

.newsletter p{
    margin:20px 0 30px;

    font-size:12px;

    color:#777;
}

.email-box{
    display:flex;

    max-width:500px;

    margin:auto;
}

.email-box input{
    flex:1;

    padding:16px;

    border:1px solid #ddd;

    outline:none;

    font-size:11px;
}

.email-box button{
    background:#080808;

    color:white;

    border:0;

    padding:0 25px;

    font-size:10px;

    font-weight:800;
}

/* FOOTER */

footer{
    padding:60px 7%;

    border-top:1px solid #e5e5e5;

    display:flex;

    justify-content:space-between;

    flex-wrap:wrap;

    gap:30px;
}

footer strong{
    font-size:20px;
}

footer p{
    font-size:10px;

    color:#777;

    margin-top:7px;
}

.footer-links{
    display:flex;

    gap:25px;
}

.footer-links a{
    color:#080808;

    text-decoration:none;

    font-size:10px;

    font-weight:600;
}

/* CART */

.cart{
    position:fixed;

    top:0;
    right:-420px;

    width:min(420px,100%);

    height:100vh;

    background:white;

    z-index:3000;

    padding:30px;

    transition:.4s;

    box-shadow:-10px 0 40px rgba(0,0,0,.12);
}

.cart.open{
    right:0;
}

.cart-header{
    display:flex;

    justify-content:space-between;

    align-items:center;

    margin-bottom:40px;
}

.cart-header h2{
    font-size:20px;
}

.close-cart{
    background:none;

    border:0;

    font-size:25px;
}

.cart-item{
    display:flex;

    justify-content:space-between;

    padding:16px 0;

    border-bottom:1px solid #eee;

    font-size:11px;
}

.cart-total{
    display:flex;

    justify-content:space-between;

    margin-top:30px;

    font-weight:800;
}

.checkout{
    width:100%;

    margin-top:25px;

    padding:17px;

    background:#080808;

    color:white;

    border:0;

    font-weight:800;
}

/* MODAL */

.modal{
    position:fixed;

    inset:0;

    background:rgba(255,255,255,.88);

    backdrop-filter:blur(15px);

    display:none;

    align-items:center;

    justify-content:center;

    z-index:2500;

    padding:20px;
}

.modal.show{
    display:flex;
}

.modal-box{
    background:white;

    width:850px;

    max-width:100%;

    display:grid;

    grid-template-columns:1fr 1fr;

    box-shadow:0 20px 70px rgba(0,0,0,.15);
}

.modal-product{
    min-height:500px;

    display:flex;

    align-items:center;

    justify-content:center;

    background:#f4f4f2;

    overflow:hidden;
}

.modal-product img{
    width:100%;
    height:100%;

    object-fit:cover;
}

.modal-info{
    padding:50px;
}

.modal-info h2{
    font-size:30px;

    letter-spacing:-2px;
}

.modal-info h3{
    margin-top:12px;
}

.modal-info p{
    margin-top:25px;

    font-size:12px;

    line-height:1.8;

    color:#666;
}

.sizes{
    display:flex;

    gap:8px;

    margin:25px 0;
}

.size{
    width:43px;

    height:40px;

    background:white;

    border:1px solid #ddd;
}

.size.selected{
    background:#080808;

    color:white;

    border-color:#080808;
}

.add{
    width:100%;

    padding:17px;

    background:#080808;

    color:white;

    border:0;

    font-weight:800;
}

/* RESPONSIVE */

@media(max-width:900px){

    .nav-links{
        display:none;
    }

    .lookbook-section{
        grid-template-columns:1fr;

        gap:45px;
    }

    .about-container{
        grid-template-columns:1fr;

        gap:50px;
    }

    .products{
        grid-template-columns:repeat(2,1fr);
    }

    .modal-box{
        grid-template-columns:1fr;

        max-height:90vh;

        overflow-y:auto;
    }

    .modal-product{
        min-height:300px;
    }
}

@media(max-width:500px){

    .products{
        grid-template-columns:1fr;
    }

    .hero h1{
        letter-spacing:-4px;
    }

    .about-box{
        grid-template-columns:1fr;
    }

    .about-stat{
        border-right:0;

        border-bottom:1px solid #ddd;
    }

    .email-box{
        flex-direction:column;

        gap:8px;
    }

    .email-box button{
        padding:16px;
    }
}
</style>
</head>

<body>

<!-- NAV -->

<nav>

<div class="logo">
SNG<span>®</span>
</div>

<ul class="nav-links">

<li>
<a href="#about">ABOUT</a>
</li>

<li>
<a href="#collection">COLLECTION</a>
</li>

<li>
<a href="#manifesto">MESSAGE</a>
</li>

</ul>

<button class="cart-button" onclick="openCart()">
BAG <span id="cartCount">0</span>
</button>

</nav>


<!-- HERO -->

<section class="hero">

<div class="hero-logo"></div>

<div class="hero-content">

<div class="hero-small">
SNG STREETWEAR
</div>

<h1>
GOD<br>
STAYS<br>
NEAR
</h1>

<p class="hero-description">

A clothing brand built around identity,
simplicity and a message that stays with you.

Every piece carries the SNG identity.

</p>

<button
class="hero-button"
onclick="showCollection()">

EXPLORE COLLECTION

</button>

</div>

</section>


<!-- MARQUEE -->

<div class="marquee">

<div class="marquee-track">

<span>SNG</span>
<span>GOD STAYS NEAR</span>
<span>STAY CLOSE</span>
<span>SNG STREETWEAR</span>
<span>GOD STAYS NEAR</span>
<span>MOVE DIFFERENT</span>

<span>SNG</span>
<span>GOD STAYS NEAR</span>
<span>STAY CLOSE</span>
<span>SNG STREETWEAR</span>
<span>GOD STAYS NEAR</span>
<span>MOVE DIFFERENT</span>

</div>

</div>


<!-- ABOUT -->

<section class="about" id="about">

<div class="about-container">

<div>

<div class="about-label">
WHO WE ARE
</div>

<h2>
MORE THAN<br>
CLOTHING.
</h2>

</div>

<div class="about-text">

<p>

SNG is an independent streetwear concept
built around one simple message:

<strong>GOD STAYS NEAR.</strong>

</p>

<p>

Our goal is to create clothing that feels
clean, modern and different while keeping
a strong identity behind every piece.

</p>

<p>

From everyday T-shirts to hoodies,
pants, shorts and accessories,
every collection is designed to carry
the SNG identity.

</p>

<div class="about-box">

<div class="about-stat">
<strong>01</strong>
<span>IDENTITY</span>
</div>

<div class="about-stat">
<strong>02</strong>
<span>DESIGN</span>
</div>

<div class="about-stat">
<strong>03</strong>
<span>MESSAGE</span>
</div>

</div>

</div>

</div>

</section>


<!-- LOOKBOOK -->

<section class="lookbook-section">

<div class="lookbook-copy">

<div class="about-label">
SNG COLLECTION
</div>

<h2>
BUILT TO<br>
BE WORN.
</h2>

<p>

Every piece is part of the same message.
Clean silhouettes, strong graphics and
the SNG identity.

<strong>GOD STAYS NEAR.</strong>

</p>

</div>

<img
src="images/lookbook.jpg"
alt="SNG Collection Lookbook">

</section>


<!-- COLLECTION -->

<section
class="collection-intro"
id="collection">

<div class="about-label">
SNG COLLECTION 01
</div>

<h2>
THE DROP.
</h2>

<p>

Explore the SNG collection.

T-shirts, hoodies, pants,
shorts and accessories.

</p>

</section>


<!-- SHOP -->

<section class="shop">

<div class="filters">

<button
class="filter active"
onclick="filterProducts('all',this)">
ALL
</button>

<button
class="filter"
onclick="filterProducts('shirts',this)">
T-SHIRTS
</button>

<button
class="filter"
onclick="filterProducts('hoodies',this)">
HOODIES
</button>

<button
class="filter"
onclick="filterProducts('pants',this)">
PANTS
</button>

<button
class="filter"
onclick="filterProducts('shorts',this)">
SHORTS
</button>

<button
class="filter"
onclick="filterProducts('caps',this)">
CAPS
</button>

</div>


<div class="products">


<!-- T-SHIRTS -->

<article
class="product"
data-category="shirts"
onclick="openProduct(
'SNG White Tee',
29.99,
'images/tee-white.jpg'
)">

<div class="product-image">

<span class="tag">
NEW
</span>

<img
src="images/tee-white.jpg"
alt="SNG White Tee">

</div>

<div class="product-info">

<h3>SNG White Tee</h3>

<p>White / SNG Graphic</p>

<div class="price">
29,99 €
</div>

</div>

</article>


<article
class="product"
data-category="shirts"
onclick="openProduct(
'SNG Black Tee',
29.99,
'images/tee-black.jpg'
)">

<div class="product-image">

<img
src="images/tee-black.jpg"
alt="SNG Black Tee">

</div>

<div class="product-info">

<h3>SNG Black Tee</h3>

<p>Black / SNG Graphic</p>

<div class="price">
29,99 €
</div>

</div>

</article>


<article
class="product"
data-category="shirts"
onclick="openProduct(
'SNG Olive Tee',
34.99,
'images/tee-green.jpg'
)">

<div class="product-image">

<img
src="images/tee-green.jpg"
alt="SNG Olive Tee">

</div>

<div class="product-info">

<h3>SNG Olive Tee</h3>

<p>Olive / Oversized</p>

<div class="price">
34,99 €
</div>

</div>

</article>


<article
class="product"
data-category="shirts"
onclick="openProduct(
'SNG Cream Tee',
34.99,
'images/tee-cream.jpg'
)">

<div class="product-image">

<img
src="images/tee-cream.jpg"
alt="SNG Cream Tee">

</div>

<div class="product-info">

<h3>SNG Cream Tee</h3>

<p>Cream / God Stays Near</p>

<div class="price">
34,99 €
</div>

</div>

</article>


<!-- HOODIES -->

<article
class="product"
data-category="hoodies"
onclick="openProduct(
'SNG Black Hoodie',
64.99,
'images/hoodie-black.jpg'
)">

<div class="product-image">

<span class="tag">
BESTSELLER
</span>

<img
src="images/hoodie-black.jpg"
alt="SNG Black Hoodie">

</div>

<div class="product-info">

<h3>SNG Black Hoodie</h3>

<p>Black / Oversized</p>

<div class="price">
64,99 €
</div>

</div>

</article>


<article
class="product"
data-category="hoodies"
onclick="openProduct(
'SNG Grey Hoodie',
64.99,
'images/hoodie-grey.jpg'
)">

<div class="product-image">

<img
src="images/hoodie-grey.jpg"
alt="SNG Grey Hoodie">

</div>

<div class="product-info">

<h3>SNG Grey Hoodie</h3>

<p>Grey / Oversized</p>

<div class="price">
64,99 €
</div>

</div>

</article>


<article
class="product"
data-category="hoodies"
onclick="openProduct(
'SNG Brown Hoodie',
64.99,
'images/hoodie-brown.jpg'
)">

<div class="product-image">

<img
src="images/hoodie-brown.jpg"
alt="SNG Brown Hoodie">

</div>

<div class="product-info">

<h3>SNG Brown Hoodie</h3>

<p>Brown / Heavyweight</p>

<div class="price">
64,99 €
</div>

</div>

</article>


<article
class="product"
data-category="hoodies"
onclick="openProduct(
'God Stays Near Hoodie',
64.99,
'images/hoodie-cream.jpg'
)">

<div class="product-image">

<img
src="images/hoodie-cream.jpg"
alt="God Stays Near Hoodie">

</div>

<div class="product-info">

<h3>God Stays Near Hoodie</h3>

<p>Cream / Statement</p>

<div class="price">
64,99 €
</div>

</div>

</article>


<article
class="product"
data-category="hoodies"
onclick="openProduct(
'SNG Prayer Hoodie',
64.99,
'images/hoodie-prayer.jpg'
)">

<div class="product-image">

<img
src="images/hoodie-prayer.jpg"
alt="SNG Prayer Hoodie">

</div>

<div class="product-info">

<h3>SNG Prayer Hoodie</h3>

<p>Black / Prayer Graphic</p>

<div class="price">
64,99 €
</div>

</div>

</article>


<!-- PANTS -->

<article
class="product"
data-category="pants"
onclick="openProduct(
'SNG Black Pants',
64.99,
'images/pants-black.jpg'
)">

<div class="product-image">

<img
src="images/pants-black.jpg"
alt="SNG Black Pants">

</div>

<div class="product-info">

<h3>SNG Black Pants</h3>

<p>Black / Relaxed</p>

<div class="price">
64,99 €
</div>

</div>

</article>


<article
class="product"
data-category="pants"
onclick="openProduct(
'SNG Grey Pants',
64.99,
'images/pants-grey.jpg'
)">

<div class="product-image">

<img
src="images/pants-grey.jpg"
alt="SNG Grey Pants">

</div>

<div class="product-info">

<h3>SNG Grey Pants</h3>

<p>Grey / Relaxed</p>

<div class="price">
64,99 €
</div>

</div>

</article>


<article
class="product"
data-category="pants"
onclick="openProduct(
'SNG Cargo Green',
69.99,
'images/cargo-green.jpg'
)">

<div class="product-image">

<img
src="images/cargo-green.jpg"
alt="SNG Cargo Green">

</div>

<div class="product-info">

<h3>SNG Cargo Green</h3>

<p>Olive / Utility</p>

<div class="price">
69,99 €
</div>

</div>

</article>


<article
class="product"
data-category="pants"
onclick="openProduct(
'SNG Cargo Black',
69.99,
'images/cargo-black.jpg'
)">

<div class="product-image">

<img
src="images/cargo-black.jpg"
alt="SNG Cargo Black">

</div>

<div class="product-info">

<h3>SNG Cargo Black</h3>

<p>Black / Utility</p>

<div class="price">
69,99 €
</div>

</div>

</article>


<!-- SHORTS -->

<article
class="product"
data-category="shorts"
onclick="openProduct(
'SNG Black Shorts',
39.99,
'images/shorts-black.jpg'
)">

<div class="product-image">

<img
src="images/shorts-black.jpg"
alt="SNG Black Shorts">

</div>

<div class="product-info">

<h3>SNG Black Shorts</h3>

<p>Black / Relaxed</p>

<div class="price">
39,99 €
</div>

</div>

</article>


<article
class="product"
data-category="shorts"
onclick="openProduct(
'SNG Grey Shorts',
39.99,
'images/shorts-grey.jpg'
)">

<div class="product-image">

<img
src="images/shorts-grey.jpg"
alt="SNG Grey Shorts">

</div>

<div class="product-info">

<h3>SNG Grey Shorts</h3>

<p>Grey / Relaxed</p>

<div class="price">
39,99 €
</div>

</div>

</article>


<article
class="product"
data-category="shorts"
onclick="openProduct(
'SNG Olive Shorts',
39.99,
'images/shorts-green.jpg'
)">

<div class="product-image">

<img
src="images/shorts-green.jpg"
alt="SNG Olive Shorts">

</div>

<div class="product-info">

<h3>SNG Olive Shorts</h3>

<p>Olive / Relaxed</p>

<div class="price">
39,99 €
</div>

</div>

</article>


<article
class="product"
data-category="shorts"
onclick="openProduct(
'SNG Cream Shorts',
39.99,
'images/shorts-cream.jpg'
)">

<div class="product-image">

<img
src="images/shorts-cream.jpg"
alt="SNG Cream Shorts">

</div>

<div class="product-info">

<h3>SNG Cream Shorts</h3>

<p>Cream / Relaxed</p>

<div class="price">
39,99 €
</div>

</div>

</article>


<!-- CAPS -->

<article
class="product"
data-category="caps"
onclick="openProduct(
'SNG Signature Cap',
24.99,
'images/cap-black.jpg'
)">

<div class="product-image">

<span class="tag">
ACCESSORY
</span>

<img
src="images/cap-black.jpg"
alt="SNG Black Cap">

</div>

<div class="product-info">

<h3>SNG Signature Cap</h3>

<p>Black / Embroidered</p>

<div class="price">
24,99 €
</div>

</div>

</article>


<article
class="product"
data-category="caps"
onclick="openProduct(
'SNG Cream Cap',
24.99,
'images/cap-cream.jpg'
)">

<div class="product-image">

<img
src="images/cap-cream.jpg"
alt="SNG Cream Cap">

</div>

<div class="product-info">

<h3>SNG Cream Cap</h3>

<p>Cream / Embroidered</p>

<div class="price">
24,99 €
</div>

</div>

</article>


<article
class="product"
data-category="caps"
onclick="openProduct(
'SNG Olive Cap',
24.99,
'images/cap-green.jpg'
)">

<div class="product-image">

<img
src="images/cap-green.jpg"
alt="SNG Olive Cap">

</div>

<div class="product-info">

<h3>SNG Olive Cap</h3>

<p>Olive / Embroidered</p>

<div class="price">
24,99 €
</div>

</div>

</article>


<article
class="product"
data-category="caps"
onclick="openProduct(
'SNG Navy Cap',
24.99,
'images/cap-navy.jpg'
)">

<div class="product-image">

<img
src="images/cap-navy.jpg"
alt="SNG Navy Cap">

</div>

<div class="product-info">

<h3>SNG Navy Cap</h3>

<p>Navy / Embroidered</p>

<div class="price">
24,99 €
</div>

</div>

</article>


<article
class="product"
data-category="caps"
onclick="openProduct(
'SNG Charcoal Cap',
24.99,
'images/cap-charcoal.jpg'
)">

<div class="product-image">

<img
src="images/cap-charcoal.jpg"
alt="SNG Charcoal Cap">

</div>

<div class="product-info">

<h3>SNG Charcoal Cap</h3>

<p>Charcoal / Embroidered</p>

<div class="price">
24,99 €
</div>

</div>

</article>


<article
class="product"
data-category="caps"
onclick="openProduct(
'SNG Brown Cap',
24.99,
'images/cap-brown.jpg'
)">

<div class="product-image">

<img
src="images/cap-brown.jpg"
alt="SNG Brown Cap">

</div>

<div class="product-info">

<h3>SNG Brown Cap</h3>

<p>Brown / Embroidered</p>

<div class="price">
24,99 €
</div>

</div>

</article>

</div>

</section>


<!-- MANIFESTO -->

<section class="manifesto" id="manifesto">

<div class="manifesto-small">
THE SNG MESSAGE
</div>

<h2>
GOD STAYS NEAR.
</h2>

<p>

SNG represents a reminder to stay close
to what matters.

No matter where you go,
what you wear or what comes next,

<strong>GOD STAYS NEAR.</strong>

</p>

</section>


<!-- NEWSLETTER -->

<section class="newsletter">

<h2>
STAY NEAR.
</h2>

<p>
Join the SNG community and discover new drops first.
</p>

<form
class="email-box"
onsubmit="subscribe(event)">

<input
type="email"
placeholder="YOUR EMAIL"
required>

<button>
JOIN SNG
</button>

</form>

</section>


<!-- FOOTER -->

<footer>

<div>

<strong>SNG®</strong>

<p>
GOD STAYS NEAR.
</p>

</div>

<div class="footer-links">

<a href="#">
Instagram
</a>

<a href="#">
TikTok
</a>

<a href="#">
Contact
</a>

</div>

</footer>


<!-- CART -->

<aside
class="cart"
id="cart">

<div class="cart-header">

<h2>
YOUR BAG
</h2>

<button
class="close-cart"
onclick="closeCart()">
×
</button>

</div>

<div id="cartItems">

<p style="color:#777;font-size:12px;">
Your bag is empty.
</p>

</div>

<div class="cart-total">

<span>
TOTAL
</span>

<span id="cartTotal">
0,00 €
</span>

</div>

<button
class="checkout"
onclick="checkout()">

CHECKOUT

</button>

</aside>


<!-- PRODUCT MODAL -->

<div
class="modal"
id="modal">

<div class="modal-box">

<div class="modal-product">

<img
id="modalImage"
src=""
alt="SNG Product">

</div>

<div class="modal-info">

<h2 id="modalName">
SNG
</h2>

<h3 id="modalPrice">
29,99 €
</h3>

<p>

A piece from the SNG collection.

Designed around the message

<strong>GOD STAYS NEAR.</strong>

</p>

<div class="sizes">

<button
class="size"
onclick="selectSize(this)">
XS
</button>

<button
class="size"
onclick="selectSize(this)">
S
</button>

<button
class="size selected"
onclick="selectSize(this)">
M
</button>

<button
class="size"
onclick="selectSize(this)">
L
</button>

<button
class="size"
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

let cart=[];

let currentProduct=null;

let selectedSize="M";


/* SHOW COLLECTION */

function showCollection(){

document
.querySelector(".collection-intro")
.classList.add("visible");

document
.querySelector(".shop")
.classList.add("visible");

setTimeout(()=>{

document
.querySelector(".collection-intro")
.scrollIntoView({
behavior:"smooth"
});

},100);

}


/* CART */

function openCart(){

document
.getElementById("cart")
.classList.add("open");

}

function closeCart(){

document
.getElementById("cart")
.classList.remove("open");

}


/* PRODUCT */

function openProduct(name,price,image){

currentProduct={
name:name,
price:price,
image:image
};

document
.getElementById("modalName")
.innerText=name;

document
.getElementById("modalPrice")
.innerText=
price.toFixed(2)
.replace(".",",")+" €";

document
.getElementById("modalImage")
.src=image;

document
.getElementById("modal")
.classList.add("show");

}


function closeProduct(){

document
.getElementById("modal")
.classList.remove("show");

}


/* SIZE */

function selectSize(button){

document
.querySelectorAll(".size")
.forEach(b=>{
b.classList.remove("selected");
});

button.classList.add("selected");

selectedSize=button.innerText;

}


/* ADD TO CART */

function addToCart(){

if(!currentProduct){
return;
}

cart.push({

name:currentProduct.name,

price:currentProduct.price,

size:selectedSize

});

updateCart();

closeProduct();

openCart();

}


/* REMOVE */

function removeItem(index){

cart.splice(index,1);

updateCart();

}


/* UPDATE CART */

function updateCart(){

const items=
document.getElementById("cartItems");

const count=
document.getElementById("cartCount");

const total=
document.getElementById("cartTotal");

count.innerText=cart.length;


if(cart.length===0){

items.innerHTML=`

<p style="color:#777;font-size:12px;">
Your bag is empty.
</p>

`;

total.innerText="0,00 €";

return;

}


let totalPrice=0;


items.innerHTML=
cart.map((item,index)=>{

totalPrice+=item.price;

return `

<div class="cart-item">

<div>

<strong>
${item.name}
</strong>

<br>

<span style="color:#777">
Size ${item.size}
</span>

</div>

<div>

${item.price.toFixed(2)} €

<button
onclick="removeItem(${index})"
style="
border:0;
background:none;
margin-left:8px;
cursor:pointer;
">

×
</button>

</div>

</div>

`;

}).join("");


total.innerText=
totalPrice
.toFixed(2)
.replace(".",",")+" €";

}


/* FILTER */

function filterProducts(category,button){

document
.querySelectorAll(".filter")
.forEach(b=>{
b.classList.remove("active");
});

button.classList.add("active");


document
.querySelectorAll(".product")
.forEach(product=>{

if(
category==="all" ||
product.dataset.category===category
){

product.style.display="";

}else{

product.style.display="none";

}

});

}


/* CHECKOUT */

function checkout(){

if(cart.length===0){

alert("Your bag is empty.");

return;

}

alert(
"Checkout will be connected to your payment system."
);

}


/* NEWSLETTER */

function subscribe(event){

event.preventDefault();

alert(
"Welcome to SNG. GOD STAYS NEAR."
);

}


/* ESC */

document.addEventListener(
"keydown",
event=>{

if(event.key==="Escape"){

closeProduct();

closeCart();

}

});


/* CLICK OUTSIDE MODAL */

document
.getElementById("modal")
.addEventListener("click",e=>{

if(e.target.id==="modal"){

closeProduct();

}

});

</script>

</body>
</html>
