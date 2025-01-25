# EV Adoption Visualization

## Overview
This project investigates strategies to make electric vehicles (EVs) more affordable and accessible in the Netherlands, with a focus on achieving **Sustainable Development Goal 7 (SDG 7): Affordable and Clean Energy**. Using descriptive data analysis and Power BI visualizations, this research highlights key factors influencing EV adoption, such as economic benefits, government incentives, and regional disparities, while addressing the barriers that hinder low-income groups from adopting EVs.

---

## Objectives
1. **Understand Affordability**:
   - Evaluate the costs of EV ownership (e.g., purchase, maintenance, fuel savings) across income groups.
2. **Analyze Environmental Impact**:
   - Assess CO2 emission reductions resulting from increased EV adoption.
3. **Support Policy and Business Strategies**:
   - Identify actionable recommendations for businesses and policymakers to promote affordable EV adoption, particularly for low-income individuals.

---

## Research Question
**How can businesses in the Netherlands promote affordable and sustainable EV adoption among individuals within Sustainable Development Goal 7 (SDG 7)?**

---

## Key Insights

### **Findings from Exploratory Data Analysis (EDA)**:
1. **Income Diversity**:
   - Income distribution in the Netherlands shows a wide range, directly affecting EV affordability.
2. **Government Incentives**:
   - Regional disparities in government incentives significantly influence EV ownership rates.
3. **EV Ownership Patterns**:
   - Higher EV ownership rates are observed in regions with better incentives and higher average incomes.

### **Barriers to EV Adoption**:
1. **High Upfront Costs**:
   - The average EV price of €25,990 and monthly installment plans averaging €481.25 make EVs unaffordable for many low-income households.
2. **Regional Policy Disparities**:
   - Variations in tax relief and incentives create unequal opportunities for EV adoption.
3. **Awareness and Infrastructure**:
   - Limited awareness and inadequate charging infrastructure are additional barriers.

### **Economic and Environmental Benefits**:
1. **Fuel and Tax Savings**:
   - EVs provide significant savings, with average fuel costs for EVs being substantially lower than traditional vehicles.
2. **CO2 Reduction**:
   - EV adoption is strongly correlated with reduced CO2 emissions, with a correlation coefficient of -0.85.

---

## Methodology

### **Data Collection**:
- **Sources**:
  - National EV adoption statistics, CO2 emission data, government reports, and surveys on public perception.
- **Types of Data**:
  - EV prices, income levels, government policies, and adoption rates.

### **Data Cleaning & Transformation**:
- Missing values were addressed using imputation techniques.
- Skewed variables were normalized to ensure accurate statistical analysis.
- Composite metrics (e.g., affordability scores) were created to better capture relationships.

### **Visualizations**:
- **Histograms**: Income distribution across regions.
- **Box Plots**: Comparing EV prices and affordability.
- **Scatter Plots**: Correlations between incentives and adoption rates.
- **Bar Charts**: Regional tax relief and CO2 reductions.

---

## Results

### **PDF Report**
The full report summarizing the findings, visualizations, and actionable recommendations is available for download:
- [EV-Adoption-Report.pdf](./visuals/EV-Adoption-Report.pdf)

---

## Tools & Technologies
- **Power BI**: For creating data visualizations and dashboards.
- **Python**: For data cleaning and preprocessing.
- **Statistical Techniques**: Correlation analysis, descriptive statistics, and data transformation.

---

## Folder Structure

```plaintext
EV-Adoption-Visualization/
├── README.md                # Description of the project
├── datasets/                # Raw and processed data files
├── visuals/                 # Exported reports and visualizations
│   ├── EV-Adoption-Report.pdf  # Full PDF report
├── code/                    # Python scripts (if applicable)
└── docs/                    # Additional research documents (optional)

```
## Recommendations for Future Work

1. **Expand Data Sources**:
   - Incorporate more granular data on household incomes and charging infrastructure availability.

2. **Policy Design**:
   - Suggest targeted government incentives for low-income groups to close the affordability gap.

3. **Interactive Tools**:
   - Develop calculators or dashboards to help users estimate savings and evaluate EV affordability.

---

## How to Explore This Project

### Option 1: Download the Report
Access the detailed findings in the [EV-Adoption-Report.pdf](./visuals/EV-Adoption-Report.pdf).

### Option 2: Run Locally
Clone the repository to explore raw data or Python scripts (if provided):
```bash
git clone https://github.com/yourusername/EV-Adoption-Visualization.git
cd EV-Adoption-Visualization




