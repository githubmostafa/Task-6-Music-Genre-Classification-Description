
✅ Music Genre Classification

This repository contains a machine learning project that builds and compares multiple models to classify music tracks into genres using the GTZAN dataset. The project includes MFCC-based feature extraction, spectrogram image generation, model training using Random Forest, CNN, SVM, and transfer learning with MobileNetV2, followed by evaluation and visualization of results.

📁 Dataset Source: GTZAN (Kaggle)

Description:
1,000 audio tracks (30 seconds each), covering 10 genres:
blues, classical, country, disco, hiphop, jazz, metal, pop, reggae, rock

🎯 Target:
Classify each audio track into its correct genre using different ML/DL approaches.

📊 Models Compared

✅ Random Forest Classifier (Tabular — MFCCs)
Extracted 13 MFCC features per track
Used on tabular data
Baseline model for genre classification

✅ SVM (Image-Based — Spectrograms 64×64)
Converted audio to spectrogram images
Applied SVM classifier
Lower performance compared to deep models

✅ Custom CNN (Image-Based)
Built and trained a Convolutional Neural Network
Input size: 64×64×3 spectrograms
Moderate improvement over SVM

✅ MobileNetV2 (Transfer Learning — Spectrograms 96×96)
Pretrained on ImageNet, fine-tuned with spectrograms
Best accuracy among all models
Used only final dense layer as trainable

🔧 Features & Workflow

Audio loading and preprocessing with Librosa

MFCC extraction and CSV generation

Spectrogram generation using Mel scaling

Image resizing to 64×64 and 96×96

Train/test split (80/20)

Model training with:

RandomForestClassifier (scikit-learn)

SVM (scikit-learn)

CNN (Keras)

MobileNetV2 (Keras Applications)

Model evaluation using:

Accuracy

Classification Report

Confusion Matrix

Best model performance plotted and analyzed

📦 Requirements

nginx
Copy
Edit
pandas
numpy
matplotlib
librosa
opencv-python
scikit-learn
tensorflow / keras
📈 Sample Results

Model	Input Type	Accuracy
Random Forest	MFCC (Tabular)	0.56
SVM	Spectrogram	0.44
CNN	Spectrogram	0.55
MobileNetV2	Spectrogram	0.63 ✅

📊 Result Summary

MobileNetV2 with transfer learning gave the best results (Accuracy ≈ 0.63)

MFCC-based Random Forest provided quick and interpretable baseline

CNNs performed better than traditional SVM on spectrograms

Spectrogram-based models benefit significantly from pre-trained networks

Project includes full comparison between classical and deep learning models

📌 License
This project is intended for educational and research purposes as part of the Elevvo Pathways ML 
