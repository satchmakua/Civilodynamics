# Civilodynamics — Lexicon and Ontology

**Canonical Corpus, Document 7 of 8 · Version 0.1 · June 2026**
**Satchel Hamilton · Civilodynamics Initiative**

> **Status and role.** This is the discipline's controlled vocabulary: the authoritative reference for every coined term, every symbol, and the relationships among the core concepts. It consolidates terminology defined in full elsewhere and exists to prevent terminological and notational drift as the corpus grows and as collaborators join. **Where a term's full definition lives in another document, that document governs; this lexicon canonicalizes the short form and the notation.** Beyond a glossary, §3 specifies the *ontology* (how the objects relate as a type system) and §6 records *deprecated and corrected usage* so that prior errors do not reappear. In assembling the notation (§2), two latent symbol collisions in the reflexivity model were identified and are resolved here.

---

## 1. How to use this document

- For a **definition**, see the lexicon (§4), grouped by domain; each entry names the canonical document.
- For a **symbol**, see the notation table (§2).
- For **how concepts relate**, see the ontology (§3).
- For **terms or notations that have been retired or corrected**, see §6 — consult it before reusing any older phrasing.
- **Proposals for new terms or symbols** are made by amending this document, so that the vocabulary has a single source of truth.

---

## 2. Notation conventions

Canonical from Document 2; reproduced here as the authoritative reference.

| Symbol | Meaning | Notes |
|--------|---------|-------|
| $\mathbf{S}(t)$ | **Structural configuration vector** | Bold; the *slow* state, locating a society in the morphospace. Axes $E,C,I,X,T,K$. |
| $\mathbf{u}(t)$ | **Stress readout vector** | Bold; the *fast* state behind the CSI. Blocks $\sigma_{\bullet}$. |
| $\Omega$ | **Configuration space (morphospace)** | $\Omega \subseteq \mathbb{R}^n$, $n\approx 24$. |
| $n,\ p$ | Dimensions of $\mathbf{S}$ and $\mathbf{u}$ | $n\approx 24$ (configuration); $p\approx 14\text{–}18$ (stress). |
| $E,C,I,X,T,K$ | Configuration axes | Energy, Coordination, Information, eXtraction, Trust, ecology (K). |
| $\sigma_{\mathrm{econ}},\sigma_{\mathrm{elite}},\sigma_{\mathrm{leg}},\sigma_{\mathrm{coh}},\sigma_{\mathrm{epi}},\sigma_{\mathrm{dem}}$ | Stress blocks | Economic, elite, legitimacy, cohesion, epistemic, demographic. |
| $\Sigma$ | Covariance matrix | Subscript $\mathcal{B}$ for baseline covariance, $\Sigma_{\mathcal{B}}$. |
| $\boldsymbol{\mu}_{\mathcal{B}}$ | Baseline centroid | Mean of the stress vector over the baseline. |
| $d(\cdot,\cdot)$ | **Mahalanobis metric** | $\sqrt{(\cdot)^{\mathsf{T}}\Sigma^{-1}(\cdot)}$; a *flat* metric (see §6). |
| $\textit{CSI}_{\mathrm{lin}},\textit{CSI}_{\mathrm{nl}},\textit{CSI}_{\mathrm{M}}$ | The three CSI constructions | Linear, nonlinear, Mahalanobis. |
| $\Pi,\ B(\Pi),\ \partial B(\Pi)$ | Poliform, its basin, its boundary | A poliform *is* the attractor/basin. |
| $V(\mathbf{S},t)$ | Potential function | Minima are poliform attractors; $\hat V \approx -\log\hat\rho$. |
| $\hat\rho$ | Empirical density estimate | Kernel density over historical configurations. |
| $\mathbf{F}(\mathbf{S},t)$ | Deterministic vector field | $\mathbf{F}=-\nabla V + R$. |
| $R(\mathbf{S},t)$ | **Rotational (non-conservative) component** | Generates secular cycles. **See collision note below.** |
| $\boldsymbol{\eta}(t)$ | Shock term | Exogenous stochastic perturbation. |
| $\mathcal{B}$ | Baseline interval | Society-specific; explicitly defended, never universal. |
| $O(t)$ | Object layer (reflexivity) | Actual social dynamics. |
| $\mathcal{E}(t)$ | **Epistemic/belief layer (reflexivity)** | Beliefs about the dynamics. **Script-E; see collision note.** |
| $\Phi(O,\mathcal{E})$ | **Reflexivity coupling** | **Newly assigned symbol; see collision note.** |
| $c_{g,k}$ | Per-item, per-group correct-belief rate | FCR instrument; group $g$, item $k$. *(Doc 9 §2.)* |
| $\Delta_k$ | Cross-group gap on item $k$ | $\lvert c_{A,k}-c_{B,k}\rvert$; max pairwise for >2 groups. *(Doc 9 §2.)* |
| $\theta$ | Consensus threshold | Gap below which an item counts as agreed. *(Doc 9 §2, §8.)* |
| $\textit{FCR}_\theta,\ \textit{FCR}_c$ | The two FCR statistics | Consensus-share (threshold) and mean-gap (continuous); $\textit{FCR}_c$ primary. *(Doc 9 §2.)* |
| $\mathcal{A}\ (=\mathcal{K})$ | Anchor core | Fixed item set held constant for longitudinal comparability. *(Doc 9 §3.2.)* |
| $\textit{XP}$ | Expressive component | $\textit{FCR}_c^{a}-\textit{FCR}_c^{b}$; consensus recovered by accuracy incentives. *(Doc 9 §4.)* |
| $\textit{ACC}$ | Knowledge level | Mean cross-group correct rate; companion to FCR, never folded in. *(Doc 9 §5.2.)* |
| $(\cdot)^{b},\ (\cdot)^{a}$ | Response-arm superscripts | Belief (standard) arm; accuracy-incentivized arm. *(Doc 9 §4.)* |

> **Resolved symbol collisions (new in this document).** Two collisions in the reflexivity model of Document 2 §8.1 are resolved here, and Document 2 will be reconciled to match:
> 1. The reflexivity **coupling term** was written $R(O,\mathcal{E})$, but $R$ already denotes the **rotational component** of the dynamics ($\mathbf{F}=-\nabla V + R$). The coupling is reassigned the symbol **$\Phi$**; $R$ is reserved for the rotational component.
> 2. The reflexivity **epistemic layer** was written $E(t)$, but $E$ already denotes the **energy axis** of the configuration vector. The epistemic layer is reassigned the script symbol **$\mathcal{E}(t)$**; $E$ is reserved for energy.
> These join the earlier resolution of the $\mathbf{S}(t)$ overload (configuration $\mathbf{S}$ vs. stress $\mathbf{u}$) and the energy/economic and coordination/cohesion label collisions (Document 2 §1).

---

## 3. The ontology — how the concepts relate

The discipline's objects form a small type system. Stating it explicitly prevents category errors (e.g., treating an index as a state, or a cluster as an attractor).

**Spaces.** There is one fundamental space: the **configuration space** $\Omega$ (the morphospace), in which a society is a point.

**Points and vectors.** A society at time $t$ is the **structural configuration vector** $\mathbf{S}(t)\in\Omega$ (slow). Derived from it is the **stress readout** $\mathbf{u}(t)$ (fast), a projection capturing deviation from baseline: $\mathbf{u}=h(\mathbf{S},\dot{\mathbf{S}};\mathcal{B})$. These are the *only* two state objects; everything else is a region, a functional, a dynamical operator, or a diagnostic.

**Regions.** A **poliform** $\Pi$ is a *region* of $\Omega$ — specifically an attractor with a **basin** $B(\Pi)$ and a **boundary** $\partial B(\Pi)$. Poliforms are not vectors and not indices; they are subsets of the state space.

**Functionals (scalars derived from states).** The **CSI**, **ECI**, and **EOI** are scalar *functionals* — reductions of the state (or of sub-vectors of it), not states themselves. The CSI reduces $\mathbf{u}$; the ECI reads the information axis $I$ / block $\sigma_{\mathrm{epi}}$; the EOI is a component feeding $\sigma_{\mathrm{elite}}$.

**Dynamical operators.** The **vector field** $\mathbf{F}$ governs motion; it decomposes into the gradient of the **potential** $V$ (whose minima are poliforms) and the **rotational component** $R$ (secular cycles), plus the **shock** $\boldsymbol{\eta}$.

**Diagnostics.** **Distance-to-bifurcation** is the signature diagnostic — distance from $\mathbf{S}$ to the nearest $\partial B$ — with a geometric (Tier 1) and a dynamical (Tier 2) reading.

**Bridging relations.** The **bridging hypothesis (H0)** asserts that the CSI (a functional on the fast state) tracks distance-to-bifurcation (a diagnostic on the slow state) — the claim that the stress layer and the poliform layer are two views of one object.

A compact type summary:

```
Space:        Ω  (configuration space / morphospace)
States:       S(t) ∈ Ω   (slow, structural)   →   u(t)   (fast, stress; a projection of S)
Regions:      Π ⊂ Ω      (poliform = attractor) ; B(Π) basin ; ∂B(Π) boundary
Functionals:  CSI(u) , ECI(I) , EOI → σ_elite     (scalars derived from states)
Dynamics:     dS/dt = F + η ;  F = −∇V + R          (operators on Ω)
Diagnostic:   distance-to-bifurcation  (S → ∂B)     (Tier 1 geometric / Tier 2 dynamical)
Bridge:       H0:  CSI  ⇄  distance-to-bifurcation  (the load-bearing hypothesis)
```

---

## 4. The lexicon

Grouped by domain. Format: **term** — definition — *(symbol; units if any; canonical document)*.

### 4.1 State-space and configuration

- **Configuration space / morphospace** — the finite-dimensional space whose axes are the constraint stack; a society is a point in it. *( $\Omega$; Doc 2 §2, Doc 3.)*
- **Structural configuration vector** — the slow-moving state locating a society in $\Omega$ along six axes. *( $\mathbf{S}$; Doc 2 §1.)*
- **Constraint stack** — the six layers carving the morphospace: energy, coordination, information, extraction, trust, ecology. *( $E,C,I,X,T,K$; Doc 2 §2, Doc 3 §5, Doc 4 §7.)*
- **Forbidden region** — combinations of axis values no real society can occupy (functional/developmental constraints). *(Doc 2 §2.3.)*
- **Occupied region** — the small, sparse, clustered subset of $\Omega$ that real societies actually fill; its sparseness is the central empirical claim of poliform theory. *(Doc 2 §2.3, Doc 3 §3.)*

### 4.2 Poliforms

- **Poliform** — a recurrent stable configuration; formally, a basin of attraction in $\Omega$. *( $\Pi$; Doc 3, Doc 2 §3.)*
- **Basin of attraction** — the set of states evolving toward a given attractor absent shock. *( $B(\Pi)$; Doc 2 §3.)*
- **Basin boundary / separatrix** — the surface separating basins; often fractal. *( $\partial B(\Pi)$; Doc 2 §3.)*
- **Basin depth** — potential difference between the boundary and the attractor minimum; the formal measure of poliform stability. *( $D(\Pi)$; Doc 2 §3.2.)*
- **Basin volume** — the breadth of initial conditions converging to a poliform. *(Doc 2 §3.2.)*
- **Sub-poliform** — a poliform nested within another (e.g., a region within a nation-state); the formal nesting structure is an open problem. *(Doc 3 §7.)*
- **Poliform transition** — a society's movement from one basin to another; see transition types. *(Doc 3 §6, Doc 2 §6.3.)*

### 4.3 Stress and indices

- **Stress readout** — the fast-moving state behind the CSI; a baseline-deviation projection of $\mathbf{S}$. *( $\mathbf{u}$; Doc 2 §1.)*
- **Civilizational Stress Index (CSI)** — scalar functional measuring distance of $\mathbf{u}$ from the baseline regime; three constructions (linear, nonlinear, Mahalanobis). *( $\textit{CSI}$; Doc 2 §4, Doc 4 §4.)*
- **Per-dimension-normalized headline** — the recommended reported scalar ($\textit{CSI}_{\mathrm{M}}/\sqrt{p}$ or mean $z$), interpretable across differing $p$. *(Doc 2 §4.5.)*
- **Epistemic Coherence Index (ECI)** — composite measuring shared factual/information commons; the discipline's distinctive and least-mature measure. *(Doc 2 §5, Doc 4 §5.)*
  - **Media Overlap Score (MOS)** — $1-\mathrm{JSD}$ of two communities' source distributions. *(Doc 4 §5.1.)*
  - **Factual Consensus Rate (FCR)** — cross-group agreement on a verifiable battery; the share of items whose cross-group gap is below threshold ($\textit{FCR}_\theta$) and/or one minus the mean gap ($\textit{FCR}_c$, primary). *(Doc 4 §5.2; full instrument and pre-registration Doc 9.)*
    - **Anchor core / rotating pool** — the fixed item set held constant for longitudinal comparability vs. the per-wave refreshed set guarding against priming and coaching. *(Doc 9 §3.2.)*
    - **Directional balance** — the requirement that correct answers, as a set, favor no partition; the FCR's structural even-handedness safeguard. *(Doc 9 §3.3.)*
    - **Ground-truth adjudication** — the pre-registered sourcing hierarchy and multi-perspective panel that admit only settled, documentable items. *(Doc 9 §3.4.)*
    - **Incentivized-accuracy arm / expressive component ($\textit{XP}$)** — the accuracy-paid arm isolating believed from performed divergence, and the consensus it recovers. *(Doc 9 §4.)*
  - **Network Connectivity Index (NCI)** — share of cross-community ties in information networks. *(Doc 4 §5.3.)*
- **Elite Overproduction Index (EOI)** — ratio of credentialed elite aspirants to elite positions, aggregated across domains; feeds $\sigma_{\mathrm{elite}}$. *(Doc 4 §6.)*
- **Baseline** — a society-specific, explicitly defended reference interval defining "normal"; never universal. *( $\mathcal{B}$; Doc 2 §0, Doc 4 §4.)*
- **z-score normalization** — expression of each variable as standard deviations from its baseline mean, sign-oriented so larger = more stress. *(Doc 2 §4.1.)*

### 4.4 Dynamics and transitions

- **Vector field** — the deterministic part of the dynamics. *( $\mathbf{F}$; Doc 2 §6.)*
- **Potential** — the function whose minima are poliform attractors; estimable as $-\log\hat\rho$ (location/depth only). *( $V$; Doc 2 §6.2.)*
- **Rotational component** — the non-conservative part of $\mathbf{F}$ producing secular cycles. *( $R$; Doc 2 §6.1.)*
- **Shock term** — exogenous stochastic perturbation (climate, plague, contact, discovery). *( $\boldsymbol{\eta}$; Doc 2 §6.1.)*
- **Secular cycle** — within-basin oscillation (elite overproduction, immiseration, fiscal capacity, legitimation); the cliodynamics object. *(Doc 3 §2.3.)*
- **Transition types** — Type 1 (cross-basin), Type 2 (basin reshaping), Type 3 (bifurcation). *(Doc 2 §6.3.)*
- **Distance-to-bifurcation** — the signature diagnostic; distance to the nearest basin boundary, with geometric (Tier 1) and dynamical (Tier 2) readings. *(Doc 2 §6.4.)*
- **Hysteresis** — the irreversibility of poliform transitions: the path back is not the path forward reversed. *(Doc 3 §6.)*
- **Collapse** — a downward (higher- to lower-energy) transition, often skipping intermediate forms. *(Doc 3 §6.)*

### 4.5 Methodological and epistemic

- **Tier 1 / Tier 2** — the two evidentiary tiers: Tier 1 = basin location/depth from cross-sectional density (estimable now); Tier 2 = flow field, transitions, dynamical distance-to-bifurcation (longitudinal, deferred). *(Doc 2 §3.)*
- **Estimated vs. computed** — the integrity labels: *computed* = produced end-to-end from disclosed data by disclosed code; *estimated* = an expert/interpolated stand-in. Estimated values are never reported with computed-looking precision. *(Doc 4 §1.)*
- **Bridging Hypothesis (H0)** — the claim that the CSI tracks distance-to-bifurcation; the load-bearing link between the stress and poliform layers. *(Doc 2 §1.3.)*
- **Reflexivity** — the modification of a social system by knowledge of its own dynamics; modeled as a two-layer coupling $\Phi(O,\mathcal{E})$, a research target, not a solved problem. *(Doc 2 §8.1.)*
- **Anti-Systemic Political Event (ASPE)** — a pre-defined class of political outcomes (non-institutional nomination; delegitimation candidacy >35%; third-party >15%). *(Doc 5 §2.)*
- **The Mule Problem** — that the framework predicts the *type* of emergence likely in a stressed state, never which *individual* fills the role (after Asimov). *(Doc 1 §2, Doc 2 §10.)*
- **Epistemic phase separation** — a demixing of an information commons into near-hermetic communities diverging on basic facts above a fragmentation threshold. *(Doc 1 §5, Doc 5 §4.)*
- **Velocity mismatch** — institutional feedback operating slower than the information environment reorganizes, disabling self-correction. *(Doc 1 §5.)*
- **Negative control** — a high-stress non-transition (or stable) case used to test the framework's *specificity*; what makes retrodiction falsifiable. *(Doc 6 §4.)*
- **Two-sided scoring** — requiring both sensitivity (flagging transitions) and specificity (not flagging controls). *(Doc 6 §5.)*
- **Pre-registration** — fixing cases, criteria, weights, and thresholds before computation, to prevent post-hoc fitting. *(Doc 2 §11.4, Doc 6.)*
- **Pre-analysis plan (PAP)** — a registry-grade, frozen-before-fielding statement of constructs, decision rules, power, and confirmatory hypotheses for a forward instrument; pre-registration applied to data not yet collected. *(Doc 11.)*
- **Confirmatory vs. exploratory** — the pre-registered, falsifier-bearing hypotheses (corrected for multiplicity) versus all other, clearly-labeled secondary analysis. *(Doc 11 §7.)*
- **Anchor noise floor** — the mean cross-group gap on neutral-anchor items; the measurement-noise baseline against which "real" charged-item divergence is judged. *(Doc 9 §3.1; Doc 10 §3; Doc 11 §7.)*
- **Cut code (R/L/S/X)** — the directional-balance tag on a charged item: which prior its correct answer cuts against (right / left / swing-incumbent / cross-partisan). *(Doc 10 §2, §5.)*
- **Directional-balance ledger** — the audit ensuring correct answers favor no partition, run per bank and per wave. *(Doc 9 §3.3; Doc 10 §5.)*
- **Dead-band** — the small change band within which a live-series directional item is coded "about the same," preventing within-revision noise from forcing a direction. *(Doc 10 §7; Doc 11 §6.)*
- **Dark subset / Goodhart tripwire** — rotating items held back longer to detect coaching/gaming of the published instrument. *(Doc 9 §9; Doc 10 §9.)*
- **Rigor leads reach** — the dissemination principle: establish priority cheaply now; defer promotion of predictive claims until measurement is real. *(Doc 1 §8, Doc 8.)*

### 4.6 Lineage and positioning

- **Cliodynamics** — Turchin's quantitative-history program; the *direct parent* of Civilodynamics, extended (not superseded) by it. *(Doc 1 §3.)*
- **Structural-demographic theory** — the elite-overproduction/immiseration/fiscal-stress model of instability, inherited from cliodynamics. *(Doc 1 §3, Doc 5 §1.)*
- **Theoretical morphospace** — McGhee's program mapping possible-form-space in biology; the homologous (not identical) source of the poliform idea. *(Doc 3 §4.)*
- **The three novelty claims** — the narrow basis of CVD's distinctness: (1) the epistemic/information layer as a first-class state variable; (2) the poliform↔morphospace integration; (3) real-time measurement. *(Doc 1 §3.)*

---

## 5. Status and evidentiary tags (controlled usage)

To keep claims honest, the corpus uses a fixed status vocabulary:

| Tag | Meaning |
|-----|---------|
| **Computed** | End-to-end from disclosed data and code. |
| **Estimated** | Expert/interpolated stand-in; no computed precision. |
| **Illustrative** | Shown to convey shape/magnitude; not a result. |
| **Tier 1** | Supported by cross-sectional density (location/depth). |
| **Tier 2** | Requires longitudinal data (flow/transitions); currently deferred. |
| **Hypothesis** | A stated, falsifiable claim with a way to be wrong (not a result). |
| **Research target** | An aim of the program, not yet a capability. |

Every quantitative claim in the corpus should carry the appropriate tag; an untagged number defaults to *estimated/illustrative*.

---

## 6. Deprecated and corrected usage

A quick-reference register of usages retired across the corpus, with the correction and rationale. **Consult before reusing older phrasing.**

| Deprecated usage | Corrected usage | Rationale | Canonical doc |
|------------------|-----------------|-----------|---------------|
| $\mathbf{S}(t)$ for *both* configuration and stress | $\mathbf{S}$ = configuration; $\mathbf{u}$ = stress | They are different objects (dimensions, units, timescales). | Doc 2 §1 |
| Stress labels $E$ (economic), $C$ (cohesion) | $\sigma_{\mathrm{econ}}$, $\sigma_{\mathrm{coh}}$ | Collided with configuration energy/coordination. | Doc 2 §1 |
| Reflexivity coupling $R(O,E)$ | $\Phi(O,\mathcal{E})$ | $R$ = rotational component; $E$ = energy axis. | §2 (this doc) |
| "$\Omega$ is a Riemannian manifold" | "$\Omega$ with a flat Mahalanobis metric" | No position-dependent metric tensor is specified or needed. | Doc 2 §2.2 |
| CSI "$>2$ ⇒ outside 95%, $>3$ ⇒ 99.7%" | $\textit{CSI}_{\mathrm{M}}^2\sim\chi^2_p$; thresholds from $\chi^2$/Hotelling-$F$ | The $2\sigma/3\sigma$ rule is univariate; the distance is multivariate. | Doc 2 §4.4 |
| Biology link as "structural identity" | "structural homology / shared mathematics" | Identity overclaims; substrate, generative process, selection, and lineage-isolation differ. | Doc 3 §4 |
| Conservation laws via "Noether's theorem" | "empirical quasi-conservation hypotheses" | No action principle exists from which to derive them. | Doc 2 §8.2 |
| "Universality classes" (as a property) | "universality (a hypothesis under test)" | Requires demonstrated scaling/critical exponents. | Doc 2 §8.3 |
| Clusters treated as "attractors" | "clusters (Tier 1); attractors (Tier 2 hypothesis)" | Density shows clustering, not dynamics. | Doc 2 §3, Doc 3 §3 |
| CVD "supersedes" other disciplines | "extends / departs from" | More accurate and strategically necessary (alliances). | Doc 1 §3, §7 |
| Weimar as "validation" | "hypothesis-generating analogy" | A qualitatively-scored sample of one cannot validate. | Doc 5 §5 |
| "$V\!=\!-\log\rho$ gives the dynamics" | "gives location/depth, not the flow field" | Density does not yield $\mathbf{F}$ or $R$. | Doc 2 §6.2 |
| Information degradation "deliberately cultivated" | the *mechanism* (engagement-optimization) is retained; coordinated *intent* is not asserted | The intent claim is hard to establish and pulls toward unfalsifiability. | Doc 5 §4 |

---

## 7. Closing

A discipline that coins terms must govern them, and one that has corrected errors must record the corrections so they do not return. This lexicon is the single source of truth for what the words and symbols of Civilodynamics mean, how the concepts relate as a type system, and which usages have been retired. It is a living standard: as the empirical and computational program proceeds (Documents 4, 6, 8, 9), terms will be added and refined here first, and the rest of the corpus reconciled to match. The $\Phi$/$\mathcal{E}$ adoption noted in earlier versions is now reflected in Document 2 §8.1 and §11.10; this version incorporates the FCR-instrument notation and terms introduced by Document 9 (§2, §4.3). The standing next task is to add configuration-database and reference-implementation vocabulary as those building-phase artifacts take shape.

---

*Working draft. Cite with caution. This lexicon canonicalizes terminology and notation defined across the corpus; where a full definition lives elsewhere, that document governs. New terms and symbols are introduced by amending this document.*
