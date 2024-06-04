# Tennis Analysis System

## Overview

This project demonstrates how to use machine learning, computer vision, and deep learning techniques to create a comprehensive tennis analysis system. The system utilizes YOLO for object detection, CNN for court key points detection, and various other tools for data tracking and analysis.

[](
https://github.com/kemswd/Tennis-analysis-using-deep-learning-and-machine-learning./assets/87093504/fb5fd44c-87b3-499d-b839-3481fac9f924
)

## Features

- **Object Detection**: Detect players and tennis balls using YOLOv8.
- **Object Tracking**: Track detected objects across frames.
- **Court Key Points Detection**: Custom CNN model to detect key points on the court.
- **Visualization**: Mini court to show player and ball positions.
- **Speed Analysis**: Analysis board for player speed, average speed, ball speed, and average ball speed.

## Table of Contents

1. [Installation](#installation)
2. [Usage](#usage)
3. [Features](#features)
    - [Object Detection](#object-detection)
    - [Object Tracking](#object-tracking)
    - [Court Key Points Detection](#court-key-points-detection)
    - [Visualization](#visualization)
    - [Speed Analysis](#speed-analysis)
## Features

### Object Detection

- Uses YOLOv8 from Ultralytics to detect players and tennis balls in video frames.
- Fine-tuned on a custom dataset for optimal performance.

### Object Tracking

- Tracks detected objects across video frames to maintain consistent identification.

### Court Key Points Detection

- Custom Convolutional Neural Network (CNN) developed using PyTorch to detect key points on the tennis court.

### Visualization

- Mini court visualization to display the positions of players and the ball in real-time.
- Provides a clear and concise view of the game's progress.

### Speed Analysis

- Analysis board to monitor and display:
  - Player speed and average speed.
  - Ball speed and average ball speed.

## Installation
To run the code, ensure you have Python installed and install the required packages using:

```bash
pip install -r requirements.txt
```
## Usage
- Clone the repository:
```bash
git clone https://github.com/yourusername/tennis-analysis.git
```
- Navigate to the project directory:
```bash
cd tennis-analysis
```
- Run the analysis script:
```bash
python main.py
```
