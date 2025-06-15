# Cattle-Identification-via-Muzzle-Print

# Cattle Muzzle Print Recognition using a Hybrid CNN-Transformer Model

This project presents a novel deep learning approach for identifying individual cattle based on their unique muzzle prints. By leveraging a custom hybrid architecture, the model achieves high accuracy, offering a reliable and non-invasive alternative to traditional identification methods like ear tags.

## 🌟 Key Features

- **High Accuracy**: Achieved **97.46%** accuracy on the validation set.
- **Hybrid Architecture**: Combines a Convolutional Neural Network (**EfficientNetV2-S**) and a **Vision Transformer (ViT)** to capture both local textures and global patterns.
- **Attention-Based Fusion**: Utilizes a **Multi-Head Attention (MHA)** mechanism to intelligently fuse features from both backbones, enhancing predictive power.
- **End-to-End Training**: The entire model is trained from scratch in a single, streamlined process.
- **Built with PyTorch**: Implemented using modern, industry-standard deep learning tools.

## ⚙️ Model Architecture (MHAFF)

The core of this project is the **M**ulti-**H**ead **A**ttention **F**eature **F**usion (MHAFF) model. It processes an input image through two parallel backbones:

1.  **CNN Backbone (`EfficientNetV2-S`)**: Excels at extracting detailed local features, such as the unique lines and textures of the muzzle print.
2.  **Transformer Backbone (`vit_small_patch16_224`)**: Divides the image into patches and analyzes the relationships between them, capturing the global structure of the print.

The feature vectors from both backbones are then concatenated and passed through a **Multi-Head Attention** layer. This layer acts as a fusion module, weighing the importance of different feature combinations before the final classification is made by a linear layer.
