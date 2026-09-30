# Hugo Magee 👋

**Data analyst who builds** | Python, SQL, ML, AI systems | MSc Business Analytics and Data Science @ IE University, Madrid

🇮🇪 International 400m sprinter for Ireland (PB 46.95s, European U23 relay finalist)

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://linkedin.com/in/hugo-magee-ooo)

> I take messy real world data, turn it into something a person can act on, and check my own numbers before anyone else has to.

Most of what I build starts with a raw source like CRM records, SEC filings, stock fundamentals, Kaggle datasets or my own training logs. It ends with something a team can use: a forecast, a dashboard, an alert or a ranked list. I build quickly with AI coding tools, then spend the time I save on tests and validation. Two of the projects below were rebuilt after I found errors in my own earlier results, and I published what I found.

## 🔭 Now

* **Studying:** MSc Business Analytics and Data Science at IE, Madrid. Available for roles from August 2027.
* **Building:** a tool that drafts security questionnaire answers from a vendor's public trust pages, with a citation for every answer and a flagged gap wherever the evidence is missing
* **Learning:** Spanish (A2, working toward B1)

## 🚀 Featured projects

Each project follows the same shape: what goes in, what I do to it, what comes out.

### 🤖 [medalist](https://github.com/hugomagee/medalist) · an AI agent that enters ML competitions on its own

**In:** a competition bundle (training data, target column, scoring metric, fixed cross validation folds)

**Transformation:** an AI agent designs and runs experiments. The harness around it enforces the rules the agent can't be trusted to keep itself: a holdout set carved off before the agent sees any data, fixed folds, a time and experiment budget, and a SQLite ledger of every run.

**Out:** a valid submission and a written report. On Kaggle Playground S6E3 (4,143 teams) it reached an estimated top 15.8% in 17 experiments with no human input.

**Stack:** Python, LightGBM, XGBoost, CatBoost, SQLite, pytest (139 tests), GitHub Actions

### 📈 [TradeMetrics](https://github.com/hugomagee/TradeMetrics) · portfolio analytics you can check line by line

**In:** daily portfolio values, a trade log and benchmark prices. The repo uses synthetic data; my own account stays private.

**Transformation:** computes Sharpe with confidence intervals, Sortino, CAPM alpha and beta, Value at Risk, and long and short FIFO profit and loss net of commissions.

**Out:** a single file HTML report, plus a notebook that proves every metric against simulated data where the true answer is known in advance.

**Why it exists:** my first version got Sortino, alpha, VaR and FIFO wrong. I rebuilt it test first (79 tests) and removed the Sharpe ratio I used to quote, because one year of returns can't support it.

**Stack:** Python, pandas, NumPy, SciPy, pytest, Jupyter, GitHub Actions

### 🏃 [OptimalAthlete](https://github.com/hugomagee/OptimalAthlete) · the model that taught me about data leakage

**In:** training sessions, wellness metrics and race results for 400m sprinters

**Transformation:** builds 12 features over real calendar windows, trains Random Forest and XGBoost, and scores them with walk forward validation against a simple "recent average" baseline.

**Out:** a Streamlit dashboard and an honest verdict. My first version claimed R² of 0.84. When I audited it, the model was recognising which athlete was racing, not predicting form. I retracted the number and built a demo: on data with zero signal, the old method still reports R² of 0.906.

**Stack:** Python, sklearn, XGBoost, SQLAlchemy, Streamlit, Plotly, pytest (31 tests), GitHub Actions

### 🔎 [GrowthHog](https://github.com/hugomagee/GrowthHog) · a weekly screener for 170+ growth stocks

**In:** fundamentals, prices and news from Polygon, with FMP and yfinance as fallbacks

**Transformation:** computes 8 trailing twelve month metrics, puts each company in a lifecycle stage (Early, Hypergrowth, Scaling, Maturing) and reweights its score to match. Sanity caps and a cyclical sector adjustment stop one off events from looking like quality.

**Out:** a 0 to 100 score per company, an HTML report and a Dash dashboard, refreshed weekly on cron

**Stack:** Python, pandas, Dash, Polygon API, Anthropic API

## 💼 Client work

The code for these is private because it runs on client data. Happy to walk through any of them.

**Fund Recs, Dublin** · fund reconciliation FinTech · GTM Systems and Analytics Intern, 2026

* **Churn early warning:** product telemetry + CRM + revenue records → the company's first account by month table → a Kibana dashboard showing how far ahead usage drops signal revenue decline
* **Pipeline forecast:** 707 resolved CRM deals → a forecast rebuilt in SQL → adopted by the CRO
* **Compliance answers:** internal policy and due diligence documents → a RAG system → answers in seconds instead of a manual search

**Leaving Cert Plus** · EdTech for Ireland's school leaving exams · freelance AI and technical consultant, 2026 to now

* **Maths verification engine:** AI generated exam questions → a deterministic checker validates each one → only verified questions reach students (content costs down about 50%)
* **Content pipelines:** three AI generation pipelines for information subjects, languages and maths
* **Email CRM:** replaced Mailchimp with a custom EU hosted CRM (platform costs down 60%+)

**Side build:** an SEC filing monitor that watches EDGAR for new filings, flags odd lot tender offers and sends Telegram alerts. Deployed on Railway.

## 🛠️ Tech stack

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat&logo=postgresql&logoColor=white)
![R](https://img.shields.io/badge/R-276DC3?style=flat&logo=r&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-150458?style=flat&logo=pandas&logoColor=white)
![scikit learn](https://img.shields.io/badge/scikit_learn-F7931E?style=flat&logo=scikitlearn&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-189FDD?style=flat)
![LightGBM](https://img.shields.io/badge/LightGBM-02569B?style=flat)
![SQLite](https://img.shields.io/badge/SQLite-003B57?style=flat&logo=sqlite&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat&logo=streamlit&logoColor=white)
![Kibana](https://img.shields.io/badge/Kibana-005571?style=flat&logo=kibana&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat&logo=jupyter&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat&logo=githubactions&logoColor=white)
![Railway](https://img.shields.io/badge/Railway-0B0D0E?style=flat&logo=railway&logoColor=white)
![Claude Code](https://img.shields.io/badge/Claude_Code-D97757?style=flat&logo=anthropic&logoColor=white)
