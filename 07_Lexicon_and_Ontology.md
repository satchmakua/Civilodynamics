# Civilodynamics — Lexicon and Ontology

**Canonical Corpus, Document 7 of 8 · Version 0.2 · June 2026, revised November 2026**
**Satchel Hamilton · Civilodynamics Initiative**

> **Status and role.** This is the discipline's controlled vocabulary: the authoritative reference for every coined term, every symbol, and the relationships among the core concepts. It consolidates terminology defined in full elsewhere and exists to prevent terminological and notational drift as the corpus grows and as collaborators join. **Where a term's full definition lives in another document, that document governs; this lexicon canonicalizes the short form and the notation.** Beyond a glossary, §3 specifies the *ontology* (how the objects relate as a type system) and §6 records *deprecated and corrected usage* so that prior errors do not reappear. In assembling the notation (§2), two latent symbol collisions in the reflexivity model were identified and are resolved here. Version 0.2 resolves seven more that version 0.1 missed, and records the usages retired by the November 2026 review of the corpus (§2, §6).

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
| $m$ | Baseline sample size | Number of observations in $\mathcal{B}$; thresholds depend on the *effective* $m$, which must exceed $p$ comfortably. *(Doc 2 §4.4.)* |
| $\ell,\ b,\ \zeta,\ \boldsymbol{\xi},\ \kappa$ | Configuration sub-components reassigned in v0.2 | Coordination layers; bandwidth; verticality; extraction-modality vector; clustering coefficient. **See collision note below.** *(Doc 2 §2.1.)* |
| $E,C,I,X,T,K$ | Configuration axes | Energy, Coordination, Information, eXtraction, Trust, ecology (K). |
| $\sigma_{\mathrm{econ}},\sigma_{\mathrm{elite}},\sigma_{\mathrm{leg}},\sigma_{\mathrm{coh}},\sigma_{\mathrm{epi}},\sigma_{\mathrm{dem}}$ | Stress blocks | Economic, elite, legitimacy, cohesion, epistemic, demographic. |
| $\Sigma$ | Covariance matrix | Subscript $\mathcal{B}$ for baseline covariance, $\Sigma_{\mathcal{B}}$. |
| $\boldsymbol{\mu}_{\mathcal{B}}$ | Baseline centroid | Mean of the stress vector over the baseline. |
| $d(\cdot,\cdot)$ | **Mahalanobis metric** | $\sqrt{(\cdot)^{\mathsf{T}}\Sigma^{-1}(\cdot)}$; a *flat* metric (see §6). |
| $\textit{CSI}_{\mathrm{lin}},\textit{CSI}_{\mathrm{nl}},\textit{CSI}_{\mathrm{M}}$ | The three CSI constructions | Linear, nonlinear, Mahalanobis. |
| $\Pi,\ B(\Pi),\ \partial B(\Pi)$ | Poliform, its basin, its boundary | A poliform *is* the attractor/basin. |
| $V(\mathbf{S},t)$ | Potential function | Minima are poliform attractors; $\hat V \approx -\log\hat\rho$ under the assumptions of Doc 2 §6.2. |
| $\hat\rho$ | Empirical density estimate | Kernel density over historical configurations. |
| $\mathbf{F}(\mathbf{S},t)$ | Deterministic vector field | $\mathbf{F}=-\nabla V + R$. |
| $R(\mathbf{S},t)$ | **Rotational (non-conservative) component** | Generates secular cycles. **See collision note below.** |
| $\boldsymbol{\eta}(t)$ | Shock term | Exogenous stochastic perturbation. |
| $\mathcal{B}$ | Baseline interval | Society-specific; explicitly defended, never universal. |
| $O(t)$ | Object layer (reflexivity) | Actual social dynamics. |
| $\mathcal{E}(t)$ | **Epistemic/belief layer (reflexivity)** | Beliefs about the dynamics. **Script-E; see collision note.** |
| $\Phi(O,\mathcal{E})$ | **Reflexivity coupling** | **Newly assigned symbol; see collision note.** |
| $\Gamma(\cdot)$ | ECI aggregate | $\textit{ECI}=\Gamma(\textit{MOS},\textit{FCR},\textit{NCI})$; equal-weight mean by default. Formerly $g$. *(Doc 4 §5; Doc 9 §2.4.)* |
| $c_{g,k}$ | Per-item, per-group correct-belief rate | FCR instrument; group $g$, item $k$. *(Doc 9 §2.1.)* |
| $\delta_k,\ \Delta_k$ | Signed and absolute cross-group gap on item $k$ | $\delta_k = c_{A,k}-c_{B,k}$; $\Delta_k=\lvert\delta_k\rvert$. Two-group partitions are primary. *(Doc 9 §2.2.)* |
| $v_k$ | Sampling variance of $\hat\delta_k$ | Design-based; used in the noise correction. *(Doc 9 §2.2.)* |
| $\overline{\Delta}_{\mathcal{S}}$ | Noise-corrected root-mean-square gap over an item set $\mathcal{S}$ | $\sqrt{\max\{0,\ \lvert\mathcal{S}\rvert^{-1}\sum_{k\in\mathcal{S}}(\hat\delta_k^{2}-\hat v_k)\}}$. *(Doc 9 §2.2.)* |
| $\theta$ | Consensus threshold | Gap below which an item counts as agreed; set above the noise floor. *(Doc 9 §2.3, §8.)* |
| $\textit{FCR}_c,\ \textit{FCR}_\theta$ | The two FCR statistics | $\textit{FCR}_c = 1-\overline{\Delta}_{\mathcal{K}}$ (primary); $\textit{FCR}_\theta$ = share of charged-core items with $\hat\Delta_k<\theta$. *(Doc 9 §2.3.)* |
| $\mathcal{A},\ \mathcal{A}_0,\ \mathcal{K},\ \mathcal{K}_{\mathrm{f}}$ | Item sets | Anchor core $\mathcal{A}=\mathcal{A}_0\cup\mathcal{K}$; neutral anchors $\mathcal{A}_0$ (noise floor); charged core $\mathcal{K}$ (the FCR is computed here); $\mathcal{K}_{\mathrm{f}}$ = charged core less swing items. *(Doc 9 §3.2, §3.3.)* |
| $\bar\delta$ | Balance statistic | Signed mean gap over $\mathcal{K}_{\mathrm{f}}$; must lie within tolerance of zero. *(Doc 9 §3.3.)* |
| $\textit{XP}$ | Expressive component | $\textit{FCR}_c^{a}-\textit{FCR}_c^{b}$; consensus recovered by accuracy incentives. *(Doc 9 §4.)* |
| $\textit{ACC}$ | Knowledge level | Mean cross-group correct rate over $\mathcal{K}$; companion to FCR, never folded in, never reported by group. *(Doc 9 §5.2.)* |
| $(\cdot)^{b},\ (\cdot)^{a}$ | Response-arm superscripts | Belief (standard) arm; accuracy-incentivized arm. *(Doc 9 §4.)* |

> **Resolved symbol collisions.** Two collisions in the reflexivity model of Document 2 §8.1 were resolved in version 0.1, and Document 2 has been reconciled to match:
> 1. The reflexivity **coupling term** was written $R(O,\mathcal{E})$, but $R$ already denotes the **rotational component** of the dynamics ($\mathbf{F}=-\nabla V + R$). The coupling is reassigned the symbol **$\Phi$**; $R$ is reserved for the rotational component.
> 2. The reflexivity **epistemic layer** was written $E(t)$, but $E$ already denotes the **energy axis** of the configuration vector. The epistemic layer is reassigned the script symbol **$\mathcal{E}(t)$**; $E$ is reserved for energy.
> These join the earlier resolution of the $\mathbf{S}(t)$ overload (configuration $\mathbf{S}$ vs. stress $\mathbf{u}$) and the energy/economic and coordination/cohesion label collisions (Document 2 §1).
>
> **Seven further collisions resolved in version 0.2.** Version 0.1 claimed to have cleared the notation and had not. Each of the following used one symbol for two things:
> 1. $h$ — coordination layers *and* the configuration-to-stress map $h(\cdot)$. Layers are now $\ell$.
> 2. $B$ — bandwidth *and* the basin $B(\Pi)$ (with $\mathcal{B}$ the baseline besides). Bandwidth is now $b$.
> 3. $V$ — verticality *and* the potential. Verticality is now $\zeta$.
> 4. $\boldsymbol{\mu}$ — the extraction-modality vector *and* the baseline centroid $\boldsymbol{\mu}_{\mathcal{B}}$. The modality vector is now $\boldsymbol{\xi}$.
> 5. $c$ — the clustering coefficient *and* the correct-belief rate $c_{g,k}$. The clustering coefficient is now $\kappa$.
> 6. $n$ — the dimension of $\mathbf{S}$ *and* the baseline sample size. The sample size is now $m$.
> 7. $g$ — the ECI aggregate *and* the subgroup index. The aggregate is now $\Gamma$.
>
> Script and italic forms of one letter remain distinct symbols by convention ($E$ and $\mathcal{E}$; $K$ and $\mathcal{K}$; $B$, $b$ and $\mathcal{B}$).

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
- **Constraint stack** — the six layers carving the morphospace: energy, coordination, information, extraction, trust, ecology. *( $E,C,I,X,T,K$; Doc 3 §4.1, Doc 2 §2, Doc 4 §7.)*
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
  - **Media Overlap Score (MOS)** — one minus the Jensen–Shannon divergence (base-2 logarithms, so bounded in $[0,1]$) of two communities' source distributions; 1 = identical sources. *(Doc 4 §5.1.)*
  - **Factual Consensus Rate (FCR)** — cross-group agreement on a verifiable battery, computed over the charged core: one minus the noise-corrected gap ($\textit{FCR}_c$, primary), and the share of items whose gap is below threshold ($\textit{FCR}_\theta$). *(Doc 4 §5.2; full instrument and pre-registration Doc 9.)*
    - **Anchor core** — the fixed item set held constant for longitudinal comparability. It has two parts: the **neutral anchors**, non-political items that supply the noise floor and do not enter the FCR, and the **charged core**, the charged-but-settled items over which the FCR is computed. *(Doc 9 §3.1–§3.2; Doc 10.)*
    - **Rotating pool** — the per-wave refreshed item set guarding against priming and coaching; reported separately. *(Doc 9 §3.2.)*
    - **Directional balance** — the requirement that correct answers, as a set, favor no partition. Designed in through cut codes; tested by the signed mean gap. Because it is enforced by item selection, the instrument cannot say which group is better informed. *(Doc 9 §3.3.)*
    - **Ground-truth adjudication** — the pre-registered sourcing hierarchy and multi-perspective panel that admit only settled, documentable items. *(Doc 9 §3.4; procedures Doc 12 §2.)*
    - **Sourcing hierarchy** — (i) official statistical series; (ii) the standing, concordant consensus of independent scientific bodies; (iii) the documentable public record. An agency statement is not a tier-(i) source. *(Doc 9 §3.4.)*
    - **Divergence rule** — when an official source and the scientific-consensus tier diverge on an item, the item is suspended and returned to the panel; the instrument does not resolve the dispute. *(Doc 9 §3.4; Doc 12 §2.5.)*
    - **Adjudication panel** — the cross-perspective body whose unanimity *on settledness* admits an item; the safeguard against the instrument-builder deciding what is a fact. *(Doc 12 §2.)*
    - **Cognitive pretest (think-aloud)** — interviews verifying respondents read an item as intended and answer on belief, not cue, before freeze. *(Doc 9 §3.5; Doc 12 §3.)*
    - **Freeze gate** — passing both adjudication and pretest, hashing instrument v1.1, and registering the pre-analysis plan. *(Doc 12 §4.)*
    - **Incentivized-accuracy arm / expressive component ($\textit{XP}$)** — the accuracy-paid arm isolating believed from performed divergence, and the consensus it recovers. *(Doc 9 §4.)*
  - **Network Connectivity Index (NCI)** — share of cross-community ties in information networks, relative to its random-mixing expectation and computed on an exogenous partition. *(Doc 4 §5.3.)*
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
- **Measurement independence** — the condition on any test of H0 that the stress index and the distance-to-boundary share no variables; without it the two co-vary by construction. *(Doc 2 §1.3; Doc 4 §1.)*
- **Effective sample size** — the number of independent observations a serially correlated baseline is worth; it, not the nominal count, governs the thresholds and the dimension at which $\textit{CSI}_{\mathrm{M}}$ can be computed. *(Doc 2 §4.4.)*
- **Reflexivity** — the modification of a social system by knowledge of its own dynamics; modeled as a two-layer coupling $\Phi(O,\mathcal{E})$, a research target, not a solved problem. *(Doc 2 §8.1.)*
- **Anti-Systemic Political Event (ASPE)** — a pre-defined class of political outcomes (non-institutional nomination; delegitimation candidacy >35%; third-party >15%). *(Doc 5 §2.)*
- **The Mule Problem** — that the framework predicts the *type* of emergence likely in a stressed state, never which *individual* fills the role (after Asimov). *(Doc 1 §2, Doc 2 §10.)*
- **Epistemic phase separation** — a demixing of an information commons into near-hermetic communities diverging on basic facts above a fragmentation threshold. *(Doc 1 §5, Doc 5 §4.)*
- **Velocity mismatch** — institutional feedback operating slower than the information environment reorganizes, disabling self-correction. *(Doc 1 §5.)*
- **Negative control** — a high-stress non-transition (or stable) case used to test the framework's *specificity*; what makes retrodiction falsifiable. *(Doc 6 §4.)*
- **Two-sided scoring** — requiring both sensitivity (flagging transitions) and specificity (not flagging controls). *(Doc 6 §5.)*
- **Trailing baseline** — the outcome-blind baseline rule of the retrodiction protocol: for each year, a window of fixed length ending a fixed lag earlier, identical for every case. *(Doc 6 §2.)*
- **Pre-registration** — fixing cases, criteria, weights, and thresholds before computation, to prevent post-hoc fitting. *(Doc 2 §11.4, Doc 6.)*
- **Pre-analysis plan (PAP)** — a registry-grade, frozen-before-fielding statement of constructs, decision rules, power, and confirmatory hypotheses for a forward instrument; pre-registration applied to data not yet collected. *(Doc 11.)*
- **Confirmatory vs. exploratory** — the pre-registered, falsifier-bearing hypotheses (corrected for multiplicity) versus all other, clearly-labeled secondary analysis. *(Doc 11 §7.)*
- **Anchor noise floor** — the noise-corrected gap on the neutral anchors, difficulty-matched to the charged items; the baseline against which charged-core divergence is judged. *(Doc 9 §2.3, §3.1; Doc 10 §3; Doc 11 §7.1.)*
- **Cut code (R/L/S/X)** — the provisional tag on a charged item for which prior its correct answer is expected to cut against (right / left / swing-incumbent / cross-partisan). A hypothesis about respondents, confirmed by the panel and validated in the pilot. *(Doc 10 §2, §5.)*
- **Directional-balance ledger** — the count of cut codes used to design a balanced bank, re-run per wave; the signed mean gap is the test it prepares for. *(Doc 9 §3.3; Doc 10 §5.)*
- **Key type (fixed / live / wave-set)** — whether an item's correct answer is closed, read from a still-moving series, or set fresh each wave. *(Doc 10 §2.)*
- **Dead-band** — the small change band within which a live or wave-set directional item is coded "about the same," preventing within-revision noise from forcing a direction. *(Doc 10 §7; Doc 11 §6.)*
- **Dark subset / Goodhart tripwire** — rotating items held back longer to detect coaching/gaming of the published instrument. *(Doc 9 §9; Doc 10 §9.)*
- **Rigor leads reach** — the dissemination principle: establish priority cheaply now; defer promotion of predictive claims until measurement is real. *(Doc 1 §8, Doc 8.)*

### 4.6 Lineage and positioning

- **Cliodynamics** — Turchin's quantitative-history program; the *direct parent* of Civilodynamics, extended (not superseded) by it. *(Doc 1 §3.)*
- **Structural-demographic theory** — the elite-overproduction/immiseration/fiscal-stress model of instability, inherited from cliodynamics. *(Doc 1 §3, Doc 5 §1.)*
- **Theoretical morphospace** — the program, begun by Raup and developed by McGhee, of mapping possible-form-space in biology; the homologous (not identical) source of the poliform idea. *(Doc 3 §4.)*
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
| CVD "supersedes" other disciplines | "extends / departs from" | More accurate: the discipline extends its parent program and works alongside it. | Doc 1 §3, §7 |
| Weimar as "validation" | "hypothesis-generating analogy" | A qualitatively-scored sample of one cannot validate. | Doc 5 §5 |
| "$V\!=\!-\log\rho$ gives the dynamics" | "gives location/depth, not the flow field" | Density does not yield $\mathbf{F}$ or $R$. | Doc 2 §6.2 |
| Information degradation "deliberately cultivated" | the *mechanism* (engagement-optimization) is retained; coordinated *intent* is not asserted | The intent claim is hard to establish and pulls toward unfalsifiability. | Doc 5 §4 |

**Retired by the November 2026 review.**

| Deprecated usage | Corrected usage | Rationale | Canonical doc |
|------------------|-----------------|-----------|---------------|
| Sub-component symbols $h$, $B$, $V$, $\boldsymbol{\mu}$, $c$; baseline size $n$; aggregate $g$ | $\ell$, $b$, $\zeta$, $\boldsymbol{\xi}$, $\kappa$; $m$; $\Gamma$ | Each collided with another symbol (§2). | Doc 2 §2.1, §4.4; Doc 9 §2.4 |
| The Seshat clustering study by "Shults and colleagues" | Miranda and Freeman (2020) | Misattribution. | Doc 3 §3.1 |
| Plains nomad societies "wholly out of contact" / "genuinely isolated" | Institutionally independent; the horse was an Old World introduction | The enabling technology diffused; the social form did not. | Doc 3 §5 |
| The comparative record shows "attractor structure" | It shows clustering, read as candidate attractors | Same error as the row above on clusters, surviving in the charter. | Doc 1 §3 |
| FCR computed over the whole anchor core | FCR computed over the charged core; neutral anchors are the noise floor | Near-zero-gap anchors diluted the statistic by an arbitrary item ratio. | Doc 9 §2.3 |
| Mean of estimated absolute gaps | Noise-corrected root-mean-square gap | The former is biased upward by sampling noise and moves with sample size. | Doc 9 §2.2 |
| Cut codes as properties of items | Cut codes as provisional hypotheses, validated in the pilot | A code is a guess about respondents. | Doc 10 §5 |
| "Fielding the FCR makes Prediction 2 resolvable" | Prediction 2 resolves on the components with a 2024 value (MOS; NCI where available) | The FCR has no 2024 value. | Doc 9 §7; Doc 5 §7 |
| NCI "0.5 = balanced" | NCI relative to its random-mixing expectation | 0.5 holds only for two communities of equal size. | Doc 2 §5; Doc 4 §5.3 |
| JSD "bounded $[0,1]$" without a base | JSD with base-2 logarithms | The bound depends on the base. | Doc 2 §5 |
| Mobility deficit as one minus a ratio of rank correlations | One minus a ratio of absolute-mobility rates | As written, the measure fell as mobility worsened. | Doc 4 §3 |
| Lower-half real wages "by quintile" from the CES | Census quintile income series, with CES average earnings as the check | The CES has no quintiles. | Doc 4 §3 |
| The Survey of Earned Doctorates as an NCES source | An NCSES (NSF) survey | Wrong agency. | Doc 4 §2.1 |
| A retrodiction baseline chosen as the calm before the crisis | A trailing baseline set by a rule blind to the outcome | Choosing the baseline with the outcome in view defeats blind computation. | Doc 6 §2 |
| The nine-case retrodiction result as validation | A demonstration of the protocol with a stated chance level | An 80% AUC arises by chance about one time in twelve. | Doc 6 §5.3 |

---

## 7. Closing

A discipline that coins terms must govern them, and one that has corrected errors must record the corrections so they do not return. This lexicon is the single source of truth for what the words and symbols of Civilodynamics mean, how the concepts relate as a type system, and which usages have been retired. It is a living standard: as the empirical and computational program proceeds (Documents 4, 6, 8, and the building-phase documents 9–12), terms are added and refined here first, and the rest of the corpus reconciled to match.

Version 0.2 is a reminder of why the register in §6 exists. Version 0.1 announced that the notation had been cleared of collisions; a review five months later found seven more, along with a misattributed study, an overstated piece of evidence, and several definitions that did not say what they meant. All are recorded above. The standing next task is to add configuration-database and reference-implementation vocabulary as those building-phase artifacts take shape.

---

*Working draft. Cite with caution. This lexicon canonicalizes terminology and notation defined across the corpus; where a full definition lives elsewhere, that document governs. New terms and symbols are introduced by amending this document.*
