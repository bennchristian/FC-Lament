# SCHEMA — KNOWN

**No database.** The prototype has no server, no accounts and no stored history (`PRD.md` §7). This file therefore documents the one piece of device-local state and the fixed content KNOWN reads, so nobody adds storage by accident.

## Entity overview

```
PathwayContent (static, bundled)  ←─ pathwayId ─  UnfinishedMoment (device-local, 0 or 1)
```

## Device-local state

### `UnfinishedMoment` (at most one per device)

| Field | Type | Notes |
|---|---|---|
| `currentStep` | enum: `emotional-processing` · `meet` · `story` · `scripture` · `recognize` · `respond` | The next unfinished step |
| `pathwayId` | string, nullable | Null if she stopped before selecting a feeling |
| `entryMode` | enum: `guided` · `independent` | TODO(team): confirm this is needed to skip or show orientation on continue. Remove it if not |

**Lifecycle**
- Written only when Esther chooses *Save this step for later*.
- Deleted when she chooses *End without saving* or *Start a new moment*, or finishes the pathway.

**Never stored:** selections' free text, Recognize "Something else" text, Reflect text, the share message, recipient, guide identity, timestamps of past moments, completion counts.

## Static content

### `PathwayContent` (authored by Deb, read-only)

| Field | Notes |
|---|---|
| `pathwayId` | Stable id |
| `person` | Biblical person's name, plus the visual for Meet |
| `storyContext` | Enter the Story copy |
| `passage` | Reference + translation. Text comes from YouVersion Platform, not copied into the bundle unless licensing allows. TODO(team) |
| `recognizeChoices[]` | Nuanced options. "Something else" is always appended by the client |
| `prayerDirection` | Pray about it copy. Must not claim to know how she feels |

TODO(Deb): the two pathways' content. TODO(Dorcas/Deb): the selection → `pathwayId` mapping.

## Off-store state

- **OS share sheet:** once Esther taps send in her messaging app, the message is outside KNOWN entirely.
- **YouVersion Platform:** Scripture text is fetched from it. TODO(team): API key storage, if a coded build happens.
- **Figma file:** holds the design-phase source for screens and copy (`PRD.md` §11).

## Access control

Not applicable. There is no shared store and no user-to-user access. The rule that stands in for access policy is `RULES.md` → Data rules.

## Migrations

None. If a store is ever added, that is a scope change: stop and update `PRD.md` first.
