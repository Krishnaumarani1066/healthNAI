<title>Pratham Chikitse</title> <style> :root { --red: #e63946; --dark: #0d0d0d; --card: #141414; --border: rgba(255,255,255,0.08); --muted: #888; --green: #2dc653; --blue: #3a86ff; --amber: #f4a261; }
{ margin: 0; padding: 0; box-sizing: border-box; }
body { background: var(--dark); color: #e0e0e0; font-family: 'Sora', sans-serif; font-size: 15px; line-height: 1.75; min-height: 100vh; }

/* ── HERO ── */ .hero { text-align: center; padding: 80px 40px 60px; border-bottom: 1px solid var(--border); position: relative; overflow: hidden; }

.hero::before { content: ''; position: absolute; inset: 0; background: radial-gradient(ellipse 80% 60% at 50% -10%, rgba(230,57,70,0.18), transparent); pointer-events: none; }

.hero-icon { font-size: 56px; display: block; margin: 0 auto 24px; animation: pulse 3s ease-in-out infinite; }

@keyframes pulse { 0%,100% { transform: scale(1); } 50% { transform: scale(1.08); } }

/* Moving gradient title */ .title-wrap { overflow: hidden; margin-bottom: 8px; }

h1.main-title { font-family: 'Sora', sans-serif; font-size: clamp(2.2rem, 6vw, 4rem); font-weight: 700; letter-spacing: -1px; background: linear-gradient(90deg, #ff6b6b, #e63946, #ff9f43, #e63946, #ff6b6b, #c9184a); background-size: 300% 100%; -webkit-background-clip: text; -webkit-text-fill-color: transparent; background-clip: text; animation: shimmer 4s linear infinite; display: inline-block; }

@keyframes shimmer { 0% { background-position: 0% 50%; } 100% { background-position: 300% 50%; } }

/* Typewriter subtitle */ .subtitle-type { font-family: 'Space Mono', monospace; font-size: 13px; color: var(--muted); letter-spacing: 0.5px; margin-bottom: 28px; min-height: 20px; }

.cursor { display: inline-block; width: 2px; height: 14px; background: var(--red); margin-left: 2px; vertical-align: middle; animation: blink 0.8s step-end infinite; }

@keyframes blink { 0%,100%{opacity:1} 50%{opacity:0} }

/* Badges */ .badges { display: flex; flex-wrap: wrap; justify-content: center; gap: 8px; margin-top: 24px; }

.badge { font-family: 'Space Mono', monospace; font-size: 11px; padding: 4px 12px; border-radius: 20px; border: 1px solid; }

.badge-blue { color: #90c8ff; border-color: rgba(58,134,255,0.4); background: rgba(58,134,255,0.08); } .badge-green { color: #7aecaa; border-color: rgba(45,198,83,0.4); background: rgba(45,198,83,0.08); } .badge-amber { color: #ffd09b; border-color: rgba(244,162,97,0.4); background: rgba(244,162,97,0.08); } .badge-red { color: #ff9fa6; border-color: rgba(230,57,70,0.4); background: rgba(230,57,70,0.08); }

/* ── LAYOUT ── */ .container { max-width: 860px; margin: 0 auto; padding: 0 28px 80px; }

/* ── SECTIONS ── */ section { margin-top: 56px; }

.section-label { font-family: 'Space Mono', monospace; font-size: 11px; text-transform: uppercase; letter-spacing: 2px; color: var(--red); margin-bottom: 12px; }

h2.section-title { font-size: 22px; font-weight: 600; color: #f0f0f0; margin-bottom: 16px; padding-bottom: 12px; border-bottom: 1px solid var(--border); }

p { color: #bbb; margin-bottom: 12px; } p strong { color: #e0e0e0; font-weight: 600; }

/* Feature cards */ .features-grid { display: grid; grid-template-columns: repeat(auto-fit, minmax(240px, 1fr)); gap: 16px; margin-top: 20px; }

.feat-card { background: var(--card); border: 1px solid var(--border); border-radius: 12px; padding: 20px; transition: border-color 0.25s, transform 0.25s; }

.feat-card:hover { border-color: rgba(230,57,70,0.35); transform: translateY(-2px); }

.feat-icon { font-size: 22px; margin-bottom: 10px; display: block; } .feat-title { font-size: 14px; font-weight: 600; color: #e8e8e8; margin-bottom: 6px; } .feat-desc { font-size: 13px; color: var(--muted); line-height: 1.6; }

/* Tech table */ .tech-table { width: 100%; border-collapse: collapse; margin-top: 16px; font-size: 14px; }

.tech-table th { text-align: left; font-family: 'Space Mono', monospace; font-size: 11px; text-transform: uppercase; letter-spacing: 1px; color: var(--muted); padding: 10px 14px; border-bottom: 1px solid var(--border); }

.tech-table td { padding: 11px 14px; border-bottom: 1px solid rgba(255,255,255,0.04); color: #bbb; vertical-align: top; }

.tech-table td:first-child { color: #e0e0e0; font-weight: 600; white-space: nowrap; width: 35%; }

.tech-tag { display: inline-block; background: rgba(58,134,255,0.1); color: #90c8ff; border: 1px solid rgba(58,134,255,0.25); border-radius: 6px; font-family: 'Space Mono', monospace; font-size: 11px; padding: 2px 8px; }

/* Architecture tree */ .arch-block { background: var(--card); border: 1px solid var(--border); border-radius: 12px; padding: 20px 24px; margin-top: 16px; font-family: 'Space Mono', monospace; font-size: 12px; color: #999; line-height: 2; overflow-x: auto; }

.arch-block .hl { color: #3a86ff; } .arch-block .hl2 { color: #2dc653; } .arch-block .hl3 { color: var(--amber); }

/* Steps */ .steps { margin-top: 16px; }

.step { display: flex; gap: 16px; margin-bottom: 20px; align-items: flex-start; }

.step-num { min-width: 32px; height: 32px; border-radius: 50%; background: rgba(230,57,70,0.15); border: 1px solid rgba(230,57,70,0.35); color: var(--red); font-family: 'Space Mono', monospace; font-size: 12px; font-weight: 700; display: flex; align-items: center; justify-content: center; flex-shrink: 0; margin-top: 2px; }

.step-content h3 { font-size: 15px; font-weight: 600; color: #e0e0e0; margin-bottom: 4px; } .step-content p { font-size: 13px; color: var(--muted); margin: 0; }

/* Code block */ .code-block { background: #0a0a0a; border: 1px solid var(--border); border-radius: 10px; padding: 14px 18px; font-family: 'Space Mono', monospace; font-size: 12px; color: #7aecaa; margin: 10px 0; overflow-x: auto; }

/* Troubleshoot table */ .trouble-table { width: 100%; border-collapse: collapse; font-size: 13px; margin-top: 16px; }

.trouble-table th { text-align: left; font-family: 'Space Mono', monospace; font-size: 11px; text-transform: uppercase; letter-spacing: 1px; color: var(--muted); padding: 10px 12px; border-bottom: 1px solid var(--border); }

.trouble-table td { padding: 12px; border-bottom: 1px solid rgba(255,255,255,0.04); vertical-align: top; color: #bbb; }

.trouble-table td:first-child { color: #ffd09b; font-weight: 600; } .trouble-table td:nth-child(2) { color: var(--muted); } .trouble-table td:nth-child(3) { color: #7aecaa; }

/* Prereqs */ .prereq-list { list-style: none; margin-top: 12px; } .prereq-list li { display: flex; align-items: baseline; gap: 10px; padding: 9px 0; border-bottom: 1px solid rgba(255,255,255,0.04); font-size: 14px; } .prereq-list li::before { content: '→'; color: var(--red); font-family: monospace; flex-shrink: 0; } .prereq-list li strong { color: #e0e0e0; margin-right: 4px; }

/* Footer */ footer { margin-top: 72px; border-top: 1px solid var(--border); padding: 32px 28px; text-align: center; font-size: 13px; color: var(--muted); }

footer a { color: var(--red); text-decoration: none; } footer a:hover { text-decoration: underline; }

/* Animate sections on scroll */ .reveal { opacity: 0; transform: translateY(20px); transition: opacity 0.55s ease, transform 0.55s ease; } .reveal.visible { opacity: 1; transform: translateY(0); } </style>

🩺
Pratham Chikitse
Kotlin 2.0.0 Android 14.0 Jetpack Compose · Material 3 Build · Passing MIT License
01 — Overview
Project Overview
Pratham Chikitse is a comprehensive, life-saving Android application engineered to provide immediate, actionable first-aid guidance. Built entirely offline-first, the app acts as a pocket medical triage assistant, designed to work reliably in remote areas or low-connectivity zones.

By focusing on accessibility, the application includes a Voice-First mode, multi-language support, and an AI-powered triage chatbot to help users quickly identify the appropriate emergency response without needing internet connectivity.

02 — Features
Key Features
🚨
Interactive AI Triage Chatbot
Parses user input locally and maps it to immediate, high-priority emergency guidelines and hospital recommendations.
🌐
Robust Multi-Language Support
Seamlessly switch between English, Kannada, Hindi, Gujarati, Marathi, and Tamil — UI and data adapt instantly.
🔊
Voice-First & TTS
Built-in TTS reads emergency instructions in regional languages, ensuring accessibility in chaotic environments.
📴
Offline-First Architecture
All guides, myths & facts, and triage logic are driven by localized JSON assets. No internet required.
🏥
Geo-Spatial Hospital Locator
Calculates nearest hospitals using offline boundary data when location permissions are granted.
🆘
SOS Mode
Floating action button for immediate shortcuts to emergency numbers (108, 112, 100, 101) and custom contacts.
03 — Technology
Technology Stack
Category	Technology / Library
Language	Kotlin 2.0.0
UI Toolkit	Jetpack Compose (Material 3)
Architecture	MVVM
Dependency Injection	Dagger Hilt
Local Persistence	Preferences DataStore
Async Programming	Kotlin Coroutines & StateFlow
Navigation	Jetpack Navigation Compose
JSON Parsing	Gson
04 — Architecture
Project Architecture
Follows Clean Architecture principles with complete separation of concerns between UI, state management, and data sources.

app/src/main/
├── assets/ # Offline JSON Datasets
├── java/com/example/health/
│ ├── data/ # Repositories & Data Models
│ │ ├── local/ # DataStore and JsonDataSource
│ │ ├── model/ # Kotlin Data Classes (DTOs)
│ │ └── repository/ # Abstraction layers
│ ├── navigation/ # Compose NavGraph & Routes
│ ├── ui/ # UI Layer (Screens & ViewModels)
│ │ ├── assistant/ # Triage Chatbot
│ │ ├── emergency/ # Emergency Guides
│ │ ├── home/ # Dashboard & Quick Actions
│ │ ├── hospital/ # Offline Hospital Directory
│ │ ├── learning/ # Educational Modules
│ │ ├── onboarding/ # First-launch flow
│ │ └── settings/ # Preferences
│ └── util/ # TTSManager, LocaleHelper
└── res/ # Localized strings (kn, hi, gu…)
05 — Prerequisites
Prerequisites
Android Studio: Koala Feature Drop (2024.1.2) or newer
JDK: Java Development Kit 17
Android SDK: API Level 34 (Android 14) via SDK Manager
Minimum Device: Android 8.0 (API Level 26) or newer
06 — Setup
Installation & Setup
1
Clone the Repository
git clone https://github.com/AlphaDoc1/PrathamChikitse.git
cd PrathamChikitse
2
Open in Android Studio
Go to File → Open, select the PrathamChikitse root directory, and allow Gradle to sync dependencies.

3
Zero-Configuration Run
No API keys or manual local.properties needed. Just verify Gradle JDK is set to jbr-17 under Build Tools → Gradle settings.

07 — Running
Running the Application
🖥️
Emulator
Open Device Manager → Create Virtual Device (Pixel 7, API 34) → click Run ▶️
📱
Physical Device
Enable Developer Options → USB Debugging → connect via USB → select device → Run ▶️
08 — Localization
Data & Localization
All core data is stored in localized JSON files within assets/. Non-developers can easily contribute new content or translations.

1
Add language code to LocaleHelper.kt
Register the new locale in LocaleHelper.kt and the Settings UI options.

2
Create Android strings
Add res/values-{lang}/strings.xml with all translated UI strings.

3
Add localized JSON assets
Create emergencies_{lang}.json, hospitals_{lang}.json, etc. The engine auto-falls back to English if missing.

09 — Troubleshooting
Troubleshooting
Issue	Potential Cause	Solution
Gradle Sync Failed	Incorrect JDK version	Change Gradle JDK to Java 17 in Settings
TTS is silent	Missing TTS Engine	Install/update Google TTS from Play Store. Falls back to English automatically
Double spacing above Top App Bar	Inset/Edge-to-Edge collision	Use .consumeWindowInsets() in NavGraph — pull latest branch
Unresolved reference: hiltViewModel	Hilt KAPT/KSP issue	Build → Clean Project, then Rebuild Project
10 — Contributing
Contributing
