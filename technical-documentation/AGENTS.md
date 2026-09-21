# Technical Documentation Tone Guide

Documentation is the antidote to the guru problem. If the knowledge only lives in one
person's head, the system has a single point of failure wearing shoes. Write it down so
nobody has to go and ask Magic Jeff.

Read [the blog guide](../blog/AGENTS.md) for the underlying voice. Docs are more neutral
than a blog post, but they're still written by a person for a person.

## Core voice

- Use UK English.
- Be precise. Factual clarity beats personality here.
- Use present tense for system behaviour. "The gateway drops the packet", not "will drop".
- Use `you` for the reader and `we` for maintainer decisions.
- Drop the first-person anecdotes. Keep the plain wording.

## Scope

Say at the top what the document covers and what it doesn't. Half the frustration with
docs is finding out three pages in that you're in the wrong place.

## Structure

1. Purpose and scope
2. Prerequisites
3. Procedure
4. Expected result
5. Error handling and troubleshooting
6. References

Use `##` and `###` in order. Never skip a level - screen reader users navigate by heading
structure, and a jump from `##` to `####` breaks that.

## Style details

- Define acronyms on first use, every document. Don't assume the reader arrived via page one.
- Keep terminology stable. Pick one name for a thing and use it everywhere. Synonyms are a kindness to the writer and a trap for the reader.
- Use code formatting for commands, paths, flags, config keys, and values.
- Show expected output alongside commands. "Run this" is half an instruction.
- Label warnings and irreversible actions clearly and before the step, not after it.
- Use numbered steps for procedures and tables for configuration matrices.
- One canonical example per task path. Link the variants rather than inlining them all.
- Mermaid diagrams need `accTitle` and `accDescr`, plus a prose sentence saying what they show.
- Move deep theory to linked references. Keep the procedure walkable.

## Inclusive language

Docs are read under pressure, often at 3am by someone who didn't build the system.
Language that assumes context they don't have is a real failure, not a style nitpick.

- Use gender-neutral language by default (`they`, `the operator`, `the reader`).
- Don't assume ability, prior experience, tooling access, hardware, region, or network conditions.
- Use people-first language unless a group clearly prefers identity-first.
- Never minimise effort. `just`, `simply`, `easy`, `trivial`, and `obviously` all tell a stuck reader that they're the problem.
- Describe requirements and behaviours, not personal traits. "Requires keyboard navigation", not "for users who can't use a mouse".
- Prefer globally clear wording. Avoid idiom and culture-specific examples.
- Use neutral placeholder names and data. `example.com`, `alice` and `bob`, not in-jokes.
- Include accessibility guidance where it applies: keyboard paths, screen reader labels, contrast requirements, and alt text on every screenshot and diagram.
- Don't rely on colour or position alone. "The red box on the right" fails for a lot of readers; name the element.

| Avoid | Prefer |
|---|---|
| master/slave | primary/secondary, leader/follower, or the protocol's own terms |
| blacklist/whitelist | denylist/allowlist, blocklist/allowlist |
| dummy value | placeholder value |
| sanity check | validation check, verification step |
| grandfathered | legacy status, existing configuration |
| man-hours | person-hours, effort |
| normal user, normal behaviour | typical user, expected behaviour |
| native support | built-in support |
| he, she (generic) | they |

Where a protocol or vendor API still uses the old terms, use the exact term in the code
block and the neutral term in the prose. Accuracy wins in the command; clarity wins in the
sentence around it.

## Token-efficient generation

- Keep explanations tight and link the theory.
- Remove duplicate warnings and repeated definitions - say it once, in the right place.
- Generate one section at a time when iterating on a long document.

## Phrases to avoid

- "Obviously", "clearly", "as we all know", "of course"
- "Just do X", "simply run", "it's easy to", "trivially"
- "Should work", "should be fine" - test it and say what happens
- "See above", "as mentioned earlier" - link to the anchor instead
- "In the ever changing world of..."
