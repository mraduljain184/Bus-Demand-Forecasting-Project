# 🚌 RedBus Seat Demand Forecasting

Forecast seat bookings for intercity buses 15 days before departure using historical booking, transaction, and search data. This project was developed as part of a hackathon challenge.

---

## 👥 Team Members

- **Mradul Jain** – Data preprocessing, model engineering, validation pipeline  
- **Meghansh Bhati** – Feature engineering, model tuning, ensemble strategy

---

## 📌 Problem Statement

Demand for bus journeys is influenced by various dynamic factors like holiday calendars, wedding seasons, long weekends, school vacations, and regional events. However, not all holidays impact demand equally, making this a complex, non-trivial forecasting problem.

### 🎯 Hackathon Challenge Objective

Your task is to develop a model that accurately forecasts the demand for bus journeys 15 days prior to the journey date.

We are provided with:

- **Seats booked**: Historical demand data  
- **Date of Journey (doj)**: The actual travel date  
- **Date of Issue (doi)**: The ticket booking date  
- **Search Data**: Number of users searching for a specific journey  

#### 📈 Target

Predict the **final seat count** for each route on the day exactly **15 days before the actual Date of Journey (doj)**.
**Example**: For a route from City A to City B with `doj = 30-Jan-2025`, you must predict the final seat count **as of 16-Jan-2025**.

---

## 🧠 Approach

- Focused only on rows where `dbd = 15` to simulate the real forecasting window
- Engineered new features from city tiers, region pairs, day-of-week, search trends, and booking behavior
- Used time-aware validation (chronological split) to avoid data leakage
- Final model ensemble included:
  - LightGBM
  - XGBoost
  - CatBoost

---

## 📊 Evaluation Metric

- Root Mean Squared Error (**RMSE**)
- Real-world simulation through:
  - **Public split (30%)**: Real-time leaderboard
  - **Private split (70%)**: Final ranking post-hackathon
- Best Val RMSE: 540.2987
---

## 🛠 Tech Stack

- Python (Colab)
- Pandas, NumPy
- Scikit-learn
- LightGBM, XGBoost, CatBoost
- Matplotlib, Seaborn

---

## 📸 Visuals

The notebook contains:
- 📈 Feature Importance Plots
- 🧪 RMSE comparison between models
- 📊 Predictions vs Ground Truth
---

## 📬 Contact

- **Mradul Jain**: [GitHub](https://github.com/mraduljain184)
- **Meghansh**: [GitHub](https://github.com/Meghansh2005)

---

## 📄 License

MIT License – open for academic & non-commercial use.
