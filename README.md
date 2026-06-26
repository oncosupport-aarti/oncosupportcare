# OncoSupportCare
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>OncoSupport Care – Compassionate Home Healthcare | Kharghar, Navi Mumbai</title>
  <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:wght@400;500;600;700&family=DM+Sans:wght@300;400;500;600&display=swap" rel="stylesheet"/>
  <style>
    :root {
      --teal:      #0a7c6e;
      --teal-lt:   #12a090;
      --teal-bg:   #e8f5f3;
      --green:     #3aaa7a;
      --green-lt:  #d4f0e3;
      --gold:      #c9933a;
      --gold-lt:   #fdf3e3;
      --ink:       #1a2726;
      --muted:     #4a6360;
      --white:     #ffffff;
      --off-white: #f7fbfa;
      --border:    #cde8e3;
    }
    *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
    html { scroll-behavior: smooth; }
    body {
      font-family: 'DM Sans', sans-serif;
      color: var(--ink);
      background: var(--white);
      overflow-x: hidden;
    }
    h1, h2, h3, h4 {
      font-family: 'Cormorant Garamond', serif;
      line-height: 1.15;
    }
    /* ── NAV ── */
    nav {
      position: fixed; top: 0; width: 100%; z-index: 999;
      background: rgba(255,255,255,0.96);
      backdrop-filter: blur(12px);
      border-bottom: 1px solid var(--border);
      padding: 0 6vw;
      display: flex; align-items: center; justify-content: space-between;
      height: 64px;
      animation: slideDown .6s ease both;
    }
    @keyframes slideDown { from { transform: translateY(-100%); opacity:0; } to { transform: translateY(0); opacity:1; } }
    .nav-logo {
      font-family: 'Cormorant Garamond', serif;
      font-size: 1.35rem; font-weight: 700;
      color: var(--teal);
      letter-spacing: .01em;
      text-decoration: none;
      display: flex; align-items: center; gap: .5rem;
    }
    .nav-logo span { color: var(--green); }
    .nav-links { display: flex; gap: 2rem; list-style: none; }
    .nav-links a {
      font-size: .85rem; font-weight: 500; letter-spacing: .04em;
      text-decoration: none; color: var(--muted);
      transition: color .2s;
    }
    .nav-links a:hover { color: var(--teal); }
    .nav-cta {
      background: var(--teal); color: var(--white);
      padding: .5rem 1.25rem; border-radius: 50px;
      font-size: .82rem; font-weight: 600; letter-spacing: .04em;
      text-decoration: none; transition: background .2s, transform .15s;
      white-space: nowrap;
    }
    .nav-cta:hover { background: var(--teal-lt); transform: translateY(-1px); }
    /* ── HERO ── */
    .hero {
      min-height: 100vh;
      display: grid; place-items: center;
      position: relative; overflow: hidden;
      background: linear-gradient(145deg, #0d524a 0%, #0a7c6e 40%, #13a090 100%);
      padding: 120px 6vw 80px;
    }
    .hero-bg-pattern {
      position: absolute; inset: 0; pointer-events: none;
      background-image:
        radial-gradient(circle at 20% 30%, rgba(255,255,255,.06) 0%, transparent 50%),
        radial-gradient(circle at 80% 70%, rgba(58,170,122,.2) 0%, transparent 50%);
    }
    .hero-dots {
      position: absolute; inset: 0; pointer-events: none;
      background-image: radial-gradient(rgba(255,255,255,.08) 1px, transparent 1px);
      background-size: 32px 32px;
    }
    .hero-inner {
      position: relative; text-align: center; max-width: 780px;
      animation: fadeUp .9s .2s ease both;
    }
    @keyframes fadeUp { from { opacity:0; transform: translateY(30px); } to { opacity:1; transform: translateY(0); } }
    .hero-badge {
      display: inline-flex; align-items: center; gap: .4rem;
      background: rgba(255,255,255,.12); border: 1px solid rgba(255,255,255,.25);
      border-radius: 50px; padding: .35rem 1rem;
      color: rgba(255,255,255,.9); font-size: .78rem; font-weight: 500;
      letter-spacing: .08em; text-transform: uppercase;
      margin-bottom: 1.5rem;
    }
    .hero-badge .dot {
      width: 6px; height: 6px; background: #7dffcc;
      border-radius: 50%; animation: pulse 2s infinite;
    }
    @keyframes pulse { 0%,100%{opacity:1;transform:scale(1)} 50%{opacity:.5;transform:scale(1.4)} }
    .hero h1 {
      font-size: clamp(2.8rem, 6vw, 5rem);
      color: var(--white); font-weight: 600;
      margin-bottom: 1.25rem;
      line-height: 1.1;
    }
    .hero h1 em { color: #7dffcc; font-style: normal; }
    .hero-sub {
      font-size: 1.1rem; color: rgba(255,255,255,.8);
      line-height: 1.7; max-width: 560px; margin: 0 auto 2.5rem;
    }
    .hero-actions {
      display: flex; flex-wrap: wrap; gap: 1rem;
      justify-content: center;
    }
    .btn-primary {
      background: var(--white); color: var(--teal);
      padding: .85rem 2rem; border-radius: 50px;
      font-weight: 600; font-size: .95rem; text-decoration: none;
      transition: transform .2s, box-shadow .2s;
      box-shadow: 0 4px 20px rgba(0,0,0,.15);
    }
    .btn-primary:hover { transform: translateY(-2px); box-shadow: 0 8px 30px rgba(0,0,0,.2); }
    .btn-ghost {
      border: 1.5px solid rgba(255,255,255,.5); color: var(--white);
      padding: .85rem 2rem; border-radius: 50px;
      font-weight: 500; font-size: .95rem; text-decoration: none;
      transition: background .2s, transform .2s;
    }
    .btn-ghost:hover { background: rgba(255,255,255,.12); transform: translateY(-2px); }
    .hero-trust {
      margin-top: 3.5rem;
      display: flex; flex-wrap: wrap; justify-content: center; gap: 1.5rem 2.5rem;
    }
    .trust-item {
      color: rgba(255,255,255,.75); font-size: .82rem;
      display: flex; align-items: center; gap: .4rem;
    }
    .trust-item .check { color: #7dffcc; font-size: 1rem; }
    /* ── SECTION BASE ── */
    section { padding: 100px 6vw; }
    .section-tag {
      display: inline-block;
      font-size: .72rem; font-weight: 600; letter-spacing: .12em;
      text-transform: uppercase; color: var(--teal);
      background: var(--teal-bg); border: 1px solid var(--border);
      padding: .3rem .9rem; border-radius: 50px;
      margin-bottom: 1rem;
    }
    .section-title {
      font-size: clamp(2rem, 4vw, 3rem);
      color: var(--ink); font-weight: 600;
      margin-bottom: 1rem;
    }
    .section-lead {
      font-size: 1.05rem; color: var(--muted);
      line-height: 1.75; max-width: 580px;
    }
    .section-header { margin-bottom: 3.5rem; }
    /* ── ABOUT ── */
    .about { background: var(--off-white); }
    .about-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 5rem; align-items: center;
    }
    .about-visual {
      position: relative;
    }
    .about-card-main {
      background: var(--white);
      border: 1px solid var(--border);
      border-radius: 20px;
      padding: 2.5rem;
      box-shadow: 0 8px 40px rgba(10,124,110,.08);
    }
    .about-card-main h3 {
      font-size: 1.7rem; color: var(--teal); margin-bottom: .75rem;
    }
    .about-card-main p { color: var(--muted); line-height: 1.8; }
    .about-card-float {
      position: absolute; bottom: -24px; right: -24px;
      background: var(--teal); color: var(--white);
      border-radius: 16px; padding: 1.25rem 1.5rem;
      box-shadow: 0 12px 40px rgba(10,124,110,.3);
    }
    .about-card-float .big { font-size: 2.2rem; font-weight: 700; line-height: 1; }
    .about-card-float .label { font-size: .8rem; opacity: .85; margin-top: .2rem; }
    .values-list { margin-top: 2rem; display: flex; flex-direction: column; gap: .9rem; }
    .value-item {
      display: flex; align-items: flex-start; gap: .75rem;
      padding: .9rem 1rem;
      background: var(--white); border: 1px solid var(--border);
      border-radius: 12px;
      transition: border-color .2s, transform .2s;
    }
    .value-item:hover { border-color: var(--teal); transform: translateX(4px); }
    .value-icon {
      width: 36px; height: 36px; background: var(--teal-bg);
      border-radius: 8px; display: grid; place-items: center;
      font-size: 1rem; flex-shrink: 0;
    }
    .value-text strong { display: block; font-weight: 600; font-size: .92rem; color: var(--ink); }
    .value-text span { font-size: .82rem; color: var(--muted); }
    /* ── SERVICES ── */
    .services { background: var(--white); }
    .services-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(270px, 1fr));
      gap: 1.5rem;
    }
    .service-card {
      border: 1px solid var(--border);
      border-radius: 18px; padding: 2rem;
      transition: transform .25s, box-shadow .25s, border-color .25s;
      position: relative; overflow: hidden;
      cursor: default;
    }
    .service-card::before {
      content: ''; position: absolute;
      top: 0; left: 0; right: 0; height: 3px;
      background: linear-gradient(90deg, var(--teal), var(--green));
      transform: scaleX(0); transform-origin: left;
      transition: transform .3s ease;
    }
    .service-card:hover { transform: translateY(-6px); box-shadow: 0 16px 48px rgba(10,124,110,.12); border-color: var(--teal); }
    .service-card:hover::before { transform: scaleX(1); }
    .service-emoji {
      font-size: 2rem; margin-bottom: 1rem; display: block;
      width: 52px; height: 52px; background: var(--teal-bg);
      border-radius: 12px; display: grid; place-items: center;
    }
    .service-card h3 {
      font-size: 1.25rem; color: var(--ink); margin-bottom: .5rem;
    }
    .service-card p { font-size: .88rem; color: var(--muted); line-height: 1.65; }
    /* ── WHY CHOOSE ── */
    .why { background: var(--teal); position: relative; overflow: hidden; }
    .why::before {
      content: '';
      position: absolute; inset: 0;
      background-image: radial-gradient(rgba(255,255,255,.05) 1px, transparent 1px);
      background-size: 28px 28px;
    }
    .why .section-title { color: var(--white); }
    .why .section-lead { color: rgba(255,255,255,.75); }
    .why .section-tag { background: rgba(255,255,255,.15); color: rgba(255,255,255,.9); border-color: rgba(255,255,255,.2); }
    .why-grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(240px, 1fr));
      gap: 1.25rem;
    }
    .why-item {
      background: rgba(255,255,255,.1); border: 1px solid rgba(255,255,255,.18);
      border-radius: 16px; padding: 1.75rem;
      transition: background .2s, transform .2s;
    }
    .why-item:hover { background: rgba(255,255,255,.16); transform: translateY(-4px); }
    .why-item .icon { font-size: 1.5rem; margin-bottom: .75rem; display: block; }
    .why-item h4 { font-size: 1.05rem; color: var(--white); font-family: 'DM Sans', sans-serif; font-weight: 600; }
    /* ── AREA ── */
    .area { background: var(--off-white); }
    .area-inner {
      display: grid; grid-template-columns: 1fr 1fr;
      gap: 4rem; align-items: center;
    }
    .area-map-placeholder {
      background: var(--white);
      border: 1px solid var(--border);
      border-radius: 20px; height: 320px;
      display: flex; flex-direction: column;
      align-items: center; justify-content: center;
      gap: 1rem;
      box-shadow: 0 4px 30px rgba(10,124,110,.07);
    }
    .area-map-placeholder .map-icon { font-size: 3.5rem; }
    .area-map-placeholder p { font-size: .9rem; color: var(--muted); text-align: center; }
    .area-map-placeholder strong { display: block; font-size: 1.1rem; color: var(--teal); margin-bottom: .25rem; }
    /* ── CONTACT ── */
    .contact { background: var(--white); }
    .contact-grid {
      display: grid; grid-template-columns: 1fr 1fr;
      gap: 4rem; align-items: start;
    }
    .contact-info { display: flex; flex-direction: column; gap: 1.25rem; }
    .contact-card {
      display: flex; align-items: flex-start; gap: 1rem;
      padding: 1.25rem 1.5rem;
      border: 1px solid var(--border); border-radius: 14px;
      background: var(--off-white);
      transition: border-color .2s, transform .2s;
      text-decoration: none; color: inherit;
    }
    .contact-card:hover { border-color: var(--teal); transform: translateX(4px); }
    .contact-card .ci {
      width: 44px; height: 44px; border-radius: 10px;
      background: var(--teal-bg); display: grid; place-items: center;
      font-size: 1.2rem; flex-shrink: 0;
    }
    .contact-card .ct strong { display: block; font-weight: 600; font-size: .88rem; color: var(--muted); margin-bottom: .15rem; }
    .contact-card .ct span { font-size: 1rem; color: var(--ink); font-weight: 500; }
    .contact-form-box {
      background: var(--off-white);
      border: 1px solid var(--border);
      border-radius: 20px; padding: 2.5rem;
    }
    .contact-form-box h3 { font-size: 1.6rem; color: var(--ink); margin-bottom: 1.5rem; }
    .form-group { display: flex; flex-direction: column; gap: .4rem; margin-bottom: 1rem; }
    .form-group label { font-size: .82rem; font-weight: 600; color: var(--muted); letter-spacing: .04em; }
    .form-group input,
    .form-group select,
    .form-group textarea {
      border: 1px solid var(--border); border-radius: 10px;
      padding: .75rem 1rem; font-family: 'DM Sans', sans-serif;
      font-size: .92rem; color: var(--ink);
      background: var(--white);
      outline: none; transition: border-color .2s;
      resize: vertical;
    }
    .form-group input:focus,
    .form-group select:focus,
    .form-group textarea:focus { border-color: var(--teal); }
    .form-row { display: grid; grid-template-columns: 1fr 1fr; gap: 1rem; }
    .btn-form {
      width: 100%; background: var(--teal); color: var(--white);
      border: none; border-radius: 10px; padding: .9rem;
      font-size: .95rem; font-weight: 600; cursor: pointer;
      font-family: 'DM Sans', sans-serif;
      transition: background .2s, transform .15s;
    }
    .btn-form:hover { background: var(--teal-lt); transform: translateY(-1px); }
    /* ── WHATSAPP FLOAT ── */
    .wa-float {
      position: fixed; bottom: 28px; right: 28px; z-index: 888;
      width: 58px; height: 58px; border-radius: 50%;
      background: #25D366;
      display: grid; place-items: center;
      box-shadow: 0 6px 24px rgba(37,211,102,.4);
      text-decoration: none;
      animation: waBounce 2.5s 3s ease infinite;
      transition: transform .2s;
    }
    .wa-float:hover { transform: scale(1.1); animation: none; }
    .wa-float svg { width: 30px; height: 30px; fill: white; }
    @keyframes waBounce {
      0%,100%{ transform: translateY(0); }
      50%{ transform: translateY(-8px); }
    }
    /* ── FORMS ── */
    .forms-section { background: var(--off-white); }
    .forms-tabs {
      display: flex; gap: 1rem; margin-bottom: 2.5rem; flex-wrap: wrap;
    }
    .tab-btn {
      padding: .65rem 1.5rem; border-radius: 50px;
      border: 1.5px solid var(--border); background: var(--white);
      font-family: 'DM Sans', sans-serif; font-size: .9rem; font-weight: 600;
      color: var(--muted); cursor: pointer;
      transition: all .2s;
    }
    .tab-btn.active {
      background: var(--teal); color: var(--white); border-color: var(--teal);
    }
    .tab-btn:hover:not(.active) { border-color: var(--teal); color: var(--teal); }
    .form-panels { position: relative; }
    .form-panel { display: none; }
    .form-panel.active { display: block; }
    .gform-wrap {
      background: var(--white); border: 1px solid var(--border);
      border-radius: 20px; overflow: hidden;
      box-shadow: 0 8px 40px rgba(10,124,110,.08);
    }
    .gform-wrap iframe {
      width: 100%; min-height: 720px; border: none; display: block;
    }
    .gform-header {
      background: var(--teal); padding: 1.5rem 2rem;
      display: flex; align-items: center; gap: 1rem;
    }
    .gform-header .gh-icon {
      width: 44px; height: 44px; background: rgba(255,255,255,.2);
      border-radius: 10px; display: grid; place-items: center; font-size: 1.3rem;
      flex-shrink: 0;
    }
    .gform-header h3 { color: var(--white); font-size: 1.3rem; }
    .gform-header p { color: rgba(255,255,255,.75); font-size: .83rem; margin-top: .15rem; }
    .gform-fallback {
      padding: 2.5rem; text-align: center; display: none;
    }
    .gform-fallback p { color: var(--muted); margin-bottom: 1rem; font-size: .9rem; }
    .gform-fallback a {
      display: inline-block; background: var(--teal); color: var(--white);
      padding: .75rem 2rem; border-radius: 50px; text-decoration: none;
      font-weight: 600; font-size: .9rem; transition: background .2s;
    }
    .gform-fallback a:hover { background: var(--teal-lt); }
    /* ── SOCIAL MEDIA ── */
    .social-bar {
      background: var(--ink);
      padding: 60px 6vw;
      text-align: center;
    }
    .social-bar h3 {
      font-family: 'Cormorant Garamond', serif;
      font-size: 1.8rem; color: var(--white);
      margin-bottom: .5rem;
    }
    .social-bar p { color: rgba(255,255,255,.55); font-size: .88rem; margin-bottom: 2rem; }
    .social-icons {
      display: flex; flex-wrap: wrap;
      justify-content: center; gap: 1rem;
    }
    .social-btn {
      display: flex; align-items: center; gap: .6rem;
      padding: .75rem 1.5rem; border-radius: 50px;
      text-decoration: none; font-weight: 600; font-size: .88rem;
      transition: transform .2s, box-shadow .2s;
      border: 1.5px solid transparent;
    }
    .social-btn:hover { transform: translateY(-3px); box-shadow: 0 8px 24px rgba(0,0,0,.25); }
    .social-btn svg { width: 18px; height: 18px; flex-shrink: 0; }
    .social-btn.instagram { background: linear-gradient(135deg,#f09433,#e6683c,#dc2743,#cc2366,#bc1888); color: white; }
    .social-btn.facebook  { background: #1877F2; color: white; }
    .social-btn.youtube   { background: #FF0000; color: white; }
    .social-btn.threads   { background: #101010; color: white; border-color: #333; }
    .social-btn.whatsapp  { background: #25D366; color: white; }
    footer .f-social {
      display: flex; justify-content: center; gap: 1rem;
      margin-bottom: 1.25rem; flex-wrap: wrap;
    }
    footer .f-social a {
      width: 36px; height: 36px; border-radius: 50%;
      background: rgba(255,255,255,.1); border: 1px solid rgba(255,255,255,.15);
      display: grid; place-items: center;
      transition: background .2s, transform .2s;
      text-decoration: none; font-size: .95rem;
    }
    footer .f-social a:hover { background: rgba(255,255,255,.2); transform: translateY(-2px); }
    /* ── FOOTER ── */
    footer {
      background: var(--ink); color: rgba(255,255,255,.65);
      padding: 3rem 6vw;
      text-align: center;
    }
    footer .f-logo {
      font-family: 'Cormorant Garamond', serif;
      font-size: 1.4rem; color: var(--white);
      display: block; margin-bottom: .5rem;
    }
    footer .f-tagline { font-size: .85rem; margin-bottom: 1.5rem; line-height: 1.7; }
    footer .f-links { display: flex; justify-content: center; flex-wrap: wrap; gap: .75rem 1.75rem; margin-bottom: 1.5rem; }
    footer .f-links a { color: rgba(255,255,255,.55); text-decoration: none; font-size: .83rem; transition: color .2s; }
    footer .f-links a:hover { color: var(--white); }
    footer .f-copy { font-size: .78rem; border-top: 1px solid rgba(255,255,255,.1); padding-top: 1.25rem; }
    /* ── ANIMATIONS ON SCROLL ── */
    .reveal { opacity: 0; transform: translateY(28px); transition: opacity .7s ease, transform .7s ease; }
    .reveal.visible { opacity: 1; transform: translateY(0); }
    /* ── RESPONSIVE ── */
    @media (max-width: 900px) {
      .about-grid,
      .area-inner,
      .contact-grid { grid-template-columns: 1fr; }
      .about-card-float { position: static; margin-top: 1rem; }
      .nav-links { display: none; }
    }
    @media (max-width: 600px) {
      section { padding: 70px 5vw; }
      .form-row { grid-template-columns: 1fr; }
      .hero { padding: 110px 5vw 60px; }
    }
  </style>
</head>
<body>
<!-- NAV -->
<nav>
  <a class="nav-logo" href="#">OncoSupport <span>Care</span></a>
  <ul class="nav-links">
    <li><a href="#about">About</a></li>
    <li><a href="#services">Services</a></li>
    <li><a href="#why">Why Us</a></li>
    <li><a href="#forms">Forms</a></li>
    <li><a href="#social">Social</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
  <a class="nav-cta" href="#" onclick="openBooking(); return false;">📋 Book a Home Visit</a>
</nav>
<!-- HERO -->
<section class="hero" id="home">
  <div class="hero-bg-pattern"></div>
  <div class="hero-dots"></div>
  <div class="hero-inner">
    <div class="hero-badge">
      <span class="dot"></span>
      Kharghar, Navi Mumbai
    </div>
    <h1>Care, Comfort &amp;<br/><em>Hope at Home</em></h1>
    <p class="hero-sub">Professional nursing care and patient support services delivered in the comfort of your home. Compassionate. Qualified. Trusted.</p>
    <div class="hero-actions">
      <a class="btn-primary" href="#" onclick="openBooking(); return false;">📋 Book a Home Visit</a>
    </div>
    <div class="hero-trust">
      <span class="trust-item"><span class="check">✔</span> Qualified Nurses</span>
      <span class="trust-item"><span class="check">✔</span> Oncology Specialists</span>
      <span class="trust-item"><span class="check">✔</span> Palliative Care</span>
      <span class="trust-item"><span class="check">✔</span> 24/7 Support</span>
    </div>
  </div>
</section>
<!-- ABOUT -->
<section class="about" id="about">
  <div class="about-grid">
    <div class="about-visual reveal">
      <div class="about-card-main">
        <h3>Caring Beyond Treatment</h3>
        <p>OncoSupport Care (OSC) is a trusted home healthcare provider based in Kharghar, Navi Mumbai. We specialize in delivering personalized healthcare services at home, helping patients recover comfortably while maintaining their independence and quality of life.</p>
        <p style="margin-top:1rem;">Our team is committed to providing safe, compassionate, and professional care tailored to each patient's unique needs.</p>
      </div>
      <div class="about-card-float">
        <div class="big">💙💚</div>
        <div class="label">Compassion · Dignity · Respect</div>
      </div>
    </div>
    <div class="reveal" style="transition-delay:.15s">
      <div class="section-tag">About Us</div>
      <h2 class="section-title">Why Families Trust OSC</h2>
      <p class="section-lead">We believe quality healthcare should not be limited to hospitals. Our mission is to bring expert medical support directly to your doorstep.</p>
      <div class="values-list">
        <div class="value-item">
          <div class="value-icon">🏥</div>
          <div class="value-text">
            <strong>Specialized Oncology Care</strong>
            <span>Expert home care for cancer patients and their families</span>
          </div>
        </div>
        <div class="value-item">
          <div class="value-icon">❤️</div>
          <div class="value-text">
            <strong>Palliative & Comfort Care</strong>
            <span>Focused on dignity, pain relief, and emotional well-being</span>
          </div>
        </div>
        <div class="value-item">
          <div class="value-icon">📋</div>
          <div class="value-text">
            <strong>Personalized Care Plans</strong>
            <span>Every patient receives a plan tailored to their specific needs</span>
          </div>
        </div>
        <div class="value-item">
          <div class="value-icon">🤝</div>
          <div class="value-text">
            <strong>Affordable & Accessible</strong>
            <span>Quality healthcare solutions that don't break your budget</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>
<!-- SERVICES -->
<section class="services" id="services">
  <div class="section-header reveal">
    <div class="section-tag">What We Offer</div>
    <h2 class="section-title">Our Services</h2>
    <p class="section-lead">Comprehensive home healthcare services delivered with professionalism and a human touch.</p>
  </div>
  <div class="services-grid">
    <div class="service-card reveal">
      <div class="service-emoji">🩺</div>
      <h3>Home Nursing Care</h3>
      <p>Professional nursing support for patients requiring medical care at home, ensuring clinical standards are maintained.</p>
    </div>
    <div class="service-card reveal" style="transition-delay:.07s">
      <div class="service-emoji">💉</div>
      <h3>Injection &amp; IV Therapy</h3>
      <p>Safe administration of injections, IV infusions, and comprehensive medication management by trained nurses.</p>
    </div>
    <div class="service-card reveal" style="transition-delay:.14s">
      <div class="service-emoji">🩹</div>
      <h3>Wound Dressing Care</h3>
      <p>Expert wound assessment and sterile dressing services to promote healing and prevent infection.</p>
    </div>
    <div class="service-card reveal" style="transition-delay:.21s">
      <div class="service-emoji">👵</div>
      <h3>Elderly Care</h3>
      <p>Dedicated care and compassionate support for senior citizens, helping them live with dignity and independence.</p>
    </div>
    <div class="service-card reveal" style="transition-delay:.28s">
      <div class="service-emoji">🛏</div>
      <h3>Patient Attendant Services</h3>
      <p>Reliable assistance with daily activities, personal hygiene, mobility, and round-the-clock patient care.</p>
    </div>
    <div class="service-card reveal" style="transition-delay:.35s">
      <div class="service-emoji">🏥</div>
      <h3>Post-Hospitalization Care</h3>
      <p>Structured recovery support after hospital discharge to ensure a smooth, safe return to full health.</p>
    </div>
    <div class="service-card reveal" style="transition-delay:.42s">
      <div class="service-emoji">🎗</div>
      <h3>Oncology Home Care</h3>
      <p>Specialized care plans for cancer patients — physical, emotional, and medical support throughout the journey.</p>
    </div>
    <div class="service-card reveal" style="transition-delay:.49s">
      <div class="service-emoji">❤️</div>
      <h3>Palliative Care Support</h3>
      <p>Comfort-focused care for patients with serious illnesses, prioritizing quality of life and family peace of mind.</p>
    </div>
  </div>
</section>
<!-- WHY CHOOSE -->
<section class="why" id="why">
  <div class="section-header reveal">
    <div class="section-tag">Why Choose Us</div>
    <h2 class="section-title">The OSC Difference</h2>
    <p class="section-lead">We combine clinical expertise with heartfelt compassion to deliver care that truly makes a difference.</p>
  </div>
  <div class="why-grid">
    <div class="why-item reveal">
      <span class="icon">👨‍⚕️</span>
      <h4>Qualified Healthcare Professionals</h4>
    </div>
    <div class="why-item reveal" style="transition-delay:.08s">
      <span class="icon">📋</span>
      <h4>Personalized Care Plans</h4>
    </div>
    <div class="why-item reveal" style="transition-delay:.16s">
      <span class="icon">🏠</span>
      <h4>Home-Based Medical Support</h4>
    </div>
    <div class="why-item reveal" style="transition-delay:.24s">
      <span class="icon">💙</span>
      <h4>Reliable &amp; Compassionate Service</h4>
    </div>
    <div class="why-item reveal" style="transition-delay:.32s">
      <span class="icon">🚗</span>
      <h4>Convenient Home Visits</h4>
    </div>
    <div class="why-item reveal" style="transition-delay:.40s">
      <span class="icon">💰</span>
      <h4>Affordable Healthcare Solutions</h4>
    </div>
  </div>
</section>
<!-- SERVICE AREA -->
<section class="area" id="area">
  <div class="area-inner">
    <div class="reveal">
      <div class="section-tag">Service Area</div>
      <h2 class="section-title">Where We Serve</h2>
      <p class="section-lead">Primarily serving Kharghar, Navi Mumbai. We also extend our services to nearby areas across Navi Mumbai and Thane based on availability.</p>
      <div style="margin-top:2rem; display:flex; flex-direction:column; gap:.75rem;">
        <div class="value-item">
          <div class="value-icon">📍</div>
          <div class="value-text">
            <strong>Kharghar, Navi Mumbai</strong>
            <span>Primary service zone — full coverage</span>
          </div>
        </div>
        <div class="value-item">
          <div class="value-icon">🗺️</div>
          <div class="value-text">
            <strong>Navi Mumbai &amp; Thane</strong>
            <span>Extended service areas based on availability</span>
          </div>
        </div>
      </div>
    </div>
    <div class="area-map-placeholder reveal" style="transition-delay:.15s">
      <div class="map-icon">📍</div>
      <div>
        <strong>Kharghar, Navi Mumbai</strong>
        <p>Maharashtra, India</p>
      </div>
      <a href="#" onclick="window.open('https://maps.google.com/?q=Kharghar,Navi+Mumbai','_blank'); return false;"
             style="font-size:.84rem; color:var(--teal); font-weight:600; text-decoration:none; border:1px solid var(--border); padding:.4rem 1rem; border-radius:50px;">Open in Maps →</a>
    </div>
  </div>
</section>
<!-- CONTACT -->
<section class="contact" id="contact">
  <div class="section-header reveal">
    <div class="section-tag">Get In Touch</div>
    <h2 class="section-title">Book a Home Visit</h2>
    <p class="section-lead">Reach out today and we'll arrange a visit at your convenience. Fill out the form below or contact us directly.</p>
  </div>
  <div class="contact-grid">
    <div class="contact-info reveal">
      <a class="contact-card" href="tel:+919324563795">
        <div class="ci">📞</div>
        <div class="ct">
          <strong>Call / WhatsApp</strong>
          <span>+91 93245 63795</span>
        </div>
      </a>
      <a class="contact-card" href="mailto:OncoSupport@gmail.com">
        <div class="ci">📧</div>
        <div class="ct">
          <strong>Email</strong>
          <span>OncoSupport@gmail.com</span>
        </div>
      </a>
      <div class="contact-card" style="cursor:default;">
        <div class="ci">📍</div>
        <div class="ct">
          <strong>Location</strong>
          <span>Kharghar, Navi Mumbai, Maharashtra</span>
        </div>
      </div>
  </div>
    <!-- WhatsApp Channel Banner -->
    <div class="reveal" style="margin-top:2.5rem;">
      <div style="background:linear-gradient(135deg,#0d524a,#0a7c6e); border-radius:20px; padding:2.5rem; color:white; text-align:center; box-shadow:0 8px 40px rgba(10,124,110,.2);">
        <div style="font-size:2.8rem; margin-bottom:1rem;">📢</div>
        <h3 style="font-family:'Cormorant Garamond',serif; font-size:1.8rem; color:white; margin-bottom:.6rem;">Follow Our WhatsApp Channel</h3>
        <p style="color:rgba(255,255,255,.8); font-size:.9rem; line-height:1.7; margin-bottom:.5rem;">
          OncoSupport Care 💙💚<br/>Care, Comfort &amp; Hope at Home
        </p>
        <p style="color:rgba(255,255,255,.7); font-size:.83rem; margin-bottom:1.75rem;">
          🏥 Oncology &amp; Home Healthcare Services · Navi Mumbai &amp; Thane
        </p>
        <a href="https://whatsapp.com/channel/0029VbCZD762f3EPHPTsTi3W"
           target="_blank"
           onclick="window.open('https://whatsapp.com/channel/0029VbCZD762f3EPHPTsTi3W','_blank'); return false;"
           style="display:inline-flex; align-items:center; gap:.6rem; background:#25D366; color:white;
                  padding:.85rem 2rem; border-radius:50px; text-decoration:none;
                  font-weight:600; font-size:.95rem; box-shadow:0 4px 20px rgba(37,211,102,.4);"
           onmouseover="this.style.transform='translateY(-2px)'"
           onmouseout="this.style.transform='translateY(0)'">
          Follow WhatsApp Channel →
        </a>
      </div>
    </div>
</section>
<!-- FORMS SECTION — tabbed -->
<section class="forms-section" id="forms">
  <div class="section-header reveal">
    <div class="section-tag">Forms</div>
    <h2 class="section-title">Submit a Form</h2>
    <p class="section-lead">Fill out the Patient Enquiry Form below and we'll get back to you shortly.</p>
  </div>
  
  <div class="form-panels">
    <div class="form-panel active" id="panel-patient">
      <div class="gform-wrap reveal">
        <div class="gform-header">
          <div class="gh-icon">🏥</div>
          <div>
            <h3>Patient Enquiry Form</h3>
            <p>Tell us about your healthcare needs and we'll contact you</p>
          </div>
        </div>
        <iframe src="https://forms.gle/XSboS9fBrBnbCreE7" title="OncoSupport Care – Patient Enquiry Form">Loading…</iframe>
        <div style="padding:1rem 2rem 1.5rem;text-align:center;border-top:1px solid var(--border);">
          <a href="https://forms.gle/XSboS9fBrBnbCreE7" target="_blank"
             style="font-size:.85rem;color:var(--teal);font-weight:600;text-decoration:none;">
            🔗 Open form in new tab →
          </a>
        </div>
      </div>
    </div>
    </div>
  </div>
  </div>
</section>
<!-- SOCIAL MEDIA -->
<section class="social-bar" id="social">
  <h3>Follow Us on Social Media</h3>
  <p>Stay connected for health tips, updates & more</p>
  <div class="social-icons">
    <a class="social-btn instagram" href="https://www.instagram.com/onco_supporthealth?igsh=MTBuZzFtMXAwY3Mx" target="_blank" rel="noopener">
      <svg viewBox="0 0 24 24" fill="white"><path d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zm0-2.163c-3.259 0-3.667.014-4.947.072-4.358.2-6.78 2.618-6.98 6.98-.059 1.281-.073 1.689-.073 4.948 0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98 1.281.058 1.689.072 4.948.072 3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98-1.281-.059-1.69-.073-4.949-.073zm0 5.838c-3.403 0-6.162 2.759-6.162 6.162s2.759 6.163 6.162 6.163 6.162-2.759 6.162-6.163c0-3.403-2.759-6.162-6.162-6.162zm0 10.162c-2.209 0-4-1.79-4-4 0-2.209 1.791-4 4-4s4 1.791 4 4c0 2.21-1.791 4-4 4zm6.406-11.845c-.796 0-1.441.645-1.441 1.44s.645 1.44 1.441 1.44c.795 0 1.439-.645 1.439-1.44s-.644-1.44-1.439-1.44z"/></svg>
      Instagram
    </a>
    <a class="social-btn facebook" href="https://www.facebook.com/share/1BmPsZXC4Q/" target="_blank" rel="noopener">
      <svg viewBox="0 0 24 24" fill="white"><path d="M24 12.073c0-6.627-5.373-12-12-12s-12 5.373-12 12c0 5.99 4.388 10.954 10.125 11.854v-8.385H7.078v-3.47h3.047V9.43c0-3.007 1.792-4.669 4.533-4.669 1.312 0 2.686.235 2.686.235v2.953H15.83c-1.491 0-1.956.925-1.956 1.874v2.25h3.328l-.532 3.47h-2.796v8.385C19.612 23.027 24 18.062 24 12.073z"/></svg>
      Facebook
    </a>
    <a class="social-btn youtube" href="https://youtube.com/@oncosupportcarecarecomforthope?si=UOM_ih9M3ioQK-gw" target="_blank" rel="noopener">
      <svg viewBox="0 0 24 24" fill="white"><path d="M23.498 6.186a3.016 3.016 0 0 0-2.122-2.136C19.505 3.545 12 3.545 12 3.545s-7.505 0-9.377.505A3.017 3.017 0 0 0 .502 6.186C0 8.07 0 12 0 12s0 3.93.502 5.814a3.016 3.016 0 0 0 2.122 2.136c1.871.505 9.376.505 9.376.505s7.505 0 9.377-.505a3.015 3.015 0 0 0 2.122-2.136C24 15.93 24 12 24 12s0-3.93-.502-5.814zM9.545 15.568V8.432L15.818 12l-6.273 3.568z"/></svg>
      YouTube
    </a>
    <a class="social-btn threads" href="https://www.threads.com/@onco_supporthealth" target="_blank" rel="noopener">
      <svg viewBox="0 0 24 24" fill="white"><path d="M12.186 24h-.007c-3.581-.024-6.334-1.205-8.184-3.509C2.35 18.44 1.5 15.586 1.472 12.01v-.017c.03-3.579.879-6.43 2.525-8.482C5.845 1.205 8.6.024 12.18 0h.014c2.746.02 5.043.725 6.826 2.098 1.677 1.29 2.858 3.13 3.509 5.467l-2.04.569c-1.104-3.96-3.898-5.984-8.304-6.015-2.91.022-5.11.936-6.54 2.717C4.307 6.504 3.616 8.914 3.589 12c.027 3.086.718 5.496 2.057 7.164 1.43 1.783 3.631 2.698 6.54 2.717 2.623-.02 4.358-.631 5.8-2.045 1.647-1.613 1.618-3.593 1.09-4.798-.31-.71-.873-1.3-1.634-1.75-.192 1.352-.622 2.446-1.284 3.272-.886 1.102-2.14 1.704-3.73 1.79-1.202.065-2.361-.218-3.259-.801-1.063-.689-1.685-1.74-1.752-2.964-.065-1.19.408-2.285 1.33-3.082.88-.76 2.119-1.207 3.583-1.291a13.853 13.853 0 0 1 3.02.142c-.126-.742-.375-1.332-.75-1.757-.513-.586-1.308-.883-2.371-.887h-.018c-.59 0-1.52.158-2.195 1.128l-1.699-1.17c.903-1.31 2.357-2.033 4.095-2.033h.025c2.726.018 4.stavbu.956 5.133 2.703.484 1.21.603 2.738.347 4.54.402.269.77.576 1.1.92 1.047 1.094 1.624 2.5 1.625 3.957.004 2.96-1.493 5.404-4.043 6.832C16.11 23.657 14.27 24 12.186 24z"/></svg>
      Threads
    </a>
    <a class="social-btn whatsapp" href="https://whatsapp.com/channel/0029VbCZD762f3EPHPTsTi3W" target="_blank" rel="noopener">
      <svg viewBox="0 0 24 24" fill="white"><path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347z"/><path d="M12 0C5.373 0 0 5.373 0 12c0 2.136.563 4.14 1.546 5.875L0 24l6.337-1.524A11.94 11.94 0 0012 24c6.627 0 12-5.373 12-12S18.627 0 12 0zm0 21.882a9.875 9.875 0 01-5.042-1.376l-.362-.214-3.762.905.958-3.664-.236-.376A9.875 9.875 0 012.118 12C2.118 6.553 6.553 2.118 12 2.118S21.882 6.553 21.882 12 17.447 21.882 12 21.882z"/></svg>
      WhatsApp Channel
    </a>
  </div>
</section>
<!-- BOOKING MODAL -->
<div id="bookingModal" style="
  display:none; position:fixed; inset:0; z-index:9999;
  background:rgba(10,40,36,.6); backdrop-filter:blur(6px);
  align-items:center; justify-content:center; padding:1.5rem;">
  <div style="
    background:var(--white); border-radius:24px;
    padding:2.5rem 2rem; max-width:420px; width:100%;
    box-shadow:0 24px 80px rgba(0,0,0,.25);
    animation: popIn .3s ease both;">
    <div style="text-align:center; margin-bottom:1.75rem;">
      <div style="font-size:2.5rem; margin-bottom:.75rem;">🏥</div>
      <h3 style="font-family:'Cormorant Garamond',serif; font-size:1.7rem; color:var(--ink); margin-bottom:.4rem;">Book a Home Visit</h3>
      <p style="font-size:.88rem; color:var(--muted); line-height:1.6;">Choose how you'd like to connect with us</p>
    </div>
    <a href="#"
       onclick="window.open('https://wa.me/919324563795?text=Hello%20OncoSupport%20Care%2C%20I%20would%20like%20to%20book%20a%20home%20visit.','_blank'); return false;"
       style="
         display:flex; align-items:center; gap:1rem;
         background:#25D366; color:white; text-decoration:none;
         border-radius:14px; padding:1.1rem 1.5rem;
         margin-bottom:.9rem; transition:transform .2s, box-shadow .2s;
         box-shadow: 0 4px 16px rgba(37,211,102,.3);"
       onmouseover="this.style.transform='translateY(-2px)'"
       onmouseout="this.style.transform='translateY(0)'">
      <span style="font-size:1.8rem; flex-shrink:0;">💬</span>
      <div>
        <strong style="display:block; font-size:1rem;">WhatsApp Chat</strong>
        <span style="font-size:.82rem; opacity:.9;">+91 93245 63795 · Chat instantly</span>
      </div>
      <span style="margin-left:auto; font-size:1.1rem;">→</span>
    </a>
    <a href="#"
       onclick="window.open('https://forms.gle/XSboS9fBrBnbCreE7','_blank'); return false;"
       style="
         display:flex; align-items:center; gap:1rem;
         background:var(--teal-bg); border:1.5px solid var(--border);
         color:var(--ink); text-decoration:none;
         border-radius:14px; padding:1.1rem 1.5rem;
         margin-bottom:1.5rem; transition:transform .2s, border-color .2s;"
       onmouseover="this.style.transform='translateY(-2px)'; this.style.borderColor='var(--teal)'"
       onmouseout="this.style.transform='translateY(0)'; this.style.borderColor='var(--border)'">
      <span style="font-size:1.8rem; flex-shrink:0;">📋</span>
      <div>
        <strong style="display:block; font-size:1rem; color:var(--teal);">Fill Enquiry Form</strong>
        <span style="font-size:.82rem; color:var(--muted);">Patient Enquiry · Google Form</span>
      </div>
      <span style="margin-left:auto; font-size:1.1rem; color:var(--teal);">→</span>
    </a>
    <button onclick="closeBooking()" style="
      width:100%; background:none; border:1px solid var(--border);
      border-radius:10px; padding:.65rem; font-family:'DM Sans',sans-serif;
      font-size:.88rem; color:var(--muted); cursor:pointer;
      transition:background .2s;"
      onmouseover="this.style.background='var(--off-white)'"
      onmouseout="this.style.background='none'">
      ✕ Close
    </button>
  </div>
</div>
<style>
@keyframes popIn {
  from { opacity:0; transform:scale(.92) translateY(16px); }
  to   { opacity:1; transform:scale(1)   translateY(0); }
}
</style>
<!-- FOOTER -->
<footer>
  <span class="f-logo">OncoSupport Care 💙💚</span>
  <p class="f-tagline">Care, Comfort &amp; Hope at Home<br/>Oncology &amp; Home Healthcare Services · Kharghar, Navi Mumbai</p>
  <div class="f-social">
    <a href="https://www.instagram.com/onco_supporthealth?igsh=MTBuZzFtMXAwY3Mx" target="_blank" rel="noopener" title="Instagram">📸</a>
    <a href="https://www.facebook.com/share/1BmPsZXC4Q/" target="_blank" rel="noopener" title="Facebook">📘</a>
    <a href="https://youtube.com/@oncosupportcarecarecomforthope?si=UOM_ih9M3ioQK-gw" target="_blank" rel="noopener" title="YouTube">▶️</a>
    <a href="https://www.threads.com/@onco_supporthealth" target="_blank" rel="noopener" title="Threads">🧵</a>
    <a href="https://whatsapp.com/channel/0029VbCZD762f3EPHPTsTi3W" target="_blank" rel="noopener" title="WhatsApp">💬</a>
  </div>
  <div class="f-links">
    <a href="#about">About Us</a>
    <a href="#services">Services</a>
    <a href="#why">Why Us</a>
    <a href="#area">Service Area</a>
    <a href="#forms">Forms</a>
    <a href="#contact">Contact</a>
    <a href="tel:+919324563795">+91 93245 63795</a>
    <a href="mailto:OncoSupport@gmail.com">OncoSupport@gmail.com</a>
  </div>
  <p class="f-copy">© 2025 OncoSupport Care. All rights reserved. · Serving Navi Mumbai &amp; Thane</p>
</footer>
<!-- WHATSAPP FLOAT -->
<a class="wa-float" href="#" onclick="window.open('https://wa.me/919324563795','_blank'); return false;" title="WhatsApp Us">
  <svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
    <path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347z"/>
    <path d="M12 0C5.373 0 0 5.373 0 12c0 2.136.563 4.14 1.546 5.875L0 24l6.337-1.524A11.94 11.94 0 0012 24c6.627 0 12-5.373 12-12S18.627 0 12 0zm0 21.882a9.875 9.875 0 01-5.042-1.376l-.362-.214-3.762.905.958-3.664-.236-.376A9.875 9.875 0 012.118 12C2.118 6.553 6.553 2.118 12 2.118S21.882 6.553 21.882 12 17.447 21.882 12 21.882z"/>
  </svg>
</a>
<script>
  // Booking modal
  const modal = document.getElementById('bookingModal');
  function openBooking() {
    modal.style.display = 'flex';
    document.body.style.overflow = 'hidden';
  }
  function closeBooking() {
    modal.style.display = 'none';
    document.body.style.overflow = '';
  }
  modal.addEventListener('click', function(e) {
    if (e.target === modal) closeBooking();
  });
  // Tab switching for forms
  function switchTab(tab, btn) {
    document.querySelectorAll('.form-panel').forEach(p => p.classList.remove('active'));
    document.querySelectorAll('.tab-btn').forEach(b => b.classList.remove('active'));
    document.getElementById('panel-' + tab).classList.add('active');
    btn.classList.add('active');
  }
  // Scroll reveal
  const reveals = document.querySelectorAll('.reveal');
  const observer = new IntersectionObserver((entries) => {
    entries.forEach(e => {
      if (e.isIntersecting) {
        e.target.classList.add('visible');
        observer.unobserve(e.target);
      }
    });
  }, { threshold: 0.12 });
  reveals.forEach(el => observer.observe(el));
  // Nav shadow on scroll
  const nav = document.querySelector('nav');
  window.addEventListener('scroll', () => {
    nav.style.boxShadow = window.scrollY > 20
      ? '0 4px 24px rgba(10,124,110,.1)' : 'none';
  });
</script>
</body>
