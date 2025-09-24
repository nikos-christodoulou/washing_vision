# 👕 Washing Vision - Keep your clothes safe and clean!

A deep learning project for **binary color classification** using **Convolutional Neural Networks (CNNs)**.  

This project was carried out as part of the HCI course in AUEB for the spring semester of 2023. The idea was to create 
a washing machine that would warn the user if colored and white clothes have been mixed in laundry, in order to 
retain the color of all clothing intact.

The model predicts whether a clothing item is **white** or **colored** with an accuracy of ~85% on test data.  




## 📂 Dataset  

Used the **Digikala Products Dataset**, which originally had **6,239 clothing images** categorized into **12 color classes**.  

### Preprocessing Steps  
- ✅ Removed mislabeled & irrelevant items (e.g., sunglasses, chains).  
- ✅ Reorganized into **2 categories**:  
  - `white`  
  - `colored`  
- ✅ Resized images to **224 × 224 × 3 (RGB)**.  
- ✅ Normalized pixel values to range `[0, 1]`.  
- ✅ Split into training (80%) and testing (20%).  

📌 Final dataset size: **5,929 images**  

---

## 🛠️ Methodology  

### 🔹 Model Architecture  
The CNN architecture includes:  
- **5 Convolutional layers** (ReLU activation)  
  - MaxPooling + BatchNormalization between convolutional layers  
- **3 Dense layers** (with Dropout for regularization)  
- **1 Output layer** with **Sigmoid activation** (binary classification)  

### 🔹 Training Setup  
- **Epochs:** 100  
- **Loss function:** Binary Cross-Entropy  
- **Optimizer:** (e.g., Adam — update if different)  

---

## 📊 Results  

- **Training Loss:** 0.032  
- **Training Accuracy:** 98.8%  
- **Test Accuracy:** ~85%  

### ⚠️ Observations  
- Strong overall performance.  
- Model struggles with **very light-colored clothing** (e.g., light gray or multicolored clothes with some white).  


---
