# 🫁 Pneumonia Detection on Chest X-rays (RSNA Dataset)

This project demonstrates a **complete end-to-end AI workflow** for pneumonia detection using chest X-ray (DICOM) images — from preprocessing to model interpretability (Grad-CAM).

Developed as part of my professional transition from **Radiologic Technologist (MTRA)** to **AI/ML Specialist in Medical Imaging**, this project combines practical clinical insight with deep learning.

---

## 🧠 Project Overview
- **Modality:** Chest X-ray (DICOM)
- **Dataset:** RSNA Pneumonia Detection Challenge
- **Framework:** PyTorch and Pytorch_lightning
- **Goal:** Detect and localize pneumonia on X-rays with visual explanations (Grad-CAM).
## 🧩 Repository Structure
Pneumonia detection project/
│
├── 01_DICOM_Preproc.ipynb → DICOM loading, normalization, pixel value scaling
├── 02_Pneumonia_classification.ipynb → CNN model (ResNet/DenseNet) for pneumonia classification
├── 03_Pneumonia_Boundbox.ipynb → Bounding box localization of pneumonia regions
├── 04_Pneumonia_cam.ipynb → Grad-CAM heatmap visualization
│
├── requirements.txt
└── README.md

## ⚙️ Technologies Used
| Category | Library |
|-----------|----------|
| Deep Learning | PyTorch, TorchVision |
| Image Processing | OpenCV, NumPy, pydicom |
| Data Handling | pandas, tqdm |
| Visualization | Matplotlib |
| Model Evaluation | TorchMetrics |

---

## 🚀 How to Run

1️⃣ Clone this repository  
```bash
git clone https://github.com/Kenkai993/Pneumonia-detection.git
cd Pneumonia-detection

2️⃣Install dependencies

pip install -r requirements.txt

3️⃣ Run the notebooks in order:
01_DICOM_image_Preproc_.ipynb
02_Pneumonia_classification.ipynb
03_Pneumonia_Boundbox.ipynb
04_Pneumonia_Cam.ipynb

🔬 Results

Pneumonia classification using ResNet models.

Bounding box localization of affected lung regions.

Grad-CAM heatmaps providing model interpretability.

Clean visualization workflow adapted for radiology projects.

Author

Miloš Stanisljevic
🎓 Radiologic Technologist (MTRA) | AI & Digital Healthcare Enthusiast
💡 Focus: Medical Imaging, Machine Learning, and Computer Vision,Medical Image Annotation

📫 Connect on Linkedin:linkedin.com/in/miloš-stanišljević-b1431b24a



🧭 Notes

This repository is part of my ongoing learning journey in AI for Medical Imaging.
Some notebooks are in the process of optimization and documentation (v1.0 – October 2025).

⭐ If you found this project interesting, give it a star on GitHub!
