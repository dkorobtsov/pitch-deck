# pitch-deck

> A Claude Code plugin that builds investor-grade pitch decks through narrative-first methodology — story before slides, writing before design, meaning before data.

Most pitch decks fail before investors read a single bullet point. The headlines say "Team," "Market," "Financials" — and the investor's pattern-matching brain files it under "generic." This plugin forces a different approach: every headline is a message, every slide earns its place, and the complete headline sequence tells a compelling story even without body text.

## What it does

### `/create` — Build a pitch deck from scratch

Runs a structured founder interview (12 questions, one at a time), then builds the deck through 6 gated phases. Each phase requires your approval before advancing. Output: Marp markdown + PDF.

### `/audit` — Stress-test an existing deck

Runs 7 investor-lens tests against any Marp markdown or PDF deck. Outputs a structured report with PASS/WEAK/FAIL per test, an overall grade, and a revised headline sequence.

## Why this exists

Founders dump information into slides. Investors make decisions using heuristics. The gap between "everything about my company" and "the 3 things that make you write a check" is where most pitch decks die.

This plugin engineers takeaways instead of dumping information:

- **Headlines are messages, not labels** — "Team" tells investors nothing. "Team that shipped payments infrastructure to 200M users" makes them lean forward
- **Phases force rigor** — you can't design slides until the story is locked, and the story doesn't get locked until the foundation research checks out
- **Anti-BS rules are hard constraints** — no invented metrics, no top-down market numbers, no superlatives without proof. If you can't back it up, it gets flagged
- **CoVe verification catches weak spots** — four critic roles (Skeptical VC, Domain Expert, Storyteller, First-Time Reader) stress-test each phase before you advance

### The headline test

This is the single most important differentiator. Read just the headlines of your deck aloud. Do they tell a complete story? Would an investor take a meeting based on headlines alone?

**Generic deck headlines:**

1. Company Overview
2. The Problem
3. Our Solution
4. Market Size
5. Business Model
6. Team
7. Traction
8. Competition
9. Financials
10. The Ask

**After this plugin:**

1. $47B in freight invoices are processed by hand every year
2. We lived this problem — 11 years inside logistics operations
3. One API call replaces 6 hours of manual reconciliation
4. 340 carriers already process through us — $120M monthly volume
5. We win because incumbents can't cannibalize their consulting revenue
6. Net revenue retention: 147%. Customers expand faster than we can onboard
7. Unit economics work today — not "at scale"
8. The competitors VCs will ask about, and why they're stuck
9. $2.4M ARR, 18 months. Path to $10M requires 40 more mid-market accounts
10. $8M to own mid-market freight reconciliation in North America

The first version is a table of contents. The second is an investment thesis.

## Phase overview

| Phase | Name       | Output                   | Gate                          |
| ----- | ---------- | ------------------------ | ----------------------------- |
| 0     | Interview  | `pitch-interview.md`     | Founder approves summary      |
| 1     | Foundation | `pitch-foundation.md`    | Founder approves strategy     |
| 2     | Story      | `pitch-story.md`         | Founder approves narrative    |
| 3     | Objections | `pitch-objections.md`    | Founder approves responses    |
| 4     | Design     | `pitch-visual-brief.md`  | Founder approves visual brief |
| 5     | Slides     | `pitch-deck.md` + `.pdf` | Final review                  |

## Audit battery

| #   | Test                            | Focus                                                       |
| --- | ------------------------------- | ----------------------------------------------------------- |
| 1   | **Headlines Tell the Story** ⭐ | Do headlines alone tell a compelling investment story?      |
| 2   | Team Placement                  | Is the team slide optimally positioned for the stage?       |
| 3   | 5-Second Test                   | Can you state each slide's message after 5 seconds?         |
| 4   | Narrative Arc                   | Does the deck build visceral → logical momentum?            |
| 5   | Anti-BS Check                   | Any invented claims, missing proof, or hidden competition?  |
| 6   | Investor Psychology             | Are partner talking points and objection responses obvious? |
| 7   | Structural Completeness         | Are all critical deck elements present?                     |

## Requirements

- [Claude Code](https://claude.ai/code) (CLI)
- [Marp CLI](https://github.com/marp-team/marp-cli) — `npm install -g @marp-team/marp-cli` (for PDF rendering)

## Installation

From the CLI:

```bash
claude plugin marketplace add dkorobtsov/pitch-deck
claude plugin install pitch-deck@dkorobtsov-pitch-deck
```

Or from within a Claude Code session:

```
/plugin marketplace add dkorobtsov/pitch-deck
/plugin install pitch-deck@dkorobtsov-pitch-deck
```

### Manual installation

Copy the plugin directory into your Claude Code plugins folder:

```bash
cp -r plugins/pitch-deck ~/.claude/plugins/pitch-deck
```

## Usage

### Create a new pitch deck

```
/create
```

The interview starts immediately — 12 questions, one at a time. Follow-up questions dig deeper when your answers reveal something interesting. After the interview, the plugin scans your working directory for existing business documents (plans, financials, research) and incorporates them.

All output files are saved to `./pitch/` relative to your current directory.

### Audit an existing deck

```
/audit ./pitch/pitch-deck.md
```

Or point it at any Marp markdown or PDF:

```
/audit path/to/deck.pdf
```

Produces a structured report with overall grade (A-F), per-test verdicts, critical issues, and a revised headline sequence. Saved to `./pitch/pitch-audit.md`.

## How it works

1. **Structured interview** — 12 questions asked one at a time, with follow-ups on interesting answers. Captures the founder's story, not just facts
2. **Phased gates** — each phase must be approved before the next begins. Foundation work (research, positioning, psychology mapping) happens before any slide is written
3. **CoVe verification** — Chain-of-Verification runs at each gate with four critic roles stress-testing the work
4. **Anti-BS enforcement** — 10 hard rules enforced throughout: no invented metrics, bottom-up-only market sizing, no superlatives without proof, every number cross-checked
5. **Narrative-first design** — headlines are written first and must tell the complete story alone. Body text only emphasizes what the headline already conveys
6. **Marp rendering** — final output is a Marp markdown file with a clean, minimal theme (system fonts, no dependencies) rendered to PDF

## File structure

```
plugins/pitch-deck/
├── .claude-plugin/
│   └── plugin.json          # Plugin manifest
├── commands/
│   ├── create.md            # /create — build a deck from scratch
│   └── audit.md             # /audit — 7-test stress test
├── references/
│   └── reference.md         # Detailed frameworks (Seven Moats, Onion Theory, etc.)
├── assets/
│   └── theme.css            # Canonical Marp theme source
├── AGENTS.md                # Agent guidelines
└── CLAUDE.md                # Points to AGENTS.md
```

## Output files

All output is written to `./pitch/` relative to your working directory:

| File                    | Phase | Description                                               |
| ----------------------- | ----- | --------------------------------------------------------- |
| `pitch-interview.md`    | 0     | Founder interview transcript                              |
| `pitch-foundation.md`   | 1     | Business audit, investor psychology map, moat analysis    |
| `pitch-story.md`        | 2     | 30-second commercial, slide budget, headline sequence     |
| `pitch-objections.md`   | 3     | Burning questions + appendix slide answers                |
| `pitch-visual-brief.md` | 4     | Per-slide design specs, visual suggestions, speaker notes |
| `pitch-deck.md`         | 5     | Marp markdown source                                      |
| `pitch-deck.pdf`        | 5     | Rendered PDF                                              |
| `theme.css`             | 5     | Marp theme (written at build time)                        |
| `pitch-audit.md`        | —     | Audit report (from `/audit`)                              |

## Credits

Methodology synthesized from Eric Paley (Founder Collective), Andy Raskin (strategic narrative), Marc Andreessen (risk onion framework), Hamilton Helmer (7 Powers/moats), and years of pitch coaching.

Built by [Dmitry Korobtsov](https://github.com/dkorobtsov).

## License

MIT
