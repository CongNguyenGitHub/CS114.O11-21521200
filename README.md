# Sign Language Detection Project

## Overview

This project aims to implement Sign Language Detection using a custom dataset consisting of 500 signs with over 3000 videos collected from YouTube and self-recordings. Each sign category should have a minimum of 5 videos. The approach is inspired by the paper "Word-level Deep Sign Language Recognition from Video: A New Large-scale Dataset and Methods Comparison" (Dongxu Li, 2020).

## Dataset

The custom dataset includes 500 signs with more than 3000 videos sourced from YouTube and self-recordings. Each sign category is represented by a folder containing a minimum of 5 videos.

## Methodology

The implementation is based on one of the four methods presented in the paper mentioned above. Additionally, the code implementation is influenced by the "Sign Language Detection using ACTION RECOGNITION with Python | LSTM Deep Learning Model" video by Renotte (2021).

1. **Data Augmentation:** Videos for training are augmented using shear, translate, and rotate methods (Tung, 2022).

2. **Background Removal:** YOLOv5 is used to obtain bounding boxes around the signers, and videos are cropped based on these bounding boxes to focus on the signer, enhancing model accuracy.

3. **Keypoint Extraction:** MediaPipe models (MediaPipe BlazePose GHUM 3D, Model Card Hand Tracking (Lite/Full) with Fairness Oct 2021) are utilized to extract keypoints from background-removed videos.

4. **LSTM Model:** Information from extracted keypoints is fed into a stacked 2-layer LSTM network for training.

5. **Evaluation:** Top-K evaluation metric is used to assess and comment on model performance.

## Usage

### Prerequisites

- Python 3.x
- Dependencies listed in `requirements.txt`

### Installation

```bash
pip install -r requirements.txt
