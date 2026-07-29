# Attendance Truth — the definitive record

**Compiled:** Jul 29, 2026 from Zoom's own reports (`Top_10_events` + `Attendee_breakdown`,
362 registration rows across 9 events).
**Supersedes** every earlier claim in this repo that Foundations attendance data does not
exist. It does. The tracker simply could not see it. Specifically superseded:
`audience-routing-model.md` §"The completion data does not exist", `launch-readiness-jul30.md`
P1-6, and the third bullet under `CLAUDE.md` "Known open conflicts".

---

## Why this correction was needed

`Cohort Health` in the Manager Validation Tracker marks all four Foundations groups as
**"⚠ event not found"** and reports 0 attended, 106 not registered. That was read — by me
included — as *nobody attended*.

It actually meant *the tracker was never linked to those Zoom events.* The sessions ran,
people came, and Zoom recorded all of it. The failure was plumbing, not participation.

**Fix:** add the Cowork and Skills & Projects event IDs to `Zoom Events List` so ADA's pull
covers them. Event IDs are in the table below.

---

## Events and attendance rates

| Event | Date | Attendees | Registrants | Rate | Event ID |
|---|---|---|---|---|---|
| AFS Next Cohort 1 | Jun 10 | 40 | 43 | **93%** | `QyjDXldxR9CdGIn4wOgWLw` |
| AFS Next Cohort 2 | Jun 11 | 31 | 33 | **93%** | `Xqbb4A0vRp29ZD_nbyQeXQ` |
| Claude Cowork | Jun 23 | 29 | 59 | 49% | `SKA6_tqASBec35t6KJcxVw` |
| Claude Skills & Projects | Jun 24 | 22 | 48 | 45% | `kIQf3D6XTJOeYK-kI_p1iA` |
| AFS Next Cohort 4 | Jul 29 | 19 | 25 | 76% | `OTqqWiEbQOSGO8dvhayGMA` |
| AFS Next Cohort 3 | Jul 7 | 13 | 23 | 56% | `-kofbbO-QYCdCEGQ__hDUQ` |
| Claude Cowork | Jul 28 | 12 | 23 | 52% | `JWwLDqLcTv-_ns6a22FHOA` |
| Claude Skills & Projects | Jul 15 | 11 | 21 | 52% | `hIcwwq2EQRC2zBJtzaB04A` |
| Skills & Projects — Added Session | Jul 8 | 1 | 6 | **16%** | `sJIrn9E-TECCSS7tOqXLdA` |

Note there are **two Cowork sessions and three Skills & Projects sessions** — these are
recurring labs, not single cohorts. Any "Group 1 / Group 2" framing in the tracker
under-describes them.

## Unique people, facilitators removed

| Program | Registered | Attended live | Watched recording | Registered but never came |
|---|---|---|---|---|
| AFS Next | 109 | **73** | 0 | 36 |
| Claude Cowork | 78 | **32** | 0 | 46 |
| Claude Skills & Projects | 72 | **21** | 0 | 51 |
| **Any program (unique)** | **226** | **119** | **0** | **107** |

Facilitators excluded throughout: Alex Zesch, David Brinegar, Lee Gonzales. They appear in
attendance data as hosts, never as learners.

---

## Three findings that change decisions

### 1. Nobody watches recordings. Zero, across all nine events.
Not one person in 362 registration rows watched a recording. The launch comms treat "both
sessions recorded" as coverage for non-attendees. On this evidence, recording is not a
fallback. If the Aug 4 / Aug 6 webinars matter, live attendance is the only thing that
counts — and the copy should stop implying otherwise.

### 2. The Cowork prerequisite is fiction.
Cowork lists Claude Skills & Projects as its prerequisite. Of the 32 people who attended
Cowork live, **2 had attended Skills & Projects. Six percent.** Thirty people took Cowork
with no prerequisite at all.

Either drop the prereq from all learner-facing copy, or start enforcing it. Publishing it
while not enforcing it is the worst of the three options.

### 3. Applied-for programs hold. Assigned programs don't.
AFS Next runs at **93%** for its first two cohorts. The Foundations labs run at **45–52%**.
The difference is not content quality — it is that AFS Next participants *chose* it and lab
participants were *assigned*.

This is the strongest internal evidence for the "acceleration, not access" frame, and a
direct warning about assigning anyone to Augment & Automate without asking first. Expect
roughly half to no-show on an assignment; expect nine in ten on an application.

---

## The 85 Augment & Automate candidates, measured properly

| Status | n |
|---|---|
| Attended live | **35** |
| Watched recording only | 0 |
| Registered, no-show | 15 |
| Never touched a program | 33 |
| Facilitators — exclude | 2 |

By program, of the 85: AFS Next 25 attended / 33 registered · Cowork 6 / 18 ·
Skills & Projects 6 / 10.

**Reading it:** the 33 who never touched a program are self-taught builders with no BetterUp
scaffolding behind them — the strongest cohort for a program about aiming your building at
the right problems. The 15 no-shows are the second most interesting: they said yes and
didn't come, which is a calendar or relevance problem rather than a capability one, and it
deserves one question before re-inviting them.

---

## Data hygiene surfaced along the way

| Issue | Detail |
|---|---|
| **ADA cannot write back** | Zoom data for Cohorts 3 and 4 was pulled Jul 29 11:04 but the C3/C4 tabs show no marks. Matches ADA's logged `Exception: The data you entered in cell H212…` — sheet data-validation is rejecting the write. Fix the validation rule and ~10 more builders gain verified attendance instantly. |
| **Unrostered attendees** | Jen Freiman and Nick Ernst are verified attendees who appear on no cohort roster. People are attending sessions they were never rostered for. |
| **Orphan email** | Jess Lieberman — Tier A builder, 6 Projects, AFS Next attendee — is one of the 9 emails ADA repeatedly fails on. |
| **Facilitators in learner data** | Alex Zesch and David Brinegar surface as builders and attendees. Filter by role before any list ships. |
| **Self-inclusion** | Fabia appears in her own builder list. Remove before the IT handoff. |
