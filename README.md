# COVID-19 and Pneumonia Chest X-Ray Classifier

A deep learning computer vision project that classifies chest X-ray images into three categories:

- COVID-19
- Pneumonia
- Normal

This project uses TensorFlow and Keras to build, train, and evaluate image classification models. A baseline neural network was developed and compared against a Convolutional Neural Network (CNN) to determine the most effective architecture for medical image classification.

---

## Project Overview

Medical image classification is an important real-world application of deep learning that can assist healthcare professionals by identifying disease patterns from diagnostic images.

Using chest X-ray images, this project aims to classify patients into one of three categories:

- COVID-19
- Pneumonia
- Normal

The project explores:

- Image preprocessing
- Neural network development
- Convolutional neural networks
- Model evaluation
- Performance visualization

---

## Dataset Summary

### Training Dataset

| Class | Images |
|---------|---------:|
| Covid | 111 |
| Normal | 70 |
| Pneumonia | 70 |

**Total Training Images:** 251

### Testing Dataset

**Total Testing Images:** 66

The dataset is used for a multi-class image classification task.

> Note: The dataset is intentionally excluded from source control via `.gitignore` to keep the repository lightweight and to respect dataset licensing restrictions.

---

## Project Structure

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
│   ├── training_history.png
│   └── confusion_matrix.png
│
├── requirements.txt
├── README.md
├── LICENSE
├── .gitignore
└── model.keras

---

## Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Scikit-learn
- Matplotlib
- Jupyter Notebook
- VS Code
- Git & GitHub

---

## Models Developed

### Baseline Neural Network

Architecture:

Input Image
↓
Flatten
↓
Dense(128, ReLU)
↓
Dense(3, Softmax)

Results:

| Metric | Value |
|---------|---------:|
| Test Accuracy | 84.85% |
| Test Loss | 1.8944 |

Observations:

- Achieved strong accuracy for a simple architecture
- Contained over 19 million trainable parameters
- Showed signs of overfitting
- Served as a benchmark for comparison against the CNN

---

### Convolutional Neural Network (CNN)

Architecture:

Input
↓
Conv2D (32 Filters)
↓
MaxPooling2D
↓
Conv2D (64 Filters)
↓
MaxPooling2D
↓
Flatten
↓
Dense(128)
↓
Dropout(30%)
↓
Softmax Output (3 Classes)

Results:

| Metric | Value |
|---------|---------:|
| Test Accuracy | 90.91% |
| Test Loss | 0.1598 |

Improvement over Baseline:

Accuracy Improvement: +6.06%

The CNN significantly improved performance by learning spatial image features directly from the chest X-ray images.

---

## Results Summary

| Model | Test Accuracy |
|---------|---------:|
| Baseline Neural Network | 84.85% |
| Convolutional Neural Network | 90.91% |

### Key Findings

- CNN improved accuracy by 6.06%
- CNN reduced test loss from 1.8944 to 0.1598
- COVID images were classified perfectly
- Pneumonia images were classified perfectly
- Most errors occurred between Normal and Pneumonia images
- CNN demonstrated significantly better generalization than the baseline model

---

## Training Performance

### CNN Training Curves

[Training History](images/training_history.png)

### Training Analysis

The CNN showed strong learning performance throughout training.

- Training accuracy increased steadily toward 100%
- Validation accuracy remained above 90%
- Validation loss remained low and stable
- The model demonstrated strong generalization performance

Although a small amount of overfitting appeared near the end of training, validation performance remained strong.

---

## Confusion Matrix

### CNN Confusion Matrix

[Confusion Matrix](images/confusion_matrix.png)

### Classification Report

| Class | Precision | Recall | F1-Score |
|---------|---------:|---------:|---------:|
| Covid | 1.00 | 1.00 | 1.00 |
| Normal | 1.00 | 0.85 | 0.92 |
| Pneumonia | 0.87 | 1.00 | 0.93 |

### Confusion Matrix Analysis

The CNN correctly classified:

- 26 out of 26 COVID images
- 20 out of 20 Pneumonia images

The only classification errors occurred when several Normal images were predicted as Pneumonia.

This suggests the model was highly effective at identifying disease-related image features while occasionally interpreting healthy lungs as showing signs of Pneumonia.

---

## Lessons Learned

This project reinforced several important machine learning concepts:

- Image data requires specialized architectures
- CNNs outperform traditional dense neural networks for image classification
- Model evaluation requires more than accuracy alone
- Confusion matrices and classification reports provide deeper insight into model performance
- Training and validation curves can reveal overfitting and generalization behavior

---

## Future Improvements

Potential future enhancements include:

- Replace `Flatten()` with `GlobalAveragePooling2D()`
- Data augmentation
- Additional convolutional layers
- Transfer learning using pre-trained models
- Hyperparameter tuning
- Early stopping optimization
- Grad-CAM model explainability
- Model deployment as a web application

---

## Environment Setup

Create and activate a virtual environment:

**powershell**
py -3.14 -m venv .venv

.\.venv\Scripts\Activate.ps1

Install dependencies:

**powershell**
python -m pip install -r requirements.txt

Open the notebook:

**powershell**
jupyter notebook

or open the notebook directly in VS Code and select the project `.venv` interpreter.

---

## License

This project is licensed under the MIT License.

The license applies to the source code only.

Any datasets used remain subject to their original licensing terms and conditions.
