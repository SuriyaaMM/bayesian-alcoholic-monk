# Estimator Theory & Verification using Monte Carlo Simulation
- Estimate parameters of a Distribution using Maximum Moment, Maximum Likelihood & Maximum Aposteriori Methods
- Use the Monte Carlo Simulation technique to verify the correctness & unveil mathematical properties of the distribution itself
- Use techniques like Blackwell-Rao Methods to enhance the estimator starting from a dumb estimator

# Estimators

## Maximum Likelihood Estimator (Univariate Gaussian) & Maximum Aposteriori Estimator (Univariate Gaussian)

### MLE vs MAP Estimator Performance Comparison (Univariate Gaussian)
| Metric | MLE Estimator | MAP Estimator |
|--------|---------------|---------------|
| **Mean Estimate Bias (L2 Norm)** | 0.00359 | 75.18458 |
| **Mean Estimate Variance (L2 Norm)** | 0.02976 | 10.09032 |
| **Variance Estimate Bias (L2 Norm)** | 0.03825 | - |
| **Variance Estimate Variance (L2 Norm)** | 3.03262 | - |

- Further Steps
    - Calculates Fischer Information Matrix using Numeric Hessians 
    - Calculate Cramer-Rao Lower Bound to prove that is indeed an Unbiased Estimator!