# ARPaint

ARPaint demonstrates how to draw in the air with bare fingers using ARKit and Vision libraries introduced in iOS 11.

[Watch Demo Video Here](https://media.giphy.com/media/xThta1PpzDiyPJkt0Y/giphy.gif)

## How it works 

ARKit Immersion Features
ARKit provides two main features; the first is the camera location in 3D space and the second is horizontal plane detection. To achieve the former, ARKit assumes that your phone is a camera moving in the real 3D space such that dropping some 3D virtual object at any point will be anchored to that point in real 3D space. And to the latter, ARKit detects horizontal planes like tables so you can place objects on it.

So how does ARKit achieve this? This is done through a technique called Visual Inertial Odometry (VIO). Don’t worry, just like entrepreneurs find their pleasure in the number of giggles you giggle when you figure out the source behind their startup name, researchers find theirs in the number of head scratches you do trying to decipher any term they come up with when naming their inventions - so let’s allow them to have their fun, and move on.

VIO is a technique by which camera frames are fused with motion sensors to track the location of the device in 3D space. Tracking the motion from camera frames is done by detecting features, or, in other words, edge points in the image with high contrast - like the edge between a blue vase and a white table. By detecting how much these points moved relative to each other from one frame to another, one can estimate where the device is in 3D space. That is why ARKit won’t work properly when placed facing a featureless white wall or when the device moves very fast resulting in blurred images.

## Getting Started

ARKit is available on any iOS 11 device, but the world tracking features that enable high-quality AR experiences require a device with the A9 or later processor.
