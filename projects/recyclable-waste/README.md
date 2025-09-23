# Recyclable Waste Classifier  

<img align="left" src="./projects/recyclable-waste/buas_logo.png" alt="BUas Logo" width="120"/>  

This project develops an **image classifier for recycling facilities** to enhance sorting efficiency and improve the quality of recycled materials.  
By leveraging deep learning, the system identifies **recyclable vs. non-recyclable items** in real-time, reducing contamination in recycling streams and enabling more sustainable operations.  

---

## Project Highlights
- **Problem**: Inefficient waste sorting leads to contamination and lower recycling quality.  
- **Solution**: A computer vision model that classifies recyclable vs. non-recyclable waste items.  
- **Dataset**: ~830 labeled images, 2 classes (*Recyclable*, *Non-Recyclable*) with 5 subcategories per class.  
- **Baseline Benchmarks**:  
  - Random guess → 50%  
  - Human-level → ~90%  
  - Basic MLP → ~83%  
- **Final Model**: Deep learning classifier with visual interpretability tools.  

---

## Key Takeaways
- **Improved Sorting Accuracy**: Helps recycling facilities streamline their processes.  
- **Operational Efficiency**: Reduces errors and contamination in recycling streams.  
- **Responsible AI**: Applied explainability methods (Saliency Maps, Grad-CAM) to interpret model decisions.  
- **Human-Centered Design**: Incorporated feedback from user studies to improve UX and interface design.  

---

## Model Performance
- Final classifier achieved strong accuracy compared to baseline models.  
- Applied **Grad-CAM & Saliency Maps** to visualize how the model detects objects, textures, and shapes in waste items.  

---

## Methodology
1. **Data Processing**: Loading, cleaning, preprocessing, and train/test split.  
2. **Modeling**: Designed and trained deep learning models.  
3. **Evaluation**: Benchmarked against baselines and validated using explainable AI tools.  
4. **User Testing**: Conducted UX-focused evaluation with design feedback.  

---

## Tools & Technologies
- **Python** (data preprocessing, modeling)  
- **Deep Learning Frameworks** (PyTorch/TensorFlow)  
- **Explainable AI**: Grad-CAM, Vanilla Saliency Maps  
- **UX Prototyping**: Wireframes & usability studies  

---

## Folder Structure
```plaintext
recyclable-waste/
├── README.md                 # Project description
├── buas_logo.png             # Project/BUas logo
├── datasets/                 # Training and validation data
├── models/                   # Trained models
├── notebooks/                # Jupyter notebooks
├── reports/                  # Presentations & project reports
└── visuals/                  # Plots, Grad-CAM, saliency maps
```
Key Recommendations

Deploy the model in recycling facilities for real-time waste classification.

Could you extend the dataset to improve robustness across materials and lighting conditions?

Integrate with sorting hardware for automated processing.

Authors

Musaed Alfareh – AI Engineer / Data Science student at BUas

Collaborators: Block-C Data Modelling team
