# Cleaned EV Adoption Data

## Overview
This dataset is part of the **EV Adoption Visualization** project, which investigates strategies to promote the affordability and accessibility of electric vehicles (EVs) in the Netherlands. The data focuses on key factors such as income distribution, EV pricing, government incentives, and environmental impact. It was meticulously collected, cleaned, and processed to ensure accuracy and usability.

## Purpose
The cleaned dataset aims to:
- Support insights into EV affordability and adoption rates.
- Provide actionable data for policymakers, researchers, and businesses.
- Highlight the environmental and economic impacts of EV adoption in alignment with **Sustainable Development Goal 7 (SDG 7)**.

---

## Why This Data Was Collected
The dataset was created to address the research question:

**"How can businesses in the Netherlands promote affordable and sustainable EV adoption among individuals within Sustainable Development Goal 7 (SDG 7)?"**

Key objectives:
1. **Understand Affordability**:
   - Explore the relationship between income levels and EV ownership.
2. **Analyze Policy Impact**:
   - Evaluate the effectiveness of government incentives in driving EV adoption.
3. **Assess Environmental Benefits**:
   - Highlight the role of EVs in reducing CO2 emissions.

---

## How the Data Was Collected

### **Sources**
1. **National Statistical Reports**:
   - Regional income levels, EV prices, and adoption rates.
2. **Government Policy Data**:
   - Tax reliefs, subsidies, and other incentive programs.
3. **Environmental Data**:
   - CO2 emissions and renewable energy contributions.
4. **Survey Data**:
   - Public sentiment on EVs, collected through Google Forms.
5. **Online APIs**:
   - Real-time data on EV prices and charging infrastructure.

### **Methods**
- **Manual Extraction**:
  - Tabular data was extracted from official reports and converted into structured formats.
- **APIs**:
  - Collected live data on EV pricing and charging stations.
- **Surveys**:
  - Designed to capture the perspectives of diverse demographic groups.
- **Cross-Validation**:
  - Data was cross-referenced with multiple sources to ensure accuracy.

---

## How the Data Was Cleaned

### **Cleaning Steps**
1. **Handling Missing Values**:
   - Missing income data was imputed using regional medians.
   - Gaps in time-series data (e.g., CO2 emissions) were filled using interpolation.
2. **Removing Duplicates**:
   - Duplicate rows were removed to avoid bias.
3. **Normalization**:
   - Skewed variables, such as EV prices, were normalized for consistent comparisons.
4. **Derived Metrics**:
   - **Affordability_Score**: Ratio of income to EV price.
   - **Policy_Impact**: Composite score of incentives and adoption rates.

---

## Dataset Details

The cleaned dataset is stored as an Excel file (`Cleaned_Data.xlsx`) with **12 sheets**, each representing a specific dataset:

| **Sheet Name**            | **Description**                                                                 |
|---------------------------|---------------------------------------------------------------------------------|
| Income Levels             | Regional income distribution in the Netherlands.                                |
| EV Prices                 | Average EV prices by region.                                                   |
| Government Incentives     | Tax reliefs, subsidies, and other incentive programs.                          |
| Adoption Rates            | EV adoption rates segmented by region.                                         |
| CO2 Reductions            | Estimated reductions in CO2 emissions due to increased EV adoption.            |
| Charging Infrastructure   | Number of charging stations and their capacity by region.                      |
| Fuel Cost Comparisons     | Average fuel costs for EVs versus traditional vehicles.                        |
| Public Perception         | Survey data on attitudes towards EV adoption.                                  |
| Policy Effectiveness      | Effectiveness scores for government policies.                                  |
| Affordability Scores      | Composite metric combining income and EV prices.                               |
| Electric Vehicle Models   | Popular EV models with details like price and range.                           |
| Economic Impact           | Economic benefits of EV adoption (e.g., job creation, GDP growth).             |

---

## File Structure

data/
├── cleaned/
│   ├── Cleaned_Data.xlsx        # Excel file with 12 sheets of cleaned data
│   ├── README.md                # Documentation of the datasets
How to Use This Data
Option 1: View Directly
Open Cleaned_Data.xlsx in any spreadsheet application to explore the data.
Option 2: Run Locally
Clone the repository:
bash
Copy
Edit
git clone https://github.com/yourusername/EV-Adoption-Visualization.git
cd EV-Adoption-Visualization/data/cleaned
Use Python, R, or Power BI to load and analyze the data.
Limitations
Missing Data:
Some gaps were filled using imputation techniques, which may introduce bias.
Survey Representation:
Survey responses may underrepresent low-income groups.
Regional Variations:
EV adoption patterns vary significantly across regions due to differing policies.
Recommendations for Future Work
Expand Data Sources:
Include more granular data on household incomes and EV charging infrastructure.
Policy Recommendations:
Suggest targeted subsidies for low-income groups to bridge the affordability gap.
Interactive Tools:
Develop dashboards or calculators to help users estimate EV affordability by region.
Contact
For inquiries or collaboration opportunities:

LinkedIn: Musaed Alfareh
Email: jimalfareh@gmail.com
Thank you for exploring this project and supporting sustainable transportation!

yaml
Copy
Edit

---

You can directly paste this into your `README.md` file for the dataset. Let me know if you'd li
