# Patina community pattern packs

Small, reviewed pattern packs for Patina's prompt-based writing workflow.
They add editing guidance; they do not establish authorship or bypass detectors.

The first pack is `en-corporate-bizspeak`: two bounded substitutions for corporate
phrasing, with exclusions and meaning-preserving examples.

Requires Patina CLI 8.2.0 or newer, below 9.0.0:

```sh
patina pattern install en-corporate-bizspeak
patina pattern list
patina pattern remove en-corporate-bizspeak
```

The CLI resolves this repository's main branch to an immutable commit before
downloading `packs/<name>/pack.yaml` and its Markdown files. Installations are
unsigned. Review the source before installing; there are no install scripts,
executable hooks, registry service or provider credentials in this repository.

To contribute, add `packs/<language>-<name>/pack.yaml` using `pack.schema.json`.
Use filenames starting with `<language>-community-`. Every pattern needs a fire
condition, exclusions, a semantic preservation note, and before/after examples.
Do not invent facts, remove warranted uncertainty, or change numbers or causation.
Record the author and redistribution license in the manifest. New packs and
changes receive independent review before merging into main.

The main Patina repository documents the CLI contract in `docs/PATTERNS.md` and
tests installation, offline listing/removal, loader integration and unsafe files.
Pack source is MIT licensed unless its manifest explicitly states otherwise.
