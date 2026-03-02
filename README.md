# 🧠 Liver Tumor Segmentation using U-Net, Segmentation Autoencoder (SegAE) & Denoising Autoencoder (DAE)

Deep Learning project implementing convolutional architectures for liver tumor segmentation on the **LiTS17 medical imaging dataset** available on Kaggle.

---

## 📌 Project Overview

This project explores semantic segmentation of liver tumors from CT scans using:

- ✅ Convolutional Autoencoder (CAE)
- ✅ Denoising Autoencoder (DAE)
- ✅ U-Net Architecture

The objective was to compare reconstruction-based approaches (CAE/DAE) with a fully supervised segmentation model (U-Net) and analyze qualitative outputs in NIfTI format.

---

## 🏗️ Model Architectures

### 🔹 1. Convolutional Autoencoder (CAE)
- Encoder-decoder CNN
- Trained using reconstruction loss (MSE)
- Learns compact latent representation of CT slices

### 🔹 2. Denoising Autoencoder (DAE)
- Noise injected into inputs
- Model trained to recover clean reconstruction
- Improves robustness

### 🔹 3. U-Net
- Fully convolutional encoder-decoder
- Skip connections for spatial feature preservation
- Optimized for medical segmentation tasks

---

## 📂 Repository Structure

```

├── Case 000 NIfTI/            # Sample NIfTI prediction outputs
│   ├── seg_ae_case_000.nii.gz
│   ├── unet_case_000.nii.gz
│
├── images/                     # Sample visualization outputs
├── 26100337_PA2_1.ipynb
├── 26100337_PA2_2.ipynb
├── 26100337_Overall_Results.json
├── .gitignore
└── README.md

````

---

## 🧪 Sample Outputs

Included:
- Segmentation outputs for **Case 000**
- NIfTI format predictions for AE and U-Net models

These were visualized using: **MITK Workbench (Medical Imaging Interaction Toolkit)**

**MITK** allows:
- Multi-planar reconstruction (axial, coronal, sagittal views)
- 3D surface rendering
- Overlay comparison between ground truth and predicted masks
- Opacity and label control for tumor boundary inspection

To visualize manually:

1. Open MITK Workbench.
2. Load the original CT volume.
3. Load the predicted `.nii/.nii.gz` segmentation file.
4. Adjust opacity or enable label overlay for comparison.

Refer to **MITK User Guide - PA2 Deep Learning.pdf** for more.

---

## 📊 Training

Models were trained using:

- Loss: Mean Squared Error (AE/DAE), Segmentation loss for U-Net
- Input: CT slices
- Output: Tumor mask predictions
- Dataset: LiTS17 (Liver Tumor Segmentation Challenge)

---

## 🛠️ Dependencies

```bash
pip install torch torchvision
pip install nibabel
pip install numpy matplotlib
````

---

## 🚀 How to Run

1. Open the Jupyter notebooks:

   * `26100337_PA2_1.ipynb`
   * `26100337_PA2_2.ipynb`

2. Ensure dataset paths are updated locally.

3. Run training / inference cells.

---

## 📈 Key Learnings

* Skip connections significantly improve segmentation performance.
* Reconstruction-based models struggle with fine tumor boundaries.
* U-Net outperforms AE/DAE in pixel-level accuracy.
* NIfTI handling is critical in 3D medical workflows.

---

## 📎 Notes

* Only sample NIfTI outputs are included for demonstration.
* Full dataset not included due to size constraints.
* Repository structured for academic + portfolio purposes.

---

## 👩‍💻 Author

**Maheen Raza**

Deep Learning & Medical Imaging Enthusiast

GitHub: [https://github.com/maheenrazza](https://github.com/maheenrazza)
