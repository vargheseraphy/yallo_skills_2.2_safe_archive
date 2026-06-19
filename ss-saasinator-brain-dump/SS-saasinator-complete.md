# SS — saasinator · Complete Brain Dump
*Exported from Raphy Varghese's personal Claude account — June 2026*
*For re-seeding into YALLO Group Claude Organisation*

---

## 1. WHAT IS saasinator

**Product name:** saasinator (always lowercase — NEVER "Saasinator")
**Website:** saasinator.ai
**Domain registrar:** GoDaddy
**Owner:** YALLO Group
**Product Owner / Orchestrator:** Raphy Varghese
**Founder / Strategic Lead:** Sumeet Goenka

### The One-Line Pitch
saasinator is YALLO Group's "build not buy" AI platform — it challenges enterprise organisations to stop paying SaaS licence fees and instead build AI-native software they own outright.

### The Positioning Framework: "Just In Time Software"
The brand was repositioned away from vendor-attack messaging toward a build-ownership framework. The core idea: most enterprise SaaS is bloat you pay for forever. saasinator delivers custom AI software just-in-time — fast, owned, zero licence.

### Three Service Pillars (RIL)
- **LIBERATE** — Replace SaaS bloat. Exit vendor lock-in.
- **REFORGE** — Rebuild legacy systems as AI-native.
- **IGNITE** — Ship what wasn't previously possible.

### Complexity Decision Framework
- Easy → First Party AI (Claude/GPT wrappers)
- Medium → Hybrid build
- Complex → Full custom AI Factory delivery

### Who Buys It
- CIO, CFO, CTO at $1B+ revenue enterprises
- Priority geographies: UAE, KSA
- Priority sectors: Financial Services, Retail, Oil & Gas, Government, Manufacturing

---

## 2. BRAND RULES (NON-NEGOTIABLE)

- Always written **saasinator** — lowercase, never capitalised
- No pricing anywhere on site or in content
- No unverified statistics
- No AI-generated copy on insights pages — human-written only
- "Yallo Group" mentioned in footer and About only — saasinator is its own brand
- All saasinator content approved by Raphy before anything goes live
- Brand voice: direct, credible, no hype, Gulf enterprise tone

### Colour System (Dark Theme Primary)
- Background: #0A0A0A / #0D0D0D
- Surface cards: #111111 / #141414
- Primary accent: saasinator purple/violet gradient
- Anthropic partnership accent: #D97757 (orange — for Claude CCA-F certification badge)
- Typography: Plus Jakarta Sans + DM Mono

---

## 3. WEBSITE — TECHNICAL ARCHITECTURE

### Tech Stack (Locked)
- **Framework:** Next.js (started as Next.js 16, App Router)
- **Frontend:** React 19, TypeScript (strict), Tailwind CSS 4
- **Database:** Neon (Postgres) — NEVER Supabase
- **ORM:** Drizzle ORM (Phase 2)
- **Package manager:** pnpm (monorepo workspace)
- **Icons:** Lucide throughout — no emoji (SparkleIcon SVG replaced 🪄)
- **Hosting:** Vercel

### Code Rules
- No hardcoded hex in components — globals.css only for colour tokens
- All copy in data files, never in page.tsx
- Every section: forced-light OR forced-dark (never system default)
- PR-only policy on main branch
- Homepage versioning: /h1 = v1 (noindex), /h2 = v2 (noindex), / = live

### Claude Code Skills Installed in Repo
Three skills installed in `.claude/skills/`:
1. **design-taste-frontend** — anti-slop, prevents generic AI UI patterns
2. **ui-ux-pro-max** — design intelligence for Next.js
3. **design-motion-principles** — Emil Kowalski motion standards

### Key Files & Packages
```
packages/
  chat-agent/        — standalone separable chat agent package
apps/
  web/               — main saasinator.ai Next.js app

CLAUDE.md           — master rules file for Claude Code agents
.claude/
  rules/
    brand.md
    code-style.md
    animation.md
    dark-light.md
    seo.md
    components.md
    demand-gen.md   — no HubSpot; Calendly + Resend + server actions
```

---

## 4. HOMEPAGE (v3 — Current Live)

### Section Structure
1. Hero (light bg with CSS dot/line grid)
2. Logo rail (social proof logos)
3. RIL paths (LIBERATE / REFORGE / IGNITE cards)
4. Easy / Medium / Complex decision framework
5. Build Options (First Party vs Third Party AI)
6. AI Factory Methodology (animated FactoryDiagram SVG component)
7. Claude CCA-F Certification badge (Anthropic orange #D97757)
8. Governance / Security / Business Impact (CxO audience)
9. Proof section
10. Why saasinator
11. Stack Audit CTA
12. Final CTA with Sumeet's quote

### ROI Stack Audit Tool
- Trust block with counter seeded at 247
- Feedback collection to Neon DB
- Print summary (8 sections)
- LinkedIn share card
- OG metadata

---

## 5. CHAT AGENT (feat/chat-agent-v1)

### Package Location
`packages/chat-agent/` — standalone, separable from main app

### Entry Hero
Three clickable text links:
- "Escape my SaaS contract"
- "Rebuild what I own"
- "Bring my idea to life"

### UI
- Glassmorphic input field
- SparkleIcon (custom SVG sparkle — not emoji)
- Glassmorphism mega panel drops from nav bar

### Agent State Machine
```
GREETING → QUALIFYING → EDUCATING → CONVERTING → CAPTURING → HANDOFF
```

### Critical Bugs Found in QA Testing (June 2026)
**P0 — Must fix before launch:**
1. Agent fails to answer diagnostic pricing and timeline questions — deflects with "fixed-fee" + Calendly link every time. Buyers frustrated.
2. RAG retrieval weak — surfaces retail/government/hospitality content regardless of buyer's vertical (construction, logistics, fintech etc.)

**Systemic pattern across all test runs:**
- Agent performs well on: persona voice, honesty about case study gaps, buzzword avoidance
- Agent fails consistently at: conversion moment when buyer asks "what does this cost and how long does it take?"

---

## 6. CHAT AGENT TESTING FRAMEWORK

### Sprint Structure
- **Testers:** 3 people
  - Rohit Raj → 10 personas on Claude (localhost:3000)
  - Anil → 5 personas on Gemini
  - Tanzil → 5 personas on ChatGPT
- **Method:** Copy-paste loop (tester feeds persona brief to AI, AI plays buyer, tester relays to live agent)
- **Timeline:** Thursday setup, Friday EOD all scorecards in Notion, Tuesday aggregate report
- **P0 escalation:** WhatsApp to Raphy immediately

### 20 Gulf Enterprise Buyer Personas Tested
Covering UAE, Saudi Arabia, Qatar, Bahrain, Oman. Archetypes include:
- R01: Khalid Al-Mansoori — Group CIO, UAE conglomerate (SAP migration)
- R02: Fatima Al-Rashidi — CFO, Saudi logistics company (SaaS cost savings)
- R03: Pradeep Nair — CTO, UAE fintech (ServiceNow replacement)
- Aisha Mohammed Al-Zaabi — VP Operations, Abu Dhabi DED (government, data sovereignty hard blocker)
- + 16 additional personas across CIO, CFO, CTO, VP-Ops, gatekeeper, and stress-test (won't convert) archetypes

### Bug Taxonomy
- **P0** — Critical: pricing leaks, confabulation, fabricated case studies, guardrail breaks
- **P1** — High: conversion failures, RAG wrong-vertical retrieval
- **P2** — Medium: tone, pacing, persona mismatch
- **P3** — Low: UI, copy, minor UX

### Output Format
- `.md` files per persona run
- Uploaded to Notion page: "saasinator Agent Test Results"
- Aggregate report by Raphy on Tuesday

---

## 7. DIAGNOSTIC PAGE & CALENDLY

**URL:** /diagnostic
**Calendly embed:** https://go.yallo.co/saasinator_ACDC
**Session types:** Sumeet's quote featured
**Purpose:** Convert qualified buyer from chat agent to booked diagnostic session

### ACDC Methodology (Internal)
Roadmap → Waves → Sprints → Execution
Maps to Claude tools:
- Claude Chat → strategy / wave planning
- Claude Cowork → specs
- Claude Code → execution

---

## 8. COMING SOON LANDING PAGE (GitHub Pages)

**Deployed to:** saasinator.ai (GitHub Pages, GoDaddy DNS)
**Design:** Dark theme, CSS line grid, wave animations

### DNS Setup (GoDaddy)
- 4 x GitHub A records added
- www CNAME added
- Deleted "Parked" A record (was causing conflict)

### Design Decisions
- CSS line grid (replaced canvas dot grid)
- Wave animation speed reduced: `0.003 + i*0.001`, multiplier `t*speed*4`
- "Just In Time Software" text: 38% opacity (was 15%)
- "Arriving just in time." coming soon block with animated build segments
- No email capture at launch (Formspree/Tally.so considered but dropped)
- Footer: white, centred

---

## 9. BRAND ASSETS CREATED

### HTML Deliverables
- **saasinator-brand-book-v3.html** — logo golden ratio analysis, colour system, typography, voice, do/don'ts, social specs, SVG downloads, 6 gradients, 6 patterns, 4 monotone versions, Canva poster templates, 10 LinkedIn post templates (accordion), 9 ad mockups (3×3 grid)
- **saasinator-competitor-research-guide.html** — 14 competitor accounts across 3 priority tiers, 6-expert virtual research panel, step-by-step process, 4 ChatGPT/Claude prompts, SWOT framework

### Launch Landing Page Variants
- Dark v1, Light v2, Dark v3
- Logo with orbiting rings, AI wave effects, particle systems, ripple on mouse, parallax

### 404 Page Concept
- Auto-sequencing fake SAP contract that tears apart
- Reveals portal room with three LIBERATE/REFORGE/IGNITE portals

---

## 10. PROOF POINTS (KNOWN CASE STUDIES)

- **YALLO Hub (REFORGE)** — Rebuilt YALLO's own ops Claude-native; 35 screens; replaces HubSpot + Apollo + Vincere
- **MENA retail group (LIBERATE)** — 70+ brands; core platform replaced in 30 days; $0 licence post-delivery

---

## 11. GAMMA PRESENTATION

A Gamma presentation was generated from dev.saasinator.ai site content covering:
- AI Factory methodology
- 70-20-10 delivery model
- Enterprise personas

---

## 12. KEY CONTACTS & LINKS

| Item | Value |
|------|-------|
| Website | saasinator.ai |
| Domain registrar | GoDaddy |
| GitHub repo | Public repo with CNAME + index.html |
| Hosting | Vercel (main app), GitHub Pages (coming soon) |
| DB | Neon (Postgres) |
| Calendly | https://go.yallo.co/saasinator_ACDC |
| Notion results | "saasinator Agent Test Results" page |

---

*Brain dump prepared by Claude from Raphy Varghese's personal account conversation history.*
*Date: June 2026*
*Use this document to re-seed context into YALLO Group's Claude Organisation account.*
