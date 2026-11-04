# test
# COAST Steering on PushT

This repository contains the implementation and experimental results of activation steering methods applied to a pretrained state-based Diffusion Policy on the PushT benchmark.

The project compares two steering approaches:

- **Difference-in-Means (DiM)** — steering using the difference between mean activations of successful and failed episodes.
- **COAST-style steering** — steering based on contrastive conceptors estimated from activation covariance matrices.

## Repository Structure

```text
.
├── COAST_PushT.ipynb
├── Report_COAST_PushT.pdf
├── README.md
│
├── config/
│   └── metadata.json
│
├── baseline/
│   ├── results_baseline.pkl
│   └── baseline_test_*.pkl
│
└── steering/
    ├── steering_train_act_*.pkl
    ├── results_mean_steering.pkl
    └── results_coast.pkl
```
# Project Structure

- **`COAST_PushT.ipynb`** — main notebook with experimental code.
- **`Report_COAST_PushT.pdf`** — research report with methodology and results.
- **`config/metadata.json`** — experiment configuration and metadata.
- **`baseline/`** — baseline evaluation results and test episode data.
- **`steering/`** — training activations and evaluation results for DiM and COAST methods.
- **`README.md`** — project overview and file descriptions.
