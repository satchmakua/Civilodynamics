# Civilodynamics — Measurement Program and Data Architecture

**Canonical Corpus, Document 4 of 8 · Working Draft v0.1 · June 2026**
**Satchel Hamilton · Civilodynamics Initiative**

> **Status and role.** This document operationalizes the abstract measures defined in **Document 2 (Mathematical & Methodological Foundations)** — it is the manual that says, for each index, exactly which variables are used, where the data come from, how far back they reach, what is broken about them, and how the index is assembled and released. It is the dependency for **Document 5** (the U.S. case study) and **Document 6** (the Retrodiction Casebook), both of which draw their numbers from the protocols specified here. It does **not** re-derive any mathematics; where construction is concerned it cites Document 2 and supplies the operational detail. It is a working draft: the protocols are specified, but with one minor exception nothing in the corpus has yet been computed against data, and all illustrative values elsewhere remain estimates.
>
> **A standing caveat on the data estate.** Every coverage window, access modality, and vintage stated below reflects the program's current understanding and **must be verified against each provider's current documentation before computation.** Several access conditions have changed materially in recent years — social-platform research access in particular — and are flagged where known.

---

## 0. What this document covers

Five measurement objects, in order of treatment:

1. **The stress readout** $\mathbf{u}(t)$ — the six fast-moving stress blocks behind the CSI (§3).
2. **The Civilizational Stress Index (CSI)** — construction protocol, with the corrected thresholds and the concrete resolution of the baseline-covariance problem (§4).
3. **The Epistemic Coherence Index (ECI)** — the discipline's distinctive and least-mature measure, treated in the most detail because it requires new infrastructure (§5).
4. **The Elite Overproduction Index (EOI)** — a worked example of a well-specified component index (§6).
5. **The structural configuration vector** $\mathbf{S}(t)$ — the six constraint axes used for morphospace work (§7).

Preceded by the measurement philosophy (§1) and the data estate (§2); followed by the consolidated infrastructure-gap list (§8) and the release protocol (§9).

---

## 1. Measurement philosophy and standing rules

These rules bind every measurement in the corpus. They are drawn from Document 2 and the charter's ethics, restated here as operational requirements.

**Estimated vs. computed.** Every reported value carries one of two labels: **computed** (produced end-to-end from disclosed data by disclosed code) or **estimated** (an expert or interpolated figure standing in for a computation not yet performed). No estimated value is reported with computed-looking precision. As of this draft, essentially every numerical value in the corpus is estimated; the program's near-term object is to convert a defined subset to computed.

**Reproducibility.** Each index is published with: (i) its exact construction; (ii) the baseline interval and an explicit defense of it; (iii) the data vintage (provider, version, access date); (iv) the normalization; (v) the uncertainty; (vi) the code. A figure lacking any of these is provisional.

**Two data tiers (from Document 2 §3).** **Tier 1** data are cross-sectional — a snapshot of many polities — and support basin *location* and *relative depth*, and the computation of a society's instantaneous stress readout. **Tier 2** data are *longitudinal* — a temporal sequence for a single polity — and are required for the flow field, transition dynamics, and the dynamical reading of distance-to-bifurcation. Tier 2 data are far sparser, and the program does not pretend otherwise.

**Pre-registration.** Index weights, interaction terms, thresholds, and the functional form of any stress-to-outcome relationship are registered before they are tested against the cases they are meant to explain. This is the primary guard against fitting the framework to its own validation set.

**Provenance and versioning.** Source data are archived at the vintage used (a frozen copy), because providers revise series retroactively. Index versions are tied to data vintages so that any published figure can be regenerated exactly.

---

## 2. The data estate

The empirical foundation has two layers: a **historical baseline layer** (deep time, lower resolution, the calibration substrate) and a **contemporary stream layer** (shallow time, high resolution, the real-time measurement substrate). The fusion of the two is the core data-engineering problem of the program.

### 2.1 Historical baseline datasets

| Dataset | Primary contribution | Approx. coverage | Notes / limitations |
|---------|----------------------|------------------|---------------------|
| Seshat Global History Databank | Cross-civilizational configuration variables; basin-location substrate | Prehistory–present | Polity-based partitioning (a unit-of-analysis choice); uneven coverage of the $I$ and $T$ axes |
| World Inequality Database (WID) | Wealth/income concentration | ~1900–present (some series earlier) | Methodology evolves; historical reconstructions carry wider uncertainty |
| Varieties of Democracy (V-Dem) | Institutional quality, legitimacy proxies | 1789–present | Expert-coded; coder variance modeled but present |
| Polity / Quality of Government | Institutional/regime structure | Modern–historical | Useful for $\rho_{\mathrm{inst}}$, regime type |
| Gallup Confidence in Institutions | Institutional trust | 1973–present | Begins at the tail of a mid-century baseline (see §4.2) |
| Pew trust / media-consumption series | Trust; pre-digital media overlap | Trust ~1958–present; media surveys biennial, multi-decade | Instrument and mode changes over time |
| General Social Survey (GSS) | Social capital, legal-fairness, attitudes | 1972–present | Biennial; no mid-century coverage |
| ANES | Affective polarization (thermometers), threat | Thermometers ~1964/1978–present | Sparse early; mode effects |
| BLS CES / OEWS | Real wages; EOI position-side inputs | CES ~1939/1947–present; OEWS ~1988–present | Occupational reclassifications (2000, 2010 SOC) create discontinuities |
| NCES / Survey of Earned Doctorates | EOI credential-side inputs | SED ~1957–present | Field classifications change over time |
| ABA enrollment/conferral data | EOI legal-domain inputs | Multi-decade | Definitional changes in reporting |
| Federal Reserve DFA | Household wealth by quantile | 1989–present | No mid-century coverage |
| MIT Election Lab / Census | Geographic sorting; demographic blocks | Elections 1976–present; Census long-run | Precinct/county boundary changes |
| UCDP / related conflict datasets | Political violence, intra-state conflict | 1946–present | Coding thresholds for "conflict" |
| Smil (2017) and biophysical-economics literature | Historical energy throughput; EROI baselines | Long-run estimates | Estimates, not measurements, for deep history |

### 2.2 Contemporary stream datasets

| Stream | Primary contribution | Access modality | Risk / limitation |
|--------|----------------------|-----------------|-------------------|
| Reuters Institute Digital News Report | Cross-partisan media overlap (MOS) | Annual public reports / microdata | Begins ~2012; self-reported consumption |
| AllSides / media-bias audience data | MOS supplement | Public / commercial | Bias ratings are themselves contestable |
| Survey panels (commercial / academic) | Factual-consensus battery (FCR) — see §5 | Commissioned | **Does not yet exist for FCR; must be built** |
| Social-platform network data | Cross-cutting tie density (NCI) | Research APIs / data-sharing programs | **Access degraded materially post-2023** (e.g., deprecation of broad academic API access on some platforms); Meta Content Library, Bluesky (open), and Reddit are current partial options |
| Computational-social-science research datasets | NCI, content similarity | Academic (e.g., Lazer, Bail labs) | Access subject to agreements; coverage uneven |
| Economic/transactional and satellite data | Real-time economic and demographic proxies | Research partnerships / commercial | Cost; access; representativeness |

> **A structural data risk worth naming.** The discipline's distinctive axis — information — depends partly on social-platform data whose research access has become less reliable. The program should not architect a core measure on a single platform's goodwill. The ECI design (§5) therefore leans hardest on the **survey-based** factual-consensus instrument, which the program can build and control directly, and treats platform-derived network measures as a valuable but supplementary component.

---

## 3. The stress readout $\mathbf{u}(t)$

The six stress blocks and their operationalized variables. (Notation follows Document 2 §1: $\sigma_{\bullet}$ are stress observables, distinct from the configuration axes; the earlier $E,D,L,C,\Psi,P$ labels map here, with the energy/economic and coordination/cohesion symbol collisions resolved.) Each variable is sign-oriented so larger values mean more stress.

| Block | Variable | Operationalization | Source | Approx. coverage |
|-------|----------|--------------------|--------|------------------|
| **Economic** $\sigma_{\mathrm{econ}}$ | Real wage growth | 5-yr rolling mean, bottom two quintiles, CPI-deflated (sign-flipped) | BLS CES; BLS CPI | ~1947– |
| | Wealth concentration | Top-1% net wealth share ÷ baseline mean | WID; Fed DFA | WID ~1913–; DFA 1989– |
| | Mobility deficit | $1-$ (observed intergen. rank corr. ÷ baseline) | Opportunity Insights | Modern cohorts |
| | Fiscal stress | Federal debt/GDP vs. baseline | IMF HPDD; CBO | Long-run |
| **Elite** $\sigma_{\mathrm{elite}}$ | Elite Overproduction Index | See §6 | ABA; NCES/SED; BLS OEWS | Mixed |
| | Elite fragmentation | Variance in elite-tier donations across parties | FEC / DIME | ~1979– |
| **Legitimacy** $\sigma_{\mathrm{leg}}$ | Institutional trust composite | Mean trust across consistently-tracked institutions (sign-flipped) | Gallup; Pew | Gallup 1973– |
| | Legal-fairness gap | Trust gap, legal system, top vs. bottom income quintile | GSS; Pew | GSS 1972– |
| **Cohesion** $\sigma_{\mathrm{coh}}$ | Geographic sorting | Population-weighted mean county partisan lean | MIT Election Lab; Census | 1976– (reconstructable earlier) |
| | Intergroup threat | Perceived economic/cultural out-group threat | ANES; Pew | Modern |
| **Epistemic** $\sigma_{\mathrm{epi}}$ | Media Overlap Score | $1-\mathrm{JSD}$ of L/R news-source distributions | Reuters DNR; AllSides | ~2012– (recon. to ~2000) |
| | Factual Consensus Rate | Cross-partisan agreement on a verifiable battery | **New survey — §5** | **To be built** |
| **Demographic** $\sigma_{\mathrm{dem}}$ | Youth cohort pressure | Pop. 18–29 ÷ working-age, normalized | Census ACS | Long-run |
| | Rural-urban divergence | Urban/rural median income ratio, normalized | Census ACS; ERS | Long-run |

This is the variable set behind all three CSI constructions. The epistemic block is the weak point: one component (MOS) is reconstructable to ~2000 but estimated before ~2012, and the other (FCR) does not yet have an instrument at all.

---

## 4. The Civilizational Stress Index — construction protocol

The mathematics is in Document 2 §4; this is the recipe. The CSI is computed in five steps.

**Step 1 — Assemble and orient.** Collect the variables of §3 at the chosen vintage; sign-orient each so larger = more stress.

**Step 2 — Choose and defend a baseline $\mathcal{B}$.** State the interval, defend it explicitly, and commit to sensitivity analysis over at least two alternatives. (Document 5's U.S. baseline of 1948–1973 is defended there, with its acknowledged limitations — that period's prosperity coexisted with racial apartheid, Cold War anxiety, and gendered exclusion — and is stress-tested against 1948–1968 and 1950–1980.)

**Step 3 — Normalize.** Convert each variable to a baseline $z$-score (Document 2 §4.1).

**Step 4 — Resolve the baseline-covariance problem concretely.** The Mahalanobis construction needs the covariance $\Sigma_{\mathcal B}$ of the stress vector *over the baseline*, but several variables have no mid-century data. Per Document 2 §4.1, the program adopts a **coverage-restricted baseline vector** plus a **modern-era epistemic extension**. Concretely, for the U.S. with $\mathcal B = 1948\text{–}1973$:

| Variable | Mid-century coverage? | Assignment |
|----------|------------------------|------------|
| Real wage growth | Yes | Baseline $\Sigma_{\mathcal B}$ |
| Wealth concentration | Yes (WID) | Baseline $\Sigma_{\mathcal B}$ |
| Fiscal stress | Yes | Baseline $\Sigma_{\mathcal B}$ |
| Youth cohort pressure | Yes (Census) | Baseline $\Sigma_{\mathcal B}$ |
| Rural-urban divergence | Yes (Census) | Baseline $\Sigma_{\mathcal B}$ |
| Geographic sorting | Partial (reconstructable) | Baseline $\Sigma_{\mathcal B}$, flagged |
| EOI (credential side) | Partial (SED from ~1957) | Baseline $\Sigma_{\mathcal B}$, flagged |
| Mobility deficit | No (modern cohorts) | Modern extension |
| Elite fragmentation | No (DIME ~1979–) | Modern extension |
| Institutional trust | Borderline (Gallup 1973) | Modern extension (anchored at baseline tail) |
| Legal-fairness gap | No (GSS 1972–) | Modern extension |
| Intergroup threat | No | Modern extension |
| Media Overlap Score | No | Modern extension |
| Factual Consensus Rate | No | Modern extension |

The baseline $\Sigma_{\mathcal B}$ is estimated only over the upper block; the modern-era variables enter through a separately reported extension with its own later reference window and explicit uncertainty. The corpus must **never** imply a full-vector mid-century covariance, because it cannot exist.

**Step 5 — Compute all three indices and report them together.**
- $\textit{CSI}_{\mathrm{lin}}$ (equal weights default; calibrated and theory-weighted variants as sensitivity).
- $\textit{CSI}_{\mathrm{nl}}$ (pre-registered interaction terms).
- $\textit{CSI}_{\mathrm{M}}$ over the coverage-restricted vector, with thresholds set from the **$\chi^2_p$ distribution** (or the finite-sample **Hotelling-$F$** when $\boldsymbol\mu_{\mathcal B},\Sigma_{\mathcal B}$ are estimated), **not** the $2\sigma/3\sigma$ rule (Document 2 §4.4). Report multivariate-normality diagnostics; if normality fails, set thresholds from the empirical baseline distribution.

**Headline scalar.** Report a **per-dimension-normalized** quantity (e.g., $\textit{CSI}_{\mathrm{M}}/\sqrt{p}$ or the mean $z$) as the headline, because it is interpretable across differing $p$ and does not invite the $\sigma$-rule misreading.

**Uncertainty and sensitivity (mandatory).** Propagate measurement uncertainty (especially from the estimated epistemic block) into a band around every trajectory; report sensitivity to baseline choice and to weighting. A CSI value without a band is incomplete.

---

## 5. The Epistemic Coherence Index — measurement specification

The ECI is the discipline's distinctive contribution and its highest-priority empirical build (charter §5). It operationalizes the information axis $I$ in $\mathbf{S}$ and supplies $\sigma_{\mathrm{epi}}$ in $\mathbf{u}$. It has three components; the second requires new infrastructure and is specified at length.

$$\textit{ECI}(t) = g\big(\textit{MOS}(t),\; \textit{FCR}(t),\; \textit{NCI}(t)\big),$$

with $g$ a normalized aggregate (equal-weight mean as default, weights pre-registered). All three components are bounded so that higher means *more* coherence; the stress observable $\sigma_{\mathrm{epi}}$ is the sign-flipped, baseline-normalized ECI.

### 5.1 Media Overlap Score (MOS)

$\textit{MOS}(t) = 1 - \mathrm{JSD}(P_A, P_B)$, the Jensen–Shannon divergence between the information-source distributions of two communities (partisan identification as the default partition), bounded $[0,1]$. **Sources:** Reuters DNR microdata and AllSides audience data from ~2012; Pew's long-run biennial media-consumption surveys for pre-digital reconstruction to ~2000 (interpolated, hence **estimated**). **Known issues:** self-reported consumption; the partition choice (partisan) is one of several defensible choices and should be sensitivity-tested.

### 5.2 Factual Consensus Rate (FCR) — the new instrument

No existing survey tracks cross-partisan agreement on *verifiable* propositions consistently over time. Building one is the single most valuable, and most feasible, near-term metrological investment in the program. The conceptual specification below is operationalized into a full fieldable instrument and pre-registration in **Document 9**. Specification:

**Object.** The fraction of a standing battery of verifiable factual propositions on which agreement holds across partisan (and other) subgroups — operationally, the share of items for which the cross-group gap in the rate of correct belief falls below a pre-registered threshold (and/or a continuous index of the mean cross-group gap).

**Item design.** Items must be **verifiable and settled**, not values or contested interpretation. The battery mixes:
- *Neutral anchors* — uncontroversial empirical facts (basic civic, scientific, and numerical facts) that establish a baseline of measurement noise.
- *Charged-but-settled items* — empirical propositions with established ground truth that are nonetheless politically salient (e.g., directional facts about measurable economic, demographic, environmental, or epidemiological quantities, stated as checkable claims). These are where epistemic phase separation, if real, shows up.
- Items are rotated and refreshed to prevent priming and to track new factual terrain, with an anchor core held constant for longitudinal comparability.

**The expressive-responding problem (critical).** A known confound is that some respondents give partisan answers to *signal identity* rather than report belief (partisan cheerleading; Bullock and colleagues). An FCR that mistakes expressive responding for genuine factual divergence would overstate epistemic fragmentation. **Mitigation:** include an **incentivized-accuracy** arm (small payments for correct answers, which compress apparent partisan gaps and isolate genuine belief divergence from expressive signaling), and report the FCR both with and without incentives. The gap between the two is itself an informative measure of how much of the divergence is expressive versus believed.

**Method.** Nationally representative panel; quarterly cadence (a rolling tracker); pre-registered analysis. Feasible at modest cost via an established survey house or a probability-based online panel; the anchor-core design keeps marginal cost low once established.

**Honesty about coverage.** FCR begins when the instrument is fielded; it has no historical values. Pre-instrument FCR is not reported as data. (This is a primary reason the epistemic block sits in the modern-era extension of §4.)

### 5.3 Network Connectivity Index (NCI)

$\textit{NCI}(t) = E_{\mathrm{cross}} / (E_{\mathrm{cross}} + E_{\mathrm{within}})$ — the share of cross-community ties in information-sharing networks, with community structure detected via modularity; $0.5$ balanced, $\to 0$ hermetic. **Sources:** social-platform research data where available (with the access caveats of §2.2 — the program treats this as supplementary, not load-bearing) and academic computational-social-science datasets. **Known issues:** platform-specific; access instability post-2023; sampling and bot contamination.

### 5.4 ECI build sequence

In order: (1) field the FCR instrument (highest priority, fully under program control); (2) build the MOS pipeline from existing sources with documented reconstruction; (3) add NCI from whatever platform/academic data are reliably accessible. Publish the construction as a candidate **field standard** with reproducible code, so others can adopt and critique it.

---

## 6. The Elite Overproduction Index — measurement specification

A worked example of a fully specified component index. The EOI is the ratio of credentialed elite aspirants to available elite positions, aggregated across domains.

**Per-domain ratios** (numerator = credential supply; denominator = position availability):

| Domain | Numerator | Denominator | Source |
|--------|-----------|-------------|--------|
| Law | JD conferrals / 1L enrollment | Lawyer openings (projected + JOLTS) | ABA; BLS OEWS |
| Academia | PhD conferrals by field | Tenure-track openings | NCES/SED; AHA & MLA jobs reports |
| Finance | Relevant graduate conferrals | Finance/analyst positions | NCES; BLS OEWS |
| Management | MBA conferrals | Management openings | NCES; BLS OEWS |
| Media | Journalism/comms degrees | Newsroom employment | NCES; Pew newsroom-employment data |

**Aggregation.** Normalize each domain ratio to its baseline, then aggregate (geometric mean of normalized domain ratios, to avoid one domain dominating), producing a single baseline-relative EOI.

**Known issues, stated.** BLS occupational classification revisions (2000 and 2010 SOC) create discontinuities in the denominators that must be bridged explicitly. Degree-field taxonomies in NCES/SED also change. Until a purpose-built protocol harmonizes these, the EOI is **estimated**, not computed. A dedicated EOI protocol — harmonized occupational and degree classifications, with a documented bridging method — is a defined task in the program (Document 8, and Document 2 §11.6).

---

## 7. The structural configuration vector $\mathbf{S}(t)$

For morphospace work (basin location and depth, Tier 1), the six constraint axes are operationalized as in Document 2 §2, with sources and coverage:

| Axis | Sub-components | Principal sources | Coverage / gap |
|------|----------------|-------------------|----------------|
| **Energy** $E$ | $e_{\mathrm{pc}}$, EROI, $H_E$ | Smil (2017); biophysical-economics (Hall et al.); IEA for modern | Deep-history values are estimates |
| **Coordination** $C$ | $N$, $h$, $r$, $\rho_{\mathrm{inst}}$ | Seshat; V-Dem/Polity/QoG; Dunbar/Zhou literature for $r$ | $h$ and $\rho_{\mathrm{inst}}$ require coding conventions |
| **Information** $I$ | $B$, $\lambda$, $V$, $H_I$ | Media-history literature; ECI components for modern | **Under-served historically — priority gap** |
| **Extraction** $X$ | $s$, $\boldsymbol\mu$, $G$, $f$, $r_{\mathrm{rent}}$ | WID; fiscal-history (fiscal capacity ~1500 CE+); political-economy literature | $r_{\mathrm{rent}}$ needs a stable operational definition |
| **Trust** $T$ | $\tau_{\mathrm{inst}}$, $\tau_{\mathrm{str}}$, $\rho_{\mathrm{clan}}$, $c$ | WVS, Edelman (modern); historical proxies (credit-based long-distance trade, compliance rates) | **Under-served historically — priority gap** |
| **Ecology** $K$ | CC, $\varepsilon$, $D_{\mathrm{clim}}$, $D_{\mathrm{dis}}$ | Paleoclimate, agronomic, epidemiological-history literatures | Deep-history values are estimates |

The two priority gaps — the information ($I$) and trust ($T$) axes in deep history — are exactly the dimensions on which Civilodynamics' distinctiveness rests, and closing them is a defined data task (Document 2 §11.6; Document 8). The configuration measurement supports Tier-1 work (locate basins, test the sparse-clustered-occupancy prediction). Tier-2 dynamical reconstruction additionally requires *longitudinal* per-polity sequences (§1, Document 2 §3).

---

## 8. Data gaps and required infrastructure (prioritized)

Consolidated for the milestone tracker (Document 8).

1. **FCR survey instrument** (§5.2) — highest priority; fully under program control; feasible at modest cost; can begin on paper now. **Specified and pre-registered in Document 9.**
2. **MOS pipeline** (§5.1) from existing sources, with documented historical reconstruction.
3. **Configuration database** with full six-axis coverage (§7), prioritizing the under-served $I$ and $T$ axes; computes $\Omega$-coordinates and tests the morphospace occupancy prediction (Tier 1).
4. **Longitudinal trajectories** for the retrodiction cases (Document 6) to enable Tier-2 dynamics.
5. **Purpose-built EOI protocol** (§6) harmonizing occupational and degree classifications across the 2000/2010 reclassifications.
6. **NCI data strategy** (§5.3) robust to single-platform access risk.
7. **Provenance/versioning infrastructure** (§1): frozen data snapshots tied to index versions, enabling exact regeneration.

---

## 9. Reproducibility and release protocol

Every published index follows the same release discipline:

- **Frozen inputs.** A snapshot of each source at the vintage used is archived; the release names provider, version, and access date.
- **Open construction.** The exact recipe (variables, baseline + defense, normalization, weights/thresholds, aggregation) is published.
- **Open code.** Code that regenerates the figure from the frozen inputs is released (the reference implementation is scoped in Document 8; Document 2 §7 names the tooling).
- **Uncertainty and sensitivity.** Every value ships with a band and with baseline/weight sensitivity.
- **Estimated/computed labels.** Each value is labeled per §1; pre-instrument and interpolated values are never presented as measured.
- **Versioning.** Index versions are tied to data vintages so any published figure can be reproduced exactly.

This discipline is not bureaucratic overhead; it is the operational form of the claim that Civilodynamics is a science. An index that cannot be regenerated from disclosed inputs by disclosed code is, by the standards of this document, not yet a result.

---

*Working draft. Cite with caution. All variables, sources, coverage windows, and protocols are subject to revision and to verification against current provider documentation before computation. This document operationalizes Document 2 and supplies the numbers-side protocols for Documents 5 and 6.*
