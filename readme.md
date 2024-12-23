# Unmanned Aerial Vehicle (UAV) Detection

This repository contains a YOLOv8-based model for detecting both regular drones (multirotors) and fixed-wing drones in images.

## Overview

This project aims to provide a robust solution for detecting UAVs (Unmanned Aerial Vehicles), commonly known as drones, in visual data. The model is trained using the YOLOv8 object detection framework, known for its speed and accuracy. This repository includes the trained model weights, example usage scripts, and documentation to help you get started with UAV detection.

## Requirements Installation

```bash
pip install -r requirements.txt
```

## Dataset

*The training dataset contains 3,000 ***Drone*** images, evenly distributed between multirotor and ***fixed-wing*** types.*

*   **Description:** The dataset consists of images collected from various sources, including online datasets and custom captures. It contains images of both multirotor and fixed-wing drones in different environments and lighting conditions.
*   **Size:** The training set contains 1000 images, the validation set contains 200 images, and the test set contains 300 images.
*   **Classes:** The model is trained to detect two classes: 'drone' and 'fixed-wing'."

    Example:
    ```
    path: direct/project/path
    train: train
    val: valid

    names:
    0: drone
    1: Fix-wing-drone
    ```

## Model Training

The model was trained using YOLOv8 with the following parameters:

*   **Model Architecture:** YOLOv8n, YOLOv8s, YOLOv8m 
*   **Epochs:** 51
*   **Batch Size:** 16
*   **Image Size:** 640x640
*   **Device:** GPU (MPS for Apple Silicon or CUDA for NVIDIA, if used) or CPU (I used MPS)

## Training command:

```bash
python3 main.py