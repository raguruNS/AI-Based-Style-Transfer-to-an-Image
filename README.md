# Assignment 6: Applying AI-Based Style Transfer to an Image

## 📌 Project Overview

This project demonstrates and compares two different AI-based image transformation techniques:

1. **CycleGAN**
2. **VGG-based Neural Style Transfer**

The same original image is processed using both approaches, and the resulting outputs are compared based on content preservation and style transformation.

---

## 🎯 Objective

The objective of this assignment is to understand how deep learning models can be used for image-to-image translation and artistic style transfer.

The experiment compares:

* Original Image
* CycleGAN Output
* Neural Style Transfer Output

---

## 🧠 Methods Used

### 1. CycleGAN

CycleGAN is a Generative Adversarial Network designed for **unpaired image-to-image translation**.

For this experiment, a pretrained **Horse-to-Zebra CycleGAN model** was used.

The model translates:

```text
Horse Image
     ↓
CycleGAN
     ↓
Zebra-style Image
```

CycleGAN does not require every horse image to have a corresponding paired zebra image.

### Cycle Consistency

An important concept in CycleGAN is **cycle consistency**.

The idea is:

```text
Domain A
  ↓
Domain B
  ↓
Domain A
```

For example:

```text
Horse
  ↓
Zebra
  ↓
Horse
```

The reconstructed horse image should remain similar to the original horse image.

This cycle-consistency constraint helps the model preserve important information during image translation.

---

### 2. Neural Style Transfer

Neural Style Transfer combines the **content of one image** with the **artistic style of another image**.

The experiment uses a pretrained neural style-transfer model based on convolutional neural network features.

The process is:

```text
Content Image + Style Image
            ↓
    Neural Style Transfer
            ↓
      Stylized Image
```

The original image provides the content and structure, while the painting provides visual characteristics such as colors, textures, and artistic patterns.

---

## 🛠️ Technologies Used

* Python
* Google Colab
* TensorFlow
* TensorFlow Hub
* PyTorch
* CycleGAN
* VGG-based Neural Style Transfer
* NumPy
* Matplotlib
* Pillow

---

## 📂 Project Structure

```text
Assignment-6/
│
├── README.md
│
├── original_image.jpg
│
├── cyclegan_output.jpg
│
├── neural_style_transfer_output.jpg
│
├── Assignment6_Final_Comparison.jpg
│
└── Assignment6.ipynb
```

---

## ⚙️ Requirements

Install the required Python libraries using:

```bash
pip install tensorflow
pip install tensorflow-hub
pip install torch
pip install torchvision
pip install matplotlib
pip install numpy
pip install pillow
```

The project can also be executed directly in **Google Colab**.

---

## 🚀 Implementation Steps

### Step 1: Upload Original Image

Upload the image that will be used as the content/input image.

For the CycleGAN experiment, a horse image is used because the pretrained model performs Horse-to-Zebra translation.

---

### Step 2: CycleGAN Processing

A pretrained Horse-to-Zebra CycleGAN model is loaded.

The input image is passed through the model to generate the translated image.

Output:

```text
Original Horse → CycleGAN → Zebra
```

The resulting image is saved as:

```text
cyclegan_output.jpg
```

---

### Step 3: Select Style Image

An artistic painting is selected as the style image.

For example:

```text
Van Gogh-style painting
```

The painting provides the artistic characteristics that will be transferred to the original image.

---

### Step 4: Neural Style Transfer

The content image and style image are passed to the pretrained neural style-transfer model.

```text
Content Image
      +
Style Image
      ↓
Neural Style Transfer
      ↓
Stylized Image
```

The resulting image is saved as:

```text
neural_style_transfer_output.jpg
```

---

### Step 5: Final Comparison

The three images are placed side by side:

```text
Original Image | CycleGAN Output | Neural Style Transfer Output
```

The final comparison is saved as:

```text
Assignment6_Final_Comparison.jpg
```

---

## 📊 Results

### Original Image

The original image provides the content and structure used for both transformations.

### CycleGAN Output

CycleGAN changes the visual domain of the original image. In this experiment, the horse image is transformed into a zebra-style image.

### Neural Style Transfer Output

Neural Style Transfer preserves the main content of the original image while applying the visual characteristics of the selected painting.

---

## 🔍 Comparison

| Feature              | CycleGAN                      | Neural Style Transfer             |
| -------------------- | ----------------------------- | --------------------------------- |
| Main purpose         | Image-to-image translation    | Artistic style transfer           |
| Input                | Image from a source domain    | Content + style image             |
| Content preservation | Preserves important structure | Strongly preserves content        |
| Style transformation | Domain-based transformation   | Artistic transformation           |
| Training concept     | GAN + cycle consistency       | CNN feature representations       |
| Example              | Horse → Zebra                 | Horse + Painting → Artistic Horse |

---

## 📝 Written Comparison

CycleGAN changes the original image from one visual domain to another while preserving important structural information. Neural Style Transfer preserves the content of the original image while applying the colors, textures, and artistic patterns of the selected painting. CycleGAN uses adversarial learning and cycle consistency, whereas Neural Style Transfer uses CNN-based feature representations to combine content and artistic style.

---

## 🔄 Cycle Consistency

Cycle consistency is a key concept in CycleGAN.

If an image is translated from domain A to domain B, it should be possible to translate the generated image back to domain A.

For example:

```text
Horse
  ↓
Horse → Zebra Generator
  ↓
Zebra
  ↓
Zebra → Horse Generator
  ↓
Reconstructed Horse
```

The reconstructed horse should be similar to the original horse.

This encourages CycleGAN to preserve important information while changing the visual domain.

---

## 📌 Conclusion

This assignment demonstrated two different approaches to AI-based image transformation. CycleGAN was used for image-to-image domain translation, specifically Horse-to-Zebra translation, while Neural Style Transfer was used to apply the visual characteristics of an artistic painting to the original image.

The experiment demonstrates that different deep learning methods can produce different types of image transformations while retaining important information from the original image.

---

## 👨‍💻 Author

**Nitheesh**

**Course:** Bachelor of Computer Applications (BCA)

**Assignment:** 6 – Applying AI-Based Style Transfer to an Image
