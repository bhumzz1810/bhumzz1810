<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Bhumil Parate – GitHub Profile</title>
<link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;600;700;800&family=DM+Mono:wght@400;500&family=Inter:wght@300;400;500&display=swap" rel="stylesheet"/>
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --bg: #080c14;
    --bg2: #0e1520;
    --bg3: #141c2b;
    --border: rgba(99,182,255,0.12);
    --border-glow: rgba(99,182,255,0.35);
    --teal: #2dd4bf;
    --blue: #63b6ff;
    --text: #e2eaf8;
    --muted: #7a8fa8;
    --dim: #3d506a;
    --accent: #f0b429;
  }

  body {
    font-family: 'Inter', sans-serif;
    background: var(--bg);
    color: var(--text);
    min-height: 100vh;
    overflow-x: hidden;
  }

  /* ── Background grid ── */
  body::before {
    content: '';
    position: fixed;
    inset: 0;
    background-image:
      linear-gradient(rgba(99,182,255,0.04) 1px, transparent 1px),
      linear-gradient(90deg, rgba(99,182,255,0.04) 1px, transparent 1px);
    background-size: 40px 40px;
    pointer-events: none;
    z-index: 0;
  }

  /* ── Orbs ── */
  .orb {
    position: fixed;
    border-radius: 50%;
    filter: blur(90px);
    opacity: 0.18;
    pointer-events: none;
    z-index: 0;
    animation: orbFloat 12s ease-in-out infinite alternate;
  }
  .orb-1 { width: 500px; height: 500px; background: #1a6bff; top: -120px; left: -120px; animation-delay: 0s; }
  .orb-2 { width: 400px; height: 400px; background: #2dd4bf; bottom: 5%; right: -100px; animation-delay: -5s; }
  .orb-3 { width: 300px; height: 300px; background: #7c3aed; top: 40%; left: 40%; animation-delay: -8s; }

  @keyframes orbFloat {
    from { transform: translate(0, 0) scale(1); }
    to   { transform: translate(30px, 20px) scale(1.08); }
  }

  /* ── Layout ── */
  .page { position: relative; z-index: 1; max-width: 860px; margin: 0 auto; padding: 60px 24px 100px; }

  /* ── Fade-in animations ── */
  .reveal {
    opacity: 0;
    transform: translateY(28px);
    animation: fadeUp 0.7s cubic-bezier(.22,1,.36,1) forwards;
  }
  @keyframes fadeUp {
    to { opacity: 1; transform: translateY(0); }
  }

  /* ── Hero ── */
  .hero { text-align: center; padding: 40px 0 64px; }
  .hero-tag {
    display: inline-block;
    font-family: 'DM Mono', monospace;
    font-size: 12px;
    color: var(--teal);
    border: 1px solid rgba(45,212,191,0.3);
    padding: 5px 14px;
    border-radius: 20px;
    letter-spacing: 0.12em;
    margin-bottom: 24px;
    animation: fadeUp 0.5s ease forwards, pulseBorder 3s ease-in-out 1s infinite;
  }
  @keyframes pulseBorder {
    0%, 100% { border-color: rgba(45,212,191,0.3); box-shadow: none; }
    50% { border-color: rgba(45,212,191,0.7); box-shadow: 0 0 14px rgba(45,212,191,0.15); }
  }

  .hero-name {
    font-family: 'Syne', sans-serif;
    font-size: clamp(48px, 8vw, 82px);
    font-weight: 800;
    line-height: 1;
    letter-spacing: -0.02em;
    background: linear-gradient(135deg, #e2eaf8 30%, var(--blue) 70%, var(--teal) 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    margin-bottom: 18px;
  }

  .hero-sub {
    font-size: 16px;
    color: var(--muted);
    font-weight: 300;
    letter-spacing: 0.04em;
    max-width: 480px;
    margin: 0 auto 32px;
    line-height: 1.6;
  }

  /* ── Typewriter ── */
  .typewriter-wrap {
    font-family: 'DM Mono', monospace;
    font-size: 14px;
    color: var(--blue);
    margin-bottom: 36px;
    min-height: 22px;
  }
  .typewriter-wrap span { border-right: 2px solid var(--blue); padding-right: 2px; animation: blink 0.75s step-end infinite; }
  @keyframes blink { 50% { border-color: transparent; } }

  /* ── Badges ── */
  .badges { display: flex; gap: 10px; justify-content: center; flex-wrap: wrap; margin-bottom: 8px; }
  .badge {
    display: inline-flex; align-items: center; gap: 6px;
    padding: 8px 16px;
    border-radius: 8px;
    border: 1px solid var(--border);
    background: rgba(255,255,255,0.03);
    font-size: 13px;
    color: var(--text);
    text-decoration: none;
    transition: border-color 0.25s, background 0.25s, transform 0.2s;
    cursor: pointer;
  }
  .badge:hover { border-color: var(--border-glow); background: rgba(99,182,255,0.07); transform: translateY(-2px); }
  .badge-dot { width: 8px; height: 8px; border-radius: 50%; }
  .dot-teal { background: var(--teal); box-shadow: 0 0 6px var(--teal); }
  .dot-blue { background: var(--blue); box-shadow: 0 0 6px var(--blue); }
  .dot-purple { background: #a78bfa; box-shadow: 0 0 6px #a78bfa; }
  .dot-gold { background: var(--accent); box-shadow: 0 0 6px var(--accent); }

  /* ── Divider ── */
  .divider { height: 1px; background: linear-gradient(90deg, transparent, var(--border-glow), transparent); margin: 48px 0; }

  /* ── Section heading ── */
  .section-label {
    font-family: 'DM Mono', monospace;
    font-size: 11px;
    color: var(--teal);
    letter-spacing: 0.15em;
    text-transform: uppercase;
    margin-bottom: 8px;
  }
  .section-title {
    font-family: 'Syne', sans-serif;
    font-size: 28px;
    font-weight: 700;
    color: var(--text);
    margin-bottom: 28px;
  }

  /* ── About grid ── */
  .about-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 16px; margin-bottom: 20px; }
  @media(max-width: 560px) { .about-grid { grid-template-columns: 1fr; } }
  .about-card {
    background: var(--bg2);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 20px 22px;
    transition: border-color 0.25s, transform 0.25s;
    position: relative;
    overflow: hidden;
  }
  .about-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 2px;
    background: linear-gradient(90deg, var(--blue), var(--teal));
    opacity: 0;
    transition: opacity 0.3s;
  }
  .about-card:hover { border-color: var(--border-glow); transform: translateY(-3px); }
  .about-card:hover::before { opacity: 1; }
  .about-card-icon { font-size: 20px; margin-bottom: 10px; }
  .about-card-text { font-size: 14px; color: var(--muted); line-height: 1.6; }
  .about-card-text strong { color: var(--text); font-weight: 500; }

  /* ── Skills ── */
  .skill-groups { display: grid; grid-template-columns: 1fr 1fr; gap: 16px; }
  @media(max-width: 560px) { .skill-groups { grid-template-columns: 1fr; } }
  .skill-group {
    background: var(--bg2);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 20px 22px;
    transition: border-color 0.25s;
  }
  .skill-group:hover { border-color: var(--border-glow); }
  .skill-group-title {
    font-family: 'DM Mono', monospace;
    font-size: 11px;
    color: var(--teal);
    letter-spacing: 0.12em;
    text-transform: uppercase;
    margin-bottom: 14px;
  }
  .skill-pills { display: flex; flex-wrap: wrap; gap: 8px; }
  .pill {
    font-size: 12px;
    padding: 4px 10px;
    border-radius: 6px;
    border: 1px solid var(--border);
    color: var(--muted);
    background: rgba(255,255,255,0.02);
    transition: all 0.2s;
    animation: pillPop 0.4s cubic-bezier(.22,1,.36,1) both;
  }
  .pill:hover { color: var(--text); border-color: var(--border-glow); background: rgba(99,182,255,0.07); }

  @keyframes pillPop {
    from { opacity: 0; transform: scale(0.85); }
    to   { opacity: 1; transform: scale(1); }
  }

  /* ── Experience ── */
  .exp-item {
    background: var(--bg2);
    border: 1px solid var(--border);
    border-radius: 14px;
    padding: 28px 28px 24px;
    margin-bottom: 16px;
    position: relative;
    overflow: hidden;
    transition: border-color 0.3s, transform 0.3s;
  }
  .exp-item:hover { border-color: var(--border-glow); transform: translateX(4px); }
  .exp-side-bar {
    position: absolute;
    left: 0; top: 0; bottom: 0;
    width: 3px;
    border-radius: 3px 0 0 3px;
  }
  .bar-blue  { background: linear-gradient(180deg, var(--blue), var(--teal)); }
  .bar-teal  { background: linear-gradient(180deg, var(--teal), #7c3aed); }
  .exp-header { display: flex; justify-content: space-between; align-items: flex-start; flex-wrap: wrap; gap: 8px; margin-bottom: 6px; }
  .exp-role { font-family: 'Syne', sans-serif; font-size: 18px; font-weight: 700; color: var(--text); }
  .exp-period {
    font-family: 'DM Mono', monospace;
    font-size: 12px;
    color: var(--teal);
    border: 1px solid rgba(45,212,191,0.25);
    padding: 3px 10px;
    border-radius: 20px;
    white-space: nowrap;
  }
  .exp-company { font-size: 14px; color: var(--blue); margin-bottom: 16px; font-weight: 500; }
  .exp-bullets { list-style: none; padding: 0; }
  .exp-bullets li {
    font-size: 14px;
    color: var(--muted);
    padding: 5px 0 5px 20px;
    position: relative;
    line-height: 1.6;
    border-bottom: 1px solid rgba(255,255,255,0.04);
  }
  .exp-bullets li:last-child { border-bottom: none; }
  .exp-bullets li::before {
    content: '▸';
    position: absolute;
    left: 0;
    color: var(--teal);
    font-size: 11px;
    top: 7px;
  }
  .stat-highlight {
    color: var(--accent);
    font-weight: 500;
    font-family: 'DM Mono', monospace;
    font-size: 13px;
  }

  /* ── Stats row ── */
  .stats-row { display: grid; grid-template-columns: repeat(4, 1fr); gap: 14px; }
  @media(max-width: 560px) { .stats-row { grid-template-columns: repeat(2, 1fr); } }
  .stat-card {
    background: var(--bg2);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 20px 16px;
    text-align: center;
    transition: border-color 0.25s, transform 0.25s;
    animation: none;
  }
  .stat-card:hover { border-color: var(--border-glow); transform: translateY(-3px); }
  .stat-num {
    font-family: 'Syne', sans-serif;
    font-size: 32px;
    font-weight: 800;
    color: var(--blue);
    line-height: 1;
    margin-bottom: 6px;
  }
  .stat-label { font-size: 12px; color: var(--muted); line-height: 1.4; }

  /* ── Contact ── */
  .contact-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 14px; }
  @media(max-width: 500px) { .contact-grid { grid-template-columns: 1fr; } }
  .contact-card {
    background: var(--bg2);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 18px 20px;
    display: flex;
    align-items: center;
    gap: 14px;
    text-decoration: none;
    color: var(--text);
    transition: border-color 0.25s, transform 0.25s;
  }
  .contact-card:hover { border-color: var(--border-glow); transform: translateX(4px); }
  .contact-icon { font-size: 22px; flex-shrink: 0; }
  .contact-label { font-size: 11px; color: var(--muted); margin-bottom: 2px; font-family: 'DM Mono', monospace; letter-spacing: 0.08em; }
  .contact-value { font-size: 14px; color: var(--blue); font-weight: 500; }

  /* ── Footer ── */
  .footer { text-align: center; padding-top: 60px; }
  .footer-text { font-family: 'DM Mono', monospace; font-size: 12px; color: var(--dim); letter-spacing: 0.08em; }
  .footer-pulse {
    display: inline-block;
    width: 8px; height: 8px;
    border-radius: 50%;
    background: var(--teal);
    margin-right: 8px;
    animation: pulseGreen 2s ease-in-out infinite;
    vertical-align: middle;
  }
  @keyframes pulseGreen {
    0%, 100% { transform: scale(1); opacity: 1; }
    50% { transform: scale(1.5); opacity: 0.5; }
  }

  /* ── Scroll reveal ── */
  .scroll-reveal { opacity: 0; transform: translateY(30px); transition: opacity 0.7s cubic-bezier(.22,1,.36,1), transform 0.7s cubic-bezier(.22,1,.36,1); }
  .scroll-reveal.visible { opacity: 1; transform: translateY(0); }
</style>
</head>
<body>

<div class="orb orb-1"></div>
<div class="orb orb-2"></div>
<div class="orb orb-3"></div>

<div class="page">

  <!-- ── HERO ── -->
  <div class="hero">
    <div class="hero-tag reveal" style="animation-delay:0.1s">OPEN TO OPPORTUNITIES · ONTARIO, CANADA 🇨🇦</div>
    <h1 class="hero-name reveal" style="animation-delay:0.25s">Bhumil Parate</h1>
    <p class="hero-sub reveal" style="animation-delay:0.4s">Full Stack Developer crafting scalable, cloud-native applications with Java, Spring Boot &amp; React.js</p>
    <div class="typewriter-wrap reveal" style="animation-delay:0.55s">
      <span id="typed"></span>
    </div>
    <div class="badges reveal" style="animation-delay:0.7s">
      <a href="mailto:bhumilparate944@gmail.com" class="badge"><span class="badge-dot dot-teal"></span>Email Me</a>
      <a href="#" class="badge"><span class="badge-dot dot-blue"></span>LinkedIn</a>
      <a href="#" class="badge"><span class="badge-dot dot-purple"></span>Portfolio</a>
      <a href="#" class="badge"><span class="badge-dot dot-gold"></span>+1 (382) 885-3109</a>
    </div>
  </div>

  <div class="divider scroll-reveal"></div>

  <!-- ── ABOUT ── -->
  <section class="scroll-reveal">
    <div class="section-label">// about me</div>
    <div class="section-title">Who I Am</div>
    <div class="about-grid">
      <div class="about-card">
        <div class="about-card-icon">⚡</div>
        <div class="about-card-text"><strong>Currently @ Siemens Canada</strong><br/>Building backend microservices for smart energy & IoT monitoring platforms using Java 17 + Spring Boot.</div>
      </div>
      <div class="about-card">
        <div class="about-card-icon">🎓</div>
        <div class="about-card-text"><strong>Graduate, Conestoga College</strong><br/>Web Design & Development · Aug 2025 | B.Tech in IT from GTU, India · Jul 2021</div>
      </div>
      <div class="about-card">
        <div class="about-card-icon">☁️</div>
        <div class="about-card-text"><strong>Cloud-Native & Microservices</strong><br/>AWS, Azure, Docker, Kubernetes — from solo services to distributed fault-tolerant architectures.</div>
      </div>
      <div class="about-card">
        <div class="about-card-icon">🔐</div>
        <div class="about-card-text"><strong>Security First</strong><br/>Spring Security, OAuth2, JWT — reduced unauthorized access by <strong>40%</strong> in production environments.</div>
      </div>
    </div>
  </section>

  <div class="divider scroll-reveal"></div>

  <!-- ── STATS ── -->
  <section class="scroll-reveal">
    <div class="section-label">// impact</div>
    <div class="section-title">By the Numbers</div>
    <div class="stats-row">
      <div class="stat-card">
        <div class="stat-num" data-target="3">0</div>
        <div class="stat-label">Years of<br/>Experience</div>
      </div>
      <div class="stat-card">
        <div class="stat-num" data-target="40">0</div>
        <div class="stat-label">% API Response<br/>Improvement</div>
      </div>
      <div class="stat-card">
        <div class="stat-num" data-target="35">0</div>
        <div class="stat-label">% Faster<br/>Data Retrieval</div>
      </div>
      <div class="stat-card">
        <div class="stat-num" data-target="30">0</div>
        <div class="stat-label">% Downtime<br/>Reduction</div>
      </div>
    </div>
  </section>

  <div class="divider scroll-reveal"></div>

  <!-- ── SKILLS ── -->
  <section class="scroll-reveal">
    <div class="section-label">// tech stack</div>
    <div class="section-title">Skills & Technologies</div>
    <div class="skill-groups">
      <div class="skill-group">
        <div class="skill-group-title">// Languages</div>
        <div class="skill-pills" id="pills-lang"></div>
      </div>
      <div class="skill-group">
        <div class="skill-group-title">// Frontend</div>
        <div class="skill-pills" id="pills-front"></div>
      </div>
      <div class="skill-group">
        <div class="skill-group-title">// Backend</div>
        <div class="skill-pills" id="pills-back"></div>
      </div>
      <div class="skill-group">
        <div class="skill-group-title">// Cloud & DevOps</div>
        <div class="skill-pills" id="pills-cloud"></div>
      </div>
      <div class="skill-group">
        <div class="skill-group-title">// Databases</div>
        <div class="skill-pills" id="pills-db"></div>
      </div>
      <div class="skill-group">
        <div class="skill-group-title">// Security & Messaging</div>
        <div class="skill-pills" id="pills-sec"></div>
      </div>
    </div>
  </section>

  <div class="divider scroll-reveal"></div>

  <!-- ── EXPERIENCE ── -->
  <section class="scroll-reveal">
    <div class="section-label">// experience</div>
    <div class="section-title">Career Highlights</div>

    <div class="exp-item">
      <div class="exp-side-bar bar-blue"></div>
      <div class="exp-header">
        <div class="exp-role">Full Stack Developer</div>
        <div class="exp-period">Aug 2025 – Present</div>
      </div>
      <div class="exp-company">⚡ Siemens · Canada</div>
      <ul class="exp-bullets">
        <li>Built backend microservices for smart energy & IoT platforms (Java 17, Spring Boot, Spring Cloud) — improved grid fault detection by <span class="stat-highlight">35%</span></li>
        <li>Secured distributed APIs with OAuth2 + JWT, cutting unauthorized access incidents by <span class="stat-highlight">40%</span></li>
        <li>Deployed on AWS (EC2, S3, RDS, Lambda) with Docker & Kubernetes — reduced downtime by <span class="stat-highlight">30%</span></li>
        <li>Monitored real-time streams with Apache Kafka + AWS CloudWatch, boosting predictive maintenance by <span class="stat-highlight">25%</span></li>
        <li>Optimized PostgreSQL queries & React.js dashboards — improved responsiveness by <span class="stat-highlight">28%</span></li>
      </ul>
    </div>

    <div class="exp-item">
      <div class="exp-side-bar bar-teal"></div>
      <div class="exp-header">
        <div class="exp-role">Backend Developer</div>
        <div class="exp-period">Jan 2021 – Dec 2023</div>
      </div>
      <div class="exp-company">🚀 Luckimedia · India</div>
      <ul class="exp-bullets">
        <li>Designed RESTful microservices improving API response times by <span class="stat-highlight">40%</span> across distributed backend systems</li>
        <li>Integrated Stripe, PayPal, Shopify & Amazon APIs — reduced transaction failures by <span class="stat-highlight">25%</span></li>
        <li>Deployed on Microsoft Azure via Docker & CI/CD pipelines — cut release cycles by <span class="stat-highlight">40%</span></li>
        <li>Optimized MySQL & MongoDB queries achieving <span class="stat-highlight">35%</span> faster data retrieval</li>
        <li>Built React.js + TypeScript features — boosted platform adoption by <span class="stat-highlight">20%</span></li>
      </ul>
    </div>
  </section>

  <div class="divider scroll-reveal"></div>

  <!-- ── CONTACT ── -->
  <section class="scroll-reveal">
    <div class="section-label">// contact</div>
    <div class="section-title">Get In Touch</div>
    <div class="contact-grid">
      <a href="mailto:bhumilparate944@gmail.com" class="contact-card">
        <div class="contact-icon">✉️</div>
        <div><div class="contact-label">EMAIL</div><div class="contact-value">bhumilparate944@gmail.com</div></div>
      </a>
      <a href="#" class="contact-card">
        <div class="contact-icon">💼</div>
        <div><div class="contact-label">LINKEDIN</div><div class="contact-value">linkedin.com/in/bhumilparate</div></div>
      </a>
      <a href="#" class="contact-card">
        <div class="contact-icon">🌐</div>
        <div><div class="contact-label">PORTFOLIO</div><div class="contact-value">bhumilparate.dev</div></div>
      </a>
      <a href="tel:+13828853109" class="contact-card">
        <div class="contact-icon">📞</div>
        <div><div class="contact-label">PHONE</div><div class="contact-value">+1 (382) 885-3109</div></div>
      </a>
    </div>
  </section>

  <!-- ── FOOTER ── -->
  <div class="footer scroll-reveal">
    <p class="footer-text">
      <span class="footer-pulse"></span>
      available for full-time roles &amp; freelance projects · ontario, canada
    </p>
  </div>

</div>

<script>
  /* ── Typewriter ── */
  const phrases = [
    'Java 17 + Spring Boot',
    'React.js + TypeScript',
    'Microservices Architecture',
    'AWS · Azure · Kubernetes',
    'OAuth2 · JWT · Kafka',
  ];
  let pi = 0, ci = 0, deleting = false;
  const el = document.getElementById('typed');
  function type() {
    const cur = phrases[pi];
    el.textContent = deleting ? cur.slice(0, ci--) : cur.slice(0, ci++);
    if (!deleting && ci > cur.length) { deleting = true; setTimeout(type, 1400); return; }
    if (deleting && ci < 0) { deleting = false; pi = (pi + 1) % phrases.length; ci = 0; setTimeout(type, 400); return; }
    setTimeout(type, deleting ? 40 : 80);
  }
  setTimeout(type, 900);

  /* ── Pill injection ── */
  const skills = {
    'pills-lang':  ['Java 17', 'TypeScript', 'JavaScript (ES6+)', 'SQL'],
    'pills-front': ['React.js', 'HTML5', 'CSS3', 'Responsive UI'],
    'pills-back':  ['Spring Boot', 'Spring Cloud', 'Spring MVC', 'Hibernate', 'JPA', 'RESTful APIs'],
    'pills-cloud': ['AWS', 'Microsoft Azure', 'Docker', 'Kubernetes', 'GitHub Actions', 'Jenkins', 'CI/CD'],
    'pills-db':    ['PostgreSQL', 'MySQL', 'MongoDB', 'SQL Optimization'],
    'pills-sec':   ['Spring Security', 'OAuth2', 'JWT', 'Apache Kafka', 'JUnit', 'Mockito'],
  };
  Object.entries(skills).forEach(([id, items]) => {
    const wrap = document.getElementById(id);
    items.forEach((s, i) => {
      const p = document.createElement('span');
      p.className = 'pill';
      p.textContent = s;
      p.style.animationDelay = (i * 0.05) + 's';
      wrap.appendChild(p);
    });
  });

  /* ── Counter animation ── */
  function animateCounter(el, target) {
    let start = 0;
    const dur = 1400, step = 16;
    const inc = target / (dur / step);
    const timer = setInterval(() => {
      start = Math.min(start + inc, target);
      el.textContent = (target > 10 ? Math.round(start) : start.toFixed(0)) + (target >= 10 ? '%' : '+');
      if (start >= target) { el.textContent = target + (target >= 10 ? '%' : '+'); clearInterval(timer); }
    }, step);
  }

  /* ── Scroll reveal ── */
  const revealEls = document.querySelectorAll('.scroll-reveal');
  const counters  = document.querySelectorAll('.stat-num[data-target]');
  const observer  = new IntersectionObserver((entries) => {
    entries.forEach(e => {
      if (e.isIntersecting) {
        e.target.classList.add('visible');
        observer.unobserve(e.target);
      }
    });
  }, { threshold: 0.12 });
  revealEls.forEach(el => observer.observe(el));

  /* ── Counter observer ── */
  const cObs = new IntersectionObserver((entries) => {
    entries.forEach(e => {
      if (e.isIntersecting) {
        const t = +e.target.dataset.target;
        animateCounter(e.target, t);
        cObs.unobserve(e.target);
      }
    });
  }, { threshold: 0.4 });
  counters.forEach(c => cObs.observe(c));
</script>
</body>
</html>
