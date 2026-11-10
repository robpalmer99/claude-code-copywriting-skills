# Voice-of-customer sources for angle finding

Where to get real customer language, in order of value, and how to get it without a paid scraping tool. The angle-finder skill reads this file when it needs a source method.

## 1. First-party data (live offers)

The best seeds are the ones only you have. Ask for them before searching anywhere else.

| Source | What it gives you | How to get it |
|---|---|---|
| Post-purchase survey | Why they bought, what they tried before, what nearly stopped them | Export from the survey app (KnoCommerce, Fairing, Typeform) or a Google Sheet; paste the new rows |
| Comments on your own ads | Objections, in volume, by frequency | Export from Ads Manager or copy the comment threads on the top three ads |
| Support tickets | The question they ask after buying, which is the objection they had before buying | Export the last 30 days, or the tags the support team already uses |
| On-site reviews | What worked, what disappointed, the words they use for the result | Judge.me, Okendo, Loox, Yotpo export |

Method: read only the rows added since the last run. Generate Direct angles in the customers' own language and keep the verbatim quote on the card. Run comment mining as a separate objection pass: cluster by frequency, and turn the top three objections into answer-the-objection angles. Treat it as a recurring job, weekly or per creative sprint.

## 2. Reddit via the PullPush archive

Reddit blocks live scraping for most tools. PullPush is a free public archive with a Pushshift-style API that returns full comment bodies, subreddit and author.

```
https://api.pullpush.io/reddit/search/comment/?q=<phrase>&subreddit=<sub1,sub2>&size=100
https://api.pullpush.io/reddit/search/submission/?q=<phrase>&subreddit=<sub>&size=100
```

Useful parameters: `q` (search phrase), `subreddit` (comma-separated), `size` (max 100), `after` and `before` (epoch seconds) to window the search, `sort=desc`.

How to use it well:

- Write four to eight search phrases in the prospect's own words: pains ("can't sleep past 3am"), fears, failed attempts ("tried magnesium"), wishes.
- Target the subreddits where the avatar actually posts, not the category subreddit. A retiree with money worries posts in r/retirement and r/povertyfinance, not r/personalfinance.
- For demographic themes, filter the results for avatar keywords (age, life stage). For themes like "scam burnout" or "wish I could", relax the filter to context words, because those posts rarely state an age.
- Save the raw harvest as a markdown file beside the angle deck, with the subreddit and a date on each quote, and mine it for Direct angle seeds and for the voice-of-customer section of the offer brief.

## 3. Competitor and category reviews

| Source | Quality for angles | Access |
|---|---|---|
| Amazon reviews | High: product experience and emotion, exact objections | Blocks scraping; read by hand, or use a review-export tool if subscribed |
| Quora | High: the question behind the search, long answers in plain language | Blocks scraping; read by hand |
| YouTube comments | Medium to high: reactions to a framing, what viewers push back on | `yt-dlp --write-comments <url>` gives a JSON file of comments |
| Trustpilot | Low for angles: skews to shipping, billing and service | Blocks scraping |
| App stores, Steam, Hacker News | Medium, depending on product | Open APIs or hand reading |

Read the one-star and three-star reviews first. Five-star reviews give you the benefit language; one-star reviews give you the objection and the failed promise, which is where the Contrarian and Hidden Cause angles come from.

## 4. Research sources (Direct and Translocate)

- **ScienceDaily** and university press releases: mechanism-grade claims in plain English, with the paper linked.
- **Google Scholar** and pre-print servers: for the actual numbers, so the overclaim check in Step 5 has something to check against.
- **News and long-form features** in unrelated fields: the usual Translocate seed. A hospital whose cooling failed in a heatwave, an ecosystem that recovered after one species returned, a sports team that changed when it trained, a piece of infrastructure that failed for a reason nobody expected.

For every seed, record the claim close to verbatim and the source. The card's `Source claim` field must be faithful; the `Sample ad opener` is where the sharpening happens, and the gap between the two is what the overclaim check reads.

## 5. Clustering the harvest

Before writing cards, cluster every quote into one of four drivers and weight by frequency:

| Driver | What it sounds like | Angle types it feeds |
|---|---|---|
| Pain | "I'm so tired of…", "nothing has worked" | Hidden Cause, Deficiency |
| Objection | "sounds like a scam", "too expensive for what it is", "I've tried that" | Contrarian, Differentiation |
| Desire | "I just want to…", "imagine if…" | Identity, Timing/Method |
| Trigger | the event that made them search: a diagnosis, a birthday, a photo, a comment | Timing/Method, Identity |

Name two or three sub-avatars from the top clusters, each with its buying trigger, and write the Direct cards to those people rather than to the category.
