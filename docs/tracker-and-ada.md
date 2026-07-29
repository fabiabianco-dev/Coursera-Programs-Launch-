# The Tracker & ADA — the operating system of AI learning

**Adopted:** Jul 29, 2026 as the system of record this project reads from and writes back to.
**File:** `AI_Learning_Program___Manager_Validation_Tracker`
[live sheet](https://docs.google.com/spreadsheets/d/1HbEsAOrl8W34iJZ5YT77Y-0VmMm1HCw_h5mLb83ghQM/edit)

---

## Sheet map

| Sheet | Rows × Cols | What it is |
|---|---|---|
| `Zoom Events List` | 10 × 5 | Zoom event IDs + publish status, pulled by ADA |
| `C1–C4 · AFS Next` | ~28–42 × 8–9 | Per-cohort rosters with per-session attendance marks |
| `G1–G2 · Skills & Projects` | 65 / 10 × 8 | Foundations lab rosters |
| `G1–G2 · Cowork` | 62 / 5 × 8 | Foundations lab rosters |
| `Cohort Health` | 11 × 7 | Roster vs attended vs no-show vs not-registered, per cohort |
| `Decisions Ledger` | 16 × 8 | Locked decisions with rationale — the audit trail |
| `Identity & Alias Map` | 5 × 4 | Name/email aliases across systems |
| `Zoom Attendance` | 151 × 8 | Actual attendance rows (**AFS Next C3/C4 only**) |
| `Zoom Sessions` / `Zoom Data` | 22 / 225 | Session IDs, times, raw pull |
| `Request Queue` | 993 × 15 | Inbound requests and their agent disposition |
| `ADA Log` | 1000 × 5 | ADA's own audit log |
| `H1 Program Schedule` | 1001 × 11 | Master session calendar by initiative/cohort |
| `Manager Validation` | 1012 × 27 | **The core table** — 221 populated rows |

### `Manager Validation` schema (the write-back target)

`Manager Name · Employee Name · Employee Email · Business Title · Track Decision · Program ·
Cohort / Group · Registration Status · Master Tracker · Session 1–4 · Session Time ·
# Sessions · Delivery · Status · Response Date · Notes/Action`

Current state: **221 rows.** `Status` is `Pending` on **191** of them — manager validation
has been requested but largely not returned. Track Decision still carries Lee-era values
(`AFS Next`, `AFS Next - Top 30`, `Senior Leader Intervention - Low User`).

**This is where Coursera assignments get written back.** The proposed columns —
`Coursera Program`, `Assignment Rule`, `Usage Segment` — map onto `Track Decision` /
`Program` / `Notes/Action`, so the handoff workbook is paste-compatible.

---

## ADA — the registration desk agent

ADA maintains the tracker autonomously. Reconstructed from `ADA Log` and `Request Queue`:

**Loop.** Reads `cmd-*.json` command files from a Drive queue ("Jane Commands") → validates
the target email against the roster → mutates the tracker (typically `Cohort / Group`) →
drafts a Gmail notification → writes an audit row to `ADA Log`.

**Request Queue fields:** `ID · Date Logged · Person · Email · Source · Message Summary ·
Type · Cohort (Current) · Cohort (Requested) · Status · Fabia Notes · Agent Action ·
Agent Action Date · Confidence · Actioned By`

- **Sources:** Slack DM, Slack Group DM, cohort channels (`#afs-next-cohort-2`), Zoom data
- **Types:** `MOVE REQUEST` · `DATA FLAG` · `TECHNICAL ISSUE` · `QUESTION`
- **Statuses:** `AGENT DONE` · `RESOLVED`
- **Confidence:** `HIGH` / `MEDIUM` / `LOW` — move requests run HIGH; interpretive data
  flags run LOW and fall back to "handled by ADA safe-mode"
- **ADA Log types:** `test` · `setup` · `error` · `update`

**Human-in-the-loop is real.** `Fabia Notes` carries the decision ("MOVED TO COHORT 4",
"SPOKE TO HER IN PERSON DURING SESSION 1"), and the `Decisions Ledger` locks outcomes with
rationale. ADA executes and evidences; Fabia decides.

### ADA's failure modes, from its own log

1. **`Error: email not found`** — repeatedly on `jess.lieberman@betterup.co` and others.
   These are the **9 orphan roster emails** that are not active non-contingent employees.
   ADA cannot action a person who is not in the roster it validates against.
2. **`Exception: The data you entered in cell H212 / H191 …`** — sheet data-validation
   rejecting a write. Cohort-value validation is fighting the agent.
3. **Zoom events not found** for all four Foundations groups — which is why there is no
   attendance data for Skills & Projects or Cowork.

Fixing #1 and #2 is cheap and would stop most of ADA's error volume.

> **Not accessible from here:** ADA's own code/config lives on Fabia's desktop. This session
> runs in an isolated remote container with no access to local files, so the above is
> reconstructed from the tracker's log and queue only. To go deeper, ADA's source needs to be
> committed to a repo or shared through Drive.

---

## How this project should operate the tracker

1. **Read** the live sheet — never a stale download. Downloads flatten merged cells and lose
   sheet structure.
2. **Validate** every email against Workday active non-contingent before writing.
3. **Write back** into `Manager Validation` (`Track Decision` / `Program` / `Notes/Action`),
   never into the per-cohort tabs, which ADA owns.
4. **Log** every change in `Decisions Ledger` with rationale — matching ADA's convention.
5. **Respect the alias map.** Brendan Kelly registers as `bkelly@brendankelly.com`; Cate
   Stamos appears as Cate Connerty; Jess Lieberman as Jess Wiseman; Celeste Cheung as
   "Celest Chung" in Zoom.
