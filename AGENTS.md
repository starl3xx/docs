# filter.fun documentation — agent rules

These rules apply to every page in this repo. The Mintlify-flavor guidance
below is also valid; filter.fun rules take precedence on conflict.

## Source of truth

- **Spec:** `/Users/jakebouma/Documents/Claude/Projects/filter.fun/filter_fun_comprehensive_spec.md`
  is the design source of truth. If a docs claim contradicts the spec, the
  spec wins — fix the docs to match.
- **Roadmap:** `/Users/jakebouma/Documents/Claude/Projects/filter.fun/ROADMAP.md`
  determines tense. Shipped epics → present tense. Pending → "coming soon"
  or omit. Never describe pending behavior as if it ships today.
- **Brand kit:** `/Users/jakebouma/Documents/Claude/Projects/filter.fun/filter.fun-brand-kit/`
  is canonical. Colors come from `palette.json`; do not introduce non-brand
  colors in MDX styling.

## Canonical URLs

filter.fun runs three subdomains under one apex:

| Surface | Host | What lives here |
| --- | --- | --- |
| Web app | `https://filter.fun` | Arena gameplay (the dApp). Not a marketing landing. |
| Docs | `https://docs.filter.fun` | This site. Marketing/explainer + reference. |
| Indexer API | `https://api.filter.fun` | `/season`, `/tokens`, `/events`, `/profile/:address`. |

Rules:

- **Never link to `filterfun.mintlify.app` or `*.up.railway.app` in published docs.** Those are deployment-internal and rotate. Use the canonical hosts above.
- **Internal cross-links use site-relative paths** (`/how-it-works/the-filter`), not absolute URLs to `docs.filter.fun`. Absolute `https://docs.filter.fun` URLs only appear inside `<Visibility for="agents">` blocks where they're being **declared** as canonical-URL facts for AI clients to consume — never as cross-links.
- **MCP server URL is `https://docs.filter.fun/mcp`** — that's what the contextual toolbar's `add-mcp` option installs.
- **filter.fun root resolves to the web app**, not a marketing landing. Marketing/explainer content lives here on docs.

## The mark

The mark is **▼** (U+25BC, BLACK DOWN-POINTING TRIANGLE), **not** 🔻 (the
emoji). The geometric glyph carries the brand pink→red gradient on visual
surfaces. The emoji is acceptable only as casual shorthand in chat / social
copy where SVG can't render — never on a docs page.

## Locked tagline + canonical pitch

Locked tagline form:

> *"Get filtered or get funded ▼"*

Use this exact phrasing as the primary tagline.

The canonical elevator pitch — use **verbatim**, do not paraphrase:

> "One of the problems with most token launchpads is that the vast
> majority of tokens launched die or never take off at all. With
> filter.fun, that's a feature, not a bug. We've solved launchpads."

Acceptable short forms: *"We've solved launchpads."* / *"Death is the engine."*

## Dual-audience pages

Every page that has structured facts (cadence hours, percentages, contract
addresses, status booleans) must use the dual-audience pattern:

- `<Visibility for="humans">` — friendly explainer, prose, diagrams.
- `<Visibility for="agents">` — structured facts, tables, JSON-friendly
  shapes. Agents reading the docs (Claude / ChatGPT / MCP clients) get the
  same numbers without having to parse marketing copy.

## Banned phrasings (spec §32.3)

Never say:

- "guaranteed returns"
- "safe" or "risk-free"
- "passive income"
- heavy casino language
- heavy technical jargon

The system is speculative, competitive, partially zero-sum, and risky. Say
that plainly. The risk page is a feature, not a footnote.

## Voice (spec §32.2)

Sharp, competitive, clear, slightly ruthless. Not scammy. Not overhyped.
Transparent about risk. Active voice and second person ("you").

---

# Mintlify project conventions

## About this project

- This is a documentation site built on [Mintlify](https://mintlify.com)
- Pages are MDX files with YAML frontmatter
- Configuration lives in `docs.json`
- Run `mint dev` to preview locally
- Run `mint broken-links` to check links

## Style

- Sentence case for headings
- Bold for UI elements: Click **Settings**
- Code formatting for file names, commands, paths, code references
- Markdown links between pages use absolute paths (`/how-it-works/the-filter`),
  not relative

## Components in use

`<Visibility>`, `<Prompt>`, `<CardGroup>`, `<Card>`, `<Steps>`, `<Step>`,
`<Frame>`, `<Note>`, `<Warning>`. Brand colors come from `docs.json`
theme — don't hardcode hex values in page-level styles.
