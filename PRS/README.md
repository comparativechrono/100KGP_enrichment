
# Polygenic Risk Score Analysis

This directory contains scripts for calculating and analyzing polygenic risk scores (PRS) from 100KGP genetic variant data. The scripts are provided in both R and Python to accommodate different users' preferences and environments. These scripts calculate individual PRS based on variant weights and aggregate these scores for further statistical analysis.

## Contents

- `case_control_PRS_tidy_R.ipynb`: R notebook for PRS calculation and analysis using tidyverse.
- `case_control_PRS_base_R.ipynb`: R notebook for PRS calculation and analysis using base R.
- `case_control_PRS_Python.ipynb`: Python notebook for PRS calculation and analysis.
- `variant_weights.txt`: Example file containing variant IDs and their associated weights.
- `cases.txt`: Example file representing case samples with genetic variant information.
- `controls.txt`: Example file representing control samples with genetic variant information.

## Prerequisites

### For tidy R

- R (version 3.6 or newer)
- Packages: `dplyr`, `purrr`

Install the required packages using:

```R
install.packages(c("dplyr", "purrr"))
```

### For Python

- Python (version 3.6 or newer)
- Packages: `pandas`, `scipy`

Install the required packages using:

```bash
pip install pandas scipy
```

## Usage

To open the notebook in Colab click on the open in Colab button at the top of each notebook.


## Input Files

- `variant_weights.txt`: This file should contain two columns: variant ID and weight, separated by a tab. Each line corresponds to a variant and its associated weight in the PRS calculation.
- `cases.txt` and `controls.txt`: These files should contain the genetic variant data for case and control groups, respectively. The format should match the output of `bcftools query`, with columns for Sample ID, Chromosome, Position, Variant ID, Reference Allele, Alternate Allele, Quality, Filter, Genotype (GT), Genotype Quality (GQ), and Depth of Coverage (DP).

## Output

The scripts output CSV files with the aggregated PRS for each individual in the cases and controls groups, as well as a summary statistics file containing the mean and standard deviation of the PRS for both groups.

## Example

Example input files are provided in the repository to demonstrate the expected formats and facilitate testing of the scripts.
