# Synthetic Fingerprint Generation with GAN

This project implements a deep learning pipeline to **classify and generate synthetic fingerprint images** for both **male and female subjects**, across **10 different fingers** (left/right × 5).  

The project has two main components:
1. **CNN Classifier** – Trains a convolutional neural network to classify fingerprints by finger type.
2. **Conditional GAN (cGAN)** – Generates realistic synthetic fingerprint images conditioned on **finger type** and **gender**.

## 📊 Dataset Description
The dataset consists of **grayscale fingerprint images** collected for **multiple subjects**, covering **all 10 fingers** for both **males and females**.

- **Format:** `.BMP` images  
- **Resolution:** ~112×112 pixels (resized during preprocessing)  
- **Naming Convention:**  
<PersonID>__<Gender><Hand><Finger>.BMP | Example: 2__F_Right_ring_finger.BMP
- `2` → Person ID  
- `F` → Gender (Male: `M`, Female: `F`)  
- `Right_ring_finger` → Hand and Finger type  
- **Classes (10 fingers):**
- Left hand: thumb, index, middle, ring, little  
- Right hand: thumb, index, middle, ring, little  
- **Balanced Categories:**  
Each gender has fingerprints for all 10 fingers, allowing conditional generation of male/female fingerprints per finger type.

[Dataset Citation] Kaggle Free Datasets

