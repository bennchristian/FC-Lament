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

| `pathwayId` | Cluster | Passage | Deb's strongest fits | Weak fits (flagged) |
|---|---|---|---|---|
| `ruth` | Transition | Ruth 1:6–22 | uncertain (strong), bittersweet (moderate–strong) | homesick (indirect) |
| `nehemiah` | Transition | Nehemiah 1:1–11 | concern for people back home (very strong), helpless at a distance (strong) | homesick (indirect) |
| `david` | Isolation | Psalm 142 | unseen (very strong), lonely (strong) | disconnected (moderate) |
| `hagar` | Isolation | Genesis 16:1–14 | unseen (very strong), lonely (strong, with nuance) | disconnected (moderate) |

**Routing:** image (S05a) → feeling (S05b, ring 2) → the people for that feeling on S06 → Esther picks the `pathwayId`.
- If a coded build keeps the `UnfinishedMoment` record, `pathwayId` is set only once she has picked a person on S06.

### Feelings map (emotions wheel → pathway)

The four emotions come from Ekman's Atlas of Emotions, without Disgust. Only 8 of the 22 feelings have a pathway so far.

| Emotion | Feelings (S05b) |
|---|---|
| Fear | Anxious, Overwhelmed, Insecure, Weak, Rejected, Threatened |
| Anger | Distant, Critical, Frustrated, Bitter, Humiliated |
| Sadness | Hurt, Guilty, Despair, Vulnerable, Lonely, Disconnected |
| Enjoyment | Optimistic, Peaceful, Proud, Excited, Powerful |

| Emotion › feeling | S06 shows | Status | Basis in Deb's research |
|---|---|---|---|
| Sadness › Lonely | David, Hagar | mapped | lonely: strong for both |
| Sadness › Disconnected | David, Hagar | mapped | disconnected: moderate for both |
| Sadness › Despair | Nehemiah | mapped | helpless at a distance: strong |
| Fear › Anxious | Nehemiah | mapped | concern for people back home: very strong |
| Fear › Weak | David, Hagar | suggested | unseen / "no one notices" |
| Fear › Rejected | Hagar | suggested | alienated from the household |
| Sadness › Vulnerable | Hagar | suggested | mistreated, vulnerable |
| Anger › Distant | David, Hagar | suggested | close to disconnected |
| The other 14 (including Overwhelmed) | S05p "Pathway coming" → All four | placeholder | — |

**Statuses:**
- **mapped:** Deb's fit table supports it.
- **suggested:** Claude's reading of her story notes. TODO(Deb): confirm.
- **placeholder:** TODO(Deb): research a passage.

The full list, with draft definitions, is in Figma: the "Feelings map" card and the S05b screens. The retired third ring (50 feelings, with definitions) is kept in the "RETIRED" section of the journey page.

Ruth has no ring-3 feeling of her own. See PRD §5, research flags.

## Off-store state

- **OS share sheet:** once Esther taps send in her messaging app, the message is outside KNOWN entirely.
- **YouVersion Platform:** Scripture text is fetched from it. TODO(team): API key storage, if a coded build happens.
- **Figma file:** holds the design-phase source for screens and copy (`PRD.md` §11).

## Access control

Not applicable. There is no shared store and no user-to-user access. The rule that stands in for access policy is `RULES.md` → Data rules.

## Migrations

None. If a store is ever added, that is a scope change: stop and update `PRD.md` first.
