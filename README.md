-# 🐾 Animal Vision System: Classification & Identification

[![Python](https://img.shields.io/badge/Python-3.8+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![TensorFlow](https://img.shields.io/badge/TensorFlow-2.0+-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)](https://www.tensorflow.org/)
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/YOUR_COLAB_LINK_HERE)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)

An advanced computer vision project focused on animal identification and breed classification. This repository features two primary systems: a **Dairy Cattle Breed Classifier** and a **Dog Facial Similarity Identification** engine.

---

## 🌟 Key Features

### 🐄 Cattle Breed Classification
- **Transfer Learning**: Utilizes pre-trained **MobileNetV2** for high-accuracy feature extraction with minimal computational overhead.
- **Breed Detection**: Specifically optimized for identifying dairy cattle breeds like **Gir** and **Sahiwal**.
- **Automated Pipeline**: Includes end-to-end workflows from image scraping to model deployment.

### 🐕 Dog Facial Identification
- **Face Similarity Matching**: Calculates similarity scores between dog faces to determine if they belong to the same individual.
- **Stanford Dogs Integration**: Uses the comprehensive Stanford Dogs dataset for robust model training and testing.
- **Interactive UI**: Features an **IPyWidgets-based interface** within Jupyter Notebooks for real-time comparison and visualization.

### 🛠️ Data Infrastructure
- **Multi-Source Scraping**: Integrated `icrawler` workflows to download images from Bing, Google, and Baidu.
- **Intelligent Splitting**: Automated scripts to organize raw data into structured Train, Validation, and Test directories.
- **Augmentation**: Implements real-time data augmentation (flips, rotations, zooms) to enhance model generalization.

---

## 🏗️ Project Structure

```bash
Animal-Vision-System/
├── cattle_model.ipynb         # Cattle classification training & evaluation
├── dog_face_detection_V1.ipynb # Dog facial identification & interactive matching
├── datasets/                  # (Generated) Local storage for training data
└── README.md                  # Project documentation
```

---

## 🚀 Getting Started

### Prerequisites
- Python 3.8 or higher
- GPU recommended for training (e.g., NVIDIA T4 in Google Colab)

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/Rak2k6/Animal-Vision-System---Classification-Identification.git
   cd Animal-Vision-System---Classification-Identification
   ```

2. Install required dependencies:
   ```bash
   pip install tensorflow icrawler scikit-learn matplotlib pillow ipywidgets
   ```

---

## 📊 Methodology

### 1. Data Acquisition
The system leverages the `icrawler` library to build custom datasets. For example, the cattle model uses search keywords like "Murrah" and "Gir Cattle" to pull diverse samples across global search engines.

### 2. Model Architecture
- **Base**: MobileNetV2 (Frozen weights from ImageNet).
- **Top**: Global Average Pooling -> Dropout (0.3) -> Dense (Sigmoid/Softmax).
- **Optimizer**: Adam.
- **Loss**: Binary/Categorical Crossentropy.

### 3. Training & Validation
Models are trained with **Early Stopping** to prevent overfitting, monitoring validation loss to restore the best performing weights.

---

## 🖥️ Usage

### Cattle Classification
Open `cattle_model.ipynb` and run the cells sequentially to:
1. Scrape images for desired breeds.
2. Split data into directories.
3. Train the MobileNetV2 model.
4. Save the model as `.h5` for deployment.

### Dog Face Identification
Open `dog_face_detection_V1.ipynb` to:
1. Download and extract the Stanford Dogs dataset.
2. Run the interactive comparison widget.
3. Upload two dog images to see their similarity score and identification decision.

---

## 📜 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🤝 Contributing
Contributions are welcome! Please feel free to submit a Pull Request.

---
*Developed by [Rak2k6](https://github.com/Rak2k6)*
