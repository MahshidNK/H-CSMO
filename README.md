# H-CSMO 2026 LaTeX manuscript package

This directory contains the revised English manuscript, all figures and source result tables used by the paper, the BibTeX database, Elsevier `elsarticle.cls`, a compiled PDF, and a quality audit.

## Main files

- `main.tex` - manuscript entry point
- `references.bib` - bibliography
- `sections/` - section source files
- `figures/main/` - figures used in the main Results section
- `figures/appendix/` - supplementary/appendix figures
- `tables/` - CSV result tables used to verify reported values
- `HCSMO_Manuscript_2026_Submission.pdf` - compiled manuscript
- `HIGHLIGHTS.txt` - Elsevier-style highlights
- `MANUSCRIPT_AUDIT.md` - reproducibility and writing audit

## Compile

A standard Elsevier LaTeX workflow is sufficient:

```bash
pdflatex main.tex
bibtex main
pdflatex main.tex
pdflatex main.tex
```

The local validation environment used `bibtex8` because the container's `bibtex` executable is not available. The generated `main.bbl` is included for convenience.

## Scientific scope

The paper reports the frozen H-CSMO implementation used by the final benchmark. Representative and SLA-constrained tracks remain separate, scheduler-controllable and gross accounting are not conflated, adapted comparator implementations are labeled explicitly, and optimizer search seeds are not treated as independent workload replications.
