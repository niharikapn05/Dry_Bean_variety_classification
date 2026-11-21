# Dry Bean Variety Classification System

A beginner-friendly multiclass machine-learning project that predicts one of seven dry bean varieties from 16 numerical shape measurements.

## Dataset
Official source: https://archive.ics.uci.edu/dataset/602/dry+bean+dataset

The UCI dataset contains 13,611 rows, 16 input features and 7 target classes. The project downloads it automatically through `ucimlrepo` when you run training. Internet is required for the first run. It saves a local CSV copy in `dataset/`.

## Setup (Windows)

1. Extract this ZIP file.
2. Open the extracted `DryBean_Classification_Project` folder in VS Code.
3. Open Terminal in that folder.
4. Create and activate a virtual environment (optional but recommended):

   ```bash
   python -m venv venv
   venv\Scripts\activate
   ```

5. Install packages:

   ```bash
   pip install -r requirements.txt
   ```

6. Train and compare models:

   ```bash
   python train.py
   ```

7. Start the web app:

   ```bash
   streamlit run app.py
   ```

## Outputs
- `dataset/Dry_Bean_Dataset.csv` - downloaded dataset
- `models/best_model.joblib` - saved best model
- `reports/model_comparison.csv` - model accuracy and macro-F1 comparison
- `reports/classification_report.txt` - detailed classification report

## Models compared
Logistic Regression, K-Nearest Neighbors, Support Vector Machine, Random Forest and Extra Trees. Scaling is included in pipelines for models that need it. The best model is selected using macro-F1 on a stratified test split.

## Important
This is a tabular-feature classification project. The model expects 16 measurements extracted from a bean image; it does not directly classify a raw uploaded photo.

## Dataset citation
Köklü, M. and Özkan, I.A. (2020). Multiclass classification of dry beans using computer vision and machine learning techniques. Computers and Electronics in Agriculture, 174, 105507. UCI Machine Learning Repository, DOI: 10.24432/C50S4B. Dataset license: CC BY 4.0.
