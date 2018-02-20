#Auto Exposure Settings

Auto exposure will sample the exposure of the last 3 frames and adjust the exposure according to the algorithm used. These sampled frames will come from the live video (if currently enabled) or from the last 3 saved images.

![](/assets/auto_settings.PNG)

##EV-Control Mode (Recommended)

The EV-Control algorithm works by trying to achieve a target overall brightness setpoint, which is usually a medium gray level. It measures the setpoint by calculating the average gray level in the image (for the entire image). 

This EV-based iterative approximation uses the formula:
```
EV(n+1) = EVn + log2(BLn) - log2(BL_desired)
```
Where BL_desired is the target brightness level (setpoint) and EV is the actual reflected light intensity value of the scene as used in photography (EV ~ log2(F^2/t)), where F is the aperture f-stop and t is the exposure time. The algorithm deducts the EV and finds the optimum shutter time at the minimum gain. If the shutter is too slow (below Max Shutter Speed), it will increase the gain and speed up the shutter to maintain exposure while achieving the shutter speed threshold. 

####Setpoint: 

The setpoint value is what you use to control where on the histogram you would like the exposure to be centered around. The possible values range from 256-2560, with lower values representing the lower end of the histogram (lower pixel values) and higher setpoint values representing higher pixel values.

If you are using the Kernel cameras from an aerial platform (UAS/drone) and with the camera pointing downward (nadir) then you will typically be capturing images during bright, sunny days. So you will want to have the setpoint quite low.

**In order to reduce the chances that the pixels will be over-exposed during full sun capture we recommend the following settings:**

3.2MP Sensors (Filters Lower Than 700nm): **768**  
3.2MP Sensors (Filters Higher Than 700nm): **512**  
14MP Sensors: **512**  

####Min Shutter Speed:

You can adjust this how you like, but the default of 1/32000 should work well.

####Max Shutter Speed:

This is the main value that the auto exposure is going to adjust based on the setpoint you set. With shutter speeds, the smaller the number in the fraction (i.e. the 250 in 1/250) the longer or slower the shutter will be (stay open). The longer it stays open the more light gets captured by the sensor.

By setting the max shutter speed value you are instructing the algorithm that you do not want it to expose for longer than you want. The main reason to do this is due to movement. If the camera is moving quickly over its subject matter there is a limit to how long you can leave the shutter open before you get unwanted pixel blur. Please use our flight calculator at the bottom of the page [here](https://www.mapir.camera/pages/cameras) and look at the value towards the bottom labeled "Min Shutter S 1/X s". You want to set a higher X value in this "Max Shutter Speed" setting than the flight calculator provides you.

**We recommend the following settings depending on the sensor being used (you can adjust as desired):**

3.2MP Sensors: **1/250**  
14MP Sensors: **1/500**  

#####Note: Due to the way the 14.4MP Kernel sensor is triggered to insure synced exposures in an array you may experience large portions of the captured media having over-exposed pixels if the shutter speed is not set to 1/500s or faster (i.e. 1/1000s).

####F Stop:

Match the F-stop value as close as possible to the f-stop (aperture) of the lens you are using. More information [here](https://mapircamera.gitbooks.io/kernel-development-guide/content/kernel-lenses.html).

####Max ISO:

Having a high ISO means more image noise, which is not preferred. So only set this value as high as necessary.

The defaults we typically set for ISO:

3.2MP Sensors: **400**  
14MP Sensors: **800**  

##P-Controller Mode
![](/assets/p-control.PNG)

The [proportional control algorithm](https://en.wikipedia.org/wiki/Proportional_control) controls the level of mean brightness level of a captured frame. The mean brightness level calculation is done on the FPGA chip in real-time. The averaging is done on the entire frame, with no possibility of adjusting the area. The P controller is constantly adjusting sensor exposure time (on each frame). The sensor gain is only changed if the sensor exposure time limit has been reached. The controller is trying to keep sensor gain as low as possible in order to reduce sensor noise. 

Before the P controller, there is a hysteresis and moving average filter block (see diagram above), it is used to reduce the oscillations of the system, when the error signal is very small (error signal = set-point – signal from FPGA). The error signal is filtered with moving average filter with depth of 3. If the error signal is small no new calculation of sensor exposure time and gain is made, the previous values are applied instead. The P controller input signal is a mean brightness level error signal. After the P controller, there is an output saturation block, it is used to limit how high the output signal from the P controller can be. The P controller output signal is an exposure time in nanoseconds.

The feedback loop will produce the following result for the next frame, depending on the current frame results:
```
P_output(t+1) = AE_Gain x (AE_setpoint - FrameMeanBrightness(t))
```
```
FrameMeanBrightness(t+1) = Sensor_Gain(t) x (exposure_time(t) + P_output(t+1))
```
####Setpoint: 

This value sets the mean brightness level (gray) that the camera will attempt to capture.

**In order to reduce the chances that the pixels will be over-exposed during full sun capture we recommend the following settings:**

3.2MP Sensors (Filters Lower Than 700nm): **768**
3.2MP Sensors (Filters Higher Than 700nm): **512**
14MP Sensors: **512**

####P Controller Gain:

Gain values represent how quickly the exposure will be adjusted. We recommend setting as low a value as possible.

#####All options besides setpoint and p-controller gain do not affect exposure if the P-Controller option is selected.
