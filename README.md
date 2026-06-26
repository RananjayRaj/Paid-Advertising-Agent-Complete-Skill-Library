# Paid Ads Agent: Claude Skill Library

A collection of 15 Claude Skills that audit, improve, and scale paid ad campaigns across Google Ads, Meta Ads, and LinkedIn Ads. Each skill handles one specific task in the paid advertising workflow, from creative scoring to budget planning, so you can run a full account review without leaving Claude.

Built and tested by [Rananjay Raj](https://www.linkedin.com/in/rananjayraj/) across $500K+ in ad spend on 8 client accounts. Full write-up and results: [The AI-Driven Marketer](https://theaidrivenmarketer.beehiiv.com/p/paid-advertising-agent-complete-skill-library).

## What's inside

| Skill | Suite | What it does |
|---|---|---|
| `performance-max-auditor` | Google Ads | Grades PMax assets and flags what needs fixing |
| `google-ads-copy-generator` | Google Ads | Generates compliant headlines, descriptions, and extensions |
| `search-terms-analyzer` | Google Ads | Surfaces winning and wasted search terms from reports |
| `negative-keyword-miner` | Google Ads | Extracts negative keywords from search term data |
| `ad-performance-diagnostic` | Google Ads | Full account diagnostic with Quality Score and budget recommendations |
| `meta-ads-andromeda-auditor` | Meta Ads | Audits Advantage+ setup, signal quality, and learning stability |
| `meta-ads-audience-builder` | Meta Ads | Designs prospecting, lookalike, and retargeting audiences |
| `meta-ads-creative-brief` | Meta Ads | Generates creative briefs for designers and UGC creators |
| `meta-ads-creative-analyzer` | Meta Ads | Scores Meta creatives on hooks, visuals, copy, and CTAs, and flags fatigue |
| `linkedin-ads-audience-builder` | LinkedIn Ads | Builds high-intent B2B audiences from your ICP |
| `linkedin-ads-copy-generator` | LinkedIn Ads | Writes LinkedIn ad copy tuned for B2B tone and format limits |
| `linkedin-ads-creative-analyzer` | LinkedIn Ads | Scores LinkedIn creatives on persona fit, funnel stage, and lead quality |
| `media-planner` | Strategic Planning | Builds budget allocation, channel mix, and KPI forecasts |
| `creative-testing-framework` | Strategic Planning | Designs A/B test matrices with hypotheses and sample sizes |
| `creative-testing-insights-reporter` | Strategic Planning | Turns test results into design principles and playbooks |

Each `.skill` file is a self-contained package: a `SKILL.md` with the workflow instructions, a `README.md` with usage notes, and a `references/` folder with frameworks, benchmarks, and output templates the skill loads on demand.

## Getting started

### Prerequisites

- Claude Pro, Team, or Enterprise account
- Ad platform access (Google Ads, Meta Ads Manager, LinkedIn Campaign Manager) for live data
- Basic familiarity with paid advertising metrics

### Installation

1. Download the `.skill` file for any skill above (or grab the full `Paid Ads Agents.zip` bundle).
2. In Claude, go to **Settings > Capabilities > Skills** and upload the file. For Claude Code or Cowork, drop the unzipped folder into your skills directory.
3. Each skill triggers automatically when your prompt matches its description, or you can call it by name.

### Best practices

- Run audits weekly, Monday mornings work well for most accounts.
- Keep a tracking sheet of changes so you can compare month over month.
- Chain skills together: an audit skill's output feeds directly into a copy or creative-brief skill.
- Start with one platform suite before running the full stack across all three.

## Example weekly workflow

**Monday:** Run `performance-max-auditor`, feed results into `google-ads-copy-generator`, launch new variations.

**Tuesday:** Run `search-terms-analyzer`, pass findings to `negative-keyword-miner`, implement immediately.

**Wednesday:** Run `meta-ads-andromeda-auditor` and `meta-ads-creative-analyzer`, brief the designer with `meta-ads-creative-brief`.

**Thursday:** Run `ad-performance-diagnostic` across all platforms, reallocate budget based on recommendations.

**Friday:** Review the week's outputs, prioritize the top 3 fixes, plan next week's allocation with `media-planner`.

## Skill structure

Each skill follows the same layout:

```
skill-name/
├── SKILL.md              # Frontmatter (name, description) + workflow instructions
├── README.md              # Usage notes and example prompts
└── references/            # Frameworks, benchmarks, and templates loaded on demand
```

`SKILL.md` frontmatter contains only `name` and `description`, kebab-case naming, and no extra keys, so these install cleanly on any platform that supports the open Skills standard (Claude, and increasingly ChatGPT, Gemini, and others via [agentskills.io](https://agentskills.io/home)).

## Contributing

PRs welcome for new platform support (TikTok Ads, Pinterest Ads, etc.), bug fixes, or improvements to existing frameworks. Open an issue first for larger changes.

## Support

Questions or feedback: DM [@Rananjay_RajW](https://x.com/Rananjay_RajW) on X or [Rananjay Raj](https://www.linkedin.com/in/rananjayraj/) on LinkedIn.

## License

MIT
