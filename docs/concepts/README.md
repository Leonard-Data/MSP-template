# Documentation ownership and organization

MSP Portal is the publishing layer, but each source repository owns its own documentation.

## Ownership model

- The source repository owns the Markdown, assets, and metadata in `.docs-source.yml`.
- The portal owns aggregation, navigation, search, and presentation across many sources.
- Teams update documentation close to the code, process, or domain they already maintain.

This split keeps content maintenance local while giving readers one place to browse and search.

## Organizing a source repository

Use folders to signal the reader's intent, not to satisfy a quota.

- Keep foundational explanations in `concepts/`.
- Put step-by-step work in `guides/`.
- Put exact lookup material in `reference/`.
- Add `architecture/`, `patterns/`, `components/`, `examples/`, `snippets/`, and `troubleshooting/` when they help readers find information faster.

If one page starts serving multiple jobs, split it by reader need and cross-link the pages.

## Practical conventions

- Keep filenames descriptive and stable.
- Use relative links so pages work in both GitHub and MSP Portal.
- Prefer small, focused pages over one long catch-all document.
- Update `.docs-source.yml` when the section name, category, tags, or navigation changes.
