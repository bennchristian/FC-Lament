@AGENTS.md

# KNOWN — project guide

Keep this file current and short: after every change, remove anything stale and fold new facts into the sections below. It is the handover; nothing else is.

**Read these first. They are the contract; this file is the running commentary:**

| File | Holds |
|---|---|
| `PRD.md` | Scope, MVP, what is deliberately out |
| `ARCHITECTURE.md` | Flow, patterns, trust boundaries |
| `SCHEMA.md` | Data contracts, off-store state |
| `DESIGN.md` | Palette, typography, voice |
| `RULES.md` | SOLID / DRY-at-4 / KISS plus the KNOWN product rules |
| `AGENTS.md` | Who does what, phase gating |
| `SKILLS.md` | Which skill wins which job |

Anything below that contradicts them is stale and should be fixed here, not there.

## 1. What this is

FC's Track 2 (Scripture Beyond the App, Activation lane) entry for the 2026 Gloo AI Hackathon. KNOWN is a private, in-the-moment Scripture experience for Esther, a displaced international Christian student. The flow is: name what she is carrying → meet a biblical person → read their words → recognize what resonates → choose a gentle response. It is currently in the design phase; the work lives in Figma, and there is no code yet.

## 2. How to work on it

- **Source of truth:** the team's SAT doc (`~/Documents/Trauma (SAT).md` on Ben's machine). If it changes, update `PRD.md` from it.
- **Figma file:** `aW0qb7r1f1bbORiKmXF6qI` (Trauma-Group). It is a Design file, so write to it with `use_figma` after loading `figma:figma-use`.
- Screen IDs (S01…) are shared across the Sitemap, User flow and User journey pages. Keep them in sync.

## 3. Gotchas that cost real time

- **Read the SAT doc before designing anything.** A first sitemap built from the app name alone invented circles, memorials, a journal and profiles. `PRD.md` §6 rules out every one of them.
- **`generate_diagram` only creates FigJam boards.** It cannot write into the Trauma-Group Design file.
- **The Figma MCP's top-level page listing omitted a page** (User flow) that exists in the file. Look pages up by id or name before assuming one is missing.
- **Overlay position is read-only in the Plugin API.** S18 is a full-screen scrim frame with the sheet pinned to the bottom, so the default centered overlay still reads as a bottom sheet.
- **The Figma prototype can't hold state.** "Continue where I left off" always resumes at S07, so don't read that as a bug.

## 4. Working with Ben

- Ben owns structure (sitemap, flows, journey).
- The mockup screenshots are an earlier revision: flow and copy follow the newer SAT doc, not the screenshots.
- Commit only when asked.
