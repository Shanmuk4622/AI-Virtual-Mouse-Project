# AI Virtual Mouse Project

This project implements an AI-based virtual mouse using computer vision and hand tracking. The system uses a webcam to detect hand gestures and translates them into mouse movements and clicks, enabling hands-free control of the computer.

## Features

- **Hand Tracking**: Detects and tracks hand landmarks using the Mediapipe library.
- **Mouse Movement**: Moves the mouse cursor based on the position of the index finger.
- **Click Detection**: Simulates mouse clicks when specific gestures are detected.
- **Smooth Movement**: Implements smoothening to reduce jitter in cursor movement.
- **Real-Time Performance**: Displays the webcam feed with real-time hand tracking and gesture recognition.

## Requirements

- Python 3.8.0 or higher
- Libraries:
  - `opencv-python`
  - `mediapipe`
  - `numpy`
  - `autopy`

## Installation

1. Clone the repository or download the project files.
2. Install the required Python libraries using the `requirements.txt` file:
   ```bash
   pip install -r requirements.txt
   ```
   This will install the following libraries with their specific versions:
   - `opencv-python==4.5.5.64`
   - `mediapipe==0.9.1.0`
   - `numpy==1.21.6`
   - `autopy==4.0.0`

   Please go with the Following command lines:
   ```bash
   pip install opencv-contrib-python
   pip install opencv-contrib-python
   pip install opencv-python mediapipe numpy autopy
   ```

3. Ensure your webcam is connected and functional.

## Usage

1. Run the `AiVirtualMouseProject.py` script:
   ```bash
   python AiVirtualMouseProject.py
   ```
2. The webcam feed will open, and the system will start detecting your hand gestures.
3. Use the following gestures to control the mouse:
   - **Move Cursor**: Raise only the index finger and move it to control the cursor.
   - **Left Click**: Raise both the index and middle fingers, and bring them close together to simulate a click.
4. Press the `q` key to exit the program.

## File Structure

- `AiVirtualMouseProject.py`: Main script for the virtual mouse functionality.
- `HandTrackingModule.py`: Module for hand detection and gesture recognition.
- `requirements.txt`: File containing the required libraries and their versions.
- `ReadMe`: Documentation for the project.

## How It Works

1. **Hand Detection**: The `HandTrackingModule` uses Mediapipe to detect hand landmarks in the webcam feed.
2. **Gesture Recognition**: The system identifies which fingers are raised using the `fingersUp` method.
3. **Mouse Control**:
   - The index finger's position is mapped to the screen coordinates to move the cursor.
   - The distance between the index and middle fingers is calculated to detect clicks.
4. **Smoothening**: Cursor movement is smoothened using a weighted average to reduce jitter.

### Video Demonstration

Watch the video below to see the AI Virtual Mouse in action:

[![AI Virtual Mouse Demo](https://img.youtube.com/vi/IHkBkEHid5M/0.jpg)](https://youtu.be/IHkBkEHid5M)



## Troubleshooting

- **Camera Not Detected**: Ensure your webcam is connected and accessible. Check the `cv2.VideoCapture` index (0 or 1) in the code.
- **Dependencies Missing**: Install the required libraries using `pip install -r requirements.txt`.
- **Performance Issues**: Reduce the webcam resolution or frame rate for better performance.

## Future Improvements

- Add support for right-click and drag gestures.
- Enhance accuracy and robustness of hand tracking.
- Implement multi-hand support for additional gestures.

## License

This project is open-source and available for educational and personal use.

## Acknowledgments

- [Mediapipe](https://mediapipe.dev/) for hand tracking.
- [OpenCV](https://opencv.org/) for image processing.
- [Autopy](https://github.com/autopilot-rs/autopy) for mouse control.

