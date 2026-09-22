<!DOCTYPE html>
<html lang="ca">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>SNG — GOD STAYS NEAR</title>

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
    font-family:Arial,Helvetica,sans-serif;
    background:#fff;
    color:#000;
}

a{
    text-decoration:none;
    color:inherit;
}

button{
    cursor:pointer;
}

header{
    position:sticky;
    top:0;
    z-index:1000;
    background:#fff;
    border-bottom:1px solid #ddd;
}

.navbar{
    max-width:1200px;
    margin:auto;
    height:75px;
    display:flex;
    align-items:center;
    justify-content:space-between;
    padding:0 25px;
}

.logo{
    display:flex;
    align-items:center;
    gap:12px;
    font-weight:900;
    font-size:25px;
    letter-spacing:4px;
}

.logo img{
    width:50px;
    height:50px;
    object-fit:contain;
}

nav{
    display:flex;
    gap:30px;
}

nav a{
    font-size:13px;
    font-weight:bold;
    transition:.2s;
}

nav a:hover{
    opacity:.5;
}

.cart-button{
    background:#000;
    color:#fff;
    border:0;
    padding:12px 18px;
    font-weight:bold;
}

.hero{
    min-height:650px;
    background:#000;
    color:#fff;
    display:grid;
    grid-template-columns:1fr 1fr;
    align-items:center;
    padding:70px 8%;
    gap:50px;
}

.hero-text small{
    border:1px solid #fff;
    padding:9px 14px;
    font-weight:bold;
    letter-spacing:2px;
}

.hero h1{
    font-size:clamp(80px,12vw,150px);
    line-height:.8;
    margin-top:30px;
    letter-spacing:-8px;
}

.hero h2{
    font-size:35px;
    letter-spacing:4px;
    margin-top:30px;
}

.hero p{
    max-width:500px;
    margin-top:20px;
    color:#ccc;
    line-height:1.7;
}

.buttons{
    margin-top:30px;
    display:flex;
    gap:12px;
}

.btn{
    padding:15px 25px;
    border:1px solid #000;
    font-weight:bold;
    font-size:12px;
    display:inline-block;
}

.btn-white{
    background:#fff;
    color:#000;
}

.btn-black{
    background:#000;
    color:#fff;
}

.hero-logo{
    display:flex;
    justify-content:center;
}

.hero-logo img{
    width:min(480px,90%);
    background:#fff;
    padding:15px;
}

section{
    padding:90px 7%;
}

.section-title{
    text-align:center;
    margin-bottom:45px;
}

.section-title small{
    font-weight:bold;
    letter-spacing:2px;
}

.section-title h2{
    font-size:60px;
    margin-top:10px;
}

.categories{
    max-width:1200px;
    margin:auto;
    display:grid;
    grid-template-columns:repeat(4,1fr);
    gap:15px;
}

.category{
    height:200px;
    border:1px solid #ddd;
    background:#f5f5f5;
    padding:25px;
    display:flex;
    flex-direction:column;
    justify-content:space-between;
    transition:.25s;
}

.category:hover{
    background:#000;
    color:#fff;
}

.category span{
    font-size:12px;
    font-weight:bold;
}

.category h3{
    font-size:25px;
}

.filters{
    max-width:1200px;
    margin:0 auto 30px;
    display:flex;
    gap:8px;
    flex-wrap:wrap;
}

.filter{
    padding:11px 18px;
    border:1px solid #000;
    background:#fff;
    font-weight:bold;
}

.filter.active,
.filter:hover{
    background:#000;
    color:#fff;
}

.products{
    max-width:1200px;
    margin:auto;
    display:grid;
    grid-template-columns:repeat(4,1fr);
    gap:20px;
}

.product{
    border:1px solid #ddd;
    background:#fff;
    overflow:hidden;
}

.product-image{
    height:300px;
    background:#f1f1f1;
    display:flex;
    align-items:center;
    justify-content:center;
}

.product-image img{
    width:75%;
    height:75%;
    object-fit:contain;
}

.product-info{
    padding:20px;
}

.product-info small{
    color:#777;
    font-weight:bold;
}

.product-info h3{
    margin-top:5px;
    font-size:19px;
}

.product-info p{
    color:#777;
    font-size:13px;
    margin-top:7px;
}

.product-bottom{
    display:flex;
    justify-content:space-between;
    align-items:center;
    margin-top:20px;
}

.price{
    font-weight:bold;
}

.add{
    border:0;
    background:#000;
    color:#fff;
    padding:10px 15px;
    font-size:11px;
    font-weight:bold;
}

.about{
    background:#000;
    color:#fff;
    display:grid;
    grid-template-columns:1fr 1fr;
    min-height:500px;
    padding:0;
}

.about-image{
    display:flex;
    justify-content:center;
    align-items:center;
    padding:60px;
}

.about-image img{
    max-width:450px;
    width:100%;
    background:#fff;
    padding:15px;
}

.about-text{
    background:#f3f3f3;
    color:#000;
    padding:70px;
    display:flex;
    flex-direction:column;
    justify-content:center;
}

.about-text h2{
    font-size:65px;
    line-height:.9;
}

.about-text p{
    margin-top:25px;
    max-width:500px;
    color:#555;
    line-height:1.7;
}

.about-list{
    margin:25px 0;
}

.about-list div{
    padding:12px 0;
    border-top:1px solid #ccc;
    font-weight:bold;
    font-size:12px;
}

.values{
    background:#000;
    color:#fff;
}

.values-grid{
    max-width:1200px;
    margin:auto;
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:15px;
}

.value{
    border:1px solid #333;
    padding:35px;
}

.value span{
    color:#777;
    font-weight:bold;
}

.value h3{
    margin-top:45px;
    font-size:28px;
}

.value p{
    color:#aaa;
    margin-top:10px;
}

.promo{
    background:#000;
    color:#fff;
    text-align:center;
}

.promo h2{
    font-size:70px;
}

.promo p{
    color:#aaa;
    margin:15px auto 30px;
}

.newsletter{
    background:#f4f4f4;
    text-align:center;
}

.newsletter h2{
    font-size:40px;
}

.newsletter p{
    color:#777;
    margin:12px 0 25px;
}

.newsletter form{
    max-width:600px;
    margin:auto;
    display:flex;
}

.newsletter input{
    flex:1;
    border:1px solid #000;
    padding:15px;
}

.newsletter button{
    background:#000;
    color:#fff;
    border:1px solid #000;
    padding:0 25px;
    font-weight:bold;
}

footer{
    background:#000;
    color:#fff;
    padding:60px 7% 25px;
}

.footer-grid{
    max-width:1200px;
    margin:auto;
    display:grid;
    grid-template-columns:2fr 1fr 1fr 1fr;
    gap:40px;
}

.footer-brand h2{
    font-size:45px;
}

.footer-brand p{
    color:#888;
    max-width:300px;
    margin-top:15px;
}

.footer-column h3{
    font-size:12px;
    margin-bottom:15px;
}

.footer-column a{
    display:block;
    color:#aaa;
    margin:9px 0;
    font-size:13px;
}

.footer-column a:hover{
    color:#fff;
}

.footer-bottom{
    max-width:1200px;
    margin:45px auto 0;
    padding-top:20px;
    border-top:1px solid #333;
    display:flex;
    justify-content:space-between;
    color:#777;
    font-size:11px;
}

.cart{
    position:fixed;
    right:-450px;
    top:0;
    width:430px;
    max-width:100%;
    height:100vh;
    background:#fff;
    z-index:3000;
    box-shadow:-10px 0 40px rgba(0,0,0,.2);
    transition:.3s;
    display:flex;
    flex-direction:column;
}

.cart.open{
    right:0;
}

.cart-header{
    padding:25px;
    border-bottom:1px solid #ddd;
    display:flex;
    justify-content:space-between;
}

.cart-header button{
    background:#fff;
    border:1px solid #000;
    width:35px;
    height:35px;
}

.cart-items{
    flex:1;
    overflow:auto;
    padding:20px;
}

.empty{
    text-align:center;
    color:#777;
    margin-top:60px;
}

.cart-item{
    display:grid;
    grid-template-columns:70px 1fr auto;
    gap:12px;
    padding:15px 0;
    border-bottom:1px solid #ddd;
}

.cart-item img{
    width:70px;
    height:70px;
    object-fit:contain;
    background:#eee;
}

.cart-item h4{
    font-size:14px;
}

.cart-item p{
    color:#777;
    font-size:12px;
}

.quantity{
    display:flex;
    gap:5px;
    margin-top:8px;
}

.quantity button{
    width:25px;
    height:25px;
    border:1px solid #ccc;
    background:#fff;
}

.cart-footer{
    border-top:1px solid #ddd;
    padding:20px;
}

.total{
    display:flex;
    justify-content:space-between;
    font-size:20px;
    font-weight:bold;
    margin-bottom:15px;
}

.checkout{
    width:100%;
    background:#000;
    color:#fff;
    border:0;
    padding:16px;
    font-weight:bold;
}

.toast{
    position:fixed;
    bottom:25px;
    left:50%;
    transform:translateX(-50%);
    background:#000;
    color:#fff;
    padding:14px 22px;
    opacity:0;
    pointer-events:none;
    transition:.3s;
    z-index:5000;
}

.toast.show{
    opacity:1;
}

@media(max-width:900px){

    nav{
        display:none;
    }

    .hero{
        grid-template-columns:1fr;
        text-align:center;
    }

    .hero p{
        margin-left:auto;
        margin-right:auto;
    }

    .buttons{
        justify-content:center;
    }

    .categories{
        grid-template-columns:repeat(2,1fr);
    }

    .products{
        grid-template-columns:repeat(2,1fr);
    }

    .about{
        grid-template-columns:1fr;
    }

    .values-grid{
        grid-template-columns:1fr;
    }

    .footer-grid{
        grid-template-columns:repeat(2,1fr);
    }
}

@media(max-width:600px){

    .hero h1{
        font-size:80px;
    }

    .hero h2{
        font-size:25px;
    }

    .categories,
    .products{
        grid-template-columns:1fr;
    }

    .section-title h2{
        font-size:45px;
    }

    .about-text{
        padding:45px 25px;
    }

    .about-text h2{
        font-size:50px;
    }

    .promo h2{
        font-size:45px;
    }

    .newsletter form{
        flex-direction:column;
        gap:8px;
    }

    .newsletter button{
        padding:15px;
    }

    .footer-grid{
        grid-template-columns:1fr;
    }

    .footer-bottom{
        display:block;
    }
}
</style>
</head>

<body>

<header>
<div class="navbar">

<a href="#inicio" class="logo">
<img src="MERCHANS.png" alt="SNG">
<span>SNG</span>
</a>

<nav>
<a href="#inicio">INICI</a>
<a href="#categories">CATEGORIES</a>
<a href="#catalog">CATÀLEG</a>
<a href="#nosaltres">NOSALTRES</a>
<a href="#contacte">CONTACTE</a>
</nav>

<button class="cart-button" onclick="openCart()">
CARRET (<span id="cartCount">0</span>)
</button>

</div>
</header>

<section class="hero" id="inicio">

<div class="hero-text">

<small>NOVA COL·LECCIÓ · 2026</small>

<h1>SNG</h1>

<h2>GOD STAYS NEAR</h2>

<p>
Roba urbana amb un estil simple, modern i diferent.
Una marca creada per expressar-te i portar una identitat pròpia.
</p>

<div class="buttons">

<a href="#catalog" class="btn btn-white">
VEURE CATÀLEG
</a>

<a href="#nosaltres" class="btn btn-black">
SABER MÉS
</a>

</div>

</div>

<div class="hero-logo">

<img src="MERCHANS.png" alt="Logo oficial SNG">

</div>

</section>

<section id="categories">

<div class="section-title">

<small>EXPLORA</small>

<h2>CATEGORIES</h2>

</div>

<div class="categories">

<a href="#catalog" class="category" onclick="filterProducts('samarretes')">
<span>01</span>
<h3>SAMARRETES</h3>
<span>VEURE →</span>
</a>

<a href="#catalog" class="category" onclick="filterProducts('dessuadores')">
<span>02</span>
<h3>DESSUADORES</h3>
<span>VEURE →</span>
</a>

<a href="#catalog" class="category" onclick="filterProducts('gorres')">
<span>03</span>
<h3>GORRES</h3>
<span>VEURE →</span>
</a>

<a href="#catalog" class="category" onclick="filterProducts('bosses')">
<span>04</span>
<h3>BOSSES</h3>
<span>VEURE →</span>
</a>

</div>

</section>

<section id="catalog">

<div class="section-title">

<small>SNG SHOP</small>

<h2>CATÀLEG</h2>

</div>

<div class="filters">

<button class="filter active" onclick="filterProducts('tots')">
TOTS
</button>

<button class="filter" onclick="filterProducts('samarretes')">
SAMARRETES
</button>

<button class="filter" onclick="filterProducts('dessuadores')">
DESSUADORES
</button>

<button class="filter" onclick="filterProducts('gorres')">
GORRES
</button>

<button class="filter" onclick="filterProducts('bosses')">
BOSSES
</button>

</div>

<div class="products" id="products">

<div class="product" data-category="samarretes">

<div class="product-image">
<img src="MERCHANS.png" alt="Samarreta Classic">
</div>

<div class="product-info">

<small>SNG ESSENTIAL</small>

<h3>Samarreta Classic</h3>

<p>Samarreta negra amb el logo SNG.</p>

<div class="product-bottom">

<span class="price">20 €</span>

<button class="add" onclick="addToCart(1)">
AFEGIR
</button>

</div>

</div>

</div>

<div class="product" data-category="samarretes">

<div class="product-image">
<img src="MERCHANS.png" alt="Samarreta Logo">
</div>

<div class="product-info">

<small>SNG LOGO</small>

<h3>Samarreta Logo</h3>

<p>Disseny frontal amb el logo.</p>

<div class="product-bottom">

<span class="price">22 €</span>

<button class="add" onclick="addToCart(2)">
AFEGIR
</button>

</div>

</div>

</div>

<div class="product" data-category="dessuadores">

<div class="product-image">
<img src="MERCHANS.png" alt="Dessuadora Original">
</div>

<div class="product-info">

<small>SNG HEAVY</small>

<h3>Dessuadora Original</h3>

<p>Dessuadora còmoda per cada dia.</p>

<div class="product-bottom">

<span class="price">40 €</span>

<button class="add" onclick="addToCart(3)">
AFEGIR
</button>

</div>

</div>

</div>

<div class="product" data-category="dessuadores">

<div class="product-image">
<img src="MERCHANS.png" alt="Dessuadora God Stays Near">
</div>

<div class="product-info">

<small>LIMITED</small>

<h3>God Stays Near</h3>

<p>La peça principal de la col·lecció.</p>

<div class="product-bottom">

<span class="price">45 €</span>

<button class="add" onclick="addToCart(4)">
AFEGIR
</button>

</div>

</div>

</div>

<div class="product" data-category="gorres">

<div class="product-image">
<img src="MERCHANS.png" alt="Gorra SNG">
</div>

<div class="product-info">

<small>ACCESSORI</small>

<h3>Gorra SNG</h3>

<p>Gorra negra amb el logo.</p>

<div class="product-bottom">

<span class="price">18 €</span>

<button class="add" onclick="addToCart(5)">
AFEGIR
</button>

</div>

</div>

</div>

<div class="product" data-category="gorres">

<div class="product-image">
<img src="MERCHANS.png" alt="Gorra GSN">
</div>

<div class="product-info">

<small>ACCESSORI</small>

<h3>Gorra GSN</h3>

<p>Model especial de la marca.</p>

<div class="product-bottom">

<span class="price">20 €</span>

<button class="add" onclick="addToCart(6)">
AFEGIR
</button>

</div>

</div>

</div>

<div class="product" data-category="bosses">

<div class="product-image">
<img src="MERCHANS.png" alt="Bossa SNG">
</div>

<div class="product-info">

<small>ACCESSORI</small>

<h3>Bossa SNG</h3>

<p>Bossa de roba per al dia a dia.</p>

<div class="product-bottom">

<span class="price">12 €</span>

<button class="add" onclick="addToCart(7)">
AFEGIR
</button>

</div>

</div>

</div>

<div class="product" data-category="bosses">

<div class="product-image">
<img src="MERCHANS.png" alt="Bossa GSN">
</div>

<div class="product-info">

<small>LIMITED</small>

<h3>Bossa GSN</h3>

<p>Edició especial amb el lema.</p>

<div class="product-bottom">

<span class="price">15 €</span>

<button class="add" onclick="addToCart(8)">
AFEGIR
</button>

</div>

</div>

</div>

</div>

</section>

<section class="about" id="nosaltres">

<div class="about-image">

<img src="MERCHANS.png" alt="Logo SNG">

</div>

<div class="about-text">

<h2>GOD<br>STAYS<br>NEAR.</h2>

<p>
SNG és una marca creada per tres creadors:
Sergio, Nil i Gorka. La nostra idea és crear roba
urbana amb un disseny simple i fàcil de reconèixer.
</p>

<div class="about-list">

<div>01 — DISSENYS SIMPLES</div>

<div>02 — ESTIL URBÀ</div>

<div>03 — PREUS ASSEQUIBLES</div>

<div>04 — COL·LECCIONS LIMITADES</div>

</div>

<a href="#catalog" class="btn btn-black">
VEURE PRODUCTES
</a>

</div>

</section>

<section class="values">

<div class="section-title">

<small>LA NOSTRA IDENTITAT</small>

<h2>EL NOSTRE ESTIL</h2>

</div>

<div class="values-grid">

<div class="value">

<span>01</span>

<h3>SIMPLE</h3>

<p>
Dissenys fàcils de combinar i fàcils de recordar.
</p>

</div>

<div class="value">

<span>02</span>

<h3>URBÀ</h3>

<p>
Una estètica pensada per al dia a dia.
</p>

</div>

<div class="value">

<span>03</span>

<h3>DIFERENT</h3>

<p>
Volem crear una identitat pròpia i reconeixible.
</p>

</div>

</div>

</section>

<section class="promo">

<h2>10% DE DESCOMPTE</h2>

<p>
Oferta especial pel llançament de SNG.
</p>

<a href="#catalog" class="btn btn-white">
COMPRAR ARA
</a>

</section>

<section class="newsletter" id="contacte">

<h2>UNEIX-TE A SNG</h2>

<p>
Rep les novetats de la marca i les pròximes col·leccions.
</p>

<form onsubmit="subscribe(event)">

<input
type="email"
id="email"
placeholder="El teu correu electrònic"
required
>

<button type="submit">
SUBSCRIURE'M
</button>

</form>

</section>

<footer>

<div class="footer-grid">

<div class="footer-brand">

<h2>SNG</h2>

<p>
God Stays Near. Roba urbana creada per Sergio,
Nil i Gorka.
</p>

</div>

<div class="footer-column">

<h3>BOTIGA</h3>

<a href="#catalog">Catàleg</a>

<a href="#catalog">Samarretes</a>

<a href="#catalog">Dessuadores</a>

<a href="#catalog">Gorres</a>

<a href="#catalog">Bosses</a>

</div>

<div class="footer-column">

<h3>SNG</h3>

<a href="#nosaltres">Nosaltres</a>

<a href="#categories">Categories</a>

<a href="#contacte">Contacte</a>

</div>

<div class="footer-column">

<h3>XARXES</h3>

<a href="#">Instagram</a>

<a href="#">TikTok</a>

<a href="#">YouTube</a>

</div>

</div>

<div class="footer-bottom">

<span>© 2026 SNG</span>

<span>GOD STAYS NEAR</span>

</div>

</footer>

<div class="cart" id="cart">

<div class="cart-header">

<h2>EL TEU CARRET</h2>

<button onclick="closeCart()">✕</button>

</div>

<div class="cart-items" id="cartItems">

<div class="empty">
El teu carret està buit.
</div>

</div>

<div class="cart-footer">

<div class="total">

<span>TOTAL</span>

<span id="total">0 €</span>

</div>

<button class="checkout" onclick="checkout()">
FINALITZAR COMPRA
</button>

</div>

</div>

<div class="toast" id="toast">
Producte afegit al carret.
</div>

<script>

const products = {

1:{
name:"Samarreta Classic",
price:20,
image:"MERCHANS.png"
},

2:{
name:"Samarreta Logo",
price:22,
image:"MERCHANS.png"
},

3:{
name:"Dessuadora Original",
price:40,
image:"MERCHANS.png"
},

4:{
name:"Dessuadora God Stays Near",
price:45,
image:"MERCHANS.png"
},

5:{
name:"Gorra SNG",
price:18,
image:"MERCHANS.png"
},

6:{
name:"Gorra GSN",
price:20,
image:"MERCHANS.png"
},

7:{
name:"Bossa SNG",
price:12,
image:"MERCHANS.png"
},

8:{
name:"Bossa GSN",
price:15,
image:"MERCHANS.png"
}

};

let cart=[];

function addToCart(id){

let item=cart.find(
product=>product.id===id
);

if(item){

item.quantity++;

}else{

cart.push({
id:id,
quantity:1
});

}

renderCart();

showToast("Producte afegit al carret.");

}

function renderCart(){

const container=
document.getElementById("cartItems");

const count=
document.getElementById("cartCount");

const total=
document.getElementById("total");

let number=0;

let price=0;

cart.forEach(item=>{

number+=item.quantity;

price+=
products[item.id].price*
item.quantity;

});

count.textContent=number;

total.textContent=
price.toFixed(2)+" €";

if(cart.length===0){

container.innerHTML=
'<div class="empty">El teu carret està buit.</div>';

return;

}

container.innerHTML="";

cart.forEach(item=>{

const product=
products[item.id];

const element=
document.createElement("div");

element.className="cart-item";

element.innerHTML=`

<img
src="${product.image}"
alt="${product.name}"
>

<div>

<h4>${product.name}</h4>

<p>${product.price} €</p>

<div class="quantity">

<button
onclick="changeQuantity(${item.id},-1)"
>
−
</button>

<span>${item.quantity}</span>

<button
onclick="changeQuantity(${item.id},1)"
>
+
</button>

</div>

</div>

<strong>
${product.price*item.quantity} €
</strong>

`;

container.appendChild(element);

});

}

function changeQuantity(id,change){

const item=
cart.find(
product=>product.id===id
);

if(!item){
return;
}

item.quantity+=change;

if(item.quantity<=0){

cart=
cart.filter(
product=>product.id!==id
);

}

renderCart();

}

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

function filterProducts(category){

const products=
document.querySelectorAll(".product");

const buttons=
document.querySelectorAll(".filter");

buttons.forEach(
button=>button.classList.remove("active")
);

products.forEach(product=>{

if(
category==="tots"||
product.dataset.category===category
){

product.style.display="block";

}else{

product.style.display="none";

}

});

}

function showToast(message){

const toast=
document.getElementById("toast");

toast.textContent=message;

toast.classList.add("show");

setTimeout(
()=>{
toast.classList.remove("show");
},
2000
);

}

function subscribe(event){

event.preventDefault();

document.getElementById("email").value="";

showToast(
"T'has inscrit correctament a SNG."
);

}

function checkout(){

if(cart.length===0){

showToast(
"El carret està buit."
);

return;

}

showToast(
"Compra de demostració preparada."
);

}

renderCart();

</script>

</body>
</html>
