###RCNN-Based Chest X-Ray Classification

##Introduction
This project implements a Region-based Convolutional Neural Network (RCNN) to classify chest X-rays into two categories: Normal and Pneumonia. The model leverages the pre-trained VGG16 architecture for feature extraction and fine-tunes a custom head for binary classification.

#Installation
To run this project, install the required dependencies:
pip install tensorflow numpy matplotlib pandas pillow

#Usage
1.Prepare the Dataset: Ensure your dataset is organized as follows:
data/
├── train/
│   ├── NORMAL/
│   ├── PNEUMONIA/
├── val/
│   ├── NORMAL/
│   ├── PNEUMONIA/
├── test/
    ├── NORMAL/
    ├── PNEUMONIA/
2.Train the Model: Run the training script to train the RCNN model:
python rcnn.py
3.Make Predictions: Use the trained model to predict a chest X-ray image:
from rcnn import predict_image_rcnn
predict_image_rcnn("path/to/your/image.jpg")

#Project Structure
.
├── rcnn.py                     # Main script for training and evaluating the model
├── chestxray_rcnn_model.h5     # Trained model file
├── data/                       # Directory for training, validation, and test images
├── README.md                   # Project documentation

##License
This project is licensed under the MIT License.
