#Kernel GPS (Zubax GNSS 2)

![](/assets/Zubax GNSS 2 - Titan Elite 3 copy-500x500.jpg)

While any UAVCAN supporting GPS/GNSS can be used, we offer the reliable and high quality Zubax GNSS 2 as an optional accessory on our store. With this GPS unit plugged into Kernel (individual cameras and arrays) you will get automatic geo-tagging to each captured image.

###Purchase Zubax GNSSS 2 on MAPIR store  
###[Zubax GNSS 2 DATASHEET](https://files.zubax.com/products/com.zubax.gnss/Zubax_GNSS_2_Datasheet.pdf)  
###[Zubax manufacturer website for GNSS 2 part](https://shop.titaneliteinc.com/index.php?route=product/product&search=zubax%20gnss&product_id=987)  


##Configuring Zubax GNSS 2 For Direct Kernel Camera Geo-Tagging

When you purchase the Zubax GNSS 2 from our MAPIR store, we have already changed the UAVCAN Node ID to a value of 5 (defualt is 0) so that you can connect the GNSS directly to Kernel. If you are connecting the GNSS to an autopilot such as the Pixhawk (2/1) you will want to change it back to 0 by following the below directions. The autopilot will dynamically assign it a node ID. If you have purchased the Zubax GNSS 2 from a different supplier, then use the below information to change the Node ID value to something other than the default (0) or Kernel's default value (16).

*The following directions are for Windows OS setup. Please see [Zubax's website](https://kb.zubax.com/display/MAINKB/CLI+client+software) for Linux and Mac OS setup.

###Step 1: [Download and install PuTTY](https://kb.zubax.com/download/attachments/2195531/putty-0.70-installer.msi?version=1&modificationDate=1500123860744&api=v2)

###Step 2: Plug a micro USB cable into the Zubax GNSS 2 unit and into your computer. Verify that the RED Status LED begins to blink. Make note of which COM port the device is plugged into. To find the COM port, go to Device Manager and look in the Ports (COM & LPT) for the USB Serial Device, followed by (COM4), or whatever COM it lists.

###Step 3: Start PuTTY. Under "Connection Type" select the Serial button on the right. Enter the COM port identified in the previous step. Change speed to 115200 if it isn't already. It should look like this:
![](/assets/put.PNG)

###Step 4: Click the Open button, and a command window will pop up. (A list of the available parameters can be found in page 13 of the [Zubax GNSS 2 datasheet](https://files.zubax.com/products/com.zubax.gnss/Zubax_GNSS_2_Datasheet.pdf).)

###Step 5: Type the following and hit enter:
```
cfg list
```
###Step 6: Find the value uavcan.node_id and check the value. If it is something other than 0, then the GNSS should work fine when connected directly to the Kernel cameras. If you are using it with an autopilot, leave it on 0 as the autopilot will dynamically assign a node ID to the GNSS.

###Step 7: If the value is 0, then enter the following text and hit enter:
```
cfg set uavcan.node_id 5
```
###Step 8: Type cfg list again to verify the node_id value has been changed.

###Step 9:  Your Zubax GNSS 2 is now setup to connect directly to Kernel and provide automatic geo-tagging to the captured images.

