# 💧 Water Leakage Monitoring Dashboard (ML + GIS)

A smart city–oriented **2D GIS dashboard** for **underground water leakage detection** using
**Machine Learning (Isolation Forest)** and **interactive map visualization**.


## Features

- 2D GeoMap (Dubai region)
- Underground water pipe wireframe
- ML-based leakage detection (Isolation Forest)
- Severity classification:
  - 🟢 No Leak
  - 🔵 Normal
  - 🟡 Medium Risk
  - 🔴 High Risk Leak
- Location_Code based lookup
- Interactive popups and animations
- Clean, modern dashboard UI

---

##  ML Model

- Algorithm: **Isolation Forest**
- Input Features:
  - Pressure
  - Flow Rate
  - Temperature
  - Vibration
  - RPM
  - Operational Hours
- Output:
  - Anomaly Score
  - Leak Severity (threshold-based)

---

##  Project Structure

water_leakage_dashboard/
├── backend/
│ ├── app.py
│ ├── model/
│ │ ├── leak_model.pkl
│ │ └── scaler.pkl
│ ├── data/
│ │ └── pipe_locations.csv
│ └── utils/
├── frontend/
│ ├── index.html
│ ├── css/
│ └── js/
└── run.sh


---

## 🛠️ Setup Instructions

### 1️⃣ Backend Setup

```bash
cd backend
pip install -r requirements.txt

backend/model/leak_model.pkl
backend/model/scaler.pkl (if used)
backend/data/pipe_locations.csv

## Run Backend Server
python app.py


#Run Frontend
cd frontend
python -m http.server 5500


