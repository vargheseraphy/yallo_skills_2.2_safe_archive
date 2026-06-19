---
name: abm-research-strategy
description: Generate comprehensive account research, SWOT analysis, and 14-slide ABM strategy document for Gamma PPT generation. Transforms raw account inputs (LinkedIn, website, jobs, contact list) into actionable ABM strategy package.
version: 1.0
triggers:
  - "Start ABM research for {account}"
  - "Create ABM strategy for {account}"
  - "Generate account research and strategy for {account}"
  - "Build ABM plan for {account}"
  - "Research {account} and create strategy document"
---

# ABM Research & Strategy PPT

**Purpose:** Transform raw account inputs into complete ABM strategy package including Research Report, 14-slide Gamma document, and backup PPT.

**Total Outputs:** 3 deliverables  
**Estimated Time:** 45-60 minutes  
**Quality Control:** Research Director + Campaign Director review

---

## 🎯 OVERVIEW

This skill creates:
1. **Research Report** (8-12 page PDF) - Account analysis, pain points, SWOT
2. **ABM Strategy Document** (Markdown for Gamma) - 14 slides ready to import
3. **ABM Strategy PPT** (Backup .pptx) - Same content as Gamma version

---

## 📥 REQUIRED INPUTS

### Mandatory Information:

```yaml
ACCOUNT_BASICS:
  account_name: "Target Corporation"
  industry: "Retail"
  location: "Bengaluru, India"
  
RESEARCH_SOURCES:
  company_linkedin: "linkedin.com/company/target"
  company_website: "corporate.target.com"
  contact_list: [Upload Excel file]
  
CAMPAIGN_PARAMETERS:
  duration_weeks: 8
  primary_goal: "Book 3-5 meetings"
```

### Optional Information:

```yaml
ADDITIONAL_CONTEXT:
  open_jobs: [List of job posting URLs or "None"]
  research_materials: [Upload PPT/PDF or "None"]
  known_pain_points: "Specialist hiring delays, programme delivery risk"
  tech_stack: "Salesforce, Snowflake, AWS, etc."
  key_programmes: "GenAI Platform, Cloud Migration, etc."
```

---

## 👥 TEAM ROLES

### Role 1: Market Intelligence Analyst
**Responsibilities:**
- Analyze company LinkedIn, website, job postings
- Extract pain points and strategic signals
- Map decision makers from contact list
- Identify tech stack and hiring patterns
- Conduct competitive analysis

**Quality Standard:**
- Pain points must be specific (not generic)
- Tech stack validated from multiple sources
- Hiring patterns backed by data (job posting dates, volumes)

---

### Role 2: Research Director (QC Manager)
**Responsibilities:**
- Validate pain point accuracy
- Check data sources and credibility
- Ensure no assumptions without evidence
- Review competitive positioning
- Approve research before strategy phase

**Quality Checklist:**
```
✓ All pain points sourced from real data (jobs, LinkedIn, website)
✓ No generic statements ("they need better technology")
✓ Tech stack confirmed from official sources
✓ Hiring patterns quantified (X roles over Y weeks)
✓ Competitive context researched (not assumed)
```

---

### Role 3: ABM Strategist
**Responsibilities:**
- Design MMQQ framework for account
- Create persona breakdown (5-6 personas)
- Develop engagement strategy (timeline, touchpoints)
- Write messaging templates (LinkedIn, email)
- Conduct SWOT analysis
- Structure 14-slide Gamma document

**Quality Standard:**
- MMQQ framework must identify real people from contact list
- Personas mapped to actual roles (not theoretical)
- Messaging specific to account (not template)
- SWOT analysis actionable (not generic)

---

### Role 4: Campaign Director (QC Manager)
**Responsibilities:**
- Validate strategic coherence
- Check persona-to-message alignment
- Ensure timeline is realistic
- Review SWOT for actionability
- Approve strategy before output generation

**Quality Checklist:**
```
✓ MMQQ framework matches real contacts in list
✓ Personas reflect actual org structure
✓ Messages reference specific account details
✓ Timeline accounts for industry norms (retail tech = slower)
✓ SWOT includes specific threats/opportunities (not generic)
```

---

## 🔄 EXECUTION WORKFLOW

### STEP 1: INPUTS VALIDATION (5 minutes)

**Checklist:**
- [ ] Account name provided
- [ ] Company LinkedIn URL valid
- [ ] Company website accessible
- [ ] Contact list uploaded (Excel/CSV)
- [ ] Campaign duration specified
- [ ] Primary goal defined

**If any mandatory input missing:**
```
STOP and ask user:
"I need [missing input] to proceed. Please provide:
- [List specific missing items]
"
```

---

### STEP 2: ACCOUNT RESEARCH (20-25 minutes)

**ROLE:** Market Intelligence Analyst

#### 2.1 Company LinkedIn Analysis
**Task:** Extract strategic signals from company page

**What to analyze:**
- Employee count and growth trend
- Recent posts (hiring announcements, tech initiatives)
- Locations (GCC presence, expansion signals)
- Specialties listed
- Recent news/announcements

**Output Requirements:**
```
Company Overview:
- Size: [employee count]
- Growth: [% change over 12 months if available]
- GCC Presence: [Bengaluru, Chennai, other cities]
- Key Initiatives: [list 3-5 from recent posts]
```

**Quality Gate:**
❌ AVOID: "Target is a large retailer" (too generic)
✅ GOOD: "Target employs 8,000+ engineers at Bengaluru GCC, up 40% from 2024"

---

#### 2.2 Website Analysis
**Task:** Extract tech stack, programmes, and strategic priorities

**What to analyze:**
- Career page (tech roles, team descriptions)
- Technology/innovation section
- Press releases (tech investments, partnerships)
- About page (strategic priorities)

**Output Requirements:**
```
Tech Stack Identified:
- Platforms: [Salesforce, SAP, etc.]
- Cloud: [AWS, Azure, GCP]
- Data: [Snowflake, Databricks, etc.]
- Languages: [Java, Python, etc.]

Strategic Priorities:
- [Initiative 1: Cloud migration]
- [Initiative 2: GenAI platform]
- [Initiative 3: Omnichannel integration]
```

**Quality Gate:**
❌ AVOID: Listing technologies not confirmed on website
✅ GOOD: "Target careers page lists 12 Salesforce roles + 8 AWS architect roles"

---

#### 2.3 Job Postings Analysis
**Task:** Identify hiring patterns and pain points

**What to analyze:**
- Number of open specialist roles
- How long roles have been posted (if URLs provided)
- Technologies mentioned most frequently
- Seniority levels (IC vs leadership)
- Team names (indicates org structure)

**Output Requirements:**
```
Hiring Patterns:
- Total Open Roles: [number]
- Specialist Roles: [Salesforce: 12, Snowflake: 8, etc.]
- Average Time Posted: [X weeks if data available]
- Seniority Mix: [% IC vs % Leadership]

Pain Points Inferred:
- High volume of [X] roles = scaling challenge
- Long posting duration = specialist scarcity
- Multiple similar roles = backfill or expansion
```

**Quality Gate:**
❌ AVOID: "They need to hire faster" (generic)
✅ GOOD: "15 Salesforce Commerce Cloud roles posted, 8 reposted after 6+ weeks"

---

#### 2.4 Contact List Analysis
**Task:** Map decision makers and org structure

**What to analyze:**
- Total contacts
- Persona breakdown (titles → personas)
- Seniority distribution (VP/Director/Manager/IC)
- Priority contacts (India mobile, email verified)
- Department structure (engineering, TA, programme management)

**Output Requirements:**
```
Contact Landscape:
- Total Contacts: [number]
- By Persona:
  - P1 (SVP/VP): [count]
  - P2 (Sr Directors): [count]
  - P3 (Directors/Managers): [count]
  - P4 (TA/HR): [count]
  - P6 (TPM/PM): [count]

Priority Segments:
- India Mobile Verified: [count]
- Email Verified: [count]
- High Priority (P1-P2): [count]
```

**Quality Gate:**
✓ Contact counts match uploaded Excel
✓ Personas assigned based on titles (not guessed)

---

#### 2.5 Competitive Analysis
**Task:** Identify other vendors, incumbent suppliers, competitive threats

**What to research:**
- LinkedIn: Who else is engaging their employees?
- Website careers: Any staffing partners mentioned?
- Industry knowledge: Standard suppliers for this sector

**Output Requirements:**
```
Competitive Context:
- Incumbent Suppliers: [Known PSL vendors if any]
- Competing GCCs: [Other retail tech GCCs in same city]
- Internal TA: [Evidence of in-house recruiting team]
- Recent Vendor Activity: [Any LinkedIn signals]

YALLO Positioning:
- White Space: [Where YALLO fits uniquely]
- Competitive Advantage: [Why YALLO vs incumbents]
```

**Quality Gate:**
❌ AVOID: Assuming competitors without evidence
✅ GOOD: "No incumbent supplier signals found. Internal TA team active on LinkedIn."

---

### STEP 3: RESEARCH DIRECTOR QC REVIEW (5 minutes)

**ROLE:** Research Director

**QC Checklist:**
```
Company Overview:
[ ] Employee count verified from LinkedIn
[ ] GCC locations confirmed
[ ] Recent initiatives cited from real sources

Tech Stack:
[ ] All technologies confirmed from website/jobs
[ ] No assumptions about tech without evidence
[ ] Stack relevant to YALLO services (specialist roles)

Hiring Patterns:
[ ] Open role counts accurate
[ ] Posting duration verified where possible
[ ] Pain points specific (not "they need help")

Contact Analysis:
[ ] Persona counts match Excel
[ ] Priority contacts identified correctly
[ ] Decision makers clearly mapped

Competitive Context:
[ ] Competitor claims backed by evidence
[ ] No unfounded assumptions
[ ] YALLO positioning realistic
```

**If QC FAILS:**
```
STOP. Research Director flags issues:
"Research needs refinement:
- [Specific issue 1]
- [Specific issue 2]

Market Intelligence Analyst: Please address these before proceeding to strategy."
```

**If QC PASSES:**
```
Research Director approves:
"Research validated. Proceeding to strategy development."
```

---

### STEP 4: SWOT ANALYSIS (10 minutes)

**ROLE:** ABM Strategist

**Task:** Conduct account-specific SWOT analysis

#### 4.1 STRENGTHS (Internal to Account)
**Question:** What makes this account attractive for YALLO?

**Analyze:**
- Large GCC investment (budget signal)
- Active hiring (immediate need)
- Tech-first culture (values specialist depth)
- Specific pain points identified
- Decision makers accessible

**Output Format:**
```
STRENGTHS:
• Large GCC investment ($[X]M if known, or "[Y]+ employees")
• Active specialist hiring (15+ Salesforce, 8+ Snowflake roles open)
• Tech-first culture (proven by tech stack sophistication)
• Budget allocated (evident from job postings volume)
• Accessible decision makers ([X] contacts in list)
```

**Quality Gate:**
✅ Each strength backed by research data
✅ Strengths specific to THIS account (not generic)

---

#### 4.2 WEAKNESSES (Internal to Account)
**Question:** What makes this account challenging for YALLO?

**Analyze:**
- No existing supplier relationship with YALLO
- Long sales cycles (retail industry norms)
- Possible incumbent vendors
- Complex org structure (many decision makers)
- Budget timing (fiscal year cycles)

**Output Format:**
```
WEAKNESSES:
• No existing relationship with YALLO (cold account)
• Long enterprise sales cycle (retail = 3-6 months typical)
• [X] incumbent suppliers identified OR no supplier signals = must build from scratch
• Complex decision structure ([Y] decision makers across [Z] departments)
• Fiscal year timing ([if relevant, e.g., "Q4 budget freeze likely"])
```

**Quality Gate:**
✅ Weaknesses realistic (not pessimistic or optimistic)
✅ Based on research (not assumptions)

---

#### 4.3 OPPORTUNITIES (External to Account)
**Question:** What external factors create opportunity for YALLO?

**Analyze:**
- Market conditions (specialist scarcity in Bengaluru)
- Industry trends (GCC expansion, tech transformation)
- Timing (programme delivery pressure)
- Competitive gaps (no YALLO at competitor)
- Regulatory/economic factors (if relevant)

**Output Format:**
```
OPPORTUNITIES:
• Specialist hiring pain (10-12 week average in Bengaluru market)
• Programme delivery risk (GenAI/Cloud initiatives at risk from talent gaps)
• GCC expansion trend (Chennai launch signals continued growth)
• YALLO not engaged by competitors ([Walmart/Target/etc.] not using YALLO)
• [Any other external opportunity specific to account/industry]
```

**Quality Gate:**
✅ Opportunities external (not internal strengths)
✅ Tied to market/industry context (not just account)

---

#### 4.4 THREATS (External to Account)
**Question:** What external factors could block YALLO?

**Analyze:**
- Incumbent vendor lock-in
- Economic headwinds (budget cuts)
- Internal TA preference (build vs buy)
- Competitor activity (other specialist firms)
- Timing risks (fiscal year, hiring freezes)

**Output Format:**
```
THREATS:
• Incumbent vendors (if identified: [names]; if not: "No signals, but PSL likely exists")
• Budget freeze risk (fiscal year end Q4, timing matters)
• Internal TA preference (TA team may resist external help)
• Competitor activity ([other specialist firms if known])
• Timing sensitivity (programme milestones in [Q/month] = urgency OR slow period)
```

**Quality Gate:**
✅ Threats external (not internal weaknesses)
✅ Realistic (not paranoid)
✅ Actionable (can be mitigated)

---

#### 4.5 Strategic Approach (Based on SWOT)

**Task:** Synthesize SWOT into approach strategy

**Output Format:**
```
APPROACH STRATEGY:

Direct vs Indirect:
[Based on SWOT, recommend]
- Direct: Engage decision makers (VPs/Directors) immediately
OR
- Indirect: Build through TA/champions first, earn way to leadership

Persona Priority:
[Based on SWOT, recommend]
1. [Persona X] - Why: [reason from SWOT]
2. [Persona Y] - Why: [reason from SWOT]
3. [Persona Z] - Why: [reason from SWOT]

Timing Considerations:
[Based on SWOT threats/opportunities]
- Best time to engage: [Q/month + reason]
- Avoid: [timing to avoid + reason]
- Urgency drivers: [what creates urgency]

Partnership Positioning:
[Based on SWOT strengths/weaknesses]
- Angle: [How to position YALLO]
  Example: "Overlay on existing TA, not replacement"
  Example: "Specialist capacity for hard-to-fill roles only"
```

**Quality Gate:**
✅ Strategy directly derived from SWOT
✅ Specific recommendations (not "it depends")
✅ Actionable (clear next steps)

---

### STEP 5: ABM STRATEGY DOCUMENT - 14 SLIDES (15-20 minutes)

**ROLE:** ABM Strategist

**Task:** Create 14-slide strategy document in Gamma-compatible Markdown format

**Format:** Markdown with `#` headers for slides

---

#### SLIDE 1: Cover

```markdown
# Account Strategy: [Account Name]
[LOCATION] STRATEGIC ENTRY

[Your Name]

Enterprise ABM Plan – Retail Technology Focus
```

---

#### SLIDE 2: About [Account]

```markdown
## About [Account Name]

[Stat 1 Value]
[Stat 1 Label]

[Stat 2 Value]
[Stat 2 Label]

[Stat 3 Value]
[Stat 3 Label]

[Opening paragraph - 3-4 sentences about the company, industry position, strategic focus]

[Second paragraph - 2-3 sentences about their tech hub, GCC location, team size, technology priorities]

[Third paragraph - 2 sentences about why they're tech-first, not traditional]
```

**Example:**
```markdown
## About Walmart Global Tech India

25,000+
Employees in India GCC

Global Hub
Bengaluru + Chennai presence

Tech-First
Omnichannel and GenAI focus

Walmart Global Tech India is a Fortune 1 retail technology powerhouse operating at the intersection of e-commerce innovation and enterprise-scale engineering. With over 25,000 employees across Bengaluru and Chennai, the company has established itself as a leader in retail technology infrastructure.

The India GCC represents a strategic investment in retail technology capabilities, with significant focus on GenAI platforms, cloud architecture, and data engineering. This positions Walmart as a tech-enabled retail enterprise rather than a traditional brick-and-mortar operator.

The technology organization demonstrates maturity through sophisticated tooling, platform engineering teams, and architect-led delivery models—making it a prime candidate for specialist talent partnerships.
```

---

#### SLIDE 3: Strategic Signals Identified

```markdown
## Strategic Signals Identified

[Opening paragraph explaining what signals indicate about account phase - 2-3 sentences]

[Second paragraph on why these signals matter - 2-3 sentences]

[Signal 1 Title]
[1-2 sentences explaining the signal and evidence]

[Signal 2 Title]
[1-2 sentences explaining the signal and evidence]

[Signal 3 Title]
[1-2 sentences explaining the signal and evidence]

[Signal 4 Title]
[1-2 sentences explaining the signal and evidence]

Why This Matters
[2-3 sentences on why these signals indicate readiness for YALLO]
```

---

#### SLIDE 4: Account Objectives

```markdown
## Account Objectives

[Opening paragraph - 2-3 sentences on engagement philosophy]

01
[Objective 1 Title]
[1-2 sentences describing objective and approach]

02
[Objective 2 Title]
[1-2 sentences describing objective and approach]

03
[Objective 3 Title]
[1-2 sentences describing objective and approach]

04
[Objective 4 Title]
[1-2 sentences describing objective and approach]
```

**Standard Objectives:**
```markdown
01
Map Technology Buying Structure
Identify complete stakeholder landscape across decision-making and influence layers

02
Establish Multi-Thread Relationships
Build connections across functional areas and organizational levels

03
Navigate From Execution to Strategy
Enter through tactical layer and earn credibility to reach strategic conversations

04
Secure Strategic Discovery Call
Book qualified meeting with decision-maker within 30–45 days
```

---

#### SLIDE 5: MMQQ Framework

```markdown
## MMQQ Framework: Account Penetration Model

[Opening paragraph - 2-3 sentences explaining MMQQ]

Money: Budget Owners
[2-3 sentences describing who controls financial resources]
From contact list:
• [Name + Title]
• [Name + Title]
• [Name + Title]

Metrics: Business KPI Owners
[2-3 sentences describing who measures outcomes]
From contact list:
• [Name + Title]
• [Name + Title]

Quantified Pain: Challenge Owners
[2-3 sentences describing who feels daily operational pain]
From contact list:
• [Name + Title]
• [Name + Title]

Qualified Champion: Internal Advocate
[2-3 sentences describing who can champion YALLO internally]
From contact list:
• [Name + Title]
• [Name + Title]
```

---

#### SLIDE 6: Target Personas

```markdown
## Target Personas

[Opening paragraph - 2 sentences on persona breakdown]

1
[Persona Name]
[1-2 sentences describing role, authority, engagement approach]

2
[Persona Name]
[1-2 sentences describing role, authority, engagement approach]

3
[Persona Name]
[1-2 sentences describing role, authority, engagement approach]

4
[Persona Name]
[1-2 sentences describing role, authority, engagement approach]

5
[Persona Name]
[1-2 sentences describing role, authority, engagement approach]
```

---

#### SLIDE 7: Engagement Strategy

```markdown
## Engagement Strategy: Multi-Touch Model

[Opening paragraph - 2-3 sentences on 30-45 day approach]

Critical principle: No hard selling before the fourth touchpoint. Early interactions focus exclusively on insight sharing and professional connection.

Touch 1
LinkedIn connection request with personalized, value-focused note

Touch 2
Insight-based follow-up message addressing their specific challenges

Touch 3
Contextual email with no sales pitch, pure value delivery

Touch 4
Social engagement through thoughtful comments and reactions

Touch 5
Value-driven email sharing relevant industry insights or case studies

Touch 6
Direct meeting request positioned as idea exchange, not sales call
```

---

#### SLIDE 8: LinkedIn Connection Message

```markdown
## LinkedIn Connection Message

Hi [Name],

I've been following [Account]'s tech expansion in [Location]. I'm impressed with how the [specific team/programme] is scaling [specific technology]. Would love to connect and exchange insights.

– [Your Name]

Message Characteristics

Professional and respectful tone
Demonstrates awareness of their work
No sales pitch or agenda
Positioned as peer-to-peer connection
Short and scannable

Expected Outcome

Connection acceptance rate of 30–50% when properly personalized. The goal is simply to establish initial contact and earn the right to continue the conversation.
```

---

#### SLIDE 9: LinkedIn Follow-Up Message

```markdown
## LinkedIn Follow-Up Message

Send this message 2–3 days after connection acceptance. The follow-up continues building credibility by acknowledging their specific challenges.

Position yourself as knowledgeable peer, not vendor. Focus on their challenges, not your solutions.

Hi [Name],

Noticed your team is scaling [specific technologies]. Many retail enterprises are currently facing [specific challenge] at this stage.

We've been analyzing similar transformation patterns—happy to share insights if useful.

No rush—just opening dialogue.

Key Principle

Timing matters: Wait at least 48 hours after connection acceptance.
```

---

#### SLIDE 10: Strategic Email Approach

```markdown
## Strategic Email Approach

[Opening paragraph - 2-3 sentences on email philosophy]

Every email should pass the "so what?" test from the recipient's perspective.

01
Context: Show Relevance
Demonstrate specific knowledge of their business, team, or initiatives

02
Industry Challenge: Not About You
Frame the problem space without making it about YALLO's solution

03
Micro-Proof: One Metric
Share a single, credible data point that demonstrates understanding

04
Soft CTA: Idea Exchange
Position meeting as mutual learning, not sales opportunity
```

---

#### SLIDE 11: Email Template Example

```markdown
## Email Template Example

Subject: [Specific Technology] Scalability at [Account]

Hi [Name],

I noticed [Account] is expanding retail tech capabilities in [Location], particularly around [specific technologies from job postings].

At this scale, many retailers encounter [specific challenge identified from research] across [specific context].

In similar enterprise environments, we helped reduce [specific metric] by [percentage] and improved [specific outcome].

Would you be open to a brief 15-minute discussion to exchange perspectives?

Best,
[Your Name]

78 words – Scannable in 20 seconds
References exact tech stack
Metric provided before ask
15 minutes feels achievable
```

---

#### SLIDE 12: SWOT Analysis

```markdown
## SWOT Analysis

This analysis identifies the strategic factors that will shape our approach to [Account Name].

STRENGTHS | WEAKNESSES
• [Strength 1] | • [Weakness 1]
• [Strength 2] | • [Weakness 2]
• [Strength 3] | • [Weakness 3]
• [Strength 4] | • [Weakness 4]

OPPORTUNITIES | THREATS
• [Opportunity 1] | • [Threat 1]
• [Opportunity 2] | • [Threat 2]
• [Opportunity 3] | • [Threat 3]
• [Opportunity 4] | • [Threat 4]

Strategic Approach

Direct vs Indirect:
[Recommendation with reasoning]

Persona Priority:
1. [Persona] - [Reason]
2. [Persona] - [Reason]
3. [Persona] - [Reason]

Timing Considerations:
[Best time to engage + timing to avoid]

Partnership Positioning:
[How to position YALLO to this account]
```

---

#### SLIDE 13: Touchpoint Timeline

```markdown
## Touchpoint Timeline

Consistency trumps volume in enterprise ABM. This four-week cadence balances persistence with professionalism.

Week 1: Initial Connection
• Send 10-15 LinkedIn connection requests
• Target conversion: 3-5 acceptances
• Research each contact's background
• Prepare personalized follow-up notes

Week 2: Value Delivery
• Send insight-based LinkedIn follow-ups
• Send first contextual email to high-priority contacts
• Begin social listening for engagement opportunities

Week 3: Engagement Building
• Engage thoughtfully with their content
• Send second value email with industry insights
• Share relevant content they might find useful

Week 4: Meeting Request
• Direct meeting ask to engaged prospects
• Position as idea exchange, not sales call
• Offer flexible timing options
```

---

#### SLIDE 14: Key Message Themes

```markdown
## Key Message Themes

Messaging must resonate with the specific challenges and priorities of retail technology leaders at [Account].

[Theme 1 Title]
[1-2 sentences on this theme and why it resonates]

[Theme 2 Title]
[1-2 sentences on this theme and why it resonates]

[Theme 3 Title]
[1-2 sentences on this theme and why it resonates]

[Theme 4 Title]
[1-2 sentences on this theme and why it resonates]

[Theme 5 Title]
[1-2 sentences on this theme and why it resonates]

[Theme 6 Title]
[1-2 sentences on this theme and why it resonates]

These themes can be used for blog posts, newsletters, LinkedIn messages, and email content
```

---

### STEP 6: CAMPAIGN DIRECTOR QC REVIEW (5 minutes)

**ROLE:** Campaign Director

**QC Checklist:**
```
[ ] All 14 slides present and complete
[ ] Content account-specific throughout
[ ] MMQQ includes real names from contact list
[ ] Messages reference specific account details
[ ] SWOT strategic approach actionable
[ ] Timeline realistic for industry
[ ] Format ready for Gamma import
```

**If QC FAILS:** Stop and request refinements

**If QC PASSES:** Proceed to output generation

---

### STEP 7: OUTPUT GENERATION (10 minutes)

#### OUTPUT 1: Research Report (PDF)

**Format:** 8-12 page PDF

**Structure:**
```
PAGE 1: Cover
PAGE 2: Executive Summary
PAGE 3-4: Company Analysis
PAGE 5-6: Hiring Patterns & Pain Points
PAGE 7: Contact Landscape
PAGE 8: Competitive Context
PAGE 9: SWOT Analysis
PAGE 10-12: Appendices
```

Save as: `/mnt/user-data/outputs/[Account]_Research_Report.md`

---

#### OUTPUT 2: ABM Strategy Document (Markdown for Gamma)

**Format:** Markdown file with `#` headers for slides

**File Structure:**
```markdown
# Account Strategy: [Account Name]
[LOCATION] STRATEGIC ENTRY

[Your Name]
Enterprise ABM Plan – Retail Technology Focus

---

# About [Account Name]
[Content from Slide 2]

---

[Continue for all 14 slides]
```

Save as: `/mnt/user-data/outputs/[Account]_ABM_Strategy_Gamma.md`

Include note at top:
```
GAMMA IMPORT INSTRUCTIONS:
1. Copy entire content below
2. Paste into Gamma
3. Each # header becomes a new slide
4. Format will auto-apply based on Gamma's theme
```

---

#### OUTPUT 3: ABM Strategy PPT (Backup)

Same content as Gamma version with clear slide breaks.

Save as: `/mnt/user-data/outputs/[Account]_ABM_Strategy_Backup.md`

---

### STEP 8: FINAL DELIVERY TO USER (2 minutes)

**Present all outputs:**

```
✅ SKILL 1 COMPLETE - ABM RESEARCH & STRATEGY

I've created 3 deliverables for [Account Name]:

📄 OUTPUT 1: Research Report
- 12 pages, complete account analysis, SWOT included

📄 OUTPUT 2: ABM Strategy Document (Gamma Format)
- 14 slides in Markdown, ready to paste into Gamma

📄 OUTPUT 3: ABM Strategy PPT (Backup)
- Same content as Gamma version

Next Steps:
1. Review the Gamma document
2. Import into Gamma to generate PPT
3. Share with team for approval
4. Proceed to Skill 2 (Email, LinkedIn, Newsletter Sequences)
```

---

## ⚠️ COMMON PITFALLS TO AVOID

### Research Phase:
❌ Assuming tech stack without verification
❌ Generic pain points ("they need to hire faster")
❌ Over-relying on single source

### Strategy Phase:
❌ Template messaging
❌ MMQQ without real names
❌ Unrealistic timelines

### SWOT Analysis:
❌ Generic SWOT points
❌ Confusing strengths/opportunities
❌ Non-actionable strategy

---

## 🎯 SUCCESS METRICS

**This skill is successful when:**

1. Research is validated (all pain points backed by evidence)
2. Strategy is actionable (MMQQ maps to real contacts)
3. Outputs are usable (Gamma imports cleanly)
4. User feedback: "This is specific to our account"

---

## 📝 INCREMENTAL APPROVAL (If Needed)

```
CHECKPOINT 1: After Research (Step 3)
→ Present research findings → User approves → Proceed to SWOT

CHECKPOINT 2: After SWOT (Step 4)
→ Present SWOT analysis → User approves → Proceed to slides

CHECKPOINT 3: After Slide Draft (Step 5)
→ Present first 7 slides → User approves → Complete remaining slides

CHECKPOINT 4: Final Review (Step 6)
→ Present all 14 slides → User approves → Generate outputs
```

---

**END OF SKILL 1: ABM RESEARCH & STRATEGY**
