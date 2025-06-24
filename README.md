# Machine_Learning_Project

# Colon Cancer Cell Classification (CRCHistoPhenotypes)

> **Developed as part of a university project on machine learning in medical imaging with my teammate with both of us having equal contribution**

This project aims to develop a robust ML-based system for classifying colon cell histopathology images. It includes:

- **Binary Classification**: Predict if a cell is cancerous or non-cancerous (`isCancerous`)
- **Multiclass Classification**: Identify cell types among `epithelial`, `fibroblast`, `inflammatory`, and `others`

## Dataset

- 20,280 H&E-stained image patches from colon tissue
- Sourced from the CRCHistoPhenotypes dataset
- Two splits:
  - `main_data.csv`: 60 patients with full labels
  - `extra_data.csv`: 38 patients with binary labels only (semi-supervised potential)
- All images are 27x27 RGB

##  Project Highlights

- **Patient-wise data splitting** to avoid leakage
- **Class imbalance analysis** and correlation plots
- **MLP and CNN models** with extensive hyperparameter tuning
- Evaluated using accuracy, F1-score, and confusion matrix
- Visualizations of learning curves, metrics, and class distributions
- Benchmark comparison with prior research using CRCHistoPhenotypes

## Tech Stack

- **Python 3**, Jupyter Notebook
- **TensorFlow / Keras** for DL models
- **scikit-learn** for baseline models (e.g., Random Forest)
- **Matplotlib / Seaborn** for EDA & visualization
- **Pandas, NumPy** for data processing

## How to Run

1. Clone this repo
2. Place `patch_images/` and label CSVs in the root directory
3. Open `ML-Cancer.ipynb` and run all cells

>  Note: Training may take time. GPU acceleration is recommended.

## Sample Results (Binary MLP)

| Metric       | Value  |
|--------------|--------|
| Accuracy     | 81.9%  |
| Precision    | 88%    |
| Recall       | 81%    |
| F1-score     | 84%    |

## Key Learnings

- Importance of **patient-level split** to avoid overfitting
- Handling **label imbalance** is crucial in medical datasets
- Simpler models (MLP) can perform competitively when well-tuned

