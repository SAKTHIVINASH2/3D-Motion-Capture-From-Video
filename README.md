# 3D-Motion-Capture-From-Video

## Introduction:
3D motion capture is a technology that allows you to capture human movements and translate them into digital data. This data can then be used to animate 3D models, creating realistic and interactive experiences.

## Animation tool(unity):
Unity is a powerful game engine that provides a robust platform for creating 3D games and applications. By combining the capabilities of Python and Unity, we can develop a real-time 3D motion capture system that can be used to enhance gaming and simulation experiences.

## Understanding the Workflow:
1. Video Acquisition: Capture real-time video using a webcam or external camera.
2. Pose Estimation: Use Python libraries like OpenCV, TensorFlow, or PyTorch to estimate the 3D pose of the user from the video frames.
3. Data Transmission: Send the estimated pose data from Python to Unity in real-time.
4. 3D Model Animation: In Unity, use the pose data to animate a 3D model, mirroring the user's movements.

## To install the 3D Motion Capture From Video, please follow these steps:

1. Clone the repository to your local machine.

2. Install the required dependencies by running the following command:

```
pip install -r requirement.txt
```


## Python workflow:
### 1. Video Acquisition
   * Camera Setup: Use a webcam or external camera to capture real-time video of the user. Ensure the camera is positioned to capture the desired range of motion.
   * Lighting Conditions: Adequate lighting is crucial for accurate pose estimation. Avoid excessive shadows or glare.
### 2. Pose Estimation with Python
   * Library Selection: Choose a suitable Python library for pose estimation, such as OpenCV, TensorFlow, or PyTorch. Each library has its strengths and weaknesses.
   * Model Selection: Select a pre-trained model or train your own model based on your specific requirements.
   * Keypoint Detection: The library will detect keypoints on the user's body, such as the head, shoulders, elbows, wrists, hips, knees, and ankles.
   * Pose Estimation: Using these keypoints, the library will estimate the 3D pose of the user.

Link to code:[CLICK HERE TO SEE THE CODE](main_code.py)

## Data Storage:
* Store the estimated pose data in a structured file format (e.g.,TXT, JSON, CSV, or a custom binary format).

Link to sample data:[CLICK HERE TO SEE THE SAMPLE DATA](AnimationFile.txt)

## Unity workflow:
1. Load Pose Data: The `Animation_code` script loads pose data from the TXT file.
2. Map to Animator: The `Animation_code` script maps the loaded pose data to animator parameters. This involves associating keypoint coordinates with corresponding body parts on the 3D model.
3. Update Animator: In the `Update` method, the `Animation_code` script updates the animator's parameters based on the current pose data, causing the 3D model to animate accordingly.
4. Create Lines: The `line_code` script creates a LineRenderer component and assigns points to it. These points represent the keypoints from the pose data.
5. Update Line Positions: In the `Update` method of `line_code`, the line renderer's positions are updated based on the positions of the points. This visualizes the captured motion as lines connecting the keypoints.
