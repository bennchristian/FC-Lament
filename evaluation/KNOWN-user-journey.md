# KNOWN: user journey for the consolidated prototype

Screen by screen, from the first screen to the last, for the one prototype in `KNOWN-consolidated-prototype.md`. Screen IDs match the Figma file and `ARCHITECTURE.md`.

- **Date:** October 1, 2026
- **Journey stages:** the ten stages the companion card already follows (C01–C10)
- **List #** refers to the feature numbers in `KNOWN-consolidated-prototype.md`

## The main path at a glance

Landing → How are you using KNOWN? → Using KNOWN together → Pictures → Closest description → Who to meet → Meet → Enter the Story → Scripture → Recognize → Respond → Pray, Sit, Reflect or Share → Closing

## Verdict

The flow holds together. Every stage is one screen, she chooses at every step, and the features taken from artifacts 1 and 4 fit onto screens that already exist. The only new screen is *Need help now?*. Two things need fixing before Friday: only the Share path reaches the closing screen, and the road to Scripture is long for someone in a hard moment.

## Flow findings

| # | Finding | Why it matters | Recommendation | Owner |
|---|---|---|---|---|
| 1 | Only Share reaches the closing screen (S17). Pray, Sit and Reflect end with *Back to Respond* or the X. | The X asks "Stop for now?", which reads as quitting halfway. Three of four endings skip the thank-you and *Another story*. | Add one quiet way to finish from Pray, Sit and Reflect that leads to S17, such as *Amen* on Pray (artifact 1 does this). This partly reverses the Sept 25 removal of *Done for now*, and `PRD.md` already asks Ben to confirm S17 only after a share. | Ben (copy: Dorcas) |
| 2 | Scripture is the 8th screen from a community link and the 7th from an ad. Three choice screens come first (S05a, S05b, S06). | KNOWN is for the moment itself. Every extra tap before the encounter is a chance to give up. | Keep S05b to one choice (artifact 2's current version). Put the empathy line at the top of S06 instead of on its own screen, as artifact 4 does. Add no screens before S09. | Ben |
| 3 | Welcome back always resumes at Ruth's S07 in the Figma prototype. | A tester who chose Hagar, saved and reopened lands on Ruth, and will read it as a bug. | Test resume in artifact 2, which resumes at the saved step, or warn facilitators in the test script. | Ben |
| 4 | *Another angle* (S19a) is a placeholder. | A dead end on Friday. | Hide the option until Deb has content for it. | Deb, Ben |
| 5 | *Need help now?* would sit in the top bar beside the X on every screen. | Two corner controls can blur "stop" and "get help". | Kezia decides the placement and every word. Options: a quiet link in the top bar, or an option inside the *Stop for now?* sheet. | Kezia |
| 6 | The psalm path skips stages 3 to 8, so the companion card falls out of step. | The companion may read lines that don't match her screen. | Already handled: C02 tells the companion to go to Step 9. Watch for it in testing (`PRD.md` §9). | Team |

## The journey, screen by screen

| Step | Screen | What's on it | What she can do next | Companion card | List # |
|---|---|---|---|---|---|
| **Stage 1 · Begin** | | | | | |
| 0 | S04 Welcome back | Shown only if she saved a step last time. | *Continue where I left off* → the saved screen. *Start a new moment* → S01 or S02. | — | 37 |
| 1a | S01 Landing (from an ad) | What KNOWN is, with the line "No account. What you choose stays on this device." Language picker. | *Begin* → S05a | — | 1, 2, 7 |
| 1b | S02 Landing (from a community link) | "How are you using KNOWN right now?" Language picker. | *With someone I trust* → S03. *On my own* → S05a. | — | 2, 3, 7 |
| 2 | S03 Using KNOWN together | She makes every choice. The person beside her can't see them. | *Invite someone to accompany you* → her share sheet (OUT-6a, OUT-6b) → back to S03. *Start* → S05a. | C01 | 4, 5, 6 |
| **Stage 2 · Images** | | | | | |
| 3 | S05a Pictures | Four wordless images. Progress bar starts here. | Pick one or two → *Continue* → S05b. *I don't have the words* → S05w (psalm path). | C02 | 8, 12, 43 |
| **Stage 3 · Closest feeling** | | | | | |
| 4 | S05b Closest description | First-person lines from the pictures she chose, with no feeling words. Lines for mixed feelings when she chose two. | Pick one → *Continue* → S06. *None of these fit* → S05n → S06 · All four. | C03 | 9, 10, 11 |
| **Stage 4 · Choose a person** | | | | | |
| 5 | S06 Who to meet | Empathy line at the top that doesn't name a feeling. Best matches, ranked by her choice. | Pick a person → S07. *Show me different stories* swaps the list. | C04 | 14, 15, 16 |
| **Stage 5 · Meet** | | | | | |
| 6 | S07 Meet | Who the person was, told in the third person, with an illustration. | *Enter the story* → S08 | C05 | 17, 19, 45 |
| **Stage 6 · Story** | | | | | |
| 7 | S08 Enter the Story | The situation before the words, with references. Closing line: "In our words, from [reference]. The Scripture itself comes next." | *Read the Scripture* → S09 | C06 | 18, 20 |
| **Stage 7 · Scripture** | | | | | |
| 8 | S09 Scripture | Their own words, with reference and one translation. *Read the whole passage* link. | *I'm ready* → S10. *This doesn't fit me* → S09x: meet someone else (S06 · All four), choose a different feeling (S05a), or *Stay with this one* (S09). | C07 | 21, 22, 23 |
| **Stage 8 · Recognize** | | | | | |
| 9 | S10 Recognize | What stood out, as taps, or *Something else*, with an optional note that isn't saved. Then "Does this connect with your moment?" with four answers. | *Continue* → S11. *Not really* also offers *Meet someone else*. | C08 | 24, 25 |
| **Stage 9 · Respond** | | | | | |
| 10 | S11 Respond | Pray, Sit, Reflect or Share, each saying what it opens. | → S12, S13, S14 or S15 | C09 | 26 |
| 11a | S12 Pray about it | A prayer direction for this person's story. *Save this prayer* link. | *Save this prayer* → her share sheet (OUT-7) → S12. *Back to Respond*. | — | 27, 28 |
| 11b | S13 Sit with it | A quiet screen. Optional one-minute pause. | *Back to Respond* | — | 29 |
| 11c | S14 Reflect a little more | A 280-character field that is never saved. | *Back to Respond* | — | 30 |
| 11d | S15 Share: you're in control | She chooses who and what. KNOWN never sends. | Contact picker (OUT-3a) → S16 | — | 31 |
| 11e | S16 Your message | An editable starting message. Choose how much to share and what would help. *Add the verse I read*. | Review and send in her messaging app (OUT-3b) → S17 | — | 31, 32, 33 |
| **Stage 10 · Close** | | | | | |
| 12 | S17 Closing | "Thank you for taking this moment." No streak, history or reminder. One quiet link: *If you'd like, there's another story*. | *Another story* → S19: someone else in Scripture (S06 · All four), or another angle (S19a). | C10, then C11 | 38, 39 |

## Side paths

| When | Path | Comes back to |
|---|---|---|
| She has no words to name it | S05a → S05w: Psalm 13 or Psalm 77:3–4 → S09w, the psalm itself, with the option to read the other | S11 Respond; S12 shows a prayer written for the psalm path |
| None of the descriptions fit | S05b → S05n: name it another way (what she types is never read) | S06 · All four |
| The story doesn't fit | S09 → S09x | S06 · All four, S05a, or back to S09 |
| She wants to stop, on any screen | X → S18 *Stop for now?* → *Save this step for later* (step and person only) or *End without saving* | Her phone's home screen (OUT-5a or OUT-5b). Next time: S04 Welcome back |
| She needs help now, on any screen | *Need help now?* → the help screen (new; Kezia writes it) | The screen she left |
| The companion, at any step | C12 *She wants to stop* or C13 *If you're worried about her* (Kezia) | The step they left |
