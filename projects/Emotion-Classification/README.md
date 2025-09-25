---

# Emotion Classification from Arabic Reality Show Dialogue

<img align="left" src="./cia_logo.png" alt="CIA Logo" width="120"/>  

**Client:** Content Intelligence Agency (CIA)

This project focused on **classifying emotions in Arabic dialogue** collected from reality show content.
Since no large labeled dataset existed for this domain, we created one by **translating and adapting the GoEmotions dataset** into Arabic (including **Egyptian dialect**).
The project combined **classical ML, deep learning, and transformers (MARBERT)** into a full pipeline for robust Arabic emotion recognition.

---

## Project Highlights

* **Dataset Creation**:

  * Translated **GoEmotions (English)** → **Modern Standard Arabic (MSA)**.
  * Adapted dataset further into **Egyptian Arabic dialect**.
  * Validated and refined with **extensive manual analysis**.
* **Pipeline**: Speech-to-text → preprocessing → emotion classification.
* **Benchmarks**: Naive Bayes, Logistic Regression, RNN, BiLSTM.
* **State-of-the-Art**: Fine-tuned **MARBERT (Arabic Transformer)** for superior performance.
* **Standardized Labels**: Consolidated emotions into Ekman’s six universal categories (*happiness, sadness, anger, fear, surprise, disgust*).

---

## Key Takeaways

* Built a **custom Arabic emotion dataset** from English sources with translation + dialect adaptation.
* Hands-on experience with **low-resource language NLP** challenges.
* Fine-tuned **MARBERT**, achieving **weighted F1 ≈ 0.74–0.76**, outperforming classical and deep learning baselines.
* Applied **explainable AI** (attention visualization, LIME, SHAP) to validate predictions.

---

## Methodology

1. **Data Creation & Preprocessing**

   * Translated **GoEmotions → Arabic (MSA) → Egyptian dialect**.
   * Normalized Arabic text: diacritic removal, tokenization, stopword filtering.
   * Balanced dataset via augmentation techniques.

2. **Model Training**

   * **Baselines**: Naive Bayes, Logistic Regression with TF-IDF features.
   * **Deep Learning**: RNN & BiLSTM with weighted loss functions and early stopping.
   * **Transformers**: Fine-tuned **MARBERT** for Arabic emotion classification.

3. **Evaluation**

   * Metrics: Accuracy, Precision, Recall, F1-score.
   * MARBERT delivered the **highest weighted F1** compared to baselines.

4. **Explainability**

   * **Attention heatmaps** to visualize which words influenced predictions.
   * **LIME & SHAP** to provide interpretable examples for stakeholders.

---

## Results

* **Baselines**: ~60–65% accuracy.
* **RNN/BiLSTM**: ~70–73% weighted F1.
* **MARBERT**: **74–76% weighted F1**, best performance on translated + dialect data.
* Robust across multiple dialects (MSA & Egyptian Arabic).

---

## Tools & Technologies

* **Data Creation**: Google Translate + manual refinement for Arabic dialects.
* **Preprocessing**: NLTK, SpaCy-Arabic, custom tokenization.
* **Deep Learning**: PyTorch, TensorFlow.
* **Transformers**: Hugging Face MARBERT.
* **Explainability**: Attention visualization, LIME, SHAP.

---

## Applications

* **Media Analysis**: Identify emotional tone in Arabic reality shows & broadcasts.
* **Audience Insights**: Track sentiment & emotional response across Arabic-speaking regions.
* **Conversational AI**: Build emotion-aware Arabic dialogue systems & chatbots.

---

## Authors

* **Musaed Al-Fareh** – AI Engineer / Data Science Student @ BUas
* Collaborators – Block-C NLP Project Team

---

