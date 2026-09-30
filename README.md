# 🤟 IndiSign – Indian Sign Language Prediction

A deep learning-based computer vision project for recognizing **Indian Sign Language (ISL) hand gestures** from images.

The project uses **TensorFlow/Keras and Convolutional Neural Networks (CNNs)** to learn visual patterns from sign language images and predict the corresponding sign class.

## 📌 Project Overview

Indian Sign Language provides an important means of communication for the deaf and hard-of-hearing community.

This project explores how **Deep Learning and Computer Vision** can be used to automatically recognize Indian Sign Language gestures from images.

The complete workflow includes:

* Dataset loading
* Image preprocessing
* Dataset exploration
* Data visualization
* CNN model development
* Model training
* Model validation
* Performance analysis
* Prediction of sign language classes

---

## 🎯 Objective

The main objective of this project is to develop an image classification model capable of identifying different Indian Sign Language gestures.

### Input

An image containing an Indian Sign Language hand gesture.

### Output

The predicted Indian Sign Language class.

```text
Hand Gesture Image
        ↓
Image Preprocessing
        ↓
CNN Model
        ↓
Feature Extraction
        ↓
Classification
        ↓
Predicted ISL Sign
```

---

## 🧠 Machine Learning Approach

The project uses a **Convolutional Neural Network (CNN)** for image classification.

CNNs are particularly suitable for image-based problems because they can automatically learn spatial features such as:

* Edges
* Shapes
* Textures
* Hand structures
* Finger positions
* Gesture patterns

The network progressively learns higher-level features from the input images before performing classification.

---

## 🔄 Project Workflow

```text
Dataset
   ↓
Data Loading
   ↓
Image Resizing
   ↓
Image Preprocessing
   ↓
Dataset Visualization
   ↓
Train / Validation / Test Split
   ↓
Data Augmentation
   ↓
CNN Model
   ↓
Model Training
   ↓
Validation
   ↓
Performance Evaluation
   ↓
ISL Prediction
```

---

## 📊 Dataset

The project uses an image dataset containing different Indian Sign Language gesture classes.

The dataset is stored in the `data/` directory.

Images are processed using TensorFlow's image dataset utilities and resized to:

```text
224 × 224 × 3
```

where:

* `224` = image height
* `224` = image width
* `3` = RGB color channels

The dataset is then converted into batches for efficient model training.

---

## 🔧 Data Preprocessing

The preprocessing pipeline includes:

1. Loading images from the dataset
2. Resizing images to `224 × 224`
3. Converting images into TensorFlow tensors
4. Normalizing pixel values
5. Creating batches
6. Preparing datasets for model training
7. Applying suitable data augmentation techniques

Example:

```python
dataset = tf.keras.utils.image_dataset_from_directory(
    data_dir,
    image_size=(224, 224),
    batch_size=32
)
```

---

## 🧠 CNN Architecture

The project implements a CNN-based image classification model.

The general architecture follows:

```text
Input Image
     ↓
Convolution
     ↓
Batch Normalization
     ↓
Activation Function
     ↓
Pooling
     ↓
Convolution
     ↓
Batch Normalization
     ↓
Activation Function
     ↓
Pooling
     ↓
Feature Extraction
     ↓
Flatten / Global Pooling
     ↓
Dropout
     ↓
Dense Layer
     ↓
Output Layer
     ↓
ISL Class
```

The model learns useful visual representations automatically during training.

---

## 🛡️ Data Augmentation

Data augmentation can be used to improve model generalization by creating variations of training images.

Possible transformations include:

```python
tf.keras.layers.RandomRotation()
tf.keras.layers.RandomZoom()
tf.keras.layers.RandomContrast()
```

Augmentation needs to be applied carefully for sign-language recognition because certain transformations, especially horizontal flipping, may alter the meaning of a gesture.

---

## 📈 Model Training

The model is trained using TensorFlow/Keras.

Typical training configuration includes:

| Parameter  | Value                           |
| ---------- | ------------------------------- |
| Framework  | TensorFlow / Keras              |
| Model      | CNN                             |
| Input Size | 224 × 224 × 3                   |
| Batch Size | 32                              |
| Optimizer  | Adam                            |
| Loss       | Sparse Categorical Crossentropy |
| Metric     | Accuracy                        |

Example:

```python
model.compile(
    optimizer="adam",
    loss="sparse_categorical_crossentropy",
    metrics=["accuracy"]
)
```

---

## 📉 Training Performance

The repository includes training performance visualizations for:

### Accuracy

The training accuracy graph is used to observe how the model's classification performance changes across epochs.

### Loss

The training loss graph helps analyze how the model's prediction error changes during training.

The repository contains:

```text
Accuracy Comparison Training.png
Loss Comparion Training.png
```

These plots can be used to analyze training behavior and identify possible overfitting or underfitting.

---

## 🖼️ Prediction Output

The repository also contains an example prediction/output image:

```text
output.png
```

This provides a visual representation of the model's prediction result.

---

## 📂 Project Structure

```text
indisignlang_prediction/
│
├── data/
│   └── Dataset files
│
├── main.ipynb
│   └── Complete model development and training workflow
│
├── Accuracy Comparison Training.png
│   └── Training accuracy visualization
│
├── Loss Comparion Training.png
│   └── Training loss visualization
│
├── output.png
│   └── Prediction/output visualization
│
├── requirements.txt
│   └── Python dependencies
│
└── README.md
```

---

## 🛠️ Technologies Used

### Programming Language

* Python

### Deep Learning

* TensorFlow
* Keras
* Convolutional Neural Networks

### Data Processing

* NumPy
* Pandas

### Computer Vision

* OpenCV
* Image preprocessing

### Visualization

* Matplotlib

### Development

* Jupyter Notebook
* Git
* GitHub

---

## ⚙️ Installation

Clone the repository:

```bash
git clone https://github.com/shiv-1024/indisignlang_prediction.git
```

Navigate to the project directory:

```bash
cd indisignlang_prediction
```

Create a virtual environment:

```bash
python -m venv .venv
```

Activate the environment on Windows:

```bash
.venv\Scripts\activate
```

Install the required dependencies:

```bash
pip install -r requirements.txt
```

---

## ▶️ Running the Project

Open the Jupyter Notebook:

```bash
jupyter notebook
```

Then open:

```text
main.ipynb
```

Run the notebook cells sequentially to:

1. Load the dataset
2. Explore the images
3. Preprocess the data
4. Build the CNN model
5. Train the model
6. Evaluate the model
7. Generate predictions
8. Visualize the results

---

## 📊 Model Evaluation

The model can be evaluated using metrics such as:

* Accuracy
* Precision
* Recall
* F1-score
* Confusion Matrix
* Training/validation loss
* Training/validation accuracy

These metrics help understand how well the model performs across different sign classes.

---

## 🔍 Key Learning Outcomes

Through this project, I gained practical experience in:

* Computer Vision
* Deep Learning
* CNN architecture
* Image classification
* TensorFlow/Keras
* Image preprocessing
* Data augmentation
* Dataset analysis
* Model training
* Model evaluation
* Visualization
* Jupyter Notebook
* Git and GitHub

---

## 🚀 Future Improvements

The project can be extended with:

* Real-time ISL recognition using a webcam
* Hand detection using MediaPipe
* Real-time video-based recognition
* Transfer learning using VGG19, ResNet, or MobileNet
* Improved model generalization
* Hyperparameter tuning
* Confusion matrix analysis
* Deployment using Streamlit
* Text-to-speech conversion
* Mobile application integration

---

## 👨‍💻 Author

**P Sivarajadurai**

B.Tech – Artificial Intelligence and Data Science

### Connect with me

* LinkedIn: [P Sivarajadurai](https://www.linkedin.com/in/sivarajadurai-p-33904b252/)
* GitHub: [shiv-1024](https://github.com/shiv-1024)

---

## ⭐ Project

If you find this project useful, feel free to ⭐ the repository.

**Repository:**
https://github.com/shiv-1024/indisignlang_prediction
