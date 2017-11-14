####Each Kernel module can be customized with various sensors, lenses, and filters as you choose. This allows you to custom build each Kernel and swap them into your array depending on your current project’s requirements.
####Instead of connecting each camera together with bulky cable harnesses, we’ve designed a unique (patent pending) link board system:

###LinkM: Master Link Board

At the start of an array you’ll find the LinkM. On the vehicle connection end it has the same Kernel port found on the Kernel, so all cables and breakout boards work in both port locations. When a Kernel is plugged into the “master” slot of the LinkM it gains special abilities different than the other array locations.

Since HDMI is difficult to pass between boards without signal issues, and would require essentially a dedicated HDMI switch to function properly, the master slot is reserved for the camera you would like to output an HD video feed. The rest of the link slots support SD analog video out, which can be switched to see the video feeds from each camera. See how to toggle SD feeds in MCC [here](../content/interfacing-with-kernel/software-interface/mcc/capturing-video.html).

###LinkS: Slave Link Board

To connect more than two Kernels to the LinkM you’ll need to plug in one LinkS for each pair of Kernels you wish to add. Since LinkS boards easily connect to each other, you can build arrays of up to 6 total Kernels. If you need to connect more than 6 Kernels you can combine two LinkM arrays.


###Link Board Power Distribution

Due to the fact that each Kernel is essentially a small, yet powerful Linux computer, the power draw of 3.25 watts (max) per Kernel at 5.0 VDC is a bit much to distribute across the theoretical 6 link boards limit mentioned above. The power options are as followed based on the number of cameras connected:

**1-2 Cameras: Power from Kernel Port or 1.65mm Barrel Plug (on Master Link Board)**

**3-5 Cameras: Power from 1.65mm Barrel Plug Required**

**6 Cameras: Power from both Kernel Port and 1.65mm Barrel Plug Required**  

It is very important to apply power to both the Kernel port and the 1.65mm barrel plug **at the same exact time** if required based on the number of cameras connected. If you don't power the ports on at the same time you may find that one or more cameras will not power on with the rest of the array. Also, if the USB cable is connected and no power cables are powered yet, the array may try and power on only with that USB power input, which will not fully power up the array and you will get a constant connect/disconnect sound from your computer.