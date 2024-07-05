# Differential_Expression_Analysis

# Aim: To identify deregulated genes in Psoriatic Arthritis patients by performing differential expression analysis using EdgeR

# About Sample:
Link: https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE205748 

There are total 27 samples. It contains read counts of RNA sequencing data. 
Each sample's classification into one of the three categories: 
1. Healthy
2. PsA_les [Psoriatic Arthritis Lesional]
3. PsA_uninv [Psoriatic Arthritis Uninvolved - areas that are not affected by Psoriatic Arthritis])

# What is primary Objective?

The main objective is to find genes whose expression levels are significantly different between Psoriatic Arthritis (PsA) patients and healthy controls (i.e. between affected and unaffected tissues in PsA patients).
Identifying these deregulated genes helps in understanding the molecular mechanisms underlying PsA, which can lead to the discovery of potential biomarkers for diagnosis and therapeutic targets.

# What is Differential Expression Analysis:

Differential expression (DE) analysis involves comparing gene expression levels between different conditions to identify genes that show statistically significant differences.
This analysis helps pinpoint specific genes that may contribute to or be affected by the disease.

# What is the purpose of using EdgeR for DE Analysis:

EdgeR is a popular Bioconductor package in R designed for DE analysis of RNA-Seq count data. It uses statistical methods based on the negative binomial distribution.

# Main Workflow 

1. Data Collection:

Obtaining raw RNA-Seq read counts for genes from both PsA patients and healthy controls 
Also collecting relevant metadata, such as sample information and tissue type (affected vs. unaffected).

2. Data Preprocessing:

check for missing values and other data manipulation. 

3. Normalization:

Normalize the data to account for differences in sequencing depth and RNA composition between samples.

4. Model Design:

Grouping by defining groups based on experimental conditions (e.g., PsA vs. healthy, or PsA lesional vs. non-lesional).
Designing Matrix by creating a design matrix that models the experimental conditions, which is used to compare gene expression between groups.

5. Dispersion Estimation:

Estimating the variability in gene expression data since accurate dispersion estimation is crucial for reliable DE analysis.

6. Differential Expression Testing:

Performing statistical tests to identify genes that are differentially expressed between groups.
Multiple Testing Correction: Apply corrections (e.g., Benjamini-Hochberg) to control for false discovery rate (FDR) and reduce the chance of false positives.

7. Result Interpretation:

Top Genes: Identify top deregulated genes based on adjusted p-values and log-fold changes.
Biological Insight: Interpret the biological significance of these genes, potentially linking them to pathways or processes relevant to PsA.
Visualization:

8. Plots: Use visualizations (e.g., MA plots, volcano plots, heatmaps) to present the results and highlight significant findings.
Interactive Tools: Employ interactive visualization tools to explore the data further.
