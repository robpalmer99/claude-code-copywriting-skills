---
name: static-ad
description: Build a complete static ad CONCEPT for Meta (Facebook and Instagram), with the hook, headline, description and the paired image direction as one creative unit, then expand it with a locking variation matrix (lock the copy and vary the image, lock the image and vary the copy, or full refresh). Use when the user says "make a static ad", "static ad concept", "create ad variations", "lock the copy and try new images", "give me five variations of this ad", "vary the visual", or wants paired copy and creative for a static ad rather than copy alone or an image alone. Orchestrates the ad-copy skill for the words and writes a model-agnostic image brief for whatever image generator or designer you use. For copy only use ad-copy; for a compliance pass use compliance-checker.
---

# Static Ad (concept + locking variation matrix)

Produce a **static ad as one coherent creative unit**: primary text, headline, description and the paired image, from one brief. Then expand it into a test set with an explicit **locking variation matrix**, so when a variation wins you know which half won.

Most teams run copy and image as two separate jobs. The writer produces hooks, the designer produces pictures, and the pairing happens in the ad builder at the last minute. This skill makes the pairing the first decision, not the last.

> This is an orchestrator. The copy is written by the **ad-copy** skill if it's installed (call it with the brief from Step 1; if it isn't installed, write the copy here using the same brief). The image is described as a **reasoning brief** in Step 2 that any image model (gpt-image, Gemini, Midjourney) or a human designer can execute. This skill owns the concept, the pairing, the variation matrix and the naming.

## When to use vs neighbours

- **This skill:** a finished static ad concept (copy and image together) and a structured set of test variations.
- **ad-copy:** copy only, including UGC and video scripts.
- **angle-finder:** you don't have an angle yet. Run it first; a static ad is only as good as the angle it's built on.
- **compliance-checker:** platform policy pass. Run it after.

## Step 1: Load context

1. **Read the brief.** An offer brief if one exists, otherwise the product page, the current best ad and anything the user gives you. Pull the mechanism, the avatar, the awareness and sophistication of the market, the big idea, the objections and any angle deck.
2. **Pin the four inputs.** Ask only for what's missing; infer the rest from the brief.
   - **Funnel stage:** cold, warm or retargeting.
   - **Awareness level:** unaware, problem, solution, product or most aware.
   - **Visual style:** the look. "Candid phone photo", "clean branded studio", "documentary portrait", "editorial still life".
   - **Pain point or angle:** the one thing this concept calls out.
3. **Decide the strategic axis.** **Sell the click** (short caption, curiosity image, send to an advertorial or VSL) or **sell the solution** (more on the image, product-aware, send to a product page). Showing the product in the image makes the viewer product-aware, which changes where the click should go.
4. **Decide product-present or product-absent.** For cold traffic in a claim-exhausted market, a bottle in frame reads as retargeting and gets scrolled. `references/product-absent-brief.md` is the method for statics that sell the recognition instead of the SKU.

## Step 2: Generate the seed concept (copy and image as one unit)

One brief, one complete concept. The copy comes first and the image is built from it, never the reverse.

1. **Copy.** Produce the single best hook as primary text, headline (27 characters for mobile) and description, anchored to the angle. One concept here; the variations come in Step 3, so the paired image has one clear thing to amplify.
2. **Classify the hook type**, because it decides the visual pattern. `references/hook-to-visual-patterns.md` has the full mapping with a brief template for each; the summary:

| Hook type | Visual pattern | Why it pairs |
|---|---|---|
| Curiosity | Close-up of an unfamiliar or partly obscured object | The viewer wants to know what it is; the image must not resolve it |
| Contrarian | Split-screen or a person breaking convention | Visual tension mirrors the copy's contradiction |
| Social proof | A real-looking person with a visible result | Credibility borrowed from a person like me |
| Story | An emotional face mid-moment, before the resolution | Narrative reflex; the open tension demands the click |
| Demographic callout | Direct eye contact, recognisable context for the target | "This is about me" recognition |
| Result | The transformation moment or its aftermath, felt not shown off | Aspiration made immediate |
| Pattern interrupt | Unexpected scale, colour or juxtaposition, otherwise clean | Breaks the feed's rhythm, and must connect to the angle |

3. **Propose two or three visual concepts** as plain-English sketches and let the user pick before anything is generated. Each sketch: what the camera sees, the composition move, the aesthetic register (phone candid, studio product, documentary portrait, cinematic) and one sentence on why it pairs with the hook.
4. **Write the reasoning brief** for the chosen concept as six short paragraphs of prose, not a keyword list: **Subject** (who or what, with physical specifics), **Action** (mid-gesture, state of being), **Context** (place, time of day), **Composition** (shot type, framing, depth of field, aspect ratio), **Lighting** (source, direction, quality, temperature), **Style** (medium, camera and lens, film stock or grade, references). Specify the camera and the colour grade every time; "shot on a Sony A7R IV, 85mm, Kodak Portra 400 grade" produces a better image than "photorealistic". Bake in at least two scroll-stopping levers: a face with eye contact, high contrast, a pattern interrupt, negative space, a peak-action freeze, and legibility at thumbnail size.
5. **Set the aspect ratio** for the placement. Feed: 4:5 (1080×1350) by default, 1:1 for cross-placement. Stories and Reels: 9:16 (1080×1920), with faces, objects and any text kept out of the top 250px and bottom 250px. Never 16:9 for a static.
6. **Generate or hand off.** Run the brief through whatever image model you use, with a reference photo if the ad needs a real person, a real product or a house style, or hand the brief to the designer as written. Don't put text in the generated image; add headline overlays in the ad builder or a design tool afterwards.
7. **Present as one card** so the unit is obvious. A batch gets a heading (`# <Offer>: <n> static concepts, <cold or retargeting>`), a **Goes to** line, an **Angles in this batch** line, the numbered cards, then `## Run these first` with three to five numbers and one sentence each once the batch has more than five concepts.

```markdown
## 01. <Concept name>
**Asset ID:** <the Step 5 key, e.g. sleepco_cooling-crash_A1_20261110>
**Angle:** <plain name> · <funnel stage> / <awareness> / sell-the-<click|solution>
**Image:** <one paragraph: what is in frame, the light, what is deliberately absent> · `assets/meta-ads/<file>.png`
**On the image:** <headline text on the image, if any>
**Primary text:** <opening lines to the click line>
**Headline:** <Meta headline, 27 characters for mobile>
**Description:** <one line>
**Ratio:** <4x5 / 1x1 / 9x16>
```

The reasoning brief, the "why it pairs" note, the awareness stage and the compliance findings go in a `<Batch> - Notes.md` file beside the cards, not on the card.

## Step 3: The locking variation matrix (the core move)

Don't regenerate everything every time. **Lock one half and vary the other**, so a win is attributable. Offer the mode explicitly:

| Mode | Locks | Varies | Use when |
|---|---|---|---|
| **New visual, same message** | copy | image only | The copy is winning; find the image that stops the scroll |
| **New copy, same visual** | image | copy only | The image is strong; find the message that converts |
| **Full creative refresh** | nothing | both, on a new angle | The whole concept is tired or you want a new direction |
| **Custom brief per variation** | per row | per row | Hand-directed variants ("same style, but a woman in her thirties") |

Discipline: **vary one level at a time** so you know what moved the needle. Default to five variations per request. The image levers, in order of impact: visual concept (woman at window versus close-up of the object), subject swap (same concept, different person or demographic), composition (close-up versus medium versus wide), colour grade (warm versus cool versus muted). When locking copy, pass the locked text verbatim and change only the visual concept, subject, composition or grade. When locking the image, reuse the same file (or the same reference image and brief) and rerun the copy only.

Label every variation with the concept it belongs to and the copy it pairs with:

```
A1  Concept A (story hook, woman at window)             pairs with copy A   story-A1-20261110.png
A2  Concept A, subject swap (older woman, same setting)  pairs with copy A   story-A2-20261110.png
B1  Concept B (close-up of journal and coffee)           pairs with copy B   curiosity-B1-20261110.png
```

## Step 4: Compliance pass

Run the concept, copy and image together, through the compliance-checker skill before it's test-ready, especially for supplement and health claims, subscribe-and-save terms and finance claims. The image is part of the claim: a before-and-after panel, a scale, a bank balance or a doctor's coat can fail review on its own. Note overclaims and offer compliant rewrites that keep the punch.

## Step 5: Name, save and make it traceable

The name ties the concept to its variations and, later, to its result.

`<offer-slug>_<angle>_<concept-letter><variation-n>_<yyyymmdd>`, for example `sleepco_cooling-crash_A1_20261110` (concept A, variation 1).

- Images go in `assets/meta-ads/`, filename = the key.
- The concept set and the matrix go in a dated markdown file in the project, with the brief it drew on linked at the top.
- Use the same key as the ad name when the ad is published, so the account's reporting traces back to the concept and the angle. When a variation wins, write the result next to its card; the next batch should start from what won.

## Discipline

- **Copy drives the image, always.** The hook exists before the visual. Never generate nice pictures and back-fit copy.
- **One concept, then lock and vary.** Don't change copy and image and angle in one variation; you lose attribution.
- **Ground in the brief, not a URL.** The concept is only as good as the angle it's built on. If there's no angle, run angle-finder first.
- **Two or three sketches before one image.** One concept with no alternatives is a unilateral creative decision on the user's behalf.
- **It's a creation tool, not a publishing tool.** Mass-publishing to Meta is a separate decision with its own naming and testing rules.

## Reference files

Load on demand, not at startup:

- `references/hook-to-visual-patterns.md`: the seven hook types mapped to visual patterns, with composition rules, don'ts, a brief template and variation levers for each.
- `references/product-absent-brief.md`: the brief format for cold-traffic statics with no product in frame, and the three standing directives that go with it.
