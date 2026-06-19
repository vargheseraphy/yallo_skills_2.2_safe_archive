# AI LMS — YALLO AI Academy · Complete Brain Dump
*Exported from Raphy Varghese's personal Claude account — June 2026*
*For re-seeding into YALLO Group Claude Organisation*

---

## 1. WHAT IS THE YALLO AI ACADEMY LMS

**Product name:** YALLO AI Academy LMS
**Domain:** academy.yallo.co
**Product Owner:** Raphy Varghese
**Developer:** Aditya Nagpure (AI Intern, reports to Raphy)
**Methodology:** Saasinator AI Factory (SAIF) — governance-first, dispatch-driven

### What It Is
A learning-management platform (LMS) + CMS for the YALLO AI Academy. It combines:
- Public marketing site
- Auth-gated learner experience
- Trainer portal (course authoring)
- B2B HR portal (corporate training buyer access)

All four surfaces are built in a single Next.js 15 application.

### Origin
Assigned as Aditya Nagpure's primary product on his first day (June 2026). Described in team standup as "a fresh product" — greenfield, not a rebuild.

---

## 2. TECH STACK (LOCKED — DO NOT DEVIATE)

| Layer | Technology |
|-------|-----------|
| Framework | Next.js 15 (App Router) |
| Language | TypeScript (strict) |
| CSS | Tailwind v4 |
| UI Components | shadcn/ui |
| Auth | Auth.js v5 (Google OAuth) |
| Database | Neon Postgres 16 + pgvector |
| ORM | Drizzle ORM |
| Package manager | PNPM |
| Linter/Formatter | Biome |
| Web hosting | Vercel |
| AI/worker hosting | DigitalOcean |
| Database hosting | Neon |

### Explicitly Forbidden
- ❌ Supabase
- ❌ Prisma
- ❌ npm or yarn lockfiles (pnpm only)

---

## 3. ARCHITECTURE — SPLIT HOST MODEL

```
┌─────────────────────────────────────────────────┐
│                    VERCEL                        │
│  Next.js 15 App + Route Handlers                 │
│  (web UI, API routes, SSR pages)                 │
│  Proxies AI requests → DigitalOcean worker       │
└───────────────────┬─────────────────────────────┘
                    │ proxied requests
┌───────────────────▼─────────────────────────────┐
│               DIGITAL OCEAN WORKER               │
│  AI streaming + Background jobs                  │
│  Embeddings generation                           │
│  Dropout scoring                                 │
│  ANTHROPIC_API_KEY lives HERE ONLY               │
└───────────────────┬─────────────────────────────┘
                    │
┌───────────────────▼─────────────────────────────┐
│                    NEON                          │
│  Postgres 16 + pgvector                          │
│  Shared DB across Vercel + DO worker             │
└─────────────────────────────────────────────────┘
```

**Critical security rule:** ANTHROPIC_API_KEY lives only on the DigitalOcean worker. Vercel proxies AI requests across — never holds the key directly.

---

## 4. DATA MODEL

**35-table canonical schema (ratified — do not change without dispatch)**

### Core Data Principles
- **Multi-tenancy:** via `org_id` on all relevant tables
- **Soft-delete:** via `deleted_at` timestamp (never hard delete)
- **Audit trail:** immutable `audit_log` table
- **Quiz integrity:** tamper-proof quiz scoring via separate `app_grader` DB role

### Key Table Groups (inferred from architecture)
1. **Identity & Auth** — users, orgs, sessions, oauth_accounts
2. **Content** — courses, modules, lessons, quiz_questions, quiz_answers
3. **Learner** — enrollments, progress, quiz_attempts, quiz_scores, certificates
4. **Trainer** — trainer_assignments, draft_versions, publish_history
5. **B2B / HR Portal** — org_licenses, org_members, org_reports
6. **AI Features** — embeddings, ai_interactions, dropout_scores, recommendations
7. **System** — audit_log, notifications, feature_flags

---

## 5. PRODUCT SURFACES

### Surface 1: CMS / Public Marketing Site
Routes: `/`, `/courses`, `/pricing`, `/about`, `/insights`
Purpose: Awareness, lead generation, course discovery

### Surface 2: LMS — Learner Experience (Auth-Gated)
Routes: `/dashboard`, `/learn/*`, `/quiz/*`, `/cert/*`, `/my-courses`, `/certificates`, `/profile`
Purpose: Course consumption, quiz taking, certificate earning

### Surface 3: Trainer Portal
Routes: `/trainer/*`
Features: Course authoring → Module authoring → Lesson authoring → Quiz authoring → Publish workflow
Purpose: Content creators build and manage course content

### Surface 4: Admin / Org Portal (Planned Sprint 2+)
Routes: `/admin`, `/org`
Purpose: Corporate HR buyers manage team licenses, track completions

---

## 6. GOVERNANCE — SAIF METHODOLOGY

**SAIF = Saasinator AI Factory**

### Core Principle
Governance-first, dispatch-driven. Every change must trace to a ratified dispatch packet. No scope improvisation. No cowboy coding.

### Process Flow
```
Brief → Ratified Dispatch Packet → Build → Eval → Raphy Acceptance Gate → Deploy
```

### What Raphy Owns as Product Owner
- Sprint prioritisation
- Dispatch governance (approves all dispatch packets before build starts)
- Stakeholder alignment
- UX decisions
- Feature scope approval
- Acceptance gates on all shipped work

### What Aditya Nagpure Owns
- All development execution
- Technical implementation decisions within scope
- Code quality and test coverage

### Golden Rule
**Raphy sets scope. Aditya builds. Nothing ships without Raphy sign-off.**

---

## 7. AI FEATURES (DIGITAL OCEAN WORKER)

### Embeddings
- Content embeddings stored in Neon via pgvector
- Used for semantic search, recommendations, and AI tutoring features

### Dropout Scoring
- Background job on DigitalOcean worker
- Scores learner dropout risk based on engagement patterns
- Triggers intervention workflows (nudge emails, tutor alerts)

### AI Streaming
- Lesson explanations, quiz hints, AI tutor responses
- Streamed from DigitalOcean worker via Vercel proxy
- Key: ANTHROPIC_API_KEY never exposed to Vercel edge

---

## 8. TEAM STRUCTURE FOR LMS

| Person | Role | Involvement |
|--------|------|-------------|
| Raphy Varghese | Product Owner | Strategy, scope, sign-off, governance |
| Aditya Nagpure | AI Intern Developer | All development execution |
| Sumeet Goenka | Founder / Sponsor | Strategic direction, escalation |
| Rafi | Web & Dev Lead | Available for guidance / architecture review |

---

## 9. CONTENT OWNERSHIP

| Content Type | Created By | Approved By | Published By |
|-------------|-----------|------------|-------------|
| Academy course content | Subject matter experts / Trainers | Raphy | Trainer via portal |
| LMS feature scope | Raphy | Raphy | — |
| Code and builds | Aditya Nagpure | Raphy (acceptance gate) | Raphy approves dispatch |
| Marketing copy (academy.yallo.co) | Raphy | Raphy | Aditya Nagpure deploys |

---

## 10. RELATIONSHIP TO saasinator

The YALLO AI Academy LMS is:
- A SEPARATE product from saasinator.ai
- Built using the **SAIF (Saasinator AI Factory) methodology** — same governance, different product
- Owned by Raphy as Product Owner (same as saasinator brand/web ownership)
- Using a different tech stack from saasinator website (Next.js 15 vs saasinator's Next.js 16/Nuxt 3)
- Hosted at academy.yallo.co (subdomain of yallo.co, not saasinator.ai)

---

## 11. KNOWN DECISIONS & NON-DECISIONS

### Locked Decisions
- Tech stack (see Section 2) — ratified, not up for debate
- Split-host architecture (Vercel + DigitalOcean + Neon) — ratified
- 35-table data model — ratified
- Drizzle ORM (not Prisma) — ratified
- Auth.js v5 with Google OAuth — ratified

### Deferred / Not Yet Decided
- Admin portal (/admin, /org) — Sprint 2+
- B2B pricing model and licensing tiers — not yet defined
- Content library and course catalogue — not yet defined
- Certificate design and blockchain verification — not yet discussed
- Mobile app — not in scope

---

## 12. STANDUP NOTES (June 2026 — First Day)

From Aditya Nagpure's onboarding standup:
- Aditya assigned Academy LMS as his "fresh" primary product
- Instructed to: review materials, get briefed on Academy BRD/PRD/roadmap, plan own sprints, connect with Rafi on screens and Sumeet on ACDC methodology
- Context: saasinator.ai v2 site (Next.js, ~10 pages) was in rebuild; LMS is greenfield
- ACDC methodology: ~23 skills coded, ~80-90% complete at time of standup
- All team moving to enterprise Claude licence for AI-assisted development

---

*Brain dump prepared by Claude from Raphy Varghese's personal account conversation history.*
*Date: June 2026*
*Use this document to re-seed context into YALLO Group's Claude Organisation account.*
