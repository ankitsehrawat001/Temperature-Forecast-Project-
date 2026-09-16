# AKII WEATHER

AI-POWERED WEATHER INTELLIGENCE

A premium Streamlit web application for predicting next-day maximum and minimum temperatures using machine learning. The app uses atmospheric, geographic, and weather-derived features with an XGBoost regressor trained on a Kaggle weather dataset.

## Features

- Manual weather input form for forecasting
- Next-day Tmax and Tmin prediction
- Dark premium dashboard UI
- Model status and forecast metrics
- Data explorer and visual analytics
- XGBoost-based regression pipeline

## Project Structure

```text
Temperature_Forecast_Project_using_ML/
├── app.py
├── requirements.txt
├── .venv/
├── xgb_next_tmax.joblib
├── xgb_next_tmin.joblib
├── training_metrics.json
├── README.md
└── temp.csv   # downloaded via KaggleHub at runtime
```

## Tech Stack

- Python
- Streamlit
- pandas
- NumPy
- scikit-learn
- XGBoost
- KaggleHub
- Plotly
- joblib

## Setup

1. Open PowerShell in the project folder.
2. Create a virtual environment:

```powershell
python -m venv .venv
```

3. Activate the virtual environment:

```powershell
.\.venv\Scripts\Activate.ps1
```

4. Install dependencies:

```powershell
pip install -r requirements.txt
```

## Run the App

```powershell
streamlit run app.py
```

Then open the local URL shown in the terminal, usually:

```text
http://localhost:8501
```

## Model Details

The app trains two independent XGBoost regression models:

- Next-day maximum temperature (`Next_Tmax`)
- Next-day minimum temperature (`Next_Tmin`)

The pipeline includes:

- median imputation
- standard scaling
- XGBoost regressor

## Notes

- The app is designed for manual prediction inputs rather than displaying raw dataset rows.
- The dataset is downloaded automatically using KaggleHub when the app runs.
- If the model files are missing or invalid, the app retrains them automatically.

## License

This project is for educational and portfolio/demo purposes.
