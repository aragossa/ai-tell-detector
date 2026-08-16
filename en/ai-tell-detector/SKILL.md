---
name: ai-tell-detector
description: Audits a finished draft for the patterns that make text read as AI-generated — rhetorical symmetry, generic filler, uniform rhythm, over-resolved story arcs, missing human roughness, fabricated personal experience — and flags each one with a fix. Use before publishing anything, or when a draft "feels AI" but you can't say why.
---

# AI Tell Detector

Human AI-detectors (Grammarly, Gemini, GPTZero and similar) and human readers catch the
same handful of patterns. This skill runs that same audit before you publish, so you
catch it instead of your reader.

## Input

The finished draft (post, comment, email, DM). No other iteration needed — feed it the
final text, not a topic.

## What it checks

1. **Rhetorical symmetry.** "It's not X — it's Y", "not just A, but B", triads ("faster,
   better, stronger"). Flag every instance with the line it's on.
2. **Filler transitions and hedges.** "In today's world", "It's worth noting",
   "Let's be honest", "At the end of the day", "Spoiler:". These add length, not meaning.
3. **Uniform rhythm and structure.** If every sentence is roughly the same length and
   every paragraph the same shape, call it out. Also check the beat-by-beat shape of
   the whole piece: situation → contrast → lesson → plug → question is a template, not
   a style — flag it even if no single sentence is the problem.
4. **Generic abstraction over specifics.** Claims with no number, name, date, or quote
   behind them ("many companies struggle with...", "in my experience..." with nothing
   concrete after it).
5. **Fabricated personal experience.** Any claim of a specific past event, feeling, or
   action ("this happened to me too", "I went through the same thing") that the author
   didn't actually confirm happened. This is worse than a stylistic tell — it's a
   factual claim that may be false. Ask before assuming any personal anecdote is true.
6. **Canned CTA / sign-off.** "What do you think? Let me know in the comments!",
   "Thoughts?", a compound two-part question at the end.
7. **Em-dash overload.** More than one or two in a short post is a tell on its own.
8. **Gestured specificity without delivery.** Phrases that name-drop the idea of a
   concrete detail without ever showing it — "a real number," "an actual example,"
   "eight of these" — with no number or example actually given anywhere in the text.
   This reads as specific but is functionally as empty as rule 4's generic abstraction;
   flag it as its own category since it's easy to mistake for real concreteness.
9. **Aphoristic mic-drop line.** A short standalone sentence engineered to sound like
   a takeaway or moral — "X did more work than Y ever did," "it always comes down to
   Z" — even without the "not X — it's Y" framing already covered by rule 1. If a
   sentence could be pulled out and used as a motivational-poster caption, flag it.
10. **Over-resolved full arc.** The whole piece maps cleanly onto problem → numbers →
    cause → pattern list → fix → product plug → question, with every beat closed and
    nothing left loose — even if no single sentence trips rules 1-9. This is one of the
    strongest signals multiple independent reviewers converge on; a real off-the-cuff
    post usually leaves at least one thread hanging. Concrete check: label each paragraph
    with the one job it does (setup, analysis, experiment, result, context, question) —
    if every paragraph does exactly one distinct job with no overlap or mess, that clean
    division is the tell, independent of any single sentence.
11. **Asyndetic 3-4 item descriptor lists.** Any run of three or four abstract nouns or
    descriptors strung together with commas and no connective tissue ("rhetorical
    contrasts, symmetrical triads, invented anecdotes, filler that says nothing") is a
    tell on its own, separate from the adjective-triad-in-a-contrast case in rule 1.
    Generative models default to grouping in exactly 3-4. Cut to one or two items, fold
    it into a plain sentence, or swap one item for something concrete. A trailing hedge
    after the list ("...that kind of thing") doesn't neutralize it — the three-comma core
    is still what gets caught.
12. **Missing human roughness.** A piece with zero hedges, asides, self-corrections,
    informal register breaks, or an unresolved tangent reads as over-polished no matter
    what else it passes. Don't invent one — that's rule 5's territory — ask the author
    whether a genuine aside or hedge got edited out, and put it back if so.
13. **Meta-topic amplifier.** When the post's subject is itself AI writing, AI
    detectors, or sounding human, every tell above reads as more damning because the
    irony is legible to readers and classifiers alike. Apply the whole checklist more
    strictly on this topic than you would elsewhere.
14. **Parallel numeric triplets.** Reporting several data points in identical repeated
    syntax ("A said 8%. B said 71%. C said 82%.") reads as manufactured evidence through
    the rhythm alone, independent of whether the numbers are real. Vary the sentence
    construction when citing multiple real data points instead of a clean parallel
    triplet.
15. **Self-referential meta-wink.** A line that names its own rhetorical device while
    performing it right now ("turns out lists like this one are exactly what trips
    detectors") is itself a recognizable AI habit — self-aware commentary-on-craft as a
    flourish. Don't defuse a tell by narrating it in the same breath; cut the tell
    instead.
16. **Canned curiosity opener.** "Curious if...", "curious to hear...", "keen to
    know..." at the start of a closing question is as templated as "Thoughts?" — treat
    it as part of rule 6's canned-CTA category and swap in a plain, specific question.
17. **Evidentiary numeric tone.** Breaking a parallel triplet's syntax (rule 14) isn't
    enough by itself. Numbers delivered as flat, confident proof with no hedge, context,
    or texture (when you checked, how sure you are, what surprised you) still read as
    manufactured. Add real texture around the data, not just a different sentence shape.
18. **Plug-formula CTA.** "[Product] is on [Platform A] and [Platform B] if you want
    [it]" is a recognizable soft-ad template no matter how casual the wording is — the
    shape is the tell. Fold the mention into the story earlier instead of tacking it on
    as a separate closing beat, or cut the "if you want" invite frame entirely.
19. **Observation-then-reversal beat.** "X felt like a win until I checked Y", "X
    happened... until Y" — a reversal spread across a clause or full sentence — is rule
    1's "not X — it's Y" contrast wearing a narrative disguise. Flag it the same way even
    when it unfolds over a sentence instead of packing into one clause.
20. **Over-composed hedge.** A hedge that lands as a complete, tidy sentence ("Not sure
    which of the three to actually trust") reads as a polished stand-in for uncertainty,
    not the real thing. Genuine uncertainty in human writing tends to run on, trail off,
    or double up ("so now I honestly have no idea what's going on") instead of closing as
    a well-formed clause. When adding a hedge for rule 12, check the hedge itself isn't
    suspiciously clean.
21. **Mandatory closing question.** Ending every single post with a question, even one
    that reads as organic, is itself a structural formula that marketing copy and AI
    drafts default to. A real human post ends wherever the thought stops: a flat
    statement, a trailing aside, sometimes nothing. Don't treat a closing question as
    required — flag a draft when the ending feels obligatory rather than earned, and
    prefer no explicit question over a forced one.

## Output

A table: line/phrase → what it triggers → suggested fix. Then one line: pass / needs
revision, with the count of flags found. Never rewrite the whole text unless asked —
just point at what to cut or change.

## Hard rules

- Don't invent what the fix should say if it requires a fact you don't have (a real
  number, a real personal story) — mark it [ASK AUTHOR] instead of writing a plausible-
  sounding replacement.
- This is a checklist, not a guarantee: passing it does not mean an AI-detector will
  score 0%, only that the common tells are gone.
- Don't quote a percentage from an external AI-detector (or from asking another model
  to "rate this like Grammarly would") as if it were a stable measurement. Two
  different models scoring the same text have landed 0-10% apart from 65-85% on
  identical input — the number is a stylistic vibe-check with a percentage bolted on,
  not a calibrated classifier. If you report a detector score at all, report it as one
  data point among several, not as the verdict.
- External detectors often can't tell "human-written, AI-edited" apart from
  "AI-generated" — a well-scrubbed human draft that used any AI help drafting or editing
  can still land 40-70% on some tools. That's not a checklist failure: the goal here is
  removing structural tells, not chasing a specific score on any one detector.
