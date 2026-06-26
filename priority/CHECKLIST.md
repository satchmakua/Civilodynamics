# Stage C0 Execution Checklist — Establish Priority and Presence

These are the **account-gated** steps that require your accounts, payment, or
identity — the parts an assistant cannot do for you. The in-repo artifacts they
depend on (web flag, citation metadata, license, deposit packet) are already
drafted. Metadata to paste is in [`DEPOSIT.md`](DEPOSIT.md).

Ordered for fastest priority-flag first.

---

## 1. Citable DOI via Zenodo  ⟶  *do this first (same-day)*
- [ ] Create/log in to a [Zenodo](https://zenodo.org) account (ORCID login is convenient).
- [ ] Register a free [ORCID](https://orcid.org) iD if you don't have one; paste it into
      `CITATION.cff` and `priority/DEPOSIT.md`.
- [ ] In Zenodo, enable the **GitHub integration** and flip the switch on the
      `satchmakua/Civilodynamics` repository.
- [ ] In GitHub, **create a release** (e.g., tag `v2026.06`). Zenodo auto-archives it
      and mints a DOI.
- [ ] Copy the **DOI** into: `CITATION.cff` (`doi:` line), `index.html` (replace the
      "DOI pending" placeholder), and the repo README if one is added.
- [ ] Confirm Zenodo metadata matches `DEPOSIT.md` §1 (license = CC BY 4.0, keywords, abstract §2a).

## 2. Web flag live via GitHub Pages  ⟶  *free, no domain needed yet*
- [ ] Repo **Settings → Pages → Source: deploy from `main` / root**. `index.html` is served at
      `https://satchmakua.github.io/Civilodynamics/`.
- [ ] Verify the page loads and the GitHub links resolve.
- [ ] (After step 4) point the custom domain at Pages and add a `CNAME` file.

## 3. arXiv deposit (Charter #1, Flagship #5)  ⟶  *files ready*
- [x] Submission files generated in [`arxiv/`](arxiv/): `.pdf` (verified, 10 + 11 pp) and
      `.tex` (arXiv-preferred source; compile-test first). See [`arxiv/README.md`](arxiv/README.md).
- [ ] Create an [arXiv](https://arxiv.org) account; you may need an **endorsement** for
      `physics.soc-ph` on a first submission (request via the arXiv endorsement flow).
- [ ] Submit with categories from `DEPOSIT.md` §1 (primary `physics.soc-ph`, cross-list
      `q-bio.PE`) and abstracts §2b / §2c.
- [ ] Record the arXiv IDs back here and in the OSF project.

## 4. Secure the namespace  ⟶  *low cost, real downside if neglected*
- [ ] Register `civilodynamics.org` and `civilodynamics.com` (any reputable registrar).
- [ ] Update the contact address in `index.html` from the placeholder to
      `contact@civilodynamics.org` once email is set up.
- [ ] Claim the handle `@civilodynamics` (or closest) on the platforms you'll use.
- [ ] Create and hold `r/Civilodynamics` on Reddit.

## 5. Working-paper repository via OSF
- [ ] Create an [OSF](https://osf.io) project "Civilodynamics" (description = `DEPOSIT.md` §2a).
- [ ] Add components for the corpus and for building-phase work; link the GitHub repo and the Zenodo DOI.
- [ ] This is also where the **FCR pre-analysis plan (Document 11)** gets its timestamped
      registration when it is frozen (Document 11 §0, §11) — register it here, not just deposit it.

---

## What stays with the assistant (paper-stage, on request)
- Convert Charter (#1) and Flagship (#5) to submission-grade PDF for arXiv.
- Draft a repo `README.md` landing section (currently the corpus has none).
- Draft the adjudication-panel rubric and cognitive-pretest protocol (B1 Stage-1 freeze prerequisites).

## Done = priority established
When steps 1–2 are complete you have a **permanent, citable, dated record with your
name on it** and a public flag — the whole point of Stage C0 — at zero or near-zero
cost, with no predictive claim made. Steps 3–5 broaden reach and can follow.
