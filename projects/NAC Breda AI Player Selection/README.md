# NAC Breda Player Selection – The ML Edge

**Identifying Top Talents Through Data-Driven Decisions**

---

## 📌 Overview

Football scouting is changing, and NAC Breda is at the forefront of that transformation. This project leverages data science and machine learning to support NAC Breda in identifying the most promising attacking players. By combining statistical rigor with football intelligence, we create a streamlined, efficient, and objective approach to player selection that aligns with the club’s goals and budget.

---

## 📊 Dataset Overview

- **Size:** 16,535 player records
- **Features:** 114 (numerical + categorical)
- **Focus:** Player attributes, performance metrics, and potential contribution to NAC Breda
- **Source:** Aggregated from reputable football databases, APIs, and public records

---

## 🔧 Tools & Technologies

- **Language:** Python
- **Libraries:** pandas, NumPy, Matplotlib, Seaborn, scikit-learn
- **Model Used:** Logistic Regression
- **Environment:** Jupyter Notebook

---

## 🧪 Project Pipeline

### 1. Exploratory Data Analysis (EDA)
- Cleaned, visualized, and analyzed key features
- Studied player market values, age distribution, and position versatility
- Assessed missing values, outliers, and anomalies

### 2. Data Preprocessing
- One-hot encoded categorical features
- Normalized numerical variables
- Removed duplicates and corrected inconsistencies

### 3. Model Development
- Selected **Logistic Regression** for its speed, interpretability, and effectiveness with binary classification
- Trained to identify high-potential attackers based on selected performance metrics

### 4. Model Evaluation
- Evaluated using accuracy, confusion matrix, precision, recall, and F1-score
- Hyperparameters optimized via grid search

---

## 📈 Key Findings

- Strong positive correlation (0.90) between **Goals** and **Expected Goals (xG)**
- Age 31–40 bracket showed the highest match participation
- C. Madueke stood out as a highly versatile attacking player
- Notable market value anomaly: Liverpool had exceptionally high financial metrics

---

## 🤖 Ethical Considerations

This project adheres to GDPR principles and ethical data use. Key measures include:

- **Transparency** in data usage
- **Fairness** in model selection
- **Data security** awareness
- Recommendations made with a commitment to diversity and integrity in football recruitment

---

## 💡 Strategic Recommendations

- Focus model development on attacking roles, where data richness is highest
- Invest in players with proven consistency in xG vs. actual goals
- Utilize findings to balance experience (older players) with financial constraints
- Explore multiposition players like C. Madueke to improve tactical flexibility

---

## 📂 Folder Structure

```bash
nac-breda-player-selection/
│
├── data/                     # Processed datasets (no raw data uploaded for privacy)
├── notebooks/                # Jupyter notebooks for EDA and modeling
├── visuals/                  # Key visualizations used in the report
├── README.md                 # Project documentation (you’re here!)
└── report.pdf                # Full report submission (if available)
```
---

## 🙌 Credits

This project was developed as part of an academic collaboration and AI portfolio effort.

- **Author:** [MusaedMusaedSadeqMusaedAl-Fareh225739](https://github.com/MusaedMusaedSadeqMusaedAl-Fareh225739)  
- **LinkedIn:** [https://www.linkedin.com/in/musaed-alfareh-a365521b9](https://www.linkedin.com/in/musaed-alfareh-a365521b9)  
- **Institution:** [Breda University of Applied Sciences (BUAS)](https://www.buas.nl/en)  
- **Special Thanks:** [NAC Breda Football Club](https://www.nac.nl/) for their trust and forward-thinking approach in adopting data-driven methodologies  

---

## 📬 Contact

Have questions or want to collaborate?  
Feel free to reach out via [email](mailto:jimalfareh@gmail.com) or connect on [LinkedIn](https://www.linkedin.com/in/musaed-alfareh-a365521b9).

---
