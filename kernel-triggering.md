##Kernel Triggering

####For the most reliable triggering of a Kernel camera we recommend the following or slower frame-rates:

| **Kernel Sensor** | **Image Format**| **Configuration**    |**Frame-rate** |**Seconds Between Triggers** |
|-----------------------|-----------------|-----------------|-----------------|
| 3.2MP                | TIFF | Single Camera    | 2.00 fps    | 0.50 seconds|
| 3.2MP                | TIFF | Array Camera    | 1.11 fps    | 0.90 seconds|
| 14.4MP                | RAW | Single Camera    | 1.00 fps | 1.00 seconds|
| 14.4MP                | RAW | Array Camera    | 3.00 fps| 1.00 seconds|

The Kernel cameras can be used in two main configurations: **separate** or **in an array with the link boards**. How they are arranged may affect the rate at which they can be triggered. The SD card speed as well as some camera settings can also affect the trigger response.

###Sending a Trigger Signal to Kernel

In the Kernel tab of [MAPIR Camera Control (MCC)](../content/interfacing-with-kernel/software-interface/mcc.html) a user can set the camera to respond to either a relay (recommedned) or PWM trigger.

**Relay (Voltage) Trigger (RECOMMENDED, DEFAULT):** sending a voltage spike of 3.3 volts for 2ms is the best way to trigger the Kernel camera. The camera has less chance to miss a trigger because it's looking for any voltage spike for at least 2ms duration. Please see our guide [HERE](../content/kernel-triggering/relay-trigger-from-pixhawk-flight-controller.html)
 for setting up the relay triggering on a Pixhawk or similar flight controller.

**PWM Trigger:** This method of triggering requires the camera to measure the pulse width and thus has a slightly higher chance of the camera missing a trigger event if the duration between triggers is too short. Since it is measuring the width, it does allow you to send different duration signals, and thus perform more than just the one trigger function.

| **PWM Signal Length** | **Function**    |
|-----------------------|-----------------|
| 1000ms                | Stop Shutter    |
| 1350ms                | Neutral (No Function)    |
| 1650ms                | Change Capture Mode  |
| 2000ms                | Start Shutter    |

###Separate Kernels (No Link Boards):

When the Kernel camera is not connected to a link board then it will directly respond to a trigger signal. The camera does not have to check with other cameras whether it should keep triggering when a new signal is received since there is no camera-to-camera communication like there is with the link boards. This can lead to issues though if you are indeed using multiple cameras and one camera takes just slightly longer than the others to save the image before the next trigger comes in. This will lead to the exposures not being synced, causing issues with aligning the images in post processing.

###Kernels Connected to Link Boards:

One of the main features of the link boards is to ensure that the various cameras connected all expose the scene at the exact same moment in time. **The link boards act as the gate-keepers for trigger distribution.** They do this by using the PWM-OUT exposure signals to know whether each camera has finished exposing for the previous image prior to sending a new trigger. The master camera then sends its PWM-OUT signal out of the master link board so that a user can use it for array exposure detection (for PPK logging for instance).   

This is important to make sure that no camera is still capturing the previous image before having all the cameras in the array capture the next image. The one issue with this is that since we do not queue the trigger events (to ensure exposure sync) that there is a chance to miss a trigger if a new trigger signal arrives while one or more of the cameras are still saving the previous images. So be mindful of how you plan your triggering to reduce the chances that a trigger will be missed.

###Kernel MicoSD Memory Speed

The speed that the memory card can save the image directly affects the capture rate. We recommend only using the fastest memory cards available to have the most reliable triggering with Kernel. We sell the fastest cards we have found on our store [here](https://www.mapir.camera/collections/kernel-accessories).

###Kernel Settings that Affect Capture Speed

With Kernel you have a lot of settings that you can adjust, but some of them will directly affect the trigger reliably.  

**SD Card Unmount Time:** in order to save the image to the memory card the Kernel OS has to unmount it in software. So that the camera is able to save a new image as quickly as possible to the card we delay the re-mounting of the card. This setting adjusts the seconds after the image is saved that the camera re-mounts the card. We typically set a value longer than you expect the duration between triggers to be, but know that if it's been longer than this time since the last trigger the cameras will have a slight delay in capturing the new photo.  

If the card is physically removed from the camera while the memory is unmounted, or you send it into Transfer mode, your computer may warn you that there are issues with the card. This typically doesn't affect the stored images, unless the camera was trying to save an image when the card was ejected.

**Video Delay Time:** this is the time after the last trigger that the live video feed will come back on. This is also set to a duration longer than you are expecting to have between triggering to ensure that the cameras respond as quickly to the trigger signal as possible.