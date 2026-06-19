---
name: abm-email-social-sequences
description: Generate email sequences (Apollo format), LinkedIn sequences, and HTML newsletters (Accumba design) for ABM campaigns. Executes persona-by-persona with approval gates to ensure quality. Creates 25-30 emails across 5 personas plus influencers, LinkedIn connection/DM templates, and 3-4 HTML newsletters.
version: 1.0
triggers:
  - "Create ABM content for {account}"
  - "Generate email sequences for {account}"
  - "Create LinkedIn and newsletter sequences for {account}"
  - "Build ABM email and social content for {account}"
  - "Generate content assets for {account}"
---

# ABM Content - Email, LinkedIn & Newsletter Sequences

**Purpose:** Create all email, LinkedIn, and newsletter content for ABM campaign with incremental execution and quality control.

**Total Outputs:** 3 deliverables  
**Estimated Time:** 60-90 minutes  
**Quality Control:** Email Marketing Director + Social Media Director + Content Director

---

## 🎯 OVERVIEW

This skill creates:
1. **Email Sequences** (Apollo CSV format) - 5 emails × 5 personas = 25-30 emails
2. **LinkedIn Sequences** - Connection + 3 DMs per persona
3. **Newsletter Sequence** (HTML) - 3-4 emails matching Accumba design

**Incremental Execution:** Create one persona at a time, get approval, then proceed to next.

---

## 📥 REQUIRED INPUTS

### Mandatory Information:

```yaml
FROM_SKILL_1:
  abm_strategy_document: [Output from Skill 1]
  account_name: "Walmart Global Tech India"
  personas_identified: [P1, P2, P3, P4, P6]
  pain_points: [From research]
  tech_stack: [From research]
  key_programmes: [From research]

CONTACT_DATA:
  contact_list: [Excel with persona assignments]
  
CAMPAIGN_DETAILS:
  landing_page_url: "go.yallo.co/walmart" (if created) OR "TBD"
  discovery_call_link: "https://app.apollo.io/#/meet/9uh-bms-x75/30-min"
```

### Optional Information:

```yaml
ADDITIONAL_CONTEXT:
  specific_messaging_angles: [Any specific angles to emphasize]
  competitor_names_to_avoid: [Don't mention these vendors]
  recent_news: [Recent company announcements to reference]
```

---

## 👥 TEAM ROLES

### Role 1: Sales Copywriter
**Responsibilities:**
- Write email sequences persona by persona
- Craft subject lines that get opened (no spam triggers)
- Structure emails using 4-step framework (Context, Challenge, Proof, CTA)
- Ensure account-specific details in every email
- Follow send schedule (Day 1, 3, 7, 14, 21)

**Quality Standard:**
- Each email under 100 words
- One metric per email maximum
- Subject lines under 50 characters
- No buzzwords or jargon
- Account-specific (not template)

---

### Role 2: Email Marketing Director (QC Manager)
**Responsibilities:**
- Review each persona's email sequence before approval
- Check tone consistency across 5 emails
- Validate CTA progression (soft → medium → direct)
- Ensure no spam trigger words
- Approve before proceeding to next persona

**Quality Checklist:**
```
✓ Subject lines under 50 chars, no spam words
✓ Email body under 100 words
✓ One metric per email (not overselling)
✓ CTA progression natural (no hard ask in Email 1-2)
✓ Account details specific (tech stack, programmes)
✓ No buzzwords (transformative, holistic, best-in-class)
```

---

### Role 3: Social Selling Expert
**Responsibilities:**
- Write LinkedIn connection requests (280 chars max)
- Craft LinkedIn DM follow-ups (no sales pitch)
- Create InMail templates (if needed)
- Ensure peer-to-peer tone (not vendor-to-buyer)
- Reference account-specific details

**Quality Standard:**
- Connection request under 280 characters
- DM 1 focuses on their challenges (not YALLO)
- DM 2 shares insight/value (still no pitch)
- DM 3 soft meeting ask (idea exchange positioning)

---

### Role 4: Social Media Director (QC Manager)
**Responsibilities:**
- Review LinkedIn sequences for authenticity
- Check character limits (280 for connection, flexible for DMs)
- Validate peer positioning (not salesy)
- Ensure account-specific references
- Approve before proceeding

**Quality Checklist:**
```
✓ Connection request under 280 chars
✓ No sales language in DM 1-2
✓ Peer-to-peer tone (knowledgeable, not vendor)
✓ References specific account details
✓ Meeting ask only in DM 3 (after value delivery)
```

---

### Role 5: Email Marketing Specialist
**Responsibilities:**
- Create 3-4 HTML newsletters matching Accumba design
- Follow TOFU/MOFU/BOFU structure
- Design comparison tables, timelines, stat rows
- Ensure brand consistency (dark theme, gold accents)
- Write in editorial tone (not promotional)

**Quality Standard:**
- Newsletter 1 (TOFU): Market intelligence, no pitch
- Newsletter 2 (MOFU): Case study, industry insight
- Newsletter 3 (MOFU): Thought leadership
- Newsletter 4 (BOFU): Direct offer, meeting CTA
- HTML renders correctly in email clients

---

### Role 6: Content Director (QC Manager)
**Responsibilities:**
- Review newsletter HTML for design consistency
- Check brand alignment (tone, colors, formatting)
- Validate TOFU/MOFU/BOFU progression
- Ensure editorial tone (not advertorial)
- Approve final HTML

**Quality Checklist:**
```
✓ Matches Accumba design system (dark, gold, tables)
✓ Newsletter 1-2 no hard pitch (value only)
✓ Newsletter 3-4 progressive CTA
✓ HTML clean (no broken tables/images)
✓ Brand voice consistent (professional, data-driven)
```

---

## 🔄 EXECUTION WORKFLOW

### STEP 1: INPUTS VALIDATION (5 minutes)

**Checklist:**
- [ ] ABM Strategy Document from Skill 1 available
- [ ] Account name confirmed
- [ ] 5 personas identified (P1, P2, P3, P4, P6)
- [ ] Pain points extracted from research
- [ ] Tech stack known
- [ ] Landing page URL available (or TBD)
- [ ] Discovery call link confirmed

**If any mandatory input missing:**
```
STOP and ask user:
"I need the following to proceed:
- [List specific missing items]

Have you completed Skill 1 (ABM Research & Strategy)? 
If yes, please share the ABM Strategy Document output.
If no, please run Skill 1 first."
```

---

### STEP 2: EMAIL SEQUENCES - INCREMENTAL EXECUTION (40-50 minutes)

**ROLE:** Sales Copywriter + Email Marketing Director

**CRITICAL:** Execute persona by persona. DO NOT create all 30 emails at once.

**Process:**
```
1. Create Persona 1 (P1) - 5 emails
   → Present to user
   → Get approval
   → ONLY THEN proceed to Persona 2

2. Create Persona 2 (P2) - 5 emails
   → Present to user
   → Get approval
   → ONLY THEN proceed to Persona 3

3. Create Persona 3 (P3) - 5 emails
   → Present to user
   → Get approval
   → ONLY THEN proceed to Persona 4

4. Create Persona 4 (P4) - 5 emails
   → Present to user
   → Get approval
   → ONLY THEN proceed to Influencers

5. Create Influencers (P6) - 5 emails
   → Present to user
   → Get approval
   → Proceed to Apollo CSV generation
```

---

#### 2.1 Email Framework (Apply to ALL emails)

**4-Step Structure:**

```
STEP 1: Context (1 sentence)
Show you know their business/team/initiative

STEP 2: Challenge (1-2 sentences)
Frame the problem they're facing (not about YALLO)

STEP 3: Micro-Proof (1 sentence)
ONE metric that shows understanding (not overselling)

STEP 4: Soft CTA (1 sentence)
Ask for conversation, idea exchange (not "see our solution")
```

**Character Limits:**
- Subject line: Under 50 characters
- Email body: Under 100 words (650 characters)
- Total email: 700 characters max

**Send Schedule:**
- Email 1: Day 1
- Email 2: Day 3 (2 days after Email 1)
- Email 3: Day 7 (4 days after Email 2)
- Email 4: Day 14 (7 days after Email 3)
- Email 5: Day 21 (7 days after Email 4)

**CTA Progression:**
- Email 1-2: NO meeting ask (value only)
- Email 3: Soft mention of conversation
- Email 4: Direct but casual ask
- Email 5: Final clear CTA with urgency

---

#### 2.2 PERSONA 1 (P1): SVP / VP - Budget Owners

**Context:**
- Strategic leaders with budget authority
- Feel programme delivery pressure from talent gaps
- Short on time, need high-value insights
- No patience for vendor pitches

**Messaging Angle:**
- Programme delivery risk from specialist gaps
- ROI of faster specialist hiring
- Peer-to-peer (architect to executive)

**Tone:** Executive briefing, data-driven, respectful of time

---

**EMAIL 1 - P1 (Day 1):**

**Subject:** `[Account] specialist hiring velocity`

**Body:**
```
Hi [First Name],

I noticed [Account] is scaling [specific programme from research] in [location].

At this stage, many retail tech GCCs face 10-14 week specialist hiring cycles that create programme delivery risk.

We've helped similar retail tech teams compress specialist hiring from 12 weeks to 72 hours through pre-vetted Bengaluru networks.

Would a brief conversation be useful?

Best,
[Your Name]
YALLO
```

**Word count:** 62 words  
**CTA:** Soft ask, no pressure  
**Metric:** One (72 hours)

---

**EMAIL 2 - P1 (Day 3):**

**Subject:** `Specialist hiring bottleneck at [Account]`

**Body:**
```
Hi [First Name],

Following up on my note about [Account]'s [programme] expansion.

When specialist roles ([Salesforce Commerce Cloud / GenAI / etc.]) stay open 10+ weeks, programme milestones slip and engineering teams absorb scope gaps.

In similar environments, we reduced specialist time-to-hire by 85% through architect-led screening and pre-vetted retail domain networks.

Worth exploring?

Best,
[Your Name]
```

**Word count:** 58 words  
**CTA:** Question (not ask)  
**Metric:** One (85%)

---

**EMAIL 3 - P1 (Day 7):**

**Subject:** `[Specific role] hiring velocity`

**Body:**
```
Hi [First Name],

I noticed [Account] has [X] [specific role] positions open.

These roles typically take 12-16 weeks to fill in Bengaluru because the talent pool has tool knowledge but lacks retail domain depth.

We maintain a pre-screened network of [specific role] specialists with [specific domain experience]. Brief to shortlist in 72 hours.

Open to a 15-minute call this week?

Best,
[Your Name]
```

**Word count:** 63 words  
**CTA:** Specific ask (15 min, this week)  
**Metric:** One (72 hours)

---

**EMAIL 4 - P1 (Day 14):**

**Subject:** `Quick question on [programme] timeline`

**Body:**
```
Hi [First Name],

If [Account]'s [programme] timeline is tight and specialist hiring is creating pressure, we can help accelerate.

Our founder (ex-Richemont Chief Architect) screens every candidate from the hiring side, not just the CV. We deliver 2 vetted candidates in 72 hours.

Could we get 20 minutes on your calendar to discuss?

[Discovery Call Link]

Best,
[Your Name]
```

**Word count:** 60 words  
**CTA:** Direct ask with link  
**Metric:** One (72 hours)

---

**EMAIL 5 - P1 (Day 21):**

**Subject:** `Last note on [Account] specialist hiring`

**Body:**
```
Hi [First Name],

Final note from me on [Account]'s specialist hiring.

If [programme] delivery is at risk from specialist gaps, we can deliver architect-vetted [specific roles] in 72 hours.

Happy to have a brief call or pass you to a colleague if someone else owns this.

Otherwise, I'll step back.

Best,
[Your Name]
```

**Word count:** 53 words  
**CTA:** Clear exit (respectful close)  
**Metric:** One (72 hours)

---

#### APPROVAL CHECKPOINT 1: P1 Email Sequence

**Email Marketing Director reviews P1 sequence:**

```
QC Checklist - P1 Emails:
[ ] All 5 subject lines under 50 chars
[ ] All 5 email bodies under 100 words
[ ] One metric per email (not overselling)
[ ] CTA progression natural (soft → direct → exit)
[ ] Account details specific ([programme], [role], [location])
[ ] No buzzwords or jargon
[ ] Tone appropriate for executive (brief, data-driven)
```

**Present to user:**
```
📧 PERSONA 1 (P1) - SVP/VP SEQUENCE COMPLETE

I've created 5 emails for P1 (SVP/VP - Budget Owners):

Email 1 (Day 1): Specialist hiring velocity - Soft intro
Email 2 (Day 3): Programme delivery risk - Value share
Email 3 (Day 7): Specific role focus - Soft ask
Email 4 (Day 14): Direct meeting request
Email 5 (Day 21): Final note with respectful exit

All emails:
✓ Under 100 words
✓ One metric each
✓ Account-specific details
✓ Executive tone

[Display all 5 emails]

APPROVAL NEEDED:
- Approve to proceed to P2?
- Request changes?
```

**WAIT FOR USER APPROVAL BEFORE PROCEEDING TO P2**

---

#### 2.3 PERSONA 2 (P2): Sr Directors - Technical Authority

**Context:**
- Technical leaders who feel delivery pain directly
- Report upward on programme velocity
- Architect-to-architect conversation
- Value technical credibility over sales pitch

**Messaging Angle:**
- Specialist gaps delaying team delivery
- Architect-led screening (peer validation)
- Technical depth + retail domain fit

**Tone:** Technical peer, credible, no vendor speak

---

**EMAIL 1 - P2 (Day 1):**

**Subject:** `[Specific tech] specialists for [Account]`

**Body:**
```
Hi [First Name],

I noticed [Account] is scaling [specific technology] capabilities in [location].

At retail tech scale, finding specialists with both [technology] depth and retail domain experience typically takes 10-12 weeks.

We've built a pre-screened Bengaluru network of [technology] specialists with retail background. Architect-validated, 72-hour delivery.

Worth a conversation?

Best,
[Your Name]
```

**Word count:** 55 words

---

**EMAIL 2 - P2 (Day 3):**

**Subject:** `Retail domain depth in [tech] hiring`

**Body:**
```
Hi [First Name],

Following up on [technology] specialist hiring for [Account].

The challenge isn't finding [technology] engineers—it's finding ones who understand retail complexity ([specific domain challenge like MDM, seasonal peaks, omnichannel, etc.]).

Our founder (ex-Richemont Chief Architect) screens from the hiring side. We assess architecture thinking and retail domain fit, not just tool knowledge.

Open to exchanging perspectives?

Best,
[Your Name]
```

**Word count:** 63 words

---

**EMAIL 3 - P2 (Day 7):**

**Subject:** `[Account] [programme] delivery velocity`

**Body:**
```
Hi [First Name],

If [Account]'s [programme] timeline is feeling pressure from specialist hiring delays, we can accelerate.

We deliver 2 architect-vetted [technology] specialists in 72 hours. Both candidates screened for retail domain depth, not just certification.

Could we get 15 minutes to discuss your specific roles?

Best,
[Your Name]
```

**Word count:** 48 words

---

**EMAIL 4 - P2 (Day 14):**

**Subject:** `Quick question on [specific role]`

**Body:**
```
Hi [First Name],

I saw [Account] has [X] [specific role] openings.

These roles typically take 12+ weeks because screening for retail domain depth is hard. We've pre-screened a Bengaluru network specifically for this gap.

Can we get 20 minutes on your calendar?

[Discovery Call Link]

Best,
[Your Name]
```

**Word count:** 48 words

---

**EMAIL 5 - P2 (Day 21):**

**Subject:** `Last note on specialist hiring`

**Body:**
```
Hi [First Name],

Final note from me.

If specialist hiring delays are impacting [programme] delivery, we can help. Architect-vetted candidates in 72 hours.

Otherwise, happy to step back and reconnect later if timing changes.

Best,
[Your Name]
```

**Word count:** 37 words

---

#### APPROVAL CHECKPOINT 2: P2 Email Sequence

**Present P2 sequence to user → Get approval → Proceed to P3**

---

#### 2.4 PERSONA 3 (P3): Directors/Managers - Delivery Pain

**Context:**
- Day-to-day team leadership
- Feel specialist gaps directly (team absorbing work)
- Escalate hiring delays when milestones slip
- Less budget authority, but strong pain signal

**Messaging Angle:**
- Team-level pressure from open roles
- Engineers absorbing specialist scope
- Delivery velocity impact

**Tone:** Empathetic, team-focused, practical

---

**EMAIL 1 - P3 (Day 1):**

**Subject:** `Specialist hiring for [Account] teams`

**Body:**
```
Hi [First Name],

I noticed [Account] is scaling [technology] teams in [location].

When specialist roles stay open 8+ weeks, delivery pressure shifts to existing team members.

We help retail tech teams fill specialist roles in 72 hours through pre-vetted Bengaluru networks.

Worth a brief conversation?

Best,
[Your Name]
```

**Word count:** 46 words

---

**EMAIL 2 - P3 (Day 3):**

**Subject:** `Team delivery pressure from open roles`

**Body:**
```
Hi [First Name],

Following up on specialist hiring for [Account].

When [specific role] positions stay open, the team absorbs that scope or work sits unassigned—both create delivery risk.

We deliver architect-vetted specialists in 72 hours. Brief to shortlist, candidates start same week.

Open to discussing?

Best,
[Your Name]
```

**Word count:** 47 words

---

**EMAIL 3 - P3 (Day 7):**

**Subject:** `[Specific role] backfill support`

**Body:**
```
Hi [First Name],

If [Account]'s [specific role] hiring is creating team delivery pressure, we can accelerate.

We maintain a pre-screened network of [role] specialists with retail background. 72-hour delivery, architect-vetted.

Could we get 15 minutes to discuss your specific needs?

Best,
[Your Name]
```

**Word count:** 43 words

---

**EMAIL 4 - P3 (Day 14):**

**Subject:** `Quick question on team capacity`

**Body:**
```
Hi [First Name],

I saw [Account] has multiple [technology] roles open.

If team delivery is feeling the impact, we can help fill those gaps quickly. Architect-screened specialists in 72 hours.

Can we get 20 minutes on your calendar?

[Discovery Call Link]

Best,
[Your Name]
```

**Word count:** 45 words

---

**EMAIL 5 - P3 (Day 21):**

**Subject:** `Last note - specialist support`

**Body:**
```
Hi [First Name],

Final note from me.

If specialist hiring delays are creating delivery pressure, happy to discuss how we accelerate. Otherwise, I'll step back.

Best,
[Your Name]
```

**Word count:** 28 words

---

#### APPROVAL CHECKPOINT 3: P3 Email Sequence

**Present P3 sequence to user → Get approval → Proceed to P4**

---

#### 2.5 PERSONA 4 (P4): TA/HR - Champions

**Context:**
- Manage specialist hiring pipeline
- Open to overlay capacity for hard-to-fill roles
- Can facilitate intros to engineering leadership
- Collaborative positioning critical (not competitive)

**Messaging Angle:**
- Specialist capacity overlay (not replacement)
- Support for hard-to-fill roles only
- Partnership model (you own client relationship)

**Tone:** Collaborative, supportive, non-threatening

---

**EMAIL 1 - P4 (Day 1):**

**Subject:** `Specialist capacity for [Account] TA`

**Body:**
```
Hi [First Name],

I work with TA teams on overlay capacity for hard-to-fill specialist roles.

For [Account]'s [technology] positions, we provide pre-screened candidates in 72 hours while your team maintains the process.

Worth a brief conversation?

Best,
[Your Name]
```

**Word count:** 41 words

---

**EMAIL 2 - P4 (Day 3):**

**Subject:** `Partnership model for specialist roles`

**Body:**
```
Hi [First Name],

Following up on specialist hiring support for [Account].

We work alongside TA teams—not instead of. You brief us on hard-to-fill roles, we deliver architect-vetted candidates in 72 hours, you manage client relationship.

Open to discussing how we partner?

Best,
[Your Name]
```

**Word count:** 45 words

---

**EMAIL 3 - P4 (Day 7):**

**Subject:** `Specialist hiring overlay capacity`

**Body:**
```
Hi [First Name],

If [Account] has specialist roles ([Salesforce / GenAI / Data / etc.]) sitting open 8+ weeks, we can provide overlay capacity.

We focus only on hard-to-fill roles where standard sourcing takes longest. You stay in control.

Could we get 15 minutes to discuss?

Best,
[Your Name]
```

**Word count:** 49 words

---

**EMAIL 4 - P4 (Day 14):**

**Subject:** `TA partnership for [specific role]`

**Body:**
```
Hi [First Name],

I saw [Account] has [specific role] positions open.

If those are proving hard to fill, we can provide specialist capacity. You maintain the relationship—we accelerate sourcing.

Can we get 20 minutes to discuss partnership model?

[Discovery Call Link]

Best,
[Your Name]
```

**Word count:** 45 words

---

**EMAIL 5 - P4 (Day 21):**

**Subject:** `Last note - specialist capacity`

**Body:**
```
Hi [First Name],

Final note from me.

If specialist hiring support would be useful for hard-to-fill roles, happy to discuss. Otherwise, I'll step back.

Best,
[Your Name]
```

**Word count:** 28 words

---

#### APPROVAL CHECKPOINT 4: P4 Email Sequence

**Present P4 sequence to user → Get approval → Proceed to P6**

---

#### 2.6 PERSONA 6 (P6): TPM/PM - Influencers (Referral Bridge)

**Context:**
- No hiring authority
- Feel delivery impact from specialist gaps
- Can refer to decision makers
- Goal: Get a name, not a meeting

**Messaging Angle:**
- Brief, light touch
- Referral ask (not meeting ask)
- Acknowledge they don't own hiring

**Tone:** Quick, respectful, no pressure

---

**EMAIL 1 - P6 (Day 1):**

**Subject:** `Who handles [tech] hiring at [Account]?`

**Body:**
```
Hi [First Name],

I'm trying to reach whoever manages specialist tech hiring ([Salesforce / GenAI / Data]) at [Account].

Could you point me in the right direction?

Best,
[Your Name]
YALLO
```

**Word count:** 31 words

---

**EMAIL 2 - P6 (Day 3):**

**Subject:** `Quick referral question`

**Body:**
```
Hi [First Name],

Following up on my question about who handles specialist hiring at [Account].

We help retail tech teams fill specialist roles faster—would be great to connect with the right person.

Any guidance appreciated.

Best,
[Your Name]
```

**Word count:** 39 words

---

**EMAIL 3 - P6 (Day 7):**

**Subject:** `[Account] specialist hiring contact?`

**Body:**
```
Hi [First Name],

Still trying to connect with whoever owns specialist tech hiring at [Account].

We work with retail tech GCCs on hard-to-fill roles. Even just a name would be helpful.

Thanks,
[Your Name]
```

**Word count:** 35 words

---

**EMAIL 4 - P6 (Day 14):**

**Subject:** `Final ask - hiring contact`

**Body:**
```
Hi [First Name],

Last note from me.

If you can point me to whoever handles specialist tech hiring at [Account], I'd appreciate it.

Otherwise, no worries.

Best,
[Your Name]
```

**Word count:** 30 words

---

**EMAIL 5 - P6 (Day 21):**

**Subject:** `Thanks anyway`

**Body:**
```
Hi [First Name],

Thanks for considering my request about [Account]'s hiring contact.

I'll find another path in.

Best,
[Your Name]
```

**Word count:** 19 words

---

#### APPROVAL CHECKPOINT 5: P6 Email Sequence

**Present P6 sequence to user → Get approval → Proceed to Apollo CSV**

---

#### 2.7 Apollo CSV Generation

**ROLE:** Sales Copywriter

**Task:** Compile all approved emails into Apollo import format

**CSV Structure:**
```
persona,email_number,send_day,subject,body
P1,1,1,"[Account] specialist hiring velocity","Hi [First Name]..."
P1,2,3,"Specialist hiring bottleneck at [Account]","Hi [First Name]..."
P1,3,7,"[Specific role] hiring velocity","Hi [First Name]..."
P1,4,14,"Quick question on [programme] timeline","Hi [First Name]..."
P1,5,21,"Last note on [Account] specialist hiring","Hi [First Name]..."
P2,1,1,"[Specific tech] specialists for [Account]","Hi [First Name]..."
...
[Continue for all personas]
```

**Format Notes:**
- Escape commas in email body with quotes
- Use {{first_name}} merge tag for Apollo
- Use {{company}} merge tag where account name appears
- Include all 25-30 emails

**Save as:** `/mnt/user-data/outputs/[Account]_Email_Sequences_Apollo.csv`

---

### STEP 3: LINKEDIN SEQUENCES (15-20 minutes)

**ROLE:** Social Selling Expert + Social Media Director

**Task:** Create LinkedIn connection + DM sequences for each persona

**Format:** Document with templates (not CSV)

---

#### 3.1 LinkedIn Structure (All Personas)

**Sequence:**
```
CONNECTION REQUEST (280 chars max)
  ↓ Wait 2-3 days after acceptance
DM 1 (Day 3 after connection)
  ↓ Wait 4 days
DM 2 (Day 7 after DM 1)
  ↓ Wait 7 days
DM 3 (Day 14 after DM 2) - Meeting ask
```

---

#### 3.2 PERSONA 1 (P1): SVP/VP LinkedIn

**CONNECTION REQUEST (280 chars):**
```
Hi [First Name],

I've been following [Account]'s tech expansion in [location]. Impressed with how the [programme] is scaling. 

I work with retail tech GCCs on specialist hiring velocity. Would value connecting.

Best,
[Your Name]
```
**Character count:** 227

---

**DM 1 (Day 3 after connection):**
```
Hi [First Name],

Thanks for connecting.

I noticed [Account] is scaling [technology] capabilities. Many retail tech GCCs face 10-14 week specialist hiring cycles at this stage.

We've been analyzing these patterns—happy to share insights if useful.

Best,
[Your Name]
```

---

**DM 2 (Day 7 after DM 1):**
```
Hi [First Name],

We recently helped a similar retail tech GCC reduce specialist time-to-hire from 12 weeks to 72 hours through pre-vetted Bengaluru networks.

Might be relevant for [Account]'s [programme] if specialist hiring is creating delivery pressure.

Worth a brief conversation?

Best,
[Your Name]
```

---

**DM 3 (Day 14 after DM 2):**
```
Hi [First Name],

Final note from me.

If [Account]'s specialist hiring is creating programme delivery risk, we can help accelerate. Architect-vetted candidates in 72 hours.

Open to 15-20 minutes?

[Discovery Call Link]

Best,
[Your Name]
```

---

#### 3.3 Repeat for P2, P3, P4, P6

**Create LinkedIn sequences for all 5 personas following same structure:**
- Connection request (account-specific, under 280 chars)
- DM 1 (value share, no pitch)
- DM 2 (insight + soft mention)
- DM 3 (meeting ask with link)

---

#### Social Media Director QC Review

**QC Checklist - LinkedIn Sequences:**
```
[ ] Connection requests all under 280 chars
[ ] No sales language in DM 1-2
[ ] Peer-to-peer tone (not vendor-to-buyer)
[ ] Account-specific references in each message
[ ] Meeting ask only in DM 3
[ ] Discovery call link included in DM 3
```

**Save as:** `/mnt/user-data/outputs/[Account]_LinkedIn_Sequences.md`

---

### STEP 4: NEWSLETTER SEQUENCE (25-30 minutes)

**ROLE:** Email Marketing Specialist + Content Director

**Task:** Create 3-4 HTML newsletters matching Accumba design system

**Design Reference:** Accumba Issue 03 (dark theme, gold accents, comparison tables)

---

#### 4.1 Newsletter Design System

**Brand Colors:**
- Page background: `#F4F4F2`
- Dark surface: `#202020`
- Card: `#2B2B2B`
- Border: `#E8E8E6`
- Body text: `#202020` (light bg) / `#F4F4F2` (dark bg)
- Grey: `#888888` / `#AAAAAA`
- YALLO gold: `#D6B24C`
- Dark gold: `#BFA25E`

**Typography:**
- Headers: Georgia, serif
- Body: Arial, Helvetica, sans-serif
- Stats: Georgia (large numbers)

**Components:**
- Header (gold bar, ACCUMBA branding)
- Hero block (dark, large stats/comparison)
- Content blocks (white background, clean tables)
- Stat rows (3-column, dark background)
- CTA section (dark, gold button)
- Footer (dark, gold accents)

---

#### 4.2 NEWSLETTER 1 (TOFU): Market Intelligence

**Subject:** `The [specific market trend] pattern in [City] GCC hiring`

**Theme:** Educational, no YALLO pitch, pure market intelligence

**Content Structure:**
```
HEADER
- ACCUMBA branding
- Issue number
- go.yallo.co/[account]

HERO
- Large stat comparison (2019 vs 2025, Bengaluru vs Chennai, etc.)
- Compelling headline about market shift

INTRO
- 2-3 paragraphs on market trend
- Why it matters for retail tech GCCs

COMPARISON TABLE
- 8-10 rows comparing two market conditions
- Highlight differences in specialist hiring

VISUAL TIMELINE
- Show hiring velocity comparison
- Standard sourcing vs pre-vetted network

STAT ROW (3 stats)
- Key market metrics

WHAT WORKS SECTION
- 3 numbered points on successful approaches

QUOTE
- Sumeet Goenka quote on market dynamics

CTA
- Soft CTA (educational resource, not meeting)
```

**Save as:** `/mnt/user-data/outputs/[Account]_Newsletter_1_TOFU.html`

---

#### 4.3 NEWSLETTER 2 (MOFU): Case Study

**Subject:** `How [similar company] filled [X] specialist roles in [timeframe]`

**Theme:** Case study, industry insight, light YALLO mention

**Content Structure:**
```
HEADER

HERO
- Case study company name
- Challenge statement

INTRO
- Context on the company
- What they faced (similar to [Account])

THE CHALLENGE (section)
- Specific pain points
- Timeline pressure
- Stakes

YALLO'S APPROACH (section)
- What we did (brief)
- How it worked

RESULTS (section)
- Quantified outcomes
- Client quote

COMPARISON
- Before vs After

CTA
- Medium CTA (learn more, not hard sell)
```

**Save as:** `/mnt/user-data/outputs/[Account]_Newsletter_2_MOFU.html`

---

#### 4.4 NEWSLETTER 3 (MOFU): Thought Leadership

**Subject:** `Why [specific trend] changes [account]'s hiring strategy`

**Theme:** Thought leadership, strategic insight, positioning YALLO expertise

**Content Structure:**
```
HEADER

HERO
- Bold statement about trend
- Why conventional wisdom is wrong

INTRO
- Set up the argument
- Why this matters for [Account]

3-5 MAIN POINTS
- Numbered sections
- Each with data/example

YALLO COVERAGE SECTION
- How YALLO addresses the trend
- What we do differently

CTA
- Progressive CTA (discuss strategy)
```

**Save as:** `/mnt/user-data/outputs/[Account]_Newsletter_3_MOFU.html`

---

#### 4.5 NEWSLETTER 4 (BOFU): Direct Offer

**Subject:** `Accelerate [Account]'s [programme] with specialist capacity`

**Theme:** Direct offer, clear value prop, meeting CTA

**Content Structure:**
```
HEADER

HERO
- Direct statement of offer
- Clear benefit

INTRO
- Acknowledge their specific challenge
- Position YALLO as solution

VALUE PROPOSITION (3 columns)
- What we deliver
- How it works
- Why it's different

PROOF POINT
- Brief case study or stat

CTA SECTION
- Clear meeting ask
- Gold button with discovery call link
- Secondary: Reply to email

FOOTER
```

**Save as:** `/mnt/user-data/outputs/[Account]_Newsletter_4_BOFU.html`

---

#### Content Director QC Review

**QC Checklist - Newsletters:**
```
[ ] Newsletter 1-2: No hard pitch (educational/case study)
[ ] Newsletter 3-4: Progressive CTA (thought leadership → offer)
[ ] HTML matches Accumba design (dark theme, gold, tables)
[ ] All tables/stats render correctly
[ ] Brand voice consistent (professional, data-driven)
[ ] Account name referenced throughout
[ ] Links work (landing page, discovery call)
```

---

### STEP 5: FINAL DELIVERY TO USER (5 minutes)

**Present all outputs:**

```
✅ SKILL 2 COMPLETE - EMAIL, LINKEDIN & NEWSLETTER SEQUENCES

I've created 3 deliverables for [Account Name]:

📧 OUTPUT 1: Email Sequences (Apollo CSV)
- 25-30 emails across 5 personas
- Send schedule: Day 1, 3, 7, 14, 21
- Ready to import into Apollo
- File: [Account]_Email_Sequences_Apollo.csv

💼 OUTPUT 2: LinkedIn Sequences
- Connection + 3 DMs per persona (5 personas)
- Character limits respected
- Peer-to-peer tone throughout
- File: [Account]_LinkedIn_Sequences.md

📰 OUTPUT 3: Newsletter Sequence (HTML)
- 4 newsletters (TOFU → MOFU → MOFU → BOFU)
- Matches Accumba design system
- Ready to send via Accumba Mail
- Files: 
  - [Account]_Newsletter_1_TOFU.html
  - [Account]_Newsletter_2_MOFU.html
  - [Account]_Newsletter_3_MOFU.html
  - [Account]_Newsletter_4_BOFU.html

Next Steps:
1. Import email sequences into Apollo
2. Use LinkedIn templates for outreach
3. Schedule newsletters via Accumba Mail
4. Proceed to Skill 3 (Landing Page & Pitch Deck)

Would you like me to:
- Make any changes to the sequences?
- Proceed to Skill 3?
```

---

## ⚠️ COMMON PITFALLS TO AVOID

### Email Sequences:
❌ Overselling (multiple metrics per email)
❌ Hard ask too early (Email 1-2 should have no meeting ask)
❌ Generic templates (not account-specific)
❌ Buzzwords (transformative, holistic, synergy)

### LinkedIn Sequences:
❌ Sales pitch in connection request
❌ Exceeding 280 character limit for connection
❌ Vendor-to-buyer tone (should be peer-to-peer)

### Newsletters:
❌ Hard pitch in Newsletter 1-2 (should be educational)
❌ Breaking Accumba design system
❌ Not progressive (TOFU → BOFU should build naturally)

---

## 🎯 SUCCESS METRICS

**This skill is successful when:**

1. **Email sequences approved:**
   - All personas completed with user approval
   - Apollo CSV ready to import
   - No template language (account-specific throughout)

2. **LinkedIn sequences validated:**
   - All under character limits
   - Peer-to-peer tone confirmed
   - No sales pitch in early DMs

3. **Newsletters render correctly:**
   - HTML matches Accumba design
   - TOFU → BOFU progression natural
   - Brand voice consistent

4. **User feedback:**
   - "These emails are specific to our account"
   - "I can use these verbatim"
   - "The LinkedIn tone is perfect"

---

## 📝 INCREMENTAL APPROVAL LOG

```
[TIMESTAMP] SKILL 2 STARTED

[TIMESTAMP] P1 Email Sequence Created
→ Presented to user
→ USER APPROVED
→ Proceeding to P2

[TIMESTAMP] P2 Email Sequence Created
→ Presented to user
→ USER APPROVED
→ Proceeding to P3

[TIMESTAMP] P3 Email Sequence Created
→ Presented to user
→ USER REQUESTED CHANGES: [details]
→ REVISED
→ USER APPROVED
→ Proceeding to P4

[TIMESTAMP] P4 Email Sequence Created
→ Presented to user
→ USER APPROVED
→ Proceeding to P6

[TIMESTAMP] P6 Email Sequence Created
→ Presented to user
→ USER APPROVED
→ Generating Apollo CSV

[TIMESTAMP] Apollo CSV Generated
→ 30 emails compiled
→ File created

[TIMESTAMP] LinkedIn Sequences Created
→ 5 personas, 4 templates each
→ Social Media Director QC APPROVED

[TIMESTAMP] Newsletter 1 (TOFU) Created
→ Market intelligence theme
→ Content Director QC APPROVED

[TIMESTAMP] Newsletter 2-4 Created
→ All newsletters complete
→ Content Director QC APPROVED

[TIMESTAMP] SKILL 2 COMPLETE
Duration: 75 minutes
Quality: All QC checkpoints passed
```

---

**END OF SKILL 2: EMAIL, LINKEDIN & NEWSLETTER SEQUENCES**
