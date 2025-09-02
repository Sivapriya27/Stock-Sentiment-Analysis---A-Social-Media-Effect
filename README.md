# Stock Sentiment Analysis: The Social Media Effect 📈🐦

**Live Project:** [waynegretzky1.github.io/stock-sentiment-analysis]
(https://waynegretzky1.github.io/stock-sentiment-analysis/)  

**Does Twitter sentiment move stock prices?**  
This project investigates how social media sentiment correlates with U.S. stock returns, using **860K+ tweets**, **financial APIs**, and **NLP models**.  
It combines Python-based analysis with an interactive **Svelte web app**.

---

## ✨ Project Highlights

- **Dataset:** 860K+ sentiment-tagged tweets (2021–2022), Yahoo Finance stock prices, Kaggle sentiment datasets.  
- **Models:** TextBlob, LSTM-based sentiment classifier, transformer-based BERT (primary).  
- **Visualizations:** Line charts, correlation bar charts, Granger causality heatmaps.  
- **Frontend:** Svelte-based interactive web app with hoverable tweets, scroll storytelling, and dynamic plots.  
- **Key finding:** Sentiment often **predicts** stock returns in real-time, with Tesla as a unique case of two-way causality.

---

## 📊 Core Analyses

### 1. Sentiment vs Stock Returns
- Compared daily sentiment averages with 1–7 day returns.  
- **Finding:** Returns rose and fell in sync with sentiment trends across most stocks.  

### 2. Lag Correlation
- Tested sentiment vs returns with ±7 day lags.  
- **Finding:** 6/11 stocks showed strongest correlation at **0-day lag** → markets react almost instantly to social chatter.  

### 3. Granger Causality
- Tested predictive power in both directions.  
- **Finding:**  
  - **Sentiment → Returns**: Significant predictive strength across most stocks.  
  - **Returns → Sentiment**: Weak or none.  
  - **Exception:** Tesla showed **mutual causality**, reflecting its unique volatility and hype-driven cycle.  

---

## 📂 Project structure

- stock-sentiment-analysis/
- data analysis/ #data cleaning, modeling, analysis notebooks
- src/ # interactive Svelte website
- static/ # Media
- docs/ # final PDF report
- requirements.txt
- README.md

---

## 🛠️ Tools & Stack

- **Python**: Pandas, NumPy, SciPy (data wrangling, correlation)  
- **NLP**: TextBlob, LSTM, BERT (sentiment scoring)  
- **Visualization**: Matplotlib, Plotly (prototyping)  
- **Frontend**: Svelte (interactive charts, scroll storytelling)  
- **Collab/Infra**: Google Colab, GitHub  

---

## 📑 Documentation

Full methodology, results, and evaluation:  
[`docs/Stock sentiment analysis - Project Report.pdf`](docs/Stock sentiment analysis - Project Report.pdf)

---

## 🔮 Roadmap (nice-to-haves)

- Refine sentiment models (**FinBERT, RoBERTa**) for finance-specific sentiment detection.  
- Add **sector-wise dashboards** comparing sentiment vs performance across industries.  
- Integrate **live tweet streaming** with real-time stock price overlays.  
- Expand **causality testing** to multi-year and multi-market datasets.  

---
## 🚀 Quick start (Analysis)

> Requires Python 3.9+

```bash
# Clone
git clone https://github.com/<your-username>/stock-sentiment-analysis.git
cd stock-sentiment-analysis

## 🌐 Website (Svelte Frontend)

The interactive data story is built primarily with **Svelte**.

# Virtual environment
python -m venv .venv
source .venv/bin/activate   # macOS/Linux
.venv\Scripts\activate      # Windows

# Install dependencies
pip install -r requirements.txt

### Run locally

```bash
# Go to frontend
cd web

# Install dependencies
npm install

# Start dev server
npm run dev






