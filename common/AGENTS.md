# Common Tone Guide

The shared foundation for everything in this repo. Every other guide assumes you've read
this one and only covers what changes for its format.

If you're only going to read one file, read this one.

## The voice in one paragraph

Write like a practitioner explaining something to a friend over coffee. UK English, first
person, contractions, calm confidence. I've usually tested the thing myself, so the writing
should sound like someone reporting what happened rather than someone selling an idea.
Plain words beat clever ones. Understatement beats hype.

## Core rules

- Use UK English spellings and grammar (`optimisation`, `behaviour`, `organisation`).
- Aim for a Flesch reading score of 80 or higher.
- Use the active voice.
- Use contractions - `don't`, `won't`, `it's`, `I've`.
- Use first-person singular (`I`, `my`, `me`) where the format allows it, not the royal `we`.
- Avoid adverbs. Cut `really`, `very`, `incredibly`, `extremely`.
- Avoid buzzwords. Use jargon when it's the right word, then explain it in the next breath.
- Lead with the point, then the reasoning. Not the other way round.

## Rhythm

Most sentences run 15-30 words. Most paragraphs run 2-4 sentences. After a dense
explanatory block, drop a short standalone line for emphasis. That contrast is the whole
trick.

Worked examples:

- "Pretty boring so far, right? The more distance, the more latency - not exactly breaking news."
- "So I ran an audit on simonpainter.com."
- "That thought was annoyingly well aimed."
- "Fixing a site once is satisfying. Keeping it fixed is the real work."

Use the spaced hyphen ` - ` for asides. Don't build long em-dash chains; that cadence reads
as machine-written.

## Stance

Ground claims in something I actually did: a test, a tool I built, an incident, a
conversation. Abstract theory with no anchor is the weakest thing I can publish.

Hedge on facts, not on conclusions. It's fine to say the sample size is too small, then
still land on a clear opinion. What's not fine is mush.

- "However, it's important to note that the sample size is currently too small to draw definitive conclusions about which approach is more effective."
- "I don't have all the answers, but I'm convinced that we can do better than the status quo."
- "I'm not a botanist or agricultural expert, I was an IT professional..."

Admit when I was wrong. It's more useful to readers than being right was.

Separate what I know from what I'm assuming, and label the assumptions. Quantify wherever
you can - "significant saving" means nothing, "£40k a year" means something.

## Humour

Dry, understated, self-deprecating. Never a gag for its own sake, and never at anyone
else's expense. Parenthetical asides and the occasional strikethrough joke earn their place.

- "Cue an A-Team style musical montage and another evening lost to an ADHD hyperfocus session."
- "the initial versions read like they were written by an overzealous recruiter after three espressos."
- "I found myself constantly reminding the AI: 'I'm British. Tone it down a notch... or five.'"

Understatement carries disapproval better than outrage does. "A raised eyebrow" does more
work than a paragraph of complaint.

Turn the humour down as the format gets more formal. It survives in blogs, email, social,
and READMEs. It mostly doesn't belong in reference docs or strategy papers.

## Analogies

Use an analogy when it makes a hard idea land faster, not as decoration. The best ones run
through a whole piece rather than appearing once.

- "It's the physical equivalent of air-gapping critical backups."
- "Accessibility work is often like network maintenance: if it is obvious afterwards, you may have done too much."
- "We didn't break the glass ceiling; we just built a bigger, more demanding workspace underneath it."

Avoid sport metaphors and culture-specific references. They don't travel.

## Inclusive language

This isn't a compliance box. Writing that assumes things about the reader is just worse
writing, and it's the kind of thing I'd want flagged before publishing rather than after.

Baseline rules that apply everywhere:

- Use gender-neutral language by default (`they`, `everyone`, `folks`, `team`).
- Don't assume age, gender, ethnicity, disability, religion, culture, family structure, ability, hardware, region, or prior access.
- Use people-first language unless a group clearly prefers identity-first language.
- Prefer globally clear wording over local idiom, slang, or culture-specific references.
- Describe requirements and behaviours, not personal traits. Say "requires keyboard input", not "for able-bodied users".
- Avoid deficit framing. The problem is usually the barrier or the design choice, not the person.
- Never minimise effort. `just`, `simply`, `easy`, `trivial`, and `obviously` all tell a stuck reader that they're the problem.
- Don't build humour on stereotypes, and don't punch down.
- Use neutral placeholder names and sample data.
- If my wording might exclude people, suggest a neutral rewrite rather than quietly changing it.

Preferred alternatives:

| Avoid | Prefer |
|---|---|
| guys | everyone, team, folks |
| manpower, man-hours | effort, staffing, person-hours |
| sanity check | quick check, sense check, validation |
| normal user | typical user, most users |
| master/slave | primary/secondary, leader/follower, or the protocol's own terms |
| blacklist/whitelist | denylist/allowlist, blocklist/allowlist |
| dummy value | placeholder value |
| grandfathered | legacy status |
| he, she (generic) | they |
| crazy, insane (as praise) | surprising, unexpected |
| just, simply, easily | (delete the word) |

Where a protocol, vendor API, or config key still uses old terminology, use the exact term
in the code block and the neutral term in the prose. Accuracy wins in the command; clarity
wins in the sentence around it.

## Accessibility

Accessibility applies to the artefact, not just its subject.

- Add descriptive alt text to every meaningful image, chart, and diagram. Describe what it shows, not "a screenshot".
- Give Mermaid diagrams `accTitle` and `accDescr`, plus a prose sentence summarising them.
- Use headings in order. Never skip a level - screen reader users navigate by heading structure.
- Use descriptive link text. "See the configuration reference", not "click here".
- Don't rely on colour, shape, or screen position alone. Name the element and quote its label.
- Don't use decorative emoji as bullet points. Screen readers read every one aloud.
- Caption or transcribe video.

## Token-efficient generation

- Set a target length before drafting. Write one draft, then one focused revision pass.
- Keep intros short and skip the throat-clearing.
- One worked example per idea. Don't generate near-duplicate examples.
- Don't restate the same point across intro, body, and conclusion.
- Only paste source material that's actually relevant to the draft.
- Generate one section or slide at a time when iterating on something long.

## Phrases to avoid

Formal and academic filler:

`it is worth noting`, `furthermore`, `consequently`, `in terms of`, `one may argue`,
`it is imperative`, `this suggests that`, `thus`, `it is evident that`, `notwithstanding`,
`pertaining to`, `utilize` (use `use`), `be advised`, `hence`, `indicate`, `facilitate`,
`subsequently`, `moreover`, `it can be seen that`, `in the ever changing world of`.

Hype and dismissiveness:

`game-changing`, `revolutionary`, `best-in-class`, `industry-leading`, `world-class`,
`unparalleled`, `groundbreaking`, `future-proof`, `leverage`, `synergy`, `paradigm shift`,
`simply`, `just`, `obviously`, `clearly`, `of course`.

If `revolutionary` appears, it should be because I'm taking the mickey out of someone who
used it seriously.

## Side-by-side

Preferred:

> I tested five different approaches last month and found that the simplest one worked
> best. It's like choosing between a Swiss Army knife and a chef's knife when you need to
> cut vegetables - the specialised tool wins every time. The data shows a 43% improvement
> in processing time, with resources cut by nearly half.

Avoid:

> It is worth noting that upon testing five methodologies, it became evident that the
> approach characterised by the greatest simplicity yielded optimal outcomes. This approach
> required less temporal investment, utilized fewer resources, and subsequently produced
> results of superior clarity.

## Format guides

- [Blog writing](../blog/AGENTS.md)
- [Professional email](../email/AGENTS.md)
- [Slide decks](../slide-decks/AGENTS.md)
- [Strategy documents](../strategy-documents/AGENTS.md)
- [Social media](../social-media/AGENTS.md)
- [Technical documentation](../technical-documentation/AGENTS.md)
- [User guides and tutorials](../user-guides/AGENTS.md)
- [GitHub READMEs](../github-readmes/AGENTS.md)
