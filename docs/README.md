# Documentation overview

Use this `docs/` tree as a starting point, not a checklist.

The standard MSP structure gives readers a predictable place to look for common kinds of content, while still letting each source keep only the folders it needs.

## How to use this structure

- Keep `docs/README.md` as the landing page for the section.
- Add pages to the folder that best matches the reader's question.
- Leave lightweight `README.md` files in folders that need a visible landing page or need to stay in Git before more content exists.
- Prefer links between related pages over copying the same material into multiple folders.

## Section map

- [`concepts/`](concepts/README.md) — ownership, definitions, and mental models
- [`architecture/`](architecture/README.md) — structure, boundaries, and decisions
- [`guides/`](guides/README.md) — task-focused how-to content
- [`patterns/`](patterns/README.md) — repeatable approaches
- [`components/`](components/README.md) — reusable parts and feature areas
- [`examples/`](examples/README.md) — worked examples
- [`snippets/`](snippets/README.md) — small reusable fragments
- [`troubleshooting/`](troubleshooting/README.md) — common issues and fixes
- [`reference/`](reference/README.md) — exact fields and conventions
- [`assets/`](assets/README.md) — linked images and static files

## Keep it portable

MSP Portal syncs Markdown from source repositories. To keep the content portable:

- use relative links
- keep assets inside the repository
- avoid hidden dependencies on portal-only rendering
- write pages so they still make sense when viewed directly on GitHub
