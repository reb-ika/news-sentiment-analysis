# news-sentiment-analysis
# News Sentiment Analysis — Week 1

## Project Overview
Analysis of financial news sentiment and its correlation with 
stock price movements for Nova Financial Solutions.

## Setup Instructions
1. Clone: `git clone https://github.com/YOUR_USERNAME/news-sentiment-analysis`
2. Create venv: `python -m venv venv`
3. Activate (Windows): `source venv/Scripts/activate`
4. Install: `pip install -r requirements.txt`

## Project Structure
- notebooks/ - Analysis notebooks
- src/        - Source code
- scripts/    - Helper scripts
- tests/      - Unit tests
- data/raw/   - Raw data (not committed)

# Predicting Price Moves with News Sentiment
**Kifiya AI Training Program — Week 1**
*Nova Financial Solutions | Data Analytics Challenge*

---

## Business Objective
Nova Financial Solutions aims to enhance its predictive analytics capabilities by connecting financial news sentiment to stock price movements. This project builds a rigorous analytical pipeline that:
1. Quantifies sentiment expressed in financial news headlines using NLP
2. Computes technical indicators from historical stock price data
3. Measures statistical correlation between news sentiment and daily stock returns

The target stocks analyzed are: **AAPL, AMZN, GOOG, META, NVDA**



## Setup Instructions

### 1. Clone the repository
```bash
git clone https://github.com/reb-ika/news-sentiment-analysis.git
cd news-sentiment-analysis
```

### 2. Create and activate virtual environment
```bash
# Create
python -m venv venv

# Activate (Windows)
source venv/Scripts/activate

# Activate (Mac/Linux)
source venv/bin/activate
```

### 3. Install dependencies
```bash
pip install -r requirements.txt
```

### 4. Add data files
Download the following files and place them in `data/raw/`:
- `raw_analyst_ratings.csv` — FNSPID Financial News Dataset
- `AAPL.csv`, `AMZN.csv`, `GOOG.csv`, `META.csv`, `NVDA.csv` — YFinance stock price data

> ⚠️ Data files are excluded from version control via `.gitignore`

### 5. Launch Jupyter
```bash
jupyter notebook
# OR open notebooks/ folder in VS Code
```

---

## Notebooks

| Notebook | Task | Description |
|----------|------|-------------|
| `task_1_eda.ipynb` | Task 1 | Exploratory data analysis of 1.4M financial news headlines — headline length, publisher analysis, time series, keyword extraction |
| `task_2_technical_indicators.ipynb` | Task 2 | Technical indicator computation and visualization using TA-Lib — SMA, EMA, RSI, MACD, Bollinger Bands for all 5 stocks |
| `task_3_sentiment_correlation.ipynb` | Task 3 | VADER sentiment analysis, date alignment, daily return computation, Pearson correlation analysis, investment strategy recommendations |

---

## Data Sources

| Dataset | Source | Coverage |
|---------|--------|----------|
| Financial News | FNSPID (Benzinga) | Apr 2011 – Jun 2020, 1,407,328 articles |
| Stock Prices | YFinance | Jan 2009 – Dec 2023, daily OHLCV |

---

## CI/CD

GitHub Actions workflow (`.github/workflows/unittests.yml`) runs automatically on every push to main:
- Sets up Python 3.11
- Installs all dependencies from `requirements.txt`
- Validates the environment is reproducible

---

## Key Findings

**Task 1 — EDA:**
- Dataset spans 1,407,328 articles across 6,204 stocks and 1,034 publishers
- Publication volume spiked dramatically in March 2020 (COVID-19 crash)
- Top keywords: earnings, EPS, upgrades, downgrades — confirming sentiment-relevant vocabulary
- News peaks at 2:00 PM EST during active market hours

**Task 2 — Technical Indicators:**
- All 5 stocks show strong bullish trends throughout 2023
- NVDA recorded the most extreme MACD reading (15) during the June 2023 AI rally
- META RSI touched above 80 in February 2023 during its recovery
- Bollinger Band squeeze-and-breakout pattern visible in AAPL early 2023

**Task 3 — Sentiment Correlation:**
- VADER sentiment applied to filtered news for 5 target stocks
- Pearson correlation computed between average daily sentiment and daily returns
- Investment strategy recommendations derived from combined sentiment and technical signals

---

## Tools & Libraries

| Tool | Purpose |
|------|---------|
| Python 3.14 | Core language |
| Pandas | Data manipulation |
| TA-Lib | Technical indicators (SMA, EMA, RSI, MACD, Bollinger Bands) |
| VADER Sentiment | NLP sentiment scoring |
| Matplotlib / Seaborn | Visualization |
| Scikit-learn | MinMaxScaler for normalization |
| SciPy | Pearson correlation, statistical testing |
| Jupyter | Interactive notebooks |

---

## Author
**Rebika Woldeyesus**
Kifiya AI Training Program — Week 1
GitHub: [@reb-ika](https://github.com/reb-ika)
EOF