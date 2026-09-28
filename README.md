# 🤟 IndiSign – Indian Sign Language Recognition

An AI-powered computer vision project that recognizes **Indian Sign Language (ISL) hand gestures** using a deep learning model. The project uses **Convolutional Neural Networks (CNNs)** and image preprocessing techniques to classify different ISL signs.

## 📌 Project Overview

Communication can be challenging for people with hearing and speech disabilities, especially when others are not familiar with sign language.

**IndiSign** aims to bridge this communication gap by using computer vision and deep learning to recognize Indian Sign Language gestures from images.

The system takes a hand-gesture image as input and predicts the corresponding ISL class.

---

## 🚀 Features

- 🤟 Indian Sign Language gesture classification
- 🖼️ Image-based hand gesture recognition
- 🧠 CNN-based deep learning model
- 🔄 Image preprocessing and normalization
- 📊 Dataset analysis and class distribution
- 📈 Model training and validation
- 🎯 Model evaluation using classification metrics
- 🌐 Streamlit-based prediction interface
- 💾 Trained model saved for inference

---

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Python | Programming language |
| TensorFlow / Keras | Deep learning |
| CNN | Image classification |
| NumPy | Numerical computation |
| Pandas | Data analysis |
| Matplotlib | Visualization |
| Scikit-learn | Model evaluation |
| OpenCV | Image processing |
| Streamlit | Web application |
| Jupyter Notebook | Model development |

---

## 📂 Project Structure

IndiSign/
│
├── dataset/
│   ├── train/
│   ├── validation/
│   └── test/
│
├── notebooks/
│   └── indising.ipynb
│
├── models/
│   └── indising_model.h5
│
├── app.py
├── requirements.txt
├── README.md
└── .gitignore
````

> Update the filenames above according to the actual files in your repository.

---

## 📊 Dataset

The dataset contains images representing different **Indian Sign Language hand gestures**.

Each gesture is organized into its corresponding class directory.

Example:

```text
dataset/
│
├── A/
│   ├── image1.jpg
│   ├── image2.jpg
│   └── ...
│
├── B/
│   ├── image1.jpg
│   └── ...
│
├── C/
│   └── ...
│
└── ...
```

The images are resized to:

```text
224 × 224 × 3
```

before being provided to the neural network.

---

## 🔄 Data Preprocessing

The following preprocessing steps are performed:

1. Load images from class directories
2. Resize images to `224 × 224`
3. Convert images into TensorFlow tensors
4. Normalize pixel values
5. Create training, validation, and testing datasets
6. Apply data augmentation to improve generalization

Example:

```python
dataset = tf.keras.utils.image_dataset_from_directory(
    data_dir,
    image_size=(224, 224),
    batch_size=32,
    shuffle=False
)
```

---

## 🧠 Model Architecture

The project uses a **Convolutional Neural Network (CNN)** for image classification.

A typical architecture consists of:

```text
Input Image
     ↓
Convolution Layer
     ↓
Batch Normalization
     ↓
ReLU Activation
     ↓
Max Pooling
     ↓
Convolution Layer
     ↓
Batch Normalization
     ↓
ReLU Activation
     ↓
Max Pooling
     ↓
Flatten / Global Average Pooling
     ↓
Dropout
     ↓
Dense Layer
     ↓
Output Layer
     ↓
Predicted ISL Sign
```

### Why CNN?

CNNs are well suited for image recognition because they can automatically learn important visual features such as:

* Edges
* Shapes
* Textures
* Hand contours
* Finger positions
* Gesture patterns

---

## 📈 Model Training

The model is trained using:

* Optimizer: `Adam`
* Loss function: `Sparse Categorical Crossentropy`
* Evaluation metric: `Accuracy`
* Batch size: `32`
* Input size: `224 × 224`

Example:

```python
model.compile(
    optimizer="adam",
    loss="sparse_categorical_crossentropy",
    metrics=["accuracy"]
)
```

---

## 🛡️ Data Augmentation

Data augmentation is used to create variations of training images and help reduce overfitting.

Possible transformations include:

```python
data_augmentation = tf.keras.Sequential([
    tf.keras.layers.RandomFlip("horizontal"),
    tf.keras.layers.RandomRotation(0.1),
    tf.keras.layers.RandomZoom(0.1)
])
```

> Augmentation should be selected carefully because some transformations may change the meaning of a sign.

---

## 📊 Model Evaluation

The trained model can be evaluated using:

* Accuracy
* Precision
* Recall
* F1-score
* Confusion Matrix

Example:

```text
Classification Report

              precision    recall    f1-score
Class A          ...
Class B          ...
Class C          ...
...
```

---

## 🌐 Streamlit Application

The trained model can be integrated into a Streamlit application.

The application allows users to:

1. Upload an image
2. Preprocess the image
3. Pass it through the trained model
4. Predict the corresponding ISL gesture
5. Display the predicted class

Run the application:

```bash
streamlit run app.py
```

---

## ⚙️ Installation

Clone the repository:

```bash
git clone https://github.com/shiv-1024/IndiSign.git
```

Move into the project directory:

```bash
cd IndiSign
```

Create a virtual environment:

```bash
python -m venv .venv
```

Activate it on Windows:

```bash
.venv\Scripts\activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## ▶️ Usage

### Train the model

Open the notebook:

```bash
jupyter notebook
```

Run the training pipeline.

### Run the Streamlit application

```bash
streamlit run app.py
```

Upload an ISL gesture image and the model will generate a prediction.

---

## 📌 Future Improvements

* 🎥 Real-time sign recognition using webcam
* ✋ Hand detection using MediaPipe
* 🔤 Recognition of more ISL signs
* 🗣️ Convert recognized signs into text
* 🔊 Text-to-speech integration
* 📱 Mobile application
* ⚡ Model optimization for real-time inference
* 🧠 Experiment with transfer learning models such as VGG19, ResNet, and MobileNet

---

## 🎯 Learning Outcomes

Through this project, I worked with:

* Computer Vision
* Convolutional Neural Networks
* Image preprocessing
* Data augmentation
* Dataset analysis
* Deep learning model training
* Model evaluation
* TensorFlow/Keras
* Streamlit deployment

---

## 👨‍💻 Author

**P Sivarajadurai**

B.Tech – Artificial Intelligence and Data Science

### Connect with me

* 💼 LinkedIn: [P Sivarajadurai](https://www.linkedin.com/in/sivarajadurai-p-33904b252/)
* 🐙 GitHub: [shiv-1024](https://github.com/shiv-1024)

---

## ⭐ Support

If you find this project useful, consider giving the repository a ⭐.

```

**Important:** Before pushing it, replace the placeholder model/notebook filenames and the dataset description with the exact details from your repository.
```
