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

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps. First, I converted the images to grayscale, then I .... 

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by ...

If you'd like to include images to show how the pipeline works, here is how to include an image: 

![alt text][image1]


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when ... 

Another shortcoming could be ...


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to ...

Another potential improvement could be to ...
