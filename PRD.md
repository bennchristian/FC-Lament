# PRD — KNOWN

> Scope contract. Work outside this document stops and asks before widening.
> Source of truth: the team's SAT plan (`Trauma (SAT).md`, Sept 23). Where this file and
> that doc disagree, the SAT doc wins until this file is updated.
> BMAD is not installed in this repo; this PRD was written directly from the SAT doc.

## 1. Context

- **Event:** 2026 Gloo AI Hackathon, entered by a Frontier Commons (FC) fellows team.
- **Track:** Track 2 · Scripture Beyond the App · **Activation lane** (track lead: YouVersion + Biblica).
- **FC challenge space:** Trauma and Lament, framed by Aaron Mok (FC PM) around the Esther storyboard.
- **Track 2 platform expectation:** YouVersion Platform is the core Scripture layer; Gloo Studio only where it meaningfully strengthens the solution.

## 2. Product definition

**KNOWN** is a Scripture Activation tool that helps someone privately reflect on a difficult or emotionally complex moment, name what they are experiencing, encounter a relevant biblical experience, and respond honestly to God.

- **Guiding principle:** empathy first, then prayer.
- **One sentence:** an in-the-moment Scripture experience that helps a person encounter someone in Scripture, recognize what resonates, and choose a gentle next response.
- **Core promise:** before Esther is asked to pray, fix the moment or explain herself, she encounters a biblical person whose honest experience helps her feel less alone.

## 3. Users

| Persona | Priority | Summary |
|---|---|---|
| **Esther** | Primary | International Christian student living away from familiar support. Deliberately has no assigned age, nationality, denomination or diagnosis. |
| Naomi | Adjacent | Recent Christian newcomer. Checks that the experience does not depend on campus life. |
| Ruth | Adjacent | Forcibly displaced Christian. KNOWN must not treat trauma or crisis as ordinary loneliness; needs stronger safety review. |

The adjacent personas guide later research and safety checks. They do not expand the first prototype. The full persona evidence (R / I / H labels, sources) lives in the SAT doc.

## 4. Experience principles

1. **Empathy before response.** Esther meets and understands the biblical person before she is asked what to do next.
2. **At the moment, not every day.** Not a daily journal, streak product or habit tracker.
3. **The user names what resonates.** No analysis of written text, no inferred emotions.
4. **Scripture remains central.** Context → the person's words → Esther's recognition → response.
5. **No forced disclosure.** Esther controls what she selects, writes and shares.
6. **Community can introduce the rhythm.** A trusted person may sit with her; guidance happens outside the app.
7. **The current mockup is the agreed flow** until testing feedback is reviewed.

## 5. MVP scope (first prototype)

**Entry paths**
- **Ad or shared promotion:** independent entry landing that explains KNOWN and lets her begin alone.
- **Community introduction:** a QR code or link opens "How are you using KNOWN right now?" with two answers, *With someone I trust* / *On my own*. Choosing the first shows one guided-use orientation screen.
- **Companion card (C01–C13, added Sept 25):** with someone, Esther can tap *Invite someone to accompany you* on S03 and send her trusted person a companion link through the OS share sheet (OUT-6a contacts, OUT-6b editable message, both simulated). After sending she returns to S03. It opens a static, ten-step card on that person's phone, one step per stage of her journey. Each step has one line they can say and one line of guidance. The companion taps Next themselves: the card receives nothing from Esther's phone and never shows what she selects or writes, so every line works whatever she chooses. Footer links: *She wants to stop* (C12) and *If you're worried about her* (C13, placeholder for Kezia).
  - TODO(Dorcas): add the companion card to the SAT doc, which wins over this file.
  - TODO(Dorcas): voice review of the companion copy (DRAFT in Figma), including the footer rewrite.
  - TODO(Kezia): C13 copy, and a safety review of every companion line before testing.
  - TODO(Dorcas): the invite message on OUT-6b is a Claude DRAFT ("Would you sit with me while I try KNOWN?…").
  - TODO(team): the invite and card show names ("Invite Hannah", "Esther invited you"). A build needs a generic link without names (§7); the prototype keeps the persona names.

**Core experience**
- **Emotional processing: two taps on Ekman's Atlas of Emotions (decided Sept 23).** She picks both steps; KNOWN never reads her writing or infers emotion.

| Step | What she sees | Her choice |
|---|---|---|
| S05a | Four images, one per emotion (no Disgust). The team's illustrator is making the art. | Fear, Anger, Sadness or Enjoyment |
| S05b | Six feelings for that emotion, each with a short definition. They come from the Atlas of Emotions states, plus Overwhelmed and Uncertain (Fear), Lonely, Disconnected and Homesick (Sadness), and Bittersweet (Enjoyment). | One of 24 feelings |

  - **S05n, "Name it another way":** a sheet for when none of the words fit. What she types is never read or used to route.
  - **Where she lands:** feelings go to Scripture through the feelings map in `SCHEMA.md`. Feelings with no passage yet go to **S05p, "Pathway coming"**.
  - **Retired:**
    - the earlier emotions wheel's five cores, including Disgust
    - the third ring (S05c, retired because it added too many taps)
    - the six-word S05
    - the earlier mockup's five-screen See → Encounter flow
- **Choose who to meet (S06):** Esther picks the biblical person herself, from the people matched to her feeling, or from all four after S05n or S05p. KNOWN never picks for her.
- **First-person voice (decided Sept 23):** on S06–S09, each biblical person speaks for themselves ("I stepped into a new life…"), for relatability. Quoted Scripture stays word for word, in quotation marks, with references.
- **Scripture pathway, five screens:** 1 Meet · 2 Enter the Story · 3 Scripture · 4 Recognize · 5 Respond. There are four pathways, two per cluster (Deb):

| Cluster | Pathway | Passage |
|---|---|---|
| Transition | Ruth leaving Moab | Ruth 1:6–22 |
| Transition | Nehemiah, safe somewhere else and distressed about home | Nehemiah 1:1–11 |
| Isolation | David in the cave | Psalm 142 |
| Isolation | Hagar | Genesis 16:1–14 |

- **"This doesn't fit me" (S09x, added Sept 25):** S09 has a quiet link under *I'm ready →*. It opens a sheet before S10 asks her to reflect: *Meet someone else* (S06 · All four) · *Choose a different feeling* (S05a) · *Stop for now* (S18). Nothing is recorded about which story she left. The companion card's C07 guidance tells the companion to go back to Step 4 if this happens.
  - TODO(Dorcas): add S09x to the SAT doc, and review the voice of the S09x copy and the C07 line (both DRAFT in Figma).
- **Connection to her moment (S10, added Sept 25):** when she taps what stood out, "Does this connect with your moment?" appears on the same screen, with a line tailored to her choice. She answers with a tap (*Yes · A little · I'm not sure · Not really*), and a short response appears for each answer. *Not really* also offers *Meet someone else* (S09x). Her answer isn't stored or used to route. The prompts and responses are on the "Connection copy (DRAFT)" cards in Figma, next to each pathway's Research card. C08 on the companion card now mentions the question.
  - TODO(Dorcas): voice review of the connection copy (DRAFT).
  - TODO(Deb): check that each "Yes" response ("[Person] carried something like this too") is fair to the passage.

- **Respond options:** Pray about it · Sit with it · Reflect a little more (limited-character field, not saved) · Share with someone · Done for now. Each option's subline says what it opens (DRAFT, Sept 25).
  - Pray, Sit and Reflect each offer **Back to Respond** or **Done for now**.
  - **Save this prayer (S12, added Sept 25):** a quiet link inside the prayer screen hands the prayer guide and passage reference to her phone's share sheet (OUT-7), so she saves it herself. It includes nothing she selected or wrote, and KNOWN keeps no copy.
- **Leaving:** a ✕ close control on every in-flow screen opens the Unfinished moment sheet. It is an in-app sheet, not a notification.
- **Share with someone:** an editable message sent through the device share sheet. Nothing is ever sent automatically.

**States**
- **Unfinished moment:** *Save this step for later* or *End without saving*.
- **Welcome back:** *Continue where I left off* or *Start a new moment*.
- **Closing state:** no streak, pressure, scheduling or history.
- **Another story (S19/S19a, added Sept 25):** S17 has one quiet link, *If you'd like, there's another story*. It shows once per moment, only after she has finished responding, so it never interrupts the first encounter. S19 offers *Someone else in Scripture* (S06 · All four) or *Another angle on the story you read* (S19a). C10 on the companion card mentions it.
  - TODO(Deb): S19a is a placeholder. Research a second angle for each pathway's story, if one fits, or drop the option.
  - TODO(Dorcas): add S19, S12's save link and the S11 previews to the SAT doc, and review their voice.

**Content**
- Four researched Scripture pathways, two per cluster (owner: Deb; research delivered Sept 23).
- For each pathway, the research names which cluster words the passage genuinely supports, explains the biblical context, and flags words that should not be connected to that passage.
- Scripture text is only what Deb chose. No one else adds or paraphrases passages.

**Research flags to resolve (Sept 23)**
- TODO(Deb): *Homesick* now routes to Ruth, but Deb rates it only an **indirect** fit. Keep it, reword it, or find a stronger passage.
- TODO(Deb): confirm the **suggested** mapping Grief → Nehemiah.
- TODO(Deb): research passages for the 16 placeholder feelings, including all of Anger and Enjoyment, or decide which stay out of scope.
- TODO(Deb/pastor): review the first-person retellings on S06–S09. They put words in each person's mouth, so they must stay clearly distinct from quoted Scripture.
- TODO(Dorcas): review the 24 definitions on S05b, which are drafts written by Claude. *Lonely* is kept although it isn't an Atlas state.
- TODO(illustrator): four S05a images (Fear, Anger, Sadness, Enjoyment) in the house style.
- TODO(Kezia): review before testing: Panicked, Dread, Helpless, Vengeful, Overwhelmed.
- TODO(Deb): pick one translation. Ruth uses ESV; the other three quotes match the NIV. The final build pulls text from YouVersion Platform.
- TODO(Deb): the Hagar research cites Genesis 16:7 for the address that appears in 16:8. The text's speaker there is "the angel of the LORD"; get a pastor's check on the wording "God addresses her".
- TODO(Deb): review the drafted wording, marked DRAFT in Figma: the S08 headlines and S12 prayer directions for Nehemiah, David and Hagar.

## 6. Out of scope — what KNOWN is not

- A daily journaling app, mood tracker or streak-based devotional.
- A therapy platform, diagnostic tool or replacement for professional mental health care.
- A crisis response or emergency communication service.
- A social network, community monitoring tool or guide dashboard. The companion card (§5) is not a dashboard: it is static and receives no data from Esther.
- A system that automatically reads, analyzes or shares private reflections.
- A scheduling tool for Esther and the person who introduced KNOWN.
- **From the earlier v2 pitch deck and not in this MVP** (decision Sept 23): emotions wheel, fellowship/IFI connector.
- **Translation.** The prototype shows a **placeholder** language picker (S00L, opened from a pill on S01/S02) to signal that other languages are planned. Choosing a language changes nothing yet. TODO(team): translation scope, and YouVersion translations per language.
- **"Scripture Find" free-text search** (earlier mockup, slide 06): matching Scripture to what she types conflicts with §7.
- **Push notifications** of any kind.

## 7. Technical requirements

- **No account** required, for Esther or for the trusted person.
- **Companion card:** static content only. No backend, no link between the two phones, no account or identity for the companion.
- **Device-local temporary state only:** the unfinished step, plus the pathway id needed to continue. See `SCHEMA.md`.
- **No retention** of personally written text in the prototype.
- **No text analysis**, emotion inference, or automatic Scripture matching from private writing.
- **Scripture** is sourced from YouVersion Platform with translation and reference cited. TODO(team): confirm licensing and translation.
- **Sharing** goes through the OS share sheet or contacts; KNOWN never sends.
- **Saving a prayer** goes through the OS share sheet too. KNOWN keeps no copy and has no saved-prayers list.
- **Safety copy:** any safety or crisis language is reviewed by Kezia before it enters the mockup.

## 8. Success metrics

**Prototype success criteria**
- A tester understands what KNOWN is and when she might open it.
- The move from emotional processing into story, Scripture and recognition feels natural and compassionate.
- The community-guided option is understandable without a guide account.
- The user knows her reflections stay private unless she deliberately shares them.
- The Respond screen offers clear choices without feeling like therapy or a daily journal.
- Testing identifies what to keep, change or remove before the next iteration.

**Track 2 judging** — a judge must be able to answer:
- **Need:** who, what barrier, why it matters.
- **Encounter:** does it pass the removal test (remove Scripture and the experience no longer works)?
- **Response:** what she can do next.
- **Continuation:** what happens after.
- **Validation:** who we learned from, what proved wrong, what changed.

## 9. Validation TODOs (evidence gaps)

- TODO(team): does empathy before prayer or advice feel supportive to intended users?
- TODO(team): will users recognize when to open KNOWN in the moment?
- TODO(team): does a trusted community introduction improve understanding and later recall?
- TODO(team): does Share with someone feel safe, optional and clear?
- TODO(team): does the companion card help the trusted person accompany Esther without steering her answers?
- TODO(team): does "This doesn't fit me" feel like permission rather than failure, and do testers find it on S09?
- TODO(team): does "Does this connect with your moment?" feel like an invitation rather than a quiz?
- TODO(team): does anyone use Another story, and does it feel like an offer rather than a feed?
- TODO(team): do the faith-related hypotheses in Esther's empathy map reflect real users? Aaron's brief requires testing with real international students from Myanmar.

## 10. Deliverables and owners

| Person | Responsibility | Due |
|---|---|---|
| Dorcas | Product foundation, persona, empathy map, voice and content requirements | Sept 23 |
| Deb | Two researched Scripture pathways | Sept 23 |
| Ben | Sitemap, user journey, user flows | Sept 23 |
| Kezia | Emotional-safety and safeguarding review of the mockup | TODO(Kezia): confirm date |

**Milestones**
- Wed 2:00 p.m. EDT: mock-up of one complete cycle.
- Friday: prototype ready to put in front of someone.

## 11. Working links

- Figma: https://www.figma.com/design/aW0qb7r1f1bbORiKmXF6qI/Trauma-Group
  - Sitemap: `node-id=29-2`
  - User flow: `node-id=31-2`
  - User journey (clickable prototype): page `25:3`, flows "Esther — community-guided journey", "On my own" and "Hannah — companion card" (C01–C13, the row at x=7000)
- GitHub: TODO(Ben): add remote URL
