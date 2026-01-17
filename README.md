# Power-Theft-Detection-System-PTDS
Power Theft Detection System-PTDS is an intelligent ML-based solution that detects electricity theft by analyzing real-time consumption patterns. It automates detection, replaces manual inspections, sends alerts, reduces revenue loss for utilities, ensures fair billing, and leverages scalable Google AI technologies for smart grid–ready deployment.import pandas as pd
import numpy as np
import xgboost as xgb
from sklearn.model_selection import train_test_split
from sklearn.preprocessing import StandardScaler
from sklearn.metrics import classification_report, confusion_matrix

# 1. DATA ACQUISITION & PREPROCESSING [cite: 80, 108]
# Simulating smart meter data: voltage, current, and energy flow [cite: 46, 47]
def load_and_preprocess_data(file_path):
    data = pd.read_csv(file_path)
    
    # Feature Engineering [cite: 133, 134]
    # Creating a feature to identify 'unusual spikes' mentioned in your MVP [cite: 172]
    data['power_diff'] = data['input_power'] - data['output_power']
    
    # Standardizing data for better sensor accuracy [cite: 66, 67]
    scaler = StandardScaler()
    features = ['voltage', 'current', 'energy_flow', 'power_diff']
    data[features] = scaler.fit_transform(data[features])
    
    return data, features

# 2. THEFT DETECTION LOGIC (XGBoost) [cite: 48, 117]
def train_theft_detector(data, features):
    X = data[features]
    y = data['is_theft'] # 1 for theft, 0 for normal [cite: 95, 96]
    
    X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state=42)
    
    # Using XGBoost as specified in the Ensemble learning method 
    model = xgb.XGBClassifier(
        n_estimators=100,
        learning_rate=0.1,
        max_depth=5,
        objective='binary:logistic'
    )
    
    model.fit(X_train, y_train)
    return model, X_test, y_test

# 3. ALERT GENERATION SYSTEM [cite: 131, 136]
def generate_alert(meter_id, anomaly_score):
    if anomaly_score > 0.85: # High accuracy threshold [cite: 99]
        print(f"ALERT: Power Theft Detected!")
        print(f"Meter ID: {meter_id}")
        print(f"Status: Suspicious activity - Unusual spike detected. [cite: 172]")

# Example Execution
if __name__ == "__main__":
    # In a real scenario, this would connect to Google BigQuery [cite: 111]
    print("Initializing Neural Nexus PTDS...")
    # model, X_test, y_test = train_theft_detector(data, features)
