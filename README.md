# CMPE 256 Final Project

Team 6: Jian Fu, Lawrence Lin, & Wilson Huang

Recommendation system for predicting beer ratings from the [BeerAdvocate](https://cseweb.ucsd.edu/~jmcauley/datasets.html#multi_aspect) dataset.

## Repository Layout

- `EDA/EDA_BeerAdvocate.ipynb` - exploratory data analysis for BeerAdvocate.
- `EDA/EDA_RateBeer.ipynb` - exploratory data analysis for RateBeer.

- `baselines/Baseline_Popularity.ipynb` - non-personalized popularity baseline.
- `baselines/Baseline_Content.ipynb` - content-based baseline using beer metadata/review text.
- `baselines/Baseline_Collab_SVD.ipynb` - collaborative filtering baseline with SVD.
- `variant1/Part1_metadata_4_ncf_rmse.ipynb` - metadata-based NCF (GMF, MLP, NeuMF) using beer features
- `variant1/part2_mlp_model_bpr_ranking.ipynb` - MLP recommender trained with MSE vs BPR
- `variant1/part3_mlp_model_temporal_attention.ipynb` - MLP with GRU + attention to model user history
- `variant2/Ensemble.ipynb` - ensemble-based recommendation variant with DeepFM, LightGBM, and Ridge Regression.
- `variants3_LLM/LLM.ipynb` - LLM/embedding-enhanced recommendation variant.

## Dataset

The notebooks expect line-delimited JSON files (`.json`, one JSON object per line):

- `beeradvocate_train.json`
- `beeradvocate_val.json`
- `beeradvocate_test.json`

Dataset files are excluded from the repo due to size and can be accessed from:
[Google Drive Dataset Folder](https://drive.google.com/drive/folders/1RGBerPhTfpiu6WVX8nkNse7Mkac2ayHE?usp=drive_link)

Before running any notebook, update all dataset paths to match your environment (local machine or Google Drive mount path).

## Notes

- Baseline notebooks provide reference performance for recommendation quality.
- The LLM notebook uses additional embedding/model infrastructure and is more resource intensive. A higher-end GPU is recommended.
- Notebook outputs in this repository include prior Colab runs; re-running may produce slightly different metrics depending on sampling/seeds.
