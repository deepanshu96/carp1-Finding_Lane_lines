## Finding Lane Lines on the Road

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Apply the pipeline on the given videos (collection of images)

---

### Reflection

### 1. Pipeline Description

My pipeline consisted of the following steps. 

- First, I converted the images to grayscale to properly extract the lane lines. 

![alt text](https://github.com/deepanshu96/carp1/blob/master/result/gray1.png)

- In the next step I applied Guassian blur to the grayscale image in order to reduce the noise when applying canny transformation to the image.

![alt text](https://github.com/deepanshu96/carp1/blob/master/result/gray2.png)

- Then in the next step I applied Canny transform to the image obtained so far.

![alt text](https://github.com/deepanshu96/carp1/blob/master/result/gray3.png)

- After obtaining the canny tranformed image, I masked the region of interest in which the road lanes were present 
( a trianglular area).

![alt text](https://github.com/deepanshu96/carp1/blob/master/result/gray4.png)

- Finally I applied Hough transform to the masked image in order to detect prominent edge points of the lane line and construct the lane lines on an image with black background.

![alt text](https://github.com/deepanshu96/carp1/blob/master/result/gray5.png)

- After performing all these steps, I merged the final Hough transformed image with the original image in order to get the detected lane lines.

![alt text](https://github.com/deepanshu96/carp1/blob/master/result/gray6.png)

In the Hough transform step, I called draw_lines2() function to calculate lines to the left and right side of the car and calculated the average slope and intersection constant on the left and right lanes respectively. After this I plotted the left and right lanes extrapolating them to the bottom of the image from their point of intersection.

### 2. Identify potential shortcomings with your current pipeline

One potential shortcoming would be what would happen when the lane lines were curved that is the car was travelling on a curved road or taking a sharp turn. 

Moreover the lane line finding pipeline would be difficult to implement if there were more cars on the raod that is high traffic decsity might hinder the image detection process. 

### 3. Suggest possible improvements to your pipeline

A possible improvement would be to use non linear functions in order to detect the lane lines or hop between linear or non linear functions according to the requirements.

More advanced techniques like deep forest or nueral networks could be used in order to detect lane lines accurately.
