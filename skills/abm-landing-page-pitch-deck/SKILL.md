---
name: abm-landing-page-pitch-deck
description: Generate landing page content (PDF for web team) and account-specific pitch deck (12 slides). Landing page includes hero, pain points, solution, case study, FAQ. Pitch deck covers challenge, YALLO difference, proof points, commercial model, and next steps.
version: 1.0
triggers:
  - "Create landing page for {account}"
  - "Generate pitch deck for {account}"
  - "Build landing page and pitch deck for {account}"
  - "Create ABM sales assets for {account}"
  - "Generate presentation materials for {account}"
---

# ABM Landing Page & Pitch Deck

**Purpose:** Create landing page content (PDF for web team) and account-specific pitch deck for client meetings.

**Total Outputs:** 2 deliverables  
**Estimated Time:** 40-50 minutes  
**Quality Control:** UX Director + Commercial Director

---

## 🎯 OVERVIEW

This skill creates:
1. **Landing Page Content** (PDF, content-only) - 8-10 pages for web team implementation
2. **Pitch Deck PPT** (12 slides) - Account-specific presentation for client meetings

**No wireframes or design specs** - just text content organized by section.

---

## 📥 REQUIRED INPUTS

### Mandatory Information:

```yaml
FROM_SKILL_1:
  abm_strategy_document: [Output from Skill 1]
  account_name: "Walmart Global Tech India"
  pain_points: [From research]
  tech_stack: [From research]
  key_programmes: [From research]
  personas_identified: [P1, P2, P3, P4, P6]

CAMPAIGN_DETAILS:
  landing_page_url: "go.yallo.co/walmart"
  discovery_call_link: "https://app.apollo.io/#/meet/9uh-bms-x75/30-min"
```

### Optional Information:

```yaml
CASE_STUDIES:
  similar_accounts: [Names of similar retail/tech companies YALLO has worked with]
  metrics_achieved: [Specific outcomes to reference]

YALLO_VALUE_PROPS:
  founder_credentials: "Ex-Richemont Chief Architect, 15 years retail tech"
  key_differentiators: ["72-hour delivery", "2:1 CV ratio", "Architect-vetted"]
```

---

## 👥 TEAM ROLES

### Role 1: Conversion Copywriter
**Responsibilities:**
- Write landing page content (hero, pain points, solution, case study, FAQ)
- Structure content for conversion (clear CTAs, benefit-focused)
- Ensure account-specific details throughout
- Write for web (scannable, concise, clear hierarchy)

**Quality Standard:**
- Hero section under 100 words
- Pain points specific to account (not generic)
- Solution items benefit-focused (not feature lists)
- Case study relevant to account's industry/scale
- FAQ addresses real objections

---

### Role 2: UX Director (QC Manager)
**Responsibilities:**
- Review landing page content for conversion flow
- Validate CTA placement and strength
- Ensure content hierarchy is clear
- Check that web team has enough detail
- Approve before delivery

**Quality Checklist:**
```
✓ Hero section clear and compelling
✓ Pain points resonate with target persona
✓ Solution items benefit-focused
✓ Case study relevant and credible
✓ FAQ addresses objections
✓ CTAs clear and action-oriented
✓ Content organized for web team handoff
```

---

### Role 3: Sales Enablement Manager
**Responsibilities:**
- Create 12-slide pitch deck structure
- Write account-specific content for each slide
- Include proof points and metrics
- Position commercial model appropriately
- Create clear next steps slide

**Quality Standard:**
- Slide 1-3: Problem framing (their challenge)
- Slide 4-7: Solution positioning (YALLO difference)
- Slide 8-9: Proof (case study, metrics)
- Slide 10: Commercial model (flexible, not pushy)
- Slide 11-12: Next steps and close

---

### Role 4: Commercial Director (QC Manager)
**Responsibilities:**
- Review pitch deck for strategic coherence
- Validate value proposition clarity
- Ensure commercial positioning is appropriate
- Check that deck flows naturally
- Approve before delivery

**Quality Checklist:**
```
✓ Problem framing resonates with account's pain
✓ Solution positioning differentiated (not generic)
✓ Proof points credible and relevant
✓ Commercial model flexible (not prescriptive)
✓ Next steps clear and low-friction
✓ Deck can stand alone (no presenter required)
```

---

## 🔄 EXECUTION WORKFLOW

### STEP 1: INPUTS VALIDATION (5 minutes)

**Checklist:**
- [ ] ABM Strategy Document from Skill 1 available
- [ ] Account name confirmed
- [ ] Pain points identified
- [ ] Tech stack known
- [ ] Landing page URL confirmed
- [ ] Discovery call link available

**If any mandatory input missing:**
```
STOP and ask user:
"I need the following to proceed:
- [List specific missing items]

Have you completed Skill 1 (ABM Research & Strategy)? 
If yes, please share the outputs.
If no, please run Skill 1 first."
```

---

### STEP 2: LANDING PAGE CONTENT (20-25 minutes)

**ROLE:** Conversion Copywriter

**Task:** Create content-only PDF for web team

**Format:** Text blocks organized by section (no design, no wireframes)

---

#### 2.1 LANDING PAGE STRUCTURE

**8 Core Sections:**
```
1. Hero Section
2. Pain Points (3-column grid or 3 blocks)
3. Why Choose YALLO (6 items)
4. Founder Credibility
5. How It Works (4 steps)
6. Case Study
7. FAQ (6 questions)
8. Contact/CTA Section
```

---

#### SECTION 1: HERO

**Content to provide:**

```
SUPER HEADING (All caps, small text):
FOR [ACCOUNT NAME]'S [LOCATION] TECH HUB

HEADING (Large, bold, 8-12 words):
Hire Retail Specialist Engineers in 72 Hours, Not 12 Weeks

DESCRIPTION (2-3 sentences, 40-60 words):
YALLO delivers architect-vetted [specific technologies from research] specialists who understand [specific domain complexity] so [Account]'s [specific programmes] stay on track.

PRIMARY CTA BUTTON:
Book Discovery Call

SECONDARY CTA BUTTON:
See How We Work

4 TRUST BADGES (below buttons):
✓ 72-hour delivery
✓ 2:1 CV ratio
✓ Architect-vetted
✓ Retail domain experts
```

**Example:**
```
SUPER HEADING:
FOR WALMART GLOBAL TECH INDIA'S BENGALURU & CHENNAI TECH HUB

HEADING:
Hire GenAI & Data Engineering Specialists in 72 Hours, Not 12 Weeks

DESCRIPTION:
YALLO delivers architect-vetted GenAI, Snowflake, and Kubernetes specialists who understand retail scale and omnichannel complexity so Walmart's platform transformation programmes stay on track.

PRIMARY CTA: Book Discovery Call
SECONDARY CTA: See How We Work

✓ 72-hour delivery
✓ 2:1 CV ratio  
✓ Architect-vetted
✓ Retail domain experts
```

---

#### SECTION 2: PAIN POINTS

**3-Column Grid (or 3 blocks):**

**Title for Section:**
```
We Know Your Hiring Challenge
[X]+ specialist roles. 12-week hiring cycles. Programme delivery at risk.
```

**Pain Point 1: Hiring Velocity Bottleneck**
```
Title: Hiring Velocity Bottleneck

Description:
100+ applicants per role, 3-week reposts, 8-12 week time-to-hire creating 3-4 week programme slippage for [specific programmes].
```

**Pain Point 2: Specialist Scarcity**
```
Title: Specialist Scarcity

Description:
Finding [specific technology] architects or [specific technology] engineers with retail domain experience—not just tool knowledge—takes 10-14 weeks in Bengaluru market.
```

**Pain Point 3: Programme Delivery Risk**
```
Title: Programme Delivery Risk

Description:
When [programme 1], [programme 2], and [programme 3] run simultaneously, every week of specialist hiring delay creates delivery risk and escalation pressure.
```

**Note to web team:**
```
Design as 3-column grid on desktop, stack on mobile. 
Each column has icon (choose appropriate) + title + description.
Use subtle background color differentiation.
```

---

#### SECTION 3: WHY CHOOSE YALLO

**Section Title:**
```
WHY RETAIL TECH LEADERS CHOOSE YALLO
```

**6 Items (each with title + description):**

**Item 1:**
```
Title: Strategy + Execution, Not Just Staffing

Description:
We're not a traditional staffing firm. YALLO was founded by Sumeet Goenka—former Group Chief Architect at Richemont (luxury retail, €20B revenue) and Chief Enterprise Architect at Landmark Group (Middle East retail, $6B revenue). We've led omnichannel transformations at Burberry, Ted Baker, and built tech teams at retail scale. We know your pain because we've lived it.
```

**Item 2:**
```
Title: 72-Hour Talent Delivery

Description:
While traditional hiring takes 12 weeks, YALLO delivers architect-vetted talent in 72 hours. We maintain a curated network of retail tech specialists already screened for domain expertise.
```

**Item 3:**
```
Title: 2:1 CV Ratio (Not 20:1)

Description:
You see 2 candidates maximum—both architect-vetted and retail experienced. No wasting time screening 20 generic profiles.
```

**Item 4:**
```
Title: Retail Domain Expertise

Description:
Your [specific technology] architect needs to understand [specific domain requirements like MDM, OMS, POS integration, seasonal peaks, omnichannel flows]—not just [technology] APIs.
```

**Item 5:**
```
Title: Contract Flexibility

Description:
Transformation programmes have peaks. Contract talent lets you right-size teams for programme phases without post-programme bloat.
```

**Item 6:**
```
Title: Architect-Led Screening

Description:
Every candidate is screened by enterprise architects with 15+ years in retail tech. We assess system design thinking and resilience architecture—not just keywords.
```

**Note to web team:**
```
Design as 2-row × 3-column grid.
Each item has icon + title + description.
Maintain visual consistency with rest of page.
```

---

#### SECTION 4: FOUNDER CREDIBILITY

**Section Title:**
```
FOUNDED BY A RETAIL TECH LEADER
```

**Content:**

```
NAME:
Sumeet Goenka

TITLE:
Founder & CEO, YALLO

PHOTO:
[LinkedIn headshot - provide URL or note "to be added by web team"]

QUOTE (2-3 sentences):
"When I was at Richemont and Landmark, I faced the same hiring challenge [Account] faces today: How do you hire 50+ specialist roles without derailing programme timelines? That's why I built YALLO—to solve the problem I lived as a retail tech leader."

CREDENTIALS (bullet list):
• Former Group Chief Architect, Richemont (€20B revenue)
• Chief Enterprise Architect, Landmark Group ($6B revenue)
• Head of Enterprise Architecture, Alshaya Group
• Led omnichannel transformations at Burberry, Ted Baker, Vodafone
• Hired 1,000+ engineers globally
• Deep expertise: SAP, Oracle Retail, Salesforce Commerce Cloud, POS systems, AWS

LINKEDIN LINK:
[LinkedIn profile URL]
```

**Note to web team:**
```
Design with photo on left (or top on mobile), quote prominent, credentials below.
LinkedIn icon/link included.
Use testimonial/quote styling.
```

---

#### SECTION 5: HOW IT WORKS

**Section Title:**
```
Your Pathway to Faster Talent Acquisition
```

**4 Steps (numbered):**

**Step 1:**
```
Number: 1
Title: Discovery Call
Timeframe: 20 minutes

Description:
Share your hiring roadmap, tech stack, and programme timelines. We assess fit and scope.
```

**Step 2:**
```
Number: 2
Title: Architect-Led Screening
Timeframe: 48 hours

Description:
Our retail tech architects screen our curated network. We assess domain fit, not just keywords.
```

**Step 3:**
```
Number: 3
Title: Candidate Presentation
Timeframe: 24 hours

Description:
You see max 2 candidates—both vetted. Review CVs, meet candidates, make decision.
```

**Step 4:**
```
Number: 4
Title: Onboarding & Delivery
Timeframe: Same week

Description:
Talent starts immediately. We handle contracts, compliance, onboarding logistics.
```

**CTA at bottom:**
```
Start with a Discovery Call →
[Link to discovery call]
```

**Note to web team:**
```
Design as horizontal timeline or vertical steps.
Each step has large number + title + timeframe badge + description.
Visual flow should be clear (step 1 → 2 → 3 → 4).
```

---

#### SECTION 6: CASE STUDY

**Section Title:**
```
PROVEN RESULTS
```

**Case Study Structure:**

```
CASE STUDY TITLE:
How We Helped [Similar Company] Build Their [Technology] Platform in Weeks, Not Months

COMPANY NAME:
[Similar company - e.g., Alshaya Group, Middle East retail, $6B revenue]

THE CHALLENGE (2-3 sentences):
[Similar company] needed to rapidly scale their [technology] team. Traditional hiring was taking 10-12 weeks. Programme milestones were at risk.

YALLO'S APPROACH (4-5 bullet points):
Within 72 hours, we delivered architect-vetted [technology] specialists:
• Assembled dedicated team of experienced [technology] engineers
• Provided enterprise architecture oversight
• Enabled rapid onboarding—engineers contributed from day one
• Supported flexible team scaling to match programme milestones

THE RESULTS (4-5 bullet points):
✓ Delivery timelines met through fast mobilization
✓ Robust [technology] architecture established
✓ Optimized cost through scalable team structures
✓ Expanded engagement for subsequent phases

PULL QUOTE (1 sentence, italic):
"Fast hiring does not mean compromising on quality. It means having the right network already vetted."

CLOSING QUESTION (account-specific):
Could this approach work for [Account]'s [their specific technologies] hiring?

CTA:
Book a Discovery Call
[Link to discovery call]
```

**Note to web team:**
```
Design with clear visual separation between Challenge/Approach/Results.
Use checkmarks for results.
Pull quote should be prominent (italic, larger font).
CTA button at bottom.
```

---

#### SECTION 7: FAQ

**Section Title:**
```
Questions About Specialist Hiring, Answered

[Account]'s transformation depends on finding the right talent fast. Here are the questions we hear most from retail tech leaders about accelerating [specific technologies] hiring without compromising quality.
```

**6 FAQ Questions:**

**Q1:**
```
Question: How can you deliver talent in 72 hours?

Answer:
We maintain a pre-screened Bengaluru network of retail tech specialists. While traditional sourcing starts from scratch (post job → wait for applications → screen 100+ CVs), we've already done that work. When you brief us on a role, we're matching against candidates already validated for retail domain depth. Our founder (ex-Richemont Chief Architect) screens every candidate personally. That's why we deliver in 72 hours with a 2:1 CV ratio—not 20 profiles after 12 weeks.
```

**Q2:**
```
Question: What if the candidate doesn't work out?

Answer:
We learn and iterate at no additional cost. If both candidates don't meet your bar, share the feedback and we'll refine our understanding and deliver a new shortlist within 48 hours. First iteration is included. That said, our track record is strong: 85% of candidates we present pass client technical interviews because we screen for retail domain depth upfront.
```

**Q3:**
```
Question: Is this more expensive than traditional hiring?

Answer:
We're competitively priced with traditional staffing firms, but you get architect-vetted candidates in 72 hours instead of 12 weeks. The real cost isn't our fee—it's the programme delivery risk from 10-12 week specialist hiring delays. When [programme name] milestones slip because specialist roles stay open, the business impact far exceeds any staffing cost difference.
```

**Q4:**
```
Question: Do you only work with [Account]?

Answer:
No. We work with multiple retail tech GCCs across India, Middle East, and globally. Our specialization in retail tech means we understand the domain complexity you face—whether it's [technology 1], [technology 2], or [technology 3] at retail scale.
```

**Q5:**
```
Question: What's your placement success rate?

Answer:
85% of candidates we present pass client technical interviews and 90% of placed candidates complete their contract term successfully. We screen for both technical depth and retail domain fit, which reduces false positives and improves retention.
```

**Q6:**
```
Question: Can you support both [Location 1] onsite and [Location 2] remote?

Answer:
Yes. We source primarily from Bengaluru but can deploy talent to [Location 1] onsite, [Location 2], or support hybrid/remote models. Our network includes specialists with flexibility for different work arrangements.
```

**Note to web team:**
```
Design as expandable accordion (click to open/close).
Questions visible by default, answers hidden until clicked.
Clean, minimal design.
```

---

#### SECTION 8: CONTACT/CTA

**Section Title:**
```
Let's build your dream team.
```

**Intro Text:**
```
Fill out the form, and a dedicated talent expert will contact you within 24 hours to discuss your specific needs.

• Save dozens of hours on sourcing and screening
• Access top 5% of tech talent in your region
• Fill critical roles faster than ever before
```

**Form Fields:**
```
Name * (First Last)
Email *
Company * [Pre-filled: Account name]
Role/Title
Message *

[Submit Button: "Book Discovery Call"]
```

**Alternative CTA:**
```
Or schedule directly:
[Button: "Book 30-Min Call"] → [Discovery call link]
```

**Note to web team:**
```
Standard contact form design.
Pre-fill company name with [Account].
Submit should trigger email to contact@yallo.co.
Include privacy policy link.
```

---

### STEP 3: UX DIRECTOR QC REVIEW (5 minutes)

**ROLE:** UX Director

**QC Checklist - Landing Page:**
```
[ ] Hero section clear and compelling (headline + description)
[ ] Pain points specific to account (not generic)
[ ] Solution items benefit-focused (not just features)
[ ] Case study relevant to account's scale/industry
[ ] FAQ addresses real objections
[ ] CTAs clear throughout (discovery call)
[ ] Content hierarchy logical (hero → pain → solution → proof → FAQ → CTA)
[ ] Web team has enough detail for implementation
```

**If QC FAILS:** Request revisions from Conversion Copywriter

**If QC PASSES:** Approve and proceed to pitch deck

---

### STEP 4: PITCH DECK CREATION (15-20 minutes)

**ROLE:** Sales Enablement Manager

**Task:** Create 12-slide account-specific pitch deck

**Format:** Slide-by-slide text content (no design, just content)

---

#### PITCH DECK STRUCTURE (12 Slides)

**Slide Flow:**
```
Slides 1-3: PROBLEM (Frame their challenge)
Slides 4-7: SOLUTION (YALLO difference)
Slides 8-9: PROOF (Case study, metrics)
Slide 10: COMMERCIAL (Flexible model)
Slides 11-12: CLOSE (Next steps, contact)
```

---

#### SLIDE 1: COVER

```
TITLE:
YALLO × [ACCOUNT NAME]

SUBTITLE:
Specialist Talent Acceleration for [Location] Tech Hub

VISUAL NOTE:
[YALLO logo + Account logo side by side]

FOOTER:
Confidential – Prepared for [Account Name]
[Date]
```

---

#### SLIDE 2: THE CHALLENGE YOU'RE FACING

```
TITLE:
The Challenge You're Facing

MAIN CONTENT (3-4 bullet points):
• [X]+ specialist roles open across [technologies]
• 10-14 week average time-to-hire in Bengaluru market
• [Programme 1], [Programme 2], [Programme 3] at risk from talent gaps
• Standard sourcing delivers 100+ CVs but only 2-3 with retail domain depth

VISUAL NOTE:
[Timeline graphic showing: Job Posted → 100+ CVs → Screen → 12 weeks later → Hire]

PULL QUOTE (bottom):
"Every week of specialist hiring delay creates programme delivery risk."
```

---

#### SLIDE 3: WHY SPECIALIST HIRING TAKES 12 WEEKS

```
TITLE:
Why Specialist Hiring Takes 12 Weeks

MAIN CONTENT (4-5 points):

The Problem Isn't Finding Engineers—It's Finding the RIGHT Engineers:

• Bengaluru has 500+ [Technology] engineers
  → Only 20 have retail domain depth

• Standard sourcing screens for keywords
  → Misses domain complexity (MDM, seasonal peaks, omnichannel)

• 100+ applications per role
  → 8-10 weeks to screen for retail fit

• Counter-offers and false starts
  → Add 2-4 weeks to timeline

VISUAL NOTE:
[Comparison graphic: Generic Engineer vs Retail Specialist Engineer]
```

---

#### SLIDE 4: THE YALLO DIFFERENCE

```
TITLE:
The YALLO Difference

MAIN CONTENT (3 columns):

COLUMN 1: SPEED
72-Hour Delivery
Brief to shortlist in 3 days
Candidates start same week

COLUMN 2: QUALITY
2:1 CV Ratio
2 candidates max—both vetted
85% pass client interviews

COLUMN 3: DEPTH
Architect-Led Screening
Retail domain validation
15+ years screening experience

VISUAL NOTE:
[3-column layout with icons]

BOTTOM TEXT:
We don't start from scratch—we maintain a pre-screened Bengaluru network.
```

---

#### SLIDE 5: HOW WE WORK

```
TITLE:
How We Work

MAIN CONTENT (4 steps in visual flow):

STEP 1: YOU BRIEF (Day 1)
Share role requirements, tech stack, timeline

STEP 2: WE SCREEN (Day 1-2)
Architect validates candidates from pre-vetted network

STEP 3: YOU DECIDE (Day 3)
Review 2 candidates, conduct interviews

STEP 4: THEY START (Week 1)
We handle contracts, compliance, onboarding

VISUAL NOTE:
[Horizontal timeline or process flow diagram]

BOTTOM TEXT:
From brief to hire in one week—not twelve.
```

---

#### SLIDE 6: WHO SCREENS YOUR CANDIDATES

```
TITLE:
Who Screens Your Candidates

PHOTO:
[Sumeet Goenka headshot]

NAME & TITLE:
Sumeet Goenka
Founder & CEO, YALLO

CREDENTIALS (bullet list):
• Group Chief Architect, Richemont (€20B luxury retail)
• Chief Enterprise Architect, Landmark Group ($6B Middle East retail)
• Led omnichannel transformations at Burberry, Ted Baker
• Hired 1,000+ engineers globally
• 15+ years screening for retail tech roles

PULL QUOTE:
"I screen every candidate from the hiring side—not just the CV. I know what retail domain depth looks like because I've built these teams."

VISUAL NOTE:
[Professional headshot on left, text on right]
```

---

#### SLIDE 7: OUR SPECIALIST NETWORK

```
TITLE:
Our Specialist Network

MAIN CONTENT (technologies covered):

Bengaluru Network Coverage:

• Salesforce Commerce Cloud
  Architects, Senior Engineers (omnichannel, POS, MDM)

• Snowflake & Data Engineering
  Retail analytics, seasonal forecasting, 500K+ SKU MDM

• GenAI & ML Engineering
  LLM deployment, retail use cases, responsible AI

• Performance Engineering
  Chaos engineering, Kubernetes, retail scale (10x peaks)

• Cloud Architecture (AWS/Azure/GCP)
  Retail platform migration, microservices

BOTTOM TEXT:
Pre-screened for retail domain depth—not just tool certifications.

VISUAL NOTE:
[Grid layout or icon-based list]
```

---

#### SLIDE 8: PROOF POINT - CASE STUDY

```
TITLE:
Proven Results: [Similar Company]

COMPANY:
[Company Name] – [Industry], [Scale]

THE CHALLENGE:
• [Technology] platform team needed to scale rapidly
• Traditional hiring taking 10-12 weeks
• Programme milestones at risk

YALLO'S APPROACH:
✓ 72-hour delivery of architect-vetted specialists
✓ Enterprise architecture oversight provided
✓ Rapid onboarding—contributed from day one
✓ Flexible scaling to match programme needs

THE RESULTS:
✓ Delivery timelines met
✓ Robust architecture established
✓ Cost optimized through scalable model
✓ Engagement expanded for subsequent phases

VISUAL NOTE:
[Before/After comparison or timeline graphic]
```

---

#### SLIDE 9: BY THE NUMBERS

```
TITLE:
By the Numbers

MAIN CONTENT (4-6 key stats in large font):

72 HOURS
Brief to shortlist delivery time

2:1
CV ratio (not 20:1)

85%
Candidates pass client technical interviews

90%
Contract completion rate

500+
Pre-screened specialists in Bengaluru network

15+
Years of retail tech hiring experience

VISUAL NOTE:
[Large numbers with labels, clean grid layout]
```

---

#### SLIDE 10: COMMERCIAL MODEL

```
TITLE:
Flexible Commercial Model

INTRO TEXT:
We align with your needs—not force you into rigid contracts.

MAIN CONTENT (3 pricing options):

OPTION 1: PROJECT-BASED
• Pay per successful placement
• No upfront costs
• Industry-standard fee structure
• Best for: Testing the partnership, 1-5 roles

OPTION 2: RETAINER MODEL
• Monthly retainer for dedicated capacity
• Reduced per-placement fees
• Priority access to network
• Best for: Ongoing specialist needs, 5+ roles per quarter

OPTION 3: EXCLUSIVE PARTNERSHIP
• Annual agreement for full specialist capacity
• Volume-based pricing
• Dedicated account management
• Best for: Large-scale transformation programmes

BOTTOM TEXT:
First engagement is always project-based to prove value.

VISUAL NOTE:
[3-column comparison table or cards]
```

---

#### SLIDE 11: NEXT STEPS

```
TITLE:
Next Steps

MAIN CONTENT (3-step process):

STEP 1: DISCOVERY CALL (20 Minutes)
• Share your hiring roadmap and specialist needs
• We assess fit and discuss approach
• No commitment required

STEP 2: PILOT ROLE (1-2 Weeks)
• Give us one hard-to-fill specialist role
• We deliver 2 candidates in 72 hours
• You evaluate quality and fit

STEP 3: PARTNERSHIP DECISION (You Decide)
• If we deliver value, we discuss ongoing partnership
• If not, no hard feelings—we part ways

VISUAL NOTE:
[Horizontal timeline with icons]

CTA:
Ready to start?
[Discovery Call Button with link]
```

---

#### SLIDE 12: CONTACT

```
TITLE:
Let's Discuss Your Specialist Hiring Needs

MAIN CONTENT:

DISCOVERY CALL:
[Discovery call link]
Book 20-30 minutes on our calendar

EMAIL:
contact@yallo.co

WEBSITE:
yallo.co

ACCOUNT-SPECIFIC LANDING PAGE:
go.yallo.co/[account]

VISUAL NOTE:
[YALLO logo, contact details clearly displayed]

FOOTER:
YALLO – Strategy & Talent Unified
Bengaluru · Dubai · London
```

---

### STEP 5: COMMERCIAL DIRECTOR QC REVIEW (5 minutes)

**ROLE:** Commercial Director

**QC Checklist - Pitch Deck:**
```
[ ] Problem framing resonates (Slides 2-3)
[ ] Solution positioning differentiated (Slides 4-7)
[ ] Proof points credible (Slides 8-9)
[ ] Commercial model flexible (Slide 10)
[ ] Next steps clear and low-friction (Slide 11)
[ ] Deck flows logically (problem → solution → proof → commercial → close)
[ ] Can stand alone (no presenter required)
[ ] Account-specific throughout (not template)
```

**If QC FAILS:** Request revisions from Sales Enablement Manager

**If QC PASSES:** Approve and proceed to output generation

---

### STEP 6: OUTPUT GENERATION (5 minutes)

#### OUTPUT 1: Landing Page Content (PDF)

**Format:** PDF document, content-only

**Structure:**
```
PAGE 1: Cover
- Title: "Landing Page Content for [Account]"
- URL: go.yallo.co/[account]
- Date

PAGE 2-3: Hero Section + Pain Points
PAGE 4-5: Why Choose YALLO + Founder
PAGE 6: How It Works
PAGE 7: Case Study
PAGE 8-9: FAQ
PAGE 10: Contact/CTA

APPENDIX: Notes to Web Team
- Design guidance (where applicable)
- CTA links to include
- Image placeholders
```

**Save as:** `/mnt/user-data/outputs/[Account]_Landing_Page_Content.pdf`

**Alternative if PDF not possible:**
Save as Markdown: `/mnt/user-data/outputs/[Account]_Landing_Page_Content.md`

---

#### OUTPUT 2: Pitch Deck PPT

**Format:** PowerPoint or Markdown (slide-by-slide)

**Structure:**
```markdown
# SLIDE 1: COVER
[Content from Slide 1]

---

# SLIDE 2: THE CHALLENGE YOU'RE FACING
[Content from Slide 2]

---

[Continue for all 12 slides]
```

**Save as:** `/mnt/user-data/outputs/[Account]_Pitch_Deck.pptx`

**Alternative if PPT not possible:**
Save as Markdown: `/mnt/user-data/outputs/[Account]_Pitch_Deck.md`

---

### STEP 7: FINAL DELIVERY TO USER (2 minutes)

**Present both outputs:**

```
✅ SKILL 3 COMPLETE - LANDING PAGE & PITCH DECK

I've created 2 deliverables for [Account Name]:

📄 OUTPUT 1: Landing Page Content (PDF)
- 10 pages, content-only for web team
- All 8 sections included (Hero → Contact)
- Account-specific throughout
- File: [Account]_Landing_Page_Content.pdf

📊 OUTPUT 2: Pitch Deck (12 slides)
- Account-specific presentation
- Problem → Solution → Proof → Commercial → Close
- Ready for client meetings
- File: [Account]_Pitch_Deck.pptx

Next Steps:
1. Share landing page content with web team
2. Use pitch deck for client meetings
3. Proceed to Skill 4 (Cold Calling HTML & Contact Excel)

Would you like me to:
- Make any changes to these deliverables?
- Proceed to Skill 4?
```

---

## ⚠️ COMMON PITFALLS TO AVOID

### Landing Page:
❌ Generic pain points ("you need better technology")
❌ Feature lists instead of benefits
❌ Weak CTAs ("Learn More" instead of "Book Discovery Call")
❌ Case study not relevant to account's scale/industry

### Pitch Deck:
❌ Starting with YALLO (should start with their problem)
❌ Too many slides on credentials (keep to 1-2 slides)
❌ Prescriptive commercial model (should be flexible)
❌ No clear next steps (must end with specific action)

---

## 🎯 SUCCESS METRICS

**This skill is successful when:**

1. **Landing page content is actionable:**
   - Web team can implement without asking questions
   - All sections account-specific (not template)
   - Clear conversion flow (hero → pain → solution → proof → CTA)

2. **Pitch deck is presentation-ready:**
   - Flows logically (problem → solution → proof → close)
   - Can stand alone (no presenter notes required)
   - Account-specific throughout

3. **User feedback:**
   - "This is specific to our account"
   - "Web team has everything they need"
   - "I can present this deck as-is"

---

## 📝 QUALITY ASSURANCE LOG

```
[TIMESTAMP] SKILL 3 STARTED

[TIMESTAMP] Landing Page Content Created
- Hero: ✓
- Pain Points: ✓ (account-specific)
- Why YALLO: ✓
- Founder: ✓
- How It Works: ✓
- Case Study: ✓ (relevant to account)
- FAQ: ✓
- Contact: ✓

[TIMESTAMP] UX Director QC Review
✓ All sections reviewed
✓ Conversion flow validated
✓ Content hierarchy clear
→ APPROVED

[TIMESTAMP] Pitch Deck Created
- Slides 1-3 (Problem): ✓
- Slides 4-7 (Solution): ✓
- Slides 8-9 (Proof): ✓
- Slide 10 (Commercial): ✓
- Slides 11-12 (Close): ✓

[TIMESTAMP] Commercial Director QC Review
✓ All 12 slides reviewed
✓ Problem framing resonates
✓ Solution differentiated
✓ Commercial model flexible
→ APPROVED

[TIMESTAMP] Outputs Generated
✓ Landing page PDF created
✓ Pitch deck PPT created

[TIMESTAMP] SKILL 3 COMPLETE
Duration: 42 minutes
Quality: All QC checkpoints passed
```

---

**END OF SKILL 3: LANDING PAGE & PITCH DECK**
