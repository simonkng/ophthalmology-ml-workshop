# Programming in Ophthalmology - Online Workshop

Hands-on notebooks and slides for the online workshop series *Programming in Ophthalmology*
(Dr. Simon König). The material is written for **clinicians without programming experience**:
the slides explain a concept, the notebook lets you run it on real ophthalmic data.

**Data:** all notebooks in this repository use the openly available **Harvard-GDP** glaucoma dataset
(visual-field part, CC BY-NC-ND 4.0). The data are **downloaded automatically from their public source when you run the
notebook** - no data are stored in this repository.

## Contents

| Session | Topic | Notebook (click to run) | Slides |
|---|---|---|---|
| **1** (5 Nov 2026) | Python & Jupyter, loading / merging / cleaning tables, features and labels, patient-wise splits (data leakage), scaling, two interpretable models | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/simonkng/ophthalmology-ml-workshop/blob/main/notebooks/session1/Session1_Python_and_ML_Principles.ipynb) [Kaggle](https://kaggle.com/kernels/welcome?src=https://github.com/simonkng/ophthalmology-ml-workshop/blob/main/notebooks/session1/Session1_Python_and_ML_Principles.ipynb) | [PDF](slides/Session1_Python_and_ML_Principles_slides.pdf) |
| **2** (12 Nov 2026) | Recap; reading a model critically; checklist for your own analysis; "spot the flaw"; confusion matrix, ROC / AUC, cross-validation, bootstrapped confidence intervals | [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/simonkng/ophthalmology-ml-workshop/blob/main/notebooks/session2/Session2_Evaluating_and_Trusting_Results.ipynb) [Kaggle](https://kaggle.com/kernels/welcome?src=https://github.com/simonkng/ophthalmology-ml-workshop/blob/main/notebooks/session2/Session2_Evaluating_and_Trusting_Results.ipynb) | [PDF](slides/Session2_Reading_Models_and_Evaluating_Results_slides.pdf) |

Further sessions will be added here.

**One-page cheat sheet** (checklist, data handling, leakage, metrics, thresholds, reporting, red flags):
[cheatsheet/ML_cheatsheet_one_page.pdf](cheatsheet/ML_cheatsheet_one_page.pdf)

## How do I run a notebook?

Three options - **see [SETUP.md](SETUP.md) for step-by-step instructions**:

1. **Google Colab** (easiest, nothing to install, needs a Google account): click the *Open in Colab* badge above, then
   *Runtime → Run all*.
2. **Kaggle** (free account; internet must be switched on in the notebook settings).
3. **On your own computer** with Python and Jupyter.

## Contact

Dr. Simon König - <simon.koenig@unimedizin-mainz.de>

## License

Slides, notebooks and the cheat sheet (without the third-party data) are licensed under
**[Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)](LICENSE)** - © 2026 Dr. Simon König.
You may share and adapt them for non-commercial purposes with attribution. The **Harvard-GDP dataset is not part of this
repository and has its own license** (CC BY-NC-ND 4.0) - see below.

## Notes

- Teaching material only - the models are simplified examples, **not validated clinical tools**.
- The Harvard-GDP dataset: Luo Y, Shi M, Tian Y, Elze T, Wang M. *Harvard Glaucoma Detection and Progression: A Multimodal
  Multitask Dataset and Generalization-Reinforced Semi-Supervised Learning.* ICCV 2023.
  Source: <https://huggingface.co/datasets/harvardairobotics/Harvard-GDP> (license CC BY-NC-ND 4.0, non-commercial use).
  The data are not part of this repository and must not be redistributed.
- Follow-up visits in the notebooks are **simulated** for teaching (clearly marked in the notebooks).
