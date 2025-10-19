# Masters Dissertation

## Asset Allocation and Portfolio Optimisation

### Project Workflow: 
 ## Predicting returns of ETFs tailored to Indian Market and Portfolio optimisation depending on investor's risk profile

## Project Objective:

The objective is to find the optimal portfolio allocation depending on the investor's risk tolerance, investment goal, and time horizon. ETFs with a low embedded cost, natural tax efficiencies, high liquidity, diversification, minimal tracking error, and large size are considered. Taxes are not considered in this calculation.
 
## Project Overview
- **Goal**: Build a predictive analytics pipeline to forecast asset returns and optimize portfolios.
- **Techniques**: CAPM, Fama-French 3-Factor, Black–Litterman, Mean–Variance Optimization.
- **Outcome**: Generate portfolios along the efficient frontier for conservative, balanced, and aggressive profiles.

## Project Abstract

The 2008 financial crisis marked a significant shift in the financial landscape, leading to the rapid rise of robo-advisors, with Betterment emerging as one of the largest players in the industry. India, as the world's most populous country and a developing nation with a growing economy, presents a unique opportunity for the adoption of robo-advisory services. With a majority of its population comprising young and middle-class individuals, robo-advisors have the potential to significantly aid investors in achieving their financial goals through optimal investment and portfolio management strategies. This dissertation focuses on analyzing Betterment's investment approach and adapting its features for the Indian financial market. The study develops an asset allocation and investment management model using Python, tailored specifically to India's market conditions. The resulting model, referred to as India-Betterment, successfully replicates Betterment's core features with necessary modifications and assumptions. By selecting appropriate ETFs and allocating assets based on each investor's risk tolerance, the India-Betterment model generates portfolios that are customized to align with the investor's risk aversion, investment goals, and time horizon.

## Methods Used
- **Return Forecasting**: CAPM, Fama–French 3-Factor
- **Market Equilibrium**: Reverse optimization (Black–Litterman prior)
- **Portfolio Optimization**: Markowitz mean–variance, Sharpe ratio maximization
- **Risk Management**: Constrained allocation to high-volatility assets

# Step-by-step Process

## 1. Data Collection & Preprocessing

- Gathered historical price data for selected asset classes (e.g., equities, bonds, and gold ETFs) from sources such as NSE website, Yahoo Finance, NSE, Groww, Value Research, Morningstar India, and MoneyControl.
- Collected risk-free rate data (Treasury yields, RBI rates).
- For factor models, collected the three-factors (Market, SMB, and HML) for the Indian market from IIMA (2019).
- Cleaned and preprocessed data by handling missing values, aligning time periods, and converting to monthly returns.

**Tools**: pandas, yfinance, numpy

## 2. Return & Risk Estimation

- Computed historical mean returns, volatilities, and covariance matrices for each asset.
- Estimated expected returns using:
  - CAPM: Estimate βs via regression against market excess returns.
  - Fama–French 3-Factor Model: Ran multi-factor regressions to estimate factor exposures
  - Black–Litterman:
      - Combined market equilibrium returns with investor views.
      - Converted factor model outputs into forward-looking expected returns.

**Tools**: statsmodels, numpy, pandas, matplotlib

## 3. Mean–Variance Optimization

- Used Markowitz’s Mean–Variance Optimizer to generate the Efficient Frontier.
- Inputs:
    - Expected returns (from models above)
    - Covariance matrix
- Outputs:
  - Portfolio weights for different risk–return tradeoffs
  - Minimum variance portfolio, maximum Sharpe ratio portfolio, and custom risk levels

**Tools** : scipy.optimize, numpy

## 4. Advanced Allocation Techniques

- Applied Black–Litterman model to blend:
  - Market equilibrium returns (reverse optimization)
  - Subjective investor views

- Introduced constraints:
  - Weight caps/floors
  - No short-selling
  - Applied tilts toward factors like value or small-cap for enhanced performance.

## 5. Visualization & Insights

- Plotted Efficient Frontier with selected optimal portfolios
- Plotted Correlation Matrix of ETFs
- Generated summary tables comparing different allocation strategies.

**Tools**: matplotlib, seaborn, plotly 

## 6. Documentation & Reporting

- Methodology (MPT, CAPM, Fama–French, Black–Litterman)
- Assumptions and constraints
- Key results and insights
- Produced Jupyter notebook with step-by-step execution.

# Results
## Investor 1, Age: 22, Investment goal: Education, Time Horizon: Less than 10 years
| 1. | No|
|---|---|
| 2. | Investing to generate education fund|
| 3. | Less than 10 years |
| 4. | Invest more to take advantage of lower prices |
| 5. | Unstable income and low savings |
| **Target Year** | 2030 |
| **Recommended asset allocation** | Stocks: 35.0%, Bonds: 50.0%, Gold: 15.0% |
| **Risk Score** | 11 |
| **Profile** | Aggressive (High risk tolerance) |

