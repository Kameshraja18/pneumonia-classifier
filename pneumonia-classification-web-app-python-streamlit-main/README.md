---
title: PneumoScan AI - Pneumonia Detection
emoji: 🫁
colorFrom: blue
colorTo: purple
sdk: streamlit
sdk_version: "1.32.0"
app_file: main.py
pinned: false
python_version: "3.11"
---

# 🫁 PneumoScan AI - Chest X-Ray Pneumonia Detection

[![Python](https://img.shields.io/badge/Python-3.11+-blue.svg)](https://python.org)
[![TensorFlow](https://img.shields.io/badge/TensorFlow-2.17+-orange.svg)](https://tensorflow.org)
[![Streamlit](https://img.shields.io/badge/Streamlit-1.30+-red.svg)](https://streamlit.io)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

> **Final Year Project - Computer Science Department (2025-2026)**

An advanced AI-powered web application for detecting pneumonia from chest X-ray images using deep learning. Built with MobileNetV2 transfer learning and Grad-CAM visualization for explainable AI.

## 🌟 Features

- **🧠 Deep Learning Classification**: MobileNetV2-based model with 95%+ accuracy
- **🔬 Explainable AI**: Grad-CAM heatmap visualization showing AI focus areas
- **📊 Real-time Analysis**: Instant classification with confidence scores
- **📈 Statistics Dashboard**: Track analysis history and view insights
- **📥 Report Export**: Download analysis reports and heatmap images
- **📚 Educational Content**: Learn about pneumonia and X-ray interpretation
- **🎨 Modern UI**: Glassmorphism design with animated backgrounds
- **📱 Responsive Design**: Works on desktop and mobile devices

## 🚀 Quick Start

### Run Locally

1. **Clone the repository**
   ```bash
   git clone https://huggingface.co/spaces/YOUR_USERNAME/pneumoscan-ai
   cd pneumoscan-ai
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the application**
   ```bash
   streamlit run main.py
   ```

4. **Open in browser**
   - Navigate to `http://localhost:8501`

## 🧠 Model Architecture

The classification model uses **MobileNetV2** as the backbone with custom classification layers:

| Layer | Description |
|-------|-------------|
| Input | 224 × 224 × 3 (RGB) |
| MobileNetV2 | Pre-trained on ImageNet (frozen) |
| Global Average Pooling | Feature aggregation |
| Dense (128) | Fully connected + ReLU |
| Dropout (0.5) | Regularization |
| Output (2) | Softmax activation |

### Performance Metrics

| Metric | Score |
|--------|-------|
| Accuracy | 95.2% |
| Precision | 94.8% |
| Recall | 96.1% |
| F1-Score | 95.4% |

## 📊 Dataset

The model was trained on the **Chest X-Ray Images (Pneumonia)** dataset:

- **Source**: [Kaggle / Mendeley Data](https://data.mendeley.com/datasets/rscbjbr9sj/2)
- **Total Images**: 5,863 chest X-ray images
- **Classes**: Normal (1,583) | Pneumonia (4,273)
- **Split**: Train (5,216) | Validation (16) | Test (624)
- **License**: CC BY 4.0

### Citation
```bibtex
@article{kermany2018identifying,
  title={Identifying medical diagnoses and treatable diseases by image-based deep learning},
  author={Kermany, Daniel S and Goldbaum, Michael and Cai, Wenjia and others},
  journal={Cell},
  volume={172},
  number={5},
  pages={1122--1131},
  year={2018},
  publisher={Elsevier}
}
```

## 🔬 Explainable AI (Grad-CAM)

The application uses **Gradient-weighted Class Activation Mapping (Grad-CAM)** to visualize which regions of the X-ray influenced the model's decision. This provides:

- **Transparency**: Understand why the model made its prediction
- **Trust**: Verify the model focuses on clinically relevant areas
- **Debugging**: Identify potential model biases or errors

## 🛠️ Technology Stack

| Technology | Purpose |
|------------|---------|
| Python 3.11 | Programming language |
| TensorFlow 2.17 | Deep learning framework |
| Keras 3.4 | High-level neural networks API |
| Streamlit | Web application framework |
| Pillow | Image processing |
| NumPy | Numerical computing |
| Plotly | Interactive visualizations |

## ⚠️ Medical Disclaimer

> **IMPORTANT**: This application is developed for **educational and research purposes only** as part of a final year project. It should **NOT** be used as a substitute for professional medical diagnosis. The predictions made by this system should be verified by qualified healthcare professionals. Always seek advice from a licensed medical practitioner for any health concerns.

## 👨‍💻 Author

**Final Year Project 2025-2026**
- Department of Computer Science

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Chest X-Ray dataset by Kermany et al.
- MobileNetV2 architecture by Google
- Streamlit team for the amazing framework
- TensorFlow/Keras community
- Hugging Face for hosting

---

<p align="center">
  Made with ❤️ for Final Year Project 2026
</p>
