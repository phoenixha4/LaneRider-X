# LaneRider-X

## Autonomous Lane Detection and Driving Simulation

This project is a Python-based simulation that demonstrates autonomous lane detection and driving using computer vision techniques. The system captures the screen, processes the frame to detect lanes, and simulates driving actions based on the detected lane slopes. The project uses the `keyboard` library to simulate key presses for driving actions and OpenCV for image processing.

### Overview

- **controller.py**: 
  - Contains the `drive` function that simulates driving actions (e.g., moving forward, turning left/right) based on the detected lane slopes.
  - Uses the `keyboard` library to simulate key presses.
  - The `frange` function generates a range of floating-point numbers with a specified step.

- **grab_screen.py**:
  - Contains the `grab` function that captures the screen or a specified region of the screen using the `win32gui` and `win32ui` libraries.
  - The captured image is returned as a NumPy array in RGB format.

- **main.py**:
  - The main script that orchestrates the screen capture, lane detection, and driving simulation.
  - The `process_frame` function processes the captured frame to detect lanes using edge detection and Hough Transform.
  - The `roi` function defines the region of interest (ROI) for lane detection.
  - The `main` function continuously captures the screen, processes the frames, and calls the `drive` function to simulate driving actions.

## Requirements

You can install the required libraries using pip:

```bash
pip install keyboard numpy opencv-python pywin32
```

## How to Run

1. Clone the repository or download the project files.
2. Install the required libraries as mentioned above.
3. Run the `main.py` script:

```bash
python main.py
```

4. The script will start capturing the screen and simulate driving actions based on the detected lanes.
5. Press the `Space` key to pause/unpause the simulation.
6. Press the `Esc` key to exit the simulation.

## Key Features

- **Screen Capture**: The project captures the screen or a specified region of the screen using the `win32gui` and `win32ui` libraries.
- **Lane Detection**: The project uses edge detection (Canny) and Hough Transform to detect lanes in the captured frames.
- **Driving Simulation**: Based on the detected lane slopes, the project simulates driving actions such as moving forward, turning left, or turning right using the `keyboard` library.
- **Pause/Resume**: The simulation can be paused or resumed using the `Space` key.

## Customization

- **Region of Interest (ROI)**: You can modify the `roi` function in `main.py` to change the region of interest for lane detection.
- **Driving Logic**: The driving logic in `controller.py` can be adjusted to change the behavior of the simulated driving actions.
- **Screen Region**: You can specify a different screen region to capture by modifying the `grab` function call in `main.py`.

## Limitations

- The project is designed for simulation purposes and may not work perfectly in all scenarios.
- The lane detection algorithm assumes a simple road environment and may not perform well in complex or noisy environments.
- The project relies on screen capture, which may not be efficient for real-time applications.

## Future Improvements

- Implement more advanced lane detection algorithms, such as deep learning-based approaches.
- Add support for real-time video input from a camera.
- Improve the driving logic to handle more complex driving scenarios.
- Optimize the screen capture and image processing for better performance.
