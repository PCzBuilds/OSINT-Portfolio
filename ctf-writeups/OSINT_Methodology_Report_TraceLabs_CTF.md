# Open Source Investigative Report: Face Sheet

**Case Reference:** Trace Labs Global OSINT Search Party CTF (Hybrid: DEF CON Las Vegas plus remote)
**Report Type:** Team Coordination & Methodology After-Action Report (Portfolio Piece)
**Analyst / Team Lead:** PCzBuilds
**Date of Operation:** August 8, 2026
**Date of Report:** August 9, 2026
**Team Composition:** 4 investigators (multi-continent, remote), self-organized
**Cases Assigned:** 5 missing persons (2 personally investigated by report author)
**Result:** 28 submissions in 4 hours; team ranked 32nd of 110 teams. (Individual contribution to the team score was not separately tracked by the competition platform and cannot be isolated from the team total.)

> **Confidentiality note:** In accordance with Trace Labs data handling policy, all case-specific identifiers (names, images, locations) have been withheld or deleted post-competition. This report documents methodology, team process, and investigative reasoning only, not investigative subject data.

> **Pre-publish checklist (per Trace Labs write-up rules):**
> - [x] No individual teammates are named or singled out; team communication is discussed only in aggregate/structural terms.
> - [x] Focus on methodology and lessons learned, not case specifics, per event guidance.
> - [x] Case-specific subject data masked; report scoped to methodology and lessons learned.

---

## Key Findings & Procudures (Summary)

- Successfully stood up a segmented Discord-based case management structure (general, voice, per-subject, resources channels) with a defined data-retention/deletion protocol *before* the competition began, demonstrating pre-operation OPSEC planning independent of the investigation itself.
- Pre-vetted team members for sock puppet readiness prior to invitation, but did not verify *operational* readiness (platform fluency, responsiveness), identified as the primary root-cause failure of the exercise.
- Personally carried a disproportionate share of both coordination and investigative output due to breakdown in team communication discipline.
- Demonstrated correct investigative restraint: declined to submit a plausible but unverified family-member linkage rather than force a match: a source-verification decision, not a data-collection failure.
- Adapted collection strategy dynamically per subject based on observed source density (high-volume social media presence vs. near-zero digital footprint), rather than applying a fixed workflow to both cases.

---

## Narrative

### 1. Pre-Operation Setup
Ahead of the event, I took on team lead / coordinator duties, which were not formally assigned but assumed out of necessity. Setup included:

- A Discord server segmented into a **general/organizational channel** (rules, strategy, scheduling; no case data permitted), a **resources channel** (competition rules, Trace Labs onboarding and training links), a **voice channel**, and **individual channels per missing-persons case** for evidence and notes.
- A hard rule that no names, links, or case identifiers would be posted in the general channel, and that all case-channel content would be deleted immediately after the competition concluded, in line with Trace Labs' data handling expectations.
- A pre-event requirement that every invited participant already hold an active sock puppet account, on the reasoning that account creation and "aging" cannot be done reliably on the day of the event.
- Distribution of Trace Labs orientation and training material in advance, with an expectation (not enforced) that all members would review it before the event.

**Assessment:** This was sound OPSEC and case-management design. The failure point was not the structure. It was that "having a sock puppet" was treated as sufficient evidence of readiness, when it does not indicate whether a member can *operate* effectively on that platform under time pressure.

### 2. Event Start: Coordination Breakdown
A pre-event sync was scheduled 30 minutes before start to align on strategy and case assignment. In practice:

- Voice channel connectivity issues and slow response times consumed most of the pre-event window, so no strategy alignment occurred before the clock started.
- At competition start, without any prior coordination, teammates began independently claiming missing-persons cases in the general channel ("I picked person X"): the exact ad hoc, unstructured behavior the channel structure had been built to prevent.
- I reacted by renaming case channels to reflect first names of assigned subjects in real time, effectively improvising the case-assignment structure *after* the competition had already started, rather than before.
- With 4 investigators and 5 cases, I took the two cases left unclaimed.

**Assessment:** The infrastructure existed; the discipline to use it before zero-hour did not. This is a process failure, not a tooling failure. The fix is a hard pre-event checkpoint (e.g., "no case work begins until assignments are confirmed in writing in the general channel"), not new tools.

### 3. Investigative Workflow: Subject A
- Primary platform: Facebook (comment sections, tagged photos, reels), treated as the highest-yield source for U.S. missing-persons cases based on prior CTF experience.
- Secondary: YouTube, including independent true-crime/missing-persons interview channels, which surfaced information not present on mainstream sources.
- Search engines (Google, Yandex) used for triangulation; results cross-checked against what was already circulated by official/government sources so as to avoid submitting information investigators already had.
- Attempted reverse image search via PimEyes; found it currently gated behind payment with no free sample tier, and therefore not practically usable mid-competition. *(Tool access status should be re-verified before relying on it in future exercises: pricing/access models change.)*
- Fell back to Google Images and Yandex reverse image search; neither returned reliable matches for this subject.
- Identified a probable family member (mother) via name match, but her profile was also access-restricted, and I could not independently verify the relationship. **I did not submit this lead**, since name-matching alone is not sufficient identity verification.
- Subject A had comparatively high source density: multiple Facebook reels, tagged content, and YouTube video coverage. Strategy shifted toward exhausting social platforms and video content before falling back to search engines.

### 4. Investigative Workflow: Subject B
- Source density was dramatically lower: one or two Facebook reels, no meaningful search engine footprint, no video coverage.
- Strategy shifted accordingly: less time on social media exhaustion, more time attempting to locate any indirect mentions (local news, community posts) since the direct-source approach that worked for Subject A was unavailable here.

### 5. Scope Discipline
Explicitly avoided pivoting into techniques that would fall outside competition rules or legal/ethical bounds: specifically, did not attempt to identify email addresses or other non-publicly-accessible personal data to force identity confirmation. Leads that could not be backed by legally and publicly accessible information were treated as investigative color (useful for advancing the real-world search) rather than submittable, scoreable findings.

### 6. Team Communication
Beyond the two personally-run cases, visibility into the rest of the team's work was limited overall. Check-ins during the operation went largely unanswered, and there was no reliable way to confirm activity or progress on the other assigned cases in real time. In practice, coordination and a significant share of submissions fell to a single member of the team for the remainder of the event.

---

## Analysis

**What worked:**
- Pre-built, segmented case-management infrastructure with a clear data-retention/deletion policy: this is professional-grade practice, not typical for a second-time competitor.
- Correct application of source-verification discipline: an unverified lead (the mother's profile) was withheld rather than submitted on circumstantial grounds.
- Adaptive, source-density-driven strategy switching between two subjects with very different digital footprints, rather than a one-size-fits-all workflow.
- Scope discipline: recognizing the line between "legally/publicly accessible" and "technically obtainable," and staying on the correct side of it.

**What failed:**
- Sock puppet *possession* was verified pre-event; sock puppet *operational readiness* (platform familiarity, responsiveness under time pressure) was not, and this was the single largest driver of team underperformance.
- No hard pre-event checkpoint existed to force case assignment and strategy alignment before the clock started, despite infrastructure being ready for it.
- No enforced check-in cadence during the operation: coordination relied on voluntary responsiveness, which did not materialize.
- Individual submissions were not consistently structured (e.g., explicit source citation, confidence level, lead vs. verified evidence flag): self-identified as an area for improvement.

**Recommendations for next operation:**
1. Add a mandatory technical/operational dry run for all team members days before the event: not just confirmation of account existence, but a live test of posting/searching on the assigned platform.
2. Institute a hard rule: no case work begins until assignments are confirmed by every member in writing.
3. Set scheduled, mandatory check-in points (e.g., every 45–60 minutes) rather than relying on ad hoc responsiveness.
4. Adopt a standard submission template (source, platform, confidence level, lead vs. verified) to improve both scoring efficiency and downstream usability of submissions.
5. Track and retain (where policy allows) scoreboard/ranking evidence in real time, so after-action reports can cite verified performance data rather than recalled estimates.

---

## Appendix

- **Team size:** 4 investigators / 5 assigned cases
- **Duration:** 4 hours
- **Submissions (self-reported):** 28
- **Placement (verified):** 32nd of 110 registered teams
- **Tools referenced:** Facebook, YouTube, different Search Engines, Yandex/Google reverse image search, PimEyes (attempted, inaccessible)
- **Frameworks referenced:** Trace Labs Search Party CTF rules and orientation materials

*This report is a training/portfolio artifact. All missing-persons case data has been withheld in accordance with Trace Labs confidentiality practice. Team placement (32nd of 110 teams) is confirmed by the author using official TraceLabs final score.*
