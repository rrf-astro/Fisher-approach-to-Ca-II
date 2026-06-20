# Fundamental precision limits for chromospheric activity indicators: a Fisher information approach to Ca II H&K spectroscopy

**Ferreira et al. 2026** — *Research in Astronomy and Astrophysics* (submitted)

---

## Overview

This repository contains the manuscript, analysis notebook, and figures for a
theoretical study of the fundamental measurement precision limits for chromospheric
activity indicators derived from the Ca II H&K doublet (S-index S_HK and
log R'_HK).

A parametric spectral model for the Ca II H&K region is developed, treating the
observed flux as a superposition of a broad photospheric trough and a narrow
chromospheric emission core. The Fisher information framework is applied to derive
closed-form Cramér–Rao lower bounds (CRB) on the precision of S_HK and R'_HK as
functions of signal-to-noise ratio (SNR), spectral resolution (R), and stellar type.
Key results include the CRB scaling σ_CRB(S_HK) ∝ SNR⁻¹ R⁻¹/², a universal
Fisher correlation ρ(A_C, σ_C) = +1/√3 independent of stellar parameters, an exact
marginalisation penalty of 3/2 in variance when chromospheric line width is a
nuisance parameter, and minimum observation counts N_min = 29 (ESPRESSO deep) vs.
~225,000 (LAMOST LRS) to reach a 1% precision target.

---

## Repository structure

```
Fisher-aproach-to-Ca-II/
├── manuscript/
│   ├── manuscript_v1_5.tex       # Main LaTeX source (RAA format)
│   └── reference.bib             # BibTeX bibliography (39 entries)
├── notebooks/
│   └── fisher_caII_analysis.ipynb  # Analysis notebook v2.0 (45 cells)
├── figs/
│   ├── fig01_spectral_model.eps
│   ├── fig02_crb_sindex_map.eps
│   ├── fig03_fisher_offdiag.eps
│   ├── fig04_crb_rhk_degrad.eps
│   ├── fig05_survey_efficiency.eps
│   └── fig06_lamost_likelihood.eps
├── state/
│   ├── PAPER_STATE_v15.md
│   ├── REVISION_LOG_v15.md
│   ├── EQUATIONS_LOG.md
│   ├── FIGURE_LOG_v4.md
│   ├── CODE_LOG_v8.md
│   └── DATA_LOG.md
├── .gitignore
└── README.md
```

---

## Reproducing the results

All numerical results and figures are generated exclusively through the Jupyter
notebook. Execute cells sequentially from top to bottom (do not skip cells).

**Requirements:** Python 3.x, numpy, scipy, matplotlib, sympy

```bash
cd notebooks/
jupyter notebook fisher_caII_analysis.ipynb
# Kernel → Restart & Run All
```

All six figures are written to `figs/` as both `.png` (preview) and `.eps`
(publication quality). Do not run figures from any external script — the notebook
is the single source of truth for all numerical output.

---

## Key results

| Result | Value |
|---|---|
| σ_CRB(S_HK) \| 4×4 Fisher | 0.1800 × (100/SNR) × √(50k/R) |
| Fisher correlation ρ(A_C, σ_C) | +1/√3 ≈ 0.5774 (universal) |
| Marginalisation penalty p_{σ_C} | 3/2 (exact) |
| Passband dilution ΔW_RV / I_WG | 42.19 (solar) |
| N_min — ESPRESSO deep | 29 |
| N_min — LAMOST LRS | ~225,000 |
| F_core (solar) | 0.08 |

---

## How to cite

If you use this work, please cite:

```
Ferreira et al. 2026, Research in Astronomy and Astrophysics, [vol], [page]
DOI: [to be assigned upon publication]
```

BibTeX entry (placeholder — update after publication):

```bibtex
@ARTICLE{Ferreira2026,
   author  = {Ferreira, [First name] and [co-authors]},
   title   = {Fundamental precision limits for chromospheric activity indicators:
              a Fisher information approach to {Ca\,{\sc ii}} H\&K spectroscopy},
   journal = {Research in Astronomy and Astrophysics},
   year    = {2026},
   volume  = {},
   pages   = {},
   doi     = {}
}
```

---

## License

To be confirmed by the authors prior to publication.
