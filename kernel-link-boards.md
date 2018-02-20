#Kernel Link Boards

####Each Kernel module can be customized with various sensors, lenses, and filters as you choose. This allows you to custom build each Kernel and swap them into your array depending on your current project’s requirements.
####Instead of connecting each camera together with bulky cable harnesses, we’ve designed a unique, modular link board system which connect together:

###LinkM: Master Link Board

At the start of an array you will find the master link board (LinkM). On the vehicle connection end it has the same Kernel port found on the Kernel, so all cables and breakout boards work in both port locations. When a Kernel is plugged into the “master” slot of the LinkM it gains special abilities different than the other array locations.

The master location on the LinkM is reserved for the camera you would like to output an HD video feed. All of the link slots support SD analog video out, which can be switched to see the video feeds from each camera. See how to toggle SD feeds in MCC [here](../content/interfacing-with-kernel/software-interface/mcc/capturing-video.html).

###LinkS: Slave Link Board

To connect more than two Kernels to the LinkM you will need to plug in one LinkS for each pair of Kernels you wish to add. Since LinkS boards easily connect to each other, you can build arrays of up to 6 total Kernels. If you need to connect more than 6 Kernels you can combine two LinkM arrays.


###Link Board Power Distribution

It is important to provide enough power to each of the connected Kernel cameras in order for them to function correctly. [Please click here for details on how much power to provide a Kernel array.](../content/interfacing-with-kernel/hardware-interface/powering-kernel.html) There is a 1.67mm barrel port on the LinkM to supply power to. If using the link board power port no power is required to be supplied through the 40pin Kernel port.

If the USB cable is connected and no power cables are powered yet, the array may try and power on only with that USB power input, which will not fully power up the array and you will get a constant connect/disconnect sound from your computer. If using the Kernel Plugs Breakout Board then the USB power wire is not connected and you do not need to worry about this.