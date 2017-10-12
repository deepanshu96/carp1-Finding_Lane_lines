
---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Apply the pipeline on the given videos (collection of images)

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps. 

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

In the Hough transform step, 

### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when ... 

Another shortcoming could be ...


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to ...

Another potential improvement could be to ...
