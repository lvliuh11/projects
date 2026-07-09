# P&C Actuarial Analytics Projects

This repository contains property and casualty actuarial analytics projects built in Python. The work focuses on loss reserving, personal auto pricing, model validation, and actuarial interpretation.

## Projects

### 1. P&C Loss Reserving

Notebook: `projects/loss_reserving/p_and_c_loss_reserving.ipynb`

This project demonstrates a loss reserving workflow using Chain Ladder and Bornhuetter-Ferguson methods. It includes a simulated cumulative paid loss triangle, selected loss development factors, reserve estimates by accident year, diagnostic charts, and a comparison against the `chainladder` package using the RAA sample triangle.

Key topics:

- Cumulative paid loss triangles
- Age-to-age loss development factors
- CDFs to ultimate
- Chain Ladder reserve estimates
- Bornhuetter-Ferguson reserve estimates
- IBNR comparison and actuarial memo writing

Selected outputs:

- `outputs/loss_reserving/reserve_summary.csv`
- `outputs/loss_reserving/reserve_by_year.png`
- `outputs/loss_reserving/ldf_pattern.png`
- `outputs/loss_reserving/method_comparison.png`
- `outputs/loss_reserving/raa_manual_vs_package_ibnr.png`

### 2. Auto Insurance Pure Premium Modeling

Notebook: `projects/auto_pricing/auto_insurance_pricing_case_study.ipynb`

This project simulates a personal auto insurance pricing workflow from raw policy and claim data to pure premium modeling, model validation, rating relativities, and actuarial interpretation. It combines traditional actuarial GLMs with machine learning challenger models.

Key topics:

- Frequency and severity modeling
- Poisson GLM with exposure offset
- Gamma GLM severity modeling
- Pure premium construction
- Gradient boosting challenger models
- Lift charts and actual-to-expected validation
- Rating relativities and bootstrap variability
- Model governance and actuarial limitations

Selected outputs:

- `outputs/auto_pricing_case_study/model_comparison.csv`
- `outputs/auto_pricing_case_study/frequency_glm_metrics.csv`
- `outputs/auto_pricing_case_study/severity_glm_metrics.csv`
- `outputs/auto_pricing_case_study/glm_actual_vs_expected_lift.png`
- `outputs/auto_pricing_case_study/gbm_actual_vs_expected_lift.png`
- `outputs/auto_pricing_case_study/actuarial_interpretation.txt`

### 3. Auto Pricing Practice Notebook

Notebook: `projects/auto_pricing/01_auto_pricing_model_framework_practice.ipynb`

This notebook is a practice version of the auto pricing case study. It keeps the structure of the completed project but leaves implementation steps as TODOs for hands-on learning.

## Repository Structure

```text
data/
  auto_pricing/
    fremtpl/
outputs/
  auto_pricing_case_study/
  loss_reserving/
projects/
  auto_pricing/
  loss_reserving/
resumes/
```

## Data

The auto pricing project uses the public French motor third-party liability datasets:

- OpenML `freMTPL2freq`
- OpenML `freMTPL2sev`
- CASdatasets package family

The loss reserving project uses a simulated triangle for the main reserving example and the built-in RAA sample triangle from the Python `chainladder` package for validation.

## Environment

The notebooks were developed with Python 3.x.

Core packages:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn statsmodels scipy chainladder
```

## How to Run

1. Clone this repository.
2. Install the required Python packages.
3. Open the notebooks in Jupyter Notebook, JupyterLab, or VS Code.
4. Run notebooks from the repository root so the relative `data/` and `outputs/` paths resolve correctly.

## Purpose

These projects are intended to demonstrate actuarial modeling skills, Python analytics workflow, reproducible project organization, and the ability to communicate technical results in a business-oriented actuarial format.
