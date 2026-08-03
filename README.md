# CardioAI+
CardioAI+ — A universal explainable cardiac risk intelligence framework supporting 11 ML models across anomaly detection and classification, with SHAP explainability, automatic dataset detection, and clinical risk recommendations.

## **The Story Behind This Project**
In 2023, my mother was rushed to hospital with a pericardial effusion — a life-threatening condition where fluid accumulates around the heart. The delayed diagnosis made me ask one question: could AI have detected the warning signs earlier?
That question became CardioAI. Then CardioAI Hybrid. Then CardioAI+.
This is not just a university project. It is a personal mission to make cardiac risk prediction more accessible, more accurate, and more explainable to the clinicians who need it most.

## **What CardioAI+ Does**
CardioAI+ is a universal cardiac risk intelligence framework that accepts any heart disease dataset in CSV format and automatically:
* Detects whether the dataset is binary or multi-class
* Preprocesses the data — handles missing values, encoding, and scaling
* Trains 6 supervised classification models and compares them
* Provides SHAP-based explanations showing WHY each model made each prediction
* Generates publication-quality comparison charts and ROC curves
* Delivers a clinical risk recommendation based on ensemble voting across all models
* 
## **Models Implemented**
Anomaly Detection (Unsupervised) — From CardioAI Hybrid
Isolation Forest - Tree-based - Fast general-purpose anomaly detection
Autoencoder - Deep Learning - Complex non-linear anomaly patterns
One-Class SVM - Kernel-based-High - dimensional anomaly detection
Local Outlier Factor - Density - based-Local density anomalies
LSTM Autoencoder-Sequence DL - Time-series cardiac signals

## **Classification (Supervised) — CardioAI+ Extension**
Logistic Regression - Linear - Interpretable baseline
Random Forest - Ensemble Trees - Robust, handles noise well
XGBoost - Gradient Boosting - State-of-the-art on tabular medical data
SVM Classifier - Kernel-based - Effective on high-dimensional medical data
MLP Neural Network - Feed-forward NN - Complex non-linear relationships
ANN (Keras) - Deep Learning - Deeper architecture with batch normalisation and dropout
Note: One-Class SVM (anomaly detection) and SVM Classifier (supervised classification) are different models serving different purposes. Both are included in this framework.

## **Key Features**
**Universal Dataset Loader**
Upload any heart disease CSV — the framework automatically detects your target column and determines whether binary or multi-class classification is needed.
## **Automatic Preprocessing Pipeline**
Handles missing values using median or mode imputation, encodes categorical variables, scales all features using StandardScaler, and generates a full preprocessing report.
## **SHAP Explainability**
Every prediction is explained using SHAP (SHapley Additive exPlanations) for Random Forest and XGBoost — showing which patient features drove the risk score up or down, making the system interpretable for clinical use.
## **ROC Curve Overlay**
All 6 classification models are compared on a single ROC curve chart with AUC-ROC scores — a publication-ready figure suitable for research papers.
## **Clinical Risk Recommendation**
An ensemble voting system collects predictions from all 5 sklearn models and outputs a structured clinical recommendation — High Risk, Moderate Risk, or Low Risk — with specific follow-up actions for each category.
## **Datasets Supported**
CardioAI+ accepts any tabular heart disease dataset in CSV format. It has been tested on:
UCI Heart Disease (Cleveland) - Binary - UCI ML Repository
Framingham Heart Study - Binary - Kaggle
Heart Failure Prediction - Binary - Kaggle
ECG Heartbeat Categorisation - Multi-class (ARR/AFF/CHF/NSR) - Kaggle / PhysioNet
Any uploaded heart CSV - Auto-detected - Your own dataset

## **Sample Results**
Results vary by dataset. The framework generates the following outputs after running:
* A comparison table of all 6 models across 5 metrics
* A 5-panel bar chart comparing Accuracy, Precision, Recall, F1 Score, and AUC-ROC
* Individual ROC curves for all models on one overlay chart
* SHAP bar and dot plots for Random Forest and XGBoost
* Confusion matrices for all 6 models
* ANN training loss and accuracy curves
* A clinical risk recommendation based on ensemble voting
## **What Makes CardioAI+ Different**
Dataset flexibility	- One fixed dataset - Any heart CSV — auto-detected
Model coverage - 1-2 models - 11 models across two paradigms
Explainability - None - SHAP for every prediction
Preprocessing - Manual - Fully automatic
Evaluation - Basic accuracy only - 5 metrics, ROC curves, confusion matrices
Clinical output - None - Ensemble-based clinical recommendation
Problem type support - Binary only - Binary and multi-class both

## **Clinical Motivation**
Cardiovascular disease is the leading cause of death globally, responsible for approximately 17.9 million deaths per year according to the World Health Organization. Early detection and risk stratification remain critical challenges in clinical practice.
CardioAI+ contributes by making cardiac risk prediction accessible across multiple dataset types, providing explainable predictions that clinicians can interpret, and comparing multiple model paradigms to identify the most reliable approach for each dataset.
**Important disclaimer**: CardioAI+ is a research prototype. All predictions and recommendations must be reviewed by a licensed medical professional. This tool is not approved for clinical use.


## **Future Work**
* Streamlit web dashboard for interactive clinical predictions
* LIME explainability alongside SHAP
* Native support for ECG time-series signal datasets
* PatternHunter AI — domain-agnostic generalisation of this framework to any tabular dataset beyond cardiac data

## **Acknowledgements**
* The SHAP library team for making ML explainability accessible
* UCI Machine Learning Repository for the Heart Disease dataset
* The scikit-learn, XGBoost, and TensorFlow communities
* My mother — whose medical emergency in 2023 inspired this project

*Built with purpose. Explained with SHAP. Dedicated to early cardiac detection.*
