https://1drv.ms/u/c/B3AC8C293C5BE2E1/IQBA5Laz0CO8RKKmZwip6E_AAUR1PLrjXxvdvsuIAdH2vP0?e=MOVVQK
https://1drv.ms/u/c/B3AC8C293C5BE2E1/IQBvxnBvbG6jS5k59W_ut3AxARv-ISOMhEw4hb25t36guvo?e=8P1DjI
https://1drv.ms/u/c/B3AC8C293C5BE2E1/IQD2gdHJVueRSLpkv8_rEFzTAfNgjpx2wbc8F_AN91z3dUg?e=3LR9hT
https://1drv.ms/u/c/B3AC8C293C5BE2E1/IQArjsQ8E9HcT6dr2tOoRVZpAZ6WncExhZslsJIVFNuri2c?e=N3b2WV
Advanced Architecturelink:https://your-name-portfolio.netlify.app/
To-Do List Application: https://pdf.ac/bPNT-bbN
weather dashboard:
https://drive.google.com/file/d/1NHYJJr1SocsyChQJ_IikmMspVviXazUJ/view?usp=drivesdk
final:https://1drv.ms/u/c/B3AC8C293C5BE2E1/IQCQXTXtIIkaQrZv2jchUkT-ASa2liLCde34i9AR5276rxY?e=veFodG
[fernweh-supply-co-STANDALONE.html](https://github.com/user-attachments/files/29959585/fernweh-supply-co-STANDALONE.html)
This is final code
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<meta name="description" content="Fernweh Supply Co. — canvas, brass, and cast-iron camp gear built to be repaired, not replaced.">
<meta name="theme-color" content="#3f6b4f">
<title>Fernweh Supply Co. — Camp &amp; Field Gear</title>
<style>
:root {
  --ink: #1b1f23;
  --paper: #fbfaf7;
  --panel: #ffffff;
  --line: #e3e0d8;
  --moss: #3f6b4f;
  --moss-dark: #2c4d38;
  --clay: #b5533c;
  --gold: #c98a2c;
  --muted: #8a8578;
  --shadow: 0 1px 2px rgba(27,31,35,0.04), 0 8px 24px rgba(27,31,35,0.06);
  --radius: 10px;
  --max: 1100px;
}

* { box-sizing: border-box; }
html { scroll-behavior: smooth; }

body {
  margin: 0;
  background: var(--paper);
  background-image: radial-gradient(circle at 1px 1px, rgba(27,31,35,0.05) 1px, transparent 0);
  background-size: 22px 22px;
  color: var(--ink);
  font-family: "Iowan Old Style", "Palatino Linotype", Georgia, serif;
  line-height: 1.55;
}

a { color: var(--moss-dark); }
img, svg { max-width: 100%; display: block; }

.skip-link {
  position: absolute; left: -999px; top: 0;
  background: var(--ink); color: var(--paper);
  padding: 10px 16px; z-index: 100;
}
.skip-link:focus { left: 0; }

/* ---------- Header ---------- */
.site-header {
  position: sticky; top: 0; z-index: 40;
  background: var(--paper);
  border-bottom: 2px solid var(--ink);
}
.site-header .inner {
  max-width: var(--max); margin: 0 auto; padding: 16px 24px;
  display: flex; align-items: center; justify-content: space-between; gap: 16px;
}
.brand-mark { display: flex; align-items: baseline; gap: 8px; text-decoration: none; color: var(--ink); }
.brand-mark .glyph { font-size: 1.3rem; }
.brand-mark .word { font-size: 1.3rem; font-weight: 700; letter-spacing: -0.01em; }
.brand-mark .word small { display: block; font-family: "Courier New", monospace; font-size: 0.6rem; color: var(--muted); letter-spacing: 0.08em; text-transform: uppercase; font-weight: 400; }

.nav-toggle {
  display: none;
  background: none; border: 1.5px solid var(--line); border-radius: 8px;
  font-family: inherit; font-size: 0.95rem; padding: 8px 12px; cursor: pointer;
}

.primary-nav ul {
  list-style: none; display: flex; gap: 22px; margin: 0; padding: 0;
  align-items: center; font-family: "Courier New", monospace; font-size: 0.82rem;
  text-transform: uppercase; letter-spacing: 0.05em;
}
.primary-nav a { text-decoration: none; color: var(--ink); padding: 6px 2px; border-bottom: 2px solid transparent; }
.primary-nav a:hover, .primary-nav a.active { color: var(--moss-dark); border-bottom-color: var(--moss); }
.cart-link { position: relative; display: inline-flex; align-items: center; gap: 6px; }
.cart-badge {
  display: none; align-items: center; justify-content: center;
  min-width: 18px; height: 18px; padding: 0 4px;
  background: var(--clay); color: #fff; border-radius: 999px;
  font-size: 0.7rem; font-family: "Courier New", monospace;
}

@media (max-width: 760px) {
  .nav-toggle { display: inline-block; }
  .primary-nav {
    position: absolute; top: 100%; left: 0; right: 0;
    background: var(--paper); border-bottom: 2px solid var(--ink);
    display: none; padding: 14px 24px 20px;
  }
  .primary-nav.open { display: block; }
  .primary-nav ul { flex-direction: column; align-items: flex-start; gap: 14px; }
}

/* ---------- Layout ---------- */
main { max-width: var(--max); margin: 0 auto; padding: 40px 24px 80px; min-height: 60vh; }
.section { margin-top: 64px; }
.section-head { display: flex; align-items: baseline; justify-content: space-between; gap: 16px; margin-bottom: 22px; }
.eyebrow { font-family: "Courier New", monospace; font-size: 0.78rem; text-transform: uppercase; letter-spacing: 0.08em; color: var(--muted); margin: 0 0 10px; }
.text-link { font-family: "Courier New", monospace; font-size: 0.8rem; text-decoration: underline; text-underline-offset: 3px; }

/* ---------- Hero ---------- */
.hero { padding: 24px 0 8px; max-width: 720px; }
.hero h1 { font-size: clamp(2.1rem, 4.5vw, 3.1rem); line-height: 1.08; letter-spacing: -0.01em; margin: 0 0 18px; }
.hero-sub { font-size: 1.08rem; color: #3a3d40; max-width: 60ch; }
.cta-row { display: flex; gap: 12px; margin-top: 22px; flex-wrap: wrap; }

.btn {
  display: inline-block; padding: 12px 22px; border-radius: var(--radius);
  background: var(--ink); color: var(--paper); border: 1.5px solid var(--ink);
  font-family: "Courier New", monospace; font-size: 0.85rem; text-transform: uppercase;
  letter-spacing: 0.05em; font-weight: 700; text-decoration: none; cursor: pointer;
  transition: background 0.15s ease, transform 0.1s ease;
}
.btn:hover { background: var(--moss-dark); border-color: var(--moss-dark); transform: translateY(-1px); }
.btn:active { transform: translateY(0); }
.btn-ghost { background: transparent; color: var(--ink); }
.btn-ghost:hover { background: var(--ink); color: var(--paper); }
.btn-small { padding: 8px 14px; font-size: 0.72rem; }

/* ---------- Product grid ---------- */
.product-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(230px, 1fr)); gap: 18px; }
.product-card {
  background: var(--panel); border: 1.5px solid var(--line); border-radius: var(--radius);
  box-shadow: var(--shadow); overflow: hidden; display: flex; flex-direction: column;
}
.product-media { background: #f1ede2; padding: 18px; }
.product-body { padding: 16px; display: flex; flex-direction: column; gap: 6px; }
.product-body h3 { margin: 0; font-size: 1.05rem; }
.product-body h3 a { text-decoration: none; color: var(--ink); }
.product-eyebrow { font-family: "Courier New", monospace; font-size: 0.68rem; text-transform: uppercase; letter-spacing: 0.06em; color: var(--muted); margin: 0; }
.product-blurb { font-size: 0.92rem; color: #4a4d50; margin: 4px 0 6px; }
.product-foot { display: flex; align-items: center; justify-content: space-between; margin-top: auto; padding-top: 6px; }
.price { font-family: "Courier New", monospace; font-weight: 700; color: var(--clay); }
.price-lg { font-size: 1.4rem; }

/* ---------- Promise band ---------- */
.band { background: var(--panel); border: 1.5px solid var(--line); border-radius: 14px; padding: 34px; }
.promise-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(220px, 1fr)); gap: 24px; margin-top: 18px; }
.promise-item h3 { margin: 0 0 6px; font-size: 1.05rem; }
.promise-item p { margin: 0; color: #4a4d50; font-size: 0.94rem; }

/* ---------- Shop page ---------- */
.shop-head { margin-bottom: 30px; }
.shop-controls { display: flex; flex-direction: column; gap: 14px; margin-top: 20px; }
#shopSearch {
  padding: 12px 16px; border: 1.5px solid var(--line); border-radius: var(--radius);
  font-family: inherit; font-size: 1rem; background: var(--panel);
}
.chip-row { display: flex; gap: 8px; flex-wrap: wrap; font-family: "Courier New", monospace; font-size: 0.78rem; text-transform: uppercase; letter-spacing: 0.05em; }
.chip { padding: 7px 14px; border-radius: 999px; border: 1.5px solid var(--line); background: transparent; color: var(--muted); cursor: pointer; }
.chip.active { background: var(--ink); border-color: var(--ink); color: var(--paper); }
.empty-note { color: var(--muted); }

/* ---------- Product detail ---------- */
.back-link { display: inline-block; margin-bottom: 20px; }
.product-detail-grid { display: grid; grid-template-columns: 320px 1fr; gap: 40px; }
.product-detail-media { background: #f1ede2; border: 1.5px solid var(--line); border-radius: var(--radius); padding: 30px; }
.product-detail-body h1 { margin: 4px 0 10px; font-size: 2rem; }
.product-detail-text { color: #3a3d40; max-width: 60ch; margin: 14px 0 22px; }
.qty-row { display: flex; align-items: center; gap: 10px; margin-bottom: 18px; font-family: "Courier New", monospace; font-size: 0.85rem; }
.qty-row input { width: 72px; padding: 8px 10px; border: 1.5px solid var(--line); border-radius: 8px; font-family: inherit; }
@media (max-width: 700px) { .product-detail-grid { grid-template-columns: 1fr; } }

/* ---------- Cart (signature: packing-list ledger) ---------- */
.cart-page h1, .cart-empty h1 { margin-bottom: 6px; }
.cart-list { display: flex; flex-direction: column; margin-top: 22px; }
.cart-line {
  display: grid; grid-template-columns: 60px 1fr auto auto auto; gap: 16px; align-items: center;
  padding: 14px 4px; border-bottom: 1px dashed var(--line);
}
.cart-line-media { width: 52px; height: 52px; background: #f1ede2; border-radius: 8px; padding: 6px; }
.cart-line-body h3 { margin: 0; font-size: 1rem; }
.cart-line-body h3 a { text-decoration: none; color: var(--ink); }
.cart-line-qty { display: flex; align-items: center; gap: 10px; font-family: "Courier New", monospace; }
.icon-btn { background: none; border: 1.5px solid var(--line); border-radius: 6px; width: 26px; height: 26px; cursor: pointer; font-family: inherit; }
.icon-btn.delete { border: none; text-decoration: underline; width: auto; font-family: "Courier New", monospace; font-size: 0.75rem; color: var(--muted); }
.icon-btn.delete:hover { color: var(--clay); }
.cart-line-total { font-family: "Courier New", monospace; font-weight: 700; }

.cart-summary {
  margin-top: 28px; padding: 22px; border: 1.5px dashed var(--ink); border-radius: var(--radius);
  background: var(--panel); max-width: 360px; margin-left: auto;
}
.cart-summary-row { display: flex; justify-content: space-between; font-family: "Courier New", monospace; font-size: 1.05rem; font-weight: 700; margin-bottom: 6px; }
.cart-note { color: var(--muted); font-size: 0.82rem; margin: 0 0 18px; }
.cart-actions { display: flex; flex-direction: column; gap: 10px; }

.confirm { text-align: center; padding: 40px 20px; }
.confirm-id { font-family: "Courier New", monospace; color: var(--moss-dark); font-size: 1.2rem; margin-bottom: 14px; }

/* ---------- Forms ---------- */
.contact-form { max-width: 520px; margin-top: 24px; display: flex; flex-direction: column; gap: 18px; }
.field { display: flex; flex-direction: column; gap: 6px; }
.field label { font-family: "Courier New", monospace; font-size: 0.78rem; text-transform: uppercase; letter-spacing: 0.05em; }
.field input, .field textarea {
  padding: 12px 14px; border: 1.5px solid var(--line); border-radius: 8px;
  font-family: inherit; font-size: 1rem; background: var(--panel); resize: vertical;
}
.field input:focus, .field textarea:focus, #shopSearch:focus { outline: none; border-color: var(--moss); }
.field input[aria-invalid="true"], .field textarea[aria-invalid="true"] { border-color: var(--clay); }
.field-error { color: var(--clay); font-size: 0.82rem; margin: 0; min-height: 1.1em; }
.form-status { font-family: "Courier New", monospace; font-size: 0.85rem; }
.form-status.success { color: var(--moss-dark); }
.form-status.error { color: var(--clay); }

/* ---------- Misc pages ---------- */
.not-found { padding: 60px 0; text-align: center; }

/* ---------- Footer ---------- */
.site-footer { border-top: 2px solid var(--ink); margin-top: 40px; }
.site-footer .inner { max-width: var(--max); margin: 0 auto; padding: 30px 24px; display: flex; justify-content: space-between; flex-wrap: wrap; gap: 14px; font-family: "Courier New", monospace; font-size: 0.78rem; color: var(--muted); }

@media (prefers-reduced-motion: reduce) {
  html { scroll-behavior: auto; }
  * { transition: none !important; animation: none !important; }
}

</style>
</head>
<body>
<a href="#main" class="skip-link">Skip to main content</a>

<header class="site-header">
  <div class="inner">
    <a href="#/" class="brand-mark">
      <span class="glyph" aria-hidden="true">⛺</span>
      <span class="word">Fernweh<small>Supply Co.</small></span>
    </a>
    <button type="button" class="nav-toggle" id="navToggle" aria-expanded="false" aria-controls="primaryNav">Menu</button>
    <nav class="primary-nav" id="primaryNav" aria-label="Primary">
      <ul>
        <li><a href="#/" data-nav-link>Home</a></li>
        <li><a href="#/shop" data-nav-link>Shop</a></li>
        <li><a href="#/about" data-nav-link>About</a></li>
        <li><a href="#/contact" data-nav-link>Contact</a></li>
        <li><a href="#/cart" data-nav-link class="cart-link">Pack <span class="cart-badge" id="cartBadge">0</span></a></li>
      </ul>
    </nav>
  </div>
</header>

<main id="main">
  <div id="view" aria-live="polite"></div>
</main>

<footer class="site-footer">
  <div class="inner">
    <span>&copy; 2026 Fernweh Supply Co. — demo storefront, no real orders are placed.</span>
    <span>Built as a static, framework-free SPA.</span>
  </div>
</footer>

<script>
// ==== js/products.js ====
// products.js — catalog data + lightweight inline "field-sketch" art.
// Inline SVG keeps the whole catalog under a few KB and needs zero
// network requests for imagery — the biggest lever for a fast first load.

const stroke = '#1b1f23';

const ICONS = {
  pack: `<svg viewBox="0 0 120 120"><rect x="30" y="34" width="60" height="66" rx="10" fill="#e7dfce" stroke="${stroke}" stroke-width="2.5"/><path d="M42 34c0-12 8-20 18-20s18 8 18 20" fill="none" stroke="${stroke}" stroke-width="2.5"/><rect x="30" y="52" width="60" height="10" fill="#3f6b4f"/><line x1="60" y1="62" x2="60" y2="100" stroke="${stroke}" stroke-width="1.5" stroke-dasharray="3 3"/></svg>`,
  mug: `<svg viewBox="0 0 120 120"><rect x="35" y="40" width="42" height="46" rx="4" fill="#b5533c" stroke="${stroke}" stroke-width="2.5"/><path d="M77 50c14 0 14 26 0 26" fill="none" stroke="${stroke}" stroke-width="2.5"/><line x1="43" y1="52" x2="43" y2="76" stroke="#fbfaf7" stroke-width="2"/></svg>`,
  compass: `<svg viewBox="0 0 120 120"><circle cx="60" cy="60" r="32" fill="#e7dfce" stroke="${stroke}" stroke-width="2.5"/><polygon points="60,36 68,60 60,84 52,60" fill="#b5533c" stroke="${stroke}" stroke-width="1.5"/><circle cx="60" cy="60" r="3.5" fill="${stroke}"/></svg>`,
  tent: `<svg viewBox="0 0 120 120"><polygon points="60,32 96,88 24,88" fill="#e7dfce" stroke="${stroke}" stroke-width="2.5"/><polygon points="60,32 78,88 42,88" fill="#3f6b4f" stroke="${stroke}" stroke-width="2"/><line x1="60" y1="32" x2="60" y2="88" stroke="${stroke}" stroke-width="1.5"/></svg>`,
  knife: `<svg viewBox="0 0 120 120"><rect x="24" y="70" width="46" height="10" rx="3" fill="#8a8578" stroke="${stroke}" stroke-width="2"/><path d="M70 72 L94 62 L94 88 L70 78 Z" fill="#c7ccce" stroke="${stroke}" stroke-width="2"/></svg>`,
  lantern: `<svg viewBox="0 0 120 120"><rect x="46" y="30" width="28" height="8" fill="${stroke}"/><path d="M40 40h40l-6 46H46z" fill="#e9c86a" stroke="${stroke}" stroke-width="2.5"/><line x1="60" y1="40" x2="60" y2="86" stroke="${stroke}" stroke-width="1.5" stroke-dasharray="2 3"/><rect x="50" y="86" width="20" height="8" fill="${stroke}"/></svg>`,
  blanket: `<svg viewBox="0 0 120 120"><rect x="26" y="40" width="68" height="44" fill="#c1543f" stroke="${stroke}" stroke-width="2.5"/><line x1="26" y1="54" x2="94" y2="54" stroke="${stroke}" stroke-width="2"/><line x1="26" y1="68" x2="94" y2="68" stroke="${stroke}" stroke-width="2"/><line x1="46" y1="40" x2="46" y2="84" stroke="${stroke}" stroke-width="1.5" stroke-dasharray="2 3"/></svg>`,
  map: `<svg viewBox="0 0 120 120"><rect x="28" y="26" width="64" height="68" fill="#f3ecd9" stroke="${stroke}" stroke-width="2.5"/><path d="M32 40 Q60 50 88 36" fill="none" stroke="#3f6b4f" stroke-width="2" stroke-dasharray="4 3"/><circle cx="70" cy="66" r="3" fill="#b5533c"/></svg>`,
};

const PRODUCTS = [
  { id: "waxed-pack",   name: "Waxed Canvas Field Pack",  price: 128, category: "Packs",       icon: "pack",
    blurb: "22L waxed cotton pack with a bridle-leather base and a roll-top that shrugs off drizzle.",
    detail: "Cut from 12oz waxed canvas and stitched over a full-grain leather base, the Field Pack is built for a day of moving between trail and town. The roll-top keeps a spare layer dry; the single external strap holds an axe, mat, or tripod without extra hardware." },
  { id: "cast-mug",     name: "Cast Iron Camp Mug",       price: 24,  category: "Kitchen",     icon: "mug",
    blurb: "Enamel-lined cast iron, seasoned to hold heat through a cold morning.",
    detail: "A camp mug that outlasts the trip. The enamel lining resists scorching and metallic taste, while the cast body holds heat twice as long as steel. Hangs clean from a pack strap by its wire bail." },
  { id: "brass-compass",name: "Brass Baseplate Compass",  price: 46,  category: "Navigation",  icon: "compass",
    blurb: "Liquid-damped needle in a solid brass housing — no batteries, no signal required.",
    detail: "A sighting compass machined from solid brass, with a liquid-damped needle that settles in under two seconds. Etched declination scale on the bezel and a lanyard hole for quick access on a moving line." },
  { id: "aframe-tent",  name: "Canvas A-Frame Tent",      price: 310, category: "Shelter",     icon: "tent",
    blurb: "Two-person A-frame in breathable cotton canvas with a stitched moss-green floor.",
    detail: "The A-frame silhouette sheds wind better than a dome and breathes better than nylon, so you wake up dry inside instead of condensation-soaked. Fits two with gear, pitches with six stakes and two poles in about six minutes." },
  { id: "camp-knife",   name: "Folding Camp Knife",       price: 58,  category: "Tools",       icon: "knife",
    blurb: "Full-tang carbon blade, walnut scales, a half-stop lock you can feel.",
    detail: "A general-purpose folder for camp chores — kindling, cordage, the occasional trout. The 1095 carbon blade takes and holds an edge better than stainless; expect a light patina with use, which is normal and protective." },
  { id: "oil-lantern",  name: "Brass Oil Lantern",        price: 62,  category: "Light",       icon: "lantern",
    blurb: "A warm, windproof flame that needs no batteries and never needs charging.",
    detail: "This lantern runs on lamp oil or citronella and throws a steady, warm light that won't wreck your night vision the way an LED does. The globe is wind-guarded, so it stays lit through a stiff breeze at camp." },
  { id: "wool-blanket", name: "Merino Camp Blanket",      price: 85,  category: "Comfort",     icon: "blanket",
    blurb: "80% merino wool, whipstitched edge, warm even when it's damp.",
    detail: "Heavier than a synthetic throw and warmer for it — wool keeps insulating even when it's wet, which matters more than any spec sheet once the dew comes in. Doubles as a ground cloth or a saddle blanket in a pinch." },
  { id: "trail-maps",   name: "Regional Trail Map Set",   price: 18,  category: "Navigation",  icon: "map",
    blurb: "Waterproof-stock topographic set covering ridge, river, and backcountry routes.",
    detail: "Six waterproof-stock topo sheets at 1:24,000 scale, covering the main ridge trail, the river corridor, and connecting backcountry routes. Printed with UTM grid lines for use alongside a compass or GPS." },
];

function getIconMarkup(iconKey) {
  return ICONS[iconKey] || "";
}

function getProduct(id) {
  return PRODUCTS.find((p) => p.id === id) || null;
}

function getCategories() {
  return [...new Set(PRODUCTS.map((p) => p.category))].sort();
}

// ==== js/cart.js ====
// cart.js — cart state, persisted to localStorage, with a tiny pub/sub
// so any view (nav badge, cart page) can react to changes.



const STORAGE_KEY = "fernweh.cart.v1";
const listeners = new Set();

function load() {
  try {
    const raw = localStorage.getItem(STORAGE_KEY);
    return raw ? JSON.parse(raw) : {};
  } catch (e) {
    console.error("Cart failed to load, starting empty.", e);
    return {};
  }
}

let cart = load(); // { [productId]: quantity }

function persist() {
  try {
    localStorage.setItem(STORAGE_KEY, JSON.stringify(cart));
  } catch (e) {
    console.error("Cart failed to save.", e);
  }
  listeners.forEach((fn) => fn(getSummary()));
}

function onCartChange(fn) {
  listeners.add(fn);
  return () => listeners.delete(fn);
}

function addToCart(id, qty = 1) {
  cart[id] = (cart[id] || 0) + qty;
  persist();
}

function setQuantity(id, qty) {
  if (qty <= 0) {
    delete cart[id];
  } else {
    cart[id] = qty;
  }
  persist();
}

function removeFromCart(id) {
  delete cart[id];
  persist();
}

function clearCart() {
  cart = {};
  persist();
}

function getLineItems() {
  return Object.entries(cart)
    .map(([id, qty]) => {
      const product = getProduct(id);
      if (!product) return null;
      return { product, qty, lineTotal: product.price * qty };
    })
    .filter(Boolean);
}

function getSummary() {
  const items = getLineItems();
  const count = items.reduce((sum, i) => sum + i.qty, 0);
  const subtotal = items.reduce((sum, i) => sum + i.lineTotal, 0);
  return { items, count, subtotal };
}

// ==== js/router.js ====
// router.js — minimal hash router. Hash-based routing needs zero server
// configuration (no rewrites), which keeps this deployable on literally
// any static host with no build step.

const routes = [];

function registerRoute(pattern, render) {
  // pattern like "/shop" or "/product/:id"
  const paramNames = [];
  const regex = new RegExp(
    "^" +
      pattern.replace(/:[^/]+/g, (m) => {
        paramNames.push(m.slice(1));
        return "([^/]+)";
      }) +
      "$"
  );
  routes.push({ regex, paramNames, render });
}

function currentPath() {
  const hash = window.location.hash.slice(1); // drop '#'
  return hash === "" ? "/" : hash;
}

async function resolve(outlet) {
  const path = currentPath();
  for (const route of routes) {
    const match = path.match(route.regex);
    if (match) {
      const params = {};
      route.paramNames.forEach((name, i) => (params[name] = match[i + 1]));
      outlet.setAttribute("aria-busy", "true");
      await route.render(outlet, params);
      outlet.removeAttribute("aria-busy");
      window.scrollTo({ top: 0, behavior: "instant" in window ? "instant" : "auto" });
      updateActiveNav(path);
      return;
    }
  }
  // No match -> 404
  outlet.innerHTML = `
    <section class="not-found">
      <h1>404 — Off the map</h1>
      <p>That trail doesn't exist. <a href="#/">Head back to base camp.</a></p>
    </section>`;
}

function updateActiveNav(path) {
  document.querySelectorAll("[data-nav-link]").forEach((link) => {
    const target = link.getAttribute("href").replace("#", "") || "/";
    const isActive = target === path || (target === "/shop" && path.startsWith("/product/"));
    link.classList.toggle("active", isActive);
    if (isActive) link.setAttribute("aria-current", "page");
    else link.removeAttribute("aria-current");
  });
}

function startRouter(outlet) {
  window.addEventListener("hashchange", () => resolve(outlet));
  window.addEventListener("DOMContentLoaded", () => resolve(outlet));
  if (document.readyState !== "loading") resolve(outlet);
}

// ==== js/views.js ====
// views.js — one render function per route. Each takes the outlet
// element and writes markup into it; event listeners are attached
// after render since the DOM is replaced wholesale each navigation.




const money = (n) => `$${n.toFixed(2)}`;

function escapeHtml(str) {
  const div = document.createElement("div");
  div.textContent = str;
  return div.innerHTML;
}

function productCard(p) {
  return `
    <article class="product-card">
      <a class="product-media" href="#/product/${p.id}" aria-hidden="true" tabindex="-1">${getIconMarkup(p.icon)}</a>
      <div class="product-body">
        <p class="product-eyebrow">${p.category}</p>
        <h3><a href="#/product/${p.id}">${p.name}</a></h3>
        <p class="product-blurb">${p.blurb}</p>
        <div class="product-foot">
          <span class="price">${money(p.price)}</span>
          <button type="button" class="btn btn-small" data-add="${p.id}">Add to pack</button>
        </div>
      </div>
    </article>`;
}

function wireAddButtons(root) {
  root.querySelectorAll("[data-add]").forEach((btn) => {
    btn.addEventListener("click", () => {
      addToCart(btn.dataset.add, 1);
      const original = btn.textContent;
      btn.textContent = "Added ✓";
      btn.disabled = true;
      setTimeout(() => {
        btn.textContent = original;
        btn.disabled = false;
      }, 900);
    });
  });
}

function renderHome(outlet) {
  const featured = PRODUCTS.slice(0, 3);
  outlet.innerHTML = `
    <section class="hero">
      <p class="eyebrow">Fernweh Supply Co. — outfitting since the first cold morning</p>
      <h1>Gear that earns its weight in the pack.</h1>
      <p class="hero-sub">No batteries to charge, no plastic that cracks in the cold. Just canvas, brass,
        cast iron, and wool — chosen because they still work when the trip goes sideways.</p>
      <div class="cta-row">
        <a class="btn" href="#/shop">Browse the catalog</a>
        <a class="btn btn-ghost" href="#/about">Our story</a>
      </div>
    </section>

    <section class="section" aria-labelledby="featured-title">
      <div class="section-head">
        <h2 id="featured-title">Field-tested favorites</h2>
        <a href="#/shop" class="text-link">See everything →</a>
      </div>
      <div class="product-grid">${featured.map(productCard).join("")}</div>
    </section>

    <section class="section band" aria-labelledby="promise-title">
      <h2 id="promise-title">The Fernweh promise</h2>
      <div class="promise-grid">
        <div class="promise-item"><h3>Repairable, not replaceable</h3><p>Every stitch, rivet, and hinge is serviceable — we'll tell you how, or do it for you.</p></div>
        <div class="promise-item"><h3>Materials over marketing</h3><p>Waxed canvas, brass, cast iron, wool. Nothing here needs a firmware update.</p></div>
        <div class="promise-item"><h3>Made to be used hard</h3><p>We test everything on our own trips before it goes in the catalog.</p></div>
      </div>
    </section>`;
  wireAddButtons(outlet);
}

function renderShop(outlet) {
  const categories = getCategories();
  outlet.innerHTML = `
    <section class="shop-head">
      <h1>The Catalog</h1>
      <p class="hero-sub">${PRODUCTS.length} pieces of gear, sorted by what they're for.</p>
      <div class="shop-controls">
        <input type="search" id="shopSearch" placeholder="Search the catalog…" aria-label="Search products">
        <div class="chip-row" id="categoryChips">
          <button type="button" class="chip active" data-cat="all">All</button>
          ${categories.map((c) => `<button type="button" class="chip" data-cat="${c}">${c}</button>`).join("")}
        </div>
      </div>
    </section>
    <div class="product-grid" id="shopGrid"></div>`;

  const grid = outlet.querySelector("#shopGrid");
  const searchEl = outlet.querySelector("#shopSearch");
  const chipsEl = outlet.querySelector("#categoryChips");
  let activeCat = "all";

  function paint() {
    const q = searchEl.value.trim().toLowerCase();
    const filtered = PRODUCTS.filter((p) => {
      const matchesCat = activeCat === "all" || p.category === activeCat;
      const matchesQuery = !q || p.name.toLowerCase().includes(q) || p.blurb.toLowerCase().includes(q);
      return matchesCat && matchesQuery;
    });
    grid.innerHTML = filtered.length
      ? filtered.map(productCard).join("")
      : `<p class="empty-note">Nothing matches that search. Try another term or clear the filter.</p>`;
    wireAddButtons(grid);
  }

  searchEl.addEventListener("input", paint);
  chipsEl.addEventListener("click", (e) => {
    const btn = e.target.closest(".chip");
    if (!btn) return;
    activeCat = btn.dataset.cat;
    chipsEl.querySelectorAll(".chip").forEach((c) => c.classList.toggle("active", c === btn));
    paint();
  });

  paint();
}

function renderProduct(outlet, params) {
  const product = getProduct(params.id);
  if (!product) {
    outlet.innerHTML = `<section class="not-found"><h1>404 — Item not found</h1><p><a href="#/shop">Back to the catalog</a></p></section>`;
    return;
  }
  outlet.innerHTML = `
    <section class="product-detail">
      <a href="#/shop" class="text-link back-link">← Back to catalog</a>
      <div class="product-detail-grid">
        <div class="product-detail-media">${getIconMarkup(product.icon)}</div>
        <div class="product-detail-body">
          <p class="product-eyebrow">${product.category}</p>
          <h1>${product.name}</h1>
          <p class="price price-lg">${money(product.price)}</p>
          <p class="product-detail-text">${product.detail}</p>
          <div class="qty-row">
            <label for="qtyInput">Quantity</label>
            <input type="number" id="qtyInput" min="1" value="1" inputmode="numeric">
          </div>
          <button type="button" class="btn" id="addDetailBtn">Add to pack</button>
        </div>
      </div>
    </section>`;

  outlet.querySelector("#addDetailBtn").addEventListener("click", () => {
    const qty = Math.max(1, parseInt(outlet.querySelector("#qtyInput").value, 10) || 1);
    addToCart(product.id, qty);
    const btn = outlet.querySelector("#addDetailBtn");
    btn.textContent = "Added to pack ✓";
    setTimeout(() => (btn.textContent = "Add to pack"), 1100);
  });
}

function renderCart(outlet) {
  paintCart();

  function paintCart() {
    const { items, subtotal } = getSummary();

    if (items.length === 0) {
      outlet.innerHTML = `
        <section class="cart-empty">
          <h1>Your pack is empty</h1>
          <p>Nothing in here yet. <a href="#/shop">Go find something worth carrying.</a></p>
        </section>`;
      return;
    }

    outlet.innerHTML = `
      <section class="cart-page">
        <h1>Your Pack</h1>
        <div class="cart-list" role="list">
          ${items
            .map(
              (i) => `
            <div class="cart-line" role="listitem" data-id="${i.product.id}">
              <div class="cart-line-media">${getIconMarkup(i.product.icon)}</div>
              <div class="cart-line-body">
                <h3><a href="#/product/${i.product.id}">${i.product.name}</a></h3>
                <p class="product-eyebrow">${i.product.category}</p>
              </div>
              <div class="cart-line-qty">
                <button type="button" class="icon-btn" data-decr="${i.product.id}" aria-label="Decrease quantity">−</button>
                <span aria-live="polite">${i.qty}</span>
                <button type="button" class="icon-btn" data-incr="${i.product.id}" aria-label="Increase quantity">+</button>
              </div>
              <div class="cart-line-total">${money(i.lineTotal)}</div>
              <button type="button" class="icon-btn delete" data-remove="${i.product.id}" aria-label="Remove ${escapeHtml(i.product.name)}">remove</button>
            </div>`
            )
            .join("")}
        </div>
        <div class="cart-summary">
          <div class="cart-summary-row"><span>Subtotal</span><span>${money(subtotal)}</span></div>
          <p class="cart-note">Shipping and taxes calculated at checkout.</p>
          <div class="cart-actions">
            <button type="button" class="btn" id="checkoutBtn">Checkout</button>
            <button type="button" class="btn btn-ghost" id="clearCartBtn">Empty pack</button>
          </div>
        </div>
      </section>`;

    outlet.querySelectorAll("[data-incr]").forEach((b) =>
      b.addEventListener("click", () => {
        const items2 = getLineItems();
        const line = items2.find((i) => i.product.id === b.dataset.incr);
        setQuantity(b.dataset.incr, (line?.qty || 0) + 1);
        paintCart();
      })
    );
    outlet.querySelectorAll("[data-decr]").forEach((b) =>
      b.addEventListener("click", () => {
        const items2 = getLineItems();
        const line = items2.find((i) => i.product.id === b.dataset.decr);
        setQuantity(b.dataset.decr, (line?.qty || 0) - 1);
        paintCart();
      })
    );
    outlet.querySelectorAll("[data-remove]").forEach((b) =>
      b.addEventListener("click", () => {
        removeFromCart(b.dataset.remove);
        paintCart();
      })
    );
    outlet.querySelector("#clearCartBtn")?.addEventListener("click", () => {
      clearCart();
      paintCart();
    });
    outlet.querySelector("#checkoutBtn")?.addEventListener("click", () => {
      const orderId = "FW-" + Math.random().toString(36).slice(2, 8).toUpperCase();
      const total = getSummary().subtotal;
      clearCart();
      outlet.innerHTML = `
        <section class="confirm">
          <h1>Order placed</h1>
          <p class="confirm-id">Confirmation ${orderId}</p>
          <p>Total charged: ${money(total)}. This is a demo checkout — no payment was processed and no
          real order was placed, but that's exactly the flow a live storefront would use.</p>
          <a class="btn" href="#/shop">Keep browsing</a>
        </section>`;
    });
  }
}

function renderAbout(outlet) {
  outlet.innerHTML = `
    <section class="about-page">
      <h1>Built for the long way round</h1>
      <p class="hero-sub">Fernweh Supply Co. started as one duffel of gear that refused to fail on a
        three-week ridge walk. Ten years later, we still only sell what we'd carry ourselves.</p>
      <div class="promise-grid">
        <div class="promise-item"><h3>Small runs</h3><p>Each piece is made in batches small enough that we know who sewed it.</p></div>
        <div class="promise-item"><h3>Honest materials</h3><p>Waxed cotton, brass, cast iron, full-grain leather, wool — nothing that turns to microplastic in a river.</p></div>
        <div class="promise-item"><h3>A repair, not a return</h3><p>If it breaks, we fix it. Most of our gear outlives the trip it was bought for.</p></div>
      </div>
    </section>`;
}

function renderContact(outlet) {
  outlet.innerHTML = `
    <section class="contact-page">
      <h1>Get in touch</h1>
      <p class="hero-sub">Questions about an order, a repair, or gear for a specific trip — write in.</p>
      <form id="contactForm" class="contact-form" novalidate>
        <div class="field">
          <label for="cName">Name</label>
          <input type="text" id="cName" name="name" required autocomplete="name">
          <p class="field-error" data-error-for="cName"></p>
        </div>
        <div class="field">
          <label for="cEmail">Email</label>
          <input type="email" id="cEmail" name="email" required autocomplete="email">
          <p class="field-error" data-error-for="cEmail"></p>
        </div>
        <div class="field">
          <label for="cMessage">Message</label>
          <textarea id="cMessage" name="message" rows="5" required></textarea>
          <p class="field-error" data-error-for="cMessage"></p>
        </div>
        <button type="submit" class="btn">Send message</button>
        <p class="form-status" id="formStatus" role="status" aria-live="polite"></p>
      </form>
    </section>`;

  const form = outlet.querySelector("#contactForm");
  form.addEventListener("submit", (e) => {
    e.preventDefault();
    let valid = true;
    const fields = [
      { id: "cName", msg: "Tell us your name." },
      { id: "cEmail", msg: "Enter a valid email address." },
      { id: "cMessage", msg: "Add a short message." },
    ];
    fields.forEach(({ id, msg }) => {
      const input = outlet.querySelector("#" + id);
      const errorEl = outlet.querySelector(`[data-error-for="${id}"]`);
      const ok = input.checkValidity() && input.value.trim().length > 0;
      errorEl.textContent = ok ? "" : msg;
      input.setAttribute("aria-invalid", ok ? "false" : "true");
      if (!ok) valid = false;
    });
    const status = outlet.querySelector("#formStatus");
    if (!valid) {
      status.textContent = "Please fix the highlighted fields.";
      status.className = "form-status error";
      return;
    }
    status.textContent = "Message sent — this demo form doesn't have a live backend yet, but the validation and flow are ready to wire up.";
    status.className = "form-status success";
    form.reset();
  });
}

// ==== js/app.js ====
// app.js — composition root. Registers routes, boots the router,
// and keeps the nav cart badge in sync with cart state.





const outlet = document.getElementById("view");
const badge = document.getElementById("cartBadge");
const navToggle = document.getElementById("navToggle");
const nav = document.getElementById("primaryNav");

registerRoute("/", renderHome);
registerRoute("/shop", renderShop);
registerRoute("/product/:id", renderProduct);
registerRoute("/cart", renderCart);
registerRoute("/about", renderAbout);
registerRoute("/contact", renderContact);

startRouter(outlet);

function paintBadge(summary) {
  badge.textContent = summary.count;
  badge.style.display = summary.count > 0 ? "inline-flex" : "none";
}
paintBadge(getSummary());
onCartChange(paintBadge);

// Mobile nav toggle
navToggle.addEventListener("click", () => {
  const open = nav.classList.toggle("open");
  navToggle.setAttribute("aria-expanded", String(open));
});
nav.addEventListener("click", (e) => {
  if (e.target.matches("a")) {
    nav.classList.remove("open");
    navToggle.setAttribute("aria-expanded", "false");
  }
});

</script>
</body>
</html>
