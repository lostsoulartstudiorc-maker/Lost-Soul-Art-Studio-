<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Lost Soul Art Studio — Roberto Cisneros | San Francisco</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;0,900;1,400;1,700&family=Cormorant+Garamond:ital,wght@0,300;0,400;0,600;1,300;1,400&family=Josefin+Sans:wght@100;300;400&display=swap" rel="stylesheet">
<style>
*,*::before,*::after{box-sizing:border-box;margin:0;padding:0}
:root{
  --blk:#0D0D0F;--obs:#131318;--char:#1C1C24;
  --gold:#C8A951;--glt:#E2C97E;--gdk:#8B6E2A;
  --crm:#F2EBD9;--mst:#A89880;--ghost:rgba(200,169,81,.08);
  --bdr:rgba(200,169,81,.18);--live:#8B1A4A;
}
html{scroll-behavior:smooth}
body{background:var(--blk);color:var(--crm);font-family:'Cormorant Garamond',serif;font-size:18px;line-height:1.7;overflow-x:hidden;cursor:crosshair}
body::before{content:'';position:fixed;inset:0;pointer-events:none;z-index:900;opacity:.35;
  background-image:url("data:image/svg+xml,%3Csvg viewBox='0 0 200 200' xmlns='http://www.w3.org/2000/svg'%3E%3Cfilter id='n'%3E%3CfeTurbulence type='fractalNoise' baseFrequency='.85' numOctaves='4'/%3E%3C/filter%3E%3Crect width='100%25' height='100%25' filter='url(%23n)' opacity='.05'/%3E%3C/svg%3E")}

/* NAV */
nav{position:fixed;top:0;left:0;right:0;z-index:800;padding:16px 48px;display:flex;justify-content:space-between;align-items:center;background:linear-gradient(to bottom,rgba(13,13,15,.96),transparent);backdrop-filter:blur(8px);transition:padding .3s}
.nav-logo{font-family:'Playfair Display',serif;font-size:15px;font-weight:700;letter-spacing:.18em;color:var(--crm);text-decoration:none;text-transform:uppercase;cursor:pointer}
.nav-logo span{color:var(--gold)}
.nav-links{display:flex;gap:0;list-style:none}
.nav-links a{font-family:'Josefin Sans',sans-serif;font-weight:100;font-size:9px;letter-spacing:.38em;text-transform:uppercase;color:var(--mst);text-decoration:none;transition:color .3s;cursor:pointer;padding:8px 14px;display:block;position:relative}
.nav-links a::after{content:'';position:absolute;bottom:0;left:14px;right:14px;height:1px;background:var(--gold);transform:scaleX(0);transition:transform .3s}
.nav-links a:hover,.nav-links a.active{color:var(--gold)}
.nav-links a:hover::after,.nav-links a.active::after{transform:scaleX(1)}
.hamburger{display:none;flex-direction:column;gap:5px;cursor:pointer;padding:4px}
.hamburger span{width:24px;height:1px;background:var(--crm);transition:all .3s}
@media(max-width:768px){
  .nav-links{display:none;position:fixed;top:0;left:0;right:0;bottom:0;background:rgba(13,13,15,.98);flex-direction:column;justify-content:center;align-items:center;gap:8px}
  .nav-links.open{display:flex}
  .nav-links a{font-size:11px;padding:16px 24px}
  .hamburger{display:flex}
  nav{padding:14px 24px}
}

/* PAGES */
.page{display:none;min-height:100vh}
.page.active{display:block}

/* HERO */
.hero{min-height:100vh;display:flex;flex-direction:column;align-items:center;justify-content:center;text-align:center;padding:120px 40px 80px;position:relative;overflow:hidden}
.hero-bg{position:absolute;inset:0;background:radial-gradient(ellipse 65% 55% at 15% 85%,rgba(200,169,81,.07),transparent 60%),radial-gradient(ellipse 45% 65% at 85% 15%,rgba(200,169,81,.05),transparent 55%);pointer-events:none}
.eyebrow{font-family:'Josefin Sans',sans-serif;font-weight:100;font-size:10px;letter-spacing:.5em;color:var(--gold);text-transform:uppercase;margin-bottom:32px;opacity:0;animation:fadeUp 1s ease forwards .2s}
.hero h1{font-family:'Playfair Display',serif;font-size:clamp(56px,11vw,118px);font-weight:900;line-height:.9;letter-spacing:-.02em;color:var(--crm);opacity:0;animation:fadeUp 1s ease forwards .45s}
.hero h1 em{font-style:italic;color:var(--gold);display:block}
.hero-sub{font-family:'Cormorant Garamond',serif;font-style:italic;font-size:clamp(16px,2.2vw,22px);color:var(--mst);margin-top:30px;max-width:520px;opacity:0;animation:fadeUp 1s ease forwards .75s;line-height:1.8}
.med-tags{display:flex;gap:10px;justify-content:center;flex-wrap:wrap;margin-top:30px;opacity:0;animation:fadeUp 1s ease forwards .95s}
.med-tag{font-family:'Josefin Sans',sans-serif;font-weight:300;font-size:9px;letter-spacing:.35em;text-transform:uppercase;color:var(--gdk);border:1px solid var(--bdr);padding:7px 16px}
.hero-line{width:1px;height:80px;background:linear-gradient(to bottom,transparent,var(--gold),transparent);margin:48px auto 0;opacity:0;animation:fadeIn 1.6s ease forwards 1.2s}
@keyframes fadeUp{from{opacity:0;transform:translateY(28px)}to{opacity:1;transform:translateY(0)}}
@keyframes fadeIn{from{opacity:0}to{opacity:1}}
@keyframes pulse{0%,100%{opacity:1;transform:scale(1)}50%{opacity:.4;transform:scale(.8)}}
@keyframes shimmer{0%{background-position:-200% center}100%{background-position:200% center}}

/* SHARED LAYOUT */
.wrap{max-width:1180px;margin:0 auto;padding:0 40px}
section{padding:90px 0}
.sec-label{font-family:'Josefin Sans',sans-serif;font-weight:100;font-size:10px;letter-spacing:.5em;color:var(--gold);text-transform:uppercase;margin-bottom:18px;display:flex;align-items:center;gap:14px}
.sec-label::after{content:'';flex:0 0 48px;height:1px;background:var(--bdr)}
.sec-h{font-family:'Playfair Display',serif;font-size:clamp(34px,5vw,58px);font-weight:700;line-height:1.08;color:var(--crm);margin-bottom:14px}
.sec-h em{font-style:italic;color:var(--gold)}
.sec-sub{font-size:17px;color:var(--mst);max-width:520px;font-style:italic;margin-bottom:56px;line-height:1.85}

/* CARDS */
.grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(310px,1fr));gap:2px}
.grid-3{display:grid;grid-template-columns:repeat(3,1fr);gap:2px}
.grid-2{display:grid;grid-template-columns:1fr 1fr;gap:2px}
@media(max-width:900px){.grid-3{grid-template-columns:1fr 1fr}}
@media(max-width:600px){.grid-3,.grid-2{grid-template-columns:1fr}.wrap{padding:0 20px}section{padding:60px 0}}
.card{background:var(--obs);border:1px solid var(--bdr);padding:38px 34px;position:relative;overflow:hidden;transition:border-color .4s,transform .4s}
.card::before{content:'';position:absolute;top:0;left:0;right:0;height:2px;background:linear-gradient(90deg,transparent,var(--gold),transparent);transform:scaleX(0);transition:transform .5s}
.card:hover{border-color:rgba(200,169,81,.45);transform:translateY(-3px)}
.card:hover::before{transform:scaleX(1)}
.card-label{font-family:'Josefin Sans',sans-serif;font-weight:100;font-size:9px;letter-spacing:.4em;text-transform:uppercase;color:var(--gdk);margin-bottom:13px}
.card-h{font-family:'Playfair Display',serif;font-size:23px;font-weight:700;color:var(--crm);margin-bottom:12px;line-height:1.2}
.card-body{font-size:15px;color:var(--mst);font-style:italic;line-height:1.78;margin-bottom:26px}
.price-from{font-family:'Josefin Sans',sans-serif;font-size:9px;letter-spacing:.35em;text-transform:uppercase;color:var(--gdk);margin-bottom:4px}
.price-val{font-family:'Playfair Display',serif;font-size:38px;font-weight:900;color:var(--gold);line-height:1}
.price-note{font-size:13px;color:var(--mst);margin-top:5px;font-style:italic}
.price-line{border-top:1px solid var(--bdr);padding-top:20px;margin-top:auto}
.incl{margin-top:16px;display:flex;flex-direction:column;gap:5px}
.incl span{font-size:13px;color:var(--mst);display:flex;align-items:flex-start;gap:9px}
.incl span::before{content:'—';color:var(--gdk);flex-shrink:0;font-size:10px;margin-top:3px}

/* BUTTONS */
.btn{font-family:'Josefin Sans',sans-serif;font-weight:300;font-size:10px;letter-spacing:.45em;text-transform:uppercase;padding:16px 38px;border:none;cursor:pointer;text-decoration:none;display:inline-block;transition:all .3s}
.btn-gold{color:var(--blk);background:var(--gold)}
.btn-gold:hover{background:var(--glt)}
.btn-out{color:var(--gold);background:transparent;border:1px solid var(--bdr)}
.btn-out:hover{border-color:var(--gold);color:var(--glt)}
.btn-row{display:flex;gap:14px;flex-wrap:wrap}

/* REVEAL */
.rev{opacity:0;transform:translateY(22px);transition:opacity .75s,transform .75s}
.rev.vis{opacity:1;transform:translateY(0)}

/* LIVE BADGE */
.live-badge{display:inline-flex;align-items:center;gap:8px;background:rgba(139,26,74,.12);border:1px solid rgba(139,26,74,.4);padding:7px 16px}
.live-dot{width:6px;height:6px;background:var(--gold);border-radius:50%;animation:pulse 2s infinite}
.live-txt{font-family:'Josefin Sans',sans-serif;font-size:9px;letter-spacing:.35em;text-transform:uppercase;color:var(--gold)}

/* BANNER */
.banner{max-width:100%;background:var(--char);padding:90px 40px}
.banner-in{max-width:1180px;margin:0 auto}

/* FOOTER */
footer{background:var(--blk);border-top:1px solid var(--bdr);padding:48px 40px;text-align:center}
.foot-logo{font-family:'Playfair Display',serif;font-size:22px;font-weight:700;color:var(--crm);margin-bottom:6px}
.foot-logo span{color:var(--gold)}
.foot-meta{font-family:'Josefin Sans',sans-serif;font-size:9px;letter-spacing:.4em;text-transform:uppercase;color:var(--mst);margin-bottom:12px}
.foot-links{display:flex;gap:24px;justify-content:center;flex-wrap:wrap;margin-bottom:20px}
.foot-links a{font-family:'Josefin Sans',sans-serif;font-size:9px;letter-spacing:.3em;text-transform:uppercase;color:var(--mst);text-decoration:none;cursor:pointer;transition:color .3s}
.foot-links a:hover{color:var(--gold)}
.foot-q{font-size:14px;color:var(--mst);font-style:italic}

/* CTA SECTION */
.cta-sec{text-align:center;padding:100px 40px;position:relative;overflow:hidden}
.cta-sec::before{content:'';position:absolute;inset:0;background:radial-gradient(ellipse 70% 60% at 50%,rgba(200,169,81,.05),transparent 70%)}
.cta-h{font-family:'Playfair Display',serif;font-size:clamp(34px,6vw,70px);font-weight:900;color:var(--crm);line-height:1.05;margin-bottom:18px}
.cta-h em{color:var(--gold);font-style:italic}
.cta-p{font-size:17px;color:var(--mst);font-style:italic;margin-bottom:44px;max-width:500px;margin-left:auto;margin-right:auto}

/* ══════════════════════════════════════ */
/* TATTOO ANNOUNCEMENT STRIP */
/* ══════════════════════════════════════ */
.tattoo-strip{background:linear-gradient(135deg,#1A0510 0%,#2A0A1A 100%);border-top:1px solid rgba(139,26,74,.5);border-bottom:1px solid rgba(139,26,74,.5);padding:60px 40px;text-align:center;position:relative;overflow:hidden}
.tattoo-strip::before{content:'TATTOO';font-family:'Playfair Display',serif;font-size:200px;font-weight:900;color:rgba(139,26,74,.04);position:absolute;right:-20px;top:50%;transform:translateY(-50%);pointer-events:none;line-height:1}
.new-pill{display:inline-block;font-family:'Josefin Sans',sans-serif;font-size:8px;letter-spacing:.45em;text-transform:uppercase;color:var(--glt);background:rgba(200,169,81,.1);border:1px solid rgba(200,169,81,.25);padding:5px 18px;margin-bottom:20px}
.ts-h{font-family:'Playfair Display',serif;font-size:clamp(26px,4vw,50px);font-weight:900;color:var(--crm);margin-bottom:12px}
.ts-h em{color:var(--glt);font-style:italic}
.ts-p{font-size:17px;color:rgba(242,235,217,.65);font-style:italic;max-width:560px;margin:0 auto 28px;line-height:1.8}

/* ══════════════════════════════════════ */
/* GALLERY */
/* ══════════════════════════════════════ */
.gallery-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(260px,1fr));gap:3px}
.gal-item{position:relative;overflow:hidden;aspect-ratio:1;cursor:pointer;background:var(--obs)}
.gal-item img{width:100%;height:100%;object-fit:cover;transition:transform .6s,filter .4s;filter:brightness(.85)}
.gal-item:hover img{transform:scale(1.06);filter:brightness(1)}
.gal-item .gal-cap{position:absolute;bottom:0;left:0;right:0;padding:20px 16px 14px;background:linear-gradient(to top,rgba(13,13,15,.9),transparent);font-family:'Josefin Sans',sans-serif;font-size:9px;letter-spacing:.3em;text-transform:uppercase;color:var(--gold);transform:translateY(100%);transition:transform .4s}
.gal-item:hover .gal-cap{transform:translateY(0)}

/* LIGHTBOX */
.lightbox{position:fixed;inset:0;background:rgba(13,13,15,.96);z-index:9000;display:none;align-items:center;justify-content:center;padding:20px}
.lightbox.open{display:flex}
.lightbox img{max-width:90vw;max-height:90vh;object-fit:contain}
.lb-close{position:absolute;top:24px;right:28px;font-size:28px;color:var(--mst);cursor:pointer;font-family:'Josefin Sans',sans-serif;line-height:1;transition:color .3s}
.lb-close:hover{color:var(--gold)}
.lb-cap{position:absolute;bottom:24px;left:50%;transform:translateX(-50%);font-family:'Josefin Sans',sans-serif;font-size:9px;letter-spacing:.4em;text-transform:uppercase;color:var(--gold)}

/* ══════════════════════════════════════ */
/* TATTOO PAGE TIERS */
/* ══════════════════════════════════════ */
.tat-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(300px,1fr));gap:2px;margin-top:48px}
.tat-tier{background:var(--obs);border:1px solid var(--bdr);padding:36px 30px;position:relative;transition:all .4s}
.tat-tier:hover{border-color:rgba(200,169,81,.45);transform:translateY(-3px)}
.tat-tier.feat{border-color:var(--gold)}
.tat-tier.feat::after{content:'MOST POPULAR';position:absolute;top:-1px;left:50%;transform:translateX(-50%);background:var(--gold);color:var(--blk);font-family:'Josefin Sans',sans-serif;font-size:8px;letter-spacing:.3em;padding:4px 14px;white-space:nowrap}
.tier-cat{font-family:'Josefin Sans',sans-serif;font-size:9px;letter-spacing:.4em;text-transform:uppercase;color:var(--gdk);margin-bottom:10px}
.tier-name{font-family:'Playfair Display',serif;font-size:22px;font-weight:700;color:var(--crm);margin-bottom:6px}
.tier-size{font-size:14px;color:var(--mst);font-style:italic;margin-bottom:14px}
.tier-price{font-family:'Playfair Display',serif;font-size:44px;font-weight:900;color:var(--gold);line-height:1;margin-bottom:5px}
.tier-time{font-family:'Josefin Sans',sans-serif;font-size:9px;letter-spacing:.3em;text-transform:uppercase;color:var(--mst);margin-bottom:14px}
.tier-desc{font-size:14px;color:var(--mst);font-style:italic;line-height:1.72;border-top:1px solid var(--bdr);padding-top:14px;margin-bottom:14px}
.tier-incl{list-style:none;display:flex;flex-direction:column;gap:6px}
.tier-incl li{font-size:13px;color:var(--mst);display:flex;gap:9px;align-items:flex-start}
.tier-incl li::before{content:'✦';color:var(--gdk);font-size:8px;margin-top:4px;flex-shrink:0}

/* ══════════════════════════════════════ */
/* PORTRAIT PRICING TABLE */
/* ══════════════════════════════════════ */
.ptable{width:100%;border-collapse:collapse;margin-top:32px}
.ptable th{background:var(--char);font-family:'Josefin Sans',sans-serif;font-size:9px;letter-spacing:.4em;text-transform:uppercase;color:var(--gold);padding:16px 20px;text-align:left;border:1px solid var(--bdr)}
.ptable td{padding:14px 20px;border:1px solid var(--bdr);font-size:15px;color:var(--mst);font-style:italic;vertical-align:top}
.ptable tr:nth-child(even) td{background:var(--obs)}
.ptable tr:nth-child(odd) td{background:rgba(255,255,255,.015)}
.ptable .tier-head td{background:var(--char);font-family:'Playfair Display',serif;font-size:16px;font-weight:700;color:var(--crm);font-style:normal}
.ptable .gold-val{color:var(--gold);font-family:'Playfair Display',serif;font-weight:700;font-size:18px;font-style:normal}
.ptable .dep-val{color:var(--gdk);font-style:normal}

/* ══════════════════════════════════════ */
/* COLLECTORS BUNDLE */
/* ══════════════════════════════════════ */
.bundle{background:linear-gradient(135deg,var(--char),var(--obs));border:1px solid var(--gold);padding:60px;position:relative;overflow:hidden}
.bundle::before{content:'COLLECTOR';font-family:'Playfair Display',serif;font-size:180px;font-weight:900;color:rgba(200,169,81,.03);position:absolute;right:-20px;top:50%;transform:translateY(-50%);line-height:1;pointer-events:none}
.bundle-inner{display:grid;grid-template-columns:1fr auto;gap:48px;align-items:center}
@media(max-width:700px){.bundle-inner{grid-template-columns:1fr}.bundle{padding:40px 28px}}
.bundle-pills{display:flex;gap:16px;flex-wrap:wrap;margin-top:28px}
.b-pill{border:1px solid var(--bdr);padding:16px 20px;text-align:center;min-width:100px;transition:all .3s;cursor:default}
.b-pill:hover{border-color:var(--gold);background:var(--ghost)}
.b-pct{font-family:'Playfair Display',serif;font-size:32px;font-weight:900;color:var(--gold);line-height:1}
.b-lbl{font-family:'Josefin Sans',sans-serif;font-size:9px;letter-spacing:.3em;text-transform:uppercase;color:var(--mst);margin-top:4px}

/* ══════════════════════════════════════ */
/* TESTIMONIALS */
/* ══════════════════════════════════════ */
.testimonials{display:grid;grid-template-columns:repeat(auto-fill,minmax(310px,1fr));gap:2px}
.tcard{background:var(--obs);border:1px solid var(--bdr);padding:36px 32px}
.tcard-q{font-size:14px;color:var(--mst);font-style:italic;line-height:1.85;margin-bottom:24px}
.tcard-q::before{content:'"';font-family:'Playfair Display',serif;font-size:48px;color:rgba(200,169,81,.25);line-height:1;display:block;margin-bottom:-10px}
.tcard-name{font-family:'Playfair Display',serif;font-size:16px;font-weight:700;color:var(--crm);margin-bottom:4px}
.tcard-role{font-family:'Josefin Sans',sans-serif;font-size:9px;letter-spacing:.35em;text-transform:uppercase;color:var(--gdk)}

/* ══════════════════════════════════════ */
/* BLOG */
/* ══════════════════════════════════════ */
.blog-grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(340px,1fr));gap:2px}
.blog-card{background:var(--obs);border:1px solid var(--bdr);overflow:hidden;transition:border-color .4s,transform .4s}
.blog-card:hover{border-color:rgba(200,169,81,.4);transform:translateY(-2px)}
.blog-card img{width:100%;height:200px;object-fit:cover;filter:brightness(.75);transition:filter .4s}
.blog-card:hover img{filter:brightness(.9)}
.blog-body{padding:28px 26px}
.blog-date{font-family:'Josefin Sans',sans-serif;font-size:9px;letter-spacing:.4em;text-transform:uppercase;color:var(--gdk);margin-bottom:10px}
.blog-h{font-family:'Playfair Display',serif;font-size:20px;font-weight:700;color:var(--crm);margin-bottom:10px;line-height:1.25}
.blog-p{font-size:14px;color:var(--mst);font-style:italic;line-height:1.75}

/* ══════════════════════════════════════ */
/* CONTRACT */
/* ══════════════════════════════════════ */
.contract-wrap{max-width:800px;margin:0 auto;padding:100px 40px}
@media(max-width:600px){.contract-wrap{padding:80px 20px}}
.contract-hdr{text-align:center;padding:60px 0 48px;border-bottom:1px solid var(--bdr);margin-bottom:56px}
.csec{margin-bottom:44px}
.csec h3{font-family:'Playfair Display',serif;font-size:20px;font-weight:700;color:var(--crm);border-left:3px solid var(--gold);padding-left:14px;margin-bottom:18px}
.csec p,.csec li{font-size:15px;color:var(--mst);line-height:1.85;font-style:italic}
.csec ul{padding-left:22px;margin-top:8px}
.csec li{margin-bottom:8px}
.form-group{margin-bottom:22px}
.form-group label{display:block;font-family:'Josefin Sans',sans-serif;font-size:9px;letter-spacing:.4em;text-transform:uppercase;color:var(--gdk);margin-bottom:8px}
.form-group input,.form-group select,.form-group textarea{width:100%;background:var(--char);border:1px solid var(--bdr);color:var(--crm);font-family:'Cormorant Garamond',serif;font-size:16px;padding:13px 16px;outline:none;transition:border-color .3s;resize:vertical}
.form-group input:focus,.form-group select:focus,.form-group textarea:focus{border-color:var(--gold)}
.form-group select option{background:var(--char)}
.form-row{display:grid;grid-template-columns:1fr 1fr;gap:18px}
@media(max-width:600px){.form-row{grid-template-columns:1fr}}
.chk-group{display:flex;flex-direction:column;gap:12px}
.chk-item{display:flex;align-items:flex-start;gap:12px;cursor:pointer}
.chk-item input[type=checkbox]{width:16px;height:16px;accent-color:var(--gold);flex-shrink:0;margin-top:3px;cursor:pointer}
.chk-item span{font-size:15px;color:var(--mst);font-style:italic;line-height:1.6}
.sig-block{margin-top:40px;padding-top:40px;border-top:1px solid var(--bdr)}
.sig-input{border:none;border-bottom:1px solid var(--gdk);background:transparent;width:100%;color:var(--crm);font-family:'Playfair Display',serif;font-size:22px;font-style:italic;padding:8px 0;outline:none}
.total-box{background:var(--obs);border:1px solid var(--gold);padding:24px 28px;margin-top:28px;display:flex;justify-content:space-between;align-items:center;flex-wrap:wrap;gap:12px}
.total-label{font-family:'Josefin Sans',sans-serif;font-size:10px;letter-spacing:.4em;text-transform:uppercase;color:var(--mst)}
.total-val{font-family:'Playfair Display',serif;font-size:38px;font-weight:900;color:var(--gold)}

/* ══════════════════════════════════════ */
/* TERMS */
/* ══════════════════════════════════════ */
.terms-wrap{max-width:780px;margin:0 auto;padding:100px 40px}
@media(max-width:600px){.terms-wrap{padding:80px 20px}}
.t-sec{margin-bottom:48px;border-bottom:1px solid var(--bdr);padding-bottom:48px}
.t-sec:last-child{border-bottom:none}
.t-num{font-family:'Playfair Display',serif;font-size:60px;font-weight:900;color:rgba(200,169,81,.06);line-height:1;margin-bottom:6px}
.t-sec h3{font-family:'Playfair Display',serif;font-size:22px;font-weight:700;color:var(--crm);margin-bottom:16px}
.t-sec p{font-size:15px;color:var(--mst);font-style:italic;line-height:1.9;margin-bottom:12px}
.t-sec ul{padding-left:18px}
.t-sec li{font-size:15px;color:var(--mst);font-style:italic;line-height:1.8;margin-bottom:8px}

/* ABOUT SECTION */
.about-grid{display:grid;grid-template-columns:1fr 1fr;gap:60px;align-items:start}
@media(max-width:700px){.about-grid{grid-template-columns:1fr;gap:32px}}
.quote-box{border:1px solid var(--bdr);padding:36px;background:var(--obs)}
.quote-txt{font-family:'Playfair Display',serif;font-size:20px;font-style:italic;color:var(--crm);line-height:1.45;margin-bottom:20px}
.quote-attr{font-family:'Josefin Sans',sans-serif;font-size:9px;letter-spacing:.4em;text-transform:uppercase;color:var(--gdk)}
</style>
</head>
<body>

<!-- LIGHTBOX -->
<div class="lightbox" id="lb" onclick="closeLB(event)">
  <span class="lb-close" onclick="closeLB()">✕</span>
  <img id="lb-img" src="" alt="">
  <span class="lb-cap" id="lb-cap"></span>
</div>

<!-- NAV -->
<nav id="main-nav">
  <span class="nav-logo" onclick="go('home')">Lost <span>Soul</span> Art</span>
  <ul class="nav-links" id="nav-links">
    <li><a onclick="go('home')" id="n-home" class="active">Home</a></li>
    <li><a onclick="go('gallery')" id="n-gallery">Gallery</a></li>
    <li><a onclick="go('portraits')" id="n-portraits">Portraits</a></li>
    <li><a onclick="go('murals')" id="n-murals">Murals</a></li>
    <li><a onclick="go('storefronts')" id="n-storefronts">Storefronts</a></li>
    <li><a onclick="go('tattoo')" id="n-tattoo" style="color:var(--gold);">✦ Tattoo</a></li>
    <li><a onclick="go('contract')" id="n-contract">Commission</a></li>
    <li><a onclick="go('blog')" id="n-blog">Blog</a></li>
    <li><a onclick="go('terms')" id="n-terms">Terms</a></li>
  </ul>
  <div class="hamburger" id="ham" onclick="toggleMenu()">
    <span></span><span></span><span></span>
  </div>
</nav>

<!-- ══════════════════════════ PAGE: HOME ══════════════════════════ -->
<div id="page-home" class="page active">
  <div class="hero">
    <div class="hero-bg"></div>
    <p class="eyebrow">Roberto Cisneros &nbsp;·&nbsp; San Francisco, CA &nbsp;·&nbsp; Fine Art Studio</p>
    <h1>Lost Soul<br><em>Art Studio</em></h1>
    <div class="med-tags">
      <span class="med-tag">Acrylic</span>
      <span class="med-tag">Ballpoint Pen</span>
      <span class="med-tag">Watercolor</span>
      <span class="med-tag" style="color:var(--gold);border-color:rgba(200,169,81,.45);">✦ Now Tattooing</span>
    </div>
    <p class="hero-sub">Fine art portraiture and contemporary surrealism. Custom murals, storefront installations, workshops — and now, original tattoo art. Getting lost in imagination.</p>
    <div class="hero-line"></div>
  </div>

  <!-- TATTOO ANNOUNCEMENT -->
  <div class="tattoo-strip">
    <div class="new-pill">Now Available · April 2026</div>
    <h2 class="ts-h">Introducing <em>Tattoo Art</em><br>by Lost Soul Art Studio</h2>
    <p class="ts-p">Roberto Cisneros is now accepting custom tattoo commissions — bringing the same surrealist, fine-line vision that defines the studio's paintings directly onto skin. Original flash designs revealed every Wednesday at 5 PM.</p>
    <button class="btn btn-gold" onclick="go('tattoo')">View Tattoo Services &amp; Pricing</button>
  </div>

  <!-- SERVICES -->
  <div class="banner">
    <div class="banner-in">
      <div class="rev">
        <p class="sec-label">Professional Services</p>
        <h2 class="sec-h">Fine Art Portraiture &amp;<br><em>Contemporary Surrealism</em></h2>
        <p class="sec-sub">One artist. Every medium. A complete creative practice built around the belief that art should challenge the viewer to find beauty within the shadows of the psyche.</p>
      </div>
      <div class="grid rev">
        <div class="card" style="cursor:pointer" onclick="go('portraits')">
          <p class="card-label">Fine Art</p>
          <h3 class="card-h">Portraits of People &amp; Pets</h3>
          <p class="card-body">Hand-painted portraits in acrylic, watercolor, or ballpoint pen. Each one built from your reference photos — capturing personality, not just likeness.</p>
          <div class="price-line">
            <p class="price-from">Starting from</p>
            <div class="price-val">$150</div>
            <p class="price-note">5×7 small · Up to 24×36 statement pieces</p>
          </div>
        </div>
        <div class="card" style="cursor:pointer" onclick="go('murals')">
          <p class="card-label">Interior Murals</p>
          <h3 class="card-h">Residential &amp; Commercial</h3>
          <p class="card-body">Acrylic murals that transform a space into something people remember and photograph. Homes, cafés, restaurants, offices, and hotel lobbies.</p>
          <div class="price-line">
            <p class="price-from">Starting from</p>
            <div class="price-val">$500</div>
            <p class="price-note">Quoted by square footage and complexity</p>
          </div>
        </div>
        <div class="card" style="cursor:pointer" onclick="go('storefronts')">
          <p class="card-label">Storefront Art</p>
          <h3 class="card-h">Window Installations</h3>
          <p class="card-body">Seasonal and custom window painting for businesses. Halloween, Christmas, summer themes, branded permanent pieces — completed in one day.</p>
          <div class="price-line">
            <p class="price-from">Starting from</p>
            <div class="price-val">$200</div>
            <p class="price-note">Up to 15 sq ft · Larger tiers available</p>
          </div>
        </div>
        <div class="card" style="border-color:rgba(139,26,74,.5);cursor:pointer" onclick="go('tattoo')">
          <p class="card-label" style="color:var(--live);">✦ New — Now Booking</p>
          <h3 class="card-h">Custom Tattoo Art</h3>
          <p class="card-body">Original custom tattoos and flash designs rooted in surrealist fine-line imagery. The same vision that defines the paintings — now permanent on skin.</p>
          <div class="price-line">
            <p class="price-from">Studio minimum</p>
            <div class="price-val">$150</div>
            <p class="price-note">Custom, flash &amp; friend rates available</p>
          </div>
          <div class="live-badge" style="margin-top:18px"><div class="live-dot"></div><span class="live-txt">Flash drops · Wednesday Lives · 5 PM</span></div>
        </div>
        <div class="card" onclick="go('contract')" style="cursor:pointer">
          <p class="card-label">Workshops</p>
          <h3 class="card-h">Studio Instruction</h3>
          <p class="card-body">Monthly group sessions and private one-on-one instruction in acrylic, watercolor, and ballpoint pen. Small groups. Real technique. Work you take home.</p>
          <div class="price-line">
            <p class="price-from">Group sessions from</p>
            <div class="price-val">$100</div>
            <p class="price-note">Per student · Private sessions $180</p>
          </div>
        </div>
        <div class="card" onclick="go('gallery')" style="cursor:pointer">
          <p class="card-label">Originals &amp; Prints</p>
          <h3 class="card-h">Own a Lost Soul Work</h3>
          <p class="card-body">Original acrylic paintings, watercolor studies, and ballpoint pen works. Fine art prints from $50. Wednesday Live drops — first access to new work.</p>
          <div class="price-line">
            <p class="price-from">Prints from</p>
            <div class="price-val">$50</div>
            <p class="price-note">Originals from $150 · Ships nationwide</p>
          </div>
          <div class="live-badge" style="margin-top:18px"><div class="live-dot"></div><span class="live-txt">Live drops every Wednesday · 5 PM</span></div>
        </div>
      </div>
    </div>
  </div>

  <!-- ABOUT -->
  <section>
    <div class="wrap">
      <div class="about-grid rev">
        <div>
          <p class="sec-label">The Artist</p>
          <h2 class="sec-h">Roberto<br><em>Cisneros</em></h2>
          <p style="font-size:17px;color:var(--mst);font-style:italic;line-height:1.85;margin-bottom:18px">Roberto Cisneros is a multidisciplinary artist whose work bridges the gap between classical fine-art technique and contemporary graphic expressionism. Under the banner of Lost Soul Art Studio, he creates works that challenge the viewer to find beauty within the shadows of the psyche.</p>
          <p style="font-size:17px;color:var(--mst);font-style:italic;line-height:1.85;margin-bottom:32px">Working in acrylic, ballpoint pen, and watercolor from his San Francisco studio, Roberto brings a surrealist's eye to every commission — and now extends that same creative vision into original tattoo art.</p>
          <div class="btn-row">
            <button class="btn btn-gold" onclick="go('gallery')">View Portfolio</button>
            <button class="btn btn-out" onclick="go('contract')">Start a Commission</button>
          </div>
        </div>
        <div>
          <div class="quote-box">
            <img src="https://lostsoulart.simdif.com/images/th/sd_69c862b26dc86.png?no_cache=1774740168" alt="Roberto Cisneros" style="width:100%;margin-bottom:28px;filter:brightness(.9)">
            <p class="quote-txt">"The labyrinth of the creative mind is where the soul goes to find itself."</p>
            <p class="quote-attr">— Roberto Cisneros, Lost Soul Art Studio</p>
            <div style="margin-top:24px;padding-top:24px;border-top:1px solid var(--bdr)">
              <p style="font-family:'Josefin Sans',sans-serif;font-size:9px;letter-spacing:.35em;text-transform:uppercase;color:var(--mst);margin-bottom:12px">Watch Live Every Wednesday at 5 PM</p>
              <div class="live-badge"><div class="live-dot"></div><span class="live-txt">Facebook · Instagram · TikTok · YouTube</span></div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- TESTIMONIALS -->
  <div class="banner">
    <div class="banner-in">
      <div class="rev">
        <p class="sec-label">Client Words</p>
        <h2 class="sec-h">What People<br><em>Are Saying</em></h2>
      </div>
      <div class="testimonials rev">
        <div class="tcard">
          <p class="tcard-q">Working with Lost Soul Art was an incredible experience. The custom piece created for our home perfectly captures my innovative spirit and has become a conversation starter with every person who visits. The attention to detail and Roberto's process exceeded our expectations.</p>
          <p class="tcard-name">Jojo Collins</p>
          <p class="tcard-role">San Francisco, CA Resident</p>
        </div>
        <div class="tcard">
          <p class="tcard-q">I commissioned a piece for my home and was blown away by the result. The artist truly listened to what I wanted and delivered something even better than I imagined. The colors, energy, and emotion in the work make it the centerpiece of my living room.</p>
          <p class="tcard-name">Lawrence Renfield</p>
          <p class="tcard-role">Interior Designer</p>
        </div>
        <div class="tcard">
          <p class="tcard-q">The mural painted for our Mission District café has transformed the entire atmosphere of our space. Customers constantly ask about it and it's become a signature part of our brand identity. Professional, creative, and completed on time — couldn't ask for more.</p>
          <p class="tcard-name">David Park</p>
          <p class="tcard-role">Owner, Ritual Coffee Collective</p>
        </div>
      </div>
    </div>
  </div>

  <div class="cta-sec">
    <h2 class="cta-h">Ready to Begin<br><em>Something Real?</em></h2>
    <p class="cta-p">Every commission starts with a conversation. Tell me what you have in mind.</p>
    <div class="btn-row" style="justify-content:center">
      <button class="btn btn-gold" onclick="go('contract')">Start a Commission</button>
      <a href="https://wa.me/13412539299" target="_blank" class="btn btn-out">WhatsApp Roberto</a>
    </div>
  </div>
  <footer>
    <p class="foot-logo">Lost <span>Soul</span> Art Studio</p>
    <p class="foot-meta">Roberto Cisneros &nbsp;·&nbsp; San Francisco, CA</p>
    <div class="foot-links">
      <a onclick="go('home')">Home</a><a onclick="go('gallery')">Gallery</a>
      <a onclick="go('portraits')">Portraits</a><a onclick="go('murals')">Murals</a>
      <a onclick="go('storefronts')">Storefronts</a><a onclick="go('tattoo')">Tattoo</a>
      <a onclick="go('contract')">Commission</a><a onclick="go('blog')">Blog</a>
      <a onclick="go('terms')">Terms</a>
    </div>
    <p class="foot-q">"The labyrinth of the creative mind is where the soul goes to find itself." © 2026 Lost Soul Art Studio</p>
  </footer>
</div>

<!-- ══════════════════════════ PAGE: GALLERY ══════════════════════════ -->
<div id="page-gallery" class="page">
  <div class="hero" style="min-height:50vh;padding:130px 40px 60px">
    <div class="hero-bg"></div>
    <p class="eyebrow">Lost Soul Art Studio</p>
    <h1 style="font-size:clamp(44px,8vw,88px)">SF <em>Gallery</em></h1>
    <p class="hero-sub">Original works in acrylic, ballpoint pen, and watercolor — surrealist portraiture and contemporary expressionism from the Lost Soul Art Studio.</p>
  </div>
  <div style="padding:60px 40px 100px">
    <div class="gallery-grid rev" id="gallery-grid"></div>
  </div>
  <div class="cta-sec">
    <h2 class="cta-h">Own a Piece of<br><em>Lost Soul Art</em></h2>
    <p class="cta-p">Commission an original or enquire about a print. Every piece in this gallery is available as a limited edition giclée print.</p>
    <div class="btn-row" style="justify-content:center">
      <button class="btn btn-gold" onclick="go('contract')">Commission Your Piece</button>
      <a href="https://wa.me/13412539299" target="_blank" class="btn btn-out">Ask About Prints</a>
    </div>
  </div>
  <footer>
    <p class="foot-logo">Lost <span>Soul</span> Art Studio</p>
    <p class="foot-meta">Roberto Cisneros &nbsp;·&nbsp; San Francisco, CA</p>
    <p class="foot-q">"The labyrinth of the creative mind is where the soul goes to find itself." © 2026</p>
  </footer>
</div>

<!-- ══════════════════════════ PAGE: PORTRAITS ══════════════════════════ -->
<div id="page-portraits" class="page">
  <div class="hero" style="min-height:55vh;padding:130px 40px 60px">
    <div class="hero-bg"></div>
    <p class="eyebrow">Fine Art Portraiture</p>
    <h1 style="font-size:clamp(44px,8vw,88px)">Portraits of<br><em>People &amp; Pets</em></h1>
    <p class="hero-sub">Hand-painted portraits in acrylic, watercolor, or ballpoint pen. Each one a singular piece — capturing personality, not just likeness.</p>
  </div>
  <section>
    <div class="wrap rev">
      <p class="sec-label">Official Pricing Scale</p>
      <h2 class="sec-h">Portrait<br><em>Pricing</em></h2>
      <p class="sec-sub">All prices reflect a single subject. A 30% non-refundable deposit is required to secure your spot. The remaining 70% is due upon completion.</p>
      <table class="ptable">
        <thead><tr><th>Tier</th><th>Size</th><th>Total Price</th><th>30% Deposit</th><th>PayPal</th></tr></thead>
        <tbody>
          <tr class="tier-head"><td colspan="5">SMALL PORTRAITS</td></tr>
          <tr><td>Small</td><td>5 × 7</td><td class="gold-val">$150</td><td class="dep-val">$45</td><td rowspan="3" style="vertical-align:middle;text-align:center"><a href="https://www.paypal.com/ncp/payment/8LZGEN2GHFUMU" target="_blank" class="btn btn-gold" style="font-size:8px;padding:10px 18px">Pay Deposit</a></td></tr>
          <tr><td>Small</td><td>8 × 8</td><td class="gold-val">$200</td><td class="dep-val">$60</td></tr>
          <tr><td>Small</td><td>8 × 10</td><td class="gold-val">$275</td><td class="dep-val">$82.50</td></tr>
          <tr class="tier-head"><td colspan="5">MEDIUM PORTRAITS</td></tr>
          <tr><td>Medium</td><td>11 × 14</td><td class="gold-val">$400</td><td class="dep-val">$120</td><td rowspan="3" style="vertical-align:middle;text-align:center"><a href="https://www.paypal.com/ncp/payment/8LZGEN2GHFUMU" target="_blank" class="btn btn-gold" style="font-size:8px;padding:10px 18px">Pay Deposit</a></td></tr>
          <tr><td>Medium</td><td>12 × 12</td><td class="gold-val">$525</td><td class="dep-val">$157.50</td></tr>
          <tr><td>Medium</td><td>12 × 16</td><td class="gold-val">$650</td><td class="dep-val">$195</td></tr>
          <tr class="tier-head"><td colspan="5">LARGE PORTRAITS</td></tr>
          <tr><td>Large</td><td>16 × 20</td><td class="gold-val">$850</td><td class="dep-val">$255</td><td rowspan="3" style="vertical-align:middle;text-align:center"><a href="https://www.paypal.com/ncp/payment/8LZGEN2GHFUMU" target="_blank" class="btn btn-gold" style="font-size:8px;padding:10px 18px">Pay Deposit</a></td></tr>
          <tr><td>Large</td><td>18 × 24</td><td class="gold-val">$1,100</td><td class="dep-val">$330</td></tr>
          <tr><td>Statement</td><td>24 × 36</td><td class="gold-val">$1,500+</td><td class="dep-val">$450</td></tr>
        </tbody>
      </table>
      <div style="margin-top:24px;background:var(--obs);border:1px solid var(--bdr);padding:20px 24px">
        <p style="font-size:15px;color:var(--mst);font-style:italic"><strong style="color:var(--crm);font-style:normal">Extra subjects:</strong> 30% of the final price per additional person or pet. &nbsp;·&nbsp; <strong style="color:var(--crm);font-style:normal">Medium options:</strong> Acrylic, watercolor, or ballpoint pen — your choice or leave it to Roberto. &nbsp;·&nbsp; <strong style="color:var(--crm);font-style:normal">Balance:</strong> Remaining 70% due upon completion.</p>
      </div>
    </div>
  </section>
  <div class="banner">
    <div class="banner-in rev">
      <p class="sec-label">The Process</p>
      <h2 class="sec-h">How a Portrait<br><em>Comes to Life</em></h2>
      <div class="grid-2" style="gap:2px;margin-top:0">
        <div class="card"><div style="font-family:'Playfair Display',serif;font-size:48px;font-weight:900;color:rgba(200,169,81,.1);line-height:1;margin-bottom:8px">01</div><h3 class="card-h">Share Your References</h3><p class="card-body">Send clear photos with good lighting, ideally showing the eyes and expression clearly. For pets, multiple angles help capture their personality.</p></div>
        <div class="card"><div style="font-family:'Playfair Display',serif;font-size:48px;font-weight:900;color:rgba(200,169,81,.1);line-height:1;margin-bottom:8px">02</div><h3 class="card-h">Confirm &amp; Deposit</h3><p class="card-body">Roberto confirms the commission details and you pay the 30% deposit via PayPal. No work begins without a confirmed deposit.</p></div>
        <div class="card"><div style="font-family:'Playfair Display',serif;font-size:48px;font-weight:900;color:rgba(200,169,81,.1);line-height:1;margin-bottom:8px">03</div><h3 class="card-h">Work in Progress</h3><p class="card-body">You receive updates at key stages so you are never in the dark. The work evolves from rough block-in to final detail.</p></div>
        <div class="card"><div style="font-family:'Playfair Display',serif;font-size:48px;font-weight:900;color:rgba(200,169,81,.1);line-height:1;margin-bottom:8px">04</div><h3 class="card-h">Final Delivery</h3><p class="card-body">Pay the remaining 70% balance and receive your original. Ships nationwide in protective packaging or available for pickup in San Francisco.</p></div>
      </div>
    </div>
  </div>
  <div class="cta-sec">
    <h2 class="cta-h">Commission<br><em>Your Portrait</em></h2>
    <p class="cta-p">Ready to begin? Fill out the commission form or reach out directly via WhatsApp.</p>
    <div class="btn-row" style="justify-content:center">
      <button class="btn btn-gold" onclick="go('contract')">Commission Now</button>
      <a href="https://wa.me/13412539299" target="_blank" class="btn btn-out">WhatsApp Roberto</a>
    </div>
  </div>
  <footer><p class="foot-logo">Lost <span>Soul</span> Art Studio</p><p class="foot-meta">Roberto Cisneros · San Francisco, CA</p><p class="foot-q">"The labyrinth of the creative mind is where the soul goes to find itself." © 2026</p></footer>
</div>

<!-- ══════════════════════════ PAGE: MURALS ══════════════════════════ -->
<div id="page-murals" class="page">
  <div class="hero" style="min-height:55vh;padding:130px 40px 60px">
    <div class="hero-bg"></div>
    <p class="eyebrow">Interior Murals</p>
    <h1 style="font-size:clamp(44px,8vw,88px)">Walls That<br><em>Remember You</em></h1>
    <p class="hero-sub">Custom acrylic murals for residential and commercial interiors. Work that transforms a space rather than merely decorating it.</p>
  </div>
  <section>
    <div class="wrap rev">
      <p class="sec-label">Services &amp; Pricing</p>
      <h2 class="sec-h">Mural<br><em>Commissions</em></h2>
      <div class="grid" style="margin-bottom:32px">
        <div class="card">
          <p class="card-label">Residential</p>
          <h3 class="card-h">Home Murals</h3>
          <p class="card-body">Living rooms, bedrooms, nurseries, entryways, stairwells. Spaces where you live should carry the work that reflects how you see the world.</p>
          <div class="price-line">
            <p class="price-from">Starting from</p>
            <div class="price-val">$500</div>
            <p class="price-note">Priced by square footage · On-site consultation required</p>
          </div>
          <div class="incl">
            <span>In-home consultation and concept development</span>
            <span>Custom design sketches for your approval</span>
            <span>All materials and wall preparation</span>
            <span>Protective sealant finish</span>
            <span>Documentation photography upon completion</span>
          </div>
        </div>
        <div class="card">
          <p class="card-label">Commercial</p>
          <h3 class="card-h">Business Murals</h3>
          <p class="card-body">Cafés, restaurants, offices, retail, hotel lobbies. Work that becomes part of your brand identity — and gives your customers something worth photographing.</p>
          <div class="price-line">
            <p class="price-from">Starting from</p>
            <div class="price-val">$1,500</div>
            <p class="price-note">Priced per project · Scheduled around your business hours</p>
          </div>
          <div class="incl">
            <span>Brand alignment consultation</span>
            <span>Custom concept sketches for approval</span>
            <span>Scheduled around your business hours</span>
            <span>All materials, prep, and sealant included</span>
            <span>Documentation photography for your marketing</span>
          </div>
        </div>
      </div>
      <div style="background:var(--obs);border:1px solid var(--bdr);padding:32px">
        <p style="font-size:15px;color:var(--mst);font-style:italic;line-height:1.8"><strong style="color:var(--crm);font-style:normal">To get a quote:</strong> Please provide your address, the dimensions of the wall space (width × height), the desired theme or visual direction, and your target completion date. Quotes are provided within 48 hours of consultation.</p>
      </div>
    </div>
  </section>
  <div class="cta-sec">
    <h2 class="cta-h">Transform<br><em>Your Space</em></h2>
    <div class="btn-row" style="justify-content:center">
      <button class="btn btn-gold" onclick="go('contract')">Request a Quote</button>
      <a href="https://wa.me/13412539299" target="_blank" class="btn btn-out">WhatsApp Roberto</a>
    </div>
  </div>
  <footer><p class="foot-logo">Lost <span>Soul</span> Art Studio</p><p class="foot-meta">Roberto Cisneros · San Francisco, CA</p><p class="foot-q">"The labyrinth of the creative mind is where the soul goes to find itself." © 2026</p></footer>
</div>

<!-- ══════════════════════════ PAGE: STOREFRONTS ══════════════════════════ -->
<div id="page-storefronts" class="page">
  <div class="hero" style="min-height:55vh;padding:130px 40px 60px">
    <div class="hero-bg"></div>
    <p class="eyebrow">Storefront Installations</p>
    <h1 style="font-size:clamp(44px,8vw,88px)">Windows That<br><em>Stop People Cold</em></h1>
    <p class="hero-sub">Professional hand-painted window illustrations for businesses. High-impact seasonal and branded displays that set you apart from every other storefront on the block.</p>
  </div>
  <section>
    <div class="wrap rev">
      <p class="sec-label">Tiers &amp; Pricing</p>
      <h2 class="sec-h">Storefront<br><em>Packages</em></h2>
      <div class="grid">
        <div class="card">
          <p class="card-label">Tier I</p>
          <h3 class="card-h">Minimalist / Line Work</h3>
          <p class="card-body">Clean branding and line illustration. Up to 15 sq ft. Perfect for boutiques wanting an elegant seasonal touch without heavy detail.</p>
          <div class="price-line">
            <p class="price-from">Starting from</p>
            <div class="price-val">$200</div>
            <p class="price-note">Deposit: $50 &nbsp;·&nbsp; Timeline: 4–6 hours</p>
          </div>
          <div class="incl">
            <span>Up to 15 sq ft coverage</span>
            <span>Professional line work and branding</span>
            <span>Weather-resistant pigments on glass</span>
            <span>Easy removal via standard glass scraper</span>
          </div>
        </div>
        <div class="card">
          <p class="card-label">Tier II</p>
          <h3 class="card-h">Standard / Seasonal</h3>
          <p class="card-body">Mid-detail seasonal illustration — Halloween scenes, Christmas tableaux, spring florals, summer themes. The most popular tier for repeat seasonal clients.</p>
          <div class="price-line">
            <p class="price-from">Starting from</p>
            <div class="price-val">$450</div>
            <p class="price-note">Deposit: $100 &nbsp;·&nbsp; 15–40 sq ft coverage</p>
          </div>
          <div class="incl">
            <span>15–40 sq ft seasonal illustration</span>
            <span>Custom design for your theme</span>
            <span>Completed in one day</span>
            <span>Returhning client rates available</span>
          </div>
        </div>
        <div class="card">
          <p class="card-label">Tier III</p>
          <h3 class="card-h">Signature / Full Mural</h3>
          <p class="card-body">Highly detailed full storefront murals — 40+ sq ft of original hand-painted illustration. Branded permanent installations and large statement seasonal displays.</p>
          <div class="price-line">
            <p class="price-from">Starting from</p>
            <div class="price-val">$800</div>
            <p class="price-note">Quoted individually &nbsp;·&nbsp; 40+ sq ft</p>
          </div>
          <div class="incl">
            <span>40+ sq ft coverage</span>
            <span>Full custom concept and design</span>
            <span>Brand color and identity integration</span>
            <span>Permanent UV-resistant option available</span>
          </div>
        </div>
      </div>
      <div style="margin-top:32px;background:var(--obs);border:1px solid var(--bdr);padding:32px">
        <p style="font-family:'Josefin Sans',sans-serif;font-size:9px;letter-spacing:.4em;text-transform:uppercase;color:var(--gdk);margin-bottom:10px">To Request a Quote — Include:</p>
        <p style="font-size:15px;color:var(--mst);font-style:italic;line-height:1.8">Your business address &nbsp;·&nbsp; Glass dimensions (width × height in feet) &nbsp;·&nbsp; Desired theme or season &nbsp;·&nbsp; Target completion date &nbsp;·&nbsp; 14-day lead time required for custom designs. Materials: professional-grade, weather-resistant pigments on glass.</p>
      </div>
    </div>
  </section>
  <div class="cta-sec">
    <h2 class="cta-h">Book Your<br><em>Storefront</em></h2>
    <div class="btn-row" style="justify-content:center">
      <button class="btn btn-gold" onclick="go('contract')">Request a Quote</button>
      <a href="https://wa.me/13412539299" target="_blank" class="btn btn-out">WhatsApp Roberto</a>
    </div>
  </div>
  <footer><p class="foot-logo">Lost <span>Soul</span> Art Studio</p><p class="foot-meta">Roberto Cisneros · San Francisco, CA</p><p class="foot-q">"The labyrinth of the creative mind is where the soul goes to find itself." © 2026</p></footer>
</div>

<!-- ══════════════════════════ PAGE: TATTOO ══════════════════════════ -->
<div id="page-tattoo" class="page">
  <div class="hero" style="background:linear-gradient(180deg,#0D0D0F,#1A0510 100%);min-height:60vh;padding:130px 40px 60px">
    <div class="hero-bg"></div>
    <p class="eyebrow">✦ Now Accepting Bookings · San Francisco</p>
    <h1 style="font-size:clamp(52px,9vw,100px)">Tattoo<br><em>Art</em></h1>
    <div class="med-tags">
      <span class="med-tag">Custom Design</span>
      <span class="med-tag">Flash Available</span>
      <span class="med-tag">Surrealist Fine Line</span>
      <span class="med-tag">Portrait Tattoos</span>
    </div>
    <p class="hero-sub">The same visual language that defines Lost Soul Art's paintings — now permanent. Surrealist imagery, fine-line portraiture, and original flash art rooted in fine art tradition.</p>
  </div>

  <!-- STYLE -->
  <section>
    <div class="wrap rev">
      <p class="sec-label">The Style</p>
      <h2 class="sec-h">Fine Art<br><em>Made Permanent</em></h2>
      <p class="sec-sub">Every tattoo design is original. Nothing is repeated. The same ballpoint-pen precision, dreamlike imagery, and portraiture sensibility from the studio — now something you carry with you always.</p>
      <div class="grid-3" style="margin-bottom:0">
        <div class="card"><h3 class="card-h">Surrealist</h3><p class="card-body">Dreamlike imagery, symbolic objects, figures caught between worlds. Work that means something beyond surface decoration.</p></div>
        <div class="card"><h3 class="card-h">Fine Line</h3><p class="card-body">Precise linework informed by years of ballpoint pen illustration. Clean, controlled, built to age beautifully on skin.</p></div>
        <div class="card"><h3 class="card-h">Portrait</h3><p class="card-body">People, pets, loved ones. The same fine art portraiture sensibility — now something you carry with you always.</p></div>
      </div>
    </div>
  </section>

  <!-- PRICING -->
  <div class="banner">
    <div class="banner-in">
      <div class="rev">
        <p class="sec-label">Honest Pricing · San Francisco 2026</p>
        <h2 class="sec-h">Tattoo<br><em>Pricing</em></h2>
        <p class="sec-sub">Grounded in current San Francisco market rates for independent fine-art tattoo work. A deposit is required to hold every appointment.</p>
      </div>
      <div class="tat-grid rev">
        <div class="tat-tier">
          <p class="tier-cat">Studio Minimum</p>
          <h3 class="tier-name">Flash &amp; Micro</h3>
          <p class="tier-size">Up to 2 inches · Simple linework</p>
          <div class="tier-price">$150</div>
          <p class="tier-time">30–60 minutes</p>
          <p class="tier-desc">Small flash designs, minimal linework, single words or symbols. The studio minimum covers sterile setup, materials, and your artist's time — no matter the size.</p>
          <ul class="tier-incl">
            <li>Pre-designed flash from current sheet</li>
            <li>Single needle or fine line</li>
            <li>Placement consultation included</li>
            <li>Aftercare instructions provided</li>
          </ul>
        </div>
        <div class="tat-tier feat">
          <p class="tier-cat">Custom Small</p>
          <h3 class="tier-name">Custom Small</h3>
          <p class="tier-size">2–4 inches · Original design</p>
          <div class="tier-price">$250</div>
          <p class="tier-time">1–2 hours</p>
          <p class="tier-desc">Original custom design created specifically for you — surrealist motifs, small portraits, animal studies, botanical imagery. This piece is yours alone and will never be repeated.</p>
          <ul class="tier-incl">
            <li>Original design consultation</li>
            <li>Custom artwork created before your session</li>
            <li>One revision round on design</li>
            <li>Placement guidance and sizing</li>
            <li>Aftercare kit included</li>
          </ul>
        </div>
        <div class="tat-tier">
          <p class="tier-cat">Custom Medium</p>
          <h3 class="tier-name">Custom Medium</h3>
          <p class="tier-size">4–6 inches · Detailed work</p>
          <div class="tier-price">$400</div>
          <p class="tier-time">2–4 hours</p>
          <p class="tier-desc">The ideal size for detailed portraits, surrealist scenes, and fine-line compositions that need room to breathe. Most collectors find this the best balance of impact and healing.</p>
          <ul class="tier-incl">
            <li>Full custom design session</li>
            <li>Portrait or scene composition</li>
            <li>Two revision rounds on design</li>
            <li>May require two sessions for heavy detail</li>
            <li>Aftercare kit and follow-up check-in</li>
          </ul>
        </div>
        <div class="tat-tier">
          <p class="tier-cat">Large Piece</p>
          <h3 class="tier-name">Large &amp; Statement</h3>
          <p class="tier-size">6–10 inches · Statement work</p>
          <div class="tier-price">$700<span style="font-size:18px;color:var(--mst)">+</span></div>
          <p class="tier-time">4–6+ hours · May be multi-session</p>
          <p class="tier-desc">Sleeve sections, back pieces, thigh work, large-format surrealist compositions. Quoted individually based on design complexity and placement.</p>
          <ul class="tier-incl">
            <li>Comprehensive design consultation</li>
            <li>Multi-session planning if needed</li>
            <li>Full composition development</li>
            <li>Touch-up included within 60 days</li>
          </ul>
        </div>
        <div class="tat-tier">
          <p class="tier-cat">Special Rate</p>
          <h3 class="tier-name">Friend &amp; Loyalty Rate</h3>
          <p class="tier-size">Friends · Returning clients · Referrals</p>
          <div class="tier-price" style="font-size:28px;padding:6px 0">Ask Roberto</div>
          <p class="tier-time">Discussed at consultation</p>
          <p class="tier-desc">Roberto believes in taking care of the people who believe in him. Friends, returning collectors, and people who refer new clients are always welcomed with a rate that reflects the relationship. Just ask — no awkwardness, no pressure.</p>
          <ul class="tier-incl">
            <li>Discounted rate on any service</li>
            <li>Discussed privately and honestly</li>
            <li>Applies to tattoo and fine art work</li>
          </ul>
        </div>
        <div class="tat-tier">
          <p class="tier-cat">Hourly Rate</p>
          <h3 class="tier-name">Large Custom / Hourly</h3>
          <p class="tier-size">Complex large-format &amp; multi-session</p>
          <div class="tier-price">$150<span style="font-size:18px;color:var(--mst)">/hr</span></div>
          <p class="tier-time">Quoted per project at consultation</p>
          <p class="tier-desc">For projects better scoped hourly — large surrealist scenes, full sleeves, detailed portraiture spanning multiple sessions. Transparent time tracking throughout.</p>
          <ul class="tier-incl">
            <li>Project quote provided before booking</li>
            <li>Deposit applied toward total</li>
            <li>Session breaks included in timing</li>
            <li>Transparent time tracking</li>
          </ul>
        </div>
      </div>
    </div>
  </div>

  <!-- BOOKING POLICY -->
  <section>
    <div class="wrap rev">
      <p class="sec-label">Booking Policy</p>
      <h2 class="sec-h">How Tattoo<br><em>Bookings Work</em></h2>
      <div class="grid-2">
        <div class="card"><h3 class="card-h">Deposits</h3><p class="card-body">A non-refundable deposit of $50–$100 (depending on project size) is required to confirm your appointment. Applied toward your total. No session is confirmed without it.</p></div>
        <div class="card"><h3 class="card-h">Cancellation</h3><p class="card-body">More than 48 hours notice: deposit may be applied to a rescheduled appointment. Less than 48 hours notice or no-show: deposit is forfeited. Life happens — communicate early.</p></div>
        <div class="card"><h3 class="card-h">Design Ownership</h3><p class="card-body">Your custom design will not be tattooed on anyone else. Roberto retains the right to photograph and share the work unless you request otherwise in writing before your session.</p></div>
        <div class="card"><h3 class="card-h">Touch-Ups</h3><p class="card-body">One complimentary touch-up within 60 days, provided aftercare instructions were followed. Touch-ups needed from picking, sun exposure, or improper care are not covered.</p></div>
      </div>
      <div style="margin-top:32px;background:var(--obs);border:1px solid rgba(139,26,74,.5);padding:36px;text-align:center">
        <p style="font-family:'Playfair Display',serif;font-size:20px;font-style:italic;color:var(--crm);margin-bottom:8px">Flash designs revealed every Wednesday at 5 PM</p>
        <p style="font-size:15px;color:var(--mst);font-style:italic;margin-bottom:20px">Watch live on Facebook, Instagram, TikTok, and YouTube — claim a flash design in real time.</p>
        <div class="live-badge" style="display:inline-flex"><div class="live-dot"></div><span class="live-txt">Wednesday Lives · 5:00 PM · All Platforms</span></div>
      </div>
    </div>
  </section>
  <div class="cta-sec">
    <h2 class="cta-h">Book Your<br><em>Tattoo Consultation</em></h2>
    <p class="cta-p">Free consultation — no pressure, just a conversation about your vision.</p>
    <div class="btn-row" style="justify-content:center">
      <button class="btn btn-gold" onclick="go('contract')">Book a Consultation</button>
      <a href="https://wa.me/13412539299" target="_blank" class="btn btn-out">WhatsApp Roberto</a>
    </div>
  </div>
  <footer><p class="foot-logo">Lost <span>Soul</span> Art Studio</p><p class="foot-meta">Roberto Cisneros · San Francisco, CA</p><p class="foot-q">"The labyrinth of the creative mind is where the soul goes to find itself." © 2026</p></footer>
</div>

<!-- ══════════════════════════ PAGE: CONTRACT ══════════════════════════ -->
<div id="page-contract" class="page">
  <div style="padding-top:80px;background:var(--char);border-bottom:1px solid var(--bdr)">
    <div class="contract-hdr">
      <p style="font-family:'Josefin Sans',sans-serif;font-size:9px;letter-spacing:.5em;text-transform:uppercase;color:var(--gdk);margin-bottom:16px">Lost Soul Art Studio</p>
      <h1 style="font-family:'Playfair Display',serif;font-size:clamp(36px,6vw,64px);font-weight:900;color:var(--crm);margin-bottom:14px">Commission Agreement</h1>
      <p style="font-size:17px;color:var(--mst);font-style:italic;max-width:560px;margin:0 auto;line-height:1.8">This agreement is between you and Roberto Cisneros, the independent artist behind Lost Soul Art Studio. Please read every section before signing.</p>
      <div style="margin-top:22px;display:inline-block;background:rgba(200,169,81,.06);border:1px solid var(--bdr);padding:14px 22px">
        <p style="font-size:14px;color:var(--mst);font-style:italic">Note: Lost Soul Art Studio is an independent artist practice operated by Roberto Cisneros as a sole creative professional — not a registered LLC or incorporated business. This agreement is personal between you and Roberto Cisneros.</p>
      </div>
    </div>
  </div>
  <div class="contract-wrap">

    <div class="csec">
      <h3>Services Covered by This Agreement</h3>
      <p>Select the service you are commissioning below. The following descriptions explain exactly what each service includes and what both parties are committing to.</p>
      <ul>
        <li><strong style="color:var(--crm);font-style:normal">Fine Art Portrait</strong> — Original hand-painted portrait in acrylic, watercolor, or ballpoint pen. Includes reference consultation, work-in-progress updates, and delivery of the physical original.</li>
        <li><strong style="color:var(--crm);font-style:normal">Interior Mural</strong> — Custom acrylic mural painted on-site. Includes consultation, concept sketches, wall preparation, painting, and protective sealant.</li>
        <li><strong style="color:var(--crm);font-style:normal">Storefront Installation</strong> — Seasonal or custom window painting for your business. Includes design concept, one day of on-site work, and clean removal when the season ends.</li>
        <li><strong style="color:var(--crm);font-style:normal">Original Artwork Purchase</strong> — Purchase of an existing studio work. Includes signed certificate of authenticity and protective packaging.</li>
        <li><strong style="color:var(--crm);font-style:normal">Workshop / Instruction</strong> — Group or private instruction session in acrylic, watercolor, or ballpoint pen. Includes all materials and a finished piece to take home.</li>
        <li><strong style="color:var(--crm);font-style:normal">Tattoo — Custom Design</strong> — Original tattoo design created for you, tattooed by Roberto Cisneros. Includes design consultation, one revision round, and the session itself.</li>
        <li><strong style="color:var(--crm);font-style:normal">Tattoo — Flash Design</strong> — Pre-designed original from the current flash sheet. Done once — never repeated. Deposit required to hold your design.</li>
      </ul>
    </div>

    <div class="csec">
      <h3>Your Information</h3>
      <div class="form-row">
        <div class="form-group"><label>First Name</label><input type="text" placeholder="First name"></div>
        <div class="form-group"><label>Last Name</label><input type="text" placeholder="Last name"></div>
      </div>
      <div class="form-row">
        <div class="form-group"><label>Email Address</label><input type="email" placeholder="your@email.com"></div>
        <div class="form-group"><label>Phone Number</label><input type="tel" placeholder="(415) 000-0000"></div>
      </div>
      <div class="form-group"><label>City / Neighborhood</label><input type="text" placeholder="e.g. Mission District, SF"></div>
    </div>

    <div class="csec">
      <h3>Service Selection</h3>
      <div class="form-group">
        <label>Which service are you commissioning?</label>
        <select id="svc-select" onchange="calcTotal()">
          <option value="">— Select a service —</option>
          <optgroup label="Fine Art Portraits">
            <option value="150">Portrait — Small 5×7 ($150)</option>
            <option value="200">Portrait — Small 8×8 ($200)</option>
            <option value="275">Portrait — Small 8×10 ($275)</option>
            <option value="400">Portrait — Medium 11×14 ($400)</option>
            <option value="525">Portrait — Medium 12×12 ($525)</option>
            <option value="650">Portrait — Medium 12×16 ($650)</option>
            <option value="850">Portrait — Large 16×20 ($850)</option>
            <option value="1100">Portrait — Large 18×24 ($1,100)</option>
            <option value="1500">Portrait — Statement 24×36 ($1,500+)</option>
          </optgroup>
          <optgroup label="Murals">
            <option value="500">Interior Mural — Residential (starting $500)</option>
            <option value="1500">Interior Mural — Commercial (starting $1,500)</option>
          </optgroup>
          <optgroup label="Storefronts">
            <option value="200">Storefront — Tier I Minimalist ($200+)</option>
            <option value="450">Storefront — Tier II Standard/Seasonal ($450+)</option>
            <option value="800">Storefront — Tier III Signature/Full Mural ($800+)</option>
          </optgroup>
          <optgroup label="Workshops">
            <option value="100">Workshop — Group Studio Saturday ($100/student)</option>
            <option value="180">Workshop — Private One-on-One ($180)</option>
          </optgroup>
          <optgroup label="Tattoo">
            <option value="150">Tattoo — Flash &amp; Micro ($150 minimum)</option>
            <option value="250">Tattoo — Custom Small 2–4 inches ($250)</option>
            <option value="400">Tattoo — Custom Medium 4–6 inches ($400)</option>
            <option value="700">Tattoo — Large &amp; Statement 6–10 inches ($700+)</option>
            <option value="0">Tattoo — Friend / Loyalty Rate (discuss with Roberto)</option>
          </optgroup>
        </select>
      </div>
      <div class="form-group"><label>Describe your subject, idea, or project</label><textarea rows="4" placeholder="For portraits: describe who or what the subject is, any mood or story you want captured. For murals/storefronts: describe the space and theme. For tattoos: describe placement and design vision."></textarea></div>
      <div class="form-group"><label>Preferred medium — portraits only (optional)</label>
        <select><option>— Leave to Roberto's judgment —</option><option>Acrylic</option><option>Watercolor</option><option>Ballpoint Pen</option><option>Mixed</option></select>
      </div>
      <div class="form-row">
        <div class="form-group"><label>Desired size or dimensions</label><input type="text" placeholder='e.g. 11×14 or "as large as works"'></div>
        <div class="form-group"><label>Preferred timeline or deadline</label><input type="text" placeholder='"Before the holidays" or "No rush"'></div>
      </div>
      <div class="total-box">
        <span class="total-label">Starting Price Estimate</span>
        <span class="total-val" id="t-val">Select a service above</span>
      </div>
      <div style="margin-top:16px;padding:16px 20px;background:var(--obs);border:1px solid var(--bdr)">
        <p style="font-size:14px;color:var(--mst);font-style:italic">Deposit required (30% for portraits, 50% for all other services) via <a href="https://www.paypal.com/ncp/payment/8LZGEN2GHFUMU" target="_blank" style="color:var(--gold)">PayPal</a> or <a href="https://wa.me/13412539299" target="_blank" style="color:var(--gold)">WhatsApp</a>. Roberto will confirm details and send deposit instructions within 48 hours.</p>
      </div>
    </div>

    <div class="csec">
      <h3>What Roberto Agrees To</h3>
      <ul>
        <li>To create original work in the style and medium described, using acrylic, ballpoint pen, or watercolor as appropriate.</li>
        <li>To communicate at key stages so you are never surprised by the direction of the work.</li>
        <li>To deliver within the agreed timeline, or notify you promptly if circumstances require a change.</li>
        <li>To treat your reference materials, story, and project with the care he brings to his own work.</li>
        <li>To keep your personal information and reference photos private and use them solely for your commission.</li>
      </ul>
    </div>

    <div class="csec">
      <h3>What You Are Agreeing To</h3>
      <ul>
        <li>To pay the required deposit before any work begins. No work starts without a confirmed deposit.</li>
        <li>To pay the remaining balance when the work is complete and approved — or for tattoos, on the day of your session.</li>
        <li>To provide clear reference materials in a timely manner so work can proceed as planned.</li>
        <li>To communicate concerns during the work-in-progress phase — changes requested after completion may incur additional fees.</li>
        <li>For tattoo clients: to follow all aftercare instructions provided. Touch-ups needed due to improper care are not covered.</li>
        <li>To allow Roberto Cisneros to photograph and share the completed work on his portfolio and social media unless you request otherwise in writing before work begins.</li>
      </ul>
    </div>

    <div class="csec">
      <h3>Refund &amp; Cancellation</h3>
      <ul>
        <li>Deposits are non-refundable under all circumstances, except if Roberto is unable to complete the commission — in which case your deposit is returned in full within 14 days.</li>
        <li>Refunds are not issued for completed work. Any concerns about a finished piece will be addressed at Roberto's discretion.</li>
        <li>Murals/storefronts cancelled after on-site work has begun: a 25% kill fee of the total quoted price applies in addition to the deposit.</li>
        <li>Tattoo cancellations with less than 48 hours notice forfeit the full deposit. More than 48 hours notice may allow the deposit to roll to a rescheduled appointment at Roberto's discretion.</li>
      </ul>
    </div>

    <div class="csec">
      <h3>Copyright &amp; Ownership</h3>
      <ul>
        <li>Roberto Cisneros retains full copyright and reproduction rights to all original works.</li>
        <li>You receive the physical artwork and the right to display and enjoy it personally.</li>
        <li>You may not reproduce, sell, or use images of the work for commercial purposes without written permission.</li>
        <li>For tattoo designs: your custom design will not be tattooed on anyone else. Design copyright remains with the artist.</li>
        <li>Personal, non-commercial sharing on social media is welcome and encouraged. Please tag @lostsoulart.</li>
      </ul>
    </div>

    <div class="csec">
      <h3>Please Confirm the Following</h3>
      <div class="chk-group">
        <label class="chk-item"><input type="checkbox"><span>I have read and understood the full description of the service I am commissioning.</span></label>
        <label class="chk-item"><input type="checkbox"><span>I understand that a deposit is required before work begins and is non-refundable.</span></label>
        <label class="chk-item"><input type="checkbox"><span>I understand that Roberto Cisneros retains copyright to all original work created.</span></label>
        <label class="chk-item"><input type="checkbox"><span>I agree to the refund and cancellation policy described above.</span></label>
        <label class="chk-item"><input type="checkbox"><span>I consent to Roberto Cisneros photographing and sharing the completed work on his portfolio and social media.</span></label>
        <label class="chk-item" id="tat-chk" style="display:none"><input type="checkbox"><span>For tattoo services: I confirm I am 18 years of age or older and have read the tattoo booking policy.</span></label>
      </div>
    </div>

    <div class="csec">
      <h3>Signature &amp; Agreement</h3>
      <p>By typing your name below, you confirm that you have read this agreement in full and agree to all terms. This is a personal agreement between you and Roberto Cisneros, entered into voluntarily by both parties.</p>
      <div class="form-row" style="margin-top:28px">
        <div class="sig-block">
          <label style="font-family:'Josefin Sans',sans-serif;font-size:9px;letter-spacing:.4em;text-transform:uppercase;color:var(--gdk);display:block;margin-bottom:8px">Your Full Name (typed signature)</label>
          <input type="text" class="sig-input" placeholder="Type your full name to sign">
        </div>
        <div class="form-group">
          <label>Date</label>
          <input type="date" id="sig-date">
        </div>
      </div>
      <div style="margin-top:40px;text-align:center">
        <button class="btn btn-gold" style="width:100%;max-width:380px" onclick="submitForm()">Submit Commission Agreement</button>
        <p style="font-size:13px;color:var(--mst);font-style:italic;margin-top:14px">Roberto will contact you within 48 hours to confirm details and arrange your deposit.</p>
        <div style="margin-top:20px;display:flex;gap:14px;justify-content:center;flex-wrap:wrap">
          <a href="https://www.paypal.com/ncp/payment/8LZGEN2GHFUMU" target="_blank" class="btn btn-out" style="font-size:8px">Pay via PayPal</a>
          <a href="https://wa.me/13412539299" target="_blank" class="btn btn-out" style="font-size:8px">WhatsApp Roberto</a>
        </div>
      </div>
    </div>
  </div>
  <footer><p class="foot-logo">Lost <span>Soul</span> Art Studio</p><p class="foot-meta">Roberto Cisneros · San Francisco, CA</p><p class="foot-q">"The labyrinth of the creative mind is where the soul goes to find itself." © 2026</p></footer>
</div>

<!-- ══════════════════════════ PAGE: BLOG ══════════════════════════ -->
<div id="page-blog" class="page">
  <div class="hero" style="min-height:50vh;padding:130px 40px 60px">
    <div class="hero-bg"></div>
    <p class="eyebrow">Lost Soul Art Studio</p>
    <h1 style="font-size:clamp(44px,8vw,88px)">Creative<br><em>Art Blog</em></h1>
    <p class="hero-sub">Thoughts on the creative process, the artist's journey, and the ongoing conversation between art, identity, and imagination.</p>
  </div>
  <section>
    <div class="wrap">
      <div class="blog-grid rev">
        <div class="blog-card">
          <img src="https://lostsoulart.simdif.com/images/th/sd_6969c62e7f820.jpg?no_cache=1768543300" alt="Lost Soul Art Blog">
          <div class="blog-body">
            <p class="blog-date">January 15, 2026</p>
            <h3 class="blog-h">Lost Soul: The Artist, The Creativity &amp; The Brand</h3>
            <p class="blog-p">In a world that demands we fit into neat, labeled boxes, there is a profound power in being "lost." For the creator, being a Lost Soul isn't about being aimless — it is the raw, unpolished space where the artist, the creative process, and the brand identity finally collide.</p>
            <p class="blog-p" style="margin-top:12px">Every artist starts as a seeker. We create because we are looking for something — a feeling, a truth, or a way to explain the static in our heads. Embracing vulnerability. Rejecting perfection. Authenticity over conformity. Stay lost. Keep creating. Find yourself in the work.</p>
          </div>
        </div>
        <div class="blog-card">
          <img src="https://lostsoulart.simdif.com/images/th/sd_696ce60557266.jpg?no_cache=1768748102" alt="Creative Block">
          <div class="blog-body">
            <p class="blog-date">January 18, 2026</p>
            <h3 class="blog-h">The Creative Block: When the Well Runs Dry</h3>
            <p class="blog-p">Every artist, no matter how seasoned or brilliant, has faced it — the dreaded creative block. It's a completely normal part of the creative process, and more importantly, something you can absolutely overcome.</p>
            <p class="blog-p" style="margin-top:12px">Change your scenery. Engage in mindless creation. Learn something new. Revisit old work. Set small, achievable goals. Embrace constraints. True innovation happens in the Lost State — where time disappears and you aren't just making art, you are letting the art happen through you.</p>
          </div>
        </div>
        <div class="blog-card">
          <img src="https://lostsoulart.simdif.com/images/th/sd_698d319f2190a.png?no_cache=1770864584" alt="Pre Renewal Phase">
          <div class="blog-body">
            <p class="blog-date">February 12, 2026</p>
            <h3 class="blog-h">Pre Renewal Phase: The Journey Behind the Brush Stroke</h3>
            <p class="blog-p">"The labyrinth of the creative mind is where the soul goes to find itself." This quote isn't just a footer on my website — it is the heartbeat of every morning I spend in the studio.</p>
            <p class="blog-p" style="margin-top:12px">In my latest work for The Renewal Collection, I've been leaning into the chaos of the line. By layering raw, evocative strokes over structured forms, I'm exploring the bridge between classical training and the contemporary expressionism that feels so urgent right now. Art isn't just about the finished product — it's about the messy, beautiful process of getting lost so you can finally be found.</p>
          </div>
        </div>
      </div>
      <div style="margin-top:60px;text-align:center" class="rev">
        <p style="font-size:17px;color:var(--mst);font-style:italic;margin-bottom:28px">New blog posts published monthly. Follow along on social media for weekly creative updates and live painting sessions every Wednesday at 5 PM.</p>
        <div class="live-badge" style="display:inline-flex"><div class="live-dot"></div><span class="live-txt">Watch Live Every Wednesday · 5 PM · All Platforms</span></div>
      </div>
    </div>
  </section>
  <footer><p class="foot-logo">Lost <span>Soul</span> Art Studio</p><p class="foot-meta">Roberto Cisneros · San Francisco, CA</p><p class="foot-q">"The labyrinth of the creative mind is where the soul goes to find itself." © 2026</p></footer>
</div>

<!-- ══════════════════════════ PAGE: TERMS ══════════════════════════ -->
<div id="page-terms" class="page">
  <div style="padding-top:100px;background:var(--char);border-bottom:1px solid var(--bdr);text-align:center;padding-bottom:56px">
    <p style="font-family:'Josefin Sans',sans-serif;font-size:9px;letter-spacing:.5em;text-transform:uppercase;color:var(--gdk);margin-bottom:16px">Lost Soul Art Studio</p>
    <h1 style="font-family:'Playfair Display',serif;font-size:clamp(34px,6vw,62px);font-weight:900;color:var(--crm);margin-bottom:12px">Terms of Service</h1>
    <p style="font-size:17px;color:var(--mst);font-style:italic;max-width:540px;margin:0 auto;line-height:1.8">These terms govern all services provided by Roberto Cisneros under the Lost Soul Art Studio name. Please read fully before engaging any service.</p>
    <p style="font-family:'Josefin Sans',sans-serif;font-size:9px;letter-spacing:.3em;text-transform:uppercase;color:var(--mst);margin-top:18px">Last Updated: April 2026</p>
  </div>
  <div class="terms-wrap">
    <div class="t-sec">
      <div class="t-num">01</div>
      <h3>Who These Terms Apply To</h3>
      <p>These Terms of Service apply to anyone who commissions, purchases, or engages any service offered by Roberto Cisneros operating as Lost Soul Art Studio — including fine art portrait commissions, interior murals, storefront window installations, studio workshops, original artwork purchases, print sales, and tattoo services.</p>
      <p>Lost Soul Art Studio is an independent artist practice. Roberto Cisneros operates as a sole creative professional and is not a registered LLC, corporation, or formally licensed business entity. These terms constitute a personal agreement between you and Roberto Cisneros as an individual artist.</p>
    </div>
    <div class="t-sec">
      <div class="t-num">02</div>
      <h3>Payment Terms</h3>
      <p>Portrait commissions require a 30% non-refundable deposit to secure your place in the production calendar. All other commissions (murals, storefronts, tattoos) require a 50% non-refundable deposit before work begins. No work commences until the deposit is received.</p>
      <p>The remaining balance is due upon completion and your approval of the work — or for tattoos, on the day of your appointment before the session begins.</p>
      <p>Accepted payment methods: PayPal (link provided on the portraits page), Venmo, cash, and bank transfer. Payment plans for commissions over $1,000 may be arranged at Roberto's discretion — discuss during consultation.</p>
    </div>
    <div class="t-sec">
      <div class="t-num">03</div>
      <h3>Deposits &amp; Refund Policy</h3>
      <p>Deposits are non-refundable under all circumstances, except in the case where Roberto Cisneros is unable to fulfill the commission — in which case the deposit is returned in full within 14 days.</p>
      <p>Refunds are not issued for completed work. If you have a concern about a finished piece, Roberto will make reasonable efforts to address it, but the decision on how to respond rests entirely with him as the artist.</p>
      <p>For murals and large-scale commercial projects cancelled after on-site work has commenced, a kill fee of 25% of the total quoted price applies in addition to the non-refundable deposit.</p>
    </div>
    <div class="t-sec">
      <div class="t-num">04</div>
      <h3>Timelines &amp; Delivery</h3>
      <p>Estimated timelines are provided in good faith but are not guaranteed. Roberto will communicate with you if a timeline needs to shift. Standard timelines: portrait commissions 2–4 weeks from deposit; mural projects 1–5 days on-site; storefront installations one day; tattoo sessions scheduled at time of booking.</p>
      <p>Rush portrait commissions (under 10 days) are available at a 25% surcharge if capacity allows — discuss before placing your deposit.</p>
    </div>
    <div class="t-sec">
      <div class="t-num">05</div>
      <h3>Copyright &amp; Intellectual Property</h3>
      <p>Roberto Cisneros retains full copyright and reproduction rights to all original works created, including portrait commissions, mural designs, tattoo designs, flash sheets, and any preparatory sketches.</p>
      <p>Clients receive the physical artwork and the right to display and enjoy it personally and non-commercially. Clients may share images of their commissioned work on personal social media. Tagging @lostsoulart is always appreciated.</p>
      <p>Clients may not reproduce, sell, license, or use images of commissioned work for commercial purposes without prior written permission from Roberto Cisneros.</p>
      <p>For tattoo clients: custom tattoo designs will not be repeated on another person. The design copyright — the right to reproduce, print, or sell the image — remains with Roberto Cisneros as the artist.</p>
    </div>
    <div class="t-sec">
      <div class="t-num">06</div>
      <h3>Reference Materials &amp; Privacy</h3>
      <p>Reference photos and any personal information shared with Roberto Cisneros for your commission are kept private and used solely for that purpose. They will not be shared with any third party.</p>
      <p>By submitting reference photos, you confirm that you have the right to share those images and that they do not infringe on any third party's rights. Completed commissions may be photographed and shared on Roberto's portfolio and social media. If you prefer your commission remain private, notify Roberto in writing before your deposit is placed.</p>
    </div>
    <div class="t-sec">
      <div class="t-num">07</div>
      <h3>Workshops &amp; Events</h3>
      <p>Workshop fees are non-refundable within 48 hours of the scheduled session date. Cancellations with more than 48 hours notice may receive a studio credit toward a future session at Roberto's discretion. All workshop materials are included in the session fee. Students take home their completed work.</p>
    </div>
    <div class="t-sec">
      <div class="t-num">08</div>
      <h3>Tattoo Services</h3>
      <p>All tattoo services are provided by Roberto Cisneros as an independent tattoo artist. A non-refundable deposit of $50–$100 is required to hold your appointment. Cancellations with less than 48 hours notice forfeit the deposit entirely. Cancellations with more than 48 hours notice may have the deposit applied to a rescheduled appointment at Roberto's discretion.</p>
      <p>One complimentary touch-up is included within 60 days of your appointment for work that has been properly cared for. Touch-ups needed due to picking, sun exposure, or improper aftercare are billed at the standard rate.</p>
      <p>All tattoo clients must be 18 years of age or older. By booking a tattoo appointment, you confirm you are of legal age.</p>
    </div>
    <div class="t-sec">
      <div class="t-num">09</div>
      <h3>Limitation of Liability</h3>
      <p>Roberto Cisneros's total liability for any claim or damage arising from services provided under the Lost Soul Art Studio name shall not exceed the total amount paid by the client for that specific service.</p>
      <p>Roberto Cisneros is not liable for any indirect, incidental, or consequential damages arising from commissioned work, including but not limited to loss of business, damage to property where work is installed, or dissatisfaction with artistic style.</p>
    </div>
    <div class="t-sec">
      <div class="t-num">10</div>
      <h3>Agreement &amp; Contact</h3>
      <p>By engaging any service provided by Lost Soul Art Studio, you confirm that you have read and agree to these Terms of Service. These terms may be updated periodically — the current version is always available on this page.</p>
      <p>For questions, concerns, or to start a commission: reach Roberto Cisneros via <a href="https://wa.me/13412539299" target="_blank" style="color:var(--gold)">WhatsApp</a> or through the Commission page on this site. All communications are responded to within 48 hours.</p>
    </div>
    <div style="margin-top:48px;text-align:center">
      <button class="btn btn-gold" onclick="go('contract')">Start a Commission</button>
    </div>
  </div>
  <footer><p class="foot-logo">Lost <span>Soul</span> Art Studio</p><p class="foot-meta">Roberto Cisneros · San Francisco, CA</p><p class="foot-q">"The labyrinth of the creative mind is where the soul goes to find itself." © 2026 Lost Soul Art Studio. All Rights Reserved.</p></footer>
</div>

<script>
// ── Gallery data ──────────────────────────────────────────────────────
const artworks = [
  {src:"sd_6960b6bc6042c",title:"The Lost Soul"},
  {src:"sd_6960b6eda8c79",title:"Rebellious"},
  {src:"sd_6960b75a5f55d",title:"Opening the 3rd Eye"},
  {src:"sd_6961163e36540",title:"A Child of Rebellion"},
  {src:"sd_6961186390c3d",title:"Lost Skull"},
  {src:"sd_6961187a8cb70",title:"Sunset Watercolor"},
  {src:"sd_696118a09104f",title:"Beautiful Angel"},
  {src:"sd_696118bd8d258",title:"Bang Bang"},
  {src:"sd_696118d7d2eb0",title:"Before"},
  {src:"sd_696118f828591",title:"After"},
  {src:"sd_69611906c780c",title:"Inside My Head"},
  {src:"sd_6961191f78095",title:"Down the Rabbit Hole"},
  {src:"sd_69611934e540a",title:"Flip Through the Pages"},
  {src:"sd_6961194839a6d",title:"10 Min Portrait of Cameron"},
  {src:"sd_6961195f6b077",title:"Heart of Gold"},
  {src:"sd_6961197b527e1",title:"Princess of Hearts"},
  {src:"sd_696119a390eed",title:"The Duality of It All"},
  {src:"sd_69611a0f8684c",title:"Is That Britney?"},
  {src:"sd_69611a7e7297a",title:"Rose on Thigh"},
  {src:"sd_69611a40a03b1",title:"Thizz Face"},
  {src:"sd_69611a908cb77",title:"Pop Art"},
  {src:"sd_69611ac43e283",title:"Ball Point Pen Self Portrait"},
  {src:"sd_69611addad79a",title:"Butterfly Spirit"},
  {src:"sd_69611ab210abb",title:"Alien"},
  {src:"sd_69611b4ec3b48",title:"Aaaahhhhh"},
  {src:"sd_69611b5fd49f1",title:"Transcend to Your Highest Vibrational Self"},
  {src:"sd_69611b937b7d9",title:"Self"},
  {src:"sd_69611af573cff",title:"Ariel / Alter Ego"},
  {src:"sd_69611b2f1ba4f",title:"Blue Rose"},
  {src:"sd_69611b17a8d28",title:"My Grandpa"},
  {src:"sd_69ac0471e561f",title:"Childlike Wonder"},
];

function buildGallery(){
  const g = document.getElementById('gallery-grid');
  artworks.forEach(a=>{
    const url = `https://lostsoulart.simdif.com/images/th/${a.src}.jpg?no_cache=1767949552`;
    const bigUrl = `https://lostsoulart.simdif.com/images/public/${a.src}.jpg?no_cache=1767949552`;
    const el = document.createElement('div');
    el.className='gal-item';
    el.innerHTML=`<img src="${url}" alt="${a.title}" loading="lazy"><div class="gal-cap">${a.title}</div>`;
    el.onclick=()=>openLB(bigUrl,a.title);
    g.appendChild(el);
  });
}

function openLB(src,cap){
  document.getElementById('lb-img').src=src;
  document.getElementById('lb-cap').textContent=cap;
  document.getElementById('lb').classList.add('open');
  document.body.style.overflow='hidden';
}
function closeLB(e){
  if(!e||e.target===document.getElementById('lb')||e.target.classList.contains('lb-close')){
    document.getElementById('lb').classList.remove('open');
    document.body.style.overflow='';
  }
}

// ── Page navigation ───────────────────────────────────────────────────
function go(page){
  document.querySelectorAll('.page').forEach(p=>p.classList.remove('active'));
  document.querySelectorAll('.nav-links a').forEach(a=>a.classList.remove('active'));
  document.getElementById('page-'+page).classList.add('active');
  const nav = document.getElementById('n-'+page);
  if(nav) nav.classList.add('active');
  window.scrollTo({top:0,behavior:'smooth'});
  document.getElementById('nav-links').classList.remove('open');
  if(page==='contract'){
    const d=new Date();
    document.getElementById('sig-date').valueAsDate=d;
  }
}

function toggleMenu(){
  document.getElementById('nav-links').classList.toggle('open');
}

// ── Contract logic ────────────────────────────────────────────────────
function calcTotal(){
  const s=document.getElementById('svc-select');
  const v=parseInt(s.value)||0;
  const tv=document.getElementById('t-val');
  const tc=document.getElementById('tat-chk');
  if(!s.value){tv.textContent='Select a service above';return;}
  if(s.value==='0'){tv.textContent='Discuss with Roberto';tc.style.display='flex';return;}
  const isTat=s.options[s.selectedIndex].parentElement.label==='Tattoo';
  tc.style.display=isTat?'flex':'none';
  const dep=s.value&&parseInt(s.value)>=400?Math.round(v*.3):Math.round(v*.5);
  tv.textContent=`$${v.toLocaleString()} · Deposit: $${dep.toLocaleString()}`;
}

function submitForm(){
  const checks=document.querySelectorAll('.chk-group input[type=checkbox]:not([style*="none"])');
  let allChecked=true;
  checks.forEach(c=>{if(!c.checked)allChecked=false;});
  const sig=document.querySelector('.sig-input').value.trim();
  if(!sig){alert('Please type your full name to sign the agreement.');return;}
  if(!allChecked){alert('Please check all confirmation boxes before submitting.');return;}
  const svc=document.getElementById('svc-select').value;
  if(!svc){alert('Please select a service.');return;}
  alert('Thank you! Roberto will contact you within 48 hours to confirm your commission details and arrange the deposit. You can also reach him directly via WhatsApp: +1 (341) 253-9299');
}

// ── Scroll reveal ─────────────────────────────────────────────────────
const ro = new IntersectionObserver(entries=>{
  entries.forEach((e,i)=>{
    if(e.isIntersecting){
      setTimeout(()=>e.target.classList.add('vis'), i*60);
      ro.unobserve(e.target);
    }
  });
},{threshold:.07});
function activateReveal(){document.querySelectorAll('.rev').forEach(el=>ro.observe(el));}

// ── Init ──────────────────────────────────────────────────────────────
document.addEventListener('DOMContentLoaded',()=>{
  buildGallery();
  activateReveal();
  document.getElementById('sig-date').valueAsDate=new Date();
});

// Re-observe on page change
const origGo=go;
window.go=function(page){
  origGo(page);
  setTimeout(activateReveal,100);
};
</script>
</body>
</html>
