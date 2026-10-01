# KNOWN: MoSCoW across four artifacts

One MoSCoW pass over every feature in the four KNOWN artifacts, merged into a single list.

- **Date:** October 1, 2026
- **Rated against:** `PRD.md` (scope contract) and `RULES.md` (product rules) at commit `209de61`, for the Friday prototype test (`AGENTS.md` phase 4)
- **Feature detail for artifact 2:** `KNOWN-walkthrough-features.md` in this folder

## The four artifacts

| # | Artifact | What it is | Access |
|---|---|---|---|
| 1 | [KNOWN (multilingual build)](https://claude.ai/artifact/EDweyiP3eCh48o9Jvf2mnq) | Single-phone web app, 23 screens. Three-layer feelings picker, about 65 passage entries, English, Chinese and Japanese (Burmese Scripture left blank), optional live NIV from YouVersion, AI translation of her message, Moments, reminders, and an in-app feedback form. | Someone else's, shared by link |
| 2 | [KNOWN walkthrough](https://claude.ai/artifact/JgMaUekQgh6Qg8axJuDrY5) | Ben's two-phone walkthrough. Esther's flow rebuilt from the Figma screens and copy, Hannah's companion card beside it, notes for every screen. | Ben's, shared in the org |
| 3 | [Feelings check-in](https://claude.ai/artifact/N7RrsBgEenjuXkVZpCkM1V) | Design canvas, 14 screens. Labelled emotions, 16 passages in the KJV, first-person retellings, Moments, reminders, help and settings. | Someone else's, shared in the org |
| 4 | [KNOWN Pathways](https://claude.ai/artifact/D4jo7vTBDGKvwJ661zyqJt) | Single-phone prototype with an English developer panel, 21 screens. Wordless pictures, 11 pathways (Deb's four plus seven more), four languages each with a published Bible, Moments, unfinished moments kept 3 days, help screen, dark mode. | Made outside the org, public |

## How the ratings were set

| Rating | Meaning here |
|---|---|
| **M** Must | Without it the Friday test can't answer a `PRD.md` §8 success criterion, or a `RULES.md` product rule breaks. |
| **S** Should | In the PRD, or strongly supports a §8 criterion or a §9 test question, but the test can run without it. |
| **C** Could | Helpful and low-risk. Usually not in the PRD yet, so adding it is a scope change the owner approves. |
| **W** Won't (this time) | Ruled out by `PRD.md` §6 or §7, by a recorded decision, or by a `RULES.md` rule. |

In the artifact columns, **●** means the artifact has the feature, **◐** means it has it in a different form (see the note), and **—** means it doesn't. On a W row, ● means the artifact contains something the PRD rules out.

## Summary

| | M | S | C | W | Total |
|---|---|---|---|---|---|
| Features | 20 | 15 | 14 | 13 | 62 |

| Artifact | Musts met in full (of 20) | Won't-have features it contains |
|---|---|---|
| 1 · KNOWN (multilingual build) | 12 | 11, plus translation in part |
| 2 · KNOWN walkthrough | 20 | 0 |
| 3 · Feelings check-in | 5 | 7 |
| 4 · KNOWN Pathways | 12 | 7 |

**Base the Friday prototype on artifact 2.** It is the only one that meets every Must and breaks no product rule, and the only one with the companion card.

**Worth pulling in from the others, once the owner approves:**

- From 4: the "In our words, from [reference]. The Scripture itself comes next." line (F-25), the empathy line after the pictures (F-17), *Stay with this one* on the doesn't-fit sheet (F-29), and its four published Bibles if translation comes back into scope (F-08).
- From 1: its first-person descriptions as candidate copy for Dorcas (F-11), the share-message builder (F-40), the YouVersion hook for a build (F-27), and its three feedback questions for the Friday test script (F-60).
- From 1, 3 and 4: their extra passages, as a candidate list for Deb's 16 unmapped feelings (F-22).

**Check this before treating the Won'ts as settled.** Artifacts 1, 3 and 4 share opening copy ("Carrying something you can't quite say?") and break the PRD in the same places: a Moments history, reminders (1 and 3), routing her straight to one passage, Scripture beyond Deb's four, and unreviewed crisis copy. They look like one line of work built from a different brief. Artifact 4 cites "team meeting 4" for its Psalm 77 choice. If that brief records newer team decisions, `PRD.md` is out of date and several W ratings change. Dorcas (SAT doc) and Ben should settle which brief is current.

## Decisions only the owners can make

**Ben**
- S05b: artifact 2 now offers one of four descriptions; `PRD.md` still says up to three of 6 or 12. Record whichever stands (F-11).
- The psalm path now continues to Respond in all four artifacts. Record it in `PRD.md`, which still says S09w has no Respond step (F-16).
- Confirm artifact 2 as the base for Friday.

**Deb**
- One translation for every passage (F-26). Artifact 2 mixes ESV and NIV; 1 uses the WEB; 3 uses the KJV; 4 uses the WEBBE. The KJV's older English is a reading barrier for second-language readers.
- Which psalm or psalms for "I don't have the words" (F-15).
- Whether any of the extra passages in 1, 3 and 4 should fill the unmapped feelings, especially Anger and Enjoyment (F-22).

**Dorcas**
- Which brief is current: the SAT doc behind `PRD.md`, or the one behind artifacts 1, 3 and 4.
- Voice review for anything pulled in: empathy lines (F-17), "In our words" (F-25), the message builder (F-40).
- Remove "Done for now" from the SAT doc (F-35).

**Kezia**
- Whether a help screen is a Must before real users, and its copy (F-53). None of the existing help copy has been reviewed, and all of it is US-only.
- C13, *If you're worried about her* (F-54).
- Psalm 13:3 on the no-words path (F-15).

**Team**
- Translation scope if Friday's testers are Burmese speakers. `PRD.md` §9 says Aaron's brief requires testing with students from Myanmar (F-08).

---

## A. Entry and setup

| ID | Feature | 1 | 2 | 3 | 4 | Rating | Why | Take it from / note |
|---|---|---|---|---|---|---|---|---|
| F-01 | Landing that says what KNOWN is, with no account and nothing kept | ● | ● | ◐ | ● | M | §5 entry paths; §8: she understands what KNOWN is and that it stays private | 2 for the SAT copy. 4's line "No account. What you choose stays on this device." is clearer. 3 has no privacy line. |
| F-02 | *On my own* or *With someone I trust* | ● | ● | ● | ● | M | §5 community entry | 2 |
| F-03 | Guided-use orientation: she makes every choice, the person beside her sees nothing | ● | ● | ◐ | ● | M | §5; §8: guided option understandable without a guide account | 2. 3 folds it into the choice screen. |
| F-04 | Separate ad and community entries (S01 and S02) | — | ● | — | — | S | §5 lists both; the test can run from one | 2 |
| F-05 | Invite a companion through the share sheet | ◐ | ● | — | — | S | §5 companion card | 2. 1 sends a link to KNOWN itself and asks to "walk with me through my first few times", which leans against §4.2 (at the moment, not every day). |
| F-06 | Companion card C01–C13: static, receives nothing from her phone | — | ● | — | — | S | §5, §7; §9 asks whether it helps without steering her | 2, the only one. Without it the §9 companion question can't be tested. |
| F-07 | Language picker as a placeholder | ◐ | ● | ◐ | ◐ | C | §6: picker only, choosing changes nothing | 2. In 1, 3 and 4 the picker works. |
| F-08 | Working translation: interface plus a published Bible per language | ◐ | — | — | ● | W | §6: translation out of scope | 4 has Burmese (Judson), Chinese Union and Japanese Kougo-yaku. 1 has the interface strings; its Burmese Scripture is blank. Reopen first if testers are Burmese speakers. |

## B. Naming what she's carrying

| ID | Feature | 1 | 2 | 3 | 4 | Rating | Why | Take it from / note |
|---|---|---|---|---|---|---|---|---|
| F-09 | Unlabelled pictures; she picks one or two | ● | ● | — | ● | M | §5 S05a; no-labels decision, Sept 25 | 2 for Deb's art. 1 and 4 have usable wordless pictures too. |
| F-10 | Labelled emotions and feeling words (Fear, Anxious, Grieving…) | — | — | ● | — | W | No-labels decision, Sept 25 | 3 names four emotions, then 20 feelings with a line each. |
| F-11 | First-person descriptions with no feeling words | ● | ● | ◐ | — | M | §5 S05b | 2. 1's lines are strong candidate copy for Dorcas ("I smile in class, but inside I feel very far away."). 3 pairs each line with a feeling word. 4 goes straight from pictures to a story. Open: 2 allows one of four, the PRD up to three (Ben). |
| F-12 | Descriptions written for two-picture mixes (thankful and sad, safe and guilty) | ● | ◐ | — | ● | C | Not in the PRD | 1 and 4. 2 shows both pictures' descriptions together. Dorcas and Deb. |
| F-13 | A third layer ("Who or what do you miss most?") | ● | — | — | — | W | §5 retired S05c for adding too many taps | — |
| F-14 | *None of these fit*, with typed text never read | ◐ | ● | ◐ | — | M | §5 S05n; Rule 1 | 2. 1 asks her to choose again. 4 has no descriptions to reject. |
| F-15 | *I don't have the words* leads to a psalm | ● | ● | ● | ● | M | §5 S05w | 2 offers Psalm 13 or Psalm 77:3–4. 1 and 3 use Psalm 139. 4 goes to Psalm 77:3–4 ("team meeting 4"). Deb picks; Kezia reviews Psalm 13:3. |
| F-16 | The psalm path can continue to Respond | ● | ● | ● | ● | S | Resolves TODO(Ben) on S09w | All four do it. `PRD.md` isn't updated yet. |
| F-17 | An empathy line before the story that acknowledges without naming | ◐ | — | — | ● | C | Serves "empathy first" (§2); not in the PRD | 4 never names the feeling. 1's lines sometimes do ("Your anger makes sense"). Dorcas. |

## C. Choosing who to meet

| ID | Feature | 1 | 2 | 3 | 4 | Rating | Why | Take it from / note |
|---|---|---|---|---|---|---|---|---|
| F-18 | She chooses the person from ranked matches (S06) | — | ● | — | — | M | §5: "KNOWN never picks the person for her" | 2, the only one |
| F-19 | Her tap routes straight to one passage | ● | — | ● | ● | W | Same §5 line | 1, 3 and 4 skip S06. |
| F-20 | *Show me different stories*, or another person when one doesn't fit | ◐ | ● | ◐ | ◐ | S | §5 S06 | 2. 3 swaps twice, then offers Psalm 139. 4 offers one alternate. |

## D. Scripture pathway

| ID | Feature | 1 | 2 | 3 | 4 | Rating | Why | Take it from / note |
|---|---|---|---|---|---|---|---|---|
| F-21 | Deb's four pathways: Ruth 1:6–22, Nehemiah 1:1–11, Psalm 142, Genesis 16:1–14 | ◐ | ● | ◐ | ◐ | M | §5 content | 2. 4 has the same four people with shorter excerpts inside Deb's ranges. 1 has no Hagar and uses Ruth 2. 3 has Nehemiah 1:4 and Ruth 2:10 only. |
| F-22 | Passages beyond Deb's four | ● | — | ● | ● | W | §5: "Scripture text is only what Deb chose"; Rule 3 | 1 has about 65 entries, 3 has 16, 4 has 7 more. Give the lists to Deb as candidates for the unmapped feelings, such as Habakkuk 1:2–4, Jonah 4, Psalm 126 and Psalm 131. |
| F-23 | Meet → Enter the Story → Scripture → Recognize → Respond | ◐ | ● | ◐ | ● | M | §4.4: context, then the person's words, then recognition, then response | 2 or 4. 1 shows Scripture before the context. 3 folds the context into Meet. |
| F-24 | Stories told in the third person | ● | ● | — | ● | M | Sept 25 decision; `DESIGN.md` voice | 3 speaks as the biblical person ("I was a king…"). |
| F-25 | The retelling is labelled as "in our words", apart from Scripture | — | — | — | ● | S | Rule 3: interpretation is never presented as Scripture | 4. One line of copy. Dorcas. |
| F-26 | Every passage cited with reference and translation | ● | ● | ● | ● | M | Rule 3 | Translations differ: 2 mixes ESV and NIV, 1 uses the WEB, 3 the KJV, 4 the WEBBE. Deb picks one. |
| F-27 | YouVersion Platform as the Scripture source | ◐ | — | — | — | S | §1 and §7; Track 2 judges expect it | 1 can load the NIV live with a key. In a build the key can't ship in the page (`RULES.md` security). |
| F-28 | Read the full passage or the whole chapter | ● | — | ● | ● | C | Answers the judges' "Continuation" question if it opens YouVersion | 1 opens YouVersion. 4 links to ebible.org and others. |
| F-29 | *This doesn't fit me*, with nothing recorded | ● | ● | ● | ● | M | §5 S09x | 2. 4 adds *Stay with this one*, a good Could. |
| F-30 | Recognize what resonates, with an optional note that isn't saved | ● | ● | ◐ | ◐ | M | §5 S10; §7 no retention | 2. 3 blocks *Continue* until she picks, and lets her keep it. 4 autosaves the note. |
| F-31 | "Does this connect with your moment?" | — | ● | — | — | S | §5 S10; a §9 test question | 2 |
| F-32 | A breathing pause or a one-minute sit timer | ● | — | — | ● | C | Not in the PRD | 1 and 4 |
| F-33 | "For your life now" practical suggestions | ● | — | — | — | W | Reads as advice; §8 says Respond shouldn't feel like therapy; not Deb's content | — |

## E. Respond

| ID | Feature | 1 | 2 | 3 | 4 | Rating | Why | Take it from / note |
|---|---|---|---|---|---|---|---|---|
| F-34 | Pray · Sit · Reflect · Share, each saying what it opens, each returning to Respond | ◐ | ● | ◐ | ● | M | §5 Respond options | 2 or 4. 1 and 3 swap in Write, Reach out and Keep. |
| F-35 | *Done for now* or *Finish* on Respond | ● | — | ● | ● | W | Removed Sept 25 (Ben) | The SAT doc still lists it (Dorcas). |
| F-36 | A prayer direction she can make her own | ● | ● | ● | ● | M | §5 Pray about it | Any. What she types isn't saved. |
| F-37 | *Save this prayer* through the share sheet, with no copy kept | — | ● | — | ◐ | S | §5 S12; §7 | 2. 4 saves it to Moments. |
| F-38 | Reflect: a short field that is never saved | ◐ | ● | ◐ | ◐ | M | §5; §7 no retention | 2. 1, 3 and 4 let her keep it. |
| F-39 | Share: an editable message she sends herself | ● | ● | ◐ | ◐ | M | Rule 2 | 2 for the test (simulated share sheet and contacts). 1 opens the phone's real share sheet, useful for a build. 3 and 4 copy to the clipboard. |
| F-40 | Message builder: how much to share, and what would help | ● | — | — | — | C | Supports §4.5, no forced disclosure; not in the PRD | 1. Dorcas. |
| F-41 | *Add the verse I read* to the message | ◐ | — | — | ● | C | Not in the PRD | 4 |
| F-42 | AI translation of her message | ● | — | — | — | W | `RULES.md` security: never transmit free text; §6 | — |

## F. Leaving, saving and closing

| ID | Feature | 1 | 2 | 3 | 4 | Rating | Why | Take it from / note |
|---|---|---|---|---|---|---|---|---|
| F-43 | Close (X) on every screen, opening *Stop for now?* | — | ● | — | ● | M | §5 Leaving; she can stop anywhere | 2 or 4. 1 and 3 have back and home only. |
| F-44 | *Save this step for later*: step and person only, only when she taps | ◐ | ● | — | ◐ | S | §7; `SCHEMA.md` UnfinishedMoment | 2. 1 saves on every screen. 4 also saves her words. |
| F-45 | Autosave of what she typed (prayer, notes) | ● | — | — | ● | W | Data rule: only UnfinishedMoment is stored; §7 | — |
| F-46 | An unfinished step expires after 3 days | ● | — | — | ● | C | Strengthens privacy; needs a `SCHEMA.md` change | 1 and 4 |
| F-47 | Welcome back: continue or start new | ● | ● | — | ● | S | §5 States | 2 |
| F-48 | Closing screen with no streak, history or reminder | ◐ | ● | ◐ | ◐ | M | §5 Closing state; Rule 4 | 2. The others point her to Moments. |
| F-49 | Another story (S19, S19a) | — | ● | — | — | C | §9 asks whether anyone uses it; S19a is still a placeholder | 2. Deb researches S19a or drops it. |
| F-50 | Moments: saved passages, prayers, reflections and messages | ● | — | ● | ● | W | Rule 4 (history, counters); §7 no retention of written text; §5 S12 has no saved-prayers list | — |
| F-51 | A "what to keep" screen before she leaves | ● | — | ● | ● | W | Depends on Moments | — |
| F-52 | Reminders ("A gentle check-in", weekly to monthly) | ● | — | ● | — | W | §6 no push notifications or scheduling; Rule 4; §4.2 | — |

## G. Safety

| ID | Feature | 1 | 2 | 3 | 4 | Rating | Why | Take it from / note |
|---|---|---|---|---|---|---|---|---|
| F-53 | *Need help now?*: emergency number, 988, findahelpline.com, school counseling, "KNOWN can't respond in an emergency" | ● | — | ● | ● | S | Rule 5: safety copy needs Kezia's review before it enters a mockup; §6: not a crisis service | Kezia decides whether this is a Must before real users. All existing copy is unreviewed and US-only. |
| F-54 | Companion safety: *She wants to stop* (C12) and *If you're worried about her* (C13) | — | ● | — | — | S | §5 companion card | 2. C13 is a placeholder for Kezia. |

## H. Look and feel

| ID | Feature | 1 | 2 | 3 | 4 | Rating | Why | Take it from / note |
|---|---|---|---|---|---|---|---|---|
| F-55 | KNOWN's palette and type from `DESIGN.md` (Crimson Pro, DM Sans) | — | ● | — | — | S | `DESIGN.md` | 2, in a dark version. 1 uses Literata and Atkinson Hyperlegible; 3 and 4 use Libre Baskerville and DM Sans. |
| F-56 | Dark mode | — | ● | ● | ● | C | `DESIGN.md` defines light values only | 4 follows the device and has a toggle. 2 and 3 are dark only. |
| F-57 | A progress bar within one moment | — | ● | — | — | C | `DESIGN.md` bans progress across sessions only | 2 |
| F-58 | Scene art for each pathway | — | ◐ | ● | ● | C | Illustrator TODO | 2 has Ruth only. 3 and 4 have simple placeholder art. |
| F-59 | Simulated phone screens, marked SIMULATED | — | ● | — | — | S | Shows in a browser test that KNOWN never sends | 2 |

## I. Testing and review tooling

| ID | Feature | 1 | 2 | 3 | 4 | Rating | Why | Take it from / note |
|---|---|---|---|---|---|---|---|---|
| F-60 | Feedback form inside KNOWN, sent to a team database | ● | — | — | — | W | Rule 6: it needs a user id; `RULES.md` security: it sends free text | Use its three questions in the Friday test script instead. |
| F-61 | Two phones side by side, notes, stage jumps | — | ● | — | — | C | For team review and a judges' demo, not the tester's view | 2 |
| F-62 | Developer QA panel: time travel, state, sitemap | — | — | — | ● | C | Tooling only | 4 |
