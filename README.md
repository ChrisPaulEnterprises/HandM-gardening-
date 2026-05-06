<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Greenfield Landscaping | 30 Years of Excellence</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;0,900;1,400&family=DM+Sans:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
  :root {
    --green-deep: #1a3a1f;
    --green-mid: #2d5a35;
    --green-fresh: #4a8c55;
    --green-light: #7ab87e;
    --gold: #c9a84c;
    --gold-light: #e8c97a;
    --cream: #f7f3ec;
    --warm-white: #fdfaf5;
    --text-dark: #1a1a18;
    --text-mid: #3a3a36;
    --text-light: #6e6e68;
  }

  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  html { scroll-behavior: smooth; }

  body {
    font-family: 'DM Sans', sans-serif;
    background: var(--warm-white);
    color: var(--text-dark);
    overflow-x: hidden;
  }

  /* ── NAV ── */
  nav {
    position: fixed; top: 0; left: 0; right: 0; z-index: 100;
    display: flex; align-items: center; justify-content: space-between;
    padding: 1.2rem 5%;
    background: rgba(26, 58, 31, 0.97);
    backdrop-filter: blur(12px);
    border-bottom: 1px solid rgba(201,168,76,.2);
  }
  .nav-logo {
    font-family: 'Playfair Display', serif;
    font-size: 1.5rem; font-weight: 900;
    color: var(--cream);
    letter-spacing: -.5px;
    display: flex; align-items: center; gap: .5rem;
  }
  .nav-logo span { color: var(--gold); }
  .nav-links { display: flex; gap: 2rem; list-style: none; }
  .nav-links a {
    color: rgba(247,243,236,.8);
    text-decoration: none; font-size: .9rem; font-weight: 500;
    letter-spacing: .03em;
    transition: color .2s;
  }
  .nav-links a:hover { color: var(--gold-light); }
  .nav-cta {
    background: var(--gold); color: var(--green-deep);
    padding: .65rem 1.6rem; border-radius: 2px;
    font-weight: 600; font-size: .9rem;
    text-decoration: none; letter-spacing: .03em;
    transition: background .2s, transform .15s;
  }
  .nav-cta:hover { background: var(--gold-light); transform: translateY(-1px); }

  /* ── HERO ── */
  .hero {
    min-height: 100vh;
    background:
      linear-gradient(160deg, rgba(26,58,31,.82) 0%, rgba(26,58,31,.55) 50%, rgba(26,58,31,.75) 100%),
      url('https://images.unsplash.com/photo-1558618666-fcd25c85cd64?w=1600&q=80') center/cover no-repeat;
    display: flex; flex-direction: column; justify-content: center;
    padding: 10rem 5% 5rem;
    position: relative; overflow: hidden;
  }
  .hero::after {
    content: '';
    position: absolute; bottom: 0; left: 0; right: 0; height: 120px;
    background: linear-gradient(to bottom, transparent, var(--warm-white));
  }
  .hero-badge {
    display: inline-flex; align-items: center; gap: .5rem;
    background: rgba(201,168,76,.18); border: 1px solid rgba(201,168,76,.4);
    color: var(--gold-light); padding: .45rem 1.1rem; border-radius: 2px;
    font-size: .8rem; font-weight: 600; letter-spacing: .1em; text-transform: uppercase;
    margin-bottom: 1.8rem;
    animation: fadeUp .7s ease both;
  }
  .hero h1 {
    font-family: 'Playfair Display', serif;
    font-size: clamp(3rem, 7vw, 6.5rem);
    font-weight: 900; line-height: 1.02;
    color: var(--cream);
    max-width: 820px;
    animation: fadeUp .7s .15s ease both;
  }
  .hero h1 em { color: var(--gold); font-style: italic; }
  .hero-sub {
    margin-top: 1.5rem;
    font-size: clamp(1rem, 1.8vw, 1.2rem);
    color: rgba(247,243,236,.8);
    max-width: 540px; line-height: 1.7;
    font-weight: 300;
    animation: fadeUp .7s .3s ease both;
  }
  .hero-actions {
    display: flex; gap: 1rem; margin-top: 2.5rem; flex-wrap: wrap;
    animation: fadeUp .7s .45s ease both;
  }
  .btn-primary {
    background: var(--gold); color: var(--green-deep);
    padding: 1rem 2.5rem; border-radius: 2px;
    font-weight: 700; font-size: 1rem; letter-spacing: .03em;
    text-decoration: none; border: none; cursor: pointer;
    transition: background .2s, transform .15s, box-shadow .2s;
    box-shadow: 0 4px 20px rgba(201,168,76,.3);
  }
  .btn-primary:hover {
    background: var(--gold-light); transform: translateY(-2px);
    box-shadow: 0 8px 30px rgba(201,168,76,.4);
  }
  .btn-outline {
    background: transparent; color: var(--cream);
    padding: 1rem 2.5rem; border-radius: 2px;
    font-weight: 500; font-size: 1rem;
    text-decoration: none;
    border: 1.5px solid rgba(247,243,236,.4);
    transition: border-color .2s, background .2s;
  }
  .btn-outline:hover {
    border-color: var(--cream);
    background: rgba(247,243,236,.08);
  }
  .hero-stats {
    display: flex; gap: 3rem; margin-top: 4rem;
    animation: fadeUp .7s .6s ease both;
  }
  .stat-item { display: flex; flex-direction: column; gap: .2rem; }
  .stat-num {
    font-family: 'Playfair Display', serif;
    font-size: 2.4rem; font-weight: 900; color: var(--gold);
    line-height: 1;
  }
  .stat-label {
    font-size: .8rem; color: rgba(247,243,236,.65);
    letter-spacing: .08em; text-transform: uppercase; font-weight: 500;
  }

  /* ── TRUST BAR ── */
  .trust-bar {
    background: var(--green-deep);
    padding: 1.5rem 5%;
    display: flex; align-items: center; justify-content: center;
    gap: 3rem; flex-wrap: wrap;
  }
  .trust-item {
    display: flex; align-items: center; gap: .7rem;
    color: rgba(247,243,236,.8); font-size: .88rem; font-weight: 500;
  }
  .trust-icon { font-size: 1.1rem; }
  .trust-divider { width: 1px; height: 20px; background: rgba(247,243,236,.15); }

  /* ── SECTIONS SHARED ── */
  section { padding: 7rem 5%; }

  .section-label {
    font-size: .75rem; letter-spacing: .18em; text-transform: uppercase;
    font-weight: 600; color: var(--green-fresh);
    margin-bottom: .8rem;
  }
  .section-title {
    font-family: 'Playfair Display', serif;
    font-size: clamp(2rem, 4vw, 3.2rem);
    font-weight: 900; line-height: 1.12;
    color: var(--green-deep);
  }
  .section-title em { color: var(--gold); font-style: italic; }

  /* ── ABOUT ── */
  .about { background: var(--cream); }
  .about-grid {
    display: grid; grid-template-columns: 1fr 1fr;
    gap: 6rem; align-items: center;
    max-width: 1200px; margin: 0 auto;
  }
  .about-img-wrap {
    position: relative;
  }
  .about-img-wrap img {
    width: 100%; height: 520px; object-fit: cover;
    border-radius: 2px;
    box-shadow: 0 30px 80px rgba(26,58,31,.15);
  }
  .about-img-badge {
    position: absolute; bottom: -1.5rem; right: -1.5rem;
    background: var(--green-deep); color: var(--cream);
    padding: 1.5rem 2rem; border-radius: 2px;
    text-align: center;
    box-shadow: 0 10px 40px rgba(26,58,31,.3);
  }
  .about-img-badge .num {
    font-family: 'Playfair Display', serif;
    font-size: 3.5rem; font-weight: 900;
    color: var(--gold); line-height: 1;
  }
  .about-img-badge .label {
    font-size: .78rem; letter-spacing: .12em;
    text-transform: uppercase; color: rgba(247,243,236,.7);
    margin-top: .3rem;
  }
  .about-content { padding-top: 1rem; }
  .about-content p {
    font-size: 1.05rem; line-height: 1.8; color: var(--text-mid);
    margin-top: 1.5rem; font-weight: 300;
  }
  .about-features { margin-top: 2.5rem; display: flex; flex-direction: column; gap: 1rem; }
  .about-feature {
    display: flex; gap: 1rem; align-items: flex-start;
  }
  .feature-dot {
    width: 8px; height: 8px; border-radius: 50%;
    background: var(--gold); margin-top: .55rem; flex-shrink: 0;
  }
  .feature-text strong { display: block; font-weight: 600; color: var(--green-deep); }
  .feature-text span { font-size: .93rem; color: var(--text-light); }

  /* ── SERVICES ── */
  .services { background: var(--warm-white); }
  .services-header { max-width: 600px; margin-bottom: 4rem; }
  .services-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 1.5px;
    background: #d0d0c8;
    border-radius: 2px; overflow: hidden;
    max-width: 1200px;
  }
  .service-card {
    background: var(--warm-white);
    padding: 2.8rem 2.5rem;
    position: relative; overflow: hidden;
    transition: background .3s;
    cursor: default;
  }
  .service-card::before {
    content: '';
    position: absolute; bottom: 0; left: 0; right: 0; height: 3px;
    background: var(--gold);
    transform: scaleX(0); transform-origin: left;
    transition: transform .4s cubic-bezier(.4,0,.2,1);
  }
  .service-card:hover { background: var(--cream); }
  .service-card:hover::before { transform: scaleX(1); }
  .service-icon {
    font-size: 2.2rem; margin-bottom: 1.2rem; display: block;
  }
  .service-card h3 {
    font-family: 'Playfair Display', serif;
    font-size: 1.35rem; font-weight: 700;
    color: var(--green-deep); margin-bottom: .8rem;
  }
  .service-card p {
    font-size: .93rem; line-height: 1.7; color: var(--text-light);
  }
  .service-link {
    display: inline-flex; align-items: center; gap: .4rem;
    margin-top: 1.5rem; font-size: .88rem; font-weight: 600;
    color: var(--green-fresh); text-decoration: none;
    transition: gap .2s;
  }
  .service-link:hover { gap: .8rem; }

  /* ── PROCESS ── */
  .process { background: var(--green-deep); position: relative; overflow: hidden; }
  .process::before {
    content: '';
    position: absolute; top: -100px; right: -100px;
    width: 500px; height: 500px; border-radius: 50%;
    background: rgba(74,140,85,.08);
  }
  .process-header { max-width: 600px; margin-bottom: 4rem; }
  .process-header .section-label { color: var(--gold-light); }
  .process-header .section-title { color: var(--cream); }
  .process-steps {
    display: grid; grid-template-columns: repeat(4, 1fr);
    gap: 2rem; position: relative;
    max-width: 1200px;
  }
  .process-steps::before {
    content: '';
    position: absolute; top: 2rem; left: 12%; right: 12%;
    height: 1px; background: rgba(201,168,76,.25);
  }
  .process-step { text-align: center; padding: 0 1rem; }
  .step-num {
    width: 4rem; height: 4rem; border-radius: 50%;
    background: rgba(201,168,76,.12); border: 1.5px solid rgba(201,168,76,.35);
    display: flex; align-items: center; justify-content: center;
    margin: 0 auto 1.5rem;
    font-family: 'Playfair Display', serif;
    font-size: 1.2rem; font-weight: 900; color: var(--gold);
    position: relative; z-index: 1;
    background: var(--green-deep);
  }
  .process-step h4 {
    font-family: 'Playfair Display', serif;
    font-size: 1.1rem; font-weight: 700;
    color: var(--cream); margin-bottom: .6rem;
  }
  .process-step p {
    font-size: .88rem; line-height: 1.65;
    color: rgba(247,243,236,.55);
  }

  /* ── REVIEWS ── */
  .reviews { background: var(--cream); }
  .reviews-header { max-width: 600px; margin-bottom: 1rem; }
  .stars-summary {
    display: flex; align-items: center; gap: 1rem;
    margin-bottom: 3.5rem;
  }
  .stars-big { font-size: 1.8rem; letter-spacing: .1em; color: var(--gold); }
  .stars-meta strong {
    font-family: 'Playfair Display', serif;
    font-size: 2rem; font-weight: 900; color: var(--green-deep);
  }
  .stars-meta span { display: block; font-size: .85rem; color: var(--text-light); }
  .reviews-grid {
    display: grid; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 1.5rem; max-width: 1200px;
  }
  .review-card {
    background: var(--warm-white);
    padding: 2rem; border-radius: 2px;
    border: 1px solid rgba(0,0,0,.06);
    position: relative;
    transition: box-shadow .3s, transform .3s;
  }
  .review-card:hover {
    box-shadow: 0 15px 45px rgba(26,58,31,.1);
    transform: translateY(-4px);
  }
  .review-quote {
    font-size: 3rem; line-height: 1;
    color: rgba(201,168,76,.25);
    font-family: 'Playfair Display', serif;
    margin-bottom: -.8rem;
  }
  .review-stars { color: var(--gold); font-size: .95rem; letter-spacing: .05em; margin-bottom: 1rem; }
  .review-text {
    font-size: .95rem; line-height: 1.75; color: var(--text-mid);
    font-weight: 300;
  }
  .review-author {
    display: flex; align-items: center; gap: .8rem;
    margin-top: 1.5rem; padding-top: 1.2rem;
    border-top: 1px solid rgba(0,0,0,.06);
  }
  .review-avatar {
    width: 40px; height: 40px; border-radius: 50%;
    background: var(--green-fresh);
    display: flex; align-items: center; justify-content: center;
    font-weight: 700; color: white; font-size: .9rem;
  }
  .review-name strong { display: block; font-size: .9rem; font-weight: 600; color: var(--green-deep); }
  .review-name span { font-size: .78rem; color: var(--text-light); }

  /* ── GALLERY ── */
  .gallery { background: var(--warm-white); padding-bottom: 2rem; }
  .gallery-header { max-width: 600px; margin-bottom: 3rem; }
  .gallery-grid {
    display: grid;
    grid-template-columns: repeat(12, 1fr);
    grid-template-rows: repeat(2, 280px);
    gap: 1rem; max-width: 1200px;
  }
  .gallery-item {
    overflow: hidden; border-radius: 2px;
    position: relative;
  }
  .gallery-item img {
    width: 100%; height: 100%; object-fit: cover;
    transition: transform .6s cubic-bezier(.4,0,.2,1);
  }
  .gallery-item:hover img { transform: scale(1.07); }
  .gallery-item:nth-child(1) { grid-column: span 5; }
  .gallery-item:nth-child(2) { grid-column: span 4; }
  .gallery-item:nth-child(3) { grid-column: span 3; }
  .gallery-item:nth-child(4) { grid-column: span 3; }
  .gallery-item:nth-child(5) { grid-column: span 5; }
  .gallery-item:nth-child(6) { grid-column: span 4; }

  /* ── CTA SECTION ── */
  .cta-section {
    background:
      linear-gradient(135deg, rgba(26,58,31,.94) 0%, rgba(45,90,53,.94) 100%),
      url('https://images.unsplash.com/photo-1416879595882-3373a0480b5b?w=1200&q=80') center/cover;
    text-align: center;
    padding: 8rem 5%;
  }
  .cta-section .section-label { color: var(--gold-light); }
  .cta-section .section-title { color: var(--cream); margin-bottom: 1rem; max-width: none; }
  .cta-section p {
    color: rgba(247,243,236,.75); font-size: 1.05rem;
    max-width: 520px; margin: 0 auto 2.5rem; line-height: 1.7; font-weight: 300;
  }
  .cta-form {
    display: flex; gap: 1rem; justify-content: center; flex-wrap: wrap;
    max-width: 560px; margin: 0 auto;
  }
  .cta-form input {
    flex: 1; min-width: 220px;
    padding: 1rem 1.4rem; border: none; border-radius: 2px;
    background: rgba(247,243,236,.12);
    color: var(--cream); font-family: 'DM Sans', sans-serif;
    font-size: .95rem;
    border: 1.5px solid rgba(247,243,236,.2);
    outline: none;
    transition: border-color .2s, background .2s;
  }
  .cta-form input::placeholder { color: rgba(247,243,236,.45); }
  .cta-form input:focus {
    border-color: var(--gold);
    background: rgba(247,243,236,.15);
  }
  .cta-form .btn-primary { white-space: nowrap; }
  .cta-phone {
    margin-top: 2rem; color: rgba(247,243,236,.6); font-size: .9rem;
  }
  .cta-phone a { color: var(--gold-light); text-decoration: none; font-weight: 600; }

  /* ── FOOTER ── */
  footer {
    background: #111510; color: rgba(247,243,236,.6);
    padding: 4rem 5% 2rem;
  }
  .footer-grid {
    display: grid; grid-template-columns: 2fr 1fr 1fr 1.5fr;
    gap: 4rem; padding-bottom: 3rem;
    border-bottom: 1px solid rgba(247,243,236,.08);
  }
  .footer-brand .nav-logo { font-size: 1.4rem; margin-bottom: 1rem; }
  .footer-brand p {
    font-size: .88rem; line-height: 1.7; max-width: 260px;
  }
  .footer-col h4 {
    color: var(--cream); font-size: .82rem; letter-spacing: .12em;
    text-transform: uppercase; font-weight: 600; margin-bottom: 1.2rem;
  }
  .footer-col ul { list-style: none; display: flex; flex-direction: column; gap: .7rem; }
  .footer-col a { color: rgba(247,243,236,.55); text-decoration: none; font-size: .88rem; transition: color .2s; }
  .footer-col a:hover { color: var(--gold-light); }
  .footer-contact p { font-size: .88rem; line-height: 1.9; }
  .footer-contact a { color: var(--gold-light); text-decoration: none; }
  .footer-bottom {
    display: flex; justify-content: space-between; align-items: center;
    padding-top: 2rem; font-size: .82rem;
    flex-wrap: wrap; gap: 1rem;
  }
  .footer-bottom a { color: rgba(247,243,236,.4); text-decoration: none; }

  /* ── ANIMATIONS ── */
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(28px); }
    to   { opacity: 1; transform: translateY(0); }
  }
  .reveal {
    opacity: 0; transform: translateY(30px);
    transition: opacity .8s ease, transform .8s ease;
  }
  .reveal.visible { opacity: 1; transform: translateY(0); }

  /* ── RESPONSIVE ── */
  @media (max-width: 900px) {
    .nav-links { display: none; }
    .about-grid { grid-template-columns: 1fr; gap: 3rem; }
    .about-img-wrap img { height: 360px; }
    .about-img-badge { right: 0; bottom: -1rem; }
    .process-steps { grid-template-columns: repeat(2, 1fr); }
    .process-steps::before { display: none; }
    .gallery-grid { grid-template-columns: 1fr 1fr; grid-template-rows: auto; }
    .gallery-item { grid-column: span 1 !important; height: 220px; }
    .footer-grid { grid-template-columns: 1fr 1fr; }
    .hero-stats { gap: 1.5rem; flex-wrap: wrap; }
  }
  @media (max-width: 600px) {
    section { padding: 5rem 5%; }
    .trust-bar { gap: 1.5rem; }
    .trust-divider { display: none; }
    .process-steps { grid-template-columns: 1fr; }
    .footer-grid { grid-template-columns: 1fr; gap: 2.5rem; }
    .footer-bottom { flex-direction: column; text-align: center; }
    .gallery-grid { grid-template-columns: 1fr; }
    .gallery-item { height: 200px; }
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <div class="nav-logo">🌿 Green<span>field</span></div>
  <ul class="nav-links">
    <li><a href="#about">About</a></li>
    <li><a href="#services">Services</a></li>
    <li><a href="#process">Our Process</a></li>
    <li><a href="#reviews">Reviews</a></li>
    <li><a href="#gallery">Gallery</a></li>
  </ul>
  <a href="#contact" class="nav-cta">Free Estimate</a>
</nav>

<!-- HERO -->
<section class="hero" id="home">
  <div class="hero-badge">⭐ Rated #1 in the Region • Since 1994</div>
  <h1>Your Property.<br>Our <em>Masterpiece.</em></h1>
  <p class="hero-sub">Trusted by hundreds of homeowners and businesses for over 30 years. We don't just maintain landscapes — we craft outdoor living spaces that last a lifetime.</p>
  <div class="hero-actions">
    <a href="#contact" class="btn-primary">Get a Free Estimate</a>
    <a href="#gallery" class="btn-outline">View Our Work</a>
  </div>
  <div class="hero-stats">
    <div class="stat-item">
      <span class="stat-num">30+</span>
      <span class="stat-label">Years in Business</span>
    </div>
    <div class="stat-item">
      <span class="stat-num">5.0</span>
      <span class="stat-label">Star Average</span>
    </div>
    <div class="stat-item">
      <span class="stat-num">800+</span>
      <span class="stat-label">Happy Clients</span>
    </div>
    <div class="stat-item">
      <span class="stat-num">100%</span>
      <span class="stat-label">Satisfaction Guaranteed</span>
    </div>
  </div>
</section>

<!-- TRUST BAR -->
<div class="trust-bar">
  <div class="trust-item"><span class="trust-icon">✅</span> Licensed & Insured</div>
  <div class="trust-divider"></div>
  <div class="trust-item"><span class="trust-icon">🏆</span> BBB A+ Rated</div>
  <div class="trust-divider"></div>
  <div class="trust-item"><span class="trust-icon">⭐</span> 5-Star Google Reviews</div>
  <div class="trust-divider"></div>
  <div class="trust-item"><span class="trust-icon">🌱</span> Eco-Friendly Practices</div>
  <div class="trust-divider"></div>
  <div class="trust-item"><span class="trust-icon">📞</span> Free Estimates Always</div>
</div>

<!-- ABOUT -->
<section class="about" id="about">
  <div class="about-grid">
    <div class="about-img-wrap reveal">
      <img src="https://images.unsplash.com/photo-1416879595882-3373a0480b5b?w=800&q=80" alt="Professional landscaping team at work">
      <div class="about-img-badge">
        <div class="num">30</div>
        <div class="label">Years of Excellence</div>
      </div>
    </div>
    <div class="about-content reveal">
      <p class="section-label">Our Story</p>
      <h2 class="section-title">A Legacy Built on<br><em>Beautiful Lawns</em></h2>
      <p>Since 1994, Greenfield Landscaping has been the trusted name for homeowners and businesses who demand the best. What started as a one-man operation with a single mower has grown into a full-service landscaping company with a team of 25+ certified professionals.</p>
      <p>We've built our reputation one yard at a time — showing up on time, doing the job right, and treating every property like it's our own.</p>
      <div class="about-features">
        <div class="about-feature">
          <div class="feature-dot"></div>
          <div class="feature-text">
            <strong>Family Owned & Operated</strong>
            <span>Three decades of personal service, not a franchise call center.</span>
          </div>
        </div>
        <div class="about-feature">
          <div class="feature-dot"></div>
          <div class="feature-text">
            <strong>Certified Horticulturists On Staff</strong>
            <span>We know plants deeply — not just how to cut them.</span>
          </div>
        </div>
        <div class="about-feature">
          <div class="feature-dot"></div>
          <div class="feature-text">
            <strong>Fully Licensed, Bonded & Insured</strong>
            <span>Your property is always protected when we're on it.</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- SERVICES -->
<section class="services" id="services">
  <div class="services-header reveal">
    <p class="section-label">What We Do</p>
    <h2 class="section-title">Complete Outdoor <em>Services</em></h2>
  </div>
  <div class="services-grid reveal">
    <div class="service-card">
      <span class="service-icon">🌿</span>
      <h3>Lawn Care & Maintenance</h3>
      <p>Weekly, bi-weekly, or custom mowing schedules. Edging, trimming, blowing — everything done to perfection, every single visit.</p>
      <a href="#contact" class="service-link">Get a quote →</a>
    </div>
    <div class="service-card">
      <span class="service-icon">🏡</span>
      <h3>Landscape Design</h3>
      <p>Transform your outdoor space with custom designs that balance beauty, function, and the natural character of your property.</p>
      <a href="#contact" class="service-link">Get a quote →</a>
    </div>
    <div class="service-card">
      <span class="service-icon">🌳</span>
      <h3>Tree & Shrub Care</h3>
      <p>Pruning, shaping, planting, and removal. Our certified arborists keep your trees healthy and your property safe.</p>
      <a href="#contact" class="service-link">Get a quote →</a>
    </div>
    <div class="service-card">
      <span class="service-icon">💧</span>
      <h3>Irrigation Systems</h3>
      <p>Smart sprinkler installation and maintenance. We design water-efficient systems that keep your lawn lush without waste.</p>
      <a href="#contact" class="service-link">Get a quote →</a>
    </div>
    <div class="service-card">
      <span class="service-icon">🪨</span>
      <h3>Hardscaping</h3>
      <p>Patios, walkways, retaining walls, fire pits, and more. We build outdoor structures that stand the test of time.</p>
      <a href="#contact" class="service-link">Get a quote →</a>
    </div>
    <div class="service-card">
      <span class="service-icon">❄️</span>
      <h3>Seasonal Services</h3>
      <p>Spring clean-ups, fall leaf removal, snow plowing, and holiday lighting. Year-round care for your property.</p>
      <a href="#contact" class="service-link">Get a quote →</a>
    </div>
  </div>
</section>

<!-- PROCESS -->
<section class="process" id="process">
  <div class="process-header reveal">
    <p class="section-label">How It Works</p>
    <h2 class="section-title">Simple Process.<br><em>Stunning Results.</em></h2>
  </div>
  <div class="process-steps reveal">
    <div class="process-step">
      <div class="step-num">1</div>
      <h4>Free Consultation</h4>
      <p>We visit your property, listen to your vision, and assess what's needed — no pressure, no obligation.</p>
    </div>
    <div class="process-step">
      <div class="step-num">2</div>
      <h4>Custom Proposal</h4>
      <p>You receive a detailed, transparent quote within 24 hours. No hidden fees. Ever.</p>
    </div>
    <div class="process-step">
      <div class="step-num">3</div>
      <h4>Skilled Execution</h4>
      <p>Our experienced crew shows up on time and gets to work with care, precision, and professionalism.</p>
    </div>
    <div class="process-step">
      <div class="step-num">4</div>
      <h4>Your Satisfaction</h4>
      <p>We do a walkthrough with you. If anything isn't perfect, we fix it. Guaranteed.</p>
    </div>
  </div>
</section>

<!-- REVIEWS -->
<section class="reviews" id="reviews">
  <div class="reviews-header reveal">
    <p class="section-label">What Clients Say</p>
    <h2 class="section-title">Real Words from <em>Real Neighbors</em></h2>
  </div>
  <div class="stars-summary reveal">
    <span class="stars-big">★★★★★</span>
    <div class="stars-meta">
      <strong>5.0</strong>
      <span>Average across 400+ verified reviews</span>
    </div>
  </div>
  <div class="reviews-grid reveal">
    <div class="review-card">
      <div class="review-quote">"</div>
      <div class="review-stars">★★★★★</div>
      <p class="review-text">Greenfield completely transformed our backyard. We went from a patchy mess to a beautiful outdoor living space. The attention to detail was incredible — they even came back two weeks later just to check on the new sod.</p>
      <div class="review-author">
        <div class="review-avatar">SM</div>
        <div class="review-name">
          <strong>Sarah M.</strong>
          <span>Homeowner • Naperville, IL</span>
        </div>
      </div>
    </div>
    <div class="review-card">
      <div class="review-quote">"</div>
      <div class="review-stars">★★★★★</div>
      <p class="review-text">We've used Greenfield for 8 years and will never switch. They're reliable, professional, and genuinely care about the work. Our lawn is the best on the street and our neighbors always ask who we use.</p>
      <div class="review-author">
        <div class="review-avatar">JK</div>
        <div class="review-name">
          <strong>James K.</strong>
          <span>Long-term Client • Oak Park, IL</span>
        </div>
      </div>
    </div>
    <div class="review-card">
      <div class="review-quote">"</div>
      <div class="review-stars">★★★★★</div>
      <p class="review-text">I manage three commercial properties and Greenfield handles all of them. Consistent, communicative, and the results are always outstanding. If something ever isn't right, they make it right — no questions asked.</p>
      <div class="review-author">
        <div class="review-avatar">RL</div>
        <div class="review-name">
          <strong>Rachel L.</strong>
          <span>Property Manager • Downers Grove, IL</span>
        </div>
      </div>
    </div>
    <div class="review-card">
      <div class="review-quote">"</div>
      <div class="review-stars">★★★★★</div>
      <p class="review-text">Got quotes from 4 companies. Greenfield wasn't the cheapest, but the owner came out personally, explained everything clearly, and you could just tell these people take real pride in their work. Best money I've spent on my home.</p>
      <div class="review-author">
        <div class="review-avatar">TD</div>
        <div class="review-name">
          <strong>Tom D.</strong>
          <span>Homeowner • Orland Park, IL</span>
        </div>
      </div>
    </div>
    <div class="review-card">
      <div class="review-quote">"</div>
      <div class="review-stars">★★★★★</div>
      <p class="review-text">The hardscape patio they installed is absolutely stunning. Friends and family can't stop complimenting it. The crew was clean, efficient, and respectful of our home. 10/10 would recommend to everyone.</p>
      <div class="review-author">
        <div class="review-avatar">AP</div>
        <div class="review-name">
          <strong>Amanda P.</strong>
          <span>Homeowner • Tinley Park, IL</span>
        </div>
      </div>
    </div>
    <div class="review-card">
      <div class="review-quote">"</div>
      <div class="review-stars">★★★★★</div>
      <p class="review-text">As a real estate agent, curb appeal is everything. Greenfield is the only company I recommend to my clients. They've helped sell houses faster and at higher prices. That's not an exaggeration — it's just what great landscaping does.</p>
      <div class="review-author">
        <div class="review-avatar">MG</div>
        <div class="review-name">
          <strong>Mike G.</strong>
          <span>Real Estate Agent • Homer Glen, IL</span>
        </div>
      </div>
    </div>
  </div>
</section>

<!-- GALLERY -->
<section class="gallery" id="gallery">
  <div class="gallery-header reveal">
    <p class="section-label">Our Work</p>
    <h2 class="section-title">Every Property a <em>Portfolio Piece</em></h2>
  </div>
  <div class="gallery-grid reveal">
    <div class="gallery-item">
      <img src="https://images.unsplash.com/photo-1585320806297-9794b3e4edd0?w=600&q=80" alt="Manicured lawn">
    </div>
    <div class="gallery-item">
      <img src="https://images.unsplash.com/photo-1558618666-fcd25c85cd64?w=600&q=80" alt="Beautiful garden design">
    </div>
    <div class="gallery-item">
      <img src="https://images.unsplash.com/photo-1591857177580-dc82b9ac4e1e?w=600&q=80" alt="Outdoor patio">
    </div>
    <div class="gallery-item">
      <img src="https://images.unsplash.com/photo-1416879595882-3373a0480b5b?w=600&q=80" alt="Flower garden">
    </div>
    <div class="gallery-item">
      <img src="https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?w=600&q=80" alt="Lush landscape">
    </div>
    <div class="gallery-item">
      <img src="https://images.unsplash.com/photo-1523348837708-15d4a09cfac2?w=600&q=80" alt="Stone pathway">
    </div>
  </div>
</section>

<!-- CTA -->
<section class="cta-section" id="contact">
  <p class="section-label">Ready to Transform Your Property?</p>
  <h2 class="section-title">Get Your Free Estimate Today</h2>
  <p>No pushy sales. No hidden fees. Just an honest conversation about what your property needs — and what it could become.</p>
  <div class="cta-form">
    <input type="text" placeholder="Your name">
    <input type="tel" placeholder="Phone number">
    <button class="btn-primary" onclick="alert('Thank you! We\'ll call you within 24 hours.')">Request Callback</button>
  </div>
  <p class="cta-phone">Prefer to call? <a href="tel:+17085550194">(708) 555-0194</a> — We answer 7 days a week.</p>
</section>

<!-- FOOTER -->
<footer>
  <div class="footer-grid">
    <div class="footer-brand">
      <div class="nav-logo">🌿 Green<span style="color:var(--gold)">field</span></div>
      <p>Serving Chicagoland's southwest suburbs since 1994. Family owned, community rooted, quality obsessed.</p>
    </div>
    <div class="footer-col">
      <h4>Services</h4>
      <ul>
        <li><a href="#">Lawn Maintenance</a></li>
        <li><a href="#">Landscape Design</a></li>
        <li><a href="#">Tree & Shrub Care</a></li>
        <li><a href="#">Irrigation</a></li>
        <li><a href="#">Hardscaping</a></li>
        <li><a href="#">Seasonal Services</a></li>
      </ul>
    </div>
    <div class="footer-col">
      <h4>Company</h4>
      <ul>
        <li><a href="#">About Us</a></li>
        <li><a href="#">Our Team</a></li>
        <li><a href="#">Reviews</a></li>
        <li><a href="#">Gallery</a></li>
        <li><a href="#">Service Areas</a></li>
        <li><a href="#">Careers</a></li>
      </ul>
    </div>
    <div class="footer-col footer-contact">
      <h4>Contact</h4>
      <p>
        📞 <a href="tel:+17085550194">(708) 555-0194</a><br>
        ✉️ <a href="mailto:hello@greenfieldlandscaping.com">hello@greenfieldlandscaping.com</a><br><br>
        📍 Orland Park, IL<br>
        Serving all of Southwest Chicagoland<br><br>
        🕐 Mon–Sat: 7am – 6pm<br>
        Sun: Emergency calls only
      </p>
    </div>
  </div>
  <div class="footer-bottom">
    <span>© 2024 Greenfield Landscaping. All rights reserved.</span>
    <span><a href="#">Privacy Policy</a> · <a href="#">Terms</a></span>
  </div>
</footer>

<script>
  // Scroll reveal
  const reveals = document.querySelectorAll('.reveal');
  const observer = new IntersectionObserver((entries) => {
    entries.forEach((entry, i) => {
      if (entry.isIntersecting) {
        setTimeout(() => {
          entry.target.classList.add('visible');
        }, i * 80);
        observer.unobserve(entry.target);
      }
    });
  }, { threshold: 0.1 });
  reveals.forEach(el => observer.observe(el));

  // Smooth scroll for all anchor links
  document.querySelectorAll('a[href^="#"]').forEach(link => {
    link.addEventListener('click', e => {
      const target = document.querySelector(link.getAttribute('href'));
      if (target) {
        e.preventDefault();
        target.scrollIntoView({ behavior: 'smooth', block: 'start' });
      }
    });
  });
</script>
</body>
</html>
