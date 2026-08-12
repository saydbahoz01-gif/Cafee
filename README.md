<html lang="ku" dir="rtl" data-theme="light">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1,maximum-scale=1,user-scalable=no">
<title>CAFE_64</title>
<link rel="icon" type="image/svg+xml" href="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'%3E%3Crect rx='20' width='100' height='100' fill='%23d4a574'/%3E%3Ctext x='50' y='70' text-anchor='middle' font-size='48' font-weight='800' fill='%23331a00'%3E64%3C/text%3E%3C/svg%3E">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Noto+Sans+Arabic:wght@300;400;500;600;700;800;900&family=Noto+Kufi+Arabic:wght@500;600;700;800;900&display=swap" rel="stylesheet">
<style>
:root{
--bg:#FAF6F1;--fg:#2C1810;--muted:#8B7355;--accent:#C8956C;--accent2:#A0714F;
--card:rgba(255,255,255,0.55);--card-border:rgba(200,149,108,0.18);--glass:rgba(255,255,255,0.22);
--glass-border:rgba(255,255,255,0.35);--glass-shadow:rgba(200,149,108,0.12);
--nav-bg:rgba(250,246,241,0.72);--overlay:rgba(44,24,16,0.35);
--blob1:rgba(200,149,108,0.12);--blob2:rgba(160,113,79,0.10);--blob3:rgba(232,200,160,0.15);
--success:#4CAF50;--danger:#E53935;--warn:#FF9800;
--header-h:58px;--nav-h:76px;
}
[data-theme="dark"]{
--bg:#151010;--fg:#F0E6DA;--muted:#A89880;--accent:#D4A574;--accent2:#B8845A;
--card:rgba(40,28,22,0.7);--card-border:rgba(212,165,116,0.15);--glass:rgba(255,255,255,0.08);
--glass-border:rgba(255,255,255,0.12);--glass-shadow:rgba(0,0,0,0.3);
--nav-bg:rgba(21,16,16,0.78);--overlay:rgba(0,0,0,0.55);
--blob1:rgba(212,165,116,0.06);--blob2:rgba(184,132,90,0.05);--blob3:rgba(200,160,120,0.07);
}
*{margin:0;padding:0;box-sizing:border-box;-webkit-tap-highlight-color:transparent}
html,body{height:100%;overflow:hidden;font-family:'Noto Sans Arabic',sans-serif;background:var(--bg);color:var(--fg);transition:background .5s,color .5s}
body{display:flex;flex-direction:column}

/* === ANIMATED BACKGROUND === */
.bg-layer{position:fixed;inset:0;z-index:0;overflow:hidden;pointer-events:none}
.blob{position:absolute;border-radius:50%;filter:blur(80px);will-change:transform}
.blob-1{width:300px;height:300px;background:var(--blob1);top:-80px;right:-60px;animation:bfloat1 12s ease-in-out infinite}
.blob-2{width:250px;height:250px;background:var(--blob2);bottom:10%;left:-70px;animation:bfloat2 15s ease-in-out infinite}
.blob-3{width:200px;height:200px;background:var(--blob3);top:40%;right:20%;animation:bfloat3 18s ease-in-out infinite}
@keyframes bfloat1{0%,100%{transform:translate(0,0) scale(1)}33%{transform:translate(-40px,60px) scale(1.15)}66%{transform:translate(30px,-30px) scale(0.9)}}
@keyframes bfloat2{0%,100%{transform:translate(0,0) scale(1)}40%{transform:translate(50px,-40px) scale(1.1)}70%{transform:translate(-20px,50px) scale(0.95)}}
@keyframes bfloat3{0%,100%{transform:translate(0,0) scale(1)}50%{transform:translate(-60px,30px) scale(1.2)}}

/* === HEADER === */
header{position:fixed;top:0;left:0;right:0;z-index:100;height:var(--header-h);display:flex;align-items:center;justify-content:space-between;padding:10px 16px;background:var(--nav-bg);backdrop-filter:blur(24px);-webkit-backdrop-filter:blur(24px);border-bottom:1px solid var(--glass-border);transition:all .5s}
.header-logo{display:flex;align-items:center;gap:8px}
.header-logo img{width:36px;height:36px;border-radius:10px;object-fit:cover}
.header-logo span{font-size:18px;font-weight:800;color:var(--accent);letter-spacing:-0.5px;font-family:'Noto Kufi Arabic',sans-serif}
.header-actions{display:flex;align-items:center;gap:6px}
.hdr-btn{width:36px;height:36px;border-radius:12px;border:1px solid var(--glass-border);background:var(--glass);backdrop-filter:blur(10px);display:flex;align-items:center;justify-content:center;cursor:pointer;transition:all .3s;color:var(--fg);font-size:16px}
.hdr-btn:active{transform:scale(0.9)}
.lang-dropdown{position:relative}
.lang-menu{position:absolute;top:42px;left:0;background:var(--card);backdrop-filter:blur(20px);border:1px solid var(--card-border);border-radius:14px;padding:6px;min-width:120px;opacity:0;transform:translateY(-8px);pointer-events:none;transition:all .3s;z-index:200}
.lang-menu.open{opacity:1;transform:translateY(0);pointer-events:all}
.lang-item{padding:8px 14px;border-radius:10px;cursor:pointer;font-size:13px;font-weight:500;transition:all .2s;display:flex;align-items:center;gap:8px}
.lang-item:hover,.lang-item.active{background:var(--glass);color:var(--accent)}
.lang-item .flag{font-size:16px}

/* === MAIN CONTENT === */
main{flex:1;overflow:hidden;position:relative;z-index:1;
  padding-top:var(--header-h);
  padding-bottom:var(--nav-h);
}
.page{position:absolute;top:0;left:0;right:0;bottom:0;
  padding:16px;
  overflow-y:auto;-webkit-overflow-scrolling:touch;
  opacity:0;transform:translateY(20px);pointer-events:none;
  transition:opacity .4s,transform .4s;
}
.page.active{opacity:1;transform:translateY(0);pointer-events:all}
.page::-webkit-scrollbar{width:0}

/* === WELCOME PAGE === */
.welcome-wrap{display:flex;flex-direction:column;align-items:center;justify-content:center;min-height:100%;text-align:center;padding:20px}
.welcome-img{width:120px;height:120px;border-radius:28px;object-fit:cover;border:3px solid var(--glass-border);box-shadow:0 8px 32px var(--glass-shadow);margin-bottom:20px;animation:welcomePulse 3s ease-in-out infinite}
@keyframes welcomePulse{0%,100%{transform:scale(1);box-shadow:0 8px 32px var(--glass-shadow)}50%{transform:scale(1.05);box-shadow:0 12px 40px var(--glass-shadow)}}
.welcome-title{font-size:30px;font-weight:900;color:var(--accent);margin-bottom:6px;animation:fadeUp .8s ease;font-family:'Noto Kufi Arabic',sans-serif}
.welcome-sub{font-size:14px;color:var(--muted);margin-bottom:30px;animation:fadeUp .8s ease .15s both}
.welcome-start{padding:14px 48px;border-radius:16px;border:none;background:linear-gradient(135deg,var(--accent),var(--accent2));color:#fff;font-size:16px;font-weight:700;font-family:inherit;cursor:pointer;box-shadow:0 6px 24px rgba(200,149,108,0.35);transition:all .3s;animation:fadeUp .8s ease .3s both}
.welcome-start:active{transform:scale(0.95)}
@keyframes fadeUp{from{opacity:0;transform:translateY(16px)}to{opacity:1;transform:translateY(0)}}

/* === MENU PAGE === */
.menu-cats{display:flex;gap:8px;padding:4px 0 14px;overflow-x:auto;-webkit-overflow-scrolling:touch;position:sticky;top:0;z-index:10;background:linear-gradient(to bottom,var(--bg) 70%,transparent);padding-top:8px;margin:-16px -16px 0;padding-left:16px;padding-right:16px}
.menu-cats::-webkit-scrollbar{display:none}
.cat-btn{flex-shrink:0;padding:9px 22px;border-radius:14px;border:1.5px solid var(--card-border);background:var(--card);backdrop-filter:blur(10px);font-family:inherit;font-size:13px;font-weight:600;color:var(--muted);cursor:pointer;transition:all .3s;white-space:nowrap}
.cat-btn.active{background:linear-gradient(135deg,var(--accent),var(--accent2));color:#fff;border-color:transparent;box-shadow:0 4px 16px rgba(200,149,108,0.3)}
.menu-grid{display:grid;grid-template-columns:1fr 1fr;gap:12px;padding-bottom:16px}
.menu-card{border-radius:18px;border:1px solid var(--card-border);background:var(--card);backdrop-filter:blur(12px);overflow:hidden;cursor:pointer;transition:all .3s;animation:cardIn .4s ease both;position:relative}
.menu-card:active{transform:scale(0.96)}
@keyframes cardIn{from{opacity:0;transform:scale(0.92)}to{opacity:1;transform:scale(1)}}
.menu-card-img{width:100%;aspect-ratio:1;object-fit:cover;display:block}
.menu-card-body{padding:10px}
.menu-card-name{font-size:13px;font-weight:700;margin-bottom:4px;line-height:1.4}
.menu-card-price{font-size:14px;font-weight:800;color:var(--accent)}

/* === TABLE SELECTION PAGE === */
.section-title{font-size:20px;font-weight:800;margin-bottom:4px;font-family:'Noto Kufi Arabic',sans-serif}
.section-desc{font-size:13px;color:var(--muted);margin-bottom:18px}
.table-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:12px;padding-bottom:16px}
.table-card{aspect-ratio:1;border-radius:20px;border:2px solid var(--card-border);background:var(--card);backdrop-filter:blur(12px);display:flex;flex-direction:column;align-items:center;justify-content:center;gap:6px;cursor:pointer;transition:all .3s;position:relative;overflow:hidden}
.table-card::before{content:'';position:absolute;inset:0;border-radius:18px;background:linear-gradient(135deg,transparent,var(--glass));opacity:0;transition:opacity .3s}
.table-card:hover::before,.table-card:active::before{opacity:1}
.table-card.selected{border-color:var(--accent);background:linear-gradient(135deg,rgba(200,149,108,0.15),rgba(200,149,108,0.05));box-shadow:0 4px 20px rgba(200,149,108,0.2)}
.table-card:active{transform:scale(0.95)}
.table-num{font-size:28px;font-weight:900;color:var(--accent)}
.table-label{font-size:11px;color:var(--muted);font-weight:500}
.table-check{position:absolute;top:8px;right:8px;width:22px;height:22px;border-radius:50%;background:var(--accent);display:none;align-items:center;justify-content:center;color:#fff;font-size:12px}
.table-card.selected .table-check{display:flex}

/* === ORDER PAGE === */
.order-table-info{padding:12px 16px;border-radius:14px;background:var(--card);border:1px solid var(--card-border);backdrop-filter:blur(10px);margin-bottom:14px;display:flex;align-items:center;gap:10px}
.order-table-info svg{color:var(--accent);flex-shrink:0}
.order-table-info span{font-size:14px;font-weight:600}
.order-empty{text-align:center;padding:60px 20px;color:var(--muted)}
.order-empty svg{margin-bottom:12px;opacity:.4}
.order-empty p{font-size:14px}
.order-list{display:flex;flex-direction:column;gap:10px;padding-bottom:14px}
.order-item{display:flex;align-items:center;gap:10px;padding:12px;border-radius:16px;background:var(--card);border:1px solid var(--card-border);backdrop-filter:blur(10px);animation:slideIn .3s ease}
@keyframes slideIn{from{opacity:0;transform:translateX(20px)}to{opacity:1;transform:translateX(0)}}
.order-item-img{width:52px;height:52px;border-radius:12px;object-fit:cover;flex-shrink:0}
.order-item-info{flex:1;min-width:0}
.order-item-name{font-size:13px;font-weight:700;white-space:nowrap;overflow:hidden;text-overflow:ellipsis}
.order-item-price{font-size:12px;color:var(--accent);font-weight:600}
.qty-controls{display:flex;align-items:center;gap:6px}
.qty-btn{width:28px;height:28px;border-radius:8px;border:1px solid var(--card-border);background:var(--glass);color:var(--fg);font-size:16px;font-weight:700;display:flex;align-items:center;justify-content:center;cursor:pointer;transition:all .2s;font-family:inherit}
.qty-btn:active{transform:scale(0.9)}
.qty-btn.remove{color:var(--danger)}
.qty-val{font-size:14px;font-weight:700;min-width:20px;text-align:center}
.order-footer{position:sticky;bottom:0;padding:14px 0 4px;background:linear-gradient(to top,var(--bg) 60%,transparent)}
.order-total{display:flex;justify-content:space-between;align-items:center;margin-bottom:12px;padding:0 4px}
.order-total-label{font-size:14px;font-weight:600;color:var(--muted)}
.order-total-val{font-size:22px;font-weight:900;color:var(--accent)}
.send-btn{width:100%;padding:15px;border-radius:16px;border:none;background:linear-gradient(135deg,var(--accent),var(--accent2));color:#fff;font-size:16px;font-weight:800;font-family:inherit;cursor:pointer;box-shadow:0 6px 24px rgba(200,149,108,0.35);transition:all .3s;display:flex;align-items:center;justify-content:center;gap:8px}
.send-btn:active{transform:scale(0.97)}
.send-btn:disabled{opacity:.4;pointer-events:none}

/* === GALLERY PAGE === */
.gallery-grid{display:grid;grid-template-columns:1fr 1fr;gap:10px;padding-bottom:16px}
.gallery-item{border-radius:16px;overflow:hidden;position:relative;cursor:pointer;transition:all .3s;aspect-ratio:1}
.gallery-item:active{transform:scale(0.97)}
.gallery-item img{width:100%;height:100%;object-fit:cover;display:block;transition:transform .4s}
.gallery-item:active img{transform:scale(1.05)}
.gallery-overlay{position:absolute;inset:0;background:linear-gradient(to top,rgba(0,0,0,0.5),transparent);display:flex;align-items:flex-end;padding:10px;opacity:0;transition:opacity .3s}
.gallery-item:active .gallery-overlay{opacity:1}
.gallery-overlay span{color:#fff;font-size:12px;font-weight:600}

/* === LIGHTBOX === */
.lightbox{position:fixed;inset:0;z-index:500;background:rgba(0,0,0,0.92);display:none;align-items:center;justify-content:center;flex-direction:column;gap:12px;padding:20px}
.lightbox.open{display:flex}
.lightbox img{max-width:100%;max-height:70vh;border-radius:12px;object-fit:contain}
.lightbox-close{position:absolute;top:16px;right:16px;width:40px;height:40px;border-radius:50%;border:none;background:rgba(255,255,255,0.15);color:#fff;font-size:22px;cursor:pointer;display:flex;align-items:center;justify-content:center}
.lightbox-dl{padding:12px 32px;border-radius:14px;border:none;background:var(--accent);color:#fff;font-size:15px;font-weight:700;font-family:inherit;cursor:pointer;display:flex;align-items:center;gap:8px;transition:all .3s}
.lightbox-dl:active{transform:scale(0.95)}

/* === BOTTOM NAV === */
.bottom-nav{position:fixed;bottom:0;left:0;right:0;z-index:100;height:var(--nav-h);display:flex;align-items:flex-end;justify-content:space-around;padding:0 8px 10px;background:var(--nav-bg);backdrop-filter:blur(28px);-webkit-backdrop-filter:blur(28px);border-top:1px solid var(--glass-border);transition:all .5s}
.nav-pill{display:flex;flex-direction:column;align-items:center;gap:3px;padding:8px 0 6px;cursor:pointer;transition:all .3s;position:relative;border-radius:16px;min-width:64px}
.nav-pill svg{width:24px;height:24px;color:var(--muted);transition:all .35s}
.nav-pill span{font-size:10px;font-weight:600;color:var(--muted);transition:all .35s}
.nav-pill.active svg{color:var(--accent);filter:drop-shadow(0 2px 8px rgba(200,149,108,0.4))}
.nav-pill.active span{color:var(--accent)}
.nav-pill.active::before{content:'';position:absolute;top:-1px;left:20%;right:20%;height:3px;border-radius:0 0 4px 4px;background:var(--accent);box-shadow:0 2px 10px rgba(200,149,108,0.5)}
.nav-pill:active{transform:scale(0.92)}

/* === TOAST === */
.toast{position:fixed;top:70px;left:50%;transform:translateX(-50%) translateY(-20px);z-index:600;padding:12px 24px;border-radius:14px;background:var(--card);backdrop-filter:blur(20px);border:1px solid var(--card-border);font-size:13px;font-weight:600;opacity:0;pointer-events:none;transition:all .4s;white-space:nowrap;box-shadow:0 8px 32px var(--glass-shadow)}
.toast.show{opacity:1;transform:translateX(-50%) translateY(0);pointer-events:all}
.toast.success{border-color:var(--success);color:var(--success)}
.toast.error{border-color:var(--danger);color:var(--danger)}

/* === MENU SELECTED BADGE === */
.menu-selected-badge{position:absolute;top:8px;left:8px;width:24px;height:24px;border-radius:50%;background:var(--accent);color:#fff;display:none;align-items:center;justify-content:center;font-size:11px;font-weight:800;z-index:2}
.menu-card.in-order .menu-selected-badge{display:flex}

/* === WELCOME PAGE NAV ADJUSTMENT === */
#page-welcome .welcome-wrap{padding-bottom:20px}

@media(min-width:500px){
.menu-grid,.gallery-grid{grid-template-columns:repeat(4,1fr);max-width:500px;margin:0 auto}
.table-grid{grid-template-columns:repeat(5,1fr);max-width:500px;margin:0 auto}
}
@media(prefers-reduced-motion:reduce){
*{animation-duration:0.01ms!important;transition-duration:0.01ms!important}
}
</style>
</head>
<body>

<!-- Animated Background -->
<div class="bg-layer" aria-hidden="true">
  <div class="blob blob-1"></div>
  <div class="blob blob-2"></div>
  <div class="blob blob-3"></div>
</div>

<!-- Header -->
<header>
  <div class="header-logo">
    <img src="https://picsum.photos/seed/cafe64logo/100/100.jpg" alt="CAFE_64">
    <span>CAFE_64</span>
  </div>
  <div class="header-actions">
    <button class="hdr-btn" id="themeToggle" aria-label="تۆمەربوون">
      <svg id="sunIcon" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round"><circle cx="12" cy="12" r="5"/><line x1="12" y1="1" x2="12" y2="3"/><line x1="12" y1="21" x2="12" y2="23"/><line x1="4.22" y1="4.22" x2="5.64" y2="5.64"/><line x1="18.36" y1="18.36" x2="19.78" y2="19.78"/><line x1="1" y1="12" x2="3" y2="12"/><line x1="21" y1="12" x2="23" y2="12"/><line x1="4.22" y1="19.78" x2="5.64" y2="18.36"/><line x1="18.36" y1="5.64" x2="19.78" y2="4.22"/></svg>
      <svg id="moonIcon" width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" style="display:none"><path d="M21 12.79A9 9 0 1 1 11.21 3 7 7 0 0 0 21 12.79z"/></svg>
    </button>
    <div class="lang-dropdown">
      <button class="hdr-btn" id="langToggle" aria-label="زمان">
        <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round"><circle cx="12" cy="12" r="10"/><line x1="2" y1="12" x2="22" y2="12"/><path d="M12 2a15.3 15.3 0 0 1 4 10 15.3 15.3 0 0 1-4 10 15.3 15.3 0 0 1-4-10 15.3 15.3 0 0 1 4-10z"/></svg>
      </button>
      <div class="lang-menu" id="langMenu">
        <div class="lang-item active" data-lang="ku"><span class="flag">🟡</span>کوردی</div>
        <div class="lang-item" data-lang="ar"><span class="flag">🟢</span>العربية</div>
        <div class="lang-item" data-lang="en"><span class="flag">🔵</span>English</div>
      </div>
    </div>
  </div>
</header>

<!-- Main Content -->
<main>

  <!-- Welcome Page -->
  <section class="page active" id="page-welcome">
    <div class="welcome-wrap">
      <img class="welcome-img" src="https://picsum.photos/seed/cafe64logo/300/300.jpg" alt="CAFE_64">
      <h1 class="welcome-title" data-i18n="welcomeTitle">بەخێربێیت بۆ CAFE_64</h1>
      <p class="welcome-sub" data-i18n="welcomeSub">چێژ لە باشترین قاوە و شیرینیەکان وەربگرە</p>
      <button class="welcome-start" id="startBtn" data-i18n="start">دەستپێبکە</button>
    </div>
  </section>

  <!-- Menu Page -->
  <section class="page" id="page-menu">
    <div class="menu-cats" id="menuCats"></div>
    <div class="menu-grid" id="menuGrid"></div>
  </section>

  <!-- Tables Page -->
  <section class="page" id="page-tables">
    <h2 class="section-title" data-i18n="selectTable">مێزێک هەڵبژێرە</h2>
    <p class="section-desc" data-i18n="selectTableDesc">تکایە مێزی خۆت هەڵبژێرە</p>
    <div class="table-grid" id="tableGrid"></div>
  </section>

  <!-- Order Page -->
  <section class="page" id="page-order">
    <div id="orderTableInfo" class="order-table-info" style="display:none">
      <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><rect x="3" y="3" width="18" height="18" rx="2"/><path d="M3 9h18"/><path d="M9 3v18"/></svg>
      <span id="orderTableName"></span>
    </div>
    <div id="orderContent"></div>
  </section>

  <!-- Gallery Page -->
  <section class="page" id="page-gallery">
    <h2 class="section-title" data-i18n="galleryTitle">گەلەری</h2>
    <p class="section-desc" data-i18n="galleryDesc">وێنەکانی کافێکەمان ببینە</p>
    <div class="gallery-grid" id="galleryGrid"></div>
  </section>

</main>

<!-- Lightbox -->
<div class="lightbox" id="lightbox">
  <button class="lightbox-close" id="lightboxClose">&times;</button>
  <img id="lightboxImg" src="" alt="">
  <button class="lightbox-dl" id="lightboxDl">
    <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round"><path d="M21 15v4a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2v-4"/><polyline points="7 10 12 15 17 10"/><line x1="12" y1="15" x2="12" y2="3"/></svg>
    <span data-i18n="download">داگرتن</span>
  </button>
</div>

<!-- Toast -->
<div class="toast" id="toast"></div>

<!-- Bottom Navigation - هەمیشە دیارە -->
<nav class="bottom-nav" id="bottomNav">
  <div class="nav-pill" data-page="page-welcome">
    <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round"><path d="M3 9l9-7 9 7v11a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2z"/><polyline points="9 22 9 12 15 12 15 22"/></svg>
    <span data-i18n="navHome">سەرەتا</span>
  </div>
  <div class="nav-pill" data-page="page-menu">
    <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round"><path d="M18 8h1a4 4 0 0 1 0 8h-1"/><path d="M2 8h16v9a4 4 0 0 1-4 4H6a4 4 0 0 1-4-4V8z"/><line x1="6" y1="1" x2="6" y2="4"/><line x1="10" y1="1" x2="10" y2="4"/><line x1="14" y1="1" x2="14" y2="4"/></svg>
    <span data-i18n="navMenu">مێنیو</span>
  </div>
  <div class="nav-pill" data-page="page-tables">
    <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round"><rect x="3" y="3" width="18" height="18" rx="2"/><path d="M3 9h18"/><path d="M9 3v18"/></svg>
    <span data-i18n="navTables">مێزەکان</span>
  </div>
  <div class="nav-pill" data-page="page-order">
    <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round"><path d="M6 2L3 6v14a2 2 0 0 0 2 2h14a2 2 0 0 0 2-2V6l-3-4z"/><line x1="3" y1="6" x2="21" y2="6"/><path d="M16 10a4 4 0 0 1-8 0"/></svg>
    <span data-i18n="navOrder">ئۆردەر</span>
  </div>
  <div class="nav-pill" data-page="page-gallery">
    <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round"><rect x="3" y="3" width="18" height="18" rx="2"/><circle cx="8.5" cy="8.5" r="1.5"/><polyline points="21 15 16 10 5 21"/></svg>
    <span data-i18n="navGallery">گەلەری</span>
  </div>
</nav>

<script>
/* ========================================
   داتای مێنیو
   ======================================== */
const menuData = {
  cake: [
    {id:'c1',name:{ku:'کێکی شکلاتی',ar:'كيك شوكولاتة',en:'Chocolate Cake'},price:4500,img:'https://picsum.photos/seed/chocake64/400/400.jpg'},
    {id:'c2',name:{ku:'کێکی توتفرەنگی',ar:'كيك فراولة',en:'Strawberry Cake'},price:5000,img:'https://picsum.photos/seed/strawcake64/400/400.jpg'},
    {id:'c3',name:{ku:'کێکی نوتێلا',ar:'كيك نوتيلا',en:'Nutella Cake'},price:5500,img:'https://picsum.photos/seed/nutellacake64/400/400.jpg'},
    {id:'c4',name:{ku:'کێکی وەنەستە',ar:'كيك فانيلا',en:'Vanilla Cake'},price:4000,img:'https://picsum.photos/seed/vancake64/400/400.jpg'},
    {id:'c5',name:{ku:'کێکی موز',ar:'كيك موز',en:'Banana Cake'},price:4200,img:'https://picsum.photos/seed/banacake64/400/400.jpg'},
    {id:'c6',name:{ku:'کێکی پرتەقاڵی',ar:'كيك برتقال',en:'Orange Cake'},price:4300,img:'https://picsum.photos/seed/orangecake64/400/400.jpg'},
    {id:'c7',name:{ku:'کێکی قاوە',ar:'كيك قهوة',en:'Coffee Cake'},price:4800,img:'https://picsum.photos/seed/coffeecake64/400/400.jpg'},
    {id:'c8',name:{ku:'کێکی کارۆت',ar:'كيك جزر',en:'Carrot Cake'},price:4600,img:'https://picsum.photos/seed/carrotcake64/400/400.jpg'},
    {id:'c9',name:{ku:'کێکی لیمۆ',ar:'كيك ليمون',en:'Lemon Cake'},price:4100,img:'https://picsum.photos/seed/lemoncake64/400/400.jpg'},
    {id:'c10',name:{ku:'کێکی کەرەسوونە',ar:'كيك رد فيلفيت',en:'Red Velvet Cake'},price:6000,img:'https://picsum.photos/seed/redvelvet64/400/400.jpg'}
  ],
  sweet: [
    {id:'s1',name:{ku:'کلاکچە',ar:'كلاكاج',en:'Clafoutis'},price:3000,img:'https://picsum.photos/seed/kalacha64/400/400.jpg'},
    {id:'s2',name:{ku:'باقلوا',ar:'باقلوا',en:'Baklava'},price:3500,img:'https://picsum.photos/seed/baklawa64/400/400.jpg'},
    {id:'s3',name:{ku:'کنافە',ar:'كنافة',en:'Kunafa'},price:4000,img:'https://picsum.photos/seed/kunafa64/400/400.jpg'},
    {id:'s4',name:{ku:'ڕەشبەق',ar:'رش باغ',en:'Rash Bakh'},price:2500,img:'https://picsum.photos/seed/rashbagh64/400/400.jpg'},
    {id:'s5',name:{ku:'پانکیک',ar:'بان كيك',en:'Pancake'},price:3200,img:'https://picsum.photos/seed/pancake64/400/400.jpg'},
    {id:'s6',name:{ku:'دۆنەت',ar:'دونات',en:'Donut'},price:2000,img:'https://picsum.photos/seed/donut64/400/400.jpg'},
    {id:'s7',name:{ku:'ماکارۆن',ar:'ماكارون',en:'Macaron'},price:2800,img:'https://picsum.photos/seed/macaron64/400/400.jpg'},
    {id:'s8',name:{ku:'تیرامیسو',ar:'تيراميسو',en:'Tiramisu'},price:4500,img:'https://picsum.photos/seed/tiramisu64/400/400.jpg'},
    {id:'s9',name:{ku:'کرۆسان',ar:'كرواسون',en:'Croissant'},price:2200,img:'https://picsum.photos/seed/croissant64/400/400.jpg'},
    {id:'s10',name:{ku:'چیزکەیک',ar:'تشيز كيك',en:'Cheesecake'},price:4800,img:'https://picsum.photos/seed/cheesecake64/400/400.jpg'}
  ],
  coffee: [
    {id:'cf1',name:{ku:'ئێسپرێسۆ',ar:'اسبريسو',en:'Espresso'},price:2000,img:'https://picsum.photos/seed/espresso64/400/400.jpg'},
    {id:'cf2',name:{ku:'کاپوچینۆ',ar:'كابتشينو',en:'Cappuccino'},price:3000,img:'https://picsum.photos/seed/cappuccino64/400/400.jpg'},
    {id:'cf3',name:{ku:'لاتە',ar:'لاتيه',en:'Latte'},price:3500,img:'https://picsum.photos/seed/latte64/400/400.jpg'},
    {id:'cf4',name:{ku:'موکا',ar:'موكا',en:'Mocha'},price:3800,img:'https://picsum.photos/seed/mocha64/400/400.jpg'},
    {id:'cf5',name:{ku:'ئەمریکانۆ',ar:'امريكانو',en:'Americano'},price:2500,img:'https://picsum.photos/seed/americano64/400/400.jpg'},
    {id:'cf6',name:{ku:'ماکیاتۆ',ar:'ماكياتو',en:'Macchiato'},price:3200,img:'https://picsum.photos/seed/macchiato64/400/400.jpg'},
    {id:'cf7',name:{ku:'فلات وایت',ar:'فلات وايت',en:'Flat White'},price:3300,img:'https://picsum.photos/seed/flatwhite64/400/400.jpg'},
    {id:'cf8',name:{ku:'ئافوگاتۆ',ar:'افوجاتو',en:'Affogato'},price:4000,img:'https://picsum.photos/seed/affogato64/400/400.jpg'},
    {id:'cf9',name:{ku:'کەرەمێل لاتە',ar:'كارامل لاتيه',en:'Caramel Latte'},price:4000,img:'https://picsum.photos/seed/caramellatte64/400/400.jpg'},
    {id:'cf10',name:{ku:'فیلتەر کافی',ar:'فيلتر قهوة',en:'Filter Coffee'},price:2200,img:'https://picsum.photos/seed/filtercoffee64/400/400.jpg'}
  ],
  cold: [
    {id:'d1',name:{ku:'مۆجیتۆ',ar:'موهيتو',en:'Mojito'},price:3000,img:'https://picsum.photos/seed/mojito64/400/400.jpg'},
    {id:'d2',name:{ku:'لیمۆناد',ar:'ليموناد',en:'Lemonade'},price:2500,img:'https://picsum.photos/seed/lemonade64/400/400.jpg'},
    {id:'d3',name:{ku:'شیکەی ئاناناس',ar:'شيك أناناس',en:'Pineapple Shake'},price:3500,img:'https://picsum.photos/seed/pineappleshake64/400/400.jpg'},
    {id:'d4',name:{ku:'شیکەی توتفرەنگی',ar:'شيك فراولة',en:'Strawberry Shake'},price:3500,img:'https://picsum.photos/seed/strawshake64/400/400.jpg'},
    {id:'d5',name:{ku:'آیس لاتە',ar:'آيس لاتيه',en:'Iced Latte'},price:3500,img:'https://picsum.photos/seed/icedlatte64/400/400.jpg'},
    {id:'d6',name:{ku:'آیس ئەمریکانۆ',ar:'آيس أمريكانو',en:'Iced Americano'},price:3000,img:'https://picsum.photos/seed/icedamericano64/400/400.jpg'},
    {id:'d7',name:{ku:'فراپێچینۆ',ar:'فرابتشينو',en:'Frappuccino'},price:4000,img:'https://picsum.photos/seed/frappuccino64/400/400.jpg'},
    {id:'d8',name:{ku:'شیکەی چۆکلەت',ar:'شيك شوكولاتة',en:'Chocolate Shake'},price:3500,img:'https://picsum.photos/seed/chocshake64/400/400.jpg'},
    {id:'d9',name:{ku:'جوسی پرتەقاڵ',ar:'عصير برتقال',en:'Orange Juice'},price:2500,img:'https://picsum.photos/seed/orangejuice64/400/400.jpg'},
    {id:'d10',name:{ku:'سمووتی توت',ar:'سموذي توت',en:'Berry Smoothie'},price:3800,img:'https://picsum.photos/seed/berrysmoothie64/400/400.jpg'}
  ]
};

/* وێنەکانی گەلەری */
const galleryImages = [
  {src:'https://picsum.photos/seed/cafe64g1/800/800.jpg',title:{ku:'ناوخانی کافێ',ar:'داخل الكافيه',en:'Cafe Interior'}},
  {src:'https://picsum.photos/seed/cafe64g2/800/800.jpg',title:{ku:'قاوەی تازە',ar:'قهوة طازجة',en:'Fresh Coffee'}},
  {src:'https://picsum.photos/seed/cafe64g3/800/800.jpg',title:{ku:'شیرینیەکان',ar:'الحلويات',en:'Desserts'}},
  {src:'https://picsum.photos/seed/cafe64g4/800/800.jpg',title:{ku:'مێزەکان',ar:'الطاولات',en:'Tables'}},
  {src:'https://picsum.photos/seed/cafe64g5/800/800.jpg',title:{ku:'لایەنی دەرەکی',ar:'الواجهة الخارجية',en:'Exterior'}},
  {src:'https://picsum.photos/seed/cafe64g6/800/800.jpg',title:{ku:'کاپوچینۆ',ar:'كابتشينو',en:'Cappuccino'}},
  {src:'https://picsum.photos/seed/cafe64g7/800/800.jpg',title:{ku:'کێکەکان',ar:'الكيكات',en:'Cakes'}},
  {src:'https://picsum.photos/seed/cafe64g8/800/800.jpg',title:{ku:'ئەتەشگە',ar:'الموقد',en:'Fireplace'}},
  {src:'https://picsum.photos/seed/cafe64g9/800/800.jpg',title:{ku:'خواردنەوە ساردەکان',ar:'المشروبات الباردة',en:'Cold Drinks'}},
  {src:'https://picsum.photos/seed/cafe64g10/800/800.jpg',title:{ku:'ئێوارانی کافێ',ar:'مساء الكافيه',en:'Cafe Evening'}}
];

/* وەرگێڕان */
const i18n = {
  ku:{
    welcomeTitle:'بەخێربێیت بۆ CAFE_64',
    welcomeSub:'چێژ لە باشترین قاوە و شیرینیەکان وەربگرە',
    start:'دەستپێبکە',
    catCake:'کێک',catSweet:'شیرینی',catCoffee:'قاوە',catCold:'خواردنەوەی سارد',
    selectTable:'مێزێک هەڵبژێرە',selectTableDesc:'تکایە مێزی خۆت هەڵبژێرە',
    tableWord:'مێز',
    navHome:'سەرەتا',navMenu:'مێنیو',navTables:'مێزەکان',navOrder:'ئۆردەر',navGallery:'گەلەری',
    galleryTitle:'گەلەری',galleryDesc:'وێنەکانی کافێکەمان ببینە',
    download:'داگرتن',
    orderEmpty:'هیچ بابەتێک نییە لە ئۆردەردا',
    orderEmptySub:'سەرەتا لە مێنیو بابەت زیاد بکە',
    sendOrder:'ناردنی ئۆردەر',
    total:'کۆی گشتی',
    added:'زیاد کرا',removed:'لابرا',
    selectTableFirst:'تکایە سەرەتا مێزێک هەڵبژێرە',
    orderSent:'ئۆردەرەکەت نێردرا!',
    tableLabel:'مێزی',
    iqd:'دینار'
  },
  ar:{
    welcomeTitle:'مرحباً بك في CAFE_64',
    welcomeSub:'استمتع بأفضل القهوة والحلويات',
    start:'ابدأ',
    catCake:'كيك',catSweet:'حلويات',catCoffee:'قهوة',catCold:'مشروبات باردة',
    selectTable:'اختر طاولة',selectTableDesc:'يرجى اختيار طاولتك',
    tableWord:'طاولة',
    navHome:'الرئيسية',navMenu:'القائمة',navTables:'الطاولات',navOrder:'الطلب',navGallery:'المعرض',
    galleryTitle:'المعرض',galleryDesc:'شاهد صور مقهانا',
    download:'تحميل',
    orderEmpty:'لا توجد عناصر في الطلب',
    orderEmptySub:'أضف عناصر من القائمة أولاً',
    sendOrder:'إرسال الطلب',
    total:'المجموع',
    added:'تمت الإضافة',removed:'تمت الإزالة',
    selectTableFirst:'يرجى اختيار طاولة أولاً',
    orderSent:'تم إرسال طلبك!',
    tableLabel:'طاولة',
    iqd:'دينار'
  },
  en:{
    welcomeTitle:'Welcome to CAFE_64',
    welcomeSub:'Enjoy the best coffee and desserts',
    start:'Get Started',
    catCake:'Cake',catSweet:'Sweets',catCoffee:'Coffee',catCold:'Cold Drinks',
    selectTable:'Select a Table',selectTableDesc:'Please choose your table',
    tableWord:'Table',
    navHome:'Home',navMenu:'Menu',navTables:'Tables',navOrder:'Order',navGallery:'Gallery',
    galleryTitle:'Gallery',galleryDesc:'See photos of our cafe',
    download:'Download',
    orderEmpty:'No items in your order',
    orderEmptySub:'Add items from the menu first',
    sendOrder:'Send Order',
    total:'Total',
    added:'Added',removed:'Removed',
    selectTableFirst:'Please select a table first',
    orderSent:'Your order has been sent!',
    tableLabel:'Table',
    iqd:'IQD'
  }
};

/* ========================================
   دۆخەکانی بەرنامەکە
   ======================================== */
let state = {
  lang: 'ku',
  theme: 'light',
  currentPage: 'page-welcome',
  selectedTable: null,
  currentCat: 'cake',
  order: []
};

/* ========================================
   یاریدەدەرەکان
   ======================================== */
const $ = s => document.querySelector(s);
const $$ = s => document.querySelectorAll(s);
const t = key => (i18n[state.lang] && i18n[state.lang][key]) || key;
const fmt = n => n.toLocaleString();

function showToast(msg, type='') {
  const toast = $('#toast');
  toast.textContent = msg;
  toast.className = 'toast show ' + type;
  clearTimeout(toast._timer);
  toast._timer = setTimeout(() => toast.className = 'toast', 2200);
}

/* ========================================
   تۆمەربوون / دارک مۆد
   ======================================== */
 $('#themeToggle').addEventListener('click', () => {
  state.theme = state.theme === 'light' ? 'dark' : 'light';
  document.documentElement.setAttribute('data-theme', state.theme);
  $('#sunIcon').style.display = state.theme === 'light' ? '' : 'none';
  $('#moonIcon').style.display = state.theme === 'dark' ? '' : 'none';
});

/* ========================================
   زمان
   ======================================== */
 $('#langToggle').addEventListener('click', (e) => {
  e.stopPropagation();
  $('#langMenu').classList.toggle('open');
});
document.addEventListener('click', () => $('#langMenu').classList.remove('open'));

 $$('.lang-item').forEach(el => {
  el.addEventListener('click', () => {
    const lang = el.dataset.lang;
    state.lang = lang;
    $$('.lang-item').forEach(i => i.classList.remove('active'));
    el.classList.add('active');
    $('#langMenu').classList.remove('open');
    if (lang === 'en') {
      document.documentElement.setAttribute('dir', 'ltr');
      document.documentElement.setAttribute('lang', 'en');
    } else {
      document.documentElement.setAttribute('dir', 'rtl');
      document.documentElement.setAttribute('lang', lang);
    }
    applyI18n();
    renderMenuCats();
    renderMenu();
    renderOrder();
    renderTables();
    renderGallery();
  });
});

function applyI18n() {
  $$('[data-i18n]').forEach(el => {
    const key = el.dataset.i18n;
    if (i18n[state.lang][key]) el.textContent = i18n[state.lang][key];
  });
  if (state.selectedTable !== null) {
    $('#orderTableName').textContent = t('tableLabel') + ' ' + state.selectedTable;
  }
}

/* ========================================
   پەڕەی بەخێرهاتن
   ======================================== */
 $('#startBtn').addEventListener('click', () => {
  navigateTo('page-menu');
});

/* ========================================
   نەڤیگەیشن - Apple Liquid Navbar
   ======================================== */
function navigateTo(pageId) {
  if (state.currentPage === pageId) return;
  state.currentPage = pageId;
  $$('.page').forEach(p => p.classList.remove('active'));
  const target = $('#' + pageId);
  if (target) {
    target.classList.add('active');
    target.scrollTop = 0;
  }
  $$('.nav-pill').forEach(pill => {
    pill.classList.toggle('active', pill.dataset.page === pageId);
  });
  if (pageId === 'page-order') renderOrder();
}

 $$('.nav-pill').forEach(pill => {
  pill.addEventListener('click', () => navigateTo(pill.dataset.page));
});

/* ========================================
   ڕێندەرکردنی مێنیو
   ======================================== */
function renderMenuCats() {
  const cats = [
    {key:'cake', i18nKey:'catCake'},
    {key:'sweet', i18nKey:'catSweet'},
    {key:'coffee', i18nKey:'catCoffee'},
    {key:'cold', i18nKey:'catCold'}
  ];
  $('#menuCats').innerHTML = cats.map(c =>
    `<button class="cat-btn${state.currentCat===c.key?' active':''}" data-cat="${c.key}">${t(c.i18nKey)}</button>`
  ).join('');
  $$('.cat-btn').forEach(btn => {
    btn.addEventListener('click', () => {
      state.currentCat = btn.dataset.cat;
      renderMenuCats();
      renderMenu();
    });
  });
}

function renderMenu() {
  const items = menuData[state.currentCat] || [];
  const grid = $('#menuGrid');
  grid.innerHTML = items.map((item, i) => {
    const inOrder = state.order.find(o => o.item.id === item.id);
    return `<div class="menu-card${inOrder?' in-order':''}" data-id="${item.id}" style="animation-delay:${i*0.05}s">
      <div class="menu-selected-badge">${inOrder ? inOrder.qty : ''}</div>
      <img class="menu-card-img" src="${item.img}" alt="${item.name[state.lang]}" loading="lazy">
      <div class="menu-card-body">
        <div class="menu-card-name">${item.name[state.lang]}</div>
        <div class="menu-card-price">${fmt(item.price)} ${t('iqd')}</div>
      </div>
    </div>`;
  }).join('');
  $$('.menu-card').forEach(card => {
    card.addEventListener('click', () => {
      const id = card.dataset.id;
      let found = null;
      for (const cat of Object.values(menuData)) {
        found = cat.find(i => i.id === id);
        if (found) break;
      }
      if (!found) return;
      const existing = state.order.find(o => o.item.id === id);
      if (existing) {
        existing.qty++;
      } else {
        state.order.push({item: found, qty: 1});
      }
      showToast(t('added') + ' ✓', 'success');
      renderMenu();
    });
  });
}

/* ========================================
   ڕێندەرکردنی مێزەکان
   ======================================== */
function renderTables() {
  $('#tableGrid').innerHTML = Array.from({length:15}, (_, i) => {
    const num = i + 1;
    const sel = state.selectedTable === num ? ' selected' : '';
    return `<div class="table-card${sel}" data-table="${num}">
      <div class="table-check">✓</div>
      <div class="table-num">${num}</div>
      <div class="table-label">${t('tableWord')}</div>
    </div>`;
  }).join('');
  $$('.table-card').forEach(card => {
    card.addEventListener('click', () => {
      state.selectedTable = parseInt(card.dataset.table);
      renderTables();
      showToast(t('tableLabel') + ' ' + state.selectedTable + ' ✓', 'success');
    });
  });
}

/* ========================================
   ڕێندەرکردنی ئۆردەر
   ======================================== */
function renderOrder() {
  const info = $('#orderTableInfo');
  if (state.selectedTable !== null) {
    info.style.display = 'flex';
    $('#orderTableName').textContent = t('tableLabel') + ' ' + state.selectedTable;
  } else {
    info.style.display = 'none';
  }
  const container = $('#orderContent');
  if (state.order.length === 0) {
    container.innerHTML = `<div class="order-empty">
      <svg width="64" height="64" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1.5"><path d="M6 2L3 6v14a2 2 0 0 0 2 2h14a2 2 0 0 0 2-2V6l-3-4z"/><line x1="3" y1="6" x2="21" y2="6"/><path d="M16 10a4 4 0 0 1-8 0"/></svg>
      <p>${t('orderEmpty')}</p>
      <p style="font-size:12px;margin-top:4px;opacity:.6">${t('orderEmptySub')}</p>
    </div>`;
    return;
  }
  let total = 0;
  const itemsHtml = state.order.map(o => {
    const sub = o.item.price * o.qty;
    total += sub;
    return `<div class="order-item">
      <img class="order-item-img" src="${o.item.img}" alt="${o.item.name[state.lang]}" loading="lazy">
      <div class="order-item-info">
        <div class="order-item-name">${o.item.name[state.lang]}</div>
        <div class="order-item-price">${fmt(sub)} ${t('iqd')}</div>
      </div>
      <div class="qty-controls">
        <button class="qty-btn" data-action="dec" data-id="${o.item.id}">−</button>
        <span class="qty-val">${o.qty}</span>
        <button class="qty-btn" data-action="inc" data-id="${o.item.id}">+</button>
      </div>
    </div>`;
  }).join('');
  container.innerHTML = `<div class="order-list">${itemsHtml}</div>
    <div class="order-footer">
      <div class="order-total">
        <span class="order-total-label">${t('total')}</span>
        <span class="order-total-val">${fmt(total)} ${t('iqd')}</span>
      </div>
      <button class="send-btn" id="sendOrderBtn">
        <svg width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5" stroke-linecap="round"><line x1="22" y1="2" x2="11" y2="13"/><polygon points="22 2 15 22 11 13 2 9 22 2"/></svg>
        ${t('sendOrder')}
      </button>
    </div>`;
  $$('.qty-btn').forEach(btn => {
    btn.addEventListener('click', (e) => {
      e.stopPropagation();
      const id = btn.dataset.id;
      const action = btn.dataset.action;
      const idx = state.order.findIndex(o => o.item.id === id);
      if (idx === -1) return;
      if (action === 'inc') {
        state.order[idx].qty++;
      } else {
        state.order[idx].qty--;
        if (state.order[idx].qty <= 0) {
          state.order.splice(idx, 1);
          showToast(t('removed'), 'error');
        }
      }
      renderOrder();
      renderMenu();
    });
  });
  $('#sendOrderBtn').addEventListener('click', sendOrder);
}

/* ========================================
   ناردنی ئۆردەر بۆ واتسئەپ
   ======================================== */
function sendOrder() {
  if (state.selectedTable === null) {
    showToast(t('selectTableFirst'), 'error');
    return;
  }
  if (state.order.length === 0) return;
  const phone = '9647505850338';
  let msg = `*CAFE_64*\n`;
  msg += `━━━━━━━━━━━━━━\n`;
  msg += `${t('tableLabel')}: *${state.selectedTable}*\n`;
  msg += `━━━━━━━━━━━━━━\n\n`;
  let total = 0;
  state.order.forEach(o => {
    const sub = o.item.price * o.qty;
    total += sub;
    msg += `• ${o.item.name[state.lang]} × ${o.qty} = ${fmt(sub)} ${t('iqd')}\n`;
  });
  msg += `\n━━━━━━━━━━━━━━\n`;
  msg += `${t('total')}: *${fmt(total)} ${t('iqd')}*\n`;
  window.open(`https://wa.me/${phone}?text=${encodeURIComponent(msg)}`, '_blank');
  showToast(t('orderSent'), 'success');
}

/* ========================================
   گەلەری
   ======================================== */
function renderGallery() {
  $('#galleryGrid').innerHTML = galleryImages.map((img, i) =>
    `<div class="gallery-item" data-idx="${i}" style="animation:cardIn .4s ease ${i*0.05}s both">
      <img src="${img.src}" alt="${img.title[state.lang]}" loading="lazy">
      <div class="gallery-overlay"><span>${img.title[state.lang]}</span></div>
    </div>`
  ).join('');
  $$('.gallery-item').forEach(item => {
    item.addEventListener('click', () => {
      const idx = parseInt(item.dataset.idx);
      openLightbox(galleryImages[idx].src);
    });
  });
}

/* ========================================
   لایتباکس
   ======================================== */
function openLightbox(src) {
  const highRes = src.replace('/800/800', '/1600/1600');
  $('#lightboxImg').src = src;
  $('#lightboxDl').dataset.src = highRes;
  $('#lightbox').classList.add('open');
}
 $('#lightboxClose').addEventListener('click', () => $('#lightbox').classList.remove('open'));
 $('#lightbox').addEventListener('click', (e) => {
  if (e.target === $('#lightbox')) $('#lightbox').classList.remove('open');
});
 $('#lightboxDl').addEventListener('click', () => {
  const src = $('#lightboxDl').dataset.src;
  const a = document.createElement('a');
  a.href = src;
  a.download = 'CAFE_64_' + Date.now() + '.jpg';
  a.target = '_blank';
  document.body.appendChild(a);
  a.click();
  document.body.removeChild(a);
  showToast(t('download') + ' ✓', 'success');
});

/* ========================================
   دەستپێکردن
   ======================================== */
function init() {
  renderMenuCats();
  renderMenu();
  renderTables();
  renderGallery();
  applyI18n();
  // چالاککردنی تابی سەرەتا
  $$('.nav-pill').forEach(pill => {
    pill.classList.toggle('active', pill.dataset.page === 'page-welcome');
  });
}
init();
</script>
</body>
</html>
