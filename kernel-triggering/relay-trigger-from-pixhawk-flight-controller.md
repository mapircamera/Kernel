#Relay Triggering From Pixhawk Flight Controller

Below is the recommended settings for triggering the Kernel cameras from a GPIO source such as a Pixhawk flight controller.

##Hardware Settings:

Kernel provides a PWM_IN and PWM_OUT pins to assist with triggering the camera's shutter as well as outputting exposure feedback for PPK corrections. The location of the PWM_IN and PWM_OUT pins depends on which cables or breakout boards you're using with Kernel, so please refer to that hardware documentation for more information.

On the Pixhawk we recommend setting up relay triggering. To do this we suggest the following setup:
###PWM_IN = AUX 5 (Pin 54)
###PWM_OUT = AUX 4 (Pin 53)

![](/assets/pixhawk2.jpg)

####Example on Pixhawk2.1:
![](/assets/pix2_pwm.jpg)


##Software Settings: