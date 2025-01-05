# GAMED-Snake: Gradient-aware Adaptive Momentum Evolution Deep Snake Model for Multi-organ Segmentation
This is the code repository for the paper:


If you use any content of this repo for your work, please cite the following our paper:




## Introduction
Multi-organ segmentation is a critical yet challenging task due to complex anatomical backgrounds, blurred boundaries, and diverse morphologies. This study introduces the Gradient-aware Adaptive Momentum Evolution Deep Snake (GAMED-Snake) model, which establishes a novel paradigm for contour-based segmentation by integrating gradient-based learning with adaptive momentum evolution mechanisms. The GAMED-Snake model incorporates three major innovations: First, the Distance Energy Map Prior (DEMP) generates a pixel-level force field that effectively attracts contour points towards the true boundaries, even in scenarios with complex backgrounds and blurred edges. Second, the Differential Convolution Inception Module (DCIM) precisely extracts comprehensive energy gradients, significantly enhancing segmentation accuracy. Third, the Adaptive Momentum Evolution Mechanism (AMEM) employs cross-attention to establish dynamic features across different iterations of evolution, enabling precise boundary alignment for diverse morphologies. Experimental results on four challenging multi-organ segmentation datasets demonstrate that GAMED-Snake improves the mDice metric by approximately 2\% compared to state-of-the-art methods. 

![image](https://github.com/user-attachments/assets/c2a0de00-0ff2-4f6d-bc71-f50b699cd914)

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

```

## Training

### Import Dataset Path
All dataset paths for this project are set in the configuration files `sbd_snake.yaml` and `config.py`.  
Please modify the paths to match your actual dataset paths, set the training parameters, and then start model training.

### Start Training
```bash
python train_net.py --cfg_file configs/sbd_snake.yaml model sbd_snake
```
## Evaluation

### Import Dataset Path
All dataset paths for this project are set in the configuration files`sbd_snake.yaml` and `config.py`.  
Please modify the paths to match your actual dataset paths to start model testing.

### Start testing
```bash

python test.py

```
