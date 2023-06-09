# Assignment_AI_Associate
In this assignment 
Task:
Create a program using Computer Vision to track the movement of the balls of
different colors across various quadrants in the video provided. The program
should record the event of each ball entering and exiting each numbered
quadrant. The event data should be recorded in the below format.
Time, Quadrant Number, Ball Colour, Type (Entry or Exit)
Timestamp: consider start of the video as 0 seconds and compute timestamp
based on video duration.
The program should have provisions for feeding a new video and output should
be saved in the local hard disk. Details of which need to be shared at the time of
submission 

#Approach

Task 1: Video Pre-processing : 
Crop and rotate the video to remove unwanted background and align the frames for accurate ball tracking.

Task 2: Ball Detection : 
Develop a function that can detect the presence of balls in each frame of the video.
The function should be able to identify the ball's position.

Task 3: Ball Color Recognition :
Develop a function that can recognize the color of each ball.
The function should be able to differentiate between different colors of balls and provide accurate result.

Task 4: Ball Position Tracking :
Develop a function that can track the movement of each ball and calculate its position in each frame.
The function should be able to identify the quadrant in which the ball is located.

Task 5: Event Detection : 
Develop an function that can detect when a ball crosses its quadrant boundary.
The function should be able to identify the type of event (entry or exit) and the time at which it occurred.

Task 6: Data Storage and Export :
Store the information gathered from the video analysis in a text file.
Write the processed video with the ball tracking information overlaid on the frames.

Please find below result in video.
https://drive.google.com/file/d/1kVwGPF-JA2zxHMVk2P0RNCEYnmF6Wclg/view?usp=sharing

![demo](https://user-images.githubusercontent.com/29145107/229869880-e8ea7d0f-ca98-4acb-b1fa-1460d10125ae.png)



Ball Detection.py is used to show result.

Write video.py  file is used to write result in video and text file.

Information.txt file contain the required file.
# Experiments with different approach
I have been using OpenCV to detect balls in images. Initially, I attempted to use the Hough Circle algorithm, but it did not work well due to factors such as shadows, which made some balls undetectable. I also tried using OpenCV Legacy trackers, but they yielded similar results as the Hough Circle algorithm.

Next, I explored using a convolutional neural network (CNN) to build a ball detection model, but it did not provide the desired level of accuracy. Therefore, I decided to try object detection algorithms, including YoloV3, YoloV4, YoloV5, and YoloV8. Out of these, YoloV8 produced the best results

All tasks were completed successfully, but there was a slight loss in accuracy during ball detection. Therefore, I am  building an persistent object detection model that can more smoothly detect and recognize the balls to improve accuracy.


# Yolov8 Result.
![val_batch1_labels](https://user-images.githubusercontent.com/29145107/231818477-f2e80852-3624-4223-afab-98f6ff2dc4ed.jpg)
