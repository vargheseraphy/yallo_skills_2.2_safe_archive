# SKILL 4: ABM COLD CALL & CONTACT ENRICHMENT

**Generate cold calling HTML cheat sheet and enriched contact Excel with Apollo integration**

---

## 📋 WHAT THIS SKILL DOES

This skill creates cold calling assets for your sales team:

**Outputs:**
1. Cold Calling HTML Cheat Sheet (single-file HTML)
2. Enriched Contact Excel (Apollo-integrated)

**Execution Time:** 40-50 minutes

---

## 🚀 HOW TO INSTALL

### Step 1: Extract ZIP
1. Download and extract this ZIP file
2. You'll see 2 files:
   - `SKILL.md` (the skill file)
   - `README.md` (this file)

### Step 2: Upload to Claude Projects
1. Go to **Claude.ai**
2. Click **Projects** in left sidebar
3. Create new project OR select existing project
4. Click **Settings** (gear icon)
5. Go to **Skills** tab
6. Click **"Add Skill"** or **"Upload Skill"**
7. Upload the `SKILL.md` file

### Step 3: Verify
You should see "ABM Cold Call & Contact Enrichment" in your Skills list

---

## 💡 HOW TO USE

### Trigger Phrases:
```
Create cold call assets for Walmart
Generate calling cheat sheet for Target
Build cold call HTML and contact list for Lululemon
Create calling assets for Nike
```

### Required Inputs:
```yaml
FROM_SKILL_1:
  abm_strategy_document: [Output from Skill 1]
  account_name: "Walmart Global Tech India"
  personas_identified: [P1, P2, P3, P4, P6]
  pain_points: [From research]

ACCOUNT_DETAILS:
  account_accent_color: "#0071CE" (e.g., Walmart blue)
  gcc_location: "Bengaluru + Chennai"
  gcc_size: "25,000+ engineers"
  revenue: "$681B"
  open_roles_count: "250+"
  hardest_fill_time: "12-16 weeks"
  live_programmes: ["GenAI Platform", "Payments", "Supply Chain"]

CONTACT_DATA:
  contact_list: [Upload Excel file]

CAMPAIGN_LINKS:
  landing_page_url: "go.yallo.co/walmart"
  discovery_call_link: "https://app.apollo.io/#/meet/..."
```

---

## 📊 WHAT YOU'LL GET

### OUTPUT 1: Cold Calling HTML Cheat Sheet
**Single-file HTML (self-contained):**

**Structure:**
- **Sticky Header:** Account name, stats, landing page
- **Left Sidebar:** 5 persona tabs + OPTIC framework reminder
- **Main Content:** OPTIC scripts for each persona
- **Right Panel:** Golden rules, tips, mood selector, ChatGPT prompt

**5 Persona Scripts (OPTIC Framework):**
- P1 (SVP/VP) - Budget Owners
- P2 (Sr Directors) - Technical Authority
- P3 (Directors/Managers) - Delivery Pain
- P4 (TA/HR) - Champions
- P6 (TPM/PM) - Referral Bridge

**Each Persona Includes:**
- Quick Reference Card (5-column summary)
- Booking row (discovery + senior peer calls)
- Persona card (Who/What/Pain)
- Gatekeeper script (P1, P2 only)
- OPTIC call script (5 blocks)
- Response paths (Yes/No/Maybe)
- Objections (accordion, 5+ per persona)
- Close sequence (5 numbered steps)
- Do Not Say (2-column grid)

**Right Panel Tools:**
- Golden Rules (5 rules)
- Account At a Glance (stats)
- Persona Navigator (quick switch)
- Caller Tips (6 tips)
- Mindset Check (mood selector)
- Proof Point to Use
- ChatGPT Curveball Prompt (with copy button)
- Book the Call (buttons)

### OUTPUT 2: Enriched Contact Excel
**Apollo-integrated contact list:**

**Format (matches Walmart structure):**
- Row 1: Dashboard header with totals
- Row 3-9: Persona breakdown table
- Row 11+: Hot Signals section
- Additional specialist segments

**Enrichment:**
- Persona assignments (P1-P6)
- Priority scoring (1-5)
- Phone numbers (India mobile vs HQ)
- Email verification status
- "Why Call" reasoning per contact

---

## ⏱️ EXECUTION WORKFLOW

**Total Time:** 40-50 minutes

### Step 1: Input Validation (5 min)

### Step 2: Cold Calling HTML Generation (25-30 min)
- Header section
- Sidebar with 5 persona tabs
- Main content: OPTIC scripts for all personas
- Right panel: Tools and tips
- Footer with links

### Step 3: Sales Director QC Review (5 min)
Quality checkpoint - validates scripts are conversational

### Step 4: Contact Excel Enrichment (10-15 min)
- Persona assignments
- Priority scoring
- Phone number enrichment
- "Why Call" reasoning

### Step 5: Data Director QC Review (5 min)
Final quality checkpoint

### Step 6: Output Generation (5 min)

---

## 🎯 QUALITY CONTROL

**2 QC Managers:**
- **Sales Director** - Reviews call scripts for natural flow, OPTIC adherence
- **Data Director** - Reviews Excel for accurate enrichment, priority logic

**Quality Standards:**
- Scripts conversational (not robotic/salesy)
- Account details in every script
- Objection handling addresses real concerns
- Contact Excel matches Walmart format
- "Why Call" specific to each contact's role

---

## 💡 USAGE EXAMPLE

```
Create cold call assets for Walmart

Inputs:
- Account accent color: #0071CE
- GCC size: 25,000+ engineers
- Revenue: $681B
- Open roles: 250+
- Hardest fill time: 12-16 weeks
- Live programmes: GenAI Platform, Payments Tech, Supply Chain
- Contact list: [upload walmart_contacts.xlsx]

[Skill executes for 40-50 minutes]

Outputs delivered:
✅ Walmart_Cold_Calling_Cheat_Sheet.html
   - Single-file HTML (open in browser)
   - 5 persona scripts (OPTIC framework)
   - Right panel tools
   - Self-contained (no external files needed)

✅ Walmart_Calling_List_Enriched.xlsx
   - Dashboard with totals
   - Persona breakdown
   - Hot signals section
   - Priority scoring
   - "Why Call" per contact
```

---

## 📞 OPTIC FRAMEWORK

**Every call script follows OPTIC:**

**O - OPEN:** Warm reference (2 sentences max)
```
"Hi [First Name], this is [Your Name] from YALLO. I sent you a 
note about specialist hiring for Walmart's GenAI platform. 
Is now okay for two minutes?"
```

**P - PAIN:** Qualifying question (ask then WAIT)
```
"Do you have any GenAI or Snowflake roles open more than 
10 weeks right now?"
```

**T - TENSION:** SPIN implication (only if pain confirmed)
```
"If that role stays open another 6 weeks, what happens to 
the GenAI platform timeline?"
```

**I - INTRO:** 3 sentences on YALLO (after pain only)
```
"Our founder was Group Chief Architect at Richemont. We deliver 
2 vetted candidates in 72 hours, screened for retail domain fit. 
We work alongside your suppliers, not instead of them."
```

**C - CLOSE:** Book meeting + get email + get name
```
"Would a 20-minute call this week make sense?"
```

---

## 🖥️ HTML FEATURES

### Design
- Dark theme (#0A0A0A background)
- YALLO gold accents (#D6B24C)
- Account accent color for branding
- Sticky header + sidebar
- Responsive layout

### Interactive Elements
- Persona tab switching
- Collapsible objections
- Mood selector (Great/OK/Rough)
- ChatGPT prompt copy button
- Direct booking buttons

### Fonts (Google Fonts CDN)
- **Syne** - Headers
- **DM Sans** - Body text
- **DM Mono** - Stats/code

---

## 📊 CONTACT EXCEL STRUCTURE

**Dashboard (Row 1):**
```
WALMART × YALLO — Calling Campaign Dashboard
Total: 40 | India mobiles: 25 | HQ only: 10 | In sequence: 15
```

**Persona Breakdown (Rows 3-9):**
```
Persona              | Total | Priority 1 | India Mobile | In Sequence
P1 · SVP/VP          |   5   |     5      |      3       |      2
P2 · Sr Directors    |   8   |     8      |      5       |      3
P3 · Directors       |  12   |     0      |      8       |      4
P4 · TA/HR           |   8   |     8      |      5       |      4
P6 · TPM/PM          |   7   |     0      |      4       |      2
```

**Hot Signals (Row 11+):**
```
Name | Title | Persona | Phone | Email | Why Call
[Name] | VP Engineering | P1 | +91-xxx | [email] | Owns programme delivery...
```

---

## 🔧 TROUBLESHOOTING

### Issue: "Missing account accent color"
**Solution:** Provide a hex color code (e.g., #0071CE for Walmart blue)

### Issue: "Sales Director rejected scripts"
**Solution:** Common issues:
- Scripts too robotic/salesy
- Missing account-specific details
- Generic objection handling

### Issue: "Contact Excel format doesn't match Walmart"
**Solution:** Skill will reformat. Ensure contact list has names, titles, emails.

---

## 📚 USING THE OUTPUTS

### HTML Cheat Sheet:
1. Open in browser (Chrome, Safari, Firefox)
2. Bookmark for easy access
3. Share with calling team
4. Use during calls (leave open on screen)

### Contact Excel:
1. Import into Apollo
2. Use Hot Signals for priority calling
3. Reference "Why Call" before each call
4. Track call outcomes in Excel

---

## ✨ KEY FEATURES

- ✅ **OPTIC Framework:** Proven cold calling structure
- ✅ **Account-Specific:** All scripts reference real programmes/roles
- ✅ **Interactive HTML:** Mood selector, ChatGPT prompt, tabs
- ✅ **Apollo-Ready:** Contact Excel matches standard format
- ✅ **Quality Control:** 2 QC managers ensure natural, effective scripts

---

## 📞 SUPPORT

**Questions?**
- Review the full SKILL.md file for complete HTML structure
- Check OPTIC script examples per persona
- See contact enrichment logic in SKILL.md

**Ready to create calling assets?**
```
Create cold call assets for [Your Target Account]
```

---

**Version:** 1.0  
**Last Updated:** March 2026  
**License:** Proprietary - YALLO internal use
