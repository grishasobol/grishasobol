# Résumé

`eu/` is the master. The others are derived from it:

- **eu/** — full version, with photo (EU / Serbia market)
- **us/** — same as EU, **without the photo** (US / UK — photos can trigger bias filters)
- **ru/** — Russian translation, with photo

Photo source: `../photo.jpg` (single file, shared).

## Rebuild PDFs

Run from the repo root (needs `pandoc` + `typst`):

```sh
pandoc resume/eu/resume.md -o resume/eu/resume.pdf --pdf-engine=typst --resource-path=resume/eu
pandoc resume/us/resume.md -o resume/us/resume.pdf --pdf-engine=typst
pandoc resume/ru/resume.md -o resume/ru/resume.pdf --pdf-engine=typst --resource-path=resume/ru
```

When you change `eu/resume.md`, mirror the edit into `us/` (drop the photo line) and `ru/` (translate), then rebuild all three.
