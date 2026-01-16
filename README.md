# Reproducible code for:  
A structural coordination regime in delay-coupled information systems

This repository provides a fully reproducible implementation of the numerical methods used in the manuscript.

The code simulates a minimal delay-coupled dynamical system, computes information-theoretic coordination measures, and verifies the analytically predicted coordination optimum at a normalized delay ratio Δτ / T₀ ≈ 0.25.

---

## Contents

- `simulation.py`  
  Main script implementing all numerical analyses reported in the paper.

---

## Model overview

The model consists of two symmetrically coupled dynamical units receiving a common broadband input.  
Each unit is characterized by intrinsic dynamics, delayed bidirectional coupling, and stochastic noise.

Key control parameters:
- Delay asymmetry: Δτ = |τ₁ − τ₂|
- Functional heterogeneity: ΔF = |f₁ − f₂|

---

## Quantities computed

The code reproduces all quantities reported in the Methods and Results:

- Effective emergent timescale T₀ (estimated from output dynamics)
- Information integration (I_INT)
- Information differentiation (Q)
- Coordination index: C = I_INT × Q
- Fisher information (Gaussian approximation)

All quantities are computed from simulated time series after discarding transients.

---

## Running the code

```bash
python simulation.py

This will:

Simulate the system across a grid of (Δτ, ΔF)

Estimate T₀ from power spectral density

Compute C and Fisher information

Generate the coordination and sensitivity surfaces shown in Fig. 2

No external data are required.
