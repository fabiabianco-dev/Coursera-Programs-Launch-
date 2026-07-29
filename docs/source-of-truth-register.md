# Source of Truth Register & Conflict Log

**Compiled:** Jul 29, 2026 · **Trigger:** reconciling `project.md`, `PROGRAMS_1.md`, the Drive
comms doc, the Expand Your Range sheet, the Jul 2026 Claude usage roster, and
`Coursera_Launch_Project_Instructions.md`.

`project.md` is the newest artifact (compiled Jul 29) and it explicitly deprecates facts
that other files still assert. Where it does, it wins. Where the usage roster has a number,
the roster wins over every prose document.

---

## Proposed hierarchy

| Rank | Source | Authoritative for | Notes |
|---|---|---|---|
| 1 | **Fabia in-session** | Everything | Always wins. Flag which file needs updating so it doesn't drift again. |
| 2 | **Claude usage roster** (`CompanyWide_Claude_Usage…xlsx`) | All segmentation, headcount, population sizes | Workday export Jul 24 + Anthropic Enterprise Analytics, via Lee Gonzales. |
| 3 | **Live Google Sheets** (skill selection, capability map, curation scope) | Skill cut, curation status | Listed in `project.md` §8. They update; uploads don't. |
| 4 | **`project.md`** (Jul 29) | Dates, names, launch architecture, people, wave design | Newest compiled context. |
| 5 | **Coursera platform** (via Deepika) | What courses actually exist inside each program | Nothing else can settle the course-list conflict. |
| 6 | **`Coursera_Launch_Communications`** (Google Doc) | Comms copy only | Currently mid-review with three open Sarah comments. |
| 7 | **`PROGRAMS_1.md`** | Program URLs, learner-facing descriptions | Unreliable on course lists — see C8. |
| 8 | ~~`locked-facts.md`, `COURSERA_LAUNCH_MASTER_CONTEXT.docx`, `Coursera_Launch_Project_Instructions.md`~~ | **Deprecated for dates, licenses, headcount** | Still good for voice rules, DACI, glossary. |

---

## Tier 1 — numbers that change the work

### C1 · Licenses: 250 vs 350
- `Coursera_Launch_Project_Instructions.md` + `locked-facts.md`: **250**, activated Apr 22.
- `project.md` §0/§4: **350 of 500 held**, deployed Phase 1 — and states "250 is stale."
- **SOT: 350.** Confirm with Deepika or Angelo.
- **Impact:** the routing model was built on 250. 100 additional seats is a materially
  different allocation. ⚠️ `audience-routing-model.md` needs rebuilding.

### C2 · Headcount: 466 vs 468
- Prose docs: ~466. Usage roster: **468 active non-contractor**.
- **SOT: 468.** Also: **82 Claude accounts unmatched to an active Workday employee** — worth
  resolving before IT provisions seats.

### C3 · "Movable middle" size: 105 vs 200 vs the data
- `project.md` §13: ~105 sustained-but-not-yet-building.
- Expand Your Range sheet: ~200 customer-facing.
- **Roster says neither.** Actual construction behavior across 468 people:

| Band | Definition | Count |
|---|---|---|
| No usage | Zero messages, zero construction | **24** |
| Conversation only | Messages, no Projects/Skills/Code signal | **30** |
| Early construction | Some signal, shallow | **244** |
| Constructing | ≥2 Projects created, or ≥50 Code sessions | **170** |

**SOT: the roster.** The cleanest single Autonomy signal is *Projects Created* — only
**160 of 468 (34%) created any project**, so **308 people have never built one.** That is
the real Autonomy gap, and it is the number to plan against.

### C4 · Completion window: 6–8 weeks vs 12 weeks
- Everything built references 6–8 weeks from invitation; Fabia floated 12 weeks later.
- **UNRESOLVED.** Blocks the manager email and the Aug 7 invitations — both need a number.

---

## Tier 2 — the launch architecture contradiction

### C5 · Wave 2 is shipping first, as the lead message ⚠️ **biggest conflict**
`project.md` §3 defines the architecture:
- **Wave 1 (the real launch):** targeted invitation to movers. Message = **acceleration**.
  Business case = 84% of lean-forward AI users are customer-facing.
- **Wave 2 (level-set):** all-employee *"Coursera is here, and it's more than AI"* utility
  note. Ships **after** Wave 1. Recommendation: hold 2–3 weeks, low-key, **no campaign weight**.

Tomorrow's BU News email is **Wave 2 content, shipping first, with full campaign weight**:

> "Coursera isn't only for AI: sharpen customer service skills, go deeper on behavioral
> science, learn the HR industry, expand your market development strategies — the sky is
> the limit."

That is the "more than AI" utility message, sent to everyone, before any targeted invitation
exists. It also contradicts the governing frame — **"acceleration, not access"** — by
leading on access.

**This is very likely what Sarah is asking about.** Her open comment on the doc is *"is this
going to everyone?"* Answering it is an architecture decision, not a copy edit.

### C6 · Aug 7 means two different things, and the sequence inverts
| Source | Aug 7 is | Webinars |
|---|---|---|
| Comms doc timeline | **Program** invitations to selected learners | Aug 4 + Aug 6 (i.e. *before* Aug 7) |
| `project.md` §0 | **Webinar** invitations | "after Aug 7 invites — CONFIRM" |

`project.md` states a load-bearing rule: *manager comms → all-employee email → webinar
invites → webinars → program starts*. The comms doc violates it by running webinars three
days before the Aug 7 invitation.

### C7 · Manager comms: one email or three?
- Comms doc Section 3 (empty) reads as one manager announcement — what I drafted.
- `project.md` §2 describes **three program-specific manager waves**.
- Also: `project.md` §9 says **HRBPs (Ron, Diana, Lola, Jo) carry manager heads-up
  messaging** — my draft has no HRBP distribution path.

---

## Tier 3 — content that cannot be published yet

### C8 · Expand Your Range course list: three incompatible answers
| Source | Courses |
|---|---|
| `PROGRAMS_1.md` | Rethink How You Decide with AI · Systems Thinking for AI & Automation · Trustworthy Generative AI |
| Expand Your Range sheet | AI Fundamentals with Claude · Start Writing Prompts like a Pro · Claude Cowork for Automating Processes · Trustworthy Generative AI · AI Collaboration with Claude |
| `project.md` §6 | The Claude courses are **unverified candidates**, not confirmed catalog content |

### C9 · The Claude course series may not exist ⚠️
`project.md` §6: *"no verified Claude course series is confirmed in the catalog yet… All need
catalog verification before use in learner-facing assets. Until resolved, Foundation
Sessions carry the Claude-fluency story — don't promise a Coursera Claude series we can't
point to."*

Tomorrow's email promises exactly that series. `PROGRAMS_1.md` lists Running with Claude as
live with a working URL. **Either the URL resolves to real content, or the email promises
something we cannot deliver.** Deepika or Nana must confirm.

### C10 · Two Claude courses assigned to two programs at once
*AI Fundamentals with Claude* and *AI Collaboration with Claude* sit inside Expand Your
Range (sheet) **and** Running with Claude (`PROGRAMS_1.md`). Learners routed to both take
them twice; the "~7–9 hours" claim breaks.

### C11 · Program 2: name vs Coursera slug
Program is **Running with Claude**; the Coursera slug is **nail-it-with-claude**. Reconcile
before any invitation references a name.

### C12 · Program 3: five names, plus an open rename question
"Augment & Automate Your BetterUp Processes" (`project.md`, working name) ·
"Augment and Automate Your BetterUp Processes" (comms doc) ·
"…with AI" (sheet) · "Improve Your Process" (older spec) ·
"Automating our Commit to a Better Business Process" (Fabia, verbal).

Open: add **"agentic"** to the title? Can Deepika rename in Coursera **without breaking the
URL**? Separately, the Expand Your Range sheet lists a different third program entirely —
*Horizontal Leadership & AI: Strategic Awareness & Change Management*. Retired, deferred, or
a fourth?

### C13 · Program 3 audience
- `project.md` §2: initial focus **P6+, ~50 medium-high users who did AFS-Next on R&D/TPS**.
- `PROGRAMS_1.md`: "BetterUppers ready to improve a real process they own."
- **SOT: `project.md`** — it is specific and gated on AFS-Next completion.

---

## Tier 4 — facts and framing to correct

| # | Conflict | Source of truth |
|---|---|---|
| C14 | Cameran Hetrick listed as current VP AI Enablement | **Departed** (`project.md` §9). Remove from stakeholder lists. |
| C15 | Hub live Jul 29? Timeline row struck through; returns 403 to me | `project.md` §2: **hub design vision unresolved, blocking hub-live.** Assume NOT live. Tomorrow's email links to it 6+ times. |
| C16 | Curation blocker open (project instructions, escalated twice) | **Closed.** `project.md` §5: 20-skill cut done (A6/E6/N6/R2), package ready pending Fabia's send. |
| C17 | Banned words = 4 | **Longer list:** unlock, unleash, journey, velocity, **democratize**. Also retired: "movable middle" (never external), "raise the floor," maturity framing. |
| C18 | Sarah as "approver and budget sponsor" gating the launch | `project.md` §9: **Fabia is Driver and owns the launch decision — she *aligns* Sarah, she does not ask Sarah to decide.** My readiness doc over-subordinated this. Corrected framing: Fabia decides, Sarah is aligned. |
| C19 | "Expand Your Range" vs "Expand Your RANGE" | Pick one. Comms doc uses sentence case; `PROGRAMS_1.md` uses caps. |
| C20 | AFS Next prerequisite "AFS 100" | Unresolved — AI Flight School is retired. `PROGRAMS_1.md` Open Q1. |

---

## What this changes in work already delivered

| File | Status |
|---|---|
| `audience-routing-model.md` | ✅ **Rebuilt** against the roster. |
| `CLAUDE.md` | ✅ Patched: licenses, headcount, Cameran, banned words, Sarah framing. |
| `manager-launch-announcement.md` | ⚠️ Revise: one email vs three waves, no completion-window number, no HRBP path, seat count wrong. |
| `launch-readiness-jul30.md` | Mostly holds. Upgrade P0-4 (hub is likely *not* live) and add C5 as the top blocker. |
