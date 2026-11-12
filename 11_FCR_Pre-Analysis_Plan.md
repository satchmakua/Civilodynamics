# Civilodynamics — Factual Consensus Rate: Pre-Analysis Plan

**Building-Phase Document 11 · Pre-Analysis Plan v1.0, draft 2 (to be frozen for fielding) · June 2026, revised November 2026**
**Stage-1 deliverable of Document 9 §11 · Satchel Hamilton · Civilodynamics Initiative**

> **Status and role.** This is the **analysis** half of the FCR Stage-1 deliverable (Document 9 §11; the instrument half is **Document 10**, the item bank; the procedures that take both to freeze are **Document 12**). It expands the pre-registration skeleton of Document 9 §8 into a registry-grade pre-analysis plan (PAP): every construct, decision rule, sampling and power assumption, exclusion, and hypothesis is fixed **before any wave is fielded**, so the FCR series cannot be tuned after the data arrive. This is the Document 6 §5.2 discipline applied to a forward survey instead of a retrodiction.
>
> **Freeze and registration.** This PAP is frozen jointly with the instrument (Document 10, v1.1 or later, post-adjudication and pretest), hashed (§11), and deposited to a public registry (OSF and/or AsPredicted) with a timestamp, in keeping with Stage C0 of Document 8 (establish priority cheaply, no overclaiming). Until it is frozen it is a **draft**; until waves are fielded there are **no results**, and every illustrative figure here is **estimated** (Document 4 §1; Document 7 §5).
>
> **Revised November 2026, before freeze.** Draft 2 carries through the corrections made to Document 9 (the statistic is computed over the charged core with a noise-corrected gap; balance has an empirical test; the claim about Document 5's Prediction 2 is withdrawn) and closes gaps of its own: it defines the two groups, separates the pilot from confirmatory analysis, and guards the arm comparison against differential exclusion. Changes are logged in §15.

---

## 0. Administrative

- **Instrument:** the Factual Consensus Rate (FCR), Document 9; anchor-core item bank, Document 10.
- **Design type:** repeated cross-sectional rolling tracker; quarterly cadence; two randomized response arms.
- **Primary unit of analysis:** the cross-group gap on charged-core items, aggregated to a wave-level scalar.
- **Confirmatory vs. exploratory:** §7 designates three **confirmatory** hypotheses (H-FCR1–3); everything else (partition sensitivities, domain breakdowns, item-level analyses) is **exploratory** and labeled as such in any output.
- **The pilot is a design sample, not evidence.** The pilot wave is used to select, recode, and calibrate (cut codes, anchors, $\theta$, dead-bands, variances). Because those choices are made on it, pilot data never enter a confirmatory test; confirmatory tests use tracker waves only.
- **What freezing locks:** the constructs (§2), design (§3), sampling/power targets (§4), decision rules (§6), confirmatory hypotheses and their falsifiers (§7), and inference rules (§8). Post-freeze changes follow the amendment protocol (§12).

---

## 1. Objectives

To produce a reproducible, forward time series measuring the **shared factual commons** across population subgroups (Document 9 §1; Charter §5), decomposed into **believed** versus **expressive** divergence (Document 9 §4), and to feed the resulting series into the ECI and the epistemic stress block $\sigma_{\mathrm{epi}}$ (Document 4 §5). Background, rationale, and the construct's place in the discipline are in Document 9; not repeated here.

---

## 2. Constructs and estimands

Notation and definitions are canonical from Document 9 §2; restated as estimands.

- **Item sets.** The anchor core is $\mathcal{A} = \mathcal{A}_0 \cup \mathcal{K}$: the neutral anchors $\mathcal{A}_0$ (Document 10, Table A) and the charged core $\mathcal{K}$ (Table B). $\mathcal{K}_{\mathrm{f}} \subset \mathcal{K}$ is the charged core less the swing items.
- **Per-item quantities.** Per-group correct rate $c_{g,k}(t)$; signed gap $\delta_k = c_{A,k} - c_{B,k}$ with sampling variance $v_k$; absolute gap $\Delta_k = |\delta_k|$.
- **Gap summary.** For an item set $\mathcal{S}$, the noise-corrected root-mean-square gap $\overline{\Delta}_{\mathcal{S}} = \sqrt{\max\{0,\ |\mathcal{S}|^{-1}\sum_{k\in\mathcal{S}}(\hat\delta_k^{\,2}-\hat v_k)\}}$ (Document 9 §2.2).
- **Primary estimand — incentivized-arm continuous FCR:** $\textit{FCR}_c^{a}(t) = 1 - \overline{\Delta}_{\mathcal{K}}^{a}(t)$, over the charged core. This is the value fed into the ECI (Document 9 §2.4) and the headline series. *Rationale for primacy:* the incentivized arm is the closest available estimate of genuine cross-group belief divergence (Document 9 §4).
- **Secondary estimands:** belief-arm $\textit{FCR}_c^{b}(t)$; threshold forms $\textit{FCR}_\theta^{a,b}(t)$; the **expressive component** $\textit{XP}(t)=\textit{FCR}_c^{a}-\textit{FCR}_c^{b}$; the **knowledge level** $\textit{ACC}(t)$ (companion only, pooled across groups, never folded into FCR — Document 9 §5.2); the **uncertainty rate** (share choosing "not sure").
- **Anchor noise floor** $\overline{\Delta}_{\mathcal{A}_0}(t)$: the same gap summary over the neutral anchors, the comparison baseline for "real" divergence.
- **Balance statistic** $\bar\delta(t)$: the signed mean gap over $\mathcal{K}_{\mathrm{f}}$ (Document 9 §3.3). A design check, not a finding.

---

## 3. Design

- **Two arms (between-subjects, randomized within subgroup to preserve balance):** a **belief arm** ($b$, conventional items) and an **accuracy-incentivized arm** ($a$, small per-correct payments). Randomization is 1:1 with allocation concealed from respondents (Document 9 §4).
- **Wave structure:** each quarterly wave fields the full **anchor core** (Document 10, fixed) to every respondent, plus a **rotating pool** (per-wave, embargoed). Only the anchor core enters the headline series; the rotating pool is reported as a separate non-longitudinal panel.
- **Length.** The anchor core is 46 items in draft 2. To hold median completion time near fifteen minutes, the rotating pool is **matrix-sampled** — each respondent sees a random subset — rather than asked in full.
- **Order.** Item order is randomized per respondent, with neutral anchors and charged items interleaved; option order is randomized where the options have no natural order.
- **The two groups.** $A$ and $B$ are the identifiers of the two major parties, *including* independents who lean toward one. Independents who lean toward neither are excluded from the two-group gap and reported separately. Self-identification can shift between waves, so the composition of the groups is monitored (§7.4).
- **Other partitions** (education, age cohort, urban/rural, self-reported media diet) are pre-specified exploratory sensitivities (§7.4, Document 9 §6.3).
- **Live and wave-set items** are adjudicated each wave with a dead-band per Document 10 §7.

---

## 4. Sampling and power

### 4.1 Frame, mode, weighting

Probability-based panel (address-based recruitment), self-administered online with offline accommodation in the recruited frame (Document 9 §6.1). Survey weights to population benchmarks (age, sex, education, region, race/ethnicity). Party identification defines the groups and is not a weighting target unless a high-quality benchmark is named at freeze. Design-based standard errors throughout (§8).

### 4.2 Targets (estimated; to be confirmed by the pilot)

| Quantity | Design target |
|----------|---------------|
| Completes per wave | 2,500–3,500 |
| Arms | 1:1 split (belief / incentivized) |
| Per-arm, per-partisan-subgroup cell | ~500–900, held as constant as practicable across waves |
| Charged core $\lvert\mathcal{K}\rvert$ | 30 in draft 2 (Document 10, Table B) |
| Neutral anchors $\lvert\mathcal{A}_0\rvert$ | 16 in draft 2 (Document 10, Table A) |
| Cadence | quarterly |

### 4.3 Power (illustrative; estimated)

Approximate, assuming proportions near 0.5 (the conservative maximum-variance case), a modest design effect, and independent cross-sections:

- **Single-item correct rate** $c_{g,k}$: SE ≈ ±2.0 pts at a cell of about 600.
- **Single-item signed gap** $\delta_k$ (difference of two group proportions): SE ≈ ±2.9 pts.
- **Wave-level $\textit{FCR}_c$** (noise-corrected gap over 30 correlated items): SE ≈ ±1.0–1.5 pts after design and item-correlation inflation.
- **Expressive component $\textit{XP}$** (difference of two independent split-sample $\textit{FCR}_c$): SE ≈ ±1.7 pts → **minimum detectable effect ≈ 4 pts at 80% power**.
- **Linear trend** over 8 quarterly waves (~2 yr) at per-wave SE ≈ ±1.2 pts → slope SE ≈ 0.19 pt/quarter → detectable slope ≈ **0.5 pt/quarter** (≈ 2 pts/yr) at 80% power.

These are planning figures only; the **pilot wave** (Document 9 §11 stage 2) replaces the assumed variances and design effect with measured ones, and a simulation of the noise-corrected estimator at the measured cell sizes (Document 9 §12, item 6) re-derives the targets before freeze.

---

## 5. Variables and measurement pipeline

1. Code each response correct / incorrect / "not sure" against the wave's adjudicated key (Document 10 §2, §7).
2. Estimate weighted $c_{g,k}$ per arm with design-based variances.
3. Form $\hat\delta_k$ and $\hat v_k$; from them the noise-corrected gaps over $\mathcal{K}$ and over $\mathcal{A}_0$; then $\textit{FCR}_c$ and $\textit{FCR}_\theta$ per arm, $\textit{XP}$, $\textit{ACC}$, the uncertainty rate, and the balance statistic $\bar\delta$.
4. Propagate sampling uncertainty to a band on every reported value (Document 4 §1).
5. Normalize for the ECI (modern-era extension, internal early-wave reference window; Document 9 §7) and supply $\sigma_{\mathrm{epi}}$ (Document 4 §5).

---

## 6. Pre-specified decision rules

Fixed at freeze; no post-hoc adjustment.

- **Gap statistic:** the noise-corrected root-mean-square gap of §2, on the two-group partition.
- **Primary FCR:** $\textit{FCR}_c^{a}$ (continuous, incentivized, charged core).
- **Consensus threshold $\theta$** (for $\textit{FCR}_\theta$): a single value fixed at freeze (target $\theta = 0.10$, i.e., a sub-10-point gap counts as agreement), with $\textit{FCR}_\theta$ also reported as a curve over $\theta\in[0.05,0.25]$ for transparency. $\theta$ is re-anchored once, after the pilot, to sit above the measured anchor noise floor, then locked.
- **Balance tolerance:** $|\bar\delta| \le 0.03$ in the incentivized arm (design target, re-derived from the pilot and locked at freeze). A wave outside tolerance is rebalanced by rotating-pool substitution before any FCR is reported, and the rebalancing is disclosed.
- **Cut-code validation (pilot):** a cut code stands only if the sign of the pilot's $\hat\delta_k$ matches it at the pilot's stated confidence level; an item whose gap is indistinguishable from zero is recoded cross-partisan; an item with the opposite sign is recoded accordingly. The ledger of Document 10 §5 is then recomputed.
- **Difficulty match:** the neutral anchors must overlap the charged items in measured correct rate. H-FCR1 is tested within difficulty strata fixed at freeze from pilot correct rates.
- **Dead-band** for live and wave-set direction coding (Document 10 §7): a 12-month change within ±0.2 standard deviations of the series' recent volatility is coded "about the same"; the exact band per series is tabled at freeze.
- **"Not sure":** excluded from the correctness denominator; tracked as uncertainty rate (Document 9 §5.1). Guessing correction reported as sensitivity.
- **Respondent exclusions (data quality):** failing one or more *dedicated* attention checks; completion time below a pre-set speeding threshold (e.g., under one-third of the median); straightlining across a screen; duplicate or fraud flags from the panel provider. Exclusion rules are applied **before** any FCR computation and the excluded share is reported **by arm**. Neutral anchors are never an exclusion criterion: screening on them would bias the noise floor they exist to measure.
- **Missing data:** item-level missingness handled by available-case analysis with weights; a wave is reported only if completes and cell sizes meet the §4.2 minima.
- **Multiple comparisons:** the three confirmatory hypotheses (§7) are tested as a pre-specified primary family with Holm correction at family-wise $\alpha=0.05$; all domain/item/partition breakdowns are exploratory and reported without confirmatory claims.

---

## 7. Hypotheses, tests, and falsifiers

Three **confirmatory** hypotheses (extending Document 9 §8), each with a test and a way to be wrong, plus pre-specified exploratory analyses. All confirmatory tests use tracker waves, never the pilot (§0).

### 7.1 H-FCR1 — phase-separation signature *(confirmatory)*
*Statement:* cross-group gaps are concentrated in the charged core (Table B) and near zero on neutral anchors of comparable difficulty (Table A).
*Test:* $\overline{\Delta}_{\mathcal{K}}^{a} > \overline{\Delta}_{\mathcal{A}_0}^{a}$, one-sided, within the difficulty strata of §6, by design-based bootstrap.
*Decision:* support if the difference is positive and significant after Holm correction.
*Falsifier:* if anchor gaps are comparable to charged gaps, the apparent divergence is measurement noise or inattention, not epistemic separation — the instrument is the story, not the population.

### 7.2 H-FCR2 — believed vs. expressive *(confirmatory)*
*Statement:* incentives compress gaps ($\textit{XP}>0$, material), **and** a residual believed gap remains (the incentivized-arm charged gap still exceeds the anchor floor).
*Test:* (a) $\textit{XP}>0$ at the §4.3 minimum detectable effect; (b) the H-FCR1 inequality in the incentivized arm.
*Decision:* support requires **both** (a) and (b).
*Guard:* because incentives may change who passes the attention checks, $\textit{XP}$ is also computed without exclusions; a conclusion that depends on the exclusions is reported as fragile.
*Falsifier:* if incentivized charged gaps collapse to the anchor floor, the divergence is *entirely expressive* — epistemic phase separation as a **belief** phenomenon is not supported. This narrows the discipline's information-layer claim from "divergent beliefs" to "divergent expression," and is a major, publishable negative result (Document 9 §8).

### 7.3 H-FCR3 — trend *(confirmatory; activates once at least six waves exist)*
*Statement:* the primary FCR declines over the tracking window.
*Test:* sign and significance of the linear slope of $\textit{FCR}_c^{a}(t)$ over the available waves (§4.3).
*Constraint:* forward-only; **no backcasting** (Document 9 §7).
*Decision/Falsifier:* a significant negative slope supports the secular-degradation reading of Document 5 §3; a flat or positive slope bears **against** it and is reported as such.
*Scope:* this is supplementary evidence on the mechanism behind Document 5's Prediction 2. It is **not** that prediction's resolution criterion — the FCR has no 2024 value, so it cannot enter a 2024-to-2028 comparison (Document 9 §7).

### 7.4 Pre-specified exploratory analyses
Partition sensitivity (education, age, urban/rural, media diet; Document 9 §6.3); results for non-leaning independents; **compositional change** in the two groups between waves, and the series recomputed holding composition fixed by reweighting; per-domain gap decomposition; the **per-wave directional-balance audit** (Document 10 §5) recorded with every release; mode and weighting robustness; the swing items analyzed separately as expressive-responding probes; and the relationship between the FCR and the other ECI components (MOS, NCI) as a convergent-validity check (Document 9 §12). All labeled exploratory.

---

## 8. Inference

- **Estimation:** weighted, design-based point estimates with variances from the panel's replicate weights (or a survey bootstrap where replicate weights are unavailable). The noise-corrected gaps and every statistic built on them take their bands from the same bootstrap, resampling respondents.
- **Uncertainty:** every reported scalar carries a band; bands propagate to the ECI and $\sigma_{\mathrm{epi}}$.
- **Framework:** frequentist primary (Holm-corrected family, §6); a Bayesian posterior on $\textit{FCR}_c^{a}$ and its trend is reported as a pre-specified complement, with weakly-informative priors stated at freeze.
- **"Support" thresholds:** confirmatory claims require post-correction significance and an effect at least at the §4.3 minimum detectable effect; smaller effects are reported as inconclusive, not as null.

---

## 9. Quality control and data integrity

- **Attention checks** are dedicated items embedded each wave. The neutral anchors (Table A) are monitored as a population-level inattention signal — an elevated anchor noise floor halts reporting pending investigation (Document 9 §3.1) — but are never used to exclude a respondent (§6).
- **Fraud/bot screening** via the panel provider plus internal duplicate and speeding checks (§6).
- **Incentivized-arm payment protocol:** small, pre-disclosed per-correct payments; payment logic concealed at response time; the schedule is fixed at freeze and reported. The arm is for *measurement*, not persuasion — correctness is not disclosed to respondents during the survey.
- **Noise-floor gate:** a wave is reportable only if the anchor floor is below a pre-set ceiling (fixed after the pilot).
- **Balance gate:** a wave is reportable only if the balance statistic is within tolerance, or after disclosed rebalancing (§6).

---

## 10. Reflexivity and ethics

- **IRB/consent:** standard informed consent; the instrument poses minimal risk; incentives are nominal.
- **Reflexivity (Document 2 §8.1):** publishing an FCR is itself an intervention in the epistemic environment it measures — it can become a Goodhart target or a corrective common-knowledge signal. Mitigations: the **dark rotating subset** (Document 10 §9) as an un-coachable tripwire; the transparency norm of Charter §10.
- **No ranking of groups.** Balance is enforced by item selection, so the instrument cannot say which group is better informed, and no output is presented as doing so (Document 9 §3.3). $\textit{ACC}$ is published pooled, never by group.
- **Two-sided publication commitment:** results are published whether or not they support the phase-separation hypothesis, with the anchor bank, ground-truth sources, code, and de-identified microdata released (Document 4 §9). The purely-expressive (H-FCR2 falsified) and no-signature (H-FCR1 falsified) outcomes are reported as such. This is non-negotiable (Document 6 §5; Charter §10).

---

## 11. Reproducibility

- **Frozen instrument hash:** the Document 10 bank (v1.1 or later) is hashed at freeze; the PAP records the hash; index versions tie to instrument versions (Document 4 §9).
- **Open code** regenerates every scalar from de-identified microdata.
- **Frozen inputs** for live and wave-set keys (provider, series, vintage, retrieval date) archived per wave.
- **Registry deposit:** this PAP and the instrument hash are time-stamped on a public registry before the first reportable wave.

---

## 12. Amendment and deviation protocol

Any change after freeze is a **timestamped amendment** appended to the registry record, stating what changed, when, and why, and whether it affects confirmatory or exploratory analyses. Confirmatory hypotheses and their falsifiers are not revised mid-stream; if circumstances force a change, the affected analysis is demoted to exploratory and a new confirmatory test is registered prospectively. Deviations discovered at analysis are disclosed in every output (Document 6 §5 discipline). Changes made *before* freeze are logged in §15.

---

## 13. Timeline and "done" definitions

| Step | Done when |
|------|-----------|
| Bank adjudication + cognitive pretest | Panel sign-off and pretest pass (Document 12 §2–§3; Document 10 §10) |
| Freeze + registry deposit | Instrument hash and this PAP timestamped on OSF/AsPredicted (Document 12 §4) |
| Pilot wave | Cut codes validated; anchor difficulty measured; variances and design effect measured; §4 targets re-derived; $\theta$, balance tolerance, and dead-bands re-anchored and locked |
| First reportable tracker wave | A published, reproducible $\textit{FCR}_c^{a}$ with band, $\textit{XP}$, $\textit{ACC}$, the noise floor, and the balance audit |
| Integration | FCR feeds a computed ECI and $\sigma_{\mathrm{epi}}$ (Document 4 §5; Document 9 §7) |

The first two rows complete Document 9 §11 stage 1 (frozen instrument and registered plan); the rest are stages 2–4.

**Two lock points.** The freeze fixes the design and the instrument before the pilot. The pilot then calibrates what can only be measured — cut codes, anchor difficulty, $\theta$, the balance tolerance, the dead-bands — and may replace items. Those pilot-driven changes are registered together as one dated amendment, and the instrument is re-tagged, before the first tracker wave is fielded. Nothing is changed after tracker data exist except under §12.

---

## 14. Reconciliation record

All of the following have been applied.

- **Document 8:** Phase B1 tracks FCR Stage 1 with this plan as its analysis half; registry deposit is noted as also serving Stage C0.
- **Document 9:** §8 remains the canonical summary of the pre-registration; §6–§8 here give it in full.
- **Document 7 (lexicon):** *pre-analysis plan*, *confirmatory vs. exploratory*, *anchor noise floor*, *dead-band*, and the balance vocabulary are entered in §4.3 and §4.5.
- **Document 5:** §7 carries the clarified resolution rule for Prediction 2, which does not depend on this plan.

---

## 15. Revision log

Changes made before freeze, with no data collected.

| Draft | Date | Section | Change | Reason |
|-------|------|---------|--------|--------|
| 1 | June 2026 | — | First draft | — |
| 2 | November 2026 | §2, §5, §6 | Statistics computed over the charged core with a noise-corrected root-mean-square gap; neutral anchors held apart | Carries through Document 9's corrections (dilution; sample-size dependence) |
| 2 | November 2026 | §0, §7 | Pilot barred from confirmatory tests | Items and codes are selected on the pilot |
| 2 | November 2026 | §3 | Groups defined (major-party identifiers including leaners; non-leaners separate) | Draft 1 never said who the two groups were |
| 2 | November 2026 | §3 | Matrix-sampled rotating pool; randomized item order | Survey length; order effects |
| 2 | November 2026 | §6, §9 | Balance tolerance, cut-code validation, and difficulty matching added; balance gate added | Balance and the noise floor had no empirical check |
| 2 | November 2026 | §6, §7.2, §9 | Exclusions reported by arm; neutral anchors barred as an exclusion criterion; $\textit{XP}$ re-run without exclusions | Differential exclusion could bias the arm comparison and the noise floor |
| 2 | November 2026 | §4.3 | Detectable trend restated as ≈ 0.5 pt/quarter | The earlier range was optimistic for eight waves |
| 2 | November 2026 | §1, §7.3 | Withdrawn: that this plan makes Document 5's Prediction 2 resolvable | The FCR has no 2024 value |
| 2 | November 2026 | §4.1 | Party identification removed as a default weighting target | It defines the groups |

---

*Draft pre-analysis plan, not yet frozen. Cite with caution. All power and threshold figures are estimated planning values to be replaced by pilot measurements before freeze; no wave has been fielded and no FCR exists. Constructs: Document 9 §2. Instrument: Document 10. Procedures to freeze: Document 12. Integrity and release: Document 4 §1, §9. Pre-registration precedent: Document 6.*
