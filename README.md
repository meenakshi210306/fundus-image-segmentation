# 🔬 Fundus Image Segmentation

> Deep learning based retinal fundus image segmentation using Improved U-Net architecture with transformer blocks.

---

## 📌 Project Overview

This project focuses on **automatic segmentation of blood vessels in retinal fundus images** using a deep learning model. Early and accurate detection of retinal vessel patterns is critical for diagnosing diseases like:

- Diabetic Retinopathy
- Glaucoma
- Hypertensive Retinopathy
- Age-related Macular Degeneration

The model is based on an **Improved U-Net architecture enhanced with Transformer blocks**, combining the spatial precision of U-Net with the global context understanding of Transformer attention mechanisms.

---

## 🧠 Model Architecture

The architecture is an enhanced version of the classic **U-Net**, with the following key improvements:

- **Encoder**: Convolutional blocks with skip connections
- **Bottleneck**: Transformer blocks for global attention
- **Decoder**: Upsampling with skip connection fusion
- **Output**: Binary segmentation mask (vessel / non-vessel)

```
Input Image
    ↓
Encoder (Conv Blocks)
    ↓
Transformer Bottleneck (Self-Attention)
    ↓
Decoder (UpConv + Skip Connections)
    ↓
Segmentation Mask
```

---

## 📁 Project Structure

```
fundus-image-segmentation/
│
├── fundus_segmentation.ipynb   # Main notebook (training + evaluation)
├── requirements.txt            # Python dependencies
├── README.md                   # Project documentation
│
├── data/                       # Dataset (not included - see below)
│   ├── images/                 # Original fundus images
│   ├── 1st_manual/             # Ground truth masks (1st annotator)
│   └── 2nd_manual/             # Ground truth masks (2nd annotator)
│
└── results/                    # Output predictions
    └── sample_predictions/
```

---

## 📊 Dataset

This project uses the **[DRIVE Dataset](https://drive.grand-challenge.org/)** (Digital Retinal Images for Vessel Extraction).

| Property | Details |
|----------|---------|
| Total Images | 40 retinal fundus images |
| Training Set | 20 images |
| Test Set | 20 images |
| Image Size | 565 × 584 pixels |
| Annotations | Two manual segmentation masks per image |
| Format | TIFF / PNG |

> ⚠️ **Note:** The dataset is **not included** in this repository due to licensing. Download it from the [DRIVE Challenge website](https://drive.grand-challenge.org/) and place it in the `data/` folder.

---

## ⚙️ Installation

### 1. Clone the Repository

```bash
git clone https://github.com/meenakshi210306/fundus-image-segmentation.git
cd fundus-image-segmentation
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. Download the Dataset

- Visit [DRIVE Challenge](https://drive.grand-challenge.org/)
- Download and extract into the `data/` folder

---

## 🚀 How to Run

Open and run the Jupyter notebook:

```bash
jupyter notebook fundus_segmentation.ipynb
```

The notebook includes:
1. Data loading and preprocessing
2. Model architecture definition
3. Model training
4. Evaluation and visualization of predictions

---

## 📈 Sample Results

Below are sample outputs comparing the original image, ground truth mask, and model prediction:

| Input Image | Ground Truth | Prediction |
|:-----------:|:------------:|:----------:|
| Fundus Image | Manual Annotation | Model Output |

> Sample prediction images will be added after training is complete.

---

## 📦 Requirements

```
tensorflow>=2.10
numpy
opencv-python
matplotlib
scikit-learn
Pillow
tqdm
```

---

## 📚 References

- [U-Net: Convolutional Networks for Biomedical Image Segmentation](https://arxiv.org/abs/1505.04597) — Ronneberger et al., 2015
- [Attention Is All You Need](https://arxiv.org/abs/1706.03762) — Vaswani et al., 2017
- [DRIVE Dataset](https://drive.grand-challenge.org/) — Staal et al., 2004
- [TransUNet](https://arxiv.org/abs/2102.04306) — Chen et al., 2021
- [A Systematic Review on Fundus Image-Based DR Detection](https://doi.org/10.1109/ACCESS.2024.3427394) — Ikram et al., 2024
- [A Review of Retinal Vessel Segmentation for Fundus Image Analysis](https://doi.org/10.1016/j.engappai.2023.107454) — Qin & Chen, 2024

---

## 👩‍💻 Author

**Meenakshi** — [@meenakshi210306](https://github.com/meenakshi210306)

---

## 📄 License

This project is for academic and educational purposes.
