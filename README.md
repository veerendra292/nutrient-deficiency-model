# nutrient-deficiency-model
# Nutrient Deficiency Prediction Model

## Overview

This project predicts nutrient deficiencies from symptom text using machine learning and natural language processing (NLP).
It is designed to handle real-world clinical-style inputs, including noise, negation, and multi-label conditions.

---

## Model Details

* Algorithm: Logistic Regression (MultiOutputClassifier)
* Feature Extraction: TF-IDF (n-grams: 1–2)
* Problem Type: Multi-label classification
* Dataset: Level 2 (Real-world dataset with 12,000 samples)

---

## Performance

### Test Set Performance

* F1 Score: ~0.86
* Precision: ~0.80
* Recall: ~0.72
* Hamming Accuracy: ~0.95
* Subset Accuracy: ~0.60

### Cross-Validation Performance

* F1 Score (CV): ~0.86
* Hamming Accuracy (CV): ~0.95
* Subset Accuracy (CV): ~0.60

---

## Interpretation

* The model achieves strong performance with high F1-score and Hamming accuracy, indicating reliable prediction of individual labels.
* Subset accuracy is lower due to the strict requirement that all 10 labels must be predicted correctly for each sample.
* The model generalizes well across different data splits, as shown by consistent cross-validation scores.
* Performance reflects realistic behavior on complex, noisy, and ambiguous data.

---

## Files

* `model.pkl` → Trained machine learning model
* `vectorizer.pkl` → TF-IDF text transformer
* `notebook.ipynb` → Full training and evaluation pipeline

---

## Example

Input:
fatigue dizziness pale skin low hemoglobin

Output:
iron

---

## Future Improvements

* Improve recall by adding more diverse and complex training samples
* Enhance handling of negation and contextual meaning
* Experiment with deep learning models (CNN / Transformers)
* Deploy as a web application

---

## Conclusion

This project demonstrates a complete machine learning pipeline for multi-label medical text classification, progressing from basic models to real-world robust datasets and optimization techniques. The final model achieves strong generalization and is suitable for practical applications.

---
