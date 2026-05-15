<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Pratham Chikitse | Documentation</title>
    <link href="https://fonts.googleapis.com/css2?family=Sora:wght@400;600;700&family=Space+Mono:wght@400;700&display=swap" rel="stylesheet">
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
            scroll-behavior: smooth;
        }

        /* ── HERO ── */
        .hero { 
            text-align: center; 
            padding: 100px 40px 80px; 
            border-bottom: 1px solid var(--border); 
            position: relative; 
            background: radial-gradient(circle at 50% -20%, rgba(230,57,70,0.15), transparent 70%);
        }

        .hero-icon { font-size: 64px; display: block; margin-bottom: 24px; animation: pulse 3s ease-in-out infinite; }
        @keyframes pulse { 0%,100% { transform: scale(1); } 50% { transform: scale(1.08); } }

        h1.main-title { 
            font-size: clamp(2.5rem, 8vw, 4.5rem); 
            font-weight: 700; 
            letter-spacing: -2px; 
            background: linear-gradient(90deg, #ff6b6b, #e63946, #ff9f43, #e63946);
            background-size: 300% 100%;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            animation: shimmer 5s linear infinite;
        }

        @keyframes shimmer { 0% { background-position: 0% 50%; } 100% { background-position: 300% 50%; } }

        .badges { display: flex; flex-wrap: wrap; justify-content: center; gap: 10px; margin-top: 32px; }
        .badge { font-family: 'Space Mono', monospace; font-size: 11px; padding: 6px 14px; border-radius: 20px; border: 1px solid; background: rgba(255,255,255,0.03); }
        .badge-blue { color: #90c8ff; border-color: rgba(58,134,255,0.3); }
        .badge-green { color: #7aecaa; border-color: rgba(45,198,83,0.3); }
        .badge-red { color: #ff9fa6; border-color: rgba(230,57,70,0.3); }

        /* ── CONTENT ── */
        .container { max-width: 900px; margin: 0 auto; padding: 40px 28px 100px; }
        
        section { margin-top: 80px; }
        .section-label { font-family: 'Space Mono', monospace; font-size: 11px; text-transform: uppercase; letter-spacing: 3px; color: var(--red); margin-bottom: 12px; }
        h2.section-title { font-size: 26px; font-weight: 600; color: #fff; margin-bottom: 24px; padding-bottom: 12px; border-bottom: 1px solid var(--border); }

        /* Features */
        .features-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 20px; }
        .feat-card { background: var(--card); border: 1px solid var(--border); border-radius: 16px; padding: 24px; transition: 0.3s; }
        .feat-card:hover { border-color: var(--red); transform: translateY(-4px); background: #1a1a1a; }
        .feat-icon { font-size: 28px; margin-bottom: 12px; display: block; }
        .feat-title { font-size: 16px; font-weight: 600; color: #fff; margin-bottom: 8px; }
        .feat-desc { font-size: 14px; color: var(--muted); line-height: 1.6; }

        /* Architecture Block */
        .arch-block { 
            background: #080808; border: 1px solid var(--border); border-radius: 12px; 
            padding: 24px; font-family: 'Space Mono', monospace; font-size: 13px; 
            color: #aaa; line-height: 1.8; overflow-x: auto;
        }
        .hl { color: var(--blue); } .hl2 { color: var(--green); } .hl3 { color: var(--amber); }

        /* Tech Table */
        .tech-table { width: 100%; border-collapse: collapse; margin-top: 10px; }
        .tech-table td { padding: 14px; border-bottom: 1px solid var(--border); color: #bbb; }
        .tech-table td:first-child { color: #fff; font-weight: 600; width: 30%; }
        .tech-tag { background: rgba(58,134,255,0.1); color: #90c8ff; border: 1px solid rgba(58,134,255,0.2); padding: 2px 8px; border-radius: 4px; font-size: 11px; }

        /* Steps */
        .step { display: flex; gap: 20px; margin-bottom: 24px; }
        .step-num { width: 36px; height: 36px; background: rgba(230,57,70,0.1); border: 1px solid var(--red); color: var(--red); border-radius: 50%; display: flex; align-items: center; justify-content: center; flex-shrink: 0; font-weight: 700; font-family: 'Space Mono'; }
        .code-block { background: #000; padding: 12px 18px; border-radius: 8px; color: var(--green); font-family: 'Space Mono'; font-size: 13px; margin: 12px 0; }

        footer { text-align: center; padding: 60px; color: var(--muted); border-top: 1px solid var(--border); }
        footer a { color: var(--red); text-decoration: none; font-weight: 600; }
    </style>
</head>
<body>

    <header class="hero">
        <span class="hero-icon">🩺</span>
        <h1 class="main-title">Pratham Chikitse</h1>
        <p style="color: var(--muted); margin-top: 10px;">First-Aid at your fingertips — Offline. Multi-lingual. Life-saving.</p>
        
        <div class="badges">
            <span class="badge badge-red">Kotlin 2.0.0</span>
            <span class="badge badge-blue">Jetpack Compose</span>
            <span class="badge badge-green">Material 3</span>
            <span class="badge badge-red">MIT License</span>
        </div>
    </header>

    <div class="container">
        <section id="overview">
            <p class="section-label">01 — Overview</p>
            <h2 class="section-title">Offline-First Medical Triage</h2>
            <p><strong>Pratham Chikitse</strong> is an Android application engineered for immediate first-aid response. By utilizing an <strong>offline-first architecture</strong>, it serves as a pocket triage assistant for remote areas where connectivity is unreliable.</p>
        </section>

        <section id="features">
            <p class="section-label">02 — Features</p>
            <h2 class="section-title">Life-Saving Capabilities</h2>
            <div class="features-grid">
                <div class="feat-card">
                    <span class="feat-icon">🤖</span>
                    <h3 class="feat-title">AI Triage Chatbot</h3>
                    <p class="feat-desc">Local NLP parsing maps symptoms to emergency guidelines instantly.</p>
                </div>
                <div class="feat-card">
                    <span class="feat-icon">🗣️</span>
                    <h3 class="feat-title">Voice-First Mode</h3>
                    <p class="feat-desc">Integrated TTS reads instructions in regional languages for hands-free help.</p>
                </div>
                <div class="feat-card">
                    <span class="feat-icon">📴</span>
                    <h3 class="feat-title">100% Offline</h3>
                    <p class="feat-desc">All guides and hospital directories are powered by localized JSON assets.</p>
                </div>
                <div class="feat-card">
                    <span class="feat-icon">🆘</span>
                    <h3 class="feat-title">Instant SOS</h3>
                    <p class="feat-desc">One-tap shortcuts for 108, 112, 100, and 101 emergency services.</p>
                </div>
            </div>
        </section>

        <section id="tech">
            <p class="section-label">03 — Technology</p>
            <h2 class="section-title">Modern Android Stack</h2>
            <table class="tech-table">
                <tr><td>Language</td><td><span class="tech-tag">Kotlin 2.0.0</span></td></tr>
                <tr><td>UI Toolkit</td><td>Jetpack Compose (Material 3)</td></tr>
                <tr><td>Architecture</td><td>MVVM + Clean Architecture</td></tr>
                <tr><td>DI</td><td>Dagger Hilt</td></tr>
                <tr><td>Persistence</td><td>Preferences DataStore & Gson</td></tr>
            </table>
        </section>

        <section id="architecture">
            <p class="section-label">04 — Architecture</p>
            <h2 class="section-title">Project Structure</h2>
            <div class="arch-block">
                app/src/main/<br>
                ├── <span class="hl">assets/</span> <span class="hl3">// Localized JSON Datasets</span><br>
                ├── java/com/example/health/<br>
                │   ├── <span class="hl2">data/</span> <span class="hl3">// Repositories & DataStore</span><br>
                │   ├── <span class="hl2">ui/</span> <span class="hl3">// Compose Screens & ViewModels</span><br>
                │   │   ├── assistant/ & emergency/ & hospital/<br>
                │   ├── <span class="hl2">util/</span> <span class="hl3">// TTSManager & LocaleHelper</span><br>
                └── <span class="hl">res/</span> <span class="hl3">// values-kn, values-hi, values-gu...</span>
            </div>
        </section>

        <section id="setup">
            <p class="section-label">05 — Setup</p>
            <h2 class="section-title">Getting Started</h2>
            <div class="step">
                <div class="step-num">1</div>
                <div class="step-content">
                    <h3>Clone the repo</h3>
                    <div class="code-block">git clone https://github.com/AlphaDoc1/PrathamChikitse.git</div>
                </div>
            </div>
            <div class="step">
                <div class="step-num">2</div>
                <div class="step-content">
                    <h3>Build & Run</h3>
                    <p>Open in Android Studio Koala+, ensure JDK is set to Java 17, and click Run.</p>
                </div>
            </div>
        </section>
    </div>

    <footer>
        <p>Built by <a href="#">AlphaDoc1</a> &copy; 2026. Available under MIT License.</p>
    </footer>

</body>
</html>
