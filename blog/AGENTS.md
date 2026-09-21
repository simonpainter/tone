# Blog Writing Tone Guide

This is the anchor guide for the whole repo. The other guides bend this voice to fit
their format, but they don't replace it.

## The voice in one paragraph

Write like a practitioner explaining something to a friend over coffee. UK English,
first person, contractions, calm confidence. I've usually tested the thing myself, so
the writing should sound like someone reporting what happened rather than someone
selling an idea. Plain words beat clever ones. Understatement beats hype.

## Core rules

- Use UK English spellings and grammar (`optimisation`, `behaviour`, `organisation`).
- Aim for a Flesch reading score of 80 or higher.
- Use the active voice.
- Use contractions - `don't`, `won't`, `it's`, `I've`.
- Use first-person singular (`I`, `my`, `me`), not the royal `we`.
- Avoid adverbs. Cut `really`, `very`, `incredibly`, `extremely`.
- Avoid buzzwords. Use jargon when it's the right word, then explain it in the next breath.
- Format in Markdown.

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

## Rhythm

Most sentences run 15-30 words. Most paragraphs run 2-4 sentences. After a dense
explanatory block, drop a short standalone line for emphasis. That contrast is the whole
trick.

Worked examples:

- "Pretty boring so far, right? The more distance, the more latency - not exactly breaking news."
- "So I ran an audit on simonpainter.com."
- "That thought was annoyingly well aimed."
- "Fixing a site once is satisfying. Keeping it fixed is the real work."

Use the spaced hyphen ` - ` for asides. Don't build long em-dash chains; that cadence
reads as machine-written.

## Stance

Ground claims in something I actually did: a test, a tool I built, an incident, a
conversation. Abstract theory with no anchor is the weakest thing this blog can publish.

Hedge on facts, not on conclusions. It's fine to say the sample size is too small, then
still land on a clear opinion. What's not fine is mush.

- "However, it's important to note that the sample size is currently too small to draw definitive conclusions about which approach is more effective."
- "I don't have all the answers, but I'm convinced that we can do better than the status quo."
- "I'm not a botanist or agricultural expert, I was an IT professional..."

Admit when I was wrong. It's more useful to readers than being right was.

## Humour

Dry, understated, self-deprecating. Never a gag for its own sake, and never at anyone
else's expense. Parenthetical asides and the occasional strikethrough joke earn their place.

- "Cue an A-Team style musical montage and another evening lost to an ADHD hyperfocus session."
- "the initial versions read like they were written by an overzealous recruiter after three espressos."
- "I found myself constantly reminding the AI: 'I'm British. Tone it down a notch... or five.'"
- "somewhere between jetwashing the patio and enjoying the sunshine on a rare day off"

Understatement carries disapproval better than outrage does. "A raised eyebrow" does more
work than a paragraph of complaint.

## Analogies

Use an analogy when it makes a hard idea land faster, not as decoration. The best ones run
through a whole post rather than appearing once.

- "It's the physical equivalent of air-gapping critical backups."
- "Accessibility work is often like network maintenance: if it is obvious afterwards, you may have done too much."
- "We didn't break the glass ceiling; we just built a bigger, more demanding workspace underneath it."
- "the web equivalent of mumbling into the carpet whenever a screen reader turned up"

## Technical explanation

- Name the jargon, then give the plain-English gist immediately. "BGP (Border Gateway Protocol) is the routing protocol that powers the internet."
- Use real, runnable code - PowerShell, Python, YAML, whatever fits. Not decorative pseudocode.
- When pseudocode genuinely helps, write it Pythonic with 4-space indentation. Label anything outside the standard library (`math.sqrt()`) or give it a self-explanatory name (`calculate_network_latency()`).
- Use Mermaid diagrams where they cut explanation text. Always include `accTitle` and `accDescr`, and follow the diagram with a sentence that summarises it in prose for anyone not seeing it.
- Use tables for comparative data. Keep them terse and numeric.
- Use blockquotes for "for the curious" side-notes that would otherwise break the flow.
- Back claims with specific numbers wherever possible.

## Structure

- `##` for major sections, `###` for subsections. Never skip a heading level.
- Keep the intro to 2-4 sentences before the `<!-- truncate -->` marker.
- Use short paragraphs. Use subheadings every 2-4 paragraphs.
- Don't lean on bullet points. Explain in prose; save lists for things that are genuinely a list.
- Target 600-1,200 words unless the topic needs more.

Endings can go three ways, and all three are fine:

1. Numbered practical takeaways after a technical post.
2. A direct question to readers after an opinion piece.
3. Just stopping, after a final reflective paragraph. No call to action needed.

What endings shouldn't do is restate the post. Examples that land:

- "But fundamentally, the hard part is done. If you need to query BGP routes from Claude Desktop, you can now do that in a few minutes. That's the goal."
- "And if you spot accessibility issues on this blog, please open a GitHub issue or send me a message on LinkedIn. Accountability is the point."

## Inclusive language

This isn't a compliance box. Writing that assumes things about the reader is just worse
writing, and it's the kind of thing I'd want flagged before publishing.

- Use gender-neutral language by default (`they`, `everyone`, `folks`, `team`).
- Don't assume age, gender, ethnicity, disability, religion, culture, or family structure.
- Use people-first language unless a group clearly prefers identity-first language.
- Prefer globally clear wording over local idiom, slang, or culture-specific references.
- Describe requirements and behaviours, not personal traits. Say "requires keyboard input", not "for able-bodied users".
- Don't build humour on stereotypes.
- If my wording might exclude people, suggest a neutral rewrite rather than quietly changing it.

Preferred alternatives:

| Avoid | Prefer |
|---|---|
| guys | everyone, team |
| manpower, man-hours | effort, staffing, person-hours |
| sanity check | quick check, sense check |
| normal user | typical user, most users |
| master/slave | primary/secondary, leader/follower, or the protocol's own terms |
| blacklist/whitelist | denylist/allowlist, blocklist/allowlist |
| dummy value | placeholder value |
| grandfathered | legacy status |

Accessibility applies to the post itself, not just its subject. Alt text on images,
`accTitle`/`accDescr` on Mermaid diagrams, descriptive link text instead of "click here",
and headings in order.

## Token-efficient generation

- Set a target length before drafting. Write one draft, then one focused revision pass.
- Keep intros short and skip the throat-clearing.
- One worked example per idea. Don't generate near-duplicate examples.
- Don't restate the same point across intro, body, and conclusion.
- Only paste source material that's actually relevant to the draft.

## Tagging

Every post gets **at most 3 tags**, all of which must already exist in `blog/tags.yml`.

Drop these first when trimming, because they're too generic to filter anything useful:
`networks`, `cloud`, `security`, `architecture`.

Favour tags in this order:

1. Technology-specific: `dns`, `bgp`, `expressroute`, `private-link`, `terraform`, `ipv6`, `anycast`, `mcp`, `firewall`, `zero-trust`, `ospf`, `dhcp`, `sdwan`, `load-balancing`, `high-availability`, `performance`, `troubleshooting`, `monitoring`, `cicd`, `github-actions`, `docusaurus`, `ai`, `algorithms`, `routing-protocols`, `netbox`, `enforza`, `nfc`, `making`
2. Generic tools: `python`, `bash`, `programming`, `scripting`, `automation`, `github`
3. Platform: `azure`, `aws`
4. Content type: `opinion`, `educational`, `labs`, `personal`
5. Catch-all: `business`, `career`, `documentation`, `migration`

Don't invent a tag without adding it to `blog/tags.yml` too.

## Phrases to avoid

Formal and academic filler:

`it is worth noting`, `furthermore`, `consequently`, `in terms of`, `one may argue`,
`it is imperative`, `this suggests that`, `thus`, `it is evident that`, `notwithstanding`,
`pertaining to`, `utilize` (use `use`), `be advised`, `hence`, `indicate`, `facilitate`,
`subsequently`, `moreover`, `it can be seen that`, `in the ever changing world of`.

Hype and dismissiveness:

`game-changing`, `revolutionary`, `best-in-class`, `unparalleled`, `simply`, `just`,
`obviously`, `clearly`, `of course`.

If `revolutionary` appears, it should be because I'm taking the mickey out of someone
who used it seriously.

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
