<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Pratham Chikitse</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Space+Mono:wght@400;700&family=Sora:wght@300;400;600;700&display=swap" rel="stylesheet">
<style>
  :root {
    --red: #e63946;
    --dark: #0d0d0d;
    --card: #141414;
    --border: rgba(255,255,255,0.08);
    --muted: #888;
    --green: #2dc653;
    --blue: #3a86ff;
    --amber: #f4a261;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    background: var(--dark);
    color: #e0e0e0;
    font-family: 'Sora', sans-serif;
    font-size: 15px;
    line-height: 1.75;
    min-height: 100vh;
  }

  /* ── HERO ── */
  .hero {
    text-align: center;
    padding: 80px 40px 60px;
    border-bottom: 1px solid var(--border);
    position: relative;
    overflow: hidden;
  }

  .hero::before {
    content: '';
    position: absolute;
    inset: 0;
    background: radial-gradient(ellipse 80% 60% at 50% -10%, rgba(230,57,70,0.18), transparent);
    pointer-events: none;
  }

  .hero-icon {
    font-size: 56px;
    display: block;
    margin: 0 auto 24px;
    animation: pulse 3s ease-in-out infinite;
  }

  @keyframes pulse {
    0%,100% { transform: scale(1); }
    50% { transform: scale(1.08); }
  }

  /* Moving gradient title */
  .title-wrap {
    overflow: hidden;
    margin-bottom: 8px;
  }

  h1.main-title {
    font-family: 'Sora', sans-serif;
    font-size: clamp(2.2rem, 6vw, 4rem);
    font-weight: 700;
    letter-spacing: -1px;
    background: linear-gradient(90deg, #ff6b6b, #e63946, #ff9f43, #e63946, #ff6b6b, #c9184a);
    background-size: 300% 100%;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    animation: shimmer 4s linear infinite;
    display: inline-block;
  }

  @keyframes shimmer {
    0% { background-position: 0% 50%; }
    100% { background-position: 300% 50%; }
  }

  /* Typewriter subtitle */
  .subtitle-type {
    font-family: 'Space Mono', monospace;
    font-size: 13px;
    color: var(--muted);
    letter-spacing: 0.5px;
    margin-bottom: 28px;
    min-height: 20px;
  }

  .cursor {
    display: inline-block;
    width: 2px;
    height: 14px;
    background: var(--red);
    margin-left: 2px;
    vertical-align: middle;
    animation: blink 0.8s step-end infinite;
  }

  @keyframes blink { 0%,100%{opacity:1} 50%{opacity:0} }

  /* Badges */
  .badges {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 8px;
    margin-top: 24px;
  }

  .badge {
    font-family: 'Space Mono', monospace;
    font-size: 11px;
    padding: 4px 12px;
    border-radius: 20px;
    border: 1px solid;
  }

  .badge-blue  { color: #90c8ff; border-color: rgba(58,134,255,0.4); background: rgba(58,134,255,0.08); }
  .badge-green { color: #7aecaa; border-color: rgba(45,198,83,0.4); background: rgba(45,198,83,0.08); }
  .badge-amber { color: #ffd09b; border-color: rgba(244,162,97,0.4); background: rgba(244,162,97,0.08); }
  .badge-red   { color: #ff9fa6; border-color: rgba(230,57,70,0.4); background: rgba(230,57,70,0.08); }

  /* ── LAYOUT ── */
  .container {
    max-width: 860px;
    margin: 0 auto;
    padding: 0 28px 80px;
  }

  /* ── SECTIONS ── */
  section { margin-top: 56px; }

  .section-label {
    font-family: 'Space Mono', monospace;
    font-size: 11px;
    text-transform: uppercase;
    letter-spacing: 2px;
    color: var(--red);
    margin-bottom: 12px;
  }

  h2.section-title {
    font-size: 22px;
    font-weight: 600;
    color: #f0f0f0;
    margin-bottom: 16px;
    padding-bottom: 12px;
    border-bottom: 1px solid var(--border);
  }

  p { color: #bbb; margin-bottom: 12px; }
  p strong { color: #e0e0e0; font-weight: 600; }

  /* Feature cards */
  .features-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
    gap: 16px;
    margin-top: 20px;
  }

  .feat-card {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 20px;
    transition: border-color 0.25s, transform 0.25s;
  }

  .feat-card:hover {
    border-color: rgba(230,57,70,0.35);
    transform: translateY(-2px);
  }

  .feat-icon { font-size: 22px; margin-bottom: 10px; display: block; }
  .feat-title { font-size: 14px; font-weight: 600; color: #e8e8e8; margin-bottom: 6px; }
  .feat-desc { font-size: 13px; color: var(--muted); line-height: 1.6; }

  /* Tech table */
  .tech-table {
    width: 100%;
    border-collapse: collapse;
    margin-top: 16px;
    font-size: 14px;
  }

  .tech-table th {
    text-align: left;
    font-family: 'Space Mono', monospace;
    font-size: 11px;
    text-transform: uppercase;
    letter-spacing: 1px;
    color: var(--muted);
    padding: 10px 14px;
    border-bottom: 1px solid var(--border);
  }

  .tech-table td {
    padding: 11px 14px;
    border-bottom: 1px solid rgba(255,255,255,0.04);
    color: #bbb;
    vertical-align: top;
  }

  .tech-table td:first-child {
    color: #e0e0e0;
    font-weight: 600;
    white-space: nowrap;
    width: 35%;
  }

  .tech-tag {
    display: inline-block;
    background: rgba(58,134,255,0.1);
    color: #90c8ff;
    border: 1px solid rgba(58,134,255,0.25);
    border-radius: 6px;
    font-family: 'Space Mono', monospace;
    font-size: 11px;
    padding: 2px 8px;
  }

  /* Architecture tree */
  .arch-block {
    background: var(--card);
    border: 1px solid var(--border);
    border-radius: 12px;
    padding: 20px 24px;
    margin-top: 16px;
    font-family: 'Space Mono', monospace;
    font-size: 12px;
    color: #999;
    line-height: 2;
    overflow-x: auto;
  }

  .arch-block .hl { color: #3a86ff; }
  .arch-block .hl2 { color: #2dc653; }
  .arch-block .hl3 { color: var(--amber); }

  /* Steps */
  .steps { margin-top: 16px; }

  .step {
    display: flex;
    gap: 16px;
    margin-bottom: 20px;
    align-items: flex-start;
  }

  .step-num {
    min-width: 32px;
    height: 32px;
    border-radius: 50%;
    background: rgba(230,57,70,0.15);
    border: 1px solid rgba(230,57,70,0.35);
    color: var(--red);
    font-family: 'Space Mono', monospace;
    font-size: 12px;
    font-weight: 700;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-shrink: 0;
    margin-top: 2px;
  }

  .step-content h3 { font-size: 15px; font-weight: 600; color: #e0e0e0; margin-bottom: 4px; }
  .step-content p  { font-size: 13px; color: var(--muted); margin: 0; }

  /* Code block */
  .code-block {
    background: #0a0a0a;
    border: 1px solid var(--border);
    border-radius: 10px;
    padding: 14px 18px;
    font-family: 'Space Mono', monospace;
    font-size: 12px;
    color: #7aecaa;
    margin: 10px 0;
    overflow-x: auto;
  }

  /* Troubleshoot table */
  .trouble-table {
    width: 100%;
    border-collapse: collapse;
    font-size: 13px;
    margin-top: 16px;
  }

  .trouble-table th {
    text-align: left;
    font-family: 'Space Mono', monospace;
    font-size: 11px;
    text-transform: uppercase;
    letter-spacing: 1px;
    color: var(--muted);
    padding: 10px 12px;
    border-bottom: 1px solid var(--border);
  }

  .trouble-table td {
    padding: 12px;
    border-bottom: 1px solid rgba(255,255,255,0.04);
    vertical-align: top;
    color: #bbb;
  }

  .trouble-table td:first-child { color: #ffd09b; font-weight: 600; }
  .trouble-table td:nth-child(2) { color: var(--muted); }
  .trouble-table td:nth-child(3) { color: #7aecaa; }

  /* Prereqs */
  .prereq-list { list-style: none; margin-top: 12px; }
  .prereq-list li {
    display: flex;
    align-items: baseline;
    gap: 10px;
    padding: 9px 0;
    border-bottom: 1px solid rgba(255,255,255,0.04);
    font-size: 14px;
  }
  .prereq-list li::before { content: '→'; color: var(--red); font-family: monospace; flex-shrink: 0; }
  .prereq-list li strong { color: #e0e0e0; margin-right: 4px; }

  /* Footer */
  footer {
    margin-top: 72px;
    border-top: 1px solid var(--border);
    padding: 32px 28px;
    text-align: center;
    font-size: 13px;
    color: var(--muted);
  }

  footer a { color: var(--red); text-decoration: none; }
  footer a:hover { text-decoration: underline; }

  /* Animate sections on scroll */
  .reveal {
    opacity: 0;
    transform: translateY(20px);
    transition: opacity 0.55s ease, transform 0.55s ease;
  }
  .reveal.visible {
    opacity: 1;
    transform: translateY(0);
  }
</style>
</head>
<body>

<!-- HERO -->
<div class="hero">
  <span class="hero-icon">🩺</span>
  <div class="title-wrap">
    <h1 class="main-title">Pratham Chikitse</h1>
  </div>
  <div class="subtitle-type" id="typewriter"></div>
  <div class="badges">
    <span class="badge badge-blue">Kotlin 2.0.0</span>
    <span class="badge badge-green">Android 14.0</span>
    <span class="badge badge-blue">Jetpack Compose · Material 3</span>
    <span class="badge badge-green">Build · Passing</span>
    <span class="badge badge-amber">MIT License</span>
  </div>
</div>

<div class="container">

  <!-- OVERVIEW -->
  <section class="reveal">
    <div class="section-label">01 — Overview</div>
    <h2 class="section-title">Project Overview</h2>
    <p><strong>Pratham Chikitse</strong> is a comprehensive, life-saving Android application engineered to provide immediate, actionable first-aid guidance. Built entirely offline-first, the app acts as a pocket medical triage assistant, designed to work reliably in remote areas or low-connectivity zones.</p>
    <p>By focusing on accessibility, the application includes a Voice-First mode, multi-language support, and an AI-powered triage chatbot to help users quickly identify the appropriate emergency response without needing internet connectivity.</p>
  </section>

  <!-- FEATURES -->
  <section class="reveal">
    <div class="section-label">02 — Features</div>
    <h2 class="section-title">Key Features</h2>
    <div class="features-grid">
      <div class="feat-card">
        <span class="feat-icon">🚨</span>
        <div class="feat-title">Interactive AI Triage Chatbot</div>
        <div class="feat-desc">Parses user input locally and maps it to immediate, high-priority emergency guidelines and hospital recommendations.</div>
      </div>
      <div class="feat-card">
        <span class="feat-icon">🌐</span>
        <div class="feat-title">Robust Multi-Language Support</div>
        <div class="feat-desc">Seamlessly switch between English, Kannada, Hindi, Gujarati, Marathi, and Tamil — UI and data adapt instantly.</div>
      </div>
      <div class="feat-card">
        <span class="feat-icon">🔊</span>
        <div class="feat-title">Voice-First & TTS</div>
        <div class="feat-desc">Built-in TTS reads emergency instructions in regional languages, ensuring accessibility in chaotic environments.</div>
      </div>
      <div class="feat-card">
        <span class="feat-icon">📴</span>
        <div class="feat-title">Offline-First Architecture</div>
        <div class="feat-desc">All guides, myths & facts, and triage logic are driven by localized JSON assets. No internet required.</div>
      </div>
      <div class="feat-card">
        <span class="feat-icon">🏥</span>
        <div class="feat-title">Geo-Spatial Hospital Locator</div>
        <div class="feat-desc">Calculates nearest hospitals using offline boundary data when location permissions are granted.</div>
      </div>
      <div class="feat-card">
        <span class="feat-icon">🆘</span>
        <div class="feat-title">SOS Mode</div>
        <div class="feat-desc">Floating action button for immediate shortcuts to emergency numbers (108, 112, 100, 101) and custom contacts.</div>
      </div>
    </div>
  </section>

  <!-- TECH STACK -->
  <section class="reveal">
    <div class="section-label">03 — Technology</div>
    <h2 class="section-title">Technology Stack</h2>
    <table class="tech-table">
      <thead><tr><th>Category</th><th>Technology / Library</th></tr></thead>
      <tbody>
        <tr><td>Language</td><td><span class="tech-tag">Kotlin 2.0.0</span></td></tr>
        <tr><td>UI Toolkit</td><td><span class="tech-tag">Jetpack Compose (Material 3)</span></td></tr>
        <tr><td>Architecture</td><td><span class="tech-tag">MVVM</span></td></tr>
        <tr><td>Dependency Injection</td><td><span class="tech-tag">Dagger Hilt</span></td></tr>
        <tr><td>Local Persistence</td><td><span class="tech-tag">Preferences DataStore</span></td></tr>
        <tr><td>Async Programming</td><td><span class="tech-tag">Kotlin Coroutines & StateFlow</span></td></tr>
        <tr><td>Navigation</td><td><span class="tech-tag">Jetpack Navigation Compose</span></td></tr>
        <tr><td>JSON Parsing</td><td><span class="tech-tag">Gson</span></td></tr>
      </tbody>
    </table>
  </section>

  <!-- ARCHITECTURE -->
  <section class="reveal">
    <div class="section-label">04 — Architecture</div>
    <h2 class="section-title">Project Architecture</h2>
    <p>Follows Clean Architecture principles with complete separation of concerns between UI, state management, and data sources.</p>
    <div class="arch-block">
      <span class="hl">app/src/main/</span><br>
      ├── <span class="hl2">assets/</span>                  <span style="color:#555"># Offline JSON Datasets</span><br>
      ├── java/com/example/health/<br>
      │   ├── <span class="hl2">data/</span>                <span style="color:#555"># Repositories & Data Models</span><br>
      │   │   ├── local/           <span style="color:#555"># DataStore and JsonDataSource</span><br>
      │   │   ├── model/           <span style="color:#555"># Kotlin Data Classes (DTOs)</span><br>
      │   │   └── repository/      <span style="color:#555"># Abstraction layers</span><br>
      │   ├── <span class="hl2">navigation/</span>          <span style="color:#555"># Compose NavGraph & Routes</span><br>
      │   ├── <span class="hl3">ui/</span>                  <span style="color:#555"># UI Layer (Screens & ViewModels)</span><br>
      │   │   ├── assistant/       <span style="color:#555"># Triage Chatbot</span><br>
      │   │   ├── emergency/       <span style="color:#555"># Emergency Guides</span><br>
      │   │   ├── home/            <span style="color:#555"># Dashboard & Quick Actions</span><br>
      │   │   ├── hospital/        <span style="color:#555"># Offline Hospital Directory</span><br>
      │   │   ├── learning/        <span style="color:#555"># Educational Modules</span><br>
      │   │   ├── onboarding/      <span style="color:#555"># First-launch flow</span><br>
      │   │   └── settings/        <span style="color:#555"># Preferences</span><br>
      │   └── <span class="hl2">util/</span>                <span style="color:#555"># TTSManager, LocaleHelper</span><br>
      └── <span class="hl">res/</span>                     <span style="color:#555"># Localized strings (kn, hi, gu…)</span>
    </div>
  </section>

  <!-- PREREQUISITES -->
  <section class="reveal">
    <div class="section-label">05 — Prerequisites</div>
    <h2 class="section-title">Prerequisites</h2>
    <ul class="prereq-list">
      <li><strong>Android Studio:</strong> Koala Feature Drop (2024.1.2) or newer</li>
      <li><strong>JDK:</strong> Java Development Kit 17</li>
      <li><strong>Android SDK:</strong> API Level 34 (Android 14) via SDK Manager</li>
      <li><strong>Minimum Device:</strong> Android 8.0 (API Level 26) or newer</li>
    </ul>
  </section>

  <!-- SETUP -->
  <section class="reveal">
    <div class="section-label">06 — Setup</div>
    <h2 class="section-title">Installation & Setup</h2>
    <div class="steps">
      <div class="step">
        <div class="step-num">1</div>
        <div class="step-content">
          <h3>Clone the Repository</h3>
          <div class="code-block">git clone https://github.com/AlphaDoc1/PrathamChikitse.git<br>cd PrathamChikitse</div>
        </div>
      </div>
      <div class="step">
        <div class="step-num">2</div>
        <div class="step-content">
          <h3>Open in Android Studio</h3>
          <p>Go to File → Open, select the <code style="color:#90c8ff">PrathamChikitse</code> root directory, and allow Gradle to sync dependencies.</p>
        </div>
      </div>
      <div class="step">
        <div class="step-num">3</div>
        <div class="step-content">
          <h3>Zero-Configuration Run</h3>
          <p>No API keys or manual <code style="color:#90c8ff">local.properties</code> needed. Just verify Gradle JDK is set to <code style="color:#90c8ff">jbr-17</code> under Build Tools → Gradle settings.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- RUNNING -->
  <section class="reveal">
    <div class="section-label">07 — Running</div>
    <h2 class="section-title">Running the Application</h2>
    <div style="display:grid;grid-template-columns:1fr 1fr;gap:16px;margin-top:16px;">
      <div style="background:var(--card);border:1px solid var(--border);border-radius:12px;padding:20px;">
        <div style="font-size:20px;margin-bottom:8px;">🖥️</div>
        <div style="font-size:14px;font-weight:600;color:#e0e0e0;margin-bottom:6px;">Emulator</div>
        <div style="font-size:13px;color:var(--muted);">Open Device Manager → Create Virtual Device (Pixel 7, API 34) → click Run ▶️</div>
      </div>
      <div style="background:var(--card);border:1px solid var(--border);border-radius:12px;padding:20px;">
        <div style="font-size:20px;margin-bottom:8px;">📱</div>
        <div style="font-size:14px;font-weight:600;color:#e0e0e0;margin-bottom:6px;">Physical Device</div>
        <div style="font-size:13px;color:var(--muted);">Enable Developer Options → USB Debugging → connect via USB → select device → Run ▶️</div>
      </div>
    </div>
  </section>

  <!-- LOCALIZATION -->
  <section class="reveal">
    <div class="section-label">08 — Localization</div>
    <h2 class="section-title">Data & Localization</h2>
    <p>All core data is stored in localized JSON files within <code style="color:#90c8ff">assets/</code>. Non-developers can easily contribute new content or translations.</p>
    <div class="steps" style="margin-top:16px;">
      <div class="step">
        <div class="step-num">1</div>
        <div class="step-content">
          <h3>Add language code to LocaleHelper.kt</h3>
          <p>Register the new locale in <code style="color:#90c8ff">LocaleHelper.kt</code> and the Settings UI options.</p>
        </div>
      </div>
      <div class="step">
        <div class="step-num">2</div>
        <div class="step-content">
          <h3>Create Android strings</h3>
          <p>Add <code style="color:#90c8ff">res/values-{lang}/strings.xml</code> with all translated UI strings.</p>
        </div>
      </div>
      <div class="step">
        <div class="step-num">3</div>
        <div class="step-content">
          <h3>Add localized JSON assets</h3>
          <p>Create <code style="color:#90c8ff">emergencies_{lang}.json</code>, <code style="color:#90c8ff">hospitals_{lang}.json</code>, etc. The engine auto-falls back to English if missing.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- TROUBLESHOOTING -->
  <section class="reveal">
    <div class="section-label">09 — Troubleshooting</div>
    <h2 class="section-title">Troubleshooting</h2>
    <table class="trouble-table">
      <thead><tr><th>Issue</th><th>Potential Cause</th><th>Solution</th></tr></thead>
      <tbody>
        <tr>
          <td>Gradle Sync Failed</td>
          <td>Incorrect JDK version</td>
          <td>Change Gradle JDK to Java 17 in Settings</td>
        </tr>
        <tr>
          <td>TTS is silent</td>
          <td>Missing TTS Engine</td>
          <td>Install/update Google TTS from Play Store. Falls back to English automatically</td>
        </tr>
        <tr>
          <td>Double spacing above Top App Bar</td>
          <td>Inset/Edge-to-Edge collision</td>
          <td>Use <code style="color:#90c8ff">.consumeWindowInsets()</code> in NavGraph — pull latest branch</td>
        </tr>
        <tr>
          <td>Unresolved reference: hiltViewModel</td>
          <td>Hilt KAPT/KSP issue</td>
          <td>Build → Clean Project, then Rebuild Project</td>
        </tr>
      </tbody>
    </table>
  </section>

  <!-- CONTRIBUTING -->
  <section class="reveal">
    <div class="section-label">10 — Contributing</div>
    <h2 class="section-title">Contributing</h2>
    <p>Contributions are welcome to make Pratham Chikitse a robust global medical tool!</p>
    <div class="steps" style="margin-top:16px;">
      <div class="step"><div class="step-num">1</div><div class="step-content"><h3>Fork the Project</h3></div></div>
      <div class="step"><div class="step-num">2</div><div class="step-content"><h3>Create your Feature Branch</h3><div class="code-block">git checkout -b feature/AmazingFeature</div></div></div>
      <div class="step"><div class="step-num">3</div><div class="step-content"><h3>Commit & Push</h3><div class="code-block">git commit -m 'Add some AmazingFeature'<br>git push origin feature/AmazingFeature</div></div></div>
      <div class="step"><div class="step-num">4</div><div class="step-content"><h3>Open a Pull Request</h3><p>Ensure your code aligns with standard Kotlin formatting and doesn't break the offline JSON parsing engine.</p></div></div>
    </div>
  </section>

</div>

<!-- FOOTER -->
<footer>
  <p>Distributed under the <strong style="color:#e0e0e0">MIT License</strong> · Maintainer: <a href="https://github.com/AlphaDoc1/PrathamChikitse">AlphaDoc1</a></p>
  <p style="margin-top:8px;">Issue Tracker: <a href="https://github.com/AlphaDoc1/PrathamChikitse/issues">GitHub Issues</a></p>
</footer>

<script>
  // Typewriter effect
  const phrases = [
    'A Production-Grade, Offline-First Emergency First-Aid App',
    'Life-saving guidance — no internet required.',
    'Voice-first · Multi-language · AI Triage'
  ];
  let pi = 0, ci = 0, del = false;
  const el = document.getElementById('typewriter');

  function type() {
    const phrase = phrases[pi];
    if (!del) {
      el.innerHTML = phrase.slice(0, ++ci) + '<span class="cursor"></span>';
      if (ci === phrase.length) { del = true; setTimeout(type, 2200); return; }
      setTimeout(type, 45);
    } else {
      el.innerHTML = phrase.slice(0, --ci) + '<span class="cursor"></span>';
      if (ci === 0) { del = false; pi = (pi + 1) % phrases.length; setTimeout(type, 400); return; }
      setTimeout(type, 22);
    }
  }
  type();

  // Scroll reveal
  const reveals = document.querySelectorAll('.reveal');
  const obs = new IntersectionObserver(entries => {
    entries.forEach(e => { if (e.isIntersecting) { e.target.classList.add('visible'); obs.unobserve(e.target); } });
  }, { threshold: 0.1 });
  reveals.forEach(r => obs.observe(r));
</script>
</body>
</html>
