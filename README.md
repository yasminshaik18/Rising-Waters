# 🌊 Rising Waters: A Machine Learning Approach to Flood Prediction

[![Python Version](https://img.shields.io/badge/python-3.8%2B-blue.svg)](https://www.python.org/)
[![Flask](https://img.shields.io/badge/Flask-Web%20Framework-lightgrey.svg)](https://flask.palletsprojects.com/)
[![XGBoost](https://img.shields.io/badge/XGBoost-Machine%20Learning-success.svg)](https://xgboost.readthedocs.io/)

Floods are among the most devastating natural disasters, claiming thousands of lives and displacing millions every year. This project addresses the critical gap in early-warning systems by providing a Machine Learning-powered flood prediction web application trained on historical meteorological data. 

This project was developed as part of a virtual internship program managed by **SmartBridge** and overseen by **APSCHE**.

---

## 🏗️ Technical Architecture
* **Presentation Layer:** Interactive UI built with HTML/CSS (`about.html`, `index.html`, `result.html`).
* **Application Layer:** Python Flask server (`app.py`) handling routing and predictions.
* **Machine Learning Layer:** XGBoost classification model built and serialized via `train_model.py` (saved as `flood_model.pkl`).
* **Testing & Deployment:** Load testing is configured via `locustfile.py`, with cloud deployment configurations handled by `Procfile` and `runtime.txt`.

---

## 📊 Dataset & Model Training
The project processes a massive historical flood prediction dataset. During the training phase (`train_model.py`), the system utilizes a robust sampling method:
* **Total Dataset Size:** 1,117,957 rows
* **Sample Used:** 50,000 rows
* **Training Set:** 40,000 rows (80%)
* **Testing Set:** 10,000 rows (20%)

---

## 📁 Project Structure

```text
FLOOD_PREDICTION(SOURCE CODE)/
│
├── Dataset/
│   ├── test.csv             # Testing data subset
│   └── train.csv            # Training data subset
│
├── Model/
│   └── flood_model.pkl      # Serialized XGBoost classification model
│
├── Templates/
│   ├── about.html           # Information page about the project
│   ├── index.html           # Main input dashboard
│   └── result.html          # Prediction output page
│
├── app.py                   # Main Flask application backend
├── locustfile.py            # Script for load testing the web application
├── Procfile                 # Cloud deployment configuration
├── requirements.txt         # Required Python libraries
├── runtime.txt              # Specifies the Python version for deployment
└── train_model.py           # Script to clean data, train, and save the ML model
```

---

## ⚙️ Installation & Setup

**1. Clone the repository and navigate to the directory**
```bash
cd "FLOOD_PREDICTION(SOURCE CODE)"
```

**2. Set up a virtual environment (Recommended)**
```bash
python -m venv venv
source venv/bin/activate  # On Windows use: venv\Scripts\activate
```

**3. Install Dependencies**
```bash
pip install -r requirements.txt
```
*(Key libraries include: pandas, numpy, scikit-learn, xgboost, and flask)*

**4. (Optional) Retrain the Model**
If you wish to rebuild `flood_model.pkl` from the datasets:
```bash
python train_model.py
```

**5. Run the Flask Application**
```bash
python app.py
```

**6. Access the Web App**
Open your web browser and navigate to: `http://127.0.0.1:5000/`

---

## 👥 Project Members
* **Yasmin Shaik** (Team Lead)
* **Ameena Shaik** (Member)
* **Chetan Reddy Sannapareddy** (Member)
* **Seethal Somisetty** (Member)
* **Sufronia Ganta** (Member)

*Built for the SmartBridge Virtual Internship.*

