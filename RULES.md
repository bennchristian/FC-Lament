# RULES — coding and implementation

## Principles

1. **SOLID.** One responsibility per file and per function. Depend on small named helpers, not on incidental structure that can shift underneath you.
2. **DRY at 4.** Extract a shared helper only when the same logic appears 4 or more times. Below that, repetition is acceptable and clearer: the wrong abstraction couples callers that had no reason to be coupled, and costs more to unwind than the duplication cost to tolerate.
3. **KISS.** A new function does one thing in the simplest way that passes the check. No options objects, no abstractions "for later", no configuration that nothing reads.

## Stack rules

TODO(team): no stack chosen yet (`ARCHITECTURE.md` §1). Add rules here once one is picked.

## KNOWN product rules (hard — these come from the Track 2 guardrails and the SAT doc)

1. **No inference.** Never analyze free text, infer emotion, or route by anything except the user's explicit selection.
2. **No auto-send.** Share hands an editable message to the OS; KNOWN never sends, schedules or notifies anyone.
3. **Scripture is cited and never fabricated.** Every passage shows its reference and translation. Interpretation is never presented as Scripture, and no model paraphrases or chooses passages.
4. **No retention metrics.** No streaks, counters, history, push re-engagement or analytics that optimize for return visits.
5. **Safety copy is gated.** Any safety, crisis or care language goes through Kezia's review before it enters a mockup or a build.
6. **No account, no personal info.** Nothing requires a name, email, phone or identity, for Esther or for the guide.

## Security rules

- Never log or transmit free-text fields.
- API keys (e.g. YouVersion) never ship in client bundles or commits. TODO: secret handling once a build exists.

## Data rules

- The only persisted state is `UnfinishedMoment` in `SCHEMA.md`, stored on the device.
- Adding any stored field is a scope change: update `PRD.md` §7 and `SCHEMA.md` first.

## Process rules

- Before any implementation, the eight context files exist and are current: CLAUDE, AGENTS, ARCHITECTURE, DESIGN, PRD, RULES, SCHEMA, SKILLS.
- `PRD.md` is the scope contract. Work outside it stops and asks rather than widening.
- TODO(team): check command once a build exists. Until then, a design handover requires every sitemap screen to be present in the prototype with no dead-end buttons.
- Keep an explicit resolved/unresolved list when auditing; never imply a pass fixed more than it did.
- Figma is the source of truth for screens and copy during the design phase. Copy changes land in Figma and the SAT doc, not only in one of them.

## Prefer enforcement over prose

A rule a linter, formatter, type checker or CI check can enforce belongs there instead of here. Rules in this file are followed by hand every time; a check fails the build once and is never forgotten. When a rule above becomes mechanically enforced, delete it from this file.
