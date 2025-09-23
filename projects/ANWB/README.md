Traffic Accident Prevention in Breda with AI
<img align="left" src=https://github.com/MusaedMusaedSadeqMusaedAl-Fareh225739/AI-DataScience-Portfolio/blob/main/projects/ANWB/anwb_logo.png
alt="BUas Logo" width="120"/>

This project leverages deep learning (CNN & MLP models) to predict high-risk accident areas in Breda using driving, road, and environmental data.
The goal is to reduce accidents, support traffic management, and optimize insurance premiums through data-driven insights.

Project Highlights

Problem: High-risk driving behaviors and complex road conditions lead to accidents in Breda.

Solution: Predict accident severity and high-risk locations using deep learning.

Datasets Used:

ANWB Safe Driving – driving events (speed, harsh braking, cornering, severity).

Breda Road – road conditions, usage, slopes.

KNMI Weather – precipitation, wind, temperature.

Argaleo Greenery – vegetation impacting visibility and road conditions.

Models:

CNN (Convolutional Neural Networks) – spatial & temporal analysis of high-risk patterns.

MLP (Multi-Layer Perceptron) – structured prediction of accident severity.

Deployment: Streamlit-based dashboard for real-time prediction and risk visualization.

Key Takeaways

Life-Saving Potential: Identify accident hotspots before they occur.

Smarter Traffic Management: Supports local authorities with targeted interventions.

Insurance Optimization: Provides dynamic risk-based pricing models.

Environmental Awareness: Incorporates weather and greenery into predictive insights.

Methodology

Data Collection – Integrating driving, road, and environmental datasets.

Preprocessing – Cleaning, feature engineering, and normalization.

Modeling – Training CNN and MLP models for accident prediction.

Evaluation – Benchmarked with accuracy, precision, recall, and F1-score.

Deployment – Real-time dashboard for monitoring and alerts.

Results

CNN & MLP achieved strong performance in predicting severity levels and detecting high-risk areas.

Explainability methods (Grad-CAM, Saliency Maps) used to interpret model predictions.

Streamlit application demo provided real-time insights for traffic managers.

Tools & Technologies

Python – Data preprocessing, model development.

TensorFlow & PyTorch – Deep learning model training.

Streamlit – Interactive dashboard for deployment.

SQL & Pandas – Data management and feature engineering.

Visualization – Seaborn, Matplotlib.

Project Benefits

Safer roads and more efficient traffic systems.

Improved decision-making for insurance providers.
Enhanced support for local authorities and emergency services.

Scalable approach for other cities beyond Breda.


Folder Structure
```
traffic-accident-prevention/
├── README.md                # Project documentation
├── datasets/                # Data files (ANWB, KNMI, Argaleo, Breda Road)
├── notebooks/               # Model training & evaluation notebooks
├── models/                  # Trained deep learning models
├── reports/                 # Project Proposal & Presentations
└── visuals/                 # Plots, Grad-CAM, and saliency maps
````
Authors

Musaed Al-Fareh – AI Engineer / Data Science student at BUas

Alexi Kehayias, Michon Goddijn, Benjamin Spiertz – Collaborators, Block-C Project Team
