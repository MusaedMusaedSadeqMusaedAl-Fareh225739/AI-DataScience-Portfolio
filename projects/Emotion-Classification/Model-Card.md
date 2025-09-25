# Model Card: MARBERT-Based Emotion Classifier for Arabic Text

---

## Model Overview

This model is a fine-tuned version of **UBC-NLP/MARBERT**, a pre-trained BERT-based transformer designed specifically for Arabic language processing. It has been adapted for emotion classification over seven classes: neutral, happiness, sadness, anger, surprise, fear, and disgust.

The model was trained on labeled Arabic social text and evaluated on held-out and external datasets. It incorporates extensive error analysis and explainability to support trustworthy and responsible deployment.

---

## Architecture

- **Base Model:** MARBERT (based on BERT architecture)
- **Fine-Tuning:** Classification head added for 7 emotion classes
- **Training Framework:** Hugging Face Transformers with PyTorch backend
- **Tokenizer:** WordPiece tokenizer from MARBERT
- **Training Configuration:**
  - **Batch size:** 128 (training) / 128 (eval)
  - **Learning rate:** 3e-5
  - **Epochs:** 15
  - **FP16 mixed precision:** Enabled
  - **cuDNN benchmark:** Enabled (optimized for NVIDIA A6000 GPU)
  - **DataLoader workers:** 16
  - **Checkpoint Output:** model.safetensors, tokenizer configs, evaluation logs

---

## Purpose

The model was developed to classify emotions in Arabic-language social text, especially for media monitoring and sentiment analysis applications.

It supports:

- Automated analysis of user-generated Arabic content (e.g., social media, forums)
- Media client use cases like trend detection, content moderation, and audience reaction mapping
- Low-resource NLP experimentation for dialectal Arabic

---

## Development Context

- **Hardware:** NVIDIA A6000 GPU with PyTorch 2.6
- **Software Stack:** Transformers 4.x, scikit-learn, pandas, matplotlib
- **Training Time:** ~10 minutes and 53 seconds for 15 epochs

**Constraints:**

- Class imbalance, especially in disgust, surprise, and fear
- No external knowledge bases or emotion lexicons used
- Emotion subjectivity in annotation and label noise in test data

---

## Intended Use

This model is suitable for:

- Media analysis pipelines detecting emotion in video subtitles or comment streams
- Social sentiment research in Arabic-speaking communities
- Dialogue systems or virtual agents responding to emotion cues

**NOT recommended for:**

- Clinical or mental health applications
- Legal or high-stakes decision-making
- Languages outside Arabic or low-resource dialects not represented in training

---

## Dataset Details

We used the **GoEmotions dataset**, originally sourced from Reddit, as the base for training. It contains user-generated text annotated with 28 emotion labels. These were mapped to 7 core emotions — happiness, neutral, anger, sadness, disgust, surprise, and fear — to simplify the classification task.

**Preprocessing steps included:**

- Cleaning the text (removing duplicates, noise, and irrelevant content)
- Translating to Modern Standard Arabic (MSA) using Google Translate
- Adapting to Egyptian Arabic using the `facebook/nllb-200-distilled-600M` model via Hugging Face Transformers

The final version of our dataset (`goemotion_egy.csv`) contains both MSA and Egyptian Arabic text aligned with the 7 core emotion labels.

**Label Distribution (Train Set):**

| Emotion   | Samples |
|-----------|---------|
| happiness | 14,012  |
| neutral   | 13,723  |
| anger     | 6,454   |
| sadness   | 2,838   |
| disgust   | 1,129   |
| surprise  | 950     |
| fear      | 811     |

This imbalance may bias the model toward high-frequency emotions. Future work may include balancing techniques such as class weighting or data augmentation.

---

## Test Set & Evaluation

We evaluated the model using a real-world Arabic YouTube video containing expressive emotional speech. The test set is highly imbalanced (e.g., only 3 samples of disgust), yet the model successfully predicted several low-frequency emotions, suggesting a degree of generalization.

---

## Language, Cultural Representation & Multilingual Challenges

The original dataset reflects Western, English-speaking contexts, while the translated version aims to capture Arabic linguistic and cultural nuances. We selected Egyptian Arabic for its high representation (~50%) in regional emotional communication, based on analysis of real-world data. This enhances cultural relevance for Arabic-speaking users.

**Challenges in translating emotion-rich content:**

- Some words or phrases may not have direct equivalents.
- Dialectal variations can affect emotional intensity and interpretation.
- The model is trained on written data but evaluated on spoken dialect, which may create mismatches.

These issues underscore the importance of further dialect coverage and culturally aligned annotation in future datasets.

---

## Performance Metrics and Evaluation

### 1. Performance Overview

- **Overall Accuracy:** 75.76% (on 462 samples)

**Per-Class Performance:**

- **Neutral:**  
  - Precision: 0.8210  
  - Recall: 0.9042  
  - F1-score: 0.8606
- **Anger:**  
  - F1-score: 0.3000
- **Sadness:**  
  - F1-score: 0.4500
- **Happiness:**  
  - F1-score: 0.2462
- **Surprise:**  
  - F1-score: 0.5333
- **Fear:**  
  - F1-score: 0.2667
- **Disgust:**  
  - F1-score: 0.0000

**Aggregated Metrics:**

- **Weighted F1-score:** 0.7373
- **Macro F1-score:** 0.3795

---

### 2. Error Analysis Highlights

- **Neutral Bias:**  
  The model often defaults to predicting neutral even when distinct emotions are present.

- **Sentence Length Impact:**  
  Longer sentences tend to have higher misclassification rates (up to 0.55% error for sentences with 7–15 tokens). As shown in the bar chart below, the (7–15) token range exhibits the highest error rate:  
  ![Error Rate by Sentence Length](https://github.com/BredaUniversityADSAI/2024-25c-fai2-adsai-group-arb-5/blob/main/DataLab%20Tasks/Task%208/erorr.png)

- **Ambiguity in Language:**  
  Repeated patterns (e.g., phrases like "من كده" or "أكبر من كده") contribute to systematic misclassifications.

- **Overconfidence:**  
  Incorrect predictions are frequently made with moderate to high confidence (0.5 to 0.7), indicating overconfidence in ambiguous cases. For additional visual context, see the illustration below:  
  ![Overconfidence Visual](https://github.com/BredaUniversityADSAI/2024-25c-fai2-adsai-group-arb-5/blob/main/DataLab%20Tasks/Task%208/over.png)

---

### 3. Recommendations for Improvement

- **Data Balancing:**  
  Consider applying class weighting or data augmentation techniques for underrepresented emotions.
  
- **Enhance Contextual Understanding:**  
  Refine feature engineering approaches to better capture subtle language nuances, especially in longer texts.
  
- **Continued Evaluation:**  
  Further analyze misclassified examples to identify specific linguistic challenges and adjust the model accordingly.

---

### 4. Additional Details & Files

- **Error Analysis Details:**  
  - [Error_Analysis.ipynb](https://github.com/BredaUniversityADSAI/2024-25c-fai2-adsai-group-arb-5/blob/main/DataLab%20Tasks/Task%208/Error_Analysis.ipynb)  
  - [Error Analysis Notebook.pdf](https://github.com/BredaUniversityADSAI/2024-25c-fai2-adsai-group-arb-5/blob/main/DataLab%20Tasks/Task%208/Error%20Analysis%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20%20Notebook.pdf)

- **Explainable AI (XAI) Analysis:**  
  - [XAI_notebook (1).ipynb](https://github.com/BredaUniversityADSAI/2024-25c-fai2-adsai-group-arb-5/blob/main/DataLab%20Tasks/Task%209/XAI_notebook%20(1).ipynb)  
  - [XAI in Emotion Classification Using Transformer Models.pdf](https://github.com/BredaUniversityADSAI/2024-25c-fai2-adsai-group-arb-5/blob/main/DataLab%20Tasks/Task%209/XAI%20in%20Emotion%20Classification%20Using%20Transformer%20Models.pdf)

---

## Explainability and Transparency

- **Token-Level Relevance:**  
  Each token in the sentence is assigned a relevance score indicating its contribution to the final prediction. These scores are computed using techniques such as Gradient × Input and Layer-wise Relevance Propagation (LRP). Strong emotional tokens (e.g., “حب” for love) receive high relevance, driving accurate predictions.

- **Handling Ambiguity:**  
  When emotional cues are clear and strong, the model confidently assigns the corresponding emotion. However, if the input contains ambiguous or diluted signals—even if key emotional words like “شكت” or “اتهمت” (indicative of anger) are present—the model may not give these tokens sufficient weight, often defaulting to a neutral prediction.

- **Mismatch Between Expected and Assigned Relevance:**  
  Our analysis revealed that the model sometimes assigns significant relevance to tokens that might seem unimportant from a human perspective while underweighting critical emotional tokens. This discrepancy shows that the internal decision process of the model doesn’t always align with human expectations, causing occasional misclassifications.

- **Decision Aggregation:**  
  Ultimately, the model sums the weighted contributions of all tokens to form its final prediction. When the combined effect of strongly relevant tokens is decisive, the predicted emotion is accurate. In cases where ambiguity or irrelevant influence dominates, the prediction tends to lean toward neutral.

For technical details on how these relevance scores are computed and visualized, please refer to our repository files: **[XAI_notebook (1).ipynb](https://github.com/BredaUniversityADSAI/2024-25c-fai2-adsai-group-arb-5/blob/main/DataLab%20Tasks/Task%209/XAI_notebook%20(1).ipynb)**, and **[XAI in Emotion Classification Using Transformer Models.pdf](https://github.com/BredaUniversityADSAI/2024-25c-fai2-adsai-group-arb-5/blob/main/DataLab%20Tasks/Task%209/XAI%20in%20Emotion%20Classification%20Using%20Transformer%20Models.pdf)**.

All techniques followed the principles outlined in Ali et al. (2022):

> **"XAI for Transformers: Better Explanations through Conservative Propagation"**  
> [https://proceedings.mlr.press/v162/ali22a/ali22a.pdf](https://proceedings.mlr.press/v162/ali22a/ali22a.pdf)

---

## Recommendations for Use

- **Bias and Ambiguity:**  
  The model often defaults to neutral when faced with unclear emotional cues. Users should consider implementing confidence thresholding or human review for ambiguous cases.
  
- **Overconfidence Risk:**  
  Our analysis shows that the model can be overconfident in its misclassifications. Regular calibration and monitoring of prediction confidence are recommended.
  
- **Cultural and Linguistic Alignment:**  
  As the model was adapted from an English-based dataset to Arabic, ensure that deployment aligns with the target language’s nuances. Fine-tuning on additional local data may be necessary.

### 2. Use Cases for Media Companies and Client Stakeholders

- **Audience Sentiment Analysis:**  
  Employ the model to gauge public sentiment from social media comments or video subtitles, especially where strong, clear emotional signals are present.
  
- **Content Personalization:**  
  Use emotion classification to tailor recommendations and advertising based on detected emotional tone, enhancing engagement and customer satisfaction.
  
- **Customer Support & Feedback:**  
  Integrate the model into customer support pipelines to rapidly assess sentiment in text-based interactions, with manual intervention for ambiguous outputs.

### 3. Risk Mitigation and Continuous Improvement

- **Post-Processing and Oversight:**  
  Incorporate mechanisms for error detection and fallback processing (e.g., human review) when confidence levels are low or predictions appear inconsistent.
  
- **Iterative Refinement:**  
  Leverage ongoing error analysis and XAI insights to refine data augmentation, improve feature engineering, and update the model in response to new linguistic patterns.

---

## Sustainability Considerations

- **Training Hardware:**  
  Single NVIDIA A6000 (Ampere architecture, energy efficient)
  
- **Training Time:**  
  ~10 minutes and 53 seconds for 15 epochs
  
- **Storage Footprint:**  
  ~400MB (model + tokenizer)

**Green Optimization Steps Taken:**

- cuDNN benchmark and FP16 mixed precision enabled
- DataLoader optimizations to avoid CPU bottlenecks
- Reuse of pre-trained MARBERT weights reduced training time by 90% versus training from scratch

**Recommendations:**

- Use batch inference to reduce compute cost
- Host the model on platforms using carbon-aware scheduling (e.g., Hugging Face Accelerated Inference)

---

## References

- Ali, et al. (2022). **XAI for Transformers: Better Explanations through Conservative Propagation**. Available at: [https://proceedings.mlr.press/v162/ali22a/ali22a.pdf](https://proceedings.mlr.press/v162/ali22a/ali22a.pdf)

- **GoEmotions Dataset:** Available at: [https://github.com/google-research/google-research/tree/master/goemotions](https://github.com/google-research/google-research/tree/master/goemotions)

- Abdul-Mageed, Muhammad, Elmadany, AbdelRahim, & Nagoudi, El Moatez Billah. (2021). **ARBERT & MARBERT: Deep Bidirectional Transformers for Arabic**. In *Proceedings of the 59th Annual Meeting of the Association for Computational Linguistics and the 11th International Joint Conference on Natural Language Processing (Volume 1: Long Papers)* (pp. 7088–7105). Association for Computational Linguistics. Available at: [https://aclanthology.org/2021.acl-long.551](https://aclanthology.org/2021.acl-long.551)

*We used the above references for additional insights.*
