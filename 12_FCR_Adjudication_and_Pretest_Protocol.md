# Civilodynamics — Factual Consensus Rate: Adjudication Rubric and Cognitive-Pretest Protocol

**Building-Phase Document 12 · Freeze-Gating Procedures v1.1 · June 2026, revised November 2026**
**Stage-1 (path-to-freeze) of Document 9 §11 · Satchel Hamilton · Civilodynamics Initiative**

> **Status and role.** This document is the **procedural package that takes the FCR instrument from draft to frozen**. The item bank (Document 10) is explicitly a *draft for adjudication*; the two gates it must pass before freeze — multi-perspective **ground-truth adjudication** and **cognitive pretesting** — are specified in Document 9 §3.4–§3.5 and listed in the Document 10 §10 path-to-freeze checklist. This document operationalizes both into runnable protocols with usable templates.
>
> **What it does and does not require.** The protocols are fully specified here (paper stage, no funding). **Executing** them requires people: a convened adjudication panel and a handful of pretest participants. Until both gates are passed there is no frozen instrument and no pre-registration deposit (Document 11). Construction and rules defer to Documents 9 and 10; nothing here changes the canon.

---

## 1. Where this sits — the freeze gate

```
Document 10 (item bank, draft v1.0)
        │
        ├─ Gate A: Adjudication panel        (this doc §2)  → admitted/revised items + balance re-audit
        ├─ Gate B: Cognitive pretest         (this doc §3)  → comprehension/cueing fixes
        ▼
Instrument v1.1 (frozen) + hash  →  register Pre-Analysis Plan (Document 11) on OSF/AsPredicted
        ▼
Pilot wave (Document 9 §11, stage 2)
```

An item reaches the frozen instrument only if it **passes both gates**. Gate A tests whether the item is *admissible* (settled, sourced, balanced); Gate B tests whether it *works on real respondents* (understood as intended, free of cueing). The two are complementary and neither substitutes for the other.

---

## 2. Gate A — The adjudication panel

### 2.1 Purpose and principle
The deepest validity threat to an FCR is "who decides what is a fact" (Document 9 §3.4). The answer is **not** the instrument-builder's judgment; it is the agreement of a panel that spans perspectives, under a rule that an item survives **only if people across the spectrum agree its ground truth is settled**. Cross-perspective unanimity *on settledness* is what converts "the author's facts" into "shared facts."

### 2.2 Composition (target 5–7 voting + 2 non-voting)
- **Voting (5–7):** at least 2 members with a declared left-of-center perspective, at least 2 with a declared right-of-center perspective, and at least 1 declared independent/center. The point of declared perspectives is not tokenism; it is that the unanimity-on-settledness rule (§2.5) is only meaningful if the panel actually contains the perspectives an item might be contested across.
- **Non-voting:** a **methodologist** (chair; survey-methods background) who runs process and rules on framing; a **professional fact-checker or research librarian** who verifies each item's source against the sourcing hierarchy.
- **Independence:** members are external where possible; the author may observe but does not vote.

### 2.3 Conflict-of-interest and integrity
Each member signs the COI declaration (§5.1): no financial, organizational, or advocacy stake in how any particular item resolves; recusal from any item where a stake exists. Deliberations and the per-item rationale are recorded. The panel's full ledger is published with the instrument (Document 4 §9) so the adjudication itself is auditable.

### 2.4 The per-item rubric
Each voting member scores each item on the criteria below; the chair and fact-checker complete C2. (Scoring sheet template in §5.2.)

| # | Criterion | Scale | Admit condition |
|---|-----------|-------|-----------------|
| C1 | Ground truth is **settled & documentable** | Settled / Contested / Not settled | **Unanimous "Settled"** (any "Contested/Not settled" → not admitted as-is) |
| C2 | Source meets the **sourcing hierarchy** (Document 9 §3.4) | Tier i statistical series / Tier ii scientific consensus / Tier iii public record / Inadequate | At least Tier iii, with an exact, frozen citation. An agency statement or web page is not a Tier i source |
| C3 | **Verifiable & checkable** — not values, prediction, or causal attribution | Pass / Fail | Pass |
| C4 | **Neutral wording** — no partisan cue or loaded framing | Neutral / Mild cue / Loaded | Neutral (Mild → revise; Loaded → reject) |
| C5 | **Directional cut** (R / L / S / X) confirmed or corrected | record code | Majority agreement; dissent recorded. The code stays provisional until the pilot validates it (Document 10 §5) |
| C6 | **Answerability / reading level** | OK / Too hard / Ambiguous | OK |
| C7 | **Format** appropriate (directional / bracket / categorical / T-F) | OK / Revise | OK |

### 2.5 Decision rule
- **ADMIT** iff: C1 unanimous *Settled* **and** C2 ≥ Tier iii **and** C3 Pass **and** C4 Neutral **and** C6 OK **and** C7 OK.
- **REVISE (one round)** if the only failures are C4 *Mild cue*, C6 *Ambiguous*, or C7 *Revise*: the chair edits, the item returns for one re-vote.
- **REJECT** otherwise — recorded in the rejected-items register (Document 10 §6) with rationale.
- **Contestedness disqualifies** (Document 9 §3.4): a single credible "Contested" on C1, sustained after discussion, removes the item. This is deliberate: it is better to exclude a true-but-contested item than to let the instrument adjudicate a live dispute.
- **Divergence returns an item to the panel** (Document 9 §3.4). If an official source and the scientific-consensus tier come to diverge on an item — before or after admission — the item is suspended and voted again under C1, and it re-enters only on a unanimous *Settled*. One item in the draft bank is already in this position (Document 10 §4, B17).

### 2.6 Live-series keys and dead-bands
For S and live-series items the panel additionally ratifies, once: the named series and retrieval rule, and the **dead-band** width per series (Document 10 §7; Document 11 §6). Per-wave key-setting thereafter follows that ratified rule and does not return to the full panel.

### 2.7 Outputs
1. **Adjudication ledger:** every item → ADMIT / REVISE→outcome / REJECT, with source citation, cut code, and rationale (and any dissent).
2. **Balance re-audit:** re-run the Document 10 §5 directional-balance ledger over the *admitted* set; if a net lean appears, rebalance by promoting reserve items or adjusting the rotating-pool plan **before** freeze. This audits the codes only. The empirical test of balance — the signed mean gap — can be run only on data and follows in the pilot (Document 11 §6).
3. **Sign-off:** chair certifies the gate passed; the admitted set becomes the candidate frozen core.

---

## 3. Gate B — Cognitive pretest

### 3.1 Purpose
Adjudication establishes that an item is *admissible*; cognitive pretesting establishes that respondents *read it as intended and answer on belief, not cue* (Document 9 §3.5). An item can be impeccably sourced and still fail here — e.g., wording that telegraphs the "right" answer, or a frame that activates identity rather than recall.

### 3.2 Method and sample
- **Technique:** semi-structured **cognitive interviews** using concurrent and retrospective **think-aloud**, probing the four stages of survey response (comprehension → retrieval → judgment → response).
- **Sample:** 9–15 participants, quota-balanced across partisanship and spanning education and age; **two iterative rounds** (revise the bank between rounds, then re-test the revised items).
- **Administration:** items presented in the fielding format (including the "Not sure" option and, for a subset, the incentivized framing) so the pretest reflects the real instrument.

### 3.3 Per-item probe script (the interview)
For each item, after the participant answers:
1. **Comprehension:** "In your own words, what is this question asking?"
2. **Retrieval/judgment:** "How did you arrive at your answer?"
3. **Cueing check:** "Was there anything in the wording that hinted at a 'correct' or expected answer?"
4. **Partisan-slant check:** "Did the question feel slanted toward one political side?"
5. **Uncertainty:** "How sure were you? When would you choose 'Not sure'?"
6. **Format:** for directional/bracket items — "Were the answer options clear and complete?"

### 3.4 Coding and decision rules
An item is **revised or cut** if any holds:
- **Comprehension drift:** participants systematically read it differently than intended.
- **Detected cue/slant:** participants identify an expected answer or a partisan lean (a C4 failure surfacing only in practice).
- **Unanswerable:** it requires specialist knowledge beyond the construct (it measures expertise, not the shared commons).
- **Identity loading:** it elicits group-signaling rather than belief reporting (the expressive-responding confound at the wording level; Document 9 §4).
Revised items re-enter Gate A if the edit touches C1–C4; cosmetic edits do not.

### 3.5 Output
A **pretest report** (per-item findings + edits) producing **bank v1.1**: the items that passed both gates, in final wording.

---

## 4. The freeze gate

1. Compile the items passing **both** gates → instrument **v1.1**.
2. Run the final balance re-audit (§2.7) on v1.1.
3. Compute and record the **instrument hash** (Document 10 §8; Document 11 §11).
4. **Register** the Pre-Analysis Plan (Document 11) **with the hash** on OSF/AsPredicted — this is both the pre-registration and a Stage-C0 priority timestamp (Document 8 §C0).
5. Proceed to the **pilot wave** (Document 9 §11, stage 2), which validates the cut codes and the signed mean gap, measures the difficulty of the neutral anchors against the charged items, re-anchors $\theta$, the balance tolerance, and the dead-bands to measured values, and confirms the anchor noise floor sits below charged-core gaps (the H-FCR1 precondition, Document 11 §7.1).

After step 4 the design and the instrument are **locked**. The pilot's calibrations, and any item replacements it forces, are registered together as one dated amendment, with the instrument re-tagged, before the first tracker wave (Document 11 §13). From then on changes follow the amendment protocol (Document 11 §12).

---

## 5. Templates

### 5.1 Conflict-of-interest declaration (panelist)
> *I, [name], serving on the FCR adjudication panel, declare: (a) my general perspective for the record [left / center / right / other]; (b) any financial, organizational, or advocacy interest that could be served by how a particular item resolves [list or "none"]; (c) that I will recuse from any item where such an interest exists; (d) that I will judge each item solely on whether its ground truth is settled and documentable, not on whether I find the fact congenial. Signed / dated.*

### 5.2 Adjudication scoring sheet (one row per item; member completes C1, C3–C7; chair/fact-checker complete C2)
| Item ID | C1 settled? | C2 source tier + citation | C3 checkable? | C4 wording | C5 cut | C6 answerable? | C7 format | Vote (admit/revise/reject) | Notes |
|---------|-------------|---------------------------|---------------|------------|--------|----------------|-----------|----------------------------|-------|
| | | | | | | | | | |

### 5.3 Cognitive-interview record (one per participant per item)
| Item ID | Answer given | Comprehension (paraphrase) | Cue/slant detected? | Basis of answer | "Not sure" reasoning | Coder flag (keep/revise/cut) |
|---------|--------------|----------------------------|---------------------|-----------------|----------------------|------------------------------|
| | | | | | | |

---

## 6. Reconciliation record

All of the following have been applied.

- **Document 8:** Phase B1 Stage 1 records these procedures as drafted; what remains is execution — convene the panel, run adjudication, run the two pretest rounds, then freeze and register.
- **Document 10:** its §10 path-to-freeze checklist cross-references this document for the procedures.
- **Document 11:** its §13 timeline gates freeze and registration on §4 here.
- **Document 7 (lexicon):** *adjudication panel*, *cognitive pretest*, and *freeze gate* are entered under the FCR cluster (§4.3).

## 7. Revision log

| Version | Date | Change | Reason |
|---------|------|--------|--------|
| 1.0 | June 2026 | First version | — |
| 1.1 | November 2026 | C2 states that agency statements are not Tier i sources; divergence rule added to §2.5 | Follows the sourcing-hierarchy correction in Document 9 §3.4 |
| 1.1 | November 2026 | C5 codes declared provisional until the pilot; §2.7 and §4 distinguish the audit of codes from the empirical balance test | Cut codes are hypotheses about respondents (Document 10 §5) |
| 1.1 | November 2026 | §4 states the two lock points (freeze, then one post-pilot amendment) | The pilot calibrates and may replace items after the freeze |

---

*Procedural specification. Cite with caution. The protocols are fully specified but unexecuted; no panel has been convened and no pretest run, so the Document 10 bank remains a draft and no FCR instrument is frozen. Procedures: Document 9 §3.4–§3.5; instrument: Document 10; analysis to be registered at freeze: Document 11.*
