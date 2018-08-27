# Finding lane line on road
homework.ipynb is described 

## Lane Line Decetion Pipeline Image Processing
### Step 1. Invalid Region Masking
A triangle area ,that is closed by bottoms vertex and center on screen, is fixed.

> note: If you not sufficient that Center on screen and more adaptive controll is necessary, Optical-flow or sume solution is better. 

### Step 2. Color Select
White and orange colors are supported. Please adjust variable __white_th__ and __orange_th__.

> note1 : Binalized data is not shape. I think that dilate and erode filters are effective.

> note2 : RGB color selection is depended luminance, I suggest that RBG shold be convert to HSV color.

### Step 3. Edge Feature extraction cannyFilter

low_threshold = 50
high_threshold = 150
    
### Step 4. hough 

rho = 2 
Distance resolution in pixels of the Hough grid

theta = nm.pi/180 
Angular resolution in radians of the Hough grid

threshold = 15     
Minimum number of votes (intersections in Hough grid cell)

min_line_length = 40 
Minimum number of pixels making up a line

max_line_gap = 20    
Maximum gap in pixels between connectable line segments

