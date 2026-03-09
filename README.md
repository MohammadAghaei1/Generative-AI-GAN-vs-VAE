# 🔢 Generative Models for Handwritten Digit Synthesis (GAN vs VAE)

This project investigates the effectiveness of two popular generative models:

- **Variational Autoencoders (VAE)**
- **Generative Adversarial Networks (GAN)**

for generating handwritten digits using the **MNIST dataset**.

The goal is to compare these two generative approaches in terms of **image quality, diversity, and training stability**.

---

# 🎯 Research Question

Is it better to use **Generative Adversarial Networks (GANs)** or **Variational Autoencoders (VAEs)** for generating realistic handwritten digits?

---

# 📊 Dataset

The experiments were conducted on the **MNIST dataset**, a widely used benchmark for image generation tasks.

Dataset characteristics:

- **70,000 grayscale images**
- Resolution: **28 × 28 pixels**
- Digits: **0–9**
- Unconditional generation (no labels used during training)

---

# 🏗 Project Architecture

The system follows a standard **generative modeling pipeline**.

### ML Pipeline

1. **Dataset Preparation**
2. **Model Architecture Design**
3. **Model Training**
4. **Sample Generation**
5. **Evaluation & Comparison**

---

# 🧠 Model 1 — Variational Autoencoder (VAE)

A **Variational Autoencoder** is a probabilistic generative model that learns a compressed latent representation of data.

### VAE Architecture

The model consists of three main components:

**Encoder**

Maps input images into a latent probability distribution.

**Latent Space**

The learned representation of the data distribution.

**Decoder**

Reconstructs images from the latent representation.

### Key Characteristics

- stable training
- smooth latent space
- probabilistic generation

However, VAE often produces **slightly blurry images**.

---

# 🧠 Model 2 — Generative Adversarial Network (GAN)

GANs consist of two neural networks competing with each other.

### GAN Architecture

**Generator**

Generates synthetic digit images from random noise.

**Discriminator**

Attempts to distinguish between real and generated images.

During training:

- the generator learns to create realistic images
- the discriminator learns to detect fake samples

This adversarial process leads to **high-quality image generation**.

---

# ⚙️ Training Setup

Both models were trained under similar conditions to ensure fair comparison.

### Training Assumptions

Evaluation focused on three main aspects:

- **Visual realism**  
  digit clarity and stroke sharpness

- **Sample diversity**  
  ability to generate digits from 0–9

- **Training stability**  
  smooth loss behavior and absence of mode collapse

---

# 📈 Evaluation Metric

Model performance was evaluated using:

### Fréchet Inception Distance (FID)

FID measures the similarity between real images and generated images.

Lower FID values indicate **better image quality and distribution similarity**.

---

# 📊 Results

### VAE Results

Characteristics:

- stable training process
- smooth latent representations
- slightly blurred generated digits

### GAN Results

Characteristics:

- sharper generated images
- higher visual realism
- risk of **mode collapse** during training

---

# 🔎 Comparison

| Criterion | VAE | GAN |
|------|------|------|
| Image Quality | Medium | High |
| Training Stability | High | Medium |
| Diversity | Good | Very Good |
| Training Complexity | Low | Higher |

---

# 🧪 Key Observations

- **GAN produced sharper digits** with better visual quality.
- **VAE training was more stable** and easier to optimize.
- GAN required careful tuning to avoid **mode collapse**.

Overall, GAN demonstrated **better generative performance for MNIST digit synthesis**, while VAE provided more stable and interpretable training.

---
