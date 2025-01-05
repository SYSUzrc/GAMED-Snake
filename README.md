# GAMED-Snake: Gradient-aware Adaptive Momentum Evolution Deep Snake Model for Multi-organ Segmentation
This is the code repository for the paper:


If you use any content of this repo for your work, please cite the following our paper:




## Introduction
Multi-organ segmentation is a critical yet challenging task due to complex anatomical backgrounds, blurred boundaries, and diverse morphologies. This study introduces the Gradient-aware Adaptive Momentum Evolution Deep Snake (GAMED-Snake) model, which establishes a novel paradigm for contour-based segmentation by integrating gradient-based learning with adaptive momentum evolution mechanisms. The GAMED-Snake model incorporates three major innovations: First, the Distance Energy Map Prior (DEMP) generates a pixel-level force field that effectively attracts contour points towards the true boundaries, even in scenarios with complex backgrounds and blurred edges. Second, the Differential Convolution Inception Module (DCIM) precisely extracts comprehensive energy gradients, significantly enhancing segmentation accuracy. Third, the Adaptive Momentum Evolution Mechanism (AMEM) employs cross-attention to establish dynamic features across different iterations of evolution, enabling precise boundary alignment for diverse morphologies. Experimental results on four challenging multi-organ segmentation datasets demonstrate that GAMED-Snake improves the mDice metric by approximately 2\% compared to state-of-the-art methods. 

## Environment Setup
You can set up your own conda virtual environment by running the commands below.

```bash
# create a clean conda environment from scratch
conda create --name dymultidepth python=3.7
conda activate GAMEDSnake

# install pip
conda install ipython
conda install pip

# install required packages
pip install -r requirements.txt

