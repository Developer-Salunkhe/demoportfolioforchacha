<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
<title>Ashutosh Salunkhe — Video Editor & Videographer</title>
<meta name="description" content="Portfolio of Ashutosh Salunkhe, video editor & videographer specializing in Social Media, Commercial and Documentary content.">
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Fraunces:ital,opsz,wght@0,9..144,400;0,9..144,500;0,9..144,600;1,9..144,500&family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">

<style>
  :root{
    /* ============ THEME COLORS ============ */
    --bg-0: #0c0a10;
    --bg-1: #15111d;
    --bg-2: #1e1830;
    --line: rgba(232, 221, 255, 0.10);

    --text-hi: #f6f3fb;
    --text-mid: #c9c2d9;
    --text-low: #8d84a3;

    --accent: #d9a441;
    --accent-soft: #f0cd83;
    --accent-2: #8b6bf0;

    --glow: radial-gradient(60% 50% at 50% 30%, rgba(139,107,240,0.28), transparent 70%);

    --radius-lg: 28px;
    --radius-md: 18px;
    --radius-sm: 12px;

    --maxw: 1120px;
    --pad: clamp(20px, 5vw, 64px);
  }

  *{ box-sizing: border-box; }
  html{ scroll-behavior: smooth; }
  body{
    margin:0;
    background: var(--bg-0);
    color: var(--text-mid);
    font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
    -webkit-font-smoothing: antialiased;
    overflow-x: hidden;
  }
  h1,h2,h3{
    font-family: 'Fraunces', Georgia, serif;
    color: var(--text-hi);
    margin: 0;
    line-height: 1.08;
    letter-spacing: -0.01em;
  }
  h4{
    font-family:'Inter', sans-serif;
    color: var(--text-hi);
    margin:0;
  }
  em{
    font-style: italic;
    color: var(--accent-soft);
  }
  a{ color: inherit; text-decoration: none; }
  img{ max-width:100%; display:block; }
  section{ position: relative; }
  .wrap{
    max-width: var(--maxw);
    margin: 0 auto;
    padding: 0 var(--pad);
  }
  .eyebrow{
    display:inline-flex;
    align-items:center;
    gap:8px;
    font-size: 13px;
    letter-spacing: .04em;
    color: var(--text-low);
    background: var(--bg-2);
    border: 1px solid var(--line);
    padding: 6px 14px;
    border-radius: 999px;
  }
  ::selection{ background: var(--accent); color: #1a1420; }
  :focus-visible{ outline: 2px solid var(--accent-soft); outline-offset: 3px; }

  /* ---------------- NAV ---------------- */
  header{
    position: fixed;
    top: 0; left: 0; right: 0;
    z-index: 100;
    padding: 18px var(--pad);
    display:flex;
    align-items:center;
    justify-content:space-between;
    backdrop-filter: blur(14px);
    background: linear-gradient(to bottom, rgba(12,10,16,0.85), rgba(12,10,16,0));
  }
  .logo{
    font-family:'Fraunces', serif;
    font-size: 19px;
    color: var(--text-hi);
    font-weight: 600;
  }
  nav.links{
    display:flex;
    align-items:center;
    gap: 6px;
    background: rgba(30,24,48,0.6);
    border: 1px solid var(--line);
    padding: 6px;
    border-radius: 999px;
  }
  nav.links a{
    padding: 9px 18px;
    border-radius: 999px;
    font-size: 14.5px;
    color: var(--text-mid);
    transition: background .2s ease, color .2s ease;
    white-space: nowrap;
  }
  nav.links a:hover{ color: var(--text-hi); background: rgba(255,255,255,0.06); }
  nav.links a.cta{
    background: var(--accent);
    color: #201607;
    font-weight: 600;
  }
  nav.links a.cta:hover{ background: var(--accent-soft); }

  .menu-btn{
    display:none;
    width: 42px; height: 42px;
    border-radius: 50%;
    border: 1px solid var(--line);
    background: rgba(30,24,48,0.7);
    color: var(--text-hi);
    align-items:center; justify-content:center;
    font-size: 18px;
    cursor:pointer;
  }

  .mobile-panel{
    position: fixed;
    top: 0; right: 0;
    height: 100dvh;
    width: min(78vw, 320px);
    background: var(--bg-1);
    border-left: 1px solid var(--line);
    z-index: 200;
    transform: translateX(100%);
    transition: transform .35s cubic-bezier(.65,0,.35,1);
    padding: 24px;
    display:flex;
    flex-direction:column;
    gap: 6px;
    overflow-y:auto;
  }
  .mobile-panel.open{ transform: translateX(0); }
  .mobile-panel a{
    padding: 16px 10px;
    font-size: 17px;
    border-bottom: 1px solid var(--line);
    color: var(--text-mid);
  }
  .mobile-panel a.cta{
    margin-top: 14px;
    text-align:center;
    background: var(--accent);
    color:#201607;
    border-radius: 12px;
    border-bottom:none;
    font-weight:600;
  }
  .scrim{
    position: fixed; inset:0;
    background: rgba(0,0,0,0.55);
    z-index: 150;
    opacity:0; pointer-events:none;
    transition: opacity .3s ease;
  }
  .scrim.show{ opacity:1; pointer-events:auto; }

  /* ---------------- HERO ---------------- */
  .hero{
    padding: clamp(120px,20vw,180px) var(--pad) 80px;
    text-align:center;
    background: var(--glow), var(--bg-0);
  }
  .hero h1{
    font-size: clamp(38px, 7vw, 68px);
    font-weight: 500;
  }
  .hero h1 span.hi{ color: var(--text-hi); }
  .hero p.lead{
    max-width: 620px;
    margin: 22px auto 0;
    font-size: clamp(15px, 2vw, 18px);
    color: var(--text-mid);
    line-height: 1.65;
  }
  .hero .years{
    margin-top: 20px;
    font-size: 15px;
    color: var(--text-low);
  }
  .avatars{
    margin: 46px auto 0;
    display:flex;
    align-items:center;
    justify-content:center;
    gap: 10px;
    flex-wrap:wrap;
  }
  .avatars .stack {
  display: flex;
  align-items: center;
}

.avatars .stack img {
  width: 56px;
  height: 56px;
  border-radius: 50%;
  object-fit: cover;
  border: 2px solid var(--bg-0);
  margin-left: -10px;
  background: var(--bg-2);
  transition: transform 0.25s ease;
}

.avatars .stack img:first-child {
  margin-left: 0;
}

.avatars .stack img:hover {
  transform: translateY(-4px);
  z-index: 2;
}

  /* ---------------- SECTION HEAD ---------------- */
  .section-head{
    text-align:center;
    margin: 0 0 48px;
  }
  .section-head h2{
    font-size: clamp(30px, 5vw, 46px);
    font-weight: 500;
    margin-top: 16px;
  }
  .section-head p{
    max-width: 560px;
    margin: 16px auto 0;
    color: var(--text-low);
    font-size: 15.5px;
    line-height: 1.6;
  }
  .subhead{
    display:flex;
    align-items:center;
    gap: 14px;
    margin: 64px 0 26px;
  }
  .subhead:first-of-type{ margin-top: 0; }
  .subhead h3{
    font-size: clamp(20px, 3vw, 26px);
    font-weight: 500;
    white-space: nowrap;
  }
  .subhead .rule{
    height:1px;
    width:100%;
    background: var(--line);
  }

  /* ---------------- ABOUT ---------------- */
  .about{ padding: 40px var(--pad) 100px; }
  .about-card{
    background: linear-gradient(160deg, var(--bg-2), var(--bg-1));
    border: 1px solid var(--line);
    border-radius: var(--radius-lg);
    padding: clamp(28px, 5vw, 56px);
    display:grid;
    grid-template-columns: 1.1fr 0.9fr;
    gap: 48px;
    align-items:center;
  }
  .about h2{ font-size: clamp(26px,4vw,34px); font-weight:500; margin-bottom: 18px; }
  .about p{ margin: 0 0 14px; font-size: 15.5px; line-height: 1.7; color: var(--text-mid); }
  .about strong{ color: var(--text-hi); }
 #about-photo {
  width: 100%;
  max-width: 500px;
  margin: 0 auto;
  border-radius: var(--radius-md);
  overflow: hidden;
  border: 1px solid var(--line);
  background: var(--bg-2);
}

#about-photo img {
  display: block;
  width: 100%;
  height: auto;
  max-width: 100%;
  object-fit: contain;
}

  /* ---------------- WORK / PROJECTS ---------------- */
  .work{ padding: 40px var(--pad) 100px; }

  /* Long-form video grid (real YouTube embeds + external link cards) */
  .video-grid{
    display:grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 22px;
  }
  .video-card{
    background: var(--bg-2);
    border: 1px solid var(--line);
    border-radius: var(--radius-md);
    overflow:hidden;
    transition: transform .3s ease, border-color .3s ease;
  }
  .video-card:hover{ transform: translateY(-6px); border-color: rgba(217,164,65,0.4); }
  .video-frame-wrap{
    position:relative;
    aspect-ratio: 16/9;
    background: #000;
  }
  .video-frame-wrap{
  position:relative;
  aspect-ratio: 16/9;   /* <- this is what gives it height */
  background: #000;
}
.video-frame-wrap iframe{
  position:absolute; inset:0;
  width:100%; height:100%;
  border:0;
}
  .video-info{ padding: 16px 20px 20px; }
  .video-info h4{ font-size: 15.5px; font-weight:600; }
  .video-info .platform{ margin: 8px 0 0; font-size: 12.5px; color: var(--text-low); }

  /* External (Instagram / Drive) link-out cards */
  .link-card{
    background: var(--bg-2);
    border: 1px solid var(--line);
    border-radius: var(--radius-md);
    overflow:hidden;
    display:flex;
    flex-direction:column;
    transition: transform .3s ease, border-color .3s ease;
  }
  .link-card:hover{ transform: translateY(-6px); border-color: rgba(217,164,65,0.4); }
  .link-thumb{
    aspect-ratio: 16/9;
    background: linear-gradient(140deg, var(--accent-2) 0%, var(--bg-2) 70%);
    display:flex; align-items:center; justify-content:center;
    flex-direction:column;
    gap:8px;
  }
  .link-thumb .ic{ font-size: 26px; }
  .link-thumb .plat-label{ font-size:12px; letter-spacing:.05em; color: rgba(255,255,255,0.85); text-transform:uppercase; }
  .link-card a.watch-btn{
    display:block;
    text-align:center;
    padding: 16px 20px 20px;
  }
  .link-card .video-info h4{ padding: 0 20px; margin-top:16px; }
  .link-card .watch-btn .go{
    display:inline-block;
    margin-top:12px;
    padding: 9px 18px;
    border-radius: 999px;
    background: var(--accent);
    color: #201607;
    font-weight:600;
    font-size: 13px;
  }
  .link-card .watch-btn:hover .go{ background: var(--accent-soft); }

  /* Shorts / reels grid — vertical cards */
  .shorts-grid{
    display:grid;
    grid-template-columns: repeat(auto-fill, minmax(180px, 1fr));
    gap: 20px;
  }
  .short-card{
    background: var(--bg-2);
    border: 1px solid var(--line);
    border-radius: var(--radius-md);
    overflow:hidden;
    transition: transform .3s ease, border-color .3s ease;
  }
  .short-card:hover{ transform: translateY(-6px); border-color: rgba(217,164,65,0.4); }
  .short-frame-wrap{
    position:relative;
    aspect-ratio: 9/16;
    background:#000;
  }
  .short-frame-wrap iframe{
    position:absolute; inset:0;
    width:100%; height:100%;
    border:0;
  }
  .short-link-thumb{
    aspect-ratio: 9/16;
    background: linear-gradient(150deg, var(--accent-2) 0%, var(--bg-2) 75%);
    display:flex; flex-direction:column; align-items:center; justify-content:center; gap:10px;
  }
  .short-link-thumb .ic{ font-size:22px; }
  .short-link-thumb .plat-label{ font-size:11px; letter-spacing:.05em; color:rgba(255,255,255,0.85); text-transform:uppercase; }
  .short-info{ padding: 12px 14px 16px; text-align:center; }
  .short-info h4{ font-size: 13.5px; font-weight:600; }
  .short-info a.go{
    display:inline-block;
    margin-top:8px;
    padding: 6px 14px;
    border-radius: 999px;
    background: var(--accent);
    color:#201607;
    font-weight:600;
    font-size: 11.5px;
  }
  .short-info a.go:hover{ background: var(--accent-soft); }

  /* Channels table */
  .channels-wrap{
    overflow-x:auto;
    border: 1px solid var(--line);
    border-radius: var(--radius-md);
    background: var(--bg-2);
  }
  table.channels-table{
    width:100%;
    border-collapse: collapse;
    min-width: 560px;
  }
  table.channels-table th{
    text-align:left;
    background: rgba(217,164,65,0.12);
    color: var(--accent-soft);
    font-size: 13px;
    letter-spacing:.03em;
    text-transform:uppercase;
    padding: 16px 20px;
    border-bottom: 1px solid var(--line);
  }
  table.channels-table td{
    padding: 16px 20px;
    font-size: 14.5px;
    color: var(--text-mid);
    border-bottom: 1px solid var(--line);
  }
  table.channels-table tr:last-child td{ border-bottom:none; }
  table.channels-table td a{ color: var(--accent-soft); word-break: break-word; }
  table.channels-table td a:hover{ text-decoration: underline; }

  /* ---------------- EXPERIENCE ---------------- */
  .experience{ padding: 40px var(--pad) 100px; }
  .timeline{
    border-top: 1px solid var(--line);
  }
  .timeline-row{
    display:flex;
    justify-content:space-between;
    align-items:baseline;
    gap: 20px;
    padding: 26px 4px;
    border-bottom: 1px solid var(--line);
  }
  .timeline-row h3{
    font-size: clamp(17px, 2.4vw, 21px);
    font-weight: 500;
    color: var(--text-hi);
  }
  .timeline-row .meta{ text-align:right; flex-shrink:0; }
  .timeline-row .meta .co{ color: var(--accent-soft); font-size: 14.5px; font-weight:600; }
  .timeline-row .meta .dt{ color: var(--text-low); font-size: 13px; margin-top:2px; }

  /* ---------------- TESTIMONIALS ---------------- */
  .testimonials{ padding: 40px var(--pad) 100px; }
  .grid-testimonials{
    display:grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 20px;
  }
  .t-card{
    background: linear-gradient(160deg, rgba(139,107,240,0.10), var(--bg-2));
    border: 1px solid var(--line);
    border-radius: var(--radius-md);
    padding: 26px 24px;
    display:flex;
    flex-direction:column;
  }
  .stars{ color: var(--accent); font-size: 14px; letter-spacing:2px; }
  .t-card p.quote{
    margin: 16px 0 22px;
    font-size: 14.5px;
    line-height: 1.7;
    color: var(--text-mid);
    white-space: pre-line;
  }
  .t-person{ display:flex; align-items:center; gap: 12px; margin-top:auto; }
  .t-avatar{
    width: 38px; height:38px; border-radius:50%;
    background: linear-gradient(135deg, var(--accent), var(--accent-2));
    flex-shrink:0;
    display:flex; align-items:center; justify-content:center;
    color:#201607; font-weight:700; font-size:14px;
  }
  .t-person .name{ color: var(--text-hi); font-size: 14.5px; font-weight:600; }
  .t-person .role{ color: var(--text-low); font-size: 12.5px; }

  /* ---------------- CONTACT ---------------- */
  .contact{
    padding: 60px var(--pad) 90px;
    text-align:center;
    background: var(--glow), var(--bg-1);
    border-top: 1px solid var(--line);
  }
  .contact h2{
    font-size: clamp(32px, 6vw, 54px);
    font-weight:500;
  }
  .contact p{
    max-width: 480px;
    margin: 18px auto 0;
    color: var(--text-low);
    font-size: 15.5px;
  }
  .btn-primary{
    display:inline-block;
    margin-top: 30px;
    background: linear-gradient(135deg, var(--accent-soft), var(--accent));
    color: #201607;
    font-weight: 700;
    padding: 15px 34px;
    border-radius: 999px;
    font-size: 15.5px;
    box-shadow: 0 10px 30px -8px rgba(217,164,65,0.55);
    transition: transform .2s ease, box-shadow .2s ease;
  }
  .btn-primary:hover{ transform: translateY(-2px); box-shadow: 0 14px 34px -8px rgba(217,164,65,0.7); }

  footer{
    padding: 30px var(--pad) 40px;
    display:flex;
    justify-content:center;
    gap: 28px;
    color: var(--text-low);
    font-size: 14px;
  }
  footer a:hover{ color: var(--text-hi); }

  /* ---------------- RESPONSIVE ---------------- */
 @media (max-width: 900px) {
  .about-card {
    grid-template-columns: 1fr;
  }

  #about-photo {
    order: -1;
    width: 100%;
    max-width: 500px;
    margin: 0 auto;
  }
}

  @media (max-width: 760px){
    nav.links{ display:none; }
    .menu-btn{ display:flex; }
    .video-grid{ grid-template-columns: 1fr; }
    .shorts-grid{ grid-template-columns: repeat(auto-fill, minmax(140px, 1fr)); }
    .timeline-row{ flex-direction:column; align-items:flex-start; gap:6px; }
    .timeline-row .meta{ text-align:left; }

    /* Channels table -> stacked cards on mobile */
    .channels-wrap{ border:none; background:none; overflow-x:visible; }
    table.channels-table{ min-width: 0; display:block; }
    table.channels-table thead{ display:none; }
    table.channels-table tbody{ display:block; }
    table.channels-table tr{
      display:block;
      background: var(--bg-2);
      border: 1px solid var(--line);
      border-radius: var(--radius-md);
      padding: 6px 4px;
      margin-bottom: 16px;
    }
    table.channels-table tr:last-child{ margin-bottom:0; }
    table.channels-table td{
      display:flex;
      justify-content:space-between;
      align-items:center;
      gap: 16px;
      padding: 12px 16px;
      border-bottom: 1px solid var(--line);
      text-align:right;
    }
    table.channels-table tr td:last-child{ border-bottom:none; }
    table.channels-table td::before{
      content: attr(data-label);
      flex-shrink:0;
      text-align:left;
      font-size: 12px;
      letter-spacing:.03em;
      text-transform:uppercase;
      color: var(--accent-soft);
      font-weight:600;
    }
  }

  @media (max-width: 420px){
    :root{ --pad: 16px; }
    .hero{ padding-top: 110px; }
    .about-card{ padding: 22px; border-radius: var(--radius-md); }
  }

  @media (min-width: 1440px){
    .hero h1{ font-size: 74px; }
  }

  @media (prefers-reduced-motion: reduce){
    html{ scroll-behavior:auto; }
    *{ transition:none !important; animation:none !important; }
  }
</style>
</head>
<body>

<header>
  <div class="logo">Ashutosh Salunkhe</div>
  <nav class="links">
    <a href="#work">Work</a>
    <a href="#experience">Experience</a>
    <a href="#testimonials">Testimonials</a>
    <a href="#contact" class="cta">Contact</a>
  </nav>
  <button class="menu-btn" id="menuBtn" aria-label="Open menu">☰</button>
</header>

<div class="scrim" id="scrim"></div>
<div class="mobile-panel" id="mobilePanel">
  <a href="#work">Work</a>
  <a href="#experience">Experience</a>
  <a href="#testimonials">Testimonials</a>
  <a href="#contact" class="cta">Contact</a>
</div>

<section class="hero">
  <div class="wrap">
    <h1>Hey,<br><span class="hi">I'm Ashutosh Salunkhe</span></h1>
    <p class="lead">Creative and detail-oriented video professional skilled in content production, visual storytelling, digital media, YouTube, social media reels, brand campaigns, and AI-assisted video workflows. Specializing in Social Media, Commercial and Documentary editing & videography.</p>
    <p class="years">7+ Years of experience · Since 2019</p>
    <div class="avatars">
  <div class="stack">

    <img src="Img/IndianFarmer.jpg" alt="Indian Farmer">
    <img src="Img/DeshKaKisan.jpg" alt="Desh Ki Jaan Hamare Kisan">
    <img src="Img/IntCoach.jpg" alt="Interior Coach">
    <img src="Img/RushLane.jpg" alt="Rushlane">
   

  </div>

  <span class="label">5+ YouTube channels & brands worked with</span>
</div>
  </div>
</section>

<section class="about" id="about">
  <div class="wrap about-card">
    <div>
      <h2>About Me :</h2>
      <p>I'm a video editor and videographer with <strong>7+ years of experience</strong> (since June 2019), specializing in Social Media, Commercial, and Documentary content.</p>
      <p>I started my journey with the YouTube channel <strong>Indian Farmer</strong> (Jun 2019 – Oct 2024), where I built deep, hands-on expertise in farming and rural content — shooting and editing on location for over five years. I went on to work as Video Editor & Videographer for <strong>Desh Ki Jaan Hamare Kisan</strong> (Apr – Dec 2025), and I'm currently full-time with <strong>Interior Coach</strong> (Jan 2026 – Present).</p>
      <p>Alongside my full-time role, I freelance for automotive publication <strong>Rushlane</strong> (since Oct 2024) and <strong>Andizzymag</strong> (since Sep 2025) — covering everything from EV and luxury-car test drives to interior design, real estate, construction, and brand campaigns across YouTube, Instagram, and Shorts/Reels.</p>
      <p>Clients consistently point to the same things: reliable delivery, clear communication, and shooting + editing quality that's helped their channels land better brand deals and get noticed in the industry.</p>
    </div>
    <div id="about-photo">
      <img src="Img/Ashutosh.png" alt="Ashutosh Salunkhe">
    </div>
  </div>
</section>

<section class="work" id="work">
  <div class="wrap">
    <div class="section-head">
      <span class="eyebrow">Portfolio</span>
      <h2>Selected Work</h2>
      <p>A selection of real long-form videos, shorts/reels, and the YouTube channels I've worked with.</p>
    </div>

    <!-- ===== LONG-FORM VIDEOS ===== -->
    <div class="subhead"><h3>Long-form Videos</h3><div class="rule"></div></div>
    <div class="video-grid">

     <div class="video-card">
  <div class="video-frame-wrap">
    <iframe width="560" height="315" src="https://www.youtube.com/embed/4sO7nY39hgc?si=biypcHEw6d8Mo_Mz" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
  </div>

  <div class="video-info">
    <h4>Avoid Lighting Mistakes — Interior Edit</h4>
    <p class="platform">YouTube · Long-form</p>
  </div>
</div>

      <div class="video-card">
        <div class="video-frame-wrap">
          <iframe src="https://www.youtube.com/embed/cx344K0VOFw?start=64" title="Driving Next Gen Honda Cars — EVs and Hybrids" loading="lazy" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
        </div>
        <div class="video-info">
          <h4>Driving Next-Gen Honda Cars — EVs & Hybrids</h4>
          <p class="platform">YouTube · Automobile</p>
        </div>
      </div>

      <a class="link-card" href="https://www.instagram.com/reel/DSGrqdQCCOD/?utm_source=ig_web_copy_link&igsh=NTc4MTIwNjQ2YQ==" target="_blank" rel="noopener">
        <div class="link-thumb">
          <div class="ic">🔗</div>
          <div class="plat-label">Instagram</div>
        </div>
        <h4>Essay Invitation 2025 — Shethi Games</h4>
        <div class="watch-btn"><span class="go">Watch on Instagram ↗</span></div>
      </a>

      <div class="video-card">
        <div class="video-frame-wrap">
          <iframe src="https://www.youtube.com/embed/KRtywHRX4Gg" title="India's Most Expensive Tractor" loading="lazy" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
        </div>
        <div class="video-info">
          <h4>India's Most Expensive Tractor (इंडिया का सबसे महंगा ट्रैक्टर)</h4>
          <p class="platform">YouTube · Farming</p>
        </div>
      </div>

      <a class="link-card" href="https://drive.google.com/file/d/1NL97-8r7SdT0fSo_ndFV7d2kQKZhynWb/view?usp=sharing" target="_blank" rel="noopener">
        <div class="link-thumb">
          <div class="ic">🔗</div>
          <div class="plat-label">Google Drive</div>
        </div>
        <h4>Porsche India — 4 Years</h4>
        <div class="watch-btn"><span class="go">Watch on Drive ↗</span></div>
      </a>

    </div>

    <!-- ===== SHORTS / REELS ===== -->
    <div class="subhead"><h3>Shorts / Reels</h3><div class="rule"></div></div>
    <div class="shorts-grid">

      <a class="short-card" href="https://www.instagram.com/reel/DPN7rJFERGP/?utm_source=ig_web_copy_link&igsh=NTc4MTIwNjQ2YQ==" target="_blank" rel="noopener">
        <div class="short-link-thumb">
          <div class="ic">🔗</div>
          <div class="plat-label">Instagram</div>
        </div>
        <div class="short-info">
          <h4>Music / Pop</h4>
          <span class="go">Watch ↗</span>
        </div>
      </a>

      <a class="short-card" href="https://www.instagram.com/reel/DOfP6n9kgW0/?utm_source=ig_web_copy_link&igsh=NTc4MTIwNjQ2YQ==" target="_blank" rel="noopener">
        <div class="short-link-thumb">
          <div class="ic">🔗</div>
          <div class="plat-label">Instagram</div>
        </div>
        <div class="short-info">
          <h4>Automobile</h4>
          <span class="go">Watch ↗</span>
        </div>
      </a>

      <div class="short-card">
        <div class="short-frame-wrap">
          <iframe src="https://www.youtube.com/embed/cokY9I5V62s" title="Construction Short" loading="lazy" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
        </div>
        <div class="short-info">
          <h4>Construction</h4>
        </div>
      </div>

      <div class="short-card">
        <div class="short-frame-wrap">
          <iframe src="https://www.youtube.com/embed/ZO1cEqn-Lps" title="Interior Short" loading="lazy" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
        </div>
        <div class="short-info">
          <h4>Interior</h4>
        </div>
      </div>

      <a class="short-card" href="https://drive.google.com/file/d/1O9yxgpHrxKAdu" target="_blank" rel="noopener">
        <div class="short-link-thumb">
          <div class="ic">🔗</div>
          <div class="plat-label">Google Drive</div>
        </div>
        <div class="short-info">
          <h4>Real Estate</h4>
          <span class="go">Watch ↗</span>
        </div>
      </a>

      <a class="short-card" href="https://www.instagram.com/reel/C3EojSEvoVI/?utm_source=ig_web_copy_link&igsh=NTc4MTIwNjQ2YQ==" target="_blank" rel="noopener">
        <div class="short-link-thumb">
          <div class="ic">🔗</div>
          <div class="plat-label">Instagram</div>
        </div>
        <div class="short-info">
          <h4>Farming</h4>
          <span class="go">Watch ↗</span>
        </div>
      </a>

    </div>

    <!-- ===== YOUTUBE CHANNELS WORKED WITH ===== -->
    <div class="subhead"><h3>YouTube Channels Worked With</h3><div class="rule"></div></div>
    <div class="channels-wrap">
      <table class="channels-table">
        <thead>
          <tr><th>Channel Name</th><th>Duration</th><th>Link</th></tr>
        </thead>
        <tbody>
          <tr>
            <td data-label="Channel Name">Indian Farmer</td>
            <td data-label="Duration">06/2019 – 10/2024</td>
            <td data-label="Link"><a href="https://www.youtube.com/@IndianFarmer" target="_blank" rel="noopener">youtube.com/@IndianFarmer</a></td>
          </tr>
          <tr>
            <td data-label="Channel Name">Desh Ki Jaan Hamare Kisan (DKJHK)</td>
            <td data-label="Duration">04/2025 – 12/2025</td>
            <td data-label="Link"><a href="https://www.youtube.com/@DeshKiJaanHamarekisan/" target="_blank" rel="noopener">youtube.com/@DeshKiJaanHamarekisan</a></td>
          </tr>
          <tr>
            <td data-label="Channel Name">Interior Coach</td>
            <td data-label="Duration">01/2026 – Present</td>
            <td data-label="Link"><a href="https://www.youtube.com/@interiorcoach/videos" target="_blank" rel="noopener">youtube.com/@interiorcoach</a></td>
          </tr>
          <tr>
            <td data-label="Channel Name">Rushlane (Freelancing)</td>
            <td data-label="Duration">10/2024 – Present</td>
            <td data-label="Link"><a href="https://www.youtube.com/@RushLaneNews/featured" target="_blank" rel="noopener">youtube.com/@RushLaneNews</a></td>
          </tr>
          <tr>
            <td data-label="Channel Name">Andizzymag (Freelancing)</td>
            <td data-label="Duration">09/2025 – Present</td>
            <td data-label="Link"><a href="https://www.instagram.com/andizzymag/" target="_blank" rel="noopener">instagram.com/andizzymag</a></td>
          </tr>
        </tbody>
      </table>
    </div>

  </div>
</section>

<section class="experience" id="experience">
  <div class="wrap">
    <div class="section-head" style="text-align:left; margin-bottom:20px;">
      <h2>Experience</h2>
    </div>
    <div class="timeline">
      <div class="timeline-row">
        <h3>Video Editor & Videographer — Interior Coach</h3>
        <div class="meta"><div class="co">Interior Coach</div><div class="dt">Jan 2026 – Present</div></div>
      </div>
      <div class="timeline-row">
        <h3>Freelance Video Editor — Andizzymag</h3>
        <div class="meta"><div class="co">Andizzymag</div><div class="dt">Sep 2025 – Present</div></div>
      </div>
      <div class="timeline-row">
        <h3>Freelance Video Editor — Rushlane</h3>
        <div class="meta"><div class="co">Rushlane</div><div class="dt">Oct 2024 – Present</div></div>
      </div>
      <div class="timeline-row">
        <h3>Video Editor & Videographer — Desh Ki Jaan Hamare Kisan</h3>
        <div class="meta"><div class="co">DKJHK</div><div class="dt">Apr 2025 – Dec 2025</div></div>
      </div>
      <div class="timeline-row">
        <h3>Video Editor & Videographer — Indian Farmer</h3>
        <div class="meta"><div class="co">Indian Farmer</div><div class="dt">Jun 2019 – Oct 2024</div></div>
      </div>
    </div>
  </div>
</section>

<section class="testimonials" id="testimonials">
  <div class="wrap">
    <div class="section-head">
      <span class="eyebrow">Testimonials</span>
      <h2>What <em>Clients</em> are saying.</h2>
      <p>Trusted by creators, brands, and startups who believe in storytelling through powerful visuals.</p>
    </div>
    <div class="grid-testimonials">

      <div class="t-card">
        <div class="stars">★★★★★</div>
        <p class="quote">Hi, main Indrapal Yadav hoon aur Ashutosh ne hamare YouTube channel "Desh Ki Jaan Hamare Kisan" ke liye lagbhag 1 saal tak Video Editor aur Videographer ke roop me kaam kiya hai.

Unke paas farming content ka pehle se kaafi experience tha, jiska hamare channel ko bhi bahut fayda hua. Unki shooting aur editing quality ki wajah se content ki overall quality aur brand value improve hui. Isse hume achhi brand deals milne lagi aur channel ko industry me bhi zyada notice milne laga.

Ashutosh professional hain, feedback ko achhe se samajhte hain aur hamesha quality aur deadlines ka dhyan rakhte hain. Unke saath kaam karne ka experience bahut accha raha aur main content creation aur video production ke liye unhe zarur recommend karunga.</p>
        <div class="t-person">
          <div class="t-avatar">IY</div>
          <div><div class="name">Indrapal Yadav</div><div class="role">Founder, Desh Ki Jaan Hamare Kisan</div></div>
        </div>
      </div>

      <div class="t-card">
        <div class="stars">★★★★★</div>
        <p class="quote">Maine aapke saath kaam karke bahut achha experience kiya hai. Aap sirf ek skilled editor hi nahi, balki bahut professional aur dedicated insaan bhi hain. Har project me aapne details par dhyaan diya aur content ko ek alag hi quality level tak pahunchaya.

Communication hamesha clear raha, deadlines ka poora dhyaan rakha, aur aapke creative suggestions ne final output ko aur bhi behtar banaya. Aapke saath kaam karna smooth aur enjoyable raha. Main aapko kisi bhi creator ya brand ko confidently recommend karunga jo high-quality editing aur professionalism ki talash me ho.

Wishing you all the best for your future projects and growth!</p>
        <div class="t-person">
          <div class="t-avatar">CC</div>
          <div><div class="name">Content Creator</div><div class="role">YouTube Client</div></div>
        </div>
      </div>

      <div class="t-card">
        <div class="stars">★★★★★</div>
        <p class="quote">Ashutosh has been a reliable freelance video editor for our projects. He consistently delivers quality work, understands briefs well, and meets deadlines on time. He is responsive to feedback, professional in his approach, and dependable when working on time-sensitive content. It's been a positive experience working with him, and I would gladly recommend him for video editing and creative projects.</p>
        <div class="t-person">
          <div class="t-avatar">BC</div>
          <div><div class="name">Brand Client</div><div class="role">Freelance Video Editing Partner</div></div>
        </div>
      </div>

      <div class="t-card">
        <div class="stars">★★★★★</div>
        <p class="quote">Hello Ashutosh, पिछले 3 सालों में तुम्हारे साथ काम करके अच्छा लगा। तुम मेहनती हो, अपने काम के प्रति गंभीर रहते हो और वीडियो एडिटिंग में और शूट में भी अच्छी पकड़ रखते हो। हमने साथ मिलके काफ़ी ट्रैवल किया, वहाँ भी एनर्जी के साथ तुमने काम किया। ओवरऑल तुम्हारे साथ काम करने का अनुभव अच्छा रहा। आगे के लिए ढेर सारी शुभकामनाएं।</p>
        <div class="t-person">
          <div class="t-avatar">3Y</div>
          <div><div class="name">Long-term Collaborator</div><div class="role">3 Years — Travel & Video Production</div></div>
        </div>
      </div>

    </div>
  </div>
</section>

<section class="contact" id="contact">
  <div class="wrap">
    <h2>Ready to bring <em>story</em><br>to life?</h2>
    <p>Let's collaborate and craft visuals that connect, inspire, and stand out.</p>
    <a class="btn-primary" href="mailto:hello@example.com">Let's Connect</a>
  </div>
</section>

<footer>
  <a href="https://linkedin.com" target="_blank" rel="noopener">LinkedIn</a>
  <a href="mailto:hello@example.com">Mail</a>
</footer>

<script>
  const menuBtn = document.getElementById('menuBtn');
  const mobilePanel = document.getElementById('mobilePanel');
  const scrim = document.getElementById('scrim');

  function closeMenu(){
    mobilePanel.classList.remove('open');
    scrim.classList.remove('show');
  }
  menuBtn.addEventListener('click', () => {
    mobilePanel.classList.add('open');
    scrim.classList.add('show');
  });
  scrim.addEventListener('click', closeMenu);
  mobilePanel.querySelectorAll('a').forEach(a => a.addEventListener('click', closeMenu));
</script>

</body>
</html>
