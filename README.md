# Stationary Strings Theorem VIII — Publication Package

> **Türkçe:** [README_TR.md](./README_TR.md)

**Stationary Strings Theorem VIII: Falsifiable Predictions, 511 keV Spectral Band, and Uncertainty Quantification**

Author: Fahri Meral · Date: October 17, 2026 · Version: v1 (Paper VIII)

> **Status:** Unpublished preprint (v1). Not peer-reviewed.

## Contents

| File | Description |
|---|---|
| `paper/duran_sicimler_teoremi_VIII.tex` | Main paper, Turkish (Tables 1–4, Figure 1 2×2) |
| `paper/duran_sicimler_teoremi_VIII_EN.tex` | English version |
| `figs/fig10_falsifiable_predictions_UQ.pdf` | Tests T20–T22 + UQ figure (TR, 2×2) |
| `figs/fig10_falsifiable_predictions_UQ.png` | Tests T20–T22 + UQ figure preview (TR) |
| `figs/fig10_falsifiable_predictions_UQ_en.pdf` | Tests T20–T22 + UQ figure (EN, 2×2) |
| `figs/fig10_falsifiable_predictions_UQ_en.png` | Tests T20–T22 + UQ figure preview (EN) |
| `CITATION.cff` | Citation record |
| `LICENSE` | CC BY 4.0 |

## Numerical reproduction

Tests T20–T22 (+ UQ) are produced with the solver in the **Paper V repository**
([`stationary-strings-v`](https://github.com/fahrim/stationary-strings-v)):

```bash
git clone https://github.com/fahrim/stationary-strings-v
pip install numpy scipy matplotlib
python duran_sicimler_sim/solver_engine.py   # T1–T22 (22/22 PASS)
python duran_sicimler_sim/mini_check_viii.py  # independent cross-check (7/7 PASS)
python duran_sicimler_sim/generate_figures.py  # Figure 1 (+_en)
```

The independent cross-check never imports the solver.

## Key findings

- T20: BASE-STEP 136 mT weak-field falsification pair (`r* = 1.1167668231 µm`,
  offsets `1–4 mm` recaptured, unprotected arm lost).
- T21: ALPHA third-field prediction (`ḟ(1.05 T) = −74.2301213010 ± 0.0055473080 kHz/h`,
  `R(1.05/1.03) = 1.0194406565`, `R(1.07/1.05) = 1.0190695066`).
- T22: 511 keV photon-budget prediction band (`R = 3.3387096774` at `f_Ps = 0.92`,
  band `[3.115, 3.585]`, `P_s = 1` budget `2.6900000000`).
- UQ: lock-output sensitivities + self-audit note (solver proton constant caught
  and corrected by the independent chain; slopes changed only 0.04%).

## License

CC BY 4.0 — see `LICENSE`. Content is not peer-reviewed.
