##Connecting to Kernel

1) First make sure that you have [proper power connected](../interfacing-with-kernel/hardware-interface/powering-kernel.html) to Kernel and that the USB cable is plugged into your computer.   
2) While the cameras boot (takes a few minutes) you should hear a series of USB connection/disconnection sounds. If you have the live video output connected you can watch the cameras boot.  
3) Once the final USB disconnect sound is heard open the [MAPIR Camera Control (MCC)](../interfacing-with-kernel/software-interface/mcc/installation.html) application, click the Kernel tab at the top and click the Connect button in the top left of the window. The log window will let you know which cameras it has found. If you don't see all the cameras listed in the log then power cycle the cameras and try again.  

![](/assets/kernel_connect.png)

4) The drop-down in the middle labeled "Camera:" allows you to choose which camera you want to control/edit. The settings in the Kernel>Configure tab are **for the selected camera** in the Camera drop-down.
