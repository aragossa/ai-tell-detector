# ai-tell-detector

A Claude skill that audits a finished draft for the patterns that make text read as
AI-generated, and flags each one with the line it's on and a suggested fix.

24 checks, including:

- rhetorical symmetry ("it's not X, it's Y", triads, mirrored sentence pairs)
- filler transitions and hedges ("in today's world", "let's be honest")
- uniform rhythm: every sentence the same length, every paragraph the same shape
- the full template arc: situation, contrast, lesson, plug, question at the end
- gestured specificity ("a real number", "an actual example") with no number or example given
- fabricated personal experience, which is a factual problem rather than a stylistic one
- canned CTAs and compound two-part closing questions
- em-dash overload

The checklist was built from real published posts and comments that readers (and external
AI detectors) called out, then refined every time a new pattern slipped past it. One honest
caveat baked into the skill: external detector scores on the same text can spread 60+
points between tools, so the skill treats any single score as one data point, never a verdict.

Works in English and Russian. Both versions included.

## Install

Copy the folder for your language into `~/.claude/skills/`:

```bash
cp -r en/ai-tell-detector ~/.claude/skills/
```

or for the Russian version:

```bash
cp -r ru/ai-tell-detector ~/.claude/skills/
```

Then ask Claude to audit any finished draft before you publish it. Works in Claude Code and
Claude.ai (on plans with Skills support), and in other tools that read the open `SKILL.md` format.

## Part of a larger pack

This is one of 9 skills in the SMM Skill Pack for Claude (EN + RU): LinkedIn writing,
Telegram posts, content repurposing, hooks and CTAs, content calendar, visual briefs,
metrics analysis, and brand voice. Every skill ships with a real before/after test:
the same prompt run with and without the skill, both outputs unedited.

- [Gumroad ($19)](https://iploskov.gumroad.com/l/xqwbwh)
- [Boosty (RU)](https://boosty.to/aragossa/posts/9aebe4e4-518a-4690-a83f-65af94fc0521)

## License

MIT for everything in this repository.
