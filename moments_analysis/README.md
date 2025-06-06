# Moments analysis steps

This folder contains the scripts for Moments demographic analysis.

## Snakemake Pipeline

The Moments inferences is automated using Snakemake. The pipeline includes the following steps:

1. Fit Moments models using `fit_moments.py`.
2. Compute residual statistics using `compute_residuals.py`.
3. Identify potential clade structure using `find_clades.py`.
3. Postprocess results using `postprocess_results.py`.
4. Plot the full SFS using `plot_moments_SFS_full.py`.
5. Generate diagnostic plots using `plot_moments_results.py`.

The pipeline is defined in the `Snakefile` and can be executed by running:
```sh
snakemake -j <number_of_jobs>
```

## Population-specific SNV analysis
- `plot_private_SNVs.py` contains codes for computing the probabilities of observing population-specific (or private) SNVs in the data. The script also generates a plot comparing a null free migration scenario with the fitted Moments model.
- `plot_private_SNVs_model.py` plots the predicted private SNV probabilities for simulated demographic models.