# AI-Based Drowsiness and Yawn Detection System

## Overview

The AI-Based Drowsiness and Yawn Detection System is an advanced solution designed to bolster driver safety through the application of cutting-edge computer vision techniques. Leveraging the Raspberry Pi camera module, this system detects signs of drowsiness and yawning in real-time, providing timely alerts to mitigate the risk of accidents.

## Table of Contents

- [Background](#background)
- [Features](#features)
- [Detection Algorithms](#detection-algorithms)
- [Project Configuration](#project-configuration)
- [Dependencies](#dependencies)
- [Installation](#installation)
- [Usage](#usage)
- [Code Overview](#code-overview)
- [Results](#results)
- [Conclusion](#conclusion)
- [Contributing](#contributing)

## Background

Driver fatigue stands as a critical issue contributing to accidents and fatalities on the roads. This research project confronts this concern head-on by implementing a robust drowsiness and yawning detection system. The system intricately analyzes facial features, focusing on the eye aspect ratio (EAR) for drowsiness detection and lip distance for detecting yawning events.

## Features

- **Real-time Monitoring:** Continuous monitoring of the driver's face.
- **Immediate Alerts:** Swift alerts triggered in the presence of drowsiness or yawning.
- **Configurability:** Adjustable parameters for sensitivity to suit varying scenarios.
- **Raspberry Pi Integration:** Seamless integration with the Raspberry Pi camera module for practical in-car deployment.

## Detection Algorithms

### Drowsiness Detection

- The EAR is calculated using the formula: `EAR = (|P2 – P6| + |P3 – P5|) / (2|P1 – P4|)`. Refer to the pdf in the repository.
- Drowsiness is declared if the EAR falls within the predefined threshold `[0.15, 1]`.

### Yawn Detection

- Lip distance is calculated, considering the positions of the upper and lower lips.
- The mean of the lip region points is used to calculate the lip distance.
- Yawning is declared if the lip distance exceeds the predefined threshold.

## Project Configuration

- `Eye_threshold_value`: 0.3
- `Frame_Check`: 30 frames/sec
- `Yawn_Threshold`: 2

## Dependencies

- OpenCV
- dlib
- scipy
- numpy
- argparse

## Installation

1. **Clone the Repository:**
    ```bash
    git clone https://github.com/your_username/your_repository.git
    ```

2. **Install Dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

## Usage

1. **Run the Main Script:**
    ```bash
    python drowniness_yawn.py --webcam webcam_index
    ```

2. **Ensure Proper Camera Positioning:**
    - Ensure proper camera positioning and lighting for accurate results.

## Code Overview

The Python code utilizes state-of-the-art computer vision libraries, including OpenCV and dlib. The integration with the Raspberry Pi camera module ensures real-time processing, making it suitable for in-car applications.

## Results

The system has undergone extensive testing under various conditions, demonstrating its effectiveness in detecting drowsiness and yawning. Detailed research findings and performance metrics are available in the pdf  document provided in the repository.

## Conclusion

The AI-Based Drowsiness and Yawn Detection System delivers a comprehensive solution to combat driver fatigue, significantly enhancing road safety. The use of cutting-edge algorithms and the Raspberry Pi camera module positions it as a viable choice for implementation in vehicles.

## Contributing

Contributions to this project are welcome. For major changes, please open an issue first to discuss the proposed changes.


