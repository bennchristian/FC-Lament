# DESIGN — KNOWN

> BMAD is not installed. Tokens below were **sampled from the earlier mockup screenshots (Sept 23)**
> and live as the `KNOWN` variable collection and `KNOWN/*` text styles in the Figma file.
> Confirm them against the mockup's source file if one exists.

## Brand identity

- **Name:** KNOWN, always in capitals in product copy.
- **Feel:** a quiet, private place to be honest before God. Calm rather than cheerful, and spiritually grounded without rushing to resolution.

## Color

The existing system is **brown, cream and muted blue** (SAT doc).

| Token | Role | Value |
|---|---|---|
| `color/bg` | Cream screen background | `#FAF5F0` |
| `color/surface` | Cards, rows, inputs | `#FBFAF6` |
| `color/surface-soft` | Note cards, illustration placeholder | `#F4EAE2` |
| `color/selected` | Selected choice row | `#F1E3D5` |
| `color/chip` | Unselected word chip | `#ECE4DD` |
| `color/primary` | Brown primary button, selected chip | `#82543C` |
| `color/on-primary` | Text on primary | `#FAF5F0` |
| `color/secondary` | Secondary button | `#F5E7DC` |
| `color/ink` | Headings (deep muted blue) | `#1B2638` |
| `color/body` | Body text (slate blue) | `#475467` |
| `color/wordmark` | KNOWN wordmark | `#5A2F28` |
| `color/icon` | Line icons | `#644A3E` |
| `color/border` | Hairlines | `#E6DDD3` |
| `color/placeholder` | **Design-phase only:** marks content still owed by Deb | `#9A5B45` |

"Muted blue" in the SAT doc shows up as the ink and body text colors, not as a fill.

## Typography

| Style | Font | Size / line height | Use |
|---|---|---|---|
| `KNOWN/Wordmark` | Crimson Pro Regular | 14, +60% tracking | KNOWN wordmark |
| `KNOWN/Display` | Crimson Pro Regular | 30 / 115% | Screen headings |
| `KNOWN/Heading` | Crimson Pro Regular | 24 / 120% | Subheadings |
| `KNOWN/Scripture` | Crimson Pro Regular | 20 / 140% | Passage text |
| `KNOWN/Body` | DM Sans Regular | 15 / 145% | Body |
| `KNOWN/Body strong` | DM Sans Medium | 15 / 145% | Emphasis |
| `KNOWN/Caption` | DM Sans Regular | 13 / 140% | Captions |
| `KNOWN/Button` | DM Sans Medium | 16 | Buttons |
| `KNOWN/Placeholder` | Crimson Pro Italic | 15 | `[bracketed]` placeholders |

- The serif is a close match to the mockup, not confirmed. TODO(Dorcas): confirm the typefaces.
- Readability comes first: body text is never below 13px.

## Spacing and layout

- Mobile first, 390 × 844 frames in Figma.
- One primary action per screen. Choices stack vertically with generous tap targets.
- TODO: spacing scale.

## Motion

Minimal. No celebratory animation, confetti or streak effects. Transitions should be slow and soft. TODO: durations.

## Content voice (from the SAT doc — binding)

- Warm, calm and direct.
- Spiritually grounded without rushing to correction or resolution.
- Short enough to read during an emotionally difficult moment.
- Invitational rather than clinical, commanding or overly cheerful.
- Clear about privacy, choice, and what the tool can and cannot do.
- Never diagnose, never label a situation as a crisis, never promise a recipient will respond, never imply KNOWN monitors her.
- **Biblical people speak in first person** on S06–S09 ("I stepped into a new life…"). KNOWN's own voice stays second person ("Meet Ruth in this moment", "Take a moment to read them again").
- **Quoted Scripture** stays word for word, in quotation marks, with references, so a retelling is never mistaken for Scripture.
- **Recognize (S10)** options are Esther's own observations, so they keep "he" and "she" (e.g. "He tells God plainly that he feels alone").

## Anti-patterns

- Streaks, badges, progress bars across sessions, or "you've completed N moments."
- Emotion scores, mood graphs, or anything that reads as tracking.
- Scripture text that is not visibly cited (reference + translation).
- Guilt or urgency copy ("Don't give up!", "Come back tomorrow").

## Accessibility

- TODO: contrast check of the brown/cream/blue palette against WCAG AA once the values are known.
- Every choice is reachable without typing; free text is always optional.
- TODO(team): language and translation, the main contextualization lever for Track 2 bonus points. Out of MVP (`PRD.md` §6).
