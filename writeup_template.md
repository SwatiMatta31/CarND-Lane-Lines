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

My pipeline consisted of 5 steps. First, I converted the images to grayscale, then I .... 

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by ...

If you'd like to include images to show how the pipeline works, here is how to include an image: 


![alt ]text[image1]

Algorithm Explanation:
1. Input image is changed to gray scale image.
2. Gaussian bluring is applied.
3. Edges are detected with Canny Edge Detection Algorithm.
4. If the image after edge detection is given directly to line detectio function, then lines will be detected over all image. This would cause unncessary computation and also would result in erroneous line in the final result. Hence region of interest is selected which mask all the unwanted region and apply line detection ony on the selected area.
5. Lines detected afterwards are still too many, so in the end averaging is applied to get one smooth line for each side. The result line is overlayed on color image and displayed.


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when ... 

The results can still be improved as the lines detected are still not continuous.


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to ...

Calculate slope and intercept, which can be used to improve the results.
