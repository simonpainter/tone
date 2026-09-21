# Tone Guides

A set of tone guides for getting an LLM to write in my voice rather than in the voice of
an overenthusiastic press release. They're the same rules I use on
[simonpainter.com](https://www.simonpainter.com), adapted for eight different formats.

Each guide lives in an `AGENTS.md` file, which most coding agents and LLM tools pick up
automatically. Drop one into a prompt, point a tool at the directory, or copy the relevant
section.

## Start here

**[common/AGENTS.md](common/AGENTS.md)** carries the voice, the inclusive language
baseline, the accessibility rules, and the banned phrases. It's about 80% of what matters.

Everything else is a thin layer on top that covers what changes for one format. If you only
read one file, read the common one.

## The format guides

| Guide | What it's for |
|---|---|
| [Blog writing](blog/AGENTS.md) | Openings, shape, explaining technical things, endings |
| [Professional email](email/AGENTS.md) | Short, one ask, explicit deadlines |
| [Slide decks](slide-decks/AGENTS.md) | One idea per slide, spoken descriptions |
| [Strategy documents](strategy-documents/AGENTS.md) | Options, trade-offs, labelled assumptions |
| [Social media](social-media/AGENTS.md) | LinkedIn without the performance |
| [Technical documentation](technical-documentation/AGENTS.md) | Reference docs and procedures |
| [User guides and tutorials](user-guides/AGENTS.md) | Getting someone to a working result |
| [GitHub READMEs](github-readmes/AGENTS.md) | Fifteen seconds to answer two questions |

## What they're all trying to do

Three things, really.

**Sound like a person.** UK English, first person, contractions, short sentences, calm
confidence. Claims anchored in something I actually tested rather than something I read.
Dry humour where it fits, understatement instead of outrage. The humour dial turns down as
the format gets more formal, but the plainness never does.

**Stay inclusive.** The common guide sets the baseline, and each format adds what's
specific to it - alt text and emoji for social, "this chart shows" for decks, deficit
framing for strategy, effort-minimising words for tutorials. This isn't a compliance
exercise bolted on the end. Writing that assumes things about the reader is just worse
writing, and it's the kind of thing I want flagged before publishing rather than after.

**Cost less to generate.** Set a length target before drafting. One draft, one revision
pass. One worked example per idea instead of five near-duplicates. Splitting the shared
rules into `common/` helps here too - you paste the baseline once and add a short format
file, rather than eight near-identical guides.

## Using them

The pattern that works:

1. **Task** - what to produce.
2. **Audience** - who it's for and what they already know.
3. **Guides** - paste `common/AGENTS.md` plus the relevant format file.
4. **Budget** - max words, sections, or examples.
5. **Checks** - factual accuracy, inclusive language, and whether it's actually actionable.

## The short version

If you only take one thing from these guides, take the banned phrase list. "It is worth
noting", "in the ever changing world of", "game-changing", "leverage", "simply", "just",
"obviously". Cut those and most of the AI smell goes with them.

## Making them yours

Swap in your own domain terminology, regulatory constraints, and audience expectations. The
voice section in `common/` is mine, so change that freely. The inclusive language,
accessibility, and efficiency rules are worth keeping whoever you are.
