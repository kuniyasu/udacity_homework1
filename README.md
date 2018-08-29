# Finding Lane Lines on the Road

This is jupyter noitebok code. It is necessary opencv2, numpy and VideoFileClip libraries. Additonally for debugging, you should import matplot library.

![Alt text](./v1.png)

## Lane Line Decetion Pipeline Image Processing
### Step 1. Invalid Region Masking

![reagion](./reagion_image.png)

A triangle area ,that is closed by bottoms vertex and center on screen, is fixed.

> note: If you not sufficient that Center on screen and more adaptive controll is necessary, Optical-flow or sume solution is better. 

### Step 2. Color Select
![select](./select_color.png)

White and orange colors are supported. Please adjust variable _white_th_ and _orange_th_.

> note1 : Binalized data is not shape sometime. I think that dilate and erode filters are effective.

> note2 : RGB color selection is depended luminance, I suggest that RBG shold be convert to HSV color.

### Step 3. Edge Feature Extraction Canny Filter
![canny](./canny_image.png)

Edge data is generated by Binalized data.
_low_threshold_ and _high_threshold_ is adjust variable.
    
### Step 4. Hough Line Detect
![hough](./result_image.png)
 
For lines detection, Hough conversion is used. Adjust variables are shown below.

Distance resolution in pixels of the Hough grid

_rho = 2_ 

Angular resolution in radians of the Hough grid

_theta = nm.pi/180_

Minimum number of votes (intersections in Hough grid cell)

_threshold = 15_

Minimum number of pixels making up a line

_min_line_length = 40_ 

Maximum gap in pixels between connectable line segments

_max_line_gap = 20_


### Step 5. Result
 _result = cv2.addWeighted(lines, 0.8, image, 1, 0)_
 
 It is overlay detect line on source image.
 

## Function Description In Source code
### def colorSelect(image)  
This function can be take whte and orange colors. Those colors are used road line. white_th and orange_th are defined color code.

### def regionMask(image):  
This funtion can cliping image area. Clipped area is defined by left_bottom, right_bottom,and apex .
Clipping Default value are screens edge-bottoms and center.

### def cannyFilter(image):  
This function can be get edge image. We can adjust variable low_threshold's and  high_threshold's  value for filter behavioral.
This function argment shoud be 3 color image.

### def hough(image):  
It is hough line detection function. Return values is drown line vertexes image. 


### def detectLine(image):  
Those defined functions pipeline.

