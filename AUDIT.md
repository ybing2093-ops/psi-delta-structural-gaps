# ψ–Δ Structural Audit — Executive Summary (AUDIT.md)

This repository records a **package-relative** framework for diagnosing **structural gaps** in cross-scale modeling.
It treats “continuity / smooth matching” as a **statement with conditions**, not a default license.

---

## 1) Minimal declaration: the package V

All claims in this framework are relative to a declared package

\[
V := (\Phi_I,\ \Phi_G,\ D,\ U,\ \Omega_{\mathrm{reach}},\ \varepsilon,\ \text{comparability/transport})
\]

- \(\Phi_I, \Phi_G\): micro/macro interfaces (what objects are compared)
- \(D\): discrepancy rule (metric/divergence) **locked** under \(V\)
- \(U\): admissible lifting / reconstruction family
- \(\Omega_{\mathrm{reach}}\): reachability / task domain
- \(\varepsilon\): resolution threshold for reporting equivalence
- comparability/transport: explicit terms that make cross-object comparisons meaningful

**Resolution semantics:** cross-level “=” is read as \(\approx_\varepsilon\) (reportable equivalence under \(V\)),
not as ontic identity.

---

## 2) Core quantities: Ψ and Δ

- **\(\Psi\)** (intra-level tension): a level-internal witness of whether closure/consistency can be pushed below the
  declared resolution within the declared operations.

- **\(\Delta_{I\to G}\)** (cross-level gap): the **irreducible residual** between micro and macro interfaces after
  optimizing over admissible reconstructions \(U\), evaluated under the locked rule \(D\) and domain \(\Omega_{\mathrm{reach}}\).

Informal reading: \(\Psi\) is “how small the level can make its internal conflicts”; \(\Delta\) is “what cannot be
eliminated across levels once \(V\) is fixed”.

---

## 3) “Not reportable” (Undefined) triggers

The correct output is **Not reportable / Undefined** when any of the following is missing or unstable:

- comparability/transport terms are not declared (no implicit transport)
- \(D\) and/or \(\varepsilon\) are not locked (prevents moving-goalpost reporting)
- interfaces \(\Phi_I,\Phi_G\) do not support a well-defined comparison under \(V\)
- the admissible reconstruction family \(U\) is unspecified

This is a reporting discipline: it blocks convenient numbers when the comparison itself is not well-defined.

---

## 4) Companion work (separate repository): endpoint ≠ path

A companion repository derives a **relative-entropy endpoint–path decomposition identity** (via chain decomposition)
and provides a QED-grade verification path for finite-window RG / coarse-graining endpoint matching.

\[
\Delta_{\mathrm{path}}=\Delta_{\mathrm{pair}}+\Gamma_{\mathrm{path}},\qquad \Gamma_{\mathrm{path}}\ge 0
\]

Interpretation: endpoint agreement can coexist with non-negligible irrecoverable path loss \(\Gamma_{\mathrm{path}}\).
This is a concrete worked case consistent with the ψ–Δ reporting discipline.

Repo: https://github.com/ybing2093-ops/endpoint-path-gaps-qed  
DOI:  https://doi.org/10.5281/zenodo.18414030

---

## 5) Falsification entry points (technical)

1) **Semantics:** show \(\Psi\) or \(\Delta\) is ill-defined / circular on its declared domain.  
2) **Counterexample:** under a fixed \(V\) and \(\varepsilon\), construct a reproducible system where the framework’s
   “reportable / not reportable” conclusion contradicts checkable facts.  
3) **Derivation:** identify a concrete break in the companion identity’s chain decomposition or its verification path.

---
