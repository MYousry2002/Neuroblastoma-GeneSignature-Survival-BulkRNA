# Neuroblastoma Gene Signature Survival Analysis
Gene Signature Survival analysis for Bulk RNA data from Neuroblastoma pateints.

## Project Overview
This project focuses on the survival analysis of neuroblastoma patients using gene signature scores derived from bulk RNA sequencing data. The goal is to identify key gene signatures that correlate with survival outcomes. Gene Pathways in the analysis include TGF-Beta, IL2/STAT5, IL6/JAK/STAT3, IFN-Alpha, IFN-Gamma, Inflamatory, and Housekeeping ACTB. The survival analysis includes quantile-stratified analysis using the Kaplan-Meier Plot and continuous analysis using the Cox proportional hazards regression model.

## Data Description
The dataset used in this analysis includes the following:

- Gene expression data from bulk RNA sequencing of neuroblastoma samples that is normalized and Log2 transformed accessed from (GSE49711)[https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE49711]. 
- Pateints Meta Data accessed from (GSE49711)[https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE49711] and (GSE62564)[https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE62564]. Key variables include:
    - `os_days`: Overall survival in days.
    - `os_event`: Event indicator (1 if the death event occurred, 0 otherwise).
- Human gene sets for the gene pathways analyzed accessed from the (Gene Set Enrichment Analysis)[https://www.gsea-msigdb.org/gsea/msigdb/human/genesets.jsp?collection=H].


## Repository Contents
Below is a map of the repository, detailing the main components and their purpose:

-Neuroblastoma-GeneSignature-Survival-BulkRNA
│
├── dataset                                             # Folder containing all datasets used
│   ├── GSE49711_SEQC_NB_TAV_G_log2.final.txt           # Processed dataset for analysis
│   ├── GSE49711_series_matrix.txt                      # Pateints meta data
│   ├── GSE62564_series_matrix.txt                      # Pateints meta data
│   ├── HALLMARK_IL2_STAT5_SIGNALING                    # Gene sets related to IL2/STAT5 signaling
│   ├── HALLMARK_IL6_JAK_STAT3_SIGNALING                # Gene sets for IL6/JAK/STAT3 pathway
│   ├── HALLMARK_INFLAMMATORY_RESPONSE                  # Gene sets for inflammatory responses
│   ├── HALLMARK_INTERFERON_ALPHA_RESPONSE              # Gene sets for interferon alpha response
│   ├── HALLMARK_INTERFERON_GAMMA_RESPONSE              # Gene sets for interferon gamma response
│   └── HALLMARK_TGF_BETA_SIGNALING                     # Gene sets for TGF-beta signaling
│
├── .gitignore                                          # Specifies intentionally untracked files to ignore
├── Neuroblastoma-GeneSignature-Survival-BulkRNA.ipynb  # Main Jupyter notebook with analysis
├── README.md                                           # Detailed description of the project, repository, and usage
└── requirements.txt                                    # Required Python libraries for running the project

## Installation and Requirements
Ensure you have Python 3.x installed. To install all required libraries, run the following command:
```bash
python3 -m venv <envname>
Source <envname>/bin/activate
pip install -r requirements.txt
```

## Running the Analysis
To execute the analysis, open the Jupyter notebook in an environment that supports IPython notebooks (e.g., JupyterLab, Jupyter Notebook, or VSCode):
```bash
jupyter notebook Neuroblastoma-GeneSignature-Survival-BulkRNA.ipynb
```

## Analysis Workflow
1. **Data Preprocessing**: Cleaning the metadata, calculating gene signature scores, and preparing data for analysis.
2. **Survival Analysis**:
    - Kaplan-Meier Estimates: Visualize survival functions for quantile-stratified gene expression groups.
    - Cox Proportional Hazards Model: Assess the impact of continuous gene expression levels on survival.
3. **Results and Visiualizations**: Generate plots illustrating survival curves and the impact of gene expressions on survival, along with hazard ratios for significant genes.

## Results
[to-do] This section should summarize key findings, including which gene signatures are significantly associated with survival outcomes in neuroblastoma, along with interpretations.

## Contributing
Contributions to this project are welcome. Please contact us through email or the issues tab, or fork the repository and submit pull requests with your proposed changes.

## License
This project is shared under MIT lisence.

## Contact Information
For questions or feedback, please contact:
- Name: Mohamed Yousry ElSadec
- Position/Institution: Computational Biologist I at Dr. Jared Rowe's lab at Dana Farber Cancer Institute
- Email: mohamed.y.elsadec@gmail.com