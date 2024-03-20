# 100KGP_enrichment
Enrichment analysis scripts for working on case control data in the 100KGP in a tidy vcf wide data format rather than aggregate data files

The main directory contains notebooks for performing enrichment analysis. The PRS subdirectory contains PRS calculations on the same input data.

# Allele Frequency Analysis

This directory contains Jupyter notebooks for performing allele frequency analysis on genetic variant data extracted from VCF files in a modified wide VCF, to make the whole data compliant with tidyverse long data format. The analysis calculates allele frequencies for each variant and performs Fisher's Exact Test to compare the frequencies between cases and controls. The repository includes both R and Python implementations.

## Contents

- `case_control_enrichment_with_R.ipynb`: A Jupyter notebook with the R kernel showcasing the allele frequency analysis workflow in tidy R.
- `case_control_enrichment_with_base_R.ipynb`: A Jupyter notebook with the R kernel showcasing the allele frequency analysis workflow in tidy R.
- `case_control_enrichment_with_python.ipynb`: A Jupyter notebook with the Python kernel demonstrating the allele frequency analysis workflow in Python.

## Prerequisites

Ensure you have R and the R kernel for Jupyter installed. Install the required R packages by running the following in an R console:

## Contributing
Contributions to this project are welcome! Please fork the repository, make your changes, and submit a pull request.

## License
This project is licensed under the MIT License - see the LICENSE file for details.
