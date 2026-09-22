<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>GOD STAYS NEAR</title>

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
    font-family:Arial, Helvetica, sans-serif;
    background:#000;
    color:#fff;
}

/* =========================
   HEADER
========================= */

header{
    position:sticky;
    top:0;
    z-index:1000;
    height:82px;
    background:#000;
    border-bottom:1px solid #222;
    display:flex;
    align-items:center;
    justify-content:space-between;
    padding:0 6%;
}

.logo-area{
    display:flex;
    align-items:center;
    gap:14px;
}

.logo{
    width:55px;
    height:55px;
}

.logo svg{
    width:100%;
    height:100%;
}

.brand{
    font-size:17px;
    font-weight:900;
    letter-spacing:4px;
}

nav{
    display:flex;
    gap:12px;
}

.nav-btn{
    border:1px solid #444;
    background:#111;
    color:#fff;
    padding:12px 22px;
    border-radius:50px;
    cursor:pointer;
    font-size:13px;
    transition:.3s;
}

.nav-btn:hover{
    background:#fff;
    color:#000;
}

/* =========================
   HERO
========================= */

.hero{
    min-height:90vh;
    display:flex;
    flex-direction:column;
    justify-content:center;
    align-items:center;
    text-align:center;
    padding:70px 20px;
    background:
        radial-gradient(circle at center,#202020 0%,#080808 40%,#000 75%);
}

.hero-logo{
    width:180px;
    height:180px;
    margin-bottom:30px;
}

.hero-logo svg{
    width:100%;
    height:100%;
}

.hero h1{
    font-size:clamp(45px,8vw,100px);
    letter-spacing:8px;
    font-weight:900;
    line-height:.9;
}

.hero p{
    margin-top:25px;
    color:#aaa;
    font-size:15px;
    letter-spacing:5px;
}

.hero-buttons{
    display:flex;
    gap:15px;
    margin-top:40px;
}

.round-btn{
    border:none;
    background:#fff;
    color:#000;
    padding:15px 30px;
    border-radius:50px;
    font-weight:bold;
    cursor:pointer;
    transition:.3s;
}

.round-btn:hover{
    transform:scale(1.06);
    background:#ddd;
}

.round-btn.dark{
    background:#111;
    color:#fff;
    border:1px solid #444;
}

/* =========================
   SECTION
========================= */

section{
    padding:100px 7%;
}

.section-title{
    text-align:center;
    margin-bottom:55px;
}

.section-title h2{
    font-size:42px;
    letter-spacing:4px;
}

.section-title p{
    color:#888;
    margin-top:12px;
}

/* =========================
   PRODUCTS
========================= */

.products{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(230px,1fr));
    gap:25px;
}

.product{
    background:#0d0d0d;
    border:1px solid #222;
    border-radius:24px;
    overflow:hidden;
    cursor:pointer;
    transition:.35s;
    position:relative;
}

.product:hover{
    transform:translateY(-8px);
    border-color:#555;
}

.product-image{
    height:360px;
    background:#111;
    display:flex;
    align-items:center;
    justify-content:center;
    overflow:hidden;
    position:relative;
}

.product-image img{
    width:100%;
    height:100%;
    object-fit:cover;
    transition:.4s;
}

.product:hover img{
    transform:scale(1.05);
}

.favorite{
    position:absolute;
    top:15px;
    right:15px;
    width:42px;
    height:42px;
    border-radius:50%;
    background:#000;
    color:#fff;
    border:1px solid #444;
    font-size:19px;
    cursor:pointer;
    z-index:5;
}

.favorite.active{
    background:#fff;
    color:#000;
}

.product-info{
    padding:20px;
}

.product-info h3{
    font-size:18px;
    margin-bottom:8px;
}

.product-info p{
    color:#777;
    font-size:13px;
}

.price{
    margin-top:15px;
    font-size:17px;
    font-weight:bold;
}

/* =========================
   CATEGORIES
========================= */

.categories{
    display:flex;
    justify-content:center;
    flex-wrap:wrap;
    gap:12px;
    margin-bottom:45px;
}

.category{
    border:1px solid #333;
    background:#0c0c0c;
    color:white;
    padding:12px 25px;
    border-radius:50px;
    cursor:pointer;
    transition:.3s;
}

.category:hover,
.category.active{
    background:#fff;
    color:#000;
}

/* =========================
   PRODUCT MODAL
========================= */

.modal{
    position:fixed;
    inset:0;
    background:rgba(0,0,0,.9);
    backdrop-filter:blur(10px);
    display:none;
    align-items:center;
    justify-content:center;
    z-index:3000;
    padding:20px;
}

.modal.show{
    display:flex;
}

.modal-content{
    width:min(950px,100%);
    max-height:90vh;
    overflow:auto;
    background:#0b0b0b;
    border:1px solid #333;
    border-radius:30px;
    display:grid;
    grid-template-columns:1fr 1fr;
    position:relative;
}

.modal-image{
    min-height:550px;
}

.modal-image img{
    width:100%;
    height:100%;
    min-height:550px;
    object-fit:cover;
}

.modal-info{
    padding:45px;
    display:flex;
    flex-direction:column;
    justify-content:center;
}

.close{
    position:absolute;
    top:18px;
    right:18px;
    width:45px;
    height:45px;
    border-radius:50%;
    border:1px solid #555;
    background:#000;
    color:#fff;
    cursor:pointer;
    font-size:20px;
    z-index:10;
}

.modal-info h2{
    font-size:38px;
    margin-bottom:12px;
}

.modal-info .description{
    color:#999;
    line-height:1.7;
    margin:20px 0;
}

.modal-price{
    font-size:25px;
    font-weight:bold;
    margin-bottom:25px;
}

.sizes{
    display:flex;
    gap:10px;
    flex-wrap:wrap;
    margin-bottom:25px;
}

.size{
    width:50px;
    height:50px;
    border-radius:50%;
    border:1px solid #444;
    background:#111;
    color:#fff;
    cursor:pointer;
}

.size:hover,
.size.selected{
    background:#fff;
    color:#000;
}

.buy{
    width:100%;
    border:none;
    border-radius:50px;
    padding:17px;
    background:#fff;
    color:#000;
    font-weight:bold;
    cursor:pointer;
}

/* =========================
   ABOUT
========================= */

.about{
    background:#080808;
    text-align:center;
}

.about-box{
    max-width:750px;
    margin:auto;
}

.about h2{
    font-size:40px;
    letter-spacing:3px;
    margin-bottom:25px;
}

.about p{
    color:#999;
    line-height:1.8;
}

/* =========================
   FOOTER
========================= */

footer{
    padding:50px 7%;
    border-top:1px solid #222;
    text-align:center;
}

.footer-logo{
    font-weight:900;
    letter-spacing:5px;
    font-size:20px;
}

footer p{
    margin-top:15px;
    color:#666;
    font-size:12px;
}

/* =========================
   RESPONSIVE
========================= */

@media(max-width:750px){

    header{
        padding:0 20px;
    }

    nav{
        display:none;
    }

    .brand{
        font-size:13px;
    }

    .hero h1{
        letter-spacing:4px;
    }

    .hero-logo{
        width:130px;
        height:130px;
    }

    .modal-content{
        grid-template-columns:1fr;
    }

    .modal-image,
    .modal-image img{
        min-height:350px;
        height:350px;
    }

    .modal-info{
        padding:30px;
    }

    section{
        padding:70px 20px;
    }
}
</style>
</head>

<body>

<!-- =========================
     LOGO SVG
========================= -->

<svg id="logo-template"
     xmlns="http://www.w3.org/2000/svg"
     viewBox="0 0 500 500"
     style="display:none">

    <polygon
        points="250,25 470,145 470,355 250,475 30,355 30,145"
        fill="none"
        stroke="white"
        stroke-width="24"/>

    <text
        x="250"
        y="315"
        text-anchor="middle"
        fill="white"
        font-size="150"
        font-family="Arial"
        font-weight="900"
        letter-spacing="-20">
        GSN
    </text>
</svg>


<!-- =========================
     HEADER
========================= -->

<header>

    <div class="logo-area">

        <div class="logo">
            <svg viewBox="0 0 500 500">
                <polygon
                    points="250,25 470,145 470,355 250,475 30,355 30,145"
                    fill="none"
                    stroke="white"
                    stroke-width="24"/>
                <text
                    x="250"
                    y="315"
                    text-anchor="middle"
                    fill="white"
                    font-size="150"
                    font-family="Arial"
                    font-weight="900"
                    letter-spacing="-20">
                    GSN
                </text>
            </svg>
        </div>

        <div class="brand">GOD STAYS NEAR</div>

    </div>

    <nav>
        <button class="nav-btn" onclick="goTo('catalogo')">Catálogo</button>
        <button class="nav-btn" onclick="goTo('sobre')">Sobre nosotros</button>
        <button class="nav-btn" onclick="goTo('favoritos')">♡ Favoritos</button>
    </nav>

</header>


<!-- =========================
     HERO
========================= -->

<div class="hero">

    <div class="hero-logo">

        <svg viewBox="0 0 500 500">

            <polygon
                points="250,25 470,145 470,355 250,475 30,355 30,145"
                fill="none"
                stroke="white"
                stroke-width="24"/>

            <text
                x="250"
                y="315"
                text-anchor="middle"
                fill="white"
                font-size="150"
                font-family="Arial"
                font-weight="900"
                letter-spacing="-20">
                GSN
            </text>

        </svg>

    </div>

    <h1>GOD STAYS NEAR</h1>

    <p>STREETWEAR • FAITH • STYLE</p>

    <div class="hero-buttons">

        <button class="round-btn" onclick="goTo('catalogo')">
            VER COLECCIÓN
        </button>

        <button class="round-btn dark" onclick="goTo('sobre')">
            CONOCER MARCA
        </button>

    </div>

</div>


<!-- =========================
     CATALOGO
========================= -->

<section id="catalogo">

    <div class="section-title">

        <h2>CATÁLOGO</h2>

        <p>Descubre nuestra colección</p>

    </div>


    <div class="categories">

        <button class="category active" onclick="filterProducts('todos',this)">
            Todos
        </button>

        <button class="category" onclick="filterProducts('camisetas',this)">
            Camisetas
        </button>

        <button class="category" onclick="filterProducts('sudaderas',this)">
            Sudaderas
        </button>

        <button class="category" onclick="filterProducts('pantalones',this)">
            Pantalones
        </button>

        <button class="category" onclick="filterProducts('gorras',this)">
            Gorras
        </button>

    </div>


    <div class="products" id="products">

        <!-- CAMISETA -->

        <div class="product"
             data-category="camisetas"
             onclick="openProduct(0)">

            <div class="product-image">

                <button class="favorite"
                        onclick="toggleFavorite(event,this)">
                    ♡
                </button>

                <img src="https://images.unsplash.com/photo-1521572163474-6864f9cf17ab?auto=format&fit=crop&w=800&q=90">

            </div>

            <div class="product-info">

                <h3>Oversized Essential</h3>

                <p>Camiseta negra oversized</p>

                <div class="price">29,99 €</div>

            </div>

        </div>


        <!-- SUDADERA -->

        <div class="product"
             data-category="sudaderas"
             onclick="openProduct(1)">

            <div class="product-image">

                <button class="favorite"
                        onclick="toggleFavorite(event,this)">
                    ♡
                </button>

                <img src="https://images.unsplash.com/photo-1556821840-3a63f95609a7?auto=format&fit=crop&w=800&q=90">

            </div>

            <div class="product-info">

                <h3>Classic Hoodie</h3>

                <p>Sudadera negra con capucha</p>

                <div class="price">54,99 €</div>

            </div>

        </div>


        <!-- PANTALON -->

        <div class="product"
             data-category="pantalones"
             onclick="openProduct(2)">

            <div class="product-image">

                <button class="favorite"
                        onclick="toggleFavorite(event,this)">
                    ♡
                </button>

                <img src="https://images.unsplash.com/photo-1624378439575-d8705ad7ae80?auto=format&fit=crop&w=800&q=90">

            </div>

            <div class="product-info">

                <h3>Wide Street Pants</h3>

                <p>Pantalón negro estilo street</p>

                <div class="price">49,99 €</div>

            </div>

        </div>


        <!-- GORRA -->

        <div class="product"
             data-category="gorras"
             onclick="openProduct(3)">

            <div class="product-image">

                <button class="favorite"
                        onclick="toggleFavorite(event,this)">
                    ♡
                </button>

                <img src="https://images.unsplash.com/photo-1588850561407-ed78c282e89b?auto=format&fit=crop&w=800&q=90">

            </div>

            <div class="product-info">

                <h3>GSN Cap</h3>

                <p>Gorra negra minimalista</p>

                <div class="price">24,99 €</div>

            </div>

        </div>


        <!-- CAMISETA 2 -->

        <div class="product"
             data-category="camisetas"
             onclick="openProduct(4)">

            <div class="product-image">

                <button class="favorite"
                        onclick="toggleFavorite(event,this)">
                    ♡
                </button>

                <img src="https://images.unsplash.com/photo-1503341504253-dff4815485f1?auto=format&fit=crop&w=800&q=90">

            </div>

            <div class="product-info">

                <h3>Minimal Logo Tee</h3>

                <p>Camiseta de algodón</p>

                <div class="price">32,99 €</div>

            </div>

        </div>


        <!-- SUDADERA 2 -->

        <div class="product"
             data-category="sudaderas"
             onclick="openProduct(5)">

            <div class="product-image">

                <button class="favorite"
                        onclick="toggleFavorite(event,this)">
                    ♡
                </button>

                <img src="https://images.unsplash.com/photo-1578681994506-b8f463449011?auto=format&fit=crop&w=800&q=90">

            </div>

            <div class="product-info">

                <h3>Heavy Oversized</h3>

                <p>Sudadera oversize</p>

                <div class="price">59,99 €</div>

            </div>

        </div>

    </div>

</section>


<!-- =========================
     FAVORITOS
========================= -->

<section id="favoritos">

    <div class="section-title">

        <h2>♡ FAVORITOS</h2>

        <p>Guarda tus prendas favoritas.</p>

    </div>

    <div style="text-align:center;color:#777;">
        Pulsa el corazón de cualquier producto para guardarlo.
    </div>

</section>


<!-- =========================
     SOBRE
========================= -->

<section class="about" id="sobre">

    <div class="about-box">

        <h2>GOD STAYS NEAR</h2>

        <p>
            Una marca de ropa urbana con un estilo sencillo,
            moderno y diferente. Nuestra idea es crear prendas
            cómodas que puedas llevar todos los días.
            El diseño combina el blanco y negro con nuestro
            logo GSN para conseguir una identidad reconocible.
        </p>

    </div>

</section>


<!-- =========================
     MODAL
========================= -->

<div class="modal" id="productModal">

    <div class="modal-content">

        <button class="close" onclick="closeProduct()">×</button>

        <div class="modal-image">
            <img id="modalImage">
        </div>

        <div class="modal-info">

            <h2 id="modalTitle"></h2>

            <div class="modal-price" id="modalPrice"></div>

            <p class="description" id="modalDescription"></p>

            <h3 style="margin-bottom:15px;">Selecciona tu talla</h3>

            <div class="sizes">

                <button class="size" onclick="selectSize(this)">XS</button>
                <button class="size" onclick="selectSize(this)">S</button>
                <button class="size" onclick="selectSize(this)">M</button>
                <button class="size" onclick="selectSize(this)">L</button>
                <button class="size" onclick="selectSize(this)">XL</button>

            </div>

            <button class="buy" onclick="buyProduct()">
                AÑADIR A FAVORITOS
            </button>

        </div>

    </div>

</div>


<!-- =========================
     FOOTER
========================= -->

<footer>

    <div class="footer-logo">
        GOD STAYS NEAR
    </div>

    <p>GSN — STREETWEAR COLLECTION</p>

</footer>


<script>

/* =========================
   PRODUCT DATA
========================= */

const products = [

    {
        title:"Oversized Essential",
        price:"29,99 €",
        image:"https://images.unsplash.com/photo-1521572163474-6864f9cf17ab?auto=format&fit=crop&w=1000&q=90",
        description:"Camiseta negra oversized, cómoda y sencilla. Diseñada para combinar fácilmente con cualquier outfit."
    },

    {
        title:"Classic Hoodie",
        price:"54,99 €",
        image:"https://images.unsplash.com/photo-1556821840-3a63f95609a7?auto=format&fit=crop&w=1000&q=90",
        description:"Sudadera negra con capucha y diseño minimalista. Una prenda cómoda para cualquier día."
    },

    {
        title:"Wide Street Pants",
        price:"49,99 €",
        image:"https://images.unsplash.com/photo-1624378439575-d8705ad7ae80?auto=format&fit=crop&w=1000&q=90",
        description:"Pantalón negro de estilo urbano con un corte cómodo y amplio."
    },

    {
        title:"GSN Cap",
        price:"24,99 €",
        image:"https://images.unsplash.com/photo-1588850561407-ed78c282e89b?auto=format&fit=crop&w=1000&q=90",
        description:"Gorra negra minimalista inspirada en la identidad de GOD STAYS NEAR."
    },

    {
        title:"Minimal Logo Tee",
        price:"32,99 €",
        image:"https://images.unsplash.com/photo-1503341504253-dff4815485f1?auto=format&fit=crop&w=1000&q=90",
        description:"Camiseta de algodón con un diseño limpio y moderno."
    },

    {
        title:"Heavy Oversized",
        price:"59,99 €",
        image:"https://images.unsplash.com/photo-1578681994506-b8f463449011?auto=format&fit=crop&w=1000&q=90",
        description:"Sudadera oversize de estilo urbano, pensada para conseguir un look moderno."
    }

];


/* =========================
   SCROLL
========================= */

function goTo(id){

    document.getElementById(id).scrollIntoView({
        behavior:"smooth"
    });

}


/* =========================
   FILTER
========================= */

function filterProducts(category,button){

    document.querySelectorAll(".category").forEach(btn=>{
        btn.classList.remove("active");
    });

    button.classList.add("active");

    document.querySelectorAll(".product").forEach(product=>{

        if(category === "todos"){
            product.style.display="block";
        }
        else if(product.dataset.category === category){
            product.style.display="block";
        }
        else{
            product.style.display="none";
        }

    });

}


/* =========================
   FAVORITES
========================= */

function toggleFavorite(event,button){

    event.stopPropagation();

    button.classList.toggle("active");

    if(button.classList.contains("active")){
        button.innerHTML="♥";
    }
    else{
        button.innerHTML="♡";
    }

}


/* =========================
   OPEN PRODUCT
========================= */

function openProduct(index){

    const product = products[index];

    document.getElementById("modalTitle").textContent=product.title;

    document.getElementById("modalPrice").textContent=product.price;

    document.getElementById("modalDescription").textContent=product.description;

    document.getElementById("modalImage").src=product.image;

    document.getElementById("productModal").classList.add("show");

    document.body.style.overflow="hidden";

}


/* =========================
   CLOSE PRODUCT
========================= */

function closeProduct(){

    document.getElementById("productModal").classList.remove("show");

    document.body.style.overflow="auto";

}


/* =========================
   SIZE
========================= */

function selectSize(button){

    document.querySelectorAll(".size").forEach(size=>{
        size.classList.remove("selected");
    });

    button.classList.add("selected");

}


/* =========================
   FAVORITE FROM MODAL
========================= */

function buyProduct(){

    alert("Prenda añadida a favoritos ♡");

}


/* =========================
   CLOSE MODAL OUTSIDE
========================= */

document.getElementById("productModal").addEventListener("click",function(e){

    if(e.target === this){
        closeProduct();
    }

});


/* =========================
   ESC KEY
========================= */

document.addEventListener("keydown",function(e){

    if(e.key === "Escape"){
        closeProduct();
    }

});

</script>

</body>
</html>
