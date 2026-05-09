# CS C124 — Problem Set 2

GWAS and ridge regression assignment.

## Layout

```
CS_C124_PS2_Template.ipynb   # all problem-set code
ps2_data/
  Q2_data/                    # gwas.geno, gwas.pheno
  Q3_data/                    # ridge.training.{geno,pheno}, ridge.test.{geno,pheno}
ps2_results/
  Q2_data/                    # GWAS results CSV + Manhattan / QQ / histogram / boxplot PNGs
  Q3_data/                    # ridge MSE results CSV + MSE vs λ plot
```

## Q2 — GWAS

Single-SNP linear regression (statsmodels OLS) of each phenotype on each SNP. Outputs:
- `gwas_results.csv` — per-(phenotype, SNP) coefficients, SEs, t-stats, p-values, Bonferroni flag
- `manhattan_plots.png`, `qq_plots.png`, `pvalue_histograms.png`, `genotype_phenotype_boxplots.png`

## Q3 — Ridge regression

Closed-form ridge `β = (XᵀX + λI)⁻¹ Xᵀy` fit on training data, evaluated on held-out test data for λ ∈ {0.001, 2, 5, 8}. Outputs:
- `ridge_results.csv` — train/test MSE per λ
- `ridge_mse_vs_lambda.png`

## Running

Open `CS_C124_PS2_Template.ipynb` in Jupyter and run cells top-to-bottom. Requires `numpy`, `pandas`, `matplotlib`, `statsmodels`.
