<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <!-- SEO & Keywords -->
  <meta name="description" content="Upendra Chary – Full Stack .NET Developer specialized in C#, ASP.NET Core, React, SQL Server, Web API, and production-grade enterprise applications." />
  <meta name="keywords" content="Upendra Chary, Full Stack .NET Developer, C# Developer, ASP.NET Core, React, Web API, SQL Server, MongoDB, Healthcare Applications, Enterprise Software, IIS Deployment" />
  <meta name="author" content="Upendra Chary" />
  <title>Upendra Chary · Full Stack .NET Developer</title>

  <!-- Fonts & Icons -->
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link href="https://fonts.googleapis.com/css2?family=Inter:opsz,wght@14..32,400;14..32,600;14..32,700;14..32,800&family=JetBrains+Mono:wght@400;600;700&display=swap" rel="stylesheet" />
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css" />

  <style>
    /* ----- reset & base ----- */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      background: #020617;
      font-family: 'Inter', sans-serif;
      color: #e2e8f0;
      line-height: 1.6;
      padding: 2rem 1rem;
    }

    .profile-container {
      max-width: 1200px;
      margin: 0 auto;
      background: linear-gradient(145deg, #0f172a 0%, #1e293b 100%);
      border-radius: 3rem;
      padding: 2.5rem 2rem;
      box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.8);
      backdrop-filter: blur(2px);
      border: 1px solid rgba(37, 99, 235, 0.25);
      position: relative;
      overflow: hidden;
    }

    /* animated gradient glow */
    .profile-container::before {
      content: '';
      position: absolute;
      top: -30%;
      left: -20%;
      width: 140%;
      height: 140%;
      background: radial-gradient(circle at 30% 40%, rgba(6, 182, 212, 0.08), transparent 60%);
      z-index: 0;
      animation: ambientGlow 12s ease-in-out infinite alternate;
    }

    @keyframes ambientGlow {
      0% { opacity: 0.3; transform: scale(1) rotate(0deg); }
      100% { opacity: 0.7; transform: scale(1.2) rotate(8deg); }
    }

    .profile-container > * {
      position: relative;
      z-index: 2;
    }

    /* ----- utility ----- */
    .text-center { text-align: center; }
    .flex-center { display: flex; justify-content: center; align-items: center; gap: 0.75rem; flex-wrap: wrap; }
    .gap-2 { gap: 1rem; }
    .mt-2 { margin-top: 1.5rem; }
    .mb-1 { margin-bottom: 1rem; }
    .mb-2 { margin-bottom: 2rem; }

    /* ----- typography & glow ----- */
    .glow-text {
      background: linear-gradient(135deg, #22d3ee, #2563eb, #06b6d4);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      font-weight: 800;
    }

    .terminal-box {
      background: #0b1120;
      border-radius: 1.5rem;
      padding: 1.8rem 1.5rem;
      border: 1px solid #1e3a8a;
      box-shadow: inset 0 0 20px rgba(6, 182, 212, 0.08);
      font-family: 'JetBrains Mono', monospace;
      font-size: 0.95rem;
      line-height: 1.9;
      color: #a5b4fc;
      transition: all 0.2s ease;
    }

    .terminal-box:hover {
      border-color: #22d3ee;
      box-shadow: 0 0 25px rgba(34, 211, 238, 0.15);
    }

    .badge-pill {
      display: inline-block;
      padding: 0.4rem 1.2rem;
      border-radius: 40px;
      font-weight: 600;
      font-size: 0.8rem;
      letter-spacing: 0.5px;
      background: rgba(37, 99, 235, 0.2);
      border: 1px solid #2563eb;
      color: #93c5fd;
      transition: all 0.3s;
    }

    .badge-pill:hover {
      background: #2563eb;
      color: white;
      transform: translateY(-3px);
      box-shadow: 0 8px 20px -6px #2563eb;
    }

    .tech-icon {
      filter: drop-shadow(0 0 6px rgba(34, 211, 238, 0.2));
      transition: transform 0.25s ease, filter 0.3s;
      display: inline-block;
    }

    .tech-icon:hover {
      transform: translateY(-6px) scale(1.05);
      filter: drop-shadow(0 0 18px #22d3ee);
    }

    /* ----- header wave animation (capsule style) ----- */
    .wave-header {
      background: linear-gradient(90deg, #020617, #0f172a, #1e3a8a, #2563eb, #06b6d4);
      background-size: 300% 100%;
      border-radius: 40px;
      padding: 1.6rem 1rem;
      margin-bottom: 2rem;
      animation: waveMove 8s ease-in-out infinite alternate;
      box-shadow: 0 10px 30px -10px #1e3a8a;
    }

    @keyframes waveMove {
      0% { background-position: 0% 50%; }
      100% { background-position: 100% 50%; }
    }

    .wave-header h1 {
      font-size: 3.2rem;
      font-weight: 800;
      letter-spacing: 2px;
      text-shadow: 0 0 20px rgba(6, 182, 212, 0.4);
    }

    .wave-header p {
      font-size: 1.2rem;
      font-weight: 500;
      color: #b6e6f0;
      letter-spacing: 3px;
    }

    /* ----- cards & sections ----- */
    .section-card {
      background: rgba(15, 23, 42, 0.5);
      backdrop-filter: blur(4px);
      border-radius: 2rem;
      padding: 1.8rem 1.8rem;
      border: 1px solid #1e3a8a;
      transition: 0.3s;
    }

    .section-card:hover {
      border-color: #22d3ee;
      box-shadow: 0 0 28px rgba(34, 211, 238, 0.08);
    }

    .skill-grid {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 1.2rem 2rem;
    }

    .skill-item {
      background: #0f172a;
      padding: 0.6rem 1.6rem;
      border-radius: 60px;
      border: 1px solid #1e3a8a;
      font-weight: 600;
      font-size: 0.9rem;
      color: #b9d0f0;
      box-shadow: 0 4px 10px rgba(0,0,0,0.3);
      transition: 0.25s;
    }

    .skill-item i {
      margin-right: 8px;
      color: #22d3ee;
    }

    .skill-item:hover {
      background: #1e293b;
      border-color: #22d3ee;
      transform: scale(1.04);
    }

    /* github stats */
    .stats-wrapper {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 1.5rem;
    }

    .stats-wrapper > * {
      flex: 1 1 280px;
      min-width: 240px;
      border-radius: 1.8rem;
      overflow: hidden;
      transition: 0.3s;
      filter: drop-shadow(0 8px 20px rgba(0,0,0,0.6));
    }

    .stats-wrapper > *:hover {
      transform: scale(1.02);
      filter: drop-shadow(0 0 30px #1e3a8a);
    }

    .stats-wrapper img {
      width: 100%;
      height: auto;
      display: block;
      border-radius: 1.8rem;
    }

    /* snake animation container */
    .snake-box {
      background: #0b1120;
      border-radius: 2.5rem;
      padding: 0.5rem 0.5rem 0 0.5rem;
      border: 1px solid #1e3a8a;
      margin: 2rem 0;
      overflow: hidden;
    }

    .snake-box img {
      width: 100%;
      display: block;
      border-radius: 2rem;
      opacity: 0.95;
    }

    /* social buttons */
    .social-btn {
      display: inline-flex;
      align-items: center;
      gap: 0.6rem;
      background: #0f172a;
      padding: 0.65rem 1.8rem;
      border-radius: 60px;
      border: 1px solid #2563eb;
      color: #e2e8f0;
      font-weight: 600;
      transition: 0.25s;
      text-decoration: none;
      font-size: 0.9rem;
    }

    .social-btn i {
      font-size: 1.2rem;
      color: #22d3ee;
    }

    .social-btn:hover {
      background: #2563eb;
      border-color: #22d3ee;
      transform: translateY(-4px);
      box-shadow: 0 12px 20px -10px #2563eb;
      color: white;
    }

    /* typing animation (svg simulated) */
    .typing-demo {
      display: inline-block;
      border-right: 3px solid #22d3ee;
      white-space: nowrap;
      overflow: hidden;
      animation: typeBlink 0.9s step-end infinite;
      font-weight: 700;
      color: #67e8f9;
    }

    @keyframes typeBlink {
      0%, 100% { border-color: #22d3ee; }
      50% { border-color: transparent; }
    }

    /* responsiveness */
    @media (max-width: 640px) {
      .profile-container { padding: 1.5rem 1rem; }
      .wave-header h1 { font-size: 2.2rem; }
      .wave-header p { font-size: 1rem; }
      .terminal-box { font-size: 0.8rem; padding: 1.2rem; }
    }
  </style>
</head>
<body>

<div class="profile-container">

  <!-- ========== HEADER WAVE ========== -->
  <div class="wave-header text-center">
    <h1 class="glow-text" style="font-size: clamp(2.2rem, 8vw, 3.8rem);">UPENDRA CHARY</h1>
    <p style="color: #bae6fd; font-size: clamp(1rem, 3vw, 1.4rem); letter-spacing: 3px;">
      <i class="fas fa-code" style="color:#22d3ee;"></i> FULL STACK .NET DEVELOPER
    </p>
    <div class="flex-center mt-2 gap-2">
      <span class="badge-pill"><i class="fas fa-cog fa-spin"></i> C# / ASP.NET Core</span>
      <span class="badge-pill"><i class="fas fa-database"></i> SQL / MongoDB</span>
      <span class="badge-pill"><i class="fab fa-react"></i> React</span>
      <span class="badge-pill"><i class="fas fa-cloud"></i> AWS / IIS</span>
    </div>
  </div>

  <!-- ========== TYPING SVG + VIEWS ========== -->
  <div class="text-center mb-2">
    <div style="background: #0b1120; border-radius: 60px; padding: 0.5rem 1.8rem; display: inline-block; border:1px solid #1e3a8a;">
      <span class="typing-demo" style="font-size: 1.2rem; color:#a5f3fc;">
        <i class="fas fa-terminal"></i> &nbsp; Full Stack .NET · React · Cloud
      </span>
    </div>
    <div class="flex-center mt-2">
      <img src="https://komarev.com/ghpvc/?username=upendra505&label=PROFILE%20VIEWS&color=06b6d4&style=for-the-badge" alt="views" style="border-radius:30px;"/>
    </div>
  </div>

  <!-- ========== ABOUT + TERMINAL ========== -->
  <div class="section-card mb-2">
    <div style="display: flex; flex-wrap: wrap; align-items: center; gap: 1.8rem;">
      <div style="flex:2; min-width: 260px;">
        <h2 style="color:#22d3ee; font-weight:700;"><i class="fas fa-user-astronaut"></i> About Upendra Chary</h2>
        <p style="color:#cbd5e1; margin: 0.8rem 0 0.2rem;">
          I'm a <strong style="color:#93c5fd;">Full Stack .NET Developer</strong> with a passion for building production-grade web applications. 
          From <span style="color:#67e8f9;">frontend (React)</span> to <span style="color:#67e8f9;">backend (C# / ASP.NET Core)</span>, 
          REST APIs, databases, and deployment — I cover the entire lifecycle.
        </p>
        <p style="color:#94a3b8; margin-top:0.6rem;">
          <i class="fas fa-check-circle" style="color:#22d3ee;"></i> Healthcare · Enterprise · Admin dashboards · QR & PDF generation · Auth
        </p>
        <div style="display: flex; flex-wrap: wrap; gap: 0.5rem; margin-top: 0.8rem;">
          <span class="skill-item"><i class="fas fa-shield-alt"></i> Auth / RBAC</span>
          <span class="skill-item"><i class="fas fa-file-pdf"></i> PDF / Certificates</span>
          <span class="skill-item"><i class="fas fa-qrcode"></i> QR Codes</span>
          <span class="skill-item"><i class="fas fa-server"></i> IIS / AWS</span>
        </div>
      </div>
      <div style="flex:1.2; min-width: 200px; text-align:center;">
        <img src="https://raw.githubusercontent.com/rajput2107/rajput2107/master/Assets/Developer.gif" alt="dev gif" style="width:100%; max-width:280px; border-radius: 30px; border:2px solid #1e3a8a; box-shadow: 0 0 30px rgba(6,182,212,0.15);"/>
      </div>
    </div>
  </div>

  <!-- ========== TERMINAL BOX ========== -->
  <div class="terminal-box mb-2">
    <pre style="margin:0; white-space: pre-wrap; word-break: break-word;">
╔══════════════════════════════════════════════════════════════╗
║  SYSTEM INITIALIZED                                         ║
║  UPENDRA CHARY  ·  FULL STACK .NET DEVELOPER               ║
║  Backend      → C# / ASP.NET Core / Web API                ║
║  Frontend     → React / JavaScript / TypeScript            ║
║  Database     → SQL Server / MySQL / MongoDB               ║
║  Deployment   → IIS / Windows Server / AWS                 ║
║  STATUS       → 🚀 BUILDING THE FUTURE                     ║
╚══════════════════════════════════════════════════════════════╝
    </pre>
  </div>

  <!-- ========== TECH STACK ========== -->
  <div class="section-card mb-2">
    <h3 class="text-center glow-text" style="font-size:1.8rem;"><i class="fas fa-cubes"></i> Technology Universe</h3>
    <div class="skill-grid mt-2">
      <span class="skill-item"><i class="fab fa-microsoft"></i> C#</span>
      <span class="skill-item"><i class="fas fa-dot-circle"></i> ASP.NET Core</span>
      <span class="skill-item"><i class="fab fa-react"></i> React</span>
      <span class="skill-item"><i class="fab fa-js"></i> JavaScript</span>
      <span class="skill-item"><i class="fab fa-html5"></i> HTML5 / CSS3</span>
      <span class="skill-item"><i class="fas fa-database"></i> SQL Server</span>
      <span class="skill-item"><i class="fas fa-leaf"></i> MongoDB</span>
      <span class="skill-item"><i class="fas fa-cloud"></i> AWS</span>
      <span class="skill-item"><i class="fab fa-git-alt"></i> Git / GitHub</span>
      <span class="skill-item"><i class="fas fa-wind"></i> Bootstrap</span>
    </div>
    <div class="flex-center mt-2" style="gap: 0.8rem; flex-wrap: wrap;">
      <img src="https://skillicons.dev/icons?i=cs,dotnet,react,js,ts,mysql,mongodb,aws,git" alt="skills" style="border-radius:30px; background:#0f172a; padding:0.3rem 0.8rem;" />
    </div>
  </div>

  <!-- ========== ARCHITECTURE FLOW ========== -->
  <div class="section-card mb-2 text-center">
    <h4 style="color:#22d3ee; font-weight:700;"><i class="fas fa-sitemap"></i> From Idea to Production</h4>
    <div style="display: flex; flex-wrap: wrap; justify-content: center; gap: 0.2rem 0.8rem; font-size:0.9rem; background:#0b1120; border-radius:60px; padding:0.7rem 1.2rem; border:1px solid #1e3a8a; margin-top:0.8rem;">
      <span>💡 Business</span> <span style="color:#22d3ee;">→</span>
      <span>🎨 UI/UX</span> <span style="color:#22d3ee;">→</span>
      <span>⚛️ React</span> <span style="color:#22d3ee;">→</span>
      <span>🔌 Web API</span> <span style="color:#22d3ee;">→</span>
      <span>⚙️ ASP.NET Core</span> <span style="color:#22d3ee;">→</span>
      <span>🧠 Logic</span> <span style="color:#22d3ee;">→</span>
      <span>🗄️ SQL</span> <span style="color:#22d3ee;">→</span>
      <span>🚀 IIS / Cloud</span>
    </div>
  </div>

  <!-- ========== FEATURED REPO ========== -->
  <div class="section-card mb-2 text-center">
    <h4 style="color:#22d3ee;"><i class="fas fa-rocket"></i> Featured Engineering</h4>
    <a href="https://github.com/Upendra505/TDF" target="_blank" style="display:inline-block; margin-top:0.5rem;">
      <img src="https://github-readme-stats.vercel.app/api/pin/?username=Upendra505&repo=TDF&theme=tokyonight&hide_border=true&bg_color=0f172a&title_color=22d3ee&text_color=cbd5e1&icon_color=2563eb" alt="TDF repo" style="border-radius: 1.5rem; max-width:100%;"/>
    </a>
    <div class="flex-center" style="gap:0.6rem; flex-wrap:wrap; margin-top:0.5rem;">
      <span class="badge-pill"><i class="fas fa-hospital"></i> Healthcare</span>
      <span class="badge-pill"><i class="fas fa-users"></i> Doctor/Patient</span>
      <span class="badge-pill"><i class="fas fa-calendar-check"></i> Appointments</span>
      <span class="badge-pill"><i class="fas fa-certificate"></i> Certificates</span>
    </div>
  </div>

  <!-- ========== GITHUB STATS ========== -->
  <div class="stats-wrapper">
    <img src="https://github-readme-stats.vercel.app/api?username=Upendra505&show_icons=true&include_all_commits=true&count_private=true&theme=tokyonight&hide_border=true&bg_color=0F172A&title_color=22D3EE&icon_color=2563EB&text_color=CBD5E1&rank_icon=github" alt="stats" />
    <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Upendra505&layout=compact&langs_count=8&theme=tokyonight&hide_border=true&bg_color=0F172A&title_color=22D3EE&text_color=CBD5E1" alt="top langs" />
  </div>

  <!-- ========== STREAK ========== -->
  <div class="text-center mt-2 mb-2">
    <img src="https://streak-stats.demolab.com?user=Upendra505&theme=tokyonight&hide_border=true&background=0F172A&ring=22D3EE&fire=2563EB&currStreakLabel=22D3EE" alt="streak" style="border-radius: 2rem; max-width:100%;" />
  </div>

  <!-- ========== SNAKE ========== -->
  <div class="snake-box">
    <img src="https://raw.githubusercontent.com/platane/snk/output/github-contribution-grid-snake-dark.svg" alt="snake animation" />
  </div>

  <!-- ========== SOCIALS ========== -->
  <div class="flex-center mt-2 mb-2" style="gap: 0.8rem; flex-wrap: wrap;">
    <a href="https://github.com/Upendra505" class="social-btn"><i class="fab fa-github"></i> GitHub</a>
    <a href="mailto:gorojuupendrachary@gmail.com" class="social-btn"><i class="fas fa-envelope"></i> Email</a>
    <a href="https://twitter.com/upendra2880" class="social-btn"><i class="fab fa-x-twitter"></i> X</a>
    <a href="https://instagram.com/upendra_goroju" class="social-btn"><i class="fab fa-instagram"></i> Instagram</a>
  </div>

  <!-- ========== FOOTER WAVE ========== -->
  <div style="margin-top: 1.5rem; border-radius: 40px; overflow:hidden;">
    <img src="https://capsule-render.vercel.app/api?type=waving&color=0:06b6d4,50:2563eb,100:020617&height=100&section=footer&animation=fadeIn" alt="wave footer" style="width:100%; display:block;" />
  </div>

  <!-- ========== TYPING FOOTER ========== -->
  <div class="text-center mt-2">
    <span style="font-family: 'JetBrains Mono'; color:#67e8f9; font-weight:600;">
      ⚡ BUILD → TEST → DEPLOY → SCALE ⚡
    </span>
    <div style="margin-top: 0.4rem; font-size:0.9rem; color:#94a3b8;">
      <i class="fas fa-code"></i> Thanks for visiting · Let's build something great
    </div>
  </div>

</div>
<!-- end container -->

<!-- extra seo keywords (hidden but visible in source) -->
<div style="display:none;" aria-hidden="true">
  Upendra Chary, Full Stack .NET Developer, C# Developer, ASP.NET Core, React Developer, SQL Server, MongoDB, Web API, Enterprise Applications, Healthcare Platforms, IIS Deployment, AWS, JavaScript, TypeScript, Production-Ready Software.
</div>
</body>
</html>
