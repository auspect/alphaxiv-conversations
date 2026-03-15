<alphaxiv-thinking-title title="Searching for Bayesian Merton model adaptations" />

Yes, there are several Bayesian adaptations of the Merton model. These are particularly useful because the Merton model requires estimating "latent" (unobserved) variables like the market value of a firm's assets and its true volatility, which cannot be seen directly in accounting data.

Bayesian methods allow researchers to treat these unobserved values as random variables and use Markov Chain Monte Carlo (MCMC) or other sampling techniques to estimate them more robustly than traditional maximum likelihood methods.

### 1. Bayesian Estimation of Latent Asset Values
Since firm assets aren't traded like stocks, their "market value" is hidden. Bayesian adaptations use observed stock prices and debt levels to back-calculate the posterior distribution of the firm's assets.

- **MCMC for Default and Recovery**: Recent work has used MCMC to jointly estimate default probabilities and recovery rates. By treating the "systemic factor" (the state of the economy) as a latent variable, researchers can model how default and recovery become correlated during downturns.
- **Particle MCMC and Expert Opinion**: A 2023 study introduced **Particle MCMC** to forecast default models. This approach is unique because it allows for the integration of "expert opinion" as a Bayesian prior, helping the model perform better when historical data is thin or unrepresentative.

### 2. Bayesian Structural and State-Space Models
These models treat the firm's financial health as a "state" that evolves over time.

- **Bayesian State-Space Models**: These are used to assess default risk at an aggregate level (like a mortgage portfolio). They allow for parameters to evolve stochastically, capturing how the risk profile of a bank's customers changes over time.
- **Stan for Credit Portfolios**: Modern probabilistic programming languages like **Stan** are being used to estimate default correlations in portfolios through a Bayesian framework. This helps banks comply with Basel III requirements by providing more reliable estimates of "tail risk."

### 3. Bayesian Neural Networks for Credit Default
As machine learning enters the field, Bayesian principles are being applied to neural networks to make them more interpretable for risk managers.

- **Automatic Relevance Determination (ARD)**: Some researchers use Bayesian Neural Networks with ARD to model credit card defaults. This provides a "confidence interval" for every prediction, which a standard black-box AI model cannot do, making it much more acceptable for banking regulators.

---

### Key Papers on Bayesian Merton Adaptations

| Paper | Focus |
| :--- | :--- |
| [Bayesian Estimation of Corporate Default Spreads](https://arxiv.org/abs/2503.02991) | Uses Bayesian inference to estimate bankruptcy likelihood and credit risk for portfolio exclusion. |
| [Particle MCMC in forecasting frailty correlated default models](https://arxiv.org/abs/2304.11586) | Combines Particle MCMC with expert opinion to forecast corporate defaults. |
| [Estimating Default Probability and Correlation using Stan](https://arxiv.org/abs/2401.11346) | Implements a Bayesian framework in Stan to estimate portfolio default rates and correlations. |
| [Predicting Credit Default Probabilities Using Bayesian Statistics](https://arxiv.org/abs/2108.03389) | Applies Bayesian Monte Carlo simulations to manage large bank portfolios of risky customers. |
| [Dependent default and recovery: MCMC study](https://arxiv.org/abs/1112.05766) | A classic MCMC application for estimating capital against credit risk during economic downturns. |
