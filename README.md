[etaleme website v4.html](https://github.com/user-attachments/files/33781040/etaleme.website.v4.html)
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Etaleme Solutions — Reusable Body Care, Made with Dignity</title>
<meta name="description" content="Affordable, skin-friendly, reusable body care alternatives for mothers, fistula patients, nursing mothers, and women across Addis Ababa and Sheger City.">
<script>document.documentElement.classList.add('js');</script>
<meta property="og:type" content="website">
<meta property="og:title" content="Etaleme Solutions — Reusable Body Care, Made with Dignity">
<meta property="og:description" content="Affordable, skin-friendly, reusable body care alternatives for mothers, fistula patients, nursing mothers, and women across Addis Ababa and Sheger City.">
<!-- For a share picture, add: <meta property="og:image" content="https://YOUR-FULL-SITE-URL/hero.jpg"> (must be a full URL) -->
<link rel="icon" type="image/svg+xml" href="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 200 200'%3E%3Ccircle cx='100' cy='100' r='95' fill='%236b7a3a'/%3E%3Cpath d='M100 46 C112 64 120 78 120 90 C120 102 111 110 100 110 C89 110 80 102 80 90 C80 78 88 64 100 46 Z' fill='%23e8a13c'/%3E%3Cpath d='M42 112 C55 157 145 157 158 112 C140 132 60 132 42 112 Z' fill='%231a5c4a'/%3E%3C/svg%3E">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600&family=Lora:ital,wght@0,500;0,600;1,400&family=Noto+Sans+Ethiopic:wght@400;500;600&display=swap" rel="stylesheet">
<style>
  :root {
    --primary: #0F5D4E;
    --accent:  #E8A23A;
    --olive:   #5B6F3A;
    --bg:      #F4EDE2;
    --text:    #2b2b2b;
    --light:   #ffffff;
    --border:  #e0dcd3;
  }
  * { margin: 0; padding: 0; box-sizing: border-box; }
  html { scroll-behavior: smooth; }
  body {
    font-family: 'Inter', 'Noto Sans Ethiopic', sans-serif;
    color: var(--text); background: var(--bg); line-height: 1.6;
  }
  h1, h2, h3 {
    font-family: 'Lora', 'Noto Sans Ethiopic', serif;
    font-weight: 600;
  }
  .container { max-width: 1100px; margin: 0 auto; padding: 0 20px; }

  section { scroll-margin-top: 90px; padding: 80px 0; }

  /* --- ANIMATIONS & EFFECTS --- */
  .js .reveal {
    opacity: 0;
    transform: translateY(40px);
    transition: opacity 0.8s ease-out, transform 0.8s ease-out;
  }
  .js .reveal.active {
    opacity: 1;
    transform: translateY(0);
  }
  @media (prefers-reduced-motion: reduce) {
    .js .reveal { opacity: 1; transform: none; transition: none; }
  }

  .logo-drop {
    transition: transform 0.3s ease;
    transform-origin: center bottom;
  }
  .brand:hover .logo-drop {
    animation: pulseDrop 1s ease-in-out infinite alternate;
  }
  @keyframes pulseDrop {
    0% { transform: translateY(0); }
    100% { transform: translateY(-6px); }
  }

  /* --- NAVIGATION --- */
  nav {
    background: rgba(255, 255, 255, 0.95);
    backdrop-filter: blur(10px);
    padding: 12px 0;
    box-shadow: 0 2px 10px rgba(0,0,0,.05);
    position: sticky; top: 0; z-index: 100;
  }
  nav .container { display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 10px; }

  .brand { display: flex; align-items: center; gap: 12px; text-decoration: none; }
  .brand svg { width: 42px; height: 42px; }
  .brand-text { font-family: 'Lora', serif; font-weight: 600; color: var(--primary); font-size: 1.3rem; letter-spacing: -0.5px; }

  .nav-right { display: flex; align-items: center; gap: 24px; flex-wrap: wrap; }
  nav ul { list-style: none; display: flex; gap: 24px; flex-wrap: wrap; }
  nav a.nav-link { text-decoration: none; color: var(--text); font-weight: 500; font-size: 0.95rem; transition: color 0.2s; }
  nav a.nav-link:hover { color: var(--primary); }

  .lang-group { display: flex; gap: 4px; background: #eee; padding: 4px; border-radius: 20px; }
  .lang-btn {
    background: transparent; color: var(--text); border: none;
    padding: 6px 12px; border-radius: 16px; cursor: pointer; font-weight: 600;
    font-size: .8rem; transition: all 0.2s;
  }
  .lang-btn[aria-pressed="true"] { background: var(--primary); color: var(--light); box-shadow: 0 2px 4px rgba(0,0,0,0.1); }

  /* --- INTRO VIDEO --- */
  .video-hero { position: relative; height: 60vh; max-height: 520px; min-height: 280px; background: var(--primary); overflow: hidden; }
  .video-hero video { position: absolute; inset: 0; width: 100%; height: 100%; object-fit: cover; }
  .video-hero::after { content: ""; position: absolute; inset: 0; background: linear-gradient(180deg, rgba(0,0,0,.15) 0%, rgba(15,93,78,.65) 100%); }
  .video-text { position: absolute; z-index: 1; left: 0; right: 0; bottom: 8%; text-align: center; padding: 0 20px; color: #fff;
    font-family: 'Lora', 'Noto Sans Ethiopic', serif; font-weight: 600; font-size: clamp(1.4rem, 4.5vw, 2.6rem); line-height: 1.25; text-shadow: 0 2px 12px rgba(0,0,0,.4); }

  /* --- HERO SECTION --- */
  header {
    padding: 80px 0 100px;
    position: relative;
    overflow: hidden;
    background: linear-gradient(180deg, #EBE5D9 0%, var(--bg) 100%);
  }
  header .container { position: relative; z-index: 1; display: flex; align-items: center; justify-content: space-between; gap: 50px; }
  .hero-text { flex: 1.2; text-align: left; }
  .hero-image { flex: 0.8; display: flex; justify-content: center; position: relative; }

  header h1 { font-size: clamp(2rem, 4vw, 3.2rem); color: var(--primary); margin-bottom: 20px; line-height: 1.2; }
  header p { font-size: 1.15rem; color: #444; margin-bottom: 30px; max-width: 600px; }

  .hero-image img {
    width: 100%;
    max-width: 480px;
    aspect-ratio: 1 / 1;
    object-fit: cover;
    display: block;
    border-radius: 50%;
    box-shadow: 0 20px 40px rgba(15, 93, 78, 0.15);
    border: 4px solid rgba(255,255,255,0.5);
  }

  .cta {
    display: inline-block; padding: 14px 32px;
    background: var(--accent); color: #111;
    border-radius: 30px; text-decoration: none; font-weight: 600; font-size: 1.05rem;
    transition: transform 0.2s, box-shadow 0.2s;
    box-shadow: 0 4px 15px rgba(232, 162, 58, 0.3);
  }
  .cta:hover { transform: translateY(-2px); box-shadow: 0 6px 20px rgba(232, 162, 58, 0.4); }

  .status-line {
    display: inline-block; margin-top: 20px; padding: 8px 16px;
    background: rgba(91, 111, 58, 0.1); color: var(--olive);
    border-radius: 20px; font-size: .85rem; font-weight: 600;
    border: 1px solid rgba(91, 111, 58, 0.2);
  }

  /* --- CONTENT SECTIONS --- */
  .mission { padding: 80px 0; text-align: center; }
  .mission h2 { color: var(--primary); margin-bottom: 20px; font-size: 2.2rem; }
  .mission p { max-width: 800px; margin: 0 auto; font-size: 1.15rem; color: #444; line-height: 1.7; }

  .why { padding: 80px 0; background: var(--light); text-align: center; }
  .why h2 { color: var(--primary); margin-bottom: 20px; font-size: 2.2rem; }
  .why p { max-width: 800px; margin: 0 auto; font-size: 1.15rem; color: #444; line-height: 1.7; }

  /* --- PRODUCTS --- */
  .products { padding: 80px 0; }
  .products h2 { color: var(--primary); text-align: center; margin-bottom: 50px; font-size: 2.2rem; }
  .grid { display: grid; gap: 30px; grid-template-columns: repeat(auto-fit, minmax(300px, 1fr)); }
  .card {
    background: var(--light); border-radius: 16px; padding: 32px;
    box-shadow: 0 10px 30px rgba(0,0,0,.04);
    border: 1px solid var(--border);
    border-top: 5px solid var(--accent);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
  }
  .card:hover { transform: translateY(-8px); box-shadow: 0 15px 35px rgba(0,0,0,.08); }
  .card.olive { border-top-color: var(--olive); }
  .card h3 { color: var(--primary); margin-bottom: 12px; font-size: 1.3rem; }
  .card p { font-size: .95rem; color: #555; }

  /* --- PARTNERS --- */
  .partners { padding: 80px 0; text-align: center; background: var(--bg); }
  .partners h2 { color: var(--primary); margin-bottom: 16px; font-size: 2.2rem; }
  .partners p { max-width: 700px; margin: 0 auto 30px; color: #555; font-size: 1.1rem; }
  .partner-tags { display: flex; flex-wrap: wrap; gap: 12px; justify-content: center; }
  .tag {
    background: var(--light); border: 1px solid var(--border);
    padding: 10px 24px; border-radius: 30px; font-size: .9rem; color: var(--primary);
    font-weight: 500; box-shadow: 0 2px 5px rgba(0,0,0,0.02);
  }

  /* --- FAQ --- */
  .faq { padding: 80px 0; background: var(--light); }
  .faq h2 { color: var(--primary); text-align: center; margin-bottom: 40px; font-size: 2.2rem; }
  .faq-item { max-width: 800px; margin: 0 auto 24px; padding-bottom: 20px; border-bottom: 1px solid var(--border); }
  .faq-item:last-child { border-bottom: none; }
  .faq-item h3 { color: var(--primary); font-size: 1.15rem; margin-bottom: 8px; }
  .faq-item p { color: #555; font-size: 1rem; }

  /* --- CONTACT --- */
  .contact { padding: 80px 0 100px; background: var(--bg); }
  .contact h2 { color: var(--primary); text-align: center; margin-bottom: 30px; font-size: 2.2rem; }

  .contact-ctas { display: flex; gap: 16px; justify-content: center; flex-wrap: wrap; margin-bottom: 40px; }
  .contact-ctas a {
    padding: 12px 28px; border-radius: 30px; text-decoration: none; font-weight: 600; font-size: .95rem;
    transition: opacity 0.2s, transform 0.2s;
  }
  .contact-ctas a:hover { opacity: 0.9; transform: translateY(-2px); }
  .contact-ctas .inst { background: var(--olive); color: var(--light); }
  .contact-ctas .indiv { background: var(--accent); color: #111; }

  .chat-ctas { display: flex; gap: 16px; justify-content: center; flex-wrap: wrap; margin-bottom: 40px; }
  .chat-btn { padding: 12px 24px; border-radius: 30px; text-decoration: none; font-weight: 600; font-size: .95rem; color: var(--light); transition: transform 0.2s; }
  .chat-btn:hover { transform: translateY(-2px); }
  .chat-btn.telegram { background: #1d8fcf; }
  .chat-btn.whatsapp { background: #1a9d4f; }
  .chat-btn.call { background: var(--primary); }

  .form-status { text-align: center; margin-top: 14px; font-weight: 600; color: var(--primary); display: none; }
  .form-status.visible { display: block; }
  .form-status.error { color: #b3261e; }

  form { max-width: 560px; margin: 0 auto; display: grid; gap: 16px; background: var(--light); padding: 40px; border-radius: 16px; box-shadow: 0 10px 30px rgba(0,0,0,0.05); }
  label { font-size: .9rem; color: var(--text); font-weight: 600; margin-bottom: -8px; }
  input, textarea {
    padding: 14px; border: 1px solid var(--border); border-radius: 8px;
    font-size: 1rem; font-family: inherit; width: 100%; background: var(--bg);
    transition: border-color 0.2s;
  }
  input:focus, textarea:focus { outline: none; border-color: var(--primary); }
  textarea { min-height: 120px; resize: vertical; }
  form button {
    padding: 16px; background: var(--primary); color: var(--light);
    border: none; border-radius: 8px; font-size: 1rem; font-weight: 600; cursor: pointer;
    transition: background 0.2s, transform 0.2s; margin-top: 10px;
  }
  form button:hover { background: #0a4036; transform: translateY(-2px); }
  .privacy-note { font-size: .8rem; color: #888; text-align: center; margin-top: 10px; }
  .email-alt { text-align: center; margin-top: 30px; color: #555; }
  .phone-line { text-align: center; margin-top: 10px; color: #555; }
  .email-alt a, .phone-line a { color: var(--primary); font-weight: 600; text-decoration: underline; }

  /* --- FOOTER --- */
  footer { background: var(--primary); color: var(--light); text-align: center; padding: 40px 0 20px; font-size: .9rem; }

  /* --- RESPONSIVE DESIGN --- */
  @media (max-width: 850px) {
    header .container { flex-direction: column; text-align: center; gap: 40px; }
    .hero-text { text-align: center; }
    header p { margin: 0 auto 30px; }
    .hero-text, .hero-image { flex: none; }
    .hero-image { width: 80%; margin: 0 auto; }
    header { padding: 50px 0 60px; }
    .video-hero { height: 50vh; }
    section { padding: 60px 0; }
  }
  @media (max-width: 600px) {
    nav .container { justify-content: center; }
    .nav-right { justify-content: center; width: 100%; margin-top: 10px; }
    nav ul { width: 100%; justify-content: center; gap: 6px 16px; }
    nav a.nav-link { font-size: .85rem; }
    form { padding: 24px; }
  }
</style>
</head>
<body>

<nav>
  <div class="container">
    <a href="#" class="brand">
      <!-- Logo A: simple teardrop (LOGO_STYLE = 'simple') -->
      <svg id="logoSimple" viewBox="0 0 100 100" fill="none" xmlns="http://www.w3.org/2000/svg">
        <circle cx="50" cy="50" r="50" fill="#5B6F3A"/>
        <path class="logo-drop" d="M50 22 C50 22 33 45 33 57 C33 65.5 40.5 72 50 72 C59.5 72 67 65.5 67 57 C67 45 50 22 50 22Z" fill="#E8A23A"/>
        <path class="logo-leaf" d="M24 64 C35 76 65 76 76 64 C65 71 35 71 24 64Z" fill="#0F5D4E"/>
      </svg>
      <!-- Logo B: leaf cupping a droplet (LOGO_STYLE = 'concept5') -->
      <svg id="logoConcept5" viewBox="0 0 200 200" fill="none" xmlns="http://www.w3.org/2000/svg" style="display:none">
        <circle cx="100" cy="100" r="95" fill="#6b7a3a"/>
        <path class="logo-drop" d="M100 46 C112 64 120 78 120 90 C120 102 111 110 100 110 C89 110 80 102 80 90 C80 78 88 64 100 46 Z" fill="#e8a13c"/>
        <path class="logo-leaf" d="M42 112 C55 157 145 157 158 112 C140 132 60 132 42 112 Z" fill="#1a5c4a"/>
        <path d="M52 117 C72 143 128 143 148 117" stroke="#6b7a3a" stroke-width="2.5" fill="none" stroke-linecap="round"/>
      </svg>
      <span class="brand-text">Etaleme Solutions</span>
    </a>

    <div class="nav-right">
      <ul>
        <li><a href="#mission" class="nav-link" data-en="Our Mission" data-am="የእኛ ተልዕኮ" data-om="Ergama Keenya">Our Mission</a></li>
        <li><a href="#products" class="nav-link" data-en="Products" data-am="ዕቃዎች" data-om="Oomishaalee">Products</a></li>
        <li><a href="#faq" class="nav-link" data-en="FAQ" data-am="ተደጋጋሚ ጥያቄዎች" data-om="Gaaffilee">FAQ</a></li>
        <li><a href="#partners" class="nav-link" data-en="Partners" data-am="አጋሮች" data-om="Michoottan">Partners</a></li>
        <li><a href="#contact" class="nav-link" data-en="Contact" data-am="ያግኙን" data-om="Nu Qunnamaa">Contact</a></li>
      </ul>
      <div class="lang-group" id="langGroup" role="group" aria-label="Language selection">
        <button class="lang-btn" data-lang="en" aria-label="Switch to English" aria-pressed="true">EN</button>
        <button class="lang-btn" data-lang="am" aria-label="Switch to Amharic" aria-pressed="false">አማ</button>
        <button class="lang-btn" data-lang="om" aria-label="Switch to Afaan Oromo" aria-pressed="false">OR</button>
      </div>
    </div>
  </div>
</nav>

<!-- INTRO VIDEO: upload your MP4 next to this file, set HERO_VIDEO in the settings. Hides itself if off or missing. -->
<section class="video-hero" id="videoHero" style="display:none; padding:0">
  <video id="heroVideo" autoplay muted loop playsinline preload="metadata" aria-hidden="true">
    <source id="heroVideoSrc" type="video/mp4">
  </video>
  <div class="video-text"
       data-en="Reusable body care, made with dignity."
       data-am="በክብር የተመሠረተ ዳግም የሚያገለግል የሰውነት እንክብካቤ።"
       data-om="Kunuunsa qaamaa deebi'ee itti fayyadamamu, ulfinaan hojjetame.">Reusable body care, made with dignity.</div>
</section>

<header>
  <div class="container reveal">
    <div class="hero-text">
      <h1 data-en="Reusable body care, made with dignity."
          data-am="በክብር የተመሠረተ ዳግም የሚያገለግል የሰውነት እንክብካቤ።"
          data-om="Kunuunsa qaamaa deebi'ee itti fayyadamamu, ulfinaan hojjetame.">Reusable body care, made with dignity.</h1>
      <p data-en="Affordable, skin-friendly, reusable alternatives for mothers, fistula patients, nursing mothers, active adults, and women across Addis Ababa and Sheger City."
         data-am="በአዲስ አበባና በሸገር ከተማ ለእናቶች፣ ለፊስቱላ ታካሚዎች፣ ለጡት አጥባቢ እናቶች፣ ለንቁ አዋቂዎች እና ለሴቶች ተመጣጣኝ፣ ለቆዳ ተስማሚ እና ዳግም የሚውሉ አማራጮች።"
         data-om="Addis Ababaa fi Magaalaa Shaggar keessatti haadhotaaf, dhukkubsattoota fistulaaf, haadhota harma hoosisaniif, namoota jajjaboo fi dubartootaaf filannoo gatii madaalawaa, gogaaf mijataa fi deebi'anii itti fayyadamamu.">Affordable, skin-friendly, reusable alternatives for mothers, fistula patients, nursing mothers, active adults, and women across Addis Ababa and Sheger City.</p>

      <a href="#contact" class="cta" data-en="Get in Touch" data-am="ያግኙን" data-om="Nu Qunnamaa">Get in Touch</a>
      <div>
        <span class="status-line" data-en="Launching soon — join our early-access list" data-am="በቅርቡ ይጀምራል — ቀድሞ ተጠቃሚ ይሁኑ" data-om="Dhiyootti ni jalqabna — tarreeffama dursaa keessatti makamaa">Launching soon — join our early-access list</span>
      </div>
    </div>

    <div class="hero-image">
      <!-- CHANGE "hero.jpg" TO YOUR REAL IMAGE FILENAME, AND UPDATE THE alt TEXT TO MATCH THE PICTURE -->
      <img src="hero.jpg" alt="Etaleme Solutions hero illustration">
    </div>
  </div>
</header>

<section class="mission reveal" id="mission">
  <div class="container">
    <h2 data-en="Our Mission" data-am="የእኛ ተልዕኮ" data-om="Ergama Keenya">Our Mission</h2>
    <p data-en="Etaleme Solutions exists to solve real problems — the recurring cost of disposables, skin irritation from chemical exposure, the loss of dignity for fistula patients, and the environmental burden of single-use products. We provide affordable, skin-friendly, reusable alternatives that protect health, restore dignity, and reduce waste."
       data-am="እታለሜ ሶሉሽንስ ችግሮችን ለመፍታት ይኖራል — የአንድ ጊዜ መገልገያ ዕቃዎች ተደጋጋሚ ወጪ፣ ከኬሚካል ጋር በተገናኘ የቆዳ መቆጣት፣ የፊስቱላ ታካሚዎች የክብር መጓደል፣ እና የአንድ ጊዜ መገልገያ ዕቃዎች የአካባቢ ጫና። ጤናን የሚጠብቅ፣ ክብርን የሚመልስ እና ብክነትን የሚቀንስ ተመጣጣኝ እና ለቆዳ ተስማሚ፣ ዳግም የሚያገለግል አማራጮችን እናቀርባለን።"
       data-om="Etaleme Solutions rakkoolee dhugaa furuuf jira — baasii irra deddeebi'ee meeshaalee yeroo tokkoof oolan, miidhaa gogaa kan kemikaalaan dhufu, ulfina dhukkubsattoota fistulaa dhabamuu, akkasumas culaalaa naannoo meeshaalee yeroo tokkoof oolan. Filannoo gatii madaalawaa, gogaaf mijataa, deebi'anii itti fayyadamamu kan fayyaa eegu, ulfina deebisu, xurii immoo xiqqeessinu ni kenninaa.">Etaleme Solutions exists to solve real problems — the recurring cost of disposables, skin irritation from chemical exposure, the loss of dignity for fistula patients, and the environmental burden of single-use products. We provide affordable, skin-friendly, reusable alternatives that protect health, restore dignity, and reduce waste.</p>
  </div>
</section>

<section class="why reveal" id="why">
  <div class="container">
    <h2 data-en="Why Reusable?" data-am="ለምን ዳግም የሚያገለግል?" data-om="Maaliif Deebi'anii Itti Fayyadamamu?">Why Reusable?</h2>
    <p data-en="Disposable products add up — financially and environmentally. A reusable pad or pair of shorts is washed and used again, cutting the ongoing cost to households and reducing the waste that single-use products leave behind. For patients managing fistula or heavy postpartum flow, reusable design also means not running out at the wrong moment."
       data-am="የአንድ ጊዜ መገልገያ ዕቃዎች ወጪያቸው ይጨምራል — በገንዘብም በአካባቢም። ዳግም የሚያገለግል ጨርቅ ወይም ቁምጣ ታጥቦ ደጋግሞ ስለሚያገለግል ለቤተሰብ ያለማቋረጥ ወጪን ይቀንሳል እንዲሁም የአንድ ጊዜ መገልገያ ዕቃዎች የሚተዉትን ቆሻሻ ይቀንሳል። ፊስቱላን ወይም ከፍተኛ የወሊድ በኋላ ፍሰትን ለሚያስግዱ ታካሚዎች፣ ዳግም የሚያገለግል ንድፍ በተሳሳተ ሰዓት እንዳያልቅባቸው ያግዛል።"
       data-om="Meeshaaleen yeroo tokkoof oolan baasii guddaa fida — maallaqaanis ta'e naannoodhaan. Bastrii ykn sureeffaa deebi'anii itti fayyadaman dhiqamanii irra deddeebi'anii waan fayyadamaniif, baasii maatiif yeroo hunda jiru ni xiqqeessu, xuriin meeshaalee yeroo tokkoof oolan hambisanis ni hir'isu. Dhukkubsattoota fistulaa ykn dhangala'aa da'umsaa booda guddaa qabaniif, dizaayinni deebi'anii itti fayyadamuu yeroo sirrii hin taaneen akka hin dhumne gargaara.">Disposable products add up — financially and environmentally. A reusable pad or pair of shorts is washed and used again, cutting the ongoing cost to households and reducing the waste that single-use products leave behind. For patients managing fistula or heavy postpartum flow, reusable design also means not running out at the wrong moment.</p>
  </div>
</section>

<section class="products reveal" id="products">
  <div class="container">
    <h2 data-en="Our Products" data-am="የእኛ ዕቃዎች" data-om="Oomishaalee Keenya">Our Products</h2>
    <div class="grid">
      <div class="card">
        <h3 data-en="Maternity Pads & Diapers" data-am="የእናቶች የንጽህና ጨርቆች እና ዳይፐሮች" data-om="Baaxii fi Daayipara Haadholii">Maternity Pads & Diapers</h3>
        <p data-en="Reusable, gentle protection designed for comfort and confidence during postpartum recovery."
           data-am="ከወሊድ በኋላ ማገገሚያ ወቅት ምቾትን እና በራስ መተማመንን ለመስጠት የተሰናዱ ዳግም የሚውሉ፣ ለስላሳ ጥበቃዎች።"
           data-om="Eegumsa deebi'anii itti fayyadamamu, mi'aawaa, yeroo fayyaa da'umsaa booda deebisaniif mijaawaa fi of-amanuu kenniif qophaa'e.">Reusable, gentle protection designed for comfort and confidence during postpartum recovery.</p>
      </div>
      <div class="card">
        <h3 data-en="Fistula Diapers" data-am="የፊስቱላ ዳይፐሮች" data-om="Daayipara Fistulaa">Fistula Diapers</h3>
        <p data-en="Dignified protection for patients managing continuous flow — designed for daily life."
           data-am="ያለማቋረጥ ፍሰት ላለባቸው ታካሚዎች ክብርን የጠበቀ ጥበቃ — ለዕለት ተዕለት ኑሮ የተሰናዳ።"
           data-om="Eegumsa ulfina qabu dhukkubsattoota dhangala'aa addaan hin cinneen rakkataniif — jireenya guyyuu keessaaf qophaa'e.">Dignified protection for patients managing continuous flow — designed for daily life.</p>
      </div>
      <div class="card">
        <h3 data-en="Breast Pads" data-am="የጡት ጨርቆች" data-om="Baaxii Harmaa">Breast Pads</h3>
        <p data-en="Soft, washable pads designed to help keep nursing mothers dry and comfortable."
           data-am="ጡት አጥባቢ እናቶችን ደረቅ እና ምቹ ለማድረግ የታሰቡ ለስላሳ፣ ሊታጠቡ የሚችሉ ጨርቆች።"
           data-om="Baaxii mi'aawaa, dhiqamuu danda'u kan haadhota harma hoosisan gogaa fi mijataa taasisuuf qophaa'e.">Soft, washable pads designed to help keep nursing mothers dry and comfortable.</p>
      </div>
      <div class="card olive">
        <h3 data-en="Sweat Pads" data-am="የላብ ጨርቆች" data-om="Baaxii Dafaa">Sweat Pads</h3>
        <p data-en="A chemical-free fabric shield that absorbs underarm sweat — a gentler option for active adults."
           data-am="የብብት ላብን የሚስብ ከኬሚካል ነፃ የጨርቅ ጥበቃ — ለንቁ አዋቂዎች ለስላሳ አማራጭ።"
           data-om="Haguuggii uffataa kemikaala hin qabne kan dafaa gudeeda jala xuuxu — namoota jajjaboof filannoo mi'aawaa.">A chemical-free fabric shield that absorbs underarm sweat — a gentler option for active adults.</p>
      </div>
      <div class="card olive">
        <h3 data-en="AeroLayer Dignity Shorts" data-am="ኤሮሌየር የክብር ቁምጣዎች" data-om="Sureeffaa Ulfinaa AeroLayer">AeroLayer Dignity Shorts</h3>
        <p data-en="Comfortable, breathable pull-on shorts, designed to be worn with confidence under long or wide dresses."
           data-am="ምቹ እና አየር የሚያስገቡ፣ በቀላሉ የሚለበሱ ቁምጣዎች፣ ረዣዥም ወይም ሰፊ ልብሶች ስር በልበ ሙሉነት ለመልበስ የተሰናዳ።"
           data-om="Sureeffaa mijataa, qilleensa dabarsu, salphaatti uffatamu, uffata dheeraa ykn balʼaa jalatti of-amanuun uffachuuf qophaa'e.">Comfortable, breathable pull-on shorts, designed to be worn with confidence under long or wide dresses.</p>
      </div>
    </div>
  </div>
</section>

<section class="faq reveal" id="faq">
  <div class="container">
    <h2 data-en="Frequently Asked Questions" data-am="ተደጋጋሚ ጥያቄዎች" data-om="Gaaffilee Yeroo Baay'ee Gaafataman">Frequently Asked Questions</h2>
    <div class="faq-item">
      <h3 data-en="How do I wash and care for these products?" data-am="እነዚህን ዕቃዎች እንዴት አጥባቸዋለሁ?" data-om="Oomishaalee kana akkamittin dhiqaa, kunuunsas nan godha?">How do I wash and care for these products?</h3>
      <p data-en="Care instructions vary by product and will be included with each item once available. As a general guide, items in frequent contact with high flow should be washed after each use."
         data-am="የአጠባበቅ መመሪያ እንደ እያንዳንዱ ዕቃ ይለያያል፣ ዕቃው ዝግጁ ሲሆን ከምርቱ ጋር ይካተታል። በአጠቃላይ ግን ከፍተኛ ፍሰት ጋር ደጋግሞ ንክኪ ያላቸው ዕቃዎች በየአጠቃቀማቸው ሊታጠቡ ይገባል።"
         data-om="Qajeelfamni kunuunsaa akka oomishaatti adda addaa ta'a, yeroo oomishni qophaa'utti wajjin ni dabalama. Haala waliigalaatiin, meeshaaleen dhangala'aa baay'ee waliin yeroo baay'ee wal qunnaman tajaajila tokkoon booda dhiqamuu qabu.">Care instructions vary by product and will be included with each item once available. As a general guide, items in frequent contact with high flow should be washed after each use.</p>
    </div>
    <div class="faq-item">
      <h3 data-en="How long do they last?" data-am="ለምን ያህል ጊዜ ያገለግላሉ?" data-om="Hanga meeqaatti tajaajilu?">How long do they last?</h3>
      <p data-en="This depends on the product and how it's cared for. We're finalizing durability figures through our own testing and will publish them once confirmed."
         data-am="ይህ እንደ ዕቃው እና አያያዙ ይለያያል። የመቆያ ጊዜያቸውን በራሳችን ሙከራ እያረጋገጥን ሲሆን ከተረጋገጠ በኋላ እናሳውቃለን።"
         data-om="Kun akka oomishichaa fi kunuunsa isaatti garaagarummaa qabaata. Dheerina tajaajila isaanii qorannoo keenyaan mirkaneessaa jirra, erga mirkanaa'ee boodas ni beeksifna.">This depends on the product and how it's cared for. We're finalizing durability figures through our own testing and will publish them once confirmed.</p>
    </div>
    <div class="faq-item">
      <h3 data-en="How many will I need?" data-am="ስንት ያስፈልጉኛል?" data-om="Meeqatu na barbaachisa?">How many will I need?</h3>
      <p data-en="We'll provide guidance per product once pricing and pack sizes are finalized — join our early-access list to be notified."
         data-am="ዋጋ እና የጥቅል መጠን ከተወሰነ በኋላ ለእያንዳንዱ ዕቃ መመሪያ እንሰጣለን — እንድናሳውቅዎ ቀድሞ ተጠቃሚ ይሁኑ።"
         data-om="Gatiin fi hangi paakeejii erga murtaa'ee booda oomisha hundaaf qajeelfama ni kennina — akka beeksifamtaniif tarreeffama dursaa keessatti makamaa.">We'll provide guidance per product once pricing and pack sizes are finalized — join our early-access list to be notified.</p>
    </div>
    <div class="faq-item">
      <h3 data-en="Is my information kept private?" data-am="መረጃዬ በሚስጥር ይቀመጣል?" data-om="Odeeffannoon koo iccitiidhaan ni eegamaa?">Is my information kept private?</h3>
      <p data-en="Yes. Information you share through this site is used only to respond to your inquiry and is not shared with third parties."
         data-am="አዎ። በዚህ ድረ-ገጽ በኩል የሚያጋሩት መረጃ ለጥያቄዎ ምላሽ ለመስጠት ብቻ ጥቅም ላይ ይውላል፣ ለሶስተኛ ወገን አይተላለፍም።"
         data-om="Eeyyee. Odeeffannoon marsariitii kana irraa qoodattan gaaffii keessan deebisuuf qofa itti fayyadama, gara namoota sadaffaattis hin daddabarfamu.">Yes. Information you share through this site is used only to respond to your inquiry and is not shared with third parties.</p>
    </div>
  </div>
</section>

<section class="partners reveal" id="partners">
  <div class="container">
    <h2 data-en="Who We Serve" data-am="እነማንን እናገለግላለን" data-om="Eenyuuf Tajaajilla">Who We Serve</h2>
    <p data-en="We aim to reach the women who need these products most through local retailers and through institutions that serve them."
       data-am="እነዚህን ዕቃዎች በብዙ የሚያስፈልጉባቸውን ሴቶች በአካባቢ ንግዶች እና በሚያገለግሏቸው ተቋማት በኩል ለመድረስ እንሻለን።"
       data-om="Dubartoota oomishaalee kana caalaatti barbaadan gurgurtoota naannoo fi dhaabbilee isaan tajaajilan karaa isaaniitiin gahuuf kaayyeffanne.">We aim to reach the women who need these products most through local retailers and through institutions that serve them.</p>
    <div class="partner-tags">
      <span class="tag" data-en="Pharmacies" data-am="ፋርማሲዎች" data-om="Faarmaasiiwwan">Pharmacies</span>
      <span class="tag" data-en="Baby Stores" data-am="የህፃናት ሱቆች" data-om="Suuqii Daa'immanii">Baby Stores</span>
      <span class="tag" data-en="Women's Clothing Stores" data-am="የሴቶች ልብስ ሱቆች" data-om="Suuqii Uffata Dubartootaa">Women's Clothing Stores</span>
      <span class="tag" data-en="Institutions we aim to supply (prospective)" data-am="ለማቅረብ ያለምናቸው ተቋማት (እቅድ ላይ)" data-om="Dhaabbilee dhiyeessuu barbaannu (karoora irra jiru)">Institutions we aim to supply (prospective)</span>
      <span class="tag">UNFPA</span>
      <span class="tag" data-en="Hamlin / Desta Mender" data-am="ሃምሊን / ደስታ መንደር" data-om="Hamlin / Desta Mender">Hamlin / Desta Mender</span>
    </div>
  </div>
</section>

<section class="contact reveal" id="contact">
  <div class="container">
    <h2 data-en="Contact Us" data-am="ያግኙን" data-om="Nu Qunnamaa">Contact Us</h2>

    <div class="contact-ctas">
      <a href="#contactForm" class="inst" data-en="For Clinics & Organizations" data-am="ለክሊኒኮችና ድርጅቶች" data-om="Kiliinikaalee fi Dhaabbilleef">For Clinics & Organizations</a>
      <a href="#contactForm" class="indiv" data-en="For You" data-am="ለእርስዎ" data-om="Siif">For You</a>
    </div>

    <div class="chat-ctas" id="chatCtas">
      <a href="#" id="telegramBtn" class="chat-btn telegram" target="_blank" rel="noopener"
         data-en="Message us on Telegram" data-am="በቴሌግራም መልእክት ይላኩልን" data-om="Telegramiin nuuf barreessaa">Message us on Telegram</a>
      <a href="#" id="callBtn" class="chat-btn call"
         data-en="Call us" data-am="ይደውሉልን" data-om="Nuuf Bilbilaa">Call us</a>
      <a href="#" id="whatsappBtn" class="chat-btn whatsapp" target="_blank" rel="noopener"
         data-en="Message us on WhatsApp" data-am="በዋትስአፕ መልእክት ይላኩልን" data-om="WhatsAppiin nuuf barreessaa">Message us on WhatsApp</a>
    </div>

    <form id="contactForm">
      <input type="text" name="_gotcha" tabindex="-1" autocomplete="off" aria-hidden="true" style="display:none">
      <label for="nameInput" data-en="Your name" data-am="ስምዎ" data-om="Maqaa Keessan">Your name</label>
      <input id="nameInput" type="text" name="name" data-en-ph="Your name" data-am-ph="ስምዎ" data-om-ph="Maqaa Keessan" placeholder="Your name" required>

      <label for="emailInput" data-en="Your email" data-am="ኢሜይልዎ" data-om="Imeelii Keessan">Your email</label>
      <input id="emailInput" type="email" name="email" data-en-ph="Your email" data-am-ph="ኢሜይልዎ" data-om-ph="Imeelii Keessan" placeholder="Your email" required>

      <label for="messageInput" data-en="Your message or inquiry" data-am="መልእክትዎ ወይም ጥያቄዎ" data-om="Ergaa Keessan Yookiin Gaaffii Keessan">Your message or inquiry</label>
      <textarea id="messageInput" name="message" data-en-ph="Your message or inquiry" data-am-ph="መልእክትዎ ወይም ጥያቄዎ" data-om-ph="Ergaa keessan yookiin gaaffii keessan" placeholder="Your message or inquiry" required></textarea>

      <button type="submit" data-en="Send Inquiry" data-am="ጥያቄ ላክ" data-om="Gaaffii Ergi">Send Inquiry</button>
      <p class="privacy-note" data-en="We only use this information to respond to you — it is not shared with third parties."
         data-am="ይህን መረጃ ለእርስዎ ምላሽ ለመስጠት ብቻ እንጠቀማለን — ለሶስተኛ ወገን አይተላለፍም።"
         data-om="Odeeffannoo kana deebii isiniif kennuuf qofa itti fayyadamna — gara namoota sadaffaatti hin daddabarfamu.">We only use this information to respond to you — it is not shared with third parties.</p>
      <p class="form-status" id="formStatus" role="status" aria-live="polite"></p>
    </form>

    <p class="email-alt" id="emailLine"><span data-en="Or email us directly at" data-am="ወይም በቀጥታ ወደዚህ ኢሜይል ይላኩን" data-om="Yookiin kallattiin imeelii kanaan nu qunnamaa">Or email us directly at</span> <strong><a id="emailLink" href="mailto:info@etaleme.com">info@etaleme.com</a></strong></p>
    <p class="phone-line" id="phoneLine"><span data-en="Call or message us on Telegram:" data-am="ይደውሉልን ወይም በቴሌግራም ያግኙን፦" data-om="Bilbilaa ykn Telegramiin nu qunnamaa:">Call or message us on Telegram:</span> <strong><a id="phoneLink" href="tel:+2519XXXXXXXX">+251 9XX XXX XXX</a></strong></p>
  </div>
</section>

<footer>
  <div class="container">
    <span id="footerText" data-en="© 2026 Etaleme Solutions · Addis Ababa & Sheger City, Ethiopia"
       data-am="© 2026 እታለሜ ሶሉሽንስ · አዲስ አበባ እና ሸገር ከተማ፣ ኢትዮጵያ"
       data-om="© 2026 Etaleme Solutions · Addis Ababaa fi Magaalaa Shaggar, Itoophiyaa">© 2026 Etaleme Solutions · Addis Ababa & Sheger City, Ethiopia</span>
  </div>
</footer>

<script>
  // ==================== SETTINGS ====================
  const AMHARIC_ENABLED = true;
  const OROMO_ENABLED   = true;

  // Intro video (8–13 s loop, MP4, ideally under 5 MB)
  const SHOW_HERO_VIDEO = true;
  const HERO_VIDEO = 'intro.mp4';
  const HERO_VIDEO_POSTER = 'hero.jpg';

  // Logo: 'simple' = teardrop + curve   |   'concept5' = leaf cupping a droplet
  const LOGO_STYLE = 'simple';

  const CONTACT_EMAIL = 'etalemesolutions@gmail.com';
  const CONTACT_PHONE_DISPLAY = '+251 723581334';
  const CONTACT_PHONE_TEL     = '+251723581334';
  const SHOW_PHONE = false;      // shows the number as text
  const SHOW_CALL_BUTTON = true; // shows a "Call us" button without printing the number

  const FORMSPREE_ENDPOINT = 'https://formspree.io/f/xdeajvzr';

  const SHOW_TELEGRAM   = true;
  const TELEGRAM_USERNAME = 'Malefyae';
  const SHOW_WHATSAPP   = true;
  const WHATSAPP_NUMBER = '251723581334';
  const WHATSAPP_GREETING = "Hello, I'd like to know more about Etaleme's products.";
  // ==================================================

  // ==================== INTRO VIDEO ====================
  (function () {
    const box = document.getElementById('videoHero');
    if (!SHOW_HERO_VIDEO || !HERO_VIDEO) return;
    const vid = document.getElementById('heroVideo');
    const src = document.getElementById('heroVideoSrc');
    vid.poster = HERO_VIDEO_POSTER;
    src.src = HERO_VIDEO;
    box.style.display = '';
    src.addEventListener('error', () => { box.style.display = 'none'; });
    vid.load();
    if (window.matchMedia('(prefers-reduced-motion: reduce)').matches) {
      vid.removeAttribute('autoplay');
      vid.pause();
    } else {
      const p = vid.play();
      if (p && p.catch) p.catch(() => {});
    }
  })();
  // ==================================================

  // ==================== LOGO SWITCH ====================
  if (LOGO_STYLE === 'concept5') {
    document.getElementById('logoSimple').style.display = 'none';
    document.getElementById('logoConcept5').style.display = '';
  }
  // ==================================================

  // ==================== SCROLL ANIMATIONS ====================
  const revealEls = document.querySelectorAll('.reveal');
  if ('IntersectionObserver' in window) {
    const observer = new IntersectionObserver((entries) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          entry.target.classList.add('active');
          observer.unobserve(entry.target);
        }
      });
    }, { threshold: 0, rootMargin: '0px 0px -5% 0px' });
    revealEls.forEach((el) => observer.observe(el));
    // Safety net: never leave content hidden
    setTimeout(() => revealEls.forEach((el) => el.classList.add('active')), 3000);
  } else {
    revealEls.forEach((el) => el.classList.add('active'));
  }
  // ==================================================

  let currentLang = 'en';

  function applyLang(lang) {
    currentLang = lang;
    document.querySelectorAll('[data-en]').forEach(el => {
      const val = el.getAttribute('data-' + lang);
      if (val) el.textContent = val;
    });
    document.querySelectorAll('[data-en-ph]').forEach(el => {
      const val = el.getAttribute('data-' + lang + '-ph');
      if (val) el.placeholder = val;
    });
    document.documentElement.lang = lang;
    if (typeof refreshStatus === 'function') refreshStatus();

    document.querySelectorAll('.lang-btn').forEach(btn => {
      btn.setAttribute('aria-pressed', btn.dataset.lang === lang ? 'true' : 'false');
    });
  }

  document.querySelectorAll('.lang-btn').forEach(btn => {
    btn.addEventListener('click', () => applyLang(btn.dataset.lang));
  });

  if (!AMHARIC_ENABLED) {
    document.querySelector('.lang-btn[data-lang="am"]').style.display = 'none';
  }
  if (!OROMO_ENABLED) {
    document.querySelector('.lang-btn[data-lang="om"]').style.display = 'none';
  }

  document.getElementById('emailLink').textContent = CONTACT_EMAIL;
  document.getElementById('emailLink').href = 'mailto:' + CONTACT_EMAIL;

  const phoneLine = document.getElementById('phoneLine');
  if (!SHOW_PHONE) {
    phoneLine.style.display = 'none';
  } else {
    document.getElementById('phoneLink').textContent = CONTACT_PHONE_DISPLAY;
    document.getElementById('phoneLink').href = 'tel:' + CONTACT_PHONE_TEL;
  }

  const telegramBtn = document.getElementById('telegramBtn');
  const whatsappBtn = document.getElementById('whatsappBtn');
  telegramBtn.href = 'https://t.me/' + TELEGRAM_USERNAME;
  whatsappBtn.href = 'https://wa.me/' + WHATSAPP_NUMBER + '?text=' + encodeURIComponent(WHATSAPP_GREETING);
  const callBtn = document.getElementById('callBtn');
  callBtn.href = 'tel:' + CONTACT_PHONE_TEL;
  if (!SHOW_CALL_BUTTON) callBtn.style.display = 'none';
  if (!SHOW_TELEGRAM) telegramBtn.style.display = 'none';
  if (!SHOW_WHATSAPP) whatsappBtn.style.display = 'none';
  if (!SHOW_TELEGRAM && !SHOW_WHATSAPP && !SHOW_CALL_BUTTON) document.getElementById('chatCtas').style.display = 'none';

  const formMessages = {
    sending: { en: 'Sending…', am: 'በመላክ ላይ…', om: 'Ergaa jira…' },
    sent:    { en: "Message sent — thank you! We'll get back to you soon.",
               am: 'መልእክትዎ ተልኳል — እናመሰግናለን! በቅርቡ እንመልስልዎታለን።',
               om: 'Ergaan ergameera — galatoomaa! Dhiyootti isin deebisna.' },
    error:   { en: 'Sorry, something went wrong. Please try again or email us directly.',
               am: 'ይቅርታ፣ የሆነ ችግር ተፈጥሯል። እባክዎ እንደገና ይሞክሩ ወይም በቀጥታ ኢሜይል ይላኩልን።',
               om: "Dhiifama, rakkoon uumameera. Maaloo irra deebi'aa yaalaa ykn kallattiin imeelii nuuf ergaa." }
  };
  let statusKey = null;
  const statusEl = document.getElementById('formStatus');

  function refreshStatus() {
    if (!statusKey) return;
    statusEl.textContent = formMessages[statusKey][currentLang];
    statusEl.classList.add('visible');
    statusEl.classList.toggle('error', statusKey === 'error');
  }
  function showStatus(key) { statusKey = key; refreshStatus(); }

  document.getElementById('contactForm').addEventListener('submit', async function(e) {
    e.preventDefault();
    const btn = this.querySelector('button[type="submit"]');
    btn.disabled = true;
    showStatus('sending');
    try {
      const res = await fetch(FORMSPREE_ENDPOINT, {
        method: 'POST',
        body: new FormData(this),
        headers: { 'Accept': 'application/json' }
      });
      if (res.ok) { this.reset(); showStatus('sent'); }
      else { showStatus('error'); }
    } catch (err) {
      showStatus('error');
    }
    btn.disabled = false;
  });
</script>

</body>
</html>
