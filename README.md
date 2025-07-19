# DeepFake Creation and Detection of Multimedia Data 🎭🔍

## 📌 Overview

This project explores both the **creation** and **detection** of DeepFakes in multimedia content. While the generation aspect is purely educational, the focus is on building a robust DeepFake **detection pipeline** using computer vision and deep learning techniques.

---

## 🎯 Objectives

- Understand DeepFake generation using encoder-decoder models (for academic purpose only).
- Build a DeepFake detection system using **ResNet50 + LSTM**.
- Trigger **real-time alerts** using Telegram bots.
- Evaluate model performance on test images/videos.

---

## 🛠️ Tools and Technologies

- Python, Google Colab
- TensorFlow, Keras
- OpenCV, MTCNN, dlib
- Telepot (Telegram Bot API)
- Streamlit (optional UI)

## 📁 Folder Structure
📂 datasets  
├── 📂 celeb_df  
│   ├── 📄 real/ — Real .mp4 videos  
│   └── 📄 fake/ — DeepFake .mp4 videos  
└── 📂 preprocessed  
    ├── 📄 real/ — Extracted real face images  
    └── 📄 fake/ — Extracted fake face images  

## 📦 Dataset

- Subset of **Celeb-DF v2**
- 10 real and 10 fake videos used for training
- Frames extracted every 10th frame
- Faces cropped to 160x160 using **MTCNN**

---

## 🧠 Methodology

### 🔹 Preprocessing
- Extract frames from videos using OpenCV
- Detect faces using **MTCNN**
- Save cropped face images (160x160 px)

### 🔹 Model Architecture
- **Feature Extractor**: Pretrained **ResNet50**
- **Temporal Modeling**: **LSTM** layer
- **Classifier**: Dense layer + Sigmoid activation

### 🔹 Training
- Input: Sequences of 5 face images
- Loss: Binary Crossentropy
- Optimizer: Adam
- Metrics: Accuracy
- Epochs: 5 (demo scale)

---

## 🚨 Real-time Alerting (Telegram Bot)

- Bot setup via [@BotFather](https://t.me/botfather)
- Prediction threshold set at 0.88
- If `prediction < 0.88` → sends alert:  
  ⚠️ *DeepFake Detected!*
- Integrated within the model’s prediction function

---

## 📊 Results

- **Training Accuracy**: ~95%
- **Validation Accuracy**: ~85%
- Graphs plotted using Matplotlib in Google Colab

---

## 🧪 Sample Test

- Uploaded real image (e.g., actor's photo)
- Model sometimes predicts false positives due to small dataset

---

## ✅ Conclusion

This project demonstrates a working DeepFake detection pipeline, from data preprocessing to alert generation. The ResNet50 + LSTM combo shows strong performance, and with additional training data, this can be scaled for real-world applications.

---

## 🚀 Future Enhancements

- Train on a larger dataset (200+ videos)
- Integrate audio-based DeepFake detection
- Add web interface using **Streamlit**
- Deploy on cloud or mobile for real-time analysis

---

## 📬 Contact

Created by **Deeksha SM**  
- 📧 deekshamurthys@gmail.com  
- 🌐 [LinkedIn](https://www.linkedin.com/in/deekshasm18)  
- 💻 [GitHub](https://github.com/Deeksha1803)

---


