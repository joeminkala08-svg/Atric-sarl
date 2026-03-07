<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>ATRIC SARL – African Trade and Industry Company</title>
<link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Oswald:wght@300;400;600;700&family=Lato:ital,wght@0,300;0,400;0,700;1,300&display=swap" rel="stylesheet"/>
<style>
:root {
  --gold:#D4AF37; --gold2:#EDD060; --gold3:#A0841A;
  --dark:#0f0f0f; --dark2:#1a1a1a; --dark3:#222; --dark4:#2c3e50;
  --white:#fff; --muted:rgba(255,255,255,0.5); --muted2:rgba(255,255,255,0.75);
  --F:'Bebas Neue',sans-serif; --T:'Oswald',sans-serif; --B:'Lato',sans-serif;
}
*{box-sizing:border-box;margin:0;padding:0}
html{scroll-behavior:smooth}
body{background:var(--dark);color:#fff;font-family:var(--B);overflow-x:hidden}
a{text-decoration:none;color:inherit}
::-webkit-scrollbar{width:4px}::-webkit-scrollbar-thumb{background:var(--gold)}

/* ── TOPBAR ── */
.topbar{background:#000;border-bottom:1px solid rgba(212,175,55,.2);padding:8px 40px;display:flex;justify-content:space-between;align-items:center;font-size:.72rem;color:var(--muted)}
.tb-left{display:flex;gap:24px;align-items:center}
.tb-left span{display:flex;align-items:center;gap:7px}
.tb-left a{color:var(--gold)}
.tb-right{display:flex;gap:14px}
.tb-right a{color:var(--muted);transition:color .2s}
.tb-right a:hover{color:var(--gold)}
.ico{width:14px;height:14px;stroke:var(--gold);fill:none;stroke-width:2;stroke-linecap:round;stroke-linejoin:round}
.ico-fill{width:15px;height:15px;fill:currentColor}

/* ── NAV ── */
nav{position:sticky;top:0;z-index:999;height:68px;background:rgba(15,15,15,.97);backdrop-filter:blur(14px);border-bottom:2px solid var(--gold);padding:0 40px;display:flex;align-items:center;justify-content:space-between}
.logo{display:flex;align-items:center}
.logo-main{font-family:var(--F);font-size:1.8rem;color:var(--gold);letter-spacing:5px;line-height:1}
.logo-sub{font-family:var(--T);font-size:.5rem;letter-spacing:4px;color:rgba(255,255,255,.35);text-transform:uppercase}
.nav-links{display:flex;list-style:none;gap:4px}
.nav-links>li>a{display:block;padding:0 14px;height:68px;line-height:68px;font-family:var(--T);font-size:.72rem;letter-spacing:1.8px;text-transform:uppercase;color:rgba(255,255,255,.65);transition:color .2s;white-space:nowrap}
.nav-links>li>a:hover{color:var(--gold)}
.has-drop{position:relative}
.drop{display:none;position:absolute;top:100%;left:0;background:#1a1a1a;border:1px solid rgba(212,175,55,.25);border-top:2px solid var(--gold);min-width:220px;list-style:none;z-index:99}
.has-drop:hover .drop{display:block}
.drop li a{display:block;padding:12px 20px;font-family:var(--T);font-size:.7rem;letter-spacing:1.5px;text-transform:uppercase;color:var(--muted2);border-bottom:1px solid rgba(255,255,255,.04);transition:color .2s,padding-left .2s}
.drop li a:hover{color:var(--gold);padding-left:28px}
.btn-nav{background:var(--gold);color:#000;font-family:var(--T);font-size:.75rem;letter-spacing:2px;text-transform:uppercase;padding:11px 22px;border:none;cursor:pointer;transition:background .2s;white-space:nowrap}
.btn-nav:hover{background:var(--gold2)}

/* ── BUTTONS ── */
.btn-g{display:inline-block;background:var(--gold);color:#000;font-family:var(--T);font-size:.8rem;letter-spacing:2px;text-transform:uppercase;padding:14px 32px;border:none;cursor:pointer;transition:background .2s,transform .2s}
.btn-g:hover{background:var(--gold2);transform:translateY(-2px)}
.btn-w{display:inline-block;background:transparent;color:#fff;font-family:var(--T);font-size:.8rem;letter-spacing:2px;text-transform:uppercase;padding:13px 30px;border:1.5px solid rgba(255,255,255,.4);cursor:pointer;transition:border-color .2s,color .2s}
.btn-w:hover{border-color:var(--gold);color:var(--gold)}
.btn-og{display:inline-block;background:transparent;color:var(--gold);font-family:var(--T);font-size:.75rem;letter-spacing:2px;text-transform:uppercase;padding:11px 24px;border:1.5px solid var(--gold);cursor:pointer;transition:background .2s,color .2s}
.btn-og:hover{background:var(--gold);color:#000}

/* ── LABELS ── */
.tag{display:inline-flex;align-items:center;gap:10px;font-family:var(--T);font-size:.65rem;letter-spacing:5px;color:var(--gold);text-transform:uppercase;margin-bottom:12px}
.tag::before{content:'';width:26px;height:1.5px;background:var(--gold)}
.h2s{font-family:var(--F);font-size:clamp(2.2rem,4.5vw,3.6rem);line-height:1;text-transform:uppercase;color:#fff;margin-bottom:16px}
.h2s .a{color:var(--gold)}
.bar{width:48px;height:2.5px;background:var(--gold);margin-bottom:28px}
.bar.c{margin-left:auto;margin-right:auto}

/* ══════════════════════════
   HERO
══════════════════════════ */
#hero{min-height:100vh;position:relative;display:flex;align-items:center;justify-content:center;text-align:center;overflow:hidden}

/* SVG background scene */
.hero-scene{position:absolute;inset:0;z-index:0}
.hero-overlay{position:absolute;inset:0;z-index:1;background:linear-gradient(160deg,rgba(0,0,0,.88) 0%,rgba(15,25,40,.75) 50%,rgba(0,0,0,.92) 100%)}
/* animated grid */
.hero-grid-anim{position:absolute;inset:0;z-index:2;overflow:hidden}
.hero-grid-anim::before{content:'';position:absolute;inset:-50%;background-image:linear-gradient(rgba(212,175,55,.035) 1px,transparent 1px),linear-gradient(90deg,rgba(212,175,55,.035) 1px,transparent 1px);background-size:70px 70px;animation:gridSlide 18s linear infinite}
@keyframes gridSlide{to{transform:translate(70px,70px)}}
/* glow orbs */
.orb{position:absolute;border-radius:50%;filter:blur(80px);animation:orbPulse 7s ease-in-out infinite alternate}
.orb1{width:500px;height:500px;background:rgba(212,175,55,.06);top:-100px;left:-100px;animation-delay:0s}
.orb2{width:400px;height:400px;background:rgba(44,62,80,.4);bottom:-80px;right:-80px;animation-delay:3s}
.orb3{width:300px;height:300px;background:rgba(212,175,55,.04);top:40%;left:60%;animation-delay:1.5s}
@keyframes orbPulse{from{opacity:.5;transform:scale(1)}to{opacity:1;transform:scale(1.2)}}
/* diagonal cut */
.hero-cut{position:absolute;bottom:0;left:0;right:0;height:90px;background:var(--dark);clip-path:polygon(0 100%,100% 100%,100% 0);z-index:3}

.hero-body{position:relative;z-index:4;max-width:920px;padding:80px 24px 130px}
.hero-badge{display:inline-flex;align-items:center;gap:10px;background:rgba(212,175,55,.1);border:1px solid rgba(212,175,55,.3);padding:7px 20px;margin-bottom:32px;font-family:var(--T);font-size:.62rem;letter-spacing:5px;color:var(--gold);text-transform:uppercase;animation:up .9s .1s both}
.dot{width:6px;height:6px;border-radius:50%;background:var(--gold);animation:blink 2s infinite}
@keyframes blink{0%,100%{opacity:1}50%{opacity:.15}}
.hero-h1{font-family:var(--F);font-size:clamp(3rem,8vw,6.5rem);line-height:.95;text-transform:uppercase;margin-bottom:22px;animation:up .9s .25s both}
.hero-h1 span{color:var(--gold);display:block}
.hero-p{font-size:clamp(.9rem,1.8vw,1.1rem);font-weight:300;color:var(--muted2);line-height:1.8;max-width:640px;margin:0 auto 40px;animation:up .9s .4s both}
.hero-btns{display:flex;gap:14px;justify-content:center;flex-wrap:wrap;animation:up .9s .55s both}
.scroll-hint{position:absolute;bottom:100px;left:50%;transform:translateX(-50%);z-index:4;display:flex;flex-direction:column;align-items:center;gap:8px;font-family:var(--T);font-size:.58rem;letter-spacing:4px;color:var(--gold);text-transform:uppercase;animation:float 2.5s ease-in-out infinite}
.scroll-line{width:1px;height:46px;background:linear-gradient(var(--gold),transparent)}
@keyframes up{from{opacity:0;transform:translateY(26px)}to{opacity:1;transform:none}}
@keyframes float{0%,100%{transform:translateX(-50%) translateY(0)}50%{transform:translateX(-50%) translateY(8px)}}

/* ══════════════════════════
   ABOUT STRIP (quick intro)
══════════════════════════ */
#about-strip{background:var(--dark2);padding:70px 40px}
.about-strip-grid{max-width:1100px;margin:0 auto;display:grid;grid-template-columns:1fr 1fr 1fr;gap:0}
.as-item{padding:40px 36px;border-right:1px solid rgba(212,175,55,.12);position:relative}
.as-item:last-child{border-right:none}
.as-icon{width:52px;height:52px;border:1.5px solid var(--gold);display:flex;align-items:center;justify-content:center;margin-bottom:20px;color:var(--gold)}
.as-icon svg{width:24px;height:24px;stroke:currentColor;fill:none;stroke-width:1.5;stroke-linecap:round;stroke-linejoin:round}
.as-title{font-family:var(--T);font-size:1.05rem;letter-spacing:1.5px;text-transform:uppercase;color:#fff;margin-bottom:10px;font-weight:600}
.as-text{font-size:.85rem;color:var(--muted2);line-height:1.75}

/* ══════════════════════════
   DEPARTMENTS
══════════════════════════ */
#depts{background:var(--dark3);padding:100px 40px}
.depts-intro{max-width:1100px;margin:0 auto 64px}
.dept-grid{max-width:1100px;margin:0 auto;display:grid;grid-template-columns:repeat(5,1fr);gap:3px}
.dc{background:var(--dark2);padding:36px 26px 32px;position:relative;overflow:hidden;transition:transform .3s}
.dc::before{content:'';position:absolute;top:0;left:0;right:0;height:3px;background:var(--gold);transform:scaleX(0);transform-origin:left;transition:transform .4s}
.dc:hover{transform:translateY(-6px)}
.dc:hover::before{transform:scaleX(1)}
.dc-num{font-family:var(--F);font-size:3.5rem;color:rgba(212,175,55,.1);line-height:1;margin-bottom:16px;transition:color .3s}
.dc:hover .dc-num{color:rgba(212,175,55,.22)}
.dc-icon{color:var(--gold);margin-bottom:16px}
.dc-icon svg{width:30px;height:30px;stroke:currentColor;fill:none;stroke-width:1.5;stroke-linecap:round;stroke-linejoin:round}
.dc-title{font-family:var(--T);font-size:.95rem;letter-spacing:1.5px;text-transform:uppercase;color:#fff;margin-bottom:12px;font-weight:600;line-height:1.3}
.dc-prob{font-size:.7rem;color:#e74c3c;font-style:italic;margin-bottom:12px;line-height:1.4}
.dc-list{list-style:none;display:flex;flex-direction:column;gap:7px}
.dc-list li{font-size:.78rem;color:var(--muted2);display:flex;align-items:flex-start;gap:8px;line-height:1.4}
.dc-list li::before{content:'';width:5px;height:5px;border-radius:50%;background:var(--gold);flex-shrink:0;margin-top:5px}

/* ══════════════════════════
   IMPACT
══════════════════════════ */
#impact{background:var(--gold)}
.impact-row{display:grid;grid-template-columns:repeat(4,1fr)}
.imp{padding:56px 20px;text-align:center;border-right:1px solid rgba(0,0,0,.12)}
.imp:last-child{border-right:none}
.imp-num{font-family:var(--F);font-size:4.5rem;color:#000;line-height:1;margin-bottom:8px}
.imp-label{font-family:var(--T);font-size:.7rem;letter-spacing:2.5px;text-transform:uppercase;color:rgba(0,0,0,.6)}
.imp-desc{font-size:.78rem;color:rgba(0,0,0,.5);margin-top:6px;line-height:1.5}

/* ══════════════════════════
   CEO
══════════════════════════ */
#ceo{background:var(--dark4);padding:100px 40px;overflow:hidden;position:relative}
#ceo::before{content:'';position:absolute;top:-100px;right:-100px;width:500px;height:500px;border-radius:50%;background:radial-gradient(circle,rgba(212,175,55,.06) 0%,transparent 70%)}
.ceo-wrap{max-width:1100px;margin:0 auto;display:grid;grid-template-columns:380px 1fr;gap:80px;align-items:center;position:relative;z-index:1}
/* Photo frame */
.ceo-frame{position:relative}
.ceo-photo{width:100%;aspect-ratio:3/4;background:linear-gradient(145deg,#1e2d40,#0d1b2e);border:1px solid rgba(212,175,55,.2);display:flex;align-items:center;justify-content:center;flex-direction:column;gap:0;overflow:hidden;position:relative}
/* Decorative SVG portrait placeholder */
.ceo-photo svg.portrait{width:100%;height:100%;position:absolute;inset:0}
.ceo-photo-label{position:absolute;bottom:0;left:0;right:0;background:rgba(0,0,0,.7);padding:16px 20px;border-top:2px solid var(--gold)}
.ceo-photo-name{font-family:var(--T);font-size:.9rem;letter-spacing:2px;color:#fff;text-transform:uppercase}
.ceo-photo-role{font-size:.65rem;letter-spacing:2px;color:var(--gold);text-transform:uppercase;margin-top:3px}
.corner{position:absolute;width:50px;height:50px}
.tl{top:-12px;left:-12px;border-top:2px solid var(--gold);border-left:2px solid var(--gold)}
.br{bottom:-12px;right:-12px;border-bottom:2px solid var(--gold);border-right:2px solid var(--gold)}
/* Text */
.ceo-quote{background:rgba(212,175,55,.05);border-left:3px solid var(--gold);padding:26px 28px;margin:24px 0;position:relative}
.qmark{font-family:var(--F);font-size:5rem;color:var(--gold);opacity:.12;position:absolute;top:-10px;left:12px;line-height:1}
.ceo-quote p{font-size:.95rem;line-height:1.85;color:var(--muted2);font-style:italic;position:relative;z-index:1}
.ceo-sig{font-family:var(--T);font-size:1rem;letter-spacing:2px;color:var(--gold);margin-top:20px}
.ceo-role-txt{font-size:.7rem;letter-spacing:2px;color:var(--muted);text-transform:uppercase;margin-top:4px}
.ceo-badges{display:flex;gap:12px;flex-wrap:wrap;margin-top:24px}
.badge{background:rgba(212,175,55,.08);border:1px solid rgba(212,175,55,.25);padding:7px 16px;font-family:var(--T);font-size:.65rem;letter-spacing:2px;color:var(--gold);text-transform:uppercase}

/* ══════════════════════════
   PROJECTS
══════════════════════════ */
#projets{background:var(--dark);padding:100px 40px}
.proj-wrap{max-width:1100px;margin:0 auto}
.proj-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:3px;margin-top:56px}
.pc{background:var(--dark2);overflow:hidden;position:relative;transition:transform .3s}
.pc:hover{transform:translateY(-4px)}
/* Illustrated thumbnails */
.pc-thumb{height:180px;position:relative;overflow:hidden;display:flex;align-items:center;justify-content:center}
.pc-thumb svg{width:100%;height:100%;position:absolute;inset:0}
.pc-cat{position:absolute;top:14px;left:14px;background:var(--gold);color:#000;font-family:var(--T);font-size:.58rem;letter-spacing:2px;text-transform:uppercase;padding:4px 10px;z-index:2}
.pc-body{padding:22px 22px 26px}
.pc-title{font-family:var(--T);font-size:.9rem;letter-spacing:1.2px;text-transform:uppercase;color:#fff;margin-bottom:10px;font-weight:600;line-height:1.3}
.pc-text{font-size:.78rem;color:var(--muted);line-height:1.65}
.pc-link{display:inline-flex;align-items:center;gap:8px;margin-top:14px;font-family:var(--T);font-size:.62rem;letter-spacing:2px;text-transform:uppercase;color:var(--gold);transition:gap .2s}
.pc:hover .pc-link{gap:12px}

/* ══════════════════════════
   INVEST
══════════════════════════ */
#investir{background:var(--dark2);padding:100px 40px;position:relative;overflow:hidden}
#investir::after{content:'';position:absolute;bottom:-200px;right:-200px;width:600px;height:600px;border-radius:50%;background:radial-gradient(circle,rgba(212,175,55,.05) 0%,transparent 70%)}
.inv-wrap{max-width:1100px;margin:0 auto;display:grid;grid-template-columns:1fr 1fr;gap:80px;align-items:center;position:relative;z-index:1}
.inv-left p{font-size:.93rem;color:var(--muted2);line-height:1.85;margin-bottom:32px;max-width:460px}
.inv-pillars{display:flex;flex-direction:column;gap:0;margin-top:28px}
.pil{display:flex;align-items:center;gap:20px;padding:18px 0;border-bottom:1px solid rgba(212,175,55,.1)}
.pil:first-child{border-top:1px solid rgba(212,175,55,.1)}
.pil-ic{width:44px;height:44px;border:1.5px solid var(--gold);display:flex;align-items:center;justify-content:center;flex-shrink:0;color:var(--gold)}
.pil-ic svg{width:20px;height:20px;stroke:currentColor;fill:none;stroke-width:1.5;stroke-linecap:round;stroke-linejoin:round}
.pil-name{font-family:var(--T);font-size:.82rem;letter-spacing:1.5px;text-transform:uppercase;color:#fff}
.pil-sub{font-size:.72rem;color:var(--muted);margin-top:2px}
/* Visual right side */
.inv-visual{position:relative}
.inv-card{background:var(--dark3);border:1px solid rgba(212,175,55,.15);padding:36px;position:relative;overflow:hidden}
.inv-card::before{content:'';position:absolute;top:0;left:0;right:0;height:3px;background:linear-gradient(90deg,var(--gold),transparent)}
.inv-card-title{font-family:var(--F);font-size:2.2rem;color:var(--gold);letter-spacing:2px;text-transform:uppercase;margin-bottom:20px;line-height:1}
.inv-stat-row{display:grid;grid-template-columns:1fr 1fr;gap:16px;margin-bottom:24px}
.inv-stat{background:rgba(212,175,55,.06);border:1px solid rgba(212,175,55,.12);padding:20px;text-align:center}
.inv-stat-n{font-family:var(--F);font-size:2.4rem;color:var(--gold);line-height:1}
.inv-stat-l{font-size:.65rem;letter-spacing:2px;text-transform:uppercase;color:var(--muted);margin-top:4px}
.inv-card p{font-size:.82rem;color:var(--muted2);line-height:1.7;margin-bottom:20px}

/* ══════════════════════════
   INSTAGRAM
══════════════════════════ */
#insta{background:#111;padding:80px 40px}
.insta-wrap{max-width:960px;margin:0 auto;text-align:center}
.insta-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:4px;max-width:800px;margin:40px auto 28px}
.ig{position:relative;aspect-ratio:1;overflow:hidden;cursor:pointer}
.ig-bg{width:100%;height:100%;display:flex;align-items:center;justify-content:center;transition:transform .4s}
.ig:hover .ig-bg{transform:scale(1.06)}
.ig-ov{position:absolute;inset:0;background:rgba(212,175,55,.8);display:flex;align-items:center;justify-content:center;opacity:0;transition:opacity .3s}
.ig:hover .ig-ov{opacity:1}
.ig-ov svg{width:40px;height:40px;stroke:#000;fill:none;stroke-width:1.5}

/* ══════════════════════════
   CONTACT
══════════════════════════ */
#contact{background:var(--dark4);padding:100px 40px}
.contact-wrap{max-width:1100px;margin:0 auto}
.contact-grid{display:grid;grid-template-columns:1fr 1.5fr;gap:80px;margin-top:60px}
.cinfo{display:flex;flex-direction:column;gap:0}
.ci-block{padding:22px 0;border-bottom:1px solid rgba(212,175,55,.1);display:flex;gap:18px;align-items:flex-start}
.ci-block:first-child{border-top:1px solid rgba(212,175,55,.1)}
.ci-icon{width:44px;height:44px;border:1px solid rgba(212,175,55,.3);display:flex;align-items:center;justify-content:center;flex-shrink:0;color:var(--gold)}
.ci-icon svg{width:20px;height:20px;stroke:currentColor;fill:none;stroke-width:1.5;stroke-linecap:round;stroke-linejoin:round}
.ci-label{font-family:var(--T);font-size:.62rem;letter-spacing:2px;text-transform:uppercase;color:var(--gold);margin-bottom:4px}
.ci-val{font-size:.88rem;color:var(--muted2);line-height:1.6}
.ci-val a{color:var(--gold)}
/* map */
.map-box{margin-top:24px;height:170px;background:linear-gradient(135deg,#1e2d40,#0d1520);border:1px solid rgba(212,175,55,.15);display:flex;align-items:center;justify-content:center;flex-direction:column;gap:10px;color:var(--muted);font-family:var(--T);font-size:.6rem;letter-spacing:3px;text-transform:uppercase;position:relative;overflow:hidden}
.map-box svg.map-svg{width:100%;height:100%;position:absolute;inset:0;opacity:.3}
.map-box span{position:relative;z-index:1;color:var(--gold)}
.map-box .map-pin{position:relative;z-index:1}
.map-pin svg{width:28px;height:28px;stroke:var(--gold);fill:none;stroke-width:1.5}
/* form */
.cform{display:flex;flex-direction:column;gap:16px}
.frow{display:grid;grid-template-columns:1fr 1fr;gap:14px}
.fl{display:flex;flex-direction:column;gap:5px}
.fl label{font-family:var(--T);font-size:.6rem;letter-spacing:2.5px;text-transform:uppercase;color:var(--gold)}
.fl input,.fl select,.fl textarea{background:rgba(255,255,255,.04);border:1px solid rgba(212,175,55,.2);color:#fff;font-family:var(--B);font-size:.88rem;padding:13px 15px;outline:none;transition:border-color .2s;width:100%}
.fl input:focus,.fl select:focus,.fl textarea:focus{border-color:var(--gold)}
.fl input::placeholder,.fl textarea::placeholder{color:rgba(255,255,255,.22)}
.fl select option{background:#2c3e50}
.fl textarea{min-height:110px;resize:vertical}
.form-note{font-size:.7rem;color:var(--muted);margin-top:4px}

/* ══════════════════════════
   FOOTER
══════════════════════════ */
footer{background:#000;border-top:2px solid var(--gold);padding:72px 40px 28px}
.ft{max-width:1100px;margin:0 auto}
.ft-grid{display:grid;grid-template-columns:2.2fr 1fr 1fr 1fr;gap:48px;padding-bottom:48px;border-bottom:1px solid rgba(