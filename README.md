# navjyoti-website
Luxury car accessories website for Navjyoti Car Accessories Incorporated in Surrey, BC.
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Navjyoti Car Accessories | Surrey BC</title>

  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&family=Manrope:wght@500;600;700;800&display=swap" rel="stylesheet">

  <style>
    :root {
      --bg: #080909;
      --bg-soft: #101111;
      --card: #141515;
      --card-hover: #1a1b1b;
      --gold: #d8b36a;
      --gold-light: #f0d18c;
      --white: #f7f5ef;
      --muted: #a6a6a1;
      --line: rgba(255,255,255,.09);
      --green: #78c091;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      font-family: "Inter", sans-serif;
      background: var(--bg);
      color: var(--white);
      line-height: 1.6;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    .container {
      width: min(1160px, calc(100% - 40px));
      margin: auto;
    }

    /* NAV */

    nav {
      position: fixed;
      top: 0;
      width: 100%;
      z-index: 100;
      background: rgba(8,9,9,.82);
      backdrop-filter: blur(18px);
      border-bottom: 1px solid var(--line);
    }

    .nav-inner {
      height: 76px;
      display: flex;
      align-items: center;
      justify-content: space-between;
    }

    .logo {
      font-family: "Manrope", sans-serif;
      font-weight: 800;
      letter-spacing: -.5px;
      font-size: 19px;
    }

    .logo span {
      color: var(--gold);
    }

    .nav-links {
      display: flex;
      gap: 32px;
      align-items: center;
      font-size: 14px;
      color: #d0d0cc;
    }

    .nav-links a:hover {
      color: var(--gold-light);
    }

    .nav-button {
      padding: 11px 19px;
      background: var(--gold);
      color: #111;
      border-radius: 999px;
      font-weight: 700;
    }

    /* HERO */

    .hero {
      min-height: 760px;
      display: flex;
      align-items: center;
      position: relative;
      overflow: hidden;
      background:
        radial-gradient(circle at 75% 45%, rgba(216,179,106,.13), transparent 30%),
        radial-gradient(circle at 20% 30%, rgba(255,255,255,.035), transparent 25%),
        var(--bg);
    }

    .hero::after {
      content: "";
      position: absolute;
      inset: 0;
      pointer-events: none;
      background: linear-gradient(
        90deg,
        rgba(8,9,9,.95),
        rgba(8,9,9,.55),
        rgba(8,9,9,.1)
      );
    }

    .hero-content {
      position: relative;
      z-index: 2;
      max-width: 700px;
      padding-top: 60px;
    }

    .eyebrow {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      color: var(--gold-light);
      font-size: 12px;
      letter-spacing: 2px;
      text-transform: uppercase;
      font-weight: 700;
      margin-bottom: 22px;
    }

    .eyebrow::before {
      content: "";
      width: 30px;
      height: 1px;
      background: var(--gold);
    }

    h1 {
      font-family: "Manrope", sans-serif;
      font-size: clamp(48px, 7vw, 88px);
      line-height: .98;
      letter-spacing: -4px;
      margin-bottom: 25px;
    }

    h1 span {
      color: var(--gold);
    }

    .hero-text {
      color: #bdbdb8;
      max-width: 590px;
      font-size: 17px;
      margin-bottom: 35px;
    }

    .buttons {
      display: flex;
      gap: 13px;
      flex-wrap: wrap;
    }

    .button {
      padding: 14px 23px;
      border-radius: 999px;
      font-weight: 700;
      font-size: 14px;
      transition: .2s ease;
    }

    .button-primary {
      background: var(--gold);
      color: #111;
    }

    .button-primary:hover {
      background: var(--gold-light);
      transform: translateY(-2px);
    }

    .button-secondary {
      border: 1px solid var(--line);
      background: rgba(255,255,255,.035);
    }

    .button-secondary:hover {
      background: rgba(255,255,255,.08);
    }

    .rating-strip {
      display: flex;
      gap: 35px;
      margin-top: 55px;
    }

    .rating-number {
      font-family: "Manrope", sans-serif;
      font-size: 28px;
      font-weight: 800;
    }

    .stars {
      color: var(--gold);
      letter-spacing: 2px;
      font-size: 14px;
    }

    .rating-label {
      color: var(--muted);
      font-size: 12px;
      margin-top: 3px;
    }

    /* SECTIONS */

    section {
      padding: 110px 0;
    }

    .section-heading {
      display: flex;
      justify-content: space-between;
      align-items: end;
      margin-bottom: 45px;
      gap: 30px;
    }

    .section-heading h2 {
      font-family: "Manrope", sans-serif;
      font-size: clamp(32px, 4vw, 50px);
      line-height: 1.05;
      letter-spacing: -2px;
    }

    .section-heading p {
      color: var(--muted);
      max-width: 430px;
      font-size: 14px;
    }

    /* SERVICES */

    #services {
      background: #0d0e0e;
    }

    .service-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 15px;
    }

    .service {
      background: var(--card);
      border: 1px solid var(--line);
      padding: 28px;
      min-height: 205px;
      border-radius: 18px;
      transition: .25s ease;
    }

    .service:hover {
      background: var(--card-hover);
      transform: translateY(-4px);
      border-color: rgba(216,179,106,.35);
    }

    .service-number {
      color: var(--gold);
      font-size: 12px;
      font-weight: 700;
      letter-spacing: 2px;
    }

    .service h3 {
      font-family: "Manrope", sans-serif;
      margin: 32px 0 9px;
      font-size: 20px;
    }

    .service p {
      color: var(--muted);
      font-size: 13px;
    }

    .service-price {
      margin-top: 18px;
      color: var(--gold-light);
      font-weight: 700;
      font-size: 14px;
    }

    /* REVIEWS */

    .review-summary {
      display: grid;
      grid-template-columns: 280px 1fr;
      gap: 55px;
      align-items: center;
      margin-bottom: 45px;
      padding: 35px;
      border: 1px solid var(--line);
      background: linear-gradient(135deg, #151616, #101111);
      border-radius: 22px;
    }

    .big-rating {
      text-align: center;
      border-right: 1px solid var(--line);
      padding-right: 45px;
    }

    .big-rating strong {
      display: block;
      font-family: "Manrope", sans-serif;
      font-size: 70px;
      line-height: 1;
    }

    .big-rating .stars {
      margin: 8px 0;
    }

    .big-rating small {
      color: var(--muted);
    }

    .review-bars {
      display: grid;
      gap: 10px;
    }

    .bar-row {
      display: grid;
      grid-template-columns: 35px 1fr 35px;
      align-items: center;
      gap: 10px;
      font-size: 12px;
      color: var(--muted);
    }

    .bar {
      height: 7px;
      background: #272827;
      border-radius: 10px;
      overflow: hidden;
    }

    .bar-fill {
      height: 100%;
      background: var(--gold);
      border-radius: inherit;
    }

    .review-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 15px;
    }

    .review {
      background: var(--card);
      border: 1px solid var(--line);
      border-radius: 18px;
      padding: 27px;
      min-height: 250px;
      display: flex;
      flex-direction: column;
    }

    .review-stars {
      color: var(--gold);
      font-size: 14px;
      letter-spacing: 2px;
    }

    .review p {
      margin: 23px 0;
      color: #d4d4d0;
      font-size: 14px;
      flex: 1;
    }

    .review-author {
      display: flex;
      justify-content: space-between;
      border-top: 1px solid var(--line);
      padding-top: 17px;
      font-size: 12px;
    }

    .review-author strong {
      color: #eee;
    }

    .review-author span {
      color: var(--muted);
    }

    /* CTA */

    .cta {
      padding: 90px 0;
      background:
        radial-gradient(circle at 50% 0%, rgba(216,179,106,.15), transparent 40%),
        #0d0e0e;
      text-align: center;
      border-top: 1px solid var(--line);
      border-bottom: 1px solid var(--line);
    }

    .cta h2 {
      font-family: "Manrope", sans-serif;
      font-size: clamp(34px, 5vw, 58px);
      letter-spacing: -2px;
      margin-bottom: 15px;
    }

    .cta p {
      color: var(--muted);
      margin-bottom: 30px;
    }

    /* CONTACT */

    .contact-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 18px;
    }

    .contact-card {
      border: 1px solid var(--line);
      border-radius: 20px;
      padding: 35px;
      background: var(--card);
    }

    .contact-card h3 {
      font-family: "Manrope", sans-serif;
      margin-bottom: 20px;
    }

    .contact-item {
      padding: 14px 0;
      border-bottom: 1px solid var(--line);
      color: #ccc;
      font-size: 14px;
    }

    .contact-item:last-child {
      border: none;
    }

    .contact-item span {
      display: block;
      color: var(--muted);
      font-size: 11px;
      text-transform: uppercase;
      letter-spacing: 1px;
      margin-bottom: 3px;
    }

    /* FOOTER */

    footer {
      padding: 30px 0;
      border-top: 1px solid var(--line);
      color: var(--muted);
      font-size: 12px;
    }

    .footer-inner {
      display: flex;
      justify-content: space-between;
      gap: 20px;
    }

    /* MOBILE */

    @media (max-width: 800px) {
      .nav-links {
        display: none;
      }

      .hero {
        min-height: 700px;
      }

      .hero::after {
        background: rgba(8,9,9,.65);
      }

      .service-grid,
      .review-grid {
        grid-template-columns: 1fr;
      }

      .review-summary {
        grid-template-columns: 1fr;
        gap: 30px;
      }

      .big-rating {
        border-right: none;
        border-bottom: 1px solid var(--line);
        padding-right: 0;
        padding-bottom: 30px;
      }

      .contact-grid {
        grid-template-columns: 1fr;
      }

      .section-heading {
        display: block;
      }

      .section-heading p {
        margin-top: 15px;
      }

      .footer-inner {
        flex-direction: column;
      }
    }
  </style>
</head>

<body>

  <!-- NAVIGATION -->
  <nav>
    <div class="container nav-inner">
      <a href="#" class="logo">NAVJYOTI<span>.</span></a>

      <div class="nav-links">
        <a href="#services">Services</a>
        <a href="#reviews">Reviews</a>
        <a href="#about">About</a>
        <a href="#contact">Contact</a>
        <a href="tel:2368894447" class="nav-button">Call Now</a>
      </div>
    </div>
  </nav>

  <!-- HERO -->
  <header class="hero">
    <div class="container">
      <div class="hero-content">

        <div class="eyebrow">
          Surrey's Car Accessories Specialists
        </div>

        <h1>
          Upgrade your<br>
          <span>drive.</span>
        </h1>

        <p class="hero-text">
          Professional car accessories, dash cam installations,
          cameras, screens, tinting and more — installed with
          precision in Surrey, BC.
        </p>

        <div class="buttons">
          <a href="#services" class="button button-primary">
            Explore Services
          </a>

          <a href="tel:2368894447" class="button button-secondary">
            (236) 889-4447
          </a>
        </div>

        <div class="rating-strip">
          <div>
            <div class="rating-number">4.7</div>
            <div class="stars">★★★★★</div>
            <div class="rating-label">Google Rating</div>
          </div>

          <div>
            <div class="rating-number">54+</div>
            <div class="rating-label">Customer Reviews</div>
          </div>

          <div>
            <div class="rating-number">BC</div>
            <div class="rating-label">Surrey, Canada</div>
          </div>
        </div>

      </div>
    </div>
  </header>

  <!-- SERVICES -->
  <section id="services">
    <div class="container">

      <div class="section-heading">
        <h2>The Menu</h2>
        <p>
          Premium upgrades for your vehicle, professionally
          installed and tailored to your needs.
        </p>
      </div>

      <div class="service-grid">

        <div class="service">
          <div class="service-number">01 / DASH CAM</div>
          <h3>Dash Cam Installation</h3>
          <p>
            Clean, professional installation with discreet wiring
            and a factory-style finish.
          </p>
          <div class="service-price">Professional Installation</div>
        </div>

        <div class="service">
          <div class="service-number">02 / CAMERA</div>
          <h3>Backup Cameras</h3>
          <p>
            Improve visibility and parking confidence with
            professionally installed backup camera systems.
          </p>
          <div class="service-price">Installation Available</div>
        </div>

        <div class="service">
          <div class="service-number">03 / SCREEN</div>
          <h3>Android Screens</h3>
          <p>
            Modernize your dashboard with upgraded screens,
            entertainment and smart vehicle features.
          </p>
          <div class="service-price">Upgrade Your Interior</div>
        </div>

        <div class="service">
          <div class="service-number">04 / TINT</div>
          <h3>Window Tinting</h3>
          <p>
            Give your vehicle a cleaner look while improving
            privacy and driving comfort.
          </p>
          <div class="service-price">Multiple Options</div>
        </div>

        <div class="service">
          <div class="service-number">05 / INSTALL</div>
          <h3>Accessory Installation</h3>
          <p>
            Expert installation of vehicle accessories with
            attention to fit, wiring and finish.
          </p>
          <div class="service-price">Custom Installation</div>
        </div>

        <div class="service">
          <div class="service-number">06 / CUSTOM</div>
          <h3>Custom Upgrades</h3>
          <p>
            Have something specific in mind? Talk to the team
            about your vehicle and the upgrade you want.
          </p>
          <div class="service-price">Ask About Your Vehicle</div>
        </div>

      </div>
    </div>
  </section>

  <!-- REVIEWS -->
  <section id="reviews">
    <div class="container">

      <div class="section-heading">
        <h2>Loved by<br>local drivers.</h2>
        <p>
          Real customer feedback highlighting the service,
          installation quality and attention to detail.
        </p>
      </div>

      <div class="review-summary">

        <div class="big-rating">
          <strong>4.7</strong>
          <div class="stars">★★★★★</div>
          <small>54 Google reviews</small>
        </div>

        <div class="review-bars">
          <div class="bar-row">
            <span>5★</span>
            <div class="bar"><div class="bar-fill" style="width:88%"></div></div>
            <span>88%</span>
          </div>

          <div class="bar-row">
            <span>4★</span>
            <div class="bar"><div class="bar-fill" style="width:8%"></div></div>
            <span>8%</span>
          </div>

          <div class="bar-row">
            <span>3★</span>
            <div class="bar"><div class="bar-fill" style="width:2%"></div></div>
            <span>2%</span>
          </div>

          <div class="bar-row">
            <span>2★</span>
            <div class="bar"><div class="bar-fill" style="width:1%"></div></div>
            <span>1%</span>
          </div>

          <div class="bar-row">
            <span>1★</span>
            <div class="bar"><div class="bar-fill" style="width:1%"></div></div>
            <span>1%</span>
          </div>
        </div>

      </div>

      <div class="review-grid">

        <article class="review">
          <div class="review-stars">★★★★★</div>
          <p>
            "Great service, genuine installation and amazing
            experience."
          </p>
          <div class="review-author">
            <strong>Customer Review</strong>
            <span>5 stars</span>
          </div>
        </article>

        <article class="review">
          <div class="review-stars">★★★★★</div>
          <p>
            "Amazing customer service, reasonable price and
            quality work done."
          </p>
          <div class="review-author">
            <strong>Customer Review</strong>
            <span>5 stars</span>
          </div>
        </article>

        <article class="review">
          <div class="review-stars">★★★★★</div>
          <p>
            "The quality of work and attention to detail were
            top-notch."
          </p>
          <div class="review-author">
            <strong>Customer Review</strong>
            <span>5 stars</span>
          </div>
        </article>

        <article class="review">
          <div class="review-stars">★★★★★</div>
          <p>
            "Professional dash cam installation in Surrey.
            Highly recommend Nav."
          </p>
          <div class="review-author">
            <strong>604 Gutters</strong>
            <span>5 stars</span>
          </div>
        </article>

        <article class="review">
          <div class="review-stars">★★★★★</div>
          <p>
            "Neeraj is one of the best car accessories
            technicians I have met in Canada."
          </p>
          <div class="review-author">
            <strong>Imran Khan</strong>
            <span>5 stars</span>
          </div>
        </article>

        <article class="review">
          <div class="review-stars">★★★★★</div>
          <p>
            "The installation was professionally handled and
            the team was helpful throughout."
          </p>
          <div class="review-author">
            <strong>Local Customer</strong>
            <span>5 stars</span>
          </div>
        </article>

      </div>
    </div>
  </section>

  <!-- CTA -->
  <section class="cta">
    <div class="container">
      <h2>Your car deserves better.</h2>
      <p>
        Book your installation or call us to discuss your vehicle.
      </p>

      <div class="buttons" style="justify-content:center;">
        <a href="tel:2368894447" class="button button-primary">
          Call (236) 889-4447
        </a>

        <a
          href="https://www.google.com/maps/search/?api=1&query=Navjyoti+Car+Accessories+Incorporated+7743+128+St+Surrey+BC"
          target="_blank"
          class="button button-secondary"
        >
          Get Directions
        </a>
      </div>
    </div>
  </section>

  <!-- ABOUT / CONTACT -->
  <section id="about">
    <div class="container">

      <div class="section-heading">
        <h2>Built around<br>your vehicle.</h2>
        <p>
          A local Surrey car accessories shop focused on clean
          installations, quality work and customer service.
        </p>
      </div>

      <div class="contact-grid">

        <div class="contact-card">
          <h3>Visit Navjyoti</h3>

          <div class="contact-item">
            <span>Address</span>
            7743 128 St Unit 16<br>
            Surrey, BC V3W 1L4
          </div>

          <div class="contact-item">
            <span>Phone</span>
            <a href="tel:2368894447">(236) 889-4447</a>
          </div>

          <div class="contact-item">
            <span>Hours</span>
            Open · Closes 8 p.m.
          </div>
        </div>

        <div class="contact-card">
          <h3>Why customers choose us</h3>

          <div class="contact-item">
            <span>01</span>
            Professional installations
          </div>

          <div class="contact-item">
            <span>02</span>
            Attention to detail
          </div>

          <div class="contact-item">
            <span>03</span>
            Reasonable pricing
          </div>

          <div class="contact-item">
            <span>04</span>
            Local Surrey service
          </div>
        </div>

      </div>
    </div>
  </section>

  <!-- FOOTER -->
  <footer id="contact">
    <div class="container footer-inner">
      <div>
        © 2026 Navjyoti Car Accessories Incorporated
      </div>

      <div>
        Surrey, British Columbia · (236) 889-4447
      </div>
    </div>
  </footer>

</body>
</html>
