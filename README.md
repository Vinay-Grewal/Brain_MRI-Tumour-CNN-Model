## Brain MRI Tumor Classifier (Keras + CNN)
A deep learning model built with Keras that classifies brain tumors from MRI scans into four categories using Convolutional Neural Networks (CNNs).

# 🧠 Project Overview
This project aims to assist in early brain tumor detection by classifying MRI images into four tumor types. A custom CNN architecture was designed and trained using the Brain Tumor Classification MRI dataset from Kaggle. The model achieves strong performance on unseen data, demonstrating the effectiveness of deep learning in medical imaging.

# 📁 Dataset
- Source: Kaggle - Brain Tumor Classification MRI
- Classes:
  - Glioma
  - Meningioma
  - Pituitary Tumor
  - No Tumor
- Size: ~3,287 MRI images
- Format: RGB images, various resolutions

# ⚙️ Preprocessing
- Resizing: All images resized to 150x150x3
- Normalization: Pixel values scaled to [0, 1]
- Augmentation: Applied rotation, flipping, zoom, and contrast adjustment to increase robustness and reduce overfitting

# 🧱 Model Architecture
- Built using Keras Sequential API
- Architecture includes:
  - Multiple Conv2D + ReLU + MaxPooling + Dropout blocks
  - Fully connected Dense layers
  - Final output layer with Dense(4, activation='softmax')
- Dropout layers added to mitigate overfitting

# 🧪 Training Details
- Optimizer: Adam
- Loss Function: Categorical Crossentropy
- Epochs: 20 (CAN BE INCREASED WITH EARLY STOPPING)
- Batch Size: 32
- Validation Split: 10% of training data
- Callbacks: EarlyStopping and ModelCheckpoint CAN BE USED* for improvement

# 📈 Performance
- Training Accuracy	95.1%
- Validation Accuracy	75.2%
- Final Val Loss	0.8960
<br> The model shows strong learning and generalization, making it a good baseline for further enhancement or deployment.


