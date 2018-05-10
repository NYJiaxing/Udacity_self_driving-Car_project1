# Self-Driving Car Engineer Nanodegree
## Project: **Finding Lane Lines on the Road**

Ensuring vehicle driving within the traffic lanes is the essential requirement for human drivers, however,the vehicle sometimes will departure the lane when driver is tired or texting with mobile phone. Although the Radar or Lidar system help vehicle to identify the front or surrounding objects, it cannot identify the lanes. Therefor, with growing of computer vision techniques, the traffice lanes can be identified easily.

This project is using computer vision techniques, 

* grayscale image transfer 
* canny edge detection
* hough trasfer techniques
* draw the lines on the detected lanes

### Reflection

My pipline consisted of 6 steps. 
* 1. Import the image with help of matplotlib package. 
* 2. Do the gaussian blur to reduce the image noise.
* 3. Transfer this blured image to grayscale image to ready for the Canny edge detection.
* 4. Canny edge detection applied with threshold
* 5. Hough transform applied to detect lines on the image
* 6. Draw lines on the image

One of the hard part of this project is to draw continue line on the identified hough lines. The resolution is calculate the slope of each line, if the slope is minus than zero then the line is identified on the left line, if the slope is greater than zero then the line is identified on the right line. Build a list to store slope of each line in each iteration.

Then using the function of a line y = kx + b to calculate the start point (x1', y1') and start point (x2', y2') of each line. Then use the opencv function to draw the line on the image.

### 2. Identify potential shortcomings with your current pipeline

One potential shortcoming would be the lane detection algorithm only works find on the straight lines not on the challange video. When the line is in a curve, the line looks like a mess.

Second shortcoming is the interested region currently is change by hand which means all the vertices are hyperparameters.

### 3. Suggest possible improvements to your pipeline

A possible improvement would be to using concpet of differential. Separate all the lines in several small pieces (boxes) and find and draw lines in each small box and combine all the small box together to build a line.

Another potential improvement for shortcoming 2 could be to using neural networks to identify the interested regions in the future.
