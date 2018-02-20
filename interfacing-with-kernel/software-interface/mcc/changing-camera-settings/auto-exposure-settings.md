#Auto Exposure Settings

Auto exposure will sample the exposure of the last 3 frames and adjust the exposure according to the algorithm used. These sampled frames will come from the live video (if currently enabled) or from the last 3 saved images.

![](/assets/auto_settings.PNG)

##EV-Control Mode

EV-Control is the recommended auto exposure algorithm to use as it is typically more accurate.

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

####F Stop:

Match the F-stop value as close as possible to the f-stop (aperture) of the lens you are using. More information [here](../content/kernel-lenses.html).

####Max ISO:

Having a high ISO means more image noise, which is not preferred. So only set this value as high as necessary.

The defaults we typically se
t for ISO:

3.2MP Sensors: **400**
14MP Sensors: **800**

##P-Controller Mode



####P Controller Gain:

