[etaleme_website.html](https://github.com/user-attachments/files/33664882/etaleme_website.html)
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Etaleme Solutions — Reusable Body Care, Made with Dignity</title>
<meta name="description" content="Affordable, skin-friendly, reusable body care alternatives for mothers, fistula patients, nursing mothers, and women across Addis Ababa and Sheger City.">
<style>
  :root {
    --primary: #1a5c4a;
    --accent:  #e8a13c;
    --olive:   #6b7a3a;
    --bg:      #faf7f2;
    --text:    #2b2b2b;
    --light:   #ffffff;
  }
  * { margin: 0; padding: 0; box-sizing: border-box; }
  body {
    font-family: 'Segoe UI', 'Noto Sans Ethiopic', system-ui, sans-serif;
    color: var(--text); background: var(--bg); line-height: 1.6;
  }
  .container { max-width: 1000px; margin: 0 auto; padding: 0 20px; }

  section { scroll-margin-top: 80px; }

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
  .lang-group { display: flex; gap: 6px; }
  .lang-btn {
    background: var(--primary); color: var(--light); border: none;
    padding: 8px 14px; border-radius: 20px; cursor: pointer; font-weight: 600;
    font-size: .85rem;
  }
  .lang-btn[aria-pressed="true"] { background: var(--olive); }

  header { padding: 80px 0 60px; text-align: center; position: relative; overflow: hidden; }
  header .wave-bg {
    position: absolute; inset: 0; z-index: -1;
    background: linear-gradient(180deg, #e8f2ee 0%, var(--bg) 70%);
  }
  header .wave-bg svg { position: absolute; bottom: -2px; left: 0; width: 100%; height: auto; }
  header .container { position: relative; z-index: 1; }
  header h1 { font-size: clamp(1.6rem, 5vw, 3rem); color: var(--primary); margin-bottom: 16px; }
  header p { max-width: 720px; margin: 0 auto; font-size: 1.15rem; color: #555; }
  .cta {
    display: inline-block; margin-top: 28px; padding: 14px 32px;
    background: var(--primary); color: var(--light);
    border-radius: 30px; text-decoration: none; font-weight: 600;
  }
  .cta:hover { background: #14453a; }

  .status-line {
    display: inline-block; margin-top: 18px; padding: 6px 16px;
    background: #fff3e0; color: #8a5a00; border-radius: 20px; font-size: .85rem; font-weight: 600;
  }

  .mission, .why { padding: 60px 0; }
  .mission h2, .why h2 { color: var(--primary); margin-bottom: 16px; font-size: 1.8rem; }
  .mission p, .why p { max-width: 760px; font-size: 1.05rem; color: #444; }
  .why { background: var(--light); }

  .products { padding: 60px 0; }
  .products h2 { color: var(--primary); text-align: center; margin-bottom: 40px; font-size: 1.8rem; }
  .grid { display: grid; gap: 24px; grid-template-columns: repeat(auto-fit, minmax(260px, 1fr)); }
  .card {
    background: var(--light); border-radius: 12px; padding: 28px;
    box-shadow: 0 2px 8px rgba(0,0,0,.06); border-top: 4px solid var(--accent);
  }
  .card.olive { border-top-color: var(--olive); }
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

  .faq { padding: 60px 0; background: var(--light); }
  .faq h2 { color: var(--primary); text-align: center; margin-bottom: 30px; font-size: 1.8rem; }
  .faq-item { max-width: 760px; margin: 0 auto 20px; }
  .faq-item h3 { color: var(--primary); font-size: 1.05rem; margin-bottom: 6px; }
  .faq-item p { color: #555; font-size: .95rem; }

  .contact { padding: 60px 0 80px; }
  .contact h2 { color: var(--primary); text-align: center; margin-bottom: 20px; font-size: 1.8rem; }
  .contact-ctas { display: flex; gap: 14px; justify-content: center; flex-wrap: wrap; margin-bottom: 36px; }
  .contact-ctas a {
    padding: 12px 24px; border-radius: 24px; text-decoration: none; font-weight: 600; font-size: .95rem;
  }
  .contact-ctas .inst { background: var(--olive); color: var(--light); }
  .contact-ctas .indiv { background: var(--accent); color: var(--text); }
  .chat-ctas { display: flex; gap: 14px; justify-content: center; flex-wrap: wrap; margin-bottom: 36px; }
  .chat-btn { padding: 12px 24px; border-radius: 24px; text-decoration: none; font-weight: 600; font-size: .95rem; color: var(--light); }
  .chat-btn.telegram { background: #1d8fcf; }
  .chat-btn.whatsapp { background: #1a9d4f; }
  .form-status { text-align: center; margin-top: 14px; font-weight: 600; color: var(--primary); display: none; }
  .form-status.visible { display: block; }
  .form-status.error { color: #b3261e; }
  form { max-width: 520px; margin: 0 auto; display: grid; gap: 16px; }
  label { font-size: .85rem; color: #555; font-weight: 600; margin-bottom: -10px; }
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
  .privacy-note { font-size: .8rem; color: #888; text-align: center; margin-top: 10px; }
  .email-alt { text-align: center; margin-top: 20px; color: #555; }
  .phone-line { text-align: center; margin-top: 8px; color: #555; }
  .phone-line a, .email-alt a { color: var(--primary); text-decoration: none; }

  footer { background: var(--primary); color: var(--light); text-align: center; padding: 24px 0; font-size: .9rem; }
</style>
</head>
<body>

<nav>
  <div class="container">
    <a href="#" class="logo">Etaleme Solutions</a>
    <div class="nav-right">
      <ul>
        <li><a href="#mission" data-en="Our Mission" data-am="የእኛ ተልዕኮ" data-om="Ergama Keenya">Our Mission</a></li>
        <li><a href="#products" data-en="Products" data-am="ዕቃዎች" data-om="Oomishaalee">Products</a></li>
        <li><a href="#faq" data-en="FAQ" data-am="ተደጋጋሚ ጥያቄዎች" data-om="Gaaffilee Yeroo Baay'ee Gaafataman">FAQ</a></li>
        <li><a href="#partners" data-en="Partners" data-am="አጋሮች" data-om="Michoottan">Partners</a></li>
        <li><a href="#contact" data-en="Contact" data-am="ያግኙን" data-om="Nu Qunnamaa">Contact</a></li>
      </ul>
      <div class="lang-group" id="langGroup" role="group" aria-label="Language selection">
        <button class="lang-btn" data-lang="en" aria-label="Switch to English" aria-pressed="true">EN</button>
        <button class="lang-btn" data-lang="am" aria-label="Switch to Amharic" aria-pressed="false">አማ</button>
        <button class="lang-btn" data-lang="om" aria-label="Switch to Afaan Oromo" aria-pressed="false">OR</button>
      </div>
    </div>
  </div>
</nav>

<header>
  <div class="wave-bg" aria-hidden="true">
    <svg viewBox="0 0 1440 220" preserveAspectRatio="none" xmlns="http://www.w3.org/2000/svg">
      <path d="M0,120 C240,200 480,40 720,100 C960,160 1200,60 1440,110 L1440,220 L0,220 Z" fill="var(--olive)" opacity="0.18"></path>
      <path d="M0,150 C240,90 480,190 720,140 C960,90 1200,170 1440,140 L1440,220 L0,220 Z" fill="var(--primary)" opacity="0.15"></path>
    </svg>
  </div>
  <div class="container">
    <h1 data-en="Etaleme Solutions — Reusable body care, made with dignity."
        data-am="እታለሜ ሶሉሽንስ — በክብር የተመሠረተ ዳግም የሚያገለግል የሰውነት እንክብካቤ።"
        data-om="Etaleme Solutions — Kunuunsa qaamaa deebi'ee itti fayyadamamu, ulfinaan hojjetame.">Etaleme Solutions — Reusable body care, made with dignity.</h1>
    <p data-en="Affordable, skin-friendly, reusable alternatives for mothers, fistula patients, nursing mothers, active adults, and women across Addis Ababa and Sheger City."
       data-am="በአዲስ አበባና በሸገር ከተማ ለእናቶች፣ ለፊስቱላ ታካሚዎች፣ ለጡት አጥባቢ እናቶች፣ ለንቁ አዋቂዎች እና ለሴቶች ተመጣጣኝ፣ ለቆዳ ተስማሚ እና ዳግም የሚውሉ አማራጮች።"
       data-om="Addis Ababaa fi Magaalaa Shaggar keessatti haadhotaaf, dhukkubsattoota fistulaaf, haadhota harma hoosisaniif, namoota jajjaboo fi dubartootaaf filannoo gatii madaalawaa, gogaaf mijataa fi deebi'anii itti fayyadamamu.">Affordable, skin-friendly, reusable alternatives for mothers, fistula patients, nursing mothers, active adults, and women across Addis Ababa and Sheger City.</p>
    <a href="#contact" class="cta" data-en="Get in Touch" data-am="ያግኙን" data-om="Nu Qunnamaa">Get in Touch</a>
    <div>
      <span class="status-line" data-en="Launching soon — join our early-access list" data-am="በቅርቡ ይጀምራል — ቀድሞ ተጠቃሚ ይሁኑ" data-om="Dhiyootti ni jalqabna — tarreeffama dursaa keessatti makamaa">Launching soon — join our early-access list</span>
    </div>
  </div>
</header>

<section class="mission" id="mission">
  <div class="container">
    <h2 data-en="Our Mission" data-am="የእኛ ተልዕኮ" data-om="Ergama Keenya">Our Mission</h2>
    <p data-en="Etaleme Solutions exists to solve real problems — the recurring cost of disposables, skin irritation from chemical exposure, the loss of dignity for fistula patients, and the environmental burden of single-use products. We provide affordable, skin-friendly, reusable alternatives that protect health, restore dignity, and reduce waste."
       data-am="እታለሜ ሶሉሽንስ ችግሮችን ለመፍታት ይኖራል — የአንድ ጊዜ መገልገያ ዕቃዎች ተደጋጋሚ ወጪ፣ ከኬሚካል ጋር በተገናኘ የቆዳ መቆጣት፣ የፊስቱላ ታካሚዎች የክብር መጓደል፣ እና የአንድ ጊዜ መገልገያ ዕቃዎች የአካባቢ ጫና። ጤናን የሚጠብቅ፣ ክብርን የሚመልስ እና ብክነትን የሚቀንስ ተመጣጣኝ እና ለቆዳ ተስማሚ፣ ዳግም የሚያገለግል አማራጮችን እናቀርባለን።"
       data-om="Etaleme Solutions rakkoolee dhugaa furuuf jira — baasii irra deddeebi'ee meeshaalee yeroo tokkoof oolan, miidhaa gogaa kan kemikaalaan dhufu, ulfina dhukkubsattoota fistulaa dhabamuu, akkasumas culaalaa naannoo meeshaalee yeroo tokkoof oolan. Filannoo gatii madaalawaa, gogaaf mijataa, deebi'anii itti fayyadamamu kan fayyaa eegu, ulfina deebisu, xurii immoo xiqqeessinu ni kenninaa.">Etaleme Solutions exists to solve real problems — the recurring cost of disposables, skin irritation from chemical exposure, the loss of dignity for fistula patients, and the environmental burden of single-use products. We provide affordable, skin-friendly, reusable alternatives that protect health, restore dignity, and reduce waste.</p>
  </div>
</section>

<section class="why" id="why">
  <div class="container">
    <h2 data-en="Why Reusable?" data-am="ለምን ዳግም የሚያገለግል?" data-om="Maaliif Deebi'anii Itti Fayyadamamu?">Why Reusable?</h2>
    <p data-en="Disposable products add up — financially and environmentally. A reusable pad or pair of shorts is washed and used again, cutting the ongoing cost to households and reducing the waste that single-use products leave behind. For patients managing fistula or heavy postpartum flow, reusable design also means not running out at the wrong moment."
       data-am="የአንድ ጊዜ መገልገያ ዕቃዎች ወጪያቸው ይጨምራል — በገንዘብም በአካባቢም። ዳግም የሚያገለግል ጨርቅ ወይም ቁምጣ ታጥቦ ደጋግሞ ስለሚያገለግል ለቤተሰብ ያለማቋረጥ ወጪን ይቀንሳል እንዲሁም የአንድ ጊዜ መገልገያ ዕቃዎች የሚተዉትን ቆሻሻ ይቀንሳል። ፊስቱላን ወይም ከፍተኛ የወሊድ በኋላ ፍሰትን ለሚያስተናግዱ ታካሚዎች፣ ዳግም የሚያገለግል ንድፍ በተሳሳተ ሰዓት እንዳያልቅባቸው ያግዛል።"
       data-om="Meeshaaleen yeroo tokkoof oolan baasii guddaa fida — maallaqaanis ta'e naannoodhaan. Bastrii ykn sureeffaa deebi'anii itti fayyadaman dhiqamanii irra deddeebi'anii waan fayyadamaniif, baasii maatiif yeroo hunda jiru ni xiqqeessu, xuriin meeshaalee yeroo tokkoof oolan hambisanis ni hir'isu. Dhukkubsattoota fistulaa ykn dhangala'aa da'umsaa booda guddaa qabaniif, dizaayinni deebi'anii itti fayyadamuu yeroo sirrii hin taaneen akka hin dhumne gargaara.">Disposable products add up — financially and environmentally. A reusable pad or pair of shorts is washed and used again, cutting the ongoing cost to households and reducing the waste that single-use products leave behind. For patients managing fistula or heavy postpartum flow, reusable design also means not running out at the wrong moment.</p>
  </div>
</section>

<section class="products" id="products">
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

<section class="faq" id="faq">
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

<section class="partners" id="partners">
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

<section class="contact" id="contact">
  <div class="container">
    <h2 data-en="Contact Us" data-am="ያግኙን" data-om="Nu Qunnamaa">Contact Us</h2>
    <div class="contact-ctas">
      <a href="#contactForm" class="inst" data-en="For Clinics & Organizations" data-am="ለክሊኒኮችና ድርጅቶች" data-om="Kiliinikaalee fi Dhaabbilleef">For Clinics & Organizations</a>
      <a href="#contactForm" class="indiv" data-en="For You" data-am="ለእርስዎ" data-om="Siif">For You</a>
    </div>
    <div class="chat-ctas" id="chatCtas">
      <a href="#" id="telegramBtn" class="chat-btn telegram" target="_blank" rel="noopener"
         data-en="Message us on Telegram" data-am="በቴሌግራም መልእክት ይላኩልን" data-om="Telegramiin nuuf barreessaa">Message us on Telegram</a>
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
  // Edit these values to configure the site — nothing else needs changing.

  // Enable/disable each language toggle independently.
  // true = selectable on the site, false = hidden entirely.
  const AMHARIC_ENABLED = true;
  const OROMO_ENABLED   = true;
  // English is always enabled and is the fallback language.

  // Your contact details (shown in the Contact section)
  const CONTACT_EMAIL = 'etalemesolutions@gmail.com';     // ← replace with your real email
  const CONTACT_PHONE_DISPLAY = '+251 723581334'; // ← shown to visitors
  const CONTACT_PHONE_TEL     = '+251723581334';    // ← used in the tel: link, digits only after +

  // Show the phone line?  true = yes, false = hide it
  const SHOW_PHONE = false;

  // Contact form (Formspree). Submissions are emailed to the address set up in your Formspree account.
  const FORMSPREE_ENDPOINT = 'https://formspree.io/f/xdeajvzr';

  // Instant-chat buttons. Both are OFF until you add your real details.
  // Fill in the username/number, then change false to true.
  const SHOW_TELEGRAM   = true;
  const TELEGRAM_USERNAME = 'Malefyae';   // without the @
  const SHOW_WHATSAPP   = true;
  const WHATSAPP_NUMBER = '251723581334';               // digits only: country code + number, no + or spaces
  const WHATSAPP_GREETING = "Hello, I'd like to know more about Etaleme's products.";
  // ==================================================

  const phoneTextByLang = {
    en: 'Call or message us on Telegram:',
    am: 'ይደውሉልን ወይም በቴሌግራም ያግኙን፦',
    om: 'Bilbilaa ykn Telegramiin nu qunnamaa:'
  };
  const emailTextByLang = {
    en: 'Or email us directly at',
    am: 'ወይም በቀጥታ ወደዚህ ኢሜይል ይላኩን',
    om: 'Yookiin kallattiin imeelii kanaan nu qunnamaa'
  };

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

  // Hide disabled language buttons
  if (!AMHARIC_ENABLED) {
    document.querySelector('.lang-btn[data-lang="am"]').style.display = 'none';
  }
  if (!OROMO_ENABLED) {
    document.querySelector('.lang-btn[data-lang="om"]').style.display = 'none';
  }

  // Apply contact settings (email/phone are in their own untranslated spans/links,
  // so the language switch no longer wipes them out)
  document.getElementById('emailLink').textContent = CONTACT_EMAIL;
  document.getElementById('emailLink').href = 'mailto:' + CONTACT_EMAIL;

  const phoneLine = document.getElementById('phoneLine');
  if (!SHOW_PHONE) {
    phoneLine.style.display = 'none';
  } else {
    document.getElementById('phoneLink').textContent = CONTACT_PHONE_DISPLAY;
    document.getElementById('phoneLink').href = 'tel:' + CONTACT_PHONE_TEL;
  }

  // Instant-chat buttons
  const telegramBtn = document.getElementById('telegramBtn');
  const whatsappBtn = document.getElementById('whatsappBtn');
  telegramBtn.href = 'https://t.me/' + TELEGRAM_USERNAME;
  whatsappBtn.href = 'https://wa.me/' + WHATSAPP_NUMBER + '?text=' + encodeURIComponent(WHATSAPP_GREETING);
  if (!SHOW_TELEGRAM) telegramBtn.style.display = 'none';
  if (!SHOW_WHATSAPP) whatsappBtn.style.display = 'none';
  if (!SHOW_TELEGRAM && !SHOW_WHATSAPP) document.getElementById('chatCtas').style.display = 'none';

  // Contact form: sends in the background via Formspree and shows a message on the page
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
