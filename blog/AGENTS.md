# Blog Writing Tone Guide

Read [the common guide](../common/AGENTS.md) first. It carries the voice, the inclusive
language baseline, and the banned phrases. This file only covers language choices specific
to blog posts.

This is about how a post reads, not how a site is built. Tagging rules, frontmatter fields,
truncate markers, and file layout belong in the blog repo's own instructions, because
they're plumbing rather than language.

Blog writing is where the common voice runs at full strength: first person throughout,
humour allowed, opinions landed rather than hedged.

## How to open

Never start with a definition or a scene-setting throat-clear. Start with an anecdote, a
direct question, or the problem stated flatly. Get to the substance inside three sentences.

Openings that work:

- "I recently got drawn into a bit of LinkedIn rage bait: a post with a CCNA level question asking people to identify the broadcast domains in a given diagram."
- "When I set out to explore network latency in Azure, I had a simple goal: to understand how physical distance affects performance."
- "I had one of those mildly awkward moments that only bloggers and other people who publish opinions on the internet seem able to engineer for themselves."
- "Have we been sold a false bill of goods when it comes to gender equality in the workplace?"

Openings that don't:

- "In the ever changing world of cloud networking..."
- "Network latency is the time it takes for a packet to travel from source to destination."
- "In this post, we will explore..."

The first paragraph is doing the most work in the whole post. If a reader can't tell what
they're getting from it, they've already gone.

## Shape

- Keep the intro to 2-4 sentences. Say what the post is about and why it's worth reading, then move.
- Use subheadings every 2-4 paragraphs. Write them as statements where you can - "Latency doubles across regions" tells a skim-reader more than "Results".
- Don't lean on bullet points. Explain in prose; save lists for things that are genuinely a list.
- Target 600-1,200 words unless the topic needs more. Length should follow the argument, not a word count.

## Technical explanation

- Name the jargon, then give the plain-English gist immediately. "BGP (Border Gateway Protocol) is the routing protocol that powers the internet."
- Use real, runnable code - PowerShell, Python, YAML, whatever fits. Not decorative pseudocode.
- When pseudocode genuinely helps, write it Pythonic with 4-space indentation. Label anything outside the standard library (`math.sqrt()`) or give it a self-explanatory name (`calculate_network_latency()`).
- Use diagrams where they cut explanation text, not as decoration.
- Use tables for comparative data. Keep them terse and numeric.
- Use blockquotes for "for the curious" side-notes that would otherwise break the flow.
- Back claims with specific numbers wherever possible, and say where the numbers came from.

## How to end

Three endings work, and all three are fine:

1. Numbered practical takeaways after a technical post.
2. A direct question to readers after an opinion piece.
3. Just stopping, after a final reflective paragraph. No call to action needed.

What an ending shouldn't do is restate the post. Examples that land:

- "But fundamentally, the hard part is done. If you need to query BGP routes from Claude Desktop, you can now do that in a few minutes. That's the goal."
- "And if you spot accessibility issues on this blog, please open a GitHub issue or send me a message on LinkedIn. Accountability is the point."

## Inclusive language additions

The [common baseline](../common/AGENTS.md#inclusive-language) applies. On top of it:

- Link to earlier posts rather than assuming the reader followed a series. Anyone can arrive at any post from a search result.
- Don't assume shared industry history. "Back when we all ran Frame Relay" excludes most of the audience.
- Where a post covers accessibility or inclusion, cite the specific standard or test rather than speaking in generalities.
- Opinion posts get more latitude on strong views, none on stereotyping.
