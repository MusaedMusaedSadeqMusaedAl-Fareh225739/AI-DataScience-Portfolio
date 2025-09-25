Traffic Accident Prevention in Breda with AI 
<img align="left" src=https://github.com/MusaedMusaedSadeqMusaedAl-Fareh225739/AI-DataScience-Portfolio/blob/main/projects/ANWB/anwb_logo.png alt="ANWB Logo" width="120"/>

This project uses deep learning to predict high-risk accident areas in Breda, Netherlands, by analyzing driving behavior, road conditions, and environmental data. Our goal is to create safer roads, support proactive traffic management, and provide data-driven insights for insurance optimization. This initiative was part of a Block-C project at Breda University of Applied Sciences (BUas), in collaboration with ANWB.

The Challenge
Traffic accidents are often caused by a complex combination of factors, including high-risk driving behaviors and unpredictable environmental conditions. Identifying accident hotspots before they occur is a critical challenge for urban planners and traffic authorities. This project addresses this problem by leveraging a rich, multi-source dataset to predict accident severity and pinpoint high-risk areas.

Solution & Methodology
Our solution employs a machine learning pipeline to integrate and analyze various datasets. We used two primary deep learning models to predict accident risks:

Convolutional Neural Networks (CNN): Used for spatial and temporal analysis of high-risk driving patterns.

Multi-Layer Perceptron (MLP): Used for structured prediction of accident severity based on a range of features.

The project's methodology followed these key steps:

Data Collection & Integration: We integrated four distinct datasets:

ANWB Safe Driving: Contains driving events like speed, harsh braking, and cornering.

Breda Road: Includes data on road conditions, slopes, and usage.

KNMI Weather: Provides weather data, such as precipitation and temperature.

Argaleo Greenery: Offers information on vegetation affecting visibility and road conditions.

Preprocessing & Feature Engineering: Raw data was cleaned, normalized, and engineered to create meaningful features for our models.

Model Training & Evaluation: The CNN and MLP models were trained and then evaluated using standard metrics like accuracy, precision, recall, and F1-score.

Deployment: A Streamlit dashboard was developed for real-time visualization of risk predictions, providing an intuitive interface for traffic managers and other stakeholders.

Key Results & Takeaways
Strong Predictive Performance: Both the CNN and MLP models achieved strong performance in predicting accident severity and identifying high-risk locations.

Explainable AI: We used techniques like Grad-CAM and Saliency Maps to interpret our model's predictions, providing transparency and trust in the AI's recommendations.

Real-Time Insights: The Streamlit application effectively demonstrated how real-time insights can be used for proactive traffic management.

Benefits of the Project
Life-Saving Potential: Our models can help identify accident hotspots before incidents happen, enabling authorities to implement targeted interventions and save lives.

Smarter Traffic Management: Provides local authorities with a data-driven tool for optimizing traffic flow and road safety.

Insurance Optimization: The insights can inform dynamic, risk-based pricing models for insurance providers, promoting safer driving.

Scalability: The approach is scalable and can be applied to other cities beyond Breda.

Technologies Used
Python: Core language for data processing and model development.

TensorFlow & PyTorch: Frameworks for building and training deep learning models.

Streamlit: For creating the interactive web dashboard.

SQL & Pandas: For efficient data management and manipulation.

Seaborn & Matplotlib: For data visualization.



Authors

Musaed Al-Fareh – AI Engineer / Data Science student at BUas

Alexi Kehayias, Michon Goddijn, Benjamin Spiertz – Collaborators, Block-C Project Team
