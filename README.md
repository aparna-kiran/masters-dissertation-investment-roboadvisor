# Masters Dissertation
## Investment Roboadvisor
### Predicting forward-looking returns of ETFs tailored to Indian Market

## 📊 Project Overview
- **Goal**: Build a predictive analytics pipeline to forecast asset returns and optimize portfolios.
- **Techniques**: CAPM, Fama-French 3-Factor, Black–Litterman, Mean–Variance Optimization.
- **Outcome**: Generate portfolios along the efficient frontier for conservative, balanced, and aggressive profiles.

## Project Description

The 2008 financial crisis marked a significant shift in the financial landscape, leading to the rapid rise of robo-advisors, with Betterment emerging as one of the largest players in the industry. India, as the world's most populous country and a developing nation with a growing economy, presents a unique opportunity for the adoption of robo-advisory services. With a majority of its population comprising young and middle-class individuals, robo-advisors have the potential to significantly aid investors in achieving their financial goals through optimal investment and portfolio management strategies. This dissertation focuses on analyzing Betterment's investment approach and adapting its features for the Indian financial market. The study develops an asset allocation and investment management model using Python, tailored specifically to India's market conditions. The resulting model, referred to as India-Betterment, successfully replicates Betterment's core features with necessary modifications and assumptions. By selecting appropriate ETFs and allocating assets based on each investor's risk tolerance, the India-Betterment model generates portfolios that are customized to align with the investor's risk aversion, investment goals, and time horizon.

## 🧠 Methods Used
- **Return Forecasting**: CAPM, Fama–French 3-Factor
- **Market Equilibrium**: Reverse optimization (Black–Litterman prior)
- **Portfolio Optimization**: Markowitz mean–variance, Sharpe ratio maximization
- **Risk Management**: Constrained allocation to high-volatility assets
