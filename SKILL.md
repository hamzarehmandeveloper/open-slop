---
name: open-slop
description: Remove common AI writing patterns from supplied text while preserving meaning and intended tone.
---

# OpenSlop

Edit the supplied text to remove recognizable AI writing patterns. Preserve the author's meaning, facts, intent, and appropriate tone. Do not add claims or polish the text into generic corporate prose.

## Process

1. Scan the text for the rules below.
2. Rewrite only where a rule applies.
3. Preserve useful specificity, natural voice, and the original level of formality.
4. Do not change factual meaning, names, numbers, or commitments unless the user asks.
5. Return the revised text directly. Do not add chatbot filler or explain every edit unless asked.

## Rules

Rule numbers are stable IDs. Keep the numbering even if a rule is removed later.

### Content

3. Superficial -ing phrases. Remove empty phrases such as "highlighting", "ensuring", "reflecting", "showcasing", and "fostering" when they add no concrete information. Keep them when they describe a real action or result.
5. Vague attributions. Remove phrases such as "Experts believe", "Industry reports suggest", and "Some critics argue" unless a specific source is named. Do not invent sources.

### Language

7. AI vocabulary. Prefer plain words over "Additionally", "crucial", "delve", "enduring", "enhance", "fostering", "garner", "interplay", "intricate", "landscape" when abstract, "pivotal", "showcase", "tapestry" when abstract, "testament", "underscore", and "vibrant".
8. Fancy ways to say "is". Replace "serves as", "stands as", "boasts", and "features" with direct wording such as "is" or "has" when that preserves the meaning.
9. "Not just X, but Y." State the point directly.
10. Rule of three. Do not force ideas into groups of three. Use the number that fits the meaning.
11. Synonym cycling. Pick one clear term and use it consistently instead of cycling through synonyms for the same thing.
12. False ranges. Do not write "from X to Y" when X and Y are not points on a meaningful scale. List the topics directly.

### Style

13. Em dash overuse. Avoid em dashes entirely. Use periods or commas. Do not replace them with en dashes or hyphens used as sentence dashes.
14. Colon overuse. Use colons mainly before lists or examples. Rewrite mid-sentence colon constructions when a normal sentence is clearer.
15. Boldface overuse. Do not bold every proper noun, acronym, or ordinary phrase.
16. Inline-header lists. Avoid bold labels that merely restate the following sentence. A bold lead-in is fine when it names an item and the following text adds new information.
17. Title case headings. Use sentence case headings.
18. Decorative emojis. Remove decorative emojis from headings and bullets unless they are part of the user's intended content.
19. Curly quotes. Replace curly quotes with straight quotes.

### Communication artifacts

20. Chatbot phrases. Remove "I hope this helps!", "Let me know if...", "Of course!", "Certainly!", and similar assistant filler when it is not part of the user's intended message.
22. Sycophantic tone. Remove praise such as "Great question!" and "You're absolutely right!" when it is unnecessary.

### Filler

23. Filler phrases. Replace "in order to" with "to", "due to the fact that" with "because", and "It is important to note that" with nothing.
24. Excessive hedging. Reduce stacked hedges such as "could potentially possibly be argued that it might" to the clearest accurate wording.
25. Generic conclusions. Replace broad claims such as "The future looks bright" with specific plans or facts, or remove them if they add nothing.

### Jargon

26. Abstract metaphor nouns. Prefer concrete words over "substrate", "wedge" as a verb, "vector" as an abstract method, "locus", "vantage", "nexus", "primitive" as a noun, "harness" as a metaphor, "surface" as in "API surface", "bedrock", "scaffolding" as a metaphor, "modality", "paradigm", "gold-plating", "ratchet" as a metaphor, "evacuate" for moving code, "endgame", and "north star". Use the actual mechanism or a plain word.

### Plain speech

27. Say what it does, not how it feels. Replace vague descriptions with concrete instructions, facts, mechanisms, or numbers. If a sentence gives the reader nothing concrete to know or do, cut it.
28. Shorten or split dense sentences. Use one main idea per sentence where possible. Drop clauses that make the reader backtrack.
29. Active voice. Prefer active voice and name the actor when known. Keep passive voice when the actor is unknown or does not matter.
30. Cut adverbs or use a stronger verb. Replace adverbs that prop up weak verbs with a stronger verb or a measurable result when available.
31. Prefer the plain word. Prefer "use" over "utilize" or "leverage", "help" over "facilitate", "many" over "numerous", and "if" over "in the event that".
32. Mannered prose. Remove unnecessary metaphors, aphorisms, rhetorical fragments, personification, figurative verbs, and stock framing when a literal phrase is available.
33. Over-compression. Restore missing articles, verbs, and context when shorthand forces the reader to decode the sentence. Turn symbol-heavy fragments into normal sentences.

## Guardrails

- Preserve the author's voice. "Unslop" does not mean "make formal".
- Keep intentional humor, slang, profanity, technical terms, or personality when they serve the author's purpose.
- Do not remove domain-specific terms merely because they are technical. Replace jargon only when a simpler accurate term exists.
- Do not rewrite every sentence. If a sentence is already natural, leave it alone.
- Do not introduce em dashes, curly quotes, decorative emojis, or generic AI-sounding filler.
