<h1 align="center">Lukas Nilsson</h1>

<p align="center">
  AI engineer<br />
  M.S. Computer Science and Information Systems, UNCW · B.S. Business Administration (Information Systems), UNCW
</p>

<p align="center">
  <a href="https://lukas-nilsson.com">Portfolio</a> •
  <a href="https://www.linkedin.com/in/lukas-nilsson7">LinkedIn</a> •
  <a href="mailto:lukas.nilsson.dev@gmail.com">Email</a>
</p>

I build AI and data tools that work on top of real systems. At Atlantic Packaging that means turning
emailed purchase orders into ERP sales orders, checking tax rates against our ERP setup, and letting
the team ask plain-language questions about its own code. On my own I work on market data, risk and
forecasting: a C++ NASDAQ feed handler, Value-at-Risk models put through bank-style backtests, and
probabilistic forecasts checked against what actually happened.

## Now

- **AI Engineer, Atlantic Packaging.** AI and data tools around the company's Infor A+ ERP. I also
  own security and access controls for a new REST API layer in front of the ERP, while an outside
  firm builds the RPG endpoints.
- **M.S. Computer Science and Information Systems, UNCW**, finished May 2026.

Before that, graduate teaching assistant at UNCW, supporting 200+ students in information systems,
software development and databases.

## Selected work

**AI purchase-order processor** · React, Python Azure Functions, Azure OpenAI · Atlantic Packaging<br />
Turns emailed customer POs into validated ERP sales orders, with sales reps reviewing and confirming
what the model produced. It submitted 1,000+ orders in its first three months. When telemetry traced
duplicate ERP orders to timeout-triggered retries, an idempotency guard stopped the repeats.

**[ITCH 5.0 feed handler](https://github.com/LukasUser/market-data-pipeline)** · C++20, CMake, GoogleTest<br />
The first stage of a market data → order book → strategy pipeline. It decodes the NASDAQ
TotalView-ITCH messages that change the order book, with zero-copy framing and fixed-point prices.
On a full NASDAQ trading day of 268.7M messages it runs at 54.7M messages/s (1.68 GB/s). CI runs
GCC and Clang, with AddressSanitizer and UBSan.

**[Wilmington rental pipeline](https://github.com/LukasUser/Wilmington-Rental-Pipeline)** · Databricks, PySpark, Delta Lake, Claude API<br />
A daily Bronze → Silver → Gold pipeline that pulls live rental listings and has Claude score each one
1–10 against our group's preferences, with pros, cons and a summary in a fixed JSON contract. It
scored 50 listings a run, with a dashboard for the 7+ scores and a morning email for the 9s.

**[VaR risk modeling and backtesting engine](https://github.com/LukasUser/VaR-Risk-Modeling-Backtesting-Engine)** · Python, SciPy, Streamlit<br />
Five Value-at-Risk models (historical, parametric, Monte Carlo, GARCH, EVT) forecast out-of-sample
over 2,699 trading days, then judged with Kupiec and Christoffersen tests. Normal-based models broke
2.5× too often. EVT got the rate right (1.19%), and only GARCH's failures weren't clustered.

**[Solar activity and geomagnetic forecasting](https://github.com/LukasUser/Solar-Activity-and-Geomagnetic-Forecasting)** · R<br />
60 years of monthly sunspot, F10.7 flux and Ap index data, forecast six years ahead. A VAR(4)
cut sunspot error by 45% compared with ARIMA. A dynamic regression on solar activity was the best Ap
model, at RMSE 3.15.

**[Australian Open 2024 Monte Carlo](https://github.com/LukasUser/Australian-Open-2024-Monte-Carlo-Simulation)** · Python<br />
A surface-weighted Elo model frozen before the tournament, then used to play the real 128-player draw
100,000 times. Champion Jannik Sinner was its #2 pick, and it named 7 of the 8 quarterfinalists in
its top 8, one more than the seedings did.

**More at Atlantic Packaging:** a sales and use tax monitor that checks official rates nationwide
against our ERP setup, an in-house alternative to vendor tools quoted at $150K+; a D3 profitability
and seasonality explorer over 10 years of sales that surfaced $164M in intercompany transfers
overstating sales; and a RAG system over 100+ GitHub and Azure DevOps repositories.

## Tech

**Languages**<br />
<img src="https://img.shields.io/badge/-Python-05122A?style=flat&logo=python" />
<img src="https://img.shields.io/badge/-TypeScript-05122A?style=flat&logo=typescript" />
<img src="https://img.shields.io/badge/-SQL-05122A?style=flat&logo=postgresql" />
<img src="https://img.shields.io/badge/-C%23-05122A?style=flat&logo=dotnet" />
<img src="https://img.shields.io/badge/-C++-05122A?style=flat&logo=cplusplus" />
<img src="https://img.shields.io/badge/-R-05122A?style=flat&logo=r" />

**Libraries and frameworks**<br />
<img src="https://img.shields.io/badge/-React-05122A?style=flat&logo=react" />
<img src="https://img.shields.io/badge/-FastAPI-05122A?style=flat&logo=fastapi" />
<img src="https://img.shields.io/badge/-NumPy-05122A?style=flat&logo=numpy" />
<img src="https://img.shields.io/badge/-Pandas-05122A?style=flat&logo=pandas" />
<img src="https://img.shields.io/badge/-SciPy-05122A?style=flat&logo=scipy" />
<img src="https://img.shields.io/badge/-scikit--learn-05122A?style=flat&logo=scikitlearn" />
<img src="https://img.shields.io/badge/-Matplotlib-05122A?style=flat" />
<img src="https://img.shields.io/badge/-PySpark-05122A?style=flat&logo=apachespark" />
<img src="https://img.shields.io/badge/-Streamlit-05122A?style=flat&logo=streamlit" />
<img src="https://img.shields.io/badge/-forecast_(R)-05122A?style=flat&logo=r" />

**AI applications**<br />
<img src="https://img.shields.io/badge/-RAG_%2F_LLM_apps-05122A?style=flat" />
<img src="https://img.shields.io/badge/-Azure_OpenAI-05122A?style=flat" />
<img src="https://img.shields.io/badge/-Claude_API-05122A?style=flat&logo=anthropic" />
<img src="https://img.shields.io/badge/-Azure_Functions-05122A?style=flat" />

**Platforms and integration**<br />
<img src="https://img.shields.io/badge/-Azure_DevOps-05122A?style=flat" />
<img src="https://img.shields.io/badge/-Databricks-05122A?style=flat&logo=databricks" />
<img src="https://img.shields.io/badge/-Delta_Lake-05122A?style=flat" />
<img src="https://img.shields.io/badge/-Docker-05122A?style=flat&logo=docker" />
<img src="https://img.shields.io/badge/-CMake-05122A?style=flat&logo=cmake" />
<img src="https://img.shields.io/badge/-Git-05122A?style=flat&logo=git" />
<img src="https://img.shields.io/badge/-GitHub-05122A?style=flat&logo=github" />
<img src="https://img.shields.io/badge/-REST_APIs-05122A?style=flat" />
<img src="https://img.shields.io/badge/-IBM_Db2_for_i-05122A?style=flat" />
<img src="https://img.shields.io/badge/-ERP_%2F_EDI-05122A?style=flat" />
