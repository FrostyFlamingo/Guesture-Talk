# Guesture-Talk
Sign Language Converter (Gesture Talk) 

Gesture Talk is an innovative sign language conversion system designed to bridge the communication gap between the hearing and deaf communities. This cutting-edge application harnesses the power of multiple advanced technologies, including Python, MediaPipe, TensorFlow, and Long Short-Term Memory (LSTM) neural networks, to interpret sign language gestures and translate them into spoken and written language in real-time. 

# PROBLEM STATEMENT 
The communication gap between sign language users and non-users poses significant challenges, leading to social isolation and limited access to opportunities for the deaf and hard-of-hearing community. Traditional solutions, such as human interpreters and manual dictionaries, are often impractical and inadequate in providing real-time, accurate translations. There is a critical need for a technological solution that can seamlessly and accurately translate sign language into spoken and written language, facilitating inclusive communication in everyday situations. Gesture Talk aims to address this need by developing an accessible, real-time sign language interpreter that converts gestures into text and speech, making communication more inclusive and accessible for all.

# Steps Involved in the Sign Language Converter:
1.	Setup and Initialization
•	Libraries: Import necessary libraries such as OpenCV, NumPy, MediaPipe, TensorFlow, and Tkinter.
•	Model Loading: Load the pre-trained action recognition model using TensorFlow.
•	Configuration: Initialize variables for storing sequences, sentences, predictions, and set a confidence threshold.
2.	Start Recognition
•	Video Capture: Start capturing video from the webcam using OpenCV.
•	Threading: Run the recognition process in a separate thread to keep the GUI responsive.
3.	Real-Time Landmark Detection
•	MediaPipe Initialization: Initialize the MediaPipe holistic model for detecting face, pose, and hand landmarks.
•	Frame Processing: Convert the image color space, process the frame with the MediaPipe model, and extract landmarks.
4.	Keypoints Extraction
•	Pose Keypoints: Extract keypoints from pose landmarks.
•	Face Keypoints: Extract keypoints from face landmarks.
•	Hand Keypoints: Extract keypoints from left- and right-hand landmarks.
•	Concatenation: Concatenate all extracted keypoints into a single array.
5.	Action Prediction
•	Sequence Formation: Append extracted keypoints to the sequence list and maintain a fixed-length sequence.
•	Model Prediction: Use the pre-trained model to predict the action based on the sequence of keypoints.
•	Confidence Check: Compare the prediction confidence with the threshold to filter out low-confidence predictions.
6.	Feedback and Visualization
•	Text Feedback: Display the predicted action and confidence score on the video feed.
•	Audio Feedback: Convert the predicted action to speech using the text-to-speech engine.
•	Sentence Formation: Form sentences from a sequence of detected actions and display them.
7.	User Interface (GUI)
•	Tkinter Window: Initialize a GUI window using Tkinter.
•	Control Buttons: Add buttons for starting and stopping recognition.
•	Event Loop: Start the Tkinter event loop to handle user interactions.
8.	Stop Recognition
•	Release Resources: Stop the video capture, release the webcam, and destroy OpenCV windows.

![image](https://github.com/user-attachments/assets/4c38c58d-8be3-4640-b6a0-1f8484cbbd67)

# SYSTEM REQUIREMENTS
Hardware Requirements: The device should be either a laptop or desktop equipped with a camera. It must run on Windows, macOS, or Linux operating systems. The processor should be an Intel Core i5 11th Gen with a clock speed of 2.50 GHz or higher, and the system should include an NVIDIA GeForce RTX 2050 GPU. Additionally, a minimum of 8 GB of RAM and 25 GB of available hard disk space are required.

Software Requirements: The project supports Windows, macOS, and Linux operating systems. It requires Python 3 as the programming language, and the development environment should include IDEs like Visual Studio Code or Jupyter Notebook. Essential libraries and modules needed for the project include TensorFlow, Mediapipe, Numpy, Sklearn, pyttxs3, OpenCV, and Matplotlib.
