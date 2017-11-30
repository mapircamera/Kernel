#Updating Kernel Camera Stack Firmware

The Kernel camera stack is the 3 main circuit boards of the camera (not including the sensor board). The main camera may require periodic firmware updates to provide access to the newest features or performance improvements. Below are the instructions to update the camera firmware:

##Powering the Camera On in Boot Mode

To load new firmware onto the camera you will need to connect to the 40pin Kernel port and put 0ohm resistors on both pin 1 (BM0) and pin 5 (BM1).

![](/assets/dip.PNG)

If you are using our [Plugs Breakout Board](https://www.mapir.camera/collections/kernel-accessories/products/kernel-plugs-breakout-board-kernel-40pin-port) then simply move both dip switches to the side opposite the 1 and 2 numbers, as this photo demonstrates:

![](/assets/dip_comp.jpg)

Connect the camera to a 5 volt power source and it will be ready to load new firmware on.

##Loading New Firmware Onto the Camera

1: Download the following package that corresponds to the sensor you are using:

[3.2MP Sony IMX265LLR-C](http://mapir.peauproductions.com/kernel_firmware/kernel_firmware_imx265.zip)
[14.4MP On Semiconductor MT9F002](http://mapir.peauproductions.com/kernel_firmware/kernel_firmware_mt9f.zip)
    
2: Extract the contents of the downloaded folder.

3: Power the camera on with 5VDC and plug the camera's USB cable into your computer.

4: Launch the MfgTool2.exe program

5: The window should look like this image. Make sure the text "HID-compliant vendor-defined device" is present. If it is not, then the application cannot detect the camera. Please power off the camera, remove the USB and repeat the steps above.

![](/assets/mfg.PNG)

6: Press the Start button.

7: After a minute or so you will likely see something like the below screen, which you can simply click the Cancel button to ignore.

![](/assets/mfg2.PNG)

8: Let the program proceed with the firmware upgrade, it will likely take up to 5-10 minutes.

![](/assets/mfg3.PNG)

9: Once you see the green bars then the update was successful. Press the Stop button and then the Exit button. The camera's firmware is now updated.

![](/assets/mfg4.PNG)

*If you see red bars then something happened during the install. Please disconnect everything and try again. Be careful not to bump the camera during updating such that the connection becomes interrupted.

![](/assets/mfg5.PNG)
