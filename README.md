# Impact of Label Noise on Logistic Regression vs Perceptron

Analysing how increasing label noise affects two classic machine learning models: **Logistic Regression** and **Perceptron**.  
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

### Original and Noisy Dataset
<img width=45% height="455" alt="image" src="https://github.com/user-attachments/assets/530ff420-61cd-4586-974d-6bfcf1fced07" />

<img width=45% height="455" alt="Original and Noisy Data" src="https://github.com/user-attachments/assets/4dde0e5b-67b0-4f4f-b375-0f0b364a27a7" />

### Training vs Test Split
<img width=45% height="455" alt="Train Test Split" src="https://github.com/user-attachments/assets/ebd2bc05-d27a-460c-8b0e-f3cbce7e1351" />
<img width=45% height="455" alt="image" src="https://github.com/user-attachments/assets/52267e5e-29cb-4dc7-a455-c7d40f88b398" />


### Accuracy at 0–5% Noise and Accuracy at 0–10% Noise
<img width=45% height="455" alt="Accuracy 0–0.05 Noise" src="https://github.com/user-attachments/assets/75360c41-4b9f-4a74-b3ba-9756da45837b" />


<img width=45% height="455" alt="Accuracy 0–0.10 Noise" src="https://github.com/user-attachments/assets/e561a674-4b71-4d34-b37b-ebec58b787f0" />

---
#Key findings


1.   Plots show that LR degrades smoothly; Perceptron drops faster and is more volatile—LR is more robust to noisy labels. (Your observation, kept.) 
2.   Mechanism: LR’s probabilistic loss tolerates mislabeled points better than a hard-boundary Perceptron. (Your point, tightened.)
3.   Around ~50% noise, accuracy should approach ~0.5 (random). If the 0–100% plot shows an uptick beyond 50%, that’s likely variance / evaluating against the same noisy labels in CV—do not claim real generalization. On a clean test set, accuracy would not increase past 50%.
4.   Practical: prefer logistic (probabilistic) training under noisy supervision; add data cleaning/robust loss if noise is high.

---
## How to Run
You can run this project entirely in **Google Colab**:

1. Click the badge below to open in Colab.  
2. Save a copy to your Drive (**File → Save a copy in Drive**).  
3. Run all cells in order; dependencies are pre-installed (`scikit-learn`, `numpy`, `matplotlib`).  

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/nipun-taneja/label-noise-logreg-perceptron.ipynb/blob/main/label_noise_logreg_perceptron.ipynb)

---

## ✍️ Author
Nipun Taneja – MS Artificial Intelligence @ SFSU
