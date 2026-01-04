CareVision Analytics Dashboard (CareTrack)

🔗 Live Demo: https://carevision-insights-16.vercel.app/analytics

CareVision Analytics Dashboard (CareTrack) is a healthcare analytics and forecasting application built using synthetic healthcare data from Synthea. The project enables healthcare administrators and clinical staff to explore patient demographics, monitor chronic disease trends, analyze medication demand, and forecast future patient influx using time-series models.

⸻

Project Motivation

Healthcare professionals often face challenges interpreting complex patient data and forecasting future resource needs. Existing tools are either overly technical or lack predictive insights.

CareTrack addresses this gap by providing:
	•	Clear visual analytics
	•	Predictive modeling for future trends
	•	A user-friendly interface for non-technical users
	•	Exportable insights for operational planning

⸻

Key Features
	•	📊 Patient Demographics Analysis (age, gender, location)
	•	📈 Chronic Disease Trend Monitoring (cardiovascular, respiratory, neurological, etc.)
	•	🔮 Time-Series Forecasting using ARIMA
	•	🏙 City-level Patient Influx Prediction
	•	💊 Medication Demand Analysis
	•	🎛 Interactive Filters (condition, age group, year, location)
	•	📤 Exportable Reports (CSV/PDF)
	•	🌐 Web-based Dashboard deployed on Vercel

⸻

Tech Stack

Analytics & Modeling
	•	Python
	•	pandas, NumPy
	•	statsmodels (ARIMA)
	•	scikit-learn (preprocessing, evaluation)
	•	matplotlib / Plotly

Data
	•	Synthea Synthetic Healthcare Dataset
	•	Cleaned and processed CSV datasets

Frontend & Deployment
	•	Web dashboard (React / Next.js)
	•	Vercel deployment


carevision-analytics-dashboard/
│
├── notebooks/
│   ├── Preliminary_data_generation_and_reporting.ipynb
│   ├── timeseries_model_for_influx_in_terms_of_city_zipcode.ipynb
│
├── data/
│   ├── processed/
│   │   ├── cleaned_patients.csv
│   │   ├── cleaned_conditions.csv
│   │   ├── cleaned_medications.csv
│   │   ├── cleaned_observations.csv
│   │   ├── cleaned_procedures.csv
│   │   ├── cleaned_allergies.csv
│   │   └── cleaned_careplans.csv
│   └── README.md
│
├── README.md
├── .gitignore
Data Pipeline Overview
	1.	Raw Synthea datasets are ingested
	2.	Data cleaning and preprocessing using pandas
	3.	Feature engineering for time-series analysis
	4.	Aggregation by year, condition, and city (ZIP/FIPS)
	5.	Storage of cleaned datasets under data/processed/
	6.	Consumption by analytics notebooks and dashboard

⸻

Forecasting Methodology
	•	Model: ARIMA (AutoRegressive Integrated Moving Average)
	•	Targets:
	•	Condition-specific case counts
	•	City-level patient influx
	•	Forecast Horizon: 1–2 years
	•	Evaluation Metrics:
	•	RMSE
	•	MAE
	•	Visual inspection of actual vs predicted trends

⸻

Validation & Accuracy
	•	Forecast outputs validated against historical hold-out data
	•	Cross-checked with raw Synthea source files
	•	Usability testing conducted with non-technical users
	•	Feature traceability ensured via validation matrix

⸻

How to Run Locally

1️⃣ Clone the repository
git clone https://github.com/Chenchuvamsidharmallem/carevision-analytics-dashboard.git
cd carevision-analytics-dashboard
2️⃣ Install dependencies
pip install pandas numpy matplotlib scikit-learn statsmodels
3️⃣ Run notebooks

Open in Jupyter or Google Colab:
notebooks/

⸻

Intended Users
	•	Healthcare administrators
	•	Clinical operations teams
	•	Public health analysts
	•	Data analysts exploring healthcare forecasting

⸻

Data Ethics & Privacy
	•	All data used is synthetic (generated using Synthea)
	•	No real patient or PHI data is included
	•	Raw datasets are excluded to minimize size and maintain clarity

⸻

Future Enhancements
	•	Advanced forecasting models (SARIMA, Prophet, LSTM)
	•	Real-time data ingestion
	•	Role-based dashboard access
	•	API layer for external integrations

⸻

Contributors
	•	Mallem Chenchu Vamsidhar
	•	Gowtham Chapalamadugu
	•	Maryam Maqsood
	•	Srinidhi Dulipalla
	•	Vaishnavi Mailwar

⸻

License

This project is developed for academic and demonstration purposes.
