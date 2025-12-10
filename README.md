<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>RP Crispy & Grills Foods — Catering & Live Restaurant</title>
<style>

  .custom-wrap {
    display: grid;
    grid-template-columns: 1fr 360px; /* left column flexible, right column fixed */
    gap: 18px;
}
@media(max-width:980px){
    .custom-wrap { grid-template-columns:1fr } /* stack on small screens */
}

:root{
  --brand:#b30000; --accent:#ff9900; --bg:#fff5e6; --card:#fff;
  --glass: rgba(255,255,255,0.6);
}
*{box-sizing:border-box;font-family:Arial,Helvetica,sans-serif}
body{margin:0;background:linear-gradient(180deg,#fff8ef 0%, #fff5e6 100%);color:#222; -webkit-font-smoothing:antialiased}
.header{background:var(--brand);color:#fff;padding:14px 18px;position:sticky;top:0;z-index:50}
.container{max-width:1100px;margin:0 auto;padding:16px}
.header .wrap{display:flex;align-items:center;justify-content:space-between;gap:12px;flex-wrap:wrap}
.header h1{font-size:20px;margin:0;font-weight:700}
.nav{display:flex;gap:10px;flex-wrap:wrap}
.nav button{background:transparent;border:0;color:#fff;font-weight:600;padding:8px 10px;border-radius:8px;cursor:pointer;opacity:0.95}
.nav button:hover{background:rgba(255,255,255,0.08)}
.hero{display:flex;gap:20px;align-items:center;padding:28px 0;flex-wrap:wrap}
.hero-left{flex:1;min-width:260px}
.hero h2{color:var(--brand);font-size:28px;margin:0 0 8px}
.lead{color:#444;margin-bottom:12px}
.hero .actions{display:flex;gap:10px;flex-wrap:wrap}
.btn{background:var(--accent);border:0;padding:10px 14px;border-radius:10px;color:#fff;font-weight:700;cursor:pointer;box-shadow:0 6px 14px rgba(0,0,0,0.08);transition:transform .18s}
.btn:hover{transform:translateY(-3px)}
.btn.secondary{background:var(--brand)}
.hero-img{width:420px;max-width:45%;border-radius:14px;box-shadow:0 18px 40px rgba(0,0,0,0.12);border:6px solid rgba(255,255,255,0.5)}

/* layout sections */
section{display:none;padding:22px 0;animation:fadeIn .45s ease both}
section.active{display:block}
@keyframes fadeIn{from{opacity:0;transform:translateY(6px)}to{opacity:1;transform:none}}

/* grid */
.grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:16px}

/* card */
.card{background:var(--card);padding:12px;border-radius:12px;box-shadow:0 10px 24px rgba(0,0,0,0.06);text-align:center;transition:transform .18s, box-shadow .18s}
.card:hover{transform:translateY(-6px); box-shadow:0 20px 40px rgba(0,0,0,0.12)}
.card img{width:100%;aspect-ratio:1/1;object-fit:cover;border-radius:8px}
.card h4{color:var(--brand);margin:10px 0 6px}
.card p{color:#333;margin:0}

/* customize UI */
.custom-wrap{display:grid;grid-template-columns:1fr 360px;gap:18px}
@media(max-width:980px){.custom-wrap{grid-template-columns:1fr}}
.panel{background:var(--card);padding:12px;border-radius:12px;box-shadow:0 8px 20px rgba(0,0,0,0.06)}
.item-row{display:flex;align-items:center;gap:10px;padding:8px;border-radius:8px}
.item-row label{flex:1;cursor:pointer}
.qty{width:64px;padding:6px;border-radius:8px;border:1px solid #ddd;text-align:center}
.small{font-size:13px;color:#666}
.summary ul{list-style:none;padding-left:0;margin:8px 0}

/* delivery */
.delivery-grid{display:flex;gap:18px;flex-wrap:wrap;align-items:center;justify-content:center}
.delivery-grid .d{width:120px;text-align:center}
.delivery-grid img{width:100%;border-radius:10px;box-shadow:0 8px 18px rgba(0,0,0,0.08);cursor:pointer;transition:transform .15s}
.delivery-grid img:hover{transform:translateY(-6px)}

/* QR modal */
.modal{position:fixed;left:0;top:0;width:100%;height:100%;display:flex;align-items:center;justify-content:center;background:rgba(0,0,0,0.45);z-index:100;opacity:0;pointer-events:none;transition:opacity .18s}
.modal.show{opacity:1;pointer-events:auto}
.modal .box{background:#fff;padding:18px;border-radius:12px;max-width:420px;width:92%;text-align:center}
.qr{width:260px;height:260px;margin:10px auto 8px;background:#f5f5f5;display:flex;align-items:center;justify-content:center;border-radius:4px;box-shadow:inset 0 0 8px rgba(0,0,0,0.04)}
.close{background:transparent;border:0;color:#333;margin-top:8px;padding:8px 10px;cursor:pointer}

/* footer */
.footer{background:var(--brand);color:#fff;padding:14px;text-align:center;margin-top:18px}

/* micro animations */
.fade-up{animation:fadeUp .6s ease both}
@keyframes fadeUp{from{opacity:0;transform:translateY(8px)}to{opacity:1;transform:none}}

/* small screens */
@media(max-width:720px){
  .hero-img{width:100%}
  .hero{padding:8px 0}
  .header .wrap{flex-direction:column;align-items:flex-start}
}

.slider {
    width: 380px;
    height: 330px;
    position: relative;
    overflow: hidden;
    border-radius: 15px;
    box-shadow: 0 0 12px rgba(0,0,0,0.3);
}

.slide {
    width: 100%;
    height: 100%;
    object-fit: cover;
    position: absolute;
    opacity: 0;
    transition: opacity 1s ease-in-out;
}

.slide.active {
    opacity: 1;
}

.event-container {
  display: flex;
  align-items: flex-start;
  gap: 25px;
}

.event-container {
  display: flex;
  align-items: flex-start;
  gap: 40px;
}

.event-list li {
  list-style: disc;
  margin-bottom: 8px;
  cursor: pointer;
  font-size: 18px;
}

.event-list li.active {
  color: red;
  font-weight: bold;
}

.event-image-box img {
  width: 400px;
  border-radius: 10px;
}


</style>
</head>
<body>
<!-- Add this at the top of your <body> -->
<div id="loginOverlay" style="
  position:fixed;
  top:0; left:0;
  width:100%; height:100%;
  background:rgba(0,0,0,0.85);
  display:flex;
  justify-content:center;
  align-items:center;
  z-index:9999;
  flex-direction:column;
  color:#fff;
  font-family:Arial, sans-serif;
">
  <div style="
    background:#fff;
    color:#333;
    padding:30px 40px;
    border-radius:20px;
    text-align:center;
    min-width:300px;
    box-shadow:0 20px 50px rgba(0,0,0,0.3);
  ">
    <h2 style="color:#b30000;">Crispy & Grills Login</h2>
    <input type="text" id="loginUser" placeholder="Username" style="width:100%;padding:10px;margin:10px 0;border-radius:10px;border:1px solid #ccc;">
    <input type="password" id="loginPass" placeholder="Password" style="width:100%;padding:10px;margin:10px 0;border-radius:10px;border:1px solid #ccc;">
    <button id="loginBtn" style="width:100%;padding:10px;background:#b30000;color:#fff;border:none;border-radius:10px;cursor:pointer;margin-top:10px;">Login</button>
    <p style="margin:15px 0;color:#444;">or</p>
    <button id="googleLoginBtn" style="width:100%;padding:10px;background:#4285F4;color:#fff;border:none;border-radius:10px;cursor:pointer;">Login with Google</button>
    <p style="font-size:12px;color:#666;margin-top:10px;">Demo login: username: <b>admin</b>, password: <b>1234</b></p>
  </div>
</div>


<!-- HEADER -->
<header class="header">
  <div class="container wrap">
    <h1>RP Crispy & Grills Foods</h1>
    <nav class="nav" role="navigation" aria-label="main navigation">
      <button onclick="show('home')">Home</button>
      <button onclick="show('menu')">Menu</button>
      <button onclick="show('custom')">Customize Thali</button>
      <button onclick="show('delivery')">Delivery</button>
      <button onclick="show('events')">Events</button>
      <button onclick="show('contact')">Contact</button>
    </nav>
  </div>
</header>

<!-- MAIN -->
<main class="container">
  <!-- HOME -->
  <section id="home" class="active">
    <div class="hero">
      <div class="hero-left">
        <h2>We cater events & run a live restaurant — order via QR on table or delivery partners</h2>
        <p class="lead">Homestyle freshness, crispy bites and perfectly grilled specials. Catering for weddings, parties, corporate events & more.</p>
        <div class="actions">
          <button class="btn" onclick="show('menu')">View Menu</button>
          <button class="btn secondary" onclick="show('custom')">Customize Thali</button>
          <button class="btn" onclick="openQR()">Show Table QR</button>
        </div>
        <p class="small" style="margin-top:10px">At table: scan QR code — open this site on phone → choose items → confirm to order from table.</p>
      </div>
      <div class="slider">
    <img src="11.jpg" class="slide active">
    <img src="pun.jpg" class="slide">
    <img src="rasgulla.jpg" class="slide">
    <img src="brownie.webp" class="slide">

  
</div>

    </div>
  </section>

  <!-- MENU -->
  <section id="menu">
    <h2>Menu — Thalis & Extra Items</h2>
    <p class="lead">Pick main thalis or individual items. You can customize a thali in the "Customize Thali" tab.</p>

    <h3 style="color:var(--brand);margin-top:12px">Thalis</h3>
    <div class="grid">
      <div class="card"><img src="11.jpg" alt=""><h4>Gujarati Thali</h4><p>Rotli, Kadhi, Undhiyu, Mix Veg, Khichdi</p><p class="small">Base ₹250</p></div>
      <div class="card"><img src="pun.jpg" alt=""><h4>Punjabi Thali</h4><p>Paneer Sabji, Dal Makhani, Naan, Jeera Rice</p><p class="small">Base ₹300</p></div>
      <div class="card"><img src="fix.jpg" alt=""><h4>Special Thali</h4><p>Sabji + Rotli + Dal/Kadhi + Rice + Salad + Sweet</p><p class="small">Base ₹350</p></div>
    </div>

    <h3 style="color:var(--brand);margin-top:18px">Extra Items</h3>
    <div class="grid">
      <!-- list each item card (names only, price shown) -->
      <div class="card"><img src="mvc.jpg" alt=""><h4>Sabji (Vegetable Curry)</h4><p class="small">₹120</p></div>
      <div class="card"><img src="roti.jpg" alt=""><h4>Rotli / Roti</h4><p class="small">₹15</p></div>
      <div class="card"><img src="dk.jpg" alt=""><h4>Dal / Kadhi</h4><p class="small">₹80</p></div>
      <div class="card"><img src="rice.jpg" alt=""><h4>Rice</h4><p class="small">₹60</p></div>
      <div class="card"><img src="salad.jpg" alt=""><h4>Salad</h4><p class="small">₹40</p></div>
      <div class="card"><img src="sweet.jpg" alt=""><h4>Sweet</h4><p class="small">₹50</p></div>
      <div class="card"><img src="paneer.jpg" alt=""><h4>Paneer Sabji</h4><p class="small">₹150</p></div>
      <div class="card"><img src="dalmakhani.jpg" alt=""><h4>Dal Makhani</h4><p class="small">₹140</p></div>
      <div class="card"><img src="naan.jpg" alt=""><h4>Naan</h4><p class="small">₹20</p></div>
      <div class="card"><img src="jeerarice.jpg" alt=""><h4>Jeera Rice</h4><p class="small">₹80</p></div>
      <div class="card"><img src="chapati.jpg" alt=""><h4>Chapati</h4><p class="small">₹15</p></div>
      <div class="card"><img src="undhiyu.jpg" alt=""><h4>Undhiyu (Mixed Veg)</h4><p class="small">₹160</p></div>
      <div class="card"><img src="mixveg.jpg" alt=""><h4>Mix Veg</h4><p class="small">₹120</p></div>

      <!-- Extra fast food -->
      <div class="card"><img src="pizza.jpg" alt=""><h4>Pizza</h4><p class="small">₹180</p></div>
      <div class="card"><img src="dosa.jpg" alt=""><h4>Dosa</h4><p class="small">₹120</p></div>
      <div class="card"><img src="pp.jpg" alt=""><h4>Pani Puri</h4><p class="small">₹50</p></div>
      <div class="card"><img src="sandwich.jpg" alt=""><h4>Sandwich</h4><p class="small">₹70</p></div>
      <div class="card"><img src="chaat.jpg" alt=""><h4>Chaat</h4><p class="small">₹60</p></div>
    </div>
      <h3 style="color:var(--brand);margin-top:18px">Fast Food</h3>
<div class="grid">
  <!-- Vada Pav -->
  <div class="card"><img src="vadapav.jpg" alt=""><h4>Cheese Vadapav</h4><p class="small">₹40</p></div>
  <div class="card"><img src="butter.jpg" alt=""><h4>Butter Vadapav</h4><p class="small">₹35</p></div>
  <div class="card"><img src="masala.jpg" alt=""><h4>Cheese Masala Vadapav</h4><p class="small">₹50</p></div>
  <div class="card"><img src="plain.jpg" alt=""><h4>Plain Vadapav</h4><p class="small">₹30</p></div>

  <!-- Frankie -->
  <div class="card"><img src="c frankie.jpg" alt=""><h4>Veg Cheese Frankie</h4><p class="small">₹60</p></div>
  <div class="card"><img src="m frankie.jpg" alt=""><h4>Mayonnaise Frankie</h4><p class="small">₹55</p></div>
  <div class="card"><img src="k frankie.jpg" alt=""><h4>Kurkure Frankie</h4><p class="small">₹50</p></div>
  <div class="card"><img src="p frankie.jpg" alt=""><h4>Paneer Frankie</h4><p class="small">₹70</p></div>

  <!-- Burger -->
  <div class="card"><img src="v burger.jpg" alt=""><h4>Veg Cheese Burger</h4><p class="small">₹80</p></div>
  <div class="card"><img src="t burger.jpg" alt=""><h4>Tandoori Mayo Burger</h4><p class="small">₹90</p></div>
  <div class="card"><img src="c burger.jpg" alt=""><h4>Chicken Burger</h4><p class="small">₹100</p></div>

  <!-- French Fries -->
  <div class="card"><img src="s fries.jpg" alt=""><h4>Salted Fries</h4><p class="small">₹40</p></div>
  <div class="card"><img src="pp fries.jpg" alt=""><h4>Peri Peri Fries</h4><p class="small">₹50</p></div>
  <div class="card"><img src="cc fries.jpg" alt=""><h4>Cheese Fries</h4><p class="small">₹60</p></div>
</div>

    <h3 style="color:var(--brand);margin-top:18px">Cold Drinks</h3>
    <div class="grid">
      <div class="card"><img src="cola.jpg" alt=""><h4>Coca-Cola</h4><p class="small">₹40</p></div>
      <div class="card"><img src="sprite.jpeg" alt=""><h4>Sprite</h4><p class="small">₹40</p></div>
      <div class="card"><img src="lemon.jpg" alt=""><h4>Lemon Soda</h4><p class="small">₹50</p></div>
      <div class="card"><img src="chaas.jpg" alt=""><h4>Masala Chaas</h4><p class="small">₹35</p></div>
      <div class="card"><img src="coldcoffee.jpg" alt=""><h4>Cold Coffee</h4><p class="small">₹70</p></div>
    </div>

    <h3 style="color:var(--brand);margin-top:18px">Sweets & Desserts</h3>
    <div class="grid">
      <div class="card"><img src="gulab.jpg" alt=""><h4>Gulab Jamun</h4><p class="small">₹50</p></div>
      <div class="card"><img src="jalebi.jpeg" alt=""><h4>Jalebi</h4><p class="small">₹60</p></div>
      <div class="card"><img src="rasgulla.jpg" alt=""><h4>Rasgulla</h4><p class="small">₹55</p></div>
      <div class="card"><img src="basundi.jpg" alt=""><h4>Basundi</h4><p class="small">₹70</p></div>
      <div class="card"><img src="shrikandh.jpg" alt=""><h4>Shrikhand</h4><p class="small">₹65</p></div>

      <div class="card"><img src="sundae.jpg" alt=""><h4>Ice-Cream Sundae</h4><p class="small">₹90</p></div>
      <div class="card"><img src="brownie.webp" alt=""><h4>Chocolate Brownie</h4><p class="small">₹120</p></div>
      <div class="card"><img src="kulfie.jpg" alt=""><h4>Kesar Kulfi</h4><p class="small">₹110</p></div>
    </div>
    

  </section>

  <!-- CUSTOMIZE -->
  <section id="custom">
    <h2>Customize Your Thali</h2>
    <p class="lead">Choose a base thali and add any items with quantity. Total updates automatically.</p>

    <div class="custom-wrap">
      <div class="panel">
        <div style="margin-bottom:10px"><strong>Base Thali (choose one)</strong></div>
        <div class="item-row"><input type="radio" name="base" id="b_guj" data-price="250"><label for="b_guj">Gujarati Thali — ₹250</label></div>
        <div class="item-row"><input type="radio" name="base" id="b_pun" data-price="300"><label for="b_pun">Punjabi Thali — ₹300</label></div>
        <div class="item-row"><input type="radio" name="base" id="b_sp" data-price="350"><label for="b_sp">Special Thali — ₹350</label></div>

        <hr style="margin:10px 0">

        <div style="margin-bottom:8px"><strong>Extra Items (check + set qty)</strong></div>

        <!-- extras - each row has checkbox, label, qty -->
        <div class="item-row"><input class="ex" id="ex_sabji" data-price="120" type="checkbox"><label for="ex_sabji">Sabji (Vegetable Curry) — ₹120</label><input type="number" class="qty" id="q_sabji" min="1" value="1" disabled></div>

        <div class="item-row"><input class="ex" id="ex_rotli" data-price="15" type="checkbox"><label for="ex_rotli">Rotli / Roti — ₹15</label><input type="number" class="qty" id="q_rotli" min="1" value="1" disabled></div>

        <div class="item-row"><input class="ex" id="ex_dal" data-price="80" type="checkbox"><label for="ex_dal">Dal / Kadhi — ₹80</label><input type="number" class="qty" id="q_dal" min="1" value="1" disabled></div>

        <div class="item-row"><input class="ex" id="ex_rice" data-price="60" type="checkbox"><label for="ex_rice">Rice — ₹60</label><input type="number" class="qty" id="q_rice" min="1" value="1" disabled></div>

        <div class="item-row"><input class="ex" id="ex_salad" data-price="40" type="checkbox"><label for="ex_salad">Salad — ₹40</label><input type="number" class="qty" id="q_salad" min="1" value="1" disabled></div>

        <div class="item-row"><input class="ex" id="ex_sweet" data-price="50" type="checkbox"><label for="ex_sweet">Sweet — ₹50</label><input type="number" class="qty" id="q_sweet" min="1" value="1" disabled></div>

        <div class="item-row"><input class="ex" id="ex_paneer" data-price="150" type="checkbox"><label for="ex_paneer">Paneer Sabji — ₹150</label><input type="number" class="qty" id="q_paneer" min="1" value="1" disabled></div>

        <div class="item-row"><input class="ex" id="ex_dalmak" data-price="140" type="checkbox"><label for="ex_dalmak">Dal Makhani — ₹140</label><input type="number" class="qty" id="q_dalmak" min="1" value="1" disabled></div>

        <div class="item-row"><input class="ex" id="ex_naan" data-price="20" type="checkbox"><label for="ex_naan">Naan — ₹20</label><input type="number" class="qty" id="q_naan" min="1" value="1" disabled></div>

        <div class="item-row"><input class="ex" id="ex_jeera" data-price="80" type="checkbox"><label for="ex_jeera">Jeera Rice — ₹80</label><input type="number" class="qty" id="q_jeera" min="1" value="1" disabled></div>

        <div class="item-row"><input class="ex" id="ex_chap" data-price="15" type="checkbox"><label for="ex_chap">Chapati — ₹15</label><input type="number" class="qty" id="q_chap" min="1" value="1" disabled></div>

        <div class="item-row"><input class="ex" id="ex_und" data-price="160" type="checkbox"><label for="ex_und">Undhiyu — ₹160</label><input type="number" class="qty" id="q_und" min="1" value="1" disabled></div>

        <div class="item-row"><input class="ex" id="ex_mix" data-price="120" type="checkbox"><label for="ex_mix">Mix Veg — ₹120</label><input type="number" class="qty" id="q_mix" min="1" value="1" disabled></div>
        <hr style="margin:10px 0">
<div style="margin-bottom:8px"><strong>Fast Food (choose items)</strong></div>

<div class="item-row"><input class="ex" id="ex_vadapav_cheese" data-price="40" type="checkbox"><label for="ex_vadapav_cheese">Cheese Vadapav — ₹40</label><input type="number" class="qty" id="q_vadapav_cheese" min="1" value="1" disabled></div>
<div class="item-row"><input class="ex" id="ex_vadapav_butter" data-price="35" type="checkbox"><label for="ex_vadapav_butter">Butter Vadapav — ₹35</label><input type="number" class="qty" id="q_vadapav_butter" min="1" value="1" disabled></div>
<div class="item-row"><input class="ex" id="ex_vadapav_cheese_masala" data-price="50" type="checkbox"><label for="ex_vadapav_cheese_masala">Cheese Masala Vadapav — ₹50</label><input type="number" class="qty" id="q_vadapav_cheese_masala" min="1" value="1" disabled></div>
<div class="item-row"><input class="ex" id="ex_vadapav_plain" data-price="30" type="checkbox"><label for="ex_vadapav_plain">Plain Vadapav — ₹30</label><input type="number" class="qty" id="q_vadapav_plain" min="1" value="1" disabled></div>

<div class="item-row"><input class="ex" id="ex_frankie_veg_cheese" data-price="60" type="checkbox"><label for="ex_frankie_veg_cheese">Veg Cheese Frankie — ₹60</label><input type="number" class="qty" id="q_frankie_veg_cheese" min="1" value="1" disabled></div>
<div class="item-row"><input class="ex" id="ex_frankie_mayo" data-price="55" type="checkbox"><label for="ex_frankie_mayo">Mayonnaise Frankie — ₹55</label><input type="number" class="qty" id="q_frankie_mayo" min="1" value="1" disabled></div>
<div class="item-row"><input class="ex" id="ex_frankie_kurkure" data-price="50" type="checkbox"><label for="ex_frankie_kurkure">Kurkure Frankie — ₹50</label><input type="number" class="qty" id="q_frankie_kurkure" min="1" value="1" disabled></div>
<div class="item-row"><input class="ex" id="ex_frankie_paneer" data-price="70" type="checkbox"><label for="ex_frankie_paneer">Paneer Frankie — ₹70</label><input type="number" class="qty" id="q_frankie_paneer" min="1" value="1" disabled></div>

<div class="item-row"><input class="ex" id="ex_burger_veg_cheese" data-price="80" type="checkbox"><label for="ex_burger_veg_cheese">Veg Cheese Burger — ₹80</label><input type="number" class="qty" id="q_burger_veg_cheese" min="1" value="1" disabled></div>
<div class="item-row"><input class="ex" id="ex_burger_tandoori" data-price="90" type="checkbox"><label for="ex_burger_tandoori">Tandoori Mayo Burger — ₹90</label><input type="number" class="qty" id="q_burger_tandoori" min="1" value="1" disabled></div>
<div class="item-row"><input class="ex" id="ex_burger_chicken" data-price="100" type="checkbox"><label for="ex_burger_chicken">Chicken Burger — ₹100</label><input type="number" class="qty" id="q_burger_chicken" min="1" value="1" disabled></div>

<div class="item-row"><input class="ex" id="ex_fries_salted" data-price="40" type="checkbox"><label for="ex_fries_salted">Salted Fries — ₹40</label><input type="number" class="qty" id="q_fries_salted" min="1" value="1" disabled></div>
<div class="item-row"><input class="ex" id="ex_fries_peri" data-price="50" type="checkbox"><label for="ex_fries_peri">Peri Peri Fries — ₹50</label><input type="number" class="qty" id="q_fries_peri" min="1" value="1" disabled></div>
<div class="item-row"><input class="ex" id="ex_fries_cheese" data-price="60" type="checkbox"><label for="ex_fries_cheese">Cheese Fries — ₹60</label><input type="number" class="qty" id="q_fries_cheese" min="1" value="1" disabled></div>

        <hr style="margin:10px 0">
        <div style="margin-top:8px"><strong>Cold Drinks</strong></div>
        <div class="item-row"><input class="ex" id="ex_cola" data-price="40" type="checkbox"><label for="ex_cola">Coca-Cola — ₹40</label><input type="number" class="qty" id="q_cola" min="1" value="1" disabled></div>
        <div class="item-row"><input class="ex" id="ex_sprite" data-price="40" type="checkbox"><label for="ex_sprite">Sprite — ₹40</label><input type="number" class="qty" id="q_sprite" min="1" value="1" disabled></div>
        <div class="item-row"><input class="ex" id="ex_lemon" data-price="50" type="checkbox"><label for="ex_lemon">Lemon Soda — ₹50</label><input type="number" class="qty" id="q_lemon" min="1" value="1" disabled></div>
        <div class="item-row"><input class="ex" id="ex_chaas" data-price="35" type="checkbox"><label for="ex_chaas">Masala Chaas — ₹35</label><input type="number" class="qty" id="q_chaas" min="1" value="1" disabled></div>
        <div class="item-row"><input class="ex" id="ex_coldc" data-price="70" type="checkbox"><label for="ex_coldc">Cold Coffee — ₹70</label><input type="number" class="qty" id="q_coldc" min="1" value="1" disabled></div>
      </div>
        
      <div class="panel summary">
        <h4>Your Selection</h4>
        <div id="selList"><p class="small">No items selected yet.</p></div>
        <hr style="margin:10px 0">
        <p><strong>Grand Total: ₹<span id="grand">0</span></strong></p>
        <div style="display:flex;gap:8px;margin-top:12px">
          <button class="btn" onclick="confirmOrder()">Confirm</button>
          <button class="btn secondary" onclick="clearCustom()">Clear</button>
          <button class="btn" onclick="copySummary()">Copy</button>
        </div>
        <p class="small" style="margin-top:8px">After confirm you can choose Delivery option to place order.</p>
      </div>
    </div>
  </section>

  <!-- DELIVERY -->
  <section id="delivery">
    <h2>Delivery Options</h2>
    <p class="lead">Choose how you'd like to receive your order.</p>

    <div class="delivery-grid">
      <div class="d"><img src="swiggy.png" alt="swiggy" onclick="openDelivery('swiggy')"><div class="small">Swiggy</div></div>
      <div class="d"><img src="zomato.jpg" alt="zomato" onclick="openDelivery('zomato')"><div class="small">Zomato</div></div>
      <div class="d"><img src="self.webp" alt="pickup" onclick="openDelivery('pickup')"><div class="small">Self Pickup</div></div>
      <div class="d"><img src="we deliver.jpg" alt="we delivers" onclick="openDelivery('wedelivers')"><div class="small">WE DELIVERS</div></div>
    </div>

    <div id="deliveryFormContainer" style="margin-top:16px"></div>
  </section>

  <!-- EVENTS -->
  
<!-- EVENTS -->
<section id="events">
  <h2>We Serve For</h2>

  <!-- clickable list -->
  <ul class="event-list">
  <li onclick="changeEvent('event1.webp', this)">Wedding Catering</li>
  <li onclick="changeEvent('ev2.png', this)">Ring Ceremony</li>
  <li onclick="changeEvent('ev3.png', this)">Birthday Party</li>
  <li onclick="changeEvent('ev4.png', this)">Corporate Events</li>
  <li onclick="changeEvent('ev5.png', this)">Festival Catering</li>
  <li onclick="changeEvent('ev6.png', this)">Baby Shower / Housewarming</li>
</ul>
<div class="event-image-box">
  <img id="eventDisplay" src="event1.webp" alt="">
</div>


</section>



  <!-- CONTACT -->
  <section id="contact">
    <h2>Contact & Booking</h2>
    <p class="small"><strong>Call / WhatsApp:</strong> +91 8866506326 OR 9875112820</p>
    <p class="small"><strong>Email:</strong> princerabari68@gmail.com OR vaghelarudra074@gmail.com</p>
    <p class="small"><strong>Location:</strong> Vadodara, Gujarat</p>
  </section>
</main>

<footer class="footer">© 2025 RP Crispy & Grills Foods — All Rights Reserved</footer>

<!-- QR Modal -->
<div id="qrModal" class="modal" role="dialog" aria-hidden="true">
  <div class="box">
    <h3>Table QR Code (Scan to Order)</h3>
    <div class="qr" id="qrBox">
      <!-- placeholder; replace with actual QR image 'qr.png' or integrate QR generator -->
      <img src="qr.png" alt="QR code" style="max-width:100%;height:auto">
    </div>
    <p class="small">Scan the QR on your phone to open the menu and place a table order.</p>
    <button class="close" onclick="closeQR()">Close</button>
  </div>
</div>

<script>
/* Simple SPA show */
function show(id){
  document.querySelectorAll('main section').forEach(s=>s.classList.remove('active'));
  document.getElementById(id).classList.add('active');
  window.scrollTo({top:0,behavior:'smooth'});
}

/* QR modal */
function openQR(){ document.getElementById('qrModal').classList.add('show'); document.getElementById('qrModal').ariaHidden = 'false' }
function closeQR(){ document.getElementById('qrModal').classList.remove('show'); document.getElementById('qrModal').ariaHidden = 'true' }

/* CUSTOMIZE THALI logic */
const extras = Array.from(document.querySelectorAll('.ex'));
extras.forEach(ch => {
  ch.addEventListener('change', ()=> {
    const q = document.getElementById('q_' + ch.id.replace('ex_',''));
    if(q){ q.disabled = !ch.checked; if(!ch.checked) q.value = 1; }
    updateCustom();
  });
});
document.querySelectorAll('.qty').forEach(q=> q.addEventListener('input', updateCustom));
document.querySelectorAll('input[name="base"]').forEach(r=> r.addEventListener('change', updateCustom));

function updateCustom(){
  const sel = [];
  let total = 0;
  // base
  const base = document.querySelector('input[name="base"]:checked');
  if(base){
    const price = parseInt(base.dataset.price);
    sel.push(`${base.id.replace('b_','').toUpperCase()} Thali — ₹${price}`);
    total += price;
  }
  // extras
  extras.forEach(ch => {
    if(ch.checked){
      const price = parseInt(ch.dataset.price || 0);
      const key = ch.id.replace('ex_','');
      const qty = parseInt(document.getElementById('q_' + key).value)||0;
      const subtotal = price * qty;
      const label = ch.nextElementSibling ? ch.nextElementSibling.textContent : key;
      sel.push(`${label.trim()} × ${qty} — ₹${subtotal}`);
      total += subtotal;
    }
  });
  const list = document.getElementById('selList');
  if(sel.length===0) list.innerHTML = '<p class="small">No items selected yet.</p>'; else list.innerHTML = `<ul>${sel.map(i=>'<li>'+i+'</li>').join('')}</ul>`;
  document.getElementById('grand').textContent = total;
}

/* clear and confirm */
function clearCustom(){
  document.querySelectorAll('input[name="base"]').forEach(r=>r.checked=false);
  extras.forEach(ch => { ch.checked=false; const q = document.getElementById('q_' + ch.id.replace('ex_','')); if(q){ q.disabled=true; q.value=1 }});
  updateCustom();
}
function confirmOrder(){
  const base = document.querySelector('input[name="base"]:checked');
  if(!base){ alert('Please select a base thali first.'); show('custom'); return; }
  const total = document.getElementById('grand').textContent;
  let msg = `Customized Thali order:\nBase: ${base.id.replace('b_','')} Thali — ₹${base.dataset.price}\n`;
  const lis = document.querySelectorAll('#selList ul li');
  if(lis.length) { msg += 'Items:\n'; lis.forEach(li => msg += '- '+li.textContent + '\n') }
  msg += `\nGrand Total: ₹${total}`;
  alert(msg);
}

/* copy summary */
function copySummary(){
  const text = document.querySelector('#selList').innerText + '\nTotal: ₹' + document.getElementById('grand').textContent;
  navigator.clipboard?.writeText(text).then(()=> alert('Summary copied to clipboard.'));
}

/* DELIVERY handlers (Swiggy, Zomato, pickup, wedelivers) */
function openDelivery(opt){
  const cont = document.getElementById('deliveryFormContainer');
  if(opt === 'pickup'){
    cont.innerHTML = `<div class="panel"><h3>Self Pickup</h3><p>Pickup at: Out Catrus Restaurant<br>Near GSFC University, Vadodara<br>Contact: 9876543210</p></div>`;
    window.scrollTo({top:cont.offsetTop-20,behavior:'smooth'}); return;
  }
  cont.innerHTML = `<div class="panel"><h3>${opt.toUpperCase()} Order</h3>
    <label>Name</label><input id="d_name" placeholder="Full name">
    <label>Mobile</label><input id="d_mobile" placeholder="Mobile number">
    <label>Address</label><textarea id="d_addr" placeholder="Full delivery address"></textarea>
    <label>State</label>
    <select id="d_state" onchange="calcCharge()"><option value="">Select State</option><option value="Gujarat">Gujarat</option><option value="Other">Other</option></select>
    <p id="d_charge" class="small">Select state to calculate delivery charge</p>
    <div style="display:flex;gap:8px;margin-top:8px">
      <button class="btn" onclick="submitDelivery('${opt}')">Submit</button>
      <button class="btn secondary" onclick="sendWhatsAppOrder('${opt}')">WhatsApp Order</button>
    </div></div>`;
  window.scrollTo({top:cont.offsetTop-20,behavior:'smooth'});
}

function calcCharge(){
  const st = document.getElementById('d_state').value;
  const el = document.getElementById('d_charge');
  if(st === 'Gujarat'){ el.textContent = 'Delivery charge: ₹40 (Inside Gujarat)'; el.dataset.charge = 40; }
  else if(st === 'Other'){ el.textContent = 'Delivery charge: ₹120 (Outside Gujarat)'; el.dataset.charge = 120; }
  else { el.textContent = 'Select state to calculate delivery charge'; delete el.dataset.charge; }
}

function submitDelivery(opt){
  const name = document.getElementById('d_name')?.value;
  const mobile = document.getElementById('d_mobile')?.value;
  const addr = document.getElementById('d_addr')?.value;
  const ch = document.getElementById('d_charge')?.dataset?.charge;
  if(!name || !mobile || !addr || !ch){ alert('Please fill all fields and select state.'); return; }
  alert(`${opt.toUpperCase()} Order Received\nName: ${name}\nMobile: ${mobile}\nAddress: ${addr}\nDelivery charge: ₹${ch}\nThank you!`);
  document.getElementById('deliveryFormContainer').innerHTML = '';
}

/* WhatsApp order (prefill message with summary + delivery) */
function sendWhatsAppOrder(opt){
  const name = document.getElementById('d_name')?.value || '';
  const mobile = document.getElementById('d_mobile')?.value || '';
  const addr = document.getElementById('d_addr')?.value || '';
  const ch = document.getElementById('d_charge')?.dataset?.charge || '';
  const summary = document.getElementById('selList').innerText || 'No items selected';
  const msg = encodeURIComponent(`Order via ${opt.toUpperCase()}%0AName: ${name}%0AMobile: ${mobile}%0AAddress: ${addr}%0AItems:%0A${summary}%0ADelivery charge: ₹${ch}`);
  // your restaurant WhatsApp number in international format (replace if needed)
  const wa = `https://wa.me/919876543210?text=${msg}`;
  window.open(wa,'_blank');
}

let slideIndex = 0;
function showHomeSlides() {
    let slides = document.querySelectorAll("#home .slide"); // <- change here
    slides.forEach(s => s.classList.remove("active"));
    slides[slideIndex].classList.add("active");
    slideIndex = (slideIndex + 1) % slides.length; // this keeps looping
}
setInterval(showHomeSlides, 2500);

// change event image and mark active list item
function changeEvent(imageName, liElem) {
  // update image
  const img = document.getElementById('eventImage');
  if(img) img.src = imageName;

  // update active class on list
  document.querySelectorAll('.event-list li').forEach(li => li.classList.remove('active'));
  if(liElem) liElem.classList.add('active');

 
}
function changeEvent(imageName, liElem) {
  // change image
  document.getElementById("eventImage").src = imageName;

  // highlight selected list item
  document.querySelectorAll(".event-list li").forEach(li => li.classList.remove("active"));
  liElem.classList.add("active");
}


function changeEvent(image, liElem) {
  document.getElementById("eventDisplay").src = image;

  document.querySelectorAll(".event-list li").forEach(li => li.classList.remove("active"));
  liElem.classList.add("active");
}

document.addEventListener("DOMContentLoaded", () => {
  document.querySelector(".event-list li").classList.add("active");
});

// Login overlay
const overlay = document.getElementById('loginOverlay');
const loginBtn = document.getElementById('loginBtn');
const googleBtn = document.getElementById('googleLoginBtn');

loginBtn.addEventListener('click', ()=>{
    const user = document.getElementById('loginUser').value;
    const pass = document.getElementById('loginPass').value;

    if(user === 'admin' && pass === '1234'){ // Demo credentials
        overlay.style.display = 'none'; // Hide login overlay
    } else {
        alert('Invalid username or password! Use admin / 1234.');
    }
});

// Google login placeholder
googleBtn.addEventListener('click', ()=>{
    alert('Google login placeholder. Integrate OAuth for real login.');
    overlay.style.display = 'none'; // Allow access after click (demo)
});

</script>



</script>


</script>
</body>
</html>
