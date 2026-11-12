# Civilodynamics — Factual Consensus Rate: Anchor-Core Item Bank

**Building-Phase Document 10 · Instrument v1.0, draft 2 (for adjudication) · June 2026, revised November 2026**
**Stage-1 deliverable of Document 9 §11 · Satchel Hamilton · Civilodynamics Initiative**

> **Status and role.** This is the **instrument** half of the FCR Stage-1 deliverable (Document 9 §11, stage 1; the analysis half is **Document 11**, the pre-analysis plan). It is the concrete anchor-core item bank that Document 9 §3 specifies but — by deliberate design (§3.1) — does **not** enumerate, because fixing partisan-charged exemplars in the *canon* would date the instrument and risk encoding a lean. The items therefore live here, in the instrument document, where they can be adjudicated, revised, and versioned without touching the canon.
>
> **It is a draft, not a frozen instrument.** Per Document 9 §3.4–§3.5, the bank is not frozen until (i) the multi-perspective **adjudication panel** has confirmed each item's ground truth is settled and documentable and ruled on directional balance, and (ii) every item has passed **cognitive pretesting** (comprehension, unintended cueing, answerability). This document is the input to those two steps (procedures: Document 12). Items flagged **`[PANEL]`** carry specific adjudication questions. Nothing here has been fielded; there are no responses and no FCR values.
>
> **Scope.** This document contains only the **anchor core** $\mathcal{A} = \mathcal{A}_0 \cup \mathcal{K}$ (Document 9 §3.2): the neutral anchors $\mathcal{A}_0$ (Table A), which supply the noise floor, and the charged core $\mathcal{K}$ (Table B), over which the FCR is computed. The rotating pool is generated per wave under the same rules and is embargoed until its wave is fielded (§9). Construction defers to Document 9 §2–§5; release discipline follows Document 4 §9.
>
> **What changed in draft 2 (November 2026).** A review of draft 1 found one wrong key, one defective item, and several cut codes that could not be defended. B20 carried a key that newer data had already overturned and is now a fixed-window item; B17 is narrowed to the claim the consensus reviews actually address; anchor A09 no longer prints its own answer; B20 and B23 are recoded cross-partisan; two left-cutting items with statistical-series sources (B29, B30) and six harder neutral anchors (A11–A16) are added. Cut codes are now explicitly provisional and are validated empirically (§5). Details are in §12.

---

## 1. What an item must satisfy (recap)

Each item obeys the Document 9 §3.3 rules, reproduced here as the acceptance checklist the adjudication panel applies:

1. **Verifiable and settled** — a single documentable ground truth from an authoritative source (Document 9 §3.4); no predictions, no attributions of cause, no values or normative content.
2. **Directional / checkable framing** — for continuous quantities, ask a *direction* or a *coarse magnitude bracket*, never a point estimate, so "correct" is unambiguous and robust to data revision.
3. **Directional balance** — across the battery the correct answers favor no partition (§5); balance is audited, not assumed.
4. **Neutral wording** — no partisan cue words, loaded framing, or affect-laden terms; controlled reading level.
5. **Explicit "not sure"** on every item (Document 9 §5.1).

---

## 2. Response and scoring conventions

- **Response options.** Every item offers its substantive options **plus "Not sure."** Directional items use *increased / decreased / stayed about the same*; magnitude items use coarse brackets; factual items use the stated choices or true/false.
- **Scoring key.** Each item has a coded correct answer (the *key*), of one of three types. A **fixed** key belongs to a closed historical window or a settled fact and does not change. A **live** key is read from a series that is still moving, so it is re-verified at every wave even where it has been stable for decades. A **wave-set** key has no standing value at all and is set fresh each wave. Live and wave-set keys are adjudicated from the named source at a frozen retrieval date (Document 9 §3.2, §3.4), so the question template is fixed while the truth is re-verified.
- **The key column is illustrative.** It states the key as of November 2026. It is **estimated**, not a fielded result, and it is not what a wave is scored against: the wave's own adjudication is.
- **"Not sure."** Excluded from the correctness denominator by default (Document 9 §5.1); the share choosing it is tracked as the **uncertainty rate**. The explicit option suppresses blind guessing; a guessing correction is reported as sensitivity (Document 11).
- **Per-item statistics.** From responses the pipeline computes $c_{g,k}$ (per-group correct rate), the signed gap $\delta_k$ and its sampling variance, and thence the noise-corrected gap, $\textit{FCR}_\theta$, $\textit{FCR}_c$, $\textit{XP}$, and $\textit{ACC}$ (Document 9 §2, §4, §5).

**Cut codes (the balance ledger, §5).** Each charged item carries a *provisional* code for which prior its correct answer is expected to cut against: **R** (challenges a right-leaning prior), **L** (challenges a left-leaning prior), **X** (cross-partisan — both sides tend to err, or no stable partisan prior is asserted), **S** (swing — incumbent-dependent; the cut flips with which party holds power, so these are the prime expressive-responding items of Document 9 §4 and balance over time by construction). A cut code is a hypothesis about respondents, not a property of the fact; §5 says how it is tested.

---

## 3. Table A — Neutral anchors $\mathcal{A}_0$ (the noise floor)

Non-political facts establishing the measurement-noise floor and detecting inattentive responding (Document 9 §3.1). **They do not enter the FCR.** A non-trivial cross-group gap here is a data-quality alarm, **not** a finding.

Easy items cannot show a gap — a correct rate near 1 leaves no room for one — so a floor built only from easy items would flatter the comparison with Table B. The anchors therefore span a range of difficulty (**E**asy / **M**edium / **H**ard). The bands below are provisional expectations, replaced by measured correct rates in the pilot.

| ID | Item | Options | Key | Source | Difficulty |
|----|------|---------|-----|--------|------------|
| A01 | The Earth completes one orbit of the Sun in approximately how long? | 1 day / 1 month / 1 year / 10 years | 1 year | Astronomical fact | E–M |
| A02 | How many members serve in the United States Senate? | 50 / 100 / 435 / 538 | 100 | U.S. Constitution; Senate.gov | M |
| A03 | How many justices currently sit on the U.S. Supreme Court? | 7 / 9 / 12 / 15 | 9 | 28 U.S.C. §1; SupremeCourt.gov | M |
| A04 | How many terms may a person be *elected* U.S. President? | 1 / 2 / 3 / no limit | 2 | 22nd Amendment | E |
| A05 | How many branches does the U.S. federal government have? | 2 / 3 / 4 | 3 | U.S. Constitution | E–M |
| A06 | Antibiotics kill which of the following? | bacteria / viruses / both | bacteria | WHO; standard microbiology | M |
| A07 | Which is smaller? | an electron / an atom | an electron | Standard physics | M |
| A08 | The total population of the United States is closest to: | 130 million / 230 million / 330 million / 530 million | 330 million | U.S. Census Bureau | M |
| A09 | Which is the larger amount? | 1% of 1,000 / 10% of 50 | 1% of 1,000 (10, against 5) | Numeracy | M |
| A10 | Roughly what share of the day is 6 hours? | one-quarter / one-half / three-quarters | one-quarter | Numeracy | E |
| A11 | A light-year is a measure of: | distance / time / brightness / speed | distance | Standard astronomy | M |
| A12 | Ocean tides are caused mainly by: | the Moon's gravitational pull / the Earth's rotation / wind / heat from the Sun | the Moon's gravitational pull | Standard physics | M |
| A13 | Water boils at a lower temperature at high altitude than at sea level: | true / false | true | Standard physics | H |
| A14 | The loudness of a sound is determined mainly by the sound wave's: | amplitude / frequency / wavelength / speed | amplitude | Standard physics | H |
| A15 | If the chance of an event is 10%, about how many times would it be expected to occur in 1,000 trials? | 10 / 100 / 110 / 900 | 100 | Numeracy | E–M |
| A16 | If 5 machines take 5 minutes to make 5 parts, how long would 100 machines take to make 100 parts? | 5 minutes / 20 minutes / 100 minutes / 500 minutes | 5 minutes | Numeracy (reflection) | H |

*Panel note `[PANEL]`:* confirm that the science and numeracy anchors read as non-political knowledge, not as politically coded. Any anchor that shows a partisan gap in the pilot comparable to Table B is not a neutral anchor: it is demoted or replaced, and the reason is recorded.

---

## 4. Table B — Charged-but-settled items (the charged core $\mathcal{K}$)

Politically salient propositions with **settled, documentable** ground truth, stated as checkable claims (Document 9 §3.1). **The FCR is computed over these items.** The key column is illustrative as of November 2026 and marks each key *fixed*, *live*, or *wave-set* (§2).

### 4.1 Economy and labor

| ID | Item | Options | Key (illustrative) | Source | Cut |
|----|------|---------|--------------------|--------|-----|
| B01 | Over the past 12 months, the national unemployment rate has: | increased / decreased / stayed about the same | *wave-set* | BLS, CPS (U-3) | **S** |
| B02 | Over the past 12 months, the rate of consumer price inflation has: | increased / decreased / stayed about the same | *wave-set* | BLS, CPI-U (12-month change) | **S** |
| B03 | Compared with one year ago, the S&P 500 stock index is: | higher / lower / about the same | *wave-set* | Market close, frozen date | **S** |
| B04 | Over the past 12 months, the federal budget deficit has: | grown / shrunk / stayed about the same | *wave-set* | CBO; U.S. Treasury Monthly Statement | **S** |
| B05 | Adjusted for inflation, the federal minimum wage today, versus the late 1960s, is: | higher / lower / about the same | lower (live) | DOL Wage and Hour Division; BLS CPI | **R** |
| B06 | The share of all **federal individual income taxes** paid by the highest-earning 10% of filers is closest to: | ~25% / ~50% / ~70% | ~70% (live) | IRS Statistics of Income; CBO | **L** |
| B07 | Inflation-adjusted U.S. manufacturing *output* (real value added) today, versus ~30 years ago, is: | higher / lower / about the same | higher (live) | BEA; Federal Reserve G.17 | **X** |

### 4.2 Public finance and government

| ID | Item | Options | Key (illustrative) | Source | Cut |
|----|------|---------|--------------------|--------|-----|
| B08 | The single largest category of U.S. federal spending is: | Social Security / national defense / interest on the debt / foreign aid | Social Security (live) | CBO; OMB | **X** |
| B09 | Foreign aid as a share of total federal spending is closest to: | ~1% / ~10% / ~25% | ~1% (live) | OMB; ForeignAssistance.gov | **X** |
| B10 | National defense as a share of total federal spending is closest to: | ~13% / ~35% / ~55% | ~13% (live) | OMB; CBO | **X** |
| B29 | Adjusted for inflation, public-school spending per student today, versus about 30 years ago, is: | higher / lower / about the same | higher (live) | NCES, Digest of Education Statistics | **L** |

### 4.3 Crime and justice

| ID | Item | Options | Key (illustrative) | Source | Cut |
|----|------|---------|--------------------|--------|-----|
| B11 | Compared with the early 1990s, the U.S. violent crime rate is: | higher / lower / about the same | lower (live) | FBI UCR; BJS NCVS | **R** |
| B12 | The U.S. murder rate in 2020–2021, compared with 2019, was: | higher / lower / about the same | higher (fixed) | FBI UCR; NCHS | **L** |
| B13 | Most firearm deaths in the United States each year are: | homicides / suicides / accidents | suicides (live) | NCHS mortality data (WISQARS) | **X** |
| B14 | The U.S. incarceration rate, compared with other wealthy democracies, is: | among the highest / about average / among the lowest | among the highest (live) | BJS; World Prison Brief | **X** |

### 4.4 Immigration and demography

| ID | Item | Options | Key (illustrative) | Source | Cut |
|----|------|---------|--------------------|--------|-----|
| B15 | The foreign-born share of the U.S. population today, versus its early-1900s peak, is: | much higher / much lower / about the same | about the same (live) | U.S. Census Bureau (ACS; historical census) | **X** |
| B16 | Of all foreign-born people living in the U.S., the majority are present: | lawfully / unlawfully | lawfully (live) | DHS Office of Homeland Security Statistics; Census | **R** |

### 4.5 Health and epidemiology

| ID | Item | Options | Key (illustrative) | Source | Cut |
|----|------|---------|--------------------|--------|-----|
| B17 | The MMR (measles, mumps, rubella) vaccine causes autism: | true / false | false (fixed) | Tier (ii): Institute of Medicine consensus reviews (2004, 2011); WHO | **X** |
| B18 | The leading cause of death in the United States is: | heart disease / cancer / drug overdose / COVID-19 | heart disease (live) | NCHS | **X** |
| B19 | The U.S. uninsured rate today, versus 2010 (before the ACA's main provisions), is: | higher / lower / about the same | lower (live) | U.S. Census Bureau; NCHS NHIS | **R** |
| B20 | U.S. life expectancy in 2021, compared with 2019, was: | higher / lower / about the same | lower (fixed) | NCHS | **X** |

### 4.6 Energy and environment

| ID | Item | Options | Key (illustrative) | Source | Cut |
|----|------|---------|--------------------|--------|-----|
| B21 | Over the past ~100 years, the global average surface temperature has: | risen / fallen / stayed about the same | risen (fixed) | NASA GISS; NOAA; IPCC | **R** |
| B22 | Among climate scientists who actively publish on the subject, the share who agree recent warming is mostly human-caused is closest to: | ~50% / ~75% / ~97% | ~97% (fixed) | Tier (ii): published consensus studies; national academies | **R** |
| B23 | The country that produces the most crude oil in the world today is: | Saudi Arabia / Russia / the United States / China | the United States (live) | EIA; IEA | **X** |
| B24 | U.S. energy-related CO₂ emissions today, versus their mid-2000s peak, are: | higher / lower / about the same | lower (live) | EIA; EPA greenhouse-gas inventory | **L** |
| B25 | The United States today generates more electricity from natural gas than from coal: | true / false | true (live) | EIA Electric Power Monthly | **X** |
| B30 | Compared with 1990, national average levels of the major air pollutants tracked by the EPA are: | higher / lower / about the same | lower (live) | EPA air-quality trends series | **L** |

### 4.7 Global and cross-cutting

| ID | Item | Options | Key (illustrative) | Source | Cut |
|----|------|---------|--------------------|--------|-----|
| B26 | Over the past ~30 years, the number of people worldwide living in extreme poverty has: | risen / fallen / stayed about the same | fallen (live) | World Bank, Poverty and Inequality Platform | **L** |
| B27 | The U.S. Constitution assigns the power to declare war to: | Congress / the President / the Supreme Court | Congress (fixed) | U.S. Constitution, Art. I §8 | **X** |
| B28 | Over the past ~100 years, the global rate of deaths from natural disasters has: | risen / fallen / stayed about the same | fallen (fixed) | EM-DAT international disaster database | **L** |

**`[PANEL]` adjudication flags.**

- **B17 — elevated risk of exclusion.** The item is sourced at tier (ii), to the consensus reviews, and is narrowed in this draft to the MMR vaccine because that is the claim those reviews directly address. In November 2025 a U.S. public-health agency revised its public page on the subject in a way that departs from them. Under the divergence rule (Document 9 §3.4) the item is therefore *suspended pending the panel's ruling* and stays in the instrument only if the panel is unanimous that its ground truth remains settled and documentable. If the panel is not unanimous, the item is cut. The instrument does not adjudicate the dispute.
- **B15** — the share is now at or slightly above its earlier peak, and the survey and census series differ by several tenths of a point. Confirm the band within which "about the same" is the key, or convert the item to a fixed window.
- **B12, B20** — confirm that the fixed windows (2020–21 against 2019; 2021 against 2019) are settled in the final published data.
- **B22** — confirm the consensus figure against current published studies; the bracket is deliberately coarse.
- **B07, B16, B30** — confirm the keys against the latest vintage before each freeze. For B30, several pollutants have risen since 2022 while remaining well below 1990 levels; confirm the wording survives that.
- **B26, B28, B29, B30** — confirm the cut codes; see §5.
- **B29, B30** — new in this draft; they have had no prior review.

---

## 5. Directional-balance ledger (the Document 9 §3.3 audit)

The mandatory balance check. Counts over the charged core (Table B, 30 items), by provisional cut code:

| Cut | Meaning | Items | Count |
|-----|---------|-------|-------|
| **R** | Challenges a right-leaning prior | B05, B11, B16, B19, B21, B22 | 6 |
| **L** | Challenges a left-leaning prior | B06, B12, B24, B26, B28, B29, B30 | 7 |
| **S** | Swing (incumbent-dependent; flips over time) | B01, B02, B03, B04 | 4 |
| **X** | Cross-partisan, or no stable partisan prior asserted | B07, B08, B09, B10, B13, B14, B15, B17, B18, B20, B23, B25, B27 | 13 |

**Reading.** As provisionally coded, the fixed-direction partisan items are near parity (6 R / 7 L). The 4 **S** items are the designated expressive-responding probes (Document 9 §4): their cut flips with the incumbent party, so over a full political cycle they contribute no net lean, and the gap between their belief-arm and incentivized-arm answers is expected to be the largest single contributor to $\textit{XP}$.

**The codes are hypotheses, and some are weak.** A cut code is a guess about which respondents hold a mistaken prior. Draft 1 treated the codes as settled; this draft does not. The R codes rest on comparatively well-documented asymmetries. The L codes are less secure: B26 and B28 concern long-run global trends on which pessimism is widespread across groups, and they may prove cross-partisan. If they do, the L side is short and the bank is rebalanced before freeze. Draft 1 also coded B20 and B23 as L without a defensible basis; both are now X.

**How the codes are tested.** Three checks apply, in order, and the later ones override the earlier.

1. *Panel.* The adjudication panel confirms or corrects each code by majority, recording dissent (Document 12 §2.4, criterion C5).
2. *Pilot.* A code stands only if the pilot shows the predicted group with the lower correct rate on that item — that is, if the sign of the measured gap $\hat\delta_k$ matches the code. An item whose gap is indistinguishable from zero is recoded X; an item whose gap has the opposite sign is recoded accordingly.
3. *Signed mean gap.* Balance is finally judged not by counting codes but by the signed mean gap $\bar\delta$ over the fixed-direction items, which must lie within the pre-registered tolerance of zero (Document 9 §3.3; Document 11 §6). Counting codes is the design aid; the signed mean gap is the test.

> **Balance is enforced per wave, not just per bank.** Because live keys can change, this ledger is re-run at each wave's adjudication using that wave's keys, and the signed mean gap is recomputed from that wave's data; both are recorded with the release (Document 4 §9). A wave outside tolerance is rebalanced by rotating-pool substitution before the FCR is reported. This per-wave audit is a pre-registered step (Document 11 §7.4).

---

## 6. Items considered and **rejected** (and why)

Recording rejections is part of the discipline — it shows the balance and ground-truth rules doing real work, and it documents the boundary of the instrument.

| Candidate | Reason for rejection |
|-----------|----------------------|
| Share of police killings involving unarmed victims, by race | Ground-truth estimates are method-dependent and genuinely contested; fails the "settled, documentable" rule (Document 9 §3.4). |
| Monthly southern-border encounter counts | Authoritative but highly volatile and politically hot; better suited to the rotating pool with careful framing than to the fixed core. |
| "Did policy X cause outcome Y" (any) | Causal attribution, not a settled fact; excluded by rule (Document 9 §3.3, rule 1). |
| Whether a given figure is "too high/too low" | Normative; excluded by rule. |
| Human–dinosaur coexistence / age of the Earth | Settled scientifically but entangled with religious identity in a way that measures group membership more than factual belief; held for pretest evaluation only. |
| Net employment effect of the minimum wage | Genuine scholarly disagreement on magnitude/sign; not settled. |
| U.S. life expectancy, "most recent year" against 2014 *(draft 1's B20)* | The key was live, not fixed: it read "lower" when drafted and had already been overturned by the 2024 figure, a record high. Replaced by a closed window. The lesson generalizes — an open-ended comparison is a live item and must be labeled and adjudicated as one. |
| "Childhood vaccines on the recommended schedule cause autism" *(draft 1's B17)* | Broader than the claim the consensus reviews directly address; narrowed to the MMR vaccine. |

---

## 7. Wave-adjudication protocol for live and wave-set items

For every item whose key is live or wave-set:

1. At wave open, retrieve the named source at a **frozen date**; record provider, series, vintage, retrieval date (Document 4 §9).
2. Set the wave's **key** from that figure (e.g., the sign of the 12-month change), applying a pre-registered **dead-band** so that small, within-revision movements are coded "about the same" rather than forced to a direction (the dead-band is fixed in Document 11 §6).
3. Re-run the balance ledger (§5) on the realized keys; rebalance via the rotating pool if needed.
4. Archive the frozen key and source with the wave release.

This keeps the *question* stable for longitudinal comparability while keeping the *truth* current and auditable.

---

## 8. Item metadata schema (machine-readable bank)

Each item is stored with: `id`, `domain`, `class` (anchor / charged), `format` (directional / magnitude / categorical / true-false), `stem`, `options[]`, `key_type` (fixed / live / wave-set), `key` (or `key_rule` for live and wave-set items), `source` (provider, series, tier, URL, retrieval_date), `cut` and `cut_status` (provisional / panel-confirmed / pilot-validated), `difficulty` (measured correct rate, once available), `core` (bool), `wave_first_used`, `version`, `pretest_status`, `panel_status`, `notes`. The schema is the unit of the frozen instrument hash (Document 11 §11).

---

## 9. Embargo, release, and versioning

- **Anchor core published.** This document (the anchor core and its ground-truth sources) is published with the instrument, per Document 4 §9, so external critics can challenge any item's ground truth directly.
- **Rotating pool embargoed.** Rotating-pool items are withheld until after their wave is fielded, then released, to preserve the priming/coaching guard (Document 9 §3.2). A small **dark subset** of rotating items is held back longer as a Goodhart tripwire (Document 9 §9).
- **Versioning.** The bank is versioned; v1.0 is the *draft for adjudication*, of which this is draft 2. The frozen instrument used for fielding will be a later tagged version (v1.1 or later) carrying the panel and pretest sign-offs. Index versions tie to instrument versions (Document 4 §9).

---

## 10. Adjudication and pretest checklist (the path to freeze)

Before the bank is frozen for fielding (Document 9 §11 stage 1 → stage 2) — full procedures and templates in **Document 12**:

- [ ] Panel confirms each item's ground truth is settled and documentable; resolves every `[PANEL]` flag; excludes any item it cannot agree is settled.
- [ ] Panel confirms or corrects each cut code and signs off on the directional-balance ledger (§5) and the dead-band (§7).
- [ ] Cognitive pretest (think-aloud) on the full core for comprehension, cueing, and answerability; cut or rewrite items that load on reading level or partisanship rather than factual belief (Document 9 §3.5).
- [ ] Pilot wave (Document 9 §11 stage 2) validates the cut codes and the signed mean gap; measures the anchor difficulty bands and confirms they overlap the charged items'; and confirms the neutral-anchor noise floor is low and that charged-core gaps exceed it (the H-FCR1 precondition, Document 11 §7.1).
- [ ] Freeze: tag instrument version, compute the instrument hash, register alongside the pre-analysis plan (Document 11).

---

## 11. Reconciliation record

All of the following have been applied.

- **Document 8:** Phase B1 tracks FCR Stage 1 with this bank as its instrument half.
- **Document 11 (pre-analysis plan):** references this bank by table and item ID and uses the §5 ledger and §7 dead-band; the two documents are frozen together.
- **Document 7 (lexicon):** the instrument vocabulary (anchor core, charged core, rotating pool, cut code, directional-balance ledger, dead-band, dark subset) is entered in §4.3 and §4.5.

---

## 12. Revision log

| Draft | Date | Change | Reason |
|-------|------|--------|--------|
| 1 | June 2026 | First draft: 10 neutral anchors, 28 charged items | — |
| 2 | November 2026 | B20 replaced by a fixed window (2021 against 2019) and recoded L → X | Its key ("lower" than 2014) was already false when drafted: the 2024 figure is a record high. No defensible partisan cut. |
| 2 | November 2026 | B17 narrowed to the MMR vaccine; sourced at tier (ii) only; suspended pending the panel | One of its two named sources no longer supports the key; the reviews address MMR specifically |
| 2 | November 2026 | B23 recoded L → X | No stable partisan prior could be asserted |
| 2 | November 2026 | B29 and B30 added (L) | Restores the L side with items that have statistical-series sources |
| 2 | November 2026 | A09 options no longer show the computed values | The item gave away its own answer |
| 2 | November 2026 | A11–A16 added; anchors given difficulty bands | The noise floor must be difficulty-matched to the charged items |
| 2 | November 2026 | Keys typed fixed / live / wave-set; cut codes declared provisional and given an empirical test | Draft 1 mislabeled a live key as fixed and treated guesses as facts |
| 2 | November 2026 | Internal references to the ledger corrected (§5, not §4) | Wrong section numbers |

---

*Draft instrument, not frozen. Cite with caution. All keys are illustrative; no item has been fielded and no FCR exists. The charged items are enumerated here, in the instrument document, and deliberately not in the canon (Document 9 §3.1). Construction and rules: Document 9 §2–§5. Analysis: Document 11. Procedures to freeze: Document 12. Release discipline: Document 4 §9.*
