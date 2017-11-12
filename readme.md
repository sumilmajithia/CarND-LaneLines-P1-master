# **Finding Lane Lines on the Road** 


---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report

---

**Contents in the Submited ZIP file**
* P1-Submit
* readme
* test_videos
* test_videos_output

---

**Steps on running the file**

* Unzip the given Zip File
* Run the file P1-Submit.ipynb on Jupyter Notebook
* The test videos are in the folder test_videos
* Output of those videos are in the folder test_videos_output

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

**My pipeline consisted of 5 steps**

* Step 1 was to convert the image into grayscale
* Blurring theimage using Gaussian Blur
* Detecting the edges using Canny Edge Detection
* Creating a region of Mask
* Using Hough Transform to get lines from points
* Finding the inliers and out liers of those lines and catergorizing them into left and right
* finding the mean slope and intercept of those inliers and plotting them finally onto the orginal image



### 2. Identify potential shortcomings with your current pipeline
* The pipeline doesnt work with shadows folllowing on the road.
* The Pipeline will only work with camera position fixed on the car. You have to change the region of mask if you change the camera position.
* It wont work on roads with no lane markers or poor quality of lane markers
* It may not work if there are other cars in the region of mask.
* It will oonly work on highways where there are less possible distractions


### 3. Suggest possible improvements to your pipeline

* A possible improvement would be to have a very linited region of mask. The Masking region should only surround the lanes lines nothing between it or nothong beyond it.

* They only detect straight lines. We should be able to make they those lines curved too.
*  Able to extrapolate the lanes lines if there is a discontinuity in detecting the lines.