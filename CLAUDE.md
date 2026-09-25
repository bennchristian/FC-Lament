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

FC's Track 2 (Scripture Beyond the App, Activation lane) entry for the 2026 Gloo AI Hackathon. KNOWN is a private, in-the-moment Scripture experience for Esther, a displaced international Christian student. The flow is: name what she is carrying (up to two unlabelled images, then up to three descriptions) → meet a biblical person → read their words → recognize what resonates → choose a gentle response. If she goes through it with someone, a static companion card (C01–C13) on that person's phone walks them through the same ten stages without ever seeing her choices. It is currently in the design phase; the work lives in Figma, and there is no code yet.

## 2. How to work on it

- **Source of truth:** the team's SAT doc (`~/Documents/Trauma (SAT).md` on Ben's machine). If it changes, update `PRD.md` from it.
- **Figma file:** `aW0qb7r1f1bbORiKmXF6qI` (Trauma-Group). It is a Design file, so write to it with `use_figma` after loading `figma:figma-use`.
- Screen IDs (S01…) are shared across the Sitemap, User flow and User journey pages. Keep them in sync.

## 3. Gotchas that cost real time

- **Read the SAT doc before designing anything.** A first sitemap built from the app name alone invented circles, memorials, a journal and profiles. `PRD.md` §6 rules out every one of them.
- **`generate_diagram` only creates FigJam boards.** It cannot write into the Trauma-Group Design file.
- **The Figma MCP's top-level page listing omitted a page** (User flow) that exists in the file. Look pages up by id or name before assuming one is missing.
- **Overlay position is read-only in the Plugin API.** S18 is a full-screen scrim frame with the sheet pinned to the bottom, so the default centered overlay still reads as a bottom sheet.
- **The Figma prototype can't remember where she stopped.** "Continue where I left off" always resumes at Ruth's S07, so don't read that as a bug. Its session variables (collection "Prototype state") are `pathway`, the `connect*` set for S10, `offerAnother`, and the multi-select set for S05a/S05b/S06 (`img/*`, `feel/*`, `feelCount`, `justUnchecked`, `score/*`, `show/*`, `showSwap`). `ARCHITECTURE.md` §6 lists what each one does.
- **Figma conditionals keep only if/else, and they can't be nested.** Multi-way routing ("Back to Respond") is four separate single-block CONDITIONAL actions chained in one reaction.
- **Cloning a lane copies Deb's illustration images and any deleted instance children.** Run `resetOverrides()` on the Illustration instance, then set the caption again.
- **A .webp uploaded as an image fill didn't render.** Convert it to PNG before `upload_assets`.
- **Ben's newer mockup screenshots aren't in the Figma file.** Search before assuming a frame exists. The companion lane was built from scratch at x=7000. Esther's invite is an option on S03, not a separate choice screen like the mockup's, because S02 keeps the SAT copy.
- **One prototype link crosses phones:** OUT-6b's "Prototype only: see what Hannah receives →" jumps to C01. Its Send goes back to S03, so Esther's own flow stays intact.
- **Companion copy must work whatever Esther picks.** The card can't know her feeling or pathway. The mockups named David and Psalm 142 and assumed "lonely"; those were removed.
- **Crimson Pro Italic has no ⚑ glyph.** It renders as nothing in `KNOWN/Placeholder` text, so put Kezia flags in a note card instead.
- **The `plugin:figma` MCP server may ask for auth when the other Figma MCP server (`use_figma`) already works.** Check with ToolSearch before telling Ben the file is unreachable.
- **The flow lines on the journey page are a locked vector group** ("Flow lines…"). If you move screens, redraw them; they don't follow frames. Newer screens (S09x, S19, OUT-7) have no line; only their prototype links exist.
- **Setting `scopes` on a new variable in the "Prototype state" collection throws "Invalid scope"**, even `[]`. Leave the default.
- **The S05a illustrations are absolute rectangles sitting on top of the old Image tiles,** so taps hit the image, not the tile. The checkbox hotspots are the transparent "Select · <emotion>" frames above each image.
- **A Choice row's `Selected` variant can be bound to a boolean variable** with `instance.setProperties({Selected: {type:'VARIABLE_ALIAS', id}})`. That is how the S05b checkboxes work, with no extra frames.
- **The live S05b looks empty on the canvas,** because its groups stay hidden until `img/*` is set. Review it on "S05b · Preview for review". If you edit S05b, redo the preview too.
- **To screenshot S10's connection prompt, set the `connect*` variable defaults temporarily, then restore them.** Do it in its own `use_figma` call. Mixing it with reaction edits threw an "unexpected error" and rolled back the whole call.

## 4. Working with Ben

- Ben owns structure (sitemap, flows, journey).
- The mockup screenshots are an earlier revision: flow and copy follow the newer SAT doc, not the screenshots.
- Commit only when asked.
