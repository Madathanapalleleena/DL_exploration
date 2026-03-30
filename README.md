#  Brain Tumor Detection using Deep Learning

##  Project Overview

This project explores the application of **Deep Learning techniques** for detecting brain tumors from medical images. Multiple models and optimization strategies were implemented and compared to understand their performance on a real-world dataset.

The study includes:

* Multilayer Perceptron (MLP)
* Convolutional Neural Networks (CNN)
* Gradient Descent Optimization Techniques
* Regularization Methods
* Hyperparameter Tuning

---

## Dataset Description

The dataset used is a **Brain Tumor MRI Image Dataset**, organized into two classes:

* **Yes** → Images containing brain tumors
* **No** → Images without tumors

### 📊 Dataset Features:

* Image Type: MRI scans
* Format: RGB images
* Size: Variable (resized during preprocessing)
* Classes: Binary classification (Tumor / No Tumor)

---

## ⚙️ Preprocessing Steps

To prepare the dataset for training:

* Resized all images to **64×64 / 128×128**
* Normalized pixel values using:

  * Mean = `[0.5, 0.5, 0.5]`
  * Std = `[0.5, 0.5, 0.5]`
* Split dataset:

  * **70% Training**
  * **30% Testing**
* Applied optional **data augmentation**:

  * Random rotation
  * Horizontal flipping

---

## Models Implemented

### 1. Multilayer Perceptron (MLP)

* Fully connected neural network
* Input: Flattened image pixels
* Used for:

  * Studying optimization techniques
  * Testing regularization methods

---

### 2. Convolutional Neural Network (CNN)

* Extracts spatial features from images
* Layers used:

  * Convolutional layers
  * ReLU activation
  * MaxPooling
  * Fully connected layers
* Achieves significantly better performance than MLP

---

## Optimization Techniques Explored

The following Gradient Descent variants were implemented:

* Batch Gradient Descent (BGD)
* Stochastic Gradient Descent (SGD)
* Mini-Batch Gradient Descent
* SGD with Momentum
* Nesterov Accelerated Gradient
* Adagrad
* RMSProp
* Adadelta
* Adam

### Key Observation:

* **Adam optimizer performed best** due to adaptive learning rate and faster convergence.

---

## Regularization Techniques Used

To reduce overfitting and improve generalization:

* L2 Regularization (Weight Decay)
* Dropout
* Data Augmentation
* Noise Injection
* Early Stopping
* Ensemble Learning
* Parameter Sharing

### Key Observation:

* **Ensemble + Dropout + Data Augmentation** gave the best results.

---

## 🔬 Hyperparameter Tuning (CNN)

Parameters tuned:

* Learning Rate
* Batch Size
* Dropout Rate

### 🏆 Best Configuration:

* Learning Rate: `0.0005`
* Batch Size: `16`
* Dropout: `0.3`

---

## 📈 Results Summary

| Model               | Performance                              |
| ------------------- | ---------------------------------------- |
| MLP                 | Moderate accuracy, slower learning       |
| CNN                 | High accuracy, better feature extraction |
| Best Optimizer      | Adam                                     |
| Best Regularization | Ensemble + Dropout                       |

---

## Key Learnings

* CNN significantly outperforms MLP for image data
* Proper preprocessing is crucial
* Optimization techniques affect convergence speed
* Regularization prevents overfitting
* Hyperparameter tuning improves model performance

---

## Future Improvements

* Use **Transfer Learning (ResNet, VGG16)**
* Increase dataset size
* Apply **cross-validation**
* Deploy model as a web application
* Use explainable AI (Grad-CAM)

---

## Technologies Used

* Python
* PyTorch
* NumPy
* Matplotlib
* Google Colab

---

## Conclusion

This project demonstrates how different deep learning techniques can be applied and compared on a medical imaging dataset. The results highlight the importance of choosing the right model, optimizer, and regularization strategies for achieving optimal performance.

