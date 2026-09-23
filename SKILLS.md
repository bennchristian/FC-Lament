# Skills and agents for KNOWN

One winner per job. When several installed skills could plausibly handle a task, this table decides, and it names the ones not to pick, since those are what get chosen by mistake.

**This project has no BMAD-backed planning path.** BMAD is not installed, so the planning docs were authored directly from the SAT doc, and the code-phase winners are the built-ins.

## Routing

| Job | Winner | Not these |
|---|---|---|
| Scaffold or gap-fill the eight docs | `scaffold-project` | `init`, `document-generate` |
| Write anything into the Figma Design file | `figma:figma-use` (load before every `use_figma`) | `generate_diagram` (FigJam only) |
| Build or update screens in Figma | `figma:figma-generate-design` + `figma:figma-use` | `design-html`, `design-shotgun`, `canva` |
| Diagram in a separate FigJam board | `figma:figma-generate-diagram` | `diagram` (Excalidraw) |
| Figma design → code (once a stack exists) | `figma:figma-design-to-code` | `design-html` |
| Simplify existing code | `/simplify` | `health`, `review` |
| Review a diff or PR (only when asked) | `/code-review` | `review`, `plan-eng-review`, `plan-design-review`, `plan-ceo-review` |
| Debug a failure | `investigate` | `qa` |

## Delegating to a subagent

Suggest a subagent; do not auto-delegate. It earns its cost when the work is broad fan-out search across many files, or independent tasks that can genuinely run in parallel. For a single known file or symbol, searching directly is faster than briefing an agent.

## Not in scope here

Installed globally but not competing for any job in this project:
- the social-media and content suite (caption, carousel, reels, LinkedIn, Instagram, etc.)
- the iOS suite (`ios-*`)
- `gstack` deploy/ops skills (`ship`, `canary`, `land-and-deploy`, `benchmark`)
- `anthropic-skills:ifi-brand`

## Maintaining this file

Re-check it when the installed skill set changes. A row naming a skill that is no longer installed sends the agent after something that is not there, which is worse than having no table. If a winner loses in practice, change the row rather than routing around it.
