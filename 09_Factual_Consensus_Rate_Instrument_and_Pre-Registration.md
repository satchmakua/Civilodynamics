# Civilodynamics — The Factual Consensus Rate: Instrument Specification and Pre-Registration

**Canonical Corpus, Document 9 · Instrument Specification & Pre-Registration · Working Draft v0.1 · June 2026**
**First building-phase document (the foundational corpus is Documents 1–8)**
**Satchel Hamilton · Civilodynamics Initiative**

> **Status and role.** This is the first document of the program's **building phase** — the point at which, per Document 8, the work "shifts from writing to building." It operationalizes one measure, the **Factual Consensus Rate (FCR)**, from the conceptual specification in **Document 4 §5.2** into a *fieldable, pre-registered survey instrument*. The FCR is the second of the three Epistemic Coherence Index components (with MOS and NCI, Document 2 §5, Document 4 §5), and it is the discipline's **single highest-priority empirical investment** (Charter §5; Document 2 §11.5; Document 4 §8 item 1; Document 8 near-term action 3) for three reasons: it is the load-bearing component of the discipline's distinctive axis, it is the one ECI component fully under program control, and — unlike the configuration database or the longitudinal trajectories — it can be **fully specified on paper now**, before any funding.
>
> **It defers, and it pre-registers.** Where construction or interpretation is concerned this document defers to Document 2 (the ECI as a first-class axis, §5; the baseline problem, §4.1) and Document 4 (the measurement philosophy and release protocol, §1, §9; the ECI build, §5). It does **not** re-derive that material. Following the precedent of **Document 6**, the second half of this document is a **pre-registration**: the constructs, thresholds, sampling plan, and analysis are fixed *here, before the instrument is fielded*, so that the eventual FCR series cannot be tuned after the data arrive. Nothing in this document is a computed result. The FCR has no values yet; it will have none until the instrument is built and fielded, and **it will never have historical values** (§7).

---

## 0. What this document covers

Eight objects, in order:

1. The design requirements an FCR must satisfy, drawn from Document 4 §5.2 (§1).
2. The formal construct: the FCR statistics, and how they relate to the ECI (§2).
3. The item battery: taxonomy, item-writing rules, and the ground-truth standard (§3).
4. The expressive-responding problem and the incentivized-accuracy design (§4).
5. The measurement model: from raw responses to the reported scalars (§5).
6. Sampling, fielding, and subgroup definition (§6).
7. From FCR to $\sigma_{\mathrm{epi}}$ and the ECI — including the honest treatment of the missing baseline (§7).
8. The **pre-registration** of the analysis (§8), the validity threats (§9), the release protocol (§10), and the build sequence, open problems, and reconciliation tasks (§11–§13).

---

## 1. Design requirements

Document 4 §5.2 specifies *what* the FCR is: "the fraction of a standing battery of verifiable factual propositions on which agreement holds across partisan (and other) subgroups." This document specifies *how to measure it well enough to be a field standard*. Six requirements bind the design; each is the operational form of a commitment already made in the corpus.

1. **It measures coherence, not knowledge.** The construct is *cross-group convergence* on verifiable facts, not aggregate civic knowledge. Two groups can both be wrong and still agree; that is high consensus on a low knowledge base, and the instrument must report the two separately and never conflate them (§5.2). The epistemic-coherence claim of the discipline (Charter §5; Document 2 §5) is about a **shared factual commons**, which is a statement about the *gap between communities*, not about how much any one community knows.
2. **Items must be verifiable and settled** — empirical propositions with documentable ground truth — never values, predictions, or contested interpretation (§3). This is the §5 integrity commitment applied at the item level.
3. **The battery must be directionally balanced** so that the correct answers do not, as a set, favor one partition over another. An instrument whose "facts" systematically flatter one side measures the instrument-builder's lean, not the population's. This is the even-handedness commitment of Documents 1 §10 and 5 §4, made structural (§3.3).
4. **It must separate believed divergence from expressive responding.** A known confound (Document 4 §5.2; Bullock et al. 2015) is that some respondents answer to signal identity rather than report belief. The design isolates this with an incentivized-accuracy arm (§4).
5. **It must be reproducible and auditable** to the release standard of Document 4 §9: a frozen, versioned item bank; documented ground-truth sources; open code; estimated/computed labels (§10).
6. **Its analysis must be pre-registered** before fielding, to forestall the item-selection analog of overfitting — the retrodiction hazard of Document 6 §1, here arising at the level of *which facts you choose to ask about* (§8, §9).

---

## 2. The construct

### 2.1 Per-item, per-group correct-belief rate

For battery item $k$ and population subgroup $g$, at wave time $t$, let

$$c_{g,k}(t) = \Pr\big(\text{a member of group } g \text{ gives the verified-correct answer to item } k\big),$$

estimated as the weighted share of group-$g$ respondents answering item $k$ correctly. The default partition is **partisan** (the partition Document 4 §5.1 names as default), with subgroups $A$ and $B$; the partition is one of several defensible choices and is sensitivity-tested against others (education, age, region, media diet — §6.3).

### 2.2 The cross-group gap

The divergence on item $k$ is the cross-group gap

$$\Delta_k(t) = \big|\, c_{A,k}(t) - c_{B,k}(t)\,\big| \in [0,1].$$

For more than two subgroups, $\Delta_k$ is the **maximum pairwise** gap (pre-registered default), with the mean pairwise gap reported as sensitivity. $\Delta_k$ near $0$ means the groups agree (whether or not they are correct); $\Delta_k$ near $1$ means they diverge sharply on a checkable fact — the operational signature of epistemic phase separation (Document 1 §5; Document 5 §4).

### 2.3 The two FCR statistics

Document 4 §5.2 licenses both a threshold form and a continuous index ("and/or"). The corpus reports **both**, on the fixed comparability set $\mathcal{K}$ (the anchor core, §3.2):

**Consensus-share (threshold) form** — interpretable and policy-legible:

$$\textit{FCR}_\theta(t) = \frac{1}{|\mathcal{K}|}\sum_{k\in\mathcal{K}} \mathbb{1}\{\Delta_k(t) < \theta\},$$

the share of anchor-core items on which the cross-group gap is below a pre-registered threshold $\theta$ (§8 fixes $\theta$).

**Mean-gap (continuous) form** — threshold-free, higher statistical power, bounded so that higher = more coherence:

$$\textit{FCR}_c(t) = 1 - \overline{\Delta}(t), \qquad \overline{\Delta}(t) = \frac{1}{|\mathcal{K}|}\sum_{k\in\mathcal{K}} \Delta_k(t).$$

The continuous form $\textit{FCR}_c$ is the **primary** statistic (it avoids threshold artifacts and propagates uncertainty cleanly); $\textit{FCR}_\theta$ is reported alongside for legibility. Both are computed per response arm (§4).

### 2.4 Relationship to the ECI

The ECI aggregate is unchanged from Document 2 §5 / Document 4 §5:

$$\textit{ECI}(t) = g\big(\textit{MOS}(t),\, \textit{FCR}(t),\, \textit{NCI}(t)\big),$$

with $g$ a normalized aggregate (equal-weight mean default, weights pre-registered). The component fed into $g$ is the **incentivized-arm continuous FCR**, $\textit{FCR}_c^{a}$ (§4), baseline-normalized per §7. The stress observable is, as in Document 4 §5, the sign-flipped baseline-normalized ECI: $\sigma_{\mathrm{epi}} \propto -\,\widehat{\textit{ECI}}$.

> **New notation introduced here** (to be added to Document 7 §2 and §4.3): $c_{g,k}$ (per-item, per-group correct rate), $\Delta_k$ (cross-group gap), $\theta$ (consensus threshold), $\textit{FCR}_\theta$ / $\textit{FCR}_c$ (the two FCR statistics), $\mathcal{A}$ / $\mathcal{K}$ (anchor core), $\textit{XP}$ (expressive component, §4), $\textit{ACC}$ (knowledge level, §5.2), and the arm superscripts $b$/$a$ (belief / accuracy-incentivized). None collide with existing corpus symbols ($\Delta$, $\theta$, $c$ were unassigned); the reconciliation task is logged in §13.

---

## 3. The item battery

### 3.1 Taxonomy

The battery mixes two classes of item, after Document 4 §5.2:

- **Neutral anchors.** Uncontroversial, non-political empirical facts (basic civic, scientific, numerical) — e.g., the approximate length of a year, the number of branches of the federal government, a simple arithmetic comparison. These are *not* the object of interest; they establish the **measurement-noise floor** (the residual gap attributable to attention, comprehension, and guessing rather than to factual divergence) and detect inattentive or random responding. A non-trivial gap on neutral anchors is a data-quality alarm, not a finding.
- **Charged-but-settled items.** Empirical propositions that are politically salient *yet have documentable, settled ground truth* — stated as checkable, directional claims about authoritative quantities. The canonical format is directional: "Over the most recent reported 12-month period, [official quantity X] [rose / fell / was about unchanged]," scored against the relevant official series. These items span the economic, demographic, public-health, environmental, and public-record domains. **They are where epistemic phase separation, if it is real and believed, shows up** as a large $\Delta_k$.

This document deliberately does **not** enumerate specific charged items. The item bank is developed and adjudicated under the protocol below and published per §10; fixing partisan-charged exemplars in the canon would both date the instrument and risk encoding exactly the lean §3.3 exists to prevent. What is canonical is the *format* (directional, checkable, single authoritative source) and the *rules*.

### 3.2 The anchor core and the rotating pool

- **Anchor core $\mathcal{A}$** (target ≈ 30–50 items): a fixed set held constant across waves to make the FCR **longitudinally comparable**. The comparability set $\mathcal{K}$ in §2.3 is the anchor core. Anchor-core items whose ground truth can change over time (directional claims about live series) carry a *fixed question template* with a *wave-updated correct answer*, so the question is stable while the truth is re-adjudicated each wave (§3.4).
- **Rotating pool** (target ≈ 20–40 items/wave): refreshed each wave to **prevent priming and learning effects**, to track new factual terrain, and to guard against the anchor core becoming a coached target (a Goodhart risk, §9). Rotating-pool results are reported as a separate, non-longitudinal panel; only the anchor core enters the headline FCR time series.

### 3.3 Item-writing rules

Every item must satisfy, by rule:

1. **Verifiable and settled.** A single, documentable ground truth exists from an authoritative source (§3.4). Predictions, counterfactuals, attributions of cause, and any normative or values content are excluded.
2. **Directional / checkable framing.** Where the underlying quantity is continuous, the item asks for a *direction* or a *coarse magnitude bracket*, not a point estimate, so that "correct" is unambiguous and robust to data revision.
3. **Directional balance (mandatory).** Across the battery, the set of correct answers must not systematically favor either partition. Balance is pre-registered and audited: for the charged-but-settled set, the distribution of which side's prior the correct answer "cuts against" is held approximately even. An unbalanced battery is a biased instrument regardless of each item's individual truth.
4. **Neutral wording.** No partisan cue words, loaded framing, or affect-laden terms; reading level controlled and pretested for comprehension (§3.5).
5. **An explicit "not sure" option** on every item, to separate genuine uncertainty from guessing (§5.1).

### 3.4 Ground-truth adjudication — the "who decides what is a fact" problem

This is the instrument's deepest validity threat and is met head-on, in the corpus's demote-to-checkable spirit (Document 5 §4; Document 7 §6). The protocol:

- **A pre-registered sourcing hierarchy.** Ground truth is taken, in order, from: (i) official government statistical series (e.g., BLS, Census, CBO, CDC and equivalents); (ii) settled consensus of authoritative scientific bodies; (iii) the documentable public record. Each item carries its source, the exact series/figure, and a retrieval date — **frozen at the wave vintage**, exactly as Document 4 §9 requires of every input.
- **A bipartisan / multi-perspective adjudication panel** reviews each candidate item. **Any item on which adjudicators cannot agree that the ground truth is settled and documentable is excluded.** Contestedness at adjudication is a disqualifier, not a finding to be reported.
- **Audit by publication.** The full anchor-core bank and its ground-truth sources are published (§10); rotating-pool items are embargoed until after their wave is fielded, then released. External critics can therefore challenge the ground truth of any item directly.

The honest residual: this protocol restricts the FCR to the domain of propositions with institutionally-settled ground truth. That is a real limitation — it excludes exactly the most contested terrain — and it is the correct limitation, because measuring divergence on genuinely unsettled questions would conflate epistemic fragmentation with legitimate disagreement.

### 3.5 Cognitive pretesting

Before an item enters the bank it is cognitively pretested (think-aloud interviews) for comprehension, unintended cueing, and answerability, and pilot-fielded (§11, stage 2) for response distributions and discrimination. Items that load on comprehension or partisanship rather than on factual belief are cut.

---

## 4. The expressive-responding problem and the incentivized-accuracy design

> **Why this section is load-bearing.** If respondents give partisan answers to *signal identity* rather than to *report belief* (partisan cheerleading; Bullock et al. 2015; Prior et al. 2015), a naïve FCR overstates epistemic fragmentation — it measures performance, not the state of the factual commons. An FCR that cannot separate the two is not yet a measure of epistemic coherence. The design isolates them.

**The two arms.** Each wave randomizes respondents (within subgroup, to preserve balance) into:

- a **standard / belief arm** (superscript $b$): items asked conventionally;
- an **accuracy-incentivized arm** (superscript $a$): small payments for correct answers (and, optionally, for honest "not sure" calibration), which are known to compress apparent partisan gaps by raising the cost of expressive responding.

Each FCR statistic is computed per arm: $\textit{FCR}_c^{b}$ and $\textit{FCR}_c^{a}$, and likewise $\textit{FCR}_\theta^{b}$, $\textit{FCR}_\theta^{a}$.

**The expressive component.** Define

$$\textit{XP}(t) = \textit{FCR}_c^{a}(t) - \textit{FCR}_c^{b}(t),$$

the consensus that incentives *recover*. Under the expressive-responding hypothesis $\textit{XP} > 0$: incentives compress gaps, so the incentivized arm shows more consensus. $\textit{XP}$ is not a nuisance to be removed — it is **itself a substantive measure** of how performative the divergence is (a large $\textit{XP}$ means much of the apparent fragmentation is identity signaling; a small $\textit{XP}$ means the divergence is largely believed).

**Which arm is primary.** The **incentivized-accuracy arm** $\textit{FCR}_c^{a}$ is the primary FCR — it is the closest available estimate of genuine cross-group *belief* divergence, and it is the value fed into the ECI (§2.4). The belief-arm value $\textit{FCR}_c^{b}$ and the expressive component $\textit{XP}$ are reported alongside it as standing diagnostics. Both are needed: behavior is driven by what people will *act on*, which sits between the two arms, so suppressing either would discard signal.

---

## 5. The measurement model

From raw responses to the reported scalars.

**Step 1 — Score items.** Each response is coded correct / incorrect / "not sure" against the frozen ground truth (§3.4).

**Step 2 — Estimate group rates.** Compute survey-weighted $c_{g,k}(t)$ per arm (§5.1 fixes the "not sure" rule), with design-based standard errors.

**Step 3 — Compute gaps and FCR statistics.** Form $\Delta_k$ (§2.2) and then $\textit{FCR}_c$, $\textit{FCR}_\theta$ per arm (§2.3), plus $\textit{XP}$ (§4). Propagate sampling uncertainty to a band on every reported value (Document 4 §1, §4: a value without a band is incomplete).

**Step 4 — Report jointly** with the knowledge level $\textit{ACC}$ (§5.2) and the neutral-anchor noise floor (§3.1), so the FCR is never read in isolation.

### 5.1 Handling "not sure" and guessing

Every item offers an explicit "not sure." The pre-registered default excludes "not sure" from the correct-rate denominator (so $c_{g,k}$ is correctness *among those who venture an answer*) while tracking the **uncertainty rate** separately — rising *shared* uncertainty is itself an informative, and benign, epistemic state distinct from divergence. The explicit option suppresses blind guessing; for binary/directional items a guessing correction is reported as sensitivity. The treatment is fixed in §8 and not varied post hoc.

### 5.2 Coherence is not knowledge — reported jointly

To enforce requirement §1.1, every FCR is reported next to the **knowledge level**

$$\textit{ACC}(t) = \frac{1}{|\mathcal{K}|}\sum_{k\in\mathcal{K}} \tfrac{1}{2}\big(c_{A,k}(t)+c_{B,k}(t)\big),$$

the mean cross-group correct rate. A high FCR with low $\textit{ACC}$ is *shared ignorance*, not a healthy commons, and the framework must not read it as coherence; reporting the pair forecloses that error. $\textit{ACC}$ never enters the FCR or the ECI — it is a companion diagnostic only.

---

## 6. Sampling, fielding, and subgroups

### 6.1 Frame and mode

A **probability-based** panel (address-based-recruited online panel; e.g., a NORC AmeriSpeak-class or comparable instrument), not an opt-in convenience panel, so that subgroup estimates are defensible. Self-administered online mode (with offline accommodation in the recruited frame) to standardize presentation and support the incentivized arm.

### 6.2 Size and cadence

- **Cadence:** quarterly rolling tracker (Document 4 §5.2), establishing a forward time series.
- **Wave size (design target, estimated):** $n \approx 2{,}500$–$3{,}500$ completed interviews per wave, split across the two arms (§4) and weighted to population benchmarks. This targets per-arm, per-subgroup cells of roughly $n \approx 500$–$900$, giving a single-item proportion standard error of about $\pm 1.7$–$2.2$ points and a much tighter band on the anchor-core means $\overline{\Delta}$, $\textit{FCR}_c$. These figures are **estimated** planning targets, to be confirmed by the pilot power analysis (§11), not computed results.
- **Panel conditioning** is controlled by item rotation (§3.2) and by refreshing the panel with fresh probability samples on a fixed schedule.

### 6.3 Subgroups and partition sensitivity

The headline partition is partisan (default, Document 4 §5.1). Because the partition choice is itself a modeling decision, the FCR is recomputed under alternative partitions — education, age cohort, urban/rural, and self-reported media diet — and the sensitivity is reported. If the divergence structure is specific to the partisan partition, that is a finding about *political* epistemic separation; if it appears across partitions, the phenomenon is broader. Either way the partition dependence is disclosed, never buried.

---

## 7. From FCR to $\sigma_{\mathrm{epi}}$ and the ECI — and the missing baseline

The FCR enters the ECI per §2.4 and thence the epistemic stress block per Document 4 §5. Two honest constraints govern this, both inherited and non-negotiable:

**No historical values — ever.** The FCR begins when the instrument is fielded and has no pre-instrument values; **pre-instrument FCR is never reported as data** (Document 4 §5.2; Document 5 §3). This is not a temporary gap to be backfilled — there is no way to reconstruct an incentivized-accuracy cross-group gap for a population that was never surveyed. The historical epistemic block therefore continues to rest on the reconstructed MOS (Document 4 §5.1), with the FCR contributing only from its fielding date forward.

**Modern-era extension, not the mid-century baseline.** Consistent with the assignment table of Document 4 §4, the FCR (and the ECI it feeds) sits in the **modern-era extension** of the CSI, with its own later reference window and explicit uncertainty — never in the coverage-restricted mid-century baseline covariance, which cannot contain it (Document 2 §4.1). Once a few years of waves exist, the FCR's own early waves can serve as its internal reference for normalization, with the window stated and defended (Document 2 §4.1; Document 4 §4 Step 2).

**This is what makes Document 5's Prediction 2 resolvable.** Prediction 2 (ECI(2028) < ECI(2024)) is registered as *conditional on the ECI instrument being fielded*. Fielding this instrument is the precondition that converts that prediction from conditional to live. Until then, any ECI value in the corpus remains **estimated/illustrative** (Document 5 §3; Document 7 §5).

---

## 8. Pre-registration of the analysis (recorded June 2026, before fielding)

In the manner of Document 6 §5.2, the following are fixed now, before the instrument is fielded, and may not be adjusted after the data arrive without a separately-timestamped amendment.

**Fixed design and statistics.**
- The **comparability set** is the anchor core $\mathcal{A}$ (§3.2), frozen at instrument v1.0.
- The **gap statistic** is the maximum pairwise $\Delta_k$ (§2.2); mean-pairwise is sensitivity only.
- The **primary FCR** is the incentivized-arm continuous index $\textit{FCR}_c^{a}$ (§2.3, §4); $\textit{FCR}_\theta^{a}$ and the belief-arm values are reported alongside.
- The **consensus threshold** $\theta$ for $\textit{FCR}_\theta$ is fixed in the computation plan at instrument freeze (a single value, with the consensus-share reported as a curve over $\theta$ for transparency) and not re-chosen to flatter a result.
- The **"not sure" rule** is the §5.1 default (excluded from the correctness denominator; uncertainty rate tracked separately).
- The **default partition** is partisan; the alternative partitions of §6.3 are pre-specified sensitivity analyses.

**Hypotheses and their falsifiers** (stated so each can fail):

- **H-FCR1 — phase-separation signature.** Cross-group gaps are *concentrated in the charged-but-settled items and near the noise floor on neutral anchors*. **Falsifier:** if neutral-anchor gaps are comparable to charged-item gaps, the apparent divergence is measurement noise or inattention, not epistemic separation, and the instrument — not the population — is the story.
- **H-FCR2 — believed vs. expressive.** The expressive component $\textit{XP}$ is positive and material (incentives compress gaps), **and** a residual believed gap remains (the incentivized-arm charged-item gap exceeds the anchor noise floor). **Falsifier:** if incentivized gaps collapse to the noise floor, the divergence is *entirely expressive* — epistemic phase separation as a *belief* phenomenon is not supported. This would be a major, publishable negative result, narrowing the discipline's information-layer claim from "divergent beliefs" to "divergent expression."
- **H-FCR3 — trend (links to Document 5 Prediction 2).** Once the series is long enough, test whether $\textit{FCR}_c^{a}$ (and the ECI it feeds) declines over the tracking window. **Constraint:** forward-only; no backcasting. A flat or rising FCR over 2026–2028 would bear against Prediction 2 and against the secular-degradation reading of Document 5 §3.

**Two-sided publication commitment.** Results are published whether or not they support the epistemic-phase-separation hypothesis, with the anchor-core bank, ground-truth sources, and code released (§10). The purely-expressive result (H-FCR2 falsified) and the no-signature result (H-FCR1 falsified) are reported as such — this is the Document 6 §5 discipline applied to the FCR.

---

## 9. Validity threats and limitations

Stated plainly, in the corpus's self-critical register.

- **Item-selection bias — the overfitting analog.** The single largest threat is that the *choice of items* manufactures or hides divergence. This is the retrodiction hazard of Document 6 §1 relocated to instrument design: with enough latitude in item choice, an analyst can produce nearly any FCR. **Mitigations:** the pre-registered selection protocol (§3, §8), mandatory directional balance (§3.3), adversarial item review by the adjudication panel (§3.4), a large anchor core, and full publication of the bank for external audit.
- **The ground-truth problem.** Addressed at length in §3.4; the residual is that the FCR is confined to propositions with settled, documentable ground truth — by design, and at the cost of excluding the most contested terrain.
- **Residual expressive responding.** Incentives compress but do not eliminate expressive answering; $\textit{XP}$ captures the recovered portion, and the incentivized arm is the best available approximation of belief, not a perfect one.
- **Mode, weighting, and panel conditioning.** Online-mode and weighting effects, and conditioning from repeated participation, are controlled by the probability frame, item rotation, and scheduled panel refreshment (§6) — controlled, not eliminated.
- **Partition dependence.** The headline result depends on the partisan partition; §6.3 discloses the sensitivity rather than asserting partisan primacy.
- **Cross-national comparability is deferred.** Translating the instrument and its ground-truth sourcing across polities (for Document 8 Phase B4) introduces comparability problems not solved here; the FCR as specified is a single-polity instrument.
- **Reflexivity (Document 2 §8.1).** Publishing an FCR is itself an intervention in the epistemic environment it measures: a published "consensus score" can become a Goodhart target, or, conversely, a corrective common-knowledge signal. The program's posture is the transparency norm of Charter §10 (publish openly so the effect is distributed), reinforced by the dark rotating pool (§3.2) that keeps part of the instrument un-coachable.

---

## 10. Reproducibility and release protocol

Per Document 4 §9, every published FCR wave ships with:

- **Frozen instrument.** The versioned item bank, with each item's ground-truth source, exact series/figure, and retrieval date archived at the wave vintage.
- **Open construction.** The full recipe: items, scoring, "not sure" rule, gap statistic, $\theta$, arm design, weighting, and aggregation into the ECI.
- **Open code** that regenerates every reported scalar from the de-identified microdata.
- **Uncertainty and sensitivity.** A band on every value; the partition and threshold sensitivities of §6.3 and §8.
- **Estimated/computed labels** (Document 4 §1; Document 7 §5). Pilot and pre-instrument figures are labeled estimated; only fielded-wave values are computed.
- **Item disclosure with embargo.** The anchor core is published; rotating-pool items are released after their wave to preserve the priming guard.

Published as a **candidate field standard** (Document 4 §5.4) so that others can adopt, replicate, and critique it.

---

## 11. Build sequence and milestones (Track B1)

Slotting into Document 8 Track B1 and Document 2 §11.5. Four stages, with a "done" definition each.

1. **Instrument development & pre-registration — paper stage, feasible now, no funding.** Draft the item bank; convene the adjudication panel; cognitively pretest; freeze the pre-analysis plan (this document is its skeleton). The Stage-1 drafts are **Document 10** (anchor-core item bank) and **Document 11** (pre-analysis plan), with freeze pending panel sign-off and pretest. *Done:* a frozen instrument v1.0 and a registered pre-analysis plan.
2. **Pilot wave.** A single cross-section ($n \approx 1{,}500$, including the incentivized split) to validate item performance, comprehension, directional balance, the anchor noise floor, and the expressive component; refine and re-freeze the anchor core; run the power analysis that fixes §6.2. *Done:* a validated anchor core and confirmed sampling parameters.
3. **Standing quarterly tracker.** Field the rolling tracker; produce the first **computed** FCR series. *Done:* a published, reproducible FCR time series with bands.
4. **Integration.** Combine with the MOS pipeline (Document 4 §5.1) and NCI (§5.3) into the ECI; supply the baseline-normalized $\sigma_{\mathrm{epi}}$ to the CSI as a modern-era extension (§7). *Done:* a computed ECI feeding a computed epistemic stress block.

**Cost (estimated, planning only — not financial advice; cf. Document 8).** The pilot is small; standing waves run on the order of a modest per-wave survey cost, with the anchor-core design keeping marginal cost low once established. This is the cheapest high-value build in the program (Charter §5), which is why it leads Track B1.

---

## 12. Open problems (for Document 2 §11 / Document 8)

1. **Calibrate $\theta$** empirically once the noise floor is measured (relate the consensus threshold to the anchor-anchor gap distribution).
2. **Formalize the belief/expressive decomposition** beyond the single $\textit{XP}$ scalar (e.g., per-item, and as a function of item charge).
3. **The pre-instrument epistemic block** remains MOS-reconstruction-only; quantify how much of $\sigma_{\mathrm{epi}}$ history the FCR can never cover, and bound the resulting uncertainty.
4. **Pre-register the ECI weighting $g$** (§2.4) and test whether FCR, MOS, and NCI actually co-move (a convergent-validity check on the ECI itself).
5. **Cross-national instrument** design for Phase B4 (§9).

---

## 13. Reconciliation tasks created by this document

In the corpus's standing practice of logging the forward changes a new document requires (cf. Document 7 §7; Document 2 §11):

- **Document 8 (program map):** add the FCR instrument as the first **active** B1 deliverable with the four stages of §11; update the near-term action list (item 3 moves from "scope" to "in progress / instrument drafted"); note that fielding it makes Document 5 Prediction 2 live.
- **Document 7 (lexicon):** add the §2.4 notation ($c_{g,k}$, $\Delta_k$, $\theta$, $\textit{FCR}_\theta$, $\textit{FCR}_c$, $\mathcal{A}$, $\textit{XP}$, $\textit{ACC}$, arm superscripts $b$/$a$) to §2, and add lexicon entries (anchor core, rotating pool, directional balance, incentivized-accuracy arm, expressive component, ground-truth adjudication) to §4.3 / §4.5.
- **Document 4 (measurement program):** §5.2 is now operationalized here; cross-reference this document as the FCR's full specification and pre-registration.
- **Document 5 (case study):** the "Bullock et al." reference stub (Document 5, references note) lands here; Prediction 2's conditional is the fielding of this instrument.

---

## References

Bullock, J. G., Gerber, A. S., Hill, S. J., & Huber, G. A. (2015), *Partisan bias in factual beliefs about politics*; Prior, M., Sood, G., & Khanna, K. (2015), *You cannot be serious: the impact of accuracy incentives on partisan bias in reports of economic perceptions*; Kahan, D. M. (2017); Pennycook, G., & Rand, D. G. (2019); Reuters Institute (2023); plus the public-statistics providers named as ground-truth sources in §3.4 (BLS, Census, CBO, CDC and equivalents), cited at item vintage.

---

*Working draft and pre-registration. Cite with caution. No FCR has yet been computed; this document specifies an instrument and fixes its analysis before fielding. The FCR has no historical values and will acquire none. Construction defers to Documents 2 §5 and 4 §5; integrity labels and release discipline follow Document 4 §1, §9; the pre-registration follows the precedent of Document 6. This is the first building-phase document of the corpus; the foundational corpus is Documents 1–8.*
