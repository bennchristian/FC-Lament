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

**Core experience**
- **Emotional processing (one screen, S05; decided Sept 23):** Esther deliberately *selects* the words that feel close. Her selection routes her to one of two Scripture pathways:
  - **Transition** cluster: bittersweet, homesick, uncertain.
  - **Isolation** cluster: lonely, disconnected, unseen.
  - Plus "Something else".
  - The earlier mockup's five-screen version (See → Recognize → Name → Understand → Encounter) is retired.
- **Scripture pathway, five screens:** 1 Meet · 2 Enter the Story · 3 Scripture · 4 Recognize · 5 Respond. One pathway per cluster (Deb).
- **Respond options:** Pray about it · Sit with it · Reflect a little more (limited-character field, not saved) · Share with someone · Done for now.
  - Pray, Sit and Reflect each offer **Back to Respond** or **Done for now**.
- **Leaving:** a ✕ close control on every in-flow screen opens the Unfinished moment sheet. It is an in-app sheet, not a notification.
- **Share with someone:** an editable message sent through the device share sheet. Nothing is ever sent automatically.

**States**
- **Unfinished moment:** *Save this step for later* or *End without saving*.
- **Welcome back:** *Continue where I left off* or *Start a new moment*.
- **Closing state:** no streak, pressure, scheduling or history.

**Content**
- Two researched Scripture pathways (owner: Deb), one per cluster above.
- For each pathway, the research names which cluster words the passage genuinely supports, explains the biblical context, and flags words that should not be connected to that passage.
- Until they land, the prototype shows bracketed placeholders; no Scripture is filled in by anyone else.

## 6. Out of scope — what KNOWN is not

- A daily journaling app, mood tracker or streak-based devotional.
- A therapy platform, diagnostic tool or replacement for professional mental health care.
- A crisis response or emergency communication service.
- A social network, community monitoring tool or guide dashboard.
- A system that automatically reads, analyzes or shares private reflections.
- A scheduling tool for Esther and the person who introduced KNOWN.
- **From the earlier v2 pitch deck and not in this MVP** (decision Sept 23): emotions wheel, Burmese-language picker, fellowship/IFI connector.
- **"Scripture Find" free-text search** (earlier mockup, slide 06): matching Scripture to what she types conflicts with §7.
- **Push notifications** of any kind.

## 7. Technical requirements

- **No account** required, for Esther or for the trusted person.
- **Device-local temporary state only:** the unfinished step, plus the pathway id needed to continue. See `SCHEMA.md`.
- **No retention** of personally written text in the prototype.
- **No text analysis**, emotion inference, or automatic Scripture matching from private writing.
- **Scripture** is sourced from YouVersion Platform with translation and reference cited. TODO(team): confirm licensing and translation.
- **Sharing** goes through the OS share sheet or contacts; KNOWN never sends.
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
  - User journey (clickable prototype): page `25:3`, flows "Esther — community-guided journey" and "On my own"
- GitHub: TODO(Ben): add remote URL
