# Teeth Classification Using Deep Learning

## Introduction
The classification of dental images is pivotal in modern dentistry, aiding in diagnostic precision and tailored patient care. With advancements in AI, there is a growing potential to automate this process, offering consistent and efficient diagnostic tools. This project focuses on developing a robust teeth classification model, aligning with healthcare industry standards to provide enhanced diagnostic capabilities.

## Project Overview
This project is designed to classify images of teeth into seven categories:
- OLP
- OT
- CaS
- MC
- OC
- CoS
- Gum

## Dataset
The dataset contains images classified into seven categories, stored in three separate directories:
- **Training:** 3087 images
- **Validation:** 1028 images
- **Testing:** 1028 images

The images are stored in directories corresponding to their class labels.

## Preprocessing and Augmentation
Preprocessing and augmentation were performed using the `ImageDataGenerator` class from Keras. The following augmentations were applied to the training data:
- Rescaling
- Rotation (up to 20 degrees)
- Width and height shifts (up to 20%)
- Shear transformation
- Zooming
- Horizontal flipping
- Nearest-fill mode for filling in missing pixels after transformations

The validation data was only rescaled without additional augmentation.

## Methodology
### 1. Data Preprocessing
To ensure the model's effectiveness, preprocessing is crucial. Techniques such as normalization and augmentation were employed:
- **Normalization:** Standardizing image data to improve model performance.
- **Augmentation:** Techniques like rotation, flipping, and scaling were applied to increase dataset variability, combating overfitting.

### 2. Visualization
Understanding the dataset distribution is essential. The dataset’s class distribution was visualized to ensure a balanced representation, which is crucial for training a fair model. Additionally, samples before and after augmentation were displayed to evaluate preprocessing efficacy.

### 3. Model Architecture and Training
A custom deep learning model was constructed using TensorFlow/PyTorch. The architecture was designed specifically for the classification task:
- **Layers:** Convolutional layers followed by pooling layers, capturing spatial hierarchies in the images.
- **Activation Functions:** ReLU for non-linearity and softmax for output probabilities.
- **Training:** The model was trained using a standard training loop, optimizing for categorical cross-entropy loss and monitored via accuracy metrics.

## Results
The model achieved an accuracy of **92%** on the test set, establishing a solid performance baseline. This result demonstrates the model's potential effectiveness in clinical settings, with further fine-tuning expected to enhance results.


