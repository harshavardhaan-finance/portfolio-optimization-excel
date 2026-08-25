# Portfolio Analytics, Optimization & Risk Management Using Excel

## Overview

This project develops an integrated **equity portfolio analytics, optimization, and risk management model using Microsoft Excel**.

The model evaluates a portfolio of five Indian equities across historical performance, statistical relationships, risk-adjusted returns, portfolio construction, Monte Carlo simulation, Value at Risk (VaR), stress testing, and futures-based hedging.

The objective is to demonstrate how quantitative finance techniques can be combined into a single analytical framework to support **portfolio allocation, risk assessment, and investment decision-making**.

> **Note:** The Excel model, calculations, formulas, optimization framework, simulations, and analysis were built as part of the project. Some project framing and documentation were assisted by AI.

---

## Project Objective

The primary objective is to construct an optimized equity portfolio that balances **expected return and portfolio risk**, while also evaluating potential downside scenarios and hedging requirements.

The project addresses questions such as:

* How have the selected stocks performed historically?
* How are the stocks related to each other?
* Which securities offer the strongest risk-adjusted performance?
* What is the optimal portfolio allocation under defined constraints?
* What return and volatility can be expected from the optimized portfolio?
* How could the portfolio perform under simulated future outcomes?
* What are the potential losses at different confidence levels?
* How does portfolio risk change under adverse market scenarios?
* How many index futures contracts could be required to hedge the portfolio?

---

## Portfolio

The analysis covers five Indian equities:

| Security   | Ticker / Reference            |
| ---------- | ----------------------------- |
| Maruti     | Maruti Suzuki India           |
| Sun Pharma | Sun Pharmaceutical Industries |
| HUL        | Hindustan Unilever            |
| Infosys    | Infosys                       |
| HDFC Bank  | HDFC Bank                     |

The portfolio is evaluated against the **Nifty 50** as the market benchmark.

---

## Methodology

The workbook combines several quantitative finance techniques into one integrated model.

### 1. Historical Return Analysis

Historical price data is processed to calculate:

* Daily returns
* Annualized returns
* Standard deviation
* Variance
* Median
* Skewness
* Kurtosis

This provides an initial view of the return characteristics and volatility of each security.

### 2. Correlation & Covariance Analysis

A correlation and covariance matrix is constructed to understand the relationships between securities.

This is used to evaluate the potential diversification benefits of combining assets with different return patterns.

### 3. Performance Measurement

Individual securities are evaluated using:

* Beta
* CAPM expected return
* Actual return
* Alpha
* Sharpe Ratio

The model compares realized returns with CAPM-based required returns to identify securities that generated positive or negative excess returns.

### 4. Portfolio Optimization

The portfolio is optimized using **Modern Portfolio Theory (MPT)** and Microsoft Excel Solver.

Portfolio constraints include:

* Minimum allocation: 5% per security
* Maximum allocation: 25% per security
* Total portfolio allocation: 100%

The optimization framework evaluates the trade-off between expected portfolio return and portfolio volatility.

### 5. Efficient Frontier

The model incorporates an **Efficient Frontier** analysis to examine combinations of portfolio return and risk.

This provides a visual framework for understanding how different portfolio allocations affect the risk-return trade-off.

### 6. Monte Carlo Simulation

A **10,000-iteration Monte Carlo simulation** is used to estimate possible future portfolio outcomes.

The model uses the portfolio's expected return and volatility to generate simulated outcomes over a 252-day investment horizon.

A separate daily simulation is also included in the workbook.

### 7. Value at Risk

The project incorporates both:

* Parametric VaR
* Monte Carlo VaR

VaR is evaluated at:

* 95% confidence level
* 99% confidence level

This provides an estimate of potential portfolio losses under specified probability assumptions.

### 8. Stress Testing

The portfolio is evaluated under multiple adverse market scenarios to understand how losses could develop during increasingly severe market declines.

This helps assess portfolio resilience beyond normal market conditions.

### 9. Portfolio Hedging

The model evaluates a **Nifty futures-based hedging strategy**.

It calculates:

* Portfolio exposure
* Futures contract value
* Number of contracts required
* Hedge ratios
* Different hedging levels

The analysis considers hedge ratios of:

* 100%
* 75%
* 50%
* 25%

This demonstrates how derivatives can potentially be used to reduce systematic market exposure.

---

## Key Portfolio Results

The optimization model produces the following portfolio allocation under the defined constraints:

| Security   | Optimal Weight |
| ---------- | -------------: |
| Maruti     |            25% |
| Sun Pharma |            25% |
| HUL        |            20% |
| Infosys    |             5% |
| HDFC Bank  |            25% |
| **Total**  |       **100%** |

### Optimized Portfolio Metrics

| Metric                       |     Result |
| ---------------------------- | ---------: |
| Expected Return              |  **8.58%** |
| Portfolio Standard Deviation | **13.54%** |
| Risk-Free Rate               |  **6.75%** |
| Sharpe Ratio                 |  **0.135** |
| Portfolio Beta               |  **0.781** |
| Portfolio Alpha              |  **0.37%** |

The resulting portfolio maintains diversification across all five securities while respecting the predefined allocation limits.

---

## Individual Security Insights

The performance analysis highlights meaningful differences across the selected securities.

### Sun Pharma

Sun Pharma recorded the strongest historical return among the five securities in the model and also produced the highest individual Sharpe Ratio.

### Maruti

Maruti generated a positive historical return and positive alpha while maintaining a beta below 1, indicating lower systematic market sensitivity than the benchmark in the model.

### HUL

HUL generated a negative historical return during the analyzed period, resulting in negative alpha and a negative Sharpe Ratio.

### Infosys

Infosys also recorded negative historical performance in the analyzed dataset, accompanied by negative alpha and Sharpe Ratio.

### HDFC Bank

HDFC Bank produced a positive historical return but exhibited a beta above 1, indicating relatively higher sensitivity to movements in the market benchmark.

---

## Monte Carlo Simulation

The annual Monte Carlo model runs **10,000 simulations** using:

* Initial portfolio investment
* Expected portfolio return
* Portfolio standard deviation
* 252-day investment horizon

The simulations generate a distribution of potential portfolio outcomes rather than relying on a single expected-return forecast.

This allows the model to examine the range of possible future portfolio values and better visualize uncertainty around the expected outcome.

---

## Risk Management Framework

The project follows a layered risk-management approach:

```text
Historical Data
      ↓
Return & Statistical Analysis
      ↓
Correlation / Covariance
      ↓
Performance Metrics
      ↓
Portfolio Optimization
      ↓
Efficient Frontier
      ↓
Monte Carlo Simulation
      ↓
VaR & Stress Testing
      ↓
Futures Hedging
```

This structure connects portfolio construction with subsequent risk measurement and mitigation.

---

## Excel Workbook Structure

The workbook contains the following major sections:

| Sheet                     | Purpose                                 |
| ------------------------- | --------------------------------------- |
| Problem Statement         | Project objective and scope             |
| Returns                   | Return calculations                     |
| Statistics                | Descriptive statistical analysis        |
| Correlation & Covariance  | Asset relationship analysis             |
| Performance Metrics       | Beta, CAPM, Alpha and Sharpe Ratio      |
| Portfolio Optimizer       | Optimal portfolio allocation            |
| Efficient Frontier        | Risk-return portfolio analysis          |
| Monte Carlo Simulation    | 10,000 annual simulations               |
| Risk Analysis and Hedging | VaR, stress testing and futures hedging |
| MCS(Daily)                | Daily Monte Carlo simulation            |
| Maruti                    | Security-level data                     |
| Sun Pharma                | Security-level data                     |
| HUL                       | Security-level data                     |
| Infosys                   | Security-level data                     |
| HDFC Bank                 | Security-level data                     |
| Nifty 50                  | Benchmark data                          |

---

## Tools & Techniques

**Tools**

* Microsoft Excel
* Excel Solver

**Finance & Quantitative Techniques**

* Modern Portfolio Theory
* Portfolio Optimization
* Efficient Frontier
* CAPM
* Beta
* Alpha
* Sharpe Ratio
* Correlation & Covariance Analysis
* Monte Carlo Simulation
* Value at Risk
* Stress Testing
* Futures Hedging

---

## Key Takeaways

The project demonstrates how an investor can move from **raw market data to portfolio construction and risk management** within a single analytical framework.

Key takeaways include:

1. Portfolio construction should consider both return and risk rather than maximizing historical returns alone.
2. Correlation between securities plays an important role in diversification.
3. Risk-adjusted metrics can provide a different perspective from absolute returns.
4. Optimization constraints materially affect the resulting portfolio allocation.
5. Monte Carlo simulation illustrates the uncertainty surrounding future portfolio outcomes.
6. VaR and stress testing provide complementary approaches to understanding downside risk.
7. Index futures can be incorporated into a portfolio risk-management framework to reduce market exposure.

---

## Limitations

The model is intended as an **analytical and educational portfolio-management framework**, rather than a live investment recommendation.

Important limitations include:

* Historical returns do not guarantee future performance.
* Monte Carlo results depend on the assumptions and statistical characteristics used as inputs.
* CAPM relies on simplifying assumptions regarding expected returns and systematic risk.
* VaR does not describe the full distribution of losses beyond the selected confidence level.
* Stress-test outcomes are scenario-dependent.
* Futures prices, contract specifications, and market conditions can change over time.
* Transaction costs, taxes, liquidity constraints, and slippage are not comprehensively incorporated.

---

## Repository Contents

```text
portfolio-optimization-excel/
│
├── README.md
├── Portfolio Optimization using Excel.xlsx
│
├── screenshots/
│   ├── portfolio-optimizer.png
│   ├── efficient-frontier.png
│   ├── monte-carlo.png
│   └── risk-hedging.png
│
└── docs/
    └── Portfolio Optimization Report.pdf
```

*The `screenshots` and `docs` folders are optional and can be added if supporting materials are uploaded to the repository.*

---

## Disclaimer

This project is for **educational and portfolio-analysis purposes only**. It does not constitute investment advice or a recommendation to buy or sell any security or derivative.

---

## Author

**Harshavardhaan**

Finance | Financial Analysis | Valuation | Quantitative Finance | Data Analytics

