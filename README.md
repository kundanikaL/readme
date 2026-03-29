<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8"/>
<meta name="viewport" content="width=device-width, initial-scale=1.0"/>
<title>Kundanika L — Profile</title>
<link href="https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;500;700&family=Syne:wght@400;600;700;800&display=swap" rel="stylesheet"/>
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }

  :root {
    --bg: #0d0e10;
    --bg2: #14151a;
    --bg3: #1a1b21;
    --border: #242530;
    --text: #e2e3e8;
    --muted: #555668;
    --dim: #888a99;
    --purple: #7c3aed;
    --purple-l: #a78bfa;
    --teal: #06b6d4;
    --green: #10b981;
    --amber: #f59e0b;
    --red: #ef4444;
    --blue: #3b82f6;
  }

  body {
    background: #080909;
    min-height: 100vh;
    display: flex;
    align-items: flex-start;
    justify-content: center;
    padding: 40px 16px;
    font-family: 'Syne', sans-serif;
    color: var(--text);
  }

  .card {
    background: var(--bg);
    border-radius: 20px;
    width: 100%;
    max-width: 860px;
    overflow: hidden;
    border: 1px solid var(--border);
    animation: fadeUp .6s ease both;
  }

  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(24px); }
    to   { opacity: 1; transform: translateY(0); }
  }

  .top-bar {
    height: 3px;
    background: linear-gradient(90deg, #7c3aed 0%, #06b6d4 50%, #10b981 100%);
  }

  /* ── HEADER ── */
  .header { padding: 28px 30px 24px; border-bottom: 1px solid var(--border); }

  .hdr-top { display: flex; align-items: center; gap: 16px; margin-bottom: 14px; }

  .avatar {
    width: 60px; height: 60px; border-radius: 50%;
    background: linear-gradient(135deg, #7c3aed, #06b6d4);
    display: flex; align-items: center; justify-content: center;
    font-weight: 800; font-size: 21px; color: #fff;
    flex-shrink: 0;
    box-shadow: 0 0 0 3px #1e1040;
  }

  .hdr-name { font-size: 26px; font-weight: 800; color: #fff; line-height: 1.15; }
  .hdr-handle { font-family: 'JetBrains Mono', monospace; font-size: 12px; color: var(--muted); margin-top: 3px; }

  .tagline { font-size: 14px; color: var(--dim); line-height: 1.7; margin-bottom: 14px; }

  .badges { display: flex; flex-wrap: wrap; gap: 8px; }
  .badge {
    display: inline-flex; align-items: center; gap: 6px;
    padding: 5px 13px; border-radius: 999px; font-size: 11px; font-weight: 600;
    border: 1px solid; letter-spacing: .01em;
  }
  .badge .dot { width: 6px; height: 6px; border-radius: 50%; display: inline-block; }
  .b-purple { background: #1a0e3a; color: #a78bfa; border-color: #4c2fa0; }
  .b-purple .dot { background: #7c3aed; }
  .b-teal   { background: #041f1a; color: #34d399; border-color: #0a5240; }
  .b-teal   .dot { background: #10b981; }
  .b-amber  { background: #1f1100; color: #fbbf24; border-color: #7a4500; }
  .b-blue   { background: #070f25; color: #60a5fa; border-color: #1d3a80; }

  /* ── STATS ── */
  .stats { display: flex; border-bottom: 1px solid var(--border); }
  .stat { flex: 1; text-align: center; padding: 22px 10px; }
  .stat + .stat { border-left: 1px solid var(--border); }
  .stat-n {
    display: block; font-family: 'JetBrains Mono', monospace;
    font-size: 26px; font-weight: 700; color: #fff; letter-spacing: -.5px;
  }
  .stat-l { display: block; font-size: 11px; color: var(--muted); margin-top: 4px; }

  /* ── ABOUT GRID ── */
  .about { display: grid; grid-template-columns: 1fr 1fr; border-bottom: 1px solid var(--border); }

  .acard {
    padding: 18px 20px 18px 22px;
    border-right: 1px solid var(--border);
    border-bottom: 1px solid var(--border);
    position: relative;
    overflow: hidden;
    transition: background .2s;
  }
  .acard:hover { background: var(--bg2); }
  .acard:nth-child(2n) { border-right: none; }
  .acard:nth-last-child(-n+2) { border-bottom: none; }

  .acard::before {
    content: '';
    position: absolute; left: 0; top: 0; bottom: 0;
    width: 3px;
  }
  .ac-purple::before { background: #7c3aed; }
  .ac-teal::before   { background: #06b6d4; }
  .ac-green::before  { background: #10b981; }
  .ac-amber::before  { background: #f59e0b; }

  .acard-label {
    font-family: 'JetBrains Mono', monospace; font-size: 10px;
    color: var(--muted); letter-spacing: .08em; text-transform: uppercase;
    display: flex; align-items: center; gap: 6px; margin-bottom: 7px;
  }
  .acard-label svg { width: 12px; height: 12px; flex-shrink: 0; }
  .acard-text { font-size: 13px; color: #ccc; line-height: 1.6; }

  /* ── LEETCODE ── */
  .leet-section { padding: 18px 22px; border-bottom: 1px solid var(--border); }
  .leet-row { display: flex; align-items: center; gap: 16px; }
  .leet-icon {
    width: 38px; height: 38px; border-radius: 10px;
    background: #160d00; border: 1px solid #f59e0b44;
    display: flex; align-items: center; justify-content: center; flex-shrink: 0;
  }
  .leet-icon svg { width: 20px; height: 20px; }
  .leet-info { flex: 1; }
  .leet-title { font-size: 14px; font-weight: 600; color: #fff; }
  .leet-sub { font-size: 11px; color: var(--muted); margin-top: 2px; }
  .leet-bars { display: flex; align-items: flex-end; gap: 4px; margin-top: 10px; }
  .lbar { width: 8px; border-radius: 3px; }
  @keyframes barGrow { from { transform: scaleY(0); } to { transform: scaleY(1); } }
  .lbar { transform-origin: bottom; animation: barGrow .5s ease both; }
  .leet-count { text-align: right; flex-shrink: 0; }
  .leet-num { font-family: 'JetBrains Mono', monospace; font-size: 22px; font-weight: 700; color: var(--amber); display: block; }
  .leet-numl { font-size: 10px; color: var(--muted); }

  /* ── TECH STACK ── */
  .tech-section { padding: 18px 22px; border-bottom: 1px solid var(--border); }
  .section-lbl { font-family: 'JetBrains Mono', monospace; font-size: 10px; color: var(--muted); letter-spacing: .08em; margin-bottom: 12px; }
  .pills { display: flex; flex-wrap: wrap; gap: 7px; }
  .pill {
    font-family: 'JetBrains Mono', monospace; font-size: 11px;
    padding: 4px 11px; border-radius: 6px;
    background: var(--bg3); border: 1px solid var(--border);
    color: #aaa; transition: border-color .2s, color .2s;
    cursor: default;
  }
  .pill:hover { border-color: #444; color: #ddd; }

  /* ── GITHUB STATS ── */
  .github-section { padding: 18px 22px; border-bottom: 1px solid var(--border); }
  .github-imgs { display: flex; flex-direction: column; gap: 10px; align-items: flex-start; }
  .github-imgs img { max-width: 100%; border-radius: 8px; }

  /* ── TROPHIES ── */
  .trophies-section { padding: 18px 22px; border-bottom: 1px solid var(--border); }
  .trophies-section img { max-width: 100%; border-radius: 8px; }

  /* ── QUOTE ── */
  .quote-section { padding: 18px 22px; border-bottom: 1px solid var(--border); }
  .quote-section img { max-width: 100%; border-radius: 8px; }

  /* ── TOP REPOS ── */
  .repos-section { padding: 18px 22px; border-bottom: 1px solid var(--border); }
  .repos-section img { max-width: 100%; border-radius: 8px; }

  /* ── SOCIALS ── */
  .socials-section { padding: 18px 22px; border-bottom: 1px solid var(--border); }
  .social-links { display: flex; flex-wrap: wrap; gap: 8px; margin-top: 10px; }
  .social-btn {
    display: inline-flex; align-items: center; gap: 7px;
    padding: 7px 16px; border-radius: 8px;
    font-family: 'JetBrains Mono', monospace; font-size: 12px; font-weight: 500;
    border: 1px solid; text-decoration: none; transition: opacity .2s;
  }
  .social-btn:hover { opacity: .75; }
  .social-btn svg { width: 14px; height: 14px; flex-shrink: 0; }
  .s-blue  { background: #070f25; color: #60a5fa; border-color: #1d3a80; }
  .s-indigo{ background: #0a0b25; color: #818cf8; border-color: #2a2f80; }
  .s-red   { background: #1a0505; color: #f87171; border-color: #7a1515; }

  /* ── FOOTER ── */
  .footer {
    display: flex; align-items: center; justify-content: space-between;
    padding: 14px 22px; background: #0a0b0d; flex-wrap: wrap; gap: 8px;
  }
  .footer-note { font-family: 'JetBrains Mono', monospace; font-size: 10px; color: #333; }
  .visit-badge { font-family: 'JetBrains Mono', monospace; font-size: 10px; color: var(--muted); }

  /* Responsive */
  @media (max-width: 560px) {
    .about { grid-template-columns: 1fr; }
    .acard:nth-child(2n) { border-right: 1px solid var(--border); }
    .acard:nth-last-child(-n+2) { border-bottom: 1px solid var(--border); }
    .acard:last-child { border-bottom: none; }
    .stats { flex-wrap: wrap; }
    .stat { min-width: 50%; }
    .stat:nth-child(2) { border-left: 1px solid var(--border); }
    .stat:nth-child(3) { border-left: none; border-top: 1px solid var(--border); }
    .stat:nth-child(4) { border-top: 1px solid var(--border); }
    .hdr-name { font-size: 22px; }
  }
</style>
</head>
<body>

<div class="card">
  <div class="top-bar"></div>

  <!-- HEADER -->
  <div class="header">
    <div class="hdr-top">
      <div class="avatar">KL</div>
      <div>
        <div class="hdr-name">Kundanika L</div>
        <div class="hdr-handle">@kundanika &middot; she/her</div>
      </div>
    </div>
    <div class="tagline">
      Passionate developer building the future &mdash; one startup idea at a time.<br>
      Turning code into solutions that actually matter.
    </div>
    <div class="badges">
      <span class="badge b-purple"><span class="dot"></span>CSE &middot; AI &amp; ML</span>
      <span class="badge b-teal"><span class="dot"></span>Open to collaborate</span>
      <span class="badge b-amber">B.E. Student</span>
      <span class="badge b-blue">Startup Builder</span>
    </div>
  </div>

  <!-- STATS -->
  <div class="stats">
    <div class="stat">
      <span class="stat-n">500+</span>
      <span class="stat-l">Problems Solved</span>
    </div>
    <div class="stat">
      <span class="stat-n">AI/ML</span>
      <span class="stat-l">Specialisation</span>
    </div>
    <div class="stat">
      <span class="stat-n">&infin;</span>
      <span class="stat-l">Ideas in Queue</span>
    </div>
    <div class="stat">
      <span class="stat-n">0&rarr;1</span>
      <span class="stat-l">Startup Mode</span>
    </div>
  </div>

  <!-- ABOUT GRID -->
  <div class="about">
    <div class="acard ac-purple">
      <div class="acard-label">
        <svg viewBox="0 0 16 16" fill="none"><circle cx="8" cy="8" r="5.5" stroke="#7c3aed" stroke-width="1.4"/><path d="M8 5.5V8l1.5 1.5" stroke="#7c3aed" stroke-width="1.4" stroke-linecap="round"/></svg>
        Working on
      </div>
      <div class="acard-text">Building a startup from ground zero &mdash; product, tech &amp; vision all in one</div>
    </div>
    <div class="acard ac-teal">
      <div class="acard-label">
        <svg viewBox="0 0 16 16" fill="none"><path d="M4.5 7.5a3.5 3.5 0 107 0 3.5 3.5 0 00-7 0z" stroke="#06b6d4" stroke-width="1.4"/><path d="M2 13.5c0-1.5 1.5-2.5 6-2.5s6 1 6 2.5" stroke="#06b6d4" stroke-width="1.4" stroke-linecap="round"/></svg>
        Looking to collaborate
      </div>
      <div class="acard-text">Open source AI/ML projects, startup MVPs &amp; creative dev experiments</div>
    </div>
    <div class="acard ac-green">
      <div class="acard-label">
        <svg viewBox="0 0 16 16" fill="none"><circle cx="8" cy="8" r="5.5" stroke="#10b981" stroke-width="1.4"/><path d="M8 5v3.5l2 1.5" stroke="#10b981" stroke-width="1.4" stroke-linecap="round"/></svg>
        Currently learning
      </div>
      <div class="acard-text">Deep learning, system design, product thinking &amp; startup fundamentals</div>
    </div>
    <div class="acard ac-amber">
      <div class="acard-label">
        <svg viewBox="0 0 16 16" fill="none"><path d="M8 2.5L2.5 12.5h11L8 2.5z" stroke="#f59e0b" stroke-width="1.4" stroke-linejoin="round"/><path d="M8 7v2.5M8 11v.5" stroke="#f59e0b" stroke-width="1.4" stroke-linecap="round"/></svg>
        Looking for help with
      </div>
      <div class="acard-text">Mentorship in startup strategy &amp; connecting with builders who share the vision</div>
    </div>
    <div class="acard ac-purple">
      <div class="acard-label">
        <svg viewBox="0 0 16 16" fill="none"><path d="M3 8h10M9 5l4 3-4 3" stroke="#a78bfa" stroke-width="1.4" stroke-linecap="round" stroke-linejoin="round"/></svg>
        Ask me about
      </div>
      <div class="acard-text">Problem solving, AI/ML concepts, competitive coding &amp; building from scratch</div>
    </div>
    <div class="acard ac-teal">
      <div class="acard-label">
        <svg viewBox="0 0 16 16" fill="none"><path d="M2.5 8.5l3 3 8-7" stroke="#34d399" stroke-width="1.4" stroke-linecap="round" stroke-linejoin="round"/></svg>
        Fun fact
      </div>
      <div class="acard-text">I debug life the same way I debug code &mdash; one error at a time, never giving up</div>
    </div>
  </div>

  <!-- LEETCODE -->
  <div class="leet-section">
    <div class="leet-row">
      <div class="leet-icon">
        <svg viewBox="0 0 24 24" fill="none">
          <path d="M13.5 3.5L6.5 14h7L11 20.5l8.5-11h-7L13.5 3.5z" fill="#f59e0b"/>
        </svg>
      </div>
      <div class="leet-info">
        <div class="leet-title">LeetCode &mdash; DSA Grind</div>
        <div class="leet-sub">Solving problems daily &middot; consistency is the algorithm</div>
        <div class="leet-bars">
          <div class="lbar" style="height:18px;background:#10b981;animation-delay:.1s"></div>
          <div class="lbar" style="height:26px;background:#f59e0b;animation-delay:.15s"></div>
          <div class="lbar" style="height:12px;background:#ef4444;animation-delay:.2s"></div>
          <div class="lbar" style="height:20px;background:#10b981;animation-delay:.25s"></div>
          <div class="lbar" style="height:30px;background:#f59e0b;animation-delay:.3s"></div>
          <div class="lbar" style="height:14px;background:#ef4444;animation-delay:.35s"></div>
          <div class="lbar" style="height:22px;background:#10b981;animation-delay:.4s"></div>
          <div class="lbar" style="height:16px;background:#f59e0b;animation-delay:.45s"></div>
          <div class="lbar" style="height:28px;background:#10b981;animation-delay:.5s"></div>
          <div class="lbar" style="height:10px;background:#ef4444;animation-delay:.55s"></div>
        </div>
      </div>
      <div class="leet-count">
        <span class="leet-num">500+</span>
        <span class="leet-numl">problems solved</span>
      </div>
    </div>
  </div>

  <!-- TECH STACK -->
  <div class="tech-section">
    <div class="section-lbl">// tech stack &amp; tools</div>
    <div class="pills">
      <span class="pill">C</span>
      <span class="pill">JavaScript</span>
      <span class="pill">Kotlin</span>
      <span class="pill">HTML5</span>
      <span class="pill">CSS3</span>
      <span class="pill">Python</span>
      <span class="pill">Angular.js</span>
      <span class="pill">Vue.js</span>
      <span class="pill">Node.js</span>
      <span class="pill">FastAPI</span>
      <span class="pill">Django</span>
      <span class="pill">DjangoREST</span>
      <span class="pill">NestJS</span>
      <span class="pill">Express.js</span>
      <span class="pill">TailwindCSS</span>
      <span class="pill">MongoDB</span>
      <span class="pill">MySQL</span>
      <span class="pill">SQLite</span>
      <span class="pill">TensorFlow</span>
      <span class="pill">PyTorch</span>
      <span class="pill">NumPy</span>
      <span class="pill">Pandas</span>
      <span class="pill">Power BI</span>
      <span class="pill">GitHub</span>
      <span class="pill">GitLab</span>
      <span class="pill">Nginx</span>
      <span class="pill">Canva</span>
      <span class="pill">Pi-Hole</span>
      <span class="pill">Bun</span>
      <span class="pill">Vitest</span>
      <span class="pill">PowerShell</span>
    </div>
  </div>

  <!-- GITHUB STATS -->
  <div class="github-section">
    <div class="section-lbl">// github stats</div>
    <div class="github-imgs">
      <img src="https://github-readme-stats.vercel.app/api?username=kundanikal&theme=dark&hide_border=true&include_all_commits=true&count_private=true" alt="GitHub Stats"/>
      <img src="https://nirzak-streak-stats.vercel.app/?user=kundanikal&theme=dark&hide_border=true" alt="GitHub Streak"/>
      <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=kundanikal&theme=dark&hide_border=true&include_all_commits=true&count_private=true&layout=compact" alt="Top Languages"/>
    </div>
  </div>

  <!-- TROPHIES -->
  <div class="trophies-section">
    <div class="section-lbl">// github trophies</div>
    <img src="https://github-profile-trophy.vercel.app/?username=kundanikal&theme=radical&no-frame=true&no-bg=true&margin-w=4" alt="GitHub Trophies"/>
  </div>

  <!-- DEV QUOTE -->
  <div class="quote-section">
    <div class="section-lbl">// random dev quote</div>
    <img src="https://quotes-github-readme.vercel.app/api?type=horizontal&theme=radical" alt="Dev Quote"/>
  </div>

  <!-- TOP REPOS -->
  <div class="repos-section">
    <div class="section-lbl">// top contributed repos</div>
    <img src="https://github-contributor-stats.vercel.app/api?username=kundanikal&limit=5&theme=dark&combine_all_yearly_contributions=true" alt="Top Contributed Repos"/>
  </div>

  <!-- SOCIALS -->
  <div class="socials-section">
    <div class="section-lbl">// socials</div>
    <div class="social-links">
      <a class="social-btn s-blue" href="https://bsky.app/profile/KUNDANA" target="_blank" rel="noopener">
        <svg viewBox="0 0 24 24" fill="#60a5fa"><circle cx="12" cy="12" r="10"/><path d="M8 9c0 0 4 2 4 6 0-4 4-6 4-6" fill="none" stroke="#070f25" stroke-width="1.5"/></svg>
        Bluesky
      </a>
      <a class="social-btn s-indigo" href="https://behance.net/KUNDANIKA" target="_blank" rel="noopener">
        <svg viewBox="0 0 24 24" fill="#818cf8"><rect width="24" height="24" rx="4"/><text x="4" y="17" font-size="11" font-weight="700" fill="#0a0b25" font-family="sans-serif">Be</text></svg>
        Behance
      </a>
      <a class="social-btn s-red" href="mailto:kundanika808@gmail.com">
        <svg viewBox="0 0 24 24" fill="none" stroke="#f87171" stroke-width="1.8"><rect x="2" y="4" width="20" height="16" rx="2"/><path d="M2 7l10 7 10-7"/></svg>
        Email
      </a>
    </div>
  </div>

  <!-- FOOTER -->
  <div class="footer">
    <span class="footer-note">// goal: build a better future &middot; one commit at a time</span>
    <span class="visit-badge">
      <img src="https://visitcount.itsvg.in/api?id=kundanikal&icon=0&color=0" alt="Visit Count" style="height:18px;vertical-align:middle;border-radius:4px;"/>
    </span>
  </div>

</div>

</body>
</html>
