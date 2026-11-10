---
name: angle-finder
description: Generate fresh ad angles, hooks and big ideas for a product or offer by mining real customer language and research, then forcing cross-domain bridges (the translocation method). Use whenever the user wants new angles, hooks, big ideas, ad concepts or "ways in" for an offer, e.g. "find angles for [offer]", "I need fresh hooks for [product]", "what angles haven't we tried", "mine these reviews / survey responses / ad comments for angles". Produces scored angle cards (source claim, bridge, big idea, sample ad opener) saved to a file, ready to hand to the ad-copy, landing-page-copy or direct-response-copy skills. Do NOT use it to write finished ads or pages; those skills do that.
---

# Angle Finder

Turns a product or offer into a deck of **scored angle cards** by researching where the customer actually talks, researching outside the niche, and bridging back in. The deliverable is two or three breakout angles the market has not seen, not a big pile. Cull hard.

An **angle** is the way into the sale: the belief, the enemy, the mechanism or the story the ad leads with. Most accounts die from running the same three angles with new footage. This skill exists to find the fourth.

## When to use

- "find angles / hooks / big ideas for [offer]"
- "run angle finder on [product or URL]"
- "I need fresh ways into [market]"
- "what angles haven't we tried for [offer]"
- "mine our reviews / post-purchase survey / ad comments for angles"

## Inputs to gather first

1. **The offer.** Read whatever exists: an offer brief, the product page, the current best ad, the landing page. Extract the mechanism, the avatar, the price, the awareness and sophistication of the market, and what has already been run. If only a URL is available, fetch it and extract the basics, and say the brief is thin.
2. **Strategy.** **Direct**, **Translocate**, or **both**. Default to both, run as two passes.
3. **Count.** Default 20 to 26 cards in total, split across the passes. Fewer with a thin brief.
4. **Market.** For health, supplements and finance, weight the research sources and tighten the overclaim check in Step 5.
5. **Burned angles.** Ask what has been tested. Never regenerate an angle the account has already run and lost with.

## The two strategies

| Strategy | Research targets | Yields |
|---|---|---|
| **Direct** | On-topic to the product: the mechanism, the category, the condition, the ingredient, the activity, and above all the customer's own words | Believable angles; the mechanism lives inside the category |
| **Translocate** | Deliberately unrelated domains: physics, history, ecology, computing, sport, ancient practice, a news story | Breakout angles; a borrowed mechanism that feels new because nobody in the niche runs it |

The translocation move, in one line: pull a real, citable claim from a domain that has nothing to do with the product, then answer the question "how could this possibly relate to what we sell?" The answer is the angle, and the category mismatch is itself the curiosity loop. (Stefan Georgi's term for the move is translocation; his example is a self-organising principle in quantum physics bridged to cellular energy, so a supplement ad can open on what tired cells and burning stars have in common.)

## Workflow

### Step 1: Load context

Read the brief or the page. Write down, in a few lines at the top of the run file: mechanism, avatar, awareness stage, sophistication stage, price, and the angles already run. Everything downstream is judged against these lines.

### Step 2: Source the seeds

A seed is one real claim, quote or fact, with its provenance. Collect seeds from the sources below, in this order of value.

**First-party voice of customer (live offers only, and the best source there is).** Ask for these before going anywhere else:

- Post-purchase survey responses: what made them buy, what they had tried before, what nearly stopped them.
- Comments on the brand's own ads, exported from the ad platform or pasted in. Every repeated objection is a candidate for the next ad to answer.
- Support tickets and on-site reviews.

Read only the rows added since the last run so the angles stay fresh. Generate the Direct angles in the customers' own language, and keep the verbatim quote that inspired each card in its `Source claim` field. Run comment mining as a separate objection pass: cluster objections by frequency and turn each of the top three into an answer-the-objection angle. A customer's own words are also the safest phrasing source for compliance, though a quote describing a health outcome is still a claim and still goes through a compliance check.

**Reddit.** Lived experience, failed attempts, contrarian takes, and the exact phrases prospects use. Live scraping of Reddit is blocked for most tools, so use the free PullPush archive API instead, which returns full comment bodies with subreddit and author:

```
https://api.pullpush.io/reddit/search/comment/?q=<phrase>&subreddit=<sub>&size=100
```

Pick four to eight search phrases in the prospect's own words (pains, fears, failed attempts, wishes), target the subreddits where the avatar actually posts, and save the raw harvest alongside the run file. See `references/voc-sources.md` for the full method and the other review sources.

**Competitor reviews.** Amazon, Trustpilot, Quora and app-store reviews carry buyer language Reddit lacks: what worked, what failed, the exact objection to a specific product. Amazon, Quora and Reddit skew toward product experience and emotion; Trustpilot skews toward service and logistics and is weaker for angles.

**Research and science.** ScienceDaily, Google Scholar, pre-print servers and university press releases, for mechanism-grade claims. Essential for health and science offers, where the mechanism has to survive a sceptical reader.

**YouTube and podcasts.** Trending, well-viewed framings of the problem, and the comments beneath them.

For **Direct**, search on-topic terms. For **Translocate**, pick four to six deliberately unrelated, well-trafficked topics (a trending science story, a historical event, a sports method, a piece of infrastructure, a nature mechanism) and find one real claim in each.

Capture for every seed: the claim, close to verbatim, and where it came from.

### Step 2b: Cluster before you write

Don't leave the quotes as a flat list. Cluster them into **pain, objection, desire, trigger**, weight each cluster by how often it recurs (repeated pains rise, one-off anecdotes fall), and keep each quote's source attached. From the top clusters, name two or three **sub-avatars with a buying trigger**, for example "the 3am negotiator: has tried every routine, now needs proof before trying another". Write the Direct cards off the top-ranked drivers, so the deck is evidence-led rather than taste-led.

### Step 3: Force the bridges and write the cards

For each seed, write one angle card. Aim for about five cards per strong seed. Use this exact schema so the next skill can consume the card directly:

```markdown
### NN. <Headline: the angle as a scroll-stopping line>

`<Angle | Hidden angle>` · Bridge distance: **<Conservative | Moderate | Aggressive>** · Types: <Hidden Cause, Identity, Contrarian, Timing/Method, Deficiency, Differentiation> · Awareness: <unaware | problem | solution | product>

- **Source claim:** <the real external claim or customer quote, faithful to the source>
- **Bridge:** <how it connects to THIS offer; the connective logic>
- **Big idea:** <the ownable reframing the prospect has never heard>

> Sample ad opener
> <the hook written out, two to five sentences, in-market voice>

- **Momentum signals:** <why now: recency, trend alignment, adjacent awareness already in the market>
- **Awareness reasoning:** <why this framing is fresh for this market at its sophistication stage>
- **Source:** <title, URL or citation>
```

Card types, for the `Types` field:

- **Hidden Cause**: the real reason the problem persists, which the prospect has never been told.
- **Identity**: who the prospect is or wants to be, and what this product says about them.
- **Contrarian**: the opposite of what the market has been told.
- **Timing/Method**: the same goal reached by a new when or how.
- **Deficiency**: something the prospect is missing and did not know mattered.
- **Differentiation**: why this product and not the category.

### Step 4: Score and cull

Give each card a **0 to 10** score for believability, freshness and fit to the avatar, and show the score. Mark the genuinely novel-for-market cards as `Hidden angle`. Then **call the top three explicitly**, one line of rationale each. This is the deliverable the user acts on. Be honest: most cards are mediocre, and the run is a success if two or three are not. Thumbs down freely.

### Step 5: Overclaim check

Translocated claims come from real studies and the punchy version usually overstates them. For every card, compare the sharpened hook against the source claim and flag any specific number, causal statement or outcome that outruns it in a clearly marked **Warning** block under the card. Critical for health and finance. If the compliance-checker skill is installed, say so and offer to run the top three through it.

### Step 6: Save the deck

Write the deck to a file in the project, for example `angles/<offer>-angles-<YYYY-MM-DD>.md`, with:

1. A one-paragraph method note: strategy used, sources, how many seeds, what was excluded as burned.
2. The **top-three call**.
3. The **overclaim warnings** gathered in one place.
4. A **score summary table**: card number, headline, type, bridge distance, score.
5. The cards.

Keep the raw voice-of-customer harvest in a sibling file so the next run can read only what's new.

### Step 7: Chain

Offer the next step: "write three Meta ads for angle 4", "write a 500-word advertorial lead for angle 9", "write the pre-sell page for angle 2". Hand the card to the ad-copy, landing-page-copy or direct-response-copy skill, with the card pasted in full so the source claim and the bridge travel with the hook. When an angle gets tested, record the result next to the card so the next run knows what won.

## Discipline (do not skip)

- **The win is two or three breakout angles, not a big pile.** Score and cull ruthlessly.
- **Translocate is where the breakouts live.** Don't let every card collapse back to on-topic claims.
- **Customer language beats cleverness.** If a first-party quote and a translocated science claim compete for the same slot, the quote wins for a product-aware market and the claim wins for an unaware one.
- **Always fact-check the sharpening.** A great emotional angle on an overstated number is a compliance liability, not a win.
- **Keep it chain-ready.** The card schema exists so the next skill can consume an angle directly. Don't improvise the format.
- **Never regenerate a burned angle.** Ask what has been run, and read the previous decks in the folder.
