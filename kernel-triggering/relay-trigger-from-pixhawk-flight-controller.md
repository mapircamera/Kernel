#Relay Triggering From Pixhawk Flight Controller

#####Below is the recommended settings for triggering the Kernel cameras from a GPIO source such as a Pixhawk flight controller.

##Hardware Settings:

Kernel provides PWM_IN and PWM_OUT pins to assist with triggering the camera's shutter as well as outputting exposure feedback for PPK corrections. The location of the PWM_IN and PWM_OUT pins depends on which cables or breakout boards you're using with Kernel, so please refer to that hardware documentation for more information.

On the Pixhawk we recommend setting up relay triggering. To do this we suggest the following hardware setup:
###PWM_IN = AUX 5 (Pin 54)
###PWM_OUT = AUX 4 (Pin 53)

![](/assets/pixhawk2.jpg)

###Example on Pixhawk2.1:

####Purple Wire = PWM_IN
####Green Wire = PWM_OUT
####Black Wires = GROUND
![](/assets/pix2_pwm.jpg)


##Software Settings:

Sending a relay (voltage) spike of 3.3 volts for 2ms is the best way to trigger the Kernel camera. The camera has less chance to miss a trigger because it's looking for any voltage spike for at least 2ms duration.

