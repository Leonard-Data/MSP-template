# Contributing

Thanks for improving this documentation source.

The goal of this template is balanced structure: enough consistency for MSP Portal to sync and present the content well, without forcing a rigid process for small updates.

## First steps for contributors

1. Read `docs/README.md` to understand the current section structure.
2. Confirm whether the change belongs in an existing page or a new file.
3. Update `.docs-source.yml` only when source-level metadata changes.
4. Check links, image paths, and headings before opening a pull request.

## Folder selection guidance

Choose the folder based on the reader's job:

- `docs/concepts/` for context, ownership, and definitions
- `docs/architecture/` for structure and technical decisions
- `docs/guides/` for step-by-step tasks
- `docs/patterns/` for reusable approaches
- `docs/components/` for reusable parts or feature areas
- `docs/examples/` for worked samples
- `docs/snippets/` for small reusable fragments
- `docs/troubleshooting/` for common issues and fixes
- `docs/reference/` for exact fields, commands, and conventions
- `docs/assets/` for linked images and static files

When a page overlaps multiple folders, put it where readers will look first and link to the related page rather than duplicating content.

## Markdown conventions

- Use plain Markdown that stays readable on GitHub.
- Keep one top-level heading per file.
- Prefer short sections, descriptive headings, and concrete examples.
- Use fenced code blocks with a language when it helps readability.
- Choose clear kebab-case filenames.
- Avoid raw HTML unless Markdown cannot express the content cleanly.

## Links and images

- Use relative links for pages and assets within the repository.
- Keep images in `docs/assets/` unless a subfolder makes ownership clearer.
- Add meaningful alt text.
- Prefer SVG or compressed PNG/WebP for diagrams when practical.
- Remove or replace broken links before requesting review.

## Metadata expectations

`.docs-source.yml` is the contract MSP Portal uses to discover and organize this source.

Update it when you change:

- the source name or description
- the category
- the set of tags
- the folder list represented in `navigation`
- the documentation root if `docs_path` changes

For field-by-field guidance, see `docs/reference/docs-source-yml.md`.

## Review expectations

A pull request should describe:

- the documentation scope
- the paths changed under `docs/`
- whether `.docs-source.yml` changed
- the link and asset checks you ran
- anything reviewers should open locally or review carefully

If the change adds a new page, reviewers should be able to answer three questions quickly: why this page exists, why it belongs in that folder, and how readers will find it.

## Connection to MSP Portal

This repository is a source, not the portal itself. Keep content source-owned and portable:

- do not rely on portal-only components to make a page understandable
- keep relative links working from the source repository
- avoid assumptions that only make sense inside one product area unless the repository is explicitly about that area

That keeps the template reusable for future MSP documentation sections.
