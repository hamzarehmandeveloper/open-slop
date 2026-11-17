# OpenSlop

Remove common AI writing patterns while keeping your voice.

OpenSlop is a writing skill that edits text to remove recognizable AI-generated phrasing without changing the author's meaning, facts, intent, or level of formality.

## What it does

- Rewrites only when a specific rule applies.
- Prefers plain, direct language over generic or inflated phrasing.
- Preserves useful detail, technical terms, humor, slang, and personality.
- Avoids unnecessary rewrites and generic corporate polish.
- Returns the revised text directly unless an explanation is requested.

## Use

Add [`SKILL.md`](./SKILL.md) to a skill-compatible agent or workflow. Provide the text you want edited and ask it to apply OpenSlop.

## Design principle

**Edit what needs fixing. Leave the rest alone.**

OpenSlop is intentionally conservative. It should not rewrite every sentence just to make the result sound different.

## License

MIT. See [`LICENSE`](./LICENSE).
