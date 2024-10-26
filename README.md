# Potato Plant Disease Identification

## 1. Project Overview

This project focuses on using image recognition to identify diseases in potato plants. This dataset contains high-resolution images of potato plants exhibiting various diseases, including early blight, late blight, and healthy leaves. It is curated to aid in the development and testing of image recognition models for accurate disease detection and classification, promoting advancements in agricultural diagnostics.

## 2. Dataset Preparation

### 2.1 Image Directories

The dataset consists of images organized into three main categories:
- **Early Blight**
- **Late Blight**
- **Healthy Leaves**

### 2.2 Creating Target Directory

A target directory is created to store a balanced set of images, ensuring each category has an equal number of samples for training.

### 2.3 Copying Images

- A function is used to randomly select 500 images from the early and late blight categories and copy them to the target directory.
- Healthy images are augmented to also reach a total of 500 images. This includes applying techniques like rotation and shifting to create variations of the original images.

## 3. Model Training

### 3.1 Model Selection

Several models were chosen for training:
- **Convolutional Neural Network (CNN)**
- **ResNet50**
- **VGG16**
- **MobileNet**

### 3.2 Data Splitting

The dataset is divided into three parts:
- **Training Set:** 70% of the data used to train the models.
- **Validation Set:** 15% of the data used to tune model parameters.
- **Test Set:** 15% of the data used to evaluate final model performance.

### 3.3 Training Process

Each model is trained on the dataset, tracking metrics such as accuracy and loss throughout the training process.

## 4. Model Evaluation and Metrics

### 4.1 CNN
- **Training Summary:**
  - **Epochs:** 50
  - **Best Epoch:** 3
  - **Training Time:** ~17s per epoch

### 4.2 ResNet50
- **Training Summary:**
  - **Epochs:** 50
  - **Training Time:** ~11s per epoch

### 4.3 VGG16
- **Training Summary:**
  - **Epochs:** 50
  - **Training Time:** ~10s per epoch

### 4.4 MobileNetV2
- **Training Summary:**
  - **Epochs:** 50
  - **Training Time:** ~5s per epoch

## 5. Summary of Results

| Model       | Test Accuracy | Test Loss |
|-------------|---------------|-----------|
| CNN         | 96.88%        | 0.2635    |
| ResNet50    | 35.28%        | 1.0890    |
| VGG16       | 36.46%        | 1.0831    |
| MobileNetV2 | 39.58%        | 20.0780   |

## 6. Conclusion

The CNN model outperformed the other architectures, achieving a test accuracy of 96.88% with a minimal loss of 0.2635. In contrast, the other models (ResNet50, VGG16, and MobileNetV2) demonstrated significantly lower performance, suggesting a need for further exploration of hyperparameter tuning or architecture modifications.

## 7. Future Work

Future directions may include:
- Fine-tuning of the underperforming models.
- Experimentation with different data augmentation techniques.
- Exploration of ensemble methods to improve overall classification performance.

