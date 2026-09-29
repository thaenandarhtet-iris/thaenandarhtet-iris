# Hi, I'm Iris

**Analytics engineer / data engineer.** I build tested data pipelines and models that turn raw data into numbers people can trust, and I check that they reconcile.

- Modelling with dbt and SQL: dimensional models, slowly changing dimensions, metrics that reconcile
- Pipelines that run end to end from one command, with data tests and CI on every push
- Python for ingestion, forecasting and tooling; Tableau for the last mile

## Projects

### [SaaS Subscription Analytics Pipeline](https://github.com/thaenandarhtet-iris/saas-analytics-pipeline)
dbt + DuckDB pipeline modelling three years of subscription revenue: SCD Type 2 subscriptions, an MRR bridge that reconciles exactly to the monthly snapshot, churn and cohort retention, and a [Tableau Public dashboard](https://public.tableau.com/app/profile/iris.htet/viz/saas-analytics-dashboard/Dashboard). 12 models and 48 data tests run in CI on every push.

`dbt` `DuckDB` `SQL` `Python` `Tableau` `GitHub Actions`

### [TalkToData: English to SQL](https://github.com/thaenandarhtet-iris/talktodata-text-to-sql-assistant)
Ask a question in plain English and get the SQL, the result table and a one-sentence answer. It uses the Claude API, runs as a read-only database user, and is scored on a 25-question test set: 100% with schema hints vs 80–84% without them.

`Python` `LLM` `MySQL` `Streamlit` `Docker` `pytest`

### [RetailStock Demand Forecaster](https://github.com/thaenandarhtet-iris/retailstock-demand-forecaster)
Prophet forecasts for 500 retail SKUs (11.6% error vs 21.3% for a naive baseline), turned into safety stock and reorder points. Sizing the buffer from forecast error instead of past sales variability needed 48% less stock and gave fewer stockouts.

`Python` `Prophet` `pandas` `time series` `Tableau`

## Tools

**Languages:** SQL, Python
**Data engineering:** dbt, DuckDB, MySQL, data testing, CI/CD with GitHub Actions, Docker
**Analysis:** pandas, Prophet, time series forecasting
**Visualisation:** Tableau, Streamlit, matplotlib
**Engineering practice:** Git, pytest, reproducible one-command pipelines
