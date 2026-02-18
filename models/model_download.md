# Pretrained Model Download

## Model Name
Portrait-to-Sketch Translation GAN (100 Epoch Trained)

Kaggle Model Link:  
https://www.kaggle.com/models/mahiruddin/portrait-to-sketch-translation-gan-model-100-epoch

---

## Available Models

The following trained models (after 100 epochs) are available:

- Generator Model
- Discriminator Model
- Combined GAN Model

These were trained using:
- Pix2Pix architecture
- U-Net Generator
- PatchGAN Discriminator
- Batch Size: 1
- Image Resolution: 256 × 256
- Total Training Epochs: 100

---

## How to Download

1. Visit the Kaggle model page.
2. Download the required model files.
3. Place them inside:

```
models/
```

Example structure:

```
models/
├── generator_100_epoch.h5
├── discriminator_100_epoch.h5
└── gan_100_epoch.h5
```

---

## Recommended Usage (Inference Only)

For deployment or inference, only the **Generator model** is required.

The discriminator and combined GAN model are only needed if:
- Continuing training
- Fine-tuning the model
- Further adversarial experimentation

---

## Loading the Generator (Example)

```python
from tensorflow.keras.models import load_model

generator = load_model("models/generator_100_epoch.h5", compile=False)
```

---

## Notes

- Ensure TensorFlow version compatibility with the training environment.
- If training is to be resumed, load generator and discriminator weights before rebuilding the combined GAN model.

---

