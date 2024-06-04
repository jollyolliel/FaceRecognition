
## Face Detection Project

This project utilizes Python and OpenCV library to detect faces in a live video stream.

### Requirements

-   Python 3.x
-   OpenCV library: You can install OpenCV using `pip install opencv-python`

### Usage

1.  Save the script as `facerecognition.py`.
2.  Run the script using `python facerecognition.py`.

### How it Works

The script performs the following steps:

1.  Imports necessary libraries: OpenCV (`cv2`) and `datetime`.
2.  Loads the pre-trained face detection model (`haarcascade_frontalface_default.xml`) from OpenCV's Haar cascade collection.
3.  Initializes video capture using your webcam (device index 0).
4.  Defines a function `detect_bounding_box` that:
    -   Converts the video frame to grayscale.
    -   Detects faces using the loaded cascade classifier.
    -   Draws a green rectangle around each detected face.
    -   Returns a list of detected faces (bounding boxes).
5.  Enters a loop that continues until the user presses `Esc` key:
    -   Captures a frame from the video stream.
    -   Calls `detect_bounding_box` to detect faces in the frame.
    -   Gets the current timestamp.
    -   If no faces are detected (i.e.,  `faces` is not a tuple), saves the frame as an image with a unique filename based on the timestamp.
    -   Displays the video frame with detected faces in a window titled "My Face Detection Project".
    -   Waits for a key press for 1 millisecond.
    -   If the pressed key is `Esc`, exits the loop.
6.  Releases the video capture and closes all OpenCV windows.

**Note:** This script uses a basic face detection model. More advanced models can be explored for improved accuracy and recognition capabilities.
