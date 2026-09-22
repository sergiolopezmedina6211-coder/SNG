<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>GOD STAYS NEAR | Streetwear</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

:root{
    --black:#151515;
    --dark:#202020;
    --soft:#292929;
    --light:#f5f5f5;
    --gray:#cfcfcf;
    --muted:#999;
    --white:#ffffff;
}

html{
    scroll-behavior:smooth;
}

body{
    font-family:Arial,Helvetica,sans-serif;
    background:#181818;
    color:var(--light);
    overflow-x:hidden;
}

/* FONDO SUAVE */

body::before{
    content:"";
    position:fixed;
    inset:0;
    z-index:-5;
    background:
        linear-gradient(
            rgba(20,20,20,.72),
            rgba(20,20,20,.86)
        ),
        url("https://images.unsplash.com/photo-1441986300917-64674bd600d8?auto=format&fit=crop&w=2200&q=85")
        center/cover no-repeat;
    filter:saturate(.45);
}

/* LOGO GIGANTE DE FONDO */

body::after{
    content:"GSN";
    position:fixed;
    right:-100px;
    bottom:-50px;
    z-index:-4;
    font-size:clamp(250px,35vw,650px);
    font-weight:900;
    line-height:.7;
    letter-spacing:-45px;
    color:rgba(255,255,255,.035);
    pointer-events:none;
}

a{
    color:inherit;
    text-decoration:none;
}

button{
    font-family:inherit;
}

/* HEADER */

header{
    position:fixed;
    top:0;
    left:0;
    width:100%;
    height:82px;
    z-index:1000;
    display:flex;
    align-items:center;
    justify-content:space-between;
    padding:0 5%;
    background:rgba(18,18,18,.78);
    backdrop-filter:blur(18px);
    border-bottom:1px solid rgba(255,255,255,.09);
}

.logo-area{
    display:flex;
    align-items:center;
    gap:13px;
}

.logo{
    width:48px;
    height:48px;
    display:flex;
    align-items:center;
    justify-content:center;
}

.logo svg{
    width:100%;
    height:100%;
}

.brand-name{
    font-size:17px;
    font-weight:800;
    letter-spacing:2px;
}

nav{
    display:flex;
    align-items:center;
    gap:9px;
}

.nav-btn{
    border:1px solid rgba(255,255,255,.13);
    background:rgba(255,255,255,.07);
    color:white;
    border-radius:999px;
    padding:11px 18px;
    cursor:pointer;
    transition:.25s;
    font-size:13px;
}

.nav-btn:hover{
    background:white;
    color:#151515;
    transform:translateY(-2px);
}

.fav-counter{
    min-width:23px;
    height:23px;
    padding:0 7px;
    display:inline-flex;
    align-items:center;
    justify-content:center;
    border-radius:50%;
    background:white;
    color:#151515;
    margin-left:4px;
    font-size:11px;
    font-weight:bold;
}

/* HERO */

.hero{
    min-height:100vh;
    padding:150px 6% 90px;
    display:grid;
    grid-template-columns:1.05fr .95fr;
    align-items:center;
    gap:50px;
    position:relative;
    overflow:hidden;
}

.hero::before{
    content:"";
    position:absolute;
    width:600px;
    height:600px;
    border-radius:50%;
    background:rgba(255,255,255,.045);
    filter:blur(30px);
    right:-200px;
    top:80px;
}

.hero-content{
    position:relative;
    z-index:2;
}

.eyebrow{
    display:inline-block;
    padding:9px 15px;
    border:1px solid rgba(255,255,255,.16);
    border-radius:999px;
    background:rgba(255,255,255,.06);
    color:#d7d7d7;
    font-size:11px;
    letter-spacing:2px;
    text-transform:uppercase;
    margin-bottom:22px;
}

.hero h1{
    font-size:clamp(55px,8vw,112px);
    line-height:.86;
    letter-spacing:-6px;
    font-weight:900;
    max-width:800px;
}

.hero h1 span{
    color:#bcbcbc;
}

.hero-text{
    max-width:560px;
    color:#c1c1c1;
    line-height:1.7;
    margin-top:30px;
    font-size:16px;
}

.hero-actions{
    display:flex;
    gap:12px;
    margin-top:32px;
    flex-wrap:wrap;
}

.primary-btn,
.secondary-btn{
    border-radius:999px;
    padding:15px 25px;
    font-weight:700;
    cursor:pointer;
    transition:.25s;
}

.primary-btn{
    background:white;
    color:#151515;
    border:1px solid white;
}

.primary-btn:hover{
    transform:translateY(-3px);
    box-shadow:0 15px 30px rgba(0,0,0,.25);
}

.secondary-btn{
    background:rgba(255,255,255,.06);
    color:white;
    border:1px solid rgba(255,255,255,.16);
}

.secondary-btn:hover{
    background:rgba(255,255,255,.12);
    transform:translateY(-3px);
}

/* HERO VISUAL */

.hero-visual{
    min-height:580px;
    border-radius:35px;
    position:relative;
    overflow:hidden;
    border:1px solid rgba(255,255,255,.12);
    box-shadow:0 35px 80px rgba(0,0,0,.3);
    background:
        linear-gradient(
            rgba(20,20,20,.15),
            rgba(20,20,20,.62)
        ),
        url("https://images.unsplash.com/photo-1555529771-35a38b2f8f9d?auto=format&fit=crop&w=1200&q=85")
        center/cover;
}

.hero-logo{
    position:absolute;
    inset:0;
    display:flex;
    align-items:center;
    justify-content:center;
    background:rgba(0,0,0,.15);
}

.hero-logo svg{
    width:55%;
    max-width:310px;
    filter:drop-shadow(0 20px 35px rgba(0,0,0,.4));
}

.hero-label{
    position:absolute;
    left:25px;
    bottom:25px;
    padding:14px 18px;
    border-radius:20px;
    background:rgba(15,15,15,.67);
    backdrop-filter:blur(12px);
    border:1px solid rgba(255,255,255,.12);
}

.hero-label strong{
    display:block;
    font-size:15px;
}

.hero-label small{
    color:#aaa;
    display:block;
    margin-top:4px;
}

/* SECCIONES */

section{
    padding:100px 6%;
}

.section-heading{
    display:flex;
    justify-content:space-between;
    align-items:end;
    gap:30px;
    margin-bottom:35px;
}

.section-heading h2{
    font-size:clamp(35px,5vw,65px);
    letter-spacing:-3px;
}

.section-heading p{
    max-width:430px;
    color:#aaa;
    line-height:1.6;
}

/* CATEGORÍAS */

.categories{
    display:flex;
    gap:10px;
    flex-wrap:wrap;
    margin-bottom:35px;
}

.category{
    border:1px solid rgba(255,255,255,.13);
    background:rgba(255,255,255,.06);
    color:#ddd;
    border-radius:999px;
    padding:12px 20px;
    cursor:pointer;
    transition:.25s;
}

.category:hover,
.category.active{
    background:white;
    color:#111;
}

/* PRODUCTOS */

.products{
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:22px;
}

.product{
    position:relative;
    border-radius:27px;
    overflow:hidden;
    background:rgba(35,35,35,.82);
    border:1px solid rgba(255,255,255,.09);
    transition:.3s;
}

.product:hover{
    transform:translateY(-7px);
    border-color:rgba(255,255,255,.22);
    box-shadow:0 25px 50px rgba(0,0,0,.3);
}

.product-image{
    height:420px;
    overflow:hidden;
    position:relative;
    cursor:pointer;
    background:#292929;
}

.product-image img{
    width:100%;
    height:100%;
    object-fit:cover;
    transition:.5s;
}

.product:hover .product-image img{
    transform:scale(1.04);
}

.favorite{
    position:absolute;
    right:15px;
    top:15px;
    width:43px;
    height:43px;
    border-radius:50%;
    border:1px solid rgba(255,255,255,.2);
    background:rgba(20,20,20,.65);
    color:white;
    cursor:pointer;
    font-size:18px;
    backdrop-filter:blur(8px);
    transition:.2s;
}

.favorite:hover{
    transform:scale(1.08);
}

.favorite.active{
    background:white;
    color:#111;
}

.product-info{
    padding:20px;
}

.product-category{
    color:#929292;
    text-transform:uppercase;
    font-size:10px;
    letter-spacing:1.5px;
}

.product-name{
    font-size:19px;
    font-weight:700;
    margin-top:7px;
}

.product-bottom{
    display:flex;
    align-items:center;
    justify-content:space-between;
    margin-top:15px;
}

.price{
    font-weight:800;
    font-size:16px;
}

.view-product{
    border:1px solid rgba(255,255,255,.14);
    background:rgba(255,255,255,.06);
    color:white;
    border-radius:999px;
    padding:9px 14px;
    cursor:pointer;
    transition:.2s;
}

.view-product:hover{
    background:white;
    color:#111;
}

/* BANNER */

.store-banner{
    min-height:480px;
    border-radius:35px;
    overflow:hidden;
    position:relative;
    display:flex;
    align-items:center;
    padding:60px;
    background:
        linear-gradient(
            90deg,
            rgba(10,10,10,.9),
            rgba(10,10,10,.45),
            rgba(10,10,10,.2)
        ),
        url("https://images.unsplash.com/photo-1556740749-887f6717d7e4?auto=format&fit=crop&w=1800&q=85")
        center/cover;
    border:1px solid rgba(255,255,255,.12);
}

.store-banner-content{
    max-width:600px;
}

.store-banner h2{
    font-size:clamp(45px,7vw,90px);
    line-height:.9;
    letter-spacing:-4px;
}

.store-banner p{
    color:#ccc;
    line-height:1.7;
    margin-top:22px;
    max-width:500px;
}

/* FAVORITOS */

#favoritesSection{
    display:none;
}

#favoritesSection.show{
    display:block;
}

.empty{
    padding:80px 20px;
    text-align:center;
    border:1px dashed rgba(255,255,255,.15);
    border-radius:28px;
    color:#aaa;
}

.empty h3{
    color:white;
    margin-bottom:10px;
}

/* ABOUT */

.about{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:25px;
}

.about-card{
    min-height:320px;
    padding:40px;
    border-radius:30px;
    background:rgba(35,35,35,.76);
    border:1px solid rgba(255,255,255,.09);
}

.about-card h3{
    font-size:28px;
    margin-bottom:17px;
}

.about-card p{
    color:#aaa;
    line-height:1.8;
}

.about-card.logo-card{
    display:flex;
    align-items:center;
    justify-content:center;
    position:relative;
    overflow:hidden;
    background:
        linear-gradient(rgba(20,20,20,.7),rgba(20,20,20,.7)),
        url("https://images.unsplash.com/photo-1529139574466-a303027c1d8b?auto=format&fit=crop&w=1000&q=80")
        center/cover;
}

.logo-card svg{
    width:230px;
    position:relative;
}

/* FOOTER */

footer{
    padding:60px 6% 35px;
    border-top:1px solid rgba(255,255,255,.09);
    background:rgba(12,12,12,.65);
}

.footer-top{
    display:flex;
    justify-content:space-between;
    gap:40px;
    flex-wrap:wrap;
}

.footer-brand{
    max-width:360px;
}

.footer-brand h3{
    font-size:22px;
    letter-spacing:2px;
}

.footer-brand p{
    color:#888;
    line-height:1.6;
    margin-top:12px;
}

.footer-links{
    display:flex;
    gap:12px;
    flex-wrap:wrap;
}

.footer-links a{
    color:#aaa;
    border:1px solid rgba(255,255,255,.1);
    padding:10px 15px;
    border-radius:999px;
}

.footer-bottom{
    margin-top:50px;
    padding-top:20px;
    border-top:1px solid rgba(255,255,255,.07);
    color:#666;
    font-size:12px;
}

/* MODAL */

.modal{
    position:fixed;
    inset:0;
    z-index:3000;
    display:none;
    align-items:center;
    justify-content:center;
    padding:25px;
    background:rgba(0,0,0,.72);
    backdrop-filter:blur(15px);
}

.modal.open{
    display:flex;
}

.modal-box{
    width:min(950px,100%);
    max-height:90vh;
    overflow:auto;
    border-radius:30px;
    background:#222;
    border:1px solid rgba(255,255,255,.13);
    display:grid;
    grid-template-columns:1fr 1fr;
    box-shadow:0 40px 100px rgba(0,0,0,.5);
}

.modal-image{
    min-height:560px;
}

.modal-image img{
    width:100%;
    height:100%;
    object-fit:cover;
}

.modal-content{
    padding:42px;
    position:relative;
}

.close{
    position:absolute;
    right:18px;
    top:18px;
    width:42px;
    height:42px;
    border-radius:50%;
    border:1px solid rgba(255,255,255,.15);
    background:rgba(255,255,255,.06);
    color:white;
    cursor:pointer;
    font-size:18px;
}

.modal-category{
    color:#999;
    font-size:11px;
    text-transform:uppercase;
    letter-spacing:2px;
}

.modal-content h2{
    font-size:42px;
    line-height:1;
    margin:12px 0;
    letter-spacing:-2px;
}

.modal-price{
    font-size:22px;
    font-weight:bold;
    margin-bottom:20px;
}

.modal-description{
    color:#aaa;
    line-height:1.7;
}

.sizes{
    display:flex;
    gap:8px;
    margin-top:28px;
    flex-wrap:wrap;
}

.size{
    min-width:48px;
    height:44px;
    border:1px solid rgba(255,255,255,.15);
    border-radius:12px;
    background:transparent;
    color:white;
    cursor:pointer;
}

.size:hover,
.size.selected{
    background:white;
    color:#111;
}

.modal-favorite{
    width:100%;
    margin-top:25px;
    padding:15px;
    border-radius:999px;
    border:1px solid rgba(255,255,255,.16);
    background:white;
    color:#111;
    font-weight:bold;
    cursor:pointer;
}

/* TOAST */

.toast{
    position:fixed;
    right:25px;
    bottom:25px;
    z-index:5000;
    padding:15px 20px;
    border-radius:999px;
    background:white;
    color:#111;
    font-size:13px;
    font-weight:700;
    transform:translateY(100px);
    opacity:0;
    transition:.3s;
}

.toast.show{
    transform:translateY(0);
    opacity:1;
}

/* RESPONSIVE */

@media(max-width:950px){
    .hero{
        grid-template-columns:1fr;
    }

    .hero-visual{
        min-height:500px;
    }

    .products{
        grid-template-columns:repeat(2,1fr);
    }

    .about{
        grid-template-columns:1fr;
    }

    .modal-box{
        grid-template-columns:1fr;
    }

    .modal-image{
        min-height:380px;
        max-height:450px;
    }
}

@media(max-width:650px){
    header{
        height:70px;
        padding:0 4%;
    }

    .brand-name{
        display:none;
    }

    nav .nav-btn:nth-child(1),
    nav .nav-btn:nth-child(2){
        display:none;
    }

    .hero{
        padding:120px 5% 70px;
    }

    .hero h1{
        letter-spacing:-4px;
    }

    section{
        padding:70px 5%;
    }

    .products{
        grid-template-columns:1fr;
    }

    .product-image{
        height:460px;
    }

    .store-banner{
        padding:35px;
        min-height:430px;
    }

    .modal-content{
        padding:30px 25px;
    }
}
</style>
</head>

<body>

<header>
    <a href="#" class="logo-area">
        <div class="logo">
            <svg viewBox="0 0 500 500">
                <polygon points="250,25 470,145 470,355 250,475 30,355 30,145"
                    fill="none"
                    stroke="white"
                    stroke-width="24"/>
                <text x="250"
                    y="315"
                    text-anchor="middle"
                    fill="white"
                    font-size="150"
                    font-family="Arial"
                    font-weight="900"
                    letter-spacing="-20">GSN</text>
            </svg>
        </div>
        <span class="brand-name">GOD STAYS NEAR</span>
    </a>

    <nav>
        <a href="#shop" class="nav-btn">Tienda</a>
        <a href="#about" class="nav-btn">Nosotros</a>
        <button class="nav-btn" onclick="toggleFavorites()">
            Favoritos
            <span class="fav-counter" id="favCounter">0</span>
        </button>
    </nav>
</header>

<main>

<section class="hero">

    <div class="hero-content">

        <span class="eyebrow">GSN / STREETWEAR</span>

        <h1>
            GOD<br>
            <span>STAYS</span><br>
            NEAR.
        </h1>

        <p class="hero-text">
            Ropa urbana sencilla, cómoda y actual.
            Diseños pensados para llevar todos los días,
            con una identidad limpia y diferente.
        </p>

        <div class="hero-actions">
            <a href="#shop" class="primary-btn">Ver colección</a>
            <a href="#about" class="secondary-btn">Conocer GSN</a>
        </div>

    </div>

    <div class="hero-visual">

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

        <div class="hero-label">
            <strong>GOD STAYS NEAR</strong>
            <small>New streetwear collection</small>
        </div>

    </div>

</section>

<section id="shop">

    <div class="section-heading">

        <div>
            <span class="eyebrow">COLECCIÓN</span>
            <h2>Descubre GSN</h2>
        </div>

        <p>
            Explora camisetas, sudaderas, pantalones y gorras.
            Pulsa sobre una prenda para ver todos sus detalles.
        </p>

    </div>

    <div class="categories">

        <button class="category active" onclick="filterProducts('all',this)">
            Todo
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

    <div class="products" id="products"></div>

</section>

<section>

    <div class="store-banner">

        <div class="store-banner-content">

            <span class="eyebrow">GOD STAYS NEAR</span>

            <h2>
                TU ESTILO.<br>
                TU FORMA.
            </h2>

            <p>
                Una colección creada con una estética urbana,
                cómoda y fácil de combinar.
            </p>

            <a href="#shop" class="primary-btn"
               style="display:inline-block;margin-top:25px;">
                Explorar ropa
            </a>

        </div>

    </div>

</section>

<section id="favoritesSection">

    <div class="section-heading">

        <div>
            <span class="eyebrow">GUARDADOS</span>
            <h2>Mis favoritos</h2>
        </div>

    </div>

    <div id="favoritesContainer"></div>

</section>

<section id="about">

    <div class="section-heading">

        <div>
            <span class="eyebrow">SOBRE GSN</span>
            <h2>Más que ropa.</h2>
        </div>

        <p>
            Una marca de streetwear con una imagen limpia,
            moderna y fácil de reconocer.
        </p>

    </div>

    <div class="about">

        <div class="about-card">

            <h3>GOD STAYS NEAR</h3>

            <p>
                GSN nace como una propuesta de ropa urbana
                con prendas sencillas y diseños que buscan
                transmitir una identidad propia.
            </p>

            <p style="margin-top:18px;">
                La colección combina tonos neutros,
                formas simples y un estilo actual.
            </p>

        </div>

        <div class="about-card logo-card">

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

    </div>

</section>

</main>

<footer>

    <div class="footer-top">

        <div class="footer-brand">

            <h3>GOD STAYS NEAR</h3>

            <p>
                Streetwear sencillo, cómodo y con identidad.
            </p>

        </div>

        <div class="footer-links">

            <a href="#shop">Tienda</a>
            <a href="#about">Nosotros</a>
            <a href="#shop">Colección</a>

        </div>

    </div>

    <div class="footer-bottom">
        © 2026 GOD STAYS NEAR · Proyecto escolar
    </div>

</footer>

<div class="modal" id="modal">

    <div class="modal-box">

        <div class="modal-image">
            <img id="modalImage" src="" alt="Producto">
        </div>

        <div class="modal-content">

            <button class="close" onclick="closeModal()">×</button>

            <div class="modal-category" id="modalCategory"></div>

            <h2 id="modalName"></h2>

            <div class="modal-price" id="modalPrice"></div>

            <p class="modal-description" id="modalDescription"></p>

            <div style="margin-top:25px;font-weight:bold;">
                Elige tu talla
            </div>

            <div class="sizes">

                <button class="size">XS</button>
                <button class="size">S</button>
                <button class="size">M</button>
                <button class="size">L</button>
                <button class="size">XL</button>

            </div>

            <button class="modal-favorite" id="modalFavorite">
                ♡ Añadir a favoritos
            </button>

        </div>

    </div>

</div>

<div class="toast" id="toast">
    Añadido a favoritos
</div>

<script>

const products = [

{
    id:1,
    name:"Oversized Essential",
    category:"camisetas",
    price:"29,99 €",
    image:"https://images.unsplash.com/photo-1521572163474-6864f9cf17ab?auto=format&fit=crop&w=1000&q=90",
    description:"Camiseta oversized de estilo sencillo y urbano. Una prenda fácil de combinar para cualquier día."
},

{
    id:2,
    name:"Minimal Logo Tee",
    category:"camisetas",
    price:"32,99 €",
    image:"https://images.unsplash.com/photo-1503341504253-dff4815485f1?auto=format&fit=crop&w=1000&q=90",
    description:"Camiseta de corte limpio con una estética minimalista inspirada en GSN."
},

{
    id:3,
    name:"GSN Black Tee",
    category:"camisetas",
    price:"34,99 €",
    image:"https://images.unsplash.com/photo-1583743814966-8936f37f4678?auto=format&fit=crop&w=1000&q=90",
    description:"Camiseta negra básica con inspiración streetwear y detalles sencillos."
},

{
    id:4,
    name:"Classic Hoodie",
    category:"sudaderas",
    price:"54,99 €",
    image:"https://images.unsplash.com/photo-1556821840-3a63f95609a7?auto=format&fit=crop&w=1000&q=90",
    description:"Sudadera cómoda para un look urbano y relajado."
},

{
    id:5,
    name:"Heavy Oversized",
    category:"sudaderas",
    price:"59,99 €",
    image:"https://images.unsplash.com/photo-1578681994506-b8f463449011?auto=format&fit=crop&w=1000&q=90",
    description:"Sudadera oversized con una silueta amplia y moderna."
},

{
    id:6,
    name:"Essential Crew",
    category:"sudaderas",
    price:"49,99 €",
    image:"https://images.unsplash.com/photo-1604644401890-0bd678c83788?auto=format&fit=crop&w=1000&q=90",
    description:"Sudadera clásica y sencilla pensada para combinar fácilmente."
},

{
    id:7,
    name:"Wide Street Pants",
    category:"pantalones",
    price:"49,99 €",
    image:"https://images.unsplash.com/photo-1624378439575-d8705ad7ae80?auto=format&fit=crop&w=1000&q=90",
    description:"Pantalón ancho con inspiración streetwear y un corte cómodo."
},

{
    id:8,
    name:"Urban Cargo",
    category:"pantalones",
    price:"54,99 €",
    image:"https://images.unsplash.com/photo-1515886657613-9f3515b0c78f?auto=format&fit=crop&w=1000&q=90",
    description:"Pantalón cargo urbano con bolsillos y diseño actual."
},

{
    id:9,
    name:"Daily Black",
    category:"pantalones",
    price:"44,99 €",
    image:"https://images.unsplash.com/photo-1551488831-00ddcb6c6bd3?auto=format&fit=crop&w=1000&q=90",
    description:"Pantalón negro sencillo para crear diferentes looks."
},

{
    id:10,
    name:"GSN Cap",
    category:"gorras",
    price:"24,99 €",
    image:"https://images.unsplash.com/photo-1588850561407-ed78c282e89b?auto=format&fit=crop&w=1000&q=90",
    description:"Gorra GSN de estilo sencillo para completar cualquier outfit."
},

{
    id:11,
    name:"Classic Cap",
    category:"gorras",
    price:"22,99 €",
    image:"https://images.unsplash.com/photo-1521369909029-2afed882baee?auto=format&fit=crop&w=1000&q=90",
    description:"Gorra clásica con una estética limpia y fácil de combinar."
},

{
    id:12,
    name:"Street GSN Cap",
    category:"gorras",
    price:"27,99 €",
    image:"https://images.unsplash.com/photo-1575428652377-a2d80e2277fc?auto=format&fit=crop&w=1000&q=90",
    description:"Gorra urbana inspirada en la identidad visual de GOD STAYS NEAR."
}

];

let favorites =
    JSON.parse(localStorage.getItem("gsnFavorites")) || [];

let currentProduct = null;

function renderProducts(list = products){

    const container = document.getElementById("products");

    container.innerHTML = "";

    list.forEach(product => {

        const isFavorite =
            favorites.includes(product.id);

        const card = document.createElement("article");

        card.className = "product";

        card.innerHTML = `

            <div
                class="product-image"
                onclick="openModal(${product.id})"
            >

                <img
                    src="${product.image}"
                    alt="${product.name}"
                    loading="lazy"
                >

                <button
                    class="favorite ${isFavorite ? "active" : ""}"
                    onclick="event.stopPropagation();toggleFavorite(${product.id})"
                    aria-label="Favorito"
                >
                    ${isFavorite ? "♥" : "♡"}
                </button>

            </div>

            <div class="product-info">

                <div class="product-category">
                    ${product.category}
                </div>

                <div class="product-name">
                    ${product.name}
                </div>

                <div class="product-bottom">

                    <div class="price">
                        ${product.price}
                    </div>

                    <button
                        class="view-product"
                        onclick="openModal(${product.id})"
                    >
                        Ver
                    </button>

                </div>

            </div>
        `;

        container.appendChild(card);

    });

}

function filterProducts(category, button){

    document
        .querySelectorAll(".category")
        .forEach(btn => btn.classList.remove("active"));

    button.classList.add("active");

    if(category === "all"){

        renderProducts(products);

    }else{

        renderProducts(
            products.filter(
                product => product.category === category
            )
        );

    }

}

function toggleFavorite(id){

    if(favorites.includes(id)){

        favorites =
            favorites.filter(
                favorite => favorite !== id
            );

        showToast("Eliminado de favoritos");

    }else{

        favorites.push(id);

        showToast("Añadido a favoritos");

    }

    localStorage.setItem(
        "gsnFavorites",
        JSON.stringify(favorites)
    );

    updateCounter();

    renderProducts();

    if(
        document
            .getElementById("favoritesSection")
            .classList.contains("show")
    ){

        renderFavorites();

    }

}

function updateCounter(){

    document.getElementById("favCounter").textContent =
        favorites.length;

}

function toggleFavorites(){

    const section =
        document.getElementById("favoritesSection");

    section.classList.toggle("show");

    if(section.classList.contains("show")){

        renderFavorites();

        section.scrollIntoView({
            behavior:"smooth"
        });

    }

}

function renderFavorites(){

    const container =
        document.getElementById("favoritesContainer");

    const favoriteProducts =
        products.filter(
            product => favorites.includes(product.id)
        );

    if(favoriteProducts.length === 0){

        container.innerHTML = `

            <div class="empty">

                <h3>No tienes favoritos todavía</h3>

                <p>
                    Pulsa el corazón de una prenda para guardarla aquí.
                </p>

            </div>

        `;

        return;

    }

    container.innerHTML = `
        <div class="products" id="favoriteProducts"></div>
    `;

    const grid =
        document.getElementById("favoriteProducts");

    favoriteProducts.forEach(product => {

        const card =
            document.createElement("article");

        card.className = "product";

        card.innerHTML = `

            <div
                class="product-image"
                onclick="openModal(${product.id})"
            >

                <img
                    src="${product.image}"
                    alt="${product.name}"
                >

                <button
                    class="favorite active"
                    onclick="event.stopPropagation();toggleFavorite(${product.id})"
                >
                    ♥
                </button>

            </div>

            <div class="product-info">

                <div class="product-category">
                    ${product.category}
                </div>

                <div class="product-name">
                    ${product.name}
                </div>

                <div class="product-bottom">

                    <div class="price">
                        ${product.price}
                    </div>

                    <button
                        class="view-product"
                        onclick="openModal(${product.id})"
                    >
                        Ver
                    </button>

                </div>

            </div>

        `;

        grid.appendChild(card);

    });

}

function openModal(id){

    const product =
        products.find(
            item => item.id === id
        );

    if(!product){
        return;
    }

    currentProduct = product;

    document.getElementById("modalImage").src =
        product.image;

    document.getElementById("modalName").textContent =
        product.name;

    document.getElementById("modalCategory").textContent =
        product.category;

    document.getElementById("modalPrice").textContent =
        product.price;

    document.getElementById("modalDescription").textContent =
        product.description;

    updateModalFavorite();

    document
        .getElementById("modal")
        .classList.add("open");

    document.body.style.overflow = "hidden";

}

function closeModal(){

    document
        .getElementById("modal")
        .classList.remove("open");

    document.body.style.overflow = "";

}

function updateModalFavorite(){

    const button =
        document.getElementById("modalFavorite");

    if(!currentProduct){
        return;
    }

    if(
        favorites.includes(currentProduct.id)
    ){

        button.textContent =
            "♥ Quitar de favoritos";

    }else{

        button.textContent =
            "♡ Añadir a favoritos";

    }

}

document
    .getElementById("modalFavorite")
    .addEventListener("click",function(){

        if(!currentProduct){
            return;
        }

        toggleFavorite(currentProduct.id);

        updateModalFavorite();

    });

document
    .querySelectorAll(".size")
    .forEach(size => {

        size.addEventListener("click",function(){

            document
                .querySelectorAll(".size")
                .forEach(item =>
                    item.classList.remove("selected")
                );

            this.classList.add("selected");

        });

    });

document
    .getElementById("modal")
    .addEventListener("click",function(event){

        if(event.target === this){

            closeModal();

        }

    });

document.addEventListener(
    "keydown",
    function(event){

        if(event.key === "Escape"){

            closeModal();

        }

    }
);

function showToast(message){

    const toast =
        document.getElementById("toast");

    toast.textContent = message;

    toast.classList.add("show");

    setTimeout(
        () => toast.classList.remove("show"),
        1800
    );

}

renderProducts();

updateCounter();

</script>

</body>
</html>
