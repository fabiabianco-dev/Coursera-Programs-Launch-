# Audience Routing Model — FY27 Q3 Coursera Programs

**Rebuilt:** Jul 29, 2026 against real data. Supersedes the Jul 29 draft that assumed 250
seats and a ~200-person "movable middle" — both wrong.
**Resolves:** `PROGRAMS_1.md` Open Question #3.

---

## The three-source model

| Source | Role | Authority |
|---|---|---|
| **Workday Current Worker Detail** (eff. 2026-07-27) | **The universe.** Who exists. Guarantees nobody is forgotten. Answers manager, department, tenure, level. | Employment facts |
| **Claude Enterprise Analytics** (Jun 21 – Jul 20) | **The decision engine.** Defines who goes to which program. | Routing |
| **Manager Validation Tracker** | **The commitments.** Who is already in AFS Next or a Claude Foundations lab. | Prevents double-tapping |

**Inclusion rule:** `Active Status = Yes` AND `Worker Type = Employee`. Contingent and
inactive workers are excluded everywhere. This removes **150 active contingent workers**.

---

## What the data actually says

**Adoption is not the problem.** 443 of 468 measured employees used Claude in the trailing
30 days — **94.7%**. Only 24 have zero usage. The "get people using AI" framing is solved.

**Construction is the problem.** Only **160 people have ever created a Project.** 308 have
not. That is the Autonomy gap, and it matches `project.md`'s Tier 2 → Tier 3 plateau:
people converse with AI but have not crossed to building.

| Segment | Definition | All 468 | Available pool |
|---|---|---|---|
| Constructing | ≥2 Projects created, or ≥50 Code sessions | 170 | 107 |
| Early construction | Any Project / Skill / Code signal | 244 | 117 |
| Conversation only | Messages, no construction signal | 30 | 22 |
| No usage | Zero | 24 | 19 |
| New — no usage data | Hired after the measurement window | 3 | 3 |

---

## Population reconciliation

```
  471  active non-contingent employees (Workday, unique work emails)
  468  matched to the Claude usage roster
    3  in Workday with NO usage row — all hired 2026-07-27, two are VPs
    0  usage rows that are not active employees  ✓ clean
─────
  203  already committed to a live program  → held separately
  268  available to route to Coursera
```

The 3 unmatched people are the concrete "forgetting" risk: a purely usage-driven model
skips them silently because they postdate the measurement window. They route on tenure.

---

## Routing rules

| Program | Rule | Count |
|---|---|---|
| **1 · Expand Your RANGE** | New hire ≤90 days, no usage, or conversation-only | **72** |
| **2 · Running with Claude** | Early construction, or constructing below P6 | **172** |
| **3 · Augment & Automate** | Constructing **and** P6+/leader — owns a real process | **24** |

Program 3 lands at 24 rather than `project.md`'s "~50" because the ~50 P6 population is
heavily represented in the 203 already committed to AFS Next. The advanced builders are
mostly already in a program — which is the pilot working as designed.

### Held separately: the 203

Not excluded — **held**. They are mid-flight in AFS Next or a Claude Foundations lab.
Re-routing them now is the double-tap Fabia flagged. Revisit after their current program
ends, then route on the same rules.

---

## ⚠ The completion data does not exist

Fabia asked who completed Claude Skills Foundations and Claude Cowork. **The honest answer
is that no one can be evidenced as complete.**

| Program family | Assigned | Zoom-verified attendance |
|---|---|---|
| AFS Next (C1–C4) | 111 | 24 |
| Claude Skills & Projects (G1–G2) | 59 | 2 |
| Claude Cowork (G1–G2) | 47 | 4 |

The `Zoom Attendance` sheet contains **only AFS Next Cohorts 3 and 4** — 49 rows, 33 unique
people, none with all four sessions. `Cohort Health` marks **all four Foundations groups as
"⚠ event not found."** The ✓ Attended marks on the C1/C2 tabs come from a source not present
in the workbook.

Consequences:
1. **Cowork's prerequisite cannot be enforced or evidenced.** 106 people are assigned to
   Foundations labs with no attendance record.
2. **AFS Next C1/C2 "completions" rest on unverifiable marks.** C3 finishes Aug 18; C4
   started today and finishes Sep 9 — so *no* AFS Next cohort has actually completed.
3. Any comms claiming "you have completed X, so now do Y" is unsupported today.

---

## Inherited tension in Lee's original model

Lee's Apr 14 phased plan (207 TPS roster members × Claude Analytics Jan 1 – Apr 4) routed:

| Phase | Track | N | Avg msgs | Rule |
|---|---|---|---|---|
| 1 | AFS Next | 100 | 818 | Top 100 by composite, 200-message floor |
| 2 | Senior Leader Intervention | 10 | 90 | Critical Role holders below the floor |
| 3 | Claude Cowork | 46 | 274 | Upper half of remaining by messages |
| 4 | Claude Skills & Projects | 51 | 72 | Lower half of remaining + unmatched |

Composite = messages + Critical Role +500 + Team Priority (High +200 / Med +100) +
multi-tree +150 + recency +100.

**The tension:** Cowork was given to *higher*-usage people than Skills & Projects, yet
Cowork lists Skills & Projects as its prerequisite. The `H1 Program Schedule` sheet resolves
part of this — Skills & Projects Group 1 is labelled *"TPS Path B for AFS Next … needs to
complete Claude foundational sessions before enrolling on AFS Next"*, i.e. a **ramp into**
AFS Next, not a step toward Cowork. Worth making explicit before invitations reference a
sequence.

---

## What we are deliberately not doing

- **Not routing by job family.** Banned as a fluency proxy.
- **Not enforcing prerequisites.** No verified completion data exists to enforce against.
- **Not assigning all three programs at once.** One primary each.
- **Not re-routing the 203 committed.** Held, not excluded.
- **Not gating on the AI Fluency Assessment.** Preferred signal, but its link is still TBD
  and cannot be the critical path.

---

## Dependencies before Aug 7 invitations

| # | Dependency | Owner | Needed by |
|---|---|---|---|
| 1 | Confirm licence count — 350 or 250 | Deepika / Angelo | Aug 3 |
| 2 | Confirm completion window — 6–8 or 12 weeks | Fabia | Aug 3 |
| 3 | Decide whether unverified Foundations attendance counts as complete | Fabia | Aug 3 |
| 4 | Resolve the Expand Your RANGE course list | Fabia + Nana | Aug 5 |
| 5 | Reconcile the 82 unmatched Claude accounts | Lee / Angelo | Aug 5 |
| 6 | Clean the 9 orphan roster emails ADA keeps failing on | Deepika | Aug 5 |
| 7 | Load seat holders in Coursera admin | Deepika | Aug 6 |
