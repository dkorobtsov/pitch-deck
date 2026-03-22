---
description: >-
  Build an investor-grade pitch deck through narrative-first methodology.
  Story before slides. Writing before design. Meaning before data.
  Runs through 6 phases: Interview, Foundation, Story, Objections, Design, Slides.
allowed-tools:
  - Read
  - Write
  - Bash
  - WebSearch
  - AskUserQuestion
---

# Pitch Deck Builder

Build investor-grade pitch decks through narrative-first methodology. Story before slides. Writing
before design. Meaning before data.

**Core principle**: Audiences skim. Decision-makers use heuristics. If you give them too much info
and not enough meaning, they make sub-optimal decisions. Your job: engineer the takeaways.

## Execution Phases

This skill runs in sequential phases. **Complete each phase before moving to the next.** Get user
approval at each gate.

---

### Phase 0: Founder Interview

Before anything else, understand the founder and the business through a structured interview.

**Check for existing interview**: If `./pitch/pitch-interview.md` exists, ask the user:

> "I found a previous interview at ./pitch/pitch-interview.md. Would you like to use it, or start fresh?"

If starting fresh (or no previous interview exists), ask these 12 questions **ONE AT A TIME**.
Wait for each answer before asking the next. Follow up on interesting answers — dig deeper when
you sense passion, unique insight, or a story worth telling.

1. What does your company do? Explain it like I'm 5
2. What specific pain does your product solve? Who feels this pain most acutely?
3. Why did YOU start this company? What's your personal connection to the problem?
4. What's your unfair advantage — why can YOUR team win this?
5. What traction do you have? Users, revenue, LOIs, growth rate — anything earned, not just done
6. Who are your competitors? Be honest — what do they do better, and where do you win?
7. What's your business model? How do you make money, and what are the unit economics?
8. What's the market size? (Think bottom-up: how many potential customers × what they'd pay)
9. What's your biggest risk right now? What keeps you up at night?
10. How much are you raising, and what will you do with the money? What milestones will it unlock?
11. What's the 3-year vision? What does the world look like if you succeed?
12. Is there anything else investors MUST know that I haven't asked about?

Save the complete interview transcript to `./pitch/pitch-interview.md`.

**Context enrichment**: After the interview, scan the current working directory for any existing
business documents (business plans, financial projections, competitive research, pitch materials,
marketing docs). Read and internalize any relevant files found.

If the user specifies target investors, research them. Tailor the message.

---

### Phase 1: Foundation Work (Writing, Not Slides)

Do NOT touch slides yet. Pen and paper mindset. Output a single markdown document.

#### Step 1A: Business Audit

Analyze interview answers and any discovered context. Produce:

- **The Pain** (not vitamin): What specific, acute problem do we alleviate?
  - Must be visceral, not abstract
  - "Healthcare is broken" = BAD. Specific pain point = GOOD
  - Prove it beyond stating it
- **The Inevitable Future**: Describe a future impossible to deny will exist
- **Current Blockers**: What prevents/slows that future from happening?
- **Our Solution**: How we solve those blockers, unique insights, why now
- **Hard Value**: Quantifiable metrics, cost savings, revenue impact, measurable outcomes
- **Soft Value**: Trust, reliability, brand values, certainty, meaning

#### Step 1B: Investor Psychology Map

Produce these lists (be brutally honest, no BS):

1. **5 Reasons to Invest** (emotional/greed reasons work better):
   - Start with ALL reasons, reduce to 3-5 "lures"
   - Connect to big, less competitive markets
   - Each reason = a talking point for the partner to sell internally

2. **10-15 Reasons NOT to Invest** (address fear directly):
   - Get in front of every risk
   - For each: write the contingency plan / defang strategy
   - "We understand the risk but the rewards are huge" — only if true
   - Frame through Onion Theory: what risks has this round already peeled?
   - What risks does THIS raise peel away?

3. **Moat Analysis** — Seven Moats Framework (which apply honestly):
   - Process Power: last 10% to 99% reliability = 10-100x effort. Competitors won't do the painstaking edge case work
   - Cornered Resource: unique data, regulatory approvals, relationships, proprietary datasets
   - Switching Costs: data migration pain, custom workflows, personalization lock-in
   - Counter-Positioning: what incumbents can't do without cannibalizing themselves
   - Brand: speed + no legacy business model to protect
   - Network Effects: more users → better product → more users
   - Scale Economies: massive upfront investment creates cost advantages

4. **Risk Onion** (Andreessen framework):
   - List ALL conceivable risks (founding team, product, technical, launch, market acceptance,
     revenue, cost of sale, viral growth)
   - Mark which are already peeled (with evidence)
   - Mark which THIS round peels (with milestones)
   - Mark which remain for next round

#### Step 1C: Traction Narrative

Traction is your story — own it. Rules:

- **Traction != Action**. Building something = action. Users/revenue/LOIs = traction
- Traction is earned, not done. External proof you're onto something
- Format: "In the past X time we've done {amazing things}. Customers {proof}. We {validation}."
- Force a double take
- Big traction + small time = best signal

#### Step 1D: "Special Person" Assessment

At early stages, 80-90% of the deal is team. Before the spreadsheet opens, investors ask: "Is this
founder special?"

Document:

- What makes this team world-class at something that matters?
- Technical depth others can't touch?
- Insight from living the problem for years?
- Execution speed that makes normal timelines look slow?
- Scar tissue from doing the impossible?
- The "gene pool" — why THIS team for THIS company?

#### Step 1E: Competitive Positioning

- Full disclosure on competition (hiding it = instant credibility kill)
- Address competition through the prism of advantages
- On market slides: show holes created by competition falling short
- Weave throughout the deck, not just one slide

Save to `./pitch/pitch-foundation.md`.

**GATE 1**: Present Foundation document to user. Get approval before Phase 2.

---

### Phase 2: Story Architecture

#### Step 2A: 30-Second Commercial

If Hollywood can tease a 2-hour film in 30 seconds, you can tease a 45-minute meeting.

Write 3-4 alternative versions. Each must:

- Explain what we do in terms a kindergartner understands
- Make the grand ambition and upside immediately clear
- Follow: inevitable future → current blockers → our solution → why now
- Hierarchy: who (team) > why (conviction) > what (problem) > how (solution)
- Earlier the stage, stronger the ">" between elements

#### Step 2B: Slide Budget

Allocate ~20 slides. **Team placement decision** (critical at early stage):

Team slide(s) should go in the **first 3-5 slides** when:

- Founder has personal connection to the problem (lived it, built in the space)
- Industry expertise IS the moat ("why should I believe you can do this?")
- The "why us" story makes everything else more credible
- Founder origin story creates emotional hook: "I saw this problem at X, spent Y years on it"

When founder story is strong, lead with it right after the hook. It makes the audience
listen more carefully to every slide that follows. They're no longer evaluating an idea —
they're rooting for a person.

Team goes later (slide 12+) only when product/traction is so strong it speaks for itself.
At pre-seed/seed: this is rare. Default to team early.

Use one of these presentation budgets:

**Option A: Founder-Led (team early — DEFAULT for pre-seed/seed)**
Use when founder story is personal, industry expertise is the moat.

1. Hook / 30-second commercial (1 slide)
2. Founder story — why this problem is personal (1-2 slides)
3. Problem & pain (2 slides)
4. Solution & market (1-2 slides)
5. Special sauce / advantages (2-3 slides)
6. Traction & validation (1-2 slides)
7. Risks & how we manage them (2-3 slides)
8. Go-to-market & segmentation (2 slides)
9. Financials & cash flow (2-3 slides)
10. Competition — full disclosure (1-2 slides)
11. Milestones & use of funds (1 slide)
12. Close — commercial reprise / "did I convince you?" (1 slide)

**Option B: Product-Led (team later — use when traction speaks for itself)**

1. Hook / 30-second commercial (1 slide)
2. Problem & pain (2 slides)
3. Solution & market (1-2 slides)
4. Traction & validation (1-2 slides)
5. Special sauce / advantages (2-3 slides)
6. Go-to-market & segmentation (2 slides)
7. Team — why us for this (1-2 slides)
8. Risks & how we manage them (2-3 slides)
9. Financials & cash flow (2-3 slides)
10. Competition — full disclosure (1-2 slides)
11. Milestones & use of funds (1 slide)
12. Close — commercial reprise / "did I convince you?" (1 slide)

Appendix: 15+ slides, one per anticipated question.

#### Step 2C: 20 Headline Narrative

Write 20 slide headlines that ALONE tell the complete investment story.

**CRITICAL RULES**:

- Headlines are MESSAGES, not titles
  - BAD: "Team"
  - GOOD: "Team engineered for this opportunity"
- Headlines without any slide content should tell an emotional narrative
- Lay them out in a text document — does it capture the reader?
- Start with the biggest statement tuned to the audience
- Start like kindergartners, advance like graduate students
- Visceral > logical order
- "Left hook, right hook" style — keep them engaged
- End with the 30-second commercial as summary / flourish

Test: Read just the 20 headlines aloud. Does it make you want to invest?

#### Step 2D: Body Text (Minimal)

After headlines are approved, decide where body text is needed:

- Body text ONLY to emphasize the headline message
- De-word aggressively. Single lines only
- One line per bullet, max 4-5 lines per slide
- Max 30 words per slide (40 absolute max)
- No full sentences, no periods
- No clutter: where does the eye go FIRST?

Save to `./pitch/pitch-story.md`.

**GATE 2**: Present Story Architecture to user. Get approval before Phase 3.

---

### Phase 3: Objection Arsenal

#### Step 3A: Burning Questions List

Write 15+ hardest questions investors will ask. Include:

- Churn rate concerns
- Competitive differentiation
- Unit economics viability
- Sales cycle / capital needs
- Ideal customer profile / GTM fit
- Long tail business scalability
- Path to unit profitability + key levers
- Regulatory de-risking
- Pricing rationale + expansion opportunities
- Revenue stream focus vs. diversification
- Any business-specific hard questions

#### Step 3B: Appendix Slides

For each burning question: one appendix slide with detailed answer.

- Detail is OK in appendix — complexity is OK
- This IS your arsenal. Update it after every investor meeting
- Find excuses to flip to appendix during Q&A (shows preparedness)
- If you don't have an answer: offer to get back. Never BS.

#### Step 3C: Investor Targeting Notes

If specific investors are known:

- Research their last 6-10 investments
- Identify biases, fund status, thesis
- Approach order: five least important first (practice rounds)
- Fine-tune commercial and emphasis per investor
- Remember: you're selling the partnership. Give the partner talking points to overcome objections
  from their partners

Save to `./pitch/pitch-objections.md`.

**GATE 3**: Present Objection Arsenal to user. Get approval before Phase 4.

---

### Phase 4: Visual Design Brief

Only after story is locked. Output design specifications before generating slides.

#### Slide Design Rules (5-Second Test)

Every slide must pass: show for 5 seconds, take away. Can viewer state the message?

- **One message per slide**
- Eyes should know where to focus, not wander
- Billboard design: if you can't read it driving past at 60mph, simplify
- Lots of white space, reduce visual complexity
- All text >20pt (readable) OR <13pt (not meant to be read)
- High Signal:Clutter ratio
- Photos > graphics. Real > stock
- Superlatives are not proof: SHOW, don't tell
- No edges, no mixed messages, no gratuitous graphics
- Streamline font colors, sizes, lines, boxes

#### Output Format

For each slide, specify:

- Headline (from Phase 2)
- Body text (if any, from Phase 2)
- Visual suggestion (photo concept, data viz, demo screenshot)
- Speaker notes (what to SAY, not what's on screen)
- Timing estimate (seconds)

Save to `./pitch/pitch-visual-brief.md`.

**GATE 4**: Present Visual Design Brief to user. Get approval before Phase 5.

---

### Phase 5: Marp Slide Generation

Generate the actual slide deck as a Marp markdown file + render to PDF/HTML.

#### Theme

First, write the theme CSS to `./pitch/theme.css`. Use this exact content:

```css
/* @theme pitch-deck */

/*
  Pitch deck theme — clean, minimal, Apple keynote aesthetic.
  System fonts, no external dependencies.
  Classes: lead, invert, big-number, quote, comparison, light
  Layout: columns, columns-3, metric, steps
*/

@import "default";

:root {
  --color-bg: #ffffff;
  --color-bg-alt: #f8f9fa;
  --color-bg-dark: #000000;
  --color-accent: #0071e3;
  --color-accent-light: rgba(0, 113, 227, 0.08);
  --color-text: #1d1d1f;
  --color-text-secondary: #6e6e73;
  --color-text-tertiary: #86868b;
  --color-border: #d2d2d7;
  --color-bold: #0071e3;
  --font-main:
    -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue",
    sans-serif;
  --font-mono: "SF Mono", "Fira Code", "JetBrains Mono", monospace;
}

/* Base slide */
section {
  background: var(--color-bg);
  color: var(--color-text);
  font-family: var(--font-main);
  font-size: 28px;
  font-weight: 400;
  line-height: 1.4;
  padding: 70px 80px;
  justify-content: flex-start;
  letter-spacing: -0.3px;
}

/* Typography */
h1 {
  color: var(--color-text);
  font-size: 2.6em;
  font-weight: 700;
  line-height: 1.1;
  letter-spacing: -0.02em;
  margin-bottom: 0.4em;
  border: none;
}
h2 {
  color: var(--color-text);
  font-size: 1.5em;
  font-weight: 600;
  line-height: 1.2;
  letter-spacing: -0.01em;
  margin-bottom: 0.5em;
  border: none;
}
h3 {
  color: var(--color-text-secondary);
  font-size: 1em;
  font-weight: 600;
  text-transform: uppercase;
  letter-spacing: 0.06em;
  margin-bottom: 0.6em;
  border: none;
}
p {
  color: var(--color-text-secondary);
  font-size: 32px;
  margin-bottom: 0.5em;
  letter-spacing: -0.3px;
}
strong {
  color: var(--color-bold);
  font-weight: 600;
}
em {
  color: var(--color-text);
  font-style: italic;
}
code {
  font-family: var(--font-mono);
  font-size: 0.85em;
  color: var(--color-accent);
  background: var(--color-accent-light);
  padding: 0.15em 0.4em;
  border-radius: 6px;
}
a {
  color: var(--color-accent);
  text-decoration: none;
}

/* Lists */
ul,
ol {
  margin-left: 0;
  padding-left: 1.2em;
}
li {
  margin-bottom: 0.4em;
  color: var(--color-text-secondary);
  font-size: 105%;
  line-height: 1.3;
}
li::marker {
  color: var(--color-accent);
}

/* Blockquote — callout box */
blockquote {
  border-left: 4px solid var(--color-accent);
  background: var(--color-accent-light);
  padding: 20px 28px;
  border-radius: 0 12px 12px 0;
  margin: 1em 0;
}
blockquote p {
  color: var(--color-text) !important;
  font-size: 1em !important;
  margin: 0;
}

/* Tables */
table {
  width: 100%;
  border-collapse: collapse;
  margin: 1em 0;
}
th {
  background: var(--color-bg-alt);
  color: var(--color-text);
  font-weight: 600;
  text-align: left;
  padding: 12px 16px;
  font-size: 0.85em;
  text-transform: uppercase;
  letter-spacing: 0.04em;
  border-bottom: 2px solid var(--color-border);
}
td {
  padding: 10px 16px;
  border-bottom: 1px solid rgba(0, 0, 0, 0.06);
  color: var(--color-text-secondary);
}
tr:last-child td {
  border-bottom: none;
}

hr {
  border: none;
  height: 1px;
  background: var(--color-border);
  margin: 1.5em 0;
}
img {
  border-radius: 12px;
}

/* Page number */
section::after {
  font-family: var(--font-main);
  font-size: 14px;
  color: var(--color-text-tertiary);
}
header,
footer {
  font-family: var(--font-main);
  font-size: 14px;
  color: var(--color-text-tertiary);
}

/* ─── TITLE slide — class: lead ─── */
section.lead {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  padding: 80px;
  background: var(--color-bg);
}
section.lead h1 {
  font-size: 3.2em;
  font-weight: 700;
  margin-bottom: 0.15em;
  color: var(--color-text);
}
section.lead h2 {
  font-size: 1.2em;
  color: var(--color-text-secondary);
  font-weight: 400;
  letter-spacing: -0.01em;
}
section.lead p {
  color: var(--color-text-tertiary);
  font-size: 0.75em;
  margin-top: 2.5em;
}
section.lead footer,
section.lead header,
section.lead::after {
  display: none;
}

/* ─── DARK slide — class: invert ─── */
/* Section breaks, dramatic statements */
section.invert {
  background: var(--color-bg-dark);
  color: #ffffff;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  padding: 80px 100px;
}
section.invert h1 {
  color: #ffffff;
  font-size: 3em;
  font-weight: 700;
}
section.invert h2 {
  color: rgba(255, 255, 255, 0.6);
  font-weight: 400;
}
section.invert p {
  color: rgba(255, 255, 255, 0.7);
}
section.invert strong {
  color: var(--color-accent);
}
section.invert footer,
section.invert header,
section.invert::after {
  display: none;
}

/* ─── BIG NUMBER slide ─── */
/* Single stat/metric hero. h1 = the number */
section.big-number {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
}
section.big-number h1 {
  font-size: 6em;
  color: var(--color-accent);
  font-weight: 700;
  margin-bottom: 0.05em;
  letter-spacing: -0.03em;
}
section.big-number h2 {
  font-size: 1.1em;
  color: var(--color-text-secondary);
  font-weight: 400;
}

/* ─── QUOTE slide ─── */
/* Use > for quote text, > for attribution */
section[class~="quote"] {
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 80px 100px;
  background: var(--color-bg);
}
section[class~="quote"] > blockquote {
  border-left: none !important;
  background: none !important;
  padding: 0 !important;
  margin: 0 !important;
}
section[class~="quote"] > blockquote > p {
  font-size: 1.7em !important;
  font-style: italic !important;
  color: var(--color-text) !important;
  line-height: 1.4 !important;
  margin: 0 !important;
  font-weight: 400 !important;
  letter-spacing: -0.5px !important;
}
section[class~="quote"] > blockquote + blockquote {
  margin-top: 1.5em !important;
}
section[class~="quote"] > blockquote + blockquote > p {
  font-size: 0.85em !important;
  font-style: normal !important;
  color: var(--color-text-tertiary) !important;
  font-weight: 400 !important;
}

/* ─── COMPARISON slide ─── */
/* Use with .columns for side-by-side */
section.comparison .columns > div:first-child {
  border-right: 1px solid var(--color-border);
  padding-right: 40px;
}
section.comparison .columns > div:last-child {
  padding-left: 20px;
}

/* ─── LIGHT (alt background) slide ─── */
/* Subtle emphasis, screenshots/demos */
section.light {
  background: var(--color-bg-alt);
}

/* ─── Two columns layout ─── */
section .columns {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 60px;
  align-items: start;
}

/* ─── Three columns layout ─── */
section .columns-3 {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  gap: 40px;
  align-items: start;
}

/* ─── KPI Metric card ─── */
section .metric {
  text-align: center;
  padding: 20px;
}
section .metric span:first-child {
  display: block;
  font-size: 2.6em;
  font-weight: 700;
  color: var(--color-accent);
  line-height: 1.2;
  letter-spacing: -0.02em;
}
section .metric span:last-child {
  display: block;
  font-size: 0.7em;
  color: var(--color-text-tertiary);
  text-transform: uppercase;
  letter-spacing: 0.06em;
  margin-top: 0.3em;
  font-weight: 600;
}

/* ─── Timeline / steps ─── */
section .steps {
  display: flex;
  gap: 20px;
  align-items: stretch;
}
section .steps > div {
  flex: 1;
  background: var(--color-bg-alt);
  padding: 28px;
  border-radius: 16px;
  border-top: 3px solid var(--color-accent);
  font-size: 0.85em;
}
```

#### Marp Frontmatter (REQUIRED)

Every deck must start with (replace `[Company Name]` with the actual company name from the interview):

```yaml
---
marp: true
theme: pitch-deck
paginate: true
header: "[Company Name]"
footer: "Confidential"
---
```

#### Slide Classes (pick the right one per slide)

| Class        | Directive                     | Use For                                |
| ------------ | ----------------------------- | -------------------------------------- |
| `lead`       | `<!-- _class: lead -->`       | Title slide, closing slide             |
| `invert`     | `<!-- _class: invert -->`     | Section breaks (dark bg, white text)   |
| `big-number` | `<!-- _class: big-number -->` | Single stat/metric hero (h1 = number)  |
| `quote`      | `<!-- _class: quote -->`      | Customer quotes (two blockquotes)      |
| `comparison` | `<!-- _class: comparison -->` | Us vs them (with `.columns`)           |
| `light`      | `<!-- _class: light -->`      | Screenshots/demos (light bg)           |
| _(default)_  | _(none)_                      | Content slides (bullets, text, tables) |

#### Layout Components (HTML, requires `--html` flag)

**Two columns:**

```html
<div class="columns">
  <div>Left content</div>
  <div>Right content</div>
</div>
```

**Three columns:**

```html
<div class="columns-3">
  <div>Col 1</div>
  <div>Col 2</div>
  <div>Col 3</div>
</div>
```

**KPI metrics grid** (use inside `.columns-3`):

```html
<div class="metric">
  <span>$1.2M</span>
  <span>Annual Revenue</span>
</div>
```

**Timeline / steps:**

```html
<div class="steps">
  <div><strong>Phase 1</strong>Description</div>
  <div><strong>Phase 2</strong>Description</div>
  <div><strong>Phase 3</strong>Description</div>
</div>
```

#### Slide Writing Rules

1. **Max 30 words per slide** (40 absolute max, excluding speaker notes)
2. One message per slide — if you need two points, use two slides
3. Bullets: max 4-5 per slide, one line each, no periods
4. Headlines are MESSAGES not titles: "Team engineered for this" not "Team"
5. Use `big-number` class for any impressive single metric
6. Use `invert` class for narrative pivots / section transitions
7. Open with `lead`, close with `lead`
8. Put detailed talking points in speaker notes, not on slides

#### Build Command

After writing the `.md` file, render with:

```bash
marp --theme ./pitch/theme.css --html --pdf ./pitch/pitch-deck.md -o ./pitch/pitch-deck.pdf
```

Save the Marp source to `./pitch/pitch-deck.md` and render PDF to `./pitch/pitch-deck.pdf`.

---

## Anti-Bullshit Rules (ENFORCED THROUGHOUT)

These are non-negotiable. Violating any = restart that section.

1. **Never invent metrics**. If unknown: "needs verification" or omit
2. **Never use top-down market numbers** that aren't relevant ("$4 trillion healthcare spend" =
   instant credibility kill)
3. **Bottom-up projections only** for market sizing
4. **No superlatives without proof**. "World-class team" means nothing. Show what makes them
   world-class
5. **No leading questions in customer validation**. Cherry-picked results = fabrication
6. **Numbers must match**. Cross-check every figure across slides
7. **Overselling or hiding issues always bites later**. If the investor feels spun, you're done
8. **Don't be flippant with numbers or statements**
9. **Acknowledge concept vs. data-driven stage honestly**
10. **Value proposition must meet reality**. It needs to work, not just sound good

## CoVe Verification (Applied at Each Gate)

At each phase gate, run Chain-of-Verification:

1. Present the draft
2. Generate 3-5 verification questions from these critics:
   - **Target Customer**: "Would I actually pay for this?"
   - **Skeptical VC Partner**: "Is this claim verifiable? What's missing?"
   - **Competitor's CTO**: "We could build this in a weekend. Why can't we?"
   - **IC Committee Member**: "Why should I stake my reputation on this?"
3. Answer each independently and honestly
4. Flag any invented claims — remove or mark "needs verification"
5. Revise and present final version

## Reference Material

For detailed frameworks (Onion Theory, Seven Moats, Value Proposition, Traction Rules, Elevator
Pitch, Presentation Budgets, Headline Writing, Anti-Patterns, Slide Design Specs), read
`references/reference.md` in this plugin directory.

## Output Files

All output goes to `./pitch/` relative to the current working directory:

- `pitch-interview.md` — Phase 0 output (founder interview transcript)
- `pitch-foundation.md` — Phase 1 output (business audit + psychology map)
- `pitch-story.md` — Phase 2 output (headlines + narrative architecture)
- `pitch-objections.md` — Phase 3 output (Q&A arsenal)
- `pitch-visual-brief.md` — Phase 4 output (design specs per slide)
- `pitch-deck.md` — Phase 5 output (Marp source)
- `pitch-deck.pdf` — Phase 5 output (rendered PDF)
- `theme.css` — Phase 5 output (Marp theme)
