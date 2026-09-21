# Strategy Document Tone Guide

Strategy documents fail in one of two ways: they're vague enough that nobody can disagree,
or they're confident about things nobody has measured. Say what you know, say what you're
assuming, and keep those two things apart.

Read [the blog guide](../blog/AGENTS.md) for the voice. Strategy docs are more formal but
still plain-spoken.

## Core voice

- Use UK English.
- Precise, practical, evidence-led.
- Clear declarative sentences. Active voice for decisions and actions.
- Use `we` for organisational recommendations.
- Confidence tied to data. Where there's no data, say so.

## Structure

1. Executive summary
2. Context and constraints
3. Options assessed
4. Recommendation and rationale
5. Cost, risk, and mitigation
6. Delivery plan and milestones
7. Success metrics

Keep the executive summary to 150-300 words and make it stand alone. Assume some readers
never get past it - that's not a failure of theirs, it's the job of the summary.

## Style details

- Scope each section to a decision, not a background essay. Appendices exist for depth.
- Use tables for options, trade-offs, costs, and risks.
- Quantify claims. "Significant saving" means nothing; "£40k a year" means something.
- Separate observed facts from assumptions, and label the assumptions.
- State the known unknowns explicitly, along with what would resolve them.
- Define terms and acronyms on first use.
- Don't repeat the same rationale in three sections. Say it once and reference it.
- Name the option you rejected and why. A recommendation without alternatives isn't a recommendation.

## Inclusive language

Strategy documents decide what gets built and who it gets built for. Careless framing here
turns into exclusion downstream, which is expensive to unpick later.

- Use gender-neutral language by default (`they`, `stakeholders`, `the team`).
- Don't assume things about user groups, teams, markets, or regions. Say what evidence you have about them.
- Use neutral role and seniority terms. Don't equate job title with capability.
- Describe impacted groups specifically and respectfully. "Users on low-bandwidth connections", not "less sophisticated users".
- Avoid deficit framing. The problem is usually the barrier or the design choice, not the person. "The current flow requires a desktop browser" beats "users lack the right equipment".
- Use people-first language unless a group clearly prefers identity-first.
- Treat accessibility and inclusion as requirements with costs and metrics, not as a risk to accept later. Retrofitting costs more.
- Prefer globally clear wording. Avoid idiom and culture-specific references in documents that travel.

| Avoid | Prefer |
|---|---|
| manpower, man-hours, headcount as people | effort, staffing, person-hours, roles |
| the disabled, disabled users | people with disabilities, disabled people (check preference) |
| non-technical users | users without a technical background |
| normal user, standard customer | typical user, most customers |
| blacklist/whitelist | denylist/allowlist |
| master plan | overall plan, programme plan |
| sanity check | sense check, validation |
| grandfathered | legacy status |

## Phrases to use

- "Based on our analysis..."
- "The data indicates..."
- "We recommend..., because..."
- "We considered X and rejected it because..."
- "Key risks and mitigations are..."
- "This assumes... and we'd revisit if..."

## Phrases to avoid

- "Best-in-class", "world-class", "groundbreaking", "industry-leading"
- "Leverage", "synergy", "paradigm shift", "north star"
- "Obviously", "clearly", "simply"
- "Future-proof" - nothing is
- "In the ever changing world of..."
