# Civilodynamics — Mathematical and Methodological Foundations

**Canonical Corpus, Document 2 of 8 · Working Draft v0.1 · June 2026**
**Satchel Hamilton · Civilodynamics Initiative**

> **Status of this document.** This is the formal core of the Civilodynamics corpus and the dependency for Documents 1 and 3–8. It consolidates and supersedes the earlier *Formalizing the Poliform* companion paper and the mathematical sections of the v1.0 Foundational Charter. It is a *working draft*: the framework is specified, but most quantities are not yet computed against data. Throughout, the document is explicit about what is **settled** (definitions, mathematical structure, estimability claims), what is **schematic** (illustrative values, candidate functional forms), and what is **deferred** (calibration, validation, and several open theoretical problems collected in §11). Where this draft corrects an error or overstatement in prior drafts, it says so in a marked **Correction** callout.

---

## 0. Purpose and scope

Civilodynamics models human societies as complex dynamical systems whose structural state can be measured and whose proximity to qualitative reorganization ("phase transition") can be estimated. This document specifies the mathematical objects the discipline uses and the methodological commitments that govern their use. It does four things:

1. Resolves a latent inconsistency in the prior corpus by distinguishing two state descriptions — a **structural configuration vector** that locates a society in poliform morphospace, and a **stress readout** that measures a society's distance from its own stable regime — and specifies their relationship.
2. Defines poliforms as **basins of attraction** and separates two distinct evidentiary claims about them (where the basins *are*, versus how a society *moves* between them) that prior drafts conflated.
3. Repairs the construction and interpretation of the **Civilizational Stress Index (CSI)**, including a mathematical error in how the Mahalanobis form was read.
4. States precisely what is estimable from data available today and what requires data and methods not yet in hand.

This document deliberately does **not** make substantive empirical claims about any particular society; those belong to Documents 5 (United States case study) and 6 (Retrodiction Casebook). It is concerned only with whether the apparatus is coherent, rigorous, and falsifiable.

### Notation conventions

- Vectors are bold lowercase or uppercase (**S**, **u**); scalars are italic ($\textit{CSI}$, $D$); matrices are uppercase ($\Sigma$).
- $\mathbb{R}^n$ denotes real $n$-space; $\Omega \subseteq \mathbb{R}^n$ is the configuration space (the morphospace).
- $^{\mathsf{T}}$ denotes transpose; $\Sigma^{-1}$ the inverse covariance (precision) matrix.
- $t$ is time in years (historical work) with finer resolution permitted for contemporary measurement.
- A **baseline** $\mathcal{B}$ is a stated reference interval for a specific society used to define "normal" for that society. Baselines are society-specific and explicitly defended, never universal.

---

## 1. Two state descriptions, one framework

The prior corpus uses the symbol $\mathbf{S}(t)$ for *two different vectors*: the six-layer constraint stack $(E, C, I, X, T, K)$ in the poliform/morphospace work, and the six-component stress vector $(E, D, L, C, \Psi, P)$ in the stress-index work. These are not the same object, they do not have the same dimensions, units, or timescales, and treating them as interchangeable is a genuine source of confusion. We separate them explicitly.

### 1.1 The structural configuration vector (slow variables)

A society's structural configuration is a point

$$\mathbf{S}(t) = \big(E,\; C,\; I,\; X,\; T,\; K\big) \in \Omega \subseteq \mathbb{R}^n$$

where the six blocks are the layers of the **constraint stack** (Document 3):

| Symbol | Layer | Role |
|--------|-------|------|
| $E$ | Energy / thermodynamics | Complexity ceiling |
| $C$ | Coordination scaling | How coordination extends past the Dunbar limit |
| $I$ | Information architecture | How information flows; **the discipline's distinctive axis** |
| $X$ | Extraction logic | How surplus is generated and captured |
| $T$ | Trust topology | Which institutional forms are feasible |
| $K$ | Ecological carrying capacity | The biophysical envelope |

Each block decomposes into measurable sub-components (§2); the minimal specification uses $n \approx 24$. These are **slow variables**: energy regime, coordination architecture, and information architecture change over decades to centuries. The configuration vector answers the question *which poliform does this society occupy, and where within it?*

### 1.2 The stress readout (fast variables)

A society's stress state is a vector of observables

$$\mathbf{u}(t) = \big(\sigma_{\mathrm{econ}},\; \sigma_{\mathrm{elite}},\; \sigma_{\mathrm{leg}},\; \sigma_{\mathrm{coh}},\; \sigma_{\mathrm{epi}},\; \sigma_{\mathrm{dem}}\big) \in \mathbb{R}^{p}$$

corresponding to the prior corpus's economic stress, elite dynamics, legitimacy, social cohesion, epistemic coherence, and demographic pressure blocks (the $(E, D, L, C, \Psi, P)$ of the charter and Document 5). With sub-components, $p \approx 14\text{–}18$. These are **faster variables** — wages, trust, polarization, and media fragmentation move on the scale of months to a few years — and they are the quantities for which good modern time series exist.

> **Correction (notation, vs. prior drafts).** The earlier symbol overlap is a hazard: configuration-$E$ is *energy throughput*, stress-$E$ is *economic stress*; configuration-$C$ is *coordination*, stress-$C$ is *cohesion*. They are distinct objects. Going forward the corpus should use $\mathbf{S}$ (with axes $E,C,I,X,T,K$) only for structural configuration and $\mathbf{u}$ (with axes $\sigma_{\bullet}$) only for the stress readout. Document 5 will be revised to adopt this.

### 1.3 The relationship between them

The stress readout is not independent of the structural configuration; it is a derived, faster-timescale projection of the structural state, its rate of change, and its deviation from the society's baseline:

$$\mathbf{u}(t) = h\big(\mathbf{S}(t),\; \dot{\mathbf{S}}(t);\; \mathcal{B}\big).$$

Economic stress, elite overproduction, legitimacy decline, cohesion loss, epistemic fragmentation, and demographic pressure are *symptoms* read off a society relative to its own stable regime, sensitive especially near the edges of a basin. The map $h$ is not yet specified functionally; specifying and estimating it is a research target (§11).

This separation lets us state the **central bridging hypothesis** of the discipline cleanly:

> **Bridging Hypothesis (H0).** A society's scalar stress index $\textit{CSI}(t)$ (§4) is monotonically related to its proximity to the nearest basin boundary in $\Omega$ (§3, §6). High stress is the observable signature of a structural configuration approaching a bifurcation.

H0 is the load-bearing claim that connects the easily-measured stress layer to the structurally-fundamental morphospace layer. It is falsifiable: if computed stress indices do not co-vary with independently estimated distance-to-boundary across the retrodiction set (Document 6), H0 fails and the two layers must be treated as only loosely coupled.

---

## 2. The configuration space $\Omega$

### 2.1 The dimensions and their operationalization

Each constraint layer is a vector of measurable sub-components. The minimal specification (full operational definitions, sources, and coverage windows are the subject of Document 4) is:

- **Energy** $E = (e_{\mathrm{pc}},\, \mathrm{EROI},\, H_E)$: per-capita energy throughput (GJ/yr); system-level energy return on energy invested (dimensionless); Shannon entropy of the energy-source mix.
- **Coordination** $C = (N,\, h,\, r,\, \rho_{\mathrm{inst}})$: population; number of coordination layers between median individual and apex node; empirical scaling ratio between adjacent layers; institutional scaffolding density (formal institutions per 10,000 population).
- **Information** $I = (B,\, \lambda,\, V,\, H_I)$: per-capita reachable bandwidth (bits/day); propagation latency to 50% of population; verticality (top-down ÷ lateral volume); Shannon entropy of the information environment.
- **Extraction** $X = (s,\, \boldsymbol{\mu},\, G,\, f,\, r_{\mathrm{rent}})$: surplus as fraction of output; modality vector across extraction types; Gini coefficient; fiscal capacity (share of output reliably extractable centrally); rent share.
- **Trust** $T = (\tau_{\mathrm{inst}},\, \tau_{\mathrm{str}},\, \rho_{\mathrm{clan}},\, c)$: institutional trust; generalized stranger trust; trust-network radius; clustering coefficient.
- **Ecology** $K = (\mathrm{CC},\, \varepsilon,\, D_{\mathrm{clim}},\, D_{\mathrm{dis}})$: carrying capacity; population/carrying-capacity ratio; climate stability; disease pressure.

### 2.2 The metric on $\Omega$

The dimensions have incommensurable units and are correlated, so the Euclidean metric is inappropriate. The natural choice is the **Mahalanobis (whitened-Euclidean) metric**:

$$d(\mathbf{S}_1, \mathbf{S}_2) = \sqrt{(\mathbf{S}_1 - \mathbf{S}_2)^{\mathsf{T}}\, \Sigma^{-1}\, (\mathbf{S}_1 - \mathbf{S}_2)}$$

where $\Sigma$ is the covariance of empirical historical state vectors. This rescales each axis by its empirical spread and removes redundancy from correlated axes; distances measure *how unusual a separation is given the historical record*.

> **Correction (vs. *Formalizing the Poliform* §1).** The prior draft called $\Omega$ "a Riemannian manifold." This is an overstatement. A Riemannian structure requires a position-dependent metric tensor field $g_{ij}(\mathbf{S})$, which the framework neither specifies nor currently needs. The Mahalanobis metric is a single global inner product — i.e., a **flat** geometry (Euclidean after whitening). The correct claim is: $\Omega$ is a constrained subset of $\mathbb{R}^n$ equipped with a flat Mahalanobis metric. A genuinely curved geometry (e.g., a Fisher-information metric on a statistical manifold, which *is* generally curved) is a possible future refinement, but it must be motivated and specified before the word "Riemannian" is used.

### 2.3 Forbidden regions

Most of $\Omega$ is unoccupiable. A society cannot have $N = 10^{8}$ and $h \approx 1$ (a hundred million people cannot be coordinated by one face-to-face layer); it cannot have $B = 10^{10}$ bits/day reachable while trust is mediated only by oral consensus. Following the morphospace tradition (Document 3), the empirically realized region is a small subset of the geometrically possible region, carved by functional and developmental constraints. The existence and shape of these forbidden regions is the central empirical fact the configuration framework exists to explain — and it is testable: compute $\Omega$-coordinates for the Seshat-type sample and confirm the occupied region is sparse and clustered rather than space-filling.

---

## 3. Poliforms as basins of attraction

### 3.1 Definition

A **poliform** $\Pi$ is an attractor of the configuration dynamics (§5): a region of $\Omega$ toward which nearby configurations evolve and from which the system does not escape under small perturbation. Each poliform $\Pi_k$ comprises:

1. a **core attractor** (a region, limit cycle, or low-dimensional manifold) where dynamics settle;
2. a **basin** $B(\Pi_k)$, the set of configurations that evolve toward it absent external shock;
3. a **basin boundary** $\partial B(\Pi_k)$, the separatrix from which trajectories diverge into different basins (often fractal in dissipative systems — implying genuine sensitivity of civilizational fate to small differences near boundaries).

The catalog of Document 3 (foraging band, tribal confederacy, chiefdom, agrarian state, pastoral-nomadic confederacy, city-state, thalassocracy, universalist empire, industrial nation-state, algorithmic surveillance state, and niche forms) is interpreted here as a list of basins in $\Omega$.

### 3.2 Two derived quantities

**Basin depth.** With a potential function $V$ (§5),

$$D(\Pi_k) = \min_{\mathbf{S} \in \partial B(\Pi_k)} V(\mathbf{S}) - V(\Pi_k^{*})$$

where $\Pi_k^{*}$ is the attractor minimum. Deeper basins are more stable; this is the formal version of "how robust is this society in its current poliform."

**Basin volume.** The volume of $B(\Pi_k)$ in $\Omega$ measures the breadth of initial conditions that converge to $\Pi_k$. Some poliforms have large basins (the agrarian state, historically); others are reachable only from narrow conditions (the maritime thalassocracy).

### 3.3 Two evidentiary tiers — kept rigorously separate

> **Correction (vs. prior drafts).** The earlier formalization slid from "we can recover the potential $V$ from the density of historical states" to "we can therefore reconstruct the dynamics, the basins, and the transitions between them." That slide is not licensed and is the most important methodological repair in this document. We separate two tiers with **different evidentiary bars**:
>
> - **Tier 1 — Basin location and relative depth (estimable now).** From a sufficiently dense cross-sectional sample of historical configurations, the *modes* of the empirical density estimate basin centers, and *differences* in $-\log\hat{\rho}$ estimate relative basin depths (§5.3, §7). This uses where societies *are*; it does not require observing any society *move*.
> - **Tier 2 — The flow field and transitions (deferred; needs longitudinal data).** The vector field $\mathbf{F}$ (§5), the rotational/secular component $R$, transition pathways, and distance-to-bifurcation *as a dynamical quantity* require **within-trajectory time series** for individual polities, not a static cloud of different polities. These data are far sparser, and recovering $\mathbf{F}$ from them needs data-driven dynamical-systems methods (§7) that the framework has not yet applied.
>
> Claims in Documents 3, 5, and 6 must be tagged Tier 1 or Tier 2 so that strong (Tier 2) claims are not smuggled in on Tier 1 evidence.

---

## 4. The stress readout and the Civilizational Stress Index

The CSI is a scalar reduction of the stress readout $\mathbf{u}(t)$, measuring distance from a society's stable regime. The corpus carries three candidate constructions; we keep all three, treat disagreement among them as a research signal, and **fix the interpretation of the third**.

### 4.1 Normalization and the baseline problem

Each stress sub-component $x$ is normalized to a $z$-score against the society's baseline $\mathcal{B}$:

$$z_x(t) = \frac{x(t) - \mu_x(\mathcal{B})}{\sigma_x(\mathcal{B})},$$

sign-oriented so that larger $z$ always means more stress. Baseline selection is a **falsifiable methodological claim, not a free parameter**: it must be stated, defended, and subjected to sensitivity analysis. (Document 5's U.S. baseline of 1948–1973 is contestable on exactly these grounds and is treated there with alternative-baseline robustness checks.)

> **Correction (vs. prior drafts) — the baseline covariance is not constructable as written.** Constructions §4.4 require $\Sigma_{\mathcal{B}}$, the covariance of the *full* stress vector over the baseline period. But several components — the epistemic block $\sigma_{\mathrm{epi}}$ above all, plus affective polarization and geographic-sorting measures — have **no data in a mid-20th-century baseline**. One cannot estimate a covariance among variables that do not co-exist in the baseline window. Three honest resolutions, in recommended order:
> 1. **Coverage-restricted baseline vector.** Form $\Sigma_{\mathcal{B}}$ only over the sub-vector with genuine baseline coverage (economic, legitimacy, demographic, partial elite). Treat the epistemic/information block as a **modern-era extension** with its own later baseline and a separately reported stress contribution.
> 2. **Forward baseline.** Move $\mathcal{B}$ to a later, fully-covered interval, accepting that it is a less "pristine" reference.
> 3. **Block-structured covariance with documented imputation**, used only with explicit uncertainty propagation.
> The recommended default is (1). Whichever is chosen must be stated; the framework must not imply a full-vector mid-century $\Sigma$ that cannot exist.

### 4.2 Construction 1 — Weighted linear composite (the transparent baseline)

$$\textit{CSI}_{\mathrm{lin}}(t) = \sum_{i=1}^{p} w_i\, z_i(t), \qquad \sum_i w_i = 1.$$

Weights begin **equal** (a transparent default that makes no claim about relative importance). Alternatives — empirically calibrated weights (risk: overfitting a small historical sample) and theory-derived weights (correct long-run target, requires the calibrated dynamics of §5) — are reported as sensitivity analyses, never as the headline. *Caveat:* equal weights on correlated components double-count shared stress (e.g., wealth concentration, mobility, and wage stagnation are facets of one inequality signal). This is the price of transparency and is the motivation for Construction 3.

### 4.3 Construction 2 — Nonlinear composite (interaction effects)

Stress components do not add independently; economic stress is far more dangerous under low legitimacy, and elite overproduction is most destabilizing under epistemic fragmentation. A minimal interaction model:

$$\textit{CSI}_{\mathrm{nl}}(t) = \textit{CSI}_{\mathrm{lin}}(t) + \beta_1\,(\bar\sigma_{\mathrm{econ}}\!\cdot\!\bar\sigma_{\mathrm{leg}}) + \beta_2\,(\bar\sigma_{\mathrm{elite}}\!\cdot\!\bar\sigma_{\mathrm{epi}}) + \beta_3\,(\bar\sigma_{\mathrm{coh}}\!\cdot\!\bar\sigma_{\mathrm{leg}})$$

where $\bar\sigma_{\bullet}$ are baseline-normalized deviations and the $\beta$ are estimated from historical data. The interaction terms are themselves hypotheses about which *combinations* drive transitions; they must be pre-registered and tested, not fit post hoc to the cases they are meant to explain.

### 4.4 Construction 3 — Phase-space (Mahalanobis) distance, **correctly interpreted**

The most principled scalar is the distance of the current stress vector from the baseline centroid in the metric that accounts for covariance:

$$\textit{CSI}_{\mathrm{M}}(t) = \sqrt{\big(\mathbf{u}(t) - \boldsymbol{\mu}_{\mathcal B}\big)^{\mathsf{T}}\, \Sigma_{\mathcal B}^{-1}\, \big(\mathbf{u}(t) - \boldsymbol{\mu}_{\mathcal B}\big)}.$$

> **Correction (vs. prior drafts) — the central mathematical error.** Prior drafts stated: "$\textit{CSI}_{\mathrm{M}} > 2 \Rightarrow$ outside ~95% of baseline observations; $> 3 \Rightarrow$ outside ~99.7%." **This is the univariate $2\sigma/3\sigma$ rule applied to a multivariate distance, and it is wrong.** For a $p$-dimensional approximately-Gaussian baseline, the *squared* Mahalanobis distance is chi-squared distributed:
> $$\textit{CSI}_{\mathrm{M}}^2(t) \;\sim\; \chi^2_{p}.$$
> Consequently $\mathbb{E}[\textit{CSI}_{\mathrm{M}}^2] = p$ and $\mathbb{E}[\textit{CSI}_{\mathrm{M}}] \approx \sqrt{p}$ — a **typical baseline point already sits at distance $\approx \sqrt{p}$, not near zero.**
>
> Concretely, with $p = 6$ top-level blocks, a baseline-typical state has $\textit{CSI}_{\mathrm{M}} \approx 2.45$ and the 95% contour is at $\approx 3.5$; with $p \approx 14$ sub-components, the baseline mean is $\approx 3.7$ and the 95% contour at $\approx 4.9$. Under the corrected reading, a value like $3.2$ is **inside** the baseline cloud, not "critical." The $2\sigma/3\sigma$ thresholds are correct only for $p = 1$.
>
> **The fix.** Set thresholds from the appropriate $\chi^2_p$ quantiles (e.g., the 95% stress contour is $\textit{CSI}_{\mathrm{M}} = \sqrt{\chi^2_{p,0.95}}$), and when $\boldsymbol{\mu}_{\mathcal B}$ and $\Sigma_{\mathcal B}$ are *estimated* from a finite baseline of size $n$, use the exact finite-sample distribution — a scaled $F$ (Hotelling's $T^2$):
> $$\frac{n - p}{p\,(n-1)}\cdot\frac{n}{n+1}\;\textit{CSI}_{\mathrm{M}}^2 \;\sim\; F_{p,\, n-p}.$$
> Because a historical baseline has a small *effective* $n$, this correction is not cosmetic: it widens the uncertainty on every threshold substantially. Finally, multivariate normality of $\mathbf{u}$ is itself an assumption — it should be tested (e.g., via the empirical distribution of $\textit{CSI}_{\mathrm{M}}^2$ over the baseline), and where it fails, thresholds should be set from the empirical baseline distribution or a Gaussianized transform rather than from $\chi^2$.

### 4.5 Reporting standard

Report all three constructions together, on a single normalized scale, with their disagreement shown. The headline scalar should be a **per-dimension-normalized** quantity (e.g., $\textit{CSI}_{\mathrm{M}}/\sqrt{p}$, or the mean $z$-score), because it is interpretable across different $p$ and does not invite the $\sigma$-rule confusion. Until $\mathbf{u}(t)$, $\boldsymbol{\mu}_{\mathcal B}$, and $\Sigma_{\mathcal B}$ are computed from data, **every CSI value in the corpus is an illustrative estimate and must be labeled as such** (no computed-looking decimals presented as if measured).

---

## 5. The Epistemic Coherence Index as a first-class axis

The Epistemic Coherence Index (ECI) is the discipline's distinctive contribution and the least mature of its measures. It is the operationalization of the information axis $I$ in $\Omega$ and supplies the epistemic stress component $\sigma_{\mathrm{epi}}$ in $\mathbf{u}$. Conceptually, the ECI measures the degree to which a population shares a common factual and informational commons sufficient for collective deliberation to function. Three components (constructions and data in Document 4):

- **Media Overlap Score:** $\textit{MOS}(t) = 1 - \mathrm{JSD}(P_A, P_B)$, the Jensen–Shannon divergence between the information-source distributions of two communities (bounded $[0,1]$; $0$ = identical, $1$ = disjoint). Estimable with good quality from ~2010, with reconstruction to ~2000.
- **Factual Consensus Rate:** the fraction of a standing battery of *verifiable* (not values-based) propositions on which agreement holds across partisan subgroups. **Requires new standing survey infrastructure** — no existing instrument tracks this consistently. This is a Phase-1 metrological investment, feasible and inexpensive at the scale of a rolling tracking poll, and is specified as a fieldable, pre-registered instrument in **Document 9**.
- **Network Connectivity Index:** $\textit{NCI}(t) = E_{\mathrm{cross}} / (E_{\mathrm{cross}} + E_{\mathrm{within}})$, the share of cross-community ties in information-sharing networks (community structure detected by modularity); $0.5$ = balanced, $\to 0$ = hermetic separation.

> **Why this axis is elevated, and the honest cost.** Treating the information environment as a primary state variable — not a background condition — is the cleanest of Civilodynamics' three novelty claims (Document 1). The cost is measurement immaturity and short coverage: the ECI cannot currently be carried back to a mid-century baseline (see §4.1), and its pre-2012 values are interpolations. The framework's credibility depends on *building* the ECI infrastructure rather than asserting ECI values; this is the single highest-priority empirical investment in the program (§11, Document 4, Document 8).

The mechanism by which the information layer matters — engagement-optimizing algorithmic environments amplifying emotionally arousing, identity-confirming, low-accuracy content, thereby degrading the shared factual commons and accelerating the translation of structural stress into political outcome — is defensible and partly measurable, and the framework retains it. It should be stated as a **mechanism**, kept separate from any stronger claim of coordinated intent, which is harder to establish and pulls toward unfalsifiability. (See Document 5's treatment of this as an operationalized sub-hypothesis.)

---

## 6. The dynamics

### 6.1 Governing form

The configuration state evolves as a stochastic dynamical system:

$$\frac{d\mathbf{S}}{dt} = \mathbf{F}(\mathbf{S}, t) + \boldsymbol{\eta}(t),$$

with $\mathbf{F}$ a deterministic vector field and $\boldsymbol{\eta}(t)$ exogenous shock (climate events, plagues, contact, technological discovery). $\mathbf{F}$ is, in general, not derivable in closed form; it is to be reconstructed empirically (§7). For analysis it decomposes into a gradient (relaxational) part and a rotational (cyclic) part:

$$\mathbf{F}(\mathbf{S}, t) = -\nabla V(\mathbf{S}, t) + R(\mathbf{S}, t),$$

where $V$ is a (time-varying) potential whose minima are poliform attractors, and $R$ is the non-conservative component generating the secular cycles documented by the cliodynamics literature. Within a poliform, a society circulates under $R$ (Goldstone–Turchin secular dynamics) without leaving the basin; transitions occur when it crosses $\partial B$.

### 6.2 The scope of $V \approx -\log\rho$, restated

The potential is estimable from the empirical density of historical configurations,

$$\hat V(\mathbf{S}) \approx -\log\hat\rho(\mathbf{S}),$$

with $\hat\rho$ a kernel density estimate. **This recovers $V$ (hence basin centers and relative depths — Tier 1), not $\mathbf{F}$.** The gradient $-\nabla V$ is the relaxational part only; $R$ and the time-dependence of $V$ require longitudinal trajectory data and are Tier 2. Restating §3.3 in dynamical terms: density gives you the landscape's valleys; it does not give you the wind.

### 6.3 A taxonomy of transitions

Three mathematically distinct events are routinely conflated in ordinary talk of "civilizational change":

- **Type 1 — Cross-basin transition.** $\mathbf{S}$ crosses $\partial B(\Pi_k)$ into another basin, via a large $\boldsymbol\eta$-shock or endogenous drift to the boundary. (Rome→post-Roman fragmentation; Bronze Age Collapse.)
- **Type 2 — Basin reshaping.** $\mathbf{F}$ itself changes, deforming the landscape: a basin opens, closes, or migrates. This accompanies regime changes in the constraint stack — energy transitions (foraging→agriculture; agriculture→fossil), information transitions (oral→literate; broadcast→algorithmic), coordination transitions. (Medieval→modern European morphospace.)
- **Type 3 — Bifurcation.** A continuous parameter change causes an attractor to lose stability and split, merge, or vanish (saddle-node, transcritical, pitchfork, Hopf). The contemporary global situation — simultaneous shifts in all six constraint layers — is best modeled as approaching a multi-parameter bifurcation in which several attractors lose stability while one or more new ones form.

### 6.4 Distance-to-bifurcation — the central diagnostic, two readings

The discipline's signature output is **distance-to-bifurcation**. It has two readings that must not be confused:

- **Geometric proxy (Tier 1, available now):** the distance, in the Mahalanobis metric, from the current configuration to the nearest estimated basin boundary. This is a static, density-based estimate.
- **Dynamical quantity (Tier 2, deferred):** the genuine stability margin of the current attractor under the calibrated $\mathbf{F}$ — e.g., the leading eigenvalue of the linearization approaching zero (a critical-slowing-down signature). This requires the calibrated dynamics of §7.

Per H0 (§1.3), CSI elevation is hypothesized to track shrinking distance-to-bifurcation. Forecasts derived from this are **probabilistic, not point predictions**: given an estimated basin $B(\Pi)$ and a shock distribution $P(\boldsymbol\eta)$, the probability of remaining in-basin over horizon $\tau$,

$$P_{\mathrm{stable}}(\mathbf{S}, \tau) = \Pr\big(\mathbf{S}(t)\in B(\Pi)\ \forall\, t\in[0,\tau]\ \big|\ \mathbf{S}(0)=\mathbf{S}\big),$$

is a quantifiable, retrospectively falsifiable forecast — a probability, never a date.

---

## 7. Estimation and computation

What the framework can and cannot compute today, stated plainly.

**Estimable now (Tier 1).**
- $\hat\rho$ and $\hat V = -\log\hat\rho$ over a Seshat-compatible configuration sample → basin centers and relative depths.
- Confirmation (or refutation) of the sparse, clustered, non-space-filling structure of the occupied region of $\Omega$ (§2.3) — a direct test of the morphospace claim.
- Stress readouts $\mathbf{u}(t)$ for modern societies on the coverage-restricted vector, with all three CSI constructions and honest uncertainty.

**Deferred — needs longitudinal data and dedicated methods (Tier 2).**
- The vector field $\mathbf{F}$, via data-driven dynamical-systems methods — sparse identification of nonlinear dynamics (SINDy), Koopman-operator methods, or neural ODEs — applied to *per-polity* trajectories through $\Omega$.
- Explicit basin geometry from the calibrated $\mathbf{F}$, via basin-finding algorithms (e.g., Datseris–Wagemakers) or, for data-reconstructed fields, persistence-based topological methods, cell-mapping, and trajectory tracing.
- The dynamical distance-to-bifurcation and critical-slowing-down indicators.

**Cross-cutting statistical requirements.**
- Finite-sample corrections (§4.4) wherever a baseline mean/covariance is estimated.
- A test of multivariate normality of $\mathbf{u}$, with an empirical-distribution fallback for thresholds.
- A principal-components analysis of the configuration sample to recover *effective* dimensionality, which is expected to be well below $n$ (energy and coordination, in particular, co-vary strongly), and which may reveal that the natural axes are composite factors (a "scale" factor over $N, h, \rho_{\mathrm{inst}}$; a "complexity" factor) rather than the raw six. Reporting in the composite basis is acceptable and consistent with what Peregrine and the Seshat clustering already find.

**Reproducibility.** Every index is to be published with: its exact construction, the baseline interval and its justification, the data vintage, the normalization, the uncertainty, and code. A reference implementation is feasible with existing tools (Julia's `DifferentialEquations.jl` / `DynamicalSystems.jl`; Python's `pysindy` and standard scientific stack) and is scoped as Document/Deliverable in the program map (Document 8).

---

## 8. Reflexivity, conserved quantities, and universality — research targets, demarcated

These three ideas are central to the discipline's ambition and are frequently the points on which serious readers (especially physicists) will test it. Each is stated here as a **research target with an honest status and a way to be wrong**, not as an established result.

### 8.1 Reflexivity

Social systems are modified by knowledge of their own dynamics; a sufficiently accurate, public model becomes part of the system it models. The proposed treatment is a two-layer model — an object layer $O(t)$ (actual dynamics) and an epistemic layer $\mathcal{E}(t)$ (beliefs about those dynamics, including beliefs about predictions) — coupled by a term $\Phi(O, \mathcal{E})$ with an empirically estimable strength and lag (the symbol $\Phi$ is used to avoid collision with the rotational component $R$ of §6.1; see Document 7 §2). **Status:** this is *notation for a research program*, not a solved model — no functional form for $\Phi$ is specified and none is estimated. The analogy to quantum measurement (the observer effect formalized rather than fatal) is a *heuristic*, and the suggestion that reflexivity is a Gödel-type formal limit is **speculation, not a theorem**. The discipline's practical posture is the transparency norm (Document 1): publish predictions openly so the reflexive effect is distributed, and treat reflexivity as a measurable coupling to be characterized.

### 8.2 Conserved quantities

The charter floats candidate quasi-conservation laws (legitimacy, coercive capacity, information entropy).

> **Correction (vs. charter §3.2).** Invoking **Noether's theorem** for these is not warranted. Noether's theorem derives conservation laws from continuous symmetries of an **action functional**; Civilodynamics has no established action principle or Lagrangian, so there is presently no Noetherian route to a civilizational conservation law. These should be stated as **empirical quasi-conservation hypotheses** — e.g., "aggregate legitimacy is approximately conserved under transfer, so state-legitimacy decline predicts a measurable rise elsewhere" — each with an operational measure and a falsification condition. The Noether framing may be retained only as explicit aspiration ("were an action principle ever found, symmetries would imply conservation laws"), clearly marked as such.

### 8.3 Universality

The hypothesis is that civilizational transitions fall into a small number of **universality classes** — the same mathematical behavior near transitions across radically different societies.

> **Correction (vs. charter §3.6).** In statistical physics, a universality class is defined by renormalization-group fixed points and characterized by **critical exponents** and **data collapse**. Asserting that civilizational transitions form universality classes requires *demonstrating* such scaling, which has not been done. The honest status is a **research hypothesis with a concrete test**: near independently identified transitions in the retrodiction set, look for power-law scaling of fluctuations and for data collapse of suitably rescaled trajectories. Absence of scaling falsifies the universality hypothesis (though not the rest of the framework). Until then, "universality class" should appear only as a hypothesis under test.

---

## 9. Worked illustrative sketch: the late Western Roman Empire

The following demonstrates the apparatus on one case. **Every value below is an illustrative expert estimate, not a computed quantity**; the sketch shows *what a classification looks like*, not a result. A genuine computation is specified in §9.3.

### 9.1 Estimated configuration, Western Empire c. 350 CE

| Axis | Illustrative state | Reading |
|------|--------------------|---------|
| $E$ | $e_{\mathrm{pc}}\!\approx\!18$ GJ; EROI $\approx 6\text{–}8$ (declining); low source entropy | Modest, agrarian-slave energy base near its complexity ceiling |
| $C$ | $N\!\approx\!50$M; $h\!\approx\!7$; $r$ near natural value; high $\rho_{\mathrm{inst}}$ | Deep, well-scaffolded bureaucratic coordination |
| $I$ | $B$ moderate (literate elite, oral majority); $\lambda\!\sim$ weeks; high $V$; declining $H_I$ | Top-down imperial information; narrowing under religious unification |
| $X$ | High but declining surplus; agrarian-tributary modality; high $G$; declining $f$; rising $r_{\mathrm{rent}}$ | Latifundia consolidation; eroding fiscal capacity |
| $T$ | High $\tau_{\mathrm{inst}}$; moderate stranger trust; small regional $\rho_{\mathrm{clan}}$ | Regionally fragmenting trust topology |
| $K$ | Declining CC (soil exhaustion); $\varepsilon\!\approx\!1$; worsening climate; elevated disease | Tightening ecological envelope post-Antonine/Cyprian plagues |

### 9.2 Classification (illustrative)

These estimates place the Western Empire firmly within the **universalist-empire basin** but near several boundaries: declining $E$ and rising $r_{\mathrm{rent}}$ push toward the **agrarian-state** boundary (a smaller, less complex configuration), while declining $f$ and increasingly clan-based trust push toward the **chiefdom** boundary (severe fragmentation). The trajectory 350→500 CE reads as endogenous drift toward a boundary, repeated barbarian-incursion shocks ($\boldsymbol\eta$), and ultimately a **Type 1** cross-basin transition into a fragmented configuration resembling a chiefdom-superposition more than a coherent agrarian state. The Eastern Empire, with a different $E$/$K$ profile, remained within the universalist-empire basin for another millennium. This is a *retrodiction*, not a prediction.

### 9.3 What would make this a computation (not a sketch)

To convert §9.1–9.2 from illustration to result requires: (i) $\Omega$-coordinates for Rome and a comparison set drawn from a Seshat-compatible database with documented sources for each sub-component; (ii) $\hat V$ estimated from that sample, with the universalist-empire basin center and the relevant boundaries located (Tier 1); (iii) for the dynamical claims (drift toward boundary, transition timing), a *temporal* sequence of Roman configurations and a calibrated $\mathbf{F}$ (Tier 2). Document 6 will carry this case at whatever tier the available data support, labeled accordingly.

---

## 10. What this framework does and does not claim

**It does not predict specific events.** It locates basin boundaries and estimates stability margins; it does not say which war, election, or crisis occurs, or when.

**It does not eliminate contingency.** Two societies at the same point in $\Omega$ can diverge if their shocks $\boldsymbol\eta$ differ; determinism in $\mathbf{F}$ coexists with genuine stochasticity in $\boldsymbol\eta$. (This is the formal content of the "Mule Problem": the model predicts that *a* Mule-type emergence becomes likely in sufficiently stressed states, not *which* individual fills the role.)

**It is anthropocentric in its current form.** The constraint stack assumes human cognition (Dunbar scaling), metabolism, and ecology. Generalization to non-human social systems requires an explicit theory of how the axes transform under different cognitive and metabolic substrates — a research program, not a current capability, and one to be kept clearly separate from the empirical core to avoid diluting credibility.

**Its dimensions are not independent.** Effective dimensionality is below $n$; the metric's covariance is non-trivial. Interpretation should proceed in the empirically recovered (composite) basis (§7).

**Its validation is, as of this draft, promissory.** No basin has been computed, no $\mathbf{F}$ calibrated, no CSI measured end-to-end, no retrodiction scored. The framework is a coherent, falsifiable skeleton. Calibration and validation are the work, not a footnote — and the discipline's claim to be science rests on doing them and on publishing the failures alongside the successes.

---

## 11. Open problems and required future work

Collected here for the milestone tracker (Document 8). Each is a concrete, checkable task.

**Mathematical / methodological.**
1. Specify the map $h$ (configuration+rate → stress readout, §1.3) functionally, and test H0 (CSI ↔ distance-to-boundary) against the retrodiction set.
2. Implement the corrected CSI thresholds ($\chi^2_p$ / Hotelling $F$, §4.4) and the per-dimension-normalized headline scalar; retire the $2\sigma/3\sigma$ language everywhere in the corpus.
3. Resolve the baseline-covariance problem per §4.1 (default: coverage-restricted baseline + modern-era epistemic extension); document the choice in Documents 4 and 5.
4. Pre-register the interaction terms $\beta_1,\beta_2,\beta_3$ (§4.3) and a stated functional form for $P(\text{ASPE}\mid \textit{CSI})$ with a base rate (so absence of events costs Brier points — see Document 5).

**Empirical / data.**
5. Build the ECI measurement infrastructure (§5): a standing factual-consensus battery and survey, MOS/NCI pipelines, and the best feasible backward reconstruction. **Highest-priority investment.** (The factual-consensus battery is specified and pre-registered in **Document 9**.)
6. Assemble a Seshat-compatible configuration database with full six-axis coverage, prioritizing the under-served information ($I$) and trust ($T$) axes; compute $\Omega$-coordinates and test the sparse-clustered-occupancy prediction (§2.3, Tier 1).
7. Assemble *longitudinal* per-polity trajectories for the retrodiction cases to enable Tier-2 dynamics.

**Computational.**
8. Reference implementation: $\hat V$ and basin structure from input data; the three CSI constructions with uncertainty; diagnostic outputs for arbitrary state vectors (scoped in Document 8).
9. Pilot $\mathbf{F}$-reconstruction (SINDy / Koopman / neural ODE) on the richest available trajectory; report honestly whether the data support it yet.

**Theoretical (lower urgency, higher reward).**
10. Reflexivity: propose and pilot-estimate a functional form for the coupling $\Phi(O,\mathcal E)$ (§8.1).
11. Conserved quantities: operationalize and test the legitimacy-transfer hypothesis (§8.2).
12. Universality: test for scaling/data-collapse near transitions (§8.3).

**Statistical hygiene (continuous).**
13. Multivariate-normality tests with empirical-distribution fallbacks (§4.4, §7).
14. PCA for effective dimensionality and a decision on the reporting basis (§7).

---

*Working draft. Cite with caution. All metrics, equations, and thresholds are subject to revision as the empirical and computational program proceeds. This document is the dependency for Documents 1 and 3–8 of the Civilodynamics corpus; changes here propagate forward and must be reconciled in those documents.*
