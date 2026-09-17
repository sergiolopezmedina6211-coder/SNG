<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1.0">

<title>SNG — GOD STAYS NEAR</title>

<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800;900&display=swap" rel="stylesheet">

<style>
*{
box-sizing:border-box;
margin:0;
padding:0
}

html{
scroll-behavior:smooth
}

body{
font-family:Inter,Arial,sans-serif;
background:#fff;
color:#080808
}

button,input{
font:inherit
}

button{
cursor:pointer
}

/* =========================
   NAV
========================= */

nav{
position:fixed;
top:0;
left:0;
width:100%;
height:72px;
z-index:50;

display:flex;
align-items:center;
justify-content:space-between;

padding:0 5%;

background:rgba(255,255,255,.88);
backdrop-filter:blur(18px);

border-bottom:1px solid #eee
}

.brand{
font-size:24px;
font-weight:900;
letter-spacing:-2px
}

.brand span{
font-size:9px;
vertical-align:top;
margin-left:2px
}

.navlinks{
display:flex;
gap:28px;
list-style:none
}

.navlinks a{
font-size:10px;
font-weight:800;
letter-spacing:1.5px;
text-decoration:none;
color:#111
}

.navlinks a:hover{
opacity:.45
}

.bag{
border:0;
background:#080808;
color:#fff;
border-radius:999px;
padding:11px 16px;
font-size:10px;
font-weight:800
}


/* =========================
   HERO
========================= */

.hero{
min-height:100vh;

position:relative;

display:grid;
place-items:center;

overflow:hidden;

background:#fff;

text-align:center;

padding:100px 20px 60px
}

/* LOGO GRANDE DETRÁS */

.hero:before{
content:"";

position:absolute;

inset:5%;

background:url('images/logo.png') center/contain no-repeat;

opacity:.12;

filter:grayscale(1);

z-index:0
}

/* LUZ SOBRE EL LOGO */

.hero:after{
content:"";

position:absolute;

inset:0;

background:
radial-gradient(
circle,
transparent 10%,
rgba(255,255,255,.72) 75%
);

z-index:1
}

.hero-content{
position:relative;

z-index:2;

max-width:850px
}

.eyebrow{
font-size:9px;

letter-spacing:6px;

font-weight:800;

opacity:.45;

margin-bottom:24px
}

.hero h1{
font-size:clamp(58px,10vw,128px);

line-height:.86;

letter-spacing:-7px;

font-weight:900
}

.hero p{
max-width:540px;

margin:30px auto 0;

font-size:13px;

line-height:1.8;

color:#555
}

.hero-actions{
display:flex;

gap:10px;

justify-content:center;

margin-top:32px;

flex-wrap:wrap
}

.primary,
.secondary{
padding:15px 24px;

border:1px solid #111;

font-size:10px;

font-weight:800;

letter-spacing:1.5px
}

.primary{
background:#080808;
color:#fff
}

.secondary{
background:#fff;
color:#080808
}

.primary:hover{
transform:translateY(-2px)
}


/* =========================
   MARQUEE
========================= */

.strip{
border-block:1px solid #eee;

overflow:hidden;

white-space:nowrap;

padding:13px 0
}

.strip div{
display:inline-block;

animation:move 22s linear infinite
}

.strip span{
font-size:9px;

font-weight:800;

letter-spacing:4px;

margin:0 35px
}

@keyframes move{

to{
transform:translateX(-50%)
}

}


/* =========================
   CONTAINER
========================= */

.wrap{
max-width:1400px;

margin:auto;

padding:0 5%
}


/* =========================
   QUICK CATEGORIES
========================= */

.quick{
padding:70px 0 25px
}

.quick-head{
display:flex;

align-items:end;

justify-content:space-between;

gap:20px;

margin-bottom:22px
}

.quick h2{
font-size:clamp(35px,5vw,68px);

letter-spacing:-4px;

line-height:.9
}

.quick p{
font-size:11px;

color:#777;

max-width:350px;

line-height:1.7
}

.categories{
display:grid;

grid-template-columns:repeat(5,1fr);

gap:10px
}

.cat{
position:relative;

min-height:125px;

border:1px solid #ddd;

background:#f5f5f3;

display:flex;

align-items:end;

padding:16px;

overflow:hidden;

text-align:left
}

.cat:before{
content:"";

position:absolute;

inset:0;

background:url('images/lookbook.jpg') center/cover;

opacity:.13;

transition:.4s
}

.cat:hover:before{
opacity:.28;

transform:scale(1.04)
}

.cat div{
position:relative;
z-index:2
}

.cat strong{
font-size:12px;

letter-spacing:1px
}

.cat small{
display:block;

font-size:8px;

opacity:.55;

margin-top:5px
}


/* =========================
   SHOP
========================= */

.shop{
padding:55px 0 120px
}

.shopbar{
display:flex;

align-items:center;

justify-content:space-between;

gap:15px;

margin-bottom:25px;

position:sticky;

top:72px;

background:rgba(255,255,255,.92);

backdrop-filter:blur(12px);

padding:14px 0;

z-index:20
}

.filters{
display:flex;

gap:7px;

flex-wrap:wrap
}

.filter{
border:1px solid #ddd;

background:#fff;

border-radius:999px;

padding:9px 14px;

font-size:9px;

font-weight:800;

letter-spacing:.7px
}

.filter.active,
.filter:hover{
background:#080808;

color:#fff;

border-color:#080808
}

.search{
width:190px;

border:1px solid #ddd;

padding:10px 13px;

font-size:10px;

outline:0
}


/* =========================
   PRODUCTS
========================= */

.products{
display:grid;

grid-template-columns:repeat(4,1fr);

gap:18px
}

.product{
cursor:pointer
}

.photo{
aspect-ratio:4/5;

background:#f4f4f2;

overflow:hidden;

position:relative
}

.photo img{
width:100%;

height:100%;

object-fit:cover;

display:block;

transition:.5s
}

.product:hover img{
transform:scale(1.035)
}

.badge{
position:absolute;

left:10px;

top:10px;

background:#080808;

color:#fff;

padding:6px 8px;

font-size:7px;

font-weight:800;

z-index:2
}

.info{
padding:14px 2px
}

.info h3{
font-size:12px
}

.info p{
font-size:9px;

color:#777;

margin-top:5px
}

.price{
font-size:11px;

font-weight:800;

margin-top:9px
}


/* =========================
   STORY
========================= */

.story{
background:#080808;

color:#fff;

padding:130px 0
}

.storygrid{
display:grid;

grid-template-columns:1fr 1fr;

gap:70px;

align-items:center
}

.story h2{
font-size:clamp(42px,6vw,82px);

line-height:.9;

letter-spacing:-5px
}

.story p{
color:#aaa;

font-size:12px;

line-height:2;

max-width:520px
}

.story strong{
color:#fff
}


/* =========================
   LOOKBOOK
========================= */

.look{
padding:110px 0
}

.lookgrid{
display:grid;

grid-template-columns:.8fr 1.2fr;

gap:60px;

align-items:center
}

.look img{
width:100%;

display:block
}

.look h2{
font-size:clamp(42px,6vw,82px);

letter-spacing:-5px;

line-height:.9
}

.look p{
font-size:12px;

color:#666;

line-height:1.9;

margin-top:25px
}


/* =========================
   FOOTER
========================= */

footer{
border-top:1px solid #eee;

padding:50px 5%;

display:flex;

justify-content:space-between;

gap:20px
}

footer strong{
font-size:20px
}

footer p,
footer a{
font-size:9px;

color:#777;

text-decoration:none
}

footer .flinks{
display:flex;

gap:20px
}


/* =========================
   PRODUCT MODAL
========================= */

.overlay{
position:fixed;

inset:0;

background:rgba(255,255,255,.85);

backdrop-filter:blur(14px);

z-index:100;

display:none;

align-items:center;

justify-content:center;

padding:18px
}

.overlay.show{
display:flex
}

.modal{
background:#fff;

max-width:900px;

width:100%;

display:grid;

grid-template-columns:1fr 1fr;

box-shadow:0 20px 70px #0002;

max-height:90vh;

overflow:auto
}

.modalphoto{
background:#f4f4f2
}

.modalphoto img{
width:100%;

height:100%;

min-height:430px;

object-fit:cover
}

.modalinfo{
padding:42px
}

.close{
float:right;

border:0;

background:none;

font-size:24px
}

.modalinfo h2{
font-size:28px;

letter-spacing:-2px;

margin-top:25px
}

.modalinfo .mp{
margin-top:12px;

font-weight:800
}

.modalinfo p{
font-size:11px;

color:#666;

line-height:1.8;

margin-top:20px
}

.sizes{
display:flex;

gap:7px;

margin:24px 0
}

.size{
width:40px;

height:38px;

border:1px solid #ddd;

background:#fff;

font-size:9px
}

.size.sel{
background:#080808;

color:#fff;

border-color:#080808
}

.add{
width:100%;

padding:16px;

background:#080808;

color:#fff;

border:0;

font-size:10px;

font-weight:800;

letter-spacing:1px
}


/* =========================
   CART
========================= */

.cart{
position:fixed;

right:-430px;

top:0;

width:min(430px,100%);

height:100vh;

background:#fff;

z-index:120;

padding:28px;

box-shadow:-20px 0 60px #0001;

transition:.35s
}

.cart.open{
right:0
}

.carthead{
display:flex;

justify-content:space-between
}

.cartitems{
margin-top:30px
}

.ci{
display:flex;

justify-content:space-between;

border-bottom:1px solid #eee;

padding:15px 0;

font-size:10px
}

.total{
display:flex;

justify-content:space-between;

font-weight:800;

margin-top:25px
}

.checkout{
width:100%;

padding:16px;

margin-top:20px;

background:#080808;

color:#fff;

border:0;

font-size:10px;

font-weight:800
}


/* =========================
   MOBILE
========================= */

@media(max-width:900px){

.navlinks{
display:none
}

.categories{
grid-template-columns:repeat(2,1fr)
}

.products{
grid-template-columns:repeat(2,1fr)
}

.storygrid,
.lookgrid{
grid-template-columns:1fr
}

.shopbar{
align-items:flex-start;

flex-direction:column
}

.search{
width:100%
}

}


@media(max-width:520px){

.hero h1{
letter-spacing:-4px
}

.categories{
grid-template-columns:1fr 1fr
}

.products{
grid-template-columns:1fr 1fr;

gap:12px
}

.modal{
grid-template-columns:1fr
}

.modalphoto img{
min-height:280px
}

.modalinfo{
padding:25px
}

.hero:before{
inset:15% 0
}

.quick-head{
display:block
}

.quick p{
margin-top:15px
}

}
</style>
</head>


<body>


<!-- =========================
     NAV
========================= -->

<nav>

<div class="brand">
SNG<span>®</span>
</div>

<ul class="navlinks">

<li>
<a href="#shop">SHOP</a>
</li>

<li>
<a href="#categories">CATEGORIES</a>
</li>

<li>
<a href="#story">ABOUT</a>
</li>

</ul>

<button class="bag" onclick="openCart()">
BAG (<span id="count">0</span>)
</button>

</nav>


<!-- =========================
     HERO
========================= -->

<section class="hero">

<div class="hero-content">

<div class="eyebrow">
SNG STREETWEAR · COLLECTION 01
</div>

<h1>
GOD<br>
STAYS<br>
NEAR
</h1>

<p>
Streetwear con identidad.
Diseños limpios, piezas para todos los días
y un mensaje que va contigo.
</p>

<div class="hero-actions">

<button
class="primary"
onclick="document.querySelector('#shop').scrollIntoView({behavior:'smooth'})">

SHOP THE DROP

</button>

<button
class="secondary"
onclick="document.querySelector('#categories').scrollIntoView({behavior:'smooth'})">

VIEW CATEGORIES

</button>

</div>

</div>

</section>


<!-- =========================
     MARQUEE
========================= -->

<div class="strip">

<div>

<span>SNG</span>

<span>GOD STAYS NEAR</span>

<span>COLLECTION 01</span>

<span>STAY CLOSE</span>

<span>SNG</span>

<span>GOD STAYS NEAR</span>

<span>COLLECTION 01</span>

<span>STAY CLOSE</span>

</div>

</div>


<!-- =========================
     CATEGORIES
========================= -->

<section
class="quick wrap"
id="categories">

<div class="quick-head">

<div>

<div class="eyebrow">
FIND IT FAST
</div>

<h2>
SHOP BY<br>
CATEGORY.
</h2>

</div>

<p>
Entra directamente en la categoría que buscas.
Sin perder tiempo.
</p>

</div>


<div class="categories">

<button
class="cat"
onclick="setFilter('shirts')">

<div>

<strong>
T-SHIRTS
</strong>

<small>
ESSENTIALS & GRAPHICS
</small>

</div>

</button>


<button
class="cat"
onclick="setFilter('hoodies')">

<div>

<strong>
HOODIES
</strong>

<small>
HEAVY & OVERSIZED
</small>

</div>

</button>


<button
class="cat"
onclick="setFilter('pants')">

<div>

<strong>
PANTS
</strong>

<small>
RELAXED & CARGO
</small>

</div>

</button>


<button
class="cat"
onclick="setFilter('shorts')">

<div>

<strong>
SHORTS
</strong>

<small>
EVERYDAY FIT
</small>

</div>

</button>


<button
class="cat"
onclick="setFilter('caps')">

<div>

<strong>
CAPS
</strong>

<small>
SIGNATURE ACCESSORIES
</small>

</div>

</button>

</div>

</section>


<!-- =========================
     SHOP
========================= -->

<section
class="shop wrap"
id="shop">


<div class="shopbar">


<div class="filters">

<button
class="filter active"
data-f="all"
onclick="setFilter('all')">
ALL
</button>

<button
class="filter"
data-f="shirts"
onclick="setFilter('shirts')">
T-SHIRTS
</button>

<button
class="filter"
data-f="hoodies"
onclick="setFilter('hoodies')">
HOODIES
</button>

<button
class="filter"
data-f="pants"
onclick="setFilter('pants')">
PANTS
</button>

<button
class="filter"
data-f="shorts"
onclick="setFilter('shorts')">
SHORTS
</button>

<button
class="filter"
data-f="caps"
onclick="setFilter('caps')">
CAPS
</button>

</div>


<input
id="search"
class="search"
placeholder="Search SNG..."
oninput="render()">

</div>


<div
class="products"
id="products">
</div>


</section>


<!-- =========================
     MESSAGE
========================= -->

<section
class="story"
id="story">

<div class="storygrid wrap">

<div>

<div class="eyebrow">
THE MESSAGE
</div>

<h2>
GOD STAYS<br>
NEAR.
</h2>

</div>


<p>

SNG nace alrededor de una idea sencilla:

<strong>
GOD STAYS NEAR.
</strong>

Creamos prendas modernas para llevar ese mensaje contigo.

No buscamos llenar el armario;
buscamos crear piezas que tengan identidad.

</p>

</div>

</section>


<!-- =========================
     LOOKBOOK
========================= -->

<section class="look wrap">

<div class="lookgrid">


<div>

<div class="eyebrow">
COLLECTION 01
</div>

<h2>
MADE TO<br>
STAY.
</h2>

<p>
Una colección construida alrededor de tonos
fáciles de llevar, gráficos fuertes y el lenguaje
visual de SNG.
</p>

</div>


<div>

<img
src="images/lookbook.jpg"
alt="SNG Collection">

</div>


</div>

</section>


<!-- =========================
     FOOTER
========================= -->

<footer>

<div>

<strong>
SNG®
</strong>

<p>
GOD STAYS NEAR.
</p>

</div>


<div class="flinks">

<a href="#">
INSTAGRAM
</a>

<a href="#">
TIKTOK
</a>

<a href="#">
CONTACT
</a>

</div>

</footer>


<!-- =========================
     PRODUCT MODAL
========================= -->

<div
class="overlay"
id="overlay"
onclick="if(event.target===this)closeModal()">


<div class="modal">


<div class="modalphoto">

<img
id="mimg"
src=""
alt="">

</div>


<div class="modalinfo">

<button
class="close"
onclick="closeModal()">

×

</button>


<h2 id="mname">
</h2>


<div
class="mp"
id="mprice">
</div>


<p>

Una pieza de SNG diseñada alrededor
del mensaje

<strong>
GOD STAYS NEAR.
</strong>

</p>


<div class="sizes">

<button
class="size"
onclick="size(this)">
XS
</button>

<button
class="size"
onclick="size(this)">
S
</button>

<button
class="size sel"
onclick="size(this)">
M
</button>

<button
class="size"
onclick="size(this)">
L
</button>

<button
class="size"
onclick="size(this)">
XL
</button>

</div>


<button
class="add"
onclick="add()">

ADD TO BAG

</button>


</div>

</div>

</div>


<!-- =========================
     CART
========================= -->

<aside
class="cart"
id="cart">


<div class="carthead">

<strong>
YOUR BAG
</strong>

<button
class="close"
onclick="closeCart()">

×

</button>

</div>


<div
class="cartitems"
id="items">
</div>


<div class="total">

<span>
TOTAL
</span>

<span id="total">
0,00 €
</span>

</div>


<button
class="checkout"
onclick="checkout()">

CHECKOUT

</button>


</aside>


<script>

/* =========================
   PRODUCTS
========================= */

const products=[

[
'Essential White Tee',
'shirts',
'29,99 €',
'images/tee-1.jpg'
],

[
'Signature Black Tee',
'shirts',
'29,99 €',
'images/tee-2.jpg'
],

[
'Olive Near Tee',
'shirts',
'34,99 €',
'images/tee-3.jpg'
],

[
'Cream Cross Tee',
'shirts',
'34,99 €',
'images/tee-4.jpg'
],


[
'Midnight Faith Hoodie',
'hoodies',
'64,99 €',
'images/hoodie-1.jpg'
],

[
'Heavy Grey Hoodie',
'hoodies',
'64,99 €',
'images/hoodie-2.jpg'
],

[
'Earth Brown Hoodie',
'hoodies',
'64,99 €',
'images/hoodie-3.jpg'
],

[
'Cream Statement Hoodie',
'hoodies',
'64,99 €',
'images/hoodie-4.jpg'
],


[
'Core Black Pants',
'pants',
'64,99 €',
'images/bottom-1.jpg'
],

[
'Grey Essential Pants',
'pants',
'64,99 €',
'images/bottom-2.jpg'
],

[
'Olive Utility Cargo',
'pants',
'69,99 €',
'images/bottom-3.jpg'
],

[
'Black Utility Cargo',
'pants',
'69,99 €',
'images/bottom-4.jpg'
],


[
'Black Everyday Shorts',
'shorts',
'39,99 €',
'images/bottom-5.jpg'
],

[
'Grey Everyday Shorts',
'shorts',
'39,99 €',
'images/bottom-6.jpg'
],

[
'Olive Everyday Shorts',
'shorts',
'39,99 €',
'images/bottom-7.jpg'
],

[
'Cream Everyday Shorts',
'shorts',
'39,99 €',
'images/bottom-8.jpg'
],


[
'Signature Black Cap',
'caps',
'24,99 €',
'images/cap-1.jpg'
],

[
'Cream Near Cap',
'caps',
'24,99 €',
'images/cap-2.jpg'
],

[
'Olive SNG Cap',
'caps',
'24,99 €',
'images/cap-3.jpg'
],

[
'Navy Signature Cap',
'caps',
'24,99 €',
'images/cap-4.jpg'
],

[
'Charcoal SNG Cap',
'caps',
'24,99 €',
'images/cap-5.jpg'
],

[
'Brown Near Cap',
'caps',
'24,99 €',
'images/cap-6.jpg'
]

];


let filter='all';

let cart=[];

let current=null;

let chosen='M';


/* =========================
   FILTER
========================= */

function setFilter(f){

filter=f;

document
.querySelectorAll('.filter')
.forEach(button=>{

button.classList.toggle(
'active',
button.dataset.f===f
);

});

document
.querySelector('#shop')
.scrollIntoView({
behavior:'smooth',
block:'start'
});

render();

}


/* =========================
   RENDER PRODUCTS
========================= */

function render(){

const search=
document
.querySelector('#search')
.value
.toLowerCase();


const list=
products.filter(product=>{

const categoryMatch=
filter==='all' ||
product[1]===filter;

const searchMatch=
product[0]
.toLowerCase()
.includes(search);

return categoryMatch && searchMatch;

});


document
.querySelector('#products')
.innerHTML=

list.map((product)=>{

const originalIndex=
products.indexOf(product);

return `

<article
class="product"
onclick="openModal(${originalIndex})">

<div class="photo">

${
originalIndex<4 && filter==='all'
?
'<span class="badge">NEW DROP</span>'
:
''
}

<img
src="${product[3]}"
alt="${product[0]}"
onerror="this.style.display='none';this.parentElement.innerHTML='<div style=&quot;height:100%;display:grid;place-items:center;font-size:10px;color:#777;text-align:center;padding:20px&quot;>IMAGEN NO ENCONTRADA<br>${product[3]}</div>'">

</div>


<div class="info">

<h3>
${product[0]}
</h3>

<p>
GOD STAYS NEAR · ${product[1].toUpperCase()}
</p>

<div class="price">
${product[2]}
</div>

</div>

</article>

`;

}).join('');


if(list.length===0){

document
.querySelector('#products')
.innerHTML=`

<p
style="
grid-column:1/-1;
padding:40px 0;
color:#777;
">

No hemos encontrado esa prenda.

</p>

`;

}

}


/* =========================
   PRODUCT MODAL
========================= */

function openModal(index){

current=products[index];

document
.querySelector('#mimg')
.src=current[3];

document
.querySelector('#mname')
.textContent=current[0];

document
.querySelector('#mprice')
.textContent=current[2];

document
.querySelector('#overlay')
.classList.add('show');

}


/* =========================
   CLOSE MODAL
========================= */

function closeModal(){

document
.querySelector('#overlay')
.classList.remove('show');

}


/* =========================
   SIZE
========================= */

function size(button){

document
.querySelectorAll('.size')
.forEach(x=>{

x.classList.remove('sel');

});

button.classList.add('sel');

chosen=button.textContent;

}


/* =========================
   ADD TO CART
========================= */

function add(){

if(!current){
return;
}

cart.push({

name:current[0],

price:current[2],

size:chosen

});

updateCart();

closeModal();

openCart();

}


/* =========================
   CART
========================= */

function openCart(){

document
.querySelector('#cart')
.classList.add('open');

}


function closeCart(){

document
.querySelector('#cart')
.classList.remove('open');

}


/* =========================
   UPDATE CART
========================= */

function updateCart(){

document
.querySelector('#count')
.textContent=cart.length;


document
.querySelector('#items')
.innerHTML=

cart.length

?

cart.map((item,index)=>`

<div class="ci">

<span>

<b>
${item.name}
</b>

<br>

Size ${item.size}

</span>


<span>

${item.price}

<button
onclick="removeItem(${index})"
style="
border:0;
background:none;
font-size:16px;
margin-left:6px;
">

×
</button>

</span>

</div>

`).join('')

:

'<p style="color:#777;font-size:11px">Your bag is empty.</p>';


let total=0;


cart.forEach(item=>{

total+=parseFloat(
item.price
.replace('.','')
.replace(',','.')
);

});


document
.querySelector('#total')
.textContent=

total
.toFixed(2)
.replace('.',',')
+' €';

}


/* =========================
   REMOVE ITEM
========================= */

function removeItem(index){

cart.splice(index,1);

updateCart();

}


/* =========================
   CHECKOUT
========================= */

function checkout(){

if(cart.length===0){

alert(
'Tu bolsa está vacía.'
);

return;

}

alert(
'El checkout se conectará aquí con tu sistema de pago.'
);

}


/* =========================
   ESC CLOSE
========================= */

document
.addEventListener(
'keydown',
function(event){

if(event.key==='Escape'){

closeModal();

closeCart();

}

});


/* =========================
   INITIAL RENDER
========================= */

render();

</script>

</body>
</html>
