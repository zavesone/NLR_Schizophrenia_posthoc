# Post-hoc Analysis of Variation in Neutrophil-to-Lymphocyte Ratio Across Schizophrenia Subtypes
![mygif](https://s12.gifyu.com/images/SDs0v.gif)

This repository contains additional statistical analyses examining variability patterns in Neutrophil-to-Lymphocyte Ratio (NLR) across different schizophrenia subtypes, extending the findings from our original study [doi: 10.52567/2712-9179-2024-4-3-12-23].

## Project Overview
This post-hoc analysis investigates the heterogeneity in NLR measurements across schizophrenia subtypes using variation coefficient ratios and standardized mean differences. The analysis aims to provide deeper insights into the patterns of inflammatory marker variability in different manifestations of schizophrenia.

## Repository Structure
```python
repository/
├── analysis/
│   ├── lnVCR_analysis.py        # Variation coefficient ratio calculations
│   ├── mean_difference.py       # Standardized mean difference analysis  
│   └── sensitivity.py           # Leave-one-out sensitivity analysis
├── data/
│   └── original_values.py       # Input data and parameters
├── visualizations/
│   └── figures/                 # Generated plots and visualizations
└── results/
    └── analysis_outputs.csv     # Computed metrics and statistics



```markdown
# Post-hoc Analysis of Variation in Neutrophil-to-Lymphocyte Ratio Across Schizophrenia Subtypes
![mygif](https://s12.gifyu.com/images/SDs0v.gif)

This repository contains additional statistical analyses examining variability patterns in Neutrophil-to-Lymphocyte Ratio (NLR) across different schizophrenia subtypes, extending the findings from our original study [doi: 10.52567/2712-9179-2024-4-3-12-23].

## Project Overview
This post-hoc analysis investigates the heterogeneity in NLR measurements across schizophrenia subtypes using variation coefficient ratios and standardized mean differences. The analysis aims to provide deeper insights into the patterns of inflammatory marker variability in different manifestations of schizophrenia.

## Repository Structure
```python
repository/
├── analysis/
│   ├── lnVCR_analysis.py        # Variation coefficient ratio calculations
│   ├── mean_difference.py       # Standardized mean difference analysis  
│   └── sensitivity.py           # Leave-one-out sensitivity analysis
├── data/
│   └── original_values.py       # Input data and parameters
├── visualizations/
│   └── figures/                 # Generated plots and visualizations
└── results/
    └── analysis_outputs.csv     # Computed metrics and statistics
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

## Installation & Usage
```bash
# Clone repository
git clone https://github.com/yourusername/nlr-variation-analysis

# Install requirements
pip install -r requirements.txt

# Run analyses
python analysis/lnVCR_analysis.py
python analysis/mean_difference.py
python analysis/sensitivity.py
```

## Key Findings
- Identified significant heterogeneity in NLR variability across subgroups
- Found distinct patterns of variation in different schizophrenia manifestations
- Confirmed robustness of results through sensitivity analyses
- Demonstrated utility of lnVCR for measuring biological variability

## Limitations
- Based on aggregated data
- Cannot account for individual variations
- Limited to available subgroup classifications

## Future Directions
- Extension to other inflammatory markers
- Integration with clinical outcomes
- Development of more sophisticated variability metrics

## Contributors
N.V. Zakharova
R.F. Nasyrova
M.N. Rumyantseva
A.I. Rakhmatullin
K.I. Sizykh
F.N. Kostin

## Contact
For queries regarding this post-hoc analysis:
- Open an issue in this repository
- Email: fedor3016@gmail.com

## Commitment to Open Science
![mygif](https://s12.gifyu.com/images/SDxHt.gif)

*"Understanding variability in biological markers is crucial for advancing personalized medicine approaches in psychiatry."*

---
**Note**: This analysis is part of ongoing research into inflammatory markers in schizophrenia. For the original analysis, see the [original repository](link-to-original-repo).
```

Now the entire README is in proper markdown format that you can directly paste into a README.md file. All sections are consistently formatted with appropriate headings, code blocks, and list formatting.
