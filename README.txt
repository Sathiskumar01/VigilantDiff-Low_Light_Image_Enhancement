# PRO2DIFF and VigilantDiff

## Overview
This repository contains two main components:
1. **PRO2DIFF**: A diffusion-based model for multi-object tracking (MOT)
2. **VigilantDiff**: A low-light image enhancement system with human detection

## Installation

### Requirements
- Python 3.8+
- PyTorch 1.12+
- torchvision
- Additional packages:
  ```bash
  pip install numpy pandas Pillow tqdm streamlit opencv-python ultralytics


1)PRO2DIFF (Multi-Object Tracking)
	Training Setup
		1.Dataset structure:
			dancetrack0001/
			├── img1/        # Frame images (0001.jpg, 0002.jpg, etc.)
			└── gt/
    	     			└── gt.txt   # Ground truth bounding boxes

		2.Run training:
			python train_pro2diff.py

	Key Features

		1.ResNet50 backbone with custom prediction heads

		2.Generalized IoU loss for bounding box regression

		3.Diffusion-based denoising refinement

2)VigilantDiff (Low-Light Enhancement)

	1.Launch the web interface:

		bash: streamlit run vigilant_diff.py

	2.In the browser:

		Upload low-light images

		View enhanced results with human detections

	3.Key Components
		1.UNet-based image enhancement

		2.YOLOv5 human detection

		3.Interactive web interface

File Structure

├── train_pro2diff.py      # PRO2DIFF training
├── vigilant_diff.py       # VigilantDiff app
├── models/                # Model definitions
└── checkpoints/           # Pretrained weights