---
name: abm-cold-call-contact-enrichment
description: Generate cold calling HTML cheat sheet (matching existing YALLO format) and enriched contact Excel for calling team. HTML includes 5 persona scripts (OPTIC framework), objection handling, right panel tools. Excel enrichment uses Apollo for missing contacts, phone numbers, job changes, and priority scoring.
version: 1.0
triggers:
  - "Create cold call assets for {account}"
  - "Generate calling cheat sheet for {account}"
  - "Build cold call HTML and contact list for {account}"
  - "Create calling assets for {account}"
  - "Generate call scripts and contact Excel for {account}"
---

# ABM Cold Call & Contact Enrichment

**Purpose:** Create cold calling HTML cheat sheet and enriched contact Excel for calling team with Apollo integration.

**Total Outputs:** 2 deliverables  
**Estimated Time:** 40-50 minutes  
**Quality Control:** Sales Director + Data Director

---

## 🎯 OVERVIEW

This skill creates:
1. **Cold Calling HTML Cheat Sheet** - Single-file HTML matching existing YALLO format
2. **Enriched Contact Excel** - Apollo-integrated contact list with phone numbers, priority scoring

**HTML Format:** Matches your existing Walmart cold call prompt exactly (dark theme, persona scripts, OPTIC framework, right panel tools)

---

## 📥 REQUIRED INPUTS

### Mandatory Information:

```yaml
FROM_SKILL_1:
  abm_strategy_document: [Output from Skill 1]
  account_name: "Walmart Global Tech India"
  swot_analysis: [From Skill 1]
  personas_identified: [P1, P2, P3, P4, P6]
  pain_points: [From research]
  key_programmes: [From research]

ACCOUNT_DETAILS:
  account_accent_color: "#0071CE" (e.g., Walmart blue)
  gcc_location: "Bengaluru + Chennai"
  gcc_size: "25,000+ engineers"
  revenue: "$681B"
  fortune_rank: "Fortune #1" (if applicable)
  open_roles_count: "250+"
  hardest_fill_time: "12-16 weeks"
  live_programmes: ["GenAI Platform", "Payments Tech", "Supply Chain"]
  hardest_roles: ["Principal ML Engineer", "Payments Architect", "Data Platform Lead"]

CONTACT_DATA:
  contact_list: [Upload Excel file]
  
CAMPAIGN_LINKS:
  landing_page_url: "go.yallo.co/walmart"
  discovery_call_link: "https://app.apollo.io/#/meet/9uh-bms-x75/30-min"
  senior_peer_call_link: "https://calendly.com/sumeet-goenka/30min"
```

### Optional Information:

```yaml
ADDITIONAL_CONTEXT:
  canva_embed_code: [If you have open roles deck]
  contact_list_sharepoint_url: [If contact tracker in SharePoint/OneDrive]
  specific_hot_signals: [Any specific contacts to highlight]
```

---

## 👥 TEAM ROLES

### Role 1: Sales Development Coach
**Responsibilities:**
- Write cold call scripts for all 5 personas (OPTIC framework)
- Create objection handling responses
- Write gatekeeper scripts (P1, P2 only)
- Ensure scripts are conversational (not robotic)
- Account-specific throughout (not template)

**Quality Standard:**
- Scripts match OPTIC framework exactly (O-P-T-I-C)
- No buzzwords or jargon
- Conversational tone (how people actually talk)
- Account details in every script (programmes, roles, pain points)
- Objections address real concerns (not generic)

---

### Role 2: Sales Director (QC Manager)
**Responsibilities:**
- Review all call scripts for natural flow
- Validate objection handling
- Check OPTIC framework adherence
- Ensure account-specificity
- Approve HTML before generation

**Quality Checklist:**
```
✓ All 5 personas have complete OPTIC scripts
✓ Scripts conversational (not salesy/robotic)
✓ Account details specific (programmes, roles, tech stack)
✓ Objection handling addresses real concerns
✓ Gatekeeper scripts included (P1, P2)
✓ No buzzwords or jargon
```

---

### Role 3: Data Operations Specialist
**Responsibilities:**
- Analyze uploaded contact list
- Identify enrichment needs (missing contacts, phone numbers)
- Structure Excel for calling team (Walmart format)
- Add priority scoring logic
- Create "Why Call" reasoning per contact

**Quality Standard:**
- All contacts assigned to personas
- Priority scoring clear (1-5 or High/Medium/Low)
- Phone numbers formatted correctly (India mobile vs HQ)
- Email verification status included
- Apollo sequence status tracked
- "Why Call" specific to each contact's role

---

### Role 4: Data Director (QC Manager)
**Responsibilities:**
- Validate contact enrichment accuracy
- Check Excel format matches Walmart structure
- Ensure priority scoring is logical
- Review "Why Call" reasoning
- Approve Excel before delivery

**Quality Checklist:**
```
✓ All contacts have persona assignments
✓ Priority scoring logical and consistent
✓ Phone numbers formatted correctly
✓ Email verification status accurate
✓ "Why Call" specific (not generic)
✓ Excel matches Walmart calling list format
✓ Summary dashboard accurate (totals, counts)
```

---

## 🔄 EXECUTION WORKFLOW

### STEP 1: INPUTS VALIDATION (5 minutes)

**Checklist:**
- [ ] ABM Strategy Document from Skill 1 available
- [ ] Account name confirmed
- [ ] Account accent color provided (hex code)
- [ ] GCC stats available (size, revenue, programmes, etc.)
- [ ] Contact list uploaded (Excel)
- [ ] Discovery call link confirmed
- [ ] Landing page URL confirmed

**If any mandatory input missing:**
```
STOP and ask user:
"I need the following to proceed:
- [List specific missing items]

For the cold call HTML, I need:
- Account accent color (hex code like #0071CE)
- GCC stats (size, revenue, open roles, programmes)

For contact enrichment, I need:
- Contact list Excel file
"
```

---

### STEP 2: COLD CALLING HTML GENERATION (25-30 minutes)

**ROLE:** Sales Development Coach + Sales Director

**Task:** Generate single-file HTML matching existing YALLO format

**Reference Format:** Your Walmart cold call prompt structure

---

#### 2.1 HTML STRUCTURE OVERVIEW

```
┌─────────────────────────────────────────────────┐
│  STICKY HEADER (full width)                     │
├──────────┬──────────────────────────┬───────────┤
│          │                          │           │
│ SIDEBAR  │   MAIN CONTENT           │   RIGHT   │
│ 200px    │   (scrollable)           │   PANEL   │
│ (sticky) │                          │   260px   │
│          │                          │ (sticky)  │
├──────────┴──────────────────────────┴───────────┤
│  EMBEDDED RESOURCES (full width)                │
└─────────────────────────────────────────────────┘
```

**Key Components:**
1. **Header** - Account name, stats, landing page URL
2. **Left Sidebar** - 5 persona tabs + OPTIC reminder
3. **Main Content** - Persona scripts (OPTIC framework)
4. **Right Panel** - Golden rules, tips, mood selector, ChatGPT prompt
5. **Footer** - Links and notes

---

#### 2.2 BRAND COLORS (Use These)

```css
/* Page colors */
--page-bg: #0A0A0A;
--dark-surface: #141414;
--card: #1C1C1C;
--card-raised: #242424;
--border: #2E2E2E;

/* Text colors */
--body-text: #F5F5F0;
--grey: #888880;
--light: #CCCCCC;

/* Brand colors */
--yallo-gold: #D6B24C;
--account-accent: [ACCOUNT_ACCENT_COLOR]; /* e.g., #0071CE for Walmart */

/* Status colors */
--red-bg: #2A0A0A;
--red-border: #8B1A1A;
--red-text: #FF6B6B;
--green-bg: #0A1F0A;
--green-border: #1A5C1A;
--green-text: #4CAF50;
--amber-bg: #1F1500;
--amber-border: #6B4A00;
--amber-text: #D6B24C;

/* Persona colors */
--p1-color: #D6B24C; /* Gold - SVP/VP */
--p2-color: #4FC3F7; /* Sky blue - Sr Directors */
--p3-color: #81C784; /* Green - Directors */
--p4-color: #FF8A65; /* Coral - TA/Recruiters */
--p6-color: #CE93D8; /* Lavender - TPM/PM */
```

**Fonts:**
- Headers: `Syne` (from Google Fonts)
- Body: `DM Sans` (from Google Fonts)
- Code/Stats: `DM Mono` (from Google Fonts)

---

#### 2.3 HEADER SECTION

```html
<!-- STICKY HEADER -->
<header>
  <div class="header-row-1">
    <div class="left">
      <span class="yallo-badge">YALLO</span>
      <span class="separator">×</span>
      <span class="account-badge" style="background: [ACCOUNT_ACCENT_COLOR]">
        [ACCOUNT NAME]
      </span>
    </div>
    
    <div class="center">
      <span class="stat-chip">[GCC SIZE]</span>
      <span class="stat-chip">[REVENUE]</span>
      <span class="stat-chip">[OPEN ROLES] open</span>
      <span class="stat-chip">[FILL TIME] specialist fill</span>
      <span class="stat-chip">[PROGRAMME COUNT] programmes</span>
    </div>
    
    <div class="right">
      <span class="goal">🎯 GOAL: Book a 20-min discovery meeting</span>
    </div>
  </div>
  
  <div class="header-row-2">
    <span>[PROGRAMME 1]</span> |
    <span>[PROGRAMME 2]</span> |
    <span>[HARDEST ROLES]</span> |
    <span>[LANDING PAGE URL]</span> |
    <span>Alshaya: 72hr Azure delivery</span>
  </div>
</header>
```

---

#### 2.4 LEFT SIDEBAR - PERSONA TABS

```html
<!-- SIDEBAR -->
<aside class="sidebar">
  <!-- 5 PERSONA TABS -->
  
  <!-- Tab 1: P1 -->
  <button class="tab-btn active" onclick="switchTab('p1')" 
          style="--tab-color: var(--p1-color)">
    <div class="tab-stripe"></div>
    <div class="tab-content">
      <div class="tab-emoji">👔</div>
      <div class="tab-code">P1</div>
      <div class="tab-name">SVP / VP</div>
      <div class="tab-subtitle">Budget Owners</div>
    </div>
  </button>
  
  <!-- Tab 2: P2 -->
  <button class="tab-btn" onclick="switchTab('p2')" 
          style="--tab-color: var(--p2-color)">
    <div class="tab-stripe"></div>
    <div class="tab-content">
      <div class="tab-emoji">⚙️</div>
      <div class="tab-code">P2</div>
      <div class="tab-name">Sr Directors</div>
      <div class="tab-subtitle">Technical Authority</div>
    </div>
  </button>
  
  <!-- Repeat for P3, P4, P6 -->
  
  <div class="divider"></div>
  
  <!-- OPTIC REMINDER CARD -->
  <div class="optic-card">
    <div class="optic-title">OPTIC Framework</div>
    <div class="optic-items">
      <div><strong>O</strong> Open - Warm reference, 2 sentences max</div>
      <div><strong>P</strong> Pain - One qualifying question, wait</div>
      <div><strong>T</strong> Tension - SPIN implication, only if pain confirmed</div>
      <div><strong>I</strong> Intro - 3 sentences on YALLO, after pain only</div>
      <div><strong>C</strong> Close - Book meeting + confirm email + get a name</div>
    </div>
  </div>
</aside>
```

---

#### 2.5 MAIN CONTENT - PERSONA SCRIPTS

**For Each Persona (P1-P6), include:**

```html
<!-- TAB PANEL: P1 -->
<div id="p1" class="tab-panel active" style="--accent-color: var(--p1-color)">
  
  <!-- 1. TAB ACCENT BAR -->
  <div class="tab-accent-bar">
    <span class="persona-code">P1 · SVP / VP</span>
    <span class="persona-name">Budget Owners — Programme ROI</span>
    <span class="call-goal">Book a 20-min discovery meeting</span>
  </div>
  
  <!-- 2. QUICK REFERENCE CARD (TOP) -->
  <div class="qrc">
    <div class="qrc-title">⚡ QUICK REFERENCE — P1 · Read this before every call</div>
    <div class="qrc-grid">
      <div class="qrc-col">
        <div class="qrc-label">OPEN</div>
        <div class="qrc-value">"Is now okay for two minutes?"</div>
      </div>
      <div class="qrc-col">
        <div class="qrc-label">PAIN Q</div>
        <div class="qrc-value">"Any specialist roles open 10+ weeks?"</div>
      </div>
      <div class="qrc-col">
        <div class="qrc-label">TENSION Q</div>
        <div class="qrc-value">"If that stays open 6 more weeks, what happens?"</div>
      </div>
      <div class="qrc-col">
        <div class="qrc-label">KEY PHRASE</div>
        <div class="qrc-value">"We work alongside your suppliers"</div>
      </div>
      <div class="qrc-col">
        <div class="qrc-label">CLOSE</div>
        <div class="qrc-value">"20-min meeting this week?"</div>
      </div>
    </div>
  </div>
  
  <!-- 3. BOOKING ROW -->
  <div class="booking-row">
    <div class="booking-card">
      <div class="booking-title">Discovery Call</div>
      <div class="booking-desc">Talent & Operations Lead — specialist hiring overview</div>
      <div class="booking-link">[DISCOVERY_CALL_LINK]</div>
      <button class="btn-gold">Book 30-min ↗</button>
    </div>
    <div class="booking-card">
      <div class="booking-title">Senior Peer Call</div>
      <div class="booking-desc">For VP/SVP level — peer discussion with YALLO leadership</div>
      <div class="booking-link">[SENIOR_PEER_CALL_LINK]</div>
      <button class="btn-gold">Book 30-min ↗</button>
    </div>
  </div>
  
  <!-- 4. PERSONA CARD (3-column) -->
  <div class="persona-card">
    <div class="persona-col">
      <div class="persona-col-title">Who They Are</div>
      <div class="persona-col-content">
        [List specific names from contact list for P1]
      </div>
    </div>
    <div class="persona-col">
      <div class="persona-col-title">What They Care About</div>
      <div class="persona-col-content">
        Programme delivery, ROI, GCC scaling, budget efficiency
      </div>
    </div>
    <div class="persona-col">
      <div class="persona-col-title">Pain YALLO Solves</div>
      <div class="persona-col-content">
        10-14 week specialist hiring delays creating programme delivery risk
      </div>
    </div>
  </div>
  <div class="risk-warning">
    ⚠️ RISK: Never pitch features before pain is confirmed. Never ask for more than 20 minutes.
  </div>
  
  <!-- 5. GATEKEEPER SCRIPT (P1, P2 only) -->
  <div class="gatekeeper-section">
    <div class="gatekeeper-title">Gatekeeper Script</div>
    
    <div class="gatekeeper-scenario">
      <div class="scenario-title">Someone else answers</div>
      <div class="scenario-script">
        "Hi, this is [Your Name] from YALLO. I'm trying to reach [VP Name] about specialist tech hiring for [Account]. Is [VP Name] available?"
      </div>
    </div>
    
    <div class="gatekeeper-scenario">
      <div class="scenario-title">Asked "what is this about?"</div>
      <div class="scenario-script">
        "We work with retail tech GCCs on specialist hiring—[specific technology] roles with retail domain depth. It's about accelerating [programme name] if specialist hiring is creating pressure."
      </div>
    </div>
    
    <div class="gatekeeper-scenario">
      <div class="scenario-title">Not available</div>
      <div class="scenario-script">
        "No problem. When's a better time to reach them? I'll try back then."
        
        NEVER leave a voicemail on first attempt. Try callback 2-3 times before leaving voicemail.
      </div>
    </div>
  </div>
  
  <!-- 6. CALL SCRIPT - OPTIC FRAMEWORK -->
  <div class="optic-section">
    
    <!-- OPEN -->
    <div class="optic-block">
      <div class="optic-header">
        <span class="optic-badge">O</span>
        <span class="optic-title">OPEN — Warm Reference</span>
        <span class="optic-tag amber">2 sentences max</span>
      </div>
      <div class="optic-script">
        "Hi [First Name], this is [Your Name] calling from YALLO. I sent you a short note last week about specialist hiring for [Account]'s [Programme] programme. Is now okay for two minutes?"
      </div>
      <div class="optic-wait">⏸ WAIT for response. If no = "When's better?" If yes = proceed to PAIN.</div>
    </div>
    
    <!-- PAIN -->
    <div class="optic-block">
      <div class="optic-header">
        <span class="optic-badge">P</span>
        <span class="optic-title">PAIN — Qualifying Question</span>
        <span class="optic-tag green">Ask then WAIT</span>
      </div>
      <div class="optic-script">
        "We focus on the specialist roles that sit open longest—[GenAI engineers / Salesforce Commerce Cloud architects / Snowflake engineers / etc.]. Do you have any roles like that open more than 10 weeks right now?"
      </div>
      <div class="optic-wait">⏸ WAIT for response. If NO = thank and exit. If YES = proceed to TENSION.</div>
    </div>
    
    <!-- TENSION -->
    <div class="optic-block">
      <div class="optic-header">
        <span class="optic-badge">T</span>
        <span class="optic-title">TENSION — SPIN Implication</span>
        <span class="optic-tag amber">Only if pain confirmed</span>
      </div>
      <div class="optic-script">
        "If that [specific role] stays open another 6 weeks, what does that mean for the [programme name] timeline?"
      </div>
      <div class="optic-wait">⏸ WAIT for response. Listen for escalation, delivery risk, team pressure.</div>
    </div>
    
    <!-- INTRO -->
    <div class="optic-block">
      <div class="optic-header">
        <span class="optic-badge">I</span>
        <span class="optic-title">INTRO — 3 Sentences on YALLO</span>
        <span class="optic-tag green">After pain only</span>
      </div>
      <div class="optic-script">
        "Our founder was Group Chief Architect at Richemont before building YALLO—he screens candidates from the hiring side, not just the CV. We deliver two vetted candidates in 72 hours, screened for retail domain fit. We work alongside your existing suppliers, not instead of them."
      </div>
    </div>
    
    <!-- CLOSE -->
    <div class="optic-block">
      <div class="optic-header">
        <span class="optic-badge">C</span>
        <span class="optic-title">CLOSE — Book Meeting</span>
        <span class="optic-tag green">Get commitment</span>
      </div>
      <div class="optic-script">
        "Would it make sense to get a 20-minute call in the diary this week? Our team will tell you within that conversation whether we can genuinely help or not."
        
        [If YES] → "Perfect. Let me send you a calendar link. What's your email?"
        [If MAYBE] → "No pressure. I'll send you the link and you can book if it makes sense."
        [If NO] → "No problem. Can I check back in a month or is there someone else who handles this?"
      </div>
    </div>
    
  </div>
  
  <!-- 7. RESPONSE PATHS -->
  <div class="response-paths">
    <div class="response-path green">
      <div class="path-title">✓ YES — They Have Pain</div>
      <div class="path-script">
        "Great. Let me send you our calendar link. What's your email address?"
        
        Confirm email. Send discovery call link immediately after call.
      </div>
    </div>
    
    <div class="response-path red">
      <div class="path-title">✗ NO — No Current Pain</div>
      <div class="path-script">
        "No problem. If specialist hiring becomes a bottleneck later, feel free to reach out. Thanks for your time."
        
        Mark in CRM: No current pain. Follow up in 30-60 days.
      </div>
    </div>
    
    <div class="response-path amber">
      <div class="path-title">~ MAYBE — Interested But Not Ready</div>
      <div class="path-script">
        "Totally understand. I'll send you our info and you can reach out when timing is better. What's your email?"
        
        Send landing page link + discovery call link. Follow up in 14 days.
      </div>
    </div>
  </div>
  
  <!-- 8. OBJECTIONS -->
  <div class="objections-section">
    <div class="objections-title">Common Objections</div>
    
    <div class="objection-item">
      <div class="objection-trigger" onclick="toggleObj(this)">
        "We use suppliers already" ▼
      </div>
      <div class="objection-body">
        <div class="objection-response">
          "We work alongside your existing suppliers, not instead of them. We focus only on the 5-8 specialist roles per year where standard sourcing takes longest. Your suppliers handle general hiring—we accelerate the specialist bottleneck."
        </div>
        <div class="objection-redirect">
          ↩ Redirect: "Do you have any specialist roles sitting open 10+ weeks right now?"
        </div>
      </div>
    </div>
    
    <div class="objection-item">
      <div class="objection-trigger" onclick="toggleObj(this)">
        "We have internal TA" ▼
      </div>
      <div class="objection-body">
        <div class="objection-response">
          "That's great. We work with internal TA teams—we don't replace them. We provide specialist capacity for hard-to-fill roles while your TA team maintains the relationship. Think of us as your specialist sourcing arm."
        </div>
        <div class="objection-redirect">
          ↩ Redirect: "Does your TA team have any specialist roles taking 10+ weeks to fill?"
        </div>
      </div>
    </div>
    
    <div class="objection-item">
      <div class="objection-trigger" onclick="toggleObj(this)">
        "Send me info" ▼
      </div>
      <div class="objection-body">
        <div class="objection-response">
          "Happy to. Before I do, quick question: Are you dealing with any specialist roles that have been open 10+ weeks right now?"
          
          [If YES] → Continue OPTIC
          [If NO] → "No problem. I'll send you our info and you can reach out if specialist hiring becomes a bottleneck."
        </div>
        <div class="objection-redirect">
          ↩ Redirect: Qualify pain before sending info. No pain = send and exit.
        </div>
      </div>
    </div>
    
    <div class="objection-item">
      <div class="objection-trigger" onclick="toggleObj(this)">
        "Not the right time" ▼
      </div>
      <div class="objection-body">
        <div class="objection-response">
          "Totally understand. When would be a better time—next quarter? Or is there someone else on the team who handles specialist hiring day-to-day?"
        </div>
        <div class="objection-redirect">
          ↩ Redirect: Get timing or referral. Mark in CRM for follow-up.
        </div>
      </div>
    </div>
    
    <div class="objection-item">
      <div class="objection-trigger" onclick="toggleObj(this)">
        "Call back later" ▼
      </div>
      <div class="objection-body">
        <div class="objection-response">
          "No problem. When's a better time? I'll make a note and try back then."
          
          Get specific time. Mark in CRM. Do NOT just say "I'll try next week."
        </div>
        <div class="objection-redirect">
          ↩ Redirect: Lock in specific callback time.
        </div>
      </div>
    </div>
    
  </div>
  
  <!-- 9. CLOSE SEQUENCE -->
  <div class="close-sequence">
    <div class="close-title">Close Sequence</div>
    
    <div class="close-step">
      <div class="close-number">1</div>
      <div class="close-action">ASK FOR MEETING</div>
      <div class="close-script">"Would a 20-minute call this week make sense?"</div>
    </div>
    
    <div class="close-step">
      <div class="close-number">2</div>
      <div class="close-action">GET EMAIL</div>
      <div class="close-script">"Perfect. What's your email address?"</div>
    </div>
    
    <div class="close-step">
      <div class="close-number">3</div>
      <div class="close-action">CONFIRM DETAILS</div>
      <div class="close-script">"Great. I'll send you the calendar link to [email] right after this call."</div>
    </div>
    
    <div class="close-step">
      <div class="close-number">4</div>
      <div class="close-action">GET A NAME</div>
      <div class="close-script">"And just so the team knows who to expect—your full name is [First Last]?"</div>
    </div>
    
    <div class="close-step">
      <div class="close-number">5</div>
      <div class="close-action">THANK & EXIT</div>
      <div class="close-script">"Perfect. You'll get the link in the next few minutes. Looking forward to it."</div>
    </div>
  </div>
  
  <!-- 10. DO NOT SAY -->
  <div class="dont-say-section">
    <div class="dont-say-title">Do Not Say</div>
    <div class="dont-say-grid">
      <div class="dont-say-item">✗ "I'm just calling to touch base"</div>
      <div class="dont-say-item">✗ "Did you get my email?"</div>
      <div class="dont-say-item">✗ "I'll be brief"</div>
      <div class="dont-say-item">✗ "We're the best in the industry"</div>
      <div class="dont-say-item">✗ "Can I have 5 minutes?"</div>
      <div class="dont-say-item">✗ "Sorry to bother you"</div>
    </div>
  </div>
  
</div>
```

**Repeat entire structure for P2, P3, P4, P6 with persona-specific scripts**

---

#### 2.6 RIGHT PANEL (260px, sticky)

```html
<!-- RIGHT PANEL -->
<aside class="right-panel">
  
  <!-- GOLDEN RULES -->
  <div class="rp-section gold-header">
    <div class="rp-header">⚡ Golden Rules</div>
    <div class="rp-body">
      <div class="rule-box green">1. Talk less. Ask more.</div>
      <div class="rule-box green">2. Stop the moment they say yes.</div>
      <div class="rule-box green">3. Every objection ends with a question back.</div>
      <div class="rule-box green">4. One question at a time. Never two.</div>
      <div class="rule-box green">5. Curious tone. Not salesy tone.</div>
    </div>
  </div>
  
  <!-- ACCOUNT AT A GLANCE -->
  <div class="rp-section">
    <div class="rp-header">📊 [Account] — At a Glance</div>
    <div class="rp-body">
      <div class="stat-row">
        <div class="stat-label">GCC Size</div>
        <div class="stat-value">[GCC_SIZE]</div>
      </div>
      <div class="stat-row">
        <div class="stat-label">Open Roles</div>
        <div class="stat-value">[OPEN_ROLES]</div>
      </div>
      <div class="stat-row">
        <div class="stat-label">Hardest Fill</div>
        <div class="stat-value">[FILL_TIME]</div>
      </div>
      <div class="stat-row">
        <div class="stat-label">Live Programmes</div>
        <div class="stat-value">[PROGRAMME_COUNT]</div>
      </div>
      <div class="stat-row">
        <div class="stat-label">Location</div>
        <div class="stat-value">[LOCATION]</div>
      </div>
      <div class="stat-row">
        <div class="stat-label">Revenue</div>
        <div class="stat-value">[REVENUE]</div>
      </div>
    </div>
  </div>
  
  <!-- PERSONA NAVIGATOR -->
  <div class="rp-section">
    <div class="rp-header">👤 Persona Navigator</div>
    <div class="rp-body">
      <div class="persona-pill p1" onclick="switchTabDirect('p1')">
        <div class="persona-dot"></div>
        <div class="persona-text">P1 · SVP/VP — Budget owners</div>
      </div>
      <div class="persona-pill p2" onclick="switchTabDirect('p2')">
        <div class="persona-dot"></div>
        <div class="persona-text">P2 · Sr Directors — Tech authority</div>
      </div>
      <div class="persona-pill p3" onclick="switchTabDirect('p3')">
        <div class="persona-dot"></div>
        <div class="persona-text">P3 · Directors — Delivery pain</div>
      </div>
      <div class="persona-pill p4" onclick="switchTabDirect('p4')">
        <div class="persona-dot"></div>
        <div class="persona-text">P4 · TA/HR — Champions</div>
      </div>
      <div class="persona-pill p6" onclick="switchTabDirect('p6')">
        <div class="persona-dot"></div>
        <div class="persona-text">P6 · TPM/PM — Referral bridge</div>
      </div>
    </div>
  </div>
  
  <!-- CALLER TIPS -->
  <div class="rp-section green-header">
    <div class="rp-header">💡 Caller Tips</div>
    <div class="rp-body">
      <div class="tip">🎙 Smile before you dial. Changes vocal tone.</div>
      <div class="tip">⏱ Stand while calling. More energy and confidence.</div>
      <div class="tip">📝 Write their name down. Use it once only.</div>
      <div class="tip">🔇 Silence after question is thinking. Don't fill it.</div>
      <div class="tip">📞 Bad call is data. Log it and move on.</div>
      <div class="tip">🎯 Referral = win. Callback = win. "Not now" ≠ no.</div>
    </div>
  </div>
  
  <!-- MINDSET CHECK -->
  <div class="rp-section amber-header">
    <div class="rp-header">🧠 Mindset Check</div>
    <div class="rp-body">
      <div class="mindset-warning">
        <div class="warning-box">1. "No" is not personal. They said no to timing, not you.</div>
        <div class="warning-box">2. You're qualifying, not selling. No pressure to convert.</div>
        <div class="warning-box">3. 5 rejections in a row? Take 5-min break. Water. Reset.</div>
      </div>
      
      <div class="mood-selector">
        <div class="mood-label">How are you feeling right now?</div>
        <div class="mood-buttons">
          <button class="mood-btn" onclick="setMood('great', this)">😊 Great</button>
          <button class="mood-btn" onclick="setMood('ok', this)">😐 OK</button>
          <button class="mood-btn" onclick="setMood('rough', this)">😓 Rough</button>
        </div>
        
        <div id="mood-great" class="mood-msg">
          You're in the zone. Keep energy even—curiosity not urgency.
        </div>
        <div id="mood-ok" class="mood-msg">
          Totally normal. Focus on next call only. Forget last one.
        </div>
        <div id="mood-rough" class="mood-msg">
          Take 5 minutes. Seriously. Reset call always better than tired one.
        </div>
      </div>
    </div>
  </div>
  
  <!-- PROOF POINT -->
  <div class="rp-section">
    <div class="rp-header">🏆 Proof Point to Use</div>
    <div class="rp-body">
      <div class="proof-box">
        <strong>Alshaya Group</strong> — Middle East retail ($6B). Specialist Azure data platform engineer gap. Programme milestones slipping. YALLO delivered in 72 hours. Engineer contributed from week one.
      </div>
    </div>
  </div>
  
  <!-- CHATGPT PROMPT -->
  <div class="rp-section" style="border-color: #19C37D">
    <div class="rp-header" style="color: #19C37D">🤖 Got a Curveball? Ask ChatGPT</div>
    <div class="rp-body">
      <div class="gpt-intro">
        If they ask something unexpected—pricing, legal, technical role—pause, say "Let me check and come back", then use this prompt:
      </div>
      
      <div id="gpt-prompt-text" class="gpt-prompt">
I'm a sales caller for YALLO—specialist tech staffing for retail GCCs. Our founder was Group Chief Architect at Richemont (€20B). We deliver 2 vetted candidates in 72 hours. I'm calling [ACCOUNT_NAME]'s [PERSONA]. They asked: [PASTE THEIR QUESTION]. Give me a calm, confident 1-2 sentence response. No jargon. No long pitches.
      </div>
      
      <button id="copy-gpt-btn" onclick="copyGptPrompt()" class="btn-gpt">
        📋 Copy Prompt
      </button>
      
      <div class="gpt-note">
        Replace [PERSONA] and [THEIR QUESTION] before sending
      </div>
    </div>
  </div>
  
  <!-- BOOK THE CALL -->
  <div class="rp-section gold-header">
    <div class="rp-header">📅 Book the Discovery Call</div>
    <div class="rp-body">
      <button class="btn-booking gold" onclick="window.open('[DISCOVERY_CALL_LINK]')">
        Discovery Call — Apollo ↗
      </button>
      <button class="btn-booking dark" onclick="window.open('[SENIOR_PEER_CALL_LINK]')">
        Senior Peer Call — Calendly ↗
      </button>
    </div>
  </div>
  
</aside>
```

---

#### 2.7 FOOTER

```html
<footer>
  <div class="footer-content">
    <div class="footer-left">
      <span class="footer-brand">YALLO</span>
    </div>
    
    <div class="footer-center">
      <a href="[LANDING_PAGE_URL]">[LANDING_PAGE_URL]</a> ·
      <a href="[DISCOVERY_CALL_LINK]">Discovery Call</a> ·
      <a href="[SENIOR_PEER_CALL_LINK]">Senior Peer Call</a>
    </div>
    
    <div class="footer-right">
      Log every call in Apollo immediately after hanging up.
    </div>
  </div>
</footer>
```

---

#### 2.8 JAVASCRIPT FUNCTIONS

```javascript
// Tab switching
function switchTab(id) {
  document.querySelectorAll('.tab-panel').forEach(p => p.classList.remove('active'));
  document.querySelectorAll('.tab-btn').forEach(b => b.classList.remove('active'));
  document.getElementById(id).classList.add('active');
  event.currentTarget.classList.add('active');
  window.scrollTo({ top: 0, behavior: 'smooth' });
}

// Direct tab switch from right panel
function switchTabDirect(id) {
  document.querySelectorAll('.tab-panel').forEach(p => p.classList.remove('active'));
  document.querySelectorAll('.tab-btn').forEach(b => b.classList.remove('active'));
  document.getElementById(id).classList.add('active');
  document.querySelectorAll('.tab-btn').forEach(btn => {
    if (btn.getAttribute('onclick')?.includes("'" + id + "'")) btn.classList.add('active');
  });
  window.scrollTo({ top: 0, behavior: 'smooth' });
}

// Objection toggle
function toggleObj(trigger) {
  trigger.parentElement.classList.toggle('open');
}

// Mood selector
function setMood(mood, btn) {
  document.querySelectorAll('.mood-btn').forEach(b => b.classList.remove('active'));
  document.querySelectorAll('.mood-msg').forEach(m => m.classList.remove('visible'));
  btn.classList.add('active');
  document.getElementById('mood-' + mood).classList.add('visible');
}

// ChatGPT prompt copy
function copyGptPrompt() {
  const text = document.getElementById('gpt-prompt-text').innerText;
  navigator.clipboard.writeText(text).then(() => {
    const btn = document.getElementById('copy-gpt-btn');
    btn.textContent = '✓ Copied!';
    btn.style.background = '#0f9a5f';
    setTimeout(() => { 
      btn.textContent = '📋 Copy Prompt'; 
      btn.style.background = '#19C37D'; 
    }, 2000);
  }).catch(() => {
    const el = document.createElement('textarea');
    el.value = text; 
    document.body.appendChild(el); 
    el.select();
    document.execCommand('copy'); 
    document.body.removeChild(el);
    const btn = document.getElementById('copy-gpt-btn');
    btn.textContent = '✓ Copied!';
    setTimeout(() => { btn.textContent = '📋 Copy Prompt'; }, 2000);
  });
}
```

---

### STEP 3: SALES DIRECTOR QC REVIEW (5 minutes)

**ROLE:** Sales Director

**QC Checklist - Cold Call HTML:**
```
[ ] All 5 personas have complete OPTIC scripts
[ ] Scripts conversational (not robotic/salesy)
[ ] Account details throughout (programmes, roles, tech)
[ ] Objection handling addresses real concerns
[ ] Gatekeeper scripts included (P1, P2)
[ ] Quick Reference Cards accurate
[ ] Right panel complete (golden rules, tips, mood, GPT)
[ ] HTML structure matches existing format
[ ] All links working (discovery, peer call, landing page)
```

**If QC FAILS:** Request revisions

**If QC PASSES:** Proceed to contact enrichment

---

### STEP 4: CONTACT EXCEL ENRICHMENT (10-15 minutes)

**ROLE:** Data Operations Specialist

**Task:** Create enriched contact Excel matching Walmart format

---

#### 4.1 EXCEL STRUCTURE (Walmart Format)

**Sheet Structure:**

```
ROW 1: HEADER
- Title: "[ACCOUNT] × YALLO — Calling Campaign Dashboard"
- Stats: "Total contacts: [X] | India mobiles: [Y] | HQ only: [Z] | In sequence: [W]"

ROW 3: COLUMN HEADERS
- Persona | Total | Priority 1 | India Mobile | In Sequence | Email Verified

ROWS 4-9: PERSONA BREAKDOWN
- P1 · SVP/VP Country Head | [count] | [count] | [count] | [count] | [count]
- P2 · Sr Directors | [count] | [count] | [count] | [count] | [count]
- P3 · Directors/Managers | [count] | [count] | [count] | [count] | [count]
- P4 · TA/HR/Recruiters | [count] | [count] | [count] | [count] | [count]
- P6 · TPM/PM | [count] | [count] | [count] | [count] | [count]
- TOTAL | [count] | [count] | [count] | [count] | [count]

ROW 11: HOT SIGNALS SECTION
- "🔥 HOT SIGNALS — Priority contacts to call first"

ROW 12: COLUMN HEADERS FOR HOT SIGNALS
- Name | Title | Persona | Phone | Email | Why Call

ROWS 13+: HOT SIGNAL CONTACTS
- [Name] | [Title] | [Persona] | [Phone] | [Email] | [Why call reasoning]

Additional sections as needed:
- Specialist segments (if applicable)
- SAP specialists
- GenAI specialists
- etc.
```

---

#### 4.2 CONTACT ENRICHMENT LOGIC

**Persona Assignment:**
```
VP / SVP / C-Level → P1
Senior Director → P2
Director / Manager → P3
TA / Recruiter / HR → P4
TPM / PM / Program Manager → P6
```

**Priority Scoring (1-5):**
```
Priority 1 (Highest):
- P1 (all VPs/SVPs)
- P2 (all Sr Directors)
- P4 (all TA/Recruiters)

Priority 2:
- P3 Directors with India mobile verified

Priority 3:
- P3 Managers with India mobile verified

Priority 4:
- P3 with email only (no phone)

Priority 5:
- P6 (influencers, no decision authority)
```

**Phone Number Status:**
```
India Mobile: +91 [10 digits]
HQ Only: +1 [area code]-[number] or international format
No Number: Mark as "No number"
```

**Email Verification:**
```
Verified: Email matches company domain
Unverified: Generic email or missing
```

**"Why Call" Reasoning (Account-Specific):**
```
For P1: "[Name] owns programme delivery and GCC P&L. Specialist roles open 10+ weeks blocking [programme] milestones."

For P2: "[Name] (Sr Director [Technology]) leads engineering delivery and feels specialist gaps directly. [X] open roles under their org."

For P3: "[Name] ([Title]) manages [technology] teams. Specialist hiring delays create team delivery pressure and escalation."

For P4: "[Name] (TA Lead) handles specialist hiring. Open to overlay capacity for hard-to-fill [technology] roles."

For P6: "[Name] coordinates programmes. Feels delivery impact. Can refer to hiring decision makers."
```

---

#### 4.3 APOLLO ENRICHMENT NOTES

**What to add from Apollo (if using Apollo connector):**
- Missing contacts from org chart
- Phone numbers for contacts without them
- Recent job changes (title updates)
- Email verification status
- LinkedIn URL validation
- Sequence enrollment status

**Note in Excel:**
```
ENRICHMENT LOG (separate tab or bottom section):
- Original contacts: [X]
- Added from Apollo: [Y]
- Phone numbers found: [Z]
- Email verification: [W] verified, [V] unverified
- Total enriched contacts: [X+Y]
```

---

### STEP 5: DATA DIRECTOR QC REVIEW (5 minutes)

**ROLE:** Data Director

**QC Checklist - Contact Excel:**
```
[ ] All contacts assigned to personas (P1-P6)
[ ] Priority scoring logical (P1/P2/P4 = Priority 1)
[ ] Phone numbers formatted correctly
[ ] Email verification accurate
[ ] "Why Call" specific to each contact (not generic)
[ ] Summary dashboard totals correct
[ ] Hot signals section populated
[ ] Excel matches Walmart structure
```

**If QC FAILS:** Request corrections

**If QC PASSES:** Proceed to output generation

---

### STEP 6: OUTPUT GENERATION (5 minutes)

#### OUTPUT 1: Cold Calling HTML

**Format:** Single-file HTML (self-contained)

**Filename:** `[Account]_Cold_Calling_Cheat_Sheet.html`

**Save as:** `/mnt/user-data/outputs/[Account]_Cold_Calling_Cheat_Sheet.html`

---

#### OUTPUT 2: Enriched Contact Excel

**Format:** Excel file (.xlsx)

**Filename:** `[Account]_Calling_List_Enriched.xlsx`

**Save as:** `/mnt/user-data/outputs/[Account]_Calling_List_Enriched.xlsx`

**Alternative if Excel not possible:**
Save as CSV: `/mnt/user-data/outputs/[Account]_Calling_List_Enriched.csv`

---

### STEP 7: FINAL DELIVERY TO USER (2 minutes)

**Present both outputs:**

```
✅ SKILL 4 COMPLETE - COLD CALLING HTML & CONTACT EXCEL

I've created 2 deliverables for [Account Name]:

📞 OUTPUT 1: Cold Calling HTML Cheat Sheet
- Single-file HTML (self-contained)
- 5 persona scripts (OPTIC framework)
- Objection handling, gatekeeper scripts
- Right panel tools (mood selector, GPT prompt)
- Matches existing YALLO format
- File: [Account]_Cold_Calling_Cheat_Sheet.html

📊 OUTPUT 2: Enriched Contact Excel
- Matches Walmart calling list format
- All contacts persona-assigned
- Priority scoring (1-5)
- Phone numbers included
- "Why Call" reasoning per contact
- Hot signals section
- File: [Account]_Calling_List_Enriched.xlsx

Next Steps:
1. Open HTML in browser, bookmark for calling team
2. Share Excel with calling team
3. Import contacts into Apollo
4. Begin outreach campaign

🎉 ALL 4 SKILLS COMPLETE! 🎉

You now have:
- SKILL 1: ABM Research & Strategy
- SKILL 2: Email, LinkedIn & Newsletter
- SKILL 3: Landing Page & Pitch Deck
- SKILL 4: Cold Call HTML & Contact Excel

Ready to run full ABM campaigns from research to execution!
```

---

## ⚠️ COMMON PITFALLS TO AVOID

### Cold Call HTML:
❌ Scripts too long or robotic
❌ Buzzwords and jargon
❌ Generic templates (not account-specific)
❌ Missing gatekeeper scripts (P1, P2 need them)
❌ Weak objection handling (doesn't address real concerns)

### Contact Excel:
❌ Generic "Why Call" (not specific to person's role)
❌ Incorrect persona assignments
❌ Missing priority scoring
❌ Phone numbers not formatted consistently
❌ Summary totals don't match

---

## 🎯 SUCCESS METRICS

**This skill is successful when:**

1. **HTML is usable:**
   - Calling team can open and use immediately
   - Scripts natural and conversational
   - All 5 personas covered
   - Account-specific throughout

2. **Excel is actionable:**
   - Calling team knows who to call first (hot signals)
   - Priority scoring clear
   - "Why Call" gives context
   - Phone numbers ready to dial

3. **User feedback:**
   - "This HTML is exactly what we need"
   - "Excel has all the context for calling"
   - "Scripts are natural, not robotic"

---

## 📝 QUALITY ASSURANCE LOG

```
[TIMESTAMP] SKILL 4 STARTED

[TIMESTAMP] Cold Call HTML Created
- 5 persona scripts: ✓ (OPTIC framework)
- Gatekeeper scripts: ✓ (P1, P2)
- Objections: ✓ (5+ per persona)
- Right panel: ✓ (all sections)
- Account-specific: ✓

[TIMESTAMP] Sales Director QC Review
✓ All scripts conversational
✓ Account details throughout
✓ OPTIC framework followed
→ APPROVED

[TIMESTAMP] Contact Excel Created
- Persona assignments: ✓
- Priority scoring: ✓
- Phone numbers: ✓
- "Why Call": ✓ (specific)
- Hot signals: ✓

[TIMESTAMP] Data Director QC Review
✓ All contacts assigned
✓ Priority logic correct
✓ "Why Call" specific
✓ Totals accurate
→ APPROVED

[TIMESTAMP] Outputs Generated
✓ HTML file created (self-contained)
✓ Excel file created (enriched)

[TIMESTAMP] SKILL 4 COMPLETE
Duration: 45 minutes
Quality: All QC checkpoints passed
```

---

**END OF SKILL 4: COLD CALLING HTML & CONTACT EXCEL**

---

## 🎉 **ALL 4 ABM SKILLS COMPLETE!**

**Full ABM Workflow Now Available:**
1. SKILL 1: ABM Research & Strategy → Research report + 14-slide Gamma doc
2. SKILL 2: Email, LinkedIn & Newsletter → 30 emails + LinkedIn + 4 newsletters
3. SKILL 3: Landing Page & Pitch Deck → Content PDF + 12-slide pitch deck
4. SKILL 4: Cold Call & Contact Excel → HTML cheat sheet + enriched contacts

**Total:** 9+ deliverables across complete ABM campaign lifecycle
