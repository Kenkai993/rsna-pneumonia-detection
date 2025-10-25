# RSNA Pneumonia Detection Project 🫁

This project demonstrates a complete AI pipeline for detecting and visualizing pneumonia in chest X-rays using the **RSNA Pneumonia Detection Challenge** dataset.
It was developed independently as part of my exploration of AI in medical imaging.
All code and experiments were written and tested manually.
It combines medical imaging preprocessing, model training, bounding box visualization, and Grad-CAM interpretability into a unified, reproducible workflow.



*Note:**  
> • This project was developed as a personal learning exercise to explore:  
>   – Medical image preprocessing  
>   – CNN classification  
>   – Model interpretability (Grad-CAM)  
> • Dataset: RSNA Pneumonia Detection Challenge (Kaggle, public DICOM).  
> • Paths are local and checkpoints are not included due to dataset licensing.

> **Reproducibility note:**  
> All file paths are kept local by design to maintain transparency of the experimental workflow.  
> The notebooks demonstrate the logic and results, but require adjusting paths to match  
> the user’s environment for full reproducibility.

---

## 📁 Project Structure
rsna-pneumonia-detection-challenge
│
├── 01_Dicom_image_Preproc.ipynb # DICOM loading & preprocessing
├── 02_Pneumonia_classification.ipynb # Model training & evaluation (PyTorch Lightning)
├── 03_Pneumonia_Boundbox.ipynb # Radiologist bounding box visualization
├── 04_Pneumonia_Cam.ipynb # Grad-CAM explainability (AI heatmap)

🧠 Model Performance Summary

| Metric | Value |
|:--------|:------:|
| **Validation Accuracy** | 0.8294 |
| **Validation AUROC** | 0.8936 |
| **Best Accuracy Checkpoint** | `logs/lightning_logs/version_5/checkpoints/best-acc-epoch=23-val_acc=0.8294-val_auroc=0.8840.ckpt` |
| **Best AUROC Checkpoint** | `logs/lightning_logs/version_5/checkpoints/best-auroc-epoch=25-val_acc=0.8171-val_auroc=0.8936.ckpt` |

These metrics demonstrate strong model performance on the validation set,  
showing reliable pneumonia detection and high interpretability via Grad-CAM heatmaps.

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

Click the link for an example image:
https://raw.githubusercontent.com/Kenkai993/rsna-pneumonia-detection/main/Pneumonia%20detection%20project/docs/BBOX_Pneumonia.png




4️⃣ Grad-CAM (Model Interpretability)

Visualizes AI model attention over the same chest X-ray

Compares human (radiologist) vs AI focus

Click the link for an example image:
https://raw.githubusercontent.com/Kenkai993/rsna-pneumonia-detection/main/Pneumonia%20detection%20project/docs/Heatmap_Pneumonia.png



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


🧩 Future Work
- Integrating automatic DICOM anonymization.
- Extending to MRI segmentation tasks.
- Experimenting with EfficientNet for improved performance.


🧩 Author
Milos Stanisljevic

Contact & Portfolio
GitHub: [milos-stanisljevic](https://github.com/milos-stanisljevic)  
LinkedIn: [Miloš Stanišljević](https://www.linkedin.com/in/miloš-stanišljević-b1431b24a/)

 
