# Tone Guides

A set of tone guides for getting an LLM to write in my voice rather than in the voice of
an overenthusiastic press release. They're the same rules I use on
[simonpainter.com](https://www.simonpainter.com), adapted for eight different formats.

Each guide lives in an `AGENTS.md` file, which most coding agents and LLM tools pick up
automatically. Drop one into a prompt, point a tool at the directory, or copy the relevant
section.

## The guides

- [Blog writing](blog/AGENTS.md) - the anchor guide. Start here.
- [Professional email](email/AGENTS.md)
- [Slide decks](slide-decks/AGENTS.md)
- [Strategy documents](strategy-documents/AGENTS.md)
- [Social media](social-media/AGENTS.md)
- [Technical documentation](technical-documentation/AGENTS.md)
- [User guides and tutorials](user-guides/AGENTS.md)
- [GitHub READMEs](github-readmes/AGENTS.md)

The blog guide carries the full voice. The others assume you've read it and only cover
what changes for that format.

## What they're all trying to do

Three things, really.

**Sound like a person.** UK English, first person, contractions, short sentences, calm
confidence. Claims anchored in something I actually tested rather than something I read.
Dry humour where it fits, understatement instead of outrage.

**Stay inclusive.** Every guide has an inclusive language section, tailored to the format.
This isn't a compliance exercise bolted on the end. Writing that assumes things about the
reader - their gender, their ability, their hardware, their idiom - is just worse writing,
and it's the kind of thing I want flagged before publishing rather than after.

**Cost less to generate.** Set a length target before drafting. One draft, one revision
pass. One worked example per idea instead of five near-duplicates. Don't restate the same
point in the intro, the body, and the conclusion.

## Using them

The pattern that works:

1. **Task** - what to produce.
2. **Audience** - who it's for and what they already know.
3. **Guide** - paste the relevant `AGENTS.md`.
4. **Budget** - max words, sections, or examples.
5. **Checks** - factual accuracy, inclusive language, and whether it's actually actionable.

## The short version

If you only take one thing from these guides, take the banned phrase list. "It is worth
noting", "in the ever changing world of", "game-changing", "leverage", "simply", "just",
"obviously". Cut those and most of the AI smell goes with them.

## Making them yours

Swap in your own domain terminology, regulatory constraints, and audience expectations.
The voice section is mine, so change that freely. The inclusive language and efficiency
rules are worth keeping whoever you are.
