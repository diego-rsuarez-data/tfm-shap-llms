# Prefix Reuse SHAP

This repository contains the notebooks developed for a Master's Thesis on
token-level explainability in autoregressive language models.

The project studies how prompt tokens contribute to the prediction of a fixed
target token using Leave-One-Out attribution, prefix-based analysis, permutation
SHAP, and efficient SHAP evaluation strategies.

## Notebooks

The notebooks should be read in the following order:

1. `01_leave_one_out_next_token_attribution.ipynb`  
   Basic Leave-One-Out attribution for next-token prediction.

2. `02_prefix_based_leave_one_out.ipynb`  
   Prefix-based Leave-One-Out analysis for autoregressive language models.

3. `03_permutation_shap_next_token_prediction.ipynb`  
   Permutation SHAP for next-token prediction.

4. `04_efficient_permutation_shap.ipynb`  
   Efficient permutation SHAP using caching, batching, and prefix reuse.

## Structure

```text
tfm-shap-llms/
│
├── README.md
├── requirements.txt
├── .gitignore
│
└── notebooks/
    ├── 01_leave_one_out_next_token_attribution.ipynb
    ├── 02_prefix_based_leave_one_out.ipynb
    ├── 03_permutation_shap_next_token_prediction.ipynb
    └── 04_efficient_permutation_shap.ipynb
```

## Installation

Create a virtual environment:

```bash
python -m venv .venv
```

Activate it.

On Windows:

```bash
.venv\Scripts\activate
```

On Linux/macOS:

```bash
source .venv/bin/activate
```

Install the dependencies:

```bash
pip install -r requirements.txt
```

## Notes

The experiments use small autoregressive language models from Hugging Face.
GPU execution is recommended for the SHAP experiments involving multiple
permutations.

The notebooks keep selected outputs and figures to make the results readable
without re-running all cells.

This repository is intended for academic and experimental use.
