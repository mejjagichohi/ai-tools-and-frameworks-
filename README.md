# 🧠 AI & Machine Learning Engineering Portfolio

This repository contains a collection of three distinct AI/ML tasks demonstrating proficiency in **Classical Machine Learning**, **Deep Learning (Computer Vision)**, and **Natural Language Processing (NLP)**.

Each task addresses a specific problem statement, from data preprocessing to model evaluation and ethical analysis.

## 📂 Project Structure

| File | Domain | Key Libraries | Description |
| :--- | :--- | :--- | :--- |
| `Task1_Iris_Classical_ML.ipynb` | Classical ML | `scikit-learn`, `pandas` | Decision Tree classifier for Iris species prediction. |
| `Task2_MNIST_CNN.ipynb` | Deep Learning | `tensorflow`, `keras` | CNN architecture for handwritten digit classification (MNIST). |
| `Task3_Amazon_NLP.ipynb` | NLP | `spacy` | Named Entity Recognition (NER) and rule-based sentiment analysis. |

---

## 🚀 Task Breakdowns

### 1. Classical ML: Iris Species Classification
**Objective:** Preprocess data and train a model to classify iris plants into three species.
* **Techniques:** Data imputation, Label Encoding, Decision Tree Classifier.
* **Metrics:** Accuracy, Precision, Recall (Macro-averaged).
* **Results:** The Decision Tree achieves high accuracy (>95%) on the test set due to the clear separability of the dataset features.

### 2. Deep Learning: MNIST Digit Recognition
**Objective:** Build a Convolutional Neural Network (CNN) to identify handwritten digits with >95% accuracy.
* **Architecture:**
    * 2x Convolutional Layers (Relu activation)
    * 2x Max Pooling Layers
    * Dense Output Layer (Softmax)
* **Performance:** Achieves **~98-99% accuracy** on the test set after 3 epochs.
* **Visualization:** Includes a custom function to visualize predictions vs. ground truth labels.
* **⚠️ Note:** Designed to run on **GPU**. If using Google Colab, enable T4 GPU runtime.

### 3. NLP: Amazon Review Analysis
**Objective:** Extract insights from unstructured text reviews.
* **Named Entity Recognition (NER):** Uses `en_core_web_sm` to identify brands and products.
* **Sentiment Analysis:** Implements a custom rule-based system (Lexicon approach) to score reviews as Positive, Negative, or Neutral based on adjective lemmas.

---

## ⚖️ Ethics & Optimization Report

A critical component of this project involves analyzing the ethical implications of the models:

1.  **Bias in Data:**
    * **MNIST:** Potential geographic bias (Western handwriting styles) could lower accuracy for users from different educational systems.
    * **Amazon Reviews:** Selection bias in reviews (polarized opinions) and potential language bias against non-standard English dialects.
2.  **Mitigation Strategies:**
    * **Fairness Indicators:** Recommended usage of TensorFlow Fairness Indicators to slice metrics by demographic groups.
    * **Entity Rulers:** Proposed adding manual rules to spaCy to ensure minority/local brands are recognized equally.

---

## 🛠️ How to Run

### Option 1: Google Colab (Recommended)
1.  Download the `.ipynb` files from this repo.
2.  Upload them to [Google Colab](https://colab.research.google.com/).
3.  **For Task 2 (MNIST):** Go to `Runtime` > `Change runtime type` > Select **T4 GPU**.
4.  Run all cells.

### Option 2: Local Environment (VS Code)
Ensure you have Python 3.8+ installed.

```bash
# Install dependencies
pip install numpy pandas scikit-learn matplotlib tensorflow spacy

# Download spaCy English model
python -m spacy download en_core_web_sm
