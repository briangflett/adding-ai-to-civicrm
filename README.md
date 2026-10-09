# Adding AI to CiviCRM

A community discussion draft on adding AI capabilities to CiviCRM, building on what WordPress
and Drupal have learned. Published as a website with [MkDocs](https://www.mkdocs.org/) and
[Material for MkDocs](https://squidfunk.github.io/mkdocs-material/), the same toolchain as
docs.civicrm.org, so the pages can move into a docs.civicrm.org book later with little change.

- Pages live in `docs/`, one Markdown file per page; navigation is in `mkdocs.yml`.
- Diagrams are [Mermaid](https://mermaid.js.org/) blocks; `click` lines make boxes into links.
- Comments use [giscus](https://giscus.app) (GitHub Discussions), configured in
  `overrides/partials/comments.html`. Nothing renders until the repo and category IDs are set.

## Preview locally

```bash
python3 -m venv .venv && .venv/bin/pip install "mkdocs<2" "mkdocs-material<10"
.venv/bin/mkdocs build --strict && python3 -m http.server -d site 8766
```

## Publishing (one-time set-up)

1. Create the public GitHub repository and push `main`.
2. Settings → Pages → Source: **GitHub Actions** (the `publish` workflow builds and deploys on every push).
3. Settings → General → Features: enable **Discussions**, create a category named **Comments** (type: Announcement, so only giscus creates threads).
4. Install the [giscus app](https://github.com/apps/giscus) on the repository, then copy the repo and category IDs from giscus.app into `overrides/partials/comments.html`.

## Licence

Text is licensed [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/).
