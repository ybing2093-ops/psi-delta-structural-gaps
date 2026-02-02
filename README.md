# The ψ–Δ Framework (Package-Locked Cross-Level Diagnostics)

> Public record • reviewable • falsifiable (by counterexample or proof)

## What this repository is
This repository publishes a technical longform paper. 
It does one thing: it places a reviewable, falsifiable framework into the public record, so anyone can
test it with counterexamples or proofs.

**Scope note.** This repository contains **only the ψ–Δ framework paper**.
A companion repository hosts the **relative-entropy endpoint–path gap diagnostic** (see below).

---

## Core claim (minimal)
When a system is described across genuinely different levels (micro ↔ macro; fine ↔ coarse; process ↔ endpoint),
there can exist a **structural gap** that is not removable by “more compute” or “better fitting” alone.
A central source of error is often **structural**: attempting to glue cross-level objects using continuous reasoning
without licensed information recovery.

The framework formalizes this as **package-locked diagnostics**:
- `Ψ(L, A; V)` — an intra-level structural parameter (tension/residual conflict under a declared perspective).
- `Δ_{I→G}(L; V)` — an inter-level structural gap (compression → admissible reconstruction residual).

All reported quantities are **package-relative**: they are well-posed only after a declaration package `V`
locks the boundary, reachable domain, interfaces, discrepancy rule, admissible reconstructions, and the reporting
threshold.

---

## Repository contents
- `papers/The_Psi_Delta_Framework.pdf` — the main paper.

(Optional folders you may add later: `examples/`, `notebooks/`, `src/`.)

---

## Reading map (shortest path)
1. **Package-locked reporting**: what a declaration package `V` is, and what “well-posed” means.
2. **Resolution-aware reporting**: the meaning of `≈_ε` (“indistinguishable at threshold ε”).
3. **Core quantities**: definitions of `Ψ(L, A; V)` and `Δ_{I→G}(L; V)`.
4. **Witnesses / certificates**: how a report can be audited (e.g., fiber witnesses for non-negligible gaps).
5. (Optional) **Dynamics interface**: accumulated gap `Δ_acc(γ)` driven by a running readout `Ψ_run(γ)`—invoked only
   with explicit transport/comparability clauses.

---

## Minimal semantics (no hidden moves)

### 1) Resolution-aware equality is a reporting convention
The symbol `≈_ε` is **not ontological equality**. It is a resolution/threshold convention:
- a report `x ≈_ε 0` is licensed only under the declared threshold rule used by the package.

### 2) “Ontology” is guarded by a meta-gap axiom (not a numerical diagnostic)
The paper also uses `Δ*_R > 0` as a **semantic guardrail**: across a genuine cross-level relation `R`,
cross-level “=” is not to be read as an ontological identity.
This axiom is **not** an inf–sup diagnostic and is **never** used as a numerical threshold criterion.

---

## How to use the framework (conceptually)
You do not “apply ψ–Δ” by importing a library. You apply it by **declaring a package** and producing **auditable reports**.

### Package Card (template)
Create a package card `V` that locks the objects needed for `Ψ` and `Δ_{I→G}`:

- ID / scope
- Target system `L` and boundary (what counts as inside vs environment)
- Reachability / audited domain `Ω_reach`
- Level specifications and perspectives:
  - perspective for `Ψ` (representation map `Φ_A`)
  - interfaces for `Δ_{I→G}` (pair `Φ_I`, `Φ_G`)
- Conflict functional for `Ψ`: `E_A`
- Discrepancy rule for `Δ_{I→G}`: `D`
- Admissible liftings / reconstructions: `U`
- Reporting threshold `ε` and the meaning of `≈_ε`
- (Optional) audit clause, transport/comparability law, invoked optional modules

**Protocol rule:** If required clauses are missing (or cross-package comparisons are attempted without an explicit
transport/comparability law), the correct output is **undefined**, with an explicit diagnosis of what is missing.

---

## Companion work: relative-entropy endpoint–path gap diagnostic (separate repository)

A companion repository derives a **relative-entropy endpoint–path identity** (via chain decomposition) and provides a **QED-grade verification path** for finite-window RG / coarse-graining endpoint matching problems.

**Relationship to ψ–Δ (conceptual):**

* The diagnostic paper is a worked case study of the general theme: **endpoint agreement does not necessarily certify path/process agreement**.
* It supplies a concrete “certificate-style” way to expose non-negligible gaps that are consistent with the ψ–Δ reporting discipline (package-locked objects; auditable witnesses).

**Companion repository:** `https://github.com/ybing2093-ops/endpoint-path-gaps-qed`
**DOI (Zenodo):** `https://doi.org/10.5281/zenodo.18414030`

