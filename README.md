<p align="center">
  <img src="assets/banner.svg" width="100%" alt="Lukas Nilsson. AI engineer, data pipelines, markets and forecasting. Atlantic Packaging; M.S. CS and IS, UNCW." />
</p>

<p align="center">
  <a href="https://lukas-nilsson.com"><img src="https://img.shields.io/badge/-lukas--nilsson.com-121a2f?style=for-the-badge&logo=googlechrome&logoColor=2dd4bf" alt="Portfolio" /></a>
  <a href="https://www.linkedin.com/in/lukas-nilsson7"><img src="https://img.shields.io/badge/-LinkedIn-0A66C2?style=for-the-badge" alt="LinkedIn" /></a>
  <a href="mailto:lukas.nilsson.dev@gmail.com"><img src="https://img.shields.io/badge/-lukas.nilsson.dev@gmail.com-121a2f?style=for-the-badge&logo=gmail&logoColor=fbbf24" alt="Email" /></a>
</p>

I build AI and data tools that work on top of real systems: an LLM that turns emailed purchase orders
into ERP sales orders, a monitor that checks tax rates against our ERP, and plain-language search over
our own code. On my own time it's markets, risk and forecasting. That means a C++ NASDAQ feed handler,
Value-at-Risk models put through bank-style backtests, and forecasts checked against what actually
happened.

**Now** · AI Engineer at Atlantic Packaging, building AI and data tools around its Infor A+ ERP and
owning security and access controls for a new REST API layer in front of it.<br />
**Before** · M.S. Computer Science and Information Systems, UNCW (May 2026), and graduate TA for 200+
students in information systems, software development and databases.

## At Atlantic Packaging

<img src="assets/atlantic.svg" width="100%" alt="1,000+ orders submitted by the AI PO processor in 3 months; $150K+ vendor quote replaced by an in-house sales tax monitor; $164M of intercompany transfers found overstating two years of sales; 100+ repositories searchable in plain language through RAG." />

<details>
<summary><b>How these work</b></summary>
<br />

**AI purchase-order processor** · React, Python Azure Functions, Azure OpenAI<br />
Turns emailed customer POs into validated ERP sales orders, with sales reps reviewing and confirming
what the model produced. When telemetry traced duplicate ERP orders to timeout-triggered retries, an
idempotency guard stopped the repeats.

**Sales and use tax monitor**<br />
Checks official tax rate data nationwide against our Infor A+ configuration, then flags each
discrepancy with the affected ship-to locations and supporting evidence for a person to review.

**Profitability and seasonality explorer** · D3<br />
STL decomposition over 10 years and about 5.6M sales lines. The intercompany transfers it surfaced
are now excluded from the analysis.

**Code search with RAG** · Azure OpenAI<br />
Indexes GitHub and Azure DevOps repositories and answers questions grounded in the source, sending the
model only the relevant code to keep token costs low.

</details>

## Selected work

<a href="https://github.com/LukasUser/market-data-pipeline"><img src="assets/itch.svg" width="100%" alt="ITCH 5.0 feed handler: 54.7M messages per second decoding NASDAQ TotalView-ITCH at 1.68 GB/s. C++20, CMake, GoogleTest, ASan/UBSan." /></a>

<a href="https://github.com/LukasUser/Wilmington-Rental-Pipeline"><img src="assets/rental.svg" width="49%" alt="Wilmington rental pipeline: 50 live listings a day scored by Claude. Databricks, PySpark, Claude API." /></a>
<a href="https://github.com/LukasUser/VaR-Risk-Modeling-Backtesting-Engine"><img src="assets/var.svg" width="49%" alt="VaR backtesting engine: 5 models judged over 2,699 trading days. Python, SciPy, Streamlit." /></a>
<a href="https://github.com/LukasUser/Solar-Activity-and-Geomagnetic-Forecasting"><img src="assets/solar.svg" width="49%" alt="Solar and geomagnetic forecasting: 45% lower sunspot RMSE with VAR(4) than ARIMA. R." /></a>
<a href="https://github.com/LukasUser/Australian-Open-2024-Monte-Carlo-Simulation"><img src="assets/ao.svg" width="49%" alt="Australian Open 2024 Monte Carlo: 100,000 simulated tournaments. Python." /></a>

<details>
<summary><b>Read the write-ups</b></summary>
<br />

**[ITCH 5.0 feed handler](https://github.com/LukasUser/market-data-pipeline)**<br />
The first stage of a market data → order book → strategy pipeline. It decodes the NASDAQ
TotalView-ITCH messages that change the order book, with zero-copy framing and fixed-point prices. On
a full trading day of 268.7M messages it runs at 54.7M messages/s from an uncompressed file. CI runs
GCC and Clang, with AddressSanitizer and UBSan.

**[Wilmington rental pipeline](https://github.com/LukasUser/Wilmington-Rental-Pipeline)**<br />
A daily Bronze → Silver → Gold pipeline that pulls live rental listings and has Claude score each one
1–10 against our group's preferences, with pros, cons and a summary in a fixed JSON contract. A
dashboard shows the 7+ scores and a morning email flags the 9s.

**[VaR risk modeling and backtesting engine](https://github.com/LukasUser/VaR-Risk-Modeling-Backtesting-Engine)**<br />
Five Value-at-Risk models (historical, parametric, Monte Carlo, GARCH, EVT) forecast out-of-sample
over 2,699 trading days, then judged with Kupiec and Christoffersen tests. Normal-based models broke
2.5× too often. EVT got the rate right (1.19%), and only GARCH's failures weren't clustered.

**[Solar activity and geomagnetic forecasting](https://github.com/LukasUser/Solar-Activity-and-Geomagnetic-Forecasting)**<br />
60 years of monthly sunspot, F10.7 flux and Ap index data, forecast six years ahead. A VAR(4) cut
sunspot error by 45% compared with ARIMA. A dynamic regression on solar activity was the best Ap
model, at RMSE 3.15.

**[Australian Open 2024 Monte Carlo](https://github.com/LukasUser/Australian-Open-2024-Monte-Carlo-Simulation)**<br />
A surface-weighted Elo model frozen before the tournament, then used to play the real 128-player draw
100,000 times. Champion Jannik Sinner was its #2 pick, and it named 7 of the 8 quarterfinalists in its
top 8, one more than the seedings did.

</details>

## Tech

<p>
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/SQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" alt="SQL" />
  <img src="https://img.shields.io/badge/C%23-512BD4?style=flat-square&logo=dotnet&logoColor=white" alt="C#" />
  <img src="https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white" alt="C++" />
  <img src="https://img.shields.io/badge/R-276DC3?style=flat-square&logo=r&logoColor=white" alt="R" />
</p>
<p>
  <img src="https://img.shields.io/badge/Azure_OpenAI-0078D4?style=flat-square" alt="Azure OpenAI" />
  <img src="https://img.shields.io/badge/Claude_API-D97757?style=flat-square&logo=anthropic&logoColor=white" alt="Claude API" />
  <img src="https://img.shields.io/badge/RAG_%2F_LLM_apps-6E40C9?style=flat-square" alt="RAG / LLM apps" />
  <img src="https://img.shields.io/badge/Azure_Functions-0062AD?style=flat-square" alt="Azure Functions" />
  <img src="https://img.shields.io/badge/React-20232A?style=flat-square&logo=react&logoColor=61DAFB" alt="React" />
  <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white" alt="FastAPI" />
  <img src="https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white" alt="Streamlit" />
</p>
<p>
  <img src="https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white" alt="NumPy" />
  <img src="https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white" alt="Pandas" />
  <img src="https://img.shields.io/badge/SciPy-8CAAE6?style=flat-square&logo=scipy&logoColor=white" alt="SciPy" />
  <img src="https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white" alt="scikit-learn" />
  <img src="https://img.shields.io/badge/Matplotlib-11557C?style=flat-square" alt="Matplotlib" />
  <img src="https://img.shields.io/badge/PySpark-E25A1C?style=flat-square&logo=apachespark&logoColor=white" alt="PySpark" />
  <img src="https://img.shields.io/badge/forecast_(R)-276DC3?style=flat-square&logo=r&logoColor=white" alt="forecast (R)" />
</p>
<p>
  <img src="https://img.shields.io/badge/Databricks-FF3621?style=flat-square&logo=databricks&logoColor=white" alt="Databricks" />
  <img src="https://img.shields.io/badge/Delta_Lake-00ADD4?style=flat-square" alt="Delta Lake" />
  <img src="https://img.shields.io/badge/Azure_DevOps-0078D7?style=flat-square" alt="Azure DevOps" />
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" alt="Docker" />
  <img src="https://img.shields.io/badge/CMake-064F8C?style=flat-square&logo=cmake&logoColor=white" alt="CMake" />
  <img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white" alt="Git" />
  <img src="https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white" alt="GitHub" />
  <img src="https://img.shields.io/badge/REST_APIs-2a3550?style=flat-square" alt="REST APIs" />
  <img src="https://img.shields.io/badge/IBM_Db2_for_i-052FAD?style=flat-square" alt="IBM Db2 for i" />
  <img src="https://img.shields.io/badge/ERP_%2F_EDI-2a3550?style=flat-square" alt="ERP / EDI" />
</p>
