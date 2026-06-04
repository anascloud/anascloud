
<style>
  @import url('https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@300;400;500;700&family=Syne:wght@400;600;700;800&display=swap');

  :root {
    --primary: #00E5C3;
    --secondary: #FF6B6B;
    --accent: #A78BFA;
    --gold: #FFB84D;
    --bg-1: #0A0E1A;
    --bg-2: #111827;
    --bg-3: #1A2235;
    --border: rgba(0,229,195,0.18);
    --text: #E2E8F0;
    --muted: #64748B;
    --card-bg: rgba(17,24,39,0.9);
  }

  * { box-sizing: border-box; margin: 0; padding: 0; }

  body {
    background: var(--bg-1);
    color: var(--text);
    font-family: 'JetBrains Mono', monospace;
    overflow-x: hidden;
  }

  .readme-wrap {
    max-width: 860px;
    margin: 0 auto;
    padding: 20px 16px 40px;
  }

  /* ─── HERO ─── */
  .hero {
    position: relative;
    border: 1px solid var(--border);
    border-radius: 16px;
    padding: 36px 32px 32px;
    margin-bottom: 24px;
    background: linear-gradient(135deg, #0A0E1A 60%, #0d1a2e);
    overflow: hidden;
  }
  .hero::before {
    content: '';
    position: absolute;
    top: -80px; right: -80px;
    width: 300px; height: 300px;
    border-radius: 50%;
    background: radial-gradient(circle, rgba(0,229,195,0.08) 0%, transparent 70%);
    pointer-events: none;
  }
  .hero-top {
    display: flex;
    align-items: flex-start;
    gap: 20px;
    margin-bottom: 20px;
  }
  .avatar {
    width: 72px; height: 72px;
    border-radius: 14px;
    border: 2px solid var(--primary);
    background: var(--bg-3);
    display: flex; align-items: center; justify-content: center;
    font-family: 'Syne', sans-serif;
    font-size: 24px;
    font-weight: 800;
    color: var(--primary);
    flex-shrink: 0;
    position: relative;
    overflow: hidden;
  }
  .avatar::after {
    content: '';
    position: absolute; inset: 0;
    background: linear-gradient(135deg, rgba(0,229,195,0.15), transparent);
  }
  .hero-text { flex: 1; }
  .hero-prompt {
    font-size: 11px;
    color: var(--primary);
    letter-spacing: 0.12em;
    text-transform: uppercase;
    margin-bottom: 4px;
    opacity: 0.7;
  }
  .hero-name {
    font-family: 'Syne', sans-serif;
    font-size: 28px;
    font-weight: 800;
    color: #fff;
    line-height: 1.1;
    margin-bottom: 6px;
  }
  .hero-name span { color: var(--primary); }
  .hero-role {
    font-size: 12px;
    color: var(--muted);
    letter-spacing: 0.04em;
  }
  .hero-role strong { color: var(--accent); font-weight: 500; }
  .hero-badges {
    display: flex; gap: 8px; flex-wrap: wrap;
    margin-bottom: 20px;
  }
  .badge {
    font-size: 10px;
    padding: 3px 10px;
    border-radius: 100px;
    letter-spacing: 0.06em;
    text-transform: uppercase;
    border: 1px solid;
    font-weight: 500;
  }
  .badge-green { color: var(--primary); border-color: rgba(0,229,195,0.3); background: rgba(0,229,195,0.06); }
  .badge-purple { color: var(--accent); border-color: rgba(167,139,250,0.3); background: rgba(167,139,250,0.06); }
  .badge-red { color: var(--secondary); border-color: rgba(255,107,107,0.3); background: rgba(255,107,107,0.06); }
  .badge-gold { color: var(--gold); border-color: rgba(255,184,77,0.3); background: rgba(255,184,77,0.06); }

  .hero-bio {
    font-size: 12px;
    line-height: 1.75;
    color: #94A3B8;
    max-width: 600px;
    border-left: 2px solid var(--primary);
    padding-left: 14px;
    margin-bottom: 20px;
  }
  .hero-links {
    display: flex; gap: 16px; flex-wrap: wrap;
  }
  .hero-link {
    font-size: 11px;
    color: var(--muted);
    text-decoration: none;
    display: flex; align-items: center; gap: 6px;
    transition: color 0.2s;
  }
  .hero-link:hover { color: var(--primary); }
  .hero-link i { font-size: 14px; }

  /* ─── SECTION TITLE ─── */
  .section-label {
    display: flex;
    align-items: center;
    gap: 8px;
    margin-bottom: 12px;
  }
  .section-label span {
    font-size: 10px;
    text-transform: uppercase;
    letter-spacing: 0.14em;
    color: var(--primary);
    font-weight: 700;
  }
  .section-label::after {
    content: '';
    flex: 1;
    height: 1px;
    background: var(--border);
  }

  /* ─── STAT CARDS ─── */
  .stats-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(160px, 1fr));
    gap: 12px;
    margin-bottom: 24px;
  }
  .stat-card {
    background: var(--card-bg);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 16px;
    position: relative;
    overflow: hidden;
  }
  .stat-card::before {
    content: '';
    position: absolute;
    top: 0; left: 0; right: 0;
    height: 2px;
  }
  .stat-card.c-teal::before { background: linear-gradient(90deg, var(--primary), transparent); }
  .stat-card.c-purple::before { background: linear-gradient(90deg, var(--accent), transparent); }
  .stat-card.c-red::before { background: linear-gradient(90deg, var(--secondary), transparent); }
  .stat-card.c-gold::before { background: linear-gradient(90deg, var(--gold), transparent); }
  .stat-card.c-blue::before { background: linear-gradient(90deg, #60A5FA, transparent); }
  .stat-card.c-pink::before { background: linear-gradient(90deg, #F472B6, transparent); }

  .stat-label {
    font-size: 10px;
    color: var(--muted);
    text-transform: uppercase;
    letter-spacing: 0.1em;
    margin-bottom: 6px;
  }
  .stat-val {
    font-family: 'Syne', sans-serif;
    font-size: 26px;
    font-weight: 800;
    line-height: 1;
    margin-bottom: 2px;
  }
  .stat-card.c-teal .stat-val { color: var(--primary); }
  .stat-card.c-purple .stat-val { color: var(--accent); }
  .stat-card.c-red .stat-val { color: var(--secondary); }
  .stat-card.c-gold .stat-val { color: var(--gold); }
  .stat-card.c-blue .stat-val { color: #60A5FA; }
  .stat-card.c-pink .stat-val { color: #F472B6; }

  .stat-sub {
    font-size: 10px;
    color: var(--muted);
  }

  /* ─── SKILLS GRID ─── */
  .skills-section { margin-bottom: 24px; }
  .skill-row { margin-bottom: 14px; }
  .skill-row-header {
    display: flex; justify-content: space-between; align-items: center;
    margin-bottom: 6px;
  }
  .skill-name {
    font-size: 11px;
    color: var(--text);
    display: flex; align-items: center; gap: 6px;
  }
  .skill-name i { font-size: 13px; }
  .skill-pct {
    font-size: 10px;
    color: var(--muted);
  }
  .skill-bar-bg {
    height: 5px;
    background: var(--bg-3);
    border-radius: 100px;
    overflow: hidden;
  }
  .skill-bar-fill {
    height: 100%;
    border-radius: 100px;
    transition: width 1s ease;
  }
  .f-teal { background: linear-gradient(90deg, var(--primary), #00B4A0); }
  .f-purple { background: linear-gradient(90deg, var(--accent), #7C3AED); }
  .f-red { background: linear-gradient(90deg, var(--secondary), #DC2626); }
  .f-gold { background: linear-gradient(90deg, var(--gold), #D97706); }
  .f-blue { background: linear-gradient(90deg, #60A5FA, #2563EB); }

  /* ─── GITHUB CARDS ─── */
  .github-section { margin-bottom: 24px; }
  .github-cards { display: grid; grid-template-columns: 1fr 1fr; gap: 12px; }
  .github-card {
    background: var(--card-bg);
    border: 1px solid var(--border);
    border-radius: 12px;
    overflow: hidden;
  }
  .github-card img { width: 100%; display: block; }
  .github-card-wide { grid-column: 1 / -1; }
  .github-lang-card {
    background: var(--card-bg);
    border: 1px solid var(--border);
    border-radius: 12px;
    overflow: hidden;
    margin-top: 12px;
  }
  .github-lang-card img { width: 100%; display: block; }

  /* ─── TECH STACK PILLS ─── */
  .stack-section { margin-bottom: 24px; }
  .stack-group { margin-bottom: 14px; }
  .stack-group-label {
    font-size: 10px;
    color: var(--muted);
    text-transform: uppercase;
    letter-spacing: 0.1em;
    margin-bottom: 8px;
  }
  .stack-pills { display: flex; flex-wrap: wrap; gap: 6px; }
  .pill {
    font-size: 10px;
    padding: 4px 10px;
    border-radius: 6px;
    background: var(--bg-3);
    border: 1px solid rgba(255,255,255,0.07);
    color: #94A3B8;
    display: flex; align-items: center; gap: 5px;
    cursor: default;
    transition: all 0.2s;
  }
  .pill:hover {
    background: rgba(0,229,195,0.08);
    border-color: rgba(0,229,195,0.25);
    color: var(--primary);
  }
  .pill img { width: 14px; height: 14px; object-fit: contain; }

  /* ─── ACTIVITY HEATMAP PLACEHOLDER ─── */
  .heatmap-section { margin-bottom: 24px; }
  .heatmap-card {
    background: var(--card-bg);
    border: 1px solid var(--border);
    border-radius: 12px;
    overflow: hidden;
  }
  .heatmap-card img { width: 100%; display: block; }

  /* ─── FOOTER ─── */
  .footer-bar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    font-size: 10px;
    color: var(--muted);
    padding-top: 16px;
    border-top: 1px solid var(--border);
    flex-wrap: wrap;
    gap: 8px;
  }
  .footer-bar a { color: var(--primary); text-decoration: none; }

  /* ─── STREAK / TROPHIES ─── */
  .extra-section { margin-bottom: 24px; }
  .extra-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 12px; }
  .extra-card {
    background: var(--card-bg);
    border: 1px solid var(--border);
    border-radius: 12px;
    overflow: hidden;
  }
  .extra-card img { width: 100%; display: block; }
  .extra-wide { grid-column: 1 / -1; }

  /* ─── TYPING CURSOR ─── */
  .cursor {
    display: inline-block;
    width: 2px; height: 1em;
    background: var(--primary);
    animation: blink 1s steps(1) infinite;
    vertical-align: middle;
    margin-left: 2px;
  }
  @keyframes blink { 50% { opacity: 0; } }

  /* ─── PROFILE VIEWS BADGE ─── */
  .profile-meta {
    display: flex; gap: 8px; flex-wrap: wrap; align-items: center;
    margin-bottom: 16px;
  }
  .meta-chip {
    font-size: 10px;
    background: var(--bg-3);
    border: 1px solid var(--border);
    border-radius: 6px;
    padding: 3px 10px;
    color: var(--muted);
    display: flex; align-items: center; gap: 5px;
  }
  .meta-chip i { font-size: 12px; }
  .dot-online {
    width: 6px; height: 6px;
    border-radius: 50%;
    background: var(--primary);
    animation: pulse 2s ease-in-out infinite;
    flex-shrink: 0;
  }
  @keyframes pulse {
    0%, 100% { opacity: 1; transform: scale(1); }
    50% { opacity: 0.5; transform: scale(0.7); }
  }
</style>

<h2 class="sr-only" style="position:absolute;width:1px;height:1px;overflow:hidden;clip:rect(0,0,0,0)">Anas Bin Sabiet — Senior Full Stack Developer GitHub Profile README</h2>

<div class="readme-wrap">

  <!-- HERO -->
  <div class="hero">
    <div class="hero-top">
      <div class="avatar">AB</div>
      <div class="hero-text">
        <div class="hero-prompt">// @anascloud</div>
        <div class="hero-name">Anas Bin <span>Sabiet</span><span class="cursor"></span></div>
        <div class="hero-role"><strong>Senior Full Stack Engineer</strong> · Dhaka, Bangladesh 🇧🇩</div>
      </div>
    </div>
    <div class="profile-meta">
      <div class="meta-chip"><div class="dot-online"></div>Available for work</div>
      <div class="meta-chip"><i class="ti ti-clock" aria-hidden="true"></i>GMT+6 (BDT)</div>
      <div class="meta-chip"><i class="ti ti-mail" aria-hidden="true"></i>anasbinsabiet@gmail.com</div>
      <div class="meta-chip"><i class="ti ti-world" aria-hidden="true"></i>anascloud.blogspot.com</div>
    </div>
    <div class="hero-badges">
      <span class="badge badge-green">Laravel Expert</span>
      <span class="badge badge-purple">React / Next.js</span>
      <span class="badge badge-red">Flutter / Dart</span>
      <span class="badge badge-gold">9+ Yrs Experience</span>
      <span class="badge badge-green">Open Source</span>
    </div>
    <div class="hero-bio">
      Full Stack Developer with 9 years of building enterprise-grade systems — ERP, CRM, POS, inventory, accounting, vehicle & farm management. I architect scalable solutions from database schema to pixel-perfect UI, delivering across Laravel, React, Next.js, Flutter, and cloud infrastructure.
    </div>
    <div class="hero-links">
      <a class="hero-link" href="https://github.com/anascloud"><i class="ti ti-brand-github" aria-hidden="true"></i>anascloud</a>
      <a class="hero-link" href="https://linkedin.com/in/anasbd"><i class="ti ti-brand-linkedin" aria-hidden="true"></i>anasbd</a>
      <a class="hero-link" href="https://discord.com/users/anasbinsabiet"><i class="ti ti-brand-discord" aria-hidden="true"></i>anasbinsabiet</a>
      <a class="hero-link" href="http://anascloud.blogspot.com"><i class="ti ti-notebook" aria-hidden="true"></i>portfolio</a>
    </div>
  </div>

  <!-- STATS GRID -->
  <div class="section-label"><span>// stats</span></div>
  <div class="stats-grid">
    <div class="stat-card c-teal">
      <div class="stat-label">Experience</div>
      <div class="stat-val">9+</div>
      <div class="stat-sub">years in production</div>
    </div>
    <div class="stat-card c-purple">
      <div class="stat-label">Projects shipped</div>
      <div class="stat-val">300+</div>
      <div class="stat-sub">websites & software</div>
    </div>
    <div class="stat-card c-gold">
      <div class="stat-label">Tech stack</div>
      <div class="stat-val">40+</div>
      <div class="stat-sub">tools & frameworks</div>
    </div>
    <div class="stat-card c-red">
      <div class="stat-label">Domains</div>
      <div class="stat-val">8+</div>
      <div class="stat-sub">ERP, CRM, POS, FM…</div>
    </div>
    <div class="stat-card c-blue">
      <div class="stat-label">Languages</div>
      <div class="stat-val">10+</div>
      <div class="stat-sub">programming langs</div>
    </div>
    <div class="stat-card c-pink">
      <div class="stat-label">Commits (est.)</div>
      <div class="stat-val">5k+</div>
      <div class="stat-sub">across all repos</div>
    </div>
  </div>

  <!-- SKILL PROFICIENCY -->
  <div class="skills-section">
    <div class="section-label"><span>// proficiency</span></div>
    <div style="display:grid; grid-template-columns: 1fr 1fr; gap: 0 32px;">
      <div>
        <div class="skill-row">
          <div class="skill-row-header">
            <span class="skill-name"><i class="ti ti-brand-php" aria-hidden="true"></i>Laravel / PHP</span>
            <span class="skill-pct">97%</span>
          </div>
          <div class="skill-bar-bg"><div class="skill-bar-fill f-teal" style="width:97%"></div></div>
        </div>
        <div class="skill-row">
          <div class="skill-row-header">
            <span class="skill-name"><i class="ti ti-brand-react" aria-hidden="true"></i>React / Next.js</span>
            <span class="skill-pct">90%</span>
          </div>
          <div class="skill-bar-bg"><div class="skill-bar-fill f-purple" style="width:90%"></div></div>
        </div>
        <div class="skill-row">
          <div class="skill-row-header">
            <span class="skill-name"><i class="ti ti-device-mobile" aria-hidden="true"></i>Flutter / Dart</span>
            <span class="skill-pct">88%</span>
          </div>
          <div class="skill-bar-bg"><div class="skill-bar-fill f-red" style="width:88%"></div></div>
        </div>
        <div class="skill-row">
          <div class="skill-row-header">
            <span class="skill-name"><i class="ti ti-database" aria-hidden="true"></i>MySQL / Oracle</span>
            <span class="skill-pct">92%</span>
          </div>
          <div class="skill-bar-bg"><div class="skill-bar-fill f-gold" style="width:92%"></div></div>
        </div>
      </div>
      <div>
        <div class="skill-row">
          <div class="skill-row-header">
            <span class="skill-name"><i class="ti ti-brand-nodejs" aria-hidden="true"></i>Node / NestJS</span>
            <span class="skill-pct">82%</span>
          </div>
          <div class="skill-bar-bg"><div class="skill-bar-fill f-teal" style="width:82%"></div></div>
        </div>
        <div class="skill-row">
          <div class="skill-row-header">
            <span class="skill-name"><i class="ti ti-brand-docker" aria-hidden="true"></i>Docker / K8s</span>
            <span class="skill-pct">78%</span>
          </div>
          <div class="skill-bar-bg"><div class="skill-bar-fill f-blue" style="width:78%"></div></div>
        </div>
        <div class="skill-row">
          <div class="skill-row-header">
            <span class="skill-name"><i class="ti ti-brand-python" aria-hidden="true"></i>Python / Django</span>
            <span class="skill-pct">75%</span>
          </div>
          <div class="skill-bar-bg"><div class="skill-bar-fill f-purple" style="width:75%"></div></div>
        </div>
        <div class="skill-row">
          <div class="skill-row-header">
            <span class="skill-name"><i class="ti ti-cloud" aria-hidden="true"></i>AWS / GCP / Azure</span>
            <span class="skill-pct">80%</span>
          </div>
          <div class="skill-bar-bg"><div class="skill-bar-fill f-gold" style="width:80%"></div></div>
        </div>
      </div>
    </div>
  </div>

  <!-- GITHUB STATS CARDS -->
  <div class="github-section">
    <div class="section-label"><span>// github stats</span></div>
    <div class="github-cards">
      <div class="github-card">
        <img src="https://github-readme-stats.vercel.app/api?username=anascloud&show_icons=true&count_private=true&hide_border=true&title_color=00E5C3&text_color=E2E8F0&icon_color=A78BFA&bg_color=0d1117&ring_color=00E5C3&include_all_commits=true&show=reviews,discussions_started,discussions_answered,prs_merged,prs_merged_percentage" alt="Anas GitHub Stats" loading="lazy" />
      </div>
      <div class="github-card">
        <img src="https://github-readme-streak-stats.herokuapp.com/?user=anascloud&hide_border=true&stroke=00E5C3&background=0d1117&ring=00E5C3&fire=FF6B6B&currStreakNum=E2E8F0&currStreakLabel=00E5C3&sideNums=E2E8F0&sideLabels=64748B&dates=64748B" alt="GitHub Streak" loading="lazy" />
      </div>
    </div>
    <div class="github-lang-card" style="margin-top:12px">
      <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=anascloud&layout=compact&hide_border=true&title_color=00E5C3&text_color=E2E8F0&bg_color=0d1117&langs_count=12&card_width=860" alt="Top Languages" loading="lazy" />
    </div>
  </div>

  <!-- TROPHIES -->
  <div class="extra-section">
    <div class="section-label"><span>// achievements</span></div>
    <div style="background: var(--card-bg); border: 1px solid var(--border); border-radius: 12px; overflow: hidden;">
      <img src="https://github-profile-trophy.vercel.app/?username=anascloud&theme=darkhub&no-frame=true&no-bg=true&margin-w=6&margin-h=6&column=7&title=Stars,Followers,Commits,Repositories,PullRequest,Issues,Reviews" alt="GitHub Trophies" loading="lazy" style="width:100%; display:block;" />
    </div>
  </div>

  <!-- ACTIVITY GRAPH -->
  <div class="heatmap-section">
    <div class="section-label"><span>// contribution graph</span></div>
    <div class="heatmap-card">
      <img src="https://github-readme-activity-graph.vercel.app/graph?username=anascloud&bg_color=0d1117&color=00E5C3&line=A78BFA&point=FF6B6B&area=true&hide_border=true" alt="Activity Graph" loading="lazy" />
    </div>
  </div>

  <!-- TECH STACK -->
  <div class="stack-section">
    <div class="section-label"><span>// tech stack</span></div>

    <div class="stack-group">
      <div class="stack-group-label">backend</div>
      <div class="stack-pills">
        <span class="pill"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/laravel-colored.svg" alt=""/>Laravel</span>
        <span class="pill"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/php-colored.svg" alt=""/>PHP</span>
        <span class="pill"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/nodejs-colored.svg" alt=""/>Node.js</span>
        <span class="pill"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/nestjs-colored.svg" alt=""/>NestJS</span>
        <span class="pill"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/python-colored.svg" alt=""/>Python</span>
        <span class="pill"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/django-colored-dark.svg" alt=""/>Django</span>
        <span class="pill"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/graphql-colored.svg" alt=""/>GraphQL</span>
        <span class="pill"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/fastapi-colored.svg" alt=""/>FastAPI</span>
      </div>
    </div>

    <div class="stack-group">
      <div class="stack-group-label">frontend</div>
      <div class="stack-pills">
        <span class="pill"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/react-colored.svg" alt=""/>React</span>
        <span class="pill"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/nextjs-colored-dark.svg" alt=""/>Next.js</span>
        <span class="pill"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/typescript-colored.svg" alt=""/>TypeScript</span>
        <span class="pill"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/vuejs-colored.svg" alt=""/>Vue</span>
        <span class="pill"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/tailwindcss-colored.svg" alt=""/>Tailwind</span>
        <span class="pill"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/redux-colored.svg" alt=""/>Redux</span>
        <span class="pill"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/materialui-colored.svg" alt=""/>MUI</span>
        <span class="pill"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/shadcnui-colored-dark.svg" alt=""/>shadcn/ui</span>
      </div>
    </div>

    <div class="stack-group">
      <div class="stack-group-label">mobile & database</div>
      <div class="stack-pills">
        <span class="pill"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/flutter-colored.svg" alt=""/>Flutter</span>
        <span class="pill"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/dart-colored.svg" alt=""/>Dart</span>
        <span class="pill"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/mysql-colored.svg" alt=""/>MySQL</span>
        <span class="pill"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/postgresql-colored.svg" alt=""/>PostgreSQL</span>
        <span class="pill"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/oracle-colored.svg" alt=""/>Oracle</span>
        <span class="pill"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/mongodb-colored.svg" alt=""/>MongoDB</span>
        <span class="pill"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/firebase-colored.svg" alt=""/>Firebase</span>
        <span class="pill"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/supabase-colored.svg" alt=""/>Supabase</span>
      </div>
    </div>

    <div class="stack-group">
      <div class="stack-group-label">cloud & devops</div>
      <div class="stack-pills">
        <span class="pill"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/docker-colored.svg" alt=""/>Docker</span>
        <span class="pill"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/kubernetes-colored.svg" alt=""/>Kubernetes</span>
        <span class="pill"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/aws-colored-dark.svg" alt=""/>AWS</span>
        <span class="pill"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/googlecloud-colored.svg" alt=""/>GCP</span>
        <span class="pill"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/azure-colored.svg" alt=""/>Azure</span>
        <span class="pill"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/linux-colored.svg" alt=""/>Linux</span>
        <span class="pill"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/ubuntu-colored.svg" alt=""/>Ubuntu</span>
      </div>
    </div>
  </div>

  <!-- FOOTER -->
  <div class="footer-bar">
    <span>Built with <span style="color:var(--secondary)">♥</span> by <a href="https://github.com/anascloud">@anascloud</a></span>
    <span>Profile views: <img src="https://komarev.com/ghpvc/?username=anascloud&style=flat-square&color=00E5C3&label=" alt="profile views" style="vertical-align:middle; height:16px;" /></span>
    <span style="color: var(--muted)">// last updated 2026</span>
  </div>

</div>
