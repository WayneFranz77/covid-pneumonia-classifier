# COVID-19 and Pneumonia Chest X-Ray Classifier

A deep learning computer vision project that classifies chest X-ray images into three categories:

- COVID-19
- Pneumonia
- Normal

This project uses TensorFlow and Keras to develop, train, and evaluate image classification models capable of identifying lung conditions from chest X-ray images. The project forms part of a machine learning and deep learning portfolio focused on real-world healthcare applications.

---

## Project Overview

Medical image classification is a challenging and impactful application of deep learning. Using a dataset of chest X-ray scans, this project aims to build a multi-class classification model that can distinguish between:

- COVID-19
- Pneumonia
- Healthy lungs

The project explores image preprocessing, neural network design, model evaluation, and performance optimization using TensorFlow.

---

## Project Objectives

- Build a deep learning image classifier using TensorFlow and Keras
- Preprocess and normalize medical image data
- Train and evaluate convolutional neural networks (CNNs)
- Monitor model performance using training and validation metrics
- Visualize loss and accuracy during training
- Evaluate predictions using confusion matrices and classification reports
- Develop a professional machine learning project workflow suitable for a portfolio

---

## Project Structure

```text
covid-pneumonia-classifier/
│
├── data/
│   ├── train/
│   └── test/
│
├── notebooks/
│   └── covid_pneumonia_classifier.ipynb
│
├── images/
│
├── requirements.txt
├── README.md
├── LICENSE
└── .gitignore
```

---

## Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Matplotlib
- Scikit-learn
- Jupyter Notebook
- VS Code
- Git & GitHub

---

## Machine Learning Workflow

### 1. Data Preparation

- Load chest X-ray images
- Resize images to a consistent shape
- Normalize pixel values
- Create training and testing datasets

### 2. Model Development

- Build a baseline neural network
- Implement Convolutional Neural Networks (CNNs)
- Experiment with hyperparameters
- Apply regularization techniques to reduce overfitting

### 3. Model Evaluation

Evaluate performance using:

- Accuracy
- Loss
- Confusion Matrix
- Classification Report
- Training and Validation Curves

### 4. Model Improvement

Potential enhancements include:

- Data augmentation
- Additional convolutional layers
- Transfer learning
- Hyperparameter tuning
- Early stopping

---

## Results

Results will be added as the project progresses.

Planned outputs include:

- Training accuracy and loss charts
- Confusion matrix
- Classification report
- Final model performance metrics
- Sample predictions

---

## Dataset

The dataset consists of chest X-ray images categorized into:

- COVID
- Pneumonia
- Normal

To keep this repository lightweight and suitable for GitHub, the image dataset is not tracked by Git and should be obtained separately from its original source.

Dataset source:

- Kaggle COVID-19 Radiography Dataset

---

## Environment Setup

Create and activate a virtual environment:

```powershell
py -3.14 -m venv .venv

.\.venv\Scripts\Activate.ps1
```

Install dependencies:

```powershell
python -m pip install --upgrade pip

python -m pip install -r requirements.txt
```

Launch Jupyter:

```powershell
jupyter notebook
```

or open the notebook directly in VS Code and select the project's `.venv` interpreter.

---

## Future Improvements

- Transfer learning with pre-trained CNN architectures
- Model explainability using Grad-CAM
- Performance comparison between multiple architectures
- Deployment as a web application
- Automated prediction pipeline

---

## License

This project is licensed under the MIT License.

The license applies only to the source code contained in this repository.

Any datasets used remain subject to their original licensing terms and conditions.
