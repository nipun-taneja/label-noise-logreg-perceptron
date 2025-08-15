# Impact of Label Noise on Logistic Regression vs Perceptron

This project studies how increasing label noise affects two classic machine learning models: **Logistic Regression** and **Perceptron**.  
Using a synthetic binary dataset, labels are randomly flipped to simulate noise, and model accuracy is evaluated under different noise levels.

---

## Goal
Quantify how label noise impacts model performance, using 10-fold cross-validation and visualization of accuracy degradation.

## 📝 Methodology
1. Generate synthetic dataset (`sklearn.make_blobs`)  
2. Add controlled label noise (0% → 100%)  
3. Train/test split  
4. Train Logistic Regression & Perceptron  
5. Evaluate via 10-fold cross-validation  
6. Plot accuracy vs noise levels  

---

## Results

### Original vs Noisy Dataset
<img width="562" height="455" alt="Original and Noisy Data" src="https://github.com/user-attachments/assets/4dde0e5b-67b0-4f4f-b375-0f0b364a27a7" />

### Training vs Test Split
<img width="562" height="455" alt="Train Test Split" src="https://github.com/user-attachments/assets/ebd2bc05-d27a-460c-8b0e-f3cbce7e1351" />

### Accuracy at 0–5% Noise
<img width="567" height="455" alt="Accuracy 0–0.05 Noise" src="https://github.com/user-attachments/assets/75360c41-4b9f-4a74-b3ba-9756da45837b" />

### Accuracy at 0–10% Noise
<img width="569" height="455" alt="Accuracy 0–0.10 Noise" src="https://github.com/user-attachments/assets/e561a674-4b71-4d34-b37b-ebec58b787f0" />

---

## How to Run
You can run this project entirely in **Google Colab**:

1. Click the badge below to open in Colab.  
2. Save a copy to your Drive (**File → Save a copy in Drive**).  
3. Run all cells in order; dependencies are pre-installed (`scikit-learn`, `numpy`, `matplotlib`).  

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/<nipun-taneja>/<repo-name>/blob/main/label_noise_logreg_perceptron.ipynb)

---

## ✍️ Author
Nipun Taneja – MS Artificial Intelligence @ SFSU
