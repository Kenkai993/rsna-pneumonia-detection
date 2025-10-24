# RSNA Pneumonia Detection Project 🫁

This project demonstrates a complete AI pipeline for detecting and visualizing pneumonia in chest X-rays using the **RSNA Pneumonia Detection Challenge** dataset.

It combines medical imaging preprocessing, model training, bounding box visualization, and Grad-CAM interpretability into a unified, reproducible workflow.

---

## 📁 Project Structure
rsna-pneumonia-detection-challenge
│
├── 01_Dicom_image_Preproc.ipynb # DICOM loading & preprocessing
├── 02_Pneumonia_classification.ipynb # Model training & evaluation (PyTorch Lightning)
├── 03_Pneumonia_Boundbox.ipynb # Radiologist bounding box visualization
├── 04_Pneumonia_Cam.ipynb # Grad-CAM explainability (AI heatmap)


## ⚙️ Installation

Create a virtual environment and install dependencies:

```bash
python -m venv venv
venv\Scripts\activate          # On Windows
# source venv/bin/activate     # On Linux/Mac

pip install -r requirements.txt

🧠 Key Components


1️⃣ DICOM Preprocessing

Converts .dcm medical images to normalized tensors

Performs intensity normalization and resizing

Saves processed data for efficient training

2️⃣ Pneumonia Classification

Model: ResNet18 (PyTorch Lightning)

Metric: AUROC, Accuracy

Training logs and checkpoints saved automatically in logs/lightning_logs/

3️⃣ Bounding Box Visualization

Displays radiologist-annotated regions of pneumonia (ground truth)

Uses bounding boxes from stage_2_train_labels.csv

Example:(docs/BBOX_Pneumonia.png)


4️⃣ Grad-CAM (Model Interpretability)

Visualizes AI model attention over the same chest X-ray

Compares human (radiologist) vs AI focus

Example:

![Grad-CAM Example](https://raw.githubusercontent.com/Kenkai993/rsna-pneumonia-detection/main/Pneumonia%20detection%20project/docs/Heatmap_Pneumonia.png)



🧩 Requirements

All dependencies are listed in requirements.txt.
Key packages:

torch, torchvision, pytorch-lightning

pydicom, opencv-python, matplotlib, pandas, numpy

🩻 Dataset Info

Dataset: RSNA Pneumonia Detection Challenge (Kaggle)

Each image is a chest X-ray in DICOM format.

Each pneumonia region is labeled with bounding box coordinates.

Labels CSV columns:
patientId, x, y, width, height, Target



🧩 Author

Milos Stanisljevic
Radiology Technologist (MTRA) | AI & Medical Imaging Enthusiast
LinkedIn Profile:
 
