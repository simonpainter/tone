# User Guide and Tutorial Tone Guide

A tutorial's job is to get someone to a working result without making them feel stupid.
That's the whole brief. Read [the blog guide](../blog/AGENTS.md) for the voice underneath.

## Core voice

- Use UK English.
- Write directly to the reader (`you`).
- Supportive without being patronising. Assume competence, not context.
- Use contractions and short sentences.
- Calm and action-focused. Nobody reading a tutorial wants a personality.

## Shape

1. What you'll achieve - the outcome, stated first.
2. What you need - versions, access, accounts, prerequisites.
3. The steps.
4. What success looks like.
5. Troubleshooting, organised by symptom.
6. What to do next.

Give the outcome before the prerequisites. People need to know it's the right guide
before they start installing things.

## Style details

- One action per step. Number sequential actions.
- Keep the explanation next to the step it explains, not in a preamble.
- Show expected output after each command so readers can check they're on track.
- Use active voice and 2-3 sentence paragraphs.
- Use screenshots and diagrams only when words are genuinely ambiguous, and give them real alt text.
- Give one complete walkthrough, then short variants. Don't fork the main path.
- Keep troubleshooting symptom-first: "If you see `connection refused`..." not "Common problems".

## Inclusive language

Tutorials are where careless wording does the most damage, because the reader is already
uncertain. Anything that implies "this should be obvious" makes a stuck person feel worse
and teaches them nothing.

- Use gender-neutral language by default (`they`, `you`, `everyone`).
- Don't assume prior knowledge, role, ability, hardware, region, connection speed, or tool access.
- Never minimise difficulty. Cut `just`, `simply`, `easy`, `quick`, `obviously`, `of course`, and `all you need to do is`. If a step is genuinely short, the reader will notice on their own.
- Use people-first language unless a group clearly prefers identity-first.
- Describe requirements and behaviours, not personal traits.
- Give keyboard paths alongside mouse instructions. Not everyone points and clicks.
- Don't rely on colour, shape, or screen position alone. Name the element and quote its label.
- Add descriptive alt text to every visual. Describe what it shows, not "screenshot of the settings page".
- Avoid idiom, slang, and culture-specific examples. Use neutral sample data and placeholder names.
- Spell out time and date formats, and name the time zone.

| Avoid | Prefer |
|---|---|
| just, simply, easily | (delete the word) |
| obviously, clearly, of course | (delete the phrase) |
| normal user | typical user, most users |
| sanity check | quick check, verification step |
| blacklist/whitelist | denylist/allowlist |
| dummy data | sample data, placeholder data |
| guys | everyone |
| click the green button on the right | select **Continue** |
| he, she (generic) | they |

## Phrases to use

- "In this section, you'll..."
- "Before you begin, check that..."
- "You should now see..."
- "If this doesn't work, verify..."
- "This step takes a few minutes to complete."

## Phrases to avoid

- "Just", "simply", "obviously", "clearly", "easily"
- "All users should know"
- "It's easy to", "this is straightforward"
- "As you can see"
- "In the ever changing world of..."
