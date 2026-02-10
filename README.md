# Speaker Verification Model 🔊🔐

This project implements a Speaker Verification system developed as part of my Speech Processing internship.  
The goal is simple: **verify whether two audio samples belong to the same speaker** using deep learning–based audio embeddings.

---

## 🚀 Project Overview

Speaker Verification is different from general speech classification — instead of identifying *what* is spoken, we identify *who* is speaking.  
This notebook explores:

- Audio preprocessing  
- MFCC & spectrogram feature extraction  
- CNN-based embedding model  
- Similarity scoring between speaker audio samples  
- Evaluation using ROC curves, AUC, confusion matrix, and accuracy  

The project is implemented inside a Jupyter Notebook and follows a simple, easy-to-reproduce structure.

---

## 📁 Repository Structure

speaker-verification-model/
│── notebooks/
│ ├── model_training.ipynb
│ ├── model_testing.ipynb
│
│── results/
│ └── confusion_matrix.png
│ └── far_frr_vs_threshold.png
│ └── roc_curve.png
│ └── similarity_histogram.png
│ └── tpr_fpr.png
│
│── README.md
│── requirements.txt
│── .gitignore

---

## 🧠 Model Details

- **Framework:** PyTorch  
- **Input Features:** Mel-Spectrograms / MFCCs  
- **Model Type:** CNN-based speaker embedding network  
- **Output:** Similarity score between audio samples  
- **Task:** Verification (same-speaker vs different-speaker)  

The trained model file (`speaker_cnn_trained.pth`) is included and used directly by the verification notebook.

---

## 📊 Results & Evaluation

The model is evaluated using:

- Confusion Matrix
- FAR FRR vs Threshold
- ROC Curve  
- Similarity Histogram
- TPR FPR 

(These plots are located in the `results/` folder.)

---

## 📦 How to Run Locally

1. Clone this repository: git clone https://github.com/dastardly_kat/speaker-verification-model.git

2. Install dependencies: pip install -r requirements.txt

3. Place your audio dataset in this structure:
                data/
                │── true_speaker/
                │── false_speaker/
                │── test_speakers/

4. Update paths inside the notebooks  
(Kaggle paths are provided but can be replaced with local paths.)

5. Run the notebooks
Open Jupyter: jupyter notebook

Then open:

- `notebooks/model_training.ipynb`
- `notebooks/model_testing.ipynb`

---

## 📘 Dataset Notes

The notebook was originally executed in a Kaggle environment, which uses paths like: /kaggle/input/speaker-verification/...

For local execution, simply replace these paths with local dataset directories as shown above.
