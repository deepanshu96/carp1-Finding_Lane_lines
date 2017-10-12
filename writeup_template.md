# **Finding Lane Lines on the Road** 

## Writeup Template

### You can use this file as a template for your writeup if you want to submit it as a markdown file. But feel free to use some other method and submit a pdf if you prefer.

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps. 

- First, I converted the images to grayscale to properly extract the lane lines. 

![alt text](https://github.com/deepanshu96/carp1/blob/master/result/gray1.png)

- In the next step I applied Guassian blur to the grayscale image in order to reduce the noise when 

applying canny transformation to the image.

![alt text](https://github.com/deepanshu96/carp1/blob/master/result/gray2.png)

- Then in the next step I applied Canny transform to the image obtained so far.

![alt text](https://github.com/deepanshu96/carp1/blob/master/result/gray3.png)

- After obtaining the canny tranformed image, I masked the region of interest in which the road lanes were 

present ( a trianglular area).

![alt text](https://github.com/deepanshu96/carp1/blob/master/result/gray4.png)



In order to draw a single line on the left and right lanes, I modified the draw_lines() function by ...

If you'd like to include images to show how the pipeline works, here is how to include an image: 

![alt text][image1]


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when ... 

Another shortcoming could be ...


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to ...

Another potential improvement could be to ...
