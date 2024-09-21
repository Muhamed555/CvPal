# CvPal 🖼️

<div align="center">

![CvPal Logo](assets/cvpal.png)

[![PyPI version](https://badge.fury.io/py/cvpal.svg)](https://badge.fury.io/py/cvpal)
[![License](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1Q_gYCQv85ImulAPXgQ1qOa_HGA7aytec?usp=sharing)

[![Documentation](https://img.shields.io/badge/Documentation-📚-blue)](https://github.com/Muhamed555/CvPal/tree/main/documentation)

</div>

## 🌟 Introduction

Welcome to **CvPal** - Your Ultimate Computer Vision Companion! 🚀

**CvPal** is a cutting-edge Python package designed to empower Computer Vision engineers worldwide. Our mission is to streamline image operations and dataset management, allowing you to focus on what truly matters: building and optimizing your machine learning pipelines.

🏆 **Proudly Sponsored by VisionFullSpace** 🏆

## 🎯 Features

- 🔄 **Dataset Merging**: Seamlessly combine datasets with multiple attributes
- 🗑️ **Label Removal**: Effortlessly remove specific labels from your dataset
- 📊 **Label Occurrence Counting**: Accurately track label frequencies
- 📝 **Dataset Reporting**: Generate comprehensive reports on your dataset
- 🔌 **Easy Integration**: Smoothly integrate with existing ML pipelines
- 📚 **Comprehensive Documentation**: Detailed guides for all features

## 🆕 Coming Soon: AI-Powered Dataset Creation

🎉 We're thrilled to announce our upcoming feature: Create entire datasets with just a prompt! Stay tuned for this game-changing addition to CvPal.

## 📁 Dataset Folder Structure

For optimal performance, please structure your dataset folder as follows:

```
folder/
├── train/
│   ├── images/
│   └── labels/
├── test/
│   ├── images/
│   └── labels/
└── valid/
    ├── images/
    └── labels/
```

For TXT format datasets, include a `data.yaml` config file:

```
folder/
└── data.yaml
```

Example `data.yaml`:

```yaml
names:
  - Old_Paper
  - Rock
  - Scissors
nc: 3
roboflow:
  license: Private
  project: rock-paper-scissors-sxsw
  url: https://universe.roboflow.com/roboflow-58fyf/rock-paper-scissors-sxsw/dataset/14
  version: 14
  workspace: roboflow-58fyf
test: ../test/images
train: Rock-Paper-Scissors-SXSW-14/train/images
val: Rock-Paper-Scissors-SXSW-14/valid/images
```

## 🚀 Installation

Install CvPal with a simple pip command:

```bash
pip install cvpal==0.0.2
```

## 🔧 Example Usage

```python
from cvpal import CvPal

cp = CvPal()

# Read data from the specified directory
cp.read_data("/content/Rock-Paper-Scissors-SXSW-14", data_type="txt")

# Generate a comprehensive report on the dataset
cp.report()
```

## 📊 Supported Models and Formats

| Model Name | Supported Format | Support in Package | Detection | Segmentation |
|------------|------------------|---------------------|-----------|--------------|
| YOLOv5-v10 | TXT & YAML config | ✅ | ✅ | ✅ |
| YOLOv3-v4 | Darknet TXT | ❌ | ❌ | ❌ |
| EfficientDet | Pytorch JSON annotations | ❌ | ❌ | ❌ |
| Detectron 2 | JSON annotations | ❌ | ❌ | ❌ |
| Segmentation Models | XML format | ❌ | ❌ | ❌ |
| TensorFlow Object Detection | Binary format | ❌ | ❌ | ❌ |
| Fine-tune PaliGemma | JSONL annotations | ❌ | ❌ | ❌ |
| Apple's CreateML | Proprietary JSON format | ❌ | ❌ | ❌ |
| Turi Create tools | Proprietary JSON format | ❌ | ❌ | ❌ |

## 🤝 Call for Contributions

Join the CvPal community and make a global impact! We welcome contributions of all sizes:

- 🐛 Bug fixes and enhancements
- 📝 Documentation improvements
- 🎨 UI/UX enhancements
- 🧪 New feature development

To contribute major changes, please reach out through our mailing list first.

Other ways to contribute:
- 🔍 Help triage issues
- 📚 Create tutorials and presentations
- 🕵️ Review pull requests

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE.txt) file for details.

---

<div align="center">
  <strong>Powered by VisionFullSpace</strong><br>
  Empowering Computer Vision Worldwide
</div>
