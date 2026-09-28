# AGENTS.md

## Standard

This book follows the [QuadriviumPress MyST baseline](https://github.com/QuadriviumPress/bindery/blob/main/doc/myst-baseline.md) and the [presentation skill](https://github.com/QuadriviumPress/bindery/blob/main/skills/quadrivium-myst-presentation/SKILL.md).

## Commands

```bash
npm run start
npm run build
npm run verify
npm run check
npm run build:exports
npm run build:pdf
npm run build:docx
```

`npm run check` is the production-equivalent verification and HTML build.

## Intentional differences

- `build` and `check` pass `--execute --strict` so Jupyter content runs during the build, and both finish with `node scripts/setup-pwa.mjs`.
- Print exports: `build:exports`, `build:pdf`, `build:docx`.
- Source lives under `content/`, not `chapters/`.
- `scripts/setup-pwa.mjs` looks for a logo in `content/images/` before `images/`, because this book's logo is not the template SVG.

## Presentation gap

Homework is written as notebook sections titled Exercise N, including paper-and-pencil and Jupyter submissions. It does not use `{exercise}` or `{solution}`. Aligning that computational pedagogy is deferred.
