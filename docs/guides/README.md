# Add a documentation page

Use this guide when you want to add a new page without reshaping the whole repository.

## 1. Choose the folder

Start with the reader's question:

- "What is this?" -> `concepts/`
- "How do I do it?" -> `guides/`
- "What is the exact rule or field?" -> `reference/`
- "What broke and how do I fix it?" -> `troubleshooting/`

If none of those fit, use the nearest folder and add links to related pages.

## 2. Create the file

Choose a descriptive kebab-case filename, for example:

```text
/docs/guides/add-a-documentation-page.md
```

Start with one `#` heading, then add the smallest set of sections needed to help the reader finish the task.

## 3. Link it from a nearby landing page

Add or update a short list in the folder's `README.md` or in `docs/README.md` so readers can discover the new page by browsing.

## 4. Add assets only when needed

Place diagrams or screenshots in `docs/assets/` and reference them with relative paths, for example:

```md
![Portal sync flow](../assets/portal-sync-flow.svg)
```

## 5. Check metadata if the structure changed

If you added a brand-new section folder or removed one, review `.docs-source.yml` and keep `navigation` aligned with the folders readers should see in MSP Portal.

## 6. Review before opening a PR

- headings are clear
- links resolve
- asset paths render
- the page lives in the right folder
- `.docs-source.yml` still reflects the source
