---
name: compliance-checker
description: "Check ad copy, landing pages, VSLs, and emails for platform compliance issues — Meta/Facebook, Google, TikTok, YouTube, and ClickBank. Use this skill whenever the user asks to check compliance, run a compliance audit, review copy for platform policy violations, check if copy will get banned or flagged, audit for Meta/Facebook ad policy, or scan for trigger words. Also trigger for 'is this compliant', 'will this get rejected', 'check for banned words', 'platform policy check', or any task involving reviewing direct response copy against advertising platform rules."
---

> Created by **Rob Palmer** — direct-response copywriter ($523M+ tracked).
> Source & updates: https://github.com/robpalmer99/claude-code-copywriting-skills
> Free under CC-BY-4.0. Attribution requested when redistributed.

# Compliance Checker Skill

This skill checks direct response copy (ads, landing pages, VSLs, emails) against platform compliance rules. Built on real-world compliance knowledge from practitioners who've been banned 300+ times and learned what actually triggers rejections.

The goal: catch compliance issues BEFORE your ad gets rejected or your account gets banned, while preserving persuasive power through compliant rewrites.

---

# Step 1: Classify the Copy

Before checking anything, determine these four things. Ask the user if unclear.

## Copy Type
- **Ad** (primary text, headline, description, video script)
- **Landing page** (bridge page, pre-sell, PDP)
- **VSL script** (video sales letter transcript)
- **Email** (broadcast, sequence, autoresponder)
- **Advertorial** (native content, editorial-style)

## Platform
- **Meta/Facebook** (strictest — deep rules below)
- **Google Ads** (medical claims ban, bait-and-switch enforcement)
- **TikTok** (commercial disclosure, biometric imagery ban)
- **YouTube** (more lenient — before/afters allowed)
- **ClickBank** (affiliate network rules, income claims)

## Product Category
- **Supplement / ingestible** (HIGHEST scrutiny on Meta — extra fine-tooth comb)
- **Ecom physical** (post-purchase surveys, page score penalties)
- **Digital product** (lower scrutiny — no post-purchase surveys)
- **Coaching / service** (income claim sensitivity)

Note: Digital products with physical upsells may be reclassified as ecom.

## Funnel Position
- **Front-end ad** (strictest rules)
- **Landing page** (strict — product must be visible, exit nav required)
- **Upsell page** (more leniency — countdown timers, urgency, aggressive language OK post-purchase)

---

# Step 2: Load Trigger Words Reference

Read `references/trigger-words.md` for the consolidated table of trigger words and compliant substitutions.

---

# Step 3: Phase 1 — Checklist Audit

Run through each category. Report PASS / FAIL / WARN for each.

## The 9-Point Compliance Checklist

### 1. Personal Attributes
- [ ] No "you" or "your" assuming the viewer has a condition (ecom/supplement ads)
- [ ] No questions implying problems ("Are you struggling with...?" = implies they have the problem)
- [ ] No singling out demographics ("women's metabolism" = personal attribute)
- [ ] No calling out conditions ("if you have diabetes" = implies they have it)
- [ ] Uses third-person framing where needed ("Many Americans..." / "Most people...")

**Why this matters:** Facebook considers implying you know the viewer's personal attributes (age, medical conditions, body type, financial status) a violation. Change "you" to "I" when describing pain, or use third-person framing.

**Compliant patterns:**
- "Many Americans are looking for ways to..." (third-person)
- "I used to struggle with..." (first-person story)
- "People working on problem areas..." (general group)

**Non-compliant patterns:**
- "Are you struggling with...?" (implies they have the problem)
- "If you have diabetes..." (calls out condition)
- "Women over 40 who..." (singles out demographic + age)

### 2. Sensational & Negative Language
- [ ] No banned negative words: ruin, destroy, kill, wreck, terrible, worse, disgusting, bad, harmful, detrimental, damaging, wipe out, butcher
- [ ] No scare tactics ("If you don't take X, you'll decrease your lifespan")
- [ ] No shocking, violent, or fear-based content
- [ ] No negative imagery descriptions (sad faces, red spots on bodies, weapons)
- [ ] Positive/neutral framing throughout

**Compliant substitutions:** impact, change, support, help, balance, manage, affect, influence

### 3. Medical & Health Claims
- [ ] All health claims use softening words (helps, supports, can, may, promotes)
- [ ] No definitive claims ("grow hair" → "help support hair growth")
- [ ] No "X results in Y days" (timelines + outcomes = definitive claim)
- [ ] No disease names used directly (diabetes, Alzheimer's, dementia, cancer)
- [ ] Scientific claims reference studies if made
- [ ] Testimonials include "results may vary" asterisk

**The softening rule:** NEVER use health verbs without a modifier. "Regulate blood sugar" is a claim. "Helps support blood sugar" is compliant.

**Required modifiers:** helps, supports, can, may, promotes, aids in, assists with

**Disease name workarounds:**
- "Diabetes" → "type two" (without the word "diabetes")
- "Alzheimer's/dementia" → "memory," "brain health," "brain fog"
- "Cancer" → cannot mention, must reframe entirely
- "Arthritis" → "joint health," "joint comfort"

### 4. Income & Financial Claims
- [ ] No guaranteed income promises
- [ ] No specific earnings claims without disclaimers
- [ ] Uses "revenue" not "earnings" where possible
- [ ] No "lifetime" access (ClickBank ban)
- [ ] Reflects actual/typical effort required

**Compliant income language:**
- NOT: "Let me show you how to generate XXX leads at $5 a pop"
- OK: "My unique process makes generating XXX leads for $5 possible"
- NOT: "Guarantee passive income"
- OK: "Potential income opportunity with effort and attention"

### 5. Before & After
- [ ] No before/after side-by-side images (Facebook ban)
- [ ] No zooming into body parts (makes users feel self-conscious)
- [ ] Compliant alternatives used if showing results

**Compliant alternatives:**
- First-person success stories on camera (influencer style)
- Customer testimonials describing specific benefits (text, not images)
- Product demonstration videos

**Note:** YouTube ALLOWS before/afters. This rule is Facebook-specific.

### 6. Open Loops & Clickbait
- [ ] No unresolved open loops (even if closed in body, headline can't leave them open)
- [ ] No multi-click curiosity chains / information gates
- [ ] Product name visible in post text, headline, or video watermark
- [ ] Ad accurately reflects landing page content

**The open loop rule:**
- NOT compliant: "Watch now to discover 5 foods that accelerate arthritis" (open loop)
- Compliant: "We reveal what foods to avoid below" (resolved)
- NOT compliant: "Find out what the 3 most effective ways to lose weight really are" (hidden behind noun)
- Compliant: "Three effective ways to manage weight" (direct statement)

### 7. Trigger Words
- [ ] Check all copy against `references/trigger-words.md`
- [ ] All flagged words replaced with compliant alternatives
- [ ] Softening modifiers present on all health/medical verbs

### 8. Landing Page Elements (if reviewing a landing page)
- [ ] Product info visible without watching VSL (viewer can determine what's sold by scrolling)
- [ ] VSL does not auto-play (looping GIF OK if not first 2 seconds of video)
- [ ] Exit navigation present (hamburger menu, header links, footer links)
- [ ] Homepage is legitimate (not just 2-page blog — needs substance, privacy policy, ToS)
- [ ] No fake countdown timers or fake scarcity
- [ ] Disclaimers present (privacy policy, return policy, ToS)
- [ ] "Results may vary" on testimonials
- [ ] Scientific claims have citation + full study reference at page bottom

### 9. Ad-to-Page Consistency
- [ ] Visual consistency (same logo/watermark across ad and page)
- [ ] Same messaging vibe (viewer feels they're in the right place)
- [ ] No bait-and-switch (ad claims match landing page content)
- [ ] Same root domain (no redirect chains to different domains — common ban reason)
- [ ] Go direct to brand URL (no affiliate-style redirect links)

---

# Step 4: Phase 2 — Line-Level Flagging

Go through the copy line by line. For each issue found:

```
### Issue N [SEVERITY]
> "The exact problematic text quoted here"
**Rule:** Which compliance rule this violates and why
**Rewrite:** A compliant alternative that preserves persuasive power
```

**Severity levels:**
- **HIGH** — Likely rejection or account ban. Must fix before running.
- **MEDIUM** — Risky, could be flagged depending on reviewer. Should fix.
- **LOW** — Minor concern, could be flagged in stricter review cycles.

**Prioritize issues by severity.** HIGH first, then MEDIUM, then LOW.

**Rewrite rules:**
- Preserve the persuasive intent of the original
- Use compliant substitutions from `references/trigger-words.md`
- Maintain the copy's voice and rhythm
- The rewrite should be drop-in ready — same approximate length, same tone

---

# Step 5: Compliance Score

After both phases, calculate:

**Scoring:** Start at 10. Subtract 2 per HIGH issue, 1 per MEDIUM, 0.5 per LOW. Floor at 0.

| Score | Rating | Recommendation |
|-------|--------|----------------|
| 8-10 | Ready to run | Minor or no changes needed |
| 5-7 | Needs fixes | Address flagged issues before submitting |
| 0-4 | Major rewrite | Significant compliance issues — rewrite required |

---

# Output Format

```
## Copy Classification
- Type: [ad / landing page / VSL / email / advertorial]
- Platform: [Meta / Google / TikTok / YouTube / ClickBank]
- Product: [supplement / digital / ecom / coaching]
- Funnel position: [front-end ad / landing page / upsell]

## Phase 1: Checklist Audit

| # | Category | Status | Notes |
|---|----------|--------|-------|
| 1 | Personal Attributes | PASS/FAIL/WARN | [brief note] |
| 2 | Sensational/Negative Language | PASS/FAIL/WARN | [brief note] |
| 3 | Medical/Health Claims | PASS/FAIL/WARN | [brief note] |
| 4 | Income/Financial Claims | PASS/FAIL/WARN | [brief note] |
| 5 | Before/After | PASS/FAIL/WARN | [brief note] |
| 6 | Open Loops & Clickbait | PASS/FAIL/WARN | [brief note] |
| 7 | Trigger Words | PASS/FAIL/WARN | [brief note] |
| 8 | Landing Page Elements | PASS/FAIL/WARN/N/A | [brief note] |
| 9 | Ad-to-Page Consistency | PASS/FAIL/WARN/N/A | [brief note] |

## Phase 2: Line-Level Issues

### Issue 1 [HIGH]
> "quoted text"
**Rule:** explanation
**Rewrite:** compliant alternative

### Issue 2 [MEDIUM]
> ...

## Compliance Score: X/10
[Ready to run / Needs fixes / Major rewrite needed]

## Summary
- X HIGH issues, Y MEDIUM, Z LOW
- Top priority fixes: [numbered list]
- What's already compliant: [brief note]
```

---

# Platform-Specific Rules

## Meta / Facebook (Deep Coverage)

### The 7 Deadly Sins of Facebook Ads
1. **Implied negative attributes** — assuming you know the viewer's problems
2. **Sensational/shocking language** — scare tactics, violent imagery, death language
3. **Withholding information** — clickbait loops that never deliver
4. **Definitive medical claims** — "X results in Y days," guaranteed outcomes
5. **Before/after imagery** — side-by-side body comparisons
6. **Personal attributes** — singling out gender, age, condition
7. **Negative language framing** — ruin, destroy, kill, wreck, terrible

### Meta's 3-Tier Review System
| Tier | What They Check |
|------|----------------|
| **1. The Ad** | Claims, sensational language, personal attributes, clickbait, accuracy to landing page |
| **2. Landing Page** | Product visibility, VSL auto-play, exit nav, disclaimers, fake urgency |
| **3. Post-Conversion** | Feedback surveys to purchasers (ecom only); low scores = penalty |

### Digital vs Ecom Scrutiny on Meta
| Factor | Digital Products | Ecom / Supplements |
|--------|-----------------|-------------------|
| Post-purchase surveys | No (automatic delivery) | Yes (feedback score) |
| Page score penalties | No | Yes (below threshold = automatic penalty) |
| Ingestible scrutiny | N/A | Extra fine-tooth-comb |
| Reclassification risk | Yes, if physical upsell | Default |
| Overall scrutiny | Lower | Higher |

### Compliant Headline Rewrites (Meta Examples)
| Non-Compliant | Why It Fails | Compliant |
|---|---|---|
| "Are you struggling with high blood sugar?" | Personal attribute + disease name | "Many Americans are looking for ways to help support balanced glucose levels" |
| "Regulate erratic blood sugar with XYZ" | Definitive claim ("regulate") | "XYZ helps support erratic blood sugar" |
| "Why a spare tire increases death risk" | Sensational + scare tactic | "How does a spare tire impact health?" |
| "The ideal way to stabilize weight" | "The ideal" = only way | "An ideal way to support weight management" |
| "These 5 foods ruin women's metabolism" | Personal attribute + negative word | "Discover how 5 foods impact metabolism" |
| "Avoid these 5 foods at all costs" | Scare tactic + negative | "5 foods that may impact digestive health" |
| "If you don't take X, you'll gain weight" | Scare tactic + "you" + definitive | "How X may help support weight management" |

### Facebook vs YouTube Comparison
| Element | Facebook | YouTube |
|---------|----------|---------|
| Before/afters | Banned | Allowed |
| Zooming into body parts | Banned | Allowed |
| Aggressive claims | Heavily restricted | More lenient |
| Scrutiny level | High (especially ingestibles) | Lower |
| Language tone | Must be positive/neutral | Can be more direct |

## Google Ads (Light Coverage)
- **Prohibited:** medical claims, "free trial," "miracle cure," "unproven remedy"
- **All claims must be supported by scientific evidence**
- **Bait-and-switch:** Landing page must align perfectly with ad
- **Consequences:** Immediate account suspension without warning; potential permanent ban
- Google is less nuanced than Meta — they tend to ban first, ask questions never

## TikTok (Light Coverage)
- **Mandatory commercial content disclosure** for all promotional posts
- **Claims must be proven** with in-frame disclosures
- **Medical props or "biometric imagery" banned**
- **Hormone-related keyword ads removed**
- **Supplement advertisers must show regional certification** before approval
- More focused on disclosure requirements than language policing

## YouTube (Light Coverage)
- **More lenient than Facebook** — before/afters allowed, more direct claims
- **Same FTC rules apply** — no deceptive claims, income disclaimers required
- Many things banned on Facebook are fine on YouTube
- Still: no outright false claims, no medical diagnosis language

## ClickBank (Light Coverage)
- **Never use "lifetime"** for lifetime access
- **No personalized coaching/services claims** that cannot be delivered at scale
- **Cannot claim specific income** from techniques taught
- **Reasonable assumption:** Average person can achieve supplemental income with effort
- **Sales pages must clearly explain what customers receive**
- **Salesmanship encouraged, but do not over-embellish**

---

# FDA Language Rules (Health/Supplement Specific)

For health and supplement copy, FDA rules apply on top of platform rules:

- **Cannot claim to treat, cure, diagnose, or prevent** any disease
- **Structure talk is OK:** Describe anatomy and body functions ("supporting healthy liver function")
- **Function talk is OK:** "Helping brain function in a healthy way"
- **Conditional language required:** "may," "can," "helps support"
- **Abstract nouns safe:** Happiness, wellness, vitality, freedom (cannot be measured = cannot be disputed)

**Specific FDA language flags:**
- "High blood sugar" → use "erratic blood sugar"
- "Blood sugar spike" → use "blood sugar fluctuations"
- "Managing your blood sugar" → use "sustaining your blood sugar"

**Pro tip:** Read FDA warning letters — they show the exact language the FDA does not like. These are essentially a cheat sheet for what to avoid.

---

# The Compliance Philosophy

Compliance is a creative constraint that produces better copy. When you cannot rely on hype, you need:
- Better stories
- Stronger mechanisms
- More credible proof
- More nuanced emotional appeals

The best modern DR copy is MORE sophisticated because of compliance. Smart copywriters treat compliance as a competitive advantage — those who understand it can scale while others get banned.

**The golden rule:** Write for conversion, then edit for compliance. Do not let compliance thinking kill the creative process — get the persuasive draft right first, then run it through this checklist.

**Being compliant and being persuasive are not mutually exclusive.** The best copy does both.
