# MSP Template

Starter repository for documentation sources that plug into MSP Portal.

This template gives a new documentation section a predictable shape without forcing every folder to be used on day one. Keep the content plain Markdown, keep assets local to the repository, and adjust the structure as the section grows.

## How this repository fits into MSP Portal

Each MSP documentation source owns its own `docs/` content and `.docs-source.yml` metadata.

MSP Portal then:

1. reads `.docs-source.yml`
2. syncs the repository's `docs/` directory
3. builds shared navigation and search from the source metadata

That keeps documentation close to the team that maintains it while still publishing through one portal.

## Getting started

1. Review `.docs-source.yml` and set the source `id`, `name`, `category`, and `description` for your section; add `tags` only if they help discovery.
2. Update `docs/README.md` so the overview matches your subject area.
3. Keep the folders you need today; if you remove one, update `.docs-source.yml` so `navigation` only lists folders that still exist.
4. Add pages in the folder that best matches the reader's question.
5. Open a pull request with link and asset checks completed.

## Repository layout

| Path | Purpose |
| --- | --- |
| `.docs-source.yml` | Source metadata consumed by MSP Portal sync and build scripts |
| `docs/README.md` | Landing page for the documentation section |
| `docs/concepts/` | Foundational ideas, ownership, terminology, and mental models |
| `docs/architecture/` | System shape, boundaries, decisions, and diagrams |
| `docs/guides/` | Step-by-step how-to content |
| `docs/patterns/` | Repeatable approaches and recommended structures |
| `docs/components/` | Reusable building blocks, modules, or feature areas |
| `docs/examples/` | Worked examples and sample implementations |
| `docs/snippets/` | Small copy-pasteable fragments |
| `docs/troubleshooting/` | Common mistakes, failure modes, and recovery steps |
| `docs/reference/` | Schemas, conventions, commands, and lookup material |
| `docs/assets/` | Images, diagrams, and other linked static assets |
| `.github/PULL_REQUEST_TEMPLATE.md` | Review checklist for documentation changes |

## Choosing the right folder

Use the lightest folder that matches the reader's need:

- **Concepts** for "what is this and who owns it?"
- **Architecture** for "how is it structured?"
- **Guides** for "how do I do it?"
- **Patterns** for "what approach should I repeat?"
- **Components** for "what reusable pieces exist?"
- **Examples** for "show me a complete sample"
- **Snippets** for "give me the small piece"
- **Troubleshooting** for "what went wrong?"
- **Reference** for "what are the exact fields, commands, or rules?"

If a page could fit in two places, choose the folder readers are most likely to browse first and link to related material instead of duplicating it.

## Markdown, links, and images

- Prefer plain Markdown that renders well on GitHub and in static site pipelines.
- Use one `#` heading per file and descriptive filenames such as `add-a-documentation-page.md`.
- Keep links relative inside the repository so they survive sync into MSP Portal.
- Store images and diagrams in `docs/assets/` and use relative paths from the page that references them.
- Add alt text for images and avoid embedding text only in screenshots when a Markdown explanation would be clearer.

## Review expectations

A documentation pull request should make it easy for reviewers to answer:

- what changed
- which audience the page is for
- whether links and assets render correctly
- whether `.docs-source.yml` still reflects the section
- whether the new page sits in the right folder

See `CONTRIBUTING.md` for the working agreement used by this template.
