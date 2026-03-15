# Chat Transcript: Recent Merton model improvements

## User

Are there any recent papers improving the Merton model that financial or credit risk people use in banking?

## Aurelle

<alphaxiv-thinking-title title="Searching for recent Merton model improvements" />

> **Tool Call: Embedding Similarity Search**\
> **Tool Call: Full Text Papers Search**\
> **Tool Call: Agentic Paper Retrieval**

Recent research on the Merton model has moved beyond the original "structural" assumptions (which often fail in real-world markets due to unobserved liabilities and constant volatility) toward hybrid frameworks that integrate **machine learning**, **climate risk**, and **non-stationary correlations**. 

While the Merton model remains a cornerstone of credit risk in banking, modern improvements focus on making the model "dynamic" and "data-driven" rather than purely mathematical.

## Key Recent Improvements to the Merton Model

### 1. Integrating Machine Learning and Non-Financial Data
Modern banking practice is shifting from purely structural models to hybrid frameworks that use machine learning to capture irregularities that the Merton model's diffusion process misses. Recent work has integrated large sets of non-financial indicators (like corporate disclosure text) to improve default prediction accuracy.

- **Multimodal and AI Integration**: Researchers are now using models like BERT to analyze corporate disclosures alongside financial ratios to predict bankruptcies, filling the gap where market prices alone (the core of Merton) fail to signal distress.
- **Hybrid Neural Frameworks**: New approaches combine Convolutional Neural Networks (CNNs) and Transformers to capture complex patterns in tabular financial data that traditional Merton-based KMV models often ignore.

### 2. Structural Extensions for Real-World Constraints
The classic Merton assumption—that liabilities are a single zero-coupon bond—is being replaced with more realistic structural definitions.

- **Observed Liabilities**: A 2024 paper developed a version of the Merton model specifically for public companies where liabilities are explicitly observed and modeled using Campbell-Shiller approximations.
- **Climate-Extended Risk Model (CERM)**: The Merton framework has been adapted to include "climate risk" by adjusting the firm's asset value and volatility to account for physical and transition risks associated with climate change.

### 3. Volatility and Correlation Refinements
The original Merton model assumes constant asset volatility, which is rarely true during financial stress.

- **CEV-KMV and qGaussian Models**: Recent extensions apply the **Constant Elasticity of Variance (CEV)** process or **qGaussian** distributions to account for "slow fluctuations" in volatility and fat-tailed distributions of asset values.
- **Random Matrix Theory**: To handle non-stationary correlations between firms (systemic risk), researchers have used Random Matrix Theory to refine how the Merton model estimates joint default probabilities in large portfolios.

---

## Relevant Recent Papers (2023–2026)

| Paper | Key Contribution |
| :--- | :--- |
| [The Merton's Default Risk Model for Public Company](https://arxiv.org/abs/2406.18121) | Develops a structural model assuming observed liabilities and uses Campbell-Shiller approximations. |
| [Predicting Credit Spreads and Ratings with Machine Learning](https://arxiv.org/abs/2509.19042) | Integrates 167 indicators including macro and non-financial data into credit risk modeling. |
| [The Climate Extended Risk Model (CERM)](https://arxiv.org/abs/2103.03275) | Adapts structural models to incorporate embedded climate risk within bank portfolios. |
| [Why Bonds Fail Differently?](https://arxiv.org/abs/2509.10802) | Uses explainable multimodal learning for multi-class default prediction in volatile markets. |
| [The financial health of a company and the risk of its default](https://arxiv.org/abs/2302.10140) | Re-theorizes default risk based on the cost of equilibrium in financial systems. |
| [Corporate Bankruptcy Prediction with Domain-Adapted BERT](https://arxiv.org/abs/2312.03194) | Uses LLMs to analyze corporate disclosures for superior bankruptcy prediction over structural models. |

## User

And are there any Bayesian adaptations of the Merton model?

## Aurelle

<alphaxiv-thinking-title title="Searching for Bayesian Merton model adaptations" />

> **Tool Call: Embedding Similarity Search**\
> **Tool Call: Full Text Papers Search**\
> **Tool Call: Agentic Paper Retrieval**

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
