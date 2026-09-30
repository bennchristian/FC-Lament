# KNOWN walkthrough: feature list

Every feature in the KNOWN walkthrough artifact, ready for a MoSCoW pass alongside other artifacts.

- **Artifact:** https://claude.ai/artifact/JgMaUekQgh6Qg8axJuDrY5 (version 2, September 30, 2026)
- **Built from:** the Trauma-Group Figma file, plus the changes Ben asked for on September 30

## How to use this list

Fill the **MoSCoW** column with one letter per row:

| Letter | Meaning |
|---|---|
| M | Must have |
| S | Should have |
| C | Could have |
| W | Won't have (this time) |

The **Source** column says where each feature comes from:

| Source | Meaning |
|---|---|
| Figma | In the Figma prototype as it stands |
| Figma · placeholder | In Figma, but the content is still owed |
| New in v2 | Added in the artifact on September 30. Not yet in Figma or `PRD.md` |
| Artifact only | Works differently in the artifact than in Figma, or exists only in the artifact |

IDs use the prefix `KW-` (KNOWN walkthrough) so they stay distinct when compared with other artifacts' lists. Sections A–I are product features. Section J is the walkthrough tooling around the phones, which is not part of the product.

---

## A. Entry and return

| ID | Feature | What it does | Screens | Source | Open items | MoSCoW |
|---|---|---|---|---|---|---|
| KW-01 | Independent entry | Landing for someone arriving from an ad or shared post. Says what KNOWN is, that no account is needed and nothing is kept, then *Begin →*. | S01 | Figma | — | |
| KW-02 | Community entry choice | Opened by a QR code or link from someone she trusts. *With someone I trust* or *On my own*. | S02 | Figma | — | |
| KW-03 | Guided-use orientation | Sets the terms for going through it together: she makes every choice, and the person beside her can't see them. | S03 | Figma | — | |
| KW-04 | Invite a companion | From S03, she sends a companion link through her phone's share sheet, edits the invite, sends it herself, and returns to S03. | S03 → OUT-6a → OUT-6b | Figma | Dorcas: invite text is DRAFT. Team: link names Esther and Hannah; a build needs a generic link | |
| KW-05 | Language picker | Pill on S01 and S02 opens a language sheet. Choosing a language changes nothing yet. | S00L | Figma · placeholder | Team: translation scope, YouVersion translations | |
| KW-06 | Welcome back | On reopening after a saved step: *Continue where I left off* or *Start a new moment*. | S04 | Figma | Artifact resumes at the saved step; Figma always resumes at Ruth's S07 | |

## B. Naming what she's carrying

| ID | Feature | What it does | Screens | Source | Open items | MoSCoW |
|---|---|---|---|---|---|---|
| KW-07 | Unlabelled emotion images | Four illustrations, one each for fear, anger, sadness and enjoyment (Ekman's Atlas of Emotions). She picks one or two. No emotion names are shown. | S05a | Figma | — | |
| KW-08 | Four descriptions, single choice | After the images, four first-person descriptions from the image or images she chose. She picks the one closest to her moment. Each carries a hidden feeling tag. | S05b | New in v2 | Figma shows 6 or 12 and allows up to 3. Deb: choose the four per image (artifact uses strongest passage fit, which drops Homesick). Dorcas: new instruction line (DRAFT). Kezia: Dread and Helpless can appear | |
| KW-09 | Name it another way | Sheet for when none of the descriptions fit. What she types is never read or used to route; she sees all four people. | S05n | Figma | — | |
| KW-10 | "I can't explain it right now" | Quiet link under *Continue* on S05a, for someone too overwhelmed to name anything. | S05a → S05w | New in v2 | Wording was "I don't have the words to explain how I feel". Dorcas: voice | |
| KW-11 | Psalm choice | Asks for nothing and offers two psalms: Psalm 13 and Psalm 77:3–4. | S05w | Figma | Deb: confirm psalms. Kezia: review before testing | |
| KW-12 | Psalm reading | The psalm, cited and word for word, with an option to read the other psalm. No tag is set; nothing is recorded. | S09w | Figma | Kezia: Psalm 13:3 "or I will sleep in death". Deb: translation ("NIV?" on screen) | |
| KW-13 | Psalm path goes to Respond | After a psalm, *I'm ready →* leads to Respond (pray, sit, reflect, share), not to meeting a person. | S09w → S11 | New in v2 | Figma sends her to S06 · All four | |
| KW-14 | Prayer direction after a psalm | S12 shows a prayer direction written for the psalm path, since the others belong to a pathway. | S12 | New in v2 | Deb: review (Claude DRAFT) | |

## C. Choosing who to meet

| ID | Feature | What it does | Screens | Source | Open items | MoSCoW |
|---|---|---|---|---|---|---|
| KW-15 | Tag-based ranking | Stories are ranked by the hidden tag on the description she chose, weighted by Deb's fit ratings (5 very strong … 1 indirect). No inference, no text analysis. | S05b → S06 | Figma (v2: one tag instead of up to three) | Deb: confirm weights; 16 of 24 feelings have no passage yet | |
| KW-16 | Best matches | S06 shows the stories her tag matches, ties included. She picks the person herself. | S06 | Figma | Art: four cards still show [art] | |
| KW-17 | Show me different stories | Swaps to the stories not shown. | S06 | Figma | — | |
| KW-18 | All four | All four people, after she names it another way, leaves a story, or picks a description with no passage. | S06 · All four | Figma | — | |
| KW-19 | Best match listed first | Cards are sorted by score. | S06 | Artifact only | Figma keeps a fixed order because it can't sort | |

## D. Scripture pathways

| ID | Feature | What it does | Screens | Source | Open items | MoSCoW |
|---|---|---|---|---|---|---|
| KW-20 | Four researched pathways | Ruth (Ruth 1:6–22) and Nehemiah (Nehemiah 1:1–11) for Transition; David (Psalm 142) and Hagar (Genesis 16:1–14) for Isolation. | S07–S12 × 4 | Figma | Deb: research content | |
| KW-21 | Meet | Who the person was, told in the third person, with an illustration. | S07 | Figma | Art: only Ruth's is done. Deb/pastor: review retellings | |
| KW-22 | Enter the Story | The situation before the words, with references. | S08 | Figma | Deb: S08 headlines for Nehemiah, David, Hagar (DRAFT) | |
| KW-23 | Scripture | Their own words, cited with reference and translation. | S09 | Figma | Deb: one translation (Ruth ESV, others NIV); confirm verses | |
| KW-24 | This doesn't fit me | Sheet before reflection: *Meet someone else* or *Choose a different feeling*. Nothing recorded. | S09x | Figma | Dorcas: voice (DRAFT) | |
| KW-25 | Recognize | She taps what resonates, or *Something else*, with an optional note that isn't saved. | S10 | Figma | Choices are in Esther's voice for three pathways, David's for one | |
| KW-26 | Connection question | After a choice, "Does this connect with your moment?" with a tailored line, four answers (*Yes · A little · I'm not sure · Not really*) and a response. *Not really* offers *Meet someone else*. Not stored. | S10 | Figma | Dorcas: voice (DRAFT). Deb: "Yes" lines | |

## E. Respond

| ID | Feature | What it does | Screens | Source | Open items | MoSCoW |
|---|---|---|---|---|---|---|
| KW-27 | Respond menu | Four choices, each saying what it opens. No "Done for now"; to stop she taps the X. | S11 | Figma | Dorcas: SAT doc still lists Done for now | |
| KW-28 | Pray about it | A direction for prayer, per pathway. | S12 | Figma | Deb: Nehemiah, David, Hagar prayers (DRAFT) | |
| KW-29 | Save this prayer | Hands the prayer guide and passage reference to her phone's share sheet. KNOWN keeps no copy. | S12 → OUT-7 | Figma | — | |
| KW-30 | Sit with it | A quiet screen with nothing else to do. | S13 | Figma | — | |
| KW-31 | Reflect a little more | A small writing space (280 characters) that is never saved. | S14 | Figma | — | |
| KW-32 | Share: you're in control | Explains that she chooses who and what, and KNOWN never sends anything. | S15 | Figma | — | |
| KW-33 | Contact picker | Her phone's own contact picker, simulated. | OUT-3a | Figma | — | |
| KW-34 | Editable message | A starting message she can change or delete. | S16 | Figma | — | |
| KW-35 | Review and send | She reviews the final message in her messaging app and taps send herself. Leads to the closing screen. | OUT-3b | Figma | — | |
| KW-36 | Back to Respond | Pray, Sit, Reflect and Share each return to her own Respond screen. | S12–S16 | Figma | — | |

## F. Closing, pausing and returning

| ID | Feature | What it does | Screens | Source | Open items | MoSCoW |
|---|---|---|---|---|---|---|
| KW-37 | Closing screen | "Thank you for taking this moment." No streak, history or reminder. Reached only after a share. | S17 | Figma | Ben: confirm S17 only after a share (Pray, Sit and Reflect have no ending) | |
| KW-38 | Another story | One quiet offer, once per moment: someone else in Scripture, or another angle. | S17 → S19 | Figma | — | |
| KW-39 | Another angle | A second angle on the same story. | S19a | Figma · placeholder | Deb: research, or drop | |
| KW-40 | Close (X) on every screen | Opens "Stop for now?" from anywhere in the flow. | S18 | Figma | — | |
| KW-41 | Save this step for later | Keeps only the step and chosen person, on her phone. Reopening shows Welcome back. | S18 → OUT-5a → S04 | Figma | — | |
| KW-42 | End without saving | Closes with nothing kept. | S18 → OUT-5b | Figma | — | |
| KW-43 | Back arrow | Returns to the previous screen throughout. | All in-flow screens | Figma | — | |

## G. Companion card (Hannah's phone)

| ID | Feature | What it does | Screens | Source | Open items | MoSCoW |
|---|---|---|---|---|---|---|
| KW-44 | Ten-step companion card | One step per stage of Esther's moment. Each has a line Hannah can say and one line of guidance. Hannah taps Next by hand; the card never receives anything from Esther's phone. | C01–C10 | Figma | Dorcas: voice (DRAFT). Kezia: review every line | |
| KW-45 | Psalm-path guidance | Step 2 now says that after a psalm she may go on to a response (Step 9). | C02 | New in v2 | Dorcas: voice (DRAFT) | |
| KW-46 | She wants to stop | Tells Hannah that Esther can save or end on her own phone, and gives a line to say. | C12 | Figma | — | |
| KW-47 | If you're worried about her | Safety guidance for Hannah. | C13 | Figma · placeholder | Kezia: write it | |
| KW-48 | Card closed | Thanks Hannah and confirms nothing was seen or saved. | C11 | Figma | — | |
| KW-49 | See what Hannah receives | Prototype-only link on the invite message that jumps to the companion card. | OUT-6b → C01 | Figma | Prototype only | |

## H. Look and feel

| ID | Feature | What it does | Screens | Source | Open items | MoSCoW |
|---|---|---|---|---|---|---|
| KW-50 | Progress bar | Thin bar under the wordmark that fills from the first image screen to the closing screen. Hannah's card has the same bar, by step. Hidden on entry screens and her phone's own screens. | S05a–S19a, C01–C13 | New in v2 | DESIGN.md bans progress across sessions, not within a moment | |
| KW-51 | Dark mode | KNOWN's brown, cream and muted-blue system in dark, for every screen, including the simulated phone screens. | All | New in v2 | DESIGN.md defines light values only | |
| KW-52 | Illustrations | Finished art on S01, S05a, Ruth's S07–S08 and S17. | S01, S05a, S07–S08, S17 | Figma | Art: S06 cards, and Nehemiah, David, Hagar on S07–S08 | |
| KW-53 | Simulated phone screens | Her phone's own share sheet, contacts, messages and home screen, marked "SIMULATED: this is her phone, not KNOWN". | OUT-3a/3b, OUT-5a/5b, OUT-6a/6b, OUT-7 | Figma | — | |
| KW-54 | Soft motion | Screens fade in, sheets slide up, the progress bar grows. Turned off under reduced-motion settings. | All | Artifact only | — | |
| KW-55 | Selection states | Checkmarks for the one-or-two image choice, radio buttons for the single description, a highlighted row for Recognize. | S05a, S05b, S10 | Artifact only | Figma's S10 card doesn't show as selected | |

## I. Built-in guarantees

These are product rules from `PRD.md` §7 and `RULES.md`. Every screen above depends on them.

| ID | Feature | What it does | Screens | Source | Open items | MoSCoW |
|---|---|---|---|---|---|---|
| KW-56 | No account | Nothing asks for a name, email or identity, for Esther or for Hannah. | All | Figma | — | |
| KW-57 | Only the step is kept | The only stored state is the unfinished step and chosen person, on her phone, and only if she taps Save. | S18, S04 | Figma | — | |
| KW-58 | Routing by her taps only | No reading of what she writes, no inferred emotion, no automatic Scripture matching. | S05b, S06 | Figma | — | |
| KW-59 | KNOWN never sends | Sharing and saving go through her own share sheet, after she taps send. | S15–S16, OUT-7 | Figma | — | |
| KW-60 | Scripture always cited | Every passage shows its reference and translation. No paraphrase is presented as Scripture. | S09, S09w | Figma | — | |

## J. Walkthrough tooling (not product features)

| ID | Feature | What it does | Source | MoSCoW |
|---|---|---|---|---|
| KW-61 | Clickable Esther phone | The full flow with every branch, rebuilt from the Figma screens and copy. | Artifact only | |
| KW-62 | Hannah's phone alongside | The companion card on a second phone, showing the matching step. | Artifact only | |
| KW-63 | Try it as Esther or Hannah | Picks which phone leads. As Hannah, Esther's phone shows the matching screen with sample choices. | Artifact only | |
| KW-64 | Start from | Starts at the community link (S02) or the ad (S01). | Artifact only | |
| KW-65 | Start over | Resets both phones. | Artifact only | |
| KW-66 | Ten-stage track | Shows the current stage and jumps to any stage, filling in sample choices where needed. | Artifact only | |
| KW-67 | Notes beside the phones | For each screen: what's happening, what's kept on her phone, the hidden tags and scores behind it, and open items by owner. | Artifact only | |
| KW-68 | Match Esther's stage | Brings Hannah's card back in step after it has been moved by hand. | Artifact only | |
| KW-69 | Screen IDs | Each phone shows the current screen's ID (S05b, C03, and so on). | Artifact only | |
| KW-70 | Responsive layout | Three columns on wide screens, two phones with notes below on tablets, stacked on phones. The phones scale to fit. | Artifact only | |
