🫀 ECG Signal Classification with ML Models
This project demonstrates how to classify ECG (electrocardiogram) signals using machine learning models. It utilizes the MIT-BIH Arrhythmia Dataset, which contains thousands of heartbeat samples. The pipeline includes signal visualization, feature extraction, model training, and performance evaluation using multiple metrics including ROC curves.

📦 Dataset
The dataset used in this project is downloaded via KaggleHub and includes:

-mitbih_train.csv
-mitbih_test.csv

Each row in the dataset represents a heartbeat signal (187 data points) followed by a label (class).

⚙️ Workflow
1) Download and Load Dataset
Uses kagglehub to download and load ECG signals into pandas DataFrames.

2) Data Visualization
Plots a sample ECG signal and detects R-peaks using scipy.signal.find_peaks.

3) Feature Extraction
For each signal, 4 key features are extracted:

-Root Mean Square (RMS)
-Mean
-Standard Deviation
-Number of R-peaks

4)Preprocessing

-The feature matrix is scaled using StandardScaler.
-Labels are binarized for multi-class ROC analysis.

5)Model Training and Evaluation
Trains and evaluates the following models:

-Logistic Regression
-Support Vector Machine (SVM)
-Decision Tree
-Random Forest
-Multi-Layer Perceptron (MLP)

For each model:
-Accuracy and classification report are printed.
-Confusion matrix is visualized with seaborn heatmaps.
-ROC curves are plotted for each class (if supported by the model).

📊 Output
-Confusion matrices for all models
-ROC curves per class
-Performance comparison across five classifiers

🛠️ Requirements
pip install pandas numpy matplotlib seaborn scikit-learn scipy kagglehub

📁 Project Structure
.
├── ecg_classifier.py       # Main script
└── README.md               # Project explanation

🚀 Future Work
Use deep learning models (e.g., CNNs) for raw signal classification

Explore time-series specific features (e.g., wavelet transforms)

Real-time classification in a medical application
