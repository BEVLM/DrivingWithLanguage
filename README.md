# BeVLM: GoT-based Integration of BEV and LLM for Driving with Language

[![CVPR Workshop](https://img.shields.io/badge/CVPR%20Workshop-2024-blue.svg)](https://cvpr2024.org/workshops)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## Overview

The integration of large language models (LLMs) with autonomous driving systems has garnered significant attention. However, several challenges persist in this domain. First, aligning LLMs with multi-view visual sequences, commonly encountered in autonomous driving tasks, remains an open problem. Second, the multi-stage nature of autonomous driving, involving perception, prediction, planning, and behavior, necessitates robust contextual understanding.
To address these challenges, we first introduce the Bird’s Eye View (BEV) feature using a BEV encoder to improve visual context understanding. By fusing BEV representations with textual context, we enhance the alignment between LLMs and multi-view visual data. Second, we augment question-answering (QA) pairs to facilitate cross-modal alignment, bridging the gap between different modalities. Finally, we design a Graph of Thoughts (GoT) scheme that empowers multimodal LLMs to comprehensively understand both visual and textual contexts.
Our experimental results demonstrate the effectiveness of our proposed methods.

## Features

- Model architecture integrating BEV features and VLM
- Supports parsing and executing natural language commands
- Efficient training and inference scripts
- Provides pre-trained models and example datasets

## Installation

### Prerequisites

- Python 3.8+
- PyTorch 2.0+
- Other dependencies listed in `requirements.txt`

### Steps

1. Clone the repository

    ```bash
    git clone https://github.com/BEVLM/DrivingWithLanguage.git
    cd BEVLM
    ```

2. Create a virtual environment and install dependencies

    ```bash
    python -m venv venv
    source venv/bin/activate   # Linux/MacOS
    venv\Scripts\activate.bat  # Windows
    pip install -r requirements.txt
    ```

3. Download pre-trained models

    Visit [pre-trained models link](#) to download the model weights and place them in the `weights/` directory.

## Usage

### Training

1. Prepare your dataset. The structure should follow the `data/` directory format.
2. Run the training script:

    ```bash
    python train.py --config configs/config.yaml
    ```

### Inference and Testing

1. Run inference with the following command:

    ```bash
    python infer.py --input data/sample_input/ --output results/
    ```

2. Evaluate the model:

    ```bash
    python evaluate.py --predictions results/ --ground_truth data/sample_gt/
    ```

## Project Structure

