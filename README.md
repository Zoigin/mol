# 3D Equivariant Diffusion for Target-Aware Molecule Generation and Affinity Prediction (Using for test VFDiff result)

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://github.com/guanjq/targetdiff/blob/main/LICIENCE)


This repository is the official implementation of 3D Equivariant Diffusion for Target-Aware Molecule Generation and Affinity Prediction (ICLR 2023). [[PDF]](https://openreview.net/pdf?id=kJqXEPXMsE0) 

<p align="center">
  <img src="assets/overview.png" /> 
</p>

## Installation

### Dependency

The code has been tested in the following environment:


| Package           | Version   |
|-------------------|-----------|
| Python            | 3.8       |
| PyTorch           | 1.13.1    |
| CUDA              | 11.6      |
| PyTorch Geometric | 2.2.0     |
| RDKit             | 2022.03.2 |

### Install via Conda and Pip
```bash
conda create -n targetdiff python=3.8
conda activate targetdiff
conda install pytorch pytorch-cuda=11.6 -c pytorch -c nvidia
conda install pyg -c pyg
conda install rdkit openbabel tensorboard pyyaml easydict python-lmdb -c conda-forge

# For Vina Docking
pip install meeko==0.1.dev3 scipy pdb2pqr vina==1.2.2 
python -m pip install git+https://github.com/Valdes-Tresanco-MS/AutoDockTools_py3
```
The code should work with PyTorch >= 1.9.0 and PyG >= 2.0. You can change the package version according to your need.

### Test for VFNet
```bash
unzip targetdiff.zip
```
Please move metrics_-1.pt in **Supplementary Materials** to 
```bash
./targetdiff/
```
run the evaluation file
```bash
cd targetdiff
python evaluate_diffusion.py
```


## Citation
```
@inproceedings{guan3d,
  title={3D Equivariant Diffusion for Target-Aware Molecule Generation and Affinity Prediction},
  author={Guan, Jiaqi and Qian, Wesley Wei and Peng, Xingang and Su, Yufeng and Peng, Jian and Ma, Jianzhu},
  booktitle={International Conference on Learning Representations},
  year={2023}
}
```
