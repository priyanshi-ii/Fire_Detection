
# Fire Detection System using OpenCV and Python

## Introduction

This project demonstrates a simple fire detection system using computer vision techniques and the OpenCV library in Python. The system captures video from the webcam, processes the frames, and alerts the user if a potential fire is detected in the frame. The system uses color-based segmentation to identify areas that match the color characteristics of fire.

## Requirements

- Python 3.x
- OpenCV (`opencv-python` package)
- NumPy (`numpy` package)
- `winsound` library (for audio alerts)

## Installation

1. Install Python: If you don't have Python installed, download and install it from the official Python website: [python.org](https://www.python.org/downloads/)

2. Install Required Packages: Open a terminal or command prompt and run the following commands to install the required packages:

   ```
   pip install opencv-python
   pip install numpy
   ```

3. Clone or Download the Repository: Clone this repository to your local machine using Git, or download and extract the ZIP archive.

## Usage

1. Open a terminal or command prompt.

2. Navigate to the directory where you've saved the project files.

3. Run the `fire_detection.py` script:

   ```
   python fire_detection.py
   ```

4. The webcam feed will open, and the system will start analyzing frames for potential fires.

5. When a fire-like color range is detected, a bounding box will be drawn around the potential fire area in the frame, and an audio alert will be played.

6. Press the 'q' key in the window to quit the application.

## Customization

You can customize the system by adjusting the color range used for fire detection. The `lower_cutoff` and `upper_cutoff` variables in the `fire_detection.py` script define the color range in HSV color space that corresponds to the color of fire. Modify these values to suit your needs.

```python
lower_cutoff = np.array([0, 150, 150])
upper_cutoff = np.array([10, 255, 255])
```

## Notes

- This system is a simple demonstration and may not work perfectly in all scenarios.
- Ensure that your webcam is properly connected and configured before running the system.
- The `winsound` library used for audio alerts is available on Windows systems. If you're using a different operating system, you may need to use an alternative method for audio alerts.
