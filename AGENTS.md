# AGENTS — who does what

## Roles

| Role | Who | Does | Never does |
|---|---|---|---|
| Product foundation | Dorcas | Persona, empathy map, product voice, content requirements; owns the SAT doc | — |
| Scripture content | Deb | Researches and writes the two Scripture pathways | — |
| Structure | Ben | Sitemap, user flows, clickable user journey in Figma | — |
| Safeguarding | Kezia | Emotional-safety and safeguarding review; approves any safety or crisis copy | — |
| AI agent (Claude or other) | — | Drafts structure, docs and Figma layouts from the SAT doc; checks work against `PRD.md` and `RULES.md` | Writes or chooses Scripture, invents persona facts, adds safety/crisis copy, widens scope, commits without being asked |

## Brief format for an implementer

Every brief is self-contained and includes: the plan file path, the reading order, the rules block from `RULES.md`, the exact findings to address, the files and functions expected to change, what must not change, the check command, and the required final report (per-finding changes, skipped items with reasons, verbatim check output).

A brief that assumes the implementer shares this conversation's context is the usual failure: the implementer starts cold every time.

## Phase gating

1. **Content:** the SAT doc and `PRD.md` agree. Deb's pathways are in.
2. **Structure:** the sitemap and flows in Figma cover every PRD screen and state.
3. **Mockup:** screens carry SAT-doc copy. Kezia reviews them before external testing.
4. **Test:** the Friday prototype goes in front of real users. Findings go into `PRD.md` §9 as keep / change / remove.
5. **Build:** only after the stack is chosen and recorded in `ARCHITECTURE.md` and `RULES.md`.

An agent does not move work to the next phase on its own; the owner above confirms.

## Handover

End every session by updating `CLAUDE.md` §3 with anything that actually cost time, and by listing open `TODO(owner)` items from the eight documents, grouped by owner.

<!-- bmad:context -->
<!-- bmad-project-context manages this block. Run it once the repo has real code to scan;
     it path-checks every claim it writes, so running it against an empty repo produces
     guesses or nothing. Everything above these markers is preserved across its runs. -->
<!-- /bmad:context -->
