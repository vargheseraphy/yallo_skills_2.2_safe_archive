---
name: yallo-patterns
version: 1.0.0
description: |
  YALLO Group approved background patterns and textures for brand design work.
  Use this skill whenever working on any YALLO brand asset that needs a background
  treatment — presentations, social posts, letterhead, proposals, email banners,
  business cards, or any digital/print design. Covers all 10 approved patterns
  (A–J), correct opacity values, dark vs light surface rules, CSS code, SVG tiles,
  and the explicitly rejected patterns list. Trigger this skill any time the user
  asks about YALLO backgrounds, textures, patterns, watermarks, grid overlays,
  or glow effects — even if they just say "add a background" or "make it look
  more branded".
---

# YALLO Patterns & Textures

Core rule: **patterns support content, never compete with it.**
One pattern per layout. Max 10% opacity when text sits above any pattern.

## Quick reference

| ID | Name | Opacity | Surface | Best use |
|----|------|---------|---------|----------|
| A | Petal tile | 7% | Dark | Social posts, presentations |
| B | Fine grid | 4% | Dark | All dark surfaces, slides |
| C | Gradient glow | 20%/8% | Dark | Hero sections, cover slides |
| D | Diagonal lines | 3% | Dark | Technical/CTO decks |
| E | Dot grid | 18% dot | Dark | Data slides, precision context |
| F | Large watermark | 5% | Dark | Letterhead digital, cover slides |
| G | Fine grid | 5% | Light | Letterhead, formal print |
| H | Dot grid | 12% dot | Light | Proposals, client reports |
| I | Gold glow | 8% | Light | Print letterhead corner accent |
| J | Large watermark | 4% | Light | Letterhead body, formal docs |

## Dark patterns (A–F) — use on #000, #111, #1F1F1F

Read `references/patterns-dark.md` for full CSS code for each pattern.

## Light patterns (G–J) — use on #FFF, #F9F9F7, #F4F4F2

Read `references/patterns-light.md` for full CSS code for each pattern.

## SVG tiles

Read `references/svg-tiles.md` for copy-paste SVG code for tile-based patterns (A, E, H, F, J).

## Rejected patterns — never use

Read `references/rejected.md` for the full list with reasons.

## Usage rules (always apply)

1. One pattern per layout — never layer two patterns
2. Opacity cap: never exceed 10% when text appears above
3. Dark (A–F): digital and screen only
4. Light (G–J): print, letterhead, formal proposals only
5. Never place patterns over photography
6. Always add a dark overlay/vignette if pattern reduces text readability
7. Pattern C (gradient glow): approved for hero sections and cover slides only — do not use on every slide
8. Pattern F / J (watermark): icon must be centred, never tiled
