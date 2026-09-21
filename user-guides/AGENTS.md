# User Guide and Tutorial Tone Guide

Read [the common guide](../common/AGENTS.md) first. This file only covers what's specific
to tutorials.

A tutorial's job is to get someone to a working result without making them feel stupid.
That's the whole brief.

## What changes

- Write directly to the reader (`you`).
- Supportive without being patronising. Assume competence, not context.
- Calm and action-focused. Nobody reading a tutorial wants a personality.
- Short sentences, even by the common guide's standards.

## Structure

1. What you'll achieve - the outcome, stated first.
2. What you need - versions, access, accounts, prerequisites.
3. The steps.
4. What success looks like.
5. Troubleshooting, organised by symptom.
6. What to do next.

Give the outcome before the prerequisites. People need to know it's the right guide before
they start installing things.

## Style details

- One action per step. Number sequential actions.
- Keep the explanation next to the step it explains, not in a preamble.
- Show expected output after each command so readers can check they're on track.
- Use screenshots and diagrams only when words are genuinely ambiguous.
- Give one complete walkthrough, then short variants. Don't fork the main path.
- Keep troubleshooting symptom-first: "If you see `connection refused`..." not "Common problems".

## Inclusive language additions

The [common baseline](../common/AGENTS.md#inclusive-language) applies. Tutorials are where
careless wording does the most damage, because the reader is already uncertain. Anything
that implies "this should be obvious" makes a stuck person feel worse and teaches them
nothing.

- The effort-minimising words are the big one. Cut `just`, `simply`, `easy`, `quick`, `obviously`, `of course`, and `all you need to do is`. If a step is genuinely short, the reader will notice on their own.
- Don't assume prior knowledge, hardware, region, connection speed, or tool access.
- Give keyboard paths alongside mouse instructions. Not everyone points and clicks.
- Name the element and quote its label rather than describing where it sits or what colour it is.
- Spell out time and date formats, and name the time zone.

| Avoid | Prefer |
|---|---|
| click the green button on the right | select **Continue** |
| this is straightforward | (delete the phrase) |
| dummy data | sample data |

## Phrases to use

- "In this section, you'll..."
- "Before you begin, check that..."
- "You should now see..."
- "If this doesn't work, verify..."
- "This step takes a few minutes to complete."

## Phrases to avoid

Beyond the [common list](../common/AGENTS.md#phrases-to-avoid):

- "All users should know"
- "It's easy to", "this is straightforward"
- "As you can see"
