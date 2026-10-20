# Daniel González · `SleepyKomodo`

**Computational biologist who builds and evaluates the models — cluster-aware splits, bootstrap CIs, published negative results.**

Ph.D. in bioinformatics (University of Tokyo), M.Sc. in AI & Data Science, B.Sc. in software engineering. Currently a postdoc at Tecnológico de Monterrey with DTU BRIGHT, engineering *Bacillus subtilis* for recombinant protein production on agro-industrial side streams — through December 2026.

I train models and, more to the point, build the evaluations that decide whether they actually work. Twice now I have published benchmarks where **my own model lost**, with the confidence intervals to show the comparison was fair.

---

### Public work

| | |
|---|---|
| **[bio-ml-eval-protocols](https://github.com/GDanielGzz/bio-ml-eval-protocols)** | An opinionated, runnable standard for evaluating biological ML. Three documents plus `bioeval`, a package that enforces them — group-aware splits, leakage auditing, cluster-aware BCa bootstrap, paired head-to-head tests. 66 tests, CI on Python 3.10–3.12. The demo reproduces homology leakage from scratch in ten seconds: **+11.8 AUC of pure inflation**, and an error bar five times too narrow. |
| **[amp-classifier](https://github.com/GDanielGzz/amp-classifier)** · [live demo](https://huggingface.co/spaces/SleepyKomodo/amp-classifier) | Antimicrobial-peptide classifier on mmseqs2 cluster-aware splits at 40% identity. Frozen ESM2-650M + MLP beats a 428-feature XGBoost baseline at **AUC 0.919 [0.906–0.931] vs 0.864**, non-overlapping bootstrap CIs on both AUC and MCC. CI on Python 3.11–3.13. |
| **[crispr-designer](https://github.com/GDanielGzz/crispr-designer)** | sgRNA efficiency scoring. Reproduced the Rule Set 2 baseline (ρ +0.459 [+0.389, +0.527]), then ran a transformer head-to-head on identical splits: **tied** on mammalian data, **cleanly beaten** on a 33,743-guide bacterial corpus. Published as a negative result. |
| **[ale-outcome-predictor](https://github.com/GDanielGzz/ale-outcome-predictor)** | Predicts which genes mutate under adaptive laboratory evolution, fusing genome-scale-model flux features with ESM2 embeddings. The fusion wins in **73% of random seeds** — reported as the seed distribution, not the best run. Tests and CI on Python 3.10–3.12. |
| **[foldit-lite](https://github.com/GDanielGzz/foldit-lite)** | Browser puzzle game with live ESMFold structure prediction. The interesting part is latency: an async warm queue hides 3–15 s of inference behind instant interaction. 111 backend tests with ESMFold stubbed out; CI builds and lints the frontend. |

Also: a production Windows appraisal application in daily use by practising appraisers in Monterrey (~7,400 LOC, 1,872 LOC of tests), a literature platform that scores study quality against CONSORT/STROBE/PRISMA, and a bioprocess simulator with Wright–Fisher and Luria–Delbrück evolution engines.

---

### How I work

- **Leakage-free splits or the number means nothing.** Cluster-aware at the identity threshold that matters for the data, audited in CI.
- **Intervals, not point estimates.** Bootstrap CIs on every reported metric; resample the unit the split respected.
- **Reproduce the baseline before claiming to beat it.**
- **A tie is a tie.** If the paired difference contains zero, that is what gets written down.
- **Negative results ship.** The file drawer is expensive.

---

### Elsewhere

[Portfolio](https://gdanielgzz.github.io/) · [Hugging Face](https://huggingface.co/SleepyKomodo) · [ORCID](https://orcid.org/0009-0002-1737-276X) · sleepy.komodo@protonmail.com

Three peer-reviewed publications in computational plant science; root-architecture parameters contributed upstream to [OpenSimRoot](https://rootmodels.gitlab.io/). Lead-author manuscript in preparation.

English · Español · Deutsch (C1) · 日本語 (N2–N3)
