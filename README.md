# EEG-schizophrenia-detection
Deep learning-based classification of EEG signals for schizophrenia detection using VGG16

# EEG-Based Schizophrenia Detection using VGG16

This project uses EEG spectrogram images and a fine-tuned VGG16 deep learning model to classify schizophrenia patients vs control subjects.

## 📁 Dataset
- Dataset: ASZED EEG Dataset
- Source: https://zenodo.org/records/14178398
- Spectrograms are generated and stored in the `/EEG_IMAGES_VGG16` directory.

## 🚀 Workflow
- Preprocessing raw EEG (.edf)
- Spectrogram generation
- Dataset stratified splitting (train/val/test)
- Training VGG16 with class imbalance handling
- Evaluation using Accuracy, Confusion Matrix, ROC-AUC

## 📊 Results
- Best Test Accuracy: ~76.6%
- ROC-AUC: 0.84
- Confusion Matrix and classification report provided

## 🧠 Future Work
- Include transformer models
- Improve interpretability with Grad-CAM
