# SCG & GCG - Heart Diseases

## Overview

This project focuses on analyzing accelerometer signals to study different heart-related activities using SCG (Seismocardiogram) and GCG (Gyrocardiogram) data. The goal is to preprocess, analyze, and classify these signals to gain insights into various physiological states such as normal breathing, deep breathing, and speaking while breathing.

## Key Features

### 1. **Data Loading and Visualization**
- Extracted file paths from the directory structure and associated them with corresponding labels.
- Loaded the data into a DataFrame, where each row represents a file and its respective label.
- Plotted time-domain signals for `accX`, `accY`, and `accZ`.
![image](https://github.com/user-attachments/assets/730a853e-5ea9-41e5-b7eb-b2253facda92)

### 2. **Frequency Domain Analysis**
- Applied Discrete Fourier Transform (DFT) to convert time-domain signals into the frequency domain.
- Calculated the frequency spectrum using FFT and filtered frequencies between 0.5 Hz and 20 Hz.
- Plotted magnitude spectra to analyze dominant frequency components.
![image](https://github.com/user-attachments/assets/44b37443-fc6e-4e28-a49f-af605266c290)

### 3. **Signal Filtering**
- Designed a band-pass filter using a Butterworth filter for accelerometer data.
- Applied the filter to the data, significantly improving signal clarity compared to raw input.
![image](https://github.com/user-attachments/assets/7baec7dc-8cad-432c-9226-21b8fdd85ed2)

### 4. **Feature Extraction**
- Extracted time-domain and frequency-domain features, including:
  - Absolute Energy
  - RMS Value
  - Median Value
  - Standard Deviation
  - Kurtosis
  - Skewness
  - Spectral Entropy
  - Power Band
- Organized these features into a DataFrame for advanced analysis.

### 5. **Dimensionality Reduction**
- Performed Principal Component Analysis (PCA) to simplify the data while preserving its essential features.
- Visualized the data in 2D space to distinguish between activities such as normal breathing, deep breathing, and speaking while breathing.
![image](https://github.com/user-attachments/assets/1a4e5c30-7b91-402f-95d9-6c63e4d4a0f5)

### 6. **Data Standardization**
- Rescaled the features to have a mean of 0 and standard deviation of 1.
- Improved performance and convergence of machine learning models.

### 7. **Classification Models**
#### **k-Nearest Neighbors (KNN) Classifier**
- Implemented KNN with leave-one-out cross-validation (LOOCV) to estimate model performance.
![image](https://github.com/user-attachments/assets/df60d5fd-ac6d-4473-9518-105527f9ca2c)

#### **Random Forest Classifier**
- Built a robust classifier with high accuracy and efficient performance.
![image](https://github.com/user-attachments/assets/c87eaa5a-af76-479a-bffc-855920acac45)

## Conclusion
- The models successfully distinguished between various physiological states.
- PCA visualization revealed clear separations among labels, particularly for unique activities like speaking while breathing.

## Technologies and Tools
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- SciPy
- Scikit-learn
