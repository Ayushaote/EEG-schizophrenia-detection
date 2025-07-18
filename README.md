# EEG-schizophrenia-detection
Deep learning-based classification of EEG signals for schizophrenia detection using VGG16

# EEG-Based Schizophrenia Detection using VGG16

This project uses EEG spectrogram images and a fine-tuned VGG16 deep learning model to classify schizophrenia patients vs control subjects.

## 📁 Dataset
- Dataset: ASZED EEG Dataset
- Source: https://zenodo.org/records/14178398
- Spectrograms are generated and stored in the `/EEG_IMAGES_VGG16` directory.

## 📁 Dataset and Artifacts
The project dataset, preprocessed spectrograms, and trained model are stored in Google Drive and can be accessed here:

🔗 https://drive.google.com/drive/folders/1l19MrHUAVGcFp_MirPlvCYMxn_kbvSjN?usp=drive_link

The folder contains:

 - EEG_ASZED_ORGANIZED: EDF files organized and labeled.

 - EEG_IMAGES_VGG16: Spectrogram PNGs generated from EEGs.

 - vgg16_eeg_model.h5: Trained VGG16 model.

🔧 How to Use
After downloading the dataset:

 - Upload it to your Google Drive.
 - Mount Drive in Colab using:

python
`from google.colab import drive
drive.mount('/content/drive')`

Update these paths in the notebook:

python
`data_dir = "/content/EEG_SPLIT"
spectrogram_dir = "/content/drive/MyDrive/EEG_ASZED_PROJECT/EEG_IMAGES_VGG16"
labels_csv_path = "/content/drive/MyDrive/EEG_ASZED_PROJECT/EEG_ASZED_ORGANIZED/labels.csv"
model_path = "/content/drive/MyDrive/EEG_ASZED_PROJECT/vgg16_eeg_model.h5"`

Run the notebook end-to-end. The notebook includes:

 - Preprocessing pipeline
 - Spectrogram generation
 - Train/validation/test splitting
 - VGG16 fine-tuning and evaluation

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
