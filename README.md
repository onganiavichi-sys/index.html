<title>NHair Amiens</title>
<meta name="claude:viewport-fit-sides" content="cover">
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Bricolage+Grotesque:opsz,wght@12..96,600;12..96,800&family=DM+Sans:wght@400;500;700&display=swap">
<style>
/* Concept : page de réservation mobile aux couleurs de la marque (brun profond et beige), le bord du hero forme les dents d'un peigne, puis un parcours en 3 étapes (style, créneau, coordonnées) qui aboutit à un message DM prêt à envoyer. */
:root {
  --bg: #f2ede7;
  --surface: #faf7f3;
  --fg: #231a15;
  --muted: #6b5d54;
  --line: #d9cec4;
  --accent: #8a5a2b;
  --accent-fg: #ffffff;
  --accent-soft: #ead9c6;
  --hero-bg: #2a1d16;
  --hero-fg: #f3e9dc;
  --hero-muted: #bfa78f;
  --warn: #9a4a1a;
  --font-display: "Bricolage Grotesque", "Avenir Next", "Segoe UI", system-ui, sans-serif;
  --font-body: "DM Sans", "Segoe UI", system-ui, -apple-system, sans-serif;
}
@media (prefers-color-scheme: dark) {
  :root:not([data-theme="light"]) {
    --bg: #15100d; --surface: #1f1814; --fg: #efe5da; --muted: #b3a291; --line: #3a2e26;
    --accent: #d9a46a; --accent-fg: #1a120c; --accent-soft: #3a2a1d;
    --hero-bg: #0f0a07; --hero-fg: #efe5da; --hero-muted: #a89078; --warn: #e0a070;
    color-scheme: dark;
  }
}
:root[data-theme="dark"] {
  --bg: #15100d; --surface: #1f1814; --fg: #efe5da; --muted: #b3a291; --line: #3a2e26;
  --accent: #d9a46a; --accent-fg: #1a120c; --accent-soft: #3a2a1d;
  --hero-bg: #0f0a07; --hero-fg: #efe5da; --hero-muted: #a89078; --warn: #e0a070;
  color-scheme: dark;
}
* { box-sizing: border-box; }
body {
  background: var(--bg); color: var(--fg);
  font-family: var(--font-body); font-size: 16px; line-height: 1.5;
  -webkit-text-size-adjust: 100%;
}
body.has-bar { padding-bottom: 5.5rem; }
h1, h2, h3 { font-family: var(--font-display); text-wrap: balance; margin: 0; line-height: 1.1; }
p { margin: 0; }
a { color: inherit; }
:focus-visible { outline: 3px solid var(--accent); outline-offset: 2px; }
.wrap {
  width: 100%; max-width: 44rem; margin-inline: auto;
  padding-left: max(16px, env(safe-area-inset-left, 0px));
  padding-right: max(16px, env(safe-area-inset-right, 0px));
}

/* Hero */
.hero {
  background: var(--hero-bg); color: var(--hero-fg);
  margin-top: calc(-1 * env(safe-area-inset-top, 0px));
  padding-top: calc(env(safe-area-inset-top, 0px) + 1.25rem);
  padding-bottom: 2.25rem;
}
.brand-row { display: flex; align-items: center; justify-content: space-between; gap: 0.75rem 1rem; flex-wrap: wrap; }
.brand { font-family: var(--font-display); font-weight: 800; font-size: 1.35rem; letter-spacing: 0.02em; line-height: 1.1; }
.brand small { display: block; font-family: var(--font-body); font-weight: 400; font-size: 0.75rem; letter-spacing: 0.08em; text-transform: uppercase; color: var(--hero-muted); margin-top: 0.15rem; }
.ig-link {
  font-size: 0.875rem; font-weight: 500; text-decoration: none; color: var(--hero-fg);
  border: 1px solid color-mix(in srgb, var(--hero-fg) 35%, transparent);
  border-radius: 999px; padding: 0.4rem 0.9rem;
}
.ig-link:hover { background: color-mix(in srgb, var(--hero-fg) 12%, transparent); }
.hero h1 { font-weight: 800; font-size: clamp(2.1rem, 9vw, 3.5rem); letter-spacing: -0.025em; margin-top: 2.5rem; max-width: 15ch; }
.hero .lead { color: var(--hero-muted); margin-top: 1rem; max-width: 36ch; font-size: 1.05rem; }
.hero-actions { display: flex; flex-wrap: wrap; gap: 0.75rem 1.25rem; align-items: center; margin-top: 1.5rem; }
.hero-note { font-size: 0.875rem; color: var(--hero-muted); }
.teeth {
  height: 18px;
  background: repeating-linear-gradient(90deg, var(--hero-bg) 0 3px, transparent 3px 9px);
}

/* Buttons */
.btn {
  appearance: none; border: 0; cursor: pointer; font: inherit; font-weight: 700;
  display: inline-flex; align-items: center; justify-content: center; gap: 0.5rem;
  min-height: 3rem; padding: 0.6rem 1.4rem; border-radius: 10px; text-decoration: none;
  background: var(--accent); color: var(--accent-fg);
}
.btn:hover { filter: brightness(1.08); }
.btn[aria-disabled="true"], .btn:disabled { opacity: 0.45; cursor: not-allowed; filter: none; }
.btn.on-hero { background: var(--hero-fg); color: var(--hero-bg); }
.btn.ghost { background: transparent; color: var(--fg); border: 1.5px solid var(--line); }
.btn.ghost:hover { border-color: var(--accent); filter: none; }

/* Sections */
main { padding-block: 2rem 1rem; display: flex; flex-direction: column; gap: 2.5rem; }
.step-head { display: flex; align-items: baseline; gap: 0.75rem; margin-bottom: 1rem; }
.step-n {
  flex: none; width: 1.75rem; height: 1.75rem; border-radius: 50%;
  display: grid; place-items: center; font-weight: 700; font-size: 0.875rem;
  background: var(--accent); color: var(--accent-fg);
}
.step-head h2 { font-size: 1.5rem; letter-spacing: -0.01em; }
.hint { color: var(--muted); font-size: 0.9rem; }
section[id] { scroll-margin-top: 1rem; }

/* Services */
.services { display: flex; flex-direction: column; gap: 0.5rem; padding: 0; margin: 0; list-style: none; }
.svc {
  width: 100%; text-align: left; font: inherit; color: inherit; cursor: pointer;
  display: grid; grid-template-columns: 1.5rem minmax(0, 1fr) auto; gap: 0.75rem; align-items: center;
  background: var(--surface); border: 1.5px solid var(--line); border-radius: 12px; padding: 0.85rem 1rem;
}
.svc:hover { border-color: var(--accent); }
.svc[aria-pressed="true"] { border-color: var(--accent); background: var(--accent-soft); }
.tick {
  width: 1.5rem; height: 1.5rem; border-radius: 6px; border: 1.5px solid var(--line);
  display: grid; place-items: center; color: transparent; background: var(--bg);
}
.svc[aria-pressed="true"] .tick { background: var(--accent); border-color: var(--accent); color: var(--accent-fg); }
.svc-name { font-weight: 700; display: block; }
.svc-desc { color: var(--muted); font-size: 0.875rem; display: block; }
.svc[aria-pressed="true"] .svc-desc { color: var(--fg); }
.svc-meta { text-align: right; font-variant-numeric: tabular-nums; white-space: nowrap; }
.svc-price { font-weight: 700; display: block; }
.svc-dur { color: var(--muted); font-size: 0.8125rem; display: block; }
.svc[aria-pressed="true"] .svc-dur { color: var(--fg); }
.sizes { display: flex; align-items: center; flex-wrap: wrap; gap: 0.5rem; padding: 0.6rem 0.25rem 0.25rem; }
.sizes .lbl { font-size: 0.875rem; font-weight: 500; margin-right: 0.25rem; }
.size {
  font: inherit; color: inherit; cursor: pointer; font-variant-numeric: tabular-nums;
  background: var(--surface); border: 1.5px solid var(--line); border-radius: 10px; padding: 0.45rem 0.9rem; min-height: 2.5rem;
}
.size:hover { border-color: var(--accent); }
.size[aria-pressed="true"] { background: var(--accent); border-color: var(--accent); color: var(--accent-fg); font-weight: 700; }

/* Dates and slots */
.dates { display: flex; gap: 0.5rem; overflow-x: auto; padding-bottom: 0.5rem; margin-bottom: 0.75rem; scrollbar-width: thin; }
.day {
  flex: none; min-width: 4.25rem; font: inherit; color: inherit; cursor: pointer;
  display: flex; flex-direction: column; align-items: center; gap: 0.1rem;
  background: var(--surface); border: 1.5px solid var(--line); border-radius: 12px; padding: 0.6rem 0.5rem;
}
.day:hover { border-color: var(--accent); }
.day[aria-pressed="true"] { background: var(--accent); border-color: var(--accent); color: var(--accent-fg); }
.day .dw { font-size: 0.75rem; text-transform: uppercase; letter-spacing: 0.06em; }
.day .dn { font-family: var(--font-display); font-weight: 800; font-size: 1.5rem; line-height: 1.1; }
.day .dm { font-size: 0.75rem; }
.slots { display: grid; grid-template-columns: repeat(auto-fill, minmax(5rem, 1fr)); gap: 0.5rem; }
.slot {
  font: inherit; font-variant-numeric: tabular-nums; color: inherit; cursor: pointer;
  background: var(--surface); border: 1.5px solid var(--line); border-radius: 10px; padding: 0.65rem 0.25rem; text-align: center;
}
.slot:hover { border-color: var(--accent); }
.slot[aria-pressed="true"] { background: var(--accent); border-color: var(--accent); color: var(--accent-fg); font-weight: 700; }
.empty { color: var(--muted); background: var(--surface); border: 1.5px dashed var(--line); border-radius: 12px; padding: 1rem; }

/* Form */
.fields { display: grid; gap: 1rem; grid-template-columns: repeat(auto-fit, minmax(14rem, 1fr)); }
.field { display: flex; flex-direction: column; gap: 0.35rem; min-width: 0; }
.field.full { grid-column: 1 / -1; }
label { font-weight: 500; font-size: 0.9rem; }
input, textarea {
  font: inherit; color: var(--fg); background: var(--surface);
  border: 1.5px solid var(--line); border-radius: 10px; padding: 0.7rem 0.85rem; width: 100%; min-width: 0;
}
textarea { resize: vertical; min-height: 5rem; }
input:focus-visible, textarea:focus-visible { border-color: var(--accent); }

/* Send block */
.send { background: var(--surface); border: 1.5px solid var(--line); border-radius: 14px; padding: 1.1rem; display: flex; flex-direction: column; gap: 1rem; }
.send h3 { font-size: 1.15rem; }
.msg {
  margin: 0; white-space: pre-wrap; overflow-wrap: anywhere; font-family: var(--font-body); font-size: 0.95rem;
  background: var(--bg); border: 1px solid var(--line); border-radius: 10px; padding: 0.85rem; user-select: text;
}
.send-actions { display: flex; flex-wrap: wrap; gap: 0.6rem; }
.send-actions .btn { flex: 1 1 12rem; }
.status { min-height: 1.4em; font-size: 0.9rem; color: var(--muted); }
.status.warn { color: var(--warn); }

.deposit { background: var(--accent-soft); border-radius: 10px; padding: 0.85rem 1rem; display: flex; flex-direction: column; gap: 0.6rem; }
.deposit p { font-size: 0.95rem; }
.deposit label { display: flex; align-items: flex-start; gap: 0.6rem; font-weight: 500; cursor: pointer; }
.deposit input { flex: none; width: 1.35rem; height: 1.35rem; padding: 0; margin: 0.1rem 0 0; accent-color: var(--accent); }

/* Infos */
.info { display: grid; gap: 1.5rem; grid-template-columns: repeat(auto-fit, minmax(15rem, 1fr)); }
.info h2 { font-size: 1.25rem; margin-bottom: 0.6rem; }
.hours { display: grid; grid-template-columns: auto 1fr; gap: 0.25rem 1.25rem; margin: 0; font-variant-numeric: tabular-nums; }
.hours dt { font-weight: 500; }
.hours dd { margin: 0; color: var(--muted); }
.sel { user-select: text; }
footer { padding-block: 1.5rem 2rem; color: var(--muted); font-size: 0.85rem; border-top: 1px solid var(--line); margin-top: 1rem; }

/* Sticky bar */
.bar {
  position: fixed; left: 0; right: 0; bottom: 0; z-index: 20;
  background: var(--surface); border-top: 1px solid var(--line);
  padding: 0.65rem max(16px, env(safe-area-inset-right, 0px)) calc(0.65rem + env(safe-area-inset-bottom, 0px)) max(16px, env(safe-area-inset-left, 0px));
}
.bar-in { max-width: 44rem; margin-inline: auto; display: flex; align-items: center; justify-content: space-between; gap: 0.75rem; }
.bar-txt { min-width: 0; font-variant-numeric: tabular-nums; }
.bar-txt strong { display: block; font-size: 1rem; }
.bar-txt span { font-size: 0.8125rem; color: var(--muted); }
.bar .btn { flex: none; min-height: 2.75rem; padding-inline: 1.1rem; }
@media (prefers-reduced-motion: no-preference) {
  .svc, .day, .slot, .size, .btn { transition: background-color 0.15s, border-color 0.15s, color 0.15s; }
}
</style>

<header class="hero">
  <div class="wrap">
    <div class="brand-row">
      <span class="brand" id="brand">NHair<small>Nélia Hair · Amiens</small></span>
      <a class="ig-link" id="igTop" href="https://instagram.com/nhair.amiens" target="_blank" rel="noopener">@nhair.amiens</a>
    </div>
    <h1>Votre coiffure afro à domicile, à Amiens.</h1>
    <p class="lead">Nélia se déplace chez vous. Choisissez votre style et un créneau, votre demande arrive en DM puis Nélia confirme.</p>
    <div class="hero-actions">
      <a class="btn on-hero" href="#prestations">Réserver</a>
      <span class="hero-note">Réservation par DM Instagram</span>
    </div>
  </div>
</header>
<div class="teeth" aria-hidden="true"></div>

<main class="wrap">
  <section id="prestations" aria-labelledby="h-prest">
    <div class="step-head"><span class="step-n" aria-hidden="true">1</span><h2 id="h-prest">Votre style</h2></div>
    <p class="hint" style="margin-bottom:0.9rem">Vous pouvez en choisir plusieurs. La durée totale sert à trouver les créneaux.</p>
    <ul class="services" id="services"></ul>
  </section>

  <section id="creneau" aria-labelledby="h-cren">
    <div class="step-head"><span class="step-n" aria-hidden="true">2</span><h2 id="h-cren">Jour et heure</h2></div>
    <div class="dates" id="dates" role="group" aria-label="Jours disponibles"></div>
    <div id="slots" aria-live="polite"></div>
  </section>

  <section id="coordonnees" aria-labelledby="h-coord">
    <div class="step-head"><span class="step-n" aria-hidden="true">3</span><h2 id="h-coord">Vos coordonnées</h2></div>
    <div class="fields">
      <div class="field">
        <label for="fName">Prénom et nom</label>
        <input id="fName" type="text" autocomplete="name" placeholder="Camille Martin">
      </div>
      <div class="field">
        <label for="fTel">Téléphone</label>
        <input id="fTel" type="tel" autocomplete="tel" inputmode="tel" placeholder="06 12 34 56 78">
      </div>
      <div class="field full">
        <label for="fAddr">Adresse du rendez-vous (Amiens)</label>
        <input id="fAddr" type="text" autocomplete="street-address" placeholder="Numéro et rue, étage ou digicode si besoin">
      </div>
      <div class="field full">
        <label for="fNote">Précision (facultatif)</label>
        <textarea id="fNote" placeholder="Longueur souhaitée, couleur des mèches, mèches fournies ou non…"></textarea>
      </div>
    </div>
  </section>

  <section id="envoi" aria-labelledby="h-envoi">
    <div class="send">
      <h3 id="h-envoi">Envoyer ma demande</h3>
      <div class="deposit">
        <p><strong>Acompte de 20 € non remboursable.</strong> Il confirme votre rendez-vous. Nélia vous envoie les moyens de paiement avec sa réponse.</p>
        <label for="fDeposit"><input id="fDeposit" type="checkbox"><span>J'ai compris et j'accepte l'acompte de 20 €</span></label>
      </div>
      <pre class="msg" id="msg">Choisissez un style et un créneau pour voir votre message.</pre>
      <div class="send-actions">
        <a class="btn" id="igSend" href="https://ig.me/m/nhair.amiens" target="_blank" rel="noopener" aria-disabled="true">Copier et ouvrir Instagram</a>
        <button class="btn ghost" id="copyBtn" type="button" aria-disabled="true">Copier le message</button>
      </div>
      <p class="status" id="status" role="status" aria-live="polite"></p>
      <p class="hint">Le rendez-vous est confirmé par Nélia une fois l'acompte reçu.</p>
    </div>
  </section>

  <section class="info" aria-label="Infos pratiques">
    <div>
      <h2>Horaires</h2>
      <dl class="hours" id="hours"></dl>
      <p class="hint" style="margin-top:0.5rem">Les durées affichées sont indicatives.</p>
    </div>
    <div>
      <h2>Où</h2>
      <p class="sel" id="addr">À domicile, à Amiens</p>
      <p class="hint" style="margin-top:0.5rem">Nélia se déplace chez vous avec son matériel. Indiquez votre adresse en réservant.</p>
    </div>
  </section>
</main>

<footer>
  <div class="wrap"><span id="foot">NHair · Nélia Hair</span> · Coiffure à domicile à Amiens</div>
</footer>

<div class="bar" id="bar" hidden>
  <div class="bar-in">
    <div class="bar-txt"><strong id="barMain"></strong><span id="barSub"></span></div>
    <button class="btn" id="barBtn" type="button">Choisir un créneau</button>
  </div>
</div>

<script>
(function () {
  // À modifier : horaires (en minutes depuis minuit), prestations, prix et durées.
  var CONFIG = {
    name: "NHair",
    owner: "Nélia",
    instagram: "nhair.amiens",
    sizeLabel: "Taille des tresses",
    sizeNames: { S: "petites", M: "moyennes", L: "grandes" },
    hours: { 1: [540, 1140], 2: [540, 1140], 3: [540, 1140], 4: [540, 1140], 5: [540, 1140], 6: [540, 1140] },
    services: [
      { id: "vanilles", name: "Vanilles / twists", desc: "Twists en deux brins", min: 180, price: 50 },
      { id: "knotless", name: "Knotless braids", desc: "Tresses sans nœud, effet naturel", sizes: [
        { k: "S", min: 360, price: 100 }, { k: "M", min: 300, price: 80 }, { k: "L", min: 240, price: 60 } ] },
      { id: "nattes", name: "Nattes collées", desc: "Nattes collées au cuir chevelu", min: 60, price: 25 },
      { id: "fulani", name: "Fulani braids", desc: "Tresses avec nattes collées sur l'avant", min: 240, price: 70 },
      { id: "miracle", name: "Miracle Knots braids", desc: "Tresses nouées", min: 300, price: 80 },
      { id: "boho", name: "Boho braids", desc: "Tresses avec mèches bouclées", sizes: [
        { k: "S", min: 360, price: 120 }, { k: "M", min: 300, price: 85 }, { k: "L", min: 240, price: 65 } ] }
    ]
  };

  var $ = function (s) { return document.querySelector(s); };
  var state = { svc: {}, date: null, time: null };
  var reduce = window.matchMedia && matchMedia("(prefers-reduced-motion: reduce)").matches;

  function fmtDur(m) {
    var h = Math.floor(m / 60), r = m % 60;
    if (!h) return r + " min";
    return r ? h + " h " + (r < 10 ? "0" + r : r) : h + " h";
  }
  function fmtTime(m) {
    var h = Math.floor(m / 60), r = m % 60;
    return h + "h" + (r < 10 ? "0" + r : r);
  }
  function variant(s) {
    if (!s.sizes) return s;
    var k = state.svc[s.id];
    return s.sizes.filter(function (v) { return v.k === k; })[0] || s.sizes[0];
  }
  function selected() {
    return CONFIG.services.filter(function (s) { return s.id in state.svc; }).map(function (s) {
      var v = variant(s);
      return { id: s.id, name: s.sizes ? s.name + " (taille " + v.k + ")" : s.name, min: v.min, price: v.price };
    });
  }
  function totals() {
    return selected().reduce(function (a, s) { a.min += s.min; a.price += s.price; return a; }, { min: 0, price: 0 });
  }
  function dateLong(d) { return d.toLocaleDateString("fr-FR", { weekday: "long", day: "numeric", month: "long" }); }

  // Static content
  $("#igTop").href = "https://instagram.com/" + CONFIG.instagram;
  $("#igSend").href = "https://ig.me/m/" + CONFIG.instagram;

  var dayNames = ["Dimanche", "Lundi", "Mardi", "Mercredi", "Jeudi", "Vendredi", "Samedi"];
  $("#hours").innerHTML = [1, 2, 3, 4, 5, 6, 0].map(function (d) {
    var h = CONFIG.hours[d];
    return "<dt>" + dayNames[d] + "</dt><dd>" + (h ? fmtTime(h[0]) + " – " + fmtTime(h[1]) : "Fermé") + "</dd>";
  }).join("");

  // Services
  var tickSvg = '<svg width="14" height="14" viewBox="0 0 14 14" aria-hidden="true"><path d="M2.5 7.5l3 3 6-7" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg>';
  function priceText(s) {
    if (!s.sizes) return s.price + " €";
    return s.sizes[0].price + " – " + s.sizes[s.sizes.length - 1].price + " €";
  }
  function durText(s) {
    if (!s.sizes) return fmtDur(s.min);
    var mins = s.sizes.map(function (v) { return v.min; });
    return fmtDur(Math.min.apply(null, mins)) + " – " + fmtDur(Math.max.apply(null, mins));
  }
  $("#services").innerHTML = CONFIG.services.map(function (s) {
    var sizes = s.sizes ? '<div class="sizes" data-sizes="' + s.id + '" hidden><span class="lbl">' + CONFIG.sizeLabel + '</span>' +
      s.sizes.map(function (v) {
        return '<button type="button" class="size" data-id="' + s.id + '" data-k="' + v.k + '" aria-pressed="false">' + v.k + ' ' + (CONFIG.sizeNames[v.k] || "") + ' · ' + v.price + ' €</button>';
      }).join("") + '</div>' : "";
    return '<li><button type="button" class="svc" data-id="' + s.id + '" aria-pressed="false">' +
      '<span class="tick">' + tickSvg + '</span>' +
      '<span><span class="svc-name">' + s.name + '</span><span class="svc-desc">' + s.desc + '</span></span>' +
      '<span class="svc-meta"><span class="svc-price">' + (s.sizes ? "dès " + Math.min.apply(null, s.sizes.map(function (v) { return v.price; })) + " €" : s.price + " €") + '</span><span class="svc-dur">' + durText(s) + '</span></span>' +
      '</button>' + sizes + '</li>';
  }).join("");

  // Dates: next 21 open days
  var days = [];
  var now0 = new Date();
  for (var i = 0; i < 21; i++) {
    var d = new Date(now0.getFullYear(), now0.getMonth(), now0.getDate() + i);
    if (CONFIG.hours[d.getDay()]) days.push(d);
  }
  $("#dates").innerHTML = days.map(function (d, i) {
    return '<button type="button" class="day" data-i="' + i + '" aria-pressed="false">' +
      '<span class="dw">' + d.toLocaleDateString("fr-FR", { weekday: "short" }).replace(".", "") + '</span>' +
      '<span class="dn">' + d.getDate() + '</span>' +
      '<span class="dm">' + d.toLocaleDateString("fr-FR", { month: "short" }).replace(".", "") + '</span></button>';
  }).join("");

  function computeSlots() {
    if (!state.date || !selected().length) return [];
    var h = CONFIG.hours[state.date.getDay()];
    var dur = totals().min;
    var now = new Date();
    var isToday = state.date.toDateString() === now.toDateString();
    var earliest = now.getHours() * 60 + now.getMinutes() + 60;
    var out = [];
    for (var t = h[0]; t + dur <= h[1]; t += 30) {
      if (isToday && t < earliest) continue;
      out.push(t);
    }
    return out;
  }

  function renderSlots() {
    var box = $("#slots");
    if (!selected().length) {
      box.innerHTML = '<p class="empty">Choisissez d\'abord un style, les horaires s\'adaptent à sa durée.</p>';
      return;
    }
    if (!state.date) {
      box.innerHTML = '<p class="empty">Choisissez un jour pour voir les horaires.</p>';
      return;
    }
    var slots = computeSlots();
    if (state.time !== null && slots.indexOf(state.time) === -1) state.time = null;
    if (!slots.length) {
      box.innerHTML = '<p class="empty">Plus de créneau ce jour-là pour ' + fmtDur(totals().min) + '. Essayez un autre jour.</p>';
      return;
    }
    box.innerHTML = '<p class="hint" style="margin-bottom:0.6rem">' + dateLong(state.date) + ' · durée ' + fmtDur(totals().min) + '</p>' +
      '<div class="slots">' + slots.map(function (t) {
        return '<button type="button" class="slot" data-t="' + t + '" aria-pressed="' + (state.time === t) + '">' + fmtTime(t) + '</button>';
      }).join("") + '</div>';
  }

  function phoneOk() { return ($("#fTel").value.replace(/\D/g, "").length >= 6); }
  function missing() {
    var m = [];
    if (!selected().length) m.push("un style");
    if (!state.date || state.time === null) m.push("un créneau");
    if (!$("#fName").value.trim()) m.push("votre nom");
    if (!phoneOk()) m.push("votre téléphone");
    if (!$("#fAddr").value.trim()) m.push("votre adresse");
    if (!$("#fDeposit").checked) m.push("l'accord sur l'acompte");
    return m;
  }
  function buildMessage() {
    var sel = selected(), t = totals();
    var l = [];
    l.push("Bonjour " + CONFIG.owner + ", je souhaite réserver :");
    l.push(sel.map(function (s) { return s.name; }).join(" + ") + " (" + fmtDur(t.min) + ", " + t.price + " €)");
    l.push("Le " + dateLong(state.date) + " à " + fmtTime(state.time));
    l.push("Nom : " + $("#fName").value.trim());
    l.push("Téléphone : " + $("#fTel").value.trim());
    l.push("Adresse : " + $("#fAddr").value.trim());
    var note = $("#fNote").value.trim();
    if (note) l.push("Précision : " + note);
    l.push("J'accepte l'acompte de 20 € non remboursable.");
    l.push("Merci !");
    return l.join("\n");
  }

  var statusEl = $("#status");
  function setStatus(text, warn) {
    statusEl.textContent = text || "";
    statusEl.className = "status" + (warn ? " warn" : "");
  }

  function refreshSend() {
    var miss = missing();
    var ok = miss.length === 0;
    var msgEl = $("#msg");
    if (ok) msgEl.textContent = buildMessage();
    else msgEl.textContent = "Il manque encore : " + miss.join(", ") + ".";
    ["#igSend", "#copyBtn"].forEach(function (id) { $(id).setAttribute("aria-disabled", ok ? "false" : "true"); });
    if (ok) setStatus("");
  }

  function nextStep() {
    if (!state.date || state.time === null) return { label: "Choisir un créneau", target: "creneau" };
    if (!$("#fName").value.trim() || !phoneOk() || !$("#fAddr").value.trim()) return { label: "Mes coordonnées", target: "coordonnees" };
    return { label: "Envoyer ma demande", target: "envoi" };
  }
  function refreshBar() {
    var sel = selected(), t = totals();
    var bar = $("#bar");
    bar.hidden = sel.length === 0;
    document.body.classList.toggle("has-bar", sel.length > 0);
    if (!sel.length) return;
    $("#barMain").textContent = sel.length + (sel.length > 1 ? " styles" : " style") + " · " + t.price + " €";
    $("#barSub").textContent = fmtDur(t.min) + (state.date && state.time !== null ? " · " + dateLong(state.date) + " " + fmtTime(state.time) : "");
    var next = nextStep();
    $("#barBtn").textContent = next.label;
    $("#barBtn").dataset.target = next.target;
  }

  function refreshAll() {
    document.querySelectorAll(".svc").forEach(function (b) { b.setAttribute("aria-pressed", (b.dataset.id in state.svc) ? "true" 

nhair_Amiens 
