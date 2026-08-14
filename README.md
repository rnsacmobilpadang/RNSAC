<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>RNS AC — Spesialis AC Mobil</title>

<!-- FONT -->
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet">

<style>

:root{
    --red:#e21d2f;
    --red-dark:#c91627;

    --blue:#0877c9;
    --blue-dark:#075b9b;

    --dark:#111827;
    --text:#1f2937;
    --muted:#6b7280;

    --white:#ffffff;
    --soft:#f5f7fa;
    --line:#e5e7eb;

    --max:1240px;
}

*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

html{
    scroll-behavior:smooth;
}

body{
    font-family:'Inter',Arial,sans-serif;
    color:var(--text);
    background:#fff;
    line-height:1.6;
}

img{
    max-width:100%;
    display:block;
}

a{
    text-decoration:none;
    color:inherit;
}

button{
    font-family:inherit;
}

.container{
    width:min(var(--max), calc(100% - 64px));
    margin:auto;
}


/* =========================================================
   NAVBAR
========================================================= */

.header{
    position:fixed;
    top:0;
    left:0;
    width:100%;
    z-index:1000;

    background:rgba(255,255,255,.96);
    backdrop-filter:blur(12px);

    border-bottom:1px solid rgba(0,0,0,.08);
}

.nav{
    height:82px;

    display:flex;
    align-items:center;
    justify-content:space-between;
}


/* LOGO */

.logo{
    display:flex;
    align-items:center;
    gap:12px;
}

.logo-symbol{
    width:43px;
    height:43px;

    position:relative;

    display:flex;
    align-items:center;
    justify-content:center;

    font-size:21px;
    font-weight:800;

    color:white;

    background:linear-gradient(
        135deg,
        var(--red),
        #ff4a57
    );

    border-radius:10px;

    box-shadow:
        0 5px 15px rgba(226,29,47,.25);
}

.logo-symbol::after{
    content:"";
    position:absolute;

    width:12px;
    height:12px;

    background:var(--blue);

    right:-4px;
    bottom:-3px;

    border-radius:4px;
}

.logo-name{
    font-size:20px;
    font-weight:800;
    letter-spacing:-.04em;

    color:#111827;
}

.logo-tagline{
    display:block;

    margin-top:-2px;

    font-size:9px;
    font-weight:600;

    color:#6b7280;

    letter-spacing:.12em;
}


/* NAV LINKS */

.nav-menu{
    display:flex;
    align-items:center;
    gap:34px;
}

.nav-menu a{
    font-size:14px;
    font-weight:600;

    color:#374151;

    transition:.2s;
}

.nav-menu a:hover{
    color:var(--red);
}


/* NAV BUTTON */

.nav-button{
    display:inline-flex;
    align-items:center;
    justify-content:center;

    padding:12px 20px;

    border-radius:30px;

    color:white !important;

    background:var(--red);

    box-shadow:
        0 6px 18px rgba(226,29,47,.2);

    transition:.2s;
}

.nav-button:hover{
    background:var(--red-dark);
    transform:translateY(-1px);
}


/* MOBILE MENU */

.menu-toggle{
    display:none;

    border:0;
    background:none;

    font-size:28px;

    cursor:pointer;

    color:#111827;
}


/* =========================================================
   HERO
========================================================= */

.hero{
    position:relative;

    min-height:720px;

    display:flex;
    align-items:center;

    padding-top:82px;

    overflow:hidden;
}


/*
   GANTI GAMBAR HERO DI SINI

   Contoh:
   assets/hero-ac.jpg
*/

.hero-background{
    position:absolute;
    inset:0;

    background-image:
        linear-gradient(
            90deg,
            rgba(0,0,0,.75) 0%,
            rgba(0,0,0,.50) 45%,
            rgba(0,0,0,.15) 100%
        ),
        url("gambar_1.jpeg");

    background-size:cover;
    background-position:center;
}

.hero-content{
    position:relative;
    z-index:2;

    max-width:720px;

    color:white;
}

.hero-label{
    display:inline-flex;
    align-items:center;
    gap:10px;

    margin-bottom:22px;

    font-size:13px;
    font-weight:700;

    color:#dbeafe;

    letter-spacing:.02em;
}

.hero-label::before{
    content:"";

    width:28px;
    height:2px;

    background:#ff4050;
}

.hero h1{
    font-size:clamp(42px,6vw,76px);

    line-height:1.05;

    font-weight:800;

    letter-spacing:-.055em;

    margin-bottom:24px;
}

.hero h1 span{
    color:#ff3347;
}

.hero-description{
    max-width:600px;

    color:rgba(255,255,255,.86);

    font-size:17px;

    line-height:1.8;

    margin-bottom:34px;
}

.hero-buttons{
    display:flex;
    gap:14px;

    flex-wrap:wrap;
}


/* BUTTON */

.btn{
    display:inline-flex;
    align-items:center;
    justify-content:center;
    gap:10px;

    padding:14px 24px;

    border-radius:30px;

    font-size:14px;
    font-weight:700;

    transition:.2s;
}

.btn-red{
    color:#fff;
    background:var(--red);

    box-shadow:
        0 8px 25px rgba(226,29,47,.25);
}

.btn-red:hover{
    background:#f02a3d;
    transform:translateY(-2px);
}

.btn-white{
    color:#111827;
    background:white;
}

.btn-white:hover{
    transform:translateY(-2px);
}


/* HERO BOTTOM */

.hero-info{
    position:absolute;

    z-index:3;

    bottom:0;
    left:0;
    width:100%;

    background:rgba(255,255,255,.96);

    border-top:1px solid rgba(0,0,0,.08);
}

.hero-info-inner{
    min-height:105px;

    display:grid;
    grid-template-columns:repeat(3,1fr);
}

.hero-info-item{
    padding:24px 30px;

    border-right:1px solid var(--line);
}

.hero-info-item:last-child{
    border-right:0;
}

.hero-info-number{
    font-size:25px;
    font-weight:800;

    color:var(--red);
}

.hero-info-label{
    font-size:13px;
    color:#6b7280;
}


/* =========================================================
   SECTION
========================================================= */

section{
    padding:110px 0;
}

.section-header{
    max-width:700px;

    margin-bottom:55px;
}

.section-label{
    display:flex;
    align-items:center;
    gap:10px;

    margin-bottom:14px;

    font-size:12px;
    font-weight:700;

    color:var(--red);

    text-transform:uppercase;
    letter-spacing:.08em;
}

.section-label::before{
    content:"";

    width:24px;
    height:2px;

    background:var(--red);
}

.section-title{
    font-size:clamp(32px,4vw,50px);

    line-height:1.08;

    letter-spacing:-.045em;

    font-weight:800;

    color:#111827;
}

.section-description{
    max-width:600px;

    margin-top:18px;

    color:var(--muted);

    font-size:16px;
}


/* =========================================================
   INTRO / ABOUT
========================================================= */

.about{
    background:white;
}

.about-grid{
    display:grid;

    grid-template-columns:1fr 1fr;

    gap:80px;

    align-items:center;
}

.about-image{
    min-height:450px;

    border-radius:18px;

    overflow:hidden;

    position:relative;

    background:
        linear-gradient(
            rgba(0,0,0,.1),
            rgba(0,0,0,.2)
        ),
        url("RNS (3).png"),
        url("gambar_1.jpeg");

    background-size:cover;
    background-position:center;
}

.about-image-badge{
    position:absolute;

    left:24px;
    bottom:24px;

    background:white;

    padding:18px 22px;

    border-radius:12px;

    box-shadow:
        0 15px 40px rgba(0,0,0,.15);
}

.about-image-badge strong{
    display:block;

    font-size:27px;
    font-weight:800;

    color:var(--red);
}

.about-image-badge span{
    font-size:12px;

    color:#6b7280;
}

.about-text h2{
    font-size:clamp(32px,4vw,48px);

    line-height:1.1;

    letter-spacing:-.04em;

    margin-bottom:20px;
}

.about-text p{
    color:var(--muted);

    margin-bottom:16px;
}

.about-list{
    margin-top:28px;

    display:grid;

    gap:15px;
}

.about-list li{
    display:flex;
    align-items:flex-start;

    gap:12px;

    font-size:14px;
    font-weight:600;
}

.check{
    width:23px;
    height:23px;

    flex:none;

    display:flex;
    align-items:center;
    justify-content:center;

    color:white;

    background:var(--red);

    border-radius:50%;

    font-size:12px;
}


/* =========================================================
   SERVICES
========================================================= */

.services{
    background:var(--soft);
}

.service-grid{
    display:grid;

    grid-template-columns:
        repeat(3,1fr);

    gap:22px;
}

.service-card{
    background:white;

    padding:32px;

    border-radius:15px;

    border:1px solid #e9edf2;

    transition:.25s;
}

.service-card:hover{
    transform:translateY(-5px);

    box-shadow:
        0 18px 45px rgba(17,24,39,.09);
}

.service-icon{
    width:50px;
    height:50px;

    display:flex;
    align-items:center;
    justify-content:center;

    margin-bottom:22px;

    color:var(--red);

    background:#fff1f2;

    border-radius:12px;

    font-size:22px;
}

.service-card h3{
    font-size:20px;

    font-weight:750;

    margin-bottom:10px;

    letter-spacing:-.02em;
}

.service-card p{
    font-size:14px;

    color:var(--muted);

    line-height:1.7;
}


/* =========================================================
   WHY US
========================================================= */

.why{
    background:white;
}

.why-grid{
    display:grid;

    grid-template-columns:
        repeat(4,1fr);

    border-top:1px solid var(--line);
    border-left:1px solid var(--line);
}

.why-card{
    padding:35px 28px;

    border-right:1px solid var(--line);
    border-bottom:1px solid var(--line);
}

.why-number{
    font-size:42px;

    font-weight:800;

    color:var(--red);

    letter-spacing:-.05em;

    margin-bottom:12px;
}

.why-card h3{
    font-size:16px;

    font-weight:750;

    margin-bottom:8px;
}

.why-card p{
    font-size:13px;

    color:var(--muted);

    line-height:1.7;
}


/* =========================================================
   PROCESS
========================================================= */

.process{
    background:var(--soft);
}

.process-grid{
    display:grid;

    grid-template-columns:
        repeat(4,1fr);

    position:relative;
}

.process-grid::before{
    content:"";

    position:absolute;

    top:25px;
    left:8%;
    right:8%;

    height:2px;

    background:#dce1e7;
}

.process-card{
    position:relative;

    padding:0 20px;

    text-align:center;
}

.process-number{
    position:relative;
    z-index:2;

    width:50px;
    height:50px;

    margin:0 auto 25px;

    display:flex;
    align-items:center;
    justify-content:center;

    border-radius:50%;

    color:white;

    font-size:13px;
    font-weight:800;

    background:var(--red);

    box-shadow:
        0 0 0 8px var(--soft);
}

.process-card h3{
    font-size:18px;

    margin-bottom:9px;

    font-weight:750;
}

.process-card p{
    font-size:13px;

    color:var(--muted);

    line-height:1.7;
}


/* =========================================================
   TESTIMONIAL
========================================================= */

.testimonials{
    background:white;
}

.testimonial-grid{
    display:grid;

    grid-template-columns:
        repeat(3,1fr);

    gap:24px;
}

.testimonial-card{
    padding:32px;

    background:white;

    border:1px solid var(--line);

    border-radius:15px;

    transition:.2s;
}

.testimonial-card:hover{
    box-shadow:
        0 15px 40px rgba(0,0,0,.07);
}

.stars{
    color:#f59e0b;

    letter-spacing:3px;

    font-size:14px;

    margin-bottom:20px;
}

.testimonial-card p{
    font-size:15px;

    line-height:1.8;

    color:#374151;
}

.customer{
    display:flex;

    align-items:center;

    gap:12px;

    margin-top:24px;
}

.customer-avatar{
    width:42px;
    height:42px;

    display:flex;
    align-items:center;
    justify-content:center;

    border-radius:50%;

    color:white;

    background:linear-gradient(
        135deg,
        var(--red),
        var(--blue)
    );

    font-size:12px;
    font-weight:700;
}

.customer-name{
    font-size:14px;

    font-weight:700;
}

.customer-car{
    font-size:12px;

    color:var(--muted);
}


/* =========================================================
   CTA
========================================================= */

.cta{
    padding:80px 0;

    background:
        linear-gradient(
            110deg,
            var(--red),
            #bd1326
        );

    color:white;
}

.cta-inner{
    display:flex;

    align-items:center;

    justify-content:space-between;

    gap:40px;
}

.cta h2{
    max-width:650px;

    font-size:clamp(34px,5vw,58px);

    line-height:1.05;

    letter-spacing:-.05em;

    font-weight:800;
}

.cta-text{
    max-width:500px;

    margin-top:18px;

    color:rgba(255,255,255,.85);

    font-size:15px;
}

.cta-buttons{
    display:flex;

    gap:12px;

    flex-wrap:wrap;

    flex:none;
}

.cta .btn-red{
    background:#111827;
}

.cta .btn-white{
    background:white;
}


/* =========================================================
   FOOTER
========================================================= */

footer{
    background:#111827;

    color:white;

    padding:65px 0 25px;
}

.footer-grid{
    display:grid;

    grid-template-columns:
        1.5fr
        1fr
        1fr
        1fr;

    gap:50px;

    padding-bottom:50px;

    border-bottom:1px solid rgba(255,255,255,.1);
}

.footer-logo{
    font-size:22px;

    font-weight:800;

    margin-bottom:14px;
}

.footer-description{
    max-width:300px;

    color:#9ca3af;

    font-size:13px;

    line-height:1.8;
}

.footer-title{
    font-size:12px;

    text-transform:uppercase;

    letter-spacing:.08em;

    color:#9ca3af;

    margin-bottom:18px;
}

.footer-links{
    display:grid;

    gap:11px;
}

.footer-links a{
    color:#e5e7eb;

    font-size:13px;

    transition:.2s;
}

.footer-links a:hover{
    color:#ff4658;
}

.footer-bottom{
    display:flex;

    align-items:center;
    justify-content:space-between;

    gap:20px;

    padding-top:24px;
}

.footer-bottom p{
    color:#6b7280;

    font-size:12px;
}


/* =========================================================
   WHATSAPP
========================================================= */

.whatsapp{
    position:fixed;

    right:25px;
    bottom:25px;

    z-index:900;

    width:58px;
    height:58px;

    display:flex;
    align-items:center;
    justify-content:center;

    border-radius:50%;

    background:#25d366;

    color:white;

    box-shadow:
        0 10px 30px rgba(0,0,0,.2);

    transition:.2s;
}

.whatsapp:hover{
    transform:scale(1.08);
}

.whatsapp svg{
    width:28px;
    height:28px;

    fill:white;
}


/* =========================================================
   RESPONSIVE — CLEAN MOBILE VERSION
========================================================= */

@media (max-width:1000px){
    .nav-menu{
        position:absolute;
        top:82px;
        left:0;
        width:100%;
        padding:22px 25px;
        display:none;
        flex-direction:column;
        align-items:stretch;
        gap:0;
        background:#fff;
        border-bottom:1px solid var(--line);
        box-shadow:0 15px 30px rgba(0,0,0,.08);
    }

    .nav-menu.active{ display:flex; }
    .menu-toggle{ display:block; }
    .nav-button{ display:none; }

    .nav-menu a{
        width:100%;
        padding:13px 0;
        border-bottom:1px solid #eef0f3;
    }
    .nav-menu a:last-child{ border-bottom:0; }

    .about-grid{ grid-template-columns:1fr; gap:45px; }
    .service-grid{ grid-template-columns:repeat(2,1fr); }
    .why-grid{ grid-template-columns:repeat(2,1fr); }
    .process-grid{ grid-template-columns:repeat(2,1fr); gap:45px 20px; }
    .process-grid::before{ display:none; }
    .testimonial-grid{ grid-template-columns:1fr; }
    .footer-grid{ grid-template-columns:repeat(2,1fr); }
}

@media (max-width:650px){
    html{ scroll-padding-top:68px; }

    body{ overflow-x:hidden; }

    .container{
        width:calc(100% - 32px);
        max-width:none;
    }

    /* NAVBAR */
    .nav{ height:68px; }

    .nav-menu{
        top:68px;
        padding:12px 18px 18px;
        border-radius:0 0 14px 14px;
    }

    .menu-toggle{
        width:44px;
        height:44px;
        display:flex;
        align-items:center;
        justify-content:center;
        padding:0;
        font-size:25px;
        border-radius:10px;
    }

    .logo-name{ font-size:17px; }
    .logo-tagline{ font-size:7px; }

    /* HERO — keep the image visible */
    .hero{
        min-height:0;
        padding-top:68px;
        display:block;
    }

    .hero-background{
        position:absolute;
        inset:0;
        min-height:100%;
        background-size:cover;
        background-repeat:no-repeat;
        background-position:62% center;
    }

    .hero-content{
        max-width:none;
        padding:82px 0 52px;
    }

    .hero h1{
        font-size:clamp(36px,10.5vw,48px);
        line-height:1.04;
        margin-bottom:18px;
    }

    .hero-description{
        max-width:100%;
        font-size:14px;
        line-height:1.7;
        margin-bottom:24px;
    }

    .hero-buttons{
        width:100%;
        display:grid;
        grid-template-columns:1fr;
        gap:10px;
    }

    .hero-buttons .btn,
    .cta-buttons .btn{
        width:100%;
        min-height:48px;
    }

    .hero-info{
        position:relative;
        left:auto;
        bottom:auto;
        width:100%;
    }

    .hero-info-inner{
        width:100%;
        display:grid;
        grid-template-columns:repeat(3,1fr);
    }

    .hero-info-item{
        min-width:0;
        padding:15px 5px;
        border-right:1px solid var(--line);
        border-bottom:0;
        text-align:center;
    }

    .hero-info-item:last-child{ border-right:0; }
    .hero-info-number{ font-size:18px; }
    .hero-info-label{ font-size:9px; line-height:1.35; }

    /* SECTIONS */
    section{ padding:65px 0; }

    .section-header{ margin-bottom:32px; }
    .section-title{ font-size:31px; line-height:1.08; }
    .section-description{ font-size:14px; line-height:1.7; }

    /* ABOUT IMAGE */
    .about-grid{
        grid-template-columns:1fr;
        gap:30px;
    }

    .about-image{
        width:100%;
        min-height:300px;
        height:58vw;
        max-height:390px;
        border-radius:15px;
        background-size:cover;
        background-repeat:no-repeat;
        background-position:center;
    }

    .about-image-badge{
        left:14px;
        bottom:14px;
        padding:12px 15px;
    }

    .about-image-badge strong{ font-size:22px; }
    .about-image-badge span{ font-size:10px; }

    .about-text h2{ font-size:30px; line-height:1.08; }
    .about-text p{ font-size:14px; line-height:1.75; }

    /* CARDS */
    .service-grid,
    .why-grid,
    .testimonial-grid{
        grid-template-columns:1fr;
        gap:14px;
    }

    .service-card,
    .why-card,
    .testimonial-card{
        width:100%;
        padding:22px;
    }

    /* PROCESS */
    .process-grid{
        grid-template-columns:1fr;
        gap:28px;
    }

    .process-card{
        display:grid;
        grid-template-columns:52px 1fr;
        column-gap:14px;
        text-align:left;
        align-items:start;
    }

    .process-number{
        grid-row:1 / span 2;
        margin:0;
        width:48px;
        height:48px;
    }

    .process-card h3{ margin:2px 0 5px; }
    .process-card p{ font-size:13px; line-height:1.6; }

    /* CTA */
    .cta{ padding:55px 0; }
    .cta-inner{
        flex-direction:column;
        align-items:flex-start;
        gap:25px;
    }

    .cta h2{ font-size:32px; line-height:1.08; }
    .cta-text{ font-size:14px; line-height:1.7; }

    .cta-buttons{
        width:100%;
        display:grid;
        grid-template-columns:1fr;
        gap:10px;
    }

    /* FOOTER */
    .footer-grid{
        grid-template-columns:1fr;
        gap:28px;
    }

    .footer-bottom{
        flex-direction:column;
        align-items:flex-start;
        gap:6px;
    }

    /* WHATSAPP */
    .whatsapp{
        width:52px;
        height:52px;
        right:15px;
        bottom:15px;
    }
}

@media (max-width:380px){
    .container{ width:calc(100% - 26px); }
    .hero-content{ padding-top:70px; }
    .hero h1{ font-size:35px; }
    .hero-info-item{ padding:14px 3px; }
    .hero-info-number{ font-size:16px; }
    .hero-info-label{ font-size:8.5px; }
    .section-title{ font-size:28px; }
    .about-text h2{ font-size:28px; }
}

</style>
</head>


<body>


<!-- =========================================================
     NAVBAR
========================================================= -->

<header class="header">

    <div class="container nav">

        <a href="#" class="logo">

            <div class="logo-symbol">
                R
            </div>

            <div>
                <div class="logo-name">
                    RNS AC
                </div>

                <span class="logo-tagline">
                    SPESIALIS AC MOBIL
                </span>
            </div>

        </a>


        <nav class="nav-menu" id="navMenu">

            <a href="#tentang">
                Tentang Kami
            </a>

            <a href="#layanan">
                Layanan
            </a>

            <a href="#keunggulan">
                Keunggulan
            </a>

            <a href="#proses">
                Proses
            </a>

            <a href="#testimoni">
                Testimoni
            </a>

            <a href="#kontak">
                Kontak
            </a>

        </nav>


        <a
            href="https://wa.me/623899592050"
            target="_blank"
            class="nav-button"
        >
            Hubungi Kami
        </a>


        <button
            class="menu-toggle"
            id="menuToggle"
            aria-label="Menu"
        >
            ☰
        </button>

    </div>

</header>



<!-- =========================================================
     HERO
========================================================= -->

<section class="hero">

    <div class="hero-background"></div>


    <div class="container">

        <div class="hero-content">

            <div class="hero-label">
                Spesialis AC Mobil
            </div>


            <h1>
                AC Mobil Dingin,
                <span>Nyaman</span>
                Setiap Perjalanan.
            </h1>


            <p class="hero-description">
                JL. By Pass No.Km.10, Kalumbuk, Kec. Kuranji, Kota Padang, Sumatera Barat
            </p>


            <div class="hero-buttons">

                <a
                    href="https://wa.me/62895602967947"
                    target="_blank"
                    class="btn btn-red"
                >
                    Booking Servis
                    →
                </a>

                <a
                    href="#layanan"
                    class="btn btn-white"
                >
                    Lihat Layanan
                </a>

            </div>

        </div>

    </div>


    <div class="hero-info">

        <div class="container hero-info-inner">

            <div class="hero-info-item">

                <div class="hero-info-number">
                    10+
                </div>

                <div class="hero-info-label">
                    Tahun pengalaman
                </div>

            </div>


            <div class="hero-info-item">

                <div class="hero-info-number">
                    100%
                </div>

                <div class="hero-info-label">
                    Pemeriksaan sebelum pengerjaan
                </div>

            </div>


            <div class="hero-info-item">

                <div class="hero-info-number">
                    1 Bulan
                </div>

                <div class="hero-info-label">
                    Garansi pengerjaan
                </div>

            </div>

        </div>

    </div>

</section>



<!-- =========================================================
     TENTANG
========================================================= -->

<section class="about" id="tentang">

    <div class="container">

        <div class="about-grid">


            <div class="about-image">

                <div class="about-image-badge">

                    <strong>
                        RNS AC
                    </strong>

                    <span>
                        Spesialis AC Mobil
                    </span>

                </div>

            </div>


            <div class="about-text">

                <div class="section-label">
                    Tentang Kami
                </div>


                <h2>
                    Lebih Dari Sekadar Isi Freon.
                </h2>


                <p>
                    RNS AC merupakan bengkel yang berfokus pada
                    perawatan, pemeriksaan, dan perbaikan sistem
                    AC mobil.
                </p>

                <p>
                    Setiap kendaraan diperiksa terlebih dahulu
                    untuk mengetahui sumber masalah sebelum
                    menentukan tindakan yang diperlukan.
                </p>


                <ul class="about-list">

                    <li>
                        <span class="check">✓</span>
                        Teknisi berpengalaman
                    </li>

                    <li>
                        <span class="check">✓</span>
                        Pemeriksaan tekanan freon
                    </li>

                    <li>
                        <span class="check">✓</span>
                        Diagnosa sebelum pengerjaan
                    </li>

                    <li>
                        <span class="check">✓</span>
                        Garansi pengerjaan
                    </li>

                </ul>

            </div>

        </div>

    </div>

</section>



<!-- =========================================================
     LAYANAN
========================================================= -->

<section class="services" id="layanan">

    <div class="container">

        <div class="section-header">

            <div class="section-label">
                Layanan Kami
            </div>

            <h2 class="section-title">
                Solusi Lengkap Untuk AC Mobil Anda.
            </h2>

            <p class="section-description">
                Mulai dari servis ringan sampai perbaikan
                komponen AC yang membutuhkan pemeriksaan lebih lanjut.
            </p>

        </div>


        <div class="service-grid">


            <div class="service-card">

                <div class="service-icon">
                    ❄
                </div>

                <h3>
                    Isi Ulang Freon
                </h3>

                <p>
                    Pengisian freon berdasarkan kebutuhan
                    sistem AC dan hasil pemeriksaan tekanan.
                </p>

            </div>


            <div class="service-card">

                <div class="service-icon">
                    ⚙
                </div>

                <h3>
                    Perbaikan Kompresor
                </h3>

                <p>
                    Pemeriksaan dan perbaikan kompresor
                    yang lemah, bermasalah, atau tidak bekerja optimal.
                </p>

            </div>


            <div class="service-card">

                <div class="service-icon">
                    ◉
                </div>

                <h3>
                    Service Berkala
                </h3>

                <p>
                    Pemeriksaan sistem AC secara menyeluruh
                    untuk menjaga performa tetap optimal.
                </p>

            </div>


            <div class="service-card">

                <div class="service-icon">
                    ✦
                </div>

                <h3>
                    Cuci Evaporator
                </h3>

                <p>
                    Membersihkan evaporator dari kotoran,
                    debu, dan sumber bau tidak sedap.
                </p>

            </div>


            <div class="service-card">

                <div class="service-icon">
                    ⌁
                </div>

                <h3>
                    Diagnosa Kebocoran
                </h3>

                <p>
                    Pemeriksaan sistem untuk menemukan
                    kemungkinan kebocoran freon.
                </p>

            </div>


            <div class="service-card">

                <div class="service-icon">
                    + 
                </div>

                <h3>
                    Ganti Komponen
                </h3>

                <p>
                    Penggantian komponen AC sesuai hasil
                    diagnosa dan kebutuhan kendaraan.
                </p>

            </div>


        </div>

    </div>

</section>



<!-- =========================================================
     KEUNGGULAN
========================================================= -->

<section class="why" id="keunggulan">

    <div class="container">

        <div class="section-header">

            <div class="section-label">
                Kenapa RNS AC
            </div>

            <h2 class="section-title">
                Dikerjakan Dengan Standar Yang Jelas.
            </h2>

            <p class="section-description">
                Kami mengutamakan pemeriksaan dan komunikasi
                sebelum melakukan pengerjaan pada kendaraan.
            </p>

        </div>


        <div class="why-grid">


            <div class="why-card">

                <div class="why-number">
                    01
                </div>

                <h3>
                    Teknisi Berpengalaman
                </h3>

                <p>
                    Penanganan AC dilakukan oleh teknisi
                    yang memahami berbagai sistem AC mobil.
                </p>

            </div>


            <div class="why-card">

                <div class="why-number">
                    02
                </div>

                <h3>
                    Diagnosa Terlebih Dahulu
                </h3>

                <p>
                    Kendaraan diperiksa sebelum menentukan
                    tindakan servis atau penggantian komponen.
                </p>

            </div>


            <div class="why-card">

                <div class="why-number">
                    03
                </div>

                <h3>
                    Transparan
                </h3>

                <p>
                    Pelanggan mendapatkan informasi mengenai
                    kondisi AC dan kebutuhan pengerjaan.
                </p>

            </div>


            <div class="why-card">

                <div class="why-number">
                    04
                </div>

                <h3>
                    Garansi
                </h3>

                <p>
                    Pengerjaan tertentu mendapatkan garansi
                    sesuai ketentuan yang berlaku.
                </p>

            </div>


        </div>

    </div>

</section>



<!-- =========================================================
     PROSES
========================================================= -->

<section class="process" id="proses">

    <div class="container">

        <div class="section-header">

            <div class="section-label">
                Proses Kerja
            </div>

            <h2 class="section-title">
                Dari Pemeriksaan Sampai AC Kembali Dingin.
            </h2>

        </div>


        <div class="process-grid">


            <div class="process-card">

                <div class="process-number">
                    01
                </div>

                <h3>
                    Konsultasi
                </h3>

                <p>
                    Sampaikan keluhan AC mobil Anda
                    kepada teknisi.
                </p>

            </div>


            <div class="process-card">

                <div class="process-number">
                    02
                </div>

                <h3>
                    Diagnosa
                </h3>

                <p>
                    Sistem AC diperiksa untuk mengetahui
                    sumber masalah.
                </p>

            </div>


            <div class="process-card">

                <div class="process-number">
                    03
                </div>

                <h3>
                    Pengerjaan
                </h3>

                <p>
                    Perbaikan dilakukan berdasarkan hasil
                    pemeriksaan.
                </p>

            </div>


            <div class="process-card">

                <div class="process-number">
                    04
                </div>

                <h3>
                    Uji Coba
                </h3>

                <p>
                    AC diuji kembali sebelum kendaraan
                    diserahkan kepada pelanggan.
                </p>

            </div>


        </div>

    </div>

</section>



<!-- =========================================================
     TESTIMONI
========================================================= -->

<section class="testimonials" id="testimoni">

    <div class="container">

        <div class="section-header">

            <div class="section-label">
                Testimoni
            </div>

            <h2 class="section-title">
                Pengalaman Pelanggan RNS AC.
            </h2>

        </div>


        <div class="testimonial-grid">


            <div class="testimonial-card">

                <div class="stars">
                    ★★★★★
                </div>

                <p>
                    "Awalnya AC cuma terasa hangat.
                    Setelah diperiksa ternyata ada masalah
                    di kompresor. Sekarang sudah dingin lagi."
                </p>

                <div class="customer">

                    <div class="customer-avatar">
                        AH
                    </div>

                    <div>

                        <div class="customer-name">
                            Andra H.
                        </div>

                        <div class="customer-car">
                            Toyota Avanza
                        </div>

                    </div>

                </div>

            </div>


            <div class="testimonial-card">

                <div class="stars">
                    ★★★★★
                </div>

                <p>
                    "Diagnosanya jelas dan dijelaskan
                    sebelum pengerjaan. Jadi tahu masalah
                    mobilnya apa."
                </p>

                <div class="customer">

                    <div class="customer-avatar">
                        RS
                    </div>

                    <div>

                        <div class="customer-name">
                            Andri
                        </div>

                        <div class="customer-car">
                            Innova Reborn
                        </div>

                    </div>

                </div>

            </div>


            <div class="testimonial-card">

                <div class="stars">
                    ★★★★★
                </div>

                <p>
                    "Bau apek di kabin sudah hilang
                    setelah evaporator dibersihkan.
                    Pengerjaannya juga rapi."
                </p>

                <div class="customer">

                    <div class="customer-avatar">
                        DP
                    </div>

                    <div>

                        <div class="customer-name">
                            Dedi P.
                        </div>

                        <div class="customer-car">
                            Mitsubishi Xpander
                        </div>

                    </div>

                </div>

            </div>


        </div>

    </div>

</section>



<!-- =========================================================
     CTA
========================================================= -->

<section class="cta" id="kontak">

    <div class="container">

        <div class="cta-inner">

            <div>

                <h2>
                    AC Mobil Bermasalah?
                    Kami Siap Membantu.
                </h2>

                <p class="cta-text">
                    Hubungi RNS AC untuk konsultasi dan
                    booking servis AC mobil Anda.
                </p>

            </div>


            <div class="cta-buttons">

                <a
                    href="https://wa.me/62895602967947"
                    target="_blank"
                    class="btn btn-red"
                >
                    WhatsApp
                    →
                </a>

                <a
                    href="tel:+62895602967947"
                    class="btn btn-white"
                >
                    Telepon
                </a>

            </div>

        </div>

    </div>

</section>



<!-- =========================================================
     FOOTER
========================================================= -->

<footer>

    <div class="container">

        <div class="footer-grid">


            <div>

                <div class="footer-logo">
                    RNS AC
                </div>

                <p class="footer-description">
                    Spesialis AC mobil yang membantu menjaga
                    kenyamanan perjalanan Anda melalui servis,
                    pemeriksaan, dan perbaikan sistem AC mobil.
                </p>

            </div>


            <div>

                <div class="footer-title">
                    Navigasi
                </div>

                <div class="footer-links">

                    <a href="#tentang">
                        Tentang Kami
                    </a>

                    <a href="#layanan">
                        Layanan
                    </a>

                    <a href="#keunggulan">
                        Keunggulan
                    </a>

                    <a href="#proses">
                        Proses
                    </a>

                </div>

            </div>


            <div>

                <div class="footer-title">
                    Layanan
                </div>

                <div class="footer-links">

                    <a href="#layanan">
                        Isi Freon
                    </a>

                    <a href="#layanan">
                        Service AC
                    </a>

                    <a href="#layanan">
                        Cuci Evaporator
                    </a>

                    <a href="#layanan">
                        Perbaikan Kompresor
                    </a>

                </div>

            </div>


            <div>

                <div class="footer-title">
                    Kontak
                </div>

                <div class="footer-links">

                    <a href="https://wa.me/62895602967947">
                        WhatsApp
                    </a>

                    <a href="tel:+62895602967947">
                        +62 895 602967947
                    </a>

                    <a href="#kontak">
                        Alamat Bengkel
                    </a>

                </div>

            </div>


        </div>


        <div class="footer-bottom">

            <p>
                © 2026 RNS AC. All Rights Reserved.
            </p>

            <p>
                Spesialis AC Mobil
            </p>

        </div>

    </div>

</footer>



<!-- =========================================================
     WHATSAPP FLOAT
========================================================= -->

<a
    href="https://wa.me/62895602967947"
    target="_blank"
    class="whatsapp"
    aria-label="WhatsApp"
>

    <svg viewBox="0 0 32 32">

        <path d="
        M16.001 3
        C9.373 3 4 8.373 4 15
        c0 2.394.708 4.622 1.928 6.492
        L4 29l7.686-1.879
        A11.94 11.94 0 0 0 16.001 27
        C22.63 27 28 21.628 28 15
        S22.63 3 16.001 3z
        m6.964 17.033
        c-.29.816-1.44 1.494-2.353 1.688
        -.628.132-1.448.24-4.208-.9
        -3.53-1.462-5.804-5.033-5.98-5.267
        -.169-.234-1.427-1.9-1.427-3.623
        0-1.723.9-2.573 1.222-2.925
        .29-.317.628-.396.837-.396
        .209 0 .418.002.6.011
        .19.01.446-.072.699.534
        .29.7.983 2.42 1.07 2.596
        .088.176.147.383.03.617
        -.118.234-.176.38-.35.583
        -.176.205-.37.457-.528.614
        -.176.176-.36.367-.155.72
        .205.35.912 1.505 1.958 2.437
        1.345 1.2 2.478 1.573 2.83 1.75
        .351.176.556.147.76-.088
        .205-.234.878-1.024 1.112-1.375
        .235-.352.47-.293.79-.176
        .322.117 2.038.96 2.388 1.135
        .35.176.585.264.671.41
        .088.147.088.85-.202 1.665z"/>

    </svg>

</a>



<script>

/* MOBILE MENU */

const menuToggle =
    document.getElementById("menuToggle");

const navMenu =
    document.getElementById("navMenu");


menuToggle.addEventListener(
    "click",
    () => {

        navMenu.classList.toggle("active");
        menuToggle.textContent = navMenu.classList.contains("active") ? "✕" : "☰";

    }
);


/* CLOSE MOBILE MENU AFTER CLICK */

document
    .querySelectorAll(".nav-menu a")
    .forEach(link => {

        link.addEventListener(
            "click",
            () => {

                navMenu.classList.remove("active");
                menuToggle.textContent = "☰";

            }
        );

    });

</script>


</body>
</html>
