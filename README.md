# 100KGP_enrichment
*Enrichment analysis scripts for working on case control data in the 100KGP in a multi-sample tidy vcf data format rather than aggregate data files*

The main directory contains notebooks for performing enrichment analysis. The PRS subdirectory contains PRS calculations on the same input data.

## What is Tidy Data Format for VCFs
Tidy data is a standard way of mapping the meaning of a dataset to its structure. A dataset is tidy when each variable forms a column, each observation forms a row, and each type of observational unit forms a table. Data can be in this Tidy "long" format, where each row is a single observation for a variable (often leading to multiple rows per subject), or in "wide" format, where each row represents multiple observations across variables for a single subject. The tidy data principle facilitates data analysis and visualization, making it easier to manipulate, model, and visualize data sets.

Aggregate VCF (Variant Call Format) files, commonly used in genomics for storing gene sequence variations, do not meet the tidy data standard, primarily due to their structure. Aggregate VCF files encapsulate multiple observations (e.g., alleles, genotypes of different individuals) in a single row. Consequently, these VCF files are inherently in a wide format, where each row contains a mix of observational units (variants) and multiple observations per unit (genotype information across individuals), complicating direct analysis and visualization without preprocessing into a tidy format.

Instead of aggregate files, the scripts here utilise the Tidy format, where each row represents a seperate variant from a specific person. Compared to normal VCF format there is an additional sample field.

The required fields in the VCF input files are:

| Field Name  | Description                                           |
|-------------|-------------------------------------------------------|
| Sample      | Identifier for the sample                             |
| Chrom       | Chromosome where the variant is located               |
| Pos         | Position of the variant on the chromosome             |
| ID          | Variant ID (e.g., rs number)                          |
| Ref         | Reference allele                                      |
| Alt         | Alternative allele(s)                                 |
| Qual        | Quality score of the variant                          |
| Filter      | Filter status (e.g., PASS if the variant passed all filters) |
| GT          | Genotype, representation of the alleles (e.g., 0/1, 1/1) |
| GQ          | Genotype Quality, a measure of the quality of the genotype call |
| DP          | Depth of sequence coverage at the site of the variant |

# Allele Frequency Analysis

This directory contains Jupyter notebooks for performing allele frequency analysis on genetic variant data extracted from VCF files in a modified wide mulit-sample VCF, to make the whole data compliant with tidyverse long data format. The analysis calculates allele frequencies for each variant and performs Fisher's Exact Test to compare the frequencies between cases and controls. The repository includes both R and Python implementations.

## Contents

- `case_control_enrichment_with_R.ipynb`: A Jupyter notebook with the R kernel showcasing the allele frequency analysis workflow in tidy R.
- `case_control_enrichment_with_base_R.ipynb`: A Jupyter notebook with the R kernel showcasing the allele frequency analysis workflow in tidy R.
- `case_control_enrichment_with_python.ipynb`: A Jupyter notebook with the Python kernel demonstrating the allele frequency analysis workflow in Python.

## Prerequisites

Ensure you have R and the R kernel for Jupyter installed.

## Contributing
Contributions to this project are welcome! Please fork the repository, make your changes, and submit a pull request.

## License
This project is licensed under the MIT License - see the LICENSE file for details.
