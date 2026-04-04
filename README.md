# Lost-Soul-Art-Studio-
Html website
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Lost Soul Art Studio | Roberto Cisneros | San Francisco Contemporary Surrealist Artist</title>

  <!-- \u2550\u2550 SEO \u2550\u2550 -->
  <meta name="description" content="Lost Soul Art Studio \u2014 Fine art portraits, contemporary surrealism, interior murals, and storefront installations by Roberto Cisneros. San Francisco's premier surrealist artist. Commission custom work or shop limited edition archival prints.">
  <meta name="keywords" content="Lost Soul Art, Roberto Cisneros, San Francisco artist, contemporary surrealism, fine art portraits, interior murals, storefront art, custom portraits, art prints, Bay Area artist, SF mural artist, Mission District art, urban surrealism">
  <meta name="author" content="Roberto Cisneros \u2014 Lost Soul Art Studio">
  <meta name="robots" content="index, follow">
  <link rel="canonical" href="https://lostsoulart.com">

  <!-- \u2550\u2550 Open Graph \u2550\u2550 -->
  <meta property="og:title" content="Lost Soul Art Studio | Roberto Cisneros | San Francisco">
  <meta property="og:description" content="Fine art portraits, contemporary surrealism, and murals. San Francisco's premier urban surrealist artist. Commission originals or shop limited edition prints.">
  <meta property="og:image" content="https://lostsoulart.simdif.com/images/public/sd_69c8652c43062.jpg">
  <meta property="og:url" content="https://lostsoulart.com">
  <meta property="og:type" content="website">
  <meta property="og:site_name" content="Lost Soul Art Studio">

  <!-- \u2550\u2550 Twitter Card \u2550\u2550 -->
  <meta name="twitter:card" content="summary_large_image">
  <meta name="twitter:title" content="Lost Soul Art Studio | Roberto Cisneros">
  <meta name="twitter:description" content="Contemporary surrealism rooted in the urban soul of San Francisco.">
  <meta name="twitter:image" content="https://lostsoulart.simdif.com/images/public/sd_69c8652c43062.jpg">

  <!-- \u2550\u2550 Schema.org Local Business \u2550\u2550 -->
  <script type="application/ld+json">
  {
    "@context": "https://schema.org",
    "@type": ["LocalBusiness", "ArtGallery"],
    "name": "Lost Soul Art Studio",
    "description": "Fine art portraits, contemporary surrealism, interior murals, and storefront installations by Roberto Cisneros.",
    "url": "https://lostsoulart.com",
    "image": "https://lostsoulart.simdif.com/images/public/sd_69c8652c43062.jpg",
    "priceRange": "$$$",
    "address": {
      "@type": "PostalAddress",
      "addressLocality": "San Francisco",
      "addressRegion": "CA",
      "addressCountry": "US"
    },
    "founder": { "@type": "Person", "name": "Roberto Cisneros" },
    "sameAs": [
      "https://www.instagram.com/lostsoulartSF",
      "https://www.facebook.com/lostsoulart"
    ]
  }
  </script>

  <!-- \u2550\u2550 Fonts \u2550\u2550 -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,600;1,300;1,400&family=Bebas+Neue&family=Raleway:wght@300;400;500;600&display=swap" rel="stylesheet">

  <!-- \u2550\u2550 Icons \u2550\u2550 -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css">

<style>
/* \u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550
   DESIGN SYSTEM
\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550 */
:root {
  --black:      #080808;
  --deep:       #101010;
  --charcoal:   #181818;
  --smoke:      #202020;
  --gold:       #c9a84c;
  --gold-lt:    #e8c97a;
  --gold-pale:  #f5e6c0;
  --white:      #f0ece4;
  --muted:      #777;
  --border:     rgba(201,168,76,.18);
  --display:    'Bebas Neue', sans-serif;
  --serif:      'Cormorant Garamond', serif;
  --sans:       'Raleway', sans-serif;
  --ease:       cubic-bezier(.25,.46,.45,.94);
}

*,*::before,*::after { box-sizing:border-box; margin:0; padding:0; }
html { scroll-behavior:smooth; }

body {
  background: var(--black);
  color: var(--white);
  font-family: var(--serif);
  font-size: 18px;
  line-height: 1.7;
  overflow-x: hidden;
}

/* \u2500\u2500 Scrollbar \u2500\u2500 */
::-webkit-scrollbar { width:5px; }
::-webkit-scrollbar-track { background:var(--black); }
::-webkit-scrollbar-thumb { background:var(--gold); border-radius:3px; }

/* \u2500\u2500 Utilities \u2500\u2500 */
.gold { color:var(--gold); }
.container { max-width:1380px; margin:0 auto; padding:0 4rem; }
section { padding:8rem 0; }

.section-label {
  display:block;
  font-family:var(--sans);
  font-size:10px;
  letter-spacing:.5em;
  text-transform:uppercase;
  color:var(--gold);
  margin-bottom:1rem;
}

/* \u2500\u2500 Buttons \u2500\u2500 */
.btn-gold {
  display:inline-block;
  font-family:var(--sans);
  font-size:10px;
  letter-spacing:.35em;
  text-transform:uppercase;
  font-weight:600;
  background:var(--gold);
  color:var(--black);
  padding:1rem 2.8rem;
  text-decoration:none;
  border:none;
  cursor:pointer;
  transition:background .3s var(--ease), transform .3s var(--ease);
}
.btn-gold:hover { background:var(--gold-lt); transform:translateY(-2px); }

.btn-outline {
  display:inline-block;
  font-family:var(--sans);
  font-size:10px;
  letter-spacing:.35em;
  text-transform:uppercase;
  font-weight:500;
  background:transparent;
  color:var(--white);
  padding:1rem 2.8rem;
  text-decoration:none;
  border:1px solid rgba(240,236,228,.3);
  cursor:pointer;
  transition:border-color .3s, color .3s;
}
.btn-outline:hover { border-color:var(--gold); color:var(--gold); }

/* \u2500\u2500 Reveal animations \u2500\u2500 */
.reveal {
  opacity:0;
  transform:translateY(45px);
  transition:opacity .8s var(--ease), transform .8s var(--ease);
}
.reveal.on { opacity:1; transform:translateY(0); }
.d1 { transition-delay:.1s; }
.d2 { transition-delay:.2s; }
.d3 { transition-delay:.3s; }
.d4 { transition-delay:.4s; }

/* \u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550
   NAVIGATION
\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550 */
#nav {
  position:fixed;
  inset:0 0 auto;
  z-index:900;
  display:flex;
  align-items:center;
  justify-content:space-between;
  padding:1.8rem 4rem;
  transition:padding .4s var(--ease), background .4s;
}
#nav.solid {
  background:rgba(8,8,8,.96);
  backdrop-filter:blur(24px);
  padding:1rem 4rem;
  border-bottom:1px solid var(--border);
}

.nav-logo {
  font-family:var(--display);
  font-size:1.9rem;
  letter-spacing:.1em;
  color:var(--white);
  text-decoration:none;
}
.nav-logo em { color:var(--gold); font-style:normal; }

.nav-links {
  display:flex;
  gap:2.5rem;
  list-style:none;
}
.nav-links a {
  font-family:var(--sans);
  font-size:10px;
  letter-spacing:.3em;
  text-transform:uppercase;
  color:var(--white);
  text-decoration:none;
  position:relative;
  transition:color .3s;
}
.nav-links a::after {
  content:'';
  position:absolute;
  bottom:-4px;
  left:0; width:0; height:1px;
  background:var(--gold);
  transition:width .35s var(--ease);
}
.nav-links a:hover { color:var(--gold); }
.nav-links a:hover::after { width:100%; }

.nav-right { display:flex; gap:1rem; align-items:center; }

.cart-btn {
  font-family:var(--sans);
  font-size:10px;
  letter-spacing:.25em;
  text-transform:uppercase;
  background:transparent;
  border:1px solid var(--gold);
  color:var(--gold);
  padding:.55rem 1.4rem;
  cursor:pointer;
  transition:all .3s;
  position:relative;
}
.cart-btn:hover { background:var(--gold); color:var(--black); }
.cart-badge {
  position:absolute;
  top:-9px; right:-9px;
  background:var(--gold);
  color:var(--black);
  width:18px; height:18px;
  border-radius:50%;
  font-size:9px; font-weight:700;
  display:none;
  align-items:center;
  justify-content:center;
}

/* Hamburger */
.hamburger {
  display:none;
  flex-direction:column;
  gap:5px;
  background:none;
  border:none;
  cursor:pointer;
  padding:4px;
}
.hamburger span {
  display:block;
  width:26px; height:1px;
  background:var(--white);
  transition:all .3s;
}

/* Mobile Drawer */
.mobile-drawer {
  display:none;
  position:fixed;
  inset:0;
  background:var(--black);
  z-index:800;
  flex-direction:column;
  align-items:center;
  justify-content:center;
  gap:2.5rem;
}
.mobile-drawer.show { display:flex; }
.mobile-drawer a {
  font-family:var(--display);
  font-size:3.5rem;
  letter-spacing:.08em;
  color:var(--white);
  text-decoration:none;
  transition:color .3s;
}
.mobile-drawer a:hover { color:var(--gold); }

/* \u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550
   HERO
\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550 */
#hero {
  height:100vh;
  min-height:700px;
  position:relative;
  display:flex;
  align-items:center;
  justify-content:center;
  overflow:hidden;
}

.hero-bg {
  position:absolute; inset:0;
  background:url('https://lostsoulart.simdif.com/images/public/sd_69c8652c43062.jpg') center/cover;
  filter:brightness(.28) contrast(1.1);
  transform:scale(1.06);
  animation:bgDrift 22s ease-in-out infinite alternate;
}
@keyframes bgDrift {
  from { transform:scale(1.06) translateX(0); }
  to   { transform:scale(1.0)  translateX(-1%); }
}

.hero-vignette {
  position:absolute; inset:0;
  background:radial-gradient(ellipse at center, transparent 30%, rgba(8,8,8,.7) 100%);
  pointer-events:none;
}
.hero-fade {
  position:absolute; bottom:0; left:0; right:0; height:40%;
  background:linear-gradient(to bottom, transparent, var(--black));
}

.hero-body {
  position:relative; z-index:2;
  text-align:center;
  padding:0 2rem;
}

.hero-eye {
  font-family:var(--sans);
  font-size:10px;
  letter-spacing:.7em;
  text-transform:uppercase;
  color:var(--gold);
  opacity:0;
  animation:riseIn 1s var(--ease) forwards .4s;
}

.hero-h1 {
  font-family:var(--display);
  font-size:clamp(5rem,13vw,13rem);
  line-height:.9;
  letter-spacing:.04em;
  opacity:0;
  animation:riseIn 1s var(--ease) forwards .75s;
}
.hero-h1 .cursive {
  display:block;
  font-family:var(--serif);
  font-style:italic;
  font-weight:300;
  font-size:clamp(2.5rem,6vw,6.5rem);
  color:var(--gold);
  letter-spacing:.06em;
  margin-top:.4rem;
}

.hero-sub {
  font-family:var(--serif);
  font-style:italic;
  font-size:1.15rem;
  color:rgba(240,236,228,.6);
  margin-top:1.5rem;
  opacity:0;
  animation:riseIn 1s var(--ease) forwards 1.05s;
}

.hero-ctas {
  display:flex;
  gap:1.2rem;
  justify-content:center;
  margin-top:3rem;
  opacity:0;
  animation:riseIn 1s var(--ease) forwards 1.3s;
}

@keyframes riseIn {
  from { opacity:0; transform:translateY(28px); }
  to   { opacity:1; transform:translateY(0); }
}

.hero-scroll {
  position:absolute;
  bottom:2.5rem; left:50%;
  transform:translateX(-50%);
  z-index:2;
  display:flex;
  flex-direction:column;
  align-items:center;
  gap:.5rem;
  opacity:0;
  animation:riseIn 1s forwards 2s;
}
.hero-scroll span {
  font-family:var(--sans);
  font-size:8px;
  letter-spacing:.5em;
  text-transform:uppercase;
  color:var(--muted);
}
.scroll-bar {
  width:1px; height:55px;
  background:linear-gradient(to bottom, var(--gold), transparent);
  animation:pulse 2.2s ease-in-out infinite;
}
@keyframes pulse {
  0%,100% { opacity:.35; transform:scaleY(1); }
  50%      { opacity:1;   transform:scaleY(1.12); }
}

/* \u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550
   MARQUEE
\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550 */
.marquee-wrap {
  background:var(--gold);
  overflow:hidden;
  padding:.9rem 0;
}
.marquee-inner {
  display:flex;
  animation:ticker 28s linear infinite;
  white-space:nowrap;
}
.marquee-inner span {
  font-family:var(--display);
  font-size:1.1rem;
  letter-spacing:.18em;
  color:var(--black);
  padding:0 2.5rem;
}
@keyframes ticker {
  from { transform:translateX(0); }
  to   { transform:translateX(-50%); }
}

/* \u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550
   ABOUT
\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550 */
#about {
  background:var(--deep);
  position:relative;
  overflow:hidden;
}
#about::before {
  content:'LOST';
  position:absolute;
  right:-5%;
  top:50%;
  transform:translateY(-50%);
  font-family:var(--display);
  font-size:25vw;
  color:rgba(201,168,76,.025);
  pointer-events:none;
  line-height:1;
}

.about-grid {
  display:grid;
  grid-template-columns:1fr 1.1fr;
  gap:6rem;
  align-items:center;
}

.portrait-frame {
  position:relative;
}
.portrait-frame::before {
  content:'';
  position:absolute;
  top:-18px; left:-18px;
  right:18px; bottom:18px;
  border:1px solid var(--border);
  z-index:0;
  transition:all .6s;
}
.portrait-frame:hover::before {
  top:-24px; left:-24px;
  right:24px; bottom:24px;
}
.portrait-frame img {
  width:100%;
  display:block;
  position:relative;
  z-index:1;
  filter:grayscale(15%) contrast(1.08);
}

.about-txt h2 {
  font-family:var(--display);
  font-size:clamp(3rem,5.5vw,6.5rem);
  line-height:.95;
  margin-bottom:1.5rem;
}
.about-pull {
  border-left:2px solid var(--gold);
  padding-left:1.5rem;
  margin:1.8rem 0;
  font-style:italic;
  font-size:1.3rem;
  color:var(--gold-pale);
  line-height:1.5;
}
.about-txt p {
  color:rgba(240,236,228,.72);
  font-size:1.05rem;
  margin-bottom:1.2rem;
}

.stats {
  display:flex;
  gap:3rem;
  margin-top:2.5rem;
}
.stat-n {
  font-family:var(--display);
  font-size:3.8rem;
  color:var(--gold);
  line-height:1;
}
.stat-l {
  font-family:var(--sans);
  font-size:9px;
  letter-spacing:.35em;
  text-transform:uppercase;
  color:var(--muted);
}

/* \u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550
   SERVICES
\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550 */
#services { background:var(--black); }

.services-hd {
  text-align:center;
  margin-bottom:5rem;
}
.services-hd h2 {
  font-family:var(--display);
  font-size:clamp(3rem,7vw,8rem);
  line-height:1;
}

.svc-grid {
  display:grid;
  grid-template-columns:repeat(4,1fr);
  gap:2px;
}
.svc-card {
  background:var(--charcoal);
  padding:3rem 2rem;
  text-align:center;
  border-top:2px solid transparent;
  transition:all .4s var(--ease);
  cursor:default;
}
.svc-card:hover {
  background:var(--smoke);
  border-top-color:var(--gold);
  transform:translateY(-6px);
}
.svc-icon {
  font-size:2.2rem;
  color:var(--gold);
  margin-bottom:1.5rem;
}
.svc-card h3 {
  font-family:var(--display);
  font-size:1.8rem;
  letter-spacing:.05em;
  margin-bottom:.8rem;
}
.svc-card p {
  font-size:.95rem;
  color:var(--muted);
  line-height:1.65;
  margin-bottom:1.5rem;
}
.svc-price {
  font-family:var(--display);
  font-size:1.6rem;
  color:var(--gold);
  margin-bottom:1rem;
}
.svc-link {
  font-family:var(--sans);
  font-size:9px;
  letter-spacing:.35em;
  text-transform:uppercase;
  color:var(--gold);
  text-decoration:none;
  border-bottom:1px solid var(--border);
  padding-bottom:2px;
  transition:border-color .3s;
}
.svc-link:hover { border-color:var(--gold); }

/* \u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550
   GALLERY
\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550 */
#gallery { background:var(--deep); }

.gallery-hd {
  text-align:center;
  margin-bottom:3.5rem;
}
.gallery-hd h2 {
  font-family:var(--display);
  font-size:clamp(3rem,7vw,8rem);
  line-height:1;
}

.filter-row {
  display:flex;
  gap:.8rem;
  justify-content:center;
  flex-wrap:wrap;
  margin-bottom:3rem;
}
.f-btn {
  font-family:var(--sans);
  font-size:9px;
  letter-spacing:.35em;
  text-transform:uppercase;
  background:transparent;
  border:1px solid var(--border);
  color:var(--muted);
  padding:.55rem 1.5rem;
  cursor:pointer;
  transition:all .3s;
}
.f-btn.on, .f-btn:hover {
  border-color:var(--gold);
  color:var(--gold);
}

.masonry {
  columns:4;
  column-gap:10px;
}
.g-item {
  break-inside:avoid;
  margin-bottom:10px;
  position:relative;
  overflow:hidden;
  cursor:pointer;
}
.g-item img {
  width:100%;
  display:block;
  transition:transform .7s var(--ease);
  filter:contrast(1.05);
}
.g-item:hover img { transform:scale(1.09); }

.g-overlay {
  position:absolute; inset:0;
  background:linear-gradient(to top, rgba(8,8,8,.88) 0%, transparent 55%);
  opacity:0;
  transition:opacity .4s;
  display:flex;
  align-items:flex-end;
  padding:1rem 1.2rem;
}
.g-item:hover .g-overlay { opacity:1; }
.g-label {
  font-family:var(--sans);
  font-size:9px;
  letter-spacing:.25em;
  text-transform:uppercase;
}

/* \u2500\u2500 Lightbox \u2500\u2500 */
.lbox {
  display:none;
  position:fixed; inset:0;
  background:rgba(0,0,0,.96);
  z-index:2000;
  align-items:center;
  justify-content:center;
}
.lbox.on { display:flex; }
.lbox-inner {
  position:relative;
  display:flex;
  align-items:center;
  gap:1.5rem;
}
.lbox-img {
  max-width:78vw;
  max-height:85vh;
  object-fit:contain;
  display:block;
}
.lbox-x {
  position:absolute;
  top:-2.5rem; right:0;
  background:none; border:none;
  color:var(--muted); font-size:1.4rem;
  cursor:pointer;
  transition:color .3s;
}
.lbox-x:hover { color:var(--gold); }
.lbox-cap {
  position:absolute;
  bottom:-2.5rem; left:0; right:0;
  text-align:center;
  font-family:var(--display);
  font-size:1.4rem;
  color:var(--gold);
}
.lbox-nav {
  background:none;
  border:1px solid var(--border);
  color:var(--white);
  width:48px; height:48px;
  font-size:1.4rem;
  cursor:pointer;
  transition:all .3s;
  flex-shrink:0;
}
.lbox-nav:hover { border-color:var(--gold); color:var(--gold); }

/* \u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550
   PRINT SHOP
\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550 */
#shop { background:var(--black); }

.shop-hd {
  text-align:center;
  margin-bottom:5rem;
}
.shop-hd h2 {
  font-family:var(--display);
  font-size:clamp(3rem,7vw,8rem);
  line-height:1;
}
.shop-hd p {
  color:var(--muted);
  font-style:italic;
  max-width:480px;
  margin:1rem auto 0;
}

.shop-grid {
  display:grid;
  grid-template-columns:repeat(3,1fr);
  gap:1.8rem;
}

.s-card {
  background:var(--charcoal);
  border:1px solid var(--border);
  position:relative;
  overflow:hidden;
  transition:all .4s var(--ease);
}
.s-card:hover {
  border-color:var(--gold);
  transform:translateY(-6px);
  box-shadow:0 24px 64px rgba(201,168,76,.09);
}

.s-badge {
  position:absolute;
  top:.9rem; right:.9rem;
  background:var(--gold);
  color:var(--black);
  font-family:var(--sans);
  font-size:8px;
  letter-spacing:.2em;
  text-transform:uppercase;
  font-weight:700;
  padding:.25rem .75rem;
  z-index:2;
}

.s-img {
  aspect-ratio:4/3;
  overflow:hidden;
}
.s-img img {
  width:100%; height:100%;
  object-fit:cover;
  transition:transform .7s var(--ease);
}
.s-card:hover .s-img img { transform:scale(1.09); }

.s-body { padding:1.4rem 1.4rem .8rem; }
.s-body h3 {
  font-family:var(--display);
  font-size:1.55rem;
  letter-spacing:.04em;
  margin-bottom:.3rem;
}
.s-meta {
  font-family:var(--sans);
  font-size:9px;
  letter-spacing:.25em;
  text-transform:uppercase;
  color:var(--muted);
  margin-bottom:1rem;
}

.size-row { display:flex; gap:.45rem; flex-wrap:wrap; margin-bottom:.5rem; }
.sz {
  font-family:var(--sans);
  font-size:9px;
  letter-spacing:.1em;
  background:transparent;
  border:1px solid var(--border);
  color:var(--muted);
  padding:.28rem .6rem;
  cursor:pointer;
  transition:all .3s;
}
.sz.on, .sz:hover { border-color:var(--gold); color:var(--gold); }

.s-foot {
  display:flex;
  align-items:center;
  justify-content:space-between;
  padding:.8rem 1.4rem 1.2rem;
  border-top:1px solid var(--border);
  margin-top:.5rem;
}
.s-price {
  font-family:var(--display);
  font-size:2rem;
  color:var(--gold);
}
.atc-btn {
  font-family:var(--sans);
  font-size:9px;
  letter-spacing:.3em;
  text-transform:uppercase;
  font-weight:700;
  background:var(--gold);
  color:var(--black);
  border:none;
  padding:.7rem 1.5rem;
  cursor:pointer;
  transition:background .3s;
}
.atc-btn:hover { background:var(--gold-lt); }

/* \u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550
   COLLECTOR BUNDLES
\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550 */
#bundles { background:var(--charcoal); }

.bundles-hd {
  text-align:center;
  margin-bottom:4.5rem;
}
.bundles-hd h2 {
  font-family:var(--display);
  font-size:clamp(2.5rem,5.5vw,7rem);
  line-height:1;
}

.bundle-grid {
  display:grid;
  grid-template-columns:repeat(3,1fr);
  gap:2px;
}
.b-card {
  background:var(--deep);
  padding:3rem 2.5rem;
  text-align:center;
  border-top:3px solid transparent;
  position:relative;
  transition:all .4s var(--ease);
}
.b-card.star { border-top-color:var(--gold); background:var(--smoke); }
.b-card:hover { border-top-color:var(--gold); }

.b-pill {
  position:absolute;
  top:-13px; left:50%;
  transform:translateX(-50%);
  background:var(--gold);
  color:var(--black);
  font-family:var(--sans);
  font-size:8px;
  letter-spacing:.25em;
  text-transform:uppercase;
  font-weight:700;
  padding:.28rem 1.1rem;
  white-space:nowrap;
}

.b-name {
  font-family:var(--display);
  font-size:2.8rem;
  color:var(--gold);
  margin-bottom:.3rem;
}
.b-save {
  font-family:var(--sans);
  font-size:9px;
  letter-spacing:.3em;
  text-transform:uppercase;
  color:var(--muted);
  margin-bottom:2rem;
}

.b-list { list-style:none; margin-bottom:2.5rem; text-align:left; }
.b-list li {
  padding:.55rem 0;
  border-bottom:1px solid var(--border);
  font-size:.95rem;
  display:flex;
  gap:.8rem;
  align-items:center;
  color:rgba(240,236,228,.78);
}
.b-list li i { color:var(--gold); font-size:.75rem; }

/* \u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550
   TESTIMONIALS
\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550 */
#testimonials { background:var(--deep); overflow:hidden; }

.testi-hd { text-align:center; margin-bottom:4.5rem; }
.testi-hd h2 {
  font-family:var(--display);
  font-size:clamp(2.5rem,5.5vw,7rem);
  line-height:1;
}

.testi-row { display:flex; gap:1.8rem; }

.t-card {
  background:var(--charcoal);
  border:1px solid var(--border);
  padding:2.8rem;
  min-width:390px;
  flex-shrink:0;
  position:relative;
  transition:border-color .4s;
}
.t-card:hover { border-color:var(--gold); }
.t-card::before {
  content:'"';
  position:absolute;
  top:-1rem; left:1.5rem;
  font-family:var(--serif);
  font-size:9rem;
  color:var(--gold);
  opacity:.12;
  line-height:1;
  pointer-events:none;
}

.t-stars { color:var(--gold); font-size:.85rem; margin-bottom:.8rem; }

.t-text {
  font-style:italic;
  font-size:1.05rem;
  color:rgba(240,236,228,.82);
  margin-bottom:2rem;
  position:relative;
  z-index:1;
}

.t-auth { display:flex; align-items:center; gap:1rem; }
.t-avatar {
  width:46px; height:46px;
  border-radius:50%;
  background:var(--gold);
  display:flex;
  align-items:center;
  justify-content:center;
  font-family:var(--display);
  font-size:1.2rem;
  color:var(--black);
  flex-shrink:0;
}
.t-name { font-family:var(--display); font-size:1.2rem; }
.t-role {
  font-family:var(--sans);
  font-size:9px;
  letter-spacing:.25em;
  text-transform:uppercase;
  color:var(--muted);
}

/* \u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550
   COMMISSION CTA BAND
\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550 */
#cta-band {
  background:var(--gold);
  padding:7rem 0;
  text-align:center;
}
#cta-band h2 {
  font-family:var(--display);
  font-size:clamp(3.5rem,9vw,10rem);
  color:var(--black);
  line-height:.95;
  margin-bottom:1.2rem;
}
#cta-band p {
  font-size:1.2rem;
  font-style:italic;
  color:rgba(8,8,8,.65);
  margin-bottom:3rem;
}
.btn-dark {
  display:inline-block;
  font-family:var(--sans);
  font-size:10px;
  letter-spacing:.4em;
  text-transform:uppercase;
  font-weight:600;
  background:var(--black);
  color:var(--gold);
  padding:1.1rem 3rem;
  text-decoration:none;
  transition:all .3s;
}
.btn-dark:hover { background:var(--deep); color:var(--gold-lt); }

/* \u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550
   CONTACT / COMMISSION FORM
\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550 */
#contact { background:var(--black); }

.contact-grid {
  display:grid;
  grid-template-columns:1fr 1.5fr;
  gap:6rem;
  align-items:start;
}

.contact-info h2 {
  font-family:var(--display);
  font-size:clamp(2.5rem,5vw,5.5rem);
  line-height:.95;
  margin-bottom:2rem;
}
.contact-info > p {
  color:var(--muted);
  font-style:italic;
  margin-bottom:3rem;
}
.c-row {
  display:flex;
  align-items:center;
  gap:1rem;
  margin-bottom:.9rem;
  font-size:1rem;
  color:rgba(240,236,228,.78);
}
.c-row i { color:var(--gold); width:20px; }

.socials { display:flex; gap:.8rem; margin-top:2.5rem; }
.s-link {
  width:42px; height:42px;
  border:1px solid var(--border);
  display:flex;
  align-items:center;
  justify-content:center;
  color:var(--muted);
  text-decoration:none;
  font-size:.95rem;
  transition:all .3s;
}
.s-link:hover { border-color:var(--gold); color:var(--gold); }

/* Form */
.f-group { margin-bottom:1.4rem; }
.f-label {
  display:block;
  font-family:var(--sans);
  font-size:9px;
  letter-spacing:.4em;
  text-transform:uppercase;
  color:var(--muted);
  margin-bottom:.5rem;
}
.f-input, .f-select, .f-area {
  width:100%;
  background:var(--charcoal);
  border:1px solid var(--border);
  color:var(--white);
  padding:.95rem 1.1rem;
  font-family:var(--serif);
  font-size:1rem;
  transition:border-color .3s;
  outline:none;
  -webkit-appearance:none;
  appearance:none;
}
.f-input:focus, .f-select:focus, .f-area:focus { border-color:var(--gold); }
.f-area { resize:vertical; min-height:140px; }
.f-select option { background:var(--charcoal); }
.f-row { display:grid; grid-template-columns:1fr 1fr; gap:1rem; }
.f-submit {
  width:100%;
  font-family:var(--sans);
  font-size:10px;
  letter-spacing:.4em;
  text-transform:uppercase;
  font-weight:700;
  background:var(--gold);
  color:var(--black);
  border:none;
  padding:1.2rem;
  cursor:pointer;
  transition:background .3s;
  margin-top:.8rem;
}
.f-submit:hover { background:var(--gold-lt); }

/* \u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550
   NEWSLETTER
\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550 */
#newsletter {
  background:var(--charcoal);
  padding:5.5rem 0;
  text-align:center;
}
#newsletter h2 {
  font-family:var(--display);
  font-size:clamp(2rem,4.5vw,5rem);
  line-height:1;
  margin-bottom:.5rem;
}
#newsletter > .container > p {
  color:var(--muted);
  font-style:italic;
  margin-bottom:2.5rem;
}
.nl-form { display:flex; max-width:500px; margin:0 auto; }
.nl-input {
  flex:1;
  background:var(--black);
  border:1px solid var(--border);
  border-right:none;
  color:var(--white);
  padding:1rem 1.4rem;
  font-family:var(--serif);
  font-size:1rem;
  outline:none;
}
.nl-input::placeholder { color:var(--muted); }
.nl-btn {
  font-family:var(--sans);
  font-size:9px;
  letter-spacing:.35em;
  text-transform:uppercase;
  font-weight:700;
  background:var(--gold);
  color:var(--black);
  border:none;
  padding:1rem 1.8rem;
  cursor:pointer;
  transition:background .3s;
}
.nl-btn:hover { background:var(--gold-lt); }

/* \u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550
   FOOTER
\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550 */
footer {
  background:var(--deep);
  border-top:1px solid var(--border);
  padding:4.5rem 0 2rem;
}
.foot-grid {
  display:grid;
  grid-template-columns:2fr 1fr 1fr 1fr;
  gap:4rem;
  margin-bottom:4rem;
}
.foot-brand h3 {
  font-family:var(--display);
  font-size:2.5rem;
  margin-bottom:1rem;
}
.foot-brand p {
  color:var(--muted);
  font-size:.9rem;
  font-style:italic;
  max-width:270px;
  line-height:1.7;
}
.foot-col h4 {
  font-family:var(--display);
  font-size:1.2rem;
  color:var(--gold);
  margin-bottom:1.5rem;
  letter-spacing:.06em;
}
.foot-col ul { list-style:none; }
.foot-col ul li { margin-bottom:.65rem; }
.foot-col ul li a {
  color:var(--muted);
  text-decoration:none;
  font-family:var(--sans);
  font-size:.82rem;
  letter-spacing:.1em;
  transition:color .3s;
}
.foot-col ul li a:hover { color:var(--gold); }

.foot-bottom {
  border-top:1px solid var(--border);
  padding-top:2rem;
  display:flex;
  align-items:center;
  justify-content:space-between;
}
.foot-bottom p {
  font-size:.8rem;
  color:var(--muted);
  font-family:var(--sans);
}
.foot-quote {
  font-style:italic;
  color:rgba(201,168,76,.5);
  font-size:.85rem;
}

/* \u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550
   CART DRAWER
\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550\u2550 */
.cart-overlay {
  display:none;
  position:fixed; inset:0;
  background:rgba(0,0,0,.55);
  z-index:1100;
}
.cart-overlay.on { display:block; }

.cart-drawer {
  position:fixed;
  top:0; right:-440px; bottom:0;
  width:420px;
  background:var(--deep);
  border-left:1px solid var(--border);
  z-index:1200;
  display:flex;
  flex-direction:column;
  transition:right .4s var(--ease);
}
.cart-drawer.on { right:0; }

.cd-head {
  padding:2rem;
  border-bottom:1px solid var(--border);
  display:flex;
  align-items:center;
  justify-content:space-between;
}
.cd-head h3 {
  font-family:var(--display);
  font-size:2rem;
  letter-spacing:.06em;
}
.cd-x {
  background:none; border:none;
  color:var(--muted); font-size:1.1rem;
  cursor:pointer;
  transition:color .3s;
}
.cd-x:hover { color:var(--white); }

.cd-body {
  flex:1;
  overflow-y:auto;
  padding:1.5rem 2rem;
}
.cd-empty {
  text-align:center;
  padding:3rem 0;
  color:var(--muted);
  font-style:italic;
  line-height:2;
}

.cd-item {
  display:flex;
  gap:1rem;
  margin-bottom:1.5rem;
  padding-bottom:1.5rem;
  border-bottom:1px solid var(--border);
}
.cd-item img {
  width:68px; height:68px;
  object-fit:cover;
  flex-shrink:0;
}
.cd-item-info { flex:1; }
.cd-item-name {
  font-family:var(--display);
  font-size:1.15rem;
  line-height:1.2;
}
.cd-item-meta {
  font-family:var(--sans);
  font-size:9px;
  letter-spacing:.2
