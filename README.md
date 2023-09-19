# B-Pose: Bayesian Deep Network for Camera 6-DoF Pose Estimation from RGB Images

Here, we introduce, B-Pose, a Bayesian Convolutional deep network capable of not only automatically estimating the camera's pose parameters from a single RGB image but also providing a measure of uncertainty for the estimated parameters. BPose is published in  [IEEE Robotics and Automation Letters](https://ieeexplore.ieee.org/abstract/document/10242363)

P.S. This code is built on top of the [DSAC*](https://github.com/vislearn/dsacstar).

## Introduction
![image](https://github.com/arekavandi/BPose/assets/101369948/237dc923-1ae8-4e52-937b-346e822fa602)
+ BPose takes an RGB image (and optional 3D point cloud) and returns pose parameters of the camera with associated uncertainty.
+ BPose adopts the DSAC* method as the core end-to-end module and uses Bayesian Neural Nets in the last layers to make a Bayesian prediction.
+ The Samling is performed on the weights of the last layers and several scene coordinate estimations have been obtained.
+ The pose estimation and refinement have been performed for all scene coordinates.
+ The final pose is the mean of all estimated poses and the uncertainty is the associated variance of estimations.
