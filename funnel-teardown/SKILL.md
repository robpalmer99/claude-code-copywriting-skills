---
name: funnel-teardown
description: Tear down a LIVE competitor funnel or video ad from a URL, or structurally model a proven page into fresh copy for your own offer. Mode A walks the whole funnel (ad, pre-sell, sales page, checkout), critiques each page above and below the fold and flags congruency breaks. Mode B swipes a video ad scene by scene for recreation. Mode C models a proven page's structure and persuasion architecture into new, original copy for your offer with a MANDATORY compliance gate. Use when the user says "tear down this funnel", "break down this funnel", "what is this funnel doing", "swipe this video ad's structure", "analyze this competitor's funnel", or "clone / model / rebuild this page for my offer", or pastes a competitor funnel, ad or lander URL. For copy from scratch use direct-response-copy; for a single page saved as a swipe just save it.
---

# Funnel Teardown

On-demand teardown of any **live** competitor funnel or video ad, producing a study-ready breakdown. Three modes. A and B **analyse** a competitor and produce a breakdown. C **generates** copy for your own offer by modelling a proven page's structure, and it's the only mode that writes copy.

Pick the mode by intent and by what the URL is:

- "tear down / break down / CRO this funnel" plus a URL: **Mode A**
- "swipe this video ad's structure": **Mode B**
- "clone / rebuild / model this page for my offer": **Mode C**

## Mode A: live funnel teardown

### A1. Map the funnel

Start at the given URL (an ad, an advertorial or a lander) and walk the path a buyer takes: pre-sell or advertorial, sales page or VSL, checkout, then bumps and upsells if they're reachable. Fetch each page with whatever web tooling you have. Built-in web fetch covers most pages; if a crawler such as firecrawl is installed, prefer it for JS-rendered pages and multi-step flows. For a VSL, get the transcript if captions or a download are available; if the video can't be captured, say so rather than inventing its content.

Note where the trail goes cold (a checkout behind a paywall, gated upsells) and say so. Don't invent steps.

### A2. Critique each page, above and below the fold

For every page in the funnel, split the review:

- **Above the fold:** hook and headline, the promise, the visual, and the immediate "am I in the right place?" congruency with the ad or page that sent the visitor here.
- **Below the fold:** mechanism, proof, offer build, objections handled, CTA and close, urgency and risk reversal.

Flag **congruency breaks** explicitly: an ad about X landing on a page about Y, a mechanism named one way in the ad and another way on the page, a price or guarantee that changes between steps, a product-aware ad landing on a blind pre-sell. These are the highest-leverage leaks in most funnels, and they're invisible when each page is reviewed on its own.

### A3. Prioritise and grade

- List the biggest issues in **priority order**, by impact on conversion, not by how wrong they are.
- Note what's **working**. A teardown that only criticises misses the moves worth learning from.
- Give a short verdict, with a read of the awareness and sophistication stage the funnel is built for.
- Judge the funnel on the right register. A branded commerce funnel is allowed a lighter voice; a direct-response funnel lives or dies on mechanism, specificity and proof. Don't grade one on the other's axis.

### A4. Save the breakdown

Write to a dated file, for example `teardowns/<brand>-<funnel-type>-teardown-<YYYY-MM-DD>.md`, using the template in `references/output-templates.md`: funnel map, page by page (above and below the fold), congruency flags, what's working, priority fixes, verdict. Annotate **why** each move works or fails, so the file teaches rather than lists. Date it: live funnels change, and a teardown is a snapshot.

## Mode B: video ad swipe (scene by scene, for recreating the structure)

For a winning video ad you want to structurally recreate.

### B1. Get the transcript and frames

Get a transcript from captions, a download tool with caption support, or a paste from the user, and frames or screenshots at the beat changes if you can. If neither is available, ask the user to paste the transcript and describe the visuals; don't reconstruct an ad from memory.

### B2. Build the scene table

Build a scene-by-scene table aimed at recreation, with one row per beat:

| # | Timestamp | Spoken line | On-screen text | Visual / B-roll | Tone | Technique and why it works |

Then summarise the ad's **structure**: the opening hook type, the pattern of beats, the authority and proof devices, the CTA, the target audience, and the transferable template (hook, agitate, mechanism, proof, offer, CTA, or whatever the ad actually does). The goal is that a copywriter could rebuild the structure for a different product without copying a line.

### B3. Save as a swipe

Write to `teardowns/<brand>-video-ad-teardown-<YYYY-MM-DD>.md` with the scene table, the structure summary and the key frames if you saved them.

## Mode C: structural clone (generative, for YOUR offer)

Take a proven page and rebuild its **structure and persuasion architecture** as fresh copy for your own offer, with a compliance gate that most cloning tools skip. The output is a draft ready to hand to a page builder.

> **Model the structure, not the words.** Clone the section flow, the persuasion role of each beat, the offer model and the shape of the devices (the metaphor, the proof type, the urgency mechanism). Then write original copy for your offer. Never paste the reference's copy. That's plagiarism, not modelling.

### C1. Extract the reference skeleton

Scrape the reference page. Output a **wireframe, not a critique**. For each section in document order capture:

- **Persuasion role:** hook, hidden-mechanism reveal, problem agitation, fear amplification, solution tease, product introduction, how to get it, scarcity, exclusivity, price anchor, discount, risk reversal, CTA, emotional close.
- **Structural devices:** the mechanism metaphor, the proof type (testimonial, authority, demonstration, statistics), the urgency mechanism, and the **offer model** (paid product, free VSL, lead generation), because the offer model drives the re-mapping in C3.

### C2. Ground in your offer

Read your offer brief: mechanism, avatar, awareness and sophistication, proof, objections, price, guarantee. If there's no brief, build one from the product page and what the user tells you before writing a word, and say the brief is thin. The clone must be grounded in your offer, not in a bare product name.

### C3. Adapt the model and generate section by section

- **Re-map the offer model** where it differs from the reference. A paid-product page cloned for a free VSL turns the price, discount and refund sections into "watch the full video" and "nothing to lose by watching" equivalents.
- **Re-skin the devices for your market.** Map the reference's mechanism metaphor to yours. A "stuck smoke alarm" metaphor for tinnitus can become a "stuck smoke alarm" for financial worry; the shape transfers, the content doesn't.
- **Write each section** from the skeleton, filling it one to one from your brief. If the direct-response-copy skill is installed, use it for the writing; the skeleton tells it what each section has to do.

### C4. MANDATORY compliance and believability gate

Before emitting anything, run the generated copy through:

- the **compliance-checker** skill if installed (platform policy, banned claims, billing-term disclosure), or the equivalent check by hand against the platforms the page will run on; and
- a **believability check**: every claim has a source or a mechanism behind it, every proof element is real, and the urgency is true.

Strip, or hard-flag in a visible warning block, any of these: fabricated testimonials, fake live or viewer counts, invented comment feeds, unsupported income or health claims, dark-pattern timers. **Do not hand off copy that fails the gate without explicit, visible flags.** If the reference's persuasion depends on a non-compliant device, say so and propose a compliant substitute rather than cloning the violation.

### C5. Save

Write to `copy/<offer>-<reference>-structural-clone-<YYYY-MM-DD>.md`, formatted **section by section as clean markdown ready for a page builder**, each section labelled with its persuasion role, with the reference URL and the date noted at the top. This is a draft for your funnel, not a swipe. When it's tested, record the result at the top of the file so the next clone starts from what won.

## Discipline

- **Modes A and B are for study, not for helping a competitor.** Extract what's transferable to your offers.
- **Mode C models structure, not words.** Clone the architecture; write original copy.
- **Mode C's compliance gate is non-negotiable.** Never emit a clone that smuggles the reference's non-compliant devices through unflagged.
- **Live means perishable.** Date every file. Funnels and ads change.
- **Don't invent unreachable steps.** Say where the trail went cold.
- **Annotate the why.** A breakdown that lists pages without explaining the persuasion moves is a dump, not a swipe.

## Reference files

- `references/output-templates.md`: the Mode A breakdown template, the Mode B scene table, the Mode C skeleton table and the C4 gate checklist.
