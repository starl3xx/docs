# Contributing to the filter.fun docs

Thanks for the help. Read [`AGENTS.md`](./AGENTS.md) before writing —
it has the locked tagline, the ▼ glyph rule, banned phrasings (no
"safe", "risk-free", "guaranteed returns", "passive income"), and the
dual-audience `<Visibility>` pattern.

## How to contribute

### Edit on GitHub

1. Navigate to the page you want to edit.
2. Click the "Edit this file" pencil.
3. Make your changes and open a pull request against `main`.

### Local development

```sh
git clone https://github.com/starl3xx/docs.git filter-fun-docs
cd filter-fun-docs
npm i -g mint
mint dev          # preview at http://localhost:3000
mint broken-links # validate internal links
```

## Writing guidelines

- **Active voice, second person.** "Run the command" not "the command
  should be run." "You" not "the user."
- **One idea per sentence.** Keep them tight.
- **Sentence case for headings.**
- **Bold for UI elements**: Click **Settings**.
- **Code formatting** for file names, commands, paths, code references.
- **Absolute internal links** (`/how-it-works/the-filter`), not
  relative.
- **▼ not 🔻** in any docs surface. The geometric glyph (U+25BC) carries
  the brand gradient; the emoji is only for casual chat where SVG can't
  render.

## Source of truth

If a docs claim contradicts the [comprehensive spec](https://github.com/starl3xx/filter-fun/blob/main/filter_fun_comprehensive_spec.md),
the spec wins — fix the docs to match. If a feature isn't shipped per
the [roadmap](https://github.com/starl3xx/filter-fun/blob/main/ROADMAP.md),
either say "coming soon" or omit it. Never describe pending behavior as
if it ships today.
