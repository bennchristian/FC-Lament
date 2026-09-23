# ARCHITECTURE — KNOWN

> Scope comes from `PRD.md`. BMAD is not installed. This file records only what the SAT doc
> fixes; every implementation choice is still a TODO.

## 1. System overview

The first prototype is a **clickable Figma prototype**, not running code. The design-phase artifacts live in the Figma file linked in `PRD.md`:

- **Sitemap:** every screen, with a screen ID.
- **User flow:** the four flows (independent, community-guided, pause and return, Respond branches).
- **User journey (mockup):** the clickable prototype.

TODO(team): decide whether the Friday test uses the Figma prototype or a coded build. If coded, choose the stack and record it here and in `RULES.md`.

## 2. Components (target build)

| Component | Responsibility | Source |
|---|---|---|
| Client app | All screens and flow logic | TODO: stack |
| Scripture layer | Passage text, reference and translation for each pathway | YouVersion Platform (Track 2 expectation). TODO: API access and licensing |
| Pathway content | The biblical person, story context, Recognize choices, prayer direction | Authored by Deb, stored as static content bundled with the app |
| Device-local state | Unfinished-moment step only | See `SCHEMA.md` |
| Share | Editable message handed to the OS share sheet | Platform share API. KNOWN never sends |

There is **no backend, no account system and no analytics** in the prototype.

## 3. Data flow

```
Entry (ad link | community QR/link)
  → [launch] unfinished moment on device? ── yes → Welcome back → continue | start new (deletes it)
  → Independent entry  |  Community entry choice → (with someone) Guided orientation
  → S05 Name what you're carrying → user SELECTS words → cluster
       (Transition: bittersweet/homesick/uncertain · Isolation: lonely/disconnected/unseen)
  → S06 Choose who to meet → user PICKS a person → pathwayId
       (Transition: Ruth | Nehemiah · Isolation: David | Hagar · both/something else: all four)
  → Meet → Enter the Story → Scripture (YouVersion text) → Recognize → Respond
  → Pray | Sit | Reflect (in-memory only) | Share (OS share sheet) | Done → Closing
Exit at any step → Unfinished moment → save {step, pathwayId} | end without saving
```

## 4. Key design decisions

1. **Routing is by the user's selection, never by inference.** A fixed, human-authored table maps each word to a cluster. The cluster decides which people S06 shows, and Esther picks the pathway herself. Free text never influences routing.
2. **No model interprets Scripture.** If an LLM is ever used, it may not choose passages, paraphrase them, or produce interpretation presented as Scripture.
3. **The guide is outside the system.** No guide identity, session count or schedule is stored. Any guide dashboard is out of scope (`PRD.md` §6).
4. **Minimum retention.** Only the step and the pathway id persist, only on the device, and starting a new moment clears them.

## 5. Trust boundaries

- Free-text fields (Recognize "Something else", Reflect a little more, the share message) never leave the device except through Esther's own send action in the OS share sheet.
- Safety or crisis copy is changed only after Kezia's review.

## 6. Open questions

- TODO(team): stack for the coded prototype, if there is one.
- TODO(team): YouVersion Platform API access, translation choice, licensing terms.
- TODO(Dorcas/Deb): confirm that words from both clusters, or only "Something else", should show all four people. The prototype does this now.
- **Prototype limits:**
  - "Continue where I left off" always resumes at Ruth's S07; the real build resumes at the saved step.
  - The prototype stores her S06 choice in a Figma variable `pathway`, so "Back to Respond" on the shared screens returns to her own S11.
  - On S05 she can switch between word groups but can't combine them.
