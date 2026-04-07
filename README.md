# Adaptive Edge-aware Semantic Interaction Network (AESINet)

> **Official PyTorch implementation of the IEEE TGRS 2023 paper "Adaptive Edge-aware Semantic Interaction Network for Salient Object Detection in Optical Remote Sensing Images".**

## Authors

**Xiangyu Zeng**<sup>1</sup>, **Mingzhu Xu**<sup>1</sup>\*, **Yijun Hu**<sup>1</sup>, **Haoyu Tang**<sup>1</sup>, **Yupeng Hu**<sup>1</sup>, **Liqiang Nie**<sup>2</sup>


<sup>1</sup> `Shandong University`  
<sup>2</sup> `Harbin Institute of Technology (Shen Zhen)`  
\* Corresponding author

## Links


- **Paper**: [`IEEE Xplore`](https://doi.org/10.1109/TGRS.2023.3300317)
- **Code Repository**: [`GitHub`](https://github.com/iLearn-Lab/AESINet-TGRS)

---

## Table of Contents

- [Introduction](#introduction)
- [Highlights](#highlights)
- [Method / Framework](#method--framework)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Checkpoints / Models](#checkpoints--models)
- [Usage](#usage)
- [TODO](#todo)
- [Citation](#citation)
- [Contact](#contact)
- [License](#license)

---

## Introduction

This project is the official implementation of the paper **"Adaptive Edge-aware Semantic Interaction Network for Salient Object Detection in Optical Remote Sensing Images"**.


This project mainly addresses the challenge of **Salient Object Detection (SOD) in optical remote sensing images**.
- **Core Idea**：Enhance boundary localization and effectively fuse multi-scale semantic information by introducing an adaptive edge-aware semantic interaction mechanism.
- **This Repository Provides**：
  - Training and inference code based on VGG and ResNet backbones.
  - Complete pretrained models and trained checkpoint links.
  - Data processing scripts for generating dataset path list files.


### Example Description


We present **AESINet**, a framework for **Salient Object Detection (SOD) in Optical Remote Sensing Images**.  
Our method addresses **accurate boundary localization** by introducing **adaptive edge-aware semantic interaction**.  
This repository provides the official implementation, pretrained checkpoints, and data processing scripts.

---

## Highlights

- Supports **salient object detection in remote sensing images**.
- Provides implementations with both **VGG** and **ResNet** backbone networks.
- Includes an adaptive edge-aware module to effectively handle targets in complex remote sensing backgrounds.

---

## Method / Framework

AESINet aims to improve detection performance through semantic interaction and edge-aware modules.

### Framework Figure

![Framework](./assets/framework.png)

**Figure 1.** Overall framework of AESINet.

---

## Project Structure

```text
.
├── assets/                # Images and framework diagrams
├── generateTrainList.py   # Script to generate training set path list
├── generateTestList.py    # Script to generate test set path list
├── main.py                # Main execution script (example)
├── models/                # AESINet model implementations (ResNet & VGG versions)
├── README.md
└── requirements.txt
```

---

## Installation

### 1. Clone the repository

```bash
git clone [https://github.com/iLearn-Lab/AESINet-TGRS.git](https://github.com/iLearn-Lab/AESINet-TGRS.git)
cd AESINet-TGRS
```

### 2. Create environment

```bash
python -m venv .venv
source .venv/bin/activate   # Linux / Mac
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

---

## Checkpoints / Models

| Model | Link | Password |
|---|---|---|
| **AESINet-V (VGG)** | [Baidu Drive](https://pan.baidu.com/s/1Xo97lQF4TS2jak9v8iU8jA?pwd=qegm) | qegm |
| **AESINet-R (ResNet)** | [Baidu Drive](https://pan.baidu.com/s/1gYW9qOjR0YjU5R4dCN9Hfg?pwd=tj25) | tj25 |
| **Pretrained (VGG & ResNet)** | [Baidu Drive](https://pan.baidu.com/s/18k9e3YcxK1rTY8A_WajTyg?pwd=lb8l) | lb8l |

Please place the downloaded models into the project directory and modify the corresponding `path` in the code.

---

## Usage

### 1. Data Preparation
First, download the dataset and use the following scripts to generate `.txt` path list files:
```bash
python generateTrainList.py
python generateTestList.py
```
**Note**：Please ensure that the dataset paths are correctly configured in the code.

### 2. Training
```bash
python main.py --mode=train
```

### 3. Testing
```bash
python main.py --mode=test
```

---

## TODO

- [x] Initial release of ResNet and VGG codes.
- [x] Release model checkpoints.
- [ ] Improve code readability and documentation.

---

## Citation

```bibtex
@ARTICLE{10198281,
  author={Zeng, Xiangyu and Xu, Mingzhu and Hu, Yijun and Tang, Haoyu and Hu, Yupeng and Nie, Liqiang},
  journal={IEEE Transactions on Geoscience and Remote Sensing}, 
  title={Adaptive Edge-Aware Semantic Interaction Network for Salient Object Detection in Optical Remote Sensing Images}, 
  year={2023},
  volume={61},
  number={},
  pages={1-16},
  doi={10.1109/TGRS.2023.3300317}}
```

---

## Contact

If you have any questions, please contact the authors via email: z15264367990@163.com

---

## License

This project is released under the Apache License 2.0.
