# Paper 5 — Deriving the Universal QCD Entropy Constant from First Principles

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.16785245.svg)](https://doi.org/10.5281/zenodo.16785245)

**Short description.**  
This repository contains the LaTeX source and compiled PDF for Paper 5, which derives the QCD RG–entropy constant
\[
|\Delta S_{\rm RG}| \;=\; 2\pi\,[a_{\rm UV}-a_{\rm IR}]\,k_B
\]
from continuum field theory using the Casini–Huerta–Myers (CHM) map and the 4D A‑type trace anomaly. For QCD with \(SU(3)\), a gapped IR (\(a_{\rm IR}=0\)), and two effectively massless Dirac flavors at the UV end of the spherical trajectory (\(N_f^{\rm eff}=2\)), the free‑field anomaly gives \(a_{\rm UV}=281/180\) and therefore
\[
|\Delta S_{\rm RG}| \;=\; \frac{281\pi}{90}\,k_B \;=\; 9.809\,k_B \approx 9.81\,k_B.
\]
No lattice inputs are used; the value follows from anomaly coefficients and geometry (κ=2π). This matches the constant used in Papers 1–4.

---

## Repository structure
  ```
paper5-entropy-constant/
├── paper/
│ ├── main.tex
│ └── paper5_derivation.pdf
├── README.md
├── LICENSE
└── citation.cff
  ```

> If you are using Overleaf, keep `main.tex` and upload any figures there. If you build locally, see “Build” below.

---

## Key result (one line)

**Universal constant (QCD, \(N_c=3\), \(N_f^{\rm eff}=2\)):**  
\(|\Delta S_{\rm RG}| = 281\pi/90 \, k_B = 9.809\,k_B\) (CHM map + A‑anomaly, κ=2π).

**Assumptions:** gapped IR (\(a_{\rm IR}=0\)); \(u,d\) effectively massless on the spherical trajectory; renormalized \(\mathbb{H}^3\) volume set to 1.

---

## Build (local)

- TeX Live / MacTeX:
  ```bash
  cd paper
  pdflatex main
  bibtex main || true
  pdflatex main
  pdflatex main

Output: paper5_derivation.pdf (identical to the one committed here).

### Citation

If you use this work, please cite:

```bibtex
@article{tupay2025_qcd_entropy_constant,
  author = {Tupay, Johann Anton Michael},
  title  = {Deriving the Universal QCD Entropy Constant from First Principles},
  year   = {2025},
  doi    = {10.5281/zenodo.16785245},
  url    = {https://doi.org/10.5281/zenodo.16785245}
}
