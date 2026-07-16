<p align="center">
  <img src="icons/icon-192.png" alt="Luminaria" width="96" height="96" />
</p>

<h1 align="center">Luminaria · 浮光词集</h1>

<p align="center">
  <strong>Vocabulary learning reimagined as an aesthetic experience.</strong><br />
  <em>26,000+ words · FSRS algorithm · French Dispatch-inspired · Offline PWA</em>
</p>

<p align="center">
  <a href="https://onion-create.github.io/luminaria-vocab/"><strong>🌐 Live Demo</strong></a> &nbsp;&nbsp;
  <a href="LICENSE"><img src="https://img.shields.io/badge/license-proprietary-red.svg" alt="License" /></a>
  <a href="#"><img src="https://img.shields.io/badge/words-26,000%2B-blue.svg" alt="Words" /></a>
</p>

---

## Why This Exists

Most vocabulary apps force an impossible choice: **scientific rigor** with a punishing interface (Anki), or **shallow engagement** dressed up as learning (gamified alternatives). Neither treats the learning moment itself as something worth enjoying.

Luminaria starts from a different premise: **beauty and comfort are retention mechanisms, not decoration.** The words drift across the screen in a deliberate, meditative rhythm. The color palette is borrowed from Wes Anderson's French Dispatch. The science underneath is FSRS — the state-of-the-art spaced repetition algorithm that outperforms Anki's SM-2. Every visual decision was made with one question in mind: "Does this make someone want to stay here five more minutes?"

Built solo, end-to-end, using Codex CLI, Claude Code CLI, and WorkBuddy — from architecture to deployment. No design team. No engineering team. Just an idea and the conviction that learning tools don't have to look like work.

---

## Features

| Category | Details |
|----------|---------|
| 🧠 **Algorithm** | FSRS (Free Spaced Repetition Scheduler) — outperforms Anki's SM-2 in retention efficiency. Adaptive per-learner scheduling. |
| 🎨 **Visual Identity** | French Dispatch-inspired palette (wine, rose, gold, lavender). 8 distinct CSS motion-design families. Glassmorphism UI. |
| 📚 **Content** | 26,000+ words across 8 banks: CET-4, CET-6, GRE, TOEFL, IELTS, SAT, Postgraduate (考研), Business English. |
| 🌐 **Bilingual** | Full English and Chinese UI. Bilingual word definitions with pronunciation. |
| 📱 **PWA** | Install to home screen. Works offline — all data stored locally (IndexedDB + JSON schema). No account required. |
| 🔬 **FSRS Visualization** | Real-time memory-state indicators with customizable color coding. Mastered words fade elegantly. |
| ⚡ **Performance** | Single-file HTML, zero framework dependencies. Hardware-accelerated CSS (transform3d) for fluid 60 FPS motion on low-spec devices. |

---

## Tech Stack

| Layer | Technology |
|-------|-----------|
| **Core** | Single-file HTML + Vanilla JS |
| **Rendering** | Canvas 2D API, SVG, CSS keyframe animations |
| **Algorithm** | FSRS (fsrs.js) — spaced repetition |
| **Storage** | IndexedDB + structured JSON schema (offline-first) |
| **Distribution** | PWA (Service Worker, Web App Manifest), GitHub Pages |
| **Build Toolchain** | Codex CLI, Claude Code CLI, WorkBuddy |

---

## Project Structure

```
luminaria-vocab/
├── index.html          # Main application (~1.1MB, single-file PWA)
├── manifest.json       # PWA manifest
├── sw.js              # Service Worker for offline caching
├── wb_data.json       # Word bank runtime data
├── banks/             # Vocabulary source data (8 JSON files)
│   ├── cet4.json      #   College English Test Band 4
│   ├── cet6.json      #   College English Test Band 6
│   ├── gre.json       #   Graduate Record Examination
│   ├── toefl.json     #   Test of English as a Foreign Language
│   ├── ielts.json     #   International English Language Testing System
│   ├── sat.json       #   Scholastic Assessment Test
│   ├── ky.json        #   考研英语 (Postgraduate Entrance Exam)
│   └── biz.json       #   Business English
├── avatars/           # User profile avatars (54 icons)
├── icons/             # PWA icons (10 sizes)
├── LICENSE            # Source-available proprietary license
├── EULA.txt           # End User License Agreement (bilingual)
└── README.md          # This file
```

---

## Quick Start

```bash
# Clone the repository
git clone https://github.com/onion-create/luminaria-vocab.git

# Open in browser — no build step, no dependencies
open luminaria-vocab/index.html

# Or serve locally
python3 -m http.server 8080
# → http://localhost:8080
```

Add to your phone's home screen for a native app experience — works offline.

---

## Attribution

- **FSRS Algorithm** — Based on [open-spaced-repetition/fsrs.js](https://github.com/open-spaced-repetition/fsrs.js). This project uses the algorithm's integration layer and configuration. The surrounding application logic, visual identity, and curated vocabulary data are original work.
- **Typography** — Playfair Display served via Google Fonts (OFL license).
- **Avatars** — AI-generated illustrations created for this project.

---

## License

**Proprietary — All Rights Reserved.** See [LICENSE](LICENSE) for full terms.

- ✅ View the source code for learning and evaluation
- ✅ Install and use for personal, non-commercial vocabulary learning
- ❌ Redistribute, modify, or use commercially without written permission

For commercial licensing inquiries, contact the author.

---

<p align="center">
  <sub>Made with precision by <strong>袁铭 (Yuan Ming)</strong> · © 2026 All rights reserved.</sub>
</p>
