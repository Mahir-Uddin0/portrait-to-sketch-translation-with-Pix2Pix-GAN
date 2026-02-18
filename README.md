# 🎨 Portrait to Sketch Translation using Pix2Pix GAN

A deep learning project that converts portrait photographs into realistic sketch-style images using a **Pix2Pix Generative Adversarial Network (GAN)**.

This project implements supervised image-to-image translation using a U-Net generator and PatchGAN discriminator trained on paired portrait–sketch datasets (256×256 resolution).

---

## 📌 Overview

The objective of this project is to learn a mapping from **portrait photos → sketch images** using conditional adversarial training.

The trained model:
- Preserves facial structure and spatial alignment  
- Generates clean and coherent sketch strokes  
- Maintains identity consistency  
- Produces visually realistic outputs  

The final generator model is deployed using **Streamlit**, allowing users to:
- Upload their own portrait image  
- Select from predefined sample images  
- Generate sketch outputs interactively  

---

## 🧠 Model Architecture

### Generator (U-Net)
- Encoder–decoder convolutional architecture  
- Skip connections for spatial information retention  
- Input: 256×256×3  
- Output: 256×256×3  
- Activation: Tanh  

### Discriminator (70×70 PatchGAN)
- Classifies image patches as real or fake  
- Encourages high-frequency detail generation  
- Improves sharpness and texture quality  

### Loss Functions
- Adversarial Loss (Binary Crossentropy)  
- L1 Loss (Pixel-level reconstruction loss)  
- Combined objective as proposed in the original Pix2Pix paper  

---

## 📂 Dataset

Paired datasets used for supervised training:

- FS2K Dataset  
- CUHK Face Sketch Dataset  

Preprocessing:
- Resized to 256×256  
- Normalized to range [-1, 1]  
- Strictly paired alignment between portrait and sketch  

---

## 🚀 Training Details

- Image Resolution: 256×256  
- Batch Size: 1 (as recommended for Pix2Pix)  
- Epochs: 100  
- Optimizer: Adam (learning rate = 0.0002, beta1 = 0.5)  
- Framework: TensorFlow / Keras  
- Hardware: Kaggle GPU  

Total training iterations:

```
iterations = number_of_images × epochs
```

Example:

```
2104 images × 100 epochs = 210,400 iterations
```

---

## 🖥️ Streamlit Deployment

The trained generator model is deployed with Streamlit.

### Features
- Upload portrait image from local system  
- Choose sample images  
- Real-time sketch generation  
- Fast CPU inference  

---


## 📊 Results

The model successfully:
- Preserves facial geometry  
- Generates consistent sketch contours  
- Maintains identity across translation  
- Produces sharp edge structures  

(Add before/after sample images here for better presentation.)

---

## 🔄 Resume Training

Models are periodically saved during training.  
To resume training:

- Load generator, discriminator, and combined GAN models  
- Continue training from the saved checkpoint  

---

## 🧩 Future Improvements

- Multi-style sketch generation  
- Quantitative evaluation using FID / LPIPS  
- Lightweight deployment model  
- HuggingFace Spaces deployment  
- Mobile-optimized inference  

---

## 📚 Reference

Isola et al., *Image-to-Image Translation with Conditional Adversarial Networks (Pix2Pix)*, 2017.

---

