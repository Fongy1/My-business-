# Global Memory

Always give me the next concrete action I can take today. Never tell me to interview people, survey, or do market research — I learn by shipping, not talking.

## About Me

Lucas Fong, 20, Darwin NT. Refrigeration/AC apprentice (Team NT / Top End Air Conditioning & Maintenance), signed on full-time, ~4-year apprenticeship, boss is Chris. 11 years karate, started MMA (Muay Thai + BJJ) this year, moving from KMA to Combat Therapy Centre. In a relationship with Charlee, who's on the Sunshine Coast for uni; possible move there in 2028.

## Current Projects

- Apprenticeship: awaiting trade school dates; wants to lock in tools and pathway with Chris.
- KMA gym dispute: trying to cancel old membership (PaySmart direct debit), unresolved as of 27 Aug 2026; new gym CTC in progress.
- Side hustle: settled on an AI digital product idea, "Tradie Fight Fit" (tradie/shift-worker fitness x MMA training).
- MMA app concept: weight-cut tracker + sparring journal + motivation feed, planned as a no-code build (e.g. Adalo).
- Recovering from wisdom tooth surgery (24 Aug 2026), not yet back at work.

## How I Like to Work

Wants direct answers with clear recommendations, not hedging — rankings, "best option"/"worth it" verdicts, clear comparisons. Not a beginner in martial arts (skip beginner-level explanations there). Prefers well-formatted, visually structured responses without losing detail.

## Definition of Done

An answer gives a concrete recommendation or verdict, not just options; is formatted clearly (structured, scannable); and doesn't over-explain basics he already knows (MMA/martial arts especially).

## Writing voice

Before drafting anything he'll send or publish (emails, messages, docs, posts): check for `~/.claude/skills/my-writing-style/SKILL.md`. If it's missing (likely — it's container-local and doesn't survive a fresh session), rebuild it from `voice.md` in this repo instead — same tone/word rules/sentence structure, just not auto-invoked as a skill. Offer to re-run the setup-writing-style flow if he wants the real skill reinstalled.

## Business reference files (this repo)

Read whichever applies before answering — don't ask him to re-explain what's already here.

- **soul.md** — who he is at a human level: origin story, beliefs, philosophy. Read before anything about motivation, why he's building this, or messaging that needs to sound personally authentic rather than generic-business.
- **design.md** — the visual design system (color, type, spacing, component rules) for Tradie Fight Fit. Read before any UI/mockup/landing-page/app-screen work so new visuals stay consistent with what's already built (see also `design-system.html` for the living component reference).
- **voice.md** — writing tone/word rules/sentence structure. See "Writing voice" above — this is the fallback source when the skill isn't loaded.
- **audience.md** — who Tradie Fight Fit is for, the problem it solves, and real sourced quotes from Reddit/TikTok research on how that audience actually talks about their problem. Read before any copy, feature prioritization, or positioning decision for the app — treat the quotes in it as ground truth over assumptions.

Update these files (and re-commit/push) as new answers or research come in, rather than starting from scratch each time.

## Note on persistence

This file is the durable copy. `~/.claude/CLAUDE.md` (global, outside this repo) does not survive between sessions in this remote environment — only what's committed and pushed here does. If asked to update "global memory," update this file, not just the home-directory one, and push it.
