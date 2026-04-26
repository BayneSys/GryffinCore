# GryffinCore
Gryffin Core Repository
<!DOCTYPE html>

<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>The Problem — JBGC</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700;900&family=Source+Sans+3:wght@300;400;600&display=swap" rel="stylesheet">
<style>
  :root {
    --teal: #1a7a6e;
    --orange: #e07b3a;
    --gold: #c9a227;
    --red: #c0392b;
    --dark: #1c1c1c;
    --cream: #faf8f3;
    --light-teal: #e8f5f3;
  }
  * { box-sizing: border-box; margin: 0; padding: 0; }
  body {
    background: var(--cream);
    font-family: 'Source Sans 3', sans-serif;
    color: var(--dark);
    width: 900px;
    margin: 0 auto;
    padding: 0;
  }

.header {
background: var(–dark);
color: white;
padding: 48px 56px 40px;
position: relative;
overflow: hidden;
}
.header::before {
content: ‘’;
position: absolute;
top: -60px; right: -60px;
width: 280px; height: 280px;
border-radius: 50%;
border: 40px solid rgba(255,255,255,0.04);
}
.header::after {
content: ‘’;
position: absolute;
bottom: -80px; left: 40px;
width: 200px; height: 200px;
border-radius: 50%;
border: 30px solid rgba(255,255,255,0.03);
}
.badge {
display: inline-block;
background: var(–orange);
color: white;
font-size: 11px;
font-weight: 600;
letter-spacing: 0.15em;
text-transform: uppercase;
padding: 6px 14px;
border-radius: 2px;
margin-bottom: 18px;
}
.header h1 {
font-family: ‘Playfair Display’, serif;
font-size: 52px;
font-weight: 900;
line-height: 1.1;
margin-bottom: 12px;
}
.header h1 span { color: var(–orange); }
.header p {
font-size: 18px;
font-weight: 300;
color: rgba(255,255,255,0.7);
max-width: 520px;
line-height: 1.6;
}
.card-number {
font-family: ‘Playfair Display’, serif;
font-size: 11px;
font-weight: 700;
letter-spacing: 0.1em;
margin-bottom: 2px;
}

.grid {
display: grid;
grid-template-columns: 1fr 1fr;
gap: 0;
}
.card {
padding: 40px 44px;
border-right: 1px solid rgba(0,0,0,0.07);
border-bottom: 1px solid rgba(0,0,0,0.07);
position: relative;
transition: background 0.2s;
}
.card:nth-child(even) { border-right: none; }

.card-icon {
width: 56px; height: 56px;
border-radius: 50%;
display: flex; align-items: center; justify-content: center;
font-size: 26px;
margin-bottom: 20px;
}
.c1 .card-icon { background: #e8f5f3; }
.c2 .card-icon { background: #fef0e7; }
.c3 .card-icon { background: #fef9e7; }
.c4 .card-icon { background: #fce8e6; }

.c1 .card-number { color: var(–teal); }
.c2 .card-number { color: var(–orange); }
.c3 .card-number { color: var(–gold); }
.c4 .card-number { color: var(–red); }

.card h2 {
font-family: ‘Playfair Display’, serif;
font-size: 22px;
font-weight: 700;
margin-bottom: 4px;
line-height: 1.2;
}
.card .subtitle {
font-size: 13px;
font-weight: 600;
letter-spacing: 0.08em;
text-transform: uppercase;
color: #888;
margin-bottom: 16px;
}
.card p {
font-size: 15px;
line-height: 1.7;
color: #444;
margin-bottom: 20px;
}
.plain-box {
border-radius: 4px;
padding: 14px 16px;
font-size: 14px;
font-weight: 600;
line-height: 1.5;
}
.c1 .plain-box { background: var(–light-teal); color: var(–teal); }
.c2 .plain-box { background: #fef0e7; color: #b85c1a; }
.c3 .plain-box { background: #fefce8; color: #9a7a10; }
.c4 .plain-box { background: #fce8e6; color: #a02319; }

.plain-label {
font-size: 10px;
font-weight: 700;
letter-spacing: 0.12em;
text-transform: uppercase;
margin-bottom: 5px;
opacity: 0.6;
}

.root-issue {
background: var(–dark);
color: white;
padding: 44px 56px;
position: relative;
overflow: hidden;
}
.root-issue::before {
content: ‘’;
position: absolute;
right: -30px; top: 50%;
transform: translateY(-50%);
width: 220px; height: 220px;
border-radius: 50%;
background: rgba(26,122,110,0.15);
}
.root-issue .label {
font-size: 11px;
font-weight: 700;
letter-spacing: 0.15em;
text-transform: uppercase;
color: var(–teal);
margin-bottom: 14px;
}
.root-issue h3 {
font-family: ‘Playfair Display’, serif;
font-size: 26px;
font-weight: 700;
line-height: 1.3;
margin-bottom: 16px;
max-width: 640px;
}
.root-issue h3 em {
font-style: normal;
color: #7ecec4;
}
.root-issue p {
font-size: 15px;
line-height: 1.7;
color: rgba(255,255,255,0.65);
max-width: 600px;
}
.root-issue p strong { color: #7ecec4; font-weight: 600; }

.footer-bar {
background: var(–teal);
padding: 16px 56px;
display: flex;
justify-content: space-between;
align-items: center;
}
.footer-bar span {
color: white;
font-size: 13px;
font-weight: 600;
letter-spacing: 0.05em;
}
.footer-bar .series {
font-size: 12px;
color: rgba(255,255,255,0.6);
letter-spacing: 0.1em;
}
</style>

</head>
<body>

<div class="header">
  <div class="badge">Part 1 of 4</div>
  <h1>Why the World<br>Feels <span>Broken</span></h1>
  <p>Four interconnected conditions keep humanity from thriving — and they're not accidents.</p>
</div>

<div class="grid">
  <div class="card c1">
    <div class="card-icon">🏭</div>
    <div class="card-number">PROBLEM 1</div>
    <h2>Extractive Systems</h2>
    <div class="subtitle">Lack of Sustainability</div>
    <p>Most things are built to break, expire, and be replaced. They rely on exploited labor, resource extraction, and disconnection from land and community.</p>
    <div class="plain-box">
      <div class="plain-label">Plain language</div>
      We are living inside systems that take more than they give.
    </div>
  </div>

  <div class="card c2">
    <div class="card-icon">👥</div>
    <div class="card-number">PROBLEM 2</div>
    <h2>Social Fragmentation</h2>
    <div class="subtitle">Loss of Community</div>
    <p>People are isolated, overwhelmed, and disconnected from shared responsibility and care. This creates loneliness, mistrust, and burnout.</p>
    <div class="plain-box">
      <div class="plain-label">Plain language</div>
      We've forgotten how to live with each other.
    </div>
  </div>

  <div class="card c3">
    <div class="card-icon">🔒</div>
    <div class="card-number">PROBLEM 3</div>
    <h2>Artificial Scarcity</h2>
    <div class="subtitle">Denied Basic Needs</div>
    <p>Despite immense wealth and resources, people still lack food, clean water, housing, and healthcare. This scarcity is not accidental — it is maintained.</p>
    <div class="plain-box">
      <div class="plain-label">Plain language</div>
      The basics for survival exist, but access is controlled.
    </div>
  </div>

  <div class="card c4">
    <div class="card-icon">🔋</div>
    <div class="card-number">PROBLEM 4</div>
    <h2>Systemic Burnout</h2>
    <div class="subtitle">Loss of Energy</div>
    <p>All of the above leads to chronic stress, nervous system dysregulation, and burnout. People don't lack motivation — they lack capacity.</p>
    <div class="plain-box">
      <div class="plain-label">Plain language</div>
      The system drains people faster than they can recover.
    </div>
  </div>
</div>

<div class="root-issue">
  <div class="label">🌱 The Root Issue</div>
  <h3>These conditions come from <em>colonialism, racial capitalism, and white supremacy.</em></h3>
  <p>Decolonization means returning land, power, and decision-making to communities — and rebuilding systems rooted in <strong>care, reciprocity, and interdependence.</strong></p>
</div>

<div class="footer-bar">
  <span>JAX BAYNE | GRYFFIN CORE</span>
  <span class="series">jaxbayne.com · gryffincore.com</span>
</div>

</body>
</html>