GT_Instrutions


Data Format
The tracker file format should be the same as the ground truth file, which is a CSV text-file containing one object instance per line. Each line must contain 10 values:

```
<frame>,
<id>,
<bb_left>,
<bb_top>,
<bb_width>,
<bb_height>,
<conf>,
<x>,
<y>,
<z>
```
  
The world coordinates x,y,z are ignored for the 2D challenge and can be filled with -1. Similarly, the bounding boxes are ignored for the 3D challenge. However, each line is still required to contain 10 values.

All frame numbers, target IDs and bounding boxes are 1-based. Here is an example:

```
1, 3, 794.27, 247.59, 71.245, 174.88, -1, -1, -1, -1
1, 6, 1648.1, 119.61, 66.504, 163.24, -1, -1, -1, -1
1, 8, 875.49, 399.98, 95.303, 233.93, -1, -1, -1, -1
...
```

Mapping Frame Numbers: The frame number in tracking should correspond to the frame number in the ground truth.
Handling Multiple Objects: If there are multiple objects in a frame, both the ground truth and tracking data should reflect this by having multiple entries (rows) for that frame, one for each object.


