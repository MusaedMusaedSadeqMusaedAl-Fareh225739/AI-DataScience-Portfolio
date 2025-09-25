# Traffic Accident Prevention in Breda with AI  

<img align="left" src="https://github.com/MusaedMusaedSadeqMusaedAl-Fareh225739/AI-DataScience-Portfolio/blob/main/projects/ANWB/anwb_logo.png" alt="ANWB Logo" width="120"/>  

This project leverages **deep learning** to predict high-risk accident areas in Breda, Netherlands, by analyzing **driving behavior, road conditions, and environmental factors**.  
The goal is to create **safer roads**, support **proactive traffic management**, and provide **data-driven insights for insurance optimization**.  

This initiative was conducted as part of a **Block-C project at Breda University of Applied Sciences (BUas)** in collaboration with **ANWB**.

---

##  The Challenge  
Traffic accidents are often caused by a **complex interplay of driving behavior, infrastructure, and environmental conditions**.  
Urban planners and authorities face the challenge of **identifying accident hotspots before they occur**.  

Our project addresses this by building predictive AI models trained on **multi-source datasets** to forecast accident severity and detect high-risk areas.

---

##  Solution & Methodology  

We designed a **machine learning pipeline** that integrates multiple datasets and applies deep learning models for prediction.  

### Models Applied
- **Convolutional Neural Networks (CNNs):** Spatial & temporal analysis of high-risk driving patterns.  
- **Multi-Layer Perceptron (MLP):** Structured prediction of accident severity based on engineered features.  

### Methodology Steps
1. **Data Collection & Integration**
   - **ANWB Safe Driving:** Driving events (speed, harsh braking, cornering).  
   - **Breda Road:** Road conditions, slopes, and usage.  
   - **KNMI Weather:** Weather conditions (precipitation, wind, temperature).  
   - **Argaleo Greenery:** Vegetation affecting visibility and road safety.  

2. **Preprocessing & Feature Engineering**  
   - Cleaning, normalization, and creation of engineered features.  

3. **Model Training & Evaluation**  
   - CNN and MLP trained on integrated datasets.  
   - Metrics: **Accuracy, Precision, Recall, F1-score**.  

4. **Deployment**  
   - **Streamlit dashboard** for real-time visualization of accident risk predictions.  

---

##  Key Results & Takeaways  
- **Strong Predictive Performance:** CNN & MLP both performed well in forecasting high-risk zones.  
- **Explainable AI:** Grad-CAM & Saliency Maps used to interpret and validate predictions.  
- **Real-Time Insights:** Streamlit dashboard enabled proactive, data-driven traffic management.  

---

##  Benefits of the Project  
- **Life-Saving Potential:** Identifies accident hotspots in advance, enabling targeted interventions.  
- **Smarter Traffic Management:** Provides municipalities with actionable, data-driven insights.  
- **Insurance Optimization:** Supports risk-based pricing models for insurers.  
- **Scalability:** Approach can be replicated in other cities beyond Breda.  

---

##  Technologies Used  
- **Python** – Core programming language.  
- **TensorFlow & PyTorch** – Deep learning frameworks.  
- **Streamlit** – Interactive dashboard deployment.  
- **SQL & Pandas** – Data management and processing.  
- **Seaborn & Matplotlib** – Data visualization.  

---

## 👥 Authors  
- **Musaed Al-Fareh** – AI Engineer / Data Science Student @ BUas  
- **Alexi Kehayias, Michon Goddijn, Benjamin Spiertz** – Collaborators, Block-C Project Team  
