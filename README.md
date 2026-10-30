# LLM agent groups and cheap talk: paper source

LaTeX source for the ACL 2027 submission (ARR deadline 2027-01-04 AoE). Companion code, raw runs and
analyses are in the `llmrc` repository.

## Status

`main.tex` is the 29 October 2026 working draft (framing: the role-division routine). The framing is being
revised around agreement in LLM monocultures and the GPT-6 Luna replication (see `llmrc/docs/62`, `64`, `65`).
Blue `[...]` text marks pending experiments.

## Build

```bash
tectonic main.tex
```

Or `pdflatex main && bibtex main && pdflatex main && pdflatex main`. The ACL style files (`acl.sty`,
`acl_natbib.bst`) are vendored so Overleaf compiles without extra setup.

## Numbers and tables

Every data-derived number is a macro in `generated/numbers.tex`; tables are `generated/tab_*.tex`. They are
written by `llmrc/paper_acl_role_sharing/build_tables.py` from audited result files, and
`generated/provenance.json` records the input and output hashes. Do not edit `generated/` by hand. To refresh:

```bash
cd ../llmrc && python3 paper_acl_role_sharing/build_tables.py   # writes ../llmrc-paper/generated
```
