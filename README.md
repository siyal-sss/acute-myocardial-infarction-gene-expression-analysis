# acute-myocardial-infarction-gene-expression-analysis
AMI transcriptomics analysis pipeline using GEO blood expression data. Identifies differentially expressed genes between heart attack patients and controls, performs pathway enrichment (GO/KEGG), and builds a machine learning model to predict AMI status from gene expression signatures.
AMI Transcriptomics Pipeline

A bioinformatics pipeline for analyzing blood gene expression in Acute Myocardial Infarction (AMI) patients compared to healthy controls using the public GEO dataset GSE66360.

The project identifies differentially expressed genes, performs pathway enrichment analysis, and builds a machine learning model to evaluate predictive gene signatures for AMI.

Dataset

GSE66360 (NCBI GEO)
Approximately 49 AMI patients and 50 healthy controls
Platform: Affymetrix Human Genome U133 Plus 2.0 (GPL570)
https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE66360

Objectives

- Identify differentially expressed genes in AMI
- Perform statistical testing with multiple testing correction
- Visualize gene expression patterns using PCA, volcano plot, and heatmap
- Perform GO and KEGG pathway enrichment analysis
- Build a machine learning model for AMI classification

Workflow

1. Data acquisition from GEO using GEOparse
2. Preprocessing of microarray expression data
3. Gene annotation using GPL570 platform
4. Exploratory analysis using PCA
5. Differential expression analysis using Welch’s t-test and FDR correction
6. Visualization of results using volcano plot and heatmap
7. Pathway enrichment analysis using gseapy (Enrichr)
8. Machine learning model using logistic regression and ROC-AUC evaluation

Key Results

- Identification of differentially expressed genes associated with AMI
- Enrichment of immune response and inflammatory pathways
- Gene expression patterns show potential for classification of AMI status

Tools and Libraries

Python
GEOparse
pandas, numpy
scipy, statsmodels
scikit-learn
matplotlib, seaborn
gseapy

Limitations

- Small sample size
- Microarray-based dataset
- Exploratory analysis, not clinical validation
- No external validation dataset included

Future Work

- Validation using independent dataset (GSE48060)
- Improved feature selection methods
- Model interpretability using SHAP
- Deployment as a web-based tool

Project Structure

ami-transcriptomics-pipeline/
├── notebooks/
│   └── ami_analysis.ipynb
├── src/
│   └── pipeline.py
├── results/
│   ├── DEG_results.csv
│   ├── pathway_enrichment.csv
├── requirements.txt
└── README.md

Conclusion

This project presents an end-to-end bioinformatics workflow for identifying gene expression signatures associated with Acute Myocardial Infarction and evaluating their predictive potential using machine learning.
