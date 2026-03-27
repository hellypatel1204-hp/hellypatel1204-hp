<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>GitHub Profile README – Helly Patel</title>
<link href="https://fonts.googleapis.com/css2?family=Syne:wght@400;700;800&family=DM+Mono:ital,wght@0,400;0,500;1,400&display=swap" rel="stylesheet">
<style>
  :root {
    --bg: #0b0f1a;
    --surface: #121828;
    --border: #1e2d47;
    --accent: #38bdf8;
    --accent2: #818cf8;
    --accent3: #34d399;
    --text: #e2e8f0;
    --muted: #64748b;
    --glow: rgba(56,189,248,0.18);
  }

  * { box-sizing: border-box; margin: 0; padding: 0; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'DM Mono', monospace;
    min-height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 32px 16px;
  }

  .card {
    width: 100%;
    max-width: 780px;
    background: var(--surface);
    border: 1px solid var(--border);
    border-radius: 20px;
    overflow: hidden;
    box-shadow: 0 0 60px rgba(56,189,248,0.07), 0 40px 80px rgba(0,0,0,0.5);
    animation: fadeUp 0.7s ease both;
  }

  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(30px); }
    to   { opacity: 1; transform: translateY(0); }
  }

  /* ── HEADER ── */
  .header {
    position: relative;
    padding: 48px 40px 32px;
    background: linear-gradient(135deg, #0f1f38 0%, #0b0f1a 60%);
    border-bottom: 1px solid var(--border);
    overflow: hidden;
  }
  .header::before {
    content: '';
    position: absolute;
    top: -80px; right: -80px;
    width: 280px; height: 280px;
    background: radial-gradient(circle, rgba(56,189,248,0.12), transparent 70%);
    border-radius: 50%;
  }
  .header::after {
    content: '';
    position: absolute;
    bottom: -60px; left: 30%;
    width: 200px; height: 200px;
    background: radial-gradient(circle, rgba(129,140,248,0.1), transparent 70%);
    border-radius: 50%;
  }

  .tag {
    display: inline-block;
    background: rgba(56,189,248,0.1);
    border: 1px solid rgba(56,189,248,0.3);
    color: var(--accent);
    font-size: 11px;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    padding: 4px 12px;
    border-radius: 20px;
    margin-bottom: 18px;
    animation: fadeUp 0.7s 0.1s ease both;
  }

  .name {
    font-family: 'Syne', sans-serif;
    font-size: clamp(2rem, 5vw, 3rem);
    font-weight: 800;
    line-height: 1.1;
    background: linear-gradient(135deg, #e2e8f0 30%, var(--accent) 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    animation: fadeUp 0.7s 0.15s ease both;
  }

  .role {
    margin-top: 8px;
    color: var(--muted);
    font-size: 13px;
    letter-spacing: 0.05em;
    animation: fadeUp 0.7s 0.2s ease both;
  }
  .role span { color: var(--accent3); }

  .intro {
    margin-top: 20px;
    font-size: 13.5px;
    line-height: 1.75;
    color: #94a3b8;
    max-width: 520px;
    animation: fadeUp 0.7s 0.25s ease both;
  }

  /* ── BODY ── */
  .body { padding: 32px 40px 40px; }

  .section-title {
    font-family: 'Syne', sans-serif;
    font-size: 11px;
    font-weight: 700;
    letter-spacing: 0.18em;
    text-transform: uppercase;
    color: var(--muted);
    margin-bottom: 16px;
    display: flex;
    align-items: center;
    gap: 10px;
  }
  .section-title::after {
    content: '';
    flex: 1;
    height: 1px;
    background: var(--border);
  }

  /* ── STATUS GRID ── */
  .status-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 12px;
    margin-bottom: 32px;
    animation: fadeUp 0.7s 0.3s ease both;
  }

  .status-item {
    background: rgba(255,255,255,0.03);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 16px 18px;
    transition: border-color 0.2s, background 0.2s;
  }
  .status-item:hover {
    border-color: var(--accent);
    background: rgba(56,189,248,0.04);
  }
  .status-icon { font-size: 18px; margin-bottom: 8px; }
  .status-label {
    font-size: 10px;
    color: var(--muted);
    letter-spacing: 0.1em;
    text-transform: uppercase;
    margin-bottom: 4px;
  }
  .status-value {
    font-family: 'Syne', sans-serif;
    font-size: 13px;
    font-weight: 700;
    color: var(--text);
  }

  /* ── TECH STACK ── */
  .stack-wrap {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    margin-bottom: 32px;
    animation: fadeUp 0.7s 0.35s ease both;
  }

  .badge {
    display: inline-flex;
    align-items: center;
    gap: 6px;
    padding: 6px 14px;
    border-radius: 8px;
    font-size: 12px;
    font-weight: 500;
    border: 1px solid;
    transition: transform 0.15s, box-shadow 0.15s;
    cursor: default;
  }
  .badge:hover {
    transform: translateY(-2px);
    box-shadow: 0 4px 16px rgba(0,0,0,0.3);
  }
  .badge.blue   { color: #38bdf8; border-color: rgba(56,189,248,0.3);  background: rgba(56,189,248,0.08); }
  .badge.purple { color: #818cf8; border-color: rgba(129,140,248,0.3); background: rgba(129,140,248,0.08); }
  .badge.green  { color: #34d399; border-color: rgba(52,211,153,0.3);  background: rgba(52,211,153,0.08); }
  .badge.orange { color: #fb923c; border-color: rgba(251,146,60,0.3);  background: rgba(251,146,60,0.08); }
  .badge.pink   { color: #f472b6; border-color: rgba(244,114,182,0.3); background: rgba(244,114,182,0.08); }

  /* ── STATS ROW ── */
  .stats-row {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 12px;
    margin-bottom: 32px;
    animation: fadeUp 0.7s 0.4s ease both;
  }

  .stat-card {
    background: rgba(255,255,255,0.02);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 20px;
  }
  .stat-card .stat-num {
    font-family: 'Syne', sans-serif;
    font-size: 28px;
    font-weight: 800;
    color: var(--accent);
    line-height: 1;
    margin-bottom: 4px;
  }
  .stat-card .stat-num.purple { color: var(--accent2); }
  .stat-card .stat-num.green  { color: var(--accent3); }
  .stat-card .stat-desc {
    font-size: 11px;
    color: var(--muted);
    letter-spacing: 0.08em;
    text-transform: uppercase;
  }

  /* ── CONNECT ── */
  .connect-row {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    animation: fadeUp 0.7s 0.45s ease both;
  }

  .connect-btn {
    display: inline-flex;
    align-items: center;
    gap: 8px;
    padding: 10px 18px;
    border-radius: 10px;
    font-family: 'DM Mono', monospace;
    font-size: 12px;
    text-decoration: none;
    border: 1px solid var(--border);
    color: var(--text);
    background: rgba(255,255,255,0.03);
    transition: all 0.2s;
  }
  .connect-btn:hover {
    border-color: var(--accent);
    color: var(--accent);
    background: rgba(56,189,248,0.06);
    transform: translateY(-2px);
  }

  /* ── FOOTER ── */
  .footer {
    padding: 16px 40px;
    border-top: 1px solid var(--border);
    display: flex;
    align-items: center;
    justify-content: space-between;
    background: rgba(0,0,0,0.15);
  }
  .footer-left {
    font-size: 11px;
    color: var(--muted);
    letter-spacing: 0.05em;
  }
  .footer-left span { color: var(--accent3); }
  .footer-dots {
    display: flex;
    gap: 6px;
  }
  .dot {
    width: 8px; height: 8px;
    border-radius: 50%;
  }
  .dot-1 { background: var(--accent); opacity: 0.7; animation: pulse 2s 0s ease-in-out infinite; }
  .dot-2 { background: var(--accent2); opacity: 0.7; animation: pulse 2s 0.4s ease-in-out infinite; }
  .dot-3 { background: var(--accent3); opacity: 0.7; animation: pulse 2s 0.8s ease-in-out infinite; }

  @keyframes pulse {
    0%, 100% { transform: scale(1); opacity: 0.7; }
    50% { transform: scale(1.4); opacity: 1; }
  }
</style>
</head>
<body>

<div class="card">

  <!-- HEADER -->
  <div class="header">
    <div class="tag">✦ open to collaborate</div>
    <div class="name">Hey, I'm Helly Patel 👋</div>
    <div class="role">Full-Stack Developer &amp; <span>Lifelong Learner</span></div>
    <p class="intro">
      I build thoughtful, user-focused software — blending clean code with creative problem-solving.
      Passionate about web technologies, open source, and turning ideas into real products.
    </p>
  </div>

  <!-- BODY -->
  <div class="body">

    <!-- STATUS -->
    <div class="section-title">Current status</div>
    <div class="status-grid">
      <div class="status-item">
        <div class="status-icon">🔭</div>
        <div class="status-label">Working on</div>
        <div class="status-value">My next big project</div>
      </div>
      <div class="status-item">
        <div class="status-icon">🌱</div>
        <div class="status-label">Learning</div>
        <div class="status-value">System Design &amp; DevOps</div>
      </div>
      <div class="status-item">
        <div class="status-icon">👯</div>
        <div class="status-label">Open to</div>
        <div class="status-value">Collaboration</div>
      </div>
      <div class="status-item">
        <div class="status-icon">⚡</div>
        <div class="status-label">Fun fact</div>
        <div class="status-value">I debug with coffee ☕</div>
      </div>
    </div>

    <!-- TECH STACK -->
    <div class="section-title">Tech stack</div>
    <div class="stack-wrap">
      <span class="badge blue">⚡ JavaScript</span>
      <span class="badge blue">⚛ React</span>
      <span class="badge green">🟢 Node.js</span>
      <span class="badge blue">🐍 Python</span>
      <span class="badge purple">🎨 Tailwind CSS</span>
      <span class="badge orange">🔥 Firebase</span>
      <span class="badge green">🐘 PostgreSQL</span>
      <span class="badge pink">🐙 Git &amp; GitHub</span>
      <span class="badge purple">🐳 Docker</span>
      <span class="badge blue">☁️ AWS</span>
    </div>

    <!-- STATS -->
    <div class="section-title">GitHub at a glance</div>
    <div class="stats-row">
      <div class="stat-card">
        <div class="stat-num">50+</div>
        <div class="stat-desc">Repositories</div>
      </div>
      <div class="stat-card">
        <div class="stat-num purple">300+</div>
        <div class="stat-desc">Contributions this year</div>
      </div>
    </div>

    <!-- CONNECT -->
    <div class="section-title">Let's connect</div>
    <div class="connect-row">
      <a class="connect-btn" href="#">📧 Email me</a>
      <a class="connect-btn" href="#">💼 LinkedIn</a>
      <a class="connect-btn" href="#">🐦 Twitter / X</a>
      <a class="connect-btn" href="#">🌐 Portfolio</a>
    </div>

  </div>

  <!-- FOOTER -->
  <div class="footer">
    <div class="footer-left">Made with <span>♥</span> by Helly Patel</div>
    <div class="footer-dots">
      <div class="dot dot-1"></div>
      <div class="dot dot-2"></div>
      <div class="dot dot-3"></div>
    </div>
  </div>

</div>

</body>
</html>
