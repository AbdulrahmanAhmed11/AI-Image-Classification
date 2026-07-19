# AI-Image-Classification
Classifying electronic development boards using Machine Learning, Google Teachable Machine, and Keras.
# 🚀 AI Image Classification

## 📌 Project Overview
This project aims to utilize Machine Learning and Computer Vision techniques to develop a model capable of automatically recognizing different types of microcontrollers and electronic development boards. This model can later be integrated into automated sorting systems in production lines or used as part of advanced robotic vision systems to identify electronic components in a workspace.

## 📊 Dataset & Training
The dataset was built and the initial model was trained using the **Google Teachable Machine** platform. The training phase involved feeding the model with isolated and diverse images for three main categories of popular development boards used in embedded systems:

1. **Arduino Uno**: Characterized by its rectangular shape and distinct blue color.
2. **Raspberry Pi Pico**: Characterized by its slim size and the central chip.
3. **ESP32**: Characterized by the metallic shield of its communication chip (Wi-Fi/Bluetooth).

*The image below shows the model training interface and class distribution within the Teachable Machine platform:*

<img width="2171" height="1137" alt="Screenshot 2026-07-19 044223" src="https://github.com/user-attachments/assets/3f964df1-831c-4b3f-9f1f-baa0435e8479" />

## ⚙️ Methodology & Tech Stack
* **Data Collection:** Using isolated background images of the boards to ensure the model focuses purely on the hardware features and is not distracted by background elements.
* **Training:** Relying on Deep Learning techniques for image classification.
* **Model Export:** The final model was exported in `Keras (.h5)` format for seamless integration into external programming environments.
* **Testing Environment:** A Python inference script was built inside **Google Colab**, relying on the `tf-keras` library to ensure full compatibility and accurate execution of the legacy Keras model.

## 🔬 Testing & Inference
The model was tested using novel images (that it was not previously trained on) to evaluate its generalization ability. The Python script processes the input image, resizes it to `224x224` to match the model's input shape requirements, and normalizes the array data before passing it to the prediction layers.

The model demonstrated high efficiency in distinguishing between electronic boards, successfully recognizing the input board with an excellent confidence score.

*The image below demonstrates the Python script's success in recognizing an ESP32 board with nearly 90% accuracy:*

<img width="548" height="147" alt="Screenshot 2026-07-19 065312" src="https://github.com/user-attachments/assets/3164d4f7-bd43-4074-9d26-fca010996853" />

## 🛠️ Future Scope
* Converting the model to **TensorFlow Lite (TFLite)** format to reduce its size and significantly accelerate inference time.
* Integrating the model directly with a microcontroller equipped with a camera module for local, on-device image processing (Edge AI), eliminating the need for external cloud servers.
