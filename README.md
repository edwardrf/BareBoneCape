# IO Cape
### A simple BeagleBone Black Cape extending the pwm and GPIO pins with an i2c ADC chip for 5V ADC input (ADS7828) in KiCad

This board also has a connection designed for a proprietary 9 axis board using Bosch BMX055 using i2c interface

I am sorry for the poor quality and poor documentation for this project, this is largly due to my lazyness technical inability.

Note: even though the lib i created is named txb0108b, the actual chip we used is TXS0108E, which supports both open-drain (for i2c) and push-pull (for uart) devices.

####*WARNING: DO NOT BUILD THE BOARD*
For the master branch, we have manufactured one, and realized BBB will not boot with this cape on, we had to boot bbb and then put the cape to boot the device correctly. After some testing, it seems the way I powered up the devices are over simplified, which results in unexpected behavior in the buffer chips during boot up and some of the chips are connected to the pins which are shared with the SYS_BOOT and  EMMC pins, specificly, the P8_31 to P8_46. This board boots with SD card with no problem though.
We will fix these issues soon. We will keep develop the master branch as a general IO expansion board for BBB and in the mean time ...

### Plane version ###
We are creating a newer version which is designed for our flight controller (in the plane branch), this new version would be less general, but some of the main features are:
* Embedded ATmega328p for some low level processing and take over the control when BBB is not available
* builtin BMX055 (9 axis)  and BMP180 (barometer)  chips on i2c bus 2 (i2c2)
* PCA9685 as the PWM output driver which would give us more precision, more PWM output channels and maintain output when BBB is not available.

![Simple Cape](beaglebone-cape-front.png)

## Pin Mapping

* Buffer #0  on the right top

|   Name    |   BeagleBone Pin ID   | GPIO  	|
|-----------|-----------------------|-----------|
|	D70		|	P8_45				|GPIO2_6	|
|	D71		|	P8_46				|GPIO2_7	|
|	D72		|	P8_43				|GPIO2_8	|
|	D73		|	P8_44				|GPIO2_9	|
|	D74		|	P8_41				|GPIO2_10	|
|	D75		|	P8_42				|GPIO2_11	|
|	D76		|	P8_39				|GPIO2_12	|
|	D77		|	P8_40				|GPIO2_13	|

* Buffer #1 on the left

|   Name    |   BeagleBone Pin ID   | GPIO  	|
|-----------|-----------------------|-----------|
|	P9_31	|	P9_31				|		|
|	P9_29	|	P9_29				|		|
|	P9_14	|	P9_14				|		|
|	P9_16	|	P9_16				|		|
|	P9_19	|	P9_19				|		|
|	P8_13	|	P8_13				|		|
|	P9_42	|	P9_42				|		|
|	P9_28	|	P9_28				|		|

* Buffer #2 on the middle

|   Name    |   BeagleBone Pin ID   | GPIO  	|
|-----------|-----------------------|-----------|
|	D32		|	P8_25				|GPIO1_0	|
|	D33		|	P8_24				|GPIO1_1	|
|	D34		|	P8_5				|GPIO1_2	|
|	D35		|	P8_6				|GPIO1_3	|
|	D36		|	P8_23				|GPIO1_4	|
|	D37		|	P8_22				|GPIO1_5	|
|	D38		|	P8_3				|GPIO1_6	|
|	D39		|	P8_4				|GPIO1_7	|