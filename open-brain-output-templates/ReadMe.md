# Open Brain Output Templates

Three self-contained HTML report templates for turning an "Open Brain" shared memory layer into scheduled, human-readable intelligence briefs: a Daily Brief, a Weekly Digest, and a Monthly Executive Summary.

These are the sanitized templates that accompany the Recalibrated guide **From Capture to Clarity: Building Automated Intelligence Reports from Your Open Brain**. The post walks through the design principles, the two delivery approaches, and the scheduling setup in full. This folder is just the code, ready to copy and adapt.

Read the guide for context: [From Capture to Clarity](REPLACE_WITH_POST_URL)

> Replace the link above with the live Substack URL once the post is published.

## What's in this folder

```
daily_brief_template.html      Tactical morning brief (priorities, open action items, business pulse)
weekly_digest_template.html    Operational Monday review (status cards, pipeline movement, decisions)
monthly_summary_template.html  Board-ready strategic report (executive summary, deep dives, patterns)
```

Each file is a complete HTML document. Open any of them in a browser to see the rendered layout with placeholder content in place.

## The three cadences

The templates are built around the idea that daily, weekly, and monthly summaries serve different purposes, so each has its own structure rather than reusing one layout at three intervals.

The **Daily Brief** is tactical: today's top priorities, every open action item with age and status, yesterday's captures, follow-up contacts, and a one-line pulse per business entity. The **Weekly Digest** is operational: a narrative summary of the week, status cards per entity, pipeline movement, decisions made, aging action items, and relationship activity. The **Monthly Executive Summary** is strategic: an executive narrative, a deep dive per entity, decisions with reasoning, synthesized pattern observations, and next-month priorities.

## How the templates work

Every template follows the same conventions so an AI agent can populate them reliably:

**Self-contained HTML.** Inline CSS, no external dependencies beyond a single Google Fonts import. The files render identically in any modern browser and can be emailed as attachments without breaking.

**Descriptive placeholders.** Every placeholder states what belongs there, for example `[ACTION DESCRIPTION from Open Brain]` or `[ACTION ITEM from Open Brain, status: open]`, not a bare `[ITEM]`. The label is the instruction to the agent, which makes the templates close to self-documenting when you drop them into a prompt.

**Never invent.** If a field has no matching data in your Open Brain, the correct fill is `Not captured this period.` rather than a fabricated value. A partially filled brief is honest and stays trustworthy. An invented one erodes confidence in the whole system.

## Customizing

All three templates share one design system defined with CSS custom properties at the top of each file. Edit the `:root` variables once and the change propagates through the document. The main groups you will want to set are your brand colors, a color per business entity, and the status indicator colors:

```css
:root {
  /* Brand colors */
  --navy:   #1A3A5C;   /* Header, titles */
  --blue:   #2E75B6;   /* Accents, arrows */

  /* Business color coding, customize to your entities */
  --biz1:   #7C3AED;
  --biz2:   #2563EB;
  --biz3:   #E55A2B;

  /* Status indicators */
  --urgent: #DC2626;   /* Aging or overdue */
  --active: #D97706;   /* In progress */
  --good:   #059669;   /* On track */
}
```

## Using them with an AI agent

The guide describes two ways to get these templates in front of a scheduling-capable agent. In short:

**Option A, embed the template in the prompt.** The full HTML lives inside the scheduled task instruction. The agent queries your Open Brain, populates the template, and outputs the finished HTML. Simplest to set up, no file system dependencies, at the cost of a larger job payload (roughly 15 to 18 KB).

**Option B, store the template as a local file.** The agent reads the file at the start of each run, then populates and outputs it. The job definition stays small (roughly 2 to 3 KB) and all jobs share one source of truth, at the cost of requiring file access. Best once you iterate on the templates often.

The recommendation in the guide is to start with Option A, confirm output quality end to end, then migrate to Option B if you find yourself editing templates frequently. Scheduling specifics (cron expressions, job structure, and where an OpenClaw agent stores its jobs) are covered in the post.

## A note on sanitization

These are genericized versions. Business-specific names are replaced with Business One, Business Two, and Business Three, people are replaced with generic roles, and locations are genericized. Before wiring them into your own pipeline, swap in your real entities and colors, and make sure nothing identifying (project references, keys, internal URLs) ends up committed alongside your working copies.

## License

Released under the MIT License. Copy, adapt, and reuse freely. See [LICENSE](LICENSE) if present in the repository root.

## Credits

Concept credit to Nate B Jones for the Open Brain idea. Templates and guide by Thomas Jochim, published on https://the2act.substack.com/, dispatches from building companies in the AI era.
