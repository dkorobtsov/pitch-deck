---
description: >-
  Stress-test an existing pitch deck with 7 investor-lens tests.
  Headlines Tell Story, Team Placement, 5-Second Test, Narrative Arc,
  Anti-BS Check, Investor Psychology, Structural Completeness.
argument-hint: <path-to-deck.md>
allowed-tools:
  - Read
  - Write
  - AskUserQuestion
---

# Pitch Deck Audit

Run a 7-test audit battery on an existing pitch deck. Accepts Marp markdown or PDF.

## Input

Read the deck file provided as argument. If PDF, read all slides. If no argument given, ask the user
for the path.

## Audit Battery

Run ALL 7 tests. For each, output **PASS** / **WEAK** / **FAIL** with specific evidence from the
deck.

### Test 1: Headlines Tell the Story ⭐ MOST IMPORTANT

Extract every slide headline in order. Present them as a numbered list. Then evaluate:

- Read sequentially: do they tell a complete, compelling investment story WITHOUT body text?
- Is each headline a MESSAGE not a label? ("Team" = FAIL, "Team engineered for this opportunity" =
  PASS)
- Does the sequence build emotional momentum? Left hook, right hook alternation?
- Does headline sequence start with biggest statement and end with compelling close?
- Could an investor read ONLY the headlines and want to take a meeting?

**This is the single most important test.** If headlines don't tell the story, the deck fails
regardless of content quality.

### Test 2: Team Placement

Evaluate whether team slide placement is optimal:

- **Team early / first** when: founder has personal connection to problem, industry expertise is the
  moat, "why us" IS the story, team credibility makes everything else believable
- **Team later** when: product/traction speaks louder than bios, team is strong but not the
  differentiator
- If founder story creates "why this person, why this problem" conviction, team should be in first
  3-5 slides
- Founder origin story ("I lived this problem for X years") makes audience listen more carefully to
  everything after
- At early stage: 80-90% of deal is team. If team slide is buried at slide 15, that's usually wrong

### Test 3: 5-Second Test (Per Slide)

For each slide: if shown for 5 seconds and removed, can viewer state the message?

- One message per slide?
- Clear visual hierarchy — eyes know where to go?
- Max 30 words (40 absolute max)?
- Text readable (>20pt) or intentionally decorative (<13pt)?

### Test 4: Narrative Arc

- Does deck follow visceral > logical progression?
- Is there a "why now" moment?
- Does it build from problem > solution > proof > ask?
- Are there dead slides that break momentum?
- Does closing reprise the opening commercial?

### Test 5: Anti-BS Check

- Any invented or unverifiable claims?
- Top-down market numbers without bottom-up backing?
- Superlatives without proof?
- Competition hidden or dismissed?
- Numbers consistent across all slides?
- Traction vs action — is real traction shown, or just activity?

### Test 6: Investor Psychology

- Are the 3-5 partner talking points obvious from the deck?
- Are major objections pre-defanged?
- Is the risk onion visible — what's already peeled, what this round peels?
- Would an IC committee member have enough to champion this?

### Test 7: Structural Completeness

Check for missing critical elements:

- [ ] Hook / 30-second commercial
- [ ] Problem (visceral, not abstract)
- [ ] Solution (clear, differentiated)
- [ ] Market (bottom-up)
- [ ] Traction (earned, not done)
- [ ] Team (why THIS team for THIS company)
- [ ] Business model
- [ ] Competition (full disclosure)
- [ ] Financials
- [ ] Ask + use of funds
- [ ] Appendix / Q&A arsenal

## Output Format

Produce a structured report using this template:

```markdown
# Pitch Deck Audit

## Overall Grade: [A/B/C/D/F]

## Headlines Story Test

[numbered headline list]
[verdict: does this sequence tell the story?]
[specific fixes needed]

## Critical Issues (FAIL)

[issues that will kill the pitch]

## Weaknesses (WEAK)

[issues that reduce effectiveness]

## What's Working (PASS)

[what to keep and amplify]

## Recommended Slide Reorder

[if structure needs changing, propose new order with rationale]

## Revised Headlines

[rewritten headline sequence that tells the story]
```

Save audit report to `./pitch/pitch-audit.md` relative to CWD.
