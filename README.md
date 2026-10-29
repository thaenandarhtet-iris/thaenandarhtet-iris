# Hi, I'm Iris 👋

**Industrial Engineering student at Georgia Tech**, concentrating in data science and analytics, and exploring AI and operations research.

I build tested data pipelines and models that turn raw data into numbers people can trust, and I check that they reconcile. I'm now looking for research opportunities where I can ask harder questions of data, not just report on it.

- Modelling with dbt and SQL: dimensional models, slowly changing dimensions, metrics that reconcile
- Pipelines that run end to end from one command, with data tests and CI on every push
- Python for ingestion, forecasting, causal estimates and tooling; Tableau for the last mile

## Research interests

The questions my projects keep running into, and the ones I want to study properly:

- **Evaluating LLM systems:** how to measure when a model is right, where it fails, and why. In TalkToData, a small ablation showed that guessed category codes caused every miss; I want to find failure modes like that automatically and at scale.
- **Causal inference from observational data:** estimating promotion lift and price elasticity when prices weren't set at random, and being honest about when the estimates can't be trusted.
- **Forecasting under uncertainty:** turning forecast error into decisions, such as how much safety stock to hold, and understanding why methods that work on smooth data fall apart on sparse, intermittent demand.
- **Data quality and validation:** tests that prove a pipeline recovers what is known to be in the data, so the numbers coming out can be trusted.

I'm interested in research assistant roles and research-focused programs in these areas. If you're working on something related, I'd be glad to hear from you.

## Projects

### [SaaS Subscription Analytics Pipeline](https://github.com/thaenandarhtet-iris/saas-analytics-pipeline)
dbt + DuckDB pipeline modelling three years of subscription revenue: SCD Type 2 subscriptions, one shared customer-by-month model behind every monthly metric, an MRR bridge that reconciles exactly to the month-end snapshot, churn and cohort retention, and a [Tableau Public dashboard](https://public.tableau.com/app/profile/iris.htet/viz/saas-analytics-dashboard/Dashboard). 14 models and 59 data tests, plus 13 pytest tests that check the data generator produces the patterns it was configured with, all run in CI on every push.

`dbt` `DuckDB` `SQL` `Python` `pytest` `Tableau` `GitHub Actions`

### [TalkToData: English to SQL](https://github.com/thaenandarhtet-iris/talktodata-text-to-sql-assistant)
Ask a question in plain English and get the SQL, the result table and a one-sentence answer. It uses the Claude API, runs as a read-only database user, and is scored on a 25-question test set: 100% with schema hints vs 80–84% without them, with every miss traced to a guessed code value. Next on the roadmap: embedding retrieval so only the relevant schema reaches the prompt, and clustering failures on a harder benchmark to find error types automatically.

`Python` `LLM` `evaluation` `MySQL` `Streamlit` `Docker` `pytest`

### [RetailStock Demand Forecaster](https://github.com/thaenandarhtet-iris/retailstock-demand-forecaster)
Prophet forecasts for 500 retail SKUs (11.6% error vs 21.3% for a naive baseline), turned into safety stock and reorder points. Sizing the buffer from forecast error instead of past sales variability needed 48% less stock and gave fewer stockouts.

**2.0 adds price and promotion analysis** on Walmart M5 data: promotion lift by difference-in-differences (median +58%, yet only about half of promotions made money), per-item price elasticity with shrinkage, a rolling backtest of price-aware forecasts, and a daily-scraped competitor price index built from Open Prices data.

`Python` `Prophet` `pandas` `time series` `causal inference` `Selenium` `Tableau`

## Tools

**Languages:** SQL, Python
**Data engineering:** dbt, DuckDB, MySQL, data testing, CI/CD with GitHub Actions, Docker
**Analysis:** pandas, Prophet, time series forecasting, regression, difference-in-differences
**LLMs:** Claude API, prompt design, evaluation with gold sets and ablations
**Data collection:** REST APIs, Selenium, scheduled scrapes
**Visualisation:** Tableau, Streamlit, matplotlib
**Engineering practice:** Git, pytest, reproducible one-command pipelines
