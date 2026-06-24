# Face Attribute Analysis & Style Recommendation Tool 👁️💄

## 📌 Overview
This project presents an **end-to-end computer vision system** that analyzes facial attributes (face shape and eye shape) and provides **personalized style recommendations**.

The system is designed with **Responsible AI principles**, ensuring:
- ✅ No identity recognition
- ✅ No biometric tracking
- ✅ No gender classification
- ✅ Full transparency in recommendations

---

## 🎯 Objectives
- Build a deep learning model for facial attribute classification
- Predict **face shape** and **eye shape**
- Generate **explainable style recommendations**
- Ensure ethical and privacy-preserving AI design

---

## 🧠 System Pipeline

1. Face Detection & Alignment (MTCNN)
2. Image Preprocessing & Normalization
3. Feature Extraction (CNN - ResNet50)
4. Attribute Classification (Face & Eye Shape)
5. Explainability (Grad-CAM)
6. Rule-based Style Recommendation
7. User Interface (Gradio)

---

## 🗂️ Datasets

- **Face Shape Dataset (Kaggle)**
  - Classes: Oval, Round, Square, Heart, Oblong

- **Eye Shape Dataset (Roboflow - YOLO format)**
  - Classes: Almond, Hooded, Monolid, Round, Up-Turned, Down-Turned

### Key Data Engineering:
- Converted YOLO dataset → PyTorch classification format
- Cropped eye regions from bounding boxes
- Cleaned and structured datasets dynamically

---

## 🧠 Model Architecture

- **Backbone:** ResNet50 (Pretrained on ImageNet)
- Full fine-tuning applied
- Custom classification head with dropout

### Regularization Techniques:
- Data Augmentation
- Dropout (0.5)
- Weight Decay
- Early Stopping
- Learning Rate Scheduler

---

## 📊 Results

| Model            | Accuracy | Macro F1 |
|------------------|---------|----------|
| Face Shape Model | ~82%    | ~82%     |
| Eye Shape Model  | ~98%    | ~98%     |

### Insights:
- Eye shape achieved high accuracy due to precise cropping
- Face shape is harder due to overlapping features

---

## 🔍 Model Explainability

Grad-CAM was implemented to visualize model decisions:



### Key Benefit:
- Ensures model focuses on **relevant facial features**
- Improves trust and transparency

---

## 💡 Style Recommendation System

A **rule-based mapping system** ensures:
- No AI hallucination
- Full transparency

Examples:
- Round Face → Long layers (elongation)
- Hooded Eyes → Center-focused lashes

---

## 🌐 User Interface

Built using **Gradio**:



### Features:
- Upload image
- Automatic analysis
- Instant recommendations
- Privacy-focused processing

---

## 🔒 Ethical AI Considerations

- ✅ No facial recognition or identity tracking
- ✅ No demographic inference
- ✅ Ephemeral image processing (not stored)
- ⚠️ Dataset bias acknowledged and discussed

---

## 🛠️ Technologies Used

- Python
- PyTorch
- OpenCV
- MTCNN
- Grad-CAM
- Scikit-learn
- Gradio
