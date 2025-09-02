# <span style="color:#e74c3c; font-weight:bold">DBF-Net: Dual-Branch Fusion Network for Medical Image Segmentation</span>

[![Paper](https://img.shields.io/badge/Paper-DBF--Net-blue)](https://ieeexplore.ieee.org/abstract/document/11084704)

This repository provides the official implementation of <span style="color:#e67e22; font-weight:bold">DBF-Net</span>, a novel dual-branch fusion architecture designed for accurate and efficient medical image segmentation. The network combines <span style="color:#3498db; font-weight:bold">global context modeling</span> and <span style="color:#2ecc71; font-weight:bold">local detail preservation</span> through two complementary branches, achieving state-of-the-art performance on multiple medical imaging datasets.

---

## <span style="color:#d35400; font-weight:bold">🔍 Overview</span>

Medical image segmentation requires capturing <span style="color:#2980b9; font-weight:bold">global semantic information</span> while maintaining <span style="color:#27ae60; font-weight:bold">local structural details</span>. Conventional CNN-based methods struggle with long-range dependencies, while Transformer-based models are computationally expensive.

<span style="color:#e67e22; font-weight:bold">DBF-Net</span> introduces:
- <span style="color:#f39c12; font-weight:bold">Dual-Branch Encoder</span>  
  - <span style="color:#2ecc71">Local Branch:</span> Captures fine-grained local features using CNN layers.  
  - <span style="color:#3498db">Global Branch:</span> Extracts long-range dependencies using a lightweight attention mechanism.  
- <span style="color:#f39c12; font-weight:bold">Feature Fusion Module (FFM):</span> Efficiently integrates features from both branches.  
- <span style="color:#f39c12; font-weight:bold">Decoder:</span> Recovers spatial resolution with skip connections and progressive upsampling.

---

## <span style="color:#d35400; font-weight:bold">🏗 Project Structure</span>

```
├── builders/        # Model building scripts
├── dataset/         # Data loading and preprocessing
├── libs/            # Core library functions
├── model/           # DBF-Net implementation
├── utils/           # Utilities (metrics, visualization, etc.)
├── train.py         # Training pipeline
├── test.py          # Evaluation and inference
└── README.md        # Project documentation
```



---

## <span style="color:#d35400; font-weight:bold">📄 Paper Information</span>

**Title:** <span style="color:#e74c3c; font-weight:bold">DBF-Net: Dual-Branch Fusion Network for Medical Image Segmentation</span>  
**Authors:** [Your Names Here]  
**Journal/Conference:** [To be added]  
**DOI:** [To be added]  

---

## <span style="color:#d35400; font-weight:bold">⚡ Features</span>

✔ <span style="color:#2ecc71; font-weight:bold">Dual-branch architecture</span> for <span style="color:#2980b9">local + global feature learning</span>  
✔ <span style="color:#f1c40f; font-weight:bold">Feature Fusion Module</span> for multi-scale context integration  
✔ Outperforms **U-Net**, **TransUNet**, and **Swin-UNet** in Dice and HD95  
✔ Applicable to <span style="color:#9b59b6; font-weight:bold">2D medical image segmentation tasks</span>  

---

## <span style="color:#d35400; font-weight:bold">🛠 Requirements</span>

- Python ≥ 3.8  
- PyTorch ≥ 1.8  
- torchvision  
- numpy  
- SimpleITK  
- tqdm  

Install dependencies:
```bash
pip install -r requirements.txt


<span style="color:#d35400; font-weight:bold">📂 Dataset</span>

Synapse multi-organ CT dataset

ACDC cardiac MRI dataset

Other datasets as needed

Dataset preprocessing instructions can be found in dataset/README.md.

<span style="color:#d35400; font-weight:bold">🚀 Usage</span>
1. <span style="color:#3498db; font-weight:bold">Train the model</span>
python train.py

2. <span style="color:#3498db; font-weight:bold">Test the model</span>
python test.py

<span style="color:#d35400; font-weight:bold">🏆 Results</span>
Synapse Dataset
| Method                                                       | DSC ↑     | HD95 ↓    |
| ------------------------------------------------------------ | --------- | --------- |
| <span style="color:#7f8c8d">U-Net</span>                     | 76.85     | 39.70     |
| <span style="color:#2980b9">TransUNet</span>                 | 77.48     | 31.69     |
| <span style="color:#e74c3c; font-weight:bold">DBF-Net</span> | **79.XX** | **15.XX** |


<span style="color:#d35400; font-weight:bold">🔍 Citation</span>

If you find this work useful, please cite:
@article{dbfnet2025,
  title={DBF-Net: Dual-Branch Fusion Network for Medical Image Segmentation},
  author={...},
  journal={...},
  year={2025}
}
