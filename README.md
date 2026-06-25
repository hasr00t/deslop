# deslop

A [Claude](https://claude.com/claude-code) skill that rewrites a piece of writing in place to remove AI-generated "slop" tells, while keeping your meaning, your facts, and your voice.

It targets the patterns that instantly flag prose as machine-written: em dashes, parenthetical example lists, puffery, trailing significance clauses, promotional adjectives, vague appeals to authority, and a watchlist of words that spike in post-2022 AI text (crucial, robust, leverage, delve, underscore, showcase, and friends).

It works on any prose: emails, documentation, blog posts, reports, README files.

## What it does

- **Rewrites in place.** Point it at a file and it edits the file. Paste text into the conversation and it returns the cleaned version.
- **Two passes.** First a structure-and-tone pass, then a word-by-word pass against the overused-word watchlist.
- **Reports what changed.** You get a short summary by category, not a wall of diff.

## What it does not do

It does not fact-check, restructure your arguments, impose a house style, or translate/summarize. It removes slop and leaves your voice intact. A flagged word stays when it is genuinely the right word ("encryption key," "robust statistics"); the watchlist targets overuse, not the word.

## Install

Copy the skill into your Claude skills directory.

**Claude Code (user-level):**

```sh
git clone https://github.com/<your-username>/deslop.git
cp -r deslop/deslop ~/.claude/skills/deslop
```

**Or drop in the packaged skill.** `deslop.skill` is a zip of the `deslop/` skill folder. Unzip it wherever your Claude environment loads skills from.

After installing, the skill is available to Claude. Invoke it by asking, for example:

- "Deslop this file: `./blog-post.md`"
- "Make this sound less AI-generated:" (then paste the text)
- "Strip the AI tells from `README.md`"

## The rules, in brief

**Punctuation and structure**

- No em dashes. Split the sentence or repunctuate.
- No parenthetical example lists.
- No rule-of-three padding.
- No sentence-final "as well."
- No stacked hedging ("potentially could possibly").

**Tone and substance**

- No overdramatization, filler, or overexplanation.
- No puffery or inflated importance.
- No trailing significance clauses ("highlighting...", "underscoring...").
- No promotional adjectives ("boasts," "vibrant," "seamless").
- No weasel-word authority ("experts agree," "studies show") with no source named.

**Overused-word watchlist**

A table of ~30 words (crucial, robust, leverage, delve, foster, navigate, seamless, tapestry, ...) each mapped to a plain replacement.

The full, authoritative rule set lives in [`deslop/SKILL.md`](deslop/SKILL.md).

## Credit

The rule set is generalized from the anti-AI-tell rules in a Black Hills Information Security report-writing skill, with all domain-specific voice rules removed so it applies to any writing.

## License

MIT. See [LICENSE](LICENSE).
