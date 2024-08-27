# 🩺 Heart Stroke Prediction Model

## Overview
This repository contains a comprehensive data science project aimed at predicting the likelihood of a stroke based on user-provided clinical data. It integrates multiple tools and frameworks to build a full-fledged, production-ready application for healthcare professionals and medical devices.

## Users
- **Medical Professionals** 👨‍⚕️
- **Clinics & Hospitals** 🏥
- **Medical Devices** 🔬

## Usage Description 🫀
This application allows healthcare professionals or users to input clinical and personal health data through a web interface or directly into medical devices. Our machine learning model then predicts the probability of a stroke, displaying detailed results, precautions, and recommendations for professional consultation.

## Features
- **Web Interface & Data Search**: Built with Streamlit for user-friendly interaction.
- **Prediction API**: Developed using FastAPI for real-time predictions.
- **Machine Learning Model**: Packaged as a Python module (`stroke-pred-p0w11`).
- **Data Storage**: Utilizes PostgreSQL with SQLAlchemy for secure and efficient data management.
- **Data Ingestion**: Implemented using Apache Airflow to collect and manage user input data.
- **Monitoring Dashboard**: Real-time prediction monitoring with Grafana.

## Dataset
We utilize a dataset with 11 clinical features for predicting stroke events. You can access it [here](https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset).

## Getting Started

### PostgreSQL Database Setup
1. Ensure you have the necessary dependencies installed:
    ```bash
    pip install -r Heart-Stroke-Prediction/requirements.txt
    ```
    > **Note:** For Mac/Linux users, install `psycopg2-binary` instead of `psycopg2`.

2. Create a `.env` file in the root directory (`Heart-Stroke-Prediction/.env`) with the following content:
    ```env
    [POSTGRES_DB]
    POSTGRES_USER=[Your_User]
    POSTGRES_PASSWORD=[Your_Password]
    POSTGRES_SERVER=[Your_Server]
    POSTGRES_PORT=[Your_Port]
    POSTGRES_DB=[Your_Database]

    [FastApi]
    BACKEND_SERVER=[Your_Server]
    ```

3. Navigate to the PostgreSQL setup directory and run the database setup script:
    ```bash
    cd stroke_heart_prediction/postgres
    python createdb.py
    ```

## Features:
### 1.Data Ingestion with Airflow

### 2. Monitor with Grafana 

### 3. Deploy the Web Interface on Heroku

## Execute Locally
To run the application locally, execute the following commands:
```bash
# Start the Prediction API
cd Heart-Stroke-Prediction/stroke_api
uvicorn main:app --host 0.0.0.0 --port 8005

# Start the Web Interface
streamlit run web_interface.py --server.port 8010
```
## System Architecture:
![image](https://github.com/user-attachments/assets/bc36a58e-9abd-41cc-95b1-5a0ce345e1c6)
