# -Wearer-Verification-and-Identity-Attribution-Using-Smartwatch-Data
# Neural Network-Based Biometric Case Classification

## 🔍 Project Summary
This project presents a deep learning framework designed to classify biometric cases using structured feature data.  
The objective is to develop an automated classification system capable of detecting distinctive biometric patterns and assigning them to the appropriate case category.

The implementation relies on a fully connected neural network built with TensorFlow and Keras, combined with structured preprocessing and optimization techniques to enhance predictive stability and reliability.

---

## Project Goals
- Develop a multi-class biometric classification model
- Address dataset imbalance using weighted learning
- Apply normalization and feature preprocessing
- Assess model performance through quantitative evaluation metrics
- Provide a technical foundation for forensic biometric analysis

---

##  Data Description
The dataset includes multiple biometric-derived attributes alongside a classification label.

- **Predictor Variables:** Extracted biometric measurements
- **Target Label:** `DB_Case`

To improve modeling quality:
- Irrelevant attributes such as timestamps and demographic indicators were excluded
- Target labels were encoded numerically
- Feature scaling was applied using standard normalization techniques

---

##  Tools and Libraries
- Python
- TensorFlow / Keras
- Scikit-learn
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Joblib

---

##  Model Design

The classification model follows a layered feedforward neural network structure:

1. Fully Connected Layer (128 units, ReLU)
2. Batch Normalization
3. Dropout (25%)

4. Fully Connected Layer (64 units, ReLU)
5. Batch Normalization
6. Dropout (25%)

7. Fully Connected Layer (32 units, ReLU)
8. Dropout (25%)

9. Output Layer (Softmax activation for multi-class prediction)

**Optimization Details:**
- Loss Function: Sparse Categorical Crossentropy
- Optimizer: Adam

---

##  Model Stabilization Techniques
To enhance generalization and prevent overfitting, the following methods were applied:

- Dropout regularization
- Batch normalization
- Early stopping based on validation loss
- Adaptive learning rate reduction (ReduceLROnPlateau)
- Class weight adjustment for imbalanced data

---

##  Implementation Workflow
The development process included:

- Data loading and inspection
- Feature selection and cleaning
- Label encoding
- Stratified train-test splitting
- Standardization using `StandardScaler`
- Model training and validation
- Performance evaluation on unseen test data

---

## Performance Results

**Test Accuracy:** 88.7%  
**Test Loss:** 0.446  

The model demonstrates strong classification capability and maintains consistent performance across multiple biometric categories.

Evaluation metrics included:
- Overall accuracy
- Precision, Recall, and F1-score
- Confusion matrix analysis
- Training and validation performance curves

---

## Forensic Relevance

The proposed system contributes to digital forensic workflows by:

- Automating biometric case categorization
- Assisting in identity-related investigations
- Supporting analytical processing of biometric datasets
- Reducing manual effort in forensic data examination

