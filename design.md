# Tradie Fight Fit — Design System

Reference doc for `design-system.html`. Pulled from UFC-style fight-broadcast
language (Fight Pass, athlete profile pages): near-black grounds, condensed
bold display type, a red/gold corner-accent pair, and stat-block typography
built for numbers. Adapted for Tradie Fight Fit — a training app for
shift-working tradies doing MMA on the side.

Single dark theme, deliberately. This is a fight-night aesthetic, not a
brand that flips to a bright mode — every token below is set explicitly so
the page holds its look regardless of host theme.

---

## Color

| Token | Hex | Use |
|---|---|---|
| `--color-ground` | `#0C0B0E` | Page background. Near-black with a faint red-violet undertone, not pure black. |
| `--color-surface` | `#17151A` | Card and panel fill. |
| `--color-surface-raised` | `#201D24` | Hover / elevated state on surface. |
| `--color-ink` | `#F3F1ED` | Primary text. Warm off-white, not `#FFF`. |
| `--color-ink-muted` | `#9B98A3` | Secondary text, captions, stat labels. |
| `--color-red` | `#E22E24` | **Fight Red** — primary accent. Corner marks, live badges, primary CTAs, matchup dividers. |
| `--color-gold` | `#D6A02E` | **Cage Gold** — secondary accent. Upsell CTAs, highlighted price tier, "coming up" arrows. Used sparingly — one gold element per section, max. |
| `--color-red-dim` | `#7A1912` | Pressed/border state for red elements. |
| `--color-line` | `#2A2730` | Hairline dividers, card borders. |

**Rule:** red and gold never touch as adjacent fills — one is the accent in
play, the other sits quiet. Gold marks the premium/upgrade path specifically
(pricing, upsells); red marks everything else (primary actions, live status,
energy). Don't let gold become a second primary color.

Text on `--color-surface` uses `--color-ink` (contrast ~14:1) or
`--color-ink-muted` (~6:1) — both clear AA on dark ground. Red and gold are
accent/graphic colors, not body-text colors; used for text only at large
display sizes (headlines, stat numbers) where contrast is less critical and
never for running copy.

---

## Type

Three roles, three faces:

| Role | Face | Fallback | Weights |
|---|---|---|---|
| Display | **Anton** | Arial Narrow, sans-serif | 400 (single-weight, use size for hierarchy) |
| Body | **Barlow** | Helvetica Neue, sans-serif | 400, 500, 600, 700 |
| Data | **JetBrains Mono** | Courier New, monospace | 400, 500, 700 |

Load via Google Fonts:
```html
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Anton&family=Barlow:wght@400;500;600;700&family=JetBrains+Mono:wght@400;500;700&display=swap">
```

**Anton** — headlines, hero numbers, section labels. Always uppercase,
tight tracking (`-0.01em` to `-0.02em`). This is the fight-poster voice —
use it loud, but only for the thing that should win the section.

**Barlow** — everything you read: body copy, buttons, nav, card text.
Chosen over the safer Inter/Space Grotesk defaults because it reads
blue-collar and functional (drawn from road-sign and license-plate
lettering) — it fits a tradie-facing product without costume-ing it.

**JetBrains Mono** — anywhere digits need to line up: stat blocks, weight
figures, session counts, prices, timers. Set with `font-variant-numeric:
tabular-nums`.

### Scale

| Token | Size | Face | Use |
|---|---|---|---|
| `--text-caption` | 0.75rem | Barlow 600, uppercase, +0.06em tracking | Eyebrow labels, stat captions |
| `--text-body-sm` | 0.875rem | Barlow 400 | Secondary copy |
| `--text-body` | 1rem | Barlow 400 | Default running copy, 1.6 line-height |
| `--text-lead` | 1.25rem | Barlow 500 | Intro paragraphs, card lead lines |
| `--text-h4` | 1.5rem | Anton, uppercase | Card titles |
| `--text-h3` | 2.25rem | Anton, uppercase | Section sub-heads |
| `--text-h2` | 3rem | Anton, uppercase | Section heads |
| `--text-h1` | clamp(2.75rem, 6vw, 4.5rem) | Anton, uppercase | Page/hero headline — used once per page |
| `--text-stat` | 2.5rem | JetBrains Mono 700, tabular-nums | Stat block numbers |

Body copy stays under ~65 characters per line. Headlines get
`text-wrap: balance`.

---

## Spacing

4px base grid: `4 · 8 · 12 · 16 · 24 · 32 · 48 · 64 · 96`. Section padding
uses the 64/96 steps; component internals use 12–24; tight groups (icon +
label) use 4–8. Layout is flex/grid + `gap` — no stacked margins.

---

## Components

**Buttons**
- Primary — solid Fight Red fill, ink text, sharp corners (2px radius, not
  rounded-pill — this brand is square-jawed, not soft).
- Secondary — 1.5px red outline, transparent fill, red text; fills solid on
  hover.
- Gold CTA — reserved for upgrade/upsell moments only (pricing tier, "go
  Camp"). Solid gold fill, `--color-ground` text for contrast.

**Badges / weight tags** — small caps, 1px border in the relevant accent
color, transparent fill, corner-clipped (4px cut corner, not rounded) —
echoes the bracket/corner-tick marks broadcast graphics use to frame data.

**Stat block** — label (`--text-caption`, muted) stacked over value
(`--text-stat`, mono). Laid out in a row with hairline dividers between
stats, mirroring the Height / Weight / Reach layout from the athlete
profile reference.

**Matchup card** — two-sided card split by a diagonal red seam with "VS" at
the center, each side carrying a name + one stat line. Built for anything
framed as a head-to-head (session vs. rest day, this week vs. last week).

**Pricing card** — surface panel, price in mono, feature list with red
check marks, one card visually promoted (gold top border + "MOST POPULAR"
tag) — direct lift from the Fight Pass monthly/annual pattern.

**Corner ticks** — an optional 8px L-shaped bracket at two opposing corners
of a card, in the card's accent color. Use on exactly one hero component
per page, not everywhere — it's a highlight device, not a default border.

---

## Voice

Direct, short sentences, imperative where it's an action ("Log the
session," not "You can log your session here"). No hype-bro fitness
copy — the audience trains around a trade job, not around a content
calendar. Numbers over adjectives: "4 sessions this week" beats "crushing
your goals."

---

## Do / Don't

- Do keep gold rare — it should read as a signal, not a color choice.
- Do set every stat and price in the mono face, tabular-nums.
- Don't round corners on buttons or cards — square/cut corners are the
  brand's throughline.
- Don't run Anton below ~1.25rem — it loses legibility small; drop to
  Barlow 600/700 uppercase instead for small emphasis text.
- Don't add a light theme. This system is dark-committed.
