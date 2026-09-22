<!DOCTYPE html>
<html lang="ca">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>SNG — GOD STAYS NEAR</title>

<style>

/* =========================================================
   SNG — GOD STAYS NEAR
   BOTIGA STREETWEAR
   FONS NEGRE · LLETRA BLANCA
   ========================================================= */

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
    background:#050505;
    color:#fff;
    overflow-x:hidden;
}

body.modal-open{
    overflow:hidden;
}

button,
a{
    font-family:inherit;
}

button{
    cursor:pointer;
}

a{
    color:inherit;
    text-decoration:none;
}

/* =========================================================
   CURSOR / EFECTES
   ========================================================= */

::selection{
    background:#fff;
    color:#000;
}

::-webkit-scrollbar{
    width:8px;
}

::-webkit-scrollbar-track{
    background:#050505;
}

::-webkit-scrollbar-thumb{
    background:#fff;
}

/* =========================================================
   HEADER
   ========================================================= */

header{
    position:fixed;
    top:0;
    left:0;
    width:100%;
    z-index:1000;
    background:rgba(5,5,5,.88);
    backdrop-filter:blur(18px);
    border-bottom:1px solid #222;
}

.navbar{
    width:min(1400px,92%);
    height:80px;
    margin:auto;
    display:flex;
    align-items:center;
    justify-content:space-between;
}

.logo{
    display:flex;
    align-items:center;
    gap:13px;
    font-size:25px;
    font-weight:900;
    letter-spacing:5px;
}

.logo-mark{
    width:48px;
    height:48px;
    border:2px solid #fff;
    display:flex;
    align-items:center;
    justify-content:center;
    font-weight:900;
    font-size:15px;
    transform:rotate(45deg);
}

.logo-mark span{
    transform:rotate(-45deg);
}

.logo-text{
    line-height:1;
}

.logo-text small{
    display:block;
    font-size:7px;
    letter-spacing:3px;
    margin-top:5px;
    color:#aaa;
}

nav{
    display:flex;
    gap:34px;
}

nav a{
    color:#aaa;
    font-size:11px;
    font-weight:800;
    letter-spacing:2px;
    transition:.25s;
}

nav a:hover{
    color:#fff;
}

.header-actions{
    display:flex;
    align-items:center;
    gap:10px;
}

.fav-header{
    position:relative;
    background:#111;
    border:1px solid #333;
    color:#fff;
    width:45px;
    height:45px;
    font-size:19px;
    transition:.25s;
}

.fav-header:hover{
    background:#fff;
    color:#000;
}

.fav-count{
    position:absolute;
    top:-6px;
    right:-6px;
    width:18px;
    height:18px;
    border-radius:50%;
    background:#fff;
    color:#000;
    font-size:10px;
    display:flex;
    align-items:center;
    justify-content:center;
    font-weight:bold;
}

/* =========================================================
   HERO
   ========================================================= */

.hero{
    min-height:100vh;
    padding:140px 5% 80px;
    display:grid;
    grid-template-columns:1fr 1fr;
    align-items:center;
    gap:70px;
    position:relative;
    overflow:hidden;
    background:
        radial-gradient(circle at 80% 40%,#222 0%,#050505 38%),
        #050505;
}

.hero:before{
    content:"";
    position:absolute;
    width:600px;
    height:600px;
    border:1px solid #222;
    border-radius:50%;
    right:-250px;
    top:100px;
}

.hero:after{
    content:"";
    position:absolute;
    width:400px;
    height:400px;
    border:1px solid #191919;
    border-radius:50%;
    right:-120px;
    top:200px;
}

.hero-content{
    position:relative;
    z-index:2;
}

.hero-tag{
    display:inline-flex;
    align-items:center;
    gap:10px;
    border:1px solid #444;
    padding:10px 15px;
    color:#aaa;
    font-size:10px;
    font-weight:bold;
    letter-spacing:3px;
}

.hero-tag i{
    width:6px;
    height:6px;
    background:#fff;
    border-radius:50%;
    display:block;
}

.hero h1{
    font-size:clamp(100px,16vw,230px);
    line-height:.75;
    letter-spacing:-14px;
    margin:40px 0 30px;
    font-weight:1000;
}

.hero h2{
    font-size:clamp(25px,3vw,48px);
    letter-spacing:7px;
    font-weight:900;
}

.hero p{
    max-width:570px;
    margin-top:25px;
    color:#999;
    line-height:1.8;
    font-size:15px;
}

.hero-buttons{
    display:flex;
    gap:12px;
    margin-top:35px;
}

.button{
    display:inline-flex;
    align-items:center;
    justify-content:center;
    padding:16px 25px;
    font-size:11px;
    font-weight:900;
    letter-spacing:2px;
    border:1px solid #fff;
    transition:.25s;
}

.button-white{
    background:#fff;
    color:#000;
}

.button-white:hover{
    background:#000;
    color:#fff;
}

.button-dark{
    background:#111;
    color:#fff;
    border-color:#333;
}

.button-dark:hover{
    background:#fff;
    color:#000;
}

.hero-visual{
    position:relative;
    z-index:2;
    display:flex;
    justify-content:center;
    align-items:center;
}

.hero-card{
    width:min(520px,90%);
    aspect-ratio:1/1;
    background:#111;
    border:1px solid #333;
    position:relative;
    display:flex;
    align-items:center;
    justify-content:center;
    overflow:hidden;
}

.hero-card:before{
    content:"SNG";
    position:absolute;
    font-size:180px;
    font-weight:1000;
    letter-spacing:-15px;
    color:#171717;
}

.hero-shirt{
    position:relative;
    z-index:2;
    width:55%;
    height:70%;
    background:#080808;
    clip-path:polygon(
        27% 0,
        40% 8%,
        50% 11%,
        60% 8%,
        73% 0,
        100% 18%,
        87% 35%,
        76% 28%,
        76% 100%,
        24% 100%,
        24% 28%,
        13% 35%,
        0 18%
    );
    border:1px solid #444;
    filter:drop-shadow(0 25px 35px rgba(0,0,0,.7));
}

.hero-shirt:after{
    content:"GSN";
    position:absolute;
    left:50%;
    top:48%;
    transform:translate(-50%,-50%);
    color:#fff;
    font-size:34px;
    font-weight:1000;
    letter-spacing:-2px;
}

.hero-label{
    position:absolute;
    bottom:25px;
    left:25px;
    font-size:10px;
    letter-spacing:3px;
    color:#777;
}

/* =========================================================
   MARQUEE
   ========================================================= */

.marquee{
    background:#fff;
    color:#000;
    overflow:hidden;
    white-space:nowrap;
    padding:16px 0;
    border-top:1px solid #fff;
    border-bottom:1px solid #fff;
}

.marquee-track{
    display:inline-block;
    animation:move 20s linear infinite;
}

.marquee span{
    margin:0 35px;
    font-size:13px;
    font-weight:1000;
    letter-spacing:4px;
}

@keyframes move{
    from{
        transform:translateX(0);
    }

    to{
        transform:translateX(-50%);
    }
}

/* =========================================================
   SECCIONS
   ========================================================= */

section{
    padding:110px 5%;
}

.section-head{
    width:min(1400px,100%);
    margin:0 auto 50px;
    display:flex;
    align-items:end;
    justify-content:space-between;
    gap:30px;
}

.section-number{
    color:#666;
    font-size:11px;
    letter-spacing:3px;
    font-weight:bold;
}

.section-head h2{
    font-size:clamp(45px,7vw,90px);
    line-height:.9;
    letter-spacing:-5px;
}

.section-head p{
    max-width:400px;
    color:#777;
    line-height:1.6;
    font-size:13px;
}

/* =========================================================
   CATEGORIES
   ========================================================= */

.categories{
    width:min(1400px,100%);
    margin:auto;
    display:grid;
    grid-template-columns:repeat(4,1fr);
    gap:12px;
}

.category{
    min-height:240px;
    border:1px solid #282828;
    background:#0c0c0c;
    padding:25px;
    display:flex;
    flex-direction:column;
    justify-content:space-between;
    transition:.35s;
    position:relative;
    overflow:hidden;
}

.category:after{
    content:"";
    position:absolute;
    width:150px;
    height:150px;
    border:1px solid #222;
    border-radius:50%;
    right:-60px;
    bottom:-60px;
}

.category:hover{
    background:#fff;
    color:#000;
    transform:translateY(-8px);
}

.category span{
    font-size:10px;
    letter-spacing:3px;
    color:#777;
    font-weight:bold;
}

.category h3{
    font-size:30px;
    position:relative;
    z-index:2;
}

.category:hover span{
    color:#555;
}

/* =========================================================
   PRODUCTES
   ========================================================= */

.shop{
    background:#080808;
}

.filters{
    width:min(1400px,100%);
    margin:0 auto 30px;
    display:flex;
    flex-wrap:wrap;
    gap:8px;
}

.filter{
    background:#111;
    border:1px solid #333;
    color:#888;
    padding:12px 18px;
    font-size:10px;
    font-weight:bold;
    letter-spacing:2px;
    transition:.2s;
}

.filter:hover,
.filter.active{
    background:#fff;
    color:#000;
    border-color:#fff;
}

.products{
    width:min(1400px,100%);
    margin:auto;
    display:grid;
    grid-template-columns:repeat(4,1fr);
    gap:14px;
}

.product{
    background:#0e0e0e;
    border:1px solid #242424;
    transition:.3s;
    position:relative;
    overflow:hidden;
}

.product:hover{
    border-color:#666;
    transform:translateY(-5px);
}

.product-image{
    height:430px;
    background:
        radial-gradient(circle at center,#202020 0%,#0b0b0b 65%);
    position:relative;
    display:flex;
    align-items:center;
    justify-content:center;
    overflow:hidden;
    cursor:pointer;
}

.product-image:before{
    content:"VIEW";
    position:absolute;
    top:15px;
    right:15px;
    font-size:9px;
    letter-spacing:2px;
    color:#777;
    z-index:10;
}

.garment{
    width:62%;
    height:75%;
    position:relative;
    transition:.35s;
    filter:drop-shadow(0 25px 20px rgba(0,0,0,.7));
}

.product:hover .garment{
    transform:scale(1.06);
}

/* SAMARRETA */

.tshirt{
    background:#111;
    clip-path:polygon(
        28% 0,
        42% 7%,
        50% 10%,
        58% 7%,
        72% 0,
        100% 18%,
        86% 36%,
        75% 29%,
        75% 100%,
        25% 100%,
        25% 29%,
        14% 36%,
        0 18%
    );
}

/* SAMARRETA BLANCA */

.tshirt.white{
    background:#f5f5f5;
}

/* SUDADERA */

.hoodie{
    width:65%;
    height:78%;
    background:#101010;
    clip-path:polygon(
        32% 7%,
        39% 0,
        50% 8%,
        61% 0,
        68% 7%,
        88% 17%,
        100% 36%,
        88% 45%,
        78% 34%,
        78% 100%,
        22% 100%,
        22% 34%,
        12% 45%,
        0 36%,
        12% 17%
    );
}

.hoodie.grey{
    background:#777;
}

.hoodie.white{
    background:#ddd;
}

/* PANTALONS */

.pants{
    width:57%;
    height:80%;
    background:#101010;
    clip-path:polygon(
        12% 0,
        88% 0,
        75% 45%,
        72% 100%,
        53% 100%,
        50% 55%,
        47% 100%,
        28% 100%,
        25% 45%
    );
}

.pants.grey{
    background:#777;
}

.pants.white{
    background:#ddd;
}

/* GORRA */

.cap{
    width:70%;
    height:42%;
    background:#111;
    border-radius:70% 70% 25% 25%;
    position:relative;
    margin-top:50px;
}

.cap:after{
    content:"";
    position:absolute;
    width:65%;
    height:25%;
    background:#111;
    right:-35%;
    bottom:-7%;
    border-radius:0 100% 100% 0;
    transform:rotate(7deg);
}

/* LOGO EN PRENDES */

.garment-logo{
    position:absolute;
    top:46%;
    left:50%;
    transform:translate(-50%,-50%);
    color:#fff;
    font-weight:1000;
    font-size:27px;
    letter-spacing:-2px;
    text-align:center;
    z-index:4;
}

.white .garment-logo{
    color:#000;
}

.garment-logo small{
    display:block;
    font-size:5px;
    letter-spacing:2px;
    margin-top:5px;
}

.product-info{
    padding:20px;
    border-top:1px solid #242424;
}

.product-top{
    display:flex;
    justify-content:space-between;
    gap:15px;
}

.product-info h3{
    font-size:16px;
    margin-bottom:7px;
}

.product-category{
    color:#666;
    font-size:9px;
    letter-spacing:2px;
    font-weight:bold;
}

.product-price{
    font-size:16px;
    font-weight:900;
}

.product-info p{
    color:#777;
    font-size:12px;
    line-height:1.5;
    margin-top:10px;
}

.product-actions{
    display:flex;
    gap:8px;
    margin-top:17px;
}

.view-product{
    flex:1;
    background:#fff;
    color:#000;
    border:1px solid #fff;
    padding:13px;
    font-size:10px;
    font-weight:bold;
    letter-spacing:1px;
}

.favorite{
    width:45px;
    background:#111;
    color:#fff;
    border:1px solid #333;
    font-size:18px;
    transition:.2s;
}

.favorite:hover,
.favorite.selected{
    background:#fff;
    color:#000;
}

.favorite.selected{
    color:#000;
}

/* =========================================================
   DESTACAT
   ========================================================= */

.feature{
    width:min(1400px,100%);
    margin:auto;
    display:grid;
    grid-template-columns:1fr 1fr;
    min-height:600px;
    border:1px solid #292929;
}

.feature-visual{
    background:#111;
    display:flex;
    align-items:center;
    justify-content:center;
    position:relative;
    overflow:hidden;
}

.feature-visual:before{
    content:"GSN";
    position:absolute;
    font-size:200px;
    color:#171717;
    font-weight:1000;
}

.feature-hoodie{
    width:55%;
    height:72%;
    background:#e5e5e5;
    clip-path:polygon(
        32% 7%,
        39% 0,
        50% 8%,
        61% 0,
        68% 7%,
        88% 17%,
        100% 36%,
        88% 45%,
        78% 34%,
        78% 100%,
        22% 100%,
        22% 34%,
        12% 45%,
        0 36%,
        12% 17%
    );
    position:relative;
    z-index:2;
    filter:drop-shadow(0 30px 30px #000);
}

.feature-hoodie:after{
    content:"GSN";
    color:#000;
    position:absolute;
    top:48%;
    left:50%;
    transform:translate(-50%,-50%);
    font-size:40px;
    font-weight:1000;
}

.feature-content{
    padding:70px;
    display:flex;
    flex-direction:column;
    justify-content:center;
    background:#f5f5f5;
    color:#000;
}

.feature-content small{
    font-size:10px;
    letter-spacing:3px;
    color:#777;
}

.feature-content h2{
    font-size:70px;
    line-height:.85;
    letter-spacing:-5px;
    margin:25px 0;
}

.feature-content p{
    color:#555;
    line-height:1.7;
    max-width:480px;
}

.feature-price{
    font-size:30px;
    font-weight:900;
    margin:25px 0;
}

/* =========================================================
   NOSALTRES
   ========================================================= */

.about{
    width:min(1400px,100%);
    margin:auto;
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:70px;
    align-items:center;
}

.about h2{
    font-size:clamp(55px,8vw,100px);
    line-height:.85;
    letter-spacing:-6px;
}

.about p{
    color:#888;
    line-height:1.8;
    max-width:550px;
    margin-top:30px;
}

.about-grid{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:10px;
    margin-top:35px;
}

.about-box{
    border:1px solid #282828;
    padding:25px;
    background:#0c0c0c;
}

.about-box strong{
    display:block;
    font-size:25px;
    margin-bottom:8px;
}

.about-box span{
    color:#666;
    font-size:10px;
    letter-spacing:2px;
}

/* =========================================================
   NEWSLETTER
   ========================================================= */

.newsletter{
    background:#fff;
    color:#000;
    text-align:center;
}

.newsletter h2{
    font-size:clamp(40px,7vw,80px);
    letter-spacing:-4px;
}

.newsletter p{
    color:#555;
    margin:15px 0 30px;
}

.newsletter form{
    width:min(550px,100%);
    margin:auto;
    display:flex;
}

.newsletter input{
    flex:1;
    border:1px solid #000;
    background:#fff;
    color:#000;
    padding:17px;
    outline:none;
}

.newsletter button{
    background:#000;
    color:#fff;
    border:1px solid #000;
    padding:0 25px;
    font-weight:bold;
}

/* =========================================================
   FOOTER
   ========================================================= */

footer{
    padding:70px 5% 25px;
    border-top:1px solid #222;
}

.footer-grid{
    width:min(1400px,100%);
    margin:auto;
    display:grid;
    grid-template-columns:2fr 1fr 1fr 1fr;
    gap:50px;
}

.footer-brand h2{
    font-size:60px;
    letter-spacing:-5px;
}

.footer-brand p{
    color:#666;
    max-width:300px;
    line-height:1.7;
    margin-top:15px;
}

.footer-column h3{
    font-size:10px;
    letter-spacing:2px;
    margin-bottom:20px;
}

.footer-column a{
    display:block;
    color:#666;
    font-size:12px;
    margin:11px 0;
}

.footer-column a:hover{
    color:#fff;
}

.footer-bottom{
    width:min(1400px,100%);
    margin:60px auto 0;
    padding-top:20px;
    border-top:1px solid #222;
    display:flex;
    justify-content:space-between;
    color:#555;
    font-size:10px;
}

/* =========================================================
   MODAL PRODUCTE
   ========================================================= */

.modal{
    position:fixed;
    inset:0;
    background:rgba(0,0,0,.85);
    backdrop-filter:blur(12px);
    z-index:5000;
    display:none;
    align-items:center;
    justify-content:center;
    padding:25px;
}

.modal.active{
    display:flex;
}

.modal-box{
    width:min(1050px,100%);
    max-height:90vh;
    overflow:auto;
    background:#0d0d0d;
    border:1px solid #333;
    display:grid;
    grid-template-columns:1fr 1fr;
    position:relative;
}

.modal-close{
    position:absolute;
    right:15px;
    top:15px;
    width:42px;
    height:42px;
    background:#000;
    color:#fff;
    border:1px solid #444;
    z-index:5;
    font-size:18px;
}

.modal-image{
    min-height:600px;
    background:#151515;
    display:flex;
    justify-content:center;
    align-items:center;
    position:relative;
}

.modal-garment{
    width:55%;
    height:70%;
    position:relative;
    filter:drop-shadow(0 30px 25px #000);
}

.modal-info{
    padding:65px 50px;
}

.modal-category{
    color:#666;
    font-size:10px;
    letter-spacing:3px;
    font-weight:bold;
}

.modal-info h2{
    font-size:50px;
    line-height:.9;
    letter-spacing:-3px;
    margin:15px 0;
}

.modal-description{
    color:#777;
    line-height:1.7;
    margin:20px 0;
}

.modal-price{
    font-size:30px;
    font-weight:900;
    margin:20px 0 30px;
}

.size-title{
    font-size:11px;
    font-weight:bold;
    letter-spacing:2px;
    margin-bottom:10px;
}

.sizes{
    display:flex;
    gap:8px;
    flex-wrap:wrap;
}

.size{
    width:52px;
    height:45px;
    background:#111;
    border:1px solid #333;
    color:#fff;
    font-weight:bold;
}

.size:hover,
.size.selected{
    background:#fff;
    color:#000;
}

.modal-fav{
    width:100%;
    margin-top:25px;
    padding:17px;
    background:#fff;
    color:#000;
    border:0;
    font-weight:bold;
    letter-spacing:2px;
}

.info-list{
    border-top:1px solid #292929;
    margin-top:30px;
}

.info-row{
    padding:14px 0;
    border-bottom:1px solid #222;
    display:flex;
    justify-content:space-between;
    color:#777;
    font-size:12px;
}

.info-row strong{
    color:#fff;
}

/* =========================================================
   FAVORITOS
   ========================================================= */

.favorites-panel{
    position:fixed;
    right:-430px;
    top:0;
    width:430px;
    max-width:100%;
    height:100vh;
    background:#0b0b0b;
    z-index:4000;
    border-left:1px solid #333;
    transition:.3s;
    display:flex;
    flex-direction:column;
}

.favorites-panel.open{
    right:0;
}

.favorites-header{
    height:80px;
    padding:20px;
    border-bottom:1px solid #292929;
    display:flex;
    align-items:center;
    justify-content:space-between;
}

.favorites-header h2{
    font-size:18px;
}

.close-favorites{
    background:#111;
    border:1px solid #333;
    color:#fff;
    width:40px;
    height:40px;
}

.favorite-list{
    flex:1;
    overflow:auto;
    padding:20px;
}

.empty-favorites{
    text-align:center;
    color:#555;
    padding-top:80px;
    line-height:1.7;
}

.favorite-item{
    display:grid;
    grid-template-columns:90px 1fr auto;
    gap:15px;
    padding:15px 0;
    border-bottom:1px solid #222;
    align-items:center;
}

.mini-garment{
    width:90px;
    height:100px;
    background:#111;
    display:flex;
    align-items:center;
    justify-content:center;
    color:#fff;
    font-weight:1000;
    font-size:20px;
}

.favorite-item h4{
    font-size:13px;
    margin-bottom:6px;
}

.favorite-item p{
    color:#666;
    font-size:11px;
}

.remove-fav{
    background:none;
    border:0;
    color:#777;
    font-size:18px;
}

.remove-fav:hover{
    color:#fff;
}

/* =========================================================
   TOAST
   ========================================================= */

.toast{
    position:fixed;
    bottom:25px;
    left:50%;
    transform:translate(-50%,20px);
    background:#fff;
    color:#000;
    padding:15px 25px;
    font-size:11px;
    font-weight:bold;
    letter-spacing:1px;
    opacity:0;
    pointer-events:none;
    z-index:9000;
    transition:.3s;
}

.toast.show{
    opacity:1;
    transform:translate(-50%,0);
}

/* =========================================================
   RESPONSIVE
   ========================================================= */

@media(max-width:1000px){

    nav{
        display:none;
    }

    .hero{
        grid-template-columns:1fr;
    }

    .hero-content{
        text-align:center;
    }

    .hero p{
        margin-left:auto;
        margin-right:auto;
    }

    .hero-buttons{
        justify-content:center;
    }

    .categories{
        grid-template-columns:repeat(2,1fr);
    }

    .products{
        grid-template-columns:repeat(2,1fr);
    }

    .feature{
        grid-template-columns:1fr;
    }

    .feature-visual{
        min-height:500px;
    }

    .about{
        grid-template-columns:1fr;
    }

    .footer-grid{
        grid-template-columns:1fr 1fr;
    }
}

@media(max-width:650px){

    .navbar{
        height:68px;
    }

    .logo-text{
        display:none;
    }

    .hero{
        padding-top:120px;
        padding-left:20px;
        padding-right:20px;
    }

    .hero h1{
        font-size:95px;
        letter-spacing:-8px;
    }

    .hero-buttons{
        flex-direction:column;
    }

    .categories,
    .products{
        grid-template-columns:1fr;
    }

    section{
        padding:75px 20px;
    }

    .section-head{
        display:block;
    }

    .section-head p{
        margin-top:20px;
    }

    .product-image{
        height:390px;
    }

    .feature-content{
        padding:45px 25px;
    }

    .feature-content h2{
        font-size:55px;
    }

    .about-grid{
        grid-template-columns:1fr;
    }

    .newsletter form{
        flex-direction:column;
        gap:8px;
    }

    .newsletter button{
        padding:17px;
    }

    .footer-grid{
        grid-template-columns:1fr;
    }

    .footer-bottom{
        display:block;
        line-height:2;
    }

    .modal{
        padding:0;
    }

    .modal-box{
        max-height:100vh;
        height:100vh;
        grid-template-columns:1fr;
        overflow:auto;
    }

    .modal-image{
        min-height:430px;
    }

    .modal-info{
        padding:35px 25px;
    }

    .modal-info h2{
        font-size:40px;
    }

    .favorites-panel{
        width:100%;
    }
}

</style>
</head>

<body>

<!-- =========================================================
     HEADER
     ========================================================= -->

<header>

<div class="navbar">

<a href="#inicio" class="logo">

<div class="logo-mark">
<span>GSN</span>
</div>

<div class="logo-text">
SNG
<small>GOD STAYS NEAR</small>
</div>

</a>

<nav>

<a href="#inicio">INICI</a>
<a href="#categories">CATEGORIES</a>
<a href="#catalog">BOTIGA</a>
<a href="#nosaltres">NOSALTRES</a>
<a href="#contacte">CONTACTE</a>

</nav>

<div class="header-actions">

<button class="fav-header" onclick="openFavorites()">

♡

<span class="fav-count" id="favCount">0</span>

</button>

</div>

</div>

</header>


<!-- =========================================================
     HERO
     ========================================================= -->

<section class="hero" id="inicio">

<div class="hero-content">

<div class="hero-tag">
<i></i>
NOVA COL·LECCIÓ 2026
</div>

<h1>SNG</h1>

<h2>GOD STAYS NEAR</h2>

<p>
Roba urbana amb una estètica simple, moderna i fàcil de reconèixer.
Peces creades per combinar el blanc, el negre i l'estil streetwear.
</p>

<div class="hero-buttons">

<a href="#catalog" class="button button-white">
EXPLORAR COL·LECCIÓ
</a>

<a href="#nosaltres" class="button button-dark">
DESCOBREIX SNG
</a>

</div>

</div>


<div class="hero-visual">

<div class="hero-card">

<div class="hero-shirt">

<div class="garment-logo">
GSN
<small>GOD STAYS NEAR</small>
</div>

</div>

<div class="hero-label">
SNG / 001 / ESSENTIAL
</div>

</div>

</div>

</section>


<!-- =========================================================
     MARQUEE
     ========================================================= -->

<div class="marquee">

<div class="marquee-track">

<span>SNG</span>
<span>GOD STAYS NEAR</span>
<span>STREETWEAR</span>
<span>NEW COLLECTION</span>
<span>SNG</span>
<span>GOD STAYS NEAR</span>
<span>STREETWEAR</span>
<span>NEW COLLECTION</span>

</div>

</div>


<!-- =========================================================
     CATEGORIES
     ========================================================= -->

<section id="categories">

<div class="section-head">

<div>

<div class="section-number">01 / CATEGORIES</div>

<h2>EXPLORA</h2>

</div>

<p>
Descobreix les diferents peces de la col·lecció SNG.
Fes clic en una categoria per veure els models.
</p>

</div>


<div class="categories">

<a href="#catalog"
class="category"
onclick="filterProducts('samarretes')">

<span>01</span>

<h3>SAMARRETES</h3>

<span>EXPLORAR →</span>

</a>


<a href="#catalog"
class="category"
onclick="filterProducts('dessuadores')">

<span>02</span>

<h3>DESSUADORES</h3>

<span>EXPLORAR →</span>

</a>


<a href="#catalog"
class="category"
onclick="filterProducts('pantalons')">

<span>03</span>

<h3>PANTALONS</h3>

<span>EXPLORAR →</span>

</a>


<a href="#catalog"
class="category"
onclick="filterProducts('gorres')">

<span>04</span>

<h3>GORRES</h3>

<span>EXPLORAR →</span>

</a>

</div>

</section>


<!-- =========================================================
     BOTIGA
     ========================================================= -->

<section class="shop" id="catalog">

<div class="section-head">

<div>

<div class="section-number">02 / SNG SHOP</div>

<h2>COL·LECCIÓ</h2>

</div>

<p>
Clica sobre qualsevol peça per veure les talles,
informació i característiques.
</p>

</div>


<div class="filters">

<button class="filter active"
onclick="filterProducts('tots',this)">
TOTS
</button>

<button class="filter"
onclick="filterProducts('samarretes',this)">
SAMARRETES
</button>

<button class="filter"
onclick="filterProducts('dessuadores',this)">
DESSUADORES
</button>

<button class="filter"
onclick="filterProducts('pantalons',this)">
PANTALONS
</button>

<button class="filter"
onclick="filterProducts('gorres',this)">
GORRES
</button>

</div>


<div class="products" id="products">


<!-- PRODUCTE 1 -->

<div class="product"
data-category="samarretes"
data-id="1">

<div class="product-image"
onclick="openProduct(1)">

<div class="garment tshirt">

<div class="garment-logo">
GSN
<small>GOD STAYS NEAR</small>
</div>

</div>

</div>

<div class="product-info">

<div class="product-top">

<div>

<div class="product-category">
SAMARRETA
</div>

<h3>Essential Black</h3>

</div>

<div class="product-price">
20 €
</div>

</div>

<p>
Samarreta negra de tall ample amb logo frontal.
</p>

<div class="product-actions">

<button class="view-product"
onclick="openProduct(1)">
VEURE PEÇA
</button>

<button class="favorite"
id="fav-1"
onclick="toggleFavorite(event,1)">
♡
</button>

</div>

</div>

</div>


<!-- PRODUCTE 2 -->

<div class="product"
data-category="samarretes"
data-id="2">

<div class="product-image"
onclick="openProduct(2)">

<div class="garment tshirt white">

<div class="garment-logo">
GSN
<small>GOD STAYS NEAR</small>
</div>

</div>

</div>

<div class="product-info">

<div class="product-top">

<div>

<div class="product-category">
SAMARRETA
</div>

<h3>Essential White</h3>

</div>

<div class="product-price">
20 €
</div>

</div>

<p>
Samarreta blanca minimalista amb logo SNG.
</p>

<div class="product-actions">

<button class="view-product"
onclick="openProduct(2)">
VEURE PEÇA
</button>

<button class="favorite"
id="fav-2"
onclick="toggleFavorite(event,2)">
♡
</button>

</div>

</div>

</div>


<!-- PRODUCTE 3 -->

<div class="product"
data-category="samarretes"
data-id="3">

<div class="product-image"
onclick="openProduct(3)">

<div class="garment tshirt">

<div class="garment-logo">
GSN
<small>GOD STAYS NEAR</small>
</div>

</div>

</div>

<div class="product-info">

<div class="product-top">

<div>

<div class="product-category">
SAMARRETA
</div>

<h3>Logo Back</h3>

</div>

<div class="product-price">
23 €
</div>

</div>

<p>
Disseny amb logo gran a la part posterior.
</p>

<div class="product-actions">

<button class="view-product"
onclick="openProduct(3)">
VEURE PEÇA
</button>

<button class="favorite"
id="fav-3"
onclick="toggleFavorite(event,3)">
♡
</button>

</div>

</div>

</div>


<!-- PRODUCTE 4 -->

<div class="product"
data-category="samarretes"
data-id="4">

<div class="product-image"
onclick="openProduct(4)">

<div class="garment tshirt white">

<div class="garment-logo">
GSN
<small>GOD STAYS NEAR</small>
</div>

</div>

</div>

<div class="product-info">

<div class="product-top">

<div>

<div class="product-category">
SAMARRETA
</div>

<h3>Cross Edition</h3>

</div>

<div class="product-price">
24 €
</div>

</div>

<p>
Model especial amb gràfic central.
</p>

<div class="product-actions">

<button class="view-product"
onclick="openProduct(4)">
VEURE PEÇA
</button>

<button class="favorite"
id="fav-4"
onclick="toggleFavorite(event,4)">
♡
</button>

</div>

</div>

</div>


<!-- PRODUCTE 5 -->

<div class="product"
data-category="dessuadores"
data-id="5">

<div class="product-image"
onclick="openProduct(5)">

<div class="garment hoodie">

<div class="garment-logo">
GSN
<small>GOD STAYS NEAR</small>
</div>

</div>

</div>

<div class="product-info">

<div class="product-top">

<div>

<div class="product-category">
DESSUADORA
</div>

<h3>Black Hoodie</h3>

</div>

<div class="product-price">
40 €
</div>

</div>

<p>
Dessuadora negra amb caputxa i logo frontal.
</p>

<div class="product-actions">

<button class="view-product"
onclick="openProduct(5)">
VEURE PEÇA
</button>

<button class="favorite"
id="fav-5"
onclick="toggleFavorite(event,5)">
♡
</button>

</div>

</div>

</div>


<!-- PRODUCTE 6 -->

<div class="product"
data-category="dessuadores"
data-id="6">

<div class="product-image"
onclick="openProduct(6)">

<div class="garment hoodie grey">

<div class="garment-logo">
GSN
<small>GOD STAYS NEAR</small>
</div>

</div>

</div>

<div class="product-info">

<div class="product-top">

<div>

<div class="product-category">
DESSUADORA
</div>

<h3>Grey Essential</h3>

</div>

<div class="product-price">
42 €
</div>

</div>

<p>
Dessuadora gris amb disseny minimalista.
</p>

<div class="product-actions">

<button class="view-product"
onclick="openProduct(6)">
VEURE PEÇA
</button>

<button class="favorite"
id="fav-6"
onclick="toggleFavorite(event,6)">
♡
</button>

</div>

</div>

</div>


<!-- PRODUCTE 7 -->

<div class="product"
data-category="dessuadores"
data-id="7">

<div class="product-image"
onclick="openProduct(7)">

<div class="garment hoodie white">

<div class="garment-logo">
GSN
<small>GOD STAYS NEAR</small>
</div>

</div>

</div>

<div class="product-info">

<div class="product-top">

<div>

<div class="product-category">
DESSUADORA
</div>

<h3>White Edition</h3>

</div>

<div class="product-price">
42 €
</div>

</div>

<p>
Dessuadora clara per a un look més net.
</p>

<div class="product-actions">

<button class="view-product"
onclick="openProduct(7)">
VEURE PEÇA
</button>

<button class="favorite"
id="fav-7"
onclick="toggleFavorite(event,7)">
♡
</button>

</div>

</div>

</div>


<!-- PRODUCTE 8 -->

<div class="product"
data-category="dessuadores"
data-id="8">

<div class="product-image"
onclick="openProduct(8)">

<div class="garment hoodie">

<div class="garment-logo">
GSN
<small>GOD STAYS NEAR</small>
</div>

</div>

</div>

<div class="product-info">

<div class="product-top">

<div>

<div class="product-category">
DESSUADORA
</div>

<h3>Limited GSN</h3>

</div>

<div class="product-price">
45 €
</div>

</div>

<p>
Model especial de la col·lecció SNG.
</p>

<div class="product-actions">

<button class="view-product"
onclick="openProduct(8)">
VEURE PEÇA
</button>

<button class="favorite"
id="fav-8"
onclick="toggleFavorite(event,8)">
♡
</button>

</div>

</div>

</div>


<!-- PRODUCTE 9 -->

<div class="product"
data-category="pantalons"
data-id="9">

<div class="product-image"
onclick="openProduct(9)">

<div class="garment pants">

<div class="garment-logo">
GSN
</div>

</div>

</div>

<div class="product-info">

<div class="product-top">

<div>

<div class="product-category">
PANTALONS
</div>

<h3>Black Cargo</h3>

</div>

<div class="product-price">
38 €
</div>

</div>

<p>
Pantaló ample amb estil cargo urbà.
</p>

<div class="product-actions">

<button class="view-product"
onclick="openProduct(9)">
VEURE PEÇA
</button>

<button class="favorite"
id="fav-9"
onclick="toggleFavorite(event,9)">
♡
</button>

</div>

</div>

</div>


<!-- PRODUCTE 10 -->

<div class="product"
data-category="pantalons"
data-id="10">

<div class="product-image"
onclick="openProduct(10)">

<div class="garment pants grey">

<div class="garment-logo">
GSN
</div>

</div>

</div>

<div class="product-info">

<div class="product-top">

<div>

<div class="product-category">
PANTALONS
</div>

<h3>Grey Wide</h3>

</div>

<div class="product-price">
36 €
</div>

</div>

<p>
Pantaló gris de tall ample i còmode.
</p>

<div class="product-actions">

<button class="view-product"
onclick="openProduct(10)">
VEURE PEÇA
</button>

<button class="favorite"
id="fav-10"
onclick="toggleFavorite(event,10)">
♡
</button>

</div>

</div>

</div>


<!-- PRODUCTE 11 -->

<div class="product"
data-category="pantalons"
data-id="11">

<div class="product-image"
onclick="openProduct(11)">

<div class="garment pants white">

<div class="garment-logo">
GSN
</div>

</div>

</div>

<div class="product-info">

<div class="product-top">

<div>

<div class="product-category">
PANTALONS
</div>

<h3>Light Edition</h3>

</div>

<div class="product-price">
36 €
</div>

</div>

<p>
Pantaló clar per combinar amb dessuadores.
</p>

<div class="product-actions">

<button class="view-product"
onclick="openProduct(11)">
VEURE PEÇA
</button>

<button class="favorite"
id="fav-11"
onclick="toggleFavorite(event,11)">
♡
</button>

</div>

</div>

</div>


<!-- PRODUCTE 12 -->

<div class="product"
data-category="pantalons"
data-id="12">

<div class="product-image"
onclick="openProduct(12)">

<div class="garment pants">

<div class="garment-logo">
GSN
</div>

</div>

</div>

<div class="product-info">

<div class="product-top">

<div>

<div class="product-category">
PANTALONS
</div>

<h3>Street Black</h3>

</div>

<div class="product-price">
40 €
</div>

</div>

<p>
Pantaló negre inspirat en l'estil streetwear.
</p>

<div class="product-actions">

<button class="view-product"
onclick="openProduct(12)">
VEURE PEÇA
</button>

<button class="favorite"
id="fav-12"
onclick="toggleFavorite(event,12)">
♡
</button>

</div>

</div>

</div>


<!-- PRODUCTE 13 -->

<div class="product"
data-category="gorres"
data-id="13">

<div class="product-image"
onclick="openProduct(13)">

<div class="garment cap">

<div class="garment-logo">
GSN
</div>

</div>

</div>

<div class="product-info">

<div class="product-top">

<div>

<div class="product-category">
GORRA
</div>

<h3>Classic Cap</h3>

</div>

<div class="product-price">
18 €
</div>

</div>

<p>
Gorra negra amb logo brodat.
</p>

<div class="product-actions">

<button class="view-product"
onclick="openProduct(13)">
VEURE PEÇA
</button>

<button class="favorite"
id="fav-13"
onclick="toggleFavorite(event,13)">
♡
</button>

</div>

</div>

</div>


<!-- PRODUCTE 14 -->

<div class="product"
data-category="gorres"
data-id="14">

<div class="product-image"
onclick="openProduct(14)">

<div class="garment cap" style="background:#ddd;color:#000;">

<div class="garment-logo" style="color:#000;">
GSN
</div>

</div>

</div>

<div class="product-info">

<div class="product-top">

<div>

<div class="product-category">
GORRA
</div>

<h3>White Cap</h3>

</div>

<div class="product-price">
18 €
</div>

</div>

<p>
Gorra clara amb un disseny minimalista.
</p>

<div class="product-actions">

<button class="view-product"
onclick="openProduct(14)">
VEURE PEÇA
</button>

<button class="favorite"
id="fav-14"
onclick="toggleFavorite(event,14)">
♡
</button>

</div>

</div>

</div>


<!-- PRODUCTE 15 -->

<div class="product"
data-category="gorres"
data-id="15">

<div class="product-image"
onclick="openProduct(15)">

<div class="garment cap" style="background:#555;">

<div class="garment-logo">
GSN
</div>

</div>

</div>

<div class="product-info">

<div class="product-top">

<div>

<div class="product-category">
GORRA
</div>

<h3>Grey GSN</h3>

</div>

<div class="product-price">
20 €
</div>

</div>

<p>
Gorra gris per completar el look.
</p>

<div class="product-actions">

<button class="view-product"
onclick="openProduct(15)">
VEURE PEÇA
</button>

<button class="favorite"
id="fav-15"
onclick="toggleFavorite(event,15)">
♡
</button>

</div>

</div>

</div>


<!-- PRODUCTE 16 -->

<div class="product"
data-category="gorres"
data-id="16">

<div class="product-image"
onclick="openProduct(16)">

<div class="garment cap">

<div class="garment-logo">
GSN
</div>

</div>

</div>

<div class="product-info">

<div class="product-top">

<div>

<div class="product-category">
GORRA
</div>

<h3>Limited Cap</h3>

</div>

<div class="product-price">
22 €
</div>

</div>

<p>
Edició limitada amb el logo GSN.
</p>

<div class="product-actions">

<button class="view-product"
onclick="openProduct(16)">
VEURE PEÇA
</button>

<button class="favorite"
id="fav-16"
onclick="toggleFavorite(event,16)">
♡
</button>

</div>

</div>

</div>


</div>

</section>


<!-- =========================================================
     PRODUCTE DESTACAT
     ========================================================= -->

<section>

<div class="section-head">

<div>

<div class="section-number">03 / DESTACAT</div>

<h2>LIMITED</h2>

</div>

</div>


<div class="feature">

<div class="feature-visual">

<div class="feature-hoodie"></div>

</div>


<div class="feature-content">

<small>SNG LIMITED COLLECTION</small>

<h2>GOD<br>STAYS<br>NEAR.</h2>

<p>
Una dessuadora especial de la col·lecció.
Disseny net, colors neutres i el logo GSN com a element principal.
</p>

<div class="feature-price">
45 €
</div>

<button class="button button-white"
onclick="openProduct(8)">
VEURE DESSUADORA
</button>

</div>

</div>

</section>


<!-- =========================================================
     NOSALTRES
     ========================================================= -->

<section id="nosaltres">

<div class="about">

<div>

<div class="section-number">
04 / NOSALTRES
</div>

<h2>
SIMPLE.<br>
URBÀ.<br>
SNG.
</h2>

<p>
SNG és una marca de roba urbana creada amb la idea de fer peces
modernes, fàcils de combinar i amb una identitat pròpia.
El blanc i el negre són la base de la nostra estètica.
</p>

</div>


<div class="about-grid">

<div class="about-box">

<strong>01</strong>

<span>
DISSENYS MODERNS
</span>

</div>

<div class="about-box">

<strong>02</strong>

<span>
ESTIL URBÀ
</span>

</div>

<div class="about-box">

<strong>03</strong>

<span>
COL·LECCIONS LIMITADES
</span>

</div>

<div class="about-box">

<strong>04</strong>

<span>
IDENTITAT PRÒPIA
</span>

</div>

</div>

</div>

</section>


<!-- =========================================================
     NEWSLETTER
     ========================================================= -->

<section class="newsletter" id="contacte">

<h2>
FORMA PART DE SNG
</h2>

<p>
Rep informació sobre noves peces i col·leccions.
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


<!-- =========================================================
     FOOTER
     ========================================================= -->

<footer>

<div class="footer-grid">

<div class="footer-brand">

<h2>SNG</h2>

<p>
GOD STAYS NEAR.
Streetwear amb una identitat simple,
moderna i urbana.
</p>

</div>


<div class="footer-column">

<h3>BOTIGA</h3>

<a href="#catalog">Col·lecció</a>
<a href="#catalog">Samarretes</a>
<a href="#catalog">Dessuadores</a>
<a href="#catalog">Pantalons</a>
<a href="#catalog">Gorres</a>

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


<!-- =========================================================
     MODAL PRODUCTE
     ========================================================= -->

<div class="modal" id="productModal">

<div class="modal-box">

<button class="modal-close"
onclick="closeProduct()">
✕
</button>


<div class="modal-image">

<div
id="modalGarment"
class="modal-garment tshirt">

<div
id="modalLogo"
class="garment-logo">
GSN
<small>GOD STAYS NEAR</small>
</div>

</div>

</div>


<div class="modal-info">

<div
id="modalCategory"
class="modal-category">
SAMARRETA
</div>

<h2 id="modalName">
Essential Black
</h2>

<p
id="modalDescription"
class="modal-description">
Samarreta negra de tall ample amb logo frontal.
</p>

<div
id="modalPrice"
class="modal-price">
20 €
</div>


<div class="size-title">
SELECCIONA LA TALLA
</div>


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

<button class="size"
onclick="selectSize(this)">
XXL
</button>

</div>


<button
id="modalFavorite"
class="modal-fav"
onclick="favoriteFromModal()">

♡ AFEGIR A FAVORITS

</button>


<div class="info-list">

<div class="info-row">

<span>ESTIL</span>

<strong>STREETWEAR</strong>

</div>

<div class="info-row">

<span>COLOR</span>

<strong id="modalColor">
NEGRE</strong>

</div>

<div class="info-row">

<span>MATERIAL</span>

<strong>COTÓ</strong>

</div>

<div class="info-row">

<span>COL·LECCIÓ</span>

<strong>SNG 2026</strong>

</div>

</div>

</div>

</div>

</div>


<!-- =========================================================
     FAVORITS
     ========================================================= -->

<div class="favorites-panel"
id="favoritesPanel">

<div class="favorites-header">

<h2>ELS MEUS FAVORITS</h2>

<button
class="close-favorites"
onclick="closeFavorites()">
✕
</button>

</div>

<div
class="favorite-list"
id="favoriteList">

<div class="empty-favorites">

Encara no tens peces guardades.<br><br>

Prem el símbol ♡ en qualsevol peça<br>
per afegir-la als teus favorits.

</div>

</div>

</div>


<!-- =========================================================
     TOAST
     ========================================================= -->

<div
class="toast"
id="toast">
</div>


<script>

/* =========================================================
   DADES DELS PRODUCTES
   ========================================================= */

const products = {

1:{
name:"Essential Black",
category:"SAMARRETA",
price:"20 €",
description:"Samarreta negra de tall ample amb el logo SNG a la part frontal.",
type:"tshirt",
color:"NEGRE"
},

2:{
name:"Essential White",
category:"SAMARRETA",
price:"20 €",
description:"Samarreta blanca minimalista amb el logo SNG.",
type:"tshirt white",
color:"BLANC"
},

3:{
name:"Logo Back",
category:"SAMARRETA",
price:"23 €",
description:"Samarreta negra amb el logo principal a la part posterior.",
type:"tshirt",
color:"NEGRE"
},

4:{
name:"Cross Edition",
category:"SAMARRETA",
price:"24 €",
description:"Edició especial amb un gràfic central i el logo SNG.",
type:"tshirt white",
color:"BLANC"
},

5:{
name:"Black Hoodie",
category:"DESSUADORA",
price:"40 €",
description:"Dessuadora negra amb caputxa i logo frontal.",
type:"hoodie",
color:"NEGRE"
},

6:{
name:"Grey Essential",
category:"DESSUADORA",
price:"42 €",
description:"Dessuadora gris de tall còmode i estil urbà.",
type:"hoodie grey",
color:"GRIS"
},

7:{
name:"White Edition",
category:"DESSUADORA",
price:"42 €",
description:"Dessuadora clara amb una estètica neta i moderna.",
type:"hoodie white",
color:"BLANC"
},

8:{
name:"Limited GSN",
category:"DESSUADORA",
price:"45 €",
description:"Model especial de la col·lecció limitada SNG.",
type:"hoodie",
color:"NEGRE"
},

9:{
name:"Black Cargo",
category:"PANTALONS",
price:"38 €",
description:"Pantaló cargo negre amb tall ample i estil urbà.",
type:"pants",
color:"NEGRE"
},

10:{
name:"Grey Wide",
category:"PANTALONS",
price:"36 €",
description:"Pantaló gris de tall ample i molt còmode.",
type:"pants grey",
color:"GRIS"
},

11:{
name:"Light Edition",
category:"PANTALONS",
price:"36 €",
description:"Pantaló clar pensat per combinar amb les dessuadores SNG.",
type:"pants white",
color:"BLANC"
},

12:{
name:"Street Black",
category:"PANTALONS",
price:"40 €",
description:"Pantaló negre inspirat en l'estètica streetwear.",
type:"pants",
color:"NEGRE"
},

13:{
name:"Classic Cap",
category:"GORRA",
price:"18 €",
description:"Gorra negra amb el logo SNG.",
type:"cap",
color:"NEGRE"
},

14:{
name:"White Cap",
category:"GORRA",
price:"18 €",
description:"Gorra blanca amb un disseny minimalista.",
type:"cap",
color:"BLANC"
},

15:{
name:"Grey GSN",
category:"GORRA",
price:"20 €",
description:"Gorra gris amb el logo GSN.",
type:"cap",
color:"GRIS"
},

16:{
name:"Limited Cap",
category:"GORRA",
price:"22 €",
description:"Edició limitada amb el logo GSN.",
type:"cap",
color:"NEGRE"
}

};


/* =========================================================
   FAVORITS
   ========================================================= */

let favorites=[];

let currentProduct=null;


function toggleFavorite(event,id){

event.stopPropagation();

const index=favorites.indexOf(id);

if(index===-1){

favorites.push(id);

document
.getElementById("fav-"+id)
.classList.add("selected");

document
.getElementById("fav-"+id)
.textContent="♥";

showToast("Afegit als teus favorits");

}else{

favorites.splice(index,1);

document
.getElementById("fav-"+id)
.classList.remove("selected");

document
.getElementById("fav-"+id)
.textContent="♡";

showToast("Eliminat dels favorits");

}

updateFavoriteCount();

renderFavorites();

}


function updateFavoriteCount(){

document
.getElementById("favCount")
.textContent=favorites.length;

}


function renderFavorites(){

const container=
document.getElementById("favoriteList");

if(favorites.length===0){

container.innerHTML=`

<div class="empty-favorites">

Encara no tens peces guardades.<br><br>

Prem el símbol ♡ en qualsevol peça
per afegir-la als teus favorits.

</div>

`;

return;

}

container.innerHTML="";

favorites.forEach(id=>{

const product=products[id];

const item=
document.createElement("div");

item.className="favorite-item";

item.innerHTML=`

<div class="mini-garment">

GSN

</div>

<div>

<h4>${product.name}</h4>

<p>
${product.category}
·
${product.price}
</p>

</div>

<button
class="remove-fav"
onclick="removeFavorite(${id})">
♥
</button>

`;

item.onclick=(event)=>{

if(
event.target.classList.contains("remove-fav")
){
return;
}

closeFavorites();

openProduct(id);

};

container.appendChild(item);

});

}


function removeFavorite(id){

const index=favorites.indexOf(id);

if(index!==-1){

favorites.splice(index,1);

}

const button=
document.getElementById("fav-"+id);

if(button){

button.classList.remove("selected");

button.textContent="♡";

}

updateFavoriteCount();

renderFavorites();

showToast("Eliminat dels teus favorits");

}


function openFavorites(){

document
.getElementById("favoritesPanel")
.classList.add("open");

}


function closeFavorites(){

document
.getElementById("favoritesPanel")
.classList.remove("open");

}


/* =========================================================
   PRODUCTE MODAL
   ========================================================= */

function openProduct(id){

const product=products[id];

currentProduct=id;

document
.getElementById("modalCategory")
.textContent=product.category;

document
.getElementById("modalName")
.textContent=product.name;

document
.getElementById("modalDescription")
.textContent=product.description;

document
.getElementById("modalPrice")
.textContent=product.price;

document
.getElementById("modalColor")
.textContent=product.color;

const garment=
document.getElementById("modalGarment");

garment.className=
"modal-garment garment "+product.type;

const logo=
document.getElementById("modalLogo");

logo.innerHTML=`

GSN

<small>GOD STAYS NEAR</small>

`;

if(
product.type.includes("white")
){

logo.style.color="#000";

}else{

logo.style.color="#fff";

}

const favButton=
document.getElementById("modalFavorite");

if(favorites.includes(id)){

favButton.textContent=
"♥ ELIMINAR DELS FAVORITS";

}else{

favButton.textContent=
"♡ AFEGIR A FAVORITS";

}

document
.getElementById("productModal")
.classList.add("active");

document
.body.classList.add("modal-open");

}


function closeProduct(){

document
.getElementById("productModal")
.classList.remove("active");

document
.body.classList.remove("modal-open");

}


function favoriteFromModal(){

if(!currentProduct){
return;
}

const index=
favorites.indexOf(currentProduct);

if(index===-1){

favorites.push(currentProduct);

showToast("Afegit als teus favorits");

}else{

favorites.splice(index,1);

showToast("Eliminat dels teus favorits");

}

const button=
document.getElementById("fav-"+currentProduct);

if(button){

if(favorites.includes(currentProduct)){

button.classList.add("selected");

button.textContent="♥";

}else{

button.classList.remove("selected");

button.textContent="♡";

}

}

const modalButton=
document.getElementById("modalFavorite");

if(favorites.includes(currentProduct)){

modalButton.textContent=
"♥ ELIMINAR DELS FAVORITS";

}else{

modalButton.textContent=
"♡ AFEGIR A FAVORITS";

}

updateFavoriteCount();

renderFavorites();

}


/* =========================================================
   TALLA
   ========================================================= */

function selectSize(button){

const sizes=
document.querySelectorAll(".size");

sizes.forEach(
size=>size.classList.remove("selected")
);

button.classList.add("selected");

showToast(
"Talla seleccionada: "+button.textContent
);

}


/* =========================================================
   FILTRES
   ========================================================= */

function filterProducts(category,button){

const productElements=
document.querySelectorAll(".product");

productElements.forEach(product=>{

if(
category==="tots" ||
product.dataset.category===category
){

product.style.display="block";

}else{

product.style.display="none";

}

});


const filters=
document.querySelectorAll(".filter");

filters.forEach(
filter=>filter.classList.remove("active")
);

if(button){

button.classList.add("active");

}else{

filters.forEach(filter=>{

if(
filter.textContent
.trim()
.toLowerCase()
.includes(category)
){

filter.classList.add("active");

}

});

}

}


/* =========================================================
   NEWSLETTER
   ========================================================= */

function subscribe(event){

event.preventDefault();

const email=
document.getElementById("email");

if(email.value.trim()===""){
return;
}

showToast(
"Gràcies! Ja formes part de SNG."
);

email.value="";

}


/* =========================================================
   TOAST
   ========================================================= */

function showToast(message){

const toast=
document.getElementById("toast");

toast.textContent=message;

toast.classList.add("show");

setTimeout(()=>{

toast.classList.remove("show");

},2200);

}


/* =========================================================
   CERRAR MODAL CLICANDO FUERA
   ========================================================= */

document
.getElementById("productModal")
.addEventListener("click",function(event){

if(event.target===this){

closeProduct();

}

});


/* =========================================================
   ESC
   ========================================================= */

document.addEventListener(
"keydown",
function(event){

if(event.key==="Escape"){

closeProduct();

closeFavorites();

}

});


/* =========================================================
   INICIAR
   ========================================================= */

renderFavorites();

updateFavoriteCount();

</script>

</body>
</html>
