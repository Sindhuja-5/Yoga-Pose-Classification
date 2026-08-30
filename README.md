# 🧘 Yoga Pose/Asana Image Classification

🎯 **Result:** 74.8% classification accuracy across 19 Yoga Asana classes using transfer learning with a pretrained Inception-v3 CNN.

A deep learning project for classifying images into **19 different Yoga Asana categories** using **PyTorch and transfer learning**.

## 🚀 Overview

The project uses a **pretrained Inception-v3 CNN** to extract visual features from yoga pose images and classify them into one of 19 Asana categories.

Instead of training the network from scratch, the pretrained ImageNet weights are leveraged and the final classification layer is replaced with a custom **19-class fully connected layer**.

## 🧠 Model Architecture

**Inception-v3 (Pretrained on ImageNet)**

```text
Input Image (299 × 299)
        ↓
Convolutional Layers
        ↓
Inception Modules
        ↓
Feature Extraction
        ↓
Global Average Pooling
        ↓
Fully Connected Layer
        ↓
19 Yoga Asana Classes
```

### Key Architecture Details

* **Base Model:** Inception-v3
* **Pretrained Weights:** ImageNet
* **Input Resolution:** 299 × 299
* **Output Classes:** 19
* **Final Layer:** Fully connected layer mapping Inception-v3 features to 19 classes
* **Loss Function:** Cross-Entropy Loss

## ⚙️ Training

| Parameter         | Configuration          |
| ----------------- | ---------------------- |
| Framework         | PyTorch                |
| Model             | Inception-v3           |
| Optimizer         | SGD                    |
| Learning Rate     | 0.1                    |
| Momentum          | 0.9                    |
| Weight Decay      | 4 × 10⁻⁵               |
| Batch Size        | 50                     |
| Loss              | Cross-Entropy          |
| Scheduler         | OneCycleLR             |
| Data Augmentation | Random Horizontal Flip |
| Input Size        | 299 × 299              |

Images are normalized using standard **ImageNet mean and standard deviation** values.

## 📊 Results

The trained model achieved:

**🎯 Accuracy: 74.8%**

| Metric                  |           Result |
| ----------------------- | ---------------: |
| Classification Accuracy |        **74.8%** |
| Number of Classes       |           **19** |
| CNN Architecture        | **Inception-v3** |

## 🛠️ Technologies

* **Python**
* **PyTorch**
* **Torchvision**
* **Pandas**
* **PIL**
* **scikit-image**

## 🔑 Key Highlights

* Implemented a **19-class image classification system** for Yoga Asanas.
* Applied **transfer learning** using ImageNet-pretrained Inception-v3.
* Implemented image preprocessing and augmentation using PyTorch/Torchvision.
* Used **SGD with momentum and OneCycleLR** for model optimization.
* Achieved **74.8% classification accuracy**.

## 📌 Future Improvements

* Increase the training dataset and apply stronger augmentation techniques.
* Fine-tune more layers of the pretrained Inception-v3 network.
* Experiment with architectures such as **ResNet, EfficientNet, and Vision Transformers (ViT)**.
* Use confusion matrices and per-class metrics to identify difficult Asana categories.
