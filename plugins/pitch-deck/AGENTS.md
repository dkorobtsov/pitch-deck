# Pitch Deck Plugin

> Narrative-first pitch deck builder and auditor for Claude Code.

## Scope

- **Owns**: `/create` command, `/audit` command, reference frameworks, theme CSS
- **Excludes**: User's pitch content (`./pitch/`), Marp CLI installation, external dependencies

## Core Methodology: Narrative-First

Story before slides. Writing before design. Meaning before data.

Audiences skim. Decision-makers use heuristics. Your job: engineer the takeaways, not dump
information.

## Hard Constraints

### Anti-BS Rules (10 Rules — Never Violate)

1. No "revolutionary" or "game-changing" — show, don't hype
2. No unsubstantiated market sizes — bottom-up only
3. No "no competition" claims — always acknowledge alternatives
4. Every metric needs context (growth rate, not just absolute number)
5. No vanity metrics without business impact
6. Team slide must answer "why THIS team wins THIS problem"
7. No feature lists — only capabilities tied to outcomes
8. Financial projections must state assumptions explicitly
9. Ask must be specific: amount, use of funds, milestones unlocked
10. Every slide must earn its place — cut ruthlessly

### Phase Gate Discipline (Never Skip)

The `/create` command runs 6 phases sequentially. **Never skip a phase or gate.**

| Phase         | Gate                          | Purpose                    |
| ------------- | ----------------------------- | -------------------------- |
| 0. Interview  | User approval of summary      | Capture founder's story    |
| 1. Foundation | User approval of strategy     | Research + positioning     |
| 2. Story      | User approval of narrative    | Headline sequence + arc    |
| 3. Objections | User approval of responses    | Pre-empt investor concerns |
| 4. Design     | User approval of visual brief | Layout + visual strategy   |
| 5. Slides     | Final review                  | Marp markdown + PDF build  |

Each gate requires explicit user approval before proceeding. Present work, ask for feedback,
iterate if needed, then advance.

### Interview Discipline

- Ask **one question at a time** — never batch questions
- Wait for answer before asking next
- Follow up on interesting answers — dig deeper on passion, insight, stories
- Save complete interview to `./pitch/pitch-interview.md`
- If previous interview exists, ask user: reuse or start fresh

## CoVe (Chain of Verification)

Apply CoVe at two critical points:

1. **After Phase 1 (Foundation)**: Verify market sizing, competitive positioning, moat claims
2. **After Phase 2 (Story)**: Verify headline sequence tells a compelling story read aloud

Four critic roles evaluate each verification:

| Critic            | Focus                                |
| ----------------- | ------------------------------------ |
| Skeptical VC      | "Where's the proof? What's missing?" |
| Domain Expert     | "Is this technically accurate?"      |
| Storyteller       | "Does this flow? Does it build?"     |
| First-Time Reader | "Do I understand this in 5 seconds?" |

## Theme Generation

- Theme CSS lives in `assets/theme.css` as canonical source
- `/create` embeds CSS inline and writes to `./pitch/theme.css` at Phase 5
- Theme name: `pitch-deck` (used in Marp frontmatter)
- Build: `marp --theme ./pitch/theme.css --html --pdf`

## Output Convention

All output files go to `./pitch/` relative to user's CWD:

- `pitch-interview.md` — Founder interview transcript
- `pitch-foundation.md` — Research + strategy
- `pitch-story.md` — Narrative arc + headlines
- `pitch-objections.md` — Objection map + responses
- `pitch-visual-brief.md` — Design direction
- `pitch-deck.md` — Final Marp markdown
- `pitch-deck.pdf` — Built PDF
- `theme.css` — Marp theme
- `pitch-audit.md` — Audit report (from `/audit`)

## Team Placement Decision

During Phase 1, determine team slide placement:

- **Founder-Led** (strong personal story, domain expertise): Team slide early (slide 3-4)
- **Product-Led** (strong traction, metrics): Team slide late (after traction proof)

This decision shapes the entire narrative arc. Document reasoning in foundation doc.

## Reference Material

`references/reference.md` contains detailed frameworks (Seven Moats, Onion Theory, Traction Rules,
presentation budgets). The `/create` command loads it as supplementary context — not required for
`/audit`.
