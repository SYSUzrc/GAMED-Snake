#  GAMED-Snake

This is the code repository for the paper:
> **GAMED-Snake: Gradient-aware Adaptive Momentum Evolution Deep Snake Model for Multi-organ Segmentation**
>
> [Ruicheng Zhang](https://github.com/SYSUzrc), Haowei Guo, [Zeyu Zhang](https://steve-zeyu-zhang.github.io/), Puxin Yan and [Shen Zhao](https://scholar.google.com.hk/citations?hl=zh-CN&user=U68XZOgAAAAJ&view_op=list_works&sortby=pubdate)\*
>
> \*Corresponding author
>
> <em><b>ICME 2025</b></em>
> 
> **[[arXiv]](https://arxiv.org/abs/2501.12844)** **[[Paper with Code]](https://paperswithcode.com/paper/gamed-snake-gradient-aware-adaptive-momentum)**

<center class ='img'>
<img title="(a) The workflow of GAMED-Snake consists of two stages: initialization of detection boxes and contour evolution. Taking the detection boxes as the initial contours, snake evolution process iteratively deforms them to match organ boundaries. (b) Semantic segmentation models based on pixel classification often struggle with complex multi-organ segmentation scenes, resulting in errors as illustrated in Fig. \ref{fig:image1}(b). In contrast, snake algorithms inherently avoid these issues, producing smooth and precise contours. (c) Improvement of GAMED-Snake over the SOTA approaches on MR\_AVBCE \cite{Zhao2023Attractive} and BTCV \cite{landman2015miccai} datasets." src="https://github.com/SYSUzrc/GAMED-Snake/blob/main/image1.png" width="100%">
</center>


## Citation

If you use any content of this repo for your work, please cite the following our paper:
```
@article{zhang2025gamed,
  title={GAMED-Snake: Gradient-aware Adaptive Momentum Evolution Deep Snake Model for Multi-organ Segmentation},
  author={Zhang, Ruicheng and Guo, Haowei and Zhang, Zeyu and Yan, Puxin and Zhao, Shen},
  journal={arXiv preprint arXiv:2501.12844},
  year={2025}
}
```

## Introduction
Multi-organ segmentation is a critical yet challenging task due to complex anatomical backgrounds, blurred boundaries, and diverse morphologies. This study introduces the Gradient-aware Adaptive Momentum Evolution Deep Snake (GAMED-Snake) model, which establishes a novel paradigm for contour-based segmentation by integrating gradient-based learning with adaptive momentum evolution mechanisms. The GAMED-Snake model incorporates three major innovations: First, the Distance Energy Map Prior (DEMP) generates a pixel-level force field that effectively attracts contour points towards the true boundaries, even in scenarios with complex backgrounds and blurred edges. Second, the Differential Convolution Inception Module (DCIM) precisely extracts comprehensive energy gradients, significantly enhancing segmentation accuracy. Third, the Adaptive Momentum Evolution Mechanism (AMEM) employs cross-attention to establish dynamic features across different iterations of evolution, enabling precise boundary alignment for diverse morphologies. Experimental results on four challenging multi-organ segmentation datasets demonstrate that GAMED-Snake improves the mDice metric by approximately 2\% compared to state-of-the-art methods. 

![image](https://github.com/user-attachments/assets/c2a0de00-0ff2-4f6d-bc71-f50b699cd914)

## Environment Setup
You can set up your own conda virtual environment by running the commands below.

```bash
# create a clean conda environment from scratch
conda create --name GAMEDSnake python=3.7
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
