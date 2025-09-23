# EV Adoption Visualization

<p align="center">
  <img src="./SDG.png" alt="Sustainable Development Goals" width="300"/>
</p>

## Overview
This project examines strategies to make electric vehicles (EVs) more affordable and accessible in the Netherlands, with a focus on achieving Sustainable Development Goal 7 (SDG 7): Affordable and Clean Energy. Using descriptive data analysis and Power BI visualizations, this research highlights key factors influencing EV adoption, such as economic benefits, government incentives, and regional disparities, while addressing the barriers that hinder low-income groups from adopting EVs.

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
- [EV-Adoption-Report.pdf](./EV-Adoption-Report.pdf)

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
## Recommendations
### Raise Awareness
Public Campaigns:
Conduct campaigns to educate citizens on the long-term economic benefits of EV ownership, such as reduced fuel expenses and lower maintenance costs.
Highlight environmental advantages, including CO2 reductions and improved air quality, using relatable success stories and data-driven insights.
### Ease the Purchase Process
Flexible Financing Options:
Offer low-interest loans, installment plans, and EV leasing programs tailored to low-income households to lower upfront costs.
User-Friendly Tools:
Develop interactive calculators or online tools to help potential buyers estimate:
Savings in fuel and maintenance costs.
Eligibility for government incentives and subsidies.
### Targeted Incentive Programs
Income-Based Subsidies:
Design tiered subsidies that provide maximum financial support to low-income households.
Regional Tax Reliefs:
Address disparities in EV adoption by implementing targeted tax relief programs in regions with lower adoption rates.
### Infrastructure Development
Expand Charging Networks:
Build more public charging stations in underserved areas to improve accessibility and reduce range anxiety.
Collaborate with Businesses:
Partner with local businesses and organizations to establish affordable and accessible charging infrastructure in key locations.
### Interactive Tools
Dashboards and Apps:
Create user-friendly dashboards or mobile applications to visualize how EVs can benefit users economically and environmentally.
Cost-Saving Simulators:
Provide tools that allow users to compare their current vehicle costs with potential savings from switching to EVs.
## Recommendations for Future Work
### Expand Data Sources
Collect more detailed data on household incomes and the availability of EV charging infrastructure to improve the accuracy of affordability analyses.
### Policy Design
Develop new, targeted government incentives aimed at bridging the affordability gap for low-income households, with a focus on addressing regional disparities.
### Interactive Tools
Design more advanced calculators and dashboards to provide personalized insights into EV affordability and long-term benefits for individual users.

---

## How to Explore This Project

### Option 1: Download the Report
Access the detailed findings in the [EV-Adoption-Report.pdf](./EV-Adoption-Report.pdf).
### Option 2: Run Locally
Clone the repository to explore raw data or Python scripts (if provided):
```bash
git clone https://github.com/yourusername/EV-Adoption-Visualization.git
cd EV-Adoption-Visualization






