<!DOCTYPE html>  
  
<html lang="en">  
<head>  
<meta charset="UTF-8">  
<meta name="viewport" content="width=device-width, initial-scale=1.0">  
<title>BridgeWork — Connect. Create. Deliver.</title>  
<link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;600;700;800&family=DM+Sans:ital,wght@0,300;0,400;0,500;1,300&display=swap" rel="stylesheet">  
<style>  
  *, *::before, *::after { margin: 0; padding: 0; box-sizing: border-box; }  
  
:root {  
–ink: #0a0a0f;  
–paper: #f5f3ee;  
–accent: #ff4d1c;  
–accent2: #1c6eff;  
–muted: #8a8680;  
–card: #ffffff;  
–border: #e2dfd8;  
}  
  
html { scroll-behavior: smooth; }  
  
body {  
font-family: ‘DM Sans’, sans-serif;  
background: var(–paper);  
color: var(–ink);  
overflow-x: hidden;  
}  
  
/* ── NOISE TEXTURE ── */  
body::before {  
content: ‘’;  
position: fixed;  
inset: 0;  
background-image: url(“data:image/svg+xml,%3Csvg viewBox=‘0 0 256 256’ xmlns=‘http://www.w3.org/2000/svg’%3E%3Cfilter id=‘n’%3E%3CfeTurbulence type=‘fractalNoise’ baseFrequency=‘0.9’ numOctaves=‘4’ stitchTiles=‘stitch’/%3E%3C/filter%3E%3Crect width=‘100%25’ height=‘100%25’ filter=‘url(%23n)’ opacity=‘0.03’/%3E%3C/svg%3E”);  
pointer-events: none;  
z-index: 9999;  
opacity: 0.4;  
}  
  
/* ── NAV ── */  
nav {  
position: fixed;  
top: 0; left: 0; right: 0;  
z-index: 100;  
display: flex;  
align-items: center;  
justify-content: space-between;  
padding: 1.25rem 4rem;  
background: rgba(245,243,238,0.85);  
backdrop-filter: blur(12px);  
border-bottom: 1px solid var(–border);  
}  
  
.logo {  
font-family: ‘Syne’, sans-serif;  
font-weight: 800;  
font-size: 1.5rem;  
letter-spacing: -0.03em;  
color: var(–ink);  
text-decoration: none;  
}  
.logo span { color: var(–accent); }  
  
.nav-links {  
display: flex;  
gap: 2rem;  
list-style: none;  
}  
.nav-links a {  
text-decoration: none;  
color: var(–muted);  
font-size: 0.9rem;  
font-weight: 500;  
transition: color 0.2s;  
}  
.nav-links a:hover { color: var(–ink); }  
  
.nav-cta {  
display: flex;  
gap: 0.75rem;  
align-items: center;  
}  
  
.btn {  
display: inline-flex;  
align-items: center;  
gap: 0.4rem;  
padding: 0.65rem 1.4rem;  
border-radius: 100px;  
font-size: 0.875rem;  
font-weight: 500;  
cursor: pointer;  
transition: all 0.2s;  
text-decoration: none;  
border: none;  
font-family: ‘DM Sans’, sans-serif;  
}  
.btn-ghost {  
background: transparent;  
color: var(–ink);  
border: 1.5px solid var(–border);  
}  
.btn-ghost:hover { border-color: var(–ink); }  
.btn-primary {  
background: var(–ink);  
color: var(–paper);  
}  
.btn-primary:hover { background: var(–accent); }  
.btn-accent {  
background: var(–accent);  
color: white;  
}  
.btn-accent:hover { background: #e63c0a; }  
.btn-lg {  
padding: 0.9rem 2rem;  
font-size: 1rem;  
}  
  
/* ── HERO ── */  
.hero {  
min-height: 100vh;  
display: grid;  
grid-template-columns: 1fr 1fr;  
align-items: center;  
padding: 8rem 4rem 4rem;  
gap: 4rem;  
position: relative;  
overflow: hidden;  
}  
  
.hero-bg-circle {  
position: absolute;  
border-radius: 50%;  
filter: blur(80px);  
opacity: 0.12;  
pointer-events: none;  
}  
.hero-bg-circle.c1 {  
width: 600px; height: 600px;  
background: var(–accent);  
top: -100px; right: -100px;  
}  
.hero-bg-circle.c2 {  
width: 400px; height: 400px;  
background: var(–accent2);  
bottom: 0; left: 200px;  
}  
  
.hero-tag {  
display: inline-flex;  
align-items: center;  
gap: 0.5rem;  
background: white;  
border: 1px solid var(–border);  
border-radius: 100px;  
padding: 0.35rem 0.9rem;  
font-size: 0.8rem;  
font-weight: 500;  
color: var(–muted);  
margin-bottom: 1.5rem;  
animation: fadeUp 0.6s ease both;  
}  
.hero-tag .dot {  
width: 6px; height: 6px;  
background: #22c55e;  
border-radius: 50%;  
animation: pulse 2s infinite;  
}  
@keyframes pulse {  
0%,100% { opacity: 1; transform: scale(1); }  
50% { opacity: 0.5; transform: scale(1.4); }  
}  
  
.hero-title {  
font-family: ‘Syne’, sans-serif;  
font-size: clamp(2.8rem, 5vw, 4.5rem);  
font-weight: 800;  
line-height: 1.05;  
letter-spacing: -0.03em;  
animation: fadeUp 0.6s 0.1s ease both;  
}  
.hero-title em {  
font-style: normal;  
color: var(–accent);  
position: relative;  
}  
.hero-title em::after {  
content: ‘’;  
position: absolute;  
bottom: 4px; left: 0; right: 0;  
height: 3px;  
background: var(–accent);  
border-radius: 2px;  
opacity: 0.3;  
}  
  
.hero-sub {  
margin-top: 1.5rem;  
font-size: 1.1rem;  
color: var(–muted);  
line-height: 1.7;  
max-width: 480px;  
animation: fadeUp 0.6s 0.2s ease both;  
}  
  
.hero-actions {  
display: flex;  
gap: 1rem;  
margin-top: 2.5rem;  
flex-wrap: wrap;  
animation: fadeUp 0.6s 0.3s ease both;  
}  
  
.hero-stats {  
display: flex;  
gap: 2.5rem;  
margin-top: 3rem;  
animation: fadeUp 0.6s 0.4s ease both;  
}  
.stat-num {  
font-family: ‘Syne’, sans-serif;  
font-size: 1.8rem;  
font-weight: 800;  
color: var(–ink);  
}  
.stat-label {  
font-size: 0.8rem;  
color: var(–muted);  
margin-top: 0.1rem;  
}  
  
/* ── HERO VISUAL ── */  
.hero-visual {  
display: flex;  
flex-direction: column;  
gap: 1rem;  
animation: fadeLeft 0.8s 0.2s ease both;  
position: relative;  
}  
  
@keyframes fadeUp {  
from { opacity: 0; transform: translateY(20px); }  
to { opacity: 1; transform: translateY(0); }  
}  
@keyframes fadeLeft {  
from { opacity: 0; transform: translateX(30px); }  
to { opacity: 1; transform: translateX(0); }  
}  
  
.profile-card {  
background: white;  
border: 1px solid var(–border);  
border-radius: 16px;  
padding: 1.25rem 1.5rem;  
display: flex;  
align-items: center;  
gap: 1rem;  
box-shadow: 0 4px 24px rgba(0,0,0,0.05);  
transition: transform 0.3s, box-shadow 0.3s;  
}  
.profile-card:hover {  
transform: translateY(-3px);  
box-shadow: 0 8px 32px rgba(0,0,0,0.08);  
}  
  
.avatar {  
width: 48px; height: 48px;  
border-radius: 50%;  
display: flex;  
align-items: center;  
justify-content: center;  
font-size: 1.2rem;  
flex-shrink: 0;  
}  
  
.card-meta { flex: 1; }  
.card-name { font-weight: 600; font-size: 0.95rem; }  
.card-role { font-size: 0.8rem; color: var(–muted); }  
.card-badge {  
padding: 0.25rem 0.7rem;  
border-radius: 100px;  
font-size: 0.75rem;  
font-weight: 600;  
}  
.badge-green { background: #dcfce7; color: #16a34a; }  
.badge-blue { background: #dbeafe; color: #1d4ed8; }  
.badge-orange { background: #ffedd5; color: #c2410c; }  
  
.stars { color: #f59e0b; font-size: 0.8rem; }  
  
.floating-tag {  
position: absolute;  
background: var(–accent);  
color: white;  
padding: 0.5rem 1rem;  
border-radius: 100px;  
font-size: 0.8rem;  
font-weight: 600;  
right: -1rem;  
top: 50%;  
transform: translateY(-50%) rotate(3deg);  
white-space: nowrap;  
box-shadow: 0 4px 16px rgba(255,77,28,0.3);  
animation: float 3s ease-in-out infinite;  
}  
@keyframes float {  
0%,100% { transform: translateY(-50%) rotate(3deg); }  
50% { transform: translateY(calc(-50% - 6px)) rotate(3deg); }  
}  
  
/* ── HOW IT WORKS ── */  
.section {  
padding: 6rem 4rem;  
}  
  
.section-label {  
display: inline-block;  
font-size: 0.75rem;  
font-weight: 600;  
letter-spacing: 0.12em;  
text-transform: uppercase;  
color: var(–accent);  
margin-bottom: 1rem;  
}  
  
.section-title {  
font-family: ‘Syne’, sans-serif;  
font-size: clamp(2rem, 3.5vw, 3rem);  
font-weight: 800;  
letter-spacing: -0.03em;  
line-height: 1.1;  
max-width: 600px;  
}  
  
.steps-grid {  
display: grid;  
grid-template-columns: repeat(3, 1fr);  
gap: 2rem;  
margin-top: 4rem;  
}  
  
.step-card {  
background: white;  
border: 1px solid var(–border);  
border-radius: 20px;  
padding: 2.5rem 2rem;  
position: relative;  
overflow: hidden;  
transition: transform 0.3s, box-shadow 0.3s;  
}  
.step-card:hover {  
transform: translateY(-6px);  
box-shadow: 0 12px 40px rgba(0,0,0,0.08);  
}  
.step-card::before {  
content: ‘’;  
position: absolute;  
top: 0; left: 0; right: 0;  
height: 3px;  
}  
.step-card:nth-child(1)::before { background: var(–accent); }  
.step-card:nth-child(2)::before { background: var(–accent2); }  
.step-card:nth-child(3)::before { background: #8b5cf6; }  
  
.step-num {  
font-family: ‘Syne’, sans-serif;  
font-size: 3.5rem;  
font-weight: 800;  
opacity: 0.07;  
line-height: 1;  
margin-bottom: 1rem;  
}  
.step-icon {  
font-size: 2rem;  
margin-bottom: 1rem;  
}  
.step-title {  
font-family: ‘Syne’, sans-serif;  
font-size: 1.2rem;  
font-weight: 700;  
margin-bottom: 0.75rem;  
}  
.step-desc {  
color: var(–muted);  
font-size: 0.9rem;  
line-height: 1.7;  
}  
  
/* ── CATEGORIES ── */  
.categories-section {  
background: var(–ink);  
color: white;  
padding: 6rem 4rem;  
}  
  
.categories-section .section-label { color: #ff6b47; }  
.categories-section .section-title { color: white; }  
  
.cats-grid {  
display: grid;  
grid-template-columns: repeat(4, 1fr);  
gap: 1rem;  
margin-top: 3rem;  
}  
  
.cat-card {  
background: rgba(255,255,255,0.05);  
border: 1px solid rgba(255,255,255,0.08);  
border-radius: 16px;  
padding: 2rem 1.5rem;  
cursor: pointer;  
transition: all 0.3s;  
text-align: center;  
}  
.cat-card:hover {  
background: rgba(255,255,255,0.1);  
border-color: rgba(255,255,255,0.2);  
transform: translateY(-4px);  
}  
.cat-icon { font-size: 2rem; margin-bottom: 1rem; }  
.cat-name {  
font-family: ‘Syne’, sans-serif;  
font-weight: 700;  
font-size: 1rem;  
margin-bottom: 0.4rem;  
}  
.cat-count { font-size: 0.8rem; color: rgba(255,255,255,0.4); }  
  
/* ── SPLIT SECTION ── */  
.split-section {  
display: grid;  
grid-template-columns: 1fr 1fr;  
min-height: 70vh;  
}  
  
.split-left, .split-right {  
padding: 6rem 4rem;  
display: flex;  
flex-direction: column;  
justify-content: center;  
}  
  
.split-left {  
background: #fff8f6;  
border-right: 1px solid var(–border);  
}  
  
.split-right {  
background: #f0f4ff;  
}  
  
.split-icon {  
font-size: 2.5rem;  
margin-bottom: 1.5rem;  
}  
  
.split-title {  
font-family: ‘Syne’, sans-serif;  
font-size: 1.8rem;  
font-weight: 800;  
margin-bottom: 1rem;  
letter-spacing: -0.02em;  
}  
  
.split-desc {  
color: var(–muted);  
line-height: 1.8;  
margin-bottom: 2rem;  
font-size: 0.95rem;  
}  
  
.feature-list {  
list-style: none;  
display: flex;  
flex-direction: column;  
gap: 0.75rem;  
margin-bottom: 2rem;  
}  
.feature-list li {  
display: flex;  
align-items: center;  
gap: 0.75rem;  
font-size: 0.9rem;  
color: var(–ink);  
}  
.feature-list li::before {  
content: ‘✓’;  
width: 20px; height: 20px;  
background: var(–accent);  
color: white;  
border-radius: 50%;  
display: inline-flex;  
align-items: center;  
justify-content: center;  
font-size: 0.65rem;  
font-weight: 700;  
flex-shrink: 0;  
}  
  
/* ── TESTIMONIALS ── */  
.testimonials {  
padding: 6rem 4rem;  
background: var(–paper);  
}  
  
.testi-grid {  
display: grid;  
grid-template-columns: repeat(3, 1fr);  
gap: 1.5rem;  
margin-top: 3rem;  
}  
  
.testi-card {  
background: white;  
border: 1px solid var(–border);  
border-radius: 20px;  
padding: 2rem;  
position: relative;  
transition: transform 0.3s, box-shadow 0.3s;  
}  
.testi-card:hover {  
transform: translateY(-4px);  
box-shadow: 0 12px 32px rgba(0,0,0,0.07);  
}  
  
.testi-quote {  
font-size: 2rem;  
color: var(–accent);  
font-family: Georgia, serif;  
line-height: 1;  
margin-bottom: 1rem;  
}  
.testi-text {  
font-size: 0.9rem;  
color: var(–muted);  
line-height: 1.75;  
margin-bottom: 1.5rem;  
font-style: italic;  
}  
.testi-author {  
display: flex;  
align-items: center;  
gap: 0.75rem;  
}  
.testi-avatar {  
width: 40px; height: 40px;  
border-radius: 50%;  
display: flex;  
align-items: center;  
justify-content: center;  
font-size: 1rem;  
}  
.testi-name { font-weight: 600; font-size: 0.9rem; }  
.testi-role { font-size: 0.8rem; color: var(–muted); }  
  
/* ── CTA SECTION ── */  
.cta-section {  
background: var(–ink);  
color: white;  
padding: 7rem 4rem;  
text-align: center;  
position: relative;  
overflow: hidden;  
}  
  
.cta-section::before {  
content: ‘’;  
position: absolute;  
width: 500px; height: 500px;  
border-radius: 50%;  
background: var(–accent);  
opacity: 0.08;  
top: -200px; left: -100px;  
filter: blur(60px);  
}  
.cta-section::after {  
content: ‘’;  
position: absolute;  
width: 400px; height: 400px;  
border-radius: 50%;  
background: var(–accent2);  
opacity: 0.08;  
bottom: -150px; right: -50px;  
filter: blur(60px);  
}  
  
.cta-title {  
font-family: ‘Syne’, sans-serif;  
font-size: clamp(2.5rem, 5vw, 4rem);  
font-weight: 800;  
letter-spacing: -0.03em;  
margin-bottom: 1.5rem;  
position: relative;  
}  
.cta-title em {  
font-style: normal;  
color: var(–accent);  
}  
  
.cta-sub {  
color: rgba(255,255,255,0.5);  
font-size: 1.1rem;  
max-width: 500px;  
margin: 0 auto 3rem;  
line-height: 1.7;  
}  
  
.cta-btns {  
display: flex;  
gap: 1rem;  
justify-content: center;  
flex-wrap: wrap;  
position: relative;  
}  
  
.btn-white {  
background: white;  
color: var(–ink);  
border: none;  
}  
.btn-white:hover { background: var(–paper); }  
  
.btn-outline-white {  
background: transparent;  
color: white;  
border: 1.5px solid rgba(255,255,255,0.25);  
}  
.btn-outline-white:hover { border-color: white; }  
  
/* ── FOOTER ── */  
footer {  
background: #07070b;  
color: rgba(255,255,255,0.4);  
padding: 3rem 4rem;  
display: flex;  
align-items: center;  
justify-content: space-between;  
}  
  
.footer-logo {  
font-family: ‘Syne’, sans-serif;  
font-weight: 800;  
font-size: 1.25rem;  
color: white;  
}  
.footer-logo span { color: var(–accent); }  
  
.footer-links {  
display: flex;  
gap: 2rem;  
list-style: none;  
}  
.footer-links a {  
color: rgba(255,255,255,0.4);  
text-decoration: none;  
font-size: 0.85rem;  
transition: color 0.2s;  
}  
.footer-links a:hover { color: white; }  
  
/* ── TRUST BAR ── */  
.trust-bar {  
background: white;  
border-top: 1px solid var(–border);  
border-bottom: 1px solid var(–border);  
padding: 1.5rem 4rem;  
display: flex;  
align-items: center;  
justify-content: center;  
gap: 3rem;  
overflow: hidden;  
}  
.trust-item {  
display: flex;  
align-items: center;  
gap: 0.6rem;  
font-size: 0.85rem;  
color: var(–muted);  
white-space: nowrap;  
}  
.trust-item .icon { font-size: 1rem; }  
  
/* Scroll animation */  
.reveal {  
opacity: 0;  
transform: translateY(24px);  
transition: opacity 0.7s ease, transform 0.7s ease;  
}  
.reveal.visible {  
opacity: 1;  
transform: none;  
}  
</style>  
  
</head>  
<body>  
  
<!-- NAV -->  
  
<nav>  
  <a href="#" class="logo">BridgeWork<span>.</span></a>  
  <ul class="nav-links">  
    <li><a href="#how">How it works</a></li>  
    <li><a href="#categories">Categories</a></li>  
    <li><a href="#for-you">For you</a></li>  
  </ul>  
  <div class="nav-cta">  
    <a href="#" class="btn btn-ghost">Log in</a>  
    <a href="#" class="btn btn-accent">Get started</a>  
  </div>  
</nav>  
  
<!-- HERO -->  
  
<section class="hero">  
  <div class="hero-bg-circle c1"></div>  
  <div class="hero-bg-circle c2"></div>  
  
  <div>  
    <div class="hero-tag">  
      <span class="dot"></span>  
      Now live globally · 40,000+ freelancers  
    </div>  
    <h1 class="hero-title">  
      The bridge between<br>  
      talent &amp; <em>opportunity</em>  
    </h1>  
    <p class="hero-sub">  
      BridgeWork connects clients with world-class freelancers — instantly, securely, and with zero friction. Post a job or offer your skills in minutes.  
    </p>  
    <div class="hero-actions">  
      <a href="#" class="btn btn-accent btn-lg">I need a freelancer →</a>  
      <a href="#" class="btn btn-ghost btn-lg">Offer my services</a>  
    </div>  
    <div class="hero-stats">  
      <div>  
        <div class="stat-num">40K+</div>  
        <div class="stat-label">Freelancers</div>  
      </div>  
      <div>  
        <div class="stat-num">98%</div>  
        <div class="stat-label">Satisfaction rate</div>  
      </div>  
      <div>  
        <div class="stat-num">120+</div>  
        <div class="stat-label">Countries</div>  
      </div>  
    </div>  
  </div>  
  
  <div class="hero-visual">  
    <div class="profile-card" style="animation-delay:0.1s">  
      <div class="avatar" style="background:#fff0eb">🎨</div>  
      <div class="card-meta">  
        <div class="card-name">Youssef A.</div>  
        <div class="card-role">UI/UX Designer · Morocco</div>  
        <div class="stars">★★★★★</div>  
      </div>  
      <span class="card-badge badge-green">Available</span>  
    </div>  
  
```  
<div class="profile-card" style="animation-delay:0.2s">  
  <div class="avatar" style="background:#eff6ff">💻</div>  
  <div class="card-meta">  
    <div class="card-name">Sara M.</div>  
    <div class="card-role">Full-Stack Developer · Tunisia</div>  
    <div class="stars">★★★★★</div>  
  </div>  
  <span class="card-badge badge-blue">Top Rated</span>  
</div>  
  
<div class="profile-card" style="animation-delay:0.3s; position:relative">  
  <div class="avatar" style="background:#fef9ec">📱</div>  
  <div class="card-meta">  
    <div class="card-name">Karim L.</div>  
    <div class="card-role">Mobile Developer · Algeria</div>  
    <div class="stars">★★★★☆</div>  
  </div>  
  <span class="card-badge badge-orange">Hot 🔥</span>  
  <div class="floating-tag">Deal closed! +$850</div>  
</div>  
  
<div class="profile-card" style="animation-delay:0.4s">  
  <div class="avatar" style="background:#f5f0ff">✍️</div>  
  <div class="card-meta">  
    <div class="card-name">Nour B.</div>  
    <div class="card-role">Content Writer · France</div>  
    <div class="stars">★★★★★</div>  
  </div>  
  <span class="card-badge badge-green">Available</span>  
</div>  
```  
  
  </div>  
</section>  
  
<!-- TRUST BAR -->  
  
<div class="trust-bar">  
  <div class="trust-item"><span class="icon">🔒</span> Secure payments</div>  
  <div class="trust-item"><span class="icon">⚡</span> Fast matching</div>  
  <div class="trust-item"><span class="icon">💬</span> Real-time messaging</div>  
  <div class="trust-item"><span class="icon">✅</span> Verified profiles</div>  
  <div class="trust-item"><span class="icon">🌍</span> 120+ countries</div>  
  <div class="trust-item"><span class="icon">🎯</span> Commission only on success</div>  
</div>  
  
<!-- HOW IT WORKS -->  
  
<section class="section" id="how">  
  <div class="reveal">  
    <span class="section-label">How it works</span>  
    <h2 class="section-title">Three steps to your perfect match</h2>  
  </div>  
  <div class="steps-grid">  
    <div class="step-card reveal">  
      <div class="step-num">01</div>  
      <div class="step-icon">📋</div>  
      <h3 class="step-title">Post or Browse</h3>  
      <p class="step-desc">Clients post their project in seconds. Freelancers browse opportunities matching their skills — no middleman, no delay.</p>  
    </div>  
    <div class="step-card reveal">  
      <div class="step-num">02</div>  
      <div class="step-icon">🤝</div>  
      <h3 class="step-title">Connect & Agree</h3>  
      <p class="step-desc">Chat directly, negotiate terms, and lock in the deal. Our smart matching suggests the best profiles for your project.</p>  
    </div>  
    <div class="step-card reveal">  
      <div class="step-num">03</div>  
      <div class="step-icon">💸</div>  
      <h3 class="step-title">Deliver & Pay</h3>  
      <p class="step-desc">Work gets done, client approves, funds are released. We only take our commission when both parties are happy.</p>  
    </div>  
  </div>  
</section>  
  
<!-- CATEGORIES -->  
  
<section class="categories-section" id="categories">  
  <span class="section-label">Categories</span>  
  <h2 class="section-title">Every digital service, one platform</h2>  
  <div class="cats-grid">  
    <div class="cat-card">  
      <div class="cat-icon">🎨</div>  
      <div class="cat-name">Design & Creative</div>  
      <div class="cat-count">8,400+ freelancers</div>  
    </div>  
    <div class="cat-card">  
      <div class="cat-icon">💻</div>  
      <div class="cat-name">Development</div>  
      <div class="cat-count">12,000+ freelancers</div>  
    </div>  
    <div class="cat-card">  
      <div class="cat-icon">📱</div>  
      <div class="cat-name">Mobile Apps</div>  
      <div class="cat-count">5,200+ freelancers</div>  
    </div>  
    <div class="cat-card">  
      <div class="cat-icon">✍️</div>  
      <div class="cat-name">Writing & Translation</div>  
      <div class="cat-count">6,800+ freelancers</div>  
    </div>  
    <div class="cat-card">  
      <div class="cat-icon">📊</div>  
      <div class="cat-name">Marketing & SEO</div>  
      <div class="cat-count">4,500+ freelancers</div>  
    </div>  
    <div class="cat-card">  
      <div class="cat-icon">🎬</div>  
      <div class="cat-name">Video & Animation</div>  
      <div class="cat-count">3,100+ freelancers</div>  
    </div>  
    <div class="cat-card">  
      <div class="cat-icon">🤖</div>  
      <div class="cat-name">AI & Automation</div>  
      <div class="cat-count">2,900+ freelancers</div>  
    </div>  
    <div class="cat-card">  
      <div class="cat-icon">🔊</div>  
      <div class="cat-name">Audio & Music</div>  
      <div class="cat-count">1,800+ freelancers</div>  
    </div>  
  </div>  
</section>  
  
<!-- SPLIT FOR YOU -->  
  
<section class="split-section" id="for-you">  
  <div class="split-left">  
    <div class="split-icon">🏢</div>  
    <h3 class="split-title">I'm a Client</h3>  
    <p class="split-desc">Find the perfect freelancer for any project — fast. Browse verified profiles, read real reviews, and hire with confidence.</p>  
    <ul class="feature-list">  
      <li>Post a job for free</li>  
      <li>Get proposals within hours</li>  
      <li>Pay only when satisfied</li>  
      <li>24/7 dispute resolution</li>  
    </ul>  
    <a href="#" class="btn btn-accent btn-lg">Post a Project →</a>  
  </div>  
  <div class="split-right">  
    <div class="split-icon">🚀</div>  
    <h3 class="split-title">I'm a Freelancer</h3>  
    <p class="split-desc">Showcase your skills to a global audience. Build your reputation, grow your income, and work on your own terms.</p>  
    <ul class="feature-list">  
      <li>Free profile creation</li>  
      <li>Global client access</li>  
      <li>Secure, fast payments</li>  
      <li>Zero upfront cost</li>  
    </ul>  
    <a href="#" class="btn btn-primary btn-lg" style="background:var(--accent2)">Start Earning →</a>  
  </div>  
</section>  
  
<!-- TESTIMONIALS -->  
  
<section class="testimonials">  
  <div class="reveal" style="text-align:center">  
    <span class="section-label">Testimonials</span>  
    <h2 class="section-title" style="margin:0 auto; text-align:center">Trusted by thousands worldwide</h2>  
  </div>  
  <div class="testi-grid">  
    <div class="testi-card reveal">  
      <div class="testi-quote">"</div>  
      <p class="testi-text">Found an incredible designer within 2 hours of posting. The quality blew me away — and the whole process was seamless.</p>  
      <div class="testi-author">  
        <div class="testi-avatar" style="background:#fff0eb">👩</div>  
        <div>  
          <div class="testi-name">Amina R.</div>  
          <div class="testi-role">Startup Founder, UAE</div>  
        </div>  
      </div>  
    </div>  
    <div class="testi-card reveal">  
      <div class="testi-quote">"</div>  
      <p class="testi-text">As a freelancer, BridgeWork changed my life. I went from local clients to working with companies across Europe and the US.</p>  
      <div class="testi-author">  
        <div class="testi-avatar" style="background:#eff6ff">👨</div>  
        <div>  
          <div class="testi-name">Mehdi K.</div>  
          <div class="testi-role">Full-Stack Dev, Morocco</div>  
        </div>  
      </div>  
    </div>  
    <div class="testi-card reveal">  
      <div class="testi-quote">"</div>  
      <p class="testi-text">The commission-only model is genius. We only pay when we're happy with the result. No risk, no wasted budget.</p>  
      <div class="testi-author">  
        <div class="testi-avatar" style="background:#f5f0ff">👩</div>  
        <div>  
          <div class="testi-name">Léa D.</div>  
          <div class="testi-role">Marketing Director, France</div>  
        </div>  
      </div>  
    </div>  
  </div>  
</section>  
  
<!-- CTA -->  
  
<section class="cta-section">  
  <h2 class="cta-title">Ready to work<br>with the <em>world</em>?</h2>  
  <p class="cta-sub">Join 40,000+ freelancers and clients already growing together on BridgeWork.</p>  
  <div class="cta-btns">  
    <a href="#" class="btn btn-white btn-lg">Start as a Client →</a>  
    <a href="#" class="btn btn-outline-white btn-lg">Join as a Freelancer</a>  
  </div>  
</section>  
  
<!-- PRICING / COMMISSION -->  
  
<section style="padding:6rem 4rem; background:white;">  
  <div style="text-align:center; margin-bottom:3rem">  
    <span style="font-size:0.75rem; font-weight:600; letter-spacing:0.12em; text-transform:uppercase; color:#ff4d1c">Pricing</span>  
    <h2 style="font-family:'Syne',sans-serif; font-size:2.5rem; font-weight:800; letter-spacing:-0.03em; margin-top:0.75rem">Simple & transparent fees</h2>  
    <p style="color:#8a8680; margin-top:0.75rem; font-size:1rem">You only pay when a deal is done. No hidden fees.</p>  
  </div>  
  
  <div style="display:grid; grid-template-columns:repeat(3,1fr); gap:1.5rem; max-width:900px; margin:0 auto">  
  
```  
<!-- Client -->  
<div style="border:1px solid #e2dfd8; border-radius:20px; padding:2.5rem 2rem; text-align:center; transition:transform 0.3s" onmouseover="this.style.transform='translateY(-6px)'" onmouseout="this.style.transform='none'">  
  <div style="font-size:2rem; margin-bottom:1rem">🏢</div>  
  <h3 style="font-family:'Syne',sans-serif; font-weight:800; font-size:1.2rem; margin-bottom:0.5rem">Client</h3>  
  <div style="font-family:'Syne',sans-serif; font-size:3rem; font-weight:800; color:#ff4d1c; line-height:1">10%</div>  
  <div style="color:#8a8680; font-size:0.85rem; margin:0.5rem 0 1.5rem">de la valeur du deal</div>  
  <ul style="list-style:none; text-align:left; display:flex; flex-direction:column; gap:0.6rem">  
    <li style="font-size:0.85rem; display:flex; gap:0.5rem; align-items:center"><span style="color:#ff4d1c">✓</span> Postez gratuitement</li>  
    <li style="font-size:0.85rem; display:flex; gap:0.5rem; align-items:center"><span style="color:#ff4d1c">✓</span> Choisissez le meilleur profil</li>  
    <li style="font-size:0.85rem; display:flex; gap:0.5rem; align-items:center"><span style="color:#ff4d1c">✓</span> Payez à la livraison</li>  
  </ul>  
</div>  
  
<!-- Exemple deal -->  
<div style="border:2px solid #ff4d1c; border-radius:20px; padding:2.5rem 2rem; text-align:center; background:#fff8f6; position:relative">  
  <div style="position:absolute; top:-14px; left:50%; transform:translateX(-50%); background:#ff4d1c; color:white; padding:0.3rem 1rem; border-radius:100px; font-size:0.75rem; font-weight:700; white-space:nowrap">Exemple concret</div>  
  <div style="font-size:2rem; margin-bottom:1rem">💡</div>  
  <h3 style="font-family:'Syne',sans-serif; font-weight:800; font-size:1.1rem; margin-bottom:1.5rem">Deal de 1000 dh</h3>  
  <div style="display:flex; flex-direction:column; gap:0.75rem; text-align:left">  
    <div style="display:flex; justify-content:space-between; font-size:0.9rem; padding:0.5rem 0; border-bottom:1px solid #f0ece6">  
      <span style="color:#8a8680">Client paie</span>  
      <span style="font-weight:700">1 100 dh</span>  
    </div>  
    <div style="display:flex; justify-content:space-between; font-size:0.9rem; padding:0.5rem 0; border-bottom:1px solid #f0ece6">  
      <span style="color:#8a8680">Freelancer reçoit</span>  
      <span style="font-weight:700">950 dh</span>  
    </div>  
    <div style="display:flex; justify-content:space-between; font-size:0.9rem; padding:0.5rem 0">  
      <span style="color:#8a8680">BridgeWork gagne</span>  
      <span style="font-weight:700; color:#ff4d1c">150 dh 🎯</span>  
    </div>  
  </div>  
</div>  
  
<!-- Freelancer -->  
<div style="border:1px solid #e2dfd8; border-radius:20px; padding:2.5rem 2rem; text-align:center; transition:transform 0.3s" onmouseover="this.style.transform='translateY(-6px)'" onmouseout="this.style.transform='none'">  
  <div style="font-size:2rem; margin-bottom:1rem">🚀</div>  
  <h3 style="font-family:'Syne',sans-serif; font-weight:800; font-size:1.2rem; margin-bottom:0.5rem">Freelancer</h3>  
  <div style="font-family:'Syne',sans-serif; font-size:3rem; font-weight:800; color:#1c6eff; line-height:1">5%</div>  
  <div style="color:#8a8680; font-size:0.85rem; margin:0.5rem 0 1.5rem">de la valeur du deal</div>  
  <ul style="list-style:none; text-align:left; display:flex; flex-direction:column; gap:0.6rem">  
    <li style="font-size:0.85rem; display:flex; gap:0.5rem; align-items:center"><span style="color:#1c6eff">✓</span> Profil gratuit</li>  
    <li style="font-size:0.85rem; display:flex; gap:0.5rem; align-items:center"><span style="color:#1c6eff">✓</span> Clients internationaux</li>  
    <li style="font-size:0.85rem; display:flex; gap:0.5rem; align-items:center"><span style="color:#1c6eff">✓</span> Payé à la livraison</li>  
  </ul>  
</div>  
```  
  
  </div>  
</section>  
  
<!-- CONTACT -->  
  
<section style="background:#f5f3ee; padding:4rem; text-align:center; border-top:1px solid #e2dfd8">  
  <span style="font-size:0.75rem; font-weight:600; letter-spacing:0.12em; text-transform:uppercase; color:#ff4d1c">Contact</span>  
  <h2 style="font-family:'Syne',sans-serif; font-size:2rem; font-weight:800; margin:0.75rem 0 2rem; letter-spacing:-0.02em">Got a question? Reach out directly</h2>  
  <div style="display:flex; gap:1.5rem; justify-content:center; flex-wrap:wrap">  
    <a href="https://wa.me/212675817157" style="display:inline-flex; align-items:center; gap:0.6rem; background:#25d366; color:white; padding:0.9rem 2rem; border-radius:100px; font-weight:600; text-decoration:none; font-size:1rem; transition:opacity 0.2s" onmouseover="this.style.opacity='0.85'" onmouseout="this.style.opacity='1'">  
      💬 WhatsApp: +212 675 817 157  
    </a>  
    <a href="mailto:Ibrahim.safir20@gmail.com" style="display:inline-flex; align-items:center; gap:0.6rem; background:#0a0a0f; color:white; padding:0.9rem 2rem; border-radius:100px; font-weight:600; text-decoration:none; font-size:1rem; transition:opacity 0.2s" onmouseover="this.style.opacity='0.85'" onmouseout="this.style.opacity='1'">  
      ✉️ Ibrahim.safir20@gmail.com  
    </a>  
  </div>  
</section>  
  
<!-- FOOTER -->  
  
<footer>  
  <div>  
    <div class="footer-logo">BridgeWork<span>.</span></div>  
    <div style="font-size:0.75rem; margin-top:0.3rem; color:rgba(255,255,255,0.25)">Founded by Brahim Safir</div>  
  </div>  
  <ul class="footer-links">  
    <li><a href="#">About</a></li>  
    <li><a href="#">Privacy</a></li>  
    <li><a href="#">Terms</a></li>  
    <li><a href="#">Contact</a></li>  
  </ul>  
  <div style="font-size:0.8rem; text-align:right; line-height:1.8">  
    © 2026 BridgeWork · Founded by Brahim Safir<br>  
    <a href="mailto:Ibrahim.safir20@gmail.com" style="color:rgba(255,255,255,0.4); text-decoration:none">Ibrahim.safir20@gmail.com</a><br>  
    <a href="https://wa.me/212675817157" style="color:rgba(255,255,255,0.4); text-decoration:none">WhatsApp: +212 675 817 157</a>  
  </div>  
</footer>  
  
<script>  
  // Scroll reveal  
  const reveals = document.querySelectorAll('.reveal');  
  const observer = new IntersectionObserver((entries) => {  
    entries.forEach((entry, i) => {  
      if (entry.isIntersecting) {  
        setTimeout(() => entry.target.classList.add('visible'), i * 80);  
      }  
    });  
  }, { threshold: 0.1 });  
  reveals.forEach(el => observer.observe(el));  
  
  // Stagger step cards  
  document.querySelectorAll('.step-card').forEach((card, i) => {  
    card.style.transitionDelay = `${i * 0.1}s`;  
  });  
</script>  
  
</body>  
</html>  
