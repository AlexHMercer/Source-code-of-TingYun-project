# 1.Run process

**Note: the file reading path needs to be adjusted**	

​	The procedure should be executed in the following order to accomplish the separation of single leaf and the establishment of Hexagonal prism envelope. First run the single leaf separation program, then run the Noise removal program, and finally run the Hexagonal prism envelope program.

## 1.1 Run single leaf separation program

​	Just run the main.m file, and save the results in the Leaf folder.

## 1.2 Run Noise removal program

​	Just run the Noise_removal.m file, and the result is saved in the leaf_cutAgain folder.

## 1.3 Run Hexagonal prism envelope program

​	Run Color.m step_1_drawleafpoint.m, step_2_defineprism.m, step_3_drawprism.m file successively.



# 2. key parameters

**Note: For different trees with variable leaf width and length, many of the following parameters  that control the accuracy of individual leaf segmentation need to be properly adjusted**

## 2.1 parameters in single leaf separation

```matlab
% parameters in findCenterPoint.m
neipointnum = 4 % Threshold for condition judgment,to eliminate the influence of sparse point cloud
range = 0.03 % Half of the side length of a hexahedron with the same side length formed with the current point as the center. The hexahedron should be able to wrap most of the area of a leaf
range1 = 0.03 % The threshold value of the distance between the current point and the calculated center point. When the distance is less than this value, the point is determined as the center point
```

```matlab
% parameters in fun.m
threshold = 0.01 % Cluster radius
```

## 2.2 parameters in Noise removal

```matlab
% parameters in Noise_removal.m
disnear = 0.02 % Cluster radius
numberofpointlimitation = 4 % Minimum number of points in a class
```

