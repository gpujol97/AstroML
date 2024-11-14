# Automated Exoplanet Detection in Kepler Light Curves
This project is part of my Master's Thesis, titled "Detección Automatizada de Exoplanetas a partir de Flujos Lumínicos Estelares" (Automated Detection of Exoplanets from Stellar Light Fluxes). The goal is to develop an automated system for detecting potential exoplanet candidates from stellar light curves using data from the Kepler mission, applying signal processing and machine learning techniques.

## Project Structure
- Kepler Data: Uses Kepler mission light curve data, processed and made available through Kaggle's _exoTrain.csv_ and _exoTest.csv_ files.
- Machine Learning Models: Implemented multiple models, including feature-based, time-series-based, and hybrid methods to optimize exoplanet detection accuracy.
- Feature Engineering: Includes robust feature extraction such as Signal-to-Noise Ratio (SNR), Box Least Squares (BLS) period analysis, transit depth, duration, and periodicities in the light curves.

## Notebooks and Files
- _Global Project - Kepler Data Exoplanet Detection.ipynb_ : The main notebook with all steps from data preprocessing, feature extraction, model training, and evaluation.
- Data Preprocessing: Handles outlier removal, noise reduction using Savitzky-Golay and median filters, scaling, and class balancing with SMOTE.
- Feature Engineering: Calculates key features that are significant for exoplanet detection. Fourier and BLS analyses are performed to capture periodicity and transit features.
- Model Training & Evaluation: Implements three main approaches:
1. LightGBM on extracted features.
2. Convolutional Neural Network (CNN) on time-series data.
3. Hybrid model combining features with LSTM layers for temporal patterns.

## Key Results
Achieved high accuracy, with the hybrid model reaching 97% accuracy and 100% recall on a balanced dataset, highlighting robustness in detecting exoplanet signals.
On the imbalanced original dataset, the model maintained 100% recall for exoplanet detection.

## Project Dependencies 
- Python (>= 3.7)
- Key libraries: numpy, pandas, scipy, sklearn, tensorflow/keras, matplotlib

## Running the Notebook
1. Clone the repository and ensure all dependencies are installed.
2. Download _exoTrain.csv_ and _exoTest.csv_ from Kaggle’s Kepler dataset.
3. Run the cells sequentially for data import, preprocessing, feature extraction, and model training.

## Conclusion
This project presents a novel, hybrid approach that combines signal processing with machine learning for accurate exoplanet detection in light curves. The methodology is validated against existing research and offers strong generalization potential for large-scale astronomical datasets.
