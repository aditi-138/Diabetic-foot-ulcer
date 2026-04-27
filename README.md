# Optimised Hybrid Deep Learning Frameworks for DFU Segmentation

## 📌 Description
This project focuses on **Diabetic Foot Ulcer (DFU) segmentation** using advanced hybrid deep learning models. The goal is to accurately detect ulcer regions in clinical images to assist in diagnosis and treatment planning.

Two optimized hybrid architectures are implemented:
- **LEViT–UNet++**
- **Swin Transformer–Lightweight UNet++**

These models combine:
- **CNNs** for local feature extraction  
- **Transformers** for global context understanding  

This hybrid approach improves segmentation accuracy while maintaining computational efficiency.

---

## 📊 Dataset Information
- **Dataset:** DFUC2022 (Diabetic Foot Ulcer Challenge Dataset)
- **Total Images:** ~2000+
- **Data Type:**
  - Clinical foot images  
  - Pixel-level segmentation masks  

### 🔹 Data Split
- Training: 80%
- Testing: 20%

### 🔹 Preprocessing
- Resize images to **128 × 128**
- Normalize pixel values to **[0,1]**
- Data augmentation:
  - Horizontal & vertical flip  
  - Rotation  
  - Affine transformations  
  - Brightness & contrast adjustment  

---

## 💻 Code Information

### 🔹 LEViT–UNet++ Model
- CNN encoder + attention mechanism  
- Lightweight architecture  
- Efficient segmentation performance  

### 🔹 Swin Transformer–UNet++ Model
- Patch embedding  
- Hierarchical transformer blocks  
- Lightweight UNet++ decoder  

---

## ⚙️ Usage Instructions

### 1️⃣ Clone the Repository
```bash
git clone <your-repo-link>
cd project-folder
```
### 2️⃣ Install Dependencies
```bash
pip install -r requirements.txt
```
### 3️⃣ Dataset Structure
dataset/
 └── dfu train/
      └── DFUC2022_train_release/
           ├── DFUC2022_train_images/
           └── DFUC2022_train_masks/
### 4️⃣ Run Training
### ▶️ LEViT Model
python lecit_unet.py
### ▶️ Swin Transformer Model
python swin_unetpp.py
### 📈 Output
Saved Models:
lecit_unet_final.pth
swin_unetpp_final.pth
### 🧰 Requirements
🔹 Language
Python 3.8+
🔹 Libraries
torch
numpy
opencv-python
albumentations
scikit-learn
tqdm
### 🧠 Methodology
1. Data Processing
Image resizing and normalization
Data augmentation for training
2. Model Design
Hybrid CNN + Transformer architectures
Multi-scale feature extraction
Skip connections for spatial accuracy
3. Optimization
Optuna (TPE algorithm)
Hyperparameter tuning:
Learning rate
Batch size
Attention heads
4. Loss Function
Binary Cross Entropy (BCE)
Dice Loss
5. Evaluation Metrics
Accuracy
Precision
Recall
Dice Coefficient
IoU
mAP@50
### 📊 Results Summary
<img width="1157" height="162" alt="image" src="https://github.com/user-attachments/assets/907d39bd-3dbb-4fc2-b89c-0bc690a09961" />

### ⚡ Performance Analysis
Model	Training Time	Inference Time
LEViT–UNet++	~41 mins	10 ms/image
Swin-LW UNet++	~46 mins	15 ms/image
### 🚀 Future Work
Improve Swin model efficiency
Train on larger datasets
Real-time deployment
Clinical integration
