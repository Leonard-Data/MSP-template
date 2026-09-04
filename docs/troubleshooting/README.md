# Template and portal integration troubleshooting

## `.docs-source.yml` exists but the portal cannot use it

Check that the file is valid YAML, that required top-level fields are present, and that `docs_path` points to a real directory.

## The source syncs, but pages are missing

Confirm that the pages live under the directory named by `docs_path` and that the files were committed to the repository.

## Navigation looks incomplete or out of order

Review the `navigation` list in `.docs-source.yml`. It should include only real section folders and should match the order you want the portal to present.

## Images or diagrams do not render after sync

Keep assets inside the repository, usually under `docs/assets/`, and link to them with relative paths from the page that references them.

## Links work on GitHub but break in the portal

Prefer repository-relative Markdown links to other pages and assets. Avoid absolute local paths and links that depend on one specific deployment base URL.

## A new source collides with an existing one

`id` must be unique across connected repositories. If the portal reports a duplicate source, choose a stable identifier that matches the section rather than a generic label such as `docs` or `template`.
