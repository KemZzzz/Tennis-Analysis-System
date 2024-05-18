# Tennis-analysis-using-deep-learning-and-machine-learning.


This repository contains code and resources for analyzing tennis matches using deep learning and machine learning techniques. The project aims to develop a video analysis tool that includes ball tracking, court tracking, bounce detection, and player tracking using a single camera.


[project Video](https://github.com/kemswd/Tennis-analysis-using-deep-learning-and-machine-learning./assets/87093504/8ef198c5-7541-4b3f-94d3-a8787ed77427)



## Table of Contents
- [Introduction](#introduction)
- [Dataset](#dataset)
- [Court Detection](#court-detection)
- [Ball Detection](#ball-detection)
- [Bounce Detection](#bounce-detection)
- [Pipeline](#pipeline)
- [Possible Improvements](#possible-improvements)
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Introduction
Tennis analysis can be enriched with statistics like serve locations and ball depth. Existing tools like Hawk-Eye and IBM Slamtracker provide detailed statistics but are costly and complex. This project aims to create a more accessible analysis tool using deep learning and a single camera setup.

## Dataset
The dataset consists of video highlights from various tournaments, covering all court types (hard, clay, grass). Frames were extracted and manually filtered, resulting in 8841 images with a resolution of 1280×720.

## Court Detection
The court detection uses a neural network to identify 14 key points on a tennis court. A semi-automated approach was used to collect and filter the dataset, and a deep learning network similar to TrackNet was employed.

### Method
1. Extract white pixels from the image.
2. Detect lines using Hough Transform.
3. Compare detected lines with reference court configuration using homography matrix.
4. Perform warp perspective and count hits to determine the best matching lines.

### Deep Learning Approach
The proposed deep learning network detects key points of the court and restores the court configuration in the image. Postprocessing techniques refine key points using classical computer vision methods.

## Ball Detection
Ball detection uses the TrackNet deep learning network, trained to recognize the ball and its flying patterns from consecutive frames. The dataset includes video clips with labeled frames indicating ball visibility and trajectory patterns.

## Bounce Detection
Bounce detection is achieved by tracking the ball's path and using machine learning to identify sudden changes in direction, indicating a bounce. A CatBoostRegressor model was used with features derived from ball trajectory data.

## Pipeline
The pipeline integrates court detection, ball detection, bounce detection, and player tracking into a cohesive analysis tool. It starts with court detection, followed by ball tracking, bounce detection, and player tracking using a pretrained Faster RCNN neural network.

## Possible Improvements
1. Speed up the algorithm by using a lighter neural network and applying quantization and pruning.
2. Combine ball and court detection into one neural network.
3. Improve ball detection quality by adding frames without the ball to the training dataset.
4. Use augmentation during court detection training to handle shadows and different angles.

## Installation
To run the code, ensure you have Python installed and install the required packages using:

```bash
pip install -r requirements.txt
## Usage
- Clone the repository:

git clone https://github.com/yourusername/tennis-analysis.git
- Navigate to the project directory:

cd tennis-analysis
- Run the analysis script:

python main.py
