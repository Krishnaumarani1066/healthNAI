<div align="center">
  <img src="https://img.icons8.com/color/120/000000/first-aid-kit.png" width="100" />
  
  # 🩺 Pratham Chikitse (First Aid)
  
  ### *Offline. Multi-lingual. Life-saving.*

  [![Kotlin](https://img.shields.io/badge/Kotlin-2.0.0-purple.svg)](https://kotlinlang.org/)
  [![Compose](https://img.shields.io/badge/Jetpack-Compose-green.svg)](https://developer.android.com/jetpack/compose)
  [![License](https://img.shields.io/badge/License-MIT-red.svg)](LICENSE)
</div>

---

## 01 — Overview
**Pratham Chikitse** is a production-grade Android application designed for high-stakes emergency response. Engineered with an **offline-first** philosophy, it acts as a pocket medical triage assistant for remote areas or zones with zero connectivity.

## 02 — Key Features
* 🤖 **AI Triage Chatbot:** Local NLP parsing maps symptoms to high-priority guidelines.
* 🗣️ **Voice-First & TTS:** Instructions read aloud in regional languages for hands-free assistance.
* 📴 **Offline Architecture:** All guides and hospital data are stored in localized JSON assets.
* 🏥 **Geo-Spatial Locator:** Finds nearest hospitals using offline boundary data.
* 🆘 **SOS Mode:** Instant shortcuts to 108, 112, 100, and 101.

## 03 — Technology Stack
| Category | Technology |
| :--- | :--- |
| **Language** | Kotlin 2.0.0 |
| **UI Toolkit** | Jetpack Compose (Material 3) |
| **Architecture** | MVVM + Clean Architecture |
| **DI** | Dagger Hilt |
| **Persistence** | Preferences DataStore + Gson |

## 04 — Project Structure
```text
app/src/main/
├── assets/             // Localized JSON Datasets
├── java/com/health/
│   ├── data/           // Repositories & Local DataSources
│   ├── ui/             // M3 Screens & ViewModels
│   └── util/           // TTS & Locale Management
└── res/                // values-kn, values-hi, values-gu...

05 — Setup & Installation
Clone the repository:

Bash
git clone https://github.com/Krishnaumarani1066/healthNAI
Open in Android Studio: Ensure you are using Koala Feature Drop or newer.

Run: Verify Gradle JDK is set to Java 17.
