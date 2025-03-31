Cyber Threat Detection Using Machine Learning
This repository contains the code and resources developed for my MSc Computer Science dissertation titled "Cyber Threat Detection Using Machine Learning" at the University of Sussex.

**📖 Overview**

The project explores the application of machine learning (ML) techniques for detecting botnet activities in network traffic, using the CTU-13 dataset. It focuses on implementing and comparing various ML algorithms—such as Support Vector Machines (SVM), Long Short-Term Memory (LSTM) networks, Random Forest, Logistic Regression, and hybrid models—to improve accuracy and effectiveness in cybersecurity threat detection.

🎯**Objectives**

Detect and classify botnet traffic using ML models.

Compare the performance of individual ML models and hybrid approaches.

Evaluate model accuracy, precision, recall, and F1-score.

Propose improvements using data preprocessing, feature engineering, and ensemble modeling.

📊**Models Implemented**

Support Vector Machine (SVM)

Long Short-Term Memory (LSTM)

Logistic Regression

Random Forest

Hybrid Model: SVM + LSTM

Hybrid Model: Random Forest + Logistic Regression


📈 **Key Results**

Model	Accuracy

Support Vector Machine (SVM)	89.51%

Long Short-Term Memory (LSTM)	96.77%

Logistic Regression	85.17%

Random Forest	99.62%

Hybrid: SVM + LSTM	94.90%

Hybrid: Random Forest + LR	99.60%


**🛠Technology Stack**

Python

Jupyter Notebook

Scikit-learn

TensorFlow / Keras

Pandas / NumPy

Matplotlib / Seaborn

SMOTE (for data balancing)


🧪**Dataset**

CTU-13 Dataset
Real-world labeled traffic data including Botnet, Normal, and Background activity. Source: CTU University, Czech Republic.

**📌 Highlights**

Data preprocessing: PCA, normalization, SMOTE

Visualizations: Heatmaps, accuracy/loss curves, confusion matrices

Hybrid modeling for improved robustness

Real-time detection considerations using sequential models like LSTM


**📚 Acknowledgements**
Special thanks to Professor Daniel Creed for his continuous guidance and support throughout the development of this project

**📝 License**
This project is not licensed for public or commercial use. It is uploaded solely for portfolio and job reference purposes.
Please do not copy, reuse, or distribute any part of this work without explicit permission.
