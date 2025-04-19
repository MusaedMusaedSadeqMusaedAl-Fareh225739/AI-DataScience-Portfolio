# NAC Breda Player Selection – The ML Edge

**Identifying Top Talents Through Data‑Driven Decisions**

---

![NAC Breda ](https://github.com/MusaedMusaedSadeqMusaedAl-Fareh225739/AI-DataScience-Portfolio/blob/main/projects/NAC%20Breda%20AI%20Player%20Selection/visuals/NAC.jpg)

---

## 📌 Overview

Football scouting is changing, and NAC Breda is at the forefront of that transformation. This project leverages data science and machine learning to support NAC Breda in identifying the most promising attacking players. By combining statistical rigor with football intelligence, we create a streamlined, efficient, and objective approach to player selection that aligns with the club’s goals and budget.

---

## 📊 Dataset Overview

- **Size:** 16,535 player records  
- **Features:** 114 (numerical + categorical)  
- **Focus:** Player attributes, performance metrics, and potential contribution to NAC Breda  
- **Source:** Aggregated from reputable football databases, APIs, and public records  

---

## 🔧 Tools & Technologies

- **Language:** Python  
- **Libraries:** pandas, NumPy, Matplotlib, Seaborn, scikit‑learn  
- **Model Used:** Logistic Regression  
- **Environment:** Jupyter Notebook  

---

## 🧪 Project Pipeline

### 1. Exploratory Data Analysis (EDA)
- Cleaned, visualized, and analyzed key features  
- Studied player market values, age distribution, and position versatility  
- Assessed missing values, outliers, and anomalies  

#### Key Visuals

**Age vs. Market Value**  
![Market Value vs. Age](https://github.com/MusaedMusaedSadeqMusaedAl-Fareh225739/AI-DataScience-Portfolio/blob/main/projects/NAC%20Breda%20AI%20Player%20Selection/visuals/AGE.png)

**Position Distribution**  
![Player Positions Distribution](https://github.com/MusaedMusaedSadeqMusaedAl-Fareh225739/AI-DataScience-Portfolio/blob/main/projects/NAC%20Breda%20AI%20Player%20Selection/visuals/POST.png)

**Goals vs. Expected Goals (xG)**  
![Scatter Plot: Goals vs. xG](https://github.com/MusaedMusaedSadeqMusaedAl-Fareh225739/AI-DataScience-Portfolio/blob/main/projects/NAC%20Breda%20AI%20Player%20Selection/visuals/scatter.png)

**Top 10 Attackers: xG vs. Actual Goals**  
![Top 10: xG vs. Goals](https://github.com/MusaedMusaedSadeqMusaedAl-Fareh225739/AI-DataScience-Portfolio/blob/main/projects/NAC%20Breda%20AI%20Player%20Selection/visuals/TOP%2010.png)

---

### 2. Data Preprocessing
- One‑hot encoded categorical features  
- Normalized numerical variables  
- Removed duplicates and corrected inconsistencies  

---

### 3. Model Development
- Selected **Logistic Regression** for its speed, interpretability, and binary‑classification performance  
- Trained to identify high‑potential attackers based on selected performance metrics  

---

### 4. Model Evaluation
- Evaluated using **Accuracy**, **Confusion Matrix**, **Precision**, **Recall**, and **F1‑Score**  
- Hyperparameters optimized via grid search  

---

## 📈 Key Findings

- **Correlation**: Strong positive relationship (0.90) between **Goals** and **Expected Goals (xG)**  
- **Experience Matters**: Players aged 31–40 logged the highest match participation  
- **Versatility**: C. Madueke emerged as a top multiposition attacking asset  
- **Market Value Outlier**: Liverpool’s financial metrics stood significantly above the rest  

---

## 🤖 Ethical Considerations

This project adheres to GDPR principles and ethical data use:  
- **Transparency** in data usage  
- **Fairness** in model selection  
- **Data Security** awareness  
- Commitment to diversity and integrity in football recruitment  

---

## 💡 Strategic Recommendations

- **Attackers First**: Concentrate modeling efforts where data is richest—attacking roles  
- **xG Consistency**: Scout for players with a track record of meeting or exceeding their xG  
- **Experience vs. Budget**: Balance seasoned veterans with financial constraints  
- **Tactical Flexibility**: Prioritize multiposition attackers like C. Madueke  

---

## 📂 Folder Structure

```bash
nac-breda-player-selection/
│
├── data/                     # Processed datasets
├── notebooks/                # EDA & modeling notebooks
├── visuals/                  # Key visual assets
├── README.md                 # Project documentation (you’re here!)
└── report.pdf                # Full report submission
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
