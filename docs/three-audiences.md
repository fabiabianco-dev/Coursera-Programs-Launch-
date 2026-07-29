# The Three Audiences — Enrollment Definition

**Built:** Jul 29, 2026 from `phased_training_plan_2_3.html` (Lee's Apr 14 TPS plan,
207 roster members, Claude Analytics Jan 1 – Apr 4 2026).
**Named rosters:** generated to scratchpad as CSV — **not committed.** They carry names,
titles, levels and per-person usage. See `.gitignore`.

---

## The cut

| Audience | n | Critical role | P6+/leader | Messages (min / avg / max) | Mapped from |
|---|---|---|---|---|---|
| **Expand Your RANGE** | **61** | 10 | 28 | 0 / 75 / 180 | Senior Leader Intervention (10) + Skills & Projects (51) |
| **Running with Claude + Augment & Automate** | **46** | 0 | 13 | 169 / 273 / 462 | Claude Cowork (46) |
| **Keep Your RANGE** | **100** | 25 | 36 | 215 / 818 / 2752 | AFS Next (100) |
| | **207** | 35 | 77 | | |

The bands separate cleanly on usage — 75 / 273 / 818 average messages, with almost no
overlap at the boundaries (Expand tops out at 180, Running starts at 169, Keep starts at
215). That is a real signal, not an artifact of the phase labels.

---

## ⚠ Problem 1 — "Keep Your RANGE" is not a Coursera program

The three curated programs are **Expand Your RANGE**, **Running with Claude**, and
**Augment & Automate Your BetterUp Processes**. There is no "Keep Your RANGE" in the
catalog, in `PROGRAMS_1.md`, or on the hub.

Two readings, and they cost very different amounts:

1. **A label, not a program** — these 100 are already fluent (avg 818 messages) and are
   mid-flight in AFS Next. "Keep Your RANGE" means *sustain*: no new Coursera enrollment,
   just catalog access and continued AFS Next. **Zero build cost.**
2. **A new fourth program** — needs curation, and Coursera's curation clock is **7 days**.
   With invitations going out Aug 7, that is tight but not impossible if the skill
   selection goes to Nana immediately.

Reading 1 is the recommendation. These are the people who least need a course.

## ⚠ Problem 2 — 28 of the 61 in the entry program are P6+ or leaders

This is the one to fix before anything sends. Merging Lee's Phase 2 into Expand Your RANGE
puts executives into the beginner program alongside P3 individual contributors:

| Level | Msgs | Name | Title |
|---|---|---|---|
| E2 | 0 | Damian Vaughn | Chief Programs Officer |
| E3 | 9 | Sebastian Scheiter | Senior Vice President, Sales |
| E2 | 21 | Lyndsey Cochrun | VP, Client Partnership & Behavioral Science |
| E2 | 79 | Karen Lai | VP, Global Accounts |
| E2 | 112 | Abhi Shrikhande | Vice President, Platform Deployment |
| E3 | 113 | Ryan Weber | **Chief Customer Officer** |
| E2 | 141 | Mandy Schluensen | VP, Revenue Marketing |
| E3 | 180 | Samantha DeStefano | SVP, Strategic & Enterprise Accounts |

Lee separated these people into "Senior Leader Intervention" **on purpose**, with a
three-stage progressive track (Skills & Projects → Cowork → Hackathon) delivered **1:1 or
small-group**. The design note is explicit: *"their adoption has outsized organizational
impact… meets them where they are."*

Collapsing that into a mass entry-program invitation means the Chief Customer Officer gets
the same "anyone early with AI begins here" email as a P3. That is the kind of message that
ends a program's credibility with the exec team.

**Recommendation:** keep the same *content*, split the *delivery*. One audience on paper,
two invitation paths:

- **61 → Expand Your RANGE**, of which
  - **51** get the standard learner invitation
  - **10** get a 1:1 or small-group approach from their HRBP or Fabia directly, never a
    mass email

---

## Nine people with effectively zero usage

All land in Expand Your RANGE, which is correct — but five have *literally zero* messages,
and one is a Chief Officer. These need a human conversation, not an enrollment email.

| Msgs | Level | Name |
|---|---|---|
| 0 | P4 | Claire Burrow |
| 0 | E2 | Damian Vaughn |
| 0 | M2 | Gina Gottardo |
| 0 | P3 | Leonidas Kalai |
| 0 | P4 | Lindsay Pilla |
| 2 | P3 | Jessica Schild |
| 6 | S2 | Caprice Williams |
| 8 | P3 | Genesis Bravini |
| 9 | E3 | Sebastian Scheiter |

---

## Two scope limits to state out loud

**1. This covers 207 people, not the company.** The July roster has **468** matched
employees and **471** active non-contingent. So roughly **264 people are not in this plan
at all.** They still need routing — `audience-routing-model.md` covers the full population
on the newer data.

**2. The data is four months old.** Lee's plan reads Claude Analytics **Jan 1 – Apr 4**.
The current roster reads **Jun 21 – Jul 20** and tells a materially different story:
94.7% adoption, and construction — not usage — as the real gap. Anyone whose usage moved
since April is mis-banded here.

**Recommendation:** use the April plan for the *structure* (three bands, the separation
logic, the senior-leader carve-out) and re-band the individuals against the July data
before invitations go out. The bands hold; the specific names will shift.

---

## Third problem, smaller — the combined audience carries two programs

"Running with Claude + Augment & Automate" bundles programs **2 and 3** of an ordered
on-ramp. `PROGRAMS_1.md` gates Augment & Automate on comfort with Claude, and its real
entry condition is *owning a repeatable process worth automating* — a self-selection
question, not a usage threshold.

Assigning both at once to all 46 is roughly double the learning load and ignores that gate.
Cleaner: all 46 start **Running with Claude**, and Augment & Automate opens to those who
name a process they own. That question can ride along in the invitation.

---

## What needs deciding

1. **"Keep Your RANGE"** — sustain label, or a real fourth program to curate?
2. **The 10 senior leaders** — carve out the delivery, or send the standard invitation?
3. **Re-band on July data**, or ship the April bands?
4. **Split the combined audience** into sequential enrollment, or assign both?
