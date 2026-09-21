# GitHub README Tone Guide

Read [the common guide](../common/AGENTS.md) first. This file only covers what's specific
to READMEs.

A README has about fifteen seconds to answer two questions: what is this, and does it solve
my problem? Everything else is a bonus.

## What changes

- Written for someone scanning, not reading.
- Use `we` for maintainer voice, or `I` for a personal project. Pick one and stick to it.
- Humour survives in the prose. Keep it out of the setup instructions.
- Confidence grounded in evidence. No marketing claims.

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

## Inclusive language additions

The [common baseline](../common/AGENTS.md#inclusive-language) applies. READMEs are read
globally, by people at every level of experience, often through a browser translator. Plain
neutral wording is what makes the project usable, not a nicety.

- Use neutral role language: `maintainer`, `contributor`, `operator`, `reviewer`.
- Don't assume reader expertise, operating system, hardware, region, or connection speed.
- "Easy to use" without evidence is a claim, not a description.
- Keep the personality in the prose and out of the install steps. In-jokes in a setup command are a barrier.
- Give badge groups alt text, and use descriptive link text throughout.
- Keep the code of conduct and contributing guidance welcoming and specific about how to ask for help.

| Avoid | Prefer |
|---|---|
| master (branch) | main |
| native speakers | fluent speakers |
| easy to use | (state what it does, with evidence) |

## Phrases to avoid

Beyond the [common list](../common/AGENTS.md#phrases-to-avoid):

- "Blazing fast" without a benchmark
- "Easy to use" with nothing to back it
- "Batteries included" and similar idiom
