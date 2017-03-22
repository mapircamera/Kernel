# Sensor Rotation

We offer two different FPC ribbons to connect the Kernel sensor board to the main camera stack: "straight" and 90 degrees "rotated". This allows the sensor board to be rotated 90 degrees if desired.

[INSERT PHOTOS OF FPC RIBBONS]

Each camera is also setup in software to know which direction is "forward" so that images can be automatically rotated/flipped during image capture. Each image also has an EXIF metadata tag to let post processing software know if it was rotated.

When you purchase a Kernel camera or camera rig from MAPIR, we ask you to specify the forward direction the camera will be traveling during capture. You will need to look at the photos below and let us know the letter A, B, C, or D corresponding to the forward direction. If you're purchasing a single camera, it will ask you the letters based on the single camera orientation, and if you're purchasing an array the letters based on the array orientation. This will let us know whether you require an angled or straight FPC sensor board ribbon, and how the camera software should be programmed.

![](/assets/direction_kernel.png)

![](/assets/direction_array.png)