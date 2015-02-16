# IO Cape
### A simple BeagleBone Black Cape extending the pwm and GPIO pins with an i2c ADC chip for 5V ADC input (ADS7828) in KiCad

This board also has a connection designed for a proprietary 9 axis board using Bosch BMX055 using i2c interface

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