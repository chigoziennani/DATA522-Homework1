# Homework 1 - DATA 522: Practical Deep Learning Systems

Binary classification of electrocatalyst quality from electrochemical experiment data using a Random Forest classifier.

## Overview

This assignment uses data from ~500 automated electrochemical experiments. Each experiment has 11 input variables (element concentrations V, Cr, Mg, Fe, Co, Ni, Cu, S, Se, P, plus Voltage and Time) and an overpotential η. **Good** catalysts are defined as those with |η| < 0.6; the rest are **bad**. The notebook trains a Random Forest to predict good vs bad catalysts and reports precision, recall, F1, hyperparameter tuning, and permutation feature importance.

## Repository Contents

| File | Description |
|------|-------------|
| `homework1.ipynb` | Jupyter notebook with all code (data prep, visualization, split, modeling, PFI). |
| `ExerciseData.csv` | Experiment data (features + overpotential). |
| `documentation.pdf` | 2-page write-up: design, results, and discussion. |
| `Homework 1.pdf` | Assignment handout. |

## Requirements

- **Python** 3.8+
- **Libraries:** `pandas`, `numpy`, `matplotlib`, `scikit-learn`

Install with:

```bash
pip install pandas numpy matplotlib scikit-learn
```

## How to Run

1. Clone the repo and open the project folder.
2. Start Jupyter: `jupyter notebook` or open `homework1.ipynb` in VS Code / Cursor.
3. Run all cells from top to bottom (kernel → Restart & Run All).  
   The notebook expects `ExerciseData.csv` in the same directory.

## Assignment Structure (in the notebook)

- **1.1** — Visualize overpotential in 11D space (PCA to 2D, coloured by |η|).
- **1.2** — Train/validation/test split (70% / 15% / 15%).
- **1.3** — Percentage of good vs bad catalysts in the dataset.
- **1.4** — Default Random Forest; precision, recall, F1 on train/val/test.
- **1.5** — Hyperparameter tuning (4 combinations); metrics table.
- **1.6** — Permutation feature importance with and without normalization; top 5 variables.
