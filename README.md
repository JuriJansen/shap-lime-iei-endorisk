# SHAP, LIME and IEI on a Clinical Bayesian Network

Bachelor Thesis, Juri Jansen s1096620, Radboud University

Comparing 2 model-agnostic explainers (SHAP, LIME) with a BN-native method (Incremental Explanation of Inference, IEI) applied to the ENDORISK BN for preoperative lymph node metastasis (LNM) risk stratification in endometrial cancer.

## Structure of the repository
```
ImplementationENDORISK.ipynb   — runs SHAP, LIME and IEI; writes output/seed_*/
EvaluationsENDORISK.ipynb      — loads output/ computes metrics and produces all figures
output/
  seed_42/ … seed_46/          — per-seed explanation CSVs (pre computed)
  figures/                     — all thesis figures
  *.csv                        — aggregated metrics
```


## Setup
Python 3.13 is required.

## Running order
(1) Open and run 'ImplementationENDORISK.ipynb' -> this generates results stored in output/seed_*/
(2) Open and run 'EvaluationsENDORISK.ipynb' -> Loads the .csvs and produces the metrics and figures. Can be run without step (1), since /output/ is included already.

## Model

The ENDORISK BN ('endomcancer.bif') encodes the structure and CPTs published in:

> Reijnen, C., et al. (2020). Preoperative risk stratification in endometrial cancer (ENDORISK) by a Bayesian network: A multicenter prospective cohort study. *Gynecologic Oncology*, 160(1), 207–214. https://doi.org/10.1016/j.ygyno.2020.10.020

## Other key references
- Lundberg & Lee (2017) — SHAP: A Unified Approach to Interpreting Model Predictions
- Ribeiro et al. (2016) — LIME: "Why Should I Trust You?"
- Kyrimi et al. (2020) — IEI: An Incremental Explanation of Inference in Bayesian Networks
- Parimbelli et al. (2023) — Evaluation metrics (fidelity, identity, separability)
- Krishna et al. (2022) — The Disagreement Problem in XAI
