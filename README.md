# A/B Testing & Statistical Hypothesis Testing From Scratch

This repository features a pure computational implementation of inferential statistics used to evaluate product experiments. Instead of treating statistical tests as black-box functions, this project simulates user conversion data, calculates test statistics from first principles, and evaluates business metrics using rigorous mathematical frameworks.

🔗 **Live Notebook:** [View my original work on Kaggle](https://www.kaggle.com/code/harrisawan/linear-regression-from-scratch) *(Note: Swap this with your actual A/B testing Kaggle link!)*

## 🔬 Experimental Framework & Methodology
The simulation models a standard digital product experiment where users are randomly assigned to a baseline control group or a modified variant group to evaluate an optimization hypothesis:
* **Null Hypothesis ($H_0$):** $p_{variant} - p_{control} = 0$ (The change has no effect on user conversion rates).
* **Alternative Hypothesis ($H_1$):** $p_{variant} - p_{control} \neq 0$ (The change significantly alters user conversion behavior).

### Mathematical Mechanics
To test the hypothesis without relying entirely on abstract high-level wrappers, the pipeline calculates a two-proportion Z-test to evaluate the difference between sample conversion scales:

$$Z = \frac{\hat{p}_1 - \hat{p}_2}{\sqrt{\hat{p}(1-\hat{p})\left(\frac{1}{n_1} + \frac{1}{n_2}\right)}}$$

Where $\hat{p}$ represents the pooled conversion rate, $\hat{p}_1$ and $\hat{p}_2$ represent sample proportions, and $n_1, n_2$ represent group sample sizes.

## 📊 Core Findings & Interpretation
* **Statistical Significance:** Evaluated at a strict significance threshold ($\alpha = 0.05$). 
* **P-Value Derivation:** The calculated p-value represents the exact probability of observing our experimental results entirely by chance under the assumption that the null hypothesis is true.
* **Business Decision:** If $p < \alpha$, we reject the null hypothesis, mathematically justifying a production rollout of the variant layout to maximize conversions.

## 🛠️ Tech Stack & Skills Demonstrated
* **Languages:** Python
* **Libraries:** NumPy & SciPy (Vectorized tracking and probability distributions), Pandas (Dataframe restructuring)
* **Core Competencies:** Hypothesis testing, Z-scores, Type I/II error management, confidence interval derivation, and product experiment design.
