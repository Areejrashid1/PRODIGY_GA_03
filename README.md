# 🖼️ Image-to-Image Translation using Pix2Pix

This project implements an **Image-to-Image Translation** model using **Pix2Pix GANs** in TensorFlow. The implementation is based on the U-Net generator and PatchGAN discriminator architecture for tasks such as converting **building facades → architectural labels** and vice versa.

---

## 📌 Features

* Loads the **Facades dataset** from Berkeley.
* Implements **data preprocessing** (resize, crop, normalization, random jitter).
* Defines a **U-Net Generator** for image generation.
* Defines a **PatchGAN Discriminator** for real/fake classification.
* Implements **Pix2Pix loss functions** (Generator loss + L1 loss, Discriminator loss).
* Supports **training with checkpoints**.
* Provides **visualizations**:

  * Input image
  * Ground Truth
  * Model prediction

---

## 📂 Project Structure

```
image_to_image_translation.py   # Main script (Pix2Pix implementation)
```

---

## ⚙️ Installation

Clone the repository and install the required dependencies:

```bash
git clone https://github.com/yourusername/image-to-image-translation.git
cd image-to-image-translation

pip install -r requirements.txt
```

### Requirements

* Python 3.8+
* TensorFlow 2.x
* Matplotlib
* IPython

---

## 🚀 Usage

Run the training script:

```bash
python image_to_image_translation.py
```

The script will:

1. Download the **facades dataset**.
2. Train the model for **40,000 steps**.
3. Save checkpoints in `training_checkpoints/`.
4. Generate translated images during training.

---

## 📊 Training Details

* **Batch Size:** 1
* **Image Size:** 256 × 256
* **Optimizer:** Adam (lr=2e-4, β1=0.5)
* **Loss:** Binary Cross-Entropy + L1 Loss
* **Checkpoints:** Saved every 5k steps

---

## 🖼️ Results

During training, the model generates side-by-side visualizations:

* Input Image
* Ground Truth
* Predicted Image

---


Pull requests are welcome. For significant changes, please open an issue first to discuss what you’d like to change.

