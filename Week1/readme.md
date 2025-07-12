# Semiconductor Chip Dataset Analysis (CHIP Dataset)

## Project Overview

This project explores design and performance trends in CPUs and GPUs using the CHIP dataset, with a focus on validating claims such as:

- **Moore’s Law**: Transistor count doubles every ~2 years
- **Dennard Scaling**: Smaller transistors lead to stable power usage
- **GPU Performance Growth**: Doubling every ~1.5 years
- **Technology Adoption**: High-end GPUs adopt newer technologies first
- **Foundry Dominance**: TSMC as the leading chip manufacturer

---

## Data Cleaning Steps

- Converted date fields using `pd.to_datetime()`
- Identified missing values across numeric and categorical features
- Imputed:
  - **Numeric columns** using `SimpleImputer(strategy='median')`
  - **Categorical column (`Foundry`)** using `SimpleImputer(strategy='most_frequent')`
- Dropped rows with unparseable release dates
- Converted data types for modeling

---

## Exploratory Data Analysis (EDA)

### Moore’s Law
- Analyzed average GPU transistor count over time
- Used log scale to visualize exponential trend

### Dennard Scaling
- Scatterplot of `Process Size (nm)` vs `TDP (W)`
- Checked if power usage decreases with smaller node sizes

### CPU vs GPU Frequencies
- Compared frequency trends for CPUs and GPUs over time

### GPU Performance Doubling
- FP32 GFLOPS plotted to confirm 1.5-year doubling trend (log scale)

### Factors Driving Performance
- Correlation analysis between:
  - `FP32 GFLOPS` vs `Freq`, `Transistors`, `Die Size`, `Process Size`

### Tech Adoption by Performance Tier
- Created low/mid/high GPU performance tiers
- Analyzed average process size per tier over time

### Vendor Analysis
- Compared process sizes between Intel, AMD, Nvidia, ATI, and others using boxplots

### Foundry Analysis
- Counted total chips produced by each foundry
- Confirmed TSMC as the leading manufacturer

---

## Data Preparation for Modeling

- Label-encoded and one-hot encoded key categorical variables
- Created a cleaned dataset ready for ML or statistical analysis

---

## Tools & Libraries

- **Pandas**: Data manipulation
- **Seaborn & Matplotlib**: Data visualization
- **Scikit-learn**: Imputation, preprocessing
- **Jupyter Notebook**: Code development and documentation


