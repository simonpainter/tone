# Technical Documentation Tone Guide

Read [the common guide](../common/AGENTS.md) first. This file only covers what's specific
to reference documentation.

Documentation is the antidote to the guru problem. If the knowledge only lives in one
person's head, the system has a single point of failure wearing shoes. Write it down so
nobody has to go and ask Magic Jeff.

## What changes

- Be precise. Factual clarity beats personality here.
- Use present tense for system behaviour. "The gateway drops the packet", not "will drop".
- Use `you` for the reader and `we` for maintainer decisions.
- Drop the first-person anecdotes and the humour. Keep the plain wording.

## Scope

Say at the top what the document covers and what it doesn't. Half the frustration with docs
is finding out three pages in that you're in the wrong place.

## Structure

1. Purpose and scope
2. Prerequisites
3. Procedure
4. Expected result
5. Error handling and troubleshooting
6. References

## Style details

- Define acronyms on first use, every document. Don't assume the reader arrived via page one.
- Keep terminology stable. Pick one name for a thing and use it everywhere. Synonyms are a kindness to the writer and a trap for the reader.
- Use code formatting for commands, paths, flags, config keys, and values.
- Show expected output alongside commands. "Run this" is half an instruction.
- Label warnings and irreversible actions before the step, not after it.
- Use numbered steps for procedures and tables for configuration matrices.
- One canonical example per task path. Link the variants rather than inlining them all.
- Move deep theory to linked references. Keep the procedure walkable.
- Remove duplicate warnings and repeated definitions. Say it once, in the right place.

## Inclusive language additions

The [common baseline](../common/AGENTS.md#inclusive-language) applies. Docs are read under
pressure, often at 3am by someone who didn't build the system, so language that assumes
context they don't have is a real failure rather than a style nitpick.

- Don't assume tooling access, hardware, region, or network conditions.
- The effort-minimising words matter most here. `just`, `simply`, `easy`, and `trivial` all tell a stuck reader that they're the problem.
- Use neutral placeholder names and data. `example.com`, `alice` and `bob`, not in-jokes.
- Include accessibility guidance where it applies: keyboard paths, screen reader labels, contrast requirements, alt text on every screenshot and diagram.
- Don't rely on colour or position alone. "The red box on the right" fails for a lot of readers; name the element.

| Avoid | Prefer |
|---|---|
| native support | built-in support |
| normal behaviour | expected behaviour |
| the red box on the right | the **Advanced** panel |

## Phrases to avoid

Beyond the [common list](../common/AGENTS.md#phrases-to-avoid):

- "As we all know"
- "Should work", "should be fine" - test it and say what happens
- "See above", "as mentioned earlier" - link to the anchor instead
