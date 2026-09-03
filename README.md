<div align="center">
  
# Point Coupling Model (PCM)

**This repo is the official project repository of the paper *Point Coupling Model: A hybrid segmentation architecture of sparse window attention and State-Space Modeling* (Accepted by Pattern Recognition).**

[![Paper](https://img.shields.io/badge/Paper-Pattern_Recognition-blue)](https://doi.org/10.1016/j.patcog.2026.114814) 
[![Code](https://img.shields.io/badge/Code-PyTorch-orange)](#) 
[![Model](https://img.shields.io/badge/Model-Releases-green)](https://github.com/PointCouplingMode/PCM/releases)

</div>

## 📢 Highlights / News
- **[2026/08]**: Our paper PCM is accepted by **Pattern Recognition**! 🎉🎉🎉 The online version is available now.
- **[2026/08]**: We released the source code and pre-trained model weights for PCM. If you have any questions related to our work, please feel free to open an issue.

---

## 📑 Overview
- [Citation](#-citation)
- [Installation](#-installation)
- [Data Preparation](#-data-preparation)
- [Quick Start](#-quick-start)
- [Model Zoo](#-model-zoo)

---

## 🖊️ Citation

If you find PCM useful to your research, please cite our work as an acknowledgment. (੭ˊ꒳​ˋ)੭✧

```bibtex
@article{huang2026pcm,
    title={Point Coupling Model: A hybrid segmentation architecture of sparse window attention and State-Space Modeling},
    author={Huang, Wenhao and Wang, Lei and Wang, Wei and Zhou, Xiaolong},
    journal={Pattern Recognition},
    year={2026},
    doi={10.1016/j.patcog.2026.114814},
    url={[https://doi.org/10.1016/j.patcog.2026.114814](https://doi.org/10.1016/j.patcog.2026.114814)}
}

```` 
## 🛠️ Installation
Requirements
The code has been tested with Python 3.12 and PyTorch. We highly recommend using Anaconda to manage your environment.

```Bash
# 1. Clone the repository
git clone [https://github.com/PointCouplingMode/PCM.git](https://github.com/PointCouplingMode/PCM.git)
cd PCM

# 2. Create a virtual environment
conda create -n pcm_env python=3.12 -y
conda activate pcm_env

# 3. Install other dependencies
pip install -r Requirements.txt


```` 
## 🗂️ Data Preparation
Our model is evaluated on S3DIS and ScanNetV2 datasets. Please organize the dataset files as follows:
```Bash
PCM/
└── data/
    ├── s3dis/
    └── scannetv2/
```` 
## 🚀 Quick Start
Pre-trained Models
Download the pre-trained checkpoints from our GitHub Releases and place them in the ./checkpoints/ directory.

Training
To train the PCM model from scratch on the dataset, run:
```Bash
# Example running script for S3DIS training
python train.py --dataset s3dis --config configs/s3dis.yaml
```` 
Evaluation
To evaluate the pre-trained model, run:
```Bash
# Example running script for evaluation
python evaluate.py --dataset s3dis --MODEL ./MODEL/s3dis.pth
```` 

## 📦 Model Zoo
Below are the pre-trained models provided in this repository.

| Model | Benchmark | Val mIoU |                                    Config                                    | Checkpoint |                                         Exp Record                                         |
| :---: | :---: | :---: |:----------------------------------------------------------------------------:| :---: |:------------------------------------------------------------------------------------------:|
| **PCM** | S3DIS | 79.33% | [config](https://github.com/PointCouplingMode/PCM/blob/main/configs/s3dis/s3dis.yaml)  | [Download](https://github.com/PointCouplingMode/PCM/releases) |   [link](https://github.com/PointCouplingMode/PCM/raw/main/tools/exp/default/ExpRecord/s3dis.log)   |
| **PCM** | ScanNetV2 | 79.24% | [config](https://github.com/PointCouplingMode/PCM/blob/main/configs/scannet/semseg-pt-v3m1-0-base.yaml)  | [Download](https://github.com/PointCouplingMode/PCM/releases) | [link](https://github.com/PointCouplingMode/PCM/raw/main/tools/exp/default/ExpRecord/scannetv2.log) |

(Note: Download the weights and place them in the ./checkpoints/ folder.)

Acknowledgments: This codebase is heavily inspired by excellent open-source projects like Pointcept and Point Transformer V3. We thank the authors for their great contributions to the community.