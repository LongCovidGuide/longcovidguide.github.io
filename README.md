# Long COVID Guide

A bilingual (Chinese/English) resource for people living with Long COVID, their caregivers, and anyone who wants to learn more about the condition.

Live site: [longcovidguide.github.io](https://longcovidguide.github.io)

## How to Contribute

### Prerequisites

- [mdBook](https://rust-lang.github.io/mdBook/guide/installation.html) for local preview (optional but recommended)
  ```
  brew install mdbook   # macOS
  ```

### Editing Content

All content lives in the `src/` directory as Markdown files:

```
src/
├── SUMMARY.md                  # Table of contents — edit this to add/reorder pages
├── introduction.md
├── understanding/
│   ├── what-is-long-covid.md
│   ├── symptoms.md
│   └── who-is-affected.md
├── management/
│   ├── pacing.md
│   ├── treatments.md
│   └── mental-health.md
└── resources/
    ├── research.md
    ├── support.md
    └── links.md
```

Just edit the `.md` files directly. Each page is standard Markdown.

### Adding a New Page

1. Create a new `.md` file in the appropriate folder under `src/`
2. Add an entry for it in `src/SUMMARY.md`, e.g.:
   ```markdown
   - [My New Page](./understanding/my-new-page.md)
   ```

### Preview Locally

```bash
mdbook serve --open
```

This starts a local server at `http://localhost:3000` with live reload.

### Publishing Changes

Once you're happy with your changes, commit and push to `main`:

```bash
git add .
git commit -m "describe your changes"
git push
```

GitHub Actions will automatically build and deploy the site. Changes are usually live within 1–2 minutes.

### Book Configuration

`book.toml` contains the book settings (title, authors, site URL). You generally won't need to edit this.
