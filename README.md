🏎️ F1 Race Predictor – Predicting Formula 1 Outcomes with Machine Learning & FastAPI

📌 Overview
This project leverages Machine Learning (XGBoost, RandomForest) and FastAPI to predict Formula 1 race outcomes based on historical race data, weather conditions, lap times, and pit stops.

🚀 Key Features:
✅ Predict Driver Finishing Positions using ML Models
✅ Analyze Impact of Weather, Pit Stops & Track Conditions
✅ Deploy a FastAPI Endpoint for Real-Time Predictions
✅ Visualize Lap Time Distribution, Pit Stop Strategy & Weather Effects

📂 Project Structure

📦 F1-Race-Predictor
│── 📁 data/                     # Contains cleaned datasets
│   ├── cleaned_results.csv      # Race results
│   ├── cleaned_lap_times.csv    # Lap times
│   ├── cleaned_pit_stops.csv    # Pit stops
│   ├── Cleaned_F1_Weather.csv   # Weather data
│   ├── cleaned_races.csv        # Race details
│
│── 📁 models/                    # Trained models (if needed)
│
│── 📁 api/                       # API implementation using FastAPI
│   ├── main.py                   # FastAPI backend for predictions
│
│── F1_Race_Prediction.ipynb      # Jupyter Notebook with full analysis
│── requirements.txt              # Dependencies
│── README.md                     # Project Documentation
📊 Data Sources

The dataset consists of:

Race Results 🏁: Driver positions, points, constructor details, fastest laps
Lap Times ⏱️: Individual lap times for each driver
Pit Stops 🛠️: Pit stop count and duration
Weather Data 🌦️: Track temperature, humidity, wind speed, rainfall
Race Information 🏟️: Circuit, round number, and season year
🛠️ Installation Guide

To set up the project locally, follow these steps:

1️⃣ Clone the Repository
git clone https://github.com/your-username/F1-Race-Predictor.git
cd F1-Race-Predictor
2️⃣ Install Dependencies
pip install -r requirements.txt
3️⃣ Run Jupyter Notebook
jupyter notebook
Open F1_Race_Prediction.ipynb and execute the cells.

🚀 Machine Learning Pipeline

🔹 Data Preprocessing
✅ Merged datasets on raceId, driverId
✅ Handled missing values using forward-fill
✅ Encoded categorical features (constructorId, grid)
✅ Converted Time columns to seconds

🔹 Model Training
XGBoost Regressor trained on race data and weather conditions
Feature Importance Analysis for lap time prediction
Evaluation Metrics: Mean Squared Error (MSE) & R² Score
📡 FastAPI - Real-Time Prediction API

1️⃣ Start the FastAPI Server
Run the following command:

uvicorn api.main:app --host 0.0.0.0 --port 8000 --reload
2️⃣ API Endpoints
Endpoint	Method	Description
/	GET	API Status Check
/predict	POST	Predict race position
3️⃣ Example API Request
Send a POST request with feature values:

{
  "features": [0.3, 22, 1005, 0, 45, 180, 5, 1, 0]
}
Response:

{
  "predicted_position": [5]
}
📊 Data Visualizations

🔹 Lap Time Distribution


🔹 Feature Importance


🔹 Actual vs. Predicted Position


🛠️ Technologies Used

Python (pandas, numpy, matplotlib, seaborn)
Machine Learning (XGBoost, Scikit-learn)
FastAPI (Backend for Predictions)
Jupyter Notebook (Exploratory Analysis & Modeling)
📌 To-Do List

✅ Train ML models
✅ Deploy FastAPI prediction endpoint
✅ Data visualizations for F1 insights
⬜ Improve prediction accuracy
⬜ Deploy API to a cloud platform

🤝 Contributing

Fork the repository.
Create a feature branch (git checkout -b feature-branch).
Commit your changes (git commit -m "Added a new feature").
Push to the branch (git push origin feature-branch).
Create a Pull Request.
📜 License

This project is licensed under the MIT License.

💡 Acknowledgments

Special thanks to FastF1, Kaggle, and OpenAI for providing valuable insights & datasets.

🔗 Connect With Me

📧 Email: milind.bage@warwick.ac.uk/milind.gottlieb155@gmail.com
📷 LinkedIn: https://www.linkedin.com/in/milind-bage-652b67179/

