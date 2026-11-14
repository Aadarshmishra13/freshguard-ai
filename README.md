# FreshGuard AI
### Multimodal Food Freshness Assessment and Spoilage Prediction

## Overview

FreshGuard AI is a machine learning-based platform designed to assess food freshness through image analysis and environmental storage data. It combines computer vision and traditional machine learning to provide complementary insights into food quality and spoilage.

The system consists of two independent prediction models:

- **Vision Model:** Analyses food images and classifies freshness into Fresh, Nearing Spoilage and Spoiled categories.
- **Environmental Model:** Analyses food type and storage conditions to predict whether food is Not Spoiled or Spoiled.

Both models are integrated into a Streamlit application, providing separate predictions, confidence scores and model explanations.

## Model Architecture

| Component | Vision Model | Environmental Model |
|---|---|---|
| Dataset | AgriFreshNET | IntelliStore |
| Input | RGB food images | Structured storage data |
| Approach | CNN and transfer learning | Supervised machine learning |
| Algorithms | MobileNetV3, EfficientNet-B0 | Logistic Regression, Random Forest, XGBoost |
| Output | 3 freshness classes | 2 spoilage classes |

**Vision model classes:**
- Fresh
- Nearing Spoilage
- Spoiled

**Environmental model classes:**
- Not Spoiled
- Spoiled

The two models retain independent prediction outputs because they address different classification tasks.

## Datasets

**1. AgriFreshNET – Primary Vision Dataset**

- Approximately 14,500 RGB images.
- 24 food categories.
- Three freshness categories: Fresh, Semi-Fresh and Rotten.
- Used for image-based freshness classification.

Source: [Mendeley Data – AgriFreshNET](https://data.mendeley.com/datasets/42m5tb7yv9/1)

**2. IntelliStore – Environmental Dataset**

- 250 original observations.
- 10 food categories.
- Environmental measurements including temperature, humidity, storage duration and CO₂.
- Binary spoilage target.

Source: [Original Research Publication](https://onlinelibrary.wiley.com/doi/10.1002/itl2.402) | [Research Dataset](https://github.com/shivamsingha/aiot-food-storage/tree/main/datasets)

**3. Controlled Freshness Sensing Study – Research Reference**

An additional controlled freshness study is considered as a potential independent research benchmark, subject to data access.

Source: [Research Publication](https://link.springer.com/article/10.1007/s42114-026-01834-3)

## Technology Stack

| Component | Technologies |
|---|---|
| Language | Python |
| Data Processing | Pandas, NumPy |
| Image Processing | OpenCV, Pillow |
| Visualisation | Matplotlib, Seaborn, Plotly |
| Deep Learning | CNN, MobileNetV3, EfficientNet-B0 |
| Machine Learning | Scikit-learn, XGBoost |
| Explainable AI | SHAP, Permutation Importance |
| Application | Streamlit |
| Model Persistence | Joblib |
| Development | Google Colab, Jupyter Notebook |
| Version Control | Git, GitHub |

## Application Features

- **Visual Freshness Assessment:** Image-based three-class freshness prediction.
- **Storage Analysis:** Environmental-condition-based spoilage prediction.
- **Explainable AI:** Model interpretation and feature importance.
- **Food Inventory:** Food storage and shelf-life record management.
- **Batch Analytics:** CSV-based batch predictions and reporting.
- **Dashboard:** Centralised presentation of model outputs and analytics.

## Repository Structure

```text
freshguard-ai/
│
├── app/
│   ├── Home.py
│   └── pages/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── models/
│
├── notebooks/
│   ├── 01_dataset_audit.ipynb
│   ├── 02_image_eda.ipynb
│   ├── 03_tabular_eda.ipynb
│   ├── 04_vision_model.ipynb
│   └── 05_environmental_model.ipynb
│
├── reports/
│   └── figures/
│
├── src/
│   ├── data/
│   ├── preprocessing/
│   ├── models/
│   └── evaluation/
│
├── tests/
│
├── requirements.txt
├── .gitignore
└── README.md
```

## Model Evaluation

Model performance will be assessed using appropriate classification metrics, including:

- Accuracy
- Precision, Recall and F1-score
- Macro-F1 for multiclass evaluation
- Confusion Matrix
- ROC-AUC for binary classification, where applicable

Class distribution, generalisation performance and potential data leakage will also be considered during evaluation.

## Disclaimer

FreshGuard AI is an educational and research-oriented machine learning prototype. Model predictions are estimates based on available training data and should not be interpreted as definitive food-safety assessments or substitutes for established food-safety guidelines and professional evaluation.

## Author

**Aadarsh Mishra**

Undergraduate Project – Bioinformatics | Artificial Intelligence and Machine Learning
