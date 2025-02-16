# Ticker Classification

This repository provides a framework for detecting and classifying tickers in images using a heuristic approach and/or a pre-trained Convolutional Neural Network (CNN) model. The model is trained to identify the presence of tickers in the bottom region of images.

## Table of Contents
- [Requirements](#requirements)
- [Setup](#setup)
- [Dataset Preparation](#dataset-preparation)
- [Inference](#inference)
- [Visualization](#visualization)

## Requirements

Ensure you have the following dependencies installed:

- Python 3.6+
- TensorFlow 2.x
- OpenCV
- NumPy
- Pillow
- Matplotlib

You can install the required packages using pip:

```bash
pip install tensorflow opencv-python numpy matplotlib
```

## Setup
Clone the repository:
```bash
git clone https://github.com/648374hub/ticker-classification.git
cd ticker-classification
```

## Dataset Preparation

Prepare your dataset by organising your image paths as a list of JSON objects. Each JSON object has two fields - "path" and "label".
Example = [
    {
        "path": "/path/to/image.png", 
        "label": "ticker" 
    },
    {
        "path": "/path/to/image1.png", 
        "label": "no_ticker" 
    },
]
Also, download the trained CNN model file from the drive link provided over mail and put in the saved_model/ folder.

## Inference

### Using Heuristic approach
Follow the EDA.ipynb notebook for inference code. After Dataset Preparation step, call the heuristic function for each JSON object to get the prediction class.

### Using CNN-based Classifier
Follow the trainCNN.ipynb notebook for inference code block. After Dataset Preparation step, run the code cells in the block to get the prediction class.


## Visualization
All EDA steps has optional visualisations to get better understanding of the data. Run the functions with `visualize=True` to get the visualisation on the input image.