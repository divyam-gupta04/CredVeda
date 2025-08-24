# CredVeda: AI-Powered Credit Intelligence Platform  

CredVeda is an **end-to-end platform** designed to provide **dynamic, real-time, and explainable credit risk scores** for publicly traded companies.  

Traditional credit rating models are often slow, retrospective, and lack transparency.  
CredVeda leverages a **hybrid data approach**, fusing structured financial data with unstructured market sentiment to deliver **forward-looking predictions** and **clear insights** into a company's financial health.  

---

## Core Features  

- **Dynamic Credit Scoring**  
  - XGBoost ML model generates daily credit scores (0–100) based on predicted 30-day forward returns.  

- **Hybrid Data Fusion**  
  - Ingests data from 4 APIs: Yahoo Finance, FRED, NewsAPI, API Ninjas.  

- **Explainable AI (XAI)**  
  - SHAP provides transparent insights into the **top 3 drivers** behind each credit score.  

- **Full-Stack Web Dashboard** (Flask + SQLite)  
  - User Authentication (Login/Register)  
  - Interactive Dashboard with visualizations  
  - Detailed company analysis pages  

- **AI-Powered Chatbot**  
  - Conversational interface for querying credit scores + explanations.  

- **Multi-Market Analysis**  
  - Supports both **US (S&P 500)** and **Indian (NSE)** companies.  

---

## Tech Stack  

**Backend:** Python, Flask  
**Database:** SQLite  
**Machine Learning:** Scikit-learn, XGBoost, SHAP  
**Data Processing:** Pandas, NumPy  
**Frontend:** HTML, Tailwind CSS, JavaScript, Chart.js  
**APIs:** Yahoo Finance, FRED, NewsAPI, API Ninjas  

---

## Project Structure  

```text
CredVeda/
│── config.py          # Central config (tickers, features, API keys)
│── database.py        # SQLite DB setup
│── data_ingestion.py  # Ingests US market data
│── ingest_ns.py       # Ingests Indian market data
│── model_training.py  # ML training pipeline
│── scoring.py         # Generates scores + SHAP explanations
│── app.py             # Flask web app
│── chatbot.py         # Chatbot logic
│── requirements.txt   # Dependencies
│── .env               # API keys (not committed)
```


---

## Setup & Installation  

1. **Clone the Repository**  
   git clone https://github.com/your-username/CredVeda.git  
   cd CredVeda  

2. **Create & Activate a Virtual Environment**  

   Windows:  
   python -m venv venv  
   venv\Scripts\activate  

   macOS/Linux:  
   python3 -m venv venv  
   source venv/bin/activate  

3. **Install Dependencies**  
   pip install -r requirements.txt  

4. **Set Up API Keys**  
   Create a `.env` file in the project root:  
   NEWS_API_KEY="YOUR_NEWS_API_KEY_HERE"  
   API_NINJAS_KEY="YOUR_API_NINJAS_KEY_HERE"  

---

## Running the Pipeline  

1. **Set Up Database** (run once)  
   python database.py  

2. **Ingest Data**  
   python data_ingestion.py  
   python ingest_ns.py  

3. **Train Model**  
   python model_training.py xgb  

4. **Generate Scores**  
   python scoring.py xgb  

5. **Launch Web Application**  
   python app.py  

 


