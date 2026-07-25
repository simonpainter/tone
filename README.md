# AI Tone Guides Collection

Practical tone guides for modern LLM workflows. They are designed to produce output that is clear, low-hype, inclusive, and cost-efficient to generate.

## What changed in this refresh

This repository now assumes current LLM capabilities (2026-era models):

1. Models are strong at structure and rewriting, so prompts should be explicit and compact.
2. Token cost matters, so output length and context size are treated as first-class constraints.
3. Inclusive language is not optional; it is part of quality, not a nice-to-have.
4. Tone should be plain-spoken and specific: calm confidence, concrete examples, no marketing noise.

## Repository-wide defaults

Use these rules with every guide in this repo.

### 1) Output contract

- Lead with the answer or outcome.
- Keep response length proportional to the ask.
- Prefer short paragraphs over long bullet-heavy blocks.
- Avoid repeating the prompt back to the user.
- State uncertainty directly instead of padding.

### 2) Token efficiency

- Set a target length before generation (for example: 120 words, 5 bullets, 1 table).
- Include only required context in the prompt; do not paste large irrelevant source text.
- Reuse stable templates and section headings rather than regenerating structure each time.
- Ask for one draft, then one focused revision pass; avoid multi-pass churn.
- Prefer small examples over long synthetic examples unless the task explicitly needs depth.

### 3) Inclusive language recommendations

- Use people-first language unless a community clearly prefers identity-first wording.
- Default to gender-neutral terms (`they`, `everyone`, `team`, `folks`).
- Avoid assumptions about culture, age, disability, religion, family structure, or background.
- Prefer global plain wording over region-specific idioms.
- Describe access requirements, not personal traits.

Common replacements:

| Avoid | Prefer |
|---|---|
| guys | everyone / team |
| manpower / man-hours | effort / staffing / person-hours |
| sanity check | quick check / sense check |
| normal user | typical user / most users |
| blacklist / whitelist | denylist / allowlist |
| master/slave | primary/secondary or protocol-specific terms |

## Available tone guides

- [Blog Writing](/blog/CLAUDE.md)
- [Professional Emails](/email/CLAUDE.md)
- [Slide Decks](/slide-decks/CLAUDE.md)
- [Strategy Documents](/strategy-documents/CLAUDE.md)
- [Social Media (LinkedIn Focus)](/social-media/CLAUDE.md)
- [Technical Documentation](/technical-documentation/CLAUDE.md)
- [User Guides & Tutorials](/user-guides/CLAUDE.md)
- [GitHub READMEs](/github-readmes/CLAUDE.md)

## Recommended prompt pattern

1. **Task:** what to produce.
2. **Audience:** who it is for and what they already know.
3. **Guide:** paste the relevant `CLAUDE.md`.
4. **Token budget:** max words/sections/examples.
5. **Quality checks:** factual accuracy, inclusive language, and actionability.

## Customisation

Adapt these guides for domain terminology, regulatory constraints, and audience expertise, while keeping the shared efficiency and inclusion rules intact.
