---
name: deslop
description: "Rewrites a piece of writing in place to remove AI-generated 'slop' tells: em dashes, parenthetical example lists, puffery, trailing significance clauses, promotional tone, weasel-word authority, and a watchlist of overused words. Use when asked to de-slop text, make writing sound less AI-generated, strip AI tells, or clean up prose. Works on any prose: emails, docs, blog posts, reports. Self-contained single file."
---

I have a piece of writing that reads as AI-generated. Rewrite it in place so it reads as if a careful human wrote it, removing the tells listed below. Keep my meaning, my facts, and my voice. Do not add anything.

## Workflow

1. **Identify the target.**
   - If a file path was given, read the file. The cleaned text replaces the original in that file.
   - If text was pasted into the conversation, work on that text and return the cleaned version.
   - If neither is clear, ask which text to clean before doing anything.

2. **First pass: structure and tone.** Read the whole text. Fix every item under "Punctuation and structure" and "Tone and substance" below. Work sentence by sentence. When a sentence wants an em dash, split it or repunctuate; when a clause editorializes about what a fact means, end the sentence at the fact.

3. **Second pass: the watchlist.** Go word by word against the "Overused-word watchlist." Replace each genuine hit with the plain alternative or cut it. Skip any word that is genuinely the right word in context (see Preservation rules); the list targets overuse, not the word itself.

4. **Rewrite in place.**
   - File target: apply the edits to the file.
   - Pasted target: return the cleaned text.
   Preserve the original structure, formatting, and length intent. This is an edit, not a rewrite from scratch.

5. **Report what changed.** After editing, give a short summary grouped by category, for example: "Removed 4 em dashes, 2 parenthetical example lists, cut 'leverage'/'robust'/'crucial', dropped 3 trailing significance clauses." Do not paste the full before-and-after unless asked. If the text was already clean, say so plainly rather than inventing changes.

## The rules

These patterns are what flag writing as AI-generated. Scrub every one.

### Punctuation and structure

- **No em dashes.** Use a period, comma, semicolon, or colon. If a sentence feels like it needs an em dash, split it into two sentences.
- **No parenthetical example lists.** Do not write "various methods such as A, B, or C" inside parentheses. Either work the examples into the sentence proper or cut them.
- **No rule-of-three lists where two items, or one, would do.** Do not pad to three for rhythm.
- **No sentence-final "as well."** Use "also" at the start of the sentence, or omit it.
- **No stacked hedging qualifiers.** "potentially could possibly allow" becomes "could allow," or just "allows."

### Tone and substance

- **No overdramatization.** No "catastrophic," "devastating," "unprecedented," "game-changing." State what is true, plainly. The facts carry the weight; adjectives do not.
- **No repetition or filler.** Do not restate the topic in its own explanation. Cut "As mentioned above," "it is worth noting that," "it should be noted that," "needless to say." Omit needless words.
- **No overexplanation.** State the point, then stop. If a clause does not change what the reader understands or does, cut it.
- **No inflated importance (puffery).** Do not puff a thing up by tying it to a larger theme or claiming it represents a broader trend. State the concrete point and stop. Cut framings such as: "plays a crucial, pivotal, vital, or key role," "underscores/highlights its importance," "represents a shift," "marks a turning point," "reflects a broader trend," "stands as" or "serves as," "is a testament to" or "is a reminder of," "sets the stage for," and "leaves an indelible mark."
- **No trailing significance clauses.** Do not bolt a participial clause onto the end of a sentence to editorialize about what a fact means. End the sentence at the fact. Cut tails and openers such as "highlighting...", "underscoring...", "emphasizing...", "ensuring...", "reflecting...", "symbolizing...", "fostering...", "cultivating...", "contributing to...", and "demonstrating a commitment to...", along with "valuable insights" and claims that something "aligns with" or "resonates with" a goal.
- **No promotional or advertisement tone.** This is writing, not marketing copy or a travel guide. Do not describe a thing with promotional adjectives: "boasts," "vibrant," "rich," "robust," "profound," "groundbreaking," "renowned," "cutting-edge," "seamless," "state-of-the-art," "diverse array," "nestled," "in the heart of," "showcasing," "exemplifies." Where something is genuinely good, say what is specifically true about it.
- **No weasel words or vague authority.** Do not attribute a claim to an unnamed authority such as "experts agree," "studies show," "it is widely recognized," or "best practice dictates" with no source named. Name the actual source or state the point directly. Do not append a formulaic "Despite these challenges..." softener, and do not add a speculative "Future Outlook" or "In conclusion" flourish. The text ends when the point is made.

### Overused-word watchlist

These words spike in post-2022 AI-generated text and read as slop. Rewrite each genuine hit to the plain alternative.

| Avoid | Use instead |
|-------|-------------|
| Additionally (starting a sentence) | "Also," or just lead with the fact |
| align with / resonate with | matches, follows, supports |
| boasts (meaning "has") | has |
| bolster | strengthen, support |
| crucial, pivotal, vital | important, or cut it |
| delve | examine, look at, dig into |
| emphasize, highlight, underscore (as significance verbs) | state the point plainly |
| enduring, lasting | cut it |
| enhance | improve, increase |
| ever-evolving, ever-changing | changing, or cut it |
| foster, cultivate | support, build, grow |
| furthermore, moreover | also, and, or just continue |
| garner | gain, collect, earn |
| interplay | interaction |
| intricate, intricacies | complex, details |
| journey (figurative) | cut it, or name the actual process |
| key (as an adjective) | main, primary, or cut it |
| landscape (as an abstract noun) | field, area, or cut it |
| leverage (as a verb) | use |
| meticulous, meticulously | careful, or cut it |
| navigate (figurative) | handle, deal with, work through |
| realm | area, field |
| robust | strong, or name the specific quality |
| seamless, seamlessly | smooth, or cut it |
| showcase | show, demonstrate |
| tapestry | cut it |
| testament | shows, or cut it |
| unlock (figurative) | cut it, or name what it enables |
| valuable | cut it, or name the specific value |
| vibrant | cut it |

## Preservation rules

These bound the edits. Breaking them turns a clean-up into a rewrite the author did not ask for.

- **Never change meaning or delete a fact.** If removing slop would drop information, rephrase to keep the information.
- **Leave quotations, code, and citations untouched.** Do not edit text inside quotation marks attributed to someone, fenced code blocks, inline code, URLs, or reference citations, even if it contains a watchlist word.
- **A watchlist entry targets overuse, not the word.** Keep a flagged word when it is genuinely the right one: "encryption key," "robust statistics," "the customer journey" as a defined product term, "delve" in a quoted source. Judgment over find-and-replace.
- **Preserve voice and register.** Match the author's existing tone. Do not make casual writing formal or formal writing casual.
- **Preserve formatting.** Keep Markdown, headings, lists, line breaks, and the document's structure.
- **Add nothing.** No new sentences, no new examples, no editorial notes inside the text. The only new output is the change summary in your reply.

## What this skill does NOT do

- Does not fact-check or correct claims.
- Does not restructure arguments or reorder sections.
- Does not impose a house style or a particular voice; it removes slop and leaves the author's voice.
- Does not translate, summarize, or expand the text.
