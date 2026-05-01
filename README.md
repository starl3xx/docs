# filter.fun docs

Documentation site for [filter.fun](https://filter.fun) — a weekly
token-launch tournament on Base. *Get filtered or get funded ▼*

The product spec, contracts, indexer, and web app live in the main
monorepo at [github.com/starl3xx/filter-fun](https://github.com/starl3xx/filter-fun).

## Local preview

Install the [Mintlify CLI](https://www.npmjs.com/package/mint):

```sh
npm i -g mint
```

From the repo root (where `docs.json` lives):

```sh
mint dev
```

Preview at `http://localhost:3000`.

## Check links

```sh
mint broken-links
```

## Publishing

Mintlify's GitHub app deploys to production automatically on every push
to `main`.

## Contributing

See [`CONTRIBUTING.md`](./CONTRIBUTING.md) for the workflow and writing
guidelines, and [`AGENTS.md`](./AGENTS.md) for the brand + voice rules
(locked tagline, the ▼ glyph, banned phrasings, dual-audience pages).

## Source of truth

- **Spec:** the [comprehensive spec](https://github.com/starl3xx/filter-fun/blob/main/filter_fun_comprehensive_spec.md)
  in the main repo. If a docs claim contradicts the spec, the spec wins.
- **Roadmap:** the [roadmap](https://github.com/starl3xx/filter-fun/blob/main/ROADMAP.md)
  determines tense — shipped epics use present tense, pending epics
  use "coming soon" or are omitted.
