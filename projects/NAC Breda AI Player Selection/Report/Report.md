# NAC Breda Player Selection – The ML Edge  
**Identifying Top Talents Through Data‑Driven Decisions**  

---

## 📌 Overview  
Football scouting is evolving, and NAC Breda is leading the charge. This project uses data science and machine learning to pinpoint under‑the‑radar attackers who maximize performance per euro. By marrying statistical rigor with football insight, we deliver a transparent, budget‑aligned roadmap for recruiting top strikers.

---

## 📊 Dataset Overview  
- **Rows:** 16 535 players  
- **Features:** 114 (105 numerical, 9 categorical)  
- **Focus:** Performance metrics (Goals, xG, Minutes, Market Value, etc.)  
- **Source:** Aggregated from public APIs, club records & reputable football databases  

---

## 🔧 Tools & Technologies  
- **Language:** Python 3.8+  
- **Libraries:** pandas, NumPy, Matplotlib, Seaborn, scikit‑learn  
- **Model:** Logistic Regression  
- **Environment:** Jupyter Notebook / VS Code  

---

## 🧪 Project Pipeline  

### 1. Exploratory Data Analysis (EDA)  
- Handled missing values (mean/mode imputation)  
- Detected & treated outliers (IQR, log‑transform)  
- Visualized distributions & relationships  

### 2. Data Preprocessing  
- One‑hot encoding for categorical features  
- Standard scaling for numerical features  
- Train/test split (80/20)  

### 3. Model Development  
- Logistic Regression in an sklearn `Pipeline`  
- Hyperparameter tuning via `GridSearchCV`  

### 4. Evaluation & Interpretation  
- Metrics: Accuracy, Confusion Matrix, Precision, Recall, F1  
- Final accuracy: **0.953**  

---

## 📈 Key Visualizations  

### Player Positions  
![Position Distribution](https://github.com/MusaedMusaedSadeqMusaedAl-Fareh225739/AI-DataScience-Portfolio/blob/main/projects/NAC%20Breda%20AI%20Player%20Selection/visuals/POST.png)  
*Figure 1. Distribution of player positions*

---

### Age vs. Market Value  
![Market Value vs Age](https://github.com/MusaedMusaedSadeqMusaedAl-Fareh225739/AI-DataScience-Portfolio/blob/main/projects/NAC%20Breda%20AI%20Player%20Selection/visuals/AGE.png)  
*Figure 2. How market value varies with age*

---

### Goals vs. Expected Goals (xG)  
![Goals vs xG Scatter](https://github.com/MusaedMusaedSadeqMusaedAl-Fareh225739/AI-DataScience-Portfolio/blob/main/projects/NAC%20Breda%20AI%20Player%20Selection/visuals/scatter.png)  
*Figure 3. Strong positive correlation (ρ = 0.90)*

---

### Top 10 Attackers: xG vs. Goals  
![Top 10: xG vs Goals](https://github.com/MusaedMusaedSadeqMusaedAl-Fareh225739/AI-DataScience-Portfolio/blob/main/projects/NAC%20Breda%20AI%20Player%20Selection/visuals/TOP%2010.png)  
*Figure 4. Players who outperform their xG*

---

### Club Logo  
![NAC Breda FC](https://github.com/MusaedMusaedSadeqMusaedAl-Fareh225739/AI-DataScience-Portfolio/blob/main/projects/NAC%20Breda%20AI%20Player%20Selection/visuals/NAC.jpg)  
*Figure 5. NAC Breda Football Club*

---

## 🤖 Modeling Details  

```python
from sklearn.pipeline       import Pipeline
from sklearn.compose        import ColumnTransformer
from sklearn.impute         import SimpleImputer
from sklearn.preprocessing  import StandardScaler, OneHotEncoder
from sklearn.linear_model   import LogisticRegression
from sklearn.model_selection import GridSearchCV, train_test_split

# Define feature sets
num_cols = [...]  # all numeric except 'xG'
cat_cols = [...]  # ['Player','Team','Position',…]

# Build pipelines
num_pipe = Pipeline([('imp', SimpleImputer()), ('sc', StandardScaler())])
cat_pipe = Pipeline([('imp', SimpleImputer(strategy='most_frequent')),
                     ('ohe', OneHotEncoder(handle_unknown='ignore'))])

preproc = ColumnTransformer([('num', num_pipe, num_cols),
                             ('cat', cat_pipe, cat_cols)])

model = Pipeline([('prep', preproc),
                  ('clf', LogisticRegression(max_iter=1000))])

# Train/test split
X_train, X_test, y_train, y_test = train_test_split(
    df.drop(['xG','high_xG'], axis=1),
    df['high_xG'],
    test_size=0.2, random_state=42)

# Hyperparameter search
grid = GridSearchCV(model,
                    {'clf__C':[0.1,1,10], 'clf__penalty':['l1','l2']},
                    cv=5, scoring='accuracy')
grid.fit(X_train, y_train)
```
---

📊 Evaluation
Best parameters: C=1, penalty='l2'

Accuracy: 0.953

Confusion Matrix:


         	Pred 0	Pred 1
True 0	 1010  	   64  
True 1	   93  	 2140  
Precision / Recall / F1: all > 0.92
---

💡 Conclusions & Recommendations
xG → Goals: ρ=0.90 validates xG as a finishing proxy.

Recruitment window: 20–25 yrs for optimal value.

Versatile targets: multiposition strikers boost tactical flexibility.

Next steps: integrate injury/risk data and explore ensemble models.

---
