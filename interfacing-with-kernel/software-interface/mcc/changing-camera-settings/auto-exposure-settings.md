#Auto Exposure Settings

Auto exposure will sample the exposure of the last 3 frames and adjust the exposure according to the algorithm used. These sampled frames will come from the live video (if currently enabled) or from the last 3 saved images.

![](/assets/auto_settings.PNG)

##EV-Control Mode

EV-Control is the recommended auto exposure algorithm to use as it is typically more accurate.

####Setpoint: 

The setpoint value is what you use to control where on the histogram you would like the exposure to be centered around. The possible values range from 256-2560, with lower values representing the lower end of the histogram (lower pixel values) and higher setpoint values representing higher pixel values.

If you are using the Kernel cameras from an aerial platform (UAS/drone) and with the camera pointing downward (nadir) then you will typically be capturing images during bright, sunny days. 

**In order to reduce the chances that the captured pixels will be over-exposed we recommend the following settings:**

**3.2MP Sensors (Filters <700nm): 768**
**3.2MP Sensors (Filters >700nm): 512**
**14MP Sensors: 512**



####Min Shutter Speed:

####Max Shutter Speed:

####F Stop:

####Max ISO:

##P-Controller Mode



####P Controller Gain:

