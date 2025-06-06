# IBS-tract analysis steps

This folder contains the code for the identity-by-state (IBS) tract analysis. 

## Analysis of real data
- The computation of IBS tracts between MAGs and L99 statistics is done by the Snakemake workflow in the `Snakefile`.
- `simulate_mutation_accumulation.py` takes the observed within-population IBS tracts and simulates the accumulation of neutral mutations to generate the expected distribution of IBS tracts between isolated populations.
- `infer_isolation_years.py` takes the results from the above step and infers the isolation years between populations using observed between-population L99 statistics.

## Analysis of simulated data
- `run_fastsimbac.sh` is a bash script that runs the [FastSimBac](https://bitbucket.org/nicofmay/fastsimbac/src/master/) simulations.
- `fastsimbac_helper.py` implements a helper class for handling the haplotype table generated by FastSimBac. The key functionality is the compute pairwise SNP profiles and IBS tracts between genomes / haplotypes.
- `fastsimbac_analysis.ipynb` contains code for analyzing the simulation results and performing the approximate simulation (mutation accumulation) on the fastsimbac data.