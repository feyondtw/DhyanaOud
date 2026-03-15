# DhyanaOud
Dhyana out's Html
<!-- =====================================================
  DHYANA OUDS — 可直接貼入 CYBERBIZ 自訂HTML
  不含 <!DOCTYPE> / <html> / <head> / <body>
  不含模擬 header / footer
  ===================================================== -->

<link href="https://fonts.googleapis.com/css2?family=Noto+Serif+TC:wght@300;400;500;600&family=Cormorant+Garamond:ital,wght@0,300;0,400;0,500;1,300;1,400&family=Cinzel:wght@400;500&display=swap" rel="stylesheet">

<style>
/* ── CSS 變數 ── */
.ouds-wrap { --oud-dark:#1a0e07; --oud-brown:#2e1a0d; --oud-amber:#b8762a; --oud-amber-l:#d4962e; --oud-gold:#c9a84c; --oud-cream:#f7f0e4; --oud-cream2:#ede4d4; --oud-text:#e8dcc8; --oud-muted:#a08060; --oud-green:#1a2e1a; --sf:'Noto Serif TC','Noto Sans TC',sans-serif; }

/* ── Reset 只作用在子頁內 ── */
.ouds-wrap *, .ouds-wrap *::before, .ouds-wrap *::after { box-sizing:border-box; margin:0; padding:0; }

/* ── 自訂游標 ── */
.ouds-wrap { cursor: none; }
.ouds-cursor-dot {
  position: fixed !important;
  top: 0 !important; left: 0 !important;
  width: 10px !important; height: 10px !important;
  background: #d4962e !important;
  border-radius: 50% !important;
  pointer-events: none !important;
  z-index: 2147483647 !important;
  box-shadow: 0 0 0 2px rgba(255,255,255,0.6), 0 0 10px rgba(212,150,46,0.9) !important;
  will-change: transform;
}
.ouds-cursor-ring {
  position: fixed !important;
  top: 0 !important; left: 0 !important;
  width: 38px !important; height: 38px !important;
  border: 2px solid rgba(212,150,46,0.8) !important;
  border-radius: 50% !important;
  pointer-events: none !important;
  z-index: 2147483646 !important;
  background: transparent !important;
  transition: width 0.22s ease, height 0.22s ease, border-color 0.22s ease, background 0.22s ease !important;
  will-change: transform;
}
.ouds-cursor-ring.ouds-hovering {
  width: 54px !important; height: 54px !important;
  border-color: rgba(212,150,46,0.5) !important;
  background: rgba(212,150,46,0.08) !important;
}
.ouds-cursor-dot.ouds-clicking {
  width: 5px !important; height: 5px !important;
  background: #c9a84c !important;
}
/* 文字游標區域 */
.ouds-wrap p, .ouds-wrap li, .ouds-wrap .ouds-story-col-body { cursor: none; }
/* 按鈕/連結區域顯示特殊狀態 */
.ouds-wrap a, .ouds-wrap button { cursor: none; }

/* ── 麵包屑 ── */
.ouds-breadcrumb-bar { background:#faf8f5; border-bottom:1px solid #e8e0d5; padding:10px 40px; font-family:var(--sf); }
.ouds-breadcrumb { max-width:1400px; margin:0 auto; display:flex; align-items:center; gap:8px; font-size:12px; color:#888; }
.ouds-breadcrumb a { color:#888; text-decoration:none; }
.ouds-breadcrumb a:hover { color:var(--oud-amber); }
.ouds-breadcrumb strong { color:#555; font-weight:500; }
.ouds-breadcrumb-sep { color:#bbb; }

/* ── Hero ── */
.ouds-hero { width:100%; background: linear-gradient(105deg,rgba(26,14,7,0.93) 0%,rgba(26,14,7,0.7) 50%,rgba(26,14,7,0.88) 100%), url('https://images.unsplash.com/photo-1611050894640-b6e1a855cd03?w=1600&q=80') center/cover no-repeat; padding:80px 40px; position:relative; overflow:hidden; }
.ouds-hero::after { content:''; position:absolute; bottom:0; left:0; right:0; height:3px; background:linear-gradient(90deg,transparent 0%,var(--oud-amber) 30%,var(--oud-gold) 50%,var(--oud-amber) 70%,transparent 100%); }
.ouds-hero-inner { max-width:1400px; margin:0 auto; display:grid; grid-template-columns:1fr 1fr; gap:60px; align-items:center; }
.ouds-hero-badge { display:inline-flex; align-items:center; gap:10px; background:rgba(184,118,42,0.15); border:1px solid rgba(184,118,42,0.4); padding:6px 16px; margin-bottom:20px; }
.ouds-hero-badge span { font-family:'Cinzel',serif; font-size:9px; letter-spacing:0.4em; color:var(--oud-amber-l); text-transform:uppercase; }
.ouds-hero-badge::before { content:'●'; color:var(--oud-amber); font-size:6px; animation:ouds-pulse 2s infinite; }
@keyframes ouds-pulse { 0%,100%{opacity:1} 50%{opacity:0.3} }
.ouds-hero-eyebrow { font-family:var(--sf); font-size:11px; letter-spacing:0.35em; color:var(--oud-amber-l); text-transform:uppercase; margin-bottom:16px; }
.ouds-hero-title { font-family:'Cinzel',serif; font-size:clamp(36px,5vw,68px); font-weight:400; color:#fff; line-height:1.05; letter-spacing:0.06em; margin-bottom:8px; }
.ouds-hero-subtitle { font-family:'Cormorant Garamond',serif; font-size:clamp(18px,2.5vw,26px); font-style:italic; color:var(--oud-amber-l); letter-spacing:0.1em; margin-bottom:24px; }
.ouds-hero-desc { font-family:var(--sf); font-size:14px; line-height:1.9; color:rgba(232,220,200,0.75); max-width:480px; margin-bottom:36px; }
.ouds-hero-cta { display:inline-flex; align-items:center; gap:12px; background:var(--oud-amber); color:#fff; text-decoration:none; font-family:var(--sf); font-size:13px; letter-spacing:0.15em; padding:14px 32px; transition:background 0.3s; }
.ouds-hero-cta:hover { background:var(--oud-amber-l); color:#fff; }
.ouds-hero-cta-ghost { display:inline-flex; align-items:center; gap:12px; border:1px solid rgba(184,118,42,0.5); color:var(--oud-amber-l); text-decoration:none; font-family:var(--sf); font-size:13px; letter-spacing:0.15em; padding:14px 32px; margin-left:16px; transition:all 0.3s; }
.ouds-hero-cta-ghost:hover { background:rgba(184,118,42,0.1); border-color:var(--oud-amber); color:#fff; }
.ouds-hero-right { display:flex; flex-direction:column; gap:16px; }
.ouds-hero-stat-row { display:grid; grid-template-columns:repeat(3,1fr); gap:2px; }
.ouds-hero-stat { background:rgba(255,255,255,0.04); border:1px solid rgba(184,118,42,0.15); padding:20px 16px; text-align:center; transition:background 0.3s; }
.ouds-hero-stat:hover { background:rgba(184,118,42,0.08); }
.ouds-hero-stat-num { font-family:'Cinzel',serif; font-size:28px; color:var(--oud-gold); font-weight:400; line-height:1; margin-bottom:6px; }
.ouds-hero-stat-label { font-family:var(--sf); font-size:10px; color:var(--oud-muted); letter-spacing:0.1em; line-height:1.5; }
.ouds-hero-partner { background:rgba(255,255,255,0.03); border:1px solid rgba(184,118,42,0.15); padding:20px 24px; display:flex; align-items:center; gap:20px; }
.ouds-partner-quote { font-family:'Cormorant Garamond',serif; font-size:15px; font-style:italic; color:var(--oud-text); line-height:1.6; flex:1; }
.ouds-partner-info { text-align:right; flex-shrink:0; }
.ouds-partner-name { font-family:'Cinzel',serif; font-size:10px; letter-spacing:0.2em; color:var(--oud-amber); text-transform:uppercase; }
.ouds-partner-role { font-size:10px; color:var(--oud-muted); margin-top:4px; }

/* ── Tabs ── */
.ouds-tabs-bar { background:var(--oud-cream); border-bottom:2px solid var(--oud-cream2); position:sticky; top:0; z-index:200; }
.ouds-tabs { max-width:1400px; margin:0 auto; padding:0 40px; display:flex; gap:0; overflow-x:auto; scrollbar-width:none; }
.ouds-tabs::-webkit-scrollbar { display:none; }
.ouds-tab { font-family:var(--sf); font-size:13px; letter-spacing:0.08em; color:#666; padding:16px 24px; border:none; background:none; cursor:pointer; border-bottom:2px solid transparent; margin-bottom:-2px; white-space:nowrap; transition:all 0.2s; }
.ouds-tab:hover { color:var(--oud-amber); }
.ouds-tab.ouds-active { color:var(--oud-amber); border-bottom-color:var(--oud-amber); font-weight:500; }

/* ── Page Body ── */
.ouds-page-body { background:var(--oud-cream); font-family:var(--sf); }

/* ── Section ── */
.ouds-section { max-width:1400px; margin:0 auto; padding:72px 40px; }
.ouds-section-title { font-family:'Noto Serif TC',serif; font-size:clamp(20px,2.5vw,28px); font-weight:400; color:var(--oud-dark); letter-spacing:0.08em; margin-bottom:8px; }
.ouds-section-en { font-family:'Cinzel',serif; font-size:11px; letter-spacing:0.4em; color:var(--oud-amber); text-transform:uppercase; margin-bottom:12px; }
.ouds-rule { width:48px; height:2px; background:var(--oud-amber); margin-bottom:40px; }

/* ── 品牌故事 ── */
.ouds-story-grid { display:grid; grid-template-columns:1fr 1fr; gap:2px; background:var(--oud-cream2); }
.ouds-story-col { background:var(--oud-cream); padding:48px 40px; }
.ouds-story-col:first-child { border-right:2px solid var(--oud-amber); }
.ouds-story-col-label { font-family:'Cinzel',serif; font-size:12px; letter-spacing:0.3em; color:var(--oud-amber); text-transform:uppercase; margin-bottom:20px; }
.ouds-story-col-title { font-family:'Noto Serif TC',serif; font-size:24px; font-weight:500; color:var(--oud-dark); line-height:1.5; margin-bottom:20px; }
.ouds-story-col-body { font-size:15px; line-height:2; color:#555; }
.ouds-milestone-track { margin-top:48px; display:flex; flex-direction:column; gap:0; position:relative; }
.ouds-milestone-track::before { content:''; position:absolute; left:24px; top:0; bottom:0; width:1px; background:linear-gradient(180deg,var(--oud-amber),var(--oud-amber-l),transparent); }
.ouds-milestone { display:flex; flex-direction:column; padding:0 0 32px 0; position:relative; }
.ouds-milestone-year-col { display:flex; align-items:flex-start; gap:20px; }
.ouds-milestone-dot { width:48px; height:48px; border:2px solid var(--oud-amber); background:var(--oud-cream); border-radius:50%; display:flex; align-items:center; justify-content:center; flex-shrink:0; position:relative; z-index:2; }
.ouds-milestone-dot span { font-family:'Cinzel',serif; font-size:11px; color:var(--oud-amber); letter-spacing:0.05em; font-weight:500; }
.ouds-milestone-content { padding-left:68px; margin-top:-48px; }
.ouds-milestone-title { font-weight:600; font-size:15px; color:var(--oud-dark); margin-bottom:6px; }
.ouds-milestone-desc { font-size:14px; color:#666; line-height:1.8; }

/* ── 四大窖藏 ── */
.ouds-products-section { background:#fff; }
.ouds-products-grid { display:grid; grid-template-columns:repeat(4,1fr); gap:1px; background:var(--oud-cream2); border:1px solid var(--oud-cream2); }
.ouds-product-card { background:#fff; position:relative; cursor:pointer; transition:box-shadow 0.3s; }
.ouds-product-card:hover { box-shadow:0 8px 32px rgba(26,14,7,0.12); z-index:2; }
.ouds-product-card-img { aspect-ratio:3/4; background:var(--oud-dark); position:relative; overflow:hidden; display:flex; align-items:center; justify-content:center; }
.ouds-product-card-badge { position:absolute; top:16px; left:16px; background:var(--oud-amber); color:#fff; font-family:'Cinzel',serif; font-size:8px; letter-spacing:0.3em; padding:4px 10px; text-transform:uppercase; }
.ouds-product-card-body { padding:20px 20px 24px; }
.ouds-product-region-tag { font-family:'Cinzel',serif; font-size:8px; letter-spacing:0.35em; color:var(--oud-amber); text-transform:uppercase; margin-bottom:6px; }
.ouds-product-name { font-family:'Cormorant Garamond',serif; font-size:28px; font-weight:400; font-style:italic; color:var(--oud-dark); margin-bottom:4px; line-height:1; }
.ouds-product-type { font-size:11px; color:#888; letter-spacing:0.1em; margin-bottom:16px; }
.ouds-note-group { margin-bottom:10px; }
.ouds-note-group-label { font-size:9px; letter-spacing:0.3em; color:#aaa; text-transform:uppercase; margin-bottom:4px; }
.ouds-note-tags { display:flex; flex-wrap:wrap; gap:4px; }
.ouds-note-tag { font-size:11px; color:#666; background:var(--oud-cream); border:1px solid var(--oud-cream2); padding:2px 8px; letter-spacing:0.05em; transition:all 0.2s; }
.ouds-product-card:hover .ouds-note-tag { border-color:rgba(184,118,42,0.3); color:var(--oud-amber); }
.ouds-aroma-bars { margin-top:14px; display:flex; flex-direction:column; gap:5px; }
.ouds-aroma-bar-row { display:flex; align-items:center; gap:8px; }
.ouds-aroma-bar-name { font-size:10px; color:#999; width:48px; flex-shrink:0; }
.ouds-aroma-bar-track { flex:1; height:3px; background:#eee; }
.ouds-aroma-bar-fill { height:100%; background:linear-gradient(90deg,var(--oud-brown),var(--oud-amber)); }
.ouds-product-card-footer { padding:16px 20px 20px; display:flex; align-items:center; justify-content:space-between; border-top:1px solid var(--oud-cream2); }
.ouds-inquiry-btn { font-family:var(--sf); font-size:11px; letter-spacing:0.15em; color:var(--oud-dark); background:none; border:1px solid var(--oud-dark); padding:8px 16px; cursor:pointer; transition:all 0.2s; text-decoration:none; display:inline-block; }
.ouds-inquiry-btn:hover { background:var(--oud-dark); color:#fff; }
.ouds-sample-btn { font-size:11px; letter-spacing:0.1em; color:var(--oud-amber); background:none; border:none; cursor:pointer; text-decoration:underline; text-underline-offset:3px; }

/* ── 風土 ── */
.ouds-terroir-section { background:var(--oud-dark); }
.ouds-terroir-inner { display:grid; grid-template-columns:1fr 1fr; gap:0; }
.ouds-terroir-col { padding:60px 48px; position:relative; border:1px solid rgba(184,118,42,0.1); }
.ouds-terroir-col:first-child { border-right:1px solid rgba(184,118,42,0.2); }
.ouds-terroir-percent { font-family:'Cinzel',serif; font-size:64px; color:var(--oud-amber); font-weight:400; line-height:1; opacity:0.3; position:absolute; top:40px; right:40px; }
.ouds-terroir-col-title { font-family:'Cinzel',serif; font-size:14px; letter-spacing:0.3em; color:#fff; text-transform:uppercase; margin-bottom:6px; }
.ouds-terroir-col-sub { font-family:'Cormorant Garamond',serif; font-size:14px; font-style:italic; color:var(--oud-amber-l); margin-bottom:24px; }
.ouds-terroir-col-desc { font-size:14px; line-height:1.9; color:var(--oud-muted); margin-bottom:28px; }
.ouds-terroir-attrs { display:flex; flex-direction:column; gap:12px; }
.ouds-terroir-attr { display:flex; gap:12px; align-items:flex-start; font-size:12px; }
.ouds-terroir-attr-key { color:var(--oud-amber); width:80px; flex-shrink:0; letter-spacing:0.05em; }
.ouds-terroir-attr-val { color:var(--oud-muted); line-height:1.5; }
.ouds-terroir-aroma-note { margin-top:28px; padding:16px 20px; border-left:3px solid var(--oud-amber); background:rgba(184,118,42,0.06); }
.ouds-terroir-aroma-note p { font-family:'Cormorant Garamond',serif; font-size:15px; font-style:italic; color:var(--oud-text); line-height:1.7; }

/* ── 工序 ── */
.ouds-process-section { background:var(--oud-cream); }
.ouds-process-steps { display:grid; grid-template-columns:repeat(7,1fr); gap:0; position:relative; margin-top:40px; }
.ouds-process-steps::before { content:''; position:absolute; top:36px; left:5%; right:5%; height:1px; background:linear-gradient(90deg,transparent,var(--oud-amber-l),var(--oud-amber-l),transparent); opacity:0.3; }
.ouds-process-step { display:flex; flex-direction:column; align-items:center; padding:0 8px; text-align:center; transition:transform 0.3s; }
.ouds-process-step:hover { transform:translateY(-4px); }
.ouds-ps-icon { width:72px; height:72px; border:1px solid rgba(184,118,42,0.35); background:#fff; border-radius:50%; display:flex; align-items:center; justify-content:center; font-size:22px; margin-bottom:16px; position:relative; z-index:2; transition:all 0.3s; }
.ouds-process-step:hover .ouds-ps-icon { border-color:var(--oud-amber); box-shadow:0 4px 16px rgba(184,118,42,0.2); }
.ouds-ps-num { font-family:'Cinzel',serif; font-size:8px; color:var(--oud-amber); letter-spacing:0.2em; margin-bottom:4px; }
.ouds-ps-name { font-size:10px; letter-spacing:0.12em; color:#555; text-transform:uppercase; margin-bottom:4px; font-weight:500; }
.ouds-ps-zh { font-size:12px; color:#777; }

/* ── 數字 ── */
.ouds-numbers-section { background:var(--oud-brown); }
.ouds-numbers-grid { display:grid; grid-template-columns:repeat(4,1fr); gap:2px; background:rgba(255,255,255,0.05); margin-top:48px; }
.ouds-number-card { background:rgba(255,255,255,0.03); padding:40px 32px; text-align:center; border:1px solid rgba(184,118,42,0.1); transition:background 0.3s; }
.ouds-number-card:hover { background:rgba(184,118,42,0.08); }
.ouds-number-big { font-family:'Cinzel',serif; font-size:clamp(36px,4vw,60px); color:var(--oud-gold); font-weight:400; line-height:1; margin-bottom:4px; }
.ouds-number-unit { font-family:'Cormorant Garamond',serif; font-size:16px; font-style:italic; color:var(--oud-amber); margin-bottom:12px; }
.ouds-number-desc { font-size:12px; color:var(--oud-muted); line-height:1.7; letter-spacing:0.05em; }

/* ── 永續 ── */
.ouds-sustain-section { background:var(--oud-green); }
.ouds-sustain-grid { display:grid; grid-template-columns:repeat(2,1fr); gap:2px; background:rgba(255,255,255,0.03); margin-top:48px; }
.ouds-sustain-card { background:rgba(255,255,255,0.02); padding:36px 32px; border:1px solid rgba(255,255,255,0.06); transition:background 0.3s; }
.ouds-sustain-card:hover { background:rgba(255,255,255,0.05); }
.ouds-sc-icon { font-size:28px; margin-bottom:12px; }
.ouds-sc-title { font-family:'Cinzel',serif; font-size:11px; letter-spacing:0.35em; color:#adc4ad; text-transform:uppercase; margin-bottom:16px; }
.ouds-sc-items { display:flex; flex-direction:column; gap:6px; }
.ouds-sc-item { font-size:12px; color:rgba(200,220,200,0.65); padding:5px 0; border-bottom:1px solid rgba(255,255,255,0.05); letter-spacing:0.05em; display:flex; align-items:center; gap:8px; }
.ouds-sc-item::before { content:'—'; color:#5a9a5a; font-size:10px; }

/* ── CTA ── */
.ouds-cta-section { background:var(--oud-cream); }
.ouds-cta-inner { display:grid; grid-template-columns:1fr 1fr; gap:0; background:var(--oud-dark); }
.ouds-cta-col { padding:60px 48px; }
.ouds-cta-col:first-child { border-right:1px solid rgba(184,118,42,0.2); }
.ouds-cta-title { font-family:'Noto Serif TC',serif; font-size:22px; font-weight:400; color:#fff; margin-bottom:16px; line-height:1.5; }
.ouds-cta-desc { font-size:14px; color:var(--oud-muted); line-height:1.9; margin-bottom:32px; }
.ouds-cta-btn { display:inline-block; background:var(--oud-amber); color:#fff; text-decoration:none; font-size:12px; letter-spacing:0.2em; padding:14px 32px; transition:background 0.3s; text-transform:uppercase; }
.ouds-cta-btn:hover { background:var(--oud-amber-l); color:#fff; }
.ouds-contact-list { list-style:none; display:flex; flex-direction:column; gap:16px; }
.ouds-contact-list li { display:flex; gap:16px; align-items:flex-start; font-size:13px; color:var(--oud-muted); line-height:1.6; }
.ouds-contact-list li strong { color:var(--oud-amber); font-weight:400; font-family:'Cinzel',serif; font-size:9px; letter-spacing:0.3em; text-transform:uppercase; width:60px; flex-shrink:0; padding-top:2px; }

/* ── Scroll Reveal ── */
.ouds-sr { opacity:1; transform:none; }


/* ── Responsive ── */
@media (max-width:1024px) {
  .ouds-products-grid { grid-template-columns:repeat(2,1fr); }
  .ouds-process-steps { grid-template-columns:repeat(4,1fr); gap:16px; }
  .ouds-process-steps::before { display:none; }
  .ouds-numbers-grid { grid-template-columns:repeat(2,1fr); }
}
@media (max-width:768px) {
  .ouds-hero { padding:60px 20px; }
  .ouds-hero-inner { grid-template-columns:1fr; }
  .ouds-hero-right { display:none; }
  .ouds-breadcrumb-bar { padding:10px 20px; }
  .ouds-tabs { padding:0 16px; }
  .ouds-section { padding:48px 20px; }
  .ouds-story-grid { grid-template-columns:1fr; }
  .ouds-story-col:first-child { border-right:none; border-bottom:2px solid var(--oud-amber); }
  .ouds-terroir-inner { grid-template-columns:1fr; }
  .ouds-terroir-col:first-child { border-right:none; border-bottom:1px solid rgba(184,118,42,0.2); }
  .ouds-products-grid { grid-template-columns:1fr; }
  .ouds-sustain-grid { grid-template-columns:1fr; }
  .ouds-cta-inner { grid-template-columns:1fr; }
  .ouds-cta-col:first-child { border-right:none; border-bottom:1px solid rgba(184,118,42,0.2); }
  .ouds-process-steps { grid-template-columns:repeat(2,1fr); }
  .ouds-numbers-grid { grid-template-columns:1fr 1fr; }
  .ouds-hero-cta-ghost { margin-left:0; margin-top:12px; }
}
</style>

<!-- ════════ 外層容器（CSS 變數作用域） ════════ -->
<div class="ouds-wrap">

<!-- 自訂游標 -->
<div class="ouds-cursor-dot" id="oudsCursorDot"></div>
<div class="ouds-cursor-ring" id="oudsCursorRing"></div>

<!-- 麵包屑 -->
<div class="ouds-breadcrumb-bar">
  <nav class="ouds-breadcrumb">
    <a href="/zh-TW">首頁</a>
    <span class="ouds-breadcrumb-sep">›</span>
    <a href="/pages/dhyanas-brand">根本子品牌</a>
    <span class="ouds-breadcrumb-sep">›</span>
    <strong>Dhyana Ouds 越南沉香</strong>
  </nav>
</div>

<!-- Hero -->
<div class="ouds-hero">
  <div class="ouds-hero-inner">
    <div>
      <div class="ouds-hero-badge"><span>Taiwan · Dubai · Vietnam</span></div>
      <p class="ouds-hero-eyebrow">根本子品牌 · 越南沉香系列</p>
      <h1 class="ouds-hero-title">DHYANA<br>OUDS</h1>
      <p class="ouds-hero-subtitle">Vietnam Oud Collection</p>
      <p class="ouds-hero-desc">每一抹沉香都蘊含靈魂。自1980年代末，Trang女士的家族傳承，結合現代標準化工藝，將越南最純粹的沉香精油帶給世界。UEBT生物貿易倫理認證，從種植到蒸餾，全程溯源。</p>
      <div style="display:flex;flex-wrap:wrap;gap:12px">
        <a href="#ouds-grand-cru" class="ouds-hero-cta">探索四大窖藏</a>
        <a href="#ouds-contact" class="ouds-hero-cta-ghost">洽詢採購</a>
      </div>
    </div>
    <div class="ouds-hero-right">
      <div class="ouds-hero-stat-row">
        <div class="ouds-hero-stat"><div class="ouds-hero-stat-num">15</div><div class="ouds-hero-stat-label">年<br>培育週期</div></div>
        <div class="ouds-hero-stat"><div class="ouds-hero-stat-num">12</div><div class="ouds-hero-stat-label">座<br>認證莊園</div></div>
        <div class="ouds-hero-stat"><div class="ouds-hero-stat-num">UEBT</div><div class="ouds-hero-stat-label">生物貿易<br>倫理認證</div></div>
      </div>
      <div class="ouds-hero-partner">
        <p class="ouds-partner-quote">"Agarwood carries a soul. It must be preserved by those who truly understand it."</p>
        <div class="ouds-partner-info">
          <div class="ouds-partner-name">Mrs. Trang</div>
          <div class="ouds-partner-role">Dhyana Vietnamese Partner</div>
        </div>
      </div>
      <div class="ouds-hero-stat-row">
        <div class="ouds-hero-stat"><div class="ouds-hero-stat-num">1,000</div><div class="ouds-hero-stat-label">棵樹方得<br>40kg 精油</div></div>
        <div class="ouds-hero-stat"><div class="ouds-hero-stat-num">0.04%</div><div class="ouds-hero-stat-label">極稀有<br>產出率</div></div>
        <div class="ouds-hero-stat"><div class="ouds-hero-stat-num">4</div><div class="ouds-hero-stat-label">Grand<br>Cru 系列</div></div>
      </div>
    </div>
  </div>
</div>

<!-- Tabs -->
<div class="ouds-tabs-bar">
  <div class="ouds-tabs">
    <button class="ouds-tab ouds-active" onclick="oudsTab(this,'ouds-story')">品牌故事</button>
    <button class="ouds-tab" onclick="oudsTab(this,'ouds-grand-cru')">四大窖藏</button>
    <button class="ouds-tab" onclick="oudsTab(this,'ouds-terroir')">栽種區域</button>
    <button class="ouds-tab" onclick="oudsTab(this,'ouds-process')">蒸餾工藝</button>
    <button class="ouds-tab" onclick="oudsTab(this,'ouds-numbers')">滴滴珍稀</button>
    <button class="ouds-tab" onclick="oudsTab(this,'ouds-sustain')">永續認證</button>
    <button class="ouds-tab" onclick="oudsTab(this,'ouds-contact')">聯絡採購</button>
  </div>
</div>

<div class="ouds-page-body">

  <!-- 品牌故事 -->
  <section id="ouds-story">
    <div class="ouds-story-grid ouds-sr">
      <div class="ouds-story-col">
        <div class="ouds-story-col-label">品牌宣言 · Brand Story</div>
        <h2 class="ouds-story-col-title">從越南森林到世界<br>一份承載文化靈魂的傳承</h2>
        <p class="ouds-story-col-body">1980年代末，越南農村女性Trang女士，決定停止對野生森林的索求，轉而親手開啟沉香油的蒸餾事業。這份事業奠基於豐富閱歷與傳統技藝，更源於她相信香氣能傳遞深遠的意義。<br><br>今日，Dhyana Ouds 擁有完整的傳統萃取工藝，從最初的林木篩選與培育、結香引導，到最終的精油萃取，全程一手掌握。在傳統中融入技術革新，成為首間獲得UEBT生物貿易倫理聯盟認證的沉香生產商。</p>
        <div style="margin-top:28px;overflow:hidden;">
          <img src="data:ima插入圖A" alt="Dhyana Ouds 產品" style="width:100%;height:220px;object-fit:cover;object-position:center 40%;display:block;filter:brightness(0.95);">
        </div>
      </div>
      <div class="ouds-story-col">
        <div class="ouds-story-col-label">合作里程碑 · Milestones</div>
        <div class="ouds-milestone-track">
          <div class="ouds-milestone">
            <div class="ouds-milestone-year-col"><div class="ouds-milestone-dot"><span>2017</span></div></div>
            <div class="ouds-milestone-content"><div class="ouds-milestone-title">建立根本合作供應鏈</div><div class="ouds-milestone-desc">Trang女士開始與根本芳療建立合作，共同打造穩定、潔淨且永續的沉香精油供應鏈。</div></div>
          </div>
          <div class="ouds-milestone">
            <div class="ouds-milestone-year-col"><div class="ouds-milestone-dot"><span>2022</span></div></div>
            <div class="ouds-milestone-content"><div class="ouds-milestone-title">UEBT 認證 · 全新工廠落成</div><div class="ouds-milestone-desc">首間獲得UEBT生物貿易倫理聯盟認證的沉香生產商。設立里昂、台灣銷售辦事處，簽署歐洲經銷合約。</div></div>
          </div>
          <div class="ouds-milestone">
            <div class="ouds-milestone-year-col"><div class="ouds-milestone-dot"><span>2026</span></div></div>
            <div class="ouds-milestone-content"><div class="ouds-milestone-title">中東市場拓展 · 第三工廠</div><div class="ouds-milestone-desc">與Villa 515建立中東合作夥伴關係。客戶已涵蓋全球前十大香精香料公司。越南第三座沉香精油工廠落成。</div></div>
          </div>
        </div>
      </div>
    </div>
  </section>

  <!-- 四大窖藏 -->
  <section id="ouds-grand-cru" class="ouds-products-section">
    <div class="ouds-section ouds-sr">
      <div class="ouds-section-en">4 Grand Cru</div>
      <h2 class="ouds-section-title">四大特等窖藏系列</h2>
      <div class="ouds-rule"></div>
    </div>
    <div class="ouds-products-grid ouds-sr">

      <!-- FO-N -->
      <div class="ouds-product-card">
        <div class="ouds-product-card-img">
          <img src="data:image/插入圖" alt="FO-N 北部精油" style="width:70%;height:100%;object-fit:contain;padding:20px;">
          <div class="ouds-product-card-badge">North</div>
        </div>
        <div class="ouds-product-card-body">
          <div class="ouds-product-region-tag">北部產區 · Essential Oil</div>
          <div class="ouds-product-name">FO-N</div>
          <div class="ouds-product-type">Agarwood Oil — North Region</div>
          <div class="ouds-note-group"><div class="ouds-note-group-label">Top Notes</div><div class="ouds-note-tags"><span class="ouds-note-tag">煙燻木質</span><span class="ouds-note-tag">琥珀</span><span class="ouds-note-tag">陳木</span></div></div>
          <div class="ouds-note-group"><div class="ouds-note-group-label">Base Notes</div><div class="ouds-note-tags"><span class="ouds-note-tag">皮革</span><span class="ouds-note-tag">礦石</span></div></div>
          <div class="ouds-aroma-bars">
            <div class="ouds-aroma-bar-row"><span class="ouds-aroma-bar-name">Woody</span><div class="ouds-aroma-bar-track"><div class="ouds-aroma-bar-fill" style="width:85%"></div></div></div>
            <div class="ouds-aroma-bar-row"><span class="ouds-aroma-bar-name">Smokey</span><div class="ouds-aroma-bar-track"><div class="ouds-aroma-bar-fill" style="width:70%"></div></div></div>
            <div class="ouds-aroma-bar-row"><span class="ouds-aroma-bar-name">Leather</span><div class="ouds-aroma-bar-track"><div class="ouds-aroma-bar-fill" style="width:55%"></div></div></div>
          </div>
        </div>
        <div class="ouds-product-card-footer">
          <a href="#ouds-contact" class="ouds-inquiry-btn">索取樣品</a>
          <button class="ouds-sample-btn">了解更多</button>
        </div>
      </div>

      <!-- S-BO-N -->
      <div class="ouds-product-card">
        <div class="ouds-product-card-img">
          <img src="data:image/webp;插入圖" alt="S-BO-N Premium Boya" style="width:70%;height:100%;object-fit:contain;padding:20px;">
          <div class="ouds-product-card-badge" style="background:var(--oud-brown)">Premium</div>
        </div>
        <div class="ouds-product-card-body">
          <div class="ouds-product-region-tag">北部產區 · Premium Boya</div>
          <div class="ouds-product-name">S-BO-N</div>
          <div class="ouds-product-type">Premium Boya — North Region</div>
          <div class="ouds-note-group"><div class="ouds-note-group-label">Top Notes</div><div class="ouds-note-tags"><span class="ouds-note-tag">動物暖感</span><span class="ouds-note-tag">煙燻乾果</span></div></div>
          <div class="ouds-note-group"><div class="ouds-note-group-label">Base Notes</div><div class="ouds-note-tags"><span class="ouds-note-tag">柔韌皮革</span><span class="ouds-note-tag">炭香樹脂</span></div></div>
          <div class="ouds-aroma-bars">
            <div class="ouds-aroma-bar-row"><span class="ouds-aroma-bar-name">Leather</span><div class="ouds-aroma-bar-track"><div class="ouds-aroma-bar-fill" style="width:80%"></div></div></div>
            <div class="ouds-aroma-bar-row"><span class="ouds-aroma-bar-name">Animalic</span><div class="ouds-aroma-bar-track"><div class="ouds-aroma-bar-fill" style="width:75%"></div></div></div>
            <div class="ouds-aroma-bar-row"><span class="ouds-aroma-bar-name">Smokey</span><div class="ouds-aroma-bar-track"><div class="ouds-aroma-bar-fill" style="width:65%"></div></div></div>
          </div>
        </div>
        <div class="ouds-product-card-footer">
          <a href="#ouds-contact" class="ouds-inquiry-btn">索取樣品</a>
          <button class="ouds-sample-btn">了解更多</button>
        </div>
      </div>

      <!-- G-BO-N -->
      <div class="ouds-product-card">
        <div class="ouds-product-card-img">
          <img src="data:image/插入圖" alt="G-BO-N Medium Boya" style="width:70%;height:100%;object-fit:contain;padding:20px;">
          <div class="ouds-product-card-badge" style="background:#7a6010">Medium</div>
        </div>
        <div class="ouds-product-card-body">
          <div class="ouds-product-region-tag">北部產區 · Medium Boya</div>
          <div class="ouds-product-name">G-BO-N</div>
          <div class="ouds-product-type">Medium Boya — North Region</div>
          <div class="ouds-note-group"><div class="ouds-note-group-label">Top Notes</div><div class="ouds-note-tags"><span class="ouds-note-tag">動物感</span><span class="ouds-note-tag">酸韻</span><span class="ouds-note-tag">發酵果</span></div></div>
          <div class="ouds-note-group"><div class="ouds-note-group-label">Base Notes</div><div class="ouds-note-tags"><span class="ouds-note-tag">酚煙</span><span class="ouds-note-tag">皮革樹脂</span></div></div>
          <div class="ouds-aroma-bars">
            <div class="ouds-aroma-bar-row"><span class="ouds-aroma-bar-name">Animalic</span><div class="ouds-aroma-bar-track"><div class="ouds-aroma-bar-fill" style="width:90%"></div></div></div>
            <div class="ouds-aroma-bar-row"><span class="ouds-aroma-bar-name">Fruity</span><div class="ouds-aroma-bar-track"><div class="ouds-aroma-bar-fill" style="width:60%"></div></div></div>
            <div class="ouds-aroma-bar-row"><span class="ouds-aroma-bar-name">Smokey</span><div class="ouds-aroma-bar-track"><div class="ouds-aroma-bar-fill" style="width:55%"></div></div></div>
          </div>
        </div>
        <div class="ouds-product-card-footer">
          <a href="#ouds-contact" class="ouds-inquiry-btn">索取樣品</a>
          <button class="ouds-sample-btn">了解更多</button>
        </div>
      </div>

      <!-- FO-S -->
      <div class="ouds-product-card">
        <div class="ouds-product-card-img">
          <img src="data:image插入圖" alt="FO-S 南部精油" style="width:70%;height:100%;object-fit:contain;padding:20px;">
          <div class="ouds-product-card-badge" style="background:#3a6030">South</div>
        </div>
        <div class="ouds-product-card-body">
          <div class="ouds-product-region-tag">南部產區 · Essential Oil</div>
          <div class="ouds-product-name">FO-S</div>
          <div class="ouds-product-type">Agarwood Oil — South Region</div>
          <div class="ouds-note-group"><div class="ouds-note-group-label">Top Notes</div><div class="ouds-note-tags"><span class="ouds-note-tag">多汁果香</span><span class="ouds-note-tag">熟果</span><span class="ouds-note-tag">柔滑樹脂</span></div></div>
          <div class="ouds-note-group"><div class="ouds-note-group-label">Base Notes</div><div class="ouds-note-tags"><span class="ouds-note-tag">柔木</span><span class="ouds-note-tag">淡煙</span></div></div>
          <div class="ouds-aroma-bars">
            <div class="ouds-aroma-bar-row"><span class="ouds-aroma-bar-name">Fruity</span><div class="ouds-aroma-bar-track"><div class="ouds-aroma-bar-fill" style="width:85%"></div></div></div>
            <div class="ouds-aroma-bar-row"><span class="ouds-aroma-bar-name">Amber</span><div class="ouds-aroma-bar-track"><div class="ouds-aroma-bar-fill" style="width:65%"></div></div></div>
            <div class="ouds-aroma-bar-row"><span class="ouds-aroma-bar-name">Woody</span><div class="ouds-aroma-bar-track"><div class="ouds-aroma-bar-fill" style="width:50%"></div></div></div>
          </div>
        </div>
        <div class="ouds-product-card-footer">
          <a href="#ouds-contact" class="ouds-inquiry-btn">索取樣品</a>
          <button class="ouds-sample-btn">了解更多</button>
        </div>
      </div>

    </div>
  </section>

  <!-- 風土區域 -->
  <section id="ouds-terroir" class="ouds-terroir-section" style="position:relative;background-image:url('data:imgA插入圖=');background-size:cover;background-position:center;background-attachment:fixed;">
  <div style="position:absolute;inset:0;background:rgba(15,7,3,0.78);"></div>
  <div style="position:relative;z-index:1;">
    <div class="ouds-section ouds-sr" style="padding-bottom:0">
      <div class="ouds-section-en" style="color:#adc4ad">Terroir</div>
      <h2 class="ouds-section-title" style="color:#fff">兩大栽種區域的風土個性</h2>
      <div class="ouds-rule"></div>
    </div>
    <div class="ouds-terroir-inner ouds-sr">
      <div class="ouds-terroir-col">
        <div class="ouds-terroir-percent">90%</div>
        <div class="ouds-terroir-col-title">North Region</div>
        <div class="ouds-terroir-col-sub">越南北部 · Ha Tinh · Hue</div>
        <p class="ouds-terroir-col-desc">副熱帶季風氣候，季節感鮮明，冬季涼爽，夏季炎熱，全年濕度與降雨量皆有顯著變化。以 Feralit 土質為主，結合強勁的老撾（Lao）季風影響。</p>
        <div class="ouds-terroir-attrs">
          <div class="ouds-terroir-attr"><span class="ouds-terroir-attr-key">土質</span><span class="ouds-terroir-attr-val">Feralit — 富含鐵、鋁氧化物，排水良好</span></div>
          <div class="ouds-terroir-attr"><span class="ouds-terroir-attr-key">年均溫</span><span class="ouds-terroir-attr-val">24–26°C，季節差異明顯</span></div>
          <div class="ouds-terroir-attr"><span class="ouds-terroir-attr-key">結香方式</span><span class="ouds-terroir-attr-val">人工鑽孔觸發 + 自然蟲害感染</span></div>
          <div class="ouds-terroir-attr"><span class="ouds-terroir-attr-key">選料方式</span><span class="ouds-terroir-attr-val">手工分批劈切，依樹脂紋路、密度、香氣分級</span></div>
        </div>
        <div class="ouds-terroir-aroma-note"><p>季節性氣候帶來更明亮的輕盈感，具有礦石感與青翠綠意邊緣——木質煙燻主導，皮革感深邃。</p></div>
      </div>
      <div class="ouds-terroir-col">
        <div class="ouds-terroir-percent">5%</div>
        <div class="ouds-terroir-col-title">South Region</div>
        <div class="ouds-terroir-col-sub">越南南部 · Dong Nai · Cat Tien</div>
        <p class="ouds-terroir-col-desc">恆常溫暖的熱帶氣候，濕度高且雨量充沛，全年氣溫變化極小。莊園位於 Cat Tien 國家公園緩衝區，以玄武岩（Bazan）土質為主。</p>
        <div class="ouds-terroir-attrs">
          <div class="ouds-terroir-attr"><span class="ouds-terroir-attr-key">土質</span><span class="ouds-terroir-attr-val">Bazan 玄武岩 — 富含礦物質，保水性佳</span></div>
          <div class="ouds-terroir-attr"><span class="ouds-terroir-attr-key">年均溫</span><span class="ouds-terroir-attr-val">26–28°C，濕度 80–82%</span></div>
          <div class="ouds-terroir-attr"><span class="ouds-terroir-attr-key">結香方式</span><span class="ouds-terroir-attr-val">去皮 + 生物菌液接種（永續友善工法）</span></div>
          <div class="ouds-terroir-attr"><span class="ouds-terroir-attr-key">選料方式</span><span class="ouds-terroir-attr-val">灰色樹脂木萃油；白色邊材作為生質燃料</span></div>
        </div>
        <div class="ouds-terroir-aroma-note"><p>較溫暖氣候展現更圓潤的厚實度，帶有香脂般的深邃感與絲滑的木質暖意，果香調鮮明。</p></div>
      </div>
    </div>
  </div>
  </section>

  <!-- 蒸餾工藝 -->
  <section id="ouds-process" class="ouds-process-section">
    <div class="ouds-section ouds-sr">
      <div class="ouds-section-en">Distillery Process</div>
      <h2 class="ouds-section-title">從原木到精華——七道工序</h2>
      <div class="ouds-rule"></div>
      <p style="font-size:14px;color:#666;max-width:600px;line-height:1.9">廠內自主受控蒸餾，傳統技藝與標準化製程並蓄。每一批次均有完整溯源記錄，無塑化劑殘留，符合全球出口標準。</p>
      <div class="ouds-process-steps">
        <div class="ouds-process-step">
          <div class="ouds-ps-icon" style="width:90px;height:90px;border:2px solid rgba(184,118,42,0.35);background:none;padding:0;overflow:hidden;border-radius:50%;">
            <img src="data:image/webp;base64,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" alt="原木接收" style="width:100%;height:100%;object-fit:cover;display:block;">
          </div>
          <div class="ouds-ps-num">01</div>
          <div class="ouds-ps-name">Receiving</div>
          <div class="ouds-ps-zh">原木接收</div>
        </div>
        <div class="ouds-process-step">
          <div class="ouds-ps-icon" style="width:90px;height:90px;border:2px solid rgba(184,118,42,0.35);background:none;padding:0;overflow:hidden;border-radius:50%;">
            <img src="data:image/w插入圖" alt="研磨粉碎" style="width:100%;height:100%;object-fit:cover;display:block;">
          </div>
          <div class="ouds-ps-num">02</div>
          <div class="ouds-ps-name">Grinding</div>
          <div class="ouds-ps-zh">研磨粉碎</div>
        </div>
        <div class="ouds-process-step">
          <div class="ouds-ps-icon" style="width:90px;height:90px;border:2px solid rgba(184,118,42,0.35);background:none;padding:0;overflow:hidden;border-radius:50%;">
            <img src="data:image/we插入圖" alt="受控浸漬" style="width:100%;height:100%;object-fit:cover;display:block;">
          </div>
          <div class="ouds-ps-num">03</div>
          <div class="ouds-ps-name">Maceration</div>
          <div class="ouds-ps-zh">受控浸漬</div>
        </div>
        <div class="ouds-process-step">
          <div class="ouds-ps-icon" style="width:90px;height:90px;border:2px solid rgba(184,118,42,0.35);background:none;padding:0;overflow:hidden;border-radius:50%;">
            <img src="data:image/webp;插入圖" alt="傳統蒸餾" style="width:100%;height:100%;object-fit:cover;display:block;">
          </div>
          <div class="ouds-ps-num">04</div>
          <div class="ouds-ps-name">Distillation</div>
          <div class="ouds-ps-zh">傳統蒸餾</div>
        </div>
        <div class="ouds-process-step">
          <div class="ouds-ps-icon" style="width:90px;height:90px;border:2px solid rgba(184,118,42,0.35);background:none;padding:0;overflow:hidden;border-radius:50%;">
            <img src="data:image/w插入圖" alt="精油收集" style="width:100%;height:100%;object-fit:cover;display:block;">
          </div>
          <div class="ouds-ps-num">05</div>
          <div class="ouds-ps-name">Condensation<br>Oil Collection</div>
          <div class="ouds-ps-zh">精油收集</div>
        </div>
        <div class="ouds-process-step">
          <div class="ouds-ps-icon" style="width:90px;height:90px;border:2px solid rgba(184,118,42,0.35);background:none;padding:0;overflow:hidden;border-radius:50%;">
            <img src="data:image/web插入圖" alt="過濾純化" style="width:100%;height:100%;object-fit:cover;display:block;">
          </div>
          <div class="ouds-ps-num">06</div>
          <div class="ouds-ps-name">Filtration</div>
          <div class="ouds-ps-zh">過濾純化</div>
        </div>
        <div class="ouds-process-step">
          <div class="ouds-ps-icon" style="width:90px;height:90px;border:2px solid rgba(184,118,42,0.35);background:none;padding:0;overflow:hidden;border-radius:50%;">
            <img src="插入圖" alt="批次封存" style="width:100%;height:100%;object-fit:cover;display:block;">
          </div>
          <div class="ouds-ps-num">07</div>
          <div class="ouds-ps-name">Batch Sealing<br>& Sample Retention</div>
          <div class="ouds-ps-zh">批次封存</div>
        </div>
      </div></div>
    </div>
  </section>

  <!-- 滴滴珍稀 -->
  <section id="ouds-numbers" class="ouds-numbers-section" style="position:relative;background-image:url('data:image/webp;ba插入圖);background-size:cover;background-position:center top;background-attachment:fixed;">
  <div style="position:absolute;inset:0;background:rgba(20,8,2,0.82);"></div>
  <div style="position:relative;z-index:1;">
    <div class="ouds-section ouds-sr">
      <div class="ouds-section-en" style="color:#d4962e !important;font-family:Cinzel,serif;font-size:11px;letter-spacing:0.4em;text-transform:uppercase;margin-bottom:12px;">Every Drop Matters</div>
      <h2 class="ouds-section-title" style="color:#fff !important;font-family:Noto Serif TC,serif;font-size:clamp(20px,2.5vw,28px);font-weight:400;letter-spacing:0.08em;margin-bottom:8px;">滴滴珍稀——沉香之所以神聖</h2>
      <div class="ouds-rule"></div>
      <div class="ouds-numbers-grid" style="display:grid;grid-template-columns:repeat(4,1fr);gap:2px;margin-top:48px;">
        <div class="ouds-number-card" style="background:rgba(255,255,255,0.03) !important;padding:40px 32px;text-align:center;border:1px solid rgba(184,118,42,0.1);"><div class="ouds-number-big" style="font-family:Cinzel,serif !important;color:#c9a84c !important;font-size:clamp(36px,4vw,60px);font-weight:400;line-height:1;margin-bottom:4px;display:block;">15</div><div class="ouds-number-unit" style="font-family:Cormorant Garamond,serif !important;font-size:16px;font-style:italic;color:#b8762a !important;margin-bottom:12px;display:block;">Years</div><div class="ouds-number-desc" style="font-size:12px;color:#a08060 !important;line-height:1.7;letter-spacing:0.05em;display:block;">每株沉香樹所需的<br>最短培育與等待時間</div></div>
        <div class="ouds-number-card" style="background:rgba(255,255,255,0.03) !important;padding:40px 32px;text-align:center;border:1px solid rgba(184,118,42,0.1);"><div class="ouds-number-big" style="font-family:Cinzel,serif !important;color:#c9a84c !important;font-size:clamp(36px,4vw,60px);font-weight:400;line-height:1;margin-bottom:4px;display:block;">1,000</div><div class="ouds-number-unit" style="font-family:Cormorant Garamond,serif !important;font-size:16px;font-style:italic;color:#b8762a !important;margin-bottom:12px;display:block;">Trees</div><div class="ouds-number-desc" style="font-size:12px;color:#a08060 !important;line-height:1.7;letter-spacing:0.05em;display:block;">約90噸原木，方能<br>產出40公斤沉香精油</div></div>
        <div class="ouds-number-card" style="background:rgba(255,255,255,0.03) !important;padding:40px 32px;text-align:center;border:1px solid rgba(184,118,42,0.1);"><div class="ouds-number-big" style="font-family:Cinzel,serif !important;color:#c9a84c !important;font-size:clamp(36px,4vw,60px);font-weight:400;line-height:1;margin-bottom:4px;display:block;">0.04%</div><div class="ouds-number-unit" style="font-family:Cormorant Garamond,serif !important;font-size:16px;font-style:italic;color:#b8762a !important;margin-bottom:12px;display:block;">Yield</div><div class="ouds-number-desc" style="font-size:12px;color:#a08060 !important;line-height:1.7;letter-spacing:0.05em;display:block;">每棵樹的精油<br>最終產出率</div></div>
        <div class="ouds-number-card" style="background:rgba(255,255,255,0.03) !important;padding:40px 32px;text-align:center;border:1px solid rgba(184,118,42,0.1);"><div class="ouds-number-big" style="font-family:Cinzel,serif !important;color:#c9a84c !important;font-size:clamp(36px,4vw,60px);font-weight:400;line-height:1;margin-bottom:4px;display:block;">12</div><div class="ouds-number-unit" style="font-family:Cormorant Garamond,serif !important;font-size:16px;font-style:italic;color:#b8762a !important;margin-bottom:12px;display:block;">Plantations</div><div class="ouds-number-desc" style="font-size:12px;color:#a08060 !important;line-height:1.7;letter-spacing:0.05em;display:block;">南北越12座莊園<br>全程GPS溯源管理</div></div>
      </div>
    </div>
  </div>
  </section>

  <!-- 永續認證 -->
  <section id="ouds-sustain" class="ouds-sustain-section" style="background:#1a2e1a !important;">
    <div class="ouds-section ouds-sr">
      <div class="ouds-section-en" style="color:#adc4ad">Sustainability</div>
      <h2 class="ouds-section-title" style="color:#fff">永續是我們的標準，不是選項</h2>
      <div class="ouds-rule" style="background:#5a9a5a"></div>
      <div class="ouds-sustain-grid">
        <div class="ouds-sustain-card" style="background:rgba(255,255,255,0.04) !important;border:1px solid rgba(255,255,255,0.08) !important;"><div class="ouds-sc-icon" style="font-size:28px;margin-bottom:12px;color:#5a9a5a;font-family:Cinzel,serif;letter-spacing:0.2em;font-size:13px;">✦ NATURE</div><div class="ouds-sc-title" style="color:#adc4ad !important;font-family:Cinzel,serif;font-size:11px;letter-spacing:0.35em;text-transform:uppercase;margin-bottom:16px;display:block;">Nature 自然</div><div class="ouds-sc-items"><div class="ouds-sc-item" style="color:rgba(200,220,200,0.7) !important;font-size:12px;padding:6px 0;border-bottom:1px solid rgba(255,255,255,0.06);display:flex;align-items:center;gap:8px;">零農藥殘留</div><div class="ouds-sc-item" style="color:rgba(200,220,200,0.7) !important;font-size:12px;padding:6px 0;border-bottom:1px solid rgba(255,255,255,0.06);display:flex;align-items:center;gap:8px;">無塑化劑污染（嚴格控管鄰苯二甲酸酯）</div><div class="ouds-sc-item" style="color:rgba(200,220,200,0.7) !important;font-size:12px;padding:6px 0;border-bottom:1px solid rgba(255,255,255,0.06);display:flex;align-items:center;gap:8px;">氣候行動</div><div class="ouds-sc-item" style="color:rgba(200,220,200,0.7) !important;font-size:12px;padding:6px 0;border-bottom:1px solid rgba(255,255,255,0.06);display:flex;align-items:center;gap:8px;">水資源保護 · 生物多樣性</div></div></div>
        <div class="ouds-sustain-card" style="background:rgba(255,255,255,0.04) !important;border:1px solid rgba(255,255,255,0.08) !important;"><div class="ouds-sc-icon" style="font-size:28px;margin-bottom:12px;color:#5a9a5a;font-family:Cinzel,serif;letter-spacing:0.2em;font-size:13px;">✦ CREATION</div><div class="ouds-sc-title" style="color:#adc4ad !important;font-family:Cinzel,serif;font-size:11px;letter-spacing:0.35em;text-transform:uppercase;margin-bottom:16px;display:block;">Creation 創造</div><div class="ouds-sc-items"><div class="ouds-sc-item" style="color:rgba(200,220,200,0.7) !important;font-size:12px;padding:6px 0;border-bottom:1px solid rgba(255,255,255,0.06);display:flex;align-items:center;gap:8px;">永續方式滿足全球市場需求</div><div class="ouds-sc-item" style="color:rgba(200,220,200,0.7) !important;font-size:12px;padding:6px 0;border-bottom:1px solid rgba(255,255,255,0.06);display:flex;align-items:center;gap:8px;">提升使用者身心健康</div><div class="ouds-sc-item" style="color:rgba(200,220,200,0.7) !important;font-size:12px;padding:6px 0;border-bottom:1px solid rgba(255,255,255,0.06);display:flex;align-items:center;gap:8px;">文化敘事轉化為感官體驗</div></div></div>
        <div class="ouds-sustain-card" style="background:rgba(255,255,255,0.04) !important;border:1px solid rgba(255,255,255,0.08) !important;"><div class="ouds-sc-icon" style="font-size:28px;margin-bottom:12px;color:#5a9a5a;font-family:Cinzel,serif;letter-spacing:0.2em;font-size:13px;">✦ PEOPLE</div><div class="ouds-sc-title" style="color:#adc4ad !important;font-family:Cinzel,serif;font-size:11px;letter-spacing:0.35em;text-transform:uppercase;margin-bottom:16px;display:block;">People 人</div><div class="ouds-sc-items"><div class="ouds-sc-item" style="color:rgba(200,220,200,0.7) !important;font-size:12px;padding:6px 0;border-bottom:1px solid rgba(255,255,255,0.06);display:flex;align-items:center;gap:8px;">關懷所有員工的工作環境</div><div class="ouds-sc-item" style="color:rgba(200,220,200,0.7) !important;font-size:12px;padding:6px 0;border-bottom:1px solid rgba(255,255,255,0.06);display:flex;align-items:center;gap:8px;">跨世代工藝知識傳承</div><div class="ouds-sc-item" style="color:rgba(200,220,200,0.7) !important;font-size:12px;padding:6px 0;border-bottom:1px solid rgba(255,255,255,0.06);display:flex;align-items:center;gap:8px;">多元文化協作團隊</div></div></div>
        <div class="ouds-sustain-card" style="background:rgba(255,255,255,0.04) !important;border:1px solid rgba(255,255,255,0.08) !important;"><div class="ouds-sc-icon" style="font-size:28px;margin-bottom:12px;color:#5a9a5a;font-family:Cinzel,serif;letter-spacing:0.2em;font-size:13px;">✦ COMMUNITIES</div><div class="ouds-sc-title" style="color:#adc4ad !important;font-family:Cinzel,serif;font-size:11px;letter-spacing:0.35em;text-transform:uppercase;margin-bottom:16px;display:block;">Communities 社群</div><div class="ouds-sc-items"><div class="ouds-sc-item" style="color:rgba(200,220,200,0.7) !important;font-size:12px;padding:6px 0;border-bottom:1px solid rgba(255,255,255,0.06);display:flex;align-items:center;gap:8px;">本地農家夥伴關係</div><div class="ouds-sc-item" style="color:rgba(200,220,200,0.7) !important;font-size:12px;padding:6px 0;border-bottom:1px solid rgba(255,255,255,0.06);display:flex;align-items:center;gap:8px;">KPI 可量化績效管理</div><div class="ouds-sc-item" style="color:rgba(200,220,200,0.7) !important;font-size:12px;padding:6px 0;border-bottom:1px solid rgba(255,255,255,0.06);display:flex;align-items:center;gap:8px;">Kaizen 持續改善機制</div><div class="ouds-sc-item" style="color:rgba(200,220,200,0.7) !important;font-size:12px;padding:6px 0;border-bottom:1px solid rgba(255,255,255,0.06);display:flex;align-items:center;gap:8px;">長期共投資、發展聯合事業</div></div></div>
      </div>
    </div>
  </section>

  <!-- 聯絡採購 -->
  <section id="ouds-contact" class="ouds-cta-section" style="background:var(--oud-cream) !important;">
    <div class="ouds-section ouds-sr" style="padding-top:0;padding-bottom:0">
      <div class="ouds-cta-inner" style="background:#1a0e07 !important;display:grid;grid-template-columns:1fr 1fr;">
        <div class="ouds-cta-col" style="padding:60px 48px;border-right:1px solid rgba(184,118,42,0.2);">
          <h2 class="ouds-cta-title" style="color:#fff !important;font-family:Noto Serif TC,serif;font-size:22px;line-height:1.5;margin-bottom:16px;">對越南沉香有興趣？<br>歡迎洽詢合作採購</h2>
          <p class="ouds-cta-desc" style="color:#a08060 !important;font-size:14px;line-height:1.9;margin-bottom:32px;">無論您是調香師、香水品牌、或精油採購商，Dhyana Ouds 提供樣品寄送、產品規格諮詢，以及完整的批次溯源文件。根本芳療台灣辦事處提供即時中文服務支援。</p>
          <a href="/cdn-cgi/l/email-protection#ec9f8d80899fac8884958d828dc28f8381c2989b" class="ouds-cta-btn" style="background:#b8762a !important;color:#fff !important;text-decoration:none;display:inline-block;padding:14px 32px;font-size:12px;letter-spacing:0.2em;text-transform:uppercase;">寄送洽詢信件</a>
        </div>
        <div class="ouds-cta-col" style="padding:60px 48px;">
          <ul class="ouds-contact-list" style="list-style:none;display:flex;flex-direction:column;gap:16px;" style="list-style:none;">
            <li style="display:flex;gap:16px;align-items:flex-start;font-size:13px;color:#a08060 !important;line-height:1.6;"><strong style="color:#b8762a !important;font-family:Cinzel,serif;font-size:9px;letter-spacing:0.3em;text-transform:uppercase;width:60px;flex-shrink:0;padding-top:2px;font-weight:400;">Email</strong><a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="295a48454c5a694d4150484748074a4644075d5e">[email&#160;protected]</a></li>
            <li style="display:flex;gap:16px;align-items:flex-start;font-size:13px;color:#a08060 !important;line-height:1.6;"><strong style="color:#b8762a !important;font-family:Cinzel,serif;font-size:9px;letter-spacing:0.3em;text-transform:uppercase;width:60px;flex-shrink:0;padding-top:2px;font-weight:400;">Tel</strong>+886-7-3596555（台灣辦事處）</li>
            <li style="display:flex;gap:16px;align-items:flex-start;font-size:13px;color:#a08060 !important;line-height:1.6;"><strong style="color:#b8762a !important;font-family:Cinzel,serif;font-size:9px;letter-spacing:0.3em;text-transform:uppercase;width:60px;flex-shrink:0;padding-top:2px;font-weight:400;">地址</strong>高雄市左營區文學路350號</li>
            <li style="display:flex;gap:16px;align-items:flex-start;font-size:13px;color:#a08060 !important;line-height:1.6;"><strong style="color:#b8762a !important;font-family:Cinzel,serif;font-size:9px;letter-spacing:0.3em;text-transform:uppercase;width:60px;flex-shrink:0;padding-top:2px;font-weight:400;">Hours</strong>Mon–Sat 09:00–18:00（GMT+8）</li>
            <li style="display:flex;gap:16px;align-items:flex-start;font-size:13px;color:#a08060 !important;line-height:1.6;"><strong style="color:#b8762a !important;font-family:Cinzel,serif;font-size:9px;letter-spacing:0.3em;text-transform:uppercase;width:60px;flex-shrink:0;padding-top:2px;font-weight:400;">Offices</strong>台灣 · 里昂 · 河內 · 胡志明市 · 杜拜</li>
            <li style="display:flex;gap:16px;align-items:flex-start;font-size:13px;color:#a08060 !important;line-height:1.6;"><strong style="color:#b8762a !important;font-family:Cinzel,serif;font-size:9px;letter-spacing:0.3em;text-transform:uppercase;width:60px;flex-shrink:0;padding-top:2px;font-weight:400;">Cert</strong>UEBT 生物貿易倫理聯盟認證會員</li>
          </ul>
        </div>
      </div>
    </div>
  </section>

</div><!-- /ouds-page-body -->
</div><!-- /ouds-wrap -->

<script>
(function(){
  // ── Tab 切換 ──
  window.oudsTab = function(btn, id) {
    document.querySelectorAll('.ouds-tab').forEach(function(t){ t.classList.remove('ouds-active'); });
    btn.classList.add('ouds-active');
    var el = document.getElementById(id);
    if (el) {
      var offset = el.getBoundingClientRect().top + window.scrollY - 120;
      window.scrollTo({ top: offset, behavior: 'smooth' });
    }
  };

  // ── Tab 高亮（隨捲動） ──
  var sids = ['ouds-story','ouds-grand-cru','ouds-terroir','ouds-process','ouds-numbers','ouds-sustain','ouds-contact'];
  var tabs = document.querySelectorAll('.ouds-tab');
  window.addEventListener('scroll', function(){
    var cur = '';
    sids.forEach(function(id){
      var el = document.getElementById(id);
      if (el && window.scrollY >= el.offsetTop - 140) cur = id;
    });
    tabs.forEach(function(tab){
      tab.classList.remove('ouds-active');
      var oc = tab.getAttribute('onclick') || '';
      if (cur && oc.indexOf(cur) > -1) tab.classList.add('ouds-active');
    });
  }, { passive: true });

  // ── 自訂游標 ──
  var dot  = document.getElementById('oudsCursorDot');
  var ring = document.getElementById('oudsCursorRing');
  if (dot && ring) {
    var mx = window.innerWidth / 2;
    var my = window.innerHeight / 2;
    var rx = mx, ry = my;

    // 直接用 transform 定位，避免 top/left 被覆寫
    function moveDot(x, y) {
      dot.style.transform = 'translate(' + (x - 5) + 'px, ' + (y - 5) + 'px)';
    }
    function moveRing(x, y) {
      ring.style.transform = 'translate(' + (x - 19) + 'px, ' + (y - 19) + 'px)';
    }

    moveDot(mx, my);
    moveRing(rx, ry);

    document.addEventListener('mousemove', function(e) {
      mx = e.clientX;
      my = e.clientY;
      moveDot(mx, my);
    }, { passive: true });

    // Ring 緩動跟隨
    (function lerpRing() {
      rx += (mx - rx) * 0.13;
      ry += (my - ry) * 0.13;
      moveRing(rx, ry);
      requestAnimationFrame(lerpRing);
    })();

    // Hover 效果：連結、按鈕、產品卡片
    document.querySelectorAll('.ouds-wrap a, .ouds-wrap button, .ouds-product-card, .ouds-tab').forEach(function(el) {
      el.addEventListener('mouseenter', function() { ring.classList.add('ouds-hovering'); });
      el.addEventListener('mouseleave', function() { ring.classList.remove('ouds-hovering'); });
    });

    // 點擊效果
    document.addEventListener('mousedown', function() {
      dot.classList.add('ouds-clicking');
      ring.classList.add('ouds-hovering');
    });
    document.addEventListener('mouseup', function() {
      dot.classList.remove('ouds-clicking');
      ring.classList.remove('ouds-hovering');
    });

    // 離開/進入視窗
    document.addEventListener('mouseleave', function() {
      dot.style.opacity = '0';
      ring.style.opacity = '0';
    });
    document.addEventListener('mouseenter', function() {
      dot.style.opacity = '1';
      ring.style.opacity = '1';
    });
  }
})();
</script>
