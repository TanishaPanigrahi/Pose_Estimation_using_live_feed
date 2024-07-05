
# Mediapipe Holistic Detection and Pose Classification

This project demonstrates how to use Mediapipe and OpenCV to perform holistic detection of face, hand, and pose landmarks using a webcam. The collected data is then used to train a machine learning model to classify poses.

## Table of Contents

- [Introduction](#introduction)
- [Installation](#installation)
- [Usage](#usage)
- [Data Collection](#data-collection)
- [Training the Model](#training-the-model)
- [Evaluation](#evaluation)
- [Contributing](#contributing)
- [License](#license)

## Introduction

This project uses the Mediapipe library to detect face, hand, and pose landmarks. The detected landmarks are then saved into a CSV file which is used to train a machine learning model for pose classification.

## Installation

1. Clone this repository:

\`\`\`sh
git clone https://github.com/yourusername/mediapipe-holistic-detection.git
cd mediapipe-holistic-detection
\`\`\`

2. Install the required packages:

\`\`\`sh
pip install -r requirements.txt
\`\`\`

The \`requirements.txt\` file should contain:
\`\`\`
mediapipe
opencv-python
numpy
pandas
scikit-learn
\`\`\`

## Usage

To start the webcam feed and perform holistic detection, run:

\`\`\`sh
python detect_and_save.py
\`\`\`

This will start the webcam and display the detected landmarks on the screen. Press 'q' to quit.

## Data Collection

The detected landmarks are saved in a CSV file. Each row in the CSV file corresponds to one frame from the webcam feed and contains the following columns:

- \`frame\`: Frame number
- \`pose_landmarks\`: List of pose landmarks
- \`left_hand_landmarks\`: List of left hand landmarks
- \`right_hand_landmarks\`: List of right hand landmarks
- \`face_landmarks\`: List of face landmarks
- \`label\`: Pose label (if available)

You can run the data collection script with the following command:

\`\`\`sh
python collect_data.py --output landmarks.csv
\`\`\`

## Training the Model

To train the pose classification model, use the \`train_model.py\` script. Make sure you have the collected landmarks data in a CSV file.

\`\`\`sh
python train_model.py --data landmarks.csv --output model.pkl
\`\`\`

This script will train a machine learning model using the provided data and save the trained model to a file.

## Evaluation

To evaluate the trained model, use the \`evaluate_model.py\` script:

\`\`\`sh
python evaluate_model.py --model model.pkl --data test_data.csv
\`\`\`

This will load the trained model and evaluate its performance on the provided test data.

## Contributing

Contributions are welcome! If you have any ideas, suggestions, or bug reports, please open an issue or submit a pull request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
