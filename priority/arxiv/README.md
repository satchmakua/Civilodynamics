# arXiv submission package (Phase C)

Submission-ready files for the two founding papers (Document 8, Stage C0/C1).
Generated from the canonical Markdown via pandoc 3.10; PDFs rendered offline
(headless Chrome, native MathML — no LaTeX engine or network required).

| Paper | Source | PDF |
|-------|--------|-----|
| Foundational Charter (Doc 1) | `01_Foundational_Charter.tex` | `01_Foundational_Charter.pdf` (10 pp) |
| Flagship case study (Doc 5) | `05_US_2000-2024_Case_Study.tex` | `05_US_2000-2024_Case_Study.pdf` (11 pp) |

## How to submit

arXiv accepts **either** LaTeX source (preferred) **or** a PDF. Two paths:

- **Fast path — submit the PDF.** Upload the `.pdf` directly. It is complete and
  verified. Simplest; do this if you want the flag up now.
- **Preferred path — submit the source.** Upload the `.tex`. arXiv compiles it on
  its own TeX system, which gives the cleaner arXiv-native result. **Compile-test
  first** (e.g., paste into Overleaf): the `.tex` is pandoc-generated and has not
  been compiled locally (no LaTeX engine was available here), so a stray Unicode
  glyph could need a one-line fix before arXiv accepts it. The PDF is the verified
  fallback if the source needs work you don't want to do now.

**Metadata to paste** (categories + abstracts) is in [`../DEPOSIT.md`](../DEPOSIT.md)
§1 and §2b/§2c. Primary category `physics.soc-ph`; cross-list `q-bio.PE`. A first
submission to `physics.soc-ph` may require an endorsement.

## Regenerating
These are build artifacts. To rebuild after editing the source Markdown, re-run the
pandoc → MathML-HTML → headless-Chrome-print pipeline (Chrome `--headless=new
--no-pdf-header-footer --print-to-pdf`). No LaTeX install needed.
