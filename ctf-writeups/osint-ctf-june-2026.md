# Down the Rabbit Hole: My Experience at TraceLabs OSINT CTF June 2026

*A beginner-friendly writeup on chasing digital ghosts, forgetting to score points, and accidentally caring too much.*

---

## Setting the Scene

OSINT CTFs are a strange genre of competition. Unlike traditional hacking CTFs where you're cracking systems and capturing flags from servers, OSINT challenges ask you to do something deceptively simple: **find people**. Real investigative techniques, fictional (or semi-fictional) targets, a clock ticking down, and a scoreboard reminding you that this is, in fact, a game.

At OSINT CTF June 2026, the scenario was built around five missing persons. Five different individuals. Five sets of starting clues. And somewhere out there in the open web, the answers.

Our team finished **18th out of 123**. Not bad. But honestly? We could have been top ten. More on that later.

---

## The Toolkit: Simpler Than You'd Think

Before diving into the cases, here's what I used — no fancy paid tools, no elite frameworks:

- **Facebook** (with a sock puppet account)
- **YouTube**
- **TikTok**
- **TinEye** (reverse image search)
- **Search Engines** (good old fashioned searching)

If you're a beginner reading this, don't let OSINT intimidate you. The most powerful tool I used was a fake Facebook account and patience.

---

## The Cases

### The Five Missing Persons

The CTF presented five separate missing persons cases. Each came with starting information — names, photos, usernames, fragments of a life — and the goal was to dig up as much verifiable, legally-sourced information as possible and submit it as flags.

What struck me almost immediately was how much people leave behind online without realising it. Across all five cases, **Facebook alone was a treasure trove**: family members, classmates, distant relatives, businesses, phone numbers, addresses, physical descriptions. People tag each other. They comment on old photos. They leave breadcrumbs everywhere, often years apart, that when assembled together paint a surprisingly complete picture of someone's life and disappearance.

My takeaway after this CTF: **Facebook is probably the single best platform for missing persons investigations**, and it is chronically underestimated in OSINT discussions that tend to focus on flashier tools.

---

### MP1: The One That Got Away (From the Scoreboard)

MP1 was my deepest dive, and the most bittersweet outcome of the whole competition.

Starting from the initial clues, I built out a network of family profiles and friends. Through Facebook digging I uncovered a significant backstory: MP1 had reportedly been defrauded of a large sum of money by someone close to them. That person quickly became the main suspect.

Then came the YouTube breakthrough. I found an **unblurred CCTV video** — the kind that news outlets sometimes publish without realising what they're revealing — that showed the vehicle MP1 was last seen in. Clear enough to read the licence plate.

I had the plate. I tried to run it through available registries but hit a wall — no accessible public lookup that would confirm ownership. Then the trail shifted anyway: the suspect had **abandoned the vehicle and fled by motorbike**. The car was a dead end in terms of tracking, but his name wasn't.

And this is where TikTok came in. Searching his name turned up his TikTok profile — and there on his feed was a video casually showing off his motorbike. The same one he'd used to disappear.

I had a licence plate. A suspect profile. A motorbike. Fresh news from YouTube pointing to an approximate location.

And then — mid-CTF — **MP1 was marked as found**.

I never got to submit those flags. The window closed. All that digging, and the scoring system moved on before I could cash in. But here's the thing: **MP1 was found**. Someone, somewhere, using similar leads or perhaps the very information circulating in that investigation, located them. That's the point. That's what this is actually about.

---

## The Mistake I Made (And Why I Don't Regret It)

Here's the honest part.

I lost a lot of points because I kept forgetting to submit flags. Not because I didn't find things — I found a lot — but because I got so absorbed in the actual investigation that the gamified layer of the CTF completely slipped my mind. I was building timelines, cross-referencing profiles, following leads. I was treating it like a real case.

In competitive terms, that cost us. We left a top-ten finish on the table.

But I can't bring myself to call it a mistake in any meaningful sense. The instinct to actually *help* rather than just *score* feels like the right instinct to have if you ever want to do this kind of work for real. The gamified wrapper is useful for building skills. The underlying mission — finding missing people — is not a game.

**If you're doing an OSINT CTF for the first time:** submit early, submit often. The moment you find something useful, log it. Don't wait until you've built the full picture. Flags are often incremental, and cases can close without warning.

---

## What I'd Tell a Beginner

**1. Facebook is not dead.** Ignore the narrative that it's an old person's platform. For OSINT purposes, its longevity is exactly what makes it powerful. Years of posts, tags, and life events, all searchable.

**2. Sock puppet accounts matter.** Some profiles are semi-private. A blank account with no obvious investigator markers will see things a cold search won't. Build one, keep it clean, use it ethically.

**3. YouTube is an underrated OSINT source.** News segments, documentaries, and user-uploaded footage often contain inadvertently revealing details — unblurred footage, background details, location giveaways.

**4. Reverse image search everything.** TinEye and Google Images will surprise you. A photo that seems generic often has a traceable origin.

**5. Don't get lost in rabbit holes without logging what you find.** I speak from experience. The rabbit holes are real, they are deep, and the clock doesn't stop while you're in them.

**6. Remember what OSINT is actually for.** The skills you build in these CTFs — cross-referencing, source evaluation, building a picture from fragments — are the same skills used by real investigators, journalists, and volunteers who find real missing people. Take that seriously.

---

## Final Score

**18th out of 123 teams.** With flags I forgot to submit, probably top ten. With MP1's window closing on me mid-investigation, definitely some points left on the table.

But MP1 was found.

I'll take that result any day.

---

*Written as a post-event reflection on TraceLabs OSINT CTF June 2026. All personal data and research data from/about the investigation targets was deleted after the conclusion of the CTF. All sources used were legal and publicly accessible.*
