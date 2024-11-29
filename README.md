
```

```
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

## Analysis Results

### lnVCR Analysis Results
![Figure 1](https://github.com/zavesone/NLR_Schizophrenia_posthoc/blob/main/plots/lnVCR%20plot.png)
*Forest plot of lnVCR analysis with tabulated results*

Analysis of coefficient variation ratios showed:
- Unspecified: CV=0.63, lnVCR=0.2688 (CI: 0.2254-0.3122)
- First Episode: CV=0.5619, lnVCR=0.1544 (CI: 0.0863-0.2225)
- In Remission: CV=0.5764, lnVCR=0.1799 (CI: 0.1318-0.2279)
- Without Remission: CV=0.5062, lnVCR=0.05 (CI: -0.0066-0.1066)

All groups except "Without Remission" showed significantly higher variability compared to controls (p<0.001).

### Mean Differences Across Groups
![Figure 2]()
*Forest plot of mean differences from control group*

Model comparison results:
- Observed model: AIC=98.86, BIC=97.63
- Null model: AIC=1156.31, BIC=1155.70
- Statistical significance: p<0.0001

### Heterogeneity Assessment
![Figure 3](https://github.com/zavesone/NLR_Schizophrenia_posthoc/blob/main/plots/bubble_plot.png)
*Effect size vs standard error relationship with sample size representation*

![Figure 4](https://github.com/zavesone/NLR_Schizophrenia_posthoc/blob/main/plots/Heterogeneity%20Statistics.png)
*Effect size comparison showing heterogeneity between subgroups*

Heterogeneity statistics revealed substantial differences between subgroups:
- Q statistic: 36.92 (df=3)
- P-value: <0.0001
- I² value: 91.9%

### Sensitivity Analysis
![Figure 5](https://github.com/zavesone/NLR_Schizophrenia_posthoc/blob/main/plots/sensitivity_analyses.png)
*Impact of excluding individual groups on lnVCR and mean differences*

Leave-one-out analysis showed:
- Most influential group: Schizophrenia without Remission (lnVCR change: +0.0377)
- Most stable: First Episode Schizophrenia (lnVCR change: +0.0030)
- Mean difference changes ranged from -0.0875 to +0.0758

## Key Findings
- Significant heterogeneity across subgroups (I²=91.9%)
- Highest variability in Unspecified group
- Most homogeneous patterns in Without Remission group
- Results robust to group exclusion
- Strong evidence against homogeneity (Q=36.92, p<0.0001)

## Limitations
- Based on aggregated data
- Cannot account for individual variations
- Limited to available subgroup classifications

## Author
Fedor Kostin

## Contact
For queries regarding this post-hoc analysis:
- Open an issue in this repository
- Email: fedor3016@gmail.com

![mygif](https://s12.gifyu.com/images/SDxHt.gif)









