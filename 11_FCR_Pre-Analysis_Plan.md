# Civilodynamics — Factual Consensus Rate: Pre-Analysis Plan

**Building-Phase Document 11 · Pre-Analysis Plan v1.0 (to be frozen for fielding) · June 2026**
**Stage-1 deliverable of Document 9 §11 · Satchel Hamilton · Civilodynamics Initiative**

> **Status and role.** This is the **analysis** half of the FCR Stage-1 deliverable (Document 9 §11; the instrument half is **Document 10**, the item bank). It expands the pre-registration skeleton of Document 9 §8 into a registry-grade pre-analysis plan (PAP): every construct, decision rule, sampling and power assumption, exclusion, and hypothesis is fixed **before any wave is fielded**, so the FCR series cannot be tuned after the data arrive. This is the Document 6 §5.2 discipline applied to a forward survey instead of a retrodiction.
>
> **Freeze and registration.** This PAP is frozen jointly with the instrument (Document 10 ≥ v1.1, post-adjudication and pretest), hashed (§11), and deposited to a public registry (OSF and/or AsPredicted) with a timestamp, in keeping with Stage C0 of Document 8 (establish priority cheaply, no overclaiming). Until it is frozen it is a **draft**; until waves are fielded there are **no results**, and every illustrative figure here is **estimated** (Document 4 §1; Document 7 §5).

---

## 0. Administrative

- **Instrument:** the Factual Consensus Rate (FCR), Document 9; anchor-core item bank, Document 10.
- **Design type:** repeated cross-sectional rolling tracker; quarterly cadence; two randomized response arms.
- **Primary unit of analysis:** the cross-group gap on anchor-core items, aggregated to a wave-level scalar.
- **Confirmatory vs. exploratory:** §7 designates three **confirmatory** hypotheses (H-FCR1–3); everything else (partition sensitivities, domain breakdowns, item-level analyses) is **exploratory** and labeled as such in any output.
- **What freezing locks:** the constructs (§2), design (§3), sampling/power targets (§4), decision rules (§6), confirmatory hypotheses and their falsifiers (§7), and inference rules (§8). Post-freeze changes follow the amendment protocol (§12).

---

## 1. Objectives

To produce a reproducible, forward time series measuring the **shared factual commons** across population subgroups (Document 9 §1; Charter §5), decomposed into **believed** versus **expressive** divergence (Document 9 §4), and to feed the resulting series into the ECI and the epistemic stress block $\sigma_{\mathrm{epi}}$ (Document 4 §5) — thereby making Document 5's Prediction 2 resolvable. Background, rationale, and the construct's place in the discipline are in Document 9; not repeated here.

---

## 2. Constructs and estimands

Notation and definitions are canonical from Document 9 §2; restated as estimands.

- **Per-item, per-group correct rate** $c_{g,k}(t)$; **cross-group gap** $\Delta_k(t)=\max_{\text{pairs}}|c_{A,k}-c_{B,k}|$ (max pairwise; mean pairwise as sensitivity).
- **Primary estimand — incentivized-arm continuous FCR:** $\textit{FCR}_c^{a}(t) = 1 - \overline{\Delta}^{a}(t)$ over the anchor core $\mathcal{A}$. This is the value fed into the ECI (Document 9 §2.4) and the headline series. *Rationale for primacy:* the incentivized arm is the closest available estimate of genuine cross-group belief divergence (Document 9 §4).
- **Secondary estimands:** belief-arm $\textit{FCR}_c^{b}(t)$; threshold forms $\textit{FCR}_\theta^{a,b}(t)$; the **expressive component** $\textit{XP}(t)=\textit{FCR}_c^{a}-\textit{FCR}_c^{b}$; the **knowledge level** $\textit{ACC}(t)$ (companion only, never folded into FCR — Document 9 §5.2); the **uncertainty rate** (share choosing "not sure").
- **Anchor noise floor** $\overline{\Delta}_{\text{anchor}}(t)$: the mean gap over Table A (Document 10), the comparison baseline for "real" divergence.

---

## 3. Design

- **Two arms (between-subjects, randomized within subgroup to preserve balance):** a **belief arm** ($b$, conventional items) and an **accuracy-incentivized arm** ($a$, small per-correct payments). Randomization is 1:1 with allocation concealed from respondents (Document 9 §4).
- **Wave structure:** each quarterly wave fields the full **anchor core** (Document 10, fixed) plus a **rotating pool** (per-wave, embargoed). Only the anchor core enters the headline series; the rotating pool is reported as a separate non-longitudinal panel.
- **Default partition:** partisan (two groups $A$, $B$); pre-specified alternative partitions (education, age cohort, urban/rural, self-reported media diet) are exploratory sensitivities (§7.4, Document 9 §6.3).
- **Live-series items** are wave-adjudicated with a dead-band per Document 10 §7.

---

## 4. Sampling and power

### 4.1 Frame, mode, weighting

Probability-based panel (address-based recruitment), self-administered online with offline accommodation in the recruited frame (Document 9 §6.1). Survey weights to population benchmarks (age, sex, education, region, race/ethnicity, and party where benchmarks permit). Design-based standard errors throughout (§8).

### 4.2 Targets (estimated; to be confirmed by the pilot)

| Quantity | Design target |
|----------|---------------|
| Completes per wave | 2,500–3,500 |
| Arms | 1:1 split (belief / incentivized) |
| Per-arm, per-partisan-subgroup cell | ~500–900 |
| Anchor-core size $|\mathcal{A}|$ | ~30–40 (Document 10) |
| Cadence | quarterly |

### 4.3 Power (illustrative; estimated)

Approximate, assuming proportions near 0.5 (the conservative maximum-variance case) and a modest design effect:

- **Single-item correct rate** $c_{g,k}$: SE ≈ ±2.0 pts at $n\approx600$.
- **Single-item gap** $\Delta_k$ (difference of two group proportions): SE ≈ ±2.9 pts.
- **Wave-level $\textit{FCR}_c$** (mean over ~30 correlated item gaps): SE ≈ ±1.0–1.5 pts after design and item-correlation inflation.
- **Expressive component $\textit{XP}$** (difference of two independent split-sample $\textit{FCR}_c$): SE ≈ ±1.7 pts → **MDE ≈ 4 pts at 80% power**.
- **Linear trend** over 8 quarterly waves (~2 yr) at per-wave SE ≈ ±1.2 pts → detectable slope ≈ **0.3–0.5 pt/quarter** (≈ 1.2–2.0 pts/yr).

These are planning figures only; the **pilot wave** (Document 9 §11 stage 2) replaces the assumed variances and design effect with measured ones and re-derives the targets before freeze.

---

## 5. Variables and measurement pipeline

1. Code each response correct / incorrect / "not sure" against the frozen key (Document 10 §2, §7).
2. Estimate weighted $c_{g,k}$ per arm with design-based SEs.
3. Form $\Delta_k$ → $\textit{FCR}_c$, $\textit{FCR}_\theta$ per arm; $\textit{XP}$; $\textit{ACC}$; uncertainty rate; anchor noise floor.
4. Propagate sampling uncertainty to a band on every reported value (Document 4 §1).
5. Normalize for the ECI (modern-era extension, internal early-wave reference window; Document 9 §7) and supply $\sigma_{\mathrm{epi}}$ (Document 4 §5).

---

## 6. Pre-specified decision rules

Fixed at freeze; no post-hoc adjustment.

- **Gap statistic:** maximum pairwise (mean pairwise = sensitivity).
- **Primary FCR:** $\textit{FCR}_c^{a}$ (continuous, incentivized).
- **Consensus threshold $\theta$** (for $\textit{FCR}_\theta$): a single value fixed at freeze (target $\theta = 0.10$, i.e., a sub-10-point gap counts as agreement), with $\textit{FCR}_\theta$ also reported as a curve over $\theta\in[0.05,0.25]$ for transparency. $\theta$ is re-anchored once, after the pilot, to the measured anchor noise floor, then locked.
- **Dead-band** for live-series direction coding (Document 10 §7): a 12-month change within ±0.2 standard deviations of the series' recent volatility is coded "about the same"; the exact band per series is tabled at freeze.
- **"Not sure":** excluded from the correctness denominator; tracked as uncertainty rate (Document 9 §5.1). Guessing correction reported as sensitivity.
- **Respondent exclusions (data quality):** fail of ≥1 embedded attention check; completion time below a pre-set speeding threshold (e.g., < 1/3 median); straightlining across a screen; duplicate/fraud flags from the panel provider. Exclusion rules are applied **before** any FCR computation and the excluded share is reported.
- **Missing data:** item-level missingness handled by available-case analysis with weights; wave reported only if completes and cell sizes meet §4.2 minima.
- **Multiple comparisons:** the three confirmatory hypotheses (§7) are tested as a pre-specified primary family with Holm correction at family-wise $\alpha=0.05$; all domain/item/partition breakdowns are exploratory and reported without confirmatory claims.

---

## 7. Hypotheses, tests, and falsifiers

Three **confirmatory** hypotheses (extending Document 9 §8), each with a test and a way to be wrong, plus pre-specified exploratory analyses.

### 7.1 H-FCR1 — phase-separation signature *(confirmatory)*
*Statement:* cross-group gaps are concentrated in charged-but-settled items (Table B) and near the noise floor on neutral anchors (Table A).
*Test:* mean charged-item gap $\overline{\Delta}_{\text{charged}}^{a}$ exceeds the anchor noise floor $\overline{\Delta}_{\text{anchor}}^{a}$ (one-sided; design-based test).
*Decision:* support if the difference is positive and significant after Holm correction.
*Falsifier:* if anchor gaps are comparable to charged gaps, the apparent divergence is measurement noise/inattention, not epistemic separation — the instrument is the story, not the population.

### 7.2 H-FCR2 — believed vs. expressive *(confirmatory)*
*Statement:* incentives compress gaps ($\textit{XP}>0$, material), **and** a residual believed gap remains (the incentivized-arm charged gap still exceeds the anchor floor).
*Test:* (a) $\textit{XP}>0$ at the §4.3 MDE; (b) $\overline{\Delta}_{\text{charged}}^{a} > \overline{\Delta}_{\text{anchor}}^{a}$ (the H-FCR1 inequality, in the incentivized arm).
*Decision:* support requires **both** (a) and (b).
*Falsifier:* if incentivized charged gaps collapse to the anchor floor, the divergence is *entirely expressive* — epistemic phase separation as a **belief** phenomenon is not supported. This narrows the discipline's information-layer claim from "divergent beliefs" to "divergent expression," and is a major, publishable negative result (Document 9 §8).

### 7.3 H-FCR3 — trend *(confirmatory; activates once ≥ 6 waves exist)*
*Statement:* the primary FCR declines over the tracking window.
*Test:* sign and significance of the linear slope of $\textit{FCR}_c^{a}(t)$ over the available waves (§4.3 MDE).
*Constraint:* forward-only; **no backcasting** (Document 9 §7).
*Decision/Falsifier:* a significant negative slope supports the secular-degradation reading and bears on Document 5 Prediction 2; a flat or positive slope bears **against** them and is reported as such.

### 7.4 Pre-specified exploratory analyses
Partition sensitivity (education, age, urban/rural, media diet; Document 9 §6.3); per-domain gap decomposition; the **per-wave directional-balance audit** (Document 10 §5) recorded with every release; mode/weighting robustness; the relationship between FCR and the other ECI components (MOS, NCI) as a convergent-validity check (Document 9 §12). All labeled exploratory.

---

## 8. Inference

- **Estimation:** weighted, design-based point estimates with SEs from the panel's replicate weights (or a survey bootstrap where replicate weights are unavailable).
- **Uncertainty:** every reported scalar carries a band; bands propagate to the ECI and $\sigma_{\mathrm{epi}}$.
- **Framework:** frequentist primary (Holm-corrected family, §6); a Bayesian posterior on $\textit{FCR}_c^{a}$ and its trend is reported as a pre-specified complement, with weakly-informative priors stated at freeze.
- **"Support" thresholds:** confirmatory claims require post-correction significance and an effect at least at the §4.3 MDE; sub-MDE effects are reported as inconclusive, not as null.

---

## 9. Quality control and data integrity

- **Attention checks** embedded each wave; the neutral anchors (Table A) double as an inattention monitor — an elevated anchor noise floor halts reporting pending investigation (Document 9 §3.1).
- **Fraud/bot screening** via the panel provider plus internal duplicate and speeding checks (§6).
- **Incentivized-arm payment protocol:** small, pre-disclosed per-correct payments; payment logic concealed at response time; the schedule is fixed at freeze and reported. The arm is for *measurement*, not persuasion — no feedback on correctness is given during the survey.
- **Noise-floor gate:** a wave is reportable only if the anchor floor is below a pre-set ceiling (fixed after pilot).

---

## 10. Reflexivity and ethics

- **IRB/consent:** standard informed consent; the instrument poses minimal risk; incentives are nominal.
- **Reflexivity (Document 2 §8.1):** publishing an FCR is itself an intervention in the epistemic environment it measures — it can become a Goodhart target or a corrective common-knowledge signal. Mitigations: the **dark rotating subset** (Document 10 §9) as an un-coachable tripwire; the transparency norm of Charter §10.
- **Two-sided publication commitment:** results are published whether or not they support the phase-separation hypothesis, with the anchor bank, ground-truth sources, code, and de-identified microdata released (Document 4 §9). The purely-expressive (H-FCR2 falsified) and no-signature (H-FCR1 falsified) outcomes are reported as such. This is non-negotiable (Document 6 §5; Charter §10).

---

## 11. Reproducibility

- **Frozen instrument hash:** the Document 10 bank (≥ v1.1) is hashed at freeze; the PAP records the hash; index versions tie to instrument versions (Document 4 §9).
- **Open code** regenerates every scalar from de-identified microdata.
- **Frozen inputs** for live-series keys (provider, series, vintage, retrieval date) archived per wave.
- **Registry deposit:** this PAP + the instrument hash are time-stamped on a public registry before the first reportable wave.

---

## 12. Amendment and deviation protocol

Any change after freeze is a **timestamped amendment** appended to the registry record, stating what changed, when, and why, and whether it affects confirmatory or exploratory analyses. Confirmatory hypotheses and their falsifiers are not revised mid-stream; if circumstances force a change, the affected analysis is demoted to exploratory and a new confirmatory test is registered prospectively. Deviations discovered at analysis are disclosed in every output (Document 6 §5 discipline).

---

## 13. Timeline and "done" definitions

| Step | Done when |
|------|-----------|
| Bank adjudication + cognitive pretest | Panel sign-off + pretest pass (Document 10 §10) |
| Freeze + registry deposit | Instrument hash + this PAP timestamped on OSF/AsPredicted |
| Pilot wave | Variances/design effect measured; §4 targets re-derived; $\theta$ and dead-band re-anchored and locked |
| First reportable tracker wave | A published, reproducible $\textit{FCR}_c^{a}$ with band, $\textit{XP}$, $\textit{ACC}$, and the balance audit |
| Integration | FCR feeds a computed ECI and $\sigma_{\mathrm{epi}}$ (Document 4 §5; Document 9 §7) |

This completes Document 9 §11 stage 1 (frozen instrument + registered plan) and sets up stages 2–4.

---

## 14. Reconciliation tasks created by this document

- **Document 8:** Phase B1 — FCR **Stage 1** deliverable (instrument bank Document 10 + this PAP) is **drafted**; mark `[IN PROGRESS]`, freeze pending panel + pretest; note registry deposit aligns with Stage C0 (priority).
- **Document 9:** §11 stage 1's "frozen pre-analysis plan" is realized here; §8's skeleton is superseded in detail by §6–§8 of this document (Document 9 §8 remains the canonical summary).
- **Document 7 (lexicon):** add *pre-analysis plan (PAP)*, *expressive component* (if not already), *anchor noise floor*, *dead-band*, *confirmatory vs. exploratory* as methodological vocabulary.
- **Document 5:** Prediction 2 becomes resolvable once H-FCR3's series exists (≥ 6 waves) under this plan.

---

*Draft pre-analysis plan, not yet frozen. Cite with caution. All power and threshold figures are estimated planning values to be replaced by pilot measurements before freeze; no wave has been fielded and no FCR exists. Constructs: Document 9 §2. Instrument: Document 10. Integrity and release: Document 4 §1, §9. Pre-registration precedent: Document 6.*
