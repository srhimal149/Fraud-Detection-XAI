# Explainable AI for Financial Fraud Detection

End-to-end financial fraud detection using a Random Forest classifier on the PaySim synthetic dataset, with model interpretability via SHAP, DALEX, and Ceteris Paribus profiles.

## Overview

This project builds a complete fraud detection pipeline that not only achieves high classification accuracy but also provides transparent, interpretable explanations for its predictions. The notebook demonstrates how Explainable AI (XAI) techniques can be applied to a financial fraud detection model to satisfy regulatory and trust requirements.

## Dataset

The project uses the **PaySim Synthetic Financial Dataset** from Kaggle, which simulates mobile money transactions based on real-world data patterns.

- **Source:** [Kaggle — PaySim1](https://www.kaggle.com/datasets/ealaxi/paysim1)
- - **Size:** ~6.3 million transactions
  - - **Target:** Binary classification — fraudulent vs. legitimate transactions
   
    - ## Methodology
   
    - ### Data Preprocessing
    - - Filtered for fraud-relevant transaction types (TRANSFER and CASH_OUT)
      - - Engineered features including balance deltas and error flags
        - - Applied class-imbalance weighting to handle the skewed distribution
         
          - ### Model
          - - **Random Forest Classifier** with `n_estimators=100` and `class_weight={0:1, 1:100}`
            - - Train/test split for evaluation
              - - Benchmarked against a rule-based detection approach
               
                - ### Explainability (XAI)
                - - **SHAP** (SHapley Additive exPlanations) — global and local feature importance
                  - - **DALEX** — permutation-based feature importance
                    - - **Ceteris Paribus Profiles** — individual conditional expectation analysis
                     
                      - ## Key Results
                     
                      - - **Accuracy:** 99.999%
                        - - **False Positives:** 0
                          - - **Precision-Recall AUC:** ~0.995
                            - - Outperforms traditional rule-based fraud detection methods
                             
                              - ## Notebook Structure
                             
                              - | Section | Description |
                              - |---------|-------------|
                              - | 0 | Install Dependencies |
                              - | 1 | Imports & Configuration |
                              - | 2 | Load Data |
                              - | 3 | Data Cleaning & Feature Engineering |
                              - | 4 | Descriptive Statistical Analysis |
                              - | 5 | Correlation Matrix & Heatmap |
                              - | 6 | Train / Test Split |
                              - | 7 | Random Forest Classifier |
                              - | 8 | Confusion Matrix |
                              - | 9 | Precision-Recall Curve |
                              - | 10 | Rule-Based Benchmark |
                              - | 11 | Global Feature Importance (MDI) |
                              - | 12 | SHAP Values |
                              - | 13 | DALEX Explainer |
                              - | 14 | Ceteris Paribus Profiles |
                              - | 15 | Final Results Summary |
                             
                              - ## Requirements
                             
                              - ```
                                pandas
                                numpy
                                scipy
                                scikit-learn
                                matplotlib
                                seaborn
                                shap
                                dalex
                                ```

                                ## Getting Started

                                1. Clone this repository:
                                2.    ```bash
                                         git clone https://github.com/srhimal149/Fraud-Detection-XAI.git
                                         ```
                                      2. Download the PaySim dataset from [Kaggle](https://www.kaggle.com/datasets/ealaxi/paysim1) and place it in the project directory.
                                      3. 3. Open `fraud_detection_xai.ipynb` in Jupyter Notebook or JupyterLab.
                                         4. 4. Run all cells sequentially.
                                           
                                            5. ## License
                                           
                                            6. This project is for academic and educational purposes.
