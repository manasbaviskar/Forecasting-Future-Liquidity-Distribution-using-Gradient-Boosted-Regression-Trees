# Forecasting-Future-Liquidity-Distribution-using-Gradient-Boosted-Regression-Trees
This project focuses on building predictive models to forecast future liquidity distribution in corporate bond markets. Using rolling-window frameworks, the study developed bond-level and trade-specific predictors to estimate future liquidity trends.

## Overview
This repository provides an implementation of machine learning methods to predict future liquidity in the corporate bond market. The research focuses on a comparative analysis of state-of-the-art machine learning techniques, including tree-based models like Random Forest and LightGBM, as well as traditional linear models such as Elastic Net and Partial Least Squares (PLS). The primary goal is to identify predictors of liquidity (log average traded volume that will be traded on that day) and quantify the performance of different models in a rigorous, data-driven framework.

## Methodology
1. **Liquidity Measure Construction**:
   - A composite liquidity measure is constructed using the first principal component of 11 bond liquidity metrics.

2. **Prediction Model Framework**:
   - Future bond liquidity is modeled as an additive prediction error problem:
     \[ l_{i,t+1} = g(z_{i,t}) + \varepsilon_{i,t+1} \]
     where \(g(z_{i,t})\) is a flexible function of bond characteristics \(z_{i,t}\), estimated via machine learning models.

3. **Machine Learning Models**:
   - **Linear Models**: Ordinary Least Squares (OLS), Elastic Net, Partial Least Squares (PLS).
   - **Tree-Based Models**: Random Forest, LightGBM.

4. **Rolling Window Approach**:
   - The models are trained, validated, and tested in a rolling-window setup using data from 2005 Q1 to 2019 Q4.

5. **Performance Metrics**:
   - Out-of-sample \(R^2\)
   - Root Mean Square Error (RMSE)
   - Diebold-Mariano Test (DM Test) for model comparison
     
## References
The following papers provided foundational insights and methodologies for this research:

1. Müller, Marcel and Reichenbacher, Michael and Schuster, Philipp and Uhrig‐Homburg, Marliese, Expected Bond Liquidity * (December 13, 2024). Available at SSRN: https://ssrn.com/abstract=3642604 or http://dx.doi.org/10.2139/ssrn.36426042.
2. Yu, Haiyue, Liquidity Prediction in the Corporate Bond Market (April 21, 2022). Available at SSRN: https://ssrn.com/abstract=4354377 or http://dx.doi.org/10.2139/ssrn.4354377
3. Gu, S., Kelly, B., & Xiu, D. (2020). "Empirical Asset Pricing via Machine Learning." *The Review of Financial Studies*, 33(5), 2223-2273. [Link](https://academic.oup.com/rfs/article/33/5/2223/5717620)
7. Bali, T. G., Goyal, A., Huang, D., Jiang, Y., & Wen, Q. (2020). "Predicting Bond Returns: Machine Learning Models vs. Traditional Approaches." *Working Paper*. [SSRN Link](https://ssrn.com/abstract=3597059)


