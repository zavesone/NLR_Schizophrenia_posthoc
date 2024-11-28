# Post-hoc Analysis of Variation in Neutrophil-to-Lymphocyte Ratio Across Schizophrenia Subtypes
![mygif](https://s12.gifyu.com/images/SDs0v.gif)

This repository contains additional statistical analyses examining variability patterns in Neutrophil-to-Lymphocyte Ratio (NLR) across different schizophrenia subtypes, extending the findings from our original study [doi: 10.52567/2712-9179-2024-4-3-12-23].

## Project Overview
This post-hoc analysis investigates the heterogeneity in NLR measurements across schizophrenia subtypes using variation coefficient ratios and standardized mean differences. The analysis aims to provide deeper insights into the patterns of inflammatory marker variability in different manifestations of schizophrenia.

## Repository Structure
```python
repository/
└── posthoc_nlr.ipynb    # Jupyter notebook containing all analyses
```

## Data Structure
```python
# Input data format
groups = ['Schizophrenia Unspecified', 'First Episode Schizophrenia',
          'Schizophrenia in Remission', 'Schizophrenia without Remission']
means = [2.27, 1.94, 2.03, 2.43]
sds = [1.43, 1.09, 1.17, 1.23]
ns = [9148, 648, 3019, 1256]
control_mean = 1.62
control_sd = 0.78
control_n = 1150
```

## Methods
1. **Variation Coefficient Ratio (lnVCR) Analysis**
   - Calculation of coefficient variation ratios
   - Computation of confidence intervals
   - Forest plot visualization
   - AIC/BIC model comparison

2. **Mean Difference Analysis**
   - Standardized mean differences calculation
   - Confidence interval estimation
   - Statistical significance testing

3. **Sensitivity Analysis**
   - Leave-one-out approach
   - Impact assessment of individual groups
   - Robustness evaluation

## Requirements
```python
requirements = [
    'python>=3.8',
    'numpy',
    'pandas',
    'matplotlib',
    'scipy',
    'statsmodels'
]
```


# Analysis Results

## lnVCR Analysis
We performed a logarithm of Variation Coefficient Ratio (lnVCR) analysis across different schizophrenia subtypes:
- Schizophrenia Unspecified showed the highest variability (lnVCR = 0.2688, p < 0.001)
- First Episode Schizophrenia (lnVCR = 0.1544, p < 0.001)
- Schizophrenia in Remission (lnVCR = 0.1799, p < 0.001)
- Schizophrenia without Remission showed the lowest effect (lnVCR = 0.05, p = 0.0832)

## Model Comparison
The AIC/BIC analysis strongly favored the observed model over the null model:
- Observed model showed better fit (AIC = 42.64, BIC = 41.42)
- Null model performed worse (AIC = 226.86, BIC = 225.44)
- LogLik values further supported this conclusion
- Chi-square test confirmed significant difference (p < 0.001)

## Mean Differences Analysis
Forest plot analysis revealed significant mean differences from control:
- All groups showed positive mean differences
- Strongest effect in Schizophrenia Unspecified
- Significant effects across all subtypes except Schizophrenia without Remission
- 95% confidence intervals suggest reliable effects

## Sensitivity Analysis
Leave-one-out analysis revealed:
- Excluding Schizophrenia without Remission had the largest impact on lnVCR (+0.0377)
- Mean differences remained robust to group exclusion
- First Episode Schizophrenia showed consistent effects across analyses
- Results suggest stability of findings with minor variations based on group inclusion

These findings suggest heterogeneous variability patterns across schizophrenia subtypes, with particularly strong effects in unspecified cases and more stable patterns in first-episode cases.

## Key Findings
- Identified significant heterogeneity in NLR variability across subgroups
- Found distinct patterns of variation in different schizophrenia manifestations
- Confirmed robustness of results through sensitivity analyses
- Demonstrated utility of lnVCR for measuring biological variability

## Limitations
- Based on aggregated data
- Cannot account for individual variations
- Limited to available subgroup classifications

## Contact
For queries regarding this post-hoc analysis:
- Open an issue in this repository
- Email: fedor3016@gmail.com

## Author
Fedor Kostin

![mygif](https://s12.gifyu.com/images/SDxHt.gif)

*"Understanding variability in biological markers is crucial for advancing personalized medicine approaches in psychiatry."*

