**Taming the Factor Zoo: A Test of New Factors** is a seminal paper in empirical asset pricing by **Guanhao Feng**, **Stefano Giglio**, and **Dacheng Xiu**, published in the *Journal of Finance* (2020). 

The paper addresses the "factor zoo" problem—the proliferation of hundreds of purported risk factors in the literature—by introducing a systematic econometric framework to evaluate whether a new factor provides incremental pricing power beyond existing ones.

## Key Research Contributions

### 1. The Model Selection Challenge
The authors highlight that most new factors are tested against a small, arbitrary set of "standard" factors (like the Fama-French 3 or 5-factor models). This ignores the hundreds of other potential factors that could render the new discovery redundant.

### 2. Two-Step Regularized Methodology
The paper proposes a novel approach combining **model selection** and **inference**:
- **Step 1 (Dimension Reduction):** They use a double-selection LASSO-based procedure to select a parsimonious set of control factors from the vast "zoo" of existing factors.
- **Step 2 (Testing):** They test whether the candidate factor carries a significant risk premium *conditional* on the selected controls.

### 3. Key Findings
- **High Redundancy:** Many factors published in recent decades do not survive the test when controlled for the full set of existing factors.
- **Factor Evolution:** The paper documents that many "new" factors are simply noisy versions or combinations of older, well-established factors.
- **The "True" Factor Set:** They identify a small subset of factors that consistently exhibit robust pricing power across different test assets and time periods.

---

## Technical Context and Modern Research

Recent research continues to build on these methods to handle the high dimensionality of financial data.

| Paper | Focus | Relevance |
| :--- | :--- | :--- |
| [Multilayer Perceptron Neural Network Models in Asset Pricing](https://alphaxiv.org/abs/2505.01921) | Neural Network Factors | Explores how deep learning can automate the discovery of factors that "tame" the zoo without manual selection. |
| [Higher-Order Asset Pricing Factors via Forward Selection](https://alphaxiv.org/abs/2503.23501) | Non-linear Factors | Shows that higher-order terms and interactions can subsume many linear factors in the zoo. |
| [FactorMiner: A Self-Evolving Agent for Financial Alpha Discovery](https://alphaxiv.org/abs/2602.14670) | LLM-based Mining | Uses LLM reasoning to search the "zoo" for interpretable signals that maintain alpha over time. |
| [The Co-Pricing Factor Zoo](https://alphaxiv.org/abs/2604.04430) | Cross-Asset Factors | Extends the "zoo" analysis to joint pricing of stocks and corporate bonds. |

### Summary of Impact
The paper effectively shifted the "burden of proof" in asset pricing. It established that it is no longer sufficient to show a factor works in a univariate sense; instead, researchers must prove a factor provides **marginal utility** relative to the entire history of discovered factors.