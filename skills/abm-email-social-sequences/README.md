# SKILL 2: ABM EMAIL & SOCIAL SEQUENCES

**Generate email sequences (Apollo format), LinkedIn scripts, and HTML newsletters**

---

## 📋 WHAT THIS SKILL DOES

This skill creates all email, LinkedIn, and newsletter content for your ABM campaign:

**Outputs:**
1. Email Sequences (Apollo CSV, 25-30 emails)
2. LinkedIn Sequences (Connection + 3 DMs per persona)
3. Newsletter Sequence (4 HTML emails)

**Execution Time:** 60-90 minutes

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
You should see "ABM Email & Social Sequences" in your Skills list

---

## 💡 HOW TO USE

### Trigger Phrases:
```
Create ABM content for Walmart
Generate email sequences for Target
Create LinkedIn and newsletter sequences for Lululemon
Build ABM email and social content for Nike
```

### Required Inputs:
```yaml
FROM_SKILL_1:
  abm_strategy_document: [Output from Skill 1]
  account_name: "Walmart Global Tech India"
  personas_identified: [P1, P2, P3, P4, P6]
  pain_points: [From research]
  tech_stack: [From research]

CONTACT_DATA:
  contact_list: [Excel with persona assignments]

CAMPAIGN_DETAILS:
  landing_page_url: "go.yallo.co/walmart"
  discovery_call_link: "https://app.apollo.io/#/meet/..."
```

---

## 📊 WHAT YOU'LL GET

### OUTPUT 1: Email Sequences (Apollo CSV)
**25-30 emails across 5 personas:**
- P1 (SVP/VP) - 5 emails
- P2 (Sr Directors) - 5 emails
- P3 (Directors/Managers) - 5-6 emails
- P4 (TA/HR) - 5 emails
- P6 (TPM/PM - Influencers) - 5 emails

**Each email:**
- Under 100 words
- One metric maximum
- Subject line under 50 characters
- Account-specific throughout

**Send Schedule:** Day 1, 3, 7, 14, 21

### OUTPUT 2: LinkedIn Sequences
**20 templates (5 personas × 4 messages):**
- Connection request (280 chars)
- DM 1 (Day 3): Value share, no pitch
- DM 2 (Day 7): Insight + soft mention
- DM 3 (Day 14): Meeting ask

### OUTPUT 3: Newsletter Sequence (4 HTML files)
**Matching Accumba design system:**
- Newsletter 1 (TOFU): Market intelligence
- Newsletter 2 (MOFU): Case study
- Newsletter 3 (MOFU): Thought leadership
- Newsletter 4 (BOFU): Direct offer

---

## ⏱️ EXECUTION WORKFLOW

**Total Time:** 60-90 minutes

### ⚡ INCREMENTAL EXECUTION (CRITICAL!)

**This skill executes persona-by-persona with approval gates:**

```
1. Create P1 emails (5) 
   → Present to you
   → GET APPROVAL
   → Then proceed to P2

2. Create P2 emails (5)
   → Present to you
   → GET APPROVAL
   → Then proceed to P3

[And so on for P3, P4, P6]
```

**Why incremental?**
- Ensures quality at each step
- Prevents 30 generic emails at once
- Allows you to refine approach per persona

### Full Workflow:

**Step 1: Input Validation (5 min)**

**Step 2: Email Sequences - INCREMENTAL (40-50 min)**
- P1: 10 min → Approval
- P2: 10 min → Approval
- P3: 10 min → Approval
- P4: 10 min → Approval
- P6: 10 min → Approval
- Apollo CSV: 5 min

**Step 3: LinkedIn Sequences (15-20 min)**

**Step 4: Newsletter Sequence (25-30 min)**

**Step 5: Final Delivery**

---

## 🎯 QUALITY CONTROL

**3 QC Managers:**
- **Email Marketing Director** - Reviews each persona before approval (5 checkpoints)
- **Social Media Director** - Reviews LinkedIn sequences
- **Content Director** - Reviews newsletter HTML

**Quality Standards:**
- Subject lines under 50 chars
- Email bodies under 100 words
- One metric per email
- CTA progression natural (soft → direct → exit)
- Account-specific details throughout
- No buzzwords or jargon

---

## 💡 USAGE EXAMPLE

```
Create ABM content for Walmart

[Skill asks for SKILL 1 outputs]

PERSONA 1 (P1) CREATED:
Email 1: "Walmart specialist hiring velocity"
Email 2: "Specialist hiring bottleneck at Walmart"
Email 3: "GenAI engineer hiring velocity"
Email 4: "Quick question on GenAI platform timeline"
Email 5: "Last note on Walmart specialist hiring"

→ YOU APPROVE → Skill proceeds to P2
→ YOU REJECT → Skill refines and re-presents

[After all 5 personas approved]

Outputs delivered:
✅ Walmart_Email_Sequences_Apollo.csv (30 emails)
✅ Walmart_LinkedIn_Sequences.md (20 templates)
✅ Walmart_Newsletter_1_TOFU.html
✅ Walmart_Newsletter_2_MOFU.html
✅ Walmart_Newsletter_3_MOFU.html
✅ Walmart_Newsletter_4_BOFU.html
```

---

## 📧 EMAIL FRAMEWORK

**All emails follow 4-step structure:**

1. **Context (1 sentence)** - Show you know their business
2. **Challenge (1-2 sentences)** - Frame the problem
3. **Micro-Proof (1 sentence)** - ONE metric only
4. **Soft CTA (1 sentence)** - Ask for conversation

**CTA Progression:**
- Email 1-2: NO meeting ask (value only)
- Email 3: Soft mention of conversation
- Email 4: Direct but casual ask
- Email 5: Final clear CTA with respectful exit

---

## 🔧 TROUBLESHOOTING

### Issue: "Missing SKILL 1 outputs"
**Solution:** Run SKILL 1 first. This skill needs the ABM Strategy Document.

### Issue: "Email Marketing Director rejected P1"
**Solution:** Review the feedback. Common issues:
- Emails too long (over 100 words)
- Multiple metrics in one email
- No account-specific details
- Buzzwords or jargon

### Issue: "Newsletters don't match Accumba design"
**Solution:** The skill will refine the HTML. Content Director ensures brand consistency.

---

## 📚 NEXT STEPS

After completing SKILL 2, you can run:

**SKILL 3: ABM Landing Page & Pitch Deck**
- Landing page content for web team
- 12-slide pitch deck for meetings

**SKILL 4: ABM Cold Call & Contact Enrichment**
- Cold calling HTML cheat sheet
- Enriched contact Excel

---

## ✨ KEY FEATURES

- ✅ **Incremental Execution:** Persona-by-persona with 5 approval gates
- ✅ **Account-Specific:** Every email references real programmes/roles
- ✅ **Quality Control:** 3 QC managers ensure high standards
- ✅ **Apollo-Ready:** CSV format for direct import
- ✅ **Design Consistency:** Newsletters match Accumba branding

---

## 📞 SUPPORT

**Questions?**
- Review the full SKILL.md file for complete email examples
- Check "Common Pitfalls" section
- See persona-specific email templates in SKILL.md

**Ready to create content?**
```
Create ABM content for [Your Target Account]
```

---

**Version:** 1.0  
**Last Updated:** March 2026  
**License:** Proprietary - YALLO internal use
