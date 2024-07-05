
# Pose Estimation

This project demonstrates how to use Mediapipe and OpenCV to perform holistic detection of face, hand, and pose landmarks using a webcam. The collected data is then used to train a machine learning model to classify poses.

## Table of Contents

- [Introduction](#introduction)
- [Installation](#installation)
- [Data Collection](#data-collection)

## Introduction

This project uses the Mediapipe library to detect face, hand, and pose landmarks. The detected landmarks are then saved into a CSV file which is used to train a machine learning model for pose classification.

## Installation

1. Clone this repository:

```sh
git clone https://github.com/yourusername/mediapipe-holistic-detection.git
cd mediapipe-holistic-detection
```

2. Install the required packages:

```sh
pip install -r requirements.txt
```

This will start the webcam and display the detected landmarks on the screen. Press 'q' to quit.

## Data Collection

The detected landmarks are saved in a CSV file. Each row in the CSV file corresponds to one frame from the webcam feed and contains the following columns:

- \`frame\`: Frame number
- \`pose_landmarks\`: List of pose landmarks
- \`left_hand_landmarks\`: List of left hand landmarks
- \`right_hand_landmarks\`: List of right hand landmarks
- \`face_landmarks\`: List of face landmarks
- \`label\`: Pose label (if available)
