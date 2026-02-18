# ==============================
# data/dataset_info.md
# ==============================

# Dataset Information

## Dataset Name
**FS2K: Paired Portrait ↔ Sketch Dataset**

Kaggle Dataset Link:  
https://www.kaggle.com/datasets/mahiruddin/paired-portrait-to-sketch-dataset

---

## Overview

FS2K is a high-quality paired face photo-to-sketch dataset designed for image-to-image translation tasks such as Pix2Pix GAN training.

It contains **2,104 aligned image pairs** of real face photographs and corresponding hand-drawn sketches.

Each image is:
- Resolution: **256 × 256**
- Channels: **3 (RGB)**
- Paired and aligned for supervised GAN training

This dataset is suitable for:
- Pix2Pix
- Conditional GANs
- Image-to-image translation
- Style transfer
- Sketch synthesis research

---

## Dataset Structure

```
FS2K/
├── photo/
│   ├── photo1/  (1,529 images – source: CASIA-WebFace)
│   ├── photo2/  (98 images – invited actors)
│   └── photo3/  (477 images – Unsplash, Pexels, Google, etc.)
│
├── sketch/
│   ├── sketch1/
│   ├── sketch2/
│   └── sketch3/
│
├── anno_train.json
└── anno_test.json
```

---

## Data Characteristics

- Photos collected under varied:
  - Lighting conditions
  - Backgrounds
  - Facial expressions
  - Age groups

- Sketches:
  - Drawn by professional artists
  - Three distinct artistic styles
  - Style diversity improves GAN generalization

- Some identities correspond to celebrity images.

---

## How to Use in This Project

1. Download dataset from Kaggle.
2. Extract the `FS2K` folder.
3. Place it inside:

```
data/FS2K/
```

4. Update the dataset path inside the training notebook if needed.

---

## Citation / Credits

Original dataset authors and sources are credited through the Kaggle dataset page and associated research publication.

If you use this dataset for academic or research purposes, please cite the original authors accordingly.

---
