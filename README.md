# Grab Safe Driver Telematics Risk Analysis

This project leverages Grab driver telematics data, including anonymized acceleration, gyro, and GPS sensors, to analyze driving behavior patterns and identify potential risks of accidents or hazardous events. Using data exploration, feature engineering, driver segmentation, and risk prediction modeling, the results are expected to help Grab develop risk mitigation strategies, training programs, and driver incentives to improve road safety and overall service quality.

## 🎯 Business Problem

Grab, a major ride-hailing platform with millions of driver-partners, aims to improve safety and service quality by utilizing anonymous driver telematics data. The main objectives of this project:

1. Detecting high-risk driving behavior based on sensor data (acceleration, gyro, speed, and GPS accuracy) during a trip to prevent accidents and damage.

2. Identifying patterns and contributing factors to potential risks so Grab can provide education or incentives to drivers to improve safety.

3. Building risk prediction models or driver categories based on telematics data to support risk management decisions, insurance premium determination, or reward systems for safe drivers.

**Key Business Questions:**

1. What are the characteristics of driving behavior that indicate high risk?

2. Which telematics sensor features are most influential in predicting risk events?

3. How can we distinguish driver segments with different risk levels using telematics data?

4. What are the recommended risk mitigation and safety improvement strategies based on the data analysis results?

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

## 👤 Author

*Defrizal Yahdiyan Risyad*

[LinkedIn](#https://www.linkedin.com/in/defrizalyr?lipi=urn%3Ali%3Apage%3Ad_flagship3_profile_view_base_contact_details%3BqZ%2B7dZzhS%2FCtdV82zspJFQ%3D%3D) | [GitHub](#https://github.com/defrijay)