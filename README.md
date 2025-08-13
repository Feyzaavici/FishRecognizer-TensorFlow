# Akbank Deep Learning Boostcamp

## 🐟 Fish Classification Project
This project uses deep learning methods to classify different fish species based on their images.  
Built with the **TensorFlow** library, the model is trained on various fish images and supported by image processing and data preprocessing techniques.

---

## 📂 Project Contents

### 1. Setup
Before running the project, you need to install the required dependencies. Follow the steps below to set up your environment:

**Requirements**
```bash
tensorflow==2.16.1
numpy
pandas
opencv-python
matplotlib
seaborn
scikit-learn
h5py
keras
```
---
### 2. Dataset
The project works on an image dataset containing various fish species.  
The dataset consists of images representing each fish species and is split into:

- **Training Set**: Images used for the model to learn.  
- **Test Set**: Images used to measure the model’s accuracy.

---

### 3. Data Preprocessing
Before training the model, the image data is processed through several steps:

- **Resizing**: All images are resized to a fixed size (e.g., 224x224 pixels).  
- **Normalization**: Pixel values are normalized to a range between 0 and 1.  
- **Augmentation**: Data augmentation techniques (rotation, cropping, horizontal/vertical flipping) are applied during training to make the model more robust.

---

### 4. Model
The core component of the project is a deep learning model developed with TensorFlow.  
The architecture includes:

- **Input Layer**: Accepts images of size 224x224x3.  
- **Convolutional Layers**: Learn features from the images.  
- **MaxPooling Layers**: Reduce the size of the feature maps.  
- **Dense Layers**: Fully connected layers for classification.  
- **Dropout**: Randomly disables some neurons during training to prevent overfitting.  
- **Softmax Output Layer**: Calculates the probability for each fish species.


### 5. Training
The model is trained on the dataset with the following settings:

- **Loss Function**: Categorical Cross-Entropy  
- **Optimizer**: Adam  
- **Metrics**: Accuracy

---

### 6. Evaluation and Results
After training, the model is evaluated on the test data.  
The following metrics are calculated:

- **Accuracy**: Measures the model’s classification performance.  
- **Loss**: Training and validation loss values are examined.  

The results are visualized using **matplotlib** graphs.

---

### 7. Saving the Model
After training, the model is saved in `.h5` format for future use.

---

### 8. GPU Usage
The model is configured to support GPU usage.  
If a GPU is available, TensorFlow will automatically use it; otherwise, it will run on CPU.

---

## 📜 License
This project is licensed under the **MIT License**.

--- 
## Kaggle link
https://www.kaggle.com/code/feyzaavc/fish-classification

