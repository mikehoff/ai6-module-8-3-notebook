# AI6 Module 8.3 hands-on notebook (our hosted copy)

Self-contained, version-pinned copy of the Module 8.3 Lesson 3 practice notebook for the AI6 (Applied AI Engineering) programme.

## Contents

- `model_quality_practice_corndel.ipynb`: the learner notebook. Open in Google Colab.
- `requirements.txt`: the tested dependency set (informational; the notebook installs these itself).
- `LICENSE`: Apache License 2.0, retained from the upstream project.

## Attribution

Adapted from the [Evidently AI ML Observability Course](https://github.com/evidentlyai/ml_observability_course), module 5, copyright Evidently AI, used under the Apache License 2.0.

## Changes from the upstream notebook

1. A setup cell installs pinned versions: evidently 0.4.19, numpy 1.26.4, pandas 2.1.4, scikit-learn 1.3.2. The upstream notebook relied on whatever versions the runtime happened to have, which caused intermittent failures as Colab images changed.
2. A verification cell writes the `utils.py` feature engineering helper directly and checks installed versions against the tested set, with restart instructions on mismatch. This removes the need to clone the upstream repository.
3. The model is trained fresh in the notebook rather than loaded from `model2.pckl`. The upstream file is stored with Git LFS, so a plain clone yields a 14 byte pointer file rather than the model, and unpickling across scikit-learn versions is fragile in any case. Training takes a few seconds.

## Verification record

Executed end to end with zero errors on Python 3.12 under the pinned versions on 10 June 2026 (dataset download stubbed in the test container; Colab fetches it from OpenML directly). Re-verify from a fresh Colab runtime before changing the link given to learners.
