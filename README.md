# etaleme-website-
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Etaleme Solutions — Reusable Body Care, Made with Dignity</title>
<meta name="description" content="Affordable, skin-safe, reusable body care alternatives for mothers, fistula patients, nursing mothers, and modest women across Addis Ababa and Sheger City.">
<style>
  :root {
    --primary: #1a5c4a;
    --accent:  #e8a13c;
    --bg:      #faf7f2;
    --text:    #2b2b2b;
    --light:   #ffffff;
  }
  * { margin: 0; padding: 0; box-sizing: border-box; }
  body {
    font-family: 'Segoe UI', system-ui, sans-serif;
    color: var(--text); background: var(--bg); line-height: 1.6;
  }
  .container { max-width: 1000px; margin: 0 auto; padding: 0 20px; }

  nav {
    background: var(--light); padding: 16px 0;
    box-shadow: 0 1px 4px rgba(0,0,0,.08);
    position: sticky; top: 0; z-index: 10;
  }
  nav .container { display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 10px; }
  .logo { font-weight: 700; color: var(--primary); font-size: 1.2rem; text-decoration: none; }
  .nav-right { display: flex; align-items: center; gap: 20px; flex-wrap: wrap; }
  nav ul { list-style: none; display: flex; gap: 20px; flex-wrap: wrap; }
  nav a { text-decoration: none; color: var(--text); font-weight: 500; }
  nav a:hover { color: var(--primary); }
  .lang-btn {
    background: var(--primary); color: var(--light); border: none;
    padding: 8px 16px; border-radius: 20px; cursor: pointer; font-weight: 600;
  }

  header { padding: 80px 0 60px; text-align: center; }
  header h1 { font-size: clamp(1.6rem, 5vw, 3rem); color: var(--primary); margin-bottom: 16px; }
  header p { max-width: 720px; margin: 0 auto; font-size: 1.15rem; color: #555; }
  .cta {
    display: inline-block; margin-top: 28px; padding: 14px 32px;
    background: var(--primary); color: var(--light);
    border-radius: 30px; text-decoration: none; font-weight: 600;
  }
  .cta:hover { background: #14453a; }

  .mission { padding: 60px 0; }
  .mission h2 { color: var(--primary); margin-bottom: 16px; font-size: 1.8rem; }
  .mission p { max-width: 760px; font-size: 1.05rem; color: #444; }

  .products { padding: 60px 0; }
  .products h2 { color: var(--primary); text-align: center; margin-bottom: 40px; font-size: 1.8rem; }
  .grid { display: grid; gap: 24px; grid-template-columns: repeat(auto-fit, minmax(260px, 1fr)); }
  .card {
    background: var(--light); border-radius: 12px; padding: 28px;
    box-shadow: 0 2px 8px rgba(0,0,0,.06); border-top: 4px solid var(--accent);
  }
  .card h3 { color: var(--primary); margin-bottom: 10px; font-size: 1.15rem; }
  .card p { font-size: .95rem; color: #555; }

  .partners { padding: 60px 0; text-align: center; }
  .partners h2 { color: var(--primary); margin-bottom: 16px; font-size: 1.8rem; }
  .partners p { max-width: 700px; margin: 0 auto 30px; color: #555; }
  .partner-tags { display: flex; flex-wrap: wrap; gap: 12px; justify-content: center; }
  .tag {
    background: var(--light); border: 1px solid #ddd;
    padding: 8px 20px; border-radius: 20px; font-size: .9rem; color: #444;
  }

  .contact { padding: 60px 0 80px; }
  .contact h2 { color: var(--primary); text-align: center; margin-bottom: 30px; font-size: 1.8rem; }
  form { max-width: 520px; margin: 0 auto; display: grid; gap: 16px; }
  input, textarea {
    padding: 14px; border: 1px solid #ccc; border-radius: 8px;
    font-size: 1rem; font-family: inherit; width: 100%;
  }
  textarea { min-height: 120px; resize: vertical; }
  button {
    padding: 14px; background: var(--primary); color: var(--light);
    border: none; border-radius: 8px; font-size: 1rem; font-weight: 600; cursor: pointer;
  }
  button:hover { background: #14453a; }
  .email-alt { text-align: center; margin-top: 20px; color: #555; }
  .phone-line { text-align: center; margin-top: 8px; color: #555; }

  footer { background: var(--primary); color: var(--light); text-align: center; padding: 24px 0; font-size: .9rem; }
</style>
</head>
<body>

<nav>
  <div class="container">
    <a href="#" class="logo">Etaleme Solutions</a>
    <div class="nav-right">
      <ul>
        <li><a href="#mission" data-en="Our Mission" data-am="የእኛ ተልዕኮ">Our Mission</a></li>
        <li><a href="#products" data-en="Products" data-am="ዕቃዎች">Products</a></li>
        <li><a href="#partners" data-en="Partners" data-am="አጋሮች">Partners</a></li>
        <li><a href="#contact" data-en="Contact" data-am="ያግኙን">Contact</a></li>
      </ul>
      <button class="lang-btn" id="langToggle" onclick="toggleLang()">አማ</button>
    </div>
  </div>
</nav>

<header>
  <div class="container">
    <h1 data-en="Etaleme Solutions — Reusable body care, made with dignity."
        data-am="እተለመ ሶሉሽንስ — በክብር የተመሠረተ ዳግም የሚውል የሰውነት እንክብካቬ።">Etaleme Solutions — Reusable body care, made with dignity.</h1>
    <p data-en="Affordable, skin-safe, reusable alternatives for mothers, fistula patients, nursing mothers, active adults, and modest women across Addis Ababa and Sheger City."
       data-am="በአዲስ አበባና በሸገር ከተማ ለእናቶች፣ ለፊስቱላ ታካሚዎች፣ ለጡት አጥባቢ እናቶች፣ ለንቁ አዋቂዎች እና ለስሜታዊ ሴቶች ተመጣጣኝ፣ ለቆዳ ጤና ጤናማ እና ዳግም የሚውሉ አማራጮች።">Affordable, skin-safe, reusable alternatives for mothers, fistula patients, nursing mothers, active adults, and modest women across Addis Ababa and Sheger City.</p>
    <a href="#contact" class="cta" data-en="Get in Touch" data-am="ያግኙን">Get in Touch</a>
  </div>
</header>

<section class="mission" id="mission">
  <div class="container">
    <h2 data-en="Our Mission" data-am="የእኛ ተልዕኮ">Our Mission</h2>
    <p data-en="Etaleme Solutions exists to solve real problems — the recurring cost of disposables, skin irritation from chemical exposure, the loss of dignity for fistula patients, and the environmental burden of single-use products. We provide affordable, skin-safe, reusable alternatives that protect health, restore dignity, and reduce waste."
       data-am="እተለመ ሶሉሽንስ ችግሮችን ለመፍታት ይኖራል — የአንድ ጊዜ ዕቃዎች ደጋጋፊ ወጪ፣ ከኬሚካል ጋር በተገናኘ የቆዳ ብጉር፣ የፊስቱላ ታካሚዎች የክብር መጥፋት፣ እና የአንድ ጊዜ ዕቃዎች የአካባቢ ችግር። ጤናን የሚጠብቅ፣ ክብርን የሚመልስ እና ቆሰራሽን የሚቀንስ ተመጣጣኝ እና ዳግም የሚውል አማራጮችን እናቀርባለን።">Etaleme Solutions exists to solve real problems — the recurring cost of disposables, skin irritation from chemical exposure, the loss of dignity for fistula patients, and the environmental burden of single-use products. We provide affordable, skin-safe, reusable alternatives that protect health, restore dignity, and reduce waste.</p>
  </div>
</section>

<section class="products" id="products">
  <div class="container">
    <h2 data-en="Our Products" data-am="የእኛ ዕቃዎች">Our Products</h2>
       <div class="grid">
      <div class="card">
        <h3 data-en="Maternity Pads & Diapers" data-am="የእናቶች ጨርቆች እና ዲያፐሮች">Maternity Pads & Diapers</h3>
        <p data-en="Reusable, gentle protection designed for comfort and confidence during postpartum recovery."
           data-am="በህንፃ ማገገሚያ ወቅት ምቾትን እና እምመናን ለመስጠት የተነደፉ ዳግም የሚውሉ፣ ለሰውነት ተስማሚ ጥበቃዎች።">Reusable, gentle protection designed for comfort and confidence during postpartum recovery.</p>
      </div>
      <div class="card">
        <h3 data-en="Fistula Diapers" data-am="የፊስቱላ ዲያፐሮች">Fistula Diapers</h3>
        <p data-en="Reliable, dignified protection for patients managing continuous flow — designed for daily life."
           data-am="ያለ ማቆም ፍሰት ላለባቸው ታካሚዎች አስተማማኝ እና ክብርን የጠበቀ ጥበቃ — ለዕለታዊ ሕይወት የተነደፉ።">Reliable, dignified protection for patients managing continuous flow — designed for daily life.</p>
      </div>
      <div class="card">
        <h3 data-en="Breast Pads" data-am="የጡት ጨርቆች">Breast Pads</h3>
        <p data-en="Soft, washable pads that keep nursing mothers dry, comfortable, and irritation-free."
           data-am="ጡት አጥባቢ እናቶችን ደረቅ፣ ምቹ እና ከብጉር ነጻ የሚያደርጉ ለስላሳ እና የሚታጠቡ ጨርቆች።">Soft, washable pads that keep nursing mothers dry, comfortable, and irritation-free.</p>
      </div>
      <div class="card">
        <h3 data-en="Sweat Pads" data-am="የብርድ ጨርቆች">Sweat Pads</h3>
        <p data-en="A chemical-free alternative to deodorants and surgery — natural freshness for active adults."
           data-am="ከዴዮደራንት እና ከቀዶ ሕክምና ይልቅ ከኬሚካል ነጻ አማራጭ — ለንቁ አዋቂዎች ተፈጥሯዊ አዲስነት።">A chemical-free alternative to deodorants and surgery — natural freshness for active adults.</p>
      </div>
      <div class="card">
        <h3 data-en="AeroLayer Dignity Shorts" data-am="ኤሮሌየር የክብር እጅጌዎች">AeroLayer Dignity Shorts</h3>
        <p data-en="Comfortable, breathable shorts that give modest women confidence under long or wide dresses."
           data-am="ባረዝሙ ወይም በሰፉ ልብሶች ስር ለስሜታዊ ሴቶች እምመና የሚሰጡ ምቹ እና የሚተነፉ እጅጌዎች።">Comfortable, breathable shorts that give modest women confidence under long or wide dresses.</p>
      </div>
    </div>
  </div>
</section>

<section class="partners" id="partners">
  <div class="container">
    <h2 data-en="Our Partners" data-am="አጋሮቻችን">Our Partners</h2>
    <p data-en="We work hand-in-hand with local retailers and institutions to reach the women who need these products most."
       data-am="እነዚህን ዕቃዎች በብዙ የሚያስፈልጉባቸውን ሴቶች ለመድረስ ከአካባቢ ንግዶች እና ተቋማት ጋር እንተባበራለን።">We work hand-in-hand with local retailers and institutions to reach the women who need these products most.</p>
    <div class="partner-tags">
      <span class="tag" data-en="Pharmacies" data-am="ፋርማሲዎች">Pharmacies</span>
      <span class="tag" data-en="Baby Stores" data-am="የህፃናት ሱቆች">Baby Stores</span>
      <span class="tag" data-en="Women's Clothing Stores" data-am="የሴቶች ልብስ ሱቆች">Women's Clothing Stores</span>
      <span class="tag">UNFPA</span>
      <span class="tag" data-en="Hamlin / Desta Mender" data-am="ሃምሊን / ደስታ መንደር">Hamlin / Desta Mender</span>
    </div>
  </div>
</section>

<section class="contact" id="contact">
  <div class="container">
    <h2 data-en="Contact Us" data-am="ያግኙን">Contact Us</h2>
    <form id="contactForm">
      <input type="text" name="name" data-en-ph="Your name" data-am-ph="ስምዎ" placeholder="Your name" required>
      <input type="email" name="email" data-en-ph="Your email" data-am-ph="ኢሜይልዎ" placeholder="Your email" required>
      <textarea name="message" data-en-ph="Your message or inquiry" data-am-ph="መልእክትዎ ወይም ጥያቄዎ" placeholder="Your message or inquiry" required></textarea>
      <button type="submit" data-en="Send Inquiry" data-am="ጥያቄ ላክ">Send Inquiry</button>
    </form>
    <p class="email-alt" id="emailLine" data-en="Or email us directly at" data-am="ወይም በቀጥታ ወደዚህ ኢሜይል ይላኩን">Or email us directly at <strong>info@etaleme.com</strong></p>
    <p class="phone-line" id="phoneLine" data-en="Call or message us on Telegram:" data-am="ይደውሉልን ወይም በቴሌግራም ያግኙን፦">Call or message us on Telegram: <strong>+251 9XX XXX XXX</strong></p>
  </div>
</section>

<footer>
  <div class="container" data-en="© 2025 Etaleme Solutions · Addis Ababa & Sheger City, Ethiopia"
       data-am="© 2025 እተለመ ሶሉሽንስ · አዲስ አበባ እና ሸገር ከተማ፣ ኢትዮጵያ">
    © 2025 Etaleme Solutions · Addis Ababa & Sheger City, Ethiopia
  </div>
</footer>

<script>
  // ==================== SETTINGS ====================
  // Edit these values to configure the site — nothing else needs changing.

  // Show the አማ/EN language toggle?  true = yes, false = English-only
  const AMHARIC_ENABLED = true;

  // Your contact details (shown in the Contact section)
  const CONTACT_EMAIL = 'info@etaleme.com';   // ← replace with your real email
  const CONTACT_PHONE = '+251 9XX XXX XXX';   // ← replace with your real phone/Telegram

  // Show the phone/Telegram line?  true = yes, false = hide it
  const SHOW_PHONE = true;
  // ==================================================

  let currentLang = 'en';

  function toggleLang() {
    currentLang = currentLang === 'en' ? 'am' : 'en';
    document.querySelectorAll('[data-en]').forEach(el => {
      el.textContent = el.getAttribute('data-' + currentLang);
    });
    document.querySelectorAll('[data-en-ph]').forEach(el => {
      el.placeholder = el.getAttribute('data-' + currentLang + '-ph');
    });
    document.getElementById('langToggle').textContent = currentLang === 'en' ? 'አማ' : 'EN';
    document.documentElement.lang = currentLang;
  }

  // Apply email/phone settings
  document.getElementById('emailLine').innerHTML =
    document.getElementById('emailLine').textContent.replace(/\S+@\S+\.\S+/, '') +
    ' <strong>' + CONTACT_EMAIL + '</strong>';

  const phoneLine = document.getElementById('phoneLine');
  if (!SHOW_PHONE) {
    phoneLine.style.display = 'none';
  } else {
    const phonePrefix = { en: 'Call or message us on Telegram: ', am: 'ይደውሉልን ወይም በቴሌግራም ያግኙን፦ ' };
    phoneLine.innerHTML = phonePrefix[currentLang] + '<strong>' + CONTACT_PHONE + '</strong>';
    phoneLine.setAttribute('data-en', phonePrefix.en + CONTACT_PHONE);
    phoneLine.setAttribute('data-am', phonePrefix.am + CONTACT_PHONE);
  }

  // Hide language toggle if disabled
  if (!AMHARIC_ENABLED) {
    document.getElementById('langToggle').style.display = 'none';
  }

   // Contact form: opens the visitor's email app with a pre-filled message
  document.getElementById('contactForm').addEventListener('submit', function(e) {
    e.preventDefault();
    const name    = this.name.value;
    const email   = this.email.value;
    const message = this.message.value;
    const subject = encodeURIComponent('Inquiry from ' + name);
    const body    = encodeURIComponent('Name: ' + name + '\nEmail: ' + email + '\n\n' + message);
    window.location.href = 'mailto:' + CONTACT_EMAIL + '?subject=' + subject + '&body=' + body;
  });
</script>

</body>
</html>






