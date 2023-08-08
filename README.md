# Optical Satellite Flood Segmentation

## Description
This repository is dedicated to the task of segmenting and identifying flooded areas using optical satellite imagery through deep learning models.
Originally created as a solution for a Kaggle competition, this repository showcases the power of deep learning in remote sensing applications.

## Table of Contents
- [About the Challenge](#about-the-challenge)
- [Installation](#installation)
- [Usage](#usage)
- [Datasets](#datasets)
- [Models](#models)
- [Evaluation](#evaluation)

## About the Challenge
The challenge is to design and implement a deep learning model for the automatic segmentation of sUAV images.
The model is trained using training images with pixel-wise annotations.
After training, predictions on the test images are made and submitted on Kaggle.

The images are segmented into the following 25 categories:
```
0. Background
1. Property Roof
2. Secondary Structure
3. Swimming Pool
...
22. Water Body
23. Flooded
24. Boat
```
The performance of the model is evaluated using the Dice coefficient, which provides a measure of the pixel-wise agreement between predicted segmentations and ground truths. The leaderboard score represents the mean Dice coefficient across all (Image, Label) pairs in the test set.

The formula is:

**Dice coefficient = $\frac{2 \times |X \cap Y|}{|X| + |Y|}$**


where $( X )$ is the predicted set of pixels and $( Y )$ is the ground truth. The Dice coefficient is 1 when both $( X )$ and $( Y )$ are empty. The leaderboard score is the mean Dice coefficient for each (Image, Label) pair in the test set.

## Installation
1. Clone the repository to your local machine.
2. Ensure you have Python installed.
3. Set up a virtual environment: `python -m venv env`
4. Activate the virtual environment: `source env/bin/activate (on Windows: .\env\Scripts\activate)`
5. Install the required packages: `pip install -r requirements.txt`

## Usage
1. Activate the virtual environment.
2. Launch Jupyter Notebook: `jupyter notebook`
3. Navigate to and open the provided notebook to view, modify, or run cells.

## Datasets
The datasets comprise sUAV images captured in the aftermath of Hurricane Harvey. These images, rich in detail, serve as a valuable resource for training models to recognize and segment different objects and regions, with a particular focus on flooded areas.

## Models
The primary model used in this repository is the UNet architecture with a ResNet-50 encoder. This architecture has proven to be effective for various segmentation tasks, offering a balance between accuracy and computational efficiency.

## Evaluation
The Dice coefficient, also known as the Sørensen–Dice index, is a statistical metric used to gauge the similarity of two samples. For image segmentation tasks, it provides an insight into how closely the predicted segmentation aligns with the ground truth annotations. A Dice coefficient of 1 indicates perfect overlap, while 0 signifies no overlap.
