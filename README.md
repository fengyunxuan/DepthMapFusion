# DepthMapFusion
A depth map fusion algorithm fuses depth maps from different perspectives into a unified coordinate framework and
performs surface calculations to generate dense point clouds of the entire scene.
The existing algorithms ensure the quality of these dense point clouds by 
eliminating inconsistencies between depth maps, but the problem of many redundant calculations often arises. 
In this paper, a depth map fusion algorithm based on pixel region prediction is proposed.
First, the image combination is calculated to select a set of candidate neighbor images for each reference image in the scene.
Second, voxels and measure estimates are constructed on a coarse scale, and an inference strategy and a corrector are proposed 
to merge pixel regions at a fine scale guided by the coarse scale. 
Finally, the deduced pixel regions at the fine scale are used as the image-space constraints for depth fusion. 
Public and actual oblique images datasets are used for experimental verification.
Compared with the famous COLMAP, OPENMVS, Gipuma and ACMP methods, the number of redundant calculations is significantly reduced; 
according to Data1~Data9 in the experiment, as the number of images increases, the fusion efficiency is increased by 47.5% to 156.6%;
at the same time, the point cloud accuracy is comparable to other methods. 
