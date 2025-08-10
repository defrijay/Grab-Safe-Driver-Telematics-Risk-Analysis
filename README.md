# Grab Safe Driver Telematics Risk Analysis

This project leverages Grab driver telematics data, including anonymized acceleration, gyro, and GPS sensors, to analyze driving behavior patterns and identify potential risks of accidents or hazardous events. Using data exploration, feature engineering, driver segmentation, and risk prediction modeling, the results are expected to help Grab develop risk mitigation strategies, training programs, and driver incentives to improve road safety and overall service quality.

## 🎯 Business Problem

Grab aims to improve the safety of its driver-partners by leveraging anonymized telematics data from vehicle sensors (acceleration, gyro, GPS). This project aims to:

- Analyze high-risk driving behavior patterns.
- Build a risk prediction model based on telematics data.
- Provide recommendations for risk mitigation and safety improvement strategies.

## 📋 Dataset

The dataset contains anonymized telematics data from Grab driver-partners, including:
- `bookingID`: Trip ID
- `accuracy`
- Acceleration sensors on the X, Y, and Z axes
- Gyro sensors on the X, Y, and Z axes
- GPS Bearing and Accuracy
- Timestamp (`second`)

The dataset can be accessed from [Grab Safe Driver Telematics - Kaggle](https://www.kaggle.com/datasets/vancharmlab/grabai/data).

## 🛠 Methodology

1. **Data Understanding & Cleaning**
- Checking for missing values, duplication, and invalid data
- Filtering noise and sensor outliers

2. **Exploratory Data Analysis (EDA)**
- Visualizing acceleration, gyro, and bearing distributions
- Identifying extreme patterns (e.g., hard braking, sharp turns)

3. **Feature Engineering**
- Aggregating statistics per trip (mean, max, std)
- Calculating the frequency of extreme events or abrupt events

4. **Driver Segmentation**
- Clustering to group drivers based on risk patterns

5. **Risk Prediction Modeling**
- Training a classification model (Random Forest, XGBoost, etc.)
- Evaluation using accuracy, precision, recall, and AUC

6. **Model Interpretation & Business Insight**
- Feature importance analysis with SHAP
- Business recommendations for driver education and incentives

## 📈 Key Metrics

- Accuracy, Precision, Recall, F1-score
- ROC AUC for classification model performance
- Distribution and frequency of risk events

## 📂 Project Structure
```
Grab_Telematics_RiskAnalysis/
│
├── data/                  # Raw & processed datasets
├── notebooks/             # Jupyter notebooks for EDA, modeling
├── scripts/               # Python scripts for data prep, modeling
├── models/                # Saved model artifacts
├── reports/               # PDF/slide business insights
├── README.md               # Project documentation
└── requirements.txt        # Python dependencies
```

## 🚀 How to Run

```bash
# Clone repo
git clone <repo-url>
cd Grab_Telematics_RiskAnalysis

# Create a virtual environment
python -m venv venv
source venv/bin/activate # Mac/Linux
venv\Scripts\activate # Windows

# Install dependencies
pip install -r requirements.txt

# Run the notebook
jupyter notebook

```

👤 Author
Defrizal Yahdiyan Risyad
LinkedIn | GitHub