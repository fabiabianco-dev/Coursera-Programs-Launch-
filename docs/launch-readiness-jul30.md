# Launch Readiness — All-Employee Send, Thu Jul 30 2026

**Assembled:** Wed Jul 29, 2026 · **Runway:** ~24 hours
**Read alongside** `source-of-truth-register.md`, which supersedes several numbers below.

---

## Verdict

**Not ready to send as written.** The approval and link-integrity items are fixable today.
The architecture question (C5) and the course-list contradiction are decisions, not edits.

---

## P0 — blocks tomorrow's send

### P0-0 · Wave 2 content is shipping first, with full campaign weight ⚠️ **top blocker**
See `source-of-truth-register.md` C5. `project.md` designs Wave 1 as a *targeted* invitation
with an **acceleration** message, and Wave 2 as a low-key all-employee "it's more than AI"
utility note that ships **2–3 weeks later**. Tomorrow's email is the Wave 2 message, sent to
everyone, first, as the headline — and it leads on access, which contradicts the governing
frame.

This is almost certainly what Sarah's *"is this going to everyone?"* comment is about.

### P0-1 · Sarah has three open comments on the doc that sends tomorrow
Last modified Jul 29, 17:54. All three **OPEN**:

| Anchor | Comment | Status |
|---|---|---|
| "A learning license" | "What does this mean. Its confusing if you aren't clear what a learning license is." | Fabia replied, tagged Charlotte. Unresolved. |
| Section 3 header | "what is this announcement?" | No reply |
| Section 4 header | "is this going to everyone?" | No reply |

Framing per `CLAUDE.md`: **Fabia owns the launch decision and aligns Sarah.** These are
questions to answer, not approvals to wait on. "what is this announcement?" is asked
*because Section 3 is empty* — filling it answers her.

### P0-2 · Section 3 (Manager Launch Announcement) is an empty header
Manager announcements were scheduled for **Wed Jul 29 — today** — and no copy existed.
Draft now in `manager-launch-announcement.md`, with revisions flagged.

### P0-3 · Program links in the email are duplicated and mis-pointed

| Program | Current link | Problem |
|---|---|---|
| Expand Your Range | `learning-coursera#q3` | — |
| Augment and Automate | `learning-coursera#q3` | **Same anchor as Expand Your Range** |
| Running with Claude | `claude-foundations#running` | Wrong page. Claude Foundations is the *live labs* group — not the Coursera trio. |

Canonical Coursera URLs exist and are unused — see `CLAUDE.md`. `[ADD LINK]` placeholders
also remain.

### P0-4 · The hub is probably not live
`bu-learning-hub.web.app/learning-coursera` returns **HTTP 403** here. The agent proxy is
healthy with no relay failures, so this is the site. The "Wed Jul 29 · Hub goes live" row is
struck through, and `project.md` §2 records the **hub design vision as unresolved, blocking
hub-live**. Assume NOT live.

Tomorrow's email links to the hub **6+ times**. Someone on the BetterUp network must click
every link before send.

### P0-5 · The three programs' content cannot be described accurately yet
Three incompatible course lists for Expand Your Range, two Claude courses assigned to two
programs at once, and — per `project.md` §6 — **no verified Claude course series confirmed
in the catalog.** See register C8, C9, C10.

Tomorrow's email does not need course lists. Naming the three programs and who each is for
is enough, and it avoids promising content that may not exist.

### P0-6 · The seat claim is unbounded
"A learning license opens the full Coursera catalog" reads as universal. 350 seats,
471 active non-contingent employees. One qualifying sentence, or a decision to buy up.

---

## P1 — before invitations go out Fri Aug 7

| # | Item | Detail |
|---|---|---|
| P1-1 | Program names | Program 3 has five variants; Program 2's name and Coursera slug disagree. Register C11, C12. |
| P1-2 | Missing comms sections | Doc has sections 1, 3, 4. Timeline references 1, 2, 3, 6. **AI Bulletin card** and **program invitation copy** (needed Aug 7) do not exist. |
| P1-3 | Aug 7 sequence inverts | Webinars land Aug 4/6, three days *before* the Aug 7 invitation. Register C6. |
| P1-4 | Fluency Assessment has no link | The webinar copy promises "how the AI Fluency Assessment routes you," and completion gates the licence. Status TBD. |
| P1-5 | Completion window | 6–8 weeks vs 12 unresolved. Blocks the manager email and the invitations. |
| P1-6 | No verified completion data | Foundations labs show zero verified attendance, so no prerequisite can be enforced or claimed. |

---

## Fastest path to a defensible send tomorrow

1. Decide the wave question (P0-0). Everything else is downstream of it.
2. Send the manager announcement **today** (P0-2) — it also answers Sarah's Section 3 comment.
3. Answer Sarah's three comments in-thread (P0-1).
4. Swap the three program links to canonical Coursera URLs; have someone on-network click
   every link (P0-3, P0-4).
5. Add one line bounding who gets a seat in Wave 1 (P0-6).
6. Ship without course-level detail (P0-5).
