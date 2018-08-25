# Finding lane line on road
homework.ipynb is described 

## Lane Line Decetion Pipeline Image Processing
### 1 regionMask

### 2 colorSelect

### 3 Edge Feature extraction cannyFilter

low_threshold = 50
high_threshold = 150
    
### 4 hough 

rho = 2 
distance resolution in pixels of the Hough grid

theta = nm.pi/180 
angular resolution in radians of the Hough grid

threshold = 15     
minimum number of votes (intersections in Hough grid cell)

min_line_length = 40 
minimum number of pixels making up a line

max_line_gap = 20    
maximum gap in pixels between connectable line segments

