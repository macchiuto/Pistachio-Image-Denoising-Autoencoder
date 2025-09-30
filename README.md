# Pistachio Image Denoising: Autoencoder DL Project

![Python](https://img.shields.io/badge/language-Python-blue)
![Jupyter Notebook](https://img.shields.io/badge/output-Jupyter%20Notebook-orange)

## Overview

This repository contains an **image denoising project** using autoencoders applied to pistachio images. 
It was developed as a **final project for the Deep Learning course** and demonstrates the performance comparison between a baseline autoencoder and a modified version for noise removal.

---

## Repository Structure

- `B_2.zip` → folder containing raw pistachio images
- `pistachio_image_denoising.ipynb` → main notebook with EDA, preprocessing, model training, evaluation, and visualization

---

## Methodology
1. **Exploratory Data Analysis**
   - Checked image count, formats, dimensions, aspect ratios
   - Verified integrity (corrupt images)
   - Visualized sample images
2. **Data Preprocessing**
   - Split images into train (80%), validation (10%), test (10%)
   - Resized to 100x100 pixels, normalized
   - Added Gaussian noise to generate noisy inputs
3. **Autoencoder Modeling**
   - **Baseline Autoencoder:** Standard Conv2D + MaxPooling2D encoder, UpSampling2D decoder
   - **Modified Autoencoder:** Added Conv2D layer in decoder to enhance feature reconstruction
   - Trained for 25 epochs with batch size 32; EarlyStopping used for modified model
4. **Evaluation**
   - Assessed denoising quality using SSIM (Structural Similarity Index)
   - Modified model improved SSIM from 0.952 → 0.956
   - Visual comparison of noisy, ground truth, and denoised images

---

## Key Insights

- Modified autoencoder converges faster and generalizes better than baseline
- Additional Conv2D layer improves spatial feature reconstruction in decoder
- Loss curves show small gap between train and validation → minimal overfitting
- Visual results confirm noise removal with good preservation of image details

---

## Presentation Video
[Image Denoising Autoencoder – Video Presentation](https://drive.google.com/file/d/1khA1ft2UQ1kjxqMt38l0fgER6RzlZz78/view?usp=sharing)

---

## References
- Python libraries: numpy, pandas, matplotlib, seaborn, scikit-image, tensorflow, keras, pillow
- Concepts: Convolutional Autoencoder, Image Denoising, Gaussian Noise, SSIM

---

## Author

Syalista Galuh Nadira
