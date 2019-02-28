## CSE 167 HW3 Extra Credit Demo
For the extra credit portion, I created a simple 3D modeling system using Bezier and B-Spline curves. Due to limited time was given, the only modeling option implemented is surface of resolution. Users will be able to draw Bezier or B-Spline curve the same way HW3 does and visualize the surface of revolution created by rotating the curve around the y-axis on the second screen. 

### How I create the surface of revolution
I use an array to store points that are used to draw the curve, which are in [0, 1], and transform them to 3D points by adding the z value as 0. Then I create rotation matrices to rotate these points around the y-axis. The number of rotations and degrees to rotate in each rotation is determined by a variable called levelOfDetails. The number of rotations equals to levelOfDetails and the degrees equals to 360.0 / levelOfDetails. To draw these new vertices as a surface, I need to connect them to form a mesh (or wireframe). I won't go too deep but this is how it look:
                
                
                curve_i curve_i+1            
            
                v1------v3
                
                |     /  |
                
                |   /    |
                
                v2------v4
                
Calcuate the normals of these triangles is trivial.       

### Commands to use in the second screen 
* enter - draw the surface of revolution based on the curve in the first window
* "w" - toggle wireframe mode
* "\+" - increase the level of details
* "\-" - decrease the level of details
* "r" - reset the position 
* left arrow- rotate left
* right arrow- rotate right
* up arrow - rotate up
* down arrow - rotate left

### Screenshots
![screenshot1](https://raw.githubusercontent.com/GuangyanCai/CSE167-extra-credit-page/master/screenshot1.png "Screenshot 1")
![screenshot2](https://raw.githubusercontent.com/GuangyanCai/CSE167-extra-credit-page/master/screenshot2.png "Screenshot 2")
![screenshot3](https://raw.githubusercontent.com/GuangyanCai/CSE167-extra-credit-page/master/screenshot3.png "Screenshot 3")


### Video (click the image below)
<a href="https://www.youtube.com/watch?v=qCFOCko1BpU&feature=youtu.be&hd=1
" target="_blank"><img src="http://img.youtube.com/vi/qCFOCko1BpU/0.jpg" 
alt="IMAGE ALT TEXT HERE" width="240" height="180" border="10" /></a>


