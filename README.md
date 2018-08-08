# Finding Lane Lines on the Road

This is jupyter noitebok code. It is necessary opencv2, numpy and VideoFileClip libraries. Additonally for debugging, you should import matplot library.

![Alt text](/test.jpg)

## Function Description
### def colorSelect(image)  
This function can be take whte and orange colors. Those colors are used road line. white_th and orange_th are defined color code.

### def regionMask(image):  
This funtion can cliping image area. Clipped area are defined by left_bottom, right_bottom,and apex .
Clipping Default value are screens edge-buttom and center.

### def cannyFilter(image):  
This function can be get edge image. We can adjust variable low_threshold's and  high_threshold's  value for filter behavioral.
This function argment shoud be 3 color image.

### def hough(image):  
It is hough line detection function. Return values is drown line vertexes image. 


### def detectLine(image):  
Those defined functions pipeline.





