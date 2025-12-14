# Identifying-Cancer-Based-on-Methylation-Patterns-in-cfDNA-Using-Decision-Tree-Based-Ensemble-Models
Machine Learning for Functional Genomics Project by Jaclyn Zatsiorsky and Peter Tzelios. Exploring the binary calssification of cancer vs. non-cancer and the multi-class classfication of colorectal, lung, vs. liver cancer. Used ensemble based tree methods, neural networks, and lasso regression.

## Repository contents
- `final_notebook.ipynb`: complete analysis pipeline and model training
- `figures/`: figures used in the final report and presentation

## Data access
Processed feature matrices and labels are available via Google Drive:
https://drive.google.com/drive/folders/1DasU3mNDpyNR_9XsvBQr8lk-kOGz-8D-?usp=share_link

Due to size and access restrictions, raw cfDNA data are not included.
The Google Drive folder contains all data required to reproduce the results.

## Data files

- **data_fixedgrid_40kbps.csv**  
  Processed cfDNA feature matrix generated using 40 kbp genomic windows, prior to any feature selection.

- **metadata.csv**  
  Sample-level metadata, including cancer type labels and other descriptive information.

- **gene_df.csv**  
  Mapping of genomic features to corresponding genes in the human genome.

- **X_*.csv** and **y_*.csv**  
  Feature matrices (`X_*.csv`) and corresponding labels (`y_*.csv`) for model training, validation, and testing.

  - Files containing `_canc` were used for **multiclass cancer type classification** (colorectal, lung, liver).
  - Files without `_canc` were used for **binary cancer vs non-cancer classification**.
  - Files containing `_postft` include features selected using statistical tests.
  - Files containing `_postlasso` include only features with non-zero coefficients from Lasso regression.


## Running the notebook
All required Python packages are installed directly within the notebook.
After downloading the processed data, update file paths as needed and run
the notebook top-to-bottom.

