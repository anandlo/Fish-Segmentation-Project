# Real-Time Fish Segmentation for Underwater Video Analysis

This project implements a real-time video segmentation model designed to detect and segment fish in underwater environments. Using the [DeepFish dataset](https://datasetninja.com/deep-fish) of high-resolution underwater images, the model employs a ConvLSTM U-Net architecture to effectively capture spatial and temporal features, allowing for accurate segmentation across diverse marine habitats. 

## Table of Contents
- [Introduction](#introduction)
- [Dataset](#dataset)
- [Model Architecture](#model-architecture)
- [Results](#results)
- [Performance Metrics](#performance-metrics)
- [Future Work](#future-work)
- [Acknowledgments](#acknowledgments)


## Introduction
Monitoring fish populations in their natural habitats is essential for sustainable fisheries management. The DeepFish dataset provides a benchmark for training and evaluating models in underwater video analysis, containing around 40,000 labeled images across 20 distinct tropical habitats in Australia. This project utilizes ConvLSTM and U-Net to segment fish in real-time, demonstrating the model's potential in automating marine life monitoring tasks.

## Dataset
The [DeepFish dataset](https://datasetninja.com/deep-fish) includes:
- **40,000 images** from 20 habitats, featuring classification, localization, and segmentation labels.
- **High-resolution images** (1920 x 1080 pixels) collected in low-disturbance underwater environments.
- Segmentation labels enable detailed habitat analysis, crucial for understanding fish behavior, population monitoring, and size estimation.

### Example Images
- **Fish Habitat**: Mangrove, coral reef, and seagrass beds.
- **Labels**: Fish classification, localization, and instance segmentation masks.

## Model Architecture
This project uses a U-Net with ConvLSTM layers to capture both spatial and temporal information:
- **ConvLSTM Layer**: Extracts temporal features from sequential frames, enhancing model sensitivity to movement and context in underwater footage.
- **U-Net**: A fully convolutional neural network with skip connections, ideal for generating segmentation masks.

### Model Summary
- **Parameters**: 593,793
- **Model Size**: 2.27 MB
- **Performance**: Achieved near-perfect segmentation with a **Loss of 1.19e-07** and **Mean IoU of 99.99%**.

### Training the Model
Run the provided Jupyter Notebook `train_model.ipynb`:
- **Data Preprocessing**: Prepares images and masks for input to the ConvLSTM U-Net model.
- **Model Training**: Train the model on the DeepFish dataset using the defined ConvLSTM U-Net architecture.


## Results
The model produces real-time segmentation masks, overlayed on the original video frames, enabling detailed fish monitoring across various habitats.

### Visualization
Example segmentation results include:
- **Input Video Frame**: Original frame from the video.
- **Segmentation Mask**: Predicted mask overlay showing the segmented fish.
  
## Performance Metrics
- **Loss**: 1.1920930376163597e-07
- **Mean IoU**: 0.9999998807907104

## Future Work
- **Deploy on Edge Devices**: Optimize model for edge deployment in underwater environments, using lightweight architectures.
- **Multi-Species Segmentation**: Extend the model to detect and classify different fish species.
- **3D Video Processing**: Explore 3D ConvNets for enhanced spatial analysis in complex marine environments.

## Acknowledgments
- **DeepFish Dataset**: The dataset used for training is publicly available at [Dataset Ninja](https://datasetninja.com/deep-fish).
- **ConvLSTM U-Net Architecture**: Based on principles from the U-Net model for biomedical image segmentation and ConvLSTM for video processing.
