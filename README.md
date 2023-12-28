# Multi-scale Adaptive Residual Network Using Total Variation for Real Image Super-Resolution
**Multi-scale Adaptive Residual Network Using Total Variation for Real Image Super-Resolution** _(2020 IEEE International Conference on Consumer Electronics - Asia)_

Keon-Hee Ahn* , Jun-Hyuk Kim**, Jun-Ho Choi**, Jong-Seok Lee**

*Computer Science and Engineering, Ewha Womans University, Work done during an internship at Yonsei University. 

**School of Integrated Technology, Yonsei University

## Abstract 
Single image super-resolution (SISR) has developed fast for recent years. Most of the SISR models are trained and evaluated with simulated data where low-resolution (LR) images are generated from high-resolution (HR) images using pre-defined degradation. In contrast, real-world image super-resolution (RealSR) is more challenging since the process of obtaining LR images is formulated by complex degradation. To solve this problem, we propose the multi-scale adaptive real image super-resolution (MARS). Our model extracts complex features in the image and uses them for upscaling adaptively. Experimental results show that the proposed method can improve the quality of the super-resolved images in RealSR.

## Overview
![block_str](https://github.com/MaryAhn/Multi-scale-Adaptive-Residual-Network-Using-Total-Variation-for-Real-Image-Super-Resolution/assets/43198379/33ee4192-81a4-48bc-87af-269f22865d19)

Structure of the proposed residual block.

## Paper
[Paper link](https://ieeexplore.ieee.org/abstract/document/9276925)

## Code Description

### Requirements
- pytorch-gpu 
- numpy
- math
- os
- argparse
- copy
- queue
- threading
- importlib
- time
- cv2
- torch.nn
- torch.optim
- torch.nn.functional

### How To Use
'''
python get_sr.py --model=mdsr_mod5 --restore_path=your_directory\challenge\experiments\Track_1\model_200000.pth --input_path=your_directory\challenge\data\TestLRX2\TestLR --scale=2 --edsr_res_blocks=80 --output_path=your_directory\challenge\experiments\Track_1\results --cuda_device=0 --chop_forward 
'''

> --cuda_device=0: It is device selection in case of multiple GPU. If you have only one GPU, just set it to 0.
> --input_path, --output_path, --restore_path: You have to change 'your_directory' part in each argument to suit your environment.
> --scale: Upscaling factor. \times 2, \times 3, \times 4 are available. 
