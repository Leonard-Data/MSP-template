# `.docs-source.yml` reference

`.docs-source.yml` is the metadata contract between this repository and MSP Portal.

## Required fields used by the current portal scripts

| Field | Type | Purpose |
| --- | --- | --- |
| `id` | string | Stable source identifier used for URLs and aggregation |
| `name` | string | Display name shown to readers |
| `category` | string | Portal grouping label |
| `description` | string | Short summary for listings and search context |
| `docs_path` | string | Relative path to the documentation root, usually `docs` |
| `navigation` | list of strings | Ordered section names used when building navigation |

## Optional fields supported by the current portal scripts

| Field | Type | Purpose |
| --- | --- | --- |
| `tags` | list of strings | Search and discovery labels; omitted `tags` behave the same as an empty list |

## Conventions

- Keep `id` short, lowercase, and stable once the source is published.
- Use a human-readable `name`; it does not need to match the repository name exactly.
- Keep `description` concise and factual.
- Point `docs_path` at the directory the portal should sync.
- Add short tags when they improve discovery without becoming a keyword dump.
- If you omit `tags`, MSP Portal treats them as an empty list.
- List only real sections in `navigation`, in the order readers should see them.

## Example

```yml
id: msp-template
name: MSP Template
category: Shared Services
description: Starter structure for documentation repositories that publish through MSP Portal.
docs_path: docs
tags: [documentation, template, portal]
navigation:
  - concepts
  - guides
  - reference
```

## Notes on compatibility

The current MSP validation and sync scripts read these fields directly. Keep the top-level field names stable, and prefer adding comments over inventing alternative keys unless the portal schema is updated first.
