# Adey Innovations - Fraud Detection System

## Project Overview
This project aims to improve fraud detection for Adey Innovations Inc. across two transaction streams: E-commerce and Bank Credit Cards. 

## Task 1: Data Analysis and Preprocessing (Completed)
In this phase, I have:
- **Cleaned** both E-commerce and Bank datasets.
- **Geolocation Integration**: Mapped IP addresses to countries using range-based lookups.
- **Feature Engineering**: Created behavioral features including:
  - `time_since_signup`: Detects immediate purchases after account creation.
  - `device_usage_count`: Identifies high-frequency velocity attacks from single devices.
  - `hour_of_day` & `day_of_week`: Captures temporal patterns in fraudulent behavior.
- **Data Scaling**: Applied `StandardScaler` to ensure numerical parity across features.

## Project Structure
- `data/`: Raw and processed datasets (ignored by git).
- `notebooks/`: Exploratory Data Analysis and Feature Engineering steps.
- `scripts/`: Python scripts for data processing.
- `requirements.txt`: List of dependencies.

## Setup
1. Clone the repository.
2. Install dependencies: `pip install -r requirements.txt`
3. Run notebooks in order: `eda-fraud-data.ipynb` -> `eda-creditcard.ipynb` -> `feature-engineering.ipynb`.
### Key Achievements:
- **IP Mapping**: Successfully mapped IP addresses to countries using range-based lookups.
- **Feature Engineering**: Created behavioral features: `time_since_signup` (to catch instant-purchases) and `device_usage_count` (to catch velocity attacks).
- **Class Imbalance**: Documented a 9.3% fraud rate in the original data. 
- **Resampling**: Applied **SMOTE** to the training set, balancing the classes to a 50/50 distribution (109,568 samples each) to ensure the model learns fraud patterns effectively.

## Project Structure
- `data/`: Data storage (excluded from GitHub).
- `notebooks/`: Sequential process from EDA to Modeling Prep.
- `requirements.txt`: Project dependencies.