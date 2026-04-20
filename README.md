# QA Portfolio — Yevhenii Suprunenko

📍 Kyiv Oblast &nbsp;|&nbsp; 📧 seamoregs@gmail.com &nbsp;

---

## About Me

I'm a Junior QA Engineer with a technical background in software development, electronics, and game design. My path to QA came naturally — throughout my personal projects and two years of teaching programming and robotics, I consistently found myself doing what QA engineers do: analyzing systems, reproducing failures, identifying root causes, and verifying fixes.

I approach testing with a developer's mindset: I understand how things are built, which makes it easier to find where they break.

**Core strengths:**
- Structured bug reporting with clear reproduction steps and priority assessment
- Exploratory testing with attention to edge cases and unexpected user behavior
- Accessibility awareness (WCAG 2.1)
- Root cause analysis and regression verification

---

## Skills

| Area | Details |
|---|---|
| **Testing** | Manual Testing, Exploratory Testing, Functional Testing, Regression Testing, Negative Testing, Smoke Testing, Sanity Testing, UI/UX Testing, Accessibility Testing, Black Box Testing, White Box Testing, Risk Based Testing, Boundary Value Analysis, Test Case Design, Bug Reporting, Bug Lifecycle |
| **Technical** | Root Cause Analysis, SDLC, OOP |
| **Tools** | Jira, GitHub, ShareX, WebAIM, Markdown, adb, Android Studio, Visual Studio |
| **Programming** | C#, C/C++, Python |

---

## Projects

### 📱 [Barcode and QR Scanner — Mobile App Testing](./qr-scanner/)

Manual QA of a real Android application.

- **Type:** Exploratory + Functional Testing
- **Platform:** Android 16 / Google Pixel 8
- **Artifacts:** 15 bug reports covering Critical → Improvement severity
- **Highlights:** Found a runtime crash with stack trace, identified a WCAG 2.1 AA contrast violation (1.08:1 vs required 4.5:1), validated app behavior against its own Play Store feature description, applied Boundary Value Analysis to identify input length limit at ~1862 characters

→ [View Bug Reports](./qr-scanner/bug-reports/)

---

### 🎮 [The Curse of Flobs — Unity Game QA](./unity-game/)

In-depth QA of a Unity game created solo in 5 days for a game jam. As both developer and tester, I had full access to the codebase, which allowed for thorough root cause analysis alongside functional and UI testing.

- **Type:** Functional Testing, UI/UX Testing, White Box Testing
- **Platform:** PC (Windows 10 22H2), Unity Build
- **Artifacts:** 43 test cases across 5 modules, 16 bug reports
- **Highlights:** Full test coverage of core gameplay loop and all 4 stages; identified a game-breaking tutorial progression bug caused by missing input lock; documented reproducible stage-blocking issue where random color spawning could make a required stage objective uncompletable

→ [View Test Cases](./unity-game/test-cases/) &nbsp;|&nbsp; [View Bug Reports](./unity-game/bug-reports/)

---

## Testing Approach

I follow a structured but flexible process:

1. **Understand the product** — read the feature description, explore the app without a script first
2. **Define scope** — identify what needs to be tested and what the acceptance criteria are
3. **Design test cases** — cover happy paths, edge cases, and negative scenarios
4. **Execute and document** — log every finding with clear steps, expected/actual results, and evidence (screenshots, logs)
5. **Prioritize** — assign severity and priority based on user impact and frequency
6. **Verify** — after fixes, retest and check for regressions

---

## Education

**Bachelor in Computer Engineering** — National Aviation University (NAU), Kyiv
*Sept 2021 – Jul 2025*

---

## Languages

- 🇺🇦 Ukrainian — Native
- 🇬🇧 English — B2
- 🇩🇪 German — A1
