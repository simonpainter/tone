# GitHub README Tone Guide

A README has about fifteen seconds to answer two questions: what is this, and does it
solve my problem? Everything else is a bonus. Read [the blog guide](../blog/AGENTS.md) for
the voice.

## Core voice

- Use UK English.
- Direct and technically accurate. Written for someone scanning, not reading.
- Lead with what it does and who it's for.
- Confidence grounded in evidence. No marketing claims.
- Use `we` for maintainer voice, or `I` for a personal project - pick one and stick to it.

## Length

Target 400-900 words. Keep the top short: name, one-line summary, quick start. Push edge
cases into linked docs rather than bloating the file.

## Structure

1. Project name and a one-line summary
2. Quick start - the shortest path to something working
3. Core capabilities
4. Configuration
5. Limitations and known constraints
6. Contributing
7. Licence

## Style details

- The one-liner should say what it does, not what category it's in. "Queries BGP route servers from an MCP client", not "A modern tooling solution for network engineers".
- One minimal happy-path example near the top, copy-pasteable and actually tested.
- State the versions and platforms you've tested against. Don't imply support you haven't checked.
- Be honest about limitations. A "Known constraints" section builds more trust than a feature list.
- Use code formatting for commands, paths, flags, and config values.
- Use compact tables for feature and compatibility matrices.
- Use headings that describe content. `Configuration`, not `Stuff`.
- Keep badges to ones that mean something. A row of decorative shields is noise.
- If there's a diagram, give it alt text and a prose summary.

## Inclusive language

READMEs are read globally, by people at every level of experience, often translated by a
browser. Plain and neutral wording isn't a nicety here - it's what makes the project usable.

- Use gender-neutral language by default (`they`, `contributors`, `maintainers`).
- Use neutral role language: `maintainer`, `contributor`, `operator`, `reviewer`.
- Don't assume reader expertise, hardware, operating system, region, or connection speed.
- Never minimise effort. Cut `just`, `simply`, `easy`, `trivial`, and `obviously`. "Easy to use" without evidence is a claim, not a description.
- Use people-first language unless a group clearly prefers identity-first.
- Prefer globally clear wording. Avoid idiom, slang, and in-jokes in the setup instructions - keep the personality for the prose.
- Use descriptive alt text on every image, badge group, and diagram.
- Use descriptive link text. "See the configuration reference", not "click here".
- Keep the code of conduct and contributing guidance welcoming and specific about how to ask for help.
- Use neutral placeholder names and example data.

| Avoid | Prefer |
|---|---|
| master (branch) | main |
| master/slave | primary/secondary, leader/follower |
| blacklist/whitelist | denylist/allowlist, blocklist/allowlist |
| sanity check | validation check |
| dummy value | placeholder value |
| guys, dudes | everyone, contributors |
| simply run, just install | run, install |
| native speakers | fluent speakers |
| he, she (generic) | they |

Where an upstream API or config key still uses old terminology, keep the exact key in the
code block and use the neutral term in the surrounding prose.

## Phrases to avoid

- "Best-in-class", "industry-leading", "revolutionary", "blazing fast" without a benchmark
- "Simply", "just", "obviously", "clearly"
- "Easy to use" with nothing to back it
- "Batteries included" and similar idiom
- "In the ever changing world of..."
