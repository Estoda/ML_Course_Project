# 🔢 OCR for Handwritten Digit Recognition

A Machine Learning project that recognizes handwritten digits (0–9) using multiple classification algorithms and compares their performance through hyperparameter tuning and cross-validation.

---

# 📌 Project Overview

This project implements an Optical Character Recognition (OCR) system capable of classifying handwritten digits from the **DIDA Dataset**.

Instead of relying on a single machine learning algorithm, the project evaluates several different classifiers, tunes their hyperparameters, and compares their performance to determine the most accurate model.

The complete workflow includes:

- Dataset loading
- Image preprocessing
- Feature normalization
- Train/Test splitting
- Hyperparameter tuning using Grid Search
- Cross Validation
- Model evaluation
- Performance comparison
- Final model selection

---

# 📂 Dataset

The project uses the **DIDA Handwritten Digits Dataset**.

Dataset structure:

```
DIDA/
│
├── 0/
│   ├── img1.png
│   ├── img2.png
│   └── ...
│
├── 1/
│   └── ...
│
...
│
└── 9/
```

Each folder contains images belonging to one digit.

Total dataset:

- 10 Classes (0 → 9)
- 1000 images per class
- Total Images: **10,000**

---

# 🖼 Image Preprocessing

Each image goes through several preprocessing steps:

- Read image using OpenCV
- Resize to **28 × 28**
- Convert into grayscale
- Flatten image into a vector of **784 features**
- Normalize pixel values

Normalization:

```
pixel = pixel / 255
```

This scales pixel values from:

```
0–255
```

to

```
0–1
```

which improves model convergence.

---

# 📊 Data Splitting

The dataset is divided into:

- **80% Training**
- **20% Testing**

Stratified splitting is used to preserve the same class distribution across both datasets.

---

# 🤖 Machine Learning Models

The following algorithms are implemented and compared:

## 1. Gaussian Naive Bayes

A probabilistic classifier based on Bayes' theorem.

Advantages:

- Very fast
- Low memory usage
- Strong baseline model

---

## 2. One-vs-All Linear Regression

Linear Regression adapted for multiclass classification using the One-vs-All strategy.

Each digit has its own binary classifier.

---

## 3. Logistic Regression

A supervised classification algorithm suitable for multiclass problems.

Advantages:

- High accuracy
- Efficient
- Good probabilistic interpretation

---

## 4. Multi-Layer Perceptron (MLP)

A feedforward Artificial Neural Network trained using backpropagation.

Capable of learning complex non-linear relationships.

---

# ⚙ Hyperparameter Tuning

To maximize performance, every model is optimized using:

- Grid Search
- Cross Validation

The notebook searches across different parameter combinations and automatically selects the best configuration.

---

# 🔁 Cross Validation

The project evaluates models using Cross Validation to reduce overfitting and produce a more reliable estimation of model performance.

Metrics collected include:

- Mean Accuracy
- Standard Deviation
- Best Parameters

---

# 📈 Model Evaluation

Each trained model is evaluated on the testing dataset.

Evaluation includes:

- Classification Accuracy
- Cross Validation Score
- Hyperparameter Comparison
- Runtime Measurement

---

# 📊 Performance Comparison

After training, all models are compared based on:

- Test Accuracy
- Cross Validation Accuracy
- Training Time
- Best Hyperparameters

The highest-performing model is selected as the final OCR classifier.

---

# 📦 Project Structure

```
OCR_Project/

│
├── OCR_ML_Project.ipynb
├── DIDA/
│   ├── 0/
│   ├── 1/
│   ├── ...
│   └── 9/
│
└── README.md
```

---

# 🛠 Technologies Used

- Python
- NumPy
- OpenCV
- Scikit-learn
- Pandas
- Matplotlib
- Pathlib

---

# 🚀 Workflow

```
Load Dataset
        │
        ▼
Read Images
        │
        ▼
Resize Images
        │
        ▼
Flatten Images
        │
        ▼
Normalize Data
        │
        ▼
Train/Test Split
        │
        ▼
Grid Search
        │
        ▼
Cross Validation
        │
        ▼
Train Models
        │
        ▼
Evaluate Models
        │
        ▼
Compare Performance
        │
        ▼
Select Best Model
```

---

# 📌 Features

- Multiple Machine Learning models
- Hyperparameter tuning
- Cross Validation
- Performance comparison
- Modular preprocessing pipeline
- Automatic best model selection
- Clean and reproducible implementation

---

# ▶️ How to Run

1. Clone the repository

```bash
git clone https://github.com/yourusername/OCR-Handwritten-Digits.git
```

2. Install dependencies

```bash
pip install numpy pandas matplotlib opencv-python scikit-learn
```

3. Place the **DIDA** dataset in the project directory.

4. Open the notebook:

```
OCR_ML_Project.ipynb
```

5. Run all cells.

---

# 📚 Learning Objectives

This project demonstrates:

- Image preprocessing
- Feature engineering
- Classical Machine Learning algorithms
- Hyperparameter optimization
- Cross Validation
- Model comparison
- OCR fundamentals

---

# 👨‍💻 Authors

**Ahmed Magdy Hassan**

Backend Developer | Django Developer

**Ahmed Abdulrahman Mohamed Amin**

ML Engineer

Faculty of Computers and Artificial Intelligence  
Fayoum University
