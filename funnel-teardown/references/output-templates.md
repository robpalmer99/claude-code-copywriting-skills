# Output templates for funnel-teardown

Use these shapes as written so every teardown and clone in a project is comparable. Fill every field or write "not reachable" or "unknown"; never leave a section implied.

## Mode A: live funnel teardown

```markdown
# <Brand>: <funnel type> teardown

Date: <YYYY-MM-DD> (live snapshot; the funnel may have changed since)
Entry URL: <url>
Funnel type: <ecom | quiz | vsl | advertorial | info-product | call funnel | lead gen>
Market: <market> · Built for: <awareness stage> / <sophistication stage>
Register: <direct response | branded commerce>

## Funnel map
1. <Ad or entry> → 2. <Pre-sell / advertorial> → 3. <Sales page / VSL> → 4. <Checkout> → 5. <Bump / upsells, or "not reachable">

## Page by page

### 1. <Page name> (<url>)
**Above the fold**
- Hook / headline: <quote, under 15 words> · <what it promises>
- Visual: <what's shown>
- Congruency with the previous step: <PASS | BREAK: how>
**Below the fold**
- Mechanism: <named? how?>
- Proof: <types, and whether they're credible>
- Offer build: <price, bundle, guarantee, bonuses>
- Objections handled: <which, and which are missing>
- CTA and close: <verb, placement, urgency device>
**Why it works / fails:** <two or three sentences on the persuasion move, not the layout>

(repeat per page)

## Congruency flags
- <Step X → Step Y>: <what breaks: promise, mechanism name, offer numbers, awareness hand-off, CTA verb, compliance parity>

## What's working
- <the moves worth learning from, with why>

## Priority fixes (by impact on conversion)
1. <fix> · <the leak it closes>
2. …

## Verdict
<Three to five sentences: what the funnel is, who it's built for, the single biggest leak, the single best move.>
```

The six congruency rows to check at every hand-off: **promise** (does the page continue the ad's sentence?), **mechanism name** (identical string, not a synonym), **offer numbers** (price, discount, guarantee length, shipping, "X days" all match exactly), **awareness hand-off** (the level the visitor leaves at versus the level the next page assumes), **CTA verb** ("Shop now" lands on a buy box, "Learn more" on a pre-sell, "Watch" on a player), and **compliance parity** (the page escalates nothing the ad avoided).

## Mode B: video ad scene table

```markdown
# <Brand>: video ad teardown

Date: <YYYY-MM-DD> · Source: <url> · Length: <m:ss> · Platform: <Meta | YouTube | TikTok>
Target audience: <who> · Awareness: <stage>

| # | Time | Spoken line | On-screen text | Visual / B-roll | Tone | Technique and why it works |
|---|---|---|---|---|---|---|
| 1 | 0:00 | … | … | … | … | … |

## Structure
- Opening hook type: <curiosity | contrarian | social proof | story | demographic callout | result | pattern interrupt>
- Beat pattern: <e.g. hook → agitate → mechanism → proof → offer → CTA>
- Authority and proof devices: <list>
- CTA: <verb and destination>
- Transferable template: <the beat sequence written so it could be rebuilt for another product>
```

## Mode C: reference skeleton

```markdown
# Skeleton of <reference page>

Date: <YYYY-MM-DD> · URL: <url> · Offer model: <paid product | free VSL | lead gen> · Target offer model: <ours>

| # | Section (as it appears) | Persuasion role | Devices (metaphor, proof type, urgency) | Re-map for our offer |
|---|---|---|---|---|
| 1 | <headline block> | hook | <curiosity + authority> | <keep / change / drop, and how> |
| 2 | … | … | … | … |
```

Then the draft, one block per row, labelled with the persuasion role:

```markdown
## 1. Hook
<original copy for our offer>

## 2. Hidden-mechanism reveal
<original copy for our offer>
…
```

## Mode C: the C4 gate checklist

Run before handing off. Every item is a stop until it's fixed or visibly flagged.

- [ ] No testimonial, review or quote that isn't real and attributable.
- [ ] No live counters, viewer counts, "people watching now", comment feeds or notification pop-ups that aren't live and true.
- [ ] No income, health, weight or performance claim without a source, a mechanism and the qualifiers the platform requires.
- [ ] No countdown timer or scarcity line that resets, repeats or isn't true.
- [ ] Billing terms (subscription, trial, auto-ship, cancellation) disclosed where the platform and the law require.
- [ ] Every number on the page matches the offer brief: price, discount, guarantee length, shipping.
- [ ] Any device the reference's persuasion depended on that fails the above is replaced with a compliant substitute and the substitution is noted at the top of the file.
