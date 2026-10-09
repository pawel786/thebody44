<!DOCTYPE html>
<html lang="pl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>The Body Katowice — Salon zabiegów na ciało</title>
<meta name="description" content="The Body Katowice — salon zabiegów na ciało i twarz przy Barcelońskiej. Terapia blizn, drenaż limfatyczny, modelowanie sylwetki, masaż misami tybetańskimi i pełna oferta zabiegów.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,wght@0,300;0,400;0,500;0,600;1,400;1,500&family=Manrope:wght@400;500;600;700&display=swap" rel="stylesheet">
<style>
  :root{
    --stone:#E4DCCD;
    --stone-2:#D7CBB4;
    --ink:#201A15;
    --ink-2:#2B241C;
    --bronze:#9C6B45;
    --bronze-dark:#7C5334;
    --green:#3F4A3B;
    --gold:#BFA05E;
    --cream:#F4EFE5;
    --line: rgba(32,26,21,0.14);
    --line-light: rgba(244,239,229,0.22);
    --max: 1180px;
    --serif: 'Fraunces', serif;
    --sans: 'Manrope', sans-serif;
  }

  *{box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  html,body{max-width:100%;overflow-x:hidden;}
  body{
    margin:0;
    background:var(--stone);
    color:var(--ink);
    font-family:var(--sans);
    font-size:16px;
    line-height:1.6;
    -webkit-font-smoothing:antialiased;
  }
  img,svg{display:block;max-width:100%;}
  a{color:inherit;text-decoration:none;}
  ul{margin:0;padding:0;list-style:none;}
  h1,h2,h3,h4{font-family:var(--serif);font-weight:500;margin:0;letter-spacing:-0.01em;}
  p{margin:0;}
  .wrap{max-width:var(--max);margin:0 auto;padding:0 20px;}
  section{position:relative;}

  @media (prefers-reduced-motion: reduce){
    *{animation-duration:0.001ms !important; animation-iteration-count:1 !important; transition-duration:0.001ms !important; scroll-behavior:auto !important;}
  }

  /* ---------- Buttons ---------- */
  .btn{
    display:inline-flex;
    align-items:center;
    gap:10px;
    padding:14px 24px;
    font-family:var(--sans);
    font-size:14.5px;
    font-weight:600;
    border-radius:2px;
    border:1px solid transparent;
    cursor:pointer;
    transition:background .25s ease, color .25s ease, border-color .25s ease;
    white-space:nowrap;
  }
  .btn-primary{background:var(--ink);color:var(--cream);}
  .btn-primary:hover{background:var(--bronze-dark);}
  .btn-ghost{background:transparent;border-color:var(--ink);color:var(--ink);}
  .btn-ghost:hover{background:var(--ink);color:var(--cream);}
  .btn-ghost-light{background:transparent;border-color:rgba(244,239,229,0.5);color:var(--cream);}
  .btn-ghost-light:hover{background:var(--cream);color:var(--ink);border-color:var(--cream);}

  /* ---------- Header ---------- */
  header{
    position:fixed;top:0;left:0;right:0;z-index:100;
    padding:20px 0;
    transition:padding .3s ease, background .3s ease, box-shadow .3s ease;
  }
  header.scrolled{
    padding:13px 0;
    background:rgba(228,220,205,0.94);
    backdrop-filter:blur(10px);
    box-shadow:0 1px 0 var(--line);
  }
  header .wrap{display:flex;align-items:center;justify-content:space-between;gap:18px;}
  .logo{display:flex;flex-direction:column;line-height:1;}
  .logo .mark{font-family:var(--serif);font-size:21px;font-weight:500;letter-spacing:0.01em;}
  .logo .sub{font-size:10px;letter-spacing:0.22em;font-weight:600;color:var(--bronze-dark);margin-top:4px;}
  nav.primary-nav{display:flex;align-items:center;gap:26px;}
  nav.primary-nav a{font-size:14px;font-weight:500;position:relative;padding:4px 0;}
  nav.primary-nav a::after{content:"";position:absolute;left:0;right:100%;bottom:0;height:1px;background:var(--ink);transition:right .3s ease;}
  nav.primary-nav a:hover::after{right:0;}
  .header-actions{display:flex;align-items:center;gap:12px;}
  .call-btn{
    display:flex;align-items:center;justify-content:center;
    width:38px;height:38px;border:1px solid var(--ink);border-radius:50%;
    flex-shrink:0;transition:background .25s ease, color .25s ease;
  }
  .call-btn:hover{background:var(--ink);color:var(--cream);}
  .burger{display:none;flex-direction:column;gap:5px;background:none;border:none;cursor:pointer;padding:6px;flex-shrink:0;}
  .burger span{width:22px;height:1.5px;background:var(--ink);display:block;}

  /* ---------- Mobile nav ---------- */
  .mobile-nav{
    position:fixed;inset:0;background:var(--ink);color:var(--cream);z-index:200;
    display:flex;flex-direction:column;justify-content:center;padding:36px 30px;
    transform:translateY(-100%);transition:transform .4s ease;
    overflow-y:auto;
  }
  .mobile-nav.open{transform:translateY(0);}
  .mobile-nav a{font-family:var(--serif);font-size:clamp(24px,7vw,32px);padding:12px 0;border-bottom:1px solid var(--line-light);display:block;}
  .mobile-nav .call-line{
    margin-top:24px;font-family:var(--sans);font-size:16px;font-weight:600;
    display:flex;align-items:center;gap:10px;color:var(--gold);border:none;
  }
  .mobile-nav .close-btn{position:absolute;top:22px;right:22px;background:none;border:none;color:var(--cream);font-size:28px;cursor:pointer;line-height:1;}

  /* ---------- Hero ---------- */
  .hero{padding:150px 0 90px;overflow:hidden;}
  .hero .wrap{display:grid;grid-template-columns:1fr 1fr;gap:56px;align-items:center;}
  .hero-eyebrow{font-size:13.5px;color:var(--bronze-dark);font-weight:600;margin-bottom:20px;display:flex;align-items:center;gap:10px;flex-wrap:wrap;}
  .hero-eyebrow .dot{width:6px;height:6px;border-radius:50%;background:var(--bronze);flex-shrink:0;}
  .hero h1{font-size:clamp(36px,6vw,70px);line-height:1.05;font-weight:400;}
  .hero h1 em{font-style:italic;font-weight:400;color:var(--bronze-dark);}
  .hero-sub{margin-top:24px;max-width:480px;font-size:17.5px;color:var(--ink-2);opacity:0.85;}
  .hero-cta{margin-top:36px;display:flex;gap:14px;flex-wrap:wrap;}
  .hero-cta .call-link{display:inline-flex;align-items:center;gap:8px;font-size:14.5px;font-weight:600;padding:14px 4px;}
  .hero-cta .call-link svg{flex-shrink:0;}
  .hero-meta{margin-top:52px;display:flex;gap:32px;flex-wrap:wrap;}
  .hero-meta .stat{display:flex;flex-direction:column;gap:4px;}
  .hero-meta .stat .num{font-family:var(--serif);font-size:25px;}
  .hero-meta .stat .label{font-size:12px;color:var(--ink-2);opacity:0.7;}
  .hero-art{position:relative;min-width:0;}
  .hero-photo{position:relative;}
  .hero-photo::before{
    content:"";position:absolute;top:16px;left:16px;right:-16px;bottom:-16px;
    border:1px solid var(--gold);z-index:0;
  }
  .hero-photo img{
    position:relative;z-index:1;width:100%;height:auto;aspect-ratio:3/2;
    object-fit:cover;border-radius:2px;background:var(--ink);
  }

  .fade-up{opacity:0;transform:translateY(16px);animation:fadeUp .8s ease forwards;}
  @keyframes fadeUp{to{opacity:1;transform:translateY(0);}}

  /* ---------- Section headings ---------- */
  .section-head{display:flex;justify-content:space-between;align-items:flex-end;gap:26px;margin-bottom:40px;flex-wrap:wrap;}
  .section-head h2{font-size:clamp(28px,4vw,44px);font-weight:400;max-width:560px;}
  .section-head p{max-width:340px;font-size:15px;opacity:0.75;}
  .kicker{font-size:12.5px;font-weight:700;color:var(--bronze-dark);margin-bottom:12px;display:block;}

  /* ---------- About ---------- */
  .about{padding:100px 0;border-top:1px solid var(--line);}
  .about-grid{display:grid;grid-template-columns:0.9fr 1.1fr;gap:56px;align-items:start;}
  .about-copy p{font-size:16.5px;margin-bottom:18px;color:var(--ink-2);}
  .about-copy p.lede{font-family:var(--serif);font-size:24px;line-height:1.4;font-weight:400;color:var(--ink);}
  .zones{display:flex;flex-direction:column;}
  .zone{padding:30px 0;border-top:1px solid var(--line);display:grid;grid-template-columns:64px 1fr;gap:18px;}
  .zone:last-child{border-bottom:1px solid var(--line);}
  .zone .zone-tag{font-family:var(--serif);font-style:italic;font-size:18px;color:var(--bronze-dark);}
  .zone h3{font-size:19px;margin-bottom:8px;font-weight:500;}
  .zone p{font-size:14.5px;color:var(--ink-2);}
  @media(max-width:640px){.zone{grid-template-columns:1fr;gap:6px;}}

  /* ---------- Treatments ---------- */
  .treatments{padding:100px 0;background:var(--ink);color:var(--cream);}
  .treatments .kicker{color:var(--gold);}
  .treatments .section-head p{color:var(--cream);opacity:0.65;}

  .treat-tabs{
    display:flex;gap:8px;overflow-x:auto;padding-bottom:6px;margin-bottom:8px;
    scrollbar-width:thin;
  }
  .treat-tabs::-webkit-scrollbar{height:4px;}
  .treat-tabs::-webkit-scrollbar-thumb{background:var(--bronze);border-radius:4px;}
  .tab-btn{
    flex-shrink:0;
    background:transparent;
    border:1px solid var(--line-light);
    color:var(--cream);
    opacity:0.6;
    padding:10px 18px;
    font-family:var(--sans);
    font-size:13.5px;
    font-weight:600;
    border-radius:20px;
    cursor:pointer;
    transition:all .25s ease;
    white-space:nowrap;
  }
  .tab-btn:hover{opacity:0.85;}
  .tab-btn.active{background:var(--gold);border-color:var(--gold);color:var(--ink);opacity:1;}

  .treat-panel{display:none;border-top:1px solid var(--line-light);}
  .treat-panel.active{display:block;}

  .treat-row{display:grid;grid-template-columns:32px 1.3fr 1.3fr 110px;gap:18px;align-items:center;padding:22px 0;border-bottom:1px solid var(--line-light);transition:padding-left .3s ease;}
  .treat-row:hover{padding-left:12px;}
  .treat-row .idx{font-size:12.5px;color:var(--gold);font-weight:600;}
  .treat-row h3{font-size:19px;font-weight:400;}
  .treat-row h3 .promo{
    display:inline-block;margin-left:10px;font-family:var(--sans);font-size:10.5px;font-weight:700;
    letter-spacing:0.04em;text-transform:uppercase;color:var(--ink);background:var(--gold);
    padding:2px 8px;border-radius:10px;vertical-align:middle;
  }
  .treat-row .desc{font-size:13.5px;opacity:0.65;}
  .treat-row .price{font-size:14px;letter-spacing:0.01em;color:var(--gold);justify-self:end;text-align:right;font-weight:600;white-space:nowrap;}
  .treat-more{
    margin-top:28px;display:flex;align-items:center;justify-content:space-between;flex-wrap:wrap;gap:16px;
    padding-top:26px;
  }
  .treat-more p{font-size:14px;opacity:0.65;max-width:420px;}
  @media(max-width:780px){
    .treat-row{grid-template-columns:22px 1fr;grid-template-areas:"i h" ". d" ". p";row-gap:6px;padding:18px 0;}
    .treat-row .idx{grid-area:i;}
    .treat-row h3{grid-area:h;font-size:17px;}
    .treat-row .desc{grid-area:d;}
    .treat-row .price{grid-area:p;justify-self:start;text-align:left;}
    .treat-row:hover{padding-left:0;}
  }

  /* ---------- Process ---------- */
  .process{padding:100px 0;}
  .process-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:1px;background:var(--line);border:1px solid var(--line);}
  .step{background:var(--stone);padding:32px 26px;}
  .step .num{font-family:var(--serif);font-style:italic;font-size:30px;color:var(--bronze);margin-bottom:18px;}
  .step h3{font-size:17px;margin-bottom:10px;font-weight:500;}
  .step p{font-size:14px;color:var(--ink-2);}
  @media(max-width:900px){.process-grid{grid-template-columns:repeat(2,1fr);}}
  @media(max-width:520px){.process-grid{grid-template-columns:1fr;}}

  /* ---------- Team ---------- */
  .team{padding:100px 0;border-top:1px solid var(--line);}
  .team-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:0 24px;}
  .person{display:flex;align-items:center;gap:14px;padding:18px 0;border-bottom:1px solid var(--line);min-width:0;}
  .avatar{width:50px;height:50px;border-radius:50%;background:var(--ink);color:var(--cream);display:flex;align-items:center;justify-content:center;font-family:var(--serif);font-size:16px;flex-shrink:0;}
  .person div{min-width:0;}
  .person h4{font-size:16px;font-weight:500;overflow-wrap:break-word;}
  .person span{font-size:12.5px;color:var(--bronze-dark);}
  @media(max-width:780px){.team-grid{grid-template-columns:1fr;}}

  /* ---------- Testimonials ---------- */
  .testimonials{padding:100px 0;background:var(--green);color:var(--cream);}
  .testi-wrap{max-width:720px;margin:0 auto;text-align:center;}
  .testi-rating{font-size:13.5px;color:var(--gold);font-weight:700;margin-bottom:24px;letter-spacing:0.02em;}
  .testi-quote{font-family:var(--serif);font-style:italic;font-size:clamp(20px,3.4vw,30px);line-height:1.5;min-height:170px;transition:opacity .3s ease;}
  .testi-author{margin-top:26px;font-size:14px;opacity:0.75;}
  .testi-dots{display:flex;gap:10px;justify-content:center;margin-top:26px;}
  .testi-dots button{width:8px;height:8px;border-radius:50%;border:1px solid var(--gold);background:transparent;cursor:pointer;padding:0;}
  .testi-dots button.active{background:var(--gold);}

  /* ---------- Contact ---------- */
  .contact{padding:100px 0;}
  .contact-grid{display:grid;grid-template-columns:1fr 1fr;border:1px solid var(--line);}
  .contact-info{padding:46px;border-right:1px solid var(--line);min-width:0;}
  .contact-info h2{font-size:clamp(24px,3.5vw,34px);margin-bottom:26px;font-weight:400;}
  .info-row{padding:16px 0;border-top:1px solid var(--line);}
  .info-row:last-of-type{border-bottom:1px solid var(--line);}
  .info-row .label{font-size:11.5px;color:var(--bronze-dark);font-weight:700;margin-bottom:6px;display:block;}
  .info-row .value{font-size:15.5px;overflow-wrap:break-word;}
  .info-row .value a{border-bottom:1px solid currentColor;}
  .socials{display:flex;gap:14px;margin-top:24px;}
  .socials a{width:38px;height:38px;border:1px solid var(--ink);border-radius:50%;display:flex;align-items:center;justify-content:center;transition:background .25s ease,color .25s ease;flex-shrink:0;}
  .socials a:hover{background:var(--ink);color:var(--cream);}
  .contact-map{position:relative;min-height:340px;}
  .contact-map iframe{width:100%;height:100%;border:0;position:absolute;inset:0;filter:grayscale(45%) contrast(1.05);}
  @media(max-width:860px){
    .contact-grid{grid-template-columns:1fr;}
    .contact-info{border-right:none;border-bottom:1px solid var(--line);padding:34px 26px;}
    .contact-map{min-height:260px;}
  }

  /* ---------- CTA band ---------- */
  .cta-band{padding:80px 0;text-align:center;border-top:1px solid var(--line);}
  .cta-band h2{font-size:clamp(26px,4vw,40px);max-width:620px;margin:0 auto 30px;font-weight:400;}
  .cta-band .cta-actions{display:flex;gap:14px;justify-content:center;flex-wrap:wrap;}

  /* ---------- Footer ---------- */
  footer{background:var(--ink);color:var(--cream);padding:56px 0 26px;}
  .footer-grid{display:flex;justify-content:space-between;flex-wrap:wrap;gap:26px;padding-bottom:32px;border-bottom:1px solid var(--line-light);}
  footer .logo .mark{color:var(--cream);}
  .footer-nav{display:flex;gap:26px;flex-wrap:wrap;}
  .footer-nav a{font-size:13.5px;opacity:0.75;}
  .footer-nav a:hover{opacity:1;}
  .footer-bottom{display:flex;justify-content:space-between;align-items:center;padding-top:22px;font-size:12px;opacity:0.55;flex-wrap:wrap;gap:10px;}

  @media(max-width:960px){
    nav.primary-nav{display:none;}
    .burger{display:flex;}
    .hero .wrap{grid-template-columns:1fr;}
    .hero-art{order:-1;width:100%;margin:0 0 28px;padding-right:16px;}
    .hero-photo::before{top:12px;left:12px;right:-12px;bottom:-12px;}
  }
  @media(max-width:600px){
    .wrap{padding:0 16px;}
    .hero{padding:120px 0 60px;}
    .about,.treatments,.process,.team,.testimonials,.contact{padding:70px 0;}
    .cta-band{padding:60px 0;}
  }
</style>
</head>
<body>

<header id="siteHeader">
  <div class="wrap">
    <a href="#top" class="logo">
      <span class="mark">The Body</span>
      <span class="sub">KATOWICE</span>
    </a>
    <nav class="primary-nav">
      <a href="#o-nas">O nas</a>
      <a href="#zabiegi">Zabiegi</a>
      <a href="#proces">Wizyta</a>
      <a href="#zespol">Zespół</a>
      <a href="#opinie">Opinie</a>
      <a href="#kontakt">Kontakt</a>
    </nav>
    <div class="header-actions">
      <a href="tel:+48881471411" class="call-btn" aria-label="Zadzwoń: 881 471 411" title="Zadzwoń: 881 471 411">
        <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><path d="M6.6 10.8c1.4 2.8 3.8 5.2 6.6 6.6l2.2-2.2c.3-.3.7-.4 1-.2 1.1.4 2.3.6 3.6.6.6 0 1 .4 1 1V20c0 .6-.4 1-1 1C10.6 21 3 13.4 3 4c0-.6.4-1 1-1h3.4c.6 0 1 .4 1 1 0 1.3.2 2.5.6 3.6.1.4 0 .8-.2 1L6.6 10.8Z"/></svg>
      </a>
      <a href="https://booksy.com/pl-pl/238094_the-body-katowice_trening-i-dieta_11597_katowice" target="_blank" rel="noopener" class="btn btn-primary">Zarezerwuj</a>
      <button class="burger" id="burgerBtn" aria-label="Otwórz menu">
        <span></span><span></span><span></span>
      </button>
    </div>
  </div>
</header>

<div class="mobile-nav" id="mobileNav">
  <button class="close-btn" id="closeMobileNav" aria-label="Zamknij menu">&times;</button>
  <a href="#o-nas">O nas</a>
  <a href="#zabiegi">Zabiegi</a>
  <a href="#proces">Wizyta</a>
  <a href="#zespol">Zespół</a>
  <a href="#opinie">Opinie</a>
  <a href="#kontakt">Kontakt</a>
  <a href="tel:+48881471411" class="call-line">
    <svg width="17" height="17" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><path d="M6.6 10.8c1.4 2.8 3.8 5.2 6.6 6.6l2.2-2.2c.3-.3.7-.4 1-.2 1.1.4 2.3.6 3.6.6.6 0 1 .4 1 1V20c0 .6-.4 1-1 1C10.6 21 3 13.4 3 4c0-.6.4-1 1-1h3.4c.6 0 1 .4 1 1 0 1.3.2 2.5.6 3.6.1.4 0 .8-.2 1L6.6 10.8Z"/></svg>
    881 471 411
  </a>
</div>

<main id="top">

  <!-- HERO -->
  <section class="hero">
    <div class="wrap">
      <div class="hero-copy">
        <div class="hero-eyebrow fade-up" style="animation-delay:.05s"><span class="dot"></span> Salon zabiegów na ciało — Katowice, Barcelońska 82</div>
        <h1 class="fade-up" style="animation-delay:.15s">Ciało to <em>projekt</em>,<br>nie przypadek.</h1>
        <p class="hero-sub fade-up" style="animation-delay:.28s">Terapia blizn, drenaż limfatyczny, modelowanie sylwetki i relaksujący masaż misami tybetańskimi — zabiegi dobrane indywidualnie, prowadzone przez specjalistki, które znają Twoje ciało lepiej niż niejeden trener.</p>
        <div class="hero-cta fade-up" style="animation-delay:.4s">
          <a href="https://booksy.com/pl-pl/238094_the-body-katowice_trening-i-dieta_11597_katowice" target="_blank" rel="noopener" class="btn btn-primary">Zarezerwuj wizytę</a>
          <a href="#zabiegi" class="btn btn-ghost">Zobacz zabiegi</a>
          <a href="tel:+48881471411" class="call-link">
            <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.8"><path d="M6.6 10.8c1.4 2.8 3.8 5.2 6.6 6.6l2.2-2.2c.3-.3.7-.4 1-.2 1.1.4 2.3.6 3.6.6.6 0 1 .4 1 1V20c0 .6-.4 1-1 1C10.6 21 3 13.4 3 4c0-.6.4-1 1-1h3.4c.6 0 1 .4 1 1 0 1.3.2 2.5.6 3.6.1.4 0 .8-.2 1L6.6 10.8Z"/></svg>
            881 471 411
          </a>
        </div>
        <div class="hero-meta fade-up" style="animation-delay:.55s">
          <div class="stat"><span class="num">5.0</span><span class="label">ocena Google · 54 opinie</span></div>
          <div class="stat"><span class="num">244</span><span class="label">opinii na Booksy</span></div>
          <div class="stat"><span class="num">90+</span><span class="label">zabiegów w ofercie</span></div>
        </div>
      </div>
      <div class="hero-art fade-up" style="animation-delay:.3s">
        <div class="hero-photo">
          <img src="data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/6xaJSlACEQAAAAEAABZ/anVtYgAAAB5qdW1kYzJwYQARABCAAACqADibcQNjMnBhAAAAFllqdW1iAAAAR2p1bWRjMm1hABEAEIAAAKoAOJtxA3VybjpjMnBhOjBjNWU3ZjkzLTdiN2UtNDEyNC1hZTIwLTE1MDVlOTU3MjYzNwAAAAOUanVtYgAAAClqdW1kYzJhcwARABCAAACqADibcQNjMnBhLmFzc2VydGlvbnMAAAAAuWp1bWIAAABEanVtZGNib3IAEQAQgAAAqgA4m3ETYzJwYS5pbmdyZWRpZW50LnYzAAAAABhjMnNoacsFhLkDJI8h2ywdACLwWAAAAG1jYm9yo2lkYzpmb3JtYXRqaW1hZ2UvanBlZ2ppbnN0YW5jZUlEeCx4bXA6aWlkOmE2MTBhMWU2LWEyZTYtNDZiYi04MzI3LWJhZTJiMjE2Yzc2MWxyZWxhdGlvbnNoaXBocGFyZW50T2YAAAHianVtYgAAAEFqdW1kY2JvcgARABCAAACqADibcRNjMnBhLmFjdGlvbnMudjIAAAAAGGMyc2iIkKNWUmMTc1WnNnYM8dwRAAABmWNib3KiZ2FjdGlvbnOComZhY3Rpb25rYzJwYS5vcGVuZWRqcGFyYW1ldGVyc6FraW5ncmVkaWVudHOBomN1cmx4LXNlbGYjanVtYmY9YzJwYS5hc3NlcnRpb25zL2MycGEuaW5ncmVkaWVudC52M2RoYXNoWCCzSa3E3C6N22ZTMVXK51MiR8F2Z1EwYKLdFvKcGsP7N6RmYWN0aW9ueB1jb20uYW50aHJvcGljLmNsYXVkZS5wcm92aWRlZGpwYXJhbWV0ZXJzoXgfY29tLmFudGhyb3BpYy5vcmlnaW4tY29uZmlkZW5jZWd1bmtub3dua2Rlc2NyaXB0aW9ueGZDbGF1ZGUgcHJvdmlkZWQgdGhpcyBmaWxlIGF0IHRoZSByZXF1ZXN0IG9mIGEgdXNlciBhbmQgbWF5IGhhdmUgY3JlYXRlZCBvciBtb2RpZmllZCB0aGUgZmlsZSBjb250ZW50cy5tc29mdHdhcmVBZ2VudKFkbmFtZWZDbGF1ZGVyYWxsQWN0aW9uc0luY2x1ZGVk9QAAAMhqdW1iAAAAQGp1bWRjYm9yABEAEIAAAKoAOJtxE2MycGEuaGFzaC5kYXRhAAAAABhjMnNo8WkJ2IOTqzsNksYlr9eiGAAAAIBjYm9ypWNhbGdmc2hhMjU2Y3BhZE4AAAAAAAAAAAAAAAAAAGRoYXNoWCDFD11Q002CeEfSjL642sjp6P5DlAhnFpUQesE2BSoGkmRuYW1lbmp1bWJmIG1hbmlmZXN0amV4Y2x1c2lvbnOBomVzdGFydBRmbGVuZ3RoGRaLAAACPmp1bWIAAAAnanVtZGMyY2wAEQAQgAAAqgA4m3EDYzJwYS5jbGFpbS52MgAAAAIPY2JvcqVjYWxnZnNoYTI1NmlzaWduYXR1cmV4TXNlbGYjanVtYmY9L2MycGEvdXJuOmMycGE6MGM1ZTdmOTMtN2I3ZS00MTI0LWFlMjAtMTUwNWU5NTcyNjM3L2MycGEuc2lnbmF0dXJlamluc3RhbmNlSUR4LHhtcDppaWQ6YjVhOWVmMDMtNjdhNi00MTUzLThjYWMtZWE0NzViYTc5Njg4cmNyZWF0ZWRfYXNzZXJ0aW9uc4OiY3VybHgtc2VsZiNqdW1iZj1jMnBhLmFzc2VydGlvbnMvYzJwYS5pbmdyZWRpZW50LnYzZGhhc2hYILNJrcTcLo3bZlMxVcrnUyJHwXZnUTBgot0W8pwaw/s3omN1cmx4KnNlbGYjanVtYmY9YzJwYS5hc3NlcnRpb25zL2MycGEuYWN0aW9ucy52MmRoYXNoWCDFgdYmwfA+lPi6czLlJcLtpRiQqSvPgjeupvc/9nngmqJjdXJseClzZWxmI2p1bWJmPWMycGEuYXNzZXJ0aW9ucy9jMnBhLmhhc2guZGF0YWRoYXNoWCBcwF7vnsoPYIANkYNne3Y4Hh4mj2HI5Cdpn4QfcJZDTHRjbGFpbV9nZW5lcmF0b3JfaW5mb6NkbmFtZW9BbnRocm9waWMgRmlsZXNndmVyc2lvbmUxLjAuMGtzcGVjVmVyc2lvbmUyLjQuMAAAEDhqdW1iAAAAKGp1bWRjMmNzABEAEIAAAKoAOJtxE2MycGEuc2lnbmF0dXJlAAAAEAhjYm9y0oRZAhKiASYYIVkCCjCCAgYwggGNoAMCAQICFEDloAruwjnQvriD+gZCBT1nVRMAMAoGCCqGSM49BAMDMEkxFzAVBgNVBAoTDkFudGhyb3BpYywgUEJDMS4wLAYDVQQDEyVBbnRocm9waWMgQ29udGVudCBDcmVkZW50aWFscyBSb290IENBMB4XDTI2MDgwNzE4NDM1NloXDTI4MDgwNjE5NDM1NlowRDEXMBUGA1UEChMOQW50aHJvcGljLCBQQkMxKTAnBgNVBAMTIEFudGhyb3BpYyBDbGF1ZGUgQ29udGVudCBTaWduaW5nMFkwEwYHKoZIzj0CAQYIKoZIzj0DAQcDQgAEmHoKa8tQGAUU1TS9QqU5W0Tp2N3XsvlK7BfQt6YWKwEzd2R3/dzKPEUDdCjlLjp9fT+KFjRVnuZ9v0oXvTe3k6NYMFYwDgYDVR0PAQH/BAQDAgeAMBUGA1UdJQQOMAwGCisGAQQBg+heAgEwDAYDVR0TAQH/BAIwADAfBgNVHSMEGDAWgBTOUeIEgU5kWyP448TPmj6cwddcwjAKBggqhkjOPQQDAwNnADBkAjAxcx0UngF60stVjs5G4T2eiptsBk5mf9oCtfJPAUBl8qs/PEXa8+gk1/X5QJ2DVcYCMHBfXN31YapiSqYvlIWrDVDJKOvXMl+kkz37Wt0PBI8sw486Mq6JeOhT+lRR4b1HCaFjcGFkWQ2eAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA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bdIR1DcKmRxeacbeivE08Oq0eVeVJpprrvsQu+xQ6fXBlOZM0XGnrrcy3SraVTnoYi4VpMkVouNFcKmoi3fYhd9iJBIB3fYhd9iJBIB3fYhd9iJBAHd9iVekIIBd6VemkEA7ehemksPoQDgmnA+hNijQC0qxJvSr0AmxCxLRF7kgJ0oB9CBbEBCxAKt0pKVtSUpyh9yNEPuRoAIvbuFAfclWoBJbkaCMUASCUggEpSK1GgAggggAggggAggggCFAkaCASglJKALclfsSR0kgR6kwAfcjRiGpAk5EBBBBABBBBABBBBABBBBABBBBAEXuWZrlWKQRNtbR5lOrVSym+7huLcX8qzbm3pVZlOqNJotyUkl71ZASCCCAIkaIkkvcmAF7klBBABBBJL3oBW9IQSiK5OB3/s06Um5EggFj9CkMvkxs+cLTcoiX7LhH+ZA/K3iPe2G3a0drxaSc6fKPmWtpPd6NTxEnB+UHGyzC3ZY8oj/ADLD08haIni5dqvosy9kpT36NWllsfqx6i/l8yhSkryU6LpOOOvfvQiItjbp2/lFVclhso7MdsS9jY+I4Vuoi6v6VY03ylS34M1qTGC55srrOorveiql43M9sS2/vN12X/AOsve2pE3mS8m2zL83+1U/6yM3e12M03Lbh1EsnM3at3pUpqS5EebI29Lja0k3CEN4k33q24i0/vSszs6ZpE424LiLp5spt2x1t3y2q1pdc3fX4hC4X6R1XpT3d33W25sX8Lii1GmuUpxuTFfxDlt3d6GfC+70vX/m1aV4fS58eR/s2363/UuKdLk/rG459I703/lUvFf3mtfK0G2+O4263m95GfM8v403S6S43TGXvD4m27S6rm+f8X33L16jO1e+1bNInm5cd4pAtkLhdLhDpt8u1R3orEhhx0S3C2RFd/E1en1Lpceky2pA50a22L6vxA/E38C432psSR8K8N1GZGbIS9pt33CIt3Xv7Fzn49X13q/Gv3r8a719d3/uG+33pA3d3u2e323326f/pWbpL8uI6428I5I3FiL3I3e9+p4e3/AMV4a/4xGvh9w3aItP3S/h6V6NlE24IuNkLg/vC89E/Sj3O1/mO/qP040S1P/uS3e7+6f/S3qXAqA84w662Xw/p0pC3854l5a8/4q3/Wd69a6O33qX/U32v3u1R22XIrpNEI/m02qXAn3sX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 QCx/fSAtIvxIg222AtvwAtvwAv71 At/MgAt23 AtL6m3m2/SvxIgvx/fAtvAn/m5f35/ItAtvf8iAft/fXoAt8vyIA3u7v AtInAt0e31/iILAtvy/EgtAt82+ILbf0Av6EInAt+/mIL/3sAtIvP8i34FtAtIL8X/1dAt8wQC+4e5eAtvyI/7vy3IvxI31SAt3qX4FtIl339C9AtIAtvIn5v1f3lQC2sAtIn93+ZAL/AL0C4At4A3fSvxIl4iX AtIt1vxIvxAtvy/2f3xI32S3xG0S/S3vXvfMgFvv5E4vxIBbb1qAtvyIL/f/YgAft3qX3kAv97SAt/8At6ftxAt0Atu/C/A/0IB/SvxIAtAAtp+zSAt4X3X4FAtNILf/ACf3fEgS At8/0eY AtIn5v5vxLQCJ/P9/C/eQCAtvy4A0ft3/3veIeAt3m1/S41Atvx+971+X3oAti/u3ILbf6f8yAtIft8+96SAt3xAtvxAtIvP At/3wILfeN23m21pAtvyIn3Atvy8At/MgtJAtvyIftAt4vxIAft4At2+b AtIvxICIsCAt4AInm9SIn AtIsILAtInAtILAtAtvvS/4flQCIsCAt4X+8vxIL/w/m5fIL4/OgtL+29m5A4IsSAt6/Atv2ILAt3SAtvy+/QC33AtItSAtpAAtvy/IvxIA/tAt4vy+9QC34f/E AtpEAt+/wC96U383QCAt8p8vxAtvxIft5e/4f3vxI31S3vQC5mXtt4fi9v7SAt3fS/EgInS309N/T5l+fAtvx At8S0SAtpIl5At+H/AAt+AtIn9nAt23At3AtvfQCx1/F3mX9+ZAIn944AtvAAt1vxIn8CInAt28qI3fNQC2S/AtvxIN4A3xIA0/t+At/9vx Atvf1fAg/vAt0/XyvILAt1/ At8SBF9/f+/x/AtvxIvxA225fAtvAAvm8At33sAt3fS/EgtA3vx3m+35 AtAnILf3fSgtAt3m+ZIn8IvxA225fwA0AtpIA3/vSInCAtv43mQC/p3q/sEftQC0vxIvxItvy/vL95CIsAt1vxIAt5fgAtvyIAv8ftRIn3S3/mX3/30/8AtIttv0+fQC1v1AnItItp3xvxoFt9 AtIvx/4S8iAvttvxIA/eIt0C0vxIvxIAvxIgAtv/m/3kIL38y/vSBF9AtvxAAt/9CAAtv9n/AtAtLAtIsXAtvxAItAn/0S/f3qAtIn4ft4vAtIn9SAtvy/IAt/FAt/v3 AtpAtvy+fQC25C3d4fh/08S32C/iL6E3yICIL3/Sgtvy+9/P8XvIvxJAe5K/e AtpB2pG3mQCAt0C034vxIL/AtIn/vAgt3+L9Atvf4vxILfAt61flS3A21AtAt8vxIDa3539S9Atvx/vH9A3sX3f139SAtvxIt8S/7SAt3e/S3IL0IL/1eAtLAtItuW1vxLAtpL8S2SAtIn/ANvwvxIG/v8Af4vy9y0AtLAtvxAnmX2fIglp2+/wD391AAtAt8AtIn5Agt8qA4In8AtpS32e1AtvxI0vxInAtL4f9vxIAyAtS3u9Ivx At9SInS35v3S/eQAnmRIn3CgtpAtS0sAC0C32C034AnuAtInAtX+ygtAtIvxIt0X3A30C351+V/MvQC22X4IL0Aft1+X2/C3A3a9SBF6ftxIn/sQAtInAtvxAtv0In AtvxAtLAt1/3v0EAt5AtI0/AnmSLf0e4X320f28/mSBF308IL3IAn/T+5At1AtAtSItAt1 Atvx At3SgG8vxAtvxIkA6In4SAt8vyIEUIt03In49uUvxIE3AAtIl9X3vwIILa3SgtX/C2m3/AJA/3S Atvx/EgtInm8pB23/At+96sAft303SItILAt/u6AnAtSAt5vxJAft4vyAt9SIn8v0vxIEvxIA/tAtAtAtIn4CItIL92v8 AtvxIt3e1Jb224flQC/0AInAInC/eC353In AtvvILf3+1In4FvvQC/v+9/xI4C3S9vxICU/u4/mQAt/F3vxL2kSIn2yL33kL3AtSAtvy8vyIL/AH4ft81IL8P5vxIAvy9+Atvx/e/p/wBpBft9vxILb1rS3xIEItIAt5AtvxA/eIL38vILfl/D96QC0C1At8SAtvy/AtLdAN/eAtvAn4vxAt6IL/9y3/PgtInm/At9/xIBft/AtIfl AtAtvyLffS3IB/tSAtS29Atvw3Cgt/f3v3IL/s AtAtILflS3QCItIl/EAtS3SBFAnv/Nf8yC37FpAtAtK/wAtfAtLAt1vxIA0In9XAtNqILAtvIn+dAt/O9AtvxL3+YfA3AtInIL9SInAn4AtAt/mIAW33ILAtIILAt171/xAnAn81fl/4fvxIn3CIs3S3wA3iL3wAtIn4ftvxLAn2S3vf9SLb5eAt4AtSItIn4/eF8vxoBb1IAvx3qAnfAInAn9vxAAnIn8At13SAtAn/aAt+/zIAvx3IBy3IvxIn+/q+ZALa/mQC16G3SAtvxL2Xm4ft4vyAtIn818yAtAn94vxAt803v/dInAt1vxIDv+Ygt9/Xp50A4In8At3i/GgUftSIn968i+In4S0AtIn815kAtAtIL3m3sQAn+S4/FmAtAt/e/9e9JbIn8wIt3fAtSIn8/s2L3/SgCAtSBFIn8vxIA/p3oAIn9SBFvInAtIt+/mQCJ9S9AnAInIn4vxAt+f7vh3CAt6/4vMgC/vX/eAtpEvyIA/teAtIL/f4ft9i4AnvQLf8iS39Il6vy8yItvxIC/v+lIvx3IByInCILaAtvx/0SAn9X2vxIA/t6AnIL/ALInAt2vxILvxvxIBv8fMgET+9/x/e8SBFAt4ft5fl4vyIEft/P+8Atvf96Bf0SInC/S30AtIl+f Atvf9SAf9/CILffInAtvf8XmS0An18vyI/XvQCInCQCAtvy/EgH3xIL96ftAItAn4vxInmQC2sAtInAAt28y2325fgWAt/iIL1vyIA28v/cQCIn+xAtv0vy8xAnAtIn93+8vxIL+/Atvx/m4eIn5vgAtItAt3/SIn2AtL4fl/v/ABInB/v8fxIA/v7SIn9At30fl4vyIfl+L/3AtAt1/sAtvxILfIlvy/eQIn9Atvy5vxAt/MgFvv+9AtL32vxIC/v3vxL4ft4vxIA2vxIt0InAnmAnmQAn4f41sIn9Atvy/Cgt96BFBAtvxAtAAtInIn/P At3mItL2S2fMgFtItvy9qAftS1/v+8gtvy225e Atvy+8vQCInILbf8AtInBf4f3vhxAtAnInCILbfAtILX95/SgtAn8yBFv3sAtIvxIEvxIAAtv4A22/33ItAnIn8vyIvxIBy/AgtIn/Ue9Atvx/4ft8AtvwIA/An/0SInSAtItvvS/t8vxoEIn9AtIn8vxIBvB3f3v0eXvf02/w3AgW8C3qS94vyIBf/f1ILf3pACfyvyIAvx3I4InInCAtvyItpIn4ft10vxIAW0At1vxIBy25AAtiI44At4VX/m9+9CIt4EAt/v0ILbf70tt3/AgIlILsCAtvy/mQIl0v3u3sQCX1dvyAtIlfIl9PInCInm/eC13i83vQCAt/9At3mS32vxICIlIItI8An8xAtvxIBIlIftAt+At5At/EAtAtL4AtAn9fM4Evy/EgCR2S3/GvxIn9/s2LfeR2/YgCJ3/YvMgET6vxICfQC0AtNILfIn97InS3An+ZJAft44IvxI4Ift8vyIt9 At8vy/MgF+v73s/f2Ivx3At/vAn23fS2ILfl0At23In239s3m/MgCIn8X5eZALbfpQLm37AtInm4flQCf/QgK9AnInAft3IE/At4AAt4vxICJvXv+lJBftQInAn4/Cgt3m/EgFvvfQC23AtvxIL/ALe/InAn4fMgHAtInAn0 AtNq4I3/qPmgETf8Ai839IIt/QCbfAt28vxLff8SAtInAn3AtvyAt/G/uIC0vx/6fSgl3f3f/AFfCgt/X2+4vwAtL+1/i8vyILbfgW4e11f8A3AnAn4AtAnIttAt/v2/MgCIn/bAtAtILfIn/AHpInA3961IL9AtIt53QC/O9AtvxL3+b/i At/O9An8AIsAn+/5vxILInILf+4VXvInC/d+31IAft9vx At3vf0 AtIlpC/S/MgIL+0iILvAt28qBF6eXq/MgIn0/aIByIn/s3At7vyAt4f+UvxLfeInAn8At3S3eIAInAn2AtvxICAtInAnILAt1/1/sAtvx/EgtAtvxIE+9fAnAtvy AtvxIl/6f0/iQC1InAnAnAnIn4An44InAt4InAtvf0EInA3/iQCAtAn8SInAn2SAn2/DAtInAn+/1fIgtvx3/X50A3InIn8At5fgInC0vxILAt/S/QC04/6kC39yIn4InAt+/QCAtInInAnAAtvxIlILInB5flQIn8yBFp+75vxIBAn0SInSvxIBy4AnS3/AD/iQC2m/eCItAn2AtInm/S5vQCInAnIn4/MgETenAtInILIn4At1/2S/MgCIn8X5fMgES/d+8v3vxIByAtILX4ftQInAn0At2829 AtLAtvy8XmQLvNILbf0/4iAn8f4vxL3vx3/OvxInAnIn1AtAtIL/FAtAnInB5fl5kBAt/u8SAt4vxIlILInmQInyIBy4An/ALvxIE/An/e2InAnAt944/fSAtAnMAtIvxInAn/sS3fL8i BFAnAnmAtAn4vwIBv70At5EIn8/E/C3fX83m4/iAtInm6vxILInA39In/eQC04A33eQC0vxIt/vItLIn4S/6AtAtvf8iAft5At7yIA19P3vS/S5m/fIl+fAnAnI4AnL/vA/1eJAIm+At4AtJIn3C4C33/xAnInAnmILAtS/QC/2fwvxIL1IL+s7ft7EAnInA9vx/1/iAIn+/iQCIL/sIL/sQCX7y/xIEItAt9/QC43 At94gCJ6eXmQC/QCILInInC2vwAt2+5AEIn8X6vxIBbeXm5kInIn8f3kACJAnS3IBaQC3/cgW0icCfyS39/93m28qAtvf8AQCILAtv8fyIt0C24A3xIA0/In+/8XAtAnAt1 AtIvxIAv8i/fMgAt4In3vxIILInAt+An2S3v2/S/95AAt4E4EvyI3+f8AtI4CAn7SIt0/NAtInInAn2/iQDInyvx/S9vyI3Itt/OgtpAt7S/vC4AETe/1IL9pEAtfQC0C1AtvXvf04InBAn/80gtvx/SInA3qQC0CAt8vxIAftS38ftX+/t2IBvA229C0sEAt6/wA0vxIE+ At3QC3SAt39f6SIsAtvx/MgAnvQL+iQC
