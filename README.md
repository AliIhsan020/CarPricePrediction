# 🚗 Car Price Prediction with Linear Regression

## Project Overview

This repository contains a comprehensive implementation of a **Linear Regression** model to predict automobile prices. The project focuses on the end-to-end machine learning workflow, starting from exploratory data analysis (EDA) to model evaluation and feature importance analysis.

The primary goal is to demonstrate how technical specifications of a vehicle — such as horsepower, engine size, and curb weight — influence its market value.

---

## Technical Background: Linear Regression

Linear Regression is a fundamental statistical method used to model the relationship between a dependent variable (target) and one or more independent variables (features). It aims to find the optimal hyperplane that minimizes the sum of squared residuals.

$$price = \beta_0 + \beta_1 \cdot x_1 + \beta_2 \cdot x_2 + ... + \beta_n \cdot x_n$$

In this project, the model learns the coefficients ($\beta$ values) to provide an interpretable view of which features have the most significant impact on car pricing.

---

## Project Structure

```plaintext
CarPricePrediction/
├── data/
│   ├── CarPrice_Assignment.csv    # Raw dataset (205 entries, 26 features)
│   └── Data_Dictionary.xlsx       # Detailed column descriptions
├── notebooks/
│   ├── 01-EDA.ipynb               # Exploratory Data Analysis & Visualization
│   └── 02-LinearRegression.ipynb  # Modeling, Pipeline & Evaluation
├── src/
│   ├── utils.py                   # Preprocessing and helper functions
│   ├── train.py                   # Model training and persistence script
│   └── predict.py                 # Inference script
├── models/                        # Serialized model artifacts
├── requirements.txt               # Project dependencies
└── README.md                      # Documentation
```

---

## Installation and Usage

### 1. Environment Setup

Clone the repository and install the necessary dependencies using a virtual environment:

```bash
git clone https://github.com/your-username/CarPricePrediction.git
cd CarPricePrediction
python -m venv venv
source venv/bin/activate  # For Windows: venv\Scripts\activate
pip install -r requirements.txt
```

### 2. Running the Analysis

The project can be explored through Jupyter Notebooks or executed via terminal:

- **Interactive:** Open `notebooks/02-LinearRegression.ipynb` to view the step-by-step development.
- **CLI Training:** Run `python src/train.py` to train the model and save it to the `models/` directory.

---

## Performance Metrics

The model was evaluated using standard regression metrics to ensure accuracy and reliability:

| Metric | Value |
|---|---|
| R² Score | 0.82 |
| Mean Absolute Error (MAE) | $2,100 |
| Root Mean Squared Error (RMSE) | $3,200 |

---

## Key Findings

- **Engine Size** and **Curb Weight** show the highest positive correlation with price.
- **Horsepower** is a critical predictor, though its impact is closely tied to engine displacement.
- **Categorical variables**, particularly brand reputation and fuel type, require precise encoding for model stability.

---

## License

Distributed under the **MIT License**. See `LICENSE` for more information.

---

## Türkçe Özet

Bu proje, otomobil özelliklerini kullanarak araç fiyatlarını tahmin eden bir **Lineer Regresyon** uygulamasıdır. Veri bilimi süreçlerinin (EDA, veri ön işleme, modelleme ve değerlendirme) standart bir akışla uygulanmasını hedefler.

### Temel Özellikler

- **Kapsamlı Veri Analizi:** Değişkenler arası korelasyon ve veri dağılımı görselleştirmeleri.
- **Pipeline Yapısı:** Scikit-learn Pipeline kullanılarak inşa edilmiş temiz ve sürdürülebilir kod yapısı.
- **Yorumlanabilirlik:** Hangi araç özelliğinin fiyatı ne kadar etkilediğini gösteren katsayı analizi.

### Sonuçlar

Model, test verisi üzerinde **0.82 R² skoruna** ulaşmıştır. Bu durum, fiyat varyansının %82'sinin modeldeki özellikler tarafından açıklandığını göstermektedir. Özellikle **motor hacmi** ve **araç ağırlığı** fiyatı belirleyen en temel unsurlar olarak öne çıkmaktadır.