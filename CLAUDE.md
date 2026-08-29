# CLAUDE.md

This file is the durable copy of Lucas's memory and this repo's context. `~/.claude/CLAUDE.md` (global, outside this repo) does not survive between sessions in this remote environment — only what's committed and pushed here does. If asked to update "global memory," update this file and push it.

## WHAT — repo contents

No app code yet, no build tooling. This is a reference/planning repo: markdown docs + one static HTML file.

| File | Contents |
|---|---|
| `soul.md` | Origin story, beliefs, philosophy — the human motivation behind the business |
| `design.md` | Visual design system (color, type, spacing, component rules) for Tradie Fight Fit |
| `design-system.html` | Living, viewable component reference matching `design.md` |
| `voice.md` | Writing tone, word rules, sentence structure |
| `audience.md` | Who Tradie Fight Fit is for, the problem it solves, sourced Reddit/TikTok quotes |
| `README.md` | Placeholder, unused |

No commands to build, test, or run — nothing here executes. `design-system.html` opens directly in a browser.

## WHY — purpose of each part

- **soul.md**: read before anything about motivation, why he's building this, or messaging that needs to sound personally authentic rather than generic-business.
- **design.md** / **design-system.html**: read before any UI, mockup, landing page, or app-screen work, so new visuals stay consistent with what's already defined.
- **voice.md**: fallback source for writing voice when the `my-writing-style` skill isn't loaded (see HOW below).
- **audience.md**: read before any copy, feature prioritization, or positioning decision. Treat its quotes as ground truth over assumptions.

Read whichever file applies before answering — don't ask Lucas to re-explain what's already documented here. Update these files (and commit/push) as new answers or research come in, rather than starting from scratch each session.

## HOW — working with Lucas

**About him**: Lucas Fong, 20, Darwin NT. Refrigeration/AC apprentice (Team NT / Top End Air Conditioning & Maintenance), full-time, ~4-year apprenticeship, boss is Chris. 11 years karate, started MMA (Muay Thai + BJJ) this year, moving from KMA to Combat Therapy Centre. With Charlee, who's on the Sunshine Coast for uni; possible move there in 2028.

**Current threads**:
- Apprenticeship: awaiting trade school dates; wants to lock in tools and pathway with Chris.
- KMA gym dispute: cancelling old membership (PaySmart direct debit), unresolved as of 27 Aug 2026; new gym CTC in progress.
- Side hustle: "Tradie Fight Fit" — tradie/shift-worker fitness x MMA training, AI-built digital product.
- MMA app concept: weight-cut tracker + sparring journal + motivation feed, planned as a no-code build (e.g. Adalo).
- Recovering from wisdom tooth surgery (24 Aug 2026), not yet back at work.

**Always**:
- Give the next concrete action he can take today. Never suggest interviews, surveys, or market research — he learns by shipping, not talking.
- Give direct answers with clear recommendations, not hedging — rankings, "best option"/"worth it" verdicts, clear comparisons.
- Skip beginner-level explanations in martial arts — he's not a beginner.
- Format responses clearly and scannable without losing detail.

**Definition of done**: a concrete recommendation or verdict (not just options), clearly formatted, without over-explaining basics he already knows.

**Writing voice**: before drafting anything he'll send or publish (emails, messages, docs, posts), check for `~/.claude/skills/my-writing-style/SKILL.md`. If missing (likely — container-local, doesn't survive a fresh session), rebuild tone/word rules/sentence structure from `voice.md` in this repo instead. Offer to re-run the `setup-writing-style` flow if he wants the real skill reinstalled.
