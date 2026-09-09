# Fisher approach to Ca II H&K chromospheric activity indicators

**Ferreira, R.R. & Borin, A.M.S.**  
Federal Institute of Triângulo Mineiro (IFTM), Uberaba-MG, Brazil

---

## Overview

This repository contains the analysis code and manuscript source for the paper:

> *Parametric precision limits for Ca II H&K chromospheric activity indicators: a Fisher-information approach*  
> Submitted to Research in Astronomy and Astrophysics (RAA)

The paper derives Cramér-Rao bounds on the measurement precision of the chromospheric S-index S_HK and the normalized excess R'_HK using the Fisher information framework applied to a parametric spectral model for the Ca II H&K doublet.

---


## Reproducing the results

### Requirements

Python 3.10+ with the packages listed in `requirements.txt`:

```bash
pip install -r requirements.txt
```

### Running the notebook

```bash
jupyter notebook fisher_caII_analysis.ipynb
```

Execute all cells sequentially (cells 1–45). The notebook produces all six manuscript figures and verifies the key numerical results:

- σ_CRB(S_HK)|4×4 = 0.1800 × (100/SNR) × √(50 000/R)
- ρ(A_C, σ_C) = +1/√3 (universal, parameter-independent)
- p_{σ_C} = 3/2 (exact marginalisation penalty)
- N_min = 29 (ESPRESSO deep) to >2×10⁵ (LAMOST LRS)

---

## Key results

The parametric Cramér-Rao bound on S_HK scales as SNR⁻¹ R⁻¹/², with a passband dilution prefactor ΔW_RV/I_WG ≈ 42.19. A universal Fisher correlation ρ(A_C, σ_C) = +1/√3, independent of all stellar and instrumental parameters, implies an exact marginalisation penalty of 3/2 in variance when the chromospheric line width is treated as a nuisance parameter.

---

## License

Code: MIT License. Manuscript text: © the authors.

---

## Contact

R.R. Ferreira — rafaelferreira@iftm.edu.br
