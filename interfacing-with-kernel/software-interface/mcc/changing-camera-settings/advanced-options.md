#Advanced Options

For advanced users, adjust these settings as desired.

##Video Capture Restart Delay: 

This is the time after the last trigger that the live video feed will come back on. This should be set to a duration longer than you are expecting to have between triggering to ensure that the cameras respond as quickly to the trigger signal as possible.

##SD Card Time to Unmount:

In order to save the image to the memory card the Kernel OS has to unmount it in software. So that the camera is able to save a new image as quickly as possible to the card we delay the re-mounting of the card. This setting adjusts the seconds after the image is saved that the camera re-mounts the card. We typically set a value longer than you expect the duration between triggers to be, but know that if it's been longer than this time since the last trigger the cameras will have a slight delay in capturing the new photo. 

If the card is physically removed from the camera while the memory is unmounted, or you send it into Transfer mode, your computer may warn you that there are issues with the card. This typically doesn't affect the stored images, unless the camera was trying to save an image when the card was ejected.

##Photo Format:

While we recommend only saving the images in RAW (.mapir) format to allow for the fastest trigger response, smallest file size and highest fraerate you may choose to save the images instead in the TIFF format.  You will still need to run the images through the Process step to be able to fully use them though.