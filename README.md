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
**Authors:** [Guoping Xu; Xiaming Wu; Wentao Liao; Xinglong Wu; Qing Huang; Chang Li]  
**Conference:** [2025 IEEE International Conference on Image Processing (ICIP)]  
**DOI:** [10.1109/ICIP55913.2025.11084704]  

---

## <span style="color:#d35400; font-weight:bold">🛠 Requirements</span>

- Python ≥ 3.8  
- PyTorch ≥ 1.8  
- numpy==1.26.4  
- timm==0.4.12
- ptflops
- imgaug

<span style="color:#d35400; font-weight:bold">📂 Dataset</span>
```

├── train  
├── dataset_train_list.txt  
├── dataset_val_list.txt 
└── dataset_test_list.txt             
```

<span style="color:#d35400; font-weight:bold">🚀 Usage</span>
1. <span style="color:#3498db; font-weight:bold">Train the model</span>
- python train.py

2. <span style="color:#3498db; font-weight:bold">Test the model</span>
- python test.py

<span style="color:#d35400; font-weight:bold">🏆 Results</span>
BUSI Dataset
| Method                                                       | DSC ↑     | HD ↓    |
| ------------------------------------------------------------ | --------- | --------- |
| <span style="color:#7f8c8d">U-Net</span>                     | 65.19±7.19     | 9.93±0.17     |
| <span style="color:#2980b9">DeepLabV3+</span>                 | 77.76±8.92     | 7.66±0.27     |
| <span style="color:#2980b9">LinkNet</span>                 | 72.70±9.77     | 72.70±9.77     |
| <span style="color:#2980b9">DBBS-Net</span>                 |9.34±9.43     | 8.05±0.32     |
| <span style="color:#2980b9">UNeXt</span>                 | 78.17±2.57     | 8.16±0.39      |
| <span style="color:#e74c3c; font-weight:bold">DBF-Net</span> | **81.05±10.44** | **7.35±0.27** |


<span style="color:#d35400; font-weight:bold">🔍 Citation</span>

If you find this work useful, please cite:
```
@INPROCEEDINGS{11084704,
  author={Xu, Guoping and Wu, Xiaming and Liao, Wentao and Wu, Xinglong and Huang, Qing and Li, Chang},
  booktitle={2025 IEEE International Conference on Image Processing (ICIP)}, 
  title={DBF-Net: A Dual-Branch Network with Feature Fusion for Ultrasound Image Segmentation}, 
  year={2025},
  volume={},
  number={},
  pages={211-216},
  keywords={Deep learning;Image segmentation;Ultrasonic imaging;Accuracy;Codes;Anatomical structure;Artificial neural networks;Breast cancer;Brachytherapy;Lesions;Image segmentation;ultrasound;feature fusion},
  doi={10.1109/ICIP55913.2025.11084704}}
```

