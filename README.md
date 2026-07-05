# Portfolio Project 2 - A/B Testing Statistical Analysis

## Project Goal

The goal of this project is to analyze A/B testing results using statistical methods in Python and create visualizations demonstrating key conversion metrics.

This project extends the previous A/B Testing dashboard by adding statistical significance calculations and validating whether observed metric changes between control and test groups are meaningful.

---

## Project Tasks

### Stage 1 - Statistical Significance Calculation in Python

The first stage focuses on replacing manual significance calculations from online calculators with an automated Python-based solution.

Using experiment data from the previous **Create Your A/B Testing Tool** project, statistical significance was calculated for four key conversion metrics:

- add_payment_info / session
- add_shipping_info / session
- begin_checkout / session
- new_accounts / session

Metric formula:

```text
conversion_rate = event_count / session_count
```

The final dataset includes all required fields for further visualization and analysis.

---

### Dynamic Metric Processing

To make the solution scalable, statistical calculations were implemented using arrays and loops instead of hardcoded calculations for each metric.

This approach allows the script to support additional conversion metrics without changing the core calculation logic.

---

## Statistical Method

Statistical significance was evaluated using a **two-proportion Z-test**.

### Null Hypothesis (H₀)

There is no statistically significant difference between control and test groups.

### Alternative Hypothesis (H₁)

There is a statistically significant difference between control and test groups.

### Decision Rule

- p-value < 0.05 → Significant
- p-value ≥ 0.05 → Not Significant

Python calculations include:

- conversion rate
- metric uplift (%)
- z-statistic
- p-value
- significance flag

---

## Stage 2 — Visualization in Tableau

The second stage focuses on visualizing both experiment results and statistical significance.

The Tableau dashboard demonstrates:

### Experiment Overview
- experiment group distribution
- traffic channel analysis
- device analysis
- geographic distribution
- conversion metrics

### Statistical Significance Analysis
- conversion rate comparison
- metric change (%)
- p-values
- z-statistics
- significance status

Interactive filters allow analysis by test number.

---

## Dataset

The dataset contains experiment-level aggregated data with the following dimensions:

- date
- country
- device
- continent
- channel
- test
- test_group
- event_name
- value

Data source: **Google BigQuery**

---

## Tech Stack

### SQL
Used for:
- data extraction
- metric aggregation
- dataset preparation

### Python
Used for:
- statistical significance calculation
- hypothesis testing
- metric comparison

Libraries:
- Pandas
- NumPy
- SciPy

### Tableau
Used for:
- dashboard creation
- metric visualization
- interactive analysis

---

## Project Deliverables

- SQL data extraction script
- Python notebook with statistical analysis
- Tableau dashboard with visual insights
