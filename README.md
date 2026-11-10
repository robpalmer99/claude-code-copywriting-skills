# Claude Code Copywriting Skills

Eight free Claude Code skills for direct response copywriting — ad angles, static ad concepts, sales pages, Meta ads, landing pages, copy reviews, compliance checking, and funnel teardowns. Built on 40+ years of direct-response experience and **$523M+ in tracked campaign results**.

Created by **Rob Palmer** — [robpalmer.com](https://robpalmer.com)

> The full write-up, install walkthrough, and per-skill background lives at:
> **https://robpalmer.com/blog/claude-code-copywriting-skills**

## The skills

| Skill | What it does |
|---|---|
| [`angle-finder/`](./angle-finder/SKILL.md) | Find fresh ad angles, hooks and big ideas: mines real customer language and research, forces cross-domain bridges, and outputs scored angle cards ready for the writing skills. |
| [`direct-response-copy/`](./direct-response-copy/SKILL.md) | Write sales pages, VSLs, emails, headlines, CTAs — anything persuasive. Frameworks from Schwartz, Halbert, Ogilvy, Caples, Sugarman, Collier. |
| [`static-ad/`](./static-ad/SKILL.md) | Build a Meta static ad as one unit (copy + paired image brief from the same hook), then expand it with a locking variation matrix so a win is attributable. Includes a product-absent brief format for cold traffic. |
| [`ad-copy/`](./ad-copy/SKILL.md) | Write high-converting Meta (Facebook + Instagram) ad copy: primary text, headlines, UGC scripts, video ads. |
| [`landing-page-copy/`](./landing-page-copy/SKILL.md) | Write short-form bridge pages and pre-sell landers that sit between ads and VSLs/offers. |
| [`copychief/`](./copychief/SKILL.md) | Review sales copy the way a senior creative director would — line-by-line, with specific rewrites. |
| [`funnel-teardown/`](./funnel-teardown/SKILL.md) | Tear down a live competitor funnel page by page with congruency flags, swipe a video ad scene by scene, or model a proven page's structure into original copy for your offer behind a mandatory compliance gate. |
| [`compliance-checker/`](./compliance-checker/SKILL.md) | Audit ads, landing pages, VSLs, and emails against Meta/Facebook, Google, TikTok, YouTube, and ClickBank policies. |

## Install

Pick the skills you want. For each, copy the folder into your project's `.claude/skills/` directory:

```bash
git clone https://github.com/robpalmer99/claude-code-copywriting-skills.git
cp -r claude-code-copywriting-skills/direct-response-copy /path/to/your/project/.claude/skills/
cp -r claude-code-copywriting-skills/ad-copy             /path/to/your/project/.claude/skills/
# ...etc
```

Or copy individual `SKILL.md` files (and their `references/` folders, where present) by hand.

Claude Code auto-detects skills from `.claude/skills/`. The `description` in each `SKILL.md`'s YAML frontmatter triggers the skill automatically when you ask Claude something matching its purpose.

The `angle-finder`, `static-ad`, `ad-copy`, `compliance-checker` and `funnel-teardown` skills also include reference files (`references/voc-sources.md`; `references/hook-to-visual-patterns.md` and `references/product-absent-brief.md`; `references/meta-ad-specs.md`; `references/trigger-words.md`; `references/output-templates.md`). Keep those alongside `SKILL.md` inside each skill folder — the skill reads them automatically.

## Workflow

These skills are designed to chain:

0. **Find the angle** with `angle-finder` — scored angle cards from customer language and cross-domain research
1. **Draft** with `direct-response-copy` (long-form) or `ad-copy` (Meta ads) or `landing-page-copy` (bridge pages); for statics, `static-ad` pairs the copy with its image brief and runs the variation matrix
2. **Review** with `copychief` — line-level feedback with specific rewrites
3. **Comply** with `compliance-checker` before submitting paid ads
4. **Diagnose** a live funnel (yours or a competitor's) with `funnel-teardown`, and model a proven page's structure into original copy with its compliance gate

## License

CC-BY-4.0 — see [LICENSE](./LICENSE).

You can use, modify, and redistribute freely. Attribution is the only ask: link back to [robpalmer.com/blog/claude-code-copywriting-skills](https://robpalmer.com/blog/claude-code-copywriting-skills) when you share or adapt these.

## Contact

- Site: [robpalmer.com](https://robpalmer.com)
- Email: rob@gofreelance.com

If these skills help you write copy that converts or scale a winning campaign, a link back to the blog post is the only thing I ask.
